---
title: Используйте объекты данных ActiveX
TOCTitle: Use ActiveX Data Objects
description: Microsoft Access предоставляет три объектных моделей для использования в создании, обслуживания и управления баз данных Access и их данных, связанных с использованием Visual Basic.
ms:assetid: 64055c45-7a27-2296-468a-015362898329
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194969(v=office.15)
ms:contentKeyID: 48545279
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5285627
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d7e8e7e6abeea9cca86c928760eddb990517a207
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887511"
---
# <a name="use-activex-data-objects"></a><span data-ttu-id="17ba9-103">Используйте объекты данных ActiveX</span><span class="sxs-lookup"><span data-stu-id="17ba9-103">Use ActiveX Data Objects</span></span>

<span data-ttu-id="17ba9-104">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="17ba9-104">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="17ba9-105">Microsoft Access предоставляет три объектных моделей для использования в создании, обслуживания и управления баз данных Access и их данных, связанных с использованием Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="17ba9-105">Microsoft Access provides three object models to use in the creation, maintaining, and managing of your Access databases and their related data by using Visual Basic.</span></span>

## <a name="microsoft-activex-data-objects-ado"></a><span data-ttu-id="17ba9-106">Microsoft ActiveX Data Objects (ADO)</span><span class="sxs-lookup"><span data-stu-id="17ba9-106">Microsoft ActiveX Data Objects (ADO)</span></span>

<span data-ttu-id="17ba9-107">ADO содержит объекты, необходимые для создания, обслуживания и удаления записей в заданном источнике данных.</span><span class="sxs-lookup"><span data-stu-id="17ba9-107">ADO contains the objects needed to create, maintain, and delete records in a given datasource.</span></span>

## <a name="microsoft-ado-ext-for-ddl-and-security-adox"></a><span data-ttu-id="17ba9-108">Внешний Microsoft ADO для DDL и безопасности (ADOX)</span><span class="sxs-lookup"><span data-stu-id="17ba9-108">Microsoft ADO ext. for DDL and security (ADOX)</span></span>

<span data-ttu-id="17ba9-109">ADOX предоставляет язык описания данных (DDL) объекты, необходимые для создания новой базы данных и ее вложенные объекты, помимо объекты, необходимые для управления безопасностью.</span><span class="sxs-lookup"><span data-stu-id="17ba9-109">ADOX provides the Data Definition Language (DDL) objects needed to create a new database and its contained objects in addition to the objects needed to manage security.</span></span>

### <a name="microsoft-jet-and-replication-objects-25-library-jro"></a><span data-ttu-id="17ba9-110">Библиотека Microsoft Jet и репликации объектов 2.5 (JRO)</span><span class="sxs-lookup"><span data-stu-id="17ba9-110">Microsoft Jet and Replication Objects 2.5 library (JRO)</span></span>

<span data-ttu-id="17ba9-111">Так как объекты ADO были предназначена для работы с использованием многих баз данных, кроме баз данных Microsoft Jet, функциональные возможности, относящиеся к Jet был разбиваются на библиотеку JRO.</span><span class="sxs-lookup"><span data-stu-id="17ba9-111">Because ADO objects were designed to work with many databases in addition to Microsoft Jet databases, functionality specific to Jet was broken out into the JRO library.</span></span>

