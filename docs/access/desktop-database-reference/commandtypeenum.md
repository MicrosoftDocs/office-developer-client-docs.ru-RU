---
title: CommandTypeEnum (справочник по базам данных Access для настольных ПК)
TOCTitle: CommandTypeEnum
ms:assetid: 9ad8f155-88a0-00eb-2855-1e1a2a677437
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249700(v=office.15)
ms:contentKeyID: 48546549
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a9114128771d4753265208dada763ac0c9f796d1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296117"
---
# <a name="commandtypeenum"></a><span data-ttu-id="f9abd-102">CommandTypeEnum</span><span class="sxs-lookup"><span data-stu-id="f9abd-102">CommandTypeEnum</span></span>

<span data-ttu-id="f9abd-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f9abd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f9abd-104">Указывает, как следует интерпретировать аргумент команды.</span><span class="sxs-lookup"><span data-stu-id="f9abd-104">Specifies how a command argument should be interpreted.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f9abd-105">Константа</span><span class="sxs-lookup"><span data-stu-id="f9abd-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="f9abd-106">Значение</span><span class="sxs-lookup"><span data-stu-id="f9abd-106">Value</span></span></p></th>
<th><p><span data-ttu-id="f9abd-107">Описание</span><span class="sxs-lookup"><span data-stu-id="f9abd-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f9abd-108"><strong>adCmdUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="f9abd-108"><strong>adCmdUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="f9abd-109">–1</span><span class="sxs-lookup"><span data-stu-id="f9abd-109">-1</span></span></p></td>
<td><p><span data-ttu-id="f9abd-110">Не указывает аргумент типа команды.</span><span class="sxs-lookup"><span data-stu-id="f9abd-110">Does not specify the command type argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9abd-111"><strong>adCmdText</strong></span><span class="sxs-lookup"><span data-stu-id="f9abd-111"><strong>adCmdText</strong></span></span></p></td>
<td><p><span data-ttu-id="f9abd-112">1 </span><span class="sxs-lookup"><span data-stu-id="f9abd-112">1</span></span></p></td>
<td><p><span data-ttu-id="f9abd-113">Оценивает <a href="commandtext-property-ado.md">CommandText как</a> текстовое определение вызова команды или хранимой процедуры.</span><span class="sxs-lookup"><span data-stu-id="f9abd-113">Evaluates <a href="commandtext-property-ado.md">CommandText</a> as a textual definition of a command or stored procedure call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9abd-114"><strong>adCmdTable</strong></span><span class="sxs-lookup"><span data-stu-id="f9abd-114"><strong>adCmdTable</strong></span></span></p></td>
<td><p><span data-ttu-id="f9abd-115">2 </span><span class="sxs-lookup"><span data-stu-id="f9abd-115">2</span></span></p></td>
<td><p><span data-ttu-id="f9abd-116">Оценивает <strong>CommandText как</strong> имя таблицы, столбцы которой возвращаются внутренним SQL запроса.</span><span class="sxs-lookup"><span data-stu-id="f9abd-116">Evaluates <strong>CommandText</strong> as a table name whose columns are all returned by an internally generated SQL query.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9abd-117"><strong>adCmdStoredProc</strong></span><span class="sxs-lookup"><span data-stu-id="f9abd-117"><strong>adCmdStoredProc</strong></span></span></p></td>
<td><p><span data-ttu-id="f9abd-118">4 </span><span class="sxs-lookup"><span data-stu-id="f9abd-118">4</span></span></p></td>
<td><p><span data-ttu-id="f9abd-119">Оценивает <strong>CommandText в качестве</strong> имени хранимой процедуры.</span><span class="sxs-lookup"><span data-stu-id="f9abd-119">Evaluates <strong>CommandText</strong> as a stored procedure name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9abd-120"><strong>adCmdUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="f9abd-120"><strong>adCmdUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="f9abd-121">8 </span><span class="sxs-lookup"><span data-stu-id="f9abd-121">8</span></span></p></td>
<td><p><span data-ttu-id="f9abd-122">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f9abd-122">Default.</span></span> <span data-ttu-id="f9abd-123">Указывает, что тип команды в свойстве <strong>CommandText</strong> неизвестна.</span><span class="sxs-lookup"><span data-stu-id="f9abd-123">Indicates that the type of command in the <strong>CommandText</strong> property is not known.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9abd-124"><strong>adCmdFile</strong></span><span class="sxs-lookup"><span data-stu-id="f9abd-124"><strong>adCmdFile</strong></span></span></p></td>
<td><p><span data-ttu-id="f9abd-125">256</span><span class="sxs-lookup"><span data-stu-id="f9abd-125">256</span></span></p></td>
<td><p><span data-ttu-id="f9abd-126">Оценивает <strong>CommandText в</strong> качестве имени файла постоянно хранимого <a href="recordset-object-ado.md">наборов записей.</a></span><span class="sxs-lookup"><span data-stu-id="f9abd-126">Evaluates <strong>CommandText</strong> as the file name of a persistently stored <a href="recordset-object-ado.md">Recordset</a>.</span></span> <span data-ttu-id="f9abd-127">Используется с <strong>recordset.</strong> <a href="open-method-ado-recordset.md">Только open</a> или <a href="requery-method-ado.md">Requery.</a></span><span class="sxs-lookup"><span data-stu-id="f9abd-127">Used with <strong>Recordset.</strong><a href="open-method-ado-recordset.md">Open</a> or <a href="requery-method-ado.md">Requery</a> only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9abd-128"><strong>adCmdTableDirect</strong></span><span class="sxs-lookup"><span data-stu-id="f9abd-128"><strong>adCmdTableDirect</strong></span></span></p></td>
<td><p><span data-ttu-id="f9abd-129">512</span><span class="sxs-lookup"><span data-stu-id="f9abd-129">512</span></span></p></td>
<td><p><span data-ttu-id="f9abd-130">Оценивает <strong>CommandText как</strong> имя таблицы, столбцы которой возвращаются.</span><span class="sxs-lookup"><span data-stu-id="f9abd-130">Evaluates <strong>CommandText</strong> as a table name whose columns are all returned.</span></span> <span data-ttu-id="f9abd-131">Используется только <strong>с Recordset.Open</strong> или <strong>Requery.</strong></span><span class="sxs-lookup"><span data-stu-id="f9abd-131">Used with <strong>Recordset.Open</strong> or <strong>Requery</strong> only.</span></span> <span data-ttu-id="f9abd-132">Чтобы использовать метод <a href="seek-method-ado.md">Seek,</a> <strong>recordset</strong> необходимо открыть с <strong>помощью adCmdTableDirect.</strong></span><span class="sxs-lookup"><span data-stu-id="f9abd-132">To use the <a href="seek-method-ado.md">Seek</a> method, the <strong>Recordset</strong> must be opened with <strong>adCmdTableDirect</strong>.</span></span> <span data-ttu-id="f9abd-133">Это значение нельзя объединить со <a href="executeoptionenum.md">значением ExecuteOptionEnum</a> <strong>adAsyncExecute.</strong></span><span class="sxs-lookup"><span data-stu-id="f9abd-133">This value cannot be combined with the <a href="executeoptionenum.md">ExecuteOptionEnum</a> value <strong>adAsyncExecute</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="f9abd-134">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="f9abd-134">ADO/WFC equivalent</span></span>

