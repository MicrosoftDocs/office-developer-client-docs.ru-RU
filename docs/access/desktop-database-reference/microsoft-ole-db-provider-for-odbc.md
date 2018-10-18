---
title: Microsoft OLE DB Provider for ODBC
TOCTitle: Microsoft OLE DB Provider for ODBC
ms:assetid: c507567e-5ad1-b32a-f6ad-5ba2c39aa4c2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249964(v=office.15)
ms:contentKeyID: 48547602
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0098e646ea48656f44bd3ccd380ae41efc94ffba
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606943"
---
# <a name="microsoft-ole-db-provider-for-odbc"></a><span data-ttu-id="40f8f-102">Microsoft OLE DB Provider for ODBC</span><span class="sxs-lookup"><span data-stu-id="40f8f-102">Microsoft OLE DB Provider for ODBC</span></span>

<span data-ttu-id="40f8f-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="40f8f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="40f8f-104">Чтобы программист ADO или служб удаленных рабочих СТОЛОВ идеальном мире бы одно в каждом данных источника предоставляет интерфейс OLE DB, чтобы вызвать непосредственно в источник данных ADO.</span><span class="sxs-lookup"><span data-stu-id="40f8f-104">To an ADO or RDS programmer, an ideal world would be one in which every data source exposes an OLE DB interface, so that ADO could call directly into the data source.</span></span> <span data-ttu-id="40f8f-105">Несмотря на то, что все больше дополнительные базы данных поставщиков реализует интерфейсы OLE DB, некоторые источники данных не еще не представленных таким способом.</span><span class="sxs-lookup"><span data-stu-id="40f8f-105">Although increasingly more database vendors are implementing OLE DB interfaces, some data sources are not yet exposed this way.</span></span> <span data-ttu-id="40f8f-106">Тем не менее практически все СУБД в настоящее время может осуществляться через ODBC.</span><span class="sxs-lookup"><span data-stu-id="40f8f-106">However, virtually all DBMS systems in use today can be accessed through ODBC.</span></span>

<span data-ttu-id="40f8f-107">Драйверы ODBC доступны для всех основных СУБД, в настоящее время, включая Microsoft SQL Server, Microsoft Access (базы данных Microsoft Jet) и Microsoft FoxPro, кроме базы данных сторонних продуктов, таких как Oracle.</span><span class="sxs-lookup"><span data-stu-id="40f8f-107">ODBC drivers are available for every major DBMS in use today, including Microsoft SQL Server, Microsoft Access (Microsoft Jet database engine), and Microsoft FoxPro, in addition to non-Microsoft database products such as Oracle.</span></span>

<span data-ttu-id="40f8f-108">Поставщик ODBC Microsoft, однако позволяет ADO для подключения к источникам данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="40f8f-108">The Microsoft ODBC Provider, however, allows ADO to connect to any ODBC data source.</span></span> <span data-ttu-id="40f8f-109">Поставщик свободных потоков и Юникод.</span><span class="sxs-lookup"><span data-stu-id="40f8f-109">The provider is free-threaded and Unicode enabled.</span></span>

<span data-ttu-id="40f8f-110">Поставщик поддерживает транзакции, несмотря на то, что разные ядра СУБД предлагают различные виды поддержки транзакций.</span><span class="sxs-lookup"><span data-stu-id="40f8f-110">The provider supports transactions, although different DBMS engines offer different types of transaction support.</span></span> <span data-ttu-id="40f8f-111">Например Microsoft Access поддерживает до пяти уровней вложенных транзакций.</span><span class="sxs-lookup"><span data-stu-id="40f8f-111">For example, Microsoft Access supports nested transactions up to five levels deep.</span></span>

<span data-ttu-id="40f8f-112">Поставщик по умолчанию для ADO и поддерживаются все зависящие от поставщика ADO свойства и методы.</span><span class="sxs-lookup"><span data-stu-id="40f8f-112">This is the default provider for ADO, and all provider-dependent ADO properties and methods are supported.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="40f8f-113">Параметры строки подключения</span><span class="sxs-lookup"><span data-stu-id="40f8f-113">Connection String Parameters</span></span>

<span data-ttu-id="40f8f-114">Для подключения к данным поставщиком, задайте **поставщика =** аргумент свойства [ConnectionString](connectionstring-property-ado.md) для:</span><span class="sxs-lookup"><span data-stu-id="40f8f-114">To connect to this provider, set the **Provider=** argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```sql 
 
MSDASQL 
```

<span data-ttu-id="40f8f-115">Чтение свойства [поставщика](provider-property-ado.md) будет возвращать также этой строки.</span><span class="sxs-lookup"><span data-stu-id="40f8f-115">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="40f8f-116">Типичная строка подключения</span><span class="sxs-lookup"><span data-stu-id="40f8f-116">Typical Connection String</span></span>

<span data-ttu-id="40f8f-117">— Это строка соединения для данного поставщика:</span><span class="sxs-lookup"><span data-stu-id="40f8f-117">A typical connection string for this provider is:</span></span>

```sql 
 
"Provider=MSDASQL;DSN=dsnName;UID=userName;PWD=userPassword;" 
```

<span data-ttu-id="40f8f-118">Строка состоит из следующих ключевых слов:</span><span class="sxs-lookup"><span data-stu-id="40f8f-118">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="40f8f-119">Keyword</span><span class="sxs-lookup"><span data-stu-id="40f8f-119">Keyword</span></span></p></th>
<th><p><span data-ttu-id="40f8f-120">Описание</span><span class="sxs-lookup"><span data-stu-id="40f8f-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-121"><strong>Поставщик</strong></span><span class="sxs-lookup"><span data-stu-id="40f8f-121"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="40f8f-122">Задает поставщика OLE DB для ODBC.</span><span class="sxs-lookup"><span data-stu-id="40f8f-122">Specifies the OLE DB Provider for ODBC.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-123"><strong>УВЕДОМЛЕНИЯ О ДОСТАВКЕ</strong></span><span class="sxs-lookup"><span data-stu-id="40f8f-123"><strong>DSN</strong></span></span></p></td>
<td><p><span data-ttu-id="40f8f-124">Указывает имя источника данных.</span><span class="sxs-lookup"><span data-stu-id="40f8f-124">Specifies the data source name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-125"><strong>UID</strong></span><span class="sxs-lookup"><span data-stu-id="40f8f-125"><strong>UID</strong></span></span></p></td>
<td><p><span data-ttu-id="40f8f-126">Задает имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="40f8f-126">Specifies the user name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-127"><strong>PWD</strong></span><span class="sxs-lookup"><span data-stu-id="40f8f-127"><strong>PWD</strong></span></span></p></td>
<td><p><span data-ttu-id="40f8f-128">Задает пароль пользователя.</span><span class="sxs-lookup"><span data-stu-id="40f8f-128">Specifies the user password.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-129"><strong>URL</strong>.</span><span class="sxs-lookup"><span data-stu-id="40f8f-129"><strong>URL</strong></span></span></p></td>
<span data-ttu-id="40f8f-130"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="40f8f-130"><<<<<<< HEAD</span></span>
<td><p><span data-ttu-id="40f8f-131">Задает URL-адрес файла или папки, опубликованной в веб-папку.</span><span class="sxs-lookup"><span data-stu-id="40f8f-131">Specifies the URL of a file or directory published in a Web folder.</span></span></p></td>
=======
<td><p><span data-ttu-id="40f8f-132">Задает URL-адрес файла или папки, опубликованной в веб-папку.</span><span class="sxs-lookup"><span data-stu-id="40f8f-132">Specifies the URL of a file or directory published in a web folder.</span></span></p></td><span data-ttu-id="40f8f-133">
>>>>>>>Образец</span><span class="sxs-lookup"><span data-stu-id="40f8f-133">
>>>>>>> master</span></span>
</tr>
</tbody>
</table>


<span data-ttu-id="40f8f-134">Так как это поставщика по умолчанию для ADO, если опустить **поставщика =** параметра в строке подключения ADO пытается установить подключение к данным поставщиком.</span><span class="sxs-lookup"><span data-stu-id="40f8f-134">Because this is the default provider for ADO, if you omit the **Provider=** parameter from the connection string, ADO will attempt to establish a connection to this provider.</span></span>

<span data-ttu-id="40f8f-135">Поставщик не поддерживает параметры подключения в дополнение к определяемые ADO.</span><span class="sxs-lookup"><span data-stu-id="40f8f-135">The provider does not support any specific connection parameters in addition to those defined by ADO.</span></span> <span data-ttu-id="40f8f-136">Тем не менее Поставщик передает параметры соединения не ADO драйвера ODBC.</span><span class="sxs-lookup"><span data-stu-id="40f8f-136">However, the provider will pass any non-ADO connection parameters to the ODBC driver manager.</span></span>

<span data-ttu-id="40f8f-137">Так как можно опустить параметр **поставщика** , таким образом можно создать строку подключения ADO, идентичный строки подключения ODBC для одного источника данных.</span><span class="sxs-lookup"><span data-stu-id="40f8f-137">Because you can omit the **Provider** parameter, you can therefore compose an ADO connection string that is identical to an ODBC connection string for the same data source.</span></span> <span data-ttu-id="40f8f-138">Используйте одинаковые имена параметров (**ДРАЙВЕРА =**, **базы данных =**, **уведомления о Доставке =** и так далее), значения и синтаксис, как вы бы при создании строки подключения ODBC.</span><span class="sxs-lookup"><span data-stu-id="40f8f-138">Use the same parameter names (**DRIVER=**, **DATABASE=**, **DSN=**, and so on), values, and syntax as you would when composing an ODBC connection string.</span></span> <span data-ttu-id="40f8f-139">Можно подключить с и без имя источника данных (DSN) или FileDSN.</span><span class="sxs-lookup"><span data-stu-id="40f8f-139">You can connect with or without a predefined data source name (DSN) or FileDSN.</span></span>

<span data-ttu-id="40f8f-140">**Синтаксис с уведомления о Доставке или FileDSN:**</span><span class="sxs-lookup"><span data-stu-id="40f8f-140">**Syntax with a DSN or FileDSN:**</span></span>

`"[Provider=MSDASQL;] { DSN=name | FileDSN=filename } ; [DATABASE=database;] UID=user; PWD=password"`

<span data-ttu-id="40f8f-141">**Синтаксис без уведомления о Доставке (соединения):**</span><span class="sxs-lookup"><span data-stu-id="40f8f-141">**Syntax without a DSN (DSN-less connection):**</span></span>

`"[Provider=MSDASQL;] DRIVER=driver; SERVER=server;DATABASE=database; UID=user; PWD=password"`

<span data-ttu-id="40f8f-142">Если вы используете **уведомления о Доставке** или **FileDSN**, его необходимо определить через источники данных ODBC в панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="40f8f-142">If you use a **DSN** or **FileDSN**, it must be defined through the ODBC Data Source Administrator in the Windows Control Panel.</span></span> <span data-ttu-id="40f8f-143">В Microsoft Windows 2000 администратор ODBC находится в разделе Администрирование.</span><span class="sxs-lookup"><span data-stu-id="40f8f-143">In Microsoft Windows 2000, the ODBC Administrator is located under Administrative Tools.</span></span> <span data-ttu-id="40f8f-144">В предыдущих версиях Windows значок администратор ODBC называется **32-разрядная версия ODBC** или просто **ODBC**.</span><span class="sxs-lookup"><span data-stu-id="40f8f-144">In previous versions of Windows, the ODBC Administrator icon is named **32-bit ODBC** or simply **ODBC**.</span></span>

<span data-ttu-id="40f8f-145">В качестве альтернативы для установки **уведомления о Доставке**, можно указать драйвер ODBC (**ДРАЙВЕРА =**), например «SQL Server»; имя сервера (**SERVER =**); и имя базы данных (**базы данных =**).</span><span class="sxs-lookup"><span data-stu-id="40f8f-145">As an alternative to setting a **DSN**, you can specify the ODBC driver (**DRIVER=**), such as "SQL Server;" the server name (**SERVER=**); and the database name (**DATABASE=**).</span></span>

