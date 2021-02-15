---
title: Свойство QueryDef.Connect (DAO)
TOCTitle: Connect Property
ms:assetid: 14f19205-e92e-acc6-5677-b6d88772d5da
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845479(v=office.15)
ms:contentKeyID: 48543398
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 009e49a96ea1cd5ee3db0b96adb9cae4a6bce21b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301087"
---
# <a name="querydefconnect-property-dao"></a><span data-ttu-id="bf860-102">Свойство QueryDef.Connect (DAO)</span><span class="sxs-lookup"><span data-stu-id="bf860-102">QueryDef.Connect property (DAO)</span></span>

<span data-ttu-id="bf860-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bf860-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bf860-104">Задает или возвращает значение, которое предоставляет сведения об источнике базы данных, используемой в сквозных запросах.</span><span class="sxs-lookup"><span data-stu-id="bf860-104">Sets or returns a value that provides information about the source of database used in a pass-through query.</span></span> <span data-ttu-id="bf860-105">Только для чтения, **String**.</span><span class="sxs-lookup"><span data-stu-id="bf860-105">Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf860-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bf860-106">Syntax</span></span>

<span data-ttu-id="bf860-107">*expression* .Connect</span><span class="sxs-lookup"><span data-stu-id="bf860-107">*expression* .Connect</span></span>

<span data-ttu-id="bf860-108">*выражение*: переменная, представляющая объект **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="bf860-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf860-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="bf860-109">Remarks</span></span>

<span data-ttu-id="bf860-110">Параметры свойства **Connect** сохранены в **String**, состоящей из указателя типа базы данных и нуля либо нескольких параметров, разделенных точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="bf860-110">The **Connect** property setting is a **String** composed of a database type specifier and zero or more parameters separated by semicolons.</span></span> <span data-ttu-id="bf860-111">Свойство **Connect** передает дополнительные сведения для ODBC и определенным драйверам ISAM при необходимости.</span><span class="sxs-lookup"><span data-stu-id="bf860-111">The **Connect** property passes additional information to ODBC and certain ISAM drivers as needed.</span></span>

<span data-ttu-id="bf860-112">Чтобы выполнить SQL для таблицы, связанной с файлом базы данных Microsoft Access, необходимо сначала установить для свойства **Connect** базы данных связанной таблицы допустимую строку подключения ODBC.</span><span class="sxs-lookup"><span data-stu-id="bf860-112">To perform an SQL pass-through query on a table linked to your Microsoft Access database file, you must first set the **Connect** property of the linked table's database to a valid ODBC connection string.</span></span>

<span data-ttu-id="bf860-113">Путь, как показано в приведенной ниже таблице, содержит полный путь к каталогу, содержащему файлы базы данных, и должен иметь впереди идентификатор DATABASE=.</span><span class="sxs-lookup"><span data-stu-id="bf860-113">The path as shown in the following table is the full path for the directory containing the database files and must be preceded by the identifier DATABASE=.</span></span> <span data-ttu-id="bf860-114">В некоторых случаях (как в случае с базами данных Microsoft Excel и ядра СУБД Microsoft Access) следует включить конкретное имя файла в аргумент пути к базе данных.</span><span class="sxs-lookup"><span data-stu-id="bf860-114">In some cases (as with Microsoft Excel and Microsoft Access database engine databases), you should include a specific file name in the database path argument.</span></span>

