---
title: Событие WillExecute (ADO)
TOCTitle: WillExecute event (ADO)
ms:assetid: 9f516bfd-246d-9817-4ca3-64598ab466f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249732(v=office.15)
ms:contentKeyID: 48546686
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7fe15604d0160afcbde5fdf02eaa6a7831da874b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302759"
---
# <a name="willexecute-event-ado"></a>Событие WillExecute (ADO)

**Область применения**: Access 2013, Office 2013

Событие **WillExecute** вызвано перед выполнением отложенной команды на подключение.

## <a name="syntax"></a>Синтаксис

WillExecute *Source*, *CursorType*, *LockType*, *Options*, *adStatus*, *pCommand*, *pRecordset*, *pConnection*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Source* |**Строка,** которая содержит SQL или сохраненное имя процедуры.|
|*CursorType* |[CursorTypeEnum,](cursortypeenum.md) содержащий тип курсора для открываемого **наборов** записей. С помощью этого параметра можно изменить курсор на любой тип во время операции **Recordset** [Open.](open-method-ado-recordset.md) *CursorType* будет игнорироваться для любой другой операции.|
|*LockType* |[LockTypeEnum,](locktypeenum.md) содержащий тип блокировки для открываемого **Набор** записей. С помощью этого параметра можно изменить блокировку на любой тип во время операции **Recordset** **Open.** *LockType* будет игнорироваться для любой другой операции.|
|*Options* |**Длинное** значение, которое указывает параметры, которые можно использовать для выполнения команды или открытия **наборов записей.**|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Перед возвращением этого события установите этот параметр **adStatusUnwantedEvent** для предотвращения последующих уведомлений или **adStatusCancel** для запроса отмены операции, которая вызвала это событие.|
|*pCommand* |Объект [Command,](command-object-ado.md) для которого применяется это уведомление о событии.|
|*pRecordset* |Объект [Recordset,](recordset-object-ado.md) для которого применяется это уведомление о событии.|
|*pConnection* |Объект [Connection,](connection-object-ado.md) для которого применяется это уведомление о событии.|

## <a name="remarks"></a>Примечания

Событие **WillExecute** может произойти из-за **подключения.** [Выполнение](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection), **Команда.** [Выполнение](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command)или **набор записей.** [Открытый](open-method-ado-recordset.md) метод *Параметр pConnection* всегда должен содержать допустимую ссылку на **объект Подключения.** Если событие связано с **Connection.Exe,** *параметры pRecordset* и *pCommand* заданы в **Nothing**. Если событие связано с **Recordset.Open,** параметр *pRecordset* будет ссылаться на объект **Recordset,** а параметр *pCommand* задан в **Nothing**. Если событие связано с **Command.Exe,** параметр *pCommand* будет ссылаться на объект **Command,** а параметр *pRecordset* задан в **Nothing**.

**WillExecute** позволяет изучить и изменить параметры ожидающих выполнения. Это событие может вернуть запрос об отмене ожидаемой команды.

