---
title: Create USER или GROUP statement (Microsoft Access SQL)
TOCTitle: CREATE USER or GROUP statement (Microsoft Access SQL)
ms:assetid: 62148ce2-0f81-944e-a1ab-edef990fff9f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194914(v=office.15)
ms:contentKeyID: 48545229
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5b294af16498778eae94b38a7a31b93fd029585e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295382"
---
# <a name="create-user-or-group-statement-microsoft-access-sql"></a><span data-ttu-id="115f0-102">CREATE USER or GROUP statement (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="115f0-102">CREATE USER or GROUP statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="115f0-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="115f0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="115f0-104">Создает одного или несколько новых пользователей или групп.</span><span class="sxs-lookup"><span data-stu-id="115f0-104">Creates one or more new users or groups.</span></span>

## <a name="syntax"></a><span data-ttu-id="115f0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="115f0-105">Syntax</span></span>

### <a name="create-a-user"></a><span data-ttu-id="115f0-106">Создание пользователя</span><span class="sxs-lookup"><span data-stu-id="115f0-106">Create a user</span></span>

<span data-ttu-id="115f0-107">CREATE USER *user* *password pid* \[ , *user* *password pid*, ...\]</span><span class="sxs-lookup"><span data-stu-id="115f0-107">CREATE USER *user* *password pid* \[, *user* *password pid*, …\]</span></span>

### <a name="create-a-group"></a><span data-ttu-id="115f0-108">Создание группы</span><span class="sxs-lookup"><span data-stu-id="115f0-108">Create a group</span></span>

<span data-ttu-id="115f0-109">CREATE GROUP *group* *pid,* \[ *group* *pid*, ...\]</span><span class="sxs-lookup"><span data-stu-id="115f0-109">CREATE GROUP *group* *pid*\[, *group* *pid*, …\]</span></span>

<span data-ttu-id="115f0-110">The CREATE USER or GROUP statement has these parts:</span><span class="sxs-lookup"><span data-stu-id="115f0-110">The CREATE USER or GROUP statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="115f0-111">Часть</span><span class="sxs-lookup"><span data-stu-id="115f0-111">Part</span></span></p></th>
<th><p><span data-ttu-id="115f0-112">Описание</span><span class="sxs-lookup"><span data-stu-id="115f0-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="115f0-113"><em>user</em></span><span class="sxs-lookup"><span data-stu-id="115f0-113"><em>user</em></span></span></p></td>
<td><p><span data-ttu-id="115f0-114">Имя пользователя, добавляемого в файл сведений о группе.</span><span class="sxs-lookup"><span data-stu-id="115f0-114">The name of a user to be added to the workgroup information file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="115f0-115"><em>group</em></span><span class="sxs-lookup"><span data-stu-id="115f0-115"><em>group</em></span></span></p></td>
<td><p><span data-ttu-id="115f0-116">Имя группы, добавляемой в файл сведений о рабочей группе.</span><span class="sxs-lookup"><span data-stu-id="115f0-116">The name of a group to be added to the workgroup information file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="115f0-117"><em>password</em></span><span class="sxs-lookup"><span data-stu-id="115f0-117"><em>password</em></span></span></p></td>
<td><p><span data-ttu-id="115f0-118">Пароль, который должен быть связан с указанным <em>именем</em> пользователя.</span><span class="sxs-lookup"><span data-stu-id="115f0-118">The password to be associated with the specified <em>user</em> name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="115f0-119"><em>pid</em></span><span class="sxs-lookup"><span data-stu-id="115f0-119"><em>pid</em></span></span></p></td>
<td><p><span data-ttu-id="115f0-120">Личный ид.</span><span class="sxs-lookup"><span data-stu-id="115f0-120">The personal id.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="115f0-121">Заметки</span><span class="sxs-lookup"><span data-stu-id="115f0-121">Remarks</span></span>

<span data-ttu-id="115f0-122">Имя *пользователя* и *группы* не может быть одинаковым.</span><span class="sxs-lookup"><span data-stu-id="115f0-122">A *user* and a *group* cannot have the same name.</span></span>

<span data-ttu-id="115f0-123">Для *каждого* создадаемой  группы или пользователя требуется пароль. </span><span class="sxs-lookup"><span data-stu-id="115f0-123">A *password* is required for each *user* or *group* that is created.</span></span>

