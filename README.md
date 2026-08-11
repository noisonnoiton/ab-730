# AB-730: AI Business Professional

**Microsoft Certified: AI Business Professional** 시험 코드 **AB-730** 대비 강의 자료입니다. MkDocs Material로 빌드해 GitHub Pages로 배포합니다.

- 공개 문서: <https://noisonnoiton.github.io/ab-730/>
- 시험 정보: [Microsoft Learn - AB-730](https://learn.microsoft.com/en-us/credentials/certifications/exams/ab-730/)
- Study guide: <https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/ab-730>

## 시험 영역

2026년 7월 22일 기준 공식 skills measured를 반영합니다.

| Domain | 비중 | 내용 |
| --- | --- | --- |
| Domain 1 | 25-30% | 생성형 AI 기본 이해 |
| Domain 2 | 35-40% | AI를 사용한 prompt와 conversation 관리 |
| Domain 3 | 25-30% | AI를 사용한 business content 작성 및 분석 |

## 로컬 미리보기

```bash
uv sync --frozen --extra docs
NO_MKDOCS_2_WARNING=1 uv run mkdocs serve
```

`http://127.0.0.1:8000/`에서 확인합니다. `uv.lock`을 갱신해야 할 때만 `--frozen`을 제외하고 실행합니다.

## 빌드

```bash
uv run mkdocs build --strict -f mkdocs.yml
```

## 배포

`main` branch에 관련 파일을 push하면 [GitHub Actions workflow](.github/workflows/mkdocs-gh-pages.yml)가 strict build 후 `gh-pages` branch로 배포합니다. 최초 배포 후 repository **Settings -> Pages**에서 source를 `Deploy from a branch`, branch를 `gh-pages / (root)`로 지정합니다.

## 참고

- 이 자료는 Microsoft Learn 공식 문서를 기반으로 정리한 교육용 요약 노트입니다.
- 시험 dump나 기출 원문을 복제하지 않습니다.