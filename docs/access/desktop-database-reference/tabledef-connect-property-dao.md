---
title: Свойство TableDef.Connect (DAO)
TOCTitle: Connect Property
ms:assetid: 4fbb324c-a358-8fad-60f2-fb8005cf74d9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193791(v=office.15)
ms:contentKeyID: 48544782
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053064
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 2d8aef3c8bdaac93bd84231b3098d98ee896a81f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722755"
---
# <a name="tabledefconnect-property-dao"></a><span data-ttu-id="01861-102">Свойство TableDef.Connect (DAO)</span><span class="sxs-lookup"><span data-stu-id="01861-102">TableDef.Connect Property (DAO)</span></span>

<span data-ttu-id="01861-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="01861-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="01861-104">Задает или возвращает значение, которое содержит сведения о связанной таблице.</span><span class="sxs-lookup"><span data-stu-id="01861-104">Sets or returns a value that provides information about a linked table.</span></span> <span data-ttu-id="01861-105">Для чтения и записи, **String**.</span><span class="sxs-lookup"><span data-stu-id="01861-105">Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="01861-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="01861-106">Syntax</span></span>

<span data-ttu-id="01861-107">*expression* .Connect</span><span class="sxs-lookup"><span data-stu-id="01861-107">*expression* .Connect</span></span>

<span data-ttu-id="01861-108">*выражение*: переменная, представляющая объект **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="01861-108">*expression* A variable that represents a **FileDialog** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="01861-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="01861-109">Remarks</span></span>

<span data-ttu-id="01861-110">Параметры свойства **Connect** сохранены в **String**, состоящей из указателя типа базы данных и нуля либо нескольких параметров, разделенных точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="01861-110">The **Connect** property setting is a **String** composed of a database type specifier and zero or more parameters separated by semicolons.</span></span> <span data-ttu-id="01861-111">Свойство **Connect** передает дополнительные сведения для ODBC и определенным драйверам ISAM при необходимости.</span><span class="sxs-lookup"><span data-stu-id="01861-111">The **Connect** property passes additional information to ODBC and certain ISAM drivers as needed.</span></span>

<span data-ttu-id="01861-112">Для объекта **TableDef**, представляющего связанную таблицу, параметры свойства **Connect** состоит из одной или двух частей (указатель типа базы данных и путь к базе данных), каждый из которых заканчивается точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="01861-112">For a **TableDef** object that represents a linked table, the **Connect** property setting consists of one or two parts (a database type specifier and a path to the database), each of which ends with a semicolon.</span></span>

<span data-ttu-id="01861-113">Путь, как показано в приведенной ниже таблице, содержит полный путь к каталогу, содержащему файлы базы данных, и должен иметь впереди идентификатор DATABASE=.</span><span class="sxs-lookup"><span data-stu-id="01861-113">The path as shown in the following table is the full path for the directory containing the database files and must be preceded by the identifier DATABASE=.</span></span> <span data-ttu-id="01861-114">В некоторых случаях (как в случае с базами данных Microsoft Excel и ядра СУБД Microsoft Access) следует включить конкретное имя файла в аргумент пути к базе данных.</span><span class="sxs-lookup"><span data-stu-id="01861-114">In some cases (as with Microsoft Excel and Microsoft Access database engine databases), you should include a specific file name in the database path argument.</span></span>

