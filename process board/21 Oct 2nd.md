# StyleFlow dataset 준비
## Styleflow 제공 데이터 셋

- attributes
shape : [batch,8,1]  
data type : float 64  
8개 fcae id 사용, 따로 normalize하지 않고 값을 바로 저장  
microsoft face API를 이용하면 value가 바로 나와서 저장만 하면 될듯  


- latents
shape : [batch,1,18,512]  
data type : float 32  
styleGAN2 image generator 이용 : 10K sample  
latent vector와 이미지를 바로 저장하면 될 듯  
일단 z,w latent vector 둘다 저장할 생각  
궁금 : image generate한 다음에 image상태 보고 사람다운 사진 10K개를 써야겠지??  

- lightings
shape : [batch,9,1]  
data type : float 32  
DPR모델 : 사진 하나를 넣으면 9개 방향에서 비춰진 light 사진(9장)을 얻음  
styleflow을 train 시키기 위해서는 사진의 9개 방향 빛 성분 정도를 숫자로 뽑아줘야함  
DPR모델을 통해 나온 사진을 넣어주고 9개의 index list로 결과를 내놓는 네트워크를 학습시켜야 할 듯  
> ex) {좌측에서 얼굴을 빛으로 비춘 사진} -> 'Network' -> [1,0,0,0,0,0,0,0,0]  

## 중간 점검(학습 파일이 돌아가는지 check)
### Sample image generate
StyleGAN2 ada 네트워크를 기반으로 해서 10K(논문에 나와있는 대로 함)  

### Attributes
논문에 나와 있는 속성들을 동일하게 따라함  
numpy file save  

### latents
StyleGAN2에서 샘플 이미지들을 만들때 동시에 numpy file로 저장

### lightings
돌아가는지 확인만 하기 위해서 각 value들을 0.11로 고정

### results
학습 됨

## 이후 계획
### lightings
- 이미지가 들어오면 이미지 lighting의 값을 내놓는 네트워크를 학습시켜야 함
- VGG net을 사용할 것 같음(WHY?)

### main.py
- tfutil 에서 tensorflow를 사용해서 오류 계속 발생
- 이 부분 대체하여 돌아가도록 코드 수정

### etc
나머지 데이터 셋은 다 준비 완료
