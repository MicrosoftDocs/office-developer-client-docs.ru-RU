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

ОтМеняет любые изменения, внесенные в текущую или новую строку объекта [Recordset](recordset-object-ado.md) , или коллекцию [Fields](fields-collection-ado.md) объекта [Record](record-object-ado.md) перед вызовом метода [Update](update-method-ado.md) .

## <a name="syntax"></a>Синтаксис

*набор записей*. CancelUpdate

*запись*. *Поля*. CancelUpdate

## <a name="remarks"></a>Замечания

**Recordset**

Используйте метод **CancelUpdate** , чтобы отменить все изменения, внесенные в текущую строку, или удалить только что добавленную строку. Вы не можете отменить изменения в текущей строке или новой строке после вызова метода **Update** , если изменения не являются частью транзакции, которую можно откатить методом [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) или частью пакетного обновления. В случае пакетного обновления вы можете отменить **Обновление** с помощью метода **CancelUpdate** или [CancelBatch](cancelbatch-method-ado.md) .

Если вы добавляете новую строку при вызове метода **CancelUpdate** , текущая строка становится текущей строкой до вызова [AddNew](addnew-method-ado.md) .

Если вы переходите в режим правки и хотите переместиться из текущей записи (например, с помощью [Move](move-method-ado.md), [NextRecordset](nextrecordset-method-ado.md)или [Close](close-method-ado.md)), можно отменить ожидающие изменения с помощью **CancelUpdate** . Это может потребоваться, если обновление невозможно успешно отправить в источник данных (например, попытка удалить, которая не удалась из-за нарушений целостности данных, оставляет объект **Recordset** в режиме редактирования после вызова [Delete](delete-method-ado-recordset.md)).

**Record**

Метод **CancelUpdate** отменяет все ожидающие вставки или удаления объектов [field](field-object-ado.md) , а также отменяет ожидающие обновления существующих полей и восстанавливает их исходные значения. Свойству [Status](status-property-ado-recordset.md) всех полей в коллекции **Fields** присвоено значение **адфиелдок**.

