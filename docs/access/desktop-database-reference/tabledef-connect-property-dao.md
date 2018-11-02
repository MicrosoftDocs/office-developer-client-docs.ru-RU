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
ms.openlocfilehash: 322b59c6556b73186fe4034e64c75d9104d29560
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926901"
---
# <a name="tabledefconnect-property-dao"></a><span data-ttu-id="8ec2f-102">Свойство TableDef.Connect (DAO)</span><span class="sxs-lookup"><span data-stu-id="8ec2f-102">TableDef.Connect property (DAO)</span></span>


<span data-ttu-id="8ec2f-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8ec2f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8ec2f-104">Задает или возвращает значение, которое предоставляет сведения о связанной таблицы.</span><span class="sxs-lookup"><span data-stu-id="8ec2f-104">Sets or returns a value that provides information about a linked table.</span></span> <span data-ttu-id="8ec2f-105">Для чтения и записи, **String**.</span><span class="sxs-lookup"><span data-stu-id="8ec2f-105">Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ec2f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8ec2f-106">Syntax</span></span>

<span data-ttu-id="8ec2f-107">*выражение* . Подключение</span><span class="sxs-lookup"><span data-stu-id="8ec2f-107">*expression* .Connect</span></span>

<span data-ttu-id="8ec2f-108">*выражение* Переменная, которая представляет собой объект- **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="8ec2f-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ec2f-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="8ec2f-109">Remarks</span></span>

<span data-ttu-id="8ec2f-110">Настройка свойства **подключение** — **строка** состоит из спецификатора типа базы данных и ноль или больше параметров, разделенных точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="8ec2f-110">The **Connect** property setting is a **String** composed of a database type specifier and zero or more parameters separated by semicolons.</span></span> <span data-ttu-id="8ec2f-111">Свойство **Connect** передает Дополнительные сведения о ODBC и драйверы некоторых ISAM при необходимости.</span><span class="sxs-lookup"><span data-stu-id="8ec2f-111">The **Connect** property passes additional information to ODBC and certain ISAM drivers as needed.</span></span>

<span data-ttu-id="8ec2f-112">Для объекта **TableDef** , представляющий связанной таблицы значение свойства **подключение** состоит из одного или двух частях (описатель типа базы данных и путь к базе данных), каждая из которых заканчиваются точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="8ec2f-112">For a **TableDef** object that represents a linked table, the **Connect** property setting consists of one or two parts (a database type specifier and a path to the database), each of which ends with a semicolon.</span></span>

<span data-ttu-id="8ec2f-113">Путь, как показано в следующей таблице — это полный путь к каталогу, содержащему файлы базы данных и должен предшествовать идентификатор базы данных =.</span><span class="sxs-lookup"><span data-stu-id="8ec2f-113">The path as shown in the following table is the full path for the directory containing the database files and must be preceded by the identifier DATABASE=.</span></span> <span data-ttu-id="8ec2f-114">В некоторых случаях (как с помощью Microsoft Excel и Microsoft Access базы данных базами данных, ядро) должен включать имя файла в качестве аргумента базы данных.</span><span class="sxs-lookup"><span data-stu-id="8ec2f-114">In some cases (as with Microsoft Excel and Microsoft Access database engine databases), you should include a specific file name in the database path argument.</span></span>

