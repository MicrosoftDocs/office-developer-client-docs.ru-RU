---
title: Ресинценум (Справочник по базам данных Access на компьютере)
TOCTitle: ResyncEnum
ms:assetid: 3d38b77b-6afe-e6a0-1a05-7c7ffc19edef
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249164(v=office.15)
ms:contentKeyID: 48544337
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ff09d69a9cf36246b3367202531a011c4e1aba12
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306547"
---
# <a name="resyncenum"></a><span data-ttu-id="de40a-102">ResyncEnum</span><span class="sxs-lookup"><span data-stu-id="de40a-102">ResyncEnum</span></span>

<span data-ttu-id="de40a-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="de40a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="de40a-104">Указывает, перезаписываются ли базовые значения при вызове метода повторной [синхронизации](resync-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="de40a-104">Specifies whether underlying values are overwritten by a call to [Resync](resync-method-ado.md).</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="de40a-105">Константа</span><span class="sxs-lookup"><span data-stu-id="de40a-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="de40a-106">Значение</span><span class="sxs-lookup"><span data-stu-id="de40a-106">Value</span></span></p></th>
<th><p><span data-ttu-id="de40a-107">Описание</span><span class="sxs-lookup"><span data-stu-id="de40a-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="de40a-108"><strong>адресинкаллвалуес</strong></span><span class="sxs-lookup"><span data-stu-id="de40a-108"><strong>adResyncAllValues</strong></span></span></p></td>
<td><p><span data-ttu-id="de40a-109">2</span><span class="sxs-lookup"><span data-stu-id="de40a-109">2</span></span></p></td>
<td><p><span data-ttu-id="de40a-110">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="de40a-110">Default.</span></span> <span data-ttu-id="de40a-111">Перезаписывает данные, и ожидающие обновления отменяются.</span><span class="sxs-lookup"><span data-stu-id="de40a-111">Overwrites data, and pending updates are canceled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de40a-112"><strong>адресинкундерлингвалуес</strong></span><span class="sxs-lookup"><span data-stu-id="de40a-112"><strong>adResyncUnderlyingValues</strong></span></span></p></td>
<td><p><span data-ttu-id="de40a-113">1,1</span><span class="sxs-lookup"><span data-stu-id="de40a-113">1</span></span></p></td>
<td><p><span data-ttu-id="de40a-114">Не перезаписывает данные, а ожидающие обновления не отменяются.</span><span class="sxs-lookup"><span data-stu-id="de40a-114">Does not overwrite data, and pending updates are not canceled.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="de40a-115">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="de40a-115">ADO/WFC equivalent</span></span>

<span data-ttu-id="de40a-116">Пакет: **com. MS. WFC. Data**</span><span class="sxs-lookup"><span data-stu-id="de40a-116">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="de40a-117">Константа</span><span class="sxs-lookup"><span data-stu-id="de40a-117">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="de40a-118">Адоенумс. Resync. АЛЛВАЛУЕС</span><span class="sxs-lookup"><span data-stu-id="de40a-118">AdoEnums.Resync.ALLVALUES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de40a-119">Адоенумс. Resync. УНДЕРЛИНГВАЛУЕС</span><span class="sxs-lookup"><span data-stu-id="de40a-119">AdoEnums.Resync.UNDERLYINGVALUES</span></span></p></td>
</tr>
</tbody>
</table>

