---
title: PositionEnum (Ссылка на настольные базы данных)
TOCTitle: PositionEnum
ms:assetid: 2a6f294b-74f2-b951-e32a-79ff5e782204
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249054(v=office.15)
ms:contentKeyID: 48543907
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4c791cbd31e346eef5ab8503cb55b0dec5e9fbbc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287505"
---
# <a name="positionenum"></a><span data-ttu-id="c13f8-102">PositionEnum</span><span class="sxs-lookup"><span data-stu-id="c13f8-102">PositionEnum</span></span>

<span data-ttu-id="c13f8-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c13f8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c13f8-104">Указывает текущее положение указателя записи в [Наборе записей.](recordset-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="c13f8-104">Specifies the current position of the record pointer within a [Recordset](recordset-object-ado.md).</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c13f8-105">Константа</span><span class="sxs-lookup"><span data-stu-id="c13f8-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="c13f8-106">Значение</span><span class="sxs-lookup"><span data-stu-id="c13f8-106">Value</span></span></p></th>
<th><p><span data-ttu-id="c13f8-107">Описание</span><span class="sxs-lookup"><span data-stu-id="c13f8-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c13f8-108"><strong>adPosBOF</strong></span><span class="sxs-lookup"><span data-stu-id="c13f8-108"><strong>adPosBOF</strong></span></span></p></td>
<td><p><span data-ttu-id="c13f8-109">–2</span><span class="sxs-lookup"><span data-stu-id="c13f8-109">-2</span></span></p></td>
<td><p><span data-ttu-id="c13f8-110">Указывает, что текущий указатель записи находится в BOF (то есть свойство <a href="bof-eof-properties-ado.md">BOF</a> <strong>true).</strong></span><span class="sxs-lookup"><span data-stu-id="c13f8-110">Indicates that the current record pointer is at BOF (that is, the <a href="bof-eof-properties-ado.md">BOF</a> property is <strong>True</strong>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c13f8-111"><strong>adPosEOF</strong></span><span class="sxs-lookup"><span data-stu-id="c13f8-111"><strong>adPosEOF</strong></span></span></p></td>
<td><p><span data-ttu-id="c13f8-112">–3</span><span class="sxs-lookup"><span data-stu-id="c13f8-112">-3</span></span></p></td>
<td><p><span data-ttu-id="c13f8-113">Указывает, что текущий указатель записи находится в EOF (то есть свойство <a href="bof-eof-properties-ado.md">EOF</a> <strong>true).</strong></span><span class="sxs-lookup"><span data-stu-id="c13f8-113">Indicates that the current record pointer is at EOF (that is, the <a href="bof-eof-properties-ado.md">EOF</a> property is <strong>True</strong>).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c13f8-114"><strong>adPosUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="c13f8-114"><strong>adPosUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="c13f8-115">–1</span><span class="sxs-lookup"><span data-stu-id="c13f8-115">-1</span></span></p></td>
<td><p><span data-ttu-id="c13f8-116">Указывает, что <strong>Набор записей</strong> пуст, текущая позиция неизвестна, или поставщик не поддерживает свойство <a href="absolutepage-property-ado.md">AbsolutePage</a> или <a href="absoluteposition-property-ado.md">AbsolutePosition.</a></span><span class="sxs-lookup"><span data-stu-id="c13f8-116">Indicates that the <strong>Recordset</strong> is empty, the current position is unknown, or the provider does not support the <a href="absolutepage-property-ado.md">AbsolutePage</a> or <a href="absoluteposition-property-ado.md">AbsolutePosition</a> property.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="c13f8-117">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="c13f8-117">ADO/WFC equivalent</span></span>

<span data-ttu-id="c13f8-118">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="c13f8-118">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c13f8-119">Константа</span><span class="sxs-lookup"><span data-stu-id="c13f8-119">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c13f8-120">AdoEnums.Position.BOF</span><span class="sxs-lookup"><span data-stu-id="c13f8-120">AdoEnums.Position.BOF</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c13f8-121">AdoEnums.Position.EOF</span><span class="sxs-lookup"><span data-stu-id="c13f8-121">AdoEnums.Position.EOF</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c13f8-122">AdoEnums.Position.UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="c13f8-122">AdoEnums.Position.UNKNOWN</span></span></p></td>
</tr>
</tbody>
</table>

