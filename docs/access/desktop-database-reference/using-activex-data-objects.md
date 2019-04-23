---
title: Использование объектов данных ActiveX
TOCTitle: Use ActiveX Data Objects
description: Microsoft Access предоставляет три объектные модели, которые используются для создания, обслуживания и управления базами данных Access и связанных с ними данных с помощью Visual Basic.
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
# <a name="use-activex-data-objects"></a><span data-ttu-id="69868-103">Использование объектов данных ActiveX</span><span class="sxs-lookup"><span data-stu-id="69868-103">Use ActiveX Data Objects</span></span>

<span data-ttu-id="69868-104">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="69868-104">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="69868-105">Microsoft Access предоставляет три объектные модели, которые используются для создания, обслуживания и управления базами данных Access и связанных с ними данных с помощью Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="69868-105">Microsoft Access provides three object models to use in the creation, maintaining, and managing of your Access databases and their related data by using Visual Basic.</span></span>

## <a name="microsoft-activex-data-objects-ado"></a><span data-ttu-id="69868-106">Объекты данных Microsoft ActiveX (ADO)</span><span class="sxs-lookup"><span data-stu-id="69868-106">Microsoft ActiveX Data Objects (ADO)</span></span>

<span data-ttu-id="69868-107">ADO содержит объекты, необходимые для создания, обслуживания и удаления записей в заданном источнике данных.</span><span class="sxs-lookup"><span data-stu-id="69868-107">ADO contains the objects needed to create, maintain, and delete records in a given datasource.</span></span>

## <a name="microsoft-ado-ext-for-ddl-and-security-adox"></a><span data-ttu-id="69868-108">Microsoft ADO ext. для DDL и безопасности (ADOX)</span><span class="sxs-lookup"><span data-stu-id="69868-108">Microsoft ADO ext. for DDL and security (ADOX)</span></span>

<span data-ttu-id="69868-109">ADOX предоставляет объекты языка определения данных (DDL), необходимые для создания новой базы данных и ее вложенных объектов в дополнение к объектам, необходимым для управления безопасностью.</span><span class="sxs-lookup"><span data-stu-id="69868-109">ADOX provides the Data Definition Language (DDL) objects needed to create a new database and its contained objects in addition to the objects needed to manage security.</span></span>

### <a name="microsoft-jet-and-replication-objects-25-library-jro"></a><span data-ttu-id="69868-110">Microsoft Jet и библиотека объектов репликации 2,5 (JRO)</span><span class="sxs-lookup"><span data-stu-id="69868-110">Microsoft Jet and Replication Objects 2.5 library (JRO)</span></span>

<span data-ttu-id="69868-111">Так как объекты ADO спроектированы для работы с множеством баз данных в дополнение к базам данных Microsoft Jet, функции, относящиеся к Jet, были разбиты на библиотеку JRO.</span><span class="sxs-lookup"><span data-stu-id="69868-111">Because ADO objects were designed to work with many databases in addition to Microsoft Jet databases, functionality specific to Jet was broken out into the JRO library.</span></span>

