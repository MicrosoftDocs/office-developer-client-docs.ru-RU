---
title: RecordStatusEnum Enumeration (DAO)
TOCTitle: RecordStatusEnum Enumeration
ms:assetid: bf4492f2-8d8f-f10f-7a3c-d6296d2ce96b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822784(v=office.15)
ms:contentKeyID: 48547483
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c2d96c359a913660c146f4850a1846554e3b6856
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875121"
---
# <a name="recordstatusenum-enumeration-dao"></a><span data-ttu-id="e6463-102">RecordStatusEnum Enumeration (DAO)</span><span class="sxs-lookup"><span data-stu-id="e6463-102">RecordStatusEnum Enumeration (DAO)</span></span>


<span data-ttu-id="e6463-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e6463-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e6463-104">Используется совместно со свойством **RecordStatus** для указания состояния обновление текущей записи, если он входит в состав пакета обновления.</span><span class="sxs-lookup"><span data-stu-id="e6463-104">Used with the **RecordStatus** property to indicate the update status of the current record if it is part of a batch update.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e6463-105">Имя</span><span class="sxs-lookup"><span data-stu-id="e6463-105">Name</span></span></p></th>
<th><p><span data-ttu-id="e6463-106">Значение</span><span class="sxs-lookup"><span data-stu-id="e6463-106">Value</span></span></p></th>
<th><p><span data-ttu-id="e6463-107">Описание</span><span class="sxs-lookup"><span data-stu-id="e6463-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e6463-108">dbRecordDBDeleted</span><span class="sxs-lookup"><span data-stu-id="e6463-108">dbRecordDBDeleted</span></span></p></td>
<td><p><span data-ttu-id="e6463-109">4</span><span class="sxs-lookup"><span data-stu-id="e6463-109">4</span></span></p></td>
<td><p><span data-ttu-id="e6463-110">Запись была удалена, локально и в базе данных.</span><span class="sxs-lookup"><span data-stu-id="e6463-110">The record has been deleted locally and in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6463-111">dbRecordDeleted</span><span class="sxs-lookup"><span data-stu-id="e6463-111">dbRecordDeleted</span></span></p></td>
<td><p><span data-ttu-id="e6463-112">3</span><span class="sxs-lookup"><span data-stu-id="e6463-112">3</span></span></p></td>
<td><p><span data-ttu-id="e6463-113">Удален, но еще не удалены в базе данных записи.</span><span class="sxs-lookup"><span data-stu-id="e6463-113">The record has been deleted, but not yet deleted in the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6463-114">dbRecordModified</span><span class="sxs-lookup"><span data-stu-id="e6463-114">dbRecordModified</span></span></p></td>
<td><p><span data-ttu-id="e6463-115">1</span><span class="sxs-lookup"><span data-stu-id="e6463-115">1</span></span></p></td>
<td><p><span data-ttu-id="e6463-116">Запись изменения и не обновляются в базе данных.</span><span class="sxs-lookup"><span data-stu-id="e6463-116">The record has been modified and not updated in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6463-117">dbRecordNew</span><span class="sxs-lookup"><span data-stu-id="e6463-117">dbRecordNew</span></span></p></td>
<td><p><span data-ttu-id="e6463-118">2</span><span class="sxs-lookup"><span data-stu-id="e6463-118">2</span></span></p></td>
<td><p><span data-ttu-id="e6463-119">Вставить с помощью метода <strong>AddNew</strong> , но еще не вставлен в базе данных записи.</span><span class="sxs-lookup"><span data-stu-id="e6463-119">The record has been inserted with the <strong>AddNew</strong> method, but not yet inserted into the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6463-120">dbRecordUnmodified</span><span class="sxs-lookup"><span data-stu-id="e6463-120">dbRecordUnmodified</span></span></p></td>
<td><p><span data-ttu-id="e6463-121">0</span><span class="sxs-lookup"><span data-stu-id="e6463-121">0</span></span></p></td>
<td><p><span data-ttu-id="e6463-122">(По умолчанию) Записи не были изменены или успешно обновлены.</span><span class="sxs-lookup"><span data-stu-id="e6463-122">(Default) The record has not been modified or has been updated successfully.</span></span></p></td>
</tr>
</tbody>
</table>

