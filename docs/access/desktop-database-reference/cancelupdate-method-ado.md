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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296628"
---
# <a name="cancelupdate-method-ado"></a>Метод CancelUpdate (ADO)


**Область применения**: Access 2013, Office 2013

Отменяет все изменения, внесенные в текущую или новую строку объекта [Recordset](recordset-object-ado.md) или коллекцию [Fields](fields-collection-ado.md) объекта [Record,](record-object-ado.md) перед вызовом [метода Update.](update-method-ado.md)

## <a name="syntax"></a>Синтаксис

*recordset*. CancelUpdate

*record*. *Поля*. CancelUpdate

## <a name="remarks"></a>Заметки

**Recordset**

Используйте метод **CancelUpdate,** чтобы отменить все изменения, внесенные в текущую строку, или отменить добавленную строку. После вызова метода **Update** нельзя отменить изменения текущей или новой строки, если изменения не являются частью транзакции, которую можно откатить с помощью метода [RollbackTrans,](begintrans-committrans-and-rollbacktrans-methods-ado.md) или пакетного обновления. В случае пакетного обновления можно отменить обновление с помощью метода **CancelUpdate** или [CancelBatch.](cancelbatch-method-ado.md) 

При добавлении новой строки при вызове метода **CancelUpdate** текущая строка становится текущей перед вызовом [AddNew.](addnew-method-ado.md)

Если вы находитесь в режиме редактирования и хотите отключить текущую запись (например, с помощью [Move,](move-method-ado.md) [NextRecordset](nextrecordset-method-ado.md)или [Close),](close-method-ado.md)можно использовать **CancelUpdate,** чтобы отменить ожидающих изменений. Это может потребоваться, если не удается успешно опубликовать обновление в источнике данных (например, попытка удаления, которая не удалась из-за нарушения целостности, оставляет набор **записей** в режиме редактирования после вызова [delete).](delete-method-ado-recordset.md)

**Record**

Метод **CancelUpdate** отменяет ожидающих вставки или удаления объектов [Field](field-object-ado.md) и отменяет ожидающих обновлений существующих полей и восстанавливает их исходные значения. Для [свойства Status](status-property-ado-recordset.md) всех полей в коллекции **Fields** задается свойство **adFieldOK.**

