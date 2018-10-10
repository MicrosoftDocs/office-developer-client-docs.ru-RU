---
title: CREATE USER or GROUP Statement (Microsoft Access SQL)
TOCTitle: CREATE USER or GROUP Statement (Microsoft Access SQL)
ms:assetid: 62148ce2-0f81-944e-a1ab-edef990fff9f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194914(v=office.15)
ms:contentKeyID: 48545229
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dce5b9a6894eb1e09a0307b389207baefae6aa58
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481996"
---
# <a name="create-user-or-group-statement-microsoft-access-sql"></a><span data-ttu-id="e460a-102">CREATE USER or GROUP Statement (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="e460a-102">CREATE USER or GROUP Statement (Microsoft Access SQL)</span></span>


<span data-ttu-id="e460a-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e460a-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e460a-104">Создает один или несколько новых пользователей или групп.</span><span class="sxs-lookup"><span data-stu-id="e460a-104">Creates one or more new users or groups.</span></span>

## <a name="syntax"></a><span data-ttu-id="e460a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e460a-105">Syntax</span></span>

<span data-ttu-id="e460a-106">Создание пользователя:</span><span class="sxs-lookup"><span data-stu-id="e460a-106">Create a user:</span></span>

<span data-ttu-id="e460a-107">Создание пользователя *пользователя* *пароль pid* \[, *пользователь* *пароль pid*,...\]</span><span class="sxs-lookup"><span data-stu-id="e460a-107">CREATE USER *user* *password pid* \[, *user* *password pid*, …\]</span></span>

<span data-ttu-id="e460a-108">Создание группы:</span><span class="sxs-lookup"><span data-stu-id="e460a-108">Create a group:</span></span>

<span data-ttu-id="e460a-109">Создание группы *группы* *pid*\[, *Группа* *pid*...\]</span><span class="sxs-lookup"><span data-stu-id="e460a-109">CREATE GROUP *group* *pid*\[, *group* *pid*, …\]</span></span>

<span data-ttu-id="e460a-110">Создание пользователя или группы оператора состоит из следующих частей:</span><span class="sxs-lookup"><span data-stu-id="e460a-110">The CREATE USER or GROUP statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e460a-111">Часть</span><span class="sxs-lookup"><span data-stu-id="e460a-111">Part</span></span></p></th>
<th><p><span data-ttu-id="e460a-112">Описание</span><span class="sxs-lookup"><span data-stu-id="e460a-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e460a-113"><em>user</em></span><span class="sxs-lookup"><span data-stu-id="e460a-113"><em>user</em></span></span></p></td>
<td><p><span data-ttu-id="e460a-114">Имя пользователя для добавления файла рабочей группы.</span><span class="sxs-lookup"><span data-stu-id="e460a-114">The name of a user to be added to the workgroup information file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e460a-115"><em>group</em></span><span class="sxs-lookup"><span data-stu-id="e460a-115"><em>group</em></span></span></p></td>
<td><p><span data-ttu-id="e460a-116">Имя группы для добавления файла рабочей группы.</span><span class="sxs-lookup"><span data-stu-id="e460a-116">The name of a group to be added to the workgroup information file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e460a-117"><em>password</em></span><span class="sxs-lookup"><span data-stu-id="e460a-117"><em>password</em></span></span></p></td>
<td><p><span data-ttu-id="e460a-118">Пароль, будет связан с именем указанного <em>пользователя</em> .</span><span class="sxs-lookup"><span data-stu-id="e460a-118">The password to be associated with the specified <em>user</em> name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e460a-119"><em>pid</em></span><span class="sxs-lookup"><span data-stu-id="e460a-119"><em>pid</em></span></span></p></td>
<td><p><span data-ttu-id="e460a-120">Личный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="e460a-120">The personal id.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="e460a-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="e460a-121">Remarks</span></span>

<span data-ttu-id="e460a-122">*Пользователей* и *группы* не может содержать таким же именем.</span><span class="sxs-lookup"><span data-stu-id="e460a-122">A *user* and a *group* cannot have the same name.</span></span>

<span data-ttu-id="e460a-123">*Пароль* необходим для каждого *пользователя* или *группы* , которая создается.</span><span class="sxs-lookup"><span data-stu-id="e460a-123">A *password* is required for each *user* or *group* that is created.</span></span>

