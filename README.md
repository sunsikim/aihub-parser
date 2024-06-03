# aihub-parser

AI 허브에서 제공하는 공개 데이터별 파싱 로직 정리

## aihubshell 다운로드

[여기](https://aihub.or.kr/devsport/apishell/list.do?currMenu=403&topMenu=100) 설명되어 있는대로 aihubshell 설치해 CLI에서 데이터셋 다운받을 수 있도록 준비

```
curl -o "aihubshell" https://api.aihub.or.kr/api/aihubshell.do
chmod +x aihubshell
sudo cp aihubshell /usr/bin  # 맥 환경이면 /usr/local/bin
```

환경변수 사용해서 인증정보 입력

```
export AIHUB_ID=aihub@aihub.or.kr
export AIHUB_PW='12345!@#$%aihub12345!@#$%'
```

또는, CLI 실행될 때마다 자동으로 이 정보가 입력되도록 `.bashrc` 등에 인증정보 입력

## aihubshell 커맨드

```
which aihubshell  # /usr/bin/aihubshell 또는 /usr/local/bin/aihubshell
aihubshell -help
aihubshell -mode l | grep 말뭉치
aihubshell -mode l -datasetkey 625
aihubshell -mode d -datasetkey 625 -filekey 62288,62289
```
