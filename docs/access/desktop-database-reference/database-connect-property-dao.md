---
title: Свойство Database.Connect (DAO)
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
# <a name="databaseconnect-property-dao"></a><span data-ttu-id="750d9-102">Свойство Database.Connect (DAO)</span><span class="sxs-lookup"><span data-stu-id="750d9-102">Database.Connect property (DAO)</span></span>


<span data-ttu-id="750d9-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="750d9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="750d9-104">Задает или возвращает значение, которое предоставляет сведения об источнике открытой базы данных.</span><span class="sxs-lookup"><span data-stu-id="750d9-104">Sets or returns a value that provides information about the source an open database.</span></span> <span data-ttu-id="750d9-105">Для чтения и записи, **String**.</span><span class="sxs-lookup"><span data-stu-id="750d9-105">Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="750d9-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="750d9-106">Syntax</span></span>

<span data-ttu-id="750d9-107">*expression* .Connect</span><span class="sxs-lookup"><span data-stu-id="750d9-107">*expression* .Connect</span></span>

<span data-ttu-id="750d9-108">*выражение*: переменная, представляющая объект **Database**.</span><span class="sxs-lookup"><span data-stu-id="750d9-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="750d9-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="750d9-109">Remarks</span></span>

<span data-ttu-id="750d9-110">Параметры свойства **Connect** сохранены в **String**, состоящей из указателя типа базы данных и нуля либо нескольких параметров, разделенных точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="750d9-110">The **Connect** property setting is a **String** composed of a database type specifier and zero or more parameters separated by semicolons.</span></span> <span data-ttu-id="750d9-111">Свойство **Connect** передает дополнительные сведения для ODBC и определенным драйверам ISAM при необходимости.</span><span class="sxs-lookup"><span data-stu-id="750d9-111">The **Connect** property passes additional information to ODBC and certain ISAM drivers as needed.</span></span>

<span data-ttu-id="750d9-112">Чтобы выполнить SQL в таблице, связанной с файлом базы данных Microsoft Access, необходимо сначала установить для свойства **Connect** базы данных связанной таблицы допустимую строку подключения ODBC.</span><span class="sxs-lookup"><span data-stu-id="750d9-112">To perform an SQL pass-through query on a table linked to your Microsoft Access database file, you must first set the **Connect** property of the linked table's database to a valid ODBC connection string.</span></span>

<span data-ttu-id="750d9-113">Путь, как показано в приведенной ниже таблице, содержит полный путь к каталогу, содержащему файлы базы данных, и должен иметь впереди идентификатор DATABASE=.</span><span class="sxs-lookup"><span data-stu-id="750d9-113">The path as shown in the following table is the full path for the directory containing the database files and must be preceded by the identifier DATABASE=.</span></span> <span data-ttu-id="750d9-114">В некоторых случаях (как в случае с базами данных Microsoft Excel и ядра СУБД Microsoft Access) следует включить конкретное имя файла в аргумент пути к базе данных.</span><span class="sxs-lookup"><span data-stu-id="750d9-114">In some cases (as with Microsoft Excel and Microsoft Access database engine databases), you should include a specific file name in the database path argument.</span></span>

