---
title: Список RecordStatusEnum (DAO)
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
# <a name="recordstatusenum-enumeration-dao"></a><span data-ttu-id="f0659-102">Список RecordStatusEnum (DAO)</span><span class="sxs-lookup"><span data-stu-id="f0659-102">RecordStatusEnum enumeration (DAO)</span></span>


<span data-ttu-id="f0659-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f0659-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f0659-104">Используется со **свойством RecordStatus,** чтобы указать состояние обновления текущей записи, если она является частью пакетного обновления.</span><span class="sxs-lookup"><span data-stu-id="f0659-104">Used with the **RecordStatus** property to indicate the update status of the current record if it is part of a batch update.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f0659-105">Имя</span><span class="sxs-lookup"><span data-stu-id="f0659-105">Name</span></span></p></th>
<th><p><span data-ttu-id="f0659-106">Значение</span><span class="sxs-lookup"><span data-stu-id="f0659-106">Value</span></span></p></th>
<th><p><span data-ttu-id="f0659-107">Описание</span><span class="sxs-lookup"><span data-stu-id="f0659-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f0659-108">dbRecordDBDeleted</span><span class="sxs-lookup"><span data-stu-id="f0659-108">dbRecordDBDeleted</span></span></p></td>
<td><p><span data-ttu-id="f0659-109">4 </span><span class="sxs-lookup"><span data-stu-id="f0659-109">4</span></span></p></td>
<td><p><span data-ttu-id="f0659-110">Запись удалена локально и в базе данных.</span><span class="sxs-lookup"><span data-stu-id="f0659-110">The record has been deleted locally and in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f0659-111">dbRecordDeleted</span><span class="sxs-lookup"><span data-stu-id="f0659-111">dbRecordDeleted</span></span></p></td>
<td><p><span data-ttu-id="f0659-112">3 </span><span class="sxs-lookup"><span data-stu-id="f0659-112">3</span></span></p></td>
<td><p><span data-ttu-id="f0659-113">Запись была удалена, но еще не удалена в базе данных.</span><span class="sxs-lookup"><span data-stu-id="f0659-113">The record has been deleted, but not yet deleted in the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f0659-114">dbRecordModified</span><span class="sxs-lookup"><span data-stu-id="f0659-114">dbRecordModified</span></span></p></td>
<td><p><span data-ttu-id="f0659-115">1 </span><span class="sxs-lookup"><span data-stu-id="f0659-115">1</span></span></p></td>
<td><p><span data-ttu-id="f0659-116">Запись была изменена и не обновлена в базе данных.</span><span class="sxs-lookup"><span data-stu-id="f0659-116">The record has been modified and not updated in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f0659-117">dbRecordNew</span><span class="sxs-lookup"><span data-stu-id="f0659-117">dbRecordNew</span></span></p></td>
<td><p><span data-ttu-id="f0659-118">2 </span><span class="sxs-lookup"><span data-stu-id="f0659-118">2</span></span></p></td>
<td><p><span data-ttu-id="f0659-119">Запись была вставлена с помощью метода <strong>AddNew,</strong> но еще не вставлена в базу данных.</span><span class="sxs-lookup"><span data-stu-id="f0659-119">The record has been inserted with the <strong>AddNew</strong> method, but not yet inserted into the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f0659-120">dbRecordUnmodified</span><span class="sxs-lookup"><span data-stu-id="f0659-120">dbRecordUnmodified</span></span></p></td>
<td><p><span data-ttu-id="f0659-121">0</span><span class="sxs-lookup"><span data-stu-id="f0659-121">0</span></span></p></td>
<td><p><span data-ttu-id="f0659-122">(По умолчанию) Запись не была изменена или успешно обновлена.</span><span class="sxs-lookup"><span data-stu-id="f0659-122">(Default) The record has not been modified or has been updated successfully.</span></span></p></td>
</tr>
</tbody>
</table>

