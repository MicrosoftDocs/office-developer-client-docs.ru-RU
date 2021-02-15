---
title: Errors collection (ADO)
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
# <a name="errors-collection-ado"></a>Errors collection (ADO)


**Область применения**: Access 2013, Office 2013

Содержит все [объекты Error,](error-object-ado.md) созданные в ответ на один поставщик сбоев, связанный с поставщиком.

## <a name="remarks"></a>Заметки

Любая операция, включаемая объекты ADO, может создавать одну или несколько ошибок поставщика. При каждой ошибке один или несколько объектов **Error** можно поместить в коллекцию **Errors** объекта [Connection.](connection-object-ado.md) Когда другая операция ADO создает ошибку, коллекция **Errors** очищается, и новый набор объектов **Error** можно поместить в коллекцию **Errors.**

Каждый **объект Error** представляет определенную ошибку поставщика, а не ошибку ADO. Ошибки ADO оголевются механизмом обработки исключений во время работы. Например, в Microsoft Visual Basic ошибка ADO вызывает событие [onError](onerror-event-rds.md) и появляется в **объекте Err.**

Операции ADO, которые не вызывают ошибку, не влияют на **коллекцию ошибок.** Используйте метод [Clear](clear-method-ado.md) для очистки коллекции **Errors вручную.**

Набор объектов **Error** в коллекции **Errors** описывает все ошибки, которые произошли в ответ на один из них. Enumerating the specific errors in the Errors collection enables your error-handling **routines** to more precisely determine the cause and origin of an error, and take appropriate steps to recover.

Некоторые свойства и методы возвращают предупреждения, которые отображаются как объекты **Error** в коллекции **Errors,** но не останавливают выполнение программы. Перед вызовом методов [Resync,](resync-method-ado.md) [UpdateBatch](updatebatch-method-ado.md)или [CancelBatch](cancelbatch-method-ado.md) в [объекте Recordset,](recordset-object-ado.md) [методом Open](open-method-ado-connection.md) для объекта **Connection** или настройкам свойства [Filter](filter-property-ado.md) в **объекте Recordset** вызовите метод **Clear** для коллекции **Errors.** Таким образом можно считать свойство [Count](count-property-ado.md) коллекции **Errors** для проверки на возвращенных предупреждений.


> [!NOTE]
> Более **подробное описание** того, как одна операция ADO может создавать несколько ошибок, см. в разделе "Объект error".


