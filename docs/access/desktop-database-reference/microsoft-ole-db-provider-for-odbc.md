---
title: Поставщик Microsoft OLE DB для ODBC
TOCTitle: Microsoft OLE DB Provider for ODBC
ms:assetid: c507567e-5ad1-b32a-f6ad-5ba2c39aa4c2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249964(v=office.15)
ms:contentKeyID: 48547602
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4f5ffae4880cadb90f47f1ac348ffc8b3ea58785
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704562"
---
# <a name="microsoft-ole-db-provider-for-odbc"></a><span data-ttu-id="cf46b-102">Поставщик Microsoft OLE DB для ODBC</span><span class="sxs-lookup"><span data-stu-id="cf46b-102">Microsoft OLE DB Provider for ODBC</span></span>

<span data-ttu-id="cf46b-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cf46b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cf46b-104">Чтобы программист ADO или служб удаленных рабочих СТОЛОВ идеальном мире бы одно в каждом данных источника предоставляет интерфейс OLE DB, чтобы вызвать непосредственно в источник данных ADO.</span><span class="sxs-lookup"><span data-stu-id="cf46b-104">To an ADO or RDS programmer, an ideal world would be one in which every data source exposes an OLE DB interface, so that ADO could call directly into the data source.</span></span> <span data-ttu-id="cf46b-105">Несмотря на то, что все больше дополнительные базы данных поставщиков реализует интерфейсы OLE DB, некоторые источники данных не еще не представленных таким способом.</span><span class="sxs-lookup"><span data-stu-id="cf46b-105">Although increasingly more database vendors are implementing OLE DB interfaces, some data sources are not yet exposed this way.</span></span> <span data-ttu-id="cf46b-106">Тем не менее практически все СУБД в настоящее время может осуществляться через ODBC.</span><span class="sxs-lookup"><span data-stu-id="cf46b-106">However, virtually all DBMS systems in use today can be accessed through ODBC.</span></span>

<span data-ttu-id="cf46b-107">Драйверы ODBC доступны для всех основных СУБД, в настоящее время, включая Microsoft SQL Server, Microsoft Access (базы данных Microsoft Jet) и Microsoft FoxPro, кроме базы данных сторонних продуктов, таких как Oracle.</span><span class="sxs-lookup"><span data-stu-id="cf46b-107">ODBC drivers are available for every major DBMS in use today, including Microsoft SQL Server, Microsoft Access (Microsoft Jet database engine), and Microsoft FoxPro, in addition to non-Microsoft database products such as Oracle.</span></span>

<span data-ttu-id="cf46b-108">Поставщик ODBC Microsoft, однако позволяет ADO для подключения к источникам данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="cf46b-108">The Microsoft ODBC Provider, however, allows ADO to connect to any ODBC data source.</span></span> <span data-ttu-id="cf46b-109">Поставщик свободных потоков и Юникод.</span><span class="sxs-lookup"><span data-stu-id="cf46b-109">The provider is free-threaded and Unicode enabled.</span></span>

<span data-ttu-id="cf46b-110">Поставщик поддерживает транзакции, несмотря на то, что разные ядра СУБД предлагают различные виды поддержки транзакций.</span><span class="sxs-lookup"><span data-stu-id="cf46b-110">The provider supports transactions, although different DBMS engines offer different types of transaction support.</span></span> <span data-ttu-id="cf46b-111">Например Microsoft Access поддерживает до пяти уровней вложенных транзакций.</span><span class="sxs-lookup"><span data-stu-id="cf46b-111">For example, Microsoft Access supports nested transactions up to five levels deep.</span></span>

<span data-ttu-id="cf46b-112">Поставщик по умолчанию для ADO и поддерживаются все зависящие от поставщика ADO свойства и методы.</span><span class="sxs-lookup"><span data-stu-id="cf46b-112">This is the default provider for ADO, and all provider-dependent ADO properties and methods are supported.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="cf46b-113">Параметры строки подключения</span><span class="sxs-lookup"><span data-stu-id="cf46b-113">Connection String Parameters</span></span>

<span data-ttu-id="cf46b-114">Для подключения к данным поставщиком, задайте **поставщика =** аргумент свойства [ConnectionString](connectionstring-property-ado.md) для:</span><span class="sxs-lookup"><span data-stu-id="cf46b-114">To connect to this provider, set the **Provider=** argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```sql 
 
MSDASQL 
```

<span data-ttu-id="cf46b-115">Чтение свойства [поставщика](provider-property-ado.md) будет возвращать также этой строки.</span><span class="sxs-lookup"><span data-stu-id="cf46b-115">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="cf46b-116">Типичная строка подключения</span><span class="sxs-lookup"><span data-stu-id="cf46b-116">Typical Connection String</span></span>

<span data-ttu-id="cf46b-117">— Это строка соединения для данного поставщика:</span><span class="sxs-lookup"><span data-stu-id="cf46b-117">A typical connection string for this provider is:</span></span>

```sql 
 
"Provider=MSDASQL;DSN=dsnName;UID=userName;PWD=userPassword;" 
```

<span data-ttu-id="cf46b-118">Строка состоит из следующих ключевых слов:</span><span class="sxs-lookup"><span data-stu-id="cf46b-118">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cf46b-119">Keyword</span><span class="sxs-lookup"><span data-stu-id="cf46b-119">Keyword</span></span></p></th>
<th><p><span data-ttu-id="cf46b-120">Описание</span><span class="sxs-lookup"><span data-stu-id="cf46b-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-121"><strong>Поставщик</strong></span><span class="sxs-lookup"><span data-stu-id="cf46b-121"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="cf46b-122">Задает поставщика OLE DB для ODBC.</span><span class="sxs-lookup"><span data-stu-id="cf46b-122">Specifies the OLE DB Provider for ODBC.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-123"><strong>УВЕДОМЛЕНИЯ О ДОСТАВКЕ</strong></span><span class="sxs-lookup"><span data-stu-id="cf46b-123"><strong>DSN</strong></span></span></p></td>
<td><p><span data-ttu-id="cf46b-124">Указывает имя источника данных.</span><span class="sxs-lookup"><span data-stu-id="cf46b-124">Specifies the data source name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-125"><strong>UID</strong></span><span class="sxs-lookup"><span data-stu-id="cf46b-125"><strong>UID</strong></span></span></p></td>
<td><p><span data-ttu-id="cf46b-126">Задает имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="cf46b-126">Specifies the user name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-127"><strong>PWD</strong></span><span class="sxs-lookup"><span data-stu-id="cf46b-127"><strong>PWD</strong></span></span></p></td>
<td><p><span data-ttu-id="cf46b-128">Задает пароль пользователя.</span><span class="sxs-lookup"><span data-stu-id="cf46b-128">Specifies the user password.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-129"><strong>URL</strong>.</span><span class="sxs-lookup"><span data-stu-id="cf46b-129"><strong>URL</strong></span></span></p></td>
<td><p><span data-ttu-id="cf46b-130">Задает URL-адрес файла или папки, опубликованной в веб-папку.</span><span class="sxs-lookup"><span data-stu-id="cf46b-130">Specifies the URL of a file or directory published in a web folder.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cf46b-131">Так как это поставщика по умолчанию для ADO, если опустить **поставщика =** параметра в строке подключения ADO пытается установить подключение к данным поставщиком.</span><span class="sxs-lookup"><span data-stu-id="cf46b-131">Because this is the default provider for ADO, if you omit the **Provider=** parameter from the connection string, ADO will attempt to establish a connection to this provider.</span></span>

<span data-ttu-id="cf46b-132">Поставщик не поддерживает параметры подключения в дополнение к определяемые ADO.</span><span class="sxs-lookup"><span data-stu-id="cf46b-132">The provider does not support any specific connection parameters in addition to those defined by ADO.</span></span> <span data-ttu-id="cf46b-133">Тем не менее Поставщик передает параметры соединения не ADO драйвера ODBC.</span><span class="sxs-lookup"><span data-stu-id="cf46b-133">However, the provider will pass any non-ADO connection parameters to the ODBC driver manager.</span></span>

<span data-ttu-id="cf46b-134">Так как можно опустить параметр **поставщика** , таким образом можно создать строку подключения ADO, идентичный строки подключения ODBC для одного источника данных.</span><span class="sxs-lookup"><span data-stu-id="cf46b-134">Because you can omit the **Provider** parameter, you can therefore compose an ADO connection string that is identical to an ODBC connection string for the same data source.</span></span> <span data-ttu-id="cf46b-135">Используйте одинаковые имена параметров (**ДРАЙВЕРА =**, **базы данных =**, **уведомления о Доставке =** и так далее), значения и синтаксис, как вы бы при создании строки подключения ODBC.</span><span class="sxs-lookup"><span data-stu-id="cf46b-135">Use the same parameter names (**DRIVER=**, **DATABASE=**, **DSN=**, and so on), values, and syntax as you would when composing an ODBC connection string.</span></span> <span data-ttu-id="cf46b-136">Можно подключить с и без имя источника данных (DSN) или FileDSN.</span><span class="sxs-lookup"><span data-stu-id="cf46b-136">You can connect with or without a predefined data source name (DSN) or FileDSN.</span></span>

<span data-ttu-id="cf46b-137">**Синтаксис с уведомления о Доставке или FileDSN:**</span><span class="sxs-lookup"><span data-stu-id="cf46b-137">**Syntax with a DSN or FileDSN:**</span></span>

`"[Provider=MSDASQL;] { DSN=name | FileDSN=filename } ; [DATABASE=database;] UID=user; PWD=password"`

<span data-ttu-id="cf46b-138">**Синтаксис без уведомления о Доставке (соединения):**</span><span class="sxs-lookup"><span data-stu-id="cf46b-138">**Syntax without a DSN (DSN-less connection):**</span></span>

`"[Provider=MSDASQL;] DRIVER=driver; SERVER=server;DATABASE=database; UID=user; PWD=password"`

<span data-ttu-id="cf46b-139">Если вы используете **уведомления о Доставке** или **FileDSN**, его необходимо определить через источники данных ODBC в панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="cf46b-139">If you use a **DSN** or **FileDSN**, it must be defined through the ODBC Data Source Administrator in the Windows Control Panel.</span></span> <span data-ttu-id="cf46b-140">В Microsoft Windows 2000 администратор ODBC находится в разделе Администрирование.</span><span class="sxs-lookup"><span data-stu-id="cf46b-140">In Microsoft Windows 2000, the ODBC Administrator is located under Administrative Tools.</span></span> <span data-ttu-id="cf46b-141">В предыдущих версиях Windows значок администратор ODBC называется **32-разрядная версия ODBC** или просто **ODBC**.</span><span class="sxs-lookup"><span data-stu-id="cf46b-141">In previous versions of Windows, the ODBC Administrator icon is named **32-bit ODBC** or simply **ODBC**.</span></span>

<span data-ttu-id="cf46b-142">В качестве альтернативы для установки **уведомления о Доставке**, можно указать драйвер ODBC (**ДРАЙВЕРА =**), например «SQL Server»; имя сервера (**SERVER =**); и имя базы данных (**базы данных =**).</span><span class="sxs-lookup"><span data-stu-id="cf46b-142">As an alternative to setting a **DSN**, you can specify the ODBC driver (**DRIVER=**), such as "SQL Server;" the server name (**SERVER=**); and the database name (**DATABASE=**).</span></span>

<span data-ttu-id="cf46b-143">Также можно указать имя учетной записи пользователя (**UID =**) и пароль для учетной записи пользователя (**PWD =**) в параметры, относящиеся к ODBC или в стандартный определенные ADO *пользователя* и *пароль* параметры.</span><span class="sxs-lookup"><span data-stu-id="cf46b-143">You can also specify a user account name (**UID=**), and the password for the user account (**PWD=**) in the ODBC-specific parameters or in the standard ADO-defined *user* and *password* parameters.</span></span>

