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
# <a name="microsoft-ole-db-provider-for-sql-server"></a><span data-ttu-id="7c511-102">Поставщик Microsoft OLE DB для SQL Server</span><span class="sxs-lookup"><span data-stu-id="7c511-102">Microsoft OLE DB Provider for SQL Server</span></span>


<span data-ttu-id="7c511-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7c511-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7c511-104">Поставщик Microsoft OLE DB для SQL Server, SQLOLEDB позволяет ADO получать доступ к Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="7c511-104">The Microsoft OLE DB Provider for SQL Server, SQLOLEDB, allows ADO to access Microsoft SQL Server.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="7c511-105">Параметры строки подключения</span><span class="sxs-lookup"><span data-stu-id="7c511-105">Connection String Parameters</span></span>

<span data-ttu-id="7c511-106">Чтобы подключиться к поставщику, присвойте аргументу *provider* значение свойства [ConnectionString](connectionstring-property-ado.md) следующим образом:</span><span class="sxs-lookup"><span data-stu-id="7c511-106">To connect to this provider, set the *Provider* argument to the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```sql 
 
SQLOLEDB 
```

<span data-ttu-id="7c511-107">Это значение также можно задать или прочитать с помощью свойства [provider](provider-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="7c511-107">This value can also be set or read using the [Provider](provider-property-ado.md) property.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="7c511-108">Типичная строка подключения</span><span class="sxs-lookup"><span data-stu-id="7c511-108">Typical Connection String</span></span>

<span data-ttu-id="7c511-109">Типичная строка подключения для этого поставщика:</span><span class="sxs-lookup"><span data-stu-id="7c511-109">A typical connection string for this provider is:</span></span>

```sql 
 
"Provider=SQLOLEDB;Data Source=serverName;" 
Initial Catalog=databaseName; 
User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="7c511-110">Строка состоит из следующих ключевых слов:</span><span class="sxs-lookup"><span data-stu-id="7c511-110">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7c511-111">Ключевое слово</span><span class="sxs-lookup"><span data-stu-id="7c511-111">Keyword</span></span></p></th>
<th><p><span data-ttu-id="7c511-112">Описание</span><span class="sxs-lookup"><span data-stu-id="7c511-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7c511-113"><strong>Поставщик</strong></span><span class="sxs-lookup"><span data-stu-id="7c511-113"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="7c511-114">Указывает поставщика OLE DB для SQL Server.</span><span class="sxs-lookup"><span data-stu-id="7c511-114">Specifies the OLE DB Provider for SQL Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-115"><strong>Источник данных</strong> или <strong>сервер</strong></span><span class="sxs-lookup"><span data-stu-id="7c511-115"><strong>Data Source</strong> or <strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="7c511-116">Задает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="7c511-116">Specifies the name of a server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-117"><strong>Исходный каталог</strong> или <strong>база данных</strong></span><span class="sxs-lookup"><span data-stu-id="7c511-117"><strong>Initial Catalog</strong> or <strong>Database</strong></span></span></p></td>
<td><p><span data-ttu-id="7c511-118">Задает имя базы данных на сервере.</span><span class="sxs-lookup"><span data-stu-id="7c511-118">Specifies the name of a database on the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-119"><strong>Идентификатор пользователя</strong> или <strong>UID</strong></span><span class="sxs-lookup"><span data-stu-id="7c511-119"><strong>User ID</strong> or <strong>uid</strong></span></span></p></td>
<td><p><span data-ttu-id="7c511-120">Задает имя пользователя (для проверки подлинности SQL Server).</span><span class="sxs-lookup"><span data-stu-id="7c511-120">Specifies the user name (for SQL Server Authentication).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-121"><strong>Password</strong> или <strong>PWD</strong></span><span class="sxs-lookup"><span data-stu-id="7c511-121"><strong>Password</strong> or <strong>pwd</strong></span></span></p></td>
<td><p><span data-ttu-id="7c511-122">Указывает пароль пользователя (для проверки подлинности SQL Server).</span><span class="sxs-lookup"><span data-stu-id="7c511-122">Specifies the user password (for SQL Server Authentication).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-connection-parameters"></a><span data-ttu-id="7c511-123">Параметры подключения, зависящие от поставщика</span><span class="sxs-lookup"><span data-stu-id="7c511-123">Provider-Specific Connection Parameters</span></span>

<span data-ttu-id="7c511-124">Поставщик поддерживает несколько параметров подключения, относящихся к поставщику, помимо тех, которые определены в ADO.</span><span class="sxs-lookup"><span data-stu-id="7c511-124">The provider supports several provider-specific connection parameters in addition to those defined by ADO.</span></span> <span data-ttu-id="7c511-125">Как и в случае со свойствами подключения ADO, эти свойства, зависящие от поставщика, можно задать с помощью коллекции [свойств](properties-collection-ado.md) [подключения](connection-object-ado.md) или можно задать в качестве части **ConnectionString**.</span><span class="sxs-lookup"><span data-stu-id="7c511-125">As with the ADO connection properties, these provider-specific properties can be set via the [Properties](properties-collection-ado.md) collection of a [Connection](connection-object-ado.md) or can be set as part of the **ConnectionString**.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7c511-126">Параметр</span><span class="sxs-lookup"><span data-stu-id="7c511-126">Parameter</span></span></p></th>
<th><p><span data-ttu-id="7c511-127">Описание</span><span class="sxs-lookup"><span data-stu-id="7c511-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7c511-128">Trusted_Connection</span><span class="sxs-lookup"><span data-stu-id="7c511-128">Trusted_Connection</span></span></p></td>
<td><p><span data-ttu-id="7c511-129">Указывает режим проверки подлинности пользователя.</span><span class="sxs-lookup"><span data-stu-id="7c511-129">Indicates the user authentication mode.</span></span> <span data-ttu-id="7c511-130">Для этого может быть задано значение <strong>"Да" или "</strong> <strong>нет</strong>".</span><span class="sxs-lookup"><span data-stu-id="7c511-130">This can be set to <strong>Yes</strong> or <strong>No</strong>.</span></span> <span data-ttu-id="7c511-131">По умолчанию выбрано <strong>Нет</strong>.</span><span class="sxs-lookup"><span data-stu-id="7c511-131">The default value is <strong>No</strong>.</span></span> <span data-ttu-id="7c511-132">Если для этого свойства задано значение <strong>"Да"</strong>, SQLOLEDB использует режим проверки подлинности Microsoft Windows NT для авторизации доступа пользователей к базе данных SQL Server, указанной значениями свойства <strong>Location</strong> и <a href="datasource-property-ado.md">DataSource</a> .</span><span class="sxs-lookup"><span data-stu-id="7c511-132">If this property is set to <strong>Yes</strong>, then SQLOLEDB uses Microsoft Windows NT Authentication Mode to authorize user access to the SQL Server database specified by the <strong>Location</strong> and <a href="datasource-property-ado.md">Datasource</a> property values.</span></span> <span data-ttu-id="7c511-133">Если для этого свойства установлено значение <strong>нет</strong>, то SQLOLEDB использует смешанный режим для авторизации доступа пользователей к базе данных SQL Server.</span><span class="sxs-lookup"><span data-stu-id="7c511-133">If this property is set to <strong>No</strong>, then SQLOLEDB uses Mixed Mode to authorize user access to the SQL Server database.</span></span> <span data-ttu-id="7c511-134">Имя входа и пароль SQL Server указаны в свойствах <strong>идентификатора пользователя</strong> и <strong>пароля</strong> .</span><span class="sxs-lookup"><span data-stu-id="7c511-134">The SQL Server login and password are specified in the <strong>User Id</strong> and <strong>Password</strong> properties.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-135">Текущий язык</span><span class="sxs-lookup"><span data-stu-id="7c511-135">Current Language</span></span></p></td>
<td><p><span data-ttu-id="7c511-136">Указывает имя языка SQL Server.</span><span class="sxs-lookup"><span data-stu-id="7c511-136">Indicates a SQL Server language name.</span></span> <span data-ttu-id="7c511-137">Определяет язык, используемый для выбора и форматирования системных сообщений.</span><span class="sxs-lookup"><span data-stu-id="7c511-137">Identifies the language used for system message selection and formatting.</span></span> <span data-ttu-id="7c511-138">Язык должен быть установлен на SQL Server, иначе открытие подключения завершится с ошибками.</span><span class="sxs-lookup"><span data-stu-id="7c511-138">The language must be installed on the SQL Server, otherwise opening the connection will fail.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-139">Сетевой адрес</span><span class="sxs-lookup"><span data-stu-id="7c511-139">Network Address</span></span></p></td>
<td><p><span data-ttu-id="7c511-140">Указывает сетевой адрес сервера SQL Server, указанного в свойстве <strong>Location</strong> .</span><span class="sxs-lookup"><span data-stu-id="7c511-140">Indicates the network address of the SQL Server specified by the <strong>Location</strong> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-141">Сетевая библиотека</span><span class="sxs-lookup"><span data-stu-id="7c511-141">Network Library</span></span></p></td>
<td><p><span data-ttu-id="7c511-142">Указывает имя сетевой библиотеки (библиотеки динамической компоновки), используемое для связи с SQL Server.</span><span class="sxs-lookup"><span data-stu-id="7c511-142">Indicates the name of the network library (dynamic-link libraries) used to communicate with the SQL Server.</span></span> <span data-ttu-id="7c511-143">Имя не должно включать в себя путь или расширение DLL.</span><span class="sxs-lookup"><span data-stu-id="7c511-143">The name should not include the path or the .dll file name extension.</span></span> <span data-ttu-id="7c511-144">Значение по умолчанию предоставляется конфигурацией клиента SQL Server.</span><span class="sxs-lookup"><span data-stu-id="7c511-144">The default is provided by the SQL Server client configuration.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-145">Использование процедуры для подготовки</span><span class="sxs-lookup"><span data-stu-id="7c511-145">Use Procedure for Prepare</span></span></p></td>
<td><p><span data-ttu-id="7c511-146">Определяет, создает ли SQL Server временные хранимые процедуры при подготовке команд ( <strong>подготовленном</strong> свойстве).</span><span class="sxs-lookup"><span data-stu-id="7c511-146">Determines whether SQL Server creates temporary stored procedures when Commands are prepared (by the <strong>Prepared</strong> property).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-147">Автоматический перевод</span><span class="sxs-lookup"><span data-stu-id="7c511-147">Auto Translate</span></span></p></td>
<td><p><span data-ttu-id="7c511-148">Указывает, преобразуются ли символы OEM/ANSI.</span><span class="sxs-lookup"><span data-stu-id="7c511-148">Indicates whether OEM/ANSI characters are converted.</span></span> <span data-ttu-id="7c511-149">Для этого свойства можно задать значение <strong>true</strong> или <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="7c511-149">This property can be set to <strong>True</strong> or <strong>False</strong>.</span></span> <span data-ttu-id="7c511-150">Значение по умолчанию — <strong>True</strong>.</span><span class="sxs-lookup"><span data-stu-id="7c511-150">The default value is <strong>True</strong>.</span></span> <span data-ttu-id="7c511-151">Если для этого свойства задано <strong>значение true</strong>, SQLOLEDB выполняет преобразование знаков OEM/ANSI при получении или отправке многобайтовых строк в SQL Server.</span><span class="sxs-lookup"><span data-stu-id="7c511-151">If this property is set to <strong>True</strong>, then SQLOLEDB performs OEM/ANSI character conversion when multi-byte character strings are retrieved from, or sent to, the SQL Server.</span></span> <span data-ttu-id="7c511-152">Если для этого свойства задано <strong>значение false</strong>, SQLOLEDB не выполняет преобразование знаков OEM/ANSI в многобайтовой строке данных с несколькими байтами.</span><span class="sxs-lookup"><span data-stu-id="7c511-152">If this property is set to <strong>False</strong>, then SQLOLEDB does not perform OEM/ANSI character conversion on multi-byte character string data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-153">Размер пакета</span><span class="sxs-lookup"><span data-stu-id="7c511-153">Packet Size</span></span></p></td>
<td><p><span data-ttu-id="7c511-154">Указывает размер сетевого пакета в байтах.</span><span class="sxs-lookup"><span data-stu-id="7c511-154">Indicates a network packet size in bytes.</span></span> <span data-ttu-id="7c511-155">Значение свойства Size Packet должно находиться в пределах от 512 до 32767.</span><span class="sxs-lookup"><span data-stu-id="7c511-155">The packet size property value must be between 512 and 32767.</span></span> <span data-ttu-id="7c511-156">По умолчанию размер пакета для сети SQLOLEDB составляет 4096.</span><span class="sxs-lookup"><span data-stu-id="7c511-156">The default SQLOLEDB network packet size is 4096.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-157">Имя приложения</span><span class="sxs-lookup"><span data-stu-id="7c511-157">Application Name</span></span></p></td>
<td><p><span data-ttu-id="7c511-158">Указывает имя клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="7c511-158">Indicates the client application name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-159">ИДЕНТИФИКАТОР рабочей станции</span><span class="sxs-lookup"><span data-stu-id="7c511-159">Workstation ID</span></span></p></td>
<td><p><span data-ttu-id="7c511-160">Строка, идентифицирующая рабочую станцию.</span><span class="sxs-lookup"><span data-stu-id="7c511-160">A string identifying the workstation.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-object-usage"></a><span data-ttu-id="7c511-161">Использование объекта Command</span><span class="sxs-lookup"><span data-stu-id="7c511-161">Command Object Usage</span></span>

<span data-ttu-id="7c511-162">SQLOLEDB принимает в качестве допустимого синтаксиса амалгам, характерный для ODBC, ANSI и SQL Server.</span><span class="sxs-lookup"><span data-stu-id="7c511-162">SQLOLEDB accepts an amalgam of ODBC, ANSI, and SQL Server-specific Transact-SQL as valid syntax.</span></span> <span data-ttu-id="7c511-163">Например, следующая инструкция SQL использует escape-последовательность ODBC SQL для указания функции строки LCASE:</span><span class="sxs-lookup"><span data-stu-id="7c511-163">For example, the following SQL statement uses an ODBC SQL escape sequence to specify the LCASE string function:</span></span>

```sql 
 
SELECT customerid={fn LCASE(CustomerID)} FROM Customers 
```

<span data-ttu-id="7c511-164">LCASE возвращает строку символов, в которой все прописные символы преобразуются в их эквиваленты в нижнем регистре.</span><span class="sxs-lookup"><span data-stu-id="7c511-164">LCASE returns a character string, converting all uppercase characters to their lowercase equivalents.</span></span> <span data-ttu-id="7c511-165">Функция "строка ANSI SQL" ниже выполняет ту же операцию, поэтому следующая инструкция SQL является эквивалентом ANSI для приведенного выше оператора ODBC:</span><span class="sxs-lookup"><span data-stu-id="7c511-165">The ANSI SQL string function LOWER performs the same operation, so the following SQL statement is an ANSI equivalent to the ODBC statement presented above:</span></span>

```sql
 
SELECT customerid=LOWER(CustomerID) FROM Customers 
```

<span data-ttu-id="7c511-166">SQLOLEDB успешно обрабатывает любую форму оператора при указании в качестве текста для команды.</span><span class="sxs-lookup"><span data-stu-id="7c511-166">SQLOLEDB successfully processes either form of the statement when specified as text for a command.</span></span>

## <a name="stored-procedures"></a><span data-ttu-id="7c511-167">Хранимые процедуры</span><span class="sxs-lookup"><span data-stu-id="7c511-167">Stored Procedures</span></span>

<span data-ttu-id="7c511-168">При выполнении хранимой процедуры SQL Server с помощью команды SQLOLEDB используйте escape-последовательность вызова процедуры ODBC в тексте команды.</span><span class="sxs-lookup"><span data-stu-id="7c511-168">When executing a SQL Server stored procedure using a SQLOLEDB command, use the ODBC procedure call escape sequence in the command text.</span></span> <span data-ttu-id="7c511-169">Затем служба SQLOLEDB использует механизм удаленного вызова процедур SQL Server для оптимизации обработки команд.</span><span class="sxs-lookup"><span data-stu-id="7c511-169">SQLOLEDB then uses the remote procedure call mechanism of SQL Server to optimize command processing.</span></span> <span data-ttu-id="7c511-170">Например, следующая инструкция ODBC SQL является предпочтительным текстом команды в форме Transact-SQL:</span><span class="sxs-lookup"><span data-stu-id="7c511-170">For example, the following ODBC SQL statement is the preferred command text over the Transact-SQL form:</span></span>

## <a name="odbc-sql"></a><span data-ttu-id="7c511-171">ODBC SQL</span><span class="sxs-lookup"><span data-stu-id="7c511-171">ODBC SQL</span></span>

```sql 
 
{call SalesByCategory('Produce', '1995')} 
```

## <a name="transact-sql"></a><span data-ttu-id="7c511-172">Transact SQL</span><span class="sxs-lookup"><span data-stu-id="7c511-172">Transact-SQL</span></span>

```sql 
 
EXECUTE SalesByCategory 'Produce', '1995' 
```

## <a name="recordset-behavior"></a><span data-ttu-id="7c511-173">Поведение набора записей</span><span class="sxs-lookup"><span data-stu-id="7c511-173">Recordset Behavior</span></span>

<span data-ttu-id="7c511-174">SQLOLEDB не может использовать курсоры SQL Server для поддержки множественных результатов, создаваемых многими командами.</span><span class="sxs-lookup"><span data-stu-id="7c511-174">SQLOLEDB cannot use SQL Server cursors to support the multiple-result generated by many commands.</span></span> <span data-ttu-id="7c511-175">Если потребитель запрашивает набор записей, требующий поддержки курсора SQL Server, возникает ошибка, если в качестве результата использован текст команды, который создает больше одного объекта Recordset.</span><span class="sxs-lookup"><span data-stu-id="7c511-175">If a consumer requests a recordset requiring SQL Server cursor support, an error occurs if the command text used generates more than a single recordset as its result.</span></span>

<span data-ttu-id="7c511-176">Прокручиваемые наборы записей SQLOLEDB поддерживаются курсорами SQL Server.</span><span class="sxs-lookup"><span data-stu-id="7c511-176">Scrollable SQLOLEDB recordsets are supported by SQL Server cursors.</span></span> <span data-ttu-id="7c511-177">SQL Server накладывает ограничения на курсоры, которые чувствительны к изменениям, внесенным другими пользователями базы данных.</span><span class="sxs-lookup"><span data-stu-id="7c511-177">SQL Server imposes limitations on cursors that are sensitive to changes made by other users of the database.</span></span> <span data-ttu-id="7c511-178">В частности, строки в некоторых курсорах не могут быть упорядочены, и попытка создать набор записей с помощью команды, содержащей предложение ORDER BY SQL, может привести к сбою.</span><span class="sxs-lookup"><span data-stu-id="7c511-178">Specifically, the rows in some cursors cannot be ordered, and attempting to create a recordset using a command containing an SQL ORDER BY clause can fail.</span></span>

## <a name="dynamic-properties"></a><span data-ttu-id="7c511-179">Динамические свойства</span><span class="sxs-lookup"><span data-stu-id="7c511-179">Dynamic Properties</span></span>

<span data-ttu-id="7c511-180">Поставщик Microsoft OLE DB для SQL Server вставляет несколько динамических свойств в коллекцию **свойств** неоткрытых [подключений](connection-object-ado.md), [наборов записей](recordset-object-ado.md)и [командных](command-object-ado.md) объектов.</span><span class="sxs-lookup"><span data-stu-id="7c511-180">The Microsoft OLE DB Provider for SQL Server inserts several dynamic properties into the **Properties** collection of the unopened [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md), and [Command](command-object-ado.md) objects.</span></span>

<span data-ttu-id="7c511-181">В приведенных ниже таблицах указаны перекрестные индексы имен ADO и OLE DB для каждого динамического свойства.</span><span class="sxs-lookup"><span data-stu-id="7c511-181">The following tables are a cross-index of the ADO and OLE DB names for each dynamic property.</span></span> <span data-ttu-id="7c511-182">Справочник программиста OLE DB ссылается на имя свойства ADO по термину "Описание".</span><span class="sxs-lookup"><span data-stu-id="7c511-182">The OLE DB Programmer's Reference refers to an ADO property name by the term "Description."</span></span> <span data-ttu-id="7c511-183">Дополнительные сведения об этих свойствах можно найти в справочнике программиста по OLE DB.</span><span class="sxs-lookup"><span data-stu-id="7c511-183">You can find more information about these properties in the OLE DB Programmer's Reference.</span></span> <span data-ttu-id="7c511-184">Выполните поиск по имени свойства OLE DB в индексе или в разделе приложение C: свойства OLE DB.</span><span class="sxs-lookup"><span data-stu-id="7c511-184">Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span></span>

## <a name="connection-dynamic-properties"></a><span data-ttu-id="7c511-185">Динамические свойства подключения</span><span class="sxs-lookup"><span data-stu-id="7c511-185">Connection Dynamic Properties</span></span>

<span data-ttu-id="7c511-186">Следующие свойства добавляются в коллекцию **свойств** объекта **Connection** .</span><span class="sxs-lookup"><span data-stu-id="7c511-186">The following properties are added to the **Connection** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7c511-187">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="7c511-187">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="7c511-188">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="7c511-188">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7c511-189">Активные сеансы</span><span class="sxs-lookup"><span data-stu-id="7c511-189">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="7c511-190">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="7c511-190">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-191">Асинчабле Abort</span><span class="sxs-lookup"><span data-stu-id="7c511-191">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="7c511-192">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="7c511-192">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-193">Фиксация асинчабле</span><span class="sxs-lookup"><span data-stu-id="7c511-193">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="7c511-194">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="7c511-194">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-195">Уровни изоляции для автоматической фиксации</span><span class="sxs-lookup"><span data-stu-id="7c511-195">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="7c511-196">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="7c511-196">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-197">Расположение каталога</span><span class="sxs-lookup"><span data-stu-id="7c511-197">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="7c511-198">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="7c511-198">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-199">Термин каталога</span><span class="sxs-lookup"><span data-stu-id="7c511-199">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="7c511-200">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="7c511-200">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-201">Определение столбца</span><span class="sxs-lookup"><span data-stu-id="7c511-201">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="7c511-202">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="7c511-202">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-203">Время ожидания подключения</span><span class="sxs-lookup"><span data-stu-id="7c511-203">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="7c511-204">DBPROP_INIT_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="7c511-204">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-205">Текущий каталог</span><span class="sxs-lookup"><span data-stu-id="7c511-205">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="7c511-206">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="7c511-206">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-207">Источник данных</span><span class="sxs-lookup"><span data-stu-id="7c511-207">Data Source</span></span></p></td>
<td><p><span data-ttu-id="7c511-208">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="7c511-208">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-209">Имя источника данных</span><span class="sxs-lookup"><span data-stu-id="7c511-209">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="7c511-210">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="7c511-210">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-211">Модель потоков объектов источника данных</span><span class="sxs-lookup"><span data-stu-id="7c511-211">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="7c511-212">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="7c511-212">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-213">Имя СУБД</span><span class="sxs-lookup"><span data-stu-id="7c511-213">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="7c511-214">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="7c511-214">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-215">Версия DBMS</span><span class="sxs-lookup"><span data-stu-id="7c511-215">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="7c511-216">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="7c511-216">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-217">Расширенные свойства</span><span class="sxs-lookup"><span data-stu-id="7c511-217">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="7c511-218">DBPROP_INIT_PROVIDERSTRING</span><span class="sxs-lookup"><span data-stu-id="7c511-218">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-219">ГРУППИРОВКа по поддержке</span><span class="sxs-lookup"><span data-stu-id="7c511-219">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="7c511-220">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="7c511-220">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-221">Поддержка гетерогенных таблиц</span><span class="sxs-lookup"><span data-stu-id="7c511-221">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="7c511-222">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="7c511-222">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-223">Чувствительность к регистру идентификаторов</span><span class="sxs-lookup"><span data-stu-id="7c511-223">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="7c511-224">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="7c511-224">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-225">Исходный каталог</span><span class="sxs-lookup"><span data-stu-id="7c511-225">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="7c511-226">DBPROP_INIT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="7c511-226">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-227">Уровни изоляции</span><span class="sxs-lookup"><span data-stu-id="7c511-227">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="7c511-228">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="7c511-228">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-229">Хранение изоляции</span><span class="sxs-lookup"><span data-stu-id="7c511-229">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="7c511-230">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="7c511-230">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-231">Идентификатор языкового стандарта</span><span class="sxs-lookup"><span data-stu-id="7c511-231">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="7c511-232">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="7c511-232">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-233">Максимальный размер индекса</span><span class="sxs-lookup"><span data-stu-id="7c511-233">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="7c511-234">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="7c511-234">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-235">Максимальный размер строки</span><span class="sxs-lookup"><span data-stu-id="7c511-235">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="7c511-236">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="7c511-236">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-237">Максимальный размер строки включает большой двоичный объект</span><span class="sxs-lookup"><span data-stu-id="7c511-237">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="7c511-238">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="7c511-238">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-239">Максимальное число таблиц в SELECT</span><span class="sxs-lookup"><span data-stu-id="7c511-239">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="7c511-240">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="7c511-240">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-241">Наборы параметров с несколькими параметрами</span><span class="sxs-lookup"><span data-stu-id="7c511-241">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="7c511-242">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="7c511-242">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-243">Несколько результатов</span><span class="sxs-lookup"><span data-stu-id="7c511-243">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="7c511-244">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="7c511-244">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-245">Несколько объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="7c511-245">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="7c511-246">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="7c511-246">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-247">Обновление с несколькими таблицами</span><span class="sxs-lookup"><span data-stu-id="7c511-247">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="7c511-248">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="7c511-248">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-249">Порядок сортировки NULL</span><span class="sxs-lookup"><span data-stu-id="7c511-249">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="7c511-250">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="7c511-250">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-251">Поведение сцепления со значением NULL</span><span class="sxs-lookup"><span data-stu-id="7c511-251">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="7c511-252">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="7c511-252">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-253">Версия OLE DB</span><span class="sxs-lookup"><span data-stu-id="7c511-253">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="7c511-254">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="7c511-254">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-255">Поддержка объектов OLE</span><span class="sxs-lookup"><span data-stu-id="7c511-255">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="7c511-256">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="7c511-256">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-257">Поддержка открытых наборов строк</span><span class="sxs-lookup"><span data-stu-id="7c511-257">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="7c511-258">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="7c511-258">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-259">УПОРЯДОЧЕНие по столбцам в списке выборки</span><span class="sxs-lookup"><span data-stu-id="7c511-259">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="7c511-260">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="7c511-260">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-261">Доступность выходного параметра</span><span class="sxs-lookup"><span data-stu-id="7c511-261">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="7c511-262">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="7c511-262">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-263">Передача по параметрам доступа ref</span><span class="sxs-lookup"><span data-stu-id="7c511-263">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="7c511-264">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="7c511-264">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-265">Password</span><span class="sxs-lookup"><span data-stu-id="7c511-265">Password</span></span></p></td>
<td><p><span data-ttu-id="7c511-266">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="7c511-266">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-267">Сохранение сведений о безопасности</span><span class="sxs-lookup"><span data-stu-id="7c511-267">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="7c511-268">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span><span class="sxs-lookup"><span data-stu-id="7c511-268">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-269">Тип постоянного идентификатора</span><span class="sxs-lookup"><span data-stu-id="7c511-269">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="7c511-270">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="7c511-270">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-271">Действие по подготовке к прерыванию</span><span class="sxs-lookup"><span data-stu-id="7c511-271">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="7c511-272">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="7c511-272">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-273">Подготовка режима фиксации</span><span class="sxs-lookup"><span data-stu-id="7c511-273">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="7c511-274">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="7c511-274">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-275">Термин процедуры</span><span class="sxs-lookup"><span data-stu-id="7c511-275">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="7c511-276">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="7c511-276">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-277">Prompt</span><span class="sxs-lookup"><span data-stu-id="7c511-277">Prompt</span></span></p></td>
<td><p><span data-ttu-id="7c511-278">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="7c511-278">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-279">Понятное имя поставщика</span><span class="sxs-lookup"><span data-stu-id="7c511-279">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="7c511-280">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="7c511-280">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-281">Имя поставщика</span><span class="sxs-lookup"><span data-stu-id="7c511-281">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="7c511-282">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="7c511-282">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-283">Версия поставщика</span><span class="sxs-lookup"><span data-stu-id="7c511-283">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="7c511-284">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="7c511-284">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-285">Источник данных, предназначенный только для чтения</span><span class="sxs-lookup"><span data-stu-id="7c511-285">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="7c511-286">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="7c511-286">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-287">Преобразования наборов строк для команды</span><span class="sxs-lookup"><span data-stu-id="7c511-287">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="7c511-288">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="7c511-288">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-289">Термин схемы</span><span class="sxs-lookup"><span data-stu-id="7c511-289">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="7c511-290">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="7c511-290">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-291">Использование схемы</span><span class="sxs-lookup"><span data-stu-id="7c511-291">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="7c511-292">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="7c511-292">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-293">Поддержка SQL</span><span class="sxs-lookup"><span data-stu-id="7c511-293">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="7c511-294">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="7c511-294">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-295">Структурированное хранилище</span><span class="sxs-lookup"><span data-stu-id="7c511-295">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="7c511-296">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="7c511-296">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-297">Поддержка вложенных запросов</span><span class="sxs-lookup"><span data-stu-id="7c511-297">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="7c511-298">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="7c511-298">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-299">Табличный термин</span><span class="sxs-lookup"><span data-stu-id="7c511-299">Table Term</span></span></p></td>
<td><p><span data-ttu-id="7c511-300">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="7c511-300">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-301">DDL транзакции</span><span class="sxs-lookup"><span data-stu-id="7c511-301">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="7c511-302">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="7c511-302">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-303">Идентификатор пользователя</span><span class="sxs-lookup"><span data-stu-id="7c511-303">User ID</span></span></p></td>
<td><p><span data-ttu-id="7c511-304">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="7c511-304">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-305">имя пользователя;</span><span class="sxs-lookup"><span data-stu-id="7c511-305">User Name</span></span></p></td>
<td><p><span data-ttu-id="7c511-306">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="7c511-306">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-307">Дескриптор окна</span><span class="sxs-lookup"><span data-stu-id="7c511-307">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="7c511-308">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="7c511-308">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a><span data-ttu-id="7c511-309">Динамические свойства Recordset</span><span class="sxs-lookup"><span data-stu-id="7c511-309">Recordset Dynamic Properties</span></span>

<span data-ttu-id="7c511-310">Следующие свойства добавляются в коллекцию **свойств** объекта **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="7c511-310">The following properties are added to the **Recordset** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7c511-311">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="7c511-311">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="7c511-312">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="7c511-312">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7c511-313">Порядок доступа</span><span class="sxs-lookup"><span data-stu-id="7c511-313">Access Order</span></span></p></td>
<td><p><span data-ttu-id="7c511-314">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="7c511-314">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-315">Блокировка объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="7c511-315">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="7c511-316">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="7c511-316">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-317">Тип закладки</span><span class="sxs-lookup"><span data-stu-id="7c511-317">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="7c511-318">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="7c511-318">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-319">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="7c511-319">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="7c511-320">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="7c511-320">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-321">Изменение вставленных строк</span><span class="sxs-lookup"><span data-stu-id="7c511-321">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="7c511-322">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="7c511-322">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-323">Права на столбцы</span><span class="sxs-lookup"><span data-stu-id="7c511-323">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="7c511-324">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="7c511-324">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-325">Уведомление о наборе столбцов</span><span class="sxs-lookup"><span data-stu-id="7c511-325">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="7c511-326">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="7c511-326">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-327">Время ожидания команды</span><span class="sxs-lookup"><span data-stu-id="7c511-327">Command Time Out</span></span></p></td>
<td><p><span data-ttu-id="7c511-328">DBPROP_COMMANDTIMEOUT</span><span class="sxs-lookup"><span data-stu-id="7c511-328">DBPROP_COMMANDTIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-329">Откладывание столбца</span><span class="sxs-lookup"><span data-stu-id="7c511-329">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="7c511-330">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="7c511-330">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-331">Откладывание обновлений объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="7c511-331">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="7c511-332">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="7c511-332">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-333">Извлечение назад</span><span class="sxs-lookup"><span data-stu-id="7c511-333">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="7c511-334">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="7c511-334">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-335">Удержание строк</span><span class="sxs-lookup"><span data-stu-id="7c511-335">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="7c511-336">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="7c511-336">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-337">иакцессор</span><span class="sxs-lookup"><span data-stu-id="7c511-337">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="7c511-338">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="7c511-338">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-339">иколумнсинфо</span><span class="sxs-lookup"><span data-stu-id="7c511-339">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="7c511-340">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="7c511-340">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-341">иколумнсровсет</span><span class="sxs-lookup"><span data-stu-id="7c511-341">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="7c511-342">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="7c511-342">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-343">иконнектионпоинтконтаинер</span><span class="sxs-lookup"><span data-stu-id="7c511-343">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="7c511-344">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="7c511-344">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-345">иконверттипе</span><span class="sxs-lookup"><span data-stu-id="7c511-345">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="7c511-346">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="7c511-346">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-347">Строки для мобильных устройств</span><span class="sxs-lookup"><span data-stu-id="7c511-347">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="7c511-348">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="7c511-348">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-349">IRowset</span><span class="sxs-lookup"><span data-stu-id="7c511-349">IRowset</span></span></p></td>
<td><p><span data-ttu-id="7c511-350">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="7c511-350">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-351">ировсетчанже</span><span class="sxs-lookup"><span data-stu-id="7c511-351">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="7c511-352">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="7c511-352">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-353">ировсетидентити</span><span class="sxs-lookup"><span data-stu-id="7c511-353">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="7c511-354">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="7c511-354">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-355">ировсетинфо</span><span class="sxs-lookup"><span data-stu-id="7c511-355">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="7c511-356">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="7c511-356">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-357">ировсетлокате</span><span class="sxs-lookup"><span data-stu-id="7c511-357">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="7c511-358">DBPROP_IRowsestLocate</span><span class="sxs-lookup"><span data-stu-id="7c511-358">DBPROP_IRowsestLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-359">ировсетресинч</span><span class="sxs-lookup"><span data-stu-id="7c511-359">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-360">ировсетскролл</span><span class="sxs-lookup"><span data-stu-id="7c511-360">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="7c511-361">DBPROP_IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="7c511-361">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-362">ировсетупдате</span><span class="sxs-lookup"><span data-stu-id="7c511-362">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="7c511-363">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="7c511-363">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-364">исекуентиалстреам</span><span class="sxs-lookup"><span data-stu-id="7c511-364">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="7c511-365">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="7c511-365">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-366">исуппортерроринфо</span><span class="sxs-lookup"><span data-stu-id="7c511-366">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="7c511-367">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="7c511-367">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-368">Литеральные закладки</span><span class="sxs-lookup"><span data-stu-id="7c511-368">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="7c511-369">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="7c511-369">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-370">Идентификация строк литералов</span><span class="sxs-lookup"><span data-stu-id="7c511-370">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="7c511-371">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="7c511-371">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-372">Максимальное число открытых строк</span><span class="sxs-lookup"><span data-stu-id="7c511-372">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="7c511-373">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="7c511-373">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-374">Максимальное число ожидающих строк</span><span class="sxs-lookup"><span data-stu-id="7c511-374">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="7c511-375">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="7c511-375">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-376">Максимальное число строк</span><span class="sxs-lookup"><span data-stu-id="7c511-376">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="7c511-377">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="7c511-377">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-378">Детализация уведомлений</span><span class="sxs-lookup"><span data-stu-id="7c511-378">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="7c511-379">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="7c511-379">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-380">Этапы уведомления</span><span class="sxs-lookup"><span data-stu-id="7c511-380">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="7c511-381">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="7c511-381">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-382">Объекты, транзакционные</span><span class="sxs-lookup"><span data-stu-id="7c511-382">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="7c511-383">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="7c511-383">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-384">Видны другие изменения</span><span class="sxs-lookup"><span data-stu-id="7c511-384">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="7c511-385">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="7c511-385">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-386">Видимые вставки других пользователей</span><span class="sxs-lookup"><span data-stu-id="7c511-386">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="7c511-387">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="7c511-387">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-388">Видны изменения</span><span class="sxs-lookup"><span data-stu-id="7c511-388">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="7c511-389">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="7c511-389">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-390">Отображение собственных вставок</span><span class="sxs-lookup"><span data-stu-id="7c511-390">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="7c511-391">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="7c511-391">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-392">Сохранение при прерывании</span><span class="sxs-lookup"><span data-stu-id="7c511-392">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="7c511-393">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="7c511-393">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-394">Сохранение при фиксации</span><span class="sxs-lookup"><span data-stu-id="7c511-394">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="7c511-395">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="7c511-395">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-396">Быстрый перезапуск</span><span class="sxs-lookup"><span data-stu-id="7c511-396">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="7c511-397">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="7c511-397">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-398">Повторные события</span><span class="sxs-lookup"><span data-stu-id="7c511-398">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="7c511-399">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="7c511-399">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-400">Удаление удаленных строк</span><span class="sxs-lookup"><span data-stu-id="7c511-400">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="7c511-401">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="7c511-401">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-402">Отчет о нескольких изменениях</span><span class="sxs-lookup"><span data-stu-id="7c511-402">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="7c511-403">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="7c511-403">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-404">Возврат ожидающих вставок</span><span class="sxs-lookup"><span data-stu-id="7c511-404">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="7c511-405">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="7c511-405">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-406">Уведомление об удалении строки</span><span class="sxs-lookup"><span data-stu-id="7c511-406">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="7c511-407">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="7c511-407">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-408">Уведомление о первом изменении строки</span><span class="sxs-lookup"><span data-stu-id="7c511-408">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="7c511-409">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="7c511-409">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-410">Уведомление о вставке строк</span><span class="sxs-lookup"><span data-stu-id="7c511-410">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="7c511-411">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="7c511-411">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-412">Права на строки</span><span class="sxs-lookup"><span data-stu-id="7c511-412">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="7c511-413">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="7c511-413">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-414">Уведомление о повторной синхронизации строк</span><span class="sxs-lookup"><span data-stu-id="7c511-414">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="7c511-415">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="7c511-415">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-416">Потоковая модель для строк</span><span class="sxs-lookup"><span data-stu-id="7c511-416">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="7c511-417">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="7c511-417">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-418">Уведомление об отмене изменения строки</span><span class="sxs-lookup"><span data-stu-id="7c511-418">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="7c511-419">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="7c511-419">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-420">Уведомление о отмене удаления строки</span><span class="sxs-lookup"><span data-stu-id="7c511-420">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="7c511-421">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="7c511-421">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-422">Уведомление об отмене вставки строки</span><span class="sxs-lookup"><span data-stu-id="7c511-422">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="7c511-423">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="7c511-423">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-424">Уведомление об обновлении строк</span><span class="sxs-lookup"><span data-stu-id="7c511-424">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="7c511-425">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="7c511-425">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-426">Уведомление об изменении положения при получении набора строк</span><span class="sxs-lookup"><span data-stu-id="7c511-426">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="7c511-427">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="7c511-427">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-428">Уведомление о выпуске набора строк</span><span class="sxs-lookup"><span data-stu-id="7c511-428">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="7c511-429">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="7c511-429">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-430">Прокрутка назад</span><span class="sxs-lookup"><span data-stu-id="7c511-430">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="7c511-431">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="7c511-431">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-432">Серверный курсор</span><span class="sxs-lookup"><span data-stu-id="7c511-432">Server Cursor</span></span></p></td>
<td><p><span data-ttu-id="7c511-433">DBPROP_SERVERCURSOR</span><span class="sxs-lookup"><span data-stu-id="7c511-433">DBPROP_SERVERCURSOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-434">Пропуск удаленных закладок</span><span class="sxs-lookup"><span data-stu-id="7c511-434">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="7c511-435">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="7c511-435">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-436">Строгая идентификация строк</span><span class="sxs-lookup"><span data-stu-id="7c511-436">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="7c511-437">DBPROP_STRONGITDENTITY</span><span class="sxs-lookup"><span data-stu-id="7c511-437">DBPROP_STRONGITDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-438">Уникальные строки</span><span class="sxs-lookup"><span data-stu-id="7c511-438">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="7c511-439">DBPROP_UNIQUEROWS</span><span class="sxs-lookup"><span data-stu-id="7c511-439">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-440">Обновление</span><span class="sxs-lookup"><span data-stu-id="7c511-440">Updatability</span></span></p></td>
<td><p><span data-ttu-id="7c511-441">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="7c511-441">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-442">Использование закладок</span><span class="sxs-lookup"><span data-stu-id="7c511-442">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="7c511-443">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="7c511-443">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a><span data-ttu-id="7c511-444">Динамические свойства команд</span><span class="sxs-lookup"><span data-stu-id="7c511-444">Command Dynamic Properties</span></span>

<span data-ttu-id="7c511-445">Указанные ниже свойства добавляются в коллекцию **свойств** **командного** объекта.</span><span class="sxs-lookup"><span data-stu-id="7c511-445">The following properties are added to the **Command** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7c511-446">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="7c511-446">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="7c511-447">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="7c511-447">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7c511-448">Порядок доступа</span><span class="sxs-lookup"><span data-stu-id="7c511-448">Access Order</span></span></p></td>
<td><p><span data-ttu-id="7c511-449">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="7c511-449">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-450">Базовый путь</span><span class="sxs-lookup"><span data-stu-id="7c511-450">Base Path</span></span></p></td>
<td><p><span data-ttu-id="7c511-451">SSPROP_STREAM_BASEPATH</span><span class="sxs-lookup"><span data-stu-id="7c511-451">SSPROP_STREAM_BASEPATH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-452">Блокировка объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="7c511-452">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="7c511-453">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="7c511-453">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-454">Тип закладки</span><span class="sxs-lookup"><span data-stu-id="7c511-454">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="7c511-455">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="7c511-455">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-456">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="7c511-456">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="7c511-457">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="7c511-457">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-458">Изменение вставленных строк</span><span class="sxs-lookup"><span data-stu-id="7c511-458">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="7c511-459">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="7c511-459">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-460">Права на столбцы</span><span class="sxs-lookup"><span data-stu-id="7c511-460">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="7c511-461">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="7c511-461">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-462">Уведомление о наборе столбцов</span><span class="sxs-lookup"><span data-stu-id="7c511-462">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="7c511-463">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="7c511-463">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-464">Тип контента</span><span class="sxs-lookup"><span data-stu-id="7c511-464">Content Type</span></span></p></td>
<td><p><span data-ttu-id="7c511-465">SSPROP_STREAM_CONTENTTYPE</span><span class="sxs-lookup"><span data-stu-id="7c511-465">SSPROP_STREAM_CONTENTTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-466">Автоматическая выборка курсора</span><span class="sxs-lookup"><span data-stu-id="7c511-466">Cursor Auto Fetch</span></span></p></td>
<td><p><span data-ttu-id="7c511-467">SSPROP_CURSORAUTOFETCH</span><span class="sxs-lookup"><span data-stu-id="7c511-467">SSPROP_CURSORAUTOFETCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-468">Откладывание столбца</span><span class="sxs-lookup"><span data-stu-id="7c511-468">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="7c511-469">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="7c511-469">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-470">Отложить подготовку</span><span class="sxs-lookup"><span data-stu-id="7c511-470">Defer Prepare</span></span></p></td>
<td><p><span data-ttu-id="7c511-471">SSPROP_DEFERPREPARE</span><span class="sxs-lookup"><span data-stu-id="7c511-471">SSPROP_DEFERPREPARE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-472">Откладывание обновлений объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="7c511-472">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="7c511-473">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="7c511-473">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-474">Извлечение назад</span><span class="sxs-lookup"><span data-stu-id="7c511-474">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="7c511-475">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="7c511-475">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-476">Удержание строк</span><span class="sxs-lookup"><span data-stu-id="7c511-476">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="7c511-477">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="7c511-477">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-478">иакцессор</span><span class="sxs-lookup"><span data-stu-id="7c511-478">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="7c511-479">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="7c511-479">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-480">иколумнсинфо</span><span class="sxs-lookup"><span data-stu-id="7c511-480">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="7c511-481">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="7c511-481">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-482">иколумнсровсет</span><span class="sxs-lookup"><span data-stu-id="7c511-482">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="7c511-483">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="7c511-483">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-484">иконнектионпоинтконтаинер</span><span class="sxs-lookup"><span data-stu-id="7c511-484">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="7c511-485">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="7c511-485">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-486">иконверттипе</span><span class="sxs-lookup"><span data-stu-id="7c511-486">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="7c511-487">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="7c511-487">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-488">Строки для мобильных устройств</span><span class="sxs-lookup"><span data-stu-id="7c511-488">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="7c511-489">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="7c511-489">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-490">IRowset</span><span class="sxs-lookup"><span data-stu-id="7c511-490">IRowset</span></span></p></td>
<td><p><span data-ttu-id="7c511-491">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="7c511-491">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-492">ировсетчанже</span><span class="sxs-lookup"><span data-stu-id="7c511-492">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="7c511-493">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="7c511-493">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-494">ировсетидентити</span><span class="sxs-lookup"><span data-stu-id="7c511-494">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="7c511-495">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="7c511-495">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-496">ировсетинфо</span><span class="sxs-lookup"><span data-stu-id="7c511-496">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="7c511-497">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="7c511-497">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-498">ировсетлокате</span><span class="sxs-lookup"><span data-stu-id="7c511-498">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="7c511-499">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="7c511-499">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-500">ировсетресинч</span><span class="sxs-lookup"><span data-stu-id="7c511-500">IRowsetResynch</span></span></p></td>
<td><p><span data-ttu-id="7c511-501">DBPROP_IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="7c511-501">DBPROP_IRowsetResynch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-502">ировсетскролл</span><span class="sxs-lookup"><span data-stu-id="7c511-502">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="7c511-503">DBPROP_IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="7c511-503">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-504">ировсетупдате</span><span class="sxs-lookup"><span data-stu-id="7c511-504">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="7c511-505">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="7c511-505">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-506">исекуентиалстреам</span><span class="sxs-lookup"><span data-stu-id="7c511-506">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="7c511-507">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="7c511-507">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-508">исуппортерроринфо</span><span class="sxs-lookup"><span data-stu-id="7c511-508">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="7c511-509">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="7c511-509">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-510">Литеральные закладки</span><span class="sxs-lookup"><span data-stu-id="7c511-510">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="7c511-511">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="7c511-511">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-512">Идентификация строк литералов</span><span class="sxs-lookup"><span data-stu-id="7c511-512">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="7c511-513">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="7c511-513">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-514">Режим блокировки</span><span class="sxs-lookup"><span data-stu-id="7c511-514">Lock Mode</span></span></p></td>
<td><p><span data-ttu-id="7c511-515">DBPROP_LOCKMODE</span><span class="sxs-lookup"><span data-stu-id="7c511-515">DBPROP_LOCKMODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-516">Максимальное число открытых строк</span><span class="sxs-lookup"><span data-stu-id="7c511-516">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="7c511-517">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="7c511-517">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-518">Максимальное число ожидающих строк</span><span class="sxs-lookup"><span data-stu-id="7c511-518">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="7c511-519">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="7c511-519">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-520">Максимальное число строк</span><span class="sxs-lookup"><span data-stu-id="7c511-520">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="7c511-521">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="7c511-521">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-522">Детализация уведомлений</span><span class="sxs-lookup"><span data-stu-id="7c511-522">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="7c511-523">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="7c511-523">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-524">Этапы уведомления</span><span class="sxs-lookup"><span data-stu-id="7c511-524">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="7c511-525">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="7c511-525">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-526">Объекты, транзакционные</span><span class="sxs-lookup"><span data-stu-id="7c511-526">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="7c511-527">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="7c511-527">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-528">Видны другие изменения</span><span class="sxs-lookup"><span data-stu-id="7c511-528">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="7c511-529">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="7c511-529">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-530">Видимые вставки других пользователей</span><span class="sxs-lookup"><span data-stu-id="7c511-530">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="7c511-531">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="7c511-531">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-532">Свойство Encoding вывода</span><span class="sxs-lookup"><span data-stu-id="7c511-532">Output Encoding Property</span></span></p></td>
<td><p><span data-ttu-id="7c511-533">DBPROP_OUTPUTENCODING</span><span class="sxs-lookup"><span data-stu-id="7c511-533">DBPROP_OUTPUTENCODING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-534">Свойство потока вывода</span><span class="sxs-lookup"><span data-stu-id="7c511-534">Output Stream Property</span></span></p></td>
<td><p><span data-ttu-id="7c511-535">DBPROP_OUTPUTSTREAM</span><span class="sxs-lookup"><span data-stu-id="7c511-535">DBPROP_OUTPUTSTREAM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-536">Видны изменения</span><span class="sxs-lookup"><span data-stu-id="7c511-536">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="7c511-537">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="7c511-537">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-538">Отображение собственных вставок</span><span class="sxs-lookup"><span data-stu-id="7c511-538">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="7c511-539">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="7c511-539">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-540">Сохранение при прерывании</span><span class="sxs-lookup"><span data-stu-id="7c511-540">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="7c511-541">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="7c511-541">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-542">Сохранение при фиксации</span><span class="sxs-lookup"><span data-stu-id="7c511-542">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="7c511-543">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="7c511-543">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-544">Быстрый перезапуск</span><span class="sxs-lookup"><span data-stu-id="7c511-544">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="7c511-545">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="7c511-545">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-546">Повторные события</span><span class="sxs-lookup"><span data-stu-id="7c511-546">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="7c511-547">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="7c511-547">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-548">Удаление удаленных строк</span><span class="sxs-lookup"><span data-stu-id="7c511-548">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="7c511-549">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="7c511-549">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-550">Отчет о нескольких изменениях</span><span class="sxs-lookup"><span data-stu-id="7c511-550">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="7c511-551">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="7c511-551">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-552">Возврат ожидающих вставок</span><span class="sxs-lookup"><span data-stu-id="7c511-552">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="7c511-553">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="7c511-553">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-554">Уведомление об удалении строки</span><span class="sxs-lookup"><span data-stu-id="7c511-554">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="7c511-555">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="7c511-555">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-556">Уведомление о первом изменении строки</span><span class="sxs-lookup"><span data-stu-id="7c511-556">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="7c511-557">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="7c511-557">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-558">Уведомление о вставке строк</span><span class="sxs-lookup"><span data-stu-id="7c511-558">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="7c511-559">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="7c511-559">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-560">Права на строки</span><span class="sxs-lookup"><span data-stu-id="7c511-560">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="7c511-561">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="7c511-561">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-562">Уведомление о повторной синхронизации строк</span><span class="sxs-lookup"><span data-stu-id="7c511-562">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="7c511-563">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="7c511-563">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-564">Потоковая модель для строк</span><span class="sxs-lookup"><span data-stu-id="7c511-564">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="7c511-565">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="7c511-565">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-566">Уведомление об отмене изменения строки</span><span class="sxs-lookup"><span data-stu-id="7c511-566">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="7c511-567">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="7c511-567">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-568">Уведомление о отмене удаления строки</span><span class="sxs-lookup"><span data-stu-id="7c511-568">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="7c511-569">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="7c511-569">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-570">Уведомление об отмене вставки строки</span><span class="sxs-lookup"><span data-stu-id="7c511-570">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="7c511-571">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="7c511-571">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-572">Уведомление об обновлении строк</span><span class="sxs-lookup"><span data-stu-id="7c511-572">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="7c511-573">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="7c511-573">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-574">Уведомление об изменении положения при получении набора строк</span><span class="sxs-lookup"><span data-stu-id="7c511-574">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="7c511-575">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="7c511-575">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-576">Уведомление о выпуске набора строк</span><span class="sxs-lookup"><span data-stu-id="7c511-576">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="7c511-577">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="7c511-577">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-578">Прокрутка назад</span><span class="sxs-lookup"><span data-stu-id="7c511-578">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="7c511-579">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="7c511-579">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-580">Серверный курсор</span><span class="sxs-lookup"><span data-stu-id="7c511-580">Server Cursor</span></span></p></td>
<td><p><span data-ttu-id="7c511-581">DBPROP_SERVERCURSOR</span><span class="sxs-lookup"><span data-stu-id="7c511-581">DBPROP_SERVERCURSOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-582">Данные сервера при вставке</span><span class="sxs-lookup"><span data-stu-id="7c511-582">Server Data on Insert</span></span></p></td>
<td><p><span data-ttu-id="7c511-583">DBPROP_SERVERDATAONINSERT</span><span class="sxs-lookup"><span data-stu-id="7c511-583">DBPROP_SERVERDATAONINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-584">Пропуск удаленных закладок</span><span class="sxs-lookup"><span data-stu-id="7c511-584">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="7c511-585">DBPROP_BOOKMARKSKIP</span><span class="sxs-lookup"><span data-stu-id="7c511-585">DBPROP_BOOKMARKSKIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-586">Строгая идентификация строк</span><span class="sxs-lookup"><span data-stu-id="7c511-586">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="7c511-587">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="7c511-587">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-588">Обновление</span><span class="sxs-lookup"><span data-stu-id="7c511-588">Updatability</span></span></p></td>
<td><p><span data-ttu-id="7c511-589">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="7c511-589">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-590">Использование закладок</span><span class="sxs-lookup"><span data-stu-id="7c511-590">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="7c511-591">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="7c511-591">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c511-592">Корень XML</span><span class="sxs-lookup"><span data-stu-id="7c511-592">XML Root</span></span></p></td>
<td><p><span data-ttu-id="7c511-593">SSPROP_STREAM_XMLROOT</span><span class="sxs-lookup"><span data-stu-id="7c511-593">SSPROP_STREAM_XMLROOT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c511-594">XSLT</span><span class="sxs-lookup"><span data-stu-id="7c511-594">XSL</span></span></p></td>
<td><p><span data-ttu-id="7c511-595">SSPROP_STREAM_XSL</span><span class="sxs-lookup"><span data-stu-id="7c511-595">SSPROP_STREAM_XSL</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7c511-596">Для получения подробных сведений о реализации и функциональных сведений о поставщике OLE DB для Microsoft SQL Server обратитесь к документации по поставщику OLE DB для SQL Server в раздел OLE DB компонента MDAC SDK.</span><span class="sxs-lookup"><span data-stu-id="7c511-596">For specific implementation details and functional information about the Microsoft SQL Server OLE DB Provider, consult the OLE DB Provider for SQL Server documentation in the OLE DB section of the MDAC SDK.</span></span>

