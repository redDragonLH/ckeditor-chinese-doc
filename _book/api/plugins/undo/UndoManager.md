# CKEDITOR.plugins.undo.UndoManager
重做/撤消功能的主要逻辑。
## 属性
### limit : Number {{book.one}}*<span style="font-size:12px;font-width:100; border:1px solid #999">只读<span>*
堆栈中的最大快照数量。 通过[CKEDITOR.config.undoStackSize](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_config.html#cfg-undoStackSize)进行配置。
<hr>
### locked : Object  {{book.one}}*<span style="font-size:12px;font-width:100; border:1px solid #999">只读<span>*
当锁定属性不为空时，撤销管理器被锁定，因此禁止保存或更新等操作。

管理员可以分别通过[锁定](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_plugins_undo_UndoManager.html#method-lock)和[解锁](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_plugins_undo_UndoManager.html#method-unlock)方法锁定和解锁。

默认为`null`
<hr>
### previousKeyGroup : Number  {{book.one}}*<span style="font-size:12px;font-width:100; border:1px solid #999">只读<span>*
包含基于keyGroups的先前处理的[密钥组](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_plugins_undo_UndoManager.html#static-property-keyGroups)。 `-1` 表示一个未知组。

默认为 `-1`

### strokesLimit : Number  {{book.one}}*<span style="font-size:12px;font-width:100; border:1px solid #999">只读<span>*
在一个撤消步骤中键入/删除的最大字符数。

默认为 `25`

<hr>
### strokesRecorded : Array {{book.one}}*<span style="font-size:12px;font-width:100; border:1px solid #999">只读<span>*

存储按键次数的数组，连续计数。 使用[keyGroups](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_plugins_undo_UndoManager.html#static-property-keyGroups)成员作为索引。

**注意**：按键计数将在达到每个快照的字符数限制后重置。

默认为 `[0，0]`

## 静态属性
### keyGroups : Object {{book.one}}*<span style="font-size:12px;font-width:100; border:1px solid #999">只读<span>*
密钥组标识符映射。 用于访问[strokesRecorded](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_plugins_undo_UndoManager.html#property-strokesRecorded)中的成员。

FUNCTIONAL  - 退格键/删除键的标识符。

PRINTABLE  - 打印键的标识符。

**用法示例：**

      undoManager.strokesRecorded[ undoManager.keyGroups.FUNCTIONAL ];

默认为 ` {PRINTABLE: 0, FUNCTIONAL: 1}`
<hr>
### navigationKeyCodes : Object  {{book.one}}*<span style="font-size:12px;font-width:100; border:1px solid #999">只读<span>*

导航键的代码，如箭头，Page Up / Down等。由[isNavigationKey](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_plugins_undo_UndoManager.html#static-method-isNavigationKey)方法使用。

默认为 `{37: 1, 38: 1, 39: 1, 40: 1, 36: 1, 35: 1, 33: 1, 34: 1}`

## 方法
### constructor( editor ) → [UndoManager](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_plugins_undo_UndoManager.html)
创建一个 UndoManager 类实例。
#### 参数
{{book.one}} **editor** : [editor](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_editor.html)
#### 返回值
{{book.one}} [UndoManager](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_plugins_undo_UndoManager.html)
<hr>
### getNextImage( isUndo ) → Image
获取最接近的可用快照。
#### 参数
{{book.one }} **isUndo**: Boolean

  {{book.tow}} 如果为 `true`，它会返回以前的快照。
#### 返回值
{{book.one}} [Image](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_plugins_undo_Image.html)

{{book.tow}} 下一个快照或是`null`
<hr>
### keyGroupChanged( keyCode ) → Boolean
新的`keyCode`是否属于与前一个不同的组([previousKeyGroup](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_plugins_undo_UndoManager.html#property-previousKeyGroup))

#### 参数
{{book.one}} **keyCode**: Number
#### 返回值
{{book.one}} **Boolean**
<hr>
### lock( [ dontUpdate ], [ forceUpdate ] )
锁定快照堆栈以防止任何保存/更新操作，并且在需要时，在锁定期间内调用[unlock](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_plugins_undo_UndoManager.html#method-unlock)方法后，使用DOM更改更新快照堆栈的提示。

它主要用于确保不应将任何不应记录的DOM操作（例如，自动分段）添加到堆栈中。

注意：对于每个`lock`，您必须调用[nulock](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_plugins_undo_UndoManager.html#method-unlock)一次才能解锁撤消管理器。
#### 参数
{{book.one}} **[ dontUpdate ]** : Boolean

{{book.tow}} 设置为 `true`时，最后一个快照将不会使用当前内容和选择进行更新。 默认情况下，如果撤消管理器在锁定开始时处于最新状态，则在解锁时最后一个快照将更新为当前状态。 这意味着在锁定期间完成的所有更改将合并到上一个快照或下一个快照中。 使用此选项可以更好地控制此行为。 例如，可以将在锁定期间完成的更改分组到单独的快照中。

{{book.one}} **[ forceUpdate ]** : Boolean

{{book.tow}} 如果设置为`true`，则无论当前的撤消管理器状态如何，最后的快照都将随当前的内容和选择一起更新。 如果未设置，则只有在撤消管理器在锁定时处于最新状态时，才会更新最后一个快照。 此外，该选项可以在编辑器不处于`wysiwyg`模式时锁定快照，因为当它通过时，快照将不需要进行比较。

<hr>
### redo()
对当前索引执行重做操作。
<hr>
### redoable() → Boolean
检查当前的重做状态。
#### 返回值
{{book.one}} **Boolean**

{{book.tow}} 文档状态
<hr>
### refreshState()
刷新[撤销管理器](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_plugins_undo_UndoManager.html)的状态以及`undo`和`redo `命令的状态。
<hr>
### reset()
重置 undo 状态
<hr>
### resetType()
重置所有输入变量
<hr>
### restoreImage( image )
将编辑器内容/选择设置储存为快照
#### 参数
{{book.one}} **image** : [Image](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_plugins_undo_Image.html)
<hr>
### save( onContentOnly, image, [ autoFireChange ] )
保存文档的快照供以后检索。
#### 参数
{{book.one}} **onContentOnly** : Boolean

{{book.tow}}如果设置为true，则仅当内容已更改时才会保存快照。

{{book.one}} **image** : [Image](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_plugins_undo_Image.html)

{{book.tow}}一个可选的快照。 如果跳过，将使用当前编辑器。

{{book.one}} **[ autoFireChange ]** : Boolean

{{book.tow}} 如果设置为 `false`，不会触发[CKEDITOR.editor.change](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_editor.html#event-change)事件给编辑器。

{{book.tow}}  默认为 `true`
<hr>
### type( keyCode, [ strokesPerSnapshotExceeded ] )
处理撤销管理器的按键支持。 它可以调用可以改变编辑器内容的`包含基于keyGroups的先前处理的`事件。
#### 参数
{{book.one}} **keyCode**:Number

  {{book.tow}} 按键代码

{{book.one}} **[ strokesPerSnapshotExceeded ]** : Boolean

  {{book.tow}}当设置为true时，该方法的行为就好像笔画限制被超过，而不管笔划记录的值如何。
<hr>  
### undo()
对当前索引执行撤消操作。
<hr>
### undoable() → Boolean
查看当前撤销操作状态
#### 返回
{{book.one}} **Boolean**
  
  {{book.tow}} 文档是否有未来的状态来恢复
<hr>
### unlock()
Unlocks the snapshot stack and checks to amend the last snapshot.

请参[lock](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_plugins_undo_UndoManager.html#method-lock)定了解更多详情。
<hr>
### update( [ newImage ] )

用当前编辑器内容更新撤销堆栈的最后一个快照。
#### 参数
{{book.one}} **[ newImage ]** : [Image](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_plugins_undo_Image.html)

将取代当前的快照。 如果未设置，则默认为从编辑器获取的快照。
<hr>
### updateSelection( newSnapshot ) → Boolean
修改上一个快照并更改其选择（仅当这两个内容相等时）。
#### 参数
{{book.one}} **newSnapshot** : [Image][Image](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_plugins_undo_Image.html)

  {{book.tow}} 带有新选择的新快照。
#### 返回
{{book.one}} **Boolean**

  {{book.tow}} 如果选择被修改，则返回`true`。
## 静态方法
### getKeyGroup( keyCode ) → Number
返回传递的keyCode所属的组。
#### 参数
{{book.one}} **keyCode** : Number
#### 返回
{{book.one}} **Number**
<hr>
### getOppositeKeyGroup( keyGroup ) → Number
#### 参数
{{book.one}}  **keyGroup** : Number
#### 返回
{{book.one}} **Number**
<hr>
### ieFunctionalKeysBug( keyCode ) → Boolean
我们是否需要在此环境中针对功能（退格键，删除键）不使用Internet Explorer中的按键事件以及指定的keyCode使用解决方法。
#### 参数
{{book.one}}  **keyCodey** : Number
#### 返回
{{book.one}} **Number**
<hr>
### isNavigationKey( keyCode ) → Boolean
检查一个键是否是导航键之一（箭头，页面向上/向下等）。 另请参阅[navigationKeyCodes](https://docs.ckeditor.com/ckeditor4/latest/api/CKEDITOR_plugins_undo_UndoManager.html#static-property-navigationKeyCodes)属性。
#### 参数
{{book.one}}  **keyCodey** : Number
#### 返回
{{book.one}} **Number**