<span data-ttu-id="750d9-115">Таблица ниже содержит возможные типы базы данных и соответствующие указатели базы данных и пути к параметрам свойства **Connect**.</span><span class="sxs-lookup"><span data-stu-id="750d9-115">The following table shows possible database types and their corresponding database specifiers and paths for the **Connect** property setting.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="750d9-116">Тип базы данных</span><span class="sxs-lookup"><span data-stu-id="750d9-116">Database type</span></span></p></th>
<th><p><span data-ttu-id="750d9-117">Указатель</span><span class="sxs-lookup"><span data-stu-id="750d9-117">Specifier</span></span></p></th>
<th><p><span data-ttu-id="750d9-118">Пример</span><span class="sxs-lookup"><span data-stu-id="750d9-118">Example</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="750d9-119">База данных Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="750d9-119">Microsoft Access Database</span></span></p></td>
<td><p><span data-ttu-id="750d9-120">[database];</span><span class="sxs-lookup"><span data-stu-id="750d9-120">[database];</span></span></p></td>
<td><p><span data-ttu-id="750d9-121">диск: \путь\имяфайла</span><span class="sxs-lookup"><span data-stu-id="750d9-121">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="750d9-122">dBASE III</span><span class="sxs-lookup"><span data-stu-id="750d9-122">dBASE III</span></span></p></td>
<td><p><span data-ttu-id="750d9-123">dBASE III;</span><span class="sxs-lookup"><span data-stu-id="750d9-123">dBASE III;</span></span></p></td>
<td><p><span data-ttu-id="750d9-124">диск: \путь</span><span class="sxs-lookup"><span data-stu-id="750d9-124">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="750d9-125">dBASE IV</span><span class="sxs-lookup"><span data-stu-id="750d9-125">dBASE IV</span></span></p></td>
<td><p><span data-ttu-id="750d9-126">dBASE IV;</span><span class="sxs-lookup"><span data-stu-id="750d9-126">dBASE IV;</span></span></p></td>
<td><p><span data-ttu-id="750d9-127">диск: \путь</span><span class="sxs-lookup"><span data-stu-id="750d9-127">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="750d9-128">dBASE 5</span><span class="sxs-lookup"><span data-stu-id="750d9-128">dBASE 5</span></span></p></td>
<td><p><span data-ttu-id="750d9-129">dBASE 5.0;</span><span class="sxs-lookup"><span data-stu-id="750d9-129">dBASE 5.0;</span></span></p></td>
<td><p><span data-ttu-id="750d9-130">диск: \путь</span><span class="sxs-lookup"><span data-stu-id="750d9-130">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="750d9-131">Paradox 3.x</span><span class="sxs-lookup"><span data-stu-id="750d9-131">Paradox 3.x</span></span></p></td>
<td><p><span data-ttu-id="750d9-132">Paradox 3.x;</span><span class="sxs-lookup"><span data-stu-id="750d9-132">Paradox 3.x;</span></span></p></td>
<td><p><span data-ttu-id="750d9-133">диск: \путь</span><span class="sxs-lookup"><span data-stu-id="750d9-133">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="750d9-134">Paradox 4.x</span><span class="sxs-lookup"><span data-stu-id="750d9-134">Paradox 4.x</span></span></p></td>
<td><p><span data-ttu-id="750d9-135">Paradox 4.x;</span><span class="sxs-lookup"><span data-stu-id="750d9-135">Paradox 4.x;</span></span></p></td>
<td><p><span data-ttu-id="750d9-136">диск: \путь</span><span class="sxs-lookup"><span data-stu-id="750d9-136">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="750d9-137">Paradox 5.x</span><span class="sxs-lookup"><span data-stu-id="750d9-137">Paradox 5.x</span></span></p></td>
<td><p><span data-ttu-id="750d9-138">Paradox 5.x;</span><span class="sxs-lookup"><span data-stu-id="750d9-138">Paradox 5.x;</span></span></p></td>
<td><p><span data-ttu-id="750d9-139">диск: \путь</span><span class="sxs-lookup"><span data-stu-id="750d9-139">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="750d9-140">Microsoft Excel 3.0</span><span class="sxs-lookup"><span data-stu-id="750d9-140">Microsoft Excel 3.0</span></span></p></td>
<td><p><span data-ttu-id="750d9-141">Excel 3.0;</span><span class="sxs-lookup"><span data-stu-id="750d9-141">Excel 3.0;</span></span></p></td>
<td><p><span data-ttu-id="750d9-142">диск: \путь\имяфайла.xls</span><span class="sxs-lookup"><span data-stu-id="750d9-142">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="750d9-143">Microsoft Excel 4.0</span><span class="sxs-lookup"><span data-stu-id="750d9-143">Microsoft Excel 4.0</span></span></p></td>
<td><p><span data-ttu-id="750d9-144">Excel 4.0;</span><span class="sxs-lookup"><span data-stu-id="750d9-144">Excel 4.0;</span></span></p></td>
<td><p><span data-ttu-id="750d9-145">диск: \путь\имяфайла.xls</span><span class="sxs-lookup"><span data-stu-id="750d9-145">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="750d9-146">Microsoft Excel 5.0 или Microsoft Excel 95</span><span class="sxs-lookup"><span data-stu-id="750d9-146">Microsoft Excel 5.0 or Microsoft Excel 95</span></span></p></td>
<td><p><span data-ttu-id="750d9-147">Excel 5.0;</span><span class="sxs-lookup"><span data-stu-id="750d9-147">Excel 5.0;</span></span></p></td>
<td><p><span data-ttu-id="750d9-148">диск: \путь\имяфайла.xls</span><span class="sxs-lookup"><span data-stu-id="750d9-148">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="750d9-149">Microsoft Excel 97</span><span class="sxs-lookup"><span data-stu-id="750d9-149">Microsoft Excel 97</span></span></p></td>
<td><p><span data-ttu-id="750d9-150">Excel 8.0;</span><span class="sxs-lookup"><span data-stu-id="750d9-150">Excel 8.0;</span></span></p></td>
<td><p><span data-ttu-id="750d9-151">диск: \путь\имяфайла.xls</span><span class="sxs-lookup"><span data-stu-id="750d9-151">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="750d9-152">Lotus 1-2-3 WKS и WK1</span><span class="sxs-lookup"><span data-stu-id="750d9-152">Lotus 1-2-3 WKS and WK1</span></span></p></td>
<td><p><span data-ttu-id="750d9-153">Lotus WK1;</span><span class="sxs-lookup"><span data-stu-id="750d9-153">Lotus WK1;</span></span></p></td>
<td><p><span data-ttu-id="750d9-154">диск: \путь\имяфайла.wk1</span><span class="sxs-lookup"><span data-stu-id="750d9-154">drive:\path\filename.wk1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="750d9-155">Lotus 1-2-3 WK3</span><span class="sxs-lookup"><span data-stu-id="750d9-155">Lotus 1-2-3 WK3</span></span></p></td>
<td><p><span data-ttu-id="750d9-156">Lotus WK3;</span><span class="sxs-lookup"><span data-stu-id="750d9-156">Lotus WK3;</span></span></p></td>
<td><p><span data-ttu-id="750d9-157">диск: \путь\имяфайла.wk3</span><span class="sxs-lookup"><span data-stu-id="750d9-157">drive:\path\filename.wk3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="750d9-158">Lotus 1-2-3 WK4</span><span class="sxs-lookup"><span data-stu-id="750d9-158">Lotus 1-2-3 WK4</span></span></p></td>
<td><p><span data-ttu-id="750d9-159">Lotus WK4;</span><span class="sxs-lookup"><span data-stu-id="750d9-159">Lotus WK4;</span></span></p></td>
<td><p><span data-ttu-id="750d9-160">диск: \путь\имяфайла.wk4</span><span class="sxs-lookup"><span data-stu-id="750d9-160">drive:\path\filename.wk4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="750d9-161">HTML Import</span><span class="sxs-lookup"><span data-stu-id="750d9-161">HTML Import</span></span></p></td>
<td><p><span data-ttu-id="750d9-162">HTML Import;</span><span class="sxs-lookup"><span data-stu-id="750d9-162">HTML Import;</span></span></p></td>
<td><p><span data-ttu-id="750d9-163">диск: \путь\имяфайла</span><span class="sxs-lookup"><span data-stu-id="750d9-163">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="750d9-164">HTML Export</span><span class="sxs-lookup"><span data-stu-id="750d9-164">HTML Export</span></span></p></td>
<td><p><span data-ttu-id="750d9-165">HTML Export;</span><span class="sxs-lookup"><span data-stu-id="750d9-165">HTML Export;</span></span></p></td>
<td><p><span data-ttu-id="750d9-166">диск: \путь</span><span class="sxs-lookup"><span data-stu-id="750d9-166">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="750d9-167">Text</span><span class="sxs-lookup"><span data-stu-id="750d9-167">Text</span></span></p></td>
<td><p><span data-ttu-id="750d9-168">Text;</span><span class="sxs-lookup"><span data-stu-id="750d9-168">Text;</span></span></p></td>
<td><p><span data-ttu-id="750d9-169">диск: \путь</span><span class="sxs-lookup"><span data-stu-id="750d9-169">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="750d9-170">ODBC</span><span class="sxs-lookup"><span data-stu-id="750d9-170">ODBC</span></span></p></td>
<td><p><span data-ttu-id="750d9-171">ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</span><span class="sxs-lookup"><span data-stu-id="750d9-171">ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</span></span></p></td>
<td><p><span data-ttu-id="750d9-172">Нет</span><span class="sxs-lookup"><span data-stu-id="750d9-172">None</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="750d9-173">Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="750d9-173">Microsoft Exchange</span></span></p></td>
<td><p><span data-ttu-id="750d9-174">Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</span><span class="sxs-lookup"><span data-stu-id="750d9-174">Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</span></span></p></td>
<td><p><span data-ttu-id="750d9-175">диск: \путь\имяфайла</span><span class="sxs-lookup"><span data-stu-id="750d9-175">drive:\path\filename</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="750d9-176">Если указан только ODBC, драйвер ODBC отображает диалоговое окно со всеми зарегистрированными именами источников данных ODBC, чтобы пользователь мог выбрать базу данных.</span><span class="sxs-lookup"><span data-stu-id="750d9-176">If the specifier is only "ODBC;", the ODBC driver displays a dialog box listing all registered ODBC data source names so that the user can select a database.</span></span>

