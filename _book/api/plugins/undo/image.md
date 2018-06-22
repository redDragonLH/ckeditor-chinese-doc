#CKEDITOR.plugins.undo.Image

包含编辑器内容和特定时间点的快照。

## 属性
### bookmarks : Object[]  {{book.one}}*<span style="border:1px solid #999">只读<span>*
表示图像中的选择的书签。bookmark2 对象的数组，请参阅[CKEDITOR.dom.range.createBookmark2](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_dom_range.html#method-createBookmark2)以进行定义。

### contents : String   {{book.one}}*<span style="border:1px solid #999">只读<span>*
编辑内容。

## 方法

### constructor( editor, [ contentsOnly ] ) → Image
创建一个Image类实例。

#### 参数
{{book.one}}**editor** :[editor](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_editor.html)

{{book.tow}}在其上创建图像的编辑器实例。

{{book.one}} **[contentsOnly]**：Boolean

{{book.tow}}如果设置为true，图像将只包含没有选择的内容。

#### 返回
{{book.one}}[Image类](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_plugins_undo_Image.html)
### equalsContent( otherImage ) → Boolean

      Image.equalsContent( otherImage )

#### 参数
{{book.one}} **otherImage** : [Image](./image.md)
  
  {{book.tow}} 要比较的 Image
#### 返回
{{book.one}} Boolean
  
  {{book.tow}} 如果`otherImage`中的内容相同，则返回`true`。
### equalsSelection( otherImage ) → Boolean
#### 参数
{{book.one}} **otherImage** : [Image](./image.md)
  
  {{book.tow}} 要比较的 Image
#### 返回
{{book.one}} Boolean
{{book.tow}} 如果`otherImage`中的选择相同，则返回`true`。