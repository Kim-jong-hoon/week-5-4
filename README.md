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

### ✅ `ffmpeg` 사용 예시
```bash
ffmpeg -i your_video.mp4 -vf fps=5 frame_%04d.jpg


