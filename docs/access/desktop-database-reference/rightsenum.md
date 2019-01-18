---
title: RightsEnum (Справочник по для настольных баз данных Access)
TOCTitle: RightsEnum
ms:assetid: 7647b9d5-5271-fdcf-489d-5a8beb931ca5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249485(v=office.15)
ms:contentKeyID: 48545693
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3c7bf2f88632265cda7537215f2ea3c68507f16f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706606"
---
# <a name="rightsenum"></a><span data-ttu-id="c82a7-102">RightsEnum</span><span class="sxs-lookup"><span data-stu-id="c82a7-102">RightsEnum</span></span>

<span data-ttu-id="c82a7-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c82a7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c82a7-104">Задает права и разрешения для группы или пользователя на объект.</span><span class="sxs-lookup"><span data-stu-id="c82a7-104">Specifies the rights or permissions for a group or user on an object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c82a7-105">Константа</span><span class="sxs-lookup"><span data-stu-id="c82a7-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="c82a7-106">Значение</span><span class="sxs-lookup"><span data-stu-id="c82a7-106">Value</span></span></p></th>
<th><p><span data-ttu-id="c82a7-107">Описание</span><span class="sxs-lookup"><span data-stu-id="c82a7-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c82a7-108"><strong>adRightCreate</strong></span><span class="sxs-lookup"><span data-stu-id="c82a7-108"><strong>adRightCreate</strong></span></span></p></td>
<td><p><span data-ttu-id="c82a7-109">16384</span><span class="sxs-lookup"><span data-stu-id="c82a7-109">16384</span></span><br />
<span data-ttu-id="c82a7-110">(&amp;H4000)</span><span class="sxs-lookup"><span data-stu-id="c82a7-110">(&amp;H4000)</span></span></p></td>
<td><p><span data-ttu-id="c82a7-111">Пользователь или группа имеет право на создание новых объектов этого типа.</span><span class="sxs-lookup"><span data-stu-id="c82a7-111">The user or group has permission to create new objects of this type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c82a7-112"><strong>adRightDelete</strong></span><span class="sxs-lookup"><span data-stu-id="c82a7-112"><strong>adRightDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="c82a7-113">65536</span><span class="sxs-lookup"><span data-stu-id="c82a7-113">65536</span></span><br />
<span data-ttu-id="c82a7-114">(&amp;H10000)</span><span class="sxs-lookup"><span data-stu-id="c82a7-114">(&amp;H10000)</span></span></p></td>
<td><p><span data-ttu-id="c82a7-115">Пользователь или группа имеет разрешение на удаление данных из объекта.</span><span class="sxs-lookup"><span data-stu-id="c82a7-115">The user or group has permission to delete data from an object.</span></span> <span data-ttu-id="c82a7-116">Для объектов, таких как <strong>таблицы</strong>пользователь имеет право удалять данные из записей.</span><span class="sxs-lookup"><span data-stu-id="c82a7-116">For objects such as <strong>Tables</strong>, the user has permission to delete data values from records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c82a7-117"><strong>adRightDrop</strong></span><span class="sxs-lookup"><span data-stu-id="c82a7-117"><strong>adRightDrop</strong></span></span></p></td>
<td><p><span data-ttu-id="c82a7-118">256</span><span class="sxs-lookup"><span data-stu-id="c82a7-118">256</span></span><br />
<span data-ttu-id="c82a7-119">(&amp;H100)</span><span class="sxs-lookup"><span data-stu-id="c82a7-119">(&amp;H100)</span></span></p></td>
<td><p><span data-ttu-id="c82a7-120">Пользователь или группа имеет разрешение на удаление объектов из каталога.</span><span class="sxs-lookup"><span data-stu-id="c82a7-120">The user or group has permission to remove objects from the catalog.</span></span> <span data-ttu-id="c82a7-121">Например <strong>таблиц</strong> можно удалить с помощью команды DROP таблицы SQL.</span><span class="sxs-lookup"><span data-stu-id="c82a7-121">For example, <strong>Tables</strong> can be deleted by a DROP TABLE SQL command.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c82a7-122"><strong>adRightExclusive</strong></span><span class="sxs-lookup"><span data-stu-id="c82a7-122"><strong>adRightExclusive</strong></span></span></p></td>
<td><p><span data-ttu-id="c82a7-123">512</span><span class="sxs-lookup"><span data-stu-id="c82a7-123">512</span></span><br />
<span data-ttu-id="c82a7-124">(&amp;H200)</span><span class="sxs-lookup"><span data-stu-id="c82a7-124">(&amp;H200)</span></span></p></td>
<td><p><span data-ttu-id="c82a7-125">Пользователь или группа имеет разрешение на доступ к объекту исключительно.</span><span class="sxs-lookup"><span data-stu-id="c82a7-125">The user or group has permission to access the object exclusively.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c82a7-126"><strong>adRightExecute</strong></span><span class="sxs-lookup"><span data-stu-id="c82a7-126"><strong>adRightExecute</strong></span></span></p></td>
<td><p><span data-ttu-id="c82a7-127">536870912</span><span class="sxs-lookup"><span data-stu-id="c82a7-127">536870912</span></span><br />
<span data-ttu-id="c82a7-128">(&amp;H20000000)</span><span class="sxs-lookup"><span data-stu-id="c82a7-128">(&amp;H20000000)</span></span></p></td>
<td><p><span data-ttu-id="c82a7-129">Пользователь или группа имеет разрешение на выполнение объекта.</span><span class="sxs-lookup"><span data-stu-id="c82a7-129">The user or group has permission to execute the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c82a7-130"><strong>adRightFull</strong></span><span class="sxs-lookup"><span data-stu-id="c82a7-130"><strong>adRightFull</strong></span></span></p></td>
<td><p><span data-ttu-id="c82a7-131">268435456</span><span class="sxs-lookup"><span data-stu-id="c82a7-131">268435456</span></span><br />
<span data-ttu-id="c82a7-132">(&amp;H10000000)</span><span class="sxs-lookup"><span data-stu-id="c82a7-132">(&amp;H10000000)</span></span></p></td>
<td><p><span data-ttu-id="c82a7-133">Пользователь или группа имеет все разрешения для объекта.</span><span class="sxs-lookup"><span data-stu-id="c82a7-133">The user or group has all permissions on the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c82a7-134"><strong>adRightInsert</strong></span><span class="sxs-lookup"><span data-stu-id="c82a7-134"><strong>adRightInsert</strong></span></span></p></td>
<td><p><span data-ttu-id="c82a7-135">32768</span><span class="sxs-lookup"><span data-stu-id="c82a7-135">32768</span></span><br />
<span data-ttu-id="c82a7-136">(&amp;H8000)</span><span class="sxs-lookup"><span data-stu-id="c82a7-136">(&amp;H8000)</span></span></p></td>
<td><p><span data-ttu-id="c82a7-137">Пользователь или группа имеет разрешение для вставки объекта.</span><span class="sxs-lookup"><span data-stu-id="c82a7-137">The user or group has permission to insert the object.</span></span> <span data-ttu-id="c82a7-138">Для объектов, таких как <strong>таблицы</strong>пользователь имеет разрешения для вставки данных в таблицу.</span><span class="sxs-lookup"><span data-stu-id="c82a7-138">For objects such as <strong>Tables</strong>, the user has permission to insert data into the table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c82a7-139"><strong>adRightMaximumAllowed</strong></span><span class="sxs-lookup"><span data-stu-id="c82a7-139"><strong>adRightMaximumAllowed</strong></span></span></p></td>
<td><p><span data-ttu-id="c82a7-140">33554432 (&amp;H2000000)</span><span class="sxs-lookup"><span data-stu-id="c82a7-140">33554432 (&amp;H2000000)</span></span></p></td>
<td><p><span data-ttu-id="c82a7-141">Пользователь или группа имеет максимальное количество разрешений, предоставляемых поставщика.</span><span class="sxs-lookup"><span data-stu-id="c82a7-141">The user or group has the maximum number of permissions allowed by the provider.</span></span> <span data-ttu-id="c82a7-142">Отдельные разрешения, зависят от поставщика.</span><span class="sxs-lookup"><span data-stu-id="c82a7-142">Specific permissions are provider-dependent.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c82a7-143"><strong>adRightNone</strong></span><span class="sxs-lookup"><span data-stu-id="c82a7-143"><strong>adRightNone</strong></span></span></p></td>
<td><p><span data-ttu-id="c82a7-144">0</span><span class="sxs-lookup"><span data-stu-id="c82a7-144">0</span></span></p></td>
<td><p><span data-ttu-id="c82a7-145">Пользователь или группа не имеет разрешений для объекта.</span><span class="sxs-lookup"><span data-stu-id="c82a7-145">The user or group has no permissions for the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c82a7-146"><strong>adRightRead</strong></span><span class="sxs-lookup"><span data-stu-id="c82a7-146"><strong>adRightRead</strong></span></span></p></td>
<td><p><span data-ttu-id="c82a7-147">-2147483648</span><span class="sxs-lookup"><span data-stu-id="c82a7-147">-2147483648</span></span><br />
<span data-ttu-id="c82a7-148">(&amp;H80000000)</span><span class="sxs-lookup"><span data-stu-id="c82a7-148">(&amp;H80000000)</span></span></p></td>
<td><p><span data-ttu-id="c82a7-149">Пользователь или группа имеет разрешение на чтение на объект.</span><span class="sxs-lookup"><span data-stu-id="c82a7-149">The user or group has permission to read the object.</span></span> <span data-ttu-id="c82a7-150">Для объектов, таких как <a href="table-object-adox.md">таблицы</a>пользователь имеет разрешения на чтение данных в таблице.</span><span class="sxs-lookup"><span data-stu-id="c82a7-150">For objects such as <a href="table-object-adox.md">Tables</a>, the user has permission to read the data in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c82a7-151"><strong>adRightReadDesign</strong></span><span class="sxs-lookup"><span data-stu-id="c82a7-151"><strong>adRightReadDesign</strong></span></span></p></td>
<td><p><span data-ttu-id="c82a7-152">1024</span><span class="sxs-lookup"><span data-stu-id="c82a7-152">1024</span></span><br />
<span data-ttu-id="c82a7-153">(&amp;H400)</span><span class="sxs-lookup"><span data-stu-id="c82a7-153">(&amp;H400)</span></span></p></td>
<td><p><span data-ttu-id="c82a7-154">Пользователь или группа имеет разрешение на чтение конструктора для объекта.</span><span class="sxs-lookup"><span data-stu-id="c82a7-154">The user or group has permission to read the design for the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c82a7-155"><strong>adRightReadPermissions</strong></span><span class="sxs-lookup"><span data-stu-id="c82a7-155"><strong>adRightReadPermissions</strong></span></span></p></td>
<td><p><span data-ttu-id="c82a7-156">131072</span><span class="sxs-lookup"><span data-stu-id="c82a7-156">131072</span></span><br />
<span data-ttu-id="c82a7-157">(&amp;H20000)</span><span class="sxs-lookup"><span data-stu-id="c82a7-157">(&amp;H20000)</span></span></p></td>
<td><p><span data-ttu-id="c82a7-158">Пользователя или группы могут просматривать, но не изменять определенные разрешения для объекта в каталоге.</span><span class="sxs-lookup"><span data-stu-id="c82a7-158">The user or group can view, but not change, the specific permissions for an object in the catalog.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c82a7-159"><strong>adRightReference</strong></span><span class="sxs-lookup"><span data-stu-id="c82a7-159"><strong>adRightReference</strong></span></span></p></td>
<td><p><span data-ttu-id="c82a7-160">8192</span><span class="sxs-lookup"><span data-stu-id="c82a7-160">8192</span></span><br />
<span data-ttu-id="c82a7-161">(&amp;H2000)</span><span class="sxs-lookup"><span data-stu-id="c82a7-161">(&amp;H2000)</span></span></p></td>
<td><p><span data-ttu-id="c82a7-162">Пользователь или группа имеет разрешение для ссылки на объект.</span><span class="sxs-lookup"><span data-stu-id="c82a7-162">The user or group has permission to reference the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c82a7-163"><strong>adRightUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="c82a7-163"><strong>adRightUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="c82a7-164">1073741824</span><span class="sxs-lookup"><span data-stu-id="c82a7-164">1073741824</span></span><br />
<span data-ttu-id="c82a7-165">(&amp;H40000000)</span><span class="sxs-lookup"><span data-stu-id="c82a7-165">(&amp;H40000000)</span></span></p></td>
<td><p><span data-ttu-id="c82a7-166">Пользователь или группа имеет разрешение на обновление объекта.</span><span class="sxs-lookup"><span data-stu-id="c82a7-166">The user or group has permission to update the object.</span></span> <span data-ttu-id="c82a7-167">Для объектов, таких как <strong>таблицы</strong>пользователь имеет разрешения на обновление данных в таблице.</span><span class="sxs-lookup"><span data-stu-id="c82a7-167">For objects such as <strong>Tables</strong>, the user has permission to update the data in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c82a7-168"><strong>adRightWithGrant</strong></span><span class="sxs-lookup"><span data-stu-id="c82a7-168"><strong>adRightWithGrant</strong></span></span></p></td>
<td><p><span data-ttu-id="c82a7-169">4096</span><span class="sxs-lookup"><span data-stu-id="c82a7-169">4096</span></span><br />
<span data-ttu-id="c82a7-170">(&amp;H1000)</span><span class="sxs-lookup"><span data-stu-id="c82a7-170">(&amp;H1000)</span></span></p></td>
<td><p><span data-ttu-id="c82a7-171">Пользователь или группа имеет разрешение на предоставление разрешений на объект.</span><span class="sxs-lookup"><span data-stu-id="c82a7-171">The user or group has permission to grant permissions on the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c82a7-172"><strong>adRightWriteDesign</strong></span><span class="sxs-lookup"><span data-stu-id="c82a7-172"><strong>adRightWriteDesign</strong></span></span></p></td>
<td><p><span data-ttu-id="c82a7-173">2048</span><span class="sxs-lookup"><span data-stu-id="c82a7-173">2048</span></span><br />
<span data-ttu-id="c82a7-174">(&amp;H800)</span><span class="sxs-lookup"><span data-stu-id="c82a7-174">(&amp;H800)</span></span></p></td>
<td><p><span data-ttu-id="c82a7-175">Пользователь или группа имеет разрешение на изменение структуры для объекта.</span><span class="sxs-lookup"><span data-stu-id="c82a7-175">The user or group has permission to modify the design for the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c82a7-176"><strong>adRightWriteOwner</strong></span><span class="sxs-lookup"><span data-stu-id="c82a7-176"><strong>adRightWriteOwner</strong></span></span></p></td>
<td><p><span data-ttu-id="c82a7-177">524288</span><span class="sxs-lookup"><span data-stu-id="c82a7-177">524288</span></span><br />
<span data-ttu-id="c82a7-178">(&amp;H80000)</span><span class="sxs-lookup"><span data-stu-id="c82a7-178">(&amp;H80000)</span></span></p></td>
<td><p><span data-ttu-id="c82a7-179">Пользователь или группа имеет разрешение на изменение владельца объекта.</span><span class="sxs-lookup"><span data-stu-id="c82a7-179">The user or group has permission to modify the owner of the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c82a7-180"><strong>adRightWritePermissions</strong></span><span class="sxs-lookup"><span data-stu-id="c82a7-180"><strong>adRightWritePermissions</strong></span></span></p></td>
<td><p><span data-ttu-id="c82a7-181">262144</span><span class="sxs-lookup"><span data-stu-id="c82a7-181">262144</span></span><br />
<span data-ttu-id="c82a7-182">(&amp;H40000)</span><span class="sxs-lookup"><span data-stu-id="c82a7-182">(&amp;H40000)</span></span></p></td>
<td><p><span data-ttu-id="c82a7-183">Пользователь или группа можно изменить определенные разрешения для объекта в каталоге.</span><span class="sxs-lookup"><span data-stu-id="c82a7-183">The user or group can modify the specific permissions for an object in the catalog.</span></span></p></td>
</tr>
</tbody>
</table>

