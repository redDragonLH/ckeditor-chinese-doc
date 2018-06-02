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
