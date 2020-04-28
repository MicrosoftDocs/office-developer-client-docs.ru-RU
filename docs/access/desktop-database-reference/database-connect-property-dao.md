---
title: Свойство Database. Connect (DAO)
TOCTitle: Connect Property
ms:assetid: c3e511a6-baef-3758-cfb1-3459b0b19cf3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823048(v=office.15)
ms:contentKeyID: 48547578
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cb3566a4f402c1b8ae75a47880f2101bf35d77db
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294990"
---
# <a name="databaseconnect-property-dao"></a><span data-ttu-id="e3260-102">Свойство Database. Connect (DAO)</span><span class="sxs-lookup"><span data-stu-id="e3260-102">Database.Connect property (DAO)</span></span>


<span data-ttu-id="e3260-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e3260-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e3260-104">Задает или возвращает значение, предоставляющее сведения об источнике в открытой базе данных.</span><span class="sxs-lookup"><span data-stu-id="e3260-104">Sets or returns a value that provides information about the source an open database.</span></span> <span data-ttu-id="e3260-105">Для чтения и записи, **String**.</span><span class="sxs-lookup"><span data-stu-id="e3260-105">Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3260-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e3260-106">Syntax</span></span>

<span data-ttu-id="e3260-107">*expression* .Connect</span><span class="sxs-lookup"><span data-stu-id="e3260-107">*expression* .Connect</span></span>

<span data-ttu-id="e3260-108">*выражение*: переменная, представляющая объект **Database**.</span><span class="sxs-lookup"><span data-stu-id="e3260-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3260-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e3260-109">Remarks</span></span>

<span data-ttu-id="e3260-110">Параметры свойства **Connect** сохранены в **String**, состоящей из указателя типа базы данных и нуля либо нескольких параметров, разделенных точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="e3260-110">The **Connect** property setting is a **String** composed of a database type specifier and zero or more parameters separated by semicolons.</span></span> <span data-ttu-id="e3260-111">Свойство **Connect** передает дополнительные сведения для ODBC и определенным драйверам ISAM при необходимости.</span><span class="sxs-lookup"><span data-stu-id="e3260-111">The **Connect** property passes additional information to ODBC and certain ISAM drivers as needed.</span></span>

<span data-ttu-id="e3260-112">Чтобы выполнить запрос к серверу SQL для таблицы, связанной с файлом базы данных Microsoft Access, необходимо сначала задать в качестве значения свойства **Connect** базы данных связанной таблицы допустимую строку подключения ODBC.</span><span class="sxs-lookup"><span data-stu-id="e3260-112">To perform an SQL pass-through query on a table linked to your Microsoft Access database file, you must first set the **Connect** property of the linked table's database to a valid ODBC connection string.</span></span>

<span data-ttu-id="e3260-113">Путь, как показано в приведенной ниже таблице, содержит полный путь к каталогу, содержащему файлы базы данных, и должен иметь впереди идентификатор DATABASE=.</span><span class="sxs-lookup"><span data-stu-id="e3260-113">The path as shown in the following table is the full path for the directory containing the database files and must be preceded by the identifier DATABASE=.</span></span> <span data-ttu-id="e3260-114">В некоторых случаях (как в случае с базами данных Microsoft Excel и ядра СУБД Microsoft Access) следует включить конкретное имя файла в аргумент пути к базе данных.</span><span class="sxs-lookup"><span data-stu-id="e3260-114">In some cases (as with Microsoft Excel and Microsoft Access database engine databases), you should include a specific file name in the database path argument.</span></span>

