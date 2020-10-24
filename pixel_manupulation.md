# How to access and manipulate pixel data of a texture.
By default Godot imports textures as StreamTexture which doesn't allow direct access to pixel data. To be able to manipulate images we need to work with an ImageTexture. The first step is to reimport an image file as an Image. 


- texture.get_data() returns a copy of the data, not a reference to it. You need to assign it to a variable to be able to lock and unlock it and manipulate it.