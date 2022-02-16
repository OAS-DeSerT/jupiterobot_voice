# jupiterobot_voice

## Instructions

- Copy & install

  $ sudo cp libmsc.so /usr/lib/
  
  *Files are in lib.

  $ sudo apt install sox

  $ sudo apt install libsox-fmt-all

- Speech recognition demo

  $ roscore

  $ rosrun jupiterobot_voice iat_publish

  $ rostopic pub /voiceWakeup std_msgs/String "data: 'any string'"
  
- Speech synthesis demo

  $ roscore

  $ rosrun jupiterobot_voice tts_subscribe

  $ rostopic pub -1 /voiceWords std_msgs/String "data: '你好'"

  $ rostopic pub /voiceWords std_msgs/String "data: 'I'm a robot.'"

- Voice repetition demo

  $ roslaunch jupiterobot_voice repeat_voice.launch

  $ rostopic pub -1 /voiceWakeup std_msgs/String "data: 'any string'"

- Voice assistant demo
  
  *The content of Q&A is written in the cpp file.
  
  *If the program does not capture keywords，it will repeat what it heard.

  $ roslaunch jupiterobot_voice voice_assistant.launch

  $ rostopic pub /voiceWakeup std_msgs/String "data: 'any string'"

## Reference

- IFLYTEK open platform

**http://www.xfyun.cn/**

- Baidu AI open platform

**http://ai.baidu.com/**

