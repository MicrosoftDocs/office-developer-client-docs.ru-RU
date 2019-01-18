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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698857"
---
# <a name="databaseconnect-property-dao"></a><span data-ttu-id="9a487-102">Свойство Database.Connect (DAO)</span><span class="sxs-lookup"><span data-stu-id="9a487-102">Database.Connect property (DAO)</span></span>


<span data-ttu-id="9a487-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9a487-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9a487-104">Задает или возвращает значение, которое содержит сведения об источнике открыть базу данных.</span><span class="sxs-lookup"><span data-stu-id="9a487-104">Sets or returns a value that provides information about the source an open database.</span></span> <span data-ttu-id="9a487-105">Для чтения и записи, **String**.</span><span class="sxs-lookup"><span data-stu-id="9a487-105">Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a487-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9a487-106">Syntax</span></span>

<span data-ttu-id="9a487-107">*выражение* . Подключение</span><span class="sxs-lookup"><span data-stu-id="9a487-107">*expression* .Connect</span></span>

<span data-ttu-id="9a487-108">*выражение* Переменная, которая представляет собой объект **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="9a487-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a487-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="9a487-109">Remarks</span></span>

<span data-ttu-id="9a487-110">Настройка свойства **подключение** — **строка** состоит из спецификатора типа базы данных и ноль или больше параметров, разделенных точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="9a487-110">The **Connect** property setting is a **String** composed of a database type specifier and zero or more parameters separated by semicolons.</span></span> <span data-ttu-id="9a487-111">Свойство **Connect** передает Дополнительные сведения о ODBC и драйверы некоторых ISAM при необходимости.</span><span class="sxs-lookup"><span data-stu-id="9a487-111">The **Connect** property passes additional information to ODBC and certain ISAM drivers as needed.</span></span>

<span data-ttu-id="9a487-112">Для выполнения запроса к серверу для таблица, связанная с файла базы данных Microsoft Access, сначала необходимо задать свойство **подключение** базы данных, связанной таблицы допустимая строка подключения ODBC.</span><span class="sxs-lookup"><span data-stu-id="9a487-112">To perform an SQL pass-through query on a table linked to your Microsoft Access database file, you must first set the **Connect** property of the linked table's database to a valid ODBC connection string.</span></span>

<span data-ttu-id="9a487-113">Путь, как показано в следующей таблице — это полный путь к каталогу, содержащему файлы базы данных и должен предшествовать идентификатор базы данных =.</span><span class="sxs-lookup"><span data-stu-id="9a487-113">The path as shown in the following table is the full path for the directory containing the database files and must be preceded by the identifier DATABASE=.</span></span> <span data-ttu-id="9a487-114">В некоторых случаях (как с помощью Microsoft Excel и Microsoft Access базы данных базами данных, ядро) должен включать имя файла в качестве аргумента базы данных.</span><span class="sxs-lookup"><span data-stu-id="9a487-114">In some cases (as with Microsoft Excel and Microsoft Access database engine databases), you should include a specific file name in the database path argument.</span></span>

