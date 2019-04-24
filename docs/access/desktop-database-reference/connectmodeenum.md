---
title: Коннектмодинум (Справочник по базам данных Access на компьютере)
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
# <a name="connectmodeenum"></a><span data-ttu-id="ce0e6-102">ConnectModeEnum</span><span class="sxs-lookup"><span data-stu-id="ce0e6-102">ConnectModeEnum</span></span>

<span data-ttu-id="ce0e6-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ce0e6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ce0e6-104">Указывает доступные разрешения для изменения данных в [подключении](connection-object-ado.md), открытия [записи](record-object-ado.md)или указания значений для свойства [mode](mode-property-ado.md) объектов **Record** и [Stream](stream-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="ce0e6-104">Specifies the available permissions for modifying data in a [Connection](connection-object-ado.md), opening a [Record](record-object-ado.md), or specifying values for the [Mode](mode-property-ado.md) property of the **Record** and [Stream](stream-object-ado.md) objects.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ce0e6-105">Константа</span><span class="sxs-lookup"><span data-stu-id="ce0e6-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="ce0e6-106">Значение</span><span class="sxs-lookup"><span data-stu-id="ce0e6-106">Value</span></span></p></th>
<th><p><span data-ttu-id="ce0e6-107">Описание</span><span class="sxs-lookup"><span data-stu-id="ce0e6-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ce0e6-108"><strong>Адмодереад</strong></span><span class="sxs-lookup"><span data-stu-id="ce0e6-108"><strong>adModeRead</strong></span></span></p></td>
<td><p><span data-ttu-id="ce0e6-109">1,1</span><span class="sxs-lookup"><span data-stu-id="ce0e6-109">1</span></span></p></td>
<td><p><span data-ttu-id="ce0e6-110">Указывает разрешения только на чтение.</span><span class="sxs-lookup"><span data-stu-id="ce0e6-110">Indicates read-only permissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce0e6-111"><strong>Адмодереадврите</strong></span><span class="sxs-lookup"><span data-stu-id="ce0e6-111"><strong>adModeReadWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="ce0e6-112">4</span><span class="sxs-lookup"><span data-stu-id="ce0e6-112">3</span></span></p></td>
<td><p><span data-ttu-id="ce0e6-113">Указывает разрешения на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="ce0e6-113">Indicates read/write permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce0e6-114"><strong>Адмодерекурсиве</strong></span><span class="sxs-lookup"><span data-stu-id="ce0e6-114"><strong>adModeRecursive</strong></span></span></p></td>
<td><p><span data-ttu-id="ce0e6-115">0x400000</span><span class="sxs-lookup"><span data-stu-id="ce0e6-115">0x400000</span></span></p></td>
<td><p><span data-ttu-id="ce0e6-116">Используется совместно с другими значениями <em>*шаредени*</em> (<strong>адмодешаредениноне</strong>, <strong>адмодешаредениврите</strong>или <strong>адмодешаредениреад</strong>) для распространения ограничений общего доступа ко всем вложенным записям текущей <strong>записи</strong>.</span><span class="sxs-lookup"><span data-stu-id="ce0e6-116">Used in conjunction with the other <em>*ShareDeny*</em> values (<strong>adModeShareDenyNone</strong>, <strong>adModeShareDenyWrite</strong>, or <strong>adModeShareDenyRead</strong>) to propagate sharing restrictions to all sub-records of the current <strong>Record</strong>.</span></span> <span data-ttu-id="ce0e6-117">Он не оказывает влияния, если у <strong>записи</strong> нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="ce0e6-117">It has no affect if the <strong>Record</strong> does not have any children.</span></span></p><p><span data-ttu-id="ce0e6-118">Ошибка во время выполнения создается, если она используется только с <strong>адмодешаредениноне</strong> .</span><span class="sxs-lookup"><span data-stu-id="ce0e6-118">A run-time error is generated if it is used with <strong>adModeShareDenyNone</strong> only.</span></span> <span data-ttu-id="ce0e6-119">Однако его можно использовать с <strong>адмодешаредениноне</strong> в сочетании с другими значениями.</span><span class="sxs-lookup"><span data-stu-id="ce0e6-119">However, it can be used with <strong>adModeShareDenyNone</strong> when combined with other values.</span></span> <span data-ttu-id="ce0e6-120">Например, можно использовать &quot; <strong>адмодереад</strong> или <strong>адмодешаредениноне</strong> или <strong>адмодерекурсиве</strong>&quot;.</span><span class="sxs-lookup"><span data-stu-id="ce0e6-120">For example, you can use &quot;<strong>adModeRead</strong> or <strong>adModeShareDenyNone</strong> or <strong>adModeRecursive</strong>&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce0e6-121"><strong>Адмодешаредениноне</strong></span><span class="sxs-lookup"><span data-stu-id="ce0e6-121"><strong>adModeShareDenyNone</strong></span></span></p></td>
<td><p><span data-ttu-id="ce0e6-122">столбцов</span><span class="sxs-lookup"><span data-stu-id="ce0e6-122">16</span></span></p></td>
<td><p><span data-ttu-id="ce0e6-123">Позволяет другим пользователям открывать подключение с любыми разрешениями.</span><span class="sxs-lookup"><span data-stu-id="ce0e6-123">Allows others to open a connection with any permissions.</span></span> <span data-ttu-id="ce0e6-124">Ни доступ для чтения, ни доступ для записи не могут быть запрещены для других пользователей.</span><span class="sxs-lookup"><span data-stu-id="ce0e6-124">Neither read nor write access can be denied to others.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce0e6-125"><strong>Адмодешаредениреад</strong></span><span class="sxs-lookup"><span data-stu-id="ce0e6-125"><strong>adModeShareDenyRead</strong></span></span></p></td>
<td><p><span data-ttu-id="ce0e6-126">SP4</span><span class="sxs-lookup"><span data-stu-id="ce0e6-126">4</span></span></p></td>
<td><p><span data-ttu-id="ce0e6-127">Запрещает другим пользователям открывать подключение с разрешениями на чтение.</span><span class="sxs-lookup"><span data-stu-id="ce0e6-127">Prevents others from opening a connection with read permissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce0e6-128"><strong>Адмодешаредениврите</strong></span><span class="sxs-lookup"><span data-stu-id="ce0e6-128"><strong>adModeShareDenyWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="ce0e6-129">8,5</span><span class="sxs-lookup"><span data-stu-id="ce0e6-129">8</span></span></p></td>
<td><p><span data-ttu-id="ce0e6-130">Запрещает другим пользователям открывать подключение с разрешениями на запись.</span><span class="sxs-lookup"><span data-stu-id="ce0e6-130">Prevents others from opening a connection with write permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce0e6-131"><strong>Адмодешариксклусиве</strong></span><span class="sxs-lookup"><span data-stu-id="ce0e6-131"><strong>adModeShareExclusive</strong></span></span></p></td>
<td><p><span data-ttu-id="ce0e6-132">12</span><span class="sxs-lookup"><span data-stu-id="ce0e6-132">12</span></span></p></td>
<td><p><span data-ttu-id="ce0e6-133">Запрещает другим пользователям открывать подключение.</span><span class="sxs-lookup"><span data-stu-id="ce0e6-133">Prevents others from opening a connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce0e6-134"><strong>Адмодеункновн</strong></span><span class="sxs-lookup"><span data-stu-id="ce0e6-134"><strong>adModeUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="ce0e6-135">нуль</span><span class="sxs-lookup"><span data-stu-id="ce0e6-135">0</span></span></p></td>
<td><p><span data-ttu-id="ce0e6-136">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ce0e6-136">Default.</span></span> <span data-ttu-id="ce0e6-137">Указывает, что разрешения еще не установлены или не могут быть определены.</span><span class="sxs-lookup"><span data-stu-id="ce0e6-137">Indicates that the permissions have not yet been set or cannot be determined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce0e6-138"><strong>Адмодеврите</strong></span><span class="sxs-lookup"><span data-stu-id="ce0e6-138"><strong>adModeWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="ce0e6-139">2</span><span class="sxs-lookup"><span data-stu-id="ce0e6-139">2</span></span></p></td>
<td><p><span data-ttu-id="ce0e6-140">Указывает разрешения только на запись.</span><span class="sxs-lookup"><span data-stu-id="ce0e6-140">Indicates write-only permissions.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="ce0e6-141">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="ce0e6-141">ADO/WFC equivalent</span></span>

<span data-ttu-id="ce0e6-142">Пакет: **com. MS. WFC. Data**</span><span class="sxs-lookup"><span data-stu-id="ce0e6-142">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ce0e6-143">Константа</span><span class="sxs-lookup"><span data-stu-id="ce0e6-143">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ce0e6-144">Адоенумс. Коннектмоде. READ</span><span class="sxs-lookup"><span data-stu-id="ce0e6-144">AdoEnums.ConnectMode.READ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce0e6-145">Адоенумс. Коннектмоде. READWRITE</span><span class="sxs-lookup"><span data-stu-id="ce0e6-145">AdoEnums.ConnectMode.READWRITE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce0e6-146">(Нет эквивалента Адоенумс. Коннектмоде. recursive)</span><span class="sxs-lookup"><span data-stu-id="ce0e6-146">(There is no equivalent of AdoEnums.ConnectMode.RECURSIVE)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce0e6-147">Адоенумс. Коннектмоде. ШАРЕДЕНИНОНЕ</span><span class="sxs-lookup"><span data-stu-id="ce0e6-147">AdoEnums.ConnectMode.SHAREDENYNONE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce0e6-148">Адоенумс. Коннектмоде. ШАРЕДЕНИРЕАД</span><span class="sxs-lookup"><span data-stu-id="ce0e6-148">AdoEnums.ConnectMode.SHAREDENYREAD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce0e6-149">Адоенумс. Коннектмоде. ШАРЕДЕНИВРИТЕ</span><span class="sxs-lookup"><span data-stu-id="ce0e6-149">AdoEnums.ConnectMode.SHAREDENYWRITE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce0e6-150">Адоенумс. Коннектмоде. ШАРИКСКЛУСИВЕ</span><span class="sxs-lookup"><span data-stu-id="ce0e6-150">AdoEnums.ConnectMode.SHAREEXCLUSIVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce0e6-151">Адоенумс. Коннектмоде. UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="ce0e6-151">AdoEnums.ConnectMode.UNKNOWN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce0e6-152">Адоенумс. Коннектмоде. WRITE</span><span class="sxs-lookup"><span data-stu-id="ce0e6-152">AdoEnums.ConnectMode.WRITE</span></span></p></td>
</tr>
</tbody>
</table>

