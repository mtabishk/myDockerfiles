# Spotify App

## Run the Container:
```

docker run --rm -it -e DISPLAY=$DISPLAY -v /tmp/.X11-unix:/tmp/.X11-unix --net=host --device /dev/snd mtabishk/spotify-app

```

 -v /tmp/.X11-unix:/tmp/.X11-unix \ # mount the X11 socket
 
  -e DISPLAY=$DISPLAY \ # pass the display
  
  --net=host \ # to use host network
  
  --device /dev/snd \ # sound
