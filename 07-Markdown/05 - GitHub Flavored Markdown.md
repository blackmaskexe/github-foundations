

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
- an example of mermaid syntax is as follows (add mermaid fence extension):
```md
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

## Support for GeoJSON (or TopoJSON) to create interactive maps:

- add the geojson fence extension
```md
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

## Support for rendering 3D Models:

- add the stl fence extension
```md
solid cube_corner
  facet normal 0.0 -1.0 0.0
    outer loop
      vertex 0.0 0.0 0.0
      vertex 1.0 0.0 0.0
      vertex 0.0 0.0 1.0
    endloop
  endfacet
  facet normal 0.0 0.0 -1.0
    outer loop
      vertex 0.0 0.0 0.0
      vertex 0.0 1.0 0.0
      vertex 1.0 0.0 0.0
    endloop
  endfacet
  facet normal -1.0 0.0 0.0
    outer loop
      vertex 0.0 0.0 0.0
      vertex 0.0 0.0 1.0
      vertex 0.0 1.0 0.0
    endloop
  endfacet
  facet normal 0.577 0.577 0.577
    outer loop
      vertex 1.0 0.0 0.0
      vertex 0.0 1.0 0.0
      vertex 0.0 0.0 1.0
    endloop
  endfacet
endsolid
```

```stl
solid cube_corner
  facet normal 0.0 -1.0 0.0
    outer loop
      vertex 0.0 0.0 0.0
      vertex 1.0 0.0 0.0
      vertex 0.0 0.0 1.0
    endloop
  endfacet
  facet normal 0.0 0.0 -1.0
    outer loop
      vertex 0.0 0.0 0.0
      vertex 0.0 1.0 0.0
      vertex 1.0 0.0 0.0
    endloop
  endfacet
  facet normal -1.0 0.0 0.0
    outer loop
      vertex 0.0 0.0 0.0
      vertex 0.0 0.0 1.0
      vertex 0.0 1.0 0.0
    endloop
  endfacet
  facet normal 0.577 0.577 0.577
    outer loop
      vertex 1.0 0.0 0.0
      vertex 0.0 1.0 0.0
      vertex 0.0 0.0 1.0
    endloop
  endfacet
endsolid
```

## Support for Mathematical Expressions (via Latex Formatted Math)
- uses MathJax under the hood if you're curious (🤓☝️)

1. Latex Approach:
```md
**The Cauchy-Schwarz Inequality**

$$\left( \sum_{k=1}^n a_k b_k \right)^2 \leq \left( \sum_{k=1}^n a_k^2 \right) \left( \sum_{k=1}^n b_k^2 \right)$$

($$ sign to denote start and end of latex statement)
```

**The Cauchy-Schwarz Inequality**

$$\left( \sum_{k=1}^n a_k b_k \right)^2 \leq \left( \sum_{k=1}^n a_k^2 \right) \left( \sum_{k=1}^n b_k^2 \right)$$

2. Math Approach:
```md
**The Cauchy-Schwarz Inequality**

```math
\left( \sum_{k=1}^n a_k b_k \right)^2 \leq \left( \sum_{k=1}^n a_k^2 \right) \left( \sum_{k=1}^n b_k^2 \right)
```


## Quick MD Link for Issues:
- when written within a repo with a specified issue number, these links will take you to that issue
```md
#26
GH-26

(both lead to issue number 26)
```

#26
GH-26

## Quick MD Link for Repos:
```md
blackmaskexe/habitmentor-ai
```

blackmaskexe/habitmentor-ai (please star this repository, I have spent countless hours making this mobile app please and thanks)
## Some more things to note:

- github turns raw links automatically into a link like www.prathamsnehi.com
