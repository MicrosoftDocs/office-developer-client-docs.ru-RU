---
title: Заявление GRANT (Microsoft Access SQL)
TOCTitle: GRANT statement (Microsoft Access SQL)
ms:assetid: 50ae97ae-d5be-57e5-d9da-f3fc42f01d83
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193820(v=office.15)
ms:contentKeyID: 48544800
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277478
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 4357099f8bcb9b2308b5cda3543949765b8c3420
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292134"
---
# <a name="grant-statement-microsoft-access-sql"></a><span data-ttu-id="190c9-102">Заявление GRANT (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="190c9-102">GRANT statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="190c9-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="190c9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="190c9-104">Предоставляет определенные привилегии существующему пользователю или группе.</span><span class="sxs-lookup"><span data-stu-id="190c9-104">Grants specific privileges to an existing user or group.</span></span>

## <a name="syntax"></a><span data-ttu-id="190c9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="190c9-105">Syntax</span></span>

<span data-ttu-id="190c9-106">GRANT *{privilege* \[ , *privilege*, ... \] } ТАБЛИЦА ON{TABLE *|* *ОБЪЕКТ-объект*|</span><span class="sxs-lookup"><span data-stu-id="190c9-106">GRANT {*privilege*\[, *privilege*, …\]} ON{TABLE *table* | OBJECT *object*|</span></span>

<span data-ttu-id="190c9-107">КОНТЕЙНЕР *контейнера* } TO {*имя авторизации,* \[ имя *авторизации*, ... \] }</span><span class="sxs-lookup"><span data-stu-id="190c9-107">CONTAINER *container* } TO {*authorizationname*\[, *authorizationname*, …\]}</span></span>

<span data-ttu-id="190c9-108">В заявлении GRANT есть такие части:</span><span class="sxs-lookup"><span data-stu-id="190c9-108">The GRANT statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="190c9-109">Part</span><span class="sxs-lookup"><span data-stu-id="190c9-109">Part</span></span></p></th>
<th><p><span data-ttu-id="190c9-110">Описание</span><span class="sxs-lookup"><span data-stu-id="190c9-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="190c9-111"><em>привилегия</em></span><span class="sxs-lookup"><span data-stu-id="190c9-111"><em>privilege</em></span></span></p></td>
<td><p><span data-ttu-id="190c9-112">Привилегии или привилегии, которые должны быть предоставлены.</span><span class="sxs-lookup"><span data-stu-id="190c9-112">The privilege or privileges to be granted.</span></span> <span data-ttu-id="190c9-113">Привилегии заданы с помощью следующих ключевых слов: SELECT, DELETE, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA и UPDATEOWNER.</span><span class="sxs-lookup"><span data-stu-id="190c9-113">Privileges are specified using the following keywords: SELECT, DELETE, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA, and UPDATEOWNER.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="190c9-114"><em>имя таблицы</em></span><span class="sxs-lookup"><span data-stu-id="190c9-114"><em>tablename</em></span></span></p></td>
<td><p><span data-ttu-id="190c9-115">Любое допустимые имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="190c9-115">Any valid table name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="190c9-116"><em>object</em></span><span class="sxs-lookup"><span data-stu-id="190c9-116"><em>object</em></span></span></p></td>
<td><p><span data-ttu-id="190c9-117">Это может охватывать любой объект без таблицы.</span><span class="sxs-lookup"><span data-stu-id="190c9-117">This can encompass any non-table object.</span></span> <span data-ttu-id="190c9-118">Одним из примеров является сохраненный запрос (представление или процедура).</span><span class="sxs-lookup"><span data-stu-id="190c9-118">A stored query (view or procedure) is one example.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="190c9-119"><em>контейнер</em></span><span class="sxs-lookup"><span data-stu-id="190c9-119"><em>container</em></span></span></p></td>
<td><p><span data-ttu-id="190c9-120">Имя допустимого контейнера.</span><span class="sxs-lookup"><span data-stu-id="190c9-120">The name of a valid container.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="190c9-121"><em>имя авторизации</em></span><span class="sxs-lookup"><span data-stu-id="190c9-121"><em>authorizationname</em></span></span></p></td>
<td><p><span data-ttu-id="190c9-122">Имя пользователя или группы.</span><span class="sxs-lookup"><span data-stu-id="190c9-122">A user or group name.</span></span></p></td>
</tr>
</tbody>
</table>

