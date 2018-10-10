---
title: TRANSACTION Statement (Microsoft Access SQL)
TOCTitle: TRANSACTION Statement (Microsoft Access SQL)
ms:assetid: 481e807d-94e4-f201-adac-d25ee89d9220
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193241(v=office.15)
ms:contentKeyID: 48544614
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277472
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 13628ee6d384430691475eb06dbbbdce4e980103
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481561"
---
# <a name="transaction-statement-microsoft-access-sql"></a>TRANSACTION Statement (Microsoft Access SQL)


**Применимо к**: Access 2013 | Office 2013

Используется для начинать и завершать явные операции.

## <a name="syntax"></a>Синтаксис

Начать новую операцию.

НАЧАТЬ ТРАНЗАКЦИЮ

Завершение операции с возвращением действия выполняются во время операции.

ФИКСАЦИЯ \[ТРАНЗАКЦИЙ | РАБОТА\]

Завершение операции с откат всех выполненной во время операции.

ОТКАТ \[ТРАНЗАКЦИЙ | РАБОТА\]

## <a name="remarks"></a>Замечания

Не удалось автоматически запустить транзакции. Чтобы запустить операцию, необходимо выполнить явно использовать команду НАЧАТЬ ТРАНЗАКЦИЙ.

Операции могут быть вложенными до пяти уровней вложенности. Чтобы начать вложенных транзакций, используйте приступить к ТРАНЗАКЦИЙ в контексте существующей транзакции.

Транзакции не поддерживаются для связанных таблиц.