<span data-ttu-id="69868-112">В следующей таблице перечислены функциональные возможности, предоставляемые в сравнении с DAO.</span><span class="sxs-lookup"><span data-stu-id="69868-112">The following table lists the functionality provided by each compared to DAO.</span></span>

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
<th><p><span data-ttu-id="69868-113">Функция</span><span class="sxs-lookup"><span data-stu-id="69868-113">Functionality</span></span></p></th>
<th><p><span data-ttu-id="69868-114">ПРОГРАММИРОВАН</span><span class="sxs-lookup"><span data-stu-id="69868-114">DAO</span></span></p></th>
<th><p><span data-ttu-id="69868-115">ADO1</span><span class="sxs-lookup"><span data-stu-id="69868-115">ADO1</span></span></p></th>
<th><p><span data-ttu-id="69868-116">ADOX2</span><span class="sxs-lookup"><span data-stu-id="69868-116">ADOX2</span></span></p></th>
<th><p><span data-ttu-id="69868-117">JRO</span><span class="sxs-lookup"><span data-stu-id="69868-117">JRO</span></span><br />
<span data-ttu-id="69868-118">(Только для МДБС)</span><span class="sxs-lookup"><span data-stu-id="69868-118">(MDBs only)</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="69868-119">Создание наборов записей.</span><span class="sxs-lookup"><span data-stu-id="69868-119">Create Recordsets.</span></span></p></td>
<td><p><span data-ttu-id="69868-120">X</span><span class="sxs-lookup"><span data-stu-id="69868-120">X</span></span></p></td>
<td><p><span data-ttu-id="69868-121">X</span><span class="sxs-lookup"><span data-stu-id="69868-121">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69868-122">Изменение свойств запуска.</span><span class="sxs-lookup"><span data-stu-id="69868-122">Edit Startup properties.</span></span></p></td>
<td><p><span data-ttu-id="69868-123">X</span><span class="sxs-lookup"><span data-stu-id="69868-123">X</span></span></p></td>
<td><p><span data-ttu-id="69868-124">X \* \*</span><span class="sxs-lookup"><span data-stu-id="69868-124">X\*\*</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69868-125">Поддержка ANSI92 SQL. \* \* \*</span><span class="sxs-lookup"><span data-stu-id="69868-125">Support ANSI92 SQL.\*\*\*</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="69868-126">X</span><span class="sxs-lookup"><span data-stu-id="69868-126">X</span></span></p></td>
<td><p><span data-ttu-id="69868-127">X</span><span class="sxs-lookup"><span data-stu-id="69868-127">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69868-128">Создание таблиц.</span><span class="sxs-lookup"><span data-stu-id="69868-128">Create tables.</span></span></p></td>
<td><p><span data-ttu-id="69868-129">X</span><span class="sxs-lookup"><span data-stu-id="69868-129">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="69868-130">X</span><span class="sxs-lookup"><span data-stu-id="69868-130">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69868-131">Создание новой базы данных.</span><span class="sxs-lookup"><span data-stu-id="69868-131">Create new database.</span></span></p></td>
<td><p><span data-ttu-id="69868-132">X</span><span class="sxs-lookup"><span data-stu-id="69868-132">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="69868-133">X</span><span class="sxs-lookup"><span data-stu-id="69868-133">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69868-134">Изменение свойств существующей таблицы.</span><span class="sxs-lookup"><span data-stu-id="69868-134">Edit existing table properties.</span></span></p></td>
<td><p><span data-ttu-id="69868-135">X</span><span class="sxs-lookup"><span data-stu-id="69868-135">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="69868-136">X</span><span class="sxs-lookup"><span data-stu-id="69868-136">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69868-137">Создайте связи между таблицами.</span><span class="sxs-lookup"><span data-stu-id="69868-137">Create table relationships.</span></span></p></td>
<td><p><span data-ttu-id="69868-138">X</span><span class="sxs-lookup"><span data-stu-id="69868-138">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="69868-139">X</span><span class="sxs-lookup"><span data-stu-id="69868-139">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69868-140">Изменение параметров безопасности.</span><span class="sxs-lookup"><span data-stu-id="69868-140">Edit security settings.</span></span></p></td>
<td><p><span data-ttu-id="69868-141">X</span><span class="sxs-lookup"><span data-stu-id="69868-141">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="69868-142">X</span><span class="sxs-lookup"><span data-stu-id="69868-142">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69868-143">Поддержка атрибута Compression для данных столбца.</span><span class="sxs-lookup"><span data-stu-id="69868-143">Support for Compression attribute for column data.</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="69868-144">X</span><span class="sxs-lookup"><span data-stu-id="69868-144">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69868-145">Изменение хранимых, базовых запросов или представлений SQL.</span><span class="sxs-lookup"><span data-stu-id="69868-145">Edit stored, basic SQL queries or views.</span></span></p></td>
<td><p><span data-ttu-id="69868-146">X</span><span class="sxs-lookup"><span data-stu-id="69868-146">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="69868-147">X</span><span class="sxs-lookup"><span data-stu-id="69868-147">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69868-148">Создание постоянных запросов, доступных только с помощью кода.</span><span class="sxs-lookup"><span data-stu-id="69868-148">Create permanent queries that are accessible only through code.</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="69868-149">X</span><span class="sxs-lookup"><span data-stu-id="69868-149">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69868-150">Создание запросов, доступ к которым осуществляется с помощью контейнера базы данных, ПОЛЬЗОВАТЕЛЬСКОГО интерфейса и кода.</span><span class="sxs-lookup"><span data-stu-id="69868-150">Create queries accessible through database container/UI and code.</span></span></p></td>
<td><p><span data-ttu-id="69868-151">X</span><span class="sxs-lookup"><span data-stu-id="69868-151">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69868-152">Сжатие и кодирование базы данных.</span><span class="sxs-lookup"><span data-stu-id="69868-152">Compact/encode database.</span></span></p></td>
<td><p><span data-ttu-id="69868-153">X</span><span class="sxs-lookup"><span data-stu-id="69868-153">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="69868-154">X4</span><span class="sxs-lookup"><span data-stu-id="69868-154">X4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69868-155">Обновление кэша.</span><span class="sxs-lookup"><span data-stu-id="69868-155">Refresh cache.</span></span></p></td>
<td><p><span data-ttu-id="69868-156">X</span><span class="sxs-lookup"><span data-stu-id="69868-156">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="69868-157">X</span><span class="sxs-lookup"><span data-stu-id="69868-157">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69868-158">Сделайте базу данных реплицируемой.</span><span class="sxs-lookup"><span data-stu-id="69868-158">Make database replicable.</span></span></p></td>
<td><p><span data-ttu-id="69868-159">X</span><span class="sxs-lookup"><span data-stu-id="69868-159">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="69868-160">Lingvo</span><span class="sxs-lookup"><span data-stu-id="69868-160">X3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69868-161">Сделайте реплики базы данных.</span><span class="sxs-lookup"><span data-stu-id="69868-161">Make database replicas.</span></span></p></td>
<td><p><span data-ttu-id="69868-162">X</span><span class="sxs-lookup"><span data-stu-id="69868-162">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="69868-163">Lingvo</span><span class="sxs-lookup"><span data-stu-id="69868-163">X3</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69868-164">Синхронизация реплик.</span><span class="sxs-lookup"><span data-stu-id="69868-164">Synchronize replicas.</span></span></p></td>
<td><p><span data-ttu-id="69868-165">X</span><span class="sxs-lookup"><span data-stu-id="69868-165">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="69868-166">Lingvo</span><span class="sxs-lookup"><span data-stu-id="69868-166">X3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69868-167">Изменение свойств базы данных.</span><span class="sxs-lookup"><span data-stu-id="69868-167">Edit database properties.</span></span></p></td>
<td><p><span data-ttu-id="69868-168">X</span><span class="sxs-lookup"><span data-stu-id="69868-168">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69868-169">Создание настраиваемых свойств базы данных.</span><span class="sxs-lookup"><span data-stu-id="69868-169">Create custom database properties.</span></span></p></td>
<td><p><span data-ttu-id="69868-170">X</span><span class="sxs-lookup"><span data-stu-id="69868-170">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69868-171">Изменение свойств столбца таблицы.</span><span class="sxs-lookup"><span data-stu-id="69868-171">Edit table column properties.</span></span></p></td>
<td><p><span data-ttu-id="69868-172">X</span><span class="sxs-lookup"><span data-stu-id="69868-172">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="69868-173">\*Доступно только при работе с базами данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="69868-173">\* Only available when working with Microsoft Access databases.</span></span> <span data-ttu-id="69868-174">В будущих версиях поставщика SQL эта функция может быть предоставлена в проектах Microsoft Access (ADP).</span><span class="sxs-lookup"><span data-stu-id="69868-174">Future versions of the SQL Provider may provide this functionality in Microsoft Access projects (.adp).</span></span>