<span data-ttu-id="750d9-177">Если пароль необходим, но не указан в параметрах свойства **Connect**, диалоговое окно входа отображается при первой попытке доступа к таблице со стороны драйвера ODBC и еще раз при закрытии и повторном установлении подключения.</span><span class="sxs-lookup"><span data-stu-id="750d9-177">If a password is required but not provided in the **Connect** property setting, a login dialog box is displayed the first time a table is accessed by the ODBC driver and again if the connection is closed and reopened.</span></span>

<span data-ttu-id="750d9-178">Для данных в Microsoft Exchange обязательный ключ MAPILEVEL должен иметь полностью разрешенный путь к папке (например, "Mailbox - Pat SmithIAlpha/Today").</span><span class="sxs-lookup"><span data-stu-id="750d9-178">For data in Microsoft Exchange, the required MAPILEVEL key should be set to a fully-resolved folder path (for example, "Mailbox - Pat SmithIAlpha/Today").</span></span> <span data-ttu-id="750d9-179">Путь не включает имя папки, которая будет открываться в качестве таблицы; вместо этого необходимо указать имя этой папки в качестве имени аргумента для метода **CreateTable**.</span><span class="sxs-lookup"><span data-stu-id="750d9-179">The path does not include the name of the folder that will be opened as a table; that folder’s name should instead be specified as the name argument to the **CreateTable** method.</span></span> <span data-ttu-id="750d9-180">Для ключа TABLETYPE должно быть установлено значение «0», чтобы открыть папку (по умолчанию) или «1», чтобы открыть адресную книгу.</span><span class="sxs-lookup"><span data-stu-id="750d9-180">The TABLETYPE key should be set to "0" to open a folder (default) or "1" to open an address book.</span></span> <span data-ttu-id="750d9-181">Ключ PROFILE по умолчанию относится к профилю, который в настоящее время используется.</span><span class="sxs-lookup"><span data-stu-id="750d9-181">The PROFILE key defaults to the profile currently in use.</span></span>

