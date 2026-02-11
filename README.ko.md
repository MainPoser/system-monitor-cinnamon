# System Monitor Cinnamon

Cinnamon 데스크톱 패널에 CPU 사용량, 메모리 사용량 및 실시간 네트워크 속도를 표시하는 작은 도구입니다.
[RunCat365](https://github.com/Kyome22/RunCat365)에서 영감을 받았습니다.


## 기능

- 📊 실시간 CPU 사용량 표시
- 💾 메모리 사용량 표시
- 🌐 네트워크 업로드/다운로드 속도 표시
- 🎨 사용자 정의 가능한 아이콘 테마 (고양이/말)
- 🌓 자동/어두운/밝은 아이콘 테마 지원
- ⚙️ 조정 가능한 새로 고침 빈도
- 🎯 경량, 낮은 리소스 소비

## 설치 방법

1. 프로젝트 파일을 로컬로 다운로드합니다.
2. 전체 폴더를 Cinnamon 애플릿 디렉토리에 복사합니다:
   ```bash
   mkdir -p ~/.local/share/cinnamon/applets/system-monitor-cinnamon@MainPoser/;
   cp -r system-monitor-cinnamon ~/.local/share/cinnamon/applets/system-monitor-cinnamon@MainPoser/;
   # 번역 파일 설치
   mkdir -p ~/.local/share/locale/zh_CN/LC_MESSAGES/;
   msgfmt -o ~/.local/share/locale/zh_CN/LC_MESSAGES/system-monitor-cinnamon@MainPoser.mo ~/.local/share/cinnamon/applets/system-monitor-cinnamon@MainPoser/po/zh_CN.po
   ```
3. Cinnamon 설정에서 애플릿을 활성화합니다.
4. 패널을 마우스 오른쪽 버튼으로 클릭 → 애플릿 추가 → "System Monitor Cinnamon"을 선택합니다.

## 사용법

설치 후 애플릿은 패널에 시스템 모니터링 정보를 자동으로 표시합니다. 기본 형식은 다음과 같습니다:

```
CPU: 45% | MEM: 2.1G/8G | ↑ 1.2MB/s ↓ 500KB/s
```

## 구성 옵션

애플릿을 마우스 오른쪽 버튼으로 클릭하고 "구성"을 선택하여 다음 옵션을 조정할 수 있습니다:

- **네트워크 속도 표시**: 패널에 네트워크 속도를 표시할지 여부를 제어합니다.
- **새로 고침 빈도**: 데이터 업데이트 간격(1-60초)을 설정합니다.
- **아이콘 테마**: 아이콘 색상 테마(시스템 따르기/흰색/검은색)를 선택합니다.
- **애니메이션 아이콘**: 애니메이션 아이콘 유형(고양이/말)을 선택합니다.

## 프로젝트 구조

```
system-monitor-cinnamon/
├── applet.js              # 메인 프로그램 파일
├── metada.json            # 애플릿 메타데이터
├── setting-schema.json    # 구성 옵션 정의
├── stylesheet.css         # 스타일 파일
├── icons/                 # 아이콘 리소스
│   └── runners/
│       ├── cat/          # 고양이 애니메이션 아이콘
│       └── horse/        # 말 애니메이션 아이콘
├── LICENSE                # 라이선스 파일
└── README.md              # 프로젝트 설명
```

## 기술 구현

- JavaScript (ES6)로 작성됨
- Cinnamon Applet 프레임워크 기반
- 시스템 파일에서 CPU, 메모리 및 네트워크 데이터 읽기
- 애니메이션 효과에 GdkPixbuf 사용

## 문제 해결

애플릿이 제대로 작동하지 않는 경우 다음 해결 방법을 시도해 보세요:

1. Cinnamon 다시 시작: `Ctrl+Alt+Esc`를 누르거나 `cinnamon --replace`를 실행합니다.
2. 시스템 로그 확인: `~/.xsession-errors`에서 오류 메시지를 확인합니다.
3. 시스템에 필요한 종속성이 설치되었는지 확인합니다.

## 기여 안내

버그 보고 및 기능 요청을 환영합니다! 코드에 기여하고 싶다면:

1. 이 프로젝트를 포크합니다.
2. 기능 브랜치를 만듭니다 (`git checkout -b feature/AmazingFeature`).
3. 변경 사항을 커밋합니다 (`git commit -m 'Add some AmazingFeature'`).
4. 브랜치에 푸시합니다 (`git push origin feature/AmazingFeature`).
5. 풀 리퀘스트를 생성합니다.

## 라이선스

이 프로젝트는 MIT 라이선스에 따라 라이선스가 부여됩니다 - 자세한 내용은 [LICENSE](LICENSE) 파일을 참조하십시오.

## 저자

MainPoser - 2026
