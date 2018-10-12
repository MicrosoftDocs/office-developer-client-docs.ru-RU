---
title: WillExecute Event (ADO)
TOCTitle: WillExecute Event (ADO)
ms:assetid: 9f516bfd-246d-9817-4ca3-64598ab466f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249732(v=office.15)
ms:contentKeyID: 48546686
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8a5c739ffd408a1f53539c88a3bdc4169eb4cebe
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480103"
---
# <a name="willexecute-event-ado"></a>WillExecute Event (ADO)


**Применимо к**: Access 2013 | Office 2013


Событие **WillExecute** называется просто до выполнения ожидающие команды для подключения.

## <a name="syntax"></a>Синтаксис

*Источник*, *CursorType*WillExecute *LockType для*, *Параметры*, *adStatus*, *командной*, *pRecordset*, *pConnection*

## <a name="parameters"></a>Параметры

  - *Source*

  - **Строка** , содержащая команду SQL или хранимую процедуру имя.

  - *CursorType*

  - [CursorTypeEnum](cursortypeenum.md) , которая содержит тип текущей позиции для **набора записей** , который будет открыт. С помощью этого параметра можно изменить курсор к любому типу во время операции [открытия](open-method-ado-recordset.md) **набора записей** . *CursorType* будет игнорироваться для другой операции.

  - *LockType для*

  - [LockTypeEnum](locktypeenum.md) , которая содержит тип блокировки для **набора записей** , который будет открыт. С помощью этого параметра можно изменить блокировки к любому типу во время операции **открытия** **набора записей** . *LockType для* будет игнорироваться для другой операции.

  - *Варианты*

  - Значение типа **Long** , указывает параметры, которые можно использовать для выполнения команды или открыть **набора записей**.

  - *adStatus*

  - [EventStatusEnum](eventstatusenum.md)
    
    Прежде чем возвращает это событие, присвойте этому параметру значение **adStatusUnwantedEvent** , чтобы запретить последующие уведомления или **adStatusCancel** для запроса отмены операцию, которая вызвала событие.

  - *Командной*

  - Объект [команды](command-object-ado.md) , для которого применяется этого уведомления о событиях.

  - *pRecordset*

  - Объект [набора записей](recordset-object-ado.md) , к которому применяется этот уведомления о событии.

  - *pConnection*

  - Объект [подключения](connection-object-ado.md) , для которого применяется этого уведомления о событиях.

## <a name="remarks"></a>Замечания

Событие **WillExecute** могут возникнуть из-за **подключения.** [Выполнение](https://msdn.microsoft.com/library/jj249832\(v=office.15\)), **команда.** [Выполнение](https://msdn.microsoft.com/library/jj248785\(v=office.15\)), или **набора записей.** Метод [Open](open-method-ado-recordset.md) параметр *pConnection* всегда должен содержать ссылку на допустимый объект **подключения** . Если событие из-за **Connection.Execute** *pRecordset* и *командной* — значение **Nothing**. Если событие из-за **Recordset.Open**параметр *pRecordset* ссылается на объект **набора записей** , параметр *командной* задано значение **Nothing**. Если событие из-за **Command.Execute**, параметр *командной* ссылаются на объект **команды** и *pRecordset* параметру присвоено значение **Nothing**.

**WillExecute** позволяет проверять и изменять параметры ожидающих выполнения. Это событие может возвратить запрос на отменить ожидающие команды.