<span data-ttu-id="750d9-182">Вы можете настроить свойство **Connect** для объекта **Database,** предоставив **методу OpenDatabase** аргумент источника.</span><span class="sxs-lookup"><span data-stu-id="750d9-182">You can set the **Connect** property for a **Database** object by providing a source argument to the **OpenDatabase** method.</span></span> <span data-ttu-id="750d9-183">Этот параметр можно проверить, чтобы определить тип, путь, ИД пользователя, пароль или источник данных ODBC базы данных.</span><span class="sxs-lookup"><span data-stu-id="750d9-183">You can check the setting to determine the type, path, user ID, password, or ODBC data source of the database.</span></span>


> [!NOTE]
> - <span data-ttu-id="750d9-184">Необходимо задать значение свойства **Connect** перед настройкой свойства **ReturnsRecords**.</span><span class="sxs-lookup"><span data-stu-id="750d9-184">You must set the **Connect** property before you set the **ReturnsRecords** property.</span></span>
> - <span data-ttu-id="750d9-185">Необходимо иметь разрешения на доступ к компьютеру, который содержит сервер базы данных, доступ к которому вы пытаетесь получить доступ.</span><span class="sxs-lookup"><span data-stu-id="750d9-185">You must have access permissions to the computer that contains the database server you're trying to access.</span></span>


