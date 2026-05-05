# Custom Screens
Create fully customizable in-game screens for tutorials, tips, or announcements. Define your own layouts, text, images, and timing through a simple configuration file.

![ExamplePreset](https://cdn.modrinth.com/data/cached_images/c03a63d0eb02b2720a113b75131f8c54b131a4f6_0.webp)
---
## How to use
First you need to locate the config file create after the first launch. This file can be located in
```
config/arcana
```
Inside there you should see the custom-screens-preset.json. 
  
This file defines each screen preset, including:
- Preset name
- Title and body text
- Text position
- Image and background (bg size, 64x64) (optional)
- Image size
- Display duration
> _Note:_ If no image or background is specified, it will not be rendered.

To see the example preset or a new one created by you, in game use the next command
```
/show-screen [target selector] [preset name] [notify ops (true/false)]
```
To add another preset duplicate the example preset in the JSON file and modify it as needed. 

### Custom text and images (via resource pack)
Images and text can be provided using a resource pack.
- Text: 
```
myresourcepack\assets\custom_screens\lang\en_us.json
```
- Images: 
```
myresourcepack\assets\custom_screens\textures\gui\*.png 
```
> Important notes:
> - Background images will tile to fill the entire screen.
> - Only .png files are supported.

```json
{
  "example_preset": {
    "text": {
      "title": "arcana.customscreens.example_title",
      "text": "arcana.customscreens.example_desc",
      "position": "BOTTOM_LEFT"
    },
    "images": {
      "image": "textures/gui/default_image.png",
      "background": "textures/gui/default_bg.png",
      "w": 200,
      "h": 100
    },
    "duration": 5
  }
}
```

