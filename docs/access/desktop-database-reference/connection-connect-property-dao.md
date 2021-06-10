---
title: Подключение. Подключение (DAO)
TOCTitle: Connect Property
ms:assetid: 58b514a2-91cd-7918-cba5-15d71c2457a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194335(v=office.15)
ms:contentKeyID: 48545001
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e44ce5b4acf58f3f9d9e887d0136baed64c8e227
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295928"
---
# <a name="connectionconnect-property-dao"></a><span data-ttu-id="0719b-102">Подключение. Подключение (DAO)</span><span class="sxs-lookup"><span data-stu-id="0719b-102">Connection.Connect property (DAO)</span></span>


<span data-ttu-id="0719b-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0719b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0719b-104">Задает или возвращает значение, которое предоставляет сведения об источнике открытого подключения.</span><span class="sxs-lookup"><span data-stu-id="0719b-104">Sets or returns a value that provides information about the source of an open connection.</span></span> <span data-ttu-id="0719b-105">Для чтения и записи, **String**.</span><span class="sxs-lookup"><span data-stu-id="0719b-105">Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="0719b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0719b-106">Syntax</span></span>

<span data-ttu-id="0719b-107">*expression* .Connect</span><span class="sxs-lookup"><span data-stu-id="0719b-107">*expression* .Connect</span></span>

<span data-ttu-id="0719b-108">*выражение*: переменная, представляющая объект **Connection**.</span><span class="sxs-lookup"><span data-stu-id="0719b-108">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0719b-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="0719b-109">Remarks</span></span>

<span data-ttu-id="0719b-110">Параметры свойства **Connect** сохранены в **String**, состоящей из указателя типа базы данных и нуля либо нескольких параметров, разделенных точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="0719b-110">The **Connect** property setting is a **String** composed of a database type specifier and zero or more parameters separated by semicolons.</span></span> <span data-ttu-id="0719b-111">Свойство **Connect** передает дополнительные сведения для ODBC и определенным драйверам ISAM при необходимости.</span><span class="sxs-lookup"><span data-stu-id="0719b-111">The **Connect** property passes additional information to ODBC and certain ISAM drivers as needed.</span></span>

<span data-ttu-id="0719b-112">Чтобы выполнить SQL сквозной запрос на таблице, связанной с файлом базы данных  Microsoft Access, сначала необходимо Подключение свойству базы данных связанной таблицы допустимую строку подключения ODBC.</span><span class="sxs-lookup"><span data-stu-id="0719b-112">To perform an SQL pass-through query on a table linked to your Microsoft Access database file, you must first set the **Connect** property of the linked table's database to a valid ODBC connection string.</span></span>

<span data-ttu-id="0719b-113">Для объекта **TableDef**, представляющего связанную таблицу, параметры свойства **Connect** состоит из одной или двух частей (указатель типа базы данных и путь к базе данных), каждый из которых заканчивается точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="0719b-113">For a **TableDef** object that represents a linked table, the **Connect** property setting consists of one or two parts (a database type specifier and a path to the database), each of which ends with a semicolon.</span></span>

<span data-ttu-id="0719b-114">Путь, как показано в приведенной ниже таблице, содержит полный путь к каталогу, содержащему файлы базы данных, и должен иметь впереди идентификатор DATABASE=.</span><span class="sxs-lookup"><span data-stu-id="0719b-114">The path as shown in the following table is the full path for the directory containing the database files and must be preceded by the identifier DATABASE=.</span></span> <span data-ttu-id="0719b-115">В некоторых случаях (как в случае с базами данных Microsoft Excel и ядра СУБД Microsoft Access) следует включить конкретное имя файла в аргумент пути к базе данных.</span><span class="sxs-lookup"><span data-stu-id="0719b-115">In some cases (as with Microsoft Excel and Microsoft Access database engine databases), you should include a specific file name in the database path argument.</span></span>

