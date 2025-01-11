# LA fire maps

Maxar has some satellite imagery of the Palisades and Eaton fires that is high resolution and as recent as 10:30AM on the 10th.
It's a bit annoying to get access but is the best I've found.

https://xpress.maxar.com

TL;DR sign up for the free account, then click the second strange button in the toolbar to see the open data events, pick LA fires, and then there will be a series of images taken at different times and regions (some of which seem like very strange choices) and then you can zoom in via the web view or download the original "Visual Image" of an "ARD tile" of interest which is gigantic and will look blurry and break most programs except photoshop.

This is a way to make those easier to view.

```
vips dzsave infile.tif ./images/id
```

and copy and tweak the html file
