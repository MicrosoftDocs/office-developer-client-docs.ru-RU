---
title: Использование объектов данных ActiveX
TOCTitle: Use ActiveX Data Objects
description: Microsoft Access предоставляет три объектные модели, которые можно использовать при создании, обслуживании и управлении базами данных Access и связанными с ними данными с помощью Visual Basic.
ms:assetid: 64055c45-7a27-2296-468a-015362898329
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194969(v=office.15)
ms:contentKeyID: 48545279
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5285627
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 3b530db43a816e66b9fbef254984142aadf0b841
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312742"
---
# <a name="use-activex-data-objects"></a><span data-ttu-id="a113e-103">Использование объектов данных ActiveX</span><span class="sxs-lookup"><span data-stu-id="a113e-103">Use ActiveX Data Objects</span></span>

<span data-ttu-id="a113e-104">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a113e-104">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a113e-105">Microsoft Access предоставляет три объектные модели, которые можно использовать при создании, обслуживании и управлении базами данных Access и связанными с ними данными с помощью Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="a113e-105">Microsoft Access provides three object models to use in the creation, maintaining, and managing of your Access databases and their related data by using Visual Basic.</span></span>

## <a name="microsoft-activex-data-objects-ado"></a><span data-ttu-id="a113e-106">Microsoft ActiveX Data Objects (ADO)</span><span class="sxs-lookup"><span data-stu-id="a113e-106">Microsoft ActiveX Data Objects (ADO)</span></span>

<span data-ttu-id="a113e-107">ADO содержит объекты, необходимые для создания, обслуживания и удаления записей в заданный datasource.</span><span class="sxs-lookup"><span data-stu-id="a113e-107">ADO contains the objects needed to create, maintain, and delete records in a given datasource.</span></span>

## <a name="microsoft-ado-ext-for-ddl-and-security-adox"></a><span data-ttu-id="a113e-108">Microsoft ADO ext. for DDL and security (ADOX)</span><span class="sxs-lookup"><span data-stu-id="a113e-108">Microsoft ADO ext. for DDL and security (ADOX)</span></span>

<span data-ttu-id="a113e-109">ADOX предоставляет объекты языка определения данных (DDL), необходимые для создания новой базы данных и ее содержащихся объектов в дополнение к объектам, необходимым для управления безопасностью.</span><span class="sxs-lookup"><span data-stu-id="a113e-109">ADOX provides the Data Definition Language (DDL) objects needed to create a new database and its contained objects in addition to the objects needed to manage security.</span></span>

### <a name="microsoft-jet-and-replication-objects-25-library-jro"></a><span data-ttu-id="a113e-110">Библиотека Объектов Microsoft Jet и объектов репликации 2.5 (JRO)</span><span class="sxs-lookup"><span data-stu-id="a113e-110">Microsoft Jet and Replication Objects 2.5 library (JRO)</span></span>

<span data-ttu-id="a113e-111">Поскольку объекты ADO были разработаны для работы со многими базами данных в дополнение к базам данных Microsoft Jet, функциональные возможности, специфифиченные для Jet, были разбиты на библиотеку JRO.</span><span class="sxs-lookup"><span data-stu-id="a113e-111">Because ADO objects were designed to work with many databases in addition to Microsoft Jet databases, functionality specific to Jet was broken out into the JRO library.</span></span>

