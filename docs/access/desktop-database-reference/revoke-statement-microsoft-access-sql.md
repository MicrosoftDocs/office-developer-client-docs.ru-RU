---
title: ОТМЕНИТЬ оператора (Microsoft Access SQL)
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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698452"
---
# <a name="revoke-statement-microsoft-access-sql"></a><span data-ttu-id="f1930-102">ОТМЕНИТЬ оператора (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="f1930-102">REVOKE statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="f1930-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f1930-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f1930-104">Запрещение определенных привилегий существующему пользователю или группе.</span><span class="sxs-lookup"><span data-stu-id="f1930-104">Revokes specific privileges from an existing user or group.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1930-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f1930-105">Syntax</span></span>

<span data-ttu-id="f1930-106">ОТМЕНИТЬ {*принципу предоставления минимальных прав*\[, *принципу предоставления минимальных прав*,... \]} Д {таблицы в *таблице* | Объект *object*|</span><span class="sxs-lookup"><span data-stu-id="f1930-106">REVOKE {*privilege*\[, *privilege*, …\]} ON {TABLE *table* | OBJECT *object*|</span></span>

<span data-ttu-id="f1930-107">CONTAINTER *container*} из {*имя_обладателя_прав*\[, *имя_обладателя_прав*,... \]}</span><span class="sxs-lookup"><span data-stu-id="f1930-107">CONTAINTER *container*} FROM {*authorizationname*\[, *authorizationname*, …\]}</span></span>

<span data-ttu-id="f1930-108">Инструкция REVOKE состоит из следующих частей:</span><span class="sxs-lookup"><span data-stu-id="f1930-108">The REVOKE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f1930-109">Часть</span><span class="sxs-lookup"><span data-stu-id="f1930-109">Part</span></span></p></th>
<th><p><span data-ttu-id="f1930-110">Описание</span><span class="sxs-lookup"><span data-stu-id="f1930-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1930-111"><em>принципу предоставления минимальных прав</em></span><span class="sxs-lookup"><span data-stu-id="f1930-111"><em>privilege</em></span></span></p></td>
<td><p><span data-ttu-id="f1930-112">Привилегии или права, которое требуется отозвать.</span><span class="sxs-lookup"><span data-stu-id="f1930-112">The privilege or privileges to be revoked.</span></span> <span data-ttu-id="f1930-113">Привилегии задаются с помощью следующих ключевых слов: выбор, DELETE, INSERT, UPDATE, размещения сообщений, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, создать, SELECTSCHEMA, СХЕМЫ и UPDATEOWNER.</span><span class="sxs-lookup"><span data-stu-id="f1930-113">Privileges are specified using the following keywords: SELECT, DELETE, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA, and UPDATEOWNER.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1930-114"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="f1930-114"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="f1930-115">Любое допустимое имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="f1930-115">Any valid table name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1930-116"><em>object</em></span><span class="sxs-lookup"><span data-stu-id="f1930-116"><em>object</em></span></span></p></td>
<td><p><span data-ttu-id="f1930-117">Это могут использовать любой объект не таблицы.</span><span class="sxs-lookup"><span data-stu-id="f1930-117">This can encompass any non-table object.</span></span> <span data-ttu-id="f1930-118">Сохраненные запрос (представления или процедуры) — один пример.</span><span class="sxs-lookup"><span data-stu-id="f1930-118">A stored query (view or procedure) is one example.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1930-119"><em>контейнер</em></span><span class="sxs-lookup"><span data-stu-id="f1930-119"><em>container</em></span></span></p></td>
<td><p><span data-ttu-id="f1930-120">Имя допустимого хранилища.</span><span class="sxs-lookup"><span data-stu-id="f1930-120">The name of a valid container.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1930-121"><em>имя_обладателя_прав</em></span><span class="sxs-lookup"><span data-stu-id="f1930-121"><em>authorizationname</em></span></span></p></td>
<td><p><span data-ttu-id="f1930-122">Имя пользователя или группы.</span><span class="sxs-lookup"><span data-stu-id="f1930-122">A user or group name.</span></span></p></td>
</tr>
</tbody>
</table>

