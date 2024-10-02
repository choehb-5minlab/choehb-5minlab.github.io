---
title:  "CPI와 LTV 방정식 이해하기"

categories:
  - 번역
  
tags:
  - Lancaric
toc: true
toc_sticky: true
 
date: 2024-10-02
last_modified_at: 2024-10-02
---
모바일 게임의 경쟁 환경에서 사용자 확보(UA) 전략을 최적화하고 수익을 극대화하려면 설치당 비용(CPI)과 평생 가치(LTV) 간의 역학 관계를 이해하는 것이 중요합니다.

이 문서에서는 CPI가 UA 지출에 미치는 영향, LTV 계산, CPI 대 LTV 공식에 따른 의사 결정, 게임 장르별 이상적인 투자 회수 기간, UA에서 LTV 예측 사용, 벤치마크 설정과 LTV 예측 활용에 대해 자세히 설명합니다.

## CPI가 사용자 확보 지출에 미치는 영향

**CPI(설치당 비용)** 는 게임 개발자 또는 퍼블리셔가 유료 광고 활동을 통해 사용자가 게임을 설치할 때마다 발생하는 평균 비용입니다. CPI는 UA 캠페인에 필요한 전체 예산에 직접적인 영향을 미치기 때문에 매우 중요한 지표입니다.

*   **예산 할당**: CPI가 높을수록 각 유저를 확보하는 데 더 많은 비용이 들며, UA 목표를 달성하기 위해 더 많은 예산이 필요합니다. 반대로 CPI가 낮으면 동일한 예산 내에서 더 많은 사용자를 확보할 수 있습니다.
    
*   **시장 경쟁력**: CPI는 시장 수요와 경쟁의 영향을 받습니다. 인기 있는 장르나 키워드는 여러 광고주의 입찰이 증가하기 때문에 CPI가 더 높을 수 있습니다.
    
*   **타겟팅 및 품질**: 타겟팅 범위를 넓게 설정하면 CPI는 낮아질 수 있지만 참여도가 낮은 사용자를 유치할 수 있습니다. 타겟팅 범위를 좁히면 CPI는 높아지지만 잠재적으로 더 높은 가치의 사용자를 유치할 수 있습니다.
    

**UA 지출에 미치는 영향**:

*   **캠페인 확장**: CPI를 이해하면 캠페인을 효율적으로 확장하는 데 도움이 됩니다. CPI가 낮고 사용자 품질이 높으면 UA 지출을 늘리는 것이 합리적입니다.
    
*   **ROI 고려 사항**: CPI가 확보한 유저의 LTV를 초과하지 않도록 UA 지출을 조정하여 긍정적인 투자 수익률(ROI)을 보장해야 합니다.
    

