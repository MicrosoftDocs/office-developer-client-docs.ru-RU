---
title: Интерфейсы и объекты ADO
TOCTitle: ADO objects and interfaces
ms:assetid: bebf4a80-8b6e-c43c-4138-897055cc60d3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249927(v=office.15)
ms:contentKeyID: 48547471
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 539feb1918877189548d0e7cff6ceb28e50abddc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283263"
---
# <a name="ado-objects-and-interfaces"></a><span data-ttu-id="1c6fb-102">Интерфейсы и объекты ADO</span><span class="sxs-lookup"><span data-stu-id="1c6fb-102">ADO objects and interfaces</span></span>

<span data-ttu-id="1c6fb-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1c6fb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1c6fb-104">Отношения между этими объектами представлены в объектной модели объектов данных ActiveX (ADO).</span><span class="sxs-lookup"><span data-stu-id="1c6fb-104">The relationships between these objects are represented in the ActiveX Data Objects (ADO) Object Model.</span></span>

<span data-ttu-id="1c6fb-105">Каждый объект может содержаться в соответствующей коллекции.</span><span class="sxs-lookup"><span data-stu-id="1c6fb-105">Each object can be contained in its corresponding collection.</span></span> <span data-ttu-id="1c6fb-106">Например, объект [Error](error-object-ado.md) может содержаться в коллекции [Errors](errors-collection-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="1c6fb-106">For example, an [Error](error-object-ado.md) object can be contained in an [Errors](errors-collection-ado.md) collection.</span></span> <span data-ttu-id="1c6fb-107">Дополнительные сведения см. в статье [коллекции ADO](ado-collections.md)</span><span class="sxs-lookup"><span data-stu-id="1c6fb-107">For more information, see [ADO collections](ado-collections.md) or a specific collection topic.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th><span data-ttu-id="1c6fb-108">Object</span><span class="sxs-lookup"><span data-stu-id="1c6fb-108">Object</span></span></th>
<th><span data-ttu-id="1c6fb-109">Описание</span><span class="sxs-lookup"><span data-stu-id="1c6fb-109">Description</span></span></th>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c6fb-110"><a href="adorecordconstruction-interface-ado.md">ADORecordConstruction</a></span><span class="sxs-lookup"><span data-stu-id="1c6fb-110"><a href="adorecordconstruction-interface-ado.md">ADORecordConstruction</a></span></span></p></td>
<td><p><span data-ttu-id="1c6fb-111">Создает объект <strong>записи</strong> ADO из объекта <strong>строки</strong> OLE DB в приложении C/C++.</span><span class="sxs-lookup"><span data-stu-id="1c6fb-111">Constructs an ADO <strong>Record</strong> object from an OLE DB <strong>Row</strong> object in a C/C++ application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c6fb-112"><a href="adorecordsetconstruction-interface-ado.md">ADORecordsetConstruction</a></span><span class="sxs-lookup"><span data-stu-id="1c6fb-112"><a href="adorecordsetconstruction-interface-ado.md">ADORecordsetConstruction</a></span></span></p></td>
<td><p><span data-ttu-id="1c6fb-113">Создает объект <strong>набора записей</strong> ADO из объекта <strong>набора строк</strong> OLE DB в приложении C/C++.</span><span class="sxs-lookup"><span data-stu-id="1c6fb-113">Constructs an ADO <strong>Recordset</strong> object from an OLE DB <strong>Rowset</strong> object in a C/C++ application.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c6fb-114"><a href="error-object-ado.md">Command</a></span><span class="sxs-lookup"><span data-stu-id="1c6fb-114"><a href="error-object-ado.md">Command</a></span></span></p></td>
<td><p><span data-ttu-id="1c6fb-115">Определяет определенную команду, которую необходимо выполнить для источника данных.</span><span class="sxs-lookup"><span data-stu-id="1c6fb-115">Defines a specific command that you intend to execute against a data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c6fb-116"><a href="field-object-ado.md">Connection</a></span><span class="sxs-lookup"><span data-stu-id="1c6fb-116"><a href="field-object-ado.md">Connection</a></span></span></p></td>
<td><p><span data-ttu-id="1c6fb-117">Представляет открытое подключение к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="1c6fb-117">Represents an open connection to a data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c6fb-118"><a href="error-object-ado.md">Error</a></span><span class="sxs-lookup"><span data-stu-id="1c6fb-118"><a href="error-object-ado.md">Error</a></span></span></p></td>
<td><p><span data-ttu-id="1c6fb-119">Содержит сведения об ошибках доступа к данным, относящихся к одной операции, включающей в себя поставщика.</span><span class="sxs-lookup"><span data-stu-id="1c6fb-119">Contains details about data access errors that pertain to a single operation involving the provider.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c6fb-120"><a href="field-object-ado.md">Field</a></span><span class="sxs-lookup"><span data-stu-id="1c6fb-120"><a href="field-object-ado.md">Field</a></span></span></p></td>
<td><p><span data-ttu-id="1c6fb-121">Представляет столбец данных с общим типом данных.</span><span class="sxs-lookup"><span data-stu-id="1c6fb-121">Represents a column of data with a common data type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c6fb-122"><a href="parameter-object-ado.md">Parameter</a></span><span class="sxs-lookup"><span data-stu-id="1c6fb-122"><a href="parameter-object-ado.md">Parameter</a></span></span></p></td>
<td><p><span data-ttu-id="1c6fb-123">Представляет параметр или аргумент, связанный с объектом <strong>Command</strong> на основе параметризованного запроса или хранимой процедуры.</span><span class="sxs-lookup"><span data-stu-id="1c6fb-123">Represents a parameter or argument associated with a <strong>Command</strong> object based on a parameterized query or stored procedure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c6fb-124"><a href="property-object-ado.md">Property</a></span><span class="sxs-lookup"><span data-stu-id="1c6fb-124"><a href="property-object-ado.md">Property</a></span></span></p></td>
<td><p><span data-ttu-id="1c6fb-125">Представляет динамическую характеристику объекта ADO, определяемого поставщиком.</span><span class="sxs-lookup"><span data-stu-id="1c6fb-125">Represents a dynamic characteristic of an ADO object that is defined by the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c6fb-126"><a href="record-object-ado.md">Record</a></span><span class="sxs-lookup"><span data-stu-id="1c6fb-126"><a href="record-object-ado.md">Record</a></span></span></p></td>
<td><p><span data-ttu-id="1c6fb-127">Представляет строку объекта <strong>Recordset</strong>или каталога или файла в файловой системе.</span><span class="sxs-lookup"><span data-stu-id="1c6fb-127">Represents a row of a <strong>Recordset</strong>, or a directory or file in a file system.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c6fb-128"><a href="recordset-object-ado.md">Recordset</a></span><span class="sxs-lookup"><span data-stu-id="1c6fb-128"><a href="recordset-object-ado.md">Recordset</a></span></span></p></td>
<td><p><span data-ttu-id="1c6fb-129">Представляет весь набор записей из базовой таблицы или результаты выполненной команды.</span><span class="sxs-lookup"><span data-stu-id="1c6fb-129">Represents the entire set of records from a base table or the results of an executed command.</span></span> <span data-ttu-id="1c6fb-130">В любой момент объект <strong>Recordset</strong> относится только к одной записи в наборе в качестве текущей записи.</span><span class="sxs-lookup"><span data-stu-id="1c6fb-130">At any time, the <strong>Recordset</strong> object refers to only a single record within the set as the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c6fb-131"><a href="stream-object-ado.md">Stream</a></span><span class="sxs-lookup"><span data-stu-id="1c6fb-131"><a href="stream-object-ado.md">Stream</a></span></span></p></td>
<td><p><span data-ttu-id="1c6fb-132">Представляет двоичный поток данных.</span><span class="sxs-lookup"><span data-stu-id="1c6fb-132">Represents a binary stream of data.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

