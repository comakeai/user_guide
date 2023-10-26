---
layout: default
title: OPEN API 제공
nav_order: 7
permalink: /docs/openapi
---


<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
- TOC
{:toc}
</details>

# OPEN API 제공
코메이크는 각 기업이 내부 시스템 안에서 전자계약시스템을 이용하실 수 있도록, OPEN API를 제공합니다. api의 사용 도메인은 https://comake.ai/api 입니다. 각 api 상세는 [https://comake.ai/api-doc](https://comake.ai/api-doc){:target="_blank"}에서 확인하실 수 있습니다.

## OPEN API 사용 방법
###  API KEY와 SECRET을 발급
OPEN API를 사용하고자 하는 기업은 코메이크의 관리자에게 OPEN API 사용 승인 절차를 거친 후, 해당 기업 고유의 API KEY와 SECRET을 발급받습니다.

### 관리자 로그인 :
발급받은 API KEY를 Authorization Bearer의 토큰으로 사용하여 코메이크 시스템에 관리자 로그인 API를 호출하고 adminToken 을 발급받습니다. 이 토큰은 JWT 웹표준 토큰입니다. 
(정확한 로그인 방법은 [API 상세문서](https://comake.ai/api-doc){:target="_blank"} 의 admin 카테고리의 /bussiness/login-admin api 설명을 보세요.)

### 사용자 등록 :
관리자 로그인을 통해 발급받은 adminToken을 Authorization Bearer의 토큰으로 사용하여 코메이크를 이용할 사용자를 코메이크에 등록합니다. 
(정확한 사용자 등록 방법은  [API 상세문서](https://comake.ai/api-doc){:target="_blank"} 의 admin 카테고리의 /bussiness/register-client api 설명을 보세요.)

### 사용자 로그인 :
사용자가 전자계약관련 기능을 이용할 때, 기업의 내부 시스템은 사용자 로그인 API를 이용하여 코메이크에 사용자 로그인을 먼저 해야합니다. 관리자 로그인을 통해 발급받은 adminToken을 Authorization Bearer의 토큰으로 사용하여 사용자 로그인을 하여 사용자의 clientToken을 발급받습니다. 이 토큰은 JWT 웹표준 토큰입니다. 토큰의 만료시간은 1시간이라 시간이 초과하면 다시 로그인하여 새로운 clientToken을 발급받아야합니다. 
(정확한 사용자 등록 방법은  [API 상세문서](https://comake.ai/api-doc){:target="_blank"} 의 admin 카테고리의 /bussiness/login-client api 설명을 보세요.)


### 계약 생성 및 서명란 설정 :
PDF 문서에 서명란을 드래그앤 드롭으로 지정하는 것은 기업 내부에서 API 만으로 개발하기 어려운 기능이므로, 코메이크는 OPEN API 사용 기업을 위한 해당화면을 별도로 제공합니다. 
별도 제공 화면에서는 계약서 업로드 -> 서명란 설정 -> 계약 이름 저장이 순서대로 이루어집니다.

기업에서는 사용자가 신규계약 생성할 때 해당 url로 웹브라우저를 띄우면 됩니다. 
이 url은 [https://comake.ai/contract/upload?token=${clientToken}](https://comake.ai/contract/upload?token=${clientToken}){:target="_blank"}  입니다. 
계약을 생성하기를 원하는 사용자의 로그인 후 발급받은 clientToken을 함께 넘겨줍니다. 

### 계약 변경
계약의 업로드한 문서, 설정한 서명란 등을 변경하기 위한 별도의 화면을 제공합니다. 
url은 [https://comake.ai/contract/upload?token=${clientToken}&contractId=${contract._id}](https://comake.ai/contract/upload?token=${clientToken}&contractId=${contract._id}){:target="_blank"} 입니다. contract._id는 계약목록 들어있는 field입니다. 

### 계약 목록 관리 - 목록 가져오기, 계약 삭제, 상세정보 :
계약 목록을 가져오고, 계약을 삭제하고, 변경하고, 계약의 상세정보를 보는 API를 제공합니다. 
(정확한 api 이용 방법은  [API 상세문서](https://comake.ai/api-doc){:target="_blank"} 의 contractbox 카테고리의 api 리스트를 보세요.)

### 서명 요청 받는 이의 정보 저장 :
서명요청을 보내기전에, 서명요청을 받을 서명자의 정보를 세팅합니다. Authorization Bearer의 토큰으로 해당 사용자의 clientToken을 사용합니다.
(정확한 api 이용 방법은  [API 상세문서](https://comake.ai/api-doc){:target="_blank"} 의 contract contract/pre-signee-set 을 보세요.)

### 서명요청 :
서명 요청 받는 이의 정보를 저장했으면 이제 서명요청 할 수 있습니다. Authorization Bearer의 토큰으로 해당 사용자의 clientToken을 사용합니다. 
(정확한 api 이용 방법은  [API 상세문서](https://comake.ai/api-doc){:target="_blank"} 의 contract contract/request-sign 을 보세요.)

### 서명 요청 취소:
서명 요청을 보낸후 취소하는 API 를 젲공합니다.. Authorization Bearer의 토큰으로 해당 사용자의 clientToken을 사용합니다. 
(정확한 api 이용 방법은  [API 상세문서](https://comake.ai/api-doc){:target="_blank"} 의 contract contract/cancel-sign 을 보세요.)
