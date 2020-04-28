---
title: Ригхтсенум (Справочник по базам данных Access на компьютере)
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
# <a name="rightsenum"></a><span data-ttu-id="935a1-102">RightsEnum</span><span class="sxs-lookup"><span data-stu-id="935a1-102">RightsEnum</span></span>

<span data-ttu-id="935a1-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="935a1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="935a1-104">Задает права или разрешения для группы или пользователя в объекте.</span><span class="sxs-lookup"><span data-stu-id="935a1-104">Specifies the rights or permissions for a group or user on an object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="935a1-105">Константа</span><span class="sxs-lookup"><span data-stu-id="935a1-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="935a1-106">Значение</span><span class="sxs-lookup"><span data-stu-id="935a1-106">Value</span></span></p></th>
<th><p><span data-ttu-id="935a1-107">Описание</span><span class="sxs-lookup"><span data-stu-id="935a1-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="935a1-108"><strong>адригхткреате</strong></span><span class="sxs-lookup"><span data-stu-id="935a1-108"><strong>adRightCreate</strong></span></span></p></td>
<td><p><span data-ttu-id="935a1-109">16384</span><span class="sxs-lookup"><span data-stu-id="935a1-109">16384</span></span><br />
<span data-ttu-id="935a1-110">(&amp;H4000)</span><span class="sxs-lookup"><span data-stu-id="935a1-110">(&amp;H4000)</span></span></p></td>
<td><p><span data-ttu-id="935a1-111">Пользователь или группа имеет разрешение на создание новых объектов этого типа.</span><span class="sxs-lookup"><span data-stu-id="935a1-111">The user or group has permission to create new objects of this type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="935a1-112"><strong>адригхтделете</strong></span><span class="sxs-lookup"><span data-stu-id="935a1-112"><strong>adRightDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="935a1-113">65536</span><span class="sxs-lookup"><span data-stu-id="935a1-113">65536</span></span><br />
<span data-ttu-id="935a1-114">(&amp;H10000)</span><span class="sxs-lookup"><span data-stu-id="935a1-114">(&amp;H10000)</span></span></p></td>
<td><p><span data-ttu-id="935a1-115">Пользователь или группа имеет разрешение на удаление данных из объекта.</span><span class="sxs-lookup"><span data-stu-id="935a1-115">The user or group has permission to delete data from an object.</span></span> <span data-ttu-id="935a1-116">Для объектов, таких как <strong>таблицы</strong>, пользователь имеет разрешение на удаление значений данных из записей.</span><span class="sxs-lookup"><span data-stu-id="935a1-116">For objects such as <strong>Tables</strong>, the user has permission to delete data values from records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="935a1-117"><strong>адригхтдроп</strong></span><span class="sxs-lookup"><span data-stu-id="935a1-117"><strong>adRightDrop</strong></span></span></p></td>
<td><p><span data-ttu-id="935a1-118">256</span><span class="sxs-lookup"><span data-stu-id="935a1-118">256</span></span><br />
<span data-ttu-id="935a1-119">(&amp;H100)</span><span class="sxs-lookup"><span data-stu-id="935a1-119">(&amp;H100)</span></span></p></td>
<td><p><span data-ttu-id="935a1-120">Пользователь или группа имеет разрешение на удаление объектов из каталога.</span><span class="sxs-lookup"><span data-stu-id="935a1-120">The user or group has permission to remove objects from the catalog.</span></span> <span data-ttu-id="935a1-121">Например, <strong>таблицы</strong> можно удалить с помощью команды DROP TABLE SQL.</span><span class="sxs-lookup"><span data-stu-id="935a1-121">For example, <strong>Tables</strong> can be deleted by a DROP TABLE SQL command.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="935a1-122"><strong>адригхтексклусиве</strong></span><span class="sxs-lookup"><span data-stu-id="935a1-122"><strong>adRightExclusive</strong></span></span></p></td>
<td><p><span data-ttu-id="935a1-123">512</span><span class="sxs-lookup"><span data-stu-id="935a1-123">512</span></span><br />
<span data-ttu-id="935a1-124">(&amp;H200)</span><span class="sxs-lookup"><span data-stu-id="935a1-124">(&amp;H200)</span></span></p></td>
<td><p><span data-ttu-id="935a1-125">Пользователь или группа имеет разрешение на доступ к объекту в монопольном режиме.</span><span class="sxs-lookup"><span data-stu-id="935a1-125">The user or group has permission to access the object exclusively.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="935a1-126"><strong>адригхтексекуте</strong></span><span class="sxs-lookup"><span data-stu-id="935a1-126"><strong>adRightExecute</strong></span></span></p></td>
<td><p><span data-ttu-id="935a1-127">536870912</span><span class="sxs-lookup"><span data-stu-id="935a1-127">536870912</span></span><br />
<span data-ttu-id="935a1-128">(&amp;H20000000)</span><span class="sxs-lookup"><span data-stu-id="935a1-128">(&amp;H20000000)</span></span></p></td>
<td><p><span data-ttu-id="935a1-129">Пользователь или группа имеет разрешение на выполнение объекта.</span><span class="sxs-lookup"><span data-stu-id="935a1-129">The user or group has permission to execute the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="935a1-130"><strong>адригхтфулл</strong></span><span class="sxs-lookup"><span data-stu-id="935a1-130"><strong>adRightFull</strong></span></span></p></td>
<td><p><span data-ttu-id="935a1-131">268435456</span><span class="sxs-lookup"><span data-stu-id="935a1-131">268435456</span></span><br />
<span data-ttu-id="935a1-132">(&amp;H10000000)</span><span class="sxs-lookup"><span data-stu-id="935a1-132">(&amp;H10000000)</span></span></p></td>
<td><p><span data-ttu-id="935a1-133">У пользователя или группы есть все разрешения для объекта.</span><span class="sxs-lookup"><span data-stu-id="935a1-133">The user or group has all permissions on the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="935a1-134"><strong>адригхтинсерт</strong></span><span class="sxs-lookup"><span data-stu-id="935a1-134"><strong>adRightInsert</strong></span></span></p></td>
<td><p><span data-ttu-id="935a1-135">32768</span><span class="sxs-lookup"><span data-stu-id="935a1-135">32768</span></span><br />
<span data-ttu-id="935a1-136">(&amp;H8000)</span><span class="sxs-lookup"><span data-stu-id="935a1-136">(&amp;H8000)</span></span></p></td>
<td><p><span data-ttu-id="935a1-137">Пользователь или группа имеет разрешение на вставку объекта.</span><span class="sxs-lookup"><span data-stu-id="935a1-137">The user or group has permission to insert the object.</span></span> <span data-ttu-id="935a1-138">Для объектов, таких как <strong>таблицы</strong>, пользователь имеет разрешение на вставку данных в таблицу.</span><span class="sxs-lookup"><span data-stu-id="935a1-138">For objects such as <strong>Tables</strong>, the user has permission to insert data into the table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="935a1-139"><strong>адригхтмаксимумалловед</strong></span><span class="sxs-lookup"><span data-stu-id="935a1-139"><strong>adRightMaximumAllowed</strong></span></span></p></td>
<td><p><span data-ttu-id="935a1-140">33554432 (&amp;H2000000)</span><span class="sxs-lookup"><span data-stu-id="935a1-140">33554432 (&amp;H2000000)</span></span></p></td>
<td><p><span data-ttu-id="935a1-141">У пользователя или группы максимально допустимое количество разрешений, разрешенных поставщиком.</span><span class="sxs-lookup"><span data-stu-id="935a1-141">The user or group has the maximum number of permissions allowed by the provider.</span></span> <span data-ttu-id="935a1-142">Конкретные разрешения зависят от поставщика.</span><span class="sxs-lookup"><span data-stu-id="935a1-142">Specific permissions are provider-dependent.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="935a1-143"><strong>адригхтноне</strong></span><span class="sxs-lookup"><span data-stu-id="935a1-143"><strong>adRightNone</strong></span></span></p></td>
<td><p><span data-ttu-id="935a1-144">нуль</span><span class="sxs-lookup"><span data-stu-id="935a1-144">0</span></span></p></td>
<td><p><span data-ttu-id="935a1-145">Пользователь или группа не имеет разрешений для объекта.</span><span class="sxs-lookup"><span data-stu-id="935a1-145">The user or group has no permissions for the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="935a1-146"><strong>адригхтреад</strong></span><span class="sxs-lookup"><span data-stu-id="935a1-146"><strong>adRightRead</strong></span></span></p></td>
<td><p><span data-ttu-id="935a1-147">— 2147483648</span><span class="sxs-lookup"><span data-stu-id="935a1-147">-2147483648</span></span><br />
<span data-ttu-id="935a1-148">(&amp;H80000000)</span><span class="sxs-lookup"><span data-stu-id="935a1-148">(&amp;H80000000)</span></span></p></td>
<td><p><span data-ttu-id="935a1-149">Пользователь или группа имеет разрешение на чтение объекта.</span><span class="sxs-lookup"><span data-stu-id="935a1-149">The user or group has permission to read the object.</span></span> <span data-ttu-id="935a1-150">Для объектов, таких как <a href="table-object-adox.md">таблицы</a>, пользователь имеет разрешение на чтение данных в таблице.</span><span class="sxs-lookup"><span data-stu-id="935a1-150">For objects such as <a href="table-object-adox.md">Tables</a>, the user has permission to read the data in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="935a1-151"><strong>адригхтреаддесигн</strong></span><span class="sxs-lookup"><span data-stu-id="935a1-151"><strong>adRightReadDesign</strong></span></span></p></td>
<td><p><span data-ttu-id="935a1-152">1024</span><span class="sxs-lookup"><span data-stu-id="935a1-152">1024</span></span><br />
<span data-ttu-id="935a1-153">(&amp;H400)</span><span class="sxs-lookup"><span data-stu-id="935a1-153">(&amp;H400)</span></span></p></td>
<td><p><span data-ttu-id="935a1-154">Пользователь или группа имеет разрешение на чтение макета для объекта.</span><span class="sxs-lookup"><span data-stu-id="935a1-154">The user or group has permission to read the design for the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="935a1-155"><strong>адригхтреадпермиссионс</strong></span><span class="sxs-lookup"><span data-stu-id="935a1-155"><strong>adRightReadPermissions</strong></span></span></p></td>
<td><p><span data-ttu-id="935a1-156">131072</span><span class="sxs-lookup"><span data-stu-id="935a1-156">131072</span></span><br />
<span data-ttu-id="935a1-157">(&amp;H20000)</span><span class="sxs-lookup"><span data-stu-id="935a1-157">(&amp;H20000)</span></span></p></td>
<td><p><span data-ttu-id="935a1-158">Пользователь или группа может просматривать, но не изменять определенные разрешения для объекта в каталоге.</span><span class="sxs-lookup"><span data-stu-id="935a1-158">The user or group can view, but not change, the specific permissions for an object in the catalog.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="935a1-159"><strong>адригхтреференце</strong></span><span class="sxs-lookup"><span data-stu-id="935a1-159"><strong>adRightReference</strong></span></span></p></td>
<td><p><span data-ttu-id="935a1-160">8192</span><span class="sxs-lookup"><span data-stu-id="935a1-160">8192</span></span><br />
<span data-ttu-id="935a1-161">(&amp;H2000)</span><span class="sxs-lookup"><span data-stu-id="935a1-161">(&amp;H2000)</span></span></p></td>
<td><p><span data-ttu-id="935a1-162">Пользователь или группа имеет разрешение на ссылку на объект.</span><span class="sxs-lookup"><span data-stu-id="935a1-162">The user or group has permission to reference the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="935a1-163"><strong>адригхтупдате</strong></span><span class="sxs-lookup"><span data-stu-id="935a1-163"><strong>adRightUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="935a1-164">1073741824</span><span class="sxs-lookup"><span data-stu-id="935a1-164">1073741824</span></span><br />
<span data-ttu-id="935a1-165">(&amp;H40000000)</span><span class="sxs-lookup"><span data-stu-id="935a1-165">(&amp;H40000000)</span></span></p></td>
<td><p><span data-ttu-id="935a1-166">Пользователь или группа имеет разрешение на обновление объекта.</span><span class="sxs-lookup"><span data-stu-id="935a1-166">The user or group has permission to update the object.</span></span> <span data-ttu-id="935a1-167">Для объектов, таких как <strong>таблицы</strong>, пользователь имеет разрешение на обновление данных в таблице.</span><span class="sxs-lookup"><span data-stu-id="935a1-167">For objects such as <strong>Tables</strong>, the user has permission to update the data in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="935a1-168"><strong>адригхтвисгрант</strong></span><span class="sxs-lookup"><span data-stu-id="935a1-168"><strong>adRightWithGrant</strong></span></span></p></td>
<td><p><span data-ttu-id="935a1-169">4096</span><span class="sxs-lookup"><span data-stu-id="935a1-169">4096</span></span><br />
<span data-ttu-id="935a1-170">(&amp;H1000)</span><span class="sxs-lookup"><span data-stu-id="935a1-170">(&amp;H1000)</span></span></p></td>
<td><p><span data-ttu-id="935a1-171">Пользователь или группа имеет разрешение на предоставление разрешений для объекта.</span><span class="sxs-lookup"><span data-stu-id="935a1-171">The user or group has permission to grant permissions on the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="935a1-172"><strong>адригхтвритедесигн</strong></span><span class="sxs-lookup"><span data-stu-id="935a1-172"><strong>adRightWriteDesign</strong></span></span></p></td>
<td><p><span data-ttu-id="935a1-173">2048</span><span class="sxs-lookup"><span data-stu-id="935a1-173">2048</span></span><br />
<span data-ttu-id="935a1-174">(&amp;H800)</span><span class="sxs-lookup"><span data-stu-id="935a1-174">(&amp;H800)</span></span></p></td>
<td><p><span data-ttu-id="935a1-175">Пользователь или группа имеет разрешение на изменение макета объекта.</span><span class="sxs-lookup"><span data-stu-id="935a1-175">The user or group has permission to modify the design for the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="935a1-176"><strong>адригхтвритеовнер</strong></span><span class="sxs-lookup"><span data-stu-id="935a1-176"><strong>adRightWriteOwner</strong></span></span></p></td>
<td><p><span data-ttu-id="935a1-177">524288</span><span class="sxs-lookup"><span data-stu-id="935a1-177">524288</span></span><br />
<span data-ttu-id="935a1-178">(&amp;H80000)</span><span class="sxs-lookup"><span data-stu-id="935a1-178">(&amp;H80000)</span></span></p></td>
<td><p><span data-ttu-id="935a1-179">Пользователь или группа имеет разрешение на изменение владельца объекта.</span><span class="sxs-lookup"><span data-stu-id="935a1-179">The user or group has permission to modify the owner of the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="935a1-180"><strong>адригхтвритепермиссионс</strong></span><span class="sxs-lookup"><span data-stu-id="935a1-180"><strong>adRightWritePermissions</strong></span></span></p></td>
<td><p><span data-ttu-id="935a1-181">262144</span><span class="sxs-lookup"><span data-stu-id="935a1-181">262144</span></span><br />
<span data-ttu-id="935a1-182">(&amp;H40000)</span><span class="sxs-lookup"><span data-stu-id="935a1-182">(&amp;H40000)</span></span></p></td>
<td><p><span data-ttu-id="935a1-183">Пользователь или группа может изменять определенные разрешения для объекта в каталоге.</span><span class="sxs-lookup"><span data-stu-id="935a1-183">The user or group can modify the specific permissions for an object in the catalog.</span></span></p></td>
</tr>
</tbody>
</table>

