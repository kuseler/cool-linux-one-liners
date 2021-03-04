# Stuff with I/O

## live stream of window as fake webcam

```bash
modprobe v4l2loopback; ffmpeg -f x11grab -r 15 -s 1280x720 -i :0.0+0,0 -vcodec rawvideo -pix_fmt yuv420p -threads 0 -f v4l2 /dev/video0

```

Creates a virtual camera from a video stream from a website
this only works with x11
