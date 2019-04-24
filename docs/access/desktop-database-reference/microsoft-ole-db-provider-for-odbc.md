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
# <a name="microsoft-ole-db-provider-for-odbc"></a><span data-ttu-id="33750-102">Поставщик Microsoft OLE DB для ODBC</span><span class="sxs-lookup"><span data-stu-id="33750-102">Microsoft OLE DB Provider for ODBC</span></span>

<span data-ttu-id="33750-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="33750-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="33750-104">Для программистов ADO или RDS лучше всего один, в котором каждый источник данных предоставляет интерфейс OLE DB, чтобы ADO мог напрямую вызывать источник данных.</span><span class="sxs-lookup"><span data-stu-id="33750-104">To an ADO or RDS programmer, an ideal world would be one in which every data source exposes an OLE DB interface, so that ADO could call directly into the data source.</span></span> <span data-ttu-id="33750-105">Несмотря на то, что дополнительные поставщики баз данных реализуют интерфейсы OLE DB, некоторые источники данных пока не предоставляются таким образом.</span><span class="sxs-lookup"><span data-stu-id="33750-105">Although increasingly more database vendors are implementing OLE DB interfaces, some data sources are not yet exposed this way.</span></span> <span data-ttu-id="33750-106">Тем не менее, практически все используемые сегодня системы СУБД можно получить с помощью ODBC.</span><span class="sxs-lookup"><span data-stu-id="33750-106">However, virtually all DBMS systems in use today can be accessed through ODBC.</span></span>

<span data-ttu-id="33750-107">Драйверы ODBC доступны для всех основных СУБД, используемых в настоящее время, включая Microsoft SQL Server, Microsoft Access (ядро базы данных Microsoft Jet) и Microsoft FoxPro, в дополнение к продуктам баз данных, отличным от Майкрософт, например Oracle.</span><span class="sxs-lookup"><span data-stu-id="33750-107">ODBC drivers are available for every major DBMS in use today, including Microsoft SQL Server, Microsoft Access (Microsoft Jet database engine), and Microsoft FoxPro, in addition to non-Microsoft database products such as Oracle.</span></span>

<span data-ttu-id="33750-108">Тем не менее, поставщик Microsoft ODBC позволяет ADO подключаться к любому источнику данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="33750-108">The Microsoft ODBC Provider, however, allows ADO to connect to any ODBC data source.</span></span> <span data-ttu-id="33750-109">Поставщик доступен для бесплатных потоков и включен Юникод.</span><span class="sxs-lookup"><span data-stu-id="33750-109">The provider is free-threaded and Unicode enabled.</span></span>

<span data-ttu-id="33750-110">Поставщик поддерживает транзакции, хотя различные механизмы СУБД предоставляют различные типы поддержки транзакций.</span><span class="sxs-lookup"><span data-stu-id="33750-110">The provider supports transactions, although different DBMS engines offer different types of transaction support.</span></span> <span data-ttu-id="33750-111">Например, Microsoft Access поддерживает вложенные транзакции вплоть до пяти уровней.</span><span class="sxs-lookup"><span data-stu-id="33750-111">For example, Microsoft Access supports nested transactions up to five levels deep.</span></span>

<span data-ttu-id="33750-112">Это поставщик по умолчанию для ADO, а также поддерживаются все свойства и методы, зависящие от поставщика.</span><span class="sxs-lookup"><span data-stu-id="33750-112">This is the default provider for ADO, and all provider-dependent ADO properties and methods are supported.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="33750-113">Параметры строки подключения</span><span class="sxs-lookup"><span data-stu-id="33750-113">Connection String Parameters</span></span>

<span data-ttu-id="33750-114">Чтобы подключиться к поставщику, присвойте аргументу **provider =** свойства [ConnectionString](connectionstring-property-ado.md) значение:</span><span class="sxs-lookup"><span data-stu-id="33750-114">To connect to this provider, set the **Provider=** argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```sql 
 
MSDASQL 
```

<span data-ttu-id="33750-115">Считывание свойства [provider](provider-property-ado.md) также возвратит эту строку.</span><span class="sxs-lookup"><span data-stu-id="33750-115">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="33750-116">Типичная строка подключения</span><span class="sxs-lookup"><span data-stu-id="33750-116">Typical Connection String</span></span>

<span data-ttu-id="33750-117">Типичная строка подключения для этого поставщика:</span><span class="sxs-lookup"><span data-stu-id="33750-117">A typical connection string for this provider is:</span></span>

```sql 
 
"Provider=MSDASQL;DSN=dsnName;UID=userName;PWD=userPassword;" 
```

<span data-ttu-id="33750-118">Строка состоит из следующих ключевых слов:</span><span class="sxs-lookup"><span data-stu-id="33750-118">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="33750-119">Ключевое слово</span><span class="sxs-lookup"><span data-stu-id="33750-119">Keyword</span></span></p></th>
<th><p><span data-ttu-id="33750-120">Описание</span><span class="sxs-lookup"><span data-stu-id="33750-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="33750-121"><strong>Поставщик</strong></span><span class="sxs-lookup"><span data-stu-id="33750-121"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="33750-122">Указывает поставщика OLE DB для ODBC.</span><span class="sxs-lookup"><span data-stu-id="33750-122">Specifies the OLE DB Provider for ODBC.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-123"><strong>DSN</strong></span><span class="sxs-lookup"><span data-stu-id="33750-123"><strong>DSN</strong></span></span></p></td>
<td><p><span data-ttu-id="33750-124">Указывает имя источника данных.</span><span class="sxs-lookup"><span data-stu-id="33750-124">Specifies the data source name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-125"><strong>UID</strong></span><span class="sxs-lookup"><span data-stu-id="33750-125"><strong>UID</strong></span></span></p></td>
<td><p><span data-ttu-id="33750-126">Задает имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="33750-126">Specifies the user name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-127"><strong>PWD</strong></span><span class="sxs-lookup"><span data-stu-id="33750-127"><strong>PWD</strong></span></span></p></td>
<td><p><span data-ttu-id="33750-128">Указывает пароль пользователя.</span><span class="sxs-lookup"><span data-stu-id="33750-128">Specifies the user password.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-129"><strong>URL</strong></span><span class="sxs-lookup"><span data-stu-id="33750-129"><strong>URL</strong></span></span></p></td>
<td><p><span data-ttu-id="33750-130">Указывает URL-адрес файла или каталога, опубликованного в веб-папке.</span><span class="sxs-lookup"><span data-stu-id="33750-130">Specifies the URL of a file or directory published in a web folder.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="33750-131">Так как это поставщик по умолчанию для ADO, если вы опустите параметр **provider =** из строки подключения, ADO попытается установить подключение к этому поставщику.</span><span class="sxs-lookup"><span data-stu-id="33750-131">Because this is the default provider for ADO, if you omit the **Provider=** parameter from the connection string, ADO will attempt to establish a connection to this provider.</span></span>

<span data-ttu-id="33750-132">Поставщик не поддерживает никакие особые параметры подключения, кроме тех, которые определены в ADO.</span><span class="sxs-lookup"><span data-stu-id="33750-132">The provider does not support any specific connection parameters in addition to those defined by ADO.</span></span> <span data-ttu-id="33750-133">Тем не менее, поставщик передаст параметры подключений, не являющихся ADO, в диспетчер драйверов ODBC.</span><span class="sxs-lookup"><span data-stu-id="33750-133">However, the provider will pass any non-ADO connection parameters to the ODBC driver manager.</span></span>

<span data-ttu-id="33750-134">Так как вы можете опустить параметр **provider** , вы можете создать строку подключения ADO, идентичную строке подключения ODBC для одного и того же источника данных.</span><span class="sxs-lookup"><span data-stu-id="33750-134">Because you can omit the **Provider** parameter, you can therefore compose an ADO connection string that is identical to an ODBC connection string for the same data source.</span></span> <span data-ttu-id="33750-135">Используйте те же имена параметров (**Driver =**, **Database =**, **DSN =** и т. д.), значения и синтаксис, что и при создании строки подключения ODBC.</span><span class="sxs-lookup"><span data-stu-id="33750-135">Use the same parameter names (**DRIVER=**, **DATABASE=**, **DSN=**, and so on), values, and syntax as you would when composing an ODBC connection string.</span></span> <span data-ttu-id="33750-136">Можно подключаться к предварительно заданному имени источника данных (DSN) или Филедсн без него.</span><span class="sxs-lookup"><span data-stu-id="33750-136">You can connect with or without a predefined data source name (DSN) or FileDSN.</span></span>

<span data-ttu-id="33750-137">**Синтаксис с именем DSN или Филедсн:**</span><span class="sxs-lookup"><span data-stu-id="33750-137">**Syntax with a DSN or FileDSN:**</span></span>

`"[Provider=MSDASQL;] { DSN=name | FileDSN=filename } ; [DATABASE=database;] UID=user; PWD=password"`

<span data-ttu-id="33750-138">**Синтаксис без имени DSN (подключение без DSN):**</span><span class="sxs-lookup"><span data-stu-id="33750-138">**Syntax without a DSN (DSN-less connection):**</span></span>

`"[Provider=MSDASQL;] DRIVER=driver; SERVER=server;DATABASE=database; UID=user; PWD=password"`

<span data-ttu-id="33750-139">Если вы используете **имя DSN** или **филедсн**, оно должно быть определено администратором источника данных ODBC в панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="33750-139">If you use a **DSN** or **FileDSN**, it must be defined through the ODBC Data Source Administrator in the Windows Control Panel.</span></span> <span data-ttu-id="33750-140">В Microsoft Windows 2000 администратор ODBC находится в разделе Администрирование.</span><span class="sxs-lookup"><span data-stu-id="33750-140">In Microsoft Windows 2000, the ODBC Administrator is located under Administrative Tools.</span></span> <span data-ttu-id="33750-141">В предыдущих версиях Windows значок администратора ODBC называется **32-разрядНЫМ ODBC** или просто **ODBC**.</span><span class="sxs-lookup"><span data-stu-id="33750-141">In previous versions of Windows, the ODBC Administrator icon is named **32-bit ODBC** or simply **ODBC**.</span></span>

<span data-ttu-id="33750-142">В качестве альтернативы для установки **DSN**можно указать драйвер ODBC (**Driver =**), например "SQL Server;" имя сервера (**Server =**); и имя базы данных (**Database =**).</span><span class="sxs-lookup"><span data-stu-id="33750-142">As an alternative to setting a **DSN**, you can specify the ODBC driver (**DRIVER=**), such as "SQL Server;" the server name (**SERVER=**); and the database name (**DATABASE=**).</span></span>

<span data-ttu-id="33750-143">Вы также можете указать имя учетной записи пользователя (**UID =**) и пароль для учетной записи пользователя (**PWD =**) в параметрах, ОТносящихся к ODBC, или в стандартных параметрах *пользователя* и *пароля* , определенных в ADO.</span><span class="sxs-lookup"><span data-stu-id="33750-143">You can also specify a user account name (**UID=**), and the password for the user account (**PWD=**) in the ODBC-specific parameters or in the standard ADO-defined *user* and *password* parameters.</span></span>

<span data-ttu-id="33750-144">Несмотря на то, что определение **DSN** уже определяет базу данных, \*\* можно указать параметр *базы данных* в дополнение к **имени DSN** для подключения к другой базе данных.</span><span class="sxs-lookup"><span data-stu-id="33750-144">Although a **DSN** definition already specifies a database, you can specify *a* *database* parameter in addition to a **DSN** to connect to a different database.</span></span> <span data-ttu-id="33750-145">Рекомендуется всегда включать параметр \*\* *Database* при использовании **DSN**.</span><span class="sxs-lookup"><span data-stu-id="33750-145">It is a good idea to always include *the* *database* parameter when you use a **DSN**.</span></span> <span data-ttu-id="33750-146">Это обеспечит подключение к соответствующей базе данных в случае, если другой пользователь изменил параметр базы данных по умолчанию после последней проверки определения **DSN** .</span><span class="sxs-lookup"><span data-stu-id="33750-146">This will ensure that you connect to the proper database in the event that another user changed the default database parameter since you last checked the **DSN** definition.</span></span>

## <a name="provider-specific-connection-properties"></a><span data-ttu-id="33750-147">Свойства подключения, зависящие от поставщика</span><span class="sxs-lookup"><span data-stu-id="33750-147">Provider-Specific Connection Properties</span></span>

