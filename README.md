<!DOCTYPE html>
<html>
<head><meta charset="utf-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Penguin Project</title><script src="https://cdnjs.cloudflare.com/ajax/libs/require.js/2.1.10/require.min.js"></script>




<style type="text/css">
    pre { line-height: 125%; }
td.linenos .normal { color: inherit; background-color: transparent; padding-left: 5px; padding-right: 5px; }
span.linenos { color: inherit; background-color: transparent; padding-left: 5px; padding-right: 5px; }
td.linenos .special { color: #000000; background-color: #ffffc0; padding-left: 5px; padding-right: 5px; }
span.linenos.special { color: #000000; background-color: #ffffc0; padding-left: 5px; padding-right: 5px; }
.highlight .hll { background-color: var(--jp-cell-editor-active-background) }
.highlight { background: var(--jp-cell-editor-background); color: var(--jp-mirror-editor-variable-color) }
.highlight .c { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment */
.highlight .err { color: var(--jp-mirror-editor-error-color) } /* Error */
.highlight .k { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword */
.highlight .o { color: var(--jp-mirror-editor-operator-color); font-weight: bold } /* Operator */
.highlight .p { color: var(--jp-mirror-editor-punctuation-color) } /* Punctuation */
.highlight .ch { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Hashbang */
.highlight .cm { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Multiline */
.highlight .cp { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Preproc */
.highlight .cpf { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.PreprocFile */
.highlight .c1 { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Single */
.highlight .cs { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Special */
.highlight .kc { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Constant */
.highlight .kd { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Declaration */
.highlight .kn { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Namespace */
.highlight .kp { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Pseudo */
.highlight .kr { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Reserved */
.highlight .kt { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Type */
.highlight .m { color: var(--jp-mirror-editor-number-color) } /* Literal.Number */
.highlight .s { color: var(--jp-mirror-editor-string-color) } /* Literal.String */
.highlight .ow { color: var(--jp-mirror-editor-operator-color); font-weight: bold } /* Operator.Word */
.highlight .w { color: var(--jp-mirror-editor-variable-color) } /* Text.Whitespace */
.highlight .mb { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Bin */
.highlight .mf { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Float */
.highlight .mh { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Hex */
.highlight .mi { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Integer */
.highlight .mo { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Oct */
.highlight .sa { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Affix */
.highlight .sb { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Backtick */
.highlight .sc { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Char */
.highlight .dl { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Delimiter */
.highlight .sd { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Doc */
.highlight .s2 { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Double */
.highlight .se { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Escape */
.highlight .sh { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Heredoc */
.highlight .si { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Interpol */
.highlight .sx { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Other */
.highlight .sr { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Regex */
.highlight .s1 { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Single */
.highlight .ss { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Symbol */
.highlight .il { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Integer.Long */
  </style>



<style type="text/css">
/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*
 * Mozilla scrollbar styling
 */

/* use standard opaque scrollbars for most nodes */
[data-jp-theme-scrollbars='true'] {
  scrollbar-color: rgb(var(--jp-scrollbar-thumb-color))
    var(--jp-scrollbar-background-color);
}

/* for code nodes, use a transparent style of scrollbar. These selectors
 * will match lower in the tree, and so will override the above */
[data-jp-theme-scrollbars='true'] .CodeMirror-hscrollbar,
[data-jp-theme-scrollbars='true'] .CodeMirror-vscrollbar {
  scrollbar-color: rgba(var(--jp-scrollbar-thumb-color), 0.5) transparent;
}

/*
 * Webkit scrollbar styling
 */

/* use standard opaque scrollbars for most nodes */

[data-jp-theme-scrollbars='true'] ::-webkit-scrollbar,
[data-jp-theme-scrollbars='true'] ::-webkit-scrollbar-corner {
  background: var(--jp-scrollbar-background-color);
}

[data-jp-theme-scrollbars='true'] ::-webkit-scrollbar-thumb {
  background: rgb(var(--jp-scrollbar-thumb-color));
  border: var(--jp-scrollbar-thumb-margin) solid transparent;
  background-clip: content-box;
  border-radius: var(--jp-scrollbar-thumb-radius);
}

[data-jp-theme-scrollbars='true'] ::-webkit-scrollbar-track:horizontal {
  border-left: var(--jp-scrollbar-endpad) solid
    var(--jp-scrollbar-background-color);
  border-right: var(--jp-scrollbar-endpad) solid
    var(--jp-scrollbar-background-color);
}

[data-jp-theme-scrollbars='true'] ::-webkit-scrollbar-track:vertical {
  border-top: var(--jp-scrollbar-endpad) solid
    var(--jp-scrollbar-background-color);
  border-bottom: var(--jp-scrollbar-endpad) solid
    var(--jp-scrollbar-background-color);
}

/* for code nodes, use a transparent style of scrollbar */

[data-jp-theme-scrollbars='true'] .CodeMirror-hscrollbar::-webkit-scrollbar,
[data-jp-theme-scrollbars='true'] .CodeMirror-vscrollbar::-webkit-scrollbar,
[data-jp-theme-scrollbars='true']
  .CodeMirror-hscrollbar::-webkit-scrollbar-corner,
[data-jp-theme-scrollbars='true']
  .CodeMirror-vscrollbar::-webkit-scrollbar-corner {
  background-color: transparent;
}

[data-jp-theme-scrollbars='true']
  .CodeMirror-hscrollbar::-webkit-scrollbar-thumb,
[data-jp-theme-scrollbars='true']
  .CodeMirror-vscrollbar::-webkit-scrollbar-thumb {
  background: rgba(var(--jp-scrollbar-thumb-color), 0.5);
  border: var(--jp-scrollbar-thumb-margin) solid transparent;
  background-clip: content-box;
  border-radius: var(--jp-scrollbar-thumb-radius);
}

[data-jp-theme-scrollbars='true']
  .CodeMirror-hscrollbar::-webkit-scrollbar-track:horizontal {
  border-left: var(--jp-scrollbar-endpad) solid transparent;
  border-right: var(--jp-scrollbar-endpad) solid transparent;
}

[data-jp-theme-scrollbars='true']
  .CodeMirror-vscrollbar::-webkit-scrollbar-track:vertical {
  border-top: var(--jp-scrollbar-endpad) solid transparent;
  border-bottom: var(--jp-scrollbar-endpad) solid transparent;
}

/*
 * Phosphor
 */

.lm-ScrollBar[data-orientation='horizontal'] {
  min-height: 16px;
  max-height: 16px;
  min-width: 45px;
  border-top: 1px solid #a0a0a0;
}

.lm-ScrollBar[data-orientation='vertical'] {
  min-width: 16px;
  max-width: 16px;
  min-height: 45px;
  border-left: 1px solid #a0a0a0;
}

.lm-ScrollBar-button {
  background-color: #f0f0f0;
  background-position: center center;
  min-height: 15px;
  max-height: 15px;
  min-width: 15px;
  max-width: 15px;
}

.lm-ScrollBar-button:hover {
  background-color: #dadada;
}

.lm-ScrollBar-button.lm-mod-active {
  background-color: #cdcdcd;
}

.lm-ScrollBar-track {
  background: #f0f0f0;
}

.lm-ScrollBar-thumb {
  background: #cdcdcd;
}

.lm-ScrollBar-thumb:hover {
  background: #bababa;
}

.lm-ScrollBar-thumb.lm-mod-active {
  background: #a0a0a0;
}

.lm-ScrollBar[data-orientation='horizontal'] .lm-ScrollBar-thumb {
  height: 100%;
  min-width: 15px;
  border-left: 1px solid #a0a0a0;
  border-right: 1px solid #a0a0a0;
}

.lm-ScrollBar[data-orientation='vertical'] .lm-ScrollBar-thumb {
  width: 100%;
  min-height: 15px;
  border-top: 1px solid #a0a0a0;
  border-bottom: 1px solid #a0a0a0;
}

.lm-ScrollBar[data-orientation='horizontal']
  .lm-ScrollBar-button[data-action='decrement'] {
  background-image: var(--jp-icon-caret-left);
  background-size: 17px;
}

.lm-ScrollBar[data-orientation='horizontal']
  .lm-ScrollBar-button[data-action='increment'] {
  background-image: var(--jp-icon-caret-right);
  background-size: 17px;
}

.lm-ScrollBar[data-orientation='vertical']
  .lm-ScrollBar-button[data-action='decrement'] {
  background-image: var(--jp-icon-caret-up);
  background-size: 17px;
}

.lm-ScrollBar[data-orientation='vertical']
  .lm-ScrollBar-button[data-action='increment'] {
  background-image: var(--jp-icon-caret-down);
  background-size: 17px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-Widget, /* </DEPRECATED> */
.lm-Widget {
  box-sizing: border-box;
  position: relative;
  overflow: hidden;
  cursor: default;
}


/* <DEPRECATED> */ .p-Widget.p-mod-hidden, /* </DEPRECATED> */
.lm-Widget.lm-mod-hidden {
  display: none !important;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-CommandPalette, /* </DEPRECATED> */
.lm-CommandPalette {
  display: flex;
  flex-direction: column;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}


/* <DEPRECATED> */ .p-CommandPalette-search, /* </DEPRECATED> */
.lm-CommandPalette-search {
  flex: 0 0 auto;
}


/* <DEPRECATED> */ .p-CommandPalette-content, /* </DEPRECATED> */
.lm-CommandPalette-content {
  flex: 1 1 auto;
  margin: 0;
  padding: 0;
  min-height: 0;
  overflow: auto;
  list-style-type: none;
}


/* <DEPRECATED> */ .p-CommandPalette-header, /* </DEPRECATED> */
.lm-CommandPalette-header {
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}


/* <DEPRECATED> */ .p-CommandPalette-item, /* </DEPRECATED> */
.lm-CommandPalette-item {
  display: flex;
  flex-direction: row;
}


/* <DEPRECATED> */ .p-CommandPalette-itemIcon, /* </DEPRECATED> */
.lm-CommandPalette-itemIcon {
  flex: 0 0 auto;
}


/* <DEPRECATED> */ .p-CommandPalette-itemContent, /* </DEPRECATED> */
.lm-CommandPalette-itemContent {
  flex: 1 1 auto;
  overflow: hidden;
}


/* <DEPRECATED> */ .p-CommandPalette-itemShortcut, /* </DEPRECATED> */
.lm-CommandPalette-itemShortcut {
  flex: 0 0 auto;
}


/* <DEPRECATED> */ .p-CommandPalette-itemLabel, /* </DEPRECATED> */
.lm-CommandPalette-itemLabel {
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-DockPanel, /* </DEPRECATED> */
.lm-DockPanel {
  z-index: 0;
}


/* <DEPRECATED> */ .p-DockPanel-widget, /* </DEPRECATED> */
.lm-DockPanel-widget {
  z-index: 0;
}


/* <DEPRECATED> */ .p-DockPanel-tabBar, /* </DEPRECATED> */
.lm-DockPanel-tabBar {
  z-index: 1;
}


/* <DEPRECATED> */ .p-DockPanel-handle, /* </DEPRECATED> */
.lm-DockPanel-handle {
  z-index: 2;
}


/* <DEPRECATED> */ .p-DockPanel-handle.p-mod-hidden, /* </DEPRECATED> */
.lm-DockPanel-handle.lm-mod-hidden {
  display: none !important;
}


/* <DEPRECATED> */ .p-DockPanel-handle:after, /* </DEPRECATED> */
.lm-DockPanel-handle:after {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  content: '';
}


/* <DEPRECATED> */
.p-DockPanel-handle[data-orientation='horizontal'],
/* </DEPRECATED> */
.lm-DockPanel-handle[data-orientation='horizontal'] {
  cursor: ew-resize;
}


/* <DEPRECATED> */
.p-DockPanel-handle[data-orientation='vertical'],
/* </DEPRECATED> */
.lm-DockPanel-handle[data-orientation='vertical'] {
  cursor: ns-resize;
}


/* <DEPRECATED> */
.p-DockPanel-handle[data-orientation='horizontal']:after,
/* </DEPRECATED> */
.lm-DockPanel-handle[data-orientation='horizontal']:after {
  left: 50%;
  min-width: 8px;
  transform: translateX(-50%);
}


/* <DEPRECATED> */
.p-DockPanel-handle[data-orientation='vertical']:after,
/* </DEPRECATED> */
.lm-DockPanel-handle[data-orientation='vertical']:after {
  top: 50%;
  min-height: 8px;
  transform: translateY(-50%);
}


/* <DEPRECATED> */ .p-DockPanel-overlay, /* </DEPRECATED> */
.lm-DockPanel-overlay {
  z-index: 3;
  box-sizing: border-box;
  pointer-events: none;
}


/* <DEPRECATED> */ .p-DockPanel-overlay.p-mod-hidden, /* </DEPRECATED> */
.lm-DockPanel-overlay.lm-mod-hidden {
  display: none !important;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-Menu, /* </DEPRECATED> */
.lm-Menu {
  z-index: 10000;
  position: absolute;
  white-space: nowrap;
  overflow-x: hidden;
  overflow-y: auto;
  outline: none;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}


/* <DEPRECATED> */ .p-Menu-content, /* </DEPRECATED> */
.lm-Menu-content {
  margin: 0;
  padding: 0;
  display: table;
  list-style-type: none;
}


/* <DEPRECATED> */ .p-Menu-item, /* </DEPRECATED> */
.lm-Menu-item {
  display: table-row;
}


/* <DEPRECATED> */
.p-Menu-item.p-mod-hidden,
.p-Menu-item.p-mod-collapsed,
/* </DEPRECATED> */
.lm-Menu-item.lm-mod-hidden,
.lm-Menu-item.lm-mod-collapsed {
  display: none !important;
}


/* <DEPRECATED> */
.p-Menu-itemIcon,
.p-Menu-itemSubmenuIcon,
/* </DEPRECATED> */
.lm-Menu-itemIcon,
.lm-Menu-itemSubmenuIcon {
  display: table-cell;
  text-align: center;
}


/* <DEPRECATED> */ .p-Menu-itemLabel, /* </DEPRECATED> */
.lm-Menu-itemLabel {
  display: table-cell;
  text-align: left;
}


/* <DEPRECATED> */ .p-Menu-itemShortcut, /* </DEPRECATED> */
.lm-Menu-itemShortcut {
  display: table-cell;
  text-align: right;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-MenuBar, /* </DEPRECATED> */
.lm-MenuBar {
  outline: none;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}


/* <DEPRECATED> */ .p-MenuBar-content, /* </DEPRECATED> */
.lm-MenuBar-content {
  margin: 0;
  padding: 0;
  display: flex;
  flex-direction: row;
  list-style-type: none;
}


/* <DEPRECATED> */ .p--MenuBar-item, /* </DEPRECATED> */
.lm-MenuBar-item {
  box-sizing: border-box;
}


/* <DEPRECATED> */
.p-MenuBar-itemIcon,
.p-MenuBar-itemLabel,
/* </DEPRECATED> */
.lm-MenuBar-itemIcon,
.lm-MenuBar-itemLabel {
  display: inline-block;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-ScrollBar, /* </DEPRECATED> */
.lm-ScrollBar {
  display: flex;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}


/* <DEPRECATED> */
.p-ScrollBar[data-orientation='horizontal'],
/* </DEPRECATED> */
.lm-ScrollBar[data-orientation='horizontal'] {
  flex-direction: row;
}


/* <DEPRECATED> */
.p-ScrollBar[data-orientation='vertical'],
/* </DEPRECATED> */
.lm-ScrollBar[data-orientation='vertical'] {
  flex-direction: column;
}


/* <DEPRECATED> */ .p-ScrollBar-button, /* </DEPRECATED> */
.lm-ScrollBar-button {
  box-sizing: border-box;
  flex: 0 0 auto;
}


/* <DEPRECATED> */ .p-ScrollBar-track, /* </DEPRECATED> */
.lm-ScrollBar-track {
  box-sizing: border-box;
  position: relative;
  overflow: hidden;
  flex: 1 1 auto;
}


/* <DEPRECATED> */ .p-ScrollBar-thumb, /* </DEPRECATED> */
.lm-ScrollBar-thumb {
  box-sizing: border-box;
  position: absolute;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-SplitPanel-child, /* </DEPRECATED> */
.lm-SplitPanel-child {
  z-index: 0;
}


/* <DEPRECATED> */ .p-SplitPanel-handle, /* </DEPRECATED> */
.lm-SplitPanel-handle {
  z-index: 1;
}


/* <DEPRECATED> */ .p-SplitPanel-handle.p-mod-hidden, /* </DEPRECATED> */
.lm-SplitPanel-handle.lm-mod-hidden {
  display: none !important;
}


/* <DEPRECATED> */ .p-SplitPanel-handle:after, /* </DEPRECATED> */
.lm-SplitPanel-handle:after {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  content: '';
}


/* <DEPRECATED> */
.p-SplitPanel[data-orientation='horizontal'] > .p-SplitPanel-handle,
/* </DEPRECATED> */
.lm-SplitPanel[data-orientation='horizontal'] > .lm-SplitPanel-handle {
  cursor: ew-resize;
}


/* <DEPRECATED> */
.p-SplitPanel[data-orientation='vertical'] > .p-SplitPanel-handle,
/* </DEPRECATED> */
.lm-SplitPanel[data-orientation='vertical'] > .lm-SplitPanel-handle {
  cursor: ns-resize;
}


/* <DEPRECATED> */
.p-SplitPanel[data-orientation='horizontal'] > .p-SplitPanel-handle:after,
/* </DEPRECATED> */
.lm-SplitPanel[data-orientation='horizontal'] > .lm-SplitPanel-handle:after {
  left: 50%;
  min-width: 8px;
  transform: translateX(-50%);
}


/* <DEPRECATED> */
.p-SplitPanel[data-orientation='vertical'] > .p-SplitPanel-handle:after,
/* </DEPRECATED> */
.lm-SplitPanel[data-orientation='vertical'] > .lm-SplitPanel-handle:after {
  top: 50%;
  min-height: 8px;
  transform: translateY(-50%);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-TabBar, /* </DEPRECATED> */
.lm-TabBar {
  display: flex;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}


/* <DEPRECATED> */ .p-TabBar[data-orientation='horizontal'], /* </DEPRECATED> */
.lm-TabBar[data-orientation='horizontal'] {
  flex-direction: row;
}


/* <DEPRECATED> */ .p-TabBar[data-orientation='vertical'], /* </DEPRECATED> */
.lm-TabBar[data-orientation='vertical'] {
  flex-direction: column;
}


/* <DEPRECATED> */ .p-TabBar-content, /* </DEPRECATED> */
.lm-TabBar-content {
  margin: 0;
  padding: 0;
  display: flex;
  flex: 1 1 auto;
  list-style-type: none;
}


/* <DEPRECATED> */
.p-TabBar[data-orientation='horizontal'] > .p-TabBar-content,
/* </DEPRECATED> */
.lm-TabBar[data-orientation='horizontal'] > .lm-TabBar-content {
  flex-direction: row;
}


/* <DEPRECATED> */
.p-TabBar[data-orientation='vertical'] > .p-TabBar-content,
/* </DEPRECATED> */
.lm-TabBar[data-orientation='vertical'] > .lm-TabBar-content {
  flex-direction: column;
}


/* <DEPRECATED> */ .p-TabBar-tab, /* </DEPRECATED> */
.lm-TabBar-tab {
  display: flex;
  flex-direction: row;
  box-sizing: border-box;
  overflow: hidden;
}


/* <DEPRECATED> */
.p-TabBar-tabIcon,
.p-TabBar-tabCloseIcon,
/* </DEPRECATED> */
.lm-TabBar-tabIcon,
.lm-TabBar-tabCloseIcon {
  flex: 0 0 auto;
}


/* <DEPRECATED> */ .p-TabBar-tabLabel, /* </DEPRECATED> */
.lm-TabBar-tabLabel {
  flex: 1 1 auto;
  overflow: hidden;
  white-space: nowrap;
}


/* <DEPRECATED> */ .p-TabBar-tab.p-mod-hidden, /* </DEPRECATED> */
.lm-TabBar-tab.lm-mod-hidden {
  display: none !important;
}


/* <DEPRECATED> */ .p-TabBar.p-mod-dragging .p-TabBar-tab, /* </DEPRECATED> */
.lm-TabBar.lm-mod-dragging .lm-TabBar-tab {
  position: relative;
}


/* <DEPRECATED> */
.p-TabBar.p-mod-dragging[data-orientation='horizontal'] .p-TabBar-tab,
/* </DEPRECATED> */
.lm-TabBar.lm-mod-dragging[data-orientation='horizontal'] .lm-TabBar-tab {
  left: 0;
  transition: left 150ms ease;
}


/* <DEPRECATED> */
.p-TabBar.p-mod-dragging[data-orientation='vertical'] .p-TabBar-tab,
/* </DEPRECATED> */
.lm-TabBar.lm-mod-dragging[data-orientation='vertical'] .lm-TabBar-tab {
  top: 0;
  transition: top 150ms ease;
}


/* <DEPRECATED> */
.p-TabBar.p-mod-dragging .p-TabBar-tab.p-mod-dragging
/* </DEPRECATED> */
.lm-TabBar.lm-mod-dragging .lm-TabBar-tab.lm-mod-dragging {
  transition: none;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-TabPanel-tabBar, /* </DEPRECATED> */
.lm-TabPanel-tabBar {
  z-index: 1;
}


/* <DEPRECATED> */ .p-TabPanel-stackedPanel, /* </DEPRECATED> */
.lm-TabPanel-stackedPanel {
  z-index: 0;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/

@charset "UTF-8";
/*!

Copyright 2015-present Palantir Technologies, Inc. All rights reserved.
Licensed under the Apache License, Version 2.0.

*/
html{
  -webkit-box-sizing:border-box;
          box-sizing:border-box; }

*,
*::before,
*::after{
  -webkit-box-sizing:inherit;
          box-sizing:inherit; }

body{
  text-transform:none;
  line-height:1.28581;
  letter-spacing:0;
  font-size:14px;
  font-weight:400;
  color:#182026;
  font-family:-apple-system, "BlinkMacSystemFont", "Segoe UI", "Roboto", "Oxygen", "Ubuntu", "Cantarell", "Open Sans", "Helvetica Neue", "Icons16", sans-serif; }

p{
  margin-top:0;
  margin-bottom:10px; }

small{
  font-size:12px; }

strong{
  font-weight:600; }

::-moz-selection{
  background:rgba(125, 188, 255, 0.6); }

::selection{
  background:rgba(125, 188, 255, 0.6); }
.bp3-heading{
  color:#182026;
  font-weight:600;
  margin:0 0 10px;
  padding:0; }
  .bp3-dark .bp3-heading{
    color:#f5f8fa; }

h1.bp3-heading, .bp3-running-text h1{
  line-height:40px;
  font-size:36px; }

h2.bp3-heading, .bp3-running-text h2{
  line-height:32px;
  font-size:28px; }

h3.bp3-heading, .bp3-running-text h3{
  line-height:25px;
  font-size:22px; }

h4.bp3-heading, .bp3-running-text h4{
  line-height:21px;
  font-size:18px; }

h5.bp3-heading, .bp3-running-text h5{
  line-height:19px;
  font-size:16px; }

h6.bp3-heading, .bp3-running-text h6{
  line-height:16px;
  font-size:14px; }
.bp3-ui-text{
  text-transform:none;
  line-height:1.28581;
  letter-spacing:0;
  font-size:14px;
  font-weight:400; }

.bp3-monospace-text{
  text-transform:none;
  font-family:monospace; }

.bp3-text-muted{
  color:#5c7080; }
  .bp3-dark .bp3-text-muted{
    color:#a7b6c2; }

.bp3-text-disabled{
  color:rgba(92, 112, 128, 0.6); }
  .bp3-dark .bp3-text-disabled{
    color:rgba(167, 182, 194, 0.6); }

.bp3-text-overflow-ellipsis{
  overflow:hidden;
  text-overflow:ellipsis;
  white-space:nowrap;
  word-wrap:normal; }
.bp3-running-text{
  line-height:1.5;
  font-size:14px; }
  .bp3-running-text h1{
    color:#182026;
    font-weight:600;
    margin-top:40px;
    margin-bottom:20px; }
    .bp3-dark .bp3-running-text h1{
      color:#f5f8fa; }
  .bp3-running-text h2{
    color:#182026;
    font-weight:600;
    margin-top:40px;
    margin-bottom:20px; }
    .bp3-dark .bp3-running-text h2{
      color:#f5f8fa; }
  .bp3-running-text h3{
    color:#182026;
    font-weight:600;
    margin-top:40px;
    margin-bottom:20px; }
    .bp3-dark .bp3-running-text h3{
      color:#f5f8fa; }
  .bp3-running-text h4{
    color:#182026;
    font-weight:600;
    margin-top:40px;
    margin-bottom:20px; }
    .bp3-dark .bp3-running-text h4{
      color:#f5f8fa; }
  .bp3-running-text h5{
    color:#182026;
    font-weight:600;
    margin-top:40px;
    margin-bottom:20px; }
    .bp3-dark .bp3-running-text h5{
      color:#f5f8fa; }
  .bp3-running-text h6{
    color:#182026;
    font-weight:600;
    margin-top:40px;
    margin-bottom:20px; }
    .bp3-dark .bp3-running-text h6{
      color:#f5f8fa; }
  .bp3-running-text hr{
    margin:20px 0;
    border:none;
    border-bottom:1px solid rgba(16, 22, 26, 0.15); }
    .bp3-dark .bp3-running-text hr{
      border-color:rgba(255, 255, 255, 0.15); }
  .bp3-running-text p{
    margin:0 0 10px;
    padding:0; }

.bp3-text-large{
  font-size:16px; }

.bp3-text-small{
  font-size:12px; }
a{
  text-decoration:none;
  color:#106ba3; }
  a:hover{
    cursor:pointer;
    text-decoration:underline;
    color:#106ba3; }
  a .bp3-icon, a .bp3-icon-standard, a .bp3-icon-large{
    color:inherit; }
  a code,
  .bp3-dark a code{
    color:inherit; }
  .bp3-dark a,
  .bp3-dark a:hover{
    color:#48aff0; }
    .bp3-dark a .bp3-icon, .bp3-dark a .bp3-icon-standard, .bp3-dark a .bp3-icon-large,
    .bp3-dark a:hover .bp3-icon,
    .bp3-dark a:hover .bp3-icon-standard,
    .bp3-dark a:hover .bp3-icon-large{
      color:inherit; }
.bp3-running-text code, .bp3-code{
  text-transform:none;
  font-family:monospace;
  border-radius:3px;
  -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2);
          box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2);
  background:rgba(255, 255, 255, 0.7);
  padding:2px 5px;
  color:#5c7080;
  font-size:smaller; }
  .bp3-dark .bp3-running-text code, .bp3-running-text .bp3-dark code, .bp3-dark .bp3-code{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
    background:rgba(16, 22, 26, 0.3);
    color:#a7b6c2; }
  .bp3-running-text a > code, a > .bp3-code{
    color:#137cbd; }
    .bp3-dark .bp3-running-text a > code, .bp3-running-text .bp3-dark a > code, .bp3-dark a > .bp3-code{
      color:inherit; }

.bp3-running-text pre, .bp3-code-block{
  text-transform:none;
  font-family:monospace;
  display:block;
  margin:10px 0;
  border-radius:3px;
  -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.15);
          box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.15);
  background:rgba(255, 255, 255, 0.7);
  padding:13px 15px 12px;
  line-height:1.4;
  color:#182026;
  font-size:13px;
  word-break:break-all;
  word-wrap:break-word; }
  .bp3-dark .bp3-running-text pre, .bp3-running-text .bp3-dark pre, .bp3-dark .bp3-code-block{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
    background:rgba(16, 22, 26, 0.3);
    color:#f5f8fa; }
  .bp3-running-text pre > code, .bp3-code-block > code{
    -webkit-box-shadow:none;
            box-shadow:none;
    background:none;
    padding:0;
    color:inherit;
    font-size:inherit; }

.bp3-running-text kbd, .bp3-key{
  display:-webkit-inline-box;
  display:-ms-inline-flexbox;
  display:inline-flex;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
  background:#ffffff;
  min-width:24px;
  height:24px;
  padding:3px 6px;
  vertical-align:middle;
  line-height:24px;
  color:#5c7080;
  font-family:inherit;
  font-size:12px; }
  .bp3-running-text kbd .bp3-icon, .bp3-key .bp3-icon, .bp3-running-text kbd .bp3-icon-standard, .bp3-key .bp3-icon-standard, .bp3-running-text kbd .bp3-icon-large, .bp3-key .bp3-icon-large{
    margin-right:5px; }
  .bp3-dark .bp3-running-text kbd, .bp3-running-text .bp3-dark kbd, .bp3-dark .bp3-key{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4);
    background:#394b59;
    color:#a7b6c2; }
.bp3-running-text blockquote, .bp3-blockquote{
  margin:0 0 10px;
  border-left:solid 4px rgba(167, 182, 194, 0.5);
  padding:0 20px; }
  .bp3-dark .bp3-running-text blockquote, .bp3-running-text .bp3-dark blockquote, .bp3-dark .bp3-blockquote{
    border-color:rgba(115, 134, 148, 0.5); }
.bp3-running-text ul,
.bp3-running-text ol, .bp3-list{
  margin:10px 0;
  padding-left:30px; }
  .bp3-running-text ul li:not(:last-child), .bp3-running-text ol li:not(:last-child), .bp3-list li:not(:last-child){
    margin-bottom:5px; }
  .bp3-running-text ul ol, .bp3-running-text ol ol, .bp3-list ol,
  .bp3-running-text ul ul,
  .bp3-running-text ol ul,
  .bp3-list ul{
    margin-top:5px; }

.bp3-list-unstyled{
  margin:0;
  padding:0;
  list-style:none; }
  .bp3-list-unstyled li{
    padding:0; }
.bp3-rtl{
  text-align:right; }

.bp3-dark{
  color:#f5f8fa; }

:focus{
  outline:rgba(19, 124, 189, 0.6) auto 2px;
  outline-offset:2px;
  -moz-outline-radius:6px; }

.bp3-focus-disabled :focus{
  outline:none !important; }
  .bp3-focus-disabled :focus ~ .bp3-control-indicator{
    outline:none !important; }

.bp3-alert{
  max-width:400px;
  padding:20px; }

.bp3-alert-body{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex; }
  .bp3-alert-body .bp3-icon{
    margin-top:0;
    margin-right:20px;
    font-size:40px; }

.bp3-alert-footer{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:reverse;
      -ms-flex-direction:row-reverse;
          flex-direction:row-reverse;
  margin-top:10px; }
  .bp3-alert-footer .bp3-button{
    margin-left:10px; }
.bp3-breadcrumbs{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -ms-flex-wrap:wrap;
      flex-wrap:wrap;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  margin:0;
  cursor:default;
  height:30px;
  padding:0;
  list-style:none; }
  .bp3-breadcrumbs > li{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    -webkit-box-align:center;
        -ms-flex-align:center;
            align-items:center; }
    .bp3-breadcrumbs > li::after{
      display:block;
      margin:0 5px;
      background:url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 16 16'%3e%3cpath fill-rule='evenodd' clip-rule='evenodd' d='M10.71 7.29l-4-4a1.003 1.003 0 0 0-1.42 1.42L8.59 8 5.3 11.29c-.19.18-.3.43-.3.71a1.003 1.003 0 0 0 1.71.71l4-4c.18-.18.29-.43.29-.71 0-.28-.11-.53-.29-.71z' fill='%235C7080'/%3e%3c/svg%3e");
      width:16px;
      height:16px;
      content:""; }
    .bp3-breadcrumbs > li:last-of-type::after{
      display:none; }

.bp3-breadcrumb,
.bp3-breadcrumb-current,
.bp3-breadcrumbs-collapsed{
  display:-webkit-inline-box;
  display:-ms-inline-flexbox;
  display:inline-flex;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  font-size:16px; }

.bp3-breadcrumb,
.bp3-breadcrumbs-collapsed{
  color:#5c7080; }

.bp3-breadcrumb:hover{
  text-decoration:none; }

.bp3-breadcrumb.bp3-disabled{
  cursor:not-allowed;
  color:rgba(92, 112, 128, 0.6); }

.bp3-breadcrumb .bp3-icon{
  margin-right:5px; }

.bp3-breadcrumb-current{
  color:inherit;
  font-weight:600; }
  .bp3-breadcrumb-current .bp3-input{
    vertical-align:baseline;
    font-size:inherit;
    font-weight:inherit; }

.bp3-breadcrumbs-collapsed{
  margin-right:2px;
  border:none;
  border-radius:3px;
  background:#ced9e0;
  cursor:pointer;
  padding:1px 5px;
  vertical-align:text-bottom; }
  .bp3-breadcrumbs-collapsed::before{
    display:block;
    background:url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 16 16'%3e%3cg fill='%235C7080'%3e%3ccircle cx='2' cy='8.03' r='2'/%3e%3ccircle cx='14' cy='8.03' r='2'/%3e%3ccircle cx='8' cy='8.03' r='2'/%3e%3c/g%3e%3c/svg%3e") center no-repeat;
    width:16px;
    height:16px;
    content:""; }
  .bp3-breadcrumbs-collapsed:hover{
    background:#bfccd6;
    text-decoration:none;
    color:#182026; }

.bp3-dark .bp3-breadcrumb,
.bp3-dark .bp3-breadcrumbs-collapsed{
  color:#a7b6c2; }

.bp3-dark .bp3-breadcrumbs > li::after{
  color:#a7b6c2; }

.bp3-dark .bp3-breadcrumb.bp3-disabled{
  color:rgba(167, 182, 194, 0.6); }

.bp3-dark .bp3-breadcrumb-current{
  color:#f5f8fa; }

.bp3-dark .bp3-breadcrumbs-collapsed{
  background:rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-breadcrumbs-collapsed:hover{
    background:rgba(16, 22, 26, 0.6);
    color:#f5f8fa; }
.bp3-button{
  display:-webkit-inline-box;
  display:-ms-inline-flexbox;
  display:inline-flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  border:none;
  border-radius:3px;
  cursor:pointer;
  padding:5px 10px;
  vertical-align:middle;
  text-align:left;
  font-size:14px;
  min-width:30px;
  min-height:30px; }
  .bp3-button > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-button > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-button::before,
  .bp3-button > *{
    margin-right:7px; }
  .bp3-button:empty::before,
  .bp3-button > :last-child{
    margin-right:0; }
  .bp3-button:empty{
    padding:0 !important; }
  .bp3-button:disabled, .bp3-button.bp3-disabled{
    cursor:not-allowed; }
  .bp3-button.bp3-fill{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    width:100%; }
  .bp3-button.bp3-align-right,
  .bp3-align-right .bp3-button{
    text-align:right; }
  .bp3-button.bp3-align-left,
  .bp3-align-left .bp3-button{
    text-align:left; }
  .bp3-button:not([class*="bp3-intent-"]){
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
    background-color:#f5f8fa;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.8)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.8), rgba(255, 255, 255, 0));
    color:#182026; }
    .bp3-button:not([class*="bp3-intent-"]):hover{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
      background-clip:padding-box;
      background-color:#ebf1f5; }
    .bp3-button:not([class*="bp3-intent-"]):active, .bp3-button:not([class*="bp3-intent-"]).bp3-active{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
      background-color:#d8e1e8;
      background-image:none; }
    .bp3-button:not([class*="bp3-intent-"]):disabled, .bp3-button:not([class*="bp3-intent-"]).bp3-disabled{
      outline:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      background-color:rgba(206, 217, 224, 0.5);
      background-image:none;
      cursor:not-allowed;
      color:rgba(92, 112, 128, 0.6); }
      .bp3-button:not([class*="bp3-intent-"]):disabled.bp3-active, .bp3-button:not([class*="bp3-intent-"]):disabled.bp3-active:hover, .bp3-button:not([class*="bp3-intent-"]).bp3-disabled.bp3-active, .bp3-button:not([class*="bp3-intent-"]).bp3-disabled.bp3-active:hover{
        background:rgba(206, 217, 224, 0.7); }
  .bp3-button.bp3-intent-primary{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    background-color:#137cbd;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.1)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0));
    color:#ffffff; }
    .bp3-button.bp3-intent-primary:hover, .bp3-button.bp3-intent-primary:active, .bp3-button.bp3-intent-primary.bp3-active{
      color:#ffffff; }
    .bp3-button.bp3-intent-primary:hover{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
      background-color:#106ba3; }
    .bp3-button.bp3-intent-primary:active, .bp3-button.bp3-intent-primary.bp3-active{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
      background-color:#0e5a8a;
      background-image:none; }
    .bp3-button.bp3-intent-primary:disabled, .bp3-button.bp3-intent-primary.bp3-disabled{
      border-color:transparent;
      -webkit-box-shadow:none;
              box-shadow:none;
      background-color:rgba(19, 124, 189, 0.5);
      background-image:none;
      color:rgba(255, 255, 255, 0.6); }
  .bp3-button.bp3-intent-success{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    background-color:#0f9960;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.1)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0));
    color:#ffffff; }
    .bp3-button.bp3-intent-success:hover, .bp3-button.bp3-intent-success:active, .bp3-button.bp3-intent-success.bp3-active{
      color:#ffffff; }
    .bp3-button.bp3-intent-success:hover{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
      background-color:#0d8050; }
    .bp3-button.bp3-intent-success:active, .bp3-button.bp3-intent-success.bp3-active{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
      background-color:#0a6640;
      background-image:none; }
    .bp3-button.bp3-intent-success:disabled, .bp3-button.bp3-intent-success.bp3-disabled{
      border-color:transparent;
      -webkit-box-shadow:none;
              box-shadow:none;
      background-color:rgba(15, 153, 96, 0.5);
      background-image:none;
      color:rgba(255, 255, 255, 0.6); }
  .bp3-button.bp3-intent-warning{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    background-color:#d9822b;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.1)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0));
    color:#ffffff; }
    .bp3-button.bp3-intent-warning:hover, .bp3-button.bp3-intent-warning:active, .bp3-button.bp3-intent-warning.bp3-active{
      color:#ffffff; }
    .bp3-button.bp3-intent-warning:hover{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
      background-color:#bf7326; }
    .bp3-button.bp3-intent-warning:active, .bp3-button.bp3-intent-warning.bp3-active{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
      background-color:#a66321;
      background-image:none; }
    .bp3-button.bp3-intent-warning:disabled, .bp3-button.bp3-intent-warning.bp3-disabled{
      border-color:transparent;
      -webkit-box-shadow:none;
              box-shadow:none;
      background-color:rgba(217, 130, 43, 0.5);
      background-image:none;
      color:rgba(255, 255, 255, 0.6); }
  .bp3-button.bp3-intent-danger{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    background-color:#db3737;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.1)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0));
    color:#ffffff; }
    .bp3-button.bp3-intent-danger:hover, .bp3-button.bp3-intent-danger:active, .bp3-button.bp3-intent-danger.bp3-active{
      color:#ffffff; }
    .bp3-button.bp3-intent-danger:hover{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
      background-color:#c23030; }
    .bp3-button.bp3-intent-danger:active, .bp3-button.bp3-intent-danger.bp3-active{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
      background-color:#a82a2a;
      background-image:none; }
    .bp3-button.bp3-intent-danger:disabled, .bp3-button.bp3-intent-danger.bp3-disabled{
      border-color:transparent;
      -webkit-box-shadow:none;
              box-shadow:none;
      background-color:rgba(219, 55, 55, 0.5);
      background-image:none;
      color:rgba(255, 255, 255, 0.6); }
  .bp3-button[class*="bp3-intent-"] .bp3-button-spinner .bp3-spinner-head{
    stroke:#ffffff; }
  .bp3-button.bp3-large,
  .bp3-large .bp3-button{
    min-width:40px;
    min-height:40px;
    padding:5px 15px;
    font-size:16px; }
    .bp3-button.bp3-large::before,
    .bp3-button.bp3-large > *,
    .bp3-large .bp3-button::before,
    .bp3-large .bp3-button > *{
      margin-right:10px; }
    .bp3-button.bp3-large:empty::before,
    .bp3-button.bp3-large > :last-child,
    .bp3-large .bp3-button:empty::before,
    .bp3-large .bp3-button > :last-child{
      margin-right:0; }
  .bp3-button.bp3-small,
  .bp3-small .bp3-button{
    min-width:24px;
    min-height:24px;
    padding:0 7px; }
  .bp3-button.bp3-loading{
    position:relative; }
    .bp3-button.bp3-loading[class*="bp3-icon-"]::before{
      visibility:hidden; }
    .bp3-button.bp3-loading .bp3-button-spinner{
      position:absolute;
      margin:0; }
    .bp3-button.bp3-loading > :not(.bp3-button-spinner){
      visibility:hidden; }
  .bp3-button[class*="bp3-icon-"]::before{
    line-height:1;
    font-family:"Icons16", sans-serif;
    font-size:16px;
    font-weight:400;
    font-style:normal;
    -moz-osx-font-smoothing:grayscale;
    -webkit-font-smoothing:antialiased;
    color:#5c7080; }
  .bp3-button .bp3-icon, .bp3-button .bp3-icon-standard, .bp3-button .bp3-icon-large{
    color:#5c7080; }
    .bp3-button .bp3-icon.bp3-align-right, .bp3-button .bp3-icon-standard.bp3-align-right, .bp3-button .bp3-icon-large.bp3-align-right{
      margin-left:7px; }
  .bp3-button .bp3-icon:first-child:last-child,
  .bp3-button .bp3-spinner + .bp3-icon:last-child{
    margin:0 -7px; }
  .bp3-dark .bp3-button:not([class*="bp3-intent-"]){
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
    background-color:#394b59;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.05)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.05), rgba(255, 255, 255, 0));
    color:#f5f8fa; }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"]):hover, .bp3-dark .bp3-button:not([class*="bp3-intent-"]):active, .bp3-dark .bp3-button:not([class*="bp3-intent-"]).bp3-active{
      color:#f5f8fa; }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"]):hover{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
      background-color:#30404d; }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"]):active, .bp3-dark .bp3-button:not([class*="bp3-intent-"]).bp3-active{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
      background-color:#202b33;
      background-image:none; }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"]):disabled, .bp3-dark .bp3-button:not([class*="bp3-intent-"]).bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none;
      background-color:rgba(57, 75, 89, 0.5);
      background-image:none;
      color:rgba(167, 182, 194, 0.6); }
      .bp3-dark .bp3-button:not([class*="bp3-intent-"]):disabled.bp3-active, .bp3-dark .bp3-button:not([class*="bp3-intent-"]).bp3-disabled.bp3-active{
        background:rgba(57, 75, 89, 0.7); }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"]) .bp3-button-spinner .bp3-spinner-head{
      background:rgba(16, 22, 26, 0.5);
      stroke:#8a9ba8; }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"])[class*="bp3-icon-"]::before{
      color:#a7b6c2; }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"]) .bp3-icon, .bp3-dark .bp3-button:not([class*="bp3-intent-"]) .bp3-icon-standard, .bp3-dark .bp3-button:not([class*="bp3-intent-"]) .bp3-icon-large{
      color:#a7b6c2; }
  .bp3-dark .bp3-button[class*="bp3-intent-"]{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-button[class*="bp3-intent-"]:hover{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-button[class*="bp3-intent-"]:active, .bp3-dark .bp3-button[class*="bp3-intent-"].bp3-active{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
    .bp3-dark .bp3-button[class*="bp3-intent-"]:disabled, .bp3-dark .bp3-button[class*="bp3-intent-"].bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none;
      background-image:none;
      color:rgba(255, 255, 255, 0.3); }
    .bp3-dark .bp3-button[class*="bp3-intent-"] .bp3-button-spinner .bp3-spinner-head{
      stroke:#8a9ba8; }
  .bp3-button:disabled::before,
  .bp3-button:disabled .bp3-icon, .bp3-button:disabled .bp3-icon-standard, .bp3-button:disabled .bp3-icon-large, .bp3-button.bp3-disabled::before,
  .bp3-button.bp3-disabled .bp3-icon, .bp3-button.bp3-disabled .bp3-icon-standard, .bp3-button.bp3-disabled .bp3-icon-large, .bp3-button[class*="bp3-intent-"]::before,
  .bp3-button[class*="bp3-intent-"] .bp3-icon, .bp3-button[class*="bp3-intent-"] .bp3-icon-standard, .bp3-button[class*="bp3-intent-"] .bp3-icon-large{
    color:inherit !important; }
  .bp3-button.bp3-minimal{
    -webkit-box-shadow:none;
            box-shadow:none;
    background:none; }
    .bp3-button.bp3-minimal:hover{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:rgba(167, 182, 194, 0.3);
      text-decoration:none;
      color:#182026; }
    .bp3-button.bp3-minimal:active, .bp3-button.bp3-minimal.bp3-active{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:rgba(115, 134, 148, 0.3);
      color:#182026; }
    .bp3-button.bp3-minimal:disabled, .bp3-button.bp3-minimal:disabled:hover, .bp3-button.bp3-minimal.bp3-disabled, .bp3-button.bp3-minimal.bp3-disabled:hover{
      background:none;
      cursor:not-allowed;
      color:rgba(92, 112, 128, 0.6); }
      .bp3-button.bp3-minimal:disabled.bp3-active, .bp3-button.bp3-minimal:disabled:hover.bp3-active, .bp3-button.bp3-minimal.bp3-disabled.bp3-active, .bp3-button.bp3-minimal.bp3-disabled:hover.bp3-active{
        background:rgba(115, 134, 148, 0.3); }
    .bp3-dark .bp3-button.bp3-minimal{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:none;
      color:inherit; }
      .bp3-dark .bp3-button.bp3-minimal:hover, .bp3-dark .bp3-button.bp3-minimal:active, .bp3-dark .bp3-button.bp3-minimal.bp3-active{
        -webkit-box-shadow:none;
                box-shadow:none;
        background:none; }
      .bp3-dark .bp3-button.bp3-minimal:hover{
        background:rgba(138, 155, 168, 0.15); }
      .bp3-dark .bp3-button.bp3-minimal:active, .bp3-dark .bp3-button.bp3-minimal.bp3-active{
        background:rgba(138, 155, 168, 0.3);
        color:#f5f8fa; }
      .bp3-dark .bp3-button.bp3-minimal:disabled, .bp3-dark .bp3-button.bp3-minimal:disabled:hover, .bp3-dark .bp3-button.bp3-minimal.bp3-disabled, .bp3-dark .bp3-button.bp3-minimal.bp3-disabled:hover{
        background:none;
        cursor:not-allowed;
        color:rgba(167, 182, 194, 0.6); }
        .bp3-dark .bp3-button.bp3-minimal:disabled.bp3-active, .bp3-dark .bp3-button.bp3-minimal:disabled:hover.bp3-active, .bp3-dark .bp3-button.bp3-minimal.bp3-disabled.bp3-active, .bp3-dark .bp3-button.bp3-minimal.bp3-disabled:hover.bp3-active{
          background:rgba(138, 155, 168, 0.3); }
    .bp3-button.bp3-minimal.bp3-intent-primary{
      color:#106ba3; }
      .bp3-button.bp3-minimal.bp3-intent-primary:hover, .bp3-button.bp3-minimal.bp3-intent-primary:active, .bp3-button.bp3-minimal.bp3-intent-primary.bp3-active{
        -webkit-box-shadow:none;
                box-shadow:none;
        background:none;
        color:#106ba3; }
      .bp3-button.bp3-minimal.bp3-intent-primary:hover{
        background:rgba(19, 124, 189, 0.15);
        color:#106ba3; }
      .bp3-button.bp3-minimal.bp3-intent-primary:active, .bp3-button.bp3-minimal.bp3-intent-primary.bp3-active{
        background:rgba(19, 124, 189, 0.3);
        color:#106ba3; }
      .bp3-button.bp3-minimal.bp3-intent-primary:disabled, .bp3-button.bp3-minimal.bp3-intent-primary.bp3-disabled{
        background:none;
        color:rgba(16, 107, 163, 0.5); }
        .bp3-button.bp3-minimal.bp3-intent-primary:disabled.bp3-active, .bp3-button.bp3-minimal.bp3-intent-primary.bp3-disabled.bp3-active{
          background:rgba(19, 124, 189, 0.3); }
      .bp3-button.bp3-minimal.bp3-intent-primary .bp3-button-spinner .bp3-spinner-head{
        stroke:#106ba3; }
      .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary{
        color:#48aff0; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary:hover{
          background:rgba(19, 124, 189, 0.2);
          color:#48aff0; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary:active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary.bp3-active{
          background:rgba(19, 124, 189, 0.3);
          color:#48aff0; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary:disabled, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary.bp3-disabled{
          background:none;
          color:rgba(72, 175, 240, 0.5); }
          .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary:disabled.bp3-active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary.bp3-disabled.bp3-active{
            background:rgba(19, 124, 189, 0.3); }
    .bp3-button.bp3-minimal.bp3-intent-success{
      color:#0d8050; }
      .bp3-button.bp3-minimal.bp3-intent-success:hover, .bp3-button.bp3-minimal.bp3-intent-success:active, .bp3-button.bp3-minimal.bp3-intent-success.bp3-active{
        -webkit-box-shadow:none;
                box-shadow:none;
        background:none;
        color:#0d8050; }
      .bp3-button.bp3-minimal.bp3-intent-success:hover{
        background:rgba(15, 153, 96, 0.15);
        color:#0d8050; }
      .bp3-button.bp3-minimal.bp3-intent-success:active, .bp3-button.bp3-minimal.bp3-intent-success.bp3-active{
        background:rgba(15, 153, 96, 0.3);
        color:#0d8050; }
      .bp3-button.bp3-minimal.bp3-intent-success:disabled, .bp3-button.bp3-minimal.bp3-intent-success.bp3-disabled{
        background:none;
        color:rgba(13, 128, 80, 0.5); }
        .bp3-button.bp3-minimal.bp3-intent-success:disabled.bp3-active, .bp3-button.bp3-minimal.bp3-intent-success.bp3-disabled.bp3-active{
          background:rgba(15, 153, 96, 0.3); }
      .bp3-button.bp3-minimal.bp3-intent-success .bp3-button-spinner .bp3-spinner-head{
        stroke:#0d8050; }
      .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success{
        color:#3dcc91; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success:hover{
          background:rgba(15, 153, 96, 0.2);
          color:#3dcc91; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success:active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success.bp3-active{
          background:rgba(15, 153, 96, 0.3);
          color:#3dcc91; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success:disabled, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success.bp3-disabled{
          background:none;
          color:rgba(61, 204, 145, 0.5); }
          .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success:disabled.bp3-active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success.bp3-disabled.bp3-active{
            background:rgba(15, 153, 96, 0.3); }
    .bp3-button.bp3-minimal.bp3-intent-warning{
      color:#bf7326; }
      .bp3-button.bp3-minimal.bp3-intent-warning:hover, .bp3-button.bp3-minimal.bp3-intent-warning:active, .bp3-button.bp3-minimal.bp3-intent-warning.bp3-active{
        -webkit-box-shadow:none;
                box-shadow:none;
        background:none;
        color:#bf7326; }
      .bp3-button.bp3-minimal.bp3-intent-warning:hover{
        background:rgba(217, 130, 43, 0.15);
        color:#bf7326; }
      .bp3-button.bp3-minimal.bp3-intent-warning:active, .bp3-button.bp3-minimal.bp3-intent-warning.bp3-active{
        background:rgba(217, 130, 43, 0.3);
        color:#bf7326; }
      .bp3-button.bp3-minimal.bp3-intent-warning:disabled, .bp3-button.bp3-minimal.bp3-intent-warning.bp3-disabled{
        background:none;
        color:rgba(191, 115, 38, 0.5); }
        .bp3-button.bp3-minimal.bp3-intent-warning:disabled.bp3-active, .bp3-button.bp3-minimal.bp3-intent-warning.bp3-disabled.bp3-active{
          background:rgba(217, 130, 43, 0.3); }
      .bp3-button.bp3-minimal.bp3-intent-warning .bp3-button-spinner .bp3-spinner-head{
        stroke:#bf7326; }
      .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning{
        color:#ffb366; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning:hover{
          background:rgba(217, 130, 43, 0.2);
          color:#ffb366; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning:active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning.bp3-active{
          background:rgba(217, 130, 43, 0.3);
          color:#ffb366; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning:disabled, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning.bp3-disabled{
          background:none;
          color:rgba(255, 179, 102, 0.5); }
          .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning:disabled.bp3-active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning.bp3-disabled.bp3-active{
            background:rgba(217, 130, 43, 0.3); }
    .bp3-button.bp3-minimal.bp3-intent-danger{
      color:#c23030; }
      .bp3-button.bp3-minimal.bp3-intent-danger:hover, .bp3-button.bp3-minimal.bp3-intent-danger:active, .bp3-button.bp3-minimal.bp3-intent-danger.bp3-active{
        -webkit-box-shadow:none;
                box-shadow:none;
        background:none;
        color:#c23030; }
      .bp3-button.bp3-minimal.bp3-intent-danger:hover{
        background:rgba(219, 55, 55, 0.15);
        color:#c23030; }
      .bp3-button.bp3-minimal.bp3-intent-danger:active, .bp3-button.bp3-minimal.bp3-intent-danger.bp3-active{
        background:rgba(219, 55, 55, 0.3);
        color:#c23030; }
      .bp3-button.bp3-minimal.bp3-intent-danger:disabled, .bp3-button.bp3-minimal.bp3-intent-danger.bp3-disabled{
        background:none;
        color:rgba(194, 48, 48, 0.5); }
        .bp3-button.bp3-minimal.bp3-intent-danger:disabled.bp3-active, .bp3-button.bp3-minimal.bp3-intent-danger.bp3-disabled.bp3-active{
          background:rgba(219, 55, 55, 0.3); }
      .bp3-button.bp3-minimal.bp3-intent-danger .bp3-button-spinner .bp3-spinner-head{
        stroke:#c23030; }
      .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger{
        color:#ff7373; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger:hover{
          background:rgba(219, 55, 55, 0.2);
          color:#ff7373; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger:active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger.bp3-active{
          background:rgba(219, 55, 55, 0.3);
          color:#ff7373; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger:disabled, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger.bp3-disabled{
          background:none;
          color:rgba(255, 115, 115, 0.5); }
          .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger:disabled.bp3-active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger.bp3-disabled.bp3-active{
            background:rgba(219, 55, 55, 0.3); }

a.bp3-button{
  text-align:center;
  text-decoration:none;
  -webkit-transition:none;
  transition:none; }
  a.bp3-button, a.bp3-button:hover, a.bp3-button:active{
    color:#182026; }
  a.bp3-button.bp3-disabled{
    color:rgba(92, 112, 128, 0.6); }

.bp3-button-text{
  -webkit-box-flex:0;
      -ms-flex:0 1 auto;
          flex:0 1 auto; }

.bp3-button.bp3-align-left .bp3-button-text, .bp3-button.bp3-align-right .bp3-button-text,
.bp3-button-group.bp3-align-left .bp3-button-text,
.bp3-button-group.bp3-align-right .bp3-button-text{
  -webkit-box-flex:1;
      -ms-flex:1 1 auto;
          flex:1 1 auto; }
.bp3-button-group{
  display:-webkit-inline-box;
  display:-ms-inline-flexbox;
  display:inline-flex; }
  .bp3-button-group .bp3-button{
    -webkit-box-flex:0;
        -ms-flex:0 0 auto;
            flex:0 0 auto;
    position:relative;
    z-index:4; }
    .bp3-button-group .bp3-button:focus{
      z-index:5; }
    .bp3-button-group .bp3-button:hover{
      z-index:6; }
    .bp3-button-group .bp3-button:active, .bp3-button-group .bp3-button.bp3-active{
      z-index:7; }
    .bp3-button-group .bp3-button:disabled, .bp3-button-group .bp3-button.bp3-disabled{
      z-index:3; }
    .bp3-button-group .bp3-button[class*="bp3-intent-"]{
      z-index:9; }
      .bp3-button-group .bp3-button[class*="bp3-intent-"]:focus{
        z-index:10; }
      .bp3-button-group .bp3-button[class*="bp3-intent-"]:hover{
        z-index:11; }
      .bp3-button-group .bp3-button[class*="bp3-intent-"]:active, .bp3-button-group .bp3-button[class*="bp3-intent-"].bp3-active{
        z-index:12; }
      .bp3-button-group .bp3-button[class*="bp3-intent-"]:disabled, .bp3-button-group .bp3-button[class*="bp3-intent-"].bp3-disabled{
        z-index:8; }
  .bp3-button-group:not(.bp3-minimal) > .bp3-popover-wrapper:not(:first-child) .bp3-button,
  .bp3-button-group:not(.bp3-minimal) > .bp3-button:not(:first-child){
    border-top-left-radius:0;
    border-bottom-left-radius:0; }
  .bp3-button-group:not(.bp3-minimal) > .bp3-popover-wrapper:not(:last-child) .bp3-button,
  .bp3-button-group:not(.bp3-minimal) > .bp3-button:not(:last-child){
    margin-right:-1px;
    border-top-right-radius:0;
    border-bottom-right-radius:0; }
  .bp3-button-group.bp3-minimal .bp3-button{
    -webkit-box-shadow:none;
            box-shadow:none;
    background:none; }
    .bp3-button-group.bp3-minimal .bp3-button:hover{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:rgba(167, 182, 194, 0.3);
      text-decoration:none;
      color:#182026; }
    .bp3-button-group.bp3-minimal .bp3-button:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-active{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:rgba(115, 134, 148, 0.3);
      color:#182026; }
    .bp3-button-group.bp3-minimal .bp3-button:disabled, .bp3-button-group.bp3-minimal .bp3-button:disabled:hover, .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled, .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled:hover{
      background:none;
      cursor:not-allowed;
      color:rgba(92, 112, 128, 0.6); }
      .bp3-button-group.bp3-minimal .bp3-button:disabled.bp3-active, .bp3-button-group.bp3-minimal .bp3-button:disabled:hover.bp3-active, .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled.bp3-active, .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled:hover.bp3-active{
        background:rgba(115, 134, 148, 0.3); }
    .bp3-dark .bp3-button-group.bp3-minimal .bp3-button{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:none;
      color:inherit; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:hover, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-active{
        -webkit-box-shadow:none;
                box-shadow:none;
        background:none; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:hover{
        background:rgba(138, 155, 168, 0.15); }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-active{
        background:rgba(138, 155, 168, 0.3);
        color:#f5f8fa; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:disabled, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:disabled:hover, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled:hover{
        background:none;
        cursor:not-allowed;
        color:rgba(167, 182, 194, 0.6); }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:disabled.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:disabled:hover.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled:hover.bp3-active{
          background:rgba(138, 155, 168, 0.3); }
    .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary{
      color:#106ba3; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:hover, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-active{
        -webkit-box-shadow:none;
                box-shadow:none;
        background:none;
        color:#106ba3; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:hover{
        background:rgba(19, 124, 189, 0.15);
        color:#106ba3; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-active{
        background:rgba(19, 124, 189, 0.3);
        color:#106ba3; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:disabled, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-disabled{
        background:none;
        color:rgba(16, 107, 163, 0.5); }
        .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:disabled.bp3-active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-disabled.bp3-active{
          background:rgba(19, 124, 189, 0.3); }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary .bp3-button-spinner .bp3-spinner-head{
        stroke:#106ba3; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary{
        color:#48aff0; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:hover{
          background:rgba(19, 124, 189, 0.2);
          color:#48aff0; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-active{
          background:rgba(19, 124, 189, 0.3);
          color:#48aff0; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:disabled, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-disabled{
          background:none;
          color:rgba(72, 175, 240, 0.5); }
          .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:disabled.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-disabled.bp3-active{
            background:rgba(19, 124, 189, 0.3); }
    .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success{
      color:#0d8050; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:hover, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-active{
        -webkit-box-shadow:none;
                box-shadow:none;
        background:none;
        color:#0d8050; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:hover{
        background:rgba(15, 153, 96, 0.15);
        color:#0d8050; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-active{
        background:rgba(15, 153, 96, 0.3);
        color:#0d8050; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:disabled, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-disabled{
        background:none;
        color:rgba(13, 128, 80, 0.5); }
        .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:disabled.bp3-active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-disabled.bp3-active{
          background:rgba(15, 153, 96, 0.3); }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success .bp3-button-spinner .bp3-spinner-head{
        stroke:#0d8050; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success{
        color:#3dcc91; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:hover{
          background:rgba(15, 153, 96, 0.2);
          color:#3dcc91; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-active{
          background:rgba(15, 153, 96, 0.3);
          color:#3dcc91; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:disabled, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-disabled{
          background:none;
          color:rgba(61, 204, 145, 0.5); }
          .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:disabled.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-disabled.bp3-active{
            background:rgba(15, 153, 96, 0.3); }
    .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning{
      color:#bf7326; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:hover, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-active{
        -webkit-box-shadow:none;
                box-shadow:none;
        background:none;
        color:#bf7326; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:hover{
        background:rgba(217, 130, 43, 0.15);
        color:#bf7326; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-active{
        background:rgba(217, 130, 43, 0.3);
        color:#bf7326; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:disabled, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-disabled{
        background:none;
        color:rgba(191, 115, 38, 0.5); }
        .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:disabled.bp3-active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-disabled.bp3-active{
          background:rgba(217, 130, 43, 0.3); }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning .bp3-button-spinner .bp3-spinner-head{
        stroke:#bf7326; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning{
        color:#ffb366; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:hover{
          background:rgba(217, 130, 43, 0.2);
          color:#ffb366; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-active{
          background:rgba(217, 130, 43, 0.3);
          color:#ffb366; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:disabled, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-disabled{
          background:none;
          color:rgba(255, 179, 102, 0.5); }
          .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:disabled.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-disabled.bp3-active{
            background:rgba(217, 130, 43, 0.3); }
    .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger{
      color:#c23030; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:hover, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-active{
        -webkit-box-shadow:none;
                box-shadow:none;
        background:none;
        color:#c23030; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:hover{
        background:rgba(219, 55, 55, 0.15);
        color:#c23030; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-active{
        background:rgba(219, 55, 55, 0.3);
        color:#c23030; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:disabled, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-disabled{
        background:none;
        color:rgba(194, 48, 48, 0.5); }
        .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:disabled.bp3-active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-disabled.bp3-active{
          background:rgba(219, 55, 55, 0.3); }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger .bp3-button-spinner .bp3-spinner-head{
        stroke:#c23030; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger{
        color:#ff7373; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:hover{
          background:rgba(219, 55, 55, 0.2);
          color:#ff7373; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-active{
          background:rgba(219, 55, 55, 0.3);
          color:#ff7373; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:disabled, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-disabled{
          background:none;
          color:rgba(255, 115, 115, 0.5); }
          .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:disabled.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-disabled.bp3-active{
            background:rgba(219, 55, 55, 0.3); }
  .bp3-button-group .bp3-popover-wrapper,
  .bp3-button-group .bp3-popover-target{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto; }
  .bp3-button-group.bp3-fill{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    width:100%; }
  .bp3-button-group .bp3-button.bp3-fill,
  .bp3-button-group.bp3-fill .bp3-button:not(.bp3-fixed){
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto; }
  .bp3-button-group.bp3-vertical{
    -webkit-box-orient:vertical;
    -webkit-box-direction:normal;
        -ms-flex-direction:column;
            flex-direction:column;
    -webkit-box-align:stretch;
        -ms-flex-align:stretch;
            align-items:stretch;
    vertical-align:top; }
    .bp3-button-group.bp3-vertical.bp3-fill{
      width:unset;
      height:100%; }
    .bp3-button-group.bp3-vertical .bp3-button{
      margin-right:0 !important;
      width:100%; }
    .bp3-button-group.bp3-vertical:not(.bp3-minimal) > .bp3-popover-wrapper:first-child .bp3-button,
    .bp3-button-group.bp3-vertical:not(.bp3-minimal) > .bp3-button:first-child{
      border-radius:3px 3px 0 0; }
    .bp3-button-group.bp3-vertical:not(.bp3-minimal) > .bp3-popover-wrapper:last-child .bp3-button,
    .bp3-button-group.bp3-vertical:not(.bp3-minimal) > .bp3-button:last-child{
      border-radius:0 0 3px 3px; }
    .bp3-button-group.bp3-vertical:not(.bp3-minimal) > .bp3-popover-wrapper:not(:last-child) .bp3-button,
    .bp3-button-group.bp3-vertical:not(.bp3-minimal) > .bp3-button:not(:last-child){
      margin-bottom:-1px; }
  .bp3-button-group.bp3-align-left .bp3-button{
    text-align:left; }
  .bp3-dark .bp3-button-group:not(.bp3-minimal) > .bp3-popover-wrapper:not(:last-child) .bp3-button,
  .bp3-dark .bp3-button-group:not(.bp3-minimal) > .bp3-button:not(:last-child){
    margin-right:1px; }
  .bp3-dark .bp3-button-group.bp3-vertical > .bp3-popover-wrapper:not(:last-child) .bp3-button,
  .bp3-dark .bp3-button-group.bp3-vertical > .bp3-button:not(:last-child){
    margin-bottom:1px; }
.bp3-callout{
  line-height:1.5;
  font-size:14px;
  position:relative;
  border-radius:3px;
  background-color:rgba(138, 155, 168, 0.15);
  width:100%;
  padding:10px 12px 9px; }
  .bp3-callout[class*="bp3-icon-"]{
    padding-left:40px; }
    .bp3-callout[class*="bp3-icon-"]::before{
      line-height:1;
      font-family:"Icons20", sans-serif;
      font-size:20px;
      font-weight:400;
      font-style:normal;
      -moz-osx-font-smoothing:grayscale;
      -webkit-font-smoothing:antialiased;
      position:absolute;
      top:10px;
      left:10px;
      color:#5c7080; }
  .bp3-callout.bp3-callout-icon{
    padding-left:40px; }
    .bp3-callout.bp3-callout-icon > .bp3-icon:first-child{
      position:absolute;
      top:10px;
      left:10px;
      color:#5c7080; }
  .bp3-callout .bp3-heading{
    margin-top:0;
    margin-bottom:5px;
    line-height:20px; }
    .bp3-callout .bp3-heading:last-child{
      margin-bottom:0; }
  .bp3-dark .bp3-callout{
    background-color:rgba(138, 155, 168, 0.2); }
    .bp3-dark .bp3-callout[class*="bp3-icon-"]::before{
      color:#a7b6c2; }
  .bp3-callout.bp3-intent-primary{
    background-color:rgba(19, 124, 189, 0.15); }
    .bp3-callout.bp3-intent-primary[class*="bp3-icon-"]::before,
    .bp3-callout.bp3-intent-primary > .bp3-icon:first-child,
    .bp3-callout.bp3-intent-primary .bp3-heading{
      color:#106ba3; }
    .bp3-dark .bp3-callout.bp3-intent-primary{
      background-color:rgba(19, 124, 189, 0.25); }
      .bp3-dark .bp3-callout.bp3-intent-primary[class*="bp3-icon-"]::before,
      .bp3-dark .bp3-callout.bp3-intent-primary > .bp3-icon:first-child,
      .bp3-dark .bp3-callout.bp3-intent-primary .bp3-heading{
        color:#48aff0; }
  .bp3-callout.bp3-intent-success{
    background-color:rgba(15, 153, 96, 0.15); }
    .bp3-callout.bp3-intent-success[class*="bp3-icon-"]::before,
    .bp3-callout.bp3-intent-success > .bp3-icon:first-child,
    .bp3-callout.bp3-intent-success .bp3-heading{
      color:#0d8050; }
    .bp3-dark .bp3-callout.bp3-intent-success{
      background-color:rgba(15, 153, 96, 0.25); }
      .bp3-dark .bp3-callout.bp3-intent-success[class*="bp3-icon-"]::before,
      .bp3-dark .bp3-callout.bp3-intent-success > .bp3-icon:first-child,
      .bp3-dark .bp3-callout.bp3-intent-success .bp3-heading{
        color:#3dcc91; }
  .bp3-callout.bp3-intent-warning{
    background-color:rgba(217, 130, 43, 0.15); }
    .bp3-callout.bp3-intent-warning[class*="bp3-icon-"]::before,
    .bp3-callout.bp3-intent-warning > .bp3-icon:first-child,
    .bp3-callout.bp3-intent-warning .bp3-heading{
      color:#bf7326; }
    .bp3-dark .bp3-callout.bp3-intent-warning{
      background-color:rgba(217, 130, 43, 0.25); }
      .bp3-dark .bp3-callout.bp3-intent-warning[class*="bp3-icon-"]::before,
      .bp3-dark .bp3-callout.bp3-intent-warning > .bp3-icon:first-child,
      .bp3-dark .bp3-callout.bp3-intent-warning .bp3-heading{
        color:#ffb366; }
  .bp3-callout.bp3-intent-danger{
    background-color:rgba(219, 55, 55, 0.15); }
    .bp3-callout.bp3-intent-danger[class*="bp3-icon-"]::before,
    .bp3-callout.bp3-intent-danger > .bp3-icon:first-child,
    .bp3-callout.bp3-intent-danger .bp3-heading{
      color:#c23030; }
    .bp3-dark .bp3-callout.bp3-intent-danger{
      background-color:rgba(219, 55, 55, 0.25); }
      .bp3-dark .bp3-callout.bp3-intent-danger[class*="bp3-icon-"]::before,
      .bp3-dark .bp3-callout.bp3-intent-danger > .bp3-icon:first-child,
      .bp3-dark .bp3-callout.bp3-intent-danger .bp3-heading{
        color:#ff7373; }
  .bp3-running-text .bp3-callout{
    margin:20px 0; }
.bp3-card{
  border-radius:3px;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.15), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.15), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0);
  background-color:#ffffff;
  padding:20px;
  -webkit-transition:-webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:-webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), box-shadow 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), box-shadow 200ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 200ms cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-card.bp3-dark,
  .bp3-dark .bp3-card{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0);
    background-color:#30404d; }

.bp3-elevation-0{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.15), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.15), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0); }
  .bp3-elevation-0.bp3-dark,
  .bp3-dark .bp3-elevation-0{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0); }

.bp3-elevation-1{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-elevation-1.bp3-dark,
  .bp3-dark .bp3-elevation-1{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4); }

.bp3-elevation-2{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 1px 1px rgba(16, 22, 26, 0.2), 0 2px 6px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 1px 1px rgba(16, 22, 26, 0.2), 0 2px 6px rgba(16, 22, 26, 0.2); }
  .bp3-elevation-2.bp3-dark,
  .bp3-dark .bp3-elevation-2{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.4), 0 2px 6px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.4), 0 2px 6px rgba(16, 22, 26, 0.4); }

.bp3-elevation-3{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2); }
  .bp3-elevation-3.bp3-dark,
  .bp3-dark .bp3-elevation-3{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4); }

.bp3-elevation-4{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2); }
  .bp3-elevation-4.bp3-dark,
  .bp3-dark .bp3-elevation-4{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4); }

.bp3-card.bp3-interactive:hover{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
  cursor:pointer; }
  .bp3-card.bp3-interactive:hover.bp3-dark,
  .bp3-dark .bp3-card.bp3-interactive:hover{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4); }

.bp3-card.bp3-interactive:active{
  opacity:0.9;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
  -webkit-transition-duration:0;
          transition-duration:0; }
  .bp3-card.bp3-interactive:active.bp3-dark,
  .bp3-dark .bp3-card.bp3-interactive:active{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4); }

.bp3-collapse{
  height:0;
  overflow-y:hidden;
  -webkit-transition:height 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:height 200ms cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-collapse .bp3-collapse-body{
    -webkit-transition:-webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:-webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9); }
    .bp3-collapse .bp3-collapse-body[aria-hidden="true"]{
      display:none; }

.bp3-context-menu .bp3-popover-target{
  display:block; }

.bp3-context-menu-popover-target{
  position:fixed; }

.bp3-divider{
  margin:5px;
  border-right:1px solid rgba(16, 22, 26, 0.15);
  border-bottom:1px solid rgba(16, 22, 26, 0.15); }
  .bp3-dark .bp3-divider{
    border-color:rgba(16, 22, 26, 0.4); }
.bp3-dialog-container{
  opacity:1;
  -webkit-transform:scale(1);
          transform:scale(1);
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  width:100%;
  min-height:100%;
  pointer-events:none;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-dialog-container.bp3-overlay-enter > .bp3-dialog, .bp3-dialog-container.bp3-overlay-appear > .bp3-dialog{
    opacity:0;
    -webkit-transform:scale(0.5);
            transform:scale(0.5); }
  .bp3-dialog-container.bp3-overlay-enter-active > .bp3-dialog, .bp3-dialog-container.bp3-overlay-appear-active > .bp3-dialog{
    opacity:1;
    -webkit-transform:scale(1);
            transform:scale(1);
    -webkit-transition-property:opacity, -webkit-transform;
    transition-property:opacity, -webkit-transform;
    transition-property:opacity, transform;
    transition-property:opacity, transform, -webkit-transform;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
            transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
    -webkit-transition-delay:0;
            transition-delay:0; }
  .bp3-dialog-container.bp3-overlay-exit > .bp3-dialog{
    opacity:1;
    -webkit-transform:scale(1);
            transform:scale(1); }
  .bp3-dialog-container.bp3-overlay-exit-active > .bp3-dialog{
    opacity:0;
    -webkit-transform:scale(0.5);
            transform:scale(0.5);
    -webkit-transition-property:opacity, -webkit-transform;
    transition-property:opacity, -webkit-transform;
    transition-property:opacity, transform;
    transition-property:opacity, transform, -webkit-transform;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
            transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
    -webkit-transition-delay:0;
            transition-delay:0; }

.bp3-dialog{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  margin:30px 0;
  border-radius:6px;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
  background:#ebf1f5;
  width:500px;
  padding-bottom:20px;
  pointer-events:all;
  -webkit-user-select:text;
     -moz-user-select:text;
      -ms-user-select:text;
          user-select:text; }
  .bp3-dialog:focus{
    outline:0; }
  .bp3-dialog.bp3-dark,
  .bp3-dark .bp3-dialog{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
    background:#293742;
    color:#f5f8fa; }

.bp3-dialog-header{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  border-radius:6px 6px 0 0;
  -webkit-box-shadow:0 1px 0 rgba(16, 22, 26, 0.15);
          box-shadow:0 1px 0 rgba(16, 22, 26, 0.15);
  background:#ffffff;
  min-height:40px;
  padding-right:5px;
  padding-left:20px; }
  .bp3-dialog-header .bp3-icon-large,
  .bp3-dialog-header .bp3-icon{
    -webkit-box-flex:0;
        -ms-flex:0 0 auto;
            flex:0 0 auto;
    margin-right:10px;
    color:#5c7080; }
  .bp3-dialog-header .bp3-heading{
    overflow:hidden;
    text-overflow:ellipsis;
    white-space:nowrap;
    word-wrap:normal;
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto;
    margin:0;
    line-height:inherit; }
    .bp3-dialog-header .bp3-heading:last-child{
      margin-right:20px; }
  .bp3-dark .bp3-dialog-header{
    -webkit-box-shadow:0 1px 0 rgba(16, 22, 26, 0.4);
            box-shadow:0 1px 0 rgba(16, 22, 26, 0.4);
    background:#30404d; }
    .bp3-dark .bp3-dialog-header .bp3-icon-large,
    .bp3-dark .bp3-dialog-header .bp3-icon{
      color:#a7b6c2; }

.bp3-dialog-body{
  -webkit-box-flex:1;
      -ms-flex:1 1 auto;
          flex:1 1 auto;
  margin:20px;
  line-height:18px; }

.bp3-dialog-footer{
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  margin:0 20px; }

.bp3-dialog-footer-actions{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-pack:end;
      -ms-flex-pack:end;
          justify-content:flex-end; }
  .bp3-dialog-footer-actions .bp3-button{
    margin-left:10px; }
.bp3-drawer{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  margin:0;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
  background:#ffffff;
  padding:0; }
  .bp3-drawer:focus{
    outline:0; }
  .bp3-drawer.bp3-position-top{
    top:0;
    right:0;
    left:0;
    height:50%; }
    .bp3-drawer.bp3-position-top.bp3-overlay-enter, .bp3-drawer.bp3-position-top.bp3-overlay-appear{
      -webkit-transform:translateY(-100%);
              transform:translateY(-100%); }
    .bp3-drawer.bp3-position-top.bp3-overlay-enter-active, .bp3-drawer.bp3-position-top.bp3-overlay-appear-active{
      -webkit-transform:translateY(0);
              transform:translateY(0);
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-duration:200ms;
              transition-duration:200ms;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
      -webkit-transition-delay:0;
              transition-delay:0; }
    .bp3-drawer.bp3-position-top.bp3-overlay-exit{
      -webkit-transform:translateY(0);
              transform:translateY(0); }
    .bp3-drawer.bp3-position-top.bp3-overlay-exit-active{
      -webkit-transform:translateY(-100%);
              transform:translateY(-100%);
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-duration:100ms;
              transition-duration:100ms;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
      -webkit-transition-delay:0;
              transition-delay:0; }
  .bp3-drawer.bp3-position-bottom{
    right:0;
    bottom:0;
    left:0;
    height:50%; }
    .bp3-drawer.bp3-position-bottom.bp3-overlay-enter, .bp3-drawer.bp3-position-bottom.bp3-overlay-appear{
      -webkit-transform:translateY(100%);
              transform:translateY(100%); }
    .bp3-drawer.bp3-position-bottom.bp3-overlay-enter-active, .bp3-drawer.bp3-position-bottom.bp3-overlay-appear-active{
      -webkit-transform:translateY(0);
              transform:translateY(0);
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-duration:200ms;
              transition-duration:200ms;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
      -webkit-transition-delay:0;
              transition-delay:0; }
    .bp3-drawer.bp3-position-bottom.bp3-overlay-exit{
      -webkit-transform:translateY(0);
              transform:translateY(0); }
    .bp3-drawer.bp3-position-bottom.bp3-overlay-exit-active{
      -webkit-transform:translateY(100%);
              transform:translateY(100%);
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-duration:100ms;
              transition-duration:100ms;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
      -webkit-transition-delay:0;
              transition-delay:0; }
  .bp3-drawer.bp3-position-left{
    top:0;
    bottom:0;
    left:0;
    width:50%; }
    .bp3-drawer.bp3-position-left.bp3-overlay-enter, .bp3-drawer.bp3-position-left.bp3-overlay-appear{
      -webkit-transform:translateX(-100%);
              transform:translateX(-100%); }
    .bp3-drawer.bp3-position-left.bp3-overlay-enter-active, .bp3-drawer.bp3-position-left.bp3-overlay-appear-active{
      -webkit-transform:translateX(0);
              transform:translateX(0);
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-duration:200ms;
              transition-duration:200ms;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
      -webkit-transition-delay:0;
              transition-delay:0; }
    .bp3-drawer.bp3-position-left.bp3-overlay-exit{
      -webkit-transform:translateX(0);
              transform:translateX(0); }
    .bp3-drawer.bp3-position-left.bp3-overlay-exit-active{
      -webkit-transform:translateX(-100%);
              transform:translateX(-100%);
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-duration:100ms;
              transition-duration:100ms;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
      -webkit-transition-delay:0;
              transition-delay:0; }
  .bp3-drawer.bp3-position-right{
    top:0;
    right:0;
    bottom:0;
    width:50%; }
    .bp3-drawer.bp3-position-right.bp3-overlay-enter, .bp3-drawer.bp3-position-right.bp3-overlay-appear{
      -webkit-transform:translateX(100%);
              transform:translateX(100%); }
    .bp3-drawer.bp3-position-right.bp3-overlay-enter-active, .bp3-drawer.bp3-position-right.bp3-overlay-appear-active{
      -webkit-transform:translateX(0);
              transform:translateX(0);
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-duration:200ms;
              transition-duration:200ms;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
      -webkit-transition-delay:0;
              transition-delay:0; }
    .bp3-drawer.bp3-position-right.bp3-overlay-exit{
      -webkit-transform:translateX(0);
              transform:translateX(0); }
    .bp3-drawer.bp3-position-right.bp3-overlay-exit-active{
      -webkit-transform:translateX(100%);
              transform:translateX(100%);
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-duration:100ms;
              transition-duration:100ms;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
      -webkit-transition-delay:0;
              transition-delay:0; }
  .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
  .bp3-position-right):not(.bp3-vertical){
    top:0;
    right:0;
    bottom:0;
    width:50%; }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right):not(.bp3-vertical).bp3-overlay-enter, .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right):not(.bp3-vertical).bp3-overlay-appear{
      -webkit-transform:translateX(100%);
              transform:translateX(100%); }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right):not(.bp3-vertical).bp3-overlay-enter-active, .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right):not(.bp3-vertical).bp3-overlay-appear-active{
      -webkit-transform:translateX(0);
              transform:translateX(0);
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-duration:200ms;
              transition-duration:200ms;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
      -webkit-transition-delay:0;
              transition-delay:0; }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right):not(.bp3-vertical).bp3-overlay-exit{
      -webkit-transform:translateX(0);
              transform:translateX(0); }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right):not(.bp3-vertical).bp3-overlay-exit-active{
      -webkit-transform:translateX(100%);
              transform:translateX(100%);
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-duration:100ms;
              transition-duration:100ms;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
      -webkit-transition-delay:0;
              transition-delay:0; }
  .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
  .bp3-position-right).bp3-vertical{
    right:0;
    bottom:0;
    left:0;
    height:50%; }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right).bp3-vertical.bp3-overlay-enter, .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right).bp3-vertical.bp3-overlay-appear{
      -webkit-transform:translateY(100%);
              transform:translateY(100%); }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right).bp3-vertical.bp3-overlay-enter-active, .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right).bp3-vertical.bp3-overlay-appear-active{
      -webkit-transform:translateY(0);
              transform:translateY(0);
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-duration:200ms;
              transition-duration:200ms;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
      -webkit-transition-delay:0;
              transition-delay:0; }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right).bp3-vertical.bp3-overlay-exit{
      -webkit-transform:translateY(0);
              transform:translateY(0); }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right).bp3-vertical.bp3-overlay-exit-active{
      -webkit-transform:translateY(100%);
              transform:translateY(100%);
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-duration:100ms;
              transition-duration:100ms;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
      -webkit-transition-delay:0;
              transition-delay:0; }
  .bp3-drawer.bp3-dark,
  .bp3-dark .bp3-drawer{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
    background:#30404d;
    color:#f5f8fa; }

.bp3-drawer-header{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  position:relative;
  border-radius:0;
  -webkit-box-shadow:0 1px 0 rgba(16, 22, 26, 0.15);
          box-shadow:0 1px 0 rgba(16, 22, 26, 0.15);
  min-height:40px;
  padding:5px;
  padding-left:20px; }
  .bp3-drawer-header .bp3-icon-large,
  .bp3-drawer-header .bp3-icon{
    -webkit-box-flex:0;
        -ms-flex:0 0 auto;
            flex:0 0 auto;
    margin-right:10px;
    color:#5c7080; }
  .bp3-drawer-header .bp3-heading{
    overflow:hidden;
    text-overflow:ellipsis;
    white-space:nowrap;
    word-wrap:normal;
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto;
    margin:0;
    line-height:inherit; }
    .bp3-drawer-header .bp3-heading:last-child{
      margin-right:20px; }
  .bp3-dark .bp3-drawer-header{
    -webkit-box-shadow:0 1px 0 rgba(16, 22, 26, 0.4);
            box-shadow:0 1px 0 rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-drawer-header .bp3-icon-large,
    .bp3-dark .bp3-drawer-header .bp3-icon{
      color:#a7b6c2; }

.bp3-drawer-body{
  -webkit-box-flex:1;
      -ms-flex:1 1 auto;
          flex:1 1 auto;
  overflow:auto;
  line-height:18px; }

.bp3-drawer-footer{
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  position:relative;
  -webkit-box-shadow:inset 0 1px 0 rgba(16, 22, 26, 0.15);
          box-shadow:inset 0 1px 0 rgba(16, 22, 26, 0.15);
  padding:10px 20px; }
  .bp3-dark .bp3-drawer-footer{
    -webkit-box-shadow:inset 0 1px 0 rgba(16, 22, 26, 0.4);
            box-shadow:inset 0 1px 0 rgba(16, 22, 26, 0.4); }
.bp3-editable-text{
  display:inline-block;
  position:relative;
  cursor:text;
  max-width:100%;
  vertical-align:top;
  white-space:nowrap; }
  .bp3-editable-text::before{
    position:absolute;
    top:-3px;
    right:-3px;
    bottom:-3px;
    left:-3px;
    border-radius:3px;
    content:"";
    -webkit-transition:background-color 100ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:background-color 100ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:background-color 100ms cubic-bezier(0.4, 1, 0.75, 0.9), box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:background-color 100ms cubic-bezier(0.4, 1, 0.75, 0.9), box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-editable-text:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.15);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.15); }
  .bp3-editable-text.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
    background-color:#ffffff; }
  .bp3-editable-text.bp3-disabled::before{
    -webkit-box-shadow:none;
            box-shadow:none; }
  .bp3-editable-text.bp3-intent-primary .bp3-editable-text-input,
  .bp3-editable-text.bp3-intent-primary .bp3-editable-text-content{
    color:#137cbd; }
  .bp3-editable-text.bp3-intent-primary:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(19, 124, 189, 0.4);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(19, 124, 189, 0.4); }
  .bp3-editable-text.bp3-intent-primary.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-editable-text.bp3-intent-success .bp3-editable-text-input,
  .bp3-editable-text.bp3-intent-success .bp3-editable-text-content{
    color:#0f9960; }
  .bp3-editable-text.bp3-intent-success:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px rgba(15, 153, 96, 0.4);
            box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px rgba(15, 153, 96, 0.4); }
  .bp3-editable-text.bp3-intent-success.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-editable-text.bp3-intent-warning .bp3-editable-text-input,
  .bp3-editable-text.bp3-intent-warning .bp3-editable-text-content{
    color:#d9822b; }
  .bp3-editable-text.bp3-intent-warning:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px rgba(217, 130, 43, 0.4);
            box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px rgba(217, 130, 43, 0.4); }
  .bp3-editable-text.bp3-intent-warning.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-editable-text.bp3-intent-danger .bp3-editable-text-input,
  .bp3-editable-text.bp3-intent-danger .bp3-editable-text-content{
    color:#db3737; }
  .bp3-editable-text.bp3-intent-danger:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px rgba(219, 55, 55, 0.4);
            box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px rgba(219, 55, 55, 0.4); }
  .bp3-editable-text.bp3-intent-danger.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-dark .bp3-editable-text:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(255, 255, 255, 0.15);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(255, 255, 255, 0.15); }
  .bp3-dark .bp3-editable-text.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
    background-color:rgba(16, 22, 26, 0.3); }
  .bp3-dark .bp3-editable-text.bp3-disabled::before{
    -webkit-box-shadow:none;
            box-shadow:none; }
  .bp3-dark .bp3-editable-text.bp3-intent-primary .bp3-editable-text-content{
    color:#48aff0; }
  .bp3-dark .bp3-editable-text.bp3-intent-primary:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(72, 175, 240, 0), 0 0 0 0 rgba(72, 175, 240, 0), inset 0 0 0 1px rgba(72, 175, 240, 0.4);
            box-shadow:0 0 0 0 rgba(72, 175, 240, 0), 0 0 0 0 rgba(72, 175, 240, 0), inset 0 0 0 1px rgba(72, 175, 240, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-primary.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #48aff0, 0 0 0 3px rgba(72, 175, 240, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px #48aff0, 0 0 0 3px rgba(72, 175, 240, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-success .bp3-editable-text-content{
    color:#3dcc91; }
  .bp3-dark .bp3-editable-text.bp3-intent-success:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(61, 204, 145, 0), 0 0 0 0 rgba(61, 204, 145, 0), inset 0 0 0 1px rgba(61, 204, 145, 0.4);
            box-shadow:0 0 0 0 rgba(61, 204, 145, 0), 0 0 0 0 rgba(61, 204, 145, 0), inset 0 0 0 1px rgba(61, 204, 145, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-success.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #3dcc91, 0 0 0 3px rgba(61, 204, 145, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px #3dcc91, 0 0 0 3px rgba(61, 204, 145, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-warning .bp3-editable-text-content{
    color:#ffb366; }
  .bp3-dark .bp3-editable-text.bp3-intent-warning:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(255, 179, 102, 0), 0 0 0 0 rgba(255, 179, 102, 0), inset 0 0 0 1px rgba(255, 179, 102, 0.4);
            box-shadow:0 0 0 0 rgba(255, 179, 102, 0), 0 0 0 0 rgba(255, 179, 102, 0), inset 0 0 0 1px rgba(255, 179, 102, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-warning.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #ffb366, 0 0 0 3px rgba(255, 179, 102, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px #ffb366, 0 0 0 3px rgba(255, 179, 102, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-danger .bp3-editable-text-content{
    color:#ff7373; }
  .bp3-dark .bp3-editable-text.bp3-intent-danger:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(255, 115, 115, 0), 0 0 0 0 rgba(255, 115, 115, 0), inset 0 0 0 1px rgba(255, 115, 115, 0.4);
            box-shadow:0 0 0 0 rgba(255, 115, 115, 0), 0 0 0 0 rgba(255, 115, 115, 0), inset 0 0 0 1px rgba(255, 115, 115, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-danger.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #ff7373, 0 0 0 3px rgba(255, 115, 115, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px #ff7373, 0 0 0 3px rgba(255, 115, 115, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }

.bp3-editable-text-input,
.bp3-editable-text-content{
  display:inherit;
  position:relative;
  min-width:inherit;
  max-width:inherit;
  vertical-align:top;
  text-transform:inherit;
  letter-spacing:inherit;
  color:inherit;
  font:inherit;
  resize:none; }

.bp3-editable-text-input{
  border:none;
  -webkit-box-shadow:none;
          box-shadow:none;
  background:none;
  width:100%;
  padding:0;
  white-space:pre-wrap; }
  .bp3-editable-text-input::-webkit-input-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-editable-text-input::-moz-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-editable-text-input:-ms-input-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-editable-text-input::-ms-input-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-editable-text-input::placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-editable-text-input:focus{
    outline:none; }
  .bp3-editable-text-input::-ms-clear{
    display:none; }

.bp3-editable-text-content{
  overflow:hidden;
  padding-right:2px;
  text-overflow:ellipsis;
  white-space:pre; }
  .bp3-editable-text-editing > .bp3-editable-text-content{
    position:absolute;
    left:0;
    visibility:hidden; }
  .bp3-editable-text-placeholder > .bp3-editable-text-content{
    color:rgba(92, 112, 128, 0.6); }
    .bp3-dark .bp3-editable-text-placeholder > .bp3-editable-text-content{
      color:rgba(167, 182, 194, 0.6); }

.bp3-editable-text.bp3-multiline{
  display:block; }
  .bp3-editable-text.bp3-multiline .bp3-editable-text-content{
    overflow:auto;
    white-space:pre-wrap;
    word-wrap:break-word; }
.bp3-control-group{
  -webkit-transform:translateZ(0);
          transform:translateZ(0);
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:stretch;
      -ms-flex-align:stretch;
          align-items:stretch; }
  .bp3-control-group > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-control-group > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-control-group .bp3-button,
  .bp3-control-group .bp3-html-select,
  .bp3-control-group .bp3-input,
  .bp3-control-group .bp3-select{
    position:relative; }
  .bp3-control-group .bp3-input{
    z-index:2;
    border-radius:inherit; }
    .bp3-control-group .bp3-input:focus{
      z-index:14;
      border-radius:3px; }
    .bp3-control-group .bp3-input[class*="bp3-intent"]{
      z-index:13; }
      .bp3-control-group .bp3-input[class*="bp3-intent"]:focus{
        z-index:15; }
    .bp3-control-group .bp3-input[readonly], .bp3-control-group .bp3-input:disabled, .bp3-control-group .bp3-input.bp3-disabled{
      z-index:1; }
  .bp3-control-group .bp3-input-group[class*="bp3-intent"] .bp3-input{
    z-index:13; }
    .bp3-control-group .bp3-input-group[class*="bp3-intent"] .bp3-input:focus{
      z-index:15; }
  .bp3-control-group .bp3-button,
  .bp3-control-group .bp3-html-select select,
  .bp3-control-group .bp3-select select{
    -webkit-transform:translateZ(0);
            transform:translateZ(0);
    z-index:4;
    border-radius:inherit; }
    .bp3-control-group .bp3-button:focus,
    .bp3-control-group .bp3-html-select select:focus,
    .bp3-control-group .bp3-select select:focus{
      z-index:5; }
    .bp3-control-group .bp3-button:hover,
    .bp3-control-group .bp3-html-select select:hover,
    .bp3-control-group .bp3-select select:hover{
      z-index:6; }
    .bp3-control-group .bp3-button:active,
    .bp3-control-group .bp3-html-select select:active,
    .bp3-control-group .bp3-select select:active{
      z-index:7; }
    .bp3-control-group .bp3-button[readonly], .bp3-control-group .bp3-button:disabled, .bp3-control-group .bp3-button.bp3-disabled,
    .bp3-control-group .bp3-html-select select[readonly],
    .bp3-control-group .bp3-html-select select:disabled,
    .bp3-control-group .bp3-html-select select.bp3-disabled,
    .bp3-control-group .bp3-select select[readonly],
    .bp3-control-group .bp3-select select:disabled,
    .bp3-control-group .bp3-select select.bp3-disabled{
      z-index:3; }
    .bp3-control-group .bp3-button[class*="bp3-intent"],
    .bp3-control-group .bp3-html-select select[class*="bp3-intent"],
    .bp3-control-group .bp3-select select[class*="bp3-intent"]{
      z-index:9; }
      .bp3-control-group .bp3-button[class*="bp3-intent"]:focus,
      .bp3-control-group .bp3-html-select select[class*="bp3-intent"]:focus,
      .bp3-control-group .bp3-select select[class*="bp3-intent"]:focus{
        z-index:10; }
      .bp3-control-group .bp3-button[class*="bp3-intent"]:hover,
      .bp3-control-group .bp3-html-select select[class*="bp3-intent"]:hover,
      .bp3-control-group .bp3-select select[class*="bp3-intent"]:hover{
        z-index:11; }
      .bp3-control-group .bp3-button[class*="bp3-intent"]:active,
      .bp3-control-group .bp3-html-select select[class*="bp3-intent"]:active,
      .bp3-control-group .bp3-select select[class*="bp3-intent"]:active{
        z-index:12; }
      .bp3-control-group .bp3-button[class*="bp3-intent"][readonly], .bp3-control-group .bp3-button[class*="bp3-intent"]:disabled, .bp3-control-group .bp3-button[class*="bp3-intent"].bp3-disabled,
      .bp3-control-group .bp3-html-select select[class*="bp3-intent"][readonly],
      .bp3-control-group .bp3-html-select select[class*="bp3-intent"]:disabled,
      .bp3-control-group .bp3-html-select select[class*="bp3-intent"].bp3-disabled,
      .bp3-control-group .bp3-select select[class*="bp3-intent"][readonly],
      .bp3-control-group .bp3-select select[class*="bp3-intent"]:disabled,
      .bp3-control-group .bp3-select select[class*="bp3-intent"].bp3-disabled{
        z-index:8; }
  .bp3-control-group .bp3-input-group > .bp3-icon,
  .bp3-control-group .bp3-input-group > .bp3-button,
  .bp3-control-group .bp3-input-group > .bp3-input-action{
    z-index:16; }
  .bp3-control-group .bp3-select::after,
  .bp3-control-group .bp3-html-select::after,
  .bp3-control-group .bp3-select > .bp3-icon,
  .bp3-control-group .bp3-html-select > .bp3-icon{
    z-index:17; }
  .bp3-control-group:not(.bp3-vertical) > *{
    margin-right:-1px; }
  .bp3-dark .bp3-control-group:not(.bp3-vertical) > *{
    margin-right:0; }
  .bp3-dark .bp3-control-group:not(.bp3-vertical) > .bp3-button + .bp3-button{
    margin-left:1px; }
  .bp3-control-group .bp3-popover-wrapper,
  .bp3-control-group .bp3-popover-target{
    border-radius:inherit; }
  .bp3-control-group > :first-child{
    border-radius:3px 0 0 3px; }
  .bp3-control-group > :last-child{
    margin-right:0;
    border-radius:0 3px 3px 0; }
  .bp3-control-group > :only-child{
    margin-right:0;
    border-radius:3px; }
  .bp3-control-group .bp3-input-group .bp3-button{
    border-radius:3px; }
  .bp3-control-group > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto; }
  .bp3-control-group.bp3-fill > *:not(.bp3-fixed){
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto; }
  .bp3-control-group.bp3-vertical{
    -webkit-box-orient:vertical;
    -webkit-box-direction:normal;
        -ms-flex-direction:column;
            flex-direction:column; }
    .bp3-control-group.bp3-vertical > *{
      margin-top:-1px; }
    .bp3-control-group.bp3-vertical > :first-child{
      margin-top:0;
      border-radius:3px 3px 0 0; }
    .bp3-control-group.bp3-vertical > :last-child{
      border-radius:0 0 3px 3px; }
.bp3-control{
  display:block;
  position:relative;
  margin-bottom:10px;
  cursor:pointer;
  text-transform:none; }
  .bp3-control input:checked ~ .bp3-control-indicator{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    background-color:#137cbd;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.1)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0));
    color:#ffffff; }
  .bp3-control:hover input:checked ~ .bp3-control-indicator{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    background-color:#106ba3; }
  .bp3-control input:not(:disabled):active:checked ~ .bp3-control-indicator{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
    background:#0e5a8a; }
  .bp3-control input:disabled:checked ~ .bp3-control-indicator{
    -webkit-box-shadow:none;
            box-shadow:none;
    background:rgba(19, 124, 189, 0.5); }
  .bp3-dark .bp3-control input:checked ~ .bp3-control-indicator{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-control:hover input:checked ~ .bp3-control-indicator{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
    background-color:#106ba3; }
  .bp3-dark .bp3-control input:not(:disabled):active:checked ~ .bp3-control-indicator{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
    background-color:#0e5a8a; }
  .bp3-dark .bp3-control input:disabled:checked ~ .bp3-control-indicator{
    -webkit-box-shadow:none;
            box-shadow:none;
    background:rgba(14, 90, 138, 0.5); }
  .bp3-control:not(.bp3-align-right){
    padding-left:26px; }
    .bp3-control:not(.bp3-align-right) .bp3-control-indicator{
      margin-left:-26px; }
  .bp3-control.bp3-align-right{
    padding-right:26px; }
    .bp3-control.bp3-align-right .bp3-control-indicator{
      margin-right:-26px; }
  .bp3-control.bp3-disabled{
    cursor:not-allowed;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-control.bp3-inline{
    display:inline-block;
    margin-right:20px; }
  .bp3-control input{
    position:absolute;
    top:0;
    left:0;
    opacity:0;
    z-index:-1; }
  .bp3-control .bp3-control-indicator{
    display:inline-block;
    position:relative;
    margin-top:-3px;
    margin-right:10px;
    border:none;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
    background-clip:padding-box;
    background-color:#f5f8fa;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.8)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.8), rgba(255, 255, 255, 0));
    cursor:pointer;
    width:1em;
    height:1em;
    vertical-align:middle;
    font-size:16px;
    -webkit-user-select:none;
       -moz-user-select:none;
        -ms-user-select:none;
            user-select:none; }
    .bp3-control .bp3-control-indicator::before{
      display:block;
      width:1em;
      height:1em;
      content:""; }
  .bp3-control:hover .bp3-control-indicator{
    background-color:#ebf1f5; }
  .bp3-control input:not(:disabled):active ~ .bp3-control-indicator{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
    background:#d8e1e8; }
  .bp3-control input:disabled ~ .bp3-control-indicator{
    -webkit-box-shadow:none;
            box-shadow:none;
    background:rgba(206, 217, 224, 0.5);
    cursor:not-allowed; }
  .bp3-control input:focus ~ .bp3-control-indicator{
    outline:rgba(19, 124, 189, 0.6) auto 2px;
    outline-offset:2px;
    -moz-outline-radius:6px; }
  .bp3-control.bp3-align-right .bp3-control-indicator{
    float:right;
    margin-top:1px;
    margin-left:10px; }
  .bp3-control.bp3-large{
    font-size:16px; }
    .bp3-control.bp3-large:not(.bp3-align-right){
      padding-left:30px; }
      .bp3-control.bp3-large:not(.bp3-align-right) .bp3-control-indicator{
        margin-left:-30px; }
    .bp3-control.bp3-large.bp3-align-right{
      padding-right:30px; }
      .bp3-control.bp3-large.bp3-align-right .bp3-control-indicator{
        margin-right:-30px; }
    .bp3-control.bp3-large .bp3-control-indicator{
      font-size:20px; }
    .bp3-control.bp3-large.bp3-align-right .bp3-control-indicator{
      margin-top:0; }
  .bp3-control.bp3-checkbox input:indeterminate ~ .bp3-control-indicator{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    background-color:#137cbd;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.1)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0));
    color:#ffffff; }
  .bp3-control.bp3-checkbox:hover input:indeterminate ~ .bp3-control-indicator{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    background-color:#106ba3; }
  .bp3-control.bp3-checkbox input:not(:disabled):active:indeterminate ~ .bp3-control-indicator{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
    background:#0e5a8a; }
  .bp3-control.bp3-checkbox input:disabled:indeterminate ~ .bp3-control-indicator{
    -webkit-box-shadow:none;
            box-shadow:none;
    background:rgba(19, 124, 189, 0.5); }
  .bp3-dark .bp3-control.bp3-checkbox input:indeterminate ~ .bp3-control-indicator{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-control.bp3-checkbox:hover input:indeterminate ~ .bp3-control-indicator{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
    background-color:#106ba3; }
  .bp3-dark .bp3-control.bp3-checkbox input:not(:disabled):active:indeterminate ~ .bp3-control-indicator{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
    background-color:#0e5a8a; }
  .bp3-dark .bp3-control.bp3-checkbox input:disabled:indeterminate ~ .bp3-control-indicator{
    -webkit-box-shadow:none;
            box-shadow:none;
    background:rgba(14, 90, 138, 0.5); }
  .bp3-control.bp3-checkbox .bp3-control-indicator{
    border-radius:3px; }
  .bp3-control.bp3-checkbox input:checked ~ .bp3-control-indicator::before{
    background-image:url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 16 16'%3e%3cpath fill-rule='evenodd' clip-rule='evenodd' d='M12 5c-.28 0-.53.11-.71.29L7 9.59l-2.29-2.3a1.003 1.003 0 0 0-1.42 1.42l3 3c.18.18.43.29.71.29s.53-.11.71-.29l5-5A1.003 1.003 0 0 0 12 5z' fill='white'/%3e%3c/svg%3e"); }
  .bp3-control.bp3-checkbox input:indeterminate ~ .bp3-control-indicator::before{
    background-image:url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 16 16'%3e%3cpath fill-rule='evenodd' clip-rule='evenodd' d='M11 7H5c-.55 0-1 .45-1 1s.45 1 1 1h6c.55 0 1-.45 1-1s-.45-1-1-1z' fill='white'/%3e%3c/svg%3e"); }
  .bp3-control.bp3-radio .bp3-control-indicator{
    border-radius:50%; }
  .bp3-control.bp3-radio input:checked ~ .bp3-control-indicator::before{
    background-image:radial-gradient(#ffffff, #ffffff 28%, transparent 32%); }
  .bp3-control.bp3-radio input:checked:disabled ~ .bp3-control-indicator::before{
    opacity:0.5; }
  .bp3-control.bp3-radio input:focus ~ .bp3-control-indicator{
    -moz-outline-radius:16px; }
  .bp3-control.bp3-switch input ~ .bp3-control-indicator{
    background:rgba(167, 182, 194, 0.5); }
  .bp3-control.bp3-switch:hover input ~ .bp3-control-indicator{
    background:rgba(115, 134, 148, 0.5); }
  .bp3-control.bp3-switch input:not(:disabled):active ~ .bp3-control-indicator{
    background:rgba(92, 112, 128, 0.5); }
  .bp3-control.bp3-switch input:disabled ~ .bp3-control-indicator{
    background:rgba(206, 217, 224, 0.5); }
    .bp3-control.bp3-switch input:disabled ~ .bp3-control-indicator::before{
      background:rgba(255, 255, 255, 0.8); }
  .bp3-control.bp3-switch input:checked ~ .bp3-control-indicator{
    background:#137cbd; }
  .bp3-control.bp3-switch:hover input:checked ~ .bp3-control-indicator{
    background:#106ba3; }
  .bp3-control.bp3-switch input:checked:not(:disabled):active ~ .bp3-control-indicator{
    background:#0e5a8a; }
  .bp3-control.bp3-switch input:checked:disabled ~ .bp3-control-indicator{
    background:rgba(19, 124, 189, 0.5); }
    .bp3-control.bp3-switch input:checked:disabled ~ .bp3-control-indicator::before{
      background:rgba(255, 255, 255, 0.8); }
  .bp3-control.bp3-switch:not(.bp3-align-right){
    padding-left:38px; }
    .bp3-control.bp3-switch:not(.bp3-align-right) .bp3-control-indicator{
      margin-left:-38px; }
  .bp3-control.bp3-switch.bp3-align-right{
    padding-right:38px; }
    .bp3-control.bp3-switch.bp3-align-right .bp3-control-indicator{
      margin-right:-38px; }
  .bp3-control.bp3-switch .bp3-control-indicator{
    border:none;
    border-radius:1.75em;
    -webkit-box-shadow:none !important;
            box-shadow:none !important;
    width:auto;
    min-width:1.75em;
    -webkit-transition:background-color 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:background-color 100ms cubic-bezier(0.4, 1, 0.75, 0.9); }
    .bp3-control.bp3-switch .bp3-control-indicator::before{
      position:absolute;
      left:0;
      margin:2px;
      border-radius:50%;
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.2);
      background:#ffffff;
      width:calc(1em - 4px);
      height:calc(1em - 4px);
      -webkit-transition:left 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
      transition:left 100ms cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-control.bp3-switch input:checked ~ .bp3-control-indicator::before{
    left:calc(100% - 1em); }
  .bp3-control.bp3-switch.bp3-large:not(.bp3-align-right){
    padding-left:45px; }
    .bp3-control.bp3-switch.bp3-large:not(.bp3-align-right) .bp3-control-indicator{
      margin-left:-45px; }
  .bp3-control.bp3-switch.bp3-large.bp3-align-right{
    padding-right:45px; }
    .bp3-control.bp3-switch.bp3-large.bp3-align-right .bp3-control-indicator{
      margin-right:-45px; }
  .bp3-dark .bp3-control.bp3-switch input ~ .bp3-control-indicator{
    background:rgba(16, 22, 26, 0.5); }
  .bp3-dark .bp3-control.bp3-switch:hover input ~ .bp3-control-indicator{
    background:rgba(16, 22, 26, 0.7); }
  .bp3-dark .bp3-control.bp3-switch input:not(:disabled):active ~ .bp3-control-indicator{
    background:rgba(16, 22, 26, 0.9); }
  .bp3-dark .bp3-control.bp3-switch input:disabled ~ .bp3-control-indicator{
    background:rgba(57, 75, 89, 0.5); }
    .bp3-dark .bp3-control.bp3-switch input:disabled ~ .bp3-control-indicator::before{
      background:rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-control.bp3-switch input:checked ~ .bp3-control-indicator{
    background:#137cbd; }
  .bp3-dark .bp3-control.bp3-switch:hover input:checked ~ .bp3-control-indicator{
    background:#106ba3; }
  .bp3-dark .bp3-control.bp3-switch input:checked:not(:disabled):active ~ .bp3-control-indicator{
    background:#0e5a8a; }
  .bp3-dark .bp3-control.bp3-switch input:checked:disabled ~ .bp3-control-indicator{
    background:rgba(14, 90, 138, 0.5); }
    .bp3-dark .bp3-control.bp3-switch input:checked:disabled ~ .bp3-control-indicator::before{
      background:rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-control.bp3-switch .bp3-control-indicator::before{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
    background:#394b59; }
  .bp3-dark .bp3-control.bp3-switch input:checked ~ .bp3-control-indicator::before{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4); }
  .bp3-control.bp3-switch .bp3-switch-inner-text{
    text-align:center;
    font-size:0.7em; }
  .bp3-control.bp3-switch .bp3-control-indicator-child:first-child{
    visibility:hidden;
    margin-right:1.2em;
    margin-left:0.5em;
    line-height:0; }
  .bp3-control.bp3-switch .bp3-control-indicator-child:last-child{
    visibility:visible;
    margin-right:0.5em;
    margin-left:1.2em;
    line-height:1em; }
  .bp3-control.bp3-switch input:checked ~ .bp3-control-indicator .bp3-control-indicator-child:first-child{
    visibility:visible;
    line-height:1em; }
  .bp3-control.bp3-switch input:checked ~ .bp3-control-indicator .bp3-control-indicator-child:last-child{
    visibility:hidden;
    line-height:0; }
  .bp3-dark .bp3-control{
    color:#f5f8fa; }
    .bp3-dark .bp3-control.bp3-disabled{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-control .bp3-control-indicator{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
      background-color:#394b59;
      background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.05)), to(rgba(255, 255, 255, 0)));
      background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.05), rgba(255, 255, 255, 0)); }
    .bp3-dark .bp3-control:hover .bp3-control-indicator{
      background-color:#30404d; }
    .bp3-dark .bp3-control input:not(:disabled):active ~ .bp3-control-indicator{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
      background:#202b33; }
    .bp3-dark .bp3-control input:disabled ~ .bp3-control-indicator{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:rgba(57, 75, 89, 0.5);
      cursor:not-allowed; }
    .bp3-dark .bp3-control.bp3-checkbox input:disabled:checked ~ .bp3-control-indicator, .bp3-dark .bp3-control.bp3-checkbox input:disabled:indeterminate ~ .bp3-control-indicator{
      color:rgba(167, 182, 194, 0.6); }
.bp3-file-input{
  display:inline-block;
  position:relative;
  cursor:pointer;
  height:30px; }
  .bp3-file-input input{
    opacity:0;
    margin:0;
    min-width:200px; }
    .bp3-file-input input:disabled + .bp3-file-upload-input,
    .bp3-file-input input.bp3-disabled + .bp3-file-upload-input{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:rgba(206, 217, 224, 0.5);
      cursor:not-allowed;
      color:rgba(92, 112, 128, 0.6);
      resize:none; }
      .bp3-file-input input:disabled + .bp3-file-upload-input::after,
      .bp3-file-input input.bp3-disabled + .bp3-file-upload-input::after{
        outline:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        background-color:rgba(206, 217, 224, 0.5);
        background-image:none;
        cursor:not-allowed;
        color:rgba(92, 112, 128, 0.6); }
        .bp3-file-input input:disabled + .bp3-file-upload-input::after.bp3-active, .bp3-file-input input:disabled + .bp3-file-upload-input::after.bp3-active:hover,
        .bp3-file-input input.bp3-disabled + .bp3-file-upload-input::after.bp3-active,
        .bp3-file-input input.bp3-disabled + .bp3-file-upload-input::after.bp3-active:hover{
          background:rgba(206, 217, 224, 0.7); }
      .bp3-dark .bp3-file-input input:disabled + .bp3-file-upload-input, .bp3-dark
      .bp3-file-input input.bp3-disabled + .bp3-file-upload-input{
        -webkit-box-shadow:none;
                box-shadow:none;
        background:rgba(57, 75, 89, 0.5);
        color:rgba(167, 182, 194, 0.6); }
        .bp3-dark .bp3-file-input input:disabled + .bp3-file-upload-input::after, .bp3-dark
        .bp3-file-input input.bp3-disabled + .bp3-file-upload-input::after{
          -webkit-box-shadow:none;
                  box-shadow:none;
          background-color:rgba(57, 75, 89, 0.5);
          background-image:none;
          color:rgba(167, 182, 194, 0.6); }
          .bp3-dark .bp3-file-input input:disabled + .bp3-file-upload-input::after.bp3-active, .bp3-dark
          .bp3-file-input input.bp3-disabled + .bp3-file-upload-input::after.bp3-active{
            background:rgba(57, 75, 89, 0.7); }
  .bp3-file-input.bp3-file-input-has-selection .bp3-file-upload-input{
    color:#182026; }
  .bp3-dark .bp3-file-input.bp3-file-input-has-selection .bp3-file-upload-input{
    color:#f5f8fa; }
  .bp3-file-input.bp3-fill{
    width:100%; }
  .bp3-file-input.bp3-large,
  .bp3-large .bp3-file-input{
    height:40px; }
  .bp3-file-input .bp3-file-upload-input-custom-text::after{
    content:attr(bp3-button-text); }

.bp3-file-upload-input{
  outline:none;
  border:none;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
  background:#ffffff;
  height:30px;
  padding:0 10px;
  vertical-align:middle;
  line-height:30px;
  color:#182026;
  font-size:14px;
  font-weight:400;
  -webkit-transition:-webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:-webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  -webkit-appearance:none;
     -moz-appearance:none;
          appearance:none;
  overflow:hidden;
  text-overflow:ellipsis;
  white-space:nowrap;
  word-wrap:normal;
  position:absolute;
  top:0;
  right:0;
  left:0;
  padding-right:80px;
  color:rgba(92, 112, 128, 0.6);
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-file-upload-input::-webkit-input-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-file-upload-input::-moz-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-file-upload-input:-ms-input-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-file-upload-input::-ms-input-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-file-upload-input::placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-file-upload-input:focus, .bp3-file-upload-input.bp3-active{
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-file-upload-input[type="search"], .bp3-file-upload-input.bp3-round{
    border-radius:30px;
    -webkit-box-sizing:border-box;
            box-sizing:border-box;
    padding-left:10px; }
  .bp3-file-upload-input[readonly]{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.15);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.15); }
  .bp3-file-upload-input:disabled, .bp3-file-upload-input.bp3-disabled{
    -webkit-box-shadow:none;
            box-shadow:none;
    background:rgba(206, 217, 224, 0.5);
    cursor:not-allowed;
    color:rgba(92, 112, 128, 0.6);
    resize:none; }
  .bp3-file-upload-input::after{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
    background-color:#f5f8fa;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.8)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.8), rgba(255, 255, 255, 0));
    color:#182026;
    min-width:24px;
    min-height:24px;
    overflow:hidden;
    text-overflow:ellipsis;
    white-space:nowrap;
    word-wrap:normal;
    position:absolute;
    top:0;
    right:0;
    margin:3px;
    border-radius:3px;
    width:70px;
    text-align:center;
    line-height:24px;
    content:"Browse"; }
    .bp3-file-upload-input::after:hover{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
      background-clip:padding-box;
      background-color:#ebf1f5; }
    .bp3-file-upload-input::after:active, .bp3-file-upload-input::after.bp3-active{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
      background-color:#d8e1e8;
      background-image:none; }
    .bp3-file-upload-input::after:disabled, .bp3-file-upload-input::after.bp3-disabled{
      outline:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      background-color:rgba(206, 217, 224, 0.5);
      background-image:none;
      cursor:not-allowed;
      color:rgba(92, 112, 128, 0.6); }
      .bp3-file-upload-input::after:disabled.bp3-active, .bp3-file-upload-input::after:disabled.bp3-active:hover, .bp3-file-upload-input::after.bp3-disabled.bp3-active, .bp3-file-upload-input::after.bp3-disabled.bp3-active:hover{
        background:rgba(206, 217, 224, 0.7); }
  .bp3-file-upload-input:hover::after{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
    background-clip:padding-box;
    background-color:#ebf1f5; }
  .bp3-file-upload-input:active::after{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
    background-color:#d8e1e8;
    background-image:none; }
  .bp3-large .bp3-file-upload-input{
    height:40px;
    line-height:40px;
    font-size:16px;
    padding-right:95px; }
    .bp3-large .bp3-file-upload-input[type="search"], .bp3-large .bp3-file-upload-input.bp3-round{
      padding:0 15px; }
    .bp3-large .bp3-file-upload-input::after{
      min-width:30px;
      min-height:30px;
      margin:5px;
      width:85px;
      line-height:30px; }
  .bp3-dark .bp3-file-upload-input{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
    background:rgba(16, 22, 26, 0.3);
    color:#f5f8fa;
    color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input::-webkit-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input::-moz-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input:-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input::-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input::placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input:focus{
      -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-file-upload-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-file-upload-input:disabled, .bp3-dark .bp3-file-upload-input.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:rgba(57, 75, 89, 0.5);
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input::after{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
      background-color:#394b59;
      background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.05)), to(rgba(255, 255, 255, 0)));
      background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.05), rgba(255, 255, 255, 0));
      color:#f5f8fa; }
      .bp3-dark .bp3-file-upload-input::after:hover, .bp3-dark .bp3-file-upload-input::after:active, .bp3-dark .bp3-file-upload-input::after.bp3-active{
        color:#f5f8fa; }
      .bp3-dark .bp3-file-upload-input::after:hover{
        -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
                box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
        background-color:#30404d; }
      .bp3-dark .bp3-file-upload-input::after:active, .bp3-dark .bp3-file-upload-input::after.bp3-active{
        -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
                box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
        background-color:#202b33;
        background-image:none; }
      .bp3-dark .bp3-file-upload-input::after:disabled, .bp3-dark .bp3-file-upload-input::after.bp3-disabled{
        -webkit-box-shadow:none;
                box-shadow:none;
        background-color:rgba(57, 75, 89, 0.5);
        background-image:none;
        color:rgba(167, 182, 194, 0.6); }
        .bp3-dark .bp3-file-upload-input::after:disabled.bp3-active, .bp3-dark .bp3-file-upload-input::after.bp3-disabled.bp3-active{
          background:rgba(57, 75, 89, 0.7); }
      .bp3-dark .bp3-file-upload-input::after .bp3-button-spinner .bp3-spinner-head{
        background:rgba(16, 22, 26, 0.5);
        stroke:#8a9ba8; }
    .bp3-dark .bp3-file-upload-input:hover::after{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
      background-color:#30404d; }
    .bp3-dark .bp3-file-upload-input:active::after{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
      background-color:#202b33;
      background-image:none; }

.bp3-file-upload-input::after{
  -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
          box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1); }
.bp3-form-group{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  margin:0 0 15px; }
  .bp3-form-group label.bp3-label{
    margin-bottom:5px; }
  .bp3-form-group .bp3-control{
    margin-top:7px; }
  .bp3-form-group .bp3-form-helper-text{
    margin-top:5px;
    color:#5c7080;
    font-size:12px; }
  .bp3-form-group.bp3-intent-primary .bp3-form-helper-text{
    color:#106ba3; }
  .bp3-form-group.bp3-intent-success .bp3-form-helper-text{
    color:#0d8050; }
  .bp3-form-group.bp3-intent-warning .bp3-form-helper-text{
    color:#bf7326; }
  .bp3-form-group.bp3-intent-danger .bp3-form-helper-text{
    color:#c23030; }
  .bp3-form-group.bp3-inline{
    -webkit-box-orient:horizontal;
    -webkit-box-direction:normal;
        -ms-flex-direction:row;
            flex-direction:row;
    -webkit-box-align:start;
        -ms-flex-align:start;
            align-items:flex-start; }
    .bp3-form-group.bp3-inline.bp3-large label.bp3-label{
      margin:0 10px 0 0;
      line-height:40px; }
    .bp3-form-group.bp3-inline label.bp3-label{
      margin:0 10px 0 0;
      line-height:30px; }
  .bp3-form-group.bp3-disabled .bp3-label,
  .bp3-form-group.bp3-disabled .bp3-text-muted,
  .bp3-form-group.bp3-disabled .bp3-form-helper-text{
    color:rgba(92, 112, 128, 0.6) !important; }
  .bp3-dark .bp3-form-group.bp3-intent-primary .bp3-form-helper-text{
    color:#48aff0; }
  .bp3-dark .bp3-form-group.bp3-intent-success .bp3-form-helper-text{
    color:#3dcc91; }
  .bp3-dark .bp3-form-group.bp3-intent-warning .bp3-form-helper-text{
    color:#ffb366; }
  .bp3-dark .bp3-form-group.bp3-intent-danger .bp3-form-helper-text{
    color:#ff7373; }
  .bp3-dark .bp3-form-group .bp3-form-helper-text{
    color:#a7b6c2; }
  .bp3-dark .bp3-form-group.bp3-disabled .bp3-label,
  .bp3-dark .bp3-form-group.bp3-disabled .bp3-text-muted,
  .bp3-dark .bp3-form-group.bp3-disabled .bp3-form-helper-text{
    color:rgba(167, 182, 194, 0.6) !important; }
.bp3-input-group{
  display:block;
  position:relative; }
  .bp3-input-group .bp3-input{
    position:relative;
    width:100%; }
    .bp3-input-group .bp3-input:not(:first-child){
      padding-left:30px; }
    .bp3-input-group .bp3-input:not(:last-child){
      padding-right:30px; }
  .bp3-input-group .bp3-input-action,
  .bp3-input-group > .bp3-button,
  .bp3-input-group > .bp3-icon{
    position:absolute;
    top:0; }
    .bp3-input-group .bp3-input-action:first-child,
    .bp3-input-group > .bp3-button:first-child,
    .bp3-input-group > .bp3-icon:first-child{
      left:0; }
    .bp3-input-group .bp3-input-action:last-child,
    .bp3-input-group > .bp3-button:last-child,
    .bp3-input-group > .bp3-icon:last-child{
      right:0; }
  .bp3-input-group .bp3-button{
    min-width:24px;
    min-height:24px;
    margin:3px;
    padding:0 7px; }
    .bp3-input-group .bp3-button:empty{
      padding:0; }
  .bp3-input-group > .bp3-icon{
    z-index:1;
    color:#5c7080; }
    .bp3-input-group > .bp3-icon:empty{
      line-height:1;
      font-family:"Icons16", sans-serif;
      font-size:16px;
      font-weight:400;
      font-style:normal;
      -moz-osx-font-smoothing:grayscale;
      -webkit-font-smoothing:antialiased; }
  .bp3-input-group > .bp3-icon,
  .bp3-input-group .bp3-input-action > .bp3-spinner{
    margin:7px; }
  .bp3-input-group .bp3-tag{
    margin:5px; }
  .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:not(:hover):not(:focus),
  .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:not(:hover):not(:focus){
    color:#5c7080; }
    .bp3-dark .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:not(:hover):not(:focus), .bp3-dark
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:not(:hover):not(:focus){
      color:#a7b6c2; }
    .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:not(:hover):not(:focus) .bp3-icon, .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:not(:hover):not(:focus) .bp3-icon-standard, .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:not(:hover):not(:focus) .bp3-icon-large,
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:not(:hover):not(:focus) .bp3-icon,
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:not(:hover):not(:focus) .bp3-icon-standard,
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:not(:hover):not(:focus) .bp3-icon-large{
      color:#5c7080; }
  .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:disabled,
  .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:disabled{
    color:rgba(92, 112, 128, 0.6) !important; }
    .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:disabled .bp3-icon, .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:disabled .bp3-icon-standard, .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:disabled .bp3-icon-large,
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:disabled .bp3-icon,
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:disabled .bp3-icon-standard,
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:disabled .bp3-icon-large{
      color:rgba(92, 112, 128, 0.6) !important; }
  .bp3-input-group.bp3-disabled{
    cursor:not-allowed; }
    .bp3-input-group.bp3-disabled .bp3-icon{
      color:rgba(92, 112, 128, 0.6); }
  .bp3-input-group.bp3-large .bp3-button{
    min-width:30px;
    min-height:30px;
    margin:5px; }
  .bp3-input-group.bp3-large > .bp3-icon,
  .bp3-input-group.bp3-large .bp3-input-action > .bp3-spinner{
    margin:12px; }
  .bp3-input-group.bp3-large .bp3-input{
    height:40px;
    line-height:40px;
    font-size:16px; }
    .bp3-input-group.bp3-large .bp3-input[type="search"], .bp3-input-group.bp3-large .bp3-input.bp3-round{
      padding:0 15px; }
    .bp3-input-group.bp3-large .bp3-input:not(:first-child){
      padding-left:40px; }
    .bp3-input-group.bp3-large .bp3-input:not(:last-child){
      padding-right:40px; }
  .bp3-input-group.bp3-small .bp3-button{
    min-width:20px;
    min-height:20px;
    margin:2px; }
  .bp3-input-group.bp3-small .bp3-tag{
    min-width:20px;
    min-height:20px;
    margin:2px; }
  .bp3-input-group.bp3-small > .bp3-icon,
  .bp3-input-group.bp3-small .bp3-input-action > .bp3-spinner{
    margin:4px; }
  .bp3-input-group.bp3-small .bp3-input{
    height:24px;
    padding-right:8px;
    padding-left:8px;
    line-height:24px;
    font-size:12px; }
    .bp3-input-group.bp3-small .bp3-input[type="search"], .bp3-input-group.bp3-small .bp3-input.bp3-round{
      padding:0 12px; }
    .bp3-input-group.bp3-small .bp3-input:not(:first-child){
      padding-left:24px; }
    .bp3-input-group.bp3-small .bp3-input:not(:last-child){
      padding-right:24px; }
  .bp3-input-group.bp3-fill{
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto;
    width:100%; }
  .bp3-input-group.bp3-round .bp3-button,
  .bp3-input-group.bp3-round .bp3-input,
  .bp3-input-group.bp3-round .bp3-tag{
    border-radius:30px; }
  .bp3-dark .bp3-input-group .bp3-icon{
    color:#a7b6c2; }
  .bp3-dark .bp3-input-group.bp3-disabled .bp3-icon{
    color:rgba(167, 182, 194, 0.6); }
  .bp3-input-group.bp3-intent-primary .bp3-input{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px #137cbd, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px #137cbd, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-primary .bp3-input:focus{
      -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-primary .bp3-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #137cbd;
              box-shadow:inset 0 0 0 1px #137cbd; }
    .bp3-input-group.bp3-intent-primary .bp3-input:disabled, .bp3-input-group.bp3-intent-primary .bp3-input.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-input-group.bp3-intent-primary > .bp3-icon{
    color:#106ba3; }
    .bp3-dark .bp3-input-group.bp3-intent-primary > .bp3-icon{
      color:#48aff0; }
  .bp3-input-group.bp3-intent-success .bp3-input{
    -webkit-box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px #0f9960, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px #0f9960, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-success .bp3-input:focus{
      -webkit-box-shadow:0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-success .bp3-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #0f9960;
              box-shadow:inset 0 0 0 1px #0f9960; }
    .bp3-input-group.bp3-intent-success .bp3-input:disabled, .bp3-input-group.bp3-intent-success .bp3-input.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-input-group.bp3-intent-success > .bp3-icon{
    color:#0d8050; }
    .bp3-dark .bp3-input-group.bp3-intent-success > .bp3-icon{
      color:#3dcc91; }
  .bp3-input-group.bp3-intent-warning .bp3-input{
    -webkit-box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px #d9822b, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px #d9822b, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-warning .bp3-input:focus{
      -webkit-box-shadow:0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-warning .bp3-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #d9822b;
              box-shadow:inset 0 0 0 1px #d9822b; }
    .bp3-input-group.bp3-intent-warning .bp3-input:disabled, .bp3-input-group.bp3-intent-warning .bp3-input.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-input-group.bp3-intent-warning > .bp3-icon{
    color:#bf7326; }
    .bp3-dark .bp3-input-group.bp3-intent-warning > .bp3-icon{
      color:#ffb366; }
  .bp3-input-group.bp3-intent-danger .bp3-input{
    -webkit-box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px #db3737, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px #db3737, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-danger .bp3-input:focus{
      -webkit-box-shadow:0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-danger .bp3-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #db3737;
              box-shadow:inset 0 0 0 1px #db3737; }
    .bp3-input-group.bp3-intent-danger .bp3-input:disabled, .bp3-input-group.bp3-intent-danger .bp3-input.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-input-group.bp3-intent-danger > .bp3-icon{
    color:#c23030; }
    .bp3-dark .bp3-input-group.bp3-intent-danger > .bp3-icon{
      color:#ff7373; }
.bp3-input{
  outline:none;
  border:none;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
  background:#ffffff;
  height:30px;
  padding:0 10px;
  vertical-align:middle;
  line-height:30px;
  color:#182026;
  font-size:14px;
  font-weight:400;
  -webkit-transition:-webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:-webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  -webkit-appearance:none;
     -moz-appearance:none;
          appearance:none; }
  .bp3-input::-webkit-input-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-input::-moz-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-input:-ms-input-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-input::-ms-input-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-input::placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-input:focus, .bp3-input.bp3-active{
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-input[type="search"], .bp3-input.bp3-round{
    border-radius:30px;
    -webkit-box-sizing:border-box;
            box-sizing:border-box;
    padding-left:10px; }
  .bp3-input[readonly]{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.15);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.15); }
  .bp3-input:disabled, .bp3-input.bp3-disabled{
    -webkit-box-shadow:none;
            box-shadow:none;
    background:rgba(206, 217, 224, 0.5);
    cursor:not-allowed;
    color:rgba(92, 112, 128, 0.6);
    resize:none; }
  .bp3-input.bp3-large{
    height:40px;
    line-height:40px;
    font-size:16px; }
    .bp3-input.bp3-large[type="search"], .bp3-input.bp3-large.bp3-round{
      padding:0 15px; }
  .bp3-input.bp3-small{
    height:24px;
    padding-right:8px;
    padding-left:8px;
    line-height:24px;
    font-size:12px; }
    .bp3-input.bp3-small[type="search"], .bp3-input.bp3-small.bp3-round{
      padding:0 12px; }
  .bp3-input.bp3-fill{
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto;
    width:100%; }
  .bp3-dark .bp3-input{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
    background:rgba(16, 22, 26, 0.3);
    color:#f5f8fa; }
    .bp3-dark .bp3-input::-webkit-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-input::-moz-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-input:-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-input::-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-input::placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-input:focus{
      -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-input:disabled, .bp3-dark .bp3-input.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:rgba(57, 75, 89, 0.5);
      color:rgba(167, 182, 194, 0.6); }
  .bp3-input.bp3-intent-primary{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px #137cbd, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px #137cbd, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-primary:focus{
      -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-primary[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #137cbd;
              box-shadow:inset 0 0 0 1px #137cbd; }
    .bp3-input.bp3-intent-primary:disabled, .bp3-input.bp3-intent-primary.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
    .bp3-dark .bp3-input.bp3-intent-primary{
      -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px #137cbd, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px #137cbd, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-primary:focus{
        -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
                box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-primary[readonly]{
        -webkit-box-shadow:inset 0 0 0 1px #137cbd;
                box-shadow:inset 0 0 0 1px #137cbd; }
      .bp3-dark .bp3-input.bp3-intent-primary:disabled, .bp3-dark .bp3-input.bp3-intent-primary.bp3-disabled{
        -webkit-box-shadow:none;
                box-shadow:none; }
  .bp3-input.bp3-intent-success{
    -webkit-box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px #0f9960, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px #0f9960, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-success:focus{
      -webkit-box-shadow:0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-success[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #0f9960;
              box-shadow:inset 0 0 0 1px #0f9960; }
    .bp3-input.bp3-intent-success:disabled, .bp3-input.bp3-intent-success.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
    .bp3-dark .bp3-input.bp3-intent-success{
      -webkit-box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px #0f9960, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px #0f9960, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-success:focus{
        -webkit-box-shadow:0 0 0 1px #0f9960, 0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
                box-shadow:0 0 0 1px #0f9960, 0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-success[readonly]{
        -webkit-box-shadow:inset 0 0 0 1px #0f9960;
                box-shadow:inset 0 0 0 1px #0f9960; }
      .bp3-dark .bp3-input.bp3-intent-success:disabled, .bp3-dark .bp3-input.bp3-intent-success.bp3-disabled{
        -webkit-box-shadow:none;
                box-shadow:none; }
  .bp3-input.bp3-intent-warning{
    -webkit-box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px #d9822b, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px #d9822b, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-warning:focus{
      -webkit-box-shadow:0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-warning[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #d9822b;
              box-shadow:inset 0 0 0 1px #d9822b; }
    .bp3-input.bp3-intent-warning:disabled, .bp3-input.bp3-intent-warning.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
    .bp3-dark .bp3-input.bp3-intent-warning{
      -webkit-box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px #d9822b, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px #d9822b, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-warning:focus{
        -webkit-box-shadow:0 0 0 1px #d9822b, 0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
                box-shadow:0 0 0 1px #d9822b, 0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-warning[readonly]{
        -webkit-box-shadow:inset 0 0 0 1px #d9822b;
                box-shadow:inset 0 0 0 1px #d9822b; }
      .bp3-dark .bp3-input.bp3-intent-warning:disabled, .bp3-dark .bp3-input.bp3-intent-warning.bp3-disabled{
        -webkit-box-shadow:none;
                box-shadow:none; }
  .bp3-input.bp3-intent-danger{
    -webkit-box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px #db3737, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px #db3737, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-danger:focus{
      -webkit-box-shadow:0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-danger[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #db3737;
              box-shadow:inset 0 0 0 1px #db3737; }
    .bp3-input.bp3-intent-danger:disabled, .bp3-input.bp3-intent-danger.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
    .bp3-dark .bp3-input.bp3-intent-danger{
      -webkit-box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px #db3737, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px #db3737, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-danger:focus{
        -webkit-box-shadow:0 0 0 1px #db3737, 0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
                box-shadow:0 0 0 1px #db3737, 0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-danger[readonly]{
        -webkit-box-shadow:inset 0 0 0 1px #db3737;
                box-shadow:inset 0 0 0 1px #db3737; }
      .bp3-dark .bp3-input.bp3-intent-danger:disabled, .bp3-dark .bp3-input.bp3-intent-danger.bp3-disabled{
        -webkit-box-shadow:none;
                box-shadow:none; }
  .bp3-input::-ms-clear{
    display:none; }
textarea.bp3-input{
  max-width:100%;
  padding:10px; }
  textarea.bp3-input, textarea.bp3-input.bp3-large, textarea.bp3-input.bp3-small{
    height:auto;
    line-height:inherit; }
  textarea.bp3-input.bp3-small{
    padding:8px; }
  .bp3-dark textarea.bp3-input{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
    background:rgba(16, 22, 26, 0.3);
    color:#f5f8fa; }
    .bp3-dark textarea.bp3-input::-webkit-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark textarea.bp3-input::-moz-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark textarea.bp3-input:-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark textarea.bp3-input::-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark textarea.bp3-input::placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark textarea.bp3-input:focus{
      -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark textarea.bp3-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark textarea.bp3-input:disabled, .bp3-dark textarea.bp3-input.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:rgba(57, 75, 89, 0.5);
      color:rgba(167, 182, 194, 0.6); }
label.bp3-label{
  display:block;
  margin-top:0;
  margin-bottom:15px; }
  label.bp3-label .bp3-html-select,
  label.bp3-label .bp3-input,
  label.bp3-label .bp3-select,
  label.bp3-label .bp3-slider,
  label.bp3-label .bp3-popover-wrapper{
    display:block;
    margin-top:5px;
    text-transform:none; }
  label.bp3-label .bp3-button-group{
    margin-top:5px; }
  label.bp3-label .bp3-select select,
  label.bp3-label .bp3-html-select select{
    width:100%;
    vertical-align:top;
    font-weight:400; }
  label.bp3-label.bp3-disabled,
  label.bp3-label.bp3-disabled .bp3-text-muted{
    color:rgba(92, 112, 128, 0.6); }
  label.bp3-label.bp3-inline{
    line-height:30px; }
    label.bp3-label.bp3-inline .bp3-html-select,
    label.bp3-label.bp3-inline .bp3-input,
    label.bp3-label.bp3-inline .bp3-input-group,
    label.bp3-label.bp3-inline .bp3-select,
    label.bp3-label.bp3-inline .bp3-popover-wrapper{
      display:inline-block;
      margin:0 0 0 5px;
      vertical-align:top; }
    label.bp3-label.bp3-inline .bp3-button-group{
      margin:0 0 0 5px; }
    label.bp3-label.bp3-inline .bp3-input-group .bp3-input{
      margin-left:0; }
    label.bp3-label.bp3-inline.bp3-large{
      line-height:40px; }
  label.bp3-label:not(.bp3-inline) .bp3-popover-target{
    display:block; }
  .bp3-dark label.bp3-label{
    color:#f5f8fa; }
    .bp3-dark label.bp3-label.bp3-disabled,
    .bp3-dark label.bp3-label.bp3-disabled .bp3-text-muted{
      color:rgba(167, 182, 194, 0.6); }
.bp3-numeric-input .bp3-button-group.bp3-vertical > .bp3-button{
  -webkit-box-flex:1;
      -ms-flex:1 1 14px;
          flex:1 1 14px;
  width:30px;
  min-height:0;
  padding:0; }
  .bp3-numeric-input .bp3-button-group.bp3-vertical > .bp3-button:first-child{
    border-radius:0 3px 0 0; }
  .bp3-numeric-input .bp3-button-group.bp3-vertical > .bp3-button:last-child{
    border-radius:0 0 3px 0; }

.bp3-numeric-input .bp3-button-group.bp3-vertical:first-child > .bp3-button:first-child{
  border-radius:3px 0 0 0; }

.bp3-numeric-input .bp3-button-group.bp3-vertical:first-child > .bp3-button:last-child{
  border-radius:0 0 0 3px; }

.bp3-numeric-input.bp3-large .bp3-button-group.bp3-vertical > .bp3-button{
  width:40px; }

form{
  display:block; }
.bp3-html-select select,
.bp3-select select{
  display:-webkit-inline-box;
  display:-ms-inline-flexbox;
  display:inline-flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  border:none;
  border-radius:3px;
  cursor:pointer;
  padding:5px 10px;
  vertical-align:middle;
  text-align:left;
  font-size:14px;
  -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
          box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
  background-color:#f5f8fa;
  background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.8)), to(rgba(255, 255, 255, 0)));
  background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.8), rgba(255, 255, 255, 0));
  color:#182026;
  border-radius:3px;
  width:100%;
  height:30px;
  padding:0 25px 0 10px;
  -moz-appearance:none;
  -webkit-appearance:none; }
  .bp3-html-select select > *, .bp3-select select > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-html-select select > .bp3-fill, .bp3-select select > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-html-select select::before,
  .bp3-select select::before, .bp3-html-select select > *, .bp3-select select > *{
    margin-right:7px; }
  .bp3-html-select select:empty::before,
  .bp3-select select:empty::before,
  .bp3-html-select select > :last-child,
  .bp3-select select > :last-child{
    margin-right:0; }
  .bp3-html-select select:hover,
  .bp3-select select:hover{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
    background-clip:padding-box;
    background-color:#ebf1f5; }
  .bp3-html-select select:active,
  .bp3-select select:active, .bp3-html-select select.bp3-active,
  .bp3-select select.bp3-active{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
    background-color:#d8e1e8;
    background-image:none; }
  .bp3-html-select select:disabled,
  .bp3-select select:disabled, .bp3-html-select select.bp3-disabled,
  .bp3-select select.bp3-disabled{
    outline:none;
    -webkit-box-shadow:none;
            box-shadow:none;
    background-color:rgba(206, 217, 224, 0.5);
    background-image:none;
    cursor:not-allowed;
    color:rgba(92, 112, 128, 0.6); }
    .bp3-html-select select:disabled.bp3-active,
    .bp3-select select:disabled.bp3-active, .bp3-html-select select:disabled.bp3-active:hover,
    .bp3-select select:disabled.bp3-active:hover, .bp3-html-select select.bp3-disabled.bp3-active,
    .bp3-select select.bp3-disabled.bp3-active, .bp3-html-select select.bp3-disabled.bp3-active:hover,
    .bp3-select select.bp3-disabled.bp3-active:hover{
      background:rgba(206, 217, 224, 0.7); }

.bp3-html-select.bp3-minimal select,
.bp3-select.bp3-minimal select{
  -webkit-box-shadow:none;
          box-shadow:none;
  background:none; }
  .bp3-html-select.bp3-minimal select:hover,
  .bp3-select.bp3-minimal select:hover{
    -webkit-box-shadow:none;
            box-shadow:none;
    background:rgba(167, 182, 194, 0.3);
    text-decoration:none;
    color:#182026; }
  .bp3-html-select.bp3-minimal select:active,
  .bp3-select.bp3-minimal select:active, .bp3-html-select.bp3-minimal select.bp3-active,
  .bp3-select.bp3-minimal select.bp3-active{
    -webkit-box-shadow:none;
            box-shadow:none;
    background:rgba(115, 134, 148, 0.3);
    color:#182026; }
  .bp3-html-select.bp3-minimal select:disabled,
  .bp3-select.bp3-minimal select:disabled, .bp3-html-select.bp3-minimal select:disabled:hover,
  .bp3-select.bp3-minimal select:disabled:hover, .bp3-html-select.bp3-minimal select.bp3-disabled,
  .bp3-select.bp3-minimal select.bp3-disabled, .bp3-html-select.bp3-minimal select.bp3-disabled:hover,
  .bp3-select.bp3-minimal select.bp3-disabled:hover{
    background:none;
    cursor:not-allowed;
    color:rgba(92, 112, 128, 0.6); }
    .bp3-html-select.bp3-minimal select:disabled.bp3-active,
    .bp3-select.bp3-minimal select:disabled.bp3-active, .bp3-html-select.bp3-minimal select:disabled:hover.bp3-active,
    .bp3-select.bp3-minimal select:disabled:hover.bp3-active, .bp3-html-select.bp3-minimal select.bp3-disabled.bp3-active,
    .bp3-select.bp3-minimal select.bp3-disabled.bp3-active, .bp3-html-select.bp3-minimal select.bp3-disabled:hover.bp3-active,
    .bp3-select.bp3-minimal select.bp3-disabled:hover.bp3-active{
      background:rgba(115, 134, 148, 0.3); }
  .bp3-dark .bp3-html-select.bp3-minimal select, .bp3-html-select.bp3-minimal .bp3-dark select,
  .bp3-dark .bp3-select.bp3-minimal select, .bp3-select.bp3-minimal .bp3-dark select{
    -webkit-box-shadow:none;
            box-shadow:none;
    background:none;
    color:inherit; }
    .bp3-dark .bp3-html-select.bp3-minimal select:hover, .bp3-html-select.bp3-minimal .bp3-dark select:hover,
    .bp3-dark .bp3-select.bp3-minimal select:hover, .bp3-select.bp3-minimal .bp3-dark select:hover, .bp3-dark .bp3-html-select.bp3-minimal select:active, .bp3-html-select.bp3-minimal .bp3-dark select:active,
    .bp3-dark .bp3-select.bp3-minimal select:active, .bp3-select.bp3-minimal .bp3-dark select:active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-active,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-active{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:none; }
    .bp3-dark .bp3-html-select.bp3-minimal select:hover, .bp3-html-select.bp3-minimal .bp3-dark select:hover,
    .bp3-dark .bp3-select.bp3-minimal select:hover, .bp3-select.bp3-minimal .bp3-dark select:hover{
      background:rgba(138, 155, 168, 0.15); }
    .bp3-dark .bp3-html-select.bp3-minimal select:active, .bp3-html-select.bp3-minimal .bp3-dark select:active,
    .bp3-dark .bp3-select.bp3-minimal select:active, .bp3-select.bp3-minimal .bp3-dark select:active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-active,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-active{
      background:rgba(138, 155, 168, 0.3);
      color:#f5f8fa; }
    .bp3-dark .bp3-html-select.bp3-minimal select:disabled, .bp3-html-select.bp3-minimal .bp3-dark select:disabled,
    .bp3-dark .bp3-select.bp3-minimal select:disabled, .bp3-select.bp3-minimal .bp3-dark select:disabled, .bp3-dark .bp3-html-select.bp3-minimal select:disabled:hover, .bp3-html-select.bp3-minimal .bp3-dark select:disabled:hover,
    .bp3-dark .bp3-select.bp3-minimal select:disabled:hover, .bp3-select.bp3-minimal .bp3-dark select:disabled:hover, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-disabled,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-disabled, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-disabled:hover, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-disabled:hover,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-disabled:hover, .bp3-select.bp3-minimal .bp3-dark select.bp3-disabled:hover{
      background:none;
      cursor:not-allowed;
      color:rgba(167, 182, 194, 0.6); }
      .bp3-dark .bp3-html-select.bp3-minimal select:disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select:disabled.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select:disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select:disabled.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select:disabled:hover.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select:disabled:hover.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select:disabled:hover.bp3-active, .bp3-select.bp3-minimal .bp3-dark select:disabled:hover.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-disabled.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-disabled.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-disabled:hover.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-disabled:hover.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-disabled:hover.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-disabled:hover.bp3-active{
        background:rgba(138, 155, 168, 0.3); }
  .bp3-html-select.bp3-minimal select.bp3-intent-primary,
  .bp3-select.bp3-minimal select.bp3-intent-primary{
    color:#106ba3; }
    .bp3-html-select.bp3-minimal select.bp3-intent-primary:hover,
    .bp3-select.bp3-minimal select.bp3-intent-primary:hover, .bp3-html-select.bp3-minimal select.bp3-intent-primary:active,
    .bp3-select.bp3-minimal select.bp3-intent-primary:active, .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-active{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:none;
      color:#106ba3; }
    .bp3-html-select.bp3-minimal select.bp3-intent-primary:hover,
    .bp3-select.bp3-minimal select.bp3-intent-primary:hover{
      background:rgba(19, 124, 189, 0.15);
      color:#106ba3; }
    .bp3-html-select.bp3-minimal select.bp3-intent-primary:active,
    .bp3-select.bp3-minimal select.bp3-intent-primary:active, .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-active{
      background:rgba(19, 124, 189, 0.3);
      color:#106ba3; }
    .bp3-html-select.bp3-minimal select.bp3-intent-primary:disabled,
    .bp3-select.bp3-minimal select.bp3-intent-primary:disabled, .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-disabled,
    .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-disabled{
      background:none;
      color:rgba(16, 107, 163, 0.5); }
      .bp3-html-select.bp3-minimal select.bp3-intent-primary:disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-primary:disabled.bp3-active, .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-disabled.bp3-active{
        background:rgba(19, 124, 189, 0.3); }
    .bp3-html-select.bp3-minimal select.bp3-intent-primary .bp3-button-spinner .bp3-spinner-head, .bp3-select.bp3-minimal select.bp3-intent-primary .bp3-button-spinner .bp3-spinner-head{
      stroke:#106ba3; }
    .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary{
      color:#48aff0; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary:hover, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary:hover,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary:hover, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary:hover{
        background:rgba(19, 124, 189, 0.2);
        color:#48aff0; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary:active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary:active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary:active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary:active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary.bp3-active{
        background:rgba(19, 124, 189, 0.3);
        color:#48aff0; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary:disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary:disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary:disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary:disabled, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary.bp3-disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary.bp3-disabled{
        background:none;
        color:rgba(72, 175, 240, 0.5); }
        .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary:disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary:disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary:disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary:disabled.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary.bp3-disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary.bp3-disabled.bp3-active{
          background:rgba(19, 124, 189, 0.3); }
  .bp3-html-select.bp3-minimal select.bp3-intent-success,
  .bp3-select.bp3-minimal select.bp3-intent-success{
    color:#0d8050; }
    .bp3-html-select.bp3-minimal select.bp3-intent-success:hover,
    .bp3-select.bp3-minimal select.bp3-intent-success:hover, .bp3-html-select.bp3-minimal select.bp3-intent-success:active,
    .bp3-select.bp3-minimal select.bp3-intent-success:active, .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-success.bp3-active{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:none;
      color:#0d8050; }
    .bp3-html-select.bp3-minimal select.bp3-intent-success:hover,
    .bp3-select.bp3-minimal select.bp3-intent-success:hover{
      background:rgba(15, 153, 96, 0.15);
      color:#0d8050; }
    .bp3-html-select.bp3-minimal select.bp3-intent-success:active,
    .bp3-select.bp3-minimal select.bp3-intent-success:active, .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-success.bp3-active{
      background:rgba(15, 153, 96, 0.3);
      color:#0d8050; }
    .bp3-html-select.bp3-minimal select.bp3-intent-success:disabled,
    .bp3-select.bp3-minimal select.bp3-intent-success:disabled, .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-disabled,
    .bp3-select.bp3-minimal select.bp3-intent-success.bp3-disabled{
      background:none;
      color:rgba(13, 128, 80, 0.5); }
      .bp3-html-select.bp3-minimal select.bp3-intent-success:disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-success:disabled.bp3-active, .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-success.bp3-disabled.bp3-active{
        background:rgba(15, 153, 96, 0.3); }
    .bp3-html-select.bp3-minimal select.bp3-intent-success .bp3-button-spinner .bp3-spinner-head, .bp3-select.bp3-minimal select.bp3-intent-success .bp3-button-spinner .bp3-spinner-head{
      stroke:#0d8050; }
    .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success{
      color:#3dcc91; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success:hover, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success:hover,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success:hover, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success:hover{
        background:rgba(15, 153, 96, 0.2);
        color:#3dcc91; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success:active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success:active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success:active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success:active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success.bp3-active{
        background:rgba(15, 153, 96, 0.3);
        color:#3dcc91; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success:disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success:disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success:disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success:disabled, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success.bp3-disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success.bp3-disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success.bp3-disabled{
        background:none;
        color:rgba(61, 204, 145, 0.5); }
        .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success:disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success:disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success:disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success:disabled.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success.bp3-disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success.bp3-disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success.bp3-disabled.bp3-active{
          background:rgba(15, 153, 96, 0.3); }
  .bp3-html-select.bp3-minimal select.bp3-intent-warning,
  .bp3-select.bp3-minimal select.bp3-intent-warning{
    color:#bf7326; }
    .bp3-html-select.bp3-minimal select.bp3-intent-warning:hover,
    .bp3-select.bp3-minimal select.bp3-intent-warning:hover, .bp3-html-select.bp3-minimal select.bp3-intent-warning:active,
    .bp3-select.bp3-minimal select.bp3-intent-warning:active, .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-active{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:none;
      color:#bf7326; }
    .bp3-html-select.bp3-minimal select.bp3-intent-warning:hover,
    .bp3-select.bp3-minimal select.bp3-intent-warning:hover{
      background:rgba(217, 130, 43, 0.15);
      color:#bf7326; }
    .bp3-html-select.bp3-minimal select.bp3-intent-warning:active,
    .bp3-select.bp3-minimal select.bp3-intent-warning:active, .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-active{
      background:rgba(217, 130, 43, 0.3);
      color:#bf7326; }
    .bp3-html-select.bp3-minimal select.bp3-intent-warning:disabled,
    .bp3-select.bp3-minimal select.bp3-intent-warning:disabled, .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-disabled,
    .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-disabled{
      background:none;
      color:rgba(191, 115, 38, 0.5); }
      .bp3-html-select.bp3-minimal select.bp3-intent-warning:disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-warning:disabled.bp3-active, .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-disabled.bp3-active{
        background:rgba(217, 130, 43, 0.3); }
    .bp3-html-select.bp3-minimal select.bp3-intent-warning .bp3-button-spinner .bp3-spinner-head, .bp3-select.bp3-minimal select.bp3-intent-warning .bp3-button-spinner .bp3-spinner-head{
      stroke:#bf7326; }
    .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning{
      color:#ffb366; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning:hover, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning:hover,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning:hover, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning:hover{
        background:rgba(217, 130, 43, 0.2);
        color:#ffb366; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning:active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning:active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning:active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning:active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning.bp3-active{
        background:rgba(217, 130, 43, 0.3);
        color:#ffb366; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning:disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning:disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning:disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning:disabled, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning.bp3-disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning.bp3-disabled{
        background:none;
        color:rgba(255, 179, 102, 0.5); }
        .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning:disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning:disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning:disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning:disabled.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning.bp3-disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning.bp3-disabled.bp3-active{
          background:rgba(217, 130, 43, 0.3); }
  .bp3-html-select.bp3-minimal select.bp3-intent-danger,
  .bp3-select.bp3-minimal select.bp3-intent-danger{
    color:#c23030; }
    .bp3-html-select.bp3-minimal select.bp3-intent-danger:hover,
    .bp3-select.bp3-minimal select.bp3-intent-danger:hover, .bp3-html-select.bp3-minimal select.bp3-intent-danger:active,
    .bp3-select.bp3-minimal select.bp3-intent-danger:active, .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-active{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:none;
      color:#c23030; }
    .bp3-html-select.bp3-minimal select.bp3-intent-danger:hover,
    .bp3-select.bp3-minimal select.bp3-intent-danger:hover{
      background:rgba(219, 55, 55, 0.15);
      color:#c23030; }
    .bp3-html-select.bp3-minimal select.bp3-intent-danger:active,
    .bp3-select.bp3-minimal select.bp3-intent-danger:active, .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-active{
      background:rgba(219, 55, 55, 0.3);
      color:#c23030; }
    .bp3-html-select.bp3-minimal select.bp3-intent-danger:disabled,
    .bp3-select.bp3-minimal select.bp3-intent-danger:disabled, .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-disabled,
    .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-disabled{
      background:none;
      color:rgba(194, 48, 48, 0.5); }
      .bp3-html-select.bp3-minimal select.bp3-intent-danger:disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-danger:disabled.bp3-active, .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-disabled.bp3-active{
        background:rgba(219, 55, 55, 0.3); }
    .bp3-html-select.bp3-minimal select.bp3-intent-danger .bp3-button-spinner .bp3-spinner-head, .bp3-select.bp3-minimal select.bp3-intent-danger .bp3-button-spinner .bp3-spinner-head{
      stroke:#c23030; }
    .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger{
      color:#ff7373; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger:hover, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger:hover,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger:hover, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger:hover{
        background:rgba(219, 55, 55, 0.2);
        color:#ff7373; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger:active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger:active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger:active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger:active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger.bp3-active{
        background:rgba(219, 55, 55, 0.3);
        color:#ff7373; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger:disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger:disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger:disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger:disabled, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger.bp3-disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger.bp3-disabled{
        background:none;
        color:rgba(255, 115, 115, 0.5); }
        .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger:disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger:disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger:disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger:disabled.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger.bp3-disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger.bp3-disabled.bp3-active{
          background:rgba(219, 55, 55, 0.3); }

.bp3-html-select.bp3-large select,
.bp3-select.bp3-large select{
  height:40px;
  padding-right:35px;
  font-size:16px; }

.bp3-dark .bp3-html-select select, .bp3-dark .bp3-select select{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
  background-color:#394b59;
  background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.05)), to(rgba(255, 255, 255, 0)));
  background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.05), rgba(255, 255, 255, 0));
  color:#f5f8fa; }
  .bp3-dark .bp3-html-select select:hover, .bp3-dark .bp3-select select:hover, .bp3-dark .bp3-html-select select:active, .bp3-dark .bp3-select select:active, .bp3-dark .bp3-html-select select.bp3-active, .bp3-dark .bp3-select select.bp3-active{
    color:#f5f8fa; }
  .bp3-dark .bp3-html-select select:hover, .bp3-dark .bp3-select select:hover{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
    background-color:#30404d; }
  .bp3-dark .bp3-html-select select:active, .bp3-dark .bp3-select select:active, .bp3-dark .bp3-html-select select.bp3-active, .bp3-dark .bp3-select select.bp3-active{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
    background-color:#202b33;
    background-image:none; }
  .bp3-dark .bp3-html-select select:disabled, .bp3-dark .bp3-select select:disabled, .bp3-dark .bp3-html-select select.bp3-disabled, .bp3-dark .bp3-select select.bp3-disabled{
    -webkit-box-shadow:none;
            box-shadow:none;
    background-color:rgba(57, 75, 89, 0.5);
    background-image:none;
    color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-html-select select:disabled.bp3-active, .bp3-dark .bp3-select select:disabled.bp3-active, .bp3-dark .bp3-html-select select.bp3-disabled.bp3-active, .bp3-dark .bp3-select select.bp3-disabled.bp3-active{
      background:rgba(57, 75, 89, 0.7); }
  .bp3-dark .bp3-html-select select .bp3-button-spinner .bp3-spinner-head, .bp3-dark .bp3-select select .bp3-button-spinner .bp3-spinner-head{
    background:rgba(16, 22, 26, 0.5);
    stroke:#8a9ba8; }

.bp3-html-select select:disabled,
.bp3-select select:disabled{
  -webkit-box-shadow:none;
          box-shadow:none;
  background-color:rgba(206, 217, 224, 0.5);
  cursor:not-allowed;
  color:rgba(92, 112, 128, 0.6); }

.bp3-html-select .bp3-icon,
.bp3-select .bp3-icon, .bp3-select::after{
  position:absolute;
  top:7px;
  right:7px;
  color:#5c7080;
  pointer-events:none; }
  .bp3-html-select .bp3-disabled.bp3-icon,
  .bp3-select .bp3-disabled.bp3-icon, .bp3-disabled.bp3-select::after{
    color:rgba(92, 112, 128, 0.6); }
.bp3-html-select,
.bp3-select{
  display:inline-block;
  position:relative;
  vertical-align:middle;
  letter-spacing:normal; }
  .bp3-html-select select::-ms-expand,
  .bp3-select select::-ms-expand{
    display:none; }
  .bp3-html-select .bp3-icon,
  .bp3-select .bp3-icon{
    color:#5c7080; }
    .bp3-html-select .bp3-icon:hover,
    .bp3-select .bp3-icon:hover{
      color:#182026; }
    .bp3-dark .bp3-html-select .bp3-icon, .bp3-dark
    .bp3-select .bp3-icon{
      color:#a7b6c2; }
      .bp3-dark .bp3-html-select .bp3-icon:hover, .bp3-dark
      .bp3-select .bp3-icon:hover{
        color:#f5f8fa; }
  .bp3-html-select.bp3-large::after,
  .bp3-html-select.bp3-large .bp3-icon,
  .bp3-select.bp3-large::after,
  .bp3-select.bp3-large .bp3-icon{
    top:12px;
    right:12px; }
  .bp3-html-select.bp3-fill,
  .bp3-html-select.bp3-fill select,
  .bp3-select.bp3-fill,
  .bp3-select.bp3-fill select{
    width:100%; }
  .bp3-dark .bp3-html-select option, .bp3-dark
  .bp3-select option{
    background-color:#30404d;
    color:#f5f8fa; }
  .bp3-dark .bp3-html-select::after, .bp3-dark
  .bp3-select::after{
    color:#a7b6c2; }

.bp3-select::after{
  line-height:1;
  font-family:"Icons16", sans-serif;
  font-size:16px;
  font-weight:400;
  font-style:normal;
  -moz-osx-font-smoothing:grayscale;
  -webkit-font-smoothing:antialiased;
  content:""; }
.bp3-running-text table, table.bp3-html-table{
  border-spacing:0;
  font-size:14px; }
  .bp3-running-text table th, table.bp3-html-table th,
  .bp3-running-text table td,
  table.bp3-html-table td{
    padding:11px;
    vertical-align:top;
    text-align:left; }
  .bp3-running-text table th, table.bp3-html-table th{
    color:#182026;
    font-weight:600; }
  
  .bp3-running-text table td,
  table.bp3-html-table td{
    color:#182026; }
  .bp3-running-text table tbody tr:first-child th, table.bp3-html-table tbody tr:first-child th,
  .bp3-running-text table tbody tr:first-child td,
  table.bp3-html-table tbody tr:first-child td{
    -webkit-box-shadow:inset 0 1px 0 0 rgba(16, 22, 26, 0.15);
            box-shadow:inset 0 1px 0 0 rgba(16, 22, 26, 0.15); }
  .bp3-dark .bp3-running-text table th, .bp3-running-text .bp3-dark table th, .bp3-dark table.bp3-html-table th{
    color:#f5f8fa; }
  .bp3-dark .bp3-running-text table td, .bp3-running-text .bp3-dark table td, .bp3-dark table.bp3-html-table td{
    color:#f5f8fa; }
  .bp3-dark .bp3-running-text table tbody tr:first-child th, .bp3-running-text .bp3-dark table tbody tr:first-child th, .bp3-dark table.bp3-html-table tbody tr:first-child th,
  .bp3-dark .bp3-running-text table tbody tr:first-child td,
  .bp3-running-text .bp3-dark table tbody tr:first-child td,
  .bp3-dark table.bp3-html-table tbody tr:first-child td{
    -webkit-box-shadow:inset 0 1px 0 0 rgba(255, 255, 255, 0.15);
            box-shadow:inset 0 1px 0 0 rgba(255, 255, 255, 0.15); }

table.bp3-html-table.bp3-html-table-condensed th,
table.bp3-html-table.bp3-html-table-condensed td, table.bp3-html-table.bp3-small th,
table.bp3-html-table.bp3-small td{
  padding-top:6px;
  padding-bottom:6px; }

table.bp3-html-table.bp3-html-table-striped tbody tr:nth-child(odd) td{
  background:rgba(191, 204, 214, 0.15); }

table.bp3-html-table.bp3-html-table-bordered th:not(:first-child){
  -webkit-box-shadow:inset 1px 0 0 0 rgba(16, 22, 26, 0.15);
          box-shadow:inset 1px 0 0 0 rgba(16, 22, 26, 0.15); }

table.bp3-html-table.bp3-html-table-bordered tbody tr td{
  -webkit-box-shadow:inset 0 1px 0 0 rgba(16, 22, 26, 0.15);
          box-shadow:inset 0 1px 0 0 rgba(16, 22, 26, 0.15); }
  table.bp3-html-table.bp3-html-table-bordered tbody tr td:not(:first-child){
    -webkit-box-shadow:inset 1px 1px 0 0 rgba(16, 22, 26, 0.15);
            box-shadow:inset 1px 1px 0 0 rgba(16, 22, 26, 0.15); }

table.bp3-html-table.bp3-html-table-bordered.bp3-html-table-striped tbody tr:not(:first-child) td{
  -webkit-box-shadow:none;
          box-shadow:none; }
  table.bp3-html-table.bp3-html-table-bordered.bp3-html-table-striped tbody tr:not(:first-child) td:not(:first-child){
    -webkit-box-shadow:inset 1px 0 0 0 rgba(16, 22, 26, 0.15);
            box-shadow:inset 1px 0 0 0 rgba(16, 22, 26, 0.15); }

table.bp3-html-table.bp3-interactive tbody tr:hover td{
  background-color:rgba(191, 204, 214, 0.3);
  cursor:pointer; }

table.bp3-html-table.bp3-interactive tbody tr:active td{
  background-color:rgba(191, 204, 214, 0.4); }

.bp3-dark table.bp3-html-table.bp3-html-table-striped tbody tr:nth-child(odd) td{
  background:rgba(92, 112, 128, 0.15); }

.bp3-dark table.bp3-html-table.bp3-html-table-bordered th:not(:first-child){
  -webkit-box-shadow:inset 1px 0 0 0 rgba(255, 255, 255, 0.15);
          box-shadow:inset 1px 0 0 0 rgba(255, 255, 255, 0.15); }

.bp3-dark table.bp3-html-table.bp3-html-table-bordered tbody tr td{
  -webkit-box-shadow:inset 0 1px 0 0 rgba(255, 255, 255, 0.15);
          box-shadow:inset 0 1px 0 0 rgba(255, 255, 255, 0.15); }
  .bp3-dark table.bp3-html-table.bp3-html-table-bordered tbody tr td:not(:first-child){
    -webkit-box-shadow:inset 1px 1px 0 0 rgba(255, 255, 255, 0.15);
            box-shadow:inset 1px 1px 0 0 rgba(255, 255, 255, 0.15); }

.bp3-dark table.bp3-html-table.bp3-html-table-bordered.bp3-html-table-striped tbody tr:not(:first-child) td{
  -webkit-box-shadow:inset 1px 0 0 0 rgba(255, 255, 255, 0.15);
          box-shadow:inset 1px 0 0 0 rgba(255, 255, 255, 0.15); }
  .bp3-dark table.bp3-html-table.bp3-html-table-bordered.bp3-html-table-striped tbody tr:not(:first-child) td:first-child{
    -webkit-box-shadow:none;
            box-shadow:none; }

.bp3-dark table.bp3-html-table.bp3-interactive tbody tr:hover td{
  background-color:rgba(92, 112, 128, 0.3);
  cursor:pointer; }

.bp3-dark table.bp3-html-table.bp3-interactive tbody tr:active td{
  background-color:rgba(92, 112, 128, 0.4); }

.bp3-key-combo{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center; }
  .bp3-key-combo > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-key-combo > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-key-combo::before,
  .bp3-key-combo > *{
    margin-right:5px; }
  .bp3-key-combo:empty::before,
  .bp3-key-combo > :last-child{
    margin-right:0; }

.bp3-hotkey-dialog{
  top:40px;
  padding-bottom:0; }
  .bp3-hotkey-dialog .bp3-dialog-body{
    margin:0;
    padding:0; }
  .bp3-hotkey-dialog .bp3-hotkey-label{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1; }

.bp3-hotkey-column{
  margin:auto;
  max-height:80vh;
  overflow-y:auto;
  padding:30px; }
  .bp3-hotkey-column .bp3-heading{
    margin-bottom:20px; }
    .bp3-hotkey-column .bp3-heading:not(:first-child){
      margin-top:40px; }

.bp3-hotkey{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  -webkit-box-pack:justify;
      -ms-flex-pack:justify;
          justify-content:space-between;
  margin-right:0;
  margin-left:0; }
  .bp3-hotkey:not(:last-child){
    margin-bottom:10px; }
.bp3-icon{
  display:inline-block;
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  vertical-align:text-bottom; }
  .bp3-icon:not(:empty)::before{
    content:"" !important;
    content:unset !important; }
  .bp3-icon > svg{
    display:block; }
    .bp3-icon > svg:not([fill]){
      fill:currentColor; }

.bp3-icon.bp3-intent-primary, .bp3-icon-standard.bp3-intent-primary, .bp3-icon-large.bp3-intent-primary{
  color:#106ba3; }
  .bp3-dark .bp3-icon.bp3-intent-primary, .bp3-dark .bp3-icon-standard.bp3-intent-primary, .bp3-dark .bp3-icon-large.bp3-intent-primary{
    color:#48aff0; }

.bp3-icon.bp3-intent-success, .bp3-icon-standard.bp3-intent-success, .bp3-icon-large.bp3-intent-success{
  color:#0d8050; }
  .bp3-dark .bp3-icon.bp3-intent-success, .bp3-dark .bp3-icon-standard.bp3-intent-success, .bp3-dark .bp3-icon-large.bp3-intent-success{
    color:#3dcc91; }

.bp3-icon.bp3-intent-warning, .bp3-icon-standard.bp3-intent-warning, .bp3-icon-large.bp3-intent-warning{
  color:#bf7326; }
  .bp3-dark .bp3-icon.bp3-intent-warning, .bp3-dark .bp3-icon-standard.bp3-intent-warning, .bp3-dark .bp3-icon-large.bp3-intent-warning{
    color:#ffb366; }

.bp3-icon.bp3-intent-danger, .bp3-icon-standard.bp3-intent-danger, .bp3-icon-large.bp3-intent-danger{
  color:#c23030; }
  .bp3-dark .bp3-icon.bp3-intent-danger, .bp3-dark .bp3-icon-standard.bp3-intent-danger, .bp3-dark .bp3-icon-large.bp3-intent-danger{
    color:#ff7373; }

span.bp3-icon-standard{
  line-height:1;
  font-family:"Icons16", sans-serif;
  font-size:16px;
  font-weight:400;
  font-style:normal;
  -moz-osx-font-smoothing:grayscale;
  -webkit-font-smoothing:antialiased;
  display:inline-block; }

span.bp3-icon-large{
  line-height:1;
  font-family:"Icons20", sans-serif;
  font-size:20px;
  font-weight:400;
  font-style:normal;
  -moz-osx-font-smoothing:grayscale;
  -webkit-font-smoothing:antialiased;
  display:inline-block; }

span.bp3-icon:empty{
  line-height:1;
  font-family:"Icons20";
  font-size:inherit;
  font-weight:400;
  font-style:normal; }
  span.bp3-icon:empty::before{
    -moz-osx-font-smoothing:grayscale;
    -webkit-font-smoothing:antialiased; }

.bp3-icon-add::before{
  content:""; }

.bp3-icon-add-column-left::before{
  content:""; }

.bp3-icon-add-column-right::before{
  content:""; }

.bp3-icon-add-row-bottom::before{
  content:""; }

.bp3-icon-add-row-top::before{
  content:""; }

.bp3-icon-add-to-artifact::before{
  content:""; }

.bp3-icon-add-to-folder::before{
  content:""; }

.bp3-icon-airplane::before{
  content:""; }

.bp3-icon-align-center::before{
  content:""; }

.bp3-icon-align-justify::before{
  content:""; }

.bp3-icon-align-left::before{
  content:""; }

.bp3-icon-align-right::before{
  content:""; }

.bp3-icon-alignment-bottom::before{
  content:""; }

.bp3-icon-alignment-horizontal-center::before{
  content:""; }

.bp3-icon-alignment-left::before{
  content:""; }

.bp3-icon-alignment-right::before{
  content:""; }

.bp3-icon-alignment-top::before{
  content:""; }

.bp3-icon-alignment-vertical-center::before{
  content:""; }

.bp3-icon-annotation::before{
  content:""; }

.bp3-icon-application::before{
  content:""; }

.bp3-icon-applications::before{
  content:""; }

.bp3-icon-archive::before{
  content:""; }

.bp3-icon-arrow-bottom-left::before{
  content:"↙"; }

.bp3-icon-arrow-bottom-right::before{
  content:"↘"; }

.bp3-icon-arrow-down::before{
  content:"↓"; }

.bp3-icon-arrow-left::before{
  content:"←"; }

.bp3-icon-arrow-right::before{
  content:"→"; }

.bp3-icon-arrow-top-left::before{
  content:"↖"; }

.bp3-icon-arrow-top-right::before{
  content:"↗"; }

.bp3-icon-arrow-up::before{
  content:"↑"; }

.bp3-icon-arrows-horizontal::before{
  content:"↔"; }

.bp3-icon-arrows-vertical::before{
  content:"↕"; }

.bp3-icon-asterisk::before{
  content:"*"; }

.bp3-icon-automatic-updates::before{
  content:""; }

.bp3-icon-badge::before{
  content:""; }

.bp3-icon-ban-circle::before{
  content:""; }

.bp3-icon-bank-account::before{
  content:""; }

.bp3-icon-barcode::before{
  content:""; }

.bp3-icon-blank::before{
  content:""; }

.bp3-icon-blocked-person::before{
  content:""; }

.bp3-icon-bold::before{
  content:""; }

.bp3-icon-book::before{
  content:""; }

.bp3-icon-bookmark::before{
  content:""; }

.bp3-icon-box::before{
  content:""; }

.bp3-icon-briefcase::before{
  content:""; }

.bp3-icon-bring-data::before{
  content:""; }

.bp3-icon-build::before{
  content:""; }

.bp3-icon-calculator::before{
  content:""; }

.bp3-icon-calendar::before{
  content:""; }

.bp3-icon-camera::before{
  content:""; }

.bp3-icon-caret-down::before{
  content:"⌄"; }

.bp3-icon-caret-left::before{
  content:"〈"; }

.bp3-icon-caret-right::before{
  content:"〉"; }

.bp3-icon-caret-up::before{
  content:"⌃"; }

.bp3-icon-cell-tower::before{
  content:""; }

.bp3-icon-changes::before{
  content:""; }

.bp3-icon-chart::before{
  content:""; }

.bp3-icon-chat::before{
  content:""; }

.bp3-icon-chevron-backward::before{
  content:""; }

.bp3-icon-chevron-down::before{
  content:""; }

.bp3-icon-chevron-forward::before{
  content:""; }

.bp3-icon-chevron-left::before{
  content:""; }

.bp3-icon-chevron-right::before{
  content:""; }

.bp3-icon-chevron-up::before{
  content:""; }

.bp3-icon-circle::before{
  content:""; }

.bp3-icon-circle-arrow-down::before{
  content:""; }

.bp3-icon-circle-arrow-left::before{
  content:""; }

.bp3-icon-circle-arrow-right::before{
  content:""; }

.bp3-icon-circle-arrow-up::before{
  content:""; }

.bp3-icon-citation::before{
  content:""; }

.bp3-icon-clean::before{
  content:""; }

.bp3-icon-clipboard::before{
  content:""; }

.bp3-icon-cloud::before{
  content:"☁"; }

.bp3-icon-cloud-download::before{
  content:""; }

.bp3-icon-cloud-upload::before{
  content:""; }

.bp3-icon-code::before{
  content:""; }

.bp3-icon-code-block::before{
  content:""; }

.bp3-icon-cog::before{
  content:""; }

.bp3-icon-collapse-all::before{
  content:""; }

.bp3-icon-column-layout::before{
  content:""; }

.bp3-icon-comment::before{
  content:""; }

.bp3-icon-comparison::before{
  content:""; }

.bp3-icon-compass::before{
  content:""; }

.bp3-icon-compressed::before{
  content:""; }

.bp3-icon-confirm::before{
  content:""; }

.bp3-icon-console::before{
  content:""; }

.bp3-icon-contrast::before{
  content:""; }

.bp3-icon-control::before{
  content:""; }

.bp3-icon-credit-card::before{
  content:""; }

.bp3-icon-cross::before{
  content:"✗"; }

.bp3-icon-crown::before{
  content:""; }

.bp3-icon-cube::before{
  content:""; }

.bp3-icon-cube-add::before{
  content:""; }

.bp3-icon-cube-remove::before{
  content:""; }

.bp3-icon-curved-range-chart::before{
  content:""; }

.bp3-icon-cut::before{
  content:""; }

.bp3-icon-dashboard::before{
  content:""; }

.bp3-icon-data-lineage::before{
  content:""; }

.bp3-icon-database::before{
  content:""; }

.bp3-icon-delete::before{
  content:""; }

.bp3-icon-delta::before{
  content:"Δ"; }

.bp3-icon-derive-column::before{
  content:""; }

.bp3-icon-desktop::before{
  content:""; }

.bp3-icon-diagram-tree::before{
  content:""; }

.bp3-icon-direction-left::before{
  content:""; }

.bp3-icon-direction-right::before{
  content:""; }

.bp3-icon-disable::before{
  content:""; }

.bp3-icon-document::before{
  content:""; }

.bp3-icon-document-open::before{
  content:""; }

.bp3-icon-document-share::before{
  content:""; }

.bp3-icon-dollar::before{
  content:"$"; }

.bp3-icon-dot::before{
  content:"•"; }

.bp3-icon-double-caret-horizontal::before{
  content:""; }

.bp3-icon-double-caret-vertical::before{
  content:""; }

.bp3-icon-double-chevron-down::before{
  content:""; }

.bp3-icon-double-chevron-left::before{
  content:""; }

.bp3-icon-double-chevron-right::before{
  content:""; }

.bp3-icon-double-chevron-up::before{
  content:""; }

.bp3-icon-doughnut-chart::before{
  content:""; }

.bp3-icon-download::before{
  content:""; }

.bp3-icon-drag-handle-horizontal::before{
  content:""; }

.bp3-icon-drag-handle-vertical::before{
  content:""; }

.bp3-icon-draw::before{
  content:""; }

.bp3-icon-drive-time::before{
  content:""; }

.bp3-icon-duplicate::before{
  content:""; }

.bp3-icon-edit::before{
  content:"✎"; }

.bp3-icon-eject::before{
  content:"⏏"; }

.bp3-icon-endorsed::before{
  content:""; }

.bp3-icon-envelope::before{
  content:"✉"; }

.bp3-icon-equals::before{
  content:""; }

.bp3-icon-eraser::before{
  content:""; }

.bp3-icon-error::before{
  content:""; }

.bp3-icon-euro::before{
  content:"€"; }

.bp3-icon-exchange::before{
  content:""; }

.bp3-icon-exclude-row::before{
  content:""; }

.bp3-icon-expand-all::before{
  content:""; }

.bp3-icon-export::before{
  content:""; }

.bp3-icon-eye-off::before{
  content:""; }

.bp3-icon-eye-on::before{
  content:""; }

.bp3-icon-eye-open::before{
  content:""; }

.bp3-icon-fast-backward::before{
  content:""; }

.bp3-icon-fast-forward::before{
  content:""; }

.bp3-icon-feed::before{
  content:""; }

.bp3-icon-feed-subscribed::before{
  content:""; }

.bp3-icon-film::before{
  content:""; }

.bp3-icon-filter::before{
  content:""; }

.bp3-icon-filter-keep::before{
  content:""; }

.bp3-icon-filter-list::before{
  content:""; }

.bp3-icon-filter-open::before{
  content:""; }

.bp3-icon-filter-remove::before{
  content:""; }

.bp3-icon-flag::before{
  content:"⚑"; }

.bp3-icon-flame::before{
  content:""; }

.bp3-icon-flash::before{
  content:""; }

.bp3-icon-floppy-disk::before{
  content:""; }

.bp3-icon-flow-branch::before{
  content:""; }

.bp3-icon-flow-end::before{
  content:""; }

.bp3-icon-flow-linear::before{
  content:""; }

.bp3-icon-flow-review::before{
  content:""; }

.bp3-icon-flow-review-branch::before{
  content:""; }

.bp3-icon-flows::before{
  content:""; }

.bp3-icon-folder-close::before{
  content:""; }

.bp3-icon-folder-new::before{
  content:""; }

.bp3-icon-folder-open::before{
  content:""; }

.bp3-icon-folder-shared::before{
  content:""; }

.bp3-icon-folder-shared-open::before{
  content:""; }

.bp3-icon-follower::before{
  content:""; }

.bp3-icon-following::before{
  content:""; }

.bp3-icon-font::before{
  content:""; }

.bp3-icon-fork::before{
  content:""; }

.bp3-icon-form::before{
  content:""; }

.bp3-icon-full-circle::before{
  content:""; }

.bp3-icon-full-stacked-chart::before{
  content:""; }

.bp3-icon-fullscreen::before{
  content:""; }

.bp3-icon-function::before{
  content:""; }

.bp3-icon-gantt-chart::before{
  content:""; }

.bp3-icon-geolocation::before{
  content:""; }

.bp3-icon-geosearch::before{
  content:""; }

.bp3-icon-git-branch::before{
  content:""; }

.bp3-icon-git-commit::before{
  content:""; }

.bp3-icon-git-merge::before{
  content:""; }

.bp3-icon-git-new-branch::before{
  content:""; }

.bp3-icon-git-pull::before{
  content:""; }

.bp3-icon-git-push::before{
  content:""; }

.bp3-icon-git-repo::before{
  content:""; }

.bp3-icon-glass::before{
  content:""; }

.bp3-icon-globe::before{
  content:""; }

.bp3-icon-globe-network::before{
  content:""; }

.bp3-icon-graph::before{
  content:""; }

.bp3-icon-graph-remove::before{
  content:""; }

.bp3-icon-greater-than::before{
  content:""; }

.bp3-icon-greater-than-or-equal-to::before{
  content:""; }

.bp3-icon-grid::before{
  content:""; }

.bp3-icon-grid-view::before{
  content:""; }

.bp3-icon-group-objects::before{
  content:""; }

.bp3-icon-grouped-bar-chart::before{
  content:""; }

.bp3-icon-hand::before{
  content:""; }

.bp3-icon-hand-down::before{
  content:""; }

.bp3-icon-hand-left::before{
  content:""; }

.bp3-icon-hand-right::before{
  content:""; }

.bp3-icon-hand-up::before{
  content:""; }

.bp3-icon-header::before{
  content:""; }

.bp3-icon-header-one::before{
  content:""; }

.bp3-icon-header-two::before{
  content:""; }

.bp3-icon-headset::before{
  content:""; }

.bp3-icon-heart::before{
  content:"♥"; }

.bp3-icon-heart-broken::before{
  content:""; }

.bp3-icon-heat-grid::before{
  content:""; }

.bp3-icon-heatmap::before{
  content:""; }

.bp3-icon-help::before{
  content:"?"; }

.bp3-icon-helper-management::before{
  content:""; }

.bp3-icon-highlight::before{
  content:""; }

.bp3-icon-history::before{
  content:""; }

.bp3-icon-home::before{
  content:"⌂"; }

.bp3-icon-horizontal-bar-chart::before{
  content:""; }

.bp3-icon-horizontal-bar-chart-asc::before{
  content:""; }

.bp3-icon-horizontal-bar-chart-desc::before{
  content:""; }

.bp3-icon-horizontal-distribution::before{
  content:""; }

.bp3-icon-id-number::before{
  content:""; }

.bp3-icon-image-rotate-left::before{
  content:""; }

.bp3-icon-image-rotate-right::before{
  content:""; }

.bp3-icon-import::before{
  content:""; }

.bp3-icon-inbox::before{
  content:""; }

.bp3-icon-inbox-filtered::before{
  content:""; }

.bp3-icon-inbox-geo::before{
  content:""; }

.bp3-icon-inbox-search::before{
  content:""; }

.bp3-icon-inbox-update::before{
  content:""; }

.bp3-icon-info-sign::before{
  content:"ℹ"; }

.bp3-icon-inheritance::before{
  content:""; }

.bp3-icon-inner-join::before{
  content:""; }

.bp3-icon-insert::before{
  content:""; }

.bp3-icon-intersection::before{
  content:""; }

.bp3-icon-ip-address::before{
  content:""; }

.bp3-icon-issue::before{
  content:""; }

.bp3-icon-issue-closed::before{
  content:""; }

.bp3-icon-issue-new::before{
  content:""; }

.bp3-icon-italic::before{
  content:""; }

.bp3-icon-join-table::before{
  content:""; }

.bp3-icon-key::before{
  content:""; }

.bp3-icon-key-backspace::before{
  content:""; }

.bp3-icon-key-command::before{
  content:""; }

.bp3-icon-key-control::before{
  content:""; }

.bp3-icon-key-delete::before{
  content:""; }

.bp3-icon-key-enter::before{
  content:""; }

.bp3-icon-key-escape::before{
  content:""; }

.bp3-icon-key-option::before{
  content:""; }

.bp3-icon-key-shift::before{
  content:""; }

.bp3-icon-key-tab::before{
  content:""; }

.bp3-icon-known-vehicle::before{
  content:""; }

.bp3-icon-label::before{
  content:""; }

.bp3-icon-layer::before{
  content:""; }

.bp3-icon-layers::before{
  content:""; }

.bp3-icon-layout::before{
  content:""; }

.bp3-icon-layout-auto::before{
  content:""; }

.bp3-icon-layout-balloon::before{
  content:""; }

.bp3-icon-layout-circle::before{
  content:""; }

.bp3-icon-layout-grid::before{
  content:""; }

.bp3-icon-layout-group-by::before{
  content:""; }

.bp3-icon-layout-hierarchy::before{
  content:""; }

.bp3-icon-layout-linear::before{
  content:""; }

.bp3-icon-layout-skew-grid::before{
  content:""; }

.bp3-icon-layout-sorted-clusters::before{
  content:""; }

.bp3-icon-learning::before{
  content:""; }

.bp3-icon-left-join::before{
  content:""; }

.bp3-icon-less-than::before{
  content:""; }

.bp3-icon-less-than-or-equal-to::before{
  content:""; }

.bp3-icon-lifesaver::before{
  content:""; }

.bp3-icon-lightbulb::before{
  content:""; }

.bp3-icon-link::before{
  content:""; }

.bp3-icon-list::before{
  content:"☰"; }

.bp3-icon-list-columns::before{
  content:""; }

.bp3-icon-list-detail-view::before{
  content:""; }

.bp3-icon-locate::before{
  content:""; }

.bp3-icon-lock::before{
  content:""; }

.bp3-icon-log-in::before{
  content:""; }

.bp3-icon-log-out::before{
  content:""; }

.bp3-icon-manual::before{
  content:""; }

.bp3-icon-manually-entered-data::before{
  content:""; }

.bp3-icon-map::before{
  content:""; }

.bp3-icon-map-create::before{
  content:""; }

.bp3-icon-map-marker::before{
  content:""; }

.bp3-icon-maximize::before{
  content:""; }

.bp3-icon-media::before{
  content:""; }

.bp3-icon-menu::before{
  content:""; }

.bp3-icon-menu-closed::before{
  content:""; }

.bp3-icon-menu-open::before{
  content:""; }

.bp3-icon-merge-columns::before{
  content:""; }

.bp3-icon-merge-links::before{
  content:""; }

.bp3-icon-minimize::before{
  content:""; }

.bp3-icon-minus::before{
  content:"−"; }

.bp3-icon-mobile-phone::before{
  content:""; }

.bp3-icon-mobile-video::before{
  content:""; }

.bp3-icon-moon::before{
  content:""; }

.bp3-icon-more::before{
  content:""; }

.bp3-icon-mountain::before{
  content:""; }

.bp3-icon-move::before{
  content:""; }

.bp3-icon-mugshot::before{
  content:""; }

.bp3-icon-multi-select::before{
  content:""; }

.bp3-icon-music::before{
  content:""; }

.bp3-icon-new-drawing::before{
  content:""; }

.bp3-icon-new-grid-item::before{
  content:""; }

.bp3-icon-new-layer::before{
  content:""; }

.bp3-icon-new-layers::before{
  content:""; }

.bp3-icon-new-link::before{
  content:""; }

.bp3-icon-new-object::before{
  content:""; }

.bp3-icon-new-person::before{
  content:""; }

.bp3-icon-new-prescription::before{
  content:""; }

.bp3-icon-new-text-box::before{
  content:""; }

.bp3-icon-ninja::before{
  content:""; }

.bp3-icon-not-equal-to::before{
  content:""; }

.bp3-icon-notifications::before{
  content:""; }

.bp3-icon-notifications-updated::before{
  content:""; }

.bp3-icon-numbered-list::before{
  content:""; }

.bp3-icon-numerical::before{
  content:""; }

.bp3-icon-office::before{
  content:""; }

.bp3-icon-offline::before{
  content:""; }

.bp3-icon-oil-field::before{
  content:""; }

.bp3-icon-one-column::before{
  content:""; }

.bp3-icon-outdated::before{
  content:""; }

.bp3-icon-page-layout::before{
  content:""; }

.bp3-icon-panel-stats::before{
  content:""; }

.bp3-icon-panel-table::before{
  content:""; }

.bp3-icon-paperclip::before{
  content:""; }

.bp3-icon-paragraph::before{
  content:""; }

.bp3-icon-path::before{
  content:""; }

.bp3-icon-path-search::before{
  content:""; }

.bp3-icon-pause::before{
  content:""; }

.bp3-icon-people::before{
  content:""; }

.bp3-icon-percentage::before{
  content:""; }

.bp3-icon-person::before{
  content:""; }

.bp3-icon-phone::before{
  content:"☎"; }

.bp3-icon-pie-chart::before{
  content:""; }

.bp3-icon-pin::before{
  content:""; }

.bp3-icon-pivot::before{
  content:""; }

.bp3-icon-pivot-table::before{
  content:""; }

.bp3-icon-play::before{
  content:""; }

.bp3-icon-plus::before{
  content:"+"; }

.bp3-icon-polygon-filter::before{
  content:""; }

.bp3-icon-power::before{
  content:""; }

.bp3-icon-predictive-analysis::before{
  content:""; }

.bp3-icon-prescription::before{
  content:""; }

.bp3-icon-presentation::before{
  content:""; }

.bp3-icon-print::before{
  content:"⎙"; }

.bp3-icon-projects::before{
  content:""; }

.bp3-icon-properties::before{
  content:""; }

.bp3-icon-property::before{
  content:""; }

.bp3-icon-publish-function::before{
  content:""; }

.bp3-icon-pulse::before{
  content:""; }

.bp3-icon-random::before{
  content:""; }

.bp3-icon-record::before{
  content:""; }

.bp3-icon-redo::before{
  content:""; }

.bp3-icon-refresh::before{
  content:""; }

.bp3-icon-regression-chart::before{
  content:""; }

.bp3-icon-remove::before{
  content:""; }

.bp3-icon-remove-column::before{
  content:""; }

.bp3-icon-remove-column-left::before{
  content:""; }

.bp3-icon-remove-column-right::before{
  content:""; }

.bp3-icon-remove-row-bottom::before{
  content:""; }

.bp3-icon-remove-row-top::before{
  content:""; }

.bp3-icon-repeat::before{
  content:""; }

.bp3-icon-reset::before{
  content:""; }

.bp3-icon-resolve::before{
  content:""; }

.bp3-icon-rig::before{
  content:""; }

.bp3-icon-right-join::before{
  content:""; }

.bp3-icon-ring::before{
  content:""; }

.bp3-icon-rotate-document::before{
  content:""; }

.bp3-icon-rotate-page::before{
  content:""; }

.bp3-icon-satellite::before{
  content:""; }

.bp3-icon-saved::before{
  content:""; }

.bp3-icon-scatter-plot::before{
  content:""; }

.bp3-icon-search::before{
  content:""; }

.bp3-icon-search-around::before{
  content:""; }

.bp3-icon-search-template::before{
  content:""; }

.bp3-icon-search-text::before{
  content:""; }

.bp3-icon-segmented-control::before{
  content:""; }

.bp3-icon-select::before{
  content:""; }

.bp3-icon-selection::before{
  content:"⦿"; }

.bp3-icon-send-to::before{
  content:""; }

.bp3-icon-send-to-graph::before{
  content:""; }

.bp3-icon-send-to-map::before{
  content:""; }

.bp3-icon-series-add::before{
  content:""; }

.bp3-icon-series-configuration::before{
  content:""; }

.bp3-icon-series-derived::before{
  content:""; }

.bp3-icon-series-filtered::before{
  content:""; }

.bp3-icon-series-search::before{
  content:""; }

.bp3-icon-settings::before{
  content:""; }

.bp3-icon-share::before{
  content:""; }

.bp3-icon-shield::before{
  content:""; }

.bp3-icon-shop::before{
  content:""; }

.bp3-icon-shopping-cart::before{
  content:""; }

.bp3-icon-signal-search::before{
  content:""; }

.bp3-icon-sim-card::before{
  content:""; }

.bp3-icon-slash::before{
  content:""; }

.bp3-icon-small-cross::before{
  content:""; }

.bp3-icon-small-minus::before{
  content:""; }

.bp3-icon-small-plus::before{
  content:""; }

.bp3-icon-small-tick::before{
  content:""; }

.bp3-icon-snowflake::before{
  content:""; }

.bp3-icon-social-media::before{
  content:""; }

.bp3-icon-sort::before{
  content:""; }

.bp3-icon-sort-alphabetical::before{
  content:""; }

.bp3-icon-sort-alphabetical-desc::before{
  content:""; }

.bp3-icon-sort-asc::before{
  content:""; }

.bp3-icon-sort-desc::before{
  content:""; }

.bp3-icon-sort-numerical::before{
  content:""; }

.bp3-icon-sort-numerical-desc::before{
  content:""; }

.bp3-icon-split-columns::before{
  content:""; }

.bp3-icon-square::before{
  content:""; }

.bp3-icon-stacked-chart::before{
  content:""; }

.bp3-icon-star::before{
  content:"★"; }

.bp3-icon-star-empty::before{
  content:"☆"; }

.bp3-icon-step-backward::before{
  content:""; }

.bp3-icon-step-chart::before{
  content:""; }

.bp3-icon-step-forward::before{
  content:""; }

.bp3-icon-stop::before{
  content:""; }

.bp3-icon-stopwatch::before{
  content:""; }

.bp3-icon-strikethrough::before{
  content:""; }

.bp3-icon-style::before{
  content:""; }

.bp3-icon-swap-horizontal::before{
  content:""; }

.bp3-icon-swap-vertical::before{
  content:""; }

.bp3-icon-symbol-circle::before{
  content:""; }

.bp3-icon-symbol-cross::before{
  content:""; }

.bp3-icon-symbol-diamond::before{
  content:""; }

.bp3-icon-symbol-square::before{
  content:""; }

.bp3-icon-symbol-triangle-down::before{
  content:""; }

.bp3-icon-symbol-triangle-up::before{
  content:""; }

.bp3-icon-tag::before{
  content:""; }

.bp3-icon-take-action::before{
  content:""; }

.bp3-icon-taxi::before{
  content:""; }

.bp3-icon-text-highlight::before{
  content:""; }

.bp3-icon-th::before{
  content:""; }

.bp3-icon-th-derived::before{
  content:""; }

.bp3-icon-th-disconnect::before{
  content:""; }

.bp3-icon-th-filtered::before{
  content:""; }

.bp3-icon-th-list::before{
  content:""; }

.bp3-icon-thumbs-down::before{
  content:""; }

.bp3-icon-thumbs-up::before{
  content:""; }

.bp3-icon-tick::before{
  content:"✓"; }

.bp3-icon-tick-circle::before{
  content:""; }

.bp3-icon-time::before{
  content:"⏲"; }

.bp3-icon-timeline-area-chart::before{
  content:""; }

.bp3-icon-timeline-bar-chart::before{
  content:""; }

.bp3-icon-timeline-events::before{
  content:""; }

.bp3-icon-timeline-line-chart::before{
  content:""; }

.bp3-icon-tint::before{
  content:""; }

.bp3-icon-torch::before{
  content:""; }

.bp3-icon-tractor::before{
  content:""; }

.bp3-icon-train::before{
  content:""; }

.bp3-icon-translate::before{
  content:""; }

.bp3-icon-trash::before{
  content:""; }

.bp3-icon-tree::before{
  content:""; }

.bp3-icon-trending-down::before{
  content:""; }

.bp3-icon-trending-up::before{
  content:""; }

.bp3-icon-truck::before{
  content:""; }

.bp3-icon-two-columns::before{
  content:""; }

.bp3-icon-unarchive::before{
  content:""; }

.bp3-icon-underline::before{
  content:"⎁"; }

.bp3-icon-undo::before{
  content:"⎌"; }

.bp3-icon-ungroup-objects::before{
  content:""; }

.bp3-icon-unknown-vehicle::before{
  content:""; }

.bp3-icon-unlock::before{
  content:""; }

.bp3-icon-unpin::before{
  content:""; }

.bp3-icon-unresolve::before{
  content:""; }

.bp3-icon-updated::before{
  content:""; }

.bp3-icon-upload::before{
  content:""; }

.bp3-icon-user::before{
  content:""; }

.bp3-icon-variable::before{
  content:""; }

.bp3-icon-vertical-bar-chart-asc::before{
  content:""; }

.bp3-icon-vertical-bar-chart-desc::before{
  content:""; }

.bp3-icon-vertical-distribution::before{
  content:""; }

.bp3-icon-video::before{
  content:""; }

.bp3-icon-volume-down::before{
  content:""; }

.bp3-icon-volume-off::before{
  content:""; }

.bp3-icon-volume-up::before{
  content:""; }

.bp3-icon-walk::before{
  content:""; }

.bp3-icon-warning-sign::before{
  content:""; }

.bp3-icon-waterfall-chart::before{
  content:""; }

.bp3-icon-widget::before{
  content:""; }

.bp3-icon-widget-button::before{
  content:""; }

.bp3-icon-widget-footer::before{
  content:""; }

.bp3-icon-widget-header::before{
  content:""; }

.bp3-icon-wrench::before{
  content:""; }

.bp3-icon-zoom-in::before{
  content:""; }

.bp3-icon-zoom-out::before{
  content:""; }

.bp3-icon-zoom-to-fit::before{
  content:""; }
.bp3-submenu > .bp3-popover-wrapper{
  display:block; }

.bp3-submenu .bp3-popover-target{
  display:block; }

.bp3-submenu.bp3-popover{
  -webkit-box-shadow:none;
          box-shadow:none;
  padding:0 5px; }
  .bp3-submenu.bp3-popover > .bp3-popover-content{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2); }
  .bp3-dark .bp3-submenu.bp3-popover, .bp3-submenu.bp3-popover.bp3-dark{
    -webkit-box-shadow:none;
            box-shadow:none; }
    .bp3-dark .bp3-submenu.bp3-popover > .bp3-popover-content, .bp3-submenu.bp3-popover.bp3-dark > .bp3-popover-content{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4); }
.bp3-menu{
  margin:0;
  border-radius:3px;
  background:#ffffff;
  min-width:180px;
  padding:5px;
  list-style:none;
  text-align:left;
  color:#182026; }

.bp3-menu-divider{
  display:block;
  margin:5px;
  border-top:1px solid rgba(16, 22, 26, 0.15); }
  .bp3-dark .bp3-menu-divider{
    border-top-color:rgba(255, 255, 255, 0.15); }

.bp3-menu-item{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:start;
      -ms-flex-align:start;
          align-items:flex-start;
  border-radius:2px;
  padding:5px 7px;
  text-decoration:none;
  line-height:20px;
  color:inherit;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-menu-item > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-menu-item > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-menu-item::before,
  .bp3-menu-item > *{
    margin-right:7px; }
  .bp3-menu-item:empty::before,
  .bp3-menu-item > :last-child{
    margin-right:0; }
  .bp3-menu-item > .bp3-fill{
    word-break:break-word; }
  .bp3-menu-item:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-menu-item{
    background-color:rgba(167, 182, 194, 0.3);
    cursor:pointer;
    text-decoration:none; }
  .bp3-menu-item.bp3-disabled{
    background-color:inherit;
    cursor:not-allowed;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-dark .bp3-menu-item{
    color:inherit; }
    .bp3-dark .bp3-menu-item:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-menu-item{
      background-color:rgba(138, 155, 168, 0.15);
      color:inherit; }
    .bp3-dark .bp3-menu-item.bp3-disabled{
      background-color:inherit;
      color:rgba(167, 182, 194, 0.6); }
  .bp3-menu-item.bp3-intent-primary{
    color:#106ba3; }
    .bp3-menu-item.bp3-intent-primary .bp3-icon{
      color:inherit; }
    .bp3-menu-item.bp3-intent-primary::before, .bp3-menu-item.bp3-intent-primary::after,
    .bp3-menu-item.bp3-intent-primary .bp3-menu-item-label{
      color:#106ba3; }
    .bp3-menu-item.bp3-intent-primary:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item, .bp3-menu-item.bp3-intent-primary.bp3-active{
      background-color:#137cbd; }
    .bp3-menu-item.bp3-intent-primary:active{
      background-color:#106ba3; }
    .bp3-menu-item.bp3-intent-primary:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item, .bp3-menu-item.bp3-intent-primary:hover::before, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item::before, .bp3-menu-item.bp3-intent-primary:hover::after, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item::after,
    .bp3-menu-item.bp3-intent-primary:hover .bp3-menu-item-label,
    .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item .bp3-menu-item-label, .bp3-menu-item.bp3-intent-primary:active, .bp3-menu-item.bp3-intent-primary:active::before, .bp3-menu-item.bp3-intent-primary:active::after,
    .bp3-menu-item.bp3-intent-primary:active .bp3-menu-item-label, .bp3-menu-item.bp3-intent-primary.bp3-active, .bp3-menu-item.bp3-intent-primary.bp3-active::before, .bp3-menu-item.bp3-intent-primary.bp3-active::after,
    .bp3-menu-item.bp3-intent-primary.bp3-active .bp3-menu-item-label{
      color:#ffffff; }
  .bp3-menu-item.bp3-intent-success{
    color:#0d8050; }
    .bp3-menu-item.bp3-intent-success .bp3-icon{
      color:inherit; }
    .bp3-menu-item.bp3-intent-success::before, .bp3-menu-item.bp3-intent-success::after,
    .bp3-menu-item.bp3-intent-success .bp3-menu-item-label{
      color:#0d8050; }
    .bp3-menu-item.bp3-intent-success:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item, .bp3-menu-item.bp3-intent-success.bp3-active{
      background-color:#0f9960; }
    .bp3-menu-item.bp3-intent-success:active{
      background-color:#0d8050; }
    .bp3-menu-item.bp3-intent-success:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item, .bp3-menu-item.bp3-intent-success:hover::before, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item::before, .bp3-menu-item.bp3-intent-success:hover::after, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item::after,
    .bp3-menu-item.bp3-intent-success:hover .bp3-menu-item-label,
    .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item .bp3-menu-item-label, .bp3-menu-item.bp3-intent-success:active, .bp3-menu-item.bp3-intent-success:active::before, .bp3-menu-item.bp3-intent-success:active::after,
    .bp3-menu-item.bp3-intent-success:active .bp3-menu-item-label, .bp3-menu-item.bp3-intent-success.bp3-active, .bp3-menu-item.bp3-intent-success.bp3-active::before, .bp3-menu-item.bp3-intent-success.bp3-active::after,
    .bp3-menu-item.bp3-intent-success.bp3-active .bp3-menu-item-label{
      color:#ffffff; }
  .bp3-menu-item.bp3-intent-warning{
    color:#bf7326; }
    .bp3-menu-item.bp3-intent-warning .bp3-icon{
      color:inherit; }
    .bp3-menu-item.bp3-intent-warning::before, .bp3-menu-item.bp3-intent-warning::after,
    .bp3-menu-item.bp3-intent-warning .bp3-menu-item-label{
      color:#bf7326; }
    .bp3-menu-item.bp3-intent-warning:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item, .bp3-menu-item.bp3-intent-warning.bp3-active{
      background-color:#d9822b; }
    .bp3-menu-item.bp3-intent-warning:active{
      background-color:#bf7326; }
    .bp3-menu-item.bp3-intent-warning:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item, .bp3-menu-item.bp3-intent-warning:hover::before, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item::before, .bp3-menu-item.bp3-intent-warning:hover::after, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item::after,
    .bp3-menu-item.bp3-intent-warning:hover .bp3-menu-item-label,
    .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item .bp3-menu-item-label, .bp3-menu-item.bp3-intent-warning:active, .bp3-menu-item.bp3-intent-warning:active::before, .bp3-menu-item.bp3-intent-warning:active::after,
    .bp3-menu-item.bp3-intent-warning:active .bp3-menu-item-label, .bp3-menu-item.bp3-intent-warning.bp3-active, .bp3-menu-item.bp3-intent-warning.bp3-active::before, .bp3-menu-item.bp3-intent-warning.bp3-active::after,
    .bp3-menu-item.bp3-intent-warning.bp3-active .bp3-menu-item-label{
      color:#ffffff; }
  .bp3-menu-item.bp3-intent-danger{
    color:#c23030; }
    .bp3-menu-item.bp3-intent-danger .bp3-icon{
      color:inherit; }
    .bp3-menu-item.bp3-intent-danger::before, .bp3-menu-item.bp3-intent-danger::after,
    .bp3-menu-item.bp3-intent-danger .bp3-menu-item-label{
      color:#c23030; }
    .bp3-menu-item.bp3-intent-danger:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item, .bp3-menu-item.bp3-intent-danger.bp3-active{
      background-color:#db3737; }
    .bp3-menu-item.bp3-intent-danger:active{
      background-color:#c23030; }
    .bp3-menu-item.bp3-intent-danger:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item, .bp3-menu-item.bp3-intent-danger:hover::before, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item::before, .bp3-menu-item.bp3-intent-danger:hover::after, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item::after,
    .bp3-menu-item.bp3-intent-danger:hover .bp3-menu-item-label,
    .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item .bp3-menu-item-label, .bp3-menu-item.bp3-intent-danger:active, .bp3-menu-item.bp3-intent-danger:active::before, .bp3-menu-item.bp3-intent-danger:active::after,
    .bp3-menu-item.bp3-intent-danger:active .bp3-menu-item-label, .bp3-menu-item.bp3-intent-danger.bp3-active, .bp3-menu-item.bp3-intent-danger.bp3-active::before, .bp3-menu-item.bp3-intent-danger.bp3-active::after,
    .bp3-menu-item.bp3-intent-danger.bp3-active .bp3-menu-item-label{
      color:#ffffff; }
  .bp3-menu-item::before{
    line-height:1;
    font-family:"Icons16", sans-serif;
    font-size:16px;
    font-weight:400;
    font-style:normal;
    -moz-osx-font-smoothing:grayscale;
    -webkit-font-smoothing:antialiased;
    margin-right:7px; }
  .bp3-menu-item::before,
  .bp3-menu-item > .bp3-icon{
    margin-top:2px;
    color:#5c7080; }
  .bp3-menu-item .bp3-menu-item-label{
    color:#5c7080; }
  .bp3-menu-item:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-menu-item{
    color:inherit; }
  .bp3-menu-item.bp3-active, .bp3-menu-item:active{
    background-color:rgba(115, 134, 148, 0.3); }
  .bp3-menu-item.bp3-disabled{
    outline:none !important;
    background-color:inherit !important;
    cursor:not-allowed !important;
    color:rgba(92, 112, 128, 0.6) !important; }
    .bp3-menu-item.bp3-disabled::before,
    .bp3-menu-item.bp3-disabled > .bp3-icon,
    .bp3-menu-item.bp3-disabled .bp3-menu-item-label{
      color:rgba(92, 112, 128, 0.6) !important; }
  .bp3-large .bp3-menu-item{
    padding:9px 7px;
    line-height:22px;
    font-size:16px; }
    .bp3-large .bp3-menu-item .bp3-icon{
      margin-top:3px; }
    .bp3-large .bp3-menu-item::before{
      line-height:1;
      font-family:"Icons20", sans-serif;
      font-size:20px;
      font-weight:400;
      font-style:normal;
      -moz-osx-font-smoothing:grayscale;
      -webkit-font-smoothing:antialiased;
      margin-top:1px;
      margin-right:10px; }

button.bp3-menu-item{
  border:none;
  background:none;
  width:100%;
  text-align:left; }
.bp3-menu-header{
  display:block;
  margin:5px;
  border-top:1px solid rgba(16, 22, 26, 0.15);
  cursor:default;
  padding-left:2px; }
  .bp3-dark .bp3-menu-header{
    border-top-color:rgba(255, 255, 255, 0.15); }
  .bp3-menu-header:first-of-type{
    border-top:none; }
  .bp3-menu-header > h6{
    color:#182026;
    font-weight:600;
    overflow:hidden;
    text-overflow:ellipsis;
    white-space:nowrap;
    word-wrap:normal;
    margin:0;
    padding:10px 7px 0 1px;
    line-height:17px; }
    .bp3-dark .bp3-menu-header > h6{
      color:#f5f8fa; }
  .bp3-menu-header:first-of-type > h6{
    padding-top:0; }
  .bp3-large .bp3-menu-header > h6{
    padding-top:15px;
    padding-bottom:5px;
    font-size:18px; }
  .bp3-large .bp3-menu-header:first-of-type > h6{
    padding-top:0; }

.bp3-dark .bp3-menu{
  background:#30404d;
  color:#f5f8fa; }

.bp3-dark .bp3-menu-item.bp3-intent-primary{
  color:#48aff0; }
  .bp3-dark .bp3-menu-item.bp3-intent-primary .bp3-icon{
    color:inherit; }
  .bp3-dark .bp3-menu-item.bp3-intent-primary::before, .bp3-dark .bp3-menu-item.bp3-intent-primary::after,
  .bp3-dark .bp3-menu-item.bp3-intent-primary .bp3-menu-item-label{
    color:#48aff0; }
  .bp3-dark .bp3-menu-item.bp3-intent-primary:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-primary.bp3-active{
    background-color:#137cbd; }
  .bp3-dark .bp3-menu-item.bp3-intent-primary:active{
    background-color:#106ba3; }
  .bp3-dark .bp3-menu-item.bp3-intent-primary:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-primary:hover::before, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item::before, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item::before, .bp3-dark .bp3-menu-item.bp3-intent-primary:hover::after, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item::after, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item::after,
  .bp3-dark .bp3-menu-item.bp3-intent-primary:hover .bp3-menu-item-label,
  .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item .bp3-menu-item-label,
  .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-primary:active, .bp3-dark .bp3-menu-item.bp3-intent-primary:active::before, .bp3-dark .bp3-menu-item.bp3-intent-primary:active::after,
  .bp3-dark .bp3-menu-item.bp3-intent-primary:active .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-primary.bp3-active, .bp3-dark .bp3-menu-item.bp3-intent-primary.bp3-active::before, .bp3-dark .bp3-menu-item.bp3-intent-primary.bp3-active::after,
  .bp3-dark .bp3-menu-item.bp3-intent-primary.bp3-active .bp3-menu-item-label{
    color:#ffffff; }

.bp3-dark .bp3-menu-item.bp3-intent-success{
  color:#3dcc91; }
  .bp3-dark .bp3-menu-item.bp3-intent-success .bp3-icon{
    color:inherit; }
  .bp3-dark .bp3-menu-item.bp3-intent-success::before, .bp3-dark .bp3-menu-item.bp3-intent-success::after,
  .bp3-dark .bp3-menu-item.bp3-intent-success .bp3-menu-item-label{
    color:#3dcc91; }
  .bp3-dark .bp3-menu-item.bp3-intent-success:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-success.bp3-active{
    background-color:#0f9960; }
  .bp3-dark .bp3-menu-item.bp3-intent-success:active{
    background-color:#0d8050; }
  .bp3-dark .bp3-menu-item.bp3-intent-success:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-success:hover::before, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item::before, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item::before, .bp3-dark .bp3-menu-item.bp3-intent-success:hover::after, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item::after, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item::after,
  .bp3-dark .bp3-menu-item.bp3-intent-success:hover .bp3-menu-item-label,
  .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item .bp3-menu-item-label,
  .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-success:active, .bp3-dark .bp3-menu-item.bp3-intent-success:active::before, .bp3-dark .bp3-menu-item.bp3-intent-success:active::after,
  .bp3-dark .bp3-menu-item.bp3-intent-success:active .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-success.bp3-active, .bp3-dark .bp3-menu-item.bp3-intent-success.bp3-active::before, .bp3-dark .bp3-menu-item.bp3-intent-success.bp3-active::after,
  .bp3-dark .bp3-menu-item.bp3-intent-success.bp3-active .bp3-menu-item-label{
    color:#ffffff; }

.bp3-dark .bp3-menu-item.bp3-intent-warning{
  color:#ffb366; }
  .bp3-dark .bp3-menu-item.bp3-intent-warning .bp3-icon{
    color:inherit; }
  .bp3-dark .bp3-menu-item.bp3-intent-warning::before, .bp3-dark .bp3-menu-item.bp3-intent-warning::after,
  .bp3-dark .bp3-menu-item.bp3-intent-warning .bp3-menu-item-label{
    color:#ffb366; }
  .bp3-dark .bp3-menu-item.bp3-intent-warning:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-warning.bp3-active{
    background-color:#d9822b; }
  .bp3-dark .bp3-menu-item.bp3-intent-warning:active{
    background-color:#bf7326; }
  .bp3-dark .bp3-menu-item.bp3-intent-warning:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-warning:hover::before, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item::before, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item::before, .bp3-dark .bp3-menu-item.bp3-intent-warning:hover::after, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item::after, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item::after,
  .bp3-dark .bp3-menu-item.bp3-intent-warning:hover .bp3-menu-item-label,
  .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item .bp3-menu-item-label,
  .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-warning:active, .bp3-dark .bp3-menu-item.bp3-intent-warning:active::before, .bp3-dark .bp3-menu-item.bp3-intent-warning:active::after,
  .bp3-dark .bp3-menu-item.bp3-intent-warning:active .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-warning.bp3-active, .bp3-dark .bp3-menu-item.bp3-intent-warning.bp3-active::before, .bp3-dark .bp3-menu-item.bp3-intent-warning.bp3-active::after,
  .bp3-dark .bp3-menu-item.bp3-intent-warning.bp3-active .bp3-menu-item-label{
    color:#ffffff; }

.bp3-dark .bp3-menu-item.bp3-intent-danger{
  color:#ff7373; }
  .bp3-dark .bp3-menu-item.bp3-intent-danger .bp3-icon{
    color:inherit; }
  .bp3-dark .bp3-menu-item.bp3-intent-danger::before, .bp3-dark .bp3-menu-item.bp3-intent-danger::after,
  .bp3-dark .bp3-menu-item.bp3-intent-danger .bp3-menu-item-label{
    color:#ff7373; }
  .bp3-dark .bp3-menu-item.bp3-intent-danger:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-danger.bp3-active{
    background-color:#db3737; }
  .bp3-dark .bp3-menu-item.bp3-intent-danger:active{
    background-color:#c23030; }
  .bp3-dark .bp3-menu-item.bp3-intent-danger:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-danger:hover::before, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item::before, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item::before, .bp3-dark .bp3-menu-item.bp3-intent-danger:hover::after, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item::after, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item::after,
  .bp3-dark .bp3-menu-item.bp3-intent-danger:hover .bp3-menu-item-label,
  .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item .bp3-menu-item-label,
  .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-danger:active, .bp3-dark .bp3-menu-item.bp3-intent-danger:active::before, .bp3-dark .bp3-menu-item.bp3-intent-danger:active::after,
  .bp3-dark .bp3-menu-item.bp3-intent-danger:active .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-danger.bp3-active, .bp3-dark .bp3-menu-item.bp3-intent-danger.bp3-active::before, .bp3-dark .bp3-menu-item.bp3-intent-danger.bp3-active::after,
  .bp3-dark .bp3-menu-item.bp3-intent-danger.bp3-active .bp3-menu-item-label{
    color:#ffffff; }

.bp3-dark .bp3-menu-item::before,
.bp3-dark .bp3-menu-item > .bp3-icon{
  color:#a7b6c2; }

.bp3-dark .bp3-menu-item .bp3-menu-item-label{
  color:#a7b6c2; }

.bp3-dark .bp3-menu-item.bp3-active, .bp3-dark .bp3-menu-item:active{
  background-color:rgba(138, 155, 168, 0.3); }

.bp3-dark .bp3-menu-item.bp3-disabled{
  color:rgba(167, 182, 194, 0.6) !important; }
  .bp3-dark .bp3-menu-item.bp3-disabled::before,
  .bp3-dark .bp3-menu-item.bp3-disabled > .bp3-icon,
  .bp3-dark .bp3-menu-item.bp3-disabled .bp3-menu-item-label{
    color:rgba(167, 182, 194, 0.6) !important; }

.bp3-dark .bp3-menu-divider,
.bp3-dark .bp3-menu-header{
  border-color:rgba(255, 255, 255, 0.15); }

.bp3-dark .bp3-menu-header > h6{
  color:#f5f8fa; }

.bp3-label .bp3-menu{
  margin-top:5px; }
.bp3-navbar{
  position:relative;
  z-index:10;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
  background-color:#ffffff;
  width:100%;
  height:50px;
  padding:0 15px; }
  .bp3-navbar.bp3-dark,
  .bp3-dark .bp3-navbar{
    background-color:#394b59; }
  .bp3-navbar.bp3-dark{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-navbar{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4); }
  .bp3-navbar.bp3-fixed-top{
    position:fixed;
    top:0;
    right:0;
    left:0; }

.bp3-navbar-heading{
  margin-right:15px;
  font-size:16px; }

.bp3-navbar-group{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  height:50px; }
  .bp3-navbar-group.bp3-align-left{
    float:left; }
  .bp3-navbar-group.bp3-align-right{
    float:right; }

.bp3-navbar-divider{
  margin:0 10px;
  border-left:1px solid rgba(16, 22, 26, 0.15);
  height:20px; }
  .bp3-dark .bp3-navbar-divider{
    border-left-color:rgba(255, 255, 255, 0.15); }
.bp3-non-ideal-state{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  width:100%;
  height:100%;
  text-align:center; }
  .bp3-non-ideal-state > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-non-ideal-state > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-non-ideal-state::before,
  .bp3-non-ideal-state > *{
    margin-bottom:20px; }
  .bp3-non-ideal-state:empty::before,
  .bp3-non-ideal-state > :last-child{
    margin-bottom:0; }
  .bp3-non-ideal-state > *{
    max-width:400px; }

.bp3-non-ideal-state-visual{
  color:rgba(92, 112, 128, 0.6);
  font-size:60px; }
  .bp3-dark .bp3-non-ideal-state-visual{
    color:rgba(167, 182, 194, 0.6); }

.bp3-overflow-list{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -ms-flex-wrap:nowrap;
      flex-wrap:nowrap;
  min-width:0; }

.bp3-overflow-list-spacer{
  -ms-flex-negative:1;
      flex-shrink:1;
  width:1px; }

body.bp3-overlay-open{
  overflow:hidden; }

.bp3-overlay{
  position:static;
  top:0;
  right:0;
  bottom:0;
  left:0;
  z-index:20; }
  .bp3-overlay:not(.bp3-overlay-open){
    pointer-events:none; }
  .bp3-overlay.bp3-overlay-container{
    position:fixed;
    overflow:hidden; }
    .bp3-overlay.bp3-overlay-container.bp3-overlay-inline{
      position:absolute; }
  .bp3-overlay.bp3-overlay-scroll-container{
    position:fixed;
    overflow:auto; }
    .bp3-overlay.bp3-overlay-scroll-container.bp3-overlay-inline{
      position:absolute; }
  .bp3-overlay.bp3-overlay-inline{
    display:inline;
    overflow:visible; }

.bp3-overlay-content{
  position:fixed;
  z-index:20; }
  .bp3-overlay-inline .bp3-overlay-content,
  .bp3-overlay-scroll-container .bp3-overlay-content{
    position:absolute; }

.bp3-overlay-backdrop{
  position:fixed;
  top:0;
  right:0;
  bottom:0;
  left:0;
  opacity:1;
  z-index:20;
  background-color:rgba(16, 22, 26, 0.7);
  overflow:auto;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-overlay-backdrop.bp3-overlay-enter, .bp3-overlay-backdrop.bp3-overlay-appear{
    opacity:0; }
  .bp3-overlay-backdrop.bp3-overlay-enter-active, .bp3-overlay-backdrop.bp3-overlay-appear-active{
    opacity:1;
    -webkit-transition-property:opacity;
    transition-property:opacity;
    -webkit-transition-duration:200ms;
            transition-duration:200ms;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
    -webkit-transition-delay:0;
            transition-delay:0; }
  .bp3-overlay-backdrop.bp3-overlay-exit{
    opacity:1; }
  .bp3-overlay-backdrop.bp3-overlay-exit-active{
    opacity:0;
    -webkit-transition-property:opacity;
    transition-property:opacity;
    -webkit-transition-duration:200ms;
            transition-duration:200ms;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
    -webkit-transition-delay:0;
            transition-delay:0; }
  .bp3-overlay-backdrop:focus{
    outline:none; }
  .bp3-overlay-inline .bp3-overlay-backdrop{
    position:absolute; }
.bp3-panel-stack{
  position:relative;
  overflow:hidden; }

.bp3-panel-stack-header{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -ms-flex-negative:0;
      flex-shrink:0;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  z-index:1;
  -webkit-box-shadow:0 1px rgba(16, 22, 26, 0.15);
          box-shadow:0 1px rgba(16, 22, 26, 0.15);
  height:30px; }
  .bp3-dark .bp3-panel-stack-header{
    -webkit-box-shadow:0 1px rgba(255, 255, 255, 0.15);
            box-shadow:0 1px rgba(255, 255, 255, 0.15); }
  .bp3-panel-stack-header > span{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    -webkit-box-flex:1;
        -ms-flex:1;
            flex:1;
    -webkit-box-align:stretch;
        -ms-flex-align:stretch;
            align-items:stretch; }
  .bp3-panel-stack-header .bp3-heading{
    margin:0 5px; }

.bp3-button.bp3-panel-stack-header-back{
  margin-left:5px;
  padding-left:0;
  white-space:nowrap; }
  .bp3-button.bp3-panel-stack-header-back .bp3-icon{
    margin:0 2px; }

.bp3-panel-stack-view{
  position:absolute;
  top:0;
  right:0;
  bottom:0;
  left:0;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  margin-right:-1px;
  border-right:1px solid rgba(16, 22, 26, 0.15);
  background-color:#ffffff;
  overflow-y:auto; }
  .bp3-dark .bp3-panel-stack-view{
    background-color:#30404d; }

.bp3-panel-stack-push .bp3-panel-stack-enter, .bp3-panel-stack-push .bp3-panel-stack-appear{
  -webkit-transform:translateX(100%);
          transform:translateX(100%);
  opacity:0; }

.bp3-panel-stack-push .bp3-panel-stack-enter-active, .bp3-panel-stack-push .bp3-panel-stack-appear-active{
  -webkit-transform:translate(0%);
          transform:translate(0%);
  opacity:1;
  -webkit-transition-property:opacity, -webkit-transform;
  transition-property:opacity, -webkit-transform;
  transition-property:transform, opacity;
  transition-property:transform, opacity, -webkit-transform;
  -webkit-transition-duration:400ms;
          transition-duration:400ms;
  -webkit-transition-timing-function:ease;
          transition-timing-function:ease;
  -webkit-transition-delay:0;
          transition-delay:0; }

.bp3-panel-stack-push .bp3-panel-stack-exit{
  -webkit-transform:translate(0%);
          transform:translate(0%);
  opacity:1; }

.bp3-panel-stack-push .bp3-panel-stack-exit-active{
  -webkit-transform:translateX(-50%);
          transform:translateX(-50%);
  opacity:0;
  -webkit-transition-property:opacity, -webkit-transform;
  transition-property:opacity, -webkit-transform;
  transition-property:transform, opacity;
  transition-property:transform, opacity, -webkit-transform;
  -webkit-transition-duration:400ms;
          transition-duration:400ms;
  -webkit-transition-timing-function:ease;
          transition-timing-function:ease;
  -webkit-transition-delay:0;
          transition-delay:0; }

.bp3-panel-stack-pop .bp3-panel-stack-enter, .bp3-panel-stack-pop .bp3-panel-stack-appear{
  -webkit-transform:translateX(-50%);
          transform:translateX(-50%);
  opacity:0; }

.bp3-panel-stack-pop .bp3-panel-stack-enter-active, .bp3-panel-stack-pop .bp3-panel-stack-appear-active{
  -webkit-transform:translate(0%);
          transform:translate(0%);
  opacity:1;
  -webkit-transition-property:opacity, -webkit-transform;
  transition-property:opacity, -webkit-transform;
  transition-property:transform, opacity;
  transition-property:transform, opacity, -webkit-transform;
  -webkit-transition-duration:400ms;
          transition-duration:400ms;
  -webkit-transition-timing-function:ease;
          transition-timing-function:ease;
  -webkit-transition-delay:0;
          transition-delay:0; }

.bp3-panel-stack-pop .bp3-panel-stack-exit{
  -webkit-transform:translate(0%);
          transform:translate(0%);
  opacity:1; }

.bp3-panel-stack-pop .bp3-panel-stack-exit-active{
  -webkit-transform:translateX(100%);
          transform:translateX(100%);
  opacity:0;
  -webkit-transition-property:opacity, -webkit-transform;
  transition-property:opacity, -webkit-transform;
  transition-property:transform, opacity;
  transition-property:transform, opacity, -webkit-transform;
  -webkit-transition-duration:400ms;
          transition-duration:400ms;
  -webkit-transition-timing-function:ease;
          transition-timing-function:ease;
  -webkit-transition-delay:0;
          transition-delay:0; }
.bp3-popover{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
  -webkit-transform:scale(1);
          transform:scale(1);
  display:inline-block;
  z-index:20;
  border-radius:3px; }
  .bp3-popover .bp3-popover-arrow{
    position:absolute;
    width:30px;
    height:30px; }
    .bp3-popover .bp3-popover-arrow::before{
      margin:5px;
      width:20px;
      height:20px; }
  .bp3-tether-element-attached-bottom.bp3-tether-target-attached-top > .bp3-popover{
    margin-top:-17px;
    margin-bottom:17px; }
    .bp3-tether-element-attached-bottom.bp3-tether-target-attached-top > .bp3-popover > .bp3-popover-arrow{
      bottom:-11px; }
      .bp3-tether-element-attached-bottom.bp3-tether-target-attached-top > .bp3-popover > .bp3-popover-arrow svg{
        -webkit-transform:rotate(-90deg);
                transform:rotate(-90deg); }
  .bp3-tether-element-attached-left.bp3-tether-target-attached-right > .bp3-popover{
    margin-left:17px; }
    .bp3-tether-element-attached-left.bp3-tether-target-attached-right > .bp3-popover > .bp3-popover-arrow{
      left:-11px; }
      .bp3-tether-element-attached-left.bp3-tether-target-attached-right > .bp3-popover > .bp3-popover-arrow svg{
        -webkit-transform:rotate(0);
                transform:rotate(0); }
  .bp3-tether-element-attached-top.bp3-tether-target-attached-bottom > .bp3-popover{
    margin-top:17px; }
    .bp3-tether-element-attached-top.bp3-tether-target-attached-bottom > .bp3-popover > .bp3-popover-arrow{
      top:-11px; }
      .bp3-tether-element-attached-top.bp3-tether-target-attached-bottom > .bp3-popover > .bp3-popover-arrow svg{
        -webkit-transform:rotate(90deg);
                transform:rotate(90deg); }
  .bp3-tether-element-attached-right.bp3-tether-target-attached-left > .bp3-popover{
    margin-right:17px;
    margin-left:-17px; }
    .bp3-tether-element-attached-right.bp3-tether-target-attached-left > .bp3-popover > .bp3-popover-arrow{
      right:-11px; }
      .bp3-tether-element-attached-right.bp3-tether-target-attached-left > .bp3-popover > .bp3-popover-arrow svg{
        -webkit-transform:rotate(180deg);
                transform:rotate(180deg); }
  .bp3-tether-element-attached-middle > .bp3-popover > .bp3-popover-arrow{
    top:50%;
    -webkit-transform:translateY(-50%);
            transform:translateY(-50%); }
  .bp3-tether-element-attached-center > .bp3-popover > .bp3-popover-arrow{
    right:50%;
    -webkit-transform:translateX(50%);
            transform:translateX(50%); }
  .bp3-tether-element-attached-top.bp3-tether-target-attached-top > .bp3-popover > .bp3-popover-arrow{
    top:-0.3934px; }
  .bp3-tether-element-attached-right.bp3-tether-target-attached-right > .bp3-popover > .bp3-popover-arrow{
    right:-0.3934px; }
  .bp3-tether-element-attached-left.bp3-tether-target-attached-left > .bp3-popover > .bp3-popover-arrow{
    left:-0.3934px; }
  .bp3-tether-element-attached-bottom.bp3-tether-target-attached-bottom > .bp3-popover > .bp3-popover-arrow{
    bottom:-0.3934px; }
  .bp3-tether-element-attached-top.bp3-tether-element-attached-left > .bp3-popover{
    -webkit-transform-origin:top left;
            transform-origin:top left; }
  .bp3-tether-element-attached-top.bp3-tether-element-attached-center > .bp3-popover{
    -webkit-transform-origin:top center;
            transform-origin:top center; }
  .bp3-tether-element-attached-top.bp3-tether-element-attached-right > .bp3-popover{
    -webkit-transform-origin:top right;
            transform-origin:top right; }
  .bp3-tether-element-attached-middle.bp3-tether-element-attached-left > .bp3-popover{
    -webkit-transform-origin:center left;
            transform-origin:center left; }
  .bp3-tether-element-attached-middle.bp3-tether-element-attached-center > .bp3-popover{
    -webkit-transform-origin:center center;
            transform-origin:center center; }
  .bp3-tether-element-attached-middle.bp3-tether-element-attached-right > .bp3-popover{
    -webkit-transform-origin:center right;
            transform-origin:center right; }
  .bp3-tether-element-attached-bottom.bp3-tether-element-attached-left > .bp3-popover{
    -webkit-transform-origin:bottom left;
            transform-origin:bottom left; }
  .bp3-tether-element-attached-bottom.bp3-tether-element-attached-center > .bp3-popover{
    -webkit-transform-origin:bottom center;
            transform-origin:bottom center; }
  .bp3-tether-element-attached-bottom.bp3-tether-element-attached-right > .bp3-popover{
    -webkit-transform-origin:bottom right;
            transform-origin:bottom right; }
  .bp3-popover .bp3-popover-content{
    background:#ffffff;
    color:inherit; }
  .bp3-popover .bp3-popover-arrow::before{
    -webkit-box-shadow:1px 1px 6px rgba(16, 22, 26, 0.2);
            box-shadow:1px 1px 6px rgba(16, 22, 26, 0.2); }
  .bp3-popover .bp3-popover-arrow-border{
    fill:#10161a;
    fill-opacity:0.1; }
  .bp3-popover .bp3-popover-arrow-fill{
    fill:#ffffff; }
  .bp3-popover-enter > .bp3-popover, .bp3-popover-appear > .bp3-popover{
    -webkit-transform:scale(0.3);
            transform:scale(0.3); }
  .bp3-popover-enter-active > .bp3-popover, .bp3-popover-appear-active > .bp3-popover{
    -webkit-transform:scale(1);
            transform:scale(1);
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
            transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
    -webkit-transition-delay:0;
            transition-delay:0; }
  .bp3-popover-exit > .bp3-popover{
    -webkit-transform:scale(1);
            transform:scale(1); }
  .bp3-popover-exit-active > .bp3-popover{
    -webkit-transform:scale(0.3);
            transform:scale(0.3);
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
            transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
    -webkit-transition-delay:0;
            transition-delay:0; }
  .bp3-popover .bp3-popover-content{
    position:relative;
    border-radius:3px; }
  .bp3-popover.bp3-popover-content-sizing .bp3-popover-content{
    max-width:350px;
    padding:20px; }
  .bp3-popover-target + .bp3-overlay .bp3-popover.bp3-popover-content-sizing{
    width:350px; }
  .bp3-popover.bp3-minimal{
    margin:0 !important; }
    .bp3-popover.bp3-minimal .bp3-popover-arrow{
      display:none; }
    .bp3-popover.bp3-minimal.bp3-popover{
      -webkit-transform:scale(1);
              transform:scale(1); }
      .bp3-popover-enter > .bp3-popover.bp3-minimal.bp3-popover, .bp3-popover-appear > .bp3-popover.bp3-minimal.bp3-popover{
        -webkit-transform:scale(1);
                transform:scale(1); }
      .bp3-popover-enter-active > .bp3-popover.bp3-minimal.bp3-popover, .bp3-popover-appear-active > .bp3-popover.bp3-minimal.bp3-popover{
        -webkit-transform:scale(1);
                transform:scale(1);
        -webkit-transition-property:-webkit-transform;
        transition-property:-webkit-transform;
        transition-property:transform;
        transition-property:transform, -webkit-transform;
        -webkit-transition-duration:100ms;
                transition-duration:100ms;
        -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
                transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
        -webkit-transition-delay:0;
                transition-delay:0; }
      .bp3-popover-exit > .bp3-popover.bp3-minimal.bp3-popover{
        -webkit-transform:scale(1);
                transform:scale(1); }
      .bp3-popover-exit-active > .bp3-popover.bp3-minimal.bp3-popover{
        -webkit-transform:scale(1);
                transform:scale(1);
        -webkit-transition-property:-webkit-transform;
        transition-property:-webkit-transform;
        transition-property:transform;
        transition-property:transform, -webkit-transform;
        -webkit-transition-duration:100ms;
                transition-duration:100ms;
        -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
                transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
        -webkit-transition-delay:0;
                transition-delay:0; }
  .bp3-popover.bp3-dark,
  .bp3-dark .bp3-popover{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4); }
    .bp3-popover.bp3-dark .bp3-popover-content,
    .bp3-dark .bp3-popover .bp3-popover-content{
      background:#30404d;
      color:inherit; }
    .bp3-popover.bp3-dark .bp3-popover-arrow::before,
    .bp3-dark .bp3-popover .bp3-popover-arrow::before{
      -webkit-box-shadow:1px 1px 6px rgba(16, 22, 26, 0.4);
              box-shadow:1px 1px 6px rgba(16, 22, 26, 0.4); }
    .bp3-popover.bp3-dark .bp3-popover-arrow-border,
    .bp3-dark .bp3-popover .bp3-popover-arrow-border{
      fill:#10161a;
      fill-opacity:0.2; }
    .bp3-popover.bp3-dark .bp3-popover-arrow-fill,
    .bp3-dark .bp3-popover .bp3-popover-arrow-fill{
      fill:#30404d; }

.bp3-popover-arrow::before{
  display:block;
  position:absolute;
  -webkit-transform:rotate(45deg);
          transform:rotate(45deg);
  border-radius:2px;
  content:""; }

.bp3-tether-pinned .bp3-popover-arrow{
  display:none; }

.bp3-popover-backdrop{
  background:rgba(255, 255, 255, 0); }

.bp3-transition-container{
  opacity:1;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  z-index:20; }
  .bp3-transition-container.bp3-popover-enter, .bp3-transition-container.bp3-popover-appear{
    opacity:0; }
  .bp3-transition-container.bp3-popover-enter-active, .bp3-transition-container.bp3-popover-appear-active{
    opacity:1;
    -webkit-transition-property:opacity;
    transition-property:opacity;
    -webkit-transition-duration:100ms;
            transition-duration:100ms;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
    -webkit-transition-delay:0;
            transition-delay:0; }
  .bp3-transition-container.bp3-popover-exit{
    opacity:1; }
  .bp3-transition-container.bp3-popover-exit-active{
    opacity:0;
    -webkit-transition-property:opacity;
    transition-property:opacity;
    -webkit-transition-duration:100ms;
            transition-duration:100ms;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
    -webkit-transition-delay:0;
            transition-delay:0; }
  .bp3-transition-container:focus{
    outline:none; }
  .bp3-transition-container.bp3-popover-leave .bp3-popover-content{
    pointer-events:none; }
  .bp3-transition-container[data-x-out-of-boundaries]{
    display:none; }

span.bp3-popover-target{
  display:inline-block; }

.bp3-popover-wrapper.bp3-fill{
  width:100%; }

.bp3-portal{
  position:absolute;
  top:0;
  right:0;
  left:0; }
@-webkit-keyframes linear-progress-bar-stripes{
  from{
    background-position:0 0; }
  to{
    background-position:30px 0; } }
@keyframes linear-progress-bar-stripes{
  from{
    background-position:0 0; }
  to{
    background-position:30px 0; } }

.bp3-progress-bar{
  display:block;
  position:relative;
  border-radius:40px;
  background:rgba(92, 112, 128, 0.2);
  width:100%;
  height:8px;
  overflow:hidden; }
  .bp3-progress-bar .bp3-progress-meter{
    position:absolute;
    border-radius:40px;
    background:linear-gradient(-45deg, rgba(255, 255, 255, 0.2) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.2) 50%, rgba(255, 255, 255, 0.2) 75%, transparent 75%);
    background-color:rgba(92, 112, 128, 0.8);
    background-size:30px 30px;
    width:100%;
    height:100%;
    -webkit-transition:width 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:width 200ms cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-progress-bar:not(.bp3-no-animation):not(.bp3-no-stripes) .bp3-progress-meter{
    animation:linear-progress-bar-stripes 300ms linear infinite reverse; }
  .bp3-progress-bar.bp3-no-stripes .bp3-progress-meter{
    background-image:none; }

.bp3-dark .bp3-progress-bar{
  background:rgba(16, 22, 26, 0.5); }
  .bp3-dark .bp3-progress-bar .bp3-progress-meter{
    background-color:#8a9ba8; }

.bp3-progress-bar.bp3-intent-primary .bp3-progress-meter{
  background-color:#137cbd; }

.bp3-progress-bar.bp3-intent-success .bp3-progress-meter{
  background-color:#0f9960; }

.bp3-progress-bar.bp3-intent-warning .bp3-progress-meter{
  background-color:#d9822b; }

.bp3-progress-bar.bp3-intent-danger .bp3-progress-meter{
  background-color:#db3737; }
@-webkit-keyframes skeleton-glow{
  from{
    border-color:rgba(206, 217, 224, 0.2);
    background:rgba(206, 217, 224, 0.2); }
  to{
    border-color:rgba(92, 112, 128, 0.2);
    background:rgba(92, 112, 128, 0.2); } }
@keyframes skeleton-glow{
  from{
    border-color:rgba(206, 217, 224, 0.2);
    background:rgba(206, 217, 224, 0.2); }
  to{
    border-color:rgba(92, 112, 128, 0.2);
    background:rgba(92, 112, 128, 0.2); } }
.bp3-skeleton{
  border-color:rgba(206, 217, 224, 0.2) !important;
  border-radius:2px;
  -webkit-box-shadow:none !important;
          box-shadow:none !important;
  background:rgba(206, 217, 224, 0.2);
  background-clip:padding-box !important;
  cursor:default;
  color:transparent !important;
  -webkit-animation:1000ms linear infinite alternate skeleton-glow;
          animation:1000ms linear infinite alternate skeleton-glow;
  pointer-events:none;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-skeleton::before, .bp3-skeleton::after,
  .bp3-skeleton *{
    visibility:hidden !important; }
.bp3-slider{
  width:100%;
  min-width:150px;
  height:40px;
  position:relative;
  outline:none;
  cursor:default;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-slider:hover{
    cursor:pointer; }
  .bp3-slider:active{
    cursor:-webkit-grabbing;
    cursor:grabbing; }
  .bp3-slider.bp3-disabled{
    opacity:0.5;
    cursor:not-allowed; }
  .bp3-slider.bp3-slider-unlabeled{
    height:16px; }

.bp3-slider-track,
.bp3-slider-progress{
  top:5px;
  right:0;
  left:0;
  height:6px;
  position:absolute; }

.bp3-slider-track{
  border-radius:3px;
  overflow:hidden; }

.bp3-slider-progress{
  background:rgba(92, 112, 128, 0.2); }
  .bp3-dark .bp3-slider-progress{
    background:rgba(16, 22, 26, 0.5); }
  .bp3-slider-progress.bp3-intent-primary{
    background-color:#137cbd; }
  .bp3-slider-progress.bp3-intent-success{
    background-color:#0f9960; }
  .bp3-slider-progress.bp3-intent-warning{
    background-color:#d9822b; }
  .bp3-slider-progress.bp3-intent-danger{
    background-color:#db3737; }

.bp3-slider-handle{
  -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
          box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
  background-color:#f5f8fa;
  background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.8)), to(rgba(255, 255, 255, 0)));
  background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.8), rgba(255, 255, 255, 0));
  color:#182026;
  position:absolute;
  top:0;
  left:0;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.2);
  cursor:pointer;
  width:16px;
  height:16px; }
  .bp3-slider-handle:hover{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
    background-clip:padding-box;
    background-color:#ebf1f5; }
  .bp3-slider-handle:active, .bp3-slider-handle.bp3-active{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
    background-color:#d8e1e8;
    background-image:none; }
  .bp3-slider-handle:disabled, .bp3-slider-handle.bp3-disabled{
    outline:none;
    -webkit-box-shadow:none;
            box-shadow:none;
    background-color:rgba(206, 217, 224, 0.5);
    background-image:none;
    cursor:not-allowed;
    color:rgba(92, 112, 128, 0.6); }
    .bp3-slider-handle:disabled.bp3-active, .bp3-slider-handle:disabled.bp3-active:hover, .bp3-slider-handle.bp3-disabled.bp3-active, .bp3-slider-handle.bp3-disabled.bp3-active:hover{
      background:rgba(206, 217, 224, 0.7); }
  .bp3-slider-handle:focus{
    z-index:1; }
  .bp3-slider-handle:hover{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
    background-clip:padding-box;
    background-color:#ebf1f5;
    z-index:2;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.2);
    cursor:-webkit-grab;
    cursor:grab; }
  .bp3-slider-handle.bp3-active{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
    background-color:#d8e1e8;
    background-image:none;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 1px rgba(16, 22, 26, 0.1);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 1px rgba(16, 22, 26, 0.1);
    cursor:-webkit-grabbing;
    cursor:grabbing; }
  .bp3-disabled .bp3-slider-handle{
    -webkit-box-shadow:none;
            box-shadow:none;
    background:#bfccd6;
    pointer-events:none; }
  .bp3-dark .bp3-slider-handle{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
    background-color:#394b59;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.05)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.05), rgba(255, 255, 255, 0));
    color:#f5f8fa; }
    .bp3-dark .bp3-slider-handle:hover, .bp3-dark .bp3-slider-handle:active, .bp3-dark .bp3-slider-handle.bp3-active{
      color:#f5f8fa; }
    .bp3-dark .bp3-slider-handle:hover{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
      background-color:#30404d; }
    .bp3-dark .bp3-slider-handle:active, .bp3-dark .bp3-slider-handle.bp3-active{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
      background-color:#202b33;
      background-image:none; }
    .bp3-dark .bp3-slider-handle:disabled, .bp3-dark .bp3-slider-handle.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none;
      background-color:rgba(57, 75, 89, 0.5);
      background-image:none;
      color:rgba(167, 182, 194, 0.6); }
      .bp3-dark .bp3-slider-handle:disabled.bp3-active, .bp3-dark .bp3-slider-handle.bp3-disabled.bp3-active{
        background:rgba(57, 75, 89, 0.7); }
    .bp3-dark .bp3-slider-handle .bp3-button-spinner .bp3-spinner-head{
      background:rgba(16, 22, 26, 0.5);
      stroke:#8a9ba8; }
    .bp3-dark .bp3-slider-handle, .bp3-dark .bp3-slider-handle:hover{
      background-color:#394b59; }
    .bp3-dark .bp3-slider-handle.bp3-active{
      background-color:#293742; }
  .bp3-dark .bp3-disabled .bp3-slider-handle{
    border-color:#5c7080;
    -webkit-box-shadow:none;
            box-shadow:none;
    background:#5c7080; }
  .bp3-slider-handle .bp3-slider-label{
    margin-left:8px;
    border-radius:3px;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
    background:#394b59;
    color:#f5f8fa; }
    .bp3-dark .bp3-slider-handle .bp3-slider-label{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
      background:#e1e8ed;
      color:#394b59; }
    .bp3-disabled .bp3-slider-handle .bp3-slider-label{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-slider-handle.bp3-start, .bp3-slider-handle.bp3-end{
    width:8px; }
  .bp3-slider-handle.bp3-start{
    border-top-right-radius:0;
    border-bottom-right-radius:0; }
  .bp3-slider-handle.bp3-end{
    margin-left:8px;
    border-top-left-radius:0;
    border-bottom-left-radius:0; }
    .bp3-slider-handle.bp3-end .bp3-slider-label{
      margin-left:0; }

.bp3-slider-label{
  -webkit-transform:translate(-50%, 20px);
          transform:translate(-50%, 20px);
  display:inline-block;
  position:absolute;
  padding:2px 5px;
  vertical-align:top;
  line-height:1;
  font-size:12px; }

.bp3-slider.bp3-vertical{
  width:40px;
  min-width:40px;
  height:150px; }
  .bp3-slider.bp3-vertical .bp3-slider-track,
  .bp3-slider.bp3-vertical .bp3-slider-progress{
    top:0;
    bottom:0;
    left:5px;
    width:6px;
    height:auto; }
  .bp3-slider.bp3-vertical .bp3-slider-progress{
    top:auto; }
  .bp3-slider.bp3-vertical .bp3-slider-label{
    -webkit-transform:translate(20px, 50%);
            transform:translate(20px, 50%); }
  .bp3-slider.bp3-vertical .bp3-slider-handle{
    top:auto; }
    .bp3-slider.bp3-vertical .bp3-slider-handle .bp3-slider-label{
      margin-top:-8px;
      margin-left:0; }
    .bp3-slider.bp3-vertical .bp3-slider-handle.bp3-end, .bp3-slider.bp3-vertical .bp3-slider-handle.bp3-start{
      margin-left:0;
      width:16px;
      height:8px; }
    .bp3-slider.bp3-vertical .bp3-slider-handle.bp3-start{
      border-top-left-radius:0;
      border-bottom-right-radius:3px; }
      .bp3-slider.bp3-vertical .bp3-slider-handle.bp3-start .bp3-slider-label{
        -webkit-transform:translate(20px);
                transform:translate(20px); }
    .bp3-slider.bp3-vertical .bp3-slider-handle.bp3-end{
      margin-bottom:8px;
      border-top-left-radius:3px;
      border-bottom-left-radius:0;
      border-bottom-right-radius:0; }

@-webkit-keyframes pt-spinner-animation{
  from{
    -webkit-transform:rotate(0deg);
            transform:rotate(0deg); }
  to{
    -webkit-transform:rotate(360deg);
            transform:rotate(360deg); } }

@keyframes pt-spinner-animation{
  from{
    -webkit-transform:rotate(0deg);
            transform:rotate(0deg); }
  to{
    -webkit-transform:rotate(360deg);
            transform:rotate(360deg); } }

.bp3-spinner{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  overflow:visible;
  vertical-align:middle; }
  .bp3-spinner svg{
    display:block; }
  .bp3-spinner path{
    fill-opacity:0; }
  .bp3-spinner .bp3-spinner-head{
    -webkit-transform-origin:center;
            transform-origin:center;
    -webkit-transition:stroke-dashoffset 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:stroke-dashoffset 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
    stroke:rgba(92, 112, 128, 0.8);
    stroke-linecap:round; }
  .bp3-spinner .bp3-spinner-track{
    stroke:rgba(92, 112, 128, 0.2); }

.bp3-spinner-animation{
  -webkit-animation:pt-spinner-animation 500ms linear infinite;
          animation:pt-spinner-animation 500ms linear infinite; }
  .bp3-no-spin > .bp3-spinner-animation{
    -webkit-animation:none;
            animation:none; }

.bp3-dark .bp3-spinner .bp3-spinner-head{
  stroke:#8a9ba8; }

.bp3-dark .bp3-spinner .bp3-spinner-track{
  stroke:rgba(16, 22, 26, 0.5); }

.bp3-spinner.bp3-intent-primary .bp3-spinner-head{
  stroke:#137cbd; }

.bp3-spinner.bp3-intent-success .bp3-spinner-head{
  stroke:#0f9960; }

.bp3-spinner.bp3-intent-warning .bp3-spinner-head{
  stroke:#d9822b; }

.bp3-spinner.bp3-intent-danger .bp3-spinner-head{
  stroke:#db3737; }
.bp3-tabs.bp3-vertical{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex; }
  .bp3-tabs.bp3-vertical > .bp3-tab-list{
    -webkit-box-orient:vertical;
    -webkit-box-direction:normal;
        -ms-flex-direction:column;
            flex-direction:column;
    -webkit-box-align:start;
        -ms-flex-align:start;
            align-items:flex-start; }
    .bp3-tabs.bp3-vertical > .bp3-tab-list .bp3-tab{
      border-radius:3px;
      width:100%;
      padding:0 10px; }
      .bp3-tabs.bp3-vertical > .bp3-tab-list .bp3-tab[aria-selected="true"]{
        -webkit-box-shadow:none;
                box-shadow:none;
        background-color:rgba(19, 124, 189, 0.2); }
    .bp3-tabs.bp3-vertical > .bp3-tab-list .bp3-tab-indicator-wrapper .bp3-tab-indicator{
      top:0;
      right:0;
      bottom:0;
      left:0;
      border-radius:3px;
      background-color:rgba(19, 124, 189, 0.2);
      height:auto; }
  .bp3-tabs.bp3-vertical > .bp3-tab-panel{
    margin-top:0;
    padding-left:20px; }

.bp3-tab-list{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  -webkit-box-align:end;
      -ms-flex-align:end;
          align-items:flex-end;
  position:relative;
  margin:0;
  border:none;
  padding:0;
  list-style:none; }
  .bp3-tab-list > *:not(:last-child){
    margin-right:20px; }

.bp3-tab{
  overflow:hidden;
  text-overflow:ellipsis;
  white-space:nowrap;
  word-wrap:normal;
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  position:relative;
  cursor:pointer;
  max-width:100%;
  vertical-align:top;
  line-height:30px;
  color:#182026;
  font-size:14px; }
  .bp3-tab a{
    display:block;
    text-decoration:none;
    color:inherit; }
  .bp3-tab-indicator-wrapper ~ .bp3-tab{
    -webkit-box-shadow:none !important;
            box-shadow:none !important;
    background-color:transparent !important; }
  .bp3-tab[aria-disabled="true"]{
    cursor:not-allowed;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-tab[aria-selected="true"]{
    border-radius:0;
    -webkit-box-shadow:inset 0 -3px 0 #106ba3;
            box-shadow:inset 0 -3px 0 #106ba3; }
  .bp3-tab[aria-selected="true"], .bp3-tab:not([aria-disabled="true"]):hover{
    color:#106ba3; }
  .bp3-tab:focus{
    -moz-outline-radius:0; }
  .bp3-large > .bp3-tab{
    line-height:40px;
    font-size:16px; }

.bp3-tab-panel{
  margin-top:20px; }
  .bp3-tab-panel[aria-hidden="true"]{
    display:none; }

.bp3-tab-indicator-wrapper{
  position:absolute;
  top:0;
  left:0;
  -webkit-transform:translateX(0), translateY(0);
          transform:translateX(0), translateY(0);
  -webkit-transition:height, width, -webkit-transform;
  transition:height, width, -webkit-transform;
  transition:height, transform, width;
  transition:height, transform, width, -webkit-transform;
  -webkit-transition-duration:200ms;
          transition-duration:200ms;
  -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
          transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
  pointer-events:none; }
  .bp3-tab-indicator-wrapper .bp3-tab-indicator{
    position:absolute;
    right:0;
    bottom:0;
    left:0;
    background-color:#106ba3;
    height:3px; }
  .bp3-tab-indicator-wrapper.bp3-no-animation{
    -webkit-transition:none;
    transition:none; }

.bp3-dark .bp3-tab{
  color:#f5f8fa; }
  .bp3-dark .bp3-tab[aria-disabled="true"]{
    color:rgba(167, 182, 194, 0.6); }
  .bp3-dark .bp3-tab[aria-selected="true"]{
    -webkit-box-shadow:inset 0 -3px 0 #48aff0;
            box-shadow:inset 0 -3px 0 #48aff0; }
  .bp3-dark .bp3-tab[aria-selected="true"], .bp3-dark .bp3-tab:not([aria-disabled="true"]):hover{
    color:#48aff0; }

.bp3-dark .bp3-tab-indicator{
  background-color:#48aff0; }

.bp3-flex-expander{
  -webkit-box-flex:1;
      -ms-flex:1 1;
          flex:1 1; }
.bp3-tag{
  display:-webkit-inline-box;
  display:-ms-inline-flexbox;
  display:inline-flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  position:relative;
  border:none;
  border-radius:3px;
  -webkit-box-shadow:none;
          box-shadow:none;
  background-color:#5c7080;
  min-width:20px;
  max-width:100%;
  min-height:20px;
  padding:2px 6px;
  line-height:16px;
  color:#f5f8fa;
  font-size:12px; }
  .bp3-tag.bp3-interactive{
    cursor:pointer; }
    .bp3-tag.bp3-interactive:hover{
      background-color:rgba(92, 112, 128, 0.85); }
    .bp3-tag.bp3-interactive.bp3-active, .bp3-tag.bp3-interactive:active{
      background-color:rgba(92, 112, 128, 0.7); }
  .bp3-tag > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-tag > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-tag::before,
  .bp3-tag > *{
    margin-right:4px; }
  .bp3-tag:empty::before,
  .bp3-tag > :last-child{
    margin-right:0; }
  .bp3-tag:focus{
    outline:rgba(19, 124, 189, 0.6) auto 2px;
    outline-offset:0;
    -moz-outline-radius:6px; }
  .bp3-tag.bp3-round{
    border-radius:30px;
    padding-right:8px;
    padding-left:8px; }
  .bp3-dark .bp3-tag{
    background-color:#bfccd6;
    color:#182026; }
    .bp3-dark .bp3-tag.bp3-interactive{
      cursor:pointer; }
      .bp3-dark .bp3-tag.bp3-interactive:hover{
        background-color:rgba(191, 204, 214, 0.85); }
      .bp3-dark .bp3-tag.bp3-interactive.bp3-active, .bp3-dark .bp3-tag.bp3-interactive:active{
        background-color:rgba(191, 204, 214, 0.7); }
    .bp3-dark .bp3-tag > .bp3-icon, .bp3-dark .bp3-tag .bp3-icon-standard, .bp3-dark .bp3-tag .bp3-icon-large{
      fill:currentColor; }
  .bp3-tag > .bp3-icon, .bp3-tag .bp3-icon-standard, .bp3-tag .bp3-icon-large{
    fill:#ffffff; }
  .bp3-tag.bp3-large,
  .bp3-large .bp3-tag{
    min-width:30px;
    min-height:30px;
    padding:0 10px;
    line-height:20px;
    font-size:14px; }
    .bp3-tag.bp3-large::before,
    .bp3-tag.bp3-large > *,
    .bp3-large .bp3-tag::before,
    .bp3-large .bp3-tag > *{
      margin-right:7px; }
    .bp3-tag.bp3-large:empty::before,
    .bp3-tag.bp3-large > :last-child,
    .bp3-large .bp3-tag:empty::before,
    .bp3-large .bp3-tag > :last-child{
      margin-right:0; }
    .bp3-tag.bp3-large.bp3-round,
    .bp3-large .bp3-tag.bp3-round{
      padding-right:12px;
      padding-left:12px; }
  .bp3-tag.bp3-intent-primary{
    background:#137cbd;
    color:#ffffff; }
    .bp3-tag.bp3-intent-primary.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-intent-primary.bp3-interactive:hover{
        background-color:rgba(19, 124, 189, 0.85); }
      .bp3-tag.bp3-intent-primary.bp3-interactive.bp3-active, .bp3-tag.bp3-intent-primary.bp3-interactive:active{
        background-color:rgba(19, 124, 189, 0.7); }
  .bp3-tag.bp3-intent-success{
    background:#0f9960;
    color:#ffffff; }
    .bp3-tag.bp3-intent-success.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-intent-success.bp3-interactive:hover{
        background-color:rgba(15, 153, 96, 0.85); }
      .bp3-tag.bp3-intent-success.bp3-interactive.bp3-active, .bp3-tag.bp3-intent-success.bp3-interactive:active{
        background-color:rgba(15, 153, 96, 0.7); }
  .bp3-tag.bp3-intent-warning{
    background:#d9822b;
    color:#ffffff; }
    .bp3-tag.bp3-intent-warning.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-intent-warning.bp3-interactive:hover{
        background-color:rgba(217, 130, 43, 0.85); }
      .bp3-tag.bp3-intent-warning.bp3-interactive.bp3-active, .bp3-tag.bp3-intent-warning.bp3-interactive:active{
        background-color:rgba(217, 130, 43, 0.7); }
  .bp3-tag.bp3-intent-danger{
    background:#db3737;
    color:#ffffff; }
    .bp3-tag.bp3-intent-danger.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-intent-danger.bp3-interactive:hover{
        background-color:rgba(219, 55, 55, 0.85); }
      .bp3-tag.bp3-intent-danger.bp3-interactive.bp3-active, .bp3-tag.bp3-intent-danger.bp3-interactive:active{
        background-color:rgba(219, 55, 55, 0.7); }
  .bp3-tag.bp3-fill{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    width:100%; }
  .bp3-tag.bp3-minimal > .bp3-icon, .bp3-tag.bp3-minimal .bp3-icon-standard, .bp3-tag.bp3-minimal .bp3-icon-large{
    fill:#5c7080; }
  .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]){
    background-color:rgba(138, 155, 168, 0.2);
    color:#182026; }
    .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive:hover{
        background-color:rgba(92, 112, 128, 0.3); }
      .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive.bp3-active, .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive:active{
        background-color:rgba(92, 112, 128, 0.4); }
    .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]){
      color:#f5f8fa; }
      .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive{
        cursor:pointer; }
        .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive:hover{
          background-color:rgba(191, 204, 214, 0.3); }
        .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive.bp3-active, .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive:active{
          background-color:rgba(191, 204, 214, 0.4); }
      .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]) > .bp3-icon, .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]) .bp3-icon-standard, .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]) .bp3-icon-large{
        fill:#a7b6c2; }
  .bp3-tag.bp3-minimal.bp3-intent-primary{
    background-color:rgba(19, 124, 189, 0.15);
    color:#106ba3; }
    .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive:hover{
        background-color:rgba(19, 124, 189, 0.25); }
      .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive.bp3-active, .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive:active{
        background-color:rgba(19, 124, 189, 0.35); }
    .bp3-tag.bp3-minimal.bp3-intent-primary > .bp3-icon, .bp3-tag.bp3-minimal.bp3-intent-primary .bp3-icon-standard, .bp3-tag.bp3-minimal.bp3-intent-primary .bp3-icon-large{
      fill:#137cbd; }
    .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-primary{
      background-color:rgba(19, 124, 189, 0.25);
      color:#48aff0; }
      .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive{
        cursor:pointer; }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive:hover{
          background-color:rgba(19, 124, 189, 0.35); }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive.bp3-active, .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive:active{
          background-color:rgba(19, 124, 189, 0.45); }
  .bp3-tag.bp3-minimal.bp3-intent-success{
    background-color:rgba(15, 153, 96, 0.15);
    color:#0d8050; }
    .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive:hover{
        background-color:rgba(15, 153, 96, 0.25); }
      .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive.bp3-active, .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive:active{
        background-color:rgba(15, 153, 96, 0.35); }
    .bp3-tag.bp3-minimal.bp3-intent-success > .bp3-icon, .bp3-tag.bp3-minimal.bp3-intent-success .bp3-icon-standard, .bp3-tag.bp3-minimal.bp3-intent-success .bp3-icon-large{
      fill:#0f9960; }
    .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-success{
      background-color:rgba(15, 153, 96, 0.25);
      color:#3dcc91; }
      .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive{
        cursor:pointer; }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive:hover{
          background-color:rgba(15, 153, 96, 0.35); }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive.bp3-active, .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive:active{
          background-color:rgba(15, 153, 96, 0.45); }
  .bp3-tag.bp3-minimal.bp3-intent-warning{
    background-color:rgba(217, 130, 43, 0.15);
    color:#bf7326; }
    .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive:hover{
        background-color:rgba(217, 130, 43, 0.25); }
      .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive.bp3-active, .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive:active{
        background-color:rgba(217, 130, 43, 0.35); }
    .bp3-tag.bp3-minimal.bp3-intent-warning > .bp3-icon, .bp3-tag.bp3-minimal.bp3-intent-warning .bp3-icon-standard, .bp3-tag.bp3-minimal.bp3-intent-warning .bp3-icon-large{
      fill:#d9822b; }
    .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-warning{
      background-color:rgba(217, 130, 43, 0.25);
      color:#ffb366; }
      .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive{
        cursor:pointer; }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive:hover{
          background-color:rgba(217, 130, 43, 0.35); }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive.bp3-active, .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive:active{
          background-color:rgba(217, 130, 43, 0.45); }
  .bp3-tag.bp3-minimal.bp3-intent-danger{
    background-color:rgba(219, 55, 55, 0.15);
    color:#c23030; }
    .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive:hover{
        background-color:rgba(219, 55, 55, 0.25); }
      .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive.bp3-active, .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive:active{
        background-color:rgba(219, 55, 55, 0.35); }
    .bp3-tag.bp3-minimal.bp3-intent-danger > .bp3-icon, .bp3-tag.bp3-minimal.bp3-intent-danger .bp3-icon-standard, .bp3-tag.bp3-minimal.bp3-intent-danger .bp3-icon-large{
      fill:#db3737; }
    .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-danger{
      background-color:rgba(219, 55, 55, 0.25);
      color:#ff7373; }
      .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive{
        cursor:pointer; }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive:hover{
          background-color:rgba(219, 55, 55, 0.35); }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive.bp3-active, .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive:active{
          background-color:rgba(219, 55, 55, 0.45); }

.bp3-tag-remove{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  opacity:0.5;
  margin-top:-2px;
  margin-right:-6px !important;
  margin-bottom:-2px;
  border:none;
  background:none;
  cursor:pointer;
  padding:2px;
  padding-left:0;
  color:inherit; }
  .bp3-tag-remove:hover{
    opacity:0.8;
    background:none;
    text-decoration:none; }
  .bp3-tag-remove:active{
    opacity:1; }
  .bp3-tag-remove:empty::before{
    line-height:1;
    font-family:"Icons16", sans-serif;
    font-size:16px;
    font-weight:400;
    font-style:normal;
    -moz-osx-font-smoothing:grayscale;
    -webkit-font-smoothing:antialiased;
    content:""; }
  .bp3-large .bp3-tag-remove{
    margin-right:-10px !important;
    padding:5px;
    padding-left:0; }
    .bp3-large .bp3-tag-remove:empty::before{
      line-height:1;
      font-family:"Icons20", sans-serif;
      font-size:20px;
      font-weight:400;
      font-style:normal; }
.bp3-tag-input{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:start;
      -ms-flex-align:start;
          align-items:flex-start;
  cursor:text;
  height:auto;
  min-height:30px;
  padding-right:0;
  padding-left:5px;
  line-height:inherit; }
  .bp3-tag-input > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-tag-input > .bp3-tag-input-values{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-tag-input .bp3-tag-input-icon{
    margin-top:7px;
    margin-right:7px;
    margin-left:2px;
    color:#5c7080; }
  .bp3-tag-input .bp3-tag-input-values{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    -webkit-box-orient:horizontal;
    -webkit-box-direction:normal;
        -ms-flex-direction:row;
            flex-direction:row;
    -ms-flex-wrap:wrap;
        flex-wrap:wrap;
    -webkit-box-align:center;
        -ms-flex-align:center;
            align-items:center;
    -ms-flex-item-align:stretch;
        align-self:stretch;
    margin-top:5px;
    margin-right:7px;
    min-width:0; }
    .bp3-tag-input .bp3-tag-input-values > *{
      -webkit-box-flex:0;
          -ms-flex-positive:0;
              flex-grow:0;
      -ms-flex-negative:0;
          flex-shrink:0; }
    .bp3-tag-input .bp3-tag-input-values > .bp3-fill{
      -webkit-box-flex:1;
          -ms-flex-positive:1;
              flex-grow:1;
      -ms-flex-negative:1;
          flex-shrink:1; }
    .bp3-tag-input .bp3-tag-input-values::before,
    .bp3-tag-input .bp3-tag-input-values > *{
      margin-right:5px; }
    .bp3-tag-input .bp3-tag-input-values:empty::before,
    .bp3-tag-input .bp3-tag-input-values > :last-child{
      margin-right:0; }
    .bp3-tag-input .bp3-tag-input-values:first-child .bp3-input-ghost:first-child{
      padding-left:5px; }
    .bp3-tag-input .bp3-tag-input-values > *{
      margin-bottom:5px; }
  .bp3-tag-input .bp3-tag{
    overflow-wrap:break-word; }
    .bp3-tag-input .bp3-tag.bp3-active{
      outline:rgba(19, 124, 189, 0.6) auto 2px;
      outline-offset:0;
      -moz-outline-radius:6px; }
  .bp3-tag-input .bp3-input-ghost{
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto;
    width:80px;
    line-height:20px; }
    .bp3-tag-input .bp3-input-ghost:disabled, .bp3-tag-input .bp3-input-ghost.bp3-disabled{
      cursor:not-allowed; }
  .bp3-tag-input .bp3-button,
  .bp3-tag-input .bp3-spinner{
    margin:3px;
    margin-left:0; }
  .bp3-tag-input .bp3-button{
    min-width:24px;
    min-height:24px;
    padding:0 7px; }
  .bp3-tag-input.bp3-large{
    height:auto;
    min-height:40px; }
    .bp3-tag-input.bp3-large::before,
    .bp3-tag-input.bp3-large > *{
      margin-right:10px; }
    .bp3-tag-input.bp3-large:empty::before,
    .bp3-tag-input.bp3-large > :last-child{
      margin-right:0; }
    .bp3-tag-input.bp3-large .bp3-tag-input-icon{
      margin-top:10px;
      margin-left:5px; }
    .bp3-tag-input.bp3-large .bp3-input-ghost{
      line-height:30px; }
    .bp3-tag-input.bp3-large .bp3-button{
      min-width:30px;
      min-height:30px;
      padding:5px 10px;
      margin:5px;
      margin-left:0; }
    .bp3-tag-input.bp3-large .bp3-spinner{
      margin:8px;
      margin-left:0; }
  .bp3-tag-input.bp3-active{
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
    background-color:#ffffff; }
    .bp3-tag-input.bp3-active.bp3-intent-primary{
      -webkit-box-shadow:0 0 0 1px #106ba3, 0 0 0 3px rgba(16, 107, 163, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #106ba3, 0 0 0 3px rgba(16, 107, 163, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-tag-input.bp3-active.bp3-intent-success{
      -webkit-box-shadow:0 0 0 1px #0d8050, 0 0 0 3px rgba(13, 128, 80, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #0d8050, 0 0 0 3px rgba(13, 128, 80, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-tag-input.bp3-active.bp3-intent-warning{
      -webkit-box-shadow:0 0 0 1px #bf7326, 0 0 0 3px rgba(191, 115, 38, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #bf7326, 0 0 0 3px rgba(191, 115, 38, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-tag-input.bp3-active.bp3-intent-danger{
      -webkit-box-shadow:0 0 0 1px #c23030, 0 0 0 3px rgba(194, 48, 48, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #c23030, 0 0 0 3px rgba(194, 48, 48, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-dark .bp3-tag-input .bp3-tag-input-icon, .bp3-tag-input.bp3-dark .bp3-tag-input-icon{
    color:#a7b6c2; }
  .bp3-dark .bp3-tag-input .bp3-input-ghost, .bp3-tag-input.bp3-dark .bp3-input-ghost{
    color:#f5f8fa; }
    .bp3-dark .bp3-tag-input .bp3-input-ghost::-webkit-input-placeholder, .bp3-tag-input.bp3-dark .bp3-input-ghost::-webkit-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-tag-input .bp3-input-ghost::-moz-placeholder, .bp3-tag-input.bp3-dark .bp3-input-ghost::-moz-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-tag-input .bp3-input-ghost:-ms-input-placeholder, .bp3-tag-input.bp3-dark .bp3-input-ghost:-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-tag-input .bp3-input-ghost::-ms-input-placeholder, .bp3-tag-input.bp3-dark .bp3-input-ghost::-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-tag-input .bp3-input-ghost::placeholder, .bp3-tag-input.bp3-dark .bp3-input-ghost::placeholder{
      color:rgba(167, 182, 194, 0.6); }
  .bp3-dark .bp3-tag-input.bp3-active, .bp3-tag-input.bp3-dark.bp3-active{
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
    background-color:rgba(16, 22, 26, 0.3); }
    .bp3-dark .bp3-tag-input.bp3-active.bp3-intent-primary, .bp3-tag-input.bp3-dark.bp3-active.bp3-intent-primary{
      -webkit-box-shadow:0 0 0 1px #106ba3, 0 0 0 3px rgba(16, 107, 163, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #106ba3, 0 0 0 3px rgba(16, 107, 163, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-tag-input.bp3-active.bp3-intent-success, .bp3-tag-input.bp3-dark.bp3-active.bp3-intent-success{
      -webkit-box-shadow:0 0 0 1px #0d8050, 0 0 0 3px rgba(13, 128, 80, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #0d8050, 0 0 0 3px rgba(13, 128, 80, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-tag-input.bp3-active.bp3-intent-warning, .bp3-tag-input.bp3-dark.bp3-active.bp3-intent-warning{
      -webkit-box-shadow:0 0 0 1px #bf7326, 0 0 0 3px rgba(191, 115, 38, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #bf7326, 0 0 0 3px rgba(191, 115, 38, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-tag-input.bp3-active.bp3-intent-danger, .bp3-tag-input.bp3-dark.bp3-active.bp3-intent-danger{
      -webkit-box-shadow:0 0 0 1px #c23030, 0 0 0 3px rgba(194, 48, 48, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #c23030, 0 0 0 3px rgba(194, 48, 48, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }

.bp3-input-ghost{
  border:none;
  -webkit-box-shadow:none;
          box-shadow:none;
  background:none;
  padding:0; }
  .bp3-input-ghost::-webkit-input-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-input-ghost::-moz-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-input-ghost:-ms-input-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-input-ghost::-ms-input-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-input-ghost::placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-input-ghost:focus{
    outline:none !important; }
.bp3-toast{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-align:start;
      -ms-flex-align:start;
          align-items:flex-start;
  position:relative !important;
  margin:20px 0 0;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
  background-color:#ffffff;
  min-width:300px;
  max-width:500px;
  pointer-events:all; }
  .bp3-toast.bp3-toast-enter, .bp3-toast.bp3-toast-appear{
    -webkit-transform:translateY(-40px);
            transform:translateY(-40px); }
  .bp3-toast.bp3-toast-enter-active, .bp3-toast.bp3-toast-appear-active{
    -webkit-transform:translateY(0);
            transform:translateY(0);
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
            transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
    -webkit-transition-delay:0;
            transition-delay:0; }
  .bp3-toast.bp3-toast-enter ~ .bp3-toast, .bp3-toast.bp3-toast-appear ~ .bp3-toast{
    -webkit-transform:translateY(-40px);
            transform:translateY(-40px); }
  .bp3-toast.bp3-toast-enter-active ~ .bp3-toast, .bp3-toast.bp3-toast-appear-active ~ .bp3-toast{
    -webkit-transform:translateY(0);
            transform:translateY(0);
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
            transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
    -webkit-transition-delay:0;
            transition-delay:0; }
  .bp3-toast.bp3-toast-exit{
    opacity:1;
    -webkit-filter:blur(0);
            filter:blur(0); }
  .bp3-toast.bp3-toast-exit-active{
    opacity:0;
    -webkit-filter:blur(10px);
            filter:blur(10px);
    -webkit-transition-property:opacity, -webkit-filter;
    transition-property:opacity, -webkit-filter;
    transition-property:opacity, filter;
    transition-property:opacity, filter, -webkit-filter;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
    -webkit-transition-delay:0;
            transition-delay:0; }
  .bp3-toast.bp3-toast-exit ~ .bp3-toast{
    -webkit-transform:translateY(0);
            transform:translateY(0); }
  .bp3-toast.bp3-toast-exit-active ~ .bp3-toast{
    -webkit-transform:translateY(-40px);
            transform:translateY(-40px);
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-duration:100ms;
            transition-duration:100ms;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
    -webkit-transition-delay:50ms;
            transition-delay:50ms; }
  .bp3-toast .bp3-button-group{
    -webkit-box-flex:0;
        -ms-flex:0 0 auto;
            flex:0 0 auto;
    padding:5px;
    padding-left:0; }
  .bp3-toast > .bp3-icon{
    margin:12px;
    margin-right:0;
    color:#5c7080; }
  .bp3-toast.bp3-dark,
  .bp3-dark .bp3-toast{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
    background-color:#394b59; }
    .bp3-toast.bp3-dark > .bp3-icon,
    .bp3-dark .bp3-toast > .bp3-icon{
      color:#a7b6c2; }
  .bp3-toast[class*="bp3-intent-"] a{
    color:rgba(255, 255, 255, 0.7); }
    .bp3-toast[class*="bp3-intent-"] a:hover{
      color:#ffffff; }
  .bp3-toast[class*="bp3-intent-"] > .bp3-icon{
    color:#ffffff; }
  .bp3-toast[class*="bp3-intent-"] .bp3-button, .bp3-toast[class*="bp3-intent-"] .bp3-button::before,
  .bp3-toast[class*="bp3-intent-"] .bp3-button .bp3-icon, .bp3-toast[class*="bp3-intent-"] .bp3-button:active{
    color:rgba(255, 255, 255, 0.7) !important; }
  .bp3-toast[class*="bp3-intent-"] .bp3-button:focus{
    outline-color:rgba(255, 255, 255, 0.5); }
  .bp3-toast[class*="bp3-intent-"] .bp3-button:hover{
    background-color:rgba(255, 255, 255, 0.15) !important;
    color:#ffffff !important; }
  .bp3-toast[class*="bp3-intent-"] .bp3-button:active{
    background-color:rgba(255, 255, 255, 0.3) !important;
    color:#ffffff !important; }
  .bp3-toast[class*="bp3-intent-"] .bp3-button::after{
    background:rgba(255, 255, 255, 0.3) !important; }
  .bp3-toast.bp3-intent-primary{
    background-color:#137cbd;
    color:#ffffff; }
  .bp3-toast.bp3-intent-success{
    background-color:#0f9960;
    color:#ffffff; }
  .bp3-toast.bp3-intent-warning{
    background-color:#d9822b;
    color:#ffffff; }
  .bp3-toast.bp3-intent-danger{
    background-color:#db3737;
    color:#ffffff; }

.bp3-toast-message{
  -webkit-box-flex:1;
      -ms-flex:1 1 auto;
          flex:1 1 auto;
  padding:11px;
  word-break:break-word; }

.bp3-toast-container{
  display:-webkit-box !important;
  display:-ms-flexbox !important;
  display:flex !important;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  position:fixed;
  right:0;
  left:0;
  z-index:40;
  overflow:hidden;
  padding:0 20px 20px;
  pointer-events:none; }
  .bp3-toast-container.bp3-toast-container-top{
    top:0;
    bottom:auto; }
  .bp3-toast-container.bp3-toast-container-bottom{
    -webkit-box-orient:vertical;
    -webkit-box-direction:reverse;
        -ms-flex-direction:column-reverse;
            flex-direction:column-reverse;
    top:auto;
    bottom:0; }
  .bp3-toast-container.bp3-toast-container-left{
    -webkit-box-align:start;
        -ms-flex-align:start;
            align-items:flex-start; }
  .bp3-toast-container.bp3-toast-container-right{
    -webkit-box-align:end;
        -ms-flex-align:end;
            align-items:flex-end; }

.bp3-toast-container-bottom .bp3-toast.bp3-toast-enter:not(.bp3-toast-enter-active),
.bp3-toast-container-bottom .bp3-toast.bp3-toast-enter:not(.bp3-toast-enter-active) ~ .bp3-toast, .bp3-toast-container-bottom .bp3-toast.bp3-toast-appear:not(.bp3-toast-appear-active),
.bp3-toast-container-bottom .bp3-toast.bp3-toast-appear:not(.bp3-toast-appear-active) ~ .bp3-toast,
.bp3-toast-container-bottom .bp3-toast.bp3-toast-leave-active ~ .bp3-toast{
  -webkit-transform:translateY(60px);
          transform:translateY(60px); }
.bp3-tooltip{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
  -webkit-transform:scale(1);
          transform:scale(1); }
  .bp3-tooltip .bp3-popover-arrow{
    position:absolute;
    width:22px;
    height:22px; }
    .bp3-tooltip .bp3-popover-arrow::before{
      margin:4px;
      width:14px;
      height:14px; }
  .bp3-tether-element-attached-bottom.bp3-tether-target-attached-top > .bp3-tooltip{
    margin-top:-11px;
    margin-bottom:11px; }
    .bp3-tether-element-attached-bottom.bp3-tether-target-attached-top > .bp3-tooltip > .bp3-popover-arrow{
      bottom:-8px; }
      .bp3-tether-element-attached-bottom.bp3-tether-target-attached-top > .bp3-tooltip > .bp3-popover-arrow svg{
        -webkit-transform:rotate(-90deg);
                transform:rotate(-90deg); }
  .bp3-tether-element-attached-left.bp3-tether-target-attached-right > .bp3-tooltip{
    margin-left:11px; }
    .bp3-tether-element-attached-left.bp3-tether-target-attached-right > .bp3-tooltip > .bp3-popover-arrow{
      left:-8px; }
      .bp3-tether-element-attached-left.bp3-tether-target-attached-right > .bp3-tooltip > .bp3-popover-arrow svg{
        -webkit-transform:rotate(0);
                transform:rotate(0); }
  .bp3-tether-element-attached-top.bp3-tether-target-attached-bottom > .bp3-tooltip{
    margin-top:11px; }
    .bp3-tether-element-attached-top.bp3-tether-target-attached-bottom > .bp3-tooltip > .bp3-popover-arrow{
      top:-8px; }
      .bp3-tether-element-attached-top.bp3-tether-target-attached-bottom > .bp3-tooltip > .bp3-popover-arrow svg{
        -webkit-transform:rotate(90deg);
                transform:rotate(90deg); }
  .bp3-tether-element-attached-right.bp3-tether-target-attached-left > .bp3-tooltip{
    margin-right:11px;
    margin-left:-11px; }
    .bp3-tether-element-attached-right.bp3-tether-target-attached-left > .bp3-tooltip > .bp3-popover-arrow{
      right:-8px; }
      .bp3-tether-element-attached-right.bp3-tether-target-attached-left > .bp3-tooltip > .bp3-popover-arrow svg{
        -webkit-transform:rotate(180deg);
                transform:rotate(180deg); }
  .bp3-tether-element-attached-middle > .bp3-tooltip > .bp3-popover-arrow{
    top:50%;
    -webkit-transform:translateY(-50%);
            transform:translateY(-50%); }
  .bp3-tether-element-attached-center > .bp3-tooltip > .bp3-popover-arrow{
    right:50%;
    -webkit-transform:translateX(50%);
            transform:translateX(50%); }
  .bp3-tether-element-attached-top.bp3-tether-target-attached-top > .bp3-tooltip > .bp3-popover-arrow{
    top:-0.22183px; }
  .bp3-tether-element-attached-right.bp3-tether-target-attached-right > .bp3-tooltip > .bp3-popover-arrow{
    right:-0.22183px; }
  .bp3-tether-element-attached-left.bp3-tether-target-attached-left > .bp3-tooltip > .bp3-popover-arrow{
    left:-0.22183px; }
  .bp3-tether-element-attached-bottom.bp3-tether-target-attached-bottom > .bp3-tooltip > .bp3-popover-arrow{
    bottom:-0.22183px; }
  .bp3-tether-element-attached-top.bp3-tether-element-attached-left > .bp3-tooltip{
    -webkit-transform-origin:top left;
            transform-origin:top left; }
  .bp3-tether-element-attached-top.bp3-tether-element-attached-center > .bp3-tooltip{
    -webkit-transform-origin:top center;
            transform-origin:top center; }
  .bp3-tether-element-attached-top.bp3-tether-element-attached-right > .bp3-tooltip{
    -webkit-transform-origin:top right;
            transform-origin:top right; }
  .bp3-tether-element-attached-middle.bp3-tether-element-attached-left > .bp3-tooltip{
    -webkit-transform-origin:center left;
            transform-origin:center left; }
  .bp3-tether-element-attached-middle.bp3-tether-element-attached-center > .bp3-tooltip{
    -webkit-transform-origin:center center;
            transform-origin:center center; }
  .bp3-tether-element-attached-middle.bp3-tether-element-attached-right > .bp3-tooltip{
    -webkit-transform-origin:center right;
            transform-origin:center right; }
  .bp3-tether-element-attached-bottom.bp3-tether-element-attached-left > .bp3-tooltip{
    -webkit-transform-origin:bottom left;
            transform-origin:bottom left; }
  .bp3-tether-element-attached-bottom.bp3-tether-element-attached-center > .bp3-tooltip{
    -webkit-transform-origin:bottom center;
            transform-origin:bottom center; }
  .bp3-tether-element-attached-bottom.bp3-tether-element-attached-right > .bp3-tooltip{
    -webkit-transform-origin:bottom right;
            transform-origin:bottom right; }
  .bp3-tooltip .bp3-popover-content{
    background:#394b59;
    color:#f5f8fa; }
  .bp3-tooltip .bp3-popover-arrow::before{
    -webkit-box-shadow:1px 1px 6px rgba(16, 22, 26, 0.2);
            box-shadow:1px 1px 6px rgba(16, 22, 26, 0.2); }
  .bp3-tooltip .bp3-popover-arrow-border{
    fill:#10161a;
    fill-opacity:0.1; }
  .bp3-tooltip .bp3-popover-arrow-fill{
    fill:#394b59; }
  .bp3-popover-enter > .bp3-tooltip, .bp3-popover-appear > .bp3-tooltip{
    -webkit-transform:scale(0.8);
            transform:scale(0.8); }
  .bp3-popover-enter-active > .bp3-tooltip, .bp3-popover-appear-active > .bp3-tooltip{
    -webkit-transform:scale(1);
            transform:scale(1);
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-duration:100ms;
            transition-duration:100ms;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
    -webkit-transition-delay:0;
            transition-delay:0; }
  .bp3-popover-exit > .bp3-tooltip{
    -webkit-transform:scale(1);
            transform:scale(1); }
  .bp3-popover-exit-active > .bp3-tooltip{
    -webkit-transform:scale(0.8);
            transform:scale(0.8);
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-duration:100ms;
            transition-duration:100ms;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
    -webkit-transition-delay:0;
            transition-delay:0; }
  .bp3-tooltip .bp3-popover-content{
    padding:10px 12px; }
  .bp3-tooltip.bp3-dark,
  .bp3-dark .bp3-tooltip{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4); }
    .bp3-tooltip.bp3-dark .bp3-popover-content,
    .bp3-dark .bp3-tooltip .bp3-popover-content{
      background:#e1e8ed;
      color:#394b59; }
    .bp3-tooltip.bp3-dark .bp3-popover-arrow::before,
    .bp3-dark .bp3-tooltip .bp3-popover-arrow::before{
      -webkit-box-shadow:1px 1px 6px rgba(16, 22, 26, 0.4);
              box-shadow:1px 1px 6px rgba(16, 22, 26, 0.4); }
    .bp3-tooltip.bp3-dark .bp3-popover-arrow-border,
    .bp3-dark .bp3-tooltip .bp3-popover-arrow-border{
      fill:#10161a;
      fill-opacity:0.2; }
    .bp3-tooltip.bp3-dark .bp3-popover-arrow-fill,
    .bp3-dark .bp3-tooltip .bp3-popover-arrow-fill{
      fill:#e1e8ed; }
  .bp3-tooltip.bp3-intent-primary .bp3-popover-content{
    background:#137cbd;
    color:#ffffff; }
  .bp3-tooltip.bp3-intent-primary .bp3-popover-arrow-fill{
    fill:#137cbd; }
  .bp3-tooltip.bp3-intent-success .bp3-popover-content{
    background:#0f9960;
    color:#ffffff; }
  .bp3-tooltip.bp3-intent-success .bp3-popover-arrow-fill{
    fill:#0f9960; }
  .bp3-tooltip.bp3-intent-warning .bp3-popover-content{
    background:#d9822b;
    color:#ffffff; }
  .bp3-tooltip.bp3-intent-warning .bp3-popover-arrow-fill{
    fill:#d9822b; }
  .bp3-tooltip.bp3-intent-danger .bp3-popover-content{
    background:#db3737;
    color:#ffffff; }
  .bp3-tooltip.bp3-intent-danger .bp3-popover-arrow-fill{
    fill:#db3737; }

.bp3-tooltip-indicator{
  border-bottom:dotted 1px;
  cursor:help; }
.bp3-tree .bp3-icon, .bp3-tree .bp3-icon-standard, .bp3-tree .bp3-icon-large{
  color:#5c7080; }
  .bp3-tree .bp3-icon.bp3-intent-primary, .bp3-tree .bp3-icon-standard.bp3-intent-primary, .bp3-tree .bp3-icon-large.bp3-intent-primary{
    color:#137cbd; }
  .bp3-tree .bp3-icon.bp3-intent-success, .bp3-tree .bp3-icon-standard.bp3-intent-success, .bp3-tree .bp3-icon-large.bp3-intent-success{
    color:#0f9960; }
  .bp3-tree .bp3-icon.bp3-intent-warning, .bp3-tree .bp3-icon-standard.bp3-intent-warning, .bp3-tree .bp3-icon-large.bp3-intent-warning{
    color:#d9822b; }
  .bp3-tree .bp3-icon.bp3-intent-danger, .bp3-tree .bp3-icon-standard.bp3-intent-danger, .bp3-tree .bp3-icon-large.bp3-intent-danger{
    color:#db3737; }

.bp3-tree-node-list{
  margin:0;
  padding-left:0;
  list-style:none; }

.bp3-tree-root{
  position:relative;
  background-color:transparent;
  cursor:default;
  padding-left:0; }

.bp3-tree-node-content-0{
  padding-left:0px; }

.bp3-tree-node-content-1{
  padding-left:23px; }

.bp3-tree-node-content-2{
  padding-left:46px; }

.bp3-tree-node-content-3{
  padding-left:69px; }

.bp3-tree-node-content-4{
  padding-left:92px; }

.bp3-tree-node-content-5{
  padding-left:115px; }

.bp3-tree-node-content-6{
  padding-left:138px; }

.bp3-tree-node-content-7{
  padding-left:161px; }

.bp3-tree-node-content-8{
  padding-left:184px; }

.bp3-tree-node-content-9{
  padding-left:207px; }

.bp3-tree-node-content-10{
  padding-left:230px; }

.bp3-tree-node-content-11{
  padding-left:253px; }

.bp3-tree-node-content-12{
  padding-left:276px; }

.bp3-tree-node-content-13{
  padding-left:299px; }

.bp3-tree-node-content-14{
  padding-left:322px; }

.bp3-tree-node-content-15{
  padding-left:345px; }

.bp3-tree-node-content-16{
  padding-left:368px; }

.bp3-tree-node-content-17{
  padding-left:391px; }

.bp3-tree-node-content-18{
  padding-left:414px; }

.bp3-tree-node-content-19{
  padding-left:437px; }

.bp3-tree-node-content-20{
  padding-left:460px; }

.bp3-tree-node-content{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  width:100%;
  height:30px;
  padding-right:5px; }
  .bp3-tree-node-content:hover{
    background-color:rgba(191, 204, 214, 0.4); }

.bp3-tree-node-caret,
.bp3-tree-node-caret-none{
  min-width:30px; }

.bp3-tree-node-caret{
  color:#5c7080;
  -webkit-transform:rotate(0deg);
          transform:rotate(0deg);
  cursor:pointer;
  padding:7px;
  -webkit-transition:-webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:-webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-tree-node-caret:hover{
    color:#182026; }
  .bp3-dark .bp3-tree-node-caret{
    color:#a7b6c2; }
    .bp3-dark .bp3-tree-node-caret:hover{
      color:#f5f8fa; }
  .bp3-tree-node-caret.bp3-tree-node-caret-open{
    -webkit-transform:rotate(90deg);
            transform:rotate(90deg); }
  .bp3-tree-node-caret.bp3-icon-standard::before{
    content:""; }

.bp3-tree-node-icon{
  position:relative;
  margin-right:7px; }

.bp3-tree-node-label{
  overflow:hidden;
  text-overflow:ellipsis;
  white-space:nowrap;
  word-wrap:normal;
  -webkit-box-flex:1;
      -ms-flex:1 1 auto;
          flex:1 1 auto;
  position:relative;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-tree-node-label span{
    display:inline; }

.bp3-tree-node-secondary-label{
  padding:0 5px;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-tree-node-secondary-label .bp3-popover-wrapper,
  .bp3-tree-node-secondary-label .bp3-popover-target{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    -webkit-box-align:center;
        -ms-flex-align:center;
            align-items:center; }

.bp3-tree-node.bp3-disabled .bp3-tree-node-content{
  background-color:inherit;
  cursor:not-allowed;
  color:rgba(92, 112, 128, 0.6); }

.bp3-tree-node.bp3-disabled .bp3-tree-node-caret,
.bp3-tree-node.bp3-disabled .bp3-tree-node-icon{
  cursor:not-allowed;
  color:rgba(92, 112, 128, 0.6); }

.bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content{
  background-color:#137cbd; }
  .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content,
  .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content .bp3-icon, .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content .bp3-icon-standard, .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content .bp3-icon-large{
    color:#ffffff; }
  .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content .bp3-tree-node-caret::before{
    color:rgba(255, 255, 255, 0.7); }
  .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content .bp3-tree-node-caret:hover::before{
    color:#ffffff; }

.bp3-dark .bp3-tree-node-content:hover{
  background-color:rgba(92, 112, 128, 0.3); }

.bp3-dark .bp3-tree .bp3-icon, .bp3-dark .bp3-tree .bp3-icon-standard, .bp3-dark .bp3-tree .bp3-icon-large{
  color:#a7b6c2; }
  .bp3-dark .bp3-tree .bp3-icon.bp3-intent-primary, .bp3-dark .bp3-tree .bp3-icon-standard.bp3-intent-primary, .bp3-dark .bp3-tree .bp3-icon-large.bp3-intent-primary{
    color:#137cbd; }
  .bp3-dark .bp3-tree .bp3-icon.bp3-intent-success, .bp3-dark .bp3-tree .bp3-icon-standard.bp3-intent-success, .bp3-dark .bp3-tree .bp3-icon-large.bp3-intent-success{
    color:#0f9960; }
  .bp3-dark .bp3-tree .bp3-icon.bp3-intent-warning, .bp3-dark .bp3-tree .bp3-icon-standard.bp3-intent-warning, .bp3-dark .bp3-tree .bp3-icon-large.bp3-intent-warning{
    color:#d9822b; }
  .bp3-dark .bp3-tree .bp3-icon.bp3-intent-danger, .bp3-dark .bp3-tree .bp3-icon-standard.bp3-intent-danger, .bp3-dark .bp3-tree .bp3-icon-large.bp3-intent-danger{
    color:#db3737; }

.bp3-dark .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content{
  background-color:#137cbd; }
/*!

Copyright 2017-present Palantir Technologies, Inc. All rights reserved.
Licensed under the Apache License, Version 2.0.

*/
.bp3-omnibar{
  -webkit-filter:blur(0);
          filter:blur(0);
  opacity:1;
  top:20vh;
  left:calc(50% - 250px);
  z-index:21;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
  background-color:#ffffff;
  width:500px; }
  .bp3-omnibar.bp3-overlay-enter, .bp3-omnibar.bp3-overlay-appear{
    -webkit-filter:blur(20px);
            filter:blur(20px);
    opacity:0.2; }
  .bp3-omnibar.bp3-overlay-enter-active, .bp3-omnibar.bp3-overlay-appear-active{
    -webkit-filter:blur(0);
            filter:blur(0);
    opacity:1;
    -webkit-transition-property:opacity, -webkit-filter;
    transition-property:opacity, -webkit-filter;
    transition-property:filter, opacity;
    transition-property:filter, opacity, -webkit-filter;
    -webkit-transition-duration:200ms;
            transition-duration:200ms;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
    -webkit-transition-delay:0;
            transition-delay:0; }
  .bp3-omnibar.bp3-overlay-exit{
    -webkit-filter:blur(0);
            filter:blur(0);
    opacity:1; }
  .bp3-omnibar.bp3-overlay-exit-active{
    -webkit-filter:blur(20px);
            filter:blur(20px);
    opacity:0.2;
    -webkit-transition-property:opacity, -webkit-filter;
    transition-property:opacity, -webkit-filter;
    transition-property:filter, opacity;
    transition-property:filter, opacity, -webkit-filter;
    -webkit-transition-duration:200ms;
            transition-duration:200ms;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
    -webkit-transition-delay:0;
            transition-delay:0; }
  .bp3-omnibar .bp3-input{
    border-radius:0;
    background-color:transparent; }
    .bp3-omnibar .bp3-input, .bp3-omnibar .bp3-input:focus{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-omnibar .bp3-menu{
    border-radius:0;
    -webkit-box-shadow:inset 0 1px 0 rgba(16, 22, 26, 0.15);
            box-shadow:inset 0 1px 0 rgba(16, 22, 26, 0.15);
    background-color:transparent;
    max-height:calc(60vh - 40px);
    overflow:auto; }
    .bp3-omnibar .bp3-menu:empty{
      display:none; }
  .bp3-dark .bp3-omnibar, .bp3-omnibar.bp3-dark{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
    background-color:#30404d; }

.bp3-omnibar-overlay .bp3-overlay-backdrop{
  background-color:rgba(16, 22, 26, 0.2); }

.bp3-select-popover .bp3-popover-content{
  padding:5px; }

.bp3-select-popover .bp3-input-group{
  margin-bottom:0; }

.bp3-select-popover .bp3-menu{
  max-width:400px;
  max-height:300px;
  overflow:auto;
  padding:0; }
  .bp3-select-popover .bp3-menu:not(:first-child){
    padding-top:5px; }

.bp3-multi-select{
  min-width:150px; }

.bp3-multi-select-popover .bp3-menu{
  max-width:400px;
  max-height:300px;
  overflow:auto; }

.bp3-select-popover .bp3-popover-content{
  padding:5px; }

.bp3-select-popover .bp3-input-group{
  margin-bottom:0; }

.bp3-select-popover .bp3-menu{
  max-width:400px;
  max-height:300px;
  overflow:auto;
  padding:0; }
  .bp3-select-popover .bp3-menu:not(:first-child){
    padding-top:5px; }
/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* This file was auto-generated by ensureUiComponents() in @jupyterlab/buildutils */

/**
 * (DEPRECATED) Support for consuming icons as CSS background images
 */

/* Icons urls */

:root {
  --jp-icon-add: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTE5IDEzaC02djZoLTJ2LTZINXYtMmg2VjVoMnY2aDZ2MnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-bug: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTIwIDhoLTIuODFjLS40NS0uNzgtMS4wNy0xLjQ1LTEuODItMS45NkwxNyA0LjQxIDE1LjU5IDNsLTIuMTcgMi4xN0MxMi45NiA1LjA2IDEyLjQ5IDUgMTIgNWMtLjQ5IDAtLjk2LjA2LTEuNDEuMTdMOC40MSAzIDcgNC40MWwxLjYyIDEuNjNDNy44OCA2LjU1IDcuMjYgNy4yMiA2LjgxIDhINHYyaDIuMDljLS4wNS4zMy0uMDkuNjYtLjA5IDF2MUg0djJoMnYxYzAgLjM0LjA0LjY3LjA5IDFINHYyaDIuODFjMS4wNCAxLjc5IDIuOTcgMyA1LjE5IDNzNC4xNS0xLjIxIDUuMTktM0gyMHYtMmgtMi4wOWMuMDUtLjMzLjA5LS42Ni4wOS0xdi0xaDJ2LTJoLTJ2LTFjMC0uMzQtLjA0LS42Ny0uMDktMUgyMFY4em0tNiA4aC00di0yaDR2MnptMC00aC00di0yaDR2MnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-build: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTYiIHZpZXdCb3g9IjAgMCAyNCAyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTE0LjkgMTcuNDVDMTYuMjUgMTcuNDUgMTcuMzUgMTYuMzUgMTcuMzUgMTVDMTcuMzUgMTMuNjUgMTYuMjUgMTIuNTUgMTQuOSAxMi41NUMxMy41NCAxMi41NSAxMi40NSAxMy42NSAxMi40NSAxNUMxMi40NSAxNi4zNSAxMy41NCAxNy40NSAxNC45IDE3LjQ1Wk0yMC4xIDE1LjY4TDIxLjU4IDE2Ljg0QzIxLjcxIDE2Ljk1IDIxLjc1IDE3LjEzIDIxLjY2IDE3LjI5TDIwLjI2IDE5LjcxQzIwLjE3IDE5Ljg2IDIwIDE5LjkyIDE5LjgzIDE5Ljg2TDE4LjA5IDE5LjE2QzE3LjczIDE5LjQ0IDE3LjMzIDE5LjY3IDE2LjkxIDE5Ljg1TDE2LjY0IDIxLjdDMTYuNjIgMjEuODcgMTYuNDcgMjIgMTYuMyAyMkgxMy41QzEzLjMyIDIyIDEzLjE4IDIxLjg3IDEzLjE1IDIxLjdMMTIuODkgMTkuODVDMTIuNDYgMTkuNjcgMTIuMDcgMTkuNDQgMTEuNzEgMTkuMTZMOS45NjAwMiAxOS44NkM5LjgxMDAyIDE5LjkyIDkuNjIwMDIgMTkuODYgOS41NDAwMiAxOS43MUw4LjE0MDAyIDE3LjI5QzguMDUwMDIgMTcuMTMgOC4wOTAwMiAxNi45NSA4LjIyMDAyIDE2Ljg0TDkuNzAwMDIgMTUuNjhMOS42NTAwMSAxNUw5LjcwMDAyIDE0LjMxTDguMjIwMDIgMTMuMTZDOC4wOTAwMiAxMy4wNSA4LjA1MDAyIDEyLjg2IDguMTQwMDIgMTIuNzFMOS41NDAwMiAxMC4yOUM5LjYyMDAyIDEwLjEzIDkuODEwMDIgMTAuMDcgOS45NjAwMiAxMC4xM0wxMS43MSAxMC44NEMxMi4wNyAxMC41NiAxMi40NiAxMC4zMiAxMi44OSAxMC4xNUwxMy4xNSA4LjI4OTk4QzEzLjE4IDguMTI5OTggMTMuMzIgNy45OTk5OCAxMy41IDcuOTk5OThIMTYuM0MxNi40NyA3Ljk5OTk4IDE2LjYyIDguMTI5OTggMTYuNjQgOC4yODk5OEwxNi45MSAxMC4xNUMxNy4zMyAxMC4zMiAxNy43MyAxMC41NiAxOC4wOSAxMC44NEwxOS44MyAxMC4xM0MyMCAxMC4wNyAyMC4xNyAxMC4xMyAyMC4yNiAxMC4yOUwyMS42NiAxMi43MUMyMS43NSAxMi44NiAyMS43MSAxMy4wNSAyMS41OCAxMy4xNkwyMC4xIDE0LjMxTDIwLjE1IDE1TDIwLjEgMTUuNjhaIi8+CiAgICA8cGF0aCBkPSJNNy4zMjk2NiA3LjQ0NDU0QzguMDgzMSA3LjAwOTU0IDguMzM5MzIgNi4wNTMzMiA3LjkwNDMyIDUuMjk5ODhDNy40NjkzMiA0LjU0NjQzIDYuNTA4MSA0LjI4MTU2IDUuNzU0NjYgNC43MTY1NkM1LjM5MTc2IDQuOTI2MDggNS4xMjY5NSA1LjI3MTE4IDUuMDE4NDkgNS42NzU5NEM0LjkxMDA0IDYuMDgwNzEgNC45NjY4MiA2LjUxMTk4IDUuMTc2MzQgNi44NzQ4OEM1LjYxMTM0IDcuNjI4MzIgNi41NzYyMiA3Ljg3OTU0IDcuMzI5NjYgNy40NDQ1NFpNOS42NTcxOCA0Ljc5NTkzTDEwLjg2NzIgNC45NTE3OUMxMC45NjI4IDQuOTc3NDEgMTEuMDQwMiA1LjA3MTMzIDExLjAzODIgNS4xODc5M0wxMS4wMzg4IDYuOTg4OTNDMTEuMDQ1NSA3LjEwMDU0IDEwLjk2MTYgNy4xOTUxOCAxMC44NTUgNy4yMTA1NEw5LjY2MDAxIDcuMzgwODNMOS4yMzkxNSA4LjEzMTg4TDkuNjY5NjEgOS4yNTc0NUM5LjcwNzI5IDkuMzYyNzEgOS42NjkzNCA5LjQ3Njk5IDkuNTc0MDggOS41MzE5OUw4LjAxNTIzIDEwLjQzMkM3LjkxMTMxIDEwLjQ5MiA3Ljc5MzM3IDEwLjQ2NzcgNy43MjEwNSAxMC4zODI0TDYuOTg3NDggOS40MzE4OEw2LjEwOTMxIDkuNDMwODNMNS4zNDcwNCAxMC4zOTA1QzUuMjg5MDkgMTAuNDcwMiA1LjE3MzgzIDEwLjQ5MDUgNS4wNzE4NyAxMC40MzM5TDMuNTEyNDUgOS41MzI5M0MzLjQxMDQ5IDkuNDc2MzMgMy4zNzY0NyA5LjM1NzQxIDMuNDEwNzUgOS4yNTY3OUwzLjg2MzQ3IDguMTQwOTNMMy42MTc0OSA3Ljc3NDg4TDMuNDIzNDcgNy4zNzg4M0wyLjIzMDc1IDcuMjEyOTdDMi4xMjY0NyA3LjE5MjM1IDIuMDQwNDkgNy4xMDM0MiAyLjA0MjQ1IDYuOTg2ODJMMi4wNDE4NyA1LjE4NTgyQzIuMDQzODMgNS4wNjkyMiAyLjExOTA5IDQuOTc5NTggMi4yMTcwNCA0Ljk2OTIyTDMuNDIwNjUgNC43OTM5M0wzLjg2NzQ5IDQuMDI3ODhMMy40MTEwNSAyLjkxNzMxQzMuMzczMzcgMi44MTIwNCAzLjQxMTMxIDIuNjk3NzYgMy41MTUyMyAyLjYzNzc2TDUuMDc0MDggMS43Mzc3NkM1LjE2OTM0IDEuNjgyNzYgNS4yODcyOSAxLjcwNzA0IDUuMzU5NjEgMS43OTIzMUw2LjExOTE1IDIuNzI3ODhMNi45ODAwMSAyLjczODkzTDcuNzI0OTYgMS43ODkyMkM3Ljc5MTU2IDEuNzA0NTggNy45MTU0OCAxLjY3OTIyIDguMDA4NzkgMS43NDA4Mkw5LjU2ODIxIDIuNjQxODJDOS42NzAxNyAyLjY5ODQyIDkuNzEyODUgMi44MTIzNCA5LjY4NzIzIDIuOTA3OTdMOS4yMTcxOCA0LjAzMzgzTDkuNDYzMTYgNC4zOTk4OEw5LjY1NzE4IDQuNzk1OTNaIi8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-caret-down-empty-thin: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwIDIwIj4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSIgc2hhcGUtcmVuZGVyaW5nPSJnZW9tZXRyaWNQcmVjaXNpb24iPgoJCTxwb2x5Z29uIGNsYXNzPSJzdDEiIHBvaW50cz0iOS45LDEzLjYgMy42LDcuNCA0LjQsNi42IDkuOSwxMi4yIDE1LjQsNi43IDE2LjEsNy40ICIvPgoJPC9nPgo8L3N2Zz4K);
  --jp-icon-caret-down-empty: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiIHNoYXBlLXJlbmRlcmluZz0iZ2VvbWV0cmljUHJlY2lzaW9uIj4KICAgIDxwYXRoIGQ9Ik01LjIsNS45TDksOS43bDMuOC0zLjhsMS4yLDEuMmwtNC45LDVsLTQuOS01TDUuMiw1Ljl6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-caret-down: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiIHNoYXBlLXJlbmRlcmluZz0iZ2VvbWV0cmljUHJlY2lzaW9uIj4KICAgIDxwYXRoIGQ9Ik01LjIsNy41TDksMTEuMmwzLjgtMy44SDUuMnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-caret-left: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSIgc2hhcGUtcmVuZGVyaW5nPSJnZW9tZXRyaWNQcmVjaXNpb24iPgoJCTxwYXRoIGQ9Ik0xMC44LDEyLjhMNy4xLDlsMy44LTMuOGwwLDcuNkgxMC44eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-caret-right: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiIHNoYXBlLXJlbmRlcmluZz0iZ2VvbWV0cmljUHJlY2lzaW9uIj4KICAgIDxwYXRoIGQ9Ik03LjIsNS4yTDEwLjksOWwtMy44LDMuOFY1LjJINy4yeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-caret-up-empty-thin: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwIDIwIj4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSIgc2hhcGUtcmVuZGVyaW5nPSJnZW9tZXRyaWNQcmVjaXNpb24iPgoJCTxwb2x5Z29uIGNsYXNzPSJzdDEiIHBvaW50cz0iMTUuNCwxMy4zIDkuOSw3LjcgNC40LDEzLjIgMy42LDEyLjUgOS45LDYuMyAxNi4xLDEyLjYgIi8+Cgk8L2c+Cjwvc3ZnPgo=);
  --jp-icon-caret-up: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSIgc2hhcGUtcmVuZGVyaW5nPSJnZW9tZXRyaWNQcmVjaXNpb24iPgoJCTxwYXRoIGQ9Ik01LjIsMTAuNUw5LDYuOGwzLjgsMy44SDUuMnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-case-sensitive: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwIDIwIj4KICA8ZyBjbGFzcz0ianAtaWNvbjIiIGZpbGw9IiM0MTQxNDEiPgogICAgPHJlY3QgeD0iMiIgeT0iMiIgd2lkdGg9IjE2IiBoZWlnaHQ9IjE2Ii8+CiAgPC9nPgogIDxnIGNsYXNzPSJqcC1pY29uLWFjY2VudDIiIGZpbGw9IiNGRkYiPgogICAgPHBhdGggZD0iTTcuNiw4aDAuOWwzLjUsOGgtMS4xTDEwLDE0SDZsLTAuOSwySDRMNy42LDh6IE04LDkuMUw2LjQsMTNoMy4yTDgsOS4xeiIvPgogICAgPHBhdGggZD0iTTE2LjYsOS44Yy0wLjIsMC4xLTAuNCwwLjEtMC43LDAuMWMtMC4yLDAtMC40LTAuMS0wLjYtMC4yYy0wLjEtMC4xLTAuMi0wLjQtMC4yLTAuNyBjLTAuMywwLjMtMC42LDAuNS0wLjksMC43Yy0wLjMsMC4xLTAuNywwLjItMS4xLDAuMmMtMC4zLDAtMC41LDAtMC43LTAuMWMtMC4yLTAuMS0wLjQtMC4yLTAuNi0wLjNjLTAuMi0wLjEtMC4zLTAuMy0wLjQtMC41IGMtMC4xLTAuMi0wLjEtMC40LTAuMS0wLjdjMC0wLjMsMC4xLTAuNiwwLjItMC44YzAuMS0wLjIsMC4zLTAuNCwwLjQtMC41QzEyLDcsMTIuMiw2LjksMTIuNSw2LjhjMC4yLTAuMSwwLjUtMC4xLDAuNy0wLjIgYzAuMy0wLjEsMC41LTAuMSwwLjctMC4xYzAuMiwwLDAuNC0wLjEsMC42LTAuMWMwLjIsMCwwLjMtMC4xLDAuNC0wLjJjMC4xLTAuMSwwLjItMC4yLDAuMi0wLjRjMC0xLTEuMS0xLTEuMy0xIGMtMC40LDAtMS40LDAtMS40LDEuMmgtMC45YzAtMC40LDAuMS0wLjcsMC4yLTFjMC4xLTAuMiwwLjMtMC40LDAuNS0wLjZjMC4yLTAuMiwwLjUtMC4zLDAuOC0wLjNDMTMuMyw0LDEzLjYsNCwxMy45LDQgYzAuMywwLDAuNSwwLDAuOCwwLjFjMC4zLDAsMC41LDAuMSwwLjcsMC4yYzAuMiwwLjEsMC40LDAuMywwLjUsMC41QzE2LDUsMTYsNS4yLDE2LDUuNnYyLjljMCwwLjIsMCwwLjQsMCwwLjUgYzAsMC4xLDAuMSwwLjIsMC4zLDAuMmMwLjEsMCwwLjIsMCwwLjMsMFY5Ljh6IE0xNS4yLDYuOWMtMS4yLDAuNi0zLjEsMC4yLTMuMSwxLjRjMCwxLjQsMy4xLDEsMy4xLTAuNVY2Ljl6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-check: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTkgMTYuMTdMNC44MyAxMmwtMS40MiAxLjQxTDkgMTkgMjEgN2wtMS40MS0xLjQxeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-circle-empty: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEyIDJDNi40NyAyIDIgNi40NyAyIDEyczQuNDcgMTAgMTAgMTAgMTAtNC40NyAxMC0xMFMxNy41MyAyIDEyIDJ6bTAgMThjLTQuNDEgMC04LTMuNTktOC04czMuNTktOCA4LTggOCAzLjU5IDggOC0zLjU5IDgtOCA4eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-circle: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMTggMTgiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPGNpcmNsZSBjeD0iOSIgY3k9IjkiIHI9IjgiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-clear: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8bWFzayBpZD0iZG9udXRIb2xlIj4KICAgIDxyZWN0IHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgZmlsbD0id2hpdGUiIC8+CiAgICA8Y2lyY2xlIGN4PSIxMiIgY3k9IjEyIiByPSI4IiBmaWxsPSJibGFjayIvPgogIDwvbWFzaz4KCiAgPGcgY2xhc3M9ImpwLWljb24zIiBmaWxsPSIjNjE2MTYxIj4KICAgIDxyZWN0IGhlaWdodD0iMTgiIHdpZHRoPSIyIiB4PSIxMSIgeT0iMyIgdHJhbnNmb3JtPSJyb3RhdGUoMzE1LCAxMiwgMTIpIi8+CiAgICA8Y2lyY2xlIGN4PSIxMiIgY3k9IjEyIiByPSIxMCIgbWFzaz0idXJsKCNkb251dEhvbGUpIi8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-close: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbi1ub25lIGpwLWljb24tc2VsZWN0YWJsZS1pbnZlcnNlIGpwLWljb24zLWhvdmVyIiBmaWxsPSJub25lIj4KICAgIDxjaXJjbGUgY3g9IjEyIiBjeT0iMTIiIHI9IjExIi8+CiAgPC9nPgoKICA8ZyBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIGpwLWljb24tYWNjZW50Mi1ob3ZlciIgZmlsbD0iIzYxNjE2MSI+CiAgICA8cGF0aCBkPSJNMTkgNi40MUwxNy41OSA1IDEyIDEwLjU5IDYuNDEgNSA1IDYuNDEgMTAuNTkgMTIgNSAxNy41OSA2LjQxIDE5IDEyIDEzLjQxIDE3LjU5IDE5IDE5IDE3LjU5IDEzLjQxIDEyeiIvPgogIDwvZz4KCiAgPGcgY2xhc3M9ImpwLWljb24tbm9uZSBqcC1pY29uLWJ1c3kiIGZpbGw9Im5vbmUiPgogICAgPGNpcmNsZSBjeD0iMTIiIGN5PSIxMiIgcj0iNyIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-console: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwMCAyMDAiPgogIDxnIGNsYXNzPSJqcC1pY29uLWJyYW5kMSBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiMwMjg4RDEiPgogICAgPHBhdGggZD0iTTIwIDE5LjhoMTYwdjE1OS45SDIweiIvPgogIDwvZz4KICA8ZyBjbGFzcz0ianAtaWNvbi1zZWxlY3RhYmxlLWludmVyc2UiIGZpbGw9IiNmZmYiPgogICAgPHBhdGggZD0iTTEwNSAxMjcuM2g0MHYxMi44aC00MHpNNTEuMSA3N0w3NCA5OS45bC0yMy4zIDIzLjMgMTAuNSAxMC41IDIzLjMtMjMuM0w5NSA5OS45IDg0LjUgODkuNCA2MS42IDY2LjV6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-copy: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMTggMTgiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTExLjksMUgzLjJDMi40LDEsMS43LDEuNywxLjcsMi41djEwLjJoMS41VjIuNWg4LjdWMXogTTE0LjEsMy45aC04Yy0wLjgsMC0xLjUsMC43LTEuNSwxLjV2MTAuMmMwLDAuOCwwLjcsMS41LDEuNSwxLjVoOCBjMC44LDAsMS41LTAuNywxLjUtMS41VjUuNEMxNS41LDQuNiwxNC45LDMuOSwxNC4xLDMuOXogTTE0LjEsMTUuNWgtOFY1LjRoOFYxNS41eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-cut: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTkuNjQgNy42NGMuMjMtLjUuMzYtMS4wNS4zNi0xLjY0IDAtMi4yMS0xLjc5LTQtNC00UzIgMy43OSAyIDZzMS43OSA0IDQgNGMuNTkgMCAxLjE0LS4xMyAxLjY0LS4zNkwxMCAxMmwtMi4zNiAyLjM2QzcuMTQgMTQuMTMgNi41OSAxNCA2IDE0Yy0yLjIxIDAtNCAxLjc5LTQgNHMxLjc5IDQgNCA0IDQtMS43OSA0LTRjMC0uNTktLjEzLTEuMTQtLjM2LTEuNjRMMTIgMTRsNyA3aDN2LTFMOS42NCA3LjY0ek02IDhjLTEuMSAwLTItLjg5LTItMnMuOS0yIDItMiAyIC44OSAyIDItLjkgMi0yIDJ6bTAgMTJjLTEuMSAwLTItLjg5LTItMnMuOS0yIDItMiAyIC44OSAyIDItLjkgMi0yIDJ6bTYtNy41Yy0uMjggMC0uNS0uMjItLjUtLjVzLjIyLS41LjUtLjUuNS4yMi41LjUtLjIyLjUtLjUuNXpNMTkgM2wtNiA2IDIgMiA3LTdWM3oiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-download: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTE5IDloLTRWM0g5djZINWw3IDcgNy03ek01IDE4djJoMTR2LTJINXoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-edit: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTMgMTcuMjVWMjFoMy43NUwxNy44MSA5Ljk0bC0zLjc1LTMuNzVMMyAxNy4yNXpNMjAuNzEgNy4wNGMuMzktLjM5LjM5LTEuMDIgMC0xLjQxbC0yLjM0LTIuMzRjLS4zOS0uMzktMS4wMi0uMzktMS40MSAwbC0xLjgzIDEuODMgMy43NSAzLjc1IDEuODMtMS44M3oiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-ellipses: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPGNpcmNsZSBjeD0iNSIgY3k9IjEyIiByPSIyIi8+CiAgICA8Y2lyY2xlIGN4PSIxMiIgY3k9IjEyIiByPSIyIi8+CiAgICA8Y2lyY2xlIGN4PSIxOSIgY3k9IjEyIiByPSIyIi8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-extension: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTIwLjUgMTFIMTlWN2MwLTEuMS0uOS0yLTItMmgtNFYzLjVDMTMgMi4xMiAxMS44OCAxIDEwLjUgMVM4IDIuMTIgOCAzLjVWNUg0Yy0xLjEgMC0xLjk5LjktMS45OSAydjMuOEgzLjVjMS40OSAwIDIuNyAxLjIxIDIuNyAyLjdzLTEuMjEgMi43LTIuNyAyLjdIMlYyMGMwIDEuMS45IDIgMiAyaDMuOHYtMS41YzAtMS40OSAxLjIxLTIuNyAyLjctMi43IDEuNDkgMCAyLjcgMS4yMSAyLjcgMi43VjIySDE3YzEuMSAwIDItLjkgMi0ydi00aDEuNWMxLjM4IDAgMi41LTEuMTIgMi41LTIuNVMyMS44OCAxMSAyMC41IDExeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-fast-forward: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTQgMThsOC41LTZMNCA2djEyem05LTEydjEybDguNS02TDEzIDZ6Ii8+CiAgICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-file-upload: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTkgMTZoNnYtNmg0bC03LTctNyA3aDR6bS00IDJoMTR2Mkg1eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-file: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTkuMyA4LjJsLTUuNS01LjVjLS4zLS4zLS43LS41LTEuMi0uNUgzLjljLS44LjEtMS42LjktMS42IDEuOHYxNC4xYzAgLjkuNyAxLjYgMS42IDEuNmgxNC4yYy45IDAgMS42LS43IDEuNi0xLjZWOS40Yy4xLS41LS4xLS45LS40LTEuMnptLTUuOC0zLjNsMy40IDMuNmgtMy40VjQuOXptMy45IDEyLjdINC43Yy0uMSAwLS4yIDAtLjItLjJWNC43YzAtLjIuMS0uMy4yLS4zaDcuMnY0LjRzMCAuOC4zIDEuMWMuMy4zIDEuMS4zIDEuMS4zaDQuM3Y3LjJzLS4xLjItLjIuMnoiLz4KPC9zdmc+Cg==);
  --jp-icon-filter-list: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEwIDE4aDR2LTJoLTR2MnpNMyA2djJoMThWNkgzem0zIDdoMTJ2LTJINnYyeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-folder: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTAgNEg0Yy0xLjEgMC0xLjk5LjktMS45OSAyTDIgMThjMCAxLjEuOSAyIDIgMmgxNmMxLjEgMCAyLS45IDItMlY4YzAtMS4xLS45LTItMi0yaC04bC0yLTJ6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-html5: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDUxMiA1MTIiPgogIDxwYXRoIGNsYXNzPSJqcC1pY29uMCBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiMwMDAiIGQ9Ik0xMDguNCAwaDIzdjIyLjhoMjEuMlYwaDIzdjY5aC0yM1Y0NmgtMjF2MjNoLTIzLjJNMjA2IDIzaC0yMC4zVjBoNjMuN3YyM0gyMjl2NDZoLTIzbTUzLjUtNjloMjQuMWwxNC44IDI0LjNMMzEzLjIgMGgyNC4xdjY5aC0yM1YzNC44bC0xNi4xIDI0LjgtMTYuMS0yNC44VjY5aC0yMi42bTg5LjItNjloMjN2NDYuMmgzMi42VjY5aC01NS42Ii8+CiAgPHBhdGggY2xhc3M9ImpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iI2U0NGQyNiIgZD0iTTEwNy42IDQ3MWwtMzMtMzcwLjRoMzYyLjhsLTMzIDM3MC4yTDI1NS43IDUxMiIvPgogIDxwYXRoIGNsYXNzPSJqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiNmMTY1MjkiIGQ9Ik0yNTYgNDgwLjVWMTMxaDE0OC4zTDM3NiA0NDciLz4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1zZWxlY3RhYmxlLWludmVyc2UiIGZpbGw9IiNlYmViZWIiIGQ9Ik0xNDIgMTc2LjNoMTE0djQ1LjRoLTY0LjJsNC4yIDQ2LjVoNjB2NDUuM0gxNTQuNG0yIDIyLjhIMjAybDMuMiAzNi4zIDUwLjggMTMuNnY0Ny40bC05My4yLTI2Ii8+CiAgPHBhdGggY2xhc3M9ImpwLWljb24tc2VsZWN0YWJsZS1pbnZlcnNlIiBmaWxsPSIjZmZmIiBkPSJNMzY5LjYgMTc2LjNIMjU1Ljh2NDUuNGgxMDkuNm0tNC4xIDQ2LjVIMjU1Ljh2NDUuNGg1NmwtNS4zIDU5LTUwLjcgMTMuNnY0Ny4ybDkzLTI1LjgiLz4KPC9zdmc+Cg==);
  --jp-icon-image: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1icmFuZDQganAtaWNvbi1zZWxlY3RhYmxlLWludmVyc2UiIGZpbGw9IiNGRkYiIGQ9Ik0yLjIgMi4yaDE3LjV2MTcuNUgyLjJ6Ii8+CiAgPHBhdGggY2xhc3M9ImpwLWljb24tYnJhbmQwIGpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iIzNGNTFCNSIgZD0iTTIuMiAyLjJ2MTcuNWgxNy41bC4xLTE3LjVIMi4yem0xMi4xIDIuMmMxLjIgMCAyLjIgMSAyLjIgMi4ycy0xIDIuMi0yLjIgMi4yLTIuMi0xLTIuMi0yLjIgMS0yLjIgMi4yLTIuMnpNNC40IDE3LjZsMy4zLTguOCAzLjMgNi42IDIuMi0zLjIgNC40IDUuNEg0LjR6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-inspector: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMjAgNEg0Yy0xLjEgMC0xLjk5LjktMS45OSAyTDIgMThjMCAxLjEuOSAyIDIgMmgxNmMxLjEgMCAyLS45IDItMlY2YzAtMS4xLS45LTItMi0yem0tNSAxNEg0di00aDExdjR6bTAtNUg0VjloMTF2NHptNSA1aC00VjloNHY5eiIvPgo8L3N2Zz4K);
  --jp-icon-json: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtaWNvbi13YXJuMSBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiNGOUE4MjUiPgogICAgPHBhdGggZD0iTTIwLjIgMTEuOGMtMS42IDAtMS43LjUtMS43IDEgMCAuNC4xLjkuMSAxLjMuMS41LjEuOS4xIDEuMyAwIDEuNy0xLjQgMi4zLTMuNSAyLjNoLS45di0xLjloLjVjMS4xIDAgMS40IDAgMS40LS44IDAtLjMgMC0uNi0uMS0xIDAtLjQtLjEtLjgtLjEtMS4yIDAtMS4zIDAtMS44IDEuMy0yLTEuMy0uMi0xLjMtLjctMS4zLTIgMC0uNC4xLS44LjEtMS4yLjEtLjQuMS0uNy4xLTEgMC0uOC0uNC0uNy0xLjQtLjhoLS41VjQuMWguOWMyLjIgMCAzLjUuNyAzLjUgMi4zIDAgLjQtLjEuOS0uMSAxLjMtLjEuNS0uMS45LS4xIDEuMyAwIC41LjIgMSAxLjcgMXYxLjh6TTEuOCAxMC4xYzEuNiAwIDEuNy0uNSAxLjctMSAwLS40LS4xLS45LS4xLTEuMy0uMS0uNS0uMS0uOS0uMS0xLjMgMC0xLjYgMS40LTIuMyAzLjUtMi4zaC45djEuOWgtLjVjLTEgMC0xLjQgMC0xLjQuOCAwIC4zIDAgLjYuMSAxIDAgLjIuMS42LjEgMSAwIDEuMyAwIDEuOC0xLjMgMkM2IDExLjIgNiAxMS43IDYgMTNjMCAuNC0uMS44LS4xIDEuMi0uMS4zLS4xLjctLjEgMSAwIC44LjMuOCAxLjQuOGguNXYxLjloLS45Yy0yLjEgMC0zLjUtLjYtMy41LTIuMyAwLS40LjEtLjkuMS0xLjMuMS0uNS4xLS45LjEtMS4zIDAtLjUtLjItMS0xLjctMXYtMS45eiIvPgogICAgPGNpcmNsZSBjeD0iMTEiIGN5PSIxMy44IiByPSIyLjEiLz4KICAgIDxjaXJjbGUgY3g9IjExIiBjeT0iOC4yIiByPSIyLjEiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-jupyter-favicon: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTUyIiBoZWlnaHQ9IjE2NSIgdmlld0JveD0iMCAwIDE1MiAxNjUiIHZlcnNpb249IjEuMSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbi13YXJuMCIgZmlsbD0iI0YzNzcyNiI+CiAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgwLjA3ODk0NywgMTEwLjU4MjkyNykiIGQ9Ik03NS45NDIyODQyLDI5LjU4MDQ1NjEgQzQzLjMwMjM5NDcsMjkuNTgwNDU2MSAxNC43OTY3ODMyLDE3LjY1MzQ2MzQgMCwwIEM1LjUxMDgzMjExLDE1Ljg0MDY4MjkgMTUuNzgxNTM4OSwyOS41NjY3NzMyIDI5LjM5MDQ5NDcsMzkuMjc4NDE3MSBDNDIuOTk5Nyw0OC45ODk4NTM3IDU5LjI3MzcsNTQuMjA2NzgwNSA3NS45NjA1Nzg5LDU0LjIwNjc4MDUgQzkyLjY0NzQ1NzksNTQuMjA2NzgwNSAxMDguOTIxNDU4LDQ4Ljk4OTg1MzcgMTIyLjUzMDY2MywzOS4yNzg0MTcxIEMxMzYuMTM5NDUzLDI5LjU2Njc3MzIgMTQ2LjQxMDI4NCwxNS44NDA2ODI5IDE1MS45MjExNTgsMCBDMTM3LjA4Nzg2OCwxNy42NTM0NjM0IDEwOC41ODI1ODksMjkuNTgwNDU2MSA3NS45NDIyODQyLDI5LjU4MDQ1NjEgTDc1Ljk0MjI4NDIsMjkuNTgwNDU2MSBaIiAvPgogICAgPHBhdGggdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMC4wMzczNjgsIDAuNzA0ODc4KSIgZD0iTTc1Ljk3ODQ1NzksMjQuNjI2NDA3MyBDMTA4LjYxODc2MywyNC42MjY0MDczIDEzNy4xMjQ0NTgsMzYuNTUzNDQxNSAxNTEuOTIxMTU4LDU0LjIwNjc4MDUgQzE0Ni40MTAyODQsMzguMzY2MjIyIDEzNi4xMzk0NTMsMjQuNjQwMTMxNyAxMjIuNTMwNjYzLDE0LjkyODQ4NzggQzEwOC45MjE0NTgsNS4yMTY4NDM5IDkyLjY0NzQ1NzksMCA3NS45NjA1Nzg5LDAgQzU5LjI3MzcsMCA0Mi45OTk3LDUuMjE2ODQzOSAyOS4zOTA0OTQ3LDE0LjkyODQ4NzggQzE1Ljc4MTUzODksMjQuNjQwMTMxNyA1LjUxMDgzMjExLDM4LjM2NjIyMiAwLDU0LjIwNjc4MDUgQzE0LjgzMzA4MTYsMzYuNTg5OTI5MyA0My4zMzg1Njg0LDI0LjYyNjQwNzMgNzUuOTc4NDU3OSwyNC42MjY0MDczIEw3NS45Nzg0NTc5LDI0LjYyNjQwNzMgWiIgLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-jupyter: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMzkiIGhlaWdodD0iNTEiIHZpZXdCb3g9IjAgMCAzOSA1MSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgtMTYzOCAtMjI4MSkiPgogICAgPGcgY2xhc3M9ImpwLWljb24td2FybjAiIGZpbGw9IiNGMzc3MjYiPgogICAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxNjM5Ljc0IDIzMTEuOTgpIiBkPSJNIDE4LjI2NDYgNy4xMzQxMUMgMTAuNDE0NSA3LjEzNDExIDMuNTU4NzIgNC4yNTc2IDAgMEMgMS4zMjUzOSAzLjgyMDQgMy43OTU1NiA3LjEzMDgxIDcuMDY4NiA5LjQ3MzAzQyAxMC4zNDE3IDExLjgxNTIgMTQuMjU1NyAxMy4wNzM0IDE4LjI2OSAxMy4wNzM0QyAyMi4yODIzIDEzLjA3MzQgMjYuMTk2MyAxMS44MTUyIDI5LjQ2OTQgOS40NzMwM0MgMzIuNzQyNCA3LjEzMDgxIDM1LjIxMjYgMy44MjA0IDM2LjUzOCAwQyAzMi45NzA1IDQuMjU3NiAyNi4xMTQ4IDcuMTM0MTEgMTguMjY0NiA3LjEzNDExWiIvPgogICAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxNjM5LjczIDIyODUuNDgpIiBkPSJNIDE4LjI3MzMgNS45MzkzMUMgMjYuMTIzNSA1LjkzOTMxIDMyLjk3OTMgOC44MTU4MyAzNi41MzggMTMuMDczNEMgMzUuMjEyNiA5LjI1MzAzIDMyLjc0MjQgNS45NDI2MiAyOS40Njk0IDMuNjAwNEMgMjYuMTk2MyAxLjI1ODE4IDIyLjI4MjMgMCAxOC4yNjkgMEMgMTQuMjU1NyAwIDEwLjM0MTcgMS4yNTgxOCA3LjA2ODYgMy42MDA0QyAzLjc5NTU2IDUuOTQyNjIgMS4zMjUzOSA5LjI1MzAzIDAgMTMuMDczNEMgMy41Njc0NSA4LjgyNDYzIDEwLjQyMzIgNS45MzkzMSAxOC4yNzMzIDUuOTM5MzFaIi8+CiAgICA8L2c+CiAgICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxNjY5LjMgMjI4MS4zMSkiIGQ9Ik0gNS44OTM1MyAyLjg0NEMgNS45MTg4OSAzLjQzMTY1IDUuNzcwODUgNC4wMTM2NyA1LjQ2ODE1IDQuNTE2NDVDIDUuMTY1NDUgNS4wMTkyMiA0LjcyMTY4IDUuNDIwMTUgNC4xOTI5OSA1LjY2ODUxQyAzLjY2NDMgNS45MTY4OCAzLjA3NDQ0IDYuMDAxNTEgMi40OTgwNSA1LjkxMTcxQyAxLjkyMTY2IDUuODIxOSAxLjM4NDYzIDUuNTYxNyAwLjk1NDg5OCA1LjE2NDAxQyAwLjUyNTE3IDQuNzY2MzMgMC4yMjIwNTYgNC4yNDkwMyAwLjA4MzkwMzcgMy42Nzc1N0MgLTAuMDU0MjQ4MyAzLjEwNjExIC0wLjAyMTIzIDIuNTA2MTcgMC4xNzg3ODEgMS45NTM2NEMgMC4zNzg3OTMgMS40MDExIDAuNzM2ODA5IDAuOTIwODE3IDEuMjA3NTQgMC41NzM1MzhDIDEuNjc4MjYgMC4yMjYyNTkgMi4yNDA1NSAwLjAyNzU5MTkgMi44MjMyNiAwLjAwMjY3MjI5QyAzLjYwMzg5IC0wLjAzMDcxMTUgNC4zNjU3MyAwLjI0OTc4OSA0Ljk0MTQyIDAuNzgyNTUxQyA1LjUxNzExIDEuMzE1MzEgNS44NTk1NiAyLjA1Njc2IDUuODkzNTMgMi44NDRaIi8+CiAgICAgIDxwYXRoIHRyYW5zZm9ybT0idHJhbnNsYXRlKDE2MzkuOCAyMzIzLjgxKSIgZD0iTSA3LjQyNzg5IDMuNTgzMzhDIDcuNDYwMDggNC4zMjQzIDcuMjczNTUgNS4wNTgxOSA2Ljg5MTkzIDUuNjkyMTNDIDYuNTEwMzEgNi4zMjYwNyA1Ljk1MDc1IDYuODMxNTYgNS4yODQxMSA3LjE0NDZDIDQuNjE3NDcgNy40NTc2MyAzLjg3MzcxIDcuNTY0MTQgMy4xNDcwMiA3LjQ1MDYzQyAyLjQyMDMyIDcuMzM3MTIgMS43NDMzNiA3LjAwODcgMS4yMDE4NCA2LjUwNjk1QyAwLjY2MDMyOCA2LjAwNTIgMC4yNzg2MSA1LjM1MjY4IDAuMTA1MDE3IDQuNjMyMDJDIC0wLjA2ODU3NTcgMy45MTEzNSAtMC4wMjYyMzYxIDMuMTU0OTQgMC4yMjY2NzUgMi40NTg1NkMgMC40Nzk1ODcgMS43NjIxNyAwLjkzMTY5NyAxLjE1NzEzIDEuNTI1NzYgMC43MjAwMzNDIDIuMTE5ODMgMC4yODI5MzUgMi44MjkxNCAwLjAzMzQzOTUgMy41NjM4OSAwLjAwMzEzMzQ0QyA0LjU0NjY3IC0wLjAzNzQwMzMgNS41MDUyOSAwLjMxNjcwNiA2LjIyOTYxIDAuOTg3ODM1QyA2Ljk1MzkzIDEuNjU4OTYgNy4zODQ4NCAyLjU5MjM1IDcuNDI3ODkgMy41ODMzOEwgNy40Mjc4OSAzLjU4MzM4WiIvPgogICAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxNjM4LjM2IDIyODYuMDYpIiBkPSJNIDIuMjc0NzEgNC4zOTYyOUMgMS44NDM2MyA0LjQxNTA4IDEuNDE2NzEgNC4zMDQ0NSAxLjA0Nzk5IDQuMDc4NDNDIDAuNjc5MjY4IDMuODUyNCAwLjM4NTMyOCAzLjUyMTE0IDAuMjAzMzcxIDMuMTI2NTZDIDAuMDIxNDEzNiAyLjczMTk4IC0wLjA0MDM3OTggMi4yOTE4MyAwLjAyNTgxMTYgMS44NjE4MUMgMC4wOTIwMDMxIDEuNDMxOCAwLjI4MzIwNCAxLjAzMTI2IDAuNTc1MjEzIDAuNzEwODgzQyAwLjg2NzIyMiAwLjM5MDUxIDEuMjQ2OTEgMC4xNjQ3MDggMS42NjYyMiAwLjA2MjA1OTJDIDIuMDg1NTMgLTAuMDQwNTg5NyAyLjUyNTYxIC0wLjAxNTQ3MTQgMi45MzA3NiAwLjEzNDIzNUMgMy4zMzU5MSAwLjI4Mzk0MSAzLjY4NzkyIDAuNTUxNTA1IDMuOTQyMjIgMC45MDMwNkMgNC4xOTY1MiAxLjI1NDYyIDQuMzQxNjkgMS42NzQzNiA0LjM1OTM1IDIuMTA5MTZDIDQuMzgyOTkgMi42OTEwNyA0LjE3Njc4IDMuMjU4NjkgMy43ODU5NyAzLjY4NzQ2QyAzLjM5NTE2IDQuMTE2MjQgMi44NTE2NiA0LjM3MTE2IDIuMjc0NzEgNC4zOTYyOUwgMi4yNzQ3MSA0LjM5NjI5WiIvPgogICAgPC9nPgogIDwvZz4+Cjwvc3ZnPgo=);
  --jp-icon-jupyterlab-wordmark: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyMDAiIHZpZXdCb3g9IjAgMCAxODYwLjggNDc1Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjIiIGZpbGw9IiM0RTRFNEUiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDQ4MC4xMzY0MDEsIDY0LjI3MTQ5MykiPgogICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMC4wMDAwMDAsIDU4Ljg3NTU2NikiPgogICAgICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgwLjA4NzYwMywgMC4xNDAyOTQpIj4KICAgICAgICA8cGF0aCBkPSJNLTQyNi45LDE2OS44YzAsNDguNy0zLjcsNjQuNy0xMy42LDc2LjRjLTEwLjgsMTAtMjUsMTUuNS0zOS43LDE1LjVsMy43LDI5IGMyMi44LDAuMyw0NC44LTcuOSw2MS45LTIzLjFjMTcuOC0xOC41LDI0LTQ0LjEsMjQtODMuM1YwSC00Mjd2MTcwLjFMLTQyNi45LDE2OS44TC00MjYuOSwxNjkuOHoiLz4KICAgICAgPC9nPgogICAgPC9nPgogICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMTU1LjA0NTI5NiwgNTYuODM3MTA0KSI+CiAgICAgIDxnIHRyYW5zZm9ybT0idHJhbnNsYXRlKDEuNTYyNDUzLCAxLjc5OTg0MikiPgogICAgICAgIDxwYXRoIGQ9Ik0tMzEyLDE0OGMwLDIxLDAsMzkuNSwxLjcsNTUuNGgtMzEuOGwtMi4xLTMzLjNoLTAuOGMtNi43LDExLjYtMTYuNCwyMS4zLTI4LDI3LjkgYy0xMS42LDYuNi0yNC44LDEwLTM4LjIsOS44Yy0zMS40LDAtNjktMTcuNy02OS04OVYwaDM2LjR2MTEyLjdjMCwzOC43LDExLjYsNjQuNyw0NC42LDY0LjdjMTAuMy0wLjIsMjAuNC0zLjUsMjguOS05LjQgYzguNS01LjksMTUuMS0xNC4zLDE4LjktMjMuOWMyLjItNi4xLDMuMy0xMi41LDMuMy0xOC45VjAuMmgzNi40VjE0OEgtMzEyTC0zMTIsMTQ4eiIvPgogICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgzOTAuMDEzMzIyLCA1My40Nzk2MzgpIj4KICAgICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMS43MDY0NTgsIDAuMjMxNDI1KSI+CiAgICAgICAgPHBhdGggZD0iTS00NzguNiw3MS40YzAtMjYtMC44LTQ3LTEuNy02Ni43aDMyLjdsMS43LDM0LjhoMC44YzcuMS0xMi41LDE3LjUtMjIuOCwzMC4xLTI5LjcgYzEyLjUtNywyNi43LTEwLjMsNDEtOS44YzQ4LjMsMCw4NC43LDQxLjcsODQuNywxMDMuM2MwLDczLjEtNDMuNywxMDkuMi05MSwxMDkuMmMtMTIuMSwwLjUtMjQuMi0yLjItMzUtNy44IGMtMTAuOC01LjYtMTkuOS0xMy45LTI2LjYtMjQuMmgtMC44VjI5MWgtMzZ2LTIyMEwtNDc4LjYsNzEuNEwtNDc4LjYsNzEuNHogTS00NDIuNiwxMjUuNmMwLjEsNS4xLDAuNiwxMC4xLDEuNywxNS4xIGMzLDEyLjMsOS45LDIzLjMsMTkuOCwzMS4xYzkuOSw3LjgsMjIuMSwxMi4xLDM0LjcsMTIuMWMzOC41LDAsNjAuNy0zMS45LDYwLjctNzguNWMwLTQwLjctMjEuMS03NS42LTU5LjUtNzUuNiBjLTEyLjksMC40LTI1LjMsNS4xLTM1LjMsMTMuNGMtOS45LDguMy0xNi45LDE5LjctMTkuNiwzMi40Yy0xLjUsNC45LTIuMywxMC0yLjUsMTUuMVYxMjUuNkwtNDQyLjYsMTI1LjZMLTQ0Mi42LDEyNS42eiIvPgogICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSg2MDYuNzQwNzI2LCA1Ni44MzcxMDQpIj4KICAgICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMC43NTEyMjYsIDEuOTg5Mjk5KSI+CiAgICAgICAgPHBhdGggZD0iTS00NDAuOCwwbDQzLjcsMTIwLjFjNC41LDEzLjQsOS41LDI5LjQsMTIuOCw0MS43aDAuOGMzLjctMTIuMiw3LjktMjcuNywxMi44LTQyLjQgbDM5LjctMTE5LjJoMzguNUwtMzQ2LjksMTQ1Yy0yNiw2OS43LTQzLjcsMTA1LjQtNjguNiwxMjcuMmMtMTIuNSwxMS43LTI3LjksMjAtNDQuNiwyMy45bC05LjEtMzEuMSBjMTEuNy0zLjksMjIuNS0xMC4xLDMxLjgtMTguMWMxMy4yLTExLjEsMjMuNy0yNS4yLDMwLjYtNDEuMmMxLjUtMi44LDIuNS01LjcsMi45LTguOGMtMC4zLTMuMy0xLjItNi42LTIuNS05LjdMLTQ4MC4yLDAuMSBoMzkuN0wtNDQwLjgsMEwtNDQwLjgsMHoiLz4KICAgICAgPC9nPgogICAgPC9nPgogICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoODIyLjc0ODEwNCwgMC4wMDAwMDApIj4KICAgICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMS40NjQwNTAsIDAuMzc4OTE0KSI+CiAgICAgICAgPHBhdGggZD0iTS00MTMuNywwdjU4LjNoNTJ2MjguMmgtNTJWMTk2YzAsMjUsNywzOS41LDI3LjMsMzkuNWM3LjEsMC4xLDE0LjItMC43LDIxLjEtMi41IGwxLjcsMjcuN2MtMTAuMywzLjctMjEuMyw1LjQtMzIuMiw1Yy03LjMsMC40LTE0LjYtMC43LTIxLjMtMy40Yy02LjgtMi43LTEyLjktNi44LTE3LjktMTIuMWMtMTAuMy0xMC45LTE0LjEtMjktMTQuMS01Mi45IFY4Ni41aC0zMVY1OC4zaDMxVjkuNkwtNDEzLjcsMEwtNDEzLjcsMHoiLz4KICAgICAgPC9nPgogICAgPC9nPgogICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoOTc0LjQzMzI4NiwgNTMuNDc5NjM4KSI+CiAgICAgIDxnIHRyYW5zZm9ybT0idHJhbnNsYXRlKDAuOTkwMDM0LCAwLjYxMDMzOSkiPgogICAgICAgIDxwYXRoIGQ9Ik0tNDQ1LjgsMTEzYzAuOCw1MCwzMi4yLDcwLjYsNjguNiw3MC42YzE5LDAuNiwzNy45LTMsNTUuMy0xMC41bDYuMiwyNi40IGMtMjAuOSw4LjktNDMuNSwxMy4xLTY2LjIsMTIuNmMtNjEuNSwwLTk4LjMtNDEuMi05OC4zLTEwMi41Qy00ODAuMiw0OC4yLTQ0NC43LDAtMzg2LjUsMGM2NS4yLDAsODIuNyw1OC4zLDgyLjcsOTUuNyBjLTAuMSw1LjgtMC41LDExLjUtMS4yLDE3LjJoLTE0MC42SC00NDUuOEwtNDQ1LjgsMTEzeiBNLTMzOS4yLDg2LjZjMC40LTIzLjUtOS41LTYwLjEtNTAuNC02MC4xIGMtMzYuOCwwLTUyLjgsMzQuNC01NS43LDYwLjFILTMzOS4yTC0zMzkuMiw4Ni42TC0zMzkuMiw4Ni42eiIvPgogICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxMjAxLjk2MTA1OCwgNTMuNDc5NjM4KSI+CiAgICAgIDxnIHRyYW5zZm9ybT0idHJhbnNsYXRlKDEuMTc5NjQwLCAwLjcwNTA2OCkiPgogICAgICAgIDxwYXRoIGQ9Ik0tNDc4LjYsNjhjMC0yMy45LTAuNC00NC41LTEuNy02My40aDMxLjhsMS4yLDM5LjloMS43YzkuMS0yNy4zLDMxLTQ0LjUsNTUuMy00NC41IGMzLjUtMC4xLDcsMC40LDEwLjMsMS4ydjM0LjhjLTQuMS0wLjktOC4yLTEuMy0xMi40LTEuMmMtMjUuNiwwLTQzLjcsMTkuNy00OC43LDQ3LjRjLTEsNS43LTEuNiwxMS41LTEuNywxNy4ydjEwOC4zaC0zNlY2OCBMLTQ3OC42LDY4eiIvPgogICAgICA8L2c+CiAgICA8L2c+CiAgPC9nPgoKICA8ZyBjbGFzcz0ianAtaWNvbi13YXJuMCIgZmlsbD0iI0YzNzcyNiI+CiAgICA8cGF0aCBkPSJNMTM1Mi4zLDMyNi4yaDM3VjI4aC0zN1YzMjYuMnogTTE2MDQuOCwzMjYuMmMtMi41LTEzLjktMy40LTMxLjEtMy40LTQ4Ljd2LTc2IGMwLTQwLjctMTUuMS04My4xLTc3LjMtODMuMWMtMjUuNiwwLTUwLDcuMS02Ni44LDE4LjFsOC40LDI0LjRjMTQuMy05LjIsMzQtMTUuMSw1My0xNS4xYzQxLjYsMCw0Ni4yLDMwLjIsNDYuMiw0N3Y0LjIgYy03OC42LTAuNC0xMjIuMywyNi41LTEyMi4zLDc1LjZjMCwyOS40LDIxLDU4LjQsNjIuMiw1OC40YzI5LDAsNTAuOS0xNC4zLDYyLjItMzAuMmgxLjNsMi45LDI1LjZIMTYwNC44eiBNMTU2NS43LDI1Ny43IGMwLDMuOC0wLjgsOC0yLjEsMTEuOGMtNS45LDE3LjItMjIuNywzNC00OS4yLDM0Yy0xOC45LDAtMzQuOS0xMS4zLTM0LjktMzUuM2MwLTM5LjUsNDUuOC00Ni42LDg2LjItNDUuOFYyNTcuN3ogTTE2OTguNSwzMjYuMiBsMS43LTMzLjZoMS4zYzE1LjEsMjYuOSwzOC43LDM4LjIsNjguMSwzOC4yYzQ1LjQsMCw5MS4yLTM2LjEsOTEuMi0xMDguOGMwLjQtNjEuNy0zNS4zLTEwMy43LTg1LjctMTAzLjcgYy0zMi44LDAtNTYuMywxNC43LTY5LjMsMzcuNGgtMC44VjI4aC0zNi42djI0NS43YzAsMTguMS0wLjgsMzguNi0xLjcsNTIuNUgxNjk4LjV6IE0xNzA0LjgsMjA4LjJjMC01LjksMS4zLTEwLjksMi4xLTE1LjEgYzcuNi0yOC4xLDMxLjEtNDUuNCw1Ni4zLTQ1LjRjMzkuNSwwLDYwLjUsMzQuOSw2MC41LDc1LjZjMCw0Ni42LTIzLjEsNzguMS02MS44LDc4LjFjLTI2LjksMC00OC4zLTE3LjYtNTUuNS00My4zIGMtMC44LTQuMi0xLjctOC44LTEuNy0xMy40VjIwOC4yeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-kernel: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiIgZmlsbD0iIzYxNjE2MSIgZD0iTTE1IDlIOXY2aDZWOXptLTIgNGgtMnYtMmgydjJ6bTgtMlY5aC0yVjdjMC0xLjEtLjktMi0yLTJoLTJWM2gtMnYyaC0yVjNIOXYySDdjLTEuMSAwLTIgLjktMiAydjJIM3YyaDJ2MkgzdjJoMnYyYzAgMS4xLjkgMiAyIDJoMnYyaDJ2LTJoMnYyaDJ2LTJoMmMxLjEgMCAyLS45IDItMnYtMmgydi0yaC0ydi0yaDJ6bS00IDZIN1Y3aDEwdjEweiIvPgo8L3N2Zz4K);
  --jp-icon-keyboard: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMjAgNUg0Yy0xLjEgMC0xLjk5LjktMS45OSAyTDIgMTdjMCAxLjEuOSAyIDIgMmgxNmMxLjEgMCAyLS45IDItMlY3YzAtMS4xLS45LTItMi0yem0tOSAzaDJ2MmgtMlY4em0wIDNoMnYyaC0ydi0yek04IDhoMnYySDhWOHptMCAzaDJ2Mkg4di0yem0tMSAySDV2LTJoMnYyem0wLTNINVY4aDJ2MnptOSA3SDh2LTJoOHYyem0wLTRoLTJ2LTJoMnYyem0wLTNoLTJWOGgydjJ6bTMgM2gtMnYtMmgydjJ6bTAtM2gtMlY4aDJ2MnoiLz4KPC9zdmc+Cg==);
  --jp-icon-launcher: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTkgMTlINVY1aDdWM0g1YTIgMiAwIDAwLTIgMnYxNGEyIDIgMCAwMDIgMmgxNGMxLjEgMCAyLS45IDItMnYtN2gtMnY3ek0xNCAzdjJoMy41OWwtOS44MyA5LjgzIDEuNDEgMS40MUwxOSA2LjQxVjEwaDJWM2gtN3oiLz4KPC9zdmc+Cg==);
  --jp-icon-line-form: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICAgIDxwYXRoIGZpbGw9IndoaXRlIiBkPSJNNS44OCA0LjEyTDEzLjc2IDEybC03Ljg4IDcuODhMOCAyMmwxMC0xMEw4IDJ6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-link: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTMuOSAxMmMwLTEuNzEgMS4zOS0zLjEgMy4xLTMuMWg0VjdIN2MtMi43NiAwLTUgMi4yNC01IDVzMi4yNCA1IDUgNWg0di0xLjlIN2MtMS43MSAwLTMuMS0xLjM5LTMuMS0zLjF6TTggMTNoOHYtMkg4djJ6bTktNmgtNHYxLjloNGMxLjcxIDAgMy4xIDEuMzkgMy4xIDMuMXMtMS4zOSAzLjEtMy4xIDMuMWgtNFYxN2g0YzIuNzYgMCA1LTIuMjQgNS01cy0yLjI0LTUtNS01eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-list: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiM2MTYxNjEiIGQ9Ik0xOSA1djE0SDVWNWgxNG0xLjEtMkgzLjljLS41IDAtLjkuNC0uOS45djE2LjJjMCAuNC40LjkuOS45aDE2LjJjLjQgMCAuOS0uNS45LS45VjMuOWMwLS41LS41LS45LS45LS45ek0xMSA3aDZ2MmgtNlY3em0wIDRoNnYyaC02di0yem0wIDRoNnYyaC02ek03IDdoMnYySDd6bTAgNGgydjJIN3ptMCA0aDJ2Mkg3eiIvPgo8L3N2Zz4=);
  --jp-icon-listings-info: url(data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iaXNvLTg4NTktMSI/Pg0KPHN2ZyB2ZXJzaW9uPSIxLjEiIGlkPSJDYXBhXzEiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyIgeG1sbnM6eGxpbms9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkveGxpbmsiIHg9IjBweCIgeT0iMHB4Ig0KCSB2aWV3Qm94PSIwIDAgNTAuOTc4IDUwLjk3OCIgc3R5bGU9ImVuYWJsZS1iYWNrZ3JvdW5kOm5ldyAwIDAgNTAuOTc4IDUwLjk3ODsiIHhtbDpzcGFjZT0icHJlc2VydmUiPg0KPGc+DQoJPGc+DQoJCTxnPg0KCQkJPHBhdGggc3R5bGU9ImZpbGw6IzAxMDAwMjsiIGQ9Ik00My41Miw3LjQ1OEMzOC43MTEsMi42NDgsMzIuMzA3LDAsMjUuNDg5LDBDMTguNjcsMCwxMi4yNjYsMi42NDgsNy40NTgsNy40NTgNCgkJCQljLTkuOTQzLDkuOTQxLTkuOTQzLDI2LjExOSwwLDM2LjA2MmM0LjgwOSw0LjgwOSwxMS4yMTIsNy40NTYsMTguMDMxLDcuNDU4YzAsMCwwLjAwMSwwLDAuMDAyLDANCgkJCQljNi44MTYsMCwxMy4yMjEtMi42NDgsMTguMDI5LTcuNDU4YzQuODA5LTQuODA5LDcuNDU3LTExLjIxMiw3LjQ1Ny0xOC4wM0M1MC45NzcsMTguNjcsNDguMzI4LDEyLjI2Niw0My41Miw3LjQ1OHoNCgkJCQkgTTQyLjEwNiw0Mi4xMDVjLTQuNDMyLDQuNDMxLTEwLjMzMiw2Ljg3Mi0xNi42MTUsNi44NzJoLTAuMDAyYy02LjI4NS0wLjAwMS0xMi4xODctMi40NDEtMTYuNjE3LTYuODcyDQoJCQkJYy05LjE2Mi05LjE2My05LjE2Mi0yNC4wNzEsMC0zMy4yMzNDMTMuMzAzLDQuNDQsMTkuMjA0LDIsMjUuNDg5LDJjNi4yODQsMCwxMi4xODYsMi40NCwxNi42MTcsNi44NzINCgkJCQljNC40MzEsNC40MzEsNi44NzEsMTAuMzMyLDYuODcxLDE2LjYxN0M0OC45NzcsMzEuNzcyLDQ2LjUzNiwzNy42NzUsNDIuMTA2LDQyLjEwNXoiLz4NCgkJPC9nPg0KCQk8Zz4NCgkJCTxwYXRoIHN0eWxlPSJmaWxsOiMwMTAwMDI7IiBkPSJNMjMuNTc4LDMyLjIxOGMtMC4wMjMtMS43MzQsMC4xNDMtMy4wNTksMC40OTYtMy45NzJjMC4zNTMtMC45MTMsMS4xMS0xLjk5NywyLjI3Mi0zLjI1Mw0KCQkJCWMwLjQ2OC0wLjUzNiwwLjkyMy0xLjA2MiwxLjM2Ny0xLjU3NWMwLjYyNi0wLjc1MywxLjEwNC0xLjQ3OCwxLjQzNi0yLjE3NWMwLjMzMS0wLjcwNywwLjQ5NS0xLjU0MSwwLjQ5NS0yLjUNCgkJCQljMC0xLjA5Ni0wLjI2LTIuMDg4LTAuNzc5LTIuOTc5Yy0wLjU2NS0wLjg3OS0xLjUwMS0xLjMzNi0yLjgwNi0xLjM2OWMtMS44MDIsMC4wNTctMi45ODUsMC42NjctMy41NSwxLjgzMg0KCQkJCWMtMC4zMDEsMC41MzUtMC41MDMsMS4xNDEtMC42MDcsMS44MTRjLTAuMTM5LDAuNzA3LTAuMjA3LDEuNDMyLTAuMjA3LDIuMTc0aC0yLjkzN2MtMC4wOTEtMi4yMDgsMC40MDctNC4xMTQsMS40OTMtNS43MTkNCgkJCQljMS4wNjItMS42NCwyLjg1NS0yLjQ4MSw1LjM3OC0yLjUyN2MyLjE2LDAuMDIzLDMuODc0LDAuNjA4LDUuMTQxLDEuNzU4YzEuMjc4LDEuMTYsMS45MjksMi43NjQsMS45NSw0LjgxMQ0KCQkJCWMwLDEuMTQyLTAuMTM3LDIuMTExLTAuNDEsMi45MTFjLTAuMzA5LDAuODQ1LTAuNzMxLDEuNTkzLTEuMjY4LDIuMjQzYy0wLjQ5MiwwLjY1LTEuMDY4LDEuMzE4LTEuNzMsMi4wMDINCgkJCQljLTAuNjUsMC42OTctMS4zMTMsMS40NzktMS45ODcsMi4zNDZjLTAuMjM5LDAuMzc3LTAuNDI5LDAuNzc3LTAuNTY1LDEuMTk5Yy0wLjE2LDAuOTU5LTAuMjE3LDEuOTUxLTAuMTcxLDIuOTc5DQoJCQkJQzI2LjU4OSwzMi4yMTgsMjMuNTc4LDMyLjIxOCwyMy41NzgsMzIuMjE4eiBNMjMuNTc4LDM4LjIydi0zLjQ4NGgzLjA3NnYzLjQ4NEgyMy41Nzh6Ii8+DQoJCTwvZz4NCgk8L2c+DQo8L2c+DQo8Zz4NCjwvZz4NCjxnPg0KPC9nPg0KPGc+DQo8L2c+DQo8Zz4NCjwvZz4NCjxnPg0KPC9nPg0KPGc+DQo8L2c+DQo8Zz4NCjwvZz4NCjxnPg0KPC9nPg0KPGc+DQo8L2c+DQo8Zz4NCjwvZz4NCjxnPg0KPC9nPg0KPGc+DQo8L2c+DQo8Zz4NCjwvZz4NCjxnPg0KPC9nPg0KPGc+DQo8L2c+DQo8L3N2Zz4NCg==);
  --jp-icon-markdown: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1jb250cmFzdDAganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjN0IxRkEyIiBkPSJNNSAxNC45aDEybC02LjEgNnptOS40LTYuOGMwLTEuMy0uMS0yLjktLjEtNC41LS40IDEuNC0uOSAyLjktMS4zIDQuM2wtMS4zIDQuM2gtMkw4LjUgNy45Yy0uNC0xLjMtLjctMi45LTEtNC4zLS4xIDEuNi0uMSAzLjItLjIgNC42TDcgMTIuNEg0LjhsLjctMTFoMy4zTDEwIDVjLjQgMS4yLjcgMi43IDEgMy45LjMtMS4yLjctMi42IDEtMy45bDEuMi0zLjdoMy4zbC42IDExaC0yLjRsLS4zLTQuMnoiLz4KPC9zdmc+Cg==);
  --jp-icon-new-folder: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTIwIDZoLThsLTItMkg0Yy0xLjExIDAtMS45OS44OS0xLjk5IDJMMiAxOGMwIDEuMTEuODkgMiAyIDJoMTZjMS4xMSAwIDItLjg5IDItMlY4YzAtMS4xMS0uODktMi0yLTJ6bS0xIDhoLTN2M2gtMnYtM2gtM3YtMmgzVjloMnYzaDN2MnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-not-trusted: url(data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI1IDI1Ij4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiIgc3Ryb2tlPSIjMzMzMzMzIiBzdHJva2Utd2lkdGg9IjIiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDMgMykiIGQ9Ik0xLjg2MDk0IDExLjQ0MDlDMC44MjY0NDggOC43NzAyNyAwLjg2Mzc3OSA2LjA1NzY0IDEuMjQ5MDcgNC4xOTkzMkMyLjQ4MjA2IDMuOTMzNDcgNC4wODA2OCAzLjQwMzQ3IDUuNjAxMDIgMi44NDQ5QzcuMjM1NDkgMi4yNDQ0IDguODU2NjYgMS41ODE1IDkuOTg3NiAxLjA5NTM5QzExLjA1OTcgMS41ODM0MSAxMi42MDk0IDIuMjQ0NCAxNC4yMTggMi44NDMzOUMxNS43NTAzIDMuNDEzOTQgMTcuMzk5NSAzLjk1MjU4IDE4Ljc1MzkgNC4yMTM4NUMxOS4xMzY0IDYuMDcxNzcgMTkuMTcwOSA4Ljc3NzIyIDE4LjEzOSAxMS40NDA5QzE3LjAzMDMgMTQuMzAzMiAxNC42NjY4IDE3LjE4NDQgOS45OTk5OSAxOC45MzU0QzUuMzMzMTkgMTcuMTg0NCAyLjk2OTY4IDE0LjMwMzIgMS44NjA5NCAxMS40NDA5WiIvPgogICAgPHBhdGggY2xhc3M9ImpwLWljb24yIiBzdHJva2U9IiMzMzMzMzMiIHN0cm9rZS13aWR0aD0iMiIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoOS4zMTU5MiA5LjMyMDMxKSIgZD0iTTcuMzY4NDIgMEwwIDcuMzY0NzkiLz4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiIgc3Ryb2tlPSIjMzMzMzMzIiBzdHJva2Utd2lkdGg9IjIiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDkuMzE1OTIgMTYuNjgzNikgc2NhbGUoMSAtMSkiIGQ9Ik03LjM2ODQyIDBMMCA3LjM2NDc5Ii8+Cjwvc3ZnPgo=);
  --jp-icon-notebook: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtaWNvbi13YXJuMCBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiNFRjZDMDAiPgogICAgPHBhdGggZD0iTTE4LjcgMy4zdjE1LjRIMy4zVjMuM2gxNS40bTEuNS0xLjVIMS44djE4LjNoMTguM2wuMS0xOC4zeiIvPgogICAgPHBhdGggZD0iTTE2LjUgMTYuNWwtNS40LTQuMy01LjYgNC4zdi0xMWgxMXoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-palette: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTE4IDEzVjIwSDRWNkg5LjAyQzkuMDcgNS4yOSA5LjI0IDQuNjIgOS41IDRINEMyLjkgNCAyIDQuOSAyIDZWMjBDMiAyMS4xIDIuOSAyMiA0IDIySDE4QzE5LjEgMjIgMjAgMjEuMSAyMCAyMFYxNUwxOCAxM1pNMTkuMyA4Ljg5QzE5Ljc0IDguMTkgMjAgNy4zOCAyMCA2LjVDMjAgNC4wMSAxNy45OSAyIDE1LjUgMkMxMy4wMSAyIDExIDQuMDEgMTEgNi41QzExIDguOTkgMTMuMDEgMTEgMTUuNDkgMTFDMTYuMzcgMTEgMTcuMTkgMTAuNzQgMTcuODggMTAuM0wyMSAxMy40MkwyMi40MiAxMkwxOS4zIDguODlaTTE1LjUgOUMxNC4xMiA5IDEzIDcuODggMTMgNi41QzEzIDUuMTIgMTQuMTIgNCAxNS41IDRDMTYuODggNCAxOCA1LjEyIDE4IDYuNUMxOCA3Ljg4IDE2Ljg4IDkgMTUuNSA5WiIvPgogICAgPHBhdGggZmlsbC1ydWxlPSJldmVub2RkIiBjbGlwLXJ1bGU9ImV2ZW5vZGQiIGQ9Ik00IDZIOS4wMTg5NEM5LjAwNjM5IDYuMTY1MDIgOSA2LjMzMTc2IDkgNi41QzkgOC44MTU3NyAxMC4yMTEgMTAuODQ4NyAxMi4wMzQzIDEySDlWMTRIMTZWMTIuOTgxMUMxNi41NzAzIDEyLjkzNzcgMTcuMTIgMTIuODIwNyAxNy42Mzk2IDEyLjYzOTZMMTggMTNWMjBINFY2Wk04IDhINlYxMEg4VjhaTTYgMTJIOFYxNEg2VjEyWk04IDE2SDZWMThIOFYxNlpNOSAxNkgxNlYxOEg5VjE2WiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-paste: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTE5IDJoLTQuMThDMTQuNC44NCAxMy4zIDAgMTIgMGMtMS4zIDAtMi40Ljg0LTIuODIgMkg1Yy0xLjEgMC0yIC45LTIgMnYxNmMwIDEuMS45IDIgMiAyaDE0YzEuMSAwIDItLjkgMi0yVjRjMC0xLjEtLjktMi0yLTJ6bS03IDBjLjU1IDAgMSAuNDUgMSAxcy0uNDUgMS0xIDEtMS0uNDUtMS0xIC40NS0xIDEtMXptNyAxOEg1VjRoMnYzaDEwVjRoMnYxNnoiLz4KICAgIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-python: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtaWNvbi1icmFuZDAganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjMEQ0N0ExIj4KICAgIDxwYXRoIGQ9Ik0xMS4xIDYuOVY1LjhINi45YzAtLjUgMC0xLjMuMi0xLjYuNC0uNy44LTEuMSAxLjctMS40IDEuNy0uMyAyLjUtLjMgMy45LS4xIDEgLjEgMS45LjkgMS45IDEuOXY0LjJjMCAuNS0uOSAxLjYtMiAxLjZIOC44Yy0xLjUgMC0yLjQgMS40LTIuNCAyLjh2Mi4ySDQuN0MzLjUgMTUuMSAzIDE0IDMgMTMuMVY5Yy0uMS0xIC42LTIgMS44LTIgMS41LS4xIDYuMy0uMSA2LjMtLjF6Ii8+CiAgICA8cGF0aCBkPSJNMTAuOSAxNS4xdjEuMWg0LjJjMCAuNSAwIDEuMy0uMiAxLjYtLjQuNy0uOCAxLjEtMS43IDEuNC0xLjcuMy0yLjUuMy0zLjkuMS0xLS4xLTEuOS0uOS0xLjktMS45di00LjJjMC0uNS45LTEuNiAyLTEuNmgzLjhjMS41IDAgMi40LTEuNCAyLjQtMi44VjYuNmgxLjdDMTguNSA2LjkgMTkgOCAxOSA4LjlWMTNjMCAxLS43IDIuMS0xLjkgMi4xaC02LjJ6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-r-kernel: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1jb250cmFzdDMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjMjE5NkYzIiBkPSJNNC40IDIuNWMxLjItLjEgMi45LS4zIDQuOS0uMyAyLjUgMCA0LjEuNCA1LjIgMS4zIDEgLjcgMS41IDEuOSAxLjUgMy41IDAgMi0xLjQgMy41LTIuOSA0LjEgMS4yLjQgMS43IDEuNiAyLjIgMyAuNiAxLjkgMSAzLjkgMS4zIDQuNmgtMy44Yy0uMy0uNC0uOC0xLjctMS4yLTMuN3MtMS4yLTIuNi0yLjYtMi42aC0uOXY2LjRINC40VjIuNXptMy43IDYuOWgxLjRjMS45IDAgMi45LS45IDIuOS0yLjNzLTEtMi4zLTIuOC0yLjNjLS43IDAtMS4zIDAtMS42LjJ2NC41aC4xdi0uMXoiLz4KPC9zdmc+Cg==);
  --jp-icon-react: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMTUwIDE1MCA1NDEuOSAyOTUuMyI+CiAgPGcgY2xhc3M9ImpwLWljb24tYnJhbmQyIGpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iIzYxREFGQiI+CiAgICA8cGF0aCBkPSJNNjY2LjMgMjk2LjVjMC0zMi41LTQwLjctNjMuMy0xMDMuMS04Mi40IDE0LjQtNjMuNiA4LTExNC4yLTIwLjItMTMwLjQtNi41LTMuOC0xNC4xLTUuNi0yMi40LTUuNnYyMi4zYzQuNiAwIDguMy45IDExLjQgMi42IDEzLjYgNy44IDE5LjUgMzcuNSAxNC45IDc1LjctMS4xIDkuNC0yLjkgMTkuMy01LjEgMjkuNC0xOS42LTQuOC00MS04LjUtNjMuNS0xMC45LTEzLjUtMTguNS0yNy41LTM1LjMtNDEuNi01MCAzMi42LTMwLjMgNjMuMi00Ni45IDg0LTQ2LjlWNzhjLTI3LjUgMC02My41IDE5LjYtOTkuOSA1My42LTM2LjQtMzMuOC03Mi40LTUzLjItOTkuOS01My4ydjIyLjNjMjAuNyAwIDUxLjQgMTYuNSA4NCA0Ni42LTE0IDE0LjctMjggMzEuNC00MS4zIDQ5LjktMjIuNiAyLjQtNDQgNi4xLTYzLjYgMTEtMi4zLTEwLTQtMTkuNy01LjItMjktNC43LTM4LjIgMS4xLTY3LjkgMTQuNi03NS44IDMtMS44IDYuOS0yLjYgMTEuNS0yLjZWNzguNWMtOC40IDAtMTYgMS44LTIyLjYgNS42LTI4LjEgMTYuMi0zNC40IDY2LjctMTkuOSAxMzAuMS02Mi4yIDE5LjItMTAyLjcgNDkuOS0xMDIuNyA4Mi4zIDAgMzIuNSA0MC43IDYzLjMgMTAzLjEgODIuNC0xNC40IDYzLjYtOCAxMTQuMiAyMC4yIDEzMC40IDYuNSAzLjggMTQuMSA1LjYgMjIuNSA1LjYgMjcuNSAwIDYzLjUtMTkuNiA5OS45LTUzLjYgMzYuNCAzMy44IDcyLjQgNTMuMiA5OS45IDUzLjIgOC40IDAgMTYtMS44IDIyLjYtNS42IDI4LjEtMTYuMiAzNC40LTY2LjcgMTkuOS0xMzAuMSA2Mi0xOS4xIDEwMi41LTQ5LjkgMTAyLjUtODIuM3ptLTEzMC4yLTY2LjdjLTMuNyAxMi45LTguMyAyNi4yLTEzLjUgMzkuNS00LjEtOC04LjQtMTYtMTMuMS0yNC00LjYtOC05LjUtMTUuOC0xNC40LTIzLjQgMTQuMiAyLjEgMjcuOSA0LjcgNDEgNy45em0tNDUuOCAxMDYuNWMtNy44IDEzLjUtMTUuOCAyNi4zLTI0LjEgMzguMi0xNC45IDEuMy0zMCAyLTQ1LjIgMi0xNS4xIDAtMzAuMi0uNy00NS0xLjktOC4zLTExLjktMTYuNC0yNC42LTI0LjItMzgtNy42LTEzLjEtMTQuNS0yNi40LTIwLjgtMzkuOCA2LjItMTMuNCAxMy4yLTI2LjggMjAuNy0zOS45IDcuOC0xMy41IDE1LjgtMjYuMyAyNC4xLTM4LjIgMTQuOS0xLjMgMzAtMiA0NS4yLTIgMTUuMSAwIDMwLjIuNyA0NSAxLjkgOC4zIDExLjkgMTYuNCAyNC42IDI0LjIgMzggNy42IDEzLjEgMTQuNSAyNi40IDIwLjggMzkuOC02LjMgMTMuNC0xMy4yIDI2LjgtMjAuNyAzOS45em0zMi4zLTEzYzUuNCAxMy40IDEwIDI2LjggMTMuOCAzOS44LTEzLjEgMy4yLTI2LjkgNS45LTQxLjIgOCA0LjktNy43IDkuOC0xNS42IDE0LjQtMjMuNyA0LjYtOCA4LjktMTYuMSAxMy0yNC4xek00MjEuMiA0MzBjLTkuMy05LjYtMTguNi0yMC4zLTI3LjgtMzIgOSAuNCAxOC4yLjcgMjcuNS43IDkuNCAwIDE4LjctLjIgMjcuOC0uNy05IDExLjctMTguMyAyMi40LTI3LjUgMzJ6bS03NC40LTU4LjljLTE0LjItMi4xLTI3LjktNC43LTQxLTcuOSAzLjctMTIuOSA4LjMtMjYuMiAxMy41LTM5LjUgNC4xIDggOC40IDE2IDEzLjEgMjQgNC43IDggOS41IDE1LjggMTQuNCAyMy40ek00MjAuNyAxNjNjOS4zIDkuNiAxOC42IDIwLjMgMjcuOCAzMi05LS40LTE4LjItLjctMjcuNS0uNy05LjQgMC0xOC43LjItMjcuOC43IDktMTEuNyAxOC4zLTIyLjQgMjcuNS0zMnptLTc0IDU4LjljLTQuOSA3LjctOS44IDE1LjYtMTQuNCAyMy43LTQuNiA4LTguOSAxNi0xMyAyNC01LjQtMTMuNC0xMC0yNi44LTEzLjgtMzkuOCAxMy4xLTMuMSAyNi45LTUuOCA0MS4yLTcuOXptLTkwLjUgMTI1LjJjLTM1LjQtMTUuMS01OC4zLTM0LjktNTguMy01MC42IDAtMTUuNyAyMi45LTM1LjYgNTguMy01MC42IDguNi0zLjcgMTgtNyAyNy43LTEwLjEgNS43IDE5LjYgMTMuMiA0MCAyMi41IDYwLjktOS4yIDIwLjgtMTYuNiA0MS4xLTIyLjIgNjAuNi05LjktMy4xLTE5LjMtNi41LTI4LTEwLjJ6TTMxMCA0OTBjLTEzLjYtNy44LTE5LjUtMzcuNS0xNC45LTc1LjcgMS4xLTkuNCAyLjktMTkuMyA1LjEtMjkuNCAxOS42IDQuOCA0MSA4LjUgNjMuNSAxMC45IDEzLjUgMTguNSAyNy41IDM1LjMgNDEuNiA1MC0zMi42IDMwLjMtNjMuMiA0Ni45LTg0IDQ2LjktNC41LS4xLTguMy0xLTExLjMtMi43em0yMzcuMi03Ni4yYzQuNyAzOC4yLTEuMSA2Ny45LTE0LjYgNzUuOC0zIDEuOC02LjkgMi42LTExLjUgMi42LTIwLjcgMC01MS40LTE2LjUtODQtNDYuNiAxNC0xNC43IDI4LTMxLjQgNDEuMy00OS45IDIyLjYtMi40IDQ0LTYuMSA2My42LTExIDIuMyAxMC4xIDQuMSAxOS44IDUuMiAyOS4xem0zOC41LTY2LjdjLTguNiAzLjctMTggNy0yNy43IDEwLjEtNS43LTE5LjYtMTMuMi00MC0yMi41LTYwLjkgOS4yLTIwLjggMTYuNi00MS4xIDIyLjItNjAuNiA5LjkgMy4xIDE5LjMgNi41IDI4LjEgMTAuMiAzNS40IDE1LjEgNTguMyAzNC45IDU4LjMgNTAuNi0uMSAxNS43LTIzIDM1LjYtNTguNCA1MC42ek0zMjAuOCA3OC40eiIvPgogICAgPGNpcmNsZSBjeD0iNDIwLjkiIGN5PSIyOTYuNSIgcj0iNDUuNyIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-refresh: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTkgMTMuNWMtMi40OSAwLTQuNS0yLjAxLTQuNS00LjVTNi41MSA0LjUgOSA0LjVjMS4yNCAwIDIuMzYuNTIgMy4xNyAxLjMzTDEwIDhoNVYzbC0xLjc2IDEuNzZDMTIuMTUgMy42OCAxMC42NiAzIDkgMyA1LjY5IDMgMy4wMSA1LjY5IDMuMDEgOVM1LjY5IDE1IDkgMTVjMi45NyAwIDUuNDMtMi4xNiA1LjktNWgtMS41MmMtLjQ2IDItMi4yNCAzLjUtNC4zOCAzLjV6Ii8+CiAgICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-regex: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwIDIwIj4KICA8ZyBjbGFzcz0ianAtaWNvbjIiIGZpbGw9IiM0MTQxNDEiPgogICAgPHJlY3QgeD0iMiIgeT0iMiIgd2lkdGg9IjE2IiBoZWlnaHQ9IjE2Ii8+CiAgPC9nPgoKICA8ZyBjbGFzcz0ianAtaWNvbi1hY2NlbnQyIiBmaWxsPSIjRkZGIj4KICAgIDxjaXJjbGUgY2xhc3M9InN0MiIgY3g9IjUuNSIgY3k9IjE0LjUiIHI9IjEuNSIvPgogICAgPHJlY3QgeD0iMTIiIHk9IjQiIGNsYXNzPSJzdDIiIHdpZHRoPSIxIiBoZWlnaHQ9IjgiLz4KICAgIDxyZWN0IHg9IjguNSIgeT0iNy41IiB0cmFuc2Zvcm09Im1hdHJpeCgwLjg2NiAtMC41IDAuNSAwLjg2NiAtMi4zMjU1IDcuMzIxOSkiIGNsYXNzPSJzdDIiIHdpZHRoPSI4IiBoZWlnaHQ9IjEiLz4KICAgIDxyZWN0IHg9IjEyIiB5PSI0IiB0cmFuc2Zvcm09Im1hdHJpeCgwLjUgLTAuODY2IDAuODY2IDAuNSAtMC42Nzc5IDE0LjgyNTIpIiBjbGFzcz0ic3QyIiB3aWR0aD0iMSIgaGVpZ2h0PSI4Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-run: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTggNXYxNGwxMS03eiIvPgogICAgPC9nPgo8L3N2Zz4K);
  --jp-icon-running: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDUxMiA1MTIiPgogIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICA8cGF0aCBkPSJNMjU2IDhDMTE5IDggOCAxMTkgOCAyNTZzMTExIDI0OCAyNDggMjQ4IDI0OC0xMTEgMjQ4LTI0OFMzOTMgOCAyNTYgOHptOTYgMzI4YzAgOC44LTcuMiAxNi0xNiAxNkgxNzZjLTguOCAwLTE2LTcuMi0xNi0xNlYxNzZjMC04LjggNy4yLTE2IDE2LTE2aDE2MGM4LjggMCAxNiA3LjIgMTYgMTZ2MTYweiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-save: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTE3IDNINWMtMS4xMSAwLTIgLjktMiAydjE0YzAgMS4xLjg5IDIgMiAyaDE0YzEuMSAwIDItLjkgMi0yVjdsLTQtNHptLTUgMTZjLTEuNjYgMC0zLTEuMzQtMy0zczEuMzQtMyAzLTMgMyAxLjM0IDMgMy0xLjM0IDMtMyAzem0zLTEwSDVWNWgxMHY0eiIvPgogICAgPC9nPgo8L3N2Zz4K);
  --jp-icon-search: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMTggMTgiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEyLjEsMTAuOWgtMC43bC0wLjItMC4yYzAuOC0wLjksMS4zLTIuMiwxLjMtMy41YzAtMy0yLjQtNS40LTUuNC01LjRTMS44LDQuMiwxLjgsNy4xczIuNCw1LjQsNS40LDUuNCBjMS4zLDAsMi41LTAuNSwzLjUtMS4zbDAuMiwwLjJ2MC43bDQuMSw0LjFsMS4yLTEuMkwxMi4xLDEwLjl6IE03LjEsMTAuOWMtMi4xLDAtMy43LTEuNy0zLjctMy43czEuNy0zLjcsMy43LTMuN3MzLjcsMS43LDMuNywzLjcgUzkuMiwxMC45LDcuMSwxMC45eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-settings: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTkuNDMgMTIuOThjLjA0LS4zMi4wNy0uNjQuMDctLjk4cy0uMDMtLjY2LS4wNy0uOThsMi4xMS0xLjY1Yy4xOS0uMTUuMjQtLjQyLjEyLS42NGwtMi0zLjQ2Yy0uMTItLjIyLS4zOS0uMy0uNjEtLjIybC0yLjQ5IDFjLS41Mi0uNC0xLjA4LS43My0xLjY5LS45OGwtLjM4LTIuNjVBLjQ4OC40ODggMCAwMDE0IDJoLTRjLS4yNSAwLS40Ni4xOC0uNDkuNDJsLS4zOCAyLjY1Yy0uNjEuMjUtMS4xNy41OS0xLjY5Ljk4bC0yLjQ5LTFjLS4yMy0uMDktLjQ5IDAtLjYxLjIybC0yIDMuNDZjLS4xMy4yMi0uMDcuNDkuMTIuNjRsMi4xMSAxLjY1Yy0uMDQuMzItLjA3LjY1LS4wNy45OHMuMDMuNjYuMDcuOThsLTIuMTEgMS42NWMtLjE5LjE1LS4yNC40Mi0uMTIuNjRsMiAzLjQ2Yy4xMi4yMi4zOS4zLjYxLjIybDIuNDktMWMuNTIuNCAxLjA4LjczIDEuNjkuOThsLjM4IDIuNjVjLjAzLjI0LjI0LjQyLjQ5LjQyaDRjLjI1IDAgLjQ2LS4xOC40OS0uNDJsLjM4LTIuNjVjLjYxLS4yNSAxLjE3LS41OSAxLjY5LS45OGwyLjQ5IDFjLjIzLjA5LjQ5IDAgLjYxLS4yMmwyLTMuNDZjLjEyLS4yMi4wNy0uNDktLjEyLS42NGwtMi4xMS0xLjY1ek0xMiAxNS41Yy0xLjkzIDAtMy41LTEuNTctMy41LTMuNXMxLjU3LTMuNSAzLjUtMy41IDMuNSAxLjU3IDMuNSAzLjUtMS41NyAzLjUtMy41IDMuNXoiLz4KPC9zdmc+Cg==);
  --jp-icon-spreadsheet: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1jb250cmFzdDEganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNENBRjUwIiBkPSJNMi4yIDIuMnYxNy42aDE3LjZWMi4ySDIuMnptMTUuNCA3LjdoLTUuNVY0LjRoNS41djUuNXpNOS45IDQuNHY1LjVINC40VjQuNGg1LjV6bS01LjUgNy43aDUuNXY1LjVINC40di01LjV6bTcuNyA1LjV2LTUuNWg1LjV2NS41aC01LjV6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-stop: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTAgMGgyNHYyNEgweiIgZmlsbD0ibm9uZSIvPgogICAgICAgIDxwYXRoIGQ9Ik02IDZoMTJ2MTJINnoiLz4KICAgIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-tab: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTIxIDNIM2MtMS4xIDAtMiAuOS0yIDJ2MTRjMCAxLjEuOSAyIDIgMmgxOGMxLjEgMCAyLS45IDItMlY1YzAtMS4xLS45LTItMi0yem0wIDE2SDNWNWgxMHY0aDh2MTB6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-terminal: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0IiA+CiAgICA8cmVjdCBjbGFzcz0ianAtaWNvbjIganAtaWNvbi1zZWxlY3RhYmxlIiB3aWR0aD0iMjAiIGhlaWdodD0iMjAiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDIgMikiIGZpbGw9IiMzMzMzMzMiLz4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uLWFjY2VudDIganAtaWNvbi1zZWxlY3RhYmxlLWludmVyc2UiIGQ9Ik01LjA1NjY0IDguNzYxNzJDNS4wNTY2NCA4LjU5NzY2IDUuMDMxMjUgOC40NTMxMiA0Ljk4MDQ3IDguMzI4MTJDNC45MzM1OSA4LjE5OTIyIDQuODU1NDcgOC4wODIwMyA0Ljc0NjA5IDcuOTc2NTZDNC42NDA2MiA3Ljg3MTA5IDQuNSA3Ljc3NTM5IDQuMzI0MjIgNy42ODk0NUM0LjE1MjM0IDcuNTk5NjEgMy45NDMzNiA3LjUxMTcyIDMuNjk3MjcgNy40MjU3OEMzLjMwMjczIDcuMjg1MTYgMi45NDMzNiA3LjEzNjcyIDIuNjE5MTQgNi45ODA0N0MyLjI5NDkyIDYuODI0MjIgMi4wMTc1OCA2LjY0MjU4IDEuNzg3MTEgNi40MzU1NUMxLjU2MDU1IDYuMjI4NTIgMS4zODQ3NyA1Ljk4ODI4IDEuMjU5NzcgNS43MTQ4NEMxLjEzNDc3IDUuNDM3NSAxLjA3MjI3IDUuMTA5MzggMS4wNzIyNyA0LjczMDQ3QzEuMDcyMjcgNC4zOTg0NCAxLjEyODkxIDQuMDk1NyAxLjI0MjE5IDMuODIyMjdDMS4zNTU0NyAzLjU0NDkyIDEuNTE1NjIgMy4zMDQ2OSAxLjcyMjY2IDMuMTAxNTZDMS45Mjk2OSAyLjg5ODQ0IDIuMTc5NjkgMi43MzQzNyAyLjQ3MjY2IDIuNjA5MzhDMi43NjU2MiAyLjQ4NDM4IDMuMDkxOCAyLjQwNDMgMy40NTExNyAyLjM2OTE0VjEuMTA5MzhINC4zODg2N1YyLjM4MDg2QzQuNzQwMjMgMi40Mjc3MyA1LjA1NjY0IDIuNTIzNDQgNS4zMzc4OSAyLjY2Nzk3QzUuNjE5MTQgMi44MTI1IDUuODU3NDIgMy4wMDE5NSA2LjA1MjczIDMuMjM2MzNDNi4yNTE5NSAzLjQ2NjggNi40MDQzIDMuNzQwMjMgNi41MDk3NyA0LjA1NjY0QzYuNjE5MTQgNC4zNjkxNCA2LjY3MzgzIDQuNzIwNyA2LjY3MzgzIDUuMTExMzNINS4wNDQ5MkM1LjA0NDkyIDQuNjM4NjcgNC45Mzc1IDQuMjgxMjUgNC43MjI2NiA0LjAzOTA2QzQuNTA3ODEgMy43OTI5NyA0LjIxNjggMy42Njk5MiAzLjg0OTYxIDMuNjY5OTJDMy42NTAzOSAzLjY2OTkyIDMuNDc2NTYgMy42OTcyNyAzLjMyODEyIDMuNzUxOTVDMy4xODM1OSAzLjgwMjczIDMuMDY0NDUgMy44NzY5NSAyLjk3MDcgMy45NzQ2MUMyLjg3Njk1IDQuMDY4MzYgMi44MDY2NCA0LjE3OTY5IDIuNzU5NzcgNC4zMDg1OUMyLjcxNjggNC40Mzc1IDIuNjk1MzEgNC41NzgxMiAyLjY5NTMxIDQuNzMwNDdDMi42OTUzMSA0Ljg4MjgxIDIuNzE2OCA1LjAxOTUzIDIuNzU5NzcgNS4xNDA2MkMyLjgwNjY0IDUuMjU3ODEgMi44ODI4MSA1LjM2NzE5IDIuOTg4MjggNS40Njg3NUMzLjA5NzY2IDUuNTcwMzEgMy4yNDAyMyA1LjY2Nzk3IDMuNDE2MDIgNS43NjE3MkMzLjU5MTggNS44NTE1NiAzLjgxMDU1IDUuOTQzMzYgNC4wNzIyNyA2LjAzNzExQzQuNDY2OCA2LjE4NTU1IDQuODI0MjIgNi4zMzk4NCA1LjE0NDUzIDYuNUM1LjQ2NDg0IDYuNjU2MjUgNS43MzgyOCA2LjgzOTg0IDUuOTY0ODQgNy4wNTA3OEM2LjE5NTMxIDcuMjU3ODEgNi4zNzEwOSA3LjUgNi40OTIxOSA3Ljc3NzM0QzYuNjE3MTkgOC4wNTA3OCA2LjY3OTY5IDguMzc1IDYuNjc5NjkgOC43NUM2LjY3OTY5IDkuMDkzNzUgNi42MjMwNSA5LjQwNDMgNi41MDk3NyA5LjY4MTY0QzYuMzk2NDggOS45NTUwOCA2LjIzNDM4IDEwLjE5MTQgNi4wMjM0NCAxMC4zOTA2QzUuODEyNSAxMC41ODk4IDUuNTU4NTkgMTAuNzUgNS4yNjE3MiAxMC44NzExQzQuOTY0ODQgMTAuOTg4MyA0LjYzMjgxIDExLjA2NDUgNC4yNjU2MiAxMS4wOTk2VjEyLjI0OEgzLjMzMzk4VjExLjA5OTZDMy4wMDE5NSAxMS4wNjg0IDIuNjc5NjkgMTAuOTk2MSAyLjM2NzE5IDEwLjg4MjhDMi4wNTQ2OSAxMC43NjU2IDEuNzc3MzQgMTAuNTk3NyAxLjUzNTE2IDEwLjM3ODlDMS4yOTY4OCAxMC4xNjAyIDEuMTA1NDcgOS44ODQ3NyAwLjk2MDkzOCA5LjU1MjczQzAuODE2NDA2IDkuMjE2OCAwLjc0NDE0MSA4LjgxNDQ1IDAuNzQ0MTQxIDguMzQ1N0gyLjM3ODkxQzIuMzc4OTEgOC42MjY5NSAyLjQxOTkyIDguODYzMjggMi41MDE5NSA5LjA1NDY5QzIuNTgzOTggOS4yNDIxOSAyLjY4OTQ1IDkuMzkyNTggMi44MTgzNiA5LjUwNTg2QzIuOTUxMTcgOS42MTUyMyAzLjEwMTU2IDkuNjkzMzYgMy4yNjk1MyA5Ljc0MDIzQzMuNDM3NSA5Ljc4NzExIDMuNjA5MzggOS44MTA1NSAzLjc4NTE2IDkuODEwNTVDNC4yMDMxMiA5LjgxMDU1IDQuNTE5NTMgOS43MTI4OSA0LjczNDM4IDkuNTE3NThDNC45NDkyMiA5LjMyMjI3IDUuMDU2NjQgOS4wNzAzMSA1LjA1NjY0IDguNzYxNzJaTTEzLjQxOCAxMi4yNzE1SDguMDc0MjJWMTFIMTMuNDE4VjEyLjI3MTVaIiB0cmFuc2Zvcm09InRyYW5zbGF0ZSgzLjk1MjY0IDYpIiBmaWxsPSJ3aGl0ZSIvPgo8L3N2Zz4K);
  --jp-icon-text-editor: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTUgMTVIM3YyaDEydi0yem0wLThIM3YyaDEyVjd6TTMgMTNoMTh2LTJIM3Yyem0wIDhoMTh2LTJIM3Yyek0zIDN2MmgxOFYzSDN6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-trusted: url(data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI1Ij4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiIgc3Ryb2tlPSIjMzMzMzMzIiBzdHJva2Utd2lkdGg9IjIiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDIgMykiIGQ9Ik0xLjg2MDk0IDExLjQ0MDlDMC44MjY0NDggOC43NzAyNyAwLjg2Mzc3OSA2LjA1NzY0IDEuMjQ5MDcgNC4xOTkzMkMyLjQ4MjA2IDMuOTMzNDcgNC4wODA2OCAzLjQwMzQ3IDUuNjAxMDIgMi44NDQ5QzcuMjM1NDkgMi4yNDQ0IDguODU2NjYgMS41ODE1IDkuOTg3NiAxLjA5NTM5QzExLjA1OTcgMS41ODM0MSAxMi42MDk0IDIuMjQ0NCAxNC4yMTggMi44NDMzOUMxNS43NTAzIDMuNDEzOTQgMTcuMzk5NSAzLjk1MjU4IDE4Ljc1MzkgNC4yMTM4NUMxOS4xMzY0IDYuMDcxNzcgMTkuMTcwOSA4Ljc3NzIyIDE4LjEzOSAxMS40NDA5QzE3LjAzMDMgMTQuMzAzMiAxNC42NjY4IDE3LjE4NDQgOS45OTk5OSAxOC45MzU0QzUuMzMzMiAxNy4xODQ0IDIuOTY5NjggMTQuMzAzMiAxLjg2MDk0IDExLjQ0MDlaIi8+CiAgICA8cGF0aCBjbGFzcz0ianAtaWNvbjIiIGZpbGw9IiMzMzMzMzMiIHN0cm9rZT0iIzMzMzMzMyIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoOCA5Ljg2NzE5KSIgZD0iTTIuODYwMTUgNC44NjUzNUwwLjcyNjU0OSAyLjk5OTU5TDAgMy42MzA0NUwyLjg2MDE1IDYuMTMxNTdMOCAwLjYzMDg3Mkw3LjI3ODU3IDBMMi44NjAxNSA0Ljg2NTM1WiIvPgo8L3N2Zz4K);
  --jp-icon-undo: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEyLjUgOGMtMi42NSAwLTUuMDUuOTktNi45IDIuNkwyIDd2OWg5bC0zLjYyLTMuNjJjMS4zOS0xLjE2IDMuMTYtMS44OCA1LjEyLTEuODggMy41NCAwIDYuNTUgMi4zMSA3LjYgNS41bDIuMzctLjc4QzIxLjA4IDExLjAzIDE3LjE1IDggMTIuNSA4eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-vega: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtaWNvbjEganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjMjEyMTIxIj4KICAgIDxwYXRoIGQ9Ik0xMC42IDUuNGwyLjItMy4ySDIuMnY3LjNsNC02LjZ6Ii8+CiAgICA8cGF0aCBkPSJNMTUuOCAyLjJsLTQuNCA2LjZMNyA2LjNsLTQuOCA4djUuNWgxNy42VjIuMmgtNHptLTcgMTUuNEg1LjV2LTQuNGgzLjN2NC40em00LjQgMEg5LjhWOS44aDMuNHY3Ljh6bTQuNCAwaC0zLjRWNi41aDMuNHYxMS4xeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-yaml: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtaWNvbi1jb250cmFzdDIganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjRDgxQjYwIj4KICAgIDxwYXRoIGQ9Ik03LjIgMTguNnYtNS40TDMgNS42aDMuM2wxLjQgMy4xYy4zLjkuNiAxLjYgMSAyLjUuMy0uOC42LTEuNiAxLTIuNWwxLjQtMy4xaDMuNGwtNC40IDcuNnY1LjVsLTIuOS0uMXoiLz4KICAgIDxjaXJjbGUgY2xhc3M9InN0MCIgY3g9IjE3LjYiIGN5PSIxNi41IiByPSIyLjEiLz4KICAgIDxjaXJjbGUgY2xhc3M9InN0MCIgY3g9IjE3LjYiIGN5PSIxMSIgcj0iMi4xIi8+CiAgPC9nPgo8L3N2Zz4K);
}

/* Icon CSS class declarations */

.jp-AddIcon {
  background-image: var(--jp-icon-add);
}
.jp-BugIcon {
  background-image: var(--jp-icon-bug);
}
.jp-BuildIcon {
  background-image: var(--jp-icon-build);
}
.jp-CaretDownEmptyIcon {
  background-image: var(--jp-icon-caret-down-empty);
}
.jp-CaretDownEmptyThinIcon {
  background-image: var(--jp-icon-caret-down-empty-thin);
}
.jp-CaretDownIcon {
  background-image: var(--jp-icon-caret-down);
}
.jp-CaretLeftIcon {
  background-image: var(--jp-icon-caret-left);
}
.jp-CaretRightIcon {
  background-image: var(--jp-icon-caret-right);
}
.jp-CaretUpEmptyThinIcon {
  background-image: var(--jp-icon-caret-up-empty-thin);
}
.jp-CaretUpIcon {
  background-image: var(--jp-icon-caret-up);
}
.jp-CaseSensitiveIcon {
  background-image: var(--jp-icon-case-sensitive);
}
.jp-CheckIcon {
  background-image: var(--jp-icon-check);
}
.jp-CircleEmptyIcon {
  background-image: var(--jp-icon-circle-empty);
}
.jp-CircleIcon {
  background-image: var(--jp-icon-circle);
}
.jp-ClearIcon {
  background-image: var(--jp-icon-clear);
}
.jp-CloseIcon {
  background-image: var(--jp-icon-close);
}
.jp-ConsoleIcon {
  background-image: var(--jp-icon-console);
}
.jp-CopyIcon {
  background-image: var(--jp-icon-copy);
}
.jp-CutIcon {
  background-image: var(--jp-icon-cut);
}
.jp-DownloadIcon {
  background-image: var(--jp-icon-download);
}
.jp-EditIcon {
  background-image: var(--jp-icon-edit);
}
.jp-EllipsesIcon {
  background-image: var(--jp-icon-ellipses);
}
.jp-ExtensionIcon {
  background-image: var(--jp-icon-extension);
}
.jp-FastForwardIcon {
  background-image: var(--jp-icon-fast-forward);
}
.jp-FileIcon {
  background-image: var(--jp-icon-file);
}
.jp-FileUploadIcon {
  background-image: var(--jp-icon-file-upload);
}
.jp-FilterListIcon {
  background-image: var(--jp-icon-filter-list);
}
.jp-FolderIcon {
  background-image: var(--jp-icon-folder);
}
.jp-Html5Icon {
  background-image: var(--jp-icon-html5);
}
.jp-ImageIcon {
  background-image: var(--jp-icon-image);
}
.jp-InspectorIcon {
  background-image: var(--jp-icon-inspector);
}
.jp-JsonIcon {
  background-image: var(--jp-icon-json);
}
.jp-JupyterFaviconIcon {
  background-image: var(--jp-icon-jupyter-favicon);
}
.jp-JupyterIcon {
  background-image: var(--jp-icon-jupyter);
}
.jp-JupyterlabWordmarkIcon {
  background-image: var(--jp-icon-jupyterlab-wordmark);
}
.jp-KernelIcon {
  background-image: var(--jp-icon-kernel);
}
.jp-KeyboardIcon {
  background-image: var(--jp-icon-keyboard);
}
.jp-LauncherIcon {
  background-image: var(--jp-icon-launcher);
}
.jp-LineFormIcon {
  background-image: var(--jp-icon-line-form);
}
.jp-LinkIcon {
  background-image: var(--jp-icon-link);
}
.jp-ListIcon {
  background-image: var(--jp-icon-list);
}
.jp-ListingsInfoIcon {
  background-image: var(--jp-icon-listings-info);
}
.jp-MarkdownIcon {
  background-image: var(--jp-icon-markdown);
}
.jp-NewFolderIcon {
  background-image: var(--jp-icon-new-folder);
}
.jp-NotTrustedIcon {
  background-image: var(--jp-icon-not-trusted);
}
.jp-NotebookIcon {
  background-image: var(--jp-icon-notebook);
}
.jp-PaletteIcon {
  background-image: var(--jp-icon-palette);
}
.jp-PasteIcon {
  background-image: var(--jp-icon-paste);
}
.jp-PythonIcon {
  background-image: var(--jp-icon-python);
}
.jp-RKernelIcon {
  background-image: var(--jp-icon-r-kernel);
}
.jp-ReactIcon {
  background-image: var(--jp-icon-react);
}
.jp-RefreshIcon {
  background-image: var(--jp-icon-refresh);
}
.jp-RegexIcon {
  background-image: var(--jp-icon-regex);
}
.jp-RunIcon {
  background-image: var(--jp-icon-run);
}
.jp-RunningIcon {
  background-image: var(--jp-icon-running);
}
.jp-SaveIcon {
  background-image: var(--jp-icon-save);
}
.jp-SearchIcon {
  background-image: var(--jp-icon-search);
}
.jp-SettingsIcon {
  background-image: var(--jp-icon-settings);
}
.jp-SpreadsheetIcon {
  background-image: var(--jp-icon-spreadsheet);
}
.jp-StopIcon {
  background-image: var(--jp-icon-stop);
}
.jp-TabIcon {
  background-image: var(--jp-icon-tab);
}
.jp-TerminalIcon {
  background-image: var(--jp-icon-terminal);
}
.jp-TextEditorIcon {
  background-image: var(--jp-icon-text-editor);
}
.jp-TrustedIcon {
  background-image: var(--jp-icon-trusted);
}
.jp-UndoIcon {
  background-image: var(--jp-icon-undo);
}
.jp-VegaIcon {
  background-image: var(--jp-icon-vega);
}
.jp-YamlIcon {
  background-image: var(--jp-icon-yaml);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/**
 * (DEPRECATED) Support for consuming icons as CSS background images
 */

:root {
  --jp-icon-search-white: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMTggMTgiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEyLjEsMTAuOWgtMC43bC0wLjItMC4yYzAuOC0wLjksMS4zLTIuMiwxLjMtMy41YzAtMy0yLjQtNS40LTUuNC01LjRTMS44LDQuMiwxLjgsNy4xczIuNCw1LjQsNS40LDUuNCBjMS4zLDAsMi41LTAuNSwzLjUtMS4zbDAuMiwwLjJ2MC43bDQuMSw0LjFsMS4yLTEuMkwxMi4xLDEwLjl6IE03LjEsMTAuOWMtMi4xLDAtMy43LTEuNy0zLjctMy43czEuNy0zLjcsMy43LTMuN3MzLjcsMS43LDMuNywzLjcgUzkuMiwxMC45LDcuMSwxMC45eiIvPgogIDwvZz4KPC9zdmc+Cg==);
}

.jp-Icon,
.jp-MaterialIcon {
  background-position: center;
  background-repeat: no-repeat;
  background-size: 16px;
  min-width: 16px;
  min-height: 16px;
}

.jp-Icon-cover {
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}

/**
 * (DEPRECATED) Support for specific CSS icon sizes
 */

.jp-Icon-16 {
  background-size: 16px;
  min-width: 16px;
  min-height: 16px;
}

.jp-Icon-18 {
  background-size: 18px;
  min-width: 18px;
  min-height: 18px;
}

.jp-Icon-20 {
  background-size: 20px;
  min-width: 20px;
  min-height: 20px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/**
 * Support for icons as inline SVG HTMLElements
 */

/* recolor the primary elements of an icon */
.jp-icon0[fill] {
  fill: var(--jp-inverse-layout-color0);
}
.jp-icon1[fill] {
  fill: var(--jp-inverse-layout-color1);
}
.jp-icon2[fill] {
  fill: var(--jp-inverse-layout-color2);
}
.jp-icon3[fill] {
  fill: var(--jp-inverse-layout-color3);
}
.jp-icon4[fill] {
  fill: var(--jp-inverse-layout-color4);
}

.jp-icon0[stroke] {
  stroke: var(--jp-inverse-layout-color0);
}
.jp-icon1[stroke] {
  stroke: var(--jp-inverse-layout-color1);
}
.jp-icon2[stroke] {
  stroke: var(--jp-inverse-layout-color2);
}
.jp-icon3[stroke] {
  stroke: var(--jp-inverse-layout-color3);
}
.jp-icon4[stroke] {
  stroke: var(--jp-inverse-layout-color4);
}
/* recolor the accent elements of an icon */
.jp-icon-accent0[fill] {
  fill: var(--jp-layout-color0);
}
.jp-icon-accent1[fill] {
  fill: var(--jp-layout-color1);
}
.jp-icon-accent2[fill] {
  fill: var(--jp-layout-color2);
}
.jp-icon-accent3[fill] {
  fill: var(--jp-layout-color3);
}
.jp-icon-accent4[fill] {
  fill: var(--jp-layout-color4);
}

.jp-icon-accent0[stroke] {
  stroke: var(--jp-layout-color0);
}
.jp-icon-accent1[stroke] {
  stroke: var(--jp-layout-color1);
}
.jp-icon-accent2[stroke] {
  stroke: var(--jp-layout-color2);
}
.jp-icon-accent3[stroke] {
  stroke: var(--jp-layout-color3);
}
.jp-icon-accent4[stroke] {
  stroke: var(--jp-layout-color4);
}
/* set the color of an icon to transparent */
.jp-icon-none[fill] {
  fill: none;
}

.jp-icon-none[stroke] {
  stroke: none;
}
/* brand icon colors. Same for light and dark */
.jp-icon-brand0[fill] {
  fill: var(--jp-brand-color0);
}
.jp-icon-brand1[fill] {
  fill: var(--jp-brand-color1);
}
.jp-icon-brand2[fill] {
  fill: var(--jp-brand-color2);
}
.jp-icon-brand3[fill] {
  fill: var(--jp-brand-color3);
}
.jp-icon-brand4[fill] {
  fill: var(--jp-brand-color4);
}

.jp-icon-brand0[stroke] {
  stroke: var(--jp-brand-color0);
}
.jp-icon-brand1[stroke] {
  stroke: var(--jp-brand-color1);
}
.jp-icon-brand2[stroke] {
  stroke: var(--jp-brand-color2);
}
.jp-icon-brand3[stroke] {
  stroke: var(--jp-brand-color3);
}
.jp-icon-brand4[stroke] {
  stroke: var(--jp-brand-color4);
}
/* warn icon colors. Same for light and dark */
.jp-icon-warn0[fill] {
  fill: var(--jp-warn-color0);
}
.jp-icon-warn1[fill] {
  fill: var(--jp-warn-color1);
}
.jp-icon-warn2[fill] {
  fill: var(--jp-warn-color2);
}
.jp-icon-warn3[fill] {
  fill: var(--jp-warn-color3);
}

.jp-icon-warn0[stroke] {
  stroke: var(--jp-warn-color0);
}
.jp-icon-warn1[stroke] {
  stroke: var(--jp-warn-color1);
}
.jp-icon-warn2[stroke] {
  stroke: var(--jp-warn-color2);
}
.jp-icon-warn3[stroke] {
  stroke: var(--jp-warn-color3);
}
/* icon colors that contrast well with each other and most backgrounds */
.jp-icon-contrast0[fill] {
  fill: var(--jp-icon-contrast-color0);
}
.jp-icon-contrast1[fill] {
  fill: var(--jp-icon-contrast-color1);
}
.jp-icon-contrast2[fill] {
  fill: var(--jp-icon-contrast-color2);
}
.jp-icon-contrast3[fill] {
  fill: var(--jp-icon-contrast-color3);
}

.jp-icon-contrast0[stroke] {
  stroke: var(--jp-icon-contrast-color0);
}
.jp-icon-contrast1[stroke] {
  stroke: var(--jp-icon-contrast-color1);
}
.jp-icon-contrast2[stroke] {
  stroke: var(--jp-icon-contrast-color2);
}
.jp-icon-contrast3[stroke] {
  stroke: var(--jp-icon-contrast-color3);
}

/* CSS for icons in selected items in the settings editor */
#setting-editor .jp-PluginList .jp-mod-selected .jp-icon-selectable[fill] {
  fill: #fff;
}
#setting-editor
  .jp-PluginList
  .jp-mod-selected
  .jp-icon-selectable-inverse[fill] {
  fill: var(--jp-brand-color1);
}

/* CSS for icons in selected filebrowser listing items */
.jp-DirListing-item.jp-mod-selected .jp-icon-selectable[fill] {
  fill: #fff;
}
.jp-DirListing-item.jp-mod-selected .jp-icon-selectable-inverse[fill] {
  fill: var(--jp-brand-color1);
}

/* CSS for icons in selected tabs in the sidebar tab manager */
#tab-manager .lm-TabBar-tab.jp-mod-active .jp-icon-selectable[fill] {
  fill: #fff;
}

#tab-manager .lm-TabBar-tab.jp-mod-active .jp-icon-selectable-inverse[fill] {
  fill: var(--jp-brand-color1);
}
#tab-manager
  .lm-TabBar-tab.jp-mod-active
  .jp-icon-hover
  :hover
  .jp-icon-selectable[fill] {
  fill: var(--jp-brand-color1);
}

#tab-manager
  .lm-TabBar-tab.jp-mod-active
  .jp-icon-hover
  :hover
  .jp-icon-selectable-inverse[fill] {
  fill: #fff;
}

/**
 * TODO: come up with non css-hack solution for showing the busy icon on top
 *  of the close icon
 * CSS for complex behavior of close icon of tabs in the sidebar tab manager
 */
#tab-manager
  .lm-TabBar-tab.jp-mod-dirty
  > .lm-TabBar-tabCloseIcon
  > :not(:hover)
  > .jp-icon3[fill] {
  fill: none;
}
#tab-manager
  .lm-TabBar-tab.jp-mod-dirty
  > .lm-TabBar-tabCloseIcon
  > :not(:hover)
  > .jp-icon-busy[fill] {
  fill: var(--jp-inverse-layout-color3);
}

#tab-manager
  .lm-TabBar-tab.jp-mod-dirty.jp-mod-active
  > .lm-TabBar-tabCloseIcon
  > :not(:hover)
  > .jp-icon-busy[fill] {
  fill: #fff;
}

/**
* TODO: come up with non css-hack solution for showing the busy icon on top
*  of the close icon
* CSS for complex behavior of close icon of tabs in the main area tabbar
*/
.lm-DockPanel-tabBar
  .lm-TabBar-tab.lm-mod-closable.jp-mod-dirty
  > .lm-TabBar-tabCloseIcon
  > :not(:hover)
  > .jp-icon3[fill] {
  fill: none;
}
.lm-DockPanel-tabBar
  .lm-TabBar-tab.lm-mod-closable.jp-mod-dirty
  > .lm-TabBar-tabCloseIcon
  > :not(:hover)
  > .jp-icon-busy[fill] {
  fill: var(--jp-inverse-layout-color3);
}

/* CSS for icons in status bar */
#jp-main-statusbar .jp-mod-selected .jp-icon-selectable[fill] {
  fill: #fff;
}

#jp-main-statusbar .jp-mod-selected .jp-icon-selectable-inverse[fill] {
  fill: var(--jp-brand-color1);
}
/* special handling for splash icon CSS. While the theme CSS reloads during
   splash, the splash icon can loose theming. To prevent that, we set a
   default for its color variable */
:root {
  --jp-warn-color0: var(--md-orange-700);
}

/* not sure what to do with this one, used in filebrowser listing */
.jp-DragIcon {
  margin-right: 4px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/**
 * Support for alt colors for icons as inline SVG HTMLElements
 */

/* alt recolor the primary elements of an icon */
.jp-icon-alt .jp-icon0[fill] {
  fill: var(--jp-layout-color0);
}
.jp-icon-alt .jp-icon1[fill] {
  fill: var(--jp-layout-color1);
}
.jp-icon-alt .jp-icon2[fill] {
  fill: var(--jp-layout-color2);
}
.jp-icon-alt .jp-icon3[fill] {
  fill: var(--jp-layout-color3);
}
.jp-icon-alt .jp-icon4[fill] {
  fill: var(--jp-layout-color4);
}

.jp-icon-alt .jp-icon0[stroke] {
  stroke: var(--jp-layout-color0);
}
.jp-icon-alt .jp-icon1[stroke] {
  stroke: var(--jp-layout-color1);
}
.jp-icon-alt .jp-icon2[stroke] {
  stroke: var(--jp-layout-color2);
}
.jp-icon-alt .jp-icon3[stroke] {
  stroke: var(--jp-layout-color3);
}
.jp-icon-alt .jp-icon4[stroke] {
  stroke: var(--jp-layout-color4);
}

/* alt recolor the accent elements of an icon */
.jp-icon-alt .jp-icon-accent0[fill] {
  fill: var(--jp-inverse-layout-color0);
}
.jp-icon-alt .jp-icon-accent1[fill] {
  fill: var(--jp-inverse-layout-color1);
}
.jp-icon-alt .jp-icon-accent2[fill] {
  fill: var(--jp-inverse-layout-color2);
}
.jp-icon-alt .jp-icon-accent3[fill] {
  fill: var(--jp-inverse-layout-color3);
}
.jp-icon-alt .jp-icon-accent4[fill] {
  fill: var(--jp-inverse-layout-color4);
}

.jp-icon-alt .jp-icon-accent0[stroke] {
  stroke: var(--jp-inverse-layout-color0);
}
.jp-icon-alt .jp-icon-accent1[stroke] {
  stroke: var(--jp-inverse-layout-color1);
}
.jp-icon-alt .jp-icon-accent2[stroke] {
  stroke: var(--jp-inverse-layout-color2);
}
.jp-icon-alt .jp-icon-accent3[stroke] {
  stroke: var(--jp-inverse-layout-color3);
}
.jp-icon-alt .jp-icon-accent4[stroke] {
  stroke: var(--jp-inverse-layout-color4);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-icon-hoverShow:not(:hover) svg {
  display: none !important;
}

/**
 * Support for hover colors for icons as inline SVG HTMLElements
 */

/**
 * regular colors
 */

/* recolor the primary elements of an icon */
.jp-icon-hover :hover .jp-icon0-hover[fill] {
  fill: var(--jp-inverse-layout-color0);
}
.jp-icon-hover :hover .jp-icon1-hover[fill] {
  fill: var(--jp-inverse-layout-color1);
}
.jp-icon-hover :hover .jp-icon2-hover[fill] {
  fill: var(--jp-inverse-layout-color2);
}
.jp-icon-hover :hover .jp-icon3-hover[fill] {
  fill: var(--jp-inverse-layout-color3);
}
.jp-icon-hover :hover .jp-icon4-hover[fill] {
  fill: var(--jp-inverse-layout-color4);
}

.jp-icon-hover :hover .jp-icon0-hover[stroke] {
  stroke: var(--jp-inverse-layout-color0);
}
.jp-icon-hover :hover .jp-icon1-hover[stroke] {
  stroke: var(--jp-inverse-layout-color1);
}
.jp-icon-hover :hover .jp-icon2-hover[stroke] {
  stroke: var(--jp-inverse-layout-color2);
}
.jp-icon-hover :hover .jp-icon3-hover[stroke] {
  stroke: var(--jp-inverse-layout-color3);
}
.jp-icon-hover :hover .jp-icon4-hover[stroke] {
  stroke: var(--jp-inverse-layout-color4);
}

/* recolor the accent elements of an icon */
.jp-icon-hover :hover .jp-icon-accent0-hover[fill] {
  fill: var(--jp-layout-color0);
}
.jp-icon-hover :hover .jp-icon-accent1-hover[fill] {
  fill: var(--jp-layout-color1);
}
.jp-icon-hover :hover .jp-icon-accent2-hover[fill] {
  fill: var(--jp-layout-color2);
}
.jp-icon-hover :hover .jp-icon-accent3-hover[fill] {
  fill: var(--jp-layout-color3);
}
.jp-icon-hover :hover .jp-icon-accent4-hover[fill] {
  fill: var(--jp-layout-color4);
}

.jp-icon-hover :hover .jp-icon-accent0-hover[stroke] {
  stroke: var(--jp-layout-color0);
}
.jp-icon-hover :hover .jp-icon-accent1-hover[stroke] {
  stroke: var(--jp-layout-color1);
}
.jp-icon-hover :hover .jp-icon-accent2-hover[stroke] {
  stroke: var(--jp-layout-color2);
}
.jp-icon-hover :hover .jp-icon-accent3-hover[stroke] {
  stroke: var(--jp-layout-color3);
}
.jp-icon-hover :hover .jp-icon-accent4-hover[stroke] {
  stroke: var(--jp-layout-color4);
}

/* set the color of an icon to transparent */
.jp-icon-hover :hover .jp-icon-none-hover[fill] {
  fill: none;
}

.jp-icon-hover :hover .jp-icon-none-hover[stroke] {
  stroke: none;
}

/**
 * inverse colors
 */

/* inverse recolor the primary elements of an icon */
.jp-icon-hover.jp-icon-alt :hover .jp-icon0-hover[fill] {
  fill: var(--jp-layout-color0);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon1-hover[fill] {
  fill: var(--jp-layout-color1);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon2-hover[fill] {
  fill: var(--jp-layout-color2);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon3-hover[fill] {
  fill: var(--jp-layout-color3);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon4-hover[fill] {
  fill: var(--jp-layout-color4);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon0-hover[stroke] {
  stroke: var(--jp-layout-color0);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon1-hover[stroke] {
  stroke: var(--jp-layout-color1);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon2-hover[stroke] {
  stroke: var(--jp-layout-color2);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon3-hover[stroke] {
  stroke: var(--jp-layout-color3);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon4-hover[stroke] {
  stroke: var(--jp-layout-color4);
}

/* inverse recolor the accent elements of an icon */
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent0-hover[fill] {
  fill: var(--jp-inverse-layout-color0);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent1-hover[fill] {
  fill: var(--jp-inverse-layout-color1);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent2-hover[fill] {
  fill: var(--jp-inverse-layout-color2);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent3-hover[fill] {
  fill: var(--jp-inverse-layout-color3);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent4-hover[fill] {
  fill: var(--jp-inverse-layout-color4);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent0-hover[stroke] {
  stroke: var(--jp-inverse-layout-color0);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent1-hover[stroke] {
  stroke: var(--jp-inverse-layout-color1);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent2-hover[stroke] {
  stroke: var(--jp-inverse-layout-color2);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent3-hover[stroke] {
  stroke: var(--jp-inverse-layout-color3);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent4-hover[stroke] {
  stroke: var(--jp-inverse-layout-color4);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* Sibling imports */

/* Override Blueprint's _reset.scss styles */
html {
  box-sizing: unset;
}

*,
*::before,
*::after {
  box-sizing: unset;
}

body {
  color: unset;
  font-family: var(--jp-ui-font-family);
}

p {
  margin-top: unset;
  margin-bottom: unset;
}

small {
  font-size: unset;
}

strong {
  font-weight: unset;
}

/* Override Blueprint's _typography.scss styles */
a {
  text-decoration: unset;
  color: unset;
}
a:hover {
  text-decoration: unset;
  color: unset;
}

/* Override Blueprint's _accessibility.scss styles */
:focus {
  outline: unset;
  outline-offset: unset;
  -moz-outline-radius: unset;
}

/* Styles for ui-components */
.jp-Button {
  border-radius: var(--jp-border-radius);
  padding: 0px 12px;
  font-size: var(--jp-ui-font-size1);
}

/* Use our own theme for hover styles */
button.jp-Button.bp3-button.bp3-minimal:hover {
  background-color: var(--jp-layout-color2);
}
.jp-Button.minimal {
  color: unset !important;
}

.jp-Button.jp-ToolbarButtonComponent {
  text-transform: none;
}

.jp-InputGroup input {
  box-sizing: border-box;
  border-radius: 0;
  background-color: transparent;
  color: var(--jp-ui-font-color0);
  box-shadow: inset 0 0 0 var(--jp-border-width) var(--jp-input-border-color);
}

.jp-InputGroup input:focus {
  box-shadow: inset 0 0 0 var(--jp-border-width)
      var(--jp-input-active-box-shadow-color),
    inset 0 0 0 3px var(--jp-input-active-box-shadow-color);
}

.jp-InputGroup input::placeholder,
input::placeholder {
  color: var(--jp-ui-font-color3);
}

.jp-BPIcon {
  display: inline-block;
  vertical-align: middle;
  margin: auto;
}

/* Stop blueprint futzing with our icon fills */
.bp3-icon.jp-BPIcon > svg:not([fill]) {
  fill: var(--jp-inverse-layout-color3);
}

.jp-InputGroupAction {
  padding: 6px;
}

.jp-HTMLSelect.jp-DefaultStyle select {
  background-color: initial;
  border: none;
  border-radius: 0;
  box-shadow: none;
  color: var(--jp-ui-font-color0);
  display: block;
  font-size: var(--jp-ui-font-size1);
  height: 24px;
  line-height: 14px;
  padding: 0 25px 0 10px;
  text-align: left;
  -moz-appearance: none;
  -webkit-appearance: none;
}

/* Use our own theme for hover and option styles */
.jp-HTMLSelect.jp-DefaultStyle select:hover,
.jp-HTMLSelect.jp-DefaultStyle select > option {
  background-color: var(--jp-layout-color2);
  color: var(--jp-ui-font-color0);
}
select {
  box-sizing: border-box;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* This file was auto-generated by ensurePackage() in @jupyterlab/buildutils */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-Collapse {
  display: flex;
  flex-direction: column;
  align-items: stretch;
  border-top: 1px solid var(--jp-border-color2);
  border-bottom: 1px solid var(--jp-border-color2);
}

.jp-Collapse-header {
  padding: 1px 12px;
  color: var(--jp-ui-font-color1);
  background-color: var(--jp-layout-color1);
  font-size: var(--jp-ui-font-size2);
}

.jp-Collapse-header:hover {
  background-color: var(--jp-layout-color2);
}

.jp-Collapse-contents {
  padding: 0px 12px 0px 12px;
  background-color: var(--jp-layout-color1);
  color: var(--jp-ui-font-color1);
  overflow: auto;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Variables
|----------------------------------------------------------------------------*/

:root {
  --jp-private-commandpalette-search-height: 28px;
}

/*-----------------------------------------------------------------------------
| Overall styles
|----------------------------------------------------------------------------*/

.lm-CommandPalette {
  padding-bottom: 0px;
  color: var(--jp-ui-font-color1);
  background: var(--jp-layout-color1);
  /* This is needed so that all font sizing of children done in ems is
   * relative to this base size */
  font-size: var(--jp-ui-font-size1);
}

/*-----------------------------------------------------------------------------
| Search
|----------------------------------------------------------------------------*/

.lm-CommandPalette-search {
  padding: 4px;
  background-color: var(--jp-layout-color1);
  z-index: 2;
}

.lm-CommandPalette-wrapper {
  overflow: overlay;
  padding: 0px 9px;
  background-color: var(--jp-input-active-background);
  height: 30px;
  box-shadow: inset 0 0 0 var(--jp-border-width) var(--jp-input-border-color);
}

.lm-CommandPalette.lm-mod-focused .lm-CommandPalette-wrapper {
  box-shadow: inset 0 0 0 1px var(--jp-input-active-box-shadow-color),
    inset 0 0 0 3px var(--jp-input-active-box-shadow-color);
}

.lm-CommandPalette-wrapper::after {
  content: ' ';
  color: white;
  background-color: var(--jp-brand-color1);
  position: absolute;
  top: 4px;
  right: 4px;
  height: 30px;
  width: 10px;
  padding: 0px 10px;
  background-image: var(--jp-icon-search-white);
  background-size: 20px;
  background-repeat: no-repeat;
  background-position: center;
}

.lm-CommandPalette-input {
  background: transparent;
  width: calc(100% - 18px);
  float: left;
  border: none;
  outline: none;
  font-size: var(--jp-ui-font-size1);
  color: var(--jp-ui-font-color0);
  line-height: var(--jp-private-commandpalette-search-height);
}

.lm-CommandPalette-input::-webkit-input-placeholder,
.lm-CommandPalette-input::-moz-placeholder,
.lm-CommandPalette-input:-ms-input-placeholder {
  color: var(--jp-ui-font-color3);
  font-size: var(--jp-ui-font-size1);
}

/*-----------------------------------------------------------------------------
| Results
|----------------------------------------------------------------------------*/

.lm-CommandPalette-header:first-child {
  margin-top: 0px;
}

.lm-CommandPalette-header {
  border-bottom: solid var(--jp-border-width) var(--jp-border-color2);
  color: var(--jp-ui-font-color1);
  cursor: pointer;
  display: flex;
  font-size: var(--jp-ui-font-size0);
  font-weight: 600;
  letter-spacing: 1px;
  margin-top: 8px;
  padding: 8px 0 8px 12px;
  text-transform: uppercase;
}

.lm-CommandPalette-header.lm-mod-active {
  background: var(--jp-layout-color2);
}

.lm-CommandPalette-header > mark {
  background-color: transparent;
  font-weight: bold;
  color: var(--jp-ui-font-color1);
}

.lm-CommandPalette-item {
  padding: 4px 12px 4px 4px;
  color: var(--jp-ui-font-color1);
  font-size: var(--jp-ui-font-size1);
  font-weight: 400;
  display: flex;
}

.lm-CommandPalette-item.lm-mod-disabled {
  color: var(--jp-ui-font-color3);
}

.lm-CommandPalette-item.lm-mod-active {
  background: var(--jp-layout-color3);
}

.lm-CommandPalette-item.lm-mod-active:hover:not(.lm-mod-disabled) {
  background: var(--jp-layout-color4);
}

.lm-CommandPalette-item:hover:not(.lm-mod-active):not(.lm-mod-disabled) {
  background: var(--jp-layout-color2);
}

.lm-CommandPalette-itemContent {
  overflow: hidden;
}

.lm-CommandPalette-itemLabel > mark {
  color: var(--jp-ui-font-color0);
  background-color: transparent;
  font-weight: bold;
}

.lm-CommandPalette-item.lm-mod-disabled mark {
  color: var(--jp-ui-font-color3);
}

.lm-CommandPalette-item .lm-CommandPalette-itemIcon {
  margin: 0 4px 0 0;
  position: relative;
  width: 16px;
  top: 2px;
  flex: 0 0 auto;
}

.lm-CommandPalette-item.lm-mod-disabled .lm-CommandPalette-itemIcon {
  opacity: 0.4;
}

.lm-CommandPalette-item .lm-CommandPalette-itemShortcut {
  flex: 0 0 auto;
}

.lm-CommandPalette-itemCaption {
  display: none;
}

.lm-CommandPalette-content {
  background-color: var(--jp-layout-color1);
}

.lm-CommandPalette-content:empty:after {
  content: 'No results';
  margin: auto;
  margin-top: 20px;
  width: 100px;
  display: block;
  font-size: var(--jp-ui-font-size2);
  font-family: var(--jp-ui-font-family);
  font-weight: lighter;
}

.lm-CommandPalette-emptyMessage {
  text-align: center;
  margin-top: 24px;
  line-height: 1.32;
  padding: 0px 8px;
  color: var(--jp-content-font-color3);
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2017, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-Dialog {
  position: absolute;
  z-index: 10000;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  top: 0px;
  left: 0px;
  margin: 0;
  padding: 0;
  width: 100%;
  height: 100%;
  background: var(--jp-dialog-background);
}

.jp-Dialog-content {
  display: flex;
  flex-direction: column;
  margin-left: auto;
  margin-right: auto;
  background: var(--jp-layout-color1);
  padding: 24px;
  padding-bottom: 12px;
  min-width: 300px;
  min-height: 150px;
  max-width: 1000px;
  max-height: 500px;
  box-sizing: border-box;
  box-shadow: var(--jp-elevation-z20);
  word-wrap: break-word;
  border-radius: var(--jp-border-radius);
  /* This is needed so that all font sizing of children done in ems is
   * relative to this base size */
  font-size: var(--jp-ui-font-size1);
  color: var(--jp-ui-font-color1);
}

.jp-Dialog-button {
  overflow: visible;
}

button.jp-Dialog-button:focus {
  outline: 1px solid var(--jp-brand-color1);
  outline-offset: 4px;
  -moz-outline-radius: 0px;
}

button.jp-Dialog-button:focus::-moz-focus-inner {
  border: 0;
}

.jp-Dialog-header {
  flex: 0 0 auto;
  padding-bottom: 12px;
  font-size: var(--jp-ui-font-size3);
  font-weight: 400;
  color: var(--jp-ui-font-color0);
}

.jp-Dialog-body {
  display: flex;
  flex-direction: column;
  flex: 1 1 auto;
  font-size: var(--jp-ui-font-size1);
  background: var(--jp-layout-color1);
  overflow: auto;
}

.jp-Dialog-footer {
  display: flex;
  flex-direction: row;
  justify-content: flex-end;
  flex: 0 0 auto;
  margin-left: -12px;
  margin-right: -12px;
  padding: 12px;
}

.jp-Dialog-title {
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}

.jp-Dialog-body > .jp-select-wrapper {
  width: 100%;
}

.jp-Dialog-body > button {
  padding: 0px 16px;
}

.jp-Dialog-body > label {
  line-height: 1.4;
  color: var(--jp-ui-font-color0);
}

.jp-Dialog-button.jp-mod-styled:not(:last-child) {
  margin-right: 12px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2016, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-HoverBox {
  position: fixed;
}

.jp-HoverBox.jp-mod-outofview {
  display: none;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-IFrame {
  width: 100%;
  height: 100%;
}

.jp-IFrame > iframe {
  border: none;
}

/*
When drag events occur, `p-mod-override-cursor` is added to the body.
Because iframes steal all cursor events, the following two rules are necessary
to suppress pointer events while resize drags are occurring. There may be a
better solution to this problem.
*/
body.lm-mod-override-cursor .jp-IFrame {
  position: relative;
}

body.lm-mod-override-cursor .jp-IFrame:before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: transparent;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2016, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-MainAreaWidget > :focus {
  outline: none;
}

/**
 * google-material-color v1.2.6
 * https://github.com/danlevan/google-material-color
 */
:root {
  --md-red-50: #ffebee;
  --md-red-100: #ffcdd2;
  --md-red-200: #ef9a9a;
  --md-red-300: #e57373;
  --md-red-400: #ef5350;
  --md-red-500: #f44336;
  --md-red-600: #e53935;
  --md-red-700: #d32f2f;
  --md-red-800: #c62828;
  --md-red-900: #b71c1c;
  --md-red-A100: #ff8a80;
  --md-red-A200: #ff5252;
  --md-red-A400: #ff1744;
  --md-red-A700: #d50000;

  --md-pink-50: #fce4ec;
  --md-pink-100: #f8bbd0;
  --md-pink-200: #f48fb1;
  --md-pink-300: #f06292;
  --md-pink-400: #ec407a;
  --md-pink-500: #e91e63;
  --md-pink-600: #d81b60;
  --md-pink-700: #c2185b;
  --md-pink-800: #ad1457;
  --md-pink-900: #880e4f;
  --md-pink-A100: #ff80ab;
  --md-pink-A200: #ff4081;
  --md-pink-A400: #f50057;
  --md-pink-A700: #c51162;

  --md-purple-50: #f3e5f5;
  --md-purple-100: #e1bee7;
  --md-purple-200: #ce93d8;
  --md-purple-300: #ba68c8;
  --md-purple-400: #ab47bc;
  --md-purple-500: #9c27b0;
  --md-purple-600: #8e24aa;
  --md-purple-700: #7b1fa2;
  --md-purple-800: #6a1b9a;
  --md-purple-900: #4a148c;
  --md-purple-A100: #ea80fc;
  --md-purple-A200: #e040fb;
  --md-purple-A400: #d500f9;
  --md-purple-A700: #aa00ff;

  --md-deep-purple-50: #ede7f6;
  --md-deep-purple-100: #d1c4e9;
  --md-deep-purple-200: #b39ddb;
  --md-deep-purple-300: #9575cd;
  --md-deep-purple-400: #7e57c2;
  --md-deep-purple-500: #673ab7;
  --md-deep-purple-600: #5e35b1;
  --md-deep-purple-700: #512da8;
  --md-deep-purple-800: #4527a0;
  --md-deep-purple-900: #311b92;
  --md-deep-purple-A100: #b388ff;
  --md-deep-purple-A200: #7c4dff;
  --md-deep-purple-A400: #651fff;
  --md-deep-purple-A700: #6200ea;

  --md-indigo-50: #e8eaf6;
  --md-indigo-100: #c5cae9;
  --md-indigo-200: #9fa8da;
  --md-indigo-300: #7986cb;
  --md-indigo-400: #5c6bc0;
  --md-indigo-500: #3f51b5;
  --md-indigo-600: #3949ab;
  --md-indigo-700: #303f9f;
  --md-indigo-800: #283593;
  --md-indigo-900: #1a237e;
  --md-indigo-A100: #8c9eff;
  --md-indigo-A200: #536dfe;
  --md-indigo-A400: #3d5afe;
  --md-indigo-A700: #304ffe;

  --md-blue-50: #e3f2fd;
  --md-blue-100: #bbdefb;
  --md-blue-200: #90caf9;
  --md-blue-300: #64b5f6;
  --md-blue-400: #42a5f5;
  --md-blue-500: #2196f3;
  --md-blue-600: #1e88e5;
  --md-blue-700: #1976d2;
  --md-blue-800: #1565c0;
  --md-blue-900: #0d47a1;
  --md-blue-A100: #82b1ff;
  --md-blue-A200: #448aff;
  --md-blue-A400: #2979ff;
  --md-blue-A700: #2962ff;

  --md-light-blue-50: #e1f5fe;
  --md-light-blue-100: #b3e5fc;
  --md-light-blue-200: #81d4fa;
  --md-light-blue-300: #4fc3f7;
  --md-light-blue-400: #29b6f6;
  --md-light-blue-500: #03a9f4;
  --md-light-blue-600: #039be5;
  --md-light-blue-700: #0288d1;
  --md-light-blue-800: #0277bd;
  --md-light-blue-900: #01579b;
  --md-light-blue-A100: #80d8ff;
  --md-light-blue-A200: #40c4ff;
  --md-light-blue-A400: #00b0ff;
  --md-light-blue-A700: #0091ea;

  --md-cyan-50: #e0f7fa;
  --md-cyan-100: #b2ebf2;
  --md-cyan-200: #80deea;
  --md-cyan-300: #4dd0e1;
  --md-cyan-400: #26c6da;
  --md-cyan-500: #00bcd4;
  --md-cyan-600: #00acc1;
  --md-cyan-700: #0097a7;
  --md-cyan-800: #00838f;
  --md-cyan-900: #006064;
  --md-cyan-A100: #84ffff;
  --md-cyan-A200: #18ffff;
  --md-cyan-A400: #00e5ff;
  --md-cyan-A700: #00b8d4;

  --md-teal-50: #e0f2f1;
  --md-teal-100: #b2dfdb;
  --md-teal-200: #80cbc4;
  --md-teal-300: #4db6ac;
  --md-teal-400: #26a69a;
  --md-teal-500: #009688;
  --md-teal-600: #00897b;
  --md-teal-700: #00796b;
  --md-teal-800: #00695c;
  --md-teal-900: #004d40;
  --md-teal-A100: #a7ffeb;
  --md-teal-A200: #64ffda;
  --md-teal-A400: #1de9b6;
  --md-teal-A700: #00bfa5;

  --md-green-50: #e8f5e9;
  --md-green-100: #c8e6c9;
  --md-green-200: #a5d6a7;
  --md-green-300: #81c784;
  --md-green-400: #66bb6a;
  --md-green-500: #4caf50;
  --md-green-600: #43a047;
  --md-green-700: #388e3c;
  --md-green-800: #2e7d32;
  --md-green-900: #1b5e20;
  --md-green-A100: #b9f6ca;
  --md-green-A200: #69f0ae;
  --md-green-A400: #00e676;
  --md-green-A700: #00c853;

  --md-light-green-50: #f1f8e9;
  --md-light-green-100: #dcedc8;
  --md-light-green-200: #c5e1a5;
  --md-light-green-300: #aed581;
  --md-light-green-400: #9ccc65;
  --md-light-green-500: #8bc34a;
  --md-light-green-600: #7cb342;
  --md-light-green-700: #689f38;
  --md-light-green-800: #558b2f;
  --md-light-green-900: #33691e;
  --md-light-green-A100: #ccff90;
  --md-light-green-A200: #b2ff59;
  --md-light-green-A400: #76ff03;
  --md-light-green-A700: #64dd17;

  --md-lime-50: #f9fbe7;
  --md-lime-100: #f0f4c3;
  --md-lime-200: #e6ee9c;
  --md-lime-300: #dce775;
  --md-lime-400: #d4e157;
  --md-lime-500: #cddc39;
  --md-lime-600: #c0ca33;
  --md-lime-700: #afb42b;
  --md-lime-800: #9e9d24;
  --md-lime-900: #827717;
  --md-lime-A100: #f4ff81;
  --md-lime-A200: #eeff41;
  --md-lime-A400: #c6ff00;
  --md-lime-A700: #aeea00;

  --md-yellow-50: #fffde7;
  --md-yellow-100: #fff9c4;
  --md-yellow-200: #fff59d;
  --md-yellow-300: #fff176;
  --md-yellow-400: #ffee58;
  --md-yellow-500: #ffeb3b;
  --md-yellow-600: #fdd835;
  --md-yellow-700: #fbc02d;
  --md-yellow-800: #f9a825;
  --md-yellow-900: #f57f17;
  --md-yellow-A100: #ffff8d;
  --md-yellow-A200: #ffff00;
  --md-yellow-A400: #ffea00;
  --md-yellow-A700: #ffd600;

  --md-amber-50: #fff8e1;
  --md-amber-100: #ffecb3;
  --md-amber-200: #ffe082;
  --md-amber-300: #ffd54f;
  --md-amber-400: #ffca28;
  --md-amber-500: #ffc107;
  --md-amber-600: #ffb300;
  --md-amber-700: #ffa000;
  --md-amber-800: #ff8f00;
  --md-amber-900: #ff6f00;
  --md-amber-A100: #ffe57f;
  --md-amber-A200: #ffd740;
  --md-amber-A400: #ffc400;
  --md-amber-A700: #ffab00;

  --md-orange-50: #fff3e0;
  --md-orange-100: #ffe0b2;
  --md-orange-200: #ffcc80;
  --md-orange-300: #ffb74d;
  --md-orange-400: #ffa726;
  --md-orange-500: #ff9800;
  --md-orange-600: #fb8c00;
  --md-orange-700: #f57c00;
  --md-orange-800: #ef6c00;
  --md-orange-900: #e65100;
  --md-orange-A100: #ffd180;
  --md-orange-A200: #ffab40;
  --md-orange-A400: #ff9100;
  --md-orange-A700: #ff6d00;

  --md-deep-orange-50: #fbe9e7;
  --md-deep-orange-100: #ffccbc;
  --md-deep-orange-200: #ffab91;
  --md-deep-orange-300: #ff8a65;
  --md-deep-orange-400: #ff7043;
  --md-deep-orange-500: #ff5722;
  --md-deep-orange-600: #f4511e;
  --md-deep-orange-700: #e64a19;
  --md-deep-orange-800: #d84315;
  --md-deep-orange-900: #bf360c;
  --md-deep-orange-A100: #ff9e80;
  --md-deep-orange-A200: #ff6e40;
  --md-deep-orange-A400: #ff3d00;
  --md-deep-orange-A700: #dd2c00;

  --md-brown-50: #efebe9;
  --md-brown-100: #d7ccc8;
  --md-brown-200: #bcaaa4;
  --md-brown-300: #a1887f;
  --md-brown-400: #8d6e63;
  --md-brown-500: #795548;
  --md-brown-600: #6d4c41;
  --md-brown-700: #5d4037;
  --md-brown-800: #4e342e;
  --md-brown-900: #3e2723;

  --md-grey-50: #fafafa;
  --md-grey-100: #f5f5f5;
  --md-grey-200: #eeeeee;
  --md-grey-300: #e0e0e0;
  --md-grey-400: #bdbdbd;
  --md-grey-500: #9e9e9e;
  --md-grey-600: #757575;
  --md-grey-700: #616161;
  --md-grey-800: #424242;
  --md-grey-900: #212121;

  --md-blue-grey-50: #eceff1;
  --md-blue-grey-100: #cfd8dc;
  --md-blue-grey-200: #b0bec5;
  --md-blue-grey-300: #90a4ae;
  --md-blue-grey-400: #78909c;
  --md-blue-grey-500: #607d8b;
  --md-blue-grey-600: #546e7a;
  --md-blue-grey-700: #455a64;
  --md-blue-grey-800: #37474f;
  --md-blue-grey-900: #263238;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2017, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-Spinner {
  position: absolute;
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 10;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  background: var(--jp-layout-color0);
  outline: none;
}

.jp-SpinnerContent {
  font-size: 10px;
  margin: 50px auto;
  text-indent: -9999em;
  width: 3em;
  height: 3em;
  border-radius: 50%;
  background: var(--jp-brand-color3);
  background: linear-gradient(
    to right,
    #f37626 10%,
    rgba(255, 255, 255, 0) 42%
  );
  position: relative;
  animation: load3 1s infinite linear, fadeIn 1s;
}

.jp-SpinnerContent:before {
  width: 50%;
  height: 50%;
  background: #f37626;
  border-radius: 100% 0 0 0;
  position: absolute;
  top: 0;
  left: 0;
  content: '';
}

.jp-SpinnerContent:after {
  background: var(--jp-layout-color0);
  width: 75%;
  height: 75%;
  border-radius: 50%;
  content: '';
  margin: auto;
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
}

@keyframes fadeIn {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}

@keyframes load3 {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2017, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

button.jp-mod-styled {
  font-size: var(--jp-ui-font-size1);
  color: var(--jp-ui-font-color0);
  border: none;
  box-sizing: border-box;
  text-align: center;
  line-height: 32px;
  height: 32px;
  padding: 0px 12px;
  letter-spacing: 0.8px;
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
}

input.jp-mod-styled {
  background: var(--jp-input-background);
  height: 28px;
  box-sizing: border-box;
  border: var(--jp-border-width) solid var(--jp-border-color1);
  padding-left: 7px;
  padding-right: 7px;
  font-size: var(--jp-ui-font-size2);
  color: var(--jp-ui-font-color0);
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
}

input.jp-mod-styled:focus {
  border: var(--jp-border-width) solid var(--md-blue-500);
  box-shadow: inset 0 0 4px var(--md-blue-300);
}

.jp-select-wrapper {
  display: flex;
  position: relative;
  flex-direction: column;
  padding: 1px;
  background-color: var(--jp-layout-color1);
  height: 28px;
  box-sizing: border-box;
  margin-bottom: 12px;
}

.jp-select-wrapper.jp-mod-focused select.jp-mod-styled {
  border: var(--jp-border-width) solid var(--jp-input-active-border-color);
  box-shadow: var(--jp-input-box-shadow);
  background-color: var(--jp-input-active-background);
}

select.jp-mod-styled:hover {
  background-color: var(--jp-layout-color1);
  cursor: pointer;
  color: var(--jp-ui-font-color0);
  background-color: var(--jp-input-hover-background);
  box-shadow: inset 0 0px 1px rgba(0, 0, 0, 0.5);
}

select.jp-mod-styled {
  flex: 1 1 auto;
  height: 32px;
  width: 100%;
  font-size: var(--jp-ui-font-size2);
  background: var(--jp-input-background);
  color: var(--jp-ui-font-color0);
  padding: 0 25px 0 8px;
  border: var(--jp-border-width) solid var(--jp-input-border-color);
  border-radius: 0px;
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2016, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

:root {
  --jp-private-toolbar-height: calc(
    28px + var(--jp-border-width)
  ); /* leave 28px for content */
}

.jp-Toolbar {
  color: var(--jp-ui-font-color1);
  flex: 0 0 auto;
  display: flex;
  flex-direction: row;
  border-bottom: var(--jp-border-width) solid var(--jp-toolbar-border-color);
  box-shadow: var(--jp-toolbar-box-shadow);
  background: var(--jp-toolbar-background);
  min-height: var(--jp-toolbar-micro-height);
  padding: 2px;
  z-index: 1;
}

/* Toolbar items */

.jp-Toolbar > .jp-Toolbar-item.jp-Toolbar-spacer {
  flex-grow: 1;
  flex-shrink: 1;
}

.jp-Toolbar-item.jp-Toolbar-kernelStatus {
  display: inline-block;
  width: 32px;
  background-repeat: no-repeat;
  background-position: center;
  background-size: 16px;
}

.jp-Toolbar > .jp-Toolbar-item {
  flex: 0 0 auto;
  display: flex;
  padding-left: 1px;
  padding-right: 1px;
  font-size: var(--jp-ui-font-size1);
  line-height: var(--jp-private-toolbar-height);
  height: 100%;
}

/* Toolbar buttons */

/* This is the div we use to wrap the react component into a Widget */
div.jp-ToolbarButton {
  color: transparent;
  border: none;
  box-sizing: border-box;
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
  padding: 0px;
  margin: 0px;
}

button.jp-ToolbarButtonComponent {
  background: var(--jp-layout-color1);
  border: none;
  box-sizing: border-box;
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
  padding: 0px 6px;
  margin: 0px;
  height: 24px;
  border-radius: var(--jp-border-radius);
  display: flex;
  align-items: center;
  text-align: center;
  font-size: 14px;
  min-width: unset;
  min-height: unset;
}

button.jp-ToolbarButtonComponent:disabled {
  opacity: 0.4;
}

button.jp-ToolbarButtonComponent span {
  padding: 0px;
  flex: 0 0 auto;
}

button.jp-ToolbarButtonComponent .jp-ToolbarButtonComponent-label {
  font-size: var(--jp-ui-font-size1);
  line-height: 100%;
  padding-left: 2px;
  color: var(--jp-ui-font-color1);
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2017, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* This file was auto-generated by ensurePackage() in @jupyterlab/buildutils */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ body.p-mod-override-cursor *, /* </DEPRECATED> */
body.lm-mod-override-cursor * {
  cursor: inherit !important;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2016, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-JSONEditor {
  display: flex;
  flex-direction: column;
  width: 100%;
}

.jp-JSONEditor-host {
  flex: 1 1 auto;
  border: var(--jp-border-width) solid var(--jp-input-border-color);
  border-radius: 0px;
  background: var(--jp-layout-color0);
  min-height: 50px;
  padding: 1px;
}

.jp-JSONEditor.jp-mod-error .jp-JSONEditor-host {
  border-color: red;
  outline-color: red;
}

.jp-JSONEditor-header {
  display: flex;
  flex: 1 0 auto;
  padding: 0 0 0 12px;
}

.jp-JSONEditor-header label {
  flex: 0 0 auto;
}

.jp-JSONEditor-commitButton {
  height: 16px;
  width: 16px;
  background-size: 18px;
  background-repeat: no-repeat;
  background-position: center;
}

.jp-JSONEditor-host.jp-mod-focused {
  background-color: var(--jp-input-active-background);
  border: 1px solid var(--jp-input-active-border-color);
  box-shadow: var(--jp-input-box-shadow);
}

.jp-Editor.jp-mod-dropTarget {
  border: var(--jp-border-width) solid var(--jp-input-active-border-color);
  box-shadow: var(--jp-input-box-shadow);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* This file was auto-generated by ensurePackage() in @jupyterlab/buildutils */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* BASICS */

.CodeMirror {
  /* Set height, width, borders, and global font properties here */
  font-family: monospace;
  height: 300px;
  color: black;
  direction: ltr;
}

/* PADDING */

.CodeMirror-lines {
  padding: 4px 0; /* Vertical padding around content */
}
.CodeMirror pre.CodeMirror-line,
.CodeMirror pre.CodeMirror-line-like {
  padding: 0 4px; /* Horizontal padding of content */
}

.CodeMirror-scrollbar-filler, .CodeMirror-gutter-filler {
  background-color: white; /* The little square between H and V scrollbars */
}

/* GUTTER */

.CodeMirror-gutters {
  border-right: 1px solid #ddd;
  background-color: #f7f7f7;
  white-space: nowrap;
}
.CodeMirror-linenumbers {}
.CodeMirror-linenumber {
  padding: 0 3px 0 5px;
  min-width: 20px;
  text-align: right;
  color: #999;
  white-space: nowrap;
}

.CodeMirror-guttermarker { color: black; }
.CodeMirror-guttermarker-subtle { color: #999; }

/* CURSOR */

.CodeMirror-cursor {
  border-left: 1px solid black;
  border-right: none;
  width: 0;
}
/* Shown when moving in bi-directional text */
.CodeMirror div.CodeMirror-secondarycursor {
  border-left: 1px solid silver;
}
.cm-fat-cursor .CodeMirror-cursor {
  width: auto;
  border: 0 !important;
  background: #7e7;
}
.cm-fat-cursor div.CodeMirror-cursors {
  z-index: 1;
}
.cm-fat-cursor-mark {
  background-color: rgba(20, 255, 20, 0.5);
  -webkit-animation: blink 1.06s steps(1) infinite;
  -moz-animation: blink 1.06s steps(1) infinite;
  animation: blink 1.06s steps(1) infinite;
}
.cm-animate-fat-cursor {
  width: auto;
  border: 0;
  -webkit-animation: blink 1.06s steps(1) infinite;
  -moz-animation: blink 1.06s steps(1) infinite;
  animation: blink 1.06s steps(1) infinite;
  background-color: #7e7;
}
@-moz-keyframes blink {
  0% {}
  50% { background-color: transparent; }
  100% {}
}
@-webkit-keyframes blink {
  0% {}
  50% { background-color: transparent; }
  100% {}
}
@keyframes blink {
  0% {}
  50% { background-color: transparent; }
  100% {}
}

/* Can style cursor different in overwrite (non-insert) mode */
.CodeMirror-overwrite .CodeMirror-cursor {}

.cm-tab { display: inline-block; text-decoration: inherit; }

.CodeMirror-rulers {
  position: absolute;
  left: 0; right: 0; top: -50px; bottom: 0;
  overflow: hidden;
}
.CodeMirror-ruler {
  border-left: 1px solid #ccc;
  top: 0; bottom: 0;
  position: absolute;
}

/* DEFAULT THEME */

.cm-s-default .cm-header {color: blue;}
.cm-s-default .cm-quote {color: #090;}
.cm-negative {color: #d44;}
.cm-positive {color: #292;}
.cm-header, .cm-strong {font-weight: bold;}
.cm-em {font-style: italic;}
.cm-link {text-decoration: underline;}
.cm-strikethrough {text-decoration: line-through;}

.cm-s-default .cm-keyword {color: #708;}
.cm-s-default .cm-atom {color: #219;}
.cm-s-default .cm-number {color: #164;}
.cm-s-default .cm-def {color: #00f;}
.cm-s-default .cm-variable,
.cm-s-default .cm-punctuation,
.cm-s-default .cm-property,
.cm-s-default .cm-operator {}
.cm-s-default .cm-variable-2 {color: #05a;}
.cm-s-default .cm-variable-3, .cm-s-default .cm-type {color: #085;}
.cm-s-default .cm-comment {color: #a50;}
.cm-s-default .cm-string {color: #a11;}
.cm-s-default .cm-string-2 {color: #f50;}
.cm-s-default .cm-meta {color: #555;}
.cm-s-default .cm-qualifier {color: #555;}
.cm-s-default .cm-builtin {color: #30a;}
.cm-s-default .cm-bracket {color: #997;}
.cm-s-default .cm-tag {color: #170;}
.cm-s-default .cm-attribute {color: #00c;}
.cm-s-default .cm-hr {color: #999;}
.cm-s-default .cm-link {color: #00c;}

.cm-s-default .cm-error {color: #f00;}
.cm-invalidchar {color: #f00;}

.CodeMirror-composing { border-bottom: 2px solid; }

/* Default styles for common addons */

div.CodeMirror span.CodeMirror-matchingbracket {color: #0b0;}
div.CodeMirror span.CodeMirror-nonmatchingbracket {color: #a22;}
.CodeMirror-matchingtag { background: rgba(255, 150, 0, .3); }
.CodeMirror-activeline-background {background: #e8f2ff;}

/* STOP */

/* The rest of this file contains styles related to the mechanics of
   the editor. You probably shouldn't touch them. */

.CodeMirror {
  position: relative;
  overflow: hidden;
  background: white;
}

.CodeMirror-scroll {
  overflow: scroll !important; /* Things will break if this is overridden */
  /* 30px is the magic margin used to hide the element's real scrollbars */
  /* See overflow: hidden in .CodeMirror */
  margin-bottom: -30px; margin-right: -30px;
  padding-bottom: 30px;
  height: 100%;
  outline: none; /* Prevent dragging from highlighting the element */
  position: relative;
}
.CodeMirror-sizer {
  position: relative;
  border-right: 30px solid transparent;
}

/* The fake, visible scrollbars. Used to force redraw during scrolling
   before actual scrolling happens, thus preventing shaking and
   flickering artifacts. */
.CodeMirror-vscrollbar, .CodeMirror-hscrollbar, .CodeMirror-scrollbar-filler, .CodeMirror-gutter-filler {
  position: absolute;
  z-index: 6;
  display: none;
}
.CodeMirror-vscrollbar {
  right: 0; top: 0;
  overflow-x: hidden;
  overflow-y: scroll;
}
.CodeMirror-hscrollbar {
  bottom: 0; left: 0;
  overflow-y: hidden;
  overflow-x: scroll;
}
.CodeMirror-scrollbar-filler {
  right: 0; bottom: 0;
}
.CodeMirror-gutter-filler {
  left: 0; bottom: 0;
}

.CodeMirror-gutters {
  position: absolute; left: 0; top: 0;
  min-height: 100%;
  z-index: 3;
}
.CodeMirror-gutter {
  white-space: normal;
  height: 100%;
  display: inline-block;
  vertical-align: top;
  margin-bottom: -30px;
}
.CodeMirror-gutter-wrapper {
  position: absolute;
  z-index: 4;
  background: none !important;
  border: none !important;
}
.CodeMirror-gutter-background {
  position: absolute;
  top: 0; bottom: 0;
  z-index: 4;
}
.CodeMirror-gutter-elt {
  position: absolute;
  cursor: default;
  z-index: 4;
}
.CodeMirror-gutter-wrapper ::selection { background-color: transparent }
.CodeMirror-gutter-wrapper ::-moz-selection { background-color: transparent }

.CodeMirror-lines {
  cursor: text;
  min-height: 1px; /* prevents collapsing before first draw */
}
.CodeMirror pre.CodeMirror-line,
.CodeMirror pre.CodeMirror-line-like {
  /* Reset some styles that the rest of the page might have set */
  -moz-border-radius: 0; -webkit-border-radius: 0; border-radius: 0;
  border-width: 0;
  background: transparent;
  font-family: inherit;
  font-size: inherit;
  margin: 0;
  white-space: pre;
  word-wrap: normal;
  line-height: inherit;
  color: inherit;
  z-index: 2;
  position: relative;
  overflow: visible;
  -webkit-tap-highlight-color: transparent;
  -webkit-font-variant-ligatures: contextual;
  font-variant-ligatures: contextual;
}
.CodeMirror-wrap pre.CodeMirror-line,
.CodeMirror-wrap pre.CodeMirror-line-like {
  word-wrap: break-word;
  white-space: pre-wrap;
  word-break: normal;
}

.CodeMirror-linebackground {
  position: absolute;
  left: 0; right: 0; top: 0; bottom: 0;
  z-index: 0;
}

.CodeMirror-linewidget {
  position: relative;
  z-index: 2;
  padding: 0.1px; /* Force widget margins to stay inside of the container */
}

.CodeMirror-widget {}

.CodeMirror-rtl pre { direction: rtl; }

.CodeMirror-code {
  outline: none;
}

/* Force content-box sizing for the elements where we expect it */
.CodeMirror-scroll,
.CodeMirror-sizer,
.CodeMirror-gutter,
.CodeMirror-gutters,
.CodeMirror-linenumber {
  -moz-box-sizing: content-box;
  box-sizing: content-box;
}

.CodeMirror-measure {
  position: absolute;
  width: 100%;
  height: 0;
  overflow: hidden;
  visibility: hidden;
}

.CodeMirror-cursor {
  position: absolute;
  pointer-events: none;
}
.CodeMirror-measure pre { position: static; }

div.CodeMirror-cursors {
  visibility: hidden;
  position: relative;
  z-index: 3;
}
div.CodeMirror-dragcursors {
  visibility: visible;
}

.CodeMirror-focused div.CodeMirror-cursors {
  visibility: visible;
}

.CodeMirror-selected { background: #d9d9d9; }
.CodeMirror-focused .CodeMirror-selected { background: #d7d4f0; }
.CodeMirror-crosshair { cursor: crosshair; }
.CodeMirror-line::selection, .CodeMirror-line > span::selection, .CodeMirror-line > span > span::selection { background: #d7d4f0; }
.CodeMirror-line::-moz-selection, .CodeMirror-line > span::-moz-selection, .CodeMirror-line > span > span::-moz-selection { background: #d7d4f0; }

.cm-searching {
  background-color: #ffa;
  background-color: rgba(255, 255, 0, .4);
}

/* Used to force a border model for a node */
.cm-force-border { padding-right: .1px; }

@media print {
  /* Hide the cursor when printing */
  .CodeMirror div.CodeMirror-cursors {
    visibility: hidden;
  }
}

/* See issue #2901 */
.cm-tab-wrap-hack:after { content: ''; }

/* Help users use markselection to safely style text background */
span.CodeMirror-selectedtext { background: none; }

.CodeMirror-dialog {
  position: absolute;
  left: 0; right: 0;
  background: inherit;
  z-index: 15;
  padding: .1em .8em;
  overflow: hidden;
  color: inherit;
}

.CodeMirror-dialog-top {
  border-bottom: 1px solid #eee;
  top: 0;
}

.CodeMirror-dialog-bottom {
  border-top: 1px solid #eee;
  bottom: 0;
}

.CodeMirror-dialog input {
  border: none;
  outline: none;
  background: transparent;
  width: 20em;
  color: inherit;
  font-family: monospace;
}

.CodeMirror-dialog button {
  font-size: 70%;
}

.CodeMirror-foldmarker {
  color: blue;
  text-shadow: #b9f 1px 1px 2px, #b9f -1px -1px 2px, #b9f 1px -1px 2px, #b9f -1px 1px 2px;
  font-family: arial;
  line-height: .3;
  cursor: pointer;
}
.CodeMirror-foldgutter {
  width: .7em;
}
.CodeMirror-foldgutter-open,
.CodeMirror-foldgutter-folded {
  cursor: pointer;
}
.CodeMirror-foldgutter-open:after {
  content: "\25BE";
}
.CodeMirror-foldgutter-folded:after {
  content: "\25B8";
}

/*
  Name:       material
  Author:     Mattia Astorino (http://github.com/equinusocio)
  Website:    https://material-theme.site/
*/

.cm-s-material.CodeMirror {
  background-color: #263238;
  color: #EEFFFF;
}

.cm-s-material .CodeMirror-gutters {
  background: #263238;
  color: #546E7A;
  border: none;
}

.cm-s-material .CodeMirror-guttermarker,
.cm-s-material .CodeMirror-guttermarker-subtle,
.cm-s-material .CodeMirror-linenumber {
  color: #546E7A;
}

.cm-s-material .CodeMirror-cursor {
  border-left: 1px solid #FFCC00;
}

.cm-s-material div.CodeMirror-selected {
  background: rgba(128, 203, 196, 0.2);
}

.cm-s-material.CodeMirror-focused div.CodeMirror-selected {
  background: rgba(128, 203, 196, 0.2);
}

.cm-s-material .CodeMirror-line::selection,
.cm-s-material .CodeMirror-line>span::selection,
.cm-s-material .CodeMirror-line>span>span::selection {
  background: rgba(128, 203, 196, 0.2);
}

.cm-s-material .CodeMirror-line::-moz-selection,
.cm-s-material .CodeMirror-line>span::-moz-selection,
.cm-s-material .CodeMirror-line>span>span::-moz-selection {
  background: rgba(128, 203, 196, 0.2);
}

.cm-s-material .CodeMirror-activeline-background {
  background: rgba(0, 0, 0, 0.5);
}

.cm-s-material .cm-keyword {
  color: #C792EA;
}

.cm-s-material .cm-operator {
  color: #89DDFF;
}

.cm-s-material .cm-variable-2 {
  color: #EEFFFF;
}

.cm-s-material .cm-variable-3,
.cm-s-material .cm-type {
  color: #f07178;
}

.cm-s-material .cm-builtin {
  color: #FFCB6B;
}

.cm-s-material .cm-atom {
  color: #F78C6C;
}

.cm-s-material .cm-number {
  color: #FF5370;
}

.cm-s-material .cm-def {
  color: #82AAFF;
}

.cm-s-material .cm-string {
  color: #C3E88D;
}

.cm-s-material .cm-string-2 {
  color: #f07178;
}

.cm-s-material .cm-comment {
  color: #546E7A;
}

.cm-s-material .cm-variable {
  color: #f07178;
}

.cm-s-material .cm-tag {
  color: #FF5370;
}

.cm-s-material .cm-meta {
  color: #FFCB6B;
}

.cm-s-material .cm-attribute {
  color: #C792EA;
}

.cm-s-material .cm-property {
  color: #C792EA;
}

.cm-s-material .cm-qualifier {
  color: #DECB6B;
}

.cm-s-material .cm-variable-3,
.cm-s-material .cm-type {
  color: #DECB6B;
}


.cm-s-material .cm-error {
  color: rgba(255, 255, 255, 1.0);
  background-color: #FF5370;
}

.cm-s-material .CodeMirror-matchingbracket {
  text-decoration: underline;
  color: white !important;
}
/**
 * "
 *  Using Zenburn color palette from the Emacs Zenburn Theme
 *  https://github.com/bbatsov/zenburn-emacs/blob/master/zenburn-theme.el
 *
 *  Also using parts of https://github.com/xavi/coderay-lighttable-theme
 * "
 * From: https://github.com/wisenomad/zenburn-lighttable-theme/blob/master/zenburn.css
 */

.cm-s-zenburn .CodeMirror-gutters { background: #3f3f3f !important; }
.cm-s-zenburn .CodeMirror-foldgutter-open, .CodeMirror-foldgutter-folded { color: #999; }
.cm-s-zenburn .CodeMirror-cursor { border-left: 1px solid white; }
.cm-s-zenburn { background-color: #3f3f3f; color: #dcdccc; }
.cm-s-zenburn span.cm-builtin { color: #dcdccc; font-weight: bold; }
.cm-s-zenburn span.cm-comment { color: #7f9f7f; }
.cm-s-zenburn span.cm-keyword { color: #f0dfaf; font-weight: bold; }
.cm-s-zenburn span.cm-atom { color: #bfebbf; }
.cm-s-zenburn span.cm-def { color: #dcdccc; }
.cm-s-zenburn span.cm-variable { color: #dfaf8f; }
.cm-s-zenburn span.cm-variable-2 { color: #dcdccc; }
.cm-s-zenburn span.cm-string { color: #cc9393; }
.cm-s-zenburn span.cm-string-2 { color: #cc9393; }
.cm-s-zenburn span.cm-number { color: #dcdccc; }
.cm-s-zenburn span.cm-tag { color: #93e0e3; }
.cm-s-zenburn span.cm-property { color: #dfaf8f; }
.cm-s-zenburn span.cm-attribute { color: #dfaf8f; }
.cm-s-zenburn span.cm-qualifier { color: #7cb8bb; }
.cm-s-zenburn span.cm-meta { color: #f0dfaf; }
.cm-s-zenburn span.cm-header { color: #f0efd0; }
.cm-s-zenburn span.cm-operator { color: #f0efd0; }
.cm-s-zenburn span.CodeMirror-matchingbracket { box-sizing: border-box; background: transparent; border-bottom: 1px solid; }
.cm-s-zenburn span.CodeMirror-nonmatchingbracket { border-bottom: 1px solid; background: none; }
.cm-s-zenburn .CodeMirror-activeline { background: #000000; }
.cm-s-zenburn .CodeMirror-activeline-background { background: #000000; }
.cm-s-zenburn div.CodeMirror-selected { background: #545454; }
.cm-s-zenburn .CodeMirror-focused div.CodeMirror-selected { background: #4f4f4f; }

.cm-s-abcdef.CodeMirror { background: #0f0f0f; color: #defdef; }
.cm-s-abcdef div.CodeMirror-selected { background: #515151; }
.cm-s-abcdef .CodeMirror-line::selection, .cm-s-abcdef .CodeMirror-line > span::selection, .cm-s-abcdef .CodeMirror-line > span > span::selection { background: rgba(56, 56, 56, 0.99); }
.cm-s-abcdef .CodeMirror-line::-moz-selection, .cm-s-abcdef .CodeMirror-line > span::-moz-selection, .cm-s-abcdef .CodeMirror-line > span > span::-moz-selection { background: rgba(56, 56, 56, 0.99); }
.cm-s-abcdef .CodeMirror-gutters { background: #555; border-right: 2px solid #314151; }
.cm-s-abcdef .CodeMirror-guttermarker { color: #222; }
.cm-s-abcdef .CodeMirror-guttermarker-subtle { color: azure; }
.cm-s-abcdef .CodeMirror-linenumber { color: #FFFFFF; }
.cm-s-abcdef .CodeMirror-cursor { border-left: 1px solid #00FF00; }

.cm-s-abcdef span.cm-keyword { color: darkgoldenrod; font-weight: bold; }
.cm-s-abcdef span.cm-atom { color: #77F; }
.cm-s-abcdef span.cm-number { color: violet; }
.cm-s-abcdef span.cm-def { color: #fffabc; }
.cm-s-abcdef span.cm-variable { color: #abcdef; }
.cm-s-abcdef span.cm-variable-2 { color: #cacbcc; }
.cm-s-abcdef span.cm-variable-3, .cm-s-abcdef span.cm-type { color: #def; }
.cm-s-abcdef span.cm-property { color: #fedcba; }
.cm-s-abcdef span.cm-operator { color: #ff0; }
.cm-s-abcdef span.cm-comment { color: #7a7b7c; font-style: italic;}
.cm-s-abcdef span.cm-string { color: #2b4; }
.cm-s-abcdef span.cm-meta { color: #C9F; }
.cm-s-abcdef span.cm-qualifier { color: #FFF700; }
.cm-s-abcdef span.cm-builtin { color: #30aabc; }
.cm-s-abcdef span.cm-bracket { color: #8a8a8a; }
.cm-s-abcdef span.cm-tag { color: #FFDD44; }
.cm-s-abcdef span.cm-attribute { color: #DDFF00; }
.cm-s-abcdef span.cm-error { color: #FF0000; }
.cm-s-abcdef span.cm-header { color: aquamarine; font-weight: bold; }
.cm-s-abcdef span.cm-link { color: blueviolet; }

.cm-s-abcdef .CodeMirror-activeline-background { background: #314151; }

/*

    Name:       Base16 Default Light
    Author:     Chris Kempson (http://chriskempson.com)

    CodeMirror template by Jan T. Sott (https://github.com/idleberg/base16-codemirror)
    Original Base16 color scheme by Chris Kempson (https://github.com/chriskempson/base16)

*/

.cm-s-base16-light.CodeMirror { background: #f5f5f5; color: #202020; }
.cm-s-base16-light div.CodeMirror-selected { background: #e0e0e0; }
.cm-s-base16-light .CodeMirror-line::selection, .cm-s-base16-light .CodeMirror-line > span::selection, .cm-s-base16-light .CodeMirror-line > span > span::selection { background: #e0e0e0; }
.cm-s-base16-light .CodeMirror-line::-moz-selection, .cm-s-base16-light .CodeMirror-line > span::-moz-selection, .cm-s-base16-light .CodeMirror-line > span > span::-moz-selection { background: #e0e0e0; }
.cm-s-base16-light .CodeMirror-gutters { background: #f5f5f5; border-right: 0px; }
.cm-s-base16-light .CodeMirror-guttermarker { color: #ac4142; }
.cm-s-base16-light .CodeMirror-guttermarker-subtle { color: #b0b0b0; }
.cm-s-base16-light .CodeMirror-linenumber { color: #b0b0b0; }
.cm-s-base16-light .CodeMirror-cursor { border-left: 1px solid #505050; }

.cm-s-base16-light span.cm-comment { color: #8f5536; }
.cm-s-base16-light span.cm-atom { color: #aa759f; }
.cm-s-base16-light span.cm-number { color: #aa759f; }

.cm-s-base16-light span.cm-property, .cm-s-base16-light span.cm-attribute { color: #90a959; }
.cm-s-base16-light span.cm-keyword { color: #ac4142; }
.cm-s-base16-light span.cm-string { color: #f4bf75; }

.cm-s-base16-light span.cm-variable { color: #90a959; }
.cm-s-base16-light span.cm-variable-2 { color: #6a9fb5; }
.cm-s-base16-light span.cm-def { color: #d28445; }
.cm-s-base16-light span.cm-bracket { color: #202020; }
.cm-s-base16-light span.cm-tag { color: #ac4142; }
.cm-s-base16-light span.cm-link { color: #aa759f; }
.cm-s-base16-light span.cm-error { background: #ac4142; color: #505050; }

.cm-s-base16-light .CodeMirror-activeline-background { background: #DDDCDC; }
.cm-s-base16-light .CodeMirror-matchingbracket { color: #f5f5f5 !important; background-color: #6A9FB5 !important}

/*

    Name:       Base16 Default Dark
    Author:     Chris Kempson (http://chriskempson.com)

    CodeMirror template by Jan T. Sott (https://github.com/idleberg/base16-codemirror)
    Original Base16 color scheme by Chris Kempson (https://github.com/chriskempson/base16)

*/

.cm-s-base16-dark.CodeMirror { background: #151515; color: #e0e0e0; }
.cm-s-base16-dark div.CodeMirror-selected { background: #303030; }
.cm-s-base16-dark .CodeMirror-line::selection, .cm-s-base16-dark .CodeMirror-line > span::selection, .cm-s-base16-dark .CodeMirror-line > span > span::selection { background: rgba(48, 48, 48, .99); }
.cm-s-base16-dark .CodeMirror-line::-moz-selection, .cm-s-base16-dark .CodeMirror-line > span::-moz-selection, .cm-s-base16-dark .CodeMirror-line > span > span::-moz-selection { background: rgba(48, 48, 48, .99); }
.cm-s-base16-dark .CodeMirror-gutters { background: #151515; border-right: 0px; }
.cm-s-base16-dark .CodeMirror-guttermarker { color: #ac4142; }
.cm-s-base16-dark .CodeMirror-guttermarker-subtle { color: #505050; }
.cm-s-base16-dark .CodeMirror-linenumber { color: #505050; }
.cm-s-base16-dark .CodeMirror-cursor { border-left: 1px solid #b0b0b0; }

.cm-s-base16-dark span.cm-comment { color: #8f5536; }
.cm-s-base16-dark span.cm-atom { color: #aa759f; }
.cm-s-base16-dark span.cm-number { color: #aa759f; }

.cm-s-base16-dark span.cm-property, .cm-s-base16-dark span.cm-attribute { color: #90a959; }
.cm-s-base16-dark span.cm-keyword { color: #ac4142; }
.cm-s-base16-dark span.cm-string { color: #f4bf75; }

.cm-s-base16-dark span.cm-variable { color: #90a959; }
.cm-s-base16-dark span.cm-variable-2 { color: #6a9fb5; }
.cm-s-base16-dark span.cm-def { color: #d28445; }
.cm-s-base16-dark span.cm-bracket { color: #e0e0e0; }
.cm-s-base16-dark span.cm-tag { color: #ac4142; }
.cm-s-base16-dark span.cm-link { color: #aa759f; }
.cm-s-base16-dark span.cm-error { background: #ac4142; color: #b0b0b0; }

.cm-s-base16-dark .CodeMirror-activeline-background { background: #202020; }
.cm-s-base16-dark .CodeMirror-matchingbracket { text-decoration: underline; color: white !important; }

/*

    Name:       dracula
    Author:     Michael Kaminsky (http://github.com/mkaminsky11)

    Original dracula color scheme by Zeno Rocha (https://github.com/zenorocha/dracula-theme)

*/


.cm-s-dracula.CodeMirror, .cm-s-dracula .CodeMirror-gutters {
  background-color: #282a36 !important;
  color: #f8f8f2 !important;
  border: none;
}
.cm-s-dracula .CodeMirror-gutters { color: #282a36; }
.cm-s-dracula .CodeMirror-cursor { border-left: solid thin #f8f8f0; }
.cm-s-dracula .CodeMirror-linenumber { color: #6D8A88; }
.cm-s-dracula .CodeMirror-selected { background: rgba(255, 255, 255, 0.10); }
.cm-s-dracula .CodeMirror-line::selection, .cm-s-dracula .CodeMirror-line > span::selection, .cm-s-dracula .CodeMirror-line > span > span::selection { background: rgba(255, 255, 255, 0.10); }
.cm-s-dracula .CodeMirror-line::-moz-selection, .cm-s-dracula .CodeMirror-line > span::-moz-selection, .cm-s-dracula .CodeMirror-line > span > span::-moz-selection { background: rgba(255, 255, 255, 0.10); }
.cm-s-dracula span.cm-comment { color: #6272a4; }
.cm-s-dracula span.cm-string, .cm-s-dracula span.cm-string-2 { color: #f1fa8c; }
.cm-s-dracula span.cm-number { color: #bd93f9; }
.cm-s-dracula span.cm-variable { color: #50fa7b; }
.cm-s-dracula span.cm-variable-2 { color: white; }
.cm-s-dracula span.cm-def { color: #50fa7b; }
.cm-s-dracula span.cm-operator { color: #ff79c6; }
.cm-s-dracula span.cm-keyword { color: #ff79c6; }
.cm-s-dracula span.cm-atom { color: #bd93f9; }
.cm-s-dracula span.cm-meta { color: #f8f8f2; }
.cm-s-dracula span.cm-tag { color: #ff79c6; }
.cm-s-dracula span.cm-attribute { color: #50fa7b; }
.cm-s-dracula span.cm-qualifier { color: #50fa7b; }
.cm-s-dracula span.cm-property { color: #66d9ef; }
.cm-s-dracula span.cm-builtin { color: #50fa7b; }
.cm-s-dracula span.cm-variable-3, .cm-s-dracula span.cm-type { color: #ffb86c; }

.cm-s-dracula .CodeMirror-activeline-background { background: rgba(255,255,255,0.1); }
.cm-s-dracula .CodeMirror-matchingbracket { text-decoration: underline; color: white !important; }

/*

    Name:       Hopscotch
    Author:     Jan T. Sott

    CodeMirror template by Jan T. Sott (https://github.com/idleberg/base16-codemirror)
    Original Base16 color scheme by Chris Kempson (https://github.com/chriskempson/base16)

*/

.cm-s-hopscotch.CodeMirror {background: #322931; color: #d5d3d5;}
.cm-s-hopscotch div.CodeMirror-selected {background: #433b42 !important;}
.cm-s-hopscotch .CodeMirror-gutters {background: #322931; border-right: 0px;}
.cm-s-hopscotch .CodeMirror-linenumber {color: #797379;}
.cm-s-hopscotch .CodeMirror-cursor {border-left: 1px solid #989498 !important;}

.cm-s-hopscotch span.cm-comment {color: #b33508;}
.cm-s-hopscotch span.cm-atom {color: #c85e7c;}
.cm-s-hopscotch span.cm-number {color: #c85e7c;}

.cm-s-hopscotch span.cm-property, .cm-s-hopscotch span.cm-attribute {color: #8fc13e;}
.cm-s-hopscotch span.cm-keyword {color: #dd464c;}
.cm-s-hopscotch span.cm-string {color: #fdcc59;}

.cm-s-hopscotch span.cm-variable {color: #8fc13e;}
.cm-s-hopscotch span.cm-variable-2 {color: #1290bf;}
.cm-s-hopscotch span.cm-def {color: #fd8b19;}
.cm-s-hopscotch span.cm-error {background: #dd464c; color: #989498;}
.cm-s-hopscotch span.cm-bracket {color: #d5d3d5;}
.cm-s-hopscotch span.cm-tag {color: #dd464c;}
.cm-s-hopscotch span.cm-link {color: #c85e7c;}

.cm-s-hopscotch .CodeMirror-matchingbracket { text-decoration: underline; color: white !important;}
.cm-s-hopscotch .CodeMirror-activeline-background { background: #302020; }

/****************************************************************/
/*   Based on mbonaci's Brackets mbo theme                      */
/*   https://github.com/mbonaci/global/blob/master/Mbo.tmTheme  */
/*   Create your own: http://tmtheme-editor.herokuapp.com       */
/****************************************************************/

.cm-s-mbo.CodeMirror { background: #2c2c2c; color: #ffffec; }
.cm-s-mbo div.CodeMirror-selected { background: #716C62; }
.cm-s-mbo .CodeMirror-line::selection, .cm-s-mbo .CodeMirror-line > span::selection, .cm-s-mbo .CodeMirror-line > span > span::selection { background: rgba(113, 108, 98, .99); }
.cm-s-mbo .CodeMirror-line::-moz-selection, .cm-s-mbo .CodeMirror-line > span::-moz-selection, .cm-s-mbo .CodeMirror-line > span > span::-moz-selection { background: rgba(113, 108, 98, .99); }
.cm-s-mbo .CodeMirror-gutters { background: #4e4e4e; border-right: 0px; }
.cm-s-mbo .CodeMirror-guttermarker { color: white; }
.cm-s-mbo .CodeMirror-guttermarker-subtle { color: grey; }
.cm-s-mbo .CodeMirror-linenumber { color: #dadada; }
.cm-s-mbo .CodeMirror-cursor { border-left: 1px solid #ffffec; }

.cm-s-mbo span.cm-comment { color: #95958a; }
.cm-s-mbo span.cm-atom { color: #00a8c6; }
.cm-s-mbo span.cm-number { color: #00a8c6; }

.cm-s-mbo span.cm-property, .cm-s-mbo span.cm-attribute { color: #9ddfe9; }
.cm-s-mbo span.cm-keyword { color: #ffb928; }
.cm-s-mbo span.cm-string { color: #ffcf6c; }
.cm-s-mbo span.cm-string.cm-property { color: #ffffec; }

.cm-s-mbo span.cm-variable { color: #ffffec; }
.cm-s-mbo span.cm-variable-2 { color: #00a8c6; }
.cm-s-mbo span.cm-def { color: #ffffec; }
.cm-s-mbo span.cm-bracket { color: #fffffc; font-weight: bold; }
.cm-s-mbo span.cm-tag { color: #9ddfe9; }
.cm-s-mbo span.cm-link { color: #f54b07; }
.cm-s-mbo span.cm-error { border-bottom: #636363; color: #ffffec; }
.cm-s-mbo span.cm-qualifier { color: #ffffec; }

.cm-s-mbo .CodeMirror-activeline-background { background: #494b41; }
.cm-s-mbo .CodeMirror-matchingbracket { color: #ffb928 !important; }
.cm-s-mbo .CodeMirror-matchingtag { background: rgba(255, 255, 255, .37); }

/*
  MDN-LIKE Theme - Mozilla
  Ported to CodeMirror by Peter Kroon <plakroon@gmail.com>
  Report bugs/issues here: https://github.com/codemirror/CodeMirror/issues
  GitHub: @peterkroon

  The mdn-like theme is inspired on the displayed code examples at: https://developer.mozilla.org/en-US/docs/Web/CSS/animation

*/
.cm-s-mdn-like.CodeMirror { color: #999; background-color: #fff; }
.cm-s-mdn-like div.CodeMirror-selected { background: #cfc; }
.cm-s-mdn-like .CodeMirror-line::selection, .cm-s-mdn-like .CodeMirror-line > span::selection, .cm-s-mdn-like .CodeMirror-line > span > span::selection { background: #cfc; }
.cm-s-mdn-like .CodeMirror-line::-moz-selection, .cm-s-mdn-like .CodeMirror-line > span::-moz-selection, .cm-s-mdn-like .CodeMirror-line > span > span::-moz-selection { background: #cfc; }

.cm-s-mdn-like .CodeMirror-gutters { background: #f8f8f8; border-left: 6px solid rgba(0,83,159,0.65); color: #333; }
.cm-s-mdn-like .CodeMirror-linenumber { color: #aaa; padding-left: 8px; }
.cm-s-mdn-like .CodeMirror-cursor { border-left: 2px solid #222; }

.cm-s-mdn-like .cm-keyword { color: #6262FF; }
.cm-s-mdn-like .cm-atom { color: #F90; }
.cm-s-mdn-like .cm-number { color:  #ca7841; }
.cm-s-mdn-like .cm-def { color: #8DA6CE; }
.cm-s-mdn-like span.cm-variable-2, .cm-s-mdn-like span.cm-tag { color: #690; }
.cm-s-mdn-like span.cm-variable-3, .cm-s-mdn-like span.cm-def, .cm-s-mdn-like span.cm-type { color: #07a; }

.cm-s-mdn-like .cm-variable { color: #07a; }
.cm-s-mdn-like .cm-property { color: #905; }
.cm-s-mdn-like .cm-qualifier { color: #690; }

.cm-s-mdn-like .cm-operator { color: #cda869; }
.cm-s-mdn-like .cm-comment { color:#777; font-weight:normal; }
.cm-s-mdn-like .cm-string { color:#07a; font-style:italic; }
.cm-s-mdn-like .cm-string-2 { color:#bd6b18; } /*?*/
.cm-s-mdn-like .cm-meta { color: #000; } /*?*/
.cm-s-mdn-like .cm-builtin { color: #9B7536; } /*?*/
.cm-s-mdn-like .cm-tag { color: #997643; }
.cm-s-mdn-like .cm-attribute { color: #d6bb6d; } /*?*/
.cm-s-mdn-like .cm-header { color: #FF6400; }
.cm-s-mdn-like .cm-hr { color: #AEAEAE; }
.cm-s-mdn-like .cm-link { color:#ad9361; font-style:italic; text-decoration:none; }
.cm-s-mdn-like .cm-error { border-bottom: 1px solid red; }

div.cm-s-mdn-like .CodeMirror-activeline-background { background: #efefff; }
div.cm-s-mdn-like span.CodeMirror-matchingbracket { outline:1px solid grey; color: inherit; }

.cm-s-mdn-like.CodeMirror { background-image: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAFcAAAAyCAYAAAAp8UeFAAAHvklEQVR42s2b63bcNgyEQZCSHCdt2vd/0tWF7I+Q6XgMXiTtuvU5Pl57ZQKkKHzEAOtF5KeIJBGJ8uvL599FRFREZhFx8DeXv8trn68RuGaC8TRfo3SNp9dlDDHedyLyTUTeRWStXKPZrjtpZxaRw5hPqozRs1N8/enzIiQRWcCgy4MUA0f+XWliDhyL8Lfyvx7ei/Ae3iQFHyw7U/59pQVIMEEPEz0G7XiwdRjzSfC3UTtz9vchIntxvry5iMgfIhJoEflOz2CQr3F5h/HfeFe+GTdLaKcu9L8LTeQb/R/7GgbsfKedyNdoHsN31uRPWrfZ5wsj/NzzRQHuToIdU3ahwnsKPxXCjJITuOsi7XLc7SG/v5GdALs7wf8JjTFiB5+QvTEfRyGOfX3Lrx8wxyQi3sNq46O7QahQiCsRFgqddjBouVEHOKDgXAQHD9gJCr5sMKkEdjwsarG/ww3BMHBU7OBjXnzdyY7SfCxf5/z6ATccrwlKuwC/jhznnPF4CgVzhhVf4xp2EixcBActO75iZ8/fM9zAs2OMzKdslgXWJ9XG8PQoOAMA5fGcsvORgv0doBXyHrCwfLJAOwo71QLNkb8n2Pl6EWiR7OCibtkPaz4Kc/0NNAze2gju3zOwekALDaCFPI5vjPFmgGY5AZqyGEvH1x7QfIb8YtxMnA/b+QQ0aQDAwc6JMFg8CbQZ4qoYEEHbRwNojuK3EHwd7VALSgq+MNDKzfT58T8qdpADrgW0GmgcAS1lhzztJmkAzcPNOQbsWEALBDSlMKUG0Eq4CLAQWvEVQ9WU57gZJwZtgPO3r9oBTQ9WO8TjqXINx8R0EYpiZEUWOF3FxkbJkgU9B2f41YBrIj5ZfsQa0M5kTgiAAqM3ShXLgu8XMqcrQBvJ0CL5pnTsfMB13oB8athpAq2XOQmcGmoACCLydx7nToa23ATaSIY2ichfOdPTGxlasXMLaL0MLZAOwAKIM+y8CmicobGdCcbbK9DzN+yYGVoNNI5iUKTMyYOjPse4A8SM1MmcXgU0toOq1yO/v8FOxlASyc7TgeYaAMBJHcY1CcCwGI/TK4AmDbDyKYBBtFUkRwto8gygiQEaByFgJ00BH2M8JWwQS1nafDXQCidWyOI8AcjDCSjCLk8ngObuAm3JAHAdubAmOaK06V8MNEsKPJOhobSprwQa6gD7DclRQdqcwL4zxqgBrQcabUiBLclRDKAlWp+etPkBaNMA0AKlrHwTdEByZAA4GM+SNluSY6wAzcMNewxmgig5Ks0nkrSpBvSaQHMdKTBAnLojOdYyGpQ254602ZILPdTD1hdlggdIm74jbTp8vDwF5ZYUeLWGJpWsh6XNyXgcYwVoJQTEhhTYkxzZjiU5npU2TaB979TQehlaAVq4kaGpiPwwwLkYUuBbQwocyQTv1tA0+1UFWoJF3iv1oq+qoSk8EQdJmwHkziIF7oOZk14EGitibAdjLYYK78H5vZOhtWpoI0ATGHs0Q8OMb4Ey+2bU2UYztCtA0wFAs7TplGLRVQCcqaFdGSPCeTI1QNIC52iWNzof6Uib7xjEp07mNNoUYmVosVItHrHzRlLgBn9LFyRHaQCtVUMbtTNhoXWiTOO9k/V8BdAc1Oq0ArSQs6/5SU0hckNy9NnXqQY0PGYo5dWJ7nINaN6o958FWin27aBaWRka1r5myvLOAm0j30eBJqCxHLReVclxhxOEN2JfDWjxBtAC7MIH1fVaGdoOp4qJYDgKtKPSFNID2gSnGldrCqkFZ+5UeQXQBIRrSwocbdZYQT/2LwRahBPBXoHrB8nxaGROST62DKUbQOMMzZIC9abkuELfQzQALWTnDNAm8KHWFOJgJ5+SHIvTPcmx1xQyZRhNL5Qci689aXMEaN/uNIWkEwDAvFpOZmgsBaaGnbs1NPa1Jm32gBZAIh1pCtG7TSH4aE0y1uVY4uqoFPisGlpP2rSA5qTecWn5agK6BzSpgAyD+wFaqhnYoSZ1Vwr8CmlTQbrcO3ZaX0NAEyMbYaAlyquFoLKK3SPby9CeVUPThrSJmkCAE0CrKUQadi4DrdSlWhmah0YL9z9vClH59YGbHx1J8VZTyAjQepJjmXwAKTDQI3omc3p1U4gDUf6RfcdYfrUp5ClAi2J3Ba6UOXGo+K+bQrjjssitG2SJzshaLwMtXgRagUNpYYoVkMSBLM+9GGiJZMvduG6DRZ4qc04DMPtQQxOjEtACmhO7K1AbNbQDEggZyJwscFpAGwENhoBeUwh3bWolhe8BTYVKxQEWrSUn/uhcM5KhvUu/+eQu0Lzhi+VrK0PrZZNDQKs9cpYUuFYgMVpD4/NxenJTiMCNqdUEUf1qZWjppLT5qSkkUZbCwkbZMSuVnu80hfSkzRbQeqCZSAh6huR4VtoM2gHAlLf72smuWgE+VV7XpE25Ab2WFDgyhnSuKbs4GuGzCjR+tIoUuMFg3kgcWKLTwRqanJQ2W00hAsenfaApRC42hbCvK1SlE0HtE9BGgneJO+ELamitD1YjjOYnNYVcraGhtKkW0EqVVeDx733I2NH581k1NNxNLG0i0IJ8/NjVaOZ0tYZ2Vtr0Xv7tPV3hkWp9EFkgS/J0vosngTaSoaG06WHi+xObQkaAdlbanP8B2+2l0f90LmUAAAAASUVORK5CYII=); }

/*

    Name:       seti
    Author:     Michael Kaminsky (http://github.com/mkaminsky11)

    Original seti color scheme by Jesse Weed (https://github.com/jesseweed/seti-syntax)

*/


.cm-s-seti.CodeMirror {
  background-color: #151718 !important;
  color: #CFD2D1 !important;
  border: none;
}
.cm-s-seti .CodeMirror-gutters {
  color: #404b53;
  background-color: #0E1112;
  border: none;
}
.cm-s-seti .CodeMirror-cursor { border-left: solid thin #f8f8f0; }
.cm-s-seti .CodeMirror-linenumber { color: #6D8A88; }
.cm-s-seti.CodeMirror-focused div.CodeMirror-selected { background: rgba(255, 255, 255, 0.10); }
.cm-s-seti .CodeMirror-line::selection, .cm-s-seti .CodeMirror-line > span::selection, .cm-s-seti .CodeMirror-line > span > span::selection { background: rgba(255, 255, 255, 0.10); }
.cm-s-seti .CodeMirror-line::-moz-selection, .cm-s-seti .CodeMirror-line > span::-moz-selection, .cm-s-seti .CodeMirror-line > span > span::-moz-selection { background: rgba(255, 255, 255, 0.10); }
.cm-s-seti span.cm-comment { color: #41535b; }
.cm-s-seti span.cm-string, .cm-s-seti span.cm-string-2 { color: #55b5db; }
.cm-s-seti span.cm-number { color: #cd3f45; }
.cm-s-seti span.cm-variable { color: #55b5db; }
.cm-s-seti span.cm-variable-2 { color: #a074c4; }
.cm-s-seti span.cm-def { color: #55b5db; }
.cm-s-seti span.cm-keyword { color: #ff79c6; }
.cm-s-seti span.cm-operator { color: #9fca56; }
.cm-s-seti span.cm-keyword { color: #e6cd69; }
.cm-s-seti span.cm-atom { color: #cd3f45; }
.cm-s-seti span.cm-meta { color: #55b5db; }
.cm-s-seti span.cm-tag { color: #55b5db; }
.cm-s-seti span.cm-attribute { color: #9fca56; }
.cm-s-seti span.cm-qualifier { color: #9fca56; }
.cm-s-seti span.cm-property { color: #a074c4; }
.cm-s-seti span.cm-variable-3, .cm-s-seti span.cm-type { color: #9fca56; }
.cm-s-seti span.cm-builtin { color: #9fca56; }
.cm-s-seti .CodeMirror-activeline-background { background: #101213; }
.cm-s-seti .CodeMirror-matchingbracket { text-decoration: underline; color: white !important; }

/*
Solarized theme for code-mirror
http://ethanschoonover.com/solarized
*/

/*
Solarized color palette
http://ethanschoonover.com/solarized/img/solarized-palette.png
*/

.solarized.base03 { color: #002b36; }
.solarized.base02 { color: #073642; }
.solarized.base01 { color: #586e75; }
.solarized.base00 { color: #657b83; }
.solarized.base0 { color: #839496; }
.solarized.base1 { color: #93a1a1; }
.solarized.base2 { color: #eee8d5; }
.solarized.base3  { color: #fdf6e3; }
.solarized.solar-yellow  { color: #b58900; }
.solarized.solar-orange  { color: #cb4b16; }
.solarized.solar-red { color: #dc322f; }
.solarized.solar-magenta { color: #d33682; }
.solarized.solar-violet  { color: #6c71c4; }
.solarized.solar-blue { color: #268bd2; }
.solarized.solar-cyan { color: #2aa198; }
.solarized.solar-green { color: #859900; }

/* Color scheme for code-mirror */

.cm-s-solarized {
  line-height: 1.45em;
  color-profile: sRGB;
  rendering-intent: auto;
}
.cm-s-solarized.cm-s-dark {
  color: #839496;
  background-color: #002b36;
  text-shadow: #002b36 0 1px;
}
.cm-s-solarized.cm-s-light {
  background-color: #fdf6e3;
  color: #657b83;
  text-shadow: #eee8d5 0 1px;
}

.cm-s-solarized .CodeMirror-widget {
  text-shadow: none;
}

.cm-s-solarized .cm-header { color: #586e75; }
.cm-s-solarized .cm-quote { color: #93a1a1; }

.cm-s-solarized .cm-keyword { color: #cb4b16; }
.cm-s-solarized .cm-atom { color: #d33682; }
.cm-s-solarized .cm-number { color: #d33682; }
.cm-s-solarized .cm-def { color: #2aa198; }

.cm-s-solarized .cm-variable { color: #839496; }
.cm-s-solarized .cm-variable-2 { color: #b58900; }
.cm-s-solarized .cm-variable-3, .cm-s-solarized .cm-type { color: #6c71c4; }

.cm-s-solarized .cm-property { color: #2aa198; }
.cm-s-solarized .cm-operator { color: #6c71c4; }

.cm-s-solarized .cm-comment { color: #586e75; font-style:italic; }

.cm-s-solarized .cm-string { color: #859900; }
.cm-s-solarized .cm-string-2 { color: #b58900; }

.cm-s-solarized .cm-meta { color: #859900; }
.cm-s-solarized .cm-qualifier { color: #b58900; }
.cm-s-solarized .cm-builtin { color: #d33682; }
.cm-s-solarized .cm-bracket { color: #cb4b16; }
.cm-s-solarized .CodeMirror-matchingbracket { color: #859900; }
.cm-s-solarized .CodeMirror-nonmatchingbracket { color: #dc322f; }
.cm-s-solarized .cm-tag { color: #93a1a1; }
.cm-s-solarized .cm-attribute { color: #2aa198; }
.cm-s-solarized .cm-hr {
  color: transparent;
  border-top: 1px solid #586e75;
  display: block;
}
.cm-s-solarized .cm-link { color: #93a1a1; cursor: pointer; }
.cm-s-solarized .cm-special { color: #6c71c4; }
.cm-s-solarized .cm-em {
  color: #999;
  text-decoration: underline;
  text-decoration-style: dotted;
}
.cm-s-solarized .cm-error,
.cm-s-solarized .cm-invalidchar {
  color: #586e75;
  border-bottom: 1px dotted #dc322f;
}

.cm-s-solarized.cm-s-dark div.CodeMirror-selected { background: #073642; }
.cm-s-solarized.cm-s-dark.CodeMirror ::selection { background: rgba(7, 54, 66, 0.99); }
.cm-s-solarized.cm-s-dark .CodeMirror-line::-moz-selection, .cm-s-dark .CodeMirror-line > span::-moz-selection, .cm-s-dark .CodeMirror-line > span > span::-moz-selection { background: rgba(7, 54, 66, 0.99); }

.cm-s-solarized.cm-s-light div.CodeMirror-selected { background: #eee8d5; }
.cm-s-solarized.cm-s-light .CodeMirror-line::selection, .cm-s-light .CodeMirror-line > span::selection, .cm-s-light .CodeMirror-line > span > span::selection { background: #eee8d5; }
.cm-s-solarized.cm-s-light .CodeMirror-line::-moz-selection, .cm-s-ligh .CodeMirror-line > span::-moz-selection, .cm-s-ligh .CodeMirror-line > span > span::-moz-selection { background: #eee8d5; }

/* Editor styling */



/* Little shadow on the view-port of the buffer view */
.cm-s-solarized.CodeMirror {
  -moz-box-shadow: inset 7px 0 12px -6px #000;
  -webkit-box-shadow: inset 7px 0 12px -6px #000;
  box-shadow: inset 7px 0 12px -6px #000;
}

/* Remove gutter border */
.cm-s-solarized .CodeMirror-gutters {
  border-right: 0;
}

/* Gutter colors and line number styling based of color scheme (dark / light) */

/* Dark */
.cm-s-solarized.cm-s-dark .CodeMirror-gutters {
  background-color: #073642;
}

.cm-s-solarized.cm-s-dark .CodeMirror-linenumber {
  color: #586e75;
  text-shadow: #021014 0 -1px;
}

/* Light */
.cm-s-solarized.cm-s-light .CodeMirror-gutters {
  background-color: #eee8d5;
}

.cm-s-solarized.cm-s-light .CodeMirror-linenumber {
  color: #839496;
}

/* Common */
.cm-s-solarized .CodeMirror-linenumber {
  padding: 0 5px;
}
.cm-s-solarized .CodeMirror-guttermarker-subtle { color: #586e75; }
.cm-s-solarized.cm-s-dark .CodeMirror-guttermarker { color: #ddd; }
.cm-s-solarized.cm-s-light .CodeMirror-guttermarker { color: #cb4b16; }

.cm-s-solarized .CodeMirror-gutter .CodeMirror-gutter-text {
  color: #586e75;
}

/* Cursor */
.cm-s-solarized .CodeMirror-cursor { border-left: 1px solid #819090; }

/* Fat cursor */
.cm-s-solarized.cm-s-light.cm-fat-cursor .CodeMirror-cursor { background: #77ee77; }
.cm-s-solarized.cm-s-light .cm-animate-fat-cursor { background-color: #77ee77; }
.cm-s-solarized.cm-s-dark.cm-fat-cursor .CodeMirror-cursor { background: #586e75; }
.cm-s-solarized.cm-s-dark .cm-animate-fat-cursor { background-color: #586e75; }

/* Active line */
.cm-s-solarized.cm-s-dark .CodeMirror-activeline-background {
  background: rgba(255, 255, 255, 0.06);
}
.cm-s-solarized.cm-s-light .CodeMirror-activeline-background {
  background: rgba(0, 0, 0, 0.06);
}

.cm-s-the-matrix.CodeMirror { background: #000000; color: #00FF00; }
.cm-s-the-matrix div.CodeMirror-selected { background: #2D2D2D; }
.cm-s-the-matrix .CodeMirror-line::selection, .cm-s-the-matrix .CodeMirror-line > span::selection, .cm-s-the-matrix .CodeMirror-line > span > span::selection { background: rgba(45, 45, 45, 0.99); }
.cm-s-the-matrix .CodeMirror-line::-moz-selection, .cm-s-the-matrix .CodeMirror-line > span::-moz-selection, .cm-s-the-matrix .CodeMirror-line > span > span::-moz-selection { background: rgba(45, 45, 45, 0.99); }
.cm-s-the-matrix .CodeMirror-gutters { background: #060; border-right: 2px solid #00FF00; }
.cm-s-the-matrix .CodeMirror-guttermarker { color: #0f0; }
.cm-s-the-matrix .CodeMirror-guttermarker-subtle { color: white; }
.cm-s-the-matrix .CodeMirror-linenumber { color: #FFFFFF; }
.cm-s-the-matrix .CodeMirror-cursor { border-left: 1px solid #00FF00; }

.cm-s-the-matrix span.cm-keyword { color: #008803; font-weight: bold; }
.cm-s-the-matrix span.cm-atom { color: #3FF; }
.cm-s-the-matrix span.cm-number { color: #FFB94F; }
.cm-s-the-matrix span.cm-def { color: #99C; }
.cm-s-the-matrix span.cm-variable { color: #F6C; }
.cm-s-the-matrix span.cm-variable-2 { color: #C6F; }
.cm-s-the-matrix span.cm-variable-3, .cm-s-the-matrix span.cm-type { color: #96F; }
.cm-s-the-matrix span.cm-property { color: #62FFA0; }
.cm-s-the-matrix span.cm-operator { color: #999; }
.cm-s-the-matrix span.cm-comment { color: #CCCCCC; }
.cm-s-the-matrix span.cm-string { color: #39C; }
.cm-s-the-matrix span.cm-meta { color: #C9F; }
.cm-s-the-matrix span.cm-qualifier { color: #FFF700; }
.cm-s-the-matrix span.cm-builtin { color: #30a; }
.cm-s-the-matrix span.cm-bracket { color: #cc7; }
.cm-s-the-matrix span.cm-tag { color: #FFBD40; }
.cm-s-the-matrix span.cm-attribute { color: #FFF700; }
.cm-s-the-matrix span.cm-error { color: #FF0000; }

.cm-s-the-matrix .CodeMirror-activeline-background { background: #040; }

/*
Copyright (C) 2011 by MarkLogic Corporation
Author: Mike Brevoort <mike@brevoort.com>

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
*/
.cm-s-xq-light span.cm-keyword { line-height: 1em; font-weight: bold; color: #5A5CAD; }
.cm-s-xq-light span.cm-atom { color: #6C8CD5; }
.cm-s-xq-light span.cm-number { color: #164; }
.cm-s-xq-light span.cm-def { text-decoration:underline; }
.cm-s-xq-light span.cm-variable { color: black; }
.cm-s-xq-light span.cm-variable-2 { color:black; }
.cm-s-xq-light span.cm-variable-3, .cm-s-xq-light span.cm-type { color: black; }
.cm-s-xq-light span.cm-property {}
.cm-s-xq-light span.cm-operator {}
.cm-s-xq-light span.cm-comment { color: #0080FF; font-style: italic; }
.cm-s-xq-light span.cm-string { color: red; }
.cm-s-xq-light span.cm-meta { color: yellow; }
.cm-s-xq-light span.cm-qualifier { color: grey; }
.cm-s-xq-light span.cm-builtin { color: #7EA656; }
.cm-s-xq-light span.cm-bracket { color: #cc7; }
.cm-s-xq-light span.cm-tag { color: #3F7F7F; }
.cm-s-xq-light span.cm-attribute { color: #7F007F; }
.cm-s-xq-light span.cm-error { color: #f00; }

.cm-s-xq-light .CodeMirror-activeline-background { background: #e8f2ff; }
.cm-s-xq-light .CodeMirror-matchingbracket { outline:1px solid grey;color:black !important;background:yellow; }

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.CodeMirror {
  line-height: var(--jp-code-line-height);
  font-size: var(--jp-code-font-size);
  font-family: var(--jp-code-font-family);
  border: 0;
  border-radius: 0;
  height: auto;
  /* Changed to auto to autogrow */
}

.CodeMirror pre {
  padding: 0 var(--jp-code-padding);
}

.jp-CodeMirrorEditor[data-type='inline'] .CodeMirror-dialog {
  background-color: var(--jp-layout-color0);
  color: var(--jp-content-font-color1);
}

/* This causes https://github.com/jupyter/jupyterlab/issues/522 */
/* May not cause it not because we changed it! */
.CodeMirror-lines {
  padding: var(--jp-code-padding) 0;
}

.CodeMirror-linenumber {
  padding: 0 8px;
}

.jp-CodeMirrorEditor-static {
  margin: var(--jp-code-padding);
}

.jp-CodeMirrorEditor,
.jp-CodeMirrorEditor-static {
  cursor: text;
}

.jp-CodeMirrorEditor[data-type='inline'] .CodeMirror-cursor {
  border-left: var(--jp-code-cursor-width0) solid var(--jp-editor-cursor-color);
}

/* When zoomed out 67% and 33% on a screen of 1440 width x 900 height */
@media screen and (min-width: 2138px) and (max-width: 4319px) {
  .jp-CodeMirrorEditor[data-type='inline'] .CodeMirror-cursor {
    border-left: var(--jp-code-cursor-width1) solid
      var(--jp-editor-cursor-color);
  }
}

/* When zoomed out less than 33% */
@media screen and (min-width: 4320px) {
  .jp-CodeMirrorEditor[data-type='inline'] .CodeMirror-cursor {
    border-left: var(--jp-code-cursor-width2) solid
      var(--jp-editor-cursor-color);
  }
}

.CodeMirror.jp-mod-readOnly .CodeMirror-cursor {
  display: none;
}

.CodeMirror-gutters {
  border-right: 1px solid var(--jp-border-color2);
  background-color: var(--jp-layout-color0);
}

.jp-CollaboratorCursor {
  border-left: 5px solid transparent;
  border-right: 5px solid transparent;
  border-top: none;
  border-bottom: 3px solid;
  background-clip: content-box;
  margin-left: -5px;
  margin-right: -5px;
}

.CodeMirror-selectedtext.cm-searching {
  background-color: var(--jp-search-selected-match-background-color) !important;
  color: var(--jp-search-selected-match-color) !important;
}

.cm-searching {
  background-color: var(
    --jp-search-unselected-match-background-color
  ) !important;
  color: var(--jp-search-unselected-match-color) !important;
}

.CodeMirror-focused .CodeMirror-selected {
  background-color: var(--jp-editor-selected-focused-background);
}

.CodeMirror-selected {
  background-color: var(--jp-editor-selected-background);
}

.jp-CollaboratorCursor-hover {
  position: absolute;
  z-index: 1;
  transform: translateX(-50%);
  color: white;
  border-radius: 3px;
  padding-left: 4px;
  padding-right: 4px;
  padding-top: 1px;
  padding-bottom: 1px;
  text-align: center;
  font-size: var(--jp-ui-font-size1);
  white-space: nowrap;
}

.jp-CodeMirror-ruler {
  border-left: 1px dashed var(--jp-border-color2);
}

/**
 * Here is our jupyter theme for CodeMirror syntax highlighting
 * This is used in our marked.js syntax highlighting and CodeMirror itself
 * The string "jupyter" is set in ../codemirror/widget.DEFAULT_CODEMIRROR_THEME
 * This came from the classic notebook, which came form highlight.js/GitHub
 */

/**
 * CodeMirror themes are handling the background/color in this way. This works
 * fine for CodeMirror editors outside the notebook, but the notebook styles
 * these things differently.
 */
.CodeMirror.cm-s-jupyter {
  background: var(--jp-layout-color0);
  color: var(--jp-content-font-color1);
}

/* In the notebook, we want this styling to be handled by its container */
.jp-CodeConsole .CodeMirror.cm-s-jupyter,
.jp-Notebook .CodeMirror.cm-s-jupyter {
  background: transparent;
}

.cm-s-jupyter .CodeMirror-cursor {
  border-left: var(--jp-code-cursor-width0) solid var(--jp-editor-cursor-color);
}
.cm-s-jupyter span.cm-keyword {
  color: var(--jp-mirror-editor-keyword-color);
  font-weight: bold;
}
.cm-s-jupyter span.cm-atom {
  color: var(--jp-mirror-editor-atom-color);
}
.cm-s-jupyter span.cm-number {
  color: var(--jp-mirror-editor-number-color);
}
.cm-s-jupyter span.cm-def {
  color: var(--jp-mirror-editor-def-color);
}
.cm-s-jupyter span.cm-variable {
  color: var(--jp-mirror-editor-variable-color);
}
.cm-s-jupyter span.cm-variable-2 {
  color: var(--jp-mirror-editor-variable-2-color);
}
.cm-s-jupyter span.cm-variable-3 {
  color: var(--jp-mirror-editor-variable-3-color);
}
.cm-s-jupyter span.cm-punctuation {
  color: var(--jp-mirror-editor-punctuation-color);
}
.cm-s-jupyter span.cm-property {
  color: var(--jp-mirror-editor-property-color);
}
.cm-s-jupyter span.cm-operator {
  color: var(--jp-mirror-editor-operator-color);
  font-weight: bold;
}
.cm-s-jupyter span.cm-comment {
  color: var(--jp-mirror-editor-comment-color);
  font-style: italic;
}
.cm-s-jupyter span.cm-string {
  color: var(--jp-mirror-editor-string-color);
}
.cm-s-jupyter span.cm-string-2 {
  color: var(--jp-mirror-editor-string-2-color);
}
.cm-s-jupyter span.cm-meta {
  color: var(--jp-mirror-editor-meta-color);
}
.cm-s-jupyter span.cm-qualifier {
  color: var(--jp-mirror-editor-qualifier-color);
}
.cm-s-jupyter span.cm-builtin {
  color: var(--jp-mirror-editor-builtin-color);
}
.cm-s-jupyter span.cm-bracket {
  color: var(--jp-mirror-editor-bracket-color);
}
.cm-s-jupyter span.cm-tag {
  color: var(--jp-mirror-editor-tag-color);
}
.cm-s-jupyter span.cm-attribute {
  color: var(--jp-mirror-editor-attribute-color);
}
.cm-s-jupyter span.cm-header {
  color: var(--jp-mirror-editor-header-color);
}
.cm-s-jupyter span.cm-quote {
  color: var(--jp-mirror-editor-quote-color);
}
.cm-s-jupyter span.cm-link {
  color: var(--jp-mirror-editor-link-color);
}
.cm-s-jupyter span.cm-error {
  color: var(--jp-mirror-editor-error-color);
}
.cm-s-jupyter span.cm-hr {
  color: #999;
}

.cm-s-jupyter span.cm-tab {
  background: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADAAAAAMCAYAAAAkuj5RAAAAAXNSR0IArs4c6QAAAGFJREFUSMft1LsRQFAQheHPowAKoACx3IgEKtaEHujDjORSgWTH/ZOdnZOcM/sgk/kFFWY0qV8foQwS4MKBCS3qR6ixBJvElOobYAtivseIE120FaowJPN75GMu8j/LfMwNjh4HUpwg4LUAAAAASUVORK5CYII=);
  background-position: right;
  background-repeat: no-repeat;
}

.cm-s-jupyter .CodeMirror-activeline-background,
.cm-s-jupyter .CodeMirror-gutter {
  background-color: var(--jp-layout-color2);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* This file was auto-generated by ensurePackage() in @jupyterlab/buildutils */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| RenderedText
|----------------------------------------------------------------------------*/

.jp-RenderedText {
  text-align: left;
  padding-left: var(--jp-code-padding);
  line-height: var(--jp-code-line-height);
  font-family: var(--jp-code-font-family);
}

.jp-RenderedText pre,
.jp-RenderedJavaScript pre,
.jp-RenderedHTMLCommon pre {
  color: var(--jp-content-font-color1);
  font-size: var(--jp-code-font-size);
  border: none;
  margin: 0px;
  padding: 0px;
  line-height: normal;
}

.jp-RenderedText pre a:link {
  text-decoration: none;
  color: var(--jp-content-link-color);
}
.jp-RenderedText pre a:hover {
  text-decoration: underline;
  color: var(--jp-content-link-color);
}
.jp-RenderedText pre a:visited {
  text-decoration: none;
  color: var(--jp-content-link-color);
}

/* console foregrounds and backgrounds */
.jp-RenderedText pre .ansi-black-fg {
  color: #3e424d;
}
.jp-RenderedText pre .ansi-red-fg {
  color: #e75c58;
}
.jp-RenderedText pre .ansi-green-fg {
  color: #00a250;
}
.jp-RenderedText pre .ansi-yellow-fg {
  color: #ddb62b;
}
.jp-RenderedText pre .ansi-blue-fg {
  color: #208ffb;
}
.jp-RenderedText pre .ansi-magenta-fg {
  color: #d160c4;
}
.jp-RenderedText pre .ansi-cyan-fg {
  color: #60c6c8;
}
.jp-RenderedText pre .ansi-white-fg {
  color: #c5c1b4;
}

.jp-RenderedText pre .ansi-black-bg {
  background-color: #3e424d;
}
.jp-RenderedText pre .ansi-red-bg {
  background-color: #e75c58;
}
.jp-RenderedText pre .ansi-green-bg {
  background-color: #00a250;
}
.jp-RenderedText pre .ansi-yellow-bg {
  background-color: #ddb62b;
}
.jp-RenderedText pre .ansi-blue-bg {
  background-color: #208ffb;
}
.jp-RenderedText pre .ansi-magenta-bg {
  background-color: #d160c4;
}
.jp-RenderedText pre .ansi-cyan-bg {
  background-color: #60c6c8;
}
.jp-RenderedText pre .ansi-white-bg {
  background-color: #c5c1b4;
}

.jp-RenderedText pre .ansi-black-intense-fg {
  color: #282c36;
}
.jp-RenderedText pre .ansi-red-intense-fg {
  color: #b22b31;
}
.jp-RenderedText pre .ansi-green-intense-fg {
  color: #007427;
}
.jp-RenderedText pre .ansi-yellow-intense-fg {
  color: #b27d12;
}
.jp-RenderedText pre .ansi-blue-intense-fg {
  color: #0065ca;
}
.jp-RenderedText pre .ansi-magenta-intense-fg {
  color: #a03196;
}
.jp-RenderedText pre .ansi-cyan-intense-fg {
  color: #258f8f;
}
.jp-RenderedText pre .ansi-white-intense-fg {
  color: #a1a6b2;
}

.jp-RenderedText pre .ansi-black-intense-bg {
  background-color: #282c36;
}
.jp-RenderedText pre .ansi-red-intense-bg {
  background-color: #b22b31;
}
.jp-RenderedText pre .ansi-green-intense-bg {
  background-color: #007427;
}
.jp-RenderedText pre .ansi-yellow-intense-bg {
  background-color: #b27d12;
}
.jp-RenderedText pre .ansi-blue-intense-bg {
  background-color: #0065ca;
}
.jp-RenderedText pre .ansi-magenta-intense-bg {
  background-color: #a03196;
}
.jp-RenderedText pre .ansi-cyan-intense-bg {
  background-color: #258f8f;
}
.jp-RenderedText pre .ansi-white-intense-bg {
  background-color: #a1a6b2;
}

.jp-RenderedText pre .ansi-default-inverse-fg {
  color: var(--jp-ui-inverse-font-color0);
}
.jp-RenderedText pre .ansi-default-inverse-bg {
  background-color: var(--jp-inverse-layout-color0);
}

.jp-RenderedText pre .ansi-bold {
  font-weight: bold;
}
.jp-RenderedText pre .ansi-underline {
  text-decoration: underline;
}

.jp-RenderedText[data-mime-type='application/vnd.jupyter.stderr'] {
  background: var(--jp-rendermime-error-background);
  padding-top: var(--jp-code-padding);
}

/*-----------------------------------------------------------------------------
| RenderedLatex
|----------------------------------------------------------------------------*/

.jp-RenderedLatex {
  color: var(--jp-content-font-color1);
  font-size: var(--jp-content-font-size1);
  line-height: var(--jp-content-line-height);
}

/* Left-justify outputs.*/
.jp-OutputArea-output.jp-RenderedLatex {
  padding: var(--jp-code-padding);
  text-align: left;
}

/*-----------------------------------------------------------------------------
| RenderedHTML
|----------------------------------------------------------------------------*/

.jp-RenderedHTMLCommon {
  color: var(--jp-content-font-color1);
  font-family: var(--jp-content-font-family);
  font-size: var(--jp-content-font-size1);
  line-height: var(--jp-content-line-height);
  /* Give a bit more R padding on Markdown text to keep line lengths reasonable */
  padding-right: 20px;
}

.jp-RenderedHTMLCommon em {
  font-style: italic;
}

.jp-RenderedHTMLCommon strong {
  font-weight: bold;
}

.jp-RenderedHTMLCommon u {
  text-decoration: underline;
}

.jp-RenderedHTMLCommon a:link {
  text-decoration: none;
  color: var(--jp-content-link-color);
}

.jp-RenderedHTMLCommon a:hover {
  text-decoration: underline;
  color: var(--jp-content-link-color);
}

.jp-RenderedHTMLCommon a:visited {
  text-decoration: none;
  color: var(--jp-content-link-color);
}

/* Headings */

.jp-RenderedHTMLCommon h1,
.jp-RenderedHTMLCommon h2,
.jp-RenderedHTMLCommon h3,
.jp-RenderedHTMLCommon h4,
.jp-RenderedHTMLCommon h5,
.jp-RenderedHTMLCommon h6 {
  line-height: var(--jp-content-heading-line-height);
  font-weight: var(--jp-content-heading-font-weight);
  font-style: normal;
  margin: var(--jp-content-heading-margin-top) 0
    var(--jp-content-heading-margin-bottom) 0;
}

.jp-RenderedHTMLCommon h1:first-child,
.jp-RenderedHTMLCommon h2:first-child,
.jp-RenderedHTMLCommon h3:first-child,
.jp-RenderedHTMLCommon h4:first-child,
.jp-RenderedHTMLCommon h5:first-child,
.jp-RenderedHTMLCommon h6:first-child {
  margin-top: calc(0.5 * var(--jp-content-heading-margin-top));
}

.jp-RenderedHTMLCommon h1:last-child,
.jp-RenderedHTMLCommon h2:last-child,
.jp-RenderedHTMLCommon h3:last-child,
.jp-RenderedHTMLCommon h4:last-child,
.jp-RenderedHTMLCommon h5:last-child,
.jp-RenderedHTMLCommon h6:last-child {
  margin-bottom: calc(0.5 * var(--jp-content-heading-margin-bottom));
}

.jp-RenderedHTMLCommon h1 {
  font-size: var(--jp-content-font-size5);
}

.jp-RenderedHTMLCommon h2 {
  font-size: var(--jp-content-font-size4);
}

.jp-RenderedHTMLCommon h3 {
  font-size: var(--jp-content-font-size3);
}

.jp-RenderedHTMLCommon h4 {
  font-size: var(--jp-content-font-size2);
}

.jp-RenderedHTMLCommon h5 {
  font-size: var(--jp-content-font-size1);
}

.jp-RenderedHTMLCommon h6 {
  font-size: var(--jp-content-font-size0);
}

/* Lists */

.jp-RenderedHTMLCommon ul:not(.list-inline),
.jp-RenderedHTMLCommon ol:not(.list-inline) {
  padding-left: 2em;
}

.jp-RenderedHTMLCommon ul {
  list-style: disc;
}

.jp-RenderedHTMLCommon ul ul {
  list-style: square;
}

.jp-RenderedHTMLCommon ul ul ul {
  list-style: circle;
}

.jp-RenderedHTMLCommon ol {
  list-style: decimal;
}

.jp-RenderedHTMLCommon ol ol {
  list-style: upper-alpha;
}

.jp-RenderedHTMLCommon ol ol ol {
  list-style: lower-alpha;
}

.jp-RenderedHTMLCommon ol ol ol ol {
  list-style: lower-roman;
}

.jp-RenderedHTMLCommon ol ol ol ol ol {
  list-style: decimal;
}

.jp-RenderedHTMLCommon ol,
.jp-RenderedHTMLCommon ul {
  margin-bottom: 1em;
}

.jp-RenderedHTMLCommon ul ul,
.jp-RenderedHTMLCommon ul ol,
.jp-RenderedHTMLCommon ol ul,
.jp-RenderedHTMLCommon ol ol {
  margin-bottom: 0em;
}

.jp-RenderedHTMLCommon hr {
  color: var(--jp-border-color2);
  background-color: var(--jp-border-color1);
  margin-top: 1em;
  margin-bottom: 1em;
}

.jp-RenderedHTMLCommon > pre {
  margin: 1.5em 2em;
}

.jp-RenderedHTMLCommon pre,
.jp-RenderedHTMLCommon code {
  border: 0;
  background-color: var(--jp-layout-color0);
  color: var(--jp-content-font-color1);
  font-family: var(--jp-code-font-family);
  font-size: inherit;
  line-height: var(--jp-code-line-height);
  padding: 0;
  white-space: pre-wrap;
}

.jp-RenderedHTMLCommon :not(pre) > code {
  background-color: var(--jp-layout-color2);
  padding: 1px 5px;
}

/* Tables */

.jp-RenderedHTMLCommon table {
  border-collapse: collapse;
  border-spacing: 0;
  border: none;
  color: var(--jp-ui-font-color1);
  font-size: 12px;
  table-layout: fixed;
  margin-left: auto;
  margin-right: auto;
}

.jp-RenderedHTMLCommon thead {
  border-bottom: var(--jp-border-width) solid var(--jp-border-color1);
  vertical-align: bottom;
}

.jp-RenderedHTMLCommon td,
.jp-RenderedHTMLCommon th,
.jp-RenderedHTMLCommon tr {
  vertical-align: middle;
  padding: 0.5em 0.5em;
  line-height: normal;
  white-space: normal;
  max-width: none;
  border: none;
}

.jp-RenderedMarkdown.jp-RenderedHTMLCommon td,
.jp-RenderedMarkdown.jp-RenderedHTMLCommon th {
  max-width: none;
}

:not(.jp-RenderedMarkdown).jp-RenderedHTMLCommon td,
:not(.jp-RenderedMarkdown).jp-RenderedHTMLCommon th,
:not(.jp-RenderedMarkdown).jp-RenderedHTMLCommon tr {
  text-align: right;
}

.jp-RenderedHTMLCommon th {
  font-weight: bold;
}

.jp-RenderedHTMLCommon tbody tr:nth-child(odd) {
  background: var(--jp-layout-color0);
}

.jp-RenderedHTMLCommon tbody tr:nth-child(even) {
  background: var(--jp-rendermime-table-row-background);
}

.jp-RenderedHTMLCommon tbody tr:hover {
  background: var(--jp-rendermime-table-row-hover-background);
}

.jp-RenderedHTMLCommon table {
  margin-bottom: 1em;
}

.jp-RenderedHTMLCommon p {
  text-align: left;
  margin: 0px;
}

.jp-RenderedHTMLCommon p {
  margin-bottom: 1em;
}

.jp-RenderedHTMLCommon img {
  -moz-force-broken-image-icon: 1;
}

/* Restrict to direct children as other images could be nested in other content. */
.jp-RenderedHTMLCommon > img {
  display: block;
  margin-left: 0;
  margin-right: 0;
  margin-bottom: 1em;
}

/* Change color behind transparent images if they need it... */
[data-jp-theme-light='false'] .jp-RenderedImage img.jp-needs-light-background {
  background-color: var(--jp-inverse-layout-color1);
}
[data-jp-theme-light='true'] .jp-RenderedImage img.jp-needs-dark-background {
  background-color: var(--jp-inverse-layout-color1);
}
/* ...or leave it untouched if they don't */
[data-jp-theme-light='false'] .jp-RenderedImage img.jp-needs-dark-background {
}
[data-jp-theme-light='true'] .jp-RenderedImage img.jp-needs-light-background {
}

.jp-RenderedHTMLCommon img,
.jp-RenderedImage img,
.jp-RenderedHTMLCommon svg,
.jp-RenderedSVG svg {
  max-width: 100%;
  height: auto;
}

.jp-RenderedHTMLCommon img.jp-mod-unconfined,
.jp-RenderedImage img.jp-mod-unconfined,
.jp-RenderedHTMLCommon svg.jp-mod-unconfined,
.jp-RenderedSVG svg.jp-mod-unconfined {
  max-width: none;
}

.jp-RenderedHTMLCommon .alert {
  padding: var(--jp-notebook-padding);
  border: var(--jp-border-width) solid transparent;
  border-radius: var(--jp-border-radius);
  margin-bottom: 1em;
}

.jp-RenderedHTMLCommon .alert-info {
  color: var(--jp-info-color0);
  background-color: var(--jp-info-color3);
  border-color: var(--jp-info-color2);
}
.jp-RenderedHTMLCommon .alert-info hr {
  border-color: var(--jp-info-color3);
}
.jp-RenderedHTMLCommon .alert-info > p:last-child,
.jp-RenderedHTMLCommon .alert-info > ul:last-child {
  margin-bottom: 0;
}

.jp-RenderedHTMLCommon .alert-warning {
  color: var(--jp-warn-color0);
  background-color: var(--jp-warn-color3);
  border-color: var(--jp-warn-color2);
}
.jp-RenderedHTMLCommon .alert-warning hr {
  border-color: var(--jp-warn-color3);
}
.jp-RenderedHTMLCommon .alert-warning > p:last-child,
.jp-RenderedHTMLCommon .alert-warning > ul:last-child {
  margin-bottom: 0;
}

.jp-RenderedHTMLCommon .alert-success {
  color: var(--jp-success-color0);
  background-color: var(--jp-success-color3);
  border-color: var(--jp-success-color2);
}
.jp-RenderedHTMLCommon .alert-success hr {
  border-color: var(--jp-success-color3);
}
.jp-RenderedHTMLCommon .alert-success > p:last-child,
.jp-RenderedHTMLCommon .alert-success > ul:last-child {
  margin-bottom: 0;
}

.jp-RenderedHTMLCommon .alert-danger {
  color: var(--jp-error-color0);
  background-color: var(--jp-error-color3);
  border-color: var(--jp-error-color2);
}
.jp-RenderedHTMLCommon .alert-danger hr {
  border-color: var(--jp-error-color3);
}
.jp-RenderedHTMLCommon .alert-danger > p:last-child,
.jp-RenderedHTMLCommon .alert-danger > ul:last-child {
  margin-bottom: 0;
}

.jp-RenderedHTMLCommon blockquote {
  margin: 1em 2em;
  padding: 0 1em;
  border-left: 5px solid var(--jp-border-color2);
}

a.jp-InternalAnchorLink {
  visibility: hidden;
  margin-left: 8px;
  color: var(--md-blue-800);
}

h1:hover .jp-InternalAnchorLink,
h2:hover .jp-InternalAnchorLink,
h3:hover .jp-InternalAnchorLink,
h4:hover .jp-InternalAnchorLink,
h5:hover .jp-InternalAnchorLink,
h6:hover .jp-InternalAnchorLink {
  visibility: visible;
}

.jp-RenderedHTMLCommon kbd {
  background-color: var(--jp-rendermime-table-row-background);
  border: 1px solid var(--jp-border-color0);
  border-bottom-color: var(--jp-border-color2);
  border-radius: 3px;
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.25);
  display: inline-block;
  font-size: 0.8em;
  line-height: 1em;
  padding: 0.2em 0.5em;
}

/* Most direct children of .jp-RenderedHTMLCommon have a margin-bottom of 1.0.
 * At the bottom of cells this is a bit too much as there is also spacing
 * between cells. Going all the way to 0 gets too tight between markdown and
 * code cells.
 */
.jp-RenderedHTMLCommon > *:last-child {
  margin-bottom: 0.5em;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* This file was auto-generated by ensurePackage() in @jupyterlab/buildutils */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-MimeDocument {
  outline: none;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* This file was auto-generated by ensurePackage() in @jupyterlab/buildutils */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Variables
|----------------------------------------------------------------------------*/

:root {
  --jp-private-filebrowser-button-height: 28px;
  --jp-private-filebrowser-button-width: 48px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-FileBrowser {
  display: flex;
  flex-direction: column;
  color: var(--jp-ui-font-color1);
  background: var(--jp-layout-color1);
  /* This is needed so that all font sizing of children done in ems is
   * relative to this base size */
  font-size: var(--jp-ui-font-size1);
}

.jp-FileBrowser-toolbar.jp-Toolbar {
  border-bottom: none;
  height: auto;
  margin: var(--jp-toolbar-header-margin);
  box-shadow: none;
}

.jp-BreadCrumbs {
  flex: 0 0 auto;
  margin: 4px 12px;
}

.jp-BreadCrumbs-item {
  margin: 0px 2px;
  padding: 0px 2px;
  border-radius: var(--jp-border-radius);
  cursor: pointer;
}

.jp-BreadCrumbs-item:hover {
  background-color: var(--jp-layout-color2);
}

.jp-BreadCrumbs-item:first-child {
  margin-left: 0px;
}

.jp-BreadCrumbs-item.jp-mod-dropTarget {
  background-color: var(--jp-brand-color2);
  opacity: 0.7;
}

/*-----------------------------------------------------------------------------
| Buttons
|----------------------------------------------------------------------------*/

.jp-FileBrowser-toolbar.jp-Toolbar {
  padding: 0px;
}

.jp-FileBrowser-toolbar.jp-Toolbar {
  justify-content: space-evenly;
}

.jp-FileBrowser-toolbar.jp-Toolbar .jp-Toolbar-item {
  flex: 1;
}

.jp-FileBrowser-toolbar.jp-Toolbar .jp-ToolbarButtonComponent {
  width: 100%;
}

/*-----------------------------------------------------------------------------
| DirListing
|----------------------------------------------------------------------------*/

.jp-DirListing {
  flex: 1 1 auto;
  display: flex;
  flex-direction: column;
  outline: 0;
}

.jp-DirListing-header {
  flex: 0 0 auto;
  display: flex;
  flex-direction: row;
  overflow: hidden;
  border-top: var(--jp-border-width) solid var(--jp-border-color2);
  border-bottom: var(--jp-border-width) solid var(--jp-border-color1);
  box-shadow: var(--jp-toolbar-box-shadow);
  z-index: 2;
}

.jp-DirListing-headerItem {
  padding: 4px 12px 2px 12px;
  font-weight: 500;
}

.jp-DirListing-headerItem:hover {
  background: var(--jp-layout-color2);
}

.jp-DirListing-headerItem.jp-id-name {
  flex: 1 0 84px;
}

.jp-DirListing-headerItem.jp-id-modified {
  flex: 0 0 112px;
  border-left: var(--jp-border-width) solid var(--jp-border-color2);
  text-align: right;
}

.jp-DirListing-narrow .jp-id-modified,
.jp-DirListing-narrow .jp-DirListing-itemModified {
  display: none;
}

.jp-DirListing-headerItem.jp-mod-selected {
  font-weight: 600;
}

/* increase specificity to override bundled default */
.jp-DirListing-content {
  flex: 1 1 auto;
  margin: 0;
  padding: 0;
  list-style-type: none;
  overflow: auto;
  background-color: var(--jp-layout-color1);
}

/* Style the directory listing content when a user drops a file to upload */
.jp-DirListing.jp-mod-native-drop .jp-DirListing-content {
  outline: 5px dashed rgba(128, 128, 128, 0.5);
  outline-offset: -10px;
  cursor: copy;
}

.jp-DirListing-item {
  display: flex;
  flex-direction: row;
  padding: 4px 12px;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

.jp-DirListing-item.jp-mod-selected {
  color: white;
  background: var(--jp-brand-color1);
}

.jp-DirListing-item.jp-mod-dropTarget {
  background: var(--jp-brand-color3);
}

.jp-DirListing-item:hover:not(.jp-mod-selected) {
  background: var(--jp-layout-color2);
}

.jp-DirListing-itemIcon {
  flex: 0 0 20px;
  margin-right: 4px;
}

.jp-DirListing-itemText {
  flex: 1 0 64px;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
  user-select: none;
}

.jp-DirListing-itemModified {
  flex: 0 0 125px;
  text-align: right;
}

.jp-DirListing-editor {
  flex: 1 0 64px;
  outline: none;
  border: none;
}

.jp-DirListing-item.jp-mod-running .jp-DirListing-itemIcon:before {
  color: limegreen;
  content: '\25CF';
  font-size: 8px;
  position: absolute;
  left: -8px;
}

.jp-DirListing-item.lm-mod-drag-image,
.jp-DirListing-item.jp-mod-selected.lm-mod-drag-image {
  font-size: var(--jp-ui-font-size1);
  padding-left: 4px;
  margin-left: 4px;
  width: 160px;
  background-color: var(--jp-ui-inverse-font-color2);
  box-shadow: var(--jp-elevation-z2);
  border-radius: 0px;
  color: var(--jp-ui-font-color1);
  transform: translateX(-40%) translateY(-58%);
}

.jp-DirListing-deadSpace {
  flex: 1 1 auto;
  margin: 0;
  padding: 0;
  list-style-type: none;
  overflow: auto;
  background-color: var(--jp-layout-color1);
}

.jp-Document {
  min-width: 120px;
  min-height: 120px;
  outline: none;
}

.jp-FileDialog.jp-mod-conflict input {
  color: red;
}

.jp-FileDialog .jp-new-name-title {
  margin-top: 12px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* This file was auto-generated by ensurePackage() in @jupyterlab/buildutils */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Private CSS variables
|----------------------------------------------------------------------------*/

:root {
}

/*-----------------------------------------------------------------------------
| Main OutputArea
| OutputArea has a list of Outputs
|----------------------------------------------------------------------------*/

.jp-OutputArea {
  overflow-y: auto;
}

.jp-OutputArea-child {
  display: flex;
  flex-direction: row;
}

.jp-OutputPrompt {
  flex: 0 0 var(--jp-cell-prompt-width);
  color: var(--jp-cell-outprompt-font-color);
  font-family: var(--jp-cell-prompt-font-family);
  padding: var(--jp-code-padding);
  letter-spacing: var(--jp-cell-prompt-letter-spacing);
  line-height: var(--jp-code-line-height);
  font-size: var(--jp-code-font-size);
  border: var(--jp-border-width) solid transparent;
  opacity: var(--jp-cell-prompt-opacity);
  /* Right align prompt text, don't wrap to handle large prompt numbers */
  text-align: right;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
  /* Disable text selection */
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

.jp-OutputArea-output {
  height: auto;
  overflow: auto;
  user-select: text;
  -moz-user-select: text;
  -webkit-user-select: text;
  -ms-user-select: text;
}

.jp-OutputArea-child .jp-OutputArea-output {
  flex-grow: 1;
  flex-shrink: 1;
}

/**
 * Isolated output.
 */
.jp-OutputArea-output.jp-mod-isolated {
  width: 100%;
  display: block;
}

/*
When drag events occur, `p-mod-override-cursor` is added to the body.
Because iframes steal all cursor events, the following two rules are necessary
to suppress pointer events while resize drags are occurring. There may be a
better solution to this problem.
*/
body.lm-mod-override-cursor .jp-OutputArea-output.jp-mod-isolated {
  position: relative;
}

body.lm-mod-override-cursor .jp-OutputArea-output.jp-mod-isolated:before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: transparent;
}

/* pre */

.jp-OutputArea-output pre {
  border: none;
  margin: 0px;
  padding: 0px;
  overflow-x: auto;
  overflow-y: auto;
  word-break: break-all;
  word-wrap: break-word;
  white-space: pre-wrap;
}

/* tables */

.jp-OutputArea-output.jp-RenderedHTMLCommon table {
  margin-left: 0;
  margin-right: 0;
}

/* description lists */

.jp-OutputArea-output dl,
.jp-OutputArea-output dt,
.jp-OutputArea-output dd {
  display: block;
}

.jp-OutputArea-output dl {
  width: 100%;
  overflow: hidden;
  padding: 0;
  margin: 0;
}

.jp-OutputArea-output dt {
  font-weight: bold;
  float: left;
  width: 20%;
  padding: 0;
  margin: 0;
}

.jp-OutputArea-output dd {
  float: left;
  width: 80%;
  padding: 0;
  margin: 0;
}

/* Hide the gutter in case of
 *  - nested output areas (e.g. in the case of output widgets)
 *  - mirrored output areas
 */
.jp-OutputArea .jp-OutputArea .jp-OutputArea-prompt {
  display: none;
}

/*-----------------------------------------------------------------------------
| executeResult is added to any Output-result for the display of the object
| returned by a cell
|----------------------------------------------------------------------------*/

.jp-OutputArea-output.jp-OutputArea-executeResult {
  margin-left: 0px;
  flex: 1 1 auto;
}

.jp-OutputArea-executeResult.jp-RenderedText {
  padding-top: var(--jp-code-padding);
}

/*-----------------------------------------------------------------------------
| The Stdin output
|----------------------------------------------------------------------------*/

.jp-OutputArea-stdin {
  line-height: var(--jp-code-line-height);
  padding-top: var(--jp-code-padding);
  display: flex;
}

.jp-Stdin-prompt {
  color: var(--jp-content-font-color0);
  padding-right: var(--jp-code-padding);
  vertical-align: baseline;
  flex: 0 0 auto;
}

.jp-Stdin-input {
  font-family: var(--jp-code-font-family);
  font-size: inherit;
  color: inherit;
  background-color: inherit;
  width: 42%;
  min-width: 200px;
  /* make sure input baseline aligns with prompt */
  vertical-align: baseline;
  /* padding + margin = 0.5em between prompt and cursor */
  padding: 0em 0.25em;
  margin: 0em 0.25em;
  flex: 0 0 70%;
}

.jp-Stdin-input:focus {
  box-shadow: none;
}

/*-----------------------------------------------------------------------------
| Output Area View
|----------------------------------------------------------------------------*/

.jp-LinkedOutputView .jp-OutputArea {
  height: 100%;
  display: block;
}

.jp-LinkedOutputView .jp-OutputArea-output:only-child {
  height: 100%;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* This file was auto-generated by ensurePackage() in @jupyterlab/buildutils */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-Collapser {
  flex: 0 0 var(--jp-cell-collapser-width);
  padding: 0px;
  margin: 0px;
  border: none;
  outline: none;
  background: transparent;
  border-radius: var(--jp-border-radius);
  opacity: 1;
}

.jp-Collapser-child {
  display: block;
  width: 100%;
  box-sizing: border-box;
  /* height: 100% doesn't work because the height of its parent is computed from content */
  position: absolute;
  top: 0px;
  bottom: 0px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Header/Footer
|----------------------------------------------------------------------------*/

/* Hidden by zero height by default */
.jp-CellHeader,
.jp-CellFooter {
  height: 0px;
  width: 100%;
  padding: 0px;
  margin: 0px;
  border: none;
  outline: none;
  background: transparent;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Input
|----------------------------------------------------------------------------*/

/* All input areas */
.jp-InputArea {
  display: flex;
  flex-direction: row;
}

.jp-InputArea-editor {
  flex: 1 1 auto;
}

.jp-InputArea-editor {
  /* This is the non-active, default styling */
  border: var(--jp-border-width) solid var(--jp-cell-editor-border-color);
  border-radius: 0px;
  background: var(--jp-cell-editor-background);
}

.jp-InputPrompt {
  flex: 0 0 var(--jp-cell-prompt-width);
  color: var(--jp-cell-inprompt-font-color);
  font-family: var(--jp-cell-prompt-font-family);
  padding: var(--jp-code-padding);
  letter-spacing: var(--jp-cell-prompt-letter-spacing);
  opacity: var(--jp-cell-prompt-opacity);
  line-height: var(--jp-code-line-height);
  font-size: var(--jp-code-font-size);
  border: var(--jp-border-width) solid transparent;
  opacity: var(--jp-cell-prompt-opacity);
  /* Right align prompt text, don't wrap to handle large prompt numbers */
  text-align: right;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
  /* Disable text selection */
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Placeholder
|----------------------------------------------------------------------------*/

.jp-Placeholder {
  display: flex;
  flex-direction: row;
  flex: 1 1 auto;
}

.jp-Placeholder-prompt {
  box-sizing: border-box;
}

.jp-Placeholder-content {
  flex: 1 1 auto;
  border: none;
  background: transparent;
  height: 20px;
  box-sizing: border-box;
}

.jp-Placeholder-content .jp-MoreHorizIcon {
  width: 32px;
  height: 16px;
  border: 1px solid transparent;
  border-radius: var(--jp-border-radius);
}

.jp-Placeholder-content .jp-MoreHorizIcon:hover {
  border: 1px solid var(--jp-border-color1);
  box-shadow: 0px 0px 2px 0px rgba(0, 0, 0, 0.25);
  background-color: var(--jp-layout-color0);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Private CSS variables
|----------------------------------------------------------------------------*/

:root {
  --jp-private-cell-scrolling-output-offset: 5px;
}

/*-----------------------------------------------------------------------------
| Cell
|----------------------------------------------------------------------------*/

.jp-Cell {
  padding: var(--jp-cell-padding);
  margin: 0px;
  border: none;
  outline: none;
  background: transparent;
}

/*-----------------------------------------------------------------------------
| Common input/output
|----------------------------------------------------------------------------*/

.jp-Cell-inputWrapper,
.jp-Cell-outputWrapper {
  display: flex;
  flex-direction: row;
  padding: 0px;
  margin: 0px;
  /* Added to reveal the box-shadow on the input and output collapsers. */
  overflow: visible;
}

/* Only input/output areas inside cells */
.jp-Cell-inputArea,
.jp-Cell-outputArea {
  flex: 1 1 auto;
}

/*-----------------------------------------------------------------------------
| Collapser
|----------------------------------------------------------------------------*/

/* Make the output collapser disappear when there is not output, but do so
 * in a manner that leaves it in the layout and preserves its width.
 */
.jp-Cell.jp-mod-noOutputs .jp-Cell-outputCollapser {
  border: none !important;
  background: transparent !important;
}

.jp-Cell:not(.jp-mod-noOutputs) .jp-Cell-outputCollapser {
  min-height: var(--jp-cell-collapser-min-height);
}

/*-----------------------------------------------------------------------------
| Output
|----------------------------------------------------------------------------*/

/* Put a space between input and output when there IS output */
.jp-Cell:not(.jp-mod-noOutputs) .jp-Cell-outputWrapper {
  margin-top: 5px;
}

/* Text output with the Out[] prompt needs a top padding to match the
 * alignment of the Out[] prompt itself.
 */
.jp-OutputArea-executeResult .jp-RenderedText.jp-OutputArea-output {
  padding-top: var(--jp-code-padding);
}

.jp-CodeCell.jp-mod-outputsScrolled .jp-Cell-outputArea {
  overflow-y: auto;
  max-height: 200px;
  box-shadow: inset 0 0 6px 2px rgba(0, 0, 0, 0.3);
  margin-left: var(--jp-private-cell-scrolling-output-offset);
}

.jp-CodeCell.jp-mod-outputsScrolled .jp-OutputArea-prompt {
  flex: 0 0
    calc(
      var(--jp-cell-prompt-width) -
        var(--jp-private-cell-scrolling-output-offset)
    );
}

/*-----------------------------------------------------------------------------
| CodeCell
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| MarkdownCell
|----------------------------------------------------------------------------*/

.jp-MarkdownOutput {
  flex: 1 1 auto;
  margin-top: 0;
  margin-bottom: 0;
  padding-left: var(--jp-code-padding);
}

.jp-MarkdownOutput.jp-RenderedHTMLCommon {
  overflow: auto;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* This file was auto-generated by ensurePackage() in @jupyterlab/buildutils */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Variables
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------

/*-----------------------------------------------------------------------------
| Styles
|----------------------------------------------------------------------------*/

.jp-NotebookPanel-toolbar {
  padding: 2px;
}

.jp-Toolbar-item.jp-Notebook-toolbarCellType .jp-select-wrapper.jp-mod-focused {
  border: none;
  box-shadow: none;
}

.jp-Notebook-toolbarCellTypeDropdown select {
  height: 24px;
  font-size: var(--jp-ui-font-size1);
  line-height: 14px;
  border-radius: 0;
  display: block;
}

.jp-Notebook-toolbarCellTypeDropdown span {
  top: 5px !important;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Private CSS variables
|----------------------------------------------------------------------------*/

:root {
  --jp-private-notebook-dragImage-width: 304px;
  --jp-private-notebook-dragImage-height: 36px;
  --jp-private-notebook-selected-color: var(--md-blue-400);
  --jp-private-notebook-active-color: var(--md-green-400);
}

/*-----------------------------------------------------------------------------
| Imports
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Notebook
|----------------------------------------------------------------------------*/

.jp-NotebookPanel {
  display: block;
  height: 100%;
}

.jp-NotebookPanel.jp-Document {
  min-width: 240px;
  min-height: 120px;
}

.jp-Notebook {
  padding: var(--jp-notebook-padding);
  outline: none;
  overflow: auto;
  background: var(--jp-layout-color0);
}

.jp-Notebook.jp-mod-scrollPastEnd::after {
  display: block;
  content: '';
  min-height: var(--jp-notebook-scroll-padding);
}

.jp-Notebook .jp-Cell {
  overflow: visible;
}

.jp-Notebook .jp-Cell .jp-InputPrompt {
  cursor: move;
}

/*-----------------------------------------------------------------------------
| Notebook state related styling
|
| The notebook and cells each have states, here are the possibilities:
|
| - Notebook
|   - Command
|   - Edit
| - Cell
|   - None
|   - Active (only one can be active)
|   - Selected (the cells actions are applied to)
|   - Multiselected (when multiple selected, the cursor)
|   - No outputs
|----------------------------------------------------------------------------*/

/* Command or edit modes */

.jp-Notebook .jp-Cell:not(.jp-mod-active) .jp-InputPrompt {
  opacity: var(--jp-cell-prompt-not-active-opacity);
  color: var(--jp-cell-prompt-not-active-font-color);
}

.jp-Notebook .jp-Cell:not(.jp-mod-active) .jp-OutputPrompt {
  opacity: var(--jp-cell-prompt-not-active-opacity);
  color: var(--jp-cell-prompt-not-active-font-color);
}

/* cell is active */
.jp-Notebook .jp-Cell.jp-mod-active .jp-Collapser {
  background: var(--jp-brand-color1);
}

/* collapser is hovered */
.jp-Notebook .jp-Cell .jp-Collapser:hover {
  box-shadow: var(--jp-elevation-z2);
  background: var(--jp-brand-color1);
  opacity: var(--jp-cell-collapser-not-active-hover-opacity);
}

/* cell is active and collapser is hovered */
.jp-Notebook .jp-Cell.jp-mod-active .jp-Collapser:hover {
  background: var(--jp-brand-color0);
  opacity: 1;
}

/* Command mode */

.jp-Notebook.jp-mod-commandMode .jp-Cell.jp-mod-selected {
  background: var(--jp-notebook-multiselected-color);
}

.jp-Notebook.jp-mod-commandMode
  .jp-Cell.jp-mod-active.jp-mod-selected:not(.jp-mod-multiSelected) {
  background: transparent;
}

/* Edit mode */

.jp-Notebook.jp-mod-editMode .jp-Cell.jp-mod-active .jp-InputArea-editor {
  border: var(--jp-border-width) solid var(--jp-cell-editor-active-border-color);
  box-shadow: var(--jp-input-box-shadow);
  background-color: var(--jp-cell-editor-active-background);
}

/*-----------------------------------------------------------------------------
| Notebook drag and drop
|----------------------------------------------------------------------------*/

.jp-Notebook-cell.jp-mod-dropSource {
  opacity: 0.5;
}

.jp-Notebook-cell.jp-mod-dropTarget,
.jp-Notebook.jp-mod-commandMode
  .jp-Notebook-cell.jp-mod-active.jp-mod-selected.jp-mod-dropTarget {
  border-top-color: var(--jp-private-notebook-selected-color);
  border-top-style: solid;
  border-top-width: 2px;
}

.jp-dragImage {
  display: flex;
  flex-direction: row;
  width: var(--jp-private-notebook-dragImage-width);
  height: var(--jp-private-notebook-dragImage-height);
  border: var(--jp-border-width) solid var(--jp-cell-editor-border-color);
  background: var(--jp-cell-editor-background);
  overflow: visible;
}

.jp-dragImage-singlePrompt {
  box-shadow: 2px 2px 4px 0px rgba(0, 0, 0, 0.12);
}

.jp-dragImage .jp-dragImage-content {
  flex: 1 1 auto;
  z-index: 2;
  font-size: var(--jp-code-font-size);
  font-family: var(--jp-code-font-family);
  line-height: var(--jp-code-line-height);
  padding: var(--jp-code-padding);
  border: var(--jp-border-width) solid var(--jp-cell-editor-border-color);
  background: var(--jp-cell-editor-background-color);
  color: var(--jp-content-font-color3);
  text-align: left;
  margin: 4px 4px 4px 0px;
}

.jp-dragImage .jp-dragImage-prompt {
  flex: 0 0 auto;
  min-width: 36px;
  color: var(--jp-cell-inprompt-font-color);
  padding: var(--jp-code-padding);
  padding-left: 12px;
  font-family: var(--jp-cell-prompt-font-family);
  letter-spacing: var(--jp-cell-prompt-letter-spacing);
  line-height: 1.9;
  font-size: var(--jp-code-font-size);
  border: var(--jp-border-width) solid transparent;
}

.jp-dragImage-multipleBack {
  z-index: -1;
  position: absolute;
  height: 32px;
  width: 300px;
  top: 8px;
  left: 8px;
  background: var(--jp-layout-color2);
  border: var(--jp-border-width) solid var(--jp-input-border-color);
  box-shadow: 2px 2px 4px 0px rgba(0, 0, 0, 0.12);
}

/*-----------------------------------------------------------------------------
| Cell toolbar
|----------------------------------------------------------------------------*/

.jp-NotebookTools {
  display: block;
  min-width: var(--jp-sidebar-min-width);
  color: var(--jp-ui-font-color1);
  background: var(--jp-layout-color1);
  /* This is needed so that all font sizing of children done in ems is
    * relative to this base size */
  font-size: var(--jp-ui-font-size1);
  overflow: auto;
}

.jp-NotebookTools-tool {
  padding: 0px 12px 0 12px;
}

.jp-ActiveCellTool {
  padding: 12px;
  background-color: var(--jp-layout-color1);
  border-top: none !important;
}

.jp-ActiveCellTool .jp-InputArea-prompt {
  flex: 0 0 auto;
  padding-left: 0px;
}

.jp-ActiveCellTool .jp-InputArea-editor {
  flex: 1 1 auto;
  background: var(--jp-cell-editor-background);
  border-color: var(--jp-cell-editor-border-color);
}

.jp-ActiveCellTool .jp-InputArea-editor .CodeMirror {
  background: transparent;
}

.jp-MetadataEditorTool {
  flex-direction: column;
  padding: 12px 0px 12px 0px;
}

.jp-RankedPanel > :not(:first-child) {
  margin-top: 12px;
}

.jp-KeySelector select.jp-mod-styled {
  font-size: var(--jp-ui-font-size1);
  color: var(--jp-ui-font-color0);
  border: var(--jp-border-width) solid var(--jp-border-color1);
}

.jp-KeySelector label,
.jp-MetadataEditorTool label {
  line-height: 1.4;
}

/*-----------------------------------------------------------------------------
| Presentation Mode (.jp-mod-presentationMode)
|----------------------------------------------------------------------------*/

.jp-mod-presentationMode .jp-Notebook {
  --jp-content-font-size1: var(--jp-content-presentation-font-size1);
  --jp-code-font-size: var(--jp-code-presentation-font-size);
}

.jp-mod-presentationMode .jp-Notebook .jp-Cell .jp-InputPrompt,
.jp-mod-presentationMode .jp-Notebook .jp-Cell .jp-OutputPrompt {
  flex: 0 0 110px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* This file was auto-generated by ensurePackage() in @jupyterlab/buildutils */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

</style>

    <style type="text/css">
/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*
The following CSS variables define the main, public API for styling JupyterLab.
These variables should be used by all plugins wherever possible. In other
words, plugins should not define custom colors, sizes, etc unless absolutely
necessary. This enables users to change the visual theme of JupyterLab
by changing these variables.

Many variables appear in an ordered sequence (0,1,2,3). These sequences
are designed to work well together, so for example, `--jp-border-color1` should
be used with `--jp-layout-color1`. The numbers have the following meanings:

* 0: super-primary, reserved for special emphasis
* 1: primary, most important under normal situations
* 2: secondary, next most important under normal situations
* 3: tertiary, next most important under normal situations

Throughout JupyterLab, we are mostly following principles from Google's
Material Design when selecting colors. We are not, however, following
all of MD as it is not optimized for dense, information rich UIs.
*/

:root {
  /* Elevation
   *
   * We style box-shadows using Material Design's idea of elevation. These particular numbers are taken from here:
   *
   * https://github.com/material-components/material-components-web
   * https://material-components-web.appspot.com/elevation.html
   */

  --jp-shadow-base-lightness: 0;
  --jp-shadow-umbra-color: rgba(
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    0.2
  );
  --jp-shadow-penumbra-color: rgba(
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    0.14
  );
  --jp-shadow-ambient-color: rgba(
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    0.12
  );
  --jp-elevation-z0: none;
  --jp-elevation-z1: 0px 2px 1px -1px var(--jp-shadow-umbra-color),
    0px 1px 1px 0px var(--jp-shadow-penumbra-color),
    0px 1px 3px 0px var(--jp-shadow-ambient-color);
  --jp-elevation-z2: 0px 3px 1px -2px var(--jp-shadow-umbra-color),
    0px 2px 2px 0px var(--jp-shadow-penumbra-color),
    0px 1px 5px 0px var(--jp-shadow-ambient-color);
  --jp-elevation-z4: 0px 2px 4px -1px var(--jp-shadow-umbra-color),
    0px 4px 5px 0px var(--jp-shadow-penumbra-color),
    0px 1px 10px 0px var(--jp-shadow-ambient-color);
  --jp-elevation-z6: 0px 3px 5px -1px var(--jp-shadow-umbra-color),
    0px 6px 10px 0px var(--jp-shadow-penumbra-color),
    0px 1px 18px 0px var(--jp-shadow-ambient-color);
  --jp-elevation-z8: 0px 5px 5px -3px var(--jp-shadow-umbra-color),
    0px 8px 10px 1px var(--jp-shadow-penumbra-color),
    0px 3px 14px 2px var(--jp-shadow-ambient-color);
  --jp-elevation-z12: 0px 7px 8px -4px var(--jp-shadow-umbra-color),
    0px 12px 17px 2px var(--jp-shadow-penumbra-color),
    0px 5px 22px 4px var(--jp-shadow-ambient-color);
  --jp-elevation-z16: 0px 8px 10px -5px var(--jp-shadow-umbra-color),
    0px 16px 24px 2px var(--jp-shadow-penumbra-color),
    0px 6px 30px 5px var(--jp-shadow-ambient-color);
  --jp-elevation-z20: 0px 10px 13px -6px var(--jp-shadow-umbra-color),
    0px 20px 31px 3px var(--jp-shadow-penumbra-color),
    0px 8px 38px 7px var(--jp-shadow-ambient-color);
  --jp-elevation-z24: 0px 11px 15px -7px var(--jp-shadow-umbra-color),
    0px 24px 38px 3px var(--jp-shadow-penumbra-color),
    0px 9px 46px 8px var(--jp-shadow-ambient-color);

  /* Borders
   *
   * The following variables, specify the visual styling of borders in JupyterLab.
   */

  --jp-border-width: 1px;
  --jp-border-color0: var(--md-grey-400);
  --jp-border-color1: var(--md-grey-400);
  --jp-border-color2: var(--md-grey-300);
  --jp-border-color3: var(--md-grey-200);
  --jp-border-radius: 2px;

  /* UI Fonts
   *
   * The UI font CSS variables are used for the typography all of the JupyterLab
   * user interface elements that are not directly user generated content.
   *
   * The font sizing here is done assuming that the body font size of --jp-ui-font-size1
   * is applied to a parent element. When children elements, such as headings, are sized
   * in em all things will be computed relative to that body size.
   */

  --jp-ui-font-scale-factor: 1.2;
  --jp-ui-font-size0: 0.83333em;
  --jp-ui-font-size1: 13px; /* Base font size */
  --jp-ui-font-size2: 1.2em;
  --jp-ui-font-size3: 1.44em;

  --jp-ui-font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica,
    Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol';

  /*
   * Use these font colors against the corresponding main layout colors.
   * In a light theme, these go from dark to light.
   */

  /* Defaults use Material Design specification */
  --jp-ui-font-color0: rgba(0, 0, 0, 1);
  --jp-ui-font-color1: rgba(0, 0, 0, 0.87);
  --jp-ui-font-color2: rgba(0, 0, 0, 0.54);
  --jp-ui-font-color3: rgba(0, 0, 0, 0.38);

  /*
   * Use these against the brand/accent/warn/error colors.
   * These will typically go from light to darker, in both a dark and light theme.
   */

  --jp-ui-inverse-font-color0: rgba(255, 255, 255, 1);
  --jp-ui-inverse-font-color1: rgba(255, 255, 255, 1);
  --jp-ui-inverse-font-color2: rgba(255, 255, 255, 0.7);
  --jp-ui-inverse-font-color3: rgba(255, 255, 255, 0.5);

  /* Content Fonts
   *
   * Content font variables are used for typography of user generated content.
   *
   * The font sizing here is done assuming that the body font size of --jp-content-font-size1
   * is applied to a parent element. When children elements, such as headings, are sized
   * in em all things will be computed relative to that body size.
   */

  --jp-content-line-height: 1.6;
  --jp-content-font-scale-factor: 1.2;
  --jp-content-font-size0: 0.83333em;
  --jp-content-font-size1: 14px; /* Base font size */
  --jp-content-font-size2: 1.2em;
  --jp-content-font-size3: 1.44em;
  --jp-content-font-size4: 1.728em;
  --jp-content-font-size5: 2.0736em;

  /* This gives a magnification of about 125% in presentation mode over normal. */
  --jp-content-presentation-font-size1: 17px;

  --jp-content-heading-line-height: 1;
  --jp-content-heading-margin-top: 1.2em;
  --jp-content-heading-margin-bottom: 0.8em;
  --jp-content-heading-font-weight: 500;

  /* Defaults use Material Design specification */
  --jp-content-font-color0: rgba(0, 0, 0, 1);
  --jp-content-font-color1: rgba(0, 0, 0, 0.87);
  --jp-content-font-color2: rgba(0, 0, 0, 0.54);
  --jp-content-font-color3: rgba(0, 0, 0, 0.38);

  --jp-content-link-color: var(--md-blue-700);

  --jp-content-font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Helvetica, Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji',
    'Segoe UI Symbol';

  /*
   * Code Fonts
   *
   * Code font variables are used for typography of code and other monospaces content.
   */

  --jp-code-font-size: 13px;
  --jp-code-line-height: 1.3077; /* 17px for 13px base */
  --jp-code-padding: 5px; /* 5px for 13px base, codemirror highlighting needs integer px value */
  --jp-code-font-family-default: Menlo, Consolas, 'DejaVu Sans Mono', monospace;
  --jp-code-font-family: var(--jp-code-font-family-default);

  /* This gives a magnification of about 125% in presentation mode over normal. */
  --jp-code-presentation-font-size: 16px;

  /* may need to tweak cursor width if you change font size */
  --jp-code-cursor-width0: 1.4px;
  --jp-code-cursor-width1: 2px;
  --jp-code-cursor-width2: 4px;

  /* Layout
   *
   * The following are the main layout colors use in JupyterLab. In a light
   * theme these would go from light to dark.
   */

  --jp-layout-color0: white;
  --jp-layout-color1: white;
  --jp-layout-color2: var(--md-grey-200);
  --jp-layout-color3: var(--md-grey-400);
  --jp-layout-color4: var(--md-grey-600);

  /* Inverse Layout
   *
   * The following are the inverse layout colors use in JupyterLab. In a light
   * theme these would go from dark to light.
   */

  --jp-inverse-layout-color0: #111111;
  --jp-inverse-layout-color1: var(--md-grey-900);
  --jp-inverse-layout-color2: var(--md-grey-800);
  --jp-inverse-layout-color3: var(--md-grey-700);
  --jp-inverse-layout-color4: var(--md-grey-600);

  /* Brand/accent */

  --jp-brand-color0: var(--md-blue-700);
  --jp-brand-color1: var(--md-blue-500);
  --jp-brand-color2: var(--md-blue-300);
  --jp-brand-color3: var(--md-blue-100);
  --jp-brand-color4: var(--md-blue-50);

  --jp-accent-color0: var(--md-green-700);
  --jp-accent-color1: var(--md-green-500);
  --jp-accent-color2: var(--md-green-300);
  --jp-accent-color3: var(--md-green-100);

  /* State colors (warn, error, success, info) */

  --jp-warn-color0: var(--md-orange-700);
  --jp-warn-color1: var(--md-orange-500);
  --jp-warn-color2: var(--md-orange-300);
  --jp-warn-color3: var(--md-orange-100);

  --jp-error-color0: var(--md-red-700);
  --jp-error-color1: var(--md-red-500);
  --jp-error-color2: var(--md-red-300);
  --jp-error-color3: var(--md-red-100);

  --jp-success-color0: var(--md-green-700);
  --jp-success-color1: var(--md-green-500);
  --jp-success-color2: var(--md-green-300);
  --jp-success-color3: var(--md-green-100);

  --jp-info-color0: var(--md-cyan-700);
  --jp-info-color1: var(--md-cyan-500);
  --jp-info-color2: var(--md-cyan-300);
  --jp-info-color3: var(--md-cyan-100);

  /* Cell specific styles */

  --jp-cell-padding: 5px;

  --jp-cell-collapser-width: 8px;
  --jp-cell-collapser-min-height: 20px;
  --jp-cell-collapser-not-active-hover-opacity: 0.6;

  --jp-cell-editor-background: var(--md-grey-100);
  --jp-cell-editor-border-color: var(--md-grey-300);
  --jp-cell-editor-box-shadow: inset 0 0 2px var(--md-blue-300);
  --jp-cell-editor-active-background: var(--jp-layout-color0);
  --jp-cell-editor-active-border-color: var(--jp-brand-color1);

  --jp-cell-prompt-width: 64px;
  --jp-cell-prompt-font-family: 'Source Code Pro', monospace;
  --jp-cell-prompt-letter-spacing: 0px;
  --jp-cell-prompt-opacity: 1;
  --jp-cell-prompt-not-active-opacity: 0.5;
  --jp-cell-prompt-not-active-font-color: var(--md-grey-700);
  /* A custom blend of MD grey and blue 600
   * See https://meyerweb.com/eric/tools/color-blend/#546E7A:1E88E5:5:hex */
  --jp-cell-inprompt-font-color: #307fc1;
  /* A custom blend of MD grey and orange 600
   * https://meyerweb.com/eric/tools/color-blend/#546E7A:F4511E:5:hex */
  --jp-cell-outprompt-font-color: #bf5b3d;

  /* Notebook specific styles */

  --jp-notebook-padding: 10px;
  --jp-notebook-select-background: var(--jp-layout-color1);
  --jp-notebook-multiselected-color: var(--md-blue-50);

  /* The scroll padding is calculated to fill enough space at the bottom of the
  notebook to show one single-line cell (with appropriate padding) at the top
  when the notebook is scrolled all the way to the bottom. We also subtract one
  pixel so that no scrollbar appears if we have just one single-line cell in the
  notebook. This padding is to enable a 'scroll past end' feature in a notebook.
  */
  --jp-notebook-scroll-padding: calc(
    100% - var(--jp-code-font-size) * var(--jp-code-line-height) -
      var(--jp-code-padding) - var(--jp-cell-padding) - 1px
  );

  /* Rendermime styles */

  --jp-rendermime-error-background: #fdd;
  --jp-rendermime-table-row-background: var(--md-grey-100);
  --jp-rendermime-table-row-hover-background: var(--md-light-blue-50);

  /* Dialog specific styles */

  --jp-dialog-background: rgba(0, 0, 0, 0.25);

  /* Console specific styles */

  --jp-console-padding: 10px;

  /* Toolbar specific styles */

  --jp-toolbar-border-color: var(--jp-border-color1);
  --jp-toolbar-micro-height: 8px;
  --jp-toolbar-background: var(--jp-layout-color1);
  --jp-toolbar-box-shadow: 0px 0px 2px 0px rgba(0, 0, 0, 0.24);
  --jp-toolbar-header-margin: 4px 4px 0px 4px;
  --jp-toolbar-active-background: var(--md-grey-300);

  /* Input field styles */

  --jp-input-box-shadow: inset 0 0 2px var(--md-blue-300);
  --jp-input-active-background: var(--jp-layout-color1);
  --jp-input-hover-background: var(--jp-layout-color1);
  --jp-input-background: var(--md-grey-100);
  --jp-input-border-color: var(--jp-border-color1);
  --jp-input-active-border-color: var(--jp-brand-color1);
  --jp-input-active-box-shadow-color: rgba(19, 124, 189, 0.3);

  /* General editor styles */

  --jp-editor-selected-background: #d9d9d9;
  --jp-editor-selected-focused-background: #d7d4f0;
  --jp-editor-cursor-color: var(--jp-ui-font-color0);

  /* Code mirror specific styles */

  --jp-mirror-editor-keyword-color: #008000;
  --jp-mirror-editor-atom-color: #88f;
  --jp-mirror-editor-number-color: #080;
  --jp-mirror-editor-def-color: #00f;
  --jp-mirror-editor-variable-color: var(--md-grey-900);
  --jp-mirror-editor-variable-2-color: #05a;
  --jp-mirror-editor-variable-3-color: #085;
  --jp-mirror-editor-punctuation-color: #05a;
  --jp-mirror-editor-property-color: #05a;
  --jp-mirror-editor-operator-color: #aa22ff;
  --jp-mirror-editor-comment-color: #408080;
  --jp-mirror-editor-string-color: #ba2121;
  --jp-mirror-editor-string-2-color: #708;
  --jp-mirror-editor-meta-color: #aa22ff;
  --jp-mirror-editor-qualifier-color: #555;
  --jp-mirror-editor-builtin-color: #008000;
  --jp-mirror-editor-bracket-color: #997;
  --jp-mirror-editor-tag-color: #170;
  --jp-mirror-editor-attribute-color: #00c;
  --jp-mirror-editor-header-color: blue;
  --jp-mirror-editor-quote-color: #090;
  --jp-mirror-editor-link-color: #00c;
  --jp-mirror-editor-error-color: #f00;
  --jp-mirror-editor-hr-color: #999;

  /* Vega extension styles */

  --jp-vega-background: white;

  /* Sidebar-related styles */

  --jp-sidebar-min-width: 180px;

  /* Search-related styles */

  --jp-search-toggle-off-opacity: 0.5;
  --jp-search-toggle-hover-opacity: 0.8;
  --jp-search-toggle-on-opacity: 1;
  --jp-search-selected-match-background-color: rgb(245, 200, 0);
  --jp-search-selected-match-color: black;
  --jp-search-unselected-match-background-color: var(
    --jp-inverse-layout-color0
  );
  --jp-search-unselected-match-color: var(--jp-ui-inverse-font-color0);

  /* Icon colors that work well with light or dark backgrounds */
  --jp-icon-contrast-color0: var(--md-purple-600);
  --jp-icon-contrast-color1: var(--md-green-600);
  --jp-icon-contrast-color2: var(--md-pink-600);
  --jp-icon-contrast-color3: var(--md-blue-600);
}
</style>

<style type="text/css">
a.anchor-link {
   display: none;
}
.highlight  {
    margin: 0.4em;
}

/* Input area styling */
.jp-InputArea {
    overflow: hidden;
}

.jp-InputArea-editor {
    overflow: hidden;
}

@media print {
  body {
    margin: 0;
  }
}
</style>



<!-- Load mathjax -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.7/latest.js?config=TeX-MML-AM_CHTML-full,Safe"> </script>
    <!-- MathJax configuration -->
    <script type="text/x-mathjax-config">
    init_mathjax = function() {
        if (window.MathJax) {
        // MathJax loaded
            MathJax.Hub.Config({
                TeX: {
                    equationNumbers: {
                    autoNumber: "AMS",
                    useLabelIds: true
                    }
                },
                tex2jax: {
                    inlineMath: [ ['$','$'], ["\\(","\\)"] ],
                    displayMath: [ ['$$','$$'], ["\\[","\\]"] ],
                    processEscapes: true,
                    processEnvironments: true
                },
                displayAlign: 'center',
                CommonHTML: {
                    linebreaks: { 
                    automatic: true 
                    }
                },
                "HTML-CSS": {
                    linebreaks: { 
                    automatic: true 
                    }
                }
            });
        
            MathJax.Hub.Queue(["Typeset", MathJax.Hub]);
        }
    }
    init_mathjax();
    </script>
    <!-- End of mathjax configuration --></head>
<body class="jp-Notebook" data-jp-theme-light="true" data-jp-theme-name="JupyterLab Light">

<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>CMSC320 Final Tutorial</p>
<h1 id="Penguins,-Penguins,-and-Penguins">Penguins, Penguins, and Penguins<a class="anchor-link" href="#Penguins,-Penguins,-and-Penguins">&#182;</a></h1><p>Sharon Zheng and Meisheng Liu</p>

</div>
</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h2 id="Introduction">Introduction<a class="anchor-link" href="#Introduction">&#182;</a></h2><p>In this tutorial, we would like to see if we are able to classify a Penguin's species and sex through data collected from the penguin's such as the length of their flippers, bill(their beak), and body mass.</p>
<p>The dataset that we're using is the Palmer Penguin's dataset created by Allison Horst, Alison Hill, and Kristen Gorman. This dataset is made publicly available as a R default dataset as a feasible alternative to the Iris dataset for data visualization and analysis since the Iris dataset is used by many others for data visualization and analysis.</p>
<p><br></p>
<p>There are three types of penguins in this dataset: Adelie, Gentoo, and Chinstrap. There are also three major islands where the penguins are observed to be living at in Palmer Archipelago, Antarctica: Torgersen, Biscoe, and Dream island. We will give a brief background on each of them.</p>
<p>Adelie penguins got their name from the wife of a French explorer in 1830 named Adèlie. Adelie penguins usually inhabit rocky beaches along the coastline of Antarctica and offshore islands. They are migratory animals that are found on large ice platforms on coastal areas during winter. When breeding season comes, the penguins would start moving towards the seashore to look for ice-free areas, and that's where they'll construct their nests. Krill, silverfish, squid, and crustaceans are the major diets for Adelie penguins.</p>
<p>Gentoo penguins live in ice-free areas such as flat, rocky beaches and low-lying cliffs in order to perform large gatherings between individuals. Just like Adelie penguins, Gentoo penguins primarily feed on crustaceans, squid and fish. Gentoo penguins usually mate with the same partner every year, and unlike other penguin species, Gentoo penguins breed two children a year as opposed to one.</p>
<p>Chinstrap penguins usually live on large icebergs in the ocean with large colonies, they are also the most numerous penguins in the world. Chinstrap penguins primarily feed on krill, fish, crustaceans, and small shoaling animals. They are fast swimmers, swimming around 30 kph (18 mph). They can also "fly" using their flippers just like other penguins, and can go at a speed of 20 miles per hour.</p>
<p>Torgersen Island is an island that is roughly circular and about 400m across in diameter. This island slopes upward and also has a rocky shoreline. A variety of mosses and two flowering plants in Antarctica grow on Torgersen Island as well.</p>
<p>Dream Island is an island located to the south-east of Cape Monaco. It contains beautiful natural features such as a cave, and even a small waterfall and grasses during the summer.</p>
<p>Biscoe island, unlike the other two, is a series of islands, lying parallel to the west coast of Graham Land. These islands are named after John Biscoe, a British commander who explored these islands in 1832.</p>
<p><br></p>
<p>Since these three species are closely related to each other, they all look very similar to each other, have similar diets, and live in similar habitats. Therefore we would like to see if there are any differences in their characteristics such as bills and flippers, and if we could identify which species it is by looking at the difference in their body mass, bills, flippers. Additionally we would also like to see if it is possible for us to identify the penguin's sex for each species.</p>
<p><br></p>
<p><strong>Libraries and Packages that we used:</strong></p>
<p>Palmerpenguins: the package that includes data for Palmer Penguins</p>
<p>Pandas: Used to create a dataframe where all our data can be accessed</p>
<p>Matplotlib: Used to create scatter plots</p>
<p>Numpy: Used to create regression lines for the scatter plots</p>
<p>Seaborn: Used to create plots for data visualization and analysis</p>

</div>
</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h2 id="Data-Collection-and-Data-Cleaning">Data Collection and Data Cleaning<a class="anchor-link" href="#Data-Collection-and-Data-Cleaning">&#182;</a></h2><p>Here, we are using the palmerpenguins dataset created by Allison Horst, Alison Hill, and Kristen Gorman. It is originally provided as an R package, but we also found that it is availible as a python package after some exploration. We also import some libraries and packages that will be used to assist us in data exploration, data visualization and machine learning here.</p>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[&nbsp;]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-python"><pre><span></span><span class="err">!</span><span class="n">pip</span> <span class="n">install</span> <span class="n">palmerpenguins</span>
<span class="kn">import</span> <span class="nn">pandas</span> <span class="k">as</span> <span class="nn">pd</span>
<span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>
<span class="kn">import</span> <span class="nn">seaborn</span> <span class="k">as</span> <span class="nn">sns</span> 
<span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>
<span class="kn">from</span> <span class="nn">palmerpenguins</span> <span class="kn">import</span> <span class="n">load_penguins</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>


<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain">
<pre>Collecting palmerpenguins
  Downloading palmerpenguins-0.1.4-py3-none-any.whl (17 kB)
Requirement already satisfied: pandas in /usr/local/lib/python3.7/dist-packages (from palmerpenguins) (1.1.5)
Requirement already satisfied: numpy in /usr/local/lib/python3.7/dist-packages (from palmerpenguins) (1.19.5)
Requirement already satisfied: pytz&gt;=2017.2 in /usr/local/lib/python3.7/dist-packages (from pandas-&gt;palmerpenguins) (2018.9)
Requirement already satisfied: python-dateutil&gt;=2.7.3 in /usr/local/lib/python3.7/dist-packages (from pandas-&gt;palmerpenguins) (2.8.2)
Requirement already satisfied: six&gt;=1.5 in /usr/local/lib/python3.7/dist-packages (from python-dateutil&gt;=2.7.3-&gt;pandas-&gt;palmerpenguins) (1.15.0)
Installing collected packages: palmerpenguins
Successfully installed palmerpenguins-0.1.4
</pre>
</div>
</div>

</div>

</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>After loading the dataset into a dataframe, we can see that there are some NaN values. We examined the dataset and decided to drop the rows that contains a NaN value, since there are only a few of those and we still have a viable set of data to work with.</p>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[&nbsp;]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-python"><pre><span></span><span class="n">penguins</span> <span class="o">=</span> <span class="n">load_penguins</span><span class="p">()</span>
<span class="n">pd</span><span class="o">.</span><span class="n">set_option</span><span class="p">(</span><span class="s1">&#39;display.max_rows&#39;</span><span class="p">,</span> <span class="kc">None</span><span class="p">)</span>
<span class="n">penguins</span> <span class="o">=</span> <span class="n">penguins</span><span class="o">.</span><span class="n">dropna</span><span class="p">()</span>
<span class="n">penguins</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[&nbsp;]:</div>



<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/html">

  <div id="df-12b2806a-e82b-4742-ba5b-750dea71f350">
    <div class="colab-df-container">
      <div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>species</th>
      <th>island</th>
      <th>bill_length_mm</th>
      <th>bill_depth_mm</th>
      <th>flipper_length_mm</th>
      <th>body_mass_g</th>
      <th>sex</th>
      <th>year</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Adelie</td>
      <td>Torgersen</td>
      <td>39.1</td>
      <td>18.7</td>
      <td>181.0</td>
      <td>3750.0</td>
      <td>male</td>
      <td>2007</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Adelie</td>
      <td>Torgersen</td>
      <td>39.5</td>
      <td>17.4</td>
      <td>186.0</td>
      <td>3800.0</td>
      <td>female</td>
      <td>2007</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Adelie</td>
      <td>Torgersen</td>
      <td>40.3</td>
      <td>18.0</td>
      <td>195.0</td>
      <td>3250.0</td>
      <td>female</td>
      <td>2007</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Adelie</td>
      <td>Torgersen</td>
      <td>36.7</td>
      <td>19.3</td>
      <td>193.0</td>
      <td>3450.0</td>
      <td>female</td>
      <td>2007</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Adelie</td>
      <td>Torgersen</td>
      <td>39.3</td>
      <td>20.6</td>
      <td>190.0</td>
      <td>3650.0</td>
      <td>male</td>
      <td>2007</td>
    </tr>
  </tbody>
</table>
</div>
      <button class="colab-df-convert" onclick="convertToInteractive('df-12b2806a-e82b-4742-ba5b-750dea71f350')"
              title="Convert this dataframe to an interactive table."
              style="display:none;">
        
  <svg xmlns="http://www.w3.org/2000/svg" height="24px"viewBox="0 0 24 24"
       width="24px">
    <path d="M0 0h24v24H0V0z" fill="none"/>
    <path d="M18.56 5.44l.94 2.06.94-2.06 2.06-.94-2.06-.94-.94-2.06-.94 2.06-2.06.94zm-11 1L8.5 8.5l.94-2.06 2.06-.94-2.06-.94L8.5 2.5l-.94 2.06-2.06.94zm10 10l.94 2.06.94-2.06 2.06-.94-2.06-.94-.94-2.06-.94 2.06-2.06.94z"/><path d="M17.41 7.96l-1.37-1.37c-.4-.4-.92-.59-1.43-.59-.52 0-1.04.2-1.43.59L10.3 9.45l-7.72 7.72c-.78.78-.78 2.05 0 2.83L4 21.41c.39.39.9.59 1.41.59.51 0 1.02-.2 1.41-.59l7.78-7.78 2.81-2.81c.8-.78.8-2.07 0-2.86zM5.41 20L4 18.59l7.72-7.72 1.47 1.35L5.41 20z"/>
  </svg>
      </button>
      
  <style>
    .colab-df-container {
      display:flex;
      flex-wrap:wrap;
      gap: 12px;
    }

    .colab-df-convert {
      background-color: #E8F0FE;
      border: none;
      border-radius: 50%;
      cursor: pointer;
      display: none;
      fill: #1967D2;
      height: 32px;
      padding: 0 0 0 0;
      width: 32px;
    }

    .colab-df-convert:hover {
      background-color: #E2EBFA;
      box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);
      fill: #174EA6;
    }

    [theme=dark] .colab-df-convert {
      background-color: #3B4455;
      fill: #D2E3FC;
    }

    [theme=dark] .colab-df-convert:hover {
      background-color: #434B5C;
      box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);
      filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));
      fill: #FFFFFF;
    }
  </style>

      <script>
        const buttonEl =
          document.querySelector('#df-12b2806a-e82b-4742-ba5b-750dea71f350 button.colab-df-convert');
        buttonEl.style.display =
          google.colab.kernel.accessAllowed ? 'block' : 'none';

        async function convertToInteractive(key) {
          const element = document.querySelector('#df-12b2806a-e82b-4742-ba5b-750dea71f350');
          const dataTable =
            await google.colab.kernel.invokeFunction('convertToInteractive',
                                                     [key], {});
          if (!dataTable) return;

          const docLinkHtml = 'Like what you see? Visit the ' +
            '<a target="_blank" href=https://colab.research.google.com/notebooks/data_table.ipynb>data table notebook</a>'
            + ' to learn more about interactive tables.';
          element.innerHTML = '';
          dataTable['output_type'] = 'display_data';
          await google.colab.output.renderOutput(dataTable, element);
          const docLink = document.createElement('div');
          docLink.innerHTML = docLinkHtml;
          element.appendChild(docLink);
        }
      </script>
    </div>
  </div>
  
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h2 id="Exploratory-Analysis-and-Data-Visualization">Exploratory Analysis and Data Visualization<a class="anchor-link" href="#Exploratory-Analysis-and-Data-Visualization">&#182;</a></h2><h3 id="Exploring-the-Spread-and-Frequency-of-the-Penguins-Among-the-Islands">Exploring the Spread and Frequency of the Penguins Among the Islands<a class="anchor-link" href="#Exploring-the-Spread-and-Frequency-of-the-Penguins-Among-the-Islands">&#182;</a></h3>
</div>
</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>First, let's see how the three penguin species are spread across the three islands by using a simple strip plot. The three penguin species are color coded, and we can see that Adelie penguins are found in all three islands. Gentoo penguins are concentrated in Biscoe island, while Chinstrap penguins are concentrated in Dream island.</p>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[&nbsp;]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-python"><pre><span></span><span class="n">stripplot</span> <span class="o">=</span> <span class="n">sns</span><span class="o">.</span><span class="n">stripplot</span><span class="p">(</span><span class="n">data</span><span class="o">=</span><span class="n">penguins</span><span class="p">,</span> <span class="n">x</span><span class="o">=</span><span class="s2">&quot;island&quot;</span><span class="p">,</span> <span class="n">y</span><span class="o">=</span><span class="n">penguins</span><span class="o">.</span><span class="n">index</span><span class="p">,</span> <span class="n">hue</span><span class="o">=</span><span class="s2">&quot;species&quot;</span><span class="p">,</span> <span class="n">jitter</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">stripplot</span><span class="o">.</span><span class="n">set</span><span class="p">(</span><span class="n">xlabel</span> <span class="o">=</span> <span class="s1">&#39;Island&#39;</span><span class="p">,</span> <span class="n">ylabel</span> <span class="o">=</span> <span class="s1">&#39;Species&#39;</span><span class="p">,</span> <span class="n">title</span> <span class="o">=</span> <span class="s1">&#39;Species across Islands&#39;</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[&nbsp;]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>[Text(0, 0.5, &#39;Species&#39;),
 Text(0.5, 0, &#39;Island&#39;),
 Text(0.5, 1.0, &#39;Species across Islands&#39;)]</pre>
</div>

</div>

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>




<div class="jp-RenderedImage jp-OutputArea-output ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>Then, we will also like to check the number of each species in the dataset and if the number of males and females are roughly even.</p>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[&nbsp;]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-python"><pre><span></span><span class="n">countplot</span> <span class="o">=</span> <span class="n">sns</span><span class="o">.</span><span class="n">countplot</span><span class="p">(</span><span class="n">data</span><span class="o">=</span><span class="n">penguins</span><span class="p">,</span> <span class="n">x</span><span class="o">=</span><span class="s1">&#39;species&#39;</span><span class="p">,</span> <span class="n">hue</span><span class="o">=</span><span class="s1">&#39;sex&#39;</span><span class="p">)</span>
<span class="n">countplot</span><span class="o">.</span><span class="n">set</span><span class="p">(</span><span class="n">title</span> <span class="o">=</span> <span class="s1">&#39;Number of Penguins for each Species&#39;</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[&nbsp;]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>[Text(0.5, 1.0, &#39;Number of Penguins for each Species&#39;)]</pre>
</div>

</div>

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>




<div class="jp-RenderedImage jp-OutputArea-output ">
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAYUAAAEcCAYAAAAoSqjDAAAABHNCSVQICAgIfAhkiAAAAAlwSFlzAAALEgAACxIB0t1+/AAAADh0RVh0U29mdHdhcmUAbWF0cGxvdGxpYiB2ZXJzaW9uMy4yLjIsIGh0dHA6Ly9tYXRwbG90bGliLm9yZy+WH4yJAAAgAElEQVR4nO3de3zP9f//8dv7/Z7NYZjNNnMIESZhjJFJJk2zqBzzo09UIqNynENzpiHlmFT0kT6fcpYhkhxyTGjJR6KZYowNGXZ8v35/7Ov1aR+Tje094369XLpcer8Oz9fj9XrN+/5+PV/v9/NlMQzDQEREBLAWdAEiInL3UCiIiIhJoSAiIiaFgoiImBQKIiJiUiiIiIhJoSBZhIeH8+677xbItg3DYPjw4TRq1IiOHTsWSA259eWXX9KrV688b/frr7+mRYsW+Pn5cfjw4TxvPy+sWLGC559/vqDL+Ftt27Zlz549BV1GoaJQuMsFBQXRtGlTrl69ak5bunQpPXr0KMCq8scPP/zAjh072Lp1K8uWLbth/ooVK/D19cXPz48GDRrQvn17vv322wKo9L/atWvHggUL8rzdyMhI3nrrLQ4cOEDt2rXzvP2CsG/fPrp27UrDhg1p3LgxXbt2JTo6Ol+3uXbtWgICAvJ1G/cahUIhYLfbWbRoUUGXkWsZGRm5Wv7UqVNUqFCB4sWL33SZ+vXrc+DAAfbt20fHjh154403uHTp0p2Wetc5ffo0Dz300G2tm9vj7ghJSUn06dOH7t27s3fvXrZt20ZYWBjOzs4FXZr8D4VCIfDSSy+xYMEC/vzzzxvm/fHHH9SsWZP09HRzWo8ePVi6dCmQ+em6a9euTJo0CX9/f1q1asX+/ftZsWIFLVq0oGnTpqxcuTJLmxcuXKBnz574+fnRvXt3Tp06Zc47fvw4PXv2pHHjxgQHB7Nu3TpzXnh4OKNHj+aVV16hfv362V62nz17lj59+tC4cWNat27NkiVLgMyrn1GjRnHw4EH8/PyYOXPm3x4Tq9VKhw4dSE5O5uTJk6SmphIZGcnjjz/Oo48+SkREBMnJyQDs2bOHxx57jAULFtC0aVMCAwNZvnx5lv3t06cPDRo0oEOHDrz77rtmt0hOju9fu1Bq1qzJv//9b5588kn8/f0ZO3Ys1wcNiI2NpXv37jRs2JCAgADeeOONG/YrNTUVPz8/MjIyaN++PU888YR53Hv06IG/vz9t27blm2++ydVxv3z5MiNGjCAwMJDmzZvz7rvvmuFx8uRJXnjhBQICAggICGDQoEFZ/tbi4uIICwujSZMmBAQEMG7cuCxtR0ZG0qhRI4KCgti6dWu25ysmJgaA0NBQbDYbRYsWJTAwkFq1apnHsWvXrowbN46GDRvSpk0bdu3alaP6AZYsWcJTTz2Fn58fISEh/Pzzz0DmlfbOnTuBzA9X8+fP54knniAgIIDXX3+dixcvApCSksLgwYMJCAjA39+fDh06cP78+Wz35V6nUCgE6tSpQ+PGjfn4449va/3o6Ghq1qzJnj17CA0NZeDAgfz00098/fXXTJ06lXHjxnHlyhVz+TVr1vDaa6+xZ88eatWqxeDBgwG4evUqvXr1IjQ0lJ07d/Luu+8yduxYjh07Zq4bFRVFnz592L9/Pw0bNryhloEDB1KuXDm2b9/OzJkzmT59Ort27aJTp06MHTvWvBIYMGDA3+5Teno6S5cupXjx4lSpUoVp06YRExPDqlWr2LhxI/Hx8cyZM8dc/vz581y+fJlt27YxceJExo0bZ15hjBs3jmLFirFjxw4iIyNZtWrVbR3n67Zs2cKyZcv48ssvWb9+Pdu3bwdgxowZNGvWjO+//55t27bRvXv3G9Z1dnbmwIEDAKxevZpNmzaRlpZGnz59aNasGTt37mTUqFEMHjyY3377zVzvVsc9PDwcJycnNm7cyKpVq9ixY4cZbIZh8Oqrr7J9+3bWr1/PmTNnmDVrFpB51fHqq69Svnx5Nm/ezLZt2wgJCTHbjY6OpmrVquzevZuXX36ZkSNHkt3IOVWrVsVmszFs2DC2bt2a7dVddHQ0DzzwALt372bAgAGEhYWZb9p/V//69euZNWsWkZGR7N+/n/fffx83N7cb2v/000/ZtGkTixcvZvv27ZQuXdoMuJUrV5KUlMSWLVvYs2cPY8eOpWjRotmd3nueQqGQGDBgAIsXLyYxMTHX61asWJEOHTpgs9kICQkhLi6Ofv364ezsTGBgIM7Ozpw8edJc/vHHH6dRo0Y4Ozvz5ptvcvDgQeLi4tiyZQsVKlSgQ4cOODk5Ubt2bYKDg/nqq6/MdVu1akXDhg2xWq24uLhkqSMuLo79+/czePBgXFxc8PX1pVOnTqxevTrH+/Ljjz/i7+9Ps2bNWLt2LXPmzMHV1ZUlS5YwYsQI3NzccHV15dVXX2Xt2rXmek5OTvTr148iRYrQokULihcvTkxMDBkZGWzcuJH+/ftTrFgxqlevzjPPPJPrY/xXr7zyCqVKlaJ8+fIEBARw5MgRs4bTp08THx+Pi4sL/v7+Od7nq1ev0rt3b5ydnWnatCktW7bMsn9/d9zPnz/P1q1bGTFiBMWLF8fDw4MXX3zRXL9y5co0a9YMZ2dn3N3d6dmzJ99//z2Q+UYdHx/P0KFDKV68+A11ly9fns6dO2Oz2Xj22Wc5d+5ctp+wXV1d+de//oXFYuGtt96iadOm9OnTJ8uy7u7u/OMf/6BIkSKEhIRQtWpVtmzZcsv6ly1bxssvv0zdunWxWCxUrlyZChUq3FDD559/zptvvkm5cuVwdnYmLCyMDRs2kJ6ejpOTExcvXiQ2NhabzUadOnVwdXXN0fm51zgVdAGSMzVq1ODxxx9n/vz5VKtWLVfrenh4mP9//dNP2bJlzWkuLi5ZrhTKlStn/n+JEiUoXbo08fHxnDp1iujo6CxvChkZGbRr18587ePjc9M64uPjKV26dJZ/bOXLl+fQoUM53pd69erx73//O8u0hIQErl27xnPPPWdOMwwDu91uvnZzc8PJ6b9/7sWKFePq1askJiaSnp6epe6/24ec8PT0zLKd68d2yJAhzJgxg44dO1K6dGl69uyZo29ZxcfHU65cOazW/36GK1++PGfPns1RzadPnyY9PZ3AwEBzmt1uN9c5f/48EydOZN++fVy5cgXDMChVqhSQGeTly5fPcuz+6q9/R8WKFQPI8qWIv6pWrRpvv/02kNkdNmTIECZNmsT06dMB8Pb2xmKxZNnH+Pj4W9YfFxfHAw88cNP9/+tx6NevX5bjaLVaSUhIoH379pw5c4aBAwfy559/0q5dO958802KFClyy3bvNQqFQmTAgAE8++yzWb4Cef2mbHJysvlme+7cuTvazpkzZ8z/v3LlCpcuXcLLywsfHx8aNWrEwoULb6tdLy8vLl26RFJSkllrXFwc3t7ed1RvmTJlKFq0KGvXrs11W+7u7jg5OXHmzBmqVq1q1nRdXh5fT09PJkyYAGR+E6dnz540atSIypUr/+16Xl5enDlzBrvdbr6hxcXFUaVKlRxt9/on4927d2f75j59+nQsFgtr1qzBzc2NTZs2md0qPj4+xMXFmZ+m80q1atV47rnn+OKLL8xpZ8+exTAMMxji4uIICgq6Zf0+Pj5ZrnRvply5ckyaNCnb7jWAsLAwwsLC+OOPP+jduzdVq1alU6dOt7mHhZe6jwqRypUrExISwqeffmpOc3d3x9vbm9WrV5ORkcGyZcv4/fff72g7W7duZd++faSmpjJjxgzq1auHj48Pjz/+OCdOnGDVqlWkpaWRlpZGdHQ0x48fz1G7Pj4++Pn5MX36dFJSUjhy5AjLli3LcqVxO6xWK506dWLSpEkkJCQAmW8w1/vy/47NZqN169bMnj2ba9eucfz48SzdWXl5fK/31wOULl0ai8WS5VPrzdStW5eiRYvy0UcfkZaWxp49e9i8eXOWvv2/4+XlRbNmzXj77bdJSkrCbrdz8uRJ9u7dC2QGf/HixSlZsiRnz57lo48+yrJtT09P3nnnHa5evUpKSgo//PBDrvf9+PHjLFiwwNz/uLg4oqKiqFevnrlMYmIiixYtIi0tjfXr13P8+HFatGhxy/o7duzIggULOHToEIZhEBsbm+XLEdc9//zzvPfee+a8xMRENm3aBMDu3bv55ZdfyMjIwNXVFScnpxydm3vR/bnXhVi/fv1uuDwfP348H3/8MQEBARw7dgw/P7872kZoaChz5swhICCAn3/+malTpwKZ/cIff/wx69ato3nz5gQGBjJt2jRSU1Nz3Pb06dM5deoUzZs3JywsjP79+/Poo4/eUb2Q2TVTuXJlOnfuTIMGDXjxxRfNb7zcSkREBJcvX6ZZs2YMHTqUtm3bZvmqZF4d359++olOnTrh5+dH3759GTlyJJUqVbrles7OzsybN49t27bRpEkTxo4dy5QpU3LVjThlyhTS0tIICQmhUaNGDBgwwLziCQsL4/Dhw/j7+9O7d2+efPJJcz2bzca8efOIjY2lZcuWPPbYY6xfvz7X++7q6sqPP/5Ip06dqF+/Pp07d6ZGjRqEh4eby9StW5fY2FiaNGnCe++9x8yZMylTpswt63/qqafo06cPgwYNokGDBvTr1y/bG9kvvPACQUFB9OrVCz8/Pzp37mz+TuL8+fMMGDCAhg0bEhISQuPGjWnfvn2u9/NeYNFDdkSymjp1KufPnycyMrKgS7lvrFixgqVLl95wv0gcT1cKct87fvw4R44cwTAMoqOjWbZsGa1bty7oskQKhG40y33vypUrDBo0iPj4eDw8POjVqxetWrUq6LJECoS6j0RExKTuIxERMSkURETEpFAQERHTPXGj+cKFK9jtujUiIpITVquFMmVKZDvvnggFu91QKIiI5AF1H4mIiEmhICIipnui+0hE7n2GYXDhwjlSU5MBdRffmgVn56KUKeOZZUjyW1EoiEihkJR0CYvFgrd3RSwWdXLcimHYuXjxPElJlyhZ8sYn0d2MjqyIFArXriVRsqSbAiGHLBYrJUuW4dq1pFytp6MrIoWC3Z6BzabOjdyw2Zyw2zNytY5CQUQKjdz0jcvtHa/7KnZdSxWlmEvheuaqPS0Za5GiBV1GjmWkJpN4Ka2gyxCR23RfhUIxlyI0HLKooMvIlR+mvsDJcY8UdBk59kDET4BCQaSwUveRiIiYFAoiIn9j8eJPeOaZp2jd+jGef/459u3bi91u59NPP6Fz5/aEhLTirbfC+fPPzOdCT5s2mZEjh5jrz507k9df70theXSNQkFE5CZOnjzBihVL+eijRXz99TamT5+Nj095li37gu3btzB79nxWrVpPyZIleeedzGd6h4W9yfHjx1m3bg0//niAtWtXM3LkmEJzk9wh9xT++OMP+vXrZ76+fPkySUlJ7N27l5iYGMLDw7l48SJubm5ERkZSpUoVR5QlIvK3rFYbqampxMT8hptbGXx8ygOwevVy3nxzKF5e3gD06vUqHTq0JT09naJFi/LWW+MYPHgAxYsX5403hpjLFQYOCYWKFSuyevVq8/XEiRPJyMj87uzo0aPp1q0b7du3Z/Xq1URERLBoUeG6GSwi96aKFSsxYMAgFiyYT0zMbwQENKF//4GcORPHiBFDsFr/++nfZrNx4UIinp5ePPxwHcqXr8CFC4kEBbUuwD3IPYd3H6WmprJmzRo6dOhAQkIChw8fJjQ0FIDQ0FAOHz5MYmKio8sSEcnWk0+24f33P2b58jWAhfffn4mXlzfTps3gq6+2mP9t3rwTT08vAJYvX0JaWiply3ryr38Vrg+5Dg+FzZs34+3tzcMPP0xcXBze3t7YbDYgM2m9vLyIi4tzdFkiIjc4efIEP/zwPampqTg7u+Di4oLFYuWZZzowf/5czpzJfK+6cOEC27dv+b91Yvnww/d5663xvPXWOD77bBG//vpLAe5F7jj8dwrLly+nQ4cOedqmh4drnrYnd8bTs2RBlyD3oPh4K05Ojv0cm5GRzgcfzObEiRicnJx45JG6hIe/hYeHBxaLhYEDwzh//hxlyrjzxBOtad78MSZMiOCFF17E17cWAH37hjFhwmgWLlyMs7OzQ+sHsFqtufo3aTEc+D2ps2fPEhwczLfffkuZMmVISEggODiYPXv2YLPZyMjIICAggI0bN+Lu7p7jdhMSknL05DVPz5L68Vo+eyDiJ86du1zQZcg96MyZWMqVq1zQZRQ62R03q9Vy0w/TDo3dlStX0qJFC8qUKQOAh4cHvr6+REVFARAVFYWvr2+uAkFERPKOw0Phf7uOxowZw+LFiwkODmbx4sWMHTvWkSWJiMhfOPSewoYNG26YVq1aNZYuXerIMkRE5Cb0i2YRETEpFERExKRQEBERk0JBRERMCgURETHdV09eE5F7R349XvdaShpJfybnebvZ+fjjD7h27RphYW84ZHs5oVAQkUIpvx6v+8PUF0jCMaFwN1IoiIjchsBAf155pS/bt2/l0qVLDBs2kn379rJnz07S09MZPz6SKlWqkpBwnjFjRnLlyhVSU1N59NFmvPba69m2uXjxJ2zdupmMjAzKlvVi2LCReHiUdeh+6Z6CiMhtcnUtyUcfLaJv3/4MHz6IRx6px8KF/6JNm7YsWrTAXCYy8l0WLFjMJ5/8iyNH/sPu3TtvaGvDhnWcOnWKDz74hAULPqNp02bMnv2eo3dJVwoiIrerVasnAahZsxZgoVmz5v/32petW78FwG63M3fuDH76KRowSEhI4Ndfj9KkyaNZ2vruu20cOfIfevXqDmSO0Orq6vgRoBUKIiK36fpQ2FarFWfn/970tlqt5tMlv/jiMy5f/pP58z/BxcWFyMiJpKam3NCWYRj84x+9CA1t75jib0LdRyIi+ejy5ct4eJTFxcWFc+fi+e67rdkuFxj4GCtXLuPPP/8EMp9S+euvRx1ZKqArBREppK6lpPHD1Bfypd281KlTV956axg9enTG09Obhg0bZbtcmzZtuXTpIv379wYyu52efbYTDz1UI0/ruRWHPmQnv+ghO3cPPWRH8osesnN77uqH7IiIyN1NoSAiIiaFgoiImBQKIiJiUiiIiIjJYV9JTUlJYdKkSezatQsXFxfq16/P+PHjiYmJITw8nIsXL+Lm5kZkZCRVqlRxVFkiIvIXDguFqVOn4uLiwoYNG7BYLJw/fx6A0aNH061bN9q3b8/q1auJiIhg0aLC9bVRyX/5NUxyfnLkEMz3I/fSRbA5F83zdjNSk0m8lLPfKmzbtoUPPpiNs7MzY8dO4oEHquR5PddNnDiGWrV86dChS75tAxwUCleuXGHVqlVs3boVi8UCQNmyZUlISODw4cMsXLgQgNDQUMaPH09iYiLu7u6OKE0KifwaJjk/3e9DMOc3m3PRfPkNzwMRPwE5C4XVq1fw0kt9CAp6Is/rKCgOCYXff/8dNzc3Zs+ezZ49eyhRogSvv/46RYsWxdvbG5vNBoDNZsPLy4u4uDiFgojc1WbOfIfo6AOcPBnLypVL6dOnP/PmzeLKlSsAvPxyHx59NJC4uNO8/HIPnn76Wfbs2UlKSgoRERNYvXo5hw8fwtnZhbfffgcPj7IcP36Md955m+Tka6SmptKu3bN07tzthm2npaUxf/5cDh78gdTUNKpXr86gQcMpXrz4He+XQ0IhIyOD33//ndq1azNs2DB+/PFH+vTpw4wZM/Kk/Zv9Mk8KhqdnyYIu4a6hY5F34uOtODk55rsxOdnOwIFD+PXXo/y//9eDevX86NevN9Onz6RsWU/Onz9Hz549+Ne/lmKzWbl06RJ+fn6EhQ1g8eJ/8sYbfZk790Nq1IhgypTJ/xcq/ahYsQKzZ8/D2dmZq1ev0qtXD5o2fZSqVR/EYrFgtVpwcrKyaNGnlCxZkoULFwMwe/YMPvvsE/r2DbuhTqvVmqu/Q4eEgo+PD05OToSGhgJQr149ypQpQ9GiRTl79iwZGRnYbDYyMjKIj4/Hx8cnV+3nZpgLyX/5McxFYT13GvIj79jtdtLT7Q7ZVk63YxgGGRkGBw8e4PTpU7zxRn9znsViITY2ltKl3ShWrDgBAc1IT7dTvXpNPD29ePDBh0hPt1OjRk2+/34P6el2rly5yuzZ73Hs2FEsFivnz5/jl19+oVKlKhiGgd1ukJ5uZ/v2LVy5coXNmzcBkJaWSvXqD2Vbt91uv+Hv8O+GuXBIKLi7uxMQEMCOHTsIDAwkJiaGhIQEqlSpgq+vL1FRUbRv356oqCh8fX3VdSQihYphQLVqDzFnzoc3zIuLO33DsNrOzi5/eW0zh9n+4IM5uLt7sGDBZzg5OfHmm/1ITU3NdnuDBoXfdHC9O+Gw3ymMHTuWDz74gKeffpqBAwcyZcoUSpUqxZgxY1i8eDHBwcEsXryYsWPHOqokEZE8UadOXf744yT79+8zp/3nPz+T2/FGk5Iu4+XljZOTE7/9dowffzyY7XKBgY/xxRefkZKS+UWGq1evcOJEzO3vwF847CuplSpV4tNPP71herVq1Vi6dKmjyhARyXOlSpXi7benM2fODGbMeIf09DTKl69AZOS7uWrnH/94ifHjI1i7djWVKj1A/fp+2S7XvfuLfPzxB7z88gtYrVbAQq9er1ClStU73hcNnX2X09DZmQrrudM9hbzzv0NA3w2/UygMcjt0th6yI5JPjPSUQneDvDC9IWbWWThqLUwUCiL5xOLkUqiu8iB3P9ySe5MGxBMREZNCQUQKjXvgFqhD3c7xUiiISKHg5OTMlSt/KhhyyDAMrlz5Eycn51ytp3sKIlIolCnjyYUL50hKuljQpRQaTk7OlCnjmbt18qkWEZE8ZbM5UbZs7obAkdxT95GIiJgUCiIiYlIoiIiISaEgIiImhYKIiJgUCiIiYlIoiIiISaEgIiImhYKIiJgUCiIiYlIoiIiISaEgIiImhw2IFxQUhLOzMy4uLgAMHjyY5s2bc/DgQSIiIkhJSaFChQpMnToVDw8PR5UlIiJ/4dBRUmfOnEmNGjXM13a7nSFDhjB58mT8/f2ZO3cu06ZNY/LkyY4sS0RE/k+Bdh8dOnQIFxcX/P39AejatStfffVVQZYkInJfc+iVwuDBgzEMg4YNGzJw4EDi4uIoX768Od/d3R273c7Fixdxc3PLcbseHq75Ua7cJk/PkgVdgtwBnb/7m8NC4bPPPsPHx4fU1FQmTpzIuHHjaN26dZ60nZCQhN1+60f06Y/dMc6du5znbercOU5+nD+5u1itlpt+mHZY95GPT+YTk5ydnenWrRv79+/Hx8eH06dPm8skJiZitVpzdZUgIiJ5xyGhcPXqVS5fzvz0YRgG69atw9fXlzp16pCcnMy+ffsA+Pzzz2nTpo0jShIRkWw4pPsoISGB/v37k5GRgd1up1q1aowePRqr1cqUKVMYPXp0lq+kiohIwXBIKFSqVIlVq1ZlO69BgwasWbPGEWWIiMgt6BfNIiJiUiiIiIhJoSAiIiaFgoiImBQKIiJiUiiIiIhJoSAiIiaFgoiImBQKIiJiUiiIiIhJoSAiIiaFgoiImBQKIiJiynEofPzxx9lOX7hwYZ4VIyIiBSvHoTBnzpxsp7///vt5VoyIiBSsWz5PYdeuXQDY7XZ2796NYfz3Wch//PEHJUqUyL/qRETEoW4ZCiNHjgQgJSWFESNGmNMtFguenp6MGjUq/6oTERGHumUobN68GYChQ4cyZcqUfC9IREQKTo4fx/nXQLDb7VnmWa36EpOIyL0gx+/mP//8M126dKF+/fo8/PDDPPzww9SuXZuHH344VxucPXs2NWvW5OjRowAcPHiQdu3aERwcTK9evUhISMjdHoiISJ7J8ZVCeHg4LVu2ZNKkSRQtWvS2Nvbzzz9z8OBBKlSoAGRecQwZMoTJkyfj7+/P3LlzmTZtGpMnT76t9kVE5M7k+Erh1KlTvPnmm1SrVo0KFSpk+S8nUlNTGTduHGPGjDGnHTp0CBcXF/z9/QHo2rUrX331Ve72QERE8kyOQ6F169Z89913t72hGTNm0K5dOypWrGhOi4uLo3z58uZrd3d37HY7Fy9evO3tiIjI7ctx91FKSgphYWE0bNiQsmXLZpl3q28lHThwgEOHDjF48ODbq/IWPDxc86VduT2eniULugS5Azp/97cch0L16tWpXr36bW3k+++/5/jx47Rq1QqAM2fO8NJLL9GjRw9Onz5tLpeYmIjVasXNzS1X7SckJGG3G7dcTn/sjnHu3OU8b1PnznHy4/zJ3cVqtdz0w3SOQyEsLOy2C+jduze9e/c2XwcFBTFv3jyqV6/OkiVL2LdvH/7+/nz++ee0adPmtrcjIiJ3JsehcH24i+w0bdr0tjZutVqZMmUKo0ePJiUlhQoVKjB16tTbaktERO5cjkPh+nAX1124cIG0tDS8vb355ptvcrXR67+SBmjQoAFr1qzJ1foiIpI/chwKf30jB8jIyOD999/XgHgiIveQ2x6fwmaz0adPHz766KO8rEdERArQHQ1atGPHDiwWS17VIiIiBSzH3UctWrTIEgDXrl0jNTWV0aNH50thIiLieDkOhf/9VlCxYsWoWrUqrq764ZiIyL0ix6HQuHFjIHMQu/Pnz1O2bFkNmS0ico/J8bt6UlISQ4cOpW7dujz22GPUrVuXYcOGcfmyfv0oInKvyHEoTJgwgWvXrrFmzRqio6NZs2YN165dY8KECflZn4iIOFCOu4+2b9/Opk2bKFasGABVq1Zl8uTJtG7dOt+KExERx8rxlYKLiwuJiYlZpl24cAFnZ+c8L0pERApGjq8UOnbsSK9evXjxxRcpX748p0+f5pNPPqFTp075WZ+IiDhQjkOhb9++eHt7s2bNGuLj4/Hy8uLll19WKIiI3ENyHAoTJ04kJCSETz75xJy2f/9+Jk6ceMNgeSIif+VaqijFXIoUdBm5Yk9Lxlrk9p5HXxAyUpNJvJR2x+3kOBSioqIYOnRolml16tShX79+CgUR+VvFXIrQcMiigi4jV36Y+gInxz1S0GXk2AMRPwF3Hgo5vtFssViw2+1ZpmVkZNwwTURECq8ch4K/vz8zZswwQ8ButzNr1iz8/f3zrTgREXGsXCnd52YAABOKSURBVD1k59VXXyUwMJDy5csTFxeHp6cn8+bNy8/6RETEgXIcCuXKlWPlypVER0cTFxeHj48PdevW1fhHIiL3kByHAmQ+U7l+/frUr18/v+oREZECpI/5IiJiytWVwp147bXX+OOPP7BarRQvXpy33noLX19fYmJiCA8P5+LFi7i5uREZGUmVKlUcVZaIiPyFw0IhMjKSkiVLArBp0yZGjBjBypUrGT16NN26daN9+/asXr2aiIgIFi0qXN9nFhG5Vzis++h6IEDmsxksFgsJCQkcPnyY0NBQAEJDQzl8+PANA++JiIhjOOxKATK/1rpjxw4Mw+Cjjz4iLi4Ob29vbDYbADabDS8vL+Li4nB3d89xux4eeiTo3cTTs+StF5K7ls5f4ZUX586hoTBx4kQAVq1axZQpU3j99dfzpN2EhCTsduOWy+mP3THOncv7p/Hp3DmOzl/hldNzZ7VabvphukC+ffTMM8+wZ88eypUrx9mzZ8nIyAAyh82Ij4/Hx8enIMoSEbnvOSQUrly5QlxcnPl68+bNlC5dGg8PD3x9fYmKigIyB93z9fXNVdeRiIjkHYd0H127do3XX3+da9euYbVaKV26NPPmzcNisTBmzBjCw8OZO3cupUqVIjIy0hEliYhINhwSCmXLlmXJkiXZzqtWrRpLly51RBkiInIL+kWziIiYFAoiImJSKIiIiEmhICIiJoWCiIiYFAoiImJSKIiIiEmhICIiJoWCiIiYFAoiImJSKIiIiEmhICIiJoWCiIiYFAoiImJSKIiIiEmhICIiJoWCiIiYFAoiImJSKIiIiMkhz2i+cOECQ4cO5eTJkzg7O1O5cmXGjRuHu7s7Bw8eJCIigpSUFCpUqMDUqVPx8PBwRFkiIvI/HHKlYLFYePnll9mwYQNr1qyhUqVKTJs2DbvdzpAhQ4iIiGDDhg34+/szbdo0R5QkIiLZcEgouLm5ERAQYL6uX78+p0+f5tChQ7i4uODv7w9A165d+eqrrxxRkoiIZMPh9xTsdjv//ve/CQoKIi4ujvLly5vz3N3dsdvtXLx40dFliYgIDrqn8Ffjx4+nePHidO/ena+//jpP2vTwcM2TdiRveHqWLOgS5A7o/BVeeXHuHBoKkZGRxMbGMm/ePKxWKz4+Ppw+fdqcn5iYiNVqxc3NLVftJiQkYbcbt1xOf+yOce7c5TxvU+fOcXT+Cq+cnjur1XLTD9MO6z6aPn06hw4dYs6cOTg7OwNQp04dkpOT2bdvHwCff/45bdq0cVRJIiLyPxxypfDrr7/ywQcfUKVKFbp27QpAxYoVmTNnDlOmTGH06NFZvpIqIiIFwyGh8NBDD/HLL79kO69BgwasWbPGEWWIiMgt6BfNIiJiUiiIiIhJoSAiIiaFgoiImBQKIiJiUiiIiIhJoSAiIiaFgoiImBQKIiJiUiiIiIhJoSAiIiaFgoiImBQKIiJiUiiIiIhJoSAiIiaFgoiImBQKIiJiUiiIiIhJoSAiIiaHhEJkZCRBQUHUrFmTo0ePmtNjYmLo0qULwcHBdOnShRMnTjiiHBERuQmHhEKrVq347LPPqFChQpbpo0ePplu3bmzYsIFu3boRERHhiHJEROQmHBIK/v7++Pj4ZJmWkJDA4cOHCQ0NBSA0NJTDhw+TmJjoiJJERCQbBXZPIS4uDm9vb2w2GwA2mw0vLy/i4uIKqiQRkfueU0EXkBc8PFwLugT5C0/PkgVdgtwBnb/CKy/OXYGFgo+PD2fPniUjIwObzUZGRgbx8fE3dDPlREJCEna7ccvl9MfuGOfOXc7zNnXuHEfnr/DK6bmzWi03/TBdYN1HHh4e+Pr6EhUVBUBUVBS+vr64u7sXVEkiIvc9h1wpTJgwgY0bN3L+/Hl69uyJm5sba9euZcyYMYSHhzN37lxKlSpFZGSkI8oREZGbcEgojBo1ilGjRt0wvVq1aixdutQRJYiISA7oF80iImJSKIiIiEmhICIiJoWCiIiYFAoiImJSKIiIiEmhICIiJoWCiIiYFAoiImJSKIiIiEmhICIiJoWCiIiYFAoiImJSKIiIiEmhICIiJoWCiIiYFAoiImJSKIiIiEmhICIiJoWCiIiY7opQiImJoUuXLgQHB9OlSxdOnDhR0CWJiNyX7opQGD16NN26dWPDhg1069aNiIiIgi5JROS+5FTQBSQkJHD48GEWLlwIQGhoKOPHjycxMRF3d/cctWG1WnK8PZ8yJW6rzoJkK12+oEvIldycj9zQuXMMnb//KmznL6fn7u+WsxiGYeRVQbfj0KFDDBs2jLVr15rTQkJCmDp1Kg8//HABViYicv+5K7qPRETk7lDgoeDj48PZs2fJyMgAICMjg/j4eHx8fAq4MhGR+0+Bh4KHhwe+vr5ERUUBEBUVha+vb47vJ4iISN4p8HsKAMePHyc8PJw///yTUqVKERkZyYMPPljQZYmI3HfuilAQEZG7Q4F3H4mIyN1DoSAiIiaFgoiImBQKIiJiUijks0uXLlG3bl0mTJhw02V69OjBt99+e8u2goKCOHr0KAAjR45k3759eVan/FdaWhqzZs0iODiYtm3b0q5dOwYMGMCxY8duu81NmzYRHR2dh1Xe39LS0pgxYwbBwcE8/fTTPPPMM7z99tssWbKEAQMGZLvON998Q2Rk5G1vc8+ePXz33Xe3vX5hUeBjH93roqKiqFevHmvXrmXo0KE4OzvnSbsTJ07Mk3bkRsOHDyc5OZmlS5dSqlQpDMNg69atxMTEUL169dtqc9OmTdSpU4e6devmcbX3p+HDh5OSksLy5ctxdXUlPT2d5cuXk5qaetN1WrVqRatWrW57m3v37uXq1asEBgZmOz89PR0np8L/llr49+Aut3z5coYMGcIHH3zAN998w1NPPcWxY8cYPnw4V69epUaNGqSkpJjLx8fHM2HCBE6fPk1KSgpt27alT58+N7Tbo0cPevXqRcuWLUlKSmLy5Mn88ssvpKSkEBAQwPDhw7HZbI7c1XvCiRMn2LRpE1u3bqVUqVIAWCwWHn/8cQBSU1N59913+f7770lNTaVmzZqMGTOGEiVKEB4ejrOzMydOnODMmTPUr1+fyMhIvvvuOzZv3szOnTtZunQpPXv25JlnnmH+/Pl8+eWXADzyyCOMGjWKEiVKcOXKFSZMmMBPP/0EQPv27XnllVcK5Hjcjf56jlxdXQFwcnKiS5curFixgqSkJN544w1+/fVXSpYsyaxZs/D09GTFihVs2bKFmTNnsmfPHiZNmkS9evU4cOAAFouFd999l2rVqvHbb78xfPhwrl27ht1u59lnnyUwMJDPP/8cu93Ozp07adu2LSEhIXTo0IHnnnuO3bt307lzZ6pUqcJ7771HSkoKGRkZ9OnTh7Zt2wKZ/2Zr1arFgQMHuHTpEk899RQDBw4syEOZPUPyzX/+8x+jZcuWht1uN1avXm289NJLhmEYxrPPPmusWLHCMAzDOHDggFGrVi1j8+bNhmEYxosvvmjs3bvXMAzDSElJMZ5//nnju+++MwzDMFq2bGn88ssvhmEYRvfu3c11RowYYaxcudIwDMPIyMgw3nzzTeOLL75w3I7eQ9auXWu0a9fupvPnzJljzJkzx3w9ZcoUY/r06YZhGMawYcOMrl27GsnJyUZKSooREhJinrthw4YZn376qbneli1bjLZt2xqXL1827Ha7MWTIEGPKlClmm0OHDjXsdrtx+fJlIyQkxNiyZUt+7G6h9HfnaPny5Ya/v79x+vRpwzAMY+TIkeb5Wb58udG/f3/DMAxj9+7dRu3atY2ff/7ZMAzDmDt3rjFw4EDDMAxj/Pjxxrx588w2L168aBiGYcycOdN4++23zem///67UaNGDWPt2rVZlk1PTzcMwzDOnTtnNG/e3Fy/e/fuRs+ePY20tDQjKSnJCA0NNf8N3010pZCPli1bRvv27bFYLDz55JNMmDCBU6dOcfToUdq3bw9A/fr1qVGjBgBXr15l7969JCYmmm1cuXKF48eP06xZs5tuZ/PmzURHR5vDjycnJ+Pt7Z2Pe3b/OHbsGIMGDSI5OZnmzZtz8OBBkpKS2LBhA5B55VCrVi1z+SeeeAIXFxcAateuzcmTJ7M9d7t27SIkJMT8pNu5c2cmTZpkzhsxYgQWiwVXV1fatm3Lrl27aNGiRX7v7j2hQYMG5thp9erVY+fOndkuV7VqVWrXrg1k/ju8fl+vUaNGTJ06lWvXrhEQEECTJk1uui0XFxeeeuop83ViYiIjRowgNjYWm83GpUuXiImJoX79+gA888wzODk54eTkREhICLt376Zly5Z5st95RaGQT1JTU4mKisLZ2ZnVq1cDmTfHVq5cedN17HY7FouFZcuWUaRIkRxvyzAM5s6dS6VKle647vtd7dq1iY2NNYdcqV69OqtXr2bx4sUcOnQIwzAYPXo0TZs2zXb964EAYLPZzIEeJe9cP0eXLl2idOnSN8zP6Tn46/09q9VKeno6AMHBwdSvX58dO3bw4Ycfsnz5cqZNm5ZtG8WKFcNi+e+zCcaMGUNQUBCzZ8/GYrEQHBycpXu4MNC3j/LJN998Q9WqVdm2bRubN29m8+bNLFiwgC+//JIaNWqwZs0aAKKjo81vFLm6utKwYUPmz59vthMXF8e5c+f+dltBQUHMnz/f/ONPTEzk999/z6c9u7dVqVKFVq1aMWrUKC5fvmxOv3r1KpB5rD/55BOSk5MBSEpK4vjx47ds19XVNUt7TZs2Zf369SQlJWEYBsuWLePRRx815y1fvhzDMEhKSmLdunXmPMk8R0FBQURERJCUlARkjq68dOlS8zzdidjYWDw9PXnuuefo16+feW/nf89hdi5fvkyFChWwWCzs2LGD2NjYLPO//PJL0tPTuXr1KuvXr//bq5CCoiuFfLJ8+XKefvrpLNP8/Pyw2+2Eh4czdepUPvzwQ2rUqMEjjzxiLjNt2jQmT55srluiRAkmTpyIp6fnTbc1YsQIpk6danZVFSlShBEjRujK4TZNnjyZuXPn0rFjR5ycnChVqhReXl707t2bGjVqMHv2bDp27IjFYsFisRAWFka1atX+ts127doxfPhwvvrqK/NG8y+//ELXrl0BqFOnDn379gXgtddeY/z48ebfQLt27Xjsscfyd6cLmbfffps5c+bQoUMHihQpgt1up0WLFlStWvWO216/fj1r1qyhSJEiWCwWRowYAWR2Da5atYr27dubN5r/16BBgxg7diyzZs3ikUceoWbNmlnmP/jgg3Tt2tW80Xy3dR2BBsQTEXGIv35j8G6m7iMRETHpSkFEREy6UhAREZNCQURETAoFERExKRREHMzPz0+/I5G7lm40i4iISVcKIiJiUiiIAPPnz6d58+b4+fkRHBzMrl27mDVrFgMGDOCNN97Az8+PZ599liNHjpjrnD17lv79+9OkSROCgoJYtGiROS8jI4N58+bxxBNP4Ofnx3PPPUdcXBwANWvWNIc/SE1NJTIykscff5xHH32UiIgIcwiNxMREXn31Vfz9/WncuDHdunXDbrc78KjI/UihIPe93377jc8++4xly5Zx4MABPv74YypUqABkjmHVpk0b9u7dS2hoKK+99hppaWnY7Xb69u1LzZo12bZtG//85z/55z//yfbt2wFYuHAha9euZf78+ezfv59JkyZRtGjRG7Y9bdo0YmJiWLVqFRs3biQ+Pp45c+aYbXh7e7Nr1y527NjBwIEDswy+JpIfFApy37PZbKSmpnL8+HHS0tKoWLEiDzzwAAAPP/wwbdq0oUiRIvTs2ZPU1FR+/PFHfvrpJxITEwkLC8PZ2ZlKlSrRuXNn1q1bB8DSpUt5/fXXefDBB7FYLNSqVYsyZcpk2a5hGCxZsoQRI0bg5uaGq6srr776KmvXrgUyHxxz7tw5Tp8+TZEiRfD391coSL7TgHhy36tcuTIjRoxg1qxZHDt2jMDAQMLDwwEoV66cuZzVasXb25v4+Hgg8yl5/v7+5vyMjAzz9ZkzZ8xguZnExESuXbvGc889Z04zDMPsInrppZeYPXs2vXr1AqBLly707t07D/ZY5OYUCiLA008/zdNPP01SUhIRERFMmzaNBx54gDNnzpjL2O12zp49i5eXFzabjYoVK7Jx48Zs2ytXrhwnT540H6CUnTJlylC0aFHWrl2b7UORXF1dCQ8PJzw8nKNHj/KPf/yDRx555KbPchDJC+o+kvveb7/9xq5du0hNTcXZ2RkXFxes1sx/Gj///DMbN24kPT2df/7znzg7O1OvXj3q1q1LiRIlmD9/PsnJyWRkZHD06FGio6MB6NSpEzNmzODEiRMYhsGRI0e4cOFClu1arVY6derEpEmTSEhIADJvXl+/L/Htt98SGxuLYRiULFkSm82m7iPJdwoFue+lpqbyzjvvEBAQQGBgIImJieYD1Vu1asW6deto1KgRq1evZtasWRQpUgSbzca8efM4cuQIrVq1okmTJowaNcp86EvPnj156qmn6NWrFw0aNGDkyJHZPoFryJAhVK5cmc6dO9OgQQNefPFFYmJigMyHvfTs2RM/Pz+6dOnC888/f1c+lEXuLfrxmshNzJo1i9jY2Js+ilHkXqQrBRERMSkURETEpO4jEREx6UpBRERMCgURETEpFERExKRQEBERk0JBRERMCgURETH9fxNfFcSbyqAgAAAAAElFTkSuQmCC
"
>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>We can see from the chart that the <em>Adelie</em> penguins are the most common penguin species, <em>Gentoo</em> penguins are the next, and <em>Chinstrap</em> penguins are the least common penguin species. This information can be used as a factor to distinguish a penguin's species initially, and can be used for further analyzation to have a more accurate prediction of the species of a penguin.  We can also see that the male to female ratio is approximately 1:1 for all species.</p>

</div>
</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h3 id="Exploring-the-Features-of-different-Penguin-Species">Exploring the Features of different Penguin Species<a class="anchor-link" href="#Exploring-the-Features-of-different-Penguin-Species">&#182;</a></h3><p>Now that we have a general picture of the three penguin species in the three islands, we will explore if there are any relationships between each type of their feature and their species. Analyzing their features will help us distinguish these species better.</p>
<p>We used boxplots as a way to see the differences between the three species, Adelie, Gentoo, and Chinstrap clearly.
We plotted each features separately for a prominent distinguishment.</p>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[&nbsp;]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-python"><pre><span></span><span class="n">specie_column</span> <span class="o">=</span> <span class="n">penguins</span><span class="o">.</span><span class="n">loc</span><span class="p">[:,</span><span class="s1">&#39;species&#39;</span><span class="p">]</span>
<span class="n">spe</span> <span class="o">=</span> <span class="n">specie_column</span><span class="o">.</span><span class="n">values</span>

<span class="n">body_mass_column</span> <span class="o">=</span> <span class="n">penguins</span><span class="o">.</span><span class="n">loc</span><span class="p">[:,</span><span class="s1">&#39;body_mass_g&#39;</span><span class="p">]</span>
<span class="n">bod</span> <span class="o">=</span> <span class="n">body_mass_column</span><span class="o">.</span><span class="n">values</span>

<span class="n">box_plot</span> <span class="o">=</span> <span class="n">sns</span><span class="o">.</span><span class="n">boxplot</span><span class="p">(</span><span class="n">x</span> <span class="o">=</span> <span class="n">spe</span><span class="p">,</span> <span class="n">y</span> <span class="o">=</span> <span class="n">bod</span><span class="p">,</span> <span class="n">showmeans</span> <span class="o">=</span> <span class="kc">True</span><span class="p">,</span> <span class="n">meanprops</span> <span class="o">=</span> <span class="p">{</span><span class="s2">&quot;marker&quot;</span><span class="p">:</span> <span class="s2">&quot;+&quot;</span><span class="p">,</span> <span class="s2">&quot;markeredgecolor&quot;</span><span class="p">:</span> <span class="s2">&quot;black&quot;</span><span class="p">,</span>
                       <span class="s2">&quot;markersize&quot;</span><span class="p">:</span> <span class="s2">&quot;10&quot;</span><span class="p">})</span>
<span class="n">box_plot</span><span class="o">.</span><span class="n">set</span><span class="p">(</span><span class="n">xlabel</span> <span class="o">=</span> <span class="s1">&#39;Species&#39;</span><span class="p">,</span> <span class="n">ylabel</span> <span class="o">=</span> <span class="s1">&#39;Body Mass&#39;</span><span class="p">,</span> <span class="n">title</span> <span class="o">=</span> <span class="s1">&#39;Species vs. Body Mass&#39;</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[&nbsp;]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>[Text(0, 0.5, &#39;Body Mass&#39;),
 Text(0.5, 0, &#39;Species&#39;),
 Text(0.5, 1.0, &#39;Species vs. Body Mass&#39;)]</pre>
</div>

</div>

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>




<div class="jp-RenderedImage jp-OutputArea-output ">
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAYsAAAEWCAYAAACXGLsWAAAABHNCSVQICAgIfAhkiAAAAAlwSFlzAAALEgAACxIB0t1+/AAAADh0RVh0U29mdHdhcmUAbWF0cGxvdGxpYiB2ZXJzaW9uMy4yLjIsIGh0dHA6Ly9tYXRwbG90bGliLm9yZy+WH4yJAAAgAElEQVR4nO3de7xVZZ3H8c8XREVREUFUjoTjwcoumh0vlTPhBQSz1DLTqTyWDVNjMtVU6mucrNRpai7qsctEeTmZSupokYmCFzIzFfCCghZHJT2ECiIkicjlN3+sZ+fmcM5Z+8BZe5/L9/167ddZ61lrPeu394b928/zrP0sRQRmZmadGVDrAMzMrOdzsjAzs1xOFmZmlsvJwszMcjlZmJlZLicLMzPL5WRhfZakBZLG1TqOapMUkuprHYf1LU4WVhWSDpd0n6RVklZI+q2kg4s8Z0S8LSJmF3mO7iBptqTXJK1Or889kt5RgziuSonm+DblF6fy06sdk/UcThZWOEk7A7cAlwHDgFHAN4C1tYyrh/l8RAwhe31mA1fXKI4/AKeVViRtA5wMPFWjeKyHcLKwatgPICKui4gNEbEmImZGxHwASaenlsZ30zfrJyUdVTpY0i6SLpe0VNISSRdKGli2/R8kPSHpFUkLJR2UyhdLOjotD5B0jqSnJL0k6XpJw9K27SX9NJWvlDRH0si2T0LS2ZJubFN2qaSmsufxdIrjGUkf7+oLFREbgGnA/mXn2E7SJZL+lB6XSNqubPtX0mvzJ0mfLis/WNILbV6rD0t6tJMQfgkcLmnXtD4RmA88X1bHvpLuSq/XcknXSBpatv3s9D69Iun3pfdS0iGS5kr6c4rrf7r6+ljtOFlYNfwB2CCpWdKksg+icoeSfXsdDpwP3FT6MAeuAtYD9cC7gAnAZwAkfRT4Otm34Z2BDwEvtVP/WcAJwPuBvYCXge+lbY3ALsDewG7AZ4E17dQxDThW0k7p3APJvnVfK2lHoAmYFBE7Ae8FHsl5XTYjaVvg48D9ZcX/ChwGHAgcABwCnJf2nwh8GRgPjAWOLh0UEXPIXosJZXV9EvhJJyG8BvwCOCWtn9bO/gK+RfY6vpXsdft6iufNwOeBg9PrcAywOB13KXBpROwM7Atc30kc1tNEhB9+FP4g+1C5Cmgl++CfDoxM204H/gSobP8HyT7YRpJ1Vw0u23YqcHdavh345w7OuRg4Oi0/ARxVtm1PYB2wDfBp4D7gnRU8j3uB09LyeOCptLwjsBL4SHmsFb42s4FX0/FrgVVtYn0KOLZs/RhgcVq+AviPsm37AQHUp/WzgWvS8rB0nj07iOMq4ELgcOB3wFDgBWBwet6nd3DcCcDDabkeeJEsaQ1qs989ZN2Pw2v979GPrj/csrCqiIgnIuL0iKgD3k72rfSSsl2WRPpESf6Y9nkTMAhYmrqIVgI/BHZP++1NZf3pbwJuLqvjCWADWTK6mizpTEtdOd+RNKiDeq4lS1YAf5/WiYi/AB8ja5UslfQrSW+pIK6SKRExlOyD+TjgRknvTNv2Ins9SkqvTWnbc222lfsp8MHU8jkZ+E1ELO0skIi4FxhB1qK5JSI2aWVJGilpWupq+nM6x/B0bAvwBbKWxotpv1KsZ5AlsydTV99xncVhPYuThVVdRDxJ9i327WXFoySpbH00WWvjObJv28MjYmh67BwRb0v7PUfWpZHnObIuoqFlj+0jYklErIuIb0TE/mTdR8dRNsjbxg3AOEl1wImkZJGe1+0RMZ6s1fIk8KMK4tpERGyMiN8ALbzRffQnsmRXUnptAJaSJczybeX1LSFrJXyYrKVW6cD5T4F/of0uq38na728I7IupU+QdU2VznltRByeYg7g26l8UUScSpbov02WEHesMB6rMScLK5ykt0j6l/QBi6S9yb6dl/fL7w5MkTQojUO8Fbg1fQueCfy3pJ3TQPW+kt6fjvsx8GVJ71amXlL5B2vJ/wIXlbZJGqF0iaikIyS9I41B/Jmse2pje88lIpaRdRtdCTwTEU+kOkZKOj59+K0FVndURwWv13vIBrgXpKLrgPNSzMOBr5F9mEPW73+6pP0l7UA23tPWT4CvAu8AbqowjCaybrZ72tm2E9nzWyVpFPCVstjfLOnINAD/GtnYz8a07ROSRkTERrIuN9jC18iqz8nCquEVsgHsByT9hSxJPE72zbXkAbIB2uXARcBJEVEaqD4N2BZYSDYwfSPZt3ci4oa0/7XpPD8n65tv61KycZKZkl5JMRyatu2R6vwzWffUr+n8G/i1ZH3y15aVDQC+RPaNfwXZQPrnACT9raTVndQH8F1lv7NYnc59XkTMSNsuBOaSXZX0GPBQKiPtcwlwF1lr5K526r6Z1A0XEa/mxEGqd0VE3Nmma7DkG8BBZGMrv2LTBLQd8B9k7+PzZF8Czk3bJgIL0nO8FDilbReX9Vxq/9+CWfUo+7HXZ1LXhRVA0lPAP0bEHbWOxXontyzM+jhJHyEbO2iv1WFWkW1qHYCZFUfSbLLxj0+msQKzLeJuKDMzy+VuKDMzy9Unu6GGDx8eY8aMqXUYZma9yrx585ZHxIj2tvXJZDFmzBjmzp1b6zDMzHoVSW1nAPgrd0OZmVkuJwszM8vlZGFmZrmcLMzMLJeThZmZ5XKyMDOzXE4WZmaWq0/+zsJsazU1NdHS0tLt9ba2tgJQV1fX7XXX19czZcqUbq/XDJwszKpqzRrfvsF6JycLs3YU9Q29VG9TU1Mh9ZsVxWMWZmaWy8nCzMxyOVmYmVkuJwszM8vlZGFmZrmcLMzMLJeThZmZ5XKyMDOzXE4WZmaWy8nCzMxyOVmYmVkuJwszM8tVaLKQNFTSjZKelPSEpPdIGiZplqRF6e+uaV9JapLUImm+pIPK6mlM+y+S1FhkzGZmtrmiWxaXArdFxFuAA4AngHOAOyNiLHBnWgeYBIxNj8nADwAkDQPOBw4FDgHOLyUYMzOrjsKShaRdgL8DLgeIiNcjYiVwPNCcdmsGTkjLxwM/icz9wFBJewLHALMiYkVEvAzMAiYWFbeZmW2uyJbFPsAy4EpJD0v6saQdgZERsTTt8zwwMi2PAp4rO741lXVUvglJkyXNlTR32bJl3fxUzMz6tyKTxTbAQcAPIuJdwF94o8sJgIgIILrjZBExNSIaIqJhxIgR3VGlmZklRSaLVqA1Ih5I6zeSJY8XUvcS6e+LafsSYO+y4+tSWUflZmZWJYUli4h4HnhO0ptT0VHAQmA6ULqiqRH4RVqeDpyWroo6DFiVuqtuByZI2jUNbE9IZWZmViVF34P7LOAaSdsCTwOfIktQ10s6A/gjcHLa91bgWKAFeDXtS0SskHQBMCft982IWFFw3GZmVqbQZBERjwAN7Ww6qp19Azizg3quAK7o3ujMzKxS/gW3mZnlcrIwM7NcThZmZpbLycLMzHI5WZiZWS4nCzMzy+VkYWZmuZwszMwsl5OFmZnlcrIwM7NcThZmZpbLycLMzHI5WZiZWS4nCzMzy+VkYWZmuZwszMwsl5OFmZnlcrIwM7NchSYLSYslPSbpEUlzU9nXJS1JZY9IOrZs/3MltUj6vaRjysonprIWSecUGbOZmW2u0HtwJ0dExPI2ZRdHxH+VF0jaHzgFeBuwF3CHpP3S5u8B44FWYI6k6RGxsOC4zcwsqUayqNTxwLSIWAs8I6kFOCRta4mIpwEkTUv7Oln0c01NTbS0tNQ6jC5ZtGgRAFOmTKlxJJWrr6/vVfFaMYpOFgHMlBTADyNiair/vKTTgLnAv0TEy8Ao4P6yY1tTGcBzbcoPbXsiSZOByQCjR4/u1idhPVNLSwt/ePwhRg/ZUOtQKrbtuqzn97XFc2ocSWWeXT2w1iFYD1F0sjg8IpZI2h2YJelJ4AfABWSJ5ALgv4FPb+2JUiKaCtDQ0BBbW5/1DqOHbOC8htW1DqPPunDukFqHYD1EoQPcEbEk/X0RuBk4JCJeiIgNEbER+BFvdDUtAfYuO7wulXVUbmZmVVJYspC0o6SdSsvABOBxSXuW7XYi8Hhang6cImk7SfsAY4EHgTnAWEn7SNqWbBB8elFxm5nZ5orshhoJ3CypdJ5rI+I2SVdLOpCsG2ox8I8AEbFA0vVkA9frgTMjYgOApM8DtwMDgSsiYkGBcZuZWRuFJYt09dIB7ZR/spNjLgIuaqf8VuDWbg3QzMwq5l9wm5lZLicLMzPL5WRhZma5nCzMzCyXk4WZmeVysjAzs1xOFmZmlsvJwszMcjlZmJlZLicLMzPL5WRhZma5nCzMzCyXk4VZlV189wu1DsGsy5wszKrsktnLah2CWZc5WZiZWS4nCzMzy+VkYWZmuYq8rapZv3fx3S+0O0bxpvMf32T9C+NG8MUjRlYrLLMuKzRZSFoMvAJsANZHRIOkYcDPgDFk9+A+OSJeVnaz7kuBY4FXgdMj4qFUTyNwXqr2wohoLjJu6x1aW1v5yysDuXDukFqH0rGdhvAPH9x3k6If/fJ+/uGDh21S9hfgwrlVjKtCf3xlIDu2ttY6DOsBqtENdUREHBgRDWn9HODOiBgL3JnWASYBY9NjMvADgJRczgcOBQ4Bzpe0axXiNjOzpBbdUMcD49JyMzAbODuV/yQiArhf0lBJe6Z9Z0XECgBJs4CJwHXVDdt6mrq6Ol5bv5TzGlbXOpQu+dEv6TUxXzh3CNvX1dU6DOsBim5ZBDBT0jxJk1PZyIhYmpafB0odtaOA58qObU1lHZWbmVmVFN2yODwilkjaHZgl6cnyjRERkqI7TpSS0WSA0aNHd0eVZoX4wrgRtQ7BrMsKbVlExJL090XgZrIxhxdS9xLp74tp9yXA3mWH16WyjsrbnmtqRDRERMOIEf7PaD2Xr3qy3qiwZCFpR0k7lZaBCcDjwHSgMe3WCPwiLU8HTlPmMGBV6q66HZggadc0sD0hlZmZWZXkJgtJ35G0s6RBku6UtEzSJyqoeyRwr6RHgQeBX0XEbcB/AOMlLQKOTusAtwJPAy3Aj4B/AkgD2xcAc9Ljm6XBbjMzq45KxiwmRMRXJZ1I9ruIDwP3AD/t7KCIeBo4oJ3yl4Cj2ikP4MwO6roCuKKCWM3MrACVdEOVEsoHgBsiYlWB8ZiZWQ9UScvilnQV0xrgc5JGAK8VG5aZmfUkuS2LiDgHeC/QEBHryGYmOL7owMzMepLly5dz1lln8dJLL9U6lJqoZID7o8C6iNgg6TyysYq9Co/MzKwHaW5uZv78+TQ398+p6SoZs/i3iHhF0uFkVy9dTpq3ycysP1i+fDkzZswgIpgxY0a/bF1Ukiw2pL8fAKZGxK+AbYsLycysZ2lubia7YBM2btzYL1sXlQxwL5H0Q2A88G1J2+GbJuVqamqipaWl2+ttTdNF1xU0uVt9fT1TpkwppG6z3mrWrFmsW7cOgHXr1jFz5ky+9KUv1Tiq6qrkQ/9ksl9MHxMRK4FhwFcKjco6tGbNGtasWVPrMMz6lfHjxzNo0CAABg0axIQJE2ocUfXltiwi4lXgJkm7SyrN0PdkZ8cYhX07L9Xb1NRUSP1mtrnGxkZmzJgBwIABA2hsbMw5ou+p5GqoD6WpOZ4Bfp3+zig6MDOznmL48OFMmjQJSUyaNInddtut1iFVXSVjFhcAhwF3RMS7JB0BVDI3lFnhnl3dw2+r2sYLr2bfz0busLHGkVTm2dUD2a/WQfQQjY2NLF68uF+2KqCyZLEuIl6SNEDSgIi4W9IlhUdmlqO+vr7WIXTZ64sWAbD9mLE1jqQy+9E7X+ciDB8+nMsuu6zWYdRMJclipaQhZJMHXiPpRbJfcZvVVG+8astjTtZbVXI11PFk80J9EbgNeAr4YJFBmZlZz1LJ1VDlrYj+90sUMzPrOFlIegUovz+20rrIbj+xc8GxmZlZD9FZy+JOYA/gJmBaRDxbnZDMzKyn6XDMIiJOAI4BlgE/kvRrSf8kaVjVojMzsx6h0zGLdFe8KyU1A6cATcD2wP9UITYzsy7zvGzF6PRqKEnvlXQZ8BDZDZBOjIguJQpJAyU9LOmWtH6VpGckPZIeB6ZySWqS1CJpvqSDyupolLQoPfrnL2LMrKb6+7xsnQ1wLwZWAtOAycD6VH4QQEQ8VOE5/hl4AigfEP9KRNzYZr9JwNj0OJTsnhmHpm6v84EGsgH2eZKmR8TLFZ7fzPoRz8tWjM66oRaTfTgfA0wguwqqJIAj8yqXVEd2H4yLgLz5fI8HfhLZpPH3SxoqaU9gHDArIlakOmcBE4Hr8s5vZmbdo8NkERHjuqH+S4CvAju1Kb9I0tfIrrg6JyLWAqOA58r2aU1lHZVvQtJkshYQo0ePbrvZzMy2QmE3MZJ0HPBiRMxrs+lc4C3AwWT3xji7O84XEVMjoiEiGkaMGNEdVZqZWVLkHe/eB3wojX1MA46U9NOIWBqZtcCVwCFp/yXA3mXH16WyjsrNzKxKCksWEXFuRNRFxBiyy27viohPpHEIJAk4AXg8HTIdOC1dFXUYsCoilpLdpW+CpF0l7Uo2fnJ7UXGbmdnmcueGknQTcDkwIyK6YxL+aySNIBswfwT4bCq/FTgWaAFeBT4FEBErJF0AzEn7fbM02G1mZtVRyRTl3yf74G6SdANwZUT8visniYjZwOy03O5VVOkqqDM72HYFcEVXzmlmZt0ntxsqIu6IiI8DB5FdTnuHpPskfUrSoKIDNDOz2qtozELSbsDpwGeAh4FLyZLHrMIiMzOzHqOSMYubgTcDVwMfTIPOAD+TNLfI4MzMrGeoZMyiKSLubm9DRDR0czxmZtYDdTY31IfbWy6JiJuKCsrMzHqWzloWpfts70424+xdaf0I4D6ymyKZmVk/0NncUJ+Cv07ct39prCL9qO6qqkRnZmY9QiVXQ9WVDWoDvAB4pj4zs36kkgHuOyXdzhtTgn8MuKO4kMzMrKfJTRYR8XlJJwJ/l4qmRsTNxYZlZmY9SSUtC8gGtNeT3fToweLCMTOznih3zELSyWQJ4iTgZOABSScVHZiZmfUclbQs/hU4OCJeBEgzxt4BtL2HtpmZ9VGVXA01oJQokpcqPM7MzPqISloWt7VzNdStxYVkZmY9TSVXQ30lTfdxeCry1VBmZv1MRVdDpXmgbpI0nKwbyszM+pEOxx4kHSZptqSbJL1L0uNk98t+QdLE6oVoZma11tlA9XeBfycbq7gL+ExE7EH247xvVXoCSQMlPSzplrS+j6QHJLVI+pmkbVP5dmm9JW0fU1bHuan895KO6fKzNDOzrdJZstgmImZGxA3A8xFxP0BEPNnFc/wz8ETZ+reBiyOiHngZOCOVnwG8nMovTvshaX/gFOBtwETg+5IGdjEGMzPbCp0li41ly2vabItKKpdUB3wA+HFaF3Akb/xGoxk4IS0fn9ZJ249K+x8PTIuItRHxDNACHFLJ+c3MrHt0NsB9gKQ/AwIGp2XS+vYV1n8J8FVgp7S+G7AyItan9VZgVFoeBTwHEBHrJa1K+48C7i+rs/yYrdbU1ERLS0t3VVe4RYsWATBlypQaR9I19fX1vS5mM3tDZ/ez2KquHknHAS9GxDxJ47amrgrPNxmYDDB6dOUzqLe0tPDwYwvZuMOwokLrVno9a9TNe+r5GkdSuQGvrqh1CGa2lSqdSHBLvA/4kKRjyVoiOwOXAkMlbZNaF3XAkrT/EmBvoFXSNsAuZJfplspLyo/5q4iYCkwFaGhoqKibrGTjDsN4bf/junKIdcH2C2+pdQhdVlSLs8iWYW9rvblVXx3d9e+isGQREecC5wKklsWXI+Ljkm4gm5RwGtAI/CIdMj2t/y5tvysiQtJ04FpJ/wPsBYzFM99aLzV48OBah9BjtLS08PCCh2ForSOpUBrFfXjJw7WNoytWdl9VRbYsOnI2ME3ShcDDwOWp/HLgakktwAqyK6CIiAWSrgcWkk2TfmZEbKh+2Naf9LZvj73WUNg4bmP+frZFBszuvmn8qpIsImI2MDstP007VzNFxGvARzs4/iLgouIiNDOzznj2WDMzy+VkYWZmuZwszMwsl5OFmZnlcrIwM6vQs7c+W+sQasbJwsysQq23tdY6hJpxsuiF/vRb36jQzKrLyaIXev53P691CGbWzzhZmJlZrlpM92Fm1uM9e+uz7Y5R3Dflvk3W6ybWMfrYyme67q36fbJobW1lwKuret3MqL0p3gGvvkRr6/r8Ha1faW1thVXdO39RdxqzwxjGfHjMJmX33nQvh3/48M13nl2VkLpuJbRG9wzK9/tk0dM9+4cFtLYs3Kz8vltv2GS9rn5/Ru/3tmqFZWb9TL9PFnV1dbywdpseez+L3fc/jt3blD30X40c9OXmzfZ9rTohddn2C2+hrm6PWodhPUxdXR3LtKx3zTp7U++aJXfA7AHUjarrnrq6pRYzM+vTnCzMzCpUN7F7vqX3Rk4WZmYV6g9XPXXEyaIX2uM9J9Q6BDPrZ5wseqG93ndirUMws37GycLMzHIVliwkbS/pQUmPSlog6Rup/CpJz0h6JD0OTOWS1CSpRdJ8SQeV1dUoaVF6NBYVs5mZta/I31msBY6MiNWSBgH3SpqRtn0lIm5ss/8kYGx6HAr8ADhU0jDgfKABCGCepOkR8XKBsZuZWZnCWhaRWZ1WB6VHdHLI8cBP0nH3A0Ml7QkcA8yKiBUpQcwCJhYVt5mZba7QX3BLGgjMA+qB70XEA5I+B1wk6WvAncA5EbEWGAU8V3Z4ayrrqLztuSYDkwFGj+6/l7eZ9Sore+7cUJspffUdUtMoumYl7XxabplCk0VEbAAOlDQUuFnS24FzgeeBbYGpwNnAN7vhXFNTfTQ0NHTWgjGzHqC+vr7WIXTJokWLABg7amyNI+mCUd33OldlbqiIWCnpbmBiRPxXKl4r6Urgy2l9CbB32WF1qWwJMK5N+exCAzazwk2ZMqXWIXRJKd6mpqYaR1IbRV4NNSK1KJA0GBgPPJnGIZAk4ATg8XTIdOC0dFXUYcCqiFgK3A5MkLSrpF2BCanMzMyqpMiWxZ5Acxq3GABcHxG3SLpL0ghAwCPAZ9P+twLHAi3Aq8CnACJihaQLgDlpv29GxIoC4zYzszYKSxYRMR94VzvlR3awfwBndrDtCuCKbg3QzMwq1ksuQzAzs1rq9zc/Ahjw6opec5tSvfZnAGL7nWscSeUGvLoC8M2PzHqzfp8set/le68AMHbf3vThu0eve53NbFP9Pln48j0zs3weszAzs1xOFmZmlsvJwszMcjlZmJlZLicLMzPL5WRhZma5nCzMzCyXk4WZmeVysjAzs1xOFmZmlsvJwszMcjlZmJlZLicLMzPL5WRhZma5CksWkraX9KCkRyUtkPSNVL6PpAcktUj6maRtU/l2ab0lbR9TVte5qfz3ko4pKmYzM2tfkS2LtcCREXEAcCAwUdJhwLeBiyOiHngZOCPtfwbwciq/OO2HpP2BU4C3AROB70saWGDcZmbWRmHJIjKr0+qg9AjgSODGVN4MnJCWj0/rpO1HSVIqnxYRayPiGaAFOKSouM3MbHOFjllIGijpEeBFYBbwFLAyItanXVqBUWl5FPAcQNq+CtitvLydY8rPNVnSXElzly1bVsTTMTPrtwpNFhGxISIOBOrIWgNvKfBcUyOiISIaRowYUdRpzMz6papcDRURK4G7gfcAQyWV7v1dByxJy0uAvQHS9l2Al8rL2znGzMyqoMiroUZIGpqWBwPjgSfIksZJabdG4BdpeXpaJ22/KyIilZ+SrpbaBxgLPFhU3GZmtrlt8nfZYnsCzenKpQHA9RFxi6SFwDRJFwIPA5en/S8HrpbUAqwguwKKiFgg6XpgIbAeODMiNhQYt5mZtVFYsoiI+cC72il/mnauZoqI14CPdlDXRcBF3R2jmfU9TU1NtLS0dHu9ixYtAmDKlCndXjdAfX19YXV3hyJbFmZmfcbgwYNrHUJNOVmYWZ/Sk7+d92ZOFgVxU9jM+hIni16mvzeFzaw2nCwK4m/nZtaXeIpyMzPL5WRhZma5nCzMzCqwfPlyzjrrLF566aVah1ITThZmZhVobm5m/vz5NDc35+/cBzlZmJnlWL58OTNmzCAimDFjRr9sXThZmJnlaG5uJpvXFDZu3NgvWxdOFmZmOWbNmsW6desAWLduHTNnzqxxRNXnZGFmlmP8+PEMGjQIgEGDBjFhwoQaR1R9ThZmZjkaGxuRBMCAAQNobGzMOaLvcbIwM8sxfPhwJk2ahCQmTZrEbrvtVuuQqs7TfZiZVaCxsZHFixf3y1YFOFmYmVVk+PDhXHbZZbUOo2bcDWVmZrmcLMzMLJeThZmZ5XKyMDOzXCr9hL0vkbQM+GOt4yjQcGB5rYOwLeb3r/fq6+/dmyJiRHsb+mSy6OskzY2IhlrHYVvG71/v1Z/fO3dDmZlZLicLMzPL5WTRO02tdQC2Vfz+9V799r3zmIWZmeVyy8LMzHI5WZiZWS4nixqTdIKkkPSWDrbPltTppXrl+0i6VdLQImI1kDRS0rWSnpY0T9LvJJ24hXV9QdIO3R2jgaQ9JE2T9FR6n26VNFnSLR3s/2NJ+2/BeQ6UdOzWR9zzOVnU3qnAvenvVouIYyNiZXfUZZtSdvebnwP3RMTfRMS7gVOAui2s8guAk0U3S+/TzcDsiNg3vU/nAiM7OiYiPhMRC7fgdAcC7SYLSX1qVm8nixqSNAQ4HDiD7EMHSYPTN6InJN0MDC7bf0L6JvuQpBvS8W3rXCxpeFr+hKQHJT0i6YeSBlbnmfVZRwKvR8T/lgoi4o8RcZmkgZL+U9IcSfMl/SOApHGp5XejpCclXaPMFGAv4G5Jd6d9T5X0mKTHJX27dI6Oyq1DRwDr2rxPjwK/AYa0fS9gs9b5akkXSXpU0v2SRqbyj6b34FFJ90jaFvgm8LH0f+xjkr4u6WpJvwWuljRG0m/S/9mHJL031TUu1fErSb+X9L+SevbncUT4UaMH8HHg8rR8H/Bu4EvAFansncB6oIFsmoF7gB3TtrOBr6Xl2UBDWl6c9n0r8EtgUCr/PnBarZ9zb34AU4CLO9g2GTgvLW8HzAX2AcYBq8haHwOA3wGHl79XaXkv4FlgBNl9Zu4CTuiovNavRRIcMRoAAATaSURBVE9+dPQ+5bwX5f+HAvhgWv5O2fv6GDAqLQ9Nf08Hvlt2jq8D84DBaX0HYPu0PBaYWxbLa8DfAAOBWcBJtX7tOnv0qWZSL3QqcGlanpbW64EmgIiYL2l+2n4YsD/w2/RlaFuyf+wdOYos+cxJ+w8GXuzm+Ps1Sd8jaxm+TjYX2TslnZQ270L24fA68GBEtKZjHgHGkHU9ljuYrNtkWdrvGuDvyD642iv/eXHPrE+r5L14HSiNbcwDxqfl3wJXSboeuKmTc0yPiDVpeRDwXUkHAhuA/drE8nSK5Tqyf0s3bsmTqgYnixqRNIysW+MdkoLs20UAD3d0CDArIiod2xDQHBHnbnWwVrIA+EhpJSLOTF1+c8m+/Z8VEbeXHyBpHLC2rGgD/n9XtAXASR1sq+S9WBfp63/5PhHxWUmHAh8A5kl6dwfn+EvZ8heBF4ADyFozr5Vta/sjtx79o7ee3UfWt50EXB0Rb4qIMRGxN/AM2TeZvweQ9HayriiA+4H3SapP23aUtF879ZbcCZwkafe0/zBJbyroufQXdwHbS/pcWVlpgPp24HOSBgFI2k/Sjjn1vQLslJYfBN4vaXgaWzoV+HUn5daxu4DtJE0uFUh6J/C3W1OppH0j4oGI+BqwDNibTd/D9uwCLI2IjcAnyb4UlhwiaZ80VvExNm/h9ChOFrVzKtkVG+X+j6yfe4ikJ8gGz+YBpG6I04HrUtfU74B2L7dN+y8EzgNmpv1nAXt283PoV9K3zRPIPryfkfQg0Ew2fvRjYCHwkKTHgR+S34KYCtwm6e6IWAqcA9wNPArMi4hfdFRewNPrM9L7dCJwtLJLZxcA3wKe38qq/7N0oQHZGOOjZO/L/qUB7naO+T7QKOlRsv+v5a2OOcB3gSfIvii2/TzoUTzdh5lZlaXuyS9HxHG1jqVSblmYmVkutyzMzCyXWxZmZpbLycLMzHI5WZiZWS4nC7MKSfpXSQvS3E+PpB9odVfdni3YejT/ktSsApLeAxwHHBQRa9Mvt7ftrvojol9Mc229l1sWZpXZE1geEWsBImJ5RPwpzfL7nfRjrQfLfmE/QtL/pVlo50h6XyofIunKtP98SR9J5Z3OFpweV6VZTx+T9MUavQ7WTzlZmFVmJrC3pD9I+r6k95dtWxUR7yD7Ne4lqexSsplPDyabT+rHqfzfSvtHxDvJpqb4K0lvJZv64X0RUZp87uNk900YFRFvT+e6spinadY+d0OZVSAiVqeJ4/6W7H4JP5N0Ttp8Xdnfi9Py0WTTQJSq2FnZ/UeOJt27JNX7cptTdTRb8C+Bv5F0GfArsuRlVjVOFmYViogNZPc9mC3pMaCxtKl8t/R3AHBYRJTPMkpZ8uhIh7MFSzoAOAb4LHAy8OkuPgWzLeZuKLMKSHqzpLFlRQeS3cMCsm6j0t/SPUZmAmeVHX9gWpwFnFlWvmubU7U7W3AazxgQEf9HNkHkQVv/rMwq55aFWWWGAJely1vXAy1kd8c7Dtg1zey7ljfupT4F+F4q34bsLoefBS5M5Y+TjUd8g7Ib6UTEQkml2YIHAOvIkssa4MqyW2/6PiVWVZ4bymwrSFpMdjvO5bWOxaxI7oYyM7NcblmYmVkutyzMzCyXk4WZmeVysjAzs1xOFmZmlsvJwszMcv0/XdZ+vua7GdsAAAAASUVORK5CYII=
"
>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>This box plot illustrates the distribution of body mass between each penguin species. According to the plot, we can see that Gentoo penguins have a higher overall body mass than Adelie and Chinstrap penguins. There are no major difference between the body mass in Adelie and Chinstrap penguins other than that Adelie penguins appear to have slightly higher overall body mass than Chinstrap penguins.</p>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[&nbsp;]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-python"><pre><span></span><span class="n">flipper_column</span> <span class="o">=</span> <span class="n">penguins</span><span class="o">.</span><span class="n">loc</span><span class="p">[:,</span><span class="s1">&#39;flipper_length_mm&#39;</span><span class="p">]</span>
<span class="n">flip</span> <span class="o">=</span> <span class="n">flipper_column</span><span class="o">.</span><span class="n">values</span>

<span class="n">box_plot</span> <span class="o">=</span> <span class="n">sns</span><span class="o">.</span><span class="n">boxplot</span><span class="p">(</span><span class="n">x</span> <span class="o">=</span> <span class="n">spe</span><span class="p">,</span> <span class="n">y</span> <span class="o">=</span> <span class="n">flip</span><span class="p">,</span> <span class="n">showmeans</span> <span class="o">=</span> <span class="kc">True</span><span class="p">,</span> <span class="n">meanprops</span> <span class="o">=</span> <span class="p">{</span><span class="s2">&quot;marker&quot;</span><span class="p">:</span> <span class="s2">&quot;+&quot;</span><span class="p">,</span> <span class="s2">&quot;markeredgecolor&quot;</span><span class="p">:</span> <span class="s2">&quot;black&quot;</span><span class="p">,</span>
                       <span class="s2">&quot;markersize&quot;</span><span class="p">:</span> <span class="s2">&quot;10&quot;</span><span class="p">})</span>
<span class="n">box_plot</span><span class="o">.</span><span class="n">set</span><span class="p">(</span><span class="n">xlabel</span> <span class="o">=</span> <span class="s1">&#39;Species&#39;</span><span class="p">,</span> <span class="n">ylabel</span> <span class="o">=</span> <span class="s1">&#39;Flipper Length&#39;</span><span class="p">,</span> <span class="n">title</span> <span class="o">=</span> <span class="s1">&#39;Species vs. Flipper Length&#39;</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[&nbsp;]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>[Text(0, 0.5, &#39;Flipper Length&#39;),
 Text(0.5, 0, &#39;Species&#39;),
 Text(0.5, 1.0, &#39;Species vs. Flipper Length&#39;)]</pre>
</div>

</div>

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>




<div class="jp-RenderedImage jp-OutputArea-output ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>Here the box plot illustrates the flipper length between each penguin species, we can see that Gentoo penguins still have a higher overall flipper length than Adelie and Chinstrap penguins, just like the distribution with the body mass. However in this plot also shows that Chinstrap penguins have slightly higher overall flipper lengths than Adelie penguins.</p>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[&nbsp;]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-python"><pre><span></span><span class="n">bill_column</span> <span class="o">=</span> <span class="n">penguins</span><span class="o">.</span><span class="n">loc</span><span class="p">[:,</span><span class="s1">&#39;bill_length_mm&#39;</span><span class="p">]</span>
<span class="n">bill</span> <span class="o">=</span> <span class="n">bill_column</span><span class="o">.</span><span class="n">values</span>

<span class="n">box_plot</span> <span class="o">=</span> <span class="n">sns</span><span class="o">.</span><span class="n">boxplot</span><span class="p">(</span><span class="n">x</span> <span class="o">=</span> <span class="n">spe</span><span class="p">,</span> <span class="n">y</span> <span class="o">=</span> <span class="n">bill</span><span class="p">,</span> <span class="n">showmeans</span> <span class="o">=</span> <span class="kc">True</span><span class="p">,</span> <span class="n">meanprops</span> <span class="o">=</span> <span class="p">{</span><span class="s2">&quot;marker&quot;</span><span class="p">:</span> <span class="s2">&quot;+&quot;</span><span class="p">,</span> <span class="s2">&quot;markeredgecolor&quot;</span><span class="p">:</span> <span class="s2">&quot;black&quot;</span><span class="p">,</span>
                       <span class="s2">&quot;markersize&quot;</span><span class="p">:</span> <span class="s2">&quot;10&quot;</span><span class="p">})</span>
<span class="n">box_plot</span><span class="o">.</span><span class="n">set</span><span class="p">(</span><span class="n">xlabel</span> <span class="o">=</span> <span class="s1">&#39;Species&#39;</span><span class="p">,</span> <span class="n">ylabel</span> <span class="o">=</span> <span class="s1">&#39;Bill Length&#39;</span><span class="p">,</span> <span class="n">title</span> <span class="o">=</span> <span class="s1">&#39;Species vs. Bill Length&#39;</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[&nbsp;]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>[Text(0, 0.5, &#39;Bill Length&#39;),
 Text(0.5, 0, &#39;Species&#39;),
 Text(0.5, 1.0, &#39;Species vs. Bill Length&#39;)]</pre>
</div>

</div>

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>




<div class="jp-RenderedImage jp-OutputArea-output ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>This box plot shows the Bill length between each penguin species. The major difference between this plot and the ones above is that Chinstrap penguins appears to have a higher overall bill length than the other two. On the other hand Adelie penguins have the lowest average bill length between the three species.</p>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[&nbsp;]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-python"><pre><span></span><span class="n">bill_d_column</span> <span class="o">=</span> <span class="n">penguins</span><span class="o">.</span><span class="n">loc</span><span class="p">[:,</span><span class="s1">&#39;bill_depth_mm&#39;</span><span class="p">]</span>
<span class="n">bill_d</span> <span class="o">=</span> <span class="n">bill_d_column</span><span class="o">.</span><span class="n">values</span>

<span class="n">box_plot</span> <span class="o">=</span> <span class="n">sns</span><span class="o">.</span><span class="n">boxplot</span><span class="p">(</span><span class="n">x</span> <span class="o">=</span> <span class="n">spe</span><span class="p">,</span> <span class="n">y</span> <span class="o">=</span> <span class="n">bill_d</span><span class="p">,</span> <span class="n">showmeans</span> <span class="o">=</span> <span class="kc">True</span><span class="p">,</span> <span class="n">meanprops</span> <span class="o">=</span> <span class="p">{</span><span class="s2">&quot;marker&quot;</span><span class="p">:</span> <span class="s2">&quot;+&quot;</span><span class="p">,</span> <span class="s2">&quot;markeredgecolor&quot;</span><span class="p">:</span> <span class="s2">&quot;black&quot;</span><span class="p">,</span>
                       <span class="s2">&quot;markersize&quot;</span><span class="p">:</span> <span class="s2">&quot;10&quot;</span><span class="p">})</span>
<span class="n">box_plot</span><span class="o">.</span><span class="n">set</span><span class="p">(</span><span class="n">xlabel</span> <span class="o">=</span> <span class="s1">&#39;Species&#39;</span><span class="p">,</span> <span class="n">ylabel</span> <span class="o">=</span> <span class="s1">&#39;Bill Depth&#39;</span><span class="p">,</span> <span class="n">title</span> <span class="o">=</span> <span class="s1">&#39;Species vs. Bill Depth&#39;</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[&nbsp;]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>[Text(0, 0.5, &#39;Bill Depth&#39;),
 Text(0.5, 0, &#39;Species&#39;),
 Text(0.5, 1.0, &#39;Species vs. Bill Depth&#39;)]</pre>
</div>

</div>

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>




<div class="jp-RenderedImage jp-OutputArea-output ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>This box plot shows the bill depth between each penguin species. We can see that Gentoo penguins have the lowest average bill depth among all three species, Adelie penguins and Chinstrap penguins have roughly the same distribution in terms of bill depth.</p>

</div>
</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h5 id="Bill-Depth-vs.-Bill-Length">Bill Depth vs. Bill Length<a class="anchor-link" href="#Bill-Depth-vs.-Bill-Length">&#182;</a></h5><p>We realized there may also be a relationship between bill depth vs. bill length, and that this ratio can probably provide an additional way/factor for us to distinguish the penguin species. So we plotted them out using scatter plots.</p>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[&nbsp;]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-python"><pre><span></span><span class="k">for</span> <span class="n">index</span><span class="p">,</span> <span class="n">col</span> <span class="ow">in</span> <span class="n">penguins</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="s1">&#39;species&#39;</span><span class="p">]):</span>
  <span class="n">bill_depth_array</span> <span class="o">=</span> <span class="n">col</span><span class="p">[</span><span class="s1">&#39;bill_depth_mm&#39;</span><span class="p">]</span>
  <span class="n">bill_length_array</span> <span class="o">=</span> <span class="n">col</span><span class="p">[</span><span class="s1">&#39;bill_length_mm&#39;</span><span class="p">]</span>
  <span class="n">fig</span><span class="p">,</span> <span class="n">ax</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">subplots</span><span class="p">()</span>
  <span class="n">ax</span><span class="o">.</span><span class="n">scatter</span><span class="p">(</span><span class="n">bill_depth_array</span><span class="p">,</span> <span class="n">bill_length_array</span><span class="p">)</span>
  <span class="n">ax</span><span class="o">.</span><span class="n">set_xlabel</span><span class="p">(</span><span class="s1">&#39;Bill Depth&#39;</span><span class="p">)</span>
  <span class="n">ax</span><span class="o">.</span><span class="n">set_ylabel</span><span class="p">(</span><span class="s1">&#39;Bill Length&#39;</span><span class="p">)</span>
  <span class="n">ax</span><span class="o">.</span><span class="n">set_title</span><span class="p">(</span><span class="sa">f</span><span class="s1">&#39;Bill Depth vs. Bill Length in </span><span class="si">{</span><span class="n">index</span><span class="si">}</span><span class="s1">&#39;</span><span class="p">)</span>

  <span class="n">x</span><span class="p">,</span> <span class="n">y</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">polyfit</span><span class="p">(</span><span class="n">bill_depth_array</span><span class="p">,</span> <span class="n">bill_length_array</span><span class="p">,</span> <span class="mi">1</span><span class="p">)</span>
  <span class="n">ax</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">penguins</span><span class="p">[</span><span class="s1">&#39;bill_depth_mm&#39;</span><span class="p">],</span> <span class="n">penguins</span><span class="p">[</span><span class="s1">&#39;bill_depth_mm&#39;</span><span class="p">]</span> <span class="o">*</span> <span class="n">x</span> <span class="o">+</span> <span class="n">y</span><span class="p">,</span> <span class="n">color</span> <span class="o">=</span> <span class="s1">&#39;red&#39;</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>




<div class="jp-RenderedImage jp-OutputArea-output ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>




<div class="jp-RenderedImage jp-OutputArea-output ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>




<div class="jp-RenderedImage jp-OutputArea-output ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>These three scatter plots shows the bill depth compared to bill length for each species. We did a regression line on these three plots and observed that there is a positive correlation between the bill depth and bill length, meaning that the higher the bill length the higher the bill depth. We will have a combined scatter plot below that shows all three species distribution in one plot.</p>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[&nbsp;]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-python"><pre><span></span><span class="n">scatter_plot</span> <span class="o">=</span> <span class="n">sns</span><span class="o">.</span><span class="n">scatterplot</span><span class="p">(</span><span class="n">data</span> <span class="o">=</span> <span class="n">penguins</span><span class="p">,</span> <span class="n">x</span> <span class="o">=</span> <span class="s2">&quot;bill_depth_mm&quot;</span><span class="p">,</span> <span class="n">y</span> <span class="o">=</span> <span class="s2">&quot;bill_length_mm&quot;</span><span class="p">,</span> <span class="n">hue</span> <span class="o">=</span> <span class="s2">&quot;species&quot;</span><span class="p">)</span>
<span class="n">scatter_plot</span><span class="o">.</span><span class="n">set</span><span class="p">(</span><span class="n">xlabel</span> <span class="o">=</span> <span class="s1">&#39;Bill Depth&#39;</span><span class="p">,</span> <span class="n">ylabel</span> <span class="o">=</span> <span class="s1">&#39;Bill Length&#39;</span><span class="p">,</span> <span class="n">title</span> <span class="o">=</span> <span class="s1">&#39;Bill Length vs. Bill Depth across different Species&#39;</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[&nbsp;]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>[Text(0, 0.5, &#39;Bill Length&#39;),
 Text(0.5, 0, &#39;Bill Depth&#39;),
 Text(0.5, 1.0, &#39;Bill Length vs. Bill Depth across different Species&#39;)]</pre>
</div>

</div>

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>




<div class="jp-RenderedImage jp-OutputArea-output ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>This scatter plot shows the bill depth compared to bill length across all three species. In this plot we can observe more clearly that Gentoo penguins generally have lower bill depth than Chinstrap and Adelie penguins. Adelie penguins have the lowest bill length but tend to have a overall higher bill depth. Chinstrap penguins have higher bill length than adelie penguins, which is roughly similar to Gentoo penguins, but they also have similar bill depth distribution with adelie penguins.</p>

</div>
</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h5 id="Male-vs.-Female">Male vs. Female<a class="anchor-link" href="#Male-vs.-Female">&#182;</a></h5><p>We also futher explored the difference between male and female body masses among different species and could clearly see that there is a significant difference which can aid us in distinguishing the sex of a penguin withn a species of penguin.</p>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[&nbsp;]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-python"><pre><span></span><span class="n">adelie</span> <span class="o">=</span> <span class="n">penguins</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="n">penguins</span><span class="p">[</span><span class="s1">&#39;species&#39;</span><span class="p">]</span> <span class="o">==</span> <span class="s2">&quot;Adelie&quot;</span><span class="p">]</span>
<span class="n">box_plot</span> <span class="o">=</span> <span class="n">sns</span><span class="o">.</span><span class="n">boxplot</span><span class="p">(</span><span class="n">data</span><span class="o">=</span><span class="n">adelie</span><span class="p">,</span> <span class="n">x</span> <span class="o">=</span> <span class="s1">&#39;sex&#39;</span><span class="p">,</span> <span class="n">y</span> <span class="o">=</span> <span class="s1">&#39;body_mass_g&#39;</span><span class="p">,</span> <span class="n">order</span> <span class="o">=</span> <span class="p">[</span><span class="s1">&#39;male&#39;</span><span class="p">,</span> <span class="s1">&#39;female&#39;</span><span class="p">])</span>
<span class="n">box_plot</span><span class="o">.</span><span class="n">set</span><span class="p">(</span><span class="n">xlabel</span> <span class="o">=</span> <span class="s1">&#39;Sex&#39;</span><span class="p">,</span> <span class="n">ylabel</span> <span class="o">=</span> <span class="s1">&#39;Body Mass&#39;</span><span class="p">,</span> <span class="n">title</span> <span class="o">=</span> <span class="s1">&#39;Sex vs. Body Mass for Adelie Penguins&#39;</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[&nbsp;]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>[Text(0, 0.5, &#39;Body Mass&#39;),
 Text(0.5, 0, &#39;Sex&#39;),
 Text(0.5, 1.0, &#39;Sex vs. Body Mass for Adelie Penguins&#39;)]</pre>
</div>

</div>

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>




<div class="jp-RenderedImage jp-OutputArea-output ">
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAZMAAAEcCAYAAAAC+llsAAAABHNCSVQICAgIfAhkiAAAAAlwSFlzAAALEgAACxIB0t1+/AAAADh0RVh0U29mdHdhcmUAbWF0cGxvdGxpYiB2ZXJzaW9uMy4yLjIsIGh0dHA6Ly9tYXRwbG90bGliLm9yZy+WH4yJAAAgAElEQVR4nO3de1iUdf7/8ecMJzUQlFBAK8rviq7WLoqVeUYrSQMP2VddrU1bNfNQhoc8QFJoktVqYpqa7pZmBxPFMFPHQ5q5kFhpaSumm4KoIAYEcpj794c/5xvraXRkRvT1uC6vi7k/9+F9DzivuT/34WMyDMNARETEAWZXFyAiItWfwkRERBymMBEREYcpTERExGEKExERcZjCREREHKYwkRvOp59+Sr9+/VxdhkNKSkoYNmwYLVu2ZNSoUS6pITQ0lMOHD192vp07d9K+fXvb627durFz586qLM1p0tPTefjhh11dRrWgMLmBpKen07dvX1q2bMm9995L3759+e6771xd1mUdOXKE0NBQwsLCCAsL44EHHuCll16irKzM6bWEhobSunVrysvLbdPKyspo3bo1oaGhTqvj888/5+TJk+zcuZPZs2dfs/X+8ssvNGnShLi4uGu2zv/22Wefcd99913xcjt37qRJkya2v4OHH36YFStWVEGF9gsPD2fdunUuraG6UJjcIAoLCxk2bBgDBgzgX//6F1u3bmXEiBF4enq6ujS7paWlkZGRQUpKCrt372bp0qUuqaN27dps3brV9nrr1q3Url3bqTVkZWUREhKCu7v7FS/7+yD8b6tWrcLX15e1a9dSWlrqSIlVol69emRkZLBr1y7Gjh3LlClTOHDggKvLEjsoTG4QP//8MwDdu3fHzc2NGjVq0LZtW5o0aWKb55NPPiEyMpJWrVoxePBgjh49CsA777xDnz59bB9Cy5Yto1u3bpw5c+a87URGRrJp0ybb6/Lycu6//3727t3LmTNniImJ4b777iM8PJzevXtz8uTJK94Xf39/HnjgATIzM23TMjMzGThwIOHh4XTr1o2NGzfa2k6dOsWwYcNo0aIFjz32GP/5z39sbVOnTuXVV1+ttP5hw4axZMmSi24/Ojqa5ORk2+tVq1bRo0ePSvOsWLGCyMhIwsLC6Ny5M8uXL7e15eXlMXToUMLDw7n33nvp378/VqsVOPtet2vXzvbNe8eOHedtf/bs2cydO5e1a9cSFhbGxx9/jNVqZe7cuXTq1InWrVszbtw4CgoKgP87svv444/p2LEjTz755AX3yzAMkpOTGT16NO7u7lgslkrtCxcupG3btrRt25ZPPvmkUltpaSkzZsygY8eOPPDAA8TGxlJSUnLB7URERPDVV18BYLVaeeedd+jSpQv33Xcfo0ePJj8//4LL/Z7JZKJLly7Url2bAwcOXHI95/Z/5cqVdOzYkfvuu4+3337btq6SkhLGjx9Pq1atiIyMZMGCBZW65f67O2/ChAm8+eabwPldeBERESxatIhHH32Uli1b8txzz9n+n1zq934zUJjcIO68807c3NwYP348W7Zs4fTp05XaN2zYwPz585kzZw47duygZcuWvPDCCwA8/fTTeHp68vbbb3Po0CHefPNNXnvtNby8vM7bTrdu3VizZo3t9bZt26hTpw7NmjVj5cqVFBYWsnnzZnbu3MnUqVOpUaPGFe9LTk4O27Zt409/+hNwtptp2LBhtGnThq+++orJkycTExPDwYMHAYiPj8fLy4tt27Yxbdq0Sl0jPXv2ZM2aNbb/1Hl5eezYsYPu3btfdPtdunQhPT2dX3/9ldOnT5Oenk7nzp0rzePv78/8+fPZtWsX06dPZ/r06ezduxeAxYsXU79+fXbs2MH27dsZM2YMJpOJgwcPsnTpUj755BMyMjJYtGgRDRo0OG/7o0aNYujQoURGRpKRkUGfPn349NNPWblyJf/85z/ZsGEDv/32G/Hx8ZWWS0tLIzU1lUWLFl1wv7755huOHTtGt27diIyMrBSYW7du5d133+Xdd9/liy++OC/kZs6cyc8//0xycjJffPEFx48fJykp6aLv4TnvvfceGzZs4P333+fLL7/E19f3vLovxGq1sn79egoKCmjcuLFd6/nmm2/4/PPP+cc//kFSUpLty8icOXM4evQoGzZsYPHixaxevfqy27+UtWvXsnDhQjZu3Mj+/fv59NNPgYv/3m8WCpMbhLe3N8uWLcNkMjFlyhRat27NsGHDbEcGy5cvZ8iQITRq1Ah3d3eGDRvGjz/+yNGjRzGbzcyYMYP33nuPZ555hqeffpo//vGPF9zOo48+isViobi4GICUlBS6desGgLu7O/n5+Rw+fBg3NzeaN2+Ot7e33ftw//33Ex4eTvv27alVqxZdu3YF4Ntvv+W3335jyJAheHp60rp1azp16sRnn31GRUUFX3zxBaNGjaJWrVo0btyYnj172tZ5zz334OPjY/twTE1N5d577+XWW2+9aB1eXl506tSJ1NRUUlNTiYiIOC9YO3bsyO23347JZOLee++lTZs2pKen296HEydOkJWVhYeHB+Hh4ZhMJtzc3CgtLSUzM5OysjIaNmzI7bffbtd7k5KSwl//+lduu+02brnlFsaMGUNqamqlLq2RI0dSq1atiwb4ypUrad++Pb6+vnTv3p0vv/yS3Nxc4OwHZK9evWjcuDG1atVixIgRtuUMw+Cjjz5i4sSJ+Pn54e3tzdChQ/nss88uW/fy5ct5/vnnCQwMxNPTkxEjRrBu3bqLdsUdP36c8PBw7r//fubMmUNiYiJ33XWXXesZMWIENWrUoEmTJjRp0oR9+/bZ9m3o0KH4+voSGBjIE088cfk3/BIGDhxI/fr18fPzo1OnTvz444/AxX/vN4sr75CV61ajRo1sXTqZmZmMHTuWadOm8cYbb5CVlcW0adOYMWOGbX7DMMjJyaFBgwY0bNiQ++67jy1btvCXv/zlotu44447aNSoEZs2baJTp05YLBbbN9zo6GiOHTvGmDFj+PXXX4mKiuL555/Hw8PDrvq//vpr3N3dKSkpYdasWQwePJgPP/yQ48ePExgYiNn8f999goODycnJIS8vj/LycoKCgiq1/V7Pnj1ZvXo1bdq0YfXq1XZ9mPTo0YPXX38dgJiYmPPat2zZQlJSEocOHcJqtVJSUkLjxo0BGDx4MHPmzGHQoEEA/O///i9DhgzhjjvuYOLEibz11lscOHCAtm3bMmHCBOrXr3/Zeo4fP17pKKZBgwaUl5fbwgAgMDDwosuXlJTw+eef88orrwAQFhZGUFCQLaSOHz9O8+bNK63/nLy8PIqLi+nVq5dtmmEYdnXhZGVl8eyzz1b63ZnNZnJzcy+43/Xq1at0vsqe9Zzz+y8INWvW5LfffgPOvne///u41Ptkj4CAgErbOX78OHDx3/vNQkcmN6hGjRrRq1cv/v3vfwMQFBTE1KlTSU9Pt/377rvvaNGiBQCbN28mIyOD1q1bk5iYeMl1d+/enTVr1rBx40b+53/+hzvuuAMADw8PRowYQWpqKsuXL2fz5s2VulLsVaNGDXr16sXu3bvJy8ujXr16HDt2rNKHV3Z2NvXr16du3bq4u7uTnZ1dqe33oqKi2LhxI/v27SMzM5MuXbpctobw8HBOnDjByZMnadmyZaW20tJSRo0axaBBg9i+fTvp6em0b9+ecw/g9vb2ZsKECWzcuJG3336bxYsX246MHn30UT744AM2bdqEyWRi5syZdr0n9erVs53jgrMfru7u7vj7+9umXepb8Pr16yksLGTq1Km0adOGNm3akJOTY/v91KtXr9L7lpWVZfu5Tp061KhRg88++8z2t/PNN9+QkZFx2boDAwNZsGBBpb+777//3q4AvVbrCQgI4NixY7bXv/8ZzgbCuSNtgBMnTlxRbedc6vd+M1CY3CAyMzN59913bf9RsrOzWbNmje28Q9++fXnnnXds4VJQUMDatWuBs988J0+eTEJCAq+++ioWi4UtW7ZcdFuPPPII27dv54MPPqh07uHrr79m//79VFRU4O3tjbu7e6VvkvYqLS1l1apVBAQEUKdOHe655x5q1KjBwoULKSsrY+fOnVgsFh555BHc3Nx48MEHmTNnDsXFxRw4cICVK1dWWl9gYCB33303Y8eO5aGHHrLrPI7JZGLevHm8/fbb531Il5aWUlpaaguyLVu2sH37dlv7pk2bOHz4MIZh4OPjg5ubm+2cyY4dOygtLcXT0xMvLy+735/u3bvzj3/8g19++YWioiLefPNNIiMj7b7aKzk5md69e5OSkkJycjLJycl88MEH7Nu3j/3799O1a1dWrlzJgQMHKC4uZs6cObZlzWYzffr0Ydq0abYjgZycHL788svLbrdfv378/e9/twVhXl4eGzZssKvma7WeyMhI5s+fz+nTp8nJyeH999+v1N6kSRPWrFlDRUUFW7duJS0t7Yrrg4v/3m8W6ua6QXh7e/Ptt9+yePFiCgoK8PHxoVOnTowbNw6ABx98kKKiIsaMGcPRo0fx8fHhgQceIDIyktjYWCIiIujQoQMACQkJTJo0iZSUFOrUqXPeturVq8ef//xn0tLS+Pvf/26bfvLkSeLi4sjJyaFWrVo88sgjREdHAxAbGwtwyZOvrVq1AsDNzY0mTZowd+5cTCYTnp6ezJs3j6lTpzJ//nzq169PYmIijRo1sq37xRdfpE2bNtx111306tXrvJvmevTowbhx45g0aZLd7+kf/vCHC0739vZm8uTJPPfcc5SWltKp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
"
>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>This box plot shows the body mass distribution for male and female Adelie penguins. According to the plot, we can see that male Adelie penguins tend to have a much higher body mass than female Adelie penguins.</p>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[&nbsp;]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-python"><pre><span></span><span class="n">gentoo</span> <span class="o">=</span> <span class="n">penguins</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="n">penguins</span><span class="p">[</span><span class="s1">&#39;species&#39;</span><span class="p">]</span> <span class="o">==</span> <span class="s2">&quot;Gentoo&quot;</span><span class="p">]</span>
<span class="n">box_plot</span> <span class="o">=</span> <span class="n">sns</span><span class="o">.</span><span class="n">boxplot</span><span class="p">(</span><span class="n">data</span><span class="o">=</span><span class="n">gentoo</span><span class="p">,</span> <span class="n">x</span> <span class="o">=</span> <span class="s1">&#39;sex&#39;</span><span class="p">,</span> <span class="n">y</span> <span class="o">=</span> <span class="s1">&#39;body_mass_g&#39;</span><span class="p">,</span> <span class="n">order</span> <span class="o">=</span> <span class="p">[</span><span class="s1">&#39;male&#39;</span><span class="p">,</span> <span class="s1">&#39;female&#39;</span><span class="p">])</span>
<span class="n">box_plot</span><span class="o">.</span><span class="n">set</span><span class="p">(</span><span class="n">xlabel</span> <span class="o">=</span> <span class="s1">&#39;Sex&#39;</span><span class="p">,</span> <span class="n">ylabel</span> <span class="o">=</span> <span class="s1">&#39;Body Mass&#39;</span><span class="p">,</span> <span class="n">title</span> <span class="o">=</span> <span class="s1">&#39;Sex vs. Body Mass for Gentoo Penguins&#39;</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[&nbsp;]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>[Text(0, 0.5, &#39;Body Mass&#39;),
 Text(0.5, 0, &#39;Sex&#39;),
 Text(0.5, 1.0, &#39;Sex vs. Body Mass for Gentoo Penguins&#39;)]</pre>
</div>

</div>

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>




<div class="jp-RenderedImage jp-OutputArea-output ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>This box plot shows the body mass distribution for male and female Gentoo penguins. Just like what we observed for Adelie penguins, we can see that male Gentoo penguins also tend to have a much higher body mass than female Gentoo penguins.</p>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[&nbsp;]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-python"><pre><span></span><span class="n">chinstrap</span> <span class="o">=</span> <span class="n">penguins</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="n">penguins</span><span class="p">[</span><span class="s1">&#39;species&#39;</span><span class="p">]</span> <span class="o">==</span> <span class="s2">&quot;Chinstrap&quot;</span><span class="p">]</span>
<span class="n">box_plot</span> <span class="o">=</span> <span class="n">sns</span><span class="o">.</span><span class="n">boxplot</span><span class="p">(</span><span class="n">data</span><span class="o">=</span><span class="n">chinstrap</span><span class="p">,</span> <span class="n">x</span> <span class="o">=</span> <span class="s1">&#39;sex&#39;</span><span class="p">,</span> <span class="n">y</span> <span class="o">=</span> <span class="s1">&#39;body_mass_g&#39;</span><span class="p">,</span> <span class="n">order</span> <span class="o">=</span> <span class="p">[</span><span class="s1">&#39;male&#39;</span><span class="p">,</span> <span class="s1">&#39;female&#39;</span><span class="p">])</span>
<span class="n">box_plot</span><span class="o">.</span><span class="n">set</span><span class="p">(</span><span class="n">xlabel</span> <span class="o">=</span> <span class="s1">&#39;Sex&#39;</span><span class="p">,</span> <span class="n">ylabel</span> <span class="o">=</span> <span class="s1">&#39;Body Mass&#39;</span><span class="p">,</span> <span class="n">title</span> <span class="o">=</span> <span class="s1">&#39;Sex vs. Body Mass for Chinstrap Penguins&#39;</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[&nbsp;]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>[Text(0, 0.5, &#39;Body Mass&#39;),
 Text(0.5, 0, &#39;Sex&#39;),
 Text(0.5, 1.0, &#39;Sex vs. Body Mass for Chinstrap Penguins&#39;)]</pre>
</div>

</div>

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>




<div class="jp-RenderedImage jp-OutputArea-output ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>This last box plot on body mass shows the body mass distribution for male and female Chinstrap penguins. Although male Chinstrap penguins appear to have higher body mass than female Chinstrap penguins as well, the difference between body mass of male and female Chinstrap penguins is significantly smaller than Adelie and Gentoo penguins.</p>

</div>
</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h2 id="Machine-Learning-and-Analysis">Machine Learning and Analysis<a class="anchor-link" href="#Machine-Learning-and-Analysis">&#182;</a></h2><p>In this portion we will use a machine learning model created with a decision tree classifier to classify our data. We would like to show that the penguin species can be classified effectively using the characteristic measurements provided in the dataset.</p>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[&nbsp;]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-python"><pre><span></span><span class="kn">from</span> <span class="nn">sklearn.model_selection</span> <span class="kn">import</span> <span class="n">train_test_split</span>
<span class="kn">from</span> <span class="nn">sklearn.tree</span> <span class="kn">import</span> <span class="n">DecisionTreeClassifier</span>
<span class="kn">from</span> <span class="nn">sklearn.metrics</span> <span class="kn">import</span> <span class="n">classification_report</span>
<span class="kn">from</span> <span class="nn">sklearn.metrics</span> <span class="kn">import</span> <span class="n">confusion_matrix</span>

<span class="n">penguin_data</span> <span class="o">=</span> <span class="n">load_penguins</span><span class="p">(</span><span class="n">return_X_y</span> <span class="o">=</span> <span class="kc">True</span><span class="p">)</span>

<span class="n">x</span> <span class="o">=</span> <span class="n">penguin_data</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span>
<span class="n">y</span> <span class="o">=</span> <span class="n">penguin_data</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span>

<span class="n">x_train</span><span class="p">,</span> <span class="n">x_test</span><span class="p">,</span> <span class="n">y_train</span><span class="p">,</span> <span class="n">y_test</span> <span class="o">=</span> <span class="n">train_test_split</span><span class="p">(</span><span class="n">x</span><span class="p">,</span> <span class="n">y</span><span class="p">,</span> <span class="n">test_size</span> <span class="o">=</span> <span class="mi">100</span><span class="p">,</span> <span class="n">random_state</span> <span class="o">=</span> <span class="mi">0</span><span class="p">)</span>

<span class="n">clf</span> <span class="o">=</span> <span class="n">DecisionTreeClassifier</span><span class="p">()</span>
<span class="n">x_train</span> <span class="o">=</span> <span class="n">x_train</span><span class="o">.</span><span class="n">fillna</span><span class="p">(</span><span class="n">x_train</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span>
<span class="n">clf</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">x_train</span><span class="p">,</span> <span class="n">y_train</span><span class="p">)</span>
<span class="n">predictions</span> <span class="o">=</span> <span class="n">clf</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">x_test</span><span class="p">)</span>

<span class="nb">print</span><span class="p">(</span><span class="n">classification_report</span><span class="p">(</span><span class="n">y_test</span><span class="p">,</span> <span class="n">predictions</span><span class="p">))</span>
<span class="nb">print</span><span class="p">(</span><span class="n">confusion_matrix</span><span class="p">(</span><span class="n">y_test</span><span class="p">,</span> <span class="n">predictions</span><span class="p">))</span>
<span class="nb">print</span><span class="p">(</span><span class="n">clf</span><span class="o">.</span><span class="n">score</span><span class="p">(</span><span class="n">x_test</span><span class="p">,</span> <span class="n">y_test</span><span class="p">))</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>


<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain">
<pre>              precision    recall  f1-score   support

      Adelie       0.94      0.98      0.96        48
   Chinstrap       0.94      0.85      0.89        20
      Gentoo       1.00      1.00      1.00        32

    accuracy                           0.96       100
   macro avg       0.96      0.94      0.95       100
weighted avg       0.96      0.96      0.96       100

[[47  1  0]
 [ 3 17  0]
 [ 0  0 32]]
0.96
</pre>
</div>
</div>

</div>

</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>The code above illustrates a machine learning model that uses the data from the penguins dataset to predict and classify a penguin's species from its data(bill length, bill depth, flipper length etc.). According to the resulting confusion matrix and score, we can see that this model has done a pretty good job in correctly predicting the species of each penguin.</p>

</div>
</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h2 id="Conclusion">Conclusion<a class="anchor-link" href="#Conclusion">&#182;</a></h2><p>Throughout this tutorial, we can see that each penguin has their unique characteristics and it is distinguishable just by observing these characteristics. As an example, Adelie penguins have a large bill depth, small bill length, small flipper length, and small body mass. Gentoo penguins in contrast have smaller bill depth, longer bill length, longer flipper length, and larger body mass. It is also easy to tell if a penguin is male or female by their body mass measurement, combining with other measurements we can identify a penguin's sex and species.
Why is it important to study penguins and explore ways to distinguish penguin species like we did in this tutorial? It is important because by studying penguins through these data, we can understand their biology, population dynamics, habitats, and their role within the Antarctic ecosystem as well as within the world. As global warming worsens, it is even more important to study living creatures like penguins in Antarctica. Here are some more resources that we found interesting and useful to better understand Antarctica and the penguins living there:</p>
<p><a href="https://www.coolantarctica.com/Antarctica%20fact%20file/wildlife/antarctic-penguins.php">https://www.coolantarctica.com/Antarctica%20fact%20file/wildlife/antarctic-penguins.php</a></p>
<p><a href="https://www.europeanpolarboard.org/fileadmin/news/FINAL_EPB_SCAR_Biology_panel_summary.pdf">https://www.europeanpolarboard.org/fileadmin/news/FINAL_EPB_SCAR_Biology_panel_summary.pdf</a></p>

</div>
</div>
</body>







</html>
