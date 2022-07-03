# Papago Alfred Workflow

apikey 발급이 필요없는 파파고 번역

- papago: nodejs 필요한 버전 크기 120KB
- papago.alfy: nodejs 없어도 되는 버전 3.6MB

## requirements

- 알프레드 유료 버전
- (nodejs)

## keyword
- ppgak - 언어감지 -> 한국어
- ppgke - 한국어 -> 영어
- ppgek - 영어 -> 한국어

## 새로운 언어 워크플로우 추가하는 방법

1. script filter(오른쪽 클릭 -> input -> script filter) 생성
2. Language를 /bin/bash
3. (nodejs 있어야 하는 버전) /usr/local/bin/node main.js [언어1] [언어2] "$1"
3-1. (nodejs 없어도 되는 버전) ./node_modules/.bin/run-node main.js [언어1] [언어2] "$1"

   - 언어1에서 언어2로 번역됨
   - 언어1, 언어2는 아래의 단축어로 써야함
   - ex) /usr/local/bin/node main.js en ko "$1" (영어 -> 한국어)
   - ex) /usr/local/bin/node main.js ko en "$1" (한국어 -> 영어)
   - ex) /usr/local/bin/node main.js zh-CN ko "$1" (중국어 -> 한국어)

     - auto - 언어감지
     - ko - 한국어
     - en - 영어
     - es - 스페인어
     - fr - 프랑스어
     - id - 인도네이사어
     - ja - 일본어
     - th - 태국어
     - vi - 베트남어
     - zh-CN - 중국어 간체
     - zh-TW - 중국어 번체
     - de - 독일어
     - ru - 러시아어
     - pt - 포루투갈어
     - hi - 힌디어
     - it - 이탈리아어
