---
title: Рабочие области члены (DAO)
TOCTitle: Workspaces Members
ms:assetid: 5eaf6de5-44dc-5566-a98f-db54aecf15cb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194667(v=office.15)
ms:contentKeyID: 48545141
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1718861237e59761c337c504508c60348df2b611
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923149"
---
# <a name="workspaces-members-dao"></a><span data-ttu-id="9a4f1-102">Рабочие области члены (DAO)</span><span class="sxs-lookup"><span data-stu-id="9a4f1-102">Workspaces members (DAO)</span></span>


<span data-ttu-id="9a4f1-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9a4f1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9a4f1-104">Рабочие области для семейства содержит все активные, Показать объекты рабочей области для объекта DBEngine.</span><span class="sxs-lookup"><span data-stu-id="9a4f1-104">A Workspaces collection contains all active, unhidden Workspace objects of the DBEngine object.</span></span> <span data-ttu-id="9a4f1-105">(Скрытые рабочей области объекты не добавляется в конец коллекции и ссылается переменная, к которому они назначены.)</span><span class="sxs-lookup"><span data-stu-id="9a4f1-105">(Hidden Workspace objects are not appended to the collection and referenced by the variable to which they are assigned.)</span></span>

## <a name="methods"></a><span data-ttu-id="9a4f1-106">Методы</span><span class="sxs-lookup"><span data-stu-id="9a4f1-106">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9a4f1-107">Имя</span><span class="sxs-lookup"><span data-stu-id="9a4f1-107">Name</span></span></p></th>
<th><p><span data-ttu-id="9a4f1-108">Описание</span><span class="sxs-lookup"><span data-stu-id="9a4f1-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9a4f1-109"><strong><a href="workspaces-append-method-dao.md">Добавление</a></strong></span><span class="sxs-lookup"><span data-stu-id="9a4f1-109"><strong><a href="workspaces-append-method-dao.md">Append</a></strong></span></span></p></td>
<td><p><span data-ttu-id="9a4f1-110">Добавление новой <strong>рабочей области для</strong> семейства сайтов <strong>рабочих областей</strong> .</span><span class="sxs-lookup"><span data-stu-id="9a4f1-110">Adds a new <strong>Workspace</strong> to the <strong>Workspaces</strong> collection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a4f1-111"><strong><a href="workspaces-delete-method-dao.md">Delete</a></strong></span><span class="sxs-lookup"><span data-stu-id="9a4f1-111"><strong><a href="workspaces-delete-method-dao.md">Delete</a></strong></span></span></p></td>
<td><p><span data-ttu-id="9a4f1-112">Удаляет указанную форму <strong>рабочей области для</strong> семейства сайтов <strong>рабочих областей</strong> .</span><span class="sxs-lookup"><span data-stu-id="9a4f1-112">Deletes the specified <strong>Workspace</strong> form the <strong>Workspaces</strong> collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a4f1-113"><strong><a href="workspaces-refresh-method-dao.md">Обновление</a></strong></span><span class="sxs-lookup"><span data-stu-id="9a4f1-113"><strong><a href="workspaces-refresh-method-dao.md">Refresh</a></strong></span></span></p></td>
<td><p><span data-ttu-id="9a4f1-114">Не поддерживается для этого объекта.</span><span class="sxs-lookup"><span data-stu-id="9a4f1-114">Not supported for this object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="9a4f1-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="9a4f1-115">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9a4f1-116">Имя</span><span class="sxs-lookup"><span data-stu-id="9a4f1-116">Name</span></span></p></th>
<th><p><span data-ttu-id="9a4f1-117">Описание</span><span class="sxs-lookup"><span data-stu-id="9a4f1-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9a4f1-118"><strong><a href="workspaces-count-property-dao.md">Count</a></strong></span><span class="sxs-lookup"><span data-stu-id="9a4f1-118"><strong><a href="workspaces-count-property-dao.md">Count</a></strong></span></span></p></td>
<td><p><span data-ttu-id="9a4f1-119">Возвращает число объектов в указанном семействе сайтов.</span><span class="sxs-lookup"><span data-stu-id="9a4f1-119">Returns the number of objects in the specified collection.</span></span> <span data-ttu-id="9a4f1-120">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="9a4f1-120">Read-only.</span></span></p></td>
</tr>
</tbody>
</table>

