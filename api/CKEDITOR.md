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
**ELEMENT_MODE_APPENDTO** : 数字  *<span style="border:1px solid #999">只读<span>*

编辑器将在元素内部创建。

默认为 `2`
<hr>
**ELEMENT_MODE_INLINE** : 数字  *<span style="border:1px solid #999">只读<span>*

编辑器将被附加到该元素，并将其用作编辑块。

默认为 `3`
<hr>
**ELEMENT_MODE_NONE** : 数字  *<span style="border:1px solid #999">只读<span>*

编辑器没有关联的元素。

默认为 `0`
<hr>
**ELEMENT_MODE_REPLACE** : 数字  *<span style="border:1px solid #999">只读<span>*

该元素将被编辑器实例替换。

默认为 `1`
<hr>
**END** : 数字  *<span style="border:1px solid #999">只读<span>*

请参阅CKEDITOR.dom.range.checkBoundaryOfElement。

默认为 `2`
<hr>
**ENLARGE_BLOCK_CONTENTS** : 数字  *<span style="border:1px solid #999">只读<span>*

默认为 `2`
<hr>
**ENLARGE_ELEMENT** : 数字  *<span style="border:1px solid #999">只读<span>*

默认为 `1`
<hr>
**ENLARGE_INLINE** : 数字  *<span style="border:1px solid #999">只读<span>*

默认为 `4`
<hr>
**ENLARGE_LIST_ITEM_CONTENTS** : 数字  *<span style="border:1px solid #999">只读<span>*

默认为 `3`
<hr>
**ENTER_BR** : 数字  *<span style="border:1px solid #999">只读<span>*

与CKEDITOR.config.enterMode和CKEDITOR.config.shiftEnterMode配置设置一起使用，以使编辑器在使用Enter键时生成`<br>`标签。

默认为 `2`

<hr>
**ENTER_DIV** : 数字  *<span style="border:1px solid #999">只读<span>*

与CKEDITOR.config.enterMode和CKEDITOR.config.shiftEnterMode配置设置一起使用，以使编辑器在使用Enter键时生成`<div>`标签。

默认为 `3`

<hr>
**ENTER_P** : 数字  *<span style="border:1px solid #999">只读<span>*

与CKEDITOR.config.enterMode和CKEDITOR.config.shiftEnterMode配置设置一起使用，以使编辑器在使用Enter键时生成`<p>`标签。

默认为 `1`
<hr>
**EVENT_PHASE_AT_TARGET** : 数字  *<span style="border:1px solid #999">只读<span>*

目标事件。

默认为 `2`
<hr>
**EVENT_PHASE_BUBBLING** : 数字  *<span style="border:1px solid #999">只读<span>*

冒泡阶段

默认为 `3`
<hr>
**EVENT_PHASE_CAPTURING** : 数字  *<span style="border:1px solid #999">只读<span>*

捕获阶段。

默认为 `1`
<hr>
**FILTER_SKIP_TREE** : 数字  *<span style="border:1px solid #999">只读<span>*

指示当前元素及其所有祖先不应被过滤的标志。

有关更多详细信息，请参阅CKEDITOR.filter.addElementCallback。

默认为 `2`
<hr>
**LINEUTILS_AFTER** : 数字  *<span style="border:1px solid #999">只读<span>*

确定相对DOM中某个元素的位置（之后）。

默认为 `2`

<hr>
**LINEUTILS_BEFORE** : 数字  *<span style="border:1px solid #999">只读<span>*

确定相对于DOM中元素的位置（之前）。

默认为  `0`
<hr>
**LINEUTILS_INSIDE** : 数字  *<span style="border:1px solid #999">只读<span>*

确定DOM中相对于元素的位置（内部）。

默认为 `4`
<hr>
**MOUSE_BUTTON_LEFT** : 数字  *<span style="border:1px solid #999">只读<span>*

鼠标左键。

默认为 `0`

<hr>
**MOUSE_BUTTON_MIDDLE** : 数字  *<span style="border:1px solid #999">只读<span>*

鼠标中键。

默认为 `1`
<hr>
**MOUSE_BUTTON_RIGHT** : 数字  *<span style="border:1px solid #999">只读<span>*

鼠标右键。

