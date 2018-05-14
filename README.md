# run-sdk-mvn-repo
IVE 실행형 SDK 메이븐 저장소

### maven 저장소 추가 ###
Project 루트에 있는 build.gradle에 다음과 같이 SDK가 등록되어 있는 메이븐 저장소를 추가해줍니다.
```
allprojects {
    repositories {
        maven { url "https://raw.githubusercontent.com/i-ve/run-sdk-mvn-repo/master/releases" }
        maven { url "https://raw.githubusercontent.com/i-ve/run-sdk-mvn-repo/master/snapshots" }
    }
}
```

### 의존성 추가 ###
메인 모듈(*Project 루트가 아닙니다*)의 build.gradle에 다음과 같이 Offerwall SDK 모듈에 대한 의존성을 추가합니다.
```
dependencies {
    compile 'kr.ive:ive_run_sdk:{version}'
}
```
* {version} 부분은 최신 버전을 입력하시면 됩니다.