<span data-ttu-id="40f8f-146">Также можно указать имя учетной записи пользователя (**UID =**) и пароль для учетной записи пользователя (**PWD =**) в параметры, относящиеся к ODBC или в стандартный определенные ADO *пользователя* и *пароль* параметры.</span><span class="sxs-lookup"><span data-stu-id="40f8f-146">You can also specify a user account name (**UID=**), and the password for the user account (**PWD=**) in the ODBC-specific parameters or in the standard ADO-defined *user* and *password* parameters.</span></span>

<span data-ttu-id="40f8f-147">Хотя **уведомления о Доставке** определение уже указывает базу данных, можно задать *параметр *базы данных* , в дополнение к **уведомления о Доставке** для подключения в другую базу данных* .</span><span class="sxs-lookup"><span data-stu-id="40f8f-147">Although a **DSN** definition already specifies a database, you can specify *a* *database* parameter in addition to a **DSN** to connect to a different database.</span></span> <span data-ttu-id="40f8f-148">Рекомендуется всегда включать \*параметр *базы данных* \* при использовании **уведомления о Доставке**.</span><span class="sxs-lookup"><span data-stu-id="40f8f-148">It is a good idea to always include *the* *database* parameter when you use a **DSN**.</span></span> <span data-ttu-id="40f8f-149">Это обеспечит подключиться к базе соответствующих прав в случае, когда другой пользователь изменить параметр базы данных по умолчанию с момента последнего извлечения определения **уведомления о Доставке** .</span><span class="sxs-lookup"><span data-stu-id="40f8f-149">This will ensure that you connect to the proper database in the event that another user changed the default database parameter since you last checked the **DSN** definition.</span></span>

## <a name="provider-specific-connection-properties"></a><span data-ttu-id="40f8f-150">Свойства подключения от поставщика</span><span class="sxs-lookup"><span data-stu-id="40f8f-150">Provider-Specific Connection Properties</span></span>

