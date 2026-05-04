# Git 练习题

所有题目都在这里。每做完一小段，就按要求提交一次。

## 第 1 题：给故事拍第一张照片

目标：学会 commit。

1. 打开 `workspace/story.md`。
2. 把标题改成：

```md
# 星星图书馆
```

3. 在标题下面加入第一句话：

```md
米粒第一次发现，学校图书馆最里面的书架会在晚上发光。
```

4. 在 GitHub Desktop 里看 diff。
5. 提交 commit：

```text
开始星星图书馆故事
```

6. 打开 `workspace/characters.md`。
7. 把主角改成：

```md
- 米粒：五年级学生，喜欢画地图和收集贴纸。
```

8. 提交 commit：

```text
加入主角米粒
```

完成后想一想：commit 和普通保存有什么不同？

## 第 2 题：找不同

目标：学会看 diff。

1. 打开 `workspace/places.md`。
2. 把图书馆描述改成：

```md
- 星星图书馆：白天是普通图书馆，晚上书脊会亮起蓝色的小光点。
```

3. 新增一个地点：

```md
- 云梯走廊：一条看起来很短，但会把人带到不同楼层的走廊。
```

4. 提交前先在 GitHub Desktop 里看 `places.md` 的 diff。
5. 提交 commit：

```text
扩展图书馆地点
```

完成后想一想：绿色和红色分别是什么意思？

## 第 3 题：后悔药

目标：学会丢弃还没有 commit 的错误修改。

### A. 先故意犯错

1. 打开 `workspace/story.md`。
2. 在文件末尾加入：

```md
这一段是乱写的，等一下要删掉。
```

3. 去 GitHub Desktop 看 diff。
4. 用 `Discard Changes...` 丢弃这次错误修改。
5. 回到 `story.md`，确认乱写的句子不见了。

### B. 再做正确修改

1. 在 `workspace/story.md` 末尾加入：

```md
书架中间滑出一本没有书名的银色笔记本，封面上慢慢浮现出米粒的名字。
```

2. 提交 commit：

```text
发现银色笔记本
```

完成后想一想：什么时候可以点 discard？

## 第 4 题：平行世界

目标：学会 branch。

### A. 小龙结局

1. 从 `main` 创建新分支：

```text
dragon-ending
```

2. 在 `workspace/story.md` 末尾加入：

```md
银色笔记本翻到最后一页，一只纸做的小龙从书页里钻出来，邀请米粒去修补星星。
```

3. 提交 commit：

```text
尝试小龙结局
```

### B. 星图结局

1. 切回 `main`。
2. 创建新分支：

```text
space-ending
```

3. 在 `workspace/story.md` 末尾加入：

```md
银色笔记本变成一张星图，图上的红点正好指向学校操场中央。
```

4. 提交 commit：

```text
尝试星图结局
```

完成后想一想：为什么切回 `main` 后，看不到小龙结局？

## 第 5 题：合并世界线

目标：学会 merge。

1. 决定采用 `space-ending`。
2. 切到 `main`。
3. 把 `space-ending` merge 到 `main`。
4. 打开 `workspace/ideas.md`。
5. 新增：

```md
- 下一章：操场中央可能藏着一座看不见的天文台。
```

6. 提交 commit：

```text
记录下一章想法
```

完成后想一想：merge 前为什么要确认自己站在哪个分支？

## 第 6 题：解决冲突

目标：知道 conflict 为什么出现，并学会整理冲突。

### A. 创建第一个标题分支

1. 从 `main` 创建新分支：

```text
title-a
```

2. 把 `workspace/story.md` 第一行改成：

```md
# 星星图书馆：银色笔记本
```

3. 提交 commit：

```text
修改标题为银色笔记本
```

### B. 创建第二个标题分支

1. 切回 `main`。
2. 创建新分支：

```text
title-b
```

3. 把 `workspace/story.md` 第一行改成：

```md
# 星星图书馆：操场星图
```

4. 提交 commit：

```text
修改标题为操场星图
```

### C. 故意制造冲突

1. 切回 `main`。
2. 先 merge `title-a`。
3. 再 merge `title-b`。
4. 出现冲突后，打开 `workspace/story.md`。
5. 把标题整理成：

```md
# 星星图书馆：银色笔记本与操场星图
```

6. 删除所有冲突标记：

```text
<<<<<<<
=======
>>>>>>>
```

7. 完成 merge commit。

完成后想一想：为什么这次会冲突？

## 第 7 题：云端备份

目标：理解 push 和 pull。

这题主要看老师演示。如果老师让你操作，可以做：

1. 确认自己在 `main`。
2. 修改 `workspace/ideas.md`，新增一个自己的下一章想法。
3. 提交 commit，信息自己写清楚。
4. push 到 GitHub。

完成后想一想：为什么 commit 以后，别人还不一定能在 GitHub 上看到你的修改？

## 最终检查

做完以后，你应该有：

- 至少 8 个自己写的 commit。
- `main`、`dragon-ending`、`space-ending` 三个主要分支。
- 至少一次 merge。
- 一次解决 conflict 的经历。
- 一个能读懂的 `workspace/story.md`。