<span data-ttu-id="e3260-115">Таблица ниже содержит возможные типы базы данных и соответствующие указатели базы данных и пути к параметрам свойства **Connect**.</span><span class="sxs-lookup"><span data-stu-id="e3260-115">The following table shows possible database types and their corresponding database specifiers and paths for the **Connect** property setting.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e3260-116">Тип базы данных</span><span class="sxs-lookup"><span data-stu-id="e3260-116">Database type</span></span></p></th>
<th><p><span data-ttu-id="e3260-117">Указатель</span><span class="sxs-lookup"><span data-stu-id="e3260-117">Specifier</span></span></p></th>
<th><p><span data-ttu-id="e3260-118">Пример</span><span class="sxs-lookup"><span data-stu-id="e3260-118">Example</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e3260-119">База данных Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="e3260-119">Microsoft Access Database</span></span></p></td>
<td><p><span data-ttu-id="e3260-120">[database];</span><span class="sxs-lookup"><span data-stu-id="e3260-120">[database];</span></span></p></td>
<td><p><span data-ttu-id="e3260-121">диск: \путь\имяфайла</span><span class="sxs-lookup"><span data-stu-id="e3260-121">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3260-122">dBASE III</span><span class="sxs-lookup"><span data-stu-id="e3260-122">dBASE III</span></span></p></td>
<td><p><span data-ttu-id="e3260-123">dBASE III;</span><span class="sxs-lookup"><span data-stu-id="e3260-123">dBASE III;</span></span></p></td>
<td><p><span data-ttu-id="e3260-124">диск: \путь</span><span class="sxs-lookup"><span data-stu-id="e3260-124">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3260-125">dBASE IV</span><span class="sxs-lookup"><span data-stu-id="e3260-125">dBASE IV</span></span></p></td>
<td><p><span data-ttu-id="e3260-126">dBASE IV;</span><span class="sxs-lookup"><span data-stu-id="e3260-126">dBASE IV;</span></span></p></td>
<td><p><span data-ttu-id="e3260-127">диск: \путь</span><span class="sxs-lookup"><span data-stu-id="e3260-127">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3260-128">dBASE 5</span><span class="sxs-lookup"><span data-stu-id="e3260-128">dBASE 5</span></span></p></td>
<td><p><span data-ttu-id="e3260-129">dBASE 5.0;</span><span class="sxs-lookup"><span data-stu-id="e3260-129">dBASE 5.0;</span></span></p></td>
<td><p><span data-ttu-id="e3260-130">диск: \путь</span><span class="sxs-lookup"><span data-stu-id="e3260-130">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3260-131">Paradox 3.x</span><span class="sxs-lookup"><span data-stu-id="e3260-131">Paradox 3.x</span></span></p></td>
<td><p><span data-ttu-id="e3260-132">Paradox 3.x;</span><span class="sxs-lookup"><span data-stu-id="e3260-132">Paradox 3.x;</span></span></p></td>
<td><p><span data-ttu-id="e3260-133">диск: \путь</span><span class="sxs-lookup"><span data-stu-id="e3260-133">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3260-134">Paradox 4.x</span><span class="sxs-lookup"><span data-stu-id="e3260-134">Paradox 4.x</span></span></p></td>
<td><p><span data-ttu-id="e3260-135">Paradox 4.x;</span><span class="sxs-lookup"><span data-stu-id="e3260-135">Paradox 4.x;</span></span></p></td>
<td><p><span data-ttu-id="e3260-136">диск: \путь</span><span class="sxs-lookup"><span data-stu-id="e3260-136">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3260-137">Paradox 5.x</span><span class="sxs-lookup"><span data-stu-id="e3260-137">Paradox 5.x</span></span></p></td>
<td><p><span data-ttu-id="e3260-138">Paradox 5.x;</span><span class="sxs-lookup"><span data-stu-id="e3260-138">Paradox 5.x;</span></span></p></td>
<td><p><span data-ttu-id="e3260-139">диск: \путь</span><span class="sxs-lookup"><span data-stu-id="e3260-139">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3260-140">Microsoft Excel 3.0</span><span class="sxs-lookup"><span data-stu-id="e3260-140">Microsoft Excel 3.0</span></span></p></td>
<td><p><span data-ttu-id="e3260-141">Excel 3.0;</span><span class="sxs-lookup"><span data-stu-id="e3260-141">Excel 3.0;</span></span></p></td>
<td><p><span data-ttu-id="e3260-142">диск: \путь\имяфайла.xls</span><span class="sxs-lookup"><span data-stu-id="e3260-142">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3260-143">Microsoft Excel 4.0</span><span class="sxs-lookup"><span data-stu-id="e3260-143">Microsoft Excel 4.0</span></span></p></td>
<td><p><span data-ttu-id="e3260-144">Excel 4.0;</span><span class="sxs-lookup"><span data-stu-id="e3260-144">Excel 4.0;</span></span></p></td>
<td><p><span data-ttu-id="e3260-145">диск: \путь\имяфайла.xls</span><span class="sxs-lookup"><span data-stu-id="e3260-145">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3260-146">Microsoft Excel 5.0 или Microsoft Excel 95</span><span class="sxs-lookup"><span data-stu-id="e3260-146">Microsoft Excel 5.0 or Microsoft Excel 95</span></span></p></td>
<td><p><span data-ttu-id="e3260-147">Excel 5.0;</span><span class="sxs-lookup"><span data-stu-id="e3260-147">Excel 5.0;</span></span></p></td>
<td><p><span data-ttu-id="e3260-148">диск: \путь\имяфайла.xls</span><span class="sxs-lookup"><span data-stu-id="e3260-148">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3260-149">Microsoft Excel 97</span><span class="sxs-lookup"><span data-stu-id="e3260-149">Microsoft Excel 97</span></span></p></td>
<td><p><span data-ttu-id="e3260-150">Excel 8.0;</span><span class="sxs-lookup"><span data-stu-id="e3260-150">Excel 8.0;</span></span></p></td>
<td><p><span data-ttu-id="e3260-151">диск: \путь\имяфайла.xls</span><span class="sxs-lookup"><span data-stu-id="e3260-151">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3260-152">Lotus 1-2-3 WKS и WK1</span><span class="sxs-lookup"><span data-stu-id="e3260-152">Lotus 1-2-3 WKS and WK1</span></span></p></td>
<td><p><span data-ttu-id="e3260-153">Lotus WK1;</span><span class="sxs-lookup"><span data-stu-id="e3260-153">Lotus WK1;</span></span></p></td>
<td><p><span data-ttu-id="e3260-154">диск: \путь\имяфайла.wk1</span><span class="sxs-lookup"><span data-stu-id="e3260-154">drive:\path\filename.wk1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3260-155">Lotus 1-2-3 WK3</span><span class="sxs-lookup"><span data-stu-id="e3260-155">Lotus 1-2-3 WK3</span></span></p></td>
<td><p><span data-ttu-id="e3260-156">Lotus WK3;</span><span class="sxs-lookup"><span data-stu-id="e3260-156">Lotus WK3;</span></span></p></td>
<td><p><span data-ttu-id="e3260-157">диск: \путь\имяфайла.wk3</span><span class="sxs-lookup"><span data-stu-id="e3260-157">drive:\path\filename.wk3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3260-158">Lotus 1-2-3 WK4</span><span class="sxs-lookup"><span data-stu-id="e3260-158">Lotus 1-2-3 WK4</span></span></p></td>
<td><p><span data-ttu-id="e3260-159">Lotus WK4;</span><span class="sxs-lookup"><span data-stu-id="e3260-159">Lotus WK4;</span></span></p></td>
<td><p><span data-ttu-id="e3260-160">диск: \путь\имяфайла.wk4</span><span class="sxs-lookup"><span data-stu-id="e3260-160">drive:\path\filename.wk4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3260-161">HTML Import</span><span class="sxs-lookup"><span data-stu-id="e3260-161">HTML Import</span></span></p></td>
<td><p><span data-ttu-id="e3260-162">HTML Import;</span><span class="sxs-lookup"><span data-stu-id="e3260-162">HTML Import;</span></span></p></td>
<td><p><span data-ttu-id="e3260-163">диск: \путь\имяфайла</span><span class="sxs-lookup"><span data-stu-id="e3260-163">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3260-164">HTML Export</span><span class="sxs-lookup"><span data-stu-id="e3260-164">HTML Export</span></span></p></td>
<td><p><span data-ttu-id="e3260-165">HTML Export;</span><span class="sxs-lookup"><span data-stu-id="e3260-165">HTML Export;</span></span></p></td>
<td><p><span data-ttu-id="e3260-166">диск: \путь</span><span class="sxs-lookup"><span data-stu-id="e3260-166">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3260-167">Text</span><span class="sxs-lookup"><span data-stu-id="e3260-167">Text</span></span></p></td>
<td><p><span data-ttu-id="e3260-168">Text;</span><span class="sxs-lookup"><span data-stu-id="e3260-168">Text;</span></span></p></td>
<td><p><span data-ttu-id="e3260-169">диск: \путь</span><span class="sxs-lookup"><span data-stu-id="e3260-169">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3260-170">ODBC</span><span class="sxs-lookup"><span data-stu-id="e3260-170">ODBC</span></span></p></td>
<td><p><span data-ttu-id="e3260-171">ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</span><span class="sxs-lookup"><span data-stu-id="e3260-171">ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</span></span></p></td>
<td><p><span data-ttu-id="e3260-172">Нет</span><span class="sxs-lookup"><span data-stu-id="e3260-172">None</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3260-173">Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="e3260-173">Microsoft Exchange</span></span></p></td>
<td><p><span data-ttu-id="e3260-174">Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</span><span class="sxs-lookup"><span data-stu-id="e3260-174">Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</span></span></p></td>
<td><p><span data-ttu-id="e3260-175">диск: \путь\имяфайла</span><span class="sxs-lookup"><span data-stu-id="e3260-175">drive:\path\filename</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e3260-176">Если описатель имеет значение только "ODBC;", драйвер ODBC отображает диалоговое окно со списком всех зарегистрированных имен источников данных ODBC, чтобы пользователь мог выбрать базу данных.</span><span class="sxs-lookup"><span data-stu-id="e3260-176">If the specifier is only "ODBC;", the ODBC driver displays a dialog box listing all registered ODBC data source names so that the user can select a database.</span></span>

