---
title: Using ActiveX Data Objects
TOCTitle: Using ActiveX Data Objects
ms:assetid: 64055c45-7a27-2296-468a-015362898329
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194969(v=office.15)
ms:contentKeyID: 48545279
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5285627
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 1f7c57ca785e115e9278145921bf50e8afe870ab
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480896"
---
# <a name="using-activex-data-objects"></a><span data-ttu-id="d8ee1-102">Using ActiveX Data Objects</span><span class="sxs-lookup"><span data-stu-id="d8ee1-102">Using ActiveX Data Objects</span></span>


<span data-ttu-id="d8ee1-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d8ee1-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d8ee1-104">Microsoft Access предоставляет три объектных моделей для использования в создании, поддержке и управлению баз данных Access и их данных, связанных с ними с помощью Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="d8ee1-104">Microsoft Access provides three object models to use in the creation, maintaining and managing of your Access databases and their related data by using Visual Basic.</span></span>

## <a name="microsoft-activex-data-objects-ado"></a><span data-ttu-id="d8ee1-105">Microsoft ActiveX Data Objects (ADO)</span><span class="sxs-lookup"><span data-stu-id="d8ee1-105">Microsoft ActiveX Data Objects (ADO)</span></span>

<span data-ttu-id="d8ee1-106">ADO содержит объекты, необходимые для создания, обслуживания и удаления записей в заданном источнике данных.</span><span class="sxs-lookup"><span data-stu-id="d8ee1-106">ADO contains the objects needed to create, maintain, and delete records in a given datasource.</span></span>

## <a name="microsoft-ado-ext-for-ddl-and-security-adox"></a><span data-ttu-id="d8ee1-107">Внешний Microsoft ADO для DDL и безопасности (ADOX)</span><span class="sxs-lookup"><span data-stu-id="d8ee1-107">Microsoft ADO Ext. for DDL and Security (ADOX)</span></span>

<span data-ttu-id="d8ee1-108">ADOX предоставляет Language(DDL) определения данных объекты, необходимые для создания новой базы данных и ее вложенные объекты, помимо объекты, необходимые для управления безопасностью.</span><span class="sxs-lookup"><span data-stu-id="d8ee1-108">ADOX provides the Data Definition Language(DDL) objects needed to create a new database and its contained objects in addition to the objects needed to manage security.</span></span>

<span data-ttu-id="d8ee1-109">**Библиотека объектов 2.5 репликации (JRO) и Microsoft Jet**</span><span class="sxs-lookup"><span data-stu-id="d8ee1-109">**Microsoft Jet and Replication Objects 2.5 Library (JRO)**</span></span>

<span data-ttu-id="d8ee1-110">Поскольку объекты ADO были предназначена для работы с использованием многих баз данных, кроме баз данных Microsoft Jet, функциональные возможности, относящиеся к Jet был разбиваются на библиотеку JRO.</span><span class="sxs-lookup"><span data-stu-id="d8ee1-110">Since ADO objects were designed to work with many databases in addition to Microsoft Jet databases, functionality specific to Jet was broken out into the JRO library.</span></span>

