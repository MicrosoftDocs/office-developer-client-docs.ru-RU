---
title: StringFormatEnum (Справочник по для настольных баз данных Access)
TOCTitle: StringFormatEnum
ms:assetid: ab069d67-d983-f390-5d45-876a9f9d9691
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249794(v=office.15)
ms:contentKeyID: 48546964
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7814b15c75cfd1dbd48c793ee8c30cc2c5348ec9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480881"
---
# <a name="stringformatenum"></a><span data-ttu-id="e8d86-102">StringFormatEnum</span><span class="sxs-lookup"><span data-stu-id="e8d86-102">StringFormatEnum</span></span>


<span data-ttu-id="e8d86-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e8d86-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e8d86-104">Задает формат при извлечении [набора записей](recordset-object-ado.md) как строку.</span><span class="sxs-lookup"><span data-stu-id="e8d86-104">Specifies the format when retrieving a [Recordset](recordset-object-ado.md) as a string.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e8d86-105">Константа</span><span class="sxs-lookup"><span data-stu-id="e8d86-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="e8d86-106">Значение</span><span class="sxs-lookup"><span data-stu-id="e8d86-106">Value</span></span></p></th>
<th><p><span data-ttu-id="e8d86-107">Описание</span><span class="sxs-lookup"><span data-stu-id="e8d86-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e8d86-108"><strong>adClipString</strong></span><span class="sxs-lookup"><span data-stu-id="e8d86-108"><strong>adClipString</strong></span></span></p></td>
<td><p><span data-ttu-id="e8d86-109">2</span><span class="sxs-lookup"><span data-stu-id="e8d86-109">2</span></span></p></td>
<td><p><span data-ttu-id="e8d86-110">Разделяет строк по <em>RowDelimiter</em>столбцов по <em>ColumnDelimiter</em>и пустых значений по <em>NullExpr</em>.</span><span class="sxs-lookup"><span data-stu-id="e8d86-110">Delimits rows by <em>RowDelimiter</em>, columns by <em>ColumnDelimiter</em>, and null values by <em>NullExpr</em>.</span></span> <span data-ttu-id="e8d86-111">Эти три параметра метода <a href="getstring-method-ado.md">GetString</a> являются допустимыми только с <em>StringFormat</em> из <strong>adClipString</strong>.</span><span class="sxs-lookup"><span data-stu-id="e8d86-111">These three parameters of the <a href="getstring-method-ado.md">GetString</a> method are valid only with a <em>StringFormat</em> of <strong>adClipString</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e8d86-112">**Эквивалент ADO/WFC**</span><span class="sxs-lookup"><span data-stu-id="e8d86-112">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="e8d86-113">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="e8d86-113">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e8d86-114">Constant</span><span class="sxs-lookup"><span data-stu-id="e8d86-114">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e8d86-115">AdoEnums.StringFormat.CLIPSTRING</span><span class="sxs-lookup"><span data-stu-id="e8d86-115">AdoEnums.StringFormat.CLIPSTRING</span></span></p></td>
</tr>
</tbody>
</table>

