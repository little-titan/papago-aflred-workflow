# Papago Alfred Workflow

apikey 발급이 필요없는 파파고 번역

## requirements

- nodejs

## keyword

- ppgke - 한국어 -> 영어
- ppgek - 영어 -> 한국어

## 새로운 언어 워크플로우 추가하는 방법

1. script filter(오른쪽 클릭 -> input -> script filter) 생성
2. Language를 /bin/bash
3. /usr/local/bin/node main.js [언어1] [언어2] "$1"
   - 언어1에서 언어2로 번역됨
   - 언어1, 언어2는 단축어로 써야함
   - ex) /usr/local/bin/node main.js en ko "$1" (영어 -> 한국어)
   - ex) /usr/local/bin/node main.js ko en "$1" (한국어 -> 영어)
   - ex) /usr/local/bin/node main.js cn ko "$1" (중국어 -> 한국어)