<span data-ttu-id="8ec2f-115">Ниже приведены возможные типы и баз данных и их соответствующие спецификаторы базы данных пути для настройки свойства **подключения** .</span><span class="sxs-lookup"><span data-stu-id="8ec2f-115">The following table shows possible database types and their corresponding database specifiers and paths for the **Connect** property setting.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8ec2f-116">Тип базы данных</span><span class="sxs-lookup"><span data-stu-id="8ec2f-116">Database type</span></span></p></th>
<th><p><span data-ttu-id="8ec2f-117">Описателя</span><span class="sxs-lookup"><span data-stu-id="8ec2f-117">Specifier</span></span></p></th>
<th><p><span data-ttu-id="8ec2f-118">Пример</span><span class="sxs-lookup"><span data-stu-id="8ec2f-118">Example</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8ec2f-119">Базы данных Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="8ec2f-119">Microsoft Access Database</span></span></p></td>
<td><p><span data-ttu-id="8ec2f-120">База данных [];</span><span class="sxs-lookup"><span data-stu-id="8ec2f-120">[database];</span></span></p></td>
<td><p><span data-ttu-id="8ec2f-121">диск: \path\filename</span><span class="sxs-lookup"><span data-stu-id="8ec2f-121">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ec2f-122">dBASE III</span><span class="sxs-lookup"><span data-stu-id="8ec2f-122">dBASE III</span></span></p></td>
<td><p><span data-ttu-id="8ec2f-123">dBASE III;</span><span class="sxs-lookup"><span data-stu-id="8ec2f-123">dBASE III;</span></span></p></td>
<td><p><span data-ttu-id="8ec2f-124">диск: \path</span><span class="sxs-lookup"><span data-stu-id="8ec2f-124">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ec2f-125">dBASE IV</span><span class="sxs-lookup"><span data-stu-id="8ec2f-125">dBASE IV</span></span></p></td>
<td><p><span data-ttu-id="8ec2f-126">dBASE IV;</span><span class="sxs-lookup"><span data-stu-id="8ec2f-126">dBASE IV;</span></span></p></td>
<td><p><span data-ttu-id="8ec2f-127">диск: \path</span><span class="sxs-lookup"><span data-stu-id="8ec2f-127">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ec2f-128">dBASE 5</span><span class="sxs-lookup"><span data-stu-id="8ec2f-128">dBASE 5</span></span></p></td>
<td><p><span data-ttu-id="8ec2f-129">dBASE 5.0;</span><span class="sxs-lookup"><span data-stu-id="8ec2f-129">dBASE 5.0;</span></span></p></td>
<td><p><span data-ttu-id="8ec2f-130">диск: \path</span><span class="sxs-lookup"><span data-stu-id="8ec2f-130">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ec2f-131">Paradox 3.x</span><span class="sxs-lookup"><span data-stu-id="8ec2f-131">Paradox 3.x</span></span></p></td>
<td><p><span data-ttu-id="8ec2f-132">Paradox 3.x;</span><span class="sxs-lookup"><span data-stu-id="8ec2f-132">Paradox 3.x;</span></span></p></td>
<td><p><span data-ttu-id="8ec2f-133">диск: \path</span><span class="sxs-lookup"><span data-stu-id="8ec2f-133">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ec2f-134">Paradox 4.x</span><span class="sxs-lookup"><span data-stu-id="8ec2f-134">Paradox 4.x</span></span></p></td>
<td><p><span data-ttu-id="8ec2f-135">Paradox 4.x;</span><span class="sxs-lookup"><span data-stu-id="8ec2f-135">Paradox 4.x;</span></span></p></td>
<td><p><span data-ttu-id="8ec2f-136">диск: \path</span><span class="sxs-lookup"><span data-stu-id="8ec2f-136">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ec2f-137">Paradox 5.x</span><span class="sxs-lookup"><span data-stu-id="8ec2f-137">Paradox 5.x</span></span></p></td>
<td><p><span data-ttu-id="8ec2f-138">Paradox 5.x;</span><span class="sxs-lookup"><span data-stu-id="8ec2f-138">Paradox 5.x;</span></span></p></td>
<td><p><span data-ttu-id="8ec2f-139">диск: \path</span><span class="sxs-lookup"><span data-stu-id="8ec2f-139">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ec2f-140">Microsoft Excel 3.0</span><span class="sxs-lookup"><span data-stu-id="8ec2f-140">Microsoft Excel 3.0</span></span></p></td>
<td><p><span data-ttu-id="8ec2f-141">Excel 3.0;</span><span class="sxs-lookup"><span data-stu-id="8ec2f-141">Excel 3.0;</span></span></p></td>
<td><p><span data-ttu-id="8ec2f-142">Drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="8ec2f-142">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ec2f-143">Microsoft Excel 4.0</span><span class="sxs-lookup"><span data-stu-id="8ec2f-143">Microsoft Excel 4.0</span></span></p></td>
<td><p><span data-ttu-id="8ec2f-144">Excel 4.0;</span><span class="sxs-lookup"><span data-stu-id="8ec2f-144">Excel 4.0;</span></span></p></td>
<td><p><span data-ttu-id="8ec2f-145">Drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="8ec2f-145">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ec2f-146">Microsoft Excel 5.0 или Microsoft Excel 95</span><span class="sxs-lookup"><span data-stu-id="8ec2f-146">Microsoft Excel 5.0 or Microsoft Excel 95</span></span></p></td>
<td><p><span data-ttu-id="8ec2f-147">Excel 5.0;</span><span class="sxs-lookup"><span data-stu-id="8ec2f-147">Excel 5.0;</span></span></p></td>
<td><p><span data-ttu-id="8ec2f-148">Drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="8ec2f-148">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ec2f-149">Microsoft Excel 97</span><span class="sxs-lookup"><span data-stu-id="8ec2f-149">Microsoft Excel 97</span></span></p></td>
<td><p><span data-ttu-id="8ec2f-150">Excel 8.0;</span><span class="sxs-lookup"><span data-stu-id="8ec2f-150">Excel 8.0;</span></span></p></td>
<td><p><span data-ttu-id="8ec2f-151">Drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="8ec2f-151">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ec2f-152">Lotus 1-2-3 WKS и WK1</span><span class="sxs-lookup"><span data-stu-id="8ec2f-152">Lotus 1-2-3 WKS and WK1</span></span></p></td>
<td><p><span data-ttu-id="8ec2f-153">Lotus WK1;</span><span class="sxs-lookup"><span data-stu-id="8ec2f-153">Lotus WK1;</span></span></p></td>
<td><p><span data-ttu-id="8ec2f-154">Drive:\path\filename.WK1</span><span class="sxs-lookup"><span data-stu-id="8ec2f-154">drive:\path\filename.wk1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ec2f-155">WK3 Lotus 1-2-3</span><span class="sxs-lookup"><span data-stu-id="8ec2f-155">Lotus 1-2-3 WK3</span></span></p></td>
<td><p><span data-ttu-id="8ec2f-156">Lotus WK3;</span><span class="sxs-lookup"><span data-stu-id="8ec2f-156">Lotus WK3;</span></span></p></td>
<td><p><span data-ttu-id="8ec2f-157">Drive:\path\filename.WK3</span><span class="sxs-lookup"><span data-stu-id="8ec2f-157">drive:\path\filename.wk3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ec2f-158">WK4 Lotus 1-2-3</span><span class="sxs-lookup"><span data-stu-id="8ec2f-158">Lotus 1-2-3 WK4</span></span></p></td>
<td><p><span data-ttu-id="8ec2f-159">Lotus WK4;</span><span class="sxs-lookup"><span data-stu-id="8ec2f-159">Lotus WK4;</span></span></p></td>
<td><p><span data-ttu-id="8ec2f-160">Drive:\path\filename.WK4</span><span class="sxs-lookup"><span data-stu-id="8ec2f-160">drive:\path\filename.wk4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ec2f-161">Импорт HTML</span><span class="sxs-lookup"><span data-stu-id="8ec2f-161">HTML Import</span></span></p></td>
<td><p><span data-ttu-id="8ec2f-162">Импорт HTML;</span><span class="sxs-lookup"><span data-stu-id="8ec2f-162">HTML Import;</span></span></p></td>
<td><p><span data-ttu-id="8ec2f-163">диск: \path\filename</span><span class="sxs-lookup"><span data-stu-id="8ec2f-163">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ec2f-164">Экспорт HTML</span><span class="sxs-lookup"><span data-stu-id="8ec2f-164">HTML Export</span></span></p></td>
<td><p><span data-ttu-id="8ec2f-165">Экспорт HTML;</span><span class="sxs-lookup"><span data-stu-id="8ec2f-165">HTML Export;</span></span></p></td>
<td><p><span data-ttu-id="8ec2f-166">диск: \path</span><span class="sxs-lookup"><span data-stu-id="8ec2f-166">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ec2f-167">Текст</span><span class="sxs-lookup"><span data-stu-id="8ec2f-167">Text</span></span></p></td>
<td><p><span data-ttu-id="8ec2f-168">Текст;</span><span class="sxs-lookup"><span data-stu-id="8ec2f-168">Text;</span></span></p></td>
<td><p><span data-ttu-id="8ec2f-169">диск: \path</span><span class="sxs-lookup"><span data-stu-id="8ec2f-169">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ec2f-170">Open Database Connectivity</span><span class="sxs-lookup"><span data-stu-id="8ec2f-170">ODBC</span></span></p></td>
<td><p><span data-ttu-id="8ec2f-171">ODBC. Базы данных = база данных; UID = пользователя; PWD = пароля; Уведомления о Доставке = источнику данных; [LOGINTIMEOUT = секунды;]</span><span class="sxs-lookup"><span data-stu-id="8ec2f-171">ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</span></span></p></td>
<td><p><span data-ttu-id="8ec2f-172">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="8ec2f-172">None</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ec2f-173">Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="8ec2f-173">Microsoft Exchange</span></span></p></td>
<td><p><span data-ttu-id="8ec2f-174">Exchange 4.0; MAPILEVEL = folderpath; [TABLETYPE = {0 | 1}]; [ПРОФИЛЕЙ = профиля;] [PWD = пароль;] [Базы данных = база данных;]</span><span class="sxs-lookup"><span data-stu-id="8ec2f-174">Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</span></span></p></td>
<td><p><span data-ttu-id="8ec2f-175">диск: \path\filename</span><span class="sxs-lookup"><span data-stu-id="8ec2f-175">drive:\path\filename</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8ec2f-176">Если пароль требуется, но не указан в параметре свойства **подключения** , диалоговое окно входа в систему отображается впервые таблицам драйвер ODBC и снова закрыто и повторно открыть подключение.</span><span class="sxs-lookup"><span data-stu-id="8ec2f-176">If a password is required but not provided in the **Connect** property setting, a login dialog box is displayed the first time a table is accessed by the ODBC driver and again if the connection is closed and reopened.</span></span>