默认为 `2`
<hr>
**NODE_COMMENT** : 数字  *<span style="border:1px solid #999">只读<span>*

注释节点类型。

默认为 `8`
<hr>
**NODE_DOCUMENT** : 数字  *<span style="border:1px solid #999">只读<span>*

文档节点类型。

默认为 `9`

<hr>
**NODE_DOCUMENT_FRAGMENT** : 数字  *<span style="border:1px solid #999">只读<span>*

文档片段节点类型。

默认为 `11`

<hr>
**NODE_ELEMENT** : 数字  *<span style="border:1px solid #999">只读<span>*

元素节点类型。

默认为 `1`
<hr>
**NODE_TEXT** : 数字  *<span style="border:1px solid #999">只读<span>*

文本节点类型。

默认为 `3`
<hr>
**POSITION_AFTER_END** : 数字  *<span style="border:1px solid #999">只读<span>*

指示节点结束后的位置。

      // When used according to an element:
      // <element>contents</element>^ (range is anchored in element's parent)

      // When used according to a text node:
      // "text"^ (range is anchored in text node's parent)

它用作如下方法的参数：CKEDITOR.dom.range.moveToPosition， CKEDITOR.dom.range.setStartAt和CKEDITOR.dom.range.setEndAt。

默认为 `4`

<hr>
**POSITION_AFTER_START** : 数字  *<span style="border:1px solid #999">只读<span>*

指示节点开始后的位置。

      // When used according to an element:
      // <element>^contents</element>

      // When used according to a text node:
      // "^text" (range is anchored in the text node)

它用作如下方法的参数：CKEDITOR.dom.range.moveToPosition， CKEDITOR.dom.range.setStartAt和CKEDITOR.dom.range.setEndAt。

默认为 `1`
<hr>
**POSITION_BEFORE_END** : 数字  *<span style="border:1px solid #999">只读<span>*

指示节点结束之前的位置。

      // When used according to an element:
      // <element>contents^</element>

      // When used according to a text node:
      // "text^" (range is anchored in the text node)

它用作如下方法的参数：CKEDITOR.dom.range.moveToPosition， CKEDITOR.dom.range.setStartAt和CKEDITOR.dom.range.setEndAt。

默认为 `2`
<hr>
**POSITION_BEFORE_START** : 数字  *<span style="border:1px solid #999">只读<span>*

指示节点开始之前的位置。

      // When used according to an element:
      // ^<element>contents</element> (range is anchored in element's parent)

      // When used according to a text node:
      // ^"text" (range is anchored in text node's parent)

它用作如下方法的参数：CKEDITOR.dom.range.moveToPosition， CKEDITOR.dom.range.setStartAt和CKEDITOR.dom.range.setEndAt。

默认为 `3`
<hr>

**POSITION_CONTAINS** : 数字  *<span style="border:1px solid #999">只读<span>*

指示上下文节点包含其他节点。请参阅CKEDITOR.dom.node.getPosition。

默认为 `16`
<hr>
**POSITION_DISCONNECTED** : 数字  *<span style="border:1px solid #999">只读<span>*

指示节点位于不同（分离）的树中。请参阅CKEDITOR.dom.node.getPosition。

默认为 `1`

<hr>
**POSITION_FOLLOWING** : 数字  *<span style="border:1px solid #999">只读<span>*

表示上下文节点在其他节点之后。请参阅CKEDITOR.dom.node.getPosition。

默认为 `2`
<hr>
**POSITION_IDENTICAL** : 数字  *<span style="border:1px solid #999">只读<span>*

指示两个节点的位置相同（这是相同的节点）。请参阅CKEDITOR.dom.node.getPosition。

默认为 `0`
<hr>
**POSITION_IS_CONTAINED** : 数字  *<span style="border:1px solid #999">只读<span>*

指示上下文节点是另一个节点的后代。请参阅CKEDITOR.dom.node.getPosition。

默认为 `8`
<hr>
**POSITION_PRECEDING** : 数字  *<span style="border:1px solid #999">只读<span>*

表示上下文节点位于另一个节点的前面。请参阅CKEDITOR.dom.node.getPosition。

默认为 4
<hr>
**ELECTION_ELEMENT** : 数字  *<span style="border:1px solid #999">只读<span>*

