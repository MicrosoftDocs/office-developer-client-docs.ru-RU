---
title: StringFormatEnum (справочник по базе данных Access для настольных ПК)
TOCTitle: StringFormatEnum
ms:assetid: ab069d67-d983-f390-5d45-876a9f9d9691
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249794(v=office.15)
ms:contentKeyID: 48546964
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 89eb3e9c972b19bc9908f29ce5ec5e42c8974d54
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314464"
---
# <a name="stringformatenum"></a><span data-ttu-id="18590-102">StringFormatEnum</span><span class="sxs-lookup"><span data-stu-id="18590-102">StringFormatEnum</span></span>

<span data-ttu-id="18590-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="18590-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="18590-104">Указывает формат при искомом наборе [записей в](recordset-object-ado.md) виде строки.</span><span class="sxs-lookup"><span data-stu-id="18590-104">Specifies the format when retrieving a [Recordset](recordset-object-ado.md) as a string.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="18590-105">Константа</span><span class="sxs-lookup"><span data-stu-id="18590-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="18590-106">Значение</span><span class="sxs-lookup"><span data-stu-id="18590-106">Value</span></span></p></th>
<th><p><span data-ttu-id="18590-107">Описание</span><span class="sxs-lookup"><span data-stu-id="18590-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="18590-108"><strong>adClipString</strong></span><span class="sxs-lookup"><span data-stu-id="18590-108"><strong>adClipString</strong></span></span></p></td>
<td><p><span data-ttu-id="18590-109">2 </span><span class="sxs-lookup"><span data-stu-id="18590-109">2</span></span></p></td>
<td><p><span data-ttu-id="18590-110">Делегировка строк <em>по RowDelimiter,</em>столбцов <em>по ColumnDelimiter</em>и значений <em>null по NullExpr</em>.</span><span class="sxs-lookup"><span data-stu-id="18590-110">Delimits rows by <em>RowDelimiter</em>, columns by <em>ColumnDelimiter</em>, and null values by <em>NullExpr</em>.</span></span> <span data-ttu-id="18590-111">Эти три параметра метода <a href="getstring-method-ado.md">GetString</a> действительны только с помощью <em>StringFormat</em> <strong>adClipString.</strong></span><span class="sxs-lookup"><span data-stu-id="18590-111">These three parameters of the <a href="getstring-method-ado.md">GetString</a> method are valid only with a <em>StringFormat</em> of <strong>adClipString</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="18590-112">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="18590-112">ADO/WFC equivalent</span></span>

<span data-ttu-id="18590-113">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="18590-113">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="18590-114">Константа</span><span class="sxs-lookup"><span data-stu-id="18590-114">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="18590-115">AdoEnums.StringFormat.CLIPSTRING</span><span class="sxs-lookup"><span data-stu-id="18590-115">AdoEnums.StringFormat.CLIPSTRING</span></span></p></td>
</tr>
</tbody>
</table>

