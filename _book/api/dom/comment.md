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

** 参数 **

comment：对象| 字符串

[ownerDocument]文档
在创建新节点的情况下将包含节点的文档。 默认为当前文档。

** 返回 **

comment

**覆盖**：CKEDITOR.dom.node.constructor