<span data-ttu-id="0719b-116">Таблица ниже содержит возможные типы базы данных и соответствующие указатели базы данных и пути к параметрам свойства **Connect**.</span><span class="sxs-lookup"><span data-stu-id="0719b-116">The following table shows possible database types and their corresponding database specifiers and paths for the **Connect** property setting.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0719b-117">Тип базы данных</span><span class="sxs-lookup"><span data-stu-id="0719b-117">Database type</span></span></p></th>
<th><p><span data-ttu-id="0719b-118">Указатель</span><span class="sxs-lookup"><span data-stu-id="0719b-118">Specifier</span></span></p></th>
<th><p><span data-ttu-id="0719b-119">Пример</span><span class="sxs-lookup"><span data-stu-id="0719b-119">Example</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0719b-120">База данных Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="0719b-120">Microsoft Access Database</span></span></p></td>
<td><p><span data-ttu-id="0719b-121">[database];</span><span class="sxs-lookup"><span data-stu-id="0719b-121">[database];</span></span></p></td>
<td><p><span data-ttu-id="0719b-122">диск: \путь\имяфайла</span><span class="sxs-lookup"><span data-stu-id="0719b-122">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0719b-123">dBASE III</span><span class="sxs-lookup"><span data-stu-id="0719b-123">dBASE III</span></span></p></td>
<td><p><span data-ttu-id="0719b-124">dBASE III;</span><span class="sxs-lookup"><span data-stu-id="0719b-124">dBASE III;</span></span></p></td>
<td><p><span data-ttu-id="0719b-125">диск: \путь</span><span class="sxs-lookup"><span data-stu-id="0719b-125">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0719b-126">dBASE IV</span><span class="sxs-lookup"><span data-stu-id="0719b-126">dBASE IV</span></span></p></td>
<td><p><span data-ttu-id="0719b-127">dBASE IV;</span><span class="sxs-lookup"><span data-stu-id="0719b-127">dBASE IV;</span></span></p></td>
<td><p><span data-ttu-id="0719b-128">диск: \путь</span><span class="sxs-lookup"><span data-stu-id="0719b-128">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0719b-129">dBASE 5</span><span class="sxs-lookup"><span data-stu-id="0719b-129">dBASE 5</span></span></p></td>
<td><p><span data-ttu-id="0719b-130">dBASE 5.0;</span><span class="sxs-lookup"><span data-stu-id="0719b-130">dBASE 5.0;</span></span></p></td>
<td><p><span data-ttu-id="0719b-131">диск: \путь</span><span class="sxs-lookup"><span data-stu-id="0719b-131">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0719b-132">Paradox 3.x</span><span class="sxs-lookup"><span data-stu-id="0719b-132">Paradox 3.x</span></span></p></td>
<td><p><span data-ttu-id="0719b-133">Paradox 3.x;</span><span class="sxs-lookup"><span data-stu-id="0719b-133">Paradox 3.x;</span></span></p></td>
<td><p><span data-ttu-id="0719b-134">диск: \путь</span><span class="sxs-lookup"><span data-stu-id="0719b-134">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0719b-135">Paradox 4.x</span><span class="sxs-lookup"><span data-stu-id="0719b-135">Paradox 4.x</span></span></p></td>
<td><p><span data-ttu-id="0719b-136">Paradox 4.x;</span><span class="sxs-lookup"><span data-stu-id="0719b-136">Paradox 4.x;</span></span></p></td>
<td><p><span data-ttu-id="0719b-137">диск: \путь</span><span class="sxs-lookup"><span data-stu-id="0719b-137">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0719b-138">Paradox 5.x</span><span class="sxs-lookup"><span data-stu-id="0719b-138">Paradox 5.x</span></span></p></td>
<td><p><span data-ttu-id="0719b-139">Paradox 5.x;</span><span class="sxs-lookup"><span data-stu-id="0719b-139">Paradox 5.x;</span></span></p></td>
<td><p><span data-ttu-id="0719b-140">диск: \путь</span><span class="sxs-lookup"><span data-stu-id="0719b-140">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0719b-141">Microsoft Excel 3.0</span><span class="sxs-lookup"><span data-stu-id="0719b-141">Microsoft Excel 3.0</span></span></p></td>
<td><p><span data-ttu-id="0719b-142">Excel 3.0;</span><span class="sxs-lookup"><span data-stu-id="0719b-142">Excel 3.0;</span></span></p></td>
<td><p><span data-ttu-id="0719b-143">диск: \путь\имяфайла.xls</span><span class="sxs-lookup"><span data-stu-id="0719b-143">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0719b-144">Microsoft Excel 4.0</span><span class="sxs-lookup"><span data-stu-id="0719b-144">Microsoft Excel 4.0</span></span></p></td>
<td><p><span data-ttu-id="0719b-145">Excel 4.0;</span><span class="sxs-lookup"><span data-stu-id="0719b-145">Excel 4.0;</span></span></p></td>
<td><p><span data-ttu-id="0719b-146">диск: \путь\имяфайла.xls</span><span class="sxs-lookup"><span data-stu-id="0719b-146">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0719b-147">Microsoft Excel 5.0 или Microsoft Excel 95</span><span class="sxs-lookup"><span data-stu-id="0719b-147">Microsoft Excel 5.0 or Microsoft Excel 95</span></span></p></td>
<td><p><span data-ttu-id="0719b-148">Excel 5.0;</span><span class="sxs-lookup"><span data-stu-id="0719b-148">Excel 5.0;</span></span></p></td>
<td><p><span data-ttu-id="0719b-149">диск: \путь\имяфайла.xls</span><span class="sxs-lookup"><span data-stu-id="0719b-149">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0719b-150">Microsoft Excel 97</span><span class="sxs-lookup"><span data-stu-id="0719b-150">Microsoft Excel 97</span></span></p></td>
<td><p><span data-ttu-id="0719b-151">Excel 8.0;</span><span class="sxs-lookup"><span data-stu-id="0719b-151">Excel 8.0;</span></span></p></td>
<td><p><span data-ttu-id="0719b-152">диск: \путь\имяфайла.xls</span><span class="sxs-lookup"><span data-stu-id="0719b-152">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0719b-153">Lotus 1-2-3 WKS и WK1</span><span class="sxs-lookup"><span data-stu-id="0719b-153">Lotus 1-2-3 WKS and WK1</span></span></p></td>
<td><p><span data-ttu-id="0719b-154">Lotus WK1;</span><span class="sxs-lookup"><span data-stu-id="0719b-154">Lotus WK1;</span></span></p></td>
<td><p><span data-ttu-id="0719b-155">диск: \путь\имяфайла.wk1</span><span class="sxs-lookup"><span data-stu-id="0719b-155">drive:\path\filename.wk1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0719b-156">Lotus 1-2-3 WK3</span><span class="sxs-lookup"><span data-stu-id="0719b-156">Lotus 1-2-3 WK3</span></span></p></td>
<td><p><span data-ttu-id="0719b-157">Lotus WK3;</span><span class="sxs-lookup"><span data-stu-id="0719b-157">Lotus WK3;</span></span></p></td>
<td><p><span data-ttu-id="0719b-158">диск: \путь\имяфайла.wk3</span><span class="sxs-lookup"><span data-stu-id="0719b-158">drive:\path\filename.wk3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0719b-159">Lotus 1-2-3 WK4</span><span class="sxs-lookup"><span data-stu-id="0719b-159">Lotus 1-2-3 WK4</span></span></p></td>
<td><p><span data-ttu-id="0719b-160">Lotus WK4;</span><span class="sxs-lookup"><span data-stu-id="0719b-160">Lotus WK4;</span></span></p></td>
<td><p><span data-ttu-id="0719b-161">диск: \путь\имяфайла.wk4</span><span class="sxs-lookup"><span data-stu-id="0719b-161">drive:\path\filename.wk4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0719b-162">HTML Import</span><span class="sxs-lookup"><span data-stu-id="0719b-162">HTML Import</span></span></p></td>
<td><p><span data-ttu-id="0719b-163">HTML Import;</span><span class="sxs-lookup"><span data-stu-id="0719b-163">HTML Import;</span></span></p></td>
<td><p><span data-ttu-id="0719b-164">диск: \путь\имяфайла</span><span class="sxs-lookup"><span data-stu-id="0719b-164">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0719b-165">HTML Export</span><span class="sxs-lookup"><span data-stu-id="0719b-165">HTML Export</span></span></p></td>
<td><p><span data-ttu-id="0719b-166">HTML Export;</span><span class="sxs-lookup"><span data-stu-id="0719b-166">HTML Export;</span></span></p></td>
<td><p><span data-ttu-id="0719b-167">диск: \путь</span><span class="sxs-lookup"><span data-stu-id="0719b-167">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0719b-168">Text</span><span class="sxs-lookup"><span data-stu-id="0719b-168">Text</span></span></p></td>
<td><p><span data-ttu-id="0719b-169">Text;</span><span class="sxs-lookup"><span data-stu-id="0719b-169">Text;</span></span></p></td>
<td><p><span data-ttu-id="0719b-170">диск: \путь</span><span class="sxs-lookup"><span data-stu-id="0719b-170">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0719b-171">ODBC</span><span class="sxs-lookup"><span data-stu-id="0719b-171">ODBC</span></span></p></td>
<td><p><span data-ttu-id="0719b-172">ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</span><span class="sxs-lookup"><span data-stu-id="0719b-172">ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</span></span></p></td>
<td><p><span data-ttu-id="0719b-173">Нет</span><span class="sxs-lookup"><span data-stu-id="0719b-173">None</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0719b-174">Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="0719b-174">Microsoft Exchange</span></span></p></td>
<td><p><span data-ttu-id="0719b-175">Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</span><span class="sxs-lookup"><span data-stu-id="0719b-175">Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</span></span></p></td>
<td><p><span data-ttu-id="0719b-176">диск: \путь\имяфайла</span><span class="sxs-lookup"><span data-stu-id="0719b-176">drive:\path\filename</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0719b-177">Если указание только "ODBC;", драйвер ODBC отображает диалоговое окно с перечислением всех зарегистрированных имен источников данных ODBC, чтобы пользователь мог выбрать базу данных.</span><span class="sxs-lookup"><span data-stu-id="0719b-177">If the specifier is only "ODBC;", the ODBC driver displays a dialog box listing all registered ODBC data source names so that the user can select a database.</span></span>

