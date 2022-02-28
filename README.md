<img alt="smoking" src="https://user-images.githubusercontent.com/63290629/155827268-bc84bf89-6473-405c-bf2d-d12c962a468f.png">

<br>

# Smoking-Detective System

> ‘컴퓨터비전’ 수업 #3 과제 → **Smoking-Detective System (Deep Learning)**


<Br>


### ✅ 프로젝트 소개  
<br>

- 금연 구역 내 흡연자 탐지
- 흡연 장면 자동 모자이크
- 흡연 데이터 기록

<Br>

### 📝 요구 사항 분석

<br>

- 담배와 흡연하는 사람 이미지 데이터 수집
- 이미지에서 담배 라벨링
- 구글 Colab을 이용한 데이터 이미지 training
- 흡연자 탐지
- 흡연 데이터 기록
- 인식된 프레임 블러 처리

<br>

### 💻 구현   

<br>

1. **데이터 수집**
    
    [kaggle.com](http://kaggle.com) → cigarette dataset, 일반 사람 이미지 다운로드
    
    [https://www.kaggle.com/lurenzhouyi/cigarette-dataset](https://www.kaggle.com/lurenzhouyi/cigarette-dataset)
    
    [https://www.kaggle.com/vitaminc/cigarette-smoker-detection](https://www.kaggle.com/vitaminc/cigarette-smoker-detection)
    
    → *구글 서버 다운*으로 인해 이번 프로젝트에서는 사용하지 못하고 다른 데이터셋을 활용함
    
    > + object detector를 학습시킬 때는 negative data가 굉장히 중요하다. 담배를 쥔 손을 검출한다고 할 때, 담배를 쥐지않는 손의 정보가 없다면 구분하지 못할 가능성이 높다. → 데이터에 비슷하지만 다른 부류가 있다면 반드시 다른 부류로 지정해서 학습시켜야 구분을 할 수 있다.

<br>

1. **라벨링**
    
    담배를 들고 있는 손, 담배를 물고 있는 입

    <img alt="smoking01" src="https://user-images.githubusercontent.com/63290629/155827272-7586c174-2db5-4f2c-8f93-20e2b72bf43b.png">

<br>

2. **구글 Colab 으로 Data Training**
    
    1) num_steps = 500, 1000으로 학습 → 제대로 인식을 못함
    
    2) num_steps = 2000으로 학습


<br>

3.  **test 실행**

<br>

4. **담배가 나오는 영상에 학습으로 나온 tar.gz 파일 적용**
   
   <img width="450" alt="smoking03" src="https://user-images.githubusercontent.com/63290629/155827274-86fe49d4-3001-4ffc-968f-edcca311229a.png">

<br>

5. **라벨링한 데이터의 탐지된 프레임을 기반으로 `흡연 장면 자동 모자이크`**


    <img width="710" alt="smoking04" src="https://user-images.githubusercontent.com/63290629/155827275-f3299e87-548d-445f-ba5f-f4db96cae9cc.png">

<br>

6. **흡연자 감지 출력**

<br>

7. **흡연 로그 데이터 기록**

---

<br>


### 🙋‍♀️ 역할

- 데이터셋 수집
- Google Colab으로 traning 진행
- 담배 영상에 tar.gz 파일 적용
- 블러 처리


<Br>


### 💦 아쉬운 점

- negative data가 필요한지 몰라서 초반에 담배와 관련된 이미지만 training을 시켰었다. → 중간에 깨닫고 담배없는 이미지 추가해서 다시 진행
- 짧은 개발 기간으로 부족한 데이터셋
- 데이터셋이 더 많고 다양해야 한다.
    - 회전시킨 이미지
    - 다양한 담배 (색상, 크기 등)
- 로그 기록과 흡연자 감지 출력의 부정확성


### [↪️ 데모 영상](https://github.com/donnyrla10/Smoking-Detective-System/tree/master/Project/Demo)

<br>