<span data-ttu-id="f9abd-135">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="f9abd-135">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f9abd-136">Константа</span><span class="sxs-lookup"><span data-stu-id="f9abd-136">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f9abd-137">AdoEnums.CommandType.UNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="f9abd-137">AdoEnums.CommandType.UNSPECIFIED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9abd-138">AdoEnums.CommandType.TEXT</span><span class="sxs-lookup"><span data-stu-id="f9abd-138">AdoEnums.CommandType.TEXT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9abd-139">AdoEnums.CommandType.TABLE</span><span class="sxs-lookup"><span data-stu-id="f9abd-139">AdoEnums.CommandType.TABLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9abd-140">AdoEnums.CommandType.STOREDPROC</span><span class="sxs-lookup"><span data-stu-id="f9abd-140">AdoEnums.CommandType.STOREDPROC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9abd-141">AdoEnums.CommandType.UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="f9abd-141">AdoEnums.CommandType.UNKNOWN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9abd-142">AdoEnums.CommandType.FILE</span><span class="sxs-lookup"><span data-stu-id="f9abd-142">AdoEnums.CommandType.FILE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9abd-143">AdoEnums.CommandType.TABLEDIRECT</span><span class="sxs-lookup"><span data-stu-id="f9abd-143">AdoEnums.CommandType.TABLEDIRECT</span></span></p></td>
</tr>
</tbody>
</table>

