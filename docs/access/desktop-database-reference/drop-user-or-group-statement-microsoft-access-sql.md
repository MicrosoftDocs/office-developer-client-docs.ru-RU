---
title: DROP USER or GROUP Statement (Microsoft Access SQL)
TOCTitle: DROP USER or GROUP Statement (Microsoft Access SQL)
ms:assetid: 46bc5916-556b-17df-2f4c-8fd7bbd21ef7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193192(v=office.15)
ms:contentKeyID: 48544575
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3a5cf75de06c13e2452e5f33b8355b7fb480d8a3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480287"
---
# <a name="drop-user-or-group-statement-microsoft-access-sql"></a><span data-ttu-id="19f2e-102">DROP USER or GROUP Statement (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="19f2e-102">DROP USER or GROUP Statement (Microsoft Access SQL)</span></span>


<span data-ttu-id="19f2e-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="19f2e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="19f2e-104">Удаляет один или несколько существующего *пользователя*или *группы*, или удаляет существующие s *пользователей*из существующей *группы*.</span><span class="sxs-lookup"><span data-stu-id="19f2e-104">Deletes one or more existing *user*s or *group*s, or removes one or more existing *user*s from an existing *group*.</span></span>

## <a name="syntax"></a><span data-ttu-id="19f2e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="19f2e-105">Syntax</span></span>

<span data-ttu-id="19f2e-106">Удаление одного или нескольких *пользователей*s или удалить один или несколько s *пользователя*из *группы*:</span><span class="sxs-lookup"><span data-stu-id="19f2e-106">Delete one or more *user*s or remove one or more *user*s from a *group*:</span></span>

<span data-ttu-id="19f2e-107">Удаление пользователя *пользователя*\[, *пользователь*... \] \[Из *группы*\]</span><span class="sxs-lookup"><span data-stu-id="19f2e-107">DROP USER *user*\[, *user*, …\] \[FROM *group*\]</span></span>

<span data-ttu-id="19f2e-108">Удаление одного или нескольких s: *группы*</span><span class="sxs-lookup"><span data-stu-id="19f2e-108">Delete one or more *group*s:</span></span>

<span data-ttu-id="19f2e-109">ГРУППА РАЗМЕЩЕНИЯ *группы*\[, *Группа*...\]</span><span class="sxs-lookup"><span data-stu-id="19f2e-109">DROP GROUP *group*\[, *group*, …\]</span></span>

<span data-ttu-id="19f2e-110">Оператор удаление пользователя или группы состоит из следующих частей:</span><span class="sxs-lookup"><span data-stu-id="19f2e-110">The DROP USER or GROUP statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="19f2e-111">Часть</span><span class="sxs-lookup"><span data-stu-id="19f2e-111">Part</span></span></p></th>
<th><p><span data-ttu-id="19f2e-112">Описание</span><span class="sxs-lookup"><span data-stu-id="19f2e-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="19f2e-113"><em>user</em></span><span class="sxs-lookup"><span data-stu-id="19f2e-113"><em>user</em></span></span></p></td>
<td><p><span data-ttu-id="19f2e-114">Имя пользователя для удаления из файла рабочей группы.</span><span class="sxs-lookup"><span data-stu-id="19f2e-114">The name of a user to be removed from the workgroup information file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19f2e-115"><em>group</em></span><span class="sxs-lookup"><span data-stu-id="19f2e-115"><em>group</em></span></span></p></td>
<td><p><span data-ttu-id="19f2e-116">Имя группы для удаления из файла рабочей группы.</span><span class="sxs-lookup"><span data-stu-id="19f2e-116">The name of a group to be removed from the workgroup information file.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="19f2e-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="19f2e-117">Remarks</span></span>

<span data-ttu-id="19f2e-118">При использовании этого ключевого слова в инструкции DROP USER каждого из s *пользователей*, перечисленных в инструкции будет удален из *группы* указанной после этого ключевого слова.</span><span class="sxs-lookup"><span data-stu-id="19f2e-118">If the FROM keyword is used in the DROP USER statement, then each of the *user*s listed in the statement will be removed from the *group* specified following the FROM keyword.</span></span> <span data-ttu-id="19f2e-119">Тем не менее *Пользователи*сами не будут удалены.</span><span class="sxs-lookup"><span data-stu-id="19f2e-119">However, the *user*s themselves will not be deleted.</span></span>

<span data-ttu-id="19f2e-120">Инструкция DROP GROUP удаляет указанный *группы*(s).</span><span class="sxs-lookup"><span data-stu-id="19f2e-120">The DROP GROUP statement will delete the specified *group*(s).</span></span> <span data-ttu-id="19f2e-121">S *пользователей*, которые входят в *группу*(s) не удаляются, но они больше не входят удаленные *группы*(s).</span><span class="sxs-lookup"><span data-stu-id="19f2e-121">The *user*s who are members of the *group*(s) will not be affected, but they will no longer be members of the deleted *group*(s).</span></span>