<span data-ttu-id="a113e-112">В следующей таблице перечислены функции, предоставляемые по сравнению с DAO.</span><span class="sxs-lookup"><span data-stu-id="a113e-112">The following table lists the functionality provided by each compared to DAO.</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a113e-113">функциональность.</span><span class="sxs-lookup"><span data-stu-id="a113e-113">Functionality</span></span></p></th>
<th><p><span data-ttu-id="a113e-114">DAO</span><span class="sxs-lookup"><span data-stu-id="a113e-114">DAO</span></span></p></th>
<th><p><span data-ttu-id="a113e-115">ADO1</span><span class="sxs-lookup"><span data-stu-id="a113e-115">ADO1</span></span></p></th>
<th><p><span data-ttu-id="a113e-116">ADOX2</span><span class="sxs-lookup"><span data-stu-id="a113e-116">ADOX2</span></span></p></th>
<th><p><span data-ttu-id="a113e-117">JRO</span><span class="sxs-lookup"><span data-stu-id="a113e-117">JRO</span></span><br />
<span data-ttu-id="a113e-118">(Только MDB)</span><span class="sxs-lookup"><span data-stu-id="a113e-118">(MDBs only)</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a113e-119">Создание записей.</span><span class="sxs-lookup"><span data-stu-id="a113e-119">Create Recordsets.</span></span></p></td>
<td><p><span data-ttu-id="a113e-120">X</span><span class="sxs-lookup"><span data-stu-id="a113e-120">X</span></span></p></td>
<td><p><span data-ttu-id="a113e-121">X</span><span class="sxs-lookup"><span data-stu-id="a113e-121">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a113e-122">Изменение свойств запуска.</span><span class="sxs-lookup"><span data-stu-id="a113e-122">Edit Startup properties.</span></span></p></td>
<td><p><span data-ttu-id="a113e-123">X</span><span class="sxs-lookup"><span data-stu-id="a113e-123">X</span></span></p></td>
<td><p><span data-ttu-id="a113e-124">X\*\*</span><span class="sxs-lookup"><span data-stu-id="a113e-124">X\*\*</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a113e-125">Поддержка anSI92 SQL.\*\*\*</span><span class="sxs-lookup"><span data-stu-id="a113e-125">Support ANSI92 SQL.\*\*\*</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="a113e-126">X</span><span class="sxs-lookup"><span data-stu-id="a113e-126">X</span></span></p></td>
<td><p><span data-ttu-id="a113e-127">X</span><span class="sxs-lookup"><span data-stu-id="a113e-127">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a113e-128">Создание таблиц.</span><span class="sxs-lookup"><span data-stu-id="a113e-128">Create tables.</span></span></p></td>
<td><p><span data-ttu-id="a113e-129">X</span><span class="sxs-lookup"><span data-stu-id="a113e-129">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="a113e-130">X</span><span class="sxs-lookup"><span data-stu-id="a113e-130">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a113e-131">Создайте новую базу данных.</span><span class="sxs-lookup"><span data-stu-id="a113e-131">Create new database.</span></span></p></td>
<td><p><span data-ttu-id="a113e-132">X</span><span class="sxs-lookup"><span data-stu-id="a113e-132">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="a113e-133">X\*</span><span class="sxs-lookup"><span data-stu-id="a113e-133">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a113e-134">Изменение существующих свойств таблицы.</span><span class="sxs-lookup"><span data-stu-id="a113e-134">Edit existing table properties.</span></span></p></td>
<td><p><span data-ttu-id="a113e-135">X</span><span class="sxs-lookup"><span data-stu-id="a113e-135">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="a113e-136">X</span><span class="sxs-lookup"><span data-stu-id="a113e-136">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a113e-137">Создание связей таблиц.</span><span class="sxs-lookup"><span data-stu-id="a113e-137">Create table relationships.</span></span></p></td>
<td><p><span data-ttu-id="a113e-138">X</span><span class="sxs-lookup"><span data-stu-id="a113e-138">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="a113e-139">X\*</span><span class="sxs-lookup"><span data-stu-id="a113e-139">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a113e-140">Изменение параметров безопасности.</span><span class="sxs-lookup"><span data-stu-id="a113e-140">Edit security settings.</span></span></p></td>
<td><p><span data-ttu-id="a113e-141">X</span><span class="sxs-lookup"><span data-stu-id="a113e-141">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="a113e-142">X\*</span><span class="sxs-lookup"><span data-stu-id="a113e-142">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a113e-143">Поддержка атрибута сжатия для данных столбцов.</span><span class="sxs-lookup"><span data-stu-id="a113e-143">Support for Compression attribute for column data.</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="a113e-144">X</span><span class="sxs-lookup"><span data-stu-id="a113e-144">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a113e-145">Изменение сохраненных, базовых SQL запросов или представлений.</span><span class="sxs-lookup"><span data-stu-id="a113e-145">Edit stored, basic SQL queries or views.</span></span></p></td>
<td><p><span data-ttu-id="a113e-146">X</span><span class="sxs-lookup"><span data-stu-id="a113e-146">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="a113e-147">X\*</span><span class="sxs-lookup"><span data-stu-id="a113e-147">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a113e-148">Создавать постоянные запросы, доступные только через код.</span><span class="sxs-lookup"><span data-stu-id="a113e-148">Create permanent queries that are accessible only through code.</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="a113e-149">X\*</span><span class="sxs-lookup"><span data-stu-id="a113e-149">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a113e-150">Создавайте запросы, доступные через контейнер базы данных, пользовательский интерфейс и код.</span><span class="sxs-lookup"><span data-stu-id="a113e-150">Create queries accessible through database container/UI and code.</span></span></p></td>
<td><p><span data-ttu-id="a113e-151">X</span><span class="sxs-lookup"><span data-stu-id="a113e-151">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a113e-152">Компактная или кодированная база данных.</span><span class="sxs-lookup"><span data-stu-id="a113e-152">Compact/encode database.</span></span></p></td>
<td><p><span data-ttu-id="a113e-153">X</span><span class="sxs-lookup"><span data-stu-id="a113e-153">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="a113e-154">X4</span><span class="sxs-lookup"><span data-stu-id="a113e-154">X4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a113e-155">Кэш обновления.</span><span class="sxs-lookup"><span data-stu-id="a113e-155">Refresh cache.</span></span></p></td>
<td><p><span data-ttu-id="a113e-156">X</span><span class="sxs-lookup"><span data-stu-id="a113e-156">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="a113e-157">X</span><span class="sxs-lookup"><span data-stu-id="a113e-157">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a113e-158">Сделайте базу данных реплицируемым.</span><span class="sxs-lookup"><span data-stu-id="a113e-158">Make database replicable.</span></span></p></td>
<td><p><span data-ttu-id="a113e-159">X</span><span class="sxs-lookup"><span data-stu-id="a113e-159">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="a113e-160">X3</span><span class="sxs-lookup"><span data-stu-id="a113e-160">X3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a113e-161">Сделайте реплики базы данных.</span><span class="sxs-lookup"><span data-stu-id="a113e-161">Make database replicas.</span></span></p></td>
<td><p><span data-ttu-id="a113e-162">X</span><span class="sxs-lookup"><span data-stu-id="a113e-162">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="a113e-163">X3</span><span class="sxs-lookup"><span data-stu-id="a113e-163">X3</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a113e-164">Синхронизировать реплики.</span><span class="sxs-lookup"><span data-stu-id="a113e-164">Synchronize replicas.</span></span></p></td>
<td><p><span data-ttu-id="a113e-165">X</span><span class="sxs-lookup"><span data-stu-id="a113e-165">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="a113e-166">X3</span><span class="sxs-lookup"><span data-stu-id="a113e-166">X3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a113e-167">Изменение свойств базы данных.</span><span class="sxs-lookup"><span data-stu-id="a113e-167">Edit database properties.</span></span></p></td>
<td><p><span data-ttu-id="a113e-168">X</span><span class="sxs-lookup"><span data-stu-id="a113e-168">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a113e-169">Создание настраиваемой базы данных.</span><span class="sxs-lookup"><span data-stu-id="a113e-169">Create custom database properties.</span></span></p></td>
<td><p><span data-ttu-id="a113e-170">X</span><span class="sxs-lookup"><span data-stu-id="a113e-170">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a113e-171">Изменение свойств столбца таблицы.</span><span class="sxs-lookup"><span data-stu-id="a113e-171">Edit table column properties.</span></span></p></td>
<td><p><span data-ttu-id="a113e-172">X</span><span class="sxs-lookup"><span data-stu-id="a113e-172">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a113e-173">\* Доступно только при работе с базами данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="a113e-173">\* Only available when working with Microsoft Access databases.</span></span> <span data-ttu-id="a113e-174">Будущие версии поставщика SQL могут предоставлять эту функциональность в проектах Microsoft Access (ADP).</span><span class="sxs-lookup"><span data-stu-id="a113e-174">Future versions of the SQL Provider may provide this functionality in Microsoft Access projects (.adp).</span></span>

