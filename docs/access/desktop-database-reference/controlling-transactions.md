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

*Транзакция* отделяет начало и конец ряда операций доступа к данным, выполняемых через подключение. В соответствии с возможностями транзакционного источника данных, объект **Connection** также позволяет создавать транзакции и управлять ими. Например, используя поставщик Microsoft OLE DB для SQL Server для доступа к базе данных в Microsoft SQL Server 2000, можно создать несколько вложенных транзакций для выполняемых команд.

ADO гарантирует, что изменения источника данных, получаемые в результате операций в транзакции, выполняются успешно или вообще не выполняются.

При отмене транзакции или при сбое одной из ее операций конечный результат будет таким же, как если бы ни выполнялась операция в транзакции. Источник данных останется в том виде, в котором он находился до начала транзакции.

Объектная модель ADO явно не включает транзакции, но представляет их с помощью набора методов объекта **подключения** (**BeginTrans**, **CommitTrans**и **RollbackTrans**).

Дополнительные сведения о транзакциях приведены в [главе 5: обновление и постоянное использование данных](chapter-5-updating-and-persisting-data.md).

