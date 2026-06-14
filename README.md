# PasteWin

> Windows용 클립보드 관리자 — 복사한 모든 것을 기억합니다.

[![GitHub release](https://img.shields.io/github/v/release/joulekr/PasteWin?style=flat-square)](https://github.com/joulekr/PasteWin/releases/latest)
[![Built with Tauri](https://img.shields.io/badge/Built%20with-Tauri%20v2-24C8DB?style=flat-square&logo=tauri)](https://tauri.app)
---

## 소개

PasteWin은 Windows 전용 클립보드 관리자입니다.  
복사한 텍스트, 이미지, 파일, URL을 자동으로 저장하고, 전역 단축키 한 번으로 빠르게 꺼내 쓸 수 있습니다.

시스템 트레이에 조용히 상주하며 불필요한 시스템 자원을 최소화합니다.

---

## 주요 기능

| 기능 | 설명 |
|------|------|
| **클립보드 자동 수집** | 텍스트 · 이미지 · 파일 · URL 실시간 저장 |
| **전역 단축키** | `Ctrl+Shift+V` (커스터마이징 가능) 로 창 즉시 호출 |
| **핀 고정** | 자주 쓰는 항목 상단 고정, `Ctrl+Shift+0~9` 즉시 붙여넣기 |
| **실시간 검색** | 텍스트·URL 내용 전문 검색, 타입별 필터 |
| **다중 선택** | `Ctrl+Click` · `Ctrl+A` 선택 후 일괄 붙여넣기 / 삭제 |
| **텍스트 편집** | 저장된 텍스트·URL 내용 직접 수정 |
| **이미지 미리보기** | 별도 창에서 이미지 확대·복사 |
| **앱 블랙리스트** | 특정 앱의 복사 내용 수집 제외 |
| **자동 정리** | 최대 보관 수·기간 설정, 핀 항목은 자동 보호 |
| **일시정지** | 클립보드 수집 일시정지·재개 (재시작 후에도 유지) |
| **자동 업데이트** | GitHub Releases 기반, minisign 서명 검증 |
| **자동 시작** | Windows 로그인 시 자동 실행 |
| **다크 / 라이트 테마** | 시스템 설정 연동 또는 수동 선택 |
| **한국어 / 영어** | 다국어 지원 |

---

## 레이아웃

**가로 모드** — 화면 하단에 작업표시줄 위로 고정되는 컴팩트 바 형태

**세로 모드** — 화면 우측에 패널 형태로 표시

---

## 설치

### 다운로드 (권장)

[Releases 페이지](https://github.com/joulekr/PasteWin/releases/latest)에서 최신 `.exe` 설치 파일을 받아 실행하세요.

설치 후 시스템 트레이에 아이콘이 표시됩니다.  
`Ctrl+Shift+V` 를 눌러 클립보드 창을 열 수 있습니다.

---

## 사용법

| 동작 | 방법 |
|------|------|
| 창 열기 / 닫기 | `Ctrl+Shift+V` (변경 가능) |
| 항목 붙여넣기 | 더블클릭 또는 `Enter` |
| 핀 고정 | 항목 우측 핀 아이콘 클릭 |
| 핀 즉시 붙여넣기 | `Ctrl+Shift+1` ~ `Ctrl+Shift+9` |
| 다중 선택 | `Ctrl+Click` |
| 전체 선택 | `Ctrl+A` |
| 검색 포커스 | `Ctrl+F` |
| 선택 항목 삭제 | `Delete` |
| 창 숨기기 | `Escape` |

---

## 기술 스택

| 레이어 | 기술 |
|--------|------|
| 플랫폼 | 윈도우 10/11 전용 |
| 런타임 | [Tauri v2](https://tauri.app) |
| 백엔드 | Rust |
| 프론트엔드 | React 19 + TypeScript |
| 데이터베이스 | SQLite (rusqlite, WAL 모드) |
| 클립보드 감시 | Win32 `WM_CLIPBOARDUPDATE` |
| 전역 단축키 | `tauri-plugin-global-shortcut` |
| 자동 업데이트 | `tauri-plugin-updater` + minisign |

---

## 기능 목록:

### 완료:

- [x] 자동 업데이트 기능 (v0.1.4)
- [ ] ...

### 계획:

- [ ] ...

---

## 라이선스

Copyright (c) 2026 Joule Jang

All rights reserved.

개인적·비상업적 사용은 무료로 허용됩니다.
재배포, 수정, 상업적 이용은 저작권자의 명시적 허가가 필요합니다.