<span data-ttu-id="a113e-175">\*\* Доступно только при работе с проектами Access.</span><span class="sxs-lookup"><span data-stu-id="a113e-175">\*\* Only available when working with Access projects.</span></span>

<span data-ttu-id="a113e-176">\*\*\* Хотя механизм баз данных Access поддерживает некоторые SQL ANSI 92, он еще не полностью совместим с ANSI92.</span><span class="sxs-lookup"><span data-stu-id="a113e-176">\*\*\* Although the Access database engine does support some ANSI 92 SQL, it is not yet fully ANSI92-compliant.</span></span>

<span data-ttu-id="a113e-177">1 Использует **объект Connection** для ссылки на базу данных.</span><span class="sxs-lookup"><span data-stu-id="a113e-177">1 Uses **Connection** object to reference database.</span></span>

<span data-ttu-id="a113e-178">2 Использует объект **Catalog** для ссылки на базу данных.</span><span class="sxs-lookup"><span data-stu-id="a113e-178">2 Uses **Catalog** object to reference database.</span></span>

<span data-ttu-id="a113e-179">3 Использует **объект Replica** для ссылки на базу данных.</span><span class="sxs-lookup"><span data-stu-id="a113e-179">3 Uses **Replica** object to reference database.</span></span>

<span data-ttu-id="a113e-180">4 Использует объект **JetEngine** для ссылки на базу данных.</span><span class="sxs-lookup"><span data-stu-id="a113e-180">4 Uses **JetEngine** object to reference database.</span></span>


> [!NOTE]
> <span data-ttu-id="a113e-181">В отличие от DAO, объекты ADO и ADOX могут выполнять помеченные действия в базах данных, кроме Jet, если поставщик этих баз данных поддерживает это действие.</span><span class="sxs-lookup"><span data-stu-id="a113e-181">Unlike DAO, ADO and ADOX objects can perform the marked actions in databases other than Jet as long as the provider for those databases supports that action.</span></span>


