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
# <a name="permissionenum-enumeration-dao"></a><span data-ttu-id="246a2-102">Перечисление Пермиссионенум (DAO)</span><span class="sxs-lookup"><span data-stu-id="246a2-102">PermissionEnum enumeration (DAO)</span></span>


<span data-ttu-id="246a2-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="246a2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="246a2-104">Используется с свойством **Permissions** для указания типа разрешений.</span><span class="sxs-lookup"><span data-stu-id="246a2-104">Used with the **Permissions** property to specify the type of permissions.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="246a2-105">Имя</span><span class="sxs-lookup"><span data-stu-id="246a2-105">Name</span></span></p></th>
<th><p><span data-ttu-id="246a2-106">Значение</span><span class="sxs-lookup"><span data-stu-id="246a2-106">Value</span></span></p></th>
<th><p><span data-ttu-id="246a2-107">Описание</span><span class="sxs-lookup"><span data-stu-id="246a2-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="246a2-108">Дбсеккреате</span><span class="sxs-lookup"><span data-stu-id="246a2-108">dbSecCreate</span></span></p></td>
<td><p><span data-ttu-id="246a2-109">1,1</span><span class="sxs-lookup"><span data-stu-id="246a2-109">1</span></span></p></td>
<td><p><span data-ttu-id="246a2-110">Пользователь может создавать новые документы (недопустимые для объектов документов).</span><span class="sxs-lookup"><span data-stu-id="246a2-110">The user can create new documents (not valid for Document objects).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="246a2-111">Дбсекдбадмин</span><span class="sxs-lookup"><span data-stu-id="246a2-111">dbSecDBAdmin</span></span></p></td>
<td><p><span data-ttu-id="246a2-112">8,5</span><span class="sxs-lookup"><span data-stu-id="246a2-112">8</span></span></p></td>
<td><p><span data-ttu-id="246a2-113">Пользователь может реплицировать базу данных и изменить ее пароль (недопустимый для объектов документов).</span><span class="sxs-lookup"><span data-stu-id="246a2-113">The user can replicate a database and change the database password (not valid for Document objects).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="246a2-114">Дбсекдбкреате</span><span class="sxs-lookup"><span data-stu-id="246a2-114">dbSecDBCreate</span></span></p></td>
<td><p><span data-ttu-id="246a2-115">1,1</span><span class="sxs-lookup"><span data-stu-id="246a2-115">1</span></span></p></td>
<td><p><span data-ttu-id="246a2-116">Пользователь может создавать новые базы данных.</span><span class="sxs-lookup"><span data-stu-id="246a2-116">The user can create new databases.</span></span> <span data-ttu-id="246a2-117">Этот параметр является допустимым только для контейнера базы данных в файле сведений о рабочей группе (предыдущие. mdw).</span><span class="sxs-lookup"><span data-stu-id="246a2-117">This option is valid only on the Databases container in the workgroup information file (Systen.mdw).</span></span> <span data-ttu-id="246a2-118">Эта константа не является допустимой для объектов Document.</span><span class="sxs-lookup"><span data-stu-id="246a2-118">This constant is not valid for Document objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="246a2-119">Дбсекдбексклусиве</span><span class="sxs-lookup"><span data-stu-id="246a2-119">dbSecDBExclusive</span></span></p></td>
<td><p><span data-ttu-id="246a2-120">SP4</span><span class="sxs-lookup"><span data-stu-id="246a2-120">4</span></span></p></td>
<td><p><span data-ttu-id="246a2-121">Пользователь имеет исключительный доступ к базе данных.</span><span class="sxs-lookup"><span data-stu-id="246a2-121">The user has exclusive access to the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="246a2-122">Дбсекдбопен</span><span class="sxs-lookup"><span data-stu-id="246a2-122">dbSecDBOpen</span></span></p></td>
<td><p><span data-ttu-id="246a2-123">2</span><span class="sxs-lookup"><span data-stu-id="246a2-123">2</span></span></p></td>
<td><p><span data-ttu-id="246a2-124">Пользователь может открыть базу данных.</span><span class="sxs-lookup"><span data-stu-id="246a2-124">The user can open the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="246a2-125">Дбсекделете</span><span class="sxs-lookup"><span data-stu-id="246a2-125">dbSecDelete</span></span></p></td>
<td><p><span data-ttu-id="246a2-126">65536</span><span class="sxs-lookup"><span data-stu-id="246a2-126">65536</span></span></p></td>
<td><p><span data-ttu-id="246a2-127">Пользователь может удалить объект.</span><span class="sxs-lookup"><span data-stu-id="246a2-127">The user can delete the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="246a2-128">Дбсекделетедата</span><span class="sxs-lookup"><span data-stu-id="246a2-128">dbSecDeleteData</span></span></p></td>
<td><p><span data-ttu-id="246a2-129">128</span><span class="sxs-lookup"><span data-stu-id="246a2-129">128</span></span></p></td>
<td><p><span data-ttu-id="246a2-130">Пользователь может удалять записи.</span><span class="sxs-lookup"><span data-stu-id="246a2-130">The user can delete records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="246a2-131">Дбсекфуллакцесс</span><span class="sxs-lookup"><span data-stu-id="246a2-131">dbSecFullAccess</span></span></p></td>
<td><p><span data-ttu-id="246a2-132">1048575</span><span class="sxs-lookup"><span data-stu-id="246a2-132">1048575</span></span></p></td>
<td><p><span data-ttu-id="246a2-133">Пользователь имеет полный доступ к объекту.</span><span class="sxs-lookup"><span data-stu-id="246a2-133">The user has full access to the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="246a2-134">ДбсеЦинсертдата</span><span class="sxs-lookup"><span data-stu-id="246a2-134">dbSecInsertData</span></span></p></td>
<td><p><span data-ttu-id="246a2-135">32</span><span class="sxs-lookup"><span data-stu-id="246a2-135">32</span></span></p></td>
<td><p><span data-ttu-id="246a2-136">Пользователь может добавлять записи.</span><span class="sxs-lookup"><span data-stu-id="246a2-136">The user can add records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="246a2-137">Дбсекноакцесс</span><span class="sxs-lookup"><span data-stu-id="246a2-137">dbSecNoAccess</span></span></p></td>
<td><p><span data-ttu-id="246a2-138">нуль</span><span class="sxs-lookup"><span data-stu-id="246a2-138">0</span></span></p></td>
<td><p><span data-ttu-id="246a2-139">У пользователя нет доступа к объекту (он не является допустимым для объектов документа).</span><span class="sxs-lookup"><span data-stu-id="246a2-139">The user does not have access to the object (not valid for Document objects).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="246a2-140">Дбсекреаддеф</span><span class="sxs-lookup"><span data-stu-id="246a2-140">dbSecReadDef</span></span></p></td>
<td><p><span data-ttu-id="246a2-141">SP4</span><span class="sxs-lookup"><span data-stu-id="246a2-141">4</span></span></p></td>
<td><p><span data-ttu-id="246a2-142">Пользователь может прочитать определение таблицы, включая сведения о столбцах и индексах.</span><span class="sxs-lookup"><span data-stu-id="246a2-142">The user can read the table definition, including column and index information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="246a2-143">Дбсекреадсек</span><span class="sxs-lookup"><span data-stu-id="246a2-143">dbSecReadSec</span></span></p></td>
<td><p><span data-ttu-id="246a2-144">131072</span><span class="sxs-lookup"><span data-stu-id="246a2-144">131072</span></span></p></td>
<td><p><span data-ttu-id="246a2-145">Пользователь может читать информацию, связанную с безопасностью объекта.</span><span class="sxs-lookup"><span data-stu-id="246a2-145">The user can read the object's security-related information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="246a2-146">Дбсекреплацедата</span><span class="sxs-lookup"><span data-stu-id="246a2-146">dbSecReplaceData</span></span></p></td>
<td><p><span data-ttu-id="246a2-147">64</span><span class="sxs-lookup"><span data-stu-id="246a2-147">64</span></span></p></td>
<td><p><span data-ttu-id="246a2-148">Пользователь может изменять записи.</span><span class="sxs-lookup"><span data-stu-id="246a2-148">The user can modify records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="246a2-149">Дбсекретриеведата</span><span class="sxs-lookup"><span data-stu-id="246a2-149">dbSecRetrieveData</span></span></p></td>
<td><p><span data-ttu-id="246a2-150">двадцать</span><span class="sxs-lookup"><span data-stu-id="246a2-150">20</span></span></p></td>
<td><p><span data-ttu-id="246a2-151">Пользователь может получить данные из объекта Document.</span><span class="sxs-lookup"><span data-stu-id="246a2-151">The user can retrieve data from the Document object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="246a2-152">Дбсеквритедеф</span><span class="sxs-lookup"><span data-stu-id="246a2-152">dbSecWriteDef</span></span></p></td>
<td><p><span data-ttu-id="246a2-153">65548</span><span class="sxs-lookup"><span data-stu-id="246a2-153">65548</span></span></p></td>
<td><p><span data-ttu-id="246a2-154">Пользователь может изменять или удалять определение таблицы, в том числе сведения о столбцах и индексах.</span><span class="sxs-lookup"><span data-stu-id="246a2-154">The user can modify or delete the table definition, including column and index information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="246a2-155">Дбсеквритеовнер</span><span class="sxs-lookup"><span data-stu-id="246a2-155">dbSecWriteOwner</span></span></p></td>
<td><p><span data-ttu-id="246a2-156">524288</span><span class="sxs-lookup"><span data-stu-id="246a2-156">524288</span></span></p></td>
<td><p><span data-ttu-id="246a2-157">Пользователь может изменить значение свойства Owner.</span><span class="sxs-lookup"><span data-stu-id="246a2-157">The user can change the Owner property setting.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="246a2-158">Дбсеквритесек</span><span class="sxs-lookup"><span data-stu-id="246a2-158">dbSecWriteSec</span></span></p></td>
<td><p><span data-ttu-id="246a2-159">262144</span><span class="sxs-lookup"><span data-stu-id="246a2-159">262144</span></span></p></td>
<td><p><span data-ttu-id="246a2-160">Пользователь может изменять разрешения доступа.</span><span class="sxs-lookup"><span data-stu-id="246a2-160">The user can alter access permissions.</span></span></p></td>
</tr>
</tbody>
</table>

