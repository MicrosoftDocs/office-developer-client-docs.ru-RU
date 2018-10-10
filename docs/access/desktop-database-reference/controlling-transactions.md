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
# <a name="controlling-transactions"></a><span data-ttu-id="ffcae-102">Controlling Transactions</span><span class="sxs-lookup"><span data-stu-id="ffcae-102">Controlling Transactions</span></span>


<span data-ttu-id="ffcae-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ffcae-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ffcae-104">*Транзакций* отделяет начала и окончания последовательность операций доступа к данным, которые пройти через подключение.</span><span class="sxs-lookup"><span data-stu-id="ffcae-104">A *transaction* delimits the beginning and end of a series of data access operations that transpire across a connection.</span></span> <span data-ttu-id="ffcae-105">Может быть возможности транзакций источника данных объект **подключения** можно создавать и управлять ими транзакции.</span><span class="sxs-lookup"><span data-stu-id="ffcae-105">Subject to the transactional capabilities of your data source, the **Connection** object also allows you to create and manage transactions.</span></span> <span data-ttu-id="ffcae-106">Например для доступа к базе данных Microsoft SQL Server 2000 используется поставщик Microsoft OLE DB для SQL Server, можно создать несколько вложенных транзакций для команды, которые можно выполнить.</span><span class="sxs-lookup"><span data-stu-id="ffcae-106">For example, using the Microsoft OLE DB Provider for SQL Server to access a database on Microsoft SQL Server 2000, you can create multiple nested transactions for the commands you execute.</span></span>

<span data-ttu-id="ffcae-107">ADO гарантирует, что успешно друг с другом или вообще не внесены изменения источника данных, в результате операций в транзакции.</span><span class="sxs-lookup"><span data-stu-id="ffcae-107">ADO ensures that changes to a data source resulting from operations in a transaction occur successfully together or not at all.</span></span>

<span data-ttu-id="ffcae-108">При отмене операции или один из его операции происходит сбой, ultimate результатом будет как если бы ни одна из этих операций в транзакции произошло.</span><span class="sxs-lookup"><span data-stu-id="ffcae-108">If you cancel the transaction, or if one of its operations fails, the ultimate result will be as if none of the operations in the transaction occurred.</span></span> <span data-ttu-id="ffcae-109">Источник данных остается, которая была до начала транзакции.</span><span class="sxs-lookup"><span data-stu-id="ffcae-109">The data source will remain as it was before the transaction began.</span></span>

<span data-ttu-id="ffcae-110">Объектная модель ADO явно не содержит транзакции, но их представляет набор методов объекта **подключения** (**BeginTrans** **CommitTrans**и **RollbackTrans**).</span><span class="sxs-lookup"><span data-stu-id="ffcae-110">The ADO object model does not explicitly include transactions, but represents them with a set of **Connection** object methods (**BeginTrans**, **CommitTrans**, and **RollbackTrans**).</span></span>

<span data-ttu-id="ffcae-111">Дополнительные сведения о транзакциях можно [Глава 5: обновления и сохранение данных](chapter-5-updating-and-persisting-data.md).</span><span class="sxs-lookup"><span data-stu-id="ffcae-111">For more information about transactions, see [Chapter 5: Updating and Persisting Data](chapter-5-updating-and-persisting-data.md).</span></span>

