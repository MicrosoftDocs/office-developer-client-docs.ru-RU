---
title: События WillMove и MoveComplete (ADO)
TOCTitle: WillMove and MoveComplete events (ADO)
ms:assetid: fe7eb823-b388-6b3d-1ae9-056018032ef5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250307(v=office.15)
ms:contentKeyID: 48548937
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 79809f9c802a5e5312b3adf3e64ecaa32a443a04
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949644"
---
# <a name="willmove-and-movecomplete-events-ado"></a>События WillMove и MoveComplete (ADO)

**Применимо к**: Access 2013, Office 2013

Событие **WillMove** вызывается перед ожидающие операции изменяет текущую позицию в наборе [записей](recordset-object-ado.md). Событие **MoveComplete** вызывается после текущей позиции в изменения **записей** .

## <a name="syntax"></a>Синтаксис

WillMove*adReason*, *adStatus* *pRecordset*

MoveComplete*adReason*, *pError*, *adStatus*, *pRecordset*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*adReason* |Значение [EventReasonEnum](eventreasonenum.md) , указывает причину это событие. Его значение может быть **adRsnMoveFirst**, **adRsnMoveLast**, **adRsnMoveNext**, **adRsnMovePrevious**, **adRsnMove**или **adRsnRequery**.|
|*pError* |Объект [Error](error-object-ado.md) . Описание ошибки, возникшей при имеет значение *adStatus* **adStatusErrorsOccurred**; в противном случае он не задан.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). При вызове **WillMove** этот параметр имеет значение **adStatusOK** , если операция, которая вызвала событие прошла успешно. Если это событие не могут запрашивать отмену ожидающие операции перейдут в **adStatusCantDeny** . <br/><br/>При вызове **MoveComplete** этот параметр имеет значение **adStatusOK** в случае успешного операцию, которая вызвала событие или **adStatusErrorsOccurred** , если операция завершилась неудачно. <br/><br/>Прежде чем возвращает **WillMove** , присвойте этому параметру значение **adStatusCancel** для запроса отмены ожидающие операции или присвойте этому параметру значение adStatusUnwantedEvent, чтобы запретить последующие notications. <br/><br/>Прежде чем возвращает **MoveComplete** , присвойте этому параметру значение **adStatusUnwantedEvent** , чтобы запретить последующие уведомления.|
|*pRecordset* |Объект [набора записей](recordset-object-ado.md) . **Набор записей** , для которого произошло это событие.|

## <a name="remarks"></a>Примечания

Событие **WillMove** или **MoveComplete** могут быть вызваны следующие операции **набора записей** :

- [Открытие](open-method-ado-recordset.md)
- [Перемещение](move-method-ado.md)
- [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)
- [MoveLast](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)
- [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) 
- [MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)
- [AddNew](addnew-method-ado.md)
- [Обновление](requery-method-ado.md)

Эти события могут возникнуть из-за следующие свойства:

- [Filter](filter-property-ado.md)
- [Индекс](index-property-ado.md)
- [Закладка](bookmark-property-ado.md)
- [AbsolutePage](absolutepage-property-ado.md)
- [AbsolutePosition](absoluteposition-property-ado.md)

Эти события также возникают при дочерних **записей** имеет **записей** событий подключенных и родительский перемещены **набора записей** .

Параметр *adStatus* должен значение **adStatusUnwantedEvent** для каждого *adReason* возможные значения для полностью остановите уведомления о событиях для любого события, которое включает параметр *adReason* .

