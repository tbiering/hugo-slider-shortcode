# hugo-slider-shortcode
A simple shortcode for hugo to add a gallery slider. It will fetch all images of a specified directory to display as a slideshow.

### Installation
Copy the file(s) to the `hugo/layouts/shortcodes` folder.

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
| `width` | `400px` | Defines the width of the slider area. Allowed values are CSS-width values. |
| `height` | `200px` | Defines the height of the slider area. Allowed values are CSS-width values. |
| `fullscreen` | `false` | Enables/Disables fullscreen display. If set to `true`, the configuration for `width` and `height` are overridden and a fullscreen display is used . |

### Examples
```go
{{< gallery-slider dir="/img/portfolio/" width="500px" height="250px" >}}
```

```go
{{< gallery-slider dir="/img/portfolio/" fullscreen="true" >}}
```
