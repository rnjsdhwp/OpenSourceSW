시각장애인을 위한 약 구별 시스템
===================================
   
![Pill So Good](https://user-images.githubusercontent.com/84956281/132686311-250a319f-63fa-425f-849f-f961d21a0879.jpg)

개발 목적
------------
21세기 현대인들에게 있어 약은 떼려야 뗄 수 없는 존재입니다.
하지만 시각장애인분들은 이러한 약을 매번 챙겨 먹기에는 무리가 있습니다.
이유는 많은 약 중에 어떤 약을 먹어야 하는지, 들고 있는 약이 내가 먹어야 하는 약인지, 약을 먹었는지 안 먹었는지 구분하기란 쉽지 않기 때문입니다.
그래서 저희는 약을 챙겨 드셔야 하는 시각장애인분들을 위한 시스템을 만들고자 합니다.


동작
----------
**Raspberry Pi의 PIR 센서**를 이용하여 알약을 감지하고
**카메라 센서**를 이용하여 알약을 촬영하여 분석할 준비를 합니다.
다음 **Flask 서버에서 csv 파일을 이용**하여 알약을 분석합니다.
이렇게 분석된 데이터를 기반으로 **스피커를 통해 음성을 출력**합니다.
또한, 시각장애인들도 사용할 수 있도록 움직임을 최소화하여 설계합니다.

Deep Learning
----------------
서버에서 데이터를 분석할 때, 텍스트와 색깔로 알약을 구분합니다.
알약 사진을 가져와 각종 전처리 과정을 거치고 **Tesseract OCR**를 이용하여 알약에 있는 텍스트를 분석합니다.
색깔 분석은 픽셀로 RGB 데이터를 불러와 **RGB 경계값**을 이용하여 구분하였습니다.
이렇게 얻은 데이터를 csv에 정리하여 기존에 저장되어있는 알약 리스트와 비교합니다.



기타
------------
저희는 이 프로젝트의 내용에서 그치지 않고 스마트폰과의 연계 가능성, 다양한 기능 추가 등을 생각하고 있습니다.   

시스템 구성도
------------------
![시스템구성도](https://user-images.githubusercontent.com/84956281/132693665-40c7fbc3-ce68-42d4-9824-7d6ade9f4174.jpg)


구성
-------------
S/W   
IDE: **Jupyter Notebook / Thonny**   
Server: **Flask**   
Language: **Python**   
Collaboration Tool: **Git**   

H/W   
**Raspberry Pi 3
PIR censor   
Camera censor   
Speaker**   

작품
----------
![3](https://user-images.githubusercontent.com/84956281/132686813-1a54074d-4197-47a4-affe-6c515d5416fa.JPG)

WING-IT
--------------
**팀장: 차수빈   
팀원: 권오제**   

링크
-------------
[Youtube](https://youtu.be/qqIU9Of07pI)