<span data-ttu-id="17ba9-112">В следующей таблице перечислены функциональные возможности, предоставляемые каждым по сравнению с DAO.</span><span class="sxs-lookup"><span data-stu-id="17ba9-112">The following table lists the functionality provided by each compared to DAO.</span></span>

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
<th><p><span data-ttu-id="17ba9-113">Функциональность</span><span class="sxs-lookup"><span data-stu-id="17ba9-113">Functionality</span></span></p></th>
<th><p><span data-ttu-id="17ba9-114">DAO</span><span class="sxs-lookup"><span data-stu-id="17ba9-114">DAO</span></span></p></th>
<th><p><span data-ttu-id="17ba9-115">ADO1</span><span class="sxs-lookup"><span data-stu-id="17ba9-115">ADO1</span></span></p></th>
<th><p><span data-ttu-id="17ba9-116">ADOX2</span><span class="sxs-lookup"><span data-stu-id="17ba9-116">ADOX2</span></span></p></th>
<th><p><span data-ttu-id="17ba9-117">JRO</span><span class="sxs-lookup"><span data-stu-id="17ba9-117">JRO</span></span><br />
<span data-ttu-id="17ba9-118">(MDB)</span><span class="sxs-lookup"><span data-stu-id="17ba9-118">(MDBs only)</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="17ba9-119">Создание наборов записей.</span><span class="sxs-lookup"><span data-stu-id="17ba9-119">Create Recordsets.</span></span></p></td>
<td><p><span data-ttu-id="17ba9-120">X </span><span class="sxs-lookup"><span data-stu-id="17ba9-120">X</span></span></p></td>
<td><p><span data-ttu-id="17ba9-121">X </span><span class="sxs-lookup"><span data-stu-id="17ba9-121">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17ba9-122">Изменение параметров запуска.</span><span class="sxs-lookup"><span data-stu-id="17ba9-122">Edit Startup properties.</span></span></p></td>
<td><p><span data-ttu-id="17ba9-123">X </span><span class="sxs-lookup"><span data-stu-id="17ba9-123">X</span></span></p></td>
<td><p><span data-ttu-id="17ba9-124">X \*\*</span><span class="sxs-lookup"><span data-stu-id="17ba9-124">X\*\*</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17ba9-125">Поддержка ANSI92 SQL.\* \*\*</span><span class="sxs-lookup"><span data-stu-id="17ba9-125">Support ANSI92 SQL.\*\*\*</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="17ba9-126">X </span><span class="sxs-lookup"><span data-stu-id="17ba9-126">X</span></span></p></td>
<td><p><span data-ttu-id="17ba9-127">X </span><span class="sxs-lookup"><span data-stu-id="17ba9-127">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17ba9-128">Создание таблиц.</span><span class="sxs-lookup"><span data-stu-id="17ba9-128">Create tables.</span></span></p></td>
<td><p><span data-ttu-id="17ba9-129">X </span><span class="sxs-lookup"><span data-stu-id="17ba9-129">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="17ba9-130">X </span><span class="sxs-lookup"><span data-stu-id="17ba9-130">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17ba9-131">Создание новой базы данных.</span><span class="sxs-lookup"><span data-stu-id="17ba9-131">Create new database.</span></span></p></td>
<td><p><span data-ttu-id="17ba9-132">X </span><span class="sxs-lookup"><span data-stu-id="17ba9-132">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="17ba9-133">X \*</span><span class="sxs-lookup"><span data-stu-id="17ba9-133">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17ba9-134">Изменение свойств существующей таблицы.</span><span class="sxs-lookup"><span data-stu-id="17ba9-134">Edit existing table properties.</span></span></p></td>
<td><p><span data-ttu-id="17ba9-135">X </span><span class="sxs-lookup"><span data-stu-id="17ba9-135">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="17ba9-136">X </span><span class="sxs-lookup"><span data-stu-id="17ba9-136">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17ba9-137">Создание связи между таблицами.</span><span class="sxs-lookup"><span data-stu-id="17ba9-137">Create table relationships.</span></span></p></td>
<td><p><span data-ttu-id="17ba9-138">X </span><span class="sxs-lookup"><span data-stu-id="17ba9-138">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="17ba9-139">X \*</span><span class="sxs-lookup"><span data-stu-id="17ba9-139">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17ba9-140">Изменение параметров безопасности.</span><span class="sxs-lookup"><span data-stu-id="17ba9-140">Edit security settings.</span></span></p></td>
<td><p><span data-ttu-id="17ba9-141">X </span><span class="sxs-lookup"><span data-stu-id="17ba9-141">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="17ba9-142">X \*</span><span class="sxs-lookup"><span data-stu-id="17ba9-142">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17ba9-143">Поддержка сжатия для столбца данных.</span><span class="sxs-lookup"><span data-stu-id="17ba9-143">Support for Compression attribute for column data.</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="17ba9-144">X </span><span class="sxs-lookup"><span data-stu-id="17ba9-144">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17ba9-145">Измените хранимые, основные запросы SQL или представления.</span><span class="sxs-lookup"><span data-stu-id="17ba9-145">Edit stored, basic SQL queries or views.</span></span></p></td>
<td><p><span data-ttu-id="17ba9-146">X </span><span class="sxs-lookup"><span data-stu-id="17ba9-146">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="17ba9-147">X \*</span><span class="sxs-lookup"><span data-stu-id="17ba9-147">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17ba9-148">Создайте постоянные запросов, которые доступны только с помощью кода.</span><span class="sxs-lookup"><span data-stu-id="17ba9-148">Create permanent queries that are accessible only through code.</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="17ba9-149">X \*</span><span class="sxs-lookup"><span data-stu-id="17ba9-149">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17ba9-150">Создание запросов через контейнер базы данных и пользовательского интерфейса и кода.</span><span class="sxs-lookup"><span data-stu-id="17ba9-150">Create queries accessible through database container/UI and code.</span></span></p></td>
<td><p><span data-ttu-id="17ba9-151">X </span><span class="sxs-lookup"><span data-stu-id="17ba9-151">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17ba9-152">Сжать/шифрование базы данных.</span><span class="sxs-lookup"><span data-stu-id="17ba9-152">Compact/encode database.</span></span></p></td>
<td><p><span data-ttu-id="17ba9-153">X </span><span class="sxs-lookup"><span data-stu-id="17ba9-153">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="17ba9-154">X4</span><span class="sxs-lookup"><span data-stu-id="17ba9-154">X4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17ba9-155">Обновление кэша.</span><span class="sxs-lookup"><span data-stu-id="17ba9-155">Refresh cache.</span></span></p></td>
<td><p><span data-ttu-id="17ba9-156">X </span><span class="sxs-lookup"><span data-stu-id="17ba9-156">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="17ba9-157">X </span><span class="sxs-lookup"><span data-stu-id="17ba9-157">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17ba9-158">Сделать реплицированной базы данных.</span><span class="sxs-lookup"><span data-stu-id="17ba9-158">Make database replicable.</span></span></p></td>
<td><p><span data-ttu-id="17ba9-159">X </span><span class="sxs-lookup"><span data-stu-id="17ba9-159">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="17ba9-160">X3</span><span class="sxs-lookup"><span data-stu-id="17ba9-160">X3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17ba9-161">Сделайте репликами баз данных.</span><span class="sxs-lookup"><span data-stu-id="17ba9-161">Make database replicas.</span></span></p></td>
<td><p><span data-ttu-id="17ba9-162">X </span><span class="sxs-lookup"><span data-stu-id="17ba9-162">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="17ba9-163">X3</span><span class="sxs-lookup"><span data-stu-id="17ba9-163">X3</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17ba9-164">Синхронизации реплик.</span><span class="sxs-lookup"><span data-stu-id="17ba9-164">Synchronize replicas.</span></span></p></td>
<td><p><span data-ttu-id="17ba9-165">X </span><span class="sxs-lookup"><span data-stu-id="17ba9-165">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="17ba9-166">X3</span><span class="sxs-lookup"><span data-stu-id="17ba9-166">X3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17ba9-167">Изменение свойств базы данных.</span><span class="sxs-lookup"><span data-stu-id="17ba9-167">Edit database properties.</span></span></p></td>
<td><p><span data-ttu-id="17ba9-168">X </span><span class="sxs-lookup"><span data-stu-id="17ba9-168">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17ba9-169">Создание настраиваемой базы данных свойств.</span><span class="sxs-lookup"><span data-stu-id="17ba9-169">Create custom database properties.</span></span></p></td>
<td><p><span data-ttu-id="17ba9-170">X </span><span class="sxs-lookup"><span data-stu-id="17ba9-170">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17ba9-171">Изменение свойств столбца в таблице.</span><span class="sxs-lookup"><span data-stu-id="17ba9-171">Edit table column properties.</span></span></p></td>
<td><p><span data-ttu-id="17ba9-172">X </span><span class="sxs-lookup"><span data-stu-id="17ba9-172">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="17ba9-173">\*Доступно только при работе с базами данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="17ba9-173">\* Only available when working with Microsoft Access databases.</span></span> <span data-ttu-id="17ba9-174">В будущих версиях поставщика SQL можно указать эту функцию в проектах Microsoft Access (файлы с расширением ADP).</span><span class="sxs-lookup"><span data-stu-id="17ba9-174">Future versions of the SQL Provider may provide this functionality in Microsoft Access projects (.adp).</span></span>

