# hugo-slider-shortcode
A simple shortcode for hugo to add a gallery slider. It will fetch all images of a specified directory to display as a slideshow.

### Installation
Copy the file `gallery-slider.html` to the `/layouts/shortcodes` folder of your hugo installation.

### Usage
1. Place the images in a subfolder inside the `hugo/static` folder (for example `hugo/static/img/portfolio`).
2. Inside your content, use the shortcode `gallery-slider` and pass the subdirectory as the `dir`-parameter.
```go
{{< gallery-slider dir="/img/portfolio/" >}}
```

### Configuration Parameters
| Variable | Default | Description |
| -------- | ------- | ----------- |
| `dir` | `none` | Path to the folder containing all the images (allowed filetypes: `gif,jpg,jpeg,tiff,png,bmp`) *(mandatory)* |
| `width` | `500px` | Defines the width of the slider area. Allowed values are CSS-width values. |
| `height` | `300px` | Defines the height of the slider area. Allowed values are CSS-width values. |
| `fullscreen` | `false` | Toggles fullscreen display. If set to `true`, the configuration for `width` and `height` are overridden and a fullscreen display is used . |
| `no-fa` | `false` | Toggles dependency inclusion for FontAwesome. If set to `true`, the dependency will be excluded from loading. |
| `no-jquery` | `false` | Toggles dependency inclusion for JQuery. If set to `true`, the dependency will be excluded from loading. |

### Examples
```{{< gallery-slider dir="/img/portfolio/" width="500px" height="250px" >}}```

```{{< gallery-slider dir="/img/portfolio/" fullscreen="true" >}}```

### Libraries used
This shortcode automatically loads it's necessary dependencies unless disabled via configuration. Thanks to these awesome libraries:
* FontAwesome 4.7.0
* JQuery 
