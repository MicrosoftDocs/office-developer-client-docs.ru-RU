---
title: RightsEnum (справочник по базе данных Access для настольных ПК)
TOCTitle: RightsEnum
ms:assetid: 7647b9d5-5271-fdcf-489d-5a8beb931ca5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249485(v=office.15)
ms:contentKeyID: 48545693
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3c7bf2f88632265cda7537215f2ea3c68507f16f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306491"
---
# <a name="rightsenum"></a><span data-ttu-id="4ea57-102">RightsEnum</span><span class="sxs-lookup"><span data-stu-id="4ea57-102">RightsEnum</span></span>

<span data-ttu-id="4ea57-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4ea57-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4ea57-104">Указывает права или разрешения для группы или пользователя объекта.</span><span class="sxs-lookup"><span data-stu-id="4ea57-104">Specifies the rights or permissions for a group or user on an object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4ea57-105">Константа</span><span class="sxs-lookup"><span data-stu-id="4ea57-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="4ea57-106">Значение</span><span class="sxs-lookup"><span data-stu-id="4ea57-106">Value</span></span></p></th>
<th><p><span data-ttu-id="4ea57-107">Описание</span><span class="sxs-lookup"><span data-stu-id="4ea57-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4ea57-108"><strong>adRightCreate</strong></span><span class="sxs-lookup"><span data-stu-id="4ea57-108"><strong>adRightCreate</strong></span></span></p></td>
<td><p><span data-ttu-id="4ea57-109">16384</span><span class="sxs-lookup"><span data-stu-id="4ea57-109">16384</span></span><br />
<span data-ttu-id="4ea57-110">( &amp; H4000)</span><span class="sxs-lookup"><span data-stu-id="4ea57-110">(&amp;H4000)</span></span></p></td>
<td><p><span data-ttu-id="4ea57-111">Пользователь или группа имеет разрешение на создание новых объектов этого типа.</span><span class="sxs-lookup"><span data-stu-id="4ea57-111">The user or group has permission to create new objects of this type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ea57-112"><strong>adRightDelete</strong></span><span class="sxs-lookup"><span data-stu-id="4ea57-112"><strong>adRightDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="4ea57-113">65536</span><span class="sxs-lookup"><span data-stu-id="4ea57-113">65536</span></span><br />
<span data-ttu-id="4ea57-114">( &amp; H10000)</span><span class="sxs-lookup"><span data-stu-id="4ea57-114">(&amp;H10000)</span></span></p></td>
<td><p><span data-ttu-id="4ea57-115">Пользователь или группа имеет разрешение на удаление данных из объекта.</span><span class="sxs-lookup"><span data-stu-id="4ea57-115">The user or group has permission to delete data from an object.</span></span> <span data-ttu-id="4ea57-116">Для таких объектов, как <strong>таблицы,</strong>пользователь имеет разрешение на удаление значений данных из записей.</span><span class="sxs-lookup"><span data-stu-id="4ea57-116">For objects such as <strong>Tables</strong>, the user has permission to delete data values from records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ea57-117"><strong>adRightDrop</strong></span><span class="sxs-lookup"><span data-stu-id="4ea57-117"><strong>adRightDrop</strong></span></span></p></td>
<td><p><span data-ttu-id="4ea57-118">256</span><span class="sxs-lookup"><span data-stu-id="4ea57-118">256</span></span><br />
<span data-ttu-id="4ea57-119">( &amp; H100)</span><span class="sxs-lookup"><span data-stu-id="4ea57-119">(&amp;H100)</span></span></p></td>
<td><p><span data-ttu-id="4ea57-120">Пользователь или группа имеет разрешение на удаление объектов из каталога.</span><span class="sxs-lookup"><span data-stu-id="4ea57-120">The user or group has permission to remove objects from the catalog.</span></span> <span data-ttu-id="4ea57-121">Например, <strong>таблицы</strong> можно удалить с помощью команды DROP TABLE SQL.</span><span class="sxs-lookup"><span data-stu-id="4ea57-121">For example, <strong>Tables</strong> can be deleted by a DROP TABLE SQL command.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ea57-122"><strong>adRightExclusive</strong></span><span class="sxs-lookup"><span data-stu-id="4ea57-122"><strong>adRightExclusive</strong></span></span></p></td>
<td><p><span data-ttu-id="4ea57-123">512</span><span class="sxs-lookup"><span data-stu-id="4ea57-123">512</span></span><br />
<span data-ttu-id="4ea57-124">( &amp; H200)</span><span class="sxs-lookup"><span data-stu-id="4ea57-124">(&amp;H200)</span></span></p></td>
<td><p><span data-ttu-id="4ea57-125">Пользователь или группа имеет разрешение на доступ к объекту исключительно.</span><span class="sxs-lookup"><span data-stu-id="4ea57-125">The user or group has permission to access the object exclusively.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ea57-126"><strong>adRightExecute</strong></span><span class="sxs-lookup"><span data-stu-id="4ea57-126"><strong>adRightExecute</strong></span></span></p></td>
<td><p><span data-ttu-id="4ea57-127">536870912</span><span class="sxs-lookup"><span data-stu-id="4ea57-127">536870912</span></span><br />
<span data-ttu-id="4ea57-128">( &amp; H20000000)</span><span class="sxs-lookup"><span data-stu-id="4ea57-128">(&amp;H20000000)</span></span></p></td>
<td><p><span data-ttu-id="4ea57-129">Пользователь или группа имеет разрешение на выполнение объекта.</span><span class="sxs-lookup"><span data-stu-id="4ea57-129">The user or group has permission to execute the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ea57-130"><strong>adRightFull</strong></span><span class="sxs-lookup"><span data-stu-id="4ea57-130"><strong>adRightFull</strong></span></span></p></td>
<td><p><span data-ttu-id="4ea57-131">268435456</span><span class="sxs-lookup"><span data-stu-id="4ea57-131">268435456</span></span><br />
<span data-ttu-id="4ea57-132">( &amp; H10000000)</span><span class="sxs-lookup"><span data-stu-id="4ea57-132">(&amp;H10000000)</span></span></p></td>
<td><p><span data-ttu-id="4ea57-133">Пользователь или группа имеет все разрешения на объект.</span><span class="sxs-lookup"><span data-stu-id="4ea57-133">The user or group has all permissions on the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ea57-134"><strong>adRightInsert</strong></span><span class="sxs-lookup"><span data-stu-id="4ea57-134"><strong>adRightInsert</strong></span></span></p></td>
<td><p><span data-ttu-id="4ea57-135">32768</span><span class="sxs-lookup"><span data-stu-id="4ea57-135">32768</span></span><br />
<span data-ttu-id="4ea57-136">( &amp; H8000)</span><span class="sxs-lookup"><span data-stu-id="4ea57-136">(&amp;H8000)</span></span></p></td>
<td><p><span data-ttu-id="4ea57-137">Пользователь или группа имеет разрешение на вставку объекта.</span><span class="sxs-lookup"><span data-stu-id="4ea57-137">The user or group has permission to insert the object.</span></span> <span data-ttu-id="4ea57-138">Для таких объектов, как <strong>таблицы,</strong>пользователь имеет разрешение на вставку данных в таблицу.</span><span class="sxs-lookup"><span data-stu-id="4ea57-138">For objects such as <strong>Tables</strong>, the user has permission to insert data into the table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ea57-139"><strong>adRightMaximumAllowed</strong></span><span class="sxs-lookup"><span data-stu-id="4ea57-139"><strong>adRightMaximumAllowed</strong></span></span></p></td>
<td><p><span data-ttu-id="4ea57-140">33554432 ( &amp; H2000000)</span><span class="sxs-lookup"><span data-stu-id="4ea57-140">33554432 (&amp;H2000000)</span></span></p></td>
<td><p><span data-ttu-id="4ea57-141">Пользователь или группа имеет максимальное число разрешений, разрешенных поставщиком.</span><span class="sxs-lookup"><span data-stu-id="4ea57-141">The user or group has the maximum number of permissions allowed by the provider.</span></span> <span data-ttu-id="4ea57-142">Определенные разрешения зависят от поставщика.</span><span class="sxs-lookup"><span data-stu-id="4ea57-142">Specific permissions are provider-dependent.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ea57-143"><strong>adRightNone</strong></span><span class="sxs-lookup"><span data-stu-id="4ea57-143"><strong>adRightNone</strong></span></span></p></td>
<td><p><span data-ttu-id="4ea57-144">0</span><span class="sxs-lookup"><span data-stu-id="4ea57-144">0</span></span></p></td>
<td><p><span data-ttu-id="4ea57-145">У пользователя или группы нет разрешений для объекта.</span><span class="sxs-lookup"><span data-stu-id="4ea57-145">The user or group has no permissions for the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ea57-146"><strong>adRightRead</strong></span><span class="sxs-lookup"><span data-stu-id="4ea57-146"><strong>adRightRead</strong></span></span></p></td>
<td><p><span data-ttu-id="4ea57-147">-2147483648</span><span class="sxs-lookup"><span data-stu-id="4ea57-147">-2147483648</span></span><br />
<span data-ttu-id="4ea57-148">( &amp; H80000000)</span><span class="sxs-lookup"><span data-stu-id="4ea57-148">(&amp;H80000000)</span></span></p></td>
<td><p><span data-ttu-id="4ea57-149">Пользователь или группа имеет разрешение на чтение объекта.</span><span class="sxs-lookup"><span data-stu-id="4ea57-149">The user or group has permission to read the object.</span></span> <span data-ttu-id="4ea57-150">Для таких объектов, как <a href="table-object-adox.md">таблицы,</a>пользователь имеет разрешение на чтение данных в таблице.</span><span class="sxs-lookup"><span data-stu-id="4ea57-150">For objects such as <a href="table-object-adox.md">Tables</a>, the user has permission to read the data in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ea57-151"><strong>adRightReadDesign</strong></span><span class="sxs-lookup"><span data-stu-id="4ea57-151"><strong>adRightReadDesign</strong></span></span></p></td>
<td><p><span data-ttu-id="4ea57-152">1024</span><span class="sxs-lookup"><span data-stu-id="4ea57-152">1024</span></span><br />
<span data-ttu-id="4ea57-153">( &amp; H400)</span><span class="sxs-lookup"><span data-stu-id="4ea57-153">(&amp;H400)</span></span></p></td>
<td><p><span data-ttu-id="4ea57-154">Пользователь или группа имеет разрешение на чтение проекта объекта.</span><span class="sxs-lookup"><span data-stu-id="4ea57-154">The user or group has permission to read the design for the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ea57-155"><strong>adRightReadPermissions</strong></span><span class="sxs-lookup"><span data-stu-id="4ea57-155"><strong>adRightReadPermissions</strong></span></span></p></td>
<td><p><span data-ttu-id="4ea57-156">131072</span><span class="sxs-lookup"><span data-stu-id="4ea57-156">131072</span></span><br />
<span data-ttu-id="4ea57-157">( &amp; H20000)</span><span class="sxs-lookup"><span data-stu-id="4ea57-157">(&amp;H20000)</span></span></p></td>
<td><p><span data-ttu-id="4ea57-158">Пользователь или группа могут просматривать( но не изменять) определенные разрешения для объекта в каталоге.</span><span class="sxs-lookup"><span data-stu-id="4ea57-158">The user or group can view, but not change, the specific permissions for an object in the catalog.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ea57-159"><strong>adRightReference</strong></span><span class="sxs-lookup"><span data-stu-id="4ea57-159"><strong>adRightReference</strong></span></span></p></td>
<td><p><span data-ttu-id="4ea57-160">8192</span><span class="sxs-lookup"><span data-stu-id="4ea57-160">8192</span></span><br />
<span data-ttu-id="4ea57-161">( &amp; H2000)</span><span class="sxs-lookup"><span data-stu-id="4ea57-161">(&amp;H2000)</span></span></p></td>
<td><p><span data-ttu-id="4ea57-162">Пользователь или группа имеет разрешение на ссылку на объект.</span><span class="sxs-lookup"><span data-stu-id="4ea57-162">The user or group has permission to reference the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ea57-163"><strong>adRightUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="4ea57-163"><strong>adRightUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="4ea57-164">1073741824</span><span class="sxs-lookup"><span data-stu-id="4ea57-164">1073741824</span></span><br />
<span data-ttu-id="4ea57-165">( &amp; H40000000)</span><span class="sxs-lookup"><span data-stu-id="4ea57-165">(&amp;H40000000)</span></span></p></td>
<td><p><span data-ttu-id="4ea57-166">Пользователь или группа имеет разрешение на обновление объекта.</span><span class="sxs-lookup"><span data-stu-id="4ea57-166">The user or group has permission to update the object.</span></span> <span data-ttu-id="4ea57-167">Для таких объектов, как <strong>таблицы,</strong>пользователь имеет разрешение на обновление данных в таблице.</span><span class="sxs-lookup"><span data-stu-id="4ea57-167">For objects such as <strong>Tables</strong>, the user has permission to update the data in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ea57-168"><strong>adRightWithGrant</strong></span><span class="sxs-lookup"><span data-stu-id="4ea57-168"><strong>adRightWithGrant</strong></span></span></p></td>
<td><p><span data-ttu-id="4ea57-169">4096</span><span class="sxs-lookup"><span data-stu-id="4ea57-169">4096</span></span><br />
<span data-ttu-id="4ea57-170">( &amp; H1000)</span><span class="sxs-lookup"><span data-stu-id="4ea57-170">(&amp;H1000)</span></span></p></td>
<td><p><span data-ttu-id="4ea57-171">Пользователь или группа имеет разрешение на предоставление разрешений для объекта.</span><span class="sxs-lookup"><span data-stu-id="4ea57-171">The user or group has permission to grant permissions on the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ea57-172"><strong>adRightWriteDesign</strong></span><span class="sxs-lookup"><span data-stu-id="4ea57-172"><strong>adRightWriteDesign</strong></span></span></p></td>
<td><p><span data-ttu-id="4ea57-173">2048</span><span class="sxs-lookup"><span data-stu-id="4ea57-173">2048</span></span><br />
<span data-ttu-id="4ea57-174">( &amp; H800)</span><span class="sxs-lookup"><span data-stu-id="4ea57-174">(&amp;H800)</span></span></p></td>
<td><p><span data-ttu-id="4ea57-175">Пользователь или группа имеет разрешение на изменение проекта объекта.</span><span class="sxs-lookup"><span data-stu-id="4ea57-175">The user or group has permission to modify the design for the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ea57-176"><strong>adRightWriteOwner</strong></span><span class="sxs-lookup"><span data-stu-id="4ea57-176"><strong>adRightWriteOwner</strong></span></span></p></td>
<td><p><span data-ttu-id="4ea57-177">524288</span><span class="sxs-lookup"><span data-stu-id="4ea57-177">524288</span></span><br />
<span data-ttu-id="4ea57-178">( &amp; H80000)</span><span class="sxs-lookup"><span data-stu-id="4ea57-178">(&amp;H80000)</span></span></p></td>
<td><p><span data-ttu-id="4ea57-179">Пользователь или группа имеет разрешение на изменение владельца объекта.</span><span class="sxs-lookup"><span data-stu-id="4ea57-179">The user or group has permission to modify the owner of the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ea57-180"><strong>adRightWritePermissions</strong></span><span class="sxs-lookup"><span data-stu-id="4ea57-180"><strong>adRightWritePermissions</strong></span></span></p></td>
<td><p><span data-ttu-id="4ea57-181">262144</span><span class="sxs-lookup"><span data-stu-id="4ea57-181">262144</span></span><br />
<span data-ttu-id="4ea57-182">( &amp; H40000)</span><span class="sxs-lookup"><span data-stu-id="4ea57-182">(&amp;H40000)</span></span></p></td>
<td><p><span data-ttu-id="4ea57-183">Пользователь или группа могут изменять определенные разрешения для объекта в каталоге.</span><span class="sxs-lookup"><span data-stu-id="4ea57-183">The user or group can modify the specific permissions for an object in the catalog.</span></span></p></td>
</tr>
</tbody>
</table>

