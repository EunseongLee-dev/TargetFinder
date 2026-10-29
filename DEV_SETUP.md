# Target Finder - Development Setup

## 1. 개발 환경

- IDE: Visual Studio Community 2022
- Visual Studio 버전: 17.14.41
- C++ 컴파일러: MSVC 19.44.35229 (x64)
- CMake: 3.31.6-msvc6
- Qt: 6.12.0
- Qt 구성: MSVC 2022 64-bit
- Qt 경로: `C:/Qt/6.12.0/msvc2022_64`
- OpenCV: 4.14.0
- OpenCV 경로: `C:/opencv`
- OpenCV CMake 설정 경로: `C:/opencv/build`
- OpenCV 라이브러리 구성: `x64/vc16`

## 2. 환경 검증 결과

- [x] 기본 C++ 프로그램 빌드 및 실행
- [x] Qt Widgets 빈 창 빌드 및 실행
- [x] OpenCV 이미지 읽기 및 크기 출력
- [ ] Git 저장소 초기화 및 첫 커밋

OpenCV 테스트 이미지 `sample.png`의 출력 크기: 674 × 1037 픽셀

## 3. 기본 CMake 명령어

설정 및 빌드 파일 생성:

```cmd
cmake -S . -B build
```

Debug 구성으로 빌드:

```cmd
cmake --build build --config Debug
```

Qt 패키지 경로 지정 예시:

```cmd
cmake -S . -B build -DCMAKE_PREFIX_PATH=C:/Qt/6.12.0/msvc2022_64
```

OpenCV 패키지 경로 지정 예시:

```cmd
cmake -S . -B build -DOpenCV_DIR=C:/opencv/build
```

## 4. 실행 시 참고 사항

테스트에서는 실행 시 필요한 DLL을 찾도록 현재 터미널의 PATH를 설정했다.

Qt DLL 경로:

`C:/Qt/6.12.0/msvc2022_64/bin`

OpenCV DLL 경로:

`C:/opencv/build/x64/vc16/bin`

위 PATH 설정은 테스트를 실행한 터미널에만 적용했다.