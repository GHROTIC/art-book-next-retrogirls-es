# **<p align=center>Art Book Next - Retrogirls Edition</p>**

*<p align=center> Based in the style of pinup magazine scans ala Sports Illustrated Swimsuit Edition, except with the girls of gaming!</p>*

<br>

| 4:3 Boot Logo Preview | 4:3 Theme Preview |
| -- | -- |
| ![4:3 Boot Logo](https://github.com/GHROTIC/art-book-next-retrogirls-es/blob/master/assets/preview/bootlogo_4-3.jpg) | ![4:3 Preview](https://github.com/GHROTIC/art-book-next-retrogirls-es/blob/master/assets/preview/retrogirls_4-3.jpg) |

### **<p align=center>-= Notes =-</p>**

* Supports 4:3 and 16:9 screen ratios. Text may be a little off on others as it's been estimated and untested.
* Original Art removed to reduce bloat and new default images added for resolutions up to 1080p(Some art is poor quality at 1080p and will eventually be replaced).
* Some systems still have placeholder images and will be gradually replaced.
* Extremely old and/or obscure systems may have a random character playing a Video Game due to the difficulty in finding art that represents it.

<br>

<br>

### **<p align=center>-= Download =-</p>**
This version of the theme only works with distributions that use the latest Batocera (v40 and above) fork of EmulationStation.  Specifically [Batocera](https://batocera.org/), [Knulli](https://www.knulli.org/) and [RetroBat](https://www.retrobat.org/)

The latest version for each OS can be found on the releases page:

https://github.com/GHROTIC/art-book-next-retrogirls-es/releases

<br>

## Theme Configuration

The following options can be changed directly from the main menu under `User Interface Settings > Theme Configuration`

| Setting | Description | Options |
| -- | -- | -- |
| Distribution | Used to define which folder to look in for Theme Customization files. | `Batocera/Knulli`, `RetroBat` |
| Aspect Ratio | Enables you to select the correct aspect ratio for your screen.  This will automatically set itself so you should not need to change it but if the theme layout looks odd or spacing looks incorrect you can use this setting to make sure the aspect ratio matches your screen. | `16:9`, `16:10`, `4:3`, `3:2`, `1:1` |
| System Artwork | Defines the set of artwork that is displayed on the system view | `Default`, `Custom`, `Custom (Fullscreen)` |
| System Logos | Defines the logo set used on all views | `Default`, `Custom` |
| Game Artwork | Defines the type of artwork used to represent a game. These are sourced from the the selections you make in the scraper menu. Image will display the image you selected to scrape for `Image Source`.  Image (Cropped) will display that same image zoomed in to fill the screen.  Boxart will display the image you selected to scrape for `Box Source` | `Image`, `Image (Cropped)`, `Boxart` |
| Game Metadata | Sets if metadata (e.g. description, release date, etc...) should be displayed for a game | `On`, `Off` |
| Font Size | Set the size for text elements throughout the theme. | `Default`, `Small`, `Large` |
| Color Scheme | Sets the color scheme that is used for the theme.  There is a set of prebuilt color schemes that you can select and an option to supply your custom color scheme (selected by choosing `custom`). You can see details on customizations below under [Theme Customizations](#theme-customizations). | `Default`, `Light`, `Steam OS`, `SNES`, `Famicom`, `DMG`, `OLED`, `Custom` |

### Additional UI Settings 

The following EmulationStation settings can also be changed and will update the look of the theme accordingly:
* `User Interface Settings > Show Clock` - This will allow you to turn the system clock on or off
* `User Interface Settings > On-Screen Help` - This will turn the display of EmulationStation's help system on or off (the theme's layout will automatically adapt to the available space)
* `User Interface Settings > Show Battery Status` - This will allow you to change what is displayed for the battery status.

## Theme Customizations

Art Book Next allows customizations to system artwork and color schemes without the need to edit the source XML.  This enables you to change the look of the theme and still retain your changes when the theme is updated.

### Start Here
- Make sure the `Distribution` setting is set to the correct value for your current OS (e.g. Batocera/Knulli or RetroBat)
- This value determines the folder where you will add your customizations
    - Batocera/Knulli = `/userdata/theme-customizations/art-book-next/`
    - Retrobat = `C:\RetroBat\emulationstation\.emulationstation\theme-customizations\art-book-next\`
- Create the folders that match your distribution and then move on to the options below...

### Background Art

The artwork used on the system view can be customized with your own images.

#### For angled artwork:

* Create your custom artwork using one of the masks i've supplied in this theme's resources directory [here](https://github.com/anthonycaccese/art-book-next-es/tree/main/resources/customizations). I've included a set of masks that should work in all major image editing programs.
* Export your final images as transparent pngs
* Create a folder in the path you created above called `artwork`
* Upload your images to that folder
* They can be named:
    * `_default.png`
    * `${system.theme}.png`
    * The theme will look them them up in that order. If a given image is not found in your folder then the the images from the theme will be used as a fallback.  This allows you to customize only the images you want and still have images displayed for all systems.
    * `_default.png` can be used for creating a single image that is used for all systems OR a fallback for systems that you did not create a custom image for (if you don't want to use the fallback that already exists in the theme)
    * `${system.theme}.png` should be named for the system you are looking to override. For example if you wanted to override the artwork for `snes` you would create an image called `snes.png` in the artwork folder.
* Once your images are in place you turn on custom images by changing the `System Artwork` setting to `Custom`

#### For fullscreen artwork:

* Create a folder in the path you created above called `artwork-fullscreen`
* Upload your images to that folder
* They can be named:
    * `_default.png`
    * `_default.jpg`
    * `${system.theme}.png`
    * `${system.theme}.jpg`
    * The theme will look them them up in that order.
    * `_default.png/jpg` can be used for creating a single image that is used for all systems OR a fallback for systems that you did not create a custom image for (if you don't want to use the fallback that already exists in the theme)
    * `${system.theme}.png/jpg` should be named for the system you are looking to override. For example if you wanted to override the artwork for `snes` you would create an image called `snes.png` or `snes.jpg` in the artwork folder.
* Once your images are in place you turn on custom images by changing the `System Artwork` setting to `Custom (Fullscreen)`

> If you create a set of images that you would like to share with the community please let me know about it [here](https://retropie.org.uk/forum/topic/33010/theme-art-book-next)

### Color Schemes

You can create your own custom color scheme to use for the theme

* Download this template: https://github.com/anthonycaccese/art-book-next-es/blob/main/resources/customizations/colors.xml
* Upload it in the path you created above and make sure its called `colors.xml`
* Change any values in the template to the colors you prefer.
* I tried to make the values as self explanatory as possible but if you have questions regarding which property does what please don't hesitate to ask.
* After your colors are defined; in theme configuration change `Color Scheme` to `Custom`

### Logos

System logos can be customized by adding your own images

* Create a folder in the path you created above called `logos`
* Upload your images to that folder
* They can be named:
    * `${system.theme}.svg`
    * `${system.theme}.png`
    * The theme will look them them up in that order. If a given image is not found in your folder then the the images from the theme will be used as a fallback.  This allows you to customize only the images you want and still have images displayed for all systems.
    * `${system.theme}.svg/png` should be named for the system you are looking to override. For example if you wanted to override the logo for `snes` you would create an image called `snes.svg` or `snes.png` in the logos folder.
* Once your images are in place you turn on custom images by changing the `System Logos` setting to `Custom`

## **Additional Notes**

### Media Scraping:

* To make game artwork look as good as possible the recommneded settings for the built-in scraper are:
    * Image Source = `Screenshot`
    * Box Source = `Box 2D`
    * Logo Source = `Marquee`

### **Acknowledgments**
* Thanks to Anthony Caccese, the creator of Art Book Next, for his excellent design that inspired this modification.
* ChangaOne font is by [Eduardo Tunni](https://www.fontsquirrel.com/fonts/changa)
* Metadata Icons sourced from [FontAwesome](https://fontawesome.com/search?o=r&m=free)
* Thank you to [GenoCL](https://genocl.carrd.co/) for the idea of the multi-artwork system view.
* All images sourced from image depositories that allow user downloads, transferable rights and creation of derivative works per thier ToS, such as Danbooru. In some cases official art, screenshots or wallpaper may be used as placeholders.
###### *<p align=center>(If you are the original artist and would like your work removed from this project, please contact me via Discord: @GHROTIC)</p>*

## **License**
Creative Commons CC-BY-NC-SA - https://creativecommons.org/licenses/by-nc-sa/2.0/
You are free to share and adapt this theme as long as you provide attribution back to me (and the above credits) as well share any updates you make under the same license terms.

Thank you for taking a look at this 😄