<span data-ttu-id="d8ee1-111">В следующей таблице перечислены функциональные возможности, предоставляемые каждым по сравнению с DAO.</span><span class="sxs-lookup"><span data-stu-id="d8ee1-111">The following table lists the functionality provided by each compared to DAO.</span></span>

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
<th><p><span data-ttu-id="d8ee1-112">Функциональность</span><span class="sxs-lookup"><span data-stu-id="d8ee1-112">Functionality</span></span></p></th>
<th><p><span data-ttu-id="d8ee1-113">DAO</span><span class="sxs-lookup"><span data-stu-id="d8ee1-113">DAO</span></span></p></th>
<th><p><span data-ttu-id="d8ee1-114">ADO1</span><span class="sxs-lookup"><span data-stu-id="d8ee1-114">ADO1</span></span></p></th>
<th><p><span data-ttu-id="d8ee1-115">ADOX2</span><span class="sxs-lookup"><span data-stu-id="d8ee1-115">ADOX2</span></span></p></th>
<th><p><span data-ttu-id="d8ee1-116">JRO</span><span class="sxs-lookup"><span data-stu-id="d8ee1-116">JRO</span></span><br />
<span data-ttu-id="d8ee1-117">(Только 's MDB)</span><span class="sxs-lookup"><span data-stu-id="d8ee1-117">(MDB's Only)</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d8ee1-118">Создание наборов записей</span><span class="sxs-lookup"><span data-stu-id="d8ee1-118">Create Recordsets</span></span></p></td>
<td><p><span data-ttu-id="d8ee1-119">X </span><span class="sxs-lookup"><span data-stu-id="d8ee1-119">X</span></span></p></td>
<td><p><span data-ttu-id="d8ee1-120">X </span><span class="sxs-lookup"><span data-stu-id="d8ee1-120">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8ee1-121">Изменение параметров запуска</span><span class="sxs-lookup"><span data-stu-id="d8ee1-121">Edit Startup properties</span></span></p></td>
<td><p><span data-ttu-id="d8ee1-122">X </span><span class="sxs-lookup"><span data-stu-id="d8ee1-122">X</span></span></p></td>
<td><p><span data-ttu-id="d8ee1-123">X \*\*</span><span class="sxs-lookup"><span data-stu-id="d8ee1-123">X\*\*</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8ee1-124">Поддержка ANSI92 SQL \*\*\*</span><span class="sxs-lookup"><span data-stu-id="d8ee1-124">Support ANSI92 SQL\*\*\*</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="d8ee1-125">X </span><span class="sxs-lookup"><span data-stu-id="d8ee1-125">X</span></span></p></td>
<td><p><span data-ttu-id="d8ee1-126">X </span><span class="sxs-lookup"><span data-stu-id="d8ee1-126">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8ee1-127">Создание таблиц</span><span class="sxs-lookup"><span data-stu-id="d8ee1-127">Create Tables</span></span></p></td>
<td><p><span data-ttu-id="d8ee1-128">X </span><span class="sxs-lookup"><span data-stu-id="d8ee1-128">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="d8ee1-129">X </span><span class="sxs-lookup"><span data-stu-id="d8ee1-129">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8ee1-130">Создание новой базы данных</span><span class="sxs-lookup"><span data-stu-id="d8ee1-130">Create New Database</span></span></p></td>
<td><p><span data-ttu-id="d8ee1-131">X </span><span class="sxs-lookup"><span data-stu-id="d8ee1-131">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="d8ee1-132">X \*</span><span class="sxs-lookup"><span data-stu-id="d8ee1-132">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8ee1-133">Изменение свойств существующей таблицы</span><span class="sxs-lookup"><span data-stu-id="d8ee1-133">Edit Existing Table properties</span></span></p></td>
<td><p><span data-ttu-id="d8ee1-134">X </span><span class="sxs-lookup"><span data-stu-id="d8ee1-134">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="d8ee1-135">X </span><span class="sxs-lookup"><span data-stu-id="d8ee1-135">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8ee1-136">Создание связи между таблицами</span><span class="sxs-lookup"><span data-stu-id="d8ee1-136">Create table relationships</span></span></p></td>
<td><p><span data-ttu-id="d8ee1-137">X </span><span class="sxs-lookup"><span data-stu-id="d8ee1-137">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="d8ee1-138">X \*</span><span class="sxs-lookup"><span data-stu-id="d8ee1-138">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8ee1-139">Изменение параметров безопасности</span><span class="sxs-lookup"><span data-stu-id="d8ee1-139">Edit security settings</span></span></p></td>
<td><p><span data-ttu-id="d8ee1-140">X </span><span class="sxs-lookup"><span data-stu-id="d8ee1-140">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="d8ee1-141">X \*</span><span class="sxs-lookup"><span data-stu-id="d8ee1-141">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8ee1-142">Поддержка сжатия для столбцы данных.</span><span class="sxs-lookup"><span data-stu-id="d8ee1-142">Support for Compression attribute for column data</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="d8ee1-143">X </span><span class="sxs-lookup"><span data-stu-id="d8ee1-143">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8ee1-144">Изменение сохраненных, основных SQL-запросов или представлений</span><span class="sxs-lookup"><span data-stu-id="d8ee1-144">Edit stored, basic SQL queries or views</span></span></p></td>
<td><p><span data-ttu-id="d8ee1-145">X </span><span class="sxs-lookup"><span data-stu-id="d8ee1-145">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="d8ee1-146">X \*</span><span class="sxs-lookup"><span data-stu-id="d8ee1-146">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8ee1-147">Создайте постоянные запросов, которые доступны только с помощью кода.</span><span class="sxs-lookup"><span data-stu-id="d8ee1-147">Create permanent queries that are accessible only through code.</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="d8ee1-148">X \*</span><span class="sxs-lookup"><span data-stu-id="d8ee1-148">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8ee1-149">Создание запросов через контейнер базы данных и пользовательского интерфейса и кода.</span><span class="sxs-lookup"><span data-stu-id="d8ee1-149">Create queries accessible through database container/UI and code.</span></span></p></td>
<td><p><span data-ttu-id="d8ee1-150">X </span><span class="sxs-lookup"><span data-stu-id="d8ee1-150">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8ee1-151">Сжать/кодирование базы данных</span><span class="sxs-lookup"><span data-stu-id="d8ee1-151">Compact/Encode database</span></span></p></td>
<td><p><span data-ttu-id="d8ee1-152">X </span><span class="sxs-lookup"><span data-stu-id="d8ee1-152">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="d8ee1-153">X4</span><span class="sxs-lookup"><span data-stu-id="d8ee1-153">X4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8ee1-154">Обновление кэша</span><span class="sxs-lookup"><span data-stu-id="d8ee1-154">Refresh Cache</span></span></p></td>
<td><p><span data-ttu-id="d8ee1-155">X </span><span class="sxs-lookup"><span data-stu-id="d8ee1-155">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="d8ee1-156">X </span><span class="sxs-lookup"><span data-stu-id="d8ee1-156">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8ee1-157">Сделать реплицированной базы данных</span><span class="sxs-lookup"><span data-stu-id="d8ee1-157">Make Database Replicable</span></span></p></td>
<td><p><span data-ttu-id="d8ee1-158">X </span><span class="sxs-lookup"><span data-stu-id="d8ee1-158">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="d8ee1-159">X3</span><span class="sxs-lookup"><span data-stu-id="d8ee1-159">X3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8ee1-160">Сделать репликами баз данных</span><span class="sxs-lookup"><span data-stu-id="d8ee1-160">Make Database Replicas</span></span></p></td>
<td><p><span data-ttu-id="d8ee1-161">X </span><span class="sxs-lookup"><span data-stu-id="d8ee1-161">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="d8ee1-162">X3</span><span class="sxs-lookup"><span data-stu-id="d8ee1-162">X3</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8ee1-163">Синхронизации реплик</span><span class="sxs-lookup"><span data-stu-id="d8ee1-163">Synchronize Replicas</span></span></p></td>
<td><p><span data-ttu-id="d8ee1-164">X </span><span class="sxs-lookup"><span data-stu-id="d8ee1-164">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="d8ee1-165">X3</span><span class="sxs-lookup"><span data-stu-id="d8ee1-165">X3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8ee1-166">Изменение свойств базы данных</span><span class="sxs-lookup"><span data-stu-id="d8ee1-166">Edit Database properties</span></span></p></td>
<td><p><span data-ttu-id="d8ee1-167">X </span><span class="sxs-lookup"><span data-stu-id="d8ee1-167">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8ee1-168">Создание настраиваемой базы данных свойств</span><span class="sxs-lookup"><span data-stu-id="d8ee1-168">Create custom database properties</span></span></p></td>
<td><p><span data-ttu-id="d8ee1-169">X </span><span class="sxs-lookup"><span data-stu-id="d8ee1-169">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8ee1-170">Изменение свойств столбца в таблице</span><span class="sxs-lookup"><span data-stu-id="d8ee1-170">Edit table column properties</span></span></p></td>
<td><p><span data-ttu-id="d8ee1-171">X </span><span class="sxs-lookup"><span data-stu-id="d8ee1-171">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d8ee1-172">\*Доступно только при работе с базами данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="d8ee1-172">\* Only available when working with Microsoft Access databases.</span></span> <span data-ttu-id="d8ee1-173">В будущих версиях поставщика SQL можно указать эту функцию в проектах Microsoft Access (файлы с расширением ADP).</span><span class="sxs-lookup"><span data-stu-id="d8ee1-173">Future versions of the SQL Provider may provide this functionality in Microsoft Access projects (.adp).</span></span>

