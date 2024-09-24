---
title:  "GTA V의 보행자 대화 시스템 분석: 추측성 예시를 통한 분석"

categories:
  - 번역
  
tags:
  - Game Developer
toc: true
toc_sticky: true
 
date: 2024-09-25
last_modified_at: 2024-09-25
---
[![Picture of Randen Banuelos](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltf854e47803046268/65088a4025eac30e9149356b/Randen_Banuelos.png?width=100&auto=webp&quality=80&disable=upscale "Picture of Randen Banuelos")](https://www.gamedeveloper.com/author/randen-banuelos)

[랜든 바누엘로스](https://www.gamedeveloper.com/author/randen-banuelos), 블로거

9월 24일, 2024

8분 읽기

![Trevor from Grand Theft Auto 5 in a Hawaiian shirt, about to hit a shocked mime with a baseball bat outside a dress shop at night](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt0faac3707967ba90/66f23f114b1cc002d25fb64f/GTA5_Trevor_Hitting_Mime_(1).png?width=1280&auto=webp&quality=95&format=jpg&disable=upscale "Trevor from Grand Theft Auto 5 in a Hawaiian shirt, about to hit a shocked mime with a baseball bat outside a dress shop at night")

GTA V의 보행자 대화 시스템은 게임의 사운드스케이프를 채웁니다.Rockstar Games

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/breaking-down-gta-v-s-pedestrian-dialogue-system-an-analysis-with-speculative-examples)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/breaking-down-gta-v-s-pedestrian-dialogue-system-an-analysis-with-speculative-examples)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/breaking-down-gta-v-s-pedestrian-dialogue-system-an-analysis-with-speculative-examples)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#95aae6e0f7fff0f6e1a8d7e7f0f4fefcfbf2b5f1fae2fbb5d2c1d4b5c3b3b6eda7a2aee6b5e5f0f1f0e6e1e7fcf4fbb5f1fcf4f9faf2e0f0b5e6ece6e1f0f8afb5d4fbb5f4fbf4f9ece6fce6b5e2fce1fdb5e6e5f0f6e0f9f4e1fce3f0b5f0edf4f8e5f9f0e6b3f4f8e5aef7faf1eca8dcb0a7a5e1fdfae0f2fde1b0a7a5e1fdf0b0a7a5f3faf9f9fae2fcfbf2b0a7a5f3e7faf8b0a7a5d2f4f8f0b0a7a5d1f0e3f0f9fae5f0e7b0a7a5f8fcf2fde1b0a7a5fcfbe1f0e7f0e6e1b0a7a5ecfae0bbb0a5d1b0a5d4b0a5d1b0a5d4b0a7a5d7e7f0f4fefcfbf2b0a7a5f1fae2fbb0a7a5d2c1d4b0a7a5c3b3b6eda7a2aee6b0a7a5e5f0f1f0e6e1e7fcf4fbb0a7a5f1fcf4f9faf2e0f0b0a7a5e6ece6e1f0f8b0a6d4b0a7a5d4fbb0a7a5f4fbf4f9ece6fce6b0a7a5e2fce1fdb0a7a5e6e5f0f6e0f9f4e1fce3f0b0a7a5f0edf4f8e5f9f0e6b0a5d1b0a5d4fde1e1e5e6b0a6d4b0a7d3b0a7d3e2e2e2bbf2f4f8f0f1f0e3f0f9fae5f0e7bbf6faf8b0a7d3f1f0e6fcf2fbb0a7d3f7e7f0f4fefcfbf2b8f1fae2fbb8f2e1f4b8e3b8e6b8e5f0f1f0e6e1e7fcf4fbb8f1fcf4f9faf2e0f0b8e6ece6e1f0f8b8f4fbb8f4fbf4f9ece6fce6b8e2fce1fdb8e6e5f0f6e0f9f4e1fce3f0b8f0edf4f8e5f9f0e6)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/breaking-down-gta-v-s-pedestrian-dialogue-system-an-analysis-with-speculative-examples&title=Breaking%20down%20GTA%20V's%20pedestrian%20dialogue%20system%3A%20An%20analysis%20with%20speculative%20examples)

