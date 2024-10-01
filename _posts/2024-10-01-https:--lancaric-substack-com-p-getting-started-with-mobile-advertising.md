---
title:  "모바일 광고 수익 시작하기"

categories:
  - 번역
  
tags:
  - Lancaric
toc: true
toc_sticky: true
 
date: 2024-10-01
last_modified_at: 2024-10-01
---
**요청하신 대로 펠릭스가 전달했고, 여러분은 제 구독자로서 독점 액세스 권한을 갖게 되었습니다!**

모바일 광고는 아름답습니다! 이상하게 들리겠지만 저는 그렇게 생각합니다. 모바일 사용자 기반을 서버 비용에서 수익 창출원으로 전환할 수 있습니다. 저는 8년 가까이 모바일 광고 수익화 작업을 해왔지만, 광고 수익에 대한 정보가 부족하여 광고 수익을 시작하는 방법에 대한 가이드를 작성하고 싶었습니다.

이 가이드는 광고 수익 창출을 마스터하는 데 도움이 되는 여러 파트로 구성된 시리즈가 될 것입니다. 이번에는 기본 사항을 빠르게 익혀서 다음 파트에서 세 가지 주요 미디에이션 플랫폼(Goole Admob, 유니티 레벨 플레이, Applovin MAX)의 작동 방식을 다룰 수 있도록 도와드리겠습니다. 시작하기 전에 수익 창출을 시작하기 전에 알아두어야 할 몇 가지 용어를 소개합니다:

