v0.9.3:
  * Add 'WindowHandle::effective_transform()` to get the full transformation from image space to virtual window space.

v0.9.2:
  * Fix horizontal stretching of saved images.

v0.9.1:
  * Fix cropping image by half a pixel on all sides.

v0.9.0:
  * Change `WindowHandle` API to provide more efficient access to window properties.
  * `WindowHandle` now guarantees that the referenced window is valid.
  * Prohibit access to `&mut ContextHandle` as long as a `WindowHandle` exists.
  * Rename `show_overlays` property to `overlays_visible`.
  * Fix interpretation of `tch::Tensor` with planar data.
  * Add user configurable image transformation.
  * Add `prev_position` to `MouseMoveEvent`.
  * Add `position` and `prev_position` to `MouseButtonEvent`.
  * Add enabled-by-default mouse controls to pan and zoom images.
  * Use `glam` vectors in public API (and publicly re-export `glam`).
  * Bump allowed `tch` version to 0.5.

v0.8.5:
  * Update to wgpu `0.9` and winit `0.25`.

v0.8.4:
  * Fix compatibility with Rust stable.

v0.8.3
  * Allow manual rendering back-end selection with the `WGPU_BACKEND` environment variables.
  * Allow manual GPU selection with the `WGPU_POWER_PREF` environment variables.
  * Fix panic when minimizing a window on Windows.

v0.8.2
  * Disable some default features of dependencies to reduce dependency tree.
  * Support `tch` versions 0.1.6 through 0.4.0.
  * Update to `wgpu` 0.7.
  * Make sure the process aborts when the main user task does so.

v0.8.1
  * Enable `macros` feature by default.
  * Add links in README.

v0.8.0
  * Complete rewrite with new API using `winit` and `wgpu` as backend.
  * Ensure macOS compatibility by running the event loop in the main thread.
  * Add support for overlays drawn on top of the main image.

v0.7.0
  * Add support for showing overlays on top of images.
  * Fold consecutive mouse move events to reduce number of events.
  * Allow registered event handlers to remove themselves.
  * Remove implicit event channel of window handles.
  * Make window handles Clone.
  * Fix the `resizable` window option.
  * Add option to make borderless windows.

v0.6.5
  * Support `tch` versions 0.1.6 through 0.3.x.
  * Support `raqote` versions 0.7.14 through 0.8.x.

v0.6.4
  * Support `tch` versions 0.1.6 through 0.2.x.

v0.6.3
  * Increase timeout on communication with background thread to 1 second.
  * Divide `raqote` images by their alpha component to undo pre-multiplication.

v0.6.2
  * Add support for `raqote::DrawTarget` and `raqote::Image`.

v0.6.1
  * Update keyboard-types dependency to 0.5.0.
  * Update sdl2 dependency to 0.33.0.

v0.6.0
  * Add support for handling mouse events.
  * Replace (data, info, name) tuple for displayed images with a struct.

v0.5.1
  * Add `window.add_key_handler`to register asynchronous key handlers.
  * Ignore key events that happened while a window was out of focus.

v0.5.0
  * Add `stop()` function to cleanly stop the background thread.
  * Add `window.get_image()` to retrieve the displayed image.
  * Associate a name with displayed images.
  * Expose `save_image()` and `promp_save_image()`.
  * Fix `window.set_image()` for windows on other workspaces.
  * Fix handling Ctrl+S with modifiers like numlock, capslock, etc.

v0.4.3
  * Add readme to Cargo manifest.

v0.4.2
  * Fix example.
  * Use `assert2` for tests.

v0.4.1
  * Allow end-users to save displayed images.
  * Fix display of color images without alpha channel.

v0.4.0
  * Remove access to `Context` to simplify API.

v0.3.0
  * Change `ImageData` trait to allow consuming images.
  * Implement `ImageData` for tuples of data and `ImageInfo`.
  * Add support for `tch::Tensor`.

v0.2.0
  * Rename `make_window` functions to favor the simple functions.

v0.1.1
  * Support 8-bit grayscale image data.
  * Preserve aspect ratio of images, if requested.
  * Add easy to use API that uses global context.

v0.1.0:
  * Initial release.
