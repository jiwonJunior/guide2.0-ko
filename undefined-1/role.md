---
description: >-
  System > Role 메뉴에서 사용자 역할을 생성 및 관리할 수 있습니다. 생성된 역할은 System > User 메뉴에서 사용자에게
  부여할 수 있습니다. 또한, SUPERUSER 계정만 사용자 역할을 관리할 수 있습니다.
---

# 사용자 역할(Role) 관리

### 1. Role 등록

* \[Add Role] 버튼을 클릭하여 새로운 역할을 생성합니다.

<figure><img src="../.gitbook/assets/image (151).png" alt=""><figcaption></figcaption></figure>



* 빨간색으로 표시된 필수 값 역할 이름을  입력하고, 8개 권한 중에 사용할 권한을 선택합니다. \[Add Role] 버튼을 클릭하여 역할(Role) 생성을 완료합니다.

<div align="left"><figure><img src="../.gitbook/assets/image (201).png" alt="" width="283"><figcaption></figcaption></figure></div>

<mark style="color:$primary;">**시스템 권한 설명 (Role & Permission)**</mark>

1. **Manager** (시스템 관리자)

* 설명: 시스템의 모든 프로젝트를 관리하고, 정책 관리와 프로덕트 생성과 본인을 프로덕트 담당자로 지정합니다.
* 주요 기능: 전체 프로젝트 관리, 프로덕트 생성 및 프로덕트 매니저 권한, 시스템 정책 관리, SBOM 포맷 관리



2. **Product Creator** (프로덕트 생성자)

* 설명: 시스템 내에서 최상위 개념인 프로덕트를 신규 생성할 수 있는 권한입니다.
* 주요 기능: _**프로덕트 생성**_ 및 _**프로덕트 관리자**_ 지정 및 프로덕트 복제.



3. **Product Manager** (프로덕트 관리자)

* 설명: 할당된 프로덕트를 전반적인 운영하는 담당자 권한입니다.
* 주요 기능: 신규 프로젝트 생성 후, _**프로젝트 관리자**_ 지정.  프로덕트 그룹 관리



4. **Project Manager** (프로젝트 관리자)

* 설명: 할당된 프로젝트를 독립적으로 관리하고 프로젝트 멤버를 관리하는 프로젝트 관리자 권한입니다.
* 주요 기능: 프로젝트 검증 워크플로우 독립적으로 진행. 프로젝트 내부 멤버 관리&#x20;



5. **Developer** (일반 사용자)

* 설명: 할당된 프로젝트와 데이터를 확인하는 일반 사용자 권한입니다.
* 주요 기능: 할당된 프로젝트에서 신규 검증 생성하고, **Project Manager**와 함께 검증 워크플로우 함께 진행합니다.



<mark style="color:$primary;">**정책 및 SBOM 포맷 관리 권한 설명**</mark>

1. **License Policy Edit** (라이선스 정책 관리 권한)

* 설명: 시스템의 라이선스 정책을 설정하고 새로운 라이선스 정책을 생성하고 변경하는 권한입니다.
* 주요 기능: 기본 정책 설정 및 새 정책 추가 및 수정 삭제



2. **SBOM Edit** (SBOM 포맷 관리 권한)

* 설명: SBOM 포맷을 추가, 수정, 삭제할 수 있는 SBOM 관리 권한입니다.
* 주요 기능: SBOM 추가 및 수정 삭제



3. **Vulnerability Policy Edit** (취약점 정책 관리 권한)

* 설명: 시스템 내에서 감지되는 보안 취약점(CVE 등)의 대응 정책과 위험도 기준을 관리하는 권한입니다.
* 주요 기능: 취약점 위험 등급 별 차단/허용 정책 수정, 보안 예외 처리 규칙 편집.



***

### 2. Role 편집/ 삭제

ACTION에 아이콘을 클릭해서, 편집 또는 삭제할 수 있습니다.

<figure><img src="../.gitbook/assets/image (41).png" alt=""><figcaption></figcaption></figure>