<span data-ttu-id="9a487-115">Ниже приведены возможные типы и баз данных и их соответствующие спецификаторы базы данных пути для настройки свойства **подключения** .</span><span class="sxs-lookup"><span data-stu-id="9a487-115">The following table shows possible database types and their corresponding database specifiers and paths for the **Connect** property setting.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9a487-116">Тип базы данных</span><span class="sxs-lookup"><span data-stu-id="9a487-116">Database type</span></span></p></th>
<th><p><span data-ttu-id="9a487-117">Описателя</span><span class="sxs-lookup"><span data-stu-id="9a487-117">Specifier</span></span></p></th>
<th><p><span data-ttu-id="9a487-118">Пример</span><span class="sxs-lookup"><span data-stu-id="9a487-118">Example</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9a487-119">Базы данных Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="9a487-119">Microsoft Access Database</span></span></p></td>
<td><p><span data-ttu-id="9a487-120">База данных [];</span><span class="sxs-lookup"><span data-stu-id="9a487-120">[database];</span></span></p></td>
<td><p><span data-ttu-id="9a487-121">диск: \path\filename</span><span class="sxs-lookup"><span data-stu-id="9a487-121">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a487-122">dBASE III</span><span class="sxs-lookup"><span data-stu-id="9a487-122">dBASE III</span></span></p></td>
<td><p><span data-ttu-id="9a487-123">dBASE III;</span><span class="sxs-lookup"><span data-stu-id="9a487-123">dBASE III;</span></span></p></td>
<td><p><span data-ttu-id="9a487-124">диск: \path</span><span class="sxs-lookup"><span data-stu-id="9a487-124">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a487-125">dBASE IV</span><span class="sxs-lookup"><span data-stu-id="9a487-125">dBASE IV</span></span></p></td>
<td><p><span data-ttu-id="9a487-126">dBASE IV;</span><span class="sxs-lookup"><span data-stu-id="9a487-126">dBASE IV;</span></span></p></td>
<td><p><span data-ttu-id="9a487-127">диск: \path</span><span class="sxs-lookup"><span data-stu-id="9a487-127">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a487-128">dBASE 5</span><span class="sxs-lookup"><span data-stu-id="9a487-128">dBASE 5</span></span></p></td>
<td><p><span data-ttu-id="9a487-129">dBASE 5.0;</span><span class="sxs-lookup"><span data-stu-id="9a487-129">dBASE 5.0;</span></span></p></td>
<td><p><span data-ttu-id="9a487-130">диск: \path</span><span class="sxs-lookup"><span data-stu-id="9a487-130">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a487-131">Paradox 3.x</span><span class="sxs-lookup"><span data-stu-id="9a487-131">Paradox 3.x</span></span></p></td>
<td><p><span data-ttu-id="9a487-132">Paradox 3.x;</span><span class="sxs-lookup"><span data-stu-id="9a487-132">Paradox 3.x;</span></span></p></td>
<td><p><span data-ttu-id="9a487-133">диск: \path</span><span class="sxs-lookup"><span data-stu-id="9a487-133">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a487-134">Paradox 4.x</span><span class="sxs-lookup"><span data-stu-id="9a487-134">Paradox 4.x</span></span></p></td>
<td><p><span data-ttu-id="9a487-135">Paradox 4.x;</span><span class="sxs-lookup"><span data-stu-id="9a487-135">Paradox 4.x;</span></span></p></td>
<td><p><span data-ttu-id="9a487-136">диск: \path</span><span class="sxs-lookup"><span data-stu-id="9a487-136">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a487-137">Paradox 5.x</span><span class="sxs-lookup"><span data-stu-id="9a487-137">Paradox 5.x</span></span></p></td>
<td><p><span data-ttu-id="9a487-138">Paradox 5.x;</span><span class="sxs-lookup"><span data-stu-id="9a487-138">Paradox 5.x;</span></span></p></td>
<td><p><span data-ttu-id="9a487-139">диск: \path</span><span class="sxs-lookup"><span data-stu-id="9a487-139">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a487-140">Microsoft Excel 3.0</span><span class="sxs-lookup"><span data-stu-id="9a487-140">Microsoft Excel 3.0</span></span></p></td>
<td><p><span data-ttu-id="9a487-141">Excel 3.0;</span><span class="sxs-lookup"><span data-stu-id="9a487-141">Excel 3.0;</span></span></p></td>
<td><p><span data-ttu-id="9a487-142">Drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="9a487-142">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a487-143">Microsoft Excel 4.0</span><span class="sxs-lookup"><span data-stu-id="9a487-143">Microsoft Excel 4.0</span></span></p></td>
<td><p><span data-ttu-id="9a487-144">Excel 4.0;</span><span class="sxs-lookup"><span data-stu-id="9a487-144">Excel 4.0;</span></span></p></td>
<td><p><span data-ttu-id="9a487-145">Drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="9a487-145">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a487-146">Microsoft Excel 5.0 или Microsoft Excel 95</span><span class="sxs-lookup"><span data-stu-id="9a487-146">Microsoft Excel 5.0 or Microsoft Excel 95</span></span></p></td>
<td><p><span data-ttu-id="9a487-147">Excel 5.0;</span><span class="sxs-lookup"><span data-stu-id="9a487-147">Excel 5.0;</span></span></p></td>
<td><p><span data-ttu-id="9a487-148">Drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="9a487-148">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a487-149">Microsoft Excel 97</span><span class="sxs-lookup"><span data-stu-id="9a487-149">Microsoft Excel 97</span></span></p></td>
<td><p><span data-ttu-id="9a487-150">Excel 8.0;</span><span class="sxs-lookup"><span data-stu-id="9a487-150">Excel 8.0;</span></span></p></td>
<td><p><span data-ttu-id="9a487-151">Drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="9a487-151">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a487-152">Lotus 1-2-3 WKS и WK1</span><span class="sxs-lookup"><span data-stu-id="9a487-152">Lotus 1-2-3 WKS and WK1</span></span></p></td>
<td><p><span data-ttu-id="9a487-153">Lotus WK1;</span><span class="sxs-lookup"><span data-stu-id="9a487-153">Lotus WK1;</span></span></p></td>
<td><p><span data-ttu-id="9a487-154">Drive:\path\filename.WK1</span><span class="sxs-lookup"><span data-stu-id="9a487-154">drive:\path\filename.wk1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a487-155">WK3 Lotus 1-2-3</span><span class="sxs-lookup"><span data-stu-id="9a487-155">Lotus 1-2-3 WK3</span></span></p></td>
<td><p><span data-ttu-id="9a487-156">Lotus WK3;</span><span class="sxs-lookup"><span data-stu-id="9a487-156">Lotus WK3;</span></span></p></td>
<td><p><span data-ttu-id="9a487-157">Drive:\path\filename.WK3</span><span class="sxs-lookup"><span data-stu-id="9a487-157">drive:\path\filename.wk3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a487-158">WK4 Lotus 1-2-3</span><span class="sxs-lookup"><span data-stu-id="9a487-158">Lotus 1-2-3 WK4</span></span></p></td>
<td><p><span data-ttu-id="9a487-159">Lotus WK4;</span><span class="sxs-lookup"><span data-stu-id="9a487-159">Lotus WK4;</span></span></p></td>
<td><p><span data-ttu-id="9a487-160">Drive:\path\filename.WK4</span><span class="sxs-lookup"><span data-stu-id="9a487-160">drive:\path\filename.wk4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a487-161">Импорт HTML</span><span class="sxs-lookup"><span data-stu-id="9a487-161">HTML Import</span></span></p></td>
<td><p><span data-ttu-id="9a487-162">Импорт HTML;</span><span class="sxs-lookup"><span data-stu-id="9a487-162">HTML Import;</span></span></p></td>
<td><p><span data-ttu-id="9a487-163">диск: \path\filename</span><span class="sxs-lookup"><span data-stu-id="9a487-163">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a487-164">Экспорт HTML</span><span class="sxs-lookup"><span data-stu-id="9a487-164">HTML Export</span></span></p></td>
<td><p><span data-ttu-id="9a487-165">Экспорт HTML;</span><span class="sxs-lookup"><span data-stu-id="9a487-165">HTML Export;</span></span></p></td>
<td><p><span data-ttu-id="9a487-166">диск: \path</span><span class="sxs-lookup"><span data-stu-id="9a487-166">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a487-167">Текст</span><span class="sxs-lookup"><span data-stu-id="9a487-167">Text</span></span></p></td>
<td><p><span data-ttu-id="9a487-168">Текст;</span><span class="sxs-lookup"><span data-stu-id="9a487-168">Text;</span></span></p></td>
<td><p><span data-ttu-id="9a487-169">диск: \path</span><span class="sxs-lookup"><span data-stu-id="9a487-169">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a487-170">Open Database Connectivity</span><span class="sxs-lookup"><span data-stu-id="9a487-170">ODBC</span></span></p></td>
<td><p><span data-ttu-id="9a487-171">ODBC. Базы данных = база данных; UID = пользователя; PWD = пароля; Уведомления о Доставке = источнику данных; [LOGINTIMEOUT = секунды;]</span><span class="sxs-lookup"><span data-stu-id="9a487-171">ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</span></span></p></td>
<td><p><span data-ttu-id="9a487-172">Нет</span><span class="sxs-lookup"><span data-stu-id="9a487-172">None</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a487-173">Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="9a487-173">Microsoft Exchange</span></span></p></td>
<td><p><span data-ttu-id="9a487-174">Exchange 4.0; MAPILEVEL = folderpath; [TABLETYPE = {0 | 1}]; [ПРОФИЛЕЙ = профиля;] [PWD = пароль;] [Базы данных = база данных;]</span><span class="sxs-lookup"><span data-stu-id="9a487-174">Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</span></span></p></td>
<td><p><span data-ttu-id="9a487-175">диск: \path\filename</span><span class="sxs-lookup"><span data-stu-id="9a487-175">drive:\path\filename</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9a487-176">Соответствует только «ODBC;», драйвер ODBC отображает диалоговое окно со списком всех зарегистрированных имен источников данных ODBC, чтобы пользователь может выбрать базу данных.</span><span class="sxs-lookup"><span data-stu-id="9a487-176">If the specifier is only "ODBC;", the ODBC driver displays a dialog box listing all registered ODBC data source names so that the user can select a database.</span></span>

