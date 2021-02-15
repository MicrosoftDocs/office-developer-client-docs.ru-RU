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
# <a name="microsoft-ole-db-provider-for-sql-server"></a><span data-ttu-id="c45bf-102">Поставщик Microsoft OLE DB для SQL Server</span><span class="sxs-lookup"><span data-stu-id="c45bf-102">Microsoft OLE DB Provider for SQL Server</span></span>


<span data-ttu-id="c45bf-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c45bf-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c45bf-104">Поставщик Microsoft OLE DB для SQL Server, SQLOLEDB, позволяет ADO получать доступ к Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c45bf-104">The Microsoft OLE DB Provider for SQL Server, SQLOLEDB, allows ADO to access Microsoft SQL Server.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="c45bf-105">Параметры строки подключения</span><span class="sxs-lookup"><span data-stu-id="c45bf-105">Connection String Parameters</span></span>

<span data-ttu-id="c45bf-106">Чтобы подключиться к этому поставщику, установите для аргумента *Provider* свойство [ConnectionString:](connectionstring-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="c45bf-106">To connect to this provider, set the *Provider* argument to the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```sql 
 
SQLOLEDB 
```

<span data-ttu-id="c45bf-107">Это значение также можно установить или прочитать с помощью свойства [Provider.](provider-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="c45bf-107">This value can also be set or read using the [Provider](provider-property-ado.md) property.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="c45bf-108">Типичная строка подключения</span><span class="sxs-lookup"><span data-stu-id="c45bf-108">Typical Connection String</span></span>

<span data-ttu-id="c45bf-109">Типичная строка подключения для этого поставщика:</span><span class="sxs-lookup"><span data-stu-id="c45bf-109">A typical connection string for this provider is:</span></span>

```sql 
 
"Provider=SQLOLEDB;Data Source=serverName;" 
Initial Catalog=databaseName; 
User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="c45bf-110">Строка состоит из таких ключевых слов:</span><span class="sxs-lookup"><span data-stu-id="c45bf-110">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c45bf-111">Ключевое слово</span><span class="sxs-lookup"><span data-stu-id="c45bf-111">Keyword</span></span></p></th>
<th><p><span data-ttu-id="c45bf-112">Описание</span><span class="sxs-lookup"><span data-stu-id="c45bf-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-113"><strong>Поставщик</strong></span><span class="sxs-lookup"><span data-stu-id="c45bf-113"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="c45bf-114">Указывает поставщика OLE DB для SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c45bf-114">Specifies the OLE DB Provider for SQL Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-115"><strong>Источник данных</strong> или <strong>сервер</strong></span><span class="sxs-lookup"><span data-stu-id="c45bf-115"><strong>Data Source</strong> or <strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c45bf-116">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="c45bf-116">Specifies the name of a server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-117"><strong>Начальный каталог</strong> или база <strong>данных</strong></span><span class="sxs-lookup"><span data-stu-id="c45bf-117"><strong>Initial Catalog</strong> or <strong>Database</strong></span></span></p></td>
<td><p><span data-ttu-id="c45bf-118">Указывает имя базы данных на сервере.</span><span class="sxs-lookup"><span data-stu-id="c45bf-118">Specifies the name of a database on the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-119"><strong>ИД пользователя</strong> или <strong>UID</strong></span><span class="sxs-lookup"><span data-stu-id="c45bf-119"><strong>User ID</strong> or <strong>uid</strong></span></span></p></td>
<td><p><span data-ttu-id="c45bf-120">Указывает имя пользователя (для SQL Server проверки подлинности).</span><span class="sxs-lookup"><span data-stu-id="c45bf-120">Specifies the user name (for SQL Server Authentication).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-121"><strong>Пароль или</strong> <strong>pwd</strong></span><span class="sxs-lookup"><span data-stu-id="c45bf-121"><strong>Password</strong> or <strong>pwd</strong></span></span></p></td>
<td><p><span data-ttu-id="c45bf-122">Указывает пароль пользователя (для SQL Server проверки подлинности).</span><span class="sxs-lookup"><span data-stu-id="c45bf-122">Specifies the user password (for SQL Server Authentication).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-connection-parameters"></a><span data-ttu-id="c45bf-123">Provider-Specific подключения</span><span class="sxs-lookup"><span data-stu-id="c45bf-123">Provider-Specific Connection Parameters</span></span>

<span data-ttu-id="c45bf-124">Поставщик поддерживает несколько параметров подключения для конкретного поставщика в дополнение к параметрам, определенным aDO.</span><span class="sxs-lookup"><span data-stu-id="c45bf-124">The provider supports several provider-specific connection parameters in addition to those defined by ADO.</span></span> <span data-ttu-id="c45bf-125">Как и в свойствах подключения ADO, эти свойства для конкретного поставщика [](connection-object-ado.md) можно установить с помощью коллекции [свойств](properties-collection-ado.md) подключения или как часть **ConnectionString.**</span><span class="sxs-lookup"><span data-stu-id="c45bf-125">As with the ADO connection properties, these provider-specific properties can be set via the [Properties](properties-collection-ado.md) collection of a [Connection](connection-object-ado.md) or can be set as part of the **ConnectionString**.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c45bf-126">Параметр</span><span class="sxs-lookup"><span data-stu-id="c45bf-126">Parameter</span></span></p></th>
<th><p><span data-ttu-id="c45bf-127">Описание</span><span class="sxs-lookup"><span data-stu-id="c45bf-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-128">Trusted_Connection</span><span class="sxs-lookup"><span data-stu-id="c45bf-128">Trusted_Connection</span></span></p></td>
<td><p><span data-ttu-id="c45bf-129">Указывает режим проверки подлинности пользователя.</span><span class="sxs-lookup"><span data-stu-id="c45bf-129">Indicates the user authentication mode.</span></span> <span data-ttu-id="c45bf-130">Для этого можно установить <strong>"Да" или</strong> <strong>"Нет"</strong>.</span><span class="sxs-lookup"><span data-stu-id="c45bf-130">This can be set to <strong>Yes</strong> or <strong>No</strong>.</span></span> <span data-ttu-id="c45bf-131">По умолчанию выбрано <strong>Нет</strong>.</span><span class="sxs-lookup"><span data-stu-id="c45bf-131">The default value is <strong>No</strong>.</span></span> <span data-ttu-id="c45bf-132">Если этому свойству задано значение <strong>"Да",</strong>то SQLOLEDB использует режим проверки подлинности Microsoft Windows NT для авторизации доступа пользователей к базе данных SQL Server, указанной значениями свойств <strong>Location</strong> и <a href="datasource-property-ado.md">Datasource.</a></span><span class="sxs-lookup"><span data-stu-id="c45bf-132">If this property is set to <strong>Yes</strong>, then SQLOLEDB uses Microsoft Windows NT Authentication Mode to authorize user access to the SQL Server database specified by the <strong>Location</strong> and <a href="datasource-property-ado.md">Datasource</a> property values.</span></span> <span data-ttu-id="c45bf-133">Если для этого свойства установлено свойство <strong>No,</strong>SQLOLEDB использует смешанный режим для авторизации доступа пользователей к SQL Server базе данных.</span><span class="sxs-lookup"><span data-stu-id="c45bf-133">If this property is set to <strong>No</strong>, then SQLOLEDB uses Mixed Mode to authorize user access to the SQL Server database.</span></span> <span data-ttu-id="c45bf-134">Имя SQL Server и пароль указаны в свойствах <strong>"ИД</strong> пользователя" <strong>и "Пароль".</strong></span><span class="sxs-lookup"><span data-stu-id="c45bf-134">The SQL Server login and password are specified in the <strong>User Id</strong> and <strong>Password</strong> properties.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-135">Текущий язык</span><span class="sxs-lookup"><span data-stu-id="c45bf-135">Current Language</span></span></p></td>
<td><p><span data-ttu-id="c45bf-136">Указывает имя SQL Server языка.</span><span class="sxs-lookup"><span data-stu-id="c45bf-136">Indicates a SQL Server language name.</span></span> <span data-ttu-id="c45bf-137">Определяет язык, используемый для выбора и форматирования системных сообщений.</span><span class="sxs-lookup"><span data-stu-id="c45bf-137">Identifies the language used for system message selection and formatting.</span></span> <span data-ttu-id="c45bf-138">Язык должен быть установлен на SQL Server, в противном случае открытие подключения не удастся.</span><span class="sxs-lookup"><span data-stu-id="c45bf-138">The language must be installed on the SQL Server, otherwise opening the connection will fail.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-139">Сетевой адрес</span><span class="sxs-lookup"><span data-stu-id="c45bf-139">Network Address</span></span></p></td>
<td><p><span data-ttu-id="c45bf-140">Указывает сетевой адрес SQL Server, указанного <strong>свойством Location.</strong></span><span class="sxs-lookup"><span data-stu-id="c45bf-140">Indicates the network address of the SQL Server specified by the <strong>Location</strong> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-141">Библиотека сети</span><span class="sxs-lookup"><span data-stu-id="c45bf-141">Network Library</span></span></p></td>
<td><p><span data-ttu-id="c45bf-142">Указывает имя сетевой библиотеки (библиотек динамической связи), используемой для связи с SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c45bf-142">Indicates the name of the network library (dynamic-link libraries) used to communicate with the SQL Server.</span></span> <span data-ttu-id="c45bf-143">Имя не должно включать путь или расширение DLL-файла.</span><span class="sxs-lookup"><span data-stu-id="c45bf-143">The name should not include the path or the .dll file name extension.</span></span> <span data-ttu-id="c45bf-144">Значение по умолчанию предоставляется конфигурацией SQL Server клиента.</span><span class="sxs-lookup"><span data-stu-id="c45bf-144">The default is provided by the SQL Server client configuration.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-145">Процедура использования для подготовки</span><span class="sxs-lookup"><span data-stu-id="c45bf-145">Use Procedure for Prepare</span></span></p></td>
<td><p><span data-ttu-id="c45bf-146">Определяет, создает ли SQL Server временные хранимые процедуры при подготовке команд (свойство <strong>Prepared).</strong></span><span class="sxs-lookup"><span data-stu-id="c45bf-146">Determines whether SQL Server creates temporary stored procedures when Commands are prepared (by the <strong>Prepared</strong> property).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-147">Автоматический перевод</span><span class="sxs-lookup"><span data-stu-id="c45bf-147">Auto Translate</span></span></p></td>
<td><p><span data-ttu-id="c45bf-148">Указывает, преобразуются ли символы OEM/ANSI.</span><span class="sxs-lookup"><span data-stu-id="c45bf-148">Indicates whether OEM/ANSI characters are converted.</span></span> <span data-ttu-id="c45bf-149">Для этого свойства можно установить true <strong>или</strong> <strong>False.</strong></span><span class="sxs-lookup"><span data-stu-id="c45bf-149">This property can be set to <strong>True</strong> or <strong>False</strong>.</span></span> <span data-ttu-id="c45bf-150">Значение по умолчанию — <strong>True</strong>.</span><span class="sxs-lookup"><span data-stu-id="c45bf-150">The default value is <strong>True</strong>.</span></span> <span data-ttu-id="c45bf-151">Если для этого свойства установлено <strong>true,</strong>то SQLOLEDB выполняет преобразование символов OEM/ANSI, когда многобайтовая строка символов извлекается или отправляется в SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c45bf-151">If this property is set to <strong>True</strong>, then SQLOLEDB performs OEM/ANSI character conversion when multi-byte character strings are retrieved from, or sent to, the SQL Server.</span></span> <span data-ttu-id="c45bf-152">Если для этого свойства установлено <strong>false,</strong>то SQLOLEDB не выполняет преобразование символов OEM/ANSI для многобайтных данных строки символов.</span><span class="sxs-lookup"><span data-stu-id="c45bf-152">If this property is set to <strong>False</strong>, then SQLOLEDB does not perform OEM/ANSI character conversion on multi-byte character string data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-153">Размер пакета</span><span class="sxs-lookup"><span data-stu-id="c45bf-153">Packet Size</span></span></p></td>
<td><p><span data-ttu-id="c45bf-154">Указывает размер сетевого пакета в ветвях.</span><span class="sxs-lookup"><span data-stu-id="c45bf-154">Indicates a network packet size in bytes.</span></span> <span data-ttu-id="c45bf-155">Значение свойства размера пакета должно быть от 512 до 32767.</span><span class="sxs-lookup"><span data-stu-id="c45bf-155">The packet size property value must be between 512 and 32767.</span></span> <span data-ttu-id="c45bf-156">По умолчанию сетевой пакет SQLOLEDB имеет размер 4096.</span><span class="sxs-lookup"><span data-stu-id="c45bf-156">The default SQLOLEDB network packet size is 4096.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-157">Имя приложения</span><span class="sxs-lookup"><span data-stu-id="c45bf-157">Application Name</span></span></p></td>
<td><p><span data-ttu-id="c45bf-158">Указывает имя клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="c45bf-158">Indicates the client application name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-159">ИД рабочей станции</span><span class="sxs-lookup"><span data-stu-id="c45bf-159">Workstation ID</span></span></p></td>
<td><p><span data-ttu-id="c45bf-160">Строка, идентифицирующие рабочие станции.</span><span class="sxs-lookup"><span data-stu-id="c45bf-160">A string identifying the workstation.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-object-usage"></a><span data-ttu-id="c45bf-161">Использование объекта Command</span><span class="sxs-lookup"><span data-stu-id="c45bf-161">Command Object Usage</span></span>

<span data-ttu-id="c45bf-162">SQLOLEDB принимает объединение ODBC, ANSI и SQL Server Transact-SQL в качестве допустимого синтаксиса.</span><span class="sxs-lookup"><span data-stu-id="c45bf-162">SQLOLEDB accepts an amalgam of ODBC, ANSI, and SQL Server-specific Transact-SQL as valid syntax.</span></span> <span data-ttu-id="c45bf-163">Например, следующая SQL использует escape-последовательность ODBC SQL для указания функции строки LCASE:</span><span class="sxs-lookup"><span data-stu-id="c45bf-163">For example, the following SQL statement uses an ODBC SQL escape sequence to specify the LCASE string function:</span></span>

```sql 
 
SELECT customerid={fn LCASE(CustomerID)} FROM Customers 
```

<span data-ttu-id="c45bf-164">LCASE возвращает строку символов, преобразуя все символы верхнего регистра в их эквиваленты в нижнем регистре.</span><span class="sxs-lookup"><span data-stu-id="c45bf-164">LCASE returns a character string, converting all uppercase characters to their lowercase equivalents.</span></span> <span data-ttu-id="c45bf-165">Строковая функция SQL ANSI LOWER выполняет ту же операцию, поэтому следующий SQL является anSI-эквивалентом представленного выше заявления ODBC:</span><span class="sxs-lookup"><span data-stu-id="c45bf-165">The ANSI SQL string function LOWER performs the same operation, so the following SQL statement is an ANSI equivalent to the ODBC statement presented above:</span></span>

```sql
 
SELECT customerid=LOWER(CustomerID) FROM Customers 
```

<span data-ttu-id="c45bf-166">SQLOLEDB успешно обрабатывает любой из форм заявления, если он указан в качестве текста для команды.</span><span class="sxs-lookup"><span data-stu-id="c45bf-166">SQLOLEDB successfully processes either form of the statement when specified as text for a command.</span></span>

## <a name="stored-procedures"></a><span data-ttu-id="c45bf-167">Хранимые процедуры</span><span class="sxs-lookup"><span data-stu-id="c45bf-167">Stored Procedures</span></span>

<span data-ttu-id="c45bf-168">При выполнении SQL Server хранимой процедуры с помощью команды SQLOLEDB используйте последовательность escape-вызовов процедуры ODBC в тексте команды.</span><span class="sxs-lookup"><span data-stu-id="c45bf-168">When executing a SQL Server stored procedure using a SQLOLEDB command, use the ODBC procedure call escape sequence in the command text.</span></span> <span data-ttu-id="c45bf-169">Затем SQLOLEDB использует механизм удаленного вызова процедуры SQL Server для оптимизации обработки команд.</span><span class="sxs-lookup"><span data-stu-id="c45bf-169">SQLOLEDB then uses the remote procedure call mechanism of SQL Server to optimize command processing.</span></span> <span data-ttu-id="c45bf-170">Например, следующий SQL ODBC является предпочтительным текстом команды в форме Transact-SQL:</span><span class="sxs-lookup"><span data-stu-id="c45bf-170">For example, the following ODBC SQL statement is the preferred command text over the Transact-SQL form:</span></span>

## <a name="odbc-sql"></a><span data-ttu-id="c45bf-171">ODBC SQL</span><span class="sxs-lookup"><span data-stu-id="c45bf-171">ODBC SQL</span></span>

```sql 
 
{call SalesByCategory('Produce', '1995')} 
```

## <a name="transact-sql"></a><span data-ttu-id="c45bf-172">Transact-SQL</span><span class="sxs-lookup"><span data-stu-id="c45bf-172">Transact-SQL</span></span>

```sql 
 
EXECUTE SalesByCategory 'Produce', '1995' 
```

## <a name="recordset-behavior"></a><span data-ttu-id="c45bf-173">Поведение наборов записей</span><span class="sxs-lookup"><span data-stu-id="c45bf-173">Recordset Behavior</span></span>

<span data-ttu-id="c45bf-174">SQLOLEDB не может использовать SQL Server для поддержки нескольких результатов, созданных множеством команд.</span><span class="sxs-lookup"><span data-stu-id="c45bf-174">SQLOLEDB cannot use SQL Server cursors to support the multiple-result generated by many commands.</span></span> <span data-ttu-id="c45bf-175">Если потребитель запрашивает набор записей, требующий поддержки SQL Server курсора, возникает ошибка, если в результате использованного текста команды создается несколько наборов записей.</span><span class="sxs-lookup"><span data-stu-id="c45bf-175">If a consumer requests a recordset requiring SQL Server cursor support, an error occurs if the command text used generates more than a single recordset as its result.</span></span>

<span data-ttu-id="c45bf-176">Прокручиваемые записи SQLOLEDB поддерживаются SQL Server курсоров.</span><span class="sxs-lookup"><span data-stu-id="c45bf-176">Scrollable SQLOLEDB recordsets are supported by SQL Server cursors.</span></span> <span data-ttu-id="c45bf-177">SQL Server накладывает ограничения на курсоры, которые чувствительны к изменениям, внесенным другими пользователями базы данных.</span><span class="sxs-lookup"><span data-stu-id="c45bf-177">SQL Server imposes limitations on cursors that are sensitive to changes made by other users of the database.</span></span> <span data-ttu-id="c45bf-178">В частности, невозможно указать строки в некоторых курсорах, и попытка создать набор записей с помощью команды, содержащей SQL ORDER BY, может привести к сбойу.</span><span class="sxs-lookup"><span data-stu-id="c45bf-178">Specifically, the rows in some cursors cannot be ordered, and attempting to create a recordset using a command containing an SQL ORDER BY clause can fail.</span></span>

## <a name="dynamic-properties"></a><span data-ttu-id="c45bf-179">Динамические свойства</span><span class="sxs-lookup"><span data-stu-id="c45bf-179">Dynamic Properties</span></span>

<span data-ttu-id="c45bf-180">Поставщик Microsoft OLE DB для SQL Server вставляет несколько динамических свойств в коллекцию **свойств** неподтвершенных объектов [Connection,](connection-object-ado.md) [Recordset](recordset-object-ado.md)и [Command.](command-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="c45bf-180">The Microsoft OLE DB Provider for SQL Server inserts several dynamic properties into the **Properties** collection of the unopened [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md), and [Command](command-object-ado.md) objects.</span></span>

<span data-ttu-id="c45bf-181">Следующие таблицы являются перекрестным индексом имен ADO и OLE DB для каждого динамического свойства.</span><span class="sxs-lookup"><span data-stu-id="c45bf-181">The following tables are a cross-index of the ADO and OLE DB names for each dynamic property.</span></span> <span data-ttu-id="c45bf-182">В справочнике программиста OLE DB имя свойства ADO обозначается термином "Description".</span><span class="sxs-lookup"><span data-stu-id="c45bf-182">The OLE DB Programmer's Reference refers to an ADO property name by the term "Description."</span></span> <span data-ttu-id="c45bf-183">Дополнительные сведения об этих свойствах можно найти в справочнике программиста OLE DB.</span><span class="sxs-lookup"><span data-stu-id="c45bf-183">You can find more information about these properties in the OLE DB Programmer's Reference.</span></span> <span data-ttu-id="c45bf-184">Найди имя свойства OLE DB в индексе или см. приложение C. Свойства OLE DB.</span><span class="sxs-lookup"><span data-stu-id="c45bf-184">Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span></span>

## <a name="connection-dynamic-properties"></a><span data-ttu-id="c45bf-185">Динамические свойства подключения</span><span class="sxs-lookup"><span data-stu-id="c45bf-185">Connection Dynamic Properties</span></span>

<span data-ttu-id="c45bf-186">Следующие свойства добавляются в коллекцию  свойств объекта **Connection.**</span><span class="sxs-lookup"><span data-stu-id="c45bf-186">The following properties are added to the **Connection** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c45bf-187">ADO Property Name</span><span class="sxs-lookup"><span data-stu-id="c45bf-187">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="c45bf-188">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="c45bf-188">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-189">Активные сеансы</span><span class="sxs-lookup"><span data-stu-id="c45bf-189">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="c45bf-190">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="c45bf-190">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-191">Asynchable Abort</span><span class="sxs-lookup"><span data-stu-id="c45bf-191">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="c45bf-192">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="c45bf-192">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-193">Asynchable Commit</span><span class="sxs-lookup"><span data-stu-id="c45bf-193">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="c45bf-194">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="c45bf-194">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-195">Уровни изоляции автозафикса</span><span class="sxs-lookup"><span data-stu-id="c45bf-195">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="c45bf-196">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="c45bf-196">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-197">Расположение каталога</span><span class="sxs-lookup"><span data-stu-id="c45bf-197">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="c45bf-198">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="c45bf-198">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-199">Термин каталога</span><span class="sxs-lookup"><span data-stu-id="c45bf-199">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="c45bf-200">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="c45bf-200">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-201">Определение столбца</span><span class="sxs-lookup"><span data-stu-id="c45bf-201">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="c45bf-202">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="c45bf-202">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-203">Время подключения</span><span class="sxs-lookup"><span data-stu-id="c45bf-203">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="c45bf-204">DBPROP_INIT_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="c45bf-204">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-205">Текущий каталог</span><span class="sxs-lookup"><span data-stu-id="c45bf-205">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="c45bf-206">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="c45bf-206">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-207">Источник данных</span><span class="sxs-lookup"><span data-stu-id="c45bf-207">Data Source</span></span></p></td>
<td><p><span data-ttu-id="c45bf-208">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="c45bf-208">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-209">Имя источника данных</span><span class="sxs-lookup"><span data-stu-id="c45bf-209">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="c45bf-210">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="c45bf-210">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-211">Потоковая модель объектов источника данных</span><span class="sxs-lookup"><span data-stu-id="c45bf-211">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="c45bf-212">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="c45bf-212">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-213">DBMS Name</span><span class="sxs-lookup"><span data-stu-id="c45bf-213">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="c45bf-214">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="c45bf-214">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-215">Версия DBMS</span><span class="sxs-lookup"><span data-stu-id="c45bf-215">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="c45bf-216">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="c45bf-216">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-217">Расширенные свойства</span><span class="sxs-lookup"><span data-stu-id="c45bf-217">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="c45bf-218">DBPROP_INIT_PROVIDERSTRING</span><span class="sxs-lookup"><span data-stu-id="c45bf-218">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-219">GROUP BY Support</span><span class="sxs-lookup"><span data-stu-id="c45bf-219">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="c45bf-220">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="c45bf-220">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-221">Поддержка разнородных таблиц</span><span class="sxs-lookup"><span data-stu-id="c45bf-221">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="c45bf-222">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="c45bf-222">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-223">Чувствительность к делу идентификатора</span><span class="sxs-lookup"><span data-stu-id="c45bf-223">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="c45bf-224">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="c45bf-224">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-225">Начальный каталог</span><span class="sxs-lookup"><span data-stu-id="c45bf-225">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="c45bf-226">DBPROP_INIT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c45bf-226">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-227">Уровни изоляции</span><span class="sxs-lookup"><span data-stu-id="c45bf-227">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="c45bf-228">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="c45bf-228">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-229">Хранение изоляции</span><span class="sxs-lookup"><span data-stu-id="c45bf-229">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="c45bf-230">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="c45bf-230">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-231">Код локализовки</span><span class="sxs-lookup"><span data-stu-id="c45bf-231">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="c45bf-232">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="c45bf-232">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-233">Максимальный размер индекса</span><span class="sxs-lookup"><span data-stu-id="c45bf-233">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="c45bf-234">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="c45bf-234">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-235">Максимальный размер строки</span><span class="sxs-lookup"><span data-stu-id="c45bf-235">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="c45bf-236">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="c45bf-236">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-237">Максимальный размер строки включает BLOB</span><span class="sxs-lookup"><span data-stu-id="c45bf-237">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="c45bf-238">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="c45bf-238">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-239">Максимальное число таблиц в SELECT</span><span class="sxs-lookup"><span data-stu-id="c45bf-239">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="c45bf-240">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="c45bf-240">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-241">Несколько наборов параметров</span><span class="sxs-lookup"><span data-stu-id="c45bf-241">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="c45bf-242">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="c45bf-242">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-243">Несколько результатов</span><span class="sxs-lookup"><span data-stu-id="c45bf-243">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="c45bf-244">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="c45bf-244">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-245">Несколько объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="c45bf-245">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="c45bf-246">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="c45bf-246">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-247">Обновление с несколькими таблицами</span><span class="sxs-lookup"><span data-stu-id="c45bf-247">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="c45bf-248">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="c45bf-248">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-249">Порядок оценки NULL</span><span class="sxs-lookup"><span data-stu-id="c45bf-249">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="c45bf-250">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="c45bf-250">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-251">Поведение при конкатенации NULL</span><span class="sxs-lookup"><span data-stu-id="c45bf-251">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="c45bf-252">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="c45bf-252">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-253">Версия OLE DB</span><span class="sxs-lookup"><span data-stu-id="c45bf-253">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="c45bf-254">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="c45bf-254">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-255">Поддержка объектов OLE</span><span class="sxs-lookup"><span data-stu-id="c45bf-255">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="c45bf-256">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="c45bf-256">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-257">Поддержка открытого наборов строк</span><span class="sxs-lookup"><span data-stu-id="c45bf-257">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="c45bf-258">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="c45bf-258">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-259">ORDER BY Columns in Select List</span><span class="sxs-lookup"><span data-stu-id="c45bf-259">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="c45bf-260">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="c45bf-260">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-261">Доступность выходных параметров</span><span class="sxs-lookup"><span data-stu-id="c45bf-261">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="c45bf-262">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="c45bf-262">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-263">Pass By Ref Accessors</span><span class="sxs-lookup"><span data-stu-id="c45bf-263">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="c45bf-264">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="c45bf-264">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-265">Password</span><span class="sxs-lookup"><span data-stu-id="c45bf-265">Password</span></span></p></td>
<td><p><span data-ttu-id="c45bf-266">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="c45bf-266">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-267">Сохранить сведения о безопасности</span><span class="sxs-lookup"><span data-stu-id="c45bf-267">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="c45bf-268">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span><span class="sxs-lookup"><span data-stu-id="c45bf-268">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-269">Тип сохраняемого ИД</span><span class="sxs-lookup"><span data-stu-id="c45bf-269">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="c45bf-270">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="c45bf-270">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-271">Подготовка поведения для отменить</span><span class="sxs-lookup"><span data-stu-id="c45bf-271">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="c45bf-272">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="c45bf-272">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-273">Подготовка поведения фиксации</span><span class="sxs-lookup"><span data-stu-id="c45bf-273">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="c45bf-274">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="c45bf-274">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-275">Термин процедуры</span><span class="sxs-lookup"><span data-stu-id="c45bf-275">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="c45bf-276">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="c45bf-276">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-277">Prompt</span><span class="sxs-lookup"><span data-stu-id="c45bf-277">Prompt</span></span></p></td>
<td><p><span data-ttu-id="c45bf-278">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="c45bf-278">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-279">Имя поставщика</span><span class="sxs-lookup"><span data-stu-id="c45bf-279">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="c45bf-280">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="c45bf-280">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-281">Имя поставщика</span><span class="sxs-lookup"><span data-stu-id="c45bf-281">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="c45bf-282">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="c45bf-282">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-283">Версия поставщика</span><span class="sxs-lookup"><span data-stu-id="c45bf-283">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="c45bf-284">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="c45bf-284">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-285">Read-Only данных</span><span class="sxs-lookup"><span data-stu-id="c45bf-285">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="c45bf-286">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="c45bf-286">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-287">Преобразование наборов строк в команде</span><span class="sxs-lookup"><span data-stu-id="c45bf-287">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="c45bf-288">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="c45bf-288">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-289">Термин схемы</span><span class="sxs-lookup"><span data-stu-id="c45bf-289">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="c45bf-290">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="c45bf-290">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-291">Использование схемы</span><span class="sxs-lookup"><span data-stu-id="c45bf-291">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="c45bf-292">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="c45bf-292">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-293">SQL поддержки</span><span class="sxs-lookup"><span data-stu-id="c45bf-293">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="c45bf-294">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="c45bf-294">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-295">Структурированное хранилище</span><span class="sxs-lookup"><span data-stu-id="c45bf-295">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="c45bf-296">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="c45bf-296">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-297">Поддержка ветвей</span><span class="sxs-lookup"><span data-stu-id="c45bf-297">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="c45bf-298">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="c45bf-298">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-299">Table Term</span><span class="sxs-lookup"><span data-stu-id="c45bf-299">Table Term</span></span></p></td>
<td><p><span data-ttu-id="c45bf-300">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="c45bf-300">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-301">DDL транзакции</span><span class="sxs-lookup"><span data-stu-id="c45bf-301">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="c45bf-302">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="c45bf-302">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-303">Идентификатор пользователя</span><span class="sxs-lookup"><span data-stu-id="c45bf-303">User ID</span></span></p></td>
<td><p><span data-ttu-id="c45bf-304">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="c45bf-304">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-305">имя пользователя;</span><span class="sxs-lookup"><span data-stu-id="c45bf-305">User Name</span></span></p></td>
<td><p><span data-ttu-id="c45bf-306">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="c45bf-306">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-307">Окне Окне</span><span class="sxs-lookup"><span data-stu-id="c45bf-307">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="c45bf-308">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="c45bf-308">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a><span data-ttu-id="c45bf-309">Динамические свойства recordset</span><span class="sxs-lookup"><span data-stu-id="c45bf-309">Recordset Dynamic Properties</span></span>

<span data-ttu-id="c45bf-310">Следующие свойства добавляются в коллекцию **свойств** объекта **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="c45bf-310">The following properties are added to the **Recordset** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c45bf-311">ADO Property Name</span><span class="sxs-lookup"><span data-stu-id="c45bf-311">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="c45bf-312">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="c45bf-312">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-313">Порядок доступа</span><span class="sxs-lookup"><span data-stu-id="c45bf-313">Access Order</span></span></p></td>
<td><p><span data-ttu-id="c45bf-314">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="c45bf-314">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-315">Блокировка объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="c45bf-315">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="c45bf-316">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="c45bf-316">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-317">Тип закладки</span><span class="sxs-lookup"><span data-stu-id="c45bf-317">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="c45bf-318">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="c45bf-318">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-319">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="c45bf-319">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="c45bf-320">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="c45bf-320">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-321">Изменение вставленных строк</span><span class="sxs-lookup"><span data-stu-id="c45bf-321">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="c45bf-322">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="c45bf-322">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-323">Привилегии столбца</span><span class="sxs-lookup"><span data-stu-id="c45bf-323">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="c45bf-324">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="c45bf-324">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-325">Уведомление о наборе столбцов</span><span class="sxs-lookup"><span data-stu-id="c45bf-325">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="c45bf-326">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="c45bf-326">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-327">Время простоя команды</span><span class="sxs-lookup"><span data-stu-id="c45bf-327">Command Time Out</span></span></p></td>
<td><p><span data-ttu-id="c45bf-328">DBPROP_COMMANDTIMEOUT</span><span class="sxs-lookup"><span data-stu-id="c45bf-328">DBPROP_COMMANDTIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-329">Отложить столбец</span><span class="sxs-lookup"><span data-stu-id="c45bf-329">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="c45bf-330">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="c45bf-330">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-331">Задержка обновлений объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="c45bf-331">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="c45bf-332">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="c45bf-332">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-333">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="c45bf-333">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="c45bf-334">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="c45bf-334">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-335">Строки удержания</span><span class="sxs-lookup"><span data-stu-id="c45bf-335">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="c45bf-336">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="c45bf-336">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-337">IAccessor</span><span class="sxs-lookup"><span data-stu-id="c45bf-337">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="c45bf-338">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="c45bf-338">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-339">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="c45bf-339">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="c45bf-340">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="c45bf-340">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-341">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="c45bf-341">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="c45bf-342">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="c45bf-342">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-343">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="c45bf-343">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="c45bf-344">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="c45bf-344">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-345">IConvertType</span><span class="sxs-lookup"><span data-stu-id="c45bf-345">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="c45bf-346">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="c45bf-346">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-347">Строки Immobile</span><span class="sxs-lookup"><span data-stu-id="c45bf-347">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="c45bf-348">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="c45bf-348">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-349">IRowset</span><span class="sxs-lookup"><span data-stu-id="c45bf-349">IRowset</span></span></p></td>
<td><p><span data-ttu-id="c45bf-350">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="c45bf-350">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-351">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="c45bf-351">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="c45bf-352">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="c45bf-352">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-353">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="c45bf-353">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="c45bf-354">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="c45bf-354">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-355">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="c45bf-355">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="c45bf-356">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="c45bf-356">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-357">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="c45bf-357">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="c45bf-358">DBPROP_IRowsestLocate</span><span class="sxs-lookup"><span data-stu-id="c45bf-358">DBPROP_IRowsestLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-359">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="c45bf-359">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-360">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="c45bf-360">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="c45bf-361">DBPROP_IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="c45bf-361">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-362">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="c45bf-362">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="c45bf-363">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="c45bf-363">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-364">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="c45bf-364">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="c45bf-365">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="c45bf-365">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-366">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="c45bf-366">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="c45bf-367">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="c45bf-367">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-368">Литеральные закладки</span><span class="sxs-lookup"><span data-stu-id="c45bf-368">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="c45bf-369">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="c45bf-369">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-370">Идентификатор строки литералов</span><span class="sxs-lookup"><span data-stu-id="c45bf-370">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="c45bf-371">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="c45bf-371">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-372">Максимальное число открытых строк</span><span class="sxs-lookup"><span data-stu-id="c45bf-372">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="c45bf-373">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="c45bf-373">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-374">Максимальное число ожидающих строк</span><span class="sxs-lookup"><span data-stu-id="c45bf-374">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="c45bf-375">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="c45bf-375">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-376">Максимальное число строк</span><span class="sxs-lookup"><span data-stu-id="c45bf-376">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="c45bf-377">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="c45bf-377">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-378">Детализация уведомлений</span><span class="sxs-lookup"><span data-stu-id="c45bf-378">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="c45bf-379">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="c45bf-379">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-380">Этапы уведомлений</span><span class="sxs-lookup"><span data-stu-id="c45bf-380">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="c45bf-381">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="c45bf-381">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-382">Transacted объектов</span><span class="sxs-lookup"><span data-stu-id="c45bf-382">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="c45bf-383">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="c45bf-383">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-384">Видимые изменения других</span><span class="sxs-lookup"><span data-stu-id="c45bf-384">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="c45bf-385">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="c45bf-385">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-386">Видимые вставки других</span><span class="sxs-lookup"><span data-stu-id="c45bf-386">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="c45bf-387">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="c45bf-387">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-388">Собственные изменения, видимые</span><span class="sxs-lookup"><span data-stu-id="c45bf-388">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="c45bf-389">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="c45bf-389">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-390">Собственные вставки видимые</span><span class="sxs-lookup"><span data-stu-id="c45bf-390">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="c45bf-391">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="c45bf-391">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-392">Сохранение при отменить</span><span class="sxs-lookup"><span data-stu-id="c45bf-392">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="c45bf-393">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="c45bf-393">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-394">Сохранение при фиксации</span><span class="sxs-lookup"><span data-stu-id="c45bf-394">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="c45bf-395">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="c45bf-395">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-396">Быстрая перезагрузка</span><span class="sxs-lookup"><span data-stu-id="c45bf-396">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="c45bf-397">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="c45bf-397">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-398">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="c45bf-398">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="c45bf-399">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="c45bf-399">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-400">Удаление удаленных строк</span><span class="sxs-lookup"><span data-stu-id="c45bf-400">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="c45bf-401">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="c45bf-401">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-402">Отчет о нескольких изменениях</span><span class="sxs-lookup"><span data-stu-id="c45bf-402">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="c45bf-403">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="c45bf-403">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-404">Возвращение ожидающих вставки</span><span class="sxs-lookup"><span data-stu-id="c45bf-404">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="c45bf-405">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="c45bf-405">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-406">Уведомление об удалении строки</span><span class="sxs-lookup"><span data-stu-id="c45bf-406">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="c45bf-407">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="c45bf-407">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-408">Уведомление о первом изменении строки</span><span class="sxs-lookup"><span data-stu-id="c45bf-408">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="c45bf-409">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="c45bf-409">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-410">Уведомление о вставке строки</span><span class="sxs-lookup"><span data-stu-id="c45bf-410">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="c45bf-411">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="c45bf-411">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-412">Привилегии строки</span><span class="sxs-lookup"><span data-stu-id="c45bf-412">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="c45bf-413">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="c45bf-413">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-414">Уведомление о повторной синхронизации строк</span><span class="sxs-lookup"><span data-stu-id="c45bf-414">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="c45bf-415">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="c45bf-415">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-416">Модель потоков по строкам</span><span class="sxs-lookup"><span data-stu-id="c45bf-416">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="c45bf-417">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="c45bf-417">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-418">Уведомление об отмене строки</span><span class="sxs-lookup"><span data-stu-id="c45bf-418">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="c45bf-419">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="c45bf-419">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-420">Уведомление об отмене удаления строки</span><span class="sxs-lookup"><span data-stu-id="c45bf-420">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="c45bf-421">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="c45bf-421">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-422">Уведомление об отмене вставки строки</span><span class="sxs-lookup"><span data-stu-id="c45bf-422">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="c45bf-423">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="c45bf-423">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-424">Уведомление об обновлении строки</span><span class="sxs-lookup"><span data-stu-id="c45bf-424">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="c45bf-425">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="c45bf-425">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-426">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="c45bf-426">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="c45bf-427">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="c45bf-427">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-428">Уведомление о выпуске rowset</span><span class="sxs-lookup"><span data-stu-id="c45bf-428">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="c45bf-429">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="c45bf-429">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-430">Прокрутка назад</span><span class="sxs-lookup"><span data-stu-id="c45bf-430">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="c45bf-431">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="c45bf-431">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-432">Курсор сервера</span><span class="sxs-lookup"><span data-stu-id="c45bf-432">Server Cursor</span></span></p></td>
<td><p><span data-ttu-id="c45bf-433">DBPROP_SERVERCURSOR</span><span class="sxs-lookup"><span data-stu-id="c45bf-433">DBPROP_SERVERCURSOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-434">Пропустить удаленные закладки</span><span class="sxs-lookup"><span data-stu-id="c45bf-434">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="c45bf-435">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="c45bf-435">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-436">Удостоверение строки strong</span><span class="sxs-lookup"><span data-stu-id="c45bf-436">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="c45bf-437">DBPROP_STRONGITDENTITY</span><span class="sxs-lookup"><span data-stu-id="c45bf-437">DBPROP_STRONGITDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-438">Уникальные строки</span><span class="sxs-lookup"><span data-stu-id="c45bf-438">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="c45bf-439">DBPROP_UNIQUEROWS</span><span class="sxs-lookup"><span data-stu-id="c45bf-439">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-440">Updatability</span><span class="sxs-lookup"><span data-stu-id="c45bf-440">Updatability</span></span></p></td>
<td><p><span data-ttu-id="c45bf-441">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="c45bf-441">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-442">Использование закладок</span><span class="sxs-lookup"><span data-stu-id="c45bf-442">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="c45bf-443">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="c45bf-443">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a><span data-ttu-id="c45bf-444">Командные динамические свойства</span><span class="sxs-lookup"><span data-stu-id="c45bf-444">Command Dynamic Properties</span></span>

<span data-ttu-id="c45bf-445">Следующие свойства добавляются в  коллекцию **свойств объекта Command.**</span><span class="sxs-lookup"><span data-stu-id="c45bf-445">The following properties are added to the **Command** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c45bf-446">ADO Property Name</span><span class="sxs-lookup"><span data-stu-id="c45bf-446">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="c45bf-447">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="c45bf-447">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-448">Порядок доступа</span><span class="sxs-lookup"><span data-stu-id="c45bf-448">Access Order</span></span></p></td>
<td><p><span data-ttu-id="c45bf-449">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="c45bf-449">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-450">Базовый путь</span><span class="sxs-lookup"><span data-stu-id="c45bf-450">Base Path</span></span></p></td>
<td><p><span data-ttu-id="c45bf-451">SSPROP_STREAM_BASEPATH</span><span class="sxs-lookup"><span data-stu-id="c45bf-451">SSPROP_STREAM_BASEPATH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-452">Блокировка объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="c45bf-452">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="c45bf-453">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="c45bf-453">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-454">Тип закладки</span><span class="sxs-lookup"><span data-stu-id="c45bf-454">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="c45bf-455">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="c45bf-455">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-456">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="c45bf-456">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="c45bf-457">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="c45bf-457">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-458">Изменение вставленных строк</span><span class="sxs-lookup"><span data-stu-id="c45bf-458">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="c45bf-459">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="c45bf-459">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-460">Привилегии столбца</span><span class="sxs-lookup"><span data-stu-id="c45bf-460">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="c45bf-461">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="c45bf-461">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-462">Уведомление о наборе столбцов</span><span class="sxs-lookup"><span data-stu-id="c45bf-462">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="c45bf-463">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="c45bf-463">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-464">Тип контента</span><span class="sxs-lookup"><span data-stu-id="c45bf-464">Content Type</span></span></p></td>
<td><p><span data-ttu-id="c45bf-465">SSPROP_STREAM_CONTENTTYPE</span><span class="sxs-lookup"><span data-stu-id="c45bf-465">SSPROP_STREAM_CONTENTTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-466">Автоматическое извлечение курсора</span><span class="sxs-lookup"><span data-stu-id="c45bf-466">Cursor Auto Fetch</span></span></p></td>
<td><p><span data-ttu-id="c45bf-467">SSPROP_CURSORAUTOFETCH</span><span class="sxs-lookup"><span data-stu-id="c45bf-467">SSPROP_CURSORAUTOFETCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-468">Отложить столбец</span><span class="sxs-lookup"><span data-stu-id="c45bf-468">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="c45bf-469">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="c45bf-469">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-470">Отложить подготовку</span><span class="sxs-lookup"><span data-stu-id="c45bf-470">Defer Prepare</span></span></p></td>
<td><p><span data-ttu-id="c45bf-471">SSPROP_DEFERPREPARE</span><span class="sxs-lookup"><span data-stu-id="c45bf-471">SSPROP_DEFERPREPARE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-472">Задержка обновлений объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="c45bf-472">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="c45bf-473">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="c45bf-473">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-474">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="c45bf-474">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="c45bf-475">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="c45bf-475">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-476">Строки удержания</span><span class="sxs-lookup"><span data-stu-id="c45bf-476">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="c45bf-477">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="c45bf-477">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-478">IAccessor</span><span class="sxs-lookup"><span data-stu-id="c45bf-478">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="c45bf-479">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="c45bf-479">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-480">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="c45bf-480">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="c45bf-481">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="c45bf-481">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-482">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="c45bf-482">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="c45bf-483">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="c45bf-483">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-484">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="c45bf-484">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="c45bf-485">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="c45bf-485">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-486">IConvertType</span><span class="sxs-lookup"><span data-stu-id="c45bf-486">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="c45bf-487">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="c45bf-487">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-488">Строки Immobile</span><span class="sxs-lookup"><span data-stu-id="c45bf-488">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="c45bf-489">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="c45bf-489">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-490">IRowset</span><span class="sxs-lookup"><span data-stu-id="c45bf-490">IRowset</span></span></p></td>
<td><p><span data-ttu-id="c45bf-491">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="c45bf-491">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-492">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="c45bf-492">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="c45bf-493">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="c45bf-493">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-494">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="c45bf-494">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="c45bf-495">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="c45bf-495">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-496">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="c45bf-496">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="c45bf-497">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="c45bf-497">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-498">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="c45bf-498">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="c45bf-499">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="c45bf-499">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-500">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="c45bf-500">IRowsetResynch</span></span></p></td>
<td><p><span data-ttu-id="c45bf-501">DBPROP_IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="c45bf-501">DBPROP_IRowsetResynch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-502">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="c45bf-502">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="c45bf-503">DBPROP_IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="c45bf-503">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-504">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="c45bf-504">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="c45bf-505">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="c45bf-505">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-506">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="c45bf-506">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="c45bf-507">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="c45bf-507">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-508">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="c45bf-508">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="c45bf-509">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="c45bf-509">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-510">Литеральные закладки</span><span class="sxs-lookup"><span data-stu-id="c45bf-510">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="c45bf-511">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="c45bf-511">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-512">Идентификатор строки литералов</span><span class="sxs-lookup"><span data-stu-id="c45bf-512">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="c45bf-513">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="c45bf-513">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-514">Режим блокировки</span><span class="sxs-lookup"><span data-stu-id="c45bf-514">Lock Mode</span></span></p></td>
<td><p><span data-ttu-id="c45bf-515">DBPROP_LOCKMODE</span><span class="sxs-lookup"><span data-stu-id="c45bf-515">DBPROP_LOCKMODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-516">Максимальное число открытых строк</span><span class="sxs-lookup"><span data-stu-id="c45bf-516">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="c45bf-517">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="c45bf-517">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-518">Максимальное число ожидающих строк</span><span class="sxs-lookup"><span data-stu-id="c45bf-518">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="c45bf-519">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="c45bf-519">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-520">Максимальное число строк</span><span class="sxs-lookup"><span data-stu-id="c45bf-520">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="c45bf-521">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="c45bf-521">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-522">Детализация уведомлений</span><span class="sxs-lookup"><span data-stu-id="c45bf-522">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="c45bf-523">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="c45bf-523">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-524">Этапы уведомлений</span><span class="sxs-lookup"><span data-stu-id="c45bf-524">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="c45bf-525">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="c45bf-525">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-526">Transacted объектов</span><span class="sxs-lookup"><span data-stu-id="c45bf-526">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="c45bf-527">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="c45bf-527">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-528">Видимые изменения других</span><span class="sxs-lookup"><span data-stu-id="c45bf-528">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="c45bf-529">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="c45bf-529">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-530">Видимые вставки других</span><span class="sxs-lookup"><span data-stu-id="c45bf-530">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="c45bf-531">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="c45bf-531">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-532">Свойство output Encoding</span><span class="sxs-lookup"><span data-stu-id="c45bf-532">Output Encoding Property</span></span></p></td>
<td><p><span data-ttu-id="c45bf-533">DBPROP_OUTPUTENCODING</span><span class="sxs-lookup"><span data-stu-id="c45bf-533">DBPROP_OUTPUTENCODING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-534">Свойство Output Stream</span><span class="sxs-lookup"><span data-stu-id="c45bf-534">Output Stream Property</span></span></p></td>
<td><p><span data-ttu-id="c45bf-535">DBPROP_OUTPUTSTREAM</span><span class="sxs-lookup"><span data-stu-id="c45bf-535">DBPROP_OUTPUTSTREAM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-536">Собственные изменения, видимые</span><span class="sxs-lookup"><span data-stu-id="c45bf-536">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="c45bf-537">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="c45bf-537">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-538">Собственные вставки видимые</span><span class="sxs-lookup"><span data-stu-id="c45bf-538">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="c45bf-539">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="c45bf-539">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-540">Сохранение при отменить</span><span class="sxs-lookup"><span data-stu-id="c45bf-540">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="c45bf-541">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="c45bf-541">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-542">Сохранение при фиксации</span><span class="sxs-lookup"><span data-stu-id="c45bf-542">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="c45bf-543">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="c45bf-543">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-544">Быстрая перезагрузка</span><span class="sxs-lookup"><span data-stu-id="c45bf-544">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="c45bf-545">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="c45bf-545">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-546">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="c45bf-546">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="c45bf-547">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="c45bf-547">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-548">Удаление удаленных строк</span><span class="sxs-lookup"><span data-stu-id="c45bf-548">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="c45bf-549">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="c45bf-549">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-550">Отчет о нескольких изменениях</span><span class="sxs-lookup"><span data-stu-id="c45bf-550">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="c45bf-551">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="c45bf-551">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-552">Возвращение ожидающих вставки</span><span class="sxs-lookup"><span data-stu-id="c45bf-552">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="c45bf-553">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="c45bf-553">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-554">Уведомление об удалении строки</span><span class="sxs-lookup"><span data-stu-id="c45bf-554">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="c45bf-555">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="c45bf-555">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-556">Уведомление о первом изменении строки</span><span class="sxs-lookup"><span data-stu-id="c45bf-556">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="c45bf-557">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="c45bf-557">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-558">Уведомление о вставке строки</span><span class="sxs-lookup"><span data-stu-id="c45bf-558">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="c45bf-559">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="c45bf-559">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-560">Привилегии строки</span><span class="sxs-lookup"><span data-stu-id="c45bf-560">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="c45bf-561">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="c45bf-561">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-562">Уведомление о повторной синхронизации строк</span><span class="sxs-lookup"><span data-stu-id="c45bf-562">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="c45bf-563">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="c45bf-563">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-564">Модель потоков по строкам</span><span class="sxs-lookup"><span data-stu-id="c45bf-564">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="c45bf-565">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="c45bf-565">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-566">Уведомление об отмене строки</span><span class="sxs-lookup"><span data-stu-id="c45bf-566">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="c45bf-567">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="c45bf-567">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-568">Уведомление об отмене удаления строки</span><span class="sxs-lookup"><span data-stu-id="c45bf-568">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="c45bf-569">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="c45bf-569">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-570">Уведомление об отмене вставки строки</span><span class="sxs-lookup"><span data-stu-id="c45bf-570">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="c45bf-571">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="c45bf-571">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-572">Уведомление об обновлении строки</span><span class="sxs-lookup"><span data-stu-id="c45bf-572">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="c45bf-573">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="c45bf-573">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-574">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="c45bf-574">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="c45bf-575">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="c45bf-575">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-576">Уведомление о выпуске rowset</span><span class="sxs-lookup"><span data-stu-id="c45bf-576">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="c45bf-577">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="c45bf-577">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-578">Прокрутка назад</span><span class="sxs-lookup"><span data-stu-id="c45bf-578">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="c45bf-579">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="c45bf-579">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-580">Курсор сервера</span><span class="sxs-lookup"><span data-stu-id="c45bf-580">Server Cursor</span></span></p></td>
<td><p><span data-ttu-id="c45bf-581">DBPROP_SERVERCURSOR</span><span class="sxs-lookup"><span data-stu-id="c45bf-581">DBPROP_SERVERCURSOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-582">Данные сервера при вставке</span><span class="sxs-lookup"><span data-stu-id="c45bf-582">Server Data on Insert</span></span></p></td>
<td><p><span data-ttu-id="c45bf-583">DBPROP_SERVERDATAONINSERT</span><span class="sxs-lookup"><span data-stu-id="c45bf-583">DBPROP_SERVERDATAONINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-584">Пропустить удаленные закладки</span><span class="sxs-lookup"><span data-stu-id="c45bf-584">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="c45bf-585">DBPROP_BOOKMARKSKIP</span><span class="sxs-lookup"><span data-stu-id="c45bf-585">DBPROP_BOOKMARKSKIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-586">Удостоверение строки strong</span><span class="sxs-lookup"><span data-stu-id="c45bf-586">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="c45bf-587">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="c45bf-587">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-588">Updatability</span><span class="sxs-lookup"><span data-stu-id="c45bf-588">Updatability</span></span></p></td>
<td><p><span data-ttu-id="c45bf-589">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="c45bf-589">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-590">Использование закладок</span><span class="sxs-lookup"><span data-stu-id="c45bf-590">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="c45bf-591">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="c45bf-591">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c45bf-592">Корень XML</span><span class="sxs-lookup"><span data-stu-id="c45bf-592">XML Root</span></span></p></td>
<td><p><span data-ttu-id="c45bf-593">SSPROP_STREAM_XMLROOT</span><span class="sxs-lookup"><span data-stu-id="c45bf-593">SSPROP_STREAM_XMLROOT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c45bf-594">XSL</span><span class="sxs-lookup"><span data-stu-id="c45bf-594">XSL</span></span></p></td>
<td><p><span data-ttu-id="c45bf-595">SSPROP_STREAM_XSL</span><span class="sxs-lookup"><span data-stu-id="c45bf-595">SSPROP_STREAM_XSL</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c45bf-596">Подробные сведения о реализации и функциональные сведения о поставщике OLE DB Microsoft SQL Server обратитесь к поставщику OLE DB для SQL Server документации в разделе OLE DB SDK MDAC.</span><span class="sxs-lookup"><span data-stu-id="c45bf-596">For specific implementation details and functional information about the Microsoft SQL Server OLE DB Provider, consult the OLE DB Provider for SQL Server documentation in the OLE DB section of the MDAC SDK.</span></span>

