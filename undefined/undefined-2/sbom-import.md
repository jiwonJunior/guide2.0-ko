---
description: SBOM Import하는 방법을 설명합니다.
---

# SBOM Import 방법

#### 1. SBOM Import 기능 개요

* SBOM Import는 **2단계 워크플로우**로 진행됩니다.
* 개발자는 관리자 함께 진행할 수 있습니다.
* 관리자가 진행합니다.
* 검증 흐름: _스캔 → Review → 완료_
* 워크플로우 바에서 현재 단계 확인할 수 있습니다.



#### 2. SBOM 파일 스캔하기

\[SBOM Verification] 클릭해서 검증할 파일을 선택합니다.

<div align="left"><figure><img src="../../.gitbook/assets/image (124).png" alt=""><figcaption></figcaption></figure></div>



* Import할 SBOM 파일과 포맷을 선택합니다.
* SBOM 파일은 JSON 형식만 지원합니다.
* &#x20;SPDX 3.0, CycloneDX 1.6, System Default SBOM 포맷을 선택할 수 있습니다. SBOM 관리에서 포맷을 추가하면 목록에 같이 표시됩니다. ([SBOM 포맷 관리 방법 참고](../../undefined-1/sbom-1.md))

<div align="left"><figure><img src="../../.gitbook/assets/image (125).png" alt="" width="446"><figcaption></figcaption></figure></div>

#### 3. SBOM 상세 화면 설명

* Clarity 검증 화면은 크게 다음 3개의 영역으로 구성됩니다.

#### (1). 프로젝트 메타정보

* 프로젝트 이름, 버전, 검증 도구, 요청자, 요청일, 실제 파일 이름,  스캔 유형, 부서, 수정일, 재 검증 기한 \
  해당 프로젝트의 주요 정보를 확인할 수 있는 영역입니다.

#### (2). SBOM 워크플로우

* SBOM 워크플로우는 총 2단계로 진행되며, 화면에서 현재 진행 상태를 확인할 수 있습니다. 개발자는 관리와 함께 단계를 진행할 수 있으며, 관리자는 모든 단계를 진행할 수 있습니다.

#### (3). 커뮤니케이션 기능(Communication)

* SBOM 워크플로우 과정 중 개발자와 관리자가 커뮤니케이션 할 수 있습니다.
  * **Comments**: 검증 단계 별로 개발자 및 관리자가 남긴 코멘트를 확인하고 의견을 교환할 수 있습니다.

<div align="left"><figure><img src="../../.gitbook/assets/clarity_section_yellow_4 (1).png" alt=""><figcaption></figcaption></figure></div>

#### (4). 스캔된 컴포넌트 리스트(Component List)

**항목 설명**

* <mark style="background-color:yellow;">CONFLICT: 컴포넌트가 라이선스 정책 해당하면 빨간색으로 표시가 되고, 충돌이 없을 시 흰색으로 표시.</mark>
* COMPONENT (COMPONENT VERSION) : 컴포넌트 이름과 컴포넌트 버전 정보.
* COMPONENT LICENSE: 컴포넌트에 대한 라이선스 정보
* OBLIGATION TYPE:  라이선스에 대한 의무  유형 정보(프로젝트 라이선스 정책에 따른 정보)
* USAGE TYPE : 기본 값 해당 없음(N/A)이며, 결합 형태 입력 단계에서 지정할 수 있습니다.
* DISCLOSE:  컴포넌트  공개 여부
* MODIFICATION: 컴포넌트  수정 여부
* NOTICE: 컴포넌트 고지 여부
* PATENT: 컴포넌트 특허 여부
* VULNERABLE LEVEL: 컴포넌트에서 발견된 보안 취약점의 위험도를 보안 취약점 정책에 따른 코드로 표시합니다.
* SEVERITY: CVSS 점수를 기준으로 취약점의 위험도를 등급입니다.
* SECURITY: 해당 컴포넌트에서 발견된 CVE(보안 취약점) 목록을 표시합니다.

