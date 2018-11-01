---
title: Событие InfoMessage (ADO)
TOCTitle: InfoMessage Event (ADO)
ms:assetid: 5d4f487f-96c8-4cf6-60ab-583510d3096f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249328(v=office.15)
ms:contentKeyID: 48545109
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 35e3962ed16415cf2d1ef2f470071a00185749bc
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875303"
---
# <a name="infomessage-event-ado"></a>Событие InfoMessage (ADO)


**Применимо к**: Access 2013, Office 2013

При появлении предупреждения в процессе выполнения операции **ConnectionEvent** вызывает события **InfoMessage** .

## <a name="syntax"></a>Синтаксис

InfoMessage*pError*, *adStatus* *pConnection*

## <a name="parameters"></a>Параметры

  - *pError*

  - Объект [Error](error-object-ado.md) . Этот параметр содержит все ошибки, которые возвращаются. Если возвращаются несколько ошибок, перечисление семейство **Errors** их поиск.

  - *adStatus*

  - [EventStatusEnum](eventstatusenum.md)
    
    Прежде чем возвращает это событие, присвойте этому параметру значение **adStatusUnwantedEvent** , чтобы запретить последующие уведомления.

  - *pConnection*

  - Объект [подключения](connection-object-ado.md) . Подключение, для которого произошло предупреждение. К примеру, можно предупреждений при открытии **подключения** объекта или выполнения [команды](command-object-ado.md) для **подключения**.

