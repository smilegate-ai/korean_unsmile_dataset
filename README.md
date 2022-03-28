# Korean UnSmile Dataset
![logo](https://github.com/smilegate-ai/korean_unsmile_dataset/blob/main/rsc/unsmile_logo.jpg)   
Smilegate AI에서 공개하는 한국어 혐오표현 "☹️ UnSmile" 데이터셋입니다.    

     
## 1. 데이터셋 overview   

본 데이터셋에서의 혐오(hate)표현은 “사회적·역사적으로 차별과 억압을 받아온 소수자 집단의 정체성을 그 대상으로 하여 공격을 일삼는 표현” 으로 정의합니다.   
- **혐오의 대상이 집단으로서 명확히 지칭**된 악플/비난/비하/차별발언   
- 대상에 대한 고정관념 (e.g. 동양인은 수학 잘하지 않아?, 역시 흑형이라 운동을 잘하네)
- 대상을 강제로 고착화하는 발언 (e.g. 여자는 집에서 애나 봐야지!, 임신은 축복이지!, 게이는 잘생겨야지)   
- 화자가 속한 집단에 대한 혐오발언 (e.g. 나도 급식이지만, 하여간 급식충들 ㅉㅉㅉ)    
- 화자 스스로를 자조적으로 표현하는 경우는 혐오 발언이 아님 (e.g. 아 내가 급식충이다!)  
    
단일 데이터는 [혐오표현, 악플/욕설, clean]으로 분류될 수 있으며, 혐오 표현은 다중 레이블(multi-label)로 전문가 집단을 통해 레이블링되었습니다.   

항목 | 문장 수
:---: | ---:
혐오표현 | 10,139
악플/욕설 | 3,929
Clean | 4,674
Total | 18,742
    
### 1.1 데이터셋 예제

문장 | 여성/가족 | 남성 | 성소수자 | 인종/국적 | 연령 | 지역 | 종교 | 기타혐오 | 악플/욕설 | clean | 개인 지칭
--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---:
한남 답이 없노 | 0 | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0
옛말에 암탉이 울면 나라 망한다고 했다 | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0
꼭 키 작은 급식충이 이런 글 씀 | 0 | 0 | 0 | 0 | 1 | 0 | 0 | 0 | 0 | 0 | 0
뭐 어쩌라고 시발 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 0 | 0
혐오가 당연한 건 없습니다 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 0

### 1.2 혐오 카테고리

- [여성/가족]   
여성성과 여성의 젠더 역할을 고착화하는 발언과 여성의 불평등을 비난하는 표현을 포함합니다.   
또한, 여성의 불평등과 고착화를 타파하고, 여성의 인권 신장을 위해 발생한 페미니즘과 여성부에 대한 비난 역시 여성혐오로 분류하였습니다.    
여초 직장, 여경 등, 여성으로만 이루어진 집단에 대한 혐오 역시 여성 혐오로 분류하였습니다.   
- [남성]    
남성 비하 은어의 사용 및 남성 집단의 혐오를 분류하였습니다.   
- [성소수자]   
이성애 이외의 섹슈얼리티를 배척하는 발언을 분류하였습니다.   
또한, 비이성애 섹슈얼리티를 부정적인 대상으로 연관시키는 행동 및 성소수 문화에 대한 비난을 성소수자에 대한 혐오로 분류하였습니다.   
- [인종/국적]   
특정 인종/국적에 대한 비속어를 포함한 경우와, 특정 인종에 대한 고정관념과 선입견을 고착화하는 표현에 대해 분류하였습니다.    
또한, 특정 종교가 국교인 국가나 난민들에 대한 혐오 역시 인종/국적에 대한 혐오로 분류하였습니다.     
- [연령]    
특정 세대나 연령을 비하하는 은어의 사용 및 혐오 표현을 분류하였습니다.   
- [지역]   
특정 지역에 대한 은어 및 혐오 표현을 분류하였습니다.   
- [종교]   
특정 종교에 대한 혐오 및 종교인 집단에 대한 비난을 분류하였습니다.  
- [기타혐오]   
위에서 정의한 카테고리 이외의 집단을 대상으로 하는 혐오 표현을 분류하였습니다. (e.g. 장애인, 정부, 기자, 경찰, 차별금지법 반대 등)   
- [악플/욕설]   
어떤 집단을 향한 혐오 표현인지 지칭할 수는 없지만, 타인 혹은 외모에 대한 비하/욕설이 포함되어 있거나, 불쾌감을 주거나, 악플과 음란성 문장을 분류하였습니다.   
- [Clean]  
혐오표현, 욕설, 불쾌감, 음란성 내용을 포함하고 있지 않은 일반 문장을 분류하였습니다.   

### 1.3 개인 지칭 여부
- 혐오 및 욕설의 대상이 특정 인물을 지칭하고, 그 대상을 대중들이 누구인지 눈치챌 수 있을 경우 '개인 지칭' 항목으로 추가 태깅하였습니다.

### 1.4 어노테이션 방법
- 단일 댓글 문장에 대해 3명의 작업자가 혐오 카테고리 분류
- 5인의 혐오 표현 전문가가 최종 검수
- **혐오의 판단 기준은 사람마다 상이할 수 있으며, 태깅 결과는 100%의 정확도를 보장하지 않습니다. 태깅 오류를 발견하실 경우, issue에 남겨주세요!**

## 2. 데이터셋 사용법
본 데이터셋은 huggingface datasets hub를 통해 사용할 수 있습니다.   

항목 | 여성/가족 | 남성 | 성소수자 | 인종/국적 | 연령 | 지역 | 종교 | 기타혐오 | 악플/욕설 | clean  
:---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---:
Train | 1,599 | 1,347 | 1,138 | 1,728 | 603 | 1,052 | 1,181 | 569 | 3,146 | 3,739
Validation | 394 | 334 | 280 | 426 | 146 | 260 | 290 | 134 | 786 | 935 
Total | 1,993 | 1,681 | 1,418 | 2,154 | 749 | 1,312 | 1,471 | 703 | 3,932 | 4,674    

- Python
```python
>>> from datasets import load_dataset
>>> datasets = load_dataset('smilegate-ai/kor_unsmile')
>>> print(datasets)
DatasetDict({
    valid: Dataset({
        features: ['문장', '여성/가족', '남성', '성소수자', '인종/국적', '연령', '지역', '종교', '기타 혐오', '악플/욕설', 'clean', '개인지칭', 'labels'],
        num_rows: 3737
    })
    train: Dataset({
        features: ['문장', '여성/가족', '남성', '성소수자', '인종/국적', '연령', '지역', '종교', '기타 혐오', '악플/욕설', 'clean', '개인지칭', 'labels'],
        num_rows: 15005
    })
})
```

## 3. Baseline 모델 사용법
### 3.1 Baseline 모델 학습
Google colab을 통해 모델 학습과 테스트를 할 수 있는 tutorial 노트북을 공유합니다.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1NKYYVSex__vde-lnYCmsRmyHjJhV6cKt?usp=sharing)   