## 앰비언트 및 보행자 대화란 무엇인가요?

그랜드 테프트 오토 시리즈나 사이버펑크 2077과 같은 대규모 AAA 게임의 경우 퀘스트, 컷신, 아군 대화 등 플레이어와 대면하는 이벤트의 대사만 작성하는 것만으로는 충분하지 않습니다. 이 정도 규모의 게임 월드에 '살아 있는' 느낌을 주려면 플레이어의 개입 없이 NPC끼리 대화를 주고받으며 독립적인 주체성을 부여해야 합니다. 이러한 주체성을 전달하는 가장 좋은 방법은 무엇일까요? 바로 앰비언트 대화를 도입하는 것입니다.

앰비언트 대화 또는 보행자 대화는 플레이어가 직접 입력하지 않고 일반 NPC와 대화하는 대화로폭넓게 정의할 수 있습니다 . 게임의 일반적인 대화는 플레이어가 NPC에게 다가가 버튼 프롬프트를 누르고 해당 캐릭터와 대화를 시작하는 플레이어 주도형 대화입니다. 반면 주변 대화는 [플레이어의 존재 여부와 관계없이](https://www.youtube.com/watch?v=pzHYESXYf4g) 자율적으로 발생합니다 .

## GTA V는 앰비언트 대화를 어떻게 구현하나요?

![A screenshot from Grand Theft Auto 5, overlooking Mount Chiliad at sunset, with the Vinewood sign and a plane visible.](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltd52f0e1a85ebb528/66f18ed317ab7da859003f6a/GTA5_Vinewood_Sign.png?width=700&auto=webp&quality=80&disable=upscale "A screenshot from Grand Theft Auto 5, overlooking Mount Chiliad at sunset, with the Vinewood sign and a plane visible.")

주변 대화 시스템은 NPC 스폰 구역과 같이 함께 작동하는 여러 하위 시스템을 사용합니다. 출처: 락스타 게임즈

참고: 이 내용은 Grand Theft Auto V에서 보행자 대화 시스템을 어떻게 구성했는지에 대한 교육적인 추론입니다. 이는 최종적이고 완전히 정확한 요약이 아닙니다.

앞서 언급했듯이 Grand Theft Auto V와 같은 거대한 규모의 게임은 보행자 대화를 사용하여 게임의 사운드스케이프를 채우고 로스 산토스를 실제 대도시처럼 느끼게 하는 데 의존합니다. 예를 들어, 57마리의 고양이에게 밥을 주는 데 도움을 요청하는 NPC가 없다면 GTA V는 훨씬 더 공허하게 느껴질 것입니다. 보행자들이 지나치는 이러한 작은 일회성 이벤트는 종종 간과되지만 게임 상호작용의 중요한 부분입니다.

### NPC 스폰 구역

GTA V의 주변 대화 시스템 작동 방식의 핵심 부분은 연결된 기본 메커니즘인 NPC 스폰 시스템에 의존합니다. 예를 들어, 사업가 NPC는 주로 록포드 힐즈 주변에, 시골 호박은 주로 포도씨와 블레인 카운티에 출현하는 등 로스 산토스의 특정 구역에서 다른 NPC보다 높은 확률로 스폰될 수 있는 NPC가 있습니다.

### NPC 원형

제작 과정에서 리소스를 절약하기 위해 록스타는 NPC마다 개별 대화 풀을 만들지 않고 NPC의 '원형'을 만들기로 결정했습니다. 숲 경비원, 머슬마니아, 연예인 지망생 등 록스타는 이런 역할을 몇 가지로 분류하고 각역할에 [맞는 대사를](https://www.youtube.com/watch?v=HJcwuD5DEdU)만든 다음 각각에 맞는 남성 및 여성 음성을 녹음했습니다.

### "범용" 대화

록스타는 이러한 캐릭터 아카이브의 활용 범위를 넓히기 위해 보행자 대화 시스템에 장소별 음성 대사를 포함하지 않기로 결정했습니다. 이 결정으로 인해 지나가는 NPC의 주변 대사가 평범하게 느껴질 수도 있지만, 각 역할마다 위치 기반 변형을 만들 필요가 없어져 아키타입 로직을 단순화하는 데 도움이 되었습니다(예: 일반적인 부자 NPC 한 명과 와인우드, 록포드 힐스, 베스푸치 등에 특정 NPC를 배치하는 등).

이 방법론은 캐릭터가 서로 대화하는 경우에도 적용됩니다. 한 NPC가 다른 NPC와 대화할 때 일반적으로 매우 짧은(종종 단절된) 대사로 응답하여 대화를 종료합니다("뭐?", "누가 신경이나 써!", "믿을 수 없어!" 등). 이는 이전과 마찬가지로 녹음된 각 대사를 최대한 활용하기 위한 것이며, 이러한 무작위 NPC 대화 이벤트를 실행하는 시스템 로직을 단순화하는 데 도움이 됩니다.

### 대화 풀

NPC의 원형이나 스폰 위치에 관계없이 각 NPC는 가져올 수 있는 음성 대사의 '풀'이 정해져 있습니다. 예를 들어, 모든 NPC는 플레이어가 너무 가까이 다가가거나, 총을 겨누거나, 차를 치는 등의 상황에 반응하는 대사가 최소 한두 개씩 있습니다. 이렇게 하면 각 원형에 대해 작성할 대사의 '체크리스트'를 제공함으로써 작가들의 작업이 간소화될 뿐만 아니라 모든 NPC가 플레이어와 제대로 상호작용할 수 있고, 로스 산토스를 돌아다니면서 할 수 있는 주변 대사도 풍부하게 확보할 수 있습니다.

### 모든 것을 하나로 모으다

이러한 모든 시스템을 염두에 두면 Grand Theft Auto V의 NPC 시스템의 기본을 유추할 수 있습니다. 게임에서 NPC가 스폰되면 다음 단계(반드시 순서는 아님)가 실행됩니다:

1.) 이 NPC는 어떤 원형인가?

*   플레이어가 현재 있는 스폰 구역에 따라 특정 유형의 NPC가 다른 유형보다 훨씬 더 많이 스폰될 가능성이 높습니다.
    

2.) 이 NPC의 일반적인 특징은 무엇인가요?

