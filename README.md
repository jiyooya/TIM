# 제작동기
글자, 색, 모양, 재형 등을 고르면 약의 정보를 손쉽게 찾아 볼 수 있는 약학정보원 홈페이지에서 분류에 따라 고르는
시스템을 차용할 수 있는 쇼핑몰 형태의 홈페이지를 구상했습니다.
![image](https://github.com/jiyooya/TIM/assets/127083635/a4c6707b-e926-4f9a-917d-8941ad519353)

# 목표
메뉴 커스텀 방식을 사용하고 있는 샌드위치 프렌차이즈 홈페이지와 샐러드 정기배송을 지원하고 있는 홈페이지를 참고하여 나만의 레시피로 다양한 메뉴를 즐길 수 있는 샐러드 주문 홈페이지를 만들었습니다.
![image](https://github.com/jiyooya/TIM/assets/127083635/bd6a8bd2-c3f0-4e77-9a46-da84b0a16950)

# 개발환경
![image](https://github.com/jiyooya/TIM/assets/127083635/b5b98047-d3ce-41d6-885e-e8d97553dee1)

# ER 다이어그램
![image](https://github.com/jiyooya/TIM/assets/127083635/a7926940-a2c0-440e-b096-d9f452f72f5a)

# 내 역할
로그인한 ID에서 상세제품 페이지 또는 장바구니 페이지에서 선택한 매장과 상품의 정보의 데이터를 받아 와 결제페이지 화면으로 넘기는 역할을 했습니다.

# 결제페이지
### 데이터 받아오기
▶로그인한 사용자의 ID의 정보 보유하고 있는 포인트 그리고 선택한 매장 정보의 데이터를 불러오고
포인트 전체사용 버튼을 클릭하면 해당 포인트 함수가 호출되고 로그인한 ID의 포인트를 매개변수로 전달해 보유하고 있는 포인트가 전체사용이 되게 만들었습니다.


![image](https://github.com/jiyooya/TIM/assets/127083635/6f358b01-156c-44e4-a139-acbdb5871597)

### 결제 방법
▶결제 수단도 무통장입금과 카카오QR로 결제하는 두 가지 방법을 만들습니다.
무통장 버튼을 클릭하면 해당 함수가 호출되어 입금 폼이 나오게 만들었고, 무통장입금 방식을 사용할 때는 영수증 버튼을 누르면 소득공제번호를 기재할 수 있는 폼을 만들었습니다. 
만약 발급을 원치 않으면 발급안함 버튼을 누르면 삭제되는 기능을 추가했습니다. 동일하게 결제수단을 카카오 결제로 변경할 경우 해당 버튼을 클릭하면 무통장입금 폼이 삭제되는 기능을 추가했습니다.


![image](https://github.com/jiyooya/TIM/assets/127083635/63fecc1f-72cb-41e6-a580-78464292fa4e)

### 데이터 받아오기
▶장바구니 페이지 또는 상세제품 페이지에서 선택한 상품명, 직접 선택한 재료, 수량, 금액 등을 데이터를 받아와 화면에 표시하였습니다.
보유하고 있는 포인트를 사용했다면 콜백 함수를 사용하여 총 주문금액에서 사용할 포인트를 제외한 결제금액이 계산되어 화면에 표시될 수 있게 만들었습니다.


![image](https://github.com/jiyooya/TIM/assets/127083635/95939e21-7061-4800-828d-f6c4337a830d)

### 결제 QR
▶결제하기 버튼을 클릭하면 카카오 QR코드가 나오고 결제 성공했다는 안내창이 나오면서 다음 페이지로 넘어갑니다.


![image](https://github.com/jiyooya/TIM/assets/127083635/08c37308-03d8-4be0-a2ba-01cf6a817540)

# 주문완료페이지
▶자바 Random 함수를 이용해 주문번호가 화면에 나오게 만들었습니다.
결제페이지와 동일하게 매장정보와 해당 ID의 정보, 주문내역들을 데이터로 받아왔고
마지막으로 결제 금액의 대해 일부 포인트가 적립되게 만들었습니다.


![image](https://github.com/jiyooya/TIM/assets/127083635/56bca965-9b82-4e22-aa20-9c8c73aec34c)


