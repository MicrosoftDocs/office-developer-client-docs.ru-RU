---
title: Перечисление Пермиссионенум (DAO)
TOCTitle: PermissionEnum Enumeration
ms:assetid: dcce9940-f8a7-e915-1b69-05c341bea8cd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835373(v=office.15)
ms:contentKeyID: 48548147
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8d4f6741bd6203dbdeffb364650b5e3550ea8b1c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287712"
---
# <a name="permissionenum-enumeration-dao"></a><span data-ttu-id="e4ee8-102">Перечисление Пермиссионенум (DAO)</span><span class="sxs-lookup"><span data-stu-id="e4ee8-102">PermissionEnum enumeration (DAO)</span></span>


<span data-ttu-id="e4ee8-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e4ee8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e4ee8-104">Используется с свойством **Permissions** для указания типа разрешений.</span><span class="sxs-lookup"><span data-stu-id="e4ee8-104">Used with the **Permissions** property to specify the type of permissions.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e4ee8-105">Имя</span><span class="sxs-lookup"><span data-stu-id="e4ee8-105">Name</span></span></p></th>
<th><p><span data-ttu-id="e4ee8-106">Значение</span><span class="sxs-lookup"><span data-stu-id="e4ee8-106">Value</span></span></p></th>
<th><p><span data-ttu-id="e4ee8-107">Описание</span><span class="sxs-lookup"><span data-stu-id="e4ee8-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e4ee8-108">дбсеккреате</span><span class="sxs-lookup"><span data-stu-id="e4ee8-108">dbSecCreate</span></span></p></td>
<td><p><span data-ttu-id="e4ee8-109">1,1</span><span class="sxs-lookup"><span data-stu-id="e4ee8-109">1</span></span></p></td>
<td><p><span data-ttu-id="e4ee8-110">Пользователь может создавать новые документы (недопустимые для объектов документов).</span><span class="sxs-lookup"><span data-stu-id="e4ee8-110">The user can create new documents (not valid for Document objects).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4ee8-111">дбсекдбадмин</span><span class="sxs-lookup"><span data-stu-id="e4ee8-111">dbSecDBAdmin</span></span></p></td>
<td><p><span data-ttu-id="e4ee8-112">8 </span><span class="sxs-lookup"><span data-stu-id="e4ee8-112">8</span></span></p></td>
<td><p><span data-ttu-id="e4ee8-113">Пользователь может реплицировать базу данных и изменить ее пароль (недопустимый для объектов документов).</span><span class="sxs-lookup"><span data-stu-id="e4ee8-113">The user can replicate a database and change the database password (not valid for Document objects).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4ee8-114">дбсекдбкреате</span><span class="sxs-lookup"><span data-stu-id="e4ee8-114">dbSecDBCreate</span></span></p></td>
<td><p><span data-ttu-id="e4ee8-115">1,1</span><span class="sxs-lookup"><span data-stu-id="e4ee8-115">1</span></span></p></td>
<td><p><span data-ttu-id="e4ee8-116">Пользователь может создавать новые базы данных.</span><span class="sxs-lookup"><span data-stu-id="e4ee8-116">The user can create new databases.</span></span> <span data-ttu-id="e4ee8-117">Этот параметр является допустимым только для контейнера базы данных в файле сведений о рабочей группе (предыдущие. mdw).</span><span class="sxs-lookup"><span data-stu-id="e4ee8-117">This option is valid only on the Databases container in the workgroup information file (Systen.mdw).</span></span> <span data-ttu-id="e4ee8-118">Эта константа не является допустимой для объектов Document.</span><span class="sxs-lookup"><span data-stu-id="e4ee8-118">This constant is not valid for Document objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4ee8-119">дбсекдбексклусиве</span><span class="sxs-lookup"><span data-stu-id="e4ee8-119">dbSecDBExclusive</span></span></p></td>
<td><p><span data-ttu-id="e4ee8-120">4 </span><span class="sxs-lookup"><span data-stu-id="e4ee8-120">4</span></span></p></td>
<td><p><span data-ttu-id="e4ee8-121">Пользователь имеет исключительный доступ к базе данных.</span><span class="sxs-lookup"><span data-stu-id="e4ee8-121">The user has exclusive access to the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4ee8-122">дбсекдбопен</span><span class="sxs-lookup"><span data-stu-id="e4ee8-122">dbSecDBOpen</span></span></p></td>
<td><p><span data-ttu-id="e4ee8-123">2</span><span class="sxs-lookup"><span data-stu-id="e4ee8-123">2</span></span></p></td>
<td><p><span data-ttu-id="e4ee8-124">Пользователь может открыть базу данных.</span><span class="sxs-lookup"><span data-stu-id="e4ee8-124">The user can open the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4ee8-125">дбсекделете</span><span class="sxs-lookup"><span data-stu-id="e4ee8-125">dbSecDelete</span></span></p></td>
<td><p><span data-ttu-id="e4ee8-126">65536</span><span class="sxs-lookup"><span data-stu-id="e4ee8-126">65536</span></span></p></td>
<td><p><span data-ttu-id="e4ee8-127">Пользователь может удалить объект.</span><span class="sxs-lookup"><span data-stu-id="e4ee8-127">The user can delete the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4ee8-128">дбсекделетедата</span><span class="sxs-lookup"><span data-stu-id="e4ee8-128">dbSecDeleteData</span></span></p></td>
<td><p><span data-ttu-id="e4ee8-129">128</span><span class="sxs-lookup"><span data-stu-id="e4ee8-129">128</span></span></p></td>
<td><p><span data-ttu-id="e4ee8-130">Пользователь может удалять записи.</span><span class="sxs-lookup"><span data-stu-id="e4ee8-130">The user can delete records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4ee8-131">дбсекфуллакцесс</span><span class="sxs-lookup"><span data-stu-id="e4ee8-131">dbSecFullAccess</span></span></p></td>
<td><p><span data-ttu-id="e4ee8-132">1048575</span><span class="sxs-lookup"><span data-stu-id="e4ee8-132">1048575</span></span></p></td>
<td><p><span data-ttu-id="e4ee8-133">Пользователь имеет полный доступ к объекту.</span><span class="sxs-lookup"><span data-stu-id="e4ee8-133">The user has full access to the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4ee8-134">дбсеЦинсертдата</span><span class="sxs-lookup"><span data-stu-id="e4ee8-134">dbSecInsertData</span></span></p></td>
<td><p><span data-ttu-id="e4ee8-135">32</span><span class="sxs-lookup"><span data-stu-id="e4ee8-135">32</span></span></p></td>
<td><p><span data-ttu-id="e4ee8-136">Пользователь может добавлять записи.</span><span class="sxs-lookup"><span data-stu-id="e4ee8-136">The user can add records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4ee8-137">дбсекноакцесс</span><span class="sxs-lookup"><span data-stu-id="e4ee8-137">dbSecNoAccess</span></span></p></td>
<td><p><span data-ttu-id="e4ee8-138">нуль</span><span class="sxs-lookup"><span data-stu-id="e4ee8-138">0</span></span></p></td>
<td><p><span data-ttu-id="e4ee8-139">У пользователя нет доступа к объекту (он не является допустимым для объектов документа).</span><span class="sxs-lookup"><span data-stu-id="e4ee8-139">The user does not have access to the object (not valid for Document objects).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4ee8-140">дбсекреаддеф</span><span class="sxs-lookup"><span data-stu-id="e4ee8-140">dbSecReadDef</span></span></p></td>
<td><p><span data-ttu-id="e4ee8-141">4 </span><span class="sxs-lookup"><span data-stu-id="e4ee8-141">4</span></span></p></td>
<td><p><span data-ttu-id="e4ee8-142">Пользователь может прочитать определение таблицы, включая сведения о столбцах и индексах.</span><span class="sxs-lookup"><span data-stu-id="e4ee8-142">The user can read the table definition, including column and index information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4ee8-143">дбсекреадсек</span><span class="sxs-lookup"><span data-stu-id="e4ee8-143">dbSecReadSec</span></span></p></td>
<td><p><span data-ttu-id="e4ee8-144">131072</span><span class="sxs-lookup"><span data-stu-id="e4ee8-144">131072</span></span></p></td>
<td><p><span data-ttu-id="e4ee8-145">Пользователь может читать информацию, связанную с безопасностью объекта.</span><span class="sxs-lookup"><span data-stu-id="e4ee8-145">The user can read the object's security-related information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4ee8-146">дбсекреплацедата</span><span class="sxs-lookup"><span data-stu-id="e4ee8-146">dbSecReplaceData</span></span></p></td>
<td><p><span data-ttu-id="e4ee8-147">64</span><span class="sxs-lookup"><span data-stu-id="e4ee8-147">64</span></span></p></td>
<td><p><span data-ttu-id="e4ee8-148">Пользователь может изменять записи.</span><span class="sxs-lookup"><span data-stu-id="e4ee8-148">The user can modify records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4ee8-149">дбсекретриеведата</span><span class="sxs-lookup"><span data-stu-id="e4ee8-149">dbSecRetrieveData</span></span></p></td>
<td><p><span data-ttu-id="e4ee8-150">двадцать</span><span class="sxs-lookup"><span data-stu-id="e4ee8-150">20</span></span></p></td>
<td><p><span data-ttu-id="e4ee8-151">Пользователь может получить данные из объекта Document.</span><span class="sxs-lookup"><span data-stu-id="e4ee8-151">The user can retrieve data from the Document object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4ee8-152">дбсеквритедеф</span><span class="sxs-lookup"><span data-stu-id="e4ee8-152">dbSecWriteDef</span></span></p></td>
<td><p><span data-ttu-id="e4ee8-153">65548</span><span class="sxs-lookup"><span data-stu-id="e4ee8-153">65548</span></span></p></td>
<td><p><span data-ttu-id="e4ee8-154">Пользователь может изменять или удалять определение таблицы, в том числе сведения о столбцах и индексах.</span><span class="sxs-lookup"><span data-stu-id="e4ee8-154">The user can modify or delete the table definition, including column and index information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4ee8-155">дбсеквритеовнер</span><span class="sxs-lookup"><span data-stu-id="e4ee8-155">dbSecWriteOwner</span></span></p></td>
<td><p><span data-ttu-id="e4ee8-156">524288</span><span class="sxs-lookup"><span data-stu-id="e4ee8-156">524288</span></span></p></td>
<td><p><span data-ttu-id="e4ee8-157">Пользователь может изменить значение свойства Owner.</span><span class="sxs-lookup"><span data-stu-id="e4ee8-157">The user can change the Owner property setting.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4ee8-158">дбсеквритесек</span><span class="sxs-lookup"><span data-stu-id="e4ee8-158">dbSecWriteSec</span></span></p></td>
<td><p><span data-ttu-id="e4ee8-159">262144</span><span class="sxs-lookup"><span data-stu-id="e4ee8-159">262144</span></span></p></td>
<td><p><span data-ttu-id="e4ee8-160">Пользователь может изменять разрешения доступа.</span><span class="sxs-lookup"><span data-stu-id="e4ee8-160">The user can alter access permissions.</span></span></p></td>
</tr>
</tbody>
</table>