<span data-ttu-id="bf860-115">Таблица ниже содержит возможные типы базы данных и соответствующие указатели базы данных и пути к параметрам свойства **Connect**.</span><span class="sxs-lookup"><span data-stu-id="bf860-115">The following table shows possible database types and their corresponding database specifiers and paths for the **Connect** property setting.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bf860-116">Тип базы данных</span><span class="sxs-lookup"><span data-stu-id="bf860-116">Database type</span></span></p></th>
<th><p><span data-ttu-id="bf860-117">Указатель</span><span class="sxs-lookup"><span data-stu-id="bf860-117">Specifier</span></span></p></th>
<th><p><span data-ttu-id="bf860-118">Пример</span><span class="sxs-lookup"><span data-stu-id="bf860-118">Example</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bf860-119">База данных Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="bf860-119">Microsoft Access Database</span></span></p></td>
<td><p><span data-ttu-id="bf860-120">[database];</span><span class="sxs-lookup"><span data-stu-id="bf860-120">[database];</span></span></p></td>
<td><p><span data-ttu-id="bf860-121">диск: \путь\имяфайла</span><span class="sxs-lookup"><span data-stu-id="bf860-121">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf860-122">dBASE III</span><span class="sxs-lookup"><span data-stu-id="bf860-122">dBASE III</span></span></p></td>
<td><p><span data-ttu-id="bf860-123">dBASE III;</span><span class="sxs-lookup"><span data-stu-id="bf860-123">dBASE III;</span></span></p></td>
<td><p><span data-ttu-id="bf860-124">диск: \путь</span><span class="sxs-lookup"><span data-stu-id="bf860-124">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf860-125">dBASE IV</span><span class="sxs-lookup"><span data-stu-id="bf860-125">dBASE IV</span></span></p></td>
<td><p><span data-ttu-id="bf860-126">dBASE IV;</span><span class="sxs-lookup"><span data-stu-id="bf860-126">dBASE IV;</span></span></p></td>
<td><p><span data-ttu-id="bf860-127">диск: \путь</span><span class="sxs-lookup"><span data-stu-id="bf860-127">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf860-128">dBASE 5</span><span class="sxs-lookup"><span data-stu-id="bf860-128">dBASE 5</span></span></p></td>
<td><p><span data-ttu-id="bf860-129">dBASE 5.0;</span><span class="sxs-lookup"><span data-stu-id="bf860-129">dBASE 5.0;</span></span></p></td>
<td><p><span data-ttu-id="bf860-130">диск: \путь</span><span class="sxs-lookup"><span data-stu-id="bf860-130">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf860-131">Paradox 3.x</span><span class="sxs-lookup"><span data-stu-id="bf860-131">Paradox 3.x</span></span></p></td>
<td><p><span data-ttu-id="bf860-132">Paradox 3.x;</span><span class="sxs-lookup"><span data-stu-id="bf860-132">Paradox 3.x;</span></span></p></td>
<td><p><span data-ttu-id="bf860-133">диск: \путь</span><span class="sxs-lookup"><span data-stu-id="bf860-133">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf860-134">Paradox 4.x</span><span class="sxs-lookup"><span data-stu-id="bf860-134">Paradox 4.x</span></span></p></td>
<td><p><span data-ttu-id="bf860-135">Paradox 4.x;</span><span class="sxs-lookup"><span data-stu-id="bf860-135">Paradox 4.x;</span></span></p></td>
<td><p><span data-ttu-id="bf860-136">диск: \путь</span><span class="sxs-lookup"><span data-stu-id="bf860-136">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf860-137">Paradox 5.x</span><span class="sxs-lookup"><span data-stu-id="bf860-137">Paradox 5.x</span></span></p></td>
<td><p><span data-ttu-id="bf860-138">Paradox 5.x;</span><span class="sxs-lookup"><span data-stu-id="bf860-138">Paradox 5.x;</span></span></p></td>
<td><p><span data-ttu-id="bf860-139">диск: \путь</span><span class="sxs-lookup"><span data-stu-id="bf860-139">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf860-140">Microsoft Excel 3.0</span><span class="sxs-lookup"><span data-stu-id="bf860-140">Microsoft Excel 3.0</span></span></p></td>
<td><p><span data-ttu-id="bf860-141">Excel 3.0;</span><span class="sxs-lookup"><span data-stu-id="bf860-141">Excel 3.0;</span></span></p></td>
<td><p><span data-ttu-id="bf860-142">диск: \путь\имяфайла.xls</span><span class="sxs-lookup"><span data-stu-id="bf860-142">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf860-143">Microsoft Excel 4.0</span><span class="sxs-lookup"><span data-stu-id="bf860-143">Microsoft Excel 4.0</span></span></p></td>
<td><p><span data-ttu-id="bf860-144">Excel 4.0;</span><span class="sxs-lookup"><span data-stu-id="bf860-144">Excel 4.0;</span></span></p></td>
<td><p><span data-ttu-id="bf860-145">диск: \путь\имяфайла.xls</span><span class="sxs-lookup"><span data-stu-id="bf860-145">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf860-146">Microsoft Excel 5.0 или Microsoft Excel 95</span><span class="sxs-lookup"><span data-stu-id="bf860-146">Microsoft Excel 5.0 or Microsoft Excel 95</span></span></p></td>
<td><p><span data-ttu-id="bf860-147">Excel 5.0;</span><span class="sxs-lookup"><span data-stu-id="bf860-147">Excel 5.0;</span></span></p></td>
<td><p><span data-ttu-id="bf860-148">диск: \путь\имяфайла.xls</span><span class="sxs-lookup"><span data-stu-id="bf860-148">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf860-149">Microsoft Excel 97</span><span class="sxs-lookup"><span data-stu-id="bf860-149">Microsoft Excel 97</span></span></p></td>
<td><p><span data-ttu-id="bf860-150">Excel 8.0;</span><span class="sxs-lookup"><span data-stu-id="bf860-150">Excel 8.0;</span></span></p></td>
<td><p><span data-ttu-id="bf860-151">диск: \путь\имяфайла.xls</span><span class="sxs-lookup"><span data-stu-id="bf860-151">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf860-152">Lotus 1-2-3 WKS и WK1</span><span class="sxs-lookup"><span data-stu-id="bf860-152">Lotus 1-2-3 WKS and WK1</span></span></p></td>
<td><p><span data-ttu-id="bf860-153">Lotus WK1;</span><span class="sxs-lookup"><span data-stu-id="bf860-153">Lotus WK1;</span></span></p></td>
<td><p><span data-ttu-id="bf860-154">диск: \путь\имяфайла.wk1</span><span class="sxs-lookup"><span data-stu-id="bf860-154">drive:\path\filename.wk1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf860-155">Lotus 1-2-3 WK3</span><span class="sxs-lookup"><span data-stu-id="bf860-155">Lotus 1-2-3 WK3</span></span></p></td>
<td><p><span data-ttu-id="bf860-156">Lotus WK3;</span><span class="sxs-lookup"><span data-stu-id="bf860-156">Lotus WK3;</span></span></p></td>
<td><p><span data-ttu-id="bf860-157">диск: \путь\имяфайла.wk3</span><span class="sxs-lookup"><span data-stu-id="bf860-157">drive:\path\filename.wk3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf860-158">Lotus 1-2-3 WK4</span><span class="sxs-lookup"><span data-stu-id="bf860-158">Lotus 1-2-3 WK4</span></span></p></td>
<td><p><span data-ttu-id="bf860-159">Lotus WK4;</span><span class="sxs-lookup"><span data-stu-id="bf860-159">Lotus WK4;</span></span></p></td>
<td><p><span data-ttu-id="bf860-160">диск: \путь\имяфайла.wk4</span><span class="sxs-lookup"><span data-stu-id="bf860-160">drive:\path\filename.wk4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf860-161">HTML Import</span><span class="sxs-lookup"><span data-stu-id="bf860-161">HTML Import</span></span></p></td>
<td><p><span data-ttu-id="bf860-162">HTML Import;</span><span class="sxs-lookup"><span data-stu-id="bf860-162">HTML Import;</span></span></p></td>
<td><p><span data-ttu-id="bf860-163">диск: \путь\имяфайла</span><span class="sxs-lookup"><span data-stu-id="bf860-163">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf860-164">HTML Export</span><span class="sxs-lookup"><span data-stu-id="bf860-164">HTML Export</span></span></p></td>
<td><p><span data-ttu-id="bf860-165">HTML Export;</span><span class="sxs-lookup"><span data-stu-id="bf860-165">HTML Export;</span></span></p></td>
<td><p><span data-ttu-id="bf860-166">диск: \путь</span><span class="sxs-lookup"><span data-stu-id="bf860-166">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf860-167">Text</span><span class="sxs-lookup"><span data-stu-id="bf860-167">Text</span></span></p></td>
<td><p><span data-ttu-id="bf860-168">Text;</span><span class="sxs-lookup"><span data-stu-id="bf860-168">Text;</span></span></p></td>
<td><p><span data-ttu-id="bf860-169">диск: \путь</span><span class="sxs-lookup"><span data-stu-id="bf860-169">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf860-170">ODBC</span><span class="sxs-lookup"><span data-stu-id="bf860-170">ODBC</span></span></p></td>
<td><p><span data-ttu-id="bf860-171">ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</span><span class="sxs-lookup"><span data-stu-id="bf860-171">ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</span></span></p></td>
<td><p><span data-ttu-id="bf860-172">Нет</span><span class="sxs-lookup"><span data-stu-id="bf860-172">None</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf860-173">Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="bf860-173">Microsoft Exchange</span></span></p></td>
<td><p><span data-ttu-id="bf860-174">Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</span><span class="sxs-lookup"><span data-stu-id="bf860-174">Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</span></span></p></td>
<td><p><span data-ttu-id="bf860-175">диск: \путь\имяфайла</span><span class="sxs-lookup"><span data-stu-id="bf860-175">drive:\path\filename</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bf860-176">Если указан только ODBC, драйвер ODBC отображает диалоговое окно со всеми зарегистрированными именами источников данных ODBC, чтобы пользователь мог выбрать базу данных.</span><span class="sxs-lookup"><span data-stu-id="bf860-176">If the specifier is only "ODBC;", the ODBC driver displays a dialog box listing all registered ODBC data source names so that the user can select a database.</span></span>

