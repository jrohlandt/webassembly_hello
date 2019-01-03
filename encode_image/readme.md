https://developers.google.com/web/updates/2018/03/emscripting-a-c-library

Compile:
```
emcc -O3 -s WASM=1 -s EXTRA_EXPORTED_RUNTIME_METHODS='["cwrap"]' -s ALLOW_MEMORY_GROWTH=1 -I libwebp     webp.c     libwebp/src/{dec,dsp,demux,enc,mux,utils}/*.c
```

Notes:
* FF doesn't support webp
* Chrome and others require file to be served by web server so start php webserver from this directory.
