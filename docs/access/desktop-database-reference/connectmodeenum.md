---
title: ConnectModeEnum (Справочник по для настольных баз данных Access)
TOCTitle: ConnectModeEnum
ms:assetid: a15aa733-f899-5fe9-e705-67a4301706d1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249743(v=office.15)
ms:contentKeyID: 48546728
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 453d84e687a31f7df5082e17b80fe2a1bda756be
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708664"
---
# <a name="connectmodeenum"></a><span data-ttu-id="b1d38-102">ConnectModeEnum</span><span class="sxs-lookup"><span data-stu-id="b1d38-102">ConnectModeEnum</span></span>

<span data-ttu-id="b1d38-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b1d38-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b1d38-104">Задает разрешения, доступные для изменения данных в [подключения](connection-object-ado.md), открытие [записи](record-object-ado.md)или указания значения для свойства [режима](mode-property-ado.md) объектов [потока](stream-object-ado.md) и **запись** .</span><span class="sxs-lookup"><span data-stu-id="b1d38-104">Specifies the available permissions for modifying data in a [Connection](connection-object-ado.md), opening a [Record](record-object-ado.md), or specifying values for the [Mode](mode-property-ado.md) property of the **Record** and [Stream](stream-object-ado.md) objects.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b1d38-105">Константа</span><span class="sxs-lookup"><span data-stu-id="b1d38-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="b1d38-106">Значение</span><span class="sxs-lookup"><span data-stu-id="b1d38-106">Value</span></span></p></th>
<th><p><span data-ttu-id="b1d38-107">Описание</span><span class="sxs-lookup"><span data-stu-id="b1d38-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b1d38-108"><strong>adModeRead</strong></span><span class="sxs-lookup"><span data-stu-id="b1d38-108"><strong>adModeRead</strong></span></span></p></td>
<td><p><span data-ttu-id="b1d38-109">1</span><span class="sxs-lookup"><span data-stu-id="b1d38-109">1</span></span></p></td>
<td><p><span data-ttu-id="b1d38-110">Указывает разрешения только для чтения.</span><span class="sxs-lookup"><span data-stu-id="b1d38-110">Indicates read-only permissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1d38-111"><strong>adModeReadWrite</strong></span><span class="sxs-lookup"><span data-stu-id="b1d38-111"><strong>adModeReadWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="b1d38-112">3</span><span class="sxs-lookup"><span data-stu-id="b1d38-112">3</span></span></p></td>
<td><p><span data-ttu-id="b1d38-113">Указывает разрешения на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="b1d38-113">Indicates read/write permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1d38-114"><strong>adModeRecursive</strong></span><span class="sxs-lookup"><span data-stu-id="b1d38-114"><strong>adModeRecursive</strong></span></span></p></td>
<td><p><span data-ttu-id="b1d38-115">0x400000</span><span class="sxs-lookup"><span data-stu-id="b1d38-115">0x400000</span></span></p></td>
<td><p><span data-ttu-id="b1d38-116">Используется в сочетании с другими <em>*ShareDeny*</em> значения (<strong>adModeShareDenyNone</strong>, <strong>adModeShareDenyWrite</strong>или <strong>adModeShareDenyRead</strong>) для распространения ограничения общего доступа ко всем дочерним записям текущей <strong>записи</strong>.</span><span class="sxs-lookup"><span data-stu-id="b1d38-116">Used in conjunction with the other <em>*ShareDeny*</em> values (<strong>adModeShareDenyNone</strong>, <strong>adModeShareDenyWrite</strong>, or <strong>adModeShareDenyRead</strong>) to propagate sharing restrictions to all sub-records of the current <strong>Record</strong>.</span></span> <span data-ttu-id="b1d38-117">Он не оказывает воздействия, если <strong>запись</strong> не имеет дочерние элементы.</span><span class="sxs-lookup"><span data-stu-id="b1d38-117">It has no affect if the <strong>Record</strong> does not have any children.</span></span></p><p><span data-ttu-id="b1d38-118">При использовании с <strong>adModeShareDenyNone</strong> только создается ошибку времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="b1d38-118">A run-time error is generated if it is used with <strong>adModeShareDenyNone</strong> only.</span></span> <span data-ttu-id="b1d38-119">Тем не менее его можно использовать с <strong>adModeShareDenyNone</strong> в сочетании с другими значениями.</span><span class="sxs-lookup"><span data-stu-id="b1d38-119">However, it can be used with <strong>adModeShareDenyNone</strong> when combined with other values.</span></span> <span data-ttu-id="b1d38-120">Например, можно использовать &quot; <strong>adModeRead</strong> или <strong>adModeShareDenyNone</strong> или <strong>adModeRecursive</strong>&quot;.</span><span class="sxs-lookup"><span data-stu-id="b1d38-120">For example, you can use &quot;<strong>adModeRead</strong> or <strong>adModeShareDenyNone</strong> or <strong>adModeRecursive</strong>&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1d38-121"><strong>adModeShareDenyNone</strong></span><span class="sxs-lookup"><span data-stu-id="b1d38-121"><strong>adModeShareDenyNone</strong></span></span></p></td>
<td><p><span data-ttu-id="b1d38-122">16</span><span class="sxs-lookup"><span data-stu-id="b1d38-122">16</span></span></p></td>
<td><p><span data-ttu-id="b1d38-123">Позволяет другим пользователям открывать соединение с другими разрешениями.</span><span class="sxs-lookup"><span data-stu-id="b1d38-123">Allows others to open a connection with any permissions.</span></span> <span data-ttu-id="b1d38-124">Доступ на запись ни чтения можно запретить другим пользователям.</span><span class="sxs-lookup"><span data-stu-id="b1d38-124">Neither read nor write access can be denied to others.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1d38-125"><strong>adModeShareDenyRead</strong></span><span class="sxs-lookup"><span data-stu-id="b1d38-125"><strong>adModeShareDenyRead</strong></span></span></p></td>
<td><p><span data-ttu-id="b1d38-126">4</span><span class="sxs-lookup"><span data-stu-id="b1d38-126">4</span></span></p></td>
<td><p><span data-ttu-id="b1d38-127">Запрет другим пользователям открывать соединение с разрешениями на чтение.</span><span class="sxs-lookup"><span data-stu-id="b1d38-127">Prevents others from opening a connection with read permissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1d38-128"><strong>adModeShareDenyWrite</strong></span><span class="sxs-lookup"><span data-stu-id="b1d38-128"><strong>adModeShareDenyWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="b1d38-129">8</span><span class="sxs-lookup"><span data-stu-id="b1d38-129">8</span></span></p></td>
<td><p><span data-ttu-id="b1d38-130">Запрет другим пользователям открывать соединение с разрешениями на запись.</span><span class="sxs-lookup"><span data-stu-id="b1d38-130">Prevents others from opening a connection with write permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1d38-131"><strong>adModeShareExclusive</strong></span><span class="sxs-lookup"><span data-stu-id="b1d38-131"><strong>adModeShareExclusive</strong></span></span></p></td>
<td><p><span data-ttu-id="b1d38-132">12</span><span class="sxs-lookup"><span data-stu-id="b1d38-132">12</span></span></p></td>
<td><p><span data-ttu-id="b1d38-133">Запрет другим пользователям открывать подключения.</span><span class="sxs-lookup"><span data-stu-id="b1d38-133">Prevents others from opening a connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1d38-134"><strong>adModeUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="b1d38-134"><strong>adModeUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="b1d38-135">0</span><span class="sxs-lookup"><span data-stu-id="b1d38-135">0</span></span></p></td>
<td><p><span data-ttu-id="b1d38-136">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b1d38-136">Default.</span></span> <span data-ttu-id="b1d38-137">Показывает, что разрешения еще не были настроены или не может быть определен.</span><span class="sxs-lookup"><span data-stu-id="b1d38-137">Indicates that the permissions have not yet been set or cannot be determined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1d38-138"><strong>adModeWrite</strong></span><span class="sxs-lookup"><span data-stu-id="b1d38-138"><strong>adModeWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="b1d38-139">2</span><span class="sxs-lookup"><span data-stu-id="b1d38-139">2</span></span></p></td>
<td><p><span data-ttu-id="b1d38-140">Указывает разрешения только для записи.</span><span class="sxs-lookup"><span data-stu-id="b1d38-140">Indicates write-only permissions.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="b1d38-141">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="b1d38-141">ADO/WFC equivalent</span></span>

