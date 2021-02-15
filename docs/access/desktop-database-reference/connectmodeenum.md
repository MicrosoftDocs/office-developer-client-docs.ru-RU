---
title: ConnectModeEnum (справочник по базам данных Access для настольных ПК)
TOCTitle: ConnectModeEnum
ms:assetid: a15aa733-f899-5fe9-e705-67a4301706d1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249743(v=office.15)
ms:contentKeyID: 48546728
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 453d84e687a31f7df5082e17b80fe2a1bda756be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295697"
---
# <a name="connectmodeenum"></a><span data-ttu-id="2f3d9-102">ConnectModeEnum</span><span class="sxs-lookup"><span data-stu-id="2f3d9-102">ConnectModeEnum</span></span>

<span data-ttu-id="2f3d9-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2f3d9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2f3d9-104">Указывает доступные разрешения для изменения данных в [connection,](connection-object-ado.md)открытия записи или указания значений для свойства [Mode](mode-property-ado.md) объектов **Record** и [Stream.](stream-object-ado.md) [](record-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="2f3d9-104">Specifies the available permissions for modifying data in a [Connection](connection-object-ado.md), opening a [Record](record-object-ado.md), or specifying values for the [Mode](mode-property-ado.md) property of the **Record** and [Stream](stream-object-ado.md) objects.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2f3d9-105">Константа</span><span class="sxs-lookup"><span data-stu-id="2f3d9-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="2f3d9-106">Значение</span><span class="sxs-lookup"><span data-stu-id="2f3d9-106">Value</span></span></p></th>
<th><p><span data-ttu-id="2f3d9-107">Описание</span><span class="sxs-lookup"><span data-stu-id="2f3d9-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2f3d9-108"><strong>adModeRead</strong></span><span class="sxs-lookup"><span data-stu-id="2f3d9-108"><strong>adModeRead</strong></span></span></p></td>
<td><p><span data-ttu-id="2f3d9-109">1 </span><span class="sxs-lookup"><span data-stu-id="2f3d9-109">1</span></span></p></td>
<td><p><span data-ttu-id="2f3d9-110">Указывает разрешения только для чтения.</span><span class="sxs-lookup"><span data-stu-id="2f3d9-110">Indicates read-only permissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f3d9-111"><strong>adModeReadWrite</strong></span><span class="sxs-lookup"><span data-stu-id="2f3d9-111"><strong>adModeReadWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="2f3d9-112">3 </span><span class="sxs-lookup"><span data-stu-id="2f3d9-112">3</span></span></p></td>
<td><p><span data-ttu-id="2f3d9-113">Указывает разрешения на чтение и записи.</span><span class="sxs-lookup"><span data-stu-id="2f3d9-113">Indicates read/write permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f3d9-114"><strong>adModeRecursive</strong></span><span class="sxs-lookup"><span data-stu-id="2f3d9-114"><strong>adModeRecursive</strong></span></span></p></td>
<td><p><span data-ttu-id="2f3d9-115">0x400000</span><span class="sxs-lookup"><span data-stu-id="2f3d9-115">0x400000</span></span></p></td>
<td><p><span data-ttu-id="2f3d9-116">Используется в сочетании с другими значениями <em>*ShareDeny*</em> <strong>(adModeShareDenyNone,</strong> <strong>adModeShareDenyWrite</strong>или <strong>adModeShareDenyRead)</strong>для распространения ограничений общего доступа ко всем в субфиксам текущей записи. <strong></strong></span><span class="sxs-lookup"><span data-stu-id="2f3d9-116">Used in conjunction with the other <em>*ShareDeny*</em> values (<strong>adModeShareDenyNone</strong>, <strong>adModeShareDenyWrite</strong>, or <strong>adModeShareDenyRead</strong>) to propagate sharing restrictions to all sub-records of the current <strong>Record</strong>.</span></span> <span data-ttu-id="2f3d9-117">Это не влияет, если <strong>у записи</strong> нет детей.</span><span class="sxs-lookup"><span data-stu-id="2f3d9-117">It has no affect if the <strong>Record</strong> does not have any children.</span></span></p><p><span data-ttu-id="2f3d9-118">Ошибка во время запуска создается, если она используется только <strong>с adModeShareDenyNone.</strong></span><span class="sxs-lookup"><span data-stu-id="2f3d9-118">A run-time error is generated if it is used with <strong>adModeShareDenyNone</strong> only.</span></span> <span data-ttu-id="2f3d9-119">Однако его можно использовать с <strong>adModeShareDenyNone</strong> в сочетании с другими значениями.</span><span class="sxs-lookup"><span data-stu-id="2f3d9-119">However, it can be used with <strong>adModeShareDenyNone</strong> when combined with other values.</span></span> <span data-ttu-id="2f3d9-120">Например, можно использовать &quot; <strong>adModeRead</strong> или <strong>adModeShareDenyNone</strong> или <strong>adModeRecursive.</strong> &quot;</span><span class="sxs-lookup"><span data-stu-id="2f3d9-120">For example, you can use &quot;<strong>adModeRead</strong> or <strong>adModeShareDenyNone</strong> or <strong>adModeRecursive</strong>&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f3d9-121"><strong>adModeShareDenyNone</strong></span><span class="sxs-lookup"><span data-stu-id="2f3d9-121"><strong>adModeShareDenyNone</strong></span></span></p></td>
<td><p><span data-ttu-id="2f3d9-122">16 </span><span class="sxs-lookup"><span data-stu-id="2f3d9-122">16</span></span></p></td>
<td><p><span data-ttu-id="2f3d9-123">Позволяет другим пользователям открывать подключение с любыми разрешениями.</span><span class="sxs-lookup"><span data-stu-id="2f3d9-123">Allows others to open a connection with any permissions.</span></span> <span data-ttu-id="2f3d9-124">Другим не может быть отказано в доступе на чтение и записи.</span><span class="sxs-lookup"><span data-stu-id="2f3d9-124">Neither read nor write access can be denied to others.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f3d9-125"><strong>adModeShareDenyRead</strong></span><span class="sxs-lookup"><span data-stu-id="2f3d9-125"><strong>adModeShareDenyRead</strong></span></span></p></td>
<td><p><span data-ttu-id="2f3d9-126">4 </span><span class="sxs-lookup"><span data-stu-id="2f3d9-126">4</span></span></p></td>
<td><p><span data-ttu-id="2f3d9-127">Запретить другим людям открывать подключение с разрешениями на чтение.</span><span class="sxs-lookup"><span data-stu-id="2f3d9-127">Prevents others from opening a connection with read permissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f3d9-128"><strong>adModeShareDenyWrite</strong></span><span class="sxs-lookup"><span data-stu-id="2f3d9-128"><strong>adModeShareDenyWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="2f3d9-129">8 </span><span class="sxs-lookup"><span data-stu-id="2f3d9-129">8</span></span></p></td>
<td><p><span data-ttu-id="2f3d9-130">Запретить другим людям открывать подключение с разрешениями на записи.</span><span class="sxs-lookup"><span data-stu-id="2f3d9-130">Prevents others from opening a connection with write permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f3d9-131"><strong>adModeShareExclusive</strong></span><span class="sxs-lookup"><span data-stu-id="2f3d9-131"><strong>adModeShareExclusive</strong></span></span></p></td>
<td><p><span data-ttu-id="2f3d9-132">12 </span><span class="sxs-lookup"><span data-stu-id="2f3d9-132">12</span></span></p></td>
<td><p><span data-ttu-id="2f3d9-133">Запретить другим людям открывать подключение.</span><span class="sxs-lookup"><span data-stu-id="2f3d9-133">Prevents others from opening a connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f3d9-134"><strong>adModeUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="2f3d9-134"><strong>adModeUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="2f3d9-135">0</span><span class="sxs-lookup"><span data-stu-id="2f3d9-135">0</span></span></p></td>
<td><p><span data-ttu-id="2f3d9-136">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2f3d9-136">Default.</span></span> <span data-ttu-id="2f3d9-137">Указывает, что разрешения еще не установлены или не могут быть определены.</span><span class="sxs-lookup"><span data-stu-id="2f3d9-137">Indicates that the permissions have not yet been set or cannot be determined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f3d9-138"><strong>adModeWrite</strong></span><span class="sxs-lookup"><span data-stu-id="2f3d9-138"><strong>adModeWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="2f3d9-139">2 </span><span class="sxs-lookup"><span data-stu-id="2f3d9-139">2</span></span></p></td>
<td><p><span data-ttu-id="2f3d9-140">Указывает разрешения только для записи.</span><span class="sxs-lookup"><span data-stu-id="2f3d9-140">Indicates write-only permissions.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="2f3d9-141">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="2f3d9-141">ADO/WFC equivalent</span></span>

<span data-ttu-id="2f3d9-142">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="2f3d9-142">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2f3d9-143">Константа</span><span class="sxs-lookup"><span data-stu-id="2f3d9-143">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2f3d9-144">AdoEnums.ConnectMode.READ</span><span class="sxs-lookup"><span data-stu-id="2f3d9-144">AdoEnums.ConnectMode.READ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f3d9-145">AdoEnums.ConnectMode.READWRITE</span><span class="sxs-lookup"><span data-stu-id="2f3d9-145">AdoEnums.ConnectMode.READWRITE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f3d9-146">(Нет эквивалента AdoEnums.ConnectMode.RECURSIVE)</span><span class="sxs-lookup"><span data-stu-id="2f3d9-146">(There is no equivalent of AdoEnums.ConnectMode.RECURSIVE)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f3d9-147">AdoEnums.ConnectMode.SHAREDENYNONE</span><span class="sxs-lookup"><span data-stu-id="2f3d9-147">AdoEnums.ConnectMode.SHAREDENYNONE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f3d9-148">AdoEnums.ConnectMode.SHAREDENYREAD</span><span class="sxs-lookup"><span data-stu-id="2f3d9-148">AdoEnums.ConnectMode.SHAREDENYREAD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f3d9-149">AdoEnums.ConnectMode.SHAREDENYWRITE</span><span class="sxs-lookup"><span data-stu-id="2f3d9-149">AdoEnums.ConnectMode.SHAREDENYWRITE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f3d9-150">AdoEnums.ConnectMode.SHAREEXCLUSIVE</span><span class="sxs-lookup"><span data-stu-id="2f3d9-150">AdoEnums.ConnectMode.SHAREEXCLUSIVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f3d9-151">AdoEnums.ConnectMode.UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="2f3d9-151">AdoEnums.ConnectMode.UNKNOWN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f3d9-152">AdoEnums.ConnectMode.WRITE</span><span class="sxs-lookup"><span data-stu-id="2f3d9-152">AdoEnums.ConnectMode.WRITE</span></span></p></td>
</tr>
</tbody>
</table>

