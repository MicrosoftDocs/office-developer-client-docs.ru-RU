---
title: Заявление REVOKE (Microsoft Access SQL)
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
# <a name="revoke-statement-microsoft-access-sql"></a><span data-ttu-id="cbbe2-102">Заявление REVOKE (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="cbbe2-102">REVOKE statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="cbbe2-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cbbe2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cbbe2-104">Отменяет определенные привилегии от существующего пользователя или группы.</span><span class="sxs-lookup"><span data-stu-id="cbbe2-104">Revokes specific privileges from an existing user or group.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbbe2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cbbe2-105">Syntax</span></span>

<span data-ttu-id="cbbe2-106">REVOKE {*привилегии* \[ , *привилегии*, ... \] } ON {TABLE *table* | *ОБЪЕКТ-объект*|</span><span class="sxs-lookup"><span data-stu-id="cbbe2-106">REVOKE {*privilege*\[, *privilege*, …\]} ON {TABLE *table* | OBJECT *object*|</span></span>

<span data-ttu-id="cbbe2-107">КОНТЕЙНЕР *CONTAINTER*} FROM *{authorizationname,* \[ *authorizationname*, ... \] }</span><span class="sxs-lookup"><span data-stu-id="cbbe2-107">CONTAINTER *container*} FROM {*authorizationname*\[, *authorizationname*, …\]}</span></span>

<span data-ttu-id="cbbe2-108">В заявлении REVOKE есть такие части:</span><span class="sxs-lookup"><span data-stu-id="cbbe2-108">The REVOKE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cbbe2-109">Part</span><span class="sxs-lookup"><span data-stu-id="cbbe2-109">Part</span></span></p></th>
<th><p><span data-ttu-id="cbbe2-110">Описание</span><span class="sxs-lookup"><span data-stu-id="cbbe2-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cbbe2-111"><em>привилегия</em></span><span class="sxs-lookup"><span data-stu-id="cbbe2-111"><em>privilege</em></span></span></p></td>
<td><p><span data-ttu-id="cbbe2-112">Привилегии или привилегии, которые необходимо отозвали.</span><span class="sxs-lookup"><span data-stu-id="cbbe2-112">The privilege or privileges to be revoked.</span></span> <span data-ttu-id="cbbe2-113">Привилегии заданы с помощью следующих ключевых слов: SELECT, DELETE, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA и UPDATEOWNER.</span><span class="sxs-lookup"><span data-stu-id="cbbe2-113">Privileges are specified using the following keywords: SELECT, DELETE, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA, and UPDATEOWNER.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cbbe2-114"><em>таблица</em></span><span class="sxs-lookup"><span data-stu-id="cbbe2-114"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="cbbe2-115">Любое допустимые имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="cbbe2-115">Any valid table name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cbbe2-116"><em>object</em></span><span class="sxs-lookup"><span data-stu-id="cbbe2-116"><em>object</em></span></span></p></td>
<td><p><span data-ttu-id="cbbe2-117">Это может охватывать любой объект без таблицы.</span><span class="sxs-lookup"><span data-stu-id="cbbe2-117">This can encompass any non-table object.</span></span> <span data-ttu-id="cbbe2-118">Одним из примеров является сохраненный запрос (представление или процедура).</span><span class="sxs-lookup"><span data-stu-id="cbbe2-118">A stored query (view or procedure) is one example.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cbbe2-119"><em>контейнер</em></span><span class="sxs-lookup"><span data-stu-id="cbbe2-119"><em>container</em></span></span></p></td>
<td><p><span data-ttu-id="cbbe2-120">Имя допустимого контейнера.</span><span class="sxs-lookup"><span data-stu-id="cbbe2-120">The name of a valid container.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cbbe2-121"><em>имя авторизации</em></span><span class="sxs-lookup"><span data-stu-id="cbbe2-121"><em>authorizationname</em></span></span></p></td>
<td><p><span data-ttu-id="cbbe2-122">Имя пользователя или группы.</span><span class="sxs-lookup"><span data-stu-id="cbbe2-122">A user or group name.</span></span></p></td>
</tr>
</tbody>
</table>

