---
title: Свойство EditMode (ADO)
TOCTitle: EditMode property (ADO)
ms:assetid: 28ca8f14-abee-ad20-9c16-11bb36b487e4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249045(v=office.15)
ms:contentKeyID: 48543867
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4c859d85dc62e09a1fd21af11deaca5d0f2e8b85
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867351"
---
# <a name="editmode-property-ado"></a>Свойство EditMode (ADO)


**Применимо к**: Access 2013, Office 2013

Указывает состояние редактирования текущей записи.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение [EditModeEnum](editmodeenum.md) .

## <a name="remarks"></a>Замечания

ADO поддерживает редактирования буфера, связанного с текущей записи. Это свойство показывает ли изменения были внесены в этот буфер или создан ли новую запись. Свойство **EditMode** используется для определения статуса редактирования текущей записи. Можно проверить наличие ожидающих изменений, если редактирования процесс был прерван и определите, нужно ли использовать [обновления](update-method-ado.md) или метод [CancelUpdate](cancelupdate-method-ado.md) .

В разделе метод [AddNew](addnew-method-ado.md) более подробное описание свойства **EditMode** в различных условиях редактирования.

Когда звонка для [удаления](delete-method-ado-recordset.md) успешно не удалять записи или записей в данных источника (из-за нарушения ссылочной целостности, например), [записей](recordset-object-ado.md) останется в режиме редактирования (**EditMode** = **adEditInProgress **). Это означает, что **CancelUpdate** необходимо вызывать перед перемещением off текущей записи (с [перемещением](move-method-ado.md), [NextRecordset](nextrecordset-method-ado.md)и [Закрыть](close-method-ado.md), например).


> [!NOTE]
> **EditMode** можно вернуть допустимое значение только в том случае, если текущая запись. **EditMode** возвращает ошибку, если [BOF или EOF](bof-eof-properties-ado.md) имеет значение true, или если текущий запись была удалена.


