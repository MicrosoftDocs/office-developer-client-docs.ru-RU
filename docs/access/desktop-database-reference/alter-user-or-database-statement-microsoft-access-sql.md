---
title: ALTER USER or DATABASE statement (Microsoft Access SQL)
TOCTitle: ALTER USER or DATABASE statement (Microsoft Access SQL)
ms:assetid: 86ccd296-5171-97e7-683f-cdaab4bde9ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197012(v=office.15)
ms:contentKeyID: 48546093
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2514ca6403ce70acae9e344d610fbd7b9ba7d73b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297181"
---
# <a name="alter-user-or-database-statement-microsoft-access-sql"></a><span data-ttu-id="534bf-102">ALTER USER or DATABASE statement (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="534bf-102">ALTER USER or DATABASE statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="534bf-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="534bf-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="534bf-104">Изменяет пароль для существующего пользователя или базы данных.</span><span class="sxs-lookup"><span data-stu-id="534bf-104">Changes the password for an existing user or for a database.</span></span>

## <a name="syntax"></a><span data-ttu-id="534bf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="534bf-105">Syntax</span></span>

<span data-ttu-id="534bf-106">ALTER DATABASE PASSWORD *newpassword oldpassword*</span><span class="sxs-lookup"><span data-stu-id="534bf-106">ALTER DATABASE PASSWORD *newpassword oldpassword*</span></span>

<span data-ttu-id="534bf-107">ALTER USER *USER* PASSWORD *newpassword oldpassword*</span><span class="sxs-lookup"><span data-stu-id="534bf-107">ALTER USER *user* PASSWORD *newpassword oldpassword*</span></span>

<span data-ttu-id="534bf-108">The ALTER USER or DATABASE statement has these parts:</span><span class="sxs-lookup"><span data-stu-id="534bf-108">The ALTER USER or DATABASE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="534bf-109">Часть</span><span class="sxs-lookup"><span data-stu-id="534bf-109">Part</span></span></p></th>
<th><p><span data-ttu-id="534bf-110">Описание</span><span class="sxs-lookup"><span data-stu-id="534bf-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="534bf-111"><em>user</em></span><span class="sxs-lookup"><span data-stu-id="534bf-111"><em>user</em></span></span></p></td>
<td><p><span data-ttu-id="534bf-112">Имя пользователя, добавляемого в файл сведений о группе.</span><span class="sxs-lookup"><span data-stu-id="534bf-112">The name of a user to be added to the workgroup information file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="534bf-113"><em>newpassword</em></span><span class="sxs-lookup"><span data-stu-id="534bf-113"><em>newpassword</em></span></span></p></td>
<td><p><span data-ttu-id="534bf-114">Новый пароль, связанный с указанным <em>пользователем или именем</em> <em>базы</em> данных.</span><span class="sxs-lookup"><span data-stu-id="534bf-114">The new password to be associated with the specified <em>user</em> or <em>database</em> name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="534bf-115"><em>oldpassword</em></span><span class="sxs-lookup"><span data-stu-id="534bf-115"><em>oldpassword</em></span></span></p></td>
<td><p><span data-ttu-id="534bf-116">Существующий пароль, который должен быть связан с указанным <em>пользователем или</em> <em>именем</em> группы.</span><span class="sxs-lookup"><span data-stu-id="534bf-116">The existing password to be associated with the specified <em>user</em> or <em>group</em> name.</span></span></p></td>
</tr>
</tbody>
</table>

