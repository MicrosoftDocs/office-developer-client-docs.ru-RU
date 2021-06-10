---
title: Переумежение PermissionEnum (DAO)
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
# <a name="permissionenum-enumeration-dao"></a><span data-ttu-id="7ac7d-102">Переумежение PermissionEnum (DAO)</span><span class="sxs-lookup"><span data-stu-id="7ac7d-102">PermissionEnum enumeration (DAO)</span></span>


<span data-ttu-id="7ac7d-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7ac7d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7ac7d-104">Используется с **свойством Permissions** для указания типа разрешений.</span><span class="sxs-lookup"><span data-stu-id="7ac7d-104">Used with the **Permissions** property to specify the type of permissions.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7ac7d-105">Имя</span><span class="sxs-lookup"><span data-stu-id="7ac7d-105">Name</span></span></p></th>
<th><p><span data-ttu-id="7ac7d-106">Значение</span><span class="sxs-lookup"><span data-stu-id="7ac7d-106">Value</span></span></p></th>
<th><p><span data-ttu-id="7ac7d-107">Описание</span><span class="sxs-lookup"><span data-stu-id="7ac7d-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7ac7d-108">dbSecCreate</span><span class="sxs-lookup"><span data-stu-id="7ac7d-108">dbSecCreate</span></span></p></td>
<td><p><span data-ttu-id="7ac7d-109">1</span><span class="sxs-lookup"><span data-stu-id="7ac7d-109">1</span></span></p></td>
<td><p><span data-ttu-id="7ac7d-110">Пользователь может создавать новые документы (не допустимые для объектов Document).</span><span class="sxs-lookup"><span data-stu-id="7ac7d-110">The user can create new documents (not valid for Document objects).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ac7d-111">dbSecDBAdmin</span><span class="sxs-lookup"><span data-stu-id="7ac7d-111">dbSecDBAdmin</span></span></p></td>
<td><p><span data-ttu-id="7ac7d-112">8 </span><span class="sxs-lookup"><span data-stu-id="7ac7d-112">8</span></span></p></td>
<td><p><span data-ttu-id="7ac7d-113">Пользователь может реплицировать базу данных и изменить пароль базы данных (не допустимый для объектов Document).</span><span class="sxs-lookup"><span data-stu-id="7ac7d-113">The user can replicate a database and change the database password (not valid for Document objects).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ac7d-114">dbSecDBCreate</span><span class="sxs-lookup"><span data-stu-id="7ac7d-114">dbSecDBCreate</span></span></p></td>
<td><p><span data-ttu-id="7ac7d-115">1</span><span class="sxs-lookup"><span data-stu-id="7ac7d-115">1</span></span></p></td>
<td><p><span data-ttu-id="7ac7d-116">Пользователь может создавать новые базы данных.</span><span class="sxs-lookup"><span data-stu-id="7ac7d-116">The user can create new databases.</span></span> <span data-ttu-id="7ac7d-117">Этот параметр действителен только в контейнере Databases в информационном файле группы (Systen.mdw).</span><span class="sxs-lookup"><span data-stu-id="7ac7d-117">This option is valid only on the Databases container in the workgroup information file (Systen.mdw).</span></span> <span data-ttu-id="7ac7d-118">Эта константа не допустима для объектов Document.</span><span class="sxs-lookup"><span data-stu-id="7ac7d-118">This constant is not valid for Document objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ac7d-119">dbSecDBExclusive</span><span class="sxs-lookup"><span data-stu-id="7ac7d-119">dbSecDBExclusive</span></span></p></td>
<td><p><span data-ttu-id="7ac7d-120">4 </span><span class="sxs-lookup"><span data-stu-id="7ac7d-120">4</span></span></p></td>
<td><p><span data-ttu-id="7ac7d-121">Пользователь имеет эксклюзивный доступ к базе данных.</span><span class="sxs-lookup"><span data-stu-id="7ac7d-121">The user has exclusive access to the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ac7d-122">dbSecDBOpen</span><span class="sxs-lookup"><span data-stu-id="7ac7d-122">dbSecDBOpen</span></span></p></td>
<td><p><span data-ttu-id="7ac7d-123">2</span><span class="sxs-lookup"><span data-stu-id="7ac7d-123">2</span></span></p></td>
<td><p><span data-ttu-id="7ac7d-124">Пользователь может открыть базу данных.</span><span class="sxs-lookup"><span data-stu-id="7ac7d-124">The user can open the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ac7d-125">dbSecDelete</span><span class="sxs-lookup"><span data-stu-id="7ac7d-125">dbSecDelete</span></span></p></td>
<td><p><span data-ttu-id="7ac7d-126">65536</span><span class="sxs-lookup"><span data-stu-id="7ac7d-126">65536</span></span></p></td>
<td><p><span data-ttu-id="7ac7d-127">Пользователь может удалить объект.</span><span class="sxs-lookup"><span data-stu-id="7ac7d-127">The user can delete the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ac7d-128">dbSecDeleteData</span><span class="sxs-lookup"><span data-stu-id="7ac7d-128">dbSecDeleteData</span></span></p></td>
<td><p><span data-ttu-id="7ac7d-129">128</span><span class="sxs-lookup"><span data-stu-id="7ac7d-129">128</span></span></p></td>
<td><p><span data-ttu-id="7ac7d-130">Пользователь может удалять записи.</span><span class="sxs-lookup"><span data-stu-id="7ac7d-130">The user can delete records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ac7d-131">dbSecFullAccess</span><span class="sxs-lookup"><span data-stu-id="7ac7d-131">dbSecFullAccess</span></span></p></td>
<td><p><span data-ttu-id="7ac7d-132">1048575</span><span class="sxs-lookup"><span data-stu-id="7ac7d-132">1048575</span></span></p></td>
<td><p><span data-ttu-id="7ac7d-133">Пользователь имеет полный доступ к объекту.</span><span class="sxs-lookup"><span data-stu-id="7ac7d-133">The user has full access to the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ac7d-134">dbSecInsertData</span><span class="sxs-lookup"><span data-stu-id="7ac7d-134">dbSecInsertData</span></span></p></td>
<td><p><span data-ttu-id="7ac7d-135">32</span><span class="sxs-lookup"><span data-stu-id="7ac7d-135">32</span></span></p></td>
<td><p><span data-ttu-id="7ac7d-136">Пользователь может добавлять записи.</span><span class="sxs-lookup"><span data-stu-id="7ac7d-136">The user can add records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ac7d-137">dbSecNoAccess</span><span class="sxs-lookup"><span data-stu-id="7ac7d-137">dbSecNoAccess</span></span></p></td>
<td><p><span data-ttu-id="7ac7d-138">0</span><span class="sxs-lookup"><span data-stu-id="7ac7d-138">0</span></span></p></td>
<td><p><span data-ttu-id="7ac7d-139">Пользователь не имеет доступа к объекту (не допустимым для объектов Document).</span><span class="sxs-lookup"><span data-stu-id="7ac7d-139">The user does not have access to the object (not valid for Document objects).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ac7d-140">dbSecReadDef</span><span class="sxs-lookup"><span data-stu-id="7ac7d-140">dbSecReadDef</span></span></p></td>
<td><p><span data-ttu-id="7ac7d-141">4 </span><span class="sxs-lookup"><span data-stu-id="7ac7d-141">4</span></span></p></td>
<td><p><span data-ttu-id="7ac7d-142">Пользователь может прочитать определение таблицы, включая сведения о столбцах и индексах.</span><span class="sxs-lookup"><span data-stu-id="7ac7d-142">The user can read the table definition, including column and index information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ac7d-143">dbSecReadSec</span><span class="sxs-lookup"><span data-stu-id="7ac7d-143">dbSecReadSec</span></span></p></td>
<td><p><span data-ttu-id="7ac7d-144">131072</span><span class="sxs-lookup"><span data-stu-id="7ac7d-144">131072</span></span></p></td>
<td><p><span data-ttu-id="7ac7d-145">Пользователь может читать сведения, связанные с безопасностью объекта.</span><span class="sxs-lookup"><span data-stu-id="7ac7d-145">The user can read the object's security-related information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ac7d-146">dbSecReplaceData</span><span class="sxs-lookup"><span data-stu-id="7ac7d-146">dbSecReplaceData</span></span></p></td>
<td><p><span data-ttu-id="7ac7d-147">64</span><span class="sxs-lookup"><span data-stu-id="7ac7d-147">64</span></span></p></td>
<td><p><span data-ttu-id="7ac7d-148">Пользователь может изменять записи.</span><span class="sxs-lookup"><span data-stu-id="7ac7d-148">The user can modify records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ac7d-149">dbSecRetrieveData</span><span class="sxs-lookup"><span data-stu-id="7ac7d-149">dbSecRetrieveData</span></span></p></td>
<td><p><span data-ttu-id="7ac7d-150">20</span><span class="sxs-lookup"><span data-stu-id="7ac7d-150">20</span></span></p></td>
<td><p><span data-ttu-id="7ac7d-151">Пользователь может получать данные из объекта Document.</span><span class="sxs-lookup"><span data-stu-id="7ac7d-151">The user can retrieve data from the Document object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ac7d-152">dbSecWriteDef</span><span class="sxs-lookup"><span data-stu-id="7ac7d-152">dbSecWriteDef</span></span></p></td>
<td><p><span data-ttu-id="7ac7d-153">65548</span><span class="sxs-lookup"><span data-stu-id="7ac7d-153">65548</span></span></p></td>
<td><p><span data-ttu-id="7ac7d-154">Пользователь может изменять или удалять определение таблицы, включая сведения о столбцах и индексах.</span><span class="sxs-lookup"><span data-stu-id="7ac7d-154">The user can modify or delete the table definition, including column and index information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ac7d-155">dbSecWriteOwner</span><span class="sxs-lookup"><span data-stu-id="7ac7d-155">dbSecWriteOwner</span></span></p></td>
<td><p><span data-ttu-id="7ac7d-156">524288</span><span class="sxs-lookup"><span data-stu-id="7ac7d-156">524288</span></span></p></td>
<td><p><span data-ttu-id="7ac7d-157">Пользователь может изменить параметр свойства Owner.</span><span class="sxs-lookup"><span data-stu-id="7ac7d-157">The user can change the Owner property setting.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ac7d-158">dbSecWriteSec</span><span class="sxs-lookup"><span data-stu-id="7ac7d-158">dbSecWriteSec</span></span></p></td>
<td><p><span data-ttu-id="7ac7d-159">262144</span><span class="sxs-lookup"><span data-stu-id="7ac7d-159">262144</span></span></p></td>
<td><p><span data-ttu-id="7ac7d-160">Пользователь может изменять разрешения доступа.</span><span class="sxs-lookup"><span data-stu-id="7ac7d-160">The user can alter access permissions.</span></span></p></td>
</tr>
</tbody>
</table>