<span data-ttu-id="bf860-177">Если пароль необходим, но не указан в параметрах свойства **Connect**, диалоговое окно входа отображается при первой попытке доступа к таблице со стороны драйвера ODBC и еще раз при закрытии и повторном установлении подключения.</span><span class="sxs-lookup"><span data-stu-id="bf860-177">If a password is required but not provided in the **Connect** property setting, a login dialog box is displayed the first time a table is accessed by the ODBC driver and again if the connection is closed and reopened.</span></span>

<span data-ttu-id="bf860-178">Для данных в Microsoft Exchange обязательный ключ MAPILEVEL должен иметь полностью разрешенный путь к папке (например, "Mailbox - Pat SmithIAlpha/Today").</span><span class="sxs-lookup"><span data-stu-id="bf860-178">For data in Microsoft Exchange, the required MAPILEVEL key should be set to a fully-resolved folder path (for example, "Mailbox - Pat SmithIAlpha/Today").</span></span> <span data-ttu-id="bf860-179">Путь не включает имя папки, которая будет открываться в качестве таблицы; вместо этого необходимо указать имя этой папки в качестве имени аргумента для метода **CreateTable**.</span><span class="sxs-lookup"><span data-stu-id="bf860-179">The path does not include the name of the folder that will be opened as a table; that folder’s name should instead be specified as the name argument to the **CreateTable** method.</span></span> <span data-ttu-id="bf860-180">Для ключа TABLETYPE должно быть установлено значение «0», чтобы открыть папку (по умолчанию) или «1», чтобы открыть адресную книгу.</span><span class="sxs-lookup"><span data-stu-id="bf860-180">The TABLETYPE key should be set to "0" to open a folder (default) or "1" to open an address book.</span></span> <span data-ttu-id="bf860-181">Ключ PROFILE по умолчанию относится к профилю, который в настоящее время используется.</span><span class="sxs-lookup"><span data-stu-id="bf860-181">The PROFILE key defaults to the profile currently in use.</span></span>

