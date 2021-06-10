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
# <a name="controlling-transactions"></a><span data-ttu-id="c86fe-102">Controlling Transactions</span><span class="sxs-lookup"><span data-stu-id="c86fe-102">Controlling Transactions</span></span>


<span data-ttu-id="c86fe-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c86fe-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c86fe-104">*Транзакция* делимитация начала и окончания серии операций доступа к данным, которые транспирация через подключение.</span><span class="sxs-lookup"><span data-stu-id="c86fe-104">A *transaction* delimits the beginning and end of a series of data access operations that transpire across a connection.</span></span> <span data-ttu-id="c86fe-105">С учетом возможностей транзакций источника данных объект **Connection** также позволяет создавать и управлять транзакциями.</span><span class="sxs-lookup"><span data-stu-id="c86fe-105">Subject to the transactional capabilities of your data source, the **Connection** object also allows you to create and manage transactions.</span></span> <span data-ttu-id="c86fe-106">Например, с помощью поставщика DB Microsoft OLE для SQL Server доступа к базе данных Microsoft SQL Server 2000 г. можно создать несколько вложенных транзакций для выполняемых команд.</span><span class="sxs-lookup"><span data-stu-id="c86fe-106">For example, using the Microsoft OLE DB Provider for SQL Server to access a database on Microsoft SQL Server 2000, you can create multiple nested transactions for the commands you execute.</span></span>

<span data-ttu-id="c86fe-107">ADO гарантирует, что изменения источника данных в результате операций в транзакции успешно происходят вместе или вообще не происходят.</span><span class="sxs-lookup"><span data-stu-id="c86fe-107">ADO ensures that changes to a data source resulting from operations in a transaction occur successfully together or not at all.</span></span>

<span data-ttu-id="c86fe-108">Если вы отмените транзакцию или одна из ее операций не состоится, конечным результатом будет то, что ни одна из операций в транзакции не была совершена.</span><span class="sxs-lookup"><span data-stu-id="c86fe-108">If you cancel the transaction, or if one of its operations fails, the ultimate result will be as if none of the operations in the transaction occurred.</span></span> <span data-ttu-id="c86fe-109">Источник данных останется таким же, как и до начала транзакции.</span><span class="sxs-lookup"><span data-stu-id="c86fe-109">The data source will remain as it was before the transaction began.</span></span>

<span data-ttu-id="c86fe-110">Объектная модель ADO явно не включает транзакции, но представляет  их с набором методов объекта подключения **(BeginTrans,** **CommitTrans** и **RollbackTrans).**</span><span class="sxs-lookup"><span data-stu-id="c86fe-110">The ADO object model does not explicitly include transactions, but represents them with a set of **Connection** object methods (**BeginTrans**, **CommitTrans**, and **RollbackTrans**).</span></span>

<span data-ttu-id="c86fe-111">Дополнительные сведения о транзакциях см. [в главе 5: Обновление и сохраняющиеся данные.](chapter-5-updating-and-persisting-data.md)</span><span class="sxs-lookup"><span data-stu-id="c86fe-111">For more information about transactions, see [Chapter 5: Updating and Persisting Data](chapter-5-updating-and-persisting-data.md).</span></span>

