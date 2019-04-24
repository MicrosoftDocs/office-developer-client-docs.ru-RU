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
# <a name="microsoft-ole-db-provider-for-sql-server"></a><span data-ttu-id="8173b-102">Поставщик Microsoft OLE DB для SQL Server</span><span class="sxs-lookup"><span data-stu-id="8173b-102">Microsoft OLE DB Provider for SQL Server</span></span>


<span data-ttu-id="8173b-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8173b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8173b-104">Поставщик Microsoft OLE DB для SQL Server, SQLOLEDB позволяет ADO получать доступ к Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8173b-104">The Microsoft OLE DB Provider for SQL Server, SQLOLEDB, allows ADO to access Microsoft SQL Server.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="8173b-105">Параметры строки подключения</span><span class="sxs-lookup"><span data-stu-id="8173b-105">Connection String Parameters</span></span>

<span data-ttu-id="8173b-106">Чтобы подключиться к поставщику, присвойте аргументу *provider* значение свойства [ConnectionString](connectionstring-property-ado.md) следующим образом:</span><span class="sxs-lookup"><span data-stu-id="8173b-106">To connect to this provider, set the *Provider* argument to the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```sql 
 
SQLOLEDB 
```

<span data-ttu-id="8173b-107">Это значение также можно задать или прочитать с помощью свойства [provider](provider-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="8173b-107">This value can also be set or read using the [Provider](provider-property-ado.md) property.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="8173b-108">Типичная строка подключения</span><span class="sxs-lookup"><span data-stu-id="8173b-108">Typical Connection String</span></span>

<span data-ttu-id="8173b-109">Типичная строка подключения для этого поставщика:</span><span class="sxs-lookup"><span data-stu-id="8173b-109">A typical connection string for this provider is:</span></span>

```sql 
 
"Provider=SQLOLEDB;Data Source=serverName;" 
Initial Catalog=databaseName; 
User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="8173b-110">Строка состоит из следующих ключевых слов:</span><span class="sxs-lookup"><span data-stu-id="8173b-110">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8173b-111">Ключевое слово</span><span class="sxs-lookup"><span data-stu-id="8173b-111">Keyword</span></span></p></th>
<th><p><span data-ttu-id="8173b-112">Описание</span><span class="sxs-lookup"><span data-stu-id="8173b-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8173b-113"><strong>Поставщик</strong></span><span class="sxs-lookup"><span data-stu-id="8173b-113"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="8173b-114">Указывает поставщика OLE DB для SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8173b-114">Specifies the OLE DB Provider for SQL Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-115"><strong>Источник данных</strong> или <strong>сервер</strong></span><span class="sxs-lookup"><span data-stu-id="8173b-115"><strong>Data Source</strong> or <strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="8173b-116">Задает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="8173b-116">Specifies the name of a server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-117"><strong>Исходный каталог</strong> или <strong>база данных</strong></span><span class="sxs-lookup"><span data-stu-id="8173b-117"><strong>Initial Catalog</strong> or <strong>Database</strong></span></span></p></td>
<td><p><span data-ttu-id="8173b-118">Задает имя базы данных на сервере.</span><span class="sxs-lookup"><span data-stu-id="8173b-118">Specifies the name of a database on the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-119"><strong>Идентификатор пользователя</strong> или <strong>UID</strong></span><span class="sxs-lookup"><span data-stu-id="8173b-119"><strong>User ID</strong> or <strong>uid</strong></span></span></p></td>
<td><p><span data-ttu-id="8173b-120">Задает имя пользователя (для проверки поДлинности SQL Server).</span><span class="sxs-lookup"><span data-stu-id="8173b-120">Specifies the user name (for SQL Server Authentication).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-121"><strong>Password</strong> или <strong>PWD</strong></span><span class="sxs-lookup"><span data-stu-id="8173b-121"><strong>Password</strong> or <strong>pwd</strong></span></span></p></td>
<td><p><span data-ttu-id="8173b-122">Указывает пароль пользователя (для проверки поДлинности SQL Server).</span><span class="sxs-lookup"><span data-stu-id="8173b-122">Specifies the user password (for SQL Server Authentication).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-connection-parameters"></a><span data-ttu-id="8173b-123">Параметры подключения, зависящие от поставщика</span><span class="sxs-lookup"><span data-stu-id="8173b-123">Provider-Specific Connection Parameters</span></span>

<span data-ttu-id="8173b-124">Поставщик поддерживает несколько параметров подключения, относящихся к поставщику, помимо тех, которые определены в ADO.</span><span class="sxs-lookup"><span data-stu-id="8173b-124">The provider supports several provider-specific connection parameters in addition to those defined by ADO.</span></span> <span data-ttu-id="8173b-125">Как и в случае со свойствами подключения ADO, эти свойства, зависящие от поставщика, можно задать с помощью коллекции [свойств](properties-collection-ado.md) [подключения](connection-object-ado.md) или можно задать в качестве части **ConnectionString**.</span><span class="sxs-lookup"><span data-stu-id="8173b-125">As with the ADO connection properties, these provider-specific properties can be set via the [Properties](properties-collection-ado.md) collection of a [Connection](connection-object-ado.md) or can be set as part of the **ConnectionString**.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8173b-126">Параметр</span><span class="sxs-lookup"><span data-stu-id="8173b-126">Parameter</span></span></p></th>
<th><p><span data-ttu-id="8173b-127">Описание</span><span class="sxs-lookup"><span data-stu-id="8173b-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8173b-128">Трустед_коннектион</span><span class="sxs-lookup"><span data-stu-id="8173b-128">Trusted_Connection</span></span></p></td>
<td><p><span data-ttu-id="8173b-129">Указывает режим проверки подлинности пользователя.</span><span class="sxs-lookup"><span data-stu-id="8173b-129">Indicates the user authentication mode.</span></span> <span data-ttu-id="8173b-130">Для этого может быть задано значение <strong>"Да" или "</strong> <strong>нет</strong>".</span><span class="sxs-lookup"><span data-stu-id="8173b-130">This can be set to <strong>Yes</strong> or <strong>No</strong>.</span></span> <span data-ttu-id="8173b-131">По умолчанию выбрано <strong>Нет</strong>.</span><span class="sxs-lookup"><span data-stu-id="8173b-131">The default value is <strong>No</strong>.</span></span> <span data-ttu-id="8173b-132">Если для этого свойства задано значение <strong>"Да"</strong>, SQLOLEDB использует режим проверки поДлинности Microsoft Windows NT для авторизации доступа пользователей к базе данных SQL Server, указанной значениями свойства <strong>Location</strong> и <a href="datasource-property-ado.md">DataSource</a> .</span><span class="sxs-lookup"><span data-stu-id="8173b-132">If this property is set to <strong>Yes</strong>, then SQLOLEDB uses Microsoft Windows NT Authentication Mode to authorize user access to the SQL Server database specified by the <strong>Location</strong> and <a href="datasource-property-ado.md">Datasource</a> property values.</span></span> <span data-ttu-id="8173b-133">Если для этого свойства установлено значение <strong>нет</strong>, то SQLOLEDB использует смешанный режим для авторизации доступа пользователей к базе данных SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8173b-133">If this property is set to <strong>No</strong>, then SQLOLEDB uses Mixed Mode to authorize user access to the SQL Server database.</span></span> <span data-ttu-id="8173b-134">Имя входа и пароль SQL Server указаны в свойствах <strong>идентификатора пользователя</strong> и <strong>пароля</strong> .</span><span class="sxs-lookup"><span data-stu-id="8173b-134">The SQL Server login and password are specified in the <strong>User Id</strong> and <strong>Password</strong> properties.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-135">Текущий язык</span><span class="sxs-lookup"><span data-stu-id="8173b-135">Current Language</span></span></p></td>
<td><p><span data-ttu-id="8173b-136">Указывает имя языка SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8173b-136">Indicates a SQL Server language name.</span></span> <span data-ttu-id="8173b-137">Определяет язык, используемый для выбора и форматирования системных сообщений.</span><span class="sxs-lookup"><span data-stu-id="8173b-137">Identifies the language used for system message selection and formatting.</span></span> <span data-ttu-id="8173b-138">Язык должен быть установлен на SQL Server, иначе открытие подключения завершится с ошибками.</span><span class="sxs-lookup"><span data-stu-id="8173b-138">The language must be installed on the SQL Server, otherwise opening the connection will fail.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-139">Сетевой адрес</span><span class="sxs-lookup"><span data-stu-id="8173b-139">Network Address</span></span></p></td>
<td><p><span data-ttu-id="8173b-140">Указывает сетевой адрес сервера SQL Server, указанного в свойстве <strong>Location</strong> .</span><span class="sxs-lookup"><span data-stu-id="8173b-140">Indicates the network address of the SQL Server specified by the <strong>Location</strong> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-141">Сетевая библиотека</span><span class="sxs-lookup"><span data-stu-id="8173b-141">Network Library</span></span></p></td>
<td><p><span data-ttu-id="8173b-142">Указывает имя сетевой библиотеки (библиотеки динамической компоновки), используемое для связи с SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8173b-142">Indicates the name of the network library (dynamic-link libraries) used to communicate with the SQL Server.</span></span> <span data-ttu-id="8173b-143">Имя не должно включать в себя путь или расширение DLL.</span><span class="sxs-lookup"><span data-stu-id="8173b-143">The name should not include the path or the .dll file name extension.</span></span> <span data-ttu-id="8173b-144">Значение по умолчанию предоставляется конфигурацией клиента SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8173b-144">The default is provided by the SQL Server client configuration.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-145">Использование процедуры для подготовки</span><span class="sxs-lookup"><span data-stu-id="8173b-145">Use Procedure for Prepare</span></span></p></td>
<td><p><span data-ttu-id="8173b-146">Определяет, создает ли SQL Server временные хранимые процедуры при подготовке команд ( <strong>подготовленном</strong> свойстве).</span><span class="sxs-lookup"><span data-stu-id="8173b-146">Determines whether SQL Server creates temporary stored procedures when Commands are prepared (by the <strong>Prepared</strong> property).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-147">Автоматический перевод</span><span class="sxs-lookup"><span data-stu-id="8173b-147">Auto Translate</span></span></p></td>
<td><p><span data-ttu-id="8173b-148">Указывает, преобразуются ли символы OEM/ANSI.</span><span class="sxs-lookup"><span data-stu-id="8173b-148">Indicates whether OEM/ANSI characters are converted.</span></span> <span data-ttu-id="8173b-149">Для этого свойства можно задать значение <strong>true</strong> или <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="8173b-149">This property can be set to <strong>True</strong> or <strong>False</strong>.</span></span> <span data-ttu-id="8173b-150">Значение по умолчанию — <strong>True</strong>.</span><span class="sxs-lookup"><span data-stu-id="8173b-150">The default value is <strong>True</strong>.</span></span> <span data-ttu-id="8173b-151">Если для этого свойства задано <strong>значение true</strong>, SQLOLEDB выполняет преобразование знаков OEM/ANSI при получении или отправке многобайтовых строк в SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8173b-151">If this property is set to <strong>True</strong>, then SQLOLEDB performs OEM/ANSI character conversion when multi-byte character strings are retrieved from, or sent to, the SQL Server.</span></span> <span data-ttu-id="8173b-152">Если для этого свойства задано <strong>значение false</strong>, SQLOLEDB не выполняет преобразование знаков OEM/ANSI в многобайтовой строке данных с несколькими байтами.</span><span class="sxs-lookup"><span data-stu-id="8173b-152">If this property is set to <strong>False</strong>, then SQLOLEDB does not perform OEM/ANSI character conversion on multi-byte character string data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-153">Размер пакета</span><span class="sxs-lookup"><span data-stu-id="8173b-153">Packet Size</span></span></p></td>
<td><p><span data-ttu-id="8173b-154">Указывает размер сетевого пакета в байтах.</span><span class="sxs-lookup"><span data-stu-id="8173b-154">Indicates a network packet size in bytes.</span></span> <span data-ttu-id="8173b-155">Значение свойства Size Packet должно находиться в пределах от 512 до 32767.</span><span class="sxs-lookup"><span data-stu-id="8173b-155">The packet size property value must be between 512 and 32767.</span></span> <span data-ttu-id="8173b-156">По умолчанию размер пакета для сети SQLOLEDB составляет 4096.</span><span class="sxs-lookup"><span data-stu-id="8173b-156">The default SQLOLEDB network packet size is 4096.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-157">Имя приложения</span><span class="sxs-lookup"><span data-stu-id="8173b-157">Application Name</span></span></p></td>
<td><p><span data-ttu-id="8173b-158">Указывает имя клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="8173b-158">Indicates the client application name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-159">ИДЕНТИФИКАТОР рабочей станции</span><span class="sxs-lookup"><span data-stu-id="8173b-159">Workstation ID</span></span></p></td>
<td><p><span data-ttu-id="8173b-160">Строка, идентифицирующая рабочую станцию.</span><span class="sxs-lookup"><span data-stu-id="8173b-160">A string identifying the workstation.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-object-usage"></a><span data-ttu-id="8173b-161">Использование объекта Command</span><span class="sxs-lookup"><span data-stu-id="8173b-161">Command Object Usage</span></span>

<span data-ttu-id="8173b-162">SQLOLEDB принимает в качестве допустимого синтаксиса амалгам, характерный для ODBC, ANSI и SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8173b-162">SQLOLEDB accepts an amalgam of ODBC, ANSI, and SQL Server-specific Transact-SQL as valid syntax.</span></span> <span data-ttu-id="8173b-163">Например, следующая инструкция SQL использует escape-последовательность ODBC SQL для указания функции строки LCASE:</span><span class="sxs-lookup"><span data-stu-id="8173b-163">For example, the following SQL statement uses an ODBC SQL escape sequence to specify the LCASE string function:</span></span>

```sql 
 
SELECT customerid={fn LCASE(CustomerID)} FROM Customers 
```

<span data-ttu-id="8173b-164">LCASE возвращает строку символов, в которой все прописные символы преобразуются в их эквиваленты в нижнем регистре.</span><span class="sxs-lookup"><span data-stu-id="8173b-164">LCASE returns a character string, converting all uppercase characters to their lowercase equivalents.</span></span> <span data-ttu-id="8173b-165">Функция "строка ANSI SQL" ниже выполняет ту же операцию, поэтому следующая инструкция SQL является эквивалентом ANSI для приведенного выше оператора ODBC:</span><span class="sxs-lookup"><span data-stu-id="8173b-165">The ANSI SQL string function LOWER performs the same operation, so the following SQL statement is an ANSI equivalent to the ODBC statement presented above:</span></span>

```sql
 
SELECT customerid=LOWER(CustomerID) FROM Customers 
```

<span data-ttu-id="8173b-166">SQLOLEDB успешно обрабатывает любую форму оператора при указании в качестве текста для команды.</span><span class="sxs-lookup"><span data-stu-id="8173b-166">SQLOLEDB successfully processes either form of the statement when specified as text for a command.</span></span>

## <a name="stored-procedures"></a><span data-ttu-id="8173b-167">Хранимые процедуры</span><span class="sxs-lookup"><span data-stu-id="8173b-167">Stored Procedures</span></span>

<span data-ttu-id="8173b-168">При выполнении хранимой процедуры SQL Server с помощью команды SQLOLEDB используйте escape-последовательность вызова процедуры ODBC в тексте команды.</span><span class="sxs-lookup"><span data-stu-id="8173b-168">When executing a SQL Server stored procedure using a SQLOLEDB command, use the ODBC procedure call escape sequence in the command text.</span></span> <span data-ttu-id="8173b-169">Затем служба SQLOLEDB использует механизм удаленного вызова процедур SQL Server для оптимизации обработки команд.</span><span class="sxs-lookup"><span data-stu-id="8173b-169">SQLOLEDB then uses the remote procedure call mechanism of SQL Server to optimize command processing.</span></span> <span data-ttu-id="8173b-170">Например, следующая инструкция ODBC SQL является предпочтительным текстом команды в форме Transact-SQL:</span><span class="sxs-lookup"><span data-stu-id="8173b-170">For example, the following ODBC SQL statement is the preferred command text over the Transact-SQL form:</span></span>

## <a name="odbc-sql"></a><span data-ttu-id="8173b-171">ODBC SQL</span><span class="sxs-lookup"><span data-stu-id="8173b-171">ODBC SQL</span></span>

```sql 
 
{call SalesByCategory('Produce', '1995')} 
```

## <a name="transact-sql"></a><span data-ttu-id="8173b-172">Transact SQL</span><span class="sxs-lookup"><span data-stu-id="8173b-172">Transact-SQL</span></span>

```sql 
 
EXECUTE SalesByCategory 'Produce', '1995' 
```

## <a name="recordset-behavior"></a><span data-ttu-id="8173b-173">Поведение набора записей</span><span class="sxs-lookup"><span data-stu-id="8173b-173">Recordset Behavior</span></span>

<span data-ttu-id="8173b-174">SQLOLEDB не может использовать курсоры SQL Server для поддержки множественных результатов, создаваемых многими командами.</span><span class="sxs-lookup"><span data-stu-id="8173b-174">SQLOLEDB cannot use SQL Server cursors to support the multiple-result generated by many commands.</span></span> <span data-ttu-id="8173b-175">Если потребитель запрашивает набор записей, требующий поддержки курсора SQL Server, возникает ошибка, если в качестве результата использован текст команды, который создает больше одного объекта Recordset.</span><span class="sxs-lookup"><span data-stu-id="8173b-175">If a consumer requests a recordset requiring SQL Server cursor support, an error occurs if the command text used generates more than a single recordset as its result.</span></span>

<span data-ttu-id="8173b-176">Прокручиваемые наборы записей SQLOLEDB поддерживаются курсорами SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8173b-176">Scrollable SQLOLEDB recordsets are supported by SQL Server cursors.</span></span> <span data-ttu-id="8173b-177">SQL Server накладывает ограничения на курсоры, которые чувствительны к изменениям, внесенным другими пользователями базы данных.</span><span class="sxs-lookup"><span data-stu-id="8173b-177">SQL Server imposes limitations on cursors that are sensitive to changes made by other users of the database.</span></span> <span data-ttu-id="8173b-178">В частности, строки в некоторых курсорах не могут быть упорядочены, и попытка создать набор записей с помощью команды, содержащей предложение ORDER BY SQL, может привести к сбою.</span><span class="sxs-lookup"><span data-stu-id="8173b-178">Specifically, the rows in some cursors cannot be ordered, and attempting to create a recordset using a command containing an SQL ORDER BY clause can fail.</span></span>

## <a name="dynamic-properties"></a><span data-ttu-id="8173b-179">Динамические свойства</span><span class="sxs-lookup"><span data-stu-id="8173b-179">Dynamic Properties</span></span>

<span data-ttu-id="8173b-180">Поставщик Microsoft OLE DB для SQL Server вставляет несколько динамических свойств в коллекцию **свойств** неоткрытых [подключений](connection-object-ado.md), [наборов записей](recordset-object-ado.md)и командных объектов. [](command-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="8173b-180">The Microsoft OLE DB Provider for SQL Server inserts several dynamic properties into the **Properties** collection of the unopened [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md), and [Command](command-object-ado.md) objects.</span></span>

<span data-ttu-id="8173b-181">В приведенных ниже таблицах указаны перекрестные индексы имен ADO и OLE DB для каждого динамического свойства.</span><span class="sxs-lookup"><span data-stu-id="8173b-181">The following tables are a cross-index of the ADO and OLE DB names for each dynamic property.</span></span> <span data-ttu-id="8173b-182">Справочник программиста OLE DB ссылается на имя свойства ADO по термину "Описание".</span><span class="sxs-lookup"><span data-stu-id="8173b-182">The OLE DB Programmer's Reference refers to an ADO property name by the term "Description."</span></span> <span data-ttu-id="8173b-183">Дополнительные сведения об этих свойствах можно найти в справочнике программиста по OLE DB.</span><span class="sxs-lookup"><span data-stu-id="8173b-183">You can find more information about these properties in the OLE DB Programmer's Reference.</span></span> <span data-ttu-id="8173b-184">Выполните поиск по имени свойства OLE DB в индексе или в разделе приложение C: свойства OLE DB.</span><span class="sxs-lookup"><span data-stu-id="8173b-184">Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span></span>

## <a name="connection-dynamic-properties"></a><span data-ttu-id="8173b-185">Динамические свойства подключения</span><span class="sxs-lookup"><span data-stu-id="8173b-185">Connection Dynamic Properties</span></span>

<span data-ttu-id="8173b-186">Следующие свойства добавляются в коллекцию **свойств** объекта **Connection** .</span><span class="sxs-lookup"><span data-stu-id="8173b-186">The following properties are added to the **Connection** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8173b-187">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="8173b-187">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="8173b-188">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="8173b-188">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8173b-189">Активные сеансы</span><span class="sxs-lookup"><span data-stu-id="8173b-189">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="8173b-190">ДБПРОП_АКТИВЕСЕССИОНС</span><span class="sxs-lookup"><span data-stu-id="8173b-190">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-191">Асинчабле Abort</span><span class="sxs-lookup"><span data-stu-id="8173b-191">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="8173b-192">ДБПРОП_АСИНКТКСНАБОРТ</span><span class="sxs-lookup"><span data-stu-id="8173b-192">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-193">Фиксация Асинчабле</span><span class="sxs-lookup"><span data-stu-id="8173b-193">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="8173b-194">ДБПРОП_АСИНКТНКСКОММИТ</span><span class="sxs-lookup"><span data-stu-id="8173b-194">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-195">Уровни изоляции для автоматической фиксации</span><span class="sxs-lookup"><span data-stu-id="8173b-195">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="8173b-196">ДБПРОП_СЕСС_АУТОКОММИТИСОЛЕВЕЛС</span><span class="sxs-lookup"><span data-stu-id="8173b-196">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-197">Расположение каталога</span><span class="sxs-lookup"><span data-stu-id="8173b-197">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="8173b-198">ДБПРОП_КАТАЛОГЛОКАТИОН</span><span class="sxs-lookup"><span data-stu-id="8173b-198">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-199">Термин каталога</span><span class="sxs-lookup"><span data-stu-id="8173b-199">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="8173b-200">ДБПРОП_КАТАЛОГТЕРМ</span><span class="sxs-lookup"><span data-stu-id="8173b-200">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-201">Определение столбца</span><span class="sxs-lookup"><span data-stu-id="8173b-201">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="8173b-202">ДБПРОП_КОЛУМНДЕФИНИТИОН</span><span class="sxs-lookup"><span data-stu-id="8173b-202">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-203">Время ожидания подключения</span><span class="sxs-lookup"><span data-stu-id="8173b-203">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="8173b-204">ДБПРОП_ИНИТ_ТИМЕАУТ</span><span class="sxs-lookup"><span data-stu-id="8173b-204">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-205">Текущий каталог</span><span class="sxs-lookup"><span data-stu-id="8173b-205">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="8173b-206">ДБПРОП_КУРРЕНТКАТАЛОГ</span><span class="sxs-lookup"><span data-stu-id="8173b-206">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-207">Источник данных</span><span class="sxs-lookup"><span data-stu-id="8173b-207">Data Source</span></span></p></td>
<td><p><span data-ttu-id="8173b-208">ДБПРОП_ИНИТ_ДАТАСАУРЦЕ</span><span class="sxs-lookup"><span data-stu-id="8173b-208">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-209">Имя источника данных</span><span class="sxs-lookup"><span data-stu-id="8173b-209">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="8173b-210">ДБПРОП_ДАТАСАУРЦЕНАМЕ</span><span class="sxs-lookup"><span data-stu-id="8173b-210">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-211">Модель потоков объектов источника данных</span><span class="sxs-lookup"><span data-stu-id="8173b-211">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="8173b-212">ДБПРОП_ДСОСРЕАДМОДЕЛ</span><span class="sxs-lookup"><span data-stu-id="8173b-212">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-213">Имя СУБД</span><span class="sxs-lookup"><span data-stu-id="8173b-213">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="8173b-214">ДБПРОП_ДБМСНАМЕ</span><span class="sxs-lookup"><span data-stu-id="8173b-214">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-215">Версия DBMS</span><span class="sxs-lookup"><span data-stu-id="8173b-215">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="8173b-216">ДБПРОП_ДБМСВЕР</span><span class="sxs-lookup"><span data-stu-id="8173b-216">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-217">Расширенные свойства</span><span class="sxs-lookup"><span data-stu-id="8173b-217">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="8173b-218">ДБПРОП_ИНИТ_ПРОВИДЕРСТРИНГ</span><span class="sxs-lookup"><span data-stu-id="8173b-218">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-219">ГРУППИРОВКа по поддержке</span><span class="sxs-lookup"><span data-stu-id="8173b-219">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="8173b-220">ДБПРОП_ГРАУПБИ</span><span class="sxs-lookup"><span data-stu-id="8173b-220">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-221">Поддержка гетерогенных таблиц</span><span class="sxs-lookup"><span data-stu-id="8173b-221">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="8173b-222">ДБПРОП_ХЕТЕРОЖЕНЕАУСТАБЛЕС</span><span class="sxs-lookup"><span data-stu-id="8173b-222">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-223">Чувствительность к регистру идентификаторов</span><span class="sxs-lookup"><span data-stu-id="8173b-223">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="8173b-224">ДБПРОП_ИДЕНТИФИЕРКАСЕ</span><span class="sxs-lookup"><span data-stu-id="8173b-224">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-225">Исходный каталог</span><span class="sxs-lookup"><span data-stu-id="8173b-225">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="8173b-226">ДБПРОП_ИНИТ_КАТАЛОГ</span><span class="sxs-lookup"><span data-stu-id="8173b-226">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-227">Уровни изоляции</span><span class="sxs-lookup"><span data-stu-id="8173b-227">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="8173b-228">ДБПРОП_СУППОРТЕДТКСНИСОЛЕВЕЛС</span><span class="sxs-lookup"><span data-stu-id="8173b-228">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-229">Хранение изоляции</span><span class="sxs-lookup"><span data-stu-id="8173b-229">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="8173b-230">ДБПРОП_СУППОРТЕДТКСНИСОРЕТАИН</span><span class="sxs-lookup"><span data-stu-id="8173b-230">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-231">Идентификатор языкового стандарта</span><span class="sxs-lookup"><span data-stu-id="8173b-231">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="8173b-232">ДБПРОП_ИНИТ_ЛЦИД</span><span class="sxs-lookup"><span data-stu-id="8173b-232">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-233">Максимальный размер индекса</span><span class="sxs-lookup"><span data-stu-id="8173b-233">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="8173b-234">ДБПРОП_МАКСИНДЕКССИЗЕ</span><span class="sxs-lookup"><span data-stu-id="8173b-234">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-235">Максимальный размер строки</span><span class="sxs-lookup"><span data-stu-id="8173b-235">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="8173b-236">ДБПРОП_МАКСРОВСИЗЕ</span><span class="sxs-lookup"><span data-stu-id="8173b-236">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-237">Максимальный размер строки включает большой ДВОИЧный объект</span><span class="sxs-lookup"><span data-stu-id="8173b-237">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="8173b-238">ДБПРОП_МАКСРОВСИЗЕИНКЛУДЕСБЛОБ</span><span class="sxs-lookup"><span data-stu-id="8173b-238">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-239">Максимальное число таблиц в SELECT</span><span class="sxs-lookup"><span data-stu-id="8173b-239">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="8173b-240">ДБПРОП_МАКСТАБЛЕСИНСЕЛЕКТ</span><span class="sxs-lookup"><span data-stu-id="8173b-240">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-241">Наборы параметров с несколькими параметрами</span><span class="sxs-lookup"><span data-stu-id="8173b-241">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="8173b-242">ДБПРОП_МУЛТИПЛЕПАРАМСЕТС</span><span class="sxs-lookup"><span data-stu-id="8173b-242">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-243">Несколько результатов</span><span class="sxs-lookup"><span data-stu-id="8173b-243">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="8173b-244">ДБПРОП_МУЛТИПЛЕРЕСУЛТС</span><span class="sxs-lookup"><span data-stu-id="8173b-244">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-245">Несколько объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="8173b-245">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="8173b-246">ДБПРОП_МУЛТИПЛЕСТОРАЖЕОБЖЕКТС</span><span class="sxs-lookup"><span data-stu-id="8173b-246">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-247">Обновление с несколькими таблицами</span><span class="sxs-lookup"><span data-stu-id="8173b-247">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="8173b-248">ДБПРОП_МУЛТИТАБЛЕУПДАТЕ</span><span class="sxs-lookup"><span data-stu-id="8173b-248">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-249">Порядок сортировки NULL</span><span class="sxs-lookup"><span data-stu-id="8173b-249">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="8173b-250">ДБПРОП_НУЛЛКОЛЛАТИОН</span><span class="sxs-lookup"><span data-stu-id="8173b-250">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-251">Поведение сцепления со ЗНАЧЕНИЕМ NULL</span><span class="sxs-lookup"><span data-stu-id="8173b-251">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="8173b-252">ДБПРОП_КОНКАТНУЛЛБЕХАВИОР</span><span class="sxs-lookup"><span data-stu-id="8173b-252">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-253">Версия OLE DB</span><span class="sxs-lookup"><span data-stu-id="8173b-253">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="8173b-254">ДБПРОП_ПРОВИДЕРОЛЕДБВЕР</span><span class="sxs-lookup"><span data-stu-id="8173b-254">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-255">Поддержка объектов OLE</span><span class="sxs-lookup"><span data-stu-id="8173b-255">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="8173b-256">ДБПРОП_ОЛЕОБЖЕКТС</span><span class="sxs-lookup"><span data-stu-id="8173b-256">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-257">Поддержка открытых наборов строк</span><span class="sxs-lookup"><span data-stu-id="8173b-257">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="8173b-258">ДБПРОП_ОПЕНРОВСЕТСУППОРТ</span><span class="sxs-lookup"><span data-stu-id="8173b-258">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-259">УПОРЯДОЧЕНие по столбцам в списке выборки</span><span class="sxs-lookup"><span data-stu-id="8173b-259">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="8173b-260">ДБПРОП_ОРДЕРБИКОЛУМНСИНСЕЛЕКТ</span><span class="sxs-lookup"><span data-stu-id="8173b-260">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-261">Доступность выходного параметра</span><span class="sxs-lookup"><span data-stu-id="8173b-261">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="8173b-262">ДБПРОП_АУТПУТПАРАМЕТЕРАВАИЛАБИЛИТИ</span><span class="sxs-lookup"><span data-stu-id="8173b-262">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-263">Передача по параметрам доступа ref</span><span class="sxs-lookup"><span data-stu-id="8173b-263">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="8173b-264">ДБПРОП_БИРЕФАКЦЕССОРС</span><span class="sxs-lookup"><span data-stu-id="8173b-264">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-265">Пароль</span><span class="sxs-lookup"><span data-stu-id="8173b-265">Password</span></span></p></td>
<td><p><span data-ttu-id="8173b-266">ДБПРОП_АУС_ПАССВОРД</span><span class="sxs-lookup"><span data-stu-id="8173b-266">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-267">Сохранение сведений о безопасности</span><span class="sxs-lookup"><span data-stu-id="8173b-267">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="8173b-268">ДБПРОП_АУС_ПЕРСИСТ_СЕНСИТИВЕ_АУСИНФО</span><span class="sxs-lookup"><span data-stu-id="8173b-268">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-269">Тип постоянного идентификатора</span><span class="sxs-lookup"><span data-stu-id="8173b-269">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="8173b-270">ДБПРОП_ПЕРСИСТЕНТИДТИПЕ</span><span class="sxs-lookup"><span data-stu-id="8173b-270">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-271">Действие по подготовке к прерыванию</span><span class="sxs-lookup"><span data-stu-id="8173b-271">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="8173b-272">ДБПРОП_ПРЕПАРЕАБОРТБЕХАВИОР</span><span class="sxs-lookup"><span data-stu-id="8173b-272">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-273">Подготовка режима фиксации</span><span class="sxs-lookup"><span data-stu-id="8173b-273">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="8173b-274">ДБПРОП_ПРЕПАРЕКОММИТБЕХАВИОР</span><span class="sxs-lookup"><span data-stu-id="8173b-274">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-275">Термин процедуры</span><span class="sxs-lookup"><span data-stu-id="8173b-275">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="8173b-276">ДБПРОП_ПРОЦЕДУРЕТЕРМ</span><span class="sxs-lookup"><span data-stu-id="8173b-276">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-277">Prompt</span><span class="sxs-lookup"><span data-stu-id="8173b-277">Prompt</span></span></p></td>
<td><p><span data-ttu-id="8173b-278">ДБПРОП_ИНИТ_ПРОМПТ</span><span class="sxs-lookup"><span data-stu-id="8173b-278">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-279">Понятное имя поставщика</span><span class="sxs-lookup"><span data-stu-id="8173b-279">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="8173b-280">ДБПРОП_ПРОВИДЕРФРИЕНДЛИНАМЕ</span><span class="sxs-lookup"><span data-stu-id="8173b-280">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-281">Имя поставщика</span><span class="sxs-lookup"><span data-stu-id="8173b-281">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="8173b-282">ДБПРОП_ПРОВИДЕРФИЛЕНАМЕ</span><span class="sxs-lookup"><span data-stu-id="8173b-282">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-283">Версия поставщика</span><span class="sxs-lookup"><span data-stu-id="8173b-283">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="8173b-284">ДБПРОП_ПРОВИДЕРВЕР</span><span class="sxs-lookup"><span data-stu-id="8173b-284">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-285">Источник данных, предназначенный только для чтения</span><span class="sxs-lookup"><span data-stu-id="8173b-285">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="8173b-286">ДБПРОП_ДАТАСАУРЦЕРЕАДОНЛИ</span><span class="sxs-lookup"><span data-stu-id="8173b-286">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-287">Преобразования наборов строк для команды</span><span class="sxs-lookup"><span data-stu-id="8173b-287">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="8173b-288">ДБПРОП_РОВСЕТКОНВЕРСИОНСОНКОММАНД</span><span class="sxs-lookup"><span data-stu-id="8173b-288">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-289">Термин схемы</span><span class="sxs-lookup"><span data-stu-id="8173b-289">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="8173b-290">ДБПРОП_СЧЕМАТЕРМ</span><span class="sxs-lookup"><span data-stu-id="8173b-290">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-291">Использование схемы</span><span class="sxs-lookup"><span data-stu-id="8173b-291">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="8173b-292">ДБПРОП_СЧЕМАУСАЖЕ</span><span class="sxs-lookup"><span data-stu-id="8173b-292">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-293">Поддержка SQL</span><span class="sxs-lookup"><span data-stu-id="8173b-293">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="8173b-294">ДБПРОП_СКЛСУППОРТ</span><span class="sxs-lookup"><span data-stu-id="8173b-294">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-295">Структурированное хранилище</span><span class="sxs-lookup"><span data-stu-id="8173b-295">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="8173b-296">ДБПРОП_СТРУКТУРЕДСТОРАЖЕ</span><span class="sxs-lookup"><span data-stu-id="8173b-296">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-297">Поддержка вложенных запросов</span><span class="sxs-lookup"><span data-stu-id="8173b-297">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="8173b-298">ДБПРОП_СУБКУЕРИЕС</span><span class="sxs-lookup"><span data-stu-id="8173b-298">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-299">Табличный термин</span><span class="sxs-lookup"><span data-stu-id="8173b-299">Table Term</span></span></p></td>
<td><p><span data-ttu-id="8173b-300">ДБПРОП_ТАБЛЕТЕРМ</span><span class="sxs-lookup"><span data-stu-id="8173b-300">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-301">DDL транзакции</span><span class="sxs-lookup"><span data-stu-id="8173b-301">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="8173b-302">ДБПРОП_СУППОРТЕДТКСНДДЛ</span><span class="sxs-lookup"><span data-stu-id="8173b-302">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-303">Идентификатор пользователя</span><span class="sxs-lookup"><span data-stu-id="8173b-303">User ID</span></span></p></td>
<td><p><span data-ttu-id="8173b-304">ДБПРОП_АУС_УСЕРИД</span><span class="sxs-lookup"><span data-stu-id="8173b-304">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-305">имя пользователя;</span><span class="sxs-lookup"><span data-stu-id="8173b-305">User Name</span></span></p></td>
<td><p><span data-ttu-id="8173b-306">ДБПРОП_УСЕРНАМЕ</span><span class="sxs-lookup"><span data-stu-id="8173b-306">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-307">Дескриптор окна</span><span class="sxs-lookup"><span data-stu-id="8173b-307">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="8173b-308">ДБПРОП_ИНИТ_ХВНД</span><span class="sxs-lookup"><span data-stu-id="8173b-308">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a><span data-ttu-id="8173b-309">Динамические свойства Recordset</span><span class="sxs-lookup"><span data-stu-id="8173b-309">Recordset Dynamic Properties</span></span>

<span data-ttu-id="8173b-310">Следующие свойства добавляются в коллекцию **свойств** объекта **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="8173b-310">The following properties are added to the **Recordset** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8173b-311">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="8173b-311">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="8173b-312">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="8173b-312">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8173b-313">Порядок доступа</span><span class="sxs-lookup"><span data-stu-id="8173b-313">Access Order</span></span></p></td>
<td><p><span data-ttu-id="8173b-314">ДБПРОП_АКЦЕССОРДЕР</span><span class="sxs-lookup"><span data-stu-id="8173b-314">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-315">Блокировка объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="8173b-315">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="8173b-316">ДБПРОП_БЛОККИНГСТОРАЖЕОБЖЕКТС</span><span class="sxs-lookup"><span data-stu-id="8173b-316">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-317">Тип закладки</span><span class="sxs-lookup"><span data-stu-id="8173b-317">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="8173b-318">ДБПРОП_БУКМАРКТИПЕ</span><span class="sxs-lookup"><span data-stu-id="8173b-318">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-319">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="8173b-319">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="8173b-320">ДБПРОП_ИРОВСЕТЛОКАТЕ</span><span class="sxs-lookup"><span data-stu-id="8173b-320">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-321">Изменение вставленных строк</span><span class="sxs-lookup"><span data-stu-id="8173b-321">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="8173b-322">ДБПРОП_ЧАНЖЕИНСЕРТЕДРОВС</span><span class="sxs-lookup"><span data-stu-id="8173b-322">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-323">Права на столбцы</span><span class="sxs-lookup"><span data-stu-id="8173b-323">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="8173b-324">ДБПРОП_КОЛУМНРЕСТРИКТ</span><span class="sxs-lookup"><span data-stu-id="8173b-324">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-325">Уведомление о наборе столбцов</span><span class="sxs-lookup"><span data-stu-id="8173b-325">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="8173b-326">ДБПРОП_НОТИФИКОЛУМНСЕТ</span><span class="sxs-lookup"><span data-stu-id="8173b-326">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-327">Время ожидания команды</span><span class="sxs-lookup"><span data-stu-id="8173b-327">Command Time Out</span></span></p></td>
<td><p><span data-ttu-id="8173b-328">ДБПРОП_КОММАНДТИМЕАУТ</span><span class="sxs-lookup"><span data-stu-id="8173b-328">DBPROP_COMMANDTIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-329">ОтКладывание столбца</span><span class="sxs-lookup"><span data-stu-id="8173b-329">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="8173b-330">ДБПРОП_ДЕФЕРРЕД</span><span class="sxs-lookup"><span data-stu-id="8173b-330">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-331">ОтКладывание обновлений объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="8173b-331">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="8173b-332">ДБПРОП_ДЕЛАЙСТОРАЖЕОБЖЕКТС</span><span class="sxs-lookup"><span data-stu-id="8173b-332">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-333">Извлечение назад</span><span class="sxs-lookup"><span data-stu-id="8173b-333">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="8173b-334">ДБПРОП_КАНФЕТЧБАККВАРДС</span><span class="sxs-lookup"><span data-stu-id="8173b-334">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-335">Удержание строк</span><span class="sxs-lookup"><span data-stu-id="8173b-335">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="8173b-336">ДБПРОП_КАНХОЛДРОВС</span><span class="sxs-lookup"><span data-stu-id="8173b-336">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-337">Иакцессор</span><span class="sxs-lookup"><span data-stu-id="8173b-337">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="8173b-338">Дбпроп_иакцессор</span><span class="sxs-lookup"><span data-stu-id="8173b-338">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-339">Иколумнсинфо</span><span class="sxs-lookup"><span data-stu-id="8173b-339">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="8173b-340">Дбпроп_иколумнсинфо</span><span class="sxs-lookup"><span data-stu-id="8173b-340">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-341">Иколумнсровсет</span><span class="sxs-lookup"><span data-stu-id="8173b-341">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="8173b-342">Дбпроп_иколумнсровсет</span><span class="sxs-lookup"><span data-stu-id="8173b-342">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-343">Иконнектионпоинтконтаинер</span><span class="sxs-lookup"><span data-stu-id="8173b-343">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="8173b-344">Дбпроп_иконнектионпоинтконтаинер</span><span class="sxs-lookup"><span data-stu-id="8173b-344">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-345">Иконверттипе</span><span class="sxs-lookup"><span data-stu-id="8173b-345">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="8173b-346">Дбпроп_иконверттипе</span><span class="sxs-lookup"><span data-stu-id="8173b-346">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-347">Строки для мобильных устройств</span><span class="sxs-lookup"><span data-stu-id="8173b-347">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="8173b-348">ДБПРОП_ИММОБИЛЕРОВС</span><span class="sxs-lookup"><span data-stu-id="8173b-348">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-349">IRowset</span><span class="sxs-lookup"><span data-stu-id="8173b-349">IRowset</span></span></p></td>
<td><p><span data-ttu-id="8173b-350">Дбпроп_ировсет</span><span class="sxs-lookup"><span data-stu-id="8173b-350">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-351">Ировсетчанже</span><span class="sxs-lookup"><span data-stu-id="8173b-351">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="8173b-352">Дбпроп_ировсетчанже</span><span class="sxs-lookup"><span data-stu-id="8173b-352">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-353">Ировсетидентити</span><span class="sxs-lookup"><span data-stu-id="8173b-353">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="8173b-354">Дбпроп_ировсетидентити</span><span class="sxs-lookup"><span data-stu-id="8173b-354">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-355">Ировсетинфо</span><span class="sxs-lookup"><span data-stu-id="8173b-355">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="8173b-356">Дбпроп_ировсетинфо</span><span class="sxs-lookup"><span data-stu-id="8173b-356">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-357">Ировсетлокате</span><span class="sxs-lookup"><span data-stu-id="8173b-357">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="8173b-358">Дбпроп_ировсестлокате</span><span class="sxs-lookup"><span data-stu-id="8173b-358">DBPROP_IRowsestLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-359">Ировсетресинч</span><span class="sxs-lookup"><span data-stu-id="8173b-359">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-360">Ировсетскролл</span><span class="sxs-lookup"><span data-stu-id="8173b-360">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="8173b-361">Дбпроп_ировсетскролл</span><span class="sxs-lookup"><span data-stu-id="8173b-361">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-362">Ировсетупдате</span><span class="sxs-lookup"><span data-stu-id="8173b-362">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="8173b-363">Дбпроп_ировсетупдате</span><span class="sxs-lookup"><span data-stu-id="8173b-363">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-364">Исекуентиалстреам</span><span class="sxs-lookup"><span data-stu-id="8173b-364">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="8173b-365">Дбпроп_исекуентиалстреам</span><span class="sxs-lookup"><span data-stu-id="8173b-365">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-366">Исуппортерроринфо</span><span class="sxs-lookup"><span data-stu-id="8173b-366">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="8173b-367">Дбпроп_исуппортерроринфо</span><span class="sxs-lookup"><span data-stu-id="8173b-367">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-368">Литеральные закладки</span><span class="sxs-lookup"><span data-stu-id="8173b-368">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="8173b-369">ДБПРОП_ЛИТЕРАЛБУКМАРКС</span><span class="sxs-lookup"><span data-stu-id="8173b-369">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-370">Идентификация строк литералов</span><span class="sxs-lookup"><span data-stu-id="8173b-370">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="8173b-371">ДБПРОП_ЛИТЕРАЛИДЕНТИТИ</span><span class="sxs-lookup"><span data-stu-id="8173b-371">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-372">Максимальное число открытых строк</span><span class="sxs-lookup"><span data-stu-id="8173b-372">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="8173b-373">ДБПРОП_МАКСОПЕНРОВС</span><span class="sxs-lookup"><span data-stu-id="8173b-373">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-374">Максимальное число ожидающих строк</span><span class="sxs-lookup"><span data-stu-id="8173b-374">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="8173b-375">ДБПРОП_МАКСПЕНДИНГРОВС</span><span class="sxs-lookup"><span data-stu-id="8173b-375">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-376">Максимальное число строк</span><span class="sxs-lookup"><span data-stu-id="8173b-376">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="8173b-377">ДБПРОП_МАКСРОВС</span><span class="sxs-lookup"><span data-stu-id="8173b-377">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-378">Детализация уведомлений</span><span class="sxs-lookup"><span data-stu-id="8173b-378">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="8173b-379">ДБПРОП_НОТИФИКАТИОНГРАНУЛАРИТИ</span><span class="sxs-lookup"><span data-stu-id="8173b-379">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-380">Этапы уведомления</span><span class="sxs-lookup"><span data-stu-id="8173b-380">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="8173b-381">ДБПРОП_НОТИФИКАТИОНФАСЕС</span><span class="sxs-lookup"><span data-stu-id="8173b-381">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-382">Объекты, транзакционные</span><span class="sxs-lookup"><span data-stu-id="8173b-382">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="8173b-383">ДБПРОП_ТРАНСАКТЕДОБЖЕКТ</span><span class="sxs-lookup"><span data-stu-id="8173b-383">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-384">Видны другие изменения</span><span class="sxs-lookup"><span data-stu-id="8173b-384">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="8173b-385">ДБПРОП_ОСЕРУПДАТЕДЕЛЕТЕ</span><span class="sxs-lookup"><span data-stu-id="8173b-385">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-386">Видимые вставки других пользователей</span><span class="sxs-lookup"><span data-stu-id="8173b-386">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="8173b-387">ДБПРОП_ОСЕРИНСЕРТ</span><span class="sxs-lookup"><span data-stu-id="8173b-387">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-388">Видны изменения</span><span class="sxs-lookup"><span data-stu-id="8173b-388">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="8173b-389">ДБПРОП_ОВНУПДАТЕДЕЛЕТЕ</span><span class="sxs-lookup"><span data-stu-id="8173b-389">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-390">Отображение собственных вставок</span><span class="sxs-lookup"><span data-stu-id="8173b-390">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="8173b-391">ДБПРОП_ОВНИНСЕРТ</span><span class="sxs-lookup"><span data-stu-id="8173b-391">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-392">Сохранение при прерывании</span><span class="sxs-lookup"><span data-stu-id="8173b-392">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="8173b-393">ДБПРОП_АБОРТПРЕСЕРВЕ</span><span class="sxs-lookup"><span data-stu-id="8173b-393">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-394">Сохранение при фиксации</span><span class="sxs-lookup"><span data-stu-id="8173b-394">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="8173b-395">ДБПРОП_КОММИТПРЕСЕРВЕ</span><span class="sxs-lookup"><span data-stu-id="8173b-395">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-396">Быстрый перезапуск</span><span class="sxs-lookup"><span data-stu-id="8173b-396">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="8173b-397">ДБПРОП_КУИККРЕСТАРТ</span><span class="sxs-lookup"><span data-stu-id="8173b-397">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-398">Повторные события</span><span class="sxs-lookup"><span data-stu-id="8173b-398">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="8173b-399">ДБПРОП_РИНТРАНТЕВЕНТС</span><span class="sxs-lookup"><span data-stu-id="8173b-399">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-400">Удаление удаленных строк</span><span class="sxs-lookup"><span data-stu-id="8173b-400">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="8173b-401">ДБПРОП_РЕМОВЕДЕЛЕТЕД</span><span class="sxs-lookup"><span data-stu-id="8173b-401">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-402">Отчет о нескольких изменениях</span><span class="sxs-lookup"><span data-stu-id="8173b-402">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="8173b-403">ДБПРОП_РЕПОРТМУЛТИПЛЕЧАНЖЕС</span><span class="sxs-lookup"><span data-stu-id="8173b-403">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-404">Возврат ожидающих вставок</span><span class="sxs-lookup"><span data-stu-id="8173b-404">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="8173b-405">ДБПРОП_РЕТУРНПЕНДИНГИНСЕРТС</span><span class="sxs-lookup"><span data-stu-id="8173b-405">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-406">Уведомление об удалении строки</span><span class="sxs-lookup"><span data-stu-id="8173b-406">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="8173b-407">ДБПРОП_НОТИФИРОВДЕЛЕТЕ</span><span class="sxs-lookup"><span data-stu-id="8173b-407">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-408">Уведомление о первом изменении строки</span><span class="sxs-lookup"><span data-stu-id="8173b-408">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="8173b-409">ДБПРОП_НОТИФИРОВФИРСТЧАНЖЕ</span><span class="sxs-lookup"><span data-stu-id="8173b-409">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-410">Уведомление о вставке строк</span><span class="sxs-lookup"><span data-stu-id="8173b-410">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="8173b-411">ДБПРОП_НОТИФИРОВИНСЕРТ</span><span class="sxs-lookup"><span data-stu-id="8173b-411">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-412">Права на строки</span><span class="sxs-lookup"><span data-stu-id="8173b-412">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="8173b-413">ДБПРОП_РОВРЕСТРИКТ</span><span class="sxs-lookup"><span data-stu-id="8173b-413">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-414">Уведомление о повторной синхронизации строк</span><span class="sxs-lookup"><span data-stu-id="8173b-414">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="8173b-415">ДБПРОП_НОТИФИРОВРЕСИНЧ</span><span class="sxs-lookup"><span data-stu-id="8173b-415">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-416">Потоковая модель для строк</span><span class="sxs-lookup"><span data-stu-id="8173b-416">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="8173b-417">ДБПРОП_РОВСРЕАДМОДЕЛ</span><span class="sxs-lookup"><span data-stu-id="8173b-417">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-418">Уведомление об отмене изменения строки</span><span class="sxs-lookup"><span data-stu-id="8173b-418">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="8173b-419">ДБПРОП_НОТИФИРОВУНДОЧАНЖЕ</span><span class="sxs-lookup"><span data-stu-id="8173b-419">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-420">Уведомление о отмене удаления строки</span><span class="sxs-lookup"><span data-stu-id="8173b-420">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="8173b-421">ДБПРОП_НОТИФИРОВУНДОДЕЛЕТЕ</span><span class="sxs-lookup"><span data-stu-id="8173b-421">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-422">Уведомление об отмене вставки строки</span><span class="sxs-lookup"><span data-stu-id="8173b-422">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="8173b-423">ДБПРОП_НОТИФИРОВУНДОИНСЕРТ</span><span class="sxs-lookup"><span data-stu-id="8173b-423">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-424">Уведомление об обновлении строк</span><span class="sxs-lookup"><span data-stu-id="8173b-424">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="8173b-425">ДБПРОП_НОТИФИРОВУПДАТЕ</span><span class="sxs-lookup"><span data-stu-id="8173b-425">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-426">Уведомление об изменении положения при получении набора строк</span><span class="sxs-lookup"><span data-stu-id="8173b-426">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="8173b-427">ДБПРОП_НОТИФИРОВСЕТФЕТЧПОСИСИОНЧАНЖЕ</span><span class="sxs-lookup"><span data-stu-id="8173b-427">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-428">Уведомление о выПуске набора строк</span><span class="sxs-lookup"><span data-stu-id="8173b-428">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="8173b-429">ДБПРОП_НОТИФИРОВСЕТРЕЛЕАСЕ</span><span class="sxs-lookup"><span data-stu-id="8173b-429">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-430">ПроКрутка назад</span><span class="sxs-lookup"><span data-stu-id="8173b-430">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="8173b-431">ДБПРОП_КАНСКРОЛЛБАККВАРДС</span><span class="sxs-lookup"><span data-stu-id="8173b-431">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-432">Серверный курсор</span><span class="sxs-lookup"><span data-stu-id="8173b-432">Server Cursor</span></span></p></td>
<td><p><span data-ttu-id="8173b-433">ДБПРОП_СЕРВЕРКУРСОР</span><span class="sxs-lookup"><span data-stu-id="8173b-433">DBPROP_SERVERCURSOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-434">Пропуск удаленных закладок</span><span class="sxs-lookup"><span data-stu-id="8173b-434">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="8173b-435">ДБПРОП_БУКМАРКСКИППЕД</span><span class="sxs-lookup"><span data-stu-id="8173b-435">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-436">Строгая идентификация строк</span><span class="sxs-lookup"><span data-stu-id="8173b-436">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="8173b-437">ДБПРОП_СТРОНГИТДЕНТИТИ</span><span class="sxs-lookup"><span data-stu-id="8173b-437">DBPROP_STRONGITDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-438">Уникальные строки</span><span class="sxs-lookup"><span data-stu-id="8173b-438">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="8173b-439">ДБПРОП_УНИКУЕРОВС</span><span class="sxs-lookup"><span data-stu-id="8173b-439">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-440">Обновление</span><span class="sxs-lookup"><span data-stu-id="8173b-440">Updatability</span></span></p></td>
<td><p><span data-ttu-id="8173b-441">ДБПРОП_УПДАТАБИЛИТИ</span><span class="sxs-lookup"><span data-stu-id="8173b-441">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-442">Использование закладок</span><span class="sxs-lookup"><span data-stu-id="8173b-442">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="8173b-443">ДБПРОП_БУКМАРКС</span><span class="sxs-lookup"><span data-stu-id="8173b-443">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a><span data-ttu-id="8173b-444">Динамические свойства команд</span><span class="sxs-lookup"><span data-stu-id="8173b-444">Command Dynamic Properties</span></span>

<span data-ttu-id="8173b-445">Указанные ниже свойства добавляются в коллекцию \*\*\*\* **свойств** командного объекта.</span><span class="sxs-lookup"><span data-stu-id="8173b-445">The following properties are added to the **Command** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8173b-446">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="8173b-446">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="8173b-447">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="8173b-447">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8173b-448">Порядок доступа</span><span class="sxs-lookup"><span data-stu-id="8173b-448">Access Order</span></span></p></td>
<td><p><span data-ttu-id="8173b-449">ДБПРОП_АКЦЕССОРДЕР</span><span class="sxs-lookup"><span data-stu-id="8173b-449">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-450">Базовый путь</span><span class="sxs-lookup"><span data-stu-id="8173b-450">Base Path</span></span></p></td>
<td><p><span data-ttu-id="8173b-451">ССПРОП_СТРЕАМ_БАСЕПАС</span><span class="sxs-lookup"><span data-stu-id="8173b-451">SSPROP_STREAM_BASEPATH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-452">Блокировка объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="8173b-452">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="8173b-453">ДБПРОП_БЛОККИНГСТОРАЖЕОБЖЕКТС</span><span class="sxs-lookup"><span data-stu-id="8173b-453">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-454">Тип закладки</span><span class="sxs-lookup"><span data-stu-id="8173b-454">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="8173b-455">ДБПРОП_БУКМАРКТИПЕ</span><span class="sxs-lookup"><span data-stu-id="8173b-455">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-456">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="8173b-456">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="8173b-457">ДБПРОП_ИРОВСЕТЛОКАТЕ</span><span class="sxs-lookup"><span data-stu-id="8173b-457">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-458">Изменение вставленных строк</span><span class="sxs-lookup"><span data-stu-id="8173b-458">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="8173b-459">ДБПРОП_ЧАНЖЕИНСЕРТЕДРОВС</span><span class="sxs-lookup"><span data-stu-id="8173b-459">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-460">Права на столбцы</span><span class="sxs-lookup"><span data-stu-id="8173b-460">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="8173b-461">ДБПРОП_КОЛУМНРЕСТРИКТ</span><span class="sxs-lookup"><span data-stu-id="8173b-461">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-462">Уведомление о наборе столбцов</span><span class="sxs-lookup"><span data-stu-id="8173b-462">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="8173b-463">ДБПРОП_НОТИФИКОЛУМНСЕТ</span><span class="sxs-lookup"><span data-stu-id="8173b-463">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-464">Тип контента</span><span class="sxs-lookup"><span data-stu-id="8173b-464">Content Type</span></span></p></td>
<td><p><span data-ttu-id="8173b-465">ССПРОП_СТРЕАМ_КОНТЕНТТИПЕ</span><span class="sxs-lookup"><span data-stu-id="8173b-465">SSPROP_STREAM_CONTENTTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-466">Автоматическая выборка курсора</span><span class="sxs-lookup"><span data-stu-id="8173b-466">Cursor Auto Fetch</span></span></p></td>
<td><p><span data-ttu-id="8173b-467">ССПРОП_КУРСОРАУТОФЕТЧ</span><span class="sxs-lookup"><span data-stu-id="8173b-467">SSPROP_CURSORAUTOFETCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-468">ОтКладывание столбца</span><span class="sxs-lookup"><span data-stu-id="8173b-468">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="8173b-469">ДБПРОП_ДЕФЕРРЕД</span><span class="sxs-lookup"><span data-stu-id="8173b-469">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-470">ОтЛожить подготовку</span><span class="sxs-lookup"><span data-stu-id="8173b-470">Defer Prepare</span></span></p></td>
<td><p><span data-ttu-id="8173b-471">ССПРОП_ДЕФЕРПРЕПАРЕ</span><span class="sxs-lookup"><span data-stu-id="8173b-471">SSPROP_DEFERPREPARE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-472">ОтКладывание обновлений объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="8173b-472">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="8173b-473">ДБПРОП_ДЕЛАЙСТОРАЖЕОБЖЕКТС</span><span class="sxs-lookup"><span data-stu-id="8173b-473">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-474">Извлечение назад</span><span class="sxs-lookup"><span data-stu-id="8173b-474">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="8173b-475">ДБПРОП_КАНФЕТЧБАККВАРДС</span><span class="sxs-lookup"><span data-stu-id="8173b-475">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-476">Удержание строк</span><span class="sxs-lookup"><span data-stu-id="8173b-476">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="8173b-477">ДБПРОП_КАНХОЛДРОВС</span><span class="sxs-lookup"><span data-stu-id="8173b-477">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-478">Иакцессор</span><span class="sxs-lookup"><span data-stu-id="8173b-478">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="8173b-479">Дбпроп_иакцессор</span><span class="sxs-lookup"><span data-stu-id="8173b-479">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-480">Иколумнсинфо</span><span class="sxs-lookup"><span data-stu-id="8173b-480">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="8173b-481">Дбпроп_иколумнсинфо</span><span class="sxs-lookup"><span data-stu-id="8173b-481">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-482">Иколумнсровсет</span><span class="sxs-lookup"><span data-stu-id="8173b-482">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="8173b-483">Дбпроп_иколумнсровсет</span><span class="sxs-lookup"><span data-stu-id="8173b-483">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-484">Иконнектионпоинтконтаинер</span><span class="sxs-lookup"><span data-stu-id="8173b-484">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="8173b-485">Дбпроп_иконнектионпоинтконтаинер</span><span class="sxs-lookup"><span data-stu-id="8173b-485">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-486">Иконверттипе</span><span class="sxs-lookup"><span data-stu-id="8173b-486">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="8173b-487">Дбпроп_иконверттипе</span><span class="sxs-lookup"><span data-stu-id="8173b-487">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-488">Строки для мобильных устройств</span><span class="sxs-lookup"><span data-stu-id="8173b-488">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="8173b-489">ДБПРОП_ИММОБИЛЕРОВС</span><span class="sxs-lookup"><span data-stu-id="8173b-489">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-490">IRowset</span><span class="sxs-lookup"><span data-stu-id="8173b-490">IRowset</span></span></p></td>
<td><p><span data-ttu-id="8173b-491">Дбпроп_ировсет</span><span class="sxs-lookup"><span data-stu-id="8173b-491">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-492">Ировсетчанже</span><span class="sxs-lookup"><span data-stu-id="8173b-492">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="8173b-493">Дбпроп_ировсетчанже</span><span class="sxs-lookup"><span data-stu-id="8173b-493">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-494">Ировсетидентити</span><span class="sxs-lookup"><span data-stu-id="8173b-494">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="8173b-495">Дбпроп_ировсетидентити</span><span class="sxs-lookup"><span data-stu-id="8173b-495">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-496">Ировсетинфо</span><span class="sxs-lookup"><span data-stu-id="8173b-496">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="8173b-497">Дбпроп_ировсетинфо</span><span class="sxs-lookup"><span data-stu-id="8173b-497">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-498">Ировсетлокате</span><span class="sxs-lookup"><span data-stu-id="8173b-498">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="8173b-499">Дбпроп_ировсетлокате</span><span class="sxs-lookup"><span data-stu-id="8173b-499">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-500">Ировсетресинч</span><span class="sxs-lookup"><span data-stu-id="8173b-500">IRowsetResynch</span></span></p></td>
<td><p><span data-ttu-id="8173b-501">Дбпроп_ировсетресинч</span><span class="sxs-lookup"><span data-stu-id="8173b-501">DBPROP_IRowsetResynch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-502">Ировсетскролл</span><span class="sxs-lookup"><span data-stu-id="8173b-502">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="8173b-503">Дбпроп_ировсетскролл</span><span class="sxs-lookup"><span data-stu-id="8173b-503">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-504">Ировсетупдате</span><span class="sxs-lookup"><span data-stu-id="8173b-504">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="8173b-505">Дбпроп_ировсетупдате</span><span class="sxs-lookup"><span data-stu-id="8173b-505">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-506">Исекуентиалстреам</span><span class="sxs-lookup"><span data-stu-id="8173b-506">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="8173b-507">Дбпроп_исекуентиалстреам</span><span class="sxs-lookup"><span data-stu-id="8173b-507">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-508">Исуппортерроринфо</span><span class="sxs-lookup"><span data-stu-id="8173b-508">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="8173b-509">Дбпроп_исуппортерроринфо</span><span class="sxs-lookup"><span data-stu-id="8173b-509">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-510">Литеральные закладки</span><span class="sxs-lookup"><span data-stu-id="8173b-510">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="8173b-511">ДБПРОП_ЛИТЕРАЛБУКМАРКС</span><span class="sxs-lookup"><span data-stu-id="8173b-511">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-512">Идентификация строк литералов</span><span class="sxs-lookup"><span data-stu-id="8173b-512">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="8173b-513">ДБПРОП_ЛИТЕРАЛИДЕНТИТИ</span><span class="sxs-lookup"><span data-stu-id="8173b-513">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-514">Режим блокировки</span><span class="sxs-lookup"><span data-stu-id="8173b-514">Lock Mode</span></span></p></td>
<td><p><span data-ttu-id="8173b-515">ДБПРОП_ЛОККМОДЕ</span><span class="sxs-lookup"><span data-stu-id="8173b-515">DBPROP_LOCKMODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-516">Максимальное число открытых строк</span><span class="sxs-lookup"><span data-stu-id="8173b-516">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="8173b-517">ДБПРОП_МАКСОПЕНРОВС</span><span class="sxs-lookup"><span data-stu-id="8173b-517">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-518">Максимальное число ожидающих строк</span><span class="sxs-lookup"><span data-stu-id="8173b-518">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="8173b-519">ДБПРОП_МАКСПЕНДИНГРОВС</span><span class="sxs-lookup"><span data-stu-id="8173b-519">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-520">Максимальное число строк</span><span class="sxs-lookup"><span data-stu-id="8173b-520">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="8173b-521">ДБПРОП_МАКСРОВС</span><span class="sxs-lookup"><span data-stu-id="8173b-521">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-522">Детализация уведомлений</span><span class="sxs-lookup"><span data-stu-id="8173b-522">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="8173b-523">ДБПРОП_НОТИФИКАТИОНГРАНУЛАРИТИ</span><span class="sxs-lookup"><span data-stu-id="8173b-523">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-524">Этапы уведомления</span><span class="sxs-lookup"><span data-stu-id="8173b-524">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="8173b-525">ДБПРОП_НОТИФИКАТИОНФАСЕС</span><span class="sxs-lookup"><span data-stu-id="8173b-525">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-526">Объекты, транзакционные</span><span class="sxs-lookup"><span data-stu-id="8173b-526">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="8173b-527">ДБПРОП_ТРАНСАКТЕДОБЖЕКТ</span><span class="sxs-lookup"><span data-stu-id="8173b-527">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-528">Видны другие изменения</span><span class="sxs-lookup"><span data-stu-id="8173b-528">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="8173b-529">ДБПРОП_ОСЕРУПДАТЕДЕЛЕТЕ</span><span class="sxs-lookup"><span data-stu-id="8173b-529">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-530">Видимые вставки других пользователей</span><span class="sxs-lookup"><span data-stu-id="8173b-530">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="8173b-531">ДБПРОП_ОСЕРИНСЕРТ</span><span class="sxs-lookup"><span data-stu-id="8173b-531">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-532">Свойство Encoding вывода</span><span class="sxs-lookup"><span data-stu-id="8173b-532">Output Encoding Property</span></span></p></td>
<td><p><span data-ttu-id="8173b-533">ДБПРОП_АУТПУТЕНКОДИНГ</span><span class="sxs-lookup"><span data-stu-id="8173b-533">DBPROP_OUTPUTENCODING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-534">Свойство потока вывода</span><span class="sxs-lookup"><span data-stu-id="8173b-534">Output Stream Property</span></span></p></td>
<td><p><span data-ttu-id="8173b-535">ДБПРОП_АУТПУТСТРЕАМ</span><span class="sxs-lookup"><span data-stu-id="8173b-535">DBPROP_OUTPUTSTREAM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-536">Видны изменения</span><span class="sxs-lookup"><span data-stu-id="8173b-536">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="8173b-537">ДБПРОП_ОВНУПДАТЕДЕЛЕТЕ</span><span class="sxs-lookup"><span data-stu-id="8173b-537">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-538">Отображение собственных вставок</span><span class="sxs-lookup"><span data-stu-id="8173b-538">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="8173b-539">ДБПРОП_ОВНИНСЕРТ</span><span class="sxs-lookup"><span data-stu-id="8173b-539">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-540">Сохранение при прерывании</span><span class="sxs-lookup"><span data-stu-id="8173b-540">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="8173b-541">ДБПРОП_АБОРТПРЕСЕРВЕ</span><span class="sxs-lookup"><span data-stu-id="8173b-541">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-542">Сохранение при фиксации</span><span class="sxs-lookup"><span data-stu-id="8173b-542">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="8173b-543">ДБПРОП_КОММИТПРЕСЕРВЕ</span><span class="sxs-lookup"><span data-stu-id="8173b-543">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-544">Быстрый перезапуск</span><span class="sxs-lookup"><span data-stu-id="8173b-544">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="8173b-545">ДБПРОП_КУИККРЕСТАРТ</span><span class="sxs-lookup"><span data-stu-id="8173b-545">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-546">Повторные события</span><span class="sxs-lookup"><span data-stu-id="8173b-546">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="8173b-547">ДБПРОП_РИНТРАНТЕВЕНТС</span><span class="sxs-lookup"><span data-stu-id="8173b-547">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-548">Удаление удаленных строк</span><span class="sxs-lookup"><span data-stu-id="8173b-548">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="8173b-549">ДБПРОП_РЕМОВЕДЕЛЕТЕД</span><span class="sxs-lookup"><span data-stu-id="8173b-549">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-550">Отчет о нескольких изменениях</span><span class="sxs-lookup"><span data-stu-id="8173b-550">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="8173b-551">ДБПРОП_РЕПОРТМУЛТИПЛЕЧАНЖЕС</span><span class="sxs-lookup"><span data-stu-id="8173b-551">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-552">Возврат ожидающих вставок</span><span class="sxs-lookup"><span data-stu-id="8173b-552">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="8173b-553">ДБПРОП_РЕТУРНПЕНДИНГИНСЕРТС</span><span class="sxs-lookup"><span data-stu-id="8173b-553">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-554">Уведомление об удалении строки</span><span class="sxs-lookup"><span data-stu-id="8173b-554">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="8173b-555">ДБПРОП_НОТИФИРОВДЕЛЕТЕ</span><span class="sxs-lookup"><span data-stu-id="8173b-555">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-556">Уведомление о первом изменении строки</span><span class="sxs-lookup"><span data-stu-id="8173b-556">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="8173b-557">ДБПРОП_НОТИФИРОВФИРСТЧАНЖЕ</span><span class="sxs-lookup"><span data-stu-id="8173b-557">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-558">Уведомление о вставке строк</span><span class="sxs-lookup"><span data-stu-id="8173b-558">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="8173b-559">ДБПРОП_НОТИФИРОВИНСЕРТ</span><span class="sxs-lookup"><span data-stu-id="8173b-559">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-560">Права на строки</span><span class="sxs-lookup"><span data-stu-id="8173b-560">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="8173b-561">ДБПРОП_РОВРЕСТРИКТ</span><span class="sxs-lookup"><span data-stu-id="8173b-561">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-562">Уведомление о повторной синхронизации строк</span><span class="sxs-lookup"><span data-stu-id="8173b-562">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="8173b-563">ДБПРОП_НОТИФИРОВРЕСИНЧ</span><span class="sxs-lookup"><span data-stu-id="8173b-563">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-564">Потоковая модель для строк</span><span class="sxs-lookup"><span data-stu-id="8173b-564">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="8173b-565">ДБПРОП_РОВСРЕАДМОДЕЛ</span><span class="sxs-lookup"><span data-stu-id="8173b-565">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-566">Уведомление об отмене изменения строки</span><span class="sxs-lookup"><span data-stu-id="8173b-566">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="8173b-567">ДБПРОП_НОТИФИРОВУНДОЧАНЖЕ</span><span class="sxs-lookup"><span data-stu-id="8173b-567">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-568">Уведомление о отмене удаления строки</span><span class="sxs-lookup"><span data-stu-id="8173b-568">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="8173b-569">ДБПРОП_НОТИФИРОВУНДОДЕЛЕТЕ</span><span class="sxs-lookup"><span data-stu-id="8173b-569">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-570">Уведомление об отмене вставки строки</span><span class="sxs-lookup"><span data-stu-id="8173b-570">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="8173b-571">ДБПРОП_НОТИФИРОВУНДОИНСЕРТ</span><span class="sxs-lookup"><span data-stu-id="8173b-571">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-572">Уведомление об обновлении строк</span><span class="sxs-lookup"><span data-stu-id="8173b-572">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="8173b-573">ДБПРОП_НОТИФИРОВУПДАТЕ</span><span class="sxs-lookup"><span data-stu-id="8173b-573">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-574">Уведомление об изменении положения при получении набора строк</span><span class="sxs-lookup"><span data-stu-id="8173b-574">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="8173b-575">ДБПРОП_НОТИФИРОВСЕТФЕТЧПОСИТИОНЧАНЖЕ</span><span class="sxs-lookup"><span data-stu-id="8173b-575">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-576">Уведомление о выПуске набора строк</span><span class="sxs-lookup"><span data-stu-id="8173b-576">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="8173b-577">ДБПРОП_НОТИФИРОВСЕТРЕЛЕАСЕ</span><span class="sxs-lookup"><span data-stu-id="8173b-577">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-578">ПроКрутка назад</span><span class="sxs-lookup"><span data-stu-id="8173b-578">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="8173b-579">ДБПРОП_КАНСКРОЛЛБАККВАРДС</span><span class="sxs-lookup"><span data-stu-id="8173b-579">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-580">Серверный курсор</span><span class="sxs-lookup"><span data-stu-id="8173b-580">Server Cursor</span></span></p></td>
<td><p><span data-ttu-id="8173b-581">ДБПРОП_СЕРВЕРКУРСОР</span><span class="sxs-lookup"><span data-stu-id="8173b-581">DBPROP_SERVERCURSOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-582">Данные сервера при вставке</span><span class="sxs-lookup"><span data-stu-id="8173b-582">Server Data on Insert</span></span></p></td>
<td><p><span data-ttu-id="8173b-583">ДБПРОП_СЕРВЕРДАТАОНИНСЕРТ</span><span class="sxs-lookup"><span data-stu-id="8173b-583">DBPROP_SERVERDATAONINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-584">Пропуск удаленных закладок</span><span class="sxs-lookup"><span data-stu-id="8173b-584">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="8173b-585">ДБПРОП_БУКМАРКСКИП</span><span class="sxs-lookup"><span data-stu-id="8173b-585">DBPROP_BOOKMARKSKIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-586">Строгая идентификация строк</span><span class="sxs-lookup"><span data-stu-id="8173b-586">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="8173b-587">ДБПРОП_СТРОНГИДЕНТИТИ</span><span class="sxs-lookup"><span data-stu-id="8173b-587">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-588">Обновление</span><span class="sxs-lookup"><span data-stu-id="8173b-588">Updatability</span></span></p></td>
<td><p><span data-ttu-id="8173b-589">ДБПРОП_УПДАТАБИЛИТИ</span><span class="sxs-lookup"><span data-stu-id="8173b-589">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-590">Использование закладок</span><span class="sxs-lookup"><span data-stu-id="8173b-590">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="8173b-591">ДБПРОП_БУКМАРКС</span><span class="sxs-lookup"><span data-stu-id="8173b-591">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8173b-592">Корень XML</span><span class="sxs-lookup"><span data-stu-id="8173b-592">XML Root</span></span></p></td>
<td><p><span data-ttu-id="8173b-593">ССПРОП_СТРЕАМ_КСМЛРУТ</span><span class="sxs-lookup"><span data-stu-id="8173b-593">SSPROP_STREAM_XMLROOT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8173b-594">XSLT</span><span class="sxs-lookup"><span data-stu-id="8173b-594">XSL</span></span></p></td>
<td><p><span data-ttu-id="8173b-595">ССПРОП_СТРЕАМ_КССЛ</span><span class="sxs-lookup"><span data-stu-id="8173b-595">SSPROP_STREAM_XSL</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8173b-596">Для получения подробных сведений о реализации и функциональных сведений о поставщике OLE DB для Microsoft SQL Server обратитесь к документации по поставщику OLE DB для SQL Server в раздел OLE DB компонента MDAC SDK.</span><span class="sxs-lookup"><span data-stu-id="8173b-596">For specific implementation details and functional information about the Microsoft SQL Server OLE DB Provider, consult the OLE DB Provider for SQL Server documentation in the OLE DB section of the MDAC SDK.</span></span>

