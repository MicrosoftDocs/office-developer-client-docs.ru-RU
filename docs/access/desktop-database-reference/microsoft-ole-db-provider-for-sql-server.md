---
title: Поставщик Microsoft OLE DB для SQL Server
TOCTitle: Microsoft OLE DB Provider for SQL Server
ms:assetid: 0ffdea03-1a76-499b-f649-423f6b3c13d7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248868(v=office.15)
ms:contentKeyID: 48543282
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c4faa664ed9001c1c06906f58c7d873faf75a5d0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288892"
---
# <a name="microsoft-ole-db-provider-for-sql-server"></a><span data-ttu-id="6e7d0-102">Поставщик Microsoft OLE DB для SQL Server</span><span class="sxs-lookup"><span data-stu-id="6e7d0-102">Microsoft OLE DB Provider for SQL Server</span></span>


<span data-ttu-id="6e7d0-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6e7d0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6e7d0-104">Поставщик DB Microsoft OLE для SQL Server SQLOLEDB позволяет ADO получать доступ к Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="6e7d0-104">The Microsoft OLE DB Provider for SQL Server, SQLOLEDB, allows ADO to access Microsoft SQL Server.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="6e7d0-105">Параметры строки подключения</span><span class="sxs-lookup"><span data-stu-id="6e7d0-105">Connection String Parameters</span></span>

