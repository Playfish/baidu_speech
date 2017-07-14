#Introduction
 this package is python package for ROS speech, which use online baidu speech to do TTS and speech recognition.

 this code is run well in ubuntu 14.04, thinkpad T44s.

 you can visit the baidu speech home page at here: http://yuyin.baidu.com/

 the key and id is show below, feel free to change it in ```simple_speaker.launch``` and ```simple_voice.launch```.


App ID: 9864431

API Key: wqGDFYG5sha2wR0EbY3Nzple

Secret Key: v4hNHmqL0Qv9YExwrKww7fMDI7kB052k

# subscribe topic
speak_string

#type
string

# How to run:

Speech Recognition:　```roslaunch simple_voice simple_voice.launch```

Text To Speech:  ```roslaunch simple_voice simple_speaker.launch```


# Installation

At first install pyaudio and vlc

Installation of pyaudio using following command:
```
$ sudo apt-get install python-pyaudio
```

Installation of vlc using following command:
```
$ cd
$ git clone https://github.com/geoffsalmon/vlc-python.git
$ sudo cp vlc-python/generated/vlc.py /usr/lib/python2.7/
```

#Running & test
## Runing simple_speaker.launch
In your src directory of catkin workspace 
```
$ git clone https://github.com/DinnerHowe/simple_voice.git
$ roslaunch simple_voice simple_speaker.launch
```
Then open other terminal
```
$ roscd simple_voice/src
$ rostopic pub /speak_string std_msgs/String -- '请让一下.mp3'
```
After this you will get voice from computer such as ```请让一下```.

## Runing simple_voice.launch

Test simple_voice is simple, just run following command is ok:
```
$ roslaunch simple_voice simple_voice.launch
```

# Refrence

This project is clone with http://github.com/DinnerHowe/baidu_speech

