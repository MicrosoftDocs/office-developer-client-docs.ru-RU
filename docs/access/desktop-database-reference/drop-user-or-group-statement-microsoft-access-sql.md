---
title: Удаление пользователя или группы оператора (Microsoft Access SQL)
TOCTitle: DROP USER or GROUP statement (Microsoft Access SQL)
ms:assetid: 46bc5916-556b-17df-2f4c-8fd7bbd21ef7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193192(v=office.15)
ms:contentKeyID: 48544575
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: f9662c4f0cb691136a556faa32cb0d5a1c775268
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936835"
---
# <a name="drop-user-or-group-statement-microsoft-access-sql"></a><span data-ttu-id="04ae9-102">Удаление пользователя или группы оператора (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="04ae9-102">DROP USER or GROUP statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="04ae9-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="04ae9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="04ae9-104">Удаляет один или несколько существующих *пользователей* или *групп*, или удаляет одного или нескольких существующих *пользователей* из существующей *группы*.</span><span class="sxs-lookup"><span data-stu-id="04ae9-104">Deletes one or more existing *users* or *groups*, or removes one or more existing *users* from an existing *group*.</span></span>

## <a name="syntax"></a><span data-ttu-id="04ae9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="04ae9-105">Syntax</span></span>

### <a name="delete-one-or-more-users-or-remove-one-or-more-users-from-a-group"></a><span data-ttu-id="04ae9-106">Удаление одного или нескольких пользователей или удалить один или несколько пользователей из группы</span><span class="sxs-lookup"><span data-stu-id="04ae9-106">Delete one or more users or remove one or more users from a group</span></span>

<span data-ttu-id="04ae9-107">Удаление пользователя *пользователя*\[, *пользователь*... \] \[Из *группы*\]</span><span class="sxs-lookup"><span data-stu-id="04ae9-107">DROP USER *user*\[, *user*, …\] \[FROM *group*\]</span></span>

### <a name="delete-one-or-more-groups"></a><span data-ttu-id="04ae9-108">Удаление одного или нескольких групп</span><span class="sxs-lookup"><span data-stu-id="04ae9-108">Delete one or more groups</span></span>

<span data-ttu-id="04ae9-109">ГРУППА РАЗМЕЩЕНИЯ *группы*\[, *Группа*...\]</span><span class="sxs-lookup"><span data-stu-id="04ae9-109">DROP GROUP *group*\[, *group*, …\]</span></span>

<span data-ttu-id="04ae9-110">Оператор удаление пользователя или группы состоит из следующих частей:</span><span class="sxs-lookup"><span data-stu-id="04ae9-110">The DROP USER or GROUP statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="04ae9-111">Часть</span><span class="sxs-lookup"><span data-stu-id="04ae9-111">Part</span></span></p></th>
<th><p><span data-ttu-id="04ae9-112">Описание</span><span class="sxs-lookup"><span data-stu-id="04ae9-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="04ae9-113"><em>user</em></span><span class="sxs-lookup"><span data-stu-id="04ae9-113"><em>user</em></span></span></p></td>
<td><p><span data-ttu-id="04ae9-114">Имя пользователя для удаления из файла рабочей группы.</span><span class="sxs-lookup"><span data-stu-id="04ae9-114">The name of a user to be removed from the workgroup information file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04ae9-115"><em>group</em></span><span class="sxs-lookup"><span data-stu-id="04ae9-115"><em>group</em></span></span></p></td>
<td><p><span data-ttu-id="04ae9-116">Имя группы для удаления из файла рабочей группы.</span><span class="sxs-lookup"><span data-stu-id="04ae9-116">The name of a group to be removed from the workgroup information file.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="04ae9-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="04ae9-117">Remarks</span></span>

<span data-ttu-id="04ae9-118">При использовании этого ключевого слова в инструкции DROP USER каждого из *пользователей* , перечисленных в инструкции будет удален из *группы* указанной после этого ключевого слова.</span><span class="sxs-lookup"><span data-stu-id="04ae9-118">If the FROM keyword is used in the DROP USER statement, each of the *users* listed in the statement will be removed from the *group* specified following the FROM keyword.</span></span> <span data-ttu-id="04ae9-119">Тем не менее, *Пользователи* сами не будут удалены.</span><span class="sxs-lookup"><span data-stu-id="04ae9-119">However, the *users* themselves will not be deleted.</span></span>

<span data-ttu-id="04ae9-120">Инструкция DROP GROUP удаляет указанный *группы*(s).</span><span class="sxs-lookup"><span data-stu-id="04ae9-120">The DROP GROUP statement will delete the specified *group*(s).</span></span> <span data-ttu-id="04ae9-121">*Пользователи* , которые входят в *группу*(s) не удаляются, но они больше не входят удаленные *группы*(s).</span><span class="sxs-lookup"><span data-stu-id="04ae9-121">The *users* who are members of the *group*(s) will not be affected, but they will no longer be members of the deleted *group*(s).</span></span>

