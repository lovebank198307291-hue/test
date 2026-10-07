# WORK SAFE NOTE 업데이트 서버

앱은 실행할 때 `version.json`을 확인합니다.

## 새 버전 배포 방법
1. Android Studio에서 기존과 **같은 서명키**로 APK를 빌드합니다.
2. 이 저장소의 GitHub **Releases**에서 새 Release를 만듭니다.
3. APK 파일명을 반드시 `WORK_SAFE_NOTE.apk`로 해서 Release asset으로 올립니다.
4. `version.json`의 `versionCode`와 `versionName`을 새 앱 버전으로 올립니다.
5. 앱을 실행하면 새 버전을 감지하고, 사용자 확인 후 APK를 자동 다운로드한 다음 Android 설치 화면을 엽니다.

## 중요
- package/applicationId: `com.worksafenote.app`
- 기존 앱 위에 업데이트하려면 같은 서명키를 계속 사용해야 합니다.
- Android 8 이상에서는 최초 1회 '알 수 없는 앱 설치' 허용이 필요할 수 있습니다.