<span data-ttu-id="cf46b-144">Хотя **уведомления о Доставке** определение уже указывает базу данных, можно задать *параметр *базы данных* , в дополнение к **уведомления о Доставке** для подключения в другую базу данных* .</span><span class="sxs-lookup"><span data-stu-id="cf46b-144">Although a **DSN** definition already specifies a database, you can specify *a* *database* parameter in addition to a **DSN** to connect to a different database.</span></span> <span data-ttu-id="cf46b-145">Рекомендуется всегда включать \*параметр *базы данных* \* при использовании **уведомления о Доставке**.</span><span class="sxs-lookup"><span data-stu-id="cf46b-145">It is a good idea to always include *the* *database* parameter when you use a **DSN**.</span></span> <span data-ttu-id="cf46b-146">Это обеспечит подключиться к базе соответствующих прав в случае, когда другой пользователь изменить параметр базы данных по умолчанию с момента последнего извлечения определения **уведомления о Доставке** .</span><span class="sxs-lookup"><span data-stu-id="cf46b-146">This will ensure that you connect to the proper database in the event that another user changed the default database parameter since you last checked the **DSN** definition.</span></span>

## <a name="provider-specific-connection-properties"></a><span data-ttu-id="cf46b-147">Свойства подключения от поставщика</span><span class="sxs-lookup"><span data-stu-id="cf46b-147">Provider-Specific Connection Properties</span></span>

