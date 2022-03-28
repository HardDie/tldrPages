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
