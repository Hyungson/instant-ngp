## instant ngp
multiview-image to 3d obj

finetuning을 하지 않은 one-2-3-45 inference 보단 3d reconstruction 성능이 좋은 듯 하다.

**** 
### 아이폰 11 카메라로 own shoes 이미지 약 70여개 촬영
### colab inference code로 obj 및 output video 생성

****

#### obj 스크린샷
![image](https://github.com/Hyungson/instant-ngp/assets/103267793/f5aed30e-fba3-4644-bc8e-b760cf7930d7)

#### video

![output_video-ezgif com-video-to-gif-converter](https://github.com/Hyungson/instant-ngp/assets/103267793/31649c3d-7fe2-48e4-b03f-d583f3879c37)

****

#### one-2-3-45 인퍼런스 예시
우리 집 고양이 레미 사진을 누끼따서 한장으로 inference 한 결과
![ezgif com-video-to-gif-converter](https://github.com/Hyungson/instant-ngp/assets/103267793/fc728bf6-f984-4f23-9a0f-9faf5b890583)
뒷 부분의 view synthesis가 부족해 보인다.
프로젝트 진행 당시에는 코드가 오픈되어 있지 않아서 파인 튜닝을 시도조차 해보지 못했던게 아쉽다.

****
우리 프로젝트에 instant-ngp를 사용하지 못해 아쉽다.

multi-view image input이 필요하고, colmap을 사용해 카메라 시점 좌표 값으로 추정되는 transform.json 파일이 필요하다.

또한 3d reconstruction 시간이 오래걸리므로 gui 배포에 어려움이 있을 것 같아 제외하게 되었다.

또한 동일한 물체에 대한 여러 각도의 사진이 필요하고, 데이터 증강에 어려움이 있다.

3d task에 맞는 데이터 증강방법을 공부해보자.
