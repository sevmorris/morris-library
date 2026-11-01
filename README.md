# Seven’s Library: A Selection

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
| `publisher`, `format` | Imprint, and hardcover or paperback type. `Ebook` marks a title held only in Calibre, and shows a tag on the page |
| `year` | Year first published |
| `series`, `seriesNo` | Series name and position |
| `readingGroup`, `readingOrder` | The set of books to read together, and this book's place in it, counting only books in the catalog. Second copies share a number. Author view lists each author's books under these sets, in this order |
| `isbn`, `price` | Stored but not shown on the page. The ISBN is searchable |
| `notes` | Shown on the page. "Hugo" or "Nebula" here shows an award chip instead |
| `summary` | A short, spoiler-light description, shown in a drop-down. Written for this catalog, not copied from publisher blurbs |
| `coverFile` | Path to a cover hosted in `docs/covers/`, cropped from a photo of the book or taken from Calibre. Used in place of `coverId` |
| `coverId` | Open Library cover id. The page loads the image from `covers.openlibrary.org/b/id/<coverId>-M.jpg`, and shows a blank block without one |
| `added` | Date catalogued, as `YYYY-MM-DD` |

## Licence

The MIT licence covers this repository's code and catalog data. It does not cover
the cover images in `docs/covers/`, which remain the property of their copyright
holders.
