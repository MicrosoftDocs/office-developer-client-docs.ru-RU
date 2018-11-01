---
title: Событие ExecuteComplete (ADO)
TOCTitle: ExecuteComplete Event (ADO)
ms:assetid: 47317d97-e373-32f4-9438-2dff46b8d367
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249219(v=office.15)
ms:contentKeyID: 48544589
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e29db2848d7ec7b229831156ee64815a152a4bfc
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887903"
---
# <a name="executecomplete-event-ado"></a>Событие ExecuteComplete (ADO)


**Применимо к**: Access 2013, Office 2013



Событие **ExecuteComplete** вызывается после завершения выполнения команды.

## <a name="syntax"></a>Синтаксис

ExecuteComplete*RecordsAffected*, *pError*, *adStatus*, *командной*, *pRecordset*, *pConnection*

## <a name="parameters"></a>Параметры

  - *RecordsAffected*

  - **Длинное** значение, указывающее количество записей командой.

  - *pError*

  - Объект [Error](error-object-ado.md) . Описание ошибки, возникшей при имеет значение **adStatus** **adStatusErrorsOccurred**; в противном случае он не задан.

  - *adStatus*

  - [EventStatusEnum](eventstatusenum.md)
    
    Прежде чем возвращает это событие, присвойте этому параметру значение **adStatusUnwantedEvent** , чтобы запретить последующие уведомления.

  - *Командной*

  - Объект [команды](command-object-ado.md) , который был выполнен. Содержит объект **команды** , даже в том случае, если вызов **Connection.Execute** или **Recordset.Open** без явного создания **команды**, в каких случаях объект **команды** создается внутренне с ADO.

  - *pRecordset*

  - Объект [набора записей](recordset-object-ado.md) , в результате выполнения команды. Этот **набор записей** может быть пустым. Никогда не следует удалить объект набора записей из в этот обработчик событий. Это приведет к нарушение прав доступа, когда ADO пытается получить доступ к объекту, который больше не существует.

  - *pConnection*

  - Объект [подключения](connection-object-ado.md) . Подключение, для которого была выполнена операция.

## <a name="remarks"></a>Замечания

Событие **ExecuteComplete** может возникнуть из-за **подключения.** [Выполнение](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection), **команда.** [Выполнение](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command), **набора записей.** После [открытия](open-method-ado-recordset.md) **набора записей.** [Повторный запрос](requery-method-ado.md), или **набора записей.** Методы [NextRecordset](nextrecordset-method-ado.md) .

