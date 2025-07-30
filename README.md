# CherryStdio - Sky Mirror

English | [简体中文](README-cmn_CN.md) | [繁體中文](README-cmn_TW.md) | [廣東話](README-jyut.md)

> [Sky Mirror: **S**erenity, **K**indness, **Y**outhful, **M**ystery, **I**ntuition, **R**adiance, **R**eflection](此处可以替换为你自己定义的主题关键词)

给你的 [Cherry Studio](https://github.com/CherryHQ/cherry-studio) 带来“天空之境”主题的视觉体验。

> [!NOTE]
> 某些视觉效果可能在特定操作系统或 Cherry Studio 版本中有所差异。

## 截图

![image](**[请替换为你的主题截图1的链接]**)**
![image](**[请替换为你的主题截图2的链接]**)**

<!--
![image](**[请替换为你的主题截图3的链接]**)**
![image](**[请替换为你的主题截图4的链接]**)**
![image](**[请替换为你的主题截图5的链接]**)**
![image](**[请替换为你的主题截图6的链接]**)**
-->

## 开始使用

复制以下 CSS 到 `Settings` -> `Display Settings` -> `Custom CSS`

![image](**[请替换为展示“自定义 CSS”设置界面的截图链接]**)**

CSS

```css
/* Cherry Studio Sky Mirror Theme */
/*  [请替换为你的主题的 GitHub 仓库链接，如果有的话]  */

/*  **[在这里开始编写你的 CSS 代码]**  */
/*  **[你可以定义颜色、背景、字体等，使界面呈现“天空之境”的风格]**  */
/*  **[例如，可以使用渐变、半透明效果，以及与天空和水面相关的颜色]**  */
/*  **[请注意，这里的 CSS 代码是示例，你需要根据你的设计进行修改]**  */

body[theme-mode='light'] {
  /*  **[浅色主题的样式，例如：]**  */
  --background-color: #E0F7FA; /*  浅蓝色背景  */
  --text-color: #333;
  --primary-color: #00BCD4; /*  强调色  */
  /*  **[更多样式...]**  */
}

body[theme-mode='dark'] {
  /*  **[深色主题的样式，例如：]**  */
  --background-color: #263238; /*  深蓝色背景  */
  --text-color: #fff;
  --primary-color: #80DEEA; /*  强调色  */
  /*  **[更多样式...]**  */
}

/*  **[以下是针对 Cherry Studio 特定组件的样式示例，请根据你的主题调整]**  */

/*  聊天窗口背景  */
#chat {
  background-color: var(--background-color);
}

/*  输入框样式  */
#inputbar {
  background-color: rgba(255, 255, 255, 0.1); /*  半透明背景  */
  border: 1px solid var(--primary-color);
  color: var(--text-color);
}

/*  **[更多组件样式，请根据你的设计进行调整]**  */
/*  **[例如：侧边栏、菜单、按钮等]**  */
