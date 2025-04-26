# ffmpeg

- How to convert and remove metadata from audio
`ffmpeg -i {{input.m4a}} -map 0:a -map_metadata -1 {{output.flac}}`
