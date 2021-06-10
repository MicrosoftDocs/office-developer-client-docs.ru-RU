---
title: Controlling Transactions
TOCTitle: Controlling Transactions
ms:assetid: 21a9f055-6907-3818-e232-21e579cc67b7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248994(v=office.15)
ms:contentKeyID: 48543685
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ced1ae7b32d25fbae53c670959a4a6c77bcea0be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295550"
---
# <a name="controlling-transactions"></a>Controlling Transactions


**Область применения**: Access 2013, Office 2013

*Транзакция* делимитация начала и окончания серии операций доступа к данным, которые транспирация через подключение. С учетом возможностей транзакций источника данных объект **Connection** также позволяет создавать и управлять транзакциями. Например, с помощью поставщика DB Microsoft OLE для SQL Server доступа к базе данных Microsoft SQL Server 2000 г. можно создать несколько вложенных транзакций для выполняемых команд.

ADO гарантирует, что изменения источника данных в результате операций в транзакции успешно происходят вместе или вообще не происходят.

Если вы отмените транзакцию или одна из ее операций не состоится, конечным результатом будет то, что ни одна из операций в транзакции не была совершена. Источник данных останется таким же, как и до начала транзакции.

Объектная модель ADO явно не включает транзакции, но представляет  их с набором методов объекта подключения **(BeginTrans,** **CommitTrans** и **RollbackTrans).**

Дополнительные сведения о транзакциях см. [в главе 5: Обновление и сохраняющиеся данные.](chapter-5-updating-and-persisting-data.md)

