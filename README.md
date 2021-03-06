# リポジトリ内の説明
SandBox -> プロジェクト本体

Document -> 放送内で使用したスライド

# 初期化
sudo apt-get update

sudo apt-get upgrade
# エディタのインストール
sudo apt-get install vim

sudo apt-get update

# 作業ディレクトリの作成
mkdir /mnt/c/workspace

ln -s /mnt/c/workspace $HOME

# C C++
sudo apt install build-essential cmake
# 必要ライブラリのインストール
sudo apt install git libgtk2.0-dev pkg-config libavcodec-dev libavformat-dev libswscale-dev
# 並列処理と画像ファイルのライブラリ
sudo apt install libtbb2 libtbb-dev libjpeg-dev  libpng-dev libtiff-dev
# GUI系
sudo apt install libqt4-dev libqt4-opengl-dev libgtkglext1 libgtkglext1-dev

# OpenCV本体のダウンロード
cd ~/workspace

sudo git clone https://github.com/opencv/opencv.git

sudo git clone https://github.com/opencv/opencv_contrib.git

cd opencv

mkdir build

cd build

# OpenCVのインストール
cmake -D CMAKE_BUILD_TYPE=Release -D CMAKE_INSTALL_PREFIX=/usr/local -D WITH_TBB=ON -D WITH_OPENGL=ON -D OPENCV_EXTRA_MODULES_PATH=~/workspace/opencv_contrib/modules -D OPENCV_GENERATE_PKGCONFIG=ON ..

make -j7

sudo make install

# 参考
https://qiita.com/kekenonono/items/031a3b41d6adb4c3e876

https://qiita.com/kekenonono/items/0fcf042bca2d3d17867a

https://github.com/yoyoyo-yo/Gasyori100knock
