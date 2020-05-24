# How to create an Image in GDScript

If we want to be able to access and manipulate the pixels of our image files we first need to create their representation in our scripts. There are two ways of doing it, both similar but requiring different steps.

## 1. Use global load() function.
This is the first method. We use the global load() function with the path to our image. However this method required an additional step.

Godot by default imports images as StreamTextures. These are very fast to render but the downside of them is that we can't access their pixel data. To bypass this issue we need to reimport our image file as an actual Image in the editor.

After doing this the rest is as simple as creating a variable and assining to it the result of load(path_to_file).

```python
var img: Image
img = load("path_to_file")
```

## 2. Use Image.load() function.
This method while requiring one extra line of code is actually easier as it doesn't require reimporting of the file we wish to use.

We first create a new instance of an Image using Image.new() then call the instance's load() method with the path to our file.

```python
var img: Image
img = Image.new()
img.load("path_to_file")
```
