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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705108"
---
# <a name="microsoft-ole-db-provider-for-sql-server"></a><span data-ttu-id="c6e9c-102">Поставщик Microsoft OLE DB для SQL Server</span><span class="sxs-lookup"><span data-stu-id="c6e9c-102">Microsoft OLE DB Provider for SQL Server</span></span>


<span data-ttu-id="c6e9c-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c6e9c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c6e9c-104">Поставщик Microsoft OLE DB для SQL Server, SQLOLEDB, позволяет ADO для доступа к Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c6e9c-104">The Microsoft OLE DB Provider for SQL Server, SQLOLEDB, allows ADO to access Microsoft SQL Server.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="c6e9c-105">Параметры строки подключения</span><span class="sxs-lookup"><span data-stu-id="c6e9c-105">Connection String Parameters</span></span>

<span data-ttu-id="c6e9c-106">Для подключения к данным поставщиком аргументе *поставщика* свойство [ConnectionString](connectionstring-property-ado.md) для:</span><span class="sxs-lookup"><span data-stu-id="c6e9c-106">To connect to this provider, set the *Provider* argument to the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```sql 
 
SQLOLEDB 
```

<span data-ttu-id="c6e9c-107">Это значение может быть задана или ознакомьтесь с помощью свойства [поставщика](provider-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="c6e9c-107">This value can also be set or read using the [Provider](provider-property-ado.md) property.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="c6e9c-108">Типичная строка подключения</span><span class="sxs-lookup"><span data-stu-id="c6e9c-108">Typical Connection String</span></span>

<span data-ttu-id="c6e9c-109">— Это строка соединения для данного поставщика:</span><span class="sxs-lookup"><span data-stu-id="c6e9c-109">A typical connection string for this provider is:</span></span>

```sql 
 
"Provider=SQLOLEDB;Data Source=serverName;" 
Initial Catalog=databaseName; 
User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="c6e9c-110">Строка состоит из следующих ключевых слов:</span><span class="sxs-lookup"><span data-stu-id="c6e9c-110">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c6e9c-111">Keyword</span><span class="sxs-lookup"><span data-stu-id="c6e9c-111">Keyword</span></span></p></th>
<th><p><span data-ttu-id="c6e9c-112">Описание</span><span class="sxs-lookup"><span data-stu-id="c6e9c-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-113"><strong>Поставщик</strong></span><span class="sxs-lookup"><span data-stu-id="c6e9c-113"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="c6e9c-114">Задает поставщика OLE DB для SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c6e9c-114">Specifies the OLE DB Provider for SQL Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-115"><strong>Источник данных</strong> или <strong>сервера</strong></span><span class="sxs-lookup"><span data-stu-id="c6e9c-115"><strong>Data Source</strong> or <strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c6e9c-116">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="c6e9c-116">Specifies the name of a server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-117"><strong>Исходный каталог</strong> или <strong>База данных</strong></span><span class="sxs-lookup"><span data-stu-id="c6e9c-117"><strong>Initial Catalog</strong> or <strong>Database</strong></span></span></p></td>
<td><p><span data-ttu-id="c6e9c-118">Указывает имя базы данных на сервере.</span><span class="sxs-lookup"><span data-stu-id="c6e9c-118">Specifies the name of a database on the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-119"><strong>Идентификатор пользователя</strong> или <strong>ИД пользователя</strong></span><span class="sxs-lookup"><span data-stu-id="c6e9c-119"><strong>User ID</strong> or <strong>uid</strong></span></span></p></td>
<td><p><span data-ttu-id="c6e9c-120">Задает имя пользователя (для проверки подлинности SQL Server).</span><span class="sxs-lookup"><span data-stu-id="c6e9c-120">Specifies the user name (for SQL Server Authentication).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-121"><strong>Пароль</strong> или <strong>pwd</strong></span><span class="sxs-lookup"><span data-stu-id="c6e9c-121"><strong>Password</strong> or <strong>pwd</strong></span></span></p></td>
<td><p><span data-ttu-id="c6e9c-122">Задает пароль пользователя (для проверки подлинности SQL Server).</span><span class="sxs-lookup"><span data-stu-id="c6e9c-122">Specifies the user password (for SQL Server Authentication).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-connection-parameters"></a><span data-ttu-id="c6e9c-123">Параметры подключения от поставщика</span><span class="sxs-lookup"><span data-stu-id="c6e9c-123">Provider-Specific Connection Parameters</span></span>

<span data-ttu-id="c6e9c-124">Поставщик поддерживает несколько параметров подключения для конкретного поставщика дополнение к тем определяется ADO.</span><span class="sxs-lookup"><span data-stu-id="c6e9c-124">The provider supports several provider-specific connection parameters in addition to those defined by ADO.</span></span> <span data-ttu-id="c6e9c-125">Как и в случае с помощью свойства подключения ADO, эти свойства от поставщика можно задать с помощью коллекции [свойств](properties-collection-ado.md) [подключения](connection-object-ado.md) или можно задать как часть **ConnectionString**.</span><span class="sxs-lookup"><span data-stu-id="c6e9c-125">As with the ADO connection properties, these provider-specific properties can be set via the [Properties](properties-collection-ado.md) collection of a [Connection](connection-object-ado.md) or can be set as part of the **ConnectionString**.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c6e9c-126">Параметр</span><span class="sxs-lookup"><span data-stu-id="c6e9c-126">Parameter</span></span></p></th>
<th><p><span data-ttu-id="c6e9c-127">Описание</span><span class="sxs-lookup"><span data-stu-id="c6e9c-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-128">Trusted_Connection</span><span class="sxs-lookup"><span data-stu-id="c6e9c-128">Trusted_Connection</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-129">Указывает режим проверки подлинности пользователя.</span><span class="sxs-lookup"><span data-stu-id="c6e9c-129">Indicates the user authentication mode.</span></span> <span data-ttu-id="c6e9c-130">Это может быть значение <strong>Да</strong> или <strong>Нет</strong>.</span><span class="sxs-lookup"><span data-stu-id="c6e9c-130">This can be set to <strong>Yes</strong> or <strong>No</strong>.</span></span> <span data-ttu-id="c6e9c-131">Значение по умолчанию — <strong>Нет</strong>.</span><span class="sxs-lookup"><span data-stu-id="c6e9c-131">The default value is <strong>No</strong>.</span></span> <span data-ttu-id="c6e9c-132">Если это свойство имеет значение <strong>Да</strong>, SQLOLEDB использует режим проверки подлинности Microsoft Windows NT для авторизации доступа пользователей к базе данных SQL Server, заданные значения свойств <strong>расположение</strong> и <a href="datasource-property-ado.md">источника данных</a> .</span><span class="sxs-lookup"><span data-stu-id="c6e9c-132">If this property is set to <strong>Yes</strong>, then SQLOLEDB uses Microsoft Windows NT Authentication Mode to authorize user access to the SQL Server database specified by the <strong>Location</strong> and <a href="datasource-property-ado.md">Datasource</a> property values.</span></span> <span data-ttu-id="c6e9c-133">Если задано значение <strong>No</strong>, SQLOLEDB использует смешанный режим для авторизации доступа пользователей к базе данных SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c6e9c-133">If this property is set to <strong>No</strong>, then SQLOLEDB uses Mixed Mode to authorize user access to the SQL Server database.</span></span> <span data-ttu-id="c6e9c-134">Имя пользователя SQL Server и пароль указанных в свойствах <strong>Идентификатор пользователя</strong> и <strong>пароль</strong> .</span><span class="sxs-lookup"><span data-stu-id="c6e9c-134">The SQL Server login and password are specified in the <strong>User Id</strong> and <strong>Password</strong> properties.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-135">Текущий язык</span><span class="sxs-lookup"><span data-stu-id="c6e9c-135">Current Language</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-136">Указывает имя языка SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c6e9c-136">Indicates a SQL Server language name.</span></span> <span data-ttu-id="c6e9c-137">Определяет язык, используемый для выбора сообщения системы и форматирование.</span><span class="sxs-lookup"><span data-stu-id="c6e9c-137">Identifies the language used for system message selection and formatting.</span></span> <span data-ttu-id="c6e9c-138">Язык должны быть установлены на SQL Server, в противном случае — открытие подключение завершится с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="c6e9c-138">The language must be installed on the SQL Server, otherwise opening the connection will fail.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-139">Адрес сети</span><span class="sxs-lookup"><span data-stu-id="c6e9c-139">Network Address</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-140">Указывает адрес сети SQL Server, заданного в свойстве <strong>расположение</strong> .</span><span class="sxs-lookup"><span data-stu-id="c6e9c-140">Indicates the network address of the SQL Server specified by the <strong>Location</strong> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-141">Сетевой библиотеки</span><span class="sxs-lookup"><span data-stu-id="c6e9c-141">Network Library</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-142">Указывает имя библиотеки сети (библиотеки динамической компоновки), используемое для взаимодействия с SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c6e9c-142">Indicates the name of the network library (dynamic-link libraries) used to communicate with the SQL Server.</span></span> <span data-ttu-id="c6e9c-143">Имя не должно содержать путь или расширение имени файла библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="c6e9c-143">The name should not include the path or the .dll file name extension.</span></span> <span data-ttu-id="c6e9c-144">Значение по умолчанию, предоставленные конфигурация клиента SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c6e9c-144">The default is provided by the SQL Server client configuration.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-145">Используйте процедуру для подготовки</span><span class="sxs-lookup"><span data-stu-id="c6e9c-145">Use Procedure for Prepare</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-146">Определяет, будет ли SQL Server создает временные хранимые процедуры, когда команды подготавливаются (свойством <strong>подготовленных</strong> ).</span><span class="sxs-lookup"><span data-stu-id="c6e9c-146">Determines whether SQL Server creates temporary stored procedures when Commands are prepared (by the <strong>Prepared</strong> property).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-147">Переводить Auto</span><span class="sxs-lookup"><span data-stu-id="c6e9c-147">Auto Translate</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-148">Указывает необходимость преобразования символов OEM или ANSI.</span><span class="sxs-lookup"><span data-stu-id="c6e9c-148">Indicates whether OEM/ANSI characters are converted.</span></span> <span data-ttu-id="c6e9c-149">Это свойство может иметь значение <strong>True</strong> или <strong>False</strong>.</span><span class="sxs-lookup"><span data-stu-id="c6e9c-149">This property can be set to <strong>True</strong> or <strong>False</strong>.</span></span> <span data-ttu-id="c6e9c-150">Значение по умолчанию — <strong>True</strong>.</span><span class="sxs-lookup"><span data-stu-id="c6e9c-150">The default value is <strong>True</strong>.</span></span> <span data-ttu-id="c6e9c-151">Если этому свойству присвоено <strong>значение True</strong>, SQLOLEDB выполняет преобразование символов OEM или ANSI при строк символов нескольких байтов извлекается из или отправленные к серверу SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c6e9c-151">If this property is set to <strong>True</strong>, then SQLOLEDB performs OEM/ANSI character conversion when multi-byte character strings are retrieved from, or sent to, the SQL Server.</span></span> <span data-ttu-id="c6e9c-152">Если этому свойству присвоено <strong>значение False</strong>, затем SQLOLEDB не выполняет преобразование символов OEM или ANSI на символ нескольких байтов строковых данных.</span><span class="sxs-lookup"><span data-stu-id="c6e9c-152">If this property is set to <strong>False</strong>, then SQLOLEDB does not perform OEM/ANSI character conversion on multi-byte character string data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-153">Размер пакета</span><span class="sxs-lookup"><span data-stu-id="c6e9c-153">Packet Size</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-154">Указывает размер сетевого пакета в байтах.</span><span class="sxs-lookup"><span data-stu-id="c6e9c-154">Indicates a network packet size in bytes.</span></span> <span data-ttu-id="c6e9c-155">Значение свойства размера пакета должно быть от 512 до 32 767.</span><span class="sxs-lookup"><span data-stu-id="c6e9c-155">The packet size property value must be between 512 and 32767.</span></span> <span data-ttu-id="c6e9c-156">Размер пакета сети SQLOLEDB по умолчанию — 4096.</span><span class="sxs-lookup"><span data-stu-id="c6e9c-156">The default SQLOLEDB network packet size is 4096.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-157">Имя приложения</span><span class="sxs-lookup"><span data-stu-id="c6e9c-157">Application Name</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-158">Указывает имя клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="c6e9c-158">Indicates the client application name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-159">Идентификатор рабочей станции</span><span class="sxs-lookup"><span data-stu-id="c6e9c-159">Workstation ID</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-160">Строка, идентифицирующая рабочей станции.</span><span class="sxs-lookup"><span data-stu-id="c6e9c-160">A string identifying the workstation.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-object-usage"></a><span data-ttu-id="c6e9c-161">Использование объекта команды</span><span class="sxs-lookup"><span data-stu-id="c6e9c-161">Command Object Usage</span></span>

<span data-ttu-id="c6e9c-162">SQLOLEDB принимает сочетание ODBC, ANSI и Transact-SQL, относящиеся к SQL Server в качестве допустимого синтаксиса.</span><span class="sxs-lookup"><span data-stu-id="c6e9c-162">SQLOLEDB accepts an amalgam of ODBC, ANSI, and SQL Server-specific Transact-SQL as valid syntax.</span></span> <span data-ttu-id="c6e9c-163">К примеру следующей инструкции SQL использует escape-последовательности ODBC SQL для указания функция LCASE string:</span><span class="sxs-lookup"><span data-stu-id="c6e9c-163">For example, the following SQL statement uses an ODBC SQL escape sequence to specify the LCASE string function:</span></span>

```sql 
 
SELECT customerid={fn LCASE(CustomerID)} FROM Customers 
```

<span data-ttu-id="c6e9c-164">LCASE возвращает строку символов, преобразование все прописные буквы в нижнем регистре эквиваленты.</span><span class="sxs-lookup"><span data-stu-id="c6e9c-164">LCASE returns a character string, converting all uppercase characters to their lowercase equivalents.</span></span> <span data-ttu-id="c6e9c-165">Функция string ANSI SQL НИЖНЕМ выполняет одной и той же операции, поэтому следующей инструкции SQL — это эквивалентно оператор ODBC, представленному выше ANSI:</span><span class="sxs-lookup"><span data-stu-id="c6e9c-165">The ANSI SQL string function LOWER performs the same operation, so the following SQL statement is an ANSI equivalent to the ODBC statement presented above:</span></span>

```sql
 
SELECT customerid=LOWER(CustomerID) FROM Customers 
```

<span data-ttu-id="c6e9c-166">SQLOLEDB успешно обрабатывает в любом из оператора, когда он указан как текст для команды.</span><span class="sxs-lookup"><span data-stu-id="c6e9c-166">SQLOLEDB successfully processes either form of the statement when specified as text for a command.</span></span>

## <a name="stored-procedures"></a><span data-ttu-id="c6e9c-167">Хранимые процедуры</span><span class="sxs-lookup"><span data-stu-id="c6e9c-167">Stored Procedures</span></span>

<span data-ttu-id="c6e9c-168">При выполнении SQL Server хранимой процедуры с помощью команды SQLOLEDB, используйте escape-последовательность вызовов ODBC процедуры в текст команды.</span><span class="sxs-lookup"><span data-stu-id="c6e9c-168">When executing a SQL Server stored procedure using a SQLOLEDB command, use the ODBC procedure call escape sequence in the command text.</span></span> <span data-ttu-id="c6e9c-169">SQLOLEDB затем использует механизм вызова удаленной процедуры из SQL Server для оптимизации обработки команд.</span><span class="sxs-lookup"><span data-stu-id="c6e9c-169">SQLOLEDB then uses the remote procedure call mechanism of SQL Server to optimize command processing.</span></span> <span data-ttu-id="c6e9c-170">К примеру следующей инструкции ODBC SQL окончена текст предпочитаемый команды формы Transact-SQL:</span><span class="sxs-lookup"><span data-stu-id="c6e9c-170">For example, the following ODBC SQL statement is the preferred command text over the Transact-SQL form:</span></span>

## <a name="odbc-sql"></a><span data-ttu-id="c6e9c-171">ODBC SQL</span><span class="sxs-lookup"><span data-stu-id="c6e9c-171">ODBC SQL</span></span>

```sql 
 
{call SalesByCategory('Produce', '1995')} 
```

## <a name="transact-sql"></a><span data-ttu-id="c6e9c-172">Transact-SQL</span><span class="sxs-lookup"><span data-stu-id="c6e9c-172">Transact-SQL</span></span>

```sql 
 
EXECUTE SalesByCategory 'Produce', '1995' 
```

## <a name="recordset-behavior"></a><span data-ttu-id="c6e9c-173">Поведение набора записей</span><span class="sxs-lookup"><span data-stu-id="c6e9c-173">Recordset Behavior</span></span>

<span data-ttu-id="c6e9c-174">SQLOLEDB нельзя использовать курсоры SQL Server для поддержки нескольких результатов, созданных функцией многие команды.</span><span class="sxs-lookup"><span data-stu-id="c6e9c-174">SQLOLEDB cannot use SQL Server cursors to support the multiple-result generated by many commands.</span></span> <span data-ttu-id="c6e9c-175">Потребитель запрашивает записей, требуя поддержки курсора SQL Server, если используется текст команды создает более чем одного набора записей в результате возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="c6e9c-175">If a consumer requests a recordset requiring SQL Server cursor support, an error occurs if the command text used generates more than a single recordset as its result.</span></span>

<span data-ttu-id="c6e9c-176">Прокручиваемой наборов записей SQLOLEDB поддерживаемых курсоров SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c6e9c-176">Scrollable SQLOLEDB recordsets are supported by SQL Server cursors.</span></span> <span data-ttu-id="c6e9c-177">SQL Server, задает ограничения на курсоров, зависит от изменения, внесенные другими пользователями базы данных.</span><span class="sxs-lookup"><span data-stu-id="c6e9c-177">SQL Server imposes limitations on cursors that are sensitive to changes made by other users of the database.</span></span> <span data-ttu-id="c6e9c-178">В частности строки в некоторые курсоры не могут быть упорядочены и попытка создания набора записей с помощью команды, содержащий предложение SQL ORDER BY может не работать.</span><span class="sxs-lookup"><span data-stu-id="c6e9c-178">Specifically, the rows in some cursors cannot be ordered, and attempting to create a recordset using a command containing an SQL ORDER BY clause can fail.</span></span>

## <a name="dynamic-properties"></a><span data-ttu-id="c6e9c-179">Динамические свойства</span><span class="sxs-lookup"><span data-stu-id="c6e9c-179">Dynamic Properties</span></span>

<span data-ttu-id="c6e9c-180">Поставщик Microsoft OLE DB для SQL Server вставляет несколько динамических свойств в коллекцию **свойств** объектов неоткрытый [подключения](connection-object-ado.md), [записей](recordset-object-ado.md)и [команды](command-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="c6e9c-180">The Microsoft OLE DB Provider for SQL Server inserts several dynamic properties into the **Properties** collection of the unopened [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md), and [Command](command-object-ado.md) objects.</span></span>

<span data-ttu-id="c6e9c-181">Следующие таблицы не cross-index имен ADO и OLE DB для каждого динамического свойства.</span><span class="sxs-lookup"><span data-stu-id="c6e9c-181">The following tables are a cross-index of the ADO and OLE DB names for each dynamic property.</span></span> <span data-ttu-id="c6e9c-182">Справочник программиста OLE DB указано имя свойства ADO по слову «Описание».</span><span class="sxs-lookup"><span data-stu-id="c6e9c-182">The OLE DB Programmer's Reference refers to an ADO property name by the term "Description."</span></span> <span data-ttu-id="c6e9c-183">Дополнительные сведения об этих свойств можно найти в Справочник программиста OLE DB.</span><span class="sxs-lookup"><span data-stu-id="c6e9c-183">You can find more information about these properties in the OLE DB Programmer's Reference.</span></span> <span data-ttu-id="c6e9c-184">Поиск имени свойства OLE DB в индексе или просмотреть приложение C: OLE DB свойства.</span><span class="sxs-lookup"><span data-stu-id="c6e9c-184">Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span></span>

## <a name="connection-dynamic-properties"></a><span data-ttu-id="c6e9c-185">Динамические свойства подключения</span><span class="sxs-lookup"><span data-stu-id="c6e9c-185">Connection Dynamic Properties</span></span>

<span data-ttu-id="c6e9c-186">Коллекция **Properties** объект **подключения** добавляются следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c6e9c-186">The following properties are added to the **Connection** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c6e9c-187">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="c6e9c-187">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="c6e9c-188">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="c6e9c-188">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-189">Активных сеансов</span><span class="sxs-lookup"><span data-stu-id="c6e9c-189">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-190">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="c6e9c-190">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-191">Прерывание Asynchable</span><span class="sxs-lookup"><span data-stu-id="c6e9c-191">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-192">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="c6e9c-192">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-193">Зафиксировать Asynchable</span><span class="sxs-lookup"><span data-stu-id="c6e9c-193">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-194">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="c6e9c-194">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-195">Уровни изоляции автоматической фиксации</span><span class="sxs-lookup"><span data-stu-id="c6e9c-195">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-196">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="c6e9c-196">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-197">Расположение каталога</span><span class="sxs-lookup"><span data-stu-id="c6e9c-197">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-198">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="c6e9c-198">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-199">Каталог терминов</span><span class="sxs-lookup"><span data-stu-id="c6e9c-199">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-200">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="c6e9c-200">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-201">Определение столбца</span><span class="sxs-lookup"><span data-stu-id="c6e9c-201">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-202">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="c6e9c-202">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-203">Время ожидания подключения</span><span class="sxs-lookup"><span data-stu-id="c6e9c-203">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-204">DBPROP_INIT_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="c6e9c-204">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-205">Текущий каталог</span><span class="sxs-lookup"><span data-stu-id="c6e9c-205">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-206">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="c6e9c-206">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-207">Источник данных</span><span class="sxs-lookup"><span data-stu-id="c6e9c-207">Data Source</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-208">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="c6e9c-208">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-209">Имя источника данных</span><span class="sxs-lookup"><span data-stu-id="c6e9c-209">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-210">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="c6e9c-210">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-211">Модель потоков объекта источника данных</span><span class="sxs-lookup"><span data-stu-id="c6e9c-211">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-212">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="c6e9c-212">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-213">Имя СУБД</span><span class="sxs-lookup"><span data-stu-id="c6e9c-213">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-214">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="c6e9c-214">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-215">Версия СУБД</span><span class="sxs-lookup"><span data-stu-id="c6e9c-215">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-216">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="c6e9c-216">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-217">Расширенные свойства</span><span class="sxs-lookup"><span data-stu-id="c6e9c-217">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-218">DBPROP_INIT_PROVIDERSTRING</span><span class="sxs-lookup"><span data-stu-id="c6e9c-218">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-219">ГРУППИРОВКА по поддержке</span><span class="sxs-lookup"><span data-stu-id="c6e9c-219">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-220">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="c6e9c-220">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-221">Поддержка разнородных таблиц</span><span class="sxs-lookup"><span data-stu-id="c6e9c-221">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-222">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="c6e9c-222">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-223">Идентификатор регистра</span><span class="sxs-lookup"><span data-stu-id="c6e9c-223">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-224">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="c6e9c-224">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-225">Исходный каталог</span><span class="sxs-lookup"><span data-stu-id="c6e9c-225">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-226">DBPROP_INIT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c6e9c-226">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-227">Уровни изоляции</span><span class="sxs-lookup"><span data-stu-id="c6e9c-227">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-228">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="c6e9c-228">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-229">Хранение изоляции</span><span class="sxs-lookup"><span data-stu-id="c6e9c-229">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-230">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="c6e9c-230">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-231">Идентификатор языка</span><span class="sxs-lookup"><span data-stu-id="c6e9c-231">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-232">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="c6e9c-232">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-233">Максимальный размер индекса</span><span class="sxs-lookup"><span data-stu-id="c6e9c-233">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-234">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="c6e9c-234">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-235">Максимальный размер строки</span><span class="sxs-lookup"><span data-stu-id="c6e9c-235">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-236">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="c6e9c-236">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-237">Максимальный размер строки включает в себя больших двоичных ОБЪЕКТОВ</span><span class="sxs-lookup"><span data-stu-id="c6e9c-237">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-238">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="c6e9c-238">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-239">Максимальная таблиц в Выбор</span><span class="sxs-lookup"><span data-stu-id="c6e9c-239">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-240">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="c6e9c-240">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-241">Несколько наборов параметров</span><span class="sxs-lookup"><span data-stu-id="c6e9c-241">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-242">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="c6e9c-242">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-243">Несколько результатов</span><span class="sxs-lookup"><span data-stu-id="c6e9c-243">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-244">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="c6e9c-244">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-245">Несколько объектов хранения</span><span class="sxs-lookup"><span data-stu-id="c6e9c-245">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-246">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="c6e9c-246">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-247">Обновление нескольких таблицы</span><span class="sxs-lookup"><span data-stu-id="c6e9c-247">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-248">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="c6e9c-248">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-249">Порядок сортировки значений NULL</span><span class="sxs-lookup"><span data-stu-id="c6e9c-249">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-250">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="c6e9c-250">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-251">Поведение NULL объединения</span><span class="sxs-lookup"><span data-stu-id="c6e9c-251">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-252">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="c6e9c-252">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-253">Версия OLE DB</span><span class="sxs-lookup"><span data-stu-id="c6e9c-253">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-254">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="c6e9c-254">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-255">Поддержка OLE-объектов</span><span class="sxs-lookup"><span data-stu-id="c6e9c-255">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-256">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="c6e9c-256">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-257">Поддержка открытых наборов строк</span><span class="sxs-lookup"><span data-stu-id="c6e9c-257">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-258">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="c6e9c-258">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-259">ORDER BY столбцы в списке Select</span><span class="sxs-lookup"><span data-stu-id="c6e9c-259">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-260">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="c6e9c-260">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-261">Выходной параметр доступности</span><span class="sxs-lookup"><span data-stu-id="c6e9c-261">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-262">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="c6e9c-262">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-263">Передайте с указанные методы</span><span class="sxs-lookup"><span data-stu-id="c6e9c-263">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-264">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="c6e9c-264">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-265">Password</span><span class="sxs-lookup"><span data-stu-id="c6e9c-265">Password</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-266">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="c6e9c-266">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-267">Сохранять сведения о безопасности</span><span class="sxs-lookup"><span data-stu-id="c6e9c-267">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-268">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span><span class="sxs-lookup"><span data-stu-id="c6e9c-268">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-269">Тип сохраняемого идентификатора</span><span class="sxs-lookup"><span data-stu-id="c6e9c-269">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-270">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="c6e9c-270">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-271">Подготовка поведение аварийное завершение</span><span class="sxs-lookup"><span data-stu-id="c6e9c-271">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-272">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="c6e9c-272">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-273">Подготовка поведение выделения</span><span class="sxs-lookup"><span data-stu-id="c6e9c-273">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-274">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="c6e9c-274">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-275">Процедура терминов</span><span class="sxs-lookup"><span data-stu-id="c6e9c-275">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-276">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="c6e9c-276">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-277">Запрос</span><span class="sxs-lookup"><span data-stu-id="c6e9c-277">Prompt</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-278">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="c6e9c-278">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-279">Понятное имя поставщика</span><span class="sxs-lookup"><span data-stu-id="c6e9c-279">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-280">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="c6e9c-280">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-281">Имя поставщика</span><span class="sxs-lookup"><span data-stu-id="c6e9c-281">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-282">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="c6e9c-282">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-283">Версия поставщика</span><span class="sxs-lookup"><span data-stu-id="c6e9c-283">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-284">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="c6e9c-284">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-285">Источник данных только для чтения</span><span class="sxs-lookup"><span data-stu-id="c6e9c-285">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-286">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="c6e9c-286">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-287">Преобразование строк на команду</span><span class="sxs-lookup"><span data-stu-id="c6e9c-287">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-288">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="c6e9c-288">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-289">Схема терминов</span><span class="sxs-lookup"><span data-stu-id="c6e9c-289">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-290">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="c6e9c-290">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-291">Об использовании схемы</span><span class="sxs-lookup"><span data-stu-id="c6e9c-291">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-292">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="c6e9c-292">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-293">Поддержка SQL</span><span class="sxs-lookup"><span data-stu-id="c6e9c-293">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-294">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="c6e9c-294">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-295">Структурированное хранилище</span><span class="sxs-lookup"><span data-stu-id="c6e9c-295">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-296">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="c6e9c-296">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-297">Поддержка вложенного запроса</span><span class="sxs-lookup"><span data-stu-id="c6e9c-297">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-298">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="c6e9c-298">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-299">В таблице терминов</span><span class="sxs-lookup"><span data-stu-id="c6e9c-299">Table Term</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-300">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="c6e9c-300">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-301">Транзакций DDL</span><span class="sxs-lookup"><span data-stu-id="c6e9c-301">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-302">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="c6e9c-302">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-303">Идентификатор пользователя</span><span class="sxs-lookup"><span data-stu-id="c6e9c-303">User ID</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-304">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="c6e9c-304">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-305">Имя пользователя</span><span class="sxs-lookup"><span data-stu-id="c6e9c-305">User Name</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-306">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="c6e9c-306">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-307">Дескриптор окна</span><span class="sxs-lookup"><span data-stu-id="c6e9c-307">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-308">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="c6e9c-308">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a><span data-ttu-id="c6e9c-309">Свойства динамической набора записей</span><span class="sxs-lookup"><span data-stu-id="c6e9c-309">Recordset Dynamic Properties</span></span>

<span data-ttu-id="c6e9c-310">Следующие свойства добавляются в коллекцию **свойств** объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="c6e9c-310">The following properties are added to the **Recordset** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c6e9c-311">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="c6e9c-311">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="c6e9c-312">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="c6e9c-312">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-313">Порядок доступа</span><span class="sxs-lookup"><span data-stu-id="c6e9c-313">Access Order</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-314">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="c6e9c-314">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-315">Блокировка объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="c6e9c-315">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-316">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="c6e9c-316">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-317">Тип закладки</span><span class="sxs-lookup"><span data-stu-id="c6e9c-317">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-318">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="c6e9c-318">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-319">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="c6e9c-319">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-320">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="c6e9c-320">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-321">Изменение вставленных строк</span><span class="sxs-lookup"><span data-stu-id="c6e9c-321">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-322">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="c6e9c-322">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-323">Права доступа столбца</span><span class="sxs-lookup"><span data-stu-id="c6e9c-323">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-324">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="c6e9c-324">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-325">Столбец набор уведомлений</span><span class="sxs-lookup"><span data-stu-id="c6e9c-325">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-326">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="c6e9c-326">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-327">Время ожидания команды</span><span class="sxs-lookup"><span data-stu-id="c6e9c-327">Command Time Out</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-328">DBPROP_COMMANDTIMEOUT</span><span class="sxs-lookup"><span data-stu-id="c6e9c-328">DBPROP_COMMANDTIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-329">Отложите столбца</span><span class="sxs-lookup"><span data-stu-id="c6e9c-329">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-330">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="c6e9c-330">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-331">Отложенное обновление объекта хранения</span><span class="sxs-lookup"><span data-stu-id="c6e9c-331">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-332">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="c6e9c-332">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-333">Выборку</span><span class="sxs-lookup"><span data-stu-id="c6e9c-333">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-334">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="c6e9c-334">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-335">Хранение строк</span><span class="sxs-lookup"><span data-stu-id="c6e9c-335">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-336">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="c6e9c-336">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-337">IAccessor</span><span class="sxs-lookup"><span data-stu-id="c6e9c-337">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-338">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="c6e9c-338">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-339">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="c6e9c-339">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-340">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="c6e9c-340">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-341">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="c6e9c-341">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-342">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="c6e9c-342">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-343">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="c6e9c-343">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-344">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="c6e9c-344">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-345">IConvertType</span><span class="sxs-lookup"><span data-stu-id="c6e9c-345">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-346">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="c6e9c-346">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-347">Немобильные строки</span><span class="sxs-lookup"><span data-stu-id="c6e9c-347">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-348">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="c6e9c-348">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-349">IRowset</span><span class="sxs-lookup"><span data-stu-id="c6e9c-349">IRowset</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-350">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="c6e9c-350">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-351">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="c6e9c-351">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-352">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="c6e9c-352">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-353">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="c6e9c-353">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-354">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="c6e9c-354">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-355">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="c6e9c-355">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-356">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="c6e9c-356">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-357">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="c6e9c-357">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-358">DBPROP_IRowsestLocate</span><span class="sxs-lookup"><span data-stu-id="c6e9c-358">DBPROP_IRowsestLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-359">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="c6e9c-359">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-360">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="c6e9c-360">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-361">DBPROP_IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="c6e9c-361">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-362">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="c6e9c-362">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-363">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="c6e9c-363">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-364">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="c6e9c-364">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-365">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="c6e9c-365">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-366">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="c6e9c-366">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-367">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="c6e9c-367">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-368">Литерал закладки</span><span class="sxs-lookup"><span data-stu-id="c6e9c-368">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-369">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="c6e9c-369">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-370">Удостоверение литерала строки</span><span class="sxs-lookup"><span data-stu-id="c6e9c-370">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-371">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="c6e9c-371">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-372">Максимальное число открытых строк</span><span class="sxs-lookup"><span data-stu-id="c6e9c-372">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-373">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="c6e9c-373">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-374">Максимум ожидающие строк</span><span class="sxs-lookup"><span data-stu-id="c6e9c-374">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-375">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="c6e9c-375">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-376">Максимальное число строк</span><span class="sxs-lookup"><span data-stu-id="c6e9c-376">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-377">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="c6e9c-377">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-378">Степень детализации уведомлений</span><span class="sxs-lookup"><span data-stu-id="c6e9c-378">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-379">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="c6e9c-379">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-380">Этапы уведомлений</span><span class="sxs-lookup"><span data-stu-id="c6e9c-380">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-381">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="c6e9c-381">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-382">Объекты в транзакции</span><span class="sxs-lookup"><span data-stu-id="c6e9c-382">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-383">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="c6e9c-383">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-384">Видны прочие изменения</span><span class="sxs-lookup"><span data-stu-id="c6e9c-384">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-385">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="c6e9c-385">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-386">Других пользователей вставки видимым</span><span class="sxs-lookup"><span data-stu-id="c6e9c-386">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-387">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="c6e9c-387">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-388">Видны собственные изменения</span><span class="sxs-lookup"><span data-stu-id="c6e9c-388">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-389">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="c6e9c-389">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-390">Видны собственные операции вставки</span><span class="sxs-lookup"><span data-stu-id="c6e9c-390">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-391">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="c6e9c-391">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-392">Сохранять при аварийном завершении</span><span class="sxs-lookup"><span data-stu-id="c6e9c-392">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-393">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="c6e9c-393">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-394">Сохранять при фиксации</span><span class="sxs-lookup"><span data-stu-id="c6e9c-394">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-395">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="c6e9c-395">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-396">Быстрый перезапуск</span><span class="sxs-lookup"><span data-stu-id="c6e9c-396">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-397">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="c6e9c-397">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-398">Повторные события</span><span class="sxs-lookup"><span data-stu-id="c6e9c-398">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-399">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="c6e9c-399">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-400">Удаление удаленных строк</span><span class="sxs-lookup"><span data-stu-id="c6e9c-400">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-401">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="c6e9c-401">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-402">Сообщить о нескольких изменений</span><span class="sxs-lookup"><span data-stu-id="c6e9c-402">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-403">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="c6e9c-403">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-404">Вернуть ожидающие вставки</span><span class="sxs-lookup"><span data-stu-id="c6e9c-404">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-405">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="c6e9c-405">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-406">Удалить строку уведомлений</span><span class="sxs-lookup"><span data-stu-id="c6e9c-406">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-407">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="c6e9c-407">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-408">Строка первого уведомления об изменении</span><span class="sxs-lookup"><span data-stu-id="c6e9c-408">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-409">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="c6e9c-409">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-410">Строка вставки уведомлений</span><span class="sxs-lookup"><span data-stu-id="c6e9c-410">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-411">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="c6e9c-411">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-412">Привилегии строки</span><span class="sxs-lookup"><span data-stu-id="c6e9c-412">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-413">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="c6e9c-413">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-414">Уведомления о повторной синхронизации строки</span><span class="sxs-lookup"><span data-stu-id="c6e9c-414">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-415">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="c6e9c-415">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-416">Строка, потоковой модели</span><span class="sxs-lookup"><span data-stu-id="c6e9c-416">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-417">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="c6e9c-417">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-418">Уведомление об изменении отмены строки</span><span class="sxs-lookup"><span data-stu-id="c6e9c-418">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-419">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="c6e9c-419">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-420">Строка отмены Delete уведомлений</span><span class="sxs-lookup"><span data-stu-id="c6e9c-420">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-421">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="c6e9c-421">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-422">Вставка отмены строки уведомлений</span><span class="sxs-lookup"><span data-stu-id="c6e9c-422">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-423">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="c6e9c-423">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-424">Уведомление об обновлении строки</span><span class="sxs-lookup"><span data-stu-id="c6e9c-424">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-425">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="c6e9c-425">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-426">Уведомление об изменении положения строк выборки</span><span class="sxs-lookup"><span data-stu-id="c6e9c-426">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-427">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="c6e9c-427">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-428">Уведомление о выпуске набора строк</span><span class="sxs-lookup"><span data-stu-id="c6e9c-428">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-429">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="c6e9c-429">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-430">Прокрутка назад</span><span class="sxs-lookup"><span data-stu-id="c6e9c-430">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-431">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="c6e9c-431">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-432">Серверный курсор</span><span class="sxs-lookup"><span data-stu-id="c6e9c-432">Server Cursor</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-433">DBPROP_SERVERCURSOR</span><span class="sxs-lookup"><span data-stu-id="c6e9c-433">DBPROP_SERVERCURSOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-434">Пропустить удаленных закладки</span><span class="sxs-lookup"><span data-stu-id="c6e9c-434">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-435">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="c6e9c-435">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-436">Строка строгого удостоверений</span><span class="sxs-lookup"><span data-stu-id="c6e9c-436">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-437">DBPROP_STRONGITDENTITY</span><span class="sxs-lookup"><span data-stu-id="c6e9c-437">DBPROP_STRONGITDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-438">Уникальные строки</span><span class="sxs-lookup"><span data-stu-id="c6e9c-438">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-439">DBPROP_UNIQUEROWS</span><span class="sxs-lookup"><span data-stu-id="c6e9c-439">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-440">Возможности обновления</span><span class="sxs-lookup"><span data-stu-id="c6e9c-440">Updatability</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-441">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="c6e9c-441">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-442">Использование закладок</span><span class="sxs-lookup"><span data-stu-id="c6e9c-442">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-443">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="c6e9c-443">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a><span data-ttu-id="c6e9c-444">Динамические свойства команды</span><span class="sxs-lookup"><span data-stu-id="c6e9c-444">Command Dynamic Properties</span></span>

<span data-ttu-id="c6e9c-445">Следующие свойства добавляются в коллекцию **свойств** объекта **команды** .</span><span class="sxs-lookup"><span data-stu-id="c6e9c-445">The following properties are added to the **Command** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c6e9c-446">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="c6e9c-446">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="c6e9c-447">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="c6e9c-447">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-448">Порядок доступа</span><span class="sxs-lookup"><span data-stu-id="c6e9c-448">Access Order</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-449">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="c6e9c-449">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-450">Базовый путь</span><span class="sxs-lookup"><span data-stu-id="c6e9c-450">Base Path</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-451">SSPROP_STREAM_BASEPATH</span><span class="sxs-lookup"><span data-stu-id="c6e9c-451">SSPROP_STREAM_BASEPATH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-452">Блокировка объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="c6e9c-452">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-453">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="c6e9c-453">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-454">Тип закладки</span><span class="sxs-lookup"><span data-stu-id="c6e9c-454">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-455">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="c6e9c-455">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-456">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="c6e9c-456">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-457">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="c6e9c-457">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-458">Изменение вставленных строк</span><span class="sxs-lookup"><span data-stu-id="c6e9c-458">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-459">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="c6e9c-459">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-460">Права доступа столбца</span><span class="sxs-lookup"><span data-stu-id="c6e9c-460">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-461">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="c6e9c-461">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-462">Столбец набор уведомлений</span><span class="sxs-lookup"><span data-stu-id="c6e9c-462">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-463">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="c6e9c-463">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-464">Тип контента</span><span class="sxs-lookup"><span data-stu-id="c6e9c-464">Content Type</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-465">SSPROP_STREAM_CONTENTTYPE</span><span class="sxs-lookup"><span data-stu-id="c6e9c-465">SSPROP_STREAM_CONTENTTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-466">Автоматическая выборка курсора</span><span class="sxs-lookup"><span data-stu-id="c6e9c-466">Cursor Auto Fetch</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-467">SSPROP_CURSORAUTOFETCH</span><span class="sxs-lookup"><span data-stu-id="c6e9c-467">SSPROP_CURSORAUTOFETCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-468">Отложите столбца</span><span class="sxs-lookup"><span data-stu-id="c6e9c-468">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-469">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="c6e9c-469">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-470">Отложите Подготовка</span><span class="sxs-lookup"><span data-stu-id="c6e9c-470">Defer Prepare</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-471">SSPROP_DEFERPREPARE</span><span class="sxs-lookup"><span data-stu-id="c6e9c-471">SSPROP_DEFERPREPARE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-472">Отложенное обновление объекта хранения</span><span class="sxs-lookup"><span data-stu-id="c6e9c-472">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-473">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="c6e9c-473">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-474">Выборку</span><span class="sxs-lookup"><span data-stu-id="c6e9c-474">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-475">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="c6e9c-475">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-476">Хранение строк</span><span class="sxs-lookup"><span data-stu-id="c6e9c-476">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-477">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="c6e9c-477">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-478">IAccessor</span><span class="sxs-lookup"><span data-stu-id="c6e9c-478">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-479">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="c6e9c-479">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-480">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="c6e9c-480">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-481">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="c6e9c-481">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-482">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="c6e9c-482">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-483">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="c6e9c-483">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-484">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="c6e9c-484">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-485">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="c6e9c-485">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-486">IConvertType</span><span class="sxs-lookup"><span data-stu-id="c6e9c-486">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-487">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="c6e9c-487">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-488">Немобильные строки</span><span class="sxs-lookup"><span data-stu-id="c6e9c-488">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-489">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="c6e9c-489">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-490">IRowset</span><span class="sxs-lookup"><span data-stu-id="c6e9c-490">IRowset</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-491">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="c6e9c-491">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-492">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="c6e9c-492">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-493">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="c6e9c-493">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-494">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="c6e9c-494">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-495">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="c6e9c-495">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-496">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="c6e9c-496">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-497">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="c6e9c-497">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-498">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="c6e9c-498">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-499">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="c6e9c-499">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-500">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="c6e9c-500">IRowsetResynch</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-501">DBPROP_IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="c6e9c-501">DBPROP_IRowsetResynch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-502">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="c6e9c-502">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-503">DBPROP_IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="c6e9c-503">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-504">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="c6e9c-504">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-505">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="c6e9c-505">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-506">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="c6e9c-506">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-507">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="c6e9c-507">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-508">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="c6e9c-508">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-509">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="c6e9c-509">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-510">Литерал закладки</span><span class="sxs-lookup"><span data-stu-id="c6e9c-510">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-511">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="c6e9c-511">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-512">Удостоверение литерала строки</span><span class="sxs-lookup"><span data-stu-id="c6e9c-512">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-513">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="c6e9c-513">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-514">Режим блокировки</span><span class="sxs-lookup"><span data-stu-id="c6e9c-514">Lock Mode</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-515">DBPROP_LOCKMODE</span><span class="sxs-lookup"><span data-stu-id="c6e9c-515">DBPROP_LOCKMODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-516">Максимальное число открытых строк</span><span class="sxs-lookup"><span data-stu-id="c6e9c-516">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-517">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="c6e9c-517">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-518">Максимум ожидающие строк</span><span class="sxs-lookup"><span data-stu-id="c6e9c-518">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-519">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="c6e9c-519">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-520">Максимальное число строк</span><span class="sxs-lookup"><span data-stu-id="c6e9c-520">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-521">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="c6e9c-521">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-522">Степень детализации уведомлений</span><span class="sxs-lookup"><span data-stu-id="c6e9c-522">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-523">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="c6e9c-523">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-524">Этапы уведомлений</span><span class="sxs-lookup"><span data-stu-id="c6e9c-524">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-525">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="c6e9c-525">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-526">Объекты в транзакции</span><span class="sxs-lookup"><span data-stu-id="c6e9c-526">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-527">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="c6e9c-527">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-528">Видны прочие изменения</span><span class="sxs-lookup"><span data-stu-id="c6e9c-528">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-529">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="c6e9c-529">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-530">Других пользователей вставки видимым</span><span class="sxs-lookup"><span data-stu-id="c6e9c-530">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-531">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="c6e9c-531">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-532">Свойство кодировки выходных данных</span><span class="sxs-lookup"><span data-stu-id="c6e9c-532">Output Encoding Property</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-533">DBPROP_OUTPUTENCODING</span><span class="sxs-lookup"><span data-stu-id="c6e9c-533">DBPROP_OUTPUTENCODING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-534">Свойство потока выходных данных</span><span class="sxs-lookup"><span data-stu-id="c6e9c-534">Output Stream Property</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-535">DBPROP_OUTPUTSTREAM</span><span class="sxs-lookup"><span data-stu-id="c6e9c-535">DBPROP_OUTPUTSTREAM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-536">Видны собственные изменения</span><span class="sxs-lookup"><span data-stu-id="c6e9c-536">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-537">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="c6e9c-537">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-538">Видны собственные операции вставки</span><span class="sxs-lookup"><span data-stu-id="c6e9c-538">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-539">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="c6e9c-539">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-540">Сохранять при аварийном завершении</span><span class="sxs-lookup"><span data-stu-id="c6e9c-540">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-541">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="c6e9c-541">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-542">Сохранять при фиксации</span><span class="sxs-lookup"><span data-stu-id="c6e9c-542">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-543">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="c6e9c-543">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-544">Быстрый перезапуск</span><span class="sxs-lookup"><span data-stu-id="c6e9c-544">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-545">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="c6e9c-545">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-546">Повторные события</span><span class="sxs-lookup"><span data-stu-id="c6e9c-546">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-547">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="c6e9c-547">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-548">Удаление удаленных строк</span><span class="sxs-lookup"><span data-stu-id="c6e9c-548">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-549">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="c6e9c-549">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-550">Сообщить о нескольких изменений</span><span class="sxs-lookup"><span data-stu-id="c6e9c-550">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-551">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="c6e9c-551">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-552">Вернуть ожидающие вставки</span><span class="sxs-lookup"><span data-stu-id="c6e9c-552">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-553">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="c6e9c-553">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-554">Удалить строку уведомлений</span><span class="sxs-lookup"><span data-stu-id="c6e9c-554">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-555">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="c6e9c-555">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-556">Строка первого уведомления об изменении</span><span class="sxs-lookup"><span data-stu-id="c6e9c-556">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-557">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="c6e9c-557">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-558">Строка вставки уведомлений</span><span class="sxs-lookup"><span data-stu-id="c6e9c-558">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-559">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="c6e9c-559">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-560">Привилегии строки</span><span class="sxs-lookup"><span data-stu-id="c6e9c-560">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-561">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="c6e9c-561">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-562">Уведомления о повторной синхронизации строки</span><span class="sxs-lookup"><span data-stu-id="c6e9c-562">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-563">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="c6e9c-563">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-564">Строка, потоковой модели</span><span class="sxs-lookup"><span data-stu-id="c6e9c-564">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-565">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="c6e9c-565">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-566">Уведомление об изменении отмены строки</span><span class="sxs-lookup"><span data-stu-id="c6e9c-566">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-567">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="c6e9c-567">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-568">Строка отмены Delete уведомлений</span><span class="sxs-lookup"><span data-stu-id="c6e9c-568">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-569">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="c6e9c-569">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-570">Вставка отмены строки уведомлений</span><span class="sxs-lookup"><span data-stu-id="c6e9c-570">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-571">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="c6e9c-571">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-572">Уведомление об обновлении строки</span><span class="sxs-lookup"><span data-stu-id="c6e9c-572">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-573">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="c6e9c-573">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-574">Уведомление об изменении положения строк выборки</span><span class="sxs-lookup"><span data-stu-id="c6e9c-574">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-575">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="c6e9c-575">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-576">Уведомление о выпуске набора строк</span><span class="sxs-lookup"><span data-stu-id="c6e9c-576">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-577">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="c6e9c-577">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-578">Прокрутка назад</span><span class="sxs-lookup"><span data-stu-id="c6e9c-578">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-579">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="c6e9c-579">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-580">Серверный курсор</span><span class="sxs-lookup"><span data-stu-id="c6e9c-580">Server Cursor</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-581">DBPROP_SERVERCURSOR</span><span class="sxs-lookup"><span data-stu-id="c6e9c-581">DBPROP_SERVERCURSOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-582">Вставка данных сервера</span><span class="sxs-lookup"><span data-stu-id="c6e9c-582">Server Data on Insert</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-583">DBPROP_SERVERDATAONINSERT</span><span class="sxs-lookup"><span data-stu-id="c6e9c-583">DBPROP_SERVERDATAONINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-584">Пропустить удаленных закладки</span><span class="sxs-lookup"><span data-stu-id="c6e9c-584">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-585">DBPROP_BOOKMARKSKIP</span><span class="sxs-lookup"><span data-stu-id="c6e9c-585">DBPROP_BOOKMARKSKIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-586">Строка строгого удостоверений</span><span class="sxs-lookup"><span data-stu-id="c6e9c-586">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-587">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="c6e9c-587">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-588">Возможности обновления</span><span class="sxs-lookup"><span data-stu-id="c6e9c-588">Updatability</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-589">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="c6e9c-589">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-590">Использование закладок</span><span class="sxs-lookup"><span data-stu-id="c6e9c-590">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-591">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="c6e9c-591">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e9c-592">Корневой XML</span><span class="sxs-lookup"><span data-stu-id="c6e9c-592">XML Root</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-593">SSPROP_STREAM_XMLROOT</span><span class="sxs-lookup"><span data-stu-id="c6e9c-593">SSPROP_STREAM_XMLROOT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e9c-594">XSL</span><span class="sxs-lookup"><span data-stu-id="c6e9c-594">XSL</span></span></p></td>
<td><p><span data-ttu-id="c6e9c-595">SSPROP_STREAM_XSL</span><span class="sxs-lookup"><span data-stu-id="c6e9c-595">SSPROP_STREAM_XSL</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c6e9c-596">Сведения о реализации и функциональным сведений о Microsoft SQL Server поставщик OLE DB можно найти поставщика OLE DB для документации по SQL Server в разделе OLE DB MDAC SDK.</span><span class="sxs-lookup"><span data-stu-id="c6e9c-596">For specific implementation details and functional information about the Microsoft SQL Server OLE DB Provider, consult the OLE DB Provider for SQL Server documentation in the OLE DB section of the MDAC SDK.</span></span>

