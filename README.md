# dkzam-assets

블로그 **[매주 일본 가는 보따리상](https://dkzam333.blogspot.com)** 의 이미지 호스팅 저장소.

Blogger API v3는 이미지 업로드를 지원하지 않아, 이미지는 여기에 두고 본문에서 URL로 참조한다.
배포는 [jsDelivr](https://www.jsdelivr.com/) CDN이 담당한다.

## URL 규칙

```
https://cdn.jsdelivr.net/gh/aispark/dkzam-assets@main/images/<YYYY-MM>/<파일명>
```

예: https://cdn.jsdelivr.net/gh/aispark/dkzam-assets@main/images/2026-07/shop-doncard-showcase.jpg

- `@main` 대신 커밋 해시를 쓰면 영구 고정된다 (캐시 갱신 문제 회피)
- jsDelivr는 `@main` 태그를 최대 7일 캐시하므로, **같은 파일명으로 덮어쓰면 반영이 늦다**. 수정본은 새 파일명을 쓸 것

## 업로드

원본 사진은 `iblog` 저장소의 `scripts/dkzam-prep-photos.ts`로 회전 보정·리사이즈·워터마크를 거친 뒤 이곳에 올린다.

```bash
npx ts-node scripts/dkzam-upload-assets.ts
```

## 이미지 목록

| 파일 | 내용 |
|---|---|
| `shop-doncard-showcase.jpg` | 원피스 돈!!카드 월드챔피언십 PSA 10 쇼케이스 (장당 ¥1,180,000) |
| `mercari-doncard-price.jpg` | 메르카리 동일 카드 출품가 ¥2,222,222 |
| `shop-luffy-gold.jpg` | 루피 OP05-119 3rd Anniversary GOLD ¥1,600,000 |
| `shop-luffy-manga-alt.jpg` | 루피 망가 얼터너티브 아트 ¥930,000 / OP13-118 ¥350,000 |
| `shop-yamato-serial.jpg` | 야마토 EB02-006 미개봉 시리얼 프로모 ¥698,000 |
| `shop-pikachu-wall.jpg` | SNKRDUNK 피카츄 PSA 10 대형 진열장 (연번 세트 ¥5,580,000) |

모든 사진은 직접 촬영본이며 워터마크가 삽입돼 있다.
