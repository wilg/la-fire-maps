# LA fire maps

This is a way to make Maxar open data easier to view on the web so people can see if their house burned down.

### Accessing the Maxar imagery directly

Maxar has some satellite imagery of the Palisades and Eaton fires that is high resolution and as recent as 10:30AM on the 10th.

1. Visit https://xpress.maxar.com and sign up for a free account.

2. Click the "Open Data" button in the sidebar.

  ![Maxar Open Data](maxarhelp.png)

3. Choose the LA fire event.

4. Select a relevant image. Note the time and region is different, and the order of everything is kinda confusing.

5. Browse the imagery in their web view. Or you can download the original "Visual Image" of an "ARD tile" of interest. These images are gigantic and will look blurry and break most programs except Photoshop.

#### Adding new images

Generate a dzi image pyramid with vips.

```
vips dzsave infile.tif ./images/id
```

and copy and tweak the html file

 Any help is welcome improving this, I will not be able to keep it up to date.
