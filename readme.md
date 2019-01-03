https://developers.google.com/web/updates/2018/03/emscripting-a-c-library
Also watch https://www.youtube.com/watch?v=ipNW6lJHVEs

Compile:
```
emcc -O3 -s WASM=1 -s EXTRA_EXPORTED_RUNTIME_METHODS='["cwrap"]' -s ALLOW_MEMORY_GROWTH=1 -I libwebp     webp.c     libwebp/src/{dec,dsp,demux,enc,mux,utils}/*.c
```

Notes:
* install emscripten and create symlinks for emcc and em++ in /usr/local/bin
* Get libwebp for encode_image example. "git clone https://github.com/webmproject/libwebp"
* FF doesn't support webp
* Chrome and others require files to be served over http not file:// so start php webserver from this directory.
