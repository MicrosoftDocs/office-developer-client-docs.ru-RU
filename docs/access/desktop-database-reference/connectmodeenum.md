---
title: ConnectModeEnum (ссылка на настольные базы данных доступа)
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
# <a name="connectmodeenum"></a><span data-ttu-id="15593-102">ConnectModeEnum</span><span class="sxs-lookup"><span data-stu-id="15593-102">ConnectModeEnum</span></span>

<span data-ttu-id="15593-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="15593-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="15593-104">Указывает доступные разрешения на изменение данных в [подключениях,](connection-object-ado.md)открытие записи [или](record-object-ado.md)указание значений для свойства [Mode](mode-property-ado.md) объектов **Record** и [Stream.](stream-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="15593-104">Specifies the available permissions for modifying data in a [Connection](connection-object-ado.md), opening a [Record](record-object-ado.md), or specifying values for the [Mode](mode-property-ado.md) property of the **Record** and [Stream](stream-object-ado.md) objects.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="15593-105">Константа</span><span class="sxs-lookup"><span data-stu-id="15593-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="15593-106">Значение</span><span class="sxs-lookup"><span data-stu-id="15593-106">Value</span></span></p></th>
<th><p><span data-ttu-id="15593-107">Описание</span><span class="sxs-lookup"><span data-stu-id="15593-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="15593-108"><strong>adModeRead</strong></span><span class="sxs-lookup"><span data-stu-id="15593-108"><strong>adModeRead</strong></span></span></p></td>
<td><p><span data-ttu-id="15593-109">1</span><span class="sxs-lookup"><span data-stu-id="15593-109">1</span></span></p></td>
<td><p><span data-ttu-id="15593-110">Указывает разрешения только для чтения.</span><span class="sxs-lookup"><span data-stu-id="15593-110">Indicates read-only permissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15593-111"><strong>adModeReadWrite</strong></span><span class="sxs-lookup"><span data-stu-id="15593-111"><strong>adModeReadWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="15593-112">3</span><span class="sxs-lookup"><span data-stu-id="15593-112">3</span></span></p></td>
<td><p><span data-ttu-id="15593-113">Указывает разрешения на чтение и записи.</span><span class="sxs-lookup"><span data-stu-id="15593-113">Indicates read/write permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15593-114"><strong>adModeRecursive</strong></span><span class="sxs-lookup"><span data-stu-id="15593-114"><strong>adModeRecursive</strong></span></span></p></td>
<td><p><span data-ttu-id="15593-115">0x400000</span><span class="sxs-lookup"><span data-stu-id="15593-115">0x400000</span></span></p></td>
<td><p><span data-ttu-id="15593-116">Используется в сочетании с другими значениями <em>*ShareDeny*</em> <strong>(adModeShareDenyNone,</strong> <strong>adModeShareDenyWrite</strong>или <strong>adModeShareDenyRead)</strong>для распространения ограничений общего доступа ко всем подп. записям текущей <strong>записи</strong>.</span><span class="sxs-lookup"><span data-stu-id="15593-116">Used in conjunction with the other <em>*ShareDeny*</em> values (<strong>adModeShareDenyNone</strong>, <strong>adModeShareDenyWrite</strong>, or <strong>adModeShareDenyRead</strong>) to propagate sharing restrictions to all sub-records of the current <strong>Record</strong>.</span></span> <span data-ttu-id="15593-117">Это не влияет, если <strong>запись</strong> не имеет детей.</span><span class="sxs-lookup"><span data-stu-id="15593-117">It has no affect if the <strong>Record</strong> does not have any children.</span></span></p><p><span data-ttu-id="15593-118">Ошибка времени запуска создается, если она используется только <strong>с помощью adModeShareDenyNone.</strong></span><span class="sxs-lookup"><span data-stu-id="15593-118">A run-time error is generated if it is used with <strong>adModeShareDenyNone</strong> only.</span></span> <span data-ttu-id="15593-119">Однако его можно использовать с <strong>помощью adModeShareDenyNone</strong> в сочетании с другими значениями.</span><span class="sxs-lookup"><span data-stu-id="15593-119">However, it can be used with <strong>adModeShareDenyNone</strong> when combined with other values.</span></span> <span data-ttu-id="15593-120">Например, можно использовать &quot; <strong>adModeRead</strong> или <strong>adModeShareDenyNone</strong> или <strong>adModeRecursive.</strong> &quot;</span><span class="sxs-lookup"><span data-stu-id="15593-120">For example, you can use &quot;<strong>adModeRead</strong> or <strong>adModeShareDenyNone</strong> or <strong>adModeRecursive</strong>&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15593-121"><strong>adModeShareDenyNone</strong></span><span class="sxs-lookup"><span data-stu-id="15593-121"><strong>adModeShareDenyNone</strong></span></span></p></td>
<td><p><span data-ttu-id="15593-122">16 </span><span class="sxs-lookup"><span data-stu-id="15593-122">16</span></span></p></td>
<td><p><span data-ttu-id="15593-123">Позволяет другим открыть подключение с любыми разрешениями.</span><span class="sxs-lookup"><span data-stu-id="15593-123">Allows others to open a connection with any permissions.</span></span> <span data-ttu-id="15593-124">Другим не может быть отказано в доступе к чтениям и записи.</span><span class="sxs-lookup"><span data-stu-id="15593-124">Neither read nor write access can be denied to others.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15593-125"><strong>adModeShareDenyRead</strong></span><span class="sxs-lookup"><span data-stu-id="15593-125"><strong>adModeShareDenyRead</strong></span></span></p></td>
<td><p><span data-ttu-id="15593-126">4 </span><span class="sxs-lookup"><span data-stu-id="15593-126">4</span></span></p></td>
<td><p><span data-ttu-id="15593-127">Не позволяет другим открывать подключение с разрешениями на чтение.</span><span class="sxs-lookup"><span data-stu-id="15593-127">Prevents others from opening a connection with read permissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15593-128"><strong>adModeShareDenyWrite</strong></span><span class="sxs-lookup"><span data-stu-id="15593-128"><strong>adModeShareDenyWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="15593-129">8 </span><span class="sxs-lookup"><span data-stu-id="15593-129">8</span></span></p></td>
<td><p><span data-ttu-id="15593-130">Не позволяет другим открывать подключение с разрешениями на записи.</span><span class="sxs-lookup"><span data-stu-id="15593-130">Prevents others from opening a connection with write permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15593-131"><strong>adModeShareExclusive</strong></span><span class="sxs-lookup"><span data-stu-id="15593-131"><strong>adModeShareExclusive</strong></span></span></p></td>
<td><p><span data-ttu-id="15593-132">12 </span><span class="sxs-lookup"><span data-stu-id="15593-132">12</span></span></p></td>
<td><p><span data-ttu-id="15593-133">Предотвращает открытие подключения другими.</span><span class="sxs-lookup"><span data-stu-id="15593-133">Prevents others from opening a connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15593-134"><strong>adModeUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="15593-134"><strong>adModeUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="15593-135">0</span><span class="sxs-lookup"><span data-stu-id="15593-135">0</span></span></p></td>
<td><p><span data-ttu-id="15593-136">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="15593-136">Default.</span></span> <span data-ttu-id="15593-137">Указывает, что разрешения еще не установлены или не могут быть определены.</span><span class="sxs-lookup"><span data-stu-id="15593-137">Indicates that the permissions have not yet been set or cannot be determined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15593-138"><strong>adModeWrite</strong></span><span class="sxs-lookup"><span data-stu-id="15593-138"><strong>adModeWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="15593-139">2</span><span class="sxs-lookup"><span data-stu-id="15593-139">2</span></span></p></td>
<td><p><span data-ttu-id="15593-140">Указывает разрешения только для записи.</span><span class="sxs-lookup"><span data-stu-id="15593-140">Indicates write-only permissions.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="15593-141">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="15593-141">ADO/WFC equivalent</span></span>

<span data-ttu-id="15593-142">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="15593-142">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="15593-143">Константа</span><span class="sxs-lookup"><span data-stu-id="15593-143">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="15593-144">AdoEnums.ConnectMode.READ</span><span class="sxs-lookup"><span data-stu-id="15593-144">AdoEnums.ConnectMode.READ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15593-145">AdoEnums.ConnectMode.READWRITE</span><span class="sxs-lookup"><span data-stu-id="15593-145">AdoEnums.ConnectMode.READWRITE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15593-146">(Нет эквивалента AdoEnums.ConnectMode.RECURSIVE)</span><span class="sxs-lookup"><span data-stu-id="15593-146">(There is no equivalent of AdoEnums.ConnectMode.RECURSIVE)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15593-147">AdoEnums.ConnectMode.SHAREDENYNONE</span><span class="sxs-lookup"><span data-stu-id="15593-147">AdoEnums.ConnectMode.SHAREDENYNONE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15593-148">AdoEnums.ConnectMode.SHAREDENYREAD</span><span class="sxs-lookup"><span data-stu-id="15593-148">AdoEnums.ConnectMode.SHAREDENYREAD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15593-149">AdoEnums.ConnectMode.SHAREDENYWRITE</span><span class="sxs-lookup"><span data-stu-id="15593-149">AdoEnums.ConnectMode.SHAREDENYWRITE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15593-150">AdoEnums.ConnectMode.SHAREEXCLUSIVE</span><span class="sxs-lookup"><span data-stu-id="15593-150">AdoEnums.ConnectMode.SHAREEXCLUSIVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15593-151">AdoEnums.ConnectMode.UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="15593-151">AdoEnums.ConnectMode.UNKNOWN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15593-152">AdoEnums.ConnectMode.WRITE</span><span class="sxs-lookup"><span data-stu-id="15593-152">AdoEnums.ConnectMode.WRITE</span></span></p></td>
</tr>
</tbody>
</table>

