---
title: Персистформатенум (Справочник по базам данных Access на компьютере)
TOCTitle: PersistFormatEnum
ms:assetid: 5aa99a63-d422-0812-5aba-19305a3ad405
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249313(v=office.15)
ms:contentKeyID: 48545050
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4954c09c3eff67bb6f55dfc9e49464ad58fad5e6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287610"
---
# <a name="persistformatenum"></a><span data-ttu-id="93179-102">PersistFormatEnum</span><span class="sxs-lookup"><span data-stu-id="93179-102">PersistFormatEnum</span></span>

<span data-ttu-id="93179-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="93179-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="93179-104">Задает формат, в котором будет сохранен [набор записей](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="93179-104">Specifies the format in which to save a [Recordset](recordset-object-ado.md).</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="93179-105">Константа</span><span class="sxs-lookup"><span data-stu-id="93179-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="93179-106">Значение</span><span class="sxs-lookup"><span data-stu-id="93179-106">Value</span></span></p></th>
<th><p><span data-ttu-id="93179-107">Описание</span><span class="sxs-lookup"><span data-stu-id="93179-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="93179-108"><strong>Адперсистадтг</strong></span><span class="sxs-lookup"><span data-stu-id="93179-108"><strong>adPersistADTG</strong></span></span></p></td>
<td><p><span data-ttu-id="93179-109">нуль</span><span class="sxs-lookup"><span data-stu-id="93179-109">0</span></span></p></td>
<td><p><span data-ttu-id="93179-110">Указывает формат Microsoft Advanced Data Таблеграм (АДТГ).</span><span class="sxs-lookup"><span data-stu-id="93179-110">Indicates Microsoft Advanced Data TableGram (ADTG) format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93179-111"><strong>Адперсистадо</strong></span><span class="sxs-lookup"><span data-stu-id="93179-111"><strong>adPersistADO</strong></span></span></p></td>
<td><p><span data-ttu-id="93179-112">1,1</span><span class="sxs-lookup"><span data-stu-id="93179-112">1</span></span></p></td>
<td><p><span data-ttu-id="93179-113">Указывает, что будет использоваться собственный формат языка XML для ADO.</span><span class="sxs-lookup"><span data-stu-id="93179-113">Indicates that ADO's own Extensible Markup Language (XML) format will be used.</span></span> <span data-ttu-id="93179-114">Это значение аналогично Адперсистксмл и включено для обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="93179-114">This value is the same as adPersistXML and is included for backwards compatibility.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93179-115"><strong>Адперсистксмл</strong></span><span class="sxs-lookup"><span data-stu-id="93179-115"><strong>adPersistXML</strong></span></span></p></td>
<td><p><span data-ttu-id="93179-116">1,1</span><span class="sxs-lookup"><span data-stu-id="93179-116">1</span></span></p></td>
<td><p><span data-ttu-id="93179-117">Указывает на XML-формат.</span><span class="sxs-lookup"><span data-stu-id="93179-117">Indicates Extensible Markup Language (XML) format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93179-118"><strong>АдперсистпровидерспеЦифик</strong></span><span class="sxs-lookup"><span data-stu-id="93179-118"><strong>adPersistProviderSpecific</strong></span></span></p></td>
<td><p><span data-ttu-id="93179-119">2</span><span class="sxs-lookup"><span data-stu-id="93179-119">2</span></span></p></td>
<td><p><span data-ttu-id="93179-120">Указывает, что поставщик сохранит <strong>набор записей</strong> в собственном формате.</span><span class="sxs-lookup"><span data-stu-id="93179-120">Indicates that the provider will persist the <strong>Recordset</strong> using its own format.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="93179-121">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="93179-121">ADO/WFC equivalent</span></span>

<span data-ttu-id="93179-122">Пакет: **com. MS. WFC. Data**</span><span class="sxs-lookup"><span data-stu-id="93179-122">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="93179-123">Константа</span><span class="sxs-lookup"><span data-stu-id="93179-123">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="93179-124">Адоенумс. Персистформат. АДТГ</span><span class="sxs-lookup"><span data-stu-id="93179-124">AdoEnums.PersistFormat.ADTG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93179-125">Адоенумс. Персистформат. XML</span><span class="sxs-lookup"><span data-stu-id="93179-125">AdoEnums.PersistFormat.XML</span></span></p></td>
</tr>
</tbody>
</table>

