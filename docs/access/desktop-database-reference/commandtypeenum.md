---
title: CommandTypeEnum (Справочник по для настольных баз данных Access)
TOCTitle: CommandTypeEnum
ms:assetid: 9ad8f155-88a0-00eb-2855-1e1a2a677437
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249700(v=office.15)
ms:contentKeyID: 48546549
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: a570aaed8f0b2da415c3866ec88e7023085a1319
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887945"
---
# <a name="commandtypeenum"></a><span data-ttu-id="d457c-102">CommandTypeEnum</span><span class="sxs-lookup"><span data-stu-id="d457c-102">CommandTypeEnum</span></span>

<span data-ttu-id="d457c-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d457c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d457c-104">Указывает, как интерпретировать аргумент команды.</span><span class="sxs-lookup"><span data-stu-id="d457c-104">Specifies how a command argument should be interpreted.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d457c-105">Константа</span><span class="sxs-lookup"><span data-stu-id="d457c-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="d457c-106">Значение</span><span class="sxs-lookup"><span data-stu-id="d457c-106">Value</span></span></p></th>
<th><p><span data-ttu-id="d457c-107">Описание</span><span class="sxs-lookup"><span data-stu-id="d457c-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d457c-108"><strong>adCmdUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="d457c-108"><strong>adCmdUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="d457c-109">-1</span><span class="sxs-lookup"><span data-stu-id="d457c-109">-1</span></span></p></td>
<td><p><span data-ttu-id="d457c-110">Не указан аргумент типа команды.</span><span class="sxs-lookup"><span data-stu-id="d457c-110">Does not specify the command type argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d457c-111"><strong>adCmdText</strong></span><span class="sxs-lookup"><span data-stu-id="d457c-111"><strong>adCmdText</strong></span></span></p></td>
<td><p><span data-ttu-id="d457c-112">1</span><span class="sxs-lookup"><span data-stu-id="d457c-112">1</span></span></p></td>
<td><p><span data-ttu-id="d457c-113">Оценивает <a href="commandtext-property-ado.md">CommandText</a> как текстовое определения вызова команды или хранимой процедуры.</span><span class="sxs-lookup"><span data-stu-id="d457c-113">Evaluates <a href="commandtext-property-ado.md">CommandText</a> as a textual definition of a command or stored procedure call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d457c-114"><strong>adCmdTable</strong></span><span class="sxs-lookup"><span data-stu-id="d457c-114"><strong>adCmdTable</strong></span></span></p></td>
<td><p><span data-ttu-id="d457c-115">2</span><span class="sxs-lookup"><span data-stu-id="d457c-115">2</span></span></p></td>
<td><p><span data-ttu-id="d457c-116">Оценивает <strong>CommandText</strong> как имя таблицы, столбцы возвращаются с внутренними запрос SQL.</span><span class="sxs-lookup"><span data-stu-id="d457c-116">Evaluates <strong>CommandText</strong> as a table name whose columns are all returned by an internally generated SQL query.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d457c-117"><strong>adCmdStoredProc</strong></span><span class="sxs-lookup"><span data-stu-id="d457c-117"><strong>adCmdStoredProc</strong></span></span></p></td>
<td><p><span data-ttu-id="d457c-118">4</span><span class="sxs-lookup"><span data-stu-id="d457c-118">4</span></span></p></td>
<td><p><span data-ttu-id="d457c-119">Оценивает <strong>CommandText</strong> как имя хранимой процедуры.</span><span class="sxs-lookup"><span data-stu-id="d457c-119">Evaluates <strong>CommandText</strong> as a stored procedure name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d457c-120"><strong>adCmdUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="d457c-120"><strong>adCmdUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="d457c-121">8</span><span class="sxs-lookup"><span data-stu-id="d457c-121">8</span></span></p></td>
<td><p><span data-ttu-id="d457c-122">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d457c-122">Default.</span></span> <span data-ttu-id="d457c-123">Указывает, что тип команды в свойстве <strong>CommandText</strong> не известен.</span><span class="sxs-lookup"><span data-stu-id="d457c-123">Indicates that the type of command in the <strong>CommandText</strong> property is not known.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d457c-124"><strong>adCmdFile</strong></span><span class="sxs-lookup"><span data-stu-id="d457c-124"><strong>adCmdFile</strong></span></span></p></td>
<td><p><span data-ttu-id="d457c-125">256</span><span class="sxs-lookup"><span data-stu-id="d457c-125">256</span></span></p></td>
<td><p><span data-ttu-id="d457c-126">Оценивает <strong>CommandText</strong> как имя файла постоянно хранимых <a href="recordset-object-ado.md">набора записей</a>.</span><span class="sxs-lookup"><span data-stu-id="d457c-126">Evaluates <strong>CommandText</strong> as the file name of a persistently stored <a href="recordset-object-ado.md">Recordset</a>.</span></span> <span data-ttu-id="d457c-127">Используется с <strong>набора записей.</strong> <a href="open-method-ado-recordset.md">Open</a> или только <a href="requery-method-ado.md">повторный запрос</a> .</span><span class="sxs-lookup"><span data-stu-id="d457c-127">Used with <strong>Recordset.</strong><a href="open-method-ado-recordset.md">Open</a> or <a href="requery-method-ado.md">Requery</a> only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d457c-128"><strong>adCmdTableDirect</strong></span><span class="sxs-lookup"><span data-stu-id="d457c-128"><strong>adCmdTableDirect</strong></span></span></p></td>
<td><p><span data-ttu-id="d457c-129">512</span><span class="sxs-lookup"><span data-stu-id="d457c-129">512</span></span></p></td>
<td><p><span data-ttu-id="d457c-130">Оценивает <strong>CommandText</strong> как имя таблицы, столбцы возвращаются все.</span><span class="sxs-lookup"><span data-stu-id="d457c-130">Evaluates <strong>CommandText</strong> as a table name whose columns are all returned.</span></span> <span data-ttu-id="d457c-131">Используется только с <strong>Recordset.Open</strong> или <strong>повторный запрос</strong> .</span><span class="sxs-lookup"><span data-stu-id="d457c-131">Used with <strong>Recordset.Open</strong> or <strong>Requery</strong> only.</span></span> <span data-ttu-id="d457c-132">Использование метода <a href="seek-method-ado.md">Seek</a> , необходимо открыть <strong>набора записей</strong> с <strong>adCmdTableDirect</strong>.</span><span class="sxs-lookup"><span data-stu-id="d457c-132">To use the <a href="seek-method-ado.md">Seek</a> method, the <strong>Recordset</strong> must be opened with <strong>adCmdTableDirect</strong>.</span></span> <span data-ttu-id="d457c-133">Это значение не может быть вместе с значение <a href="executeoptionenum.md">ExecuteOptionEnum</a> <strong>adAsyncExecute</strong>.</span><span class="sxs-lookup"><span data-stu-id="d457c-133">This value cannot be combined with the <a href="executeoptionenum.md">ExecuteOptionEnum</a> value <strong>adAsyncExecute</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="d457c-134">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="d457c-134">ADO/WFC equivalent</span></span>

