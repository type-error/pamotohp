# pamotohp : custom photo viewer + frame
* photo viewer mode : 맵 모드, 타일 모드, 슬라이드 모드
* frame : 나무 프레임 + 아크릴 물감

## Server
* web framework
  * spring-boot
    * api
      1. /photo/country/{country}
      2. /photo/date/{date}
      3. /photo/date/{from-date}/{to-date}
      4. /photo/weather/{weather}

* search engine
  * elasticsearch 2.4.1
    * query
      1. findByLocation 
      2. findByDate
      3. findByDateRange
      4. findByFace
      5. findByLandmark

* google drive synchronizer
  ~~1. google 계정 연동(토큰 정보 저장)~~
  2. maven build로 dependencies포함하여 jar생성
  3. google drive에 있는 사진정보를 elastic engine에 추가
  4. 변경되는 사진이 있는지 주기적으로 확인하여 elastic engine에 반영
  5. 추후 google cloud vision api와 결합

<hr/>

## Client
* AngularJS 2

## Hardware
* Raspberrypi 3
