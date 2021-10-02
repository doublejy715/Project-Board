# StyleFlow dataset 준비
## Face_attribute_extracter.py
### Styleflow 제공 데이터 셋

- attributes
shape : [batch,8,1]
data type : float 64
8개 fcae id 사용, 따로 normalize하지 않고 값을 바로 저장

- latents
shape : [batch,1,18,512]
data type : float 32
바로 저장하면 될 듯

- lightings
shape : [batch,9,1]
data type : float 32
9개 light 사진을 얻음. 학습 이후 softmax를 결과로 쓴 듯.
그런데 음수 값도 있음 -> 왜???
