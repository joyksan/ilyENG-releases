# ilyENG FolderMap (v1.2)

<div align="center">

[![macOS Version](https://img.shields.io/badge/macOS-11.0%2B-000000?style=flat-square&logo=apple&logoColor=white)](https://github.com/joyksan/ilyENG-releases)
[![Architecture](https://img.shields.io/badge/Arch-Apple%20Silicon%20%7C%20Intel-0284c7?style=flat-square)](https://github.com/joyksan/ilyENG-releases)
[![Runtime](https://img.shields.io/badge/Runtime-macOS%20Native-10b981?style=flat-square)](https://github.com/joyksan/ilyENG-releases)
[![Privacy](https://img.shields.io/badge/Privacy-Local%20Only-6366f1?style=flat-square)](https://github.com/joyksan/ilyENG-releases)
[![Release](https://img.shields.io/badge/Release-v1.2.0-ec4899?style=flat-square)](https://github.com/joyksan/ilyENG-releases/releases)

<br/>

**학원 교재 폴더 구조 분석 및 파일 정리 도구**  
*iCloud Drive 상태를 검사하고, 중복 파일 식별과 되돌리기(Undo)를 지원합니다.*

</div>

---

## 다운로드 (v1.2)

<div align="center">

### [ilyENG FolderMap 설치 패키지 다운로드 (.pkg)](https://github.com/joyksan/ilyENG-releases/raw/refs/heads/main/ilyENG_FolderMap_Installer.pkg)

*패키지 용량: 약 2.7 MB · Apple Silicon 및 Intel Mac 지원 · 관리자 권한 불필요*

</div>

> [!NOTE]
> **macOS 최초 실행 시 확인 안내**  
> 공인 개발자 인증서 미포함 빌드의 경우 최초 실행 시 보안 확인 안내가 표시될 수 있습니다. ilyENG는 외부 네트워크 통신 없이 로컬에서만 동작합니다.
>
> - **시스템 설정에서 열기**: Mac **시스템 설정 > 개인정보 보호 및 보안** 하단의 **[확인 없이 열기]** 클릭  
>   *(또는 Finder에서 설치 패키지를 **우클릭(Control + 클릭) > 열기** 선택)*
> - **터미널 명령어**:
>
>   ```bash
>   xattr -c ~/Downloads/ilyENG_FolderMap_Installer.pkg && open ~/Downloads/ilyENG_FolderMap_Installer.pkg
>   ```

---

## v1.2 변경 사항

- **통합 검색**  
  한글 자모·초성 검색, 연도(올해/작년) 인식, 파일명·경로 우선순위를 반영한 실시간 검색을 지원합니다.
- **다중 필터 및 교재 분포표**  
  확장자, 파일 크기, 대상 학년(중1~고3)을 함께 걸러 볼 수 있고, 학년 × 교재 유형 표로 교재 분포를 한눈에 확인할 수 있습니다.
- **사본 파일 탐지**  
  파일명 끝의 `(1)`, `사본`, `복사본` 같은 표시를 인식해 같은 파일끼리 묶어 주고, 정보 패널에서 비교한 뒤 정리 대상을 고를 수 있습니다.
- **Spotlight 본문 검색**  
  파일명 검색 외에 macOS Spotlight 색인을 활용하여 PDF 및 문서 파일 내부 텍스트를 검색하는 모드를 지원합니다.
- **Claude 진단 탭**  
  Claude와의 대화에서 전달된 진단 및 정리 제안서를 앱 안의 전용 탭에서 확인하고 승인할 수 있습니다.
- **iCloud 다중 기기 경로 및 충돌 방지**  
  작업 폴더를 기준으로 상대경로를 기록해 기기마다 사용자 경로가 달라도 복원할 수 있으며, 동시에 적용되지 않도록 잠금을 겁니다.
- **대상 폴더 범위 보호 (2026-11-05)**  
  iCloud Drive 전체가 아닌 선택한 작업 폴더만 다루도록 범위를 고정합니다. iCloud Drive 최상위 폴더가 자동으로 선택·저장되지 않으며, 다른 폴더에서 만든 계획이나 되돌리기 기록은 실행되지 않습니다.

<details>
<summary><b>v1.1 변경 사항 접기/펼치기</b></summary>

- Finder 드래그 앤 드롭 폴더 로드 지원
- macOS Quick Look 미리보기 (`Spacebar`) 지원
- Finder 키보드 내비게이션 지원 (`Return`: 이름 변경, `⌘↓`/`⌘O`: 열기, `⌘↑`: 상위 폴더)
- 실행 취소 및 다시 실행 (`⌘Z` / `⇧⌘Z`) 지원
- macOS 통합 타이틀바 및 상단 메뉴바 구성

</details>

---

## 사용 방법

### 1. 설치 및 실행

1. 다운로드한 `ilyENG_FolderMap_Installer.pkg`를 실행합니다.
2. 사용자 계정 영역(`~/Applications`)에 설치되며, 화면 하단 Dock에 바로가기가 생성됩니다.
3. 앱을 실행한 후 상단 경로 창에서 대상 폴더를 선택하거나 Finder에서 직접 드래그합니다.

### 2. 진단 및 정리 절차

1. **진단**: 상단 `진단` 버튼을 클릭하여 폴더 트리, 중복 파일, 이름 불일치 항목을 분석합니다.
2. **사전 검토**: 탐색기 및 대시보드에서 정리 대상 항목을 확인하고 사전 대조(Before ➔ After)를 검토합니다.
3. **적용 및 복원**: 계획 승인 후 정리를 실행하며, 필요한 경우 `⌘Z` 또는 상단 [실행 취소] 버튼을 통해 이전 상태로 되돌립니다.

---

## Claude MCP 커넥터

Claude Desktop에서 ilyENG의 진단·정리 도구를 대화로 사용할 수 있습니다. **앱을 켜 두지 않아도** 동작하며, 실제 파일 변경만 앱 화면의 승인을 거칩니다.

### 연결 방법

설치 패키지가 Claude Desktop 설정(`claude_desktop_config.json`)에 `ilyeng` 커넥터를 자동 등록합니다.

> **처음 설치한 경우 Claude Desktop을 완전히 종료(`⌘Q`)한 뒤 다시 실행해야 도구가 나타납니다.** 실행 중인 상태에서는 새 커넥터가 반영되지 않습니다.

자동 등록이 되지 않은 경우, 아래 파일을 열어 `mcpServers` 안에 항목을 추가합니다.

- 파일: `~/Library/Application Support/Claude/claude_desktop_config.json`
- 경로의 `<사용자>`는 실제 사용자 이름으로 바꿔 주세요.

```json
{
  "mcpServers": {
    "ilyeng": {
      "command": "/usr/bin/python3",
      "args": ["/Users/<사용자>/Applications/ilyENG FolderMap.app/Contents/Resources/app/tools/mcp_server.py"]
    }
  }
}
```

폴더 경로를 따로 지정하지 않으면 앱에서 마지막으로 선택한 작업 폴더를 사용합니다. 다른 폴더를 다루려면 대화에서 경로를 함께 말하거나, 앱에서 대상 폴더를 먼저 바꿔 주세요.

### 사용할 수 있는 도구

| 도구 | 하는 일 | 사용 조건 |
|---|---|---|
| `ilyeng_status` | 환경 상태, 최근 계획, 되돌리기 가능 목록 | 앱 없이 사용 |
| `ilyeng_scan` | 중복·오배치·띄어쓰기·인코딩 문제 진단 (읽기 전용) | 앱 없이 사용 |
| `ilyeng_inspect` | 파일 정보와 문서 첫 부분 미리보기 | 앱 없이 사용 |
| `ilyeng_find_duplicates` | 내용이 100% 같은 중복 파일 탐색 | 앱 없이 사용 |
| `ilyeng_propose` | 정리 계획 만들기 | 앱 없이 사용 |
| `ilyeng_get_plan` | 계획 상세와 작업 목록 조회 | 앱 없이 사용 |
| `ilyeng_preview` | 실제 상태 검증 + Before ➔ After 대조표 | 앱 없이 사용 |
| `ilyeng_apply` | 승인 기록이 있는 계획 적용 | 앱에서 승인한 뒤 |
| `ilyeng_undo` | 적용한 작업을 이전 상태로 복원 | 앱 없이 사용 |
| `ilyeng_report_diagnosis` | AI 진단 리포트 저장 | 앱에서 확인 |

진단·탐색 도구는 폴더를 읽기만 하며 파일을 만들거나 바꾸지 않습니다. 정리 계획은 `ilyeng_preview`로 먼저 검증하고, 실제 적용은 앱의 **Before ➔ After 비교 후 승인** 화면에서 이뤄집니다. Claude만으로는 진단·계획·미리보기·되돌리기까지 사용할 수 있습니다.

### 대화 예시

- "내 작업 폴더 구조를 진단해서 문제 있는 폴더만 알려줘"
- "중복 파일만 찾아서 정리 계획을 만들어줘"
- "이 계획을 미리보기하고, 어떤 폴더가 어떻게 바뀌는지 표로 보여줘"
- "방금 정리한 작업을 되돌려줘"

---

## 동작 및 복구 원칙

- **격리 이동**  
  정리 대상 파일은 즉시 영구 삭제되지 않고 대상 폴더 내 `_삭제대기_수동비우기/` 폴더로 이동됩니다.
- **되돌리기**  
  이동 및 이름 변경 작업은 실행 순서대로 기록되어, 필요할 때 이전 상태로 되돌릴 수 있습니다.
- **iCloud 상태 확인**  
  아직 내려받지 않은 파일과 동기화 상태를 확인합니다.
- **로컬 파일 처리**  
  외부 서버 통신 없이 사용자 로컬 환경에서만 동작합니다.

---

## 시스템 요구사항

- **운영체제**: macOS 11.0 Big Sur 이상 (macOS 12, 13, 14, 15 지원)
- **지원 아키텍처**: Apple Silicon 및 Intel 64-bit Mac
- **실행 환경**: Python 3.12 런타임을 앱에 동봉 (별도 설치 불필요)

---

## 문의

- **개발 및 유지보수**: J.S. Kim ([joyksan@gmail.com](mailto:joyksan@gmail.com))
- **버전**: `ilyENG FolderMap v1.2.0`
- Copyright © 2026 J.S. Kim. All rights reserved.
