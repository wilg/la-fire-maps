# LA fires recent satellite imagery

> ⚠️ Update: Newer images, from 2025-01-16 and 2025-01-15 have been added to Maxar's open data. I will attempt to add them here soon.

> ⚠️ Update: LAFD is conducting damage assessments of homes. More information is available at [recovery.lacounty.gov](https://recovery.lacounty.gov/)

### 2025-01-10 imagery

<a href="images/1050010040277500.html">
    🔎 Los Angeles Palisades Fire<br> Friday, 2025-01-10 10:36 AM Pacific<br>
    <img src="images/1050010040277500-preview.jpeg" width="100">
</a>

<a href="images/1050010040277300.html">
    🔎 Los Angeles Eaton Fire<br> Friday, 2025-01-10 10:36 AM Pacific<br>
    <img src="images/1050010040277300-preview.jpeg" width="100">
</a>

---

For detailed fire information, I recommend [Watchduty](https://app.watchduty.org/).


### Updates

- 2025-01-20: Noted newer images are now available at Maxar
- Added link to [recovery.lacounty.gov](https://recovery.lacounty.gov/)
- Updated both fires to include more area, but the time the photo was taken is the same.

## Source

[Maxar](https://maxar.com/) is a company that sells various satellite photo products. They make some data available for emergency situations.

The images are available from Maxar's open data with a free account, but you have to sign up and isn't super quick and doesn't work very well on the phone.

I've copied **the main two** images they've taken for quick reference.

I'm not sure if they have stopped releasing open images of this event or if there will be updated imagery in the future.

You may be able to contact them to see if they can make more imagery available, or perhaps purchase some, I'm not exactly sure.

---

### Accessing the Maxar imagery directly

Maxar has some satellite imagery of the Palisades and Eaton fires that is high resolution and is more up to date than I have found on any other services.

1. Visit [https://xpress.maxar.com](https://xpress.maxar.com) and sign up for a free account.

2. Click the "Open Data" button in the sidebar.

   ![Maxar Open Data](maxarhelp.png)

3. Choose the LA fire event.

4. Select a relevant image. Note the time and region is different, and the order of everything is kinda confusing.

5. Browse the imagery in their web view. Or you can download the original "Visual Image" of an "ARD tile" of interest. These images are gigantic and will look blurry and break most programs except Photoshop.

## Contributing
### Adding new images

Generate a dzi image pyramid with vips.

```
gdalbuildvrt my_mosaic.vrt *_visual-image.tif
gdalwarp my_mosaic.vrt final_mosaic_visual.tif -co COMPRESS=DEFLATE -multi
vips dzsave final_mosaic_visual.tif ./images/id
```

and copy and tweak the html file

Any help is welcome improving this, [make a PR or issue on GitHub](https://github.com/wilg/la-fire-maps) or [notify me somehow](http://wilgieseler.com).
