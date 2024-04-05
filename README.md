<div align="center">
 
 # 📫 청년정책 알라미
<br>

**전체 개발 기간**<br>
2024.04.01 ~ 04.03
<br>

**팀원**<br>
김지혜 (Wisdom-Kim)<br>
서형종 (aeeoou)

</div>

## 목차
1. [프로젝트 소개](#프로젝트-소개)

2. [시작 가이드](#시작-가이드)

3. [프로그램 구조](#프로그램-구조)

4. [개선 및 추후 계획](#개선-및-추후-계획)

5. [후기](#후기)
<br>
<br>


## 프로젝트 소개
"[청년몽땅정보통](https://youth.seoul.go.kr/infoData/sprtInfo/list.do?key=2309130006)" 사이트는 서울시 청년 정책에 대한 종합적인 정보를 제공하는 플랫폼이다. 이 프로젝트는 이 사이트를 대상으로 청년 정책에 관심 있는 사용자들에게 필요한 정보를 효율적으로 제공하기 위해 개발되었다. 사용자가 입력한 정보를 기반으로 현재 모집 중인 정책들을 신속하게 검색하고, 해당 정책에 대한 피드를 수집하여 정리하는 편의를 제공한다.
<br>
<br>

## 기능
**📫**
1) **유연한 검색**<br>
사용자의 입력 정보를 활용하여 현재 모집 중인 정책들을 검색한다. 이를 통해 자신에게 필요한 정책을 효율적으로 찾을 수 있다.

2) **자동 피드 수집**<br>
크롤러는 모집 중인 정책에 대한 피드를 자동으로 수집한다. 수집한 데이터를 통해 사용자는 한눈에 다양한 정책들에 대한 정보를 메일로 받아볼 수 있다.

3) **database.txt를 이용하여 중복 제거**
크롤링 시, database.txt에 없는 피드 아이디만 크롤링한다. 즉, 이전에 프로그램 실행 시 받아봤던 정책 내용은 다시 보내지 않는다.

4) **정보 객체화**<br>
크롤링한 정보를 메세지 객체로 변환하여 리스트에 담아둔다. 이를 통해 사용자는 각 정책에 대한 정보를 구조적으로 쉽게 확인할 수 있다.

5) **예외 처리 기능**<br>
개별 정책 소개 사이트를 대상으로 크롤링할 때, 신청 내용, 신청 기간, 활동 내용 등의 정보가 없는 경우에도 예외 처리를 통해 이미지와 기본 정보를 함께 제공한다. 이를 통해 필요한 정보를 놓치지 않고 확인할 수 있다.
<br>
<br>

## 시작 가이드
**🚗**

- 개발 환경 : Anaconda 22.9.0 / Python 3.10.1

- 버전 및 이슈관리 : Github / Github Issues

- 협업 툴 : Github, Notion

- 사용 방법<br>
**1) Clone the repo**
```
git clone https://github.com/Wisdom-Kim/SIAT_python_crawling.git
```
**2) Install libraries**
>셀레니움 사용을 위한 chromedriver.exe도 해당 repo 폴더에 넣어주세요.<br>
chromedriver.exe는 https://chromedriver.chromium.org/downloads 에서 받을 수 있습니다.

```
pip install selenium
pip install python-dotenv
pip install typing-extensions
```
**3) run main.py**
<br>
<br>


## 프로그램 구조
```
mail.py - 메일링 기능 관련
policy.py - 정책 객체
interface.py - tkinter을 이용한 GUI (버튼을 이용한 비동기 이벤트가 불가능하여 사용하지 못함)
old_interface.py- 일반 터미널을 이용한 GUI
py_html.py - 정책객체를 이용하여 이메일에 첨부할 html을 작성
custom_filter - 유저로부터 UI로 입력받아 생성 될 필터 객체
crawling_manager - url 크롤링 후,크롤링한 객체를 기반으로 정책 리스트 생성
```
## 개선 및 추후 계획

**💭**
* database.txt말고 진짜 DB 사용해보기
* 이번 주 마감인 정책은 한 번 더 보내줄 수 없을까?
* 필터 조건을 다중으로 걸 순 없을까? (카테고리 다중 선택)
<br>
<br>

## 버그
**🐛**
* 사이트 자체 버그
> 사이트 자체에서 필터링이 잘 작동하지 않아, 문제가 되었던 부분인 자치구 단위의 세부 필터링은 하지 못했습니다. 자치구를 입력하면, 해당 자치구 포함 인근 지역의 정책을 알려주는 방향으로 해결했습니다.

## 후기
**💬**

**지혜**
<br>
뒤로 갈수록 머리가 깨질 것 같았습니다...<br>
항상 기능 별 테스트 코드를 작성해봐야하는구나 여실히 깨달을 수 있었습니다<br>
수고 많으셨어요~
<br>
<br>

**형종**
<br>
처음으로 해보는 협업이라 개인적으로 재미있게 작업했지만 한편으로는 무기력, 암울함을 많이 느낀 프로젝트였습니다. 다시는 이런 대참사가 일어나지 않도록 정진하여 돌아오겠습니다.😥 지혜님 정말~ 고생 많으셨습니다!!😂
<br>
<br>
<br>
<br>
<br>

<div align="right"> 

[목차로 돌아가기](#목차)