<span data-ttu-id="8ec2f-177">Для данных в Microsoft Exchange требуется ключ MAPILEVEL должно быть присвоено полностью разрешить пути (например, «почтовый ящик – Pat SmithIAlpha/текущую»).</span><span class="sxs-lookup"><span data-stu-id="8ec2f-177">For data in Microsoft Exchange, the required MAPILEVEL key should be set to a fully-resolved folder path (for example, "Mailbox - Pat SmithIAlpha/Today").</span></span> <span data-ttu-id="8ec2f-178">Путь не включает имя папки, которая будет открыта в виде таблицы; Вместо этого следует указать имя этой папки в качестве аргумента имя метода **CreateTable** .</span><span class="sxs-lookup"><span data-stu-id="8ec2f-178">The path does not include the name of the folder that will be opened as a table; that folder’s name should instead be specified as the name argument to the **CreateTable** method.</span></span> <span data-ttu-id="8ec2f-179">Клавиша TABLETYPE должно быть присвоено значение «0» откройте папку (по умолчанию) или «1», чтобы открыть адресную книгу.</span><span class="sxs-lookup"><span data-stu-id="8ec2f-179">The TABLETYPE key should be set to "0" to open a folder (default) or "1" to open an address book.</span></span> <span data-ttu-id="8ec2f-180">В настоящее время с помощью ключа ПРОФИЛЯ по умолчанию к профилю.</span><span class="sxs-lookup"><span data-stu-id="8ec2f-180">The PROFILE key defaults to the profile currently in use.</span></span>

<span data-ttu-id="8ec2f-181">Для базовых таблиц в базе данных Micorosoft Access значение свойства **подключение** является строкой нулевой длины (»»).</span><span class="sxs-lookup"><span data-stu-id="8ec2f-181">For base tables in a Micorosoft Access database, the **Connect** property setting is a zero-length string ("").</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="8ec2f-182">Необходимо установить свойство <STRONG>подключение</STRONG> , прежде чем задать свойство <STRONG>ReturnsRecords</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="8ec2f-182">You must set the <STRONG>Connect</STRONG> property before you set the <STRONG>ReturnsRecords</STRONG> property.</span></span></P>
> <LI>
> <P><span data-ttu-id="8ec2f-183">Необходимо иметь разрешения доступа на компьютере, где размещается сервер базы данных, который вы пытаетесь получить доступ к.</span><span class="sxs-lookup"><span data-stu-id="8ec2f-183">You must have access permissions to the computer that contains the database server you're trying to access.</span></span></P></LI></UL>


