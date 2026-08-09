# 漢字の力 — 公開サイト

iOSアプリ「漢字の力」のサポート・法務ページ。GitHub Pages で公開している。

| | URL |
| --- | --- |
| サポート | https://kanji-no-chikara.github.io/kanji/ |
| プライバシーポリシー | https://kanji-no-chikara.github.io/kanji/privacy.html |
| 利用規約 | https://kanji-no-chikara.github.io/kanji/terms.html |
| app-ads.txt | https://kanji-no-chikara.github.io/app-ads.txt |

`app-ads.txt` は広告のなりすまし対策で、**ドメインのルートに置く必要がある**ためこの構成にしている。

## 更新のしかた

法務ページの本文は**このリポジトリで編集しない**。アプリ側リポジトリの
`App/Game/LegalText.swift` が唯一の正データで、そこから生成する。

```bash
# アプリ側リポジトリで
python3 tools/legal/build_site.py   # site/ を生成
```

生成された `site/` の中身をこのリポジトリへ反映する（`app-ads.txt` はルート、
HTMLは `kanji/` 配下）。

アプリ本体: https://github.com/reremo/kanji-justone
