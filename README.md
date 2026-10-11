# Lucky Tower Ultimate 한국어 패치

Steam 게임 **Lucky Tower Ultimate** 의 비공식 한국어 패치예요. (대사 약 9,300줄 + 메뉴/UI 470여 개)

> 캐릭터마다 말투를 살렸어요. 앨바·엑시토는 반말, 휴버트는 해요체, 소부는 노인 말투, 지니는 옛말투 등.

## 설치 (3단계)
1. [Releases](../../releases) 에서 `LTU_Korean_Patch_v1.0.0.zip` 을 받아요. **압축 암호: `0000`**
2. 압축을 풀고 `LTU_Korean_Patch.bat` 를 더블클릭해요.
3. 동의 화면에서 `Y` 를 입력하면 자동으로 설치돼요.

게임 실행 후 **설정 > 언어** 에서 **한국어** 를 고르세요. (게임이 언어를 9개로 고정해서, 중국어 자리를 한국어로 바꿨어요.)

## 제거
`LTU_Korean_Patch.bat` 를 다시 실행하고 `2` (제거)를 고르면 원래대로 돌아가요. 원본 파일은 자동으로 백업돼요.

## 어떻게 동작하나요?
- `LocaDatabase.ltu` (게임 번역 DB)의 **중국어 칸**을 한국어로 바꿔요. 원본은 `.ko_backup` 으로 보관해요.
- 게임에 한글 글꼴이 없어서, 작은 `KoreanPatch.dll` 이 시작할 때 Pretendard 글꼴을 불러와요.
- 용량이 큰 `data.unity3d` 는 건드리지 않아요.
- **게임 원문이 저장소에 들어 있지 않아요.** 번역문(`translation/*.tsv`)만 있고, 설치할 때 사용자 PC의 원본 파일에 합쳐요.

## 문제 해결
- 글자가 네모로 보임 / 게임이 멈춤: `%USERPROFILE%\AppData\LocalLow\Studio Seufz\Lucky Tower Ultimate\Player.log` 파일을 Issue 에 첨부해 주세요.
- 게임이 업데이트되면 패치가 지워질 수 있어요. 다시 설치하면 돼요. (새 대사는 영어로 나올 수 있어요.)
- Steam 무결성 검사를 하면 패치가 지워져요. 다시 설치하세요.
- 오역·어색한 문장은 `translation/ko_dialogue.tsv` 를 고쳐서 PR 을 보내 주세요. (형식: `키<TAB>번역문`, `#1.50` 같은 타이밍 표시는 그대로 두세요.)

## 폴더 구성
| 경로 | 내용 |
|---|---|
| `release/` | 배포용 zip (암호 0000) |
| `translation/` | 번역문 (키 → 한국어) |
| `src/` | 설치 프로그램, 번역 적용 도구, 글꼴 로더 소스 |

## 라이선스
코드 MIT / 번역문 출처 표기 시 자유 이용 / 글꼴 Pretendard (SIL OFL 1.1). 게임과 원문의 저작권은 Studio Seufz 및 퍼블리셔에게 있어요. 팬이 만든 비공식 패치예요.
