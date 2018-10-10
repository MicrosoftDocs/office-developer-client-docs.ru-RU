---
title: ALTER USER or DATABASE Statement (Microsoft Access SQL)
TOCTitle: ALTER USER or DATABASE Statement (Microsoft Access SQL)
ms:assetid: 86ccd296-5171-97e7-683f-cdaab4bde9ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197012(v=office.15)
ms:contentKeyID: 48546093
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2d6e471adb7ef2c5826d24f569174b40247d0fd8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480975"
---
# <a name="alter-user-or-database-statement-microsoft-access-sql"></a><span data-ttu-id="1c8e2-102">ALTER USER or DATABASE Statement (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="1c8e2-102">ALTER USER or DATABASE Statement (Microsoft Access SQL)</span></span>


<span data-ttu-id="1c8e2-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="1c8e2-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="1c8e2-104">Изменение пароля для существующего пользователя или для базы данных.</span><span class="sxs-lookup"><span data-stu-id="1c8e2-104">Changes the password for an existing user or for a database.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c8e2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1c8e2-105">Syntax</span></span>

<span data-ttu-id="1c8e2-106">Изменение ПАРОЛЯ базы данных *старый_пароль новый_пароль*</span><span class="sxs-lookup"><span data-stu-id="1c8e2-106">ALTER DATABASE PASSWORD *newpassword oldpassword*</span></span>

<span data-ttu-id="1c8e2-107">ПАРОЛЬ *пользователя* ALTER пользователя *старый_пароль новый_пароль*</span><span class="sxs-lookup"><span data-stu-id="1c8e2-107">ALTER USER *user* PASSWORD *newpassword oldpassword*</span></span>

<span data-ttu-id="1c8e2-108">Оператор ALTER пользователя или базы данных состоит из следующих частей:</span><span class="sxs-lookup"><span data-stu-id="1c8e2-108">The ALTER USER or DATABASE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1c8e2-109">Часть</span><span class="sxs-lookup"><span data-stu-id="1c8e2-109">Part</span></span></p></th>
<th><p><span data-ttu-id="1c8e2-110">Описание</span><span class="sxs-lookup"><span data-stu-id="1c8e2-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1c8e2-111"><em>user</em></span><span class="sxs-lookup"><span data-stu-id="1c8e2-111"><em>user</em></span></span></p></td>
<td><p><span data-ttu-id="1c8e2-112">Имя пользователя для добавления файла рабочей группы.</span><span class="sxs-lookup"><span data-stu-id="1c8e2-112">The name of a user to be added to the workgroup information file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c8e2-113"><em>новый_пароль</em></span><span class="sxs-lookup"><span data-stu-id="1c8e2-113"><em>newpassword</em></span></span></p></td>
<td><p><span data-ttu-id="1c8e2-114">Новый пароль, который необходимо связать с указанным именем <em>пользователя</em> или <em>базы данных</em> .</span><span class="sxs-lookup"><span data-stu-id="1c8e2-114">The new password to be associated with the specified <em>user</em> or <em>database</em> name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c8e2-115"><em>старый_пароль</em></span><span class="sxs-lookup"><span data-stu-id="1c8e2-115"><em>oldpassword</em></span></span></p></td>
<td><p><span data-ttu-id="1c8e2-116">Существующий пароль следует связать с указанным именем <em>пользователя</em> или <em>группы</em> .</span><span class="sxs-lookup"><span data-stu-id="1c8e2-116">The existing password to be associated with the specified <em>user</em> or <em>group</em> name.</span></span></p></td>
</tr>
</tbody>
</table>

