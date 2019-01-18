---
title: StreamWriteEnum (Справочник по для настольных баз данных Access)
TOCTitle: StreamWriteEnum
ms:assetid: b4356999-d7a8-abfa-f6a8-6c2dd04b9257
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249861(v=office.15)
ms:contentKeyID: 48547216
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 87144e5409fb54cf0cb8f59ad4d593ab05d694a4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706172"
---
# <a name="streamwriteenum"></a><span data-ttu-id="744d6-102">StreamWriteEnum</span><span class="sxs-lookup"><span data-stu-id="744d6-102">StreamWriteEnum</span></span>

<span data-ttu-id="744d6-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="744d6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="744d6-104">Указывает, добавлены ли разделитель к строке, записанные в объект [потока](stream-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="744d6-104">Specifies whether a line separator is appended to the string written to a [Stream](stream-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="744d6-105">Константа</span><span class="sxs-lookup"><span data-stu-id="744d6-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="744d6-106">Значение</span><span class="sxs-lookup"><span data-stu-id="744d6-106">Value</span></span></p></th>
<th><p><span data-ttu-id="744d6-107">Описание</span><span class="sxs-lookup"><span data-stu-id="744d6-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="744d6-108"><strong>adWriteChar</strong></span><span class="sxs-lookup"><span data-stu-id="744d6-108"><strong>adWriteChar</strong></span></span></p></td>
<td><p><span data-ttu-id="744d6-109">0</span><span class="sxs-lookup"><span data-stu-id="744d6-109">0</span></span></p></td>
<td><p><span data-ttu-id="744d6-110">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="744d6-110">Default.</span></span> <span data-ttu-id="744d6-111">Записывает заданную текстовую строку (указывается с помощью параметра <em>данных</em> ) на объект <strong>Stream</strong> .</span><span class="sxs-lookup"><span data-stu-id="744d6-111">Writes the specified text string (specified by the <em>Data</em> parameter) to the <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="744d6-112"><strong>adWriteLine</strong></span><span class="sxs-lookup"><span data-stu-id="744d6-112"><strong>adWriteLine</strong></span></span></p></td>
<td><p><span data-ttu-id="744d6-113">1</span><span class="sxs-lookup"><span data-stu-id="744d6-113">1</span></span></p></td>
<td><p><span data-ttu-id="744d6-114">Записывает текстовую строку и символ разделителя строки в объект <strong>потока</strong> .</span><span class="sxs-lookup"><span data-stu-id="744d6-114">Writes a text string and a line separator character to a <strong>Stream</strong> object.</span></span> <span data-ttu-id="744d6-115">Если свойство <a href="lineseparator-property-ado.md">LineSeparator</a> не определен, командлет возвращает ошибку времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="744d6-115">If the <a href="lineseparator-property-ado.md">LineSeparator</a> property is not defined, then this returns a run-time error.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="744d6-116">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="744d6-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="744d6-117">Эти константы нет ADO/WFC эквивалентами.</span><span class="sxs-lookup"><span data-stu-id="744d6-117">These constants do not have ADO/WFC equivalents.</span></span>

