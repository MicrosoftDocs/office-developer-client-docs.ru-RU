---
title: Объекты и интерфейсы ADO
TOCTitle: ADO objects and interfaces
ms:assetid: bebf4a80-8b6e-c43c-4138-897055cc60d3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249927(v=office.15)
ms:contentKeyID: 48547471
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fa301974b4b417d09b0439b3970ee366eeb5d06e
ms.sourcegitcommit: 48bfe5ab15b11105f4f52937b886c92bdc26525a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25910729"
---
# <a name="ado-objects-and-interfaces"></a><span data-ttu-id="a6584-102">Объекты и интерфейсы ADO</span><span class="sxs-lookup"><span data-stu-id="a6584-102">ADO objects and interfaces</span></span>

<span data-ttu-id="a6584-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a6584-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a6584-104">Отношения между эти объекты, представленные в объектной модели ActiveX Data Objects (ADO).</span><span class="sxs-lookup"><span data-stu-id="a6584-104">The relationships between these objects are represented in the ActiveX Data Objects (ADO) Object Model.</span></span>

<span data-ttu-id="a6584-105">Каждый объект может содержаться в соответствующие коллекции.</span><span class="sxs-lookup"><span data-stu-id="a6584-105">Each object can be contained in its corresponding collection.</span></span> <span data-ttu-id="a6584-106">Например объект [Error](error-object-ado.md) может содержаться в семейство [Errors](errors-collection-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="a6584-106">For example, an [Error](error-object-ado.md) object can be contained in an [Errors](errors-collection-ado.md) collection.</span></span> <span data-ttu-id="a6584-107">Для получения дополнительных сведений см [ADO семейств сайтов](ado-collections.md) или раздела конкретной коллекции.</span><span class="sxs-lookup"><span data-stu-id="a6584-107">For more information, see [ADO collections](ado-collections.md) or a specific collection topic.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th><span data-ttu-id="a6584-108">Объект</span><span class="sxs-lookup"><span data-stu-id="a6584-108">Object</span></span></th>
<th><span data-ttu-id="a6584-109">Описание</span><span class="sxs-lookup"><span data-stu-id="a6584-109">Description</span></span></th>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6584-110"><a href="adorecordconstruction-interface-ado.md">ADORecordConstruction</a></span><span class="sxs-lookup"><span data-stu-id="a6584-110"><a href="adorecordconstruction-interface-ado.md">ADORecordConstruction</a></span></span></p></td>
<td><p><span data-ttu-id="a6584-111">Создает объект ADO <strong>записи</strong> из объекта OLE DB <strong>строки</strong> в приложении C/C++.</span><span class="sxs-lookup"><span data-stu-id="a6584-111">Constructs an ADO <strong>Record</strong> object from an OLE DB <strong>Row</strong> object in a C/C++ application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6584-112"><a href="adorecordsetconstruction-interface-ado.md">ADORecordsetConstruction</a></span><span class="sxs-lookup"><span data-stu-id="a6584-112"><a href="adorecordsetconstruction-interface-ado.md">ADORecordsetConstruction</a></span></span></p></td>
<td><p><span data-ttu-id="a6584-113">Создает объект ADO <strong>записей</strong> из объекта OLE DB <strong>строк</strong> в приложении C/C++.</span><span class="sxs-lookup"><span data-stu-id="a6584-113">Constructs an ADO <strong>Recordset</strong> object from an OLE DB <strong>Rowset</strong> object in a C/C++ application.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6584-114"><a href="error-object-ado.md">Команда</a></span><span class="sxs-lookup"><span data-stu-id="a6584-114"><a href="error-object-ado.md">Command</a></span></span></p></td>
<td><p><span data-ttu-id="a6584-115">Определяет определенной команде, которые планируется выполнить в источнике данных.</span><span class="sxs-lookup"><span data-stu-id="a6584-115">Defines a specific command that you intend to execute against a data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6584-116"><a href="field-object-ado.md">Подключение</a></span><span class="sxs-lookup"><span data-stu-id="a6584-116"><a href="field-object-ado.md">Connection</a></span></span></p></td>
<td><p><span data-ttu-id="a6584-117">Представляет открытое подключение к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="a6584-117">Represents an open connection to a data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6584-118"><a href="error-object-ado.md">Ошибка</a></span><span class="sxs-lookup"><span data-stu-id="a6584-118"><a href="error-object-ado.md">Error</a></span></span></p></td>
<td><p><span data-ttu-id="a6584-119">Содержит сведения об ошибках доступа к данным, которые относятся к одной операции, включающие использование поставщика.</span><span class="sxs-lookup"><span data-stu-id="a6584-119">Contains details about data access errors that pertain to a single operation involving the provider.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6584-120"><a href="field-object-ado.md">Поле</a></span><span class="sxs-lookup"><span data-stu-id="a6584-120"><a href="field-object-ado.md">Field</a></span></span></p></td>
<td><p><span data-ttu-id="a6584-121">Представляет столбец данных с типом данных.</span><span class="sxs-lookup"><span data-stu-id="a6584-121">Represents a column of data with a common data type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6584-122"><a href="parameter-object-ado.md">Параметр</a></span><span class="sxs-lookup"><span data-stu-id="a6584-122"><a href="parameter-object-ado.md">Parameter</a></span></span></p></td>
<td><p><span data-ttu-id="a6584-123">Представляет параметр или аргумент, связанной с объектом <strong>команды</strong> на основе параметризованный запрос или хранимую процедуру.</span><span class="sxs-lookup"><span data-stu-id="a6584-123">Represents a parameter or argument associated with a <strong>Command</strong> object based on a parameterized query or stored procedure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6584-124"><a href="property-object-ado.md">Свойство</a></span><span class="sxs-lookup"><span data-stu-id="a6584-124"><a href="property-object-ado.md">Property</a></span></span></p></td>
<td><p><span data-ttu-id="a6584-125">Представляет характеристику динамического объекта ADO, определяемый поставщиком.</span><span class="sxs-lookup"><span data-stu-id="a6584-125">Represents a dynamic characteristic of an ADO object that is defined by the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6584-126"><a href="record-object-ado.md">Запись</a></span><span class="sxs-lookup"><span data-stu-id="a6584-126"><a href="record-object-ado.md">Record</a></span></span></p></td>
<td><p><span data-ttu-id="a6584-127">Представляет строку <strong>записей</strong>каталогов или файлов в файловой системе.</span><span class="sxs-lookup"><span data-stu-id="a6584-127">Represents a row of a <strong>Recordset</strong>, or a directory or file in a file system.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6584-128"><a href="recordset-object-ado.md">Набор записей</a></span><span class="sxs-lookup"><span data-stu-id="a6584-128"><a href="recordset-object-ado.md">Recordset</a></span></span></p></td>
<td><p><span data-ttu-id="a6584-129">Представляет полного набора записей из базовой таблицы или результаты выполнения команды.</span><span class="sxs-lookup"><span data-stu-id="a6584-129">Represents the entire set of records from a base table or the results of an executed command.</span></span> <span data-ttu-id="a6584-130">В любое время в объект <strong>набора записей</strong> называется только одной записи в наборе текущей записи.</span><span class="sxs-lookup"><span data-stu-id="a6584-130">At any time, the <strong>Recordset</strong> object refers to only a single record within the set as the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6584-131"><a href="stream-object-ado.md">Stream</a></span><span class="sxs-lookup"><span data-stu-id="a6584-131"><a href="stream-object-ado.md">Stream</a></span></span></p></td>
<td><p><span data-ttu-id="a6584-132">Представляет двоичный поток данных.</span><span class="sxs-lookup"><span data-stu-id="a6584-132">Represents a binary stream of data.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

