---
title: Члены workspaces (DAO)
TOCTitle: Workspaces Members
ms:assetid: 5eaf6de5-44dc-5566-a98f-db54aecf15cb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194667(v=office.15)
ms:contentKeyID: 48545141
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6be2aba5ab072e40193aff11ab6be54ba6c94f34
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302606"
---
# <a name="workspaces-members-dao"></a><span data-ttu-id="c5516-102">Члены workspaces (DAO)</span><span class="sxs-lookup"><span data-stu-id="c5516-102">Workspaces members (DAO)</span></span>


<span data-ttu-id="c5516-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c5516-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c5516-104">Коллекция Workspaces содержит все активные незагруженные объекты Workspace объекта DBEngine.</span><span class="sxs-lookup"><span data-stu-id="c5516-104">A Workspaces collection contains all active, unhidden Workspace objects of the DBEngine object.</span></span> <span data-ttu-id="c5516-105">(Объекты Скрытой рабочей области не примеся к коллекции и не ссылаются на них переменной, которой они назначены.)</span><span class="sxs-lookup"><span data-stu-id="c5516-105">(Hidden Workspace objects are not appended to the collection and referenced by the variable to which they are assigned.)</span></span>

## <a name="methods"></a><span data-ttu-id="c5516-106">Методы</span><span class="sxs-lookup"><span data-stu-id="c5516-106">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c5516-107">Имя</span><span class="sxs-lookup"><span data-stu-id="c5516-107">Name</span></span></p></th>
<th><p><span data-ttu-id="c5516-108">Описание</span><span class="sxs-lookup"><span data-stu-id="c5516-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c5516-109"><strong><a href="workspaces-append-method-dao.md">Append</a></strong></span><span class="sxs-lookup"><span data-stu-id="c5516-109"><strong><a href="workspaces-append-method-dao.md">Append</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c5516-110">Добавляет новую <strong>область workspace</strong> в <strong>коллекцию Workspaces.</strong></span><span class="sxs-lookup"><span data-stu-id="c5516-110">Adds a new <strong>Workspace</strong> to the <strong>Workspaces</strong> collection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5516-111"><strong><a href="workspaces-delete-method-dao.md">Delete</a></strong></span><span class="sxs-lookup"><span data-stu-id="c5516-111"><strong><a href="workspaces-delete-method-dao.md">Delete</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c5516-112">Удаляет указанную форму <strong>рабочей</strong> области для <strong>коллекции Workspaces.</strong></span><span class="sxs-lookup"><span data-stu-id="c5516-112">Deletes the specified <strong>Workspace</strong> form the <strong>Workspaces</strong> collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5516-113"><strong><a href="workspaces-refresh-method-dao.md">Refresh</a></strong></span><span class="sxs-lookup"><span data-stu-id="c5516-113"><strong><a href="workspaces-refresh-method-dao.md">Refresh</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c5516-114">Не поддерживается для объекта.</span><span class="sxs-lookup"><span data-stu-id="c5516-114">Not supported for this object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="c5516-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="c5516-115">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c5516-116">Имя</span><span class="sxs-lookup"><span data-stu-id="c5516-116">Name</span></span></p></th>
<th><p><span data-ttu-id="c5516-117">Описание</span><span class="sxs-lookup"><span data-stu-id="c5516-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c5516-118"><strong><a href="workspaces-count-property-dao.md">Count</a></strong></span><span class="sxs-lookup"><span data-stu-id="c5516-118"><strong><a href="workspaces-count-property-dao.md">Count</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c5516-119">Возвращает количество объектов в указанной коллекции.</span><span class="sxs-lookup"><span data-stu-id="c5516-119">Returns the number of objects in the specified collection.</span></span> <span data-ttu-id="c5516-120">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="c5516-120">Read-only.</span></span></p></td>
</tr>
</tbody>
</table>

