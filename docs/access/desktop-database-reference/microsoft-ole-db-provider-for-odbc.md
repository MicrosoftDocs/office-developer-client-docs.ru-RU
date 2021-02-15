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
# <a name="microsoft-ole-db-provider-for-odbc"></a><span data-ttu-id="19a5b-102">Поставщик Microsoft OLE DB для ODBC</span><span class="sxs-lookup"><span data-stu-id="19a5b-102">Microsoft OLE DB Provider for ODBC</span></span>

<span data-ttu-id="19a5b-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="19a5b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="19a5b-104">Для программистов ADO или RDS идеальным миром будет тот, в котором каждый источник данных предоставляет интерфейс OLE DB, чтобы ADO мог вызываться непосредственно в источник данных.</span><span class="sxs-lookup"><span data-stu-id="19a5b-104">To an ADO or RDS programmer, an ideal world would be one in which every data source exposes an OLE DB interface, so that ADO could call directly into the data source.</span></span> <span data-ttu-id="19a5b-105">Хотя все больше поставщиков баз данных внедряют интерфейсы OLE DB, некоторые источники данных пока не реализованы таким образом.</span><span class="sxs-lookup"><span data-stu-id="19a5b-105">Although increasingly more database vendors are implementing OLE DB interfaces, some data sources are not yet exposed this way.</span></span> <span data-ttu-id="19a5b-106">Однако практически ко всем системам DBMS, которые используются в настоящее время, можно получить доступ через ODBC.</span><span class="sxs-lookup"><span data-stu-id="19a5b-106">However, virtually all DBMS systems in use today can be accessed through ODBC.</span></span>

<span data-ttu-id="19a5b-107">Драйверы ODBC доступны для всех основных DBMS, которые используются в настоящее время, включая Microsoft SQL Server, Microsoft Access (якорь субобъедий Microsoft Jet) и Microsoft FoxPro, в дополнение к продуктам баз данных, не относянымся к Майкрософт, таким как Oracle.</span><span class="sxs-lookup"><span data-stu-id="19a5b-107">ODBC drivers are available for every major DBMS in use today, including Microsoft SQL Server, Microsoft Access (Microsoft Jet database engine), and Microsoft FoxPro, in addition to non-Microsoft database products such as Oracle.</span></span>

<span data-ttu-id="19a5b-108">Однако поставщик Microsoft ODBC позволяет ADO подключаться к любому источнику данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="19a5b-108">The Microsoft ODBC Provider, however, allows ADO to connect to any ODBC data source.</span></span> <span data-ttu-id="19a5b-109">Поставщик имеет свободный поток и Юникод включен.</span><span class="sxs-lookup"><span data-stu-id="19a5b-109">The provider is free-threaded and Unicode enabled.</span></span>

<span data-ttu-id="19a5b-110">Поставщик поддерживает транзакции, хотя различные подмозки DBMS поддерживают различные типы транзакций.</span><span class="sxs-lookup"><span data-stu-id="19a5b-110">The provider supports transactions, although different DBMS engines offer different types of transaction support.</span></span> <span data-ttu-id="19a5b-111">Например, Microsoft Access поддерживает вложенные транзакции глубиной до пяти уровней.</span><span class="sxs-lookup"><span data-stu-id="19a5b-111">For example, Microsoft Access supports nested transactions up to five levels deep.</span></span>

<span data-ttu-id="19a5b-112">Это поставщик по умолчанию для ADO, и поддерживаются все зависящие от поставщика свойства и методы ADO.</span><span class="sxs-lookup"><span data-stu-id="19a5b-112">This is the default provider for ADO, and all provider-dependent ADO properties and methods are supported.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="19a5b-113">Параметры строки подключения</span><span class="sxs-lookup"><span data-stu-id="19a5b-113">Connection String Parameters</span></span>

