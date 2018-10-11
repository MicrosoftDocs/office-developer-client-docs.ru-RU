---
title: StreamWriteEnum (Справочник по для настольных баз данных Access)
TOCTitle: StreamWriteEnum
ms:assetid: b4356999-d7a8-abfa-f6a8-6c2dd04b9257
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249861(v=office.15)
ms:contentKeyID: 48547216
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f58b5173a1208812a6eb9fd06b5f4a414de21ddd
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480813"
---
# <a name="streamwriteenum"></a><span data-ttu-id="be6d7-102">StreamWriteEnum</span><span class="sxs-lookup"><span data-stu-id="be6d7-102">StreamWriteEnum</span></span>


<span data-ttu-id="be6d7-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="be6d7-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="be6d7-104">Указывает, добавлены ли разделитель к строке, записанные в объект [потока](stream-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="be6d7-104">Specifies whether a line separator is appended to the string written to a [Stream](stream-object-ado.md) object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="be6d7-105">Константа</span><span class="sxs-lookup"><span data-stu-id="be6d7-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="be6d7-106">Значение</span><span class="sxs-lookup"><span data-stu-id="be6d7-106">Value</span></span></p></th>
<th><p><span data-ttu-id="be6d7-107">Описание</span><span class="sxs-lookup"><span data-stu-id="be6d7-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="be6d7-108"><strong>adWriteChar</strong></span><span class="sxs-lookup"><span data-stu-id="be6d7-108"><strong>adWriteChar</strong></span></span></p></td>
<td><p><span data-ttu-id="be6d7-109">0</span><span class="sxs-lookup"><span data-stu-id="be6d7-109">0</span></span></p></td>
<td><p><span data-ttu-id="be6d7-110">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="be6d7-110">Default.</span></span> <span data-ttu-id="be6d7-111">Записывает заданную текстовую строку (указывается с помощью параметра <em>данных</em> ) на объект <strong>Stream</strong> .</span><span class="sxs-lookup"><span data-stu-id="be6d7-111">Writes the specified text string (specified by the <em>Data</em> parameter) to the <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be6d7-112"><strong>adWriteLine</strong></span><span class="sxs-lookup"><span data-stu-id="be6d7-112"><strong>adWriteLine</strong></span></span></p></td>
<td><p><span data-ttu-id="be6d7-113">1</span><span class="sxs-lookup"><span data-stu-id="be6d7-113">1</span></span></p></td>
<td><p><span data-ttu-id="be6d7-114">Записывает текстовую строку и символ разделителя строки в объект <strong>потока</strong> .</span><span class="sxs-lookup"><span data-stu-id="be6d7-114">Writes a text string and a line separator character to a <strong>Stream</strong> object.</span></span> <span data-ttu-id="be6d7-115">Если свойство <a href="lineseparator-property-ado.md">LineSeparator</a> не определен, командлет возвращает ошибку времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="be6d7-115">If the <a href="lineseparator-property-ado.md">LineSeparator</a> property is not defined, then this returns a run-time error.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="be6d7-116">**Эквивалент ADO/WFC**</span><span class="sxs-lookup"><span data-stu-id="be6d7-116">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="be6d7-117">Эти константы нет ADO/WFC эквивалентами.</span><span class="sxs-lookup"><span data-stu-id="be6d7-117">These constants do not have ADO/WFC equivalents.</span></span>

