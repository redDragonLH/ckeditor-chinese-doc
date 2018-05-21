# CKEDITOR
这是API入口点。整个CKEditor代码运行在这个对象下

## 配置选项

** disableAutoInline ** : 布尔

对于 `contenteditable`属性设置为`true`的元素，禁止自动创建内联编辑器。

      CKEDITOR.disableAutoInline = true;

默认为`false`

** replaceClass ** : 字符串

用于识别CKEditor实例替换的 `<textarea>` 元素的类名称。 将其设置为 empty/`null`以禁用此功能。

      CKEDITOR.replaceClass = 'rich_editor';
      
默认为 `ckeditor`

** skinName ** : 字符串

要为所有创建的实例加载的外观，它可能是编辑器安装路径内的外观文件夹的名称，或者用逗号分隔的名称和路径。

**注意**： 这是适用于所有实例的全局配置。

      CKEDITOR.skinName = 'moono';

      CKEDITOR.skinName = 'myskin,/customstuff/myskin/';
      
默认为  `moono-lisa`