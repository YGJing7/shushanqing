# 用 Obsidian 写蜀山青博客

## 第一次设置

1. 用 GitHub Desktop 克隆 `https://github.com/YGJing7/shushanqing.git` 到电脑上的一个固定文件夹。
2. 在 Obsidian 选择“打开本地文件夹作为库”，选择刚克隆的 `shushanqing` 文件夹。
3. 在 Obsidian 的“设置 → 核心插件”启用“模板”，模板文件夹填写 `templates`。

## 写一篇文章

1. 在左侧打开 `content/posts`。
2. 新建 Markdown 文件，例如 `我的第一篇笔记.md`。
3. 插入 `templates/博客文章.md` 模板，填写标题、标签和摘要。
4. 写完后回到 GitHub Desktop，输入本次修改的说明，点击“Commit to main”，再点击“Push origin”。

几分钟内，GitHub Pages 会自动发布新文章。

## 插入图片

将图片拖到 `static/images` 文件夹；在文章中使用：

```md
![图片说明](/images/图片文件名.jpg)
```

不要把文章放在 `templates` 中，正式文章只放在 `content/posts`。
