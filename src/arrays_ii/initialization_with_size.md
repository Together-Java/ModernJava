# Initializion with Size

The Nintendo GameBoy had a screen resolution of 160 x 144.
To store the value of each pixel[^bw] you would need an array 23,040 items 
long.

To support this without you writing the word `false` 23,040 times,
arrays can be made with just by giving a size and skipping the initializer.

```java,no_run
boolean[] pixels = new boolean[23040];
```

So you have to say `new` followed by the type of element in the array, `[`, the size of the array and `]`.

[^bw]: The original GameBoy was technically capable of seven shades of gray per pixel, so in this example `boolean` implies a black and white image.
