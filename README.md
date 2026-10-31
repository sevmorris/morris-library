# Morris Library

A personal book catalog, published with GitHub Pages at
<https://sevmorris.github.io/morris-library/>.

It is a single hand-written page with no build step:

- `docs/index.html` is the page.
- `docs/books.json` is the catalog, and the only place books are kept.

To add or change a book, edit `docs/books.json`. To preview it, serve `docs/` with
`python3 -m http.server --directory docs` and open <http://localhost:8000>.

## Record fields

All values are strings. `id`, `title`, `author` and `added` are required.

| Field | Meaning |
|---|---|
| `id` | Unique slug. Second copies get a suffix, such as `bear-island-2` |
| `title`, `author` | As shown on the page |
| `authorSort` | How to sort the author, such as `Asher, Neal` |
| `publisher`, `format` | Imprint, and hardcover or paperback type |
| `year` | Year first published |
| `series`, `seriesNo` | Series name and position |
| `isbn`, `price` | Stored but not shown on the page. The ISBN is searchable |
| `notes` | Shown on the page. "Hugo" or "Nebula" here shows an award chip instead |
| `added` | Date catalogued, as `YYYY-MM-DD` |
