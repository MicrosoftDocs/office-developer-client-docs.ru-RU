---
title: Connection.Connect Property (DAO)
TOCTitle: Connect Property
ms:assetid: 58b514a2-91cd-7918-cba5-15d71c2457a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194335(v=office.15)
ms:contentKeyID: 48545001
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b1b4baff3bd1ca7d39fbf86f2002b73bda996f1a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482283"
---
# <a name="connectionconnect-property-dao"></a><span data-ttu-id="f3240-102">Connection.Connect Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="f3240-102">Connection.Connect Property (DAO)</span></span>


<span data-ttu-id="f3240-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f3240-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f3240-104">Задает или возвращает значение, которое содержит сведения об источнике открытое подключение.</span><span class="sxs-lookup"><span data-stu-id="f3240-104">Sets or returns a value that provides information about the source of an open connection.</span></span> <span data-ttu-id="f3240-105">Для чтения и записи, **String**.</span><span class="sxs-lookup"><span data-stu-id="f3240-105">Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3240-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f3240-106">Syntax</span></span>

<span data-ttu-id="f3240-107">*выражение* . Подключение</span><span class="sxs-lookup"><span data-stu-id="f3240-107">*expression* .Connect</span></span>

<span data-ttu-id="f3240-108">*выражение* Переменная, которая содержит объект **подключения** .</span><span class="sxs-lookup"><span data-stu-id="f3240-108">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3240-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="f3240-109">Remarks</span></span>

<span data-ttu-id="f3240-110">Настройка свойства **подключение** — **строка** состоит из спецификатора типа базы данных и ноль или больше параметров, разделенных точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="f3240-110">The **Connect** property setting is a **String** composed of a database type specifier and zero or more parameters separated by semicolons.</span></span> <span data-ttu-id="f3240-111">Свойство **Connect** передает Дополнительные сведения о ODBC и драйверы некоторых ISAM при необходимости.</span><span class="sxs-lookup"><span data-stu-id="f3240-111">The **Connect** property passes additional information to ODBC and certain ISAM drivers as needed.</span></span>

<span data-ttu-id="f3240-112">Для выполнения запроса к серверу для таблица, связанная с файла базы данных Microsoft Access, сначала необходимо задать свойство **подключение** базы данных, связанной таблицы допустимая строка подключения ODBC.</span><span class="sxs-lookup"><span data-stu-id="f3240-112">To perform an SQL pass-through query on a table linked to your Microsoft Access database file, you must first set the **Connect** property of the linked table's database to a valid ODBC connection string.</span></span>

<span data-ttu-id="f3240-113">Для объекта **TableDef** , представляющий связанной таблицы значение свойства **подключение** состоит из одного или двух частях (описатель типа базы данных и путь к базе данных), каждая из которых заканчиваются точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="f3240-113">For a **TableDef** object that represents a linked table, the **Connect** property setting consists of one or two parts (a database type specifier and a path to the database), each of which ends with a semicolon.</span></span>

<span data-ttu-id="f3240-114">Путь, как показано в следующей таблице — это полный путь к каталогу, содержащему файлы базы данных и должен предшествовать идентификатор базы данных =.</span><span class="sxs-lookup"><span data-stu-id="f3240-114">The path as shown in the following table is the full path for the directory containing the database files and must be preceded by the identifier DATABASE=.</span></span> <span data-ttu-id="f3240-115">В некоторых случаях (как с помощью Microsoft Excel и Microsoft Access базы данных базами данных, ядро) должен включать имя файла в качестве аргумента базы данных.</span><span class="sxs-lookup"><span data-stu-id="f3240-115">In some cases (as with Microsoft Excel and Microsoft Access database engine databases), you should include a specific file name in the database path argument.</span></span>

