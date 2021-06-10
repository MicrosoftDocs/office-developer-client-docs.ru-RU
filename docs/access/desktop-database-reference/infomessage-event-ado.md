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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291444"
---
# <a name="infomessage-event-ado"></a>Событие InfoMessage (ADO)

**Область применения**: Access 2013, Office 2013

Событие **InfoMessage** называется всякий раз, когда предупреждение возникает во время **операции ConnectionEvent.**

## <a name="syntax"></a>Синтаксис

InfoMessage *pError*, *adStatus*, *pConnection*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*pError* |Объект [Ошибки.](error-object-ado.md) Этот параметр содержит все возвращаемые ошибки. Если возвращается несколько ошибок, задайте коллекцию **ошибок,** чтобы найти их.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Перед возвращением этого события установите этот параметр **adStatusUnwantedEvent,** чтобы предотвратить последующие уведомления.|
|*pConnection* |Объект [Подключения.](connection-object-ado.md) Подключение, для которого произошло предупреждение. Например, предупреждения могут возникать при открытии объекта **Подключения** или выполнении [команды](command-object-ado.md) на **подключении.**|

