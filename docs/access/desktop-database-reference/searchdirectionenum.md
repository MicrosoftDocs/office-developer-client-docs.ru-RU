---
title: SearchDirectionEnum
TOCTitle: SearchDirectionEnum
ms:assetid: d491000b-47d0-bb28-95ed-7526dbb7c5e9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250064(v=office.15)
ms:contentKeyID: 48547943
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9f9fdf9dd5908b65ae3b6f6ce5a44eba07e4d9bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308808"
---
# <a name="searchdirectionenum"></a><span data-ttu-id="8daf0-102">SearchDirectionEnum</span><span class="sxs-lookup"><span data-stu-id="8daf0-102">SearchDirectionEnum</span></span>


<span data-ttu-id="8daf0-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8daf0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8daf0-104">Задает направление поиска записи в [наборе записей](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="8daf0-104">Specifies the direction of a record search within a [Recordset](recordset-object-ado.md).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8daf0-105">Константа</span><span class="sxs-lookup"><span data-stu-id="8daf0-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="8daf0-106">Значение</span><span class="sxs-lookup"><span data-stu-id="8daf0-106">Value</span></span></p></th>
<th><p><span data-ttu-id="8daf0-107">Описание</span><span class="sxs-lookup"><span data-stu-id="8daf0-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8daf0-108"><strong>Адсеарчбакквард</strong></span><span class="sxs-lookup"><span data-stu-id="8daf0-108"><strong>adSearchBackward</strong></span></span></p></td>
<td><p><span data-ttu-id="8daf0-109">–1</span><span class="sxs-lookup"><span data-stu-id="8daf0-109">-1</span></span></p></td>
<td><p><span data-ttu-id="8daf0-110">Выполняет поиск в обратном направлении, останавливается в начале <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="8daf0-110">Searches backward, stopping at the beginning of the <strong>Recordset</strong>.</span></span> <span data-ttu-id="8daf0-111">Если соответствующее значение не найдено, указатель записи располагается по адресу <a href="bof-eof-properties-ado.md">BOF</a>.</span><span class="sxs-lookup"><span data-stu-id="8daf0-111">If a match is not found, the record pointer is positioned at <a href="bof-eof-properties-ado.md">BOF</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8daf0-112"><strong>Адсеарчфорвард</strong></span><span class="sxs-lookup"><span data-stu-id="8daf0-112"><strong>adSearchForward</strong></span></span></p></td>
<td><p><span data-ttu-id="8daf0-113">1,1</span><span class="sxs-lookup"><span data-stu-id="8daf0-113">1</span></span></p></td>
<td><p><span data-ttu-id="8daf0-114">Выполняет поиск вперед, завершается в конце <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="8daf0-114">Searches forward, stopping at the end of the <strong>Recordset</strong>.</span></span> <span data-ttu-id="8daf0-115">Если соответствующее значение не найдено, указатель записи размещается на <a href="bof-eof-properties-ado.md">EOF</a>.</span><span class="sxs-lookup"><span data-stu-id="8daf0-115">If a match is not found, the record pointer is positioned at <a href="bof-eof-properties-ado.md">EOF</a>.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="8daf0-116">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="8daf0-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="8daf0-117">Пакет: **com. MS. WFC. Data**</span><span class="sxs-lookup"><span data-stu-id="8daf0-117">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8daf0-118">Константа</span><span class="sxs-lookup"><span data-stu-id="8daf0-118">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8daf0-119">Адоенумс. Сеарчдиректион. назад</span><span class="sxs-lookup"><span data-stu-id="8daf0-119">AdoEnums.SearchDirection.BACKWARD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8daf0-120">Адоенумс. Сеарчдиректион. FORWARD</span><span class="sxs-lookup"><span data-stu-id="8daf0-120">AdoEnums.SearchDirection.FORWARD</span></span></p></td>
</tr>
</tbody>
</table>