[공유](https://lancaric.substack.com/p/getting-started-with-mobile-advertising?utm_source=substack&utm_medium=email&utm_content=share&action=share)

### **용어**

**eCPM**

유효 마일당 비용은 애플리케이션이나 게임에서 1,000회의 노출에 대해 네트워크가 지불하는 비용입니다.

**게재율**

네트워크가 광고 요청을 처리하고 사용자에게 노출을 표시한 비율입니다.

**광고 수익**

eCPM + 게재율 = 광고에 대해 지급받는 금액

**AdARPDAU**

일일 활성 사용자당 평균 수익은 광고 수익화에서 가장 중요한 지표입니다. UA 변동에도 불구하고 광고 실적을 명확하게 파악할 수 있습니다. 매일 광고 수익과 AdARPDAU를 추적해야 합니다. 네트워크와 대화할 때는 항상 AdARPDAU를 참조하세요. 그렇지 않으면 멍청하다고 생각할 것입니다.

**광고 시청자 비율 또는 참여율**

앱에서 광고 단위에 참여하는 사용자의 비율입니다. 리워드형 광고(45% 이상), 전면 광고(60-70% 이상), 배너 광고(70-80% 이상)를 목표로 하는 지표는 다음과 같습니다. 수치가 높을수록 좋습니다(당연히).

**IMP/DAU**

일일 활성 사용자당 노출 수는 하루에 사용자당 노출되는 노출 수를 보여줍니다. 목표로 하는 지표는 보상형(5+), 전면 광고(7+), 배너(70+)입니다.

[

![alt](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F46f2e13b-79ac-4d95-9a35-c2d1d775dee7_521x496.jpeg)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F46f2e13b-79ac-4d95-9a35-c2d1d775dee7_521x496.jpeg)

이제 모바일 광고 수익화 전문가가 되기 위한 기본 사항을 충분히 익혔으니 이제 좀 더 복잡한 내용을 시작해보겠습니다.

### **광고 수익화에서 수익을 창출하는 요소는 무엇인가요?**

**공급**

공급 측면은 광고를 게재하는 퍼블리셔 또는 앱에 대한 멋진 표현입니다. 앱이나 게임의 리텐션을 떨어뜨리지 않으면서 최대한 많은 광고를 사용자에게 표시하는 것이 퍼블리셔의 역할입니다. 북극성을 목표로 삼으려면 위의 광고 시청자 비율 및 IMP/DAU 벤치마크 지표를 참조하세요.

**수요**

수요 네트워크는 앱이나 게임에 입찰하고 노출을 표시하는 광고 네트워크 및 거래소와 같은 대형 회사입니다. 여러 네트워크를 설정하여 노출 경쟁을 벌여야 광고 수익으로 연결되는 가장 높은 eCPM과 게재율을 얻을 수 있습니다.

**미디에이션 플랫폼**

미디에이션 플랫폼은 여러 광고 네트워크 또는 거래소가 인벤토리를 놓고 경쟁할 수 있는 마켓플레이스입니다. 광고 수익을 거래하는 경우 이러한 플랫폼 중 하나가 필요하며, 그렇지 않으면 인벤토리 가치의 일부만 지급받게 됩니다. 모바일의 주요 광고네트워크는 [Unity 레벨플레이](https://www.is.com/mediation/), [구글 애드](https://admob.google.com/)몹, [앱러빈 맥스입니다](https://try.applovin.com/).

그렇다면 모바일 광고로 수익을 창출하는 방법은 무엇일까요? 간단히 말해, 모바일 광고로 수익을 창출하려면 많은 사용자층이 광고를 많이 시청하도록 유도해야 합니다. 수익을 극대화하려면 여러 수요 파트너를 설정하여 미디에이션 플랫폼에서 인벤토리 가격 경쟁을 벌여야 합니다.

[

![alt](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3b8e5c04-c97a-46e4-b767-1cfc21b83643_500x575.jpeg)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3b8e5c04-c97a-46e4-b767-1cfc21b83643_500x575.jpeg)

_**기타 중요한 주제**_

광고 수익화 전문가가 되기 전에 몇 가지 더 알아두어야 할 사항도 있습니다. 이 모든 것이 결국에는 아주 멋지게 합쳐질 것이라고 믿으세요...

마테우 란카릭의 잔인하게 정직하게는 독자 지원 출판물입니다. 새 게시물을 받아보고 제 작업을 지원하려면 무료 또는 유료 구독자가 되세요.

구독 신청

### **Add-aps.txt 파일**

모바일 광고는 예전에는 완전히 엉망이었습니다. 절 믿으세요. add-apps.txt 파일은 모바일을 조금 덜 거친 서부로 만들기 위해 고안된 파일입니다. 퍼블리셔는 iOS 앱스토어 및 구글 플레이 페이지에 등록된 도메인에 이 파일을 추가해야 합니다. 다음은 콜로서기 게임즈의 [안드로이드](https://play.google.com/store/apps/details?id=com.colossi.survival.samurai&hl=en) 목록과 [앱-ads.txt 파일의](https://daisho.game/app-ads.txt)예시입니다 .

이 파일을 사용하면 광고 인벤토리를 구매할 수 있는 권한을 가진 사람을 선언할 수 있습니다. 예를 들어, King이 거래소 플랫폼에서 구매하려는 경우 이 목록을 통해 권한을 확인할 수 있습니다. app-ads.txt 파일이 없다는 것은 광고 수익이 없다는 것을 의미합니다.

이 파일에 대한 항목은 미디에이션 플랫폼과 애드 네트워크 파트너의 대시보드 두 곳에서 확인할 수 있습니다. 새 수요 파트너를 추가할 때마다 파일을 업데이트해야 합니다. 리셀러가 파트너를 추가할 때마다 60~90일마다 업데이트하는 것도 잊지 마세요. 이를 최신 상태로 유지하지 않으면 수익을 잃을 수 있습니다. 더 자세한 기술적인 분석은 [이 링크를](https://www.example.com)참조하세요.

**Sellers.json - app-ads.txt의 쌍둥이 형제**

app-ads.txt가 퍼블리셔에 초점을 맞춘다면, sellers.json은 공급 측 플랫폼이 퍼블리셔가 인벤토리를 판매할 권한이 있는지 확인하는 데 도움이 되도록 설계된 쌍둥이 형제입니다. 설정이 조금 더 까다롭지만 프로세스는 매우 유사하며, 중개 및 수요 파트너 대시보드에서 필요한 항목을 가져와 모든 항목이 합법적인지 확인합니다.

이러한 추가 검증 단계는 투명성을 보장하고 생태계 전반에서 신뢰를 구축하여 더 많은 수익을 창출하는 데 도움이 됩니다. 또한 이 파일은 60~90일마다 업데이트해야 합니다. [기술](https://support.google.com/adsense/answer/9889911?hl=en) 부분에대한 링크는 다음과 같습니다 .

### **경험 법칙**

[

![alt](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffb9b149b-cc45-4f53-8d1e-221f43276487_552x414.jpeg)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffb9b149b-cc45-4f53-8d1e-221f43276487_552x414.jpeg)

**얼마나 많은 네트워크가 필요한가요?**

지루한 대답은 광고로 얼마나 많은 돈을 벌고 있는지에 따라 다르다는 것입니다. 일반적으로 광고로 하루에 100~1,000달러를 벌고 있다면 총 4개의 파트너가 필요합니다. 하루 1000달러 이상이면 5~6개를 추가해야 하고, 하루 1만 달러 이상이면 7개 이상이 필요합니다. 네트워크가 많을수록 인벤토리에 대한 경쟁이 치열해지고 더 많은 수익을 올릴 수 있습니다.

### **네트워크를 20개 추가할 수 없는 이유는 무엇인가요?**

SDK는 앱 충돌을 일으킬 수 있으며, 골치 아픈 일을 원치 않으실 것입니다.

### **네트워크가 가치를 추가하고 있는지 어떻게 알 수 있나요?**

좋은 질문입니다! 수익 점유율이라는 것을 살펴봐야 합니다. 모든 네트워크의 수익을 일정 기간 동안 벌어들인 전체 수익으로 나누기만 하면 됩니다. 각 네트워크가 스택의 경쟁력에 가치를 더하려면 최소한 5%의 수익을 얻어야 합니다. 5%에 도달할 수 없는 네트워크가 있다면 해당 네트워크를 제거하고 다른 네트워크를 시도하세요.

구독하기

**어떤 네트워크로 시작해야 하나요?**

다음은 다양한 광고 단위를 위한 좋은 시작 네트워크입니다. 저는 보통 [앱스플라이어](https://www.appsflyer.com/resources/reports/performance-index/) 퍼포먼스 지수를 확인하여 가장 좋은 네트워크를 찾는 것을 추천합니다 . 일반적으로 UA 리더보드의 순위가 높을수록 인벤토리에 대해 더 많은 금액을 지불합니다.

#### 배너

*   구글 애드몹
    
*   메타(Android에서만 사용 가능)
    
*   Applovin(MAX 미디에이션에서만 배너 인벤토리가 있음)
    
*   유니티
    
*   디지털 튜브린(DTx 또는 파이버)
    
*   Inmobi
    

#### 인터스티셜

*   구글 애드몹
    
*   메타(Android에서만 사용 가능)
    
*   Applovin
    
*   Unity
    
*   디지털 터빈(DTx 또는 파이버라고도 함)
    
*   리프트오프(일반적으로 iOS에서 더 강력함)
    
*   Ironsource (iOS에서 가장 좋음)
    
*   Mintegral
    

#### 보상

*   구글 애드몹
    
*   메타 (안드로이드에서만 좋음)
    
*   Applovin
    
*   Unity
    
*   디지털 터빈(DTx 또는 파이버)
    
*   리프트오프(일반적으로 iOS에서 더 강력함)
    
*   Ironsource
    
*   민티그럴
    

**101 광고 수익화 과정을**수료하신 것을 축하합니다 . 이제 기본 사항을 알게 되었으니 다음 시간에는 더 흥미로운 내용을 다룰 수 있습니다. 다음 몇 개의 포스팅에서는 세 가지 주요 미디에이션 플랫폼에서 데이터를 설정, 분석 및 확인하는 방법을 보여드리겠습니다: 앱러빈 MAX, 구글 애드몹, 유니티 레벨플레이.

이와 같은 콘텐츠가 마음에 드신다면 격주로 발행되는 [뉴스레터를](https://felixbraberg.substack.com/) 구독하거나 최고의 모바일 게임 [팟캐스트인](https://www.youtube.com/@2.5gamers) 2.5 게이머를 들어보세요 .

[![](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0e0eb66c-c9dd-4f08-8e14-b84cd56fffa0_925x1071.jpeg)모바일 광고 수익모바일

게임 및 모바일 애플리케이션을 위한 모바일 광고 수익화 최적화.

게임 광고 배치 설계 및 네트워크 협상

작성자

:

Felix Braberg

](https://felixbraberg.substack.com?utm_source=substack&utm_campaign=publication_embed&utm_medium=web)

[

![alt](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd3ee36ef-cc87-4687-b1f5-5db2e4677244_1024x1024.png)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd3ee36ef-cc87-4687-b1f5-5db2e4677244_1024x1024.png)

원문: [https://lancaric.substack.com/p/getting-started-with-mobile-advertising](https://lancaric.substack.com/p/getting-started-with-mobile-advertising)