<span data-ttu-id="f3240-116">Ниже приведены возможные типы и баз данных и их соответствующие спецификаторы базы данных пути для настройки свойства **подключения** .</span><span class="sxs-lookup"><span data-stu-id="f3240-116">The following table shows possible database types and their corresponding database specifiers and paths for the **Connect** property setting.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f3240-117">Тип базы данных</span><span class="sxs-lookup"><span data-stu-id="f3240-117">Database type</span></span></p></th>
<th><p><span data-ttu-id="f3240-118">Описателя</span><span class="sxs-lookup"><span data-stu-id="f3240-118">Specifier</span></span></p></th>
<th><p><span data-ttu-id="f3240-119">Пример</span><span class="sxs-lookup"><span data-stu-id="f3240-119">Example</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f3240-120">Базы данных Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="f3240-120">Microsoft Access Database</span></span></p></td>
<td><p><span data-ttu-id="f3240-121">База данных [];</span><span class="sxs-lookup"><span data-stu-id="f3240-121">[database];</span></span></p></td>
<td><p><span data-ttu-id="f3240-122">диск: \path\filename</span><span class="sxs-lookup"><span data-stu-id="f3240-122">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3240-123">dBASE III</span><span class="sxs-lookup"><span data-stu-id="f3240-123">dBASE III</span></span></p></td>
<td><p><span data-ttu-id="f3240-124">dBASE III;</span><span class="sxs-lookup"><span data-stu-id="f3240-124">dBASE III;</span></span></p></td>
<td><p><span data-ttu-id="f3240-125">диск: \path</span><span class="sxs-lookup"><span data-stu-id="f3240-125">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f3240-126">dBASE IV</span><span class="sxs-lookup"><span data-stu-id="f3240-126">dBASE IV</span></span></p></td>
<td><p><span data-ttu-id="f3240-127">dBASE IV;</span><span class="sxs-lookup"><span data-stu-id="f3240-127">dBASE IV;</span></span></p></td>
<td><p><span data-ttu-id="f3240-128">диск: \path</span><span class="sxs-lookup"><span data-stu-id="f3240-128">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3240-129">dBASE 5</span><span class="sxs-lookup"><span data-stu-id="f3240-129">dBASE 5</span></span></p></td>
<td><p><span data-ttu-id="f3240-130">dBASE 5.0;</span><span class="sxs-lookup"><span data-stu-id="f3240-130">dBASE 5.0;</span></span></p></td>
<td><p><span data-ttu-id="f3240-131">диск: \path</span><span class="sxs-lookup"><span data-stu-id="f3240-131">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f3240-132">Paradox 3.x</span><span class="sxs-lookup"><span data-stu-id="f3240-132">Paradox 3.x</span></span></p></td>
<td><p><span data-ttu-id="f3240-133">Paradox 3.x;</span><span class="sxs-lookup"><span data-stu-id="f3240-133">Paradox 3.x;</span></span></p></td>
<td><p><span data-ttu-id="f3240-134">диск: \path</span><span class="sxs-lookup"><span data-stu-id="f3240-134">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3240-135">Paradox 4.x</span><span class="sxs-lookup"><span data-stu-id="f3240-135">Paradox 4.x</span></span></p></td>
<td><p><span data-ttu-id="f3240-136">Paradox 4.x;</span><span class="sxs-lookup"><span data-stu-id="f3240-136">Paradox 4.x;</span></span></p></td>
<td><p><span data-ttu-id="f3240-137">диск: \path</span><span class="sxs-lookup"><span data-stu-id="f3240-137">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f3240-138">Paradox 5.x</span><span class="sxs-lookup"><span data-stu-id="f3240-138">Paradox 5.x</span></span></p></td>
<td><p><span data-ttu-id="f3240-139">Paradox 5.x;</span><span class="sxs-lookup"><span data-stu-id="f3240-139">Paradox 5.x;</span></span></p></td>
<td><p><span data-ttu-id="f3240-140">диск: \path</span><span class="sxs-lookup"><span data-stu-id="f3240-140">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3240-141">Microsoft Excel 3.0</span><span class="sxs-lookup"><span data-stu-id="f3240-141">Microsoft Excel 3.0</span></span></p></td>
<td><p><span data-ttu-id="f3240-142">Excel 3.0;</span><span class="sxs-lookup"><span data-stu-id="f3240-142">Excel 3.0;</span></span></p></td>
<td><p><span data-ttu-id="f3240-143">Drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="f3240-143">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f3240-144">Microsoft Excel 4.0</span><span class="sxs-lookup"><span data-stu-id="f3240-144">Microsoft Excel 4.0</span></span></p></td>
<td><p><span data-ttu-id="f3240-145">Excel 4.0;</span><span class="sxs-lookup"><span data-stu-id="f3240-145">Excel 4.0;</span></span></p></td>
<td><p><span data-ttu-id="f3240-146">Drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="f3240-146">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3240-147">Microsoft Excel 5.0 или Microsoft Excel 95</span><span class="sxs-lookup"><span data-stu-id="f3240-147">Microsoft Excel 5.0 or Microsoft Excel 95</span></span></p></td>
<td><p><span data-ttu-id="f3240-148">Excel 5.0;</span><span class="sxs-lookup"><span data-stu-id="f3240-148">Excel 5.0;</span></span></p></td>
<td><p><span data-ttu-id="f3240-149">Drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="f3240-149">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f3240-150">Microsoft Excel 97</span><span class="sxs-lookup"><span data-stu-id="f3240-150">Microsoft Excel 97</span></span></p></td>
<td><p><span data-ttu-id="f3240-151">Excel 8.0;</span><span class="sxs-lookup"><span data-stu-id="f3240-151">Excel 8.0;</span></span></p></td>
<td><p><span data-ttu-id="f3240-152">Drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="f3240-152">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3240-153">Lotus 1-2-3 WKS и WK1</span><span class="sxs-lookup"><span data-stu-id="f3240-153">Lotus 1-2-3 WKS and WK1</span></span></p></td>
<td><p><span data-ttu-id="f3240-154">Lotus WK1;</span><span class="sxs-lookup"><span data-stu-id="f3240-154">Lotus WK1;</span></span></p></td>
<td><p><span data-ttu-id="f3240-155">Drive:\path\filename.WK1</span><span class="sxs-lookup"><span data-stu-id="f3240-155">drive:\path\filename.wk1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f3240-156">WK3 Lotus 1-2-3</span><span class="sxs-lookup"><span data-stu-id="f3240-156">Lotus 1-2-3 WK3</span></span></p></td>
<td><p><span data-ttu-id="f3240-157">Lotus WK3;</span><span class="sxs-lookup"><span data-stu-id="f3240-157">Lotus WK3;</span></span></p></td>
<td><p><span data-ttu-id="f3240-158">Drive:\path\filename.WK3</span><span class="sxs-lookup"><span data-stu-id="f3240-158">drive:\path\filename.wk3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3240-159">WK4 Lotus 1-2-3</span><span class="sxs-lookup"><span data-stu-id="f3240-159">Lotus 1-2-3 WK4</span></span></p></td>
<td><p><span data-ttu-id="f3240-160">Lotus WK4;</span><span class="sxs-lookup"><span data-stu-id="f3240-160">Lotus WK4;</span></span></p></td>
<td><p><span data-ttu-id="f3240-161">Drive:\path\filename.WK4</span><span class="sxs-lookup"><span data-stu-id="f3240-161">drive:\path\filename.wk4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f3240-162">Импорт HTML</span><span class="sxs-lookup"><span data-stu-id="f3240-162">HTML Import</span></span></p></td>
<td><p><span data-ttu-id="f3240-163">Импорт HTML;</span><span class="sxs-lookup"><span data-stu-id="f3240-163">HTML Import;</span></span></p></td>
<td><p><span data-ttu-id="f3240-164">диск: \path\filename</span><span class="sxs-lookup"><span data-stu-id="f3240-164">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3240-165">Экспорт HTML</span><span class="sxs-lookup"><span data-stu-id="f3240-165">HTML Export</span></span></p></td>
<td><p><span data-ttu-id="f3240-166">Экспорт HTML;</span><span class="sxs-lookup"><span data-stu-id="f3240-166">HTML Export;</span></span></p></td>
<td><p><span data-ttu-id="f3240-167">диск: \path</span><span class="sxs-lookup"><span data-stu-id="f3240-167">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f3240-168">Текст</span><span class="sxs-lookup"><span data-stu-id="f3240-168">Text</span></span></p></td>
<td><p><span data-ttu-id="f3240-169">Текст;</span><span class="sxs-lookup"><span data-stu-id="f3240-169">Text;</span></span></p></td>
<td><p><span data-ttu-id="f3240-170">диск: \path</span><span class="sxs-lookup"><span data-stu-id="f3240-170">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3240-171">Open Database Connectivity</span><span class="sxs-lookup"><span data-stu-id="f3240-171">ODBC</span></span></p></td>
<td><p><span data-ttu-id="f3240-172">ODBC. Базы данных = база данных; UID = пользователя; PWD = пароля; Уведомления о Доставке = источнику данных; [LOGINTIMEOUT = секунды;]</span><span class="sxs-lookup"><span data-stu-id="f3240-172">ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</span></span></p></td>
<td><p><span data-ttu-id="f3240-173">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="f3240-173">None</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f3240-174">Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="f3240-174">Microsoft Exchange</span></span></p></td>
<td><p><span data-ttu-id="f3240-175">Exchange 4.0; MAPILEVEL = folderpath; [TABLETYPE = {0 | 1}]; [ПРОФИЛЕЙ = профиля;] [PWD = пароль;] [Базы данных = база данных;]</span><span class="sxs-lookup"><span data-stu-id="f3240-175">Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</span></span></p></td>
<td><p><span data-ttu-id="f3240-176">диск: \path\filename</span><span class="sxs-lookup"><span data-stu-id="f3240-176">drive:\path\filename</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f3240-177">Соответствует только «ODBC;», драйвер ODBC отображает диалоговое окно со списком всех зарегистрированных имен источников данных ODBC, чтобы пользователь может выбрать базу данных.</span><span class="sxs-lookup"><span data-stu-id="f3240-177">If the specifier is only "ODBC;", the ODBC driver displays a dialog box listing all registered ODBC data source names so that the user can select a database.</span></span>