***

<figure><img src="../../.gitbook/assets/컴포넌트　목록 (1).png" alt=""><figcaption></figcaption></figure>



**팝업 설명**

* 1번 항목 클릭 시, 해당 컴포넌트에 적용되는 _라이선스 정책_  정보가 표시됩니다.&#x20;
  * 정책 단계&#x20;
  * 승인 여부
  * 조건(속성) 상세 정보

<div align="left"><figure><img src="../../.gitbook/assets/image (77).png" alt="" width="344"><figcaption></figcaption></figure></div>



* 2번 항목 클릭 시, 컴포넌트 간 라이선스 충돌 정보가 표시됩니다.&#x20;

<div align="left"><figure><img src="../../.gitbook/assets/image (78).png" alt="" width="429"><figcaption></figcaption></figure></div>



* 3번 항목 클릭 시, _컴포넌트 이&#xB984;_&#xACFC; _컴포넌트 버&#xC804;_&#xC5D0; 해당하는 컴포넌트 정보를 보여줍니다. DB에 없으면 표시하지 않습니다.

<div align="left"><figure><img src="../../.gitbook/assets/image (79).png" alt="" width="324"><figcaption></figcaption></figure></div>



* 4번 항목 클릭 시,  해당 라이선스 상세 정보가 표시됩니다. DB에 없으면 표시하지 않습니다.

<div align="left"><figure><img src="../../.gitbook/assets/image (81).png" alt="" width="326"><figcaption></figcaption></figure></div>



* 5번 항목 클릭 시,  해당 컴포넌트에 적용되는 라이선스 정책 의무 유형(Obligation Type)에 대한  이행 사항을  표시합니다.

<div align="left"><figure><img src="../../.gitbook/assets/image (82).png" alt="" width="396"><figcaption></figcaption></figure></div>



* 6번 항목 클릭 시, 보안취약점 등급 코드에 대한 이행 사항을 표시합니다.

<div align="left"><figure><img src="../../.gitbook/assets/image (84).png" alt="" width="416"><figcaption></figcaption></figure></div>



* 7번 항목 클릭 시, 해당 컴포넌트에서 발견된 CVE 목록이 표시되며, 각 CVE를 클릭하면 NVD의 상세 페이지로 이동합니다.

<div align="left"><figure><img src="../../.gitbook/assets/image (86).png" alt=""><figcaption></figcaption></figure></div>





### 4. SBOM 워크플로우 상세 설명

2단계를 각 단계 별로 설명하겠습니다.

{% stepper %}
{% step %}
**Step1 - Review**

* 개발자는 읽고 싶은 SBOM 파일을 업로드할 수 있습니다.
* 관리자는 재검증 또는 완료 처리를 할 수 있습니다.

<figure><img src="../../.gitbook/assets/image (142).png" alt=""><figcaption></figcaption></figure>

* SBOM Result에서 누락된 SBOM 항목과 지원하지 않는 SBOM 항목 확인할 수 있습니다.

<figure><img src="../../.gitbook/assets/image (144).png" alt=""><figcaption></figcaption></figure>


{% endstep %}

{% step %}
**Step2 - Ready**

* 관리자는 검증 해제할 수 있습니다.
* 개발자, 관리자 모두 Clarity 검증 결과와 Import SBOM 결과를 비교할 수 있습니다.

<figure><img src="../../.gitbook/assets/image (147).png" alt=""><figcaption></figcaption></figure>



* \[Compare with Clarity Verif.] 버튼 클릭해서 아래의 팝업 창에서 비교할 Clarity 검증을 선택합니다.

<figure><img src="../../.gitbook/assets/image (148).png" alt=""><figcaption></figcaption></figure>



* 선택한 _**Clarity 검증**_&#xACFC; _**Import한 SBOM**_ 결과를 비교한 결과를 볼 수 있습니다.

<figure><img src="../../.gitbook/assets/image (150).png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}









