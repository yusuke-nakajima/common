# 祝日のデータ

- 元: 内閣府「国民の祝日について」の CSV（https://www8.cao.go.jp/chosei/shukujitsu/syukujitsu.csv）。
- 元の文字コードは Shift_JIS。アプリで読みやすいよう UTF-8 に変えて置く。中身（列・日付の書き方）は元のまま。
  - 1行目は見出し。2行目から `2026/1/1,元日` の形（月日はゼロ埋めしない）。
- 内閣府は、例年2月ごろに翌年の祝日を足す。GitHub Actions（`.github/workflows/holidays.yml`）が毎月1日に元を取りに行き、変わっていれば更新する。手で動かすこともできる（Actions の画面の「Run workflow」）。
- RemiToDo は、初めて起動したときと、決まった日（毎年 2/15・8/15）を過ぎたあとの起動時にだけ、このファイルを読みに来る。
