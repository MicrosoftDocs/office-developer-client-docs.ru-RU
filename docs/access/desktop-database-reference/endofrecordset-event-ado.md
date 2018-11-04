---
title: Событие EndOfRecordset (ADO)
TOCTitle: EndOfRecordset event (ADO)
ms:assetid: 8995b851-dff6-2525-1d62-a2cfb4f95393
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249603(v=office.15)
ms:contentKeyID: 48546167
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 36babff0c6de48e0539375caaad367698906e3fd
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950190"
---
# <a name="endofrecordset-event-ado"></a>Событие EndOfRecordset (ADO)

**Применимо к**: Access 2013, Office 2013

Событие **EndOfRecordset** вызывается при попытке перейдите к строке за пределами [набора записей](recordset-object-ado.md).

## <a name="syntax"></a>Синтаксис

EndOfRecordset*fMoreData*, *adStatus* *pRecordset*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*fMoreData* |A **ВАРИАНТА\_BOOL** значение, которое, если значение типа VARIANT\_имеет значение TRUE, указывает, были добавлены увеличение количества строк **набора записей**.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). При вызове **EndOfRecordset** этот параметр имеет значение **adStatusOK** , если операция, которая вызвала событие прошла успешно. Если это событие не могут запрашивать отмену операции, вызвавшей это событие перейдут в **adStatusCantDeny** .<br/><br/>Прежде чем возвращает **EndOfRecordset** , присвойте этому параметру значение **adStatusUnwantedEvent** , чтобы запретить последующие уведомления.|
|*pRecordset* | Объект **набора записей** . **Набор записей** , для которого произошло это событие.|

## <a name="remarks"></a>Примечания

Событие **EndOfRecordset** может возникнуть, если происходит сбой операции [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) .

Этот обработчик событий вызывается при попытке переместить за пределами объекта **набора записей** , может быть выполнена в результате вызова **MoveNext**. Тем не менее в это событие может получить несколько записей из базы данных и добавить их в конец **набора записей**. В этом случае значение типа VARIANT *fMoreData* \_значение TRUE, а возвращаемое из **EndOfRecordset**. Затем вызовите **MoveNext** еще раз, чтобы получить доступ к недавно полученные записи.

