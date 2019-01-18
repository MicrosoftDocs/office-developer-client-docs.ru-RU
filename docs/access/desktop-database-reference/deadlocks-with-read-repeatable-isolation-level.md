---
title: Взаимоблокировок с уровнем изоляции чтения повторяющихся
TOCTitle: Deadlocks with read repeatable isolation level
ms:assetid: 3d5f3293-33bb-cf6d-362a-278f9ec1bd3c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249165(v=office.15)
ms:contentKeyID: 48544342
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5c3e38f6054e6548dfc14d30ce6ec89dcb2e4b01
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703778"
---
# <a name="deadlocks-with-read-repeatable-isolation-level"></a><span data-ttu-id="84237-102">Взаимоблокировок с уровнем изоляции чтения повторяющихся</span><span class="sxs-lookup"><span data-stu-id="84237-102">Deadlocks with read repeatable isolation level</span></span>


<span data-ttu-id="84237-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="84237-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="84237-104">Если настраиваемый бизнес-объект использует уровень изоляции чтения повторяющихся для доступа к SQL Server и бизнес-объект вызывается одновременно с двумя клиентами, отправьте запрос и обновление в той же транзакции, возможна взаимоблокировка.</span><span class="sxs-lookup"><span data-stu-id="84237-104">If a custom business object uses an isolation level of read repeatable to access a SQL Server, and the business object is called simultaneously by two clients that send a query and update in the same transaction, a deadlock is possible.</span></span> <span data-ttu-id="84237-105">Служба удаленных данных позволяет один процессы, используемые для времени ожидания для освобождения взаимоблокировки, но обновление завершится с ошибкой для этого клиента.</span><span class="sxs-lookup"><span data-stu-id="84237-105">Remote Data Service is designed to allow one of the processes to time out to release the deadlock, but the update will fail for that client.</span></span>

<span data-ttu-id="84237-106">Используйте свойство динамических**время ожидания команды** [Службы курсора](microsoft-cursor-service-for-ole-db-ado-service-component.md)для изменения продолжительность периода ожидания.</span><span class="sxs-lookup"><span data-stu-id="84237-106">Use the [Cursor Service](microsoft-cursor-service-for-ole-db-ado-service-component.md)**Command Time Out** dynamic property to modify the length of the timeout.</span></span>

