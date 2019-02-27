Bootstrap: debootstrap
OSVersion: bionic
MirrorURL: http://us.archive.ubuntu.com/ubuntu/

%post
  apt update
  apt install -y software-properties-common wget
  apt-add-repository universe
  wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O miniconda3.sh
  bash miniconda3.sh -b -p /opt/miniconda
  export PATH="/opt/miniconda/bin:$PATH"
  conda install pillow

%files
  Gif_Ascii_Animator.py /usr/local/bin

%environment
  export LC_ALL=C.UTF-8
  export LANG=C.UTF-8
  export PATH=/opt/miniconda/bin:"$PATH"

%runscript
  python /usr/local/bin/Gif_Ascii_Animator.py "$@"

%help
  download and convert a gif to ascii - using https://github.com/tpoff/Python-Gif-Ascii-Animator