<span data-ttu-id="17ba9-175">\*\*Доступно только при работе с проектами Access.</span><span class="sxs-lookup"><span data-stu-id="17ba9-175">\*\* Only available when working with Access projects.</span></span>

<span data-ttu-id="17ba9-176">\*\*\*Несмотря на то, что ядро СУБД Access поддерживают некоторые ANSI SQL-92, она еще не полностью спецификации ANSI92.</span><span class="sxs-lookup"><span data-stu-id="17ba9-176">\*\*\* Although the Access database engine does support some ANSI 92 SQL, it is not yet fully ANSI92-compliant.</span></span>

<span data-ttu-id="17ba9-177">1 объект использует **подключение** к базе данных ссылок.</span><span class="sxs-lookup"><span data-stu-id="17ba9-177">1 Uses **Connection** object to reference database.</span></span>

<span data-ttu-id="17ba9-178">Объект 2 использует **каталога** для базы данных ссылок.</span><span class="sxs-lookup"><span data-stu-id="17ba9-178">2 Uses **Catalog** object to reference database.</span></span>

<span data-ttu-id="17ba9-179">3 объект использует **реплику** базы данных ссылок.</span><span class="sxs-lookup"><span data-stu-id="17ba9-179">3 Uses **Replica** object to reference database.</span></span>

<span data-ttu-id="17ba9-180">4 использует **JetEngine** объект базы данных ссылок.</span><span class="sxs-lookup"><span data-stu-id="17ba9-180">4 Uses **JetEngine** object to reference database.</span></span>


> [!NOTE]
> <span data-ttu-id="17ba9-181">В отличие от DAO ADO и ADOX объекты можно выполнить помеченные действия в базах данных, отличный от Jet до тех пор, пока поставщик для этих баз данных поддерживает это действие.</span><span class="sxs-lookup"><span data-stu-id="17ba9-181">Unlike DAO, ADO and ADOX objects can perform the marked actions in databases other than Jet as long as the provider for those databases supports that action.</span></span>


