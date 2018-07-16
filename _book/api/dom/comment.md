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
<hr>
### getPreviousSourceNode( startFromSibling, nodeType, guard )
#### 参数
{{book.one}} **startFromSibling** : Object

{{book.one}} **nodeType** : Object

{{book.one}} **guard** : Object
<hr>
### getPrivate() → Object
获取使用getCustomData绑定到本机DOM对象的私有对象 `_`。

      var elementA = new CKEDITOR.dom.element( nativeElement );
      elementA.getPrivate().value = 1;
      ...
      var elementB = new CKEDITOR.dom.element( nativeElement );
      elementB.getPrivate().value; // 1

#### 返回值
{{book.one}} **Object**

  {{book.tow}} 私人对象。
<hr>
### getUniqueId() → Number
获取可用于在运行会话中标识此DOM对象的标识。

注意：此方法在Internet Explorer 9之前的文本节点上不起作用。
#### 返回值
{{book.one}} **Number**

  {{book.tow}} 唯一的ID。
<hr>
### hasAscendant( name, includeSelf )
#### 参数
{{book.one}} **name** : Object

{{book.one}} **includeSelf** : Object
<hr>
### hasListeners( eventName ) → Boolean
检查是否有任何听众注册到给定事件。

      var myListener = function() { ... };
      someObject.on( 'someEvent', myListener );
      alert( someObject.hasListeners( 'someEvent' ) );    // true
      alert( someObject.hasListeners( 'noEvent' ) );      // false

#### 参数
{{book.one}} **eventName** : string

{{book.tow}} 事件名称
#### 返回值
{{book.one}} **Boolean**
<hr>
### hasNext() → Boolean
检查节点之后有没有任何兄弟节点
#### 返回值
{{book.one}} **Boolean**
<hr>
### hasPrevious() → Boolean
检查节点之前有没有任何兄弟节点
#### 返回值
{{book.one}} **Boolean**
<hr>
### insertAfter( node ) → node
在元素之前插入此节点。

        var em = new CKEDITOR.dom.element( 'em' );
        var strong = new CKEDITOR.dom.element( 'strong' );
        strong.insertAfter( em );

        // Result: '<em></em><strong></strong>'

#### 参数
{{book.one}} **node** : [node](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_dom_node.html)

{{book.tow}} 需要插在元素之前的节点
#### 返回值
{{book.one}}**[node](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_dom_node.html)**

{{book.tow}} 插入之后的节点在此之前。
<hr>
### insertBefore( node ) → node
在元素之后插入节点

      var em = new CKEDITOR.dom.element( 'em' );
      var strong = new CKEDITOR.dom.element( 'strong' );
      strong.insertBefore( em );

      // result: '<strong></strong><em></em>'

#### 参数
{{book.one}} **[node](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_dom_node.html)**

{{book.tow}} 要插入元素之后的节点
#### 返回值
{{book.one}}**[node](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_dom_node.html)**

{{book.tow}} 插入的节点
<hr>
### insertBeforeMe( node ) → node
在此节点之前插入一个节点。
#### 参数
{{book.one}}**[node](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_dom_node.html)**

{{book.tow}} 需要插入的节点
#### 返回值
{{book.one}}**[node](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_dom_node.html)**

{{book.tow}} 插入的节点
<hr>
### isReadOnly( [ checkOnlyAttributes ] ) → Boolean
检查节点是否只读（不应该被改变）。

        // For the following HTML:
        // <b>foo</b><div contenteditable="false"><i>bar</i></div>

        elB.isReadOnly(); // -> false
        foo.isReadOnly(); // -> false
        elDiv.isReadOnly(); // -> true
        elI.isReadOnly(); // -> true

此方法在两种模式下工作，具体取决于浏览器对element.isContentEditable属性的支持和checkOnlyAttributes参数的值。该element.isContentEditable检查是快，但已知的是，在发生故障或隐患分离的节点。此外，在处理一些分离的DOM树时，您可能希望模仿这在可编辑容器内发生（就像它会发生在CKEDITOR.editable中）。为此，您可以暂时将此树附加到具有该data-cke-editable属性的元素并使用该 checkOnlyAttributes模式。

#### 参数
{{book.one}} **[ checkOnlyAttributes ]** : Boolean

{{book.tow}} 如果true仅检查属性，则不使用本机方法。此参数需要true检查隐藏或分离的元素。4.5中介绍。

{{book.tow}} 默认为 `false`

#### 返回
{{book.one}} **Boolean**
<hr>
### ltrim() （啥都没写，等我看源码）
<hr>
### move( target, toStart ) （同上）

