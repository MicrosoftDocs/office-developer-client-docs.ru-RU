---
title: Коммандтипинум (Справочник по базам данных Access на компьютере)
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
# <a name="commandtypeenum"></a><span data-ttu-id="e8322-102">CommandTypeEnum</span><span class="sxs-lookup"><span data-stu-id="e8322-102">CommandTypeEnum</span></span>

<span data-ttu-id="e8322-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e8322-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e8322-104">Указывает, как должен интерпретироваться аргумент команды.</span><span class="sxs-lookup"><span data-stu-id="e8322-104">Specifies how a command argument should be interpreted.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e8322-105">Константа</span><span class="sxs-lookup"><span data-stu-id="e8322-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="e8322-106">Значение</span><span class="sxs-lookup"><span data-stu-id="e8322-106">Value</span></span></p></th>
<th><p><span data-ttu-id="e8322-107">Описание</span><span class="sxs-lookup"><span data-stu-id="e8322-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e8322-108"><strong>адкмдунспеЦифиед</strong></span><span class="sxs-lookup"><span data-stu-id="e8322-108"><strong>adCmdUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="e8322-109">–1</span><span class="sxs-lookup"><span data-stu-id="e8322-109">-1</span></span></p></td>
<td><p><span data-ttu-id="e8322-110">Не указывает аргумент типа команды.</span><span class="sxs-lookup"><span data-stu-id="e8322-110">Does not specify the command type argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8322-111"><strong>адкмдтекст</strong></span><span class="sxs-lookup"><span data-stu-id="e8322-111"><strong>adCmdText</strong></span></span></p></td>
<td><p><span data-ttu-id="e8322-112">1,1</span><span class="sxs-lookup"><span data-stu-id="e8322-112">1</span></span></p></td>
<td><p><span data-ttu-id="e8322-113">Вычисляет значение <a href="commandtext-property-ado.md">CommandText</a> в качестве текстового определения команды или вызова хранимой процедуры.</span><span class="sxs-lookup"><span data-stu-id="e8322-113">Evaluates <a href="commandtext-property-ado.md">CommandText</a> as a textual definition of a command or stored procedure call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8322-114"><strong>адкмдтабле</strong></span><span class="sxs-lookup"><span data-stu-id="e8322-114"><strong>adCmdTable</strong></span></span></p></td>
<td><p><span data-ttu-id="e8322-115">2</span><span class="sxs-lookup"><span data-stu-id="e8322-115">2</span></span></p></td>
<td><p><span data-ttu-id="e8322-116">Оценивает свойство <strong>CommandText</strong> как имя таблицы, столбцы которой возвращаются внутренним запросом SQL.</span><span class="sxs-lookup"><span data-stu-id="e8322-116">Evaluates <strong>CommandText</strong> as a table name whose columns are all returned by an internally generated SQL query.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8322-117"><strong>адкмдсторедпрок</strong></span><span class="sxs-lookup"><span data-stu-id="e8322-117"><strong>adCmdStoredProc</strong></span></span></p></td>
<td><p><span data-ttu-id="e8322-118">4 </span><span class="sxs-lookup"><span data-stu-id="e8322-118">4</span></span></p></td>
<td><p><span data-ttu-id="e8322-119">Вычисляет значение <strong>CommandText</strong> в качестве имени хранимой процедуры.</span><span class="sxs-lookup"><span data-stu-id="e8322-119">Evaluates <strong>CommandText</strong> as a stored procedure name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8322-120"><strong>адкмдункновн</strong></span><span class="sxs-lookup"><span data-stu-id="e8322-120"><strong>adCmdUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="e8322-121">8 </span><span class="sxs-lookup"><span data-stu-id="e8322-121">8</span></span></p></td>
<td><p><span data-ttu-id="e8322-122">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e8322-122">Default.</span></span> <span data-ttu-id="e8322-123">Указывает, что тип команды в свойстве <strong>CommandText</strong> неизвестен.</span><span class="sxs-lookup"><span data-stu-id="e8322-123">Indicates that the type of command in the <strong>CommandText</strong> property is not known.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8322-124"><strong>адкмдфиле</strong></span><span class="sxs-lookup"><span data-stu-id="e8322-124"><strong>adCmdFile</strong></span></span></p></td>
<td><p><span data-ttu-id="e8322-125">256</span><span class="sxs-lookup"><span data-stu-id="e8322-125">256</span></span></p></td>
<td><p><span data-ttu-id="e8322-126">Вычисляет значение <strong>CommandText</strong> в качестве имени файла сохраняемого сохраняемого <a href="recordset-object-ado.md">набора записей</a>.</span><span class="sxs-lookup"><span data-stu-id="e8322-126">Evaluates <strong>CommandText</strong> as the file name of a persistently stored <a href="recordset-object-ado.md">Recordset</a>.</span></span> <span data-ttu-id="e8322-127">Используется с <strong>Recordset.</strong> Только для <a href="open-method-ado-recordset.md">открытия или повторного</a> <a href="requery-method-ado.md">запроса</a> .</span><span class="sxs-lookup"><span data-stu-id="e8322-127">Used with <strong>Recordset.</strong><a href="open-method-ado-recordset.md">Open</a> or <a href="requery-method-ado.md">Requery</a> only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8322-128"><strong>адкмдтабледирект</strong></span><span class="sxs-lookup"><span data-stu-id="e8322-128"><strong>adCmdTableDirect</strong></span></span></p></td>
<td><p><span data-ttu-id="e8322-129">512</span><span class="sxs-lookup"><span data-stu-id="e8322-129">512</span></span></p></td>
<td><p><span data-ttu-id="e8322-130">Оценивает свойство <strong>CommandText</strong> как имя таблицы, в которой возвращаются все столбцы.</span><span class="sxs-lookup"><span data-stu-id="e8322-130">Evaluates <strong>CommandText</strong> as a table name whose columns are all returned.</span></span> <span data-ttu-id="e8322-131">Используется с параметром <strong>Recordset. Open</strong> или <strong>Requery</strong> only.</span><span class="sxs-lookup"><span data-stu-id="e8322-131">Used with <strong>Recordset.Open</strong> or <strong>Requery</strong> only.</span></span> <span data-ttu-id="e8322-132">Чтобы использовать метод <a href="seek-method-ado.md">Seek</a> , необходимо открыть объект <strong>Recordset</strong> с помощью <strong>адкмдтабледирект</strong>.</span><span class="sxs-lookup"><span data-stu-id="e8322-132">To use the <a href="seek-method-ado.md">Seek</a> method, the <strong>Recordset</strong> must be opened with <strong>adCmdTableDirect</strong>.</span></span> <span data-ttu-id="e8322-133">Это значение не может сочетаться со <a href="executeoptionenum.md">ExecuteOptionEnum</a> значением ексекутеоптионенум <strong>адасинцексекуте</strong>.</span><span class="sxs-lookup"><span data-stu-id="e8322-133">This value cannot be combined with the <a href="executeoptionenum.md">ExecuteOptionEnum</a> value <strong>adAsyncExecute</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="e8322-134">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="e8322-134">ADO/WFC equivalent</span></span>

