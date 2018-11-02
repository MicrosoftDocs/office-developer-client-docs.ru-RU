---
title: Событие onError (RDS)
TOCTitle: onError event (RDS)
ms:assetid: e26a3f7f-0f00-919a-65ad-bf39ffb83e92
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250153(v=office.15)
ms:contentKeyID: 48548292
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c67e277c35e3cf6c75226dc138aa4b288843e6bf
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930863"
---
# <a name="onerror-event-rds"></a>Событие onError (RDS)


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

