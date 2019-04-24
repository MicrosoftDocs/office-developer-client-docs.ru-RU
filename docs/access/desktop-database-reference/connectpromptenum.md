---
title: Коннектпромптенум (Справочник по базам данных Access на компьютере)
TOCTitle: ConnectPromptEnum
ms:assetid: 81dff685-b2e4-467e-75cc-b8c5bf80fb75
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249561(v=office.15)
ms:contentKeyID: 48545965
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 54643a66316d7f534553c20ecc3aafdf755fb857
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295669"
---
# <a name="connectpromptenum"></a><span data-ttu-id="ee472-102">ConnectPromptEnum</span><span class="sxs-lookup"><span data-stu-id="ee472-102">ConnectPromptEnum</span></span>

<span data-ttu-id="ee472-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ee472-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ee472-104">Указывает, следует ли отображать диалоговое окно с запросом на отсутствие параметров при открытии подключения к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="ee472-104">Specifies whether a dialog box should be displayed to prompt for missing parameters when opening a connection to a data source.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ee472-105">Константа</span><span class="sxs-lookup"><span data-stu-id="ee472-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="ee472-106">Значение</span><span class="sxs-lookup"><span data-stu-id="ee472-106">Value</span></span></p></th>
<th><p><span data-ttu-id="ee472-107">Описание</span><span class="sxs-lookup"><span data-stu-id="ee472-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee472-108"><strong>Адпромпталвайс</strong></span><span class="sxs-lookup"><span data-stu-id="ee472-108"><strong>adPromptAlways</strong></span></span></p></td>
<td><p><span data-ttu-id="ee472-109">1,1</span><span class="sxs-lookup"><span data-stu-id="ee472-109">1</span></span></p></td>
<td><p><span data-ttu-id="ee472-110">Всегда заПрашивать.</span><span class="sxs-lookup"><span data-stu-id="ee472-110">Prompts always.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee472-111"><strong>Адпромпткомплете</strong></span><span class="sxs-lookup"><span data-stu-id="ee472-111"><strong>adPromptComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="ee472-112">2</span><span class="sxs-lookup"><span data-stu-id="ee472-112">2</span></span></p></td>
<td><p><span data-ttu-id="ee472-113">ЗаПрашивает, требуются ли дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="ee472-113">Prompts if more information is required.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee472-114"><strong>Адпромпткомплетерекуиред</strong></span><span class="sxs-lookup"><span data-stu-id="ee472-114"><strong>adPromptCompleteRequired</strong></span></span></p></td>
<td><p><span data-ttu-id="ee472-115">4</span><span class="sxs-lookup"><span data-stu-id="ee472-115">3</span></span></p></td>
<td><p><span data-ttu-id="ee472-116">ЗаПрашивает, если требуются дополнительные сведения, но необязательные параметры не допускаются.</span><span class="sxs-lookup"><span data-stu-id="ee472-116">Prompts if more information is required but optional parameters are not allowed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee472-117"><strong>Адпромптневер</strong></span><span class="sxs-lookup"><span data-stu-id="ee472-117"><strong>adPromptNever</strong></span></span></p></td>
<td><p><span data-ttu-id="ee472-118">SP4</span><span class="sxs-lookup"><span data-stu-id="ee472-118">4</span></span></p></td>
<td><p><span data-ttu-id="ee472-119">Никогда не запрашиваться.</span><span class="sxs-lookup"><span data-stu-id="ee472-119">Never prompts.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="ee472-120">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="ee472-120">ADO/WFC equivalent</span></span>

<span data-ttu-id="ee472-121">Пакет: **com. MS. WFC. Data**</span><span class="sxs-lookup"><span data-stu-id="ee472-121">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ee472-122">Константа</span><span class="sxs-lookup"><span data-stu-id="ee472-122">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee472-123">Адоенумс. Коннектпромпт. ALWAYS</span><span class="sxs-lookup"><span data-stu-id="ee472-123">AdoEnums.ConnectPrompt.ALWAYS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee472-124">Адоенумс. Коннектпромпт. COMPLETE</span><span class="sxs-lookup"><span data-stu-id="ee472-124">AdoEnums.ConnectPrompt.COMPLETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee472-125">Адоенумс. Коннектпромпт. КОМПЛЕТЕРЕКУИРЕД</span><span class="sxs-lookup"><span data-stu-id="ee472-125">AdoEnums.ConnectPrompt.COMPLETEREQUIRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee472-126">Адоенумс. Коннектпромпт. NEVER</span><span class="sxs-lookup"><span data-stu-id="ee472-126">AdoEnums.ConnectPrompt.NEVER</span></span></p></td>
</tr>
</tbody>
</table>

