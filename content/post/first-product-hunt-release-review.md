---
title: '처음으로 Product Hunt에 앱을 출시한 결과는? 1: 앱 개발 전 무슨 일이 있었는가?'
date: 2021-08-14T14:26:16+09:00
draft: false
cover:
  image: '/img/buucket-gif-1.gif'
  alt: 'buucket 구현 영상'
  relative: false
---

블록체인 공부를 시작하고 나니 봐야 할 새로운 정보들이 너무 많았다. 서브레딧 다섯 개 정도, 이메일 뉴스레터 3개, 트위터, 비탈릭을 포함한 여러 블로그 등... 들어가봐야 하는 웹사이트가 왜 이리 많은가? 뭔가 하나라도 안 보면 놓치는 게 생기니 그게 너무 싫었다. 이 모든 피드를 한 곳에 모아 볼 수 있으면 좋지 않을까? 그렇게 본 프로젝트를 시작하게 되었다.

> 제품 첫 버전이 안 부끄럽다면 너무 늦게 출시한거다 - Reid Hoffman

과거 1년간 기술 관련 창업을 하며 크게 느낀 점 하나. 처음부터 "완벽한" 뭔가를 만들려고 하지 말라. (린 스타트업의 MVP!) 그래서 이번 디자인 스프린트는 **최소 기능 제품으로 "이걸 만들면 사람들이 쓸까?에 대한 답을 찾는 것** 만을 목표로 했다. 바로 풀 스택 개발을 시작했다면 남은 25살의 소중한 시간을 거의 다 잡아먹혔겠지.

### 일주일 간 한 것은 아래와 같다

- 서비스 세부 ideation - 어떤 killer 기능이 있는지, 다른 서비스(feedly, inoReader등)와 차이점은 무엇인지, 문제점은 무엇이고 그것의 해결책이 왜 이것인지, 사용자 입장의 benefit은 무엇인지
- UX 디자인과 hi-fi prototyping
- 스토리를 이용한 제품 설명 및 copy 작성
- 랜딩 페이지 개발
- 첫 product hunt 릴리즈 준비와 릴리즈

### 세부적인 결과물들

- 문제점과 해결책 스토리

  - 😓 _문제점_ : 누구든지 관심 있는 분야(취업, 아이돌, 창업, 주식, 재테크 등...)가 있잖아요? 근데 관련된 뉴스나 새로운 일을 계속 찾아보려니까 매일 사이트를 몇 개나 확인해야되고, 이게 너무 불편하더라구요.

  - 😎 _해결책_ : 그래서 매일 보는 피드를 한번에 다 모아 볼 수 있는 앱을 만들어봤어요.

- 제품 기능

  1.  자신이 보는 모든 피드를 한 군데에 모아볼 수 있다. - 기본적인 RSS 기능

  2.  며칠간 안봐도 놓친 것들을 한 페이지로 요약해서 보여준다. - 다른 서비스에는 없는 기능

  3.  잘 보지 않는 채널들을 모아 일주일에 한번씩 솎아낼 수 있다. - 다른 서비스에는 없는 기능

모든 피드를 한 양동이(bucket)에 담아 마실 수 있다는 뜻으로 서비스 이름을 buucket으로 했고, [buucket.io](https://www.buucket.io/) 도메인을 구매해 웨이팅 리스트 랜딩 페이지를 만들었다. 시간을 단축하기 위해 ground up부터 랜딩 페이지를 개발하거나 리액트를 사용하지 않았고, [webflow](https://webflow.com/)를 이용했으며 웨이팅 리스트 구현은 외부 API인 [waitlistAPI](https://getwaitlist.com/)를 연동함으로써 해결했다. 페이지 개발에 총 3시간 정도 소요되었다.

작동 가능한 웹 앱 없이 사람들에게 서비스를 이해시키기 위해서는 높은 퀄리티의 프로토타입이 작동하는 영상 (혹은 GIF)이 필요하다고 판단했다. 여러 디자인 가안들을 만들고 선정한 뒤 피그마로 high fidelity로 와이어프레이밍 했다. 전체 프로토타이핑에 3일 정도가 소요되었으며, product hunt에 들어가는 deliverable (GIF와 설명 사진)을 만드는 데에 추가로 2일이 들었다. _하단 예시 참조_

![buucket.io gif 2](/img/buucket-gif-2.gif)

서비스는 기술적으로 충분히 구현이 가능했다. RSS와 newsletter to RSS 오픈소스 코드등을 이용해 핵심 비즈니스 로직을 만들어낼 수 있을 것이라 판단했으며 내가 풀스택 웹 앱을 구현하고 (mongoDB, expressJS, React, node를 이용) 승민이가 모바일 앱을(React Native 이용) 맡아주기로 했다.

- 선정한 카피
  - Never miss a thing
  - Thousands of feeds, in one place.
  - Browse articles and videos from multiple feeds in one place, so it is far much easier to keep up to date with everything that matters to you.

피그마 프로토타입은 [여기](https://www.figma.com/proto/1dHyvpbL3gEV6ZJ4cpGYbC/buucket?page-id=64%3A310&node-id=93%3A1192&viewport=241%2C48%2C0.19&scaling=scale-down&starting-point-node-id=93%3A1192&show-proto-sidebar=1&hide-ui=1)서 볼 수 있고 (데스크탑으로 봐야한다), 진행한 프로덕트 헌트 캠페인은 [여기](https://www.producthunt.com/posts/buucket)서 볼 수 있다.

_(2편은 이 프로젝트의 결과와 의의, 한계점에 대해 다룬다)_
