# Rust Canvas

The goal of this project is to provide a simple, easy to use, and fast canvas library for Rust.

With canvas API i mean the HTML5 canvas API. This library is not a wrapper around the HTML5 canvas API, but it is inspired by it.

The goal of this is be able to:

- Create a canvas, with any height and width.
- Be able to create simples shapes like, rectangles, circles, lines, etc.
- Be able to create paths.
- Be able to fill and stroke paths.

The dream is to be able to render frames, similarly to the `requestAnimationFrame` function in JavaScript. So we can make nice visualizations.

I will mark this project was finish when i can recreate the times table cardioid visualization, [like this one made by Daniel Shiffman](https://www.youtube.com/watch?v=bl3nc_a1nvs).
Eventually i also like to try the [PI Approximation Visualization as showed in this video of 3blue1brown](https://www.youtube.com/watch?v=HEfHFsfGXjs).

## Develop Roadmap

I need to decide a implementation strategy, we are going to try render the image in a window or just store in a buffer then save to a file? I like the idea of a window and it is my goal, part of the javascript magic its view the changes as you code, but as rust is compiled we wont have this, so i don't see real benefit to start with rendering in a window, we will already compile so we can just wait, render the image/animation the save a file, a ppm image for the sake of simplicity or multiples frames, the we can use a tool like [ffmpeg](https://ffmpeg.org/) to create a video.
Eventually i would like to have a window, but i think this is a nice way to start.

Maybe the first step is figure out how to store the data, i don't think a pixel matrix will be the best way, need to look into something that can be versatile.
I wold like to draw simples shapes like rectangles, circles, and lines. I think this is a good start, and we can start to think about how to render the image.
But the most important part is to figure out how to make the paths, as this is the way we can make all types of shapes and really make the canvas API shine.

Coloring is also important, i don't think ppm images support alpha channel but i have to consider this. We can always start with ppm and ignore the alpha channel for now.

## References

- [HTML5 Canvas API](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API)
- [PPM Image Format](https://en.wikipedia.org/wiki/Netpbm_format#PPM_example)
- [Times Table Cardioid Visualization](https://www.youtube.com/watch?v=bl3nc_a1nvs)
- [ffmpeg](https://ffmpeg.org/)
