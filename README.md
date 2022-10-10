## MobiFlight Profiles

Please visit [https://www.mobiflight.com/](MobiFlight) and [https://hubhop.mobiflight.com/](HubHop) for background information. Currently I am only in MSFS 2020. These are the configurations I use for the various controllers and panels that rely on MobiFlight along with some notes.

## Notes

### Heading Bug

This will distingush between a long press and a short press. The long press will set the heading bug to the current heading and the short press will switch auto pilot to heading hold.

Enter in `On Press` custom field
```
(E:SIMULATION TIME,second) 0.25 + (>L:myTshort)
```

Enter IN `On Release` custom field
```
(E:SIMULATION TIME,second) (L:myTshort) < if{ (>K:AP_HDG_HOLD) } els{ (A:HEADING INDICATOR, degrees) (>K:HEADING_BUG_SET) }
```
