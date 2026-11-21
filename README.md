# Hi, I'm Jiseon Lee 👋

**데이터를 이해하고, AI로 쓸모 있는 기능을 만듭니다.**

의료·바이오 데이터 분석부터 LLM 기반 서비스까지 다양한 문제를 탐구하고 있습니다.
데이터 전처리와 모델링, 결과 검증을 거쳐 사용자가 활용할 수 있는 기능으로 연결하는 데 관심이 있습니다.

## 🙋🏻‍♀️ About Me

- **AI · NLP** — 핵심어 생성, 문서 검색, 근거를 제시하는 평가 시스템을 개발했습니다.
- **Data · Bioinformatics** — 임상 데이터 예측 모델링과 단일세포 RNA-seq 분석을 경험했습니다.
- **Validation** — 모델과 파라미터를 비교하고, 결과의 안정성과 해석 가능성을 확인합니다.
- **Collaboration** — 모듈 간 입력·출력과 데이터 형식을 맞추고, 팀의 구현을 하나의 흐름으로 연결합니다.

## 📄 Projects

### [도깨비: 팔도의 비밀](https://github.com/2026-genai-ar-tourism-data-rpg) — 생성형 AI 기반 AR 관광 RPG *(관광 데이터 처리 · 대사 생성 · 앱/서버 연동)*

실제 관광지를 탐험하며 NPC와 대화하고 미션을 수행하는 위치 기반 관광 RPG입니다. 관광 공공 데이터를 장소 선정과 게임 콘텐츠에 활용하고, **AI가 생성한 이야기를 실제 장소에서의 탐험 경험으로 연결**합니다.

- **핵심:** 관광 데이터 기반 장소 선정 · 생성형 AI NPC 대화·시나리오 · 위치 기반 미션 · AR 탐험
- **담당:** 지역 단위 관광 데이터 수집·정규화·장소 매칭 · 관광 집중률과 카테고리 상대 순위를 활용한 선정 로직 개선
- **구현:** 프롤로그 대사 생성·JSON 검증·비정상 응답 폴백 · 사용자 선택 조건의 앱 → 서버 → AI 전달 · 대사·미션·엔딩 화면 연결 · 코스 진행 상태 저장·복구
- 🛠 Python · 공공 API · LLM API · JSON · Flutter · Dart · NestJS

### [AI 강의 분석 리포트 생성기](https://github.com/2026-Lecture-Analyzer) — 강의력 자동 분석·코칭 서비스 *(AI 평가 엔진 · 근거 검증 · 전처리 개선)*

STT 강의 스크립트·녹음/영상을 **5개 영역·18개 항목**으로 분석하고, 점수와 **근거 발언·타임스탬프**, 우선 개선점을 리포트로 제공합니다. **왜 그 점수인지, 무엇을 개선할지**를 함께 전달하는 것이 핵심입니다.

