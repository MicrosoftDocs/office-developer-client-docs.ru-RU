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
ms.openlocfilehash: 4bcdd7aa77823a53ba2a2c0cde4badbac571611a
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860548"
---
# <a name="revoke-statement-microsoft-access-sql"></a><span data-ttu-id="e7072-102">ОТМЕНИТЬ оператора (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="e7072-102">REVOKE statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="e7072-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e7072-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e7072-104">Запрещение определенных привилегий существующему пользователю или группе.</span><span class="sxs-lookup"><span data-stu-id="e7072-104">Revokes specific privileges from an existing user or group.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7072-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e7072-105">Syntax</span></span>

<span data-ttu-id="e7072-106">ОТМЕНИТЬ {*принципу предоставления минимальных прав*\[, *принципу предоставления минимальных прав*,... \]} Д {таблицы в *таблице* | Объект *object*|</span><span class="sxs-lookup"><span data-stu-id="e7072-106">REVOKE {*privilege*\[, *privilege*, …\]} ON {TABLE *table* | OBJECT *object*|</span></span>

<span data-ttu-id="e7072-107">CONTAINTER *container*} из {*имя_обладателя_прав*\[, *имя_обладателя_прав*,... \]}</span><span class="sxs-lookup"><span data-stu-id="e7072-107">CONTAINTER *container*} FROM {*authorizationname*\[, *authorizationname*, …\]}</span></span>

<span data-ttu-id="e7072-108">Инструкция REVOKE состоит из следующих частей:</span><span class="sxs-lookup"><span data-stu-id="e7072-108">The REVOKE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e7072-109">Часть</span><span class="sxs-lookup"><span data-stu-id="e7072-109">Part</span></span></p></th>
<th><p><span data-ttu-id="e7072-110">Описание</span><span class="sxs-lookup"><span data-stu-id="e7072-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e7072-111"><em>принципу предоставления минимальных прав</em></span><span class="sxs-lookup"><span data-stu-id="e7072-111"><em>privilege</em></span></span></p></td>
<td><p><span data-ttu-id="e7072-112">Привилегии или права, которое требуется отозвать.</span><span class="sxs-lookup"><span data-stu-id="e7072-112">The privilege or privileges to be revoked.</span></span> <span data-ttu-id="e7072-113">Привилегии задаются с помощью следующих ключевых слов: выбор, DELETE, INSERT, UPDATE, размещения сообщений, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, создать, SELECTSCHEMA, СХЕМЫ и UPDATEOWNER.</span><span class="sxs-lookup"><span data-stu-id="e7072-113">Privileges are specified using the following keywords: SELECT, DELETE, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA, and UPDATEOWNER.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7072-114"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="e7072-114"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="e7072-115">Любое допустимое имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="e7072-115">Any valid table name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7072-116"><em>object</em></span><span class="sxs-lookup"><span data-stu-id="e7072-116"><em>object</em></span></span></p></td>
<td><p><span data-ttu-id="e7072-117">Это могут использовать любой объект не таблицы.</span><span class="sxs-lookup"><span data-stu-id="e7072-117">This can encompass any non-table object.</span></span> <span data-ttu-id="e7072-118">Сохраненные запрос (представления или процедуры) — один пример.</span><span class="sxs-lookup"><span data-stu-id="e7072-118">A stored query (view or procedure) is one example.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7072-119"><em>контейнер</em></span><span class="sxs-lookup"><span data-stu-id="e7072-119"><em>container</em></span></span></p></td>
<td><p><span data-ttu-id="e7072-120">Имя допустимого хранилища.</span><span class="sxs-lookup"><span data-stu-id="e7072-120">The name of a valid container.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7072-121"><em>имя_обладателя_прав</em></span><span class="sxs-lookup"><span data-stu-id="e7072-121"><em>authorizationname</em></span></span></p></td>
<td><p><span data-ttu-id="e7072-122">Имя пользователя или группы.</span><span class="sxs-lookup"><span data-stu-id="e7072-122">A user or group name.</span></span></p></td>
</tr>
</tbody>
</table>