<span data-ttu-id="e3260-177">Если пароль необходим, но не указан в параметрах свойства **Connect**, диалоговое окно входа отображается при первой попытке доступа к таблице со стороны драйвера ODBC и еще раз при закрытии и повторном установлении подключения.</span><span class="sxs-lookup"><span data-stu-id="e3260-177">If a password is required but not provided in the **Connect** property setting, a login dialog box is displayed the first time a table is accessed by the ODBC driver and again if the connection is closed and reopened.</span></span>

<span data-ttu-id="e3260-178">Для данных в Microsoft Exchange обязательный ключ MAPILEVEL должен иметь полностью разрешенный путь к папке (например, "Mailbox - Pat SmithIAlpha/Today").</span><span class="sxs-lookup"><span data-stu-id="e3260-178">For data in Microsoft Exchange, the required MAPILEVEL key should be set to a fully-resolved folder path (for example, "Mailbox - Pat SmithIAlpha/Today").</span></span> <span data-ttu-id="e3260-179">Путь не включает имя папки, которая будет открываться в качестве таблицы; вместо этого необходимо указать имя этой папки в качестве имени аргумента для метода **CreateTable**.</span><span class="sxs-lookup"><span data-stu-id="e3260-179">The path does not include the name of the folder that will be opened as a table; that folder’s name should instead be specified as the name argument to the **CreateTable** method.</span></span> <span data-ttu-id="e3260-180">Для ключа TABLETYPE должно быть установлено значение «0», чтобы открыть папку (по умолчанию) или «1», чтобы открыть адресную книгу.</span><span class="sxs-lookup"><span data-stu-id="e3260-180">The TABLETYPE key should be set to "0" to open a folder (default) or "1" to open an address book.</span></span> <span data-ttu-id="e3260-181">Ключ PROFILE по умолчанию относится к профилю, который в настоящее время используется.</span><span class="sxs-lookup"><span data-stu-id="e3260-181">The PROFILE key defaults to the profile currently in use.</span></span>