### 3.2 Baseline 모델 테스트
- Python
```python
>>> from transformers import TextClassificationPipeline, BertForSequenceClassification, AutoTokenizer
>>> model_name = 'smilegate-ai/kor_unsmile'
>>> model = BertForSequenceClassification.from_pretrained(model_name)
>>> tokenizer = AutoTokenizer.from_pretrained(model_name)
>>> pipe = TextClassificationPipeline(
        model = model,
        tokenizer = tokenizer,
        device = 0,   # cpu: -1, gpu: gpu number
        return_all_scores = True,
        function_to_apply = 'sigmoid'
    )
>>> for result in pipe("이래서 여자는 게임을 하면 안된다")[0]:
        print(result)
    
{'label': '여성/가족', 'score': 0.8253053426742554}
{'label': '남성', 'score': 0.039725180715322495}
{'label': '성소수자', 'score': 0.012144332751631737}
{'label': '인종/국적', 'score': 0.023181889206171036}
{'label': '연령', 'score': 0.010315303690731525}
{'label': '지역', 'score': 0.018454890698194504}
{'label': '종교', 'score': 0.011270025745034218}
{'label': '기타 혐오', 'score': 0.0207340307533741}
{'label': '악플/욕설', 'score': 0.057331427931785583}
{'label': 'clean', 'score': 0.1401052623987198}
```

### 3.3 Baseline 모델 결과

