---
title: Событие onError (RDS)
TOCTitle: onError event (RDS)
ms:assetid: e26a3f7f-0f00-919a-65ad-bf39ffb83e92
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250153(v=office.15)
ms:contentKeyID: 48548292
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9fc51522d143306d9625cdc07251edfe1dddf22d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712178"
---
# <a name="onerror-event-rds"></a>Событие onError (RDS)

**Применимо к**: Access 2013, Office 2013

События **onError** вызывается каждый раз, когда возникает ошибка во время выполнения операции.

## <a name="syntax"></a>Синтаксис

onError*SCode* *Описание* *источника* *CancelDisplay*

## <a name="parameters"></a>Parameters

|Параметр|Описание|
|:--------|:----------|
|*SCode* |Целое число, указывающее код состояния ошибки.|
|*Описание* |**Строка** , указывающая описание ошибки.|
|*Source* |**Строка** , указывающая запроса или команды, вызвавшей ошибку.|
|*CancelDisplay* |**Логическое** значение, которая, в случае присвоено **значение True**, который запрещает отображение в диалоговом окне ошибки.|

