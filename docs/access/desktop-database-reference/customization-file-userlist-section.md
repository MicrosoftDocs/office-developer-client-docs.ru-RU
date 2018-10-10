---
title: Customization File UserList Section
TOCTitle: Customization File UserList Section
ms:assetid: b60ba3b0-37d4-bb59-d3cd-2ab44d178b8a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249873(v=office.15)
ms:contentKeyID: 48547263
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a14060858ad5cd90b410319a515eb271b2b397ea
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481910"
---
# <a name="customization-file-userlist-section"></a><span data-ttu-id="24609-102">Customization File UserList Section</span><span class="sxs-lookup"><span data-stu-id="24609-102">Customization File UserList Section</span></span>


<span data-ttu-id="24609-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="24609-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="24609-104">В разделе **userlist** относится к раздел **подключиться** с того же параметра *идентификатор* раздела.</span><span class="sxs-lookup"><span data-stu-id="24609-104">The **userlist** section pertains to the **connect** section with the same section *identifier* parameter.</span></span>

<span data-ttu-id="24609-105">В этом разделе может содержать с *доступом пользователя*, которая определяет права доступа для указанного пользователя и переопределяет *по умолчанию* *доступом* в соответствующий раздел **подключение** .</span><span class="sxs-lookup"><span data-stu-id="24609-105">This section can contain a *user access entry*, which specifies access rights for the specified user and overrides the *default* *access entry* in the matching **connect** section.</span></span>

## <a name="syntax"></a><span data-ttu-id="24609-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="24609-106">Syntax</span></span>

<span data-ttu-id="24609-107">Запись доступом пользователей имеет форму:</span><span class="sxs-lookup"><span data-stu-id="24609-107">A user access entry is of the form:</span></span>

<span data-ttu-id="24609-108">*имя пользователя \*\*\* =* accessRights \*\*\*</span><span class="sxs-lookup"><span data-stu-id="24609-108">*userName\*\*\*=* accessRights\*\*\*</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="24609-109">Часть</span><span class="sxs-lookup"><span data-stu-id="24609-109">Part</span></span></p></th>
<th><p><span data-ttu-id="24609-110">Описание</span><span class="sxs-lookup"><span data-stu-id="24609-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="24609-111"><em>userName</em></span><span class="sxs-lookup"><span data-stu-id="24609-111"><em>userName</em></span></span></p></td>
<td><p><span data-ttu-id="24609-112"><em>Имя пользователя</em> человека, используя это подключение.</span><span class="sxs-lookup"><span data-stu-id="24609-112">The <em>user name</em> of the person employing this connection.</span></span> <span data-ttu-id="24609-113">Диалоговое окно служб IIS <strong>Manager службы</strong> устанавливаются имен пользователей.</span><span class="sxs-lookup"><span data-stu-id="24609-113">Valid user names are established with the IIS <strong>Service Manager</strong> dialog.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24609-114"><strong><em>accessRights</em></strong></span><span class="sxs-lookup"><span data-stu-id="24609-114"><strong><em>accessRights</em></strong></span></span></p></td>
<td><p><span data-ttu-id="24609-115">Один из следующих прав доступа.</span><span class="sxs-lookup"><span data-stu-id="24609-115">One of the following access rights:</span></span><br />
</p>
<ul>
<li><p><span data-ttu-id="24609-116"><strong>NoAccess</strong> — пользователь не может получить доступ к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="24609-116"><strong>NoAccess</strong> — User cannot access the data source.</span></span></p></li>
<li><p><span data-ttu-id="24609-117"><strong>ReadOnly</strong> — пользователи могут читать источника данных.</span><span class="sxs-lookup"><span data-stu-id="24609-117"><strong>ReadOnly</strong> — User can read the data source.</span></span></p></li>
<li><p><span data-ttu-id="24609-118"><strong>ReadWrite</strong> — пользователь может чтение или запись в источник данных.</span><span class="sxs-lookup"><span data-stu-id="24609-118"><strong>ReadWrite</strong> — User can read or write to the data source.</span></span></p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>

