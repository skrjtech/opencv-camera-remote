# image
FROM debian:latest
# init process
RUN apt update && apt -y upgrade
RUN apt-get update && apt-get -y upgrade
# importante package
RUN apt install -y software-properties-common
RUN apt install -y sudo git fonts-takao ffmpeg wget
# python 
RUN apt install -y python3-pip 
RUN apt install -y build-essential libssl-dev libffi-dev python3-dev
# これ入れないとopencvが正常に作動しない
RUN apt install -y libgl1-mesa-dev
# pip update
RUN python3 -m pip install --upgrade pip setuptools
# 画像処理機能
RUN python3 -m pip install opencv-python opencv-contrib-python
# 進行状況可視化
RUN python3 -m pip install tqdm
RUN python3 -m pip install jupyterlab
RUN python3 -m pip install selenium webdriver-manager beautifulsoup4
#pyautogui
RUN python3 -m pip install pyautogui python-xlib
RUN DEBIAN_FRONTEND=noninteractive apt install -y python3-tk tk-dev

CMD [ "/bin/bash" ]