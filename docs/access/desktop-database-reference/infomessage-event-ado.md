---
title: Событие InfoMessage (ADO)
TOCTitle: InfoMessage event (ADO)
ms:assetid: 5d4f487f-96c8-4cf6-60ab-583510d3096f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249328(v=office.15)
ms:contentKeyID: 48545109
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 879d8e7b3733937687671a164f86dbb273cf7533
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699900"
---
# <a name="infomessage-event-ado"></a>Событие InfoMessage (ADO)

**Применимо к**: Access 2013, Office 2013

При появлении предупреждения в процессе выполнения операции **ConnectionEvent** вызывает события **InfoMessage** .

## <a name="syntax"></a>Синтаксис

InfoMessage*pError*, *adStatus* *pConnection*

## <a name="parameters"></a>Parameters

|Параметр|Описание|
|:--------|:----------|
|*pError* |Объект [Error](error-object-ado.md) . Этот параметр содержит все ошибки, которые возвращаются. Если возвращаются несколько ошибок, перечисление семейство **Errors** их поиск.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Прежде чем возвращает это событие, присвойте этому параметру значение **adStatusUnwantedEvent** , чтобы запретить последующие уведомления.|
|*pConnection* |Объект [подключения](connection-object-ado.md) . Подключение, для которого произошло предупреждение. К примеру, можно предупреждений при открытии **подключения** объекта или выполнения [команды](command-object-ado.md) для **подключения**.|

