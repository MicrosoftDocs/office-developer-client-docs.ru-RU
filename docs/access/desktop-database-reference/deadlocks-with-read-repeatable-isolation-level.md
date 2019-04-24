---
title: ВзаимоБлокировки с уровнем изоляции с повторяемым чтением
TOCTitle: Deadlocks with read repeatable isolation level
ms:assetid: 3d5f3293-33bb-cf6d-362a-278f9ec1bd3c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249165(v=office.15)
ms:contentKeyID: 48544342
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5c3e38f6054e6548dfc14d30ce6ec89dcb2e4b01
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294178"
---
# <a name="deadlocks-with-read-repeatable-isolation-level"></a><span data-ttu-id="b1f35-102">ВзаимоБлокировки с уровнем изоляции с повторяемым чтением</span><span class="sxs-lookup"><span data-stu-id="b1f35-102">Deadlocks with read repeatable isolation level</span></span>


<span data-ttu-id="b1f35-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b1f35-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b1f35-104">Если настраиваемый бизнес-объект использует уровень изоляции чтения повторяемых элементов для доступа к SQL Server, а бизнес-объект вызывается одновременно двумя клиентами, которые отправляют запрос и обновляет одну транзакцию, возможна взаимоблокировка.</span><span class="sxs-lookup"><span data-stu-id="b1f35-104">If a custom business object uses an isolation level of read repeatable to access a SQL Server, and the business object is called simultaneously by two clients that send a query and update in the same transaction, a deadlock is possible.</span></span> <span data-ttu-id="b1f35-105">Служба удаленных данных предназначена для того, чтобы один из процессов мог испустить блокировку, но при этом обновление для этого клиента завершится с ошибками.</span><span class="sxs-lookup"><span data-stu-id="b1f35-105">Remote Data Service is designed to allow one of the processes to time out to release the deadlock, but the update will fail for that client.</span></span>

<span data-ttu-id="b1f35-106">Используйте динамическое свойство**время ожидания команды** [службы курсора](microsoft-cursor-service-for-ole-db-ado-service-component.md), чтобы изменить продолжительность периода ожидания.</span><span class="sxs-lookup"><span data-stu-id="b1f35-106">Use the [Cursor Service](microsoft-cursor-service-for-ole-db-ado-service-component.md)**Command Time Out** dynamic property to modify the length of the timeout.</span></span>