<span data-ttu-id="9a487-177">Если пароль требуется, но не указан в параметре свойства **подключения** , диалоговое окно входа в систему отображается впервые таблицам драйвер ODBC и снова закрыто и повторно открыть подключение.</span><span class="sxs-lookup"><span data-stu-id="9a487-177">If a password is required but not provided in the **Connect** property setting, a login dialog box is displayed the first time a table is accessed by the ODBC driver and again if the connection is closed and reopened.</span></span>

<span data-ttu-id="9a487-178">Для данных в Microsoft Exchange требуется ключ MAPILEVEL должно быть присвоено полностью разрешить пути (например, «почтовый ящик – Pat SmithIAlpha/текущую»).</span><span class="sxs-lookup"><span data-stu-id="9a487-178">For data in Microsoft Exchange, the required MAPILEVEL key should be set to a fully-resolved folder path (for example, "Mailbox - Pat SmithIAlpha/Today").</span></span> <span data-ttu-id="9a487-179">Путь не включает имя папки, которая будет открыта в виде таблицы; Вместо этого следует указать имя этой папки в качестве аргумента имя метода **CreateTable** .</span><span class="sxs-lookup"><span data-stu-id="9a487-179">The path does not include the name of the folder that will be opened as a table; that folder’s name should instead be specified as the name argument to the **CreateTable** method.</span></span> <span data-ttu-id="9a487-180">Клавиша TABLETYPE должно быть присвоено значение «0» откройте папку (по умолчанию) или «1», чтобы открыть адресную книгу.</span><span class="sxs-lookup"><span data-stu-id="9a487-180">The TABLETYPE key should be set to "0" to open a folder (default) or "1" to open an address book.</span></span> <span data-ttu-id="9a487-181">В настоящее время с помощью ключа ПРОФИЛЯ по умолчанию к профилю.</span><span class="sxs-lookup"><span data-stu-id="9a487-181">The PROFILE key defaults to the profile currently in use.</span></span>

