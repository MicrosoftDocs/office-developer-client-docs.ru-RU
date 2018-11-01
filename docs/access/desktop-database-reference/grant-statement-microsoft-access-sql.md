---
title: Инструкция GRANT (Microsoft Access SQL)
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
ms.openlocfilehash: 7c109d1993d4f092439ae10828ce3143625b4ad6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871957"
---
# <a name="grant-statement-microsoft-access-sql"></a><span data-ttu-id="de5a5-102">Инструкция GRANT (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="de5a5-102">GRANT statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="de5a5-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="de5a5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="de5a5-104">Предоставление определенных привилегий существующему пользователю или группе.</span><span class="sxs-lookup"><span data-stu-id="de5a5-104">Grants specific privileges to an existing user or group.</span></span>

## <a name="syntax"></a><span data-ttu-id="de5a5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="de5a5-105">Syntax</span></span>

<span data-ttu-id="de5a5-106">Предоставление {*принципу предоставления минимальных прав*\[, *принципу предоставления минимальных прав*,... \]} Д {таблицы в *таблице* | Объект *object*|</span><span class="sxs-lookup"><span data-stu-id="de5a5-106">GRANT {*privilege*\[, *privilege*, …\]} ON{TABLE *table* | OBJECT *object*|</span></span>

<span data-ttu-id="de5a5-107">КОНТЕЙНЕР *container* } Кому {*имя_обладателя_прав*\[, *имя_обладателя_прав*,... \]}</span><span class="sxs-lookup"><span data-stu-id="de5a5-107">CONTAINER *container* } TO {*authorizationname*\[, *authorizationname*, …\]}</span></span>

<span data-ttu-id="de5a5-108">Инструкция GRANT состоит из следующих частей:</span><span class="sxs-lookup"><span data-stu-id="de5a5-108">The GRANT statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="de5a5-109">Часть</span><span class="sxs-lookup"><span data-stu-id="de5a5-109">Part</span></span></p></th>
<th><p><span data-ttu-id="de5a5-110">Описание</span><span class="sxs-lookup"><span data-stu-id="de5a5-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="de5a5-111"><em>принципу предоставления минимальных прав</em></span><span class="sxs-lookup"><span data-stu-id="de5a5-111"><em>privilege</em></span></span></p></td>
<td><p><span data-ttu-id="de5a5-112">Принципу предоставления минимальных прав или предоставляемые привилегии.</span><span class="sxs-lookup"><span data-stu-id="de5a5-112">The privilege or privileges to be granted.</span></span> <span data-ttu-id="de5a5-113">Привилегии задаются с помощью следующих ключевых слов: выбор, DELETE, INSERT, UPDATE, размещения сообщений, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, создать, SELECTSCHEMA, СХЕМЫ и UPDATEOWNER.</span><span class="sxs-lookup"><span data-stu-id="de5a5-113">Privileges are specified using the following keywords: SELECT, DELETE, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA, and UPDATEOWNER.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de5a5-114"><em>TableName</em></span><span class="sxs-lookup"><span data-stu-id="de5a5-114"><em>tablename</em></span></span></p></td>
<td><p><span data-ttu-id="de5a5-115">Любое допустимое имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="de5a5-115">Any valid table name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de5a5-116"><em>object</em></span><span class="sxs-lookup"><span data-stu-id="de5a5-116"><em>object</em></span></span></p></td>
<td><p><span data-ttu-id="de5a5-117">Это могут использовать любой объект не таблицы.</span><span class="sxs-lookup"><span data-stu-id="de5a5-117">This can encompass any non-table object.</span></span> <span data-ttu-id="de5a5-118">Сохраненные запрос (представления или процедуры) — один пример.</span><span class="sxs-lookup"><span data-stu-id="de5a5-118">A stored query (view or procedure) is one example.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de5a5-119"><em>контейнер</em></span><span class="sxs-lookup"><span data-stu-id="de5a5-119"><em>container</em></span></span></p></td>
<td><p><span data-ttu-id="de5a5-120">Имя допустимого хранилища.</span><span class="sxs-lookup"><span data-stu-id="de5a5-120">The name of a valid container.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de5a5-121"><em>имя_обладателя_прав</em></span><span class="sxs-lookup"><span data-stu-id="de5a5-121"><em>authorizationname</em></span></span></p></td>
<td><p><span data-ttu-id="de5a5-122">Имя пользователя или группы.</span><span class="sxs-lookup"><span data-stu-id="de5a5-122">A user or group name.</span></span></p></td>
</tr>
</tbody>
</table>

