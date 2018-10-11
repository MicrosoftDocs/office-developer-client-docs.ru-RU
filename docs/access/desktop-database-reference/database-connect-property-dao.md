---
title: Database.Connect Property (DAO)
TOCTitle: Connect Property
ms:assetid: c3e511a6-baef-3758-cfb1-3459b0b19cf3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823048(v=office.15)
ms:contentKeyID: 48547578
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3ccc238940ec75b04cf900fbc6604df7b41d2ca4
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480526"
---
# <a name="databaseconnect-property-dao"></a><span data-ttu-id="b842c-102">Database.Connect Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="b842c-102">Database.Connect Property (DAO)</span></span>


<span data-ttu-id="b842c-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b842c-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b842c-104">Задает или возвращает значение, которое содержит сведения об источнике открыть базу данных.</span><span class="sxs-lookup"><span data-stu-id="b842c-104">Sets or returns a value that provides information about the source an open database.</span></span> <span data-ttu-id="b842c-105">Для чтения и записи, **String**.</span><span class="sxs-lookup"><span data-stu-id="b842c-105">Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b842c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b842c-106">Syntax</span></span>

<span data-ttu-id="b842c-107">*выражение* . Подключение</span><span class="sxs-lookup"><span data-stu-id="b842c-107">*expression* .Connect</span></span>

<span data-ttu-id="b842c-108">*выражение* Переменная, которая представляет собой объект **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="b842c-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b842c-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="b842c-109">Remarks</span></span>

<span data-ttu-id="b842c-110">Настройка свойства **подключение** — **строка** состоит из спецификатора типа базы данных и ноль или больше параметров, разделенных точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="b842c-110">The **Connect** property setting is a **String** composed of a database type specifier and zero or more parameters separated by semicolons.</span></span> <span data-ttu-id="b842c-111">Свойство **Connect** передает Дополнительные сведения о ODBC и драйверы некоторых ISAM при необходимости.</span><span class="sxs-lookup"><span data-stu-id="b842c-111">The **Connect** property passes additional information to ODBC and certain ISAM drivers as needed.</span></span>

<span data-ttu-id="b842c-112">Для выполнения запроса к серверу для таблица, связанная с файла базы данных Microsoft Access, сначала необходимо задать свойство **подключение** базы данных, связанной таблицы допустимая строка подключения ODBC.</span><span class="sxs-lookup"><span data-stu-id="b842c-112">To perform an SQL pass-through query on a table linked to your Microsoft Access database file, you must first set the **Connect** property of the linked table's database to a valid ODBC connection string.</span></span>

<span data-ttu-id="b842c-113">Путь, как показано в следующей таблице — это полный путь к каталогу, содержащему файлы базы данных и должен предшествовать идентификатор базы данных =.</span><span class="sxs-lookup"><span data-stu-id="b842c-113">The path as shown in the following table is the full path for the directory containing the database files and must be preceded by the identifier DATABASE=.</span></span> <span data-ttu-id="b842c-114">В некоторых случаях (как с помощью Microsoft Excel и Microsoft Access базы данных базами данных, ядро) должен включать имя файла в качестве аргумента базы данных.</span><span class="sxs-lookup"><span data-stu-id="b842c-114">In some cases (as with Microsoft Excel and Microsoft Access database engine databases), you should include a specific file name in the database path argument.</span></span>

