# CherryStdio-Aero

English | [简体中文](README-cmn_CN.md) | [繁體中文](README-cmn_TW.md) | [廣東話](README-jyut.md)

> [Aero: **A**uthentic, **E**nergetic, **R**eflective and **O**pen](https://en.wikipedia.org/wiki/Windows_Aero)

给你的 [Cherry Studio](https://github.com/CherryHQ/cherry-studio) 带来现代的 Aero 主题

> [!NOTE]
> 毛玻璃效果仅在 macOS 上的 Cherry Studio 中有效。

## 截图

![image](https://github.com/user-attachments/assets/8a3fa8a6-e28b-4628-90c8-aadb00e7437a)
![image](https://github.com/user-attachments/assets/0865e220-8398-4564-acc7-33b04220d015)

<!--
![image](https://github.com/user-attachments/assets/f1b45077-49e7-4c04-8c5f-b5099d1020aa)
![image](https://github.com/user-attachments/assets/a1203c88-9efa-489b-b3e7-a5f41961fd9e)
![image](https://github.com/user-attachments/assets/86315ef8-9bdc-4525-a4cb-b143f8b80)
![image](https://github.com/user-attachments/assets/76d6ffdd-a6be-4694-98b8-69a788208b80)
-->

## 开始使用

将以下 CSS 复制到 `Settings` -> `Display Settings` -> `Custom CSS`

![image](https://github.com/user-attachments/assets/a8e595fb-d093-4972-b439-6dfb9029c9ae)

CSS

```css
/* Cherry Studio Aero Theme */
/* https://github.com/hakadao/CherryStudio-Aero */

body[theme-mode='light'] {
  --fill-1: rgba(120 120 122 / 0.12);
  --fill-2: rgba(120 120 122 / 0.2);
  --fill-3: rgba(120 120 122 / 0.28);

  --color-white: var(--fill-1);
  --color-white-soft: var(--fill-2);
  --color-white-mute: var(--fill-3);

  --color-list-item: var(--fill-1);
  --color-list-item-hover: var(--fill-2);

  --navbar-background: hsl(240, 100%, 99.4%);

  --aero-background-1: rgba(255 255 255 / 0.2);
  --aero-background-2: rgba(255 255 255 / 0.4);
  --aero-background-3: rgba(255 255 255 / 0.6);
  --aero-background-solid: rgba(255 255 255 / 1);

  /* remove the background of the navbar to make it more transparent on macOS */
  --navbar-background-mac: rgba(255 255 255 / 0.3);
}

body[theme-mode='dark'] {
  --aero-background-1: rgba(22 22 22 / 0.2);
  --aero-background-2: rgba(22 22 22 / 0.4);
  --aero-background-3: rgba(22 22 22 / 0.6);
  --aero-background-solid: rgba(22 22 22 / 1);
}

:root {
  --fill-1: rgba(120 120 122 / 0.15);
  --fill-2: rgba(120 120 122 / 0.2);
  --fill-3: rgba(120 120 122 / 0.25);

  --color-black: var(--fill-1);
  --color-black-soft: var(--fill-2);
  --color-black-mute: var(--fill-3);

  --color-list-item: var(--fill-1);
  --color-list-item-hover: var(--fill-2);
}

/* reset ant design variables */
body[theme-mode='light'] *,
body[theme-mode='light'] [class^='ant'] {
  --ant-select-selector-bg: var(--aero-background-1);
  --ant-color-bg-container: var(--aero-background-1);
  --ant-segmented-item-selected-bg: var(--aero-background-3);
  --ant-button-default-bg: var(--aero-background-1);
  --ant-radio-button-bg: var(--aero-background-1);
}

/* reset ant design variables */
body[theme-mode='dark'] *,
body[theme-mode='dark'] [class^='ant'] {
  --ant-select-selector-bg: var(--fill-1);
  --ant-color-bg-container: var(--fill-1);
  --ant-segmented-item-selected-bg: var(--fill-3);
  --ant-button-default-bg: var(--fill-1);
  --ant-radio-button-bg: var(--fill-1);
}

/* Fix new window background issue to adapt to new UI */
[class^='PageContainer'] {
  background-color: var(--aero-background-solid) !important;
}

@media (prefers-color-scheme: dark) {
  body[theme-mode='light'] {
    background: rgba(255 255 255 / 0.3);
  }
}

@media (prefers-color-scheme: light) {
  body[theme-mode='dark'] {
    background: rgba(0 0 0 / 0.2);
  }
}

[theme-mode='light'] #content-container,
[theme-mode='light'] .minapp-drawer .ant-drawer-body {
  background-color: rgba(120 120 122 / 0.05);
}

[theme-mode='dark'] #content-container,
[theme-mode='dark'] .minapp-drawer .ant-drawer-body {
  background-color: rgba(120 120 122 / 0.05);
}

.home-tabs,
[class^='ProgramSection'],
[class^='IconSection'],
#messages,
[class^='SettingContainer'] {
  background-color: transparent;
}

[class^='TopicListItem'] .menu {
  background-color: transparent !important;
}

#inputbar,
.system-prompt,
[class^='CardContent'],
[class^='ServerCard'] {
  background-color: var(--fill-1);
}

[theme-mode='light'] #chat,
[theme-mode='light'] [class^='SettingGroup'],
[theme-mode='light'] [class^='MainContainer'],
[theme-mode='light'] [class^='MainContent'] {
  background-color: var(--aero-background-2);
}

/* On the right side of "Model Provider" in Settings */
[theme-mode='light']
  [class^='ProviderListContainer']
  + [class^='SettingContainer'] {
  background: var(--aero-background-2) !important;
}

[theme-mode='dark'] #chat,
[theme-mode='dark'] [class^='SettingGroup'],
[theme-mode='dark'] [class^='MainContainer'],
[theme-mode='dark'] [class^='MainContent'] {
  background-color: var(--aero-background-1);
}

/* On the right side of "Model Provider" in Settings */
[theme-mode='dark']
  [class^='ProviderListContainer']
  + [class^='SettingContainer'] {
  background: var(--aero-background-1) !important;
}

/* https://github.com/hakadao/CherryStudio-Aero/issues/2 */
/* search result dialog becomes too transparent: https://github.com/hakadao/CherryStudio-Aero/issues/11 */
[theme-mode='light'] [class^='ant-modal'],
[theme-mode='light'] #root[style*='background: var(--color-white)'],
/* https://github.com/hakadao/CherryStudio-Aero/issues/14 */
/* selection assitant panel */
[theme-mode='light'] [class^='WindowFrame'],
/* https://github.com/hakadao/CherryStudio-Aero/issues/13#issuecomment-3105519544 */
/* Tooltip background is too transparent */
[theme-mode='light'] .ant-tooltip-inner {
  --color-white: #ffffff;
  --color-white-soft: rgba(255, 255, 255, 0.8);
  --color-white-mute: rgba(255, 255, 255, 0.94);

  --color-background: var(--color-white);
  --color-background-soft: var(--color-white-soft);
  --color-background-mute: var(--color-white-mute);

  --ant-modal-content-bg: var(--aero-background-solid);
}
[theme-mode='dark'] [class^='ant-modal'],
/* https://github.com/hakadao/CherryStudio-Aero/issues/14 */
/* selection assitant panel */
[theme-mode='dark'] [class^='WindowFrame'],
/* https://github.com/hakadao/CherryStudio-Aero/issues/13#issuecomment-3105519544 */
/* Tooltip background is too transparent */
[theme-mode='dark'] .ant-tooltip-inner {
  --color-black: #181818;
  --color-black-soft: #222222;
  --color-black-mute: #333333;

  --color-background: var(--color-black);
  --color-background-soft: var(--color-black-soft);
  --color-background-mute: var(--color-black-mute);

  --ant-modal-content-bg: var(--aero-background-solid);
}
.bubble .message-user,
[class^='ant'] {
  --color-black: #181818;
  --color-black-soft: #222222;
  --color-black-mute: #333333;
  --color-white: #ffffff;
  --color-white-soft: rgba(255, 255, 255, 0.8);
  --color-white-mute: rgba(255, 255, 255, 0.94);

  --chat-text-user: var(--color-black);
}

/* Fix Quick Assistant's transparent background on Windows (text hard to see) */
body[theme-mode='light'][os='windows'] {
  --color-background: hsla(0 0 100% / 1);
  --color-background-opacity: hsla(0 0 90% / 0.6);
}
body[theme-mode='dark'][os='windows'] {
  --color-background: hsla(0 0 8% / 1);
  --color-background-opacity: hsla(0 0 8% / 0.6);
}

/* https://github.com/hakadao/CherryStudio-Aero/issues/5 */
/* Quick panel text hard to see */
[class^='QuickPanelBody'] {
  background-color: var(--aero-background-3) !important;
}

/* https://github.com/hakadao/CherryStudio-Aero/issues/10 */
/* The drawer title content is hard to read when open the mini app */
#root[style*='background: var(--color-background)'],
.ant-drawer-content[style*='background-color: var(--color-background)'],
/* https://github.com/hakadao/CherryStudio-Aero/issues/12 */
/* Search bar background is too transparent */
[class^='SearchBarContainer'] {
  background: var(--aero-background-solid) !important;
}

/* https://github.com/hakadao/CherryStudio-Aero/issues/15 */
.markdown [class^='Container'] [class^='Header']+[class^='Content'] {
  background: transparent;
}