<span data-ttu-id="40f8f-151">Поставщик OLE DB для ODBC добавляет несколько свойств в коллекцию [свойств](properties-collection-ado.md) объекта **подключения** .</span><span class="sxs-lookup"><span data-stu-id="40f8f-151">The OLE DB provider for ODBC adds several properties to the [Properties](properties-collection-ado.md) collection of the **Connection** object.</span></span> <span data-ttu-id="40f8f-152">В следующей таблице перечислены эти свойства имя соответствующего свойства OLE DB в скобки.</span><span class="sxs-lookup"><span data-stu-id="40f8f-152">The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="40f8f-153">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="40f8f-153">Property Name</span></span></p></th>
<th><p><span data-ttu-id="40f8f-154">Описание</span><span class="sxs-lookup"><span data-stu-id="40f8f-154">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-155">Доступны процедуры</span><span class="sxs-lookup"><span data-stu-id="40f8f-155">Accessible Procedures</span></span><br />
<span data-ttu-id="40f8f-156">(KAGPROP_ACCESSIBLEPROCEDURES)</span><span class="sxs-lookup"><span data-stu-id="40f8f-156">(KAGPROP_ACCESSIBLEPROCEDURES)</span></span></p></td>
<td><p><span data-ttu-id="40f8f-157">Указывает, является ли пользователь имеет доступ к хранимые процедуры.</span><span class="sxs-lookup"><span data-stu-id="40f8f-157">Indicates whether the user has access to stored procedures.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-158">Доступно таблиц</span><span class="sxs-lookup"><span data-stu-id="40f8f-158">Accessible Tables</span></span><br />
<span data-ttu-id="40f8f-159">(KAGPROP_ACCESSIBLETABLES)</span><span class="sxs-lookup"><span data-stu-id="40f8f-159">(KAGPROP_ACCESSIBLETABLES)</span></span></p></td>
<td><p><span data-ttu-id="40f8f-160">Указывает, является ли пользователь имеет разрешения на выполнение инструкций SELECT таблиц базы данных.</span><span class="sxs-lookup"><span data-stu-id="40f8f-160">Indicates whether the user has permission to execute SELECT statements against the database tables.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-161">Активные операторы</span><span class="sxs-lookup"><span data-stu-id="40f8f-161">Active Statements</span></span><br />
<span data-ttu-id="40f8f-162">(KAGPROP_ACTIVESTATEMENTS)</span><span class="sxs-lookup"><span data-stu-id="40f8f-162">(KAGPROP_ACTIVESTATEMENTS)</span></span></p></td>
<td><p><span data-ttu-id="40f8f-163">Указывает число дескрипторов, которые может поддерживать драйвера ODBC для подключения.</span><span class="sxs-lookup"><span data-stu-id="40f8f-163">Indicates the number of handles an ODBC driver can support on a connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-164">Имя драйвера</span><span class="sxs-lookup"><span data-stu-id="40f8f-164">Driver Name</span></span><br />
<span data-ttu-id="40f8f-165">(KAGPROP_DRIVERNAME)</span><span class="sxs-lookup"><span data-stu-id="40f8f-165">(KAGPROP_DRIVERNAME)</span></span></p></td>
<td><p><span data-ttu-id="40f8f-166">Указывает имя файла драйвера ODBC.</span><span class="sxs-lookup"><span data-stu-id="40f8f-166">Indicates the file name of the ODBC driver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-167">Версия драйвера ODBC</span><span class="sxs-lookup"><span data-stu-id="40f8f-167">Driver ODBC Version</span></span><br />
<span data-ttu-id="40f8f-168">(KAGPROP_DRIVERODBCVER)</span><span class="sxs-lookup"><span data-stu-id="40f8f-168">(KAGPROP_DRIVERODBCVER)</span></span></p></td>
<td><p><span data-ttu-id="40f8f-169">Указывает версию, поддерживающего этот драйвер ODBC.</span><span class="sxs-lookup"><span data-stu-id="40f8f-169">Indicates the version of ODBC that this driver supports.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-170">Использование файлов</span><span class="sxs-lookup"><span data-stu-id="40f8f-170">File Usage</span></span><br />
<span data-ttu-id="40f8f-171">(KAGPROP_FILEUSAGE)</span><span class="sxs-lookup"><span data-stu-id="40f8f-171">(KAGPROP_FILEUSAGE)</span></span></p></td>
<td><p><span data-ttu-id="40f8f-172">Указывает, как драйвер обрабатывает файл источника данных. как таблицы или как к каталогу.</span><span class="sxs-lookup"><span data-stu-id="40f8f-172">Indicates how the driver treats a file in a data source; as a table or as a catalog.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-173">Как предложение escape-последовательности</span><span class="sxs-lookup"><span data-stu-id="40f8f-173">Like Escape Clause</span></span><br />
<span data-ttu-id="40f8f-174">(KAGPROP_LIKEESCAPECLAUSE)</span><span class="sxs-lookup"><span data-stu-id="40f8f-174">(KAGPROP_LIKEESCAPECLAUSE)</span></span></p></td>
<td><p><span data-ttu-id="40f8f-175">Указывает предикат LIKE предложение WHERE ли драйвер поддерживается в определение и использование escape-символ знаком процента (%) и символ подчеркивания (_).</span><span class="sxs-lookup"><span data-stu-id="40f8f-175">Indicates whether the driver supports the definition and use of an escape character for the percent character (%) and underline character (_) in the LIKE predicate of a WHERE clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-176">Максимальное число столбцов в группировать по</span><span class="sxs-lookup"><span data-stu-id="40f8f-176">Max Columns in Group By</span></span><br />
<span data-ttu-id="40f8f-177">(KAGPROP_MAXCOLUMNSINGROUPBY)</span><span class="sxs-lookup"><span data-stu-id="40f8f-177">(KAGPROP_MAXCOLUMNSINGROUPBY)</span></span></p></td>
<td><p><span data-ttu-id="40f8f-178">Указывает максимальное число столбцов, которые могут быть перечислены в предложении GROUP BY инструкции SELECT.</span><span class="sxs-lookup"><span data-stu-id="40f8f-178">Indicates the maximum number of columns that can be listed in the GROUP BY clause of a SELECT statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-179">Максимальное число столбцов в индексе</span><span class="sxs-lookup"><span data-stu-id="40f8f-179">Max Columns in Index</span></span><br />
<span data-ttu-id="40f8f-180">(KAGPROP_MAXCOLUMNSININDEX)</span><span class="sxs-lookup"><span data-stu-id="40f8f-180">(KAGPROP_MAXCOLUMNSININDEX)</span></span></p></td>
<td><p><span data-ttu-id="40f8f-181">Указывает максимальное число столбцов, которые можно включить в индекс.</span><span class="sxs-lookup"><span data-stu-id="40f8f-181">Indicates the maximum number of columns that can be included in an index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-182">Максимальное число столбцов в порядке</span><span class="sxs-lookup"><span data-stu-id="40f8f-182">Max Columns in Order By</span></span><br />
<span data-ttu-id="40f8f-183">(KAGPROP_MAXCOLUMNSINORDERBY)</span><span class="sxs-lookup"><span data-stu-id="40f8f-183">(KAGPROP_MAXCOLUMNSINORDERBY)</span></span></p></td>
<td><p><span data-ttu-id="40f8f-184">Указывает максимальное число столбцов, которые могут быть перечислены в предложение ORDER BY инструкции SELECT.</span><span class="sxs-lookup"><span data-stu-id="40f8f-184">Indicates the maximum number of columns that can be listed in the ORDER BY clause of a SELECT statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-185">Максимальное число столбцов в Выбор</span><span class="sxs-lookup"><span data-stu-id="40f8f-185">Max Columns in Select</span></span><br />
<span data-ttu-id="40f8f-186">(KAGPROP_MAXCOLUMNSINSELECT)</span><span class="sxs-lookup"><span data-stu-id="40f8f-186">(KAGPROP_MAXCOLUMNSINSELECT)</span></span></p></td>
<td><p><span data-ttu-id="40f8f-187">Указывает максимальное число столбцов, которые могут быть перечислены в разделе SELECT инструкции SELECT.</span><span class="sxs-lookup"><span data-stu-id="40f8f-187">Indicates the maximum number of columns that can be listed in the SELECT portion of a SELECT statement.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-188">Максимальное число столбцов в таблице</span><span class="sxs-lookup"><span data-stu-id="40f8f-188">Max Columns in Table</span></span><br />
<span data-ttu-id="40f8f-189">(KAGPROP_MAXCOLUMNSINTABLE)</span><span class="sxs-lookup"><span data-stu-id="40f8f-189">(KAGPROP_MAXCOLUMNSINTABLE)</span></span></p></td>
<td><p><span data-ttu-id="40f8f-190">Указывает максимальное число столбцов в таблице.</span><span class="sxs-lookup"><span data-stu-id="40f8f-190">Indicates the maximum number of columns allowed in a table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-191">Числовые функции</span><span class="sxs-lookup"><span data-stu-id="40f8f-191">Numeric Functions</span></span><br />
<span data-ttu-id="40f8f-192">(KAGPROP_NUMERICFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="40f8f-192">(KAGPROP_NUMERICFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="40f8f-193">Указывает, какие числовые функции поддерживаются драйвер ODBC.</span><span class="sxs-lookup"><span data-stu-id="40f8f-193">Indicates which numeric functions are supported by the ODBC driver.</span></span> <span data-ttu-id="40f8f-194">Список имен функций и связанные значения, используемые в этом Битовая маска, см в приложении д: скалярные в документации по ODBC.</span><span class="sxs-lookup"><span data-stu-id="40f8f-194">For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-195">Возможности внешнего соединения</span><span class="sxs-lookup"><span data-stu-id="40f8f-195">Outer Join Capabilities</span></span><br />
<span data-ttu-id="40f8f-196">(KAGPROP_OJCAPABILITY)</span><span class="sxs-lookup"><span data-stu-id="40f8f-196">(KAGPROP_OJCAPABILITY)</span></span></p></td>
<td><p><span data-ttu-id="40f8f-197">Указывает типы ВНЕШНИЕ соединения, поддерживаемых поставщиком.</span><span class="sxs-lookup"><span data-stu-id="40f8f-197">Indicates the types of OUTER JOINs supported by the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-198">Внешние соединения</span><span class="sxs-lookup"><span data-stu-id="40f8f-198">Outer Joins</span></span><br />
<span data-ttu-id="40f8f-199">(KAGPROP_OUTERJOINS)</span><span class="sxs-lookup"><span data-stu-id="40f8f-199">(KAGPROP_OUTERJOINS)</span></span></p></td>
<td><p><span data-ttu-id="40f8f-200">Указывает, является ли поставщик поддерживает ВНЕШНИЕ соединения.</span><span class="sxs-lookup"><span data-stu-id="40f8f-200">Indicates whether the provider supports OUTER JOINs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-201">Специальные символы</span><span class="sxs-lookup"><span data-stu-id="40f8f-201">Special Characters</span></span><br />
<span data-ttu-id="40f8f-202">(KAGPROP_SPECIALCHARACTERS)</span><span class="sxs-lookup"><span data-stu-id="40f8f-202">(KAGPROP_SPECIALCHARACTERS)</span></span></p></td>
<td><p><span data-ttu-id="40f8f-203">Указывает, какие символы имеет особое значение для драйвера ODBC.</span><span class="sxs-lookup"><span data-stu-id="40f8f-203">Indicates which characters have special meaning for the ODBC driver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-204">Хранимые процедуры</span><span class="sxs-lookup"><span data-stu-id="40f8f-204">Stored Procedures</span></span><br />
<span data-ttu-id="40f8f-205">(KAGPROP_PROCEDURES)</span><span class="sxs-lookup"><span data-stu-id="40f8f-205">(KAGPROP_PROCEDURES)</span></span></p></td>
<td><p><span data-ttu-id="40f8f-206">Указывает, доступны ли хранимые процедуры для использования с этой драйвер ODBC.</span><span class="sxs-lookup"><span data-stu-id="40f8f-206">Indicates whether stored procedures are available for use with this ODBC driver.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-207">Строковые функции</span><span class="sxs-lookup"><span data-stu-id="40f8f-207">String Functions</span></span><br />
<span data-ttu-id="40f8f-208">(KAGPROP_STRINGFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="40f8f-208">(KAGPROP_STRINGFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="40f8f-209">Указывает, какие функции string, поддерживаются драйвер ODBC.</span><span class="sxs-lookup"><span data-stu-id="40f8f-209">Indicates which string functions are supported by the ODBC driver.</span></span> <span data-ttu-id="40f8f-210">Список имен функций и связанные значения, используемые в этом Битовая маска, см в приложении д: скалярные в документации по ODBC.</span><span class="sxs-lookup"><span data-stu-id="40f8f-210">For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-211">Системные функции</span><span class="sxs-lookup"><span data-stu-id="40f8f-211">System Functions</span></span><br />
<span data-ttu-id="40f8f-212">(KAGPROP_SYSTEMFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="40f8f-212">(KAGPROP_SYSTEMFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="40f8f-213">Указывает, какие функции системы поддерживаются драйвер ODBC.</span><span class="sxs-lookup"><span data-stu-id="40f8f-213">Indicates which system functions are supported by the ODBC driver.</span></span> <span data-ttu-id="40f8f-214">Список имен функций и связанные значения, используемые в этом Битовая маска, см в приложении д: скалярные в документации по ODBC.</span><span class="sxs-lookup"><span data-stu-id="40f8f-214">For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-215">Время и Дата функции</span><span class="sxs-lookup"><span data-stu-id="40f8f-215">Time/Date Functions</span></span><br />
<span data-ttu-id="40f8f-216">(KAGPROP_TIMEDATEFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="40f8f-216">(KAGPROP_TIMEDATEFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="40f8f-217">Указывает, какие функции даты и времени поддерживаются драйвер ODBC.</span><span class="sxs-lookup"><span data-stu-id="40f8f-217">Indicates which time and date functions are supported by the ODBC driver.</span></span> <span data-ttu-id="40f8f-218">Список имен функций и связанные значения, используемые в этом Битовая маска, см в приложении д: скалярные в документации по ODBC.</span><span class="sxs-lookup"><span data-stu-id="40f8f-218">For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-219">Поддержка грамматики SQL</span><span class="sxs-lookup"><span data-stu-id="40f8f-219">SQL Grammar Support</span></span><br />
<span data-ttu-id="40f8f-220">(KAGPROP_ODBCSQLCONFORMANCE)</span><span class="sxs-lookup"><span data-stu-id="40f8f-220">(KAGPROP_ODBCSQLCONFORMANCE)</span></span></p></td>
<td><p><span data-ttu-id="40f8f-221">Указывает грамматику SQL, которая поддерживает драйвер ODBC.</span><span class="sxs-lookup"><span data-stu-id="40f8f-221">Indicates the SQL grammar that the ODBC driver supports.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-recordset-and-command-properties"></a><span data-ttu-id="40f8f-222">Свойства команды и записей от поставщика</span><span class="sxs-lookup"><span data-stu-id="40f8f-222">Provider-Specific Recordset and Command Properties</span></span>

<span data-ttu-id="40f8f-223">Поставщик OLE DB для ODBC добавляет несколько свойств **Свойства** набора **записей** и **командных** объектов.</span><span class="sxs-lookup"><span data-stu-id="40f8f-223">The OLE DB provider for ODBC adds several properties to the **Properties** collection of the **Recordset** and **Command** objects.</span></span> <span data-ttu-id="40f8f-224">В следующей таблице перечислены эти свойства имя соответствующего свойства OLE DB в скобки.</span><span class="sxs-lookup"><span data-stu-id="40f8f-224">The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="40f8f-225">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="40f8f-225">Property Name</span></span></p></th>
<th><p><span data-ttu-id="40f8f-226">Описание</span><span class="sxs-lookup"><span data-stu-id="40f8f-226">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-227">Запрос на основе обновления, удаления или вставки</span><span class="sxs-lookup"><span data-stu-id="40f8f-227">Query Based Updates/Deletes/Inserts</span></span><br />
<span data-ttu-id="40f8f-228">(KAGPROP_QUERYBASEDUPDATES)</span><span class="sxs-lookup"><span data-stu-id="40f8f-228">(KAGPROP_QUERYBASEDUPDATES)</span></span></p></td>
<td><p><span data-ttu-id="40f8f-229">Указывает, будет ли обновления, удаления и вставки можно выполнить с помощью SQL-запросов.</span><span class="sxs-lookup"><span data-stu-id="40f8f-229">Indicates whether updates, deletions, and insertions can be performed using SQL queries.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-230">Тип параллельного ODBC</span><span class="sxs-lookup"><span data-stu-id="40f8f-230">ODBC Concurrency Type</span></span><br />
<span data-ttu-id="40f8f-231">(KAGPROP_CONCURRENCY)</span><span class="sxs-lookup"><span data-stu-id="40f8f-231">(KAGPROP_CONCURRENCY)</span></span></p></td>
<td><p><span data-ttu-id="40f8f-232">Метод, используемый для уменьшения потенциальных проблем, вызванных двух пользователей одновременно к той же информации из источника данных.</span><span class="sxs-lookup"><span data-stu-id="40f8f-232">Indicates the method used to reduce potential problems caused by two users attempting to access the same data from the data source simultaneously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-233">Специальные возможности больших двоичных ОБЪЕКТОВ на последовательный курсор</span><span class="sxs-lookup"><span data-stu-id="40f8f-233">BLOB accessibility on Forward-Only cursor</span></span><br />
<span data-ttu-id="40f8f-234">(KAGPROP_BLOBSONFOCURSOR)</span><span class="sxs-lookup"><span data-stu-id="40f8f-234">(KAGPROP_BLOBSONFOCURSOR)</span></span></p></td>
<td><p><span data-ttu-id="40f8f-235">Указывает, будет ли при использовании последовательный курсор возможен больших двоичных ОБЪЕКТОВ <strong>полей</strong> .</span><span class="sxs-lookup"><span data-stu-id="40f8f-235">Indicates whether BLOB <strong>Fields</strong> can be accessed when using a forward-only cursor.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-236">Включить в предложения QBU WHERE SQL_FLOAT, SQL_DOUBLE и SQL_REAL</span><span class="sxs-lookup"><span data-stu-id="40f8f-236">Include SQL_FLOAT, SQL_DOUBLE, and SQL_REAL in QBU WHERE clauses</span></span><br />
<span data-ttu-id="40f8f-237">(KAGPROP_INCLUDENONEXACT)</span><span class="sxs-lookup"><span data-stu-id="40f8f-237">(KAGPROP_INCLUDENONEXACT)</span></span></p></td>
<td><p><span data-ttu-id="40f8f-238">Указывает, будет ли значения SQL_FLOAT, SQL_DOUBLE и SQL_REAL может быть включен в предложении QBU WHERE.</span><span class="sxs-lookup"><span data-stu-id="40f8f-238">Indicates whether SQL_FLOAT, SQL_DOUBLE, and SQL_REAL values can be included in a QBU WHERE clause.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-239">Положение в последней строке после вставки</span><span class="sxs-lookup"><span data-stu-id="40f8f-239">Position on the last row after insert</span></span><br />
<span data-ttu-id="40f8f-240">(KAGPROP_POSITIONONNEWROW)</span><span class="sxs-lookup"><span data-stu-id="40f8f-240">(KAGPROP_POSITIONONNEWROW)</span></span></p></td>
<td><p><span data-ttu-id="40f8f-241">Указывает, что после вставки новой записи в таблице последней строки в таблице должны быть поступают текущей строки.</span><span class="sxs-lookup"><span data-stu-id="40f8f-241">Indicates that after a new record has been inserted in a table, the last row in the table will be come the current row.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-242">IRowsetChangeExtInfo</span><span class="sxs-lookup"><span data-stu-id="40f8f-242">IRowsetChangeExtInfo</span></span><br />
<span data-ttu-id="40f8f-243">(KAGPROP_IROWSETCHANGEEXTINFO)</span><span class="sxs-lookup"><span data-stu-id="40f8f-243">(KAGPROP_IROWSETCHANGEEXTINFO)</span></span></p></td>
<td><p><span data-ttu-id="40f8f-244">Указывает, будет ли интерфейс <strong>IRowsetChange</strong> поддерживает расширенные сведения.</span><span class="sxs-lookup"><span data-stu-id="40f8f-244">Indicates whether the <strong>IRowsetChange</strong> interface provides extended information support.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-245">Тип курсора ODBC</span><span class="sxs-lookup"><span data-stu-id="40f8f-245">ODBC Cursor Type</span></span><br />
<span data-ttu-id="40f8f-246">(KAGPROP_CURSOR)</span><span class="sxs-lookup"><span data-stu-id="40f8f-246">(KAGPROP_CURSOR)</span></span></p></td>
<td><p><span data-ttu-id="40f8f-247">Указывает тип курсора, используемого <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="40f8f-247">Indicates the type of cursor used by the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-248">Создать набор строк, который может быть упакован</span><span class="sxs-lookup"><span data-stu-id="40f8f-248">Generate a Rowset that can be marshaled</span></span><br />
<span data-ttu-id="40f8f-249">(KAGPROP_MARSHALLABLE)</span><span class="sxs-lookup"><span data-stu-id="40f8f-249">(KAGPROP_MARSHALLABLE)</span></span></p></td>
<td><p><span data-ttu-id="40f8f-250">Указывает, что драйвер ODBC создает набор записей, который может быть упакован</span><span class="sxs-lookup"><span data-stu-id="40f8f-250">Indicates that the ODBC driver generates a recordset that can be marshaled</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-text"></a><span data-ttu-id="40f8f-251">Текст команды</span><span class="sxs-lookup"><span data-stu-id="40f8f-251">Command Text</span></span>

<span data-ttu-id="40f8f-252">Как использовать объект [команды](command-object-ado.md) во многом зависит от источника данных и какой тип оператора запроса или команды будет принимать.</span><span class="sxs-lookup"><span data-stu-id="40f8f-252">How you use the [Command](command-object-ado.md) object largely depends on the data source, and what type of query or command statement it will accept.</span></span>

<span data-ttu-id="40f8f-253">ODBC предоставляет определенный синтаксис для вызова хранимых процедур.</span><span class="sxs-lookup"><span data-stu-id="40f8f-253">ODBC provides a specific syntax for calling stored procedures.</span></span> <span data-ttu-id="40f8f-254">Для свойства [CommandText](commandtext-property-ado.md) объекта **команды** *CommandText* аргумента метода **Execute** на объект [подключения](connection-object-ado.md) и *исходный* аргумент методу **Open** на [набора записей](recordset-object-ado.md) объект передает в строку с помощью следующего синтаксиса:</span><span class="sxs-lookup"><span data-stu-id="40f8f-254">For the [CommandText](commandtext-property-ado.md) property of a **Command** object, the *CommandText* argument to the **Execute** method on a [Connection](connection-object-ado.md) object, or the *Source* argument to the **Open** method on a [Recordset](recordset-object-ado.md) object, passes in a string with this syntax:</span></span>

`"{ [ ? = ] call procedure [ ( ? [, ? [ ,  ]] ) ] }"`

<span data-ttu-id="40f8f-255">Каждый **?**</span><span class="sxs-lookup"><span data-stu-id="40f8f-255">Each **?**</span></span> <span data-ttu-id="40f8f-256">содержит ссылку на объект в коллекции [параметров](parameters-collection-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="40f8f-256">references an object in the [Parameters](parameters-collection-ado.md) collection.</span></span> <span data-ttu-id="40f8f-257">Первый **?**</span><span class="sxs-lookup"><span data-stu-id="40f8f-257">The first **?**</span></span> <span data-ttu-id="40f8f-258">ссылки на **Параметры**(0), Далее **?**</span><span class="sxs-lookup"><span data-stu-id="40f8f-258">references **Parameters**(0), the next **?**</span></span> <span data-ttu-id="40f8f-259">Создание ссылки **Параметры**(1) и т. д.</span><span class="sxs-lookup"><span data-stu-id="40f8f-259">references **Parameters**(1), and so on.</span></span>

<span data-ttu-id="40f8f-260">Параметр ссылки являются необязательными и зависят от структуры хранимую процедуру.</span><span class="sxs-lookup"><span data-stu-id="40f8f-260">The parameter references are optional and depend on the structure of the stored procedure.</span></span> <span data-ttu-id="40f8f-261">Если вы хотите вызвать хранимую процедуру, определяющий без параметров, строка будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="40f8f-261">If you want to call a stored procedure that defines no parameters, your string would look like this:</span></span>

`"{ call procedure }"`

<span data-ttu-id="40f8f-262">Если у вас есть два параметра запроса, строка будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="40f8f-262">If you have two query parameters, your string would look like this:</span></span>

`"{ call procedure ( ?, ? ) }"`

<span data-ttu-id="40f8f-263">Если хранимая процедура возвращает значение, возвращаемое значение обрабатывается как еще один параметр.</span><span class="sxs-lookup"><span data-stu-id="40f8f-263">If the stored procedure will return a value, the return value is treated as another parameter.</span></span> <span data-ttu-id="40f8f-264">Если у вас нет параметров запроса, но возвращаемое значение, строка будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="40f8f-264">If you have no query parameters but you do have a return value, your string would look like this:</span></span>

`"{ ? = call procedure }"`

<span data-ttu-id="40f8f-265">И, наконец Если у вас есть возвращаемое значение и два параметра запроса, строка будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="40f8f-265">Finally, if you have a return value and two query parameters, your string would look like this:</span></span>

`"{ ? = call procedure ( ?, ? ) }"`

## <a name="recordset-behavior"></a><span data-ttu-id="40f8f-266">Поведение набора записей</span><span class="sxs-lookup"><span data-stu-id="40f8f-266">Recordset Behavior</span></span>

<span data-ttu-id="40f8f-267">В следующих таблицах перечислены стандартные ADO методы и свойства, доступные для объекта **набора записей** , открытых с этим поставщиком.</span><span class="sxs-lookup"><span data-stu-id="40f8f-267">The following tables list the standard ADO methods and properties available on a **Recordset** object opened with this provider.</span></span>

<span data-ttu-id="40f8f-268">Для получения дополнительных сведений о поведении **набора записей** для вашей конфигурации поставщика, выполните метод [поддерживает](supports-method-ado.md) и перечисления коллекции **свойств** **набора записей** для определения целесообразности поставщиком динамических свойства отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="40f8f-268">For more detailed information about **Recordset** behavior for your provider configuration, run the [Supports](supports-method-ado.md) method and enumerate the **Properties** collection of the **Recordset** to determine whether provider-specific dynamic properties are present.</span></span>

<span data-ttu-id="40f8f-269">Доступность стандартными свойствами ADO **набора записей** :</span><span class="sxs-lookup"><span data-stu-id="40f8f-269">Availability of standard ADO **Recordset** properties:</span></span>

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
<th><p><span data-ttu-id="40f8f-270">Свойство</span><span class="sxs-lookup"><span data-stu-id="40f8f-270">Property</span></span></p></th>
<th><p><span data-ttu-id="40f8f-271">ForwardOnly</span><span class="sxs-lookup"><span data-stu-id="40f8f-271">ForwardOnly</span></span></p></th>
<th><p><span data-ttu-id="40f8f-272">Динамическая группа</span><span class="sxs-lookup"><span data-stu-id="40f8f-272">Dynamic</span></span></p></th>
<th><p><span data-ttu-id="40f8f-273">Набор ключей</span><span class="sxs-lookup"><span data-stu-id="40f8f-273">Keyset</span></span></p></th>
<th><p><span data-ttu-id="40f8f-274">Статическое</span><span class="sxs-lookup"><span data-stu-id="40f8f-274">Static</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-275"><a href="absolutepage-property-ado.md">AbsolutePage</a></span><span class="sxs-lookup"><span data-stu-id="40f8f-275"><a href="absolutepage-property-ado.md">AbsolutePage</a></span></span></p></td>
<td><p><span data-ttu-id="40f8f-276">Недоступен</span><span class="sxs-lookup"><span data-stu-id="40f8f-276">not available</span></span></p></td>
<td><p><span data-ttu-id="40f8f-277">Недоступен</span><span class="sxs-lookup"><span data-stu-id="40f8f-277">not available</span></span></p></td>
<td><p><span data-ttu-id="40f8f-278">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40f8f-278">read/write</span></span></p></td>
<td><p><span data-ttu-id="40f8f-279">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40f8f-279">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-280"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span><span class="sxs-lookup"><span data-stu-id="40f8f-280"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span></span></p></td>
<td><p><span data-ttu-id="40f8f-281">Недоступен</span><span class="sxs-lookup"><span data-stu-id="40f8f-281">not available</span></span></p></td>
<td><p><span data-ttu-id="40f8f-282">Недоступен</span><span class="sxs-lookup"><span data-stu-id="40f8f-282">not available</span></span></p></td>
<td><p><span data-ttu-id="40f8f-283">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40f8f-283">read/write</span></span></p></td>
<td><p><span data-ttu-id="40f8f-284">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40f8f-284">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-285"><a href="activeconnection-property-ado.md">ActiveConnection</a></span><span class="sxs-lookup"><span data-stu-id="40f8f-285"><a href="activeconnection-property-ado.md">ActiveConnection</a></span></span></p></td>
<td><p><span data-ttu-id="40f8f-286">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40f8f-286">read/write</span></span></p></td>
<td><p><span data-ttu-id="40f8f-287">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40f8f-287">read/write</span></span></p></td>
<td><p><span data-ttu-id="40f8f-288">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40f8f-288">read/write</span></span></p></td>
<td><p><span data-ttu-id="40f8f-289">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40f8f-289">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-290"><a href="bof-eof-properties-ado.md">BOF</a></span><span class="sxs-lookup"><span data-stu-id="40f8f-290"><a href="bof-eof-properties-ado.md">BOF</a></span></span></p></td>
<td><p><span data-ttu-id="40f8f-291">только для чтения</span><span class="sxs-lookup"><span data-stu-id="40f8f-291">read-only</span></span></p></td>
<td><p><span data-ttu-id="40f8f-292">только для чтения</span><span class="sxs-lookup"><span data-stu-id="40f8f-292">read-only</span></span></p></td>
<td><p><span data-ttu-id="40f8f-293">только для чтения</span><span class="sxs-lookup"><span data-stu-id="40f8f-293">read-only</span></span></p></td>
<td><p><span data-ttu-id="40f8f-294">только для чтения</span><span class="sxs-lookup"><span data-stu-id="40f8f-294">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-295"><a href="bookmark-property-ado.md">Закладка</a></span><span class="sxs-lookup"><span data-stu-id="40f8f-295"><a href="bookmark-property-ado.md">Bookmark</a></span></span></p></td>
<td><p><span data-ttu-id="40f8f-296">Недоступен</span><span class="sxs-lookup"><span data-stu-id="40f8f-296">not available</span></span></p></td>
<td><p><span data-ttu-id="40f8f-297">Недоступен</span><span class="sxs-lookup"><span data-stu-id="40f8f-297">not available</span></span></p></td>
<td><p><span data-ttu-id="40f8f-298">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40f8f-298">read/write</span></span></p></td>
<td><p><span data-ttu-id="40f8f-299">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40f8f-299">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-300"><a href="cachesize-property-ado.md">CacheSize</a></span><span class="sxs-lookup"><span data-stu-id="40f8f-300"><a href="cachesize-property-ado.md">CacheSize</a></span></span></p></td>
<td><p><span data-ttu-id="40f8f-301">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40f8f-301">read/write</span></span></p></td>
<td><p><span data-ttu-id="40f8f-302">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40f8f-302">read/write</span></span></p></td>
<td><p><span data-ttu-id="40f8f-303">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40f8f-303">read/write</span></span></p></td>
<td><p><span data-ttu-id="40f8f-304">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40f8f-304">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-305"><a href="cursorlocation-property-ado.md">CursorLocation</a></span><span class="sxs-lookup"><span data-stu-id="40f8f-305"><a href="cursorlocation-property-ado.md">CursorLocation</a></span></span></p></td>
<td><p><span data-ttu-id="40f8f-306">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40f8f-306">read/write</span></span></p></td>
<td><p><span data-ttu-id="40f8f-307">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40f8f-307">read/write</span></span></p></td>
<td><p><span data-ttu-id="40f8f-308">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40f8f-308">read/write</span></span></p></td>
<td><p><span data-ttu-id="40f8f-309">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40f8f-309">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-310"><a href="cursortype-property-ado.md">CursorType</a></span><span class="sxs-lookup"><span data-stu-id="40f8f-310"><a href="cursortype-property-ado.md">CursorType</a></span></span></p></td>
<td><p><span data-ttu-id="40f8f-311">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40f8f-311">read/write</span></span></p></td>
<td><p><span data-ttu-id="40f8f-312">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40f8f-312">read/write</span></span></p></td>
<td><p><span data-ttu-id="40f8f-313">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40f8f-313">read/write</span></span></p></td>
<td><p><span data-ttu-id="40f8f-314">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40f8f-314">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-315"><a href="editmode-property-ado.md">EditMode</a></span><span class="sxs-lookup"><span data-stu-id="40f8f-315"><a href="editmode-property-ado.md">EditMode</a></span></span></p></td>
<td><p><span data-ttu-id="40f8f-316">только для чтения</span><span class="sxs-lookup"><span data-stu-id="40f8f-316">read-only</span></span></p></td>
<td><p><span data-ttu-id="40f8f-317">только для чтения</span><span class="sxs-lookup"><span data-stu-id="40f8f-317">read-only</span></span></p></td>
<td><p><span data-ttu-id="40f8f-318">только для чтения</span><span class="sxs-lookup"><span data-stu-id="40f8f-318">read-only</span></span></p></td>
<td><p><span data-ttu-id="40f8f-319">только для чтения</span><span class="sxs-lookup"><span data-stu-id="40f8f-319">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-320"><a href="filter-property-ado.md">Filter</a></span><span class="sxs-lookup"><span data-stu-id="40f8f-320"><a href="filter-property-ado.md">Filter</a></span></span></p></td>
<td><p><span data-ttu-id="40f8f-321">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40f8f-321">read/write</span></span></p></td>
<td><p><span data-ttu-id="40f8f-322">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40f8f-322">read/write</span></span></p></td>
<td><p><span data-ttu-id="40f8f-323">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40f8f-323">read/write</span></span></p></td>
<td><p><span data-ttu-id="40f8f-324">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40f8f-324">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-325"><a href="locktype-property-ado.md">LockType для</a></span><span class="sxs-lookup"><span data-stu-id="40f8f-325"><a href="locktype-property-ado.md">LockType</a></span></span></p></td>
<td><p><span data-ttu-id="40f8f-326">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40f8f-326">read/write</span></span></p></td>
<td><p><span data-ttu-id="40f8f-327">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40f8f-327">read/write</span></span></p></td>
<td><p><span data-ttu-id="40f8f-328">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40f8f-328">read/write</span></span></p></td>
<td><p><span data-ttu-id="40f8f-329">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40f8f-329">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-330"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span><span class="sxs-lookup"><span data-stu-id="40f8f-330"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span></span></p></td>
<td><p><span data-ttu-id="40f8f-331">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40f8f-331">read/write</span></span></p></td>
<td><p><span data-ttu-id="40f8f-332">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40f8f-332">read/write</span></span></p></td>
<td><p><span data-ttu-id="40f8f-333">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40f8f-333">read/write</span></span></p></td>
<td><p><span data-ttu-id="40f8f-334">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40f8f-334">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-335"><a href="maxrecords-property-ado.md">MaxRecords</a></span><span class="sxs-lookup"><span data-stu-id="40f8f-335"><a href="maxrecords-property-ado.md">MaxRecords</a></span></span></p></td>
<td><p><span data-ttu-id="40f8f-336">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40f8f-336">read/write</span></span></p></td>
<td><p><span data-ttu-id="40f8f-337">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40f8f-337">read/write</span></span></p></td>
<td><p><span data-ttu-id="40f8f-338">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40f8f-338">read/write</span></span></p></td>
<td><p><span data-ttu-id="40f8f-339">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40f8f-339">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-340"><a href="pagecount-property-ado.md">PageCount</a></span><span class="sxs-lookup"><span data-stu-id="40f8f-340"><a href="pagecount-property-ado.md">PageCount</a></span></span></p></td>
<td><p><span data-ttu-id="40f8f-341">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40f8f-341">read/write</span></span></p></td>
<td><p><span data-ttu-id="40f8f-342">Недоступен</span><span class="sxs-lookup"><span data-stu-id="40f8f-342">not available</span></span></p></td>
<td><p><span data-ttu-id="40f8f-343">только для чтения</span><span class="sxs-lookup"><span data-stu-id="40f8f-343">read-only</span></span></p></td>
<td><p><span data-ttu-id="40f8f-344">только для чтения</span><span class="sxs-lookup"><span data-stu-id="40f8f-344">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-345"><a href="pagesize-property-ado.md">PageSize</a></span><span class="sxs-lookup"><span data-stu-id="40f8f-345"><a href="pagesize-property-ado.md">PageSize</a></span></span></p></td>
<td><p><span data-ttu-id="40f8f-346">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40f8f-346">read/write</span></span></p></td>
<td><p><span data-ttu-id="40f8f-347">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40f8f-347">read/write</span></span></p></td>
<td><p><span data-ttu-id="40f8f-348">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40f8f-348">read/write</span></span></p></td>
<td><p><span data-ttu-id="40f8f-349">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40f8f-349">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-350"><a href="recordcount-property-ado.md">RecordCount</a></span><span class="sxs-lookup"><span data-stu-id="40f8f-350"><a href="recordcount-property-ado.md">RecordCount</a></span></span></p></td>
<td><p><span data-ttu-id="40f8f-351">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40f8f-351">read/write</span></span></p></td>
<td><p><span data-ttu-id="40f8f-352">Недоступен</span><span class="sxs-lookup"><span data-stu-id="40f8f-352">not available</span></span></p></td>
<td><p><span data-ttu-id="40f8f-353">только для чтения</span><span class="sxs-lookup"><span data-stu-id="40f8f-353">read-only</span></span></p></td>
<td><p><span data-ttu-id="40f8f-354">только для чтения</span><span class="sxs-lookup"><span data-stu-id="40f8f-354">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-355"><a href="source-property-ado-recordset.md">Source</a></span><span class="sxs-lookup"><span data-stu-id="40f8f-355"><a href="source-property-ado-recordset.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="40f8f-356">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40f8f-356">read/write</span></span></p></td>
<td><p><span data-ttu-id="40f8f-357">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40f8f-357">read/write</span></span></p></td>
<td><p><span data-ttu-id="40f8f-358">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40f8f-358">read/write</span></span></p></td>
<td><p><span data-ttu-id="40f8f-359">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40f8f-359">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-360"><a href="state-property-ado.md">State</a></span><span class="sxs-lookup"><span data-stu-id="40f8f-360"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="40f8f-361">только для чтения</span><span class="sxs-lookup"><span data-stu-id="40f8f-361">read-only</span></span></p></td>
<td><p><span data-ttu-id="40f8f-362">только для чтения</span><span class="sxs-lookup"><span data-stu-id="40f8f-362">read-only</span></span></p></td>
<td><p><span data-ttu-id="40f8f-363">только для чтения</span><span class="sxs-lookup"><span data-stu-id="40f8f-363">read-only</span></span></p></td>
<td><p><span data-ttu-id="40f8f-364">только для чтения</span><span class="sxs-lookup"><span data-stu-id="40f8f-364">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-365"><a href="status-property-ado-recordset.md">Состояние</a></span><span class="sxs-lookup"><span data-stu-id="40f8f-365"><a href="status-property-ado-recordset.md">Status</a></span></span></p></td>
<td><p><span data-ttu-id="40f8f-366">только для чтения</span><span class="sxs-lookup"><span data-stu-id="40f8f-366">read-only</span></span></p></td>
<td><p><span data-ttu-id="40f8f-367">только для чтения</span><span class="sxs-lookup"><span data-stu-id="40f8f-367">read-only</span></span></p></td>
<td><p><span data-ttu-id="40f8f-368">только для чтения</span><span class="sxs-lookup"><span data-stu-id="40f8f-368">read-only</span></span></p></td>
<td><p><span data-ttu-id="40f8f-369">только для чтения</span><span class="sxs-lookup"><span data-stu-id="40f8f-369">read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="40f8f-370">Свойства [AbsolutePosition](absoluteposition-property-ado.md) и [AbsolutePage](absolutepage-property-ado.md) доступны только для записи при использовании ADO с версии 1.0 поставщик Microsoft OLE DB для ODBC.</span><span class="sxs-lookup"><span data-stu-id="40f8f-370">The [AbsolutePosition](absoluteposition-property-ado.md) and [AbsolutePage](absolutepage-property-ado.md) properties are write-only when ADO is used with version 1.0 of the Microsoft OLE DB Provider for ODBC.</span></span>

<span data-ttu-id="40f8f-371">Доступность стандартных способов ADO **набора записей** :</span><span class="sxs-lookup"><span data-stu-id="40f8f-371">Availability of standard ADO **Recordset** methods:</span></span>

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
<th><p><span data-ttu-id="40f8f-372">Метод</span><span class="sxs-lookup"><span data-stu-id="40f8f-372">Method</span></span></p></th>
<th><p><span data-ttu-id="40f8f-373">ForwardOnly</span><span class="sxs-lookup"><span data-stu-id="40f8f-373">ForwardOnly</span></span></p></th>
<th><p><span data-ttu-id="40f8f-374">Динамическая группа</span><span class="sxs-lookup"><span data-stu-id="40f8f-374">Dynamic</span></span></p></th>
<th><p><span data-ttu-id="40f8f-375">Набор ключей</span><span class="sxs-lookup"><span data-stu-id="40f8f-375">Keyset</span></span></p></th>
<th><p><span data-ttu-id="40f8f-376">Статическое</span><span class="sxs-lookup"><span data-stu-id="40f8f-376">Static</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-377"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="40f8f-377"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="40f8f-378">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-378">Yes</span></span></p></td>
<td><p><span data-ttu-id="40f8f-379">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-379">Yes</span></span></p></td>
<td><p><span data-ttu-id="40f8f-380">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-380">Yes</span></span></p></td>
<td><p><span data-ttu-id="40f8f-381">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-381">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-382"><a href="cancel-method-ado.md">Отмена</a></span><span class="sxs-lookup"><span data-stu-id="40f8f-382"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="40f8f-383">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-383">Yes</span></span></p></td>
<td><p><span data-ttu-id="40f8f-384">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-384">Yes</span></span></p></td>
<td><p><span data-ttu-id="40f8f-385">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-385">Yes</span></span></p></td>
<td><p><span data-ttu-id="40f8f-386">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-386">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-387"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="40f8f-387"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="40f8f-388">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-388">Yes</span></span></p></td>
<td><p><span data-ttu-id="40f8f-389">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-389">Yes</span></span></p></td>
<td><p><span data-ttu-id="40f8f-390">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-390">Yes</span></span></p></td>
<td><p><span data-ttu-id="40f8f-391">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-391">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-392"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="40f8f-392"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="40f8f-393">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-393">Yes</span></span></p></td>
<td><p><span data-ttu-id="40f8f-394">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-394">Yes</span></span></p></td>
<td><p><span data-ttu-id="40f8f-395">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-395">Yes</span></span></p></td>
<td><p><span data-ttu-id="40f8f-396">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-396">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-397"><a href="clone-method-ado.md">Копия</a></span><span class="sxs-lookup"><span data-stu-id="40f8f-397"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="40f8f-398">Нет</span><span class="sxs-lookup"><span data-stu-id="40f8f-398">No</span></span></p></td>
<td><p><span data-ttu-id="40f8f-399">Нет</span><span class="sxs-lookup"><span data-stu-id="40f8f-399">No</span></span></p></td>
<td><p><span data-ttu-id="40f8f-400">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-400">Yes</span></span></p></td>
<td><p><span data-ttu-id="40f8f-401">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-401">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-402"><a href="close-method-ado.md">Закрыть</a></span><span class="sxs-lookup"><span data-stu-id="40f8f-402"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="40f8f-403">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-403">Yes</span></span></p></td>
<td><p><span data-ttu-id="40f8f-404">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-404">Yes</span></span></p></td>
<td><p><span data-ttu-id="40f8f-405">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-405">Yes</span></span></p></td>
<td><p><span data-ttu-id="40f8f-406">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-406">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-407"><a href="delete-method-ado-recordset.md">Delete</a></span><span class="sxs-lookup"><span data-stu-id="40f8f-407"><a href="delete-method-ado-recordset.md">Delete</a></span></span></p></td>
<td><p><span data-ttu-id="40f8f-408">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-408">Yes</span></span></p></td>
<td><p><span data-ttu-id="40f8f-409">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-409">Yes</span></span></p></td>
<td><p><span data-ttu-id="40f8f-410">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-410">Yes</span></span></p></td>
<td><p><span data-ttu-id="40f8f-411">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-411">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-412"><a href="getrows-method-ado.md">Получение строк</a></span><span class="sxs-lookup"><span data-stu-id="40f8f-412"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="40f8f-413">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-413">Yes</span></span></p></td>
<td><p><span data-ttu-id="40f8f-414">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-414">Yes</span></span></p></td>
<td><p><span data-ttu-id="40f8f-415">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-415">Yes</span></span></p></td>
<td><p><span data-ttu-id="40f8f-416">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-416">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-417"><a href="move-method-ado.md">Перемещение</a></span><span class="sxs-lookup"><span data-stu-id="40f8f-417"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="40f8f-418">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-418">Yes</span></span></p></td>
<td><p><span data-ttu-id="40f8f-419">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-419">Yes</span></span></p></td>
<td><p><span data-ttu-id="40f8f-420">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-420">Yes</span></span></p></td>
<td><p><span data-ttu-id="40f8f-421">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-421">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-422"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span><span class="sxs-lookup"><span data-stu-id="40f8f-422"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span></span></p></td>
<td><p><span data-ttu-id="40f8f-423">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-423">Yes</span></span></p></td>
<td><p><span data-ttu-id="40f8f-424">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-424">Yes</span></span></p></td>
<td><p><span data-ttu-id="40f8f-425">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-425">Yes</span></span></p></td>
<td><p><span data-ttu-id="40f8f-426">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-426">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-427"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span><span class="sxs-lookup"><span data-stu-id="40f8f-427"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span></span></p></td>
<td><p><span data-ttu-id="40f8f-428">Нет</span><span class="sxs-lookup"><span data-stu-id="40f8f-428">No</span></span></p></td>
<td><p><span data-ttu-id="40f8f-429">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-429">Yes</span></span></p></td>
<td><p><span data-ttu-id="40f8f-430">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-430">Yes</span></span></p></td>
<td><p><span data-ttu-id="40f8f-431">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-431">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-432"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span><span class="sxs-lookup"><span data-stu-id="40f8f-432"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span></span></p></td>
<td><p><span data-ttu-id="40f8f-433">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-433">Yes</span></span></p></td>
<td><p><span data-ttu-id="40f8f-434">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-434">Yes</span></span></p></td>
<td><p><span data-ttu-id="40f8f-435">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-435">Yes</span></span></p></td>
<td><p><span data-ttu-id="40f8f-436">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-436">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-437"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span><span class="sxs-lookup"><span data-stu-id="40f8f-437"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span></span></p></td>
<td><p><span data-ttu-id="40f8f-438">Нет</span><span class="sxs-lookup"><span data-stu-id="40f8f-438">No</span></span></p></td>
<td><p><span data-ttu-id="40f8f-439">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-439">Yes</span></span></p></td>
<td><p><span data-ttu-id="40f8f-440">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-440">Yes</span></span></p></td>
<td><p><span data-ttu-id="40f8f-441">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-441">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-442"><a href="nextrecordset-method-ado.md">NextRecordset</a>\*</span><span class="sxs-lookup"><span data-stu-id="40f8f-442"><a href="nextrecordset-method-ado.md">NextRecordset</a>\*</span></span></p></td>
<td><p><span data-ttu-id="40f8f-443">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-443">Yes</span></span></p></td>
<td><p><span data-ttu-id="40f8f-444">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-444">Yes</span></span></p></td>
<td><p><span data-ttu-id="40f8f-445">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-445">Yes</span></span></p></td>
<td><p><span data-ttu-id="40f8f-446">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-446">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-447"><a href="open-method-ado-recordset.md">Открытие</a></span><span class="sxs-lookup"><span data-stu-id="40f8f-447"><a href="open-method-ado-recordset.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="40f8f-448">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-448">Yes</span></span></p></td>
<td><p><span data-ttu-id="40f8f-449">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-449">Yes</span></span></p></td>
<td><p><span data-ttu-id="40f8f-450">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-450">Yes</span></span></p></td>
<td><p><span data-ttu-id="40f8f-451">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-451">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-452"><a href="requery-method-ado.md">Обновление</a></span><span class="sxs-lookup"><span data-stu-id="40f8f-452"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="40f8f-453">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-453">Yes</span></span></p></td>
<td><p><span data-ttu-id="40f8f-454">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-454">Yes</span></span></p></td>
<td><p><span data-ttu-id="40f8f-455">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-455">Yes</span></span></p></td>
<td><p><span data-ttu-id="40f8f-456">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-456">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-457"><a href="resync-method-ado.md">Выполнить повторную синхронизацию</a></span><span class="sxs-lookup"><span data-stu-id="40f8f-457"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="40f8f-458">Нет</span><span class="sxs-lookup"><span data-stu-id="40f8f-458">No</span></span></p></td>
<td><p><span data-ttu-id="40f8f-459">Нет</span><span class="sxs-lookup"><span data-stu-id="40f8f-459">No</span></span></p></td>
<td><p><span data-ttu-id="40f8f-460">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-460">Yes</span></span></p></td>
<td><p><span data-ttu-id="40f8f-461">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-461">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-462"><a href="supports-method-ado.md">Поддерживает</a></span><span class="sxs-lookup"><span data-stu-id="40f8f-462"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="40f8f-463">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-463">Yes</span></span></p></td>
<td><p><span data-ttu-id="40f8f-464">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-464">Yes</span></span></p></td>
<td><p><span data-ttu-id="40f8f-465">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-465">Yes</span></span></p></td>
<td><p><span data-ttu-id="40f8f-466">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-466">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-467"><a href="update-method-ado.md">обновление</a>.</span><span class="sxs-lookup"><span data-stu-id="40f8f-467"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="40f8f-468">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-468">Yes</span></span></p></td>
<td><p><span data-ttu-id="40f8f-469">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-469">Yes</span></span></p></td>
<td><p><span data-ttu-id="40f8f-470">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-470">Yes</span></span></p></td>
<td><p><span data-ttu-id="40f8f-471">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-471">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-472"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="40f8f-472"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="40f8f-473">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-473">Yes</span></span></p></td>
<td><p><span data-ttu-id="40f8f-474">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-474">Yes</span></span></p></td>
<td><p><span data-ttu-id="40f8f-475">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-475">Yes</span></span></p></td>
<td><p><span data-ttu-id="40f8f-476">Да</span><span class="sxs-lookup"><span data-stu-id="40f8f-476">Yes</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="40f8f-477">\*Не поддерживается для баз данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="40f8f-477">\*Not supported for Microsoft Access databases.</span></span>

## <a name="dynamic-properties"></a><span data-ttu-id="40f8f-478">Динамические свойства</span><span class="sxs-lookup"><span data-stu-id="40f8f-478">Dynamic Properties</span></span>

<span data-ttu-id="40f8f-479">Поставщик Microsoft OLE DB для ODBC вставляет несколько динамических свойств в коллекцию **свойств** объектов неоткрытый [подключения](connection-object-ado.md), [записей](recordset-object-ado.md)и [команды](command-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="40f8f-479">The Microsoft OLE DB Provider for ODBC inserts several dynamic properties into the **Properties** collection of the unopened [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md), and [Command](command-object-ado.md) objects.</span></span>

<span data-ttu-id="40f8f-480">В таблицах ниже — это cross-index имен ADO и OLE DB для каждого динамического свойства.</span><span class="sxs-lookup"><span data-stu-id="40f8f-480">The tables below are a cross-index of the ADO and OLE DB names for each dynamic property.</span></span> <span data-ttu-id="40f8f-481">Справочник программиста OLE DB указано имя свойства ADO по слову «Описание».</span><span class="sxs-lookup"><span data-stu-id="40f8f-481">The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description."</span></span> <span data-ttu-id="40f8f-482">Дополнительные сведения об этих свойств можно найти в Справочник программиста OLE DB.</span><span class="sxs-lookup"><span data-stu-id="40f8f-482">You can find more information about these properties in the OLE DB Programmer's Reference.</span></span> <span data-ttu-id="40f8f-483">Поиск имени свойства OLE DB в индексе или просмотреть приложение C: OLE DB свойства.</span><span class="sxs-lookup"><span data-stu-id="40f8f-483">Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span></span>

## <a name="connection-dynamic-properties"></a><span data-ttu-id="40f8f-484">Динамические свойства подключения</span><span class="sxs-lookup"><span data-stu-id="40f8f-484">Connection Dynamic Properties</span></span>

<span data-ttu-id="40f8f-485">Коллекция **Properties** объект **подключения** добавляются следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="40f8f-485">The following properties are added to the **Connection** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="40f8f-486">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="40f8f-486">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="40f8f-487">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="40f8f-487">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-488">Активных сеансов</span><span class="sxs-lookup"><span data-stu-id="40f8f-488">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="40f8f-489">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="40f8f-489">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-490">Прерывание Asynchable</span><span class="sxs-lookup"><span data-stu-id="40f8f-490">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="40f8f-491">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="40f8f-491">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-492">Зафиксировать Asynchable</span><span class="sxs-lookup"><span data-stu-id="40f8f-492">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="40f8f-493">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="40f8f-493">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-494">Уровни изоляции автоматической фиксации</span><span class="sxs-lookup"><span data-stu-id="40f8f-494">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="40f8f-495">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="40f8f-495">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-496">Расположение каталога</span><span class="sxs-lookup"><span data-stu-id="40f8f-496">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="40f8f-497">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="40f8f-497">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-498">Каталог терминов</span><span class="sxs-lookup"><span data-stu-id="40f8f-498">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="40f8f-499">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="40f8f-499">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-500">Определение столбца</span><span class="sxs-lookup"><span data-stu-id="40f8f-500">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="40f8f-501">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="40f8f-501">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-502">Время ожидания подключения</span><span class="sxs-lookup"><span data-stu-id="40f8f-502">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="40f8f-503">DBPROP_INIT_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="40f8f-503">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-504">Текущий каталог</span><span class="sxs-lookup"><span data-stu-id="40f8f-504">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="40f8f-505">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="40f8f-505">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-506">Источник данных</span><span class="sxs-lookup"><span data-stu-id="40f8f-506">Data Source</span></span></p></td>
<td><p><span data-ttu-id="40f8f-507">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="40f8f-507">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-508">Имя источника данных</span><span class="sxs-lookup"><span data-stu-id="40f8f-508">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="40f8f-509">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="40f8f-509">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-510">Модель потоков объекта источника данных</span><span class="sxs-lookup"><span data-stu-id="40f8f-510">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="40f8f-511">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="40f8f-511">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-512">Имя СУБД</span><span class="sxs-lookup"><span data-stu-id="40f8f-512">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="40f8f-513">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="40f8f-513">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-514">Версия СУБД</span><span class="sxs-lookup"><span data-stu-id="40f8f-514">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="40f8f-515">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="40f8f-515">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-516">Расширенные свойства</span><span class="sxs-lookup"><span data-stu-id="40f8f-516">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="40f8f-517">DBPROP_INIT_PROVIDERSTRING</span><span class="sxs-lookup"><span data-stu-id="40f8f-517">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-518">ГРУППИРОВКА по поддержке</span><span class="sxs-lookup"><span data-stu-id="40f8f-518">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="40f8f-519">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="40f8f-519">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-520">Поддержка разнородных таблиц</span><span class="sxs-lookup"><span data-stu-id="40f8f-520">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="40f8f-521">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="40f8f-521">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-522">Идентификатор регистра</span><span class="sxs-lookup"><span data-stu-id="40f8f-522">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="40f8f-523">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="40f8f-523">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-524">Исходный каталог</span><span class="sxs-lookup"><span data-stu-id="40f8f-524">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="40f8f-525">DBPROP_INIT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="40f8f-525">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-526">Уровни изоляции</span><span class="sxs-lookup"><span data-stu-id="40f8f-526">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="40f8f-527">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="40f8f-527">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-528">Хранение изоляции</span><span class="sxs-lookup"><span data-stu-id="40f8f-528">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="40f8f-529">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="40f8f-529">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-530">Идентификатор языка</span><span class="sxs-lookup"><span data-stu-id="40f8f-530">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="40f8f-531">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="40f8f-531">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-532">Location</span><span class="sxs-lookup"><span data-stu-id="40f8f-532">Location</span></span></p></td>
<td><p><span data-ttu-id="40f8f-533">DBPROP_INIT_LOCATION</span><span class="sxs-lookup"><span data-stu-id="40f8f-533">DBPROP_INIT_LOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-534">Максимальный размер индекса</span><span class="sxs-lookup"><span data-stu-id="40f8f-534">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="40f8f-535">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="40f8f-535">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-536">Максимальный размер строки</span><span class="sxs-lookup"><span data-stu-id="40f8f-536">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="40f8f-537">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="40f8f-537">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-538">Максимальный размер строки включает в себя больших двоичных ОБЪЕКТОВ</span><span class="sxs-lookup"><span data-stu-id="40f8f-538">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="40f8f-539">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="40f8f-539">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-540">Максимальная таблиц в Выбор</span><span class="sxs-lookup"><span data-stu-id="40f8f-540">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="40f8f-541">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="40f8f-541">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-542">Mode</span><span class="sxs-lookup"><span data-stu-id="40f8f-542">Mode</span></span></p></td>
<td><p><span data-ttu-id="40f8f-543">DBPROP_INIT_MODE</span><span class="sxs-lookup"><span data-stu-id="40f8f-543">DBPROP_INIT_MODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-544">Несколько наборов параметров</span><span class="sxs-lookup"><span data-stu-id="40f8f-544">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="40f8f-545">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="40f8f-545">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-546">Несколько результатов</span><span class="sxs-lookup"><span data-stu-id="40f8f-546">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="40f8f-547">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="40f8f-547">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-548">Несколько объектов хранения</span><span class="sxs-lookup"><span data-stu-id="40f8f-548">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="40f8f-549">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="40f8f-549">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-550">Обновление нескольких таблицы</span><span class="sxs-lookup"><span data-stu-id="40f8f-550">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="40f8f-551">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="40f8f-551">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-552">Порядок сортировки значений NULL</span><span class="sxs-lookup"><span data-stu-id="40f8f-552">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="40f8f-553">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="40f8f-553">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-554">Поведение NULL объединения</span><span class="sxs-lookup"><span data-stu-id="40f8f-554">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="40f8f-555">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="40f8f-555">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-556">Службы OLE DB</span><span class="sxs-lookup"><span data-stu-id="40f8f-556">OLE DB Services</span></span></p></td>
<td><p><span data-ttu-id="40f8f-557">DBPROP_INIT_OLEDBSERVICES, УСТАНОВИТЬ</span><span class="sxs-lookup"><span data-stu-id="40f8f-557">DBPROP_INIT_OLEDBSERVICES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-558">Версия OLE DB</span><span class="sxs-lookup"><span data-stu-id="40f8f-558">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="40f8f-559">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="40f8f-559">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-560">Поддержка OLE-объектов</span><span class="sxs-lookup"><span data-stu-id="40f8f-560">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="40f8f-561">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="40f8f-561">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-562">Поддержка открытых наборов строк</span><span class="sxs-lookup"><span data-stu-id="40f8f-562">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="40f8f-563">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="40f8f-563">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-564">ORDER BY столбцы в списке Select</span><span class="sxs-lookup"><span data-stu-id="40f8f-564">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="40f8f-565">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="40f8f-565">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-566">Выходной параметр доступности</span><span class="sxs-lookup"><span data-stu-id="40f8f-566">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="40f8f-567">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="40f8f-567">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-568">Пароль</span><span class="sxs-lookup"><span data-stu-id="40f8f-568">Password</span></span></p></td>
<td><p><span data-ttu-id="40f8f-569">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="40f8f-569">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-570">Передайте с указанные методы</span><span class="sxs-lookup"><span data-stu-id="40f8f-570">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="40f8f-571">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="40f8f-571">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-572">Сохранять сведения о безопасности</span><span class="sxs-lookup"><span data-stu-id="40f8f-572">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="40f8f-573">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span><span class="sxs-lookup"><span data-stu-id="40f8f-573">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-574">Тип сохраняемого идентификатора</span><span class="sxs-lookup"><span data-stu-id="40f8f-574">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="40f8f-575">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="40f8f-575">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-576">Подготовка поведение аварийное завершение</span><span class="sxs-lookup"><span data-stu-id="40f8f-576">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="40f8f-577">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="40f8f-577">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-578">Подготовка поведение выделения</span><span class="sxs-lookup"><span data-stu-id="40f8f-578">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="40f8f-579">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="40f8f-579">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-580">Процедура терминов</span><span class="sxs-lookup"><span data-stu-id="40f8f-580">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="40f8f-581">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="40f8f-581">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-582">Запрос</span><span class="sxs-lookup"><span data-stu-id="40f8f-582">Prompt</span></span></p></td>
<td><p><span data-ttu-id="40f8f-583">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="40f8f-583">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-584">Понятное имя поставщика</span><span class="sxs-lookup"><span data-stu-id="40f8f-584">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="40f8f-585">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="40f8f-585">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-586">Имя поставщика</span><span class="sxs-lookup"><span data-stu-id="40f8f-586">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="40f8f-587">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="40f8f-587">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-588">Версия поставщика</span><span class="sxs-lookup"><span data-stu-id="40f8f-588">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="40f8f-589">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="40f8f-589">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-590">Источник данных только для чтения</span><span class="sxs-lookup"><span data-stu-id="40f8f-590">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="40f8f-591">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="40f8f-591">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-592">Преобразование строк на команду</span><span class="sxs-lookup"><span data-stu-id="40f8f-592">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="40f8f-593">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="40f8f-593">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-594">Схема терминов</span><span class="sxs-lookup"><span data-stu-id="40f8f-594">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="40f8f-595">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="40f8f-595">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-596">Об использовании схемы</span><span class="sxs-lookup"><span data-stu-id="40f8f-596">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="40f8f-597">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="40f8f-597">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-598">Поддержка SQL</span><span class="sxs-lookup"><span data-stu-id="40f8f-598">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="40f8f-599">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="40f8f-599">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-600">Структурированное хранилище</span><span class="sxs-lookup"><span data-stu-id="40f8f-600">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="40f8f-601">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="40f8f-601">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-602">Поддержка вложенного запроса</span><span class="sxs-lookup"><span data-stu-id="40f8f-602">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="40f8f-603">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="40f8f-603">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-604">В таблице терминов</span><span class="sxs-lookup"><span data-stu-id="40f8f-604">Table Term</span></span></p></td>
<td><p><span data-ttu-id="40f8f-605">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="40f8f-605">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-606">Транзакций DDL</span><span class="sxs-lookup"><span data-stu-id="40f8f-606">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="40f8f-607">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="40f8f-607">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-608">Идентификатор пользователя</span><span class="sxs-lookup"><span data-stu-id="40f8f-608">User ID</span></span></p></td>
<td><p><span data-ttu-id="40f8f-609">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="40f8f-609">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-610">Имя пользователя</span><span class="sxs-lookup"><span data-stu-id="40f8f-610">User Name</span></span></p></td>
<td><p><span data-ttu-id="40f8f-611">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="40f8f-611">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-612">Дескриптор окна</span><span class="sxs-lookup"><span data-stu-id="40f8f-612">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="40f8f-613">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="40f8f-613">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a><span data-ttu-id="40f8f-614">Свойства динамической набора записей</span><span class="sxs-lookup"><span data-stu-id="40f8f-614">Recordset Dynamic Properties</span></span>

<span data-ttu-id="40f8f-615">Следующие свойства добавляются в коллекцию **свойств** объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="40f8f-615">The following properties are added to the **Recordset** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="40f8f-616">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="40f8f-616">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="40f8f-617">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="40f8f-617">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-618">Порядок доступа</span><span class="sxs-lookup"><span data-stu-id="40f8f-618">Access Order</span></span></p></td>
<td><p><span data-ttu-id="40f8f-619">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="40f8f-619">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-620">Блокировка объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="40f8f-620">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="40f8f-621">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="40f8f-621">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-622">Тип закладки</span><span class="sxs-lookup"><span data-stu-id="40f8f-622">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="40f8f-623">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="40f8f-623">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-624">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="40f8f-624">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="40f8f-625">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="40f8f-625">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-626">Изменение вставленных строк</span><span class="sxs-lookup"><span data-stu-id="40f8f-626">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="40f8f-627">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="40f8f-627">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-628">Права доступа столбца</span><span class="sxs-lookup"><span data-stu-id="40f8f-628">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="40f8f-629">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="40f8f-629">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-630">Столбец набор уведомлений</span><span class="sxs-lookup"><span data-stu-id="40f8f-630">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="40f8f-631">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="40f8f-631">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-632">Отложенное обновление объекта хранения</span><span class="sxs-lookup"><span data-stu-id="40f8f-632">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="40f8f-633">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="40f8f-633">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-634">Выборку</span><span class="sxs-lookup"><span data-stu-id="40f8f-634">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="40f8f-635">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="40f8f-635">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-636">Хранение строк</span><span class="sxs-lookup"><span data-stu-id="40f8f-636">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="40f8f-637">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="40f8f-637">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-638">IAccessor</span><span class="sxs-lookup"><span data-stu-id="40f8f-638">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="40f8f-639">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="40f8f-639">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-640">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="40f8f-640">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="40f8f-641">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="40f8f-641">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-642">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="40f8f-642">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="40f8f-643">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="40f8f-643">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-644">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="40f8f-644">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="40f8f-645">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="40f8f-645">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-646">IConvertType</span><span class="sxs-lookup"><span data-stu-id="40f8f-646">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="40f8f-647">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="40f8f-647">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-648">Немобильные строки</span><span class="sxs-lookup"><span data-stu-id="40f8f-648">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="40f8f-649">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="40f8f-649">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-650">IRowset</span><span class="sxs-lookup"><span data-stu-id="40f8f-650">IRowset</span></span></p></td>
<td><p><span data-ttu-id="40f8f-651">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="40f8f-651">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-652">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="40f8f-652">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="40f8f-653">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="40f8f-653">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-654">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="40f8f-654">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="40f8f-655">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="40f8f-655">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-656">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="40f8f-656">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="40f8f-657">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="40f8f-657">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-658">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="40f8f-658">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="40f8f-659">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="40f8f-659">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-660">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="40f8f-660">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-661">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="40f8f-661">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="40f8f-662">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="40f8f-662">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-663">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="40f8f-663">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="40f8f-664">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="40f8f-664">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-665">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="40f8f-665">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="40f8f-666">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="40f8f-666">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-667">Литерал закладки</span><span class="sxs-lookup"><span data-stu-id="40f8f-667">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="40f8f-668">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="40f8f-668">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-669">Удостоверение литерала строки</span><span class="sxs-lookup"><span data-stu-id="40f8f-669">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="40f8f-670">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="40f8f-670">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-671">Максимальное число открытых строк</span><span class="sxs-lookup"><span data-stu-id="40f8f-671">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="40f8f-672">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="40f8f-672">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-673">Максимум ожидающие строк</span><span class="sxs-lookup"><span data-stu-id="40f8f-673">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="40f8f-674">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="40f8f-674">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-675">Максимальное число строк</span><span class="sxs-lookup"><span data-stu-id="40f8f-675">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="40f8f-676">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="40f8f-676">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-677">Степень детализации уведомлений</span><span class="sxs-lookup"><span data-stu-id="40f8f-677">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="40f8f-678">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="40f8f-678">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-679">Этапы уведомлений</span><span class="sxs-lookup"><span data-stu-id="40f8f-679">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="40f8f-680">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="40f8f-680">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-681">Объекты в транзакции</span><span class="sxs-lookup"><span data-stu-id="40f8f-681">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="40f8f-682">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="40f8f-682">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-683">Видны собственные изменения</span><span class="sxs-lookup"><span data-stu-id="40f8f-683">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="40f8f-684">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="40f8f-684">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-685">Видны собственные операции вставки</span><span class="sxs-lookup"><span data-stu-id="40f8f-685">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="40f8f-686">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="40f8f-686">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-687">Сохранять при аварийном завершении</span><span class="sxs-lookup"><span data-stu-id="40f8f-687">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="40f8f-688">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="40f8f-688">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-689">Сохранять при фиксации</span><span class="sxs-lookup"><span data-stu-id="40f8f-689">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="40f8f-690">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="40f8f-690">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-691">Быстрый перезапуск</span><span class="sxs-lookup"><span data-stu-id="40f8f-691">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="40f8f-692">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="40f8f-692">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-693">Повторные события</span><span class="sxs-lookup"><span data-stu-id="40f8f-693">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="40f8f-694">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="40f8f-694">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-695">Удаление удаленных строк</span><span class="sxs-lookup"><span data-stu-id="40f8f-695">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="40f8f-696">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="40f8f-696">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-697">Сообщить о нескольких изменений</span><span class="sxs-lookup"><span data-stu-id="40f8f-697">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="40f8f-698">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="40f8f-698">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-699">Вернуть ожидающие вставки</span><span class="sxs-lookup"><span data-stu-id="40f8f-699">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="40f8f-700">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="40f8f-700">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-701">Удалить строку уведомлений</span><span class="sxs-lookup"><span data-stu-id="40f8f-701">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="40f8f-702">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="40f8f-702">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-703">Строка первого уведомления об изменении</span><span class="sxs-lookup"><span data-stu-id="40f8f-703">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="40f8f-704">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="40f8f-704">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-705">Строка вставки уведомлений</span><span class="sxs-lookup"><span data-stu-id="40f8f-705">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="40f8f-706">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="40f8f-706">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-707">Привилегии строки</span><span class="sxs-lookup"><span data-stu-id="40f8f-707">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="40f8f-708">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="40f8f-708">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-709">Уведомления о повторной синхронизации строки</span><span class="sxs-lookup"><span data-stu-id="40f8f-709">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="40f8f-710">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="40f8f-710">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-711">Строка, потоковой модели</span><span class="sxs-lookup"><span data-stu-id="40f8f-711">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="40f8f-712">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="40f8f-712">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-713">Уведомление об изменении отмены строки</span><span class="sxs-lookup"><span data-stu-id="40f8f-713">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="40f8f-714">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="40f8f-714">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-715">Строка отмены Delete уведомлений</span><span class="sxs-lookup"><span data-stu-id="40f8f-715">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="40f8f-716">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="40f8f-716">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-717">Вставка отмены строки уведомлений</span><span class="sxs-lookup"><span data-stu-id="40f8f-717">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="40f8f-718">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="40f8f-718">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-719">Уведомление об обновлении строки</span><span class="sxs-lookup"><span data-stu-id="40f8f-719">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="40f8f-720">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="40f8f-720">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-721">Уведомление об изменении положения строк выборки</span><span class="sxs-lookup"><span data-stu-id="40f8f-721">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="40f8f-722">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="40f8f-722">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-723">Уведомление о выпуске набора строк</span><span class="sxs-lookup"><span data-stu-id="40f8f-723">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="40f8f-724">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="40f8f-724">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-725">Прокрутка назад</span><span class="sxs-lookup"><span data-stu-id="40f8f-725">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="40f8f-726">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="40f8f-726">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-727">Пропустить удаленных закладки</span><span class="sxs-lookup"><span data-stu-id="40f8f-727">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="40f8f-728">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="40f8f-728">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-729">Строка строгого удостоверений</span><span class="sxs-lookup"><span data-stu-id="40f8f-729">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="40f8f-730">DBPROP_STRONGITDENTITY</span><span class="sxs-lookup"><span data-stu-id="40f8f-730">DBPROP_STRONGITDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-731">Уникальные строки</span><span class="sxs-lookup"><span data-stu-id="40f8f-731">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="40f8f-732">DBPROP_UNIQUEROWS</span><span class="sxs-lookup"><span data-stu-id="40f8f-732">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-733">Возможности обновления</span><span class="sxs-lookup"><span data-stu-id="40f8f-733">Updatability</span></span></p></td>
<td><p><span data-ttu-id="40f8f-734">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="40f8f-734">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-735">Использование закладок</span><span class="sxs-lookup"><span data-stu-id="40f8f-735">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="40f8f-736">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="40f8f-736">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a><span data-ttu-id="40f8f-737">Динамические свойства команды</span><span class="sxs-lookup"><span data-stu-id="40f8f-737">Command Dynamic Properties</span></span>

<span data-ttu-id="40f8f-738">Следующие свойства добавляются в коллекцию **свойств** объекта **команды** .</span><span class="sxs-lookup"><span data-stu-id="40f8f-738">The following properties are added to the **Command** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="40f8f-739">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="40f8f-739">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="40f8f-740">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="40f8f-740">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-741">Порядок доступа</span><span class="sxs-lookup"><span data-stu-id="40f8f-741">Access Order</span></span></p></td>
<td><p><span data-ttu-id="40f8f-742">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="40f8f-742">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-743">Блокировка объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="40f8f-743">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="40f8f-744">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="40f8f-744">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-745">Тип закладки</span><span class="sxs-lookup"><span data-stu-id="40f8f-745">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="40f8f-746">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="40f8f-746">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-747">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="40f8f-747">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="40f8f-748">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="40f8f-748">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-749">Изменение вставленных строк</span><span class="sxs-lookup"><span data-stu-id="40f8f-749">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="40f8f-750">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="40f8f-750">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-751">Права доступа столбца</span><span class="sxs-lookup"><span data-stu-id="40f8f-751">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="40f8f-752">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="40f8f-752">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-753">Столбец набор уведомлений</span><span class="sxs-lookup"><span data-stu-id="40f8f-753">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="40f8f-754">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="40f8f-754">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-755">Отложенное обновление объекта хранения</span><span class="sxs-lookup"><span data-stu-id="40f8f-755">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="40f8f-756">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="40f8f-756">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-757">Выборку</span><span class="sxs-lookup"><span data-stu-id="40f8f-757">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="40f8f-758">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="40f8f-758">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-759">Хранение строк</span><span class="sxs-lookup"><span data-stu-id="40f8f-759">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="40f8f-760">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="40f8f-760">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-761">IAccessor</span><span class="sxs-lookup"><span data-stu-id="40f8f-761">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="40f8f-762">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="40f8f-762">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-763">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="40f8f-763">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="40f8f-764">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="40f8f-764">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-765">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="40f8f-765">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="40f8f-766">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="40f8f-766">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-767">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="40f8f-767">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="40f8f-768">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="40f8f-768">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-769">IConvertType</span><span class="sxs-lookup"><span data-stu-id="40f8f-769">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="40f8f-770">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="40f8f-770">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-771">Немобильные строки</span><span class="sxs-lookup"><span data-stu-id="40f8f-771">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="40f8f-772">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="40f8f-772">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-773">IRowset</span><span class="sxs-lookup"><span data-stu-id="40f8f-773">IRowset</span></span></p></td>
<td><p><span data-ttu-id="40f8f-774">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="40f8f-774">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-775">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="40f8f-775">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="40f8f-776">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="40f8f-776">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-777">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="40f8f-777">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="40f8f-778">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="40f8f-778">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-779">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="40f8f-779">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="40f8f-780">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="40f8f-780">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-781">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="40f8f-781">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="40f8f-782">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="40f8f-782">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-783">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="40f8f-783">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-784">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="40f8f-784">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="40f8f-785">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="40f8f-785">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-786">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="40f8f-786">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="40f8f-787">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="40f8f-787">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-788">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="40f8f-788">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="40f8f-789">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="40f8f-789">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-790">Литерал закладки</span><span class="sxs-lookup"><span data-stu-id="40f8f-790">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="40f8f-791">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="40f8f-791">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-792">Удостоверение литерала строки</span><span class="sxs-lookup"><span data-stu-id="40f8f-792">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="40f8f-793">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="40f8f-793">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-794">Максимальное число открытых строк</span><span class="sxs-lookup"><span data-stu-id="40f8f-794">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="40f8f-795">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="40f8f-795">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-796">Максимум ожидающие строк</span><span class="sxs-lookup"><span data-stu-id="40f8f-796">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="40f8f-797">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="40f8f-797">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-798">Максимальное число строк</span><span class="sxs-lookup"><span data-stu-id="40f8f-798">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="40f8f-799">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="40f8f-799">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-800">Степень детализации уведомлений</span><span class="sxs-lookup"><span data-stu-id="40f8f-800">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="40f8f-801">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="40f8f-801">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-802">Этапы уведомлений</span><span class="sxs-lookup"><span data-stu-id="40f8f-802">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="40f8f-803">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="40f8f-803">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-804">Объекты в транзакции</span><span class="sxs-lookup"><span data-stu-id="40f8f-804">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="40f8f-805">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="40f8f-805">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-806">Видны собственные изменения</span><span class="sxs-lookup"><span data-stu-id="40f8f-806">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="40f8f-807">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="40f8f-807">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-808">Видны собственные операции вставки</span><span class="sxs-lookup"><span data-stu-id="40f8f-808">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="40f8f-809">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="40f8f-809">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-810">Сохранять при аварийном завершении</span><span class="sxs-lookup"><span data-stu-id="40f8f-810">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="40f8f-811">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="40f8f-811">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-812">Сохранять при фиксации</span><span class="sxs-lookup"><span data-stu-id="40f8f-812">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="40f8f-813">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="40f8f-813">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-814">Быстрый перезапуск</span><span class="sxs-lookup"><span data-stu-id="40f8f-814">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="40f8f-815">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="40f8f-815">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-816">Повторные события</span><span class="sxs-lookup"><span data-stu-id="40f8f-816">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="40f8f-817">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="40f8f-817">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-818">Удаление удаленных строк</span><span class="sxs-lookup"><span data-stu-id="40f8f-818">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="40f8f-819">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="40f8f-819">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-820">Сообщить о нескольких изменений</span><span class="sxs-lookup"><span data-stu-id="40f8f-820">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="40f8f-821">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="40f8f-821">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-822">Вернуть ожидающие вставки</span><span class="sxs-lookup"><span data-stu-id="40f8f-822">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="40f8f-823">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="40f8f-823">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-824">Удалить строку уведомлений</span><span class="sxs-lookup"><span data-stu-id="40f8f-824">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="40f8f-825">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="40f8f-825">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-826">Строка первого уведомления об изменении</span><span class="sxs-lookup"><span data-stu-id="40f8f-826">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="40f8f-827">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="40f8f-827">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-828">Строка вставки уведомлений</span><span class="sxs-lookup"><span data-stu-id="40f8f-828">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="40f8f-829">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="40f8f-829">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-830">Привилегии строки</span><span class="sxs-lookup"><span data-stu-id="40f8f-830">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="40f8f-831">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="40f8f-831">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-832">Уведомления о повторной синхронизации строки</span><span class="sxs-lookup"><span data-stu-id="40f8f-832">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="40f8f-833">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="40f8f-833">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-834">Строка, потоковой модели</span><span class="sxs-lookup"><span data-stu-id="40f8f-834">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="40f8f-835">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="40f8f-835">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-836">Уведомление об изменении отмены строки</span><span class="sxs-lookup"><span data-stu-id="40f8f-836">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="40f8f-837">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="40f8f-837">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-838">Строка отмены Delete уведомлений</span><span class="sxs-lookup"><span data-stu-id="40f8f-838">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="40f8f-839">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="40f8f-839">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-840">Вставка отмены строки уведомлений</span><span class="sxs-lookup"><span data-stu-id="40f8f-840">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="40f8f-841">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="40f8f-841">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-842">Уведомление об обновлении строки</span><span class="sxs-lookup"><span data-stu-id="40f8f-842">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="40f8f-843">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="40f8f-843">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-844">Уведомление об изменении положения строк выборки</span><span class="sxs-lookup"><span data-stu-id="40f8f-844">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="40f8f-845">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="40f8f-845">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-846">Уведомление о выпуске набора строк</span><span class="sxs-lookup"><span data-stu-id="40f8f-846">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="40f8f-847">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="40f8f-847">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-848">Прокрутка назад</span><span class="sxs-lookup"><span data-stu-id="40f8f-848">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="40f8f-849">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="40f8f-849">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-850">Пропустить удаленных закладки</span><span class="sxs-lookup"><span data-stu-id="40f8f-850">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="40f8f-851">DBPROP_BOOKMARKSKIP</span><span class="sxs-lookup"><span data-stu-id="40f8f-851">DBPROP_BOOKMARKSKIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-852">Строка строгого удостоверений</span><span class="sxs-lookup"><span data-stu-id="40f8f-852">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="40f8f-853">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="40f8f-853">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f8f-854">Возможности обновления</span><span class="sxs-lookup"><span data-stu-id="40f8f-854">Updatability</span></span></p></td>
<td><p><span data-ttu-id="40f8f-855">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="40f8f-855">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f8f-856">Использование закладок</span><span class="sxs-lookup"><span data-stu-id="40f8f-856">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="40f8f-857">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="40f8f-857">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="40f8f-858">См. также</span><span class="sxs-lookup"><span data-stu-id="40f8f-858">See also</span></span>

<span data-ttu-id="40f8f-859">Для получения дополнительных сведений о реализации и функциональным сведения о поставщик Microsoft OLE DB для ODBC обратитесь к [OLE DB Руководство программиста](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85)) или посетите [Центр разработчиков данных платформы](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).</span><span class="sxs-lookup"><span data-stu-id="40f8f-859">For details regarding specific implementation and functional information about the Microsoft OLE DB Provider for ODBC, consult the [OLE DB Programmer's Guide](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85)) or visit the [Data Platform Developer Center](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).</span></span>