<span data-ttu-id="6e7d0-106">Чтобы подключиться к этому поставщику, установите аргумент *Поставщика* [свойству ConnectionString:](connectionstring-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="6e7d0-106">To connect to this provider, set the *Provider* argument to the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```sql 
 
SQLOLEDB 
```

<span data-ttu-id="6e7d0-107">Это значение также можно установить или прочитать с помощью свойства [Provider.](provider-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="6e7d0-107">This value can also be set or read using the [Provider](provider-property-ado.md) property.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="6e7d0-108">Типичная строка подключения</span><span class="sxs-lookup"><span data-stu-id="6e7d0-108">Typical Connection String</span></span>

<span data-ttu-id="6e7d0-109">Типичная строка подключения для этого поставщика:</span><span class="sxs-lookup"><span data-stu-id="6e7d0-109">A typical connection string for this provider is:</span></span>

```sql 
 
"Provider=SQLOLEDB;Data Source=serverName;" 
Initial Catalog=databaseName; 
User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="6e7d0-110">Строка состоит из этих ключевых слов:</span><span class="sxs-lookup"><span data-stu-id="6e7d0-110">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6e7d0-111">Ключевое слово</span><span class="sxs-lookup"><span data-stu-id="6e7d0-111">Keyword</span></span></p></th>
<th><p><span data-ttu-id="6e7d0-112">Description</span><span class="sxs-lookup"><span data-stu-id="6e7d0-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-113"><strong>Поставщик</strong></span><span class="sxs-lookup"><span data-stu-id="6e7d0-113"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="6e7d0-114">Указывает поставщика OLE DB для SQL Server.</span><span class="sxs-lookup"><span data-stu-id="6e7d0-114">Specifies the OLE DB Provider for SQL Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-115"><strong>Источник данных</strong> или <strong>сервер</strong></span><span class="sxs-lookup"><span data-stu-id="6e7d0-115"><strong>Data Source</strong> or <strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="6e7d0-116">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="6e7d0-116">Specifies the name of a server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-117"><strong>Начальный каталог</strong> или <strong>база данных</strong></span><span class="sxs-lookup"><span data-stu-id="6e7d0-117"><strong>Initial Catalog</strong> or <strong>Database</strong></span></span></p></td>
<td><p><span data-ttu-id="6e7d0-118">Указывает имя базы данных на сервере.</span><span class="sxs-lookup"><span data-stu-id="6e7d0-118">Specifies the name of a database on the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-119"><strong>Пользовательский ID</strong> или <strong>uid</strong></span><span class="sxs-lookup"><span data-stu-id="6e7d0-119"><strong>User ID</strong> or <strong>uid</strong></span></span></p></td>
<td><p><span data-ttu-id="6e7d0-120">Указывает имя пользователя (для SQL Server проверки подлинности).</span><span class="sxs-lookup"><span data-stu-id="6e7d0-120">Specifies the user name (for SQL Server Authentication).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-121"><strong>Пароль</strong> или <strong>pwd</strong></span><span class="sxs-lookup"><span data-stu-id="6e7d0-121"><strong>Password</strong> or <strong>pwd</strong></span></span></p></td>
<td><p><span data-ttu-id="6e7d0-122">Указывает пароль пользователя (для SQL Server проверки подлинности).</span><span class="sxs-lookup"><span data-stu-id="6e7d0-122">Specifies the user password (for SQL Server Authentication).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-connection-parameters"></a><span data-ttu-id="6e7d0-123">Provider-Specific параметры подключения</span><span class="sxs-lookup"><span data-stu-id="6e7d0-123">Provider-Specific Connection Parameters</span></span>

<span data-ttu-id="6e7d0-124">Поставщик поддерживает несколько параметров подключения, определенных для поставщика, в дополнение к параметрам, определенным ADO.</span><span class="sxs-lookup"><span data-stu-id="6e7d0-124">The provider supports several provider-specific connection parameters in addition to those defined by ADO.</span></span> <span data-ttu-id="6e7d0-125">Как и в свойствах подключения ADO, эти свойства, определенные для поставщика, можно установить через коллекцию [свойств](properties-collection-ado.md) подключения или установить в составе **ConnectionString.** [](connection-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="6e7d0-125">As with the ADO connection properties, these provider-specific properties can be set via the [Properties](properties-collection-ado.md) collection of a [Connection](connection-object-ado.md) or can be set as part of the **ConnectionString**.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6e7d0-126">Параметр</span><span class="sxs-lookup"><span data-stu-id="6e7d0-126">Parameter</span></span></p></th>
<th><p><span data-ttu-id="6e7d0-127">Описание</span><span class="sxs-lookup"><span data-stu-id="6e7d0-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-128">Trusted_Connection</span><span class="sxs-lookup"><span data-stu-id="6e7d0-128">Trusted_Connection</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-129">Указывает режим проверки подлинности пользователей.</span><span class="sxs-lookup"><span data-stu-id="6e7d0-129">Indicates the user authentication mode.</span></span> <span data-ttu-id="6e7d0-130">Это может быть заданной <strong>для Да</strong> или <strong>Нет</strong>.</span><span class="sxs-lookup"><span data-stu-id="6e7d0-130">This can be set to <strong>Yes</strong> or <strong>No</strong>.</span></span> <span data-ttu-id="6e7d0-131">По умолчанию выбрано <strong>Нет</strong>.</span><span class="sxs-lookup"><span data-stu-id="6e7d0-131">The default value is <strong>No</strong>.</span></span> <span data-ttu-id="6e7d0-132">Если это свойство задано <strong>да,</strong>то SQLOLEDB использует режим проверки подлинности microsoft Windows NT для авторизации доступа пользователей к базе данных SQL Server, указанной значениями свойств Location <strong>и</strong> <a href="datasource-property-ado.md">Datasource.</a></span><span class="sxs-lookup"><span data-stu-id="6e7d0-132">If this property is set to <strong>Yes</strong>, then SQLOLEDB uses Microsoft Windows NT Authentication Mode to authorize user access to the SQL Server database specified by the <strong>Location</strong> and <a href="datasource-property-ado.md">Datasource</a> property values.</span></span> <span data-ttu-id="6e7d0-133">Если это свойство настроено на <strong>нет,</strong>SQLOLEDB использует смешанный режим для авторизации доступа пользователей к SQL Server базе данных.</span><span class="sxs-lookup"><span data-stu-id="6e7d0-133">If this property is set to <strong>No</strong>, then SQLOLEDB uses Mixed Mode to authorize user access to the SQL Server database.</span></span> <span data-ttu-id="6e7d0-134">Код SQL Server и пароль указаны в <strong>свойствах User Id</strong> и <strong>Password.</strong></span><span class="sxs-lookup"><span data-stu-id="6e7d0-134">The SQL Server login and password are specified in the <strong>User Id</strong> and <strong>Password</strong> properties.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-135">Current Language</span><span class="sxs-lookup"><span data-stu-id="6e7d0-135">Current Language</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-136">Указывает имя SQL Server языка.</span><span class="sxs-lookup"><span data-stu-id="6e7d0-136">Indicates a SQL Server language name.</span></span> <span data-ttu-id="6e7d0-137">Определяет язык, используемый для выбора и форматирования системных сообщений.</span><span class="sxs-lookup"><span data-stu-id="6e7d0-137">Identifies the language used for system message selection and formatting.</span></span> <span data-ttu-id="6e7d0-138">Язык должен быть установлен на SQL Server, в противном случае открытие подключения не удастся.</span><span class="sxs-lookup"><span data-stu-id="6e7d0-138">The language must be installed on the SQL Server, otherwise opening the connection will fail.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-139">Сетевой адрес</span><span class="sxs-lookup"><span data-stu-id="6e7d0-139">Network Address</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-140">Указывает сетевой адрес SQL Server, указанного <strong>свойством Location.</strong></span><span class="sxs-lookup"><span data-stu-id="6e7d0-140">Indicates the network address of the SQL Server specified by the <strong>Location</strong> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-141">Библиотека сети</span><span class="sxs-lookup"><span data-stu-id="6e7d0-141">Network Library</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-142">Указывает имя сетевой библиотеки (библиотеки динамических ссылок), используемой для связи с SQL Server.</span><span class="sxs-lookup"><span data-stu-id="6e7d0-142">Indicates the name of the network library (dynamic-link libraries) used to communicate with the SQL Server.</span></span> <span data-ttu-id="6e7d0-143">Имя не должно включать путь или расширение .dll файла.</span><span class="sxs-lookup"><span data-stu-id="6e7d0-143">The name should not include the path or the .dll file name extension.</span></span> <span data-ttu-id="6e7d0-144">По умолчанию предоставляется конфигурация SQL Server клиента.</span><span class="sxs-lookup"><span data-stu-id="6e7d0-144">The default is provided by the SQL Server client configuration.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-145">Использование процедуры подготовки</span><span class="sxs-lookup"><span data-stu-id="6e7d0-145">Use Procedure for Prepare</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-146">Определяет, создает ли SQL Server временные сохраненные процедуры при подготовке команд (по свойству <strong>Prepared).</strong></span><span class="sxs-lookup"><span data-stu-id="6e7d0-146">Determines whether SQL Server creates temporary stored procedures when Commands are prepared (by the <strong>Prepared</strong> property).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-147">Auto Translate</span><span class="sxs-lookup"><span data-stu-id="6e7d0-147">Auto Translate</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-148">Указывает, преобразованы ли символы OEM/ANSI.</span><span class="sxs-lookup"><span data-stu-id="6e7d0-148">Indicates whether OEM/ANSI characters are converted.</span></span> <span data-ttu-id="6e7d0-149">Это свойство может быть заданной <strong>для True</strong> или <strong>False</strong>.</span><span class="sxs-lookup"><span data-stu-id="6e7d0-149">This property can be set to <strong>True</strong> or <strong>False</strong>.</span></span> <span data-ttu-id="6e7d0-150">Значение по умолчанию — <strong>True</strong>.</span><span class="sxs-lookup"><span data-stu-id="6e7d0-150">The default value is <strong>True</strong>.</span></span> <span data-ttu-id="6e7d0-151">Если это свойство настроено на <strong>True,</strong>то SQLOLEDB выполняет преобразование символов OEM/ANSI при извлечении или отправлении в SQL Server.</span><span class="sxs-lookup"><span data-stu-id="6e7d0-151">If this property is set to <strong>True</strong>, then SQLOLEDB performs OEM/ANSI character conversion when multi-byte character strings are retrieved from, or sent to, the SQL Server.</span></span> <span data-ttu-id="6e7d0-152">Если это свойство настроено на <strong>False,</strong>SQLOLEDB не выполняет преобразование символов OEM/ANSI в данные строки многобайтных символов.</span><span class="sxs-lookup"><span data-stu-id="6e7d0-152">If this property is set to <strong>False</strong>, then SQLOLEDB does not perform OEM/ANSI character conversion on multi-byte character string data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-153">Размер пакета</span><span class="sxs-lookup"><span data-stu-id="6e7d0-153">Packet Size</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-154">Указывает размер сетевого пакета в bytes.</span><span class="sxs-lookup"><span data-stu-id="6e7d0-154">Indicates a network packet size in bytes.</span></span> <span data-ttu-id="6e7d0-155">Значение свойства размера пакета должно быть между 512 и 32767.</span><span class="sxs-lookup"><span data-stu-id="6e7d0-155">The packet size property value must be between 512 and 32767.</span></span> <span data-ttu-id="6e7d0-156">Размер сетевого пакета SQLOLEDB по умолчанию — 4096.</span><span class="sxs-lookup"><span data-stu-id="6e7d0-156">The default SQLOLEDB network packet size is 4096.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-157">Имя приложения</span><span class="sxs-lookup"><span data-stu-id="6e7d0-157">Application Name</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-158">Указывает имя приложения клиента.</span><span class="sxs-lookup"><span data-stu-id="6e7d0-158">Indicates the client application name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-159">ID рабочей станции</span><span class="sxs-lookup"><span data-stu-id="6e7d0-159">Workstation ID</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-160">Строка, определяемая рабочей станции.</span><span class="sxs-lookup"><span data-stu-id="6e7d0-160">A string identifying the workstation.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-object-usage"></a><span data-ttu-id="6e7d0-161">Использование командных объектов</span><span class="sxs-lookup"><span data-stu-id="6e7d0-161">Command Object Usage</span></span>

<span data-ttu-id="6e7d0-162">SQLOLEDB принимает объединение ODBC, ANSI и SQL Server transact-SQL как допустимый синтаксис.</span><span class="sxs-lookup"><span data-stu-id="6e7d0-162">SQLOLEDB accepts an amalgam of ODBC, ANSI, and SQL Server-specific Transact-SQL as valid syntax.</span></span> <span data-ttu-id="6e7d0-163">Например, в следующем SQL для указания функции строки LCASE используется последовательность SQL ODBC:</span><span class="sxs-lookup"><span data-stu-id="6e7d0-163">For example, the following SQL statement uses an ODBC SQL escape sequence to specify the LCASE string function:</span></span>

```sql 
 
SELECT customerid={fn LCASE(CustomerID)} FROM Customers 
```

<span data-ttu-id="6e7d0-164">LCASE возвращает строку символов, преобразуя все символы верхнего шкафа в их эквиваленты нижнего регистра.</span><span class="sxs-lookup"><span data-stu-id="6e7d0-164">LCASE returns a character string, converting all uppercase characters to their lowercase equivalents.</span></span> <span data-ttu-id="6e7d0-165">Функция строки SQL ANSI LOWER выполняет ту же операцию, поэтому следующее SQL является эквивалентом утверждения ANSI, представленного выше:</span><span class="sxs-lookup"><span data-stu-id="6e7d0-165">The ANSI SQL string function LOWER performs the same operation, so the following SQL statement is an ANSI equivalent to the ODBC statement presented above:</span></span>

```sql
 
SELECT customerid=LOWER(CustomerID) FROM Customers 
```

<span data-ttu-id="6e7d0-166">SQLOLEDB успешно обрабатывает форму заявления, если указана в виде текста для команды.</span><span class="sxs-lookup"><span data-stu-id="6e7d0-166">SQLOLEDB successfully processes either form of the statement when specified as text for a command.</span></span>

## <a name="stored-procedures"></a><span data-ttu-id="6e7d0-167">Сохраненные процедуры</span><span class="sxs-lookup"><span data-stu-id="6e7d0-167">Stored Procedures</span></span>

<span data-ttu-id="6e7d0-168">При выполнении SQL Server с помощью команды SQLOLEDB используйте последовательность побега процедуры ODBC в тексте команды.</span><span class="sxs-lookup"><span data-stu-id="6e7d0-168">When executing a SQL Server stored procedure using a SQLOLEDB command, use the ODBC procedure call escape sequence in the command text.</span></span> <span data-ttu-id="6e7d0-169">Затем SQLOLEDB использует механизм удаленного вызова процедуры SQL Server для оптимизации обработки команд.</span><span class="sxs-lookup"><span data-stu-id="6e7d0-169">SQLOLEDB then uses the remote procedure call mechanism of SQL Server to optimize command processing.</span></span> <span data-ttu-id="6e7d0-170">Например, следующим утверждением SQL ODBC является предпочтительный командный текст по форме Transact-SQL:</span><span class="sxs-lookup"><span data-stu-id="6e7d0-170">For example, the following ODBC SQL statement is the preferred command text over the Transact-SQL form:</span></span>

## <a name="odbc-sql"></a><span data-ttu-id="6e7d0-171">ODBC SQL</span><span class="sxs-lookup"><span data-stu-id="6e7d0-171">ODBC SQL</span></span>

```sql 
 
{call SalesByCategory('Produce', '1995')} 
```

## <a name="transact-sql"></a><span data-ttu-id="6e7d0-172">Transact-SQL</span><span class="sxs-lookup"><span data-stu-id="6e7d0-172">Transact-SQL</span></span>

```sql 
 
EXECUTE SalesByCategory 'Produce', '1995' 
```

## <a name="recordset-behavior"></a><span data-ttu-id="6e7d0-173">Поведение наборов записей</span><span class="sxs-lookup"><span data-stu-id="6e7d0-173">Recordset Behavior</span></span>

<span data-ttu-id="6e7d0-174">SQLOLEDB не может использовать SQL Server курсоры для поддержки нескольких результатов, созданных многими командами.</span><span class="sxs-lookup"><span data-stu-id="6e7d0-174">SQLOLEDB cannot use SQL Server cursors to support the multiple-result generated by many commands.</span></span> <span data-ttu-id="6e7d0-175">Если потребитель запрашивает набор записей, требующий SQL Server поддержки курсора, возникает ошибка, если используемый текст команды создает более одного наборов записей в результате.</span><span class="sxs-lookup"><span data-stu-id="6e7d0-175">If a consumer requests a recordset requiring SQL Server cursor support, an error occurs if the command text used generates more than a single recordset as its result.</span></span>

<span data-ttu-id="6e7d0-176">Прокручиваемые записи SQLOLEDB поддерживаются SQL Server курсорами.</span><span class="sxs-lookup"><span data-stu-id="6e7d0-176">Scrollable SQLOLEDB recordsets are supported by SQL Server cursors.</span></span> <span data-ttu-id="6e7d0-177">SQL Server накладывает ограничения на курсоры, чувствительные к изменениям, внесенным другими пользователями базы данных.</span><span class="sxs-lookup"><span data-stu-id="6e7d0-177">SQL Server imposes limitations on cursors that are sensitive to changes made by other users of the database.</span></span> <span data-ttu-id="6e7d0-178">В частности, строки в некоторых курсорах невозможно заказать, и попытка создать набор записей с помощью команды, содержащей SQL ORDER BY, может привести к сбой.</span><span class="sxs-lookup"><span data-stu-id="6e7d0-178">Specifically, the rows in some cursors cannot be ordered, and attempting to create a recordset using a command containing an SQL ORDER BY clause can fail.</span></span>

## <a name="dynamic-properties"></a><span data-ttu-id="6e7d0-179">Dynamic Properties</span><span class="sxs-lookup"><span data-stu-id="6e7d0-179">Dynamic Properties</span></span>

<span data-ttu-id="6e7d0-180">Поставщик microsoft OLE DB для SQL Server вставляет несколько динамических свойств в коллекцию **свойств** незапертых объектов [Connection,](connection-object-ado.md) [Recordset](recordset-object-ado.md)и [Command.](command-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="6e7d0-180">The Microsoft OLE DB Provider for SQL Server inserts several dynamic properties into the **Properties** collection of the unopened [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md), and [Command](command-object-ado.md) objects.</span></span>

<span data-ttu-id="6e7d0-181">Следующие таблицы — это перекрестный индекс имен ADO и OLE DB для каждого динамического свойства.</span><span class="sxs-lookup"><span data-stu-id="6e7d0-181">The following tables are a cross-index of the ADO and OLE DB names for each dynamic property.</span></span> <span data-ttu-id="6e7d0-182">Ссылка программиста OLE DB относится к имени свойства ADO под термином "Описание".</span><span class="sxs-lookup"><span data-stu-id="6e7d0-182">The OLE DB Programmer's Reference refers to an ADO property name by the term "Description."</span></span> <span data-ttu-id="6e7d0-183">Дополнительные сведения об этих свойствах можно найти в справке программиста OLE DB.</span><span class="sxs-lookup"><span data-stu-id="6e7d0-183">You can find more information about these properties in the OLE DB Programmer's Reference.</span></span> <span data-ttu-id="6e7d0-184">Поиск имени свойства OLE DB в Индексе или см. в приложении C: OLE DB Properties.</span><span class="sxs-lookup"><span data-stu-id="6e7d0-184">Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span></span>

## <a name="connection-dynamic-properties"></a><span data-ttu-id="6e7d0-185">Динамические свойства подключения</span><span class="sxs-lookup"><span data-stu-id="6e7d0-185">Connection Dynamic Properties</span></span>

<span data-ttu-id="6e7d0-186">Следующие свойства добавляются в коллекцию  Свойств объекта **Connection.**</span><span class="sxs-lookup"><span data-stu-id="6e7d0-186">The following properties are added to the **Connection** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6e7d0-187">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="6e7d0-187">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="6e7d0-188">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="6e7d0-188">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-189">Активные сеансы</span><span class="sxs-lookup"><span data-stu-id="6e7d0-189">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-190">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="6e7d0-190">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-191">Asynchable Abort</span><span class="sxs-lookup"><span data-stu-id="6e7d0-191">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-192">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="6e7d0-192">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-193">Asynchable Commit</span><span class="sxs-lookup"><span data-stu-id="6e7d0-193">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-194">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="6e7d0-194">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-195">Уровни изоляции автокоммита</span><span class="sxs-lookup"><span data-stu-id="6e7d0-195">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-196">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="6e7d0-196">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-197">Расположение каталога</span><span class="sxs-lookup"><span data-stu-id="6e7d0-197">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-198">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="6e7d0-198">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-199">Термин Каталог</span><span class="sxs-lookup"><span data-stu-id="6e7d0-199">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-200">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="6e7d0-200">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-201">Определение столбцов</span><span class="sxs-lookup"><span data-stu-id="6e7d0-201">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-202">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="6e7d0-202">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-203">Подключение Время от времени</span><span class="sxs-lookup"><span data-stu-id="6e7d0-203">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-204">DBPROP_INIT_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="6e7d0-204">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-205">Текущий каталог</span><span class="sxs-lookup"><span data-stu-id="6e7d0-205">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-206">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="6e7d0-206">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-207">Источник данных</span><span class="sxs-lookup"><span data-stu-id="6e7d0-207">Data Source</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-208">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="6e7d0-208">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-209">Имя источника данных</span><span class="sxs-lookup"><span data-stu-id="6e7d0-209">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-210">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="6e7d0-210">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-211">Модель потоковой обработки объектов источника данных</span><span class="sxs-lookup"><span data-stu-id="6e7d0-211">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-212">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="6e7d0-212">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-213">Имя DBMS</span><span class="sxs-lookup"><span data-stu-id="6e7d0-213">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-214">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="6e7d0-214">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-215">Версия DBMS</span><span class="sxs-lookup"><span data-stu-id="6e7d0-215">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-216">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="6e7d0-216">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-217">Расширенные свойства</span><span class="sxs-lookup"><span data-stu-id="6e7d0-217">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-218">DBPROP_INIT_PROVIDERSTRING</span><span class="sxs-lookup"><span data-stu-id="6e7d0-218">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-219">Поддержка GROUP BY</span><span class="sxs-lookup"><span data-stu-id="6e7d0-219">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-220">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="6e7d0-220">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-221">Гетерогенная поддержка таблиц</span><span class="sxs-lookup"><span data-stu-id="6e7d0-221">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-222">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="6e7d0-222">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-223">Чувствительность к делу идентификатора</span><span class="sxs-lookup"><span data-stu-id="6e7d0-223">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-224">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="6e7d0-224">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-225">Начальный каталог</span><span class="sxs-lookup"><span data-stu-id="6e7d0-225">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-226">DBPROP_INIT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6e7d0-226">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-227">Уровни изоляции</span><span class="sxs-lookup"><span data-stu-id="6e7d0-227">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-228">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="6e7d0-228">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-229">Хранение изоляции</span><span class="sxs-lookup"><span data-stu-id="6e7d0-229">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-230">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="6e7d0-230">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-231">Идентификатор locale</span><span class="sxs-lookup"><span data-stu-id="6e7d0-231">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-232">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="6e7d0-232">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-233">Максимальный размер индекса</span><span class="sxs-lookup"><span data-stu-id="6e7d0-233">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-234">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="6e7d0-234">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-235">Максимальный размер строки</span><span class="sxs-lookup"><span data-stu-id="6e7d0-235">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-236">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="6e7d0-236">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-237">Максимальный размер строки включает BLOB</span><span class="sxs-lookup"><span data-stu-id="6e7d0-237">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-238">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="6e7d0-238">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-239">Максимальные таблицы в SELECT</span><span class="sxs-lookup"><span data-stu-id="6e7d0-239">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-240">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="6e7d0-240">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-241">Несколько наборов параметров</span><span class="sxs-lookup"><span data-stu-id="6e7d0-241">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-242">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="6e7d0-242">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-243">Несколько результатов</span><span class="sxs-lookup"><span data-stu-id="6e7d0-243">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-244">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="6e7d0-244">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-245">Несколько служба хранилища объектов</span><span class="sxs-lookup"><span data-stu-id="6e7d0-245">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-246">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="6e7d0-246">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-247">Обновление с несколькими таблицами</span><span class="sxs-lookup"><span data-stu-id="6e7d0-247">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-248">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="6e7d0-248">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-249">Порядок коллансирования NULL</span><span class="sxs-lookup"><span data-stu-id="6e7d0-249">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-250">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="6e7d0-250">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-251">NULL Concatenation Behaviour</span><span class="sxs-lookup"><span data-stu-id="6e7d0-251">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-252">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="6e7d0-252">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-253">Версия OLE DB</span><span class="sxs-lookup"><span data-stu-id="6e7d0-253">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-254">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="6e7d0-254">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-255">Поддержка объектов OLE</span><span class="sxs-lookup"><span data-stu-id="6e7d0-255">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-256">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="6e7d0-256">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-257">Поддержка open Rowset</span><span class="sxs-lookup"><span data-stu-id="6e7d0-257">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-258">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="6e7d0-258">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-259">ORDER BY Columns in Select List</span><span class="sxs-lookup"><span data-stu-id="6e7d0-259">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-260">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="6e7d0-260">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-261">Доступность параметров вывода</span><span class="sxs-lookup"><span data-stu-id="6e7d0-261">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-262">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="6e7d0-262">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-263">Pass By Ref Accessors</span><span class="sxs-lookup"><span data-stu-id="6e7d0-263">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-264">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="6e7d0-264">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-265">Password</span><span class="sxs-lookup"><span data-stu-id="6e7d0-265">Password</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-266">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="6e7d0-266">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-267">Сохраняются сведения о безопасности</span><span class="sxs-lookup"><span data-stu-id="6e7d0-267">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-268">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span><span class="sxs-lookup"><span data-stu-id="6e7d0-268">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-269">Тип сохраняемого ID</span><span class="sxs-lookup"><span data-stu-id="6e7d0-269">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-270">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="6e7d0-270">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-271">Подготовка поведения прервать</span><span class="sxs-lookup"><span data-stu-id="6e7d0-271">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-272">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="6e7d0-272">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-273">Подготовка поведения фиксации</span><span class="sxs-lookup"><span data-stu-id="6e7d0-273">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-274">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="6e7d0-274">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-275">Термин процедуры</span><span class="sxs-lookup"><span data-stu-id="6e7d0-275">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-276">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="6e7d0-276">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-277">Prompt</span><span class="sxs-lookup"><span data-stu-id="6e7d0-277">Prompt</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-278">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="6e7d0-278">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-279">Удобное имя поставщика</span><span class="sxs-lookup"><span data-stu-id="6e7d0-279">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-280">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="6e7d0-280">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-281">Имя поставщика</span><span class="sxs-lookup"><span data-stu-id="6e7d0-281">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-282">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="6e7d0-282">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-283">Версия поставщика</span><span class="sxs-lookup"><span data-stu-id="6e7d0-283">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-284">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="6e7d0-284">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-285">Read-Only источник данных</span><span class="sxs-lookup"><span data-stu-id="6e7d0-285">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-286">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="6e7d0-286">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-287">Преобразования rowset в командной строке</span><span class="sxs-lookup"><span data-stu-id="6e7d0-287">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-288">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="6e7d0-288">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-289">Термин Схемы</span><span class="sxs-lookup"><span data-stu-id="6e7d0-289">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-290">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="6e7d0-290">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-291">Использование схемы</span><span class="sxs-lookup"><span data-stu-id="6e7d0-291">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-292">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="6e7d0-292">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-293">SQL Поддержка</span><span class="sxs-lookup"><span data-stu-id="6e7d0-293">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-294">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="6e7d0-294">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-295">Структурированные служба хранилища</span><span class="sxs-lookup"><span data-stu-id="6e7d0-295">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-296">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="6e7d0-296">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-297">Поддержка subquery</span><span class="sxs-lookup"><span data-stu-id="6e7d0-297">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-298">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="6e7d0-298">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-299">Термин Таблица</span><span class="sxs-lookup"><span data-stu-id="6e7d0-299">Table Term</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-300">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="6e7d0-300">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-301">DDL транзакций</span><span class="sxs-lookup"><span data-stu-id="6e7d0-301">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-302">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="6e7d0-302">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-303">Идентификатор пользователя</span><span class="sxs-lookup"><span data-stu-id="6e7d0-303">User ID</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-304">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="6e7d0-304">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-305">имя пользователя;</span><span class="sxs-lookup"><span data-stu-id="6e7d0-305">User Name</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-306">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="6e7d0-306">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-307">Ручка окна</span><span class="sxs-lookup"><span data-stu-id="6e7d0-307">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-308">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="6e7d0-308">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a><span data-ttu-id="6e7d0-309">Динамические свойства Recordset</span><span class="sxs-lookup"><span data-stu-id="6e7d0-309">Recordset Dynamic Properties</span></span>

<span data-ttu-id="6e7d0-310">Следующие свойства добавляются в коллекцию Свойств  объекта **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="6e7d0-310">The following properties are added to the **Recordset** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6e7d0-311">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="6e7d0-311">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="6e7d0-312">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="6e7d0-312">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-313">Порядок доступа</span><span class="sxs-lookup"><span data-stu-id="6e7d0-313">Access Order</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-314">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="6e7d0-314">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-315">Блокировка служба хранилища объектов</span><span class="sxs-lookup"><span data-stu-id="6e7d0-315">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-316">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="6e7d0-316">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-317">Тип закладок</span><span class="sxs-lookup"><span data-stu-id="6e7d0-317">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-318">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="6e7d0-318">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-319">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="6e7d0-319">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-320">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="6e7d0-320">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-321">Изменение вставленных строк</span><span class="sxs-lookup"><span data-stu-id="6e7d0-321">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-322">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="6e7d0-322">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-323">Привилегии столбца</span><span class="sxs-lookup"><span data-stu-id="6e7d0-323">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-324">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="6e7d0-324">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-325">Уведомление о наборе столбцов</span><span class="sxs-lookup"><span data-stu-id="6e7d0-325">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-326">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="6e7d0-326">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-327">Командный выход</span><span class="sxs-lookup"><span data-stu-id="6e7d0-327">Command Time Out</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-328">DBPROP_COMMANDTIMEOUT</span><span class="sxs-lookup"><span data-stu-id="6e7d0-328">DBPROP_COMMANDTIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-329">Столбец Отсрочка</span><span class="sxs-lookup"><span data-stu-id="6e7d0-329">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-330">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="6e7d0-330">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-331">Задержка служба хранилища обновлений объектов</span><span class="sxs-lookup"><span data-stu-id="6e7d0-331">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-332">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="6e7d0-332">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-333">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="6e7d0-333">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-334">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="6e7d0-334">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-335">Строки удержания</span><span class="sxs-lookup"><span data-stu-id="6e7d0-335">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-336">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="6e7d0-336">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-337">IAccessor</span><span class="sxs-lookup"><span data-stu-id="6e7d0-337">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-338">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="6e7d0-338">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-339">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="6e7d0-339">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-340">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="6e7d0-340">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-341">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="6e7d0-341">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-342">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="6e7d0-342">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-343">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="6e7d0-343">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-344">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="6e7d0-344">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-345">IConvertType</span><span class="sxs-lookup"><span data-stu-id="6e7d0-345">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-346">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="6e7d0-346">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-347">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="6e7d0-347">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-348">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="6e7d0-348">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-349">IRowset</span><span class="sxs-lookup"><span data-stu-id="6e7d0-349">IRowset</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-350">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="6e7d0-350">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-351">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="6e7d0-351">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-352">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="6e7d0-352">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-353">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="6e7d0-353">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-354">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="6e7d0-354">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-355">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="6e7d0-355">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-356">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="6e7d0-356">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-357">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="6e7d0-357">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-358">DBPROP_IRowsestLocate</span><span class="sxs-lookup"><span data-stu-id="6e7d0-358">DBPROP_IRowsestLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-359">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="6e7d0-359">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-360">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="6e7d0-360">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-361">DBPROP_IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="6e7d0-361">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-362">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="6e7d0-362">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-363">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="6e7d0-363">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-364">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="6e7d0-364">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-365">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="6e7d0-365">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-366">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="6e7d0-366">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-367">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="6e7d0-367">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-368">Буквальные закладки</span><span class="sxs-lookup"><span data-stu-id="6e7d0-368">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-369">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="6e7d0-369">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-370">Удостоверение буквальных строк</span><span class="sxs-lookup"><span data-stu-id="6e7d0-370">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-371">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="6e7d0-371">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-372">Максимальные открытые строки</span><span class="sxs-lookup"><span data-stu-id="6e7d0-372">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-373">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="6e7d0-373">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-374">Максимальное количество ожидающих строк</span><span class="sxs-lookup"><span data-stu-id="6e7d0-374">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-375">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="6e7d0-375">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-376">Максимальные строки</span><span class="sxs-lookup"><span data-stu-id="6e7d0-376">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-377">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="6e7d0-377">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-378">Детализация уведомлений</span><span class="sxs-lookup"><span data-stu-id="6e7d0-378">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-379">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="6e7d0-379">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-380">Этапы уведомлений</span><span class="sxs-lookup"><span data-stu-id="6e7d0-380">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-381">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="6e7d0-381">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-382">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="6e7d0-382">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-383">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="6e7d0-383">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-384">Видимые изменения других</span><span class="sxs-lookup"><span data-stu-id="6e7d0-384">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-385">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="6e7d0-385">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-386">Видимые вставки других</span><span class="sxs-lookup"><span data-stu-id="6e7d0-386">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-387">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="6e7d0-387">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-388">Собственные изменения Видимые</span><span class="sxs-lookup"><span data-stu-id="6e7d0-388">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-389">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="6e7d0-389">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-390">Собственные вставки Видимые</span><span class="sxs-lookup"><span data-stu-id="6e7d0-390">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-391">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="6e7d0-391">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-392">Сохранение на abort</span><span class="sxs-lookup"><span data-stu-id="6e7d0-392">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-393">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="6e7d0-393">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-394">Сохранение на коммит</span><span class="sxs-lookup"><span data-stu-id="6e7d0-394">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-395">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="6e7d0-395">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-396">Быстрая перезагрузка</span><span class="sxs-lookup"><span data-stu-id="6e7d0-396">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-397">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="6e7d0-397">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-398">События для повторного антуламента</span><span class="sxs-lookup"><span data-stu-id="6e7d0-398">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-399">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="6e7d0-399">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-400">Удаление удаленных строк</span><span class="sxs-lookup"><span data-stu-id="6e7d0-400">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-401">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="6e7d0-401">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-402">Отчет о нескольких изменениях</span><span class="sxs-lookup"><span data-stu-id="6e7d0-402">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-403">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="6e7d0-403">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-404">Возвращение ожидающих вставок</span><span class="sxs-lookup"><span data-stu-id="6e7d0-404">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-405">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="6e7d0-405">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-406">Уведомление об удалении строки</span><span class="sxs-lookup"><span data-stu-id="6e7d0-406">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-407">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="6e7d0-407">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-408">Уведомление о первом изменении строки</span><span class="sxs-lookup"><span data-stu-id="6e7d0-408">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-409">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="6e7d0-409">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-410">Уведомление о вставке строки</span><span class="sxs-lookup"><span data-stu-id="6e7d0-410">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-411">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="6e7d0-411">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-412">Привилегии строки</span><span class="sxs-lookup"><span data-stu-id="6e7d0-412">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-413">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="6e7d0-413">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-414">Уведомление о повторной синхронизации строк</span><span class="sxs-lookup"><span data-stu-id="6e7d0-414">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-415">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="6e7d0-415">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-416">Модель потоков строки</span><span class="sxs-lookup"><span data-stu-id="6e7d0-416">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-417">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="6e7d0-417">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-418">Уведомление об отмене строки</span><span class="sxs-lookup"><span data-stu-id="6e7d0-418">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-419">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="6e7d0-419">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-420">Уведомление об отмене строки</span><span class="sxs-lookup"><span data-stu-id="6e7d0-420">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-421">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="6e7d0-421">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-422">Уведомление об отмене строки</span><span class="sxs-lookup"><span data-stu-id="6e7d0-422">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-423">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="6e7d0-423">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-424">Уведомление об обновлении строки</span><span class="sxs-lookup"><span data-stu-id="6e7d0-424">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-425">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="6e7d0-425">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-426">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="6e7d0-426">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-427">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="6e7d0-427">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-428">Уведомление о выпуске Rowset</span><span class="sxs-lookup"><span data-stu-id="6e7d0-428">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-429">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="6e7d0-429">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-430">Прокрутите назад</span><span class="sxs-lookup"><span data-stu-id="6e7d0-430">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-431">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="6e7d0-431">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-432">Курсор сервера</span><span class="sxs-lookup"><span data-stu-id="6e7d0-432">Server Cursor</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-433">DBPROP_SERVERCURSOR</span><span class="sxs-lookup"><span data-stu-id="6e7d0-433">DBPROP_SERVERCURSOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-434">Пропустить удаленные закладки</span><span class="sxs-lookup"><span data-stu-id="6e7d0-434">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-435">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="6e7d0-435">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-436">Удостоверение Strong Row</span><span class="sxs-lookup"><span data-stu-id="6e7d0-436">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-437">DBPROP_STRONGITDENTITY</span><span class="sxs-lookup"><span data-stu-id="6e7d0-437">DBPROP_STRONGITDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-438">Уникальные строки</span><span class="sxs-lookup"><span data-stu-id="6e7d0-438">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-439">DBPROP_UNIQUEROWS</span><span class="sxs-lookup"><span data-stu-id="6e7d0-439">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-440">Updatability</span><span class="sxs-lookup"><span data-stu-id="6e7d0-440">Updatability</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-441">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="6e7d0-441">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-442">Использование закладок</span><span class="sxs-lookup"><span data-stu-id="6e7d0-442">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-443">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="6e7d0-443">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a><span data-ttu-id="6e7d0-444">Командные динамические свойства</span><span class="sxs-lookup"><span data-stu-id="6e7d0-444">Command Dynamic Properties</span></span>

<span data-ttu-id="6e7d0-445">Следующие свойства добавляются в коллекцию **Свойств** объекта **Command.**</span><span class="sxs-lookup"><span data-stu-id="6e7d0-445">The following properties are added to the **Command** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6e7d0-446">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="6e7d0-446">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="6e7d0-447">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="6e7d0-447">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-448">Порядок доступа</span><span class="sxs-lookup"><span data-stu-id="6e7d0-448">Access Order</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-449">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="6e7d0-449">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-450">Базовый путь</span><span class="sxs-lookup"><span data-stu-id="6e7d0-450">Base Path</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-451">SSPROP_STREAM_BASEPATH</span><span class="sxs-lookup"><span data-stu-id="6e7d0-451">SSPROP_STREAM_BASEPATH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-452">Блокировка служба хранилища объектов</span><span class="sxs-lookup"><span data-stu-id="6e7d0-452">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-453">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="6e7d0-453">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-454">Тип закладок</span><span class="sxs-lookup"><span data-stu-id="6e7d0-454">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-455">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="6e7d0-455">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-456">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="6e7d0-456">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-457">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="6e7d0-457">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-458">Изменение вставленных строк</span><span class="sxs-lookup"><span data-stu-id="6e7d0-458">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-459">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="6e7d0-459">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-460">Привилегии столбца</span><span class="sxs-lookup"><span data-stu-id="6e7d0-460">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-461">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="6e7d0-461">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-462">Уведомление о наборе столбцов</span><span class="sxs-lookup"><span data-stu-id="6e7d0-462">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-463">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="6e7d0-463">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-464">Тип контента</span><span class="sxs-lookup"><span data-stu-id="6e7d0-464">Content Type</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-465">SSPROP_STREAM_CONTENTTYPE</span><span class="sxs-lookup"><span data-stu-id="6e7d0-465">SSPROP_STREAM_CONTENTTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-466">Автоматическое извлечение cursor</span><span class="sxs-lookup"><span data-stu-id="6e7d0-466">Cursor Auto Fetch</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-467">SSPROP_CURSORAUTOFETCH</span><span class="sxs-lookup"><span data-stu-id="6e7d0-467">SSPROP_CURSORAUTOFETCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-468">Столбец Отсрочка</span><span class="sxs-lookup"><span data-stu-id="6e7d0-468">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-469">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="6e7d0-469">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-470">Отсрочка подготовки</span><span class="sxs-lookup"><span data-stu-id="6e7d0-470">Defer Prepare</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-471">SSPROP_DEFERPREPARE</span><span class="sxs-lookup"><span data-stu-id="6e7d0-471">SSPROP_DEFERPREPARE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-472">Задержка служба хранилища обновлений объектов</span><span class="sxs-lookup"><span data-stu-id="6e7d0-472">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-473">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="6e7d0-473">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-474">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="6e7d0-474">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-475">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="6e7d0-475">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-476">Строки удержания</span><span class="sxs-lookup"><span data-stu-id="6e7d0-476">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-477">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="6e7d0-477">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-478">IAccessor</span><span class="sxs-lookup"><span data-stu-id="6e7d0-478">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-479">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="6e7d0-479">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-480">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="6e7d0-480">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-481">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="6e7d0-481">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-482">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="6e7d0-482">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-483">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="6e7d0-483">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-484">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="6e7d0-484">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-485">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="6e7d0-485">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-486">IConvertType</span><span class="sxs-lookup"><span data-stu-id="6e7d0-486">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-487">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="6e7d0-487">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-488">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="6e7d0-488">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-489">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="6e7d0-489">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-490">IRowset</span><span class="sxs-lookup"><span data-stu-id="6e7d0-490">IRowset</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-491">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="6e7d0-491">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-492">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="6e7d0-492">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-493">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="6e7d0-493">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-494">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="6e7d0-494">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-495">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="6e7d0-495">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-496">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="6e7d0-496">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-497">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="6e7d0-497">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-498">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="6e7d0-498">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-499">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="6e7d0-499">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-500">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="6e7d0-500">IRowsetResynch</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-501">DBPROP_IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="6e7d0-501">DBPROP_IRowsetResynch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-502">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="6e7d0-502">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-503">DBPROP_IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="6e7d0-503">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-504">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="6e7d0-504">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-505">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="6e7d0-505">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-506">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="6e7d0-506">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-507">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="6e7d0-507">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-508">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="6e7d0-508">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-509">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="6e7d0-509">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-510">Буквальные закладки</span><span class="sxs-lookup"><span data-stu-id="6e7d0-510">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-511">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="6e7d0-511">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-512">Удостоверение буквальных строк</span><span class="sxs-lookup"><span data-stu-id="6e7d0-512">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-513">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="6e7d0-513">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-514">Режим блокировки</span><span class="sxs-lookup"><span data-stu-id="6e7d0-514">Lock Mode</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-515">DBPROP_LOCKMODE</span><span class="sxs-lookup"><span data-stu-id="6e7d0-515">DBPROP_LOCKMODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-516">Максимальные открытые строки</span><span class="sxs-lookup"><span data-stu-id="6e7d0-516">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-517">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="6e7d0-517">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-518">Максимальное количество ожидающих строк</span><span class="sxs-lookup"><span data-stu-id="6e7d0-518">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-519">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="6e7d0-519">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-520">Максимальные строки</span><span class="sxs-lookup"><span data-stu-id="6e7d0-520">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-521">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="6e7d0-521">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-522">Детализация уведомлений</span><span class="sxs-lookup"><span data-stu-id="6e7d0-522">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-523">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="6e7d0-523">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-524">Этапы уведомлений</span><span class="sxs-lookup"><span data-stu-id="6e7d0-524">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-525">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="6e7d0-525">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-526">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="6e7d0-526">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-527">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="6e7d0-527">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-528">Видимые изменения других</span><span class="sxs-lookup"><span data-stu-id="6e7d0-528">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-529">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="6e7d0-529">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-530">Видимые вставки других</span><span class="sxs-lookup"><span data-stu-id="6e7d0-530">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-531">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="6e7d0-531">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-532">Свойство коди-ния выходных данных</span><span class="sxs-lookup"><span data-stu-id="6e7d0-532">Output Encoding Property</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-533">DBPROP_OUTPUTENCODING</span><span class="sxs-lookup"><span data-stu-id="6e7d0-533">DBPROP_OUTPUTENCODING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-534">Свойство Поток выходных данных</span><span class="sxs-lookup"><span data-stu-id="6e7d0-534">Output Stream Property</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-535">DBPROP_OUTPUTSTREAM</span><span class="sxs-lookup"><span data-stu-id="6e7d0-535">DBPROP_OUTPUTSTREAM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-536">Собственные изменения Видимые</span><span class="sxs-lookup"><span data-stu-id="6e7d0-536">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-537">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="6e7d0-537">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-538">Собственные вставки Видимые</span><span class="sxs-lookup"><span data-stu-id="6e7d0-538">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-539">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="6e7d0-539">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-540">Сохранение на abort</span><span class="sxs-lookup"><span data-stu-id="6e7d0-540">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-541">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="6e7d0-541">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-542">Сохранение на коммит</span><span class="sxs-lookup"><span data-stu-id="6e7d0-542">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-543">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="6e7d0-543">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-544">Быстрая перезагрузка</span><span class="sxs-lookup"><span data-stu-id="6e7d0-544">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-545">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="6e7d0-545">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-546">События для повторного антуламента</span><span class="sxs-lookup"><span data-stu-id="6e7d0-546">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-547">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="6e7d0-547">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-548">Удаление удаленных строк</span><span class="sxs-lookup"><span data-stu-id="6e7d0-548">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-549">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="6e7d0-549">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-550">Отчет о нескольких изменениях</span><span class="sxs-lookup"><span data-stu-id="6e7d0-550">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-551">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="6e7d0-551">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-552">Возвращение ожидающих вставок</span><span class="sxs-lookup"><span data-stu-id="6e7d0-552">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-553">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="6e7d0-553">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-554">Уведомление об удалении строки</span><span class="sxs-lookup"><span data-stu-id="6e7d0-554">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-555">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="6e7d0-555">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-556">Уведомление о первом изменении строки</span><span class="sxs-lookup"><span data-stu-id="6e7d0-556">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-557">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="6e7d0-557">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-558">Уведомление о вставке строки</span><span class="sxs-lookup"><span data-stu-id="6e7d0-558">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-559">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="6e7d0-559">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-560">Привилегии строки</span><span class="sxs-lookup"><span data-stu-id="6e7d0-560">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-561">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="6e7d0-561">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-562">Уведомление о повторной синхронизации строк</span><span class="sxs-lookup"><span data-stu-id="6e7d0-562">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-563">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="6e7d0-563">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-564">Модель потоков строки</span><span class="sxs-lookup"><span data-stu-id="6e7d0-564">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-565">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="6e7d0-565">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-566">Уведомление об отмене строки</span><span class="sxs-lookup"><span data-stu-id="6e7d0-566">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-567">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="6e7d0-567">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-568">Уведомление об отмене строки</span><span class="sxs-lookup"><span data-stu-id="6e7d0-568">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-569">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="6e7d0-569">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-570">Уведомление об отмене строки</span><span class="sxs-lookup"><span data-stu-id="6e7d0-570">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-571">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="6e7d0-571">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-572">Уведомление об обновлении строки</span><span class="sxs-lookup"><span data-stu-id="6e7d0-572">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-573">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="6e7d0-573">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-574">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="6e7d0-574">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-575">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="6e7d0-575">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-576">Уведомление о выпуске Rowset</span><span class="sxs-lookup"><span data-stu-id="6e7d0-576">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-577">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="6e7d0-577">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-578">Прокрутите назад</span><span class="sxs-lookup"><span data-stu-id="6e7d0-578">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-579">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="6e7d0-579">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-580">Курсор сервера</span><span class="sxs-lookup"><span data-stu-id="6e7d0-580">Server Cursor</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-581">DBPROP_SERVERCURSOR</span><span class="sxs-lookup"><span data-stu-id="6e7d0-581">DBPROP_SERVERCURSOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-582">Данные сервера на вставке</span><span class="sxs-lookup"><span data-stu-id="6e7d0-582">Server Data on Insert</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-583">DBPROP_SERVERDATAONINSERT</span><span class="sxs-lookup"><span data-stu-id="6e7d0-583">DBPROP_SERVERDATAONINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-584">Пропустить удаленные закладки</span><span class="sxs-lookup"><span data-stu-id="6e7d0-584">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-585">DBPROP_BOOKMARKSKIP</span><span class="sxs-lookup"><span data-stu-id="6e7d0-585">DBPROP_BOOKMARKSKIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-586">Удостоверение Strong Row</span><span class="sxs-lookup"><span data-stu-id="6e7d0-586">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-587">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="6e7d0-587">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-588">Updatability</span><span class="sxs-lookup"><span data-stu-id="6e7d0-588">Updatability</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-589">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="6e7d0-589">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-590">Использование закладок</span><span class="sxs-lookup"><span data-stu-id="6e7d0-590">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-591">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="6e7d0-591">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e7d0-592">Корень XML</span><span class="sxs-lookup"><span data-stu-id="6e7d0-592">XML Root</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-593">SSPROP_STREAM_XMLROOT</span><span class="sxs-lookup"><span data-stu-id="6e7d0-593">SSPROP_STREAM_XMLROOT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e7d0-594">XSL</span><span class="sxs-lookup"><span data-stu-id="6e7d0-594">XSL</span></span></p></td>
<td><p><span data-ttu-id="6e7d0-595">SSPROP_STREAM_XSL</span><span class="sxs-lookup"><span data-stu-id="6e7d0-595">SSPROP_STREAM_XSL</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6e7d0-596">Подробные сведения о реализации и функциональные сведения о поставщике Microsoft SQL Server OLE DB обратитесь к поставщику OLE DB для SQL Server документации в разделе OLE DB SDK MDAC.</span><span class="sxs-lookup"><span data-stu-id="6e7d0-596">For specific implementation details and functional information about the Microsoft SQL Server OLE DB Provider, consult the OLE DB Provider for SQL Server documentation in the OLE DB section of the MDAC SDK.</span></span>

