---
title: Перечисление PermissionEnum (DAO)
TOCTitle: PermissionEnum Enumeration
ms:assetid: dcce9940-f8a7-e915-1b69-05c341bea8cd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835373(v=office.15)
ms:contentKeyID: 48548147
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ed3abb0e3ff76ae19c6c19a3e2040b338e2b5ff3
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945868"
---
# <a name="permissionenum-enumeration-dao"></a><span data-ttu-id="cc21b-102">Перечисление PermissionEnum (DAO)</span><span class="sxs-lookup"><span data-stu-id="cc21b-102">PermissionEnum enumeration (DAO)</span></span>


<span data-ttu-id="cc21b-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cc21b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cc21b-104">Используется совместно со свойством **разрешения** , чтобы указать тип разрешения.</span><span class="sxs-lookup"><span data-stu-id="cc21b-104">Used with the **Permissions** property to specify the type of permissions.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cc21b-105">Имя</span><span class="sxs-lookup"><span data-stu-id="cc21b-105">Name</span></span></p></th>
<th><p><span data-ttu-id="cc21b-106">Значение</span><span class="sxs-lookup"><span data-stu-id="cc21b-106">Value</span></span></p></th>
<th><p><span data-ttu-id="cc21b-107">Описание</span><span class="sxs-lookup"><span data-stu-id="cc21b-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cc21b-108">dbSecCreate</span><span class="sxs-lookup"><span data-stu-id="cc21b-108">dbSecCreate</span></span></p></td>
<td><p><span data-ttu-id="cc21b-109">1</span><span class="sxs-lookup"><span data-stu-id="cc21b-109">1</span></span></p></td>
<td><p><span data-ttu-id="cc21b-110">Пользователь может создавать новые документы (недействительно для объектов-документов).</span><span class="sxs-lookup"><span data-stu-id="cc21b-110">The user can create new documents (not valid for Document objects).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc21b-111">dbSecDBAdmin</span><span class="sxs-lookup"><span data-stu-id="cc21b-111">dbSecDBAdmin</span></span></p></td>
<td><p><span data-ttu-id="cc21b-112">8</span><span class="sxs-lookup"><span data-stu-id="cc21b-112">8</span></span></p></td>
<td><p><span data-ttu-id="cc21b-113">Пользователь может репликации базы данных и изменение пароля базы данных (недействительно для объектов-документов).</span><span class="sxs-lookup"><span data-stu-id="cc21b-113">The user can replicate a database and change the database password (not valid for Document objects).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc21b-114">dbSecDBCreate</span><span class="sxs-lookup"><span data-stu-id="cc21b-114">dbSecDBCreate</span></span></p></td>
<td><p><span data-ttu-id="cc21b-115">1</span><span class="sxs-lookup"><span data-stu-id="cc21b-115">1</span></span></p></td>
<td><p><span data-ttu-id="cc21b-116">Пользователь может создавать новые базы данных.</span><span class="sxs-lookup"><span data-stu-id="cc21b-116">The user can create new databases.</span></span> <span data-ttu-id="cc21b-117">Этот параметр действителен только на контейнер баз данных в файле рабочей группы (Systen.mdw).</span><span class="sxs-lookup"><span data-stu-id="cc21b-117">This option is valid only on the Databases container in the workgroup information file (Systen.mdw).</span></span> <span data-ttu-id="cc21b-118">В этом константа недопустима для объектов документа.</span><span class="sxs-lookup"><span data-stu-id="cc21b-118">This constant is not valid for Document objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc21b-119">dbSecDBExclusive</span><span class="sxs-lookup"><span data-stu-id="cc21b-119">dbSecDBExclusive</span></span></p></td>
<td><p><span data-ttu-id="cc21b-120">4</span><span class="sxs-lookup"><span data-stu-id="cc21b-120">4</span></span></p></td>
<td><p><span data-ttu-id="cc21b-121">Пользователь имеет исключительных доступ к базе данных.</span><span class="sxs-lookup"><span data-stu-id="cc21b-121">The user has exclusive access to the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc21b-122">dbSecDBOpen</span><span class="sxs-lookup"><span data-stu-id="cc21b-122">dbSecDBOpen</span></span></p></td>
<td><p><span data-ttu-id="cc21b-123">2</span><span class="sxs-lookup"><span data-stu-id="cc21b-123">2</span></span></p></td>
<td><p><span data-ttu-id="cc21b-124">Пользователь может открыть базу данных.</span><span class="sxs-lookup"><span data-stu-id="cc21b-124">The user can open the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc21b-125">dbSecDelete</span><span class="sxs-lookup"><span data-stu-id="cc21b-125">dbSecDelete</span></span></p></td>
<td><p><span data-ttu-id="cc21b-126">65536</span><span class="sxs-lookup"><span data-stu-id="cc21b-126">65536</span></span></p></td>
<td><p><span data-ttu-id="cc21b-127">Пользователь может удалить объект.</span><span class="sxs-lookup"><span data-stu-id="cc21b-127">The user can delete the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc21b-128">dbSecDeleteData</span><span class="sxs-lookup"><span data-stu-id="cc21b-128">dbSecDeleteData</span></span></p></td>
<td><p><span data-ttu-id="cc21b-129">128</span><span class="sxs-lookup"><span data-stu-id="cc21b-129">128</span></span></p></td>
<td><p><span data-ttu-id="cc21b-130">Пользователь может удалить записи.</span><span class="sxs-lookup"><span data-stu-id="cc21b-130">The user can delete records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc21b-131">dbSecFullAccess</span><span class="sxs-lookup"><span data-stu-id="cc21b-131">dbSecFullAccess</span></span></p></td>
<td><p><span data-ttu-id="cc21b-132">1048575</span><span class="sxs-lookup"><span data-stu-id="cc21b-132">1048575</span></span></p></td>
<td><p><span data-ttu-id="cc21b-133">Пользователь имеет полный доступ к объекту.</span><span class="sxs-lookup"><span data-stu-id="cc21b-133">The user has full access to the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc21b-134">dbSecInsertData</span><span class="sxs-lookup"><span data-stu-id="cc21b-134">dbSecInsertData</span></span></p></td>
<td><p><span data-ttu-id="cc21b-135">32</span><span class="sxs-lookup"><span data-stu-id="cc21b-135">32</span></span></p></td>
<td><p><span data-ttu-id="cc21b-136">Пользователь может добавить записи.</span><span class="sxs-lookup"><span data-stu-id="cc21b-136">The user can add records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc21b-137">dbSecNoAccess</span><span class="sxs-lookup"><span data-stu-id="cc21b-137">dbSecNoAccess</span></span></p></td>
<td><p><span data-ttu-id="cc21b-138">0</span><span class="sxs-lookup"><span data-stu-id="cc21b-138">0</span></span></p></td>
<td><p><span data-ttu-id="cc21b-139">Пользователь не имеет доступ к объекту (недействительно для объектов-документов).</span><span class="sxs-lookup"><span data-stu-id="cc21b-139">The user does not have access to the object (not valid for Document objects).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc21b-140">dbSecReadDef</span><span class="sxs-lookup"><span data-stu-id="cc21b-140">dbSecReadDef</span></span></p></td>
<td><p><span data-ttu-id="cc21b-141">4</span><span class="sxs-lookup"><span data-stu-id="cc21b-141">4</span></span></p></td>
<td><p><span data-ttu-id="cc21b-142">Пользователь может читать определение таблицы, включая сведения о столбце и индекса.</span><span class="sxs-lookup"><span data-stu-id="cc21b-142">The user can read the table definition, including column and index information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc21b-143">dbSecReadSec</span><span class="sxs-lookup"><span data-stu-id="cc21b-143">dbSecReadSec</span></span></p></td>
<td><p><span data-ttu-id="cc21b-144">131072</span><span class="sxs-lookup"><span data-stu-id="cc21b-144">131072</span></span></p></td>
<td><p><span data-ttu-id="cc21b-145">Пользователи могут читать сведения из объекта безопасности.</span><span class="sxs-lookup"><span data-stu-id="cc21b-145">The user can read the object's security-related information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc21b-146">dbSecReplaceData</span><span class="sxs-lookup"><span data-stu-id="cc21b-146">dbSecReplaceData</span></span></p></td>
<td><p><span data-ttu-id="cc21b-147">64</span><span class="sxs-lookup"><span data-stu-id="cc21b-147">64</span></span></p></td>
<td><p><span data-ttu-id="cc21b-148">Пользователь может изменять записи.</span><span class="sxs-lookup"><span data-stu-id="cc21b-148">The user can modify records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc21b-149">dbSecRetrieveData</span><span class="sxs-lookup"><span data-stu-id="cc21b-149">dbSecRetrieveData</span></span></p></td>
<td><p><span data-ttu-id="cc21b-150">20</span><span class="sxs-lookup"><span data-stu-id="cc21b-150">20</span></span></p></td>
<td><p><span data-ttu-id="cc21b-151">Пользователя можно извлечь данные из объекта Document.</span><span class="sxs-lookup"><span data-stu-id="cc21b-151">The user can retrieve data from the Document object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc21b-152">dbSecWriteDef</span><span class="sxs-lookup"><span data-stu-id="cc21b-152">dbSecWriteDef</span></span></p></td>
<td><p><span data-ttu-id="cc21b-153">65548</span><span class="sxs-lookup"><span data-stu-id="cc21b-153">65548</span></span></p></td>
<td><p><span data-ttu-id="cc21b-154">Пользователь может изменить или удалить определение таблицы, включая сведения о столбце и индекса.</span><span class="sxs-lookup"><span data-stu-id="cc21b-154">The user can modify or delete the table definition, including column and index information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc21b-155">dbSecWriteOwner</span><span class="sxs-lookup"><span data-stu-id="cc21b-155">dbSecWriteOwner</span></span></p></td>
<td><p><span data-ttu-id="cc21b-156">524288</span><span class="sxs-lookup"><span data-stu-id="cc21b-156">524288</span></span></p></td>
<td><p><span data-ttu-id="cc21b-157">Пользователь может изменить значение свойства Owner.</span><span class="sxs-lookup"><span data-stu-id="cc21b-157">The user can change the Owner property setting.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc21b-158">dbSecWriteSec</span><span class="sxs-lookup"><span data-stu-id="cc21b-158">dbSecWriteSec</span></span></p></td>
<td><p><span data-ttu-id="cc21b-159">262144</span><span class="sxs-lookup"><span data-stu-id="cc21b-159">262144</span></span></p></td>
<td><p><span data-ttu-id="cc21b-160">Пользователь может изменить разрешения на доступ.</span><span class="sxs-lookup"><span data-stu-id="cc21b-160">The user can alter access permissions.</span></span></p></td>
</tr>
</tbody>
</table>

