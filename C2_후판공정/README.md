# **후판공정 Scale 불량 원인 분석 보고서**

## **팀명**
- **포스코 청년AI•Big Data 아카데미 25기 C반 2조**

---

## **목표**
스케일(scale) 불량 원인을 분석하여 후판 제조 과정의 품질을 향상시키고, 불량률을 최소화.  
공정 조건과 설비 최적화를 통해 생산 효율성을 극대화하고 현장 개선안을 도출.

---

## **주요 기능**
- **데이터 분석 및 상관관계 파악**  
  - 다양한 변수(압연 온도, 추출 온도, 후판의 두께 등)를 바탕으로 불량 발생 원인을 분석.  
  - 데이터 전처리, 통계 분석, 히트맵 등 시각화를 통해 주요 변수의 영향을 정량적으로 확인.  
- **모델링 및 성능 비교**  
  - Decision Tree, Random Forest, XGBoost 등의 알고리즘을 활용하여 핵심 변수 도출.  
  - Hyperparameter Tuning을 통해 각 모델의 성능 최적화.  
- **공정 최적화 제안**  
  - 압연 온도와 공정 시간의 최적 범위를 설정하여 불량률을 저감.  
  - Descaling 공정 횟수를 분석하여 효율적 관리 방안을 도출.

---

## **프로젝트 과정 요약 및 성능 개선 노력**
1. **데이터 전처리 및 이상치 제거**  
   - Box Plot과 Histogram을 통해 이상치를 분석하고 제거.  
   - 필요 없는 변수를 제거하여 데이터 정리 (예: Plate_no, Spec_long 등).  

2. **탐색적 데이터 분석**  
   - 히트맵을 통해 압연 온도와 추출 온도가 불량률에 가장 큰 영향을 미친다는 것을 확인.  
   - 작업조, 가열로 등 일부 변수와 불량률의 상관성이 낮다는 결과 도출.  

3. **모델링 및 비교**  
   - **Decision Tree:** 간단한 분류로 불량 원인을 분석 (Accuracy: 96%).  
   - **Random Forest:** 다중 변수 해석 및 성능 향상 (Accuracy: 95.4%).  
   - **XGBoost:** 최적의 성능 달성 (Accuracy: 95.8%).  

4. **최종 모델 선정**  
   - XGBoost 모델이 최적의 성능과 해석력을 보여 최종적으로 선택.

---

### **최종 개선안**
1. 압연 온도 한계를 초과하지 않고 HSB 공정을 반드시 적용하며 공정 온도와 시간을 최적화하여 관리.  
2. 온도를 특정 시점에서 측정하는 대신 상시 모니터링 시스템으로 개선하여 스케일 불량 핵심 파라미터를 관리.  
3. Descaling 공정 횟수와 압연 조건을 실험적으로 분석해 최적의 설정값 도출.  

---



