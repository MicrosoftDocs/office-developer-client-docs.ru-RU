---
title: Оператор REVOKE (Microsoft Access SQL)
TOCTitle: REVOKE statement (Microsoft Access SQL)
ms:assetid: 69399fd6-c4e8-f2e2-e5f4-48ae779323f5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195272(v=office.15)
ms:contentKeyID: 48545409
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277479
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 20122fee617597987940766a076d5f968a87c2d2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306533"
---
# <a name="revoke-statement-microsoft-access-sql"></a><span data-ttu-id="576e6-102">Оператор REVOKE (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="576e6-102">REVOKE statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="576e6-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="576e6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="576e6-104">Отзывает определенные привилегии у существующего пользователя или группы.</span><span class="sxs-lookup"><span data-stu-id="576e6-104">Revokes specific privileges from an existing user or group.</span></span>

## <a name="syntax"></a><span data-ttu-id="576e6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="576e6-105">Syntax</span></span>

<span data-ttu-id="576e6-106">Отзыв {*привилегия*\[, *привилегия*,... \]} В *таблице* {Table | *Объект* Object|</span><span class="sxs-lookup"><span data-stu-id="576e6-106">REVOKE {*privilege*\[, *privilege*, …\]} ON {TABLE *table* | OBJECT *object*|</span></span>

<span data-ttu-id="576e6-107">Контаинтер *Container*} из {*аусоризатионнаме*\[, *аусоризатионнаме*,... \]}</span><span class="sxs-lookup"><span data-stu-id="576e6-107">CONTAINTER *container*} FROM {*authorizationname*\[, *authorizationname*, …\]}</span></span>

<span data-ttu-id="576e6-108">Оператор REVOKE состоит из следующих частей:</span><span class="sxs-lookup"><span data-stu-id="576e6-108">The REVOKE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="576e6-109">Часть</span><span class="sxs-lookup"><span data-stu-id="576e6-109">Part</span></span></p></th>
<th><p><span data-ttu-id="576e6-110">Описание</span><span class="sxs-lookup"><span data-stu-id="576e6-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="576e6-111"><em>правах</em></span><span class="sxs-lookup"><span data-stu-id="576e6-111"><em>privilege</em></span></span></p></td>
<td><p><span data-ttu-id="576e6-112">Привилегия или привилегии, которые необходимо отменить.</span><span class="sxs-lookup"><span data-stu-id="576e6-112">The privilege or privileges to be revoked.</span></span> <span data-ttu-id="576e6-113">Разрешения указываются с помощью следующих ключевых слов: SELECT, DELETE, INSERT, UPDATE, DROP, СЕЛЕКТСЕКУРИТИ, УПДАТЕСЕКУРИТИ, DBPASSWORD, УПДАТЕИДЕНТИТИ, CREATE, СЕЛЕКТСЧЕМА, SCHEMA и УПДАТЕОВНЕР.</span><span class="sxs-lookup"><span data-stu-id="576e6-113">Privileges are specified using the following keywords: SELECT, DELETE, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA, and UPDATEOWNER.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="576e6-114"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="576e6-114"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="576e6-115">Любое допустимое имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="576e6-115">Any valid table name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="576e6-116"><em>object</em></span><span class="sxs-lookup"><span data-stu-id="576e6-116"><em>object</em></span></span></p></td>
<td><p><span data-ttu-id="576e6-117">Это может охватывать любой объект, не являющийся таблицей.</span><span class="sxs-lookup"><span data-stu-id="576e6-117">This can encompass any non-table object.</span></span> <span data-ttu-id="576e6-118">Сохраненным запросом (представление или процедура) является один из примеров.</span><span class="sxs-lookup"><span data-stu-id="576e6-118">A stored query (view or procedure) is one example.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="576e6-119"><em>Container</em></span><span class="sxs-lookup"><span data-stu-id="576e6-119"><em>container</em></span></span></p></td>
<td><p><span data-ttu-id="576e6-120">Имя допустимого контейнера.</span><span class="sxs-lookup"><span data-stu-id="576e6-120">The name of a valid container.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="576e6-121"><em>аусоризатионнаме</em></span><span class="sxs-lookup"><span data-stu-id="576e6-121"><em>authorizationname</em></span></span></p></td>
<td><p><span data-ttu-id="576e6-122">Имя пользователя или группы.</span><span class="sxs-lookup"><span data-stu-id="576e6-122">A user or group name.</span></span></p></td>
</tr>
</tbody>
</table>

