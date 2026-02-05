# GAN과 CNN을 활용한 관광지 추천 서비스 설계 및 구현

### 💡 서비스 개요 
- 인공지능 stable-diffusion 및 cnn 모델을 활용하여 사용자에게 입력받은 추상적인 관광지 정보를 바탕으로 관광지 추천.

### 팀 구성 
- BE 4명, FE- 2명

### 🛠️ 기술 스택
</div>
    <div style="text-align: left;">
    <div> <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=Python&logoColor=white">
          <img src="https://img.shields.io/badge/Selenium-43B02A?style=flat-square&logo=Selenium&logoColor=white">
          <img src="https://img.shields.io/badge/Tensorflow-FF6F00?style=flat-square&logo=Tensorflow&logoColor=white">
          <br>
          <img src="https://img.shields.io/badge/Javascript-F7DF1E?style=flat-square&logo=Javascript&logoColor=white">
          <img src="https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=CSS3&logoColor=white">
          <img src="https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=HTML5&logoColor=white">
          <img src="https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=MySQL&logoColor=white">
          <img src="https://img.shields.io/badge/Github-181717?style=flat-square&logo=Github&logoColor=white">
          </div>
   </div>

## 📝 주요 기능
<details>
<summary>시스템 흐름도</summary>
    
![image](https://github.com/user-attachments/assets/4388a7f2-5c6f-426d-9318-ad58d9e1124a)
![image](https://github.com/user-attachments/assets/f104b3c3-a10d-4622-9fd4-b2c07a77fc96)
</details>

<details>
<summary>데이터 전처리</summary>

![image](https://github.com/user-attachments/assets/f97451a2-222d-4f23-9e3a-29e04bcda4c2)
</details>

<details>
<summary>GAN 모델</summary>

![image](https://github.com/user-attachments/assets/ab12fa48-4c74-4c75-a03c-49e939ed8b13)
![image](https://github.com/user-attachments/assets/acb1c20f-b7f2-4250-a78d-798d7398a9d5)
</details>

<details>
<summary>CNN 모델</summary>
    
![image](https://github.com/user-attachments/assets/aed65320-92c0-40da-bf07-436cb2085605)
![image](https://github.com/user-attachments/assets/d09f8508-ceea-4568-9699-3f3322efc8f5)
![image](https://github.com/user-attachments/assets/808a1fea-0f39-4ceb-a12e-50a45efd7597)
![image](https://github.com/user-attachments/assets/a43a5ce4-b8c1-4307-9834-4147c38017c0)
![image](https://github.com/user-attachments/assets/e41704df-7f29-4221-9d39-2b774da1802d)
</details>

<details>
<summary>이미지 생성 결과</summary>
    
![image](https://github.com/user-attachments/assets/38144301-fa4e-4c0a-a12e-df48403e17b9)
</details>



### 👤 상세역할
- #### 개발(이미지 및 정보 크롤링, CNN 모델 훈련과 전처리)
- Selenium과 BeautifulSoup를 활용해 관광지 정보를 크롤링.
- 문헌 정보는 HTML 구조를 분석 후 XPath를 통해 정확히 추출.
- Chrome Driver를 사용하여 6,421개의 이미지 스크래핑 및 저장.
- 수집된 이미지를  전처리 작업 후 CNN 모델 학습.

### 🎯 성과 및 기여
- 정확도 향상: 초기 CNN 모델의 정확도 72%에서 하이퍼파라미터 튜닝 및 데이터 전처리를 통해 89%까지 개선.
- 협업 성과: 팀원들과 역할을 분담하여 데이터 수집, 모델 학습, 결과 통합 등 프로젝트의 모든 단계를 성공적으로 완수.
- 정보처리기술학회 금상 수상

### 🏆 논문: https://www.dbpia.co.kr/journal/articleDetail?nodeId=NODE11652126
   
```
yANUs1-travel-project_main
├─ AI_train
│  ├─ .BigTransferModel.h5.icloud
│  ├─ .BigTransferModel_v2.h5.icloud
│  ├─ .train_model_v1.h5.icloud
│  ├─ big_tranformer_model.py
│  ├─ cnn.py
│  ├─ cnn_main.py
│  ├─ gan_train1.py
│  ├─ gan_train2.py
│  ├─ preprocessing.py
│  ├─ test_model_v1.py
│  └─ train_model_v1.py
├─ adobe.py
├─ ai_fuction.py
├─ ai_model
│  ├─ .finetuned_stable_diffusion_gan_team.h5.icloud
│  └─ BigTransferModel_1.h5
├─ app.py
├─ instance
│  └─ database.db
├─ media
├─ migrations
│  ├─ README
│  ├─ alembic.ini
│  ├─ env.py
│  ├─ script.py.mako
│  └─ versions
│     ├─ __pycache__
│     │  └─ f9cce136adc0_.cpython-311.pyc
│     └─ f9cce136adc0_.py
├─ requirements.txt
├─ test_ai.py
├─ transfer_AI_MODEL
│  ├─ .DS_Store
│  └─ BigTransferModel1
│     ├─ assets
│     ├─ fingerprint.pb
│     ├─ keras_metadata.pb
│     ├─ saved_model.pb
│     └─ variables
│        ├─ variables.data-00000-of-00001
│        └─ variables.index
├─ translate.py
└─ web
   ├─ __init__.py
   ├─ auth.py
   ├─ models.py
   ├─ static
   │  ├─ css
   │  │  ├─ gaib.css
   │  │  ├─ history_detail.css
   │  │  ├─ login.css
   │  │  ├─ main.css
   │  │  ├─ mypage.css
   │  │  └─ result.css
   │  ├─ js
   │  │  ├─ .DS_Store
   │  │  ├─ gaib.js
   │  │  ├─ login.js
   │  │  ├─ main.js
   │  │  ├─ mypage.js
   │  │  └─ result.js
   │  ├─ logo.png
   │  ├─ media
   │  │  ├─ Cliffs_and_a_very_small_lake_in_a_very_dry_desert.jpeg
   │  │  ├─ Cliffs_and_tiny_lakes_in_a_very_dry_desert.jpeg
   │  │  ├─ Osaka_Castle_in_sunny_weather.jpeg
   │  │  ├─ aurora_in_the_night_sky.jpeg
   │  │  └─ houses_on_the_beach.jpeg
   │  └─ search.png
   ├─ templates
   │  ├─ gaib.html
   │  ├─ history_detail.html
   │  ├─ login.html
   │  ├─ main.html
   │  ├─ mypage.html
   │  └─ result.html
   └─ views.py

