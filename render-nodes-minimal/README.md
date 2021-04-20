# Headless EGL usage in container

## install dependencies

```
apt-get install libgles2-mesa-dev libgbm-dev
```

## configure container

```
... --bind=/dev/dri/


DeviceAllow=char-drm rwm

```

## Build and run

```
make
./render-nodes-minimal
```
