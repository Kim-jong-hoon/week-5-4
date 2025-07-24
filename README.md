# 🎥 Roboflow를 활용한 영상(Video) 데이터 라벨링 가이드

이 문서는 영상 데이터를 프레임 단위로 변환하고 Roboflow를 통해 라벨링하는 과정을 설명합니다. 영상 기반 객체 검출(Object Detection) 프로젝트에 적합합니다.

---

## 📌 전체 프로세스 요약

1. **영상 → 이미지로 분할 (프레임 추출)**
2. **Roboflow에 이미지 업로드**
3. **수동 또는 자동 라벨링**
4. **라벨링된 데이터셋 Export (YOLO, COCO 등)**

---

## 1️⃣ 영상 → 이미지 프레임으로 변환

Roboflow는 영상(mp4 등) 직접 업로드를 지원하지 않으며, **프레임 이미지**를 업로드해야 합니다.

## 2️⃣ Roboflow 프로젝트 생성 및 이미지 업로드
1. https://roboflow.com/ 에 로그인

2. Create New Project 클릭

3. 프로젝트 이름 및 타입 선택 (예: Object Detection)

4. Upload Images 버튼 클릭 → 추출한 프레임 이미지 업로드

## 3️⃣ 라벨링 수행
🖱️ 수동 라벨링
업로드된 이미지에서 "Annotate" 클릭

드래그하여 객체 지정 → 클래스(Label) 입력

객체 여러 개 지정 가능

⚡ 자동 라벨링 (옵션)
<br>Auto Annotate 또는 Smart Labeling 기능 사용 (유료 or 기존 모델 필요)

## 4️⃣ 데이터셋 생성 및 Export
Generate Dataset 클릭

사용할 포맷 선택 (YOLO, COCO, Pascal VOC 등)

ZIP으로 다운로드 후 학습에 활용


