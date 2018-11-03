---
title: Перечисление UpdateTypeEnum (DAO)
TOCTitle: UpdateTypeEnum Enumeration
ms:assetid: 7ac38bae-27fc-f3d0-5b75-569bce547954
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196186(v=office.15)
ms:contentKeyID: 48545800
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d38cf4554837c9c6434b7607746f2c40836ac950
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944622"
---
# <a name="updatetypeenum-enumeration-dao"></a><span data-ttu-id="66435-102">Перечисление UpdateTypeEnum (DAO)</span><span class="sxs-lookup"><span data-stu-id="66435-102">UpdateTypeEnum enumeration (DAO)</span></span>


<span data-ttu-id="66435-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="66435-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="66435-104">Используется с методом **обновления** для указания необходимых обновлений для записи на диск.</span><span class="sxs-lookup"><span data-stu-id="66435-104">Used with the **Update** method to specify which updates to write to disk.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="66435-105">Имя</span><span class="sxs-lookup"><span data-stu-id="66435-105">Name</span></span></p></th>
<th><p><span data-ttu-id="66435-106">Значение</span><span class="sxs-lookup"><span data-stu-id="66435-106">Value</span></span></p></th>
<th><p><span data-ttu-id="66435-107">Описание</span><span class="sxs-lookup"><span data-stu-id="66435-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="66435-108">dbUpdateBatch</span><span class="sxs-lookup"><span data-stu-id="66435-108">dbUpdateBatch</span></span></p></td>
<td><p><span data-ttu-id="66435-109">4</span><span class="sxs-lookup"><span data-stu-id="66435-109">4</span></span></p></td>
<td><p><span data-ttu-id="66435-110">Все ожидающие изменения в кэше обновления записываются на диск.</span><span class="sxs-lookup"><span data-stu-id="66435-110">All pending changes in the update cache are written to disk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66435-111">dbUpdateCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="66435-111">dbUpdateCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="66435-112">2</span><span class="sxs-lookup"><span data-stu-id="66435-112">2</span></span></p></td>
<td><p><span data-ttu-id="66435-113">Только для текущей записи ожидающие изменения записываются на диск.</span><span class="sxs-lookup"><span data-stu-id="66435-113">Only the current record's pending changes are written to disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66435-114">dbUpdateRegular</span><span class="sxs-lookup"><span data-stu-id="66435-114">dbUpdateRegular</span></span></p></td>
<td><p><span data-ttu-id="66435-115">1</span><span class="sxs-lookup"><span data-stu-id="66435-115">1</span></span></p></td>
<td><p><span data-ttu-id="66435-116">(По умолчанию) Отложенные изменения не кэшируются и записи на диск немедленно.</span><span class="sxs-lookup"><span data-stu-id="66435-116">(Default) Pending changes are not cached and are written to disk immediately.</span></span></p></td>
</tr>
</tbody>
</table>

