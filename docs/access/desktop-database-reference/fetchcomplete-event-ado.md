---
title: Событие FetchComplete (ADO)
TOCTitle: FetchComplete event (ADO)
ms:assetid: 4863d5b5-7d77-bdef-c511-f85c9e6dec9d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249224(v=office.15)
ms:contentKeyID: 48544621
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f4c1cb1379d1faec39fd44fa8273fba4aadca548
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293191"
---
# <a name="fetchcomplete-event-ado"></a>Событие FetchComplete (ADO)

**Область применения**: Access 2013, Office 2013

Событие **FetchComplete** вызвано после того, как все записи в длинной асинхронной операции были извлечены в [набор Recordset.](recordset-object-ado.md)

## <a name="syntax"></a>Синтаксис

FetchComplete *pError*, *adStatus*, *pRecordset*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*pError* |Объект [Ошибки.](error-object-ado.md) Он описывает ошибку, которая произошла, если значение **adStatus** **является adStatusErrorsOccurred;** в противном случае она не установлена.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Перед возвращением этого события установите этот параметр **adStatusUnwantedEvent,** чтобы предотвратить последующие уведомления.|
|*pRecordset* |Объект **Recordset.** Объект, для которого были извлечены записи.|

## <a name="remarks"></a>Примечания

Чтобы использовать **FetchComplete** с microsoft Visual Basic, Visual Basic 6.0 или более поздней.

