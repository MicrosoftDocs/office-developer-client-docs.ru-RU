---
title: Создание пользователя или группы оператора (Microsoft Access SQL)
TOCTitle: CREATE USER or GROUP statement (Microsoft Access SQL)
ms:assetid: 62148ce2-0f81-944e-a1ab-edef990fff9f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194914(v=office.15)
ms:contentKeyID: 48545229
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 52d376b05c195ed0ea4707e849c5ae395c2b5590
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936828"
---
# <a name="create-user-or-group-statement-microsoft-access-sql"></a><span data-ttu-id="7f98c-102">Создание пользователя или группы оператора (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="7f98c-102">CREATE USER or GROUP statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="7f98c-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7f98c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7f98c-104">Создает один или несколько новых пользователей или групп.</span><span class="sxs-lookup"><span data-stu-id="7f98c-104">Creates one or more new users or groups.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f98c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7f98c-105">Syntax</span></span>

### <a name="create-a-user"></a><span data-ttu-id="7f98c-106">Создание пользователя</span><span class="sxs-lookup"><span data-stu-id="7f98c-106">Create a user</span></span>

<span data-ttu-id="7f98c-107">Создание пользователя *пользователя* *пароль pid* \[, *пользователь* *пароль pid*,...\]</span><span class="sxs-lookup"><span data-stu-id="7f98c-107">CREATE USER *user* *password pid* \[, *user* *password pid*, …\]</span></span>

### <a name="create-a-group"></a><span data-ttu-id="7f98c-108">Создание группы</span><span class="sxs-lookup"><span data-stu-id="7f98c-108">Create a group</span></span>

<span data-ttu-id="7f98c-109">Создание группы *группы* *pid*\[, *Группа* *pid*...\]</span><span class="sxs-lookup"><span data-stu-id="7f98c-109">CREATE GROUP *group* *pid*\[, *group* *pid*, …\]</span></span>

<span data-ttu-id="7f98c-110">Создание пользователя или группы оператора состоит из следующих частей:</span><span class="sxs-lookup"><span data-stu-id="7f98c-110">The CREATE USER or GROUP statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7f98c-111">Часть</span><span class="sxs-lookup"><span data-stu-id="7f98c-111">Part</span></span></p></th>
<th><p><span data-ttu-id="7f98c-112">Описание</span><span class="sxs-lookup"><span data-stu-id="7f98c-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7f98c-113"><em>user</em></span><span class="sxs-lookup"><span data-stu-id="7f98c-113"><em>user</em></span></span></p></td>
<td><p><span data-ttu-id="7f98c-114">Имя пользователя для добавления файла рабочей группы.</span><span class="sxs-lookup"><span data-stu-id="7f98c-114">The name of a user to be added to the workgroup information file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f98c-115"><em>group</em></span><span class="sxs-lookup"><span data-stu-id="7f98c-115"><em>group</em></span></span></p></td>
<td><p><span data-ttu-id="7f98c-116">Имя группы для добавления файла рабочей группы.</span><span class="sxs-lookup"><span data-stu-id="7f98c-116">The name of a group to be added to the workgroup information file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f98c-117"><em>password</em></span><span class="sxs-lookup"><span data-stu-id="7f98c-117"><em>password</em></span></span></p></td>
<td><p><span data-ttu-id="7f98c-118">Пароль, будет связан с именем указанного <em>пользователя</em> .</span><span class="sxs-lookup"><span data-stu-id="7f98c-118">The password to be associated with the specified <em>user</em> name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f98c-119"><em>pid</em></span><span class="sxs-lookup"><span data-stu-id="7f98c-119"><em>pid</em></span></span></p></td>
<td><p><span data-ttu-id="7f98c-120">Личный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="7f98c-120">The personal id.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="7f98c-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="7f98c-121">Remarks</span></span>

<span data-ttu-id="7f98c-122">*Пользователей* и *группы* не может содержать таким же именем.</span><span class="sxs-lookup"><span data-stu-id="7f98c-122">A *user* and a *group* cannot have the same name.</span></span>

<span data-ttu-id="7f98c-123">*Пароль* необходим для каждого *пользователя* или *группы* , которая создается.</span><span class="sxs-lookup"><span data-stu-id="7f98c-123">A *password* is required for each *user* or *group* that is created.</span></span>

