---
title: Событие событие executecomplete (ADO)
TOCTitle: ExecuteComplete event (ADO)
ms:assetid: 47317d97-e373-32f4-9438-2dff46b8d367
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249219(v=office.15)
ms:contentKeyID: 48544589
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8a094968e70ace5e6cba1df184bf0ba57c2d7789
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293226"
---
# <a name="executecomplete-event-ado"></a>Событие событие executecomplete (ADO)

**Область применения**: Access 2013, Office 2013

Событие **событие executecomplete** вызывается после завершения выполнения команды.

## <a name="syntax"></a>Синтаксис

Событие executecomplete*рекордсаффектед*, *перрор*, *адстатус*, *пкомманд*, *пода*, *пконнектион*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*рекордсаффектед* |**Длинное** значение, указывающее количество записей, на которые влияет команда.|
|*перрор* |Объект [Error](error-object-ado.md) . В нем описывается ошибка, которая возникла, если значение **адстатус** равно **адстатусеррорсоккурред**; в противном случае он не задается.|
|*адстатус* |[Евентстатусенум](eventstatusenum.md). Перед возвращением этого события установите для этого параметра значение **адстатусунвантедевент** , чтобы предотвратить появление последующих уведомлений.|
|*пкомманд* |[Командный](command-object-ado.md) объект, который был выполнен. Содержит объект **Command** даже при вызове метода **Connection. Execute** или **Recordset. Open** без явного создания **команды**, при этом объект **Command** создается внутри ADO.|
|*предшнур* |Объект [Recordset](recordset-object-ado.md) , являющийся результатом выполненной команды. Этот **набор записей** может быть пустым. Не следует удалять этот объект Recordset из этого обработчика событий. Это приведет к нарушению прав доступа при попытке ADO получить доступ к объекту, который больше не существует.|
|*пконнектион* |Объект [Connection](connection-object-ado.md) . Подключение, для которого выполнялась операция.|

## <a name="remarks"></a>Примечания

В связи с **подключением** может возникнуть событие **событие executecomplete** . [Выполнение](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection), **команда.** [EXECUTE](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command), **Recordset.** [Открыть](open-method-ado-recordset.md), **Recordset.** [Requery](requery-method-ado.md)или **Recordset.** Методы [NextRecordset](nextrecordset-method-ado.md) .

