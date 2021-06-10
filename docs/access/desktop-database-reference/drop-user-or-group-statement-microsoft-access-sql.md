---
title: DROP USER или GROUP statement (Microsoft Access SQL)
TOCTitle: DROP USER or GROUP statement (Microsoft Access SQL)
ms:assetid: 46bc5916-556b-17df-2f4c-8fd7bbd21ef7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193192(v=office.15)
ms:contentKeyID: 48544575
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 995f935ceea5af3b740215c5a4137e02e7ebb1b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293646"
---
# <a name="drop-user-or-group-statement-microsoft-access-sql"></a><span data-ttu-id="f7def-102">DROP USER или GROUP statement (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="f7def-102">DROP USER or GROUP statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="f7def-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f7def-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f7def-104">Удаляет одного или несколько существующих пользователей *или* *групп* или удаляет одного или несколько существующих пользователей *из* существующей *группы.*</span><span class="sxs-lookup"><span data-stu-id="f7def-104">Deletes one or more existing *users* or *groups*, or removes one or more existing *users* from an existing *group*.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7def-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f7def-105">Syntax</span></span>

### <a name="delete-one-or-more-users-or-remove-one-or-more-users-from-a-group"></a><span data-ttu-id="f7def-106">Удаление одного или более пользователей или удаление одного или более пользователей из группы</span><span class="sxs-lookup"><span data-stu-id="f7def-106">Delete one or more users or remove one or more users from a group</span></span>

<span data-ttu-id="f7def-107">DROP *USER user,* \[ *user*, ... \] \[ FROM *group*\]</span><span class="sxs-lookup"><span data-stu-id="f7def-107">DROP USER *user*\[, *user*, …\] \[FROM *group*\]</span></span>

### <a name="delete-one-or-more-groups"></a><span data-ttu-id="f7def-108">Удаление одной или более групп</span><span class="sxs-lookup"><span data-stu-id="f7def-108">Delete one or more groups</span></span>

<span data-ttu-id="f7def-109">ГРУППА  \[ DROP, *группа*, ...\]</span><span class="sxs-lookup"><span data-stu-id="f7def-109">DROP GROUP *group*\[, *group*, …\]</span></span>

<span data-ttu-id="f7def-110">В заявлении DROP USER или GROUP есть такие части:</span><span class="sxs-lookup"><span data-stu-id="f7def-110">The DROP USER or GROUP statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f7def-111">Part</span><span class="sxs-lookup"><span data-stu-id="f7def-111">Part</span></span></p></th>
<th><p><span data-ttu-id="f7def-112">Описание</span><span class="sxs-lookup"><span data-stu-id="f7def-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f7def-113"><em>user</em></span><span class="sxs-lookup"><span data-stu-id="f7def-113"><em>user</em></span></span></p></td>
<td><p><span data-ttu-id="f7def-114">Имя пользователя, удаляемого из информационного файла группы.</span><span class="sxs-lookup"><span data-stu-id="f7def-114">The name of a user to be removed from the workgroup information file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f7def-115"><em>group</em></span><span class="sxs-lookup"><span data-stu-id="f7def-115"><em>group</em></span></span></p></td>
<td><p><span data-ttu-id="f7def-116">Имя группы, удаляемой из информационного файла рабочей группы.</span><span class="sxs-lookup"><span data-stu-id="f7def-116">The name of a group to be removed from the workgroup information file.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="f7def-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="f7def-117">Remarks</span></span>

<span data-ttu-id="f7def-118">Если ключевое слово FROM используется в заявлении  DROP USER, каждый из  пользователей, перечисленных в заявлении, будет удален из группы, указанной по ключевому слову FROM.</span><span class="sxs-lookup"><span data-stu-id="f7def-118">If the FROM keyword is used in the DROP USER statement, each of the *users* listed in the statement will be removed from the *group* specified following the FROM keyword.</span></span> <span data-ttu-id="f7def-119">Однако сами *пользователи* не будут удалены.</span><span class="sxs-lookup"><span data-stu-id="f7def-119">However, the *users* themselves will not be deleted.</span></span>

<span data-ttu-id="f7def-120">В заявлении DROP GROUP будет удалена *указанная группа*(s).</span><span class="sxs-lookup"><span data-stu-id="f7def-120">The DROP GROUP statement will delete the specified *group*(s).</span></span> <span data-ttu-id="f7def-121">Пользователи, которые являются членами группы *(s),* не будут затронуты, но они больше не будут членами *удаленных* групп (s). </span><span class="sxs-lookup"><span data-stu-id="f7def-121">The *users* who are members of the *group*(s) will not be affected, but they will no longer be members of the deleted *group*(s).</span></span>