#### 参数
{{book.one}} **target** : Object

{{book.one}} **toStart** : Object
<hr>
### on( eventName, listenerFunction, [ scopeObj ], [ listenerData ], [ priority ] ) → Object
将侦听器注册到当前对象中的特定事件。

      someObject.on( 'someEvent', function() {
          alert( this == someObject );        // true
      } );

      someObject.on( 'someEvent', function() {
          alert( this == anotherObject );     // true
      }, anotherObject );

      someObject.on( 'someEvent', function( event ) {
          alert( event.listenerData );        // 'Example'
      }, null, 'Example' );

      someObject.on( 'someEvent', function() { ... } );                       // 2nd called
      someObject.on( 'someEvent', function() { ... }, null, null, 100 );      // 3rd called
      someObject.on( 'someEvent', function() { ... }, null, null, 1 );        // 1st called

#### 参数
{{book.one}} **eventName** : String

{{book.tow}} 要监听的事件名称。

{{book.one}} **listenerFunction** : Function

{{book.tow}} 听取事件的功能。实例化的单个[CKEDITOR.eventInfo](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_eventInfo.html)对象将传递给包含所有事件数据的此函数。

{{book.one}} **[ scopeObj ]** : Object

{{book.tow}} 用于调用侦听器调用（this对象）的对象。如果省略，则使用当前对象。

{{book.one}} **[ listenerData ]** : Object

{{book.tow}} 调用侦听器时要作为[CKEDITOR.eventInfo.listenerData](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_eventInfo.html#property-listenerData)发送的数据 。

{{book.one}} **[ priority ]** : Number

{{book.tow}} 听众优先。首先调用较低优先级的侦听器。具有相同优先级值的监听器将按注册顺序调用。

{{book.tow}} 默认为 `10`

#### 返回
{{book.one}} **Object**

{{book.tow}} 包含该removeListener 函数的对象，可用于随时删除侦听器。
<hr>
### once()

Similiar与上，但听者只会在下一事件触发调用一次。

[CKEDITOR.event.on](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_event.html#method-on)
<hr>
### remove( [ preserveChildren ] ) → node
从文档DOM中删除此节点。

      var element = CKEDITOR.document.getById( 'MyElement' );
      element.remove();

#### 参数
{{book.one}} **[ preserveChildren ]** : Boolean

{{book.tow}}指示子元素必须保留在文档中，仅删除外部标记。

{{book.tow}} 默认 `false`

#### 返回值
{{book.one}} [node](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_dom_node.html)

{{book.tow}}  被删除的节点
<hr>
### removeAllListeners()
删除此对象上设置的任何侦听器。

为了避免内存泄漏，我们必须确保在不再需要对象后不再有引用。
覆盖: [CKEDITOR.event.removeAllListeners](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_event.html#method-removeAllListeners)
<hr>
### removeCustomData( key ) → Object
删除给定键内的值

#### 参数
{{book.one}} **key**: String

#### 返回值
{{book.one}} Object

{{book.tow}} 被删除的值，如果未找到则返回`null`。
<hr>
### removeListener( eventName, listenerFunction )
取消注册在指定事件处调用的侦听器函数。 如果先前未注册侦听器，则不会引发任何错误。

      var myListener = function() { ... };
      someObject.on( 'someEvent', myListener );
      someObject.fire( 'someEvent' );                 // myListener called.
      someObject.removeListener( 'someEvent', myListener );
      someObject.fire( 'someEvent' );                 // myListener not called.

#### 参数
{{book.one}} **eventName** : String

{{book.tow}} 需要取消注册的事件名称

{{book.one}} **listenerFunction** : Function

{{book.tow}} 侦听器功能注销
<hr>
### replace( nodeToReplace )
#### 参数
{{book.one}} **nodeToReplace** : Object
<hr>
### rtrim()
<hr>
### setCustomData( key, value ) → domObject
设置此对象的键值。 这些值由指向同一DOM对象的所有实例共享。

**注意**：只保证在这个唯一的DOM节点上可以使用创建的键，因此任何希望从其他元素克隆（由克隆节点或从innerHtml创建）继续访问它的任何愿望都将失败。 对于此类用法，请改用[CKEDITOR.dom.element.setAttribute](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_dom_element.html#method-setAttribute)。

**注意**：此方法不适用于Internet Explorer 9之前的文本节点。
#### 参数
{{book.one}} **key**: String

{{book.tow}} 于标识 key 的密钥。

{{book.one}} **value**: Object

{{book.tow}} 插入 key 的数据
<hr>
### trim()