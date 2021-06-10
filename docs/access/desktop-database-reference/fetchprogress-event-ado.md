---
title: Событие FetchProgress (ADO)
TOCTitle: FetchProgress event (ADO)
ms:assetid: 09145d9a-ea5e-b41c-6c54-33ec83e642a9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248828(v=office.15)
ms:contentKeyID: 48543114
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d863f51e7836acdc577ecd720df77114ed66f067
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293184"
---
# <a name="fetchprogress-event-ado"></a>Событие FetchProgress (ADO)

**Область применения**: Access 2013, Office 2013

Событие **FetchProgress** периодически вызвано во время длительной асинхронной операции, чтобы сообщить, сколько еще строк в настоящее время было извлечено в [Набор записей.](recordset-object-ado.md)

## <a name="syntax"></a>Синтаксис

FetchProgress *Progress*, *MaxProgress*, *adStatus*, *pRecordset*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Progress* |**Длинное** значение, указывающее количество записей, которые в настоящее время были извлечены операцией получения.|
|*MaxProgress* |**Длинное** значение, указывающее максимальное количество записей, которые должны быть извлечены.|
|*adStatus* |Значение [состояния EventStatusEnum.](eventstatusenum.md)|
|*pRecordset* |Объект **Recordset,** который является объектом, для которого извлекаются записи.|

## <a name="remarks"></a>Примечания

При использовании **FetchProgress** с детским набором записей **следует** помнить, что значения параметров *Progress* и *MaxProgress* являются производными от ключевых строк [службы Cursor.](microsoft-cursor-service-for-ole-db-ado-service-component.md) Возвращенные значения представляют общее число записей в основном наборе строк, а не только количество записей в текущей главе.

> [!NOTE]
> Чтобы использовать **FetchProgress** с microsoft Visual Basic, Visual Basic 6.0 или более поздней.