게임 확장은 [킬러 유저 확보](https://lancaric.me/11-tips-for-killer-user-acquisition-ops-q1-2023/) 작업의 기능만이 아닙니다 . 이는 LTV의 함수이기도 합니다. LTV가 허용하는 범위까지만 예산을 확장할 수 있습니다. 예를 들어 LTV가 5달러인 경우 4.5달러(또는 마진에 따라 계산한 다른 CPI)에 도달할 때까지 수익성 있는 캠페인을 실행할 수 있습니다.

[

![alt](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F61dfe2ad-9d0e-4d59-94f8-8383ff48d7bc_1920x1181.png)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F61dfe2ad-9d0e-4d59-94f8-8383ff48d7bc_1920x1181.png)

이것은 제가 가장 좋아하는 과거 CPI 그래프입니다. 겨울왕국 기억하시나요? 과거의 명작이지만 이 목적에 잘 부합하는 게임입니다!

방치형 게임은 일반적으로 다른 카테고리보다 CPI가 낮습니다. 여기서 중요한 것은 **로우 폴리** [시각적 디자인입니다](https://lancaric.me/tag/visual-design/).

하이퍼 캐주얼 게임이 항상 로우 폴리를 사용하는 이유를 누군가 깨달았습니다. **낮은 CPI를 유도하기** 때문입니다. 저는 게임의 고급스러운 느낌 때문에 "화려하거나 더 높은 퀄리티"의 비주얼 스타일이 어떻게 더 높은 IAP를 유도하는지에 대해 많은 토론을 했습니다. 정말 WTF?

비주얼 스타일은 IAP에 영향을 미치지 않습니다. 다른 의견이 있으시면 저에게 메시지를 보내주시면 논의해 보겠습니다. 왜 그럴까요?

## LTV는 어떻게 계산되나요?

**평생 가치(LTV)는** 사용자가 게임을 플레이하는 전체 기간 동안 게임에서 기대할 수 있는 총 수익을 나타냅니다. LTV를 정확하게 계산하는 것은 정보에 기반한 UA 결정을 내리는 데 필수적입니다.

[공유](https://lancaric.substack.com/p/understanding-the-cpi-vs-ltv-equation?utm_source=substack&utm_medium=email&utm_content=share&action=share)

**LTV 계산 방법**:

1.  **과거 데이터 분석**:
    
    *   **사용자당 평균 수익(ARPU)**: 특정 기간 동안의 총 수익을 사용자 수로 나누어 계산합니다.
        
    *   **이탈률**: 사용자가 얼마나 빨리 게임을 중단하는지 파악하면 향후 수익을 예측하는 데 도움이 됩니다.
        
    *   **리텐션율**: 리텐션율: 리텐션율이 높을수록 일반적으로 LTV가 높습니다.
        
2.  **예측 모델링**:
    
    *   **코호트 분석**: 게임을 시작한 시간을 기준으로 사용자를 그룹화하여 지출과 리텐션의 패턴을 파악합니다.
        
    *   **머신 러닝 모델**: 알고리즘을 활용하여 과거 데이터를 기반으로 미래의 사용자 행동을 예측합니다.
        

[LTV 예측은](https://appmetrica.yandex.com/about/blog/ltv-churn-predictions?utm_source=post&utm_medium=blog&utm_campaign=BrutallyHonest3009) 이 개념을 한 단계 발전시킨 것으로, AI를 활용하여 LTV가 가장 높은 잠재 사용자를 찾아냅니다. 이 기능을 통해 사용자 확보 관리자는 가장 높은 수익을 창출할 가능성이 높은 사용자를 타겟팅하여 전략을 최적화할 수 있습니다.

[

![alt](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb35614d0-dc74-42f1-9fa8-c287c6f1fd0f_1642x933.png)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb35614d0-dc74-42f1-9fa8-c287c6f1fd0f_1642x933.png)

### **주요 기능**

LTV 예측은 앱에 가입한 후 24시간 이내에 각 사용자를 평가하여 28일 동안의 LTV 예측을 생성합니다. 이러한 예측을 기반으로, 몇 번의 클릭만으로 AppMetrica에서 직접 광고 네트워크로 포스트백을 전송하고 상위 LTV 사용자를 위한 캠페인을 최적화할 수 있습니다.

[

![alt](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F91cc0f3c-f199-416b-a5ab-a520279915fd_872x512.jpeg)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F91cc0f3c-f199-416b-a5ab-a520279915fd_872x512.jpeg)

'체류 시간' 및 '참여도'와 같은 기존 지표를 기반으로 한 기존의 최적화 제안과 달리, 새로운 AI 기반 예측 모델은 모든 사용자의 잠재 LTV에 대한 방대한 양의 데이터를 수집 및 분석하여 광고 캠페인에 가장 적합한 양질의 리드를 찾아냅니다. 이 모델은 정확성을 보장하기 위해 다음 공식을 사용합니다.

LTV = 전체 수익 x P (LTV > 0) + 수익 (첫날) x 1 - P (LTV > 0)

또한 LTV 예측을 사용하면 사용자를 다양한 LTV 코호트(예: 상위 5, 상위 20, 상위 50, 하위 50)로 분류하고 비교할 수 있습니다.

[

![alt](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F37ad2ef9-f6a5-45be-91d8-0c9a63646503_1642x945.png)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F37ad2ef9-f6a5-45be-91d8-0c9a63646503_1642x945.png)

예측의 정확성을 테스트하고 어떤 방법이 더 많은 참여를 유도하는지 평가하기 위해 창립 팀은 게임 앱에 대한 A/B 테스트를 실행했습니다:

이 테스트에서는 두 가지 옵션을 비교했습니다:

*   '사용자가 10분 이상 플레이' 이벤트에 기반한 최적화
    
*   상위 20%의 유료 사용자(상위20LTV)에 대한 예측 모델에 기반한 최적화
    

캠페인 설정과 예산은 동일했습니다. 캠페인의 첫 10일 동안은 데이터 세트를 학습하고 구축하는 데 보냈습니다. 그 다음 주에는 AppMetrica 전문가들이 예측 모델에 사용할 설치 데이터를 수집했습니다.

[AppMetrica의 A/B 테스트 결과,](https://appmetrica.yandex.com/about/blog/ltv-churn-predictions?utm_source=post&utm_medium=blog&utm_campaign=BrutallyHonest3009) LTV 보고서를 기반으로 캠페인을 최적화하는 것이 압도적으로 유리한 [것으로 나타났습니다](https://appmetrica.yandex.com/about/blog/ltv-churn-predictions?utm_source=post&utm_medium=blog&utm_campaign=BrutallyHonest3009).

마테즈 란카릭의 Brutally Honest는 독자 지원 출판물입니다. 새 게시물을 받아보고 제 작업을 지원하려면 무료 또는 유료 구독자가 되세요.

구독 신청하기

### **이탈 예측**

사용자 이탈은 모바일 앱 마케팅의 일반적인 과제입니다. 앱을 떠날 가능성이 높은 사용자를 파악하고 이들을 유지하기 위한 사전 조치를 구현하는 것은 장기적인 성공을 위해 필수적입니다.

### **작동 방식**

이탈 예측을 통해 앱 소유자와 마케팅 팀은 앱을 설치하자마자 시간이 지남에 따라 이탈할 가능성이 높은 신규 사용자를 식별할 수 있습니다.

AI 모델은 3주 동안의 모든 활성 사용자를 분석하여 매일 활동 점수를 매깁니다. 이 모델에는 특정 지표가 필요하지 않지만, 특정 앱의 일반적인 사용자 라이프사이클에 따라 앱 사용을 중단할 가능성이 높은 사용자를 정확하게 예측합니다. 생성된 보고서는 이탈 확률에 따라 모든 사용자를 그룹으로 나눕니다: >95%, 75-95%, 50-75%, <50%, 3 시그마 규칙에 따라 99%의 정확도로 모든 사용자를 그룹화합니다.

[

![alt](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fee0e1a1a-8270-45fe-bf13-bb82aa6f09ce_1151x603.png)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fee0e1a1a-8270-45fe-bf13-bb82aa6f09ce_1151x603.png)

이 기능을 사용하면 개인화된 푸시 알림, 개인화된 인센티브 제공 등 예측 분석을 활용하여 사용자 이탈을 방지하는 타겟팅된 리텐션 전략을 구현할 수 있습니다.

어떤 사용자가 이탈할 가능성이 높은지 파악하면 사용자의 참여를 유도하고 가능한 한 빨리 앱에서 이탈하는 것을 방지할 수 있습니다. 앱메트리카를 사용하면 개인화된 푸시 알림을 통해 계정에서 직접 사용자에게 도달할 수 있어 매우 편리합니다!

구독하기

**LTV에 영향을 미치는 요인**:

*   **인앱 구매(IAP)**: 가상 상품이나 프리미엄 기능을 구매한 사용자로부터 발생하는 수익입니다.
    
*   **광고 수익**: 게임 내에서 사용자에게 광고를 표시하여 얻은 수익입니다.
    
*   **사용자 참여도**: 참여도가 높은 사용자는 더 많이 지출하고 더 오래 머무를 가능성이 높습니다.
    
*   **게임 업데이트 및 콘텐츠**: 정기적인 업데이트는 리텐션을 개선하고 LTV를 높일 수 있습니다.
    

## CPI와 LTV 방정식에 기반한 의사 결정

UA의 기본 원칙은 **CPI가** 확보한 유저의**LTV보다 낮아야**한다는 것입니다 . 이를 통해 발생하는 수익이 사용자 확보 비용을 정당화할 수 있습니다.

**시나리오**:

*   **CPI < LTV**: 수익성 있는 시나리오. UA 캠페인을 확장할 수 있습니다.
    
*   **CPI > LTV**: 수익성 없는 시나리오. UA 전략을 재평가해야 합니다.
    

**의사 결정 전략**:

*   **타겟팅을 조정합니다**: 잠재 고객 세그먼트를 세분화하여 LTV가 높은 사용자를 유치합니다.
    
*   **크리에이티브 최적화**: 광고 크리에이티브를 개선하여 전환율을 높이고 CPI를 낮춥니다.
    

[

## 크리에이티브 프레임워크: 2024년에 승리하는 방법

](https://lancaric.substack.com/p/creative-framework-how-to-win-in)

[마테이 란카릭](https://substack.com/profile/13004439-matej-lancaric)

\-

Feb 24

[![Creative framework: How to win in 2024?](https://substackcdn.com/image/fetch/w_280,h_280,c_fill,f_auto,q_auto:good,fl_progressive:steep,g_auto/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1c5db451-af1e-4965-b0ea-44b5e5e10b1c_1479x820.png)](https://lancaric.substack.com/p/creative-framework-how-to-win-in)

[

2024년의 크리에이티브 프레임워크에 대해 자세히 알아보겠습니다. 이 글에서는 구독을 유료로 업그레이드해야 하는 이유를 알려드리고자 합니다:

](https://lancaric.substack.com/p/creative-framework-how-to-win-in)

[

전체 스토리 읽기

](https://lancaric.substack.com/p/creative-framework-how-to-win-in)

*   **수익화 강화**: 게임 내 수익화 전략을 개선하여 LTV를 높이세요.
    

## 각 게임/장르에 가장 적합한 투자 회수 기간은 무엇인가요?

**투자 회수 기간은** 유저를 확보하는 데 드는 비용을 유저로부터 얻은 수익으로 충당하는 데 걸리는 시간입니다.

**투자 회수 기간에 영향을 미치는 요인**:

*   **게임 장르**:
    
    *   **하이퍼 캐주얼 게임**: 일반적으로 LTV가 낮고 투자 회수 기간이 짧습니다(보통 며칠 또는 몇 주 이내).
        
    *   **하이브리드 캐주얼 게임:** 더 높은 리텐션, 더 큰 지출 깊이. 하이퍼 캐주얼의 시장성을 차용하지만 플레이어가 더 많이 지출할 수 있습니다! (보통 1~6개월의 투자 회수 기간)
        
    *   **미드코어에서 하드코어 게임**: 더 긴 투자 회수 기간(수개월에서 수년)을 가진 더 높은 LTV.
        

[

## 하이브리드 캐주얼 UA 플레이북 - 실제 데이터로 알아보세요!

](https://lancaric.substack.com/p/hybrid-casual-ua-playbook-real-data)

[마테이 란카릭](https://substack.com/profile/13004439-matej-lancaric)

\-

11월 30, 2023

[![Hybrid casual UA playbook - Real data inside!](https://substackcdn.com/image/fetch/w_280,h_280,c_fill,f_auto,q_auto:good,fl_progressive:steep,g_auto/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd9bdd93e-7867-4469-9587-4fa23969156e_1920x896.png)](https://lancaric.substack.com/p/hybrid-casual-ua-playbook-real-data)

[

이번 달에도 유료 구독자만을 위한 하이브리드 캐주얼 팁과 요령으로 가득한 뉴스레터!

](https://lancaric.substack.com/p/hybrid-casual-ua-playbook-real-data)

[

전체 스토리 읽기

](https://lancaric.substack.com/p/hybrid-casual-ua-playbook-real-data)

*   **수익화 모델**:
    
    *   **광고 지원 게임**: 광고 수익에 의존하며, 사용자당 수익이 낮기 때문에 투자 회수 기간이 더 짧을 수 있습니다.
        
    *   **부분 유료화 모델**: 시간이 지남에 따라 사용자가 더 많은 비용을 지출할 수 있으므로 투자 회수 기간이 더 길어질 수 있습니다.
        

**최적의 투자 회수 기간 결정하기**:

*   **재무 목표**: 회사의 현금 흐름 요구 사항 및 투자 여력에 맞춰 조정합니다.
    
*   **시장 기준**: 유사한 게임 장르의 업계 평균과 비교하여 벤치마킹합니다.
    
*   **사용자 행동**: 사용자 지출 및 참여 패턴을 분석하여 현실적인 투자 회수 기간을 설정합니다.
    

구독하기

## 사용자 확보에 LTV 예측을 어떻게 활용하나요?

게임 개발자는정확한 **LTV 예측을** 통해 UA 전략에서 데이터 기반 의사 결정을 내릴 수 있습니다.

**LTV 예측 활용하기**:

*   **예산 할당**: LTV가 높은 유저를 유치하는 채널이나 캠페인에 더 많은 예산을 할당할 수 있습니다.
    
*   **입찰가 최적화**: 광고 플랫폼에서 입찰가를 조정하여 LTV가 높을 가능성이 높은 사용자를 타겟팅할 수 있습니다.
    
*   **개인 맞춤형 마케팅**: 더 많은 수익을 창출할 것으로 예상되는 세그먼트에 마케팅 메시지를 맞춤 설정합니다.
    

**LTV 예측 방법**:

*   **코호트 분석**: 사용자 그룹의 패턴을 파악하여 향후 행동을 예측합니다.
    
*   **예측 분석**: 통계 모델과 머신 러닝을 사용하여 초기 사용자 행동 지표를 기반으로 LTV를 예측합니다.
    

[

![alt](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb9731ab6-d818-4721-b41a-6f455f749042_1142x582.png)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb9731ab6-d818-4721-b41a-6f455f749042_1142x582.png)

## 벤치마크를 설정하는 방법과 LTV 예측을 사용하는 시기 비교

**벤치마크 설정하기**:

*   **업계 표준**: 업계 보고서의 평균 CPI, LTV, 투자 회수 기간을 초기 벤치마크로 사용합니다.
    
*   **과거 실적**: 게임의 과거 실적 데이터를 활용하여 현실적인 벤치마크를 설정합니다.
    
*   **경쟁사 분석**: 가능한 경우 경쟁사 지표를 분석합니다.
    

**LTV 예측을 사용하는 시기**:

*   **신규 게임 또는 업데이트**: 과거 데이터가 제한적인 경우 예측 모델을 통해 LTV를 예측할 수 있습니다.
    
*   **역동적인 시장**: 급변하는 시장에서는 실시간 LTV 예측을 통해 UA 전략을 즉각적으로 조정할 수 있습니다.
    
*   **개인화**: 고도로 세분화된 UA 캠페인의 경우, LTV 예측을 통해 세분화된 수준에서 노력을 최적화할 수 있습니다.
    

**벤치마크와 예측의 균형**:

*   **지속적인 모니터링**: 실제 성과를 벤치마크와 정기적으로 비교하고 그에 따라 예측을 조정합니다.
    
*   **유연한 전략**: 예측 인사이트와 벤치마크 비교를 기반으로 UA 전략을 전환할 준비를 하세요.
    

## 마지막으로 몇 가지 당부

모바일 게임의 재정적 성공을 위해서는 CPI와 LTV 방정식을 이해하고 효과적으로 관리하는 것이 필수적입니다. 개발자는 CPI가 UA 지출에 미치는 영향을 면밀히 분석하고, LTV를 정확하게 계산 및 예측하고, 이러한 지표를 기반으로 정보에 입각한 의사 결정을 내림으로써 UA 전략을 최적화하여 ROI를 극대화할 수 있습니다.

또한 적절한 투자 회수 기간을 설정하고 예측 분석과 벤치마크의 균형을 맞추면 접근 방식을 더욱 세분화하여 경쟁이 치열한 모바일 게임 업계에서 지속적인 성장과 수익성을 보장할 수 있습니다.

원문: [https://lancaric.substack.com/p/understanding-the-cpi-vs-ltv-equation](https://lancaric.substack.com/p/understanding-the-cpi-vs-ltv-equation)