<span data-ttu-id="d457c-135">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="d457c-135">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d457c-136">Constant</span><span class="sxs-lookup"><span data-stu-id="d457c-136">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d457c-137">AdoEnums.CommandType.UNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="d457c-137">AdoEnums.CommandType.UNSPECIFIED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d457c-138">AdoEnums.CommandType.TEXT</span><span class="sxs-lookup"><span data-stu-id="d457c-138">AdoEnums.CommandType.TEXT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d457c-139">AdoEnums.CommandType.TABLE</span><span class="sxs-lookup"><span data-stu-id="d457c-139">AdoEnums.CommandType.TABLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d457c-140">AdoEnums.CommandType.STOREDPROC</span><span class="sxs-lookup"><span data-stu-id="d457c-140">AdoEnums.CommandType.STOREDPROC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d457c-141">AdoEnums.CommandType.UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="d457c-141">AdoEnums.CommandType.UNKNOWN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d457c-142">AdoEnums.CommandType.FILE</span><span class="sxs-lookup"><span data-stu-id="d457c-142">AdoEnums.CommandType.FILE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d457c-143">AdoEnums.CommandType.TABLEDIRECT</span><span class="sxs-lookup"><span data-stu-id="d457c-143">AdoEnums.CommandType.TABLEDIRECT</span></span></p></td>
</tr>
</tbody>
</table>