<span data-ttu-id="bf860-182">Для объекта **QueryDef** в рабочей области Microsoft Access можно использовать свойство **Connect** со свойством ReturnsRecords для создания сквозного запроса ODBC SQL ODBC.</span><span class="sxs-lookup"><span data-stu-id="bf860-182">On a **QueryDef** object in a Microsoft Access workspace, you can use the **Connect** property with the ReturnsRecords property to create an ODBC SQL pass-through query.</span></span> <span data-ttu-id="bf860-183">Тип базы данных строки подключения — "ODBC;", а остальная часть строки содержит сведения, специфичные для драйвера ODBC, используемого для доступа к удаленным данным.</span><span class="sxs-lookup"><span data-stu-id="bf860-183">The databasetype of the connection string is "ODBC;", and the remainder of the string contains information specific to the ODBC driver used to access the remote data.</span></span> <span data-ttu-id="bf860-184">Дополнительные сведения см. в документации по конкретному драйверу.</span><span class="sxs-lookup"><span data-stu-id="bf860-184">For more information, see the documentation for the specific driver.</span></span>

> [!NOTE]
> - <span data-ttu-id="bf860-185">Необходимо задать значение свойства **Connect** перед настройкой свойства **ReturnsRecords**.</span><span class="sxs-lookup"><span data-stu-id="bf860-185">You must set the **Connect** property before you set the **ReturnsRecords** property.</span></span>
> - <span data-ttu-id="bf860-186">Необходимо иметь разрешения на доступ к компьютеру, который содержит сервер базы данных, доступ к которому вы пытаетесь получить доступ.</span><span class="sxs-lookup"><span data-stu-id="bf860-186">You must have access permissions to the computer that contains the database server you're trying to access.</span></span>


