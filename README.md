# Electricity Market Review

所有文献集中放在 papers 下，每篇一个文件夹，正文和图片一起保存。

```text
papers/
  p001-matamala2025/
    _p001-matamala2025.qmd
    figures/
      matamala2025/
        fig1_framework.png
        fig4_fairness.png
  p002-author-year/
    （下一篇正文和原有图片目录）
```

后续压缩包按篇放入 papers，保留包内图片的多级目录，避免不同文章的同名图片冲突。只调整图片引用路径和折叠格式，不改写总结文字。在 index.qmd 中为每篇添加 include，即可在同一页面展示。

当前首页引用：

```markdown
{{< include papers/p001-matamala2025/_p001-matamala2025.qmd >}}
```

图片引用相对于项目根目录，例如 `papers/p001-matamala2025/figures/matamala2025/fig1_framework.png`。

在项目根目录运行 `quarto preview` 预览，运行 `quarto render` 生成网页。请渲染整个项目，不单独渲染 papers 内的片段。

_site 是自动生成的网页，.quarto 是自动缓存；均无需手动管理。_quarto.yml、index.qmd 和 styles.css 分别负责配置、文献汇总与样式。