<span data-ttu-id="b1d38-142">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="b1d38-142">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b1d38-143">Константа</span><span class="sxs-lookup"><span data-stu-id="b1d38-143">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b1d38-144">AdoEnums.ConnectMode.READ</span><span class="sxs-lookup"><span data-stu-id="b1d38-144">AdoEnums.ConnectMode.READ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1d38-145">AdoEnums.ConnectMode.READWRITE</span><span class="sxs-lookup"><span data-stu-id="b1d38-145">AdoEnums.ConnectMode.READWRITE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1d38-146">(Нет эквивалента AdoEnums.ConnectMode.RECURSIVE)</span><span class="sxs-lookup"><span data-stu-id="b1d38-146">(There is no equivalent of AdoEnums.ConnectMode.RECURSIVE)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1d38-147">AdoEnums.ConnectMode.SHAREDENYNONE</span><span class="sxs-lookup"><span data-stu-id="b1d38-147">AdoEnums.ConnectMode.SHAREDENYNONE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1d38-148">AdoEnums.ConnectMode.SHAREDENYREAD</span><span class="sxs-lookup"><span data-stu-id="b1d38-148">AdoEnums.ConnectMode.SHAREDENYREAD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1d38-149">AdoEnums.ConnectMode.SHAREDENYWRITE</span><span class="sxs-lookup"><span data-stu-id="b1d38-149">AdoEnums.ConnectMode.SHAREDENYWRITE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1d38-150">AdoEnums.ConnectMode.SHAREEXCLUSIVE</span><span class="sxs-lookup"><span data-stu-id="b1d38-150">AdoEnums.ConnectMode.SHAREEXCLUSIVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1d38-151">AdoEnums.ConnectMode.UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="b1d38-151">AdoEnums.ConnectMode.UNKNOWN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1d38-152">AdoEnums.ConnectMode.WRITE</span><span class="sxs-lookup"><span data-stu-id="b1d38-152">AdoEnums.ConnectMode.WRITE</span></span></p></td>
</tr>
</tbody>
</table>

