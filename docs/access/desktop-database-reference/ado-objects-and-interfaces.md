---
title: ADO Objects and Interfaces
TOCTitle: ADO Objects and Interfaces
ms:assetid: bebf4a80-8b6e-c43c-4138-897055cc60d3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249927(v=office.15)
ms:contentKeyID: 48547471
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ce04896e6ae59af6917497d9e37dc1ae97222eff
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480118"
---
# <a name="ado-objects-and-interfaces"></a><span data-ttu-id="471a0-102">ADO Objects and Interfaces</span><span class="sxs-lookup"><span data-stu-id="471a0-102">ADO Objects and Interfaces</span></span>


<span data-ttu-id="471a0-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="471a0-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="471a0-104">Отношения между эти объекты, представленные в объектной модели ADO.</span><span class="sxs-lookup"><span data-stu-id="471a0-104">The relationships between these objects are represented in the ADO Object Model.</span></span>

<span data-ttu-id="471a0-105">Каждый объект может содержаться в соответствующие коллекции.</span><span class="sxs-lookup"><span data-stu-id="471a0-105">Each object can be contained in its corresponding collection.</span></span> <span data-ttu-id="471a0-106">Например объект [Error](error-object-ado.md) может содержаться в семейство [Errors](errors-collection-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="471a0-106">For example, an [Error](error-object-ado.md) object can be contained in an [Errors](errors-collection-ado.md) collection.</span></span> <span data-ttu-id="471a0-107">Для получения дополнительных сведений см [ADO семейств сайтов](ado-collections.md) или раздела конкретной коллекции.</span><span class="sxs-lookup"><span data-stu-id="471a0-107">For more information, see [ADO Collections](ado-collections.md) or a specific collection topic.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="471a0-108"><a href="adorecordconstruction-interface-ado.md">ADORecordConstruction</a></span><span class="sxs-lookup"><span data-stu-id="471a0-108"><a href="adorecordconstruction-interface-ado.md">ADORecordConstruction</a></span></span></p></td>
<td><p><span data-ttu-id="471a0-109">Создает объект ADO <strong>записи</strong> из объекта OLE DB <strong>строки</strong> в приложении C/C++.</span><span class="sxs-lookup"><span data-stu-id="471a0-109">Constructs an ADO <strong>Record</strong> object from an OLE DB <strong>Row</strong> object in a C/C++ application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="471a0-110"><a href="adorecordsetconstruction-interface-ado.md">ADORecordsetConstruction</a></span><span class="sxs-lookup"><span data-stu-id="471a0-110"><a href="adorecordsetconstruction-interface-ado.md">ADORecordsetConstruction</a></span></span></p></td>
<td><p><span data-ttu-id="471a0-111">Создает объект ADO <strong>записей</strong> из объекта OLE DB <strong>строк</strong> в приложении C/C++.</span><span class="sxs-lookup"><span data-stu-id="471a0-111">Constructs an ADO <strong>Recordset</strong> object from an OLE DB <strong>Rowset</strong> object in a C/C++ application.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="471a0-112"><a href="error-object-ado.md">Ошибка</a></span><span class="sxs-lookup"><span data-stu-id="471a0-112"><a href="error-object-ado.md">Error</a></span></span></p></td>
<td><p><span data-ttu-id="471a0-113">Содержит сведения об ошибках доступа к данным, которые относятся к одной операции, включающие использование поставщика.</span><span class="sxs-lookup"><span data-stu-id="471a0-113">Contains details about data access errors that pertain to a single operation involving the provider.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="471a0-114"><a href="field-object-ado.md">Поле</a></span><span class="sxs-lookup"><span data-stu-id="471a0-114"><a href="field-object-ado.md">Field</a></span></span></p></td>
<td><p><span data-ttu-id="471a0-115">Представляет столбец данных с типом данных.</span><span class="sxs-lookup"><span data-stu-id="471a0-115">Represents a column of data with a common data type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="471a0-116"><a href="parameter-object-ado.md">Параметр</a></span><span class="sxs-lookup"><span data-stu-id="471a0-116"><a href="parameter-object-ado.md">Parameter</a></span></span></p></td>
<td><p><span data-ttu-id="471a0-117">Представляет параметр или аргумент, связанной с объектом <strong>команды</strong> на основе параметризованный запрос или хранимую процедуру.</span><span class="sxs-lookup"><span data-stu-id="471a0-117">Represents a parameter or argument associated with a <strong>Command</strong> object based on a parameterized query or stored procedure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="471a0-118"><a href="property-object-ado.md">Свойство</a></span><span class="sxs-lookup"><span data-stu-id="471a0-118"><a href="property-object-ado.md">Property</a></span></span></p></td>
<td><p><span data-ttu-id="471a0-119">Представляет характеристику динамического объекта ADO, определяемый поставщиком.</span><span class="sxs-lookup"><span data-stu-id="471a0-119">Represents a dynamic characteristic of an ADO object that is defined by the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="471a0-120"><a href="record-object-ado.md">Запись</a></span><span class="sxs-lookup"><span data-stu-id="471a0-120"><a href="record-object-ado.md">Record</a></span></span></p></td>
<td><p><span data-ttu-id="471a0-121">Представляет строку <strong>записей</strong>каталогов или файлов в файловой системе.</span><span class="sxs-lookup"><span data-stu-id="471a0-121">Represents a row of a <strong>Recordset</strong>, or a directory or file in a file system.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="471a0-122"><a href="recordset-object-ado.md">Набор записей</a></span><span class="sxs-lookup"><span data-stu-id="471a0-122"><a href="recordset-object-ado.md">Recordset</a></span></span></p></td>
<td><p><span data-ttu-id="471a0-123">Представляет полного набора записей из базовой таблицы или результаты выполнения команды.</span><span class="sxs-lookup"><span data-stu-id="471a0-123">Represents the entire set of records from a base table or the results of an executed command.</span></span> <span data-ttu-id="471a0-124">В любое время в объект <strong>набора записей</strong> называется только одной записи в наборе текущей записи.</span><span class="sxs-lookup"><span data-stu-id="471a0-124">At any time, the <strong>Recordset</strong> object refers to only a single record within the set as the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="471a0-125"><a href="stream-object-ado.md">Stream</a></span><span class="sxs-lookup"><span data-stu-id="471a0-125"><a href="stream-object-ado.md">Stream</a></span></span></p></td>
<td><p><span data-ttu-id="471a0-126">Представляет двоичный поток данных.</span><span class="sxs-lookup"><span data-stu-id="471a0-126">Represents a binary stream of data.</span></span></p></td>
</tr>
</tbody>
</table>

