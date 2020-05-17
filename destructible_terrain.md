# Destructible terrain

This code allows to access and modify pixel data at a given position. One could set the alpha channel of a pixel, or area of pixels, to zero to create an illusion of destroyed terrain.

```python
background_data = get_node("background").get_texture().get_data()
background_data.get_pixel(pixel_pos.x, pixel_pos.y)
background_data.put_pixel(mouse_pos.x + x, mouse_pos.y + y, Color(0, 0, 0, 0))
```
