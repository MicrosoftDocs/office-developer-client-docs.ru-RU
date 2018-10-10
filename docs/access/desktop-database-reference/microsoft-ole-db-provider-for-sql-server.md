---
title: Microsoft OLE DB Provider for SQL Server
TOCTitle: Microsoft OLE DB Provider for SQL Server
ms:assetid: 0ffdea03-1a76-499b-f649-423f6b3c13d7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248868(v=office.15)
ms:contentKeyID: 48543282
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f999f9268511fd23f1fc6a20c8459d11345ceb4f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480787"
---
# <a name="microsoft-ole-db-provider-for-sql-server"></a><span data-ttu-id="dd378-102">Microsoft OLE DB Provider for SQL Server</span><span class="sxs-lookup"><span data-stu-id="dd378-102">Microsoft OLE DB Provider for SQL Server</span></span>


<span data-ttu-id="dd378-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="dd378-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="dd378-104">Поставщик Microsoft OLE DB для SQL Server, SQLOLEDB, позволяет ADO для доступа к Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="dd378-104">The Microsoft OLE DB Provider for SQL Server, SQLOLEDB, allows ADO to access Microsoft SQL Server.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="dd378-105">Параметры строки подключения</span><span class="sxs-lookup"><span data-stu-id="dd378-105">Connection String Parameters</span></span>

<span data-ttu-id="dd378-106">Для подключения к данным поставщиком аргументе *поставщика* свойство [ConnectionString](connectionstring-property-ado.md) для:</span><span class="sxs-lookup"><span data-stu-id="dd378-106">To connect to this provider, set the *Provider* argument to the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```sql 
 
SQLOLEDB 
```

