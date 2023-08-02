# Aiffel
지난 1월, Facebook CEO 마크 저커버그(Mark Zuckerberg)가 <아이언맨>에 등장하는 ‘자비스’와 같은 AI 비서 개발에 도전하겠다는 개인적인 새해 목표를 밝힌 것을 기억하시나요?

저커버그가 1년간의 도전의 결과물인 자비스를 모두에게 소개했습니다.

먼저, 저커버그가 자신의 Facebook 프로필(https://www.facebook.com/zuck)에 업로드한 동영상으로 자비스를 만나 볼까요?


 

저커버그는 자비스 구축 과정에서 배우고 느낀 점을 글로 전하기도 했는데요, 아래에서 간략한 내용을 만나 보실 수 있습니다.

자비스는 어떻게 개발됐는지, 무엇을 할 수 있는지, 그리고 AI에 대해 저커버그는 어떤 생각을 하고 있는지 살펴 보세요. 원문은 해당 링크(https://www.facebook.com/notes/mark-zuckerberg/building-jarvis/10154361492931634)에서 확인하실 수 있습니다.

**‘자비스(Jarvis)’ 구축하기**

2016년 한 해 동안 저는 개인적인 프로젝트를 하나 진행했습니다. 바로 <아이언맨>에 등장하는 ‘자비스’처럼 집안일을 도와 주는 간단한 인공지능(AI)을 구축하는 일인데요.

프로젝트 기간 동안, AI의 놀라운 발전을 직접 경험하는 동시에 아직 갈 길이 멀다는 것 역시 깨달을 수 있었습니다.

‘자비스’는 스마트폰과 컴퓨터를 매개체로 사람의 말을 이해하고 조명∙온도∙가전∙음악∙보안 등 각종 집안 시설을 제어할 수 있습니다. 또한 자비스는 사람의 취향과 습관을 학습할 수 있으며 새로운 단어와 개념을 학습하고, 심지어 아이와 놀아줄 줄도 아는 똑똑한 AI입니다. 자비스 개발에는 자연어 처리, 음성 인식, 얼굴 인식, 강화 학습처럼 다양한 AI 기술과 파이썬, PHP, 오브젝티브-C 등 다양한 프로그래밍 언어가 사용됐습니다.

지금부터 여러분께 자비스를 소개합니다. 그리고 이 프로젝트를 진행하면서 제가 배우고 느낀 점에 대해 말씀드리겠습니다.



자비스 구축을 위해 연결된 시스템 구성

**시작은 집안을 연결하는 것부터**

집안에 있는 시스템을 서로 연결하는 것은 생각보다 복잡했습니다. 시스템들이 각기 다른 프로그래밍 언어와 프로토콜로 이뤄져 있었고, 대부분의 가전제품은 인터넷에 연결조차 돼 있지 않았기 때문입니다.

자비스와 같은 AI 도우미들이 미래에 보다 널리 사용되기 위해서는 더 많은 기기를 서로 연결할 수 있는 공통 API와 같은 표준이 필요하다는 것을 알 수 있었습니다.

**자연어**

다음 단계는 집안 시스템들이 사람의 말을 알아들을 수 있도록 하는 일이었습니다. 우선, 자비스와 사람이 문자로 소통할 수 있는 체계를 만들기로 했습니다. 그 다음, 사람의 목소리를 문자로 변환하고, 자비스가 저에게 하고 싶은 말을 소리로 전달할 수 있는 능력을 추가했습니다.

처음에는 ‘침실’, ‘전등’, ‘스위치 켜줘’와 같은 기본적인 키워드로 시작했습니다. 이 과정에서 자비스에게 ‘화장실’이나 ‘욕실’과 같은 유의어를 학습시킬 필요가 있다는 것을 자연스럽게 터득할 수 있었습니다. AI에게 맥락을 이해시키는 일의 중요성도 깨달았습니다. AI가 사람이 전하고자 하는 맥락을 정확히 이해해야 보다 어려운 열린 질문에도 능숙하게 대처할 수 있기 때문입니다.

**비전인식과 얼굴인식**

AI가 이미지와 동영상에 담긴 정보를 이해하는 과정에는 추적, 사물 인식, 얼굴 인식 등이 매우 중요합니다. 시각 정보를 이해하는 AI 시스템의 활용 가능성은 무궁무진합니다. 일례로, 아기가 낮잠에서 깬 것을 알아채고 음악을 틀어줄 수도 있고, “불 좀 켜줘”라는 명령을 듣고 사람이 어느 방에 있는지 파악해 방의 전등을 켜는 일 등을 들 수 있습니다.



자비스는 현관문 앞 손님의 얼굴을 인식해 누가 방문했는지 알려줍니다.

**메신저 봇**

자비스는 컴퓨터를 기반으로 구축된 AI이지만, 시간과 장소에 대한 제약 없이 자유롭게 대화를 주고받기 위해서는 스마트폰을 활용할 필요가 있었습니다. 이를 위해 Facebook 메신저 봇을 사용했고요. Facebook 메신저 플랫폼이 제공하는 봇 프레임워크를 활용하면 별도의 앱을 구축하는 것보다 훨씬 적은 시간과 노력으로도 목적에 부합하는 메신저 봇을 개발할 수 있기 때문입니다.

이를 통해, 언제 어디서든 자비스와 대화를 주고받을 수 있게 됐습니다. 스마트폰을 통해 자비스 봇에게 메시지를 보내면, 메시지는 즉각 자비스 서버로 전송됩니다. 자비스 봇에게 음성 메시지를 보내는 것도 가능합니다. 음성 메시지는 서버에서 문자로 변환된 후 문자 메시지와 같은 방식으로 처리됩니다.

자비스를 이용하면서 놀라웠던 점은, 문자와 음성을 모두 사용할 수 있는 상황에서 문자를 선택하게 되는 경우가 생각보다 많다는 사실이었습니다. 여기에는 많은 이유가 있겠지만, 내 주변 사람들에게 불편을 끼치지 않고도 문자로 원하는 바를 전달할 수 있다는 점이 크게 작용한다고 생각합니다. 자비스로부터 메시지를 받을 때에도 텍스트로 전달받는 방식이 편했습니다. 음성에 비해 문자는 내가 원할 때 읽을 수 있다는 점에서 편리하기 때문입니다.



메신저 봇 덕분에 언제 어디서든 자비스에게 메시지 보내기

**음성 인식**

AI와 사람 사이의 의사소통에 있어 문자가 중요한 부분을 차지할 것이 예측되지만, 음성 역시 매우 중요한 역할을 담당하리라 생각합니다. 음성은 편리하고 신속하기 때문입니다.

저는 자비스가 음성을 인식할 수 있도록 전용 iOS 앱을 개발했습니다. 외출 중에도 스마트폰으로 자비스에게 말을 걸어야 하는 상황이 자주 있었기 때문이죠. 항상 음성을 인식할 준비가 돼 있는 앱 덕분에 언제나 자비스에게 말을 걸 수 있습니다. 해당 앱은 곧 안드로이드 버전으로도 개발할 계획입니다.

눈부신 발전에도 불구하고 AI가 음성 인식으로 사람들의 일상적인 대화를 이해하는 데는 아직 부족한 점이 많습니다. 새로이 음성 인식을 적용할 수 있는 분야도 무궁무진합니다. AI와 음성 인식 기술은 꾸준히 앞을 향해 나아가고 있으며, 몇 년 후에는 더욱 발전된 모습을 보여주리라 기대합니다.



자비스를 위한 iOS 앱 음성 인식 기능

**다음 단계는?**

올해의 도전은 여기서 마칩니다만, 앞으로도 매일같이 자비스를 사용하고 꾸준히 발전시킬 계획입니다.

단기 목표로는 안드로이드 앱 개발을 꼽을 수 있겠고, 이와 더불어 더 많은 방에 자비스 음성 단말기를 설치할 계획입니다. 아울러 더 많은 가전기기를 서로 연결하는 것도 빼놓을 수 없겠죠. 장기적으로는 자비스에게 자가 학습 능력을 가질 수 있도록 개발을 진행하고자 합니다. 물론, 자비스를 세상의 많은 사람들에게 선보일 방법을 찾는 것 역시 중요하고 재미있는 과제가 될 것입니다.

**결론**

이번 프로젝트는 무척이나 흥미로운 지적 도전 그 자체였습니다. 미래를 위한 AI 도구를 직접 구축해 보는 직접적인 경험을 할 수 있는 계기이기도 했고요.

이번 도전을 지켜보고 함께해 주신 여러분께 감사의 인사를 전합니다. 몇 주 안으로 2017년을 위한 제 새로운 도전에 대해 말씀드릴 계획이니 응원을 부탁드립니다.

 

아래는 저커버그 아내 입장에서 만나본 자비스 영상입니다. 부록 정도 되겠네요.
---
주커버그가 이런 새해 목표를 발표 한것에 대해서 모르고 있었는데 알게 되어서 좋았고 여러 빅테크 기업들이 인공지능 개발 경쟁이 재밌게 흘러가는거 같고 열심히 노력해서 나도 인공지능 개발 경쟁에 참여 할 수 있는 역량을 가지고 싶다.


