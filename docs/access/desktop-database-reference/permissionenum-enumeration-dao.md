---
title: PermissionEnum Enumeration (DAO)
TOCTitle: PermissionEnum Enumeration
ms:assetid: dcce9940-f8a7-e915-1b69-05c341bea8cd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835373(v=office.15)
ms:contentKeyID: 48548147
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0e87482940918f3e12713f2e207e2e590895838a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481367"
---
# <a name="permissionenum-enumeration-dao"></a><span data-ttu-id="541c9-102">PermissionEnum Enumeration (DAO)</span><span class="sxs-lookup"><span data-stu-id="541c9-102">PermissionEnum Enumeration (DAO)</span></span>


<span data-ttu-id="541c9-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="541c9-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="541c9-104">Используется совместно со свойством **разрешения** , чтобы указать тип разрешения.</span><span class="sxs-lookup"><span data-stu-id="541c9-104">Used with the **Permissions** property to specify the type of permissions.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="541c9-105">Имя</span><span class="sxs-lookup"><span data-stu-id="541c9-105">Name</span></span></p></th>
<th><p><span data-ttu-id="541c9-106">Значение</span><span class="sxs-lookup"><span data-stu-id="541c9-106">Value</span></span></p></th>
<th><p><span data-ttu-id="541c9-107">Описание</span><span class="sxs-lookup"><span data-stu-id="541c9-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="541c9-108">dbSecCreate</span><span class="sxs-lookup"><span data-stu-id="541c9-108">dbSecCreate</span></span></p></td>
<td><p><span data-ttu-id="541c9-109">1</span><span class="sxs-lookup"><span data-stu-id="541c9-109">1</span></span></p></td>
<td><p><span data-ttu-id="541c9-110">Пользователь может создавать новые документы (недействительно для объектов-документов).</span><span class="sxs-lookup"><span data-stu-id="541c9-110">The user can create new documents (not valid for Document objects).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="541c9-111">dbSecDBAdmin</span><span class="sxs-lookup"><span data-stu-id="541c9-111">dbSecDBAdmin</span></span></p></td>
<td><p><span data-ttu-id="541c9-112">8</span><span class="sxs-lookup"><span data-stu-id="541c9-112">8</span></span></p></td>
<td><p><span data-ttu-id="541c9-113">Пользователь может репликации базы данных и изменение пароля базы данных (недействительно для объектов-документов).</span><span class="sxs-lookup"><span data-stu-id="541c9-113">The user can replicate a database and change the database password (not valid for Document objects).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="541c9-114">dbSecDBCreate</span><span class="sxs-lookup"><span data-stu-id="541c9-114">dbSecDBCreate</span></span></p></td>
<td><p><span data-ttu-id="541c9-115">1</span><span class="sxs-lookup"><span data-stu-id="541c9-115">1</span></span></p></td>
<td><p><span data-ttu-id="541c9-116">Пользователь может создавать новые базы данных.</span><span class="sxs-lookup"><span data-stu-id="541c9-116">The user can create new databases.</span></span> <span data-ttu-id="541c9-117">Этот параметр действителен только на контейнер баз данных в файле рабочей группы (Systen.mdw).</span><span class="sxs-lookup"><span data-stu-id="541c9-117">This option is valid only on the Databases container in the workgroup information file (Systen.mdw).</span></span> <span data-ttu-id="541c9-118">В этом константа недопустима для объектов документа.</span><span class="sxs-lookup"><span data-stu-id="541c9-118">This constant is not valid for Document objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="541c9-119">dbSecDBExclusive</span><span class="sxs-lookup"><span data-stu-id="541c9-119">dbSecDBExclusive</span></span></p></td>
<td><p><span data-ttu-id="541c9-120">4</span><span class="sxs-lookup"><span data-stu-id="541c9-120">4</span></span></p></td>
<td><p><span data-ttu-id="541c9-121">Пользователь имеет исключительных доступ к базе данных.</span><span class="sxs-lookup"><span data-stu-id="541c9-121">The user has exclusive access to the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="541c9-122">dbSecDBOpen</span><span class="sxs-lookup"><span data-stu-id="541c9-122">dbSecDBOpen</span></span></p></td>
<td><p><span data-ttu-id="541c9-123">2</span><span class="sxs-lookup"><span data-stu-id="541c9-123">2</span></span></p></td>
<td><p><span data-ttu-id="541c9-124">Пользователь может открыть базу данных.</span><span class="sxs-lookup"><span data-stu-id="541c9-124">The user can open the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="541c9-125">dbSecDelete</span><span class="sxs-lookup"><span data-stu-id="541c9-125">dbSecDelete</span></span></p></td>
<td><p><span data-ttu-id="541c9-126">65536</span><span class="sxs-lookup"><span data-stu-id="541c9-126">65536</span></span></p></td>
<td><p><span data-ttu-id="541c9-127">Пользователь может удалить объект.</span><span class="sxs-lookup"><span data-stu-id="541c9-127">The user can delete the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="541c9-128">dbSecDeleteData</span><span class="sxs-lookup"><span data-stu-id="541c9-128">dbSecDeleteData</span></span></p></td>
<td><p><span data-ttu-id="541c9-129">128</span><span class="sxs-lookup"><span data-stu-id="541c9-129">128</span></span></p></td>
<td><p><span data-ttu-id="541c9-130">Пользователь может удалить записи.</span><span class="sxs-lookup"><span data-stu-id="541c9-130">The user can delete records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="541c9-131">dbSecFullAccess</span><span class="sxs-lookup"><span data-stu-id="541c9-131">dbSecFullAccess</span></span></p></td>
<td><p><span data-ttu-id="541c9-132">1048575</span><span class="sxs-lookup"><span data-stu-id="541c9-132">1048575</span></span></p></td>
<td><p><span data-ttu-id="541c9-133">Пользователь имеет полный доступ к объекту.</span><span class="sxs-lookup"><span data-stu-id="541c9-133">The user has full access to the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="541c9-134">dbSecInsertData</span><span class="sxs-lookup"><span data-stu-id="541c9-134">dbSecInsertData</span></span></p></td>
<td><p><span data-ttu-id="541c9-135">32</span><span class="sxs-lookup"><span data-stu-id="541c9-135">32</span></span></p></td>
<td><p><span data-ttu-id="541c9-136">Пользователь может добавить записи.</span><span class="sxs-lookup"><span data-stu-id="541c9-136">The user can add records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="541c9-137">dbSecNoAccess</span><span class="sxs-lookup"><span data-stu-id="541c9-137">dbSecNoAccess</span></span></p></td>
<td><p><span data-ttu-id="541c9-138">0</span><span class="sxs-lookup"><span data-stu-id="541c9-138">0</span></span></p></td>
<td><p><span data-ttu-id="541c9-139">Пользователь не имеет доступ к объекту (недействительно для объектов-документов).</span><span class="sxs-lookup"><span data-stu-id="541c9-139">The user does not have access to the object (not valid for Document objects).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="541c9-140">dbSecReadDef</span><span class="sxs-lookup"><span data-stu-id="541c9-140">dbSecReadDef</span></span></p></td>
<td><p><span data-ttu-id="541c9-141">4</span><span class="sxs-lookup"><span data-stu-id="541c9-141">4</span></span></p></td>
<td><p><span data-ttu-id="541c9-142">Пользователь может читать определение таблицы, включая сведения о столбце и индекса.</span><span class="sxs-lookup"><span data-stu-id="541c9-142">The user can read the table definition, including column and index information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="541c9-143">dbSecReadSec</span><span class="sxs-lookup"><span data-stu-id="541c9-143">dbSecReadSec</span></span></p></td>
<td><p><span data-ttu-id="541c9-144">131072</span><span class="sxs-lookup"><span data-stu-id="541c9-144">131072</span></span></p></td>
<td><p><span data-ttu-id="541c9-145">Пользователи могут читать сведения из объекта безопасности.</span><span class="sxs-lookup"><span data-stu-id="541c9-145">The user can read the object's security-related information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="541c9-146">dbSecReplaceData</span><span class="sxs-lookup"><span data-stu-id="541c9-146">dbSecReplaceData</span></span></p></td>
<td><p><span data-ttu-id="541c9-147">64</span><span class="sxs-lookup"><span data-stu-id="541c9-147">64</span></span></p></td>
<td><p><span data-ttu-id="541c9-148">Пользователь может изменять записи.</span><span class="sxs-lookup"><span data-stu-id="541c9-148">The user can modify records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="541c9-149">dbSecRetrieveData</span><span class="sxs-lookup"><span data-stu-id="541c9-149">dbSecRetrieveData</span></span></p></td>
<td><p><span data-ttu-id="541c9-150">20</span><span class="sxs-lookup"><span data-stu-id="541c9-150">20</span></span></p></td>
<td><p><span data-ttu-id="541c9-151">Пользователя можно извлечь данные из объекта Document.</span><span class="sxs-lookup"><span data-stu-id="541c9-151">The user can retrieve data from the Document object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="541c9-152">dbSecWriteDef</span><span class="sxs-lookup"><span data-stu-id="541c9-152">dbSecWriteDef</span></span></p></td>
<td><p><span data-ttu-id="541c9-153">65548</span><span class="sxs-lookup"><span data-stu-id="541c9-153">65548</span></span></p></td>
<td><p><span data-ttu-id="541c9-154">Пользователь может изменить или удалить определение таблицы, включая сведения о столбце и индекса.</span><span class="sxs-lookup"><span data-stu-id="541c9-154">The user can modify or delete the table definition, including column and index information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="541c9-155">dbSecWriteOwner</span><span class="sxs-lookup"><span data-stu-id="541c9-155">dbSecWriteOwner</span></span></p></td>
<td><p><span data-ttu-id="541c9-156">524288</span><span class="sxs-lookup"><span data-stu-id="541c9-156">524288</span></span></p></td>
<td><p><span data-ttu-id="541c9-157">Пользователь может изменить значение свойства Owner.</span><span class="sxs-lookup"><span data-stu-id="541c9-157">The user can change the Owner property setting.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="541c9-158">dbSecWriteSec</span><span class="sxs-lookup"><span data-stu-id="541c9-158">dbSecWriteSec</span></span></p></td>
<td><p><span data-ttu-id="541c9-159">262144</span><span class="sxs-lookup"><span data-stu-id="541c9-159">262144</span></span></p></td>
<td><p><span data-ttu-id="541c9-160">Пользователь может изменить разрешения на доступ.</span><span class="sxs-lookup"><span data-stu-id="541c9-160">The user can alter access permissions.</span></span></p></td>
</tr>
</tbody>
</table>

