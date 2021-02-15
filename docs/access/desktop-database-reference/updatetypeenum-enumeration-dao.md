---
title: Enumeration UpdateTypeEnum (DAO)
TOCTitle: UpdateTypeEnum Enumeration
ms:assetid: 7ac38bae-27fc-f3d0-5b75-569bce547954
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196186(v=office.15)
ms:contentKeyID: 48545800
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d1e4ecbc216ab4a00dabd85f623bc134772dfd4c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306190"
---
# <a name="updatetypeenum-enumeration-dao"></a><span data-ttu-id="deecc-102">Enumeration UpdateTypeEnum (DAO)</span><span class="sxs-lookup"><span data-stu-id="deecc-102">UpdateTypeEnum enumeration (DAO)</span></span>


<span data-ttu-id="deecc-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="deecc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="deecc-104">Используется вместе с **методом Update** для указания обновлений для записи на диск.</span><span class="sxs-lookup"><span data-stu-id="deecc-104">Used with the **Update** method to specify which updates to write to disk.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="deecc-105">Имя</span><span class="sxs-lookup"><span data-stu-id="deecc-105">Name</span></span></p></th>
<th><p><span data-ttu-id="deecc-106">Значение</span><span class="sxs-lookup"><span data-stu-id="deecc-106">Value</span></span></p></th>
<th><p><span data-ttu-id="deecc-107">Описание</span><span class="sxs-lookup"><span data-stu-id="deecc-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="deecc-108">dbUpdateBatch</span><span class="sxs-lookup"><span data-stu-id="deecc-108">dbUpdateBatch</span></span></p></td>
<td><p><span data-ttu-id="deecc-109">4 </span><span class="sxs-lookup"><span data-stu-id="deecc-109">4</span></span></p></td>
<td><p><span data-ttu-id="deecc-110">Все ожидающих изменений в кэше обновлений записаны на диск.</span><span class="sxs-lookup"><span data-stu-id="deecc-110">All pending changes in the update cache are written to disk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="deecc-111">dbUpdateCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="deecc-111">dbUpdateCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="deecc-112">2 </span><span class="sxs-lookup"><span data-stu-id="deecc-112">2</span></span></p></td>
<td><p><span data-ttu-id="deecc-113">На диск записывают только ожидающих изменений текущей записи.</span><span class="sxs-lookup"><span data-stu-id="deecc-113">Only the current record's pending changes are written to disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="deecc-114">dbUpdateRegular</span><span class="sxs-lookup"><span data-stu-id="deecc-114">dbUpdateRegular</span></span></p></td>
<td><p><span data-ttu-id="deecc-115">1 </span><span class="sxs-lookup"><span data-stu-id="deecc-115">1</span></span></p></td>
<td><p><span data-ttu-id="deecc-116">(По умолчанию) Ожидающих изменений не кэшировали и сразу же записаны на диск.</span><span class="sxs-lookup"><span data-stu-id="deecc-116">(Default) Pending changes are not cached and are written to disk immediately.</span></span></p></td>
</tr>
</tbody>
</table>