<span data-ttu-id="dd378-107">Это значение может быть задана или ознакомьтесь с помощью свойства [поставщика](provider-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="dd378-107">This value can also be set or read using the [Provider](provider-property-ado.md) property.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="dd378-108">Типичная строка подключения</span><span class="sxs-lookup"><span data-stu-id="dd378-108">Typical Connection String</span></span>

<span data-ttu-id="dd378-109">— Это строка соединения для данного поставщика:</span><span class="sxs-lookup"><span data-stu-id="dd378-109">A typical connection string for this provider is:</span></span>

```sql 
 
"Provider=SQLOLEDB;Data Source=serverName;" 
Initial Catalog=databaseName; 
User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="dd378-110">Строка состоит из следующих ключевых слов:</span><span class="sxs-lookup"><span data-stu-id="dd378-110">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dd378-111">Keyword</span><span class="sxs-lookup"><span data-stu-id="dd378-111">Keyword</span></span></p></th>
<th><p><span data-ttu-id="dd378-112">Описание</span><span class="sxs-lookup"><span data-stu-id="dd378-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dd378-113"><strong>Поставщик</strong></span><span class="sxs-lookup"><span data-stu-id="dd378-113"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="dd378-114">Задает поставщика OLE DB для SQL Server.</span><span class="sxs-lookup"><span data-stu-id="dd378-114">Specifies the OLE DB Provider for SQL Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-115"><strong>Источник данных</strong> или <strong>сервера</strong></span><span class="sxs-lookup"><span data-stu-id="dd378-115"><strong>Data Source</strong> or <strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="dd378-116">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="dd378-116">Specifies the name of a server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-117"><strong>Исходный каталог</strong> или <strong>База данных</strong></span><span class="sxs-lookup"><span data-stu-id="dd378-117"><strong>Initial Catalog</strong> or <strong>Database</strong></span></span></p></td>
<td><p><span data-ttu-id="dd378-118">Указывает имя базы данных на сервере.</span><span class="sxs-lookup"><span data-stu-id="dd378-118">Specifies the name of a database on the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-119"><strong>Идентификатор пользователя</strong> или <strong>ИД пользователя</strong></span><span class="sxs-lookup"><span data-stu-id="dd378-119"><strong>User ID</strong> or <strong>uid</strong></span></span></p></td>
<td><p><span data-ttu-id="dd378-120">Задает имя пользователя (для проверки подлинности SQL Server).</span><span class="sxs-lookup"><span data-stu-id="dd378-120">Specifies the user name (for SQL Server Authentication).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-121"><strong>Пароль</strong> или <strong>pwd</strong></span><span class="sxs-lookup"><span data-stu-id="dd378-121"><strong>Password</strong> or <strong>pwd</strong></span></span></p></td>
<td><p><span data-ttu-id="dd378-122">Задает пароль пользователя (для проверки подлинности SQL Server).</span><span class="sxs-lookup"><span data-stu-id="dd378-122">Specifies the user password (for SQL Server Authentication).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-connection-parameters"></a><span data-ttu-id="dd378-123">Параметры подключения от поставщика</span><span class="sxs-lookup"><span data-stu-id="dd378-123">Provider-Specific Connection Parameters</span></span>

<span data-ttu-id="dd378-124">Поставщик поддерживает несколько параметров подключения для конкретного поставщика дополнение к тем определяется ADO.</span><span class="sxs-lookup"><span data-stu-id="dd378-124">The provider supports several provider-specific connection parameters in addition to those defined by ADO.</span></span> <span data-ttu-id="dd378-125">Как и в случае с помощью свойства подключения ADO, эти свойства от поставщика можно задать с помощью коллекции [свойств](properties-collection-ado.md) [подключения](connection-object-ado.md) или можно задать как часть **ConnectionString**.</span><span class="sxs-lookup"><span data-stu-id="dd378-125">As with the ADO connection properties, these provider-specific properties can be set via the [Properties](properties-collection-ado.md) collection of a [Connection](connection-object-ado.md) or can be set as part of the **ConnectionString**.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dd378-126">Параметр</span><span class="sxs-lookup"><span data-stu-id="dd378-126">Parameter</span></span></p></th>
<th><p><span data-ttu-id="dd378-127">Описание</span><span class="sxs-lookup"><span data-stu-id="dd378-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dd378-128">Trusted_Connection</span><span class="sxs-lookup"><span data-stu-id="dd378-128">Trusted_Connection</span></span></p></td>
<td><p><span data-ttu-id="dd378-129">Указывает режим проверки подлинности пользователя.</span><span class="sxs-lookup"><span data-stu-id="dd378-129">Indicates the user authentication mode.</span></span> <span data-ttu-id="dd378-130">Это может быть значение <strong>Да</strong> или <strong>Нет</strong>.</span><span class="sxs-lookup"><span data-stu-id="dd378-130">This can be set to <strong>Yes</strong> or <strong>No</strong>.</span></span> <span data-ttu-id="dd378-131">Значение по умолчанию — <strong>Нет</strong>.</span><span class="sxs-lookup"><span data-stu-id="dd378-131">The default value is <strong>No</strong>.</span></span> <span data-ttu-id="dd378-132">Если это свойство имеет значение <strong>Да</strong>, SQLOLEDB использует режим проверки подлинности Microsoft Windows NT для авторизации доступа пользователей к базе данных SQL Server, заданные значения свойств <strong>расположение</strong> и <a href="datasource-property-ado.md">источника данных</a> .</span><span class="sxs-lookup"><span data-stu-id="dd378-132">If this property is set to <strong>Yes</strong>, then SQLOLEDB uses Microsoft Windows NT Authentication Mode to authorize user access to the SQL Server database specified by the <strong>Location</strong> and <a href="datasource-property-ado.md">Datasource</a> property values.</span></span> <span data-ttu-id="dd378-133">Если задано значение <strong>No</strong>, SQLOLEDB использует смешанный режим для авторизации доступа пользователей к базе данных SQL Server.</span><span class="sxs-lookup"><span data-stu-id="dd378-133">If this property is set to <strong>No</strong>, then SQLOLEDB uses Mixed Mode to authorize user access to the SQL Server database.</span></span> <span data-ttu-id="dd378-134">Имя пользователя SQL Server и пароль указанных в свойствах <strong>Идентификатор пользователя</strong> и <strong>пароль</strong> .</span><span class="sxs-lookup"><span data-stu-id="dd378-134">The SQL Server login and password are specified in the <strong>User Id</strong> and <strong>Password</strong> properties.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-135">Текущий язык</span><span class="sxs-lookup"><span data-stu-id="dd378-135">Current Language</span></span></p></td>
<td><p><span data-ttu-id="dd378-136">Указывает имя языка SQL Server.</span><span class="sxs-lookup"><span data-stu-id="dd378-136">Indicates a SQL Server language name.</span></span> <span data-ttu-id="dd378-137">Определяет язык, используемый для выбора сообщения системы и форматирование.</span><span class="sxs-lookup"><span data-stu-id="dd378-137">Identifies the language used for system message selection and formatting.</span></span> <span data-ttu-id="dd378-138">Язык должны быть установлены на SQL Server, в противном случае — открытие подключение завершится с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="dd378-138">The language must be installed on the SQL Server, otherwise opening the connection will fail.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-139">Адрес сети</span><span class="sxs-lookup"><span data-stu-id="dd378-139">Network Address</span></span></p></td>
<td><p><span data-ttu-id="dd378-140">Указывает адрес сети SQL Server, заданного в свойстве <strong>расположение</strong> .</span><span class="sxs-lookup"><span data-stu-id="dd378-140">Indicates the network address of the SQL Server specified by the <strong>Location</strong> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-141">Сетевой библиотеки</span><span class="sxs-lookup"><span data-stu-id="dd378-141">Network Library</span></span></p></td>
<td><p><span data-ttu-id="dd378-142">Указывает имя библиотеки сети (библиотеки динамической компоновки), используемое для взаимодействия с SQL Server.</span><span class="sxs-lookup"><span data-stu-id="dd378-142">Indicates the name of the network library (dynamic-link libraries) used to communicate with the SQL Server.</span></span> <span data-ttu-id="dd378-143">Имя не должно содержать путь или расширение имени файла библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="dd378-143">The name should not include the path or the .dll file name extension.</span></span> <span data-ttu-id="dd378-144">Значение по умолчанию, предоставленные конфигурация клиента SQL Server.</span><span class="sxs-lookup"><span data-stu-id="dd378-144">The default is provided by the SQL Server client configuration.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-145">Используйте процедуру для подготовки</span><span class="sxs-lookup"><span data-stu-id="dd378-145">Use Procedure for Prepare</span></span></p></td>
<td><p><span data-ttu-id="dd378-146">Определяет, будет ли SQL Server создает временные хранимые процедуры, когда команды подготавливаются (свойством <strong>подготовленных</strong> ).</span><span class="sxs-lookup"><span data-stu-id="dd378-146">Determines whether SQL Server creates temporary stored procedures when Commands are prepared (by the <strong>Prepared</strong> property).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-147">Переводить Auto</span><span class="sxs-lookup"><span data-stu-id="dd378-147">Auto Translate</span></span></p></td>
<td><p><span data-ttu-id="dd378-148">Указывает необходимость преобразования символов OEM или ANSI.</span><span class="sxs-lookup"><span data-stu-id="dd378-148">Indicates whether OEM/ANSI characters are converted.</span></span> <span data-ttu-id="dd378-149">Это свойство может иметь значение <strong>True</strong> или <strong>False</strong>.</span><span class="sxs-lookup"><span data-stu-id="dd378-149">This property can be set to <strong>True</strong> or <strong>False</strong>.</span></span> <span data-ttu-id="dd378-150">Значение по умолчанию — <strong>True</strong>.</span><span class="sxs-lookup"><span data-stu-id="dd378-150">The default value is <strong>True</strong>.</span></span> <span data-ttu-id="dd378-151">Если этому свойству присвоено <strong>значение True</strong>, SQLOLEDB выполняет преобразование символов OEM или ANSI при строк символов нескольких байтов извлекается из или отправленные к серверу SQL Server.</span><span class="sxs-lookup"><span data-stu-id="dd378-151">If this property is set to <strong>True</strong>, then SQLOLEDB performs OEM/ANSI character conversion when multi-byte character strings are retrieved from, or sent to, the SQL Server.</span></span> <span data-ttu-id="dd378-152">Если этому свойству присвоено <strong>значение False</strong>, затем SQLOLEDB не выполняет преобразование символов OEM или ANSI на символ нескольких байтов строковых данных.</span><span class="sxs-lookup"><span data-stu-id="dd378-152">If this property is set to <strong>False</strong>, then SQLOLEDB does not perform OEM/ANSI character conversion on multi-byte character string data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-153">Размер пакета</span><span class="sxs-lookup"><span data-stu-id="dd378-153">Packet Size</span></span></p></td>
<td><p><span data-ttu-id="dd378-154">Указывает размер сетевого пакета в байтах.</span><span class="sxs-lookup"><span data-stu-id="dd378-154">Indicates a network packet size in bytes.</span></span> <span data-ttu-id="dd378-155">Значение свойства размера пакета должно быть от 512 до 32 767.</span><span class="sxs-lookup"><span data-stu-id="dd378-155">The packet size property value must be between 512 and 32767.</span></span> <span data-ttu-id="dd378-156">Размер пакета сети SQLOLEDB по умолчанию — 4096.</span><span class="sxs-lookup"><span data-stu-id="dd378-156">The default SQLOLEDB network packet size is 4096.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-157">Имя приложения</span><span class="sxs-lookup"><span data-stu-id="dd378-157">Application Name</span></span></p></td>
<td><p><span data-ttu-id="dd378-158">Указывает имя клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="dd378-158">Indicates the client application name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-159">Идентификатор рабочей станции</span><span class="sxs-lookup"><span data-stu-id="dd378-159">Workstation ID</span></span></p></td>
<td><p><span data-ttu-id="dd378-160">Строка, идентифицирующая рабочей станции.</span><span class="sxs-lookup"><span data-stu-id="dd378-160">A string identifying the workstation.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-object-usage"></a><span data-ttu-id="dd378-161">Использование объекта команды</span><span class="sxs-lookup"><span data-stu-id="dd378-161">Command Object Usage</span></span>

<span data-ttu-id="dd378-162">SQLOLEDB принимает сочетание ODBC, ANSI и Transact-SQL, относящиеся к SQL Server в качестве допустимого синтаксиса.</span><span class="sxs-lookup"><span data-stu-id="dd378-162">SQLOLEDB accepts an amalgam of ODBC, ANSI, and SQL Server-specific Transact-SQL as valid syntax.</span></span> <span data-ttu-id="dd378-163">К примеру следующей инструкции SQL использует escape-последовательности ODBC SQL для указания функция LCASE string:</span><span class="sxs-lookup"><span data-stu-id="dd378-163">For example, the following SQL statement uses an ODBC SQL escape sequence to specify the LCASE string function:</span></span>

```sql 
 
SELECT customerid={fn LCASE(CustomerID)} FROM Customers 
```

<span data-ttu-id="dd378-164">LCASE возвращает строку символов, преобразование все прописные буквы в нижнем регистре эквиваленты.</span><span class="sxs-lookup"><span data-stu-id="dd378-164">LCASE returns a character string, converting all uppercase characters to their lowercase equivalents.</span></span> <span data-ttu-id="dd378-165">Функция string ANSI SQL НИЖНЕМ выполняет одной и той же операции, поэтому следующей инструкции SQL — это эквивалентно оператор ODBC, представленному выше ANSI:</span><span class="sxs-lookup"><span data-stu-id="dd378-165">The ANSI SQL string function LOWER performs the same operation, so the following SQL statement is an ANSI equivalent to the ODBC statement presented above:</span></span>

```sql
 
SELECT customerid=LOWER(CustomerID) FROM Customers 
```

<span data-ttu-id="dd378-166">SQLOLEDB успешно обрабатывает в любом из оператора, когда он указан как текст для команды.</span><span class="sxs-lookup"><span data-stu-id="dd378-166">SQLOLEDB successfully processes either form of the statement when specified as text for a command.</span></span>

## <a name="stored-procedures"></a><span data-ttu-id="dd378-167">Хранимые процедуры</span><span class="sxs-lookup"><span data-stu-id="dd378-167">Stored Procedures</span></span>

<span data-ttu-id="dd378-168">При выполнении SQL Server хранимой процедуры с помощью команды SQLOLEDB, используйте escape-последовательность вызовов ODBC процедуры в текст команды.</span><span class="sxs-lookup"><span data-stu-id="dd378-168">When executing a SQL Server stored procedure using a SQLOLEDB command, use the ODBC procedure call escape sequence in the command text.</span></span> <span data-ttu-id="dd378-169">SQLOLEDB затем использует механизм вызова удаленной процедуры из SQL Server для оптимизации обработки команд.</span><span class="sxs-lookup"><span data-stu-id="dd378-169">SQLOLEDB then uses the remote procedure call mechanism of SQL Server to optimize command processing.</span></span> <span data-ttu-id="dd378-170">К примеру следующей инструкции ODBC SQL окончена текст предпочитаемый команды формы Transact-SQL:</span><span class="sxs-lookup"><span data-stu-id="dd378-170">For example, the following ODBC SQL statement is the preferred command text over the Transact-SQL form:</span></span>

## <a name="odbc-sql"></a><span data-ttu-id="dd378-171">ODBC SQL</span><span class="sxs-lookup"><span data-stu-id="dd378-171">ODBC SQL</span></span>

```sql 
 
{call SalesByCategory('Produce', '1995')} 
```

## <a name="transact-sql"></a><span data-ttu-id="dd378-172">Transact-SQL</span><span class="sxs-lookup"><span data-stu-id="dd378-172">Transact-SQL</span></span>

```sql 
 
EXECUTE SalesByCategory 'Produce', '1995' 
```

## <a name="recordset-behavior"></a><span data-ttu-id="dd378-173">Поведение набора записей</span><span class="sxs-lookup"><span data-stu-id="dd378-173">Recordset Behavior</span></span>

<span data-ttu-id="dd378-174">SQLOLEDB нельзя использовать курсоры SQL Server для поддержки нескольких результатов, созданных функцией многие команды.</span><span class="sxs-lookup"><span data-stu-id="dd378-174">SQLOLEDB cannot use SQL Server cursors to support the multiple-result generated by many commands.</span></span> <span data-ttu-id="dd378-175">Потребитель запрашивает записей, требуя поддержки курсора SQL Server, если используется текст команды создает более чем одного набора записей в результате возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="dd378-175">If a consumer requests a recordset requiring SQL Server cursor support, an error occurs if the command text used generates more than a single recordset as its result.</span></span>

<span data-ttu-id="dd378-176">Прокручиваемой наборов записей SQLOLEDB поддерживаемых курсоров SQL Server.</span><span class="sxs-lookup"><span data-stu-id="dd378-176">Scrollable SQLOLEDB recordsets are supported by SQL Server cursors.</span></span> <span data-ttu-id="dd378-177">SQL Server, задает ограничения на курсоров, зависит от изменения, внесенные другими пользователями базы данных.</span><span class="sxs-lookup"><span data-stu-id="dd378-177">SQL Server imposes limitations on cursors that are sensitive to changes made by other users of the database.</span></span> <span data-ttu-id="dd378-178">В частности строки в некоторые курсоры не могут быть упорядочены и попытка создания набора записей с помощью команды, содержащий предложение SQL ORDER BY может не работать.</span><span class="sxs-lookup"><span data-stu-id="dd378-178">Specifically, the rows in some cursors cannot be ordered, and attempting to create a recordset using a command containing an SQL ORDER BY clause can fail.</span></span>

## <a name="dynamic-properties"></a><span data-ttu-id="dd378-179">Динамические свойства</span><span class="sxs-lookup"><span data-stu-id="dd378-179">Dynamic Properties</span></span>

<span data-ttu-id="dd378-180">Поставщик Microsoft OLE DB для SQL Server вставляет несколько динамических свойств в коллекцию **свойств** объектов неоткрытый [подключения](connection-object-ado.md), [записей](recordset-object-ado.md)и [команды](command-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="dd378-180">The Microsoft OLE DB Provider for SQL Server inserts several dynamic properties into the **Properties** collection of the unopened [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md), and [Command](command-object-ado.md) objects.</span></span>

<span data-ttu-id="dd378-181">Следующие таблицы не cross-index имен ADO и OLE DB для каждого динамического свойства.</span><span class="sxs-lookup"><span data-stu-id="dd378-181">The following tables are a cross-index of the ADO and OLE DB names for each dynamic property.</span></span> <span data-ttu-id="dd378-182">Справочник программиста OLE DB указано имя свойства ADO по слову «Описание».</span><span class="sxs-lookup"><span data-stu-id="dd378-182">The OLE DB Programmer's Reference refers to an ADO property name by the term "Description."</span></span> <span data-ttu-id="dd378-183">Дополнительные сведения об этих свойств можно найти в Справочник программиста OLE DB.</span><span class="sxs-lookup"><span data-stu-id="dd378-183">You can find more information about these properties in the OLE DB Programmer's Reference.</span></span> <span data-ttu-id="dd378-184">Поиск имени свойства OLE DB в индексе или просмотреть приложение C: OLE DB свойства.</span><span class="sxs-lookup"><span data-stu-id="dd378-184">Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span></span>

## <a name="connection-dynamic-properties"></a><span data-ttu-id="dd378-185">Динамические свойства подключения</span><span class="sxs-lookup"><span data-stu-id="dd378-185">Connection Dynamic Properties</span></span>

<span data-ttu-id="dd378-186">Коллекция **Properties** объект **подключения** добавляются следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="dd378-186">The following properties are added to the **Connection** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dd378-187">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="dd378-187">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="dd378-188">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="dd378-188">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dd378-189">Активных сеансов</span><span class="sxs-lookup"><span data-stu-id="dd378-189">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="dd378-190">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="dd378-190">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-191">Прерывание Asynchable</span><span class="sxs-lookup"><span data-stu-id="dd378-191">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="dd378-192">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="dd378-192">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-193">Зафиксировать Asynchable</span><span class="sxs-lookup"><span data-stu-id="dd378-193">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="dd378-194">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="dd378-194">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-195">Уровни изоляции автоматической фиксации</span><span class="sxs-lookup"><span data-stu-id="dd378-195">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="dd378-196">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="dd378-196">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-197">Расположение каталога</span><span class="sxs-lookup"><span data-stu-id="dd378-197">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="dd378-198">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="dd378-198">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-199">Каталог терминов</span><span class="sxs-lookup"><span data-stu-id="dd378-199">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="dd378-200">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="dd378-200">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-201">Определение столбца</span><span class="sxs-lookup"><span data-stu-id="dd378-201">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="dd378-202">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="dd378-202">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-203">Время ожидания подключения</span><span class="sxs-lookup"><span data-stu-id="dd378-203">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="dd378-204">DBPROP_INIT_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="dd378-204">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-205">Текущий каталог</span><span class="sxs-lookup"><span data-stu-id="dd378-205">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="dd378-206">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="dd378-206">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-207">Источник данных</span><span class="sxs-lookup"><span data-stu-id="dd378-207">Data Source</span></span></p></td>
<td><p><span data-ttu-id="dd378-208">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="dd378-208">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-209">Имя источника данных</span><span class="sxs-lookup"><span data-stu-id="dd378-209">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="dd378-210">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="dd378-210">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-211">Модель потоков объекта источника данных</span><span class="sxs-lookup"><span data-stu-id="dd378-211">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="dd378-212">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="dd378-212">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-213">Имя СУБД</span><span class="sxs-lookup"><span data-stu-id="dd378-213">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="dd378-214">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="dd378-214">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-215">Версия СУБД</span><span class="sxs-lookup"><span data-stu-id="dd378-215">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="dd378-216">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="dd378-216">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-217">Расширенные свойства</span><span class="sxs-lookup"><span data-stu-id="dd378-217">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="dd378-218">DBPROP_INIT_PROVIDERSTRING</span><span class="sxs-lookup"><span data-stu-id="dd378-218">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-219">ГРУППИРОВКА по поддержке</span><span class="sxs-lookup"><span data-stu-id="dd378-219">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="dd378-220">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="dd378-220">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-221">Поддержка разнородных таблиц</span><span class="sxs-lookup"><span data-stu-id="dd378-221">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="dd378-222">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="dd378-222">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-223">Идентификатор регистра</span><span class="sxs-lookup"><span data-stu-id="dd378-223">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="dd378-224">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="dd378-224">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-225">Исходный каталог</span><span class="sxs-lookup"><span data-stu-id="dd378-225">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="dd378-226">DBPROP_INIT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dd378-226">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-227">Уровни изоляции</span><span class="sxs-lookup"><span data-stu-id="dd378-227">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="dd378-228">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="dd378-228">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-229">Хранение изоляции</span><span class="sxs-lookup"><span data-stu-id="dd378-229">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="dd378-230">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="dd378-230">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-231">Идентификатор языка</span><span class="sxs-lookup"><span data-stu-id="dd378-231">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="dd378-232">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="dd378-232">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-233">Максимальный размер индекса</span><span class="sxs-lookup"><span data-stu-id="dd378-233">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="dd378-234">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="dd378-234">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-235">Максимальный размер строки</span><span class="sxs-lookup"><span data-stu-id="dd378-235">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="dd378-236">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="dd378-236">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-237">Максимальный размер строки включает в себя больших двоичных ОБЪЕКТОВ</span><span class="sxs-lookup"><span data-stu-id="dd378-237">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="dd378-238">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="dd378-238">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-239">Максимальная таблиц в Выбор</span><span class="sxs-lookup"><span data-stu-id="dd378-239">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="dd378-240">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="dd378-240">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-241">Несколько наборов параметров</span><span class="sxs-lookup"><span data-stu-id="dd378-241">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="dd378-242">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="dd378-242">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-243">Несколько результатов</span><span class="sxs-lookup"><span data-stu-id="dd378-243">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="dd378-244">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="dd378-244">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-245">Несколько объектов хранения</span><span class="sxs-lookup"><span data-stu-id="dd378-245">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="dd378-246">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="dd378-246">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-247">Обновление нескольких таблицы</span><span class="sxs-lookup"><span data-stu-id="dd378-247">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="dd378-248">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="dd378-248">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-249">Порядок сортировки значений NULL</span><span class="sxs-lookup"><span data-stu-id="dd378-249">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="dd378-250">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="dd378-250">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-251">Поведение NULL объединения</span><span class="sxs-lookup"><span data-stu-id="dd378-251">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="dd378-252">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="dd378-252">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-253">Версия OLE DB</span><span class="sxs-lookup"><span data-stu-id="dd378-253">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="dd378-254">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="dd378-254">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-255">Поддержка OLE-объектов</span><span class="sxs-lookup"><span data-stu-id="dd378-255">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="dd378-256">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="dd378-256">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-257">Поддержка открытых наборов строк</span><span class="sxs-lookup"><span data-stu-id="dd378-257">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="dd378-258">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="dd378-258">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-259">ORDER BY столбцы в списке Select</span><span class="sxs-lookup"><span data-stu-id="dd378-259">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="dd378-260">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="dd378-260">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-261">Выходной параметр доступности</span><span class="sxs-lookup"><span data-stu-id="dd378-261">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="dd378-262">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="dd378-262">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-263">Передайте с указанные методы</span><span class="sxs-lookup"><span data-stu-id="dd378-263">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="dd378-264">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="dd378-264">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-265">Пароль</span><span class="sxs-lookup"><span data-stu-id="dd378-265">Password</span></span></p></td>
<td><p><span data-ttu-id="dd378-266">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="dd378-266">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-267">Сохранять сведения о безопасности</span><span class="sxs-lookup"><span data-stu-id="dd378-267">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="dd378-268">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span><span class="sxs-lookup"><span data-stu-id="dd378-268">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-269">Тип сохраняемого идентификатора</span><span class="sxs-lookup"><span data-stu-id="dd378-269">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="dd378-270">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="dd378-270">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-271">Подготовка поведение аварийное завершение</span><span class="sxs-lookup"><span data-stu-id="dd378-271">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="dd378-272">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="dd378-272">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-273">Подготовка поведение выделения</span><span class="sxs-lookup"><span data-stu-id="dd378-273">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="dd378-274">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="dd378-274">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-275">Процедура терминов</span><span class="sxs-lookup"><span data-stu-id="dd378-275">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="dd378-276">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="dd378-276">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-277">Запрос</span><span class="sxs-lookup"><span data-stu-id="dd378-277">Prompt</span></span></p></td>
<td><p><span data-ttu-id="dd378-278">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="dd378-278">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-279">Понятное имя поставщика</span><span class="sxs-lookup"><span data-stu-id="dd378-279">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="dd378-280">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="dd378-280">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-281">Имя поставщика</span><span class="sxs-lookup"><span data-stu-id="dd378-281">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="dd378-282">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="dd378-282">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-283">Версия поставщика</span><span class="sxs-lookup"><span data-stu-id="dd378-283">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="dd378-284">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="dd378-284">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-285">Источник данных только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd378-285">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="dd378-286">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="dd378-286">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-287">Преобразование строк на команду</span><span class="sxs-lookup"><span data-stu-id="dd378-287">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="dd378-288">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="dd378-288">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-289">Схема терминов</span><span class="sxs-lookup"><span data-stu-id="dd378-289">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="dd378-290">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="dd378-290">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-291">Об использовании схемы</span><span class="sxs-lookup"><span data-stu-id="dd378-291">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="dd378-292">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="dd378-292">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-293">Поддержка SQL</span><span class="sxs-lookup"><span data-stu-id="dd378-293">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="dd378-294">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="dd378-294">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-295">Структурированное хранилище</span><span class="sxs-lookup"><span data-stu-id="dd378-295">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="dd378-296">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="dd378-296">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-297">Поддержка вложенного запроса</span><span class="sxs-lookup"><span data-stu-id="dd378-297">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="dd378-298">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="dd378-298">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-299">В таблице терминов</span><span class="sxs-lookup"><span data-stu-id="dd378-299">Table Term</span></span></p></td>
<td><p><span data-ttu-id="dd378-300">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="dd378-300">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-301">Транзакций DDL</span><span class="sxs-lookup"><span data-stu-id="dd378-301">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="dd378-302">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="dd378-302">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-303">Идентификатор пользователя</span><span class="sxs-lookup"><span data-stu-id="dd378-303">User ID</span></span></p></td>
<td><p><span data-ttu-id="dd378-304">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="dd378-304">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-305">Имя пользователя</span><span class="sxs-lookup"><span data-stu-id="dd378-305">User Name</span></span></p></td>
<td><p><span data-ttu-id="dd378-306">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="dd378-306">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-307">Дескриптор окна</span><span class="sxs-lookup"><span data-stu-id="dd378-307">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="dd378-308">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="dd378-308">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a><span data-ttu-id="dd378-309">Свойства динамической набора записей</span><span class="sxs-lookup"><span data-stu-id="dd378-309">Recordset Dynamic Properties</span></span>

<span data-ttu-id="dd378-310">Следующие свойства добавляются в коллекцию **свойств** объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="dd378-310">The following properties are added to the **Recordset** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dd378-311">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="dd378-311">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="dd378-312">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="dd378-312">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dd378-313">Порядок доступа</span><span class="sxs-lookup"><span data-stu-id="dd378-313">Access Order</span></span></p></td>
<td><p><span data-ttu-id="dd378-314">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="dd378-314">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-315">Блокировка объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="dd378-315">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="dd378-316">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="dd378-316">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-317">Тип закладки</span><span class="sxs-lookup"><span data-stu-id="dd378-317">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="dd378-318">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="dd378-318">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-319">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="dd378-319">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="dd378-320">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="dd378-320">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-321">Изменение вставленных строк</span><span class="sxs-lookup"><span data-stu-id="dd378-321">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="dd378-322">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="dd378-322">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-323">Права доступа столбца</span><span class="sxs-lookup"><span data-stu-id="dd378-323">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="dd378-324">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="dd378-324">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-325">Столбец набор уведомлений</span><span class="sxs-lookup"><span data-stu-id="dd378-325">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="dd378-326">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="dd378-326">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-327">Время ожидания команды</span><span class="sxs-lookup"><span data-stu-id="dd378-327">Command Time Out</span></span></p></td>
<td><p><span data-ttu-id="dd378-328">DBPROP_COMMANDTIMEOUT</span><span class="sxs-lookup"><span data-stu-id="dd378-328">DBPROP_COMMANDTIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-329">Отложите столбца</span><span class="sxs-lookup"><span data-stu-id="dd378-329">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="dd378-330">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="dd378-330">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-331">Отложенное обновление объекта хранения</span><span class="sxs-lookup"><span data-stu-id="dd378-331">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="dd378-332">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="dd378-332">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-333">Выборку</span><span class="sxs-lookup"><span data-stu-id="dd378-333">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="dd378-334">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="dd378-334">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-335">Хранение строк</span><span class="sxs-lookup"><span data-stu-id="dd378-335">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="dd378-336">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="dd378-336">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-337">IAccessor</span><span class="sxs-lookup"><span data-stu-id="dd378-337">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="dd378-338">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="dd378-338">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-339">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="dd378-339">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="dd378-340">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="dd378-340">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-341">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="dd378-341">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="dd378-342">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="dd378-342">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-343">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="dd378-343">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="dd378-344">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="dd378-344">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-345">IConvertType</span><span class="sxs-lookup"><span data-stu-id="dd378-345">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="dd378-346">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="dd378-346">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-347">Немобильные строки</span><span class="sxs-lookup"><span data-stu-id="dd378-347">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="dd378-348">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="dd378-348">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-349">IRowset</span><span class="sxs-lookup"><span data-stu-id="dd378-349">IRowset</span></span></p></td>
<td><p><span data-ttu-id="dd378-350">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="dd378-350">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-351">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="dd378-351">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="dd378-352">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="dd378-352">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-353">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="dd378-353">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="dd378-354">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="dd378-354">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-355">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="dd378-355">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="dd378-356">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="dd378-356">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-357">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="dd378-357">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="dd378-358">DBPROP_IRowsestLocate</span><span class="sxs-lookup"><span data-stu-id="dd378-358">DBPROP_IRowsestLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-359">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="dd378-359">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-360">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="dd378-360">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="dd378-361">DBPROP_IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="dd378-361">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-362">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="dd378-362">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="dd378-363">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="dd378-363">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-364">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="dd378-364">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="dd378-365">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="dd378-365">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-366">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="dd378-366">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="dd378-367">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="dd378-367">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-368">Литерал закладки</span><span class="sxs-lookup"><span data-stu-id="dd378-368">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="dd378-369">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="dd378-369">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-370">Удостоверение литерала строки</span><span class="sxs-lookup"><span data-stu-id="dd378-370">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="dd378-371">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="dd378-371">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-372">Максимальное число открытых строк</span><span class="sxs-lookup"><span data-stu-id="dd378-372">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="dd378-373">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="dd378-373">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-374">Максимум ожидающие строк</span><span class="sxs-lookup"><span data-stu-id="dd378-374">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="dd378-375">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="dd378-375">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-376">Максимальное число строк</span><span class="sxs-lookup"><span data-stu-id="dd378-376">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="dd378-377">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="dd378-377">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-378">Степень детализации уведомлений</span><span class="sxs-lookup"><span data-stu-id="dd378-378">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="dd378-379">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="dd378-379">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-380">Этапы уведомлений</span><span class="sxs-lookup"><span data-stu-id="dd378-380">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="dd378-381">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="dd378-381">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-382">Объекты в транзакции</span><span class="sxs-lookup"><span data-stu-id="dd378-382">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="dd378-383">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="dd378-383">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-384">Видны прочие изменения</span><span class="sxs-lookup"><span data-stu-id="dd378-384">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="dd378-385">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="dd378-385">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-386">Других пользователей вставки видимым</span><span class="sxs-lookup"><span data-stu-id="dd378-386">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="dd378-387">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="dd378-387">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-388">Видны собственные изменения</span><span class="sxs-lookup"><span data-stu-id="dd378-388">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="dd378-389">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="dd378-389">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-390">Видны собственные операции вставки</span><span class="sxs-lookup"><span data-stu-id="dd378-390">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="dd378-391">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="dd378-391">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-392">Сохранять при аварийном завершении</span><span class="sxs-lookup"><span data-stu-id="dd378-392">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="dd378-393">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="dd378-393">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-394">Сохранять при фиксации</span><span class="sxs-lookup"><span data-stu-id="dd378-394">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="dd378-395">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="dd378-395">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-396">Быстрый перезапуск</span><span class="sxs-lookup"><span data-stu-id="dd378-396">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="dd378-397">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="dd378-397">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-398">Повторные события</span><span class="sxs-lookup"><span data-stu-id="dd378-398">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="dd378-399">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="dd378-399">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-400">Удаление удаленных строк</span><span class="sxs-lookup"><span data-stu-id="dd378-400">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="dd378-401">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="dd378-401">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-402">Сообщить о нескольких изменений</span><span class="sxs-lookup"><span data-stu-id="dd378-402">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="dd378-403">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="dd378-403">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-404">Вернуть ожидающие вставки</span><span class="sxs-lookup"><span data-stu-id="dd378-404">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="dd378-405">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="dd378-405">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-406">Удалить строку уведомлений</span><span class="sxs-lookup"><span data-stu-id="dd378-406">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="dd378-407">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="dd378-407">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-408">Строка первого уведомления об изменении</span><span class="sxs-lookup"><span data-stu-id="dd378-408">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="dd378-409">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="dd378-409">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-410">Строка вставки уведомлений</span><span class="sxs-lookup"><span data-stu-id="dd378-410">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="dd378-411">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="dd378-411">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-412">Привилегии строки</span><span class="sxs-lookup"><span data-stu-id="dd378-412">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="dd378-413">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="dd378-413">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-414">Уведомления о повторной синхронизации строки</span><span class="sxs-lookup"><span data-stu-id="dd378-414">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="dd378-415">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="dd378-415">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-416">Строка, потоковой модели</span><span class="sxs-lookup"><span data-stu-id="dd378-416">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="dd378-417">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="dd378-417">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-418">Уведомление об изменении отмены строки</span><span class="sxs-lookup"><span data-stu-id="dd378-418">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="dd378-419">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="dd378-419">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-420">Строка отмены Delete уведомлений</span><span class="sxs-lookup"><span data-stu-id="dd378-420">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="dd378-421">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="dd378-421">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-422">Вставка отмены строки уведомлений</span><span class="sxs-lookup"><span data-stu-id="dd378-422">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="dd378-423">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="dd378-423">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-424">Уведомление об обновлении строки</span><span class="sxs-lookup"><span data-stu-id="dd378-424">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="dd378-425">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="dd378-425">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-426">Уведомление об изменении положения строк выборки</span><span class="sxs-lookup"><span data-stu-id="dd378-426">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="dd378-427">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="dd378-427">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-428">Уведомление о выпуске набора строк</span><span class="sxs-lookup"><span data-stu-id="dd378-428">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="dd378-429">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="dd378-429">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-430">Прокрутка назад</span><span class="sxs-lookup"><span data-stu-id="dd378-430">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="dd378-431">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="dd378-431">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-432">Серверный курсор</span><span class="sxs-lookup"><span data-stu-id="dd378-432">Server Cursor</span></span></p></td>
<td><p><span data-ttu-id="dd378-433">DBPROP_SERVERCURSOR</span><span class="sxs-lookup"><span data-stu-id="dd378-433">DBPROP_SERVERCURSOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-434">Пропустить удаленных закладки</span><span class="sxs-lookup"><span data-stu-id="dd378-434">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="dd378-435">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="dd378-435">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-436">Строка строгого удостоверений</span><span class="sxs-lookup"><span data-stu-id="dd378-436">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="dd378-437">DBPROP_STRONGITDENTITY</span><span class="sxs-lookup"><span data-stu-id="dd378-437">DBPROP_STRONGITDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-438">Уникальные строки</span><span class="sxs-lookup"><span data-stu-id="dd378-438">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="dd378-439">DBPROP_UNIQUEROWS</span><span class="sxs-lookup"><span data-stu-id="dd378-439">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-440">Возможности обновления</span><span class="sxs-lookup"><span data-stu-id="dd378-440">Updatability</span></span></p></td>
<td><p><span data-ttu-id="dd378-441">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="dd378-441">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-442">Использование закладок</span><span class="sxs-lookup"><span data-stu-id="dd378-442">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="dd378-443">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="dd378-443">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a><span data-ttu-id="dd378-444">Динамические свойства команды</span><span class="sxs-lookup"><span data-stu-id="dd378-444">Command Dynamic Properties</span></span>

<span data-ttu-id="dd378-445">Следующие свойства добавляются в коллекцию **свойств** объекта **команды** .</span><span class="sxs-lookup"><span data-stu-id="dd378-445">The following properties are added to the **Command** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dd378-446">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="dd378-446">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="dd378-447">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="dd378-447">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dd378-448">Порядок доступа</span><span class="sxs-lookup"><span data-stu-id="dd378-448">Access Order</span></span></p></td>
<td><p><span data-ttu-id="dd378-449">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="dd378-449">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-450">Базовый путь</span><span class="sxs-lookup"><span data-stu-id="dd378-450">Base Path</span></span></p></td>
<td><p><span data-ttu-id="dd378-451">SSPROP_STREAM_BASEPATH</span><span class="sxs-lookup"><span data-stu-id="dd378-451">SSPROP_STREAM_BASEPATH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-452">Блокировка объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="dd378-452">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="dd378-453">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="dd378-453">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-454">Тип закладки</span><span class="sxs-lookup"><span data-stu-id="dd378-454">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="dd378-455">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="dd378-455">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-456">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="dd378-456">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="dd378-457">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="dd378-457">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-458">Изменение вставленных строк</span><span class="sxs-lookup"><span data-stu-id="dd378-458">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="dd378-459">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="dd378-459">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-460">Права доступа столбца</span><span class="sxs-lookup"><span data-stu-id="dd378-460">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="dd378-461">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="dd378-461">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-462">Столбец набор уведомлений</span><span class="sxs-lookup"><span data-stu-id="dd378-462">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="dd378-463">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="dd378-463">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-464">Тип контента</span><span class="sxs-lookup"><span data-stu-id="dd378-464">Content Type</span></span></p></td>
<td><p><span data-ttu-id="dd378-465">SSPROP_STREAM_CONTENTTYPE</span><span class="sxs-lookup"><span data-stu-id="dd378-465">SSPROP_STREAM_CONTENTTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-466">Автоматическая выборка курсора</span><span class="sxs-lookup"><span data-stu-id="dd378-466">Cursor Auto Fetch</span></span></p></td>
<td><p><span data-ttu-id="dd378-467">SSPROP_CURSORAUTOFETCH</span><span class="sxs-lookup"><span data-stu-id="dd378-467">SSPROP_CURSORAUTOFETCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-468">Отложите столбца</span><span class="sxs-lookup"><span data-stu-id="dd378-468">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="dd378-469">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="dd378-469">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-470">Отложите Подготовка</span><span class="sxs-lookup"><span data-stu-id="dd378-470">Defer Prepare</span></span></p></td>
<td><p><span data-ttu-id="dd378-471">SSPROP_DEFERPREPARE</span><span class="sxs-lookup"><span data-stu-id="dd378-471">SSPROP_DEFERPREPARE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-472">Отложенное обновление объекта хранения</span><span class="sxs-lookup"><span data-stu-id="dd378-472">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="dd378-473">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="dd378-473">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-474">Выборку</span><span class="sxs-lookup"><span data-stu-id="dd378-474">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="dd378-475">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="dd378-475">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-476">Хранение строк</span><span class="sxs-lookup"><span data-stu-id="dd378-476">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="dd378-477">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="dd378-477">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-478">IAccessor</span><span class="sxs-lookup"><span data-stu-id="dd378-478">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="dd378-479">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="dd378-479">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-480">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="dd378-480">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="dd378-481">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="dd378-481">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-482">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="dd378-482">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="dd378-483">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="dd378-483">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-484">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="dd378-484">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="dd378-485">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="dd378-485">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-486">IConvertType</span><span class="sxs-lookup"><span data-stu-id="dd378-486">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="dd378-487">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="dd378-487">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-488">Немобильные строки</span><span class="sxs-lookup"><span data-stu-id="dd378-488">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="dd378-489">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="dd378-489">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-490">IRowset</span><span class="sxs-lookup"><span data-stu-id="dd378-490">IRowset</span></span></p></td>
<td><p><span data-ttu-id="dd378-491">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="dd378-491">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-492">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="dd378-492">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="dd378-493">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="dd378-493">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-494">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="dd378-494">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="dd378-495">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="dd378-495">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-496">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="dd378-496">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="dd378-497">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="dd378-497">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-498">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="dd378-498">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="dd378-499">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="dd378-499">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-500">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="dd378-500">IRowsetResynch</span></span></p></td>
<td><p><span data-ttu-id="dd378-501">DBPROP_IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="dd378-501">DBPROP_IRowsetResynch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-502">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="dd378-502">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="dd378-503">DBPROP_IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="dd378-503">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-504">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="dd378-504">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="dd378-505">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="dd378-505">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-506">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="dd378-506">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="dd378-507">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="dd378-507">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-508">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="dd378-508">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="dd378-509">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="dd378-509">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-510">Литерал закладки</span><span class="sxs-lookup"><span data-stu-id="dd378-510">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="dd378-511">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="dd378-511">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-512">Удостоверение литерала строки</span><span class="sxs-lookup"><span data-stu-id="dd378-512">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="dd378-513">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="dd378-513">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-514">Режим блокировки</span><span class="sxs-lookup"><span data-stu-id="dd378-514">Lock Mode</span></span></p></td>
<td><p><span data-ttu-id="dd378-515">DBPROP_LOCKMODE</span><span class="sxs-lookup"><span data-stu-id="dd378-515">DBPROP_LOCKMODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-516">Максимальное число открытых строк</span><span class="sxs-lookup"><span data-stu-id="dd378-516">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="dd378-517">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="dd378-517">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-518">Максимум ожидающие строк</span><span class="sxs-lookup"><span data-stu-id="dd378-518">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="dd378-519">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="dd378-519">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-520">Максимальное число строк</span><span class="sxs-lookup"><span data-stu-id="dd378-520">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="dd378-521">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="dd378-521">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-522">Степень детализации уведомлений</span><span class="sxs-lookup"><span data-stu-id="dd378-522">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="dd378-523">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="dd378-523">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-524">Этапы уведомлений</span><span class="sxs-lookup"><span data-stu-id="dd378-524">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="dd378-525">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="dd378-525">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-526">Объекты в транзакции</span><span class="sxs-lookup"><span data-stu-id="dd378-526">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="dd378-527">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="dd378-527">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-528">Видны прочие изменения</span><span class="sxs-lookup"><span data-stu-id="dd378-528">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="dd378-529">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="dd378-529">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-530">Других пользователей вставки видимым</span><span class="sxs-lookup"><span data-stu-id="dd378-530">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="dd378-531">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="dd378-531">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-532">Свойство кодировки выходных данных</span><span class="sxs-lookup"><span data-stu-id="dd378-532">Output Encoding Property</span></span></p></td>
<td><p><span data-ttu-id="dd378-533">DBPROP_OUTPUTENCODING</span><span class="sxs-lookup"><span data-stu-id="dd378-533">DBPROP_OUTPUTENCODING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-534">Свойство потока выходных данных</span><span class="sxs-lookup"><span data-stu-id="dd378-534">Output Stream Property</span></span></p></td>
<td><p><span data-ttu-id="dd378-535">DBPROP_OUTPUTSTREAM</span><span class="sxs-lookup"><span data-stu-id="dd378-535">DBPROP_OUTPUTSTREAM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-536">Видны собственные изменения</span><span class="sxs-lookup"><span data-stu-id="dd378-536">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="dd378-537">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="dd378-537">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-538">Видны собственные операции вставки</span><span class="sxs-lookup"><span data-stu-id="dd378-538">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="dd378-539">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="dd378-539">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-540">Сохранять при аварийном завершении</span><span class="sxs-lookup"><span data-stu-id="dd378-540">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="dd378-541">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="dd378-541">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-542">Сохранять при фиксации</span><span class="sxs-lookup"><span data-stu-id="dd378-542">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="dd378-543">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="dd378-543">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-544">Быстрый перезапуск</span><span class="sxs-lookup"><span data-stu-id="dd378-544">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="dd378-545">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="dd378-545">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-546">Повторные события</span><span class="sxs-lookup"><span data-stu-id="dd378-546">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="dd378-547">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="dd378-547">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-548">Удаление удаленных строк</span><span class="sxs-lookup"><span data-stu-id="dd378-548">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="dd378-549">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="dd378-549">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-550">Сообщить о нескольких изменений</span><span class="sxs-lookup"><span data-stu-id="dd378-550">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="dd378-551">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="dd378-551">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-552">Вернуть ожидающие вставки</span><span class="sxs-lookup"><span data-stu-id="dd378-552">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="dd378-553">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="dd378-553">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-554">Удалить строку уведомлений</span><span class="sxs-lookup"><span data-stu-id="dd378-554">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="dd378-555">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="dd378-555">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-556">Строка первого уведомления об изменении</span><span class="sxs-lookup"><span data-stu-id="dd378-556">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="dd378-557">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="dd378-557">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-558">Строка вставки уведомлений</span><span class="sxs-lookup"><span data-stu-id="dd378-558">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="dd378-559">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="dd378-559">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-560">Привилегии строки</span><span class="sxs-lookup"><span data-stu-id="dd378-560">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="dd378-561">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="dd378-561">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-562">Уведомления о повторной синхронизации строки</span><span class="sxs-lookup"><span data-stu-id="dd378-562">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="dd378-563">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="dd378-563">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-564">Строка, потоковой модели</span><span class="sxs-lookup"><span data-stu-id="dd378-564">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="dd378-565">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="dd378-565">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-566">Уведомление об изменении отмены строки</span><span class="sxs-lookup"><span data-stu-id="dd378-566">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="dd378-567">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="dd378-567">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-568">Строка отмены Delete уведомлений</span><span class="sxs-lookup"><span data-stu-id="dd378-568">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="dd378-569">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="dd378-569">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-570">Вставка отмены строки уведомлений</span><span class="sxs-lookup"><span data-stu-id="dd378-570">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="dd378-571">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="dd378-571">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-572">Уведомление об обновлении строки</span><span class="sxs-lookup"><span data-stu-id="dd378-572">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="dd378-573">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="dd378-573">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-574">Уведомление об изменении положения строк выборки</span><span class="sxs-lookup"><span data-stu-id="dd378-574">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="dd378-575">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="dd378-575">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-576">Уведомление о выпуске набора строк</span><span class="sxs-lookup"><span data-stu-id="dd378-576">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="dd378-577">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="dd378-577">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-578">Прокрутка назад</span><span class="sxs-lookup"><span data-stu-id="dd378-578">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="dd378-579">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="dd378-579">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-580">Серверный курсор</span><span class="sxs-lookup"><span data-stu-id="dd378-580">Server Cursor</span></span></p></td>
<td><p><span data-ttu-id="dd378-581">DBPROP_SERVERCURSOR</span><span class="sxs-lookup"><span data-stu-id="dd378-581">DBPROP_SERVERCURSOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-582">Вставка данных сервера</span><span class="sxs-lookup"><span data-stu-id="dd378-582">Server Data on Insert</span></span></p></td>
<td><p><span data-ttu-id="dd378-583">DBPROP_SERVERDATAONINSERT</span><span class="sxs-lookup"><span data-stu-id="dd378-583">DBPROP_SERVERDATAONINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-584">Пропустить удаленных закладки</span><span class="sxs-lookup"><span data-stu-id="dd378-584">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="dd378-585">DBPROP_BOOKMARKSKIP</span><span class="sxs-lookup"><span data-stu-id="dd378-585">DBPROP_BOOKMARKSKIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-586">Строка строгого удостоверений</span><span class="sxs-lookup"><span data-stu-id="dd378-586">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="dd378-587">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="dd378-587">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-588">Возможности обновления</span><span class="sxs-lookup"><span data-stu-id="dd378-588">Updatability</span></span></p></td>
<td><p><span data-ttu-id="dd378-589">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="dd378-589">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-590">Использование закладок</span><span class="sxs-lookup"><span data-stu-id="dd378-590">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="dd378-591">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="dd378-591">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd378-592">Корневой XML</span><span class="sxs-lookup"><span data-stu-id="dd378-592">XML Root</span></span></p></td>
<td><p><span data-ttu-id="dd378-593">SSPROP_STREAM_XMLROOT</span><span class="sxs-lookup"><span data-stu-id="dd378-593">SSPROP_STREAM_XMLROOT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd378-594">XSL</span><span class="sxs-lookup"><span data-stu-id="dd378-594">XSL</span></span></p></td>
<td><p><span data-ttu-id="dd378-595">SSPROP_STREAM_XSL</span><span class="sxs-lookup"><span data-stu-id="dd378-595">SSPROP_STREAM_XSL</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="dd378-596">Сведения о реализации и функциональным сведений о Microsoft SQL Server поставщик OLE DB можно найти поставщика OLE DB для документации по SQL Server в разделе OLE DB MDAC SDK.</span><span class="sxs-lookup"><span data-stu-id="dd378-596">For specific implementation details and functional information about the Microsoft SQL Server OLE DB Provider, consult the OLE DB Provider for SQL Server documentation in the OLE DB section of the MDAC SDK.</span></span>

