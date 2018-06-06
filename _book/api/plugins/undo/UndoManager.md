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