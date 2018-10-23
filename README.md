# hugo-slider-shortcode
A simple shortcode for hugo to add a gallery slider. It will fetch all images of a specified directory to display as a slideshow.

[A live demo with sample images is available.](https://tbiering.github.io/hugo-slider-shortcode/demo/)

## Installation
Copy the file `gallery-slider.html` to the `/layouts/shortcodes` folder of your hugo installation.

## Usage
1. Place the gallery images in a subfolder inside the `hugo/static` folder (for example `hugo/static/img/portfolio`).
2. Inside your content, use the shortcode `gallery-slider` and pass the subdirectory as the `dir`-parameter.
```go
{{< gallery-slider dir="/img/portfolio/" >}}
```

### Configuration Parameters
| Variable | Default | Description |
| -------------- | ------- | ----------- |
| `dir` | *`none`* | Path to image-folder *(mandatory)* |
| `width` | `500px` | Width of the slider area |
| `height` | `300px` | Height of the slider area |
| `arrow-left` | `fa-chevron-left` | Defines the left icon (See info below) |
| `arrow-right` | `fa-chevron-right` | Defines the right icon |
| `no-fa` | `false` | Toggles dependency inclusion for FontAwesome |
| `no-jquery` | `false` | Toggles dependency inclusion for JQuery |
| `auto-slide` | `0` | Set automatic sliding duration in ms |

#### Icons
You may choose any icon from the FontAwesome CSS-classes listed here: http://fontawesome.io/icons/ 

#### Examples
```html
<!-- Default use-case -->
{{< gallery-slider dir="/img/portfolio/">}}

<!-- Set width and height -->
{{< gallery-slider dir="/img/portfolio/" width="800px" height="350px" >}}

<!-- Set left and right icon -->
{{< gallery-slider dir="/img/portfolio/" arrow-left="fa-angle-double-left" arrow-right="fa-angle-double-right" >}}

<!-- Set automatic sliding duration -->
{{< gallery-slider dir="/img/portfolio/" auto-slide="2000" >}}
```

### Libraries used
This shortcode automatically loads it's necessary dependencies unless disabled via configuration. Thanks to these awesome libraries:
* FontAwesome 4.7.0
* JQuery 1.3.2

## License
Licensed under the MIT license.

For futher information see [LICENSE](LICENSE).