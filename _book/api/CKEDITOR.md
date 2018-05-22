# CKEDITOR
这是API入口点。整个CKEditor代码运行在这个对象下

## 配置选项

** disableAutoInline ** : 布尔

对于 `contenteditable`属性设置为`true`的元素，禁止自动创建内联编辑器。

      CKEDITOR.disableAutoInline = true;

默认为`false`
<hr>
** replaceClass ** : 字符串

用于识别CKEditor实例替换的 `<textarea>` 元素的类名称。 将其设置为 empty/`null`以禁用此功能。

      CKEDITOR.replaceClass = 'rich_editor';
      
默认为 `ckeditor`
<hr>
** skinName ** : 字符串

要为所有创建的实例加载的外观，它可能是编辑器安装路径内的外观文件夹的名称，或者用逗号分隔的名称和路径。

**注意**： 这是适用于所有实例的全局配置。

      CKEDITOR.skinName = 'moono';

      CKEDITOR.skinName = 'myskin,/customstuff/myskin/';
      
默认为  `moono-lisa`

## 属性

**ALT** : 数字  *<span style="border:1px solid #999">只读<span>*

ALT键（0x440000）。

默认为 `0x440000`

<hr>
**CTRL** : 数字  *<span style="border:1px solid #999">只读<span>*

CTRL键（0x110000）。

默认为 `0x110000`

<hr>
**DATA_TRANSFER_CROSS_EDITORS** : 数字  *<span style="border:1px solid #999">只读<span>*

数据传输操作（拖放或复制和粘贴）在一个编辑器实例中启动，并在另一个编辑器实例中结束。

默认为`2`
<hr>
**DATA_TRANSFER_EXTERNAL** : 数字  *<span style="border:1px solid #999">只读<span>*

数据传输操作（拖放或复制和粘贴）在编辑器之外启动。数据的来源可能是textarea，HTML，另一个应用程序等。

默认为 `3`
<hr>
**DATA_TRANSFER_INTERNAL** : 数字  *<span style="border:1px solid #999">只读<span>*

数据传输操作（拖放或复制和粘贴）在同一个编辑器实例中开始和结束。

默认为 `1`
<hr>
**DIALOG_RESIZE_BOTH** : 数字  *<span style="border:1px solid #999">只读<span>*

允许对话框在两个方向上调整大小。

默认为 `3`
<hr>
**DIALOG_RESIZE_HEIGHT** : 数字  *<span style="border:1px solid #999">只读<span>*

只允许对话框垂直调整，禁用水平调整。

默认为 `2`
<hr>
**DIALOG_RESIZE_NONE** : 数字  *<span style="border:1px solid #999">只读<span>*

禁止调整对话框大小

默认为 `0`
<hr>
**DIALOG_RESIZE_WIDTH** : 数字  *<span style="border:1px solid #999">只读<span>*

只允许对该对话框进行水平调整，禁用垂直调整。

默认为 `1`
<hr>
**DIALOG_STATE_BUSY** : 数字  *<span style="border:1px solid #999">只读<span>*

对话框状态是否运行，

默认为 `2`
<hr>
**DIALOG_STATE_IDLE** :数字  *<span style="border:1px solid #999">只读<span>*

对话框状态是否闲置。

默认为 `1`
<hr>
ELEMENT_MODE_APPENDTO : 数字  *<span style="border:1px solid #999">只读<span>*

编辑器将在元素内部创建。

默认为 `2`