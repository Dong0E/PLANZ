# PLANZ
+ ### SpringFramework를 이용한 여행일정 관리 및 추천 웹 프로젝트
![image](https://github.com/Dong0E/PLANZ/assets/168512107/24c8b6d5-9d68-409d-a22d-adecfd2080df)

## 프로젝트 목적

+ ##### 여행일정 계획시 어려움을 겪음
+ ##### 여러 사람들이 함께 여행하게될 때 각자의 사정으로 여행이 무산되는 경우가 빈번하게 발생하며 미리 예약해 두었던 숙소, 여행지 입장권 등을 완전하게 환불받지 못하는 경우가 발생함
+ ##### 개인거래를 통해 예약한 티켓등을 거래하기에는 안전하지 않음
+ ##### 여행동행을 구하는데 어려움

###### 여행일정, 예약상품을 공유 및 판매 기능을 제공하고 동행자를 안전하게 구할 수 있는 기능 구축!

## 프로젝트 기간

+ #### 2024.05.27 ~ 2024.06.21

## 개발 인원

+ #### 6명(팀프로젝트)

## 개발환경

+ #### O/S : window10
+ #### Server : Apache Tomcat 8.5
+ #### DB : Database Management System (DBMS): MySQL8.0.36
+ #### Framwork/Flatform : Spring, Mybatis, jQuery, Thymeleaf
+ #### Language : Java, Javascript, HTML5, CSS3
+ #### Tool : Eclipse, GitHub, Git(Source Tree), SQL Developer

## 구현 부분

+ #### 게시판 페이지 (board/list.html)
![image](https://github.com/Dong0E/PLANZ/assets/168512107/dee0d79d-f249-4381-8929-136dce63ee5a)


  + ##### 로그인에 상관없이 해당 페이지를 열람 할 수 있습니다.
  + ##### 가장 먼저 작성된 게시글이 먼저 보이게 되며 게시글을 클릭시 상세보기가 가능합니다.
  + ##### 한페이지에 20개씩 나타나며 게시판 하단에 페이징, 검색 기능을 이용할 수 있습니다.
  + ##### Spring Boot 컨트롤러는 'Criteria' 객체를 통해 페이징 정보를 받아와 서비스 계층을 통해 해당하는 게시물 목록을 가져오고, 이를 모델에 추가하여 뷰에서 사용할 수 있게 합니다. 뷰에서는 Thymeleaf 템플릿을 통해 동적으로 생성된 HTML을 렌더링하여 사용자에게 게시물 목록을 보여줍니다. MyBatis 매퍼는 SQL 쿼리를 통해 데이터베이스에서 필요한 데이터를 가져오고, 페이징과 검색 조건에 맞는 쿼리를 생성합니다.
 
  + #### list.html의 일부

  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/cb9afa58-dd6d-4e66-b72d-979767d853a9)
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/dce61863-1fca-4e76-b421-855003d71b1e)


  + #### BoardController의 일부
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/1e058ee7-d5c4-4093-a826-5a28d9567733)

  + #### Criteria
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/c6ce5893-cc58-4cfb-8fe9-1ccec9285376)

  + #### PageDTO
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/0bc1e5de-6170-4d7f-84d2-fe603c195ed8)

  + #### BoardServicelmpl의 일부
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/2bfd344e-8381-466a-9734-47b580d81137)
  
  + #### board.xml의 일부
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/79cdec4f-fbee-43e9-bfcf-032e5856ee2c)
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/2048017e-7db1-4150-870a-94ea1b6fa6ec)




+ #### 여행지추천 더보기 페이지 (region/regionAddView.html)
![image](https://github.com/Dong0E/PLANZ/assets/168512107/25a7efb9-3872-4944-9a9c-e8ff6a084f37)



  + ##### 사용자는 지역을 선택하여 추천 여행지를 열람할 수 있습니다.
  + ##### 공공데이터API를 이용하여 데이터를 AJAX를 통해 동적으로 불러와 화면에 출력하는 기능이 구현되어있습니다.
 
  
  + #### regionAddView의 일부
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/f8d76043-aada-41b0-b9e1-e68d713c7665)
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/93497e2d-5db9-4582-b8fc-9c34bbbf3a3a)

  + #### APIController의 일부
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/689ff8de-ae6e-43ac-8911-2acf46286a2b)
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/71d7a2f8-45ed-4bdc-9ca4-76e47dc18cf2)



