---
title: событие OnError (RDS)
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
# <a name="onerror-event-rds"></a>событие OnError (RDS)

**Область применения**: Access 2013, Office 2013

Событие **OnError** вызывается при возникновении ошибки во время выполнения операции.

## <a name="syntax"></a>Синтаксис

OnError*SCode*, *Description*, *Source*, *canceldisplay AS*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*SCode* |Целое число, указывающее код состояния ошибки.|
|*Описание* |**Строка** , указывающая описание ошибки.|
|*Source* |**Строка** , указывающая на запрос или команду, которая вызвала ошибку.|
|*Canceldisplay AS* |**Логическое** значение, при котором задано значение **true**, которое предотвращает отображение ошибки в диалоговом окне.|

