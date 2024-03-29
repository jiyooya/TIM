# 소개
이 프로젝트는 ![스프링](https://img.shields.io/badge/SpringFramework-6DB33F?style=for-the-badge&logo=spring&logoColor=white)와![MySQL](https://img.shields.io/badge/MySQL-00000F?style=for-the-badge&logo=mysql&logoColor=white)을 활용하여 개발된 프로젝트입니다.

# 제작동기💊
약의 특징(글자, 색, 모양, 재형 등)을 선택하여 약 정보를 쉽게 검색할 수 있는 약학정보원 홈페이지의 분류 방식을 참고하여, 사용자가 손쉽게 원하는 상품을 찾을 수 있는 쇼핑몰 형태의 홈페이지를 기획하였습니다.
![image](https://github.com/jiyooya/TIM/assets/127083635/a4c6707b-e926-4f9a-917d-8941ad519353)

# 목표
- 샌드위치 프렌차이즈의 메뉴 커스터마이징 방식과 샐러드 정기 배송 서비스를 제공하는 홈페이지를 벤치마킹하여, 다양한 메뉴를 나만의 레시피로 편리하게 주문하고 즐길 수 있는 샐러드 주문 전용 홈페이지를 구축하였습니다.
![image](https://github.com/jiyooya/TIM/assets/127083635/bd6a8bd2-c3f0-4e77-9a46-da84b0a16950)

# 개발환경
![개발환경](https://github.com/jiyooya/TIM/assets/127083635/4e0e358d-66fd-4bf1-9341-4bd740207834)

# ER 다이어그램
![image](https://github.com/jiyooya/TIM/assets/127083635/a7926940-a2c0-440e-b096-d9f452f72f5a)

# 메뉴 구조
![메뉴구조도](https://github.com/jiyooya/TIM/assets/127083635/a55e6c78-d3dd-4d31-93f1-3d4951fd206f)

# 맡은 역할
- 제가 맡은 역할은 로그인한 사용자가 상세 제품 페이지 또는 장바구니 페이지에서 선택한 매장과 상품 정보, 결제 금액, 그리고 적립될 포인트 데이터를 수집하고, 이를 결제 페이지로 전달하는 작업이었습니다.

# 결제페이지
![데이터 처리](https://img.shields.io/badge/데이터처리-39457E?style=for-the-badge&logoColor=white)
- 로그인한 사용자의 ID와 관련된 포인트, 그리고 선택한 매장 정보를 불러옵니다. 사용자가 '포인트 전체 사용' 버튼을 클릭하면, 해당 기능을 수행하는 함수가 호출됩니다. 이 함수는 사용자의 보유 포인트를 매개변수로 받아, 사용자의 포인트를 전체 사용 상태로 변경합니다.
![결제](https://github.com/jiyooya/TIM/assets/127083635/37a318d2-c855-4508-bd64-e84e4788b6d4)
![할인 및 포인트](https://github.com/jiyooya/TIM/assets/127083635/1f150935-dbc7-4f2f-8539-f108180db195)


### 결제 방법
- 두 가지 결제 방법을 제공합니다. 
'신용카드' 버튼을 클릭하면, 사용자가 개인카드 또는 법인카드를 선택할 수 있는 창이 새롭게 띄워집니다.
'무통장 입금' 버튼을 클릭하면 해당 기능을 수행하 함수가 호출되어 사용자에게 입금 폼을 보여줍니다. 무통장 입금을 선택한 사용자는 '영수증 발급' 버튼을 클릭하여 소득 공제를 위한 정보를 입력할 수 있는 폼에 접근할 수 있습니다. 영수증 발급을 원치 않는 경우 '발급 안함' 버튼을 클릭하면, 영수증 발급 관련 폼이 삭제됩니다.

![결제 폼](https://github.com/jiyooya/TIM/assets/127083635/f657f464-da9b-4cfe-8282-4a0fca82bfe7)

# 주문내역
![데이터 표시](https://img.shields.io/badge/데이터표시기능-39457E?style=for-the-badge&logoColor=white)
- 장바구니 페이지 또는 상세 제품 페이지에서 선택한 상품명, 사용자가 직접 선택한 재료, 수량, 금액 등의 정보를 수집하여 화면에 표시합니다. 사용자가 보유한 포인트를 사용하기로 결정하면, 콜백 함수를 통해 총 주문금액에서 사용 포인트를 제외한 최종 결제금액을 계산하고 이를 화면에 표시하도록 구현하였습니다.

![상세 페이지 데이터 표시](https://img.shields.io/badge/상세페이지데이터표시-D83B01?style=for-the-badge&logo=microsoft-office&logoColor=white)
![상세페이지](https://github.com/jiyooya/TIM/assets/127083635/a2fa4b95-1f20-45bc-8368-dabec8d35fbb)

![장바구니](https://img.shields.io/badge/장바구니페이지데이터표시-43853D?style=for-the-badge&logoColor=white)
![장바구니](https://github.com/jiyooya/TIM/assets/127083635/71cb7287-af8f-419e-8b3a-b26a0fcee8e8)

- 구매 조건에 동의하는 체크박스에 체크하지 않은 상태에서 '결제하기' 버튼을 클릭하면, 사용자에게 동의를 요청하는 안내 메시지가 출력되도록 설정하였습니다. 또한, 동의 체크박스에 체크한 후 '결제하기' 버튼을 누를 경우, 주문 취소가 불가능하다는 사실을 알리는 안내 메시지가 추가로 표시되도록 하였습니다.

![구매동의](https://github.com/jiyooya/TIM/assets/127083635/b447afa0-9c42-43fb-99ea-6a041a82c3be)


# 주문완료페이지
- 자바의 Random 함수를 활용하여 주문번호를 생성하도록 구현하였습니다. 결제 페이지와 마찬가지로 매장 정보, 사용자 ID 정보, 그리고 주문 내역을 데이터로 받아 왔습니다. 마지막으로, 결제 금액에 대한 일정 비율의 포인트가 적립되도록 기능을 추가하였습니다.

![주문 상세 내역 페이지](https://github.com/jiyooya/TIM/assets/127083635/8491a0ef-a9ca-4a0d-8825-6288ec66020b)
![주문 상세 내역 2](https://github.com/jiyooya/TIM/assets/127083635/0593b41e-d9b7-4a54-826c-54359264802a)
![결제 내역](https://github.com/jiyooya/TIM/assets/127083635/1859e8f4-1fdc-424d-83e9-172853c89ff4)


# 로그인 사용자 포인트 적립 확인하기
- 결제가 완료되면, 결제 금액의 일정 비율이 포인트가 데이터베이스에서 자신의 ID에 적립된 포인트를 확인할 수 있습니다.

![포인트 적립](https://github.com/jiyooya/TIM/assets/127083635/1b873034-c833-4867-92d2-aa87fcc4d217)





