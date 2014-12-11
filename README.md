# OSX Icons #

Open source icon framework for creating OSX icons and icon repository.

You can use an image or use an `.icns` generator with a single image as a custom OSX icon. That's not the *right* way to do it. I've tried it, and it leads to images that are pixelated when enlarged, fuzzy when shrunk, and don't match the other OSX icons. This framework creates an environment where you can create your own high-quality OSX icons. It includes template `.psd` files, required folders and samples to get you going! Finally, I'll be sure to add more icons as they come in so that this can also be a source for high-quality, custom OSX icons.
--kubasub

## Using the framework ##
1. Fork/download the repo.
1. Create a copy of `source/template` and rename it to `<ICON_NAME>/`. This is the root directory for your creation.
2. Rename `templateIcon.iconset/` to `<ICON_NAME>.iconset/`.
3. Create your icon in every `.psd` file. Note: use the layer style from the blank layer to style your custom image.
4. Save every `.psd` as a `.png` in `<ICON_NAME>.iconset/`
5. In `<ICON_NAME>/` run `iconutil -c icns <ICON_NAME>.iconset/ -o ../../<ICON_NAME>.icns`. This generates the icon in the projects root directory.
6. All done! To use the icon, check out "Installing Icons".

## Installing Icons ##
1. Download the icon that you want (`<ICON_NAME>.icns`).
2. Put the icon in `/System/Library/CoreServices/CoreTypes.bundle/Contents/Resources/`.
    - Note: You need to right-click on `CoreTypes.bundle` and select "Show Package Contents".
3. In another Finder window, go to the folder you want to customize, right-click and "Get Info".
4. Drag the icon from step 2 and drop it on the top left icon of the info window from step 3.

## Notes ##
- The framework is currently specifically set up for creating custom folder icons for OSX.
- OSX has lost much of its skeuomorphic-look as of Yosemite. These icons and framework currently only complement OSX < 10.10.
