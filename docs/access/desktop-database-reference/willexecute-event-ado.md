---
title: WillExecute event (ADO)
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
# <a name="willexecute-event-ado"></a>WillExecute event (ADO)

**Область применения**: Access 2013, Office 2013

Событие **WillExecute** вызвано перед выполнением ожидающих выполнения команды для подключения.

## <a name="syntax"></a>Синтаксис

WillExecute *Source*, *CursorType,* *LockType*, *Options*, *adStatus*, *pCommand*, *pRecordset*, *pConnection*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Source* |**Строка,** содержаная SQL или сохраненное имя процедуры.|
|*CursorType* |[CursorTypeEnum,](cursortypeenum.md) содержащий тип курсора для **открываемого** наборов записей. С помощью этого параметра можно изменить курсор на любой тип во время операции **Recordset** [Open.](open-method-ado-recordset.md) *CursorType* будет игнорироваться для любой другой операции.|
|*LockType* |[LockTypeEnum,](locktypeenum.md) содержащий тип блокировки для **открываемого** наборов записей. С помощью этого параметра можно изменить блокировку на любой тип во время операции **Open в наборе**  записей. *LockType* будет игнорироваться для любой другой операции.|
|*Options* |**Длинное** значение, которое указывает параметры, которые можно использовать для выполнения команды или открытия **recordset.**|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Перед возвращением этого события установите для этого параметра параметр **adStatusUnwantedEvent,** чтобы запретить последующие уведомления, или **adStatusCancel** для запроса отмены операции, которая вызвала это событие.|
|*pCommand* |Объект [Command,](command-object-ado.md) к которому применяется это уведомление о событии.|
|*pRecordset* |Объект [Recordset,](recordset-object-ado.md) к которому применяется это уведомление о событии.|
|*pConnection* |Объект [Connection,](connection-object-ado.md) к которому применяется это уведомление о событии.|

## <a name="remarks"></a>Заметки

Событие **WillExecute** может произойти из-за **подключения.** [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection), **Command.** [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command)( или **Recordset).** [Метод Open](open-method-ado-recordset.md) параметр *pConnection* всегда должен содержать допустимую ссылку на **объект Connection.** Если событие вызвано **Connection.Exe,** *параметры pRecordset* и *pCommand* заданы как **Nothing.** Если событие вызвано **recordset.Open,** параметр *pRecordset* будет ссылаться на объект **Recordset,** а для параметра *pCommand* задан параметр **Nothing.** Если событие вызвано **Command.Exe,** параметр *pCommand* будет ссылаться на объект **Command,** а для параметра *pRecordset* задан параметр **Nothing.**

**WillExecute** позволяет проверить и изменить ожидающих выполнения параметров. Это событие может возвращать запрос на отмену ожидающих команд.

