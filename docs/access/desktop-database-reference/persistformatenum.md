---
title: PersistFormatEnum (Справочник по для настольных баз данных Access)
TOCTitle: PersistFormatEnum
ms:assetid: 5aa99a63-d422-0812-5aba-19305a3ad405
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249313(v=office.15)
ms:contentKeyID: 48545050
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: a1e980debebe6a38ed0c27eabba3abefcd8be152
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887154"
---
# <a name="persistformatenum"></a><span data-ttu-id="a502e-102">PersistFormatEnum</span><span class="sxs-lookup"><span data-stu-id="a502e-102">PersistFormatEnum</span></span>

<span data-ttu-id="a502e-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a502e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a502e-104">Задает формат для сохранения [записей](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="a502e-104">Specifies the format in which to save a [Recordset](recordset-object-ado.md).</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a502e-105">Константа</span><span class="sxs-lookup"><span data-stu-id="a502e-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="a502e-106">Значение</span><span class="sxs-lookup"><span data-stu-id="a502e-106">Value</span></span></p></th>
<th><p><span data-ttu-id="a502e-107">Описание</span><span class="sxs-lookup"><span data-stu-id="a502e-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a502e-108"><strong>adPersistADTG</strong></span><span class="sxs-lookup"><span data-stu-id="a502e-108"><strong>adPersistADTG</strong></span></span></p></td>
<td><p><span data-ttu-id="a502e-109">0</span><span class="sxs-lookup"><span data-stu-id="a502e-109">0</span></span></p></td>
<td><p><span data-ttu-id="a502e-110">Указывает формат TableGram дополнительные данные (ADTG).</span><span class="sxs-lookup"><span data-stu-id="a502e-110">Indicates Microsoft Advanced Data TableGram (ADTG) format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a502e-111"><strong>adPersistADO</strong></span><span class="sxs-lookup"><span data-stu-id="a502e-111"><strong>adPersistADO</strong></span></span></p></td>
<td><p><span data-ttu-id="a502e-112">1</span><span class="sxs-lookup"><span data-stu-id="a502e-112">1</span></span></p></td>
<td><p><span data-ttu-id="a502e-113">Указывает, что будет использоваться формат ADO собственные языке (XML).</span><span class="sxs-lookup"><span data-stu-id="a502e-113">Indicates that ADO's own Extensible Markup Language (XML) format will be used.</span></span> <span data-ttu-id="a502e-114">Это значение совпадает с adPersistXML и будет включено для обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="a502e-114">This value is the same as adPersistXML and is included for backwards compatibility.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a502e-115"><strong>adPersistXML</strong></span><span class="sxs-lookup"><span data-stu-id="a502e-115"><strong>adPersistXML</strong></span></span></p></td>
<td><p><span data-ttu-id="a502e-116">1</span><span class="sxs-lookup"><span data-stu-id="a502e-116">1</span></span></p></td>
<td><p><span data-ttu-id="a502e-117">Указывает формат языке (XML).</span><span class="sxs-lookup"><span data-stu-id="a502e-117">Indicates Extensible Markup Language (XML) format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a502e-118"><strong>adPersistProviderSpecific</strong></span><span class="sxs-lookup"><span data-stu-id="a502e-118"><strong>adPersistProviderSpecific</strong></span></span></p></td>
<td><p><span data-ttu-id="a502e-119">2</span><span class="sxs-lookup"><span data-stu-id="a502e-119">2</span></span></p></td>
<td><p><span data-ttu-id="a502e-120">Указывает, что поставщик будет сохраняться <strong>набора записей</strong> с использованием собственного формата.</span><span class="sxs-lookup"><span data-stu-id="a502e-120">Indicates that the provider will persist the <strong>Recordset</strong> using its own format.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="a502e-121">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="a502e-121">ADO/WFC equivalent</span></span>

<span data-ttu-id="a502e-122">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="a502e-122">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a502e-123">Constant</span><span class="sxs-lookup"><span data-stu-id="a502e-123">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a502e-124">AdoEnums.PersistFormat.ADTG</span><span class="sxs-lookup"><span data-stu-id="a502e-124">AdoEnums.PersistFormat.ADTG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a502e-125">AdoEnums.PersistFormat.XML</span><span class="sxs-lookup"><span data-stu-id="a502e-125">AdoEnums.PersistFormat.XML</span></span></p></td>
</tr>
</tbody>
</table>

