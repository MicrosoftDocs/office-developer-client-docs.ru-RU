---
title: Событие EndOfRecordset (ADO)
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
# <a name="endofrecordset-event-ado"></a>Событие EndOfRecordset (ADO)

**Область применения**: Access 2013, Office 2013

Событие **EndOfRecordset** вызвано при попытке перейти к строке за конец [recordset.](recordset-object-ado.md)

## <a name="syntax"></a>Синтаксис

EndOfRecordset *fMoreData*, *adStatus*, *pRecordset*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*fMoreData* |Значение **VARIANT \_ BOOL,** если задано значение VARIANT TRUE, указывает, что в набор Recordset добавлены \_ **дополнительные строки.**|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). При **вызываемом endOfRecordset** этот параметр задан как **adStatusOK,** если операция, которая привела к событию, была успешной. Если это событие не может запросить отмену операции, которая привела к этому событию, устанавливается в качестве **adStatusCantDeny.**<br/><br/>Перед **возвращением EndOfRecordset** установите для этого параметра **параметр adStatusUnwantedEvent,** чтобы предотвратить последующие уведомления.|
|*pRecordset* | Объект **Recordset.** Набор **записей,** для которого произошло это событие.|

## <a name="remarks"></a>Заметки

Событие **EndOfRecordset может** произойти, если произойдет сбой операции [MoveNext.](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)

Этот обработец событий вызывается при попытке переместиться за конец объекта **Recordset,** возможно, в результате вызова **MoveNext.** Однако в этом событии можно получить больше записей из базы данных и применить их к концу **recordset.** В этом случае установите *для fMoreData* variant \_ TRUE и вернетесь из **EndOfRecordset.** Затем снова **вызовите MoveNext,** чтобы получить доступ к недавно полученным записям.

