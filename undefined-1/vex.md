---
description: CVE가 발견된 컴포넌트에 VEX를 설정할 수 있습니다.
---

# VEX 기능

#### 1. VEX(Vulnerability Exploitability eXchange)란?

VEX는 소프트웨어에 포함된 오픈소스 라이브러리 등에서 알려진 취약점(CVE)이 발견되었을 때, **해당 취약점이 실제 우리 제품/서비스 환경에서 실제로 악용(영향)될 수 있는지**에 대한 분석 결과와 상태를 명시하는 표준 보안 명세입니다.

* 취약점이 존재하는 버전의 라이브러리를 쓰더라도, 실제 해당 취약 코드나 함수를 호출하지 않거나 방어 로직이 적용되어 있으면 실제로는 영향이 없을 수 있습니다.
* VEX를 통해 이러한 실제 악용 가능성 여부(영향도)를 체계적으로 분류하고 관리할 수 있습니다.

<table><thead><tr><th width="145.75">메뉴 구분</th><th>화면/메뉴 위치</th><th>VEX 설정 가능 조건 및 동작</th></tr></thead><tbody><tr><td>프로젝트 </td><td><ol><li>프로젝트 <strong>Clarity, FossID, ClarityAIR</strong> 검증도구 상세 화면 하단의 COMPONENT LIST</li><li>SECURITY 항목에 아이콘 클</li></ol></td><td><p>검증 워크플로우 </p><ul><li><strong>진행 중</strong>: CVE 세부 정보 조회만 가능 </li><li> <strong>완료(Ready)</strong>: VEX 설정 패널(REVIEW) 활성화 및 편집 가능</li></ul></td></tr><tr><td>프로젝트 내 > SBOM Import</td><td><ol><li>프로젝트 내에 SBOM Import 상세 화면</li><li>SECURITY 항목에 아이콘 클</li></ol></td><td><p>워크플로우 </p><ul><li><strong>검토 중</strong>: CVE 세부 정보 조회만 가능 </li><li> <strong>완료(Ready)</strong>: VEX 설정 패널(REVIEW) 활성화 및 편집 가능</li></ul></td></tr><tr><td>SBOM 리포트</td><td><ol><li>SBOM 리포트 상세 화면</li><li>SECURITY 항목에 아이콘 클</li></ol></td><td>• 생성된 리포트 내 컴포넌트별 CVE 취약점에 대해 VEX 설정 가능</td></tr><tr><td>제품 관리</td><td><ol><li>[병합 보기], [병합된그룹컴포넌트] 버튼 클릭</li><li>프로덕트에 병합된 컴포넌트 화면</li><li>SECURITY 항목에 아이콘 클</li></ol></td><td><ul><li>프로덕트에 병합된 컴포넌트에 CVE 취약점에 대한 VEX 설정 가</li></ul></td></tr><tr><td>SBOM 병합 상세</td><td><ol><li>SBOM 병합 상세 화면</li><li>SECURITY 항목에 아이콘 클</li></ol></td><td></td></tr></tbody></table>

<figure><img src="../.gitbook/assets/image (237).png" alt=""><figcaption></figcaption></figure>