<span data-ttu-id="e3260-182">Вы можете задать свойство **Connect** для объекта **Database** , указав аргумент source для метода **openDatabase** .</span><span class="sxs-lookup"><span data-stu-id="e3260-182">You can set the **Connect** property for a **Database** object by providing a source argument to the **OpenDatabase** method.</span></span> <span data-ttu-id="e3260-183">Вы можете проверить этот параметр, чтобы определить тип, путь, идентификатор пользователя, пароль или источник данных ODBC для базы данных.</span><span class="sxs-lookup"><span data-stu-id="e3260-183">You can check the setting to determine the type, path, user ID, password, or ODBC data source of the database.</span></span>


> [!NOTE]
> - <span data-ttu-id="e3260-184">Необходимо задать значение свойства **Connect** перед настройкой свойства **ReturnsRecords**.</span><span class="sxs-lookup"><span data-stu-id="e3260-184">You must set the **Connect** property before you set the **ReturnsRecords** property.</span></span>
> - <span data-ttu-id="e3260-185">Необходимо иметь разрешения на доступ к компьютеру, который содержит сервер базы данных, доступ к которому вы пытаетесь получить доступ.</span><span class="sxs-lookup"><span data-stu-id="e3260-185">You must have access permissions to the computer that contains the database server you're trying to access.</span></span>


