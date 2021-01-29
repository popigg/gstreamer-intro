# GStreamer-intro
Introduction to GStreamer pipelines and few C scripts

``` bash
    # inspect 
    gst-inspect-1.0 playbin

    # pipelines
    # audio
    gst-launch-1.0 audiotestsrc ! audioconvert ! autoaudiosink

    # video
    gst-launch-1.0 videotestsrc ! videoconvert ! autovideosink 
    gst-launch-1.0 videotestsrc num-buffers=1 ! jpegenc ! filesink location=videotestsrc-frame.jpg

    # audio and video in a file
    gst-launch-1.0 audiotestsrc ! vorbisenc ! oggmux name=mux ! filesink location=file.ogg videotestsrc ! theoraenc ! mux.
```

