<h1>LOL_Machinlearning_Predict-win-rate-model</h1>

<h2>🌟 프로젝트 개요</h2>

<h3>이 프로젝트는 리그 오브 레전드(League of Legends)의 초반 10분 게임 데이터를 활용하여 해당 경기의 최종 승패를 예측하는 머신러닝 분류 모델을 구축하는 것을 목표로 했습니다. 데이터 수집부터 전처리, 모델 비교, 하이퍼 파라미터 튜닝까지 데이터 분석 전반의 과정을 수행했습니다.

🔬 데이터 분석 및 모델링 방법론</h3>

<h4>1. 데이터 수집 및 전처리

데이터 수집: Riot Games API를 사용하여 Challenger부터 IRON 랭크까지의 광범위한 티어에서 약 10만 개 이상의 게임 데이터를 수집했습니다. 각 경기의 GameTimelineInfo를 통해 1분 단위의 세밀한 데이터를 확보했습니다. -   특징 공학 (Feature Engineering): 팀 간의 격차(Difference)를 나타내는 변수들을 생성하여 예측 모델의 성능을 극대화했습니다.

주요 변수: Diff_Kills, Diff_Level, Diff_CS (미니언 처치 수), Diff_DRAGON (드래곤 획득 수) 등 핵심 지표를 활용.

데이터 클리닝:

이상치(Outlier)를 제거하여 데이터의 분포를 정규화하고 모델 학습의 안정성을 확보했습니다.

골드나 경험치와 같이 승패와 직접적인 상관관계가 높은 변수들은 제외하여 모델의 예측 능력을 순수하게 평가할 수 있도록 통제했습니다.

2. 모델 선정 및 학습 전략

모델 비교: 예측 성능을 비교하기 위해 4가지 분류 모델을 선정하고 테스트했습니다.

RandomForestClassifier

LightGBM (LGBMClassifier)

CatBoostClassifier

ExtraTreesClassifier -   하이퍼 파라미터 튜닝: Grid Search를 사용하여 각 모델의 최적 하이퍼 파라미터 조합을 탐색하고, 과적합(Overfitting)을 방지하기 위해 최종 파라미터를 조정했습니다. -   과적합(Overfitting) 해결: 초기 학습에서 Train Accuracy가 100%에 근접하는 과적합 현상을 발견하고, 파라미터 재조정을 통해 일반화 성능을 확보했습니다.

3. 모델 평가 및 결론 도출

평가 지표: 모델의 분류 성능을 객관적으로 측정하기 위해 다음 지표들을 활용했습니다.

Accuracy (정확도)

F1 Score: 정밀도(Precision)와 재현율(Recall)의 조화 평균을 통해 불균형 데이터에 강건한 성능을 측정.     -   ROC Curve / AUC: 분류 모델의 전반적인 성능을 평가.</h4>

<h4>결론:

티어별로 모델의 예측 정확도에 차이가 있음을 확인했습니다 (마스터, 그랜드마스터 티어에서 예측 정확도가 가장 높게 나옴).

고티어에서는 초반 스노우볼링보다는 후반 캐리형 챔피언의 잠재력이 폭발하는 경향이 있음을 분석했습니다.</h4>

초반 오브젝트(드래곤, 전령) 획득의 스노우볼 효과가 승패 결과에 미치는 영향이 매우 크다는 시사점을 도출했습니다.
# 머신러닝 기반 League of Legends 승리 요인 예측
<img width="1201" alt="image" src="https://github.com/user-attachments/assets/22c95850-b5a8-4e48-ab38-a223f74e649b" />
<img width="1205" alt="image" src="https://github.com/user-attachments/assets/ea14671b-9b03-4480-a024-400f780a8180" />
<img width="1202" alt="image" src="https://github.com/user-attachments/assets/9d6f22b4-870f-404d-83ff-01ff99da814e" />
<img width="1200" alt="image" src="https://github.com/user-attachments/assets/a07aa6dd-7ea6-4b58-8c8e-04dba118e9e6" />
<img width="1201" alt="image" src="https://github.com/user-attachments/assets/bc5c9397-e17e-491c-afe2-fb2ba0510880" />
<img width="1199" alt="image" src="https://github.com/user-attachments/assets/d499d64c-bb92-4788-aedf-0d7a50b7a558" />
<img width="1195" alt="image" src="https://github.com/user-attachments/assets/c18c3ca2-cc73-42a3-8f7c-aec8adce8e59" />
<img width="1198" alt="image" src="https://github.com/user-attachments/assets/03bd978e-d1b8-46fc-b090-cb6c3e25948b" />
<img width="1196" alt="image" src="https://github.com/user-attachments/assets/be07e7fc-8d9d-4f8b-8050-6e3dca1d9d37" />
<img width="1200" alt="image" src="https://github.com/user-attachments/assets/6889144f-0b64-402e-b348-65b814a4b780" />
<img width="1199" alt="image" src="https://github.com/user-attachments/assets/2476fcb3-9ffe-4cae-80f5-3b9bc255034f" />
<img width="1200" alt="image" src="https://github.com/user-attachments/assets/319bc7b4-a5aa-479e-b5da-4ae8b1f38713" />
<img width="1203" alt="image" src="https://github.com/user-attachments/assets/47b8d5ef-626c-421a-88c1-782cd92fbd31" />
<h2 style="font-size: 28px; font-weight: bold;">📝 더 나아가 논문화 작업 진행</h2>
<img width="100%" alt="논문작업1" src="https://github.com/user-attachments/assets/a1b500c0-075e-48ee-adba-08a8c617a3de" />



