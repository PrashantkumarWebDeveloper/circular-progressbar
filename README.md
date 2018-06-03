# circular-progressbar
Check out the demo here: [Demo](http://prashantmeandev-developer-edition.ap7.force.com/#circular-progress-bar)

This Circular progress bar was created using css only. It has various themes and size classes. Also, a UI designer can use SCSS file and create classes for theme and size according to the use, using mixins available in it.

## How to use?
It's so simple. Use the following markup and use main.css file in your page. For Lightning developers it's recomended to copy+paste the content of main-ltng.css in your component's style file.
```html5
<!DOCTYPE html>
<html>
<head>
    <title>Circular progress bar</title>
    <link rel="stylesheet" type="text/css" href="main.css">
</head>
<body>
    <div class="circular-progressbar-container">
        <div class="circular-progressbar first-half" data-progress-value="10" style="--progress-value: 10; --max-value: 100"></div>
    </div>
</body>
</html>
```
### Some basic things you need to take care of:
1. Use **data-progress-value** attribute to show text in the center of circular progress bar. It's recomanded to use the current progress value in this attribute with the units.
2. Use **--progress-value** style variable for increasing circular progress of progress bar. **--max-value** style variables stores the maximum value for circular progress.
3. One last thing but the important one is you need to toggle between two additional classes ``(first-half and second-half)``. For the progress value **0%** to ***50%***  you have to use ``first-half`` class and for progress value **51%** to **100%** you have to use ``second-half`` class. These classes will be applied to inner element having ``circular-progressbar`` class.
4. Now, nothing is left for basic setup. Enjoy :D.

## Are you looking for customisations? 
### You can customise Theme(Color) and Size. Check the classes below:
**Apply these classes to the element having ``circular-progressbar-container`` class.**

**Available ***Theme*** classes:**

|Theme|Class|
|-------|------|
|Default|Do not use any extra class|
|Success|success|
|Warning|warning|
|Danger|danger|
|Dark|dark|
|Primary|primary|
|Info|info|

**Available ***Size*** classes:**

|Size|Class|
|-----|-----|
|Default|Do not use any extra class|
|Extra Small|extra-small|
|Small|small|
|Large|large|
|Extra Large|extra-large|

**NOTE:** You can also use mixins available in main.sccs for more customization. Use ``create-theme($track-color, $progress-color)`` mixin for creating theme where ``$track-color`` is the path color and ``$progress-color`` is the color of current progress. Similarly You can use ``adjust-size($size, $path-width, $text-size)`` mixin to generate a new size for progress bar where ``$size`` controls height and width of progressbar, `$path-width`` controls the width of path/track and ``$text-size`` controls the size of text in the center of progressbar.