<span data-ttu-id="69868-175">\*\*Доступно только при работе с проектами Access.</span><span class="sxs-lookup"><span data-stu-id="69868-175">\*\* Only available when working with Access projects.</span></span>

<span data-ttu-id="69868-176">\*\*\*Несмотря на то, что ядро базы данных Access поддерживает некоторый ANSI 92 SQL, он пока не полностью совместим с ANSI92.</span><span class="sxs-lookup"><span data-stu-id="69868-176">\*\*\* Although the Access database engine does support some ANSI 92 SQL, it is not yet fully ANSI92-compliant.</span></span>

<span data-ttu-id="69868-177">1 использует объект **Connection** для ссылки на базу данных.</span><span class="sxs-lookup"><span data-stu-id="69868-177">1 Uses **Connection** object to reference database.</span></span>

<span data-ttu-id="69868-178">2 использует объект **каталога** для ссылки на базу данных.</span><span class="sxs-lookup"><span data-stu-id="69868-178">2 Uses **Catalog** object to reference database.</span></span>

<span data-ttu-id="69868-179">3 использует \*\*\*\* объект реплики для ссылки на базу данных.</span><span class="sxs-lookup"><span data-stu-id="69868-179">3 Uses **Replica** object to reference database.</span></span>

<span data-ttu-id="69868-180">4 использует объект **жетенгине** для ссылки на базу данных.</span><span class="sxs-lookup"><span data-stu-id="69868-180">4 Uses **JetEngine** object to reference database.</span></span>


> [!NOTE]
> <span data-ttu-id="69868-181">В отличие от DAO, объекты ADO и ADOX могут выполнять помеченные действия в базах данных, отличных от Jet, если поставщик этих баз данных поддерживает это действие.</span><span class="sxs-lookup"><span data-stu-id="69868-181">Unlike DAO, ADO and ADOX objects can perform the marked actions in databases other than Jet as long as the provider for those databases supports that action.</span></span>


