# BoostCamp AI Tech level 2 재활용 품목 분류를 위한 Object Detection-CV14조

## Member🔥
| [김지훈](https://github.com/kzh3010) | [원준식](https://github.com/JSJSWON) | [송영섭](https://github.com/gih0109) | [허건혁](https://github.com/GeonHyeock) | [홍주영](https://github.com/archemist-hong) |
| :-: | :-: | :-: | :-: | :-: |
| <img src="https://avatars.githubusercontent.com/kzh3010" width="100"> | <img src="https://avatars.githubusercontent.com/JSJSWON" width="100"> | <img src="https://avatars.githubusercontent.com/gih0109" width="100"> | <img src="https://avatars.githubusercontent.com/GeonHyeock" width="100"> | <img src="https://avatars.githubusercontent.com/archemist-hong" width="100"> |

## Index
* [Project](#project)
* [Team role](#team-role)
* [Procedures](#procedures)
* [Command](#command)
* [Wrap UP Report](#wrap-up-report)  



## Project

### 개요
- 배경: 쓰레기 대란, 매립지 부족과 같은 쓰레기로 인한 사회적 문제 해결 필요
- 주제: 재활용 품목 분류를 위한 Object Detection 모델 개발

<img width="150%" src="./image/sample.png"/>

- 기대 효과
    - 쓰레기장 설치 및 활용으로 분리수거의 정확도 향상
    - 아이들의 분리수거 교육에 활용
- Input: 쓰레기 객체가 담긴 이미지
- Output: detection 결과
    - bbox좌표: (x_min, y_min, x_max, y_max)
    - 카테고리: Backgroud, General trash, Paper, Paper pack, Metal, Glass, Plastic, Styrofoam, Plastic bag, Battery, Clothing
    - confidence score
    
```
 dataset
    ├── train.json      
    ├── test.json
    ├── train            #(4,883장)
    └── test             #(4,871장)
```

## Team role
- 김지훈: EDA, 2stage model 실험
- 원준식: backbone model 실험, data augmentation, 앙상블 적용
- 송영섭: 대회 실험 관리 및 진행, 1 stage model 실험
- 허건혁: data EDA를 위한 시각화 tool 개발, pseudo labeling 실험
- 홍주영: SOTA 모델(Diffusion Det) 적용, 2 stage model 실험


## Procedures
대회 기간: 2022.11.16 ~ 2022.12.01

| 날짜 | 내용 |
| :---: | :---: |
| 11.14 ~ 11.20 | Object detection 강의 수강 및 이론 학습|
| 11.21 ~ 11.27 | data EDA 및 model 실험 |
| 11.28 ~ 12.01 | model tuning 및 ensemble |

## Command
- train
```
python mmdetection/tools/train.py {config file}
```

- submission

```
python submission.py -c {config file} -r {checkpoint}
```

- streamlit
```
streamlit run app.py
```

## Wrap UP Report
- [Report](https://www.notion.so/Object-Detection-Wrap-Up-Report-CV-14-8950e897953c4660b749c8fc5b898b74)
