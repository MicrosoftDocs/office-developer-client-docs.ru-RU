---
title: Коды ошибок служб IIS
TOCTitle: Internet Information Services error codes
ms:assetid: 1ed57b89-b471-88e5-e5af-85323dec18d3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248978(v=office.15)
ms:contentKeyID: 48543625
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8c67c43922316c6c77876525c79993beba1d4131
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291281"
---
# <a name="internet-information-services-error-codes"></a><span data-ttu-id="64736-102">Коды ошибок служб IIS</span><span class="sxs-lookup"><span data-stu-id="64736-102">Internet Information Services error codes</span></span>

<span data-ttu-id="64736-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="64736-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="64736-104">В следующей таблице перечислены коды ошибок служб IIS, связанные с использованием удаленной службы данных.</span><span class="sxs-lookup"><span data-stu-id="64736-104">The following table lists Microsoft Internet Information Services (IIS) error codes related to Remote Data Service usage.</span></span> <span data-ttu-id="64736-105">При положительном десятичном преобразовании двух нижних байтов отображается отрицательный десятичный перевод полного кода ошибки и шестнадцатеричные значения.</span><span class="sxs-lookup"><span data-stu-id="64736-105">The positive decimal translation of the low two bytes, the negative decimal translation of the full error code, and the hexadecimal values are shown.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="64736-106">Ошибки служб IIS</span><span class="sxs-lookup"><span data-stu-id="64736-106">Internet Information Services errors</span></span></p></th>
<th><p><span data-ttu-id="64736-107">Номер</span><span class="sxs-lookup"><span data-stu-id="64736-107">Number</span></span></p></th>
<th><p><span data-ttu-id="64736-108">Описание</span><span class="sxs-lookup"><span data-stu-id="64736-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="64736-109"><strong>IDS_IIS_AccessDenied</strong></span><span class="sxs-lookup"><span data-stu-id="64736-109"><strong>IDS_IIS_AccessDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="64736-110">8208</span><span class="sxs-lookup"><span data-stu-id="64736-110">8208</span></span><br />
<span data-ttu-id="64736-111">— 2146820080</span><span class="sxs-lookup"><span data-stu-id="64736-111">-2146820080</span></span><br />
<span data-ttu-id="64736-112">0x800A2010</span><span class="sxs-lookup"><span data-stu-id="64736-112">0x800A2010</span></span></p></td>
<td><p><span data-ttu-id="64736-113">Ошибка сервера Интернета: доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="64736-113">Internet Server Error: Access Denied.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64736-114"><strong>IDS_IIS_ObjectNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="64736-114"><strong>IDS_IIS_ObjectNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="64736-115">8209</span><span class="sxs-lookup"><span data-stu-id="64736-115">8209</span></span><br />
<span data-ttu-id="64736-116">— 2146820079</span><span class="sxs-lookup"><span data-stu-id="64736-116">-2146820079</span></span><br />
<span data-ttu-id="64736-117">0x800A2011</span><span class="sxs-lookup"><span data-stu-id="64736-117">0x800A2011</span></span></p></td>
<td><p><span data-ttu-id="64736-118">Ошибка Интернет-сервера: объект или модуль не найден.</span><span class="sxs-lookup"><span data-stu-id="64736-118">Internet Server Error: Object/module not found.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64736-119"><strong>IDS_IIS_RequestForbidden</strong></span><span class="sxs-lookup"><span data-stu-id="64736-119"><strong>IDS_IIS_RequestForbidden</strong></span></span></p></td>
<td><p><span data-ttu-id="64736-120">8210</span><span class="sxs-lookup"><span data-stu-id="64736-120">8210</span></span><br />
<span data-ttu-id="64736-121">— 2146820078</span><span class="sxs-lookup"><span data-stu-id="64736-121">-2146820078</span></span><br />
<span data-ttu-id="64736-122">0x800A2012</span><span class="sxs-lookup"><span data-stu-id="64736-122">0x800A2012</span></span></p></td>
<td><p><span data-ttu-id="64736-123">Ошибка сервера Интернета: запрос запрещен.</span><span class="sxs-lookup"><span data-stu-id="64736-123">Internet Server Error: Request Forbidden.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64736-124"><strong>IDS_IIS_UnexpectedError</strong></span><span class="sxs-lookup"><span data-stu-id="64736-124"><strong>IDS_IIS_UnexpectedError</strong></span></span></p></td>
<td><p><span data-ttu-id="64736-125">8447</span><span class="sxs-lookup"><span data-stu-id="64736-125">8447</span></span><br />
<span data-ttu-id="64736-126">— 2146819841</span><span class="sxs-lookup"><span data-stu-id="64736-126">-2146819841</span></span><br />
<span data-ttu-id="64736-127">0x800A20FF</span><span class="sxs-lookup"><span data-stu-id="64736-127">0x800A20FF</span></span></p></td>
<td><p><span data-ttu-id="64736-128">Ошибка Интернет сервера.</span><span class="sxs-lookup"><span data-stu-id="64736-128">Internet Server Error.</span></span></p></td>
</tr>
</tbody>
</table>

