---
title: Коллекция Errors (ADO)
TOCTitle: Errors collection (ADO)
ms:assetid: 76c234b8-7fec-11c5-275e-864d5d880ee7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249486(v=office.15)
ms:contentKeyID: 48545706
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: db9fa4fccc4f3d13849f34c157f2ea07cc3f171d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293429"
---
# <a name="errors-collection-ado"></a>Коллекция Errors (ADO)


**Область применения**: Access 2013, Office 2013

Содержит все объекты [Error](error-object-ado.md) , созданные в ответ на один поставщик сбоев, связанный с поставщиком.

## <a name="remarks"></a>Примечания

Любая операция, включающая объекты ADO, может создавать одну или несколько ошибок поставщика. При возникновении каждой ошибки в коллекцию **Errors** объекта [Connection](connection-object-ado.md) можно поместить один или несколько объектов **Error** . Если при выполнении другой операции ADO возникает ошибка, удаляется коллекция **Errors** , и в коллекцию **Errors** можно поместить новый набор объектов **Error** .

Каждый объект **Error** представляет определенную ошибку поставщика, а не ошибку ADO. Ошибки ADO, доступные в механизме обработки исключений времени выполнения. Например, в Microsoft Visual Basic при возникновении ошибки, относящейся к ADO, вызывается событие [OnError](onerror-event-rds.md) и отображается в объекте **Err** .

Операции ADO, не создающие ошибку, не влияют на коллекцию **Errors** . Используйте метод [clear](clear-method-ado.md) для очистки коллекции **ошибок** вручную.

Набор объектов **Error** в коллекции **Errors** описывает все ошибки, произошедшие в ответ на один оператор. Перечисление определенных ошибок **в семействе Errors** позволяет подпрограммам обработки ошибок определять причину и происхождение ошибки и выполнять необходимые действия для восстановления.

Некоторые свойства и методы возвращают предупреждения, которые отображаются как объекты **Error** в коллекции **Errors** , но не приводят к остановке выполнения программы. Перед вызовом методов [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md)или [CancelBatch](cancelbatch-method-ado.md) для объекта [Recordset](recordset-object-ado.md) , метода [Open](open-method-ado-connection.md) для объекта **Connection** или установки свойства [Filter](filter-property-ado.md) для объекта **Recordset** вызовите метод **clear** в коллекции **Errors** . Таким образом можно прочитать свойство [Count](count-property-ado.md) коллекции **Errors** , чтобы проверить наличие возвращенных предупреждений.


> [!NOTE]
> В разделе **Error** Object содержится более подробное объяснение того, как одна операция ADO может создавать несколько ошибок.


