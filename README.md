# hugo-fullscreen-slider
A simple shortcode for hugo to add a fullscreen slider.

# Installation
Copy the file(s) to the `hugo/layouts/shortcodes` folder.

# Usage
1. Place the images in a subfolder inside the `hugo/static` folder.
2. Inside your content, use the shortcode `fullscreen-slider` and pass the subdirectory as the `dir`-parameter.
```go
{{< fullscreen-slider dir="/img/portfolio/" >}}
```