<span data-ttu-id="01861-115">Таблица ниже содержит возможные типы базы данных и соответствующие указатели базы данных и пути к параметрам свойства **Connect**.</span><span class="sxs-lookup"><span data-stu-id="01861-115">The following table shows possible database types and their corresponding database specifiers and paths for the **Connect** property setting.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="01861-116">Тип базы данных</span><span class="sxs-lookup"><span data-stu-id="01861-116">Database type</span></span></p></th>
<th><p><span data-ttu-id="01861-117">Указатель</span><span class="sxs-lookup"><span data-stu-id="01861-117">Specifier</span></span></p></th>
<th><p><span data-ttu-id="01861-118">Пример</span><span class="sxs-lookup"><span data-stu-id="01861-118">Example</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="01861-119">База данных Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="01861-119">Microsoft Access Database</span></span></p></td>
<td><p><span data-ttu-id="01861-120">[database];</span><span class="sxs-lookup"><span data-stu-id="01861-120">Database</span></span></p></td>
<td><p><span data-ttu-id="01861-121">диск: \путь\имяфайла</span><span class="sxs-lookup"><span data-stu-id="01861-121">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01861-122">dBASE III</span><span class="sxs-lookup"><span data-stu-id="01861-122">dBASE III</span></span></p></td>
<td><p><span data-ttu-id="01861-123">dBASE III;</span><span class="sxs-lookup"><span data-stu-id="01861-123">dBASE III;</span></span></p></td>
<td><p><span data-ttu-id="01861-124">диск: \путь</span><span class="sxs-lookup"><span data-stu-id="01861-124">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01861-125">dBASE IV</span><span class="sxs-lookup"><span data-stu-id="01861-125">dBASE IV</span></span></p></td>
<td><p><span data-ttu-id="01861-126">dBASE IV;</span><span class="sxs-lookup"><span data-stu-id="01861-126">dBASE IV;</span></span></p></td>
<td><p><span data-ttu-id="01861-127">диск: \путь</span><span class="sxs-lookup"><span data-stu-id="01861-127">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01861-128">dBASE 5</span><span class="sxs-lookup"><span data-stu-id="01861-128">dBASE 5</span></span></p></td>
<td><p><span data-ttu-id="01861-129">dBASE 5.0;</span><span class="sxs-lookup"><span data-stu-id="01861-129">dBASE 5.0;</span></span></p></td>
<td><p><span data-ttu-id="01861-130">диск: \путь</span><span class="sxs-lookup"><span data-stu-id="01861-130">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01861-131">Paradox 3.x</span><span class="sxs-lookup"><span data-stu-id="01861-131">Paradox 3.x</span></span></p></td>
<td><p><span data-ttu-id="01861-132">Paradox 3.x;</span><span class="sxs-lookup"><span data-stu-id="01861-132">Paradox 3.x;</span></span></p></td>
<td><p><span data-ttu-id="01861-133">диск: \путь</span><span class="sxs-lookup"><span data-stu-id="01861-133">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01861-134">Paradox 4.x</span><span class="sxs-lookup"><span data-stu-id="01861-134">Paradox 4.x</span></span></p></td>
<td><p><span data-ttu-id="01861-135">Paradox 4.x;</span><span class="sxs-lookup"><span data-stu-id="01861-135">Paradox 4.x;</span></span></p></td>
<td><p><span data-ttu-id="01861-136">диск: \путь</span><span class="sxs-lookup"><span data-stu-id="01861-136">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01861-137">Paradox 5.x</span><span class="sxs-lookup"><span data-stu-id="01861-137">Paradox 5.x</span></span></p></td>
<td><p><span data-ttu-id="01861-138">Paradox 5.x;</span><span class="sxs-lookup"><span data-stu-id="01861-138">Paradox 5.x;</span></span></p></td>
<td><p><span data-ttu-id="01861-139">диск: \путь</span><span class="sxs-lookup"><span data-stu-id="01861-139">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01861-140">Microsoft Excel 3.0</span><span class="sxs-lookup"><span data-stu-id="01861-140">Microsoft Excel 3.0</span></span></p></td>
<td><p><span data-ttu-id="01861-141">Excel 3.0;</span><span class="sxs-lookup"><span data-stu-id="01861-141">Excel 3.0;</span></span></p></td>
<td><p><span data-ttu-id="01861-142">диск: \путь\имяфайла.xls</span><span class="sxs-lookup"><span data-stu-id="01861-142">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01861-143">Microsoft Excel 4.0</span><span class="sxs-lookup"><span data-stu-id="01861-143">Microsoft Excel 4.0</span></span></p></td>
<td><p><span data-ttu-id="01861-144">Excel 4.0;</span><span class="sxs-lookup"><span data-stu-id="01861-144">Excel 4.0;</span></span></p></td>
<td><p><span data-ttu-id="01861-145">диск: \путь\имяфайла.xls</span><span class="sxs-lookup"><span data-stu-id="01861-145">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01861-146">Microsoft Excel 5.0 или Microsoft Excel 95</span><span class="sxs-lookup"><span data-stu-id="01861-146">Microsoft Excel 5.0 or Microsoft Excel 95</span></span></p></td>
<td><p><span data-ttu-id="01861-147">Excel 5.0;</span><span class="sxs-lookup"><span data-stu-id="01861-147">Excel 5.0;</span></span></p></td>
<td><p><span data-ttu-id="01861-148">диск: \путь\имяфайла.xls</span><span class="sxs-lookup"><span data-stu-id="01861-148">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01861-149">Microsoft Excel 97</span><span class="sxs-lookup"><span data-stu-id="01861-149">Microsoft Excel 97</span></span></p></td>
<td><p><span data-ttu-id="01861-150">Excel 8.0;</span><span class="sxs-lookup"><span data-stu-id="01861-150">Excel 8.0;</span></span></p></td>
<td><p><span data-ttu-id="01861-151">диск: \путь\имяфайла.xls</span><span class="sxs-lookup"><span data-stu-id="01861-151">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01861-152">Lotus 1-2-3 WKS и WK1</span><span class="sxs-lookup"><span data-stu-id="01861-152">Lotus 1-2-3 WKS and WK1</span></span></p></td>
<td><p><span data-ttu-id="01861-153">Lotus WK1;</span><span class="sxs-lookup"><span data-stu-id="01861-153">Lotus WK1;</span></span></p></td>
<td><p><span data-ttu-id="01861-154">диск: \путь\имяфайла.wk1</span><span class="sxs-lookup"><span data-stu-id="01861-154">drive:\path\filename.wk1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01861-155">Lotus 1-2-3 WK3</span><span class="sxs-lookup"><span data-stu-id="01861-155">Lotus 1-2-3 WK3</span></span></p></td>
<td><p><span data-ttu-id="01861-156">Lotus WK3;</span><span class="sxs-lookup"><span data-stu-id="01861-156">Lotus WK3;</span></span></p></td>
<td><p><span data-ttu-id="01861-157">диск: \путь\имяфайла.wk3</span><span class="sxs-lookup"><span data-stu-id="01861-157">drive:\path\filename.wk3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01861-158">Lotus 1-2-3 WK4</span><span class="sxs-lookup"><span data-stu-id="01861-158">Lotus 1-2-3 WK4</span></span></p></td>
<td><p><span data-ttu-id="01861-159">Lotus WK4;</span><span class="sxs-lookup"><span data-stu-id="01861-159">Lotus WK4;</span></span></p></td>
<td><p><span data-ttu-id="01861-160">диск: \путь\имяфайла.wk4</span><span class="sxs-lookup"><span data-stu-id="01861-160">drive:\path\filename.wk4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01861-161">HTML Import</span><span class="sxs-lookup"><span data-stu-id="01861-161">HTML Import</span></span></p></td>
<td><p><span data-ttu-id="01861-162">HTML Import;</span><span class="sxs-lookup"><span data-stu-id="01861-162">HTML Import;</span></span></p></td>
<td><p><span data-ttu-id="01861-163">диск: \путь\имяфайла</span><span class="sxs-lookup"><span data-stu-id="01861-163">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01861-164">HTML Export</span><span class="sxs-lookup"><span data-stu-id="01861-164">HTML Export</span></span></p></td>
<td><p><span data-ttu-id="01861-165">HTML Export;</span><span class="sxs-lookup"><span data-stu-id="01861-165">HTML Export;</span></span></p></td>
<td><p><span data-ttu-id="01861-166">диск: \путь</span><span class="sxs-lookup"><span data-stu-id="01861-166">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01861-167">Text</span><span class="sxs-lookup"><span data-stu-id="01861-167">Text</span></span></p></td>
<td><p><span data-ttu-id="01861-168">Text;</span><span class="sxs-lookup"><span data-stu-id="01861-168">Text</span></span></p></td>
<td><p><span data-ttu-id="01861-169">диск: \путь</span><span class="sxs-lookup"><span data-stu-id="01861-169">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01861-170">ODBC</span><span class="sxs-lookup"><span data-stu-id="01861-170">ODBC</span></span></p></td>
<td><p><span data-ttu-id="01861-171">ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</span><span class="sxs-lookup"><span data-stu-id="01861-171">ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</span></span></p></td>
<td><p><span data-ttu-id="01861-172">Нет</span><span class="sxs-lookup"><span data-stu-id="01861-172">None</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01861-173">Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="01861-173">Microsoft Exchange</span></span></p></td>
<td><p><span data-ttu-id="01861-174">Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</span><span class="sxs-lookup"><span data-stu-id="01861-174">Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</span></span></p></td>
<td><p><span data-ttu-id="01861-175">диск: \путь\имяфайла</span><span class="sxs-lookup"><span data-stu-id="01861-175">drive:\path\filename</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="01861-176">Если пароль необходим, но не указан в параметрах свойства **Connect**, диалоговое окно входа отображается при первой попытке доступа к таблице со стороны драйвера ODBC и еще раз при закрытии и повторном установлении подключения.</span><span class="sxs-lookup"><span data-stu-id="01861-176">If a password is required but not provided in the **Connect** property setting, a login dialog box is displayed the first time a table is accessed by the ODBC driver and again if the connection is closed and reopened.</span></span>