<span data-ttu-id="d8ee1-174">\*\*Доступно только при работе с проектами Access.</span><span class="sxs-lookup"><span data-stu-id="d8ee1-174">\*\* Only available when working with Access projects.</span></span>

<span data-ttu-id="d8ee1-175">\*\*\*Хотя ядро СУБД Access поддерживают некоторые ANSI SQL-92 его еще не является полностью ANSI92 спецификации.</span><span class="sxs-lookup"><span data-stu-id="d8ee1-175">\*\*\* Though the Access database engine does support some ANSI 92 SQL it is not yet fully ANSI92 compliant.</span></span>

<span data-ttu-id="d8ee1-176">Объект 1 использует **подключения** для обращения к базе данных</span><span class="sxs-lookup"><span data-stu-id="d8ee1-176">1 Uses **Connection** object to reference to database</span></span>

<span data-ttu-id="d8ee1-177">2 использует **каталога** объектов для базы данных ссылок</span><span class="sxs-lookup"><span data-stu-id="d8ee1-177">2 Uses **Catalog** object to reference database</span></span>

<span data-ttu-id="d8ee1-178">3 объект использует **реплики** для базы данных ссылок</span><span class="sxs-lookup"><span data-stu-id="d8ee1-178">3 Uses **Replica** object to reference database</span></span>

<span data-ttu-id="d8ee1-179">4 объекта использует **JetEngine** для базы данных ссылок</span><span class="sxs-lookup"><span data-stu-id="d8ee1-179">4 Uses **JetEngine** object to reference database</span></span>


> [!NOTE]
> <P><span data-ttu-id="d8ee1-180">В отличие от DAO ADO и ADOX объекты можно выполнить помеченные действия в базах данных других затем Jet до тех пор, пока поставщик для этих баз данных поддерживает это действие.</span><span class="sxs-lookup"><span data-stu-id="d8ee1-180">Unlike DAO, ADO and ADOX objects can perform the marked actions in databases other then Jet as long as the provider for those databases supports that action.</span></span></P>


