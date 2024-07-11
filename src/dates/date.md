As a beginner one of the most interesting topics you’ll learn are Dates. Even though it might sound a bit boring, it's one of the key things you might know; from your Database, API, GUI, and more learning how to deal with dates properly is a key factor in writing good applications. 

# Before we start
An important detail you must remember is Java was rushed for the web, thus you have a lot of quirky and somewhat stupid ways to do stuff. The goal of this guide will be to teach you how to use the latest Java APIs to write efficient good code. I’ll aim to teach you how not to code anything hard and rather use standardized ISO for a scalable application. 

# How to work with Dates
## The Date API 

As of `Java 8 SE` with the release of the [Date Class](https://docs.oracle.com/javase/8/docs/api/java/util/Date.html) defined as:
> The class `Date` represents a specific instant in time, with millisecond precision.

Also further on we had the addition of the [Abstract Calender Class](https://docs.oracle.com/javase/8/docs/api/java/util/Date.html) (with significant upgrade with JDK 1.1) defined as:
> The `Calendar` class is an abstract class that provides methods for converting between a specific instant in time and a set of [`calendar fields`](https://docs.oracle.com/javase/8/docs/api/java/util/Calendar.html#fields) such as `YEAR`, `MONTH`, `DAY_OF_MONTH`, `HOUR`, and so on, and for manipulating the calendar fields, such as getting the date of the next week. An instant in time can be represented by a millisecond value that is an offset from the _Epoch_, January 1, 1970 00:00:00.000 GMT (Gregorian).

As noted by the [Oracle docs](https://docs.oracle.com/javase/8/docs/api/java/util/Calendar.html) the reason was the lack of internationalization abilities.

*It’s good to note that the same documentation linked above goes into further detail about its timing if it interests you.*
## The LocalDate API 
Also with `Java 8 SE` came the [LocalDate Class](https://docs.oracle.com/javase/8/docs/api/java/time/LocalDate.html) which is referred to: 
> A date without a time-zone in the ISO-8601 calendar system, such as `2007-12-03`.
> `LocalDate` is an immutable date-time object that represents a date, often viewed as year-month-day. Other date fields, such as day-of-year, day-of-week and week-of-year, can also be accessed. For example, the value "2nd October 2007" can be stored in a `LocalDate`.

An important specification to take note of is:
> This class does not store or represent a time or time zone. Instead, it is a description of the date, as used for birthdays. It cannot represent an instant on the timeline without additional information such as an offset or time zone.
## Difference & Which one to use 
#### Issues with the Date/Time API’s 
Further reading the [LocalDate](https://docs.oracle.com/javase/8/docs/api/java/time/LocalDate.html) class will lead you to “This class is immutable and thread-safe.” This brings us to our first problem.
- Both the [Date](https://docs.oracle.com/javase/8/docs/api/java/util/Date.html) and [Calender](https://docs.oracle.com/javase/8/docs/api/java/util/Calendar.html) were not thread-safe. If you're a bit confused as to what it means - Threads are a way to implement concurrency with a computer application this allows for multiple tasks to be running concurrently rather than sequentially (If you have a programming background you can see this as `async`). 
- Another issue with the Date/Calender API was its poor design. Later on, it was revamped to be ISO-centric (If you are a bit lost on what this whole ISO thing is; in short ISO stands for “International Organization for Standardization”) And we will see the added benefits of this later on.
- And lastly coming back to the lack of internationalization was that developers were required to write their logic for handling different time zones which can result in a lot of faults as miss-matches.

#### The actual difference
The biggest difference is despite the name [Date](https://docs.oracle.com/javase/8/docs/api/java/util/Date.html) would store both time and date (as mentioned by the docs with millisecond offset since epoch - we’ll talk about epoch later on). With the newer API, we get access to easier Formatting/Parsing/Manipulation of Dates.

#### What if I want to store time as well?
Well Java has you covered there as well with their [LocalDateTime Class](https://docs.oracle.com/javase/8/docs/api/java/time/LocalDateTime.html) 
> A date-time without a time-zone in the ISO-8601 calendar system, such as `2007-12-03T10:15:30`.
> `LocalDateTime` is an immutable date-time object that represents a date-time, often viewed as year-month-day-hour-minute-second. Other date and time fields, such as day-of-year, day-of-week and week-of-year, can also be accessed. Time is represented by nanosecond precision. For example, the value "2nd October 2007 at 13:45.30.123456789" can be stored in a `LocalDateTime`.

If you would **only want to store time** then you can use the [LocalTime Class](https://docs.oracle.com/javase/8/docs/api/java/time/LocalTime.html)

#### Quick little recap and use cases
| Name                                                                                    | Should Use | Use Case               | Example                      |
| --------------------------------------------------------------------------------------- | ---------- | ---------------------- | ---------------------------- |
| [LocalDate](https://docs.oracle.com/javase/8/docs/api/java/time/LocalDate.html)         | ✅          | Interprating Dates     | 2021-02-28                   |
| [LocalTime](https://docs.oracle.com/javase/8/docs/api/java/time/LocalTime.html)         | ✅          | Interprating Time      | 19:32:25.457826              |
| [LocalDateTime](https://docs.oracle.com/javase/8/docs/api/java/time/LocalDateTime.html) | ✅          | Interprating Time/Date | 2021-02-28T19:32:25.457826.  |
| [Date](https://docs.oracle.com/javase/8/docs/api/java/util/Date.html)                   | prefer not  | Represents Time        | Tue Jul 12 18:35:37 IST 2016 |

# LocalDate

Now that we have a good understanding of its background and what we can do with it, let's explore the methods of the [LocalDate](https://docs.oracle.com/javase/8/docs/api/java/time/LocalDate.html) class.

## ISO 8601
>The ISO-8601 calendar system is the modern civil calendar system used today in most of the world. It is equivalent to the proleptic Gregorian calendar system, in which today's rules for leap years are applied for all time. For most applications written today, the ISO-8601 rules are entirely suitable. However, any application that makes use of historical dates, and requires them to be accurate will find the ISO-8601 approach unsuitable.

This is the standard Java will use to properly format our dates.

## Temporal
Before we do a deep dive I want to introduce you to the [Temporal object](https://docs.oracle.com/javase/8/docs/api/java/time/temporal/Temporal.html) which all of the new Date APIs implement (LocalDate, LocalTime, LocalDateTime) it's defined as:
> This is the base interface type for date, time, and offset objects that are complete enough to be manipulated using plus and minus. It is implemented by those classes that can provide and manipulate information as [fields](https://docs.oracle.com/javase/8/docs/api/java/time/temporal/TemporalField.html "interface in java.time.temporal") or [queries](https://docs.oracle.com/javase/8/docs/api/java/time/temporal/TemporalQuery.html "interface in java.time.temporal"). See [`TemporalAccessor`](https://docs.oracle.com/javase/8/docs/api/java/time/temporal/TemporalAccessor.html "interface in java.time.temporal") for the read-only version of this interface.

Not going into depth into this just wanted you guys to understand what this is if you encounter it.

## Methods 
The format for this will be in order - The method name, the specified return description, and a quick summary of what it does/or an in-depth dive. If you want to follow along I’m going to use `jshell` just import `java.time.LocalDate` and copy the same methods.

##### `LocalDate.now()`: > the current date using the system clock and default time-zone, not null
> As mentioned by the description it will return the current date format based on time zone as example for me it gives `2024-07-10` however the format might change based on your locale time dependent on the ISO 8601 format assigned for your country (ex. it might be 2024.07.10 or 24/7/10 this is a standard that your country would use)

The `LocalDate.now()` method *can* take an argument. To use this we will import `java.time.ZoneId`.

###### What is ZoneId?
[ZoneId](https://docs.oracle.com/javase/8/docs/api/java/time/ZoneId.html) Released with `Java 8SE` defined as:
> A `ZoneId` is used to identify the rules used to convert between an [`Instant`](https://docs.oracle.com/javase/8/docs/api/java/time/Instant.html "class in java.time") and a [`LocalDateTime`](https://docs.oracle.com/javase/8/docs/api/java/time/LocalDateTime.html "class in java.time"). There are two distinct types of ID:
> - Fixed offsets - a fully resolved offset from UTC/Greenwich, that uses the same offset for all local date-times
> - Geographical regions - an area where a specific set of rules for finding the offset from UTC/Greenwich apply

In simple terms, this resolves the internationalization issue we had with the old `Date` API. After importing `java.time.ZoneId` we can look at some of the methods it has to offer.
- `ZoneId.getAvailableZoneIds()` Shows us all available zones here are some for example: `Europe/Istanbul, America/Eirunepe, Etc/GMT-4, America/Miquelon` (Remember each one of these is unique and we have two types of unique ID’s which are listed above).
- `ZoneId.systemDefault()` The method is defined as “If the system default time-zone is changed, then the result of this method will also change.” Which is self-explanatory.
- `ZoneId.of("")` We use this to define a custom set ZoneId from the `.getAvailableZoneIds()` list. Remember both `UTC` and `Europe/Istanbul` used as an example here can be used. 
- `ZoneId.from()` Remember the temporal we talked about before? Here we will pass it as an argument. If you're not entirely sure what this does, given a ==TemporalAccessor which represents an arbitrary set of date and time information we’ll get a ZoneId. If you are still a bit clueless you can import `java.time.ZoneId` and use `ZonedDateTime.now()` which will give you a precise time/date which then you could parse to a ZoneId. Basically `ZoneId.from(ZonedDateTime.now())`  

*There also a `Clock` argument you can pass, but I don’t see any use for it when you could just use ZoneID but feel free to explore that*

Now that we learned that - Let’s get the current date in Paris!
```
LocalDate.now(ZoneId.of("Europe/Paris")) // 2024-07-10
```

##### `LocalDate.of(year, month, day of month)`: > Obtains an instance of `LocalDate` from a year, month, and day.
Remember `LocalDate` represents a Date. In this case, we can set that date to whatever year,month, and day we want!

##### `LocalDate.ofYearDay(year, dayOfYear)`: >
In a lot of cases, you might only have a year and a day. This function converts it to a Year-Month-Day format. Here’s an example `LocalDate.ofYearDay(2023, 234)` will be `2023-08-22`. Leap years will also be accounted for.

##### `LocalDate.parse(text)` : > Obtains an instance of `LocalDate` from a text string using a specific format.
Basically, if we generate a String Date format like `2023-08-22` this will convert it into a LocalDate format 
### Epoch
There’s one last method I would like to talk about and even though it might not be that useful, it's a good thing to know.
Epoch in simple terms is a date set to the start. Virtually means it's “The start of time”. For example UNIX epoch is set to 1970/1/1 This is when all Unix time is calculated. Now this is not standardized between all computers. Most programming languages will use the UNIX epoch but not between all devices. For example `NTP` epoch is 1900/1/1. Now you might be asking why. And the simple answer is I don’t know. Unix was developed in 1969 and released in 71 but I guess the developers found 70 easier to work with and now that’s what we use! 

##### `LocalDate.ofEpochDay(epochDay)` : > 
Just going based on the description I gave about the output of this would be X days from 1970/1/1. Given epochDay is 1 => `1970-01-02` and so on.

~
~
~

By now I think you guys are all bored of all this nerdy talk and most likely lost interest completely but we are going to make it way more interesting in just a bit. 
`LocalDate` methods have a ton of subsets to modify dates as we talked about above. Explaining all of these is just a waste of time. The best thing is for you guys to check ’em out and play around a bit, they are all very simple to understand.

## Locale
The main idea of this whole article was to teach you internationalization and we are going to start that now. 
If you recall above I talked about how `LocalDate.now()` might show different numbers/punctuations and this is standardized by [Locale Class](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html)
> A `Locale` object represents a specific geographical, political, or cultural region. An operation that requires a `Locale` to perform its task is called _locale-sensitive_ and uses the `Locale` to tailor information for the user. For example, displaying a number is a locale-sensitive operation— the number should be formatted according to the customs and conventions of the user's native country, region, or culture.

Again the Locale class uses pre-defined ISO standards that Oracle has included. 

As I said - In the early days of the web Java was rushed and we can really see that here. 

### Locale Constant & Why not to use 
If you import `java.util.Locale` you can see that we have a few constants. `Locale.CANADA` as an example. If you're wondering what these are and why they were picked, it's quite simple. Due to the reason mentioned above, the Java devs just picked some Locale constants to support and you should not use them. Now if you look closely we have a `Locale.French`
and a `Locale.France` and you might be confused, what is this?? I’ll talk about it in a second 

Now how do we go about using these Locales? By using `Locale.availableLocales()` you will see a large subset of available locales that you can use. you might see it in the format of `en_US` and you might get confused. Following up on the question listed above Java has accounted for different language subsets used in different countries. In this France/French example, We can refer to Canadian French versus French used in France. They are not entirely the same. Now a country like Iran will use Persian no matter the place, so you could just use `Locale.of(language)` to specify the Locale, But for French you could rather use `Locale.of(language, country)`. Remember if you split what you got from `Locale.availableLocales()` by the `_` you can just format it like that. An example would be `Locale.of("en", "US")` for en_US

Now let's implement this into our time for our different users around the globe.

```java
System.out.println(
LocalDate.now().format(

DateTimeFormatter

.ofLocalizedDate(FormatStyle.SHORT)

.localizedBy(Locale.GERMAN)));
```

Now don’t mind the extra code, and even me using `Locale.GERMAN` cause honestly I was looking for a different output and the easiest way was to use Javas constants. I landed on `Locale.GERMAN` which outputs `10.07.24` as opposed to what Japan uses (`2024/07/10`).

#### Why not use `Locale.of()`
Now it might sound weird, but first of all i tell you not to use constants and prefer Locale.of(), then I tell you not to use `Locale.of()` an important factor to consider is `Locale.of()` was introduced with Java 19 which goes against supporting Java 8 SE to combat that from now on we will use 
```java
new Locale.Builder()
            .setLanguage("language")
            .setRegion("country").build();
```
Now another thing you could use is `Locale.setDefault(language, country)` which will work as well.

# DateTimeFormatter
Now looking at the code above you might recall seeing [DateTimeFormatter](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html) defined by docs as:
> Formatter for printing and parsing date-time objects.

### `LocalDate.format()`
As I mentioned above, one of the key features of Date/Time Local* APIs was formatting. And this is how we are going to format our dates. Looking at the code above - everything should make sense apart from the `.ofLocalizedDate()` method. The easiest way to show what it does is with an example.
```java
LocalDate anotherSummerDay = LocalDate.of(2016, 8, 23);
System.out.println(DateTimeFormatter.ofLocalizedDate(FormatStyle.FULL).format(anotherSummerDay));
System.out.println(DateTimeFormatter.ofLocalizedDate(FormatStyle.LONG).format(anotherSummerDay));
System.out.println(DateTimeFormatter.ofLocalizedDate(FormatStyle.MEDIUM).format(anotherSummerDay));
System.out.println(DateTimeFormatter.ofLocalizedDate(FormatStyle.SHORT).format(anotherSummerDay));
```
will output the following in order:
```bash
Tuesday, August 23, 2016
August 23, 2016
Aug 23, 2016
8/23/16
```

Now sometimes you might want to have your own pattern which you can easily do with
```java
System.out.println(

LocalDate.now().format(

DateTimeFormatter

.ofPattern("dd-uuuu-MMM")));
```

Now I’ll quickly go over what these symbols mean:
`dd` => It's a representation of the day field, now you could also use `d` and the difference would be that `d` would not have a fixed character limit since it represents 1 digit from 0-9 and 2 from 10-31. if you're lost it basically means `dd` would show 01; however `d` would show 1. However, going into two digits it's the same
`uuuu`/`yyyy` => Is the field for years. And you could also do `yy` which would show only the last two digits of the year. ex. 24 rather than 2024
`MMM` => The last field as you might have guessed is for the month - `MMM` tells Java that we want a String representation rather than a number. If you want a number use `MM`

So by now, you should’ve guessed that the output would be:
```bash
10-2024-Jul
```

### Instants
Now that you have a firm grip on Dates. I want to introduce you to [Instants](https://docs.oracle.com/javase/8/docs/api/java/time/Instant.html) defined as:
> An instantaneous point on the timeline.

Basically, this refers to [Instants](https://docs.oracle.com/javase/8/docs/api/java/time/Instant.html) showing a specific moment.
By now you might have assumed that `LocalDateTime` has a timezone, but it doesn’t as the docs mentioned they are just a representation of date/time. However a `ZoneId` is in fact a representation of a time zone.  Also, note that Instants don’t provide methods for altering our dates and times. 

Instants capture the current moment in UTC with the `Instant.now()` . Now based on this, you realize that `Local*` really doesn’t have a meaning unless it's applied, that’s the reason why you would actually refrain from using it in a business-level application. So prefer using `ZonedDateTime` and `Insant`. As a general rule of thumb use `Locale` When it's a specific point on a timeline rather than a moment in time. A moment would be like the moment I publish this, or the moment you read this, or the moment the world explodes, however a point in a timeline would be like an appointment there’s no moment for an appointment. If you're going on a vacation it's a specific time on a timeline, not a moment. 

#### Whats ZonedDateTime?
Quite simple. It's just an `Instant` with a `ZoneId` and this is why we say `Insant` has a timezone. No matter what you do it's not going to represent a time but rather be a specific moment.


*Aigh’t well that was quite the thing, wasn’t it? phew*
*have a nice one >#* 