元素选择。

      if ( editor.getSelection().getType() == CKEDITOR.SELECTION_ELEMENT )
          alert( 'An element is selected' );
          
默认为 `3`
<hr>
**SELECTION_NONE** : 数字  *<span style="border:1px solid #999">只读<span>*

没有选择。

      if ( editor.getSelection().getType() == CKEDITOR.SELECTION_NONE )
          alert( 'Nothing is selected' );
          
默认为 `1`
<hr>
**SELECTION_TEXT** : 数字  *<span style="border:1px solid #999">只读<span>*

文字或折叠选择。

      if ( editor.getSelection().getType() == CKEDITOR.SELECTION_TEXT )
          alert( 'A text is selected' );
          
默认为 `2`
<hr>
**SHIFT** : 数字  *<span style="border:1px solid #999">只读<span>*

SHIFT键（0x220000）。

默认为 `0x220000`
<hr>
**SHRINK_ELEMENT** : 数字  *<span style="border:1px solid #999">只读<span>*

请参阅CKEDITOR.dom.range.shrink。

默认为 `1`
<hr>
**SHRINK_TEXT** : 数字  *<span style="border:1px solid #999">只读<span>*

请参阅CKEDITOR.dom.range.shrink。

默认为 `2`
<hr>
**START** : 数字  *<span style="border:1px solid #999">只读<span>*

请参阅CKEDITOR.dom.range.checkBoundaryOfElement。

默认为 `1`
<hr>
**STYLE_BLOCK** : 数字  *<span style="border:1px solid #999">只读<span>*

块样式类型。

在CKEDITOR.style类文档中阅读更多内容。

默认为 `1`
<hr>
**STYLE_INLINE** : 数字  *<span style="border:1px solid #999">只读<span>*

内联样式类型。

在[CKEDITOR.style](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_style.html)类文档中阅读更多内容。

默认为 `2`
<hr>
**STYLE_OBJECT** : 数字  *<span style="border:1px solid #999">只读<span>*

对象样式类型。

在[CKEDITOR.style](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_style.html)类文档中阅读更多内容。

默认为  `3`
<hr>
**TRISTATE_DISABLED** : 数字  *<span style="border:1px solid #999">只读<span>*

用于指示DISABLED状态。

默认为 `0`
<hr>
**TRISTATE_OFF** : 数字  *<span style="border:1px solid #999">只读<span>*

用于指示OFF或INACTIVE状态。

默认为 `2`
<hr>
**TRISTATE_ON** : 数字  *<span style="border:1px solid #999">只读<span>*

用于指示ON或ACTIVE状态。

默认为 `1`
<hr>
**UI_BUTTON** : 字符串  *<span style="border:1px solid #999">只读<span>*

按钮UI元素。

默认为 `'button'`
<hr>
**UI_MENUBUTTON** : 字符串  *<span style="border:1px solid #999">只读<span>*

菜单按钮UI元素。

默认为 `'menubutton'`
<hr>
**UI_PANEL** : 字符串  *<span style="border:1px solid #999">只读<span>*

面板UI元素。

默认为 `'panel'`
<hr>
**UI_PANELBUTTON** : String *<span style="border:1px solid #999">只读<span>*

面板按钮UI元素。

默认为 `'panelbutton'`
<hr>
**UI_RICHCOMBO** : String *<span style="border:1px solid #999">只读<span>*

组合 UI 元素。

默认为 `'richcombo'`
<hr>
**UI_SEPARATOR** : String *<span style="border:1px solid #999">只读<span>*

分隔符UI元素。

默认为 `'separator'`
<hr>
**VERBOSITY_ERROR** : Number *<span style="border:1px solid #999">只读<span>*

