---
title: Оператор ТРАНЗАКЦИЙ (Microsoft Access SQL)
TOCTitle: TRANSACTION statement (Microsoft Access SQL)
ms:assetid: 481e807d-94e4-f201-adac-d25ee89d9220
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193241(v=office.15)
ms:contentKeyID: 48544614
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277472
f1_categories:
- Office.Version=v15
ms.openlocfilehash: f48b1ab98f6f0f729fdb32b4ff20be09c5d942bf
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886391"
---
# <a name="transaction-statement-microsoft-access-sql"></a>Оператор ТРАНЗАКЦИЙ (Microsoft Access SQL)

**Применимо к**: Access 2013, Office 2013

Используется для начинать и завершать явные операции.

## <a name="syntax"></a>Синтаксис

**Начало новой операции**:

НАЧАТЬ ТРАНЗАКЦИЮ

**Conclude транзакций с внесением всех рабочих выполнена во время операции**:

ФИКСАЦИЯ \[ТРАНЗАКЦИЙ | РАБОТА\]

**Conclude транзакций с помощью отката все действия выполняются во время операции**:

ОТКАТ \[ТРАНЗАКЦИЙ | РАБОТА\]

## <a name="remarks"></a>Замечания

Не удалось автоматически запустить транзакции. Чтобы запустить операцию, необходимо выполнить явно использовать команду НАЧАТЬ ТРАНЗАКЦИЙ.

Операции могут быть вложенными до пяти уровней вложенности. Чтобы начать вложенных транзакций, используйте приступить к ТРАНЗАКЦИЙ в контексте существующей транзакции.

Транзакции не поддерживаются для связанных таблиц.

