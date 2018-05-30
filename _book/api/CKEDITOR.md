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

ALT键（0x4tow000）。

默认为 `0x4tow000`

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

SHIFT键（0x2one000）。

默认为 `0x2one000`
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

## 方法
#### add(editor)
将编辑器实例添加到全局CKEDITOR对象。该功能 **主要供内部使用**。

##### 参数

  **editor** : [editor](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_editor.html)
  
  要添加的编辑器实例
<hr>
#### addCss( css )
添加要附加到编辑器文档的CSS规则。这种方法主要被插件用来将自定义样式添加到编辑器文档中。对于基本内容样式，应该使用contents.css文件。

**注意**：应该在创建编辑器实例之前调用该函数。

      // Add styles for all headings inside editable contents.
      CKEDITOR.addCss( '.cke_editable h1,.cke_editable h2,.cke_editable h3 { border-bottom: 1px dotted red }' );

##### 参数
  **css** : String
  
    要添加的样式规则。 [CKEDITOR.config.contentsCss](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_config.html#cfg-contentsCss)
<hr>
#### addTemplate( name, source ) → [template](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_template.html)
添加一个名为[CKEDITOR.template](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_template.html)的实例，以便在所有编辑器中重用。如果已经定义了具有相同名称的模板，这将返回现有的模板。此外，它会触发“模板”事件以允许模板源自定义。
##### 参数
<em style="margin-left:one;"></em>  **name** : String
  
<em style="margin-left:tow;"></em>  标识UI模板的名称。
  
<em style="margin-left:one;"></em>  **source** : String
  
<em style="margin-left:tow;"></em>  用于构建此模板的源字符串。

##### 返回
{{book.one}}[template](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_template.html)

  {{book.tow}}创建的模板实例。

<hr>
#### appendTo( element, [ config ], [ data ] ) → [editor](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_editor.html)
在特定DOM元素的末尾创建一个新的编辑器实例

      <!DOCTYPE html>
        <html>
            <head>
                <meta charset="utf-8">
                <title>CKEditor</title>
                <!-- Make sure the path to CKEditor is correct. -->
            <script src="/ckeditor/ckeditor.js"></script>
        </head>
        <body>
            <div id="editorSpace"></div>
            <script>
                CKEDITOR.appendTo( 'editorSpace' );
            </script>
        </body>
      </html>

##### 参数

{{ book.one }}element : Object | String  

  {{ book.tow }} DOM元素，其ID或名称。
  
{{ book.one }} [ config ] : Object

  {{ book.tow }} 要应用于此编辑器实例的特定配置。此处设置的配置将覆盖全局CKEditor设置（请参阅[CKEDITOR.config](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_config.html)）。
  
{{ book.one }} [ data ] : String

  {{ book.tow }} 自3.3起。该实例的初始值。
  
##### 返回
{{ book.one }}[editor](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_editor.html)

  {{ book.tow }}编辑器实例已创建。
<hr>
####  domReady()
指定一个函数在DOM完全加载时执行。

如果在DOM初始化后调用，则传入的函数将立即执行。
<hr>
#### editorConfig( config )
函数调用加载可以修改编辑器实例配置（[CKEDITOR.editor.config](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_editor.html#property-config)）的自定义配置文件。它通常在可以包含开发人员定义的设置的自定义配置文件中定义。

      // This is supposed to be placed in the config.js file.
      CKEDITOR.editorConfig = function( config ) {
          // Define changes to default configuration here. For example:
          config.language = 'fr';
          config.uiColor = '#AADC6E';
      };

#####参数
{{ book.one }} config : [config](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_config.html)

  {{ book.tow }}包含为[CKEDITOR.editor](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_editor.html)实例定义的设置的配置对象，直至此函数调用。请注意，并非所有设置可能仍然可用。 详细信息请参阅 [配置载入顺序](https://docs.ckeditor.com/ckeditor4/latest/https://docs.ckeditor.com/ckeditor4/docs/guide/dev_configuration.html)。
<hr>
#### error( errorCode, [ additionalData ] )

错误报告功能。 如果[错误程度](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR.html#property-verbosity)设置了[VERBOSITY_ERROR](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR.html#property-VERBOSITY_ERROR)标志，则会将类型设置为错误的[日志](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR.html#event-log)事件触发。 触发的事件也包含提供的 `errorCode`和`additionalData`。

##### 参数
{{ book.one }}errorCode : String

  {{ book.tow }}描述报告问题的错误代码。

{{ book.one }} [ additionalData ] : Object

  {{ book.tow }}与报告的问题相关的其他数据。
<hr>
#### getCss() → String
  返回一个字符串，其中包含传递给[addCss](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR.html#method-addCss)方法的所有CSS规则。
  
##### 返回
{{ book.one }}字符串

  {{ book.tow }}包含CSS规则的字符串。
<hr>
#### getTemplate( name )
检索使用addTemplate创建的已定义模板。
##### 参数
{{ book.one }}name : String

  {{ book.tow }}模板名称。
<hr>
#### getUrl( resource ) → String
获取CKEditor资源的完整URL。默认情况下，该函数返回的URL包含设置为时间戳值的查询字符串参数（“t”）。

可以通过设置一个名为的全局变量来提供该函数的自定义实现CKEDITOR_GETURL。这个全局变量必须在编辑器脚本加载之前设置。如果自定义实现返回nothing（==null），则使用默认实现。

      // e.g. 'http://www.example.com/ckeditor/skins/default/editor.css?t=87dm'
      alert( CKEDITOR.getUrl( 'skins/default/editor.css' ) );

      // e.g. 'http://www.example.com/skins/default/editor.css?t=87dm'
      alert( CKEDITOR.getUrl( '/skins/default/editor.css' ) );

      // e.g. 'http://www.somesite.com/skins/default/editor.css?t=87dm'
      alert( CKEDITOR.getUrl( 'http://www.somesite.com/skins/default/editor.css' ) );

#####参数
{{ book.one }} resource : String
  
  {{ book.tow }} 我们想要获取完整网址的资源。它可能是完整的，绝对的或相对的URL。
#####返回
{{ book.one }} **String**

  {{ book.tow }}完整的网址。
<hr>
#### inline( element, [ instanceConfig ] ) → editor
将contenteditable设置为属性的DOM元素true转换为CKEditor实例。检查[CKEDITOR.dtd.$editable ](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_dtd.html#property-S-editable)的允许元素名称列表。

注意：如果启用了内联编辑的DOM元素没有contenteditable设置为的属性true，编辑器将以只读模式启动。

    <div contenteditable="true" id="content">...</div>
    ...
    CKEDITOR.inline( 'content' );
    
也可以从`<textarea>`元素创建一个内联编辑器。 如果这样做，将在`<textarea>`元素之后直接创建具有可编辑内容的额外`<div>`元素，并且`<textarea>`元素将被隐藏。    
##### 参数
{{ book.one }} **element** : Object | String

  {{ book.tow }} DOM元素或其ID。

{{ book.one }} **[ instanceConfig ]** : Object

  {{ book.tow }}要应用于此编辑器实例的特定配置。请参阅[CKEDITOR.config](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_config.html)。
<hr>
#### inlineAll()
  调用contenteditable属性设置为true的所有页面元素。
<hr>
#### loadFullCore()
如果只加载了基本代码（ckeditor_basic.js），则强制执行完整的CKEditor核心代码。这种方法在第一次调用时自毁（设置为 `undefined`）

      // Check if the full core code has been loaded and load it.
      if ( CKEDITOR.loadFullCore )
          CKEDITOR.loadFullCore();
    
<hr>
#### replace( element, [ config ] ) → editor
用CKEditor实例替换`<textarea>`或DOM元素（`<div>`）。 对于textareas，编辑器中的初始值将是textarea值。 对于DOM元素，将使用它们的`innerHTML`。 建议仅使用`<textarea>`和`<div>`元素。

      <textarea id="myfield" name="myfield"></textarea>
      ...
      CKEDITOR.replace( 'myfield' );

      var textarea = document.body.appendChild( document.createElement( 'textarea' ) );
      CKEDITOR.replace( textarea );
      
##### 参数
{{book.one}} **element** : Object | String

  {{book.tow}}DOM元素（textarea），其ID或名称。
      
{{book.one}} **[ config ]** : Object

  {{book.tow}}要应用于此编辑器实例的特定配置。此处设置的配置将覆盖全局CKEditor设置（请参阅[CKEDITOR.config](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_config.html)）。
#####返回
{{book.one}}**[editor](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_editor.html)**

  {{book.tow}}编辑器实例已创建。
<hr>
#### replaceAll( [ className ], [ evaluator ] )
`<textarea>`用编辑器实例替换文档中所有可用的元素。

      // Replace all <textarea> elements in the page.
      CKEDITOR.replaceAll();

      // Replace all <textarea class="myClassName"> elements in the page.
      CKEDITOR.replaceAll( 'myClassName' );

      // Selectively replace <textarea> elements, based on a custom evaluation function.
      CKEDITOR.replaceAll( function( textarea, config ) {
          // A function that needs to be evaluated for the <textarea>
          // to be replaced. It must explicitly return "false" to ignore a
          // specific <textarea>.
          // You can also customize the editor instance by having the function
          // modify the "config" parameter.
      } );

      // Full page example where three <textarea> elements are replaced.
      <!DOCTYPE html>
      <html>
          <head>
              <meta charset="utf-8">
              <title>CKEditor</title>
              <!-- Make sure the path to CKEditor is correct. -->
              <script src="/ckeditor/ckeditor.js"></script>
          </head>
          <body>
              <textarea name="editor1"></textarea>
              <textarea name="editor2"></textarea>
              <textarea name="editor3"></textarea>
              <script>
                  // Replace all three <textarea> elements above with CKEditor instances.
                  CKEDITOR.replaceAll();
              </script>
          </body>
      </html>

##### 参数
{{book.one}}**[ className ]** : String

  {{book.tow}}在`<textarea>`类名。

{{book.one}} **[ evaluator ]** : Function
  {{book.tow}}函数必须返回`true`才能用编辑器替换`<textarea>`。 如果函数返回`false`，则`<textarea>`元素将不会被替换。
<hr>
#### warn( errorCode, [ additionalData ] )
警告报告功能。 当设置了[VERBOSITY_WARN](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR.html#property-VERBOSITY_WARN)标志时，它会触发类型设置为警告的[日志](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR.html#event-log)事件。 Fired事件包含了也提供了errorCode和additionalData。
##### 参数
{{book.one}} **errorCode** : String

  {{book.tow}}描述报告问题的错误代码。

{{book.one}} **[ additionalData ]** : Object

  {{book.tow}}与报告的问题相关的其他数据。
## 事件
### ariaWidget( evt )
 panel 添加到文档时触发。

#### 参数
{{book.one}}**evt** : [eventInfo](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_eventInfo.html)
#### 属性

{{book.one}}**data** : Object

  {{book.tow}}包裹面板的元素。

<hr>
### contentPreview( evt )
执行preview命令时会触发事件，从而允许额外的数据操作。通过此事件，可以更改或修改要显示的预览窗口的原始HTML内容。

#### 参数
{{book.one}}**evt** : [eventInfo](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_eventInfo.html)
#### 属性
{{book.one}}**editor** : [editor](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_editor.html)

{{book.tow}}这个编辑器实例。

{{book.one}}**data** : Object

{{book.tow}}属性

{{book.tow}}**dataValue** : String

{{book.tow}}{{book.one}}将进入预览的数据。
<hr>
### currentInstance( evt )
[CKEDITOR.currentInstance](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR.html#property-currentInstance)对象引用更改时触发。将焦点设置在页面中的不同编辑器实例时可能会发生这种情况。

      var editor; // A variable to store a reference to the current editor.
      CKEDITOR.on( 'currentInstance', function() {
          editor = CKEDITOR.currentInstance;
      } );
      
#### 参数
{{book.one}}**evt** : [eventInfo](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_eventInfo.html)
<hr>
### dialogDefinition( evt )

当对话框定义即将用于创建对话框到编辑器实例中时触发事件。 此事件可以在创建定义之前自定义定义。

请注意，仅在第一次打开特定对话框时调用此事件。 连续的调用将使用缓存的对话框，并且该事件不会被触发。

#### 参数
{{book.one}}**evt** : [eventInfo](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_eventInfo.html)
{{book.tow}}##### 属性
{{book.tow}}**data** : [definition](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_dialog_definition.html)

{{book.one}}{{book.tow}}正在加载的对话框定义。

{{book.tow}}**editor** : [editor](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_editor.html)

{{book.one}}{{book.tow}}将使用该对话框的编辑器实例。

<hr>
### instanceCreated( evt )
事件在创建CKEDITOR实例时触发，但仍在初始化之前。要与完全初始化的实例进行交互，请改用 [instanceReady](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR.html#event-instanceReady)事件。

#### 参数
{{book.one}}**evt** : eventInfo
##### {{book.tow}}属性

{{book.tow}}**editor** : [editor](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_editor.html)

{{book.thre}}已创建的编辑器实例。
<hr>
### instanceDestroyed( evt )
当CKEDITOR实例被销毁时触发事件。

#### 参数
{{book.one}}**evt** : [eventInfo](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_eventInfo.html)
##### {{book.tow}}属性
{{book.tow}}**editor** : [editor](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_editor.html)

{{book.thre}}编辑器实例已被销毁。
<hr>
### instanceLoaded( evt )
当CKEDITOR实例的组件（配置，语言和插件）完全加载并初始化时触发事件。但是，编辑器将完全准备好在[instanceReady](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR.html#event-instanceReady)上进行交互。

#### 参数
{{book.one}}**evt** : eventInfo
##### {{book.tow}}属性

{{book.tow}}**editor** : [editor](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_editor.html)

{{book.thre}}此编辑器实例已被加载。
<hr>
### instanceReady( evt )
事件在创建CKEDITOR实例时触发，完全初始化并准备好进行交互。

#### 参数
{book.one}}**evt** : [eventInfo](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_eventInfo.html)
##### {{book.tow}} 属性
{{book.tow}}**editor** : [editor](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_editor.html)

{{book.thre}}已创建的编辑器实例。
<hr>
### loaded( evt )
CKEDITOR核心对象完全加载并准备好进行交互时触发。

#### {{book.one}} 参数
{{book.one}} **evt** : [eventInfo](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_eventInfo.html)
<hr>
### log( evt )

由[警告](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR.html#method-warn)和[错误](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR.html#method-error)方法引发。默认监听器日志向控制台提供信息。

此事件可用于提供自定义错误/警告处理程序：

        CKEDTIOR.on( 'log', function( evt ) {
            // Cancel default listener.
            evt.cancel();
            // Log event data.
            console.log( evt.data.type, evt.data.errorCode, evt.data.additionalData );
        } );
        
#### {{book.one}} 参数
{{book.tow}} **evt** : [eventInfo](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_eventInfo.html)
##### {{book.thre}} 属性
{{book.thre}} **data** : Object
###### {{book.thre}}{{book.one}}属性
{{book.thre}}{{book.one}} **type** : String

{{book.thre}}{{book.tow}}日志类型。可以是`error`或`warn`。

{{book.thre}}{{book.one}} **errorCode** : String

{{book.thre}}{{book.tow}} 描述报告问题的错误代码。

{{book.thre}}{{book.one}} **[ additionalData ]** : Object

{{book.thre}}{{book.tow}}与此日志事件关联的其他数据。
<hr>
### reset( evt )
最后一个实例被销毁时触发。此事件用于执行全局内存清理。

#### {{book.one}} 参数
{{book.tow}} **evt** :  [eventInfo](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_eventInfo.html)