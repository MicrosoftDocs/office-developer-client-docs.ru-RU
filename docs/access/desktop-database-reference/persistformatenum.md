---
title: PersistFormatEnum (Ссылка на настольные базы данных)
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
# <a name="persistformatenum"></a><span data-ttu-id="39687-102">PersistFormatEnum</span><span class="sxs-lookup"><span data-stu-id="39687-102">PersistFormatEnum</span></span>

<span data-ttu-id="39687-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="39687-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="39687-104">Указывает формат, в котором можно сохранить [набор записей.](recordset-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="39687-104">Specifies the format in which to save a [Recordset](recordset-object-ado.md).</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="39687-105">Константа</span><span class="sxs-lookup"><span data-stu-id="39687-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="39687-106">Значение</span><span class="sxs-lookup"><span data-stu-id="39687-106">Value</span></span></p></th>
<th><p><span data-ttu-id="39687-107">Описание</span><span class="sxs-lookup"><span data-stu-id="39687-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="39687-108"><strong>adPersistADTG</strong></span><span class="sxs-lookup"><span data-stu-id="39687-108"><strong>adPersistADTG</strong></span></span></p></td>
<td><p><span data-ttu-id="39687-109">0</span><span class="sxs-lookup"><span data-stu-id="39687-109">0</span></span></p></td>
<td><p><span data-ttu-id="39687-110">Указывает формат Microsoft Advanced Data TableGram (ADTG).</span><span class="sxs-lookup"><span data-stu-id="39687-110">Indicates Microsoft Advanced Data TableGram (ADTG) format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39687-111"><strong>adPersistADO</strong></span><span class="sxs-lookup"><span data-stu-id="39687-111"><strong>adPersistADO</strong></span></span></p></td>
<td><p><span data-ttu-id="39687-112">1</span><span class="sxs-lookup"><span data-stu-id="39687-112">1</span></span></p></td>
<td><p><span data-ttu-id="39687-113">Указывает, что будет использоваться собственный формат языка разметки (XML) ADO.</span><span class="sxs-lookup"><span data-stu-id="39687-113">Indicates that ADO's own Extensible Markup Language (XML) format will be used.</span></span> <span data-ttu-id="39687-114">Это значение такое же, как adPersistXML и включено для обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="39687-114">This value is the same as adPersistXML and is included for backwards compatibility.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39687-115"><strong>adPersistXML</strong></span><span class="sxs-lookup"><span data-stu-id="39687-115"><strong>adPersistXML</strong></span></span></p></td>
<td><p><span data-ttu-id="39687-116">1</span><span class="sxs-lookup"><span data-stu-id="39687-116">1</span></span></p></td>
<td><p><span data-ttu-id="39687-117">Указывает формат Extensible Markup Language (XML).</span><span class="sxs-lookup"><span data-stu-id="39687-117">Indicates Extensible Markup Language (XML) format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39687-118"><strong>adPersistProviderSpecific</strong></span><span class="sxs-lookup"><span data-stu-id="39687-118"><strong>adPersistProviderSpecific</strong></span></span></p></td>
<td><p><span data-ttu-id="39687-119">2</span><span class="sxs-lookup"><span data-stu-id="39687-119">2</span></span></p></td>
<td><p><span data-ttu-id="39687-120">Указывает, что поставщик сохранит <strong>набор Recordset</strong> с помощью собственного формата.</span><span class="sxs-lookup"><span data-stu-id="39687-120">Indicates that the provider will persist the <strong>Recordset</strong> using its own format.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="39687-121">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="39687-121">ADO/WFC equivalent</span></span>

<span data-ttu-id="39687-122">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="39687-122">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="39687-123">Константа</span><span class="sxs-lookup"><span data-stu-id="39687-123">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="39687-124">AdoEnums.PersistFormat.ADTG</span><span class="sxs-lookup"><span data-stu-id="39687-124">AdoEnums.PersistFormat.ADTG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39687-125">AdoEnums.PersistFormat.XML</span><span class="sxs-lookup"><span data-stu-id="39687-125">AdoEnums.PersistFormat.XML</span></span></p></td>
</tr>
</tbody>
</table>

