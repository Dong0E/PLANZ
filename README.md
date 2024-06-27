# PLANZ
![image](https://github.com/Dong0E/PLANZ/assets/168512107/caccefb9-18f8-479a-b0eb-422c36812835)

+ ### SpringFramework를 이용한 여행일정 관리 및 추천 웹 프로젝트

## 프로젝트 기간

+ #### 2024.05.27 ~ 2024.06.21

## 개발 인원

+ #### 6명(팀프로젝트)

## 프로젝트 목적

+ #### 사용자가 여행 전 계획을 세울 때 어려움을 겪지 않도록 서포트 해줄 수 있는 웹 개발
  

## 개발환경

+ #### O/S : window10
+ #### Server : Apache Tomcat 8.5
+ #### DB : Database Management System (DBMS): MySQL8.0.36
+ #### Framwork/Flatform : Spring, Mybatis, jQuery, Thymeleaf
+ #### Language : Java, Javascript, HTML5, CSS3
+ #### Tool : Eclipse, GitHub, Git(Source Tree), SQL Developer

## 구현 부분

+ #### 게시판 페이지 (board/list.html)
![image](https://github.com/Dong0E/PLANZ/assets/168512107/a46480ac-a8f9-4e75-b779-3b557c88baac)


  + ##### 로그인에 상관없이 해당 페이지를 열람 할 수 있습니다.
  + ##### 가장 먼저 작성된 게시글이 먼저 보이게 되며 게시글을 클릭시 상세보기가 가능합니다.
  + ##### 한페이지에 20개씩 나타나며 게시판 하단에 페이징, 검색 기능을 이용할 수 있습니다.
  + ##### Spring Boot 컨트롤러는 'Criteria' 객체를 통해 페이징 정보를 받아와 서비스 계층을 통해 해당하는 게시물 목록을 가져오고, 이를 모델에 추가하여 뷰에서 사용할 수 있게 합니다. 뷰에서는 Thymeleaf 템플릿을 통해 동적으로 생성된 HTML을 렌더링하여 사용자에게 게시물 목록을 보여줍니다. MyBatis 매퍼는 SQL 쿼리를 통해 데이터베이스에서 필요한 데이터를 가져오고, 페이징과 검색 조건에 맞는 쿼리를 생성합니다.
 
  + #### list.html의 일부
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/d85dfb2b-a52e-4405-8985-8625adc6631e)
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/f9648a09-e114-4bdf-8d7c-badfb2ba0234)
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/93ff2aac-59e1-4a5f-890a-4d64fe151a5f)

  + #### BoardController의 일부
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/e67d4772-8579-4a42-b883-0ae116531d7c)

  + #### Criteria
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/98f5d5ca-b98c-4ca5-ad5a-f99ee479348a)

  + #### PageDTO
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/3de21aeb-6117-4efa-a9ea-d53e7559f14f)

  + #### BoardServicelmpl의 일부
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/9a30a90b-70cd-4912-a460-ad11acf27235)

  + #### BoardMapper의 일부
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/df6299a4-3d5b-4e01-b289-aa9ea117849d)
  
  + #### board.xml의 일부
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/0299b97a-9e4e-4b68-afe0-e46ba98572e7)
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/ba1f0386-dd09-4aa2-b952-1f16c0be9a36)



+ #### 여행지추천 더보기 페이지 (region/regionAddView.html)
![image](https://github.com/Dong0E/PLANZ/assets/168512107/8ecb16da-d6f7-4739-94d7-7f52ded0b244)



  + ##### 사용자는 지역을 선택하여 추천 여행지를 열람할 수 있습니다.
  + ##### 공공데이터API를 이용하여 데이터를 AJAX를 통해 동적으로 불러와 화면에 출력하는 기능이 구현되어있습니다.
 
  
  + #### regionAddView의 일부
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/cc1da91b-6619-45c3-b009-55d9fa88ef73)
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/9e29a032-88ad-4223-ad27-bff8f47a9d56)

  + #### APIController의 일부
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/814a9c85-0f43-47a4-9abb-bbc8c55db439)
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/6135ff55-7df1-494c-9cae-3910c032e9e9)



