---
title: Раздел UserList в файле настройки
TOCTitle: Customization File UserList section
ms:assetid: b60ba3b0-37d4-bb59-d3cd-2ab44d178b8a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249873(v=office.15)
ms:contentKeyID: 48547263
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ecaf77765051a202925449d0221f0a68a2a06622
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295158"
---
# <a name="customization-file-userlist-section"></a><span data-ttu-id="df046-102">Раздел UserList в файле настройки</span><span class="sxs-lookup"><span data-stu-id="df046-102">Customization File UserList section</span></span>


<span data-ttu-id="df046-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="df046-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="df046-104">Раздел **списка пользователей** относится к разделу **connect** с тем же параметром *идентификатора* раздела.</span><span class="sxs-lookup"><span data-stu-id="df046-104">The **userlist** section pertains to the **connect** section with the same section *identifier* parameter.</span></span>

<span data-ttu-id="df046-105">В этом разделе может содержаться запись доступа *пользователя,* которая указывает права   доступа для указанного пользователя и переопределяет запись доступа по умолчанию в разделе подключения, **совпадающих.**</span><span class="sxs-lookup"><span data-stu-id="df046-105">This section can contain a *user access entry*, which specifies access rights for the specified user and overrides the *default* *access entry* in the matching **connect** section.</span></span>

## <a name="syntax"></a><span data-ttu-id="df046-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="df046-106">Syntax</span></span>

<span data-ttu-id="df046-107">Запись доступа пользователя имеет форму:</span><span class="sxs-lookup"><span data-stu-id="df046-107">A user access entry is of the form:</span></span>

<span data-ttu-id="df046-108">*userName\*\*\*=* accessRights\*\*\*</span><span class="sxs-lookup"><span data-stu-id="df046-108">*userName\*\*\*=* accessRights\*\*\*</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="df046-109">Часть</span><span class="sxs-lookup"><span data-stu-id="df046-109">Part</span></span></p></th>
<th><p><span data-ttu-id="df046-110">Описание</span><span class="sxs-lookup"><span data-stu-id="df046-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="df046-111"><em>userName</em></span><span class="sxs-lookup"><span data-stu-id="df046-111"><em>userName</em></span></span></p></td>
<td><p><span data-ttu-id="df046-112">Имя <em>пользователя,</em> применяющий это подключение.</span><span class="sxs-lookup"><span data-stu-id="df046-112">The <em>user name</em> of the person employing this connection.</span></span> <span data-ttu-id="df046-113">Допустимые имена пользователей устанавливаются в диалоговом оке "Диспетчер <strong>служб</strong> IIS".</span><span class="sxs-lookup"><span data-stu-id="df046-113">Valid user names are established with the IIS <strong>Service Manager</strong> dialog.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df046-114"><strong><em>accessRights</em></strong></span><span class="sxs-lookup"><span data-stu-id="df046-114"><strong><em>accessRights</em></strong></span></span></p></td>
<td><p><span data-ttu-id="df046-115">Одно из следующих прав доступа:</span><span class="sxs-lookup"><span data-stu-id="df046-115">One of the following access rights:</span></span><br />
</p>
<ul>
<li><p><span data-ttu-id="df046-116"><strong>NoAccess</strong> — пользователь не может получить доступ к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="df046-116"><strong>NoAccess</strong> — User cannot access the data source.</span></span></p></li>
<li><p><span data-ttu-id="df046-117"><strong>ReadOnly</strong> — пользователь может читать источник данных.</span><span class="sxs-lookup"><span data-stu-id="df046-117"><strong>ReadOnly</strong> — User can read the data source.</span></span></p></li>
<li><p><span data-ttu-id="df046-118"><strong>ReadWrite</strong> — пользователь может читать или записывать данные в источник данных.</span><span class="sxs-lookup"><span data-stu-id="df046-118"><strong>ReadWrite</strong> — User can read or write to the data source.</span></span></p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>

