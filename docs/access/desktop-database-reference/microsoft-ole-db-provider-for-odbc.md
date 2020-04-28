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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288913"
---
# <a name="microsoft-ole-db-provider-for-odbc"></a><span data-ttu-id="c77fc-102">Поставщик Microsoft OLE DB для ODBC</span><span class="sxs-lookup"><span data-stu-id="c77fc-102">Microsoft OLE DB Provider for ODBC</span></span>

<span data-ttu-id="c77fc-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c77fc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c77fc-104">Для программистов ADO или RDS лучше всего один, в котором каждый источник данных предоставляет интерфейс OLE DB, чтобы ADO мог напрямую вызывать источник данных.</span><span class="sxs-lookup"><span data-stu-id="c77fc-104">To an ADO or RDS programmer, an ideal world would be one in which every data source exposes an OLE DB interface, so that ADO could call directly into the data source.</span></span> <span data-ttu-id="c77fc-105">Несмотря на то, что дополнительные поставщики баз данных реализуют интерфейсы OLE DB, некоторые источники данных пока не предоставляются таким образом.</span><span class="sxs-lookup"><span data-stu-id="c77fc-105">Although increasingly more database vendors are implementing OLE DB interfaces, some data sources are not yet exposed this way.</span></span> <span data-ttu-id="c77fc-106">Тем не менее, практически все используемые сегодня системы СУБД можно получить с помощью ODBC.</span><span class="sxs-lookup"><span data-stu-id="c77fc-106">However, virtually all DBMS systems in use today can be accessed through ODBC.</span></span>

<span data-ttu-id="c77fc-107">Драйверы ODBC доступны для всех основных СУБД, используемых в настоящее время, включая Microsoft SQL Server, Microsoft Access (ядро базы данных Microsoft Jet) и Microsoft FoxPro, в дополнение к продуктам баз данных, отличным от Майкрософт, например Oracle.</span><span class="sxs-lookup"><span data-stu-id="c77fc-107">ODBC drivers are available for every major DBMS in use today, including Microsoft SQL Server, Microsoft Access (Microsoft Jet database engine), and Microsoft FoxPro, in addition to non-Microsoft database products such as Oracle.</span></span>

<span data-ttu-id="c77fc-108">Тем не менее, поставщик Microsoft ODBC позволяет ADO подключаться к любому источнику данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="c77fc-108">The Microsoft ODBC Provider, however, allows ADO to connect to any ODBC data source.</span></span> <span data-ttu-id="c77fc-109">Поставщик доступен для бесплатных потоков и включен Юникод.</span><span class="sxs-lookup"><span data-stu-id="c77fc-109">The provider is free-threaded and Unicode enabled.</span></span>

<span data-ttu-id="c77fc-110">Поставщик поддерживает транзакции, хотя различные механизмы СУБД предоставляют различные типы поддержки транзакций.</span><span class="sxs-lookup"><span data-stu-id="c77fc-110">The provider supports transactions, although different DBMS engines offer different types of transaction support.</span></span> <span data-ttu-id="c77fc-111">Например, Microsoft Access поддерживает вложенные транзакции вплоть до пяти уровней.</span><span class="sxs-lookup"><span data-stu-id="c77fc-111">For example, Microsoft Access supports nested transactions up to five levels deep.</span></span>

<span data-ttu-id="c77fc-112">Это поставщик по умолчанию для ADO, а также поддерживаются все свойства и методы, зависящие от поставщика.</span><span class="sxs-lookup"><span data-stu-id="c77fc-112">This is the default provider for ADO, and all provider-dependent ADO properties and methods are supported.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="c77fc-113">Параметры строки подключения</span><span class="sxs-lookup"><span data-stu-id="c77fc-113">Connection String Parameters</span></span>

<span data-ttu-id="c77fc-114">Чтобы подключиться к поставщику, присвойте аргументу **provider =** свойства [ConnectionString](connectionstring-property-ado.md) значение:</span><span class="sxs-lookup"><span data-stu-id="c77fc-114">To connect to this provider, set the **Provider=** argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```sql 
 
MSDASQL 
```

<span data-ttu-id="c77fc-115">Считывание свойства [provider](provider-property-ado.md) также возвратит эту строку.</span><span class="sxs-lookup"><span data-stu-id="c77fc-115">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="c77fc-116">Типичная строка подключения</span><span class="sxs-lookup"><span data-stu-id="c77fc-116">Typical Connection String</span></span>

<span data-ttu-id="c77fc-117">Типичная строка подключения для этого поставщика:</span><span class="sxs-lookup"><span data-stu-id="c77fc-117">A typical connection string for this provider is:</span></span>

```sql 
 
"Provider=MSDASQL;DSN=dsnName;UID=userName;PWD=userPassword;" 
```

<span data-ttu-id="c77fc-118">Строка состоит из следующих ключевых слов:</span><span class="sxs-lookup"><span data-stu-id="c77fc-118">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c77fc-119">Ключевое слово</span><span class="sxs-lookup"><span data-stu-id="c77fc-119">Keyword</span></span></p></th>
<th><p><span data-ttu-id="c77fc-120">Описание</span><span class="sxs-lookup"><span data-stu-id="c77fc-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-121"><strong>Поставщик</strong></span><span class="sxs-lookup"><span data-stu-id="c77fc-121"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="c77fc-122">Указывает поставщика OLE DB для ODBC.</span><span class="sxs-lookup"><span data-stu-id="c77fc-122">Specifies the OLE DB Provider for ODBC.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-123"><strong>DSN</strong></span><span class="sxs-lookup"><span data-stu-id="c77fc-123"><strong>DSN</strong></span></span></p></td>
<td><p><span data-ttu-id="c77fc-124">Указывает имя источника данных.</span><span class="sxs-lookup"><span data-stu-id="c77fc-124">Specifies the data source name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-125"><strong>UID</strong></span><span class="sxs-lookup"><span data-stu-id="c77fc-125"><strong>UID</strong></span></span></p></td>
<td><p><span data-ttu-id="c77fc-126">Задает имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="c77fc-126">Specifies the user name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-127"><strong>PWD</strong></span><span class="sxs-lookup"><span data-stu-id="c77fc-127"><strong>PWD</strong></span></span></p></td>
<td><p><span data-ttu-id="c77fc-128">Указывает пароль пользователя.</span><span class="sxs-lookup"><span data-stu-id="c77fc-128">Specifies the user password.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-129"><strong>URL</strong></span><span class="sxs-lookup"><span data-stu-id="c77fc-129"><strong>URL</strong></span></span></p></td>
<td><p><span data-ttu-id="c77fc-130">Указывает URL-адрес файла или каталога, опубликованного в веб-папке.</span><span class="sxs-lookup"><span data-stu-id="c77fc-130">Specifies the URL of a file or directory published in a web folder.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c77fc-131">Так как это поставщик по умолчанию для ADO, если вы опустите параметр **provider =** из строки подключения, ADO попытается установить подключение к этому поставщику.</span><span class="sxs-lookup"><span data-stu-id="c77fc-131">Because this is the default provider for ADO, if you omit the **Provider=** parameter from the connection string, ADO will attempt to establish a connection to this provider.</span></span>

<span data-ttu-id="c77fc-132">Поставщик не поддерживает никакие особые параметры подключения, кроме тех, которые определены в ADO.</span><span class="sxs-lookup"><span data-stu-id="c77fc-132">The provider does not support any specific connection parameters in addition to those defined by ADO.</span></span> <span data-ttu-id="c77fc-133">Тем не менее, поставщик передаст параметры подключений, не являющихся ADO, в диспетчер драйверов ODBC.</span><span class="sxs-lookup"><span data-stu-id="c77fc-133">However, the provider will pass any non-ADO connection parameters to the ODBC driver manager.</span></span>

<span data-ttu-id="c77fc-134">Так как вы можете опустить параметр **provider** , вы можете создать строку подключения ADO, идентичную строке подключения ODBC для одного и того же источника данных.</span><span class="sxs-lookup"><span data-stu-id="c77fc-134">Because you can omit the **Provider** parameter, you can therefore compose an ADO connection string that is identical to an ODBC connection string for the same data source.</span></span> <span data-ttu-id="c77fc-135">Используйте те же имена параметров (**Driver =**, **Database =**, **DSN =** и т. д.), значения и синтаксис, что и при создании строки подключения ODBC.</span><span class="sxs-lookup"><span data-stu-id="c77fc-135">Use the same parameter names (**DRIVER=**, **DATABASE=**, **DSN=**, and so on), values, and syntax as you would when composing an ODBC connection string.</span></span> <span data-ttu-id="c77fc-136">Можно подключаться к предварительно заданному имени источника данных (DSN) или Филедсн без него.</span><span class="sxs-lookup"><span data-stu-id="c77fc-136">You can connect with or without a predefined data source name (DSN) or FileDSN.</span></span>

<span data-ttu-id="c77fc-137">**Синтаксис с именем DSN или Филедсн:**</span><span class="sxs-lookup"><span data-stu-id="c77fc-137">**Syntax with a DSN or FileDSN:**</span></span>

`"[Provider=MSDASQL;] { DSN=name | FileDSN=filename } ; [DATABASE=database;] UID=user; PWD=password"`

<span data-ttu-id="c77fc-138">**Синтаксис без имени DSN (подключение без DSN):**</span><span class="sxs-lookup"><span data-stu-id="c77fc-138">**Syntax without a DSN (DSN-less connection):**</span></span>

`"[Provider=MSDASQL;] DRIVER=driver; SERVER=server;DATABASE=database; UID=user; PWD=password"`

<span data-ttu-id="c77fc-139">Если вы используете **имя DSN** или **филедсн**, оно должно быть определено администратором источника данных ODBC в панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="c77fc-139">If you use a **DSN** or **FileDSN**, it must be defined through the ODBC Data Source Administrator in the Windows Control Panel.</span></span> <span data-ttu-id="c77fc-140">В Microsoft Windows 2000 администратор ODBC находится в разделе Администрирование.</span><span class="sxs-lookup"><span data-stu-id="c77fc-140">In Microsoft Windows 2000, the ODBC Administrator is located under Administrative Tools.</span></span> <span data-ttu-id="c77fc-141">В предыдущих версиях Windows значок администратора ODBC называется **32-разрядным ODBC** или просто **ODBC**.</span><span class="sxs-lookup"><span data-stu-id="c77fc-141">In previous versions of Windows, the ODBC Administrator icon is named **32-bit ODBC** or simply **ODBC**.</span></span>

<span data-ttu-id="c77fc-142">В качестве альтернативы для установки **DSN**можно указать драйвер ODBC (**Driver =**), например "SQL Server;" имя сервера (**Server =**); и имя базы данных (**Database =**).</span><span class="sxs-lookup"><span data-stu-id="c77fc-142">As an alternative to setting a **DSN**, you can specify the ODBC driver (**DRIVER=**), such as "SQL Server;" the server name (**SERVER=**); and the database name (**DATABASE=**).</span></span>

<span data-ttu-id="c77fc-143">Вы также можете указать имя учетной записи пользователя (**UID =**) и пароль для учетной записи пользователя (**PWD =**) в параметрах, ОТносящихся к ODBC, или в стандартных параметрах *пользователя* и *пароля* , определенных в ADO.</span><span class="sxs-lookup"><span data-stu-id="c77fc-143">You can also specify a user account name (**UID=**), and the password for the user account (**PWD=**) in the ODBC-specific parameters or in the standard ADO-defined *user* and *password* parameters.</span></span>

<span data-ttu-id="c77fc-144">Несмотря на то, что определение **DSN** уже определяет *базу данных, можно указать параметр* *базы данных* в дополнение к **имени DSN** для подключения к другой базе данных.</span><span class="sxs-lookup"><span data-stu-id="c77fc-144">Although a **DSN** definition already specifies a database, you can specify *a* *database* parameter in addition to a **DSN** to connect to a different database.</span></span> <span data-ttu-id="c77fc-145">Рекомендуется *всегда включать параметр* *Database* при использовании **DSN**.</span><span class="sxs-lookup"><span data-stu-id="c77fc-145">It is a good idea to always include *the* *database* parameter when you use a **DSN**.</span></span> <span data-ttu-id="c77fc-146">Это обеспечит подключение к соответствующей базе данных в случае, если другой пользователь изменил параметр базы данных по умолчанию после последней проверки определения **DSN** .</span><span class="sxs-lookup"><span data-stu-id="c77fc-146">This will ensure that you connect to the proper database in the event that another user changed the default database parameter since you last checked the **DSN** definition.</span></span>