<span data-ttu-id="01861-177">Для данных в Microsoft Exchange обязательный ключ MAPILEVEL должен иметь полностью разрешенный путь к папке (например, "Mailbox - Pat SmithIAlpha/Today").</span><span class="sxs-lookup"><span data-stu-id="01861-177">For data in Microsoft Exchange, the required MAPILEVEL key should be set to a fully-resolved folder path (for example, "Mailbox - Pat SmithIAlpha/Today").</span></span> <span data-ttu-id="01861-178">Путь не включает имя папки, которая будет открываться в качестве таблицы; вместо этого необходимо указать имя этой папки в качестве имени аргумента для метода **CreateTable**.</span><span class="sxs-lookup"><span data-stu-id="01861-178">The path does not include the name of the folder that will be opened as a table; that folder’s name should instead be specified as the name argument to the **CreateTable** method.</span></span> <span data-ttu-id="01861-179">Для ключа TABLETYPE должно быть установлено значение «0», чтобы открыть папку (по умолчанию) или «1», чтобы открыть адресную книгу.</span><span class="sxs-lookup"><span data-stu-id="01861-179">The TABLETYPE key should be set to "0" to open a folder (default) or "1" to open an address book.</span></span> <span data-ttu-id="01861-180">Ключ PROFILE по умолчанию относится к профилю, который в настоящее время используется.</span><span class="sxs-lookup"><span data-stu-id="01861-180">The PROFILE key defaults to the profile currently in use.</span></span>

<span data-ttu-id="01861-181">Для базовых таблиц в базе данных Micorosoft Access параметр свойства **Connect** должен быть строкой нулевой длины ("").</span><span class="sxs-lookup"><span data-stu-id="01861-181">For base tables in a Micorosoft Access database, the **Connect** property setting is a zero-length string ("").</span></span>

> [!NOTE]
> - <span data-ttu-id="01861-182">Необходимо задать значение свойства **Connect** перед настройкой свойства **ReturnsRecords**.</span><span class="sxs-lookup"><span data-stu-id="01861-182">You must set the **Connect** property before you set the **ReturnsRecords** property.</span></span>
> - <span data-ttu-id="01861-183">Необходимо иметь разрешения на доступ к компьютеру, который содержит сервер базы данных, доступ к которому вы пытаетесь получить доступ.</span><span class="sxs-lookup"><span data-stu-id="01861-183">You must have access permissions to the computer that contains the database server you're trying to access.</span></span>
