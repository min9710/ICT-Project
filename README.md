# ICT-Project

## 기획의도
등산로 주변에서 야생동물 등장 시 퇴치하는 시스템 및 어플리케이션을 통해 사용자에게 알리고 관련 정보를 저장하고 분석하는 시스템 제작

## 기능 구현
**1) TCP/IP Socket Programming 및 Linux 기반 Server/Client 개발**

- **TCP/IP 소켓 통신을 이용하여 Server와 Client 간의 데이터 통신 기능을 개발하였습니다.**
- **멀티스레드를 활용하여 다중 접속 서버를 구현하였습니다.**

**2) Jetson Nano**

- **Jetson Nano를 활용해 모델 데이터를 학습시키고, 카메라를 연결해 객체 감지를 하였습니다.**
- **DB와 연동해 객체 감지 시 객체 수, 카메라 ID, 시간과 위치정보를 전송합니다.**

**3) Arduino**

- **Bluetooth와 연동된 Raspberry Pi4 클라이언트를 활용해 객체 감지 시 부저를 통해 경고음을 울리고 LCD에 메시지를 출력하며, 서보 모터를 이용한 퇴치 스프레이를 작동시켜 야생동물을 쫓아냅니다.**

**4) Raspberry Pi 4**

- **Jetson Nano 로부터 데이터를 수신 받을 메인 서버와 앱, Arduino 에 연결할 클라이언트를 생**

**성합니다.**

- **클라이언트는 서버에 접속을 하면 데이터 베이스와 연결을 하고 Jetson Nano 로부터 새로운 데**

**이터가 데이터 베이스에 추가될 때마다 트리거를 이용하여 서버에 클라이언트 ID 와 명령어, 데**

**이터 정보를 송신합니다.**

- **해당 ID 클라이언트는 Application이나 Arduino에 각각 명령어와 데이터 정보를 송신합니다.**

**5) Web & Application**

- **어플리케이션은 클라이언트로 로그인 되어있는 사용자에게 감지된 위치정보를 알리고, 마주쳤을 시 대처 방법을 제공합니다.**
- **웹은 최근 탐지된 DB 테이블을 보여주고 DB 데이터를 그래프를 통해 볼 수 있습니다.**

## 개발환경
- Raspberry Pi4
    
    Linux
    
    C
    
    Maria DB
    
    Apache
    
- Jetson Nano
    
    Yolov5
    
    Python
    
- Arduino Uno
    
    Arduino-ide
    
- Application
    
    Android Studio
    
    Google Map
    
    Java script
