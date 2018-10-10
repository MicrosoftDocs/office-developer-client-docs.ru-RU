---
title: ConnectModeEnum (Справочник по для настольных баз данных Access)
TOCTitle: ConnectModeEnum
ms:assetid: a15aa733-f899-5fe9-e705-67a4301706d1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249743(v=office.15)
ms:contentKeyID: 48546728
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5b39fc42259a1906891b82bf9b9ef252997e6240
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482667"
---
# <a name="connectmodeenum"></a><span data-ttu-id="54bf6-102">ConnectModeEnum</span><span class="sxs-lookup"><span data-stu-id="54bf6-102">ConnectModeEnum</span></span>


<span data-ttu-id="54bf6-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="54bf6-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="54bf6-104">Задает разрешения, доступные для изменения данных в [подключения](connection-object-ado.md), открытие [записи](record-object-ado.md)или указания значения для свойства [режима](mode-property-ado.md) объектов [потока](stream-object-ado.md) и **запись** .</span><span class="sxs-lookup"><span data-stu-id="54bf6-104">Specifies the available permissions for modifying data in a [Connection](connection-object-ado.md), opening a [Record](record-object-ado.md), or specifying values for the [Mode](mode-property-ado.md) property of the **Record** and [Stream](stream-object-ado.md) objects.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="54bf6-105">Константа</span><span class="sxs-lookup"><span data-stu-id="54bf6-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="54bf6-106">Значение</span><span class="sxs-lookup"><span data-stu-id="54bf6-106">Value</span></span></p></th>
<th><p><span data-ttu-id="54bf6-107">Описание</span><span class="sxs-lookup"><span data-stu-id="54bf6-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="54bf6-108"><strong>adModeRead</strong></span><span class="sxs-lookup"><span data-stu-id="54bf6-108"><strong>adModeRead</strong></span></span></p></td>
<td><p><span data-ttu-id="54bf6-109">1</span><span class="sxs-lookup"><span data-stu-id="54bf6-109">1</span></span></p></td>
<td><p><span data-ttu-id="54bf6-110">Указывает разрешения только для чтения.</span><span class="sxs-lookup"><span data-stu-id="54bf6-110">Indicates read-only permissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54bf6-111"><strong>adModeReadWrite</strong></span><span class="sxs-lookup"><span data-stu-id="54bf6-111"><strong>adModeReadWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="54bf6-112">3</span><span class="sxs-lookup"><span data-stu-id="54bf6-112">3</span></span></p></td>
<td><p><span data-ttu-id="54bf6-113">Указывает разрешения на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="54bf6-113">Indicates read/write permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54bf6-114"><strong>adModeRecursive</strong></span><span class="sxs-lookup"><span data-stu-id="54bf6-114"><strong>adModeRecursive</strong></span></span></p></td>
<td><p><span data-ttu-id="54bf6-115">0x400000</span><span class="sxs-lookup"><span data-stu-id="54bf6-115">0x400000</span></span></p></td>
<td><p><span data-ttu-id="54bf6-116">Используется в сочетании с другими <em>*ShareDeny*</em> значения (<strong>adModeShareDenyNone</strong>, <strong>adModeShareDenyWrite</strong>или <strong>adModeShareDenyRead</strong>) для распространения ограничения общего доступа ко всем дочерним записям текущей <strong>записи</strong>.</span><span class="sxs-lookup"><span data-stu-id="54bf6-116">Used in conjunction with the other <em>*ShareDeny*</em> values (<strong>adModeShareDenyNone</strong>, <strong>adModeShareDenyWrite</strong>, or <strong>adModeShareDenyRead</strong>) to propagate sharing restrictions to all sub-records of the current <strong>Record</strong>.</span></span> <span data-ttu-id="54bf6-117">Он не оказывает воздействия, если <strong>запись</strong> не имеет дочерние элементы.</span><span class="sxs-lookup"><span data-stu-id="54bf6-117">It has no affect if the <strong>Record</strong> does not have any children.</span></span> <span data-ttu-id="54bf6-118">При использовании с <strong>adModeShareDenyNone</strong> только создается ошибку времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="54bf6-118">A run-time error is generated if it is used with <strong>adModeShareDenyNone</strong> only.</span></span> <span data-ttu-id="54bf6-119">Тем не менее его можно использовать с <strong>adModeShareDenyNone</strong> в сочетании с другими значениями.</span><span class="sxs-lookup"><span data-stu-id="54bf6-119">However, it can be used with <strong>adModeShareDenyNone</strong> when combined with other values.</span></span> <span data-ttu-id="54bf6-120">Например, можно использовать &quot; <strong>adModeRead</strong> или <strong>adModeShareDenyNone</strong> или <strong>adModeRecursive</strong>&quot;.</span><span class="sxs-lookup"><span data-stu-id="54bf6-120">For example, you can use &quot;<strong>adModeRead</strong> Or <strong>adModeShareDenyNone</strong> Or <strong>adModeRecursive</strong>&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54bf6-121"><strong>adModeShareDenyNone</strong></span><span class="sxs-lookup"><span data-stu-id="54bf6-121"><strong>adModeShareDenyNone</strong></span></span></p></td>
<td><p><span data-ttu-id="54bf6-122">16</span><span class="sxs-lookup"><span data-stu-id="54bf6-122">16</span></span></p></td>
<td><p><span data-ttu-id="54bf6-123">Позволяет другим пользователям открывать соединение с другими разрешениями.</span><span class="sxs-lookup"><span data-stu-id="54bf6-123">Allows others to open a connection with any permissions.</span></span> <span data-ttu-id="54bf6-124">Доступ на запись ни чтения можно запретить другим пользователям.</span><span class="sxs-lookup"><span data-stu-id="54bf6-124">Neither read nor write access can be denied to others.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54bf6-125"><strong>adModeShareDenyRead</strong></span><span class="sxs-lookup"><span data-stu-id="54bf6-125"><strong>adModeShareDenyRead</strong></span></span></p></td>
<td><p><span data-ttu-id="54bf6-126">4</span><span class="sxs-lookup"><span data-stu-id="54bf6-126">4</span></span></p></td>
<td><p><span data-ttu-id="54bf6-127">Запрет другим пользователям открывать соединение с разрешениями на чтение.</span><span class="sxs-lookup"><span data-stu-id="54bf6-127">Prevents others from opening a connection with read permissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54bf6-128"><strong>adModeShareDenyWrite</strong></span><span class="sxs-lookup"><span data-stu-id="54bf6-128"><strong>adModeShareDenyWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="54bf6-129">8</span><span class="sxs-lookup"><span data-stu-id="54bf6-129">8</span></span></p></td>
<td><p><span data-ttu-id="54bf6-130">Запрет другим пользователям открывать соединение с разрешениями на запись.</span><span class="sxs-lookup"><span data-stu-id="54bf6-130">Prevents others from opening a connection with write permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54bf6-131"><strong>adModeShareExclusive</strong></span><span class="sxs-lookup"><span data-stu-id="54bf6-131"><strong>adModeShareExclusive</strong></span></span></p></td>
<td><p><span data-ttu-id="54bf6-132">12</span><span class="sxs-lookup"><span data-stu-id="54bf6-132">12</span></span></p></td>
<td><p><span data-ttu-id="54bf6-133">Запрет другим пользователям открывать подключения.</span><span class="sxs-lookup"><span data-stu-id="54bf6-133">Prevents others from opening a connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54bf6-134"><strong>adModeUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="54bf6-134"><strong>adModeUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="54bf6-135">0</span><span class="sxs-lookup"><span data-stu-id="54bf6-135">0</span></span></p></td>
<td><p><span data-ttu-id="54bf6-136">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="54bf6-136">Default.</span></span> <span data-ttu-id="54bf6-137">Показывает, что разрешения еще не были настроены или не может быть определен.</span><span class="sxs-lookup"><span data-stu-id="54bf6-137">Indicates that the permissions have not yet been set or cannot be determined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54bf6-138"><strong>adModeWrite</strong></span><span class="sxs-lookup"><span data-stu-id="54bf6-138"><strong>adModeWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="54bf6-139">2</span><span class="sxs-lookup"><span data-stu-id="54bf6-139">2</span></span></p></td>
<td><p><span data-ttu-id="54bf6-140">Указывает разрешения только для записи.</span><span class="sxs-lookup"><span data-stu-id="54bf6-140">Indicates write-only permissions.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="54bf6-141">**Эквивалент ADO/WFC**</span><span class="sxs-lookup"><span data-stu-id="54bf6-141">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="54bf6-142">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="54bf6-142">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="54bf6-143">Constant</span><span class="sxs-lookup"><span data-stu-id="54bf6-143">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="54bf6-144">AdoEnums.ConnectMode.READ</span><span class="sxs-lookup"><span data-stu-id="54bf6-144">AdoEnums.ConnectMode.READ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54bf6-145">AdoEnums.ConnectMode.READWRITE</span><span class="sxs-lookup"><span data-stu-id="54bf6-145">AdoEnums.ConnectMode.READWRITE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54bf6-146">(Нет эквивалента AdoEnums.ConnectMode.RECURSIVE)</span><span class="sxs-lookup"><span data-stu-id="54bf6-146">(There is no equivalent of AdoEnums.ConnectMode.RECURSIVE)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54bf6-147">AdoEnums.ConnectMode.SHAREDENYNONE</span><span class="sxs-lookup"><span data-stu-id="54bf6-147">AdoEnums.ConnectMode.SHAREDENYNONE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54bf6-148">AdoEnums.ConnectMode.SHAREDENYREAD</span><span class="sxs-lookup"><span data-stu-id="54bf6-148">AdoEnums.ConnectMode.SHAREDENYREAD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54bf6-149">AdoEnums.ConnectMode.SHAREDENYWRITE</span><span class="sxs-lookup"><span data-stu-id="54bf6-149">AdoEnums.ConnectMode.SHAREDENYWRITE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54bf6-150">AdoEnums.ConnectMode.SHAREEXCLUSIVE</span><span class="sxs-lookup"><span data-stu-id="54bf6-150">AdoEnums.ConnectMode.SHAREEXCLUSIVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54bf6-151">AdoEnums.ConnectMode.UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="54bf6-151">AdoEnums.ConnectMode.UNKNOWN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54bf6-152">AdoEnums.ConnectMode.WRITE</span><span class="sxs-lookup"><span data-stu-id="54bf6-152">AdoEnums.ConnectMode.WRITE</span></span></p></td>
</tr>
</tbody>
</table>

