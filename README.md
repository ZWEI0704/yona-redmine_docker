# docker-yona

![License](https://img.shields.io/github/license/mashape/apistatus.svg)
[![Build Status](https://travis-ci.org/pokev25/docker-yona.svg)](https://travis-ci.org/pokev25/docker-yona)


**yona-redmine_docker**는 [Yona](http://yona.io)와 [Redmine](http://www.redmine.org/)을 한 번에 사용하는 docker-compose 입니다.
만약 둘 중 하나만 사용하기 원하신다면 docker-compose.yml에서 해당 부분을 삭제하고 사용하시면 됩니다.

window 11, Ubuntu 22.04 LTS에서 정상 작동하는 것을 확인했습니다.

## Software Version
- yona:1.16.0
- redmine:latest
- mariadb:10.3


## 사용방법

1. **server-data를 압축해제하세요.**  
  default 설정으로는 docker-compose.yml이 있는 폴더에 server-data 폴더가 있어야 합니다.

2. **docker-compose.yml을 Customize하세요.**  
   Default 설정으로 실행해도 정상적으로 작동합니다.  
   docker-compose.yml 에서 server-data 폴더에 yona, redmine, mariadb의 모든 데이터가 모이도록 했습니다.
   > 만약 저장 장소를 바꾸고 싶다면 docker-compose.yml에서 volume의 위치를 변경하십시오.  
   > yona, redmine, mariadb 모두 데이터 저장 장소를 변경할 수 있습니다.  
   
   yona, redmine의 ports를 변경하여 자신이 필요한 ports로 할당할 수 있습니다.
   > default 설정으로는 yona가 9000, redmine이 9001입니다.

3. **dokcer-compose를 통해 서버를 실행하세요.**  
   ```
   docker-compose up -d
   ```

4. **초기 설정**  
   yona와 redmine에 접속하여 admin 초기 설정을 진행하세요.

5. **서버 재시작**  
   초기 설정을 마치면 서버를 재시작해야 정상 작동합니다.
   ```
   docker-compose restart
   ```


## License
The MIT License (MIT)

Copyright (c) 2014 SungKwang Song

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
