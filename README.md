# 🎬 영상공장 (Video Factory)

**녹화본 하나, 글 하나, 줄거리 한 줄 → 바로 올릴 수 있는 유튜브 영상.**
편집·자막·목소리·버튜버 캐릭터·AI 영상·업로드까지 한 창에서, 전부 내 PC에서 돌아가는 Windows 앱입니다.

![영상공장](https://public-files.gumroad.com/pkcza9p0z7yyiyw3lbiexpcn7mik)

> 🚀 **출시 예정** — Gumroad와 BOOTH에서 판매할 예정입니다. 출시되면 이곳에 구매 링크를 올립니다.
>
> 이 저장소는 **소개 페이지**입니다. 프로그램과 소스 코드는 판매처에서 받을 수 있습니다.

---

## 무엇을 하나요

| | 넣는 것 | 나오는 것 |
|---|---|---|
| 🎮 **게임 녹화 → 풀 편집** | 녹화 파일 | 무음 컷 · 자막 · 쇼츠 · 썸네일 · 제목을 한 번에 |
| 📰 **글 하나 → 더빙 쇼츠** | 커뮤니티 글 · 뉴스 기사 | Claude가 대본을 쓰고, 목소리 · 모션 그래픽 · 버튜버 캐릭터가 들어간 쇼츠 |
| 🎞 **줄거리 → AI 드라마** | 줄거리 한 단락 | 스토리보드 → 캐릭터 시트(모든 컷에서 같은 얼굴) → 컷마다 AI 영상 → 연기 · 음악 · 다국어 자막 |

그 밖에 **POTG 찾기**, **뜨는 영상 찾기**, **작업 대기열**(밤새 돌려두고 끝나면 업로드), **올린 영상 통계**(참여 조회수 · CTR · 30초 이탈)까지 들어 있습니다.

## Claude Code로 만들었고, Claude Code와 함께 쓸 때 가장 좋습니다

모든 기능은 앱 버튼으로 쓸 수 있지만, Claude Code와 같이 쓰는 걸 강력히 추천합니다.
데이터 폴더에서 `claude`를 열고 원하는 걸 말하면 됩니다. 예) *"1화 7번 컷, 차가 카메라 옆을 지나가게 다시 만들어줘"*

이상한 게 보이면 앱의 **[✉ Claude에게]** 칸에 한 줄 적고 Claude Code에 *"요청 확인해"* 라고 하면, 화면 · 로그 · 상태를 같이 읽고 처리합니다.

## 버튜버 캐릭터 연동 (강력 추천)

없어도 동작하지만, **VTube Studio(2D)** 또는 **Warudo / VSeeFace(3D)** 를 연결하면
캐릭터가 쇼츠 내내 목소리에 맞춰 움직이고, 분위기에 따라 표정이 바뀌고, 마지막에 한마디까지 합니다.
얼굴을 드러내지 않고도 채널의 얼굴을 만들 수 있습니다.

> *지루한 일은 앱과 Claude에게 맡기고, 아낀 시간으로 좋은 콘텐츠를 만드세요.*

---

## 구성과 가격

| | 가격 | 포함 |
|---|---|---|
| **설치판** | **$89** (얼리버드: 선착순 30명 $19 할인) | Windows 설치 파일, 업데이트, 사용 설명서 (한국어 · 영어 · 일본어, 스크린샷 포함) |
| **소스 옵션** | **+$50** | 전체 Python 소스 (UI, 엔진, Claude 프롬프트, ComfyUI 워크플로, 설치 스크립트), 기술 문서, 인계 메모, Claude Code가 구조를 바로 이해하는 `CLAUDE.md` |

## 업데이트와 지원

- 업데이트가 자주 나옵니다. 기능 방향이 바뀔 수 있어서 **모든 버전의 설치 파일을 보관**합니다. 새 버전이 안 맞으면 예전 버전으로 돌아가 계속 쓸 수 있습니다.
- **지원: 구매 후 1주일간 버그 수정.** 소스를 직접 고친 버전은 지원하지 않습니다.
- 문의: **tomcat_777@naver.com**

## 필요 사양

- Windows 10/11 64비트 (Mac · Linux 미지원)
- NVIDIA RTX GPU 권장, **AI 영상은 VRAM 16GB**
- 디스크 약 10GB (AI 영상까지 쓰면 여유 공간 약 100GB)
- **본인의 Claude 구독(Claude Code) 또는 Anthropic API 키**
- 선택: VTube Studio / Warudo / VSeeFace, YouTube 계정

## 알아두실 점

- AI 영상 속도는 GPU에 따라 다릅니다. RTX 16GB 카드에서 컷 하나에 1.5~3분 (실측: RTX 5080, Wan 2.2, 640×1120, 5초 컷 — 텍스트에서 약 3분, 이미지에서 약 2분 20초). 3분짜리 드라마는 몇 시간이 걸리므로 **대기열에 넣고 밤새 돌리는 방식**입니다.
- **샘플 드라마(고스트 카마로 1화)는 개발자 PC에서 MiniMax H3로 만들었습니다.** 제품에 포함된 영상 모델은 **Wan 2.2**(Apache-2.0, 상업 이용 가능)라서 같은 줄거리라도 결과가 다르게 보일 수 있습니다.
- Claude 사용량은 본인 구독에서 나갑니다. Civitai · Hugging Face의 LoRA는 각각 약관이 있으니 받을 때 확인하세요.
- YouTube 정책(AI 표시, 반복 콘텐츠)과 저작권은 사용자 책임입니다. 수익을 보장하지 않습니다.

## 라이선스 (요약)

- 본인(또는 본인 회사) PC에 설치해서 사용. **만든 영상은 상업적으로 사용할 수 있습니다.**
- 소스 옵션 구매 시 본인 용도로 소스 수정 가능.
- 앱이나 수정본의 재배포 · 재판매, 남을 위한 서비스 운영은 금지 (만든 영상을 의뢰인에게 납품하는 건 괜찮습니다). 전체 조건은 다운로드에 포함된 `LICENSE.md`.

## 환불

디지털 상품이라 **다운로드 후에는 환불되지 않습니다.** 구매 전에 샘플 영상, 스크린샷, 사용 설명서를 꼭 확인해 주세요.
설명대로 동작하지 않는 경우(파일이 안 열림 등)에는 교체하거나 환불해 드립니다.

---

<details>
<summary><b>English</b></summary>

**A Windows app that turns a game recording, an online post, or a one-paragraph plot into videos you can upload to YouTube right away** — editing, subtitles, voice, VTuber character, AI video and upload in one window, all running on your own PC.

- **Game recording → full edit**: cuts silences, adds subtitles, makes Shorts, thumbnails and titles.
- **One post → dubbed Shorts**: Claude writes the script; voice, motion graphics and a VTuber character.
- **A plot → AI drama**: storyboard → character sheets → AI video per shot → voice acting, music, multilingual subtitles.
- POTG finder, trending video finder, overnight queue, uploaded-video stats.

**Installer $89** (early bird $19 off, first 30 buyers) · **Source option +$50**
Requires Windows 10/11, NVIDIA RTX (16 GB VRAM for AI video), your own Claude subscription or Anthropic API key.

**Coming soon** on Gumroad and BOOTH.

</details>
