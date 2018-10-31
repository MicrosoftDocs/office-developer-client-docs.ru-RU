---
title: StringFormatEnum (Справочник по для настольных баз данных Access)
TOCTitle: StringFormatEnum
ms:assetid: ab069d67-d983-f390-5d45-876a9f9d9691
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249794(v=office.15)
ms:contentKeyID: 48546964
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 8a3b798fd0d10a3bb2c1c4bd03419a6d506bbf8b
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863040"
---
# <a name="stringformatenum"></a><span data-ttu-id="8db07-102">StringFormatEnum</span><span class="sxs-lookup"><span data-stu-id="8db07-102">StringFormatEnum</span></span>

<span data-ttu-id="8db07-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8db07-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="8db07-104">Задает формат при извлечении [набора записей](recordset-object-ado.md) как строку.</span><span class="sxs-lookup"><span data-stu-id="8db07-104">Specifies the format when retrieving a [Recordset](recordset-object-ado.md) as a string.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8db07-105">Константа</span><span class="sxs-lookup"><span data-stu-id="8db07-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="8db07-106">Значение</span><span class="sxs-lookup"><span data-stu-id="8db07-106">Value</span></span></p></th>
<th><p><span data-ttu-id="8db07-107">Описание</span><span class="sxs-lookup"><span data-stu-id="8db07-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8db07-108"><strong>adClipString</strong></span><span class="sxs-lookup"><span data-stu-id="8db07-108"><strong>adClipString</strong></span></span></p></td>
<td><p><span data-ttu-id="8db07-109">2</span><span class="sxs-lookup"><span data-stu-id="8db07-109">2</span></span></p></td>
<td><p><span data-ttu-id="8db07-110">Разделяет строк по <em>RowDelimiter</em>столбцов по <em>ColumnDelimiter</em>и пустых значений по <em>NullExpr</em>.</span><span class="sxs-lookup"><span data-stu-id="8db07-110">Delimits rows by <em>RowDelimiter</em>, columns by <em>ColumnDelimiter</em>, and null values by <em>NullExpr</em>.</span></span> <span data-ttu-id="8db07-111">Эти три параметра метода <a href="getstring-method-ado.md">GetString</a> являются допустимыми только с <em>StringFormat</em> из <strong>adClipString</strong>.</span><span class="sxs-lookup"><span data-stu-id="8db07-111">These three parameters of the <a href="getstring-method-ado.md">GetString</a> method are valid only with a <em>StringFormat</em> of <strong>adClipString</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="8db07-112">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="8db07-112">ADO/WFC equivalent</span></span>

<span data-ttu-id="8db07-113">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="8db07-113">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8db07-114">Constant</span><span class="sxs-lookup"><span data-stu-id="8db07-114">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8db07-115">AdoEnums.StringFormat.CLIPSTRING</span><span class="sxs-lookup"><span data-stu-id="8db07-115">AdoEnums.StringFormat.CLIPSTRING</span></span></p></td>
</tr>
</tbody>
</table>