<span data-ttu-id="0719b-178">Если пароль необходим, но не указан в параметрах свойства **Connect**, диалоговое окно входа отображается при первой попытке доступа к таблице со стороны драйвера ODBC и еще раз при закрытии и повторном установлении подключения.</span><span class="sxs-lookup"><span data-stu-id="0719b-178">If a password is required but not provided in the **Connect** property setting, a login dialog box is displayed the first time a table is accessed by the ODBC driver and again if the connection is closed and reopened.</span></span>

<span data-ttu-id="0719b-179">Для данных в Microsoft Exchange обязательный ключ MAPILEVEL должен иметь полностью разрешенный путь к папке (например, "Mailbox - Pat SmithIAlpha/Today").</span><span class="sxs-lookup"><span data-stu-id="0719b-179">For data in Microsoft Exchange, the required MAPILEVEL key should be set to a fully-resolved folder path (for example, "Mailbox - Pat SmithIAlpha/Today").</span></span> <span data-ttu-id="0719b-180">Путь не включает имя папки, которая будет открываться в качестве таблицы; вместо этого необходимо указать имя этой папки в качестве имени аргумента для метода **CreateTable**.</span><span class="sxs-lookup"><span data-stu-id="0719b-180">The path does not include the name of the folder that will be opened as a table; that folder’s name should instead be specified as the name argument to the **CreateTable** method.</span></span> <span data-ttu-id="0719b-181">Для ключа TABLETYPE должно быть установлено значение «0», чтобы открыть папку (по умолчанию) или «1», чтобы открыть адресную книгу.</span><span class="sxs-lookup"><span data-stu-id="0719b-181">The TABLETYPE key should be set to "0" to open a folder (default) or "1" to open an address book.</span></span> <span data-ttu-id="0719b-182">Ключ PROFILE по умолчанию относится к профилю, который в настоящее время используется.</span><span class="sxs-lookup"><span data-stu-id="0719b-182">The PROFILE key defaults to the profile currently in use.</span></span>