문장 | 여성/가족 | 남성 | 성소수자 | 인종/국적 | 연령 | 지역 | 종교 | 기타혐오 | 악플/욕설 | clean   
--- | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---:
이래서 여자는 게임을 하면 안된다 | **0.83** | 0.04 | 0.01 | 0.02 | 0.01 | 0.02 | 0.01 | 0.02 | 0.06 | 0.12
한남 재기해 | 0.04 | **0.90** | 0.01 | 0.03 | 0.02 | 0.02 | 0.02 | 0.01 | 0.08 | 0.05
젠신병자들 극혐 | 0.13 | 0.04 | **0.93** | 0.04 | 0.14 | 0.07 | 0.07 | **0.77** | 0.10 | 0.04
니네 나라로 좀 돌아가라 | 0.02 | 0.02 | 0.01 | **0.90** | 0.02 | 0.02 | 0.03 | 0.02 | 0.06 | 0.04
틀니 압수할게요 | 0.02 | 0.04 | 0.03 | 0.02 | **0.70** | 0.02 | 0.02 | 0.03 | 0.07 | 0.11
너도 설마 머구 출신? | 0.02 | 0.01 | 0.02 | 0.04 | 0.02 | **0.90** | 0.02 | 0.03 | 0.04 | 0.13
개독이나 이슬람이나 똑같지 않냐 | 0.03 | 0.02 | 0.03 | 0.08 | 0.02 | 0.03 | **0.95** | 0.04 | 0.03 | 0.04
지잡 나와서 고생한다 | 0.03 | 0.02 | 0.04 | 0.02 | 0.10 | 0.10 | 0.11 | **0.55** | 0.30 | 0.08
진짜 극혐이네요 | 0.01 | 0.01 | 0.01 | 0.01 | 0.01 | 0.02 | 0.02 | 0.02 | **0.88** | 0.08
남자 여자 모두 응원합니다 | 0.18 | 0.05 | 0.03 | 0.01 | 0.01 | 0.01 | 0.01 | 0.01 | 0.05 | **0.76**

```
                precision    recall  f1-score   support

     여성/가족       0.85      0.70      0.76       394
         남성       0.87      0.83      0.85       334
      성소수자       0.90      0.78      0.83       280
     인종/국적       0.87      0.79      0.82       426
         연령       0.92      0.75      0.83       146
         지역       0.87      0.88      0.88       260
         종교       0.87      0.86      0.87       290
      기타혐오       0.92      0.18      0.30       134
     악플/욕설       0.76      0.59      0.67       786
       clean       0.74      0.79      0.77       935

   micro avg       0.82      0.73      0.77      3985
   macro avg       0.86      0.72      0.76      3985
weighted avg       0.82      0.73      0.77      3985
 samples avg       0.76      0.74      0.75      3985

```
## 4. Citation
```
@misc{SmilegateAI2022KoreanUnSmileDataset,
  title         = {Korean UnSmile dataset: Human-annotated Korean Hate Speech Dataset},
  author        = {Seonghyun Kim},
  year          = {2022},
  howpublished  = {\url{https://github.com/smilegate-ai/korean_unsmile_dataset}},
}
```

## 5. Contributors
기획 및 제작 ([Smilegate AI](https://smilegate.ai))       
![smilegate_ai](https://github.com/smilegate-ai/korean_unsmile_dataset/blob/main/rsc/smilegate_ai.jpg)    

데이터 태깅 및 검수 ([언더스코어](http://underscore.kr/))    
![underscore](https://github.com/smilegate-ai/korean_unsmile_dataset/blob/main/rsc/underscore.jpg)     
```
언더스코어는 데이터 기반 지식 컨텐츠 스타트업입니다.    
전문지식을 소개하는 모션그래픽을 제작하고, 사회과학 분야에서 데이터 분석과 컨설팅 활동을 해오고 있습니다.     
```

## 6. 홍보 자료   
데이터셋 소개 영상    
[![[Smilegate AI] UnSmile 데이터셋](http://img.youtube.com/vi/XmCnlcnzWtQ/0.jpg)](https://youtu.be/XmCnlcnzWtQ?t=0s)    

    
## 7. License
Smilegate AI `UnSmile`의 `소스코드 및 baseline 모델`은 [Apache 2.0](https://www.apache.org/licenses/LICENSE-2.0) 라이선스 하에 공개되어 있습니다.   
Smilegate AI `UnSmile`의 `데이터셋`은 [CC-BY-NC-ND 4.0](https://creativecommons.org/licenses/by-nc-nd/4.0/) 라이선스 하에 공개되어 있습니다.   
코드 및 모델, 데이터셋을 사용할 경우 라이선스 내용을 준수해 주십시오.    
데이터셋의 상업적 사용의 경우, `seonghkim@smilegate.com` 으로 문의 부탁드립니다.    
본 데이터셋의 내용은 Smilegate AI의 의견과 무관합니다.     
