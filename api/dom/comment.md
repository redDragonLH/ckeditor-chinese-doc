# CKEDITOR.dom.comment

代表一个DOM注释节点。

    var nativeNode = document.createComment( 'Example' );
    var comment = new CKEDITOR.dom.comment( nativeNode );

    var comment = new CKEDITOR.dom.comment( 'Example' );
    

## 属性

** $ **

类型：对象

保存的是原生dom对象

    var element = new CKEDITOR.dom.element( 'span' );
    alert( element.$.nodeType ); // '1'

** type **

类型：数字

节点类型。 这是一个设置为 CKEDITOR.NODE_COMMENT 的常量值。

默认为CKEDITOR.NODE_COMMENT

CKEDITOR.NODE_COMMENT 常量默认为 8
## 静态属性

useCapture : Boolean

## 方法

### constructor 

constructor( comment, [ ownerDocument ] ) → comment

创建一个评论类实例。

#### {{book.one}}参数

{{book.tow}} **comment** ：对象| 字符串

{{book.tow}}[ownerDocument] : [文档](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_dom_document.html)

在创建新节点的情况下将包含节点的文档。 默认为当前文档。

** 返回 **

comment

覆盖：[CKEDITOR.dom.node.constructor](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_dom_node.html#method-constructor)
<hr>
### appendTo( element ) → [element](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_dom_element.html)
使此节点成为另一个元素的子节点。

    var p = new CKEDITOR.dom.element( 'p' );
    var strong = new CKEDITOR.dom.element( 'strong' );
    strong.appendTo( p );
    
#### 参数

{{book.one}}**element** : [element](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_dom_element.html)

{{book.tow}} 此节点将被追加到的目标元素。

#### Returns
{{book.one}} [element](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_dom_element.html)

{{book.tow}} 目标元素。
<hr>
### capture()
在支持目标上的捕获阶段下注册事件处理程序。
<hr>
### clearCustomData()
删除存储在此对象中的任何数据。 为了避免内存泄漏，我们必须确保在不再需要对象之后没有剩余的引用。
<hr>
### clone( [ includeChildren ], [ cloneId ] ) → node
克隆这个节点

**注意**：由{[setCustomData](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_dom_node.html#method-setCustomData)}设置的值在克隆中不可用。

#### 参数
{{book.one}} **[ includeChildren ]** : Boolean

  {{book.tow}}如果为 `true`，则所有节点的子节点将被递归克隆。
  
  {{book.tow}}默认为 `false`
  
{{book.one}} [ cloneId ] : Boolean

  {{book.tow}} ID属性是否应该被克隆。
  
  {{book.tow}}默认为 `false`。
#### 返回
  {{book.one}} [node](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_dom_node.html)
  
  {{book.tow}} 克隆的节点
<hr>
### define( name, meta )
预定义特定事件名称的一些内部属性。
#### 参数
{{book.one}} **name** :string

  {{book.tow}} 事件名称

{{book.one}} **meta** : Object

  {{book.tow}} 属性
  
  {{book.tow}} **[ errorProof ]**
  
  {{book.thre}}  事件触发是否应该捕获每个侦听器调用引发的错误。
  
  {{book.thre}} 默认为 `false`
<hr>
### equals( object ) → Boolean
确定指定的对象是否等于当前对象。

        var doc = new CKEDITOR.dom.document( document );
        alert( doc.equals( CKEDITOR.document ) );   // true
        alert( doc == CKEDITOR.document );          // false
      
#### 参数
{{book.one}} **object** : Object

{{book.tow}} 要与当前对象进行比较的对象。
#### 返回
{{book.one}} **Boolean** 

{{book.tow}}  如果对象相等返回 `true`。
<hr>
### fire( eventName, [ data ], [ editor ] ) → Boolean | Object
触发对象中的特定事件。此时调用所有已注册的侦听器。

      someObject.on( 'someEvent', function() { ... } );
      someObject.on( 'someEvent', function() { ... } );
      someObject.fire( 'someEvent' );             // Both listeners are called.

      someObject.on( 'someEvent', function( event ) {
          alert( event.data );                    // 'Example'
      } );
      someObject.fire( 'someEvent', 'Example' );

#### 参数
{{book.one}} **eventName** : String

{{book.tow}} 要触发的事件名称。

{{book.one}} **[ data ]** : Object

{{book.tow}}数据在调用侦听器时作为[CKEDITOR.eventInfo.data](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_eventInfo.html#property-data)发送 。

{{book.one}} **[ editor ]** : editor

{{book.tow}} 调用侦听器时作为[CKEDITOR.eventInfo.editor](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_eventInfo.html#property-editor)发送的编辑器实例 。

#### 返回 
{{book.one}} **Boolean | Object**

{{book.tow}}指示事件将被取消的布尔值，或由其中一个侦听器返回的数据。

<hr>
### fireOnce( eventName, [ data ], [ editor ] ) → Boolean | Object

触发对象中的特定事件，释放信号到该事件的所有侦听器。不能再次调用次特定事件

      someObject.on( 'someEvent', function() { ... } );
      someObject.fire( 'someEvent' );         // Above listener called.
      someObject.fireOnce( 'someEvent' );     // Above listener called.
      someObject.fire( 'someEvent' );         // No listeners called.

#### 参数
{{book.one}} **eventName** : String

{{book.tow}} 要触发的事件名称。

{{book.one}} **[ data ]** : Object

{{book.tow}}数据在调用侦听器时作为[CKEDITOR.eventInfo.data](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_eventInfo.html#property-data)发送 。

{{book.one}} **[ editor ]** : editor

{{book.tow}} 调用侦听器时作为[CKEDITOR.eventInfo.editor](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_eventInfo.html#property-editor)发送的编辑器实例 。

#### 返回 
{{book.one}} **Boolean | Object**

{{book.tow}}指示事件将被取消的布尔值，或由其中一个侦听器返回的数据。
<hr>
### getAddress( [ normalized ] ) → Array
为此节点检索唯一可识别的树地址。 返回的树地址是一个整数数组，每个整数指示一个DOM节点的子索引，从document.documentElement开始。

例如，假设<body>是<html>（<head>是第一个）的第二个孩子，并且我们想要解释第三个孩子在<body>的第四个孩子下，返回的树地址是：[ 1,3,2]。

一旦DOM树结构被修改，树地址就不能用于找回DOM树节点。
#### 参数
{{book.one}} **[ normalized ]** : Boolean

  {{book.tow}} 请参阅 [getIndex](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_dom_node.html#method-getIndex)。
  
  {{book.tow}} 默认为 `false`
#### 返回
{{book.one}} **数组**

{{book.tow}} 地址
<hr>
### getAscendant( query, [ includeSelf ] ) → node
获取此节点的最近的祖先节点，由其名称或使用评估函数指定。

      // Suppose we have the following HTML structure:
      // <div id="outer"><div id="inner"><p><b>Some text</b></p></div></div>
      // If node == <b>
      ascendant = node.getAscendant( 'div' );             // ascendant == <div id="inner">
      ascendant = node.getAscendant( 'b' );               // ascendant == null
      ascendant = node.getAscendant( 'b', true );         // ascendant == <b>
      ascendant = node.getAscendant( { div:1, p:1 } );    // Searches for the first 'div' or 'p': ascendant == <div id="inner">

      // Using custom evaluator:
      ascendant = node.getAscendant( function( el ) {
          return el.getId() == 'inner';
      } );
      // ascendant == <div id="inner">

#### 参数
{{book.one}} **query**: String | Function | Object

  {{book.tow}} 要搜索的祖先节点的名称或具有要搜索的节点名称的对象或评估程序函数。

{{book.one}} **[ includeSelf ]** : Boolean

  {{book.tow}} 是否在搜索中包含当前节点。

#### 返回值
{{book.one}} [node](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_dom_node.html)

  {{book.tow}} 找到的祖先节点，如果未找到，则返回null。
<hr>
### getCommonAncestor( node )
得到共同的祖先
#### 参数
{{book.one}} **node** : Object
<hr>
### getCustomData( key ) → Object
获取设置到此对象中的数据插槽的值。

      var element = new CKEDITOR.dom.element( 'span' );
      alert( element.getCustomData( 'hasCustomData' ) );      // e.g. 'true'
      alert( element.getCustomData( 'nonExistingKey' ) );     // null

#### 参数
{{book.one}} **key** : String

{{book.tow}} 用于识别数据插槽的密钥。
#### 返回值
{{book.one}} **Object**

{{book.tow}} 该值设置为数据插槽。
<hr>
### getDocument() → document
获取包含此元素的document。

      var element = CKEDITOR.document.getById( 'example' );
      alert( element.getDocument().equals( CKEDITOR.document ) ); // true

#### 返回值
{{book.one}} **[document](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_dom_document.html)**

{{book.tow}} document元素
<hr>
### getIndex( normalized ) → Number
获取parent.childNodes数组中某个节点的索引。 如果节点没有父节点，或者当规范化参数设置为true并且文本节点为空并且在规范化过程中将被删除，则返回-1。

让我们假设有以下childNodes数组：

      [ emptyText, element1, text, text, element2, emptyText2 ]

      emptyText.getIndex()            // 0
      emptyText.getIndex( true )      // -1
      element1.getIndex();            // 1
      element1.getIndex( true );      // 0
      element2.getIndex();            // 4
      element2.getIndex( true );      // 2
      emptyText2.getIndex();          // 5
      emptyText2.getIndex( true );    // -1

#### 参数
{{book.one}} **normalized** : Boolean

{{book.tow}} 如果为`true`，则会合并相邻的文本节点，并删除空的文本节点。
#### 返回值
{{book.one}} **Number**

{{book.tow}} 索引节点或-1，如果一个节点没有父节点或在规范化过程中被删除。
<hr>
### getNext( [ evaluator ] ) → node
获取其父级子级列表中此元素后面的节点。

      var element = CKEDITOR.dom.element.createFromHtml( '<div><b>Example</b><i>next</i></div>' );
      var last = element.getFirst().getNext();
      alert( last.getName() ); // 'i'

#### 参数
{{book.one}} **[ evaluator ]** : Function

{{book.tow}} Filtering the result node.
#### 返回值
{{book.one}} [node](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_dom_node.html)

{{book.tow}} 下一个节点，如果不可用，则返回null。
<hr>
### getNextSourceNode( startFromSibling, nodeType, guard )
#### 参数
{{book.one}} **startFromSibling** : Object

{{book.one}} **nodeType** : Object

{{book.one}} **guard** : Object
<hr>
### getOuterHtml() → String
获取此评论的外部HTML。
#### 返回值
{{book.one}} **String**

{{book.tow}} HTML <!-- comment value -->.
<hr>
### getParent( [ allowFragmentParent ] ) → element
获取此节点的父元素。

      var node = editor.document.getBody().getFirst();
      var parent = node.getParent();
      alert( parent.getName() ); // 'body'
      
#### 参数
{{book.one}} **[ allowFragmentParent ]** : Boolean

{{book.tow}} 参考 [CKEDITOR.NODE_DOCUMENT_FRAGMENT](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR.html#property-NODE_DOCUMENT_FRAGMENT)片段类型的父节点。

{{book.tow}} 默认为 `false`
#### 返回值
{{book.one}} **[element](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_dom_element.html)**

{{book.tow}} 父节点
<hr>
### getParents( [ closerFirst ] ) → Array
返回包含节点父节点和节点本身的数组。 默认情况下，节点按降序排列。
#### 参数
{{book.one}} **[ closerFirst ]** : Boolean

  {{book.tow}} 确定返回的节点的顺序。
  
  {{book.tow}} 默认为`false`
#### 返回值
{{book.one}} **Array**

  {{book.tow}} 返回包含[CKEDITOR.dom.node](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_dom_node.html)的数组
<hr>
### getPosition( otherNode ) → Number
确定此节点与文档中给定的[CKEDITOR.dom.node](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_dom_node.html)之间的位置关系。 该节点可以在给定节点之前（[CKEDITOR.POSITION_PRECEDING](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR.html#property-POSITION_PRECEDING)）或跟随（[CKEDITOR.POSITION_FOLLOWING](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR.html#property-POSITION_FOLLOWING)）。 该节点还可以包含（[CKEDITOR.POSITION_CONTAINS](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR.html#property-POSITION_CONTAINS)）或由（[CKEDITOR.POSITION_IS_CONTAINED](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR.html#property-POSITION_IS_CONTAINED)）包含给定节点。 如果给定节点与此节点相同，该函数将返回上面列出的常量或[CKEDITOR.POSITION_IDENTICAL](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR.html#property-POSITION_IDENTICAL)的位掩码。
#### 参数
{{book.one}} **otherNode** : [node](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_dom_node.html)

{{book.tow}} 用来检查关系的节点。
#### 返回值
{{book.one}} **Number**

{{book.tow}} 该节点和给定节点之间的位置关系。
<hr>
### getPrevious( [ evaluator ] ) → node
获取其父级子列表中此元素之前的节点。

      var element = CKEDITOR.dom.element.createFromHtml( '<div><i>prev</i><b>Example</b></div>' );
      var first = element.getLast().getPrev();
      alert( first.getName() ); // 'i'
      
#### 参数
{{book.one}} **[ evaluator ]** : Function

  {{book.tow}}过滤结果节点。
#### 返回值
{{book.one}} [node](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_dom_node.html)

  {{book.tow}} 前一个节点，如果不可用，则返回null。