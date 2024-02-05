# React-native M2 맥북 초기 환경 세팅

공통 설치

1. #### Homebrew 설치
    - https://brew.sh/ko/
2. #### NodeJS 설치

```bash
brew install node
```

## IOS

1. #### rbenv 설치
- `Ruby`의 `2.7.5` 버전이 필요
- `rbenv`는 Ruby를 버전별로 설치하고 관리할 수 있게 도와주는 툴

```bash
$ brew install rbenv
$ rbenv install 2.7.5
$ rbenv global 2.7.5

$ rbenv -v 이건 1.2.0 이 나오는데
$ rbenv versions 이건 2.7.5 라고 잘 나옴.... 쨌든 된거임..!
```

2. #### Cocoapods 설치

```bash
$ brew install cocoapods
$ sudo gem install cocoapods -> 이거 안돼서 brew 사용함
```

3. ### Watchman 설치

```bash
$ brew install watchman
```

4. ### Xcode 설치 - 앱스토어에서 다운로드

5. ### 프로젝트 폴더 진입 후 실행

```bash
npm run ios
```

## AOS

1. ### JDK 설치(macOS에서 Java를 설치하는 명령어)
    
    https://reactnative.dev/docs/environment-setup?guide=native&package-manager=npm&platform=android
    

```bash
brew tap homebrew/cask-versions
brew install --cask zulu17

# Get path to where cask was installed to double-click installer
brew info --cask zulu17
```

- 나는 밑에 껄로 버전 다르게해서 시도해보았으나 안돼서 상단 명령어로 설치함,,
    
```bash
brew tap AdoptOpenJDK/openjdk
brew install --cask adoptopenjdk11
```
    

JAVA 설치 버전, 경로 확인(mac 명령어)

```bash
java -version
```

내 설치 버전 확인 결과

- openjdk version "17.0.10" 2024-01-16 LTS
OpenJDK Runtime Environment Zulu17.48+15-CA (build 17.0.10+7-LTS)
OpenJDK 64-Bit Server VM Zulu17.48+15-CA (build 17.0.10+7-LTS, mixed mode, sharing)

```bash
which java
```

내 설치 경로 확인 결과

- /usr/bin/java

2. ### Android 개발 환경을 구성하기 위한 환경 변수 설정

```bash
vi ~/.zshrc
```

- **`~/.zshrc` 파일 수정:** **`~/.zshrc`**는 Zsh 쉘의 설정 파일로, 사용자 홈 디렉토리에 위치. **`vi ~/.zshrc`** 명령어를 사용하여 이 파일을 편집

```bash
export ANDROID_HOME=$HOME/Library/Android/sdk
export PATH=$PATH:$ANDROID_HOME/emulator
export PATH=$PATH:$ANDROID_HOME/tools
export PATH=$PATH:$ANDROID_HOME/tools/bin
export PATH=$PATH:$ANDROID_HOME/platform-tools
```

- **`ANDROID_HOME` 환경 변수 설정 :**
    - **`export ANDROID_HOME=$HOME/Library/Android/sdk`**: Android SDK의 설치 경로를 지정하는 환경 변수
- **`PATH` 환경 변수 업데이트 :**
    - **`export PATH=$PATH:$ANDROID_HOME/emulator`**: Android 에뮬레이터 실행 파일 경로를 시스템 **`PATH`**에 추가
    - **`export PATH=$PATH:$ANDROID_HOME/tools`**: Android SDK 도구 디렉토리의 실행 파일 경로를 추가
    - **`export PATH=$PATH:$ANDROID_HOME/tools/bin`**: Android SDK 도구의 **`bin`** 디렉토리의 실행 파일 경로를 추가
    - **`export PATH=$PATH:$ANDROID_HOME/platform-tools`**: Android 플랫폼 도구의 실행 파일 경로를 추가
    
- vim 관련 참고 명령어
    
    vim 설정 나가기

```bash
$ ESC + :wq!
```

vim 참고 명령어

```bash
[O]pen Read-Only (읽기 전용으로 열기): 스왑 파일을 무시하고 읽기 전용으로 파일을 엽니다.
[E]dit anyway (그래도 편집): 스왑 파일을 무시하고 파일을 편집합니다. 다른 프로세스가 편집 중인 경우 변경사항이 충돌할 수 있습니다.
[R]ecover (복구): 스왑 파일을 사용하여 파일을 복구합니다. Vim이 비정상적으로 종료된 경우 유용합니다.
[D]elete it (스왑 파일 삭제): 스왑 파일을 삭제하고 파일을 편집합니다.
[Q]uit (종료): 편집을 종료합니다.
[A]bort (중단): 편집을 중단하고 종료합니다.
보통은 [R]ecover나 [E]dit anyway를 선택하여 계속 진행할 수 있습니다. 선택한 후에는 Vim이 정상적으로 열리고, 파일을 저장하고 종료하면 스왑 파일이 삭제됩니다.
```

환경 변수 변경 후에는 터미널을 다시 시작하거나 **`source ~/.zshrc`** 명령어를 사용하여 변경된 환경 변수를 현재 세션에 적용

```bash
**source ~/.zshrc**
```
    

5. #### 프로젝트 폴더 진입 후 실행

```bash
npm run android
```

<br>

---

<br>

- 참고 사이트
    
    https://deku.posstree.com/ko/react-native/install-on-mac/#jdk-%EC%84%A4%EC%B9%98
        
        
    https://reactnative.dev/docs/environment-setup?guide=native&package-manager=npm

    https://reactnative.dev/docs/environment-setup?guide=native&package-manager=npm

    https://deku.posstree.com/ko/react-native/install-on-mac/
        
    https://deku.posstree.com/ko/react-native/install-on-mac/

    https://jpointofviewntoe.tistory.com/12

    https://velog.io/@yeontan0826/error-install-ruby-version

    https://github.com/react-native-community/cli

    https://velog.io/@mari/cocoapods-%EC%84%A4%EC%B9%98-%EC%98%A4%EB%A5%98%EC%99%80-%ED%95%B4%EA%B2%B0-%EB%B0%A9%EB%B2%95

    https://velog.io/@kimsojeong01/MAC-M2-React-Native-%EC%B4%88%EA%B8%B0-%ED%99%98%EA%B2%BD-%EC%84%B8%ED%8C%85%ED%95%98%EA%B8%B0