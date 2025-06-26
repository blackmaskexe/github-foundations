

- aka GFM
- dialect of Markdown that is supported for user content on GitHub and GitHub Enterprise

## Features of GFM: @ [GFM Spec Website](https://github.github.com/gfm)
- collapsible sections
- embed mathematical expressions
- embed diagrams
- relative paths / linking to files in the same repo
- tasks lists can be converted into issues
- extended formatting for tables
- shorthands to autolink to issues, prs and repos
- render code snippets from other codebase via linking
- etc

## Examples of GFM Syntaxes:

1. Embedded syntax within tables:
```md
| Command | Description |
|---|---|
| `git status` | List all *new or modified* files |
| `git diff` | Show file differences that **haven't been** staged |
```

| Command | Description |
|---|---|
| `git status` | List all *new or modified* files |
| `git diff` | Show file differences that **haven't been** staged |

2. Advanced Cell Alignment:

```md
| Left-aligned | Center-aligned | Right-aligned |
| :--- | :---: | ---: |
| git status | git status | git status |
| git diff | git diff | git diff |
```

| Left-aligned | Center-aligned | Right-aligned |
| :--- | :---: | ---: |
| git status | git status | git status |
| git diff | git diff | git diff |
3. Details tag (collapsible sections):
```md
<details>

<summary>Tips for collapsed sections</summary>

### You can add a header

You can add text within a collapsed section.

You can add an image or a code block, too.

(three backticks)ruby
puts "Hello World"
(three more backticks)

</details>
```

<details>

<summary>Tips for collapsed sections</summary>

### You can add a header

You can add text within a collapsed section.

You can add an image or a code block, too.

```ruby
puts "Hello World"
```
</details>


## Support for Mermaid:
- Mermaid is a markdown-inspired tool that renders texts into diagrams
- an example of mermaid syntax is as follows:
```txt
graph TD;
A-->B;
A-->C;
B-->D;
C-->D;
```

- the above code turns into the following:
```mermaid
graph TD;
A-->B;
A-->C;
B-->D;
C-->D;
```

## Support for GeoJSON or TopoJSON to create interactive maps:

```geojson
{
  "type": "FeatureCollection",
  "features": [
    {
      "type": "Feature",
      "id": 1,
      "properties": {
        "ID": 0
      },
      "geometry": {
        "type": "Polygon",
        "coordinates": [
          [
            [-90,35],
            [-90,30],
            [-85,30],
            [-85,35],
            [-90,35]
          ]
        ]
      }
    }
  ]
}
```

