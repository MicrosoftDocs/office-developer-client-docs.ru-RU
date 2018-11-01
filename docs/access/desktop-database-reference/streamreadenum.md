---
title: StreamReadEnum (Справочник по для настольных баз данных Access)
TOCTitle: StreamReadEnum
ms:assetid: 12432c0d-dc2e-10ea-13db-0c07b6ba29bc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248895(v=office.15)
ms:contentKeyID: 48543336
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 665819da2a2d31068e50e91eafdddc083645f443
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872713"
---
# <a name="streamreadenum"></a><span data-ttu-id="e0d92-102">StreamReadEnum</span><span class="sxs-lookup"><span data-stu-id="e0d92-102">StreamReadEnum</span></span>

<span data-ttu-id="e0d92-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e0d92-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e0d92-104">Указывает, следует ли считывать весь поток или следующую строку из объекта [потока](stream-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="e0d92-104">Specifies whether the whole stream or the next line should be read from a [Stream](stream-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e0d92-105">Константа</span><span class="sxs-lookup"><span data-stu-id="e0d92-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="e0d92-106">Значение</span><span class="sxs-lookup"><span data-stu-id="e0d92-106">Value</span></span></p></th>
<th><p><span data-ttu-id="e0d92-107">Описание</span><span class="sxs-lookup"><span data-stu-id="e0d92-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e0d92-108"><strong>adReadAll</strong></span><span class="sxs-lookup"><span data-stu-id="e0d92-108"><strong>adReadAll</strong></span></span></p></td>
<td><p><span data-ttu-id="e0d92-109">-1</span><span class="sxs-lookup"><span data-stu-id="e0d92-109">-1</span></span></p></td>
<td><p><span data-ttu-id="e0d92-110">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e0d92-110">Default.</span></span> <span data-ttu-id="e0d92-111">Считывает все байты из потока из текущей позиции добавляющего <a href="eos-property-ado.md">EOS</a> маркер.</span><span class="sxs-lookup"><span data-stu-id="e0d92-111">Reads all bytes from the stream, from the current position onwards to the <a href="eos-property-ado.md">EOS</a> marker.</span></span> <span data-ttu-id="e0d92-112">Это допустимо только значение <strong>StreamReadEnum</strong> с двоичных потоков (<a href="type-property-ado-stream.md">Тип</a> — <strong>adTypeBinary</strong>).</span><span class="sxs-lookup"><span data-stu-id="e0d92-112">This is the only valid <strong>StreamReadEnum</strong> value with binary streams (<a href="type-property-ado-stream.md">Type</a> is <strong>adTypeBinary</strong>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0d92-113"><strong>adReadLine</strong></span><span class="sxs-lookup"><span data-stu-id="e0d92-113"><strong>adReadLine</strong></span></span></p></td>
<td><p><span data-ttu-id="e0d92-114">-2</span><span class="sxs-lookup"><span data-stu-id="e0d92-114">-2</span></span></p></td>
<td><p><span data-ttu-id="e0d92-115">Считывает следующую строку в потоке (обозначенного свойство <a href="lineseparator-property-ado.md">LineSeparator</a> ).</span><span class="sxs-lookup"><span data-stu-id="e0d92-115">Reads the next line from the stream (designated by the <a href="lineseparator-property-ado.md">LineSeparator</a> property).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="e0d92-116">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="e0d92-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="e0d92-117">Эти константы нет ADO/WFC эквивалентами.</span><span class="sxs-lookup"><span data-stu-id="e0d92-117">These constants do not have ADO/WFC equivalents.</span></span>

