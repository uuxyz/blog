---
title: manim usage
date: 2023-09-13
---
```bash
conda create -n my-manim-environment
conda activate my-manim-environment
conda install -c conda-forge manim
manim -pqh main.py main
```

```python
class main(Scene):
    def construct(self):
        text = Text("Hello world!")
        self.play(Write(text))
```