# Project에 적합한 모델 찾기
## 목적
- image editing
- image의 identity를 변화시키면 안된다
- interpolation이 되야 한다
- custom data 이용 방법 소개

## Reference Page
[github link](https://github.com/weihaox/awesome-gan-inversion)

## candidated paper
### 1. High-Fidelity GAN Inversion for Image Attribute Editing.
- No code

### 2. Pivotal Tuning for Latent-based Editing of Real Images.
[github code link](https://github.com/danielroich/PTI)
- image editing 가능
- identity 불변
- interpolation 과정이 드러나지 않음

### 3. Transforming the Latent Space of StyleGAN for Real Face Editing.
[github code link](https://github.com/AnonSubm2021/TransStyleGAN)
- image editing 가능
- identity 불변
- interpolation 가능
- custom dataset -> 자세하게 나와있지 않음. train file은 있음

### 4. Disentangled Face Attribute Editing via Instance-Aware Latent Space Search.
[github code link](https://github.com/yxuhan/IALS)
- image editing 가능
- identity 불변
- interpolation 가능
- InterfaceGAN의 학습 데이터 셋이 필요해 보임 -> 확실하진 않음
InterfaceGAN의 결과가 좋지 않아서 문제. -> 더 많은 데이터 셋을 모아야함

### 5. Enjoy Your Editing: Controllable GANs for Image Editing via Latent Space Navigation.
- No code

### 6. Navigating the GAN Parameter Space for Semantic Image Editing
[github code link](https://github.com/yandex-research/navigan)
- image editing 가능
- identity 불변
- interpolation 가능
- 특정 attribute만 변화시키는 방법을 모르겠음...

### 7. In-Domain GAN Inversion for Real Image Editing
#### Check!!
[github code link](https://github.com/genforce/idinvert)
- image editing 가능
- identity 불변
- pytorch version 있음
- A -> B interpolation 있음
- training 가능

### 8. Editing in Style: Uncovering the Local Semantics of GANs
[github code link](https://github.com/IVRL/GANLocalEditing)
- 학습하는 방법이 안나와있음

### 9. A Latent Transformer for Disentangled and Identity-Preserving Face Editing.
#### Check!!
[github code link](https://github.com/InterDigitalInc/Latent-Transformer)
- image editing 가능
- identity 불변
- pytorch version 있음
- attribute 선택 가능
- train 가능해 보임

### 10. L2M-GAN: Learning To Manipulate Latent Space Semantics for Facial Attribute Editing
- no code

### 11. InterFaceGAN - Interpreting the Latent Space of GANs for Semantic Face Editing
- 이미 실습해 보았음.
- 적은 dataset 때문에 잘 안됨
- 추가해서 다시 해봐야함

### 12. DyStyle: Dynamic Neural Network for Multi-Attribute-Conditioned Style Editing.
- no code

### 13. Coarse-to-Fine: Facial Structure Editing of Portrait Images via Latent Space Classifications.
- no code

### 14. StyleMapGAN: Exploiting Spatial Dimensions of Latent in GAN for Real-time Image Editing
[github code link](https://github.com/naver-ai/StyleMapGAN)
- naver ai
- 학습 가능하지만, custom data 기준으로 설명되어 있지 않음

# face parser code modify
한번에 동영상에서 얼굴 추출까지 하는 코드 작성

# add dataset
데이터 셋 추가할 동영상 다운로드
