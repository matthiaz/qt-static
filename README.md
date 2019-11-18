# qt-static

This repo contains static linux64 builds of qt
The compile was done like this:

```
QTVERSION="5.12.6"
git clone git://code.qt.io/qt/qt5.git
cd qt5
git checkout $QTVERSION
git submodule update --init --recursive
./configure -opensource -confirm-license -no-gstreamer -no-mirclient -skip webengine -nomake tests -nomake examples -release -ltcg -static -prefix /opt/qt/$QTVERSION && make
```

You can use the following to download a compile

  - git clone --single-branch --branch 5.12.6 git@github.com:matthiaz/qt-static.git
  - cd qt-static && mv opt/qt /opt/qt && cd ..
