---
title: RightsEnum (Справочник по для настольных баз данных Access)
TOCTitle: RightsEnum
ms:assetid: 7647b9d5-5271-fdcf-489d-5a8beb931ca5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249485(v=office.15)
ms:contentKeyID: 48545693
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 535c80bf5cd3dbfecae0e004082ce20d01c31fde
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877389"
---
# <a name="rightsenum"></a><span data-ttu-id="4b90d-102">RightsEnum</span><span class="sxs-lookup"><span data-stu-id="4b90d-102">RightsEnum</span></span>

<span data-ttu-id="4b90d-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4b90d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4b90d-104">Задает права и разрешения для группы или пользователя на объект.</span><span class="sxs-lookup"><span data-stu-id="4b90d-104">Specifies the rights or permissions for a group or user on an object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4b90d-105">Константа</span><span class="sxs-lookup"><span data-stu-id="4b90d-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="4b90d-106">Значение</span><span class="sxs-lookup"><span data-stu-id="4b90d-106">Value</span></span></p></th>
<th><p><span data-ttu-id="4b90d-107">Описание</span><span class="sxs-lookup"><span data-stu-id="4b90d-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4b90d-108"><strong>adRightCreate</strong></span><span class="sxs-lookup"><span data-stu-id="4b90d-108"><strong>adRightCreate</strong></span></span></p></td>
<td><p><span data-ttu-id="4b90d-109">16384</span><span class="sxs-lookup"><span data-stu-id="4b90d-109">16384</span></span><br />
<span data-ttu-id="4b90d-110">(&amp;H4000)</span><span class="sxs-lookup"><span data-stu-id="4b90d-110">(&amp;H4000)</span></span></p></td>
<td><p><span data-ttu-id="4b90d-111">Пользователь или группа имеет право на создание новых объектов этого типа.</span><span class="sxs-lookup"><span data-stu-id="4b90d-111">The user or group has permission to create new objects of this type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b90d-112"><strong>adRightDelete</strong></span><span class="sxs-lookup"><span data-stu-id="4b90d-112"><strong>adRightDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="4b90d-113">65536</span><span class="sxs-lookup"><span data-stu-id="4b90d-113">65536</span></span><br />
<span data-ttu-id="4b90d-114">(&amp;H10000)</span><span class="sxs-lookup"><span data-stu-id="4b90d-114">(&amp;H10000)</span></span></p></td>
<td><p><span data-ttu-id="4b90d-115">Пользователь или группа имеет разрешение на удаление данных из объекта.</span><span class="sxs-lookup"><span data-stu-id="4b90d-115">The user or group has permission to delete data from an object.</span></span> <span data-ttu-id="4b90d-116">Для объектов, таких как <strong>таблицы</strong>пользователь имеет право удалять данные из записей.</span><span class="sxs-lookup"><span data-stu-id="4b90d-116">For objects such as <strong>Tables</strong>, the user has permission to delete data values from records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b90d-117"><strong>adRightDrop</strong></span><span class="sxs-lookup"><span data-stu-id="4b90d-117"><strong>adRightDrop</strong></span></span></p></td>
<td><p><span data-ttu-id="4b90d-118">256</span><span class="sxs-lookup"><span data-stu-id="4b90d-118">256</span></span><br />
<span data-ttu-id="4b90d-119">(&amp;H100)</span><span class="sxs-lookup"><span data-stu-id="4b90d-119">(&amp;H100)</span></span></p></td>
<td><p><span data-ttu-id="4b90d-120">Пользователь или группа имеет разрешение на удаление объектов из каталога.</span><span class="sxs-lookup"><span data-stu-id="4b90d-120">The user or group has permission to remove objects from the catalog.</span></span> <span data-ttu-id="4b90d-121">Например <strong>таблиц</strong> можно удалить с помощью команды DROP таблицы SQL.</span><span class="sxs-lookup"><span data-stu-id="4b90d-121">For example, <strong>Tables</strong> can be deleted by a DROP TABLE SQL command.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b90d-122"><strong>adRightExclusive</strong></span><span class="sxs-lookup"><span data-stu-id="4b90d-122"><strong>adRightExclusive</strong></span></span></p></td>
<td><p><span data-ttu-id="4b90d-123">512</span><span class="sxs-lookup"><span data-stu-id="4b90d-123">512</span></span><br />
<span data-ttu-id="4b90d-124">(&amp;H200)</span><span class="sxs-lookup"><span data-stu-id="4b90d-124">(&amp;H200)</span></span></p></td>
<td><p><span data-ttu-id="4b90d-125">Пользователь или группа имеет разрешение на доступ к объекту исключительно.</span><span class="sxs-lookup"><span data-stu-id="4b90d-125">The user or group has permission to access the object exclusively.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b90d-126"><strong>adRightExecute</strong></span><span class="sxs-lookup"><span data-stu-id="4b90d-126"><strong>adRightExecute</strong></span></span></p></td>
<td><p><span data-ttu-id="4b90d-127">536870912</span><span class="sxs-lookup"><span data-stu-id="4b90d-127">536870912</span></span><br />
<span data-ttu-id="4b90d-128">(&amp;H20000000)</span><span class="sxs-lookup"><span data-stu-id="4b90d-128">(&amp;H20000000)</span></span></p></td>
<td><p><span data-ttu-id="4b90d-129">Пользователь или группа имеет разрешение на выполнение объекта.</span><span class="sxs-lookup"><span data-stu-id="4b90d-129">The user or group has permission to execute the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b90d-130"><strong>adRightFull</strong></span><span class="sxs-lookup"><span data-stu-id="4b90d-130"><strong>adRightFull</strong></span></span></p></td>
<td><p><span data-ttu-id="4b90d-131">268435456</span><span class="sxs-lookup"><span data-stu-id="4b90d-131">268435456</span></span><br />
<span data-ttu-id="4b90d-132">(&amp;H10000000)</span><span class="sxs-lookup"><span data-stu-id="4b90d-132">(&amp;H10000000)</span></span></p></td>
<td><p><span data-ttu-id="4b90d-133">Пользователь или группа имеет все разрешения для объекта.</span><span class="sxs-lookup"><span data-stu-id="4b90d-133">The user or group has all permissions on the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b90d-134"><strong>adRightInsert</strong></span><span class="sxs-lookup"><span data-stu-id="4b90d-134"><strong>adRightInsert</strong></span></span></p></td>
<td><p><span data-ttu-id="4b90d-135">32768</span><span class="sxs-lookup"><span data-stu-id="4b90d-135">32768</span></span><br />
<span data-ttu-id="4b90d-136">(&amp;H8000)</span><span class="sxs-lookup"><span data-stu-id="4b90d-136">(&amp;H8000)</span></span></p></td>
<td><p><span data-ttu-id="4b90d-137">Пользователь или группа имеет разрешение для вставки объекта.</span><span class="sxs-lookup"><span data-stu-id="4b90d-137">The user or group has permission to insert the object.</span></span> <span data-ttu-id="4b90d-138">Для объектов, таких как <strong>таблицы</strong>пользователь имеет разрешения для вставки данных в таблицу.</span><span class="sxs-lookup"><span data-stu-id="4b90d-138">For objects such as <strong>Tables</strong>, the user has permission to insert data into the table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b90d-139"><strong>adRightMaximumAllowed</strong></span><span class="sxs-lookup"><span data-stu-id="4b90d-139"><strong>adRightMaximumAllowed</strong></span></span></p></td>
<td><p><span data-ttu-id="4b90d-140">33554432 (&amp;H2000000)</span><span class="sxs-lookup"><span data-stu-id="4b90d-140">33554432 (&amp;H2000000)</span></span></p></td>
<td><p><span data-ttu-id="4b90d-141">Пользователь или группа имеет максимальное количество разрешений, предоставляемых поставщика.</span><span class="sxs-lookup"><span data-stu-id="4b90d-141">The user or group has the maximum number of permissions allowed by the provider.</span></span> <span data-ttu-id="4b90d-142">Отдельные разрешения, зависят от поставщика.</span><span class="sxs-lookup"><span data-stu-id="4b90d-142">Specific permissions are provider-dependent.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b90d-143"><strong>adRightNone</strong></span><span class="sxs-lookup"><span data-stu-id="4b90d-143"><strong>adRightNone</strong></span></span></p></td>
<td><p><span data-ttu-id="4b90d-144">0</span><span class="sxs-lookup"><span data-stu-id="4b90d-144">0</span></span></p></td>
<td><p><span data-ttu-id="4b90d-145">Пользователь или группа не имеет разрешений для объекта.</span><span class="sxs-lookup"><span data-stu-id="4b90d-145">The user or group has no permissions for the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b90d-146"><strong>adRightRead</strong></span><span class="sxs-lookup"><span data-stu-id="4b90d-146"><strong>adRightRead</strong></span></span></p></td>
<td><p><span data-ttu-id="4b90d-147">-2147483648</span><span class="sxs-lookup"><span data-stu-id="4b90d-147">-2147483648</span></span><br />
<span data-ttu-id="4b90d-148">(&amp;H80000000)</span><span class="sxs-lookup"><span data-stu-id="4b90d-148">(&amp;H80000000)</span></span></p></td>
<td><p><span data-ttu-id="4b90d-149">Пользователь или группа имеет разрешение на чтение на объект.</span><span class="sxs-lookup"><span data-stu-id="4b90d-149">The user or group has permission to read the object.</span></span> <span data-ttu-id="4b90d-150">Для объектов, таких как <a href="table-object-adox.md">таблицы</a>пользователь имеет разрешения на чтение данных в таблице.</span><span class="sxs-lookup"><span data-stu-id="4b90d-150">For objects such as <a href="table-object-adox.md">Tables</a>, the user has permission to read the data in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b90d-151"><strong>adRightReadDesign</strong></span><span class="sxs-lookup"><span data-stu-id="4b90d-151"><strong>adRightReadDesign</strong></span></span></p></td>
<td><p><span data-ttu-id="4b90d-152">1024</span><span class="sxs-lookup"><span data-stu-id="4b90d-152">1024</span></span><br />
<span data-ttu-id="4b90d-153">(&amp;H400)</span><span class="sxs-lookup"><span data-stu-id="4b90d-153">(&amp;H400)</span></span></p></td>
<td><p><span data-ttu-id="4b90d-154">Пользователь или группа имеет разрешение на чтение конструктора для объекта.</span><span class="sxs-lookup"><span data-stu-id="4b90d-154">The user or group has permission to read the design for the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b90d-155"><strong>adRightReadPermissions</strong></span><span class="sxs-lookup"><span data-stu-id="4b90d-155"><strong>adRightReadPermissions</strong></span></span></p></td>
<td><p><span data-ttu-id="4b90d-156">131072</span><span class="sxs-lookup"><span data-stu-id="4b90d-156">131072</span></span><br />
<span data-ttu-id="4b90d-157">(&amp;H20000)</span><span class="sxs-lookup"><span data-stu-id="4b90d-157">(&amp;H20000)</span></span></p></td>
<td><p><span data-ttu-id="4b90d-158">Пользователя или группы могут просматривать, но не изменять определенные разрешения для объекта в каталоге.</span><span class="sxs-lookup"><span data-stu-id="4b90d-158">The user or group can view, but not change, the specific permissions for an object in the catalog.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b90d-159"><strong>adRightReference</strong></span><span class="sxs-lookup"><span data-stu-id="4b90d-159"><strong>adRightReference</strong></span></span></p></td>
<td><p><span data-ttu-id="4b90d-160">8192</span><span class="sxs-lookup"><span data-stu-id="4b90d-160">8192</span></span><br />
<span data-ttu-id="4b90d-161">(&amp;H2000)</span><span class="sxs-lookup"><span data-stu-id="4b90d-161">(&amp;H2000)</span></span></p></td>
<td><p><span data-ttu-id="4b90d-162">Пользователь или группа имеет разрешение для ссылки на объект.</span><span class="sxs-lookup"><span data-stu-id="4b90d-162">The user or group has permission to reference the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b90d-163"><strong>adRightUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="4b90d-163"><strong>adRightUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="4b90d-164">1073741824</span><span class="sxs-lookup"><span data-stu-id="4b90d-164">1073741824</span></span><br />
<span data-ttu-id="4b90d-165">(&amp;H40000000)</span><span class="sxs-lookup"><span data-stu-id="4b90d-165">(&amp;H40000000)</span></span></p></td>
<td><p><span data-ttu-id="4b90d-166">Пользователь или группа имеет разрешение на обновление объекта.</span><span class="sxs-lookup"><span data-stu-id="4b90d-166">The user or group has permission to update the object.</span></span> <span data-ttu-id="4b90d-167">Для объектов, таких как <strong>таблицы</strong>пользователь имеет разрешения на обновление данных в таблице.</span><span class="sxs-lookup"><span data-stu-id="4b90d-167">For objects such as <strong>Tables</strong>, the user has permission to update the data in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b90d-168"><strong>adRightWithGrant</strong></span><span class="sxs-lookup"><span data-stu-id="4b90d-168"><strong>adRightWithGrant</strong></span></span></p></td>
<td><p><span data-ttu-id="4b90d-169">4096</span><span class="sxs-lookup"><span data-stu-id="4b90d-169">4096</span></span><br />
<span data-ttu-id="4b90d-170">(&amp;H1000)</span><span class="sxs-lookup"><span data-stu-id="4b90d-170">(&amp;H1000)</span></span></p></td>
<td><p><span data-ttu-id="4b90d-171">Пользователь или группа имеет разрешение на предоставление разрешений на объект.</span><span class="sxs-lookup"><span data-stu-id="4b90d-171">The user or group has permission to grant permissions on the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b90d-172"><strong>adRightWriteDesign</strong></span><span class="sxs-lookup"><span data-stu-id="4b90d-172"><strong>adRightWriteDesign</strong></span></span></p></td>
<td><p><span data-ttu-id="4b90d-173">2048</span><span class="sxs-lookup"><span data-stu-id="4b90d-173">2048</span></span><br />
<span data-ttu-id="4b90d-174">(&amp;H800)</span><span class="sxs-lookup"><span data-stu-id="4b90d-174">(&amp;H800)</span></span></p></td>
<td><p><span data-ttu-id="4b90d-175">Пользователь или группа имеет разрешение на изменение структуры для объекта.</span><span class="sxs-lookup"><span data-stu-id="4b90d-175">The user or group has permission to modify the design for the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b90d-176"><strong>adRightWriteOwner</strong></span><span class="sxs-lookup"><span data-stu-id="4b90d-176"><strong>adRightWriteOwner</strong></span></span></p></td>
<td><p><span data-ttu-id="4b90d-177">524288</span><span class="sxs-lookup"><span data-stu-id="4b90d-177">524288</span></span><br />
<span data-ttu-id="4b90d-178">(&amp;H80000)</span><span class="sxs-lookup"><span data-stu-id="4b90d-178">(&amp;H80000)</span></span></p></td>
<td><p><span data-ttu-id="4b90d-179">Пользователь или группа имеет разрешение на изменение владельца объекта.</span><span class="sxs-lookup"><span data-stu-id="4b90d-179">The user or group has permission to modify the owner of the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b90d-180"><strong>adRightWritePermissions</strong></span><span class="sxs-lookup"><span data-stu-id="4b90d-180"><strong>adRightWritePermissions</strong></span></span></p></td>
<td><p><span data-ttu-id="4b90d-181">262144</span><span class="sxs-lookup"><span data-stu-id="4b90d-181">262144</span></span><br />
<span data-ttu-id="4b90d-182">(&amp;H40000)</span><span class="sxs-lookup"><span data-stu-id="4b90d-182">(&amp;H40000)</span></span></p></td>
<td><p><span data-ttu-id="4b90d-183">Пользователь или группа можно изменить определенные разрешения для объекта в каталоге.</span><span class="sxs-lookup"><span data-stu-id="4b90d-183">The user or group can modify the specific permissions for an object in the catalog.</span></span></p></td>
</tr>
</tbody>
</table>

