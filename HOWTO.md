https://randomnerdtutorials.com/getting-started-with-home-assistant-on-raspberry-pi/
## 1.라즈베리 파이 세팅
파이 imager에 가서 Homeassistance OS RPI 5를 다운
### 접속
In the browser of your desktop system, enter homeassistant.local:8123
If you are running an older Windows version or have a stricter network configuration, you might need to access Home Assistant at homeassistant:8123 or http://X.X.X.X:8123 (replace X.X.X.X with your Raspberry Pi’s IP address).
### 세팅

https://github.com/home-assistant/operating-system/releases/download/17.3/haos_rpi5-64-17.3.img.xz 

여기에서 다운

## 2. 
1.Go to https://etcher.io/ and install Etcher on your computer. Select the appropriate installation for your operating system.
2.open Etcher and click on Select image. Open the image
3.라즈베리 SD카드 확인, 라즈베리 파이 켜기!
4.http://hassio.local:8123 or go to  http://your-pi-ip-address:8123 접속

### samba share 애드온 설치
홈 어시스턴트에서 Hass.Io를 선택하기

samba share add on 활성화하기

### SSH 애드온 설치
Hass.io 탭에서 SSH server 찾고, 옵션에서 
```bash
{
"authorized_keys": [],
"password": "yourownpassword"
}
```
save 하기
Open SSH install 하기

### pi rebooting
라즈베리 파이 리부팅이 필요해요

windows는 Putty 를 사용합니다.
https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html
Port 22 로 라즈베리 파이 ip를 입력하고 오픈, 경고 메세지면 yes 클릭하기
root로 로그인하고 아까 설정해둔 비밀번호 입력

### configuration.yaml 
컴퓨터 폴더에서 network 디바이스 간뒤 HASSIO 있는지 확인 & 선택
config 폴더 선택, configuration.yaml 
```bash
# api_password: PASSWORD
```
에서 비밀번호 입력하고 주석처리 해제
### 세이브
파일을 저장하고 홈 어시스턴트에 가서 Configuration에 갑니다
General를 선택하고 CHECK CONFIG 버튼을 누릅니다! (파일과 싱크)
같은 탭에서 Server Management 창에서 RESTART를 누릅니다

### 더하기
To add components to the configuration.yaml file go to https://home-assistant.io/components/ and search for the desired components.