<span data-ttu-id="f3240-178">Если пароль требуется, но не указан в параметре свойства **подключения** , диалоговое окно входа в систему отображается впервые таблицам драйвер ODBC и снова закрыто и повторно открыть подключение.</span><span class="sxs-lookup"><span data-stu-id="f3240-178">If a password is required but not provided in the **Connect** property setting, a login dialog box is displayed the first time a table is accessed by the ODBC driver and again if the connection is closed and reopened.</span></span>

<span data-ttu-id="f3240-179">Для данных в Microsoft Exchange требуется ключ MAPILEVEL должно быть присвоено полностью разрешить пути (например, «почтовый ящик – Pat SmithIAlpha/текущую»).</span><span class="sxs-lookup"><span data-stu-id="f3240-179">For data in Microsoft Exchange, the required MAPILEVEL key should be set to a fully-resolved folder path (for example, "Mailbox - Pat SmithIAlpha/Today").</span></span> <span data-ttu-id="f3240-180">Путь не включает имя папки, которая будет открыта в виде таблицы; Вместо этого следует указать имя этой папки в качестве аргумента имя метода **CreateTable** .</span><span class="sxs-lookup"><span data-stu-id="f3240-180">The path does not include the name of the folder that will be opened as a table; that folder’s name should instead be specified as the name argument to the **CreateTable** method.</span></span> <span data-ttu-id="f3240-181">Клавиша TABLETYPE должно быть присвоено значение «0» откройте папку (по умолчанию) или «1», чтобы открыть адресную книгу.</span><span class="sxs-lookup"><span data-stu-id="f3240-181">The TABLETYPE key should be set to "0" to open a folder (default) or "1" to open an address book.</span></span> <span data-ttu-id="f3240-182">В настоящее время с помощью ключа ПРОФИЛЯ по умолчанию к профилю.</span><span class="sxs-lookup"><span data-stu-id="f3240-182">The PROFILE key defaults to the profile currently in use.</span></span>