+ #### 마이페이지의 충전탭 (user/mypage)
![image](https://github.com/Dong0E/PLANZ/assets/168512107/9f597bd6-25ac-42e8-8abc-2139a38d3baf)
![image](https://github.com/Dong0E/PLANZ/assets/168512107/758ac086-08d6-4c9f-b513-f100f67d6b55)

  + ##### 포트원 KG이니시스 종합결제API를 이용하여 사이트 화폐인 코인을 충전할 수 있습니다.
  + ##### 결제 금액을 선택 or 직접입력할 수 있으며 선택 후 에는 보유한 코인과 충전한 코인을 볼 수 있습니다 금액 설정 후 결제수단 휴대폰, 카드, 문화상품권 중 하나를 선택 한 후에 결제하기 버튼을 누르면 KG이니시스 통합결제API 팝업창을 통해 결제를 진행 할 수 있습니다.

  + #### mypage.html의 일부
![image](https://github.com/Dong0E/PLANZ/assets/168512107/3447a350-c082-4676-a5ef-debc849d979b)
![image](https://github.com/Dong0E/PLANZ/assets/168512107/9afc2890-880f-4a4c-848b-d8c21d1e43c3)



+ ### 마이페이지의 내정보수정탭 (user/mypage)
![image](https://github.com/Dong0E/PLANZ/assets/168512107/009055f9-5b41-49ee-8c33-4be763186912)
![image](https://github.com/Dong0E/PLANZ/assets/168512107/1be6efb0-760c-4fca-b8e7-30d417d6b420)
![image](https://github.com/Dong0E/PLANZ/assets/168512107/dcd0bf5f-5b5e-4988-be49-481db6806a41)
![image](https://github.com/Dong0E/PLANZ/assets/168512107/b345f4de-e088-4900-98f7-9cfa27ed09ab)
![image](https://github.com/Dong0E/PLANZ/assets/168512107/c6fa22ce-1ed1-43a1-bd6b-4356d480fd58)


  + ##### 다음우편번호찾기API, coolsms문자보내기API, 파일업로드 등을 이용한 내정보수정 기능이 구현되어있습니다.
  + ##### 간편로그인(네이버, 구글, 카카오)이용자인지 일반 회원가입 이용자인지에 따라 로그인 상태를 볼 수 있습니다.
  + ##### 간편로그인(네이버,구글, 카카오)이용자는 프로필사진과 회원탈퇴만 지원하며 일반 회원가입 유저는 프로필사진, 비밀번호, 전화번호, 이메일, 주소 등의 수정을 지원합니다.

  + #### mypage.html 일부
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/69a187db-f8a8-43c7-8e42-6238e5a052dc)
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/4e36946e-3201-4860-af7e-ebb017aa91ec)
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/5a87faf9-b756-40b3-afb4-f18e34fb051b)


  + #### UserController의 일부
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/4237c95b-9bf3-405e-bcbd-1250382c99b3)
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/242a5111-31e5-4fb4-ae68-adb3ccc372bb)
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/ee940598-d901-43ae-9aea-88ed6996726d)
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/4eec9c50-8101-42c7-8fbf-08e0d379d3c3)
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/8fbc65b3-6713-41db-a4b0-a5a856162095)
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/a2a29104-ae52-4673-be71-137e58d14b82)


## Flowchart
![image](https://github.com/Dong0E/PLANZ/assets/168512107/f75e18ae-1f7b-43d8-b7b5-91156304c3da)


## ERD
https://dbdiagram.io/d/667ba4819939893dae47edb4
![image](https://github.com/Dong0E/PLANZ/assets/168512107/0c4fe48b-8d71-4e3f-a9a7-8e6782e50899)







  




  