报告详细级别错误。当[verbosity](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR.html#property-verbosity)设置为该值时，只有[错误](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR.html#method-error) 消息将输出到控制台。它是一个二进制标志，因此它可能与[VERBOSITY_WARN](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR.html#property-VERBOSITY_WARN)标志组合在一起。

默认为 `2`
<hr>
**VERBOSITY_WARN** : Number *<span style="border:1px solid #999">只读<span>*

警告报告详细程度级别。当[verbosity](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR.html#property-verbosity)设置为此值时，只有[警告](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR.html#method-warn) 消息将输出到控制台。它是一个二进制标志，因此它可能与[VERBOSITY_ERROR](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR.html#property-VERBOSITY_ERROR)标志组合在一起。

默认为 `1`
<hr>
**basePath** : String

CKEditor安装目录的完整URL。可以通过设置名为`CKEDITOR_BASEPATH`的全局变量来手动提供基本路径。这个全局变量必须在编辑器脚本加载之前设置。
  
      alert( CKEDITOR.basePath ); // e.g. 'http://www.example.com/ckeditor/'
      
<hr>
**currentInstance** : editor(编辑器实例)

当前处于活动状态的编辑器（具有用户焦点）。

      function showCurrentEditorName() {
          if ( CKEDITOR.currentInstance )
              alert( CKEDITOR.currentInstance.name );
          else
              alert( 'Please focus an editor first.' );
      }CKEDITOR#event-currentInstance

<hr>
**document** : document 

存储CKEDITOR对象的窗口的文档。

      alert( CKEDITOR.document.getBody().getName() ); // 'body'
      
<hr>
**instances** : Object

存储对创建的所有编辑器实例的引用。 此对象中的属性名称与实例名称相对应，其值包含表示它们的[CKEDITOR.editor](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_editor.html)对象。

默认为 `{}`

<hr>
**loadFullCoreTimeout** : Number

如果使用“ckeditor_basic”文件，则等待（以秒为单位）在加载页面后加载完整编辑器代码的时间。如果设置为零，只要创建实例，编辑器就会按需加载。

该值必须在页面加载完成之前在页面上设置。

      // Loads the full source after five seconds.
      CKEDITOR.loadFullCoreTimeout = 5;
      
默认为 `0`
<hr>
**revision** : String

包含CKEditor修订版号。每修改一次CKEditor源代码，版本号会自动增加。

      alert( CKEDITOR.revision ); // e.g. '3975'

默认为 `'%REV%'`
<hr>
**rnd** : Number

一个3位随机整数，对CKEDITOR对象的整个生命周期都有效。

      alert( CKEDITOR.rnd ); // e.g. 319

<hr>
**status** : String

指示API加载状态。以下状态可用：

- unloaded：API尚未加载。
- basic_loaded：基本API功能可用。
- basic_ready：基本API已准备好加载完整的核心代码。
- loaded：API可以被完全使用。

例：

      if ( CKEDITOR.status == 'loaded' ) {
          // The API can now be fully used.
          doSomething();
      } else {
          // Wait for the full core to be loaded and fire its loading.
          CKEDITOR.on( 'load', doSomething );
          CKEDITOR.loadFullCore && CKEDITOR.loadFullCore();
      }
默认为 'unloaded'
<hr>
**timestamp** : String

每个版本的CKEditor都有一个唯一的字符串。默认情况下，它的值用于为编辑器代码加载的所有资源构建URL，以确保在升级时清除缓存结果。

注意：有一个已知的问题，其中“icons.png”不包含时间戳并可能被缓存。我们正在努力修复它。

      alert( CKEDITOR.timestamp ); // e.g. '87dm'
      
默认为 ''
<hr>
**verbosity** : Number

错误的详细程度和警告方法。接受二进制标志 VERBOSITY_WARN和VERBOSITY_ERROR。

        CKEDITOR.verbosity = 0; // No console output after CKEDITOR.warn and CKEDITOR.error methods.
        CKEDITOR.verbosity = CKEDITOR.VERBOSITY_WARN; // Console output after CKEDITOR.warn only.
        CKEDITOR.verbosity = CKEDITOR.VERBOSITY_ERROR; // Console output after CKEDITOR.error only.
        CKEDITOR.verbosity = CKEDITOR.VERBOSITY_WARN | CKEDITOR.VERBOSITY_ERROR; // Console output after both methods.

默认值启用[VERBOSITY_WARN](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR.html#property-VERBOSITY_WARN)和[VERBOSITY_ERROR](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR.html#property-VERBOSITY_ERROR)。

<hr>
**version** : String

包含CKEditor版本号。

      alert( CKEDITOR.version ); // e.g. 'CKEditor 3.4.1'
    
默认为 '%VERSION%'