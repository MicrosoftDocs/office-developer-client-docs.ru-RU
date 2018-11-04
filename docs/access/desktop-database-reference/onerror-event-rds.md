---
title: Событие onError (RDS)
TOCTitle: onError event (RDS)
ms:assetid: e26a3f7f-0f00-919a-65ad-bf39ffb83e92
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250153(v=office.15)
ms:contentKeyID: 48548292
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a61ec584f5baddcfdb8ce1f6dda1bf990546c053
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949357"
---
# <a name="onerror-event-rds"></a>Событие onError (RDS)

**Применимо к**: Access 2013, Office 2013

События **onError** вызывается каждый раз, когда возникает ошибка во время выполнения операции.

## <a name="syntax"></a>Синтаксис

onError*SCode* *Описание* *источника* *CancelDisplay*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*SCode* |Целое число, указывающее код состояния ошибки.|
|*Описание* |**Строка** , указывающая описание ошибки.|
|*Source* |**Строка** , указывающая запроса или команды, вызвавшей ошибку.|
|*CancelDisplay* |**Логическое** значение, которая, в случае присвоено **значение True**, который запрещает отображение в диалоговом окне ошибки.|

