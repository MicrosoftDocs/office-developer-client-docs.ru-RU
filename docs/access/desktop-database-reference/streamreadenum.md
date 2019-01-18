---
title: StreamReadEnum (Справочник по для настольных баз данных Access)
TOCTitle: StreamReadEnum
ms:assetid: 12432c0d-dc2e-10ea-13db-0c07b6ba29bc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248895(v=office.15)
ms:contentKeyID: 48543336
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e4d9c96a7bb34fe0ab3512a316a92e1f7a01ef4b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713662"
---
# <a name="streamreadenum"></a><span data-ttu-id="0f81b-102">StreamReadEnum</span><span class="sxs-lookup"><span data-stu-id="0f81b-102">StreamReadEnum</span></span>

<span data-ttu-id="0f81b-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0f81b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0f81b-104">Указывает, следует ли считывать весь поток или следующую строку из объекта [потока](stream-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="0f81b-104">Specifies whether the whole stream or the next line should be read from a [Stream](stream-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0f81b-105">Константа</span><span class="sxs-lookup"><span data-stu-id="0f81b-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="0f81b-106">Значение</span><span class="sxs-lookup"><span data-stu-id="0f81b-106">Value</span></span></p></th>
<th><p><span data-ttu-id="0f81b-107">Описание</span><span class="sxs-lookup"><span data-stu-id="0f81b-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0f81b-108"><strong>adReadAll</strong></span><span class="sxs-lookup"><span data-stu-id="0f81b-108"><strong>adReadAll</strong></span></span></p></td>
<td><p><span data-ttu-id="0f81b-109">–1</span><span class="sxs-lookup"><span data-stu-id="0f81b-109">-1</span></span></p></td>
<td><p><span data-ttu-id="0f81b-110">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0f81b-110">Default.</span></span> <span data-ttu-id="0f81b-111">Считывает все байты из потока из текущей позиции добавляющего <a href="eos-property-ado.md">EOS</a> маркер.</span><span class="sxs-lookup"><span data-stu-id="0f81b-111">Reads all bytes from the stream, from the current position onwards to the <a href="eos-property-ado.md">EOS</a> marker.</span></span> <span data-ttu-id="0f81b-112">Это допустимо только значение <strong>StreamReadEnum</strong> с двоичных потоков (<a href="type-property-ado-stream.md">Тип</a> — <strong>adTypeBinary</strong>).</span><span class="sxs-lookup"><span data-stu-id="0f81b-112">This is the only valid <strong>StreamReadEnum</strong> value with binary streams (<a href="type-property-ado-stream.md">Type</a> is <strong>adTypeBinary</strong>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f81b-113"><strong>adReadLine</strong></span><span class="sxs-lookup"><span data-stu-id="0f81b-113"><strong>adReadLine</strong></span></span></p></td>
<td><p><span data-ttu-id="0f81b-114">–2</span><span class="sxs-lookup"><span data-stu-id="0f81b-114">-2</span></span></p></td>
<td><p><span data-ttu-id="0f81b-115">Считывает следующую строку в потоке (обозначенного свойство <a href="lineseparator-property-ado.md">LineSeparator</a> ).</span><span class="sxs-lookup"><span data-stu-id="0f81b-115">Reads the next line from the stream (designated by the <a href="lineseparator-property-ado.md">LineSeparator</a> property).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="0f81b-116">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="0f81b-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="0f81b-117">Эти константы нет ADO/WFC эквивалентами.</span><span class="sxs-lookup"><span data-stu-id="0f81b-117">These constants do not have ADO/WFC equivalents.</span></span>