<span data-ttu-id="f3240-183">Для базовых таблиц в базе данных Micorosoft Access значение свойства **подключение** является строкой нулевой длины (»»).</span><span class="sxs-lookup"><span data-stu-id="f3240-183">For base tables in a Micorosoft Access database, the **Connect** property setting is a zero-length string ("").</span></span>

<span data-ttu-id="f3240-184">Свойства **подключения** для объекта **базы данных** с указанием исходный аргумент методу **OpenDatabase** .</span><span class="sxs-lookup"><span data-stu-id="f3240-184">You can set the **Connect** property for a **Database** object by providing a source argument to the **OpenDatabase** method.</span></span> <span data-ttu-id="f3240-185">Чтобы проверить параметр, чтобы определить тип, путь, идентификатор пользователя, пароль или источник данных ODBC базы данных.</span><span class="sxs-lookup"><span data-stu-id="f3240-185">You can check the setting to determine the type, path, user ID, password, or ODBC data source of the database.</span></span>

<span data-ttu-id="f3240-186">Для объекта **QueryDef** в рабочую область для Microsoft Access можно использовать свойство **подключение** с помощью свойства ReturnsRecords для создания запроса к серверу ODBC SQL.</span><span class="sxs-lookup"><span data-stu-id="f3240-186">On a **QueryDef** object in a Microsoft Access workspace, you can use the **Connect** property with the ReturnsRecords property to create an ODBC SQL pass-through query.</span></span> <span data-ttu-id="f3240-187">В оставшейся части строки содержит сведения, относящиеся к драйвера ODBC, используемого для доступа к удаленным данным databasetype строку подключения — «ODBC;»</span><span class="sxs-lookup"><span data-stu-id="f3240-187">The databasetype of the connection string is "ODBC;", and the remainder of the string contains information specific to the ODBC driver used to access the remote data.</span></span> <span data-ttu-id="f3240-188">Для получения дополнительных сведений см драйвера.</span><span class="sxs-lookup"><span data-stu-id="f3240-188">For more information, see the documentation for the specific driver.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="f3240-189">Необходимо установить свойство <STRONG>подключение</STRONG> , прежде чем задать свойство <STRONG>ReturnsRecords</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="f3240-189">You must set the <STRONG>Connect</STRONG> property before you set the <STRONG>ReturnsRecords</STRONG> property.</span></span></P>
> <LI>
> <P><span data-ttu-id="f3240-190">Необходимо иметь разрешения доступа на компьютере, где размещается сервер базы данных, который вы пытаетесь получить доступ к.</span><span class="sxs-lookup"><span data-stu-id="f3240-190">You must have access permissions to the computer that contains the database server you're trying to access.</span></span></P></LI></UL>


