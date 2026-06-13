# cheerdex-data

[응원도감(cheerdex)](https://github.com/kinphw/cheerdex) 앱이 읽는 데이터.

- `teams.json` — 구단·선수·응원가. `cheerdex-studio` 가 export → 여기에 push.
- 앱은 jsDelivr CDN 으로 fetch: `https://cdn.jsdelivr.net/gh/kinphw/cheerdex-data@main/teams.json`
- 앱은 ETag 조건부 요청 + 로컬캐시/번들 폴백이라, 이 파일을 갱신하면 **앱 재배포 없이** 반영됨.
- 갱신 즉시 반영하려면 push 직후 `https://purge.jsdelivr.net/gh/kinphw/cheerdex-data@main/teams.json` 호출.