<span data-ttu-id="19a5b-114">Чтобы подключиться к этому поставщику, установите для аргумента **Provider=** свойства [ConnectionString:](connectionstring-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="19a5b-114">To connect to this provider, set the **Provider=** argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```sql 
 
MSDASQL 
```

<span data-ttu-id="19a5b-115">При [чтении свойства Provider](provider-property-ado.md) также возвращается эта строка.</span><span class="sxs-lookup"><span data-stu-id="19a5b-115">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="19a5b-116">Типичная строка подключения</span><span class="sxs-lookup"><span data-stu-id="19a5b-116">Typical Connection String</span></span>

<span data-ttu-id="19a5b-117">Типичная строка подключения для этого поставщика:</span><span class="sxs-lookup"><span data-stu-id="19a5b-117">A typical connection string for this provider is:</span></span>

```sql 
 
"Provider=MSDASQL;DSN=dsnName;UID=userName;PWD=userPassword;" 
```

<span data-ttu-id="19a5b-118">Строка состоит из таких ключевых слов:</span><span class="sxs-lookup"><span data-stu-id="19a5b-118">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="19a5b-119">Ключевое слово</span><span class="sxs-lookup"><span data-stu-id="19a5b-119">Keyword</span></span></p></th>
<th><p><span data-ttu-id="19a5b-120">Описание</span><span class="sxs-lookup"><span data-stu-id="19a5b-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-121"><strong>Поставщик</strong></span><span class="sxs-lookup"><span data-stu-id="19a5b-121"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="19a5b-122">Указывает поставщика OLE DB для ODBC.</span><span class="sxs-lookup"><span data-stu-id="19a5b-122">Specifies the OLE DB Provider for ODBC.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-123"><strong>DSN</strong></span><span class="sxs-lookup"><span data-stu-id="19a5b-123"><strong>DSN</strong></span></span></p></td>
<td><p><span data-ttu-id="19a5b-124">Указывает имя источника данных.</span><span class="sxs-lookup"><span data-stu-id="19a5b-124">Specifies the data source name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-125"><strong>UID</strong></span><span class="sxs-lookup"><span data-stu-id="19a5b-125"><strong>UID</strong></span></span></p></td>
<td><p><span data-ttu-id="19a5b-126">Задает имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="19a5b-126">Specifies the user name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-127"><strong>PWD</strong></span><span class="sxs-lookup"><span data-stu-id="19a5b-127"><strong>PWD</strong></span></span></p></td>
<td><p><span data-ttu-id="19a5b-128">Указывает пароль пользователя.</span><span class="sxs-lookup"><span data-stu-id="19a5b-128">Specifies the user password.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-129"><strong>URL-адрес</strong></span><span class="sxs-lookup"><span data-stu-id="19a5b-129"><strong>URL</strong></span></span></p></td>
<td><p><span data-ttu-id="19a5b-130">Указывает URL-адрес файла или каталога, опубликованного в веб-папке.</span><span class="sxs-lookup"><span data-stu-id="19a5b-130">Specifies the URL of a file or directory published in a web folder.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="19a5b-131">Так как это поставщик по умолчанию для ADO, если опустить параметр **Provider=** из строки подключения, ADO попытается установить подключение к этому поставщику.</span><span class="sxs-lookup"><span data-stu-id="19a5b-131">Because this is the default provider for ADO, if you omit the **Provider=** parameter from the connection string, ADO will attempt to establish a connection to this provider.</span></span>

<span data-ttu-id="19a5b-132">Поставщик не поддерживает какие-либо параметры подключения в дополнение к тем, которые определены ADO.</span><span class="sxs-lookup"><span data-stu-id="19a5b-132">The provider does not support any specific connection parameters in addition to those defined by ADO.</span></span> <span data-ttu-id="19a5b-133">Однако поставщик передает диспетчеру драйверов ODBC любые параметры подключения, не относячные к ADO.</span><span class="sxs-lookup"><span data-stu-id="19a5b-133">However, the provider will pass any non-ADO connection parameters to the ODBC driver manager.</span></span>

<span data-ttu-id="19a5b-134">Так как параметр **Provider** можно опустить, можно составить строку подключения ADO, идентичную строке подключения ODBC для того же источника данных.</span><span class="sxs-lookup"><span data-stu-id="19a5b-134">Because you can omit the **Provider** parameter, you can therefore compose an ADO connection string that is identical to an ODBC connection string for the same data source.</span></span> <span data-ttu-id="19a5b-135">Используйте те же имена параметров (**DRIVER=**, **DATABASE=**, **DSN=** и так далее), значения и синтаксис, как при составления строки подключения ODBC.</span><span class="sxs-lookup"><span data-stu-id="19a5b-135">Use the same parameter names (**DRIVER=**, **DATABASE=**, **DSN=**, and so on), values, and syntax as you would when composing an ODBC connection string.</span></span> <span data-ttu-id="19a5b-136">Можно подключиться к предопределенным имени источника данных (DSN) или FileDSN или без него.</span><span class="sxs-lookup"><span data-stu-id="19a5b-136">You can connect with or without a predefined data source name (DSN) or FileDSN.</span></span>

<span data-ttu-id="19a5b-137">**Синтаксис с DSN или FileDSN:**</span><span class="sxs-lookup"><span data-stu-id="19a5b-137">**Syntax with a DSN or FileDSN:**</span></span>

`"[Provider=MSDASQL;] { DSN=name | FileDSN=filename } ; [DATABASE=database;] UID=user; PWD=password"`

<span data-ttu-id="19a5b-138">**Синтаксис без DSN (подключение без DSN):**</span><span class="sxs-lookup"><span data-stu-id="19a5b-138">**Syntax without a DSN (DSN-less connection):**</span></span>

`"[Provider=MSDASQL;] DRIVER=driver; SERVER=server;DATABASE=database; UID=user; PWD=password"`

<span data-ttu-id="19a5b-139">Если используется **DSN** или **FileDSN,** его необходимо определить с помощью администратора источника данных ODBC на панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="19a5b-139">If you use a **DSN** or **FileDSN**, it must be defined through the ODBC Data Source Administrator in the Windows Control Panel.</span></span> <span data-ttu-id="19a5b-140">В Microsoft Windows 2000 администратор ODBC находится в области администрирования.</span><span class="sxs-lookup"><span data-stu-id="19a5b-140">In Microsoft Windows 2000, the ODBC Administrator is located under Administrative Tools.</span></span> <span data-ttu-id="19a5b-141">В предыдущих версиях Windows значок администратора ODBC назывался **32-битным ODBC** или просто **ODBC.**</span><span class="sxs-lookup"><span data-stu-id="19a5b-141">In previous versions of Windows, the ODBC Administrator icon is named **32-bit ODBC** or simply **ODBC**.</span></span>

<span data-ttu-id="19a5b-142">В качестве альтернативы настройке **DSN** можно указать драйвер ODBC (**DRIVER=**), например "SQL Server;" имя сервера (**SERVER=**); и имя базы данных (**DATABASE=**).</span><span class="sxs-lookup"><span data-stu-id="19a5b-142">As an alternative to setting a **DSN**, you can specify the ODBC driver (**DRIVER=**), such as "SQL Server;" the server name (**SERVER=**); and the database name (**DATABASE=**).</span></span>

<span data-ttu-id="19a5b-143">Вы также можете указать имя учетной записи пользователя **(UID=**) и пароль для учетной записи пользователя (**PWD=**) в параметрах, характерных для ODBC, или в стандартных параметрах пользователя и пароля, определяемого ADO.  </span><span class="sxs-lookup"><span data-stu-id="19a5b-143">You can also specify a user account name (**UID=**), and the password for the user account (**PWD=**) in the ODBC-specific parameters or in the standard ADO-defined *user* and *password* parameters.</span></span>

<span data-ttu-id="19a5b-144">Хотя определение   **DSN** уже указывает базу данных, можно указать параметр базы данных в дополнение к **DSN** для подключения к другой базе данных.</span><span class="sxs-lookup"><span data-stu-id="19a5b-144">Although a **DSN** definition already specifies a database, you can specify *a* *database* parameter in addition to a **DSN** to connect to a different database.</span></span> <span data-ttu-id="19a5b-145">При использовании **DSN**   лучше всегда включать параметр базы данных.</span><span class="sxs-lookup"><span data-stu-id="19a5b-145">It is a good idea to always include *the* *database* parameter when you use a **DSN**.</span></span> <span data-ttu-id="19a5b-146">Это обеспечит подключение к соответствующей базе данных в случае, если другой пользователь изменил параметр базы данных по умолчанию с момента последней проверки **определения DSN.**</span><span class="sxs-lookup"><span data-stu-id="19a5b-146">This will ensure that you connect to the proper database in the event that another user changed the default database parameter since you last checked the **DSN** definition.</span></span>

## <a name="provider-specific-connection-properties"></a><span data-ttu-id="19a5b-147">Provider-Specific подключения</span><span class="sxs-lookup"><span data-stu-id="19a5b-147">Provider-Specific Connection Properties</span></span>

<span data-ttu-id="19a5b-148">Поставщик OLE DB для ODBC добавляет несколько свойств в коллекцию [свойств](properties-collection-ado.md) объекта **Connection.**</span><span class="sxs-lookup"><span data-stu-id="19a5b-148">The OLE DB provider for ODBC adds several properties to the [Properties](properties-collection-ado.md) collection of the **Connection** object.</span></span> <span data-ttu-id="19a5b-149">В следующей таблице перечислены эти свойства с соответствующим именем свойства OLE DB в скобки.</span><span class="sxs-lookup"><span data-stu-id="19a5b-149">The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="19a5b-150">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="19a5b-150">Property Name</span></span></p></th>
<th><p><span data-ttu-id="19a5b-151">Описание</span><span class="sxs-lookup"><span data-stu-id="19a5b-151">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-152">Доступные процедуры</span><span class="sxs-lookup"><span data-stu-id="19a5b-152">Accessible Procedures</span></span><br />
<span data-ttu-id="19a5b-153">(KAGPROP_ACCESSIBLEPROCEDURES)</span><span class="sxs-lookup"><span data-stu-id="19a5b-153">(KAGPROP_ACCESSIBLEPROCEDURES)</span></span></p></td>
<td><p><span data-ttu-id="19a5b-154">Указывает, имеет ли пользователь доступ к хранимой процедуре.</span><span class="sxs-lookup"><span data-stu-id="19a5b-154">Indicates whether the user has access to stored procedures.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-155">Доступные таблицы</span><span class="sxs-lookup"><span data-stu-id="19a5b-155">Accessible Tables</span></span><br />
<span data-ttu-id="19a5b-156">(KAGPROP_ACCESSIBLETABLES)</span><span class="sxs-lookup"><span data-stu-id="19a5b-156">(KAGPROP_ACCESSIBLETABLES)</span></span></p></td>
<td><p><span data-ttu-id="19a5b-157">Указывает, имеет ли пользователь разрешение на выполнение заявлений SELECT для таблиц базы данных.</span><span class="sxs-lookup"><span data-stu-id="19a5b-157">Indicates whether the user has permission to execute SELECT statements against the database tables.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-158">Active Statements</span><span class="sxs-lookup"><span data-stu-id="19a5b-158">Active Statements</span></span><br />
<span data-ttu-id="19a5b-159">(KAGPROP_ACTIVESTATEMENTS)</span><span class="sxs-lookup"><span data-stu-id="19a5b-159">(KAGPROP_ACTIVESTATEMENTS)</span></span></p></td>
<td><p><span data-ttu-id="19a5b-160">Указывает количество работок, поддерживаемых драйвером ODBC для подключения.</span><span class="sxs-lookup"><span data-stu-id="19a5b-160">Indicates the number of handles an ODBC driver can support on a connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-161">Имя драйвера</span><span class="sxs-lookup"><span data-stu-id="19a5b-161">Driver Name</span></span><br />
<span data-ttu-id="19a5b-162">(KAGPROP_DRIVERNAME)</span><span class="sxs-lookup"><span data-stu-id="19a5b-162">(KAGPROP_DRIVERNAME)</span></span></p></td>
<td><p><span data-ttu-id="19a5b-163">Указывает имя файла драйвера ODBC.</span><span class="sxs-lookup"><span data-stu-id="19a5b-163">Indicates the file name of the ODBC driver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-164">Версия драйвера ODBC</span><span class="sxs-lookup"><span data-stu-id="19a5b-164">Driver ODBC Version</span></span><br />
<span data-ttu-id="19a5b-165">(KAGPROP_DRIVERODBCVER)</span><span class="sxs-lookup"><span data-stu-id="19a5b-165">(KAGPROP_DRIVERODBCVER)</span></span></p></td>
<td><p><span data-ttu-id="19a5b-166">Указывает версию ODBC, поддерживаемую этим драйвером.</span><span class="sxs-lookup"><span data-stu-id="19a5b-166">Indicates the version of ODBC that this driver supports.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-167">Использование файлов</span><span class="sxs-lookup"><span data-stu-id="19a5b-167">File Usage</span></span><br />
<span data-ttu-id="19a5b-168">(KAGPROP_FILEUSAGE)</span><span class="sxs-lookup"><span data-stu-id="19a5b-168">(KAGPROP_FILEUSAGE)</span></span></p></td>
<td><p><span data-ttu-id="19a5b-169">Указывает, как драйвер обрабатывает файл в источнике данных; в качестве таблицы или каталога.</span><span class="sxs-lookup"><span data-stu-id="19a5b-169">Indicates how the driver treats a file in a data source; as a table or as a catalog.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-170">Like Escape Clause</span><span class="sxs-lookup"><span data-stu-id="19a5b-170">Like Escape Clause</span></span><br />
<span data-ttu-id="19a5b-171">(KAGPROP_LIKEESCAPECLAUSE)</span><span class="sxs-lookup"><span data-stu-id="19a5b-171">(KAGPROP_LIKEESCAPECLAUSE)</span></span></p></td>
<td><p><span data-ttu-id="19a5b-172">Указывает, поддерживает ли драйвер определение и использование escape-символа для символа процента (%) и подчеркнуть знак (_) в предикате LIKE предложения WHERE.</span><span class="sxs-lookup"><span data-stu-id="19a5b-172">Indicates whether the driver supports the definition and use of an escape character for the percent character (%) and underline character (_) in the LIKE predicate of a WHERE clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-173">Max Columns in Group By</span><span class="sxs-lookup"><span data-stu-id="19a5b-173">Max Columns in Group By</span></span><br />
<span data-ttu-id="19a5b-174">(KAGPROP_MAXCOLUMNSINGROUPBY)</span><span class="sxs-lookup"><span data-stu-id="19a5b-174">(KAGPROP_MAXCOLUMNSINGROUPBY)</span></span></p></td>
<td><p><span data-ttu-id="19a5b-175">Указывает максимальное число столбцов, которые могут быть указаны в предложении GROUP BY для заявления SELECT.</span><span class="sxs-lookup"><span data-stu-id="19a5b-175">Indicates the maximum number of columns that can be listed in the GROUP BY clause of a SELECT statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-176">Максимальное время столбцов в индексе</span><span class="sxs-lookup"><span data-stu-id="19a5b-176">Max Columns in Index</span></span><br />
<span data-ttu-id="19a5b-177">(KAGPROP_MAXCOLUMNSININDEX)</span><span class="sxs-lookup"><span data-stu-id="19a5b-177">(KAGPROP_MAXCOLUMNSININDEX)</span></span></p></td>
<td><p><span data-ttu-id="19a5b-178">Указывает максимальное число столбцов, которые можно включить в индекс.</span><span class="sxs-lookup"><span data-stu-id="19a5b-178">Indicates the maximum number of columns that can be included in an index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-179">Максимальное по порядку столбцов</span><span class="sxs-lookup"><span data-stu-id="19a5b-179">Max Columns in Order By</span></span><br />
<span data-ttu-id="19a5b-180">(KAGPROP_MAXCOLUMNSINORDERBY)</span><span class="sxs-lookup"><span data-stu-id="19a5b-180">(KAGPROP_MAXCOLUMNSINORDERBY)</span></span></p></td>
<td><p><span data-ttu-id="19a5b-181">Указывает максимальное число столбцов, которые могут быть указаны в предложении ORDER BY для заявления SELECT.</span><span class="sxs-lookup"><span data-stu-id="19a5b-181">Indicates the maximum number of columns that can be listed in the ORDER BY clause of a SELECT statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-182">Максимальное время выбора столбцов</span><span class="sxs-lookup"><span data-stu-id="19a5b-182">Max Columns in Select</span></span><br />
<span data-ttu-id="19a5b-183">(KAGPROP_MAXCOLUMNSINSELECT)</span><span class="sxs-lookup"><span data-stu-id="19a5b-183">(KAGPROP_MAXCOLUMNSINSELECT)</span></span></p></td>
<td><p><span data-ttu-id="19a5b-184">Указывает максимальное число столбцов, которые могут быть указаны в части SELECT в выписке SELECT.</span><span class="sxs-lookup"><span data-stu-id="19a5b-184">Indicates the maximum number of columns that can be listed in the SELECT portion of a SELECT statement.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-185">Максимальное время столбцов в таблице</span><span class="sxs-lookup"><span data-stu-id="19a5b-185">Max Columns in Table</span></span><br />
<span data-ttu-id="19a5b-186">(KAGPROP_MAXCOLUMNSINTABLE)</span><span class="sxs-lookup"><span data-stu-id="19a5b-186">(KAGPROP_MAXCOLUMNSINTABLE)</span></span></p></td>
<td><p><span data-ttu-id="19a5b-187">Указывает максимальное число столбцов, разрешенных в таблице.</span><span class="sxs-lookup"><span data-stu-id="19a5b-187">Indicates the maximum number of columns allowed in a table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-188">Числимые функции</span><span class="sxs-lookup"><span data-stu-id="19a5b-188">Numeric Functions</span></span><br />
<span data-ttu-id="19a5b-189">(KAGPROP_NUMERICFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="19a5b-189">(KAGPROP_NUMERICFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="19a5b-190">Указывает, какие числимые функции поддерживаются драйвером ODBC.</span><span class="sxs-lookup"><span data-stu-id="19a5b-190">Indicates which numeric functions are supported by the ODBC driver.</span></span> <span data-ttu-id="19a5b-191">Список имен функций и связанных значений, используемых в этой битовойmask, см. в приложении E. Скалярные функции в документации ODBC.</span><span class="sxs-lookup"><span data-stu-id="19a5b-191">For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-192">Возможности внешнего join</span><span class="sxs-lookup"><span data-stu-id="19a5b-192">Outer Join Capabilities</span></span><br />
<span data-ttu-id="19a5b-193">(KAGPROP_OJCAPABILITY)</span><span class="sxs-lookup"><span data-stu-id="19a5b-193">(KAGPROP_OJCAPABILITY)</span></span></p></td>
<td><p><span data-ttu-id="19a5b-194">Указывает типы ВНЕШНИХ JOI, поддерживаемые поставщиком.</span><span class="sxs-lookup"><span data-stu-id="19a5b-194">Indicates the types of OUTER JOINs supported by the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-195">Внешние joins</span><span class="sxs-lookup"><span data-stu-id="19a5b-195">Outer Joins</span></span><br />
<span data-ttu-id="19a5b-196">(KAGPROP_OUTERJOINS)</span><span class="sxs-lookup"><span data-stu-id="19a5b-196">(KAGPROP_OUTERJOINS)</span></span></p></td>
<td><p><span data-ttu-id="19a5b-197">Указывает, поддерживает ли поставщик ВНЕШНИЕ JOI.</span><span class="sxs-lookup"><span data-stu-id="19a5b-197">Indicates whether the provider supports OUTER JOINs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-198">Специальные символы</span><span class="sxs-lookup"><span data-stu-id="19a5b-198">Special Characters</span></span><br />
<span data-ttu-id="19a5b-199">(KAGPROP_SPECIALCHARACTERS)</span><span class="sxs-lookup"><span data-stu-id="19a5b-199">(KAGPROP_SPECIALCHARACTERS)</span></span></p></td>
<td><p><span data-ttu-id="19a5b-200">Указывает, какие символы имеют особое значение для драйвера ODBC.</span><span class="sxs-lookup"><span data-stu-id="19a5b-200">Indicates which characters have special meaning for the ODBC driver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-201">Хранимые процедуры</span><span class="sxs-lookup"><span data-stu-id="19a5b-201">Stored Procedures</span></span><br />
<span data-ttu-id="19a5b-202">(KAGPROP_PROCEDURES)</span><span class="sxs-lookup"><span data-stu-id="19a5b-202">(KAGPROP_PROCEDURES)</span></span></p></td>
<td><p><span data-ttu-id="19a5b-203">Указывает, доступны ли хранимые процедуры для использования с этим драйвером ODBC.</span><span class="sxs-lookup"><span data-stu-id="19a5b-203">Indicates whether stored procedures are available for use with this ODBC driver.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-204">Строки функций</span><span class="sxs-lookup"><span data-stu-id="19a5b-204">String Functions</span></span><br />
<span data-ttu-id="19a5b-205">(KAGPROP_STRINGFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="19a5b-205">(KAGPROP_STRINGFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="19a5b-206">Указывает, какие строки поддерживаются драйвером ODBC.</span><span class="sxs-lookup"><span data-stu-id="19a5b-206">Indicates which string functions are supported by the ODBC driver.</span></span> <span data-ttu-id="19a5b-207">Список имен функций и связанных значений, используемых в этой битовойmask, см. в приложении E. Скалярные функции в документации ODBC.</span><span class="sxs-lookup"><span data-stu-id="19a5b-207">For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-208">Системные функции</span><span class="sxs-lookup"><span data-stu-id="19a5b-208">System Functions</span></span><br />
<span data-ttu-id="19a5b-209">(KAGPROP_SYSTEMFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="19a5b-209">(KAGPROP_SYSTEMFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="19a5b-210">Указывает, какие системные функции поддерживаются драйвером ODBC.</span><span class="sxs-lookup"><span data-stu-id="19a5b-210">Indicates which system functions are supported by the ODBC driver.</span></span> <span data-ttu-id="19a5b-211">Список имен функций и связанных значений, используемых в этой битовойmask, см. в приложении E. Скалярные функции в документации ODBC.</span><span class="sxs-lookup"><span data-stu-id="19a5b-211">For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-212">Функции времени и даты</span><span class="sxs-lookup"><span data-stu-id="19a5b-212">Time/Date Functions</span></span><br />
<span data-ttu-id="19a5b-213">(KAGPROP_TIMEDATEFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="19a5b-213">(KAGPROP_TIMEDATEFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="19a5b-214">Указывает, какие функции времени и даты поддерживаются драйвером ODBC.</span><span class="sxs-lookup"><span data-stu-id="19a5b-214">Indicates which time and date functions are supported by the ODBC driver.</span></span> <span data-ttu-id="19a5b-215">Список имен функций и связанных значений, используемых в этой битовойmask, см. в приложении E. Скалярные функции в документации ODBC.</span><span class="sxs-lookup"><span data-stu-id="19a5b-215">For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-216">SQL грамматики</span><span class="sxs-lookup"><span data-stu-id="19a5b-216">SQL Grammar Support</span></span><br />
<span data-ttu-id="19a5b-217">(KAGPROP_ODBCSQLCONFORMANCE)</span><span class="sxs-lookup"><span data-stu-id="19a5b-217">(KAGPROP_ODBCSQLCONFORMANCE)</span></span></p></td>
<td><p><span data-ttu-id="19a5b-218">Указывает SQL, поддерживаемую драйвером ODBC.</span><span class="sxs-lookup"><span data-stu-id="19a5b-218">Indicates the SQL grammar that the ODBC driver supports.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-recordset-and-command-properties"></a><span data-ttu-id="19a5b-219">Provider-Specific Recordset and Command Properties</span><span class="sxs-lookup"><span data-stu-id="19a5b-219">Provider-Specific Recordset and Command Properties</span></span>

<span data-ttu-id="19a5b-220">Поставщик OLE DB для ODBC добавляет несколько свойств в коллекцию **свойств** объектов **Recordset** и **Command.**</span><span class="sxs-lookup"><span data-stu-id="19a5b-220">The OLE DB provider for ODBC adds several properties to the **Properties** collection of the **Recordset** and **Command** objects.</span></span> <span data-ttu-id="19a5b-221">В следующей таблице перечислены эти свойства с соответствующим именем свойства OLE DB в скобки.</span><span class="sxs-lookup"><span data-stu-id="19a5b-221">The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="19a5b-222">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="19a5b-222">Property Name</span></span></p></th>
<th><p><span data-ttu-id="19a5b-223">Описание</span><span class="sxs-lookup"><span data-stu-id="19a5b-223">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-224">Обновления на основе запросов/удаления и вставки</span><span class="sxs-lookup"><span data-stu-id="19a5b-224">Query Based Updates/Deletes/Inserts</span></span><br />
<span data-ttu-id="19a5b-225">(KAGPROP_QUERYBASEDUPDATES)</span><span class="sxs-lookup"><span data-stu-id="19a5b-225">(KAGPROP_QUERYBASEDUPDATES)</span></span></p></td>
<td><p><span data-ttu-id="19a5b-226">Указывает, можно ли выполнять обновления, удаления и вставки с помощью SQL запросов.</span><span class="sxs-lookup"><span data-stu-id="19a5b-226">Indicates whether updates, deletions, and insertions can be performed using SQL queries.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-227">Тип concurrency ODBC</span><span class="sxs-lookup"><span data-stu-id="19a5b-227">ODBC Concurrency Type</span></span><br />
<span data-ttu-id="19a5b-228">(KAGPROP_CONCURRENCY)</span><span class="sxs-lookup"><span data-stu-id="19a5b-228">(KAGPROP_CONCURRENCY)</span></span></p></td>
<td><p><span data-ttu-id="19a5b-229">Указывает метод, используемый для снижения потенциальных проблем, вызванных двумя пользователями, пытающихся получить доступ к одному и тем же данным из источника данных одновременно.</span><span class="sxs-lookup"><span data-stu-id="19a5b-229">Indicates the method used to reduce potential problems caused by two users attempting to access the same data from the data source simultaneously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-230">Доступность BLOB-Forward-Only курсора</span><span class="sxs-lookup"><span data-stu-id="19a5b-230">BLOB accessibility on Forward-Only cursor</span></span><br />
<span data-ttu-id="19a5b-231">(KAGPROP_BLOBSONFOCURSOR)</span><span class="sxs-lookup"><span data-stu-id="19a5b-231">(KAGPROP_BLOBSONFOCURSOR)</span></span></p></td>
<td><p><span data-ttu-id="19a5b-232">Указывает, можно ли получить доступ к полям <strong>BLOB</strong> при использовании курсора "Только вперед".</span><span class="sxs-lookup"><span data-stu-id="19a5b-232">Indicates whether BLOB <strong>Fields</strong> can be accessed when using a forward-only cursor.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-233">Включить SQL_FLOAT, SQL_DOUBLE и SQL_REAL в предложения QBU WHERE</span><span class="sxs-lookup"><span data-stu-id="19a5b-233">Include SQL_FLOAT, SQL_DOUBLE, and SQL_REAL in QBU WHERE clauses</span></span><br />
<span data-ttu-id="19a5b-234">(KAGPROP_INCLUDENONEXACT)</span><span class="sxs-lookup"><span data-stu-id="19a5b-234">(KAGPROP_INCLUDENONEXACT)</span></span></p></td>
<td><p><span data-ttu-id="19a5b-235">Указывает, можно ли включить значения SQL_FLOAT, SQL_DOUBLE и SQL_REAL в предложение QBU WHERE.</span><span class="sxs-lookup"><span data-stu-id="19a5b-235">Indicates whether SQL_FLOAT, SQL_DOUBLE, and SQL_REAL values can be included in a QBU WHERE clause.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-236">Положение последней строки после вставки</span><span class="sxs-lookup"><span data-stu-id="19a5b-236">Position on the last row after insert</span></span><br />
<span data-ttu-id="19a5b-237">(KAGPROP_POSITIONONNEWROW)</span><span class="sxs-lookup"><span data-stu-id="19a5b-237">(KAGPROP_POSITIONONNEWROW)</span></span></p></td>
<td><p><span data-ttu-id="19a5b-238">Указывает, что после вставки новой записи в таблицу в последнюю строку таблицы будет вводиться текущая строка.</span><span class="sxs-lookup"><span data-stu-id="19a5b-238">Indicates that after a new record has been inserted in a table, the last row in the table will be come the current row.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-239">IRowsetChangeExtInfo</span><span class="sxs-lookup"><span data-stu-id="19a5b-239">IRowsetChangeExtInfo</span></span><br />
<span data-ttu-id="19a5b-240">(KAGPROP_IROWSETCHANGEEXTINFO)</span><span class="sxs-lookup"><span data-stu-id="19a5b-240">(KAGPROP_IROWSETCHANGEEXTINFO)</span></span></p></td>
<td><p><span data-ttu-id="19a5b-241">Указывает, предоставляет ли <strong>интерфейс IRowsetChange</strong> расширенную поддержку информации.</span><span class="sxs-lookup"><span data-stu-id="19a5b-241">Indicates whether the <strong>IRowsetChange</strong> interface provides extended information support.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-242">Тип курсора ODBC</span><span class="sxs-lookup"><span data-stu-id="19a5b-242">ODBC Cursor Type</span></span><br />
<span data-ttu-id="19a5b-243">(KAGPROP_CURSOR)</span><span class="sxs-lookup"><span data-stu-id="19a5b-243">(KAGPROP_CURSOR)</span></span></p></td>
<td><p><span data-ttu-id="19a5b-244">Указывает тип курсора, используемого набором <strong>записей.</strong></span><span class="sxs-lookup"><span data-stu-id="19a5b-244">Indicates the type of cursor used by the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-245">Создание наборов строк, которые можно маршалировать</span><span class="sxs-lookup"><span data-stu-id="19a5b-245">Generate a Rowset that can be marshaled</span></span><br />
<span data-ttu-id="19a5b-246">(KAGPROP_MARSHALLABLE)</span><span class="sxs-lookup"><span data-stu-id="19a5b-246">(KAGPROP_MARSHALLABLE)</span></span></p></td>
<td><p><span data-ttu-id="19a5b-247">Указывает, что драйвер ODBC создает набор записей, который можно маршалировать</span><span class="sxs-lookup"><span data-stu-id="19a5b-247">Indicates that the ODBC driver generates a recordset that can be marshaled</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-text"></a><span data-ttu-id="19a5b-248">Текст команды</span><span class="sxs-lookup"><span data-stu-id="19a5b-248">Command Text</span></span>

<span data-ttu-id="19a5b-249">Использование объекта [Command](command-object-ado.md) во многом зависит от источника данных и типа запроса или командной команды, которые он будет принимать.</span><span class="sxs-lookup"><span data-stu-id="19a5b-249">How you use the [Command](command-object-ado.md) object largely depends on the data source, and what type of query or command statement it will accept.</span></span>

<span data-ttu-id="19a5b-250">ODBC предоставляет определенный синтаксис для вызовов хранимой процедуры.</span><span class="sxs-lookup"><span data-stu-id="19a5b-250">ODBC provides a specific syntax for calling stored procedures.</span></span> <span data-ttu-id="19a5b-251">Для свойства [CommandText](commandtext-property-ado.md) объекта **Command** аргумент *CommandText* **методу Execute** объекта [Connection](connection-object-ado.md) или аргумент *Source* **методу Open** в [объекте Recordset](recordset-object-ado.md) передает строку с помощью этого синтаксиса:</span><span class="sxs-lookup"><span data-stu-id="19a5b-251">For the [CommandText](commandtext-property-ado.md) property of a **Command** object, the *CommandText* argument to the **Execute** method on a [Connection](connection-object-ado.md) object, or the *Source* argument to the **Open** method on a [Recordset](recordset-object-ado.md) object, passes in a string with this syntax:</span></span>

`"{ [ ? = ] call procedure [ ( ? [, ? [ ,  ]] ) ] }"`

<span data-ttu-id="19a5b-252">Each **?**</span><span class="sxs-lookup"><span data-stu-id="19a5b-252">Each **?**</span></span> <span data-ttu-id="19a5b-253">ссылка на объект в коллекции [Parameters.](parameters-collection-ado.md)</span><span class="sxs-lookup"><span data-stu-id="19a5b-253">references an object in the [Parameters](parameters-collection-ado.md) collection.</span></span> <span data-ttu-id="19a5b-254">Первый **?**</span><span class="sxs-lookup"><span data-stu-id="19a5b-254">The first **?**</span></span> <span data-ttu-id="19a5b-255">references **Parameters**(0), the next **?**</span><span class="sxs-lookup"><span data-stu-id="19a5b-255">references **Parameters**(0), the next **?**</span></span> <span data-ttu-id="19a5b-256">references **Parameters**(1) и так далее.</span><span class="sxs-lookup"><span data-stu-id="19a5b-256">references **Parameters**(1), and so on.</span></span>

<span data-ttu-id="19a5b-257">Ссылки на параметры являются необязательными и зависят от структуры хранимой процедуры.</span><span class="sxs-lookup"><span data-stu-id="19a5b-257">The parameter references are optional and depend on the structure of the stored procedure.</span></span> <span data-ttu-id="19a5b-258">Если вы хотите вызвать хранимую процедуру, которая не определяет параметры, строка будет выглядеть так:</span><span class="sxs-lookup"><span data-stu-id="19a5b-258">If you want to call a stored procedure that defines no parameters, your string would look like this:</span></span>

`"{ call procedure }"`

<span data-ttu-id="19a5b-259">Если у вас есть два параметра запроса, строка будет выглядеть так:</span><span class="sxs-lookup"><span data-stu-id="19a5b-259">If you have two query parameters, your string would look like this:</span></span>

`"{ call procedure ( ?, ? ) }"`

<span data-ttu-id="19a5b-260">Если хранимая процедура возвращает значение, возвращаемого значения рассматривается как другой параметр.</span><span class="sxs-lookup"><span data-stu-id="19a5b-260">If the stored procedure will return a value, the return value is treated as another parameter.</span></span> <span data-ttu-id="19a5b-261">Если у вас нет параметров запроса, но есть возвращаемая строка, строка будет выглядеть так:</span><span class="sxs-lookup"><span data-stu-id="19a5b-261">If you have no query parameters but you do have a return value, your string would look like this:</span></span>

`"{ ? = call procedure }"`

<span data-ttu-id="19a5b-262">Наконец, если у вас есть возвращаемая строка и два параметра запроса, строка будет выглядеть так:</span><span class="sxs-lookup"><span data-stu-id="19a5b-262">Finally, if you have a return value and two query parameters, your string would look like this:</span></span>

`"{ ? = call procedure ( ?, ? ) }"`

## <a name="recordset-behavior"></a><span data-ttu-id="19a5b-263">Поведение наборов записей</span><span class="sxs-lookup"><span data-stu-id="19a5b-263">Recordset Behavior</span></span>

<span data-ttu-id="19a5b-264">В следующих таблицах фиксировать стандартные методы и свойства ADO, доступные для объекта **Recordset,** открытого с помощью этого поставщика.</span><span class="sxs-lookup"><span data-stu-id="19a5b-264">The following tables list the standard ADO methods and properties available on a **Recordset** object opened with this provider.</span></span>

<span data-ttu-id="19a5b-265">Для получения более подробных сведений о поведении **объекта Recordset** для конфигурации поставщика запустите метод [Supports](supports-method-ado.md) и нумеруйте коллекцию **свойств** объекта **Recordset,** чтобы определить, присутствуют ли динамические свойства для конкретного поставщика.</span><span class="sxs-lookup"><span data-stu-id="19a5b-265">For more detailed information about **Recordset** behavior for your provider configuration, run the [Supports](supports-method-ado.md) method and enumerate the **Properties** collection of the **Recordset** to determine whether provider-specific dynamic properties are present.</span></span>

<span data-ttu-id="19a5b-266">Доступность стандартных свойств объекта **ADO Recordset:**</span><span class="sxs-lookup"><span data-stu-id="19a5b-266">Availability of standard ADO **Recordset** properties:</span></span>

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
<th><p><span data-ttu-id="19a5b-267">Свойство</span><span class="sxs-lookup"><span data-stu-id="19a5b-267">Property</span></span></p></th>
<th><p><span data-ttu-id="19a5b-268">ForwardOnly</span><span class="sxs-lookup"><span data-stu-id="19a5b-268">ForwardOnly</span></span></p></th>
<th><p><span data-ttu-id="19a5b-269">Динамическая группа</span><span class="sxs-lookup"><span data-stu-id="19a5b-269">Dynamic</span></span></p></th>
<th><p><span data-ttu-id="19a5b-270">Keyset</span><span class="sxs-lookup"><span data-stu-id="19a5b-270">Keyset</span></span></p></th>
<th><p><span data-ttu-id="19a5b-271">Статическое</span><span class="sxs-lookup"><span data-stu-id="19a5b-271">Static</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-272"><a href="absolutepage-property-ado.md">AbsolutePage</a></span><span class="sxs-lookup"><span data-stu-id="19a5b-272"><a href="absolutepage-property-ado.md">AbsolutePage</a></span></span></p></td>
<td><p><span data-ttu-id="19a5b-273">недоступно</span><span class="sxs-lookup"><span data-stu-id="19a5b-273">not available</span></span></p></td>
<td><p><span data-ttu-id="19a5b-274">недоступно</span><span class="sxs-lookup"><span data-stu-id="19a5b-274">not available</span></span></p></td>
<td><p><span data-ttu-id="19a5b-275">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="19a5b-275">read/write</span></span></p></td>
<td><p><span data-ttu-id="19a5b-276">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="19a5b-276">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-277"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span><span class="sxs-lookup"><span data-stu-id="19a5b-277"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span></span></p></td>
<td><p><span data-ttu-id="19a5b-278">недоступно</span><span class="sxs-lookup"><span data-stu-id="19a5b-278">not available</span></span></p></td>
<td><p><span data-ttu-id="19a5b-279">недоступно</span><span class="sxs-lookup"><span data-stu-id="19a5b-279">not available</span></span></p></td>
<td><p><span data-ttu-id="19a5b-280">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="19a5b-280">read/write</span></span></p></td>
<td><p><span data-ttu-id="19a5b-281">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="19a5b-281">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-282"><a href="activeconnection-property-ado.md">ActiveConnection</a></span><span class="sxs-lookup"><span data-stu-id="19a5b-282"><a href="activeconnection-property-ado.md">ActiveConnection</a></span></span></p></td>
<td><p><span data-ttu-id="19a5b-283">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="19a5b-283">read/write</span></span></p></td>
<td><p><span data-ttu-id="19a5b-284">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="19a5b-284">read/write</span></span></p></td>
<td><p><span data-ttu-id="19a5b-285">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="19a5b-285">read/write</span></span></p></td>
<td><p><span data-ttu-id="19a5b-286">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="19a5b-286">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-287"><a href="bof-eof-properties-ado.md">BOF</a></span><span class="sxs-lookup"><span data-stu-id="19a5b-287"><a href="bof-eof-properties-ado.md">BOF</a></span></span></p></td>
<td><p><span data-ttu-id="19a5b-288">read-only</span><span class="sxs-lookup"><span data-stu-id="19a5b-288">read-only</span></span></p></td>
<td><p><span data-ttu-id="19a5b-289">read-only</span><span class="sxs-lookup"><span data-stu-id="19a5b-289">read-only</span></span></p></td>
<td><p><span data-ttu-id="19a5b-290">read-only</span><span class="sxs-lookup"><span data-stu-id="19a5b-290">read-only</span></span></p></td>
<td><p><span data-ttu-id="19a5b-291">read-only</span><span class="sxs-lookup"><span data-stu-id="19a5b-291">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-292"><a href="bookmark-property-ado.md">Bookmark</a></span><span class="sxs-lookup"><span data-stu-id="19a5b-292"><a href="bookmark-property-ado.md">Bookmark</a></span></span></p></td>
<td><p><span data-ttu-id="19a5b-293">недоступно</span><span class="sxs-lookup"><span data-stu-id="19a5b-293">not available</span></span></p></td>
<td><p><span data-ttu-id="19a5b-294">недоступно</span><span class="sxs-lookup"><span data-stu-id="19a5b-294">not available</span></span></p></td>
<td><p><span data-ttu-id="19a5b-295">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="19a5b-295">read/write</span></span></p></td>
<td><p><span data-ttu-id="19a5b-296">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="19a5b-296">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-297"><a href="cachesize-property-ado.md">CacheSize</a></span><span class="sxs-lookup"><span data-stu-id="19a5b-297"><a href="cachesize-property-ado.md">CacheSize</a></span></span></p></td>
<td><p><span data-ttu-id="19a5b-298">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="19a5b-298">read/write</span></span></p></td>
<td><p><span data-ttu-id="19a5b-299">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="19a5b-299">read/write</span></span></p></td>
<td><p><span data-ttu-id="19a5b-300">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="19a5b-300">read/write</span></span></p></td>
<td><p><span data-ttu-id="19a5b-301">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="19a5b-301">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-302"><a href="cursorlocation-property-ado.md">CursorLocation</a></span><span class="sxs-lookup"><span data-stu-id="19a5b-302"><a href="cursorlocation-property-ado.md">CursorLocation</a></span></span></p></td>
<td><p><span data-ttu-id="19a5b-303">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="19a5b-303">read/write</span></span></p></td>
<td><p><span data-ttu-id="19a5b-304">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="19a5b-304">read/write</span></span></p></td>
<td><p><span data-ttu-id="19a5b-305">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="19a5b-305">read/write</span></span></p></td>
<td><p><span data-ttu-id="19a5b-306">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="19a5b-306">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-307"><a href="cursortype-property-ado.md">CursorType</a></span><span class="sxs-lookup"><span data-stu-id="19a5b-307"><a href="cursortype-property-ado.md">CursorType</a></span></span></p></td>
<td><p><span data-ttu-id="19a5b-308">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="19a5b-308">read/write</span></span></p></td>
<td><p><span data-ttu-id="19a5b-309">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="19a5b-309">read/write</span></span></p></td>
<td><p><span data-ttu-id="19a5b-310">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="19a5b-310">read/write</span></span></p></td>
<td><p><span data-ttu-id="19a5b-311">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="19a5b-311">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-312"><a href="editmode-property-ado.md">EditMode</a></span><span class="sxs-lookup"><span data-stu-id="19a5b-312"><a href="editmode-property-ado.md">EditMode</a></span></span></p></td>
<td><p><span data-ttu-id="19a5b-313">read-only</span><span class="sxs-lookup"><span data-stu-id="19a5b-313">read-only</span></span></p></td>
<td><p><span data-ttu-id="19a5b-314">read-only</span><span class="sxs-lookup"><span data-stu-id="19a5b-314">read-only</span></span></p></td>
<td><p><span data-ttu-id="19a5b-315">read-only</span><span class="sxs-lookup"><span data-stu-id="19a5b-315">read-only</span></span></p></td>
<td><p><span data-ttu-id="19a5b-316">read-only</span><span class="sxs-lookup"><span data-stu-id="19a5b-316">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-317"><a href="filter-property-ado.md">Фильтр</a></span><span class="sxs-lookup"><span data-stu-id="19a5b-317"><a href="filter-property-ado.md">Filter</a></span></span></p></td>
<td><p><span data-ttu-id="19a5b-318">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="19a5b-318">read/write</span></span></p></td>
<td><p><span data-ttu-id="19a5b-319">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="19a5b-319">read/write</span></span></p></td>
<td><p><span data-ttu-id="19a5b-320">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="19a5b-320">read/write</span></span></p></td>
<td><p><span data-ttu-id="19a5b-321">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="19a5b-321">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-322"><a href="locktype-property-ado.md">LockType</a></span><span class="sxs-lookup"><span data-stu-id="19a5b-322"><a href="locktype-property-ado.md">LockType</a></span></span></p></td>
<td><p><span data-ttu-id="19a5b-323">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="19a5b-323">read/write</span></span></p></td>
<td><p><span data-ttu-id="19a5b-324">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="19a5b-324">read/write</span></span></p></td>
<td><p><span data-ttu-id="19a5b-325">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="19a5b-325">read/write</span></span></p></td>
<td><p><span data-ttu-id="19a5b-326">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="19a5b-326">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-327"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span><span class="sxs-lookup"><span data-stu-id="19a5b-327"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span></span></p></td>
<td><p><span data-ttu-id="19a5b-328">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="19a5b-328">read/write</span></span></p></td>
<td><p><span data-ttu-id="19a5b-329">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="19a5b-329">read/write</span></span></p></td>
<td><p><span data-ttu-id="19a5b-330">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="19a5b-330">read/write</span></span></p></td>
<td><p><span data-ttu-id="19a5b-331">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="19a5b-331">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-332"><a href="maxrecords-property-ado.md">MaxRecords</a></span><span class="sxs-lookup"><span data-stu-id="19a5b-332"><a href="maxrecords-property-ado.md">MaxRecords</a></span></span></p></td>
<td><p><span data-ttu-id="19a5b-333">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="19a5b-333">read/write</span></span></p></td>
<td><p><span data-ttu-id="19a5b-334">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="19a5b-334">read/write</span></span></p></td>
<td><p><span data-ttu-id="19a5b-335">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="19a5b-335">read/write</span></span></p></td>
<td><p><span data-ttu-id="19a5b-336">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="19a5b-336">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-337"><a href="pagecount-property-ado.md">PageCount</a></span><span class="sxs-lookup"><span data-stu-id="19a5b-337"><a href="pagecount-property-ado.md">PageCount</a></span></span></p></td>
<td><p><span data-ttu-id="19a5b-338">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="19a5b-338">read/write</span></span></p></td>
<td><p><span data-ttu-id="19a5b-339">недоступен</span><span class="sxs-lookup"><span data-stu-id="19a5b-339">not available</span></span></p></td>
<td><p><span data-ttu-id="19a5b-340">read-only</span><span class="sxs-lookup"><span data-stu-id="19a5b-340">read-only</span></span></p></td>
<td><p><span data-ttu-id="19a5b-341">read-only</span><span class="sxs-lookup"><span data-stu-id="19a5b-341">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-342"><a href="pagesize-property-ado.md">PageSize</a></span><span class="sxs-lookup"><span data-stu-id="19a5b-342"><a href="pagesize-property-ado.md">PageSize</a></span></span></p></td>
<td><p><span data-ttu-id="19a5b-343">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="19a5b-343">read/write</span></span></p></td>
<td><p><span data-ttu-id="19a5b-344">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="19a5b-344">read/write</span></span></p></td>
<td><p><span data-ttu-id="19a5b-345">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="19a5b-345">read/write</span></span></p></td>
<td><p><span data-ttu-id="19a5b-346">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="19a5b-346">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-347"><a href="recordcount-property-ado.md">RecordCount</a></span><span class="sxs-lookup"><span data-stu-id="19a5b-347"><a href="recordcount-property-ado.md">RecordCount</a></span></span></p></td>
<td><p><span data-ttu-id="19a5b-348">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="19a5b-348">read/write</span></span></p></td>
<td><p><span data-ttu-id="19a5b-349">недоступен</span><span class="sxs-lookup"><span data-stu-id="19a5b-349">not available</span></span></p></td>
<td><p><span data-ttu-id="19a5b-350">read-only</span><span class="sxs-lookup"><span data-stu-id="19a5b-350">read-only</span></span></p></td>
<td><p><span data-ttu-id="19a5b-351">read-only</span><span class="sxs-lookup"><span data-stu-id="19a5b-351">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-352"><a href="source-property-ado-recordset.md">Source</a></span><span class="sxs-lookup"><span data-stu-id="19a5b-352"><a href="source-property-ado-recordset.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="19a5b-353">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="19a5b-353">read/write</span></span></p></td>
<td><p><span data-ttu-id="19a5b-354">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="19a5b-354">read/write</span></span></p></td>
<td><p><span data-ttu-id="19a5b-355">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="19a5b-355">read/write</span></span></p></td>
<td><p><span data-ttu-id="19a5b-356">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="19a5b-356">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-357"><a href="state-property-ado.md">State</a></span><span class="sxs-lookup"><span data-stu-id="19a5b-357"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="19a5b-358">read-only</span><span class="sxs-lookup"><span data-stu-id="19a5b-358">read-only</span></span></p></td>
<td><p><span data-ttu-id="19a5b-359">read-only</span><span class="sxs-lookup"><span data-stu-id="19a5b-359">read-only</span></span></p></td>
<td><p><span data-ttu-id="19a5b-360">read-only</span><span class="sxs-lookup"><span data-stu-id="19a5b-360">read-only</span></span></p></td>
<td><p><span data-ttu-id="19a5b-361">read-only</span><span class="sxs-lookup"><span data-stu-id="19a5b-361">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-362"><a href="status-property-ado-recordset.md">Состояние</a></span><span class="sxs-lookup"><span data-stu-id="19a5b-362"><a href="status-property-ado-recordset.md">Status</a></span></span></p></td>
<td><p><span data-ttu-id="19a5b-363">read-only</span><span class="sxs-lookup"><span data-stu-id="19a5b-363">read-only</span></span></p></td>
<td><p><span data-ttu-id="19a5b-364">read-only</span><span class="sxs-lookup"><span data-stu-id="19a5b-364">read-only</span></span></p></td>
<td><p><span data-ttu-id="19a5b-365">read-only</span><span class="sxs-lookup"><span data-stu-id="19a5b-365">read-only</span></span></p></td>
<td><p><span data-ttu-id="19a5b-366">read-only</span><span class="sxs-lookup"><span data-stu-id="19a5b-366">read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="19a5b-367">Свойства [AbsolutePosition](absoluteposition-property-ado.md) и [AbsolutePage](absolutepage-property-ado.md) используются только для записи, если ADO используется с версией 1.0 поставщика Microsoft OLE DB для ODBC.</span><span class="sxs-lookup"><span data-stu-id="19a5b-367">The [AbsolutePosition](absoluteposition-property-ado.md) and [AbsolutePage](absolutepage-property-ado.md) properties are write-only when ADO is used with version 1.0 of the Microsoft OLE DB Provider for ODBC.</span></span>

<span data-ttu-id="19a5b-368">Доступность стандартных методов ADO **Recordset:**</span><span class="sxs-lookup"><span data-stu-id="19a5b-368">Availability of standard ADO **Recordset** methods:</span></span>

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
<th><p><span data-ttu-id="19a5b-369">Method</span><span class="sxs-lookup"><span data-stu-id="19a5b-369">Method</span></span></p></th>
<th><p><span data-ttu-id="19a5b-370">ForwardOnly</span><span class="sxs-lookup"><span data-stu-id="19a5b-370">ForwardOnly</span></span></p></th>
<th><p><span data-ttu-id="19a5b-371">Динамическая группа</span><span class="sxs-lookup"><span data-stu-id="19a5b-371">Dynamic</span></span></p></th>
<th><p><span data-ttu-id="19a5b-372">Keyset</span><span class="sxs-lookup"><span data-stu-id="19a5b-372">Keyset</span></span></p></th>
<th><p><span data-ttu-id="19a5b-373">Статическое</span><span class="sxs-lookup"><span data-stu-id="19a5b-373">Static</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-374"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="19a5b-374"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="19a5b-375">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-375">Yes</span></span></p></td>
<td><p><span data-ttu-id="19a5b-376">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-376">Yes</span></span></p></td>
<td><p><span data-ttu-id="19a5b-377">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-377">Yes</span></span></p></td>
<td><p><span data-ttu-id="19a5b-378">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-378">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-379"><a href="cancel-method-ado.md">Отмена</a></span><span class="sxs-lookup"><span data-stu-id="19a5b-379"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="19a5b-380">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-380">Yes</span></span></p></td>
<td><p><span data-ttu-id="19a5b-381">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-381">Yes</span></span></p></td>
<td><p><span data-ttu-id="19a5b-382">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-382">Yes</span></span></p></td>
<td><p><span data-ttu-id="19a5b-383">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-383">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-384"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="19a5b-384"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="19a5b-385">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-385">Yes</span></span></p></td>
<td><p><span data-ttu-id="19a5b-386">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-386">Yes</span></span></p></td>
<td><p><span data-ttu-id="19a5b-387">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-387">Yes</span></span></p></td>
<td><p><span data-ttu-id="19a5b-388">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-388">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-389"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="19a5b-389"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="19a5b-390">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-390">Yes</span></span></p></td>
<td><p><span data-ttu-id="19a5b-391">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-391">Yes</span></span></p></td>
<td><p><span data-ttu-id="19a5b-392">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-392">Yes</span></span></p></td>
<td><p><span data-ttu-id="19a5b-393">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-393">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-394"><a href="clone-method-ado.md">Clone</a></span><span class="sxs-lookup"><span data-stu-id="19a5b-394"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="19a5b-395">Нет</span><span class="sxs-lookup"><span data-stu-id="19a5b-395">No</span></span></p></td>
<td><p><span data-ttu-id="19a5b-396">Нет</span><span class="sxs-lookup"><span data-stu-id="19a5b-396">No</span></span></p></td>
<td><p><span data-ttu-id="19a5b-397">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-397">Yes</span></span></p></td>
<td><p><span data-ttu-id="19a5b-398">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-398">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-399"><a href="close-method-ado.md">Close</a></span><span class="sxs-lookup"><span data-stu-id="19a5b-399"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="19a5b-400">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-400">Yes</span></span></p></td>
<td><p><span data-ttu-id="19a5b-401">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-401">Yes</span></span></p></td>
<td><p><span data-ttu-id="19a5b-402">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-402">Yes</span></span></p></td>
<td><p><span data-ttu-id="19a5b-403">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-403">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-404"><a href="delete-method-ado-recordset.md">удаление</a>;</span><span class="sxs-lookup"><span data-stu-id="19a5b-404"><a href="delete-method-ado-recordset.md">Delete</a></span></span></p></td>
<td><p><span data-ttu-id="19a5b-405">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-405">Yes</span></span></p></td>
<td><p><span data-ttu-id="19a5b-406">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-406">Yes</span></span></p></td>
<td><p><span data-ttu-id="19a5b-407">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-407">Yes</span></span></p></td>
<td><p><span data-ttu-id="19a5b-408">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-408">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-409"><a href="getrows-method-ado.md">GetRows</a></span><span class="sxs-lookup"><span data-stu-id="19a5b-409"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="19a5b-410">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-410">Yes</span></span></p></td>
<td><p><span data-ttu-id="19a5b-411">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-411">Yes</span></span></p></td>
<td><p><span data-ttu-id="19a5b-412">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-412">Yes</span></span></p></td>
<td><p><span data-ttu-id="19a5b-413">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-413">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-414"><a href="move-method-ado.md">Move</a></span><span class="sxs-lookup"><span data-stu-id="19a5b-414"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="19a5b-415">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-415">Yes</span></span></p></td>
<td><p><span data-ttu-id="19a5b-416">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-416">Yes</span></span></p></td>
<td><p><span data-ttu-id="19a5b-417">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-417">Yes</span></span></p></td>
<td><p><span data-ttu-id="19a5b-418">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-418">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-419"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span><span class="sxs-lookup"><span data-stu-id="19a5b-419"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span></span></p></td>
<td><p><span data-ttu-id="19a5b-420">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-420">Yes</span></span></p></td>
<td><p><span data-ttu-id="19a5b-421">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-421">Yes</span></span></p></td>
<td><p><span data-ttu-id="19a5b-422">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-422">Yes</span></span></p></td>
<td><p><span data-ttu-id="19a5b-423">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-423">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-424"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span><span class="sxs-lookup"><span data-stu-id="19a5b-424"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span></span></p></td>
<td><p><span data-ttu-id="19a5b-425">Нет</span><span class="sxs-lookup"><span data-stu-id="19a5b-425">No</span></span></p></td>
<td><p><span data-ttu-id="19a5b-426">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-426">Yes</span></span></p></td>
<td><p><span data-ttu-id="19a5b-427">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-427">Yes</span></span></p></td>
<td><p><span data-ttu-id="19a5b-428">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-428">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-429"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span><span class="sxs-lookup"><span data-stu-id="19a5b-429"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span></span></p></td>
<td><p><span data-ttu-id="19a5b-430">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-430">Yes</span></span></p></td>
<td><p><span data-ttu-id="19a5b-431">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-431">Yes</span></span></p></td>
<td><p><span data-ttu-id="19a5b-432">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-432">Yes</span></span></p></td>
<td><p><span data-ttu-id="19a5b-433">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-433">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-434"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span><span class="sxs-lookup"><span data-stu-id="19a5b-434"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span></span></p></td>
<td><p><span data-ttu-id="19a5b-435">Нет</span><span class="sxs-lookup"><span data-stu-id="19a5b-435">No</span></span></p></td>
<td><p><span data-ttu-id="19a5b-436">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-436">Yes</span></span></p></td>
<td><p><span data-ttu-id="19a5b-437">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-437">Yes</span></span></p></td>
<td><p><span data-ttu-id="19a5b-438">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-438">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-439"><a href="nextrecordset-method-ado.md">NextRecordset</a>\*</span><span class="sxs-lookup"><span data-stu-id="19a5b-439"><a href="nextrecordset-method-ado.md">NextRecordset</a>\*</span></span></p></td>
<td><p><span data-ttu-id="19a5b-440">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-440">Yes</span></span></p></td>
<td><p><span data-ttu-id="19a5b-441">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-441">Yes</span></span></p></td>
<td><p><span data-ttu-id="19a5b-442">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-442">Yes</span></span></p></td>
<td><p><span data-ttu-id="19a5b-443">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-443">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-444"><a href="open-method-ado-recordset.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="19a5b-444"><a href="open-method-ado-recordset.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="19a5b-445">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-445">Yes</span></span></p></td>
<td><p><span data-ttu-id="19a5b-446">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-446">Yes</span></span></p></td>
<td><p><span data-ttu-id="19a5b-447">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-447">Yes</span></span></p></td>
<td><p><span data-ttu-id="19a5b-448">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-448">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-449"><a href="requery-method-ado.md">Requery</a></span><span class="sxs-lookup"><span data-stu-id="19a5b-449"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="19a5b-450">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-450">Yes</span></span></p></td>
<td><p><span data-ttu-id="19a5b-451">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-451">Yes</span></span></p></td>
<td><p><span data-ttu-id="19a5b-452">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-452">Yes</span></span></p></td>
<td><p><span data-ttu-id="19a5b-453">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-453">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-454"><a href="resync-method-ado.md">Resync</a></span><span class="sxs-lookup"><span data-stu-id="19a5b-454"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="19a5b-455">Нет</span><span class="sxs-lookup"><span data-stu-id="19a5b-455">No</span></span></p></td>
<td><p><span data-ttu-id="19a5b-456">Нет</span><span class="sxs-lookup"><span data-stu-id="19a5b-456">No</span></span></p></td>
<td><p><span data-ttu-id="19a5b-457">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-457">Yes</span></span></p></td>
<td><p><span data-ttu-id="19a5b-458">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-458">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-459"><a href="supports-method-ado.md">Поддерживает</a></span><span class="sxs-lookup"><span data-stu-id="19a5b-459"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="19a5b-460">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-460">Yes</span></span></p></td>
<td><p><span data-ttu-id="19a5b-461">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-461">Yes</span></span></p></td>
<td><p><span data-ttu-id="19a5b-462">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-462">Yes</span></span></p></td>
<td><p><span data-ttu-id="19a5b-463">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-463">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-464"><a href="update-method-ado.md">обновление</a>.</span><span class="sxs-lookup"><span data-stu-id="19a5b-464"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="19a5b-465">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-465">Yes</span></span></p></td>
<td><p><span data-ttu-id="19a5b-466">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-466">Yes</span></span></p></td>
<td><p><span data-ttu-id="19a5b-467">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-467">Yes</span></span></p></td>
<td><p><span data-ttu-id="19a5b-468">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-468">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-469"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="19a5b-469"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="19a5b-470">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-470">Yes</span></span></p></td>
<td><p><span data-ttu-id="19a5b-471">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-471">Yes</span></span></p></td>
<td><p><span data-ttu-id="19a5b-472">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-472">Yes</span></span></p></td>
<td><p><span data-ttu-id="19a5b-473">Да</span><span class="sxs-lookup"><span data-stu-id="19a5b-473">Yes</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="19a5b-474">\*Не поддерживается для баз данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="19a5b-474">\*Not supported for Microsoft Access databases.</span></span>

## <a name="dynamic-properties"></a><span data-ttu-id="19a5b-475">Динамические свойства</span><span class="sxs-lookup"><span data-stu-id="19a5b-475">Dynamic Properties</span></span>

<span data-ttu-id="19a5b-476">Поставщик Microsoft OLE DB для ODBC вставляет несколько динамических свойств в коллекцию **свойств** неоплаченных объектов [Connection,](connection-object-ado.md) [Recordset](recordset-object-ado.md)и [Command.](command-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="19a5b-476">The Microsoft OLE DB Provider for ODBC inserts several dynamic properties into the **Properties** collection of the unopened [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md), and [Command](command-object-ado.md) objects.</span></span>

<span data-ttu-id="19a5b-477">Таблицы ниже — это перекрестный индекс имен ADO и OLE DB для каждого динамического свойства.</span><span class="sxs-lookup"><span data-stu-id="19a5b-477">The tables below are a cross-index of the ADO and OLE DB names for each dynamic property.</span></span> <span data-ttu-id="19a5b-478">Справочник программиста по OLE DB ссылается на имя свойства ADO по термину "Description".</span><span class="sxs-lookup"><span data-stu-id="19a5b-478">The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description."</span></span> <span data-ttu-id="19a5b-479">Дополнительные сведения об этих свойствах можно найти в справочнике программиста OLE DB.</span><span class="sxs-lookup"><span data-stu-id="19a5b-479">You can find more information about these properties in the OLE DB Programmer's Reference.</span></span> <span data-ttu-id="19a5b-480">Найди имя свойства OLE DB в индексе или см. приложение C. Свойства OLE DB.</span><span class="sxs-lookup"><span data-stu-id="19a5b-480">Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span></span>

## <a name="connection-dynamic-properties"></a><span data-ttu-id="19a5b-481">Динамические свойства подключения</span><span class="sxs-lookup"><span data-stu-id="19a5b-481">Connection Dynamic Properties</span></span>

<span data-ttu-id="19a5b-482">Следующие свойства добавляются в коллекцию  свойств объекта **Connection.**</span><span class="sxs-lookup"><span data-stu-id="19a5b-482">The following properties are added to the **Connection** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="19a5b-483">ADO Property Name</span><span class="sxs-lookup"><span data-stu-id="19a5b-483">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="19a5b-484">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="19a5b-484">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-485">Активные сеансы</span><span class="sxs-lookup"><span data-stu-id="19a5b-485">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="19a5b-486">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="19a5b-486">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-487">Asynchable Abort</span><span class="sxs-lookup"><span data-stu-id="19a5b-487">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="19a5b-488">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="19a5b-488">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-489">Asynchable Commit</span><span class="sxs-lookup"><span data-stu-id="19a5b-489">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="19a5b-490">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="19a5b-490">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-491">Уровни изоляции автозафикса</span><span class="sxs-lookup"><span data-stu-id="19a5b-491">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="19a5b-492">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="19a5b-492">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-493">Расположение каталога</span><span class="sxs-lookup"><span data-stu-id="19a5b-493">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="19a5b-494">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="19a5b-494">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-495">Термин каталога</span><span class="sxs-lookup"><span data-stu-id="19a5b-495">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="19a5b-496">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="19a5b-496">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-497">Определение столбца</span><span class="sxs-lookup"><span data-stu-id="19a5b-497">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="19a5b-498">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="19a5b-498">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-499">Время подключения</span><span class="sxs-lookup"><span data-stu-id="19a5b-499">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="19a5b-500">DBPROP_INIT_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="19a5b-500">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-501">Текущий каталог</span><span class="sxs-lookup"><span data-stu-id="19a5b-501">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="19a5b-502">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="19a5b-502">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-503">Источник данных</span><span class="sxs-lookup"><span data-stu-id="19a5b-503">Data Source</span></span></p></td>
<td><p><span data-ttu-id="19a5b-504">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="19a5b-504">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-505">Имя источника данных</span><span class="sxs-lookup"><span data-stu-id="19a5b-505">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="19a5b-506">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="19a5b-506">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-507">Потоковая модель объектов источника данных</span><span class="sxs-lookup"><span data-stu-id="19a5b-507">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="19a5b-508">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="19a5b-508">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-509">DBMS Name</span><span class="sxs-lookup"><span data-stu-id="19a5b-509">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="19a5b-510">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="19a5b-510">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-511">Версия DBMS</span><span class="sxs-lookup"><span data-stu-id="19a5b-511">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="19a5b-512">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="19a5b-512">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-513">Расширенные свойства</span><span class="sxs-lookup"><span data-stu-id="19a5b-513">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="19a5b-514">DBPROP_INIT_PROVIDERSTRING</span><span class="sxs-lookup"><span data-stu-id="19a5b-514">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-515">GROUP BY Support</span><span class="sxs-lookup"><span data-stu-id="19a5b-515">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="19a5b-516">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="19a5b-516">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-517">Поддержка разнородных таблиц</span><span class="sxs-lookup"><span data-stu-id="19a5b-517">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="19a5b-518">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="19a5b-518">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-519">Чувствительность к делу идентификатора</span><span class="sxs-lookup"><span data-stu-id="19a5b-519">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="19a5b-520">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="19a5b-520">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-521">Начальный каталог</span><span class="sxs-lookup"><span data-stu-id="19a5b-521">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="19a5b-522">DBPROP_INIT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="19a5b-522">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-523">Уровни изоляции</span><span class="sxs-lookup"><span data-stu-id="19a5b-523">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="19a5b-524">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="19a5b-524">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-525">Хранение изоляции</span><span class="sxs-lookup"><span data-stu-id="19a5b-525">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="19a5b-526">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="19a5b-526">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-527">Код локализовки</span><span class="sxs-lookup"><span data-stu-id="19a5b-527">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="19a5b-528">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="19a5b-528">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-529">Расположение</span><span class="sxs-lookup"><span data-stu-id="19a5b-529">Location</span></span></p></td>
<td><p><span data-ttu-id="19a5b-530">DBPROP_INIT_LOCATION</span><span class="sxs-lookup"><span data-stu-id="19a5b-530">DBPROP_INIT_LOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-531">Максимальный размер индекса</span><span class="sxs-lookup"><span data-stu-id="19a5b-531">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="19a5b-532">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="19a5b-532">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-533">Максимальный размер строки</span><span class="sxs-lookup"><span data-stu-id="19a5b-533">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="19a5b-534">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="19a5b-534">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-535">Максимальный размер строки включает BLOB</span><span class="sxs-lookup"><span data-stu-id="19a5b-535">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="19a5b-536">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="19a5b-536">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-537">Максимальное число таблиц в SELECT</span><span class="sxs-lookup"><span data-stu-id="19a5b-537">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="19a5b-538">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="19a5b-538">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-539">Режим</span><span class="sxs-lookup"><span data-stu-id="19a5b-539">Mode</span></span></p></td>
<td><p><span data-ttu-id="19a5b-540">DBPROP_INIT_MODE</span><span class="sxs-lookup"><span data-stu-id="19a5b-540">DBPROP_INIT_MODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-541">Несколько наборов параметров</span><span class="sxs-lookup"><span data-stu-id="19a5b-541">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="19a5b-542">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="19a5b-542">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-543">Несколько результатов</span><span class="sxs-lookup"><span data-stu-id="19a5b-543">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="19a5b-544">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="19a5b-544">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-545">Несколько объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="19a5b-545">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="19a5b-546">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="19a5b-546">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-547">Обновление с несколькими таблицами</span><span class="sxs-lookup"><span data-stu-id="19a5b-547">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="19a5b-548">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="19a5b-548">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-549">Порядок оценки NULL</span><span class="sxs-lookup"><span data-stu-id="19a5b-549">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="19a5b-550">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="19a5b-550">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-551">Поведение при конкатенации NULL</span><span class="sxs-lookup"><span data-stu-id="19a5b-551">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="19a5b-552">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="19a5b-552">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-553">Службы OLE DB</span><span class="sxs-lookup"><span data-stu-id="19a5b-553">OLE DB Services</span></span></p></td>
<td><p><span data-ttu-id="19a5b-554">DBPROP_INIT_OLEDBSERVICES</span><span class="sxs-lookup"><span data-stu-id="19a5b-554">DBPROP_INIT_OLEDBSERVICES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-555">Версия OLE DB</span><span class="sxs-lookup"><span data-stu-id="19a5b-555">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="19a5b-556">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="19a5b-556">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-557">Поддержка объектов OLE</span><span class="sxs-lookup"><span data-stu-id="19a5b-557">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="19a5b-558">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="19a5b-558">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-559">Поддержка открытого наборов строк</span><span class="sxs-lookup"><span data-stu-id="19a5b-559">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="19a5b-560">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="19a5b-560">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-561">ORDER BY Columns in Select List</span><span class="sxs-lookup"><span data-stu-id="19a5b-561">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="19a5b-562">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="19a5b-562">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-563">Доступность выходных параметров</span><span class="sxs-lookup"><span data-stu-id="19a5b-563">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="19a5b-564">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="19a5b-564">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-565">Password</span><span class="sxs-lookup"><span data-stu-id="19a5b-565">Password</span></span></p></td>
<td><p><span data-ttu-id="19a5b-566">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="19a5b-566">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-567">Pass By Ref Accessors</span><span class="sxs-lookup"><span data-stu-id="19a5b-567">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="19a5b-568">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="19a5b-568">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-569">Сохранить сведения о безопасности</span><span class="sxs-lookup"><span data-stu-id="19a5b-569">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="19a5b-570">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span><span class="sxs-lookup"><span data-stu-id="19a5b-570">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-571">Тип сохраняемого ИД</span><span class="sxs-lookup"><span data-stu-id="19a5b-571">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="19a5b-572">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="19a5b-572">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-573">Подготовка поведения для отменить</span><span class="sxs-lookup"><span data-stu-id="19a5b-573">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="19a5b-574">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="19a5b-574">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-575">Подготовка поведения фиксации</span><span class="sxs-lookup"><span data-stu-id="19a5b-575">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="19a5b-576">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="19a5b-576">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-577">Термин процедуры</span><span class="sxs-lookup"><span data-stu-id="19a5b-577">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="19a5b-578">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="19a5b-578">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-579">Prompt</span><span class="sxs-lookup"><span data-stu-id="19a5b-579">Prompt</span></span></p></td>
<td><p><span data-ttu-id="19a5b-580">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="19a5b-580">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-581">Имя поставщика</span><span class="sxs-lookup"><span data-stu-id="19a5b-581">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="19a5b-582">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="19a5b-582">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-583">Имя поставщика</span><span class="sxs-lookup"><span data-stu-id="19a5b-583">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="19a5b-584">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="19a5b-584">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-585">Версия поставщика</span><span class="sxs-lookup"><span data-stu-id="19a5b-585">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="19a5b-586">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="19a5b-586">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-587">Read-Only данных</span><span class="sxs-lookup"><span data-stu-id="19a5b-587">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="19a5b-588">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="19a5b-588">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-589">Преобразование наборов строк в команде</span><span class="sxs-lookup"><span data-stu-id="19a5b-589">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="19a5b-590">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="19a5b-590">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-591">Термин схемы</span><span class="sxs-lookup"><span data-stu-id="19a5b-591">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="19a5b-592">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="19a5b-592">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-593">Использование схемы</span><span class="sxs-lookup"><span data-stu-id="19a5b-593">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="19a5b-594">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="19a5b-594">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-595">SQL поддержки</span><span class="sxs-lookup"><span data-stu-id="19a5b-595">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="19a5b-596">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="19a5b-596">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-597">Структурированное хранилище</span><span class="sxs-lookup"><span data-stu-id="19a5b-597">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="19a5b-598">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="19a5b-598">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-599">Поддержка ветвей</span><span class="sxs-lookup"><span data-stu-id="19a5b-599">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="19a5b-600">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="19a5b-600">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-601">Table Term</span><span class="sxs-lookup"><span data-stu-id="19a5b-601">Table Term</span></span></p></td>
<td><p><span data-ttu-id="19a5b-602">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="19a5b-602">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-603">DDL транзакции</span><span class="sxs-lookup"><span data-stu-id="19a5b-603">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="19a5b-604">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="19a5b-604">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-605">Идентификатор пользователя</span><span class="sxs-lookup"><span data-stu-id="19a5b-605">User ID</span></span></p></td>
<td><p><span data-ttu-id="19a5b-606">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="19a5b-606">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-607">имя пользователя;</span><span class="sxs-lookup"><span data-stu-id="19a5b-607">User Name</span></span></p></td>
<td><p><span data-ttu-id="19a5b-608">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="19a5b-608">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-609">Окне Окне</span><span class="sxs-lookup"><span data-stu-id="19a5b-609">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="19a5b-610">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="19a5b-610">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a><span data-ttu-id="19a5b-611">Динамические свойства recordset</span><span class="sxs-lookup"><span data-stu-id="19a5b-611">Recordset Dynamic Properties</span></span>

<span data-ttu-id="19a5b-612">Следующие свойства добавляются в коллекцию **свойств** объекта **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="19a5b-612">The following properties are added to the **Recordset** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="19a5b-613">ADO Property Name</span><span class="sxs-lookup"><span data-stu-id="19a5b-613">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="19a5b-614">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="19a5b-614">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-615">Порядок доступа</span><span class="sxs-lookup"><span data-stu-id="19a5b-615">Access Order</span></span></p></td>
<td><p><span data-ttu-id="19a5b-616">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="19a5b-616">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-617">Блокировка объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="19a5b-617">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="19a5b-618">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="19a5b-618">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-619">Тип закладки</span><span class="sxs-lookup"><span data-stu-id="19a5b-619">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="19a5b-620">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="19a5b-620">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-621">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="19a5b-621">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="19a5b-622">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="19a5b-622">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-623">Изменение вставленных строк</span><span class="sxs-lookup"><span data-stu-id="19a5b-623">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="19a5b-624">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="19a5b-624">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-625">Привилегии столбца</span><span class="sxs-lookup"><span data-stu-id="19a5b-625">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="19a5b-626">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="19a5b-626">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-627">Уведомление о наборе столбцов</span><span class="sxs-lookup"><span data-stu-id="19a5b-627">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="19a5b-628">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="19a5b-628">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-629">Задержка обновлений объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="19a5b-629">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="19a5b-630">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="19a5b-630">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-631">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="19a5b-631">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="19a5b-632">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="19a5b-632">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-633">Строки удержания</span><span class="sxs-lookup"><span data-stu-id="19a5b-633">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="19a5b-634">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="19a5b-634">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-635">IAccessor</span><span class="sxs-lookup"><span data-stu-id="19a5b-635">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="19a5b-636">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="19a5b-636">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-637">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="19a5b-637">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="19a5b-638">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="19a5b-638">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-639">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="19a5b-639">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="19a5b-640">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="19a5b-640">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-641">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="19a5b-641">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="19a5b-642">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="19a5b-642">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-643">IConvertType</span><span class="sxs-lookup"><span data-stu-id="19a5b-643">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="19a5b-644">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="19a5b-644">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-645">Строки Immobile</span><span class="sxs-lookup"><span data-stu-id="19a5b-645">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="19a5b-646">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="19a5b-646">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-647">IRowset</span><span class="sxs-lookup"><span data-stu-id="19a5b-647">IRowset</span></span></p></td>
<td><p><span data-ttu-id="19a5b-648">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="19a5b-648">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-649">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="19a5b-649">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="19a5b-650">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="19a5b-650">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-651">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="19a5b-651">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="19a5b-652">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="19a5b-652">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-653">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="19a5b-653">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="19a5b-654">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="19a5b-654">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-655">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="19a5b-655">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="19a5b-656">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="19a5b-656">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-657">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="19a5b-657">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-658">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="19a5b-658">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="19a5b-659">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="19a5b-659">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-660">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="19a5b-660">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="19a5b-661">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="19a5b-661">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-662">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="19a5b-662">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="19a5b-663">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="19a5b-663">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-664">Литеральные закладки</span><span class="sxs-lookup"><span data-stu-id="19a5b-664">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="19a5b-665">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="19a5b-665">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-666">Идентификатор строки литералов</span><span class="sxs-lookup"><span data-stu-id="19a5b-666">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="19a5b-667">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="19a5b-667">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-668">Максимальное число открытых строк</span><span class="sxs-lookup"><span data-stu-id="19a5b-668">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="19a5b-669">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="19a5b-669">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-670">Максимальное число ожидающих строк</span><span class="sxs-lookup"><span data-stu-id="19a5b-670">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="19a5b-671">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="19a5b-671">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-672">Максимальное число строк</span><span class="sxs-lookup"><span data-stu-id="19a5b-672">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="19a5b-673">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="19a5b-673">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-674">Детализация уведомлений</span><span class="sxs-lookup"><span data-stu-id="19a5b-674">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="19a5b-675">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="19a5b-675">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-676">Этапы уведомлений</span><span class="sxs-lookup"><span data-stu-id="19a5b-676">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="19a5b-677">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="19a5b-677">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-678">Transacted объектов</span><span class="sxs-lookup"><span data-stu-id="19a5b-678">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="19a5b-679">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="19a5b-679">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-680">Собственные изменения, видимые</span><span class="sxs-lookup"><span data-stu-id="19a5b-680">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="19a5b-681">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="19a5b-681">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-682">Собственные вставки видимые</span><span class="sxs-lookup"><span data-stu-id="19a5b-682">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="19a5b-683">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="19a5b-683">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-684">Сохранение при отменить</span><span class="sxs-lookup"><span data-stu-id="19a5b-684">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="19a5b-685">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="19a5b-685">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-686">Сохранение при фиксации</span><span class="sxs-lookup"><span data-stu-id="19a5b-686">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="19a5b-687">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="19a5b-687">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-688">Быстрая перезагрузка</span><span class="sxs-lookup"><span data-stu-id="19a5b-688">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="19a5b-689">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="19a5b-689">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-690">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="19a5b-690">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="19a5b-691">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="19a5b-691">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-692">Удаление удаленных строк</span><span class="sxs-lookup"><span data-stu-id="19a5b-692">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="19a5b-693">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="19a5b-693">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-694">Отчет о нескольких изменениях</span><span class="sxs-lookup"><span data-stu-id="19a5b-694">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="19a5b-695">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="19a5b-695">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-696">Возвращение ожидающих вставки</span><span class="sxs-lookup"><span data-stu-id="19a5b-696">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="19a5b-697">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="19a5b-697">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-698">Уведомление об удалении строки</span><span class="sxs-lookup"><span data-stu-id="19a5b-698">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="19a5b-699">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="19a5b-699">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-700">Уведомление о первом изменении строки</span><span class="sxs-lookup"><span data-stu-id="19a5b-700">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="19a5b-701">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="19a5b-701">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-702">Уведомление о вставке строки</span><span class="sxs-lookup"><span data-stu-id="19a5b-702">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="19a5b-703">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="19a5b-703">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-704">Привилегии строки</span><span class="sxs-lookup"><span data-stu-id="19a5b-704">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="19a5b-705">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="19a5b-705">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-706">Уведомление о повторной синхронизации строк</span><span class="sxs-lookup"><span data-stu-id="19a5b-706">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="19a5b-707">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="19a5b-707">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-708">Модель потоков по строкам</span><span class="sxs-lookup"><span data-stu-id="19a5b-708">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="19a5b-709">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="19a5b-709">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-710">Уведомление об отмене строки</span><span class="sxs-lookup"><span data-stu-id="19a5b-710">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="19a5b-711">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="19a5b-711">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-712">Уведомление об отмене удаления строки</span><span class="sxs-lookup"><span data-stu-id="19a5b-712">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="19a5b-713">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="19a5b-713">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-714">Уведомление об отмене вставки строки</span><span class="sxs-lookup"><span data-stu-id="19a5b-714">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="19a5b-715">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="19a5b-715">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-716">Уведомление об обновлении строки</span><span class="sxs-lookup"><span data-stu-id="19a5b-716">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="19a5b-717">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="19a5b-717">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-718">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="19a5b-718">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="19a5b-719">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="19a5b-719">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-720">Уведомление о выпуске rowset</span><span class="sxs-lookup"><span data-stu-id="19a5b-720">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="19a5b-721">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="19a5b-721">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-722">Прокрутка назад</span><span class="sxs-lookup"><span data-stu-id="19a5b-722">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="19a5b-723">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="19a5b-723">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-724">Пропустить удаленные закладки</span><span class="sxs-lookup"><span data-stu-id="19a5b-724">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="19a5b-725">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="19a5b-725">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-726">Удостоверение строки strong</span><span class="sxs-lookup"><span data-stu-id="19a5b-726">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="19a5b-727">DBPROP_STRONGITDENTITY</span><span class="sxs-lookup"><span data-stu-id="19a5b-727">DBPROP_STRONGITDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-728">Уникальные строки</span><span class="sxs-lookup"><span data-stu-id="19a5b-728">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="19a5b-729">DBPROP_UNIQUEROWS</span><span class="sxs-lookup"><span data-stu-id="19a5b-729">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-730">Updatability</span><span class="sxs-lookup"><span data-stu-id="19a5b-730">Updatability</span></span></p></td>
<td><p><span data-ttu-id="19a5b-731">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="19a5b-731">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-732">Использование закладок</span><span class="sxs-lookup"><span data-stu-id="19a5b-732">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="19a5b-733">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="19a5b-733">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a><span data-ttu-id="19a5b-734">Командные динамические свойства</span><span class="sxs-lookup"><span data-stu-id="19a5b-734">Command Dynamic Properties</span></span>

<span data-ttu-id="19a5b-735">Следующие свойства добавляются в  коллекцию **свойств объекта Command.**</span><span class="sxs-lookup"><span data-stu-id="19a5b-735">The following properties are added to the **Command** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="19a5b-736">ADO Property Name</span><span class="sxs-lookup"><span data-stu-id="19a5b-736">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="19a5b-737">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="19a5b-737">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-738">Порядок доступа</span><span class="sxs-lookup"><span data-stu-id="19a5b-738">Access Order</span></span></p></td>
<td><p><span data-ttu-id="19a5b-739">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="19a5b-739">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-740">Блокировка объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="19a5b-740">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="19a5b-741">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="19a5b-741">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-742">Тип закладки</span><span class="sxs-lookup"><span data-stu-id="19a5b-742">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="19a5b-743">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="19a5b-743">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-744">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="19a5b-744">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="19a5b-745">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="19a5b-745">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-746">Изменение вставленных строк</span><span class="sxs-lookup"><span data-stu-id="19a5b-746">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="19a5b-747">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="19a5b-747">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-748">Привилегии столбца</span><span class="sxs-lookup"><span data-stu-id="19a5b-748">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="19a5b-749">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="19a5b-749">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-750">Уведомление о наборе столбцов</span><span class="sxs-lookup"><span data-stu-id="19a5b-750">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="19a5b-751">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="19a5b-751">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-752">Задержка обновлений объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="19a5b-752">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="19a5b-753">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="19a5b-753">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-754">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="19a5b-754">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="19a5b-755">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="19a5b-755">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-756">Строки удержания</span><span class="sxs-lookup"><span data-stu-id="19a5b-756">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="19a5b-757">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="19a5b-757">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-758">IAccessor</span><span class="sxs-lookup"><span data-stu-id="19a5b-758">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="19a5b-759">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="19a5b-759">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-760">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="19a5b-760">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="19a5b-761">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="19a5b-761">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-762">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="19a5b-762">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="19a5b-763">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="19a5b-763">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-764">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="19a5b-764">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="19a5b-765">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="19a5b-765">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-766">IConvertType</span><span class="sxs-lookup"><span data-stu-id="19a5b-766">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="19a5b-767">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="19a5b-767">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-768">Строки Immobile</span><span class="sxs-lookup"><span data-stu-id="19a5b-768">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="19a5b-769">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="19a5b-769">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-770">IRowset</span><span class="sxs-lookup"><span data-stu-id="19a5b-770">IRowset</span></span></p></td>
<td><p><span data-ttu-id="19a5b-771">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="19a5b-771">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-772">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="19a5b-772">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="19a5b-773">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="19a5b-773">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-774">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="19a5b-774">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="19a5b-775">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="19a5b-775">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-776">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="19a5b-776">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="19a5b-777">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="19a5b-777">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-778">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="19a5b-778">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="19a5b-779">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="19a5b-779">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-780">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="19a5b-780">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-781">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="19a5b-781">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="19a5b-782">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="19a5b-782">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-783">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="19a5b-783">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="19a5b-784">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="19a5b-784">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-785">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="19a5b-785">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="19a5b-786">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="19a5b-786">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-787">Литеральные закладки</span><span class="sxs-lookup"><span data-stu-id="19a5b-787">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="19a5b-788">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="19a5b-788">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-789">Идентификатор строки литералов</span><span class="sxs-lookup"><span data-stu-id="19a5b-789">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="19a5b-790">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="19a5b-790">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-791">Максимальное число открытых строк</span><span class="sxs-lookup"><span data-stu-id="19a5b-791">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="19a5b-792">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="19a5b-792">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-793">Максимальное число ожидающих строк</span><span class="sxs-lookup"><span data-stu-id="19a5b-793">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="19a5b-794">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="19a5b-794">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-795">Максимальное число строк</span><span class="sxs-lookup"><span data-stu-id="19a5b-795">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="19a5b-796">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="19a5b-796">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-797">Детализация уведомлений</span><span class="sxs-lookup"><span data-stu-id="19a5b-797">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="19a5b-798">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="19a5b-798">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-799">Этапы уведомлений</span><span class="sxs-lookup"><span data-stu-id="19a5b-799">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="19a5b-800">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="19a5b-800">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-801">Transacted объектов</span><span class="sxs-lookup"><span data-stu-id="19a5b-801">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="19a5b-802">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="19a5b-802">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-803">Собственные изменения, видимые</span><span class="sxs-lookup"><span data-stu-id="19a5b-803">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="19a5b-804">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="19a5b-804">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-805">Собственные вставки видимые</span><span class="sxs-lookup"><span data-stu-id="19a5b-805">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="19a5b-806">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="19a5b-806">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-807">Сохранение при отменить</span><span class="sxs-lookup"><span data-stu-id="19a5b-807">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="19a5b-808">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="19a5b-808">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-809">Сохранение при фиксации</span><span class="sxs-lookup"><span data-stu-id="19a5b-809">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="19a5b-810">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="19a5b-810">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-811">Быстрая перезагрузка</span><span class="sxs-lookup"><span data-stu-id="19a5b-811">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="19a5b-812">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="19a5b-812">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-813">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="19a5b-813">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="19a5b-814">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="19a5b-814">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-815">Удаление удаленных строк</span><span class="sxs-lookup"><span data-stu-id="19a5b-815">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="19a5b-816">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="19a5b-816">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-817">Отчет о нескольких изменениях</span><span class="sxs-lookup"><span data-stu-id="19a5b-817">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="19a5b-818">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="19a5b-818">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-819">Возвращение ожидающих вставки</span><span class="sxs-lookup"><span data-stu-id="19a5b-819">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="19a5b-820">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="19a5b-820">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-821">Уведомление об удалении строки</span><span class="sxs-lookup"><span data-stu-id="19a5b-821">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="19a5b-822">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="19a5b-822">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-823">Уведомление о первом изменении строки</span><span class="sxs-lookup"><span data-stu-id="19a5b-823">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="19a5b-824">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="19a5b-824">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-825">Уведомление о вставке строки</span><span class="sxs-lookup"><span data-stu-id="19a5b-825">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="19a5b-826">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="19a5b-826">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-827">Привилегии строки</span><span class="sxs-lookup"><span data-stu-id="19a5b-827">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="19a5b-828">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="19a5b-828">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-829">Уведомление о повторной синхронизации строк</span><span class="sxs-lookup"><span data-stu-id="19a5b-829">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="19a5b-830">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="19a5b-830">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-831">Модель потоков по строкам</span><span class="sxs-lookup"><span data-stu-id="19a5b-831">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="19a5b-832">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="19a5b-832">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-833">Уведомление об отмене строки</span><span class="sxs-lookup"><span data-stu-id="19a5b-833">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="19a5b-834">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="19a5b-834">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-835">Уведомление об отмене удаления строки</span><span class="sxs-lookup"><span data-stu-id="19a5b-835">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="19a5b-836">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="19a5b-836">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-837">Уведомление об отмене вставки строки</span><span class="sxs-lookup"><span data-stu-id="19a5b-837">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="19a5b-838">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="19a5b-838">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-839">Уведомление об обновлении строки</span><span class="sxs-lookup"><span data-stu-id="19a5b-839">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="19a5b-840">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="19a5b-840">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-841">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="19a5b-841">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="19a5b-842">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="19a5b-842">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-843">Уведомление о выпуске rowset</span><span class="sxs-lookup"><span data-stu-id="19a5b-843">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="19a5b-844">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="19a5b-844">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-845">Прокрутка назад</span><span class="sxs-lookup"><span data-stu-id="19a5b-845">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="19a5b-846">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="19a5b-846">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-847">Пропустить удаленные закладки</span><span class="sxs-lookup"><span data-stu-id="19a5b-847">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="19a5b-848">DBPROP_BOOKMARKSKIP</span><span class="sxs-lookup"><span data-stu-id="19a5b-848">DBPROP_BOOKMARKSKIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-849">Удостоверение строки strong</span><span class="sxs-lookup"><span data-stu-id="19a5b-849">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="19a5b-850">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="19a5b-850">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19a5b-851">Updatability</span><span class="sxs-lookup"><span data-stu-id="19a5b-851">Updatability</span></span></p></td>
<td><p><span data-ttu-id="19a5b-852">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="19a5b-852">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19a5b-853">Использование закладок</span><span class="sxs-lookup"><span data-stu-id="19a5b-853">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="19a5b-854">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="19a5b-854">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="19a5b-855">См. также</span><span class="sxs-lookup"><span data-stu-id="19a5b-855">See also</span></span>

<span data-ttu-id="19a5b-856">Подробные сведения об определенной реализации и функциональной информации о поставщике Microsoft OLE DB для ODBC можно получить в руководстве программиста [OLE DB](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85)) или в Центре разработчиков платформы [данных.](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017)</span><span class="sxs-lookup"><span data-stu-id="19a5b-856">For details regarding specific implementation and functional information about the Microsoft OLE DB Provider for ODBC, consult the [OLE DB Programmer's Guide](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85)) or visit the [Data Platform Developer Center](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).</span></span>

