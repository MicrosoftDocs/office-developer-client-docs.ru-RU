---
title: Метод CancelUpdate (ADO)
TOCTitle: CancelUpdate method (ADO)
ms:assetid: 2bd4d168-ba52-7786-5046-44febeda88e1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249065(v=office.15)
ms:contentKeyID: 48543938
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4585679688929532d7f50be9efc71b2830bb6587
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711247"
---
# <a name="cancelupdate-method-ado"></a>Метод CancelUpdate (ADO)


**Применимо к**: Access 2013, Office 2013

Отменяет все изменения, внесенные в строку текущей или новый объект [набора записей](recordset-object-ado.md) или коллекции [полей](fields-collection-ado.md) объекта [записи](record-object-ado.md) , прежде чем вызывать метод [Update](update-method-ado.md) .

## <a name="syntax"></a>Синтаксис

*набор записей*. CancelUpdate

*запись*. *Поля*. CancelUpdate

## <a name="remarks"></a>Замечания

**Recordset**

Используйте метод **CancelUpdate** для отмены всех изменений, внесенных в текущей строке или отменить новые строки. Нельзя отменить изменения для текущей строки или новую строку после вызова метода **обновления** , если изменения не являются частью транзакции, можно отменить с помощью метода [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) или в составе пакета обновления. В случае пакета обновления можно отменить **обновление** с помощью метода **CancelUpdate** или [CancelBatch](cancelbatch-method-ado.md) .

При добавлении новой строки при вызове метода **CancelUpdate** текущей строки становится строку, которая была текущей до вызова [метода AddNew](addnew-method-ado.md) .

Если вы находитесь в режиме редактирования и требуется переместить текущей записи (например, с помощью [перемещения](move-method-ado.md), [NextRecordset](nextrecordset-method-ado.md)или [Закрыть](close-method-ado.md)), чтобы отменить ожидающие изменения можно использовать **CancelUpdate** . Может появиться в случае, если обновление не может успешно учтены к источнику данных (например, попытка delete, возникает ошибка из-за нарушения целостности данных оставьте **записей** в режиме редактирования после вызова метода для [удаления](delete-method-ado-recordset.md)).

**Record**

Метод **CancelUpdate** отменяет все ожидающие вставку или удаление объектов [полей](field-object-ado.md) и показано, как отменить ожидающие обновления существующего поля и восстанавливает их значения. [Состояние](status-property-ado-recordset.md) всех полей в коллекции **полей** задано значение **adFieldOK**.

