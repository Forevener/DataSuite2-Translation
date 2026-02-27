# Translation Files

## Format

File uses TSV format (tab-separated values): `key<TAB>translation`

### Columns
- **Key** (column 1) — the English source text. Do not modify.
- **Translation** (column 2) — the translated text.
- **Comment** (column 3, optional) — ignored by the parser. Use for context or notes.

### Rules
- Lines starting with `#` are comments.
- Empty lines are ignored.
- Files must use Linux newline format - LF-only (\n)
- Last entry must end with a newline, comment after that is allowed.

## Example

```
# === Menu items ===
File	Файл
Edit	Редактировать
Save changes	Сохранить изменения	#context: toolbar button

# === Messages ===
Processing {count} variables	Обработка {count} переменных
```

## Sections

Use `# === Section Name ===` comments and blank lines to group related keys. This is purely organizational — the parser treats them as comments.

## Placeholders

Keys may contain `{placeholder}` tokens (e.g. `{count}`, `{name}`). Keep them unchanged in the translation — they are replaced with values at runtime.

## Editing

- **Spreadsheet** — open the `.tsv` file directly; key and translation appear in columns A and B.
- **Text editor** — ensure your editor preserves tab characters (not spaces) and saves with LF line endings.
