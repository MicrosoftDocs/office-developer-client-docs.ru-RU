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

Событие **EndOfRecordset** вызвано при попытке перейти к строке, прошедшей в конце [recordset.](recordset-object-ado.md)

## <a name="syntax"></a>Синтаксис

EndOfRecordset *fMoreData*, *adStatus*, *pRecordset*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*fMoreData* |Значение **VARIANT \_ BOOL,** которое при заданном значении VARIANT TRUE указывает, что в набор Recordset добавлено больше \_ **строк.**|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Когда **вызывается EndOfRecordset,** этот параметр задан **adStatusOK,** если операция, которая вызвала событие, была успешной. Оно задалось **adStatusCantDeny,** если это событие не может запросить отмену операции, которая вызвала это событие.<br/><br/>Перед **возвращением EndOfRecordset** установите этот параметр **adStatusUnwantedEvent,** чтобы предотвратить последующие уведомления.|
|*pRecordset* | Объект **Recordset.** **Набор записей,** для которого произошло это событие.|

## <a name="remarks"></a>Примечания

Событие **EndOfRecordset может** произойти в случае срыва операции [MoveNext.](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)

Обработец этого события вызывается при попытке переместиться за конец объекта **Recordset,** возможно, в результате вызова **MoveNext**. Тем не менее, в этом случае можно получить больше записей из базы данных и примкать их к концу **recordset**. В этом случае установите *fMoreData* в VARIANT \_ TRUE и вернись из **EndOfRecordset.** Затем снова **позвоните в MoveNext,** чтобы получить доступ к вновь полученным записям.