<span data-ttu-id="0719b-183">Для базовых таблиц в базе данных Micorosoft Access параметр свойства **Connect** должен быть строкой нулевой длины ("").</span><span class="sxs-lookup"><span data-stu-id="0719b-183">For base tables in a Micorosoft Access database, the **Connect** property setting is a zero-length string ("").</span></span>

<span data-ttu-id="0719b-184">Вы можете Подключение **для** объекта **Базы** данных, предоставив исходный аргумент **методу OpenDatabase.**</span><span class="sxs-lookup"><span data-stu-id="0719b-184">You can set the **Connect** property for a **Database** object by providing a source argument to the **OpenDatabase** method.</span></span> <span data-ttu-id="0719b-185">Вы можете проверить параметр, чтобы определить тип, путь, код пользователя, пароль или источник данных ODBC базы данных.</span><span class="sxs-lookup"><span data-stu-id="0719b-185">You can check the setting to determine the type, path, user ID, password, or ODBC data source of the database.</span></span>

<span data-ttu-id="0719b-186">На **объекте QueryDef** в рабочей области Microsoft Access можно использовать свойство **Подключение** с свойством ReturnsRecords для создания сквозного запроса SQL ODBC.</span><span class="sxs-lookup"><span data-stu-id="0719b-186">On a **QueryDef** object in a Microsoft Access workspace, you can use the **Connect** property with the ReturnsRecords property to create an ODBC SQL pass-through query.</span></span> <span data-ttu-id="0719b-187">Тип базы данных строки подключения — "ODBC;", а остальная строка содержит сведения, определенные драйверу ODBC, используемой для доступа к удаленным данным.</span><span class="sxs-lookup"><span data-stu-id="0719b-187">The databasetype of the connection string is "ODBC;", and the remainder of the string contains information specific to the ODBC driver used to access the remote data.</span></span> <span data-ttu-id="0719b-188">Дополнительные сведения см. в документации по конкретному драйверу.</span><span class="sxs-lookup"><span data-stu-id="0719b-188">For more information, see the documentation for the specific driver.</span></span>


> [!NOTE]
> - <span data-ttu-id="0719b-189">Необходимо задать значение свойства **Connect** перед настройкой свойства **ReturnsRecords**.</span><span class="sxs-lookup"><span data-stu-id="0719b-189">You must set the **Connect** property before you set the **ReturnsRecords** property.</span></span>
> - <span data-ttu-id="0719b-190">Необходимо иметь разрешения на доступ к компьютеру, который содержит сервер базы данных, доступ к которому вы пытаетесь получить доступ.</span><span class="sxs-lookup"><span data-stu-id="0719b-190">You must have access permissions to the computer that contains the database server you're trying to access.</span></span>


