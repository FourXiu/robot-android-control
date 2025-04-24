# robot-android-control
控制已经导入了rip-robot项目和mjpg-streamer-experimental项目的树莓派机器人

具体操作：

ssh pi@ip地址

密码：raspberry

sudo pigpiod

唤醒摄像头：

cd rip-robot

cd /mjpg-streamer-experimental

export LD_LIBRARY_PATH=.

mjpg_streamer -i "input_uvc.so -d /dev/video0 -r 640x480" -o "output_http.so -w ./www"


打开控制程序：

cd rip-robot

python3 main.py

控制使用端口 5000
