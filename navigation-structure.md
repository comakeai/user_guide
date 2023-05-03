---
layout: default
title: Navigation Structure
nav_order: 5
---

# Navigation Structure
{: .no_toc }

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
- TOC
{:toc}
</details>

---

## In-page navigation with Table of Contents

To generate a Table of Contents on your docs pages, you can use the `{:toc}` method from Kramdown, immediately after an `<ol>` in Markdown. This will automatically generate an ordered list of anchor links to various sections of the page based on headings and heading levels. There may be occasions where you're using a heading and you don't want it to show up in the TOC, so to skip a particular heading use the `{: .no_toc }` CSS class.

#### Example
{: .no_toc }

```markdown
# Navigation Structure
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}
```

This example skips the page name heading (`#`) from the TOC, as well as the heading for the Table of Contents itself (`##`) because it is redundant, followed by the table of contents itself. To get an unordered list, replace `1. TOC` above by `- TOC`.

### Collapsible Table of Contents

The Table of Contents can be made collapsible using the `<details>` and `<summary>` elements , as in the following example. The attribute `open` (expands the Table of Contents by default) and the styling with `{: .text-delta }` are optional.

```markdown
<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>
```

The result is shown at [the top of this page](#navigation-structure) (`{:toc}` can be used only once on each page).


### 그다음은?

The Table of Contents can be made collapsible using the `<details>` and `<summary>` elements , as in the following example. The attribute `open` (expands the Table of Contents by default) and the styling with `{: .text-delta }` are optional.

#### 이러면 어떻게 되지? 

The Table of Contents can be made collapsible using the `<details>` and `<summary>` elements , as in the following example. The attribute `open` (expands the Table of Contents by default) and the styling with `{: .text-delta }` are optional.


## 그럼 다시 2개를 해볼까? 

To generate a Table of Contents on your docs pages, you can use the `{:toc}` method from Kramdown, immediately after an `<ol>` in Markdown. This will automatically generate an ordered list of anchor links to various sections of the page based on headings and heading levels. There may be occasions where you're using a heading and you don't want it to show up in the TOC, so to skip a particular heading use the `{: .no_toc }` CSS class.

#### Example
{: .no_toc }