## React-native

React native는 하단과 같은 구조로 이루어져 있음.

![스크린샷 2024-04-07 오후 9 48 59](https://github.com/1GYOU1/React-native/assets/90018379/666dc3f7-0207-40e0-a7b3-4f3ac4681fb0)

![스크린샷 2024-04-07 오후 11 15 15](https://github.com/1GYOU1/React-native/assets/90018379/88d73878-e5b8-49e7-a761-a506a34dd9fe)

![스크린샷 2024-04-07 오후 11 18 20](https://github.com/1GYOU1/React-native/assets/90018379/828210a0-0b9a-4ef5-9ce2-6708868d84d5)

개발 환경 세팅 종류

Expo cli
- 간단하게 코드를 테스트 하기 위한 용도로 많이 쓰임.
- javascript, markup/styling 빼고 모든 인프라가 갖춰져 있음. 컴파일 필요 X
- 폰에서 즉시 코드(javascript, markup/styling)를 미리보기 테스트를 할 수 있음.

cli
- 전문가 사용
- Xcode, java, 시뮬레이터 등등 여러가지의 설치가 필요함
- Xcode, java로 모든 인프라를 가져와서 .apk - aos, .ipa - ios 안에 넣어주고 그 후에 app store에 보내짐

<br>

### expo로 app 만들기

1. node 설치

>$ brew install node

2. expo 개발 환경 세팅 (참고 url - https://docs.expo.dev)

>$ npm install --global expo-cli

3. Watchman 설치 - 맥 사용자만 해당

>$ brew install watchman

4. 휴대폰에 Expo App 다운로드
- ios app store  - Expo Go 어플 다운
- aos google play store - Expo 어플 다운