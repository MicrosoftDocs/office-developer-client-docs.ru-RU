---
title: onError события (RDS)
TOCTitle: onError Event (RDS)
ms:assetid: e26a3f7f-0f00-919a-65ad-bf39ffb83e92
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250153(v=office.15)
ms:contentKeyID: 48548292
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 17cbeece67ffa19666f6209a38159c9a2c6a44ea
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889947"
---
# <a name="onerror-event-rds"></a>onError события (RDS)


**Применимо к**: Access 2013, Office 2013

События **onError** вызывается каждый раз, когда возникает ошибка во время выполнения операции.

## <a name="syntax"></a>Синтаксис

onError*SCode* *Описание* *источника* *CancelDisplay*

## <a name="parameters"></a>Параметры

  - *SCode*

  - Целое число, указывающее код состояния ошибки.

  - *Описание*

  - **Строка** , указывающая описание ошибки.

  - *Source*

  - **Строка** , указывающая запроса или команды, вызвавшей ошибку.

  - *CancelDisplay*

  - **Логическое** значение, которая, в случае присвоено **значение True**, который запрещает отображение в диалоговом окне ошибки.

