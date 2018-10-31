---
title: ConnectPromptEnum (Справочник по для настольных баз данных Access)
TOCTitle: ConnectPromptEnum
ms:assetid: 81dff685-b2e4-467e-75cc-b8c5bf80fb75
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249561(v=office.15)
ms:contentKeyID: 48545965
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: f10fd9fada954bb5e3a356961636b2022c73bae3
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862172"
---
# <a name="connectpromptenum"></a><span data-ttu-id="8d273-102">ConnectPromptEnum</span><span class="sxs-lookup"><span data-stu-id="8d273-102">ConnectPromptEnum</span></span>

<span data-ttu-id="8d273-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8d273-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="8d273-104">Указывает, следует ли отображать диалоговое окно запрашивать отсутствующие параметры при открытии подключения к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="8d273-104">Specifies whether a dialog box should be displayed to prompt for missing parameters when opening a connection to a data source.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8d273-105">Константа</span><span class="sxs-lookup"><span data-stu-id="8d273-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="8d273-106">Значение</span><span class="sxs-lookup"><span data-stu-id="8d273-106">Value</span></span></p></th>
<th><p><span data-ttu-id="8d273-107">Описание</span><span class="sxs-lookup"><span data-stu-id="8d273-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d273-108"><strong>adPromptAlways</strong></span><span class="sxs-lookup"><span data-stu-id="8d273-108"><strong>adPromptAlways</strong></span></span></p></td>
<td><p><span data-ttu-id="8d273-109">1</span><span class="sxs-lookup"><span data-stu-id="8d273-109">1</span></span></p></td>
<td><p><span data-ttu-id="8d273-110">Выдает запрос всегда.</span><span class="sxs-lookup"><span data-stu-id="8d273-110">Prompts always.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d273-111"><strong>adPromptComplete</strong></span><span class="sxs-lookup"><span data-stu-id="8d273-111"><strong>adPromptComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="8d273-112">2</span><span class="sxs-lookup"><span data-stu-id="8d273-112">2</span></span></p></td>
<td><p><span data-ttu-id="8d273-113">Выдает запрос, если требуются дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="8d273-113">Prompts if more information is required.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d273-114"><strong>adPromptCompleteRequired</strong></span><span class="sxs-lookup"><span data-stu-id="8d273-114"><strong>adPromptCompleteRequired</strong></span></span></p></td>
<td><p><span data-ttu-id="8d273-115">3</span><span class="sxs-lookup"><span data-stu-id="8d273-115">3</span></span></p></td>
<td><p><span data-ttu-id="8d273-116">Выдает запрос, если требуется Дополнительные сведения, но не разрешены необязательных параметров.</span><span class="sxs-lookup"><span data-stu-id="8d273-116">Prompts if more information is required but optional parameters are not allowed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d273-117"><strong>adPromptNever</strong></span><span class="sxs-lookup"><span data-stu-id="8d273-117"><strong>adPromptNever</strong></span></span></p></td>
<td><p><span data-ttu-id="8d273-118">4</span><span class="sxs-lookup"><span data-stu-id="8d273-118">4</span></span></p></td>
<td><p><span data-ttu-id="8d273-119">Никогда не запросы.</span><span class="sxs-lookup"><span data-stu-id="8d273-119">Never prompts.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="8d273-120">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="8d273-120">ADO/WFC equivalent</span></span>

<span data-ttu-id="8d273-121">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="8d273-121">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8d273-122">Constant</span><span class="sxs-lookup"><span data-stu-id="8d273-122">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d273-123">AdoEnums.ConnectPrompt.ALWAYS</span><span class="sxs-lookup"><span data-stu-id="8d273-123">AdoEnums.ConnectPrompt.ALWAYS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d273-124">AdoEnums.ConnectPrompt.COMPLETE</span><span class="sxs-lookup"><span data-stu-id="8d273-124">AdoEnums.ConnectPrompt.COMPLETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d273-125">AdoEnums.ConnectPrompt.COMPLETEREQUIRED</span><span class="sxs-lookup"><span data-stu-id="8d273-125">AdoEnums.ConnectPrompt.COMPLETEREQUIRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d273-126">AdoEnums.ConnectPrompt.NEVER</span><span class="sxs-lookup"><span data-stu-id="8d273-126">AdoEnums.ConnectPrompt.NEVER</span></span></p></td>
</tr>
</tbody>
</table>

