---
title: RightsEnum (Справочник по для настольных баз данных Access)
TOCTitle: RightsEnum
ms:assetid: 7647b9d5-5271-fdcf-489d-5a8beb931ca5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249485(v=office.15)
ms:contentKeyID: 48545693
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 40cd7f789461e5b354186c2d5b8f81ec18344435
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861983"
---
# <a name="rightsenum"></a><span data-ttu-id="8e80e-102">RightsEnum</span><span class="sxs-lookup"><span data-stu-id="8e80e-102">RightsEnum</span></span>

<span data-ttu-id="8e80e-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8e80e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="8e80e-104">Задает права и разрешения для группы или пользователя на объект.</span><span class="sxs-lookup"><span data-stu-id="8e80e-104">Specifies the rights or permissions for a group or user on an object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8e80e-105">Константа</span><span class="sxs-lookup"><span data-stu-id="8e80e-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="8e80e-106">Значение</span><span class="sxs-lookup"><span data-stu-id="8e80e-106">Value</span></span></p></th>
<th><p><span data-ttu-id="8e80e-107">Описание</span><span class="sxs-lookup"><span data-stu-id="8e80e-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8e80e-108"><strong>adRightCreate</strong></span><span class="sxs-lookup"><span data-stu-id="8e80e-108"><strong>adRightCreate</strong></span></span></p></td>
<td><p><span data-ttu-id="8e80e-109">16384</span><span class="sxs-lookup"><span data-stu-id="8e80e-109">16384</span></span><br />
<span data-ttu-id="8e80e-110">(&amp;H4000)</span><span class="sxs-lookup"><span data-stu-id="8e80e-110">(&amp;H4000)</span></span></p></td>
<td><p><span data-ttu-id="8e80e-111">Пользователь или группа имеет право на создание новых объектов этого типа.</span><span class="sxs-lookup"><span data-stu-id="8e80e-111">The user or group has permission to create new objects of this type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e80e-112"><strong>adRightDelete</strong></span><span class="sxs-lookup"><span data-stu-id="8e80e-112"><strong>adRightDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="8e80e-113">65536</span><span class="sxs-lookup"><span data-stu-id="8e80e-113">65536</span></span><br />
<span data-ttu-id="8e80e-114">(&amp;H10000)</span><span class="sxs-lookup"><span data-stu-id="8e80e-114">(&amp;H10000)</span></span></p></td>
<td><p><span data-ttu-id="8e80e-115">Пользователь или группа имеет разрешение на удаление данных из объекта.</span><span class="sxs-lookup"><span data-stu-id="8e80e-115">The user or group has permission to delete data from an object.</span></span> <span data-ttu-id="8e80e-116">Для объектов, таких как <strong>таблицы</strong>пользователь имеет право удалять данные из записей.</span><span class="sxs-lookup"><span data-stu-id="8e80e-116">For objects such as <strong>Tables</strong>, the user has permission to delete data values from records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e80e-117"><strong>adRightDrop</strong></span><span class="sxs-lookup"><span data-stu-id="8e80e-117"><strong>adRightDrop</strong></span></span></p></td>
<td><p><span data-ttu-id="8e80e-118">256</span><span class="sxs-lookup"><span data-stu-id="8e80e-118">256</span></span><br />
<span data-ttu-id="8e80e-119">(&amp;H100)</span><span class="sxs-lookup"><span data-stu-id="8e80e-119">(&amp;H100)</span></span></p></td>
<td><p><span data-ttu-id="8e80e-120">Пользователь или группа имеет разрешение на удаление объектов из каталога.</span><span class="sxs-lookup"><span data-stu-id="8e80e-120">The user or group has permission to remove objects from the catalog.</span></span> <span data-ttu-id="8e80e-121">Например <strong>таблиц</strong> можно удалить с помощью команды DROP таблицы SQL.</span><span class="sxs-lookup"><span data-stu-id="8e80e-121">For example, <strong>Tables</strong> can be deleted by a DROP TABLE SQL command.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e80e-122"><strong>adRightExclusive</strong></span><span class="sxs-lookup"><span data-stu-id="8e80e-122"><strong>adRightExclusive</strong></span></span></p></td>
<td><p><span data-ttu-id="8e80e-123">512</span><span class="sxs-lookup"><span data-stu-id="8e80e-123">512</span></span><br />
<span data-ttu-id="8e80e-124">(&amp;H200)</span><span class="sxs-lookup"><span data-stu-id="8e80e-124">(&amp;H200)</span></span></p></td>
<td><p><span data-ttu-id="8e80e-125">Пользователь или группа имеет разрешение на доступ к объекту исключительно.</span><span class="sxs-lookup"><span data-stu-id="8e80e-125">The user or group has permission to access the object exclusively.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e80e-126"><strong>adRightExecute</strong></span><span class="sxs-lookup"><span data-stu-id="8e80e-126"><strong>adRightExecute</strong></span></span></p></td>
<td><p><span data-ttu-id="8e80e-127">536870912</span><span class="sxs-lookup"><span data-stu-id="8e80e-127">536870912</span></span><br />
<span data-ttu-id="8e80e-128">(&amp;H20000000)</span><span class="sxs-lookup"><span data-stu-id="8e80e-128">(&amp;H20000000)</span></span></p></td>
<td><p><span data-ttu-id="8e80e-129">Пользователь или группа имеет разрешение на выполнение объекта.</span><span class="sxs-lookup"><span data-stu-id="8e80e-129">The user or group has permission to execute the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e80e-130"><strong>adRightFull</strong></span><span class="sxs-lookup"><span data-stu-id="8e80e-130"><strong>adRightFull</strong></span></span></p></td>
<td><p><span data-ttu-id="8e80e-131">268435456</span><span class="sxs-lookup"><span data-stu-id="8e80e-131">268435456</span></span><br />
<span data-ttu-id="8e80e-132">(&amp;H10000000)</span><span class="sxs-lookup"><span data-stu-id="8e80e-132">(&amp;H10000000)</span></span></p></td>
<td><p><span data-ttu-id="8e80e-133">Пользователь или группа имеет все разрешения для объекта.</span><span class="sxs-lookup"><span data-stu-id="8e80e-133">The user or group has all permissions on the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e80e-134"><strong>adRightInsert</strong></span><span class="sxs-lookup"><span data-stu-id="8e80e-134"><strong>adRightInsert</strong></span></span></p></td>
<td><p><span data-ttu-id="8e80e-135">32768</span><span class="sxs-lookup"><span data-stu-id="8e80e-135">32768</span></span><br />
<span data-ttu-id="8e80e-136">(&amp;H8000)</span><span class="sxs-lookup"><span data-stu-id="8e80e-136">(&amp;H8000)</span></span></p></td>
<td><p><span data-ttu-id="8e80e-137">Пользователь или группа имеет разрешение для вставки объекта.</span><span class="sxs-lookup"><span data-stu-id="8e80e-137">The user or group has permission to insert the object.</span></span> <span data-ttu-id="8e80e-138">Для объектов, таких как <strong>таблицы</strong>пользователь имеет разрешения для вставки данных в таблицу.</span><span class="sxs-lookup"><span data-stu-id="8e80e-138">For objects such as <strong>Tables</strong>, the user has permission to insert data into the table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e80e-139"><strong>adRightMaximumAllowed</strong></span><span class="sxs-lookup"><span data-stu-id="8e80e-139"><strong>adRightMaximumAllowed</strong></span></span></p></td>
<td><p><span data-ttu-id="8e80e-140">33554432 (&amp;H2000000)</span><span class="sxs-lookup"><span data-stu-id="8e80e-140">33554432 (&amp;H2000000)</span></span></p></td>
<td><p><span data-ttu-id="8e80e-141">Пользователь или группа имеет максимальное количество разрешений, предоставляемых поставщика.</span><span class="sxs-lookup"><span data-stu-id="8e80e-141">The user or group has the maximum number of permissions allowed by the provider.</span></span> <span data-ttu-id="8e80e-142">Отдельные разрешения, зависят от поставщика.</span><span class="sxs-lookup"><span data-stu-id="8e80e-142">Specific permissions are provider-dependent.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e80e-143"><strong>adRightNone</strong></span><span class="sxs-lookup"><span data-stu-id="8e80e-143"><strong>adRightNone</strong></span></span></p></td>
<td><p><span data-ttu-id="8e80e-144">0</span><span class="sxs-lookup"><span data-stu-id="8e80e-144">0</span></span></p></td>
<td><p><span data-ttu-id="8e80e-145">Пользователь или группа не имеет разрешений для объекта.</span><span class="sxs-lookup"><span data-stu-id="8e80e-145">The user or group has no permissions for the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e80e-146"><strong>adRightRead</strong></span><span class="sxs-lookup"><span data-stu-id="8e80e-146"><strong>adRightRead</strong></span></span></p></td>
<td><p><span data-ttu-id="8e80e-147">-2147483648</span><span class="sxs-lookup"><span data-stu-id="8e80e-147">-2147483648</span></span><br />
<span data-ttu-id="8e80e-148">(&amp;H80000000)</span><span class="sxs-lookup"><span data-stu-id="8e80e-148">(&amp;H80000000)</span></span></p></td>
<td><p><span data-ttu-id="8e80e-149">Пользователь или группа имеет разрешение на чтение на объект.</span><span class="sxs-lookup"><span data-stu-id="8e80e-149">The user or group has permission to read the object.</span></span> <span data-ttu-id="8e80e-150">Для объектов, таких как <a href="table-object-adox.md">таблицы</a>пользователь имеет разрешения на чтение данных в таблице.</span><span class="sxs-lookup"><span data-stu-id="8e80e-150">For objects such as <a href="table-object-adox.md">Tables</a>, the user has permission to read the data in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e80e-151"><strong>adRightReadDesign</strong></span><span class="sxs-lookup"><span data-stu-id="8e80e-151"><strong>adRightReadDesign</strong></span></span></p></td>
<td><p><span data-ttu-id="8e80e-152">1024</span><span class="sxs-lookup"><span data-stu-id="8e80e-152">1024</span></span><br />
<span data-ttu-id="8e80e-153">(&amp;H400)</span><span class="sxs-lookup"><span data-stu-id="8e80e-153">(&amp;H400)</span></span></p></td>
<td><p><span data-ttu-id="8e80e-154">Пользователь или группа имеет разрешение на чтение конструктора для объекта.</span><span class="sxs-lookup"><span data-stu-id="8e80e-154">The user or group has permission to read the design for the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e80e-155"><strong>adRightReadPermissions</strong></span><span class="sxs-lookup"><span data-stu-id="8e80e-155"><strong>adRightReadPermissions</strong></span></span></p></td>
<td><p><span data-ttu-id="8e80e-156">131072</span><span class="sxs-lookup"><span data-stu-id="8e80e-156">131072</span></span><br />
<span data-ttu-id="8e80e-157">(&amp;H20000)</span><span class="sxs-lookup"><span data-stu-id="8e80e-157">(&amp;H20000)</span></span></p></td>
<td><p><span data-ttu-id="8e80e-158">Пользователя или группы могут просматривать, но не изменять определенные разрешения для объекта в каталоге.</span><span class="sxs-lookup"><span data-stu-id="8e80e-158">The user or group can view, but not change, the specific permissions for an object in the catalog.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e80e-159"><strong>adRightReference</strong></span><span class="sxs-lookup"><span data-stu-id="8e80e-159"><strong>adRightReference</strong></span></span></p></td>
<td><p><span data-ttu-id="8e80e-160">8192</span><span class="sxs-lookup"><span data-stu-id="8e80e-160">8192</span></span><br />
<span data-ttu-id="8e80e-161">(&amp;H2000)</span><span class="sxs-lookup"><span data-stu-id="8e80e-161">(&amp;H2000)</span></span></p></td>
<td><p><span data-ttu-id="8e80e-162">Пользователь или группа имеет разрешение для ссылки на объект.</span><span class="sxs-lookup"><span data-stu-id="8e80e-162">The user or group has permission to reference the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e80e-163"><strong>adRightUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="8e80e-163"><strong>adRightUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="8e80e-164">1073741824</span><span class="sxs-lookup"><span data-stu-id="8e80e-164">1073741824</span></span><br />
<span data-ttu-id="8e80e-165">(&amp;H40000000)</span><span class="sxs-lookup"><span data-stu-id="8e80e-165">(&amp;H40000000)</span></span></p></td>
<td><p><span data-ttu-id="8e80e-166">Пользователь или группа имеет разрешение на обновление объекта.</span><span class="sxs-lookup"><span data-stu-id="8e80e-166">The user or group has permission to update the object.</span></span> <span data-ttu-id="8e80e-167">Для объектов, таких как <strong>таблицы</strong>пользователь имеет разрешения на обновление данных в таблице.</span><span class="sxs-lookup"><span data-stu-id="8e80e-167">For objects such as <strong>Tables</strong>, the user has permission to update the data in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e80e-168"><strong>adRightWithGrant</strong></span><span class="sxs-lookup"><span data-stu-id="8e80e-168"><strong>adRightWithGrant</strong></span></span></p></td>
<td><p><span data-ttu-id="8e80e-169">4096</span><span class="sxs-lookup"><span data-stu-id="8e80e-169">4096</span></span><br />
<span data-ttu-id="8e80e-170">(&amp;H1000)</span><span class="sxs-lookup"><span data-stu-id="8e80e-170">(&amp;H1000)</span></span></p></td>
<td><p><span data-ttu-id="8e80e-171">Пользователь или группа имеет разрешение на предоставление разрешений на объект.</span><span class="sxs-lookup"><span data-stu-id="8e80e-171">The user or group has permission to grant permissions on the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e80e-172"><strong>adRightWriteDesign</strong></span><span class="sxs-lookup"><span data-stu-id="8e80e-172"><strong>adRightWriteDesign</strong></span></span></p></td>
<td><p><span data-ttu-id="8e80e-173">2048</span><span class="sxs-lookup"><span data-stu-id="8e80e-173">2048</span></span><br />
<span data-ttu-id="8e80e-174">(&amp;H800)</span><span class="sxs-lookup"><span data-stu-id="8e80e-174">(&amp;H800)</span></span></p></td>
<td><p><span data-ttu-id="8e80e-175">Пользователь или группа имеет разрешение на изменение структуры для объекта.</span><span class="sxs-lookup"><span data-stu-id="8e80e-175">The user or group has permission to modify the design for the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e80e-176"><strong>adRightWriteOwner</strong></span><span class="sxs-lookup"><span data-stu-id="8e80e-176"><strong>adRightWriteOwner</strong></span></span></p></td>
<td><p><span data-ttu-id="8e80e-177">524288</span><span class="sxs-lookup"><span data-stu-id="8e80e-177">524288</span></span><br />
<span data-ttu-id="8e80e-178">(&amp;H80000)</span><span class="sxs-lookup"><span data-stu-id="8e80e-178">(&amp;H80000)</span></span></p></td>
<td><p><span data-ttu-id="8e80e-179">Пользователь или группа имеет разрешение на изменение владельца объекта.</span><span class="sxs-lookup"><span data-stu-id="8e80e-179">The user or group has permission to modify the owner of the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e80e-180"><strong>adRightWritePermissions</strong></span><span class="sxs-lookup"><span data-stu-id="8e80e-180"><strong>adRightWritePermissions</strong></span></span></p></td>
<td><p><span data-ttu-id="8e80e-181">262144</span><span class="sxs-lookup"><span data-stu-id="8e80e-181">262144</span></span><br />
<span data-ttu-id="8e80e-182">(&amp;H40000)</span><span class="sxs-lookup"><span data-stu-id="8e80e-182">(&amp;H40000)</span></span></p></td>
<td><p><span data-ttu-id="8e80e-183">Пользователь или группа можно изменить определенные разрешения для объекта в каталоге.</span><span class="sxs-lookup"><span data-stu-id="8e80e-183">The user or group can modify the specific permissions for an object in the catalog.</span></span></p></td>
</tr>
</tbody>
</table>