*   나이, 성별, 인종 등
    
*   선택한 원형에 따라 가능한 특성의 범위가 제한될 수 있습니다. 예를 들어, 원형이 LSPD 경찰인 경우 "노인"은 가능한 특성 중 하나가 될 수 없습니다.
    

3.) 선택한 특성 및 원형과 일치하는 대화 풀 에셋을 찾습니다. 이는 선택한 각 속성을 사용하여 특정 폴더를 인덱싱하는 것으로 요약할 수 있습니다(예: "Cop\_남성\_백인\_영"이라는 오디오 자산 폴더 경로를 인덱싱).

[4.) 근처 스폰 지점에서 NPC를 스폰합니다.](https://www.youtube.com/watch?v=ssoVhPB162g)

*   선택한 특성과 일치하는 사람 스킨 메시 에셋을 선택합니다(예: 중년의 백인 여성 에셋).
    
*   NPC의 원형에 따라 올바른 의상을 적용합니다(예: 정장 비즈니스 복장).
    
*   일치하는 대화 풀을 NPC의 대화 로직에 적용합니다.
    

## 자체 NPC 대화 풀 생성하기

![A screenshot from Grand Theft Auto 5, including the player on a yacht taking a photo of Del Perro Beach with their iFruit phone at night, with another boat and the Los Santos skyline in the distance.](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/blt60f8ed0fc302fb8b/66f18fec53eb021675908ebe/GTA5_Del_Perro_Beach.png?width=700&auto=webp&quality=80&disable=upscale "A screenshot from Grand Theft Auto 5, including the player on a yacht taking a photo of Del Perro Beach with their iFruit phone at night, with another boat and the Los Santos skyline in the distance.")

시스템을 이해하고 나면 나만의 NPC 주변 대화를 만드는 것은 간단해집니다. 출처: 락스타 게임즈

이제 앰비언트 다이얼로그 시스템의 핵심이 완성되었으니 이제 실제 다이얼로그를 작성하면 됩니다. 특정 NPC에는 고유한 음성 해설 하위 목록이 있지만(예를 들어, LSPD 경찰은 지원 요청을 위한 특정 대화 녹음 그룹이 있습니다), 기본 풀은 대체로 동일합니다.

이 예제에서는 한가로운 서퍼라는 간단한 NPC 원형을 만들어 보겠습니다. 다음 글머리 기호는 서퍼 앰비언트 오디오 풀 내의 보이스 라인의 각 하위 폴더입니다:

참고: 이 글머리 기호의 프레임워크는 [GTA V 대화 위키의](https://grand-theft-auto-v-dialogue.fandom.com/wiki/Special:AllPages)부지런한 기여자들이 사용한 발판에서 가져온 [것입니다.](https://grand-theft-auto-v-dialogue.fandom.com/wiki/Special:AllPages)

### 기본 대화 대사

다른 사람에게 인사할 때

*   "수프, 브라."
    
*   "잘 지내세요?"
    
*   "서핑 중이야."
    
*   "요!"  
    

기타 주변 대사

*   "오늘 파도가 엄청나네요."
    
*   "내 보드 왁스 봤어, 형? 아니면 내 다른 트렁크에 있던가..."
    
*   "요즘 햇빛이 너무 좋아."
    
*   "사방에 모래가 묻었어, 브라."
    
*   "태닝 스프레이가 더 필요해, 오늘 아침에 마지막 남은 거 다 써버렸어."
    

짜증나면서 말하기

*   "나 좀 내버려둬요. 나 짜증나."
    
*   "꺼져, 형씨!"
    
*   "너 진짜 짜증 나, 브라, 쿨하지 않아."
    

#### 플레이어에게 가려졌을 때

*   "'실례할게요, 친구'"
    
*   "내 흐름을 방해하고 있어, 브로-조."
    
*   "가야겠다, 형, 어서"
    

#### 차량에 충돌했을 때(차량 탑승 중)

*   "형, 뭐야?!"
    
*   "내 웨이브 머신을 망가뜨렸잖아!"
    
*   "수리할 돈이 없어, 브라!"  
    

#### 플레이어를 차에서 끌어낼 때 / 카재킹으로 인한 보복 시

*   "내가 지금 네 파도를 잡을게!"
    
*   "내 차에서 내려, 이 친구야!"
    
*   "어디 한번 보자, 형씨!"
    

#### 걸어가다가 마주쳤을 때

*   "천천히 가, 친구, 해변은 모두에게 충분해."
    
*   "내 기분이 안 좋아, 친구, 조심해."
    

#### 짜증/모욕을 당하거나 싸우는 경우

플레이어가 너무 가까이 서 있을 때

*   "내 햇빛을 가리고 있잖아, 친구."
    
*   "물러서, 브라, 내 선탠이 고르지 않아."
    
*   "넌 날 가리고 있잖아."
    

일반적인 모욕

*   "귀에 바닷물이라도 들어갔어요?"
    
*   "일사병에 걸렸다고 말하는 게 낫겠네요."
    
*   "험악한 분위기의 저를 보고 싶지 않으실 겁니다!"
    
*   "내가 두드릴 건 파도뿐만이 아니야!"
    

#### 화가 난 상태에서 도망치거나 도망쳤을 때

*   "완전히 관이 아니야..."
    
*   "물속에 들어가서 진정해, 친구."
    
*   "그래, 진정해."
    

#### 흥미로운 것을 목격했을 때

*   "브로우!"
    
*   "우와... 대단하네요."
    
*   "굉장해!"
    
*   "말도 안 돼!"
    

#### 무언가에 대해 겁이 날 때

*   "쿨하지 않아, 브라!"
    
*   "그건 쿨하지 않아, 친구!"
    
*   "말도 안 돼, 호세!"
    
*   "말도 안 돼!"
    

#### 총기를 휘두르는 플레이어를 발견했을 때

*   "그냥 파도 좀 맞으며 쉬자, 친구."
    
*   "워! 진정해, 친구!"
    
*   "해변은 네 거야, 친구, 진정해!"
    
*   "농담이야, 친구!"
    
*   "해변의 미녀들을 봐야 하는데 죽을 순 없어!"
    

#### 전화 통화

*   "형! 어디야? 너 없이 아가씨들 찾아다녔는데... 압수당했어? 저게 뭐야?... 바다 바로 옆인데, 소화전 앞에 주차한 건 왜 신경 쓰는데?... 어쨌든, 알아서 해결해."
    
*   "야, 오늘 파도가 심해!...너무 높이 떠서 저 위에서 엄마가 보이는 줄 알았어!...아니, 감옥은 너무 멀었지만 거의 볼 수 있었어...'그래, 여기 도착하면 그냥 연락해."
    
*   "야, 형?...형, 어제 일했는데 왜 오늘도 내가 필요해?...일주일에 5일?! 집세보다 내 이사회가 더 중요해, 이따 봐."
    

## 결론 및 추가 분석(언리얼)

이 GTA V의 보행자 대화 시스템 분석은 내부에서 어떻게 작동하는지에 대한 100% 정확한 다이어그램은 아니지만, 어떻게 구현할 수 있는지에 대한 개략적인 관찰입니다. 이 구현은 유연성, 적응성, 거의 무한대에 가까운 믹스 앤 매치 NPC 생성이 가능하기 때문에 대규모 게임에 적합할 것입니다. 더 좋은 점은 이 구현은 엔진에 구애받지 않으므로 Unreal, Unity 또는 Godot에서 다양한 시스템을 구현할 수 있다는 것입니다.

###### 사이버펑크 2077의 대화 시스템을 구현한 데모 영상

위에서 살펴본 것처럼 저는 다른 게임의 내러티브 시스템을 언리얼로 구현하는 실험을 해본 적이 있습니다. 앞으로의 목표는 비슷합니다. 언리얼 샘플 프로젝트에 록스타의 보행자 대화 시스템을 재현하여 그 메커니즘을 프로그래매틱 수준에서 더 깊이 파고드는 것입니다. 여기에는 무작위 NPC 생성기, 경로와 플레이어 반응을 위한 NPC AI 비헤이비어트리 등 몇 가지 다른 서브시스템이 수반될 수밖에 없습니다. 하지만 저는 이 작업이 재미있고 유익한 도전이 될 것이며, 저나 다른 사람들이 GitHub에 공개하면 본격적인 프로젝트에 활용할 수 있을 것이라고 생각합니다.

[https://randenbanuelosdev.wixsite.com/home](https://randenbanuelosdev.wixsite.com/home )

자세히 읽어보세요:

[블로그추천](https://www.gamedeveloper.com/keyword/blogs)[블로그](https://www.gamedeveloper.com/keyword/featured-blogs)

[](https://www.linkedin.com/sharing/share-offsite/?url=https://www.gamedeveloper.com/design/breaking-down-gta-v-s-pedestrian-dialogue-system-an-analysis-with-speculative-examples)[](https://www.facebook.com/sharer/sharer.php?u=https://www.gamedeveloper.com/design/breaking-down-gta-v-s-pedestrian-dialogue-system-an-analysis-with-speculative-examples)[](https://www.twitter.com/intent/tweet?url=https://www.gamedeveloper.com/design/breaking-down-gta-v-s-pedestrian-dialogue-system-an-analysis-with-speculative-examples)[](https://www.gamedeveloper.com/cdn-cgi/l/email-protection#83bcf0f6e1e9e6e0f7bec1f1e6e2e8eaede4a3e7ecf4eda3c4d7c2a3d5a5a0fbb1b4b8f0a3f3e6e7e6f0f7f1eae2eda3e7eae2efece4f6e6a3f0faf0f7e6eeb9a3c2eda3e2ede2effaf0eaf0a3f4eaf7eba3f0f3e6e0f6efe2f7eaf5e6a3e6fbe2eef3efe6f0a5e2eef3b8e1ece7fabecaa6b1b3f7ebecf6e4ebf7a6b1b3f7ebe6a6b1b3e5ecefefecf4eaede4a6b1b3e5f1eceea6b1b3c4e2eee6a6b1b3c7e6f5e6efecf3e6f1a6b1b3eeeae4ebf7a6b1b3eaedf7e6f1e6f0f7a6b1b3faecf6ada6b3c7a6b3c2a6b3c7a6b3c2a6b1b3c1f1e6e2e8eaede4a6b1b3e7ecf4eda6b1b3c4d7c2a6b1b3d5a5a0fbb1b4b8f0a6b1b3f3e6e7e6f0f7f1eae2eda6b1b3e7eae2efece4f6e6a6b1b3f0faf0f7e6eea6b0c2a6b1b3c2eda6b1b3e2ede2effaf0eaf0a6b1b3f4eaf7eba6b1b3f0f3e6e0f6efe2f7eaf5e6a6b1b3e6fbe2eef3efe6f0a6b3c7a6b3c2ebf7f7f3f0a6b0c2a6b1c5a6b1c5f4f4f4ade4e2eee6e7e6f5e6efecf3e6f1ade0eceea6b1c5e7e6f0eae4eda6b1c5e1f1e6e2e8eaede4aee7ecf4edaee4f7e2aef5aef0aef3e6e7e6f0f7f1eae2edaee7eae2efece4f6e6aef0faf0f7e6eeaee2edaee2ede2effaf0eaf0aef4eaf7ebaef0f3e6e0f6efe2f7eaf5e6aee6fbe2eef3efe6f0)[](https://www.reddit.com/submit?url=https://www.gamedeveloper.com/design/breaking-down-gta-v-s-pedestrian-dialogue-system-an-analysis-with-speculative-examples&title=Breaking%20down%20GTA%20V's%20pedestrian%20dialogue%20system%3A%20An%20analysis%20with%20speculative%20examples)

## 저자 소개

[![Randen Banuelos](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltf854e47803046268/65088a4025eac30e9149356b/Randen_Banuelos.png?width=400&auto=webp&quality=80&disable=upscale "Randen Banuelos")](https://www.gamedeveloper.com/author/randen-banuelos)

[

랜든 바누엘로스

](https://www.gamedeveloper.com/author/randen-banuelos)

Blogger

[란덴 바누엘로스 더보기](https://www.gamedeveloper.com/author/randen-banuelos)

게임 개발자의 일일 뉴스, 개발자 블로그, 스토리를 받은 편지함으로 바로 받아보세요.

[최신 소식 받기](https://gd-resources.gamedeveloper.com/free/w_gamf01/prgm.cgi)

추천 콘텐츠

* * *

원문: [https://www.gamedeveloper.com/design/breaking-down-gta-v-s-pedestrian-dialogue-system-an-analysis-with-speculative-examples](https://www.gamedeveloper.com/design/breaking-down-gta-v-s-pedestrian-dialogue-system-an-analysis-with-speculative-examples)