<span data-ttu-id="e8322-135">Пакет: **com. MS. WFC. Data**</span><span class="sxs-lookup"><span data-stu-id="e8322-135">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e8322-136">Константа</span><span class="sxs-lookup"><span data-stu-id="e8322-136">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e8322-137">Адоенумс. CommandType. unspecifiedо</span><span class="sxs-lookup"><span data-stu-id="e8322-137">AdoEnums.CommandType.UNSPECIFIED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8322-138">Адоенумс. CommandType. TEXT</span><span class="sxs-lookup"><span data-stu-id="e8322-138">AdoEnums.CommandType.TEXT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8322-139">Адоенумс. CommandType. TABLE</span><span class="sxs-lookup"><span data-stu-id="e8322-139">AdoEnums.CommandType.TABLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8322-140">Адоенумс. CommandType. СТОРЕДПРОК</span><span class="sxs-lookup"><span data-stu-id="e8322-140">AdoEnums.CommandType.STOREDPROC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8322-141">Адоенумс. CommandType. UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="e8322-141">AdoEnums.CommandType.UNKNOWN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8322-142">Адоенумс. CommandType. FILE</span><span class="sxs-lookup"><span data-stu-id="e8322-142">AdoEnums.CommandType.FILE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8322-143">Адоенумс. CommandType. TABLEDIRECT</span><span class="sxs-lookup"><span data-stu-id="e8322-143">AdoEnums.CommandType.TABLEDIRECT</span></span></p></td>
</tr>
</tbody>
</table>

