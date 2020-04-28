---
title: Событие событие endofrecordset (ADO)
TOCTitle: EndOfRecordset event (ADO)
ms:assetid: 8995b851-dff6-2525-1d62-a2cfb4f95393
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249603(v=office.15)
ms:contentKeyID: 48546167
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 48e0eb25b443175013a144fafaa433df12c2cc9c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293562"
---
# <a name="endofrecordset-event-ado"></a>Событие событие endofrecordset (ADO)

**Область применения**: Access 2013, Office 2013

Событие **событие endofrecordset** вызывается при попытке переместиться в строку, находящиеся за концом объекта [Recordset](recordset-object-ado.md).

## <a name="syntax"></a>Синтаксис

Событие endofrecordset*фморедата*, *адстатус*, *pRecordset* пред

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*фморедата* |**Логическое значение\_Variant** , которое, если задано значение\_Variant true, указывает, что в **набор записей**Добавлено больше строк.|
|*адстатус* |[Евентстатусенум](eventstatusenum.md). При вызове **событие endofrecordset** этот параметр имеет значение **адстатусок** , если операция, вызвавшая событие, прошла успешно. Он имеет значение **адстатускантдени** , если данное событие не может запрашивать отмену операции, вызвавшей это событие.<br/><br/>Перед возвратом **событие endofrecordset** присвойте этому параметру значение **адстатусунвантедевент** , чтобы предотвратить появление последующих уведомлений.|
|*предшнур* | Объект **Recordset** . Объект **Recordset** , для которого произошло это событие.|

## <a name="remarks"></a>Примечания

Если не удается выполнить операцию [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) , может произойти событие **событие endofrecordset** .

Этот обработчик событий вызывается при попытке переместиться за конец объекта **Recordset** , возможно, в результате вызова **MoveNext**. Однако в этом событии можно получить дополнительные записи из базы данных и добавить их в конец **набора записей**. В этом случае задайте для *фморедата* \_значение true и вернитесь из **событие endofrecordset**. Затем снова вызовите **MoveNext** , чтобы получить доступ к недавно извлеченным записям.