<span data-ttu-id="9a487-182">Свойства **подключения** для объекта **базы данных** с указанием исходный аргумент методу **OpenDatabase** .</span><span class="sxs-lookup"><span data-stu-id="9a487-182">You can set the **Connect** property for a **Database** object by providing a source argument to the **OpenDatabase** method.</span></span> <span data-ttu-id="9a487-183">Чтобы проверить параметр, чтобы определить тип, путь, идентификатор пользователя, пароль или источник данных ODBC базы данных.</span><span class="sxs-lookup"><span data-stu-id="9a487-183">You can check the setting to determine the type, path, user ID, password, or ODBC data source of the database.</span></span>


> [!NOTE]
> - <span data-ttu-id="9a487-184">Необходимо установить свойство **подключение** , прежде чем задать свойство **ReturnsRecords** .</span><span class="sxs-lookup"><span data-stu-id="9a487-184">You must set the **Connect** property before you set the **ReturnsRecords** property.</span></span>
> - <span data-ttu-id="9a487-185">Необходимо иметь разрешения доступа на компьютере, где размещается сервер базы данных, который вы пытаетесь получить доступ к.</span><span class="sxs-lookup"><span data-stu-id="9a487-185">You must have access permissions to the computer that contains the database server you're trying to access.</span></span>