<span data-ttu-id="b842c-115">Ниже приведены возможные типы и баз данных и их соответствующие спецификаторы базы данных пути для настройки свойства **подключения** .</span><span class="sxs-lookup"><span data-stu-id="b842c-115">The following table shows possible database types and their corresponding database specifiers and paths for the **Connect** property setting.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b842c-116">Тип базы данных</span><span class="sxs-lookup"><span data-stu-id="b842c-116">Database type</span></span></p></th>
<th><p><span data-ttu-id="b842c-117">Описателя</span><span class="sxs-lookup"><span data-stu-id="b842c-117">Specifier</span></span></p></th>
<th><p><span data-ttu-id="b842c-118">Пример</span><span class="sxs-lookup"><span data-stu-id="b842c-118">Example</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b842c-119">Базы данных Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="b842c-119">Microsoft Access Database</span></span></p></td>
<td><p><span data-ttu-id="b842c-120">База данных [];</span><span class="sxs-lookup"><span data-stu-id="b842c-120">[database];</span></span></p></td>
<td><p><span data-ttu-id="b842c-121">диск: \path\filename</span><span class="sxs-lookup"><span data-stu-id="b842c-121">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b842c-122">dBASE III</span><span class="sxs-lookup"><span data-stu-id="b842c-122">dBASE III</span></span></p></td>
<td><p><span data-ttu-id="b842c-123">dBASE III;</span><span class="sxs-lookup"><span data-stu-id="b842c-123">dBASE III;</span></span></p></td>
<td><p><span data-ttu-id="b842c-124">диск: \path</span><span class="sxs-lookup"><span data-stu-id="b842c-124">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b842c-125">dBASE IV</span><span class="sxs-lookup"><span data-stu-id="b842c-125">dBASE IV</span></span></p></td>
<td><p><span data-ttu-id="b842c-126">dBASE IV;</span><span class="sxs-lookup"><span data-stu-id="b842c-126">dBASE IV;</span></span></p></td>
<td><p><span data-ttu-id="b842c-127">диск: \path</span><span class="sxs-lookup"><span data-stu-id="b842c-127">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b842c-128">dBASE 5</span><span class="sxs-lookup"><span data-stu-id="b842c-128">dBASE 5</span></span></p></td>
<td><p><span data-ttu-id="b842c-129">dBASE 5.0;</span><span class="sxs-lookup"><span data-stu-id="b842c-129">dBASE 5.0;</span></span></p></td>
<td><p><span data-ttu-id="b842c-130">диск: \path</span><span class="sxs-lookup"><span data-stu-id="b842c-130">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b842c-131">Paradox 3.x</span><span class="sxs-lookup"><span data-stu-id="b842c-131">Paradox 3.x</span></span></p></td>
<td><p><span data-ttu-id="b842c-132">Paradox 3.x;</span><span class="sxs-lookup"><span data-stu-id="b842c-132">Paradox 3.x;</span></span></p></td>
<td><p><span data-ttu-id="b842c-133">диск: \path</span><span class="sxs-lookup"><span data-stu-id="b842c-133">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b842c-134">Paradox 4.x</span><span class="sxs-lookup"><span data-stu-id="b842c-134">Paradox 4.x</span></span></p></td>
<td><p><span data-ttu-id="b842c-135">Paradox 4.x;</span><span class="sxs-lookup"><span data-stu-id="b842c-135">Paradox 4.x;</span></span></p></td>
<td><p><span data-ttu-id="b842c-136">диск: \path</span><span class="sxs-lookup"><span data-stu-id="b842c-136">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b842c-137">Paradox 5.x</span><span class="sxs-lookup"><span data-stu-id="b842c-137">Paradox 5.x</span></span></p></td>
<td><p><span data-ttu-id="b842c-138">Paradox 5.x;</span><span class="sxs-lookup"><span data-stu-id="b842c-138">Paradox 5.x;</span></span></p></td>
<td><p><span data-ttu-id="b842c-139">диск: \path</span><span class="sxs-lookup"><span data-stu-id="b842c-139">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b842c-140">Microsoft Excel 3.0</span><span class="sxs-lookup"><span data-stu-id="b842c-140">Microsoft Excel 3.0</span></span></p></td>
<td><p><span data-ttu-id="b842c-141">Excel 3.0;</span><span class="sxs-lookup"><span data-stu-id="b842c-141">Excel 3.0;</span></span></p></td>
<td><p><span data-ttu-id="b842c-142">Drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="b842c-142">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b842c-143">Microsoft Excel 4.0</span><span class="sxs-lookup"><span data-stu-id="b842c-143">Microsoft Excel 4.0</span></span></p></td>
<td><p><span data-ttu-id="b842c-144">Excel 4.0;</span><span class="sxs-lookup"><span data-stu-id="b842c-144">Excel 4.0;</span></span></p></td>
<td><p><span data-ttu-id="b842c-145">Drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="b842c-145">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b842c-146">Microsoft Excel 5.0 или Microsoft Excel 95</span><span class="sxs-lookup"><span data-stu-id="b842c-146">Microsoft Excel 5.0 or Microsoft Excel 95</span></span></p></td>
<td><p><span data-ttu-id="b842c-147">Excel 5.0;</span><span class="sxs-lookup"><span data-stu-id="b842c-147">Excel 5.0;</span></span></p></td>
<td><p><span data-ttu-id="b842c-148">Drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="b842c-148">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b842c-149">Microsoft Excel 97</span><span class="sxs-lookup"><span data-stu-id="b842c-149">Microsoft Excel 97</span></span></p></td>
<td><p><span data-ttu-id="b842c-150">Excel 8.0;</span><span class="sxs-lookup"><span data-stu-id="b842c-150">Excel 8.0;</span></span></p></td>
<td><p><span data-ttu-id="b842c-151">Drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="b842c-151">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b842c-152">Lotus 1-2-3 WKS и WK1</span><span class="sxs-lookup"><span data-stu-id="b842c-152">Lotus 1-2-3 WKS and WK1</span></span></p></td>
<td><p><span data-ttu-id="b842c-153">Lotus WK1;</span><span class="sxs-lookup"><span data-stu-id="b842c-153">Lotus WK1;</span></span></p></td>
<td><p><span data-ttu-id="b842c-154">Drive:\path\filename.WK1</span><span class="sxs-lookup"><span data-stu-id="b842c-154">drive:\path\filename.wk1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b842c-155">WK3 Lotus 1-2-3</span><span class="sxs-lookup"><span data-stu-id="b842c-155">Lotus 1-2-3 WK3</span></span></p></td>
<td><p><span data-ttu-id="b842c-156">Lotus WK3;</span><span class="sxs-lookup"><span data-stu-id="b842c-156">Lotus WK3;</span></span></p></td>
<td><p><span data-ttu-id="b842c-157">Drive:\path\filename.WK3</span><span class="sxs-lookup"><span data-stu-id="b842c-157">drive:\path\filename.wk3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b842c-158">WK4 Lotus 1-2-3</span><span class="sxs-lookup"><span data-stu-id="b842c-158">Lotus 1-2-3 WK4</span></span></p></td>
<td><p><span data-ttu-id="b842c-159">Lotus WK4;</span><span class="sxs-lookup"><span data-stu-id="b842c-159">Lotus WK4;</span></span></p></td>
<td><p><span data-ttu-id="b842c-160">Drive:\path\filename.WK4</span><span class="sxs-lookup"><span data-stu-id="b842c-160">drive:\path\filename.wk4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b842c-161">Импорт HTML</span><span class="sxs-lookup"><span data-stu-id="b842c-161">HTML Import</span></span></p></td>
<td><p><span data-ttu-id="b842c-162">Импорт HTML;</span><span class="sxs-lookup"><span data-stu-id="b842c-162">HTML Import;</span></span></p></td>
<td><p><span data-ttu-id="b842c-163">диск: \path\filename</span><span class="sxs-lookup"><span data-stu-id="b842c-163">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b842c-164">Экспорт HTML</span><span class="sxs-lookup"><span data-stu-id="b842c-164">HTML Export</span></span></p></td>
<td><p><span data-ttu-id="b842c-165">Экспорт HTML;</span><span class="sxs-lookup"><span data-stu-id="b842c-165">HTML Export;</span></span></p></td>
<td><p><span data-ttu-id="b842c-166">диск: \path</span><span class="sxs-lookup"><span data-stu-id="b842c-166">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b842c-167">Текст</span><span class="sxs-lookup"><span data-stu-id="b842c-167">Text</span></span></p></td>
<td><p><span data-ttu-id="b842c-168">Текст;</span><span class="sxs-lookup"><span data-stu-id="b842c-168">Text;</span></span></p></td>
<td><p><span data-ttu-id="b842c-169">диск: \path</span><span class="sxs-lookup"><span data-stu-id="b842c-169">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b842c-170">Open Database Connectivity</span><span class="sxs-lookup"><span data-stu-id="b842c-170">ODBC</span></span></p></td>
<td><p><span data-ttu-id="b842c-171">ODBC. Базы данных = база данных; UID = пользователя; PWD = пароля; Уведомления о Доставке = источнику данных; [LOGINTIMEOUT = секунды;]</span><span class="sxs-lookup"><span data-stu-id="b842c-171">ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</span></span></p></td>
<td><p><span data-ttu-id="b842c-172">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="b842c-172">None</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b842c-173">Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="b842c-173">Microsoft Exchange</span></span></p></td>
<td><p><span data-ttu-id="b842c-174">Exchange 4.0; MAPILEVEL = folderpath; [TABLETYPE = {0 | 1}]; [ПРОФИЛЕЙ = профиля;] [PWD = пароль;] [Базы данных = база данных;]</span><span class="sxs-lookup"><span data-stu-id="b842c-174">Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</span></span></p></td>
<td><p><span data-ttu-id="b842c-175">диск: \path\filename</span><span class="sxs-lookup"><span data-stu-id="b842c-175">drive:\path\filename</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b842c-176">Соответствует только «ODBC;», драйвер ODBC отображает диалоговое окно со списком всех зарегистрированных имен источников данных ODBC, чтобы пользователь может выбрать базу данных.</span><span class="sxs-lookup"><span data-stu-id="b842c-176">If the specifier is only "ODBC;", the ODBC driver displays a dialog box listing all registered ODBC data source names so that the user can select a database.</span></span>