<span data-ttu-id="33750-148">Поставщик OLE DB для ODBC добавляет несколько свойств в коллекцию [свойств](properties-collection-ado.md) объекта **Connection** .</span><span class="sxs-lookup"><span data-stu-id="33750-148">The OLE DB provider for ODBC adds several properties to the [Properties](properties-collection-ado.md) collection of the **Connection** object.</span></span> <span data-ttu-id="33750-149">В приведенной ниже таблице указаны эти свойства с соответствующим именем свойства OLE DB в круглых скобках.</span><span class="sxs-lookup"><span data-stu-id="33750-149">The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="33750-150">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="33750-150">Property Name</span></span></p></th>
<th><p><span data-ttu-id="33750-151">Описание</span><span class="sxs-lookup"><span data-stu-id="33750-151">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="33750-152">Доступные процедуры</span><span class="sxs-lookup"><span data-stu-id="33750-152">Accessible Procedures</span></span><br />
<span data-ttu-id="33750-153">(КАГПРОП_АКЦЕССИБЛЕПРОЦЕДУРЕС)</span><span class="sxs-lookup"><span data-stu-id="33750-153">(KAGPROP_ACCESSIBLEPROCEDURES)</span></span></p></td>
<td><p><span data-ttu-id="33750-154">Указывает, имеет ли пользователь доступ к хранимым процедурам.</span><span class="sxs-lookup"><span data-stu-id="33750-154">Indicates whether the user has access to stored procedures.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-155">Доступные таблицы</span><span class="sxs-lookup"><span data-stu-id="33750-155">Accessible Tables</span></span><br />
<span data-ttu-id="33750-156">(КАГПРОП_АКЦЕССИБЛЕТАБЛЕС)</span><span class="sxs-lookup"><span data-stu-id="33750-156">(KAGPROP_ACCESSIBLETABLES)</span></span></p></td>
<td><p><span data-ttu-id="33750-157">Указывает, имеет ли пользователь разрешение на выполнение операторов SELECT в таблицах базы данных.</span><span class="sxs-lookup"><span data-stu-id="33750-157">Indicates whether the user has permission to execute SELECT statements against the database tables.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-158">Активные операторы</span><span class="sxs-lookup"><span data-stu-id="33750-158">Active Statements</span></span><br />
<span data-ttu-id="33750-159">(КАГПРОП_АКТИВЕСТАТЕМЕНТС)</span><span class="sxs-lookup"><span data-stu-id="33750-159">(KAGPROP_ACTIVESTATEMENTS)</span></span></p></td>
<td><p><span data-ttu-id="33750-160">Указывает количество дескрипторов, которые драйвер ODBC может поддерживать для подключения.</span><span class="sxs-lookup"><span data-stu-id="33750-160">Indicates the number of handles an ODBC driver can support on a connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-161">Имя драйвера</span><span class="sxs-lookup"><span data-stu-id="33750-161">Driver Name</span></span><br />
<span data-ttu-id="33750-162">(КАГПРОП_ДРИВЕРНАМЕ)</span><span class="sxs-lookup"><span data-stu-id="33750-162">(KAGPROP_DRIVERNAME)</span></span></p></td>
<td><p><span data-ttu-id="33750-163">Указывает имя файла драйвера ODBC.</span><span class="sxs-lookup"><span data-stu-id="33750-163">Indicates the file name of the ODBC driver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-164">Версия ODBC драйвера</span><span class="sxs-lookup"><span data-stu-id="33750-164">Driver ODBC Version</span></span><br />
<span data-ttu-id="33750-165">(КАГПРОП_ДРИВЕРОДБКВЕР)</span><span class="sxs-lookup"><span data-stu-id="33750-165">(KAGPROP_DRIVERODBCVER)</span></span></p></td>
<td><p><span data-ttu-id="33750-166">Указывает версию ODBC, поддерживаемую драйвером.</span><span class="sxs-lookup"><span data-stu-id="33750-166">Indicates the version of ODBC that this driver supports.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-167">Использование файла</span><span class="sxs-lookup"><span data-stu-id="33750-167">File Usage</span></span><br />
<span data-ttu-id="33750-168">(КАГПРОП_ФИЛЕУСАЖЕ)</span><span class="sxs-lookup"><span data-stu-id="33750-168">(KAGPROP_FILEUSAGE)</span></span></p></td>
<td><p><span data-ttu-id="33750-169">Указывает, как драйвер обрабатывает файл в источнике данных; как таблица или как каталог.</span><span class="sxs-lookup"><span data-stu-id="33750-169">Indicates how the driver treats a file in a data source; as a table or as a catalog.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-170">Как оператор escape</span><span class="sxs-lookup"><span data-stu-id="33750-170">Like Escape Clause</span></span><br />
<span data-ttu-id="33750-171">(КАГПРОП_ЛИКИСКАПЕКЛАУСЕ)</span><span class="sxs-lookup"><span data-stu-id="33750-171">(KAGPROP_LIKEESCAPECLAUSE)</span></span></p></td>
<td><p><span data-ttu-id="33750-172">Указывает, поддерживает ли драйвер определение и использование escape-символа для знака процента (%) и подчеркнуть символ (_) в предикате LIKE предложения WHERE.</span><span class="sxs-lookup"><span data-stu-id="33750-172">Indicates whether the driver supports the definition and use of an escape character for the percent character (%) and underline character (_) in the LIKE predicate of a WHERE clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-173">Максимальное число столбцов в группе Group By</span><span class="sxs-lookup"><span data-stu-id="33750-173">Max Columns in Group By</span></span><br />
<span data-ttu-id="33750-174">(КАГПРОП_МАКСКОЛУМНСИНГРАУПБИ)</span><span class="sxs-lookup"><span data-stu-id="33750-174">(KAGPROP_MAXCOLUMNSINGROUPBY)</span></span></p></td>
<td><p><span data-ttu-id="33750-175">Указывает максимальное количество столбцов, которое может быть указано в предложении GROUP BY оператора SELECT.</span><span class="sxs-lookup"><span data-stu-id="33750-175">Indicates the maximum number of columns that can be listed in the GROUP BY clause of a SELECT statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-176">Максимальное число столбцов в индексе</span><span class="sxs-lookup"><span data-stu-id="33750-176">Max Columns in Index</span></span><br />
<span data-ttu-id="33750-177">(КАГПРОП_МАКСКОЛУМНСИНИНДЕКС)</span><span class="sxs-lookup"><span data-stu-id="33750-177">(KAGPROP_MAXCOLUMNSININDEX)</span></span></p></td>
<td><p><span data-ttu-id="33750-178">Указывает максимальное число столбцов, которые можно включить в индекс.</span><span class="sxs-lookup"><span data-stu-id="33750-178">Indicates the maximum number of columns that can be included in an index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-179">Максимальное число столбцов в упорядочении по</span><span class="sxs-lookup"><span data-stu-id="33750-179">Max Columns in Order By</span></span><br />
<span data-ttu-id="33750-180">(КАГПРОП_МАКСКОЛУМНСИНОРДЕРБИ)</span><span class="sxs-lookup"><span data-stu-id="33750-180">(KAGPROP_MAXCOLUMNSINORDERBY)</span></span></p></td>
<td><p><span data-ttu-id="33750-181">Указывает максимальное количество столбцов, которое может быть указано в предложении ORDER BY оператора SELECT.</span><span class="sxs-lookup"><span data-stu-id="33750-181">Indicates the maximum number of columns that can be listed in the ORDER BY clause of a SELECT statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-182">Максимальное число столбцов в SELECT</span><span class="sxs-lookup"><span data-stu-id="33750-182">Max Columns in Select</span></span><br />
<span data-ttu-id="33750-183">(КАГПРОП_МАКСКОЛУМНСИНСЕЛЕКТ)</span><span class="sxs-lookup"><span data-stu-id="33750-183">(KAGPROP_MAXCOLUMNSINSELECT)</span></span></p></td>
<td><p><span data-ttu-id="33750-184">Указывает максимальное количество столбцов, которое может быть указано в части SELECT оператора SELECT.</span><span class="sxs-lookup"><span data-stu-id="33750-184">Indicates the maximum number of columns that can be listed in the SELECT portion of a SELECT statement.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-185">Максимальное число столбцов в таблице</span><span class="sxs-lookup"><span data-stu-id="33750-185">Max Columns in Table</span></span><br />
<span data-ttu-id="33750-186">(КАГПРОП_МАКСКОЛУМНСИНТАБЛЕ)</span><span class="sxs-lookup"><span data-stu-id="33750-186">(KAGPROP_MAXCOLUMNSINTABLE)</span></span></p></td>
<td><p><span data-ttu-id="33750-187">Указывает максимальное допустимое количество столбцов в таблице.</span><span class="sxs-lookup"><span data-stu-id="33750-187">Indicates the maximum number of columns allowed in a table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-188">Числовые функции</span><span class="sxs-lookup"><span data-stu-id="33750-188">Numeric Functions</span></span><br />
<span data-ttu-id="33750-189">(КАГПРОП_НУМЕРИКФУНКТИОНС)</span><span class="sxs-lookup"><span data-stu-id="33750-189">(KAGPROP_NUMERICFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="33750-190">Указывает, какие числовые функции поддерживаются драйвером ODBC.</span><span class="sxs-lookup"><span data-stu-id="33750-190">Indicates which numeric functions are supported by the ODBC driver.</span></span> <span data-ttu-id="33750-191">Список имен функций и соответствующих значений, используемых в этой битовой маске, приведен в разделе приложение E: скалярные функции в документации ODBC.</span><span class="sxs-lookup"><span data-stu-id="33750-191">For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-192">Возможности внешнего соединения</span><span class="sxs-lookup"><span data-stu-id="33750-192">Outer Join Capabilities</span></span><br />
<span data-ttu-id="33750-193">(КАГПРОП_ОЖКАПАБИЛИТИ)</span><span class="sxs-lookup"><span data-stu-id="33750-193">(KAGPROP_OJCAPABILITY)</span></span></p></td>
<td><p><span data-ttu-id="33750-194">Указывает типы внешних ОБЪЕДИНЕНий, поддерживаемые поставщиком.</span><span class="sxs-lookup"><span data-stu-id="33750-194">Indicates the types of OUTER JOINs supported by the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-195">Внешние соединения</span><span class="sxs-lookup"><span data-stu-id="33750-195">Outer Joins</span></span><br />
<span data-ttu-id="33750-196">(КАГПРОП_АУТЕРЖОИНС)</span><span class="sxs-lookup"><span data-stu-id="33750-196">(KAGPROP_OUTERJOINS)</span></span></p></td>
<td><p><span data-ttu-id="33750-197">Указывает, поддерживает ли поставщик внешние соединения.</span><span class="sxs-lookup"><span data-stu-id="33750-197">Indicates whether the provider supports OUTER JOINs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-198">Специальные символы</span><span class="sxs-lookup"><span data-stu-id="33750-198">Special Characters</span></span><br />
<span data-ttu-id="33750-199">(КАГПРОП_СПЕЦИАЛЧАРАКТЕРС)</span><span class="sxs-lookup"><span data-stu-id="33750-199">(KAGPROP_SPECIALCHARACTERS)</span></span></p></td>
<td><p><span data-ttu-id="33750-200">Указывает, какие символы имеют особое значение для драйвера ODBC.</span><span class="sxs-lookup"><span data-stu-id="33750-200">Indicates which characters have special meaning for the ODBC driver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-201">Хранимые процедуры</span><span class="sxs-lookup"><span data-stu-id="33750-201">Stored Procedures</span></span><br />
<span data-ttu-id="33750-202">(КАГПРОП_ПРОЦЕДУРЕС)</span><span class="sxs-lookup"><span data-stu-id="33750-202">(KAGPROP_PROCEDURES)</span></span></p></td>
<td><p><span data-ttu-id="33750-203">Указывает, доступны ли хранимые процедуры для использования с данным драйвером ODBC.</span><span class="sxs-lookup"><span data-stu-id="33750-203">Indicates whether stored procedures are available for use with this ODBC driver.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-204">Строковые функции</span><span class="sxs-lookup"><span data-stu-id="33750-204">String Functions</span></span><br />
<span data-ttu-id="33750-205">(КАГПРОП_СТРИНГФУНКТИОНС)</span><span class="sxs-lookup"><span data-stu-id="33750-205">(KAGPROP_STRINGFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="33750-206">Указывает, какие строковые функции поддерживаются драйвером ODBC.</span><span class="sxs-lookup"><span data-stu-id="33750-206">Indicates which string functions are supported by the ODBC driver.</span></span> <span data-ttu-id="33750-207">Список имен функций и соответствующих значений, используемых в этой битовой маске, приведен в разделе приложение E: скалярные функции в документации ODBC.</span><span class="sxs-lookup"><span data-stu-id="33750-207">For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-208">Системные функции</span><span class="sxs-lookup"><span data-stu-id="33750-208">System Functions</span></span><br />
<span data-ttu-id="33750-209">(КАГПРОП_СИСТЕМФУНКТИОНС)</span><span class="sxs-lookup"><span data-stu-id="33750-209">(KAGPROP_SYSTEMFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="33750-210">Указывает, какие системные функции поддерживаются драйвером ODBC.</span><span class="sxs-lookup"><span data-stu-id="33750-210">Indicates which system functions are supported by the ODBC driver.</span></span> <span data-ttu-id="33750-211">Список имен функций и соответствующих значений, используемых в этой битовой маске, приведен в разделе приложение E: скалярные функции в документации ODBC.</span><span class="sxs-lookup"><span data-stu-id="33750-211">For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-212">Функции времени и даты</span><span class="sxs-lookup"><span data-stu-id="33750-212">Time/Date Functions</span></span><br />
<span data-ttu-id="33750-213">(КАГПРОП_ТИМЕДАТЕФУНКТИОНС)</span><span class="sxs-lookup"><span data-stu-id="33750-213">(KAGPROP_TIMEDATEFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="33750-214">Указывает, какие функции времени и даты поддерживаются драйвером ODBC.</span><span class="sxs-lookup"><span data-stu-id="33750-214">Indicates which time and date functions are supported by the ODBC driver.</span></span> <span data-ttu-id="33750-215">Список имен функций и соответствующих значений, используемых в этой битовой маске, приведен в разделе приложение E: скалярные функции в документации ODBC.</span><span class="sxs-lookup"><span data-stu-id="33750-215">For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-216">Поддержка грамматики SQL</span><span class="sxs-lookup"><span data-stu-id="33750-216">SQL Grammar Support</span></span><br />
<span data-ttu-id="33750-217">(КАГПРОП_ОДБКСКЛКОНФОРМАНЦЕ)</span><span class="sxs-lookup"><span data-stu-id="33750-217">(KAGPROP_ODBCSQLCONFORMANCE)</span></span></p></td>
<td><p><span data-ttu-id="33750-218">Указывает грамматику SQL, поддерживаемую драйвером ODBC.</span><span class="sxs-lookup"><span data-stu-id="33750-218">Indicates the SQL grammar that the ODBC driver supports.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-recordset-and-command-properties"></a><span data-ttu-id="33750-219">Специфические для поставщика наборы записей и свойства команд</span><span class="sxs-lookup"><span data-stu-id="33750-219">Provider-Specific Recordset and Command Properties</span></span>

<span data-ttu-id="33750-220">Поставщик OLE DB для ODBC добавляет несколько свойств в коллекцию **свойств** объекта **Recordset** и командных объектов \*\*\*\* .</span><span class="sxs-lookup"><span data-stu-id="33750-220">The OLE DB provider for ODBC adds several properties to the **Properties** collection of the **Recordset** and **Command** objects.</span></span> <span data-ttu-id="33750-221">В приведенной ниже таблице указаны эти свойства с соответствующим именем свойства OLE DB в круглых скобках.</span><span class="sxs-lookup"><span data-stu-id="33750-221">The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="33750-222">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="33750-222">Property Name</span></span></p></th>
<th><p><span data-ttu-id="33750-223">Описание</span><span class="sxs-lookup"><span data-stu-id="33750-223">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="33750-224">Обновления, операции удаления и вставки на основе запросов</span><span class="sxs-lookup"><span data-stu-id="33750-224">Query Based Updates/Deletes/Inserts</span></span><br />
<span data-ttu-id="33750-225">(КАГПРОП_КУЕРИБАСЕДУПДАТЕС)</span><span class="sxs-lookup"><span data-stu-id="33750-225">(KAGPROP_QUERYBASEDUPDATES)</span></span></p></td>
<td><p><span data-ttu-id="33750-226">Указывает, можно ли выполнять операции обновления, удаления и вставки с помощью запросов SQL.</span><span class="sxs-lookup"><span data-stu-id="33750-226">Indicates whether updates, deletions, and insertions can be performed using SQL queries.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-227">Тип параллелизма ODBC</span><span class="sxs-lookup"><span data-stu-id="33750-227">ODBC Concurrency Type</span></span><br />
<span data-ttu-id="33750-228">(КАГПРОП_КОНКУРРЕНЦИ)</span><span class="sxs-lookup"><span data-stu-id="33750-228">(KAGPROP_CONCURRENCY)</span></span></p></td>
<td><p><span data-ttu-id="33750-229">Указывает метод, используемый для сокращения возможных проблем, вызванных двумя пользователями, пытающимися одновременно получить доступ к одним и тем же данным из источника данных.</span><span class="sxs-lookup"><span data-stu-id="33750-229">Indicates the method used to reduce potential problems caused by two users attempting to access the same data from the data source simultaneously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-230">Доступность BLOB-объектов для одноНаправленного курсора</span><span class="sxs-lookup"><span data-stu-id="33750-230">BLOB accessibility on Forward-Only cursor</span></span><br />
<span data-ttu-id="33750-231">(КАГПРОП_БЛОБСОНФОКУРСОР)</span><span class="sxs-lookup"><span data-stu-id="33750-231">(KAGPROP_BLOBSONFOCURSOR)</span></span></p></td>
<td><p><span data-ttu-id="33750-232">Указывает, можно ли получить доступ к <strong>полям</strong> BLOB при использовании однонаправленного курсора.</span><span class="sxs-lookup"><span data-stu-id="33750-232">Indicates whether BLOB <strong>Fields</strong> can be accessed when using a forward-only cursor.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-233">Включение СКЛ_ФЛОАТ, СКЛ_ДАУБЛЕ и СКЛ_РЕАЛ в КБУ WHERE предложений</span><span class="sxs-lookup"><span data-stu-id="33750-233">Include SQL_FLOAT, SQL_DOUBLE, and SQL_REAL in QBU WHERE clauses</span></span><br />
<span data-ttu-id="33750-234">(КАГПРОП_ИНКЛУДЕНОНЕКСАКТ)</span><span class="sxs-lookup"><span data-stu-id="33750-234">(KAGPROP_INCLUDENONEXACT)</span></span></p></td>
<td><p><span data-ttu-id="33750-235">Указывает, могут ли значения СКЛ_ФЛОАТ, СКЛ_ДАУБЛЕ и СКЛ_РЕАЛ включаться в предложение WHERE КБУ.</span><span class="sxs-lookup"><span data-stu-id="33750-235">Indicates whether SQL_FLOAT, SQL_DOUBLE, and SQL_REAL values can be included in a QBU WHERE clause.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-236">Положение в последней строке после вставки</span><span class="sxs-lookup"><span data-stu-id="33750-236">Position on the last row after insert</span></span><br />
<span data-ttu-id="33750-237">(КАГПРОП_ПОСИТИОНОННЕВРОВ)</span><span class="sxs-lookup"><span data-stu-id="33750-237">(KAGPROP_POSITIONONNEWROW)</span></span></p></td>
<td><p><span data-ttu-id="33750-238">Указывает, что после вставки новой записи в таблицу текущая строка будет получена из последней строки таблицы.</span><span class="sxs-lookup"><span data-stu-id="33750-238">Indicates that after a new record has been inserted in a table, the last row in the table will be come the current row.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-239">Ировсетчанжеекстинфо</span><span class="sxs-lookup"><span data-stu-id="33750-239">IRowsetChangeExtInfo</span></span><br />
<span data-ttu-id="33750-240">(КАГПРОП_ИРОВСЕТЧАНЖЕЕКСТИНФО)</span><span class="sxs-lookup"><span data-stu-id="33750-240">(KAGPROP_IROWSETCHANGEEXTINFO)</span></span></p></td>
<td><p><span data-ttu-id="33750-241">Указывает, предоставляет ли интерфейс <strong>ировсетчанже</strong> расширенную поддержку информации.</span><span class="sxs-lookup"><span data-stu-id="33750-241">Indicates whether the <strong>IRowsetChange</strong> interface provides extended information support.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-242">Тип курсора ODBC</span><span class="sxs-lookup"><span data-stu-id="33750-242">ODBC Cursor Type</span></span><br />
<span data-ttu-id="33750-243">(КАГПРОП_КУРСОР)</span><span class="sxs-lookup"><span data-stu-id="33750-243">(KAGPROP_CURSOR)</span></span></p></td>
<td><p><span data-ttu-id="33750-244">Указывает тип курсора, используемого в объекте <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="33750-244">Indicates the type of cursor used by the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-245">Создание набора строк, который может быть маршалирован</span><span class="sxs-lookup"><span data-stu-id="33750-245">Generate a Rowset that can be marshaled</span></span><br />
<span data-ttu-id="33750-246">(КАГПРОП_МАРШАЛЛАБЛЕ)</span><span class="sxs-lookup"><span data-stu-id="33750-246">(KAGPROP_MARSHALLABLE)</span></span></p></td>
<td><p><span data-ttu-id="33750-247">Указывает, что драйвер ODBC создает объект Recordset, который может быть маршалирован</span><span class="sxs-lookup"><span data-stu-id="33750-247">Indicates that the ODBC driver generates a recordset that can be marshaled</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-text"></a><span data-ttu-id="33750-248">Текст команды</span><span class="sxs-lookup"><span data-stu-id="33750-248">Command Text</span></span>

<span data-ttu-id="33750-249">Способ использования объекта [Command](command-object-ado.md) во многом зависит от источника данных, а также от того, какой тип запроса или оператора команды будет принимать.</span><span class="sxs-lookup"><span data-stu-id="33750-249">How you use the [Command](command-object-ado.md) object largely depends on the data source, and what type of query or command statement it will accept.</span></span>

<span data-ttu-id="33750-250">ODBC предоставляет специальный синтаксис для вызова хранимых процедур.</span><span class="sxs-lookup"><span data-stu-id="33750-250">ODBC provides a specific syntax for calling stored procedures.</span></span> <span data-ttu-id="33750-251">Для свойства [CommandText](commandtext-property-ado.md) объекта **Command** , аргумент *CommandText* для метода **EXECUTE** объекта [Connection](connection-object-ado.md) или аргумент *Source* для метода **Open** объекта [Recordset](recordset-object-ado.md) Объект, передаваемый в строку с помощью следующего синтаксиса:</span><span class="sxs-lookup"><span data-stu-id="33750-251">For the [CommandText](commandtext-property-ado.md) property of a **Command** object, the *CommandText* argument to the **Execute** method on a [Connection](connection-object-ado.md) object, or the *Source* argument to the **Open** method on a [Recordset](recordset-object-ado.md) object, passes in a string with this syntax:</span></span>

`"{ [ ? = ] call procedure [ ( ? [, ? [ ,  ]] ) ] }"`

<span data-ttu-id="33750-252">Каждый \*\*\*\* из них</span><span class="sxs-lookup"><span data-stu-id="33750-252">Each **?**</span></span> <span data-ttu-id="33750-253">ссылается на объект в коллекции [Parameters](parameters-collection-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="33750-253">references an object in the [Parameters](parameters-collection-ado.md) collection.</span></span> <span data-ttu-id="33750-254">Первый **?**</span><span class="sxs-lookup"><span data-stu-id="33750-254">The first **?**</span></span> <span data-ttu-id="33750-255">**Параметры**References (0), следующие **?**</span><span class="sxs-lookup"><span data-stu-id="33750-255">references **Parameters**(0), the next **?**</span></span> <span data-ttu-id="33750-256">ссылки на **Параметры**(1) и т. д.</span><span class="sxs-lookup"><span data-stu-id="33750-256">references **Parameters**(1), and so on.</span></span>

<span data-ttu-id="33750-257">Ссылки на параметры являются необязательными и зависят от структуры хранимой процедуры.</span><span class="sxs-lookup"><span data-stu-id="33750-257">The parameter references are optional and depend on the structure of the stored procedure.</span></span> <span data-ttu-id="33750-258">Если вы хотите вызвать хранимую процедуру, которая не определяет параметры, строка будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="33750-258">If you want to call a stored procedure that defines no parameters, your string would look like this:</span></span>

`"{ call procedure }"`

<span data-ttu-id="33750-259">Если у вас есть два параметра запроса, строка будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="33750-259">If you have two query parameters, your string would look like this:</span></span>

`"{ call procedure ( ?, ? ) }"`

<span data-ttu-id="33750-260">Если хранимая процедура будет возвращать значение, возвращаемое значение будет считаться другим параметром.</span><span class="sxs-lookup"><span data-stu-id="33750-260">If the stored procedure will return a value, the return value is treated as another parameter.</span></span> <span data-ttu-id="33750-261">Если у вас нет параметров запроса, но у вас есть возвращаемое значение, строка будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="33750-261">If you have no query parameters but you do have a return value, your string would look like this:</span></span>

`"{ ? = call procedure }"`

<span data-ttu-id="33750-262">Наконец, если у вас есть возвращаемое значение и два параметра запроса, строка будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="33750-262">Finally, if you have a return value and two query parameters, your string would look like this:</span></span>

`"{ ? = call procedure ( ?, ? ) }"`

## <a name="recordset-behavior"></a><span data-ttu-id="33750-263">Поведение набора записей</span><span class="sxs-lookup"><span data-stu-id="33750-263">Recordset Behavior</span></span>

<span data-ttu-id="33750-264">В следующих таблицах перечислены стандартные методы и свойства ADO, доступные для объекта **Recordset** , открытого с помощью этого поставщика.</span><span class="sxs-lookup"><span data-stu-id="33750-264">The following tables list the standard ADO methods and properties available on a **Recordset** object opened with this provider.</span></span>

<span data-ttu-id="33750-265">Для получения более подробных сведений о поведении **набора записей** для конфигурации поставщика [](supports-method-ado.md) запустите метод Supports и перечислите коллекцию **свойств** объекта **Recordset** , чтобы определить, зависит ли от поставщика динамический имеются свойства.</span><span class="sxs-lookup"><span data-stu-id="33750-265">For more detailed information about **Recordset** behavior for your provider configuration, run the [Supports](supports-method-ado.md) method and enumerate the **Properties** collection of the **Recordset** to determine whether provider-specific dynamic properties are present.</span></span>

<span data-ttu-id="33750-266">Доступность стандартных свойств **записей** ADO:</span><span class="sxs-lookup"><span data-stu-id="33750-266">Availability of standard ADO **Recordset** properties:</span></span>

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
<th><p><span data-ttu-id="33750-267">Свойство</span><span class="sxs-lookup"><span data-stu-id="33750-267">Property</span></span></p></th>
<th><p><span data-ttu-id="33750-268">Форвардонли</span><span class="sxs-lookup"><span data-stu-id="33750-268">ForwardOnly</span></span></p></th>
<th><p><span data-ttu-id="33750-269">Динамическая группа</span><span class="sxs-lookup"><span data-stu-id="33750-269">Dynamic</span></span></p></th>
<th><p><span data-ttu-id="33750-270">Сохранен</span><span class="sxs-lookup"><span data-stu-id="33750-270">Keyset</span></span></p></th>
<th><p><span data-ttu-id="33750-271">Static</span><span class="sxs-lookup"><span data-stu-id="33750-271">Static</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="33750-272"><a href="absolutepage-property-ado.md">AbsolutePage</a></span><span class="sxs-lookup"><span data-stu-id="33750-272"><a href="absolutepage-property-ado.md">AbsolutePage</a></span></span></p></td>
<td><p><span data-ttu-id="33750-273">недоступно</span><span class="sxs-lookup"><span data-stu-id="33750-273">not available</span></span></p></td>
<td><p><span data-ttu-id="33750-274">недоступно</span><span class="sxs-lookup"><span data-stu-id="33750-274">not available</span></span></p></td>
<td><p><span data-ttu-id="33750-275">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="33750-275">read/write</span></span></p></td>
<td><p><span data-ttu-id="33750-276">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="33750-276">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-277"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span><span class="sxs-lookup"><span data-stu-id="33750-277"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span></span></p></td>
<td><p><span data-ttu-id="33750-278">недоступно</span><span class="sxs-lookup"><span data-stu-id="33750-278">not available</span></span></p></td>
<td><p><span data-ttu-id="33750-279">недоступно</span><span class="sxs-lookup"><span data-stu-id="33750-279">not available</span></span></p></td>
<td><p><span data-ttu-id="33750-280">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="33750-280">read/write</span></span></p></td>
<td><p><span data-ttu-id="33750-281">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="33750-281">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-282"><a href="activeconnection-property-ado.md">ActiveConnection</a></span><span class="sxs-lookup"><span data-stu-id="33750-282"><a href="activeconnection-property-ado.md">ActiveConnection</a></span></span></p></td>
<td><p><span data-ttu-id="33750-283">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="33750-283">read/write</span></span></p></td>
<td><p><span data-ttu-id="33750-284">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="33750-284">read/write</span></span></p></td>
<td><p><span data-ttu-id="33750-285">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="33750-285">read/write</span></span></p></td>
<td><p><span data-ttu-id="33750-286">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="33750-286">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-287"><a href="bof-eof-properties-ado.md">BOF</a></span><span class="sxs-lookup"><span data-stu-id="33750-287"><a href="bof-eof-properties-ado.md">BOF</a></span></span></p></td>
<td><p><span data-ttu-id="33750-288">только для чтения</span><span class="sxs-lookup"><span data-stu-id="33750-288">read-only</span></span></p></td>
<td><p><span data-ttu-id="33750-289">только для чтения</span><span class="sxs-lookup"><span data-stu-id="33750-289">read-only</span></span></p></td>
<td><p><span data-ttu-id="33750-290">только для чтения</span><span class="sxs-lookup"><span data-stu-id="33750-290">read-only</span></span></p></td>
<td><p><span data-ttu-id="33750-291">только для чтения</span><span class="sxs-lookup"><span data-stu-id="33750-291">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-292"><a href="bookmark-property-ado.md">Bookmark</a></span><span class="sxs-lookup"><span data-stu-id="33750-292"><a href="bookmark-property-ado.md">Bookmark</a></span></span></p></td>
<td><p><span data-ttu-id="33750-293">недоступно</span><span class="sxs-lookup"><span data-stu-id="33750-293">not available</span></span></p></td>
<td><p><span data-ttu-id="33750-294">недоступно</span><span class="sxs-lookup"><span data-stu-id="33750-294">not available</span></span></p></td>
<td><p><span data-ttu-id="33750-295">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="33750-295">read/write</span></span></p></td>
<td><p><span data-ttu-id="33750-296">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="33750-296">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-297"><a href="cachesize-property-ado.md">CacheSize</a></span><span class="sxs-lookup"><span data-stu-id="33750-297"><a href="cachesize-property-ado.md">CacheSize</a></span></span></p></td>
<td><p><span data-ttu-id="33750-298">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="33750-298">read/write</span></span></p></td>
<td><p><span data-ttu-id="33750-299">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="33750-299">read/write</span></span></p></td>
<td><p><span data-ttu-id="33750-300">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="33750-300">read/write</span></span></p></td>
<td><p><span data-ttu-id="33750-301">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="33750-301">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-302"><a href="cursorlocation-property-ado.md">CursorLocation</a></span><span class="sxs-lookup"><span data-stu-id="33750-302"><a href="cursorlocation-property-ado.md">CursorLocation</a></span></span></p></td>
<td><p><span data-ttu-id="33750-303">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="33750-303">read/write</span></span></p></td>
<td><p><span data-ttu-id="33750-304">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="33750-304">read/write</span></span></p></td>
<td><p><span data-ttu-id="33750-305">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="33750-305">read/write</span></span></p></td>
<td><p><span data-ttu-id="33750-306">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="33750-306">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-307"><a href="cursortype-property-ado.md">CursorType</a></span><span class="sxs-lookup"><span data-stu-id="33750-307"><a href="cursortype-property-ado.md">CursorType</a></span></span></p></td>
<td><p><span data-ttu-id="33750-308">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="33750-308">read/write</span></span></p></td>
<td><p><span data-ttu-id="33750-309">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="33750-309">read/write</span></span></p></td>
<td><p><span data-ttu-id="33750-310">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="33750-310">read/write</span></span></p></td>
<td><p><span data-ttu-id="33750-311">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="33750-311">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-312"><a href="editmode-property-ado.md">EditMode</a></span><span class="sxs-lookup"><span data-stu-id="33750-312"><a href="editmode-property-ado.md">EditMode</a></span></span></p></td>
<td><p><span data-ttu-id="33750-313">только для чтения</span><span class="sxs-lookup"><span data-stu-id="33750-313">read-only</span></span></p></td>
<td><p><span data-ttu-id="33750-314">только для чтения</span><span class="sxs-lookup"><span data-stu-id="33750-314">read-only</span></span></p></td>
<td><p><span data-ttu-id="33750-315">только для чтения</span><span class="sxs-lookup"><span data-stu-id="33750-315">read-only</span></span></p></td>
<td><p><span data-ttu-id="33750-316">только для чтения</span><span class="sxs-lookup"><span data-stu-id="33750-316">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-317"><a href="filter-property-ado.md">Filter</a></span><span class="sxs-lookup"><span data-stu-id="33750-317"><a href="filter-property-ado.md">Filter</a></span></span></p></td>
<td><p><span data-ttu-id="33750-318">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="33750-318">read/write</span></span></p></td>
<td><p><span data-ttu-id="33750-319">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="33750-319">read/write</span></span></p></td>
<td><p><span data-ttu-id="33750-320">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="33750-320">read/write</span></span></p></td>
<td><p><span data-ttu-id="33750-321">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="33750-321">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-322"><a href="locktype-property-ado.md">LockType</a></span><span class="sxs-lookup"><span data-stu-id="33750-322"><a href="locktype-property-ado.md">LockType</a></span></span></p></td>
<td><p><span data-ttu-id="33750-323">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="33750-323">read/write</span></span></p></td>
<td><p><span data-ttu-id="33750-324">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="33750-324">read/write</span></span></p></td>
<td><p><span data-ttu-id="33750-325">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="33750-325">read/write</span></span></p></td>
<td><p><span data-ttu-id="33750-326">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="33750-326">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-327"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span><span class="sxs-lookup"><span data-stu-id="33750-327"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span></span></p></td>
<td><p><span data-ttu-id="33750-328">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="33750-328">read/write</span></span></p></td>
<td><p><span data-ttu-id="33750-329">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="33750-329">read/write</span></span></p></td>
<td><p><span data-ttu-id="33750-330">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="33750-330">read/write</span></span></p></td>
<td><p><span data-ttu-id="33750-331">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="33750-331">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-332"><a href="maxrecords-property-ado.md">MaxRecords</a></span><span class="sxs-lookup"><span data-stu-id="33750-332"><a href="maxrecords-property-ado.md">MaxRecords</a></span></span></p></td>
<td><p><span data-ttu-id="33750-333">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="33750-333">read/write</span></span></p></td>
<td><p><span data-ttu-id="33750-334">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="33750-334">read/write</span></span></p></td>
<td><p><span data-ttu-id="33750-335">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="33750-335">read/write</span></span></p></td>
<td><p><span data-ttu-id="33750-336">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="33750-336">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-337"><a href="pagecount-property-ado.md">PageCount</a></span><span class="sxs-lookup"><span data-stu-id="33750-337"><a href="pagecount-property-ado.md">PageCount</a></span></span></p></td>
<td><p><span data-ttu-id="33750-338">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="33750-338">read/write</span></span></p></td>
<td><p><span data-ttu-id="33750-339">недоступно</span><span class="sxs-lookup"><span data-stu-id="33750-339">not available</span></span></p></td>
<td><p><span data-ttu-id="33750-340">только для чтения</span><span class="sxs-lookup"><span data-stu-id="33750-340">read-only</span></span></p></td>
<td><p><span data-ttu-id="33750-341">только для чтения</span><span class="sxs-lookup"><span data-stu-id="33750-341">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-342"><a href="pagesize-property-ado.md">PageSize</a></span><span class="sxs-lookup"><span data-stu-id="33750-342"><a href="pagesize-property-ado.md">PageSize</a></span></span></p></td>
<td><p><span data-ttu-id="33750-343">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="33750-343">read/write</span></span></p></td>
<td><p><span data-ttu-id="33750-344">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="33750-344">read/write</span></span></p></td>
<td><p><span data-ttu-id="33750-345">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="33750-345">read/write</span></span></p></td>
<td><p><span data-ttu-id="33750-346">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="33750-346">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-347"><a href="recordcount-property-ado.md">RecordCount</a></span><span class="sxs-lookup"><span data-stu-id="33750-347"><a href="recordcount-property-ado.md">RecordCount</a></span></span></p></td>
<td><p><span data-ttu-id="33750-348">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="33750-348">read/write</span></span></p></td>
<td><p><span data-ttu-id="33750-349">недоступно</span><span class="sxs-lookup"><span data-stu-id="33750-349">not available</span></span></p></td>
<td><p><span data-ttu-id="33750-350">только для чтения</span><span class="sxs-lookup"><span data-stu-id="33750-350">read-only</span></span></p></td>
<td><p><span data-ttu-id="33750-351">только для чтения</span><span class="sxs-lookup"><span data-stu-id="33750-351">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-352"><a href="source-property-ado-recordset.md">Source</a></span><span class="sxs-lookup"><span data-stu-id="33750-352"><a href="source-property-ado-recordset.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="33750-353">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="33750-353">read/write</span></span></p></td>
<td><p><span data-ttu-id="33750-354">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="33750-354">read/write</span></span></p></td>
<td><p><span data-ttu-id="33750-355">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="33750-355">read/write</span></span></p></td>
<td><p><span data-ttu-id="33750-356">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="33750-356">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-357"><a href="state-property-ado.md">State</a></span><span class="sxs-lookup"><span data-stu-id="33750-357"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="33750-358">только для чтения</span><span class="sxs-lookup"><span data-stu-id="33750-358">read-only</span></span></p></td>
<td><p><span data-ttu-id="33750-359">только для чтения</span><span class="sxs-lookup"><span data-stu-id="33750-359">read-only</span></span></p></td>
<td><p><span data-ttu-id="33750-360">только для чтения</span><span class="sxs-lookup"><span data-stu-id="33750-360">read-only</span></span></p></td>
<td><p><span data-ttu-id="33750-361">только для чтения</span><span class="sxs-lookup"><span data-stu-id="33750-361">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-362"><a href="status-property-ado-recordset.md">Status</a></span><span class="sxs-lookup"><span data-stu-id="33750-362"><a href="status-property-ado-recordset.md">Status</a></span></span></p></td>
<td><p><span data-ttu-id="33750-363">только для чтения</span><span class="sxs-lookup"><span data-stu-id="33750-363">read-only</span></span></p></td>
<td><p><span data-ttu-id="33750-364">только для чтения</span><span class="sxs-lookup"><span data-stu-id="33750-364">read-only</span></span></p></td>
<td><p><span data-ttu-id="33750-365">только для чтения</span><span class="sxs-lookup"><span data-stu-id="33750-365">read-only</span></span></p></td>
<td><p><span data-ttu-id="33750-366">только для чтения</span><span class="sxs-lookup"><span data-stu-id="33750-366">read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="33750-367">Свойства [AbsolutePosition](absoluteposition-property-ado.md) и [AbsolutePage](absolutepage-property-ado.md) доступны только для записи при использовании ADO с поставщиком Microsoft OLE DB для ODBC версии 1,0.</span><span class="sxs-lookup"><span data-stu-id="33750-367">The [AbsolutePosition](absoluteposition-property-ado.md) and [AbsolutePage](absolutepage-property-ado.md) properties are write-only when ADO is used with version 1.0 of the Microsoft OLE DB Provider for ODBC.</span></span>

<span data-ttu-id="33750-368">Доступность стандартных методов **набора записей** ADO:</span><span class="sxs-lookup"><span data-stu-id="33750-368">Availability of standard ADO **Recordset** methods:</span></span>

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
<th><p><span data-ttu-id="33750-369">Метод</span><span class="sxs-lookup"><span data-stu-id="33750-369">Method</span></span></p></th>
<th><p><span data-ttu-id="33750-370">Форвардонли</span><span class="sxs-lookup"><span data-stu-id="33750-370">ForwardOnly</span></span></p></th>
<th><p><span data-ttu-id="33750-371">Динамическая группа</span><span class="sxs-lookup"><span data-stu-id="33750-371">Dynamic</span></span></p></th>
<th><p><span data-ttu-id="33750-372">Сохранен</span><span class="sxs-lookup"><span data-stu-id="33750-372">Keyset</span></span></p></th>
<th><p><span data-ttu-id="33750-373">Static</span><span class="sxs-lookup"><span data-stu-id="33750-373">Static</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="33750-374"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="33750-374"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="33750-375">Да</span><span class="sxs-lookup"><span data-stu-id="33750-375">Yes</span></span></p></td>
<td><p><span data-ttu-id="33750-376">Да</span><span class="sxs-lookup"><span data-stu-id="33750-376">Yes</span></span></p></td>
<td><p><span data-ttu-id="33750-377">Да</span><span class="sxs-lookup"><span data-stu-id="33750-377">Yes</span></span></p></td>
<td><p><span data-ttu-id="33750-378">Да</span><span class="sxs-lookup"><span data-stu-id="33750-378">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-379"><a href="cancel-method-ado.md">Отмена</a></span><span class="sxs-lookup"><span data-stu-id="33750-379"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="33750-380">Да</span><span class="sxs-lookup"><span data-stu-id="33750-380">Yes</span></span></p></td>
<td><p><span data-ttu-id="33750-381">Да</span><span class="sxs-lookup"><span data-stu-id="33750-381">Yes</span></span></p></td>
<td><p><span data-ttu-id="33750-382">Да</span><span class="sxs-lookup"><span data-stu-id="33750-382">Yes</span></span></p></td>
<td><p><span data-ttu-id="33750-383">Да</span><span class="sxs-lookup"><span data-stu-id="33750-383">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-384"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="33750-384"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="33750-385">Да</span><span class="sxs-lookup"><span data-stu-id="33750-385">Yes</span></span></p></td>
<td><p><span data-ttu-id="33750-386">Да</span><span class="sxs-lookup"><span data-stu-id="33750-386">Yes</span></span></p></td>
<td><p><span data-ttu-id="33750-387">Да</span><span class="sxs-lookup"><span data-stu-id="33750-387">Yes</span></span></p></td>
<td><p><span data-ttu-id="33750-388">Да</span><span class="sxs-lookup"><span data-stu-id="33750-388">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-389"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="33750-389"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="33750-390">Да</span><span class="sxs-lookup"><span data-stu-id="33750-390">Yes</span></span></p></td>
<td><p><span data-ttu-id="33750-391">Да</span><span class="sxs-lookup"><span data-stu-id="33750-391">Yes</span></span></p></td>
<td><p><span data-ttu-id="33750-392">Да</span><span class="sxs-lookup"><span data-stu-id="33750-392">Yes</span></span></p></td>
<td><p><span data-ttu-id="33750-393">Да</span><span class="sxs-lookup"><span data-stu-id="33750-393">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-394"><a href="clone-method-ado.md">Clone</a></span><span class="sxs-lookup"><span data-stu-id="33750-394"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="33750-395">Нет</span><span class="sxs-lookup"><span data-stu-id="33750-395">No</span></span></p></td>
<td><p><span data-ttu-id="33750-396">Нет</span><span class="sxs-lookup"><span data-stu-id="33750-396">No</span></span></p></td>
<td><p><span data-ttu-id="33750-397">Да</span><span class="sxs-lookup"><span data-stu-id="33750-397">Yes</span></span></p></td>
<td><p><span data-ttu-id="33750-398">Да</span><span class="sxs-lookup"><span data-stu-id="33750-398">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-399"><a href="close-method-ado.md">Close</a></span><span class="sxs-lookup"><span data-stu-id="33750-399"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="33750-400">Да</span><span class="sxs-lookup"><span data-stu-id="33750-400">Yes</span></span></p></td>
<td><p><span data-ttu-id="33750-401">Да</span><span class="sxs-lookup"><span data-stu-id="33750-401">Yes</span></span></p></td>
<td><p><span data-ttu-id="33750-402">Да</span><span class="sxs-lookup"><span data-stu-id="33750-402">Yes</span></span></p></td>
<td><p><span data-ttu-id="33750-403">Да</span><span class="sxs-lookup"><span data-stu-id="33750-403">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-404"><a href="delete-method-ado-recordset.md">удаление</a>;</span><span class="sxs-lookup"><span data-stu-id="33750-404"><a href="delete-method-ado-recordset.md">Delete</a></span></span></p></td>
<td><p><span data-ttu-id="33750-405">Да</span><span class="sxs-lookup"><span data-stu-id="33750-405">Yes</span></span></p></td>
<td><p><span data-ttu-id="33750-406">Да</span><span class="sxs-lookup"><span data-stu-id="33750-406">Yes</span></span></p></td>
<td><p><span data-ttu-id="33750-407">Да</span><span class="sxs-lookup"><span data-stu-id="33750-407">Yes</span></span></p></td>
<td><p><span data-ttu-id="33750-408">Да</span><span class="sxs-lookup"><span data-stu-id="33750-408">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-409"><a href="getrows-method-ado.md">GetRows</a></span><span class="sxs-lookup"><span data-stu-id="33750-409"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="33750-410">Да</span><span class="sxs-lookup"><span data-stu-id="33750-410">Yes</span></span></p></td>
<td><p><span data-ttu-id="33750-411">Да</span><span class="sxs-lookup"><span data-stu-id="33750-411">Yes</span></span></p></td>
<td><p><span data-ttu-id="33750-412">Да</span><span class="sxs-lookup"><span data-stu-id="33750-412">Yes</span></span></p></td>
<td><p><span data-ttu-id="33750-413">Да</span><span class="sxs-lookup"><span data-stu-id="33750-413">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-414"><a href="move-method-ado.md">Move</a></span><span class="sxs-lookup"><span data-stu-id="33750-414"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="33750-415">Да</span><span class="sxs-lookup"><span data-stu-id="33750-415">Yes</span></span></p></td>
<td><p><span data-ttu-id="33750-416">Да</span><span class="sxs-lookup"><span data-stu-id="33750-416">Yes</span></span></p></td>
<td><p><span data-ttu-id="33750-417">Да</span><span class="sxs-lookup"><span data-stu-id="33750-417">Yes</span></span></p></td>
<td><p><span data-ttu-id="33750-418">Да</span><span class="sxs-lookup"><span data-stu-id="33750-418">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-419"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span><span class="sxs-lookup"><span data-stu-id="33750-419"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span></span></p></td>
<td><p><span data-ttu-id="33750-420">Да</span><span class="sxs-lookup"><span data-stu-id="33750-420">Yes</span></span></p></td>
<td><p><span data-ttu-id="33750-421">Да</span><span class="sxs-lookup"><span data-stu-id="33750-421">Yes</span></span></p></td>
<td><p><span data-ttu-id="33750-422">Да</span><span class="sxs-lookup"><span data-stu-id="33750-422">Yes</span></span></p></td>
<td><p><span data-ttu-id="33750-423">Да</span><span class="sxs-lookup"><span data-stu-id="33750-423">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-424"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span><span class="sxs-lookup"><span data-stu-id="33750-424"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span></span></p></td>
<td><p><span data-ttu-id="33750-425">Нет</span><span class="sxs-lookup"><span data-stu-id="33750-425">No</span></span></p></td>
<td><p><span data-ttu-id="33750-426">Да</span><span class="sxs-lookup"><span data-stu-id="33750-426">Yes</span></span></p></td>
<td><p><span data-ttu-id="33750-427">Да</span><span class="sxs-lookup"><span data-stu-id="33750-427">Yes</span></span></p></td>
<td><p><span data-ttu-id="33750-428">Да</span><span class="sxs-lookup"><span data-stu-id="33750-428">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-429"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span><span class="sxs-lookup"><span data-stu-id="33750-429"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span></span></p></td>
<td><p><span data-ttu-id="33750-430">Да</span><span class="sxs-lookup"><span data-stu-id="33750-430">Yes</span></span></p></td>
<td><p><span data-ttu-id="33750-431">Да</span><span class="sxs-lookup"><span data-stu-id="33750-431">Yes</span></span></p></td>
<td><p><span data-ttu-id="33750-432">Да</span><span class="sxs-lookup"><span data-stu-id="33750-432">Yes</span></span></p></td>
<td><p><span data-ttu-id="33750-433">Да</span><span class="sxs-lookup"><span data-stu-id="33750-433">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-434"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span><span class="sxs-lookup"><span data-stu-id="33750-434"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span></span></p></td>
<td><p><span data-ttu-id="33750-435">Нет</span><span class="sxs-lookup"><span data-stu-id="33750-435">No</span></span></p></td>
<td><p><span data-ttu-id="33750-436">Да</span><span class="sxs-lookup"><span data-stu-id="33750-436">Yes</span></span></p></td>
<td><p><span data-ttu-id="33750-437">Да</span><span class="sxs-lookup"><span data-stu-id="33750-437">Yes</span></span></p></td>
<td><p><span data-ttu-id="33750-438">Да</span><span class="sxs-lookup"><span data-stu-id="33750-438">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-439"><a href="nextrecordset-method-ado.md">NextRecordset</a>\*</span><span class="sxs-lookup"><span data-stu-id="33750-439"><a href="nextrecordset-method-ado.md">NextRecordset</a>\*</span></span></p></td>
<td><p><span data-ttu-id="33750-440">Да</span><span class="sxs-lookup"><span data-stu-id="33750-440">Yes</span></span></p></td>
<td><p><span data-ttu-id="33750-441">Да</span><span class="sxs-lookup"><span data-stu-id="33750-441">Yes</span></span></p></td>
<td><p><span data-ttu-id="33750-442">Да</span><span class="sxs-lookup"><span data-stu-id="33750-442">Yes</span></span></p></td>
<td><p><span data-ttu-id="33750-443">Да</span><span class="sxs-lookup"><span data-stu-id="33750-443">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-444"><a href="open-method-ado-recordset.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="33750-444"><a href="open-method-ado-recordset.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="33750-445">Да</span><span class="sxs-lookup"><span data-stu-id="33750-445">Yes</span></span></p></td>
<td><p><span data-ttu-id="33750-446">Да</span><span class="sxs-lookup"><span data-stu-id="33750-446">Yes</span></span></p></td>
<td><p><span data-ttu-id="33750-447">Да</span><span class="sxs-lookup"><span data-stu-id="33750-447">Yes</span></span></p></td>
<td><p><span data-ttu-id="33750-448">Да</span><span class="sxs-lookup"><span data-stu-id="33750-448">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-449"><a href="requery-method-ado.md">Requery</a></span><span class="sxs-lookup"><span data-stu-id="33750-449"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="33750-450">Да</span><span class="sxs-lookup"><span data-stu-id="33750-450">Yes</span></span></p></td>
<td><p><span data-ttu-id="33750-451">Да</span><span class="sxs-lookup"><span data-stu-id="33750-451">Yes</span></span></p></td>
<td><p><span data-ttu-id="33750-452">Да</span><span class="sxs-lookup"><span data-stu-id="33750-452">Yes</span></span></p></td>
<td><p><span data-ttu-id="33750-453">Да</span><span class="sxs-lookup"><span data-stu-id="33750-453">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-454"><a href="resync-method-ado.md">Resync</a></span><span class="sxs-lookup"><span data-stu-id="33750-454"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="33750-455">Нет</span><span class="sxs-lookup"><span data-stu-id="33750-455">No</span></span></p></td>
<td><p><span data-ttu-id="33750-456">Нет</span><span class="sxs-lookup"><span data-stu-id="33750-456">No</span></span></p></td>
<td><p><span data-ttu-id="33750-457">Да</span><span class="sxs-lookup"><span data-stu-id="33750-457">Yes</span></span></p></td>
<td><p><span data-ttu-id="33750-458">Да</span><span class="sxs-lookup"><span data-stu-id="33750-458">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-459"><a href="supports-method-ado.md">Имеется</a></span><span class="sxs-lookup"><span data-stu-id="33750-459"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="33750-460">Да</span><span class="sxs-lookup"><span data-stu-id="33750-460">Yes</span></span></p></td>
<td><p><span data-ttu-id="33750-461">Да</span><span class="sxs-lookup"><span data-stu-id="33750-461">Yes</span></span></p></td>
<td><p><span data-ttu-id="33750-462">Да</span><span class="sxs-lookup"><span data-stu-id="33750-462">Yes</span></span></p></td>
<td><p><span data-ttu-id="33750-463">Да</span><span class="sxs-lookup"><span data-stu-id="33750-463">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-464"><a href="update-method-ado.md">обновление</a>;</span><span class="sxs-lookup"><span data-stu-id="33750-464"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="33750-465">Да</span><span class="sxs-lookup"><span data-stu-id="33750-465">Yes</span></span></p></td>
<td><p><span data-ttu-id="33750-466">Да</span><span class="sxs-lookup"><span data-stu-id="33750-466">Yes</span></span></p></td>
<td><p><span data-ttu-id="33750-467">Да</span><span class="sxs-lookup"><span data-stu-id="33750-467">Yes</span></span></p></td>
<td><p><span data-ttu-id="33750-468">Да</span><span class="sxs-lookup"><span data-stu-id="33750-468">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-469"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="33750-469"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="33750-470">Да</span><span class="sxs-lookup"><span data-stu-id="33750-470">Yes</span></span></p></td>
<td><p><span data-ttu-id="33750-471">Да</span><span class="sxs-lookup"><span data-stu-id="33750-471">Yes</span></span></p></td>
<td><p><span data-ttu-id="33750-472">Да</span><span class="sxs-lookup"><span data-stu-id="33750-472">Yes</span></span></p></td>
<td><p><span data-ttu-id="33750-473">Да</span><span class="sxs-lookup"><span data-stu-id="33750-473">Yes</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="33750-474">\*Не поддерживается для баз данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="33750-474">\*Not supported for Microsoft Access databases.</span></span>

## <a name="dynamic-properties"></a><span data-ttu-id="33750-475">Динамические свойства</span><span class="sxs-lookup"><span data-stu-id="33750-475">Dynamic Properties</span></span>

<span data-ttu-id="33750-476">Поставщик Microsoft OLE DB для ODBC вставляет несколько динамических свойств в коллекцию **свойств** неоткрытых [подключений](connection-object-ado.md), [наборов записей](recordset-object-ado.md)и командных объектов. [](command-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="33750-476">The Microsoft OLE DB Provider for ODBC inserts several dynamic properties into the **Properties** collection of the unopened [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md), and [Command](command-object-ado.md) objects.</span></span>

<span data-ttu-id="33750-477">В приведенных ниже таблицах указаны перекрестные индексы имен ADO и OLE DB для каждого динамического свойства.</span><span class="sxs-lookup"><span data-stu-id="33750-477">The tables below are a cross-index of the ADO and OLE DB names for each dynamic property.</span></span> <span data-ttu-id="33750-478">Справочник программиста OLE DB ссылается на имя свойства ADO по термину "Описание".</span><span class="sxs-lookup"><span data-stu-id="33750-478">The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description."</span></span> <span data-ttu-id="33750-479">Дополнительные сведения об этих свойствах можно найти в справочнике программиста по OLE DB.</span><span class="sxs-lookup"><span data-stu-id="33750-479">You can find more information about these properties in the OLE DB Programmer's Reference.</span></span> <span data-ttu-id="33750-480">Выполните поиск по имени свойства OLE DB в индексе или в разделе приложение C: свойства OLE DB.</span><span class="sxs-lookup"><span data-stu-id="33750-480">Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span></span>

## <a name="connection-dynamic-properties"></a><span data-ttu-id="33750-481">Динамические свойства подключения</span><span class="sxs-lookup"><span data-stu-id="33750-481">Connection Dynamic Properties</span></span>

<span data-ttu-id="33750-482">Следующие свойства добавляются в коллекцию **свойств** объекта **Connection** .</span><span class="sxs-lookup"><span data-stu-id="33750-482">The following properties are added to the **Connection** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="33750-483">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="33750-483">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="33750-484">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="33750-484">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="33750-485">Активные сеансы</span><span class="sxs-lookup"><span data-stu-id="33750-485">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="33750-486">ДБПРОП_АКТИВЕСЕССИОНС</span><span class="sxs-lookup"><span data-stu-id="33750-486">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-487">Асинчабле Abort</span><span class="sxs-lookup"><span data-stu-id="33750-487">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="33750-488">ДБПРОП_АСИНКТКСНАБОРТ</span><span class="sxs-lookup"><span data-stu-id="33750-488">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-489">Фиксация Асинчабле</span><span class="sxs-lookup"><span data-stu-id="33750-489">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="33750-490">ДБПРОП_АСИНКТНКСКОММИТ</span><span class="sxs-lookup"><span data-stu-id="33750-490">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-491">Уровни изоляции для автоматической фиксации</span><span class="sxs-lookup"><span data-stu-id="33750-491">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="33750-492">ДБПРОП_СЕСС_АУТОКОММИТИСОЛЕВЕЛС</span><span class="sxs-lookup"><span data-stu-id="33750-492">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-493">Расположение каталога</span><span class="sxs-lookup"><span data-stu-id="33750-493">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="33750-494">ДБПРОП_КАТАЛОГЛОКАТИОН</span><span class="sxs-lookup"><span data-stu-id="33750-494">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-495">Термин каталога</span><span class="sxs-lookup"><span data-stu-id="33750-495">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="33750-496">ДБПРОП_КАТАЛОГТЕРМ</span><span class="sxs-lookup"><span data-stu-id="33750-496">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-497">Определение столбца</span><span class="sxs-lookup"><span data-stu-id="33750-497">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="33750-498">ДБПРОП_КОЛУМНДЕФИНИТИОН</span><span class="sxs-lookup"><span data-stu-id="33750-498">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-499">Время ожидания подключения</span><span class="sxs-lookup"><span data-stu-id="33750-499">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="33750-500">ДБПРОП_ИНИТ_ТИМЕАУТ</span><span class="sxs-lookup"><span data-stu-id="33750-500">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-501">Текущий каталог</span><span class="sxs-lookup"><span data-stu-id="33750-501">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="33750-502">ДБПРОП_КУРРЕНТКАТАЛОГ</span><span class="sxs-lookup"><span data-stu-id="33750-502">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-503">Источник данных</span><span class="sxs-lookup"><span data-stu-id="33750-503">Data Source</span></span></p></td>
<td><p><span data-ttu-id="33750-504">ДБПРОП_ИНИТ_ДАТАСАУРЦЕ</span><span class="sxs-lookup"><span data-stu-id="33750-504">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-505">Имя источника данных</span><span class="sxs-lookup"><span data-stu-id="33750-505">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="33750-506">ДБПРОП_ДАТАСАУРЦЕНАМЕ</span><span class="sxs-lookup"><span data-stu-id="33750-506">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-507">Модель потоков объектов источника данных</span><span class="sxs-lookup"><span data-stu-id="33750-507">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="33750-508">ДБПРОП_ДСОСРЕАДМОДЕЛ</span><span class="sxs-lookup"><span data-stu-id="33750-508">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-509">Имя СУБД</span><span class="sxs-lookup"><span data-stu-id="33750-509">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="33750-510">ДБПРОП_ДБМСНАМЕ</span><span class="sxs-lookup"><span data-stu-id="33750-510">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-511">Версия DBMS</span><span class="sxs-lookup"><span data-stu-id="33750-511">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="33750-512">ДБПРОП_ДБМСВЕР</span><span class="sxs-lookup"><span data-stu-id="33750-512">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-513">Расширенные свойства</span><span class="sxs-lookup"><span data-stu-id="33750-513">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="33750-514">ДБПРОП_ИНИТ_ПРОВИДЕРСТРИНГ</span><span class="sxs-lookup"><span data-stu-id="33750-514">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-515">ГРУППИРОВКа по поддержке</span><span class="sxs-lookup"><span data-stu-id="33750-515">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="33750-516">ДБПРОП_ГРАУПБИ</span><span class="sxs-lookup"><span data-stu-id="33750-516">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-517">Поддержка гетерогенных таблиц</span><span class="sxs-lookup"><span data-stu-id="33750-517">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="33750-518">ДБПРОП_ХЕТЕРОЖЕНЕАУСТАБЛЕС</span><span class="sxs-lookup"><span data-stu-id="33750-518">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-519">Чувствительность к регистру идентификаторов</span><span class="sxs-lookup"><span data-stu-id="33750-519">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="33750-520">ДБПРОП_ИДЕНТИФИЕРКАСЕ</span><span class="sxs-lookup"><span data-stu-id="33750-520">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-521">Исходный каталог</span><span class="sxs-lookup"><span data-stu-id="33750-521">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="33750-522">ДБПРОП_ИНИТ_КАТАЛОГ</span><span class="sxs-lookup"><span data-stu-id="33750-522">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-523">Уровни изоляции</span><span class="sxs-lookup"><span data-stu-id="33750-523">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="33750-524">ДБПРОП_СУППОРТЕДТКСНИСОЛЕВЕЛС</span><span class="sxs-lookup"><span data-stu-id="33750-524">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-525">Хранение изоляции</span><span class="sxs-lookup"><span data-stu-id="33750-525">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="33750-526">ДБПРОП_СУППОРТЕДТКСНИСОРЕТАИН</span><span class="sxs-lookup"><span data-stu-id="33750-526">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-527">Идентификатор языкового стандарта</span><span class="sxs-lookup"><span data-stu-id="33750-527">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="33750-528">ДБПРОП_ИНИТ_ЛЦИД</span><span class="sxs-lookup"><span data-stu-id="33750-528">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-529">Расположение</span><span class="sxs-lookup"><span data-stu-id="33750-529">Location</span></span></p></td>
<td><p><span data-ttu-id="33750-530">ДБПРОП_ИНИТ_ЛОКАТИОН</span><span class="sxs-lookup"><span data-stu-id="33750-530">DBPROP_INIT_LOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-531">Максимальный размер индекса</span><span class="sxs-lookup"><span data-stu-id="33750-531">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="33750-532">ДБПРОП_МАКСИНДЕКССИЗЕ</span><span class="sxs-lookup"><span data-stu-id="33750-532">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-533">Максимальный размер строки</span><span class="sxs-lookup"><span data-stu-id="33750-533">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="33750-534">ДБПРОП_МАКСРОВСИЗЕ</span><span class="sxs-lookup"><span data-stu-id="33750-534">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-535">Максимальный размер строки включает большой ДВОИЧный объект</span><span class="sxs-lookup"><span data-stu-id="33750-535">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="33750-536">ДБПРОП_МАКСРОВСИЗЕИНКЛУДЕСБЛОБ</span><span class="sxs-lookup"><span data-stu-id="33750-536">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-537">Максимальное число таблиц в SELECT</span><span class="sxs-lookup"><span data-stu-id="33750-537">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="33750-538">ДБПРОП_МАКСТАБЛЕСИНСЕЛЕКТ</span><span class="sxs-lookup"><span data-stu-id="33750-538">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-539">Режим</span><span class="sxs-lookup"><span data-stu-id="33750-539">Mode</span></span></p></td>
<td><p><span data-ttu-id="33750-540">ДБПРОП_ИНИТ_МОДЕ</span><span class="sxs-lookup"><span data-stu-id="33750-540">DBPROP_INIT_MODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-541">Наборы параметров с несколькими параметрами</span><span class="sxs-lookup"><span data-stu-id="33750-541">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="33750-542">ДБПРОП_МУЛТИПЛЕПАРАМСЕТС</span><span class="sxs-lookup"><span data-stu-id="33750-542">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-543">Несколько результатов</span><span class="sxs-lookup"><span data-stu-id="33750-543">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="33750-544">ДБПРОП_МУЛТИПЛЕРЕСУЛТС</span><span class="sxs-lookup"><span data-stu-id="33750-544">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-545">Несколько объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="33750-545">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="33750-546">ДБПРОП_МУЛТИПЛЕСТОРАЖЕОБЖЕКТС</span><span class="sxs-lookup"><span data-stu-id="33750-546">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-547">Обновление с несколькими таблицами</span><span class="sxs-lookup"><span data-stu-id="33750-547">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="33750-548">ДБПРОП_МУЛТИТАБЛЕУПДАТЕ</span><span class="sxs-lookup"><span data-stu-id="33750-548">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-549">Порядок сортировки NULL</span><span class="sxs-lookup"><span data-stu-id="33750-549">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="33750-550">ДБПРОП_НУЛЛКОЛЛАТИОН</span><span class="sxs-lookup"><span data-stu-id="33750-550">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-551">Поведение сцепления со ЗНАЧЕНИЕМ NULL</span><span class="sxs-lookup"><span data-stu-id="33750-551">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="33750-552">ДБПРОП_КОНКАТНУЛЛБЕХАВИОР</span><span class="sxs-lookup"><span data-stu-id="33750-552">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-553">Службы OLE DB</span><span class="sxs-lookup"><span data-stu-id="33750-553">OLE DB Services</span></span></p></td>
<td><p><span data-ttu-id="33750-554">ДБПРОП_ИНИТ_ОЛЕДБСЕРВИЦЕС</span><span class="sxs-lookup"><span data-stu-id="33750-554">DBPROP_INIT_OLEDBSERVICES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-555">Версия OLE DB</span><span class="sxs-lookup"><span data-stu-id="33750-555">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="33750-556">ДБПРОП_ПРОВИДЕРОЛЕДБВЕР</span><span class="sxs-lookup"><span data-stu-id="33750-556">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-557">Поддержка объектов OLE</span><span class="sxs-lookup"><span data-stu-id="33750-557">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="33750-558">ДБПРОП_ОЛЕОБЖЕКТС</span><span class="sxs-lookup"><span data-stu-id="33750-558">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-559">Поддержка открытых наборов строк</span><span class="sxs-lookup"><span data-stu-id="33750-559">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="33750-560">ДБПРОП_ОПЕНРОВСЕТСУППОРТ</span><span class="sxs-lookup"><span data-stu-id="33750-560">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-561">УПОРЯДОЧЕНие по столбцам в списке выборки</span><span class="sxs-lookup"><span data-stu-id="33750-561">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="33750-562">ДБПРОП_ОРДЕРБИКОЛУМНСИНСЕЛЕКТ</span><span class="sxs-lookup"><span data-stu-id="33750-562">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-563">Доступность выходного параметра</span><span class="sxs-lookup"><span data-stu-id="33750-563">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="33750-564">ДБПРОП_АУТПУТПАРАМЕТЕРАВАИЛАБИЛИТИ</span><span class="sxs-lookup"><span data-stu-id="33750-564">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-565">Пароль</span><span class="sxs-lookup"><span data-stu-id="33750-565">Password</span></span></p></td>
<td><p><span data-ttu-id="33750-566">ДБПРОП_АУС_ПАССВОРД</span><span class="sxs-lookup"><span data-stu-id="33750-566">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-567">Передача по параметрам доступа ref</span><span class="sxs-lookup"><span data-stu-id="33750-567">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="33750-568">ДБПРОП_БИРЕФАКЦЕССОРС</span><span class="sxs-lookup"><span data-stu-id="33750-568">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-569">Сохранение сведений о безопасности</span><span class="sxs-lookup"><span data-stu-id="33750-569">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="33750-570">ДБПРОП_АУС_ПЕРСИСТ_СЕНСИТИВЕ_АУСИНФО</span><span class="sxs-lookup"><span data-stu-id="33750-570">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-571">Тип постоянного идентификатора</span><span class="sxs-lookup"><span data-stu-id="33750-571">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="33750-572">ДБПРОП_ПЕРСИСТЕНТИДТИПЕ</span><span class="sxs-lookup"><span data-stu-id="33750-572">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-573">Действие по подготовке к прерыванию</span><span class="sxs-lookup"><span data-stu-id="33750-573">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="33750-574">ДБПРОП_ПРЕПАРЕАБОРТБЕХАВИОР</span><span class="sxs-lookup"><span data-stu-id="33750-574">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-575">Подготовка режима фиксации</span><span class="sxs-lookup"><span data-stu-id="33750-575">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="33750-576">ДБПРОП_ПРЕПАРЕКОММИТБЕХАВИОР</span><span class="sxs-lookup"><span data-stu-id="33750-576">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-577">Термин процедуры</span><span class="sxs-lookup"><span data-stu-id="33750-577">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="33750-578">ДБПРОП_ПРОЦЕДУРЕТЕРМ</span><span class="sxs-lookup"><span data-stu-id="33750-578">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-579">Prompt</span><span class="sxs-lookup"><span data-stu-id="33750-579">Prompt</span></span></p></td>
<td><p><span data-ttu-id="33750-580">ДБПРОП_ИНИТ_ПРОМПТ</span><span class="sxs-lookup"><span data-stu-id="33750-580">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-581">Понятное имя поставщика</span><span class="sxs-lookup"><span data-stu-id="33750-581">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="33750-582">ДБПРОП_ПРОВИДЕРФРИЕНДЛИНАМЕ</span><span class="sxs-lookup"><span data-stu-id="33750-582">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-583">Имя поставщика</span><span class="sxs-lookup"><span data-stu-id="33750-583">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="33750-584">ДБПРОП_ПРОВИДЕРФИЛЕНАМЕ</span><span class="sxs-lookup"><span data-stu-id="33750-584">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-585">Версия поставщика</span><span class="sxs-lookup"><span data-stu-id="33750-585">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="33750-586">ДБПРОП_ПРОВИДЕРВЕР</span><span class="sxs-lookup"><span data-stu-id="33750-586">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-587">Источник данных, предназначенный только для чтения</span><span class="sxs-lookup"><span data-stu-id="33750-587">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="33750-588">ДБПРОП_ДАТАСАУРЦЕРЕАДОНЛИ</span><span class="sxs-lookup"><span data-stu-id="33750-588">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-589">Преобразования наборов строк для команды</span><span class="sxs-lookup"><span data-stu-id="33750-589">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="33750-590">ДБПРОП_РОВСЕТКОНВЕРСИОНСОНКОММАНД</span><span class="sxs-lookup"><span data-stu-id="33750-590">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-591">Термин схемы</span><span class="sxs-lookup"><span data-stu-id="33750-591">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="33750-592">ДБПРОП_СЧЕМАТЕРМ</span><span class="sxs-lookup"><span data-stu-id="33750-592">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-593">Использование схемы</span><span class="sxs-lookup"><span data-stu-id="33750-593">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="33750-594">ДБПРОП_СЧЕМАУСАЖЕ</span><span class="sxs-lookup"><span data-stu-id="33750-594">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-595">Поддержка SQL</span><span class="sxs-lookup"><span data-stu-id="33750-595">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="33750-596">ДБПРОП_СКЛСУППОРТ</span><span class="sxs-lookup"><span data-stu-id="33750-596">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-597">Структурированное хранилище</span><span class="sxs-lookup"><span data-stu-id="33750-597">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="33750-598">ДБПРОП_СТРУКТУРЕДСТОРАЖЕ</span><span class="sxs-lookup"><span data-stu-id="33750-598">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-599">Поддержка вложенных запросов</span><span class="sxs-lookup"><span data-stu-id="33750-599">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="33750-600">ДБПРОП_СУБКУЕРИЕС</span><span class="sxs-lookup"><span data-stu-id="33750-600">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-601">Табличный термин</span><span class="sxs-lookup"><span data-stu-id="33750-601">Table Term</span></span></p></td>
<td><p><span data-ttu-id="33750-602">ДБПРОП_ТАБЛЕТЕРМ</span><span class="sxs-lookup"><span data-stu-id="33750-602">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-603">DDL транзакции</span><span class="sxs-lookup"><span data-stu-id="33750-603">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="33750-604">ДБПРОП_СУППОРТЕДТКСНДДЛ</span><span class="sxs-lookup"><span data-stu-id="33750-604">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-605">Идентификатор пользователя</span><span class="sxs-lookup"><span data-stu-id="33750-605">User ID</span></span></p></td>
<td><p><span data-ttu-id="33750-606">ДБПРОП_АУС_УСЕРИД</span><span class="sxs-lookup"><span data-stu-id="33750-606">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-607">имя пользователя;</span><span class="sxs-lookup"><span data-stu-id="33750-607">User Name</span></span></p></td>
<td><p><span data-ttu-id="33750-608">ДБПРОП_УСЕРНАМЕ</span><span class="sxs-lookup"><span data-stu-id="33750-608">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-609">Дескриптор окна</span><span class="sxs-lookup"><span data-stu-id="33750-609">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="33750-610">ДБПРОП_ИНИТ_ХВНД</span><span class="sxs-lookup"><span data-stu-id="33750-610">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a><span data-ttu-id="33750-611">Динамические свойства Recordset</span><span class="sxs-lookup"><span data-stu-id="33750-611">Recordset Dynamic Properties</span></span>

<span data-ttu-id="33750-612">Следующие свойства добавляются в коллекцию **свойств** объекта **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="33750-612">The following properties are added to the **Recordset** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="33750-613">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="33750-613">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="33750-614">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="33750-614">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="33750-615">Порядок доступа</span><span class="sxs-lookup"><span data-stu-id="33750-615">Access Order</span></span></p></td>
<td><p><span data-ttu-id="33750-616">ДБПРОП_АКЦЕССОРДЕР</span><span class="sxs-lookup"><span data-stu-id="33750-616">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-617">Блокировка объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="33750-617">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="33750-618">ДБПРОП_БЛОККИНГСТОРАЖЕОБЖЕКТС</span><span class="sxs-lookup"><span data-stu-id="33750-618">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-619">Тип закладки</span><span class="sxs-lookup"><span data-stu-id="33750-619">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="33750-620">ДБПРОП_БУКМАРКТИПЕ</span><span class="sxs-lookup"><span data-stu-id="33750-620">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-621">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="33750-621">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="33750-622">ДБПРОП_ИРОВСЕТЛОКАТЕ</span><span class="sxs-lookup"><span data-stu-id="33750-622">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-623">Изменение вставленных строк</span><span class="sxs-lookup"><span data-stu-id="33750-623">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="33750-624">ДБПРОП_ЧАНЖЕИНСЕРТЕДРОВС</span><span class="sxs-lookup"><span data-stu-id="33750-624">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-625">Права на столбцы</span><span class="sxs-lookup"><span data-stu-id="33750-625">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="33750-626">ДБПРОП_КОЛУМНРЕСТРИКТ</span><span class="sxs-lookup"><span data-stu-id="33750-626">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-627">Уведомление о наборе столбцов</span><span class="sxs-lookup"><span data-stu-id="33750-627">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="33750-628">ДБПРОП_НОТИФИКОЛУМНСЕТ</span><span class="sxs-lookup"><span data-stu-id="33750-628">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-629">ОтКладывание обновлений объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="33750-629">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="33750-630">ДБПРОП_ДЕЛАЙСТОРАЖЕОБЖЕКТС</span><span class="sxs-lookup"><span data-stu-id="33750-630">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-631">Извлечение назад</span><span class="sxs-lookup"><span data-stu-id="33750-631">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="33750-632">ДБПРОП_КАНФЕТЧБАККВАРДС</span><span class="sxs-lookup"><span data-stu-id="33750-632">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-633">Удержание строк</span><span class="sxs-lookup"><span data-stu-id="33750-633">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="33750-634">ДБПРОП_КАНХОЛДРОВС</span><span class="sxs-lookup"><span data-stu-id="33750-634">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-635">Иакцессор</span><span class="sxs-lookup"><span data-stu-id="33750-635">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="33750-636">Дбпроп_иакцессор</span><span class="sxs-lookup"><span data-stu-id="33750-636">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-637">Иколумнсинфо</span><span class="sxs-lookup"><span data-stu-id="33750-637">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="33750-638">Дбпроп_иколумнсинфо</span><span class="sxs-lookup"><span data-stu-id="33750-638">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-639">Иколумнсровсет</span><span class="sxs-lookup"><span data-stu-id="33750-639">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="33750-640">Дбпроп_иколумнсровсет</span><span class="sxs-lookup"><span data-stu-id="33750-640">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-641">Иконнектионпоинтконтаинер</span><span class="sxs-lookup"><span data-stu-id="33750-641">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="33750-642">Дбпроп_иконнектионпоинтконтаинер</span><span class="sxs-lookup"><span data-stu-id="33750-642">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-643">Иконверттипе</span><span class="sxs-lookup"><span data-stu-id="33750-643">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="33750-644">Дбпроп_иконверттипе</span><span class="sxs-lookup"><span data-stu-id="33750-644">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-645">Строки для мобильных устройств</span><span class="sxs-lookup"><span data-stu-id="33750-645">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="33750-646">ДБПРОП_ИММОБИЛЕРОВС</span><span class="sxs-lookup"><span data-stu-id="33750-646">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-647">IRowset</span><span class="sxs-lookup"><span data-stu-id="33750-647">IRowset</span></span></p></td>
<td><p><span data-ttu-id="33750-648">Дбпроп_ировсет</span><span class="sxs-lookup"><span data-stu-id="33750-648">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-649">Ировсетчанже</span><span class="sxs-lookup"><span data-stu-id="33750-649">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="33750-650">Дбпроп_ировсетчанже</span><span class="sxs-lookup"><span data-stu-id="33750-650">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-651">Ировсетидентити</span><span class="sxs-lookup"><span data-stu-id="33750-651">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="33750-652">Дбпроп_ировсетидентити</span><span class="sxs-lookup"><span data-stu-id="33750-652">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-653">Ировсетинфо</span><span class="sxs-lookup"><span data-stu-id="33750-653">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="33750-654">Дбпроп_ировсетинфо</span><span class="sxs-lookup"><span data-stu-id="33750-654">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-655">Ировсетлокате</span><span class="sxs-lookup"><span data-stu-id="33750-655">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="33750-656">Дбпроп_ировсетлокате</span><span class="sxs-lookup"><span data-stu-id="33750-656">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-657">Ировсетресинч</span><span class="sxs-lookup"><span data-stu-id="33750-657">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-658">Ировсетупдате</span><span class="sxs-lookup"><span data-stu-id="33750-658">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="33750-659">Дбпроп_ировсетупдате</span><span class="sxs-lookup"><span data-stu-id="33750-659">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-660">Исекуентиалстреам</span><span class="sxs-lookup"><span data-stu-id="33750-660">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="33750-661">Дбпроп_исекуентиалстреам</span><span class="sxs-lookup"><span data-stu-id="33750-661">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-662">Исуппортерроринфо</span><span class="sxs-lookup"><span data-stu-id="33750-662">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="33750-663">Дбпроп_исуппортерроринфо</span><span class="sxs-lookup"><span data-stu-id="33750-663">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-664">Литеральные закладки</span><span class="sxs-lookup"><span data-stu-id="33750-664">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="33750-665">ДБПРОП_ЛИТЕРАЛБУКМАРКС</span><span class="sxs-lookup"><span data-stu-id="33750-665">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-666">Идентификация строк литералов</span><span class="sxs-lookup"><span data-stu-id="33750-666">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="33750-667">ДБПРОП_ЛИТЕРАЛИДЕНТИТИ</span><span class="sxs-lookup"><span data-stu-id="33750-667">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-668">Максимальное число открытых строк</span><span class="sxs-lookup"><span data-stu-id="33750-668">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="33750-669">ДБПРОП_МАКСОПЕНРОВС</span><span class="sxs-lookup"><span data-stu-id="33750-669">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-670">Максимальное число ожидающих строк</span><span class="sxs-lookup"><span data-stu-id="33750-670">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="33750-671">ДБПРОП_МАКСПЕНДИНГРОВС</span><span class="sxs-lookup"><span data-stu-id="33750-671">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-672">Максимальное число строк</span><span class="sxs-lookup"><span data-stu-id="33750-672">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="33750-673">ДБПРОП_МАКСРОВС</span><span class="sxs-lookup"><span data-stu-id="33750-673">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-674">Детализация уведомлений</span><span class="sxs-lookup"><span data-stu-id="33750-674">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="33750-675">ДБПРОП_НОТИФИКАТИОНГРАНУЛАРИТИ</span><span class="sxs-lookup"><span data-stu-id="33750-675">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-676">Этапы уведомления</span><span class="sxs-lookup"><span data-stu-id="33750-676">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="33750-677">ДБПРОП_НОТИФИКАТИОНФАСЕС</span><span class="sxs-lookup"><span data-stu-id="33750-677">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-678">Объекты, транзакционные</span><span class="sxs-lookup"><span data-stu-id="33750-678">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="33750-679">ДБПРОП_ТРАНСАКТЕДОБЖЕКТ</span><span class="sxs-lookup"><span data-stu-id="33750-679">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-680">Видны изменения</span><span class="sxs-lookup"><span data-stu-id="33750-680">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="33750-681">ДБПРОП_ОВНУПДАТЕДЕЛЕТЕ</span><span class="sxs-lookup"><span data-stu-id="33750-681">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-682">Отображение собственных вставок</span><span class="sxs-lookup"><span data-stu-id="33750-682">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="33750-683">ДБПРОП_ОВНИНСЕРТ</span><span class="sxs-lookup"><span data-stu-id="33750-683">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-684">Сохранение при прерывании</span><span class="sxs-lookup"><span data-stu-id="33750-684">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="33750-685">ДБПРОП_АБОРТПРЕСЕРВЕ</span><span class="sxs-lookup"><span data-stu-id="33750-685">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-686">Сохранение при фиксации</span><span class="sxs-lookup"><span data-stu-id="33750-686">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="33750-687">ДБПРОП_КОММИТПРЕСЕРВЕ</span><span class="sxs-lookup"><span data-stu-id="33750-687">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-688">Быстрый перезапуск</span><span class="sxs-lookup"><span data-stu-id="33750-688">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="33750-689">ДБПРОП_КУИККРЕСТАРТ</span><span class="sxs-lookup"><span data-stu-id="33750-689">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-690">Повторные события</span><span class="sxs-lookup"><span data-stu-id="33750-690">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="33750-691">ДБПРОП_РИНТРАНТЕВЕНТС</span><span class="sxs-lookup"><span data-stu-id="33750-691">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-692">Удаление удаленных строк</span><span class="sxs-lookup"><span data-stu-id="33750-692">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="33750-693">ДБПРОП_РЕМОВЕДЕЛЕТЕД</span><span class="sxs-lookup"><span data-stu-id="33750-693">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-694">Отчет о нескольких изменениях</span><span class="sxs-lookup"><span data-stu-id="33750-694">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="33750-695">ДБПРОП_РЕПОРТМУЛТИПЛЕЧАНЖЕС</span><span class="sxs-lookup"><span data-stu-id="33750-695">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-696">Возврат ожидающих вставок</span><span class="sxs-lookup"><span data-stu-id="33750-696">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="33750-697">ДБПРОП_РЕТУРНПЕНДИНГИНСЕРТС</span><span class="sxs-lookup"><span data-stu-id="33750-697">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-698">Уведомление об удалении строки</span><span class="sxs-lookup"><span data-stu-id="33750-698">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="33750-699">ДБПРОП_НОТИФИРОВДЕЛЕТЕ</span><span class="sxs-lookup"><span data-stu-id="33750-699">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-700">Уведомление о первом изменении строки</span><span class="sxs-lookup"><span data-stu-id="33750-700">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="33750-701">ДБПРОП_НОТИФИРОВФИРСТЧАНЖЕ</span><span class="sxs-lookup"><span data-stu-id="33750-701">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-702">Уведомление о вставке строк</span><span class="sxs-lookup"><span data-stu-id="33750-702">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="33750-703">ДБПРОП_НОТИФИРОВИНСЕРТ</span><span class="sxs-lookup"><span data-stu-id="33750-703">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-704">Права на строки</span><span class="sxs-lookup"><span data-stu-id="33750-704">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="33750-705">ДБПРОП_РОВРЕСТРИКТ</span><span class="sxs-lookup"><span data-stu-id="33750-705">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-706">Уведомление о повторной синхронизации строк</span><span class="sxs-lookup"><span data-stu-id="33750-706">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="33750-707">ДБПРОП_НОТИФИРОВРЕСИНЧ</span><span class="sxs-lookup"><span data-stu-id="33750-707">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-708">Потоковая модель для строк</span><span class="sxs-lookup"><span data-stu-id="33750-708">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="33750-709">ДБПРОП_РОВСРЕАДМОДЕЛ</span><span class="sxs-lookup"><span data-stu-id="33750-709">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-710">Уведомление об отмене изменения строки</span><span class="sxs-lookup"><span data-stu-id="33750-710">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="33750-711">ДБПРОП_НОТИФИРОВУНДОЧАНЖЕ</span><span class="sxs-lookup"><span data-stu-id="33750-711">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-712">Уведомление о отмене удаления строки</span><span class="sxs-lookup"><span data-stu-id="33750-712">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="33750-713">ДБПРОП_НОТИФИРОВУНДОДЕЛЕТЕ</span><span class="sxs-lookup"><span data-stu-id="33750-713">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-714">Уведомление об отмене вставки строки</span><span class="sxs-lookup"><span data-stu-id="33750-714">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="33750-715">ДБПРОП_НОТИФИРОВУНДОИНСЕРТ</span><span class="sxs-lookup"><span data-stu-id="33750-715">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-716">Уведомление об обновлении строк</span><span class="sxs-lookup"><span data-stu-id="33750-716">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="33750-717">ДБПРОП_НОТИФИРОВУПДАТЕ</span><span class="sxs-lookup"><span data-stu-id="33750-717">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-718">Уведомление об изменении положения при получении набора строк</span><span class="sxs-lookup"><span data-stu-id="33750-718">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="33750-719">ДБПРОП_НОТИФИРОВСЕТФЕТЧПОСИСИОНЧАНЖЕ</span><span class="sxs-lookup"><span data-stu-id="33750-719">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-720">Уведомление о выПуске набора строк</span><span class="sxs-lookup"><span data-stu-id="33750-720">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="33750-721">ДБПРОП_НОТИФИРОВСЕТРЕЛЕАСЕ</span><span class="sxs-lookup"><span data-stu-id="33750-721">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-722">ПроКрутка назад</span><span class="sxs-lookup"><span data-stu-id="33750-722">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="33750-723">ДБПРОП_КАНСКРОЛЛБАККВАРДС</span><span class="sxs-lookup"><span data-stu-id="33750-723">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-724">Пропуск удаленных закладок</span><span class="sxs-lookup"><span data-stu-id="33750-724">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="33750-725">ДБПРОП_БУКМАРКСКИППЕД</span><span class="sxs-lookup"><span data-stu-id="33750-725">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-726">Строгая идентификация строк</span><span class="sxs-lookup"><span data-stu-id="33750-726">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="33750-727">ДБПРОП_СТРОНГИТДЕНТИТИ</span><span class="sxs-lookup"><span data-stu-id="33750-727">DBPROP_STRONGITDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-728">Уникальные строки</span><span class="sxs-lookup"><span data-stu-id="33750-728">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="33750-729">ДБПРОП_УНИКУЕРОВС</span><span class="sxs-lookup"><span data-stu-id="33750-729">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-730">Обновление</span><span class="sxs-lookup"><span data-stu-id="33750-730">Updatability</span></span></p></td>
<td><p><span data-ttu-id="33750-731">ДБПРОП_УПДАТАБИЛИТИ</span><span class="sxs-lookup"><span data-stu-id="33750-731">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-732">Использование закладок</span><span class="sxs-lookup"><span data-stu-id="33750-732">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="33750-733">ДБПРОП_БУКМАРКС</span><span class="sxs-lookup"><span data-stu-id="33750-733">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a><span data-ttu-id="33750-734">Динамические свойства команд</span><span class="sxs-lookup"><span data-stu-id="33750-734">Command Dynamic Properties</span></span>

<span data-ttu-id="33750-735">Указанные ниже свойства добавляются в коллекцию \*\*\*\* **свойств** командного объекта.</span><span class="sxs-lookup"><span data-stu-id="33750-735">The following properties are added to the **Command** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="33750-736">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="33750-736">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="33750-737">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="33750-737">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="33750-738">Порядок доступа</span><span class="sxs-lookup"><span data-stu-id="33750-738">Access Order</span></span></p></td>
<td><p><span data-ttu-id="33750-739">ДБПРОП_АКЦЕССОРДЕР</span><span class="sxs-lookup"><span data-stu-id="33750-739">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-740">Блокировка объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="33750-740">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="33750-741">ДБПРОП_БЛОККИНГСТОРАЖЕОБЖЕКТС</span><span class="sxs-lookup"><span data-stu-id="33750-741">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-742">Тип закладки</span><span class="sxs-lookup"><span data-stu-id="33750-742">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="33750-743">ДБПРОП_БУКМАРКТИПЕ</span><span class="sxs-lookup"><span data-stu-id="33750-743">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-744">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="33750-744">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="33750-745">ДБПРОП_ИРОВСЕТЛОКАТЕ</span><span class="sxs-lookup"><span data-stu-id="33750-745">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-746">Изменение вставленных строк</span><span class="sxs-lookup"><span data-stu-id="33750-746">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="33750-747">ДБПРОП_ЧАНЖЕИНСЕРТЕДРОВС</span><span class="sxs-lookup"><span data-stu-id="33750-747">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-748">Права на столбцы</span><span class="sxs-lookup"><span data-stu-id="33750-748">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="33750-749">ДБПРОП_КОЛУМНРЕСТРИКТ</span><span class="sxs-lookup"><span data-stu-id="33750-749">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-750">Уведомление о наборе столбцов</span><span class="sxs-lookup"><span data-stu-id="33750-750">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="33750-751">ДБПРОП_НОТИФИКОЛУМНСЕТ</span><span class="sxs-lookup"><span data-stu-id="33750-751">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-752">ОтКладывание обновлений объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="33750-752">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="33750-753">ДБПРОП_ДЕЛАЙСТОРАЖЕОБЖЕКТС</span><span class="sxs-lookup"><span data-stu-id="33750-753">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-754">Извлечение назад</span><span class="sxs-lookup"><span data-stu-id="33750-754">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="33750-755">ДБПРОП_КАНФЕТЧБАККВАРДС</span><span class="sxs-lookup"><span data-stu-id="33750-755">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-756">Удержание строк</span><span class="sxs-lookup"><span data-stu-id="33750-756">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="33750-757">ДБПРОП_КАНХОЛДРОВС</span><span class="sxs-lookup"><span data-stu-id="33750-757">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-758">Иакцессор</span><span class="sxs-lookup"><span data-stu-id="33750-758">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="33750-759">Дбпроп_иакцессор</span><span class="sxs-lookup"><span data-stu-id="33750-759">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-760">Иколумнсинфо</span><span class="sxs-lookup"><span data-stu-id="33750-760">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="33750-761">Дбпроп_иколумнсинфо</span><span class="sxs-lookup"><span data-stu-id="33750-761">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-762">Иколумнсровсет</span><span class="sxs-lookup"><span data-stu-id="33750-762">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="33750-763">Дбпроп_иколумнсровсет</span><span class="sxs-lookup"><span data-stu-id="33750-763">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-764">Иконнектионпоинтконтаинер</span><span class="sxs-lookup"><span data-stu-id="33750-764">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="33750-765">Дбпроп_иконнектионпоинтконтаинер</span><span class="sxs-lookup"><span data-stu-id="33750-765">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-766">Иконверттипе</span><span class="sxs-lookup"><span data-stu-id="33750-766">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="33750-767">Дбпроп_иконверттипе</span><span class="sxs-lookup"><span data-stu-id="33750-767">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-768">Строки для мобильных устройств</span><span class="sxs-lookup"><span data-stu-id="33750-768">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="33750-769">ДБПРОП_ИММОБИЛЕРОВС</span><span class="sxs-lookup"><span data-stu-id="33750-769">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-770">IRowset</span><span class="sxs-lookup"><span data-stu-id="33750-770">IRowset</span></span></p></td>
<td><p><span data-ttu-id="33750-771">Дбпроп_ировсет</span><span class="sxs-lookup"><span data-stu-id="33750-771">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-772">Ировсетчанже</span><span class="sxs-lookup"><span data-stu-id="33750-772">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="33750-773">Дбпроп_ировсетчанже</span><span class="sxs-lookup"><span data-stu-id="33750-773">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-774">Ировсетидентити</span><span class="sxs-lookup"><span data-stu-id="33750-774">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="33750-775">Дбпроп_ировсетидентити</span><span class="sxs-lookup"><span data-stu-id="33750-775">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-776">Ировсетинфо</span><span class="sxs-lookup"><span data-stu-id="33750-776">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="33750-777">Дбпроп_ировсетинфо</span><span class="sxs-lookup"><span data-stu-id="33750-777">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-778">Ировсетлокате</span><span class="sxs-lookup"><span data-stu-id="33750-778">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="33750-779">Дбпроп_ировсетлокате</span><span class="sxs-lookup"><span data-stu-id="33750-779">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-780">Ировсетресинч</span><span class="sxs-lookup"><span data-stu-id="33750-780">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-781">Ировсетупдате</span><span class="sxs-lookup"><span data-stu-id="33750-781">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="33750-782">Дбпроп_ировсетупдате</span><span class="sxs-lookup"><span data-stu-id="33750-782">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-783">Исекуентиалстреам</span><span class="sxs-lookup"><span data-stu-id="33750-783">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="33750-784">Дбпроп_исекуентиалстреам</span><span class="sxs-lookup"><span data-stu-id="33750-784">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-785">Исуппортерроринфо</span><span class="sxs-lookup"><span data-stu-id="33750-785">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="33750-786">Дбпроп_исуппортерроринфо</span><span class="sxs-lookup"><span data-stu-id="33750-786">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-787">Литеральные закладки</span><span class="sxs-lookup"><span data-stu-id="33750-787">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="33750-788">ДБПРОП_ЛИТЕРАЛБУКМАРКС</span><span class="sxs-lookup"><span data-stu-id="33750-788">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-789">Идентификация строк литералов</span><span class="sxs-lookup"><span data-stu-id="33750-789">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="33750-790">ДБПРОП_ЛИТЕРАЛИДЕНТИТИ</span><span class="sxs-lookup"><span data-stu-id="33750-790">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-791">Максимальное число открытых строк</span><span class="sxs-lookup"><span data-stu-id="33750-791">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="33750-792">ДБПРОП_МАКСОПЕНРОВС</span><span class="sxs-lookup"><span data-stu-id="33750-792">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-793">Максимальное число ожидающих строк</span><span class="sxs-lookup"><span data-stu-id="33750-793">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="33750-794">ДБПРОП_МАКСПЕНДИНГРОВС</span><span class="sxs-lookup"><span data-stu-id="33750-794">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-795">Максимальное число строк</span><span class="sxs-lookup"><span data-stu-id="33750-795">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="33750-796">ДБПРОП_МАКСРОВС</span><span class="sxs-lookup"><span data-stu-id="33750-796">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-797">Детализация уведомлений</span><span class="sxs-lookup"><span data-stu-id="33750-797">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="33750-798">ДБПРОП_НОТИФИКАТИОНГРАНУЛАРИТИ</span><span class="sxs-lookup"><span data-stu-id="33750-798">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-799">Этапы уведомления</span><span class="sxs-lookup"><span data-stu-id="33750-799">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="33750-800">ДБПРОП_НОТИФИКАТИОНФАСЕС</span><span class="sxs-lookup"><span data-stu-id="33750-800">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-801">Объекты, транзакционные</span><span class="sxs-lookup"><span data-stu-id="33750-801">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="33750-802">ДБПРОП_ТРАНСАКТЕДОБЖЕКТ</span><span class="sxs-lookup"><span data-stu-id="33750-802">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-803">Видны изменения</span><span class="sxs-lookup"><span data-stu-id="33750-803">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="33750-804">ДБПРОП_ОВНУПДАТЕДЕЛЕТЕ</span><span class="sxs-lookup"><span data-stu-id="33750-804">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-805">Отображение собственных вставок</span><span class="sxs-lookup"><span data-stu-id="33750-805">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="33750-806">ДБПРОП_ОВНИНСЕРТ</span><span class="sxs-lookup"><span data-stu-id="33750-806">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-807">Сохранение при прерывании</span><span class="sxs-lookup"><span data-stu-id="33750-807">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="33750-808">ДБПРОП_АБОРТПРЕСЕРВЕ</span><span class="sxs-lookup"><span data-stu-id="33750-808">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-809">Сохранение при фиксации</span><span class="sxs-lookup"><span data-stu-id="33750-809">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="33750-810">ДБПРОП_КОММИТПРЕСЕРВЕ</span><span class="sxs-lookup"><span data-stu-id="33750-810">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-811">Быстрый перезапуск</span><span class="sxs-lookup"><span data-stu-id="33750-811">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="33750-812">ДБПРОП_КУИККРЕСТАРТ</span><span class="sxs-lookup"><span data-stu-id="33750-812">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-813">Повторные события</span><span class="sxs-lookup"><span data-stu-id="33750-813">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="33750-814">ДБПРОП_РИНТРАНТЕВЕНТС</span><span class="sxs-lookup"><span data-stu-id="33750-814">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-815">Удаление удаленных строк</span><span class="sxs-lookup"><span data-stu-id="33750-815">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="33750-816">ДБПРОП_РЕМОВЕДЕЛЕТЕД</span><span class="sxs-lookup"><span data-stu-id="33750-816">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-817">Отчет о нескольких изменениях</span><span class="sxs-lookup"><span data-stu-id="33750-817">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="33750-818">ДБПРОП_РЕПОРТМУЛТИПЛЕЧАНЖЕС</span><span class="sxs-lookup"><span data-stu-id="33750-818">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-819">Возврат ожидающих вставок</span><span class="sxs-lookup"><span data-stu-id="33750-819">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="33750-820">ДБПРОП_РЕТУРНПЕНДИНГИНСЕРТС</span><span class="sxs-lookup"><span data-stu-id="33750-820">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-821">Уведомление об удалении строки</span><span class="sxs-lookup"><span data-stu-id="33750-821">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="33750-822">ДБПРОП_НОТИФИРОВДЕЛЕТЕ</span><span class="sxs-lookup"><span data-stu-id="33750-822">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-823">Уведомление о первом изменении строки</span><span class="sxs-lookup"><span data-stu-id="33750-823">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="33750-824">ДБПРОП_НОТИФИРОВФИРСТЧАНЖЕ</span><span class="sxs-lookup"><span data-stu-id="33750-824">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-825">Уведомление о вставке строк</span><span class="sxs-lookup"><span data-stu-id="33750-825">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="33750-826">ДБПРОП_НОТИФИРОВИНСЕРТ</span><span class="sxs-lookup"><span data-stu-id="33750-826">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-827">Права на строки</span><span class="sxs-lookup"><span data-stu-id="33750-827">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="33750-828">ДБПРОП_РОВРЕСТРИКТ</span><span class="sxs-lookup"><span data-stu-id="33750-828">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-829">Уведомление о повторной синхронизации строк</span><span class="sxs-lookup"><span data-stu-id="33750-829">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="33750-830">ДБПРОП_НОТИФИРОВРЕСИНЧ</span><span class="sxs-lookup"><span data-stu-id="33750-830">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-831">Потоковая модель для строк</span><span class="sxs-lookup"><span data-stu-id="33750-831">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="33750-832">ДБПРОП_РОВСРЕАДМОДЕЛ</span><span class="sxs-lookup"><span data-stu-id="33750-832">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-833">Уведомление об отмене изменения строки</span><span class="sxs-lookup"><span data-stu-id="33750-833">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="33750-834">ДБПРОП_НОТИФИРОВУНДОЧАНЖЕ</span><span class="sxs-lookup"><span data-stu-id="33750-834">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-835">Уведомление о отмене удаления строки</span><span class="sxs-lookup"><span data-stu-id="33750-835">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="33750-836">ДБПРОП_НОТИФИРОВУНДОДЕЛЕТЕ</span><span class="sxs-lookup"><span data-stu-id="33750-836">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-837">Уведомление об отмене вставки строки</span><span class="sxs-lookup"><span data-stu-id="33750-837">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="33750-838">ДБПРОП_НОТИФИРОВУНДОИНСЕРТ</span><span class="sxs-lookup"><span data-stu-id="33750-838">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-839">Уведомление об обновлении строк</span><span class="sxs-lookup"><span data-stu-id="33750-839">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="33750-840">ДБПРОП_НОТИФИРОВУПДАТЕ</span><span class="sxs-lookup"><span data-stu-id="33750-840">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-841">Уведомление об изменении положения при получении набора строк</span><span class="sxs-lookup"><span data-stu-id="33750-841">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="33750-842">ДБПРОП_НОТИФИРОВСЕТФЕТЧПОСИТИОНЧАНЖЕ</span><span class="sxs-lookup"><span data-stu-id="33750-842">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-843">Уведомление о выПуске набора строк</span><span class="sxs-lookup"><span data-stu-id="33750-843">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="33750-844">ДБПРОП_НОТИФИРОВСЕТРЕЛЕАСЕ</span><span class="sxs-lookup"><span data-stu-id="33750-844">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-845">ПроКрутка назад</span><span class="sxs-lookup"><span data-stu-id="33750-845">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="33750-846">ДБПРОП_КАНСКРОЛЛБАККВАРДС</span><span class="sxs-lookup"><span data-stu-id="33750-846">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-847">Пропуск удаленных закладок</span><span class="sxs-lookup"><span data-stu-id="33750-847">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="33750-848">ДБПРОП_БУКМАРКСКИП</span><span class="sxs-lookup"><span data-stu-id="33750-848">DBPROP_BOOKMARKSKIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-849">Строгая идентификация строк</span><span class="sxs-lookup"><span data-stu-id="33750-849">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="33750-850">ДБПРОП_СТРОНГИДЕНТИТИ</span><span class="sxs-lookup"><span data-stu-id="33750-850">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33750-851">Обновление</span><span class="sxs-lookup"><span data-stu-id="33750-851">Updatability</span></span></p></td>
<td><p><span data-ttu-id="33750-852">ДБПРОП_УПДАТАБИЛИТИ</span><span class="sxs-lookup"><span data-stu-id="33750-852">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33750-853">Использование закладок</span><span class="sxs-lookup"><span data-stu-id="33750-853">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="33750-854">ДБПРОП_БУКМАРКС</span><span class="sxs-lookup"><span data-stu-id="33750-854">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="33750-855">См. также</span><span class="sxs-lookup"><span data-stu-id="33750-855">See also</span></span>

<span data-ttu-id="33750-856">Сведения о конкретных реализациях и функциональных сведениях о поставщике Microsoft OLE DB для ODBC можно найти в [руководстве программиста по OLE DB](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85)) или посетить [Центр разработчиков платформы данных](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).</span><span class="sxs-lookup"><span data-stu-id="33750-856">For details regarding specific implementation and functional information about the Microsoft OLE DB Provider for ODBC, consult the [OLE DB Programmer's Guide](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85)) or visit the [Data Platform Developer Center](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).</span></span>

