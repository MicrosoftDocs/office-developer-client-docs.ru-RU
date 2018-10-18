---
<<<<<<< Название HEAD: TOCTitle свойство EditMode (ADO): свойство EditMode (ADO) === название: свойство EditMode (ADO) TOCTitle: свойство EditMode (ADO)
>>>>>>> главные ms:assetid: 28ca8f14-abee-ad20-9c16-11bb36b487e4 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249045(v=office.15) ms:contentKeyID: 48543867 ms.date: 09/18/2015 mtps_version: v=office.15
---

<<<<<<< HEAD
# <a name="editmode-property-ado"></a>EditMode Property (ADO)
=======
# <a name="editmode-property-ado"></a>Свойство EditMode (ADO)
>>>>>>> master


**Применимо к**: Access 2013 | Office 2013

Указывает состояние редактирования текущей записи.

<<<<<<< HEAD
## <a name="return-value"></a>Возвращаемое значение
=======
## <a name="return-value"></a>Возвращаемое значение
>>>>>>> master

Возвращает значение [EditModeEnum](editmodeenum.md) .

## <a name="remarks"></a>Замечания

ADO поддерживает редактирования буфера, связанного с текущей записи. Это свойство показывает ли изменения были внесены в этот буфер или создан ли новую запись. Свойство **EditMode** используется для определения статуса редактирования текущей записи. Можно проверить наличие ожидающих изменений, если редактирования процесс был прерван и определите, нужно ли использовать [обновления](update-method-ado.md) или метод [CancelUpdate](cancelupdate-method-ado.md) .

В разделе метод [AddNew](addnew-method-ado.md) более подробное описание свойства **EditMode** в различных условиях редактирования.

Когда звонка для [удаления](delete-method-ado-recordset.md) успешно не удалять записи или записей в данных источника (из-за нарушения ссылочной целостности, например), [записей](recordset-object-ado.md) останется в режиме редактирования (**EditMode** = **adEditInProgress **). Это означает, что **CancelUpdate** необходимо вызывать перед перемещением off текущей записи (с [перемещением](move-method-ado.md), [NextRecordset](nextrecordset-method-ado.md)и [Закрыть](close-method-ado.md), например).


> [!NOTE]
> <P><STRONG>EditMode</STRONG> можно вернуть допустимое значение только в том случае, если текущая запись. <STRONG>EditMode</STRONG> возвращает ошибку, если <A href="bof-eof-properties-ado.md">BOF или EOF</A> имеет значение true, или если текущий запись была удалена.</P>


