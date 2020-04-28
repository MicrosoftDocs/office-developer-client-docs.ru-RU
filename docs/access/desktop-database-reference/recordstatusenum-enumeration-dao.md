---
title: Перечисление RecordStatusEnum (DAO)
TOCTitle: RecordStatusEnum Enumeration
ms:assetid: bf4492f2-8d8f-f10f-7a3c-d6296d2ce96b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822784(v=office.15)
ms:contentKeyID: 48547483
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: eb7bffaf91db9e1170702d2e36393da669dbe0c6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309236"
---
# <a name="recordstatusenum-enumeration-dao"></a><span data-ttu-id="71e0c-102">Перечисление RecordStatusEnum (DAO)</span><span class="sxs-lookup"><span data-stu-id="71e0c-102">RecordStatusEnum enumeration (DAO)</span></span>


<span data-ttu-id="71e0c-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="71e0c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="71e0c-104">Используется вместе со свойством **рекордстатус** , чтобы указать состояние обновления текущей записи, если она является частью пакетного обновления.</span><span class="sxs-lookup"><span data-stu-id="71e0c-104">Used with the **RecordStatus** property to indicate the update status of the current record if it is part of a batch update.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="71e0c-105">Имя</span><span class="sxs-lookup"><span data-stu-id="71e0c-105">Name</span></span></p></th>
<th><p><span data-ttu-id="71e0c-106">Значение</span><span class="sxs-lookup"><span data-stu-id="71e0c-106">Value</span></span></p></th>
<th><p><span data-ttu-id="71e0c-107">Описание</span><span class="sxs-lookup"><span data-stu-id="71e0c-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="71e0c-108">дбрекорддбделетед</span><span class="sxs-lookup"><span data-stu-id="71e0c-108">dbRecordDBDeleted</span></span></p></td>
<td><p><span data-ttu-id="71e0c-109">4 </span><span class="sxs-lookup"><span data-stu-id="71e0c-109">4</span></span></p></td>
<td><p><span data-ttu-id="71e0c-110">Запись удалена на локальном компьютере и в базе данных.</span><span class="sxs-lookup"><span data-stu-id="71e0c-110">The record has been deleted locally and in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71e0c-111">дбрекордделетед</span><span class="sxs-lookup"><span data-stu-id="71e0c-111">dbRecordDeleted</span></span></p></td>
<td><p><span data-ttu-id="71e0c-112">4</span><span class="sxs-lookup"><span data-stu-id="71e0c-112">3</span></span></p></td>
<td><p><span data-ttu-id="71e0c-113">Запись была удалена, но еще не удалена в базе данных.</span><span class="sxs-lookup"><span data-stu-id="71e0c-113">The record has been deleted, but not yet deleted in the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71e0c-114">дбрекордмодифиед</span><span class="sxs-lookup"><span data-stu-id="71e0c-114">dbRecordModified</span></span></p></td>
<td><p><span data-ttu-id="71e0c-115">1,1</span><span class="sxs-lookup"><span data-stu-id="71e0c-115">1</span></span></p></td>
<td><p><span data-ttu-id="71e0c-116">Запись изменена и не обновлена в базе данных.</span><span class="sxs-lookup"><span data-stu-id="71e0c-116">The record has been modified and not updated in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71e0c-117">дбрекорднев</span><span class="sxs-lookup"><span data-stu-id="71e0c-117">dbRecordNew</span></span></p></td>
<td><p><span data-ttu-id="71e0c-118">2</span><span class="sxs-lookup"><span data-stu-id="71e0c-118">2</span></span></p></td>
<td><p><span data-ttu-id="71e0c-119">Запись была вставлена с помощью метода <strong>AddNew</strong> , но еще не вставлена в базу данных.</span><span class="sxs-lookup"><span data-stu-id="71e0c-119">The record has been inserted with the <strong>AddNew</strong> method, but not yet inserted into the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71e0c-120">дбрекордунмодифиед</span><span class="sxs-lookup"><span data-stu-id="71e0c-120">dbRecordUnmodified</span></span></p></td>
<td><p><span data-ttu-id="71e0c-121">нуль</span><span class="sxs-lookup"><span data-stu-id="71e0c-121">0</span></span></p></td>
<td><p><span data-ttu-id="71e0c-122">Умолчани Запись не была изменена или была успешно обновлена.</span><span class="sxs-lookup"><span data-stu-id="71e0c-122">(Default) The record has not been modified or has been updated successfully.</span></span></p></td>
</tr>
</tbody>
</table>

