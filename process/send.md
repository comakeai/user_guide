---
title: 결재요청 및 서명요청
layout: default
parent: 계약 체결 과정
nav_order: 2
---

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
- TOC
{:toc}
</details>

# 결재요청 및 서명요청

[계약 문서를 업로드하고 저장](/process/create.html)하고 나면, ***요청하기/요청 보냄*** 페이지로 이동합니다. ***요청하기***에서 방금 저장한 항목을 확인할 수 있습니다.  
![](/user_guide/assets/process/send1.png)  
 ***요청하기***는 내가 생성한 ***계약에 대한 액션들***을 수행할 수 있는 영역입니다. 여기에서 [결재요청](#1-결재요청)과 [서명요청](#2-서명요청)을 할 수 있고, 진행중인 계약에 대해 ***결재요청 취소***와 ***서명요청 취소***를 할 수도 있습니다.

{: .note }
상황에 따라서 결재과정을 생략하고 서명요청을 바로 시작할 수 있습니다. 그러나 일단 결재요청을 시작했으면, 결재라인의 모든 승인이 완료가 되어야 서명요청을 시작할 수 있습니다.


## 1. 결재요청

조직에 속한 회원에게만 나타나는 버튼입니다. `결재요청`버튼을 클릭하면 ***결재라인***을 지정할 수 있는 팝업이 나타납니다.  
![](/user_guide/assets/process/send2.png)  
여기서 `결재자 추가`버튼을 클릭하면 검색란이 나옵니다. 결재라인은 ***같은 조직의 구성원***만 지정할 수 있습니다.  
![](/user_guide/assets/process/send3.png)  
요청하길 원하는 구성원의 이름이나 이메일을 적으면 구성원이 자동 검색 됩니다. 결재자는 여러명 지정할 수 있으며, 순서대로 결재요청됩니다. 따라서 적절하게 순서를 정하도록 합니다.  
![](/user_guide/assets/process/send4.png)  



## 2. 서명요청

`서명요청`버튼을 클릭하면 설정한 각 계약 당사자의 서명/입력란에 **누가 서명할 것인지**를 지정하는 팝업이 나타납니다.  
![](/user_guide/assets/process/send5.png)  
다이얼로그에 아래의 항목들을 입력합니다.

이름(필수)
: 요청받는 이의 이름을 입력합니다.  

이메일(필수)
: 요청받는 이의 이메일을 입력합니다. ***비회원에게도 서명요청할 수 있음***으로 계약 상대방에게 코메이크에 회원가입 해달라고 요청할 필요가 없습니다. 코메이크 가입여부와 상관없이 계약 상대방이 받을 수 있는 이메일을 입력하여 서명요청합니다.  

카카오톡 알람(선택)
: 상대방에게 카카오 알람을 사용하려면 카카오 알람 설정을 켜고, 상대방의 전화번호를 입력합니다.  

열람시 암호설정(선택)
: 한층 더 강화된 보안을 위해서 열람시 암호설정을 할 수 있습니다. 요청 받는 이는 고유 링크에 접속하여 약속된 암호를 입력해야만 계약에 접근할 수 있게 됩니다.  

요청 메세지 포함(선택)
: 메세지를 포함해서 요청할 수 있습니다. 이 메세지는 상세타임라인에 나타납니다.  

{: .note}
내부적으로는 입력한 이메일이 회원계정의 이메일인지 자동으로 검사하여, 만약 회원이면 코메이크 시스템의 알람으로도 전송하고, 상대방의 계약 목록에도 추가됩니다. 

{: .important}
***서명 요청시 전달되는 링크***는 아무도 알 수 없고 (요청 하는 이도 알 수 없습니다.), 오직 요청 받는 이에게만 노출된 ***고유의 링크***이며 여기에는 ***임의로 생성된 36글자의 UUID***가 포함됩니다. 따라서 요청 받는 이가 본인의 알람 수단으로 받은 링크를 외부에 공개적으로 노출하지 않는 한 악의적인 의도로 타인이 계약에 접근하는 것이 불가능합니다.