<span data-ttu-id="cf46b-148">Поставщик OLE DB для ODBC добавляет несколько свойств в коллекцию [свойств](properties-collection-ado.md) объекта **подключения** .</span><span class="sxs-lookup"><span data-stu-id="cf46b-148">The OLE DB provider for ODBC adds several properties to the [Properties](properties-collection-ado.md) collection of the **Connection** object.</span></span> <span data-ttu-id="cf46b-149">В следующей таблице перечислены эти свойства имя соответствующего свойства OLE DB в скобки.</span><span class="sxs-lookup"><span data-stu-id="cf46b-149">The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cf46b-150">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="cf46b-150">Property Name</span></span></p></th>
<th><p><span data-ttu-id="cf46b-151">Описание</span><span class="sxs-lookup"><span data-stu-id="cf46b-151">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-152">Доступны процедуры</span><span class="sxs-lookup"><span data-stu-id="cf46b-152">Accessible Procedures</span></span><br />
<span data-ttu-id="cf46b-153">(KAGPROP_ACCESSIBLEPROCEDURES)</span><span class="sxs-lookup"><span data-stu-id="cf46b-153">(KAGPROP_ACCESSIBLEPROCEDURES)</span></span></p></td>
<td><p><span data-ttu-id="cf46b-154">Указывает, является ли пользователь имеет доступ к хранимые процедуры.</span><span class="sxs-lookup"><span data-stu-id="cf46b-154">Indicates whether the user has access to stored procedures.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-155">Доступно таблиц</span><span class="sxs-lookup"><span data-stu-id="cf46b-155">Accessible Tables</span></span><br />
<span data-ttu-id="cf46b-156">(KAGPROP_ACCESSIBLETABLES)</span><span class="sxs-lookup"><span data-stu-id="cf46b-156">(KAGPROP_ACCESSIBLETABLES)</span></span></p></td>
<td><p><span data-ttu-id="cf46b-157">Указывает, является ли пользователь имеет разрешения на выполнение инструкций SELECT таблиц базы данных.</span><span class="sxs-lookup"><span data-stu-id="cf46b-157">Indicates whether the user has permission to execute SELECT statements against the database tables.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-158">Активные операторы</span><span class="sxs-lookup"><span data-stu-id="cf46b-158">Active Statements</span></span><br />
<span data-ttu-id="cf46b-159">(KAGPROP_ACTIVESTATEMENTS)</span><span class="sxs-lookup"><span data-stu-id="cf46b-159">(KAGPROP_ACTIVESTATEMENTS)</span></span></p></td>
<td><p><span data-ttu-id="cf46b-160">Указывает число дескрипторов, которые может поддерживать драйвера ODBC для подключения.</span><span class="sxs-lookup"><span data-stu-id="cf46b-160">Indicates the number of handles an ODBC driver can support on a connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-161">Имя драйвера</span><span class="sxs-lookup"><span data-stu-id="cf46b-161">Driver Name</span></span><br />
<span data-ttu-id="cf46b-162">(KAGPROP_DRIVERNAME)</span><span class="sxs-lookup"><span data-stu-id="cf46b-162">(KAGPROP_DRIVERNAME)</span></span></p></td>
<td><p><span data-ttu-id="cf46b-163">Указывает имя файла драйвера ODBC.</span><span class="sxs-lookup"><span data-stu-id="cf46b-163">Indicates the file name of the ODBC driver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-164">Версия драйвера ODBC</span><span class="sxs-lookup"><span data-stu-id="cf46b-164">Driver ODBC Version</span></span><br />
<span data-ttu-id="cf46b-165">(KAGPROP_DRIVERODBCVER)</span><span class="sxs-lookup"><span data-stu-id="cf46b-165">(KAGPROP_DRIVERODBCVER)</span></span></p></td>
<td><p><span data-ttu-id="cf46b-166">Указывает версию, поддерживающего этот драйвер ODBC.</span><span class="sxs-lookup"><span data-stu-id="cf46b-166">Indicates the version of ODBC that this driver supports.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-167">Использование файлов</span><span class="sxs-lookup"><span data-stu-id="cf46b-167">File Usage</span></span><br />
<span data-ttu-id="cf46b-168">(KAGPROP_FILEUSAGE)</span><span class="sxs-lookup"><span data-stu-id="cf46b-168">(KAGPROP_FILEUSAGE)</span></span></p></td>
<td><p><span data-ttu-id="cf46b-169">Указывает, как драйвер обрабатывает файл источника данных. как таблицы или как к каталогу.</span><span class="sxs-lookup"><span data-stu-id="cf46b-169">Indicates how the driver treats a file in a data source; as a table or as a catalog.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-170">Как предложение escape-последовательности</span><span class="sxs-lookup"><span data-stu-id="cf46b-170">Like Escape Clause</span></span><br />
<span data-ttu-id="cf46b-171">(KAGPROP_LIKEESCAPECLAUSE)</span><span class="sxs-lookup"><span data-stu-id="cf46b-171">(KAGPROP_LIKEESCAPECLAUSE)</span></span></p></td>
<td><p><span data-ttu-id="cf46b-172">Указывает предикат LIKE предложение WHERE ли драйвер поддерживается в определение и использование escape-символ знаком процента (%) и символ подчеркивания (_).</span><span class="sxs-lookup"><span data-stu-id="cf46b-172">Indicates whether the driver supports the definition and use of an escape character for the percent character (%) and underline character (_) in the LIKE predicate of a WHERE clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-173">Максимальное число столбцов в группировать по</span><span class="sxs-lookup"><span data-stu-id="cf46b-173">Max Columns in Group By</span></span><br />
<span data-ttu-id="cf46b-174">(KAGPROP_MAXCOLUMNSINGROUPBY)</span><span class="sxs-lookup"><span data-stu-id="cf46b-174">(KAGPROP_MAXCOLUMNSINGROUPBY)</span></span></p></td>
<td><p><span data-ttu-id="cf46b-175">Указывает максимальное число столбцов, которые могут быть перечислены в предложении GROUP BY инструкции SELECT.</span><span class="sxs-lookup"><span data-stu-id="cf46b-175">Indicates the maximum number of columns that can be listed in the GROUP BY clause of a SELECT statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-176">Максимальное число столбцов в индексе</span><span class="sxs-lookup"><span data-stu-id="cf46b-176">Max Columns in Index</span></span><br />
<span data-ttu-id="cf46b-177">(KAGPROP_MAXCOLUMNSININDEX)</span><span class="sxs-lookup"><span data-stu-id="cf46b-177">(KAGPROP_MAXCOLUMNSININDEX)</span></span></p></td>
<td><p><span data-ttu-id="cf46b-178">Указывает максимальное число столбцов, которые можно включить в индекс.</span><span class="sxs-lookup"><span data-stu-id="cf46b-178">Indicates the maximum number of columns that can be included in an index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-179">Максимальное число столбцов в порядке</span><span class="sxs-lookup"><span data-stu-id="cf46b-179">Max Columns in Order By</span></span><br />
<span data-ttu-id="cf46b-180">(KAGPROP_MAXCOLUMNSINORDERBY)</span><span class="sxs-lookup"><span data-stu-id="cf46b-180">(KAGPROP_MAXCOLUMNSINORDERBY)</span></span></p></td>
<td><p><span data-ttu-id="cf46b-181">Указывает максимальное число столбцов, которые могут быть перечислены в предложение ORDER BY инструкции SELECT.</span><span class="sxs-lookup"><span data-stu-id="cf46b-181">Indicates the maximum number of columns that can be listed in the ORDER BY clause of a SELECT statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-182">Максимальное число столбцов в Выбор</span><span class="sxs-lookup"><span data-stu-id="cf46b-182">Max Columns in Select</span></span><br />
<span data-ttu-id="cf46b-183">(KAGPROP_MAXCOLUMNSINSELECT)</span><span class="sxs-lookup"><span data-stu-id="cf46b-183">(KAGPROP_MAXCOLUMNSINSELECT)</span></span></p></td>
<td><p><span data-ttu-id="cf46b-184">Указывает максимальное число столбцов, которые могут быть перечислены в разделе SELECT инструкции SELECT.</span><span class="sxs-lookup"><span data-stu-id="cf46b-184">Indicates the maximum number of columns that can be listed in the SELECT portion of a SELECT statement.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-185">Максимальное число столбцов в таблице</span><span class="sxs-lookup"><span data-stu-id="cf46b-185">Max Columns in Table</span></span><br />
<span data-ttu-id="cf46b-186">(KAGPROP_MAXCOLUMNSINTABLE)</span><span class="sxs-lookup"><span data-stu-id="cf46b-186">(KAGPROP_MAXCOLUMNSINTABLE)</span></span></p></td>
<td><p><span data-ttu-id="cf46b-187">Указывает максимальное число столбцов в таблице.</span><span class="sxs-lookup"><span data-stu-id="cf46b-187">Indicates the maximum number of columns allowed in a table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-188">Числовые функции</span><span class="sxs-lookup"><span data-stu-id="cf46b-188">Numeric Functions</span></span><br />
<span data-ttu-id="cf46b-189">(KAGPROP_NUMERICFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="cf46b-189">(KAGPROP_NUMERICFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="cf46b-190">Указывает, какие числовые функции поддерживаются драйвер ODBC.</span><span class="sxs-lookup"><span data-stu-id="cf46b-190">Indicates which numeric functions are supported by the ODBC driver.</span></span> <span data-ttu-id="cf46b-191">Список имен функций и связанные значения, используемые в этом Битовая маска, см в приложении д: скалярные в документации по ODBC.</span><span class="sxs-lookup"><span data-stu-id="cf46b-191">For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-192">Возможности внешнего соединения</span><span class="sxs-lookup"><span data-stu-id="cf46b-192">Outer Join Capabilities</span></span><br />
<span data-ttu-id="cf46b-193">(KAGPROP_OJCAPABILITY)</span><span class="sxs-lookup"><span data-stu-id="cf46b-193">(KAGPROP_OJCAPABILITY)</span></span></p></td>
<td><p><span data-ttu-id="cf46b-194">Указывает типы ВНЕШНИЕ соединения, поддерживаемых поставщиком.</span><span class="sxs-lookup"><span data-stu-id="cf46b-194">Indicates the types of OUTER JOINs supported by the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-195">Внешние соединения</span><span class="sxs-lookup"><span data-stu-id="cf46b-195">Outer Joins</span></span><br />
<span data-ttu-id="cf46b-196">(KAGPROP_OUTERJOINS)</span><span class="sxs-lookup"><span data-stu-id="cf46b-196">(KAGPROP_OUTERJOINS)</span></span></p></td>
<td><p><span data-ttu-id="cf46b-197">Указывает, является ли поставщик поддерживает ВНЕШНИЕ соединения.</span><span class="sxs-lookup"><span data-stu-id="cf46b-197">Indicates whether the provider supports OUTER JOINs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-198">Специальные символы</span><span class="sxs-lookup"><span data-stu-id="cf46b-198">Special Characters</span></span><br />
<span data-ttu-id="cf46b-199">(KAGPROP_SPECIALCHARACTERS)</span><span class="sxs-lookup"><span data-stu-id="cf46b-199">(KAGPROP_SPECIALCHARACTERS)</span></span></p></td>
<td><p><span data-ttu-id="cf46b-200">Указывает, какие символы имеет особое значение для драйвера ODBC.</span><span class="sxs-lookup"><span data-stu-id="cf46b-200">Indicates which characters have special meaning for the ODBC driver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-201">Хранимые процедуры</span><span class="sxs-lookup"><span data-stu-id="cf46b-201">Stored Procedures</span></span><br />
<span data-ttu-id="cf46b-202">(KAGPROP_PROCEDURES)</span><span class="sxs-lookup"><span data-stu-id="cf46b-202">(KAGPROP_PROCEDURES)</span></span></p></td>
<td><p><span data-ttu-id="cf46b-203">Указывает, доступны ли хранимые процедуры для использования с этой драйвер ODBC.</span><span class="sxs-lookup"><span data-stu-id="cf46b-203">Indicates whether stored procedures are available for use with this ODBC driver.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-204">Строковые функции</span><span class="sxs-lookup"><span data-stu-id="cf46b-204">String Functions</span></span><br />
<span data-ttu-id="cf46b-205">(KAGPROP_STRINGFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="cf46b-205">(KAGPROP_STRINGFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="cf46b-206">Указывает, какие функции string, поддерживаются драйвер ODBC.</span><span class="sxs-lookup"><span data-stu-id="cf46b-206">Indicates which string functions are supported by the ODBC driver.</span></span> <span data-ttu-id="cf46b-207">Список имен функций и связанные значения, используемые в этом Битовая маска, см в приложении д: скалярные в документации по ODBC.</span><span class="sxs-lookup"><span data-stu-id="cf46b-207">For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-208">Системные функции</span><span class="sxs-lookup"><span data-stu-id="cf46b-208">System Functions</span></span><br />
<span data-ttu-id="cf46b-209">(KAGPROP_SYSTEMFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="cf46b-209">(KAGPROP_SYSTEMFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="cf46b-210">Указывает, какие функции системы поддерживаются драйвер ODBC.</span><span class="sxs-lookup"><span data-stu-id="cf46b-210">Indicates which system functions are supported by the ODBC driver.</span></span> <span data-ttu-id="cf46b-211">Список имен функций и связанные значения, используемые в этом Битовая маска, см в приложении д: скалярные в документации по ODBC.</span><span class="sxs-lookup"><span data-stu-id="cf46b-211">For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-212">Время и Дата функции</span><span class="sxs-lookup"><span data-stu-id="cf46b-212">Time/Date Functions</span></span><br />
<span data-ttu-id="cf46b-213">(KAGPROP_TIMEDATEFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="cf46b-213">(KAGPROP_TIMEDATEFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="cf46b-214">Указывает, какие функции даты и времени поддерживаются драйвер ODBC.</span><span class="sxs-lookup"><span data-stu-id="cf46b-214">Indicates which time and date functions are supported by the ODBC driver.</span></span> <span data-ttu-id="cf46b-215">Список имен функций и связанные значения, используемые в этом Битовая маска, см в приложении д: скалярные в документации по ODBC.</span><span class="sxs-lookup"><span data-stu-id="cf46b-215">For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-216">Поддержка грамматики SQL</span><span class="sxs-lookup"><span data-stu-id="cf46b-216">SQL Grammar Support</span></span><br />
<span data-ttu-id="cf46b-217">(KAGPROP_ODBCSQLCONFORMANCE)</span><span class="sxs-lookup"><span data-stu-id="cf46b-217">(KAGPROP_ODBCSQLCONFORMANCE)</span></span></p></td>
<td><p><span data-ttu-id="cf46b-218">Указывает грамматику SQL, которая поддерживает драйвер ODBC.</span><span class="sxs-lookup"><span data-stu-id="cf46b-218">Indicates the SQL grammar that the ODBC driver supports.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-recordset-and-command-properties"></a><span data-ttu-id="cf46b-219">Свойства команды и записей от поставщика</span><span class="sxs-lookup"><span data-stu-id="cf46b-219">Provider-Specific Recordset and Command Properties</span></span>

<span data-ttu-id="cf46b-220">Поставщик OLE DB для ODBC добавляет несколько свойств **Свойства** набора **записей** и **командных** объектов.</span><span class="sxs-lookup"><span data-stu-id="cf46b-220">The OLE DB provider for ODBC adds several properties to the **Properties** collection of the **Recordset** and **Command** objects.</span></span> <span data-ttu-id="cf46b-221">В следующей таблице перечислены эти свойства имя соответствующего свойства OLE DB в скобки.</span><span class="sxs-lookup"><span data-stu-id="cf46b-221">The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cf46b-222">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="cf46b-222">Property Name</span></span></p></th>
<th><p><span data-ttu-id="cf46b-223">Описание</span><span class="sxs-lookup"><span data-stu-id="cf46b-223">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-224">Запрос на основе обновления, удаления или вставки</span><span class="sxs-lookup"><span data-stu-id="cf46b-224">Query Based Updates/Deletes/Inserts</span></span><br />
<span data-ttu-id="cf46b-225">(KAGPROP_QUERYBASEDUPDATES)</span><span class="sxs-lookup"><span data-stu-id="cf46b-225">(KAGPROP_QUERYBASEDUPDATES)</span></span></p></td>
<td><p><span data-ttu-id="cf46b-226">Указывает, будет ли обновления, удаления и вставки можно выполнить с помощью SQL-запросов.</span><span class="sxs-lookup"><span data-stu-id="cf46b-226">Indicates whether updates, deletions, and insertions can be performed using SQL queries.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-227">Тип параллельного ODBC</span><span class="sxs-lookup"><span data-stu-id="cf46b-227">ODBC Concurrency Type</span></span><br />
<span data-ttu-id="cf46b-228">(KAGPROP_CONCURRENCY)</span><span class="sxs-lookup"><span data-stu-id="cf46b-228">(KAGPROP_CONCURRENCY)</span></span></p></td>
<td><p><span data-ttu-id="cf46b-229">Метод, используемый для уменьшения потенциальных проблем, вызванных двух пользователей одновременно к той же информации из источника данных.</span><span class="sxs-lookup"><span data-stu-id="cf46b-229">Indicates the method used to reduce potential problems caused by two users attempting to access the same data from the data source simultaneously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-230">Специальные возможности больших двоичных ОБЪЕКТОВ на последовательный курсор</span><span class="sxs-lookup"><span data-stu-id="cf46b-230">BLOB accessibility on Forward-Only cursor</span></span><br />
<span data-ttu-id="cf46b-231">(KAGPROP_BLOBSONFOCURSOR)</span><span class="sxs-lookup"><span data-stu-id="cf46b-231">(KAGPROP_BLOBSONFOCURSOR)</span></span></p></td>
<td><p><span data-ttu-id="cf46b-232">Указывает, будет ли при использовании последовательный курсор возможен больших двоичных ОБЪЕКТОВ <strong>полей</strong> .</span><span class="sxs-lookup"><span data-stu-id="cf46b-232">Indicates whether BLOB <strong>Fields</strong> can be accessed when using a forward-only cursor.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-233">Включить в предложения QBU WHERE SQL_FLOAT, SQL_DOUBLE и SQL_REAL</span><span class="sxs-lookup"><span data-stu-id="cf46b-233">Include SQL_FLOAT, SQL_DOUBLE, and SQL_REAL in QBU WHERE clauses</span></span><br />
<span data-ttu-id="cf46b-234">(KAGPROP_INCLUDENONEXACT)</span><span class="sxs-lookup"><span data-stu-id="cf46b-234">(KAGPROP_INCLUDENONEXACT)</span></span></p></td>
<td><p><span data-ttu-id="cf46b-235">Указывает, будет ли значения SQL_FLOAT, SQL_DOUBLE и SQL_REAL может быть включен в предложении QBU WHERE.</span><span class="sxs-lookup"><span data-stu-id="cf46b-235">Indicates whether SQL_FLOAT, SQL_DOUBLE, and SQL_REAL values can be included in a QBU WHERE clause.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-236">Положение в последней строке после вставки</span><span class="sxs-lookup"><span data-stu-id="cf46b-236">Position on the last row after insert</span></span><br />
<span data-ttu-id="cf46b-237">(KAGPROP_POSITIONONNEWROW)</span><span class="sxs-lookup"><span data-stu-id="cf46b-237">(KAGPROP_POSITIONONNEWROW)</span></span></p></td>
<td><p><span data-ttu-id="cf46b-238">Указывает, что после вставки новой записи в таблице последней строки в таблице должны быть поступают текущей строки.</span><span class="sxs-lookup"><span data-stu-id="cf46b-238">Indicates that after a new record has been inserted in a table, the last row in the table will be come the current row.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-239">IRowsetChangeExtInfo</span><span class="sxs-lookup"><span data-stu-id="cf46b-239">IRowsetChangeExtInfo</span></span><br />
<span data-ttu-id="cf46b-240">(KAGPROP_IROWSETCHANGEEXTINFO)</span><span class="sxs-lookup"><span data-stu-id="cf46b-240">(KAGPROP_IROWSETCHANGEEXTINFO)</span></span></p></td>
<td><p><span data-ttu-id="cf46b-241">Указывает, будет ли интерфейс <strong>IRowsetChange</strong> поддерживает расширенные сведения.</span><span class="sxs-lookup"><span data-stu-id="cf46b-241">Indicates whether the <strong>IRowsetChange</strong> interface provides extended information support.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-242">Тип курсора ODBC</span><span class="sxs-lookup"><span data-stu-id="cf46b-242">ODBC Cursor Type</span></span><br />
<span data-ttu-id="cf46b-243">(KAGPROP_CURSOR)</span><span class="sxs-lookup"><span data-stu-id="cf46b-243">(KAGPROP_CURSOR)</span></span></p></td>
<td><p><span data-ttu-id="cf46b-244">Указывает тип курсора, используемого <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="cf46b-244">Indicates the type of cursor used by the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-245">Создать набор строк, который может быть упакован</span><span class="sxs-lookup"><span data-stu-id="cf46b-245">Generate a Rowset that can be marshaled</span></span><br />
<span data-ttu-id="cf46b-246">(KAGPROP_MARSHALLABLE)</span><span class="sxs-lookup"><span data-stu-id="cf46b-246">(KAGPROP_MARSHALLABLE)</span></span></p></td>
<td><p><span data-ttu-id="cf46b-247">Указывает, что драйвер ODBC создает набор записей, который может быть упакован</span><span class="sxs-lookup"><span data-stu-id="cf46b-247">Indicates that the ODBC driver generates a recordset that can be marshaled</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-text"></a><span data-ttu-id="cf46b-248">Текст команды</span><span class="sxs-lookup"><span data-stu-id="cf46b-248">Command Text</span></span>

<span data-ttu-id="cf46b-249">Как использовать объект [команды](command-object-ado.md) во многом зависит от источника данных и какой тип оператора запроса или команды будет принимать.</span><span class="sxs-lookup"><span data-stu-id="cf46b-249">How you use the [Command](command-object-ado.md) object largely depends on the data source, and what type of query or command statement it will accept.</span></span>

<span data-ttu-id="cf46b-250">ODBC предоставляет определенный синтаксис для вызова хранимых процедур.</span><span class="sxs-lookup"><span data-stu-id="cf46b-250">ODBC provides a specific syntax for calling stored procedures.</span></span> <span data-ttu-id="cf46b-251">Для свойства [CommandText](commandtext-property-ado.md) объекта **команды** *CommandText* аргумента метода **Execute** на объект [подключения](connection-object-ado.md) и *исходный* аргумент методу **Open** на [набора записей](recordset-object-ado.md) объект передает в строку с помощью следующего синтаксиса:</span><span class="sxs-lookup"><span data-stu-id="cf46b-251">For the [CommandText](commandtext-property-ado.md) property of a **Command** object, the *CommandText* argument to the **Execute** method on a [Connection](connection-object-ado.md) object, or the *Source* argument to the **Open** method on a [Recordset](recordset-object-ado.md) object, passes in a string with this syntax:</span></span>

`"{ [ ? = ] call procedure [ ( ? [, ? [ ,  ]] ) ] }"`

<span data-ttu-id="cf46b-252">Каждый **?**</span><span class="sxs-lookup"><span data-stu-id="cf46b-252">Each **?**</span></span> <span data-ttu-id="cf46b-253">содержит ссылку на объект в коллекции [параметров](parameters-collection-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="cf46b-253">references an object in the [Parameters](parameters-collection-ado.md) collection.</span></span> <span data-ttu-id="cf46b-254">Первый **?**</span><span class="sxs-lookup"><span data-stu-id="cf46b-254">The first **?**</span></span> <span data-ttu-id="cf46b-255">ссылки на **Параметры**(0), Далее **?**</span><span class="sxs-lookup"><span data-stu-id="cf46b-255">references **Parameters**(0), the next **?**</span></span> <span data-ttu-id="cf46b-256">Создание ссылки **Параметры**(1) и т. д.</span><span class="sxs-lookup"><span data-stu-id="cf46b-256">references **Parameters**(1), and so on.</span></span>

<span data-ttu-id="cf46b-257">Параметр ссылки являются необязательными и зависят от структуры хранимую процедуру.</span><span class="sxs-lookup"><span data-stu-id="cf46b-257">The parameter references are optional and depend on the structure of the stored procedure.</span></span> <span data-ttu-id="cf46b-258">Если вы хотите вызвать хранимую процедуру, определяющий без параметров, строка будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="cf46b-258">If you want to call a stored procedure that defines no parameters, your string would look like this:</span></span>

`"{ call procedure }"`

<span data-ttu-id="cf46b-259">Если у вас есть два параметра запроса, строка будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="cf46b-259">If you have two query parameters, your string would look like this:</span></span>

`"{ call procedure ( ?, ? ) }"`

<span data-ttu-id="cf46b-260">Если хранимая процедура возвращает значение, возвращаемое значение обрабатывается как еще один параметр.</span><span class="sxs-lookup"><span data-stu-id="cf46b-260">If the stored procedure will return a value, the return value is treated as another parameter.</span></span> <span data-ttu-id="cf46b-261">Если у вас нет параметров запроса, но возвращаемое значение, строка будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="cf46b-261">If you have no query parameters but you do have a return value, your string would look like this:</span></span>

`"{ ? = call procedure }"`

<span data-ttu-id="cf46b-262">И, наконец Если у вас есть возвращаемое значение и два параметра запроса, строка будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="cf46b-262">Finally, if you have a return value and two query parameters, your string would look like this:</span></span>

`"{ ? = call procedure ( ?, ? ) }"`

## <a name="recordset-behavior"></a><span data-ttu-id="cf46b-263">Поведение набора записей</span><span class="sxs-lookup"><span data-stu-id="cf46b-263">Recordset Behavior</span></span>

<span data-ttu-id="cf46b-264">В следующих таблицах перечислены стандартные ADO методы и свойства, доступные для объекта **набора записей** , открытых с этим поставщиком.</span><span class="sxs-lookup"><span data-stu-id="cf46b-264">The following tables list the standard ADO methods and properties available on a **Recordset** object opened with this provider.</span></span>

<span data-ttu-id="cf46b-265">Для получения дополнительных сведений о поведении **набора записей** для вашей конфигурации поставщика, выполните метод [поддерживает](supports-method-ado.md) и перечисления коллекции **свойств** **набора записей** для определения целесообразности поставщиком динамических свойства отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="cf46b-265">For more detailed information about **Recordset** behavior for your provider configuration, run the [Supports](supports-method-ado.md) method and enumerate the **Properties** collection of the **Recordset** to determine whether provider-specific dynamic properties are present.</span></span>

<span data-ttu-id="cf46b-266">Доступность стандартными свойствами ADO **набора записей** :</span><span class="sxs-lookup"><span data-stu-id="cf46b-266">Availability of standard ADO **Recordset** properties:</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cf46b-267">Свойство</span><span class="sxs-lookup"><span data-stu-id="cf46b-267">Property</span></span></p></th>
<th><p><span data-ttu-id="cf46b-268">ForwardOnly</span><span class="sxs-lookup"><span data-stu-id="cf46b-268">ForwardOnly</span></span></p></th>
<th><p><span data-ttu-id="cf46b-269">Динамическая группа</span><span class="sxs-lookup"><span data-stu-id="cf46b-269">Dynamic</span></span></p></th>
<th><p><span data-ttu-id="cf46b-270">Набор ключей</span><span class="sxs-lookup"><span data-stu-id="cf46b-270">Keyset</span></span></p></th>
<th><p><span data-ttu-id="cf46b-271">Статическое</span><span class="sxs-lookup"><span data-stu-id="cf46b-271">Static</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-272"><a href="absolutepage-property-ado.md">AbsolutePage</a></span><span class="sxs-lookup"><span data-stu-id="cf46b-272"><a href="absolutepage-property-ado.md">AbsolutePage</a></span></span></p></td>
<td><p><span data-ttu-id="cf46b-273">Недоступен</span><span class="sxs-lookup"><span data-stu-id="cf46b-273">not available</span></span></p></td>
<td><p><span data-ttu-id="cf46b-274">Недоступен</span><span class="sxs-lookup"><span data-stu-id="cf46b-274">not available</span></span></p></td>
<td><p><span data-ttu-id="cf46b-275">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cf46b-275">read/write</span></span></p></td>
<td><p><span data-ttu-id="cf46b-276">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cf46b-276">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-277"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span><span class="sxs-lookup"><span data-stu-id="cf46b-277"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span></span></p></td>
<td><p><span data-ttu-id="cf46b-278">Недоступен</span><span class="sxs-lookup"><span data-stu-id="cf46b-278">not available</span></span></p></td>
<td><p><span data-ttu-id="cf46b-279">Недоступен</span><span class="sxs-lookup"><span data-stu-id="cf46b-279">not available</span></span></p></td>
<td><p><span data-ttu-id="cf46b-280">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cf46b-280">read/write</span></span></p></td>
<td><p><span data-ttu-id="cf46b-281">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cf46b-281">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-282"><a href="activeconnection-property-ado.md">ActiveConnection</a></span><span class="sxs-lookup"><span data-stu-id="cf46b-282"><a href="activeconnection-property-ado.md">ActiveConnection</a></span></span></p></td>
<td><p><span data-ttu-id="cf46b-283">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cf46b-283">read/write</span></span></p></td>
<td><p><span data-ttu-id="cf46b-284">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cf46b-284">read/write</span></span></p></td>
<td><p><span data-ttu-id="cf46b-285">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cf46b-285">read/write</span></span></p></td>
<td><p><span data-ttu-id="cf46b-286">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cf46b-286">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-287"><a href="bof-eof-properties-ado.md">BOF</a></span><span class="sxs-lookup"><span data-stu-id="cf46b-287"><a href="bof-eof-properties-ado.md">BOF</a></span></span></p></td>
<td><p><span data-ttu-id="cf46b-288">только для чтения</span><span class="sxs-lookup"><span data-stu-id="cf46b-288">read-only</span></span></p></td>
<td><p><span data-ttu-id="cf46b-289">только для чтения</span><span class="sxs-lookup"><span data-stu-id="cf46b-289">read-only</span></span></p></td>
<td><p><span data-ttu-id="cf46b-290">только для чтения</span><span class="sxs-lookup"><span data-stu-id="cf46b-290">read-only</span></span></p></td>
<td><p><span data-ttu-id="cf46b-291">только для чтения</span><span class="sxs-lookup"><span data-stu-id="cf46b-291">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-292"><a href="bookmark-property-ado.md">Bookmark</a></span><span class="sxs-lookup"><span data-stu-id="cf46b-292"><a href="bookmark-property-ado.md">Bookmark</a></span></span></p></td>
<td><p><span data-ttu-id="cf46b-293">Недоступен</span><span class="sxs-lookup"><span data-stu-id="cf46b-293">not available</span></span></p></td>
<td><p><span data-ttu-id="cf46b-294">Недоступен</span><span class="sxs-lookup"><span data-stu-id="cf46b-294">not available</span></span></p></td>
<td><p><span data-ttu-id="cf46b-295">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cf46b-295">read/write</span></span></p></td>
<td><p><span data-ttu-id="cf46b-296">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cf46b-296">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-297"><a href="cachesize-property-ado.md">CacheSize</a></span><span class="sxs-lookup"><span data-stu-id="cf46b-297"><a href="cachesize-property-ado.md">CacheSize</a></span></span></p></td>
<td><p><span data-ttu-id="cf46b-298">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cf46b-298">read/write</span></span></p></td>
<td><p><span data-ttu-id="cf46b-299">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cf46b-299">read/write</span></span></p></td>
<td><p><span data-ttu-id="cf46b-300">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cf46b-300">read/write</span></span></p></td>
<td><p><span data-ttu-id="cf46b-301">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cf46b-301">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-302"><a href="cursorlocation-property-ado.md">CursorLocation</a></span><span class="sxs-lookup"><span data-stu-id="cf46b-302"><a href="cursorlocation-property-ado.md">CursorLocation</a></span></span></p></td>
<td><p><span data-ttu-id="cf46b-303">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cf46b-303">read/write</span></span></p></td>
<td><p><span data-ttu-id="cf46b-304">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cf46b-304">read/write</span></span></p></td>
<td><p><span data-ttu-id="cf46b-305">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cf46b-305">read/write</span></span></p></td>
<td><p><span data-ttu-id="cf46b-306">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cf46b-306">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-307"><a href="cursortype-property-ado.md">CursorType</a></span><span class="sxs-lookup"><span data-stu-id="cf46b-307"><a href="cursortype-property-ado.md">CursorType</a></span></span></p></td>
<td><p><span data-ttu-id="cf46b-308">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cf46b-308">read/write</span></span></p></td>
<td><p><span data-ttu-id="cf46b-309">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cf46b-309">read/write</span></span></p></td>
<td><p><span data-ttu-id="cf46b-310">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cf46b-310">read/write</span></span></p></td>
<td><p><span data-ttu-id="cf46b-311">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cf46b-311">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-312"><a href="editmode-property-ado.md">EditMode</a></span><span class="sxs-lookup"><span data-stu-id="cf46b-312"><a href="editmode-property-ado.md">EditMode</a></span></span></p></td>
<td><p><span data-ttu-id="cf46b-313">только для чтения</span><span class="sxs-lookup"><span data-stu-id="cf46b-313">read-only</span></span></p></td>
<td><p><span data-ttu-id="cf46b-314">только для чтения</span><span class="sxs-lookup"><span data-stu-id="cf46b-314">read-only</span></span></p></td>
<td><p><span data-ttu-id="cf46b-315">только для чтения</span><span class="sxs-lookup"><span data-stu-id="cf46b-315">read-only</span></span></p></td>
<td><p><span data-ttu-id="cf46b-316">только для чтения</span><span class="sxs-lookup"><span data-stu-id="cf46b-316">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-317"><a href="filter-property-ado.md">Фильтр</a></span><span class="sxs-lookup"><span data-stu-id="cf46b-317"><a href="filter-property-ado.md">Filter</a></span></span></p></td>
<td><p><span data-ttu-id="cf46b-318">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cf46b-318">read/write</span></span></p></td>
<td><p><span data-ttu-id="cf46b-319">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cf46b-319">read/write</span></span></p></td>
<td><p><span data-ttu-id="cf46b-320">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cf46b-320">read/write</span></span></p></td>
<td><p><span data-ttu-id="cf46b-321">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cf46b-321">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-322"><a href="locktype-property-ado.md">LockType для</a></span><span class="sxs-lookup"><span data-stu-id="cf46b-322"><a href="locktype-property-ado.md">LockType</a></span></span></p></td>
<td><p><span data-ttu-id="cf46b-323">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cf46b-323">read/write</span></span></p></td>
<td><p><span data-ttu-id="cf46b-324">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cf46b-324">read/write</span></span></p></td>
<td><p><span data-ttu-id="cf46b-325">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cf46b-325">read/write</span></span></p></td>
<td><p><span data-ttu-id="cf46b-326">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cf46b-326">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-327"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span><span class="sxs-lookup"><span data-stu-id="cf46b-327"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span></span></p></td>
<td><p><span data-ttu-id="cf46b-328">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cf46b-328">read/write</span></span></p></td>
<td><p><span data-ttu-id="cf46b-329">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cf46b-329">read/write</span></span></p></td>
<td><p><span data-ttu-id="cf46b-330">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cf46b-330">read/write</span></span></p></td>
<td><p><span data-ttu-id="cf46b-331">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cf46b-331">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-332"><a href="maxrecords-property-ado.md">MaxRecords</a></span><span class="sxs-lookup"><span data-stu-id="cf46b-332"><a href="maxrecords-property-ado.md">MaxRecords</a></span></span></p></td>
<td><p><span data-ttu-id="cf46b-333">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cf46b-333">read/write</span></span></p></td>
<td><p><span data-ttu-id="cf46b-334">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cf46b-334">read/write</span></span></p></td>
<td><p><span data-ttu-id="cf46b-335">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cf46b-335">read/write</span></span></p></td>
<td><p><span data-ttu-id="cf46b-336">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cf46b-336">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-337"><a href="pagecount-property-ado.md">PageCount</a></span><span class="sxs-lookup"><span data-stu-id="cf46b-337"><a href="pagecount-property-ado.md">PageCount</a></span></span></p></td>
<td><p><span data-ttu-id="cf46b-338">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cf46b-338">read/write</span></span></p></td>
<td><p><span data-ttu-id="cf46b-339">Недоступен</span><span class="sxs-lookup"><span data-stu-id="cf46b-339">not available</span></span></p></td>
<td><p><span data-ttu-id="cf46b-340">только для чтения</span><span class="sxs-lookup"><span data-stu-id="cf46b-340">read-only</span></span></p></td>
<td><p><span data-ttu-id="cf46b-341">только для чтения</span><span class="sxs-lookup"><span data-stu-id="cf46b-341">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-342"><a href="pagesize-property-ado.md">PageSize</a></span><span class="sxs-lookup"><span data-stu-id="cf46b-342"><a href="pagesize-property-ado.md">PageSize</a></span></span></p></td>
<td><p><span data-ttu-id="cf46b-343">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cf46b-343">read/write</span></span></p></td>
<td><p><span data-ttu-id="cf46b-344">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cf46b-344">read/write</span></span></p></td>
<td><p><span data-ttu-id="cf46b-345">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cf46b-345">read/write</span></span></p></td>
<td><p><span data-ttu-id="cf46b-346">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cf46b-346">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-347"><a href="recordcount-property-ado.md">RecordCount</a></span><span class="sxs-lookup"><span data-stu-id="cf46b-347"><a href="recordcount-property-ado.md">RecordCount</a></span></span></p></td>
<td><p><span data-ttu-id="cf46b-348">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cf46b-348">read/write</span></span></p></td>
<td><p><span data-ttu-id="cf46b-349">Недоступен</span><span class="sxs-lookup"><span data-stu-id="cf46b-349">not available</span></span></p></td>
<td><p><span data-ttu-id="cf46b-350">только для чтения</span><span class="sxs-lookup"><span data-stu-id="cf46b-350">read-only</span></span></p></td>
<td><p><span data-ttu-id="cf46b-351">только для чтения</span><span class="sxs-lookup"><span data-stu-id="cf46b-351">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-352"><a href="source-property-ado-recordset.md">Source</a></span><span class="sxs-lookup"><span data-stu-id="cf46b-352"><a href="source-property-ado-recordset.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="cf46b-353">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cf46b-353">read/write</span></span></p></td>
<td><p><span data-ttu-id="cf46b-354">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cf46b-354">read/write</span></span></p></td>
<td><p><span data-ttu-id="cf46b-355">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cf46b-355">read/write</span></span></p></td>
<td><p><span data-ttu-id="cf46b-356">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cf46b-356">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-357"><a href="state-property-ado.md">State</a></span><span class="sxs-lookup"><span data-stu-id="cf46b-357"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="cf46b-358">только для чтения</span><span class="sxs-lookup"><span data-stu-id="cf46b-358">read-only</span></span></p></td>
<td><p><span data-ttu-id="cf46b-359">только для чтения</span><span class="sxs-lookup"><span data-stu-id="cf46b-359">read-only</span></span></p></td>
<td><p><span data-ttu-id="cf46b-360">только для чтения</span><span class="sxs-lookup"><span data-stu-id="cf46b-360">read-only</span></span></p></td>
<td><p><span data-ttu-id="cf46b-361">только для чтения</span><span class="sxs-lookup"><span data-stu-id="cf46b-361">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-362"><a href="status-property-ado-recordset.md">Status</a></span><span class="sxs-lookup"><span data-stu-id="cf46b-362"><a href="status-property-ado-recordset.md">Status</a></span></span></p></td>
<td><p><span data-ttu-id="cf46b-363">только для чтения</span><span class="sxs-lookup"><span data-stu-id="cf46b-363">read-only</span></span></p></td>
<td><p><span data-ttu-id="cf46b-364">только для чтения</span><span class="sxs-lookup"><span data-stu-id="cf46b-364">read-only</span></span></p></td>
<td><p><span data-ttu-id="cf46b-365">только для чтения</span><span class="sxs-lookup"><span data-stu-id="cf46b-365">read-only</span></span></p></td>
<td><p><span data-ttu-id="cf46b-366">только для чтения</span><span class="sxs-lookup"><span data-stu-id="cf46b-366">read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cf46b-367">Свойства [AbsolutePosition](absoluteposition-property-ado.md) и [AbsolutePage](absolutepage-property-ado.md) доступны только для записи при использовании ADO с версии 1.0 поставщик Microsoft OLE DB для ODBC.</span><span class="sxs-lookup"><span data-stu-id="cf46b-367">The [AbsolutePosition](absoluteposition-property-ado.md) and [AbsolutePage](absolutepage-property-ado.md) properties are write-only when ADO is used with version 1.0 of the Microsoft OLE DB Provider for ODBC.</span></span>

<span data-ttu-id="cf46b-368">Доступность стандартных способов ADO **набора записей** :</span><span class="sxs-lookup"><span data-stu-id="cf46b-368">Availability of standard ADO **Recordset** methods:</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cf46b-369">Method</span><span class="sxs-lookup"><span data-stu-id="cf46b-369">Method</span></span></p></th>
<th><p><span data-ttu-id="cf46b-370">ForwardOnly</span><span class="sxs-lookup"><span data-stu-id="cf46b-370">ForwardOnly</span></span></p></th>
<th><p><span data-ttu-id="cf46b-371">Динамическая группа</span><span class="sxs-lookup"><span data-stu-id="cf46b-371">Dynamic</span></span></p></th>
<th><p><span data-ttu-id="cf46b-372">Набор ключей</span><span class="sxs-lookup"><span data-stu-id="cf46b-372">Keyset</span></span></p></th>
<th><p><span data-ttu-id="cf46b-373">Статическое</span><span class="sxs-lookup"><span data-stu-id="cf46b-373">Static</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-374"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="cf46b-374"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="cf46b-375">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-375">Yes</span></span></p></td>
<td><p><span data-ttu-id="cf46b-376">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-376">Yes</span></span></p></td>
<td><p><span data-ttu-id="cf46b-377">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-377">Yes</span></span></p></td>
<td><p><span data-ttu-id="cf46b-378">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-378">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-379"><a href="cancel-method-ado.md">Отмена</a></span><span class="sxs-lookup"><span data-stu-id="cf46b-379"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="cf46b-380">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-380">Yes</span></span></p></td>
<td><p><span data-ttu-id="cf46b-381">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-381">Yes</span></span></p></td>
<td><p><span data-ttu-id="cf46b-382">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-382">Yes</span></span></p></td>
<td><p><span data-ttu-id="cf46b-383">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-383">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-384"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="cf46b-384"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="cf46b-385">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-385">Yes</span></span></p></td>
<td><p><span data-ttu-id="cf46b-386">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-386">Yes</span></span></p></td>
<td><p><span data-ttu-id="cf46b-387">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-387">Yes</span></span></p></td>
<td><p><span data-ttu-id="cf46b-388">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-388">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-389"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="cf46b-389"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="cf46b-390">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-390">Yes</span></span></p></td>
<td><p><span data-ttu-id="cf46b-391">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-391">Yes</span></span></p></td>
<td><p><span data-ttu-id="cf46b-392">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-392">Yes</span></span></p></td>
<td><p><span data-ttu-id="cf46b-393">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-393">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-394"><a href="clone-method-ado.md">Clone</a></span><span class="sxs-lookup"><span data-stu-id="cf46b-394"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="cf46b-395">Нет</span><span class="sxs-lookup"><span data-stu-id="cf46b-395">No</span></span></p></td>
<td><p><span data-ttu-id="cf46b-396">Нет</span><span class="sxs-lookup"><span data-stu-id="cf46b-396">No</span></span></p></td>
<td><p><span data-ttu-id="cf46b-397">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-397">Yes</span></span></p></td>
<td><p><span data-ttu-id="cf46b-398">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-398">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-399"><a href="close-method-ado.md">Close</a></span><span class="sxs-lookup"><span data-stu-id="cf46b-399"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="cf46b-400">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-400">Yes</span></span></p></td>
<td><p><span data-ttu-id="cf46b-401">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-401">Yes</span></span></p></td>
<td><p><span data-ttu-id="cf46b-402">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-402">Yes</span></span></p></td>
<td><p><span data-ttu-id="cf46b-403">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-403">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-404"><a href="delete-method-ado-recordset.md">удаление</a>;</span><span class="sxs-lookup"><span data-stu-id="cf46b-404"><a href="delete-method-ado-recordset.md">Delete</a></span></span></p></td>
<td><p><span data-ttu-id="cf46b-405">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-405">Yes</span></span></p></td>
<td><p><span data-ttu-id="cf46b-406">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-406">Yes</span></span></p></td>
<td><p><span data-ttu-id="cf46b-407">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-407">Yes</span></span></p></td>
<td><p><span data-ttu-id="cf46b-408">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-408">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-409"><a href="getrows-method-ado.md">Получение строк</a></span><span class="sxs-lookup"><span data-stu-id="cf46b-409"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="cf46b-410">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-410">Yes</span></span></p></td>
<td><p><span data-ttu-id="cf46b-411">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-411">Yes</span></span></p></td>
<td><p><span data-ttu-id="cf46b-412">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-412">Yes</span></span></p></td>
<td><p><span data-ttu-id="cf46b-413">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-413">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-414"><a href="move-method-ado.md">Move</a></span><span class="sxs-lookup"><span data-stu-id="cf46b-414"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="cf46b-415">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-415">Yes</span></span></p></td>
<td><p><span data-ttu-id="cf46b-416">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-416">Yes</span></span></p></td>
<td><p><span data-ttu-id="cf46b-417">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-417">Yes</span></span></p></td>
<td><p><span data-ttu-id="cf46b-418">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-418">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-419"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span><span class="sxs-lookup"><span data-stu-id="cf46b-419"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span></span></p></td>
<td><p><span data-ttu-id="cf46b-420">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-420">Yes</span></span></p></td>
<td><p><span data-ttu-id="cf46b-421">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-421">Yes</span></span></p></td>
<td><p><span data-ttu-id="cf46b-422">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-422">Yes</span></span></p></td>
<td><p><span data-ttu-id="cf46b-423">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-423">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-424"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span><span class="sxs-lookup"><span data-stu-id="cf46b-424"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span></span></p></td>
<td><p><span data-ttu-id="cf46b-425">Нет</span><span class="sxs-lookup"><span data-stu-id="cf46b-425">No</span></span></p></td>
<td><p><span data-ttu-id="cf46b-426">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-426">Yes</span></span></p></td>
<td><p><span data-ttu-id="cf46b-427">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-427">Yes</span></span></p></td>
<td><p><span data-ttu-id="cf46b-428">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-428">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-429"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span><span class="sxs-lookup"><span data-stu-id="cf46b-429"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span></span></p></td>
<td><p><span data-ttu-id="cf46b-430">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-430">Yes</span></span></p></td>
<td><p><span data-ttu-id="cf46b-431">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-431">Yes</span></span></p></td>
<td><p><span data-ttu-id="cf46b-432">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-432">Yes</span></span></p></td>
<td><p><span data-ttu-id="cf46b-433">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-433">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-434"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span><span class="sxs-lookup"><span data-stu-id="cf46b-434"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span></span></p></td>
<td><p><span data-ttu-id="cf46b-435">Нет</span><span class="sxs-lookup"><span data-stu-id="cf46b-435">No</span></span></p></td>
<td><p><span data-ttu-id="cf46b-436">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-436">Yes</span></span></p></td>
<td><p><span data-ttu-id="cf46b-437">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-437">Yes</span></span></p></td>
<td><p><span data-ttu-id="cf46b-438">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-438">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-439"><a href="nextrecordset-method-ado.md">NextRecordset</a>\*</span><span class="sxs-lookup"><span data-stu-id="cf46b-439"><a href="nextrecordset-method-ado.md">NextRecordset</a>\*</span></span></p></td>
<td><p><span data-ttu-id="cf46b-440">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-440">Yes</span></span></p></td>
<td><p><span data-ttu-id="cf46b-441">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-441">Yes</span></span></p></td>
<td><p><span data-ttu-id="cf46b-442">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-442">Yes</span></span></p></td>
<td><p><span data-ttu-id="cf46b-443">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-443">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-444"><a href="open-method-ado-recordset.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="cf46b-444"><a href="open-method-ado-recordset.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="cf46b-445">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-445">Yes</span></span></p></td>
<td><p><span data-ttu-id="cf46b-446">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-446">Yes</span></span></p></td>
<td><p><span data-ttu-id="cf46b-447">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-447">Yes</span></span></p></td>
<td><p><span data-ttu-id="cf46b-448">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-448">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-449"><a href="requery-method-ado.md">Requery</a></span><span class="sxs-lookup"><span data-stu-id="cf46b-449"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="cf46b-450">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-450">Yes</span></span></p></td>
<td><p><span data-ttu-id="cf46b-451">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-451">Yes</span></span></p></td>
<td><p><span data-ttu-id="cf46b-452">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-452">Yes</span></span></p></td>
<td><p><span data-ttu-id="cf46b-453">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-453">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-454"><a href="resync-method-ado.md">Выполнить повторную синхронизацию</a></span><span class="sxs-lookup"><span data-stu-id="cf46b-454"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="cf46b-455">Нет</span><span class="sxs-lookup"><span data-stu-id="cf46b-455">No</span></span></p></td>
<td><p><span data-ttu-id="cf46b-456">Нет</span><span class="sxs-lookup"><span data-stu-id="cf46b-456">No</span></span></p></td>
<td><p><span data-ttu-id="cf46b-457">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-457">Yes</span></span></p></td>
<td><p><span data-ttu-id="cf46b-458">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-458">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-459"><a href="supports-method-ado.md">Поддерживает</a></span><span class="sxs-lookup"><span data-stu-id="cf46b-459"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="cf46b-460">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-460">Yes</span></span></p></td>
<td><p><span data-ttu-id="cf46b-461">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-461">Yes</span></span></p></td>
<td><p><span data-ttu-id="cf46b-462">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-462">Yes</span></span></p></td>
<td><p><span data-ttu-id="cf46b-463">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-463">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-464"><a href="update-method-ado.md">обновление</a>.</span><span class="sxs-lookup"><span data-stu-id="cf46b-464"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="cf46b-465">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-465">Yes</span></span></p></td>
<td><p><span data-ttu-id="cf46b-466">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-466">Yes</span></span></p></td>
<td><p><span data-ttu-id="cf46b-467">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-467">Yes</span></span></p></td>
<td><p><span data-ttu-id="cf46b-468">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-468">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-469"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="cf46b-469"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="cf46b-470">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-470">Yes</span></span></p></td>
<td><p><span data-ttu-id="cf46b-471">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-471">Yes</span></span></p></td>
<td><p><span data-ttu-id="cf46b-472">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-472">Yes</span></span></p></td>
<td><p><span data-ttu-id="cf46b-473">Да</span><span class="sxs-lookup"><span data-stu-id="cf46b-473">Yes</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cf46b-474">\*Не поддерживается для баз данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="cf46b-474">\*Not supported for Microsoft Access databases.</span></span>

## <a name="dynamic-properties"></a><span data-ttu-id="cf46b-475">Динамические свойства</span><span class="sxs-lookup"><span data-stu-id="cf46b-475">Dynamic Properties</span></span>

<span data-ttu-id="cf46b-476">Поставщик Microsoft OLE DB для ODBC вставляет несколько динамических свойств в коллекцию **свойств** объектов неоткрытый [подключения](connection-object-ado.md), [записей](recordset-object-ado.md)и [команды](command-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="cf46b-476">The Microsoft OLE DB Provider for ODBC inserts several dynamic properties into the **Properties** collection of the unopened [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md), and [Command](command-object-ado.md) objects.</span></span>

<span data-ttu-id="cf46b-477">В таблицах ниже — это cross-index имен ADO и OLE DB для каждого динамического свойства.</span><span class="sxs-lookup"><span data-stu-id="cf46b-477">The tables below are a cross-index of the ADO and OLE DB names for each dynamic property.</span></span> <span data-ttu-id="cf46b-478">Справочник программиста OLE DB указано имя свойства ADO по слову «Описание».</span><span class="sxs-lookup"><span data-stu-id="cf46b-478">The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description."</span></span> <span data-ttu-id="cf46b-479">Дополнительные сведения об этих свойств можно найти в Справочник программиста OLE DB.</span><span class="sxs-lookup"><span data-stu-id="cf46b-479">You can find more information about these properties in the OLE DB Programmer's Reference.</span></span> <span data-ttu-id="cf46b-480">Поиск имени свойства OLE DB в индексе или просмотреть приложение C: OLE DB свойства.</span><span class="sxs-lookup"><span data-stu-id="cf46b-480">Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span></span>

## <a name="connection-dynamic-properties"></a><span data-ttu-id="cf46b-481">Динамические свойства подключения</span><span class="sxs-lookup"><span data-stu-id="cf46b-481">Connection Dynamic Properties</span></span>

<span data-ttu-id="cf46b-482">Коллекция **Properties** объект **подключения** добавляются следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="cf46b-482">The following properties are added to the **Connection** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cf46b-483">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="cf46b-483">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="cf46b-484">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="cf46b-484">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-485">Активных сеансов</span><span class="sxs-lookup"><span data-stu-id="cf46b-485">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="cf46b-486">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="cf46b-486">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-487">Прерывание Asynchable</span><span class="sxs-lookup"><span data-stu-id="cf46b-487">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="cf46b-488">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="cf46b-488">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-489">Зафиксировать Asynchable</span><span class="sxs-lookup"><span data-stu-id="cf46b-489">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="cf46b-490">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="cf46b-490">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-491">Уровни изоляции автоматической фиксации</span><span class="sxs-lookup"><span data-stu-id="cf46b-491">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="cf46b-492">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="cf46b-492">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-493">Расположение каталога</span><span class="sxs-lookup"><span data-stu-id="cf46b-493">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="cf46b-494">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="cf46b-494">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-495">Каталог терминов</span><span class="sxs-lookup"><span data-stu-id="cf46b-495">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="cf46b-496">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="cf46b-496">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-497">Определение столбца</span><span class="sxs-lookup"><span data-stu-id="cf46b-497">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="cf46b-498">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="cf46b-498">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-499">Время ожидания подключения</span><span class="sxs-lookup"><span data-stu-id="cf46b-499">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="cf46b-500">DBPROP_INIT_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="cf46b-500">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-501">Текущий каталог</span><span class="sxs-lookup"><span data-stu-id="cf46b-501">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="cf46b-502">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="cf46b-502">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-503">Источник данных</span><span class="sxs-lookup"><span data-stu-id="cf46b-503">Data Source</span></span></p></td>
<td><p><span data-ttu-id="cf46b-504">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="cf46b-504">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-505">Имя источника данных</span><span class="sxs-lookup"><span data-stu-id="cf46b-505">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="cf46b-506">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="cf46b-506">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-507">Модель потоков объекта источника данных</span><span class="sxs-lookup"><span data-stu-id="cf46b-507">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="cf46b-508">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="cf46b-508">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-509">Имя СУБД</span><span class="sxs-lookup"><span data-stu-id="cf46b-509">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="cf46b-510">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="cf46b-510">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-511">Версия СУБД</span><span class="sxs-lookup"><span data-stu-id="cf46b-511">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="cf46b-512">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="cf46b-512">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-513">Расширенные свойства</span><span class="sxs-lookup"><span data-stu-id="cf46b-513">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="cf46b-514">DBPROP_INIT_PROVIDERSTRING</span><span class="sxs-lookup"><span data-stu-id="cf46b-514">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-515">ГРУППИРОВКА по поддержке</span><span class="sxs-lookup"><span data-stu-id="cf46b-515">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="cf46b-516">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="cf46b-516">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-517">Поддержка разнородных таблиц</span><span class="sxs-lookup"><span data-stu-id="cf46b-517">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="cf46b-518">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="cf46b-518">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-519">Идентификатор регистра</span><span class="sxs-lookup"><span data-stu-id="cf46b-519">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="cf46b-520">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="cf46b-520">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-521">Исходный каталог</span><span class="sxs-lookup"><span data-stu-id="cf46b-521">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="cf46b-522">DBPROP_INIT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="cf46b-522">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-523">Уровни изоляции</span><span class="sxs-lookup"><span data-stu-id="cf46b-523">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="cf46b-524">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="cf46b-524">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-525">Хранение изоляции</span><span class="sxs-lookup"><span data-stu-id="cf46b-525">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="cf46b-526">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="cf46b-526">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-527">Идентификатор языка</span><span class="sxs-lookup"><span data-stu-id="cf46b-527">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="cf46b-528">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="cf46b-528">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-529">Location</span><span class="sxs-lookup"><span data-stu-id="cf46b-529">Location</span></span></p></td>
<td><p><span data-ttu-id="cf46b-530">DBPROP_INIT_LOCATION</span><span class="sxs-lookup"><span data-stu-id="cf46b-530">DBPROP_INIT_LOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-531">Максимальный размер индекса</span><span class="sxs-lookup"><span data-stu-id="cf46b-531">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="cf46b-532">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="cf46b-532">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-533">Максимальный размер строки</span><span class="sxs-lookup"><span data-stu-id="cf46b-533">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="cf46b-534">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="cf46b-534">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-535">Максимальный размер строки включает в себя больших двоичных ОБЪЕКТОВ</span><span class="sxs-lookup"><span data-stu-id="cf46b-535">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="cf46b-536">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="cf46b-536">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-537">Максимальная таблиц в Выбор</span><span class="sxs-lookup"><span data-stu-id="cf46b-537">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="cf46b-538">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="cf46b-538">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-539">Режим</span><span class="sxs-lookup"><span data-stu-id="cf46b-539">Mode</span></span></p></td>
<td><p><span data-ttu-id="cf46b-540">DBPROP_INIT_MODE</span><span class="sxs-lookup"><span data-stu-id="cf46b-540">DBPROP_INIT_MODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-541">Несколько наборов параметров</span><span class="sxs-lookup"><span data-stu-id="cf46b-541">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="cf46b-542">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="cf46b-542">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-543">Несколько результатов</span><span class="sxs-lookup"><span data-stu-id="cf46b-543">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="cf46b-544">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="cf46b-544">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-545">Несколько объектов хранения</span><span class="sxs-lookup"><span data-stu-id="cf46b-545">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="cf46b-546">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="cf46b-546">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-547">Обновление нескольких таблицы</span><span class="sxs-lookup"><span data-stu-id="cf46b-547">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="cf46b-548">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="cf46b-548">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-549">Порядок сортировки значений NULL</span><span class="sxs-lookup"><span data-stu-id="cf46b-549">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="cf46b-550">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="cf46b-550">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-551">Поведение NULL объединения</span><span class="sxs-lookup"><span data-stu-id="cf46b-551">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="cf46b-552">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="cf46b-552">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-553">Службы OLE DB</span><span class="sxs-lookup"><span data-stu-id="cf46b-553">OLE DB Services</span></span></p></td>
<td><p><span data-ttu-id="cf46b-554">DBPROP_INIT_OLEDBSERVICES, УСТАНОВИТЬ</span><span class="sxs-lookup"><span data-stu-id="cf46b-554">DBPROP_INIT_OLEDBSERVICES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-555">Версия OLE DB</span><span class="sxs-lookup"><span data-stu-id="cf46b-555">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="cf46b-556">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="cf46b-556">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-557">Поддержка OLE-объектов</span><span class="sxs-lookup"><span data-stu-id="cf46b-557">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="cf46b-558">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="cf46b-558">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-559">Поддержка открытых наборов строк</span><span class="sxs-lookup"><span data-stu-id="cf46b-559">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="cf46b-560">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="cf46b-560">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-561">ORDER BY столбцы в списке Select</span><span class="sxs-lookup"><span data-stu-id="cf46b-561">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="cf46b-562">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="cf46b-562">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-563">Выходной параметр доступности</span><span class="sxs-lookup"><span data-stu-id="cf46b-563">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="cf46b-564">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="cf46b-564">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-565">Password</span><span class="sxs-lookup"><span data-stu-id="cf46b-565">Password</span></span></p></td>
<td><p><span data-ttu-id="cf46b-566">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="cf46b-566">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-567">Передайте с указанные методы</span><span class="sxs-lookup"><span data-stu-id="cf46b-567">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="cf46b-568">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="cf46b-568">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-569">Сохранять сведения о безопасности</span><span class="sxs-lookup"><span data-stu-id="cf46b-569">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="cf46b-570">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span><span class="sxs-lookup"><span data-stu-id="cf46b-570">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-571">Тип сохраняемого идентификатора</span><span class="sxs-lookup"><span data-stu-id="cf46b-571">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="cf46b-572">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="cf46b-572">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-573">Подготовка поведение аварийное завершение</span><span class="sxs-lookup"><span data-stu-id="cf46b-573">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="cf46b-574">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="cf46b-574">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-575">Подготовка поведение выделения</span><span class="sxs-lookup"><span data-stu-id="cf46b-575">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="cf46b-576">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="cf46b-576">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-577">Процедура терминов</span><span class="sxs-lookup"><span data-stu-id="cf46b-577">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="cf46b-578">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="cf46b-578">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-579">Запрос</span><span class="sxs-lookup"><span data-stu-id="cf46b-579">Prompt</span></span></p></td>
<td><p><span data-ttu-id="cf46b-580">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="cf46b-580">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-581">Понятное имя поставщика</span><span class="sxs-lookup"><span data-stu-id="cf46b-581">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="cf46b-582">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="cf46b-582">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-583">Имя поставщика</span><span class="sxs-lookup"><span data-stu-id="cf46b-583">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="cf46b-584">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="cf46b-584">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-585">Версия поставщика</span><span class="sxs-lookup"><span data-stu-id="cf46b-585">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="cf46b-586">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="cf46b-586">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-587">Источник данных только для чтения</span><span class="sxs-lookup"><span data-stu-id="cf46b-587">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="cf46b-588">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="cf46b-588">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-589">Преобразование строк на команду</span><span class="sxs-lookup"><span data-stu-id="cf46b-589">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="cf46b-590">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="cf46b-590">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-591">Схема терминов</span><span class="sxs-lookup"><span data-stu-id="cf46b-591">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="cf46b-592">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="cf46b-592">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-593">Об использовании схемы</span><span class="sxs-lookup"><span data-stu-id="cf46b-593">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="cf46b-594">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="cf46b-594">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-595">Поддержка SQL</span><span class="sxs-lookup"><span data-stu-id="cf46b-595">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="cf46b-596">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="cf46b-596">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-597">Структурированное хранилище</span><span class="sxs-lookup"><span data-stu-id="cf46b-597">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="cf46b-598">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="cf46b-598">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-599">Поддержка вложенного запроса</span><span class="sxs-lookup"><span data-stu-id="cf46b-599">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="cf46b-600">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="cf46b-600">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-601">В таблице терминов</span><span class="sxs-lookup"><span data-stu-id="cf46b-601">Table Term</span></span></p></td>
<td><p><span data-ttu-id="cf46b-602">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="cf46b-602">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-603">Транзакций DDL</span><span class="sxs-lookup"><span data-stu-id="cf46b-603">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="cf46b-604">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="cf46b-604">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-605">Идентификатор пользователя</span><span class="sxs-lookup"><span data-stu-id="cf46b-605">User ID</span></span></p></td>
<td><p><span data-ttu-id="cf46b-606">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="cf46b-606">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-607">Имя пользователя</span><span class="sxs-lookup"><span data-stu-id="cf46b-607">User Name</span></span></p></td>
<td><p><span data-ttu-id="cf46b-608">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="cf46b-608">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-609">Дескриптор окна</span><span class="sxs-lookup"><span data-stu-id="cf46b-609">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="cf46b-610">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="cf46b-610">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a><span data-ttu-id="cf46b-611">Свойства динамической набора записей</span><span class="sxs-lookup"><span data-stu-id="cf46b-611">Recordset Dynamic Properties</span></span>

<span data-ttu-id="cf46b-612">Следующие свойства добавляются в коллекцию **свойств** объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="cf46b-612">The following properties are added to the **Recordset** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cf46b-613">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="cf46b-613">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="cf46b-614">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="cf46b-614">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-615">Порядок доступа</span><span class="sxs-lookup"><span data-stu-id="cf46b-615">Access Order</span></span></p></td>
<td><p><span data-ttu-id="cf46b-616">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="cf46b-616">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-617">Блокировка объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="cf46b-617">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="cf46b-618">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="cf46b-618">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-619">Тип закладки</span><span class="sxs-lookup"><span data-stu-id="cf46b-619">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="cf46b-620">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="cf46b-620">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-621">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="cf46b-621">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="cf46b-622">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="cf46b-622">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-623">Изменение вставленных строк</span><span class="sxs-lookup"><span data-stu-id="cf46b-623">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="cf46b-624">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="cf46b-624">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-625">Права доступа столбца</span><span class="sxs-lookup"><span data-stu-id="cf46b-625">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="cf46b-626">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="cf46b-626">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-627">Столбец набор уведомлений</span><span class="sxs-lookup"><span data-stu-id="cf46b-627">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="cf46b-628">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="cf46b-628">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-629">Отложенное обновление объекта хранения</span><span class="sxs-lookup"><span data-stu-id="cf46b-629">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="cf46b-630">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="cf46b-630">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-631">Выборку</span><span class="sxs-lookup"><span data-stu-id="cf46b-631">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="cf46b-632">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="cf46b-632">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-633">Хранение строк</span><span class="sxs-lookup"><span data-stu-id="cf46b-633">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="cf46b-634">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="cf46b-634">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-635">IAccessor</span><span class="sxs-lookup"><span data-stu-id="cf46b-635">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="cf46b-636">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="cf46b-636">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-637">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="cf46b-637">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="cf46b-638">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="cf46b-638">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-639">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="cf46b-639">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="cf46b-640">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="cf46b-640">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-641">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="cf46b-641">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="cf46b-642">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="cf46b-642">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-643">IConvertType</span><span class="sxs-lookup"><span data-stu-id="cf46b-643">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="cf46b-644">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="cf46b-644">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-645">Немобильные строки</span><span class="sxs-lookup"><span data-stu-id="cf46b-645">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="cf46b-646">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="cf46b-646">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-647">IRowset</span><span class="sxs-lookup"><span data-stu-id="cf46b-647">IRowset</span></span></p></td>
<td><p><span data-ttu-id="cf46b-648">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="cf46b-648">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-649">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="cf46b-649">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="cf46b-650">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="cf46b-650">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-651">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="cf46b-651">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="cf46b-652">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="cf46b-652">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-653">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="cf46b-653">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="cf46b-654">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="cf46b-654">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-655">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="cf46b-655">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="cf46b-656">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="cf46b-656">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-657">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="cf46b-657">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-658">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="cf46b-658">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="cf46b-659">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="cf46b-659">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-660">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="cf46b-660">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="cf46b-661">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="cf46b-661">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-662">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="cf46b-662">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="cf46b-663">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="cf46b-663">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-664">Литерал закладки</span><span class="sxs-lookup"><span data-stu-id="cf46b-664">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="cf46b-665">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="cf46b-665">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-666">Удостоверение литерала строки</span><span class="sxs-lookup"><span data-stu-id="cf46b-666">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="cf46b-667">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="cf46b-667">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-668">Максимальное число открытых строк</span><span class="sxs-lookup"><span data-stu-id="cf46b-668">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="cf46b-669">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="cf46b-669">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-670">Максимум ожидающие строк</span><span class="sxs-lookup"><span data-stu-id="cf46b-670">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="cf46b-671">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="cf46b-671">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-672">Максимальное число строк</span><span class="sxs-lookup"><span data-stu-id="cf46b-672">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="cf46b-673">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="cf46b-673">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-674">Степень детализации уведомлений</span><span class="sxs-lookup"><span data-stu-id="cf46b-674">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="cf46b-675">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="cf46b-675">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-676">Этапы уведомлений</span><span class="sxs-lookup"><span data-stu-id="cf46b-676">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="cf46b-677">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="cf46b-677">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-678">Объекты в транзакции</span><span class="sxs-lookup"><span data-stu-id="cf46b-678">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="cf46b-679">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="cf46b-679">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-680">Видны собственные изменения</span><span class="sxs-lookup"><span data-stu-id="cf46b-680">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="cf46b-681">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="cf46b-681">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-682">Видны собственные операции вставки</span><span class="sxs-lookup"><span data-stu-id="cf46b-682">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="cf46b-683">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="cf46b-683">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-684">Сохранять при аварийном завершении</span><span class="sxs-lookup"><span data-stu-id="cf46b-684">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="cf46b-685">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="cf46b-685">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-686">Сохранять при фиксации</span><span class="sxs-lookup"><span data-stu-id="cf46b-686">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="cf46b-687">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="cf46b-687">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-688">Быстрый перезапуск</span><span class="sxs-lookup"><span data-stu-id="cf46b-688">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="cf46b-689">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="cf46b-689">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-690">Повторные события</span><span class="sxs-lookup"><span data-stu-id="cf46b-690">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="cf46b-691">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="cf46b-691">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-692">Удаление удаленных строк</span><span class="sxs-lookup"><span data-stu-id="cf46b-692">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="cf46b-693">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="cf46b-693">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-694">Сообщить о нескольких изменений</span><span class="sxs-lookup"><span data-stu-id="cf46b-694">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="cf46b-695">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="cf46b-695">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-696">Вернуть ожидающие вставки</span><span class="sxs-lookup"><span data-stu-id="cf46b-696">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="cf46b-697">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="cf46b-697">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-698">Удалить строку уведомлений</span><span class="sxs-lookup"><span data-stu-id="cf46b-698">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="cf46b-699">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="cf46b-699">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-700">Строка первого уведомления об изменении</span><span class="sxs-lookup"><span data-stu-id="cf46b-700">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="cf46b-701">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="cf46b-701">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-702">Строка вставки уведомлений</span><span class="sxs-lookup"><span data-stu-id="cf46b-702">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="cf46b-703">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="cf46b-703">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-704">Привилегии строки</span><span class="sxs-lookup"><span data-stu-id="cf46b-704">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="cf46b-705">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="cf46b-705">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-706">Уведомления о повторной синхронизации строки</span><span class="sxs-lookup"><span data-stu-id="cf46b-706">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="cf46b-707">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="cf46b-707">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-708">Строка, потоковой модели</span><span class="sxs-lookup"><span data-stu-id="cf46b-708">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="cf46b-709">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="cf46b-709">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-710">Уведомление об изменении отмены строки</span><span class="sxs-lookup"><span data-stu-id="cf46b-710">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="cf46b-711">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="cf46b-711">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-712">Строка отмены Delete уведомлений</span><span class="sxs-lookup"><span data-stu-id="cf46b-712">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="cf46b-713">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="cf46b-713">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-714">Вставка отмены строки уведомлений</span><span class="sxs-lookup"><span data-stu-id="cf46b-714">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="cf46b-715">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="cf46b-715">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-716">Уведомление об обновлении строки</span><span class="sxs-lookup"><span data-stu-id="cf46b-716">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="cf46b-717">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="cf46b-717">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-718">Уведомление об изменении положения строк выборки</span><span class="sxs-lookup"><span data-stu-id="cf46b-718">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="cf46b-719">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="cf46b-719">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-720">Уведомление о выпуске набора строк</span><span class="sxs-lookup"><span data-stu-id="cf46b-720">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="cf46b-721">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="cf46b-721">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-722">Прокрутка назад</span><span class="sxs-lookup"><span data-stu-id="cf46b-722">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="cf46b-723">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="cf46b-723">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-724">Пропустить удаленных закладки</span><span class="sxs-lookup"><span data-stu-id="cf46b-724">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="cf46b-725">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="cf46b-725">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-726">Строка строгого удостоверений</span><span class="sxs-lookup"><span data-stu-id="cf46b-726">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="cf46b-727">DBPROP_STRONGITDENTITY</span><span class="sxs-lookup"><span data-stu-id="cf46b-727">DBPROP_STRONGITDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-728">Уникальные строки</span><span class="sxs-lookup"><span data-stu-id="cf46b-728">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="cf46b-729">DBPROP_UNIQUEROWS</span><span class="sxs-lookup"><span data-stu-id="cf46b-729">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-730">Возможности обновления</span><span class="sxs-lookup"><span data-stu-id="cf46b-730">Updatability</span></span></p></td>
<td><p><span data-ttu-id="cf46b-731">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="cf46b-731">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-732">Использование закладок</span><span class="sxs-lookup"><span data-stu-id="cf46b-732">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="cf46b-733">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="cf46b-733">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a><span data-ttu-id="cf46b-734">Динамические свойства команды</span><span class="sxs-lookup"><span data-stu-id="cf46b-734">Command Dynamic Properties</span></span>

<span data-ttu-id="cf46b-735">Следующие свойства добавляются в коллекцию **свойств** объекта **команды** .</span><span class="sxs-lookup"><span data-stu-id="cf46b-735">The following properties are added to the **Command** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cf46b-736">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="cf46b-736">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="cf46b-737">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="cf46b-737">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-738">Порядок доступа</span><span class="sxs-lookup"><span data-stu-id="cf46b-738">Access Order</span></span></p></td>
<td><p><span data-ttu-id="cf46b-739">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="cf46b-739">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-740">Блокировка объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="cf46b-740">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="cf46b-741">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="cf46b-741">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-742">Тип закладки</span><span class="sxs-lookup"><span data-stu-id="cf46b-742">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="cf46b-743">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="cf46b-743">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-744">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="cf46b-744">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="cf46b-745">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="cf46b-745">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-746">Изменение вставленных строк</span><span class="sxs-lookup"><span data-stu-id="cf46b-746">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="cf46b-747">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="cf46b-747">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-748">Права доступа столбца</span><span class="sxs-lookup"><span data-stu-id="cf46b-748">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="cf46b-749">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="cf46b-749">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-750">Столбец набор уведомлений</span><span class="sxs-lookup"><span data-stu-id="cf46b-750">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="cf46b-751">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="cf46b-751">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-752">Отложенное обновление объекта хранения</span><span class="sxs-lookup"><span data-stu-id="cf46b-752">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="cf46b-753">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="cf46b-753">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-754">Выборку</span><span class="sxs-lookup"><span data-stu-id="cf46b-754">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="cf46b-755">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="cf46b-755">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-756">Хранение строк</span><span class="sxs-lookup"><span data-stu-id="cf46b-756">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="cf46b-757">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="cf46b-757">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-758">IAccessor</span><span class="sxs-lookup"><span data-stu-id="cf46b-758">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="cf46b-759">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="cf46b-759">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-760">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="cf46b-760">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="cf46b-761">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="cf46b-761">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-762">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="cf46b-762">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="cf46b-763">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="cf46b-763">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-764">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="cf46b-764">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="cf46b-765">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="cf46b-765">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-766">IConvertType</span><span class="sxs-lookup"><span data-stu-id="cf46b-766">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="cf46b-767">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="cf46b-767">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-768">Немобильные строки</span><span class="sxs-lookup"><span data-stu-id="cf46b-768">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="cf46b-769">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="cf46b-769">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-770">IRowset</span><span class="sxs-lookup"><span data-stu-id="cf46b-770">IRowset</span></span></p></td>
<td><p><span data-ttu-id="cf46b-771">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="cf46b-771">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-772">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="cf46b-772">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="cf46b-773">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="cf46b-773">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-774">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="cf46b-774">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="cf46b-775">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="cf46b-775">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-776">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="cf46b-776">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="cf46b-777">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="cf46b-777">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-778">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="cf46b-778">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="cf46b-779">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="cf46b-779">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-780">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="cf46b-780">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-781">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="cf46b-781">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="cf46b-782">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="cf46b-782">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-783">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="cf46b-783">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="cf46b-784">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="cf46b-784">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-785">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="cf46b-785">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="cf46b-786">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="cf46b-786">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-787">Литерал закладки</span><span class="sxs-lookup"><span data-stu-id="cf46b-787">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="cf46b-788">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="cf46b-788">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-789">Удостоверение литерала строки</span><span class="sxs-lookup"><span data-stu-id="cf46b-789">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="cf46b-790">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="cf46b-790">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-791">Максимальное число открытых строк</span><span class="sxs-lookup"><span data-stu-id="cf46b-791">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="cf46b-792">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="cf46b-792">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-793">Максимум ожидающие строк</span><span class="sxs-lookup"><span data-stu-id="cf46b-793">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="cf46b-794">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="cf46b-794">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-795">Максимальное число строк</span><span class="sxs-lookup"><span data-stu-id="cf46b-795">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="cf46b-796">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="cf46b-796">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-797">Степень детализации уведомлений</span><span class="sxs-lookup"><span data-stu-id="cf46b-797">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="cf46b-798">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="cf46b-798">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-799">Этапы уведомлений</span><span class="sxs-lookup"><span data-stu-id="cf46b-799">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="cf46b-800">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="cf46b-800">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-801">Объекты в транзакции</span><span class="sxs-lookup"><span data-stu-id="cf46b-801">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="cf46b-802">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="cf46b-802">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-803">Видны собственные изменения</span><span class="sxs-lookup"><span data-stu-id="cf46b-803">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="cf46b-804">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="cf46b-804">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-805">Видны собственные операции вставки</span><span class="sxs-lookup"><span data-stu-id="cf46b-805">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="cf46b-806">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="cf46b-806">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-807">Сохранять при аварийном завершении</span><span class="sxs-lookup"><span data-stu-id="cf46b-807">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="cf46b-808">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="cf46b-808">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-809">Сохранять при фиксации</span><span class="sxs-lookup"><span data-stu-id="cf46b-809">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="cf46b-810">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="cf46b-810">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-811">Быстрый перезапуск</span><span class="sxs-lookup"><span data-stu-id="cf46b-811">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="cf46b-812">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="cf46b-812">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-813">Повторные события</span><span class="sxs-lookup"><span data-stu-id="cf46b-813">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="cf46b-814">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="cf46b-814">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-815">Удаление удаленных строк</span><span class="sxs-lookup"><span data-stu-id="cf46b-815">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="cf46b-816">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="cf46b-816">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-817">Сообщить о нескольких изменений</span><span class="sxs-lookup"><span data-stu-id="cf46b-817">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="cf46b-818">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="cf46b-818">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-819">Вернуть ожидающие вставки</span><span class="sxs-lookup"><span data-stu-id="cf46b-819">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="cf46b-820">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="cf46b-820">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-821">Удалить строку уведомлений</span><span class="sxs-lookup"><span data-stu-id="cf46b-821">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="cf46b-822">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="cf46b-822">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-823">Строка первого уведомления об изменении</span><span class="sxs-lookup"><span data-stu-id="cf46b-823">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="cf46b-824">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="cf46b-824">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-825">Строка вставки уведомлений</span><span class="sxs-lookup"><span data-stu-id="cf46b-825">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="cf46b-826">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="cf46b-826">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-827">Привилегии строки</span><span class="sxs-lookup"><span data-stu-id="cf46b-827">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="cf46b-828">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="cf46b-828">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-829">Уведомления о повторной синхронизации строки</span><span class="sxs-lookup"><span data-stu-id="cf46b-829">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="cf46b-830">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="cf46b-830">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-831">Строка, потоковой модели</span><span class="sxs-lookup"><span data-stu-id="cf46b-831">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="cf46b-832">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="cf46b-832">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-833">Уведомление об изменении отмены строки</span><span class="sxs-lookup"><span data-stu-id="cf46b-833">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="cf46b-834">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="cf46b-834">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-835">Строка отмены Delete уведомлений</span><span class="sxs-lookup"><span data-stu-id="cf46b-835">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="cf46b-836">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="cf46b-836">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-837">Вставка отмены строки уведомлений</span><span class="sxs-lookup"><span data-stu-id="cf46b-837">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="cf46b-838">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="cf46b-838">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-839">Уведомление об обновлении строки</span><span class="sxs-lookup"><span data-stu-id="cf46b-839">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="cf46b-840">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="cf46b-840">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-841">Уведомление об изменении положения строк выборки</span><span class="sxs-lookup"><span data-stu-id="cf46b-841">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="cf46b-842">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="cf46b-842">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-843">Уведомление о выпуске набора строк</span><span class="sxs-lookup"><span data-stu-id="cf46b-843">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="cf46b-844">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="cf46b-844">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-845">Прокрутка назад</span><span class="sxs-lookup"><span data-stu-id="cf46b-845">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="cf46b-846">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="cf46b-846">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-847">Пропустить удаленных закладки</span><span class="sxs-lookup"><span data-stu-id="cf46b-847">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="cf46b-848">DBPROP_BOOKMARKSKIP</span><span class="sxs-lookup"><span data-stu-id="cf46b-848">DBPROP_BOOKMARKSKIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-849">Строка строгого удостоверений</span><span class="sxs-lookup"><span data-stu-id="cf46b-849">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="cf46b-850">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="cf46b-850">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf46b-851">Возможности обновления</span><span class="sxs-lookup"><span data-stu-id="cf46b-851">Updatability</span></span></p></td>
<td><p><span data-ttu-id="cf46b-852">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="cf46b-852">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf46b-853">Использование закладок</span><span class="sxs-lookup"><span data-stu-id="cf46b-853">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="cf46b-854">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="cf46b-854">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="cf46b-855">См. также</span><span class="sxs-lookup"><span data-stu-id="cf46b-855">See also</span></span>

<span data-ttu-id="cf46b-856">Для получения дополнительных сведений о реализации и функциональным сведения о поставщик Microsoft OLE DB для ODBC обратитесь к [OLE DB Руководство программиста](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85)) или посетите [Центр разработчиков данных платформы](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).</span><span class="sxs-lookup"><span data-stu-id="cf46b-856">For details regarding specific implementation and functional information about the Microsoft OLE DB Provider for ODBC, consult the [OLE DB Programmer's Guide](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85)) or visit the [Data Platform Developer Center](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).</span></span>

