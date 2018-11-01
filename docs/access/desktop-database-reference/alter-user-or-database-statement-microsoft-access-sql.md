---
title: Оператор ALTER пользователя или базы данных (Microsoft Access SQL)
TOCTitle: ALTER USER or DATABASE statement (Microsoft Access SQL)
ms:assetid: 86ccd296-5171-97e7-683f-cdaab4bde9ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197012(v=office.15)
ms:contentKeyID: 48546093
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: f0baf0faab717c35da0313d36e2ec1ac73528255
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879440"
---
# <a name="alter-user-or-database-statement-microsoft-access-sql"></a><span data-ttu-id="5b5a5-102">Оператор ALTER пользователя или базы данных (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="5b5a5-102">ALTER USER or DATABASE statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="5b5a5-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5b5a5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5b5a5-104">Изменение пароля для существующего пользователя или для базы данных.</span><span class="sxs-lookup"><span data-stu-id="5b5a5-104">Changes the password for an existing user or for a database.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b5a5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5b5a5-105">Syntax</span></span>

<span data-ttu-id="5b5a5-106">Изменение ПАРОЛЯ базы данных *старый_пароль новый_пароль*</span><span class="sxs-lookup"><span data-stu-id="5b5a5-106">ALTER DATABASE PASSWORD *newpassword oldpassword*</span></span>

<span data-ttu-id="5b5a5-107">ПАРОЛЬ *пользователя* ALTER пользователя *старый_пароль новый_пароль*</span><span class="sxs-lookup"><span data-stu-id="5b5a5-107">ALTER USER *user* PASSWORD *newpassword oldpassword*</span></span>

<span data-ttu-id="5b5a5-108">Оператор ALTER пользователя или базы данных состоит из следующих частей:</span><span class="sxs-lookup"><span data-stu-id="5b5a5-108">The ALTER USER or DATABASE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5b5a5-109">Часть</span><span class="sxs-lookup"><span data-stu-id="5b5a5-109">Part</span></span></p></th>
<th><p><span data-ttu-id="5b5a5-110">Описание</span><span class="sxs-lookup"><span data-stu-id="5b5a5-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5b5a5-111"><em>user</em></span><span class="sxs-lookup"><span data-stu-id="5b5a5-111"><em>user</em></span></span></p></td>
<td><p><span data-ttu-id="5b5a5-112">Имя пользователя для добавления файла рабочей группы.</span><span class="sxs-lookup"><span data-stu-id="5b5a5-112">The name of a user to be added to the workgroup information file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5b5a5-113"><em>новый_пароль</em></span><span class="sxs-lookup"><span data-stu-id="5b5a5-113"><em>newpassword</em></span></span></p></td>
<td><p><span data-ttu-id="5b5a5-114">Новый пароль, который необходимо связать с указанным именем <em>пользователя</em> или <em>базы данных</em> .</span><span class="sxs-lookup"><span data-stu-id="5b5a5-114">The new password to be associated with the specified <em>user</em> or <em>database</em> name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5b5a5-115"><em>старый_пароль</em></span><span class="sxs-lookup"><span data-stu-id="5b5a5-115"><em>oldpassword</em></span></span></p></td>
<td><p><span data-ttu-id="5b5a5-116">Существующий пароль следует связать с указанным именем <em>пользователя</em> или <em>группы</em> .</span><span class="sxs-lookup"><span data-stu-id="5b5a5-116">The existing password to be associated with the specified <em>user</em> or <em>group</em> name.</span></span></p></td>
</tr>
</tbody>
</table>