## <a name="provider-specific-connection-properties"></a><span data-ttu-id="c77fc-147">Свойства подключения, зависящие от поставщика</span><span class="sxs-lookup"><span data-stu-id="c77fc-147">Provider-Specific Connection Properties</span></span>

<span data-ttu-id="c77fc-148">Поставщик OLE DB для ODBC добавляет несколько свойств в коллекцию [свойств](properties-collection-ado.md) объекта **Connection** .</span><span class="sxs-lookup"><span data-stu-id="c77fc-148">The OLE DB provider for ODBC adds several properties to the [Properties](properties-collection-ado.md) collection of the **Connection** object.</span></span> <span data-ttu-id="c77fc-149">В приведенной ниже таблице указаны эти свойства с соответствующим именем свойства OLE DB в круглых скобках.</span><span class="sxs-lookup"><span data-stu-id="c77fc-149">The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c77fc-150">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="c77fc-150">Property Name</span></span></p></th>
<th><p><span data-ttu-id="c77fc-151">Описание</span><span class="sxs-lookup"><span data-stu-id="c77fc-151">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-152">Доступные процедуры</span><span class="sxs-lookup"><span data-stu-id="c77fc-152">Accessible Procedures</span></span><br />
<span data-ttu-id="c77fc-153">(KAGPROP_ACCESSIBLEPROCEDURES)</span><span class="sxs-lookup"><span data-stu-id="c77fc-153">(KAGPROP_ACCESSIBLEPROCEDURES)</span></span></p></td>
<td><p><span data-ttu-id="c77fc-154">Указывает, имеет ли пользователь доступ к хранимым процедурам.</span><span class="sxs-lookup"><span data-stu-id="c77fc-154">Indicates whether the user has access to stored procedures.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-155">Доступные таблицы</span><span class="sxs-lookup"><span data-stu-id="c77fc-155">Accessible Tables</span></span><br />
<span data-ttu-id="c77fc-156">(KAGPROP_ACCESSIBLETABLES)</span><span class="sxs-lookup"><span data-stu-id="c77fc-156">(KAGPROP_ACCESSIBLETABLES)</span></span></p></td>
<td><p><span data-ttu-id="c77fc-157">Указывает, имеет ли пользователь разрешение на выполнение операторов SELECT в таблицах базы данных.</span><span class="sxs-lookup"><span data-stu-id="c77fc-157">Indicates whether the user has permission to execute SELECT statements against the database tables.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-158">Активные операторы</span><span class="sxs-lookup"><span data-stu-id="c77fc-158">Active Statements</span></span><br />
<span data-ttu-id="c77fc-159">(KAGPROP_ACTIVESTATEMENTS)</span><span class="sxs-lookup"><span data-stu-id="c77fc-159">(KAGPROP_ACTIVESTATEMENTS)</span></span></p></td>
<td><p><span data-ttu-id="c77fc-160">Указывает количество дескрипторов, которые драйвер ODBC может поддерживать для подключения.</span><span class="sxs-lookup"><span data-stu-id="c77fc-160">Indicates the number of handles an ODBC driver can support on a connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-161">Имя драйвера</span><span class="sxs-lookup"><span data-stu-id="c77fc-161">Driver Name</span></span><br />
<span data-ttu-id="c77fc-162">(KAGPROP_DRIVERNAME)</span><span class="sxs-lookup"><span data-stu-id="c77fc-162">(KAGPROP_DRIVERNAME)</span></span></p></td>
<td><p><span data-ttu-id="c77fc-163">Указывает имя файла драйвера ODBC.</span><span class="sxs-lookup"><span data-stu-id="c77fc-163">Indicates the file name of the ODBC driver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-164">Версия ODBC драйвера</span><span class="sxs-lookup"><span data-stu-id="c77fc-164">Driver ODBC Version</span></span><br />
<span data-ttu-id="c77fc-165">(KAGPROP_DRIVERODBCVER)</span><span class="sxs-lookup"><span data-stu-id="c77fc-165">(KAGPROP_DRIVERODBCVER)</span></span></p></td>
<td><p><span data-ttu-id="c77fc-166">Указывает версию ODBC, поддерживаемую драйвером.</span><span class="sxs-lookup"><span data-stu-id="c77fc-166">Indicates the version of ODBC that this driver supports.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-167">Использование файла</span><span class="sxs-lookup"><span data-stu-id="c77fc-167">File Usage</span></span><br />
<span data-ttu-id="c77fc-168">(KAGPROP_FILEUSAGE)</span><span class="sxs-lookup"><span data-stu-id="c77fc-168">(KAGPROP_FILEUSAGE)</span></span></p></td>
<td><p><span data-ttu-id="c77fc-169">Указывает, как драйвер обрабатывает файл в источнике данных; как таблица или как каталог.</span><span class="sxs-lookup"><span data-stu-id="c77fc-169">Indicates how the driver treats a file in a data source; as a table or as a catalog.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-170">Как оператор escape</span><span class="sxs-lookup"><span data-stu-id="c77fc-170">Like Escape Clause</span></span><br />
<span data-ttu-id="c77fc-171">(KAGPROP_LIKEESCAPECLAUSE)</span><span class="sxs-lookup"><span data-stu-id="c77fc-171">(KAGPROP_LIKEESCAPECLAUSE)</span></span></p></td>
<td><p><span data-ttu-id="c77fc-172">Указывает, поддерживает ли драйвер определение и использование escape-символа для знака процента (%) и подчеркнуть символ (_) в предикате LIKE предложения WHERE.</span><span class="sxs-lookup"><span data-stu-id="c77fc-172">Indicates whether the driver supports the definition and use of an escape character for the percent character (%) and underline character (_) in the LIKE predicate of a WHERE clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-173">Максимальное число столбцов в группе Group By</span><span class="sxs-lookup"><span data-stu-id="c77fc-173">Max Columns in Group By</span></span><br />
<span data-ttu-id="c77fc-174">(KAGPROP_MAXCOLUMNSINGROUPBY)</span><span class="sxs-lookup"><span data-stu-id="c77fc-174">(KAGPROP_MAXCOLUMNSINGROUPBY)</span></span></p></td>
<td><p><span data-ttu-id="c77fc-175">Указывает максимальное количество столбцов, которое может быть указано в предложении GROUP BY оператора SELECT.</span><span class="sxs-lookup"><span data-stu-id="c77fc-175">Indicates the maximum number of columns that can be listed in the GROUP BY clause of a SELECT statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-176">Максимальное число столбцов в индексе</span><span class="sxs-lookup"><span data-stu-id="c77fc-176">Max Columns in Index</span></span><br />
<span data-ttu-id="c77fc-177">(KAGPROP_MAXCOLUMNSININDEX)</span><span class="sxs-lookup"><span data-stu-id="c77fc-177">(KAGPROP_MAXCOLUMNSININDEX)</span></span></p></td>
<td><p><span data-ttu-id="c77fc-178">Указывает максимальное число столбцов, которые можно включить в индекс.</span><span class="sxs-lookup"><span data-stu-id="c77fc-178">Indicates the maximum number of columns that can be included in an index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-179">Максимальное число столбцов в упорядочении по</span><span class="sxs-lookup"><span data-stu-id="c77fc-179">Max Columns in Order By</span></span><br />
<span data-ttu-id="c77fc-180">(KAGPROP_MAXCOLUMNSINORDERBY)</span><span class="sxs-lookup"><span data-stu-id="c77fc-180">(KAGPROP_MAXCOLUMNSINORDERBY)</span></span></p></td>
<td><p><span data-ttu-id="c77fc-181">Указывает максимальное количество столбцов, которое может быть указано в предложении ORDER BY оператора SELECT.</span><span class="sxs-lookup"><span data-stu-id="c77fc-181">Indicates the maximum number of columns that can be listed in the ORDER BY clause of a SELECT statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-182">Максимальное число столбцов в SELECT</span><span class="sxs-lookup"><span data-stu-id="c77fc-182">Max Columns in Select</span></span><br />
<span data-ttu-id="c77fc-183">(KAGPROP_MAXCOLUMNSINSELECT)</span><span class="sxs-lookup"><span data-stu-id="c77fc-183">(KAGPROP_MAXCOLUMNSINSELECT)</span></span></p></td>
<td><p><span data-ttu-id="c77fc-184">Указывает максимальное количество столбцов, которое может быть указано в части SELECT оператора SELECT.</span><span class="sxs-lookup"><span data-stu-id="c77fc-184">Indicates the maximum number of columns that can be listed in the SELECT portion of a SELECT statement.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-185">Максимальное число столбцов в таблице</span><span class="sxs-lookup"><span data-stu-id="c77fc-185">Max Columns in Table</span></span><br />
<span data-ttu-id="c77fc-186">(KAGPROP_MAXCOLUMNSINTABLE)</span><span class="sxs-lookup"><span data-stu-id="c77fc-186">(KAGPROP_MAXCOLUMNSINTABLE)</span></span></p></td>
<td><p><span data-ttu-id="c77fc-187">Указывает максимальное допустимое количество столбцов в таблице.</span><span class="sxs-lookup"><span data-stu-id="c77fc-187">Indicates the maximum number of columns allowed in a table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-188">Числовые функции</span><span class="sxs-lookup"><span data-stu-id="c77fc-188">Numeric Functions</span></span><br />
<span data-ttu-id="c77fc-189">(KAGPROP_NUMERICFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="c77fc-189">(KAGPROP_NUMERICFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="c77fc-190">Указывает, какие числовые функции поддерживаются драйвером ODBC.</span><span class="sxs-lookup"><span data-stu-id="c77fc-190">Indicates which numeric functions are supported by the ODBC driver.</span></span> <span data-ttu-id="c77fc-191">Список имен функций и соответствующих значений, используемых в этой битовой маске, приведен в разделе приложение E: скалярные функции в документации ODBC.</span><span class="sxs-lookup"><span data-stu-id="c77fc-191">For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-192">Возможности внешнего соединения</span><span class="sxs-lookup"><span data-stu-id="c77fc-192">Outer Join Capabilities</span></span><br />
<span data-ttu-id="c77fc-193">(KAGPROP_OJCAPABILITY)</span><span class="sxs-lookup"><span data-stu-id="c77fc-193">(KAGPROP_OJCAPABILITY)</span></span></p></td>
<td><p><span data-ttu-id="c77fc-194">Указывает типы внешних ОБЪЕДИНЕНий, поддерживаемые поставщиком.</span><span class="sxs-lookup"><span data-stu-id="c77fc-194">Indicates the types of OUTER JOINs supported by the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-195">Внешние соединения</span><span class="sxs-lookup"><span data-stu-id="c77fc-195">Outer Joins</span></span><br />
<span data-ttu-id="c77fc-196">(KAGPROP_OUTERJOINS)</span><span class="sxs-lookup"><span data-stu-id="c77fc-196">(KAGPROP_OUTERJOINS)</span></span></p></td>
<td><p><span data-ttu-id="c77fc-197">Указывает, поддерживает ли поставщик внешние соединения.</span><span class="sxs-lookup"><span data-stu-id="c77fc-197">Indicates whether the provider supports OUTER JOINs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-198">Специальные символы</span><span class="sxs-lookup"><span data-stu-id="c77fc-198">Special Characters</span></span><br />
<span data-ttu-id="c77fc-199">(KAGPROP_SPECIALCHARACTERS)</span><span class="sxs-lookup"><span data-stu-id="c77fc-199">(KAGPROP_SPECIALCHARACTERS)</span></span></p></td>
<td><p><span data-ttu-id="c77fc-200">Указывает, какие символы имеют особое значение для драйвера ODBC.</span><span class="sxs-lookup"><span data-stu-id="c77fc-200">Indicates which characters have special meaning for the ODBC driver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-201">Хранимые процедуры</span><span class="sxs-lookup"><span data-stu-id="c77fc-201">Stored Procedures</span></span><br />
<span data-ttu-id="c77fc-202">(KAGPROP_PROCEDURES)</span><span class="sxs-lookup"><span data-stu-id="c77fc-202">(KAGPROP_PROCEDURES)</span></span></p></td>
<td><p><span data-ttu-id="c77fc-203">Указывает, доступны ли хранимые процедуры для использования с данным драйвером ODBC.</span><span class="sxs-lookup"><span data-stu-id="c77fc-203">Indicates whether stored procedures are available for use with this ODBC driver.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-204">Строковые функции</span><span class="sxs-lookup"><span data-stu-id="c77fc-204">String Functions</span></span><br />
<span data-ttu-id="c77fc-205">(KAGPROP_STRINGFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="c77fc-205">(KAGPROP_STRINGFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="c77fc-206">Указывает, какие строковые функции поддерживаются драйвером ODBC.</span><span class="sxs-lookup"><span data-stu-id="c77fc-206">Indicates which string functions are supported by the ODBC driver.</span></span> <span data-ttu-id="c77fc-207">Список имен функций и соответствующих значений, используемых в этой битовой маске, приведен в разделе приложение E: скалярные функции в документации ODBC.</span><span class="sxs-lookup"><span data-stu-id="c77fc-207">For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-208">Системные функции</span><span class="sxs-lookup"><span data-stu-id="c77fc-208">System Functions</span></span><br />
<span data-ttu-id="c77fc-209">(KAGPROP_SYSTEMFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="c77fc-209">(KAGPROP_SYSTEMFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="c77fc-210">Указывает, какие системные функции поддерживаются драйвером ODBC.</span><span class="sxs-lookup"><span data-stu-id="c77fc-210">Indicates which system functions are supported by the ODBC driver.</span></span> <span data-ttu-id="c77fc-211">Список имен функций и соответствующих значений, используемых в этой битовой маске, приведен в разделе приложение E: скалярные функции в документации ODBC.</span><span class="sxs-lookup"><span data-stu-id="c77fc-211">For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-212">Функции времени и даты</span><span class="sxs-lookup"><span data-stu-id="c77fc-212">Time/Date Functions</span></span><br />
<span data-ttu-id="c77fc-213">(KAGPROP_TIMEDATEFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="c77fc-213">(KAGPROP_TIMEDATEFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="c77fc-214">Указывает, какие функции времени и даты поддерживаются драйвером ODBC.</span><span class="sxs-lookup"><span data-stu-id="c77fc-214">Indicates which time and date functions are supported by the ODBC driver.</span></span> <span data-ttu-id="c77fc-215">Список имен функций и соответствующих значений, используемых в этой битовой маске, приведен в разделе приложение E: скалярные функции в документации ODBC.</span><span class="sxs-lookup"><span data-stu-id="c77fc-215">For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-216">Поддержка грамматики SQL</span><span class="sxs-lookup"><span data-stu-id="c77fc-216">SQL Grammar Support</span></span><br />
<span data-ttu-id="c77fc-217">(KAGPROP_ODBCSQLCONFORMANCE)</span><span class="sxs-lookup"><span data-stu-id="c77fc-217">(KAGPROP_ODBCSQLCONFORMANCE)</span></span></p></td>
<td><p><span data-ttu-id="c77fc-218">Указывает грамматику SQL, поддерживаемую драйвером ODBC.</span><span class="sxs-lookup"><span data-stu-id="c77fc-218">Indicates the SQL grammar that the ODBC driver supports.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-recordset-and-command-properties"></a><span data-ttu-id="c77fc-219">Специфические для поставщика наборы записей и свойства команд</span><span class="sxs-lookup"><span data-stu-id="c77fc-219">Provider-Specific Recordset and Command Properties</span></span>

<span data-ttu-id="c77fc-220">Поставщик OLE DB для ODBC добавляет несколько свойств в коллекцию **свойств** объекта **Recordset** и **командных** объектов.</span><span class="sxs-lookup"><span data-stu-id="c77fc-220">The OLE DB provider for ODBC adds several properties to the **Properties** collection of the **Recordset** and **Command** objects.</span></span> <span data-ttu-id="c77fc-221">В приведенной ниже таблице указаны эти свойства с соответствующим именем свойства OLE DB в круглых скобках.</span><span class="sxs-lookup"><span data-stu-id="c77fc-221">The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c77fc-222">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="c77fc-222">Property Name</span></span></p></th>
<th><p><span data-ttu-id="c77fc-223">Описание</span><span class="sxs-lookup"><span data-stu-id="c77fc-223">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-224">Обновления, операции удаления и вставки на основе запросов</span><span class="sxs-lookup"><span data-stu-id="c77fc-224">Query Based Updates/Deletes/Inserts</span></span><br />
<span data-ttu-id="c77fc-225">(KAGPROP_QUERYBASEDUPDATES)</span><span class="sxs-lookup"><span data-stu-id="c77fc-225">(KAGPROP_QUERYBASEDUPDATES)</span></span></p></td>
<td><p><span data-ttu-id="c77fc-226">Указывает, можно ли выполнять операции обновления, удаления и вставки с помощью запросов SQL.</span><span class="sxs-lookup"><span data-stu-id="c77fc-226">Indicates whether updates, deletions, and insertions can be performed using SQL queries.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-227">Тип параллелизма ODBC</span><span class="sxs-lookup"><span data-stu-id="c77fc-227">ODBC Concurrency Type</span></span><br />
<span data-ttu-id="c77fc-228">(KAGPROP_CONCURRENCY)</span><span class="sxs-lookup"><span data-stu-id="c77fc-228">(KAGPROP_CONCURRENCY)</span></span></p></td>
<td><p><span data-ttu-id="c77fc-229">Указывает метод, используемый для сокращения возможных проблем, вызванных двумя пользователями, пытающимися одновременно получить доступ к одним и тем же данным из источника данных.</span><span class="sxs-lookup"><span data-stu-id="c77fc-229">Indicates the method used to reduce potential problems caused by two users attempting to access the same data from the data source simultaneously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-230">Доступность BLOB-объектов для однонаправленного курсора</span><span class="sxs-lookup"><span data-stu-id="c77fc-230">BLOB accessibility on Forward-Only cursor</span></span><br />
<span data-ttu-id="c77fc-231">(KAGPROP_BLOBSONFOCURSOR)</span><span class="sxs-lookup"><span data-stu-id="c77fc-231">(KAGPROP_BLOBSONFOCURSOR)</span></span></p></td>
<td><p><span data-ttu-id="c77fc-232">Указывает, можно ли получить доступ к <strong>полям</strong> BLOB при использовании однонаправленного курсора.</span><span class="sxs-lookup"><span data-stu-id="c77fc-232">Indicates whether BLOB <strong>Fields</strong> can be accessed when using a forward-only cursor.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-233">Включает SQL_FLOAT, SQL_DOUBLE и SQL_REAL в КБУ, где предложения WHERE</span><span class="sxs-lookup"><span data-stu-id="c77fc-233">Include SQL_FLOAT, SQL_DOUBLE, and SQL_REAL in QBU WHERE clauses</span></span><br />
<span data-ttu-id="c77fc-234">(KAGPROP_INCLUDENONEXACT)</span><span class="sxs-lookup"><span data-stu-id="c77fc-234">(KAGPROP_INCLUDENONEXACT)</span></span></p></td>
<td><p><span data-ttu-id="c77fc-235">Указывает, могут ли значения SQL_FLOAT, SQL_DOUBLE и SQL_REAL включаться в предложение WHERE КБУ.</span><span class="sxs-lookup"><span data-stu-id="c77fc-235">Indicates whether SQL_FLOAT, SQL_DOUBLE, and SQL_REAL values can be included in a QBU WHERE clause.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-236">Положение в последней строке после вставки</span><span class="sxs-lookup"><span data-stu-id="c77fc-236">Position on the last row after insert</span></span><br />
<span data-ttu-id="c77fc-237">(KAGPROP_POSITIONONNEWROW)</span><span class="sxs-lookup"><span data-stu-id="c77fc-237">(KAGPROP_POSITIONONNEWROW)</span></span></p></td>
<td><p><span data-ttu-id="c77fc-238">Указывает, что после вставки новой записи в таблицу текущая строка будет получена из последней строки таблицы.</span><span class="sxs-lookup"><span data-stu-id="c77fc-238">Indicates that after a new record has been inserted in a table, the last row in the table will be come the current row.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-239">ировсетчанжеекстинфо</span><span class="sxs-lookup"><span data-stu-id="c77fc-239">IRowsetChangeExtInfo</span></span><br />
<span data-ttu-id="c77fc-240">(KAGPROP_IROWSETCHANGEEXTINFO)</span><span class="sxs-lookup"><span data-stu-id="c77fc-240">(KAGPROP_IROWSETCHANGEEXTINFO)</span></span></p></td>
<td><p><span data-ttu-id="c77fc-241">Указывает, предоставляет ли интерфейс <strong>ировсетчанже</strong> расширенную поддержку информации.</span><span class="sxs-lookup"><span data-stu-id="c77fc-241">Indicates whether the <strong>IRowsetChange</strong> interface provides extended information support.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-242">Тип курсора ODBC</span><span class="sxs-lookup"><span data-stu-id="c77fc-242">ODBC Cursor Type</span></span><br />
<span data-ttu-id="c77fc-243">(KAGPROP_CURSOR)</span><span class="sxs-lookup"><span data-stu-id="c77fc-243">(KAGPROP_CURSOR)</span></span></p></td>
<td><p><span data-ttu-id="c77fc-244">Указывает тип курсора, используемого в объекте <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="c77fc-244">Indicates the type of cursor used by the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-245">Создание набора строк, который может быть маршалирован</span><span class="sxs-lookup"><span data-stu-id="c77fc-245">Generate a Rowset that can be marshaled</span></span><br />
<span data-ttu-id="c77fc-246">(KAGPROP_MARSHALLABLE)</span><span class="sxs-lookup"><span data-stu-id="c77fc-246">(KAGPROP_MARSHALLABLE)</span></span></p></td>
<td><p><span data-ttu-id="c77fc-247">Указывает, что драйвер ODBC создает объект Recordset, который может быть маршалирован</span><span class="sxs-lookup"><span data-stu-id="c77fc-247">Indicates that the ODBC driver generates a recordset that can be marshaled</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-text"></a><span data-ttu-id="c77fc-248">Текст команды</span><span class="sxs-lookup"><span data-stu-id="c77fc-248">Command Text</span></span>

<span data-ttu-id="c77fc-249">Способ использования объекта [Command](command-object-ado.md) во многом зависит от источника данных, а также от того, какой тип запроса или оператора команды будет принимать.</span><span class="sxs-lookup"><span data-stu-id="c77fc-249">How you use the [Command](command-object-ado.md) object largely depends on the data source, and what type of query or command statement it will accept.</span></span>

<span data-ttu-id="c77fc-250">ODBC предоставляет специальный синтаксис для вызова хранимых процедур.</span><span class="sxs-lookup"><span data-stu-id="c77fc-250">ODBC provides a specific syntax for calling stored procedures.</span></span> <span data-ttu-id="c77fc-251">Для свойства [CommandText](commandtext-property-ado.md) объекта **Command** , аргумент *CommandText* для метода **EXECUTE** объекта [Connection](connection-object-ado.md) или аргумента *Source* для метода **Open** объекта [Recordset](recordset-object-ado.md) , передается в строку с помощью следующего синтаксиса:</span><span class="sxs-lookup"><span data-stu-id="c77fc-251">For the [CommandText](commandtext-property-ado.md) property of a **Command** object, the *CommandText* argument to the **Execute** method on a [Connection](connection-object-ado.md) object, or the *Source* argument to the **Open** method on a [Recordset](recordset-object-ado.md) object, passes in a string with this syntax:</span></span>

`"{ [ ? = ] call procedure [ ( ? [, ? [ ,  ]] ) ] }"`

<span data-ttu-id="c77fc-252">Каждый **из** них</span><span class="sxs-lookup"><span data-stu-id="c77fc-252">Each **?**</span></span> <span data-ttu-id="c77fc-253">ссылается на объект в коллекции [Parameters](parameters-collection-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="c77fc-253">references an object in the [Parameters](parameters-collection-ado.md) collection.</span></span> <span data-ttu-id="c77fc-254">Первый **?**</span><span class="sxs-lookup"><span data-stu-id="c77fc-254">The first **?**</span></span> <span data-ttu-id="c77fc-255">**Параметры**References (0), следующие **?**</span><span class="sxs-lookup"><span data-stu-id="c77fc-255">references **Parameters**(0), the next **?**</span></span> <span data-ttu-id="c77fc-256">ссылки на **Параметры**(1) и т. д.</span><span class="sxs-lookup"><span data-stu-id="c77fc-256">references **Parameters**(1), and so on.</span></span>

<span data-ttu-id="c77fc-257">Ссылки на параметры являются необязательными и зависят от структуры хранимой процедуры.</span><span class="sxs-lookup"><span data-stu-id="c77fc-257">The parameter references are optional and depend on the structure of the stored procedure.</span></span> <span data-ttu-id="c77fc-258">Если вы хотите вызвать хранимую процедуру, которая не определяет параметры, строка будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c77fc-258">If you want to call a stored procedure that defines no parameters, your string would look like this:</span></span>

`"{ call procedure }"`

<span data-ttu-id="c77fc-259">Если у вас есть два параметра запроса, строка будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c77fc-259">If you have two query parameters, your string would look like this:</span></span>

`"{ call procedure ( ?, ? ) }"`

<span data-ttu-id="c77fc-260">Если хранимая процедура будет возвращать значение, возвращаемое значение будет считаться другим параметром.</span><span class="sxs-lookup"><span data-stu-id="c77fc-260">If the stored procedure will return a value, the return value is treated as another parameter.</span></span> <span data-ttu-id="c77fc-261">Если у вас нет параметров запроса, но у вас есть возвращаемое значение, строка будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c77fc-261">If you have no query parameters but you do have a return value, your string would look like this:</span></span>

`"{ ? = call procedure }"`

<span data-ttu-id="c77fc-262">Наконец, если у вас есть возвращаемое значение и два параметра запроса, строка будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c77fc-262">Finally, if you have a return value and two query parameters, your string would look like this:</span></span>

`"{ ? = call procedure ( ?, ? ) }"`

## <a name="recordset-behavior"></a><span data-ttu-id="c77fc-263">Поведение набора записей</span><span class="sxs-lookup"><span data-stu-id="c77fc-263">Recordset Behavior</span></span>

<span data-ttu-id="c77fc-264">В следующих таблицах перечислены стандартные методы и свойства ADO, доступные для объекта **Recordset** , открытого с помощью этого поставщика.</span><span class="sxs-lookup"><span data-stu-id="c77fc-264">The following tables list the standard ADO methods and properties available on a **Recordset** object opened with this provider.</span></span>

<span data-ttu-id="c77fc-265">Для получения более подробных сведений о поведении **набора записей** для конфигурации поставщика [запустите метод](supports-method-ado.md) Supports и перечислите коллекцию **свойств** объекта **Recordset** , чтобы определить, присутствуют ли динамические свойства, зависящие от поставщика.</span><span class="sxs-lookup"><span data-stu-id="c77fc-265">For more detailed information about **Recordset** behavior for your provider configuration, run the [Supports](supports-method-ado.md) method and enumerate the **Properties** collection of the **Recordset** to determine whether provider-specific dynamic properties are present.</span></span>

<span data-ttu-id="c77fc-266">Доступность стандартных свойств **записей** ADO:</span><span class="sxs-lookup"><span data-stu-id="c77fc-266">Availability of standard ADO **Recordset** properties:</span></span>

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
<th><p><span data-ttu-id="c77fc-267">Свойство</span><span class="sxs-lookup"><span data-stu-id="c77fc-267">Property</span></span></p></th>
<th><p><span data-ttu-id="c77fc-268">форвардонли</span><span class="sxs-lookup"><span data-stu-id="c77fc-268">ForwardOnly</span></span></p></th>
<th><p><span data-ttu-id="c77fc-269">Динамическая группа</span><span class="sxs-lookup"><span data-stu-id="c77fc-269">Dynamic</span></span></p></th>
<th><p><span data-ttu-id="c77fc-270">Keyset</span><span class="sxs-lookup"><span data-stu-id="c77fc-270">Keyset</span></span></p></th>
<th><p><span data-ttu-id="c77fc-271">Static</span><span class="sxs-lookup"><span data-stu-id="c77fc-271">Static</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-272"><a href="absolutepage-property-ado.md">AbsolutePage</a></span><span class="sxs-lookup"><span data-stu-id="c77fc-272"><a href="absolutepage-property-ado.md">AbsolutePage</a></span></span></p></td>
<td><p><span data-ttu-id="c77fc-273">недоступно</span><span class="sxs-lookup"><span data-stu-id="c77fc-273">not available</span></span></p></td>
<td><p><span data-ttu-id="c77fc-274">недоступно</span><span class="sxs-lookup"><span data-stu-id="c77fc-274">not available</span></span></p></td>
<td><p><span data-ttu-id="c77fc-275">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c77fc-275">read/write</span></span></p></td>
<td><p><span data-ttu-id="c77fc-276">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c77fc-276">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-277"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span><span class="sxs-lookup"><span data-stu-id="c77fc-277"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span></span></p></td>
<td><p><span data-ttu-id="c77fc-278">недоступно</span><span class="sxs-lookup"><span data-stu-id="c77fc-278">not available</span></span></p></td>
<td><p><span data-ttu-id="c77fc-279">недоступно</span><span class="sxs-lookup"><span data-stu-id="c77fc-279">not available</span></span></p></td>
<td><p><span data-ttu-id="c77fc-280">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c77fc-280">read/write</span></span></p></td>
<td><p><span data-ttu-id="c77fc-281">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c77fc-281">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-282"><a href="activeconnection-property-ado.md">ActiveConnection</a></span><span class="sxs-lookup"><span data-stu-id="c77fc-282"><a href="activeconnection-property-ado.md">ActiveConnection</a></span></span></p></td>
<td><p><span data-ttu-id="c77fc-283">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c77fc-283">read/write</span></span></p></td>
<td><p><span data-ttu-id="c77fc-284">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c77fc-284">read/write</span></span></p></td>
<td><p><span data-ttu-id="c77fc-285">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c77fc-285">read/write</span></span></p></td>
<td><p><span data-ttu-id="c77fc-286">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c77fc-286">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-287"><a href="bof-eof-properties-ado.md">BOF</a></span><span class="sxs-lookup"><span data-stu-id="c77fc-287"><a href="bof-eof-properties-ado.md">BOF</a></span></span></p></td>
<td><p><span data-ttu-id="c77fc-288">только для чтения</span><span class="sxs-lookup"><span data-stu-id="c77fc-288">read-only</span></span></p></td>
<td><p><span data-ttu-id="c77fc-289">только для чтения</span><span class="sxs-lookup"><span data-stu-id="c77fc-289">read-only</span></span></p></td>
<td><p><span data-ttu-id="c77fc-290">только для чтения</span><span class="sxs-lookup"><span data-stu-id="c77fc-290">read-only</span></span></p></td>
<td><p><span data-ttu-id="c77fc-291">только для чтения</span><span class="sxs-lookup"><span data-stu-id="c77fc-291">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-292"><a href="bookmark-property-ado.md">Bookmark</a></span><span class="sxs-lookup"><span data-stu-id="c77fc-292"><a href="bookmark-property-ado.md">Bookmark</a></span></span></p></td>
<td><p><span data-ttu-id="c77fc-293">недоступно</span><span class="sxs-lookup"><span data-stu-id="c77fc-293">not available</span></span></p></td>
<td><p><span data-ttu-id="c77fc-294">недоступно</span><span class="sxs-lookup"><span data-stu-id="c77fc-294">not available</span></span></p></td>
<td><p><span data-ttu-id="c77fc-295">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c77fc-295">read/write</span></span></p></td>
<td><p><span data-ttu-id="c77fc-296">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c77fc-296">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-297"><a href="cachesize-property-ado.md">CacheSize</a></span><span class="sxs-lookup"><span data-stu-id="c77fc-297"><a href="cachesize-property-ado.md">CacheSize</a></span></span></p></td>
<td><p><span data-ttu-id="c77fc-298">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c77fc-298">read/write</span></span></p></td>
<td><p><span data-ttu-id="c77fc-299">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c77fc-299">read/write</span></span></p></td>
<td><p><span data-ttu-id="c77fc-300">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c77fc-300">read/write</span></span></p></td>
<td><p><span data-ttu-id="c77fc-301">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c77fc-301">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-302"><a href="cursorlocation-property-ado.md">CursorLocation</a></span><span class="sxs-lookup"><span data-stu-id="c77fc-302"><a href="cursorlocation-property-ado.md">CursorLocation</a></span></span></p></td>
<td><p><span data-ttu-id="c77fc-303">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c77fc-303">read/write</span></span></p></td>
<td><p><span data-ttu-id="c77fc-304">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c77fc-304">read/write</span></span></p></td>
<td><p><span data-ttu-id="c77fc-305">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c77fc-305">read/write</span></span></p></td>
<td><p><span data-ttu-id="c77fc-306">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c77fc-306">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-307"><a href="cursortype-property-ado.md">CursorType</a></span><span class="sxs-lookup"><span data-stu-id="c77fc-307"><a href="cursortype-property-ado.md">CursorType</a></span></span></p></td>
<td><p><span data-ttu-id="c77fc-308">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c77fc-308">read/write</span></span></p></td>
<td><p><span data-ttu-id="c77fc-309">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c77fc-309">read/write</span></span></p></td>
<td><p><span data-ttu-id="c77fc-310">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c77fc-310">read/write</span></span></p></td>
<td><p><span data-ttu-id="c77fc-311">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c77fc-311">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-312"><a href="editmode-property-ado.md">EditMode</a></span><span class="sxs-lookup"><span data-stu-id="c77fc-312"><a href="editmode-property-ado.md">EditMode</a></span></span></p></td>
<td><p><span data-ttu-id="c77fc-313">только для чтения</span><span class="sxs-lookup"><span data-stu-id="c77fc-313">read-only</span></span></p></td>
<td><p><span data-ttu-id="c77fc-314">только для чтения</span><span class="sxs-lookup"><span data-stu-id="c77fc-314">read-only</span></span></p></td>
<td><p><span data-ttu-id="c77fc-315">только для чтения</span><span class="sxs-lookup"><span data-stu-id="c77fc-315">read-only</span></span></p></td>
<td><p><span data-ttu-id="c77fc-316">только для чтения</span><span class="sxs-lookup"><span data-stu-id="c77fc-316">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-317"><a href="filter-property-ado.md">Filter</a></span><span class="sxs-lookup"><span data-stu-id="c77fc-317"><a href="filter-property-ado.md">Filter</a></span></span></p></td>
<td><p><span data-ttu-id="c77fc-318">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c77fc-318">read/write</span></span></p></td>
<td><p><span data-ttu-id="c77fc-319">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c77fc-319">read/write</span></span></p></td>
<td><p><span data-ttu-id="c77fc-320">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c77fc-320">read/write</span></span></p></td>
<td><p><span data-ttu-id="c77fc-321">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c77fc-321">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-322"><a href="locktype-property-ado.md">LockType</a></span><span class="sxs-lookup"><span data-stu-id="c77fc-322"><a href="locktype-property-ado.md">LockType</a></span></span></p></td>
<td><p><span data-ttu-id="c77fc-323">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c77fc-323">read/write</span></span></p></td>
<td><p><span data-ttu-id="c77fc-324">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c77fc-324">read/write</span></span></p></td>
<td><p><span data-ttu-id="c77fc-325">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c77fc-325">read/write</span></span></p></td>
<td><p><span data-ttu-id="c77fc-326">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c77fc-326">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-327"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span><span class="sxs-lookup"><span data-stu-id="c77fc-327"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span></span></p></td>
<td><p><span data-ttu-id="c77fc-328">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c77fc-328">read/write</span></span></p></td>
<td><p><span data-ttu-id="c77fc-329">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c77fc-329">read/write</span></span></p></td>
<td><p><span data-ttu-id="c77fc-330">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c77fc-330">read/write</span></span></p></td>
<td><p><span data-ttu-id="c77fc-331">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c77fc-331">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-332"><a href="maxrecords-property-ado.md">MaxRecords</a></span><span class="sxs-lookup"><span data-stu-id="c77fc-332"><a href="maxrecords-property-ado.md">MaxRecords</a></span></span></p></td>
<td><p><span data-ttu-id="c77fc-333">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c77fc-333">read/write</span></span></p></td>
<td><p><span data-ttu-id="c77fc-334">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c77fc-334">read/write</span></span></p></td>
<td><p><span data-ttu-id="c77fc-335">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c77fc-335">read/write</span></span></p></td>
<td><p><span data-ttu-id="c77fc-336">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c77fc-336">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-337"><a href="pagecount-property-ado.md">PageCount</a></span><span class="sxs-lookup"><span data-stu-id="c77fc-337"><a href="pagecount-property-ado.md">PageCount</a></span></span></p></td>
<td><p><span data-ttu-id="c77fc-338">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c77fc-338">read/write</span></span></p></td>
<td><p><span data-ttu-id="c77fc-339">недоступен</span><span class="sxs-lookup"><span data-stu-id="c77fc-339">not available</span></span></p></td>
<td><p><span data-ttu-id="c77fc-340">только для чтения</span><span class="sxs-lookup"><span data-stu-id="c77fc-340">read-only</span></span></p></td>
<td><p><span data-ttu-id="c77fc-341">только для чтения</span><span class="sxs-lookup"><span data-stu-id="c77fc-341">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-342"><a href="pagesize-property-ado.md">PageSize</a></span><span class="sxs-lookup"><span data-stu-id="c77fc-342"><a href="pagesize-property-ado.md">PageSize</a></span></span></p></td>
<td><p><span data-ttu-id="c77fc-343">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c77fc-343">read/write</span></span></p></td>
<td><p><span data-ttu-id="c77fc-344">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c77fc-344">read/write</span></span></p></td>
<td><p><span data-ttu-id="c77fc-345">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c77fc-345">read/write</span></span></p></td>
<td><p><span data-ttu-id="c77fc-346">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c77fc-346">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-347"><a href="recordcount-property-ado.md">RecordCount</a></span><span class="sxs-lookup"><span data-stu-id="c77fc-347"><a href="recordcount-property-ado.md">RecordCount</a></span></span></p></td>
<td><p><span data-ttu-id="c77fc-348">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c77fc-348">read/write</span></span></p></td>
<td><p><span data-ttu-id="c77fc-349">недоступен</span><span class="sxs-lookup"><span data-stu-id="c77fc-349">not available</span></span></p></td>
<td><p><span data-ttu-id="c77fc-350">только для чтения</span><span class="sxs-lookup"><span data-stu-id="c77fc-350">read-only</span></span></p></td>
<td><p><span data-ttu-id="c77fc-351">только для чтения</span><span class="sxs-lookup"><span data-stu-id="c77fc-351">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-352"><a href="source-property-ado-recordset.md">Source</a></span><span class="sxs-lookup"><span data-stu-id="c77fc-352"><a href="source-property-ado-recordset.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="c77fc-353">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c77fc-353">read/write</span></span></p></td>
<td><p><span data-ttu-id="c77fc-354">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c77fc-354">read/write</span></span></p></td>
<td><p><span data-ttu-id="c77fc-355">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c77fc-355">read/write</span></span></p></td>
<td><p><span data-ttu-id="c77fc-356">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c77fc-356">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-357"><a href="state-property-ado.md">State</a></span><span class="sxs-lookup"><span data-stu-id="c77fc-357"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="c77fc-358">только для чтения</span><span class="sxs-lookup"><span data-stu-id="c77fc-358">read-only</span></span></p></td>
<td><p><span data-ttu-id="c77fc-359">только для чтения</span><span class="sxs-lookup"><span data-stu-id="c77fc-359">read-only</span></span></p></td>
<td><p><span data-ttu-id="c77fc-360">только для чтения</span><span class="sxs-lookup"><span data-stu-id="c77fc-360">read-only</span></span></p></td>
<td><p><span data-ttu-id="c77fc-361">только для чтения</span><span class="sxs-lookup"><span data-stu-id="c77fc-361">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-362"><a href="status-property-ado-recordset.md">Состояние</a></span><span class="sxs-lookup"><span data-stu-id="c77fc-362"><a href="status-property-ado-recordset.md">Status</a></span></span></p></td>
<td><p><span data-ttu-id="c77fc-363">только для чтения</span><span class="sxs-lookup"><span data-stu-id="c77fc-363">read-only</span></span></p></td>
<td><p><span data-ttu-id="c77fc-364">только для чтения</span><span class="sxs-lookup"><span data-stu-id="c77fc-364">read-only</span></span></p></td>
<td><p><span data-ttu-id="c77fc-365">только для чтения</span><span class="sxs-lookup"><span data-stu-id="c77fc-365">read-only</span></span></p></td>
<td><p><span data-ttu-id="c77fc-366">только для чтения</span><span class="sxs-lookup"><span data-stu-id="c77fc-366">read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c77fc-367">Свойства [AbsolutePosition](absoluteposition-property-ado.md) и [AbsolutePage](absolutepage-property-ado.md) доступны только для записи при использовании ADO с поставщиком Microsoft OLE DB для ODBC версии 1,0.</span><span class="sxs-lookup"><span data-stu-id="c77fc-367">The [AbsolutePosition](absoluteposition-property-ado.md) and [AbsolutePage](absolutepage-property-ado.md) properties are write-only when ADO is used with version 1.0 of the Microsoft OLE DB Provider for ODBC.</span></span>

<span data-ttu-id="c77fc-368">Доступность стандартных методов **набора записей** ADO:</span><span class="sxs-lookup"><span data-stu-id="c77fc-368">Availability of standard ADO **Recordset** methods:</span></span>

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
<th><p><span data-ttu-id="c77fc-369">Method</span><span class="sxs-lookup"><span data-stu-id="c77fc-369">Method</span></span></p></th>
<th><p><span data-ttu-id="c77fc-370">форвардонли</span><span class="sxs-lookup"><span data-stu-id="c77fc-370">ForwardOnly</span></span></p></th>
<th><p><span data-ttu-id="c77fc-371">Динамическая группа</span><span class="sxs-lookup"><span data-stu-id="c77fc-371">Dynamic</span></span></p></th>
<th><p><span data-ttu-id="c77fc-372">Keyset</span><span class="sxs-lookup"><span data-stu-id="c77fc-372">Keyset</span></span></p></th>
<th><p><span data-ttu-id="c77fc-373">Static</span><span class="sxs-lookup"><span data-stu-id="c77fc-373">Static</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-374"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="c77fc-374"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="c77fc-375">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-375">Yes</span></span></p></td>
<td><p><span data-ttu-id="c77fc-376">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-376">Yes</span></span></p></td>
<td><p><span data-ttu-id="c77fc-377">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-377">Yes</span></span></p></td>
<td><p><span data-ttu-id="c77fc-378">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-378">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-379"><a href="cancel-method-ado.md">Отмена</a></span><span class="sxs-lookup"><span data-stu-id="c77fc-379"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="c77fc-380">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-380">Yes</span></span></p></td>
<td><p><span data-ttu-id="c77fc-381">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-381">Yes</span></span></p></td>
<td><p><span data-ttu-id="c77fc-382">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-382">Yes</span></span></p></td>
<td><p><span data-ttu-id="c77fc-383">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-383">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-384"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="c77fc-384"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="c77fc-385">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-385">Yes</span></span></p></td>
<td><p><span data-ttu-id="c77fc-386">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-386">Yes</span></span></p></td>
<td><p><span data-ttu-id="c77fc-387">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-387">Yes</span></span></p></td>
<td><p><span data-ttu-id="c77fc-388">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-388">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-389"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="c77fc-389"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="c77fc-390">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-390">Yes</span></span></p></td>
<td><p><span data-ttu-id="c77fc-391">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-391">Yes</span></span></p></td>
<td><p><span data-ttu-id="c77fc-392">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-392">Yes</span></span></p></td>
<td><p><span data-ttu-id="c77fc-393">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-393">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-394"><a href="clone-method-ado.md">Clone</a></span><span class="sxs-lookup"><span data-stu-id="c77fc-394"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="c77fc-395">Нет</span><span class="sxs-lookup"><span data-stu-id="c77fc-395">No</span></span></p></td>
<td><p><span data-ttu-id="c77fc-396">Нет</span><span class="sxs-lookup"><span data-stu-id="c77fc-396">No</span></span></p></td>
<td><p><span data-ttu-id="c77fc-397">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-397">Yes</span></span></p></td>
<td><p><span data-ttu-id="c77fc-398">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-398">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-399"><a href="close-method-ado.md">Close</a></span><span class="sxs-lookup"><span data-stu-id="c77fc-399"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="c77fc-400">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-400">Yes</span></span></p></td>
<td><p><span data-ttu-id="c77fc-401">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-401">Yes</span></span></p></td>
<td><p><span data-ttu-id="c77fc-402">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-402">Yes</span></span></p></td>
<td><p><span data-ttu-id="c77fc-403">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-403">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-404"><a href="delete-method-ado-recordset.md">удаление</a>;</span><span class="sxs-lookup"><span data-stu-id="c77fc-404"><a href="delete-method-ado-recordset.md">Delete</a></span></span></p></td>
<td><p><span data-ttu-id="c77fc-405">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-405">Yes</span></span></p></td>
<td><p><span data-ttu-id="c77fc-406">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-406">Yes</span></span></p></td>
<td><p><span data-ttu-id="c77fc-407">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-407">Yes</span></span></p></td>
<td><p><span data-ttu-id="c77fc-408">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-408">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-409"><a href="getrows-method-ado.md">GetRows</a></span><span class="sxs-lookup"><span data-stu-id="c77fc-409"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="c77fc-410">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-410">Yes</span></span></p></td>
<td><p><span data-ttu-id="c77fc-411">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-411">Yes</span></span></p></td>
<td><p><span data-ttu-id="c77fc-412">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-412">Yes</span></span></p></td>
<td><p><span data-ttu-id="c77fc-413">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-413">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-414"><a href="move-method-ado.md">Move</a></span><span class="sxs-lookup"><span data-stu-id="c77fc-414"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="c77fc-415">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-415">Yes</span></span></p></td>
<td><p><span data-ttu-id="c77fc-416">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-416">Yes</span></span></p></td>
<td><p><span data-ttu-id="c77fc-417">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-417">Yes</span></span></p></td>
<td><p><span data-ttu-id="c77fc-418">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-418">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-419"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span><span class="sxs-lookup"><span data-stu-id="c77fc-419"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span></span></p></td>
<td><p><span data-ttu-id="c77fc-420">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-420">Yes</span></span></p></td>
<td><p><span data-ttu-id="c77fc-421">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-421">Yes</span></span></p></td>
<td><p><span data-ttu-id="c77fc-422">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-422">Yes</span></span></p></td>
<td><p><span data-ttu-id="c77fc-423">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-423">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-424"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span><span class="sxs-lookup"><span data-stu-id="c77fc-424"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span></span></p></td>
<td><p><span data-ttu-id="c77fc-425">Нет</span><span class="sxs-lookup"><span data-stu-id="c77fc-425">No</span></span></p></td>
<td><p><span data-ttu-id="c77fc-426">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-426">Yes</span></span></p></td>
<td><p><span data-ttu-id="c77fc-427">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-427">Yes</span></span></p></td>
<td><p><span data-ttu-id="c77fc-428">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-428">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-429"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span><span class="sxs-lookup"><span data-stu-id="c77fc-429"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span></span></p></td>
<td><p><span data-ttu-id="c77fc-430">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-430">Yes</span></span></p></td>
<td><p><span data-ttu-id="c77fc-431">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-431">Yes</span></span></p></td>
<td><p><span data-ttu-id="c77fc-432">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-432">Yes</span></span></p></td>
<td><p><span data-ttu-id="c77fc-433">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-433">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-434"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span><span class="sxs-lookup"><span data-stu-id="c77fc-434"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span></span></p></td>
<td><p><span data-ttu-id="c77fc-435">Нет</span><span class="sxs-lookup"><span data-stu-id="c77fc-435">No</span></span></p></td>
<td><p><span data-ttu-id="c77fc-436">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-436">Yes</span></span></p></td>
<td><p><span data-ttu-id="c77fc-437">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-437">Yes</span></span></p></td>
<td><p><span data-ttu-id="c77fc-438">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-438">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-439"><a href="nextrecordset-method-ado.md">NextRecordset</a>\*</span><span class="sxs-lookup"><span data-stu-id="c77fc-439"><a href="nextrecordset-method-ado.md">NextRecordset</a>\*</span></span></p></td>
<td><p><span data-ttu-id="c77fc-440">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-440">Yes</span></span></p></td>
<td><p><span data-ttu-id="c77fc-441">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-441">Yes</span></span></p></td>
<td><p><span data-ttu-id="c77fc-442">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-442">Yes</span></span></p></td>
<td><p><span data-ttu-id="c77fc-443">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-443">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-444"><a href="open-method-ado-recordset.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="c77fc-444"><a href="open-method-ado-recordset.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="c77fc-445">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-445">Yes</span></span></p></td>
<td><p><span data-ttu-id="c77fc-446">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-446">Yes</span></span></p></td>
<td><p><span data-ttu-id="c77fc-447">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-447">Yes</span></span></p></td>
<td><p><span data-ttu-id="c77fc-448">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-448">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-449"><a href="requery-method-ado.md">Requery</a></span><span class="sxs-lookup"><span data-stu-id="c77fc-449"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="c77fc-450">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-450">Yes</span></span></p></td>
<td><p><span data-ttu-id="c77fc-451">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-451">Yes</span></span></p></td>
<td><p><span data-ttu-id="c77fc-452">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-452">Yes</span></span></p></td>
<td><p><span data-ttu-id="c77fc-453">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-453">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-454"><a href="resync-method-ado.md">Resync</a></span><span class="sxs-lookup"><span data-stu-id="c77fc-454"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="c77fc-455">Нет</span><span class="sxs-lookup"><span data-stu-id="c77fc-455">No</span></span></p></td>
<td><p><span data-ttu-id="c77fc-456">Нет</span><span class="sxs-lookup"><span data-stu-id="c77fc-456">No</span></span></p></td>
<td><p><span data-ttu-id="c77fc-457">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-457">Yes</span></span></p></td>
<td><p><span data-ttu-id="c77fc-458">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-458">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-459"><a href="supports-method-ado.md">Имеется</a></span><span class="sxs-lookup"><span data-stu-id="c77fc-459"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="c77fc-460">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-460">Yes</span></span></p></td>
<td><p><span data-ttu-id="c77fc-461">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-461">Yes</span></span></p></td>
<td><p><span data-ttu-id="c77fc-462">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-462">Yes</span></span></p></td>
<td><p><span data-ttu-id="c77fc-463">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-463">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-464"><a href="update-method-ado.md">обновление</a>.</span><span class="sxs-lookup"><span data-stu-id="c77fc-464"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="c77fc-465">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-465">Yes</span></span></p></td>
<td><p><span data-ttu-id="c77fc-466">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-466">Yes</span></span></p></td>
<td><p><span data-ttu-id="c77fc-467">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-467">Yes</span></span></p></td>
<td><p><span data-ttu-id="c77fc-468">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-468">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-469"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="c77fc-469"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="c77fc-470">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-470">Yes</span></span></p></td>
<td><p><span data-ttu-id="c77fc-471">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-471">Yes</span></span></p></td>
<td><p><span data-ttu-id="c77fc-472">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-472">Yes</span></span></p></td>
<td><p><span data-ttu-id="c77fc-473">Да</span><span class="sxs-lookup"><span data-stu-id="c77fc-473">Yes</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c77fc-474">\*Не поддерживается для баз данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="c77fc-474">\*Not supported for Microsoft Access databases.</span></span>

## <a name="dynamic-properties"></a><span data-ttu-id="c77fc-475">Динамические свойства</span><span class="sxs-lookup"><span data-stu-id="c77fc-475">Dynamic Properties</span></span>

<span data-ttu-id="c77fc-476">Поставщик Microsoft OLE DB для ODBC вставляет несколько динамических свойств в коллекцию **свойств** неоткрытых [подключений](connection-object-ado.md), [наборов записей](recordset-object-ado.md)и [командных](command-object-ado.md) объектов.</span><span class="sxs-lookup"><span data-stu-id="c77fc-476">The Microsoft OLE DB Provider for ODBC inserts several dynamic properties into the **Properties** collection of the unopened [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md), and [Command](command-object-ado.md) objects.</span></span>

<span data-ttu-id="c77fc-477">В приведенных ниже таблицах указаны перекрестные индексы имен ADO и OLE DB для каждого динамического свойства.</span><span class="sxs-lookup"><span data-stu-id="c77fc-477">The tables below are a cross-index of the ADO and OLE DB names for each dynamic property.</span></span> <span data-ttu-id="c77fc-478">Справочник программиста OLE DB ссылается на имя свойства ADO по термину "Описание".</span><span class="sxs-lookup"><span data-stu-id="c77fc-478">The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description."</span></span> <span data-ttu-id="c77fc-479">Дополнительные сведения об этих свойствах можно найти в справочнике программиста по OLE DB.</span><span class="sxs-lookup"><span data-stu-id="c77fc-479">You can find more information about these properties in the OLE DB Programmer's Reference.</span></span> <span data-ttu-id="c77fc-480">Выполните поиск по имени свойства OLE DB в индексе или в разделе приложение C: свойства OLE DB.</span><span class="sxs-lookup"><span data-stu-id="c77fc-480">Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span></span>

## <a name="connection-dynamic-properties"></a><span data-ttu-id="c77fc-481">Динамические свойства подключения</span><span class="sxs-lookup"><span data-stu-id="c77fc-481">Connection Dynamic Properties</span></span>

<span data-ttu-id="c77fc-482">Следующие свойства добавляются в коллекцию **свойств** объекта **Connection** .</span><span class="sxs-lookup"><span data-stu-id="c77fc-482">The following properties are added to the **Connection** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c77fc-483">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="c77fc-483">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="c77fc-484">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="c77fc-484">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-485">Активные сеансы</span><span class="sxs-lookup"><span data-stu-id="c77fc-485">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="c77fc-486">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="c77fc-486">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-487">Асинчабле Abort</span><span class="sxs-lookup"><span data-stu-id="c77fc-487">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="c77fc-488">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="c77fc-488">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-489">Фиксация асинчабле</span><span class="sxs-lookup"><span data-stu-id="c77fc-489">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="c77fc-490">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="c77fc-490">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-491">Уровни изоляции для автоматической фиксации</span><span class="sxs-lookup"><span data-stu-id="c77fc-491">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="c77fc-492">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="c77fc-492">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-493">Расположение каталога</span><span class="sxs-lookup"><span data-stu-id="c77fc-493">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="c77fc-494">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="c77fc-494">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-495">Термин каталога</span><span class="sxs-lookup"><span data-stu-id="c77fc-495">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="c77fc-496">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="c77fc-496">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-497">Определение столбца</span><span class="sxs-lookup"><span data-stu-id="c77fc-497">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="c77fc-498">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="c77fc-498">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-499">Время ожидания подключения</span><span class="sxs-lookup"><span data-stu-id="c77fc-499">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="c77fc-500">DBPROP_INIT_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="c77fc-500">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-501">Текущий каталог</span><span class="sxs-lookup"><span data-stu-id="c77fc-501">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="c77fc-502">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="c77fc-502">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-503">Источник данных</span><span class="sxs-lookup"><span data-stu-id="c77fc-503">Data Source</span></span></p></td>
<td><p><span data-ttu-id="c77fc-504">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="c77fc-504">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-505">Имя источника данных</span><span class="sxs-lookup"><span data-stu-id="c77fc-505">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="c77fc-506">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="c77fc-506">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-507">Модель потоков объектов источника данных</span><span class="sxs-lookup"><span data-stu-id="c77fc-507">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="c77fc-508">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="c77fc-508">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-509">Имя СУБД</span><span class="sxs-lookup"><span data-stu-id="c77fc-509">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="c77fc-510">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="c77fc-510">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-511">Версия DBMS</span><span class="sxs-lookup"><span data-stu-id="c77fc-511">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="c77fc-512">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="c77fc-512">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-513">Расширенные свойства</span><span class="sxs-lookup"><span data-stu-id="c77fc-513">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="c77fc-514">DBPROP_INIT_PROVIDERSTRING</span><span class="sxs-lookup"><span data-stu-id="c77fc-514">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-515">ГРУППИРОВКа по поддержке</span><span class="sxs-lookup"><span data-stu-id="c77fc-515">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="c77fc-516">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="c77fc-516">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-517">Поддержка гетерогенных таблиц</span><span class="sxs-lookup"><span data-stu-id="c77fc-517">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="c77fc-518">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="c77fc-518">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-519">Чувствительность к регистру идентификаторов</span><span class="sxs-lookup"><span data-stu-id="c77fc-519">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="c77fc-520">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="c77fc-520">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-521">Исходный каталог</span><span class="sxs-lookup"><span data-stu-id="c77fc-521">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="c77fc-522">DBPROP_INIT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c77fc-522">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-523">Уровни изоляции</span><span class="sxs-lookup"><span data-stu-id="c77fc-523">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="c77fc-524">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="c77fc-524">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-525">Хранение изоляции</span><span class="sxs-lookup"><span data-stu-id="c77fc-525">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="c77fc-526">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="c77fc-526">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-527">Идентификатор языкового стандарта</span><span class="sxs-lookup"><span data-stu-id="c77fc-527">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="c77fc-528">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="c77fc-528">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-529">Расположение</span><span class="sxs-lookup"><span data-stu-id="c77fc-529">Location</span></span></p></td>
<td><p><span data-ttu-id="c77fc-530">DBPROP_INIT_LOCATION</span><span class="sxs-lookup"><span data-stu-id="c77fc-530">DBPROP_INIT_LOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-531">Максимальный размер индекса</span><span class="sxs-lookup"><span data-stu-id="c77fc-531">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="c77fc-532">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="c77fc-532">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-533">Максимальный размер строки</span><span class="sxs-lookup"><span data-stu-id="c77fc-533">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="c77fc-534">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="c77fc-534">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-535">Максимальный размер строки включает большой двоичный объект</span><span class="sxs-lookup"><span data-stu-id="c77fc-535">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="c77fc-536">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="c77fc-536">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-537">Максимальное число таблиц в SELECT</span><span class="sxs-lookup"><span data-stu-id="c77fc-537">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="c77fc-538">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="c77fc-538">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-539">Режим</span><span class="sxs-lookup"><span data-stu-id="c77fc-539">Mode</span></span></p></td>
<td><p><span data-ttu-id="c77fc-540">DBPROP_INIT_MODE</span><span class="sxs-lookup"><span data-stu-id="c77fc-540">DBPROP_INIT_MODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-541">Наборы параметров с несколькими параметрами</span><span class="sxs-lookup"><span data-stu-id="c77fc-541">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="c77fc-542">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="c77fc-542">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-543">Несколько результатов</span><span class="sxs-lookup"><span data-stu-id="c77fc-543">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="c77fc-544">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="c77fc-544">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-545">Несколько объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="c77fc-545">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="c77fc-546">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="c77fc-546">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-547">Обновление с несколькими таблицами</span><span class="sxs-lookup"><span data-stu-id="c77fc-547">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="c77fc-548">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="c77fc-548">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-549">Порядок сортировки NULL</span><span class="sxs-lookup"><span data-stu-id="c77fc-549">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="c77fc-550">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="c77fc-550">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-551">Поведение сцепления со значением NULL</span><span class="sxs-lookup"><span data-stu-id="c77fc-551">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="c77fc-552">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="c77fc-552">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-553">Службы OLE DB</span><span class="sxs-lookup"><span data-stu-id="c77fc-553">OLE DB Services</span></span></p></td>
<td><p><span data-ttu-id="c77fc-554">DBPROP_INIT_OLEDBSERVICES</span><span class="sxs-lookup"><span data-stu-id="c77fc-554">DBPROP_INIT_OLEDBSERVICES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-555">Версия OLE DB</span><span class="sxs-lookup"><span data-stu-id="c77fc-555">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="c77fc-556">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="c77fc-556">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-557">Поддержка объектов OLE</span><span class="sxs-lookup"><span data-stu-id="c77fc-557">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="c77fc-558">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="c77fc-558">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-559">Поддержка открытых наборов строк</span><span class="sxs-lookup"><span data-stu-id="c77fc-559">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="c77fc-560">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="c77fc-560">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-561">УПОРЯДОЧЕНие по столбцам в списке выборки</span><span class="sxs-lookup"><span data-stu-id="c77fc-561">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="c77fc-562">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="c77fc-562">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-563">Доступность выходного параметра</span><span class="sxs-lookup"><span data-stu-id="c77fc-563">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="c77fc-564">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="c77fc-564">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-565">Password</span><span class="sxs-lookup"><span data-stu-id="c77fc-565">Password</span></span></p></td>
<td><p><span data-ttu-id="c77fc-566">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="c77fc-566">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-567">Передача по параметрам доступа ref</span><span class="sxs-lookup"><span data-stu-id="c77fc-567">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="c77fc-568">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="c77fc-568">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-569">Сохранение сведений о безопасности</span><span class="sxs-lookup"><span data-stu-id="c77fc-569">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="c77fc-570">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span><span class="sxs-lookup"><span data-stu-id="c77fc-570">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-571">Тип постоянного идентификатора</span><span class="sxs-lookup"><span data-stu-id="c77fc-571">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="c77fc-572">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="c77fc-572">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-573">Действие по подготовке к прерыванию</span><span class="sxs-lookup"><span data-stu-id="c77fc-573">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="c77fc-574">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="c77fc-574">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-575">Подготовка режима фиксации</span><span class="sxs-lookup"><span data-stu-id="c77fc-575">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="c77fc-576">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="c77fc-576">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-577">Термин процедуры</span><span class="sxs-lookup"><span data-stu-id="c77fc-577">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="c77fc-578">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="c77fc-578">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-579">Prompt</span><span class="sxs-lookup"><span data-stu-id="c77fc-579">Prompt</span></span></p></td>
<td><p><span data-ttu-id="c77fc-580">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="c77fc-580">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-581">Понятное имя поставщика</span><span class="sxs-lookup"><span data-stu-id="c77fc-581">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="c77fc-582">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="c77fc-582">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-583">Имя поставщика</span><span class="sxs-lookup"><span data-stu-id="c77fc-583">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="c77fc-584">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="c77fc-584">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-585">Версия поставщика</span><span class="sxs-lookup"><span data-stu-id="c77fc-585">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="c77fc-586">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="c77fc-586">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-587">Источник данных, предназначенный только для чтения</span><span class="sxs-lookup"><span data-stu-id="c77fc-587">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="c77fc-588">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="c77fc-588">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-589">Преобразования наборов строк для команды</span><span class="sxs-lookup"><span data-stu-id="c77fc-589">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="c77fc-590">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="c77fc-590">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-591">Термин схемы</span><span class="sxs-lookup"><span data-stu-id="c77fc-591">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="c77fc-592">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="c77fc-592">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-593">Использование схемы</span><span class="sxs-lookup"><span data-stu-id="c77fc-593">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="c77fc-594">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="c77fc-594">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-595">Поддержка SQL</span><span class="sxs-lookup"><span data-stu-id="c77fc-595">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="c77fc-596">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="c77fc-596">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-597">Структурированное хранилище</span><span class="sxs-lookup"><span data-stu-id="c77fc-597">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="c77fc-598">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="c77fc-598">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-599">Поддержка вложенных запросов</span><span class="sxs-lookup"><span data-stu-id="c77fc-599">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="c77fc-600">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="c77fc-600">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-601">Табличный термин</span><span class="sxs-lookup"><span data-stu-id="c77fc-601">Table Term</span></span></p></td>
<td><p><span data-ttu-id="c77fc-602">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="c77fc-602">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-603">DDL транзакции</span><span class="sxs-lookup"><span data-stu-id="c77fc-603">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="c77fc-604">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="c77fc-604">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-605">Идентификатор пользователя</span><span class="sxs-lookup"><span data-stu-id="c77fc-605">User ID</span></span></p></td>
<td><p><span data-ttu-id="c77fc-606">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="c77fc-606">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-607">имя пользователя;</span><span class="sxs-lookup"><span data-stu-id="c77fc-607">User Name</span></span></p></td>
<td><p><span data-ttu-id="c77fc-608">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="c77fc-608">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-609">Дескриптор окна</span><span class="sxs-lookup"><span data-stu-id="c77fc-609">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="c77fc-610">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="c77fc-610">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a><span data-ttu-id="c77fc-611">Динамические свойства Recordset</span><span class="sxs-lookup"><span data-stu-id="c77fc-611">Recordset Dynamic Properties</span></span>

<span data-ttu-id="c77fc-612">Следующие свойства добавляются в коллекцию **свойств** объекта **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="c77fc-612">The following properties are added to the **Recordset** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c77fc-613">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="c77fc-613">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="c77fc-614">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="c77fc-614">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-615">Порядок доступа</span><span class="sxs-lookup"><span data-stu-id="c77fc-615">Access Order</span></span></p></td>
<td><p><span data-ttu-id="c77fc-616">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="c77fc-616">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-617">Блокировка объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="c77fc-617">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="c77fc-618">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="c77fc-618">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-619">Тип закладки</span><span class="sxs-lookup"><span data-stu-id="c77fc-619">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="c77fc-620">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="c77fc-620">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-621">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="c77fc-621">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="c77fc-622">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="c77fc-622">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-623">Изменение вставленных строк</span><span class="sxs-lookup"><span data-stu-id="c77fc-623">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="c77fc-624">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="c77fc-624">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-625">Права на столбцы</span><span class="sxs-lookup"><span data-stu-id="c77fc-625">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="c77fc-626">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="c77fc-626">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-627">Уведомление о наборе столбцов</span><span class="sxs-lookup"><span data-stu-id="c77fc-627">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="c77fc-628">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="c77fc-628">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-629">Откладывание обновлений объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="c77fc-629">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="c77fc-630">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="c77fc-630">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-631">Извлечение назад</span><span class="sxs-lookup"><span data-stu-id="c77fc-631">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="c77fc-632">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="c77fc-632">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-633">Удержание строк</span><span class="sxs-lookup"><span data-stu-id="c77fc-633">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="c77fc-634">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="c77fc-634">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-635">иакцессор</span><span class="sxs-lookup"><span data-stu-id="c77fc-635">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="c77fc-636">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="c77fc-636">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-637">иколумнсинфо</span><span class="sxs-lookup"><span data-stu-id="c77fc-637">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="c77fc-638">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="c77fc-638">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-639">иколумнсровсет</span><span class="sxs-lookup"><span data-stu-id="c77fc-639">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="c77fc-640">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="c77fc-640">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-641">иконнектионпоинтконтаинер</span><span class="sxs-lookup"><span data-stu-id="c77fc-641">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="c77fc-642">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="c77fc-642">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-643">иконверттипе</span><span class="sxs-lookup"><span data-stu-id="c77fc-643">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="c77fc-644">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="c77fc-644">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-645">Строки для мобильных устройств</span><span class="sxs-lookup"><span data-stu-id="c77fc-645">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="c77fc-646">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="c77fc-646">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-647">IRowset</span><span class="sxs-lookup"><span data-stu-id="c77fc-647">IRowset</span></span></p></td>
<td><p><span data-ttu-id="c77fc-648">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="c77fc-648">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-649">ировсетчанже</span><span class="sxs-lookup"><span data-stu-id="c77fc-649">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="c77fc-650">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="c77fc-650">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-651">ировсетидентити</span><span class="sxs-lookup"><span data-stu-id="c77fc-651">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="c77fc-652">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="c77fc-652">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-653">ировсетинфо</span><span class="sxs-lookup"><span data-stu-id="c77fc-653">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="c77fc-654">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="c77fc-654">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-655">ировсетлокате</span><span class="sxs-lookup"><span data-stu-id="c77fc-655">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="c77fc-656">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="c77fc-656">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-657">ировсетресинч</span><span class="sxs-lookup"><span data-stu-id="c77fc-657">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-658">ировсетупдате</span><span class="sxs-lookup"><span data-stu-id="c77fc-658">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="c77fc-659">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="c77fc-659">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-660">исекуентиалстреам</span><span class="sxs-lookup"><span data-stu-id="c77fc-660">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="c77fc-661">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="c77fc-661">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-662">исуппортерроринфо</span><span class="sxs-lookup"><span data-stu-id="c77fc-662">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="c77fc-663">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="c77fc-663">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-664">Литеральные закладки</span><span class="sxs-lookup"><span data-stu-id="c77fc-664">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="c77fc-665">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="c77fc-665">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-666">Идентификация строк литералов</span><span class="sxs-lookup"><span data-stu-id="c77fc-666">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="c77fc-667">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="c77fc-667">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-668">Максимальное число открытых строк</span><span class="sxs-lookup"><span data-stu-id="c77fc-668">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="c77fc-669">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="c77fc-669">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-670">Максимальное число ожидающих строк</span><span class="sxs-lookup"><span data-stu-id="c77fc-670">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="c77fc-671">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="c77fc-671">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-672">Максимальное число строк</span><span class="sxs-lookup"><span data-stu-id="c77fc-672">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="c77fc-673">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="c77fc-673">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-674">Детализация уведомлений</span><span class="sxs-lookup"><span data-stu-id="c77fc-674">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="c77fc-675">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="c77fc-675">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-676">Этапы уведомления</span><span class="sxs-lookup"><span data-stu-id="c77fc-676">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="c77fc-677">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="c77fc-677">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-678">Объекты, транзакционные</span><span class="sxs-lookup"><span data-stu-id="c77fc-678">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="c77fc-679">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="c77fc-679">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-680">Видны изменения</span><span class="sxs-lookup"><span data-stu-id="c77fc-680">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="c77fc-681">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="c77fc-681">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-682">Отображение собственных вставок</span><span class="sxs-lookup"><span data-stu-id="c77fc-682">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="c77fc-683">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="c77fc-683">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-684">Сохранение при прерывании</span><span class="sxs-lookup"><span data-stu-id="c77fc-684">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="c77fc-685">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="c77fc-685">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-686">Сохранение при фиксации</span><span class="sxs-lookup"><span data-stu-id="c77fc-686">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="c77fc-687">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="c77fc-687">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-688">Быстрый перезапуск</span><span class="sxs-lookup"><span data-stu-id="c77fc-688">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="c77fc-689">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="c77fc-689">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-690">Повторные события</span><span class="sxs-lookup"><span data-stu-id="c77fc-690">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="c77fc-691">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="c77fc-691">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-692">Удаление удаленных строк</span><span class="sxs-lookup"><span data-stu-id="c77fc-692">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="c77fc-693">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="c77fc-693">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-694">Отчет о нескольких изменениях</span><span class="sxs-lookup"><span data-stu-id="c77fc-694">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="c77fc-695">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="c77fc-695">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-696">Возврат ожидающих вставок</span><span class="sxs-lookup"><span data-stu-id="c77fc-696">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="c77fc-697">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="c77fc-697">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-698">Уведомление об удалении строки</span><span class="sxs-lookup"><span data-stu-id="c77fc-698">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="c77fc-699">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="c77fc-699">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-700">Уведомление о первом изменении строки</span><span class="sxs-lookup"><span data-stu-id="c77fc-700">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="c77fc-701">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="c77fc-701">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-702">Уведомление о вставке строк</span><span class="sxs-lookup"><span data-stu-id="c77fc-702">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="c77fc-703">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="c77fc-703">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-704">Права на строки</span><span class="sxs-lookup"><span data-stu-id="c77fc-704">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="c77fc-705">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="c77fc-705">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-706">Уведомление о повторной синхронизации строк</span><span class="sxs-lookup"><span data-stu-id="c77fc-706">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="c77fc-707">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="c77fc-707">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-708">Потоковая модель для строк</span><span class="sxs-lookup"><span data-stu-id="c77fc-708">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="c77fc-709">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="c77fc-709">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-710">Уведомление об отмене изменения строки</span><span class="sxs-lookup"><span data-stu-id="c77fc-710">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="c77fc-711">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="c77fc-711">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-712">Уведомление о отмене удаления строки</span><span class="sxs-lookup"><span data-stu-id="c77fc-712">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="c77fc-713">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="c77fc-713">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-714">Уведомление об отмене вставки строки</span><span class="sxs-lookup"><span data-stu-id="c77fc-714">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="c77fc-715">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="c77fc-715">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-716">Уведомление об обновлении строк</span><span class="sxs-lookup"><span data-stu-id="c77fc-716">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="c77fc-717">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="c77fc-717">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-718">Уведомление об изменении положения при получении набора строк</span><span class="sxs-lookup"><span data-stu-id="c77fc-718">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="c77fc-719">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="c77fc-719">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-720">Уведомление о выпуске набора строк</span><span class="sxs-lookup"><span data-stu-id="c77fc-720">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="c77fc-721">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="c77fc-721">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-722">Прокрутка назад</span><span class="sxs-lookup"><span data-stu-id="c77fc-722">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="c77fc-723">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="c77fc-723">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-724">Пропуск удаленных закладок</span><span class="sxs-lookup"><span data-stu-id="c77fc-724">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="c77fc-725">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="c77fc-725">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-726">Строгая идентификация строк</span><span class="sxs-lookup"><span data-stu-id="c77fc-726">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="c77fc-727">DBPROP_STRONGITDENTITY</span><span class="sxs-lookup"><span data-stu-id="c77fc-727">DBPROP_STRONGITDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-728">Уникальные строки</span><span class="sxs-lookup"><span data-stu-id="c77fc-728">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="c77fc-729">DBPROP_UNIQUEROWS</span><span class="sxs-lookup"><span data-stu-id="c77fc-729">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-730">Обновление</span><span class="sxs-lookup"><span data-stu-id="c77fc-730">Updatability</span></span></p></td>
<td><p><span data-ttu-id="c77fc-731">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="c77fc-731">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-732">Использование закладок</span><span class="sxs-lookup"><span data-stu-id="c77fc-732">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="c77fc-733">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="c77fc-733">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a><span data-ttu-id="c77fc-734">Динамические свойства команд</span><span class="sxs-lookup"><span data-stu-id="c77fc-734">Command Dynamic Properties</span></span>

<span data-ttu-id="c77fc-735">Указанные ниже свойства добавляются в коллекцию **свойств** **командного** объекта.</span><span class="sxs-lookup"><span data-stu-id="c77fc-735">The following properties are added to the **Command** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c77fc-736">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="c77fc-736">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="c77fc-737">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="c77fc-737">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-738">Порядок доступа</span><span class="sxs-lookup"><span data-stu-id="c77fc-738">Access Order</span></span></p></td>
<td><p><span data-ttu-id="c77fc-739">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="c77fc-739">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-740">Блокировка объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="c77fc-740">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="c77fc-741">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="c77fc-741">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-742">Тип закладки</span><span class="sxs-lookup"><span data-stu-id="c77fc-742">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="c77fc-743">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="c77fc-743">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-744">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="c77fc-744">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="c77fc-745">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="c77fc-745">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-746">Изменение вставленных строк</span><span class="sxs-lookup"><span data-stu-id="c77fc-746">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="c77fc-747">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="c77fc-747">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-748">Права на столбцы</span><span class="sxs-lookup"><span data-stu-id="c77fc-748">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="c77fc-749">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="c77fc-749">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-750">Уведомление о наборе столбцов</span><span class="sxs-lookup"><span data-stu-id="c77fc-750">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="c77fc-751">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="c77fc-751">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-752">Откладывание обновлений объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="c77fc-752">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="c77fc-753">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="c77fc-753">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-754">Извлечение назад</span><span class="sxs-lookup"><span data-stu-id="c77fc-754">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="c77fc-755">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="c77fc-755">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-756">Удержание строк</span><span class="sxs-lookup"><span data-stu-id="c77fc-756">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="c77fc-757">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="c77fc-757">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-758">иакцессор</span><span class="sxs-lookup"><span data-stu-id="c77fc-758">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="c77fc-759">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="c77fc-759">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-760">иколумнсинфо</span><span class="sxs-lookup"><span data-stu-id="c77fc-760">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="c77fc-761">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="c77fc-761">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-762">иколумнсровсет</span><span class="sxs-lookup"><span data-stu-id="c77fc-762">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="c77fc-763">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="c77fc-763">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-764">иконнектионпоинтконтаинер</span><span class="sxs-lookup"><span data-stu-id="c77fc-764">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="c77fc-765">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="c77fc-765">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-766">иконверттипе</span><span class="sxs-lookup"><span data-stu-id="c77fc-766">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="c77fc-767">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="c77fc-767">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-768">Строки для мобильных устройств</span><span class="sxs-lookup"><span data-stu-id="c77fc-768">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="c77fc-769">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="c77fc-769">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-770">IRowset</span><span class="sxs-lookup"><span data-stu-id="c77fc-770">IRowset</span></span></p></td>
<td><p><span data-ttu-id="c77fc-771">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="c77fc-771">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-772">ировсетчанже</span><span class="sxs-lookup"><span data-stu-id="c77fc-772">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="c77fc-773">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="c77fc-773">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-774">ировсетидентити</span><span class="sxs-lookup"><span data-stu-id="c77fc-774">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="c77fc-775">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="c77fc-775">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-776">ировсетинфо</span><span class="sxs-lookup"><span data-stu-id="c77fc-776">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="c77fc-777">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="c77fc-777">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-778">ировсетлокате</span><span class="sxs-lookup"><span data-stu-id="c77fc-778">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="c77fc-779">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="c77fc-779">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-780">ировсетресинч</span><span class="sxs-lookup"><span data-stu-id="c77fc-780">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-781">ировсетупдате</span><span class="sxs-lookup"><span data-stu-id="c77fc-781">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="c77fc-782">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="c77fc-782">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-783">исекуентиалстреам</span><span class="sxs-lookup"><span data-stu-id="c77fc-783">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="c77fc-784">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="c77fc-784">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-785">исуппортерроринфо</span><span class="sxs-lookup"><span data-stu-id="c77fc-785">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="c77fc-786">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="c77fc-786">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-787">Литеральные закладки</span><span class="sxs-lookup"><span data-stu-id="c77fc-787">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="c77fc-788">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="c77fc-788">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-789">Идентификация строк литералов</span><span class="sxs-lookup"><span data-stu-id="c77fc-789">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="c77fc-790">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="c77fc-790">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-791">Максимальное число открытых строк</span><span class="sxs-lookup"><span data-stu-id="c77fc-791">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="c77fc-792">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="c77fc-792">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-793">Максимальное число ожидающих строк</span><span class="sxs-lookup"><span data-stu-id="c77fc-793">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="c77fc-794">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="c77fc-794">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-795">Максимальное число строк</span><span class="sxs-lookup"><span data-stu-id="c77fc-795">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="c77fc-796">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="c77fc-796">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-797">Детализация уведомлений</span><span class="sxs-lookup"><span data-stu-id="c77fc-797">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="c77fc-798">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="c77fc-798">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-799">Этапы уведомления</span><span class="sxs-lookup"><span data-stu-id="c77fc-799">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="c77fc-800">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="c77fc-800">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-801">Объекты, транзакционные</span><span class="sxs-lookup"><span data-stu-id="c77fc-801">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="c77fc-802">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="c77fc-802">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-803">Видны изменения</span><span class="sxs-lookup"><span data-stu-id="c77fc-803">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="c77fc-804">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="c77fc-804">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-805">Отображение собственных вставок</span><span class="sxs-lookup"><span data-stu-id="c77fc-805">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="c77fc-806">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="c77fc-806">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-807">Сохранение при прерывании</span><span class="sxs-lookup"><span data-stu-id="c77fc-807">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="c77fc-808">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="c77fc-808">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-809">Сохранение при фиксации</span><span class="sxs-lookup"><span data-stu-id="c77fc-809">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="c77fc-810">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="c77fc-810">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-811">Быстрый перезапуск</span><span class="sxs-lookup"><span data-stu-id="c77fc-811">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="c77fc-812">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="c77fc-812">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-813">Повторные события</span><span class="sxs-lookup"><span data-stu-id="c77fc-813">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="c77fc-814">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="c77fc-814">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-815">Удаление удаленных строк</span><span class="sxs-lookup"><span data-stu-id="c77fc-815">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="c77fc-816">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="c77fc-816">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-817">Отчет о нескольких изменениях</span><span class="sxs-lookup"><span data-stu-id="c77fc-817">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="c77fc-818">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="c77fc-818">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-819">Возврат ожидающих вставок</span><span class="sxs-lookup"><span data-stu-id="c77fc-819">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="c77fc-820">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="c77fc-820">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-821">Уведомление об удалении строки</span><span class="sxs-lookup"><span data-stu-id="c77fc-821">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="c77fc-822">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="c77fc-822">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-823">Уведомление о первом изменении строки</span><span class="sxs-lookup"><span data-stu-id="c77fc-823">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="c77fc-824">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="c77fc-824">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-825">Уведомление о вставке строк</span><span class="sxs-lookup"><span data-stu-id="c77fc-825">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="c77fc-826">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="c77fc-826">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-827">Права на строки</span><span class="sxs-lookup"><span data-stu-id="c77fc-827">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="c77fc-828">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="c77fc-828">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-829">Уведомление о повторной синхронизации строк</span><span class="sxs-lookup"><span data-stu-id="c77fc-829">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="c77fc-830">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="c77fc-830">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-831">Потоковая модель для строк</span><span class="sxs-lookup"><span data-stu-id="c77fc-831">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="c77fc-832">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="c77fc-832">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-833">Уведомление об отмене изменения строки</span><span class="sxs-lookup"><span data-stu-id="c77fc-833">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="c77fc-834">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="c77fc-834">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-835">Уведомление о отмене удаления строки</span><span class="sxs-lookup"><span data-stu-id="c77fc-835">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="c77fc-836">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="c77fc-836">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-837">Уведомление об отмене вставки строки</span><span class="sxs-lookup"><span data-stu-id="c77fc-837">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="c77fc-838">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="c77fc-838">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-839">Уведомление об обновлении строк</span><span class="sxs-lookup"><span data-stu-id="c77fc-839">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="c77fc-840">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="c77fc-840">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-841">Уведомление об изменении положения при получении набора строк</span><span class="sxs-lookup"><span data-stu-id="c77fc-841">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="c77fc-842">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="c77fc-842">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-843">Уведомление о выпуске набора строк</span><span class="sxs-lookup"><span data-stu-id="c77fc-843">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="c77fc-844">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="c77fc-844">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-845">Прокрутка назад</span><span class="sxs-lookup"><span data-stu-id="c77fc-845">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="c77fc-846">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="c77fc-846">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-847">Пропуск удаленных закладок</span><span class="sxs-lookup"><span data-stu-id="c77fc-847">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="c77fc-848">DBPROP_BOOKMARKSKIP</span><span class="sxs-lookup"><span data-stu-id="c77fc-848">DBPROP_BOOKMARKSKIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-849">Строгая идентификация строк</span><span class="sxs-lookup"><span data-stu-id="c77fc-849">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="c77fc-850">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="c77fc-850">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77fc-851">Обновление</span><span class="sxs-lookup"><span data-stu-id="c77fc-851">Updatability</span></span></p></td>
<td><p><span data-ttu-id="c77fc-852">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="c77fc-852">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77fc-853">Использование закладок</span><span class="sxs-lookup"><span data-stu-id="c77fc-853">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="c77fc-854">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="c77fc-854">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="c77fc-855">См. также</span><span class="sxs-lookup"><span data-stu-id="c77fc-855">See also</span></span>

<span data-ttu-id="c77fc-856">Сведения о конкретных реализациях и функциональных сведениях о поставщике Microsoft OLE DB для ODBC можно найти в [руководстве программиста по OLE DB](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85)) или посетить [Центр разработчиков платформы данных](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).</span><span class="sxs-lookup"><span data-stu-id="c77fc-856">For details regarding specific implementation and functional information about the Microsoft OLE DB Provider for ODBC, consult the [OLE DB Programmer's Guide](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85)) or visit the [Data Platform Developer Center](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).</span></span>

