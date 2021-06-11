# MASL

*(ver 2.0 - on-going since 2021.03.25)*<br/>
마슬은 내가 살기 좋은 동네의 다양한 정보를 알려주는 웹서비스입니다.<br/>
거주지 추천 서비스에서 진화한 지역 주천 알고리즘과 다양한 지역 정보를 알려주는 웹 서비스입니다.

*(ver 1.0 - expired since 2021.03.24)*<br/>
**슬세권**은 슬리퍼를 신고 다닐 수 있는 거리에 자주 이용하는 시설들이 있는 권역을 의미합니다.  
MASL은 사용자의 선호에 따라 **슬세권**을 파악하여 꼭 맞는 거주지를 추천하는 웹 서비스입니다.

## 🧑‍💻 마슬은 현재 다음과 같은 스택을 사용하고 있습니다!

1. BackEnd : Python / Flask
2. FrontEnd : React
3. Database : MongoDB
4. External API : KakaoMap Api
5. Server : Ubuntu 18.04 LTS
6. VM : Azure / Docker

## 💻  현재 서비스 프로세스

1. 사용자 정보 수집(현거주지, 직장위치, 자주 이용하는 매장 등 사용자 선호정보 수집)
2. 서울 지역정보 수집
3. 지역정보 데이터베이스화
4. 사용자 정보와 데이터베이스를 이용해 추천 리스트 TOP5 생성
5. 웹으로 결과 제공

## Getting Started

프로젝트를 git clone 합니다.
```
> git clone https://kdt-gitlab.elice.io/Jungwoo/masl.git
```

### Prerequisites

해당하는 프로그램의 설치가 필요합니다.

- MongoDB  
```
> cd masl
> wget https://fastdl.mongodb.org/linux/mongodb-linux-x86_64-ubuntu1804-4.4.4.tgz
> tar xvfz mongodb-linux-x86_64-ubuntu1804-4.4.4.tgz
> sudo mv mongodb-linux-x86_64-ubuntu1804-4.4.4 /usr/local/mongodb
> sudo chown {USER NAME} ./data/db
> vi ~/.bash_profile
```
환경변수를 작성합니다.
```
    export MONGO_PATH=/usr/local/mongodb

    export PATH=$PATH:$MONGO_PATH/bin
```
환경변수를 빌드합니다.
```
> source ~/.bash_profile
> mongod --dbpath=data/db
```
- Python  
```
> sudo apt-get install python3 python3-pip
```
- Node.js
```
> curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -
> sudo apt-get install -y nodejs
```

### Installing

아래 사항들로 현 프로젝트에 관한 모듈들을 설치할 수 있습니다.

- Python Packages
```
> cd masl
> pip3 install -r requirements.txt
```
- Node Modules
```
> cd masl/client
> npm i
```

## Running

1. Terminal 1에서 다음 명령어를 실행합니다.
```
> cd masl
> mongo
```
2. Terminal 2에서 다음 명령어를 실행합니다.
```
> cd masl
> flask run -h localhost -p 8080
```
3. Terminal 3에서 다음 명령어를 실행합니다.
```
> cd masl/client
> npm start
```

## Deployment

- Microsoft Azure VM
- Ubuntu 18.04

## Built With (link to Github)

*(ver 2.0 - on-going since 2021.03.25)*<br/>
* [황정우](https://github.com/ltxctdbnn ) - PO / Back-End
* [배재욱]() - PM / Back-End / Back Team Leader
* [정성헌](https://github.com/Heon4856) - Back-End
* [하성민](https://github.com/makeitmin) - Front-End / Front Team Leader
* [김수영](https://github.com/ksy9926) - Front-End
* [윤맑은이슬](https://github.com/irisdew) - Front-End
* [박정환](https://github.com/JeongHwan-dev) - Front-End

*(ver 1.0 - expired since 2021.03.24)*<br/>
* [황정우](https://github.com/ltxctdbnn ) - Product Owner
* [김수영](https://github.com/ksy9926) - Back-End / Algorithm
* [하성민](https://github.com/makeitmin) - Front-End / Data

## License
