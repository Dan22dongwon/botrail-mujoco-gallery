# 로봇 공정 시뮬레이션 갤러리

**https://dan22dongwon.github.io/botrail-mujoco-gallery/**

[botrail](https://github.com/botrail/botrail)로 설계한 로봇 공정 셀(머신텐딩, 가공, 조립, 용접, 도장, 팔레타이징,
물류·이동 로봇, 보행 로봇 등) 38개를 [MuJoCo](https://mujoco.org) 물리 엔진에서 다시 돌린 결과를 브라우저에서 3D로 봅니다.

- 카드를 누르면 3D로 재생 (드래그 회전, 휠·두 손가락 확대)
- **botrail 계획 / MuJoCo 물리 / 겹쳐 보기** 를 바꿔 가며 계획과 물리 결과의 차이를 비교
- 결과는 쉬운 말로: "잘 돌아가요" / "확인 필요", 수치는 "자세히" 안에

이 저장소는 정적 사이트 결과물만 담고 있습니다 (`index.html`, `data/` 재생 데이터, `thumbs/` 썸네일).

## 출처와 라이선스

- 원본 셀: botrail 0.13 예제. botrail 은 PolyForm Noncommercial / Small Business 라이선스(상용 라이선스 별도)이며,
  이 갤러리는 그 예제를 시뮬레이션한 결과를 **비상업적 공유 목적**으로 보여 줍니다.
- 물리 엔진: MuJoCo (Apache-2.0). 3D 표시: three.js (MIT).
- 재생 데이터는 보기용으로 줄였습니다 (초당 10프레임, 메쉬 3 mm 단순화).
