# convert

> Allow convert, resize images

- Install
`pacman -S imagemagic`

- Convert from PNG to JPG
`convert {{image.png}} {{image.jpg}}`

- Resize image with saved proportion
`convert {{image.png}} -resize 200x100 {{image2.png}}`

- Resize image without saved proportion
`convert {{image.png}} -resize 200x100! {{image_resized.png}}`

- Resize image with destination height, width will be calculated automatically
`convert {{image.png}} -resize 200 {{image2.png}}

- Resize image with destination width, height will be calculated automatically
`convert {{image.png}} -resize x100 {{image2.png}}

- Rotate image
`convert {{image.png}} -rotate 90 {{image2.png}}`

- Convert from PNG to JPG with white alpha channel
`convert -flatten {{image.png}} {{image.jpg}}`

- Resize pixelart
`convert -filter point -resize 200% {{src.png}} {{dst.png}}`

- Split image into parts
`convert -crop {{3x3@}} {{in.png}} {{out-%d.png}}`
`convert -crop {{420x420}} {{in.png}} {out-%d.png}}`

- List of images to pdf
`convert {{img1.png}} {{img2.png}} {{output.pdf}}`

- Join images on grid
`montage {{img1.png}} {{img2.png}} -tile {{2x1}} -geometry {{+0+0}} {{hello.png}}`
