---
title: События WillMove и MoveComplete (ADO)
TOCTitle: WillMove and MoveComplete events (ADO)
ms:assetid: fe7eb823-b388-6b3d-1ae9-056018032ef5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250307(v=office.15)
ms:contentKeyID: 48548937
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e663e18a13803097d490e0e315d139e6e15400da
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306057"
---
# <a name="willmove-and-movecomplete-events-ado"></a>События WillMove и MoveComplete (ADO)

**Область применения**: Access 2013, Office 2013

Событие **WillMove вызвано** до того, как ожидающая операция изменяет текущую позицию в [Наборе записей.](recordset-object-ado.md) Событие **MoveComplete** вызвано после изменения текущей позиции **в Recordset.**

## <a name="syntax"></a>Синтаксис

WillMove *adReason*, *adStatus*, *pRecordset*

MoveComplete *adReason*, *pError*, *adStatus*, *pRecordset*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*adReason* |Значение [EventReasonEnum,](eventreasonenum.md) которое указывает причину этого события. Его значение может быть **adRsnMoveFirst**, **adRsnMoveLast**, **adRsnMoveNext**, **adRsnMovePrevious**, **adRsnMove**, или **adRsnRequery**.|
|*pError* |Объект [Ошибки.](error-object-ado.md) Он описывает ошибку, которая произошла, если значение *adStatus* **является adStatusErrorsOccurred;** в противном случае она не установлена.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Когда **вызывается WillMove,** этот параметр задан **adStatusOK,** если операция, которая вызвала событие, была успешной. Оно устанавливается **для adStatusCantDeny,** если это событие не может запросить отмену ожидающей операции. <br/><br/>Когда **вызывается MoveComplete,** этот параметр задан **adStatusOK,** если операция, вызвавла событие, была успешной, или **adStatusErrorsOccurred,** если операция не удалась. <br/><br/>Перед возвращением **WillMove** установите этот параметр **adStatusCancel** для запроса отмены ожидаемой операции или установите этот параметр adStatusUnwantedEvent для предотвращения последующих замений. <br/><br/>Перед **возвращением MoveComplete** установите этот параметр **adStatusUnwantedEvent,** чтобы предотвратить последующие уведомления.|
|*pRecordset* |Объект [Recordset.](recordset-object-ado.md) **Набор записей,** для которого произошло это событие.|

## <a name="remarks"></a>Примечания

Событие **WillMove или** **MoveComplete** может произойти из-за следующих операций **Recordset:**

- [Open](open-method-ado-recordset.md)
- [Move](move-method-ado.md)
- [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)
- [MoveLast](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)
- [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) 
- [MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)
- [AddNew](addnew-method-ado.md)
- [Requery](requery-method-ado.md)

Эти события могут возникать из-за следующих свойств:

- [Filter](filter-property-ado.md)
- [Index](index-property-ado.md)
- [Bookmark](bookmark-property-ado.md)
- [AbsolutePage](absolutepage-property-ado.md)
- [AbsolutePosition](absoluteposition-property-ado.md)

Эти события также происходят, если у ребенка **Recordset** подключены события **Recordset** и родительский **набор записей** перемещается.

Параметр *adStatus* необходимо задать **adStatusUnwantedEvent** для каждого возможного значения *adReason,* чтобы полностью остановить уведомление о событии для любого события, которое включает параметр *adReason.*

