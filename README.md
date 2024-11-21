# Cafe_in
## 프로젝트 소개
네이버지도의 댓글 데이터들을 크롤링 합니다. 크롤링한 데이터들을 자연어처리 하고 지역과 키워드에 따라 카페를 추천하는 프로그램입니다.
## 구성인원
4명
## 기술 스택
![a](https://img.shields.io/badge/Python-14354C?style=for-the-badge&logo=python&logoColor=white) ![b](https://img.shields.io/badge/Selenium-43B02A?style=for-the-badge&logo=selenium&logoColor=white) ![c](https://img.shields.io/badge/Pandas-FF6F00?style=for-the-badge&logo=pandas&logoColor=white) ![d](https://img.shields.io/badge/NLP-FF6F00?style=for-the-badge&logo=nlp&logoColor=white)
## 역할
자연어처리를 담당했습니다. 또한 크롤링 과정에서 발생하는 문제 해결에 참여했습니다.
## 문제
1. 1) 네이버 지도에서 리뷰 버튼을 눌러 들어가야 하는데 카페마다 리뷰 버튼의 위치가 다른경우 발생. 이전의 XPATH의 인덱스를 활용한 크롤링 방식 사용 불가. 
   2) 다른 페이지는 크롤링이 잘 되는데 네이버 지도에서만 안되는 현상 발생.   
2. 자연어처리를 어떻게 할 것인가
## 문제 해결 방안
1. 1) 리뷰버튼의 클래스는 항상 같다는걸 확인하고 CLASS_NAME을 이용했습니다.
    2) 네이버 지도의 블록 영역마다 frame이 다른것을 확인하고 frame을 변경해가며 크롤링했습니다.
2. 모든 리뷰 토큰화 - 불용어 제거 - TFIDF적용 - Word2vec적용과 같은 방식으로 자연어 처리를 했습니다.
## 결과
원하는 지역과 키워드를 통해 카페추천해주는 프로그램 구현
## 고찰
최신 댓글데이터를 반영하려면 매번 크롤링 하고 자연어처리를 해야 하는 불편함이 있습니다. 
## 시연영상
### 메뉴로 검색
<img src="./img_video/find_by_menu.gif" width=450 height=250>
영상 설명<br/>
1. 원하는 지역을 선택하고 원하는 메뉴를 입력합니다.<br/>
2. 가장 상단에 추천된 카페를 검색하여 원하는 메뉴에 대해 적절한 카페가 추천되었는지 확인합니다.<br/><br/>
  
[원본영상](https://github.com/BrotherHwan/Cafe_in/blob/main/img_video/find_by_menu.mp4)(이 링크의 raw file 다운로드시 좀 더 크고 명확한 영상을 확인하실 수 있습니다. )



### 특징으로 검색
<img src="./img_video/find_by_keyword.gif" width=450 height=250>
영상 설명<br/>
1. 원하는 지역을 선택하고 원하는 특징을 입력합니다.<br/>
2. 가장 상단에 추천된 카페를 검색하여 원하는 특징에 대해 적절한 카페가 추천되었는지 확인합니다.<br/><br/>

[원본영상](https://github.com/BrotherHwan/Cafe_in/blob/main/img_video/find_by_keyword.mp4)









