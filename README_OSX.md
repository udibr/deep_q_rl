Installation
============
Look for steps at `dep_script.sh` with following modifications.

In most cases you don't need to be root (use `sudo`)

Use `conda` where possible. For example

    conda install opencv

SDL can be installed with brew:

    brew update
    brew upgrade
    brew install sdl sdl_gfx sdl_image

ALE can be installed like this:

    cd Arcade-Learning-Environment/
    cp makefile.mac makefile
    sed -i 's/USE_SDL     := 0/USE_SDL     := 1/g' makefile
    make
    pip install .

