# 해커톤 - 사람인 공고 비교하기 서비스

![헬로메가바이트해커톤 타이포 로고 (다크버전)](https://user-images.githubusercontent.com/41669026/155953674-59da535d-0667-4423-baca-8625fdc1b3ff.png)

![해커톤 결과](https://user-images.githubusercontent.com/41669026/155930069-c67f54e2-6729-4415-9952-ddd854e9b3ef.png)

### UX/UI
황지선

### FE
전도현 이동수

### BE
양승훈 정이수


## 개발목록
- grid 레이아웃을 주로 활용해 사용자가 공고를 비교하기 쉽게 개발
- react-query를 활용한 데이터 캐싱 및 fetch
- 관심 공고를 직접 선택하여 평행하게 나열하여 비교할 수 있게 개발
- 관심 공고 내 비교 항목들을 선택하여 항목별로 비교 가능하게 개발
- recoil을 이용한 비교 항목들 저장, 항목별 status 상태관리, atom get을 이용해 status별 데이터 return
---
![image](https://user-images.githubusercontent.com/41669026/158429031-ccac52da-ea57-47e2-bb31-db3868c5b48f.png)

최초의 비교공고 데이터는 react-query를 사용해 fetch하여 가져와 뿌려주며, 스크랩한 공고 목록은 recoil로 상태관리를 합니다.

관심공고를 스크랩하면 아래 사진과 같이 카테고리별로 공고를 비교할 수 있게 됩니다.

![image](https://user-images.githubusercontent.com/41669026/158428736-031e1631-2335-4164-a7de-6d8508779a9c.png)

상단의 비교항목선택 카테고리 버튼 클릭시 해당 카테고리가 활성화/비활성화 처리가 되며 비교중인 공고의 데이터도 함께 활성화/비활성화가 됩니다. 

![카테고리1](https://user-images.githubusercontent.com/41669026/158430398-2c1aaad0-17b7-40f9-9b5c-9eea47d7701d.PNG)
![카테고리2](https://user-images.githubusercontent.com/41669026/158430400-45c3aa56-f349-42f8-9b9d-20b5f68e7da6.PNG)

카테고리별 데이터는 recoil을 통해 관리하게 됩니다. 카테고리 버튼 클릭시 활성화/비활성화가 되므로 해당 버튼을 클릭시 마다 
공고 데이터 배열을 재생성하여 보여지게 됩니다.

![상태별 공고 리스트](https://user-images.githubusercontent.com/41669026/158431441-e2cf50f6-ac99-4db2-91f9-918f72ed9c97.PNG)

status 변수는 상수로 관리하였으며, 전체공고, 스크랩한 공고, 스크랩 취소한 공고 리스트들을 selector와 get을 사용하여 status별로 배열을 뽑아낼 수 있게 하였습니다.


---

## UI figma URL
- https://www.figma.com/file/Y9Y4AUiRfRqouvnYcRMOPk/%ED%95%B4%EC%BB%A4%ED%86%A4?node-id=26%3A4

## 기획자료

![살려조_최종발표_page-0001](https://user-images.githubusercontent.com/41669026/155253354-0fced7dc-d3d4-4215-83f9-61ea9781019c.jpg)
![살려조_최종발표_page-0002](https://user-images.githubusercontent.com/41669026/155253386-87d72986-c77c-4487-843c-3bba3741cd6c.jpg)
![살려조_최종발표_page-0003](https://user-images.githubusercontent.com/41669026/155253383-3eb881ee-cf03-4953-b622-c76fc37abc7b.jpg)
![살려조_최종발표_page-0004](https://user-images.githubusercontent.com/41669026/155253392-792450f4-7b27-4177-a346-d6422bc88a02.jpg)
![살려조_최종발표_page-0005](https://user-images.githubusercontent.com/41669026/155253394-9925cd51-5536-4ee9-a419-44a4e8668ccc.jpg)
![살려조_최종발표_page-0006](https://user-images.githubusercontent.com/41669026/155253395-e91379e2-7034-48cc-be13-80a5130a7b40.jpg)
![살려조_최종발표_page-0007](https://user-images.githubusercontent.com/41669026/155253396-c447f164-a24e-4db1-b2ab-a726707a5406.jpg)
![살려조_최종발표_page-0008](https://user-images.githubusercontent.com/41669026/155253397-43b25d20-2620-4908-a8f5-c5af159f6a47.jpg)
![살려조_최종발표_page-0009](https://user-images.githubusercontent.com/41669026/155253399-bb5bb366-4c75-4a08-bafe-e538b4c037ff.jpg)
![살려조_최종발표_page-0010](https://user-images.githubusercontent.com/41669026/155253401-79a0dcac-f841-4422-8900-317293cc1e5f.jpg)
![살려조_최종발표_page-0011](https://user-images.githubusercontent.com/41669026/155253402-d99a0a6b-45d7-4b71-a009-273ded1fd917.jpg)
![살려조_최종발표_page-0012](https://user-images.githubusercontent.com/41669026/155253403-ce289c1a-9e36-4eca-a80a-6e010474d2dd.jpg)
