Installation
============
Look for steps at `dep_script.sh` with following modifications.

In most cases you don't need to be root (use `sudo`)

Use `conda` where possible. For example

    conda install opencv

Use brew SDL:

    brew update
    brew upgrade
    brew install sdl sdl_gfx sdl_image
    
make sure you don't have SDL framework installed. If you do, remove it:

    sudo rm -rf /Library/Frameworks/SDL.framework

ALE can be installed like this:

    git clone https://github.com/mgbellemare/Arcade-Learning-Environment.git
    cd Arcade-Learning-Environment/
    cmake -DUSE_SDL=ON -DUSE_RLGLUE=OFF -DBUILD_EXAMPLES=ON .
    pip install .
    
If you want to watch/display the simulator (e.g. run `ale_run_watch.py`)
you will also need to install pygame:

    hg clone https://bitbucket.org/pygame/pygame
    cd pygame
    pip install .

