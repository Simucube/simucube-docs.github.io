## Image with size and caption, centered

<figure markdown>
  ![](assets/changing%20force%20range.png){ width="500" }
  <figcaption>Image caption</figcaption>
</figure>

## Explain words

In `assets/abbreviations.md` one can add words which will show automatically as tooltip. I.e. load cell.

## Hotkeys

Press ++esc++ to cancel or ++ctrl+alt+e++ to edit.

## Diagrams

Mermaid supported:

``` mermaid
graph LR
  A[Start] --> B{Error?};
  B -->|Yes| C[Hmm...];
  C --> D[Debug];
  D --> B;
  B ---->|No| E[Yay!];
```

## Videos

Note: use `/embed/` URL formatting, not `watch?=v=`.

![type:video](https://www.youtube.com/embed/EzzKEWTEJeI)

## Boxes

!!! tip "Tip title"
    Tip longer text.