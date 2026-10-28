---
description: 컴포넌트에서 발견된 CVE에 대한 VEX를 설정할 수 있습니다.
---

# VEX 기능

#### 1. VEX(Vulnerability Exploitability eXchange)란?

VEX는 소프트웨어에 포함된 오픈소스 라이브러리 등에서 알려진 취약점(CVE)이 발견되었을 때, **해당 취약점이 실제 우리 제품/서비스 환경에서 실제로 악용(영향)될 수 있는지**에 대한 분석 결과와 상태를 명시하는 표준 보안 명세입니다.

* 취약점이 존재하는 버전의 라이브러리를 쓰더라도, 실제 해당 취약 코드나 함수를 호출하지 않거나 방어 로직이 적용되어 있으면 실제로는 영향이 없을 수 있습니다.
* VEX를 통해 이러한 실제 악용 가능성 여부(영향도)를 체계적으로 분류하고 관리할 수 있습니다.



#### 2. VEX 설정 가능 화면

<table><thead><tr><th width="145.75">메뉴 구분</th><th>화면/메뉴 위치</th><th>VEX 설정 가능 조건 및 동작</th></tr></thead><tbody><tr><td>프로젝트 </td><td><ol><li>프로젝트 <strong>Clarity, FossID, ClarityAIR</strong> 검증도구 상세 화면 하단의 COMPONENT LIST</li><li>SECURITY 항목에 아이콘 클</li></ol></td><td><p>검증 워크플로우 </p><ul><li><strong>진행 중</strong>: CVE 세부 정보 조회만 가능 </li><li> <strong>완료(Ready)</strong>: VEX 설정 패널(REVIEW) 활성화 및 편집 가능</li></ul></td></tr><tr><td>프로젝트 내 > SBOM Import</td><td><ol><li>프로젝트 내에 SBOM Import 상세 화면</li><li>SECURITY 항목에 아이콘 클</li></ol></td><td><p>워크플로우 </p><ul><li><strong>검토 중</strong>: CVE 세부 정보 조회만 가능 </li><li> <strong>완료(Ready)</strong>: VEX 설정 패널(REVIEW) 활성화 및 편집 가능</li></ul></td></tr><tr><td>SBOM 리포트</td><td><ol><li>SBOM 리포트 상세 화면</li><li>SECURITY 항목에 아이콘 클</li></ol></td><td><ul><li>생성된 리포트 내 컴포넌트별 CVE에 대해 VEX 설정 가능</li></ul></td></tr><tr><td>제품 관리</td><td><ol><li>[병합 보기], [병합된그룹컴포넌트] 버튼 클릭</li><li>프로덕트에 병합된 컴포넌트 화면</li><li>SECURITY 항목에 아이콘 클</li></ol></td><td><ul><li>프로덕트에 병합된 컴포넌트에 CVE 에 대한 VEX 설정 가능</li></ul></td></tr><tr><td>SBOM 병합 상세</td><td><ol><li>SBOM 병합 상세 화면</li><li>SECURITY 항목에 아이콘 클</li></ol></td><td><ul><li>병합된 SBOM CVE에 대한 VEX 설정 가능</li></ul></td></tr></tbody></table>



#### 3. VEX 설정 방법

a. [**2. VEX 설정 가능 화면**](vex.md#id-2.-vex) 위치로 이동하여 **SECURITY 항목**의 아이콘을 클릭합니다.

<div align="left"><figure><img src="../.gitbook/assets/image (237).png" alt="" width="563"><figcaption></figcaption></figure></div>





b. VEX 설정 패널(REVIEW) 활성화되면 설정 및 편집 가능합니다.&#x20;

* **기본값 (Default)**: Affected (영향 있음)
  * CVE 탐지 시 기본적으로 실제 영향이 있는 상태(Affected)로 지정됩니다.
* **상태 옵션**
  * Affected: 현재 환경에서 실제 보안 영향이 있어 조치(패치, 설정 변경 등)가 필요한 경우
  * Not Affected: 취약한 컴포넌트가 포함되어 있으나, 호출 경로 부재/자체 방어 로직 등으로 인해 실제 악용될 위험이 없는 경우
  * Fixed: 패치나 버전 업그레이드 등을 통해 조치가 완료된 경우
  * Under Investigation: 영향도 분석이 아직 진행 중인 경우

<figure><img src="../.gitbook/assets/image (240).png" alt=""><figcaption></figcaption></figure>



c. **Not Affected(영향 없음)** 설정 시 필수 작성 기준

상태를 Not Affected로 변경할 때는 명확한 근거를 반드시 입력해야 합니다.

* Justification (필수 선택):
  * 영향이 없다고 판단한 표준 사유(예: 취약 코드 미실행, 실행 경로 없음, 인라인 완화 조치 적용 등)를 드롭다운 목록에서 필수로 선택합니다.
* Additional Notes (상세 코멘트):
  * 내부 분석 결과, 미호출 근거, 방어 로직 적용 내역 등 구체적인 설명과 검토 의견을 상세히 작성합니다.

<div align="left"><figure><img src="../.gitbook/assets/image (238).png" alt="" width="563"><figcaption></figcaption></figure></div>



#### 4. 이전 프로젝트 차수의 VEX 설정 가져오기&#x20;

* 이전에 완료된 검증 버전의 VEX 검토 내역(Status, Justification 등)을 현재 검증으로 불러와 동일한 컴포넌트 및 CVE에 일괄 적용할 수 있습니다. **\[Import Data from Previous Version]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (241).png" alt=""><figcaption></figcaption></figure>



* VEX 데이터를 가지고 올 프로젝트 차수를 선택합니다.

<figure><img src="../.gitbook/assets/image (242).png" alt=""><figcaption></figcaption></figure>



* 주의 사항을 확인한 뒤 **\[Import]** 버튼을  클릭하여 데이터 가지고 옵니다.

<figure><img src="../.gitbook/assets/image (243).png" alt=""><figcaption></figcaption></figure>



* 데이터 가져오기(Import)가 성공적으로 완료되면 **화면 우측 상단에 알림이 표시**됩니다.

<figure><img src="../.gitbook/assets/image (245).png" alt=""><figcaption></figcaption></figure>



#### 5. SBOM 내보내기 시 VEX 정보 포함 (Export SBOM)

* 생성된 SBOM 파일을 내보낼 때, 검토 완료된 VEX(취약점 영향도 분석 결과) 정보를 파일에 함께 포함하여 추출할 수 있습니다.



* **설정 옵션 설명:**
  * Export Type: 내보낼 규격을 선택합니다 (예: SPDX3.0 CycloneDX 1.6 등).
  * Format: 파일 형식을 선택합니다 (JSON, XML,RDF, Excel 등).
  * VEX (Include VEX information):
    * 체크박스를 선택(체크)하면 설정된 VEX 분석 정보(영향 상태 Status, 사유 Justification, 상세 메모 Notes 등)가 SBOM 메타데이터에 함께 포함되어 내보내집니다.

<div align="left"><figure><img src="../.gitbook/assets/image (246).png" alt=""><figcaption></figcaption></figure></div>
