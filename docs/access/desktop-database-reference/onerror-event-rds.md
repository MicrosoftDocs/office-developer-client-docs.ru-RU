---
title: onError event (RDS)
TOCTitle: onError event (RDS)
ms:assetid: e26a3f7f-0f00-919a-65ad-bf39ffb83e92
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250153(v=office.15)
ms:contentKeyID: 48548292
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9fc51522d143306d9625cdc07251edfe1dddf22d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288478"
---
# <a name="onerror-event-rds"></a>onError event (RDS)

**Область применения**: Access 2013, Office 2013

Событие **onError** называется всякий раз, когда во время операции возникает ошибка.

## <a name="syntax"></a>Синтаксис

onError *SCode*, *Описание*, *Источник*, *CancelDisplay*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*SCode* |Integer, который указывает код состояния ошибки.|
|*Описание* |**Строка,** которая указывает описание ошибки.|
|*Source* |**Строка,** которая указывает запрос или команду, которая вызвала ошибку.|
|*CancelDisplay* |Значение **Boolean,** которое, если **задано значение True,** предотвращает отображение ошибки в диалоговом окне.|

