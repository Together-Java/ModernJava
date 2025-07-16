# Filing Cabinets

The basic concept behind a Hash Map is the same concept as a filing cabinet.

If you grew up in a doctor's office like I did this will make sense. If you didn't, look up
what a filing cabinet looks like.

Basically, if you have folders for a bunch of people you can separate them into different cabinets.

You start by putting everyone in one cabinet. If you want to find someone's records, you look through
everything in that cabinet until you find it.[^sorted]

| Cabinet  |
| -------- | 
| Lightning McQueen  |
| Tow Mater |
| Doc Hudson |

Once you have enough records you separate your folders by something like the patient's last name. So you would
have your `A-M` and `N-Z` cabinets.

| A-M  | N-Z |
| -------- | |
| Lightning McQueen  | Strip Weathers |
| Tow Mater | |
| Doc Hudson | |
| Sally Carrera | |
| Chick Hicks | |

Then when you want to find someone, you can quicky pick the right cabinet by looking at their last name.

If you got too many people in one cabinet you would then subdivide that cabinet further.

| A-H    | A-M  | N-Z |
| -------- | ---- |-- |
| Doc Hudson | Lightning McQueen  | Strip Weathers |
| Sally Carrera | Tow Mater | |
| Chick Hicks | | |

And this basic system can scale to thousands of names.



[^sorted]: For a real filing cabinet system the contents of each cabinet would also be sorted. Ignore that for now.