<span data-ttu-id="b842c-177">Если пароль требуется, но не указан в параметре свойства **подключения** , диалоговое окно входа в систему отображается впервые таблицам драйвер ODBC и снова закрыто и повторно открыть подключение.</span><span class="sxs-lookup"><span data-stu-id="b842c-177">If a password is required but not provided in the **Connect** property setting, a login dialog box is displayed the first time a table is accessed by the ODBC driver and again if the connection is closed and reopened.</span></span>

<span data-ttu-id="b842c-178">Для данных в Microsoft Exchange требуется ключ MAPILEVEL должно быть присвоено полностью разрешить пути (например, «почтовый ящик – Pat SmithIAlpha/текущую»).</span><span class="sxs-lookup"><span data-stu-id="b842c-178">For data in Microsoft Exchange, the required MAPILEVEL key should be set to a fully-resolved folder path (for example, "Mailbox - Pat SmithIAlpha/Today").</span></span> <span data-ttu-id="b842c-179">Путь не включает имя папки, которая будет открыта в виде таблицы; Вместо этого следует указать имя этой папки в качестве аргумента имя метода **CreateTable** .</span><span class="sxs-lookup"><span data-stu-id="b842c-179">The path does not include the name of the folder that will be opened as a table; that folder’s name should instead be specified as the name argument to the **CreateTable** method.</span></span> <span data-ttu-id="b842c-180">Клавиша TABLETYPE должно быть присвоено значение «0» откройте папку (по умолчанию) или «1», чтобы открыть адресную книгу.</span><span class="sxs-lookup"><span data-stu-id="b842c-180">The TABLETYPE key should be set to "0" to open a folder (default) or "1" to open an address book.</span></span> <span data-ttu-id="b842c-181">В настоящее время с помощью ключа ПРОФИЛЯ по умолчанию к профилю.</span><span class="sxs-lookup"><span data-stu-id="b842c-181">The PROFILE key defaults to the profile currently in use.</span></span>

