개돼지 사료 배급기
- `App Player`/`Internet Browser`등 아무것도 필요없는 모바일 게임 바람의나라:연 쿠폰 아이템 자동 수령 프로그램

## 개발환경
- Visual Studio 2019 Community
- Windows 10 64bit
- WPF C#
- .Net Framework 4.7.2
- Fiddler 4 / Fiddler Extension – Request to Code

## 배포
- 하지않습니다.


## 사용법
1. `coupon.txt` 파일에 `쿠폰코드`를 한줄에 하나씩 작성하고 저장한다.
2. `character.txt` 파일에 쿠폰 아이템을 수령하고 싶은 `캐릭터이름` `서버` `회원코드`에 해당하는 정보를 작성한다.
    - ex) 캐릭명 연 123123123
    - 여러 계정일 경우 각 줄마다 각각의 계정에 해당하는 정보를 작성하고 한다. 
3. 위의 `coupon.txt` 및 `character.txt` 파일을 실행 프로그램과 같은 경로에 두고 프로그램을 실행시킨다.
4. `coupon.txt`/`character.txt`에 작성한 정보가 정확하게 프로그램에 나타나는지 확인 후 `start` 버튼을 누른다.
5.  완료 알림음이 들리면 `log`를 확인한다.

## log 형식
- [시간:분:초] [회원코드] 쿠폰코드 결과코드 결과메세지

## 알아두면 좋은점
- 걸리는 시간은 프로그램 실행 환경에 따라, 웹 서버 상태에 따라 상이합니다. ( 실제 테스트 결과 쿠폰 10개 1-2초 X, 쿠폰 하나당 1초 미만 ) 
- 작성한 정보는 서버에서 `회원코드 유효성` -> `쿠폰코드 유효성` -> `사용 가능 여부` -> 프로그램에서 `서버 및 캐릭터 이름 일치 여부` 순서로 검증한다.
- httpwebrequest를 이용해서 `https://mcoupon.nexon.com/baramy` 서버와 직접 통신하므로 `App Player`/`Internet Browser`등이 필요없다.
- 내가 쓰려고 내가 만든 프로그램. (WPF C# 5일차 2021-11-25)

## 시연
1. `coupon.txt` 및 `character.txt` 작성 및 저장.

![image](https://user-images.githubusercontent.com/94805997/142789452-1e288def-1fe3-4abb-8241-db6b201364ae.png)

2. 프로그램 실행.

![image](https://user-images.githubusercontent.com/94805997/143262873-60b53c45-2dc6-49b0-9727-1d74f1a73c0e.png)

3. demo.

![image](https://github.com/tester58126/BaramYeonCoupon/blob/main/image/3.gif)
