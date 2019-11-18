# qt-static

This repo contains static linux64 builds of qt
The compile was done like this:

```
git clone git://code.qt.io/qt/qt5.git
cd qt5
git checkout 5.12.6
git submodule update --init --recursive
./configure -opensource -confirm-license -no-gstreamer -no-mirclient -skip webengine -nomake tests -nomake examples -release -ltcg -static -prefix /opt/qt/5.12.6 && make
```
