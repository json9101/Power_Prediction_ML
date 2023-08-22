# Power_Prediction_ML
## 주제
그룹 프로젝트로써 전기 사용량을 예측한 모델을 사용하여 사용자가 조건을 입력한 조건을 대입해 조건에 해당하는 전기예측량 제공하는 웹 페이지 개발

## 결과물
https://github.com/power-prediction/power-ml/issues/2 

## ML 결과

- 건물의 사용용도는 전력에 큰 영향을 주지않음
- 건물의 면적보다는 냉방면적이 전력량에 더 큰 영향을 줌
- 기온과 습도가 높고 강수량이 없을 때 전력 사용량이 큼

# ML 부분에 관심이 있으시면 밑에 부분을 봐주세요!!

## ML부분

전력 데이터
- num_date_time
- 건물번호
- 일시
- 기온(C)
- 강수량(mm) 
- 풍속(m/s)
- 습도(%)
- 일조(hr)
- 일사(MJ/m2)
- 전력소비량(kWh)

빌딩 데이터
   - 건물번호 
   - 건물유형 
   - 연면적(m2)
   - 냉방면적(m2)
   - 태양광용량(kW)
   - ESS저장용량(kWh)
   - PCS용량(kW)

전력 데이터의 일시 컬럼을 연도, 월, 일, 시 컬럼을 추가

<img width="716" alt="image" src="https://github.com/json9101/Power_Prediction_ML/assets/57518426/5e67adba-218e-43ca-a706-fec444fdb300">

빌딩 데이터와 전력 데이터 건물번호 기준으로 merge

<img width="869" alt="image" src="https://github.com/json9101/Power_Prediction_ML/assets/57518426/96c4b0b5-e88e-4867-ada8-c983633847ae">

결측치 처리와 건물 OneHotEncoding 후
- 기온(C)
- 강수량(mm)
- 습도(%)
- 연도
- 월
- 일
- 시
- 연면적(m2)
- 건물유형_건물기타
- 건물유형_공공
- 건물유형_대학교
- 건물유형_데이터센터
- 건물유형_백화점및아울렛
- 건물유형_병원
- 건물유형_상용
- 건물유형_아파트
- 건물유형_연구소
- 건물유형_지식산업센터
- 건물유형_할인마트
- 건물유형_호텔및리조트
컬럼만 사용하여 Random Forest 실행

mape 결과 0.070





