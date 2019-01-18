---
title: PositionEnum (Справочник по для настольных баз данных Access)
TOCTitle: PositionEnum
ms:assetid: 2a6f294b-74f2-b951-e32a-79ff5e782204
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249054(v=office.15)
ms:contentKeyID: 48543907
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4c791cbd31e346eef5ab8503cb55b0dec5e9fbbc
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702840"
---
# <a name="positionenum"></a><span data-ttu-id="cb418-102">PositionEnum</span><span class="sxs-lookup"><span data-stu-id="cb418-102">PositionEnum</span></span>

<span data-ttu-id="cb418-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cb418-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cb418-104">Указывает текущую позицию указателя записи в наборе [записей](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="cb418-104">Specifies the current position of the record pointer within a [Recordset](recordset-object-ado.md).</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cb418-105">Константа</span><span class="sxs-lookup"><span data-stu-id="cb418-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="cb418-106">Значение</span><span class="sxs-lookup"><span data-stu-id="cb418-106">Value</span></span></p></th>
<th><p><span data-ttu-id="cb418-107">Описание</span><span class="sxs-lookup"><span data-stu-id="cb418-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cb418-108"><strong>adPosBOF</strong></span><span class="sxs-lookup"><span data-stu-id="cb418-108"><strong>adPosBOF</strong></span></span></p></td>
<td><p><span data-ttu-id="cb418-109">–2</span><span class="sxs-lookup"><span data-stu-id="cb418-109">-2</span></span></p></td>
<td><p><span data-ttu-id="cb418-110">Указывает, что указатель текущей записи BOF (то есть, свойство <a href="bof-eof-properties-ado.md">BOF</a> имеет <strong>значение True</strong>).</span><span class="sxs-lookup"><span data-stu-id="cb418-110">Indicates that the current record pointer is at BOF (that is, the <a href="bof-eof-properties-ado.md">BOF</a> property is <strong>True</strong>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb418-111"><strong>adPosEOF</strong></span><span class="sxs-lookup"><span data-stu-id="cb418-111"><strong>adPosEOF</strong></span></span></p></td>
<td><p><span data-ttu-id="cb418-112">–3</span><span class="sxs-lookup"><span data-stu-id="cb418-112">-3</span></span></p></td>
<td><p><span data-ttu-id="cb418-113">Указывает, что указатель текущей записи в конец файла (то есть, свойство <a href="bof-eof-properties-ado.md">EOF</a> имеет <strong>значение True</strong>).</span><span class="sxs-lookup"><span data-stu-id="cb418-113">Indicates that the current record pointer is at EOF (that is, the <a href="bof-eof-properties-ado.md">EOF</a> property is <strong>True</strong>).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb418-114"><strong>adPosUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="cb418-114"><strong>adPosUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="cb418-115">–1</span><span class="sxs-lookup"><span data-stu-id="cb418-115">-1</span></span></p></td>
<td><p><span data-ttu-id="cb418-116">Показывает, что <strong>записей</strong> пуст, текущей позиции не известен, или поставщик не поддерживает свойство <a href="absolutepage-property-ado.md">AbsolutePage</a> или <a href="absoluteposition-property-ado.md">AbsolutePosition</a> .</span><span class="sxs-lookup"><span data-stu-id="cb418-116">Indicates that the <strong>Recordset</strong> is empty, the current position is unknown, or the provider does not support the <a href="absolutepage-property-ado.md">AbsolutePage</a> or <a href="absoluteposition-property-ado.md">AbsolutePosition</a> property.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="cb418-117">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="cb418-117">ADO/WFC equivalent</span></span>

<span data-ttu-id="cb418-118">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="cb418-118">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cb418-119">Константа</span><span class="sxs-lookup"><span data-stu-id="cb418-119">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cb418-120">AdoEnums.Position.BOF</span><span class="sxs-lookup"><span data-stu-id="cb418-120">AdoEnums.Position.BOF</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb418-121">AdoEnums.Position.EOF</span><span class="sxs-lookup"><span data-stu-id="cb418-121">AdoEnums.Position.EOF</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb418-122">AdoEnums.Position.UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="cb418-122">AdoEnums.Position.UNKNOWN</span></span></p></td>
</tr>
</tbody>
</table>