- **핵심:** 규칙 기반 지표와 **LLM-as-Judge**를 결합한 하이브리드 평가 · 항목별 근거 태깅 · 강사 코칭 · 수강생 설문과 AI 평가 비교 · 대시보드·PDF 리포트
- **담당:** 평가 기준 구체화 · 분석 프롬프트와 평가 엔진 구현 · **근거 검증·교차 검증·점수 추적** 로직 개발
- **개선:** 18개 항목의 새 평가 기준과 하이브리드 실행 경로 반영 · 발화 병합·문맥 경계 처리 오류 수정
- 🛠 Python · Upstage Solar · Prompt Engineering · LLM Evaluation · Text Processing
- 🔗 [Demo](https://www.youtube.com/watch?v=rOUDMiKr6xk) · [개인 기여 상세](https://github.com/js-lee05/2026-AI-lecture-report/blob/main/docs/CONTRIBUTION.md)

### [Keyphrase Extraction · DiverseKey](https://github.com/Token5ive) — 학술 논문 핵심어 생성 파이프라인 *(SciBART 학습·후보 생성 · 평가 · 데이터 연결)*

학술 논문에서 핵심 개념을 찾기 위해 **SciBART 후보 생성 → 의미적 관련성과 다양성을 고려한 재순위**로 이어지는 2단계 NLP 파이프라인을 구성했습니다. 본문에 등장하는 핵심어뿐 아니라 **본문에 직접 등장하지 않는 핵심어**도 생성 대상으로 다뤘습니다.

- **핵심:** SciBART 기반 핵심어 후보 생성 · SciBERT 기반 의미 순위 · MMR을 활용한 다양성 고려
- **담당:** **SciBART 파인튜닝 코드·다중 시퀀스 후보 생성기** 구현 · 생성 결과 파싱·중복 제거 · 본문 등장 여부에 따른 후보 분리
- **연결·평가:** Arrow 학습 데이터 연결과 필수 컬럼·빈 입력 검증 · **Precision·Recall·F1 평가 코드** · 후속 재순위 단계에 전달할 예측·정답 JSON/CSV 구조 구현
- 🛠 Python · SciBART · Hugging Face Transformers · KP20K · Apache Arrow
- 🔗 [프로젝트 상세](https://github.com/Token5ive/keyphrase-extraction/tree/docs/readme)

### [Multiturn Memory Chat](https://github.com/2026-Pretrained-Conversational-Model) — 대화 맥락과 PDF 검색을 결합한 챗봇 *(RAG Retriever · 임베딩·인덱싱 · 초기 채팅 UI)*

요약 메모리와 최근 대화로 맥락을 유지하고, 필요할 때 PDF 문서를 검색해 답변을 보강하는 팀 프로젝트입니다. **문서를 검색 가능한 형태로 처리하고, 답변 생성에 필요한 문맥을 전달하는 검색 단계**를 담당했습니다.

- **핵심:** 대화 메모리 · 요청 라우팅 · PDF 문서 검색 · 검색 문맥을 활용한 답변 생성
- **담당:** **PDF RAG Retriever 베이스라인** · 재귀적 청킹 · 공통 임베딩 호출 · FAISS 캐시·인덱싱·검색 문맥 반환 로직 개선
- **검증·연동:** 청크 크기별 RAGAS 평가 · 초기 채팅 MVP UI와 WebSocket·파일 업로드 통신 구현
- 🛠 Python · RAG · FAISS · RAGAS · JavaScript · WebSocket
- 🔗 [Demo](https://youtu.be/YiBWHTeuNjY)

### [ICU Sepsis Mortality Prediction](https://github.com/js-lee05/Predicting_sepsis_ICU) — 중환자실 패혈증 환자 사망 위험 예측 *(임상 데이터 전처리 · 모델 비교·검증)*

중환자실 임상 데이터를 활용해 패혈증 환자의 사망 위험 예측 가능성을 탐구했습니다. 결측치·이상치 처리부터 모델 비교까지 수행하며 **임상 데이터를 예측 모델의 입력으로 구성하는 과정**을 다뤘습니다.

- **핵심:** 임상 데이터 전처리 · 클래스 불균형 처리 · 머신러닝·딥러닝 분류 모델 비교
- **분석:** Logistic Regression · Random Forest · XGBoost · SVM · MLP · Stacking Ensemble
- **검증:** 교차 검증을 활용한 모델 평가와 비교
- 🛠 Python · SQL · Oracle DB · Machine Learning · Deep Learning

### [Single-cell RNA-seq Analysis](https://github.com/js-lee05/Single-cell_RNAseq_analysis) — 단일세포 전사체 분석 *(QC · 차원 축소 · 클러스터링 안정성 검토)*

PBMC 3k 데이터를 Seurat로 분석하고, **QC 기준·PCA 차원·클러스터링 해상도**에 따라 결과가 어떻게 달라지는지 비교했습니다. 결과의 안정성과 생물학적 해석 가능성을 함께 확인했습니다.

- **핵심:** QC → 정규화 → PCA → 클러스터링 → UMAP → 마커 기반 세포 유형 해석
- **검증:** 미토콘드리아 비율·검출 유전자 수 기준 비교 · PCA 차원과 클러스터링 해상도별 결과 검토
- **분석 관점:** 파라미터 변화에 따른 군집 구조와 마커 일관성 확인
- 🛠 R · Seurat · PCA · UMAP · Bioinformatics

## ⚒️ Skills

- **Languages:** Python · R · SQL · Dart · Swift
- **AI · LLM / NLP:** Hugging Face Transformers · SciBART · RAG · Prompt Engineering · LLM-as-Judge · RAGAS · Upstage Solar
- **Data / Analysis:** pandas · Apache Arrow · FAISS · 임상 데이터 전처리 · 분류·앙상블 모델링 · Cross Validation
- **Bioinformatics:** Seurat · Single-cell RNA-seq · QC · PCA · UMAP · Clustering
- **Application / Integration:** Streamlit · Flutter · SwiftUI · REST API · WebSocket · 공공 API 연동
- **Database / Collaboration:** Qdrant · Oracle DB · Git · GitHub

---

프로젝트별 구현 내용과 실험 과정은 각 링크에서 확인할 수 있습니다.

