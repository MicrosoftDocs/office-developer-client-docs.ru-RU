---
title: Controlling Transactions
TOCTitle: Controlling Transactions
ms:assetid: 21a9f055-6907-3818-e232-21e579cc67b7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248994(v=office.15)
ms:contentKeyID: 48543685
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b70e6586e17286f4f7a13417d0901f1250635631
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482972"
---
# <a name="controlling-transactions"></a>Controlling Transactions


**Применимо к**: Access 2013 | Office 2013

*Транзакций* отделяет начала и окончания последовательность операций доступа к данным, которые пройти через подключение. Может быть возможности транзакций источника данных объект **подключения** можно создавать и управлять ими транзакции. Например для доступа к базе данных Microsoft SQL Server 2000 используется поставщик Microsoft OLE DB для SQL Server, можно создать несколько вложенных транзакций для команды, которые можно выполнить.

ADO гарантирует, что успешно друг с другом или вообще не внесены изменения источника данных, в результате операций в транзакции.

При отмене операции или один из его операции происходит сбой, ultimate результатом будет как если бы ни одна из этих операций в транзакции произошло. Источник данных остается, которая была до начала транзакции.

Объектная модель ADO явно не содержит транзакции, но их представляет набор методов объекта **подключения** (**BeginTrans** **CommitTrans**и **RollbackTrans**).

Дополнительные сведения о транзакциях можно [Глава 5: обновления и сохранение данных](chapter-5-updating-and-persisting-data.md).

