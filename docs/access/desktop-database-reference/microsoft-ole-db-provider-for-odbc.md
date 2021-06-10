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
# <a name="microsoft-ole-db-provider-for-odbc"></a><span data-ttu-id="baa55-102">Поставщик Microsoft OLE DB для ODBC</span><span class="sxs-lookup"><span data-stu-id="baa55-102">Microsoft OLE DB Provider for ODBC</span></span>

<span data-ttu-id="baa55-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="baa55-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="baa55-104">Для программиста ADO или RDS идеальным был бы мир, в котором каждый источник данных предоставляет интерфейс OLE DB, чтобы ADO мог вызываться непосредственно в источник данных.</span><span class="sxs-lookup"><span data-stu-id="baa55-104">To an ADO or RDS programmer, an ideal world would be one in which every data source exposes an OLE DB interface, so that ADO could call directly into the data source.</span></span> <span data-ttu-id="baa55-105">Несмотря на то, что все больше поставщиков баз данных внедряют интерфейсы OLE DB, некоторые источники данных еще не открыты таким образом.</span><span class="sxs-lookup"><span data-stu-id="baa55-105">Although increasingly more database vendors are implementing OLE DB interfaces, some data sources are not yet exposed this way.</span></span> <span data-ttu-id="baa55-106">Однако практически все системы DBMS, которые используются сегодня, можно получить доступ через ODBC.</span><span class="sxs-lookup"><span data-stu-id="baa55-106">However, virtually all DBMS systems in use today can be accessed through ODBC.</span></span>

<span data-ttu-id="baa55-107">Драйверы ODBC доступны для всех основных DBMS, которые используются сегодня, включая Microsoft SQL Server, Microsoft Access (двигатель базы данных Microsoft Jet) и Microsoft FoxPro, в дополнение к продуктам баз данных, не входим в microsoft, например Oracle.</span><span class="sxs-lookup"><span data-stu-id="baa55-107">ODBC drivers are available for every major DBMS in use today, including Microsoft SQL Server, Microsoft Access (Microsoft Jet database engine), and Microsoft FoxPro, in addition to non-Microsoft database products such as Oracle.</span></span>

<span data-ttu-id="baa55-108">Поставщик ODBC Майкрософт, однако, позволяет ADO подключаться к любому источнику данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="baa55-108">The Microsoft ODBC Provider, however, allows ADO to connect to any ODBC data source.</span></span> <span data-ttu-id="baa55-109">Поставщик имеет свободные потоки и включен Юникод.</span><span class="sxs-lookup"><span data-stu-id="baa55-109">The provider is free-threaded and Unicode enabled.</span></span>

<span data-ttu-id="baa55-110">Поставщик поддерживает транзакции, хотя различные двигатели DBMS предлагают различные типы поддержки транзакций.</span><span class="sxs-lookup"><span data-stu-id="baa55-110">The provider supports transactions, although different DBMS engines offer different types of transaction support.</span></span> <span data-ttu-id="baa55-111">Например, Microsoft Access поддерживает вложенные транзакции глубиной до пяти уровней.</span><span class="sxs-lookup"><span data-stu-id="baa55-111">For example, Microsoft Access supports nested transactions up to five levels deep.</span></span>

<span data-ttu-id="baa55-112">Это поставщик ADO по умолчанию, и все свойства и методы ADO, зависящие от поставщика, поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="baa55-112">This is the default provider for ADO, and all provider-dependent ADO properties and methods are supported.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="baa55-113">Параметры строки подключения</span><span class="sxs-lookup"><span data-stu-id="baa55-113">Connection String Parameters</span></span>