<span data-ttu-id="b842c-182">Свойства **подключения** для объекта **базы данных** с указанием исходный аргумент методу **OpenDatabase** .</span><span class="sxs-lookup"><span data-stu-id="b842c-182">You can set the **Connect** property for a **Database** object by providing a source argument to the **OpenDatabase** method.</span></span> <span data-ttu-id="b842c-183">Чтобы проверить параметр, чтобы определить тип, путь, идентификатор пользователя, пароль или источник данных ODBC базы данных.</span><span class="sxs-lookup"><span data-stu-id="b842c-183">You can check the setting to determine the type, path, user ID, password, or ODBC data source of the database.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="b842c-184">Необходимо установить свойство <STRONG>подключение</STRONG> , прежде чем задать свойство <STRONG>ReturnsRecords</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="b842c-184">You must set the <STRONG>Connect</STRONG> property before you set the <STRONG>ReturnsRecords</STRONG> property.</span></span></P>
> <LI>
> <P><span data-ttu-id="b842c-185">Необходимо иметь разрешения доступа на компьютере, где размещается сервер базы данных, который вы пытаетесь получить доступ к.</span><span class="sxs-lookup"><span data-stu-id="b842c-185">You must have access permissions to the computer that contains the database server you're trying to access.</span></span></P></LI></UL>


