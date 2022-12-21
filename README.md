# bee_detection_project

실제 수집한 데이터 샘플로 YOLO5 구현

yolov5s 모델 사용해서 학습 진행

사용한 데이터

- 이미지 데이터

- 이미지 데이터의 메타정보가 포함된 라벨링 데이터

- 이미지와 라벨링 데이터는 한쌍으로 이루어져 있음

# Index

1.Import Library

2.Data Preprocessing

3.Model Training

4.Model Test

5.Result

# Import Library

![image](https://user-images.githubusercontent.com/104436260/208832899-402b4986-e5e7-44ee-99d8-592dc2cc28ea.png)

패키지 load

# Data Preprocessing

![image](https://user-images.githubusercontent.com/104436260/208833062-4f258a3b-97c6-45f2-a0ae-9985c02b547f.png)

각 Class별 객체가 최소 몇개 있는지 확인해주는 함수 

D_Load 함수는 소스 코드에서 확인.

![image](https://user-images.githubusercontent.com/104436260/208833841-84ea1657-02b5-45d2-b096-6304a5f9bd50.png)

Data Split 비율은 Train:Valid:Test=8:1:1

이후에, 원천데이터를 Train, Valid, Test 폴더를 각각 만들어 이미지와 라벨링 데이터를 shutil.copy함수를 통해 복사 붙여넣기 해줌

![image](https://user-images.githubusercontent.com/104436260/208834542-13cfd717-1e13-46ca-b943-e043f7eb5f76.png)