<span data-ttu-id="baa55-114">Чтобы подключиться к этому поставщику, установите **аргумент Provider=** свойства [ConnectionString:](connectionstring-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="baa55-114">To connect to this provider, set the **Provider=** argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```sql 
 
MSDASQL 
```

<span data-ttu-id="baa55-115">Чтение свойства [Provider](provider-property-ado.md) также вернет эту строку.</span><span class="sxs-lookup"><span data-stu-id="baa55-115">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="baa55-116">Типичная строка подключения</span><span class="sxs-lookup"><span data-stu-id="baa55-116">Typical Connection String</span></span>

<span data-ttu-id="baa55-117">Типичная строка подключения для этого поставщика:</span><span class="sxs-lookup"><span data-stu-id="baa55-117">A typical connection string for this provider is:</span></span>

```sql 
 
"Provider=MSDASQL;DSN=dsnName;UID=userName;PWD=userPassword;" 
```

<span data-ttu-id="baa55-118">Строка состоит из этих ключевых слов:</span><span class="sxs-lookup"><span data-stu-id="baa55-118">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="baa55-119">Ключевое слово</span><span class="sxs-lookup"><span data-stu-id="baa55-119">Keyword</span></span></p></th>
<th><p><span data-ttu-id="baa55-120">Description</span><span class="sxs-lookup"><span data-stu-id="baa55-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="baa55-121"><strong>Поставщик</strong></span><span class="sxs-lookup"><span data-stu-id="baa55-121"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="baa55-122">Указывает поставщика OLE DB для ODBC.</span><span class="sxs-lookup"><span data-stu-id="baa55-122">Specifies the OLE DB Provider for ODBC.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-123"><strong>DSN</strong></span><span class="sxs-lookup"><span data-stu-id="baa55-123"><strong>DSN</strong></span></span></p></td>
<td><p><span data-ttu-id="baa55-124">Указывает имя источника данных.</span><span class="sxs-lookup"><span data-stu-id="baa55-124">Specifies the data source name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-125"><strong>UID</strong></span><span class="sxs-lookup"><span data-stu-id="baa55-125"><strong>UID</strong></span></span></p></td>
<td><p><span data-ttu-id="baa55-126">Задает имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="baa55-126">Specifies the user name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-127"><strong>PWD</strong></span><span class="sxs-lookup"><span data-stu-id="baa55-127"><strong>PWD</strong></span></span></p></td>
<td><p><span data-ttu-id="baa55-128">Указывает пароль пользователя.</span><span class="sxs-lookup"><span data-stu-id="baa55-128">Specifies the user password.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-129"><strong>URL-адрес</strong></span><span class="sxs-lookup"><span data-stu-id="baa55-129"><strong>URL</strong></span></span></p></td>
<td><p><span data-ttu-id="baa55-130">Указывает URL-адрес файла или каталога, опубликованный в веб-папке.</span><span class="sxs-lookup"><span data-stu-id="baa55-130">Specifies the URL of a file or directory published in a web folder.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="baa55-131">Так как это поставщик ADO по умолчанию, если вы не закроет параметр **Provider=** из строки подключения, ADO попытается установить подключение к этому поставщику.</span><span class="sxs-lookup"><span data-stu-id="baa55-131">Because this is the default provider for ADO, if you omit the **Provider=** parameter from the connection string, ADO will attempt to establish a connection to this provider.</span></span>

<span data-ttu-id="baa55-132">Поставщик не поддерживает какие-либо конкретные параметры подключения в дополнение к параметрам, определенным ADO.</span><span class="sxs-lookup"><span data-stu-id="baa55-132">The provider does not support any specific connection parameters in addition to those defined by ADO.</span></span> <span data-ttu-id="baa55-133">Однако поставщик передает диспетчеру драйверов ODBC любые параметры подключения, не относясь к ADO.</span><span class="sxs-lookup"><span data-stu-id="baa55-133">However, the provider will pass any non-ADO connection parameters to the ODBC driver manager.</span></span>

<span data-ttu-id="baa55-134">Так как можно отменить параметр **Provider,** можно составить строку подключения ADO, идентичную строке подключения ODBC для того же источника данных.</span><span class="sxs-lookup"><span data-stu-id="baa55-134">Because you can omit the **Provider** parameter, you can therefore compose an ADO connection string that is identical to an ODBC connection string for the same data source.</span></span> <span data-ttu-id="baa55-135">Используйте те же имена параметров **(DRIVER=**, **DATABASE=**, **DSN=** и так далее), значения и синтаксис, как при сочинении строки подключения ODBC.</span><span class="sxs-lookup"><span data-stu-id="baa55-135">Use the same parameter names (**DRIVER=**, **DATABASE=**, **DSN=**, and so on), values, and syntax as you would when composing an ODBC connection string.</span></span> <span data-ttu-id="baa55-136">Вы можете подключиться к предварительному имени источника данных (DSN) или FileDSN или без него.</span><span class="sxs-lookup"><span data-stu-id="baa55-136">You can connect with or without a predefined data source name (DSN) or FileDSN.</span></span>

<span data-ttu-id="baa55-137">**Синтаксис с DSN или FileDSN:**</span><span class="sxs-lookup"><span data-stu-id="baa55-137">**Syntax with a DSN or FileDSN:**</span></span>

`"[Provider=MSDASQL;] { DSN=name | FileDSN=filename } ; [DATABASE=database;] UID=user; PWD=password"`

<span data-ttu-id="baa55-138">**Синтаксис без подключения к DSN (без DSN):**</span><span class="sxs-lookup"><span data-stu-id="baa55-138">**Syntax without a DSN (DSN-less connection):**</span></span>

`"[Provider=MSDASQL;] DRIVER=driver; SERVER=server;DATABASE=database; UID=user; PWD=password"`

<span data-ttu-id="baa55-139">Если вы используете **DSN** или **FileDSN,** его необходимо определить с помощью администратора источника данных ODBC в панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="baa55-139">If you use a **DSN** or **FileDSN**, it must be defined through the ODBC Data Source Administrator in the Windows Control Panel.</span></span> <span data-ttu-id="baa55-140">В Microsoft Windows 2000 г. Администратор ODBC находится под административными средствами.</span><span class="sxs-lookup"><span data-stu-id="baa55-140">In Microsoft Windows 2000, the ODBC Administrator is located under Administrative Tools.</span></span> <span data-ttu-id="baa55-141">В предыдущих версиях Windows значок администратора ODBC называется **32-битным ODBC** или просто **ODBC**.</span><span class="sxs-lookup"><span data-stu-id="baa55-141">In previous versions of Windows, the ODBC Administrator icon is named **32-bit ODBC** or simply **ODBC**.</span></span>

<span data-ttu-id="baa55-142">В качестве альтернативы настройке **DSN** можно указать драйвер ODBC **(DRIVER=),** например "SQL Server;" имя сервера **(SERVER=);** и имя базы данных **(DATABASE=**).</span><span class="sxs-lookup"><span data-stu-id="baa55-142">As an alternative to setting a **DSN**, you can specify the ODBC driver (**DRIVER=**), such as "SQL Server;" the server name (**SERVER=**); and the database name (**DATABASE=**).</span></span>

<span data-ttu-id="baa55-143">Вы также можете указать имя учетной записи пользователя **(UID=)** и пароль для учетной записи пользователя **(PWD=)**  в параметрах ODBC или в стандартных параметрах пользователя и пароля, определенных ADO. </span><span class="sxs-lookup"><span data-stu-id="baa55-143">You can also specify a user account name (**UID=**), and the password for the user account (**PWD=**) in the ODBC-specific parameters or in the standard ADO-defined *user* and *password* parameters.</span></span>

<span data-ttu-id="baa55-144">Хотя **определение DSN** уже указывает базу данных, можно указать параметр базы данных в дополнение к   **DSN** для подключения к другой базе данных.</span><span class="sxs-lookup"><span data-stu-id="baa55-144">Although a **DSN** definition already specifies a database, you can specify *a* *database* parameter in addition to a **DSN** to connect to a different database.</span></span> <span data-ttu-id="baa55-145">Это хорошая идея, чтобы всегда включать *параметр* *базы данных* при использовании **DSN**.</span><span class="sxs-lookup"><span data-stu-id="baa55-145">It is a good idea to always include *the* *database* parameter when you use a **DSN**.</span></span> <span data-ttu-id="baa55-146">Это обеспечит подключение к соответствующей базе данных в том случае, если другой пользователь изменил параметр базы данных по умолчанию с момента последней проверки **определения DSN.**</span><span class="sxs-lookup"><span data-stu-id="baa55-146">This will ensure that you connect to the proper database in the event that another user changed the default database parameter since you last checked the **DSN** definition.</span></span>

## <a name="provider-specific-connection-properties"></a><span data-ttu-id="baa55-147">Provider-Specific свойств подключения</span><span class="sxs-lookup"><span data-stu-id="baa55-147">Provider-Specific Connection Properties</span></span>

<span data-ttu-id="baa55-148">Поставщик OLE DB для ODBC добавляет несколько свойств в коллекцию [свойств](properties-collection-ado.md) объекта **Connection.**</span><span class="sxs-lookup"><span data-stu-id="baa55-148">The OLE DB provider for ODBC adds several properties to the [Properties](properties-collection-ado.md) collection of the **Connection** object.</span></span> <span data-ttu-id="baa55-149">В следующей таблице перечислены эти свойства с соответствующим именем свойства OLE DB в скобки.</span><span class="sxs-lookup"><span data-stu-id="baa55-149">The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="baa55-150">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="baa55-150">Property Name</span></span></p></th>
<th><p><span data-ttu-id="baa55-151">Description</span><span class="sxs-lookup"><span data-stu-id="baa55-151">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="baa55-152">Доступные процедуры</span><span class="sxs-lookup"><span data-stu-id="baa55-152">Accessible Procedures</span></span><br />
<span data-ttu-id="baa55-153">(KAGPROP_ACCESSIBLEPROCEDURES)</span><span class="sxs-lookup"><span data-stu-id="baa55-153">(KAGPROP_ACCESSIBLEPROCEDURES)</span></span></p></td>
<td><p><span data-ttu-id="baa55-154">Указывает, имеет ли пользователь доступ к сохраненным процедурам.</span><span class="sxs-lookup"><span data-stu-id="baa55-154">Indicates whether the user has access to stored procedures.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-155">Доступные таблицы</span><span class="sxs-lookup"><span data-stu-id="baa55-155">Accessible Tables</span></span><br />
<span data-ttu-id="baa55-156">(KAGPROP_ACCESSIBLETABLES)</span><span class="sxs-lookup"><span data-stu-id="baa55-156">(KAGPROP_ACCESSIBLETABLES)</span></span></p></td>
<td><p><span data-ttu-id="baa55-157">Указывает, имеет ли пользователь разрешение на выполнение заявлений SELECT в таблицах баз данных.</span><span class="sxs-lookup"><span data-stu-id="baa55-157">Indicates whether the user has permission to execute SELECT statements against the database tables.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-158">Active Statements</span><span class="sxs-lookup"><span data-stu-id="baa55-158">Active Statements</span></span><br />
<span data-ttu-id="baa55-159">(KAGPROP_ACTIVESTATEMENTS)</span><span class="sxs-lookup"><span data-stu-id="baa55-159">(KAGPROP_ACTIVESTATEMENTS)</span></span></p></td>
<td><p><span data-ttu-id="baa55-160">Указывает количество обработок, которые драйвер ODBC может поддерживать в подключении.</span><span class="sxs-lookup"><span data-stu-id="baa55-160">Indicates the number of handles an ODBC driver can support on a connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-161">Имя драйвера</span><span class="sxs-lookup"><span data-stu-id="baa55-161">Driver Name</span></span><br />
<span data-ttu-id="baa55-162">(KAGPROP_DRIVERNAME)</span><span class="sxs-lookup"><span data-stu-id="baa55-162">(KAGPROP_DRIVERNAME)</span></span></p></td>
<td><p><span data-ttu-id="baa55-163">Указывает имя файла драйвера ODBC.</span><span class="sxs-lookup"><span data-stu-id="baa55-163">Indicates the file name of the ODBC driver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-164">Версия драйвера ODBC</span><span class="sxs-lookup"><span data-stu-id="baa55-164">Driver ODBC Version</span></span><br />
<span data-ttu-id="baa55-165">(KAGPROP_DRIVERODBCVER)</span><span class="sxs-lookup"><span data-stu-id="baa55-165">(KAGPROP_DRIVERODBCVER)</span></span></p></td>
<td><p><span data-ttu-id="baa55-166">Указывает версию ODBC, поддерживаемую этим драйвером.</span><span class="sxs-lookup"><span data-stu-id="baa55-166">Indicates the version of ODBC that this driver supports.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-167">Использование файлов</span><span class="sxs-lookup"><span data-stu-id="baa55-167">File Usage</span></span><br />
<span data-ttu-id="baa55-168">(KAGPROP_FILEUSAGE)</span><span class="sxs-lookup"><span data-stu-id="baa55-168">(KAGPROP_FILEUSAGE)</span></span></p></td>
<td><p><span data-ttu-id="baa55-169">Указывает, как драйвер обрабатывает файл в источнике данных; как таблица или каталог.</span><span class="sxs-lookup"><span data-stu-id="baa55-169">Indicates how the driver treats a file in a data source; as a table or as a catalog.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-170">Как и предложение о побеге</span><span class="sxs-lookup"><span data-stu-id="baa55-170">Like Escape Clause</span></span><br />
<span data-ttu-id="baa55-171">(KAGPROP_LIKEESCAPECLAUSE)</span><span class="sxs-lookup"><span data-stu-id="baa55-171">(KAGPROP_LIKEESCAPECLAUSE)</span></span></p></td>
<td><p><span data-ttu-id="baa55-172">Указывает, поддерживает ли драйвер определение и использование символа побега для символа процента (%) и подчеркнуть символ (_) в предикате LIKE клаузула WHERE.</span><span class="sxs-lookup"><span data-stu-id="baa55-172">Indicates whether the driver supports the definition and use of an escape character for the percent character (%) and underline character (_) in the LIKE predicate of a WHERE clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-173">Max Columns in Group By</span><span class="sxs-lookup"><span data-stu-id="baa55-173">Max Columns in Group By</span></span><br />
<span data-ttu-id="baa55-174">(KAGPROP_MAXCOLUMNSINGROUPBY)</span><span class="sxs-lookup"><span data-stu-id="baa55-174">(KAGPROP_MAXCOLUMNSINGROUPBY)</span></span></p></td>
<td><p><span data-ttu-id="baa55-175">Указывает максимальное количество столбцов, которые могут быть указаны в пункте GROUP BY в заявлении SELECT.</span><span class="sxs-lookup"><span data-stu-id="baa55-175">Indicates the maximum number of columns that can be listed in the GROUP BY clause of a SELECT statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-176">Столбцы Max в индексе</span><span class="sxs-lookup"><span data-stu-id="baa55-176">Max Columns in Index</span></span><br />
<span data-ttu-id="baa55-177">(KAGPROP_MAXCOLUMNSININDEX)</span><span class="sxs-lookup"><span data-stu-id="baa55-177">(KAGPROP_MAXCOLUMNSININDEX)</span></span></p></td>
<td><p><span data-ttu-id="baa55-178">Указывает максимальное количество столбцов, которые можно включить в индекс.</span><span class="sxs-lookup"><span data-stu-id="baa55-178">Indicates the maximum number of columns that can be included in an index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-179">Max Columns in Order By</span><span class="sxs-lookup"><span data-stu-id="baa55-179">Max Columns in Order By</span></span><br />
<span data-ttu-id="baa55-180">(KAGPROP_MAXCOLUMNSINORDERBY)</span><span class="sxs-lookup"><span data-stu-id="baa55-180">(KAGPROP_MAXCOLUMNSINORDERBY)</span></span></p></td>
<td><p><span data-ttu-id="baa55-181">Указывает максимальное количество столбцов, которые могут быть указаны в пункте ORDER BY в заявлении SELECT.</span><span class="sxs-lookup"><span data-stu-id="baa55-181">Indicates the maximum number of columns that can be listed in the ORDER BY clause of a SELECT statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-182">Столбцы Max в Выберите</span><span class="sxs-lookup"><span data-stu-id="baa55-182">Max Columns in Select</span></span><br />
<span data-ttu-id="baa55-183">(KAGPROP_MAXCOLUMNSINSELECT)</span><span class="sxs-lookup"><span data-stu-id="baa55-183">(KAGPROP_MAXCOLUMNSINSELECT)</span></span></p></td>
<td><p><span data-ttu-id="baa55-184">Указывает максимальное количество столбцов, которые могут быть указаны в части SELECT в заявлении SELECT.</span><span class="sxs-lookup"><span data-stu-id="baa55-184">Indicates the maximum number of columns that can be listed in the SELECT portion of a SELECT statement.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-185">Столбцы Max в таблице</span><span class="sxs-lookup"><span data-stu-id="baa55-185">Max Columns in Table</span></span><br />
<span data-ttu-id="baa55-186">(KAGPROP_MAXCOLUMNSINTABLE)</span><span class="sxs-lookup"><span data-stu-id="baa55-186">(KAGPROP_MAXCOLUMNSINTABLE)</span></span></p></td>
<td><p><span data-ttu-id="baa55-187">Указывает максимальное количество столбцов, разрешенных в таблице.</span><span class="sxs-lookup"><span data-stu-id="baa55-187">Indicates the maximum number of columns allowed in a table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-188">Числимые функции</span><span class="sxs-lookup"><span data-stu-id="baa55-188">Numeric Functions</span></span><br />
<span data-ttu-id="baa55-189">(KAGPROP_NUMERICFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="baa55-189">(KAGPROP_NUMERICFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="baa55-190">Указывает, какие численные функции поддерживаются драйвером ODBC.</span><span class="sxs-lookup"><span data-stu-id="baa55-190">Indicates which numeric functions are supported by the ODBC driver.</span></span> <span data-ttu-id="baa55-191">Список имен функций и связанных значений, используемых в этой битмаске, см. в документации ODBC Appendix E: Scalar Functions.</span><span class="sxs-lookup"><span data-stu-id="baa55-191">For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-192">Внешние возможности окружных окружных окруж</span><span class="sxs-lookup"><span data-stu-id="baa55-192">Outer Join Capabilities</span></span><br />
<span data-ttu-id="baa55-193">(KAGPROP_OJCAPABILITY)</span><span class="sxs-lookup"><span data-stu-id="baa55-193">(KAGPROP_OJCAPABILITY)</span></span></p></td>
<td><p><span data-ttu-id="baa55-194">Указывает типы ВНЕШНИХ ИОИ, поддерживаемые поставщиком.</span><span class="sxs-lookup"><span data-stu-id="baa55-194">Indicates the types of OUTER JOINs supported by the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-195">Внешние присоединяется</span><span class="sxs-lookup"><span data-stu-id="baa55-195">Outer Joins</span></span><br />
<span data-ttu-id="baa55-196">(KAGPROP_OUTERJOINS)</span><span class="sxs-lookup"><span data-stu-id="baa55-196">(KAGPROP_OUTERJOINS)</span></span></p></td>
<td><p><span data-ttu-id="baa55-197">Указывает, поддерживает ли поставщик ВНЕШНИЕ JOINs.</span><span class="sxs-lookup"><span data-stu-id="baa55-197">Indicates whether the provider supports OUTER JOINs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-198">Специальные символы</span><span class="sxs-lookup"><span data-stu-id="baa55-198">Special Characters</span></span><br />
<span data-ttu-id="baa55-199">(KAGPROP_SPECIALCHARACTERS)</span><span class="sxs-lookup"><span data-stu-id="baa55-199">(KAGPROP_SPECIALCHARACTERS)</span></span></p></td>
<td><p><span data-ttu-id="baa55-200">Указывает, какие символы имеют особое значение для драйвера ODBC.</span><span class="sxs-lookup"><span data-stu-id="baa55-200">Indicates which characters have special meaning for the ODBC driver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-201">Сохраненные процедуры</span><span class="sxs-lookup"><span data-stu-id="baa55-201">Stored Procedures</span></span><br />
<span data-ttu-id="baa55-202">(KAGPROP_PROCEDURES)</span><span class="sxs-lookup"><span data-stu-id="baa55-202">(KAGPROP_PROCEDURES)</span></span></p></td>
<td><p><span data-ttu-id="baa55-203">Указывает, доступны ли сохраненные процедуры для использования с этим драйвером ODBC.</span><span class="sxs-lookup"><span data-stu-id="baa55-203">Indicates whether stored procedures are available for use with this ODBC driver.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-204">Функции строки</span><span class="sxs-lookup"><span data-stu-id="baa55-204">String Functions</span></span><br />
<span data-ttu-id="baa55-205">(KAGPROP_STRINGFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="baa55-205">(KAGPROP_STRINGFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="baa55-206">Указывает, какие функции строк поддерживаются драйвером ODBC.</span><span class="sxs-lookup"><span data-stu-id="baa55-206">Indicates which string functions are supported by the ODBC driver.</span></span> <span data-ttu-id="baa55-207">Список имен функций и связанных значений, используемых в этой битмаске, см. в документации ODBC Appendix E: Scalar Functions.</span><span class="sxs-lookup"><span data-stu-id="baa55-207">For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-208">Функции системы</span><span class="sxs-lookup"><span data-stu-id="baa55-208">System Functions</span></span><br />
<span data-ttu-id="baa55-209">(KAGPROP_SYSTEMFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="baa55-209">(KAGPROP_SYSTEMFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="baa55-210">Указывает, какие функции системы поддерживаются драйвером ODBC.</span><span class="sxs-lookup"><span data-stu-id="baa55-210">Indicates which system functions are supported by the ODBC driver.</span></span> <span data-ttu-id="baa55-211">Список имен функций и связанных значений, используемых в этой битмаске, см. в документации ODBC Appendix E: Scalar Functions.</span><span class="sxs-lookup"><span data-stu-id="baa55-211">For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-212">Функции времени и даты</span><span class="sxs-lookup"><span data-stu-id="baa55-212">Time/Date Functions</span></span><br />
<span data-ttu-id="baa55-213">(KAGPROP_TIMEDATEFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="baa55-213">(KAGPROP_TIMEDATEFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="baa55-214">Указывает, какие функции времени и даты поддерживаются драйвером ODBC.</span><span class="sxs-lookup"><span data-stu-id="baa55-214">Indicates which time and date functions are supported by the ODBC driver.</span></span> <span data-ttu-id="baa55-215">Список имен функций и связанных значений, используемых в этой битмаске, см. в документации ODBC Appendix E: Scalar Functions.</span><span class="sxs-lookup"><span data-stu-id="baa55-215">For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-216">SQL Поддержка грамматики</span><span class="sxs-lookup"><span data-stu-id="baa55-216">SQL Grammar Support</span></span><br />
<span data-ttu-id="baa55-217">(KAGPROP_ODBCSQLCONFORMANCE)</span><span class="sxs-lookup"><span data-stu-id="baa55-217">(KAGPROP_ODBCSQLCONFORMANCE)</span></span></p></td>
<td><p><span data-ttu-id="baa55-218">Указывает грамматику SQL, поддерживаемую драйвером ODBC.</span><span class="sxs-lookup"><span data-stu-id="baa55-218">Indicates the SQL grammar that the ODBC driver supports.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-recordset-and-command-properties"></a><span data-ttu-id="baa55-219">Provider-Specific Recordset и Command Properties</span><span class="sxs-lookup"><span data-stu-id="baa55-219">Provider-Specific Recordset and Command Properties</span></span>

<span data-ttu-id="baa55-220">Поставщик OLE DB для ODBC добавляет несколько свойств в коллекцию **свойств** объектов **Recordset** и **Command.**</span><span class="sxs-lookup"><span data-stu-id="baa55-220">The OLE DB provider for ODBC adds several properties to the **Properties** collection of the **Recordset** and **Command** objects.</span></span> <span data-ttu-id="baa55-221">В следующей таблице перечислены эти свойства с соответствующим именем свойства OLE DB в скобки.</span><span class="sxs-lookup"><span data-stu-id="baa55-221">The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="baa55-222">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="baa55-222">Property Name</span></span></p></th>
<th><p><span data-ttu-id="baa55-223">Description</span><span class="sxs-lookup"><span data-stu-id="baa55-223">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="baa55-224">Обновления на основе запроса/удаления/вставки</span><span class="sxs-lookup"><span data-stu-id="baa55-224">Query Based Updates/Deletes/Inserts</span></span><br />
<span data-ttu-id="baa55-225">(KAGPROP_QUERYBASEDUPDATES)</span><span class="sxs-lookup"><span data-stu-id="baa55-225">(KAGPROP_QUERYBASEDUPDATES)</span></span></p></td>
<td><p><span data-ttu-id="baa55-226">Указывает, можно ли выполнять обновления, удаления и вставки с помощью SQL запросов.</span><span class="sxs-lookup"><span data-stu-id="baa55-226">Indicates whether updates, deletions, and insertions can be performed using SQL queries.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-227">Тип конвалюты ODBC</span><span class="sxs-lookup"><span data-stu-id="baa55-227">ODBC Concurrency Type</span></span><br />
<span data-ttu-id="baa55-228">(KAGPROP_CONCURRENCY)</span><span class="sxs-lookup"><span data-stu-id="baa55-228">(KAGPROP_CONCURRENCY)</span></span></p></td>
<td><p><span data-ttu-id="baa55-229">Указывает метод, используемый для уменьшения потенциальных проблем, вызванных двумя пользователями, пытающихся одновременно получить доступ к данным из источника данных.</span><span class="sxs-lookup"><span data-stu-id="baa55-229">Indicates the method used to reduce potential problems caused by two users attempting to access the same data from the data source simultaneously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-230">Доступность BLOB на Forward-Only курсоре</span><span class="sxs-lookup"><span data-stu-id="baa55-230">BLOB accessibility on Forward-Only cursor</span></span><br />
<span data-ttu-id="baa55-231">(KAGPROP_BLOBSONFOCURSOR)</span><span class="sxs-lookup"><span data-stu-id="baa55-231">(KAGPROP_BLOBSONFOCURSOR)</span></span></p></td>
<td><p><span data-ttu-id="baa55-232">Указывает, можно ли получить доступ к полям <strong>BLOB</strong> при использовании курсора только для вперед.</span><span class="sxs-lookup"><span data-stu-id="baa55-232">Indicates whether BLOB <strong>Fields</strong> can be accessed when using a forward-only cursor.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-233">Включай SQL_FLOAT, SQL_DOUBLE и SQL_REAL в QBU WHERE clauses</span><span class="sxs-lookup"><span data-stu-id="baa55-233">Include SQL_FLOAT, SQL_DOUBLE, and SQL_REAL in QBU WHERE clauses</span></span><br />
<span data-ttu-id="baa55-234">(KAGPROP_INCLUDENONEXACT)</span><span class="sxs-lookup"><span data-stu-id="baa55-234">(KAGPROP_INCLUDENONEXACT)</span></span></p></td>
<td><p><span data-ttu-id="baa55-235">Указывает, можно ли SQL_FLOAT, SQL_DOUBLE и SQL_REAL в положение QBU WHERE.</span><span class="sxs-lookup"><span data-stu-id="baa55-235">Indicates whether SQL_FLOAT, SQL_DOUBLE, and SQL_REAL values can be included in a QBU WHERE clause.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-236">Положение в последней строке после вставки</span><span class="sxs-lookup"><span data-stu-id="baa55-236">Position on the last row after insert</span></span><br />
<span data-ttu-id="baa55-237">(KAGPROP_POSITIONONNEWROW)</span><span class="sxs-lookup"><span data-stu-id="baa55-237">(KAGPROP_POSITIONONNEWROW)</span></span></p></td>
<td><p><span data-ttu-id="baa55-238">Указывает, что после вставки новой записи в таблицу последняя строка в таблице будет приходить в текущем ряду.</span><span class="sxs-lookup"><span data-stu-id="baa55-238">Indicates that after a new record has been inserted in a table, the last row in the table will be come the current row.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-239">IRowsetChangeExtInfo</span><span class="sxs-lookup"><span data-stu-id="baa55-239">IRowsetChangeExtInfo</span></span><br />
<span data-ttu-id="baa55-240">(KAGPROP_IROWSETCHANGEEXTINFO)</span><span class="sxs-lookup"><span data-stu-id="baa55-240">(KAGPROP_IROWSETCHANGEEXTINFO)</span></span></p></td>
<td><p><span data-ttu-id="baa55-241">Указывает, предоставляет ли <strong>интерфейс IRowsetChange</strong> расширенную информационную поддержку.</span><span class="sxs-lookup"><span data-stu-id="baa55-241">Indicates whether the <strong>IRowsetChange</strong> interface provides extended information support.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-242">Тип курсора ODBC</span><span class="sxs-lookup"><span data-stu-id="baa55-242">ODBC Cursor Type</span></span><br />
<span data-ttu-id="baa55-243">(KAGPROP_CURSOR)</span><span class="sxs-lookup"><span data-stu-id="baa55-243">(KAGPROP_CURSOR)</span></span></p></td>
<td><p><span data-ttu-id="baa55-244">Указывает тип курсора, используемого в <strong>Recordset.</strong></span><span class="sxs-lookup"><span data-stu-id="baa55-244">Indicates the type of cursor used by the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-245">Создание rowset, который можно маршалить</span><span class="sxs-lookup"><span data-stu-id="baa55-245">Generate a Rowset that can be marshaled</span></span><br />
<span data-ttu-id="baa55-246">(KAGPROP_MARSHALLABLE)</span><span class="sxs-lookup"><span data-stu-id="baa55-246">(KAGPROP_MARSHALLABLE)</span></span></p></td>
<td><p><span data-ttu-id="baa55-247">Указывает, что драйвер ODBC создает набор записей, который можно</span><span class="sxs-lookup"><span data-stu-id="baa55-247">Indicates that the ODBC driver generates a recordset that can be marshaled</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-text"></a><span data-ttu-id="baa55-248">Командный текст</span><span class="sxs-lookup"><span data-stu-id="baa55-248">Command Text</span></span>

<span data-ttu-id="baa55-249">Использование объекта [Command](command-object-ado.md) во многом зависит от источника данных и типа запроса или командного утверждения, которые он примет.</span><span class="sxs-lookup"><span data-stu-id="baa55-249">How you use the [Command](command-object-ado.md) object largely depends on the data source, and what type of query or command statement it will accept.</span></span>

<span data-ttu-id="baa55-250">ODBC предоставляет определенный синтаксис для вызова сохраненных процедур.</span><span class="sxs-lookup"><span data-stu-id="baa55-250">ODBC provides a specific syntax for calling stored procedures.</span></span> <span data-ttu-id="baa55-251">Для свойства  [CommandText](commandtext-property-ado.md)  объекта *CommandText аргумент CommandText* к [](connection-object-ado.md) методу Execute на объекте  Подключение или аргумент Source к методу Open на [объекте Recordset](recordset-object-ado.md) передается в строке с этим синтаксисом: </span><span class="sxs-lookup"><span data-stu-id="baa55-251">For the [CommandText](commandtext-property-ado.md) property of a **Command** object, the *CommandText* argument to the **Execute** method on a [Connection](connection-object-ado.md) object, or the *Source* argument to the **Open** method on a [Recordset](recordset-object-ado.md) object, passes in a string with this syntax:</span></span>

`"{ [ ? = ] call procedure [ ( ? [, ? [ ,  ]] ) ] }"`

<span data-ttu-id="baa55-252">**Каждый?**</span><span class="sxs-lookup"><span data-stu-id="baa55-252">Each **?**</span></span> <span data-ttu-id="baa55-253">ссылается на объект в коллекции [Параметры.](parameters-collection-ado.md)</span><span class="sxs-lookup"><span data-stu-id="baa55-253">references an object in the [Parameters](parameters-collection-ado.md) collection.</span></span> <span data-ttu-id="baa55-254">Первый? </span><span class="sxs-lookup"><span data-stu-id="baa55-254">The first **?**</span></span> <span data-ttu-id="baa55-255">ссылки **Параметры**(0), далее **?**</span><span class="sxs-lookup"><span data-stu-id="baa55-255">references **Parameters**(0), the next **?**</span></span> <span data-ttu-id="baa55-256">ссылки **Параметры**(1) и так далее.</span><span class="sxs-lookup"><span data-stu-id="baa55-256">references **Parameters**(1), and so on.</span></span>

<span data-ttu-id="baa55-257">Ссылки на параметры необязательны и зависят от структуры сохраненной процедуры.</span><span class="sxs-lookup"><span data-stu-id="baa55-257">The parameter references are optional and depend on the structure of the stored procedure.</span></span> <span data-ttu-id="baa55-258">Если вы хотите вызвать сохраненную процедуру, которая не определяет параметры, строка будет выглядеть так:</span><span class="sxs-lookup"><span data-stu-id="baa55-258">If you want to call a stored procedure that defines no parameters, your string would look like this:</span></span>

`"{ call procedure }"`

<span data-ttu-id="baa55-259">Если у вас есть два параметра запроса, строка будет выглядеть так:</span><span class="sxs-lookup"><span data-stu-id="baa55-259">If you have two query parameters, your string would look like this:</span></span>

`"{ call procedure ( ?, ? ) }"`

<span data-ttu-id="baa55-260">Если сохраненная процедура возвращает значение, возвращаемая величина рассматривается как другой параметр.</span><span class="sxs-lookup"><span data-stu-id="baa55-260">If the stored procedure will return a value, the return value is treated as another parameter.</span></span> <span data-ttu-id="baa55-261">Если у вас нет параметров запроса, но у вас есть возвращаемая величина, строка будет выглядеть так:</span><span class="sxs-lookup"><span data-stu-id="baa55-261">If you have no query parameters but you do have a return value, your string would look like this:</span></span>

`"{ ? = call procedure }"`

<span data-ttu-id="baa55-262">Наконец, если у вас есть значение возврата и два параметра запроса, строка будет выглядеть так:</span><span class="sxs-lookup"><span data-stu-id="baa55-262">Finally, if you have a return value and two query parameters, your string would look like this:</span></span>

`"{ ? = call procedure ( ?, ? ) }"`

## <a name="recordset-behavior"></a><span data-ttu-id="baa55-263">Поведение наборов записей</span><span class="sxs-lookup"><span data-stu-id="baa55-263">Recordset Behavior</span></span>

<span data-ttu-id="baa55-264">В следующих таблицах перечислить стандартные методы и свойства ADO, доступные на **объекте Recordset,** открытом с помощью этого поставщика.</span><span class="sxs-lookup"><span data-stu-id="baa55-264">The following tables list the standard ADO methods and properties available on a **Recordset** object opened with this provider.</span></span>

<span data-ttu-id="baa55-265">Дополнительные сведения о поведении **Recordset** для конфигурации поставщика запустите метод [Supports](supports-method-ado.md) и введите коллекцию **Свойств** в **наборе Recordset,** чтобы определить, присутствуют ли динамические свойства конкретного поставщика.</span><span class="sxs-lookup"><span data-stu-id="baa55-265">For more detailed information about **Recordset** behavior for your provider configuration, run the [Supports](supports-method-ado.md) method and enumerate the **Properties** collection of the **Recordset** to determine whether provider-specific dynamic properties are present.</span></span>

<span data-ttu-id="baa55-266">Доступность стандартных свойств ADO **Recordset:**</span><span class="sxs-lookup"><span data-stu-id="baa55-266">Availability of standard ADO **Recordset** properties:</span></span>

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
<th><p><span data-ttu-id="baa55-267">Свойство</span><span class="sxs-lookup"><span data-stu-id="baa55-267">Property</span></span></p></th>
<th><p><span data-ttu-id="baa55-268">ForwardOnly</span><span class="sxs-lookup"><span data-stu-id="baa55-268">ForwardOnly</span></span></p></th>
<th><p><span data-ttu-id="baa55-269">Динамический</span><span class="sxs-lookup"><span data-stu-id="baa55-269">Dynamic</span></span></p></th>
<th><p><span data-ttu-id="baa55-270">Keyset</span><span class="sxs-lookup"><span data-stu-id="baa55-270">Keyset</span></span></p></th>
<th><p><span data-ttu-id="baa55-271">Статическое</span><span class="sxs-lookup"><span data-stu-id="baa55-271">Static</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="baa55-272"><a href="absolutepage-property-ado.md">AbsolutePage</a></span><span class="sxs-lookup"><span data-stu-id="baa55-272"><a href="absolutepage-property-ado.md">AbsolutePage</a></span></span></p></td>
<td><p><span data-ttu-id="baa55-273">недоступно</span><span class="sxs-lookup"><span data-stu-id="baa55-273">not available</span></span></p></td>
<td><p><span data-ttu-id="baa55-274">недоступно</span><span class="sxs-lookup"><span data-stu-id="baa55-274">not available</span></span></p></td>
<td><p><span data-ttu-id="baa55-275">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="baa55-275">read/write</span></span></p></td>
<td><p><span data-ttu-id="baa55-276">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="baa55-276">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-277"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span><span class="sxs-lookup"><span data-stu-id="baa55-277"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span></span></p></td>
<td><p><span data-ttu-id="baa55-278">недоступно</span><span class="sxs-lookup"><span data-stu-id="baa55-278">not available</span></span></p></td>
<td><p><span data-ttu-id="baa55-279">недоступно</span><span class="sxs-lookup"><span data-stu-id="baa55-279">not available</span></span></p></td>
<td><p><span data-ttu-id="baa55-280">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="baa55-280">read/write</span></span></p></td>
<td><p><span data-ttu-id="baa55-281">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="baa55-281">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-282"><a href="activeconnection-property-ado.md">ActiveConnection</a></span><span class="sxs-lookup"><span data-stu-id="baa55-282"><a href="activeconnection-property-ado.md">ActiveConnection</a></span></span></p></td>
<td><p><span data-ttu-id="baa55-283">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="baa55-283">read/write</span></span></p></td>
<td><p><span data-ttu-id="baa55-284">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="baa55-284">read/write</span></span></p></td>
<td><p><span data-ttu-id="baa55-285">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="baa55-285">read/write</span></span></p></td>
<td><p><span data-ttu-id="baa55-286">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="baa55-286">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-287"><a href="bof-eof-properties-ado.md">BOF</a></span><span class="sxs-lookup"><span data-stu-id="baa55-287"><a href="bof-eof-properties-ado.md">BOF</a></span></span></p></td>
<td><p><span data-ttu-id="baa55-288">read-only</span><span class="sxs-lookup"><span data-stu-id="baa55-288">read-only</span></span></p></td>
<td><p><span data-ttu-id="baa55-289">read-only</span><span class="sxs-lookup"><span data-stu-id="baa55-289">read-only</span></span></p></td>
<td><p><span data-ttu-id="baa55-290">read-only</span><span class="sxs-lookup"><span data-stu-id="baa55-290">read-only</span></span></p></td>
<td><p><span data-ttu-id="baa55-291">read-only</span><span class="sxs-lookup"><span data-stu-id="baa55-291">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-292"><a href="bookmark-property-ado.md">Bookmark</a></span><span class="sxs-lookup"><span data-stu-id="baa55-292"><a href="bookmark-property-ado.md">Bookmark</a></span></span></p></td>
<td><p><span data-ttu-id="baa55-293">недоступно</span><span class="sxs-lookup"><span data-stu-id="baa55-293">not available</span></span></p></td>
<td><p><span data-ttu-id="baa55-294">недоступно</span><span class="sxs-lookup"><span data-stu-id="baa55-294">not available</span></span></p></td>
<td><p><span data-ttu-id="baa55-295">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="baa55-295">read/write</span></span></p></td>
<td><p><span data-ttu-id="baa55-296">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="baa55-296">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-297"><a href="cachesize-property-ado.md">CacheSize</a></span><span class="sxs-lookup"><span data-stu-id="baa55-297"><a href="cachesize-property-ado.md">CacheSize</a></span></span></p></td>
<td><p><span data-ttu-id="baa55-298">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="baa55-298">read/write</span></span></p></td>
<td><p><span data-ttu-id="baa55-299">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="baa55-299">read/write</span></span></p></td>
<td><p><span data-ttu-id="baa55-300">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="baa55-300">read/write</span></span></p></td>
<td><p><span data-ttu-id="baa55-301">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="baa55-301">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-302"><a href="cursorlocation-property-ado.md">CursorLocation</a></span><span class="sxs-lookup"><span data-stu-id="baa55-302"><a href="cursorlocation-property-ado.md">CursorLocation</a></span></span></p></td>
<td><p><span data-ttu-id="baa55-303">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="baa55-303">read/write</span></span></p></td>
<td><p><span data-ttu-id="baa55-304">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="baa55-304">read/write</span></span></p></td>
<td><p><span data-ttu-id="baa55-305">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="baa55-305">read/write</span></span></p></td>
<td><p><span data-ttu-id="baa55-306">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="baa55-306">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-307"><a href="cursortype-property-ado.md">CursorType</a></span><span class="sxs-lookup"><span data-stu-id="baa55-307"><a href="cursortype-property-ado.md">CursorType</a></span></span></p></td>
<td><p><span data-ttu-id="baa55-308">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="baa55-308">read/write</span></span></p></td>
<td><p><span data-ttu-id="baa55-309">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="baa55-309">read/write</span></span></p></td>
<td><p><span data-ttu-id="baa55-310">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="baa55-310">read/write</span></span></p></td>
<td><p><span data-ttu-id="baa55-311">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="baa55-311">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-312"><a href="editmode-property-ado.md">EditMode</a></span><span class="sxs-lookup"><span data-stu-id="baa55-312"><a href="editmode-property-ado.md">EditMode</a></span></span></p></td>
<td><p><span data-ttu-id="baa55-313">read-only</span><span class="sxs-lookup"><span data-stu-id="baa55-313">read-only</span></span></p></td>
<td><p><span data-ttu-id="baa55-314">read-only</span><span class="sxs-lookup"><span data-stu-id="baa55-314">read-only</span></span></p></td>
<td><p><span data-ttu-id="baa55-315">read-only</span><span class="sxs-lookup"><span data-stu-id="baa55-315">read-only</span></span></p></td>
<td><p><span data-ttu-id="baa55-316">read-only</span><span class="sxs-lookup"><span data-stu-id="baa55-316">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-317"><a href="filter-property-ado.md">Filter</a></span><span class="sxs-lookup"><span data-stu-id="baa55-317"><a href="filter-property-ado.md">Filter</a></span></span></p></td>
<td><p><span data-ttu-id="baa55-318">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="baa55-318">read/write</span></span></p></td>
<td><p><span data-ttu-id="baa55-319">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="baa55-319">read/write</span></span></p></td>
<td><p><span data-ttu-id="baa55-320">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="baa55-320">read/write</span></span></p></td>
<td><p><span data-ttu-id="baa55-321">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="baa55-321">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-322"><a href="locktype-property-ado.md">LockType</a></span><span class="sxs-lookup"><span data-stu-id="baa55-322"><a href="locktype-property-ado.md">LockType</a></span></span></p></td>
<td><p><span data-ttu-id="baa55-323">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="baa55-323">read/write</span></span></p></td>
<td><p><span data-ttu-id="baa55-324">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="baa55-324">read/write</span></span></p></td>
<td><p><span data-ttu-id="baa55-325">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="baa55-325">read/write</span></span></p></td>
<td><p><span data-ttu-id="baa55-326">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="baa55-326">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-327"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span><span class="sxs-lookup"><span data-stu-id="baa55-327"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span></span></p></td>
<td><p><span data-ttu-id="baa55-328">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="baa55-328">read/write</span></span></p></td>
<td><p><span data-ttu-id="baa55-329">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="baa55-329">read/write</span></span></p></td>
<td><p><span data-ttu-id="baa55-330">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="baa55-330">read/write</span></span></p></td>
<td><p><span data-ttu-id="baa55-331">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="baa55-331">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-332"><a href="maxrecords-property-ado.md">MaxRecords</a></span><span class="sxs-lookup"><span data-stu-id="baa55-332"><a href="maxrecords-property-ado.md">MaxRecords</a></span></span></p></td>
<td><p><span data-ttu-id="baa55-333">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="baa55-333">read/write</span></span></p></td>
<td><p><span data-ttu-id="baa55-334">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="baa55-334">read/write</span></span></p></td>
<td><p><span data-ttu-id="baa55-335">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="baa55-335">read/write</span></span></p></td>
<td><p><span data-ttu-id="baa55-336">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="baa55-336">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-337"><a href="pagecount-property-ado.md">PageCount</a></span><span class="sxs-lookup"><span data-stu-id="baa55-337"><a href="pagecount-property-ado.md">PageCount</a></span></span></p></td>
<td><p><span data-ttu-id="baa55-338">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="baa55-338">read/write</span></span></p></td>
<td><p><span data-ttu-id="baa55-339">недоступен</span><span class="sxs-lookup"><span data-stu-id="baa55-339">not available</span></span></p></td>
<td><p><span data-ttu-id="baa55-340">read-only</span><span class="sxs-lookup"><span data-stu-id="baa55-340">read-only</span></span></p></td>
<td><p><span data-ttu-id="baa55-341">read-only</span><span class="sxs-lookup"><span data-stu-id="baa55-341">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-342"><a href="pagesize-property-ado.md">PageSize</a></span><span class="sxs-lookup"><span data-stu-id="baa55-342"><a href="pagesize-property-ado.md">PageSize</a></span></span></p></td>
<td><p><span data-ttu-id="baa55-343">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="baa55-343">read/write</span></span></p></td>
<td><p><span data-ttu-id="baa55-344">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="baa55-344">read/write</span></span></p></td>
<td><p><span data-ttu-id="baa55-345">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="baa55-345">read/write</span></span></p></td>
<td><p><span data-ttu-id="baa55-346">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="baa55-346">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-347"><a href="recordcount-property-ado.md">RecordCount</a></span><span class="sxs-lookup"><span data-stu-id="baa55-347"><a href="recordcount-property-ado.md">RecordCount</a></span></span></p></td>
<td><p><span data-ttu-id="baa55-348">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="baa55-348">read/write</span></span></p></td>
<td><p><span data-ttu-id="baa55-349">недоступен</span><span class="sxs-lookup"><span data-stu-id="baa55-349">not available</span></span></p></td>
<td><p><span data-ttu-id="baa55-350">read-only</span><span class="sxs-lookup"><span data-stu-id="baa55-350">read-only</span></span></p></td>
<td><p><span data-ttu-id="baa55-351">read-only</span><span class="sxs-lookup"><span data-stu-id="baa55-351">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-352"><a href="source-property-ado-recordset.md">Source</a></span><span class="sxs-lookup"><span data-stu-id="baa55-352"><a href="source-property-ado-recordset.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="baa55-353">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="baa55-353">read/write</span></span></p></td>
<td><p><span data-ttu-id="baa55-354">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="baa55-354">read/write</span></span></p></td>
<td><p><span data-ttu-id="baa55-355">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="baa55-355">read/write</span></span></p></td>
<td><p><span data-ttu-id="baa55-356">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="baa55-356">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-357"><a href="state-property-ado.md">Состояние</a></span><span class="sxs-lookup"><span data-stu-id="baa55-357"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="baa55-358">read-only</span><span class="sxs-lookup"><span data-stu-id="baa55-358">read-only</span></span></p></td>
<td><p><span data-ttu-id="baa55-359">read-only</span><span class="sxs-lookup"><span data-stu-id="baa55-359">read-only</span></span></p></td>
<td><p><span data-ttu-id="baa55-360">read-only</span><span class="sxs-lookup"><span data-stu-id="baa55-360">read-only</span></span></p></td>
<td><p><span data-ttu-id="baa55-361">read-only</span><span class="sxs-lookup"><span data-stu-id="baa55-361">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-362"><a href="status-property-ado-recordset.md">Состояние</a></span><span class="sxs-lookup"><span data-stu-id="baa55-362"><a href="status-property-ado-recordset.md">Status</a></span></span></p></td>
<td><p><span data-ttu-id="baa55-363">read-only</span><span class="sxs-lookup"><span data-stu-id="baa55-363">read-only</span></span></p></td>
<td><p><span data-ttu-id="baa55-364">read-only</span><span class="sxs-lookup"><span data-stu-id="baa55-364">read-only</span></span></p></td>
<td><p><span data-ttu-id="baa55-365">read-only</span><span class="sxs-lookup"><span data-stu-id="baa55-365">read-only</span></span></p></td>
<td><p><span data-ttu-id="baa55-366">read-only</span><span class="sxs-lookup"><span data-stu-id="baa55-366">read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="baa55-367">Свойства [AbsolutePosition](absoluteposition-property-ado.md) и [AbsolutePage](absolutepage-property-ado.md) являются только для записи, когда ADO используется с версией 1.0 поставщика DB Microsoft OLE для ODBC.</span><span class="sxs-lookup"><span data-stu-id="baa55-367">The [AbsolutePosition](absoluteposition-property-ado.md) and [AbsolutePage](absolutepage-property-ado.md) properties are write-only when ADO is used with version 1.0 of the Microsoft OLE DB Provider for ODBC.</span></span>

<span data-ttu-id="baa55-368">Доступность стандартных методов ADO **Recordset:**</span><span class="sxs-lookup"><span data-stu-id="baa55-368">Availability of standard ADO **Recordset** methods:</span></span>

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
<th><p><span data-ttu-id="baa55-369">Метод</span><span class="sxs-lookup"><span data-stu-id="baa55-369">Method</span></span></p></th>
<th><p><span data-ttu-id="baa55-370">ForwardOnly</span><span class="sxs-lookup"><span data-stu-id="baa55-370">ForwardOnly</span></span></p></th>
<th><p><span data-ttu-id="baa55-371">Динамический</span><span class="sxs-lookup"><span data-stu-id="baa55-371">Dynamic</span></span></p></th>
<th><p><span data-ttu-id="baa55-372">Keyset</span><span class="sxs-lookup"><span data-stu-id="baa55-372">Keyset</span></span></p></th>
<th><p><span data-ttu-id="baa55-373">Статическое</span><span class="sxs-lookup"><span data-stu-id="baa55-373">Static</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="baa55-374"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="baa55-374"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="baa55-375">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-375">Yes</span></span></p></td>
<td><p><span data-ttu-id="baa55-376">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-376">Yes</span></span></p></td>
<td><p><span data-ttu-id="baa55-377">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-377">Yes</span></span></p></td>
<td><p><span data-ttu-id="baa55-378">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-378">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-379"><a href="cancel-method-ado.md">Отмена</a></span><span class="sxs-lookup"><span data-stu-id="baa55-379"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="baa55-380">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-380">Yes</span></span></p></td>
<td><p><span data-ttu-id="baa55-381">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-381">Yes</span></span></p></td>
<td><p><span data-ttu-id="baa55-382">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-382">Yes</span></span></p></td>
<td><p><span data-ttu-id="baa55-383">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-383">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-384"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="baa55-384"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="baa55-385">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-385">Yes</span></span></p></td>
<td><p><span data-ttu-id="baa55-386">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-386">Yes</span></span></p></td>
<td><p><span data-ttu-id="baa55-387">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-387">Yes</span></span></p></td>
<td><p><span data-ttu-id="baa55-388">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-388">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-389"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="baa55-389"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="baa55-390">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-390">Yes</span></span></p></td>
<td><p><span data-ttu-id="baa55-391">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-391">Yes</span></span></p></td>
<td><p><span data-ttu-id="baa55-392">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-392">Yes</span></span></p></td>
<td><p><span data-ttu-id="baa55-393">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-393">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-394"><a href="clone-method-ado.md">Clone</a></span><span class="sxs-lookup"><span data-stu-id="baa55-394"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="baa55-395">Нет</span><span class="sxs-lookup"><span data-stu-id="baa55-395">No</span></span></p></td>
<td><p><span data-ttu-id="baa55-396">Нет</span><span class="sxs-lookup"><span data-stu-id="baa55-396">No</span></span></p></td>
<td><p><span data-ttu-id="baa55-397">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-397">Yes</span></span></p></td>
<td><p><span data-ttu-id="baa55-398">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-398">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-399"><a href="close-method-ado.md">Close</a></span><span class="sxs-lookup"><span data-stu-id="baa55-399"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="baa55-400">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-400">Yes</span></span></p></td>
<td><p><span data-ttu-id="baa55-401">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-401">Yes</span></span></p></td>
<td><p><span data-ttu-id="baa55-402">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-402">Yes</span></span></p></td>
<td><p><span data-ttu-id="baa55-403">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-403">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-404"><a href="delete-method-ado-recordset.md">Delete</a></span><span class="sxs-lookup"><span data-stu-id="baa55-404"><a href="delete-method-ado-recordset.md">Delete</a></span></span></p></td>
<td><p><span data-ttu-id="baa55-405">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-405">Yes</span></span></p></td>
<td><p><span data-ttu-id="baa55-406">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-406">Yes</span></span></p></td>
<td><p><span data-ttu-id="baa55-407">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-407">Yes</span></span></p></td>
<td><p><span data-ttu-id="baa55-408">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-408">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-409"><a href="getrows-method-ado.md">GetRows</a></span><span class="sxs-lookup"><span data-stu-id="baa55-409"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="baa55-410">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-410">Yes</span></span></p></td>
<td><p><span data-ttu-id="baa55-411">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-411">Yes</span></span></p></td>
<td><p><span data-ttu-id="baa55-412">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-412">Yes</span></span></p></td>
<td><p><span data-ttu-id="baa55-413">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-413">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-414"><a href="move-method-ado.md">Move</a></span><span class="sxs-lookup"><span data-stu-id="baa55-414"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="baa55-415">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-415">Yes</span></span></p></td>
<td><p><span data-ttu-id="baa55-416">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-416">Yes</span></span></p></td>
<td><p><span data-ttu-id="baa55-417">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-417">Yes</span></span></p></td>
<td><p><span data-ttu-id="baa55-418">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-418">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-419"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span><span class="sxs-lookup"><span data-stu-id="baa55-419"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span></span></p></td>
<td><p><span data-ttu-id="baa55-420">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-420">Yes</span></span></p></td>
<td><p><span data-ttu-id="baa55-421">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-421">Yes</span></span></p></td>
<td><p><span data-ttu-id="baa55-422">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-422">Yes</span></span></p></td>
<td><p><span data-ttu-id="baa55-423">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-423">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-424"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span><span class="sxs-lookup"><span data-stu-id="baa55-424"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span></span></p></td>
<td><p><span data-ttu-id="baa55-425">Нет</span><span class="sxs-lookup"><span data-stu-id="baa55-425">No</span></span></p></td>
<td><p><span data-ttu-id="baa55-426">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-426">Yes</span></span></p></td>
<td><p><span data-ttu-id="baa55-427">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-427">Yes</span></span></p></td>
<td><p><span data-ttu-id="baa55-428">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-428">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-429"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span><span class="sxs-lookup"><span data-stu-id="baa55-429"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span></span></p></td>
<td><p><span data-ttu-id="baa55-430">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-430">Yes</span></span></p></td>
<td><p><span data-ttu-id="baa55-431">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-431">Yes</span></span></p></td>
<td><p><span data-ttu-id="baa55-432">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-432">Yes</span></span></p></td>
<td><p><span data-ttu-id="baa55-433">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-433">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-434"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span><span class="sxs-lookup"><span data-stu-id="baa55-434"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span></span></p></td>
<td><p><span data-ttu-id="baa55-435">Нет</span><span class="sxs-lookup"><span data-stu-id="baa55-435">No</span></span></p></td>
<td><p><span data-ttu-id="baa55-436">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-436">Yes</span></span></p></td>
<td><p><span data-ttu-id="baa55-437">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-437">Yes</span></span></p></td>
<td><p><span data-ttu-id="baa55-438">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-438">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-439"><a href="nextrecordset-method-ado.md">NextRecordset</a>\*</span><span class="sxs-lookup"><span data-stu-id="baa55-439"><a href="nextrecordset-method-ado.md">NextRecordset</a>\*</span></span></p></td>
<td><p><span data-ttu-id="baa55-440">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-440">Yes</span></span></p></td>
<td><p><span data-ttu-id="baa55-441">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-441">Yes</span></span></p></td>
<td><p><span data-ttu-id="baa55-442">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-442">Yes</span></span></p></td>
<td><p><span data-ttu-id="baa55-443">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-443">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-444"><a href="open-method-ado-recordset.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="baa55-444"><a href="open-method-ado-recordset.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="baa55-445">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-445">Yes</span></span></p></td>
<td><p><span data-ttu-id="baa55-446">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-446">Yes</span></span></p></td>
<td><p><span data-ttu-id="baa55-447">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-447">Yes</span></span></p></td>
<td><p><span data-ttu-id="baa55-448">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-448">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-449"><a href="requery-method-ado.md">Requery</a></span><span class="sxs-lookup"><span data-stu-id="baa55-449"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="baa55-450">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-450">Yes</span></span></p></td>
<td><p><span data-ttu-id="baa55-451">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-451">Yes</span></span></p></td>
<td><p><span data-ttu-id="baa55-452">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-452">Yes</span></span></p></td>
<td><p><span data-ttu-id="baa55-453">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-453">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-454"><a href="resync-method-ado.md">Resync</a></span><span class="sxs-lookup"><span data-stu-id="baa55-454"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="baa55-455">Нет</span><span class="sxs-lookup"><span data-stu-id="baa55-455">No</span></span></p></td>
<td><p><span data-ttu-id="baa55-456">Нет</span><span class="sxs-lookup"><span data-stu-id="baa55-456">No</span></span></p></td>
<td><p><span data-ttu-id="baa55-457">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-457">Yes</span></span></p></td>
<td><p><span data-ttu-id="baa55-458">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-458">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-459"><a href="supports-method-ado.md">Поддерживает</a></span><span class="sxs-lookup"><span data-stu-id="baa55-459"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="baa55-460">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-460">Yes</span></span></p></td>
<td><p><span data-ttu-id="baa55-461">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-461">Yes</span></span></p></td>
<td><p><span data-ttu-id="baa55-462">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-462">Yes</span></span></p></td>
<td><p><span data-ttu-id="baa55-463">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-463">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-464"><a href="update-method-ado.md">Обновление</a></span><span class="sxs-lookup"><span data-stu-id="baa55-464"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="baa55-465">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-465">Yes</span></span></p></td>
<td><p><span data-ttu-id="baa55-466">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-466">Yes</span></span></p></td>
<td><p><span data-ttu-id="baa55-467">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-467">Yes</span></span></p></td>
<td><p><span data-ttu-id="baa55-468">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-468">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-469"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="baa55-469"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="baa55-470">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-470">Yes</span></span></p></td>
<td><p><span data-ttu-id="baa55-471">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-471">Yes</span></span></p></td>
<td><p><span data-ttu-id="baa55-472">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-472">Yes</span></span></p></td>
<td><p><span data-ttu-id="baa55-473">Да</span><span class="sxs-lookup"><span data-stu-id="baa55-473">Yes</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="baa55-474">\*Не поддерживается для баз данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="baa55-474">\*Not supported for Microsoft Access databases.</span></span>

## <a name="dynamic-properties"></a><span data-ttu-id="baa55-475">Dynamic Properties</span><span class="sxs-lookup"><span data-stu-id="baa55-475">Dynamic Properties</span></span>

<span data-ttu-id="baa55-476">Поставщик DB Microsoft OLE для ODBC вставляет несколько динамических свойств в коллекцию **свойств** незапертых объектов [Connection,](connection-object-ado.md) [Recordset](recordset-object-ado.md)и [Command.](command-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="baa55-476">The Microsoft OLE DB Provider for ODBC inserts several dynamic properties into the **Properties** collection of the unopened [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md), and [Command](command-object-ado.md) objects.</span></span>

<span data-ttu-id="baa55-477">Ниже приведены перекрестные индексы имен ADO и OLE DB для каждого динамического свойства.</span><span class="sxs-lookup"><span data-stu-id="baa55-477">The tables below are a cross-index of the ADO and OLE DB names for each dynamic property.</span></span> <span data-ttu-id="baa55-478">Ссылка программиста OLE DB относится к имени свойства ADO по термину "Описание".</span><span class="sxs-lookup"><span data-stu-id="baa55-478">The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description."</span></span> <span data-ttu-id="baa55-479">Дополнительные сведения об этих свойствах можно найти в справке программиста OLE DB.</span><span class="sxs-lookup"><span data-stu-id="baa55-479">You can find more information about these properties in the OLE DB Programmer's Reference.</span></span> <span data-ttu-id="baa55-480">Поиск имени свойства OLE DB в Индексе или см. в приложении C: OLE DB Properties.</span><span class="sxs-lookup"><span data-stu-id="baa55-480">Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span></span>

## <a name="connection-dynamic-properties"></a><span data-ttu-id="baa55-481">Динамические свойства подключения</span><span class="sxs-lookup"><span data-stu-id="baa55-481">Connection Dynamic Properties</span></span>

<span data-ttu-id="baa55-482">Следующие свойства добавляются в коллекцию  Свойств объекта **Connection.**</span><span class="sxs-lookup"><span data-stu-id="baa55-482">The following properties are added to the **Connection** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="baa55-483">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="baa55-483">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="baa55-484">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="baa55-484">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="baa55-485">Активные сеансы</span><span class="sxs-lookup"><span data-stu-id="baa55-485">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="baa55-486">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="baa55-486">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-487">Asynchable Abort</span><span class="sxs-lookup"><span data-stu-id="baa55-487">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="baa55-488">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="baa55-488">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-489">Asynchable Commit</span><span class="sxs-lookup"><span data-stu-id="baa55-489">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="baa55-490">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="baa55-490">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-491">Уровни изоляции автокоммита</span><span class="sxs-lookup"><span data-stu-id="baa55-491">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="baa55-492">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="baa55-492">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-493">Расположение каталога</span><span class="sxs-lookup"><span data-stu-id="baa55-493">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="baa55-494">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="baa55-494">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-495">Термин Каталог</span><span class="sxs-lookup"><span data-stu-id="baa55-495">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="baa55-496">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="baa55-496">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-497">Определение столбцов</span><span class="sxs-lookup"><span data-stu-id="baa55-497">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="baa55-498">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="baa55-498">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-499">Подключение Время от времени</span><span class="sxs-lookup"><span data-stu-id="baa55-499">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="baa55-500">DBPROP_INIT_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="baa55-500">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-501">Текущий каталог</span><span class="sxs-lookup"><span data-stu-id="baa55-501">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="baa55-502">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="baa55-502">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-503">Источник данных</span><span class="sxs-lookup"><span data-stu-id="baa55-503">Data Source</span></span></p></td>
<td><p><span data-ttu-id="baa55-504">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="baa55-504">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-505">Имя источника данных</span><span class="sxs-lookup"><span data-stu-id="baa55-505">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="baa55-506">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="baa55-506">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-507">Модель потоковой обработки объектов источника данных</span><span class="sxs-lookup"><span data-stu-id="baa55-507">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="baa55-508">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="baa55-508">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-509">Имя DBMS</span><span class="sxs-lookup"><span data-stu-id="baa55-509">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="baa55-510">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="baa55-510">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-511">Версия DBMS</span><span class="sxs-lookup"><span data-stu-id="baa55-511">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="baa55-512">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="baa55-512">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-513">Расширенные свойства</span><span class="sxs-lookup"><span data-stu-id="baa55-513">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="baa55-514">DBPROP_INIT_PROVIDERSTRING</span><span class="sxs-lookup"><span data-stu-id="baa55-514">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-515">Поддержка GROUP BY</span><span class="sxs-lookup"><span data-stu-id="baa55-515">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="baa55-516">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="baa55-516">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-517">Гетерогенная поддержка таблиц</span><span class="sxs-lookup"><span data-stu-id="baa55-517">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="baa55-518">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="baa55-518">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-519">Чувствительность к делу идентификатора</span><span class="sxs-lookup"><span data-stu-id="baa55-519">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="baa55-520">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="baa55-520">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-521">Начальный каталог</span><span class="sxs-lookup"><span data-stu-id="baa55-521">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="baa55-522">DBPROP_INIT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="baa55-522">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-523">Уровни изоляции</span><span class="sxs-lookup"><span data-stu-id="baa55-523">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="baa55-524">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="baa55-524">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-525">Хранение изоляции</span><span class="sxs-lookup"><span data-stu-id="baa55-525">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="baa55-526">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="baa55-526">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-527">Идентификатор locale</span><span class="sxs-lookup"><span data-stu-id="baa55-527">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="baa55-528">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="baa55-528">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-529">Расположение</span><span class="sxs-lookup"><span data-stu-id="baa55-529">Location</span></span></p></td>
<td><p><span data-ttu-id="baa55-530">DBPROP_INIT_LOCATION</span><span class="sxs-lookup"><span data-stu-id="baa55-530">DBPROP_INIT_LOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-531">Максимальный размер индекса</span><span class="sxs-lookup"><span data-stu-id="baa55-531">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="baa55-532">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="baa55-532">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-533">Максимальный размер строки</span><span class="sxs-lookup"><span data-stu-id="baa55-533">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="baa55-534">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="baa55-534">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-535">Максимальный размер строки включает BLOB</span><span class="sxs-lookup"><span data-stu-id="baa55-535">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="baa55-536">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="baa55-536">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-537">Максимальные таблицы в SELECT</span><span class="sxs-lookup"><span data-stu-id="baa55-537">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="baa55-538">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="baa55-538">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-539">Режим</span><span class="sxs-lookup"><span data-stu-id="baa55-539">Mode</span></span></p></td>
<td><p><span data-ttu-id="baa55-540">DBPROP_INIT_MODE</span><span class="sxs-lookup"><span data-stu-id="baa55-540">DBPROP_INIT_MODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-541">Несколько наборов параметров</span><span class="sxs-lookup"><span data-stu-id="baa55-541">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="baa55-542">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="baa55-542">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-543">Несколько результатов</span><span class="sxs-lookup"><span data-stu-id="baa55-543">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="baa55-544">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="baa55-544">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-545">Несколько служба хранилища объектов</span><span class="sxs-lookup"><span data-stu-id="baa55-545">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="baa55-546">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="baa55-546">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-547">Обновление с несколькими таблицами</span><span class="sxs-lookup"><span data-stu-id="baa55-547">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="baa55-548">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="baa55-548">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-549">Порядок коллансирования NULL</span><span class="sxs-lookup"><span data-stu-id="baa55-549">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="baa55-550">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="baa55-550">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-551">NULL Concatenation Behaviour</span><span class="sxs-lookup"><span data-stu-id="baa55-551">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="baa55-552">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="baa55-552">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-553">Службы OLE DB</span><span class="sxs-lookup"><span data-stu-id="baa55-553">OLE DB Services</span></span></p></td>
<td><p><span data-ttu-id="baa55-554">DBPROP_INIT_OLEDBSERVICES</span><span class="sxs-lookup"><span data-stu-id="baa55-554">DBPROP_INIT_OLEDBSERVICES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-555">Версия OLE DB</span><span class="sxs-lookup"><span data-stu-id="baa55-555">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="baa55-556">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="baa55-556">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-557">Поддержка объектов OLE</span><span class="sxs-lookup"><span data-stu-id="baa55-557">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="baa55-558">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="baa55-558">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-559">Поддержка open Rowset</span><span class="sxs-lookup"><span data-stu-id="baa55-559">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="baa55-560">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="baa55-560">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-561">ORDER BY Columns in Select List</span><span class="sxs-lookup"><span data-stu-id="baa55-561">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="baa55-562">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="baa55-562">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-563">Доступность параметров вывода</span><span class="sxs-lookup"><span data-stu-id="baa55-563">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="baa55-564">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="baa55-564">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-565">Password</span><span class="sxs-lookup"><span data-stu-id="baa55-565">Password</span></span></p></td>
<td><p><span data-ttu-id="baa55-566">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="baa55-566">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-567">Pass By Ref Accessors</span><span class="sxs-lookup"><span data-stu-id="baa55-567">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="baa55-568">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="baa55-568">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-569">Сохраняются сведения о безопасности</span><span class="sxs-lookup"><span data-stu-id="baa55-569">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="baa55-570">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span><span class="sxs-lookup"><span data-stu-id="baa55-570">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-571">Тип сохраняемого ID</span><span class="sxs-lookup"><span data-stu-id="baa55-571">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="baa55-572">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="baa55-572">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-573">Подготовка поведения прервать</span><span class="sxs-lookup"><span data-stu-id="baa55-573">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="baa55-574">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="baa55-574">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-575">Подготовка поведения фиксации</span><span class="sxs-lookup"><span data-stu-id="baa55-575">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="baa55-576">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="baa55-576">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-577">Термин процедуры</span><span class="sxs-lookup"><span data-stu-id="baa55-577">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="baa55-578">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="baa55-578">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-579">Prompt</span><span class="sxs-lookup"><span data-stu-id="baa55-579">Prompt</span></span></p></td>
<td><p><span data-ttu-id="baa55-580">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="baa55-580">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-581">Удобное имя поставщика</span><span class="sxs-lookup"><span data-stu-id="baa55-581">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="baa55-582">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="baa55-582">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-583">Имя поставщика</span><span class="sxs-lookup"><span data-stu-id="baa55-583">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="baa55-584">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="baa55-584">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-585">Версия поставщика</span><span class="sxs-lookup"><span data-stu-id="baa55-585">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="baa55-586">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="baa55-586">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-587">Read-Only источник данных</span><span class="sxs-lookup"><span data-stu-id="baa55-587">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="baa55-588">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="baa55-588">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-589">Преобразования rowset в командной строке</span><span class="sxs-lookup"><span data-stu-id="baa55-589">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="baa55-590">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="baa55-590">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-591">Термин Схемы</span><span class="sxs-lookup"><span data-stu-id="baa55-591">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="baa55-592">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="baa55-592">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-593">Использование схемы</span><span class="sxs-lookup"><span data-stu-id="baa55-593">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="baa55-594">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="baa55-594">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-595">SQL Поддержка</span><span class="sxs-lookup"><span data-stu-id="baa55-595">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="baa55-596">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="baa55-596">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-597">Структурированные служба хранилища</span><span class="sxs-lookup"><span data-stu-id="baa55-597">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="baa55-598">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="baa55-598">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-599">Поддержка subquery</span><span class="sxs-lookup"><span data-stu-id="baa55-599">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="baa55-600">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="baa55-600">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-601">Термин Таблица</span><span class="sxs-lookup"><span data-stu-id="baa55-601">Table Term</span></span></p></td>
<td><p><span data-ttu-id="baa55-602">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="baa55-602">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-603">DDL транзакций</span><span class="sxs-lookup"><span data-stu-id="baa55-603">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="baa55-604">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="baa55-604">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-605">Идентификатор пользователя</span><span class="sxs-lookup"><span data-stu-id="baa55-605">User ID</span></span></p></td>
<td><p><span data-ttu-id="baa55-606">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="baa55-606">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-607">имя пользователя;</span><span class="sxs-lookup"><span data-stu-id="baa55-607">User Name</span></span></p></td>
<td><p><span data-ttu-id="baa55-608">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="baa55-608">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-609">Ручка окна</span><span class="sxs-lookup"><span data-stu-id="baa55-609">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="baa55-610">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="baa55-610">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a><span data-ttu-id="baa55-611">Динамические свойства Recordset</span><span class="sxs-lookup"><span data-stu-id="baa55-611">Recordset Dynamic Properties</span></span>

<span data-ttu-id="baa55-612">Следующие свойства добавляются в коллекцию Свойств  объекта **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="baa55-612">The following properties are added to the **Recordset** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="baa55-613">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="baa55-613">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="baa55-614">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="baa55-614">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="baa55-615">Порядок доступа</span><span class="sxs-lookup"><span data-stu-id="baa55-615">Access Order</span></span></p></td>
<td><p><span data-ttu-id="baa55-616">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="baa55-616">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-617">Блокировка служба хранилища объектов</span><span class="sxs-lookup"><span data-stu-id="baa55-617">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="baa55-618">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="baa55-618">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-619">Тип закладок</span><span class="sxs-lookup"><span data-stu-id="baa55-619">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="baa55-620">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="baa55-620">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-621">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="baa55-621">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="baa55-622">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="baa55-622">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-623">Изменение вставленных строк</span><span class="sxs-lookup"><span data-stu-id="baa55-623">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="baa55-624">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="baa55-624">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-625">Привилегии столбца</span><span class="sxs-lookup"><span data-stu-id="baa55-625">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="baa55-626">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="baa55-626">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-627">Уведомление о наборе столбцов</span><span class="sxs-lookup"><span data-stu-id="baa55-627">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="baa55-628">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="baa55-628">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-629">Задержка служба хранилища обновлений объектов</span><span class="sxs-lookup"><span data-stu-id="baa55-629">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="baa55-630">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="baa55-630">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-631">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="baa55-631">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="baa55-632">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="baa55-632">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-633">Строки удержания</span><span class="sxs-lookup"><span data-stu-id="baa55-633">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="baa55-634">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="baa55-634">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-635">IAccessor</span><span class="sxs-lookup"><span data-stu-id="baa55-635">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="baa55-636">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="baa55-636">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-637">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="baa55-637">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="baa55-638">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="baa55-638">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-639">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="baa55-639">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="baa55-640">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="baa55-640">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-641">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="baa55-641">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="baa55-642">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="baa55-642">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-643">IConvertType</span><span class="sxs-lookup"><span data-stu-id="baa55-643">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="baa55-644">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="baa55-644">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-645">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="baa55-645">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="baa55-646">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="baa55-646">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-647">IRowset</span><span class="sxs-lookup"><span data-stu-id="baa55-647">IRowset</span></span></p></td>
<td><p><span data-ttu-id="baa55-648">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="baa55-648">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-649">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="baa55-649">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="baa55-650">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="baa55-650">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-651">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="baa55-651">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="baa55-652">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="baa55-652">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-653">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="baa55-653">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="baa55-654">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="baa55-654">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-655">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="baa55-655">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="baa55-656">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="baa55-656">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-657">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="baa55-657">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-658">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="baa55-658">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="baa55-659">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="baa55-659">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-660">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="baa55-660">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="baa55-661">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="baa55-661">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-662">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="baa55-662">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="baa55-663">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="baa55-663">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-664">Буквальные закладки</span><span class="sxs-lookup"><span data-stu-id="baa55-664">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="baa55-665">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="baa55-665">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-666">Удостоверение буквальных строк</span><span class="sxs-lookup"><span data-stu-id="baa55-666">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="baa55-667">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="baa55-667">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-668">Максимальные открытые строки</span><span class="sxs-lookup"><span data-stu-id="baa55-668">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="baa55-669">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="baa55-669">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-670">Максимальное количество ожидающих строк</span><span class="sxs-lookup"><span data-stu-id="baa55-670">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="baa55-671">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="baa55-671">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-672">Максимальные строки</span><span class="sxs-lookup"><span data-stu-id="baa55-672">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="baa55-673">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="baa55-673">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-674">Детализация уведомлений</span><span class="sxs-lookup"><span data-stu-id="baa55-674">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="baa55-675">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="baa55-675">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-676">Этапы уведомлений</span><span class="sxs-lookup"><span data-stu-id="baa55-676">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="baa55-677">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="baa55-677">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-678">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="baa55-678">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="baa55-679">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="baa55-679">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-680">Собственные изменения Видимые</span><span class="sxs-lookup"><span data-stu-id="baa55-680">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="baa55-681">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="baa55-681">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-682">Собственные вставки Видимые</span><span class="sxs-lookup"><span data-stu-id="baa55-682">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="baa55-683">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="baa55-683">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-684">Сохранение на abort</span><span class="sxs-lookup"><span data-stu-id="baa55-684">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="baa55-685">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="baa55-685">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-686">Сохранение на коммит</span><span class="sxs-lookup"><span data-stu-id="baa55-686">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="baa55-687">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="baa55-687">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-688">Быстрая перезагрузка</span><span class="sxs-lookup"><span data-stu-id="baa55-688">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="baa55-689">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="baa55-689">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-690">События для повторного антуламента</span><span class="sxs-lookup"><span data-stu-id="baa55-690">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="baa55-691">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="baa55-691">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-692">Удаление удаленных строк</span><span class="sxs-lookup"><span data-stu-id="baa55-692">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="baa55-693">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="baa55-693">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-694">Отчет о нескольких изменениях</span><span class="sxs-lookup"><span data-stu-id="baa55-694">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="baa55-695">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="baa55-695">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-696">Возвращение ожидающих вставок</span><span class="sxs-lookup"><span data-stu-id="baa55-696">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="baa55-697">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="baa55-697">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-698">Уведомление об удалении строки</span><span class="sxs-lookup"><span data-stu-id="baa55-698">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="baa55-699">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="baa55-699">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-700">Уведомление о первом изменении строки</span><span class="sxs-lookup"><span data-stu-id="baa55-700">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="baa55-701">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="baa55-701">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-702">Уведомление о вставке строки</span><span class="sxs-lookup"><span data-stu-id="baa55-702">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="baa55-703">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="baa55-703">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-704">Привилегии строки</span><span class="sxs-lookup"><span data-stu-id="baa55-704">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="baa55-705">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="baa55-705">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-706">Уведомление о повторной синхронизации строк</span><span class="sxs-lookup"><span data-stu-id="baa55-706">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="baa55-707">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="baa55-707">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-708">Модель потоков строки</span><span class="sxs-lookup"><span data-stu-id="baa55-708">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="baa55-709">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="baa55-709">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-710">Уведомление об отмене строки</span><span class="sxs-lookup"><span data-stu-id="baa55-710">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="baa55-711">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="baa55-711">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-712">Уведомление об отмене строки</span><span class="sxs-lookup"><span data-stu-id="baa55-712">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="baa55-713">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="baa55-713">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-714">Уведомление об отмене строки</span><span class="sxs-lookup"><span data-stu-id="baa55-714">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="baa55-715">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="baa55-715">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-716">Уведомление об обновлении строки</span><span class="sxs-lookup"><span data-stu-id="baa55-716">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="baa55-717">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="baa55-717">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-718">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="baa55-718">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="baa55-719">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="baa55-719">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-720">Уведомление о выпуске Rowset</span><span class="sxs-lookup"><span data-stu-id="baa55-720">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="baa55-721">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="baa55-721">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-722">Прокрутите назад</span><span class="sxs-lookup"><span data-stu-id="baa55-722">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="baa55-723">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="baa55-723">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-724">Пропустить удаленные закладки</span><span class="sxs-lookup"><span data-stu-id="baa55-724">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="baa55-725">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="baa55-725">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-726">Удостоверение Strong Row</span><span class="sxs-lookup"><span data-stu-id="baa55-726">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="baa55-727">DBPROP_STRONGITDENTITY</span><span class="sxs-lookup"><span data-stu-id="baa55-727">DBPROP_STRONGITDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-728">Уникальные строки</span><span class="sxs-lookup"><span data-stu-id="baa55-728">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="baa55-729">DBPROP_UNIQUEROWS</span><span class="sxs-lookup"><span data-stu-id="baa55-729">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-730">Updatability</span><span class="sxs-lookup"><span data-stu-id="baa55-730">Updatability</span></span></p></td>
<td><p><span data-ttu-id="baa55-731">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="baa55-731">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-732">Использование закладок</span><span class="sxs-lookup"><span data-stu-id="baa55-732">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="baa55-733">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="baa55-733">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a><span data-ttu-id="baa55-734">Командные динамические свойства</span><span class="sxs-lookup"><span data-stu-id="baa55-734">Command Dynamic Properties</span></span>

<span data-ttu-id="baa55-735">Следующие свойства добавляются в коллекцию **Свойств** объекта **Command.**</span><span class="sxs-lookup"><span data-stu-id="baa55-735">The following properties are added to the **Command** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="baa55-736">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="baa55-736">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="baa55-737">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="baa55-737">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="baa55-738">Порядок доступа</span><span class="sxs-lookup"><span data-stu-id="baa55-738">Access Order</span></span></p></td>
<td><p><span data-ttu-id="baa55-739">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="baa55-739">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-740">Блокировка служба хранилища объектов</span><span class="sxs-lookup"><span data-stu-id="baa55-740">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="baa55-741">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="baa55-741">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-742">Тип закладок</span><span class="sxs-lookup"><span data-stu-id="baa55-742">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="baa55-743">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="baa55-743">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-744">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="baa55-744">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="baa55-745">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="baa55-745">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-746">Изменение вставленных строк</span><span class="sxs-lookup"><span data-stu-id="baa55-746">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="baa55-747">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="baa55-747">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-748">Привилегии столбца</span><span class="sxs-lookup"><span data-stu-id="baa55-748">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="baa55-749">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="baa55-749">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-750">Уведомление о наборе столбцов</span><span class="sxs-lookup"><span data-stu-id="baa55-750">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="baa55-751">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="baa55-751">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-752">Задержка служба хранилища обновлений объектов</span><span class="sxs-lookup"><span data-stu-id="baa55-752">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="baa55-753">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="baa55-753">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-754">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="baa55-754">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="baa55-755">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="baa55-755">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-756">Строки удержания</span><span class="sxs-lookup"><span data-stu-id="baa55-756">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="baa55-757">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="baa55-757">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-758">IAccessor</span><span class="sxs-lookup"><span data-stu-id="baa55-758">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="baa55-759">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="baa55-759">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-760">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="baa55-760">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="baa55-761">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="baa55-761">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-762">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="baa55-762">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="baa55-763">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="baa55-763">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-764">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="baa55-764">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="baa55-765">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="baa55-765">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-766">IConvertType</span><span class="sxs-lookup"><span data-stu-id="baa55-766">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="baa55-767">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="baa55-767">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-768">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="baa55-768">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="baa55-769">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="baa55-769">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-770">IRowset</span><span class="sxs-lookup"><span data-stu-id="baa55-770">IRowset</span></span></p></td>
<td><p><span data-ttu-id="baa55-771">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="baa55-771">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-772">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="baa55-772">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="baa55-773">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="baa55-773">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-774">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="baa55-774">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="baa55-775">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="baa55-775">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-776">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="baa55-776">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="baa55-777">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="baa55-777">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-778">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="baa55-778">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="baa55-779">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="baa55-779">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-780">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="baa55-780">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-781">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="baa55-781">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="baa55-782">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="baa55-782">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-783">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="baa55-783">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="baa55-784">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="baa55-784">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-785">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="baa55-785">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="baa55-786">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="baa55-786">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-787">Буквальные закладки</span><span class="sxs-lookup"><span data-stu-id="baa55-787">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="baa55-788">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="baa55-788">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-789">Удостоверение буквальных строк</span><span class="sxs-lookup"><span data-stu-id="baa55-789">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="baa55-790">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="baa55-790">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-791">Максимальные открытые строки</span><span class="sxs-lookup"><span data-stu-id="baa55-791">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="baa55-792">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="baa55-792">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-793">Максимальное количество ожидающих строк</span><span class="sxs-lookup"><span data-stu-id="baa55-793">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="baa55-794">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="baa55-794">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-795">Максимальные строки</span><span class="sxs-lookup"><span data-stu-id="baa55-795">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="baa55-796">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="baa55-796">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-797">Детализация уведомлений</span><span class="sxs-lookup"><span data-stu-id="baa55-797">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="baa55-798">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="baa55-798">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-799">Этапы уведомлений</span><span class="sxs-lookup"><span data-stu-id="baa55-799">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="baa55-800">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="baa55-800">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-801">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="baa55-801">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="baa55-802">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="baa55-802">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-803">Собственные изменения Видимые</span><span class="sxs-lookup"><span data-stu-id="baa55-803">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="baa55-804">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="baa55-804">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-805">Собственные вставки Видимые</span><span class="sxs-lookup"><span data-stu-id="baa55-805">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="baa55-806">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="baa55-806">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-807">Сохранение на abort</span><span class="sxs-lookup"><span data-stu-id="baa55-807">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="baa55-808">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="baa55-808">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-809">Сохранение на коммит</span><span class="sxs-lookup"><span data-stu-id="baa55-809">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="baa55-810">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="baa55-810">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-811">Быстрая перезагрузка</span><span class="sxs-lookup"><span data-stu-id="baa55-811">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="baa55-812">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="baa55-812">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-813">События для повторного антуламента</span><span class="sxs-lookup"><span data-stu-id="baa55-813">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="baa55-814">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="baa55-814">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-815">Удаление удаленных строк</span><span class="sxs-lookup"><span data-stu-id="baa55-815">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="baa55-816">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="baa55-816">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-817">Отчет о нескольких изменениях</span><span class="sxs-lookup"><span data-stu-id="baa55-817">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="baa55-818">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="baa55-818">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-819">Возвращение ожидающих вставок</span><span class="sxs-lookup"><span data-stu-id="baa55-819">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="baa55-820">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="baa55-820">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-821">Уведомление об удалении строки</span><span class="sxs-lookup"><span data-stu-id="baa55-821">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="baa55-822">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="baa55-822">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-823">Уведомление о первом изменении строки</span><span class="sxs-lookup"><span data-stu-id="baa55-823">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="baa55-824">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="baa55-824">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-825">Уведомление о вставке строки</span><span class="sxs-lookup"><span data-stu-id="baa55-825">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="baa55-826">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="baa55-826">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-827">Привилегии строки</span><span class="sxs-lookup"><span data-stu-id="baa55-827">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="baa55-828">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="baa55-828">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-829">Уведомление о повторной синхронизации строк</span><span class="sxs-lookup"><span data-stu-id="baa55-829">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="baa55-830">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="baa55-830">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-831">Модель потоков строки</span><span class="sxs-lookup"><span data-stu-id="baa55-831">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="baa55-832">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="baa55-832">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-833">Уведомление об отмене строки</span><span class="sxs-lookup"><span data-stu-id="baa55-833">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="baa55-834">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="baa55-834">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-835">Уведомление об отмене строки</span><span class="sxs-lookup"><span data-stu-id="baa55-835">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="baa55-836">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="baa55-836">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-837">Уведомление об отмене строки</span><span class="sxs-lookup"><span data-stu-id="baa55-837">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="baa55-838">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="baa55-838">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-839">Уведомление об обновлении строки</span><span class="sxs-lookup"><span data-stu-id="baa55-839">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="baa55-840">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="baa55-840">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-841">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="baa55-841">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="baa55-842">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="baa55-842">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-843">Уведомление о выпуске Rowset</span><span class="sxs-lookup"><span data-stu-id="baa55-843">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="baa55-844">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="baa55-844">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-845">Прокрутите назад</span><span class="sxs-lookup"><span data-stu-id="baa55-845">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="baa55-846">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="baa55-846">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-847">Пропустить удаленные закладки</span><span class="sxs-lookup"><span data-stu-id="baa55-847">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="baa55-848">DBPROP_BOOKMARKSKIP</span><span class="sxs-lookup"><span data-stu-id="baa55-848">DBPROP_BOOKMARKSKIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-849">Удостоверение Strong Row</span><span class="sxs-lookup"><span data-stu-id="baa55-849">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="baa55-850">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="baa55-850">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa55-851">Updatability</span><span class="sxs-lookup"><span data-stu-id="baa55-851">Updatability</span></span></p></td>
<td><p><span data-ttu-id="baa55-852">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="baa55-852">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa55-853">Использование закладок</span><span class="sxs-lookup"><span data-stu-id="baa55-853">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="baa55-854">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="baa55-854">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="baa55-855">См. также</span><span class="sxs-lookup"><span data-stu-id="baa55-855">See also</span></span>

<span data-ttu-id="baa55-856">Сведения о конкретной реализации и функциональных сведениях о поставщике DB Microsoft OLE для ODBC можно получить в руководстве программиста [OLE DB](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85)) или в Центре разработчиков [платформы данных.](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017)</span><span class="sxs-lookup"><span data-stu-id="baa55-856">For details regarding specific implementation and functional information about the Microsoft OLE DB Provider for ODBC, consult the [OLE DB Programmer's Guide](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85)) or visit the [Data Platform Developer Center](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).</span></span>

