# sony

> How to user Sony camera in Linux

- Install all required packages
`pacman -S v4l2loopback-utils v4l2loopback-dkms libgphoto2 ffmpeg`

- Install kernel module for v4l2loopback
`modprobe /usr/lib/modules/{{6.10.6-arch1-1}}/updates/dkms/v4l2loopback.ko.zst exclusive_caps=1 max_buffers=2`

- Check if camera detected
`gphoto2 --auto-detect`

- Run pipe from camera to new virtual camera
`gphoto2 --stdout --capture-movie | ffmpeg -i - -vcodec rawvideo -pix_fmt yuv420p -threads 0 -f v4l2 /dev/{{video4}}`
