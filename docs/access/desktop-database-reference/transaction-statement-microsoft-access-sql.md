---
title: Инструкция TRANSACTION (Microsoft Access SQL)
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
localization_priority: Priority
ms.openlocfilehash: 828bccfad83320d27f9473d532ab86f73b2fde98
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314149"
---
# <a name="transaction-statement-microsoft-access-sql"></a>Инструкция TRANSACTION (Microsoft Access SQL)

**Область применения**: Access 2013, Office 2013

Позволяет начинать и завершать явные транзакции.

## <a name="syntax"></a>Синтаксис

**Начало новой транзакции**:

BEGIN TRANSACTION

**Завершение транзакции с возвращением результата, полученного во время нее**:

COMMIT \[TRANSACTION | WORK\]

**Завершение транзакции с отменой всех действий, выполненных во время нее**:

ROLLBACK \[TRANSACTION | WORK\]

## <a name="remarks"></a>Примечания

Транзакции не запускаются автоматически. Чтобы запустить транзакцию, необходимо явно использовать команду BEGIN TRANSACTION.

У транзакций может быть до пяти уровней вложенности. Чтобы запустить вложенную транзакцию, используйте команду BEGIN TRANSACTION внутри существующей транзакции.

Транзакции не поддерживаются в связанных таблицах.

