---
hide: true
category_id: internal
subcategory_id: internal/markdown
id: internal/markdown/tables
type: guide
is_index: false
rank: 0
total_steps: 5
sibling_id: internal/markdown
parent_id: internal/markdown
next_page_id: ''
previous_page_id: ''
---
<!-- does not need translation -->

# テーブル

Tables can be created with the regular markdown syntax.

```md
| Header | Header | Header |
| ------ | ------ | ------ |
| Row 1  | Row 1  | Row 1  |
| Row 2  | Row 2  | Row 2  |
| Row 3  | Row 3  | Row 3  |
```

<H>

| ヘッダー | ヘッダー | ヘッダー |
| ---- | ---- | ---- |
| 行1   | 行1   | 行1   |
| 行2   | 行2   | 行2   |
| 行3   | 行3   | 行3   |

</H>

## ヘッダーの非表示

Leave headers at the top of a table empty to hide them.

```md
|        |        |        |
| ------ | ------ | ------ |
| Row 1  | Row 1  | Row 1  |
| Row 2  | Row 2  | Row 2  |
| Row 3  | Row 3  | Row 3  |
```

<H>

|     |     |     |
| --- | --- | --- |
| 行1  | 行1  | 行1  |
| 行2  | 行2  | 行2  |
| 行3  | 行3  | 行3  |

</H>

## 幅の広いテーブル

Wider tables are automatically set to scroll horizontally on smaller screens. To
allow for long tables in code you might want to add some hints to the markdown
linter to allow for long lines.

```md
<!-- markdownlint-disable line-length -->
| Header                                                                                                                                                 |
| ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `abcdefghijklmnopqrstuvwxyz01234567890abcdefghijklmnopqrstuvwxyz01234567890abcdefghijklmnopqrstuvwxyz01234567890abcdefghijklmnopqrstuvwxyz01234567890` |
<!-- markdownlint-enable line-length -->
```

<H>

<!-- markdownlint-disable line-length -->

| ヘッダー                                                                                                                                                   |
| ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `abcdefghijklmnopqrstuvwxyz01234567890abcdefghijklmnopqrstuvwxyz01234567890abcdefghijklmnopqrstuvwxyz01234567890abcdefghijklmnopqrstuvwxyz01234567890` |

<!-- markdownlint-enable line-length -->

</H>
