---
title: Стреамреаденум (Справочник по базам данных Access на компьютере)
TOCTitle: StreamReadEnum
ms:assetid: 12432c0d-dc2e-10ea-13db-0c07b6ba29bc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248895(v=office.15)
ms:contentKeyID: 48543336
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e4d9c96a7bb34fe0ab3512a316a92e1f7a01ef4b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314723"
---
# <a name="streamreadenum"></a><span data-ttu-id="0891c-102">StreamReadEnum</span><span class="sxs-lookup"><span data-stu-id="0891c-102">StreamReadEnum</span></span>

<span data-ttu-id="0891c-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0891c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0891c-104">Указывает, следует ли считывать весь поток или следующую строку из объекта [Stream](stream-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="0891c-104">Specifies whether the whole stream or the next line should be read from a [Stream](stream-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0891c-105">Константа</span><span class="sxs-lookup"><span data-stu-id="0891c-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="0891c-106">Значение</span><span class="sxs-lookup"><span data-stu-id="0891c-106">Value</span></span></p></th>
<th><p><span data-ttu-id="0891c-107">Описание</span><span class="sxs-lookup"><span data-stu-id="0891c-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0891c-108"><strong>Адреадалл</strong></span><span class="sxs-lookup"><span data-stu-id="0891c-108"><strong>adReadAll</strong></span></span></p></td>
<td><p><span data-ttu-id="0891c-109">–1</span><span class="sxs-lookup"><span data-stu-id="0891c-109">-1</span></span></p></td>
<td><p><span data-ttu-id="0891c-110">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0891c-110">Default.</span></span> <span data-ttu-id="0891c-111">Считывает все байты из потока, начиная с текущей позиции и до маркера <a href="eos-property-ado.md">EOS</a> .</span><span class="sxs-lookup"><span data-stu-id="0891c-111">Reads all bytes from the stream, from the current position onwards to the <a href="eos-property-ado.md">EOS</a> marker.</span></span> <span data-ttu-id="0891c-112">Это единственное допустимое значение <strong>стреамреаденум</strong> с двоичными потоками (<a href="type-property-ado-stream.md">Type</a> — <strong>адтипебинари</strong>).</span><span class="sxs-lookup"><span data-stu-id="0891c-112">This is the only valid <strong>StreamReadEnum</strong> value with binary streams (<a href="type-property-ado-stream.md">Type</a> is <strong>adTypeBinary</strong>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0891c-113"><strong>Адреадлине</strong></span><span class="sxs-lookup"><span data-stu-id="0891c-113"><strong>adReadLine</strong></span></span></p></td>
<td><p><span data-ttu-id="0891c-114">–2</span><span class="sxs-lookup"><span data-stu-id="0891c-114">-2</span></span></p></td>
<td><p><span data-ttu-id="0891c-115">Считывает следующую строку из потока (задается свойством <a href="lineseparator-property-ado.md">LineSeparator</a> ).</span><span class="sxs-lookup"><span data-stu-id="0891c-115">Reads the next line from the stream (designated by the <a href="lineseparator-property-ado.md">LineSeparator</a> property).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="0891c-116">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="0891c-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="0891c-117">Эти константы не имеют эквивалентов ADO/WFC.</span><span class="sxs-lookup"><span data-stu-id="0891c-117">These constants do not have ADO/WFC equivalents.</span></span>