+ #### 마이페이지의 충전탭 (user/mypage)
![image](https://github.com/Dong0E/PLANZ/assets/168512107/49c33489-4faf-45d4-ac94-ff31ffbf1fd0)
![image](https://github.com/Dong0E/PLANZ/assets/168512107/ba733fe2-d69e-4051-86ef-24bab27155e4)


  + ##### 포트원 KG이니시스 종합결제API를 이용하여 사이트 화폐인 코인을 충전할 수 있습니다.
  + ##### 결제 금액을 선택 or 직접입력할 수 있으며 선택 후 에는 보유한 코인과 충전한 코인을 볼 수 있습니다 금액 설정 후 결제수단 휴대폰, 카드, 문화상품권 중 하나를 선택 한 후에 결제하기 버튼을 누르면 KG이니시스 통합결제API 팝업창을 통해 결제를 진행 할 수 있습니다.

  + #### mypage.html의 일부
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/367b3ed8-4ee9-43ae-b090-3aa5a6a244e0)
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/b080b2a5-e944-4d55-ab4e-a9077ec26eda)
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/b9d3f91e-93f1-4c87-a7d0-72271b3b0ba7)
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/c3c0439b-b7c5-4cf7-948b-1128fcd42462)
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/dacc5b36-d54c-49ed-855c-8c04b7de1962)
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/3799a7a0-d913-480b-993a-3d115c28570f)
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/850b2ee4-c0a5-4e06-8152-67daac96f62a)


+ ### 마이페이지의 내정보수정탭 (user/mypage)
![image](https://github.com/Dong0E/PLANZ/assets/168512107/8360f5ee-ee35-4f52-a88b-d22415a08a2a)
![image](https://github.com/Dong0E/PLANZ/assets/168512107/3f453d4c-5c25-4f3e-9637-be55b4a088d5)
![image](https://github.com/Dong0E/PLANZ/assets/168512107/5d122552-abcf-411d-8e9f-cd8ab0a3f6a5)
![image](https://github.com/Dong0E/PLANZ/assets/168512107/ccf0d949-2e0c-4fa7-951e-286a9721dbd2)


  + ##### 다음우편번호찾기API, coolsms문자보내기API, 파일업로드 등을 이용한 내정보수정 기능이 구현되어있습니다.
  + ##### 간편로그인(네이버, 구글, 카카오)이용자인지 일반 회원가입 이용자인지에 따라 로그인 상태를 볼 수 있습니다.
  + ##### 간편로그인(네이버,구글, 카카오)이용자는 프로필사진과 회원탈퇴만 지원하며 일반 회원가입 유저는 프로필사진, 비밀번호, 전화번호, 이메일, 주소 등의 수정을 지원합니다.

  + #### mypage.html 일부
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/aa16c608-7a49-4f54-b065-b2e0151a5d12)
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/8a54a917-bb28-4474-877f-72deb25bbd0f)
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/9f003954-50f6-4aec-a6cd-a852c5d2b153)
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/dea7ee6b-8ebc-4e0e-a572-3cab68d29216)
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/cd0bcf7a-54a7-4d1e-a38a-4fb18bb1e55f)
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/8cf30cb3-6b26-4ebe-b534-a67617f9dbca)
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/801c23e7-b298-443e-8e03-bd922e6a7b3d)
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/14b36763-20f8-4359-b3ff-156ccfa70702)
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/2368f780-0da9-4a0a-8c6c-c56cf8feec36)

  + #### UserController의 일부
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/1d820e83-ea24-4fe5-b4ad-10cfe83ee4e8)
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/742ba45f-94df-4b88-be3f-4b768a8cedfc)
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/cb3af2ab-4812-46c6-97db-5069f9f57803)
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/38219a27-d228-4258-81e9-32f3345f6c6e)
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/bc67f59f-92d6-4442-a9b6-720c5b275e4b)
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/694acd3b-63f4-4ea5-9d4e-14fe36749bda)
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/2bfb817a-83c7-49f1-9778-dfecbc6a5d07)
  ![image](https://github.com/Dong0E/PLANZ/assets/168512107/3c419d38-e596-474a-85fb-fb6e16279f31)


## Flowchart
![image](https://github.com/Dong0E/PLANZ/assets/168512107/86941e8e-9499-47a7-a884-fee22ab1b75d)

## ERD
https://dbdiagram.io/d/667ba4819939893dae47edb4
![image](https://github.com/Dong0E/PLANZ/assets/168512107/206c1356-01f8-43ce-9626-5663dd95500a)






  




  

