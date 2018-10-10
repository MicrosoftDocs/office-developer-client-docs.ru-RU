---
title: Microsoft OLE DB Provider for ODBC
TOCTitle: Microsoft OLE DB Provider for ODBC
ms:assetid: c507567e-5ad1-b32a-f6ad-5ba2c39aa4c2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249964(v=office.15)
ms:contentKeyID: 48547602
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 168799b517598211ca9de680730490a0a41d1dde
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483143"
---
# <a name="microsoft-ole-db-provider-for-odbc"></a><span data-ttu-id="0695e-102">Microsoft OLE DB Provider for ODBC</span><span class="sxs-lookup"><span data-stu-id="0695e-102">Microsoft OLE DB Provider for ODBC</span></span>

<span data-ttu-id="0695e-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0695e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0695e-104">Чтобы программист ADO или служб удаленных рабочих СТОЛОВ идеальном мире бы одно в каждом данных источника предоставляет интерфейс OLE DB, чтобы вызвать непосредственно в источник данных ADO.</span><span class="sxs-lookup"><span data-stu-id="0695e-104">To an ADO or RDS programmer, an ideal world would be one in which every data source exposes an OLE DB interface, so that ADO could call directly into the data source.</span></span> <span data-ttu-id="0695e-105">Несмотря на то, что все больше дополнительные базы данных поставщиков реализует интерфейсы OLE DB, некоторые источники данных не еще не представленных таким способом.</span><span class="sxs-lookup"><span data-stu-id="0695e-105">Although increasingly more database vendors are implementing OLE DB interfaces, some data sources are not yet exposed this way.</span></span> <span data-ttu-id="0695e-106">Тем не менее практически все СУБД в настоящее время может осуществляться через ODBC.</span><span class="sxs-lookup"><span data-stu-id="0695e-106">However, virtually all DBMS systems in use today can be accessed through ODBC.</span></span>

<span data-ttu-id="0695e-107">Драйверы ODBC доступны для всех основных СУБД, в настоящее время, включая Microsoft SQL Server, Microsoft Access (базы данных Microsoft Jet) и Microsoft FoxPro, кроме базы данных сторонних продуктов, таких как Oracle.</span><span class="sxs-lookup"><span data-stu-id="0695e-107">ODBC drivers are available for every major DBMS in use today, including Microsoft SQL Server, Microsoft Access (Microsoft Jet database engine), and Microsoft FoxPro, in addition to non-Microsoft database products such as Oracle.</span></span>

<span data-ttu-id="0695e-108">Поставщик ODBC Microsoft, однако позволяет ADO для подключения к источникам данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="0695e-108">The Microsoft ODBC Provider, however, allows ADO to connect to any ODBC data source.</span></span> <span data-ttu-id="0695e-109">Поставщик свободных потоков и Юникод.</span><span class="sxs-lookup"><span data-stu-id="0695e-109">The provider is free-threaded and Unicode enabled.</span></span>

<span data-ttu-id="0695e-110">Поставщик поддерживает транзакции, несмотря на то, что разные ядра СУБД предлагают различные виды поддержки транзакций.</span><span class="sxs-lookup"><span data-stu-id="0695e-110">The provider supports transactions, although different DBMS engines offer different types of transaction support.</span></span> <span data-ttu-id="0695e-111">Например Microsoft Access поддерживает до пяти уровней вложенных транзакций.</span><span class="sxs-lookup"><span data-stu-id="0695e-111">For example, Microsoft Access supports nested transactions up to five levels deep.</span></span>

<span data-ttu-id="0695e-112">Поставщик по умолчанию для ADO и поддерживаются все зависящие от поставщика ADO свойства и методы.</span><span class="sxs-lookup"><span data-stu-id="0695e-112">This is the default provider for ADO, and all provider-dependent ADO properties and methods are supported.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="0695e-113">Параметры строки подключения</span><span class="sxs-lookup"><span data-stu-id="0695e-113">Connection String Parameters</span></span>

<span data-ttu-id="0695e-114">Для подключения к данным поставщиком, задайте **поставщика =** аргумент свойства [ConnectionString](connectionstring-property-ado.md) для:</span><span class="sxs-lookup"><span data-stu-id="0695e-114">To connect to this provider, set the **Provider=** argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```sql 
 
MSDASQL 
```

<span data-ttu-id="0695e-115">Чтение свойства [поставщика](provider-property-ado.md) будет возвращать также этой строки.</span><span class="sxs-lookup"><span data-stu-id="0695e-115">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="0695e-116">Типичная строка подключения</span><span class="sxs-lookup"><span data-stu-id="0695e-116">Typical Connection String</span></span>

<span data-ttu-id="0695e-117">— Это строка соединения для данного поставщика:</span><span class="sxs-lookup"><span data-stu-id="0695e-117">A typical connection string for this provider is:</span></span>

```sql 
 
"Provider=MSDASQL;DSN=dsnName;UID=userName;PWD=userPassword;" 
```

<span data-ttu-id="0695e-118">Строка состоит из следующих ключевых слов:</span><span class="sxs-lookup"><span data-stu-id="0695e-118">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0695e-119">Keyword</span><span class="sxs-lookup"><span data-stu-id="0695e-119">Keyword</span></span></p></th>
<th><p><span data-ttu-id="0695e-120">Описание</span><span class="sxs-lookup"><span data-stu-id="0695e-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0695e-121"><strong>Поставщик</strong></span><span class="sxs-lookup"><span data-stu-id="0695e-121"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="0695e-122">Задает поставщика OLE DB для ODBC.</span><span class="sxs-lookup"><span data-stu-id="0695e-122">Specifies the OLE DB Provider for ODBC.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-123"><strong>УВЕДОМЛЕНИЯ О ДОСТАВКЕ</strong></span><span class="sxs-lookup"><span data-stu-id="0695e-123"><strong>DSN</strong></span></span></p></td>
<td><p><span data-ttu-id="0695e-124">Указывает имя источника данных.</span><span class="sxs-lookup"><span data-stu-id="0695e-124">Specifies the data source name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-125"><strong>UID</strong></span><span class="sxs-lookup"><span data-stu-id="0695e-125"><strong>UID</strong></span></span></p></td>
<td><p><span data-ttu-id="0695e-126">Задает имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="0695e-126">Specifies the user name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-127"><strong>PWD</strong></span><span class="sxs-lookup"><span data-stu-id="0695e-127"><strong>PWD</strong></span></span></p></td>
<td><p><span data-ttu-id="0695e-128">Задает пароль пользователя.</span><span class="sxs-lookup"><span data-stu-id="0695e-128">Specifies the user password.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-129"><strong>URL</strong>.</span><span class="sxs-lookup"><span data-stu-id="0695e-129"><strong>URL</strong></span></span></p></td>
<td><p><span data-ttu-id="0695e-130">Задает URL-адрес файла или папки, опубликованной в веб-папку.</span><span class="sxs-lookup"><span data-stu-id="0695e-130">Specifies the URL of a file or directory published in a Web folder.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0695e-131">Так как это поставщика по умолчанию для ADO, если опустить **поставщика =** параметра в строке подключения ADO пытается установить подключение к данным поставщиком.</span><span class="sxs-lookup"><span data-stu-id="0695e-131">Because this is the default provider for ADO, if you omit the **Provider=** parameter from the connection string, ADO will attempt to establish a connection to this provider.</span></span>

<span data-ttu-id="0695e-132">Поставщик не поддерживает параметры подключения в дополнение к определяемые ADO.</span><span class="sxs-lookup"><span data-stu-id="0695e-132">The provider does not support any specific connection parameters in addition to those defined by ADO.</span></span> <span data-ttu-id="0695e-133">Тем не менее Поставщик передает параметры соединения не ADO драйвера ODBC.</span><span class="sxs-lookup"><span data-stu-id="0695e-133">However, the provider will pass any non-ADO connection parameters to the ODBC driver manager.</span></span>

<span data-ttu-id="0695e-134">Так как можно опустить параметр **поставщика** , таким образом можно создать строку подключения ADO, идентичный строки подключения ODBC для одного источника данных.</span><span class="sxs-lookup"><span data-stu-id="0695e-134">Because you can omit the **Provider** parameter, you can therefore compose an ADO connection string that is identical to an ODBC connection string for the same data source.</span></span> <span data-ttu-id="0695e-135">Используйте одинаковые имена параметров (**ДРАЙВЕРА =**, **базы данных =**, **уведомления о Доставке =** и так далее), значения и синтаксис, как вы бы при создании строки подключения ODBC.</span><span class="sxs-lookup"><span data-stu-id="0695e-135">Use the same parameter names (**DRIVER=**, **DATABASE=**, **DSN=**, and so on), values, and syntax as you would when composing an ODBC connection string.</span></span> <span data-ttu-id="0695e-136">Можно подключить с и без имя источника данных (DSN) или FileDSN.</span><span class="sxs-lookup"><span data-stu-id="0695e-136">You can connect with or without a predefined data source name (DSN) or FileDSN.</span></span>

<span data-ttu-id="0695e-137">**Синтаксис с уведомления о Доставке или FileDSN:**</span><span class="sxs-lookup"><span data-stu-id="0695e-137">**Syntax with a DSN or FileDSN:**</span></span>

`"[Provider=MSDASQL;] { DSN=name | FileDSN=filename } ; [DATABASE=database;] UID=user; PWD=password"`

<span data-ttu-id="0695e-138">**Синтаксис без уведомления о Доставке (соединения):**</span><span class="sxs-lookup"><span data-stu-id="0695e-138">**Syntax without a DSN (DSN-less connection):**</span></span>

`"[Provider=MSDASQL;] DRIVER=driver; SERVER=server;DATABASE=database; UID=user; PWD=password"`

<span data-ttu-id="0695e-139">Если вы используете **уведомления о Доставке** или **FileDSN**, его необходимо определить через источники данных ODBC в панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="0695e-139">If you use a **DSN** or **FileDSN**, it must be defined through the ODBC Data Source Administrator in the Windows Control Panel.</span></span> <span data-ttu-id="0695e-140">В Microsoft Windows 2000 администратор ODBC находится в разделе Администрирование.</span><span class="sxs-lookup"><span data-stu-id="0695e-140">In Microsoft Windows 2000, the ODBC Administrator is located under Administrative Tools.</span></span> <span data-ttu-id="0695e-141">В предыдущих версиях Windows значок администратор ODBC называется **32-разрядная версия ODBC** или просто **ODBC**.</span><span class="sxs-lookup"><span data-stu-id="0695e-141">In previous versions of Windows, the ODBC Administrator icon is named **32-bit ODBC** or simply **ODBC**.</span></span>

<span data-ttu-id="0695e-142">В качестве альтернативы для установки **уведомления о Доставке**, можно указать драйвер ODBC (**ДРАЙВЕРА =**), например «SQL Server»; имя сервера (**SERVER =**); и имя базы данных (**базы данных =**).</span><span class="sxs-lookup"><span data-stu-id="0695e-142">As an alternative to setting a **DSN**, you can specify the ODBC driver (**DRIVER=**), such as "SQL Server;" the server name (**SERVER=**); and the database name (**DATABASE=**).</span></span>

<span data-ttu-id="0695e-143">Также можно указать имя учетной записи пользователя (**UID =**) и пароль для учетной записи пользователя (**PWD =**) в параметры, относящиеся к ODBC или в стандартный определенные ADO *пользователя* и *пароль* параметры.</span><span class="sxs-lookup"><span data-stu-id="0695e-143">You can also specify a user account name (**UID=**), and the password for the user account (**PWD=**) in the ODBC-specific parameters or in the standard ADO-defined *user* and *password* parameters.</span></span>

<span data-ttu-id="0695e-144">Хотя **уведомления о Доставке** определение уже указывает базу данных, можно задать *параметр *базы данных* , в дополнение к **уведомления о Доставке** для подключения в другую базу данных* .</span><span class="sxs-lookup"><span data-stu-id="0695e-144">Although a **DSN** definition already specifies a database, you can specify *a* *database* parameter in addition to a **DSN** to connect to a different database.</span></span> <span data-ttu-id="0695e-145">Рекомендуется всегда включать \*параметр *базы данных* \* при использовании **уведомления о Доставке**.</span><span class="sxs-lookup"><span data-stu-id="0695e-145">It is a good idea to always include *the* *database* parameter when you use a **DSN**.</span></span> <span data-ttu-id="0695e-146">Это обеспечит подключиться к базе соответствующих прав в случае, когда другой пользователь изменить параметр базы данных по умолчанию с момента последнего извлечения определения **уведомления о Доставке** .</span><span class="sxs-lookup"><span data-stu-id="0695e-146">This will ensure that you connect to the proper database in the event that another user changed the default database parameter since you last checked the **DSN** definition.</span></span>

## <a name="provider-specific-connection-properties"></a><span data-ttu-id="0695e-147">Свойства подключения от поставщика</span><span class="sxs-lookup"><span data-stu-id="0695e-147">Provider-Specific Connection Properties</span></span>

<span data-ttu-id="0695e-148">Поставщик OLE DB для ODBC добавляет несколько свойств в коллекцию [свойств](properties-collection-ado.md) объекта **подключения** .</span><span class="sxs-lookup"><span data-stu-id="0695e-148">The OLE DB provider for ODBC adds several properties to the [Properties](properties-collection-ado.md) collection of the **Connection** object.</span></span> <span data-ttu-id="0695e-149">В следующей таблице перечислены эти свойства имя соответствующего свойства OLE DB в скобки.</span><span class="sxs-lookup"><span data-stu-id="0695e-149">The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0695e-150">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="0695e-150">Property Name</span></span></p></th>
<th><p><span data-ttu-id="0695e-151">Описание</span><span class="sxs-lookup"><span data-stu-id="0695e-151">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0695e-152">Доступны процедуры</span><span class="sxs-lookup"><span data-stu-id="0695e-152">Accessible Procedures</span></span><br />
<span data-ttu-id="0695e-153">(KAGPROP_ACCESSIBLEPROCEDURES)</span><span class="sxs-lookup"><span data-stu-id="0695e-153">(KAGPROP_ACCESSIBLEPROCEDURES)</span></span></p></td>
<td><p><span data-ttu-id="0695e-154">Указывает, является ли пользователь имеет доступ к хранимые процедуры.</span><span class="sxs-lookup"><span data-stu-id="0695e-154">Indicates whether the user has access to stored procedures.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-155">Доступно таблиц</span><span class="sxs-lookup"><span data-stu-id="0695e-155">Accessible Tables</span></span><br />
<span data-ttu-id="0695e-156">(KAGPROP_ACCESSIBLETABLES)</span><span class="sxs-lookup"><span data-stu-id="0695e-156">(KAGPROP_ACCESSIBLETABLES)</span></span></p></td>
<td><p><span data-ttu-id="0695e-157">Указывает, является ли пользователь имеет разрешения на выполнение инструкций SELECT таблиц базы данных.</span><span class="sxs-lookup"><span data-stu-id="0695e-157">Indicates whether the user has permission to execute SELECT statements against the database tables.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-158">Активные операторы</span><span class="sxs-lookup"><span data-stu-id="0695e-158">Active Statements</span></span><br />
<span data-ttu-id="0695e-159">(KAGPROP_ACTIVESTATEMENTS)</span><span class="sxs-lookup"><span data-stu-id="0695e-159">(KAGPROP_ACTIVESTATEMENTS)</span></span></p></td>
<td><p><span data-ttu-id="0695e-160">Указывает число дескрипторов, которые может поддерживать драйвера ODBC для подключения.</span><span class="sxs-lookup"><span data-stu-id="0695e-160">Indicates the number of handles an ODBC driver can support on a connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-161">Имя драйвера</span><span class="sxs-lookup"><span data-stu-id="0695e-161">Driver Name</span></span><br />
<span data-ttu-id="0695e-162">(KAGPROP_DRIVERNAME)</span><span class="sxs-lookup"><span data-stu-id="0695e-162">(KAGPROP_DRIVERNAME)</span></span></p></td>
<td><p><span data-ttu-id="0695e-163">Указывает имя файла драйвера ODBC.</span><span class="sxs-lookup"><span data-stu-id="0695e-163">Indicates the file name of the ODBC driver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-164">Версия драйвера ODBC</span><span class="sxs-lookup"><span data-stu-id="0695e-164">Driver ODBC Version</span></span><br />
<span data-ttu-id="0695e-165">(KAGPROP_DRIVERODBCVER)</span><span class="sxs-lookup"><span data-stu-id="0695e-165">(KAGPROP_DRIVERODBCVER)</span></span></p></td>
<td><p><span data-ttu-id="0695e-166">Указывает версию, поддерживающего этот драйвер ODBC.</span><span class="sxs-lookup"><span data-stu-id="0695e-166">Indicates the version of ODBC that this driver supports.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-167">Использование файлов</span><span class="sxs-lookup"><span data-stu-id="0695e-167">File Usage</span></span><br />
<span data-ttu-id="0695e-168">(KAGPROP_FILEUSAGE)</span><span class="sxs-lookup"><span data-stu-id="0695e-168">(KAGPROP_FILEUSAGE)</span></span></p></td>
<td><p><span data-ttu-id="0695e-169">Указывает, как драйвер обрабатывает файл источника данных. как таблицы или как к каталогу.</span><span class="sxs-lookup"><span data-stu-id="0695e-169">Indicates how the driver treats a file in a data source; as a table or as a catalog.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-170">Как предложение escape-последовательности</span><span class="sxs-lookup"><span data-stu-id="0695e-170">Like Escape Clause</span></span><br />
<span data-ttu-id="0695e-171">(KAGPROP_LIKEESCAPECLAUSE)</span><span class="sxs-lookup"><span data-stu-id="0695e-171">(KAGPROP_LIKEESCAPECLAUSE)</span></span></p></td>
<td><p><span data-ttu-id="0695e-172">Указывает предикат LIKE предложение WHERE ли драйвер поддерживается в определение и использование escape-символ знаком процента (%) и символ подчеркивания (_).</span><span class="sxs-lookup"><span data-stu-id="0695e-172">Indicates whether the driver supports the definition and use of an escape character for the percent character (%) and underline character (_) in the LIKE predicate of a WHERE clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-173">Максимальное число столбцов в группировать по</span><span class="sxs-lookup"><span data-stu-id="0695e-173">Max Columns in Group By</span></span><br />
<span data-ttu-id="0695e-174">(KAGPROP_MAXCOLUMNSINGROUPBY)</span><span class="sxs-lookup"><span data-stu-id="0695e-174">(KAGPROP_MAXCOLUMNSINGROUPBY)</span></span></p></td>
<td><p><span data-ttu-id="0695e-175">Указывает максимальное число столбцов, которые могут быть перечислены в предложении GROUP BY инструкции SELECT.</span><span class="sxs-lookup"><span data-stu-id="0695e-175">Indicates the maximum number of columns that can be listed in the GROUP BY clause of a SELECT statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-176">Максимальное число столбцов в индексе</span><span class="sxs-lookup"><span data-stu-id="0695e-176">Max Columns in Index</span></span><br />
<span data-ttu-id="0695e-177">(KAGPROP_MAXCOLUMNSININDEX)</span><span class="sxs-lookup"><span data-stu-id="0695e-177">(KAGPROP_MAXCOLUMNSININDEX)</span></span></p></td>
<td><p><span data-ttu-id="0695e-178">Указывает максимальное число столбцов, которые можно включить в индекс.</span><span class="sxs-lookup"><span data-stu-id="0695e-178">Indicates the maximum number of columns that can be included in an index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-179">Максимальное число столбцов в порядке</span><span class="sxs-lookup"><span data-stu-id="0695e-179">Max Columns in Order By</span></span><br />
<span data-ttu-id="0695e-180">(KAGPROP_MAXCOLUMNSINORDERBY)</span><span class="sxs-lookup"><span data-stu-id="0695e-180">(KAGPROP_MAXCOLUMNSINORDERBY)</span></span></p></td>
<td><p><span data-ttu-id="0695e-181">Указывает максимальное число столбцов, которые могут быть перечислены в предложение ORDER BY инструкции SELECT.</span><span class="sxs-lookup"><span data-stu-id="0695e-181">Indicates the maximum number of columns that can be listed in the ORDER BY clause of a SELECT statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-182">Максимальное число столбцов в Выбор</span><span class="sxs-lookup"><span data-stu-id="0695e-182">Max Columns in Select</span></span><br />
<span data-ttu-id="0695e-183">(KAGPROP_MAXCOLUMNSINSELECT)</span><span class="sxs-lookup"><span data-stu-id="0695e-183">(KAGPROP_MAXCOLUMNSINSELECT)</span></span></p></td>
<td><p><span data-ttu-id="0695e-184">Указывает максимальное число столбцов, которые могут быть перечислены в разделе SELECT инструкции SELECT.</span><span class="sxs-lookup"><span data-stu-id="0695e-184">Indicates the maximum number of columns that can be listed in the SELECT portion of a SELECT statement.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-185">Максимальное число столбцов в таблице</span><span class="sxs-lookup"><span data-stu-id="0695e-185">Max Columns in Table</span></span><br />
<span data-ttu-id="0695e-186">(KAGPROP_MAXCOLUMNSINTABLE)</span><span class="sxs-lookup"><span data-stu-id="0695e-186">(KAGPROP_MAXCOLUMNSINTABLE)</span></span></p></td>
<td><p><span data-ttu-id="0695e-187">Указывает максимальное число столбцов в таблице.</span><span class="sxs-lookup"><span data-stu-id="0695e-187">Indicates the maximum number of columns allowed in a table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-188">Числовые функции</span><span class="sxs-lookup"><span data-stu-id="0695e-188">Numeric Functions</span></span><br />
<span data-ttu-id="0695e-189">(KAGPROP_NUMERICFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="0695e-189">(KAGPROP_NUMERICFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="0695e-190">Указывает, какие числовые функции поддерживаются драйвер ODBC.</span><span class="sxs-lookup"><span data-stu-id="0695e-190">Indicates which numeric functions are supported by the ODBC driver.</span></span> <span data-ttu-id="0695e-191">Список имен функций и связанные значения, используемые в этом Битовая маска, см в приложении д: скалярные в документации по ODBC.</span><span class="sxs-lookup"><span data-stu-id="0695e-191">For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-192">Возможности внешнего соединения</span><span class="sxs-lookup"><span data-stu-id="0695e-192">Outer Join Capabilities</span></span><br />
<span data-ttu-id="0695e-193">(KAGPROP_OJCAPABILITY)</span><span class="sxs-lookup"><span data-stu-id="0695e-193">(KAGPROP_OJCAPABILITY)</span></span></p></td>
<td><p><span data-ttu-id="0695e-194">Указывает типы ВНЕШНИЕ соединения, поддерживаемых поставщиком.</span><span class="sxs-lookup"><span data-stu-id="0695e-194">Indicates the types of OUTER JOINs supported by the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-195">Внешние соединения</span><span class="sxs-lookup"><span data-stu-id="0695e-195">Outer Joins</span></span><br />
<span data-ttu-id="0695e-196">(KAGPROP_OUTERJOINS)</span><span class="sxs-lookup"><span data-stu-id="0695e-196">(KAGPROP_OUTERJOINS)</span></span></p></td>
<td><p><span data-ttu-id="0695e-197">Указывает, является ли поставщик поддерживает ВНЕШНИЕ соединения.</span><span class="sxs-lookup"><span data-stu-id="0695e-197">Indicates whether the provider supports OUTER JOINs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-198">Специальные символы</span><span class="sxs-lookup"><span data-stu-id="0695e-198">Special Characters</span></span><br />
<span data-ttu-id="0695e-199">(KAGPROP_SPECIALCHARACTERS)</span><span class="sxs-lookup"><span data-stu-id="0695e-199">(KAGPROP_SPECIALCHARACTERS)</span></span></p></td>
<td><p><span data-ttu-id="0695e-200">Указывает, какие символы имеет особое значение для драйвера ODBC.</span><span class="sxs-lookup"><span data-stu-id="0695e-200">Indicates which characters have special meaning for the ODBC driver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-201">Хранимые процедуры</span><span class="sxs-lookup"><span data-stu-id="0695e-201">Stored Procedures</span></span><br />
<span data-ttu-id="0695e-202">(KAGPROP_PROCEDURES)</span><span class="sxs-lookup"><span data-stu-id="0695e-202">(KAGPROP_PROCEDURES)</span></span></p></td>
<td><p><span data-ttu-id="0695e-203">Указывает, доступны ли хранимые процедуры для использования с этой драйвер ODBC.</span><span class="sxs-lookup"><span data-stu-id="0695e-203">Indicates whether stored procedures are available for use with this ODBC driver.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-204">Строковые функции</span><span class="sxs-lookup"><span data-stu-id="0695e-204">String Functions</span></span><br />
<span data-ttu-id="0695e-205">(KAGPROP_STRINGFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="0695e-205">(KAGPROP_STRINGFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="0695e-206">Указывает, какие функции string, поддерживаются драйвер ODBC.</span><span class="sxs-lookup"><span data-stu-id="0695e-206">Indicates which string functions are supported by the ODBC driver.</span></span> <span data-ttu-id="0695e-207">Список имен функций и связанные значения, используемые в этом Битовая маска, см в приложении д: скалярные в документации по ODBC.</span><span class="sxs-lookup"><span data-stu-id="0695e-207">For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-208">Системные функции</span><span class="sxs-lookup"><span data-stu-id="0695e-208">System Functions</span></span><br />
<span data-ttu-id="0695e-209">(KAGPROP_SYSTEMFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="0695e-209">(KAGPROP_SYSTEMFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="0695e-210">Указывает, какие функции системы поддерживаются драйвер ODBC.</span><span class="sxs-lookup"><span data-stu-id="0695e-210">Indicates which system functions are supported by the ODBC driver.</span></span> <span data-ttu-id="0695e-211">Список имен функций и связанные значения, используемые в этом Битовая маска, см в приложении д: скалярные в документации по ODBC.</span><span class="sxs-lookup"><span data-stu-id="0695e-211">For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-212">Время и Дата функции</span><span class="sxs-lookup"><span data-stu-id="0695e-212">Time/Date Functions</span></span><br />
<span data-ttu-id="0695e-213">(KAGPROP_TIMEDATEFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="0695e-213">(KAGPROP_TIMEDATEFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="0695e-214">Указывает, какие функции даты и времени поддерживаются драйвер ODBC.</span><span class="sxs-lookup"><span data-stu-id="0695e-214">Indicates which time and date functions are supported by the ODBC driver.</span></span> <span data-ttu-id="0695e-215">Список имен функций и связанные значения, используемые в этом Битовая маска, см в приложении д: скалярные в документации по ODBC.</span><span class="sxs-lookup"><span data-stu-id="0695e-215">For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-216">Поддержка грамматики SQL</span><span class="sxs-lookup"><span data-stu-id="0695e-216">SQL Grammar Support</span></span><br />
<span data-ttu-id="0695e-217">(KAGPROP_ODBCSQLCONFORMANCE)</span><span class="sxs-lookup"><span data-stu-id="0695e-217">(KAGPROP_ODBCSQLCONFORMANCE)</span></span></p></td>
<td><p><span data-ttu-id="0695e-218">Указывает грамматику SQL, которая поддерживает драйвер ODBC.</span><span class="sxs-lookup"><span data-stu-id="0695e-218">Indicates the SQL grammar that the ODBC driver supports.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-recordset-and-command-properties"></a><span data-ttu-id="0695e-219">Свойства команды и записей от поставщика</span><span class="sxs-lookup"><span data-stu-id="0695e-219">Provider-Specific Recordset and Command Properties</span></span>

<span data-ttu-id="0695e-220">Поставщик OLE DB для ODBC добавляет несколько свойств **Свойства** набора **записей** и **командных** объектов.</span><span class="sxs-lookup"><span data-stu-id="0695e-220">The OLE DB provider for ODBC adds several properties to the **Properties** collection of the **Recordset** and **Command** objects.</span></span> <span data-ttu-id="0695e-221">В следующей таблице перечислены эти свойства имя соответствующего свойства OLE DB в скобки.</span><span class="sxs-lookup"><span data-stu-id="0695e-221">The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0695e-222">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="0695e-222">Property Name</span></span></p></th>
<th><p><span data-ttu-id="0695e-223">Описание</span><span class="sxs-lookup"><span data-stu-id="0695e-223">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0695e-224">Запрос на основе обновления, удаления или вставки</span><span class="sxs-lookup"><span data-stu-id="0695e-224">Query Based Updates/Deletes/Inserts</span></span><br />
<span data-ttu-id="0695e-225">(KAGPROP_QUERYBASEDUPDATES)</span><span class="sxs-lookup"><span data-stu-id="0695e-225">(KAGPROP_QUERYBASEDUPDATES)</span></span></p></td>
<td><p><span data-ttu-id="0695e-226">Указывает, будет ли обновления, удаления и вставки можно выполнить с помощью SQL-запросов.</span><span class="sxs-lookup"><span data-stu-id="0695e-226">Indicates whether updates, deletions, and insertions can be performed using SQL queries.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-227">Тип параллельного ODBC</span><span class="sxs-lookup"><span data-stu-id="0695e-227">ODBC Concurrency Type</span></span><br />
<span data-ttu-id="0695e-228">(KAGPROP_CONCURRENCY)</span><span class="sxs-lookup"><span data-stu-id="0695e-228">(KAGPROP_CONCURRENCY)</span></span></p></td>
<td><p><span data-ttu-id="0695e-229">Метод, используемый для уменьшения потенциальных проблем, вызванных двух пользователей одновременно к той же информации из источника данных.</span><span class="sxs-lookup"><span data-stu-id="0695e-229">Indicates the method used to reduce potential problems caused by two users attempting to access the same data from the data source simultaneously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-230">Специальные возможности больших двоичных ОБЪЕКТОВ на последовательный курсор</span><span class="sxs-lookup"><span data-stu-id="0695e-230">BLOB accessibility on Forward-Only cursor</span></span><br />
<span data-ttu-id="0695e-231">(KAGPROP_BLOBSONFOCURSOR)</span><span class="sxs-lookup"><span data-stu-id="0695e-231">(KAGPROP_BLOBSONFOCURSOR)</span></span></p></td>
<td><p><span data-ttu-id="0695e-232">Указывает, будет ли при использовании последовательный курсор возможен больших двоичных ОБЪЕКТОВ <strong>полей</strong> .</span><span class="sxs-lookup"><span data-stu-id="0695e-232">Indicates whether BLOB <strong>Fields</strong> can be accessed when using a forward-only cursor.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-233">Включить в предложения QBU WHERE SQL_FLOAT, SQL_DOUBLE и SQL_REAL</span><span class="sxs-lookup"><span data-stu-id="0695e-233">Include SQL_FLOAT, SQL_DOUBLE, and SQL_REAL in QBU WHERE clauses</span></span><br />
<span data-ttu-id="0695e-234">(KAGPROP_INCLUDENONEXACT)</span><span class="sxs-lookup"><span data-stu-id="0695e-234">(KAGPROP_INCLUDENONEXACT)</span></span></p></td>
<td><p><span data-ttu-id="0695e-235">Указывает, будет ли значения SQL_FLOAT, SQL_DOUBLE и SQL_REAL может быть включен в предложении QBU WHERE.</span><span class="sxs-lookup"><span data-stu-id="0695e-235">Indicates whether SQL_FLOAT, SQL_DOUBLE, and SQL_REAL values can be included in a QBU WHERE clause.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-236">Положение в последней строке после вставки</span><span class="sxs-lookup"><span data-stu-id="0695e-236">Position on the last row after insert</span></span><br />
<span data-ttu-id="0695e-237">(KAGPROP_POSITIONONNEWROW)</span><span class="sxs-lookup"><span data-stu-id="0695e-237">(KAGPROP_POSITIONONNEWROW)</span></span></p></td>
<td><p><span data-ttu-id="0695e-238">Указывает, что после вставки новой записи в таблице последней строки в таблице должны быть поступают текущей строки.</span><span class="sxs-lookup"><span data-stu-id="0695e-238">Indicates that after a new record has been inserted in a table, the last row in the table will be come the current row.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-239">IRowsetChangeExtInfo</span><span class="sxs-lookup"><span data-stu-id="0695e-239">IRowsetChangeExtInfo</span></span><br />
<span data-ttu-id="0695e-240">(KAGPROP_IROWSETCHANGEEXTINFO)</span><span class="sxs-lookup"><span data-stu-id="0695e-240">(KAGPROP_IROWSETCHANGEEXTINFO)</span></span></p></td>
<td><p><span data-ttu-id="0695e-241">Указывает, будет ли интерфейс <strong>IRowsetChange</strong> поддерживает расширенные сведения.</span><span class="sxs-lookup"><span data-stu-id="0695e-241">Indicates whether the <strong>IRowsetChange</strong> interface provides extended information support.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-242">Тип курсора ODBC</span><span class="sxs-lookup"><span data-stu-id="0695e-242">ODBC Cursor Type</span></span><br />
<span data-ttu-id="0695e-243">(KAGPROP_CURSOR)</span><span class="sxs-lookup"><span data-stu-id="0695e-243">(KAGPROP_CURSOR)</span></span></p></td>
<td><p><span data-ttu-id="0695e-244">Указывает тип курсора, используемого <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="0695e-244">Indicates the type of cursor used by the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-245">Создать набор строк, который может быть упакован</span><span class="sxs-lookup"><span data-stu-id="0695e-245">Generate a Rowset that can be marshaled</span></span><br />
<span data-ttu-id="0695e-246">(KAGPROP_MARSHALLABLE)</span><span class="sxs-lookup"><span data-stu-id="0695e-246">(KAGPROP_MARSHALLABLE)</span></span></p></td>
<td><p><span data-ttu-id="0695e-247">Указывает, что драйвер ODBC создает набор записей, который может быть упакован</span><span class="sxs-lookup"><span data-stu-id="0695e-247">Indicates that the ODBC driver generates a recordset that can be marshaled</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-text"></a><span data-ttu-id="0695e-248">Текст команды</span><span class="sxs-lookup"><span data-stu-id="0695e-248">Command Text</span></span>

<span data-ttu-id="0695e-249">Как использовать объект [команды](command-object-ado.md) во многом зависит от источника данных и какой тип оператора запроса или команды будет принимать.</span><span class="sxs-lookup"><span data-stu-id="0695e-249">How you use the [Command](command-object-ado.md) object largely depends on the data source, and what type of query or command statement it will accept.</span></span>

<span data-ttu-id="0695e-250">ODBC предоставляет определенный синтаксис для вызова хранимых процедур.</span><span class="sxs-lookup"><span data-stu-id="0695e-250">ODBC provides a specific syntax for calling stored procedures.</span></span> <span data-ttu-id="0695e-251">Для свойства [CommandText](commandtext-property-ado.md) объекта **команды** *CommandText* аргумента метода **Execute** на объект [подключения](connection-object-ado.md) и *исходный* аргумент методу **Open** на [набора записей](recordset-object-ado.md) объект передает в строку с помощью следующего синтаксиса:</span><span class="sxs-lookup"><span data-stu-id="0695e-251">For the [CommandText](commandtext-property-ado.md) property of a **Command** object, the *CommandText* argument to the **Execute** method on a [Connection](connection-object-ado.md) object, or the *Source* argument to the **Open** method on a [Recordset](recordset-object-ado.md) object, passes in a string with this syntax:</span></span>

`"{ [ ? = ] call procedure [ ( ? [, ? [ ,  ]] ) ] }"`

<span data-ttu-id="0695e-252">Каждый **?**</span><span class="sxs-lookup"><span data-stu-id="0695e-252">Each **?**</span></span> <span data-ttu-id="0695e-253">содержит ссылку на объект в коллекции [параметров](parameters-collection-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="0695e-253">references an object in the [Parameters](parameters-collection-ado.md) collection.</span></span> <span data-ttu-id="0695e-254">Первый **?**</span><span class="sxs-lookup"><span data-stu-id="0695e-254">The first **?**</span></span> <span data-ttu-id="0695e-255">ссылки на **Параметры**(0), Далее **?**</span><span class="sxs-lookup"><span data-stu-id="0695e-255">references **Parameters**(0), the next **?**</span></span> <span data-ttu-id="0695e-256">Создание ссылки **Параметры**(1) и т. д.</span><span class="sxs-lookup"><span data-stu-id="0695e-256">references **Parameters**(1), and so on.</span></span>

<span data-ttu-id="0695e-257">Параметр ссылки являются необязательными и зависят от структуры хранимую процедуру.</span><span class="sxs-lookup"><span data-stu-id="0695e-257">The parameter references are optional and depend on the structure of the stored procedure.</span></span> <span data-ttu-id="0695e-258">Если вы хотите вызвать хранимую процедуру, определяющий без параметров, строка будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="0695e-258">If you want to call a stored procedure that defines no parameters, your string would look like this:</span></span>

`"{ call procedure }"`

<span data-ttu-id="0695e-259">Если у вас есть два параметра запроса, строка будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="0695e-259">If you have two query parameters, your string would look like this:</span></span>

`"{ call procedure ( ?, ? ) }"`

<span data-ttu-id="0695e-260">Если хранимая процедура возвращает значение, возвращаемое значение обрабатывается как еще один параметр.</span><span class="sxs-lookup"><span data-stu-id="0695e-260">If the stored procedure will return a value, the return value is treated as another parameter.</span></span> <span data-ttu-id="0695e-261">Если у вас нет параметров запроса, но возвращаемое значение, строка будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="0695e-261">If you have no query parameters but you do have a return value, your string would look like this:</span></span>

`"{ ? = call procedure }"`

<span data-ttu-id="0695e-262">И, наконец Если у вас есть возвращаемое значение и два параметра запроса, строка будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="0695e-262">Finally, if you have a return value and two query parameters, your string would look like this:</span></span>

`"{ ? = call procedure ( ?, ? ) }"`

## <a name="recordset-behavior"></a><span data-ttu-id="0695e-263">Поведение набора записей</span><span class="sxs-lookup"><span data-stu-id="0695e-263">Recordset Behavior</span></span>

<span data-ttu-id="0695e-264">В следующих таблицах перечислены стандартные ADO методы и свойства, доступные для объекта **набора записей** , открытых с этим поставщиком.</span><span class="sxs-lookup"><span data-stu-id="0695e-264">The following tables list the standard ADO methods and properties available on a **Recordset** object opened with this provider.</span></span>

<span data-ttu-id="0695e-265">Для получения дополнительных сведений о поведении **набора записей** для вашей конфигурации поставщика, выполните метод [поддерживает](supports-method-ado.md) и перечисления коллекции **свойств** **набора записей** для определения целесообразности поставщиком динамических свойства отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="0695e-265">For more detailed information about **Recordset** behavior for your provider configuration, run the [Supports](supports-method-ado.md) method and enumerate the **Properties** collection of the **Recordset** to determine whether provider-specific dynamic properties are present.</span></span>

<span data-ttu-id="0695e-266">Доступность стандартными свойствами ADO **набора записей** :</span><span class="sxs-lookup"><span data-stu-id="0695e-266">Availability of standard ADO **Recordset** properties:</span></span>

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
<th><p><span data-ttu-id="0695e-267">Свойство</span><span class="sxs-lookup"><span data-stu-id="0695e-267">Property</span></span></p></th>
<th><p><span data-ttu-id="0695e-268">ForwardOnly</span><span class="sxs-lookup"><span data-stu-id="0695e-268">ForwardOnly</span></span></p></th>
<th><p><span data-ttu-id="0695e-269">Динамическая группа</span><span class="sxs-lookup"><span data-stu-id="0695e-269">Dynamic</span></span></p></th>
<th><p><span data-ttu-id="0695e-270">Набор ключей</span><span class="sxs-lookup"><span data-stu-id="0695e-270">Keyset</span></span></p></th>
<th><p><span data-ttu-id="0695e-271">Статическое</span><span class="sxs-lookup"><span data-stu-id="0695e-271">Static</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0695e-272"><a href="absolutepage-property-ado.md">AbsolutePage</a></span><span class="sxs-lookup"><span data-stu-id="0695e-272"><a href="absolutepage-property-ado.md">AbsolutePage</a></span></span></p></td>
<td><p><span data-ttu-id="0695e-273">Недоступен</span><span class="sxs-lookup"><span data-stu-id="0695e-273">not available</span></span></p></td>
<td><p><span data-ttu-id="0695e-274">Недоступен</span><span class="sxs-lookup"><span data-stu-id="0695e-274">not available</span></span></p></td>
<td><p><span data-ttu-id="0695e-275">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0695e-275">read/write</span></span></p></td>
<td><p><span data-ttu-id="0695e-276">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0695e-276">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-277"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span><span class="sxs-lookup"><span data-stu-id="0695e-277"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span></span></p></td>
<td><p><span data-ttu-id="0695e-278">Недоступен</span><span class="sxs-lookup"><span data-stu-id="0695e-278">not available</span></span></p></td>
<td><p><span data-ttu-id="0695e-279">Недоступен</span><span class="sxs-lookup"><span data-stu-id="0695e-279">not available</span></span></p></td>
<td><p><span data-ttu-id="0695e-280">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0695e-280">read/write</span></span></p></td>
<td><p><span data-ttu-id="0695e-281">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0695e-281">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-282"><a href="activeconnection-property-ado.md">ActiveConnection</a></span><span class="sxs-lookup"><span data-stu-id="0695e-282"><a href="activeconnection-property-ado.md">ActiveConnection</a></span></span></p></td>
<td><p><span data-ttu-id="0695e-283">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0695e-283">read/write</span></span></p></td>
<td><p><span data-ttu-id="0695e-284">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0695e-284">read/write</span></span></p></td>
<td><p><span data-ttu-id="0695e-285">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0695e-285">read/write</span></span></p></td>
<td><p><span data-ttu-id="0695e-286">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0695e-286">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-287"><a href="bof-eof-properties-ado.md">BOF</a></span><span class="sxs-lookup"><span data-stu-id="0695e-287"><a href="bof-eof-properties-ado.md">BOF</a></span></span></p></td>
<td><p><span data-ttu-id="0695e-288">только для чтения</span><span class="sxs-lookup"><span data-stu-id="0695e-288">read-only</span></span></p></td>
<td><p><span data-ttu-id="0695e-289">только для чтения</span><span class="sxs-lookup"><span data-stu-id="0695e-289">read-only</span></span></p></td>
<td><p><span data-ttu-id="0695e-290">только для чтения</span><span class="sxs-lookup"><span data-stu-id="0695e-290">read-only</span></span></p></td>
<td><p><span data-ttu-id="0695e-291">только для чтения</span><span class="sxs-lookup"><span data-stu-id="0695e-291">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-292"><a href="bookmark-property-ado.md">Закладка</a></span><span class="sxs-lookup"><span data-stu-id="0695e-292"><a href="bookmark-property-ado.md">Bookmark</a></span></span></p></td>
<td><p><span data-ttu-id="0695e-293">Недоступен</span><span class="sxs-lookup"><span data-stu-id="0695e-293">not available</span></span></p></td>
<td><p><span data-ttu-id="0695e-294">Недоступен</span><span class="sxs-lookup"><span data-stu-id="0695e-294">not available</span></span></p></td>
<td><p><span data-ttu-id="0695e-295">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0695e-295">read/write</span></span></p></td>
<td><p><span data-ttu-id="0695e-296">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0695e-296">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-297"><a href="cachesize-property-ado.md">CacheSize</a></span><span class="sxs-lookup"><span data-stu-id="0695e-297"><a href="cachesize-property-ado.md">CacheSize</a></span></span></p></td>
<td><p><span data-ttu-id="0695e-298">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0695e-298">read/write</span></span></p></td>
<td><p><span data-ttu-id="0695e-299">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0695e-299">read/write</span></span></p></td>
<td><p><span data-ttu-id="0695e-300">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0695e-300">read/write</span></span></p></td>
<td><p><span data-ttu-id="0695e-301">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0695e-301">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-302"><a href="cursorlocation-property-ado.md">CursorLocation</a></span><span class="sxs-lookup"><span data-stu-id="0695e-302"><a href="cursorlocation-property-ado.md">CursorLocation</a></span></span></p></td>
<td><p><span data-ttu-id="0695e-303">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0695e-303">read/write</span></span></p></td>
<td><p><span data-ttu-id="0695e-304">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0695e-304">read/write</span></span></p></td>
<td><p><span data-ttu-id="0695e-305">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0695e-305">read/write</span></span></p></td>
<td><p><span data-ttu-id="0695e-306">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0695e-306">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-307"><a href="cursortype-property-ado.md">CursorType</a></span><span class="sxs-lookup"><span data-stu-id="0695e-307"><a href="cursortype-property-ado.md">CursorType</a></span></span></p></td>
<td><p><span data-ttu-id="0695e-308">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0695e-308">read/write</span></span></p></td>
<td><p><span data-ttu-id="0695e-309">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0695e-309">read/write</span></span></p></td>
<td><p><span data-ttu-id="0695e-310">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0695e-310">read/write</span></span></p></td>
<td><p><span data-ttu-id="0695e-311">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0695e-311">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-312"><a href="editmode-property-ado.md">EditMode</a></span><span class="sxs-lookup"><span data-stu-id="0695e-312"><a href="editmode-property-ado.md">EditMode</a></span></span></p></td>
<td><p><span data-ttu-id="0695e-313">только для чтения</span><span class="sxs-lookup"><span data-stu-id="0695e-313">read-only</span></span></p></td>
<td><p><span data-ttu-id="0695e-314">только для чтения</span><span class="sxs-lookup"><span data-stu-id="0695e-314">read-only</span></span></p></td>
<td><p><span data-ttu-id="0695e-315">только для чтения</span><span class="sxs-lookup"><span data-stu-id="0695e-315">read-only</span></span></p></td>
<td><p><span data-ttu-id="0695e-316">только для чтения</span><span class="sxs-lookup"><span data-stu-id="0695e-316">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-317"><a href="filter-property-ado.md">Filter</a></span><span class="sxs-lookup"><span data-stu-id="0695e-317"><a href="filter-property-ado.md">Filter</a></span></span></p></td>
<td><p><span data-ttu-id="0695e-318">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0695e-318">read/write</span></span></p></td>
<td><p><span data-ttu-id="0695e-319">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0695e-319">read/write</span></span></p></td>
<td><p><span data-ttu-id="0695e-320">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0695e-320">read/write</span></span></p></td>
<td><p><span data-ttu-id="0695e-321">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0695e-321">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-322"><a href="locktype-property-ado.md">LockType для</a></span><span class="sxs-lookup"><span data-stu-id="0695e-322"><a href="locktype-property-ado.md">LockType</a></span></span></p></td>
<td><p><span data-ttu-id="0695e-323">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0695e-323">read/write</span></span></p></td>
<td><p><span data-ttu-id="0695e-324">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0695e-324">read/write</span></span></p></td>
<td><p><span data-ttu-id="0695e-325">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0695e-325">read/write</span></span></p></td>
<td><p><span data-ttu-id="0695e-326">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0695e-326">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-327"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span><span class="sxs-lookup"><span data-stu-id="0695e-327"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span></span></p></td>
<td><p><span data-ttu-id="0695e-328">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0695e-328">read/write</span></span></p></td>
<td><p><span data-ttu-id="0695e-329">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0695e-329">read/write</span></span></p></td>
<td><p><span data-ttu-id="0695e-330">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0695e-330">read/write</span></span></p></td>
<td><p><span data-ttu-id="0695e-331">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0695e-331">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-332"><a href="maxrecords-property-ado.md">MaxRecords</a></span><span class="sxs-lookup"><span data-stu-id="0695e-332"><a href="maxrecords-property-ado.md">MaxRecords</a></span></span></p></td>
<td><p><span data-ttu-id="0695e-333">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0695e-333">read/write</span></span></p></td>
<td><p><span data-ttu-id="0695e-334">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0695e-334">read/write</span></span></p></td>
<td><p><span data-ttu-id="0695e-335">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0695e-335">read/write</span></span></p></td>
<td><p><span data-ttu-id="0695e-336">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0695e-336">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-337"><a href="pagecount-property-ado.md">PageCount</a></span><span class="sxs-lookup"><span data-stu-id="0695e-337"><a href="pagecount-property-ado.md">PageCount</a></span></span></p></td>
<td><p><span data-ttu-id="0695e-338">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0695e-338">read/write</span></span></p></td>
<td><p><span data-ttu-id="0695e-339">Недоступен</span><span class="sxs-lookup"><span data-stu-id="0695e-339">not available</span></span></p></td>
<td><p><span data-ttu-id="0695e-340">только для чтения</span><span class="sxs-lookup"><span data-stu-id="0695e-340">read-only</span></span></p></td>
<td><p><span data-ttu-id="0695e-341">только для чтения</span><span class="sxs-lookup"><span data-stu-id="0695e-341">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-342"><a href="pagesize-property-ado.md">PageSize</a></span><span class="sxs-lookup"><span data-stu-id="0695e-342"><a href="pagesize-property-ado.md">PageSize</a></span></span></p></td>
<td><p><span data-ttu-id="0695e-343">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0695e-343">read/write</span></span></p></td>
<td><p><span data-ttu-id="0695e-344">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0695e-344">read/write</span></span></p></td>
<td><p><span data-ttu-id="0695e-345">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0695e-345">read/write</span></span></p></td>
<td><p><span data-ttu-id="0695e-346">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0695e-346">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-347"><a href="recordcount-property-ado.md">RecordCount</a></span><span class="sxs-lookup"><span data-stu-id="0695e-347"><a href="recordcount-property-ado.md">RecordCount</a></span></span></p></td>
<td><p><span data-ttu-id="0695e-348">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0695e-348">read/write</span></span></p></td>
<td><p><span data-ttu-id="0695e-349">Недоступен</span><span class="sxs-lookup"><span data-stu-id="0695e-349">not available</span></span></p></td>
<td><p><span data-ttu-id="0695e-350">только для чтения</span><span class="sxs-lookup"><span data-stu-id="0695e-350">read-only</span></span></p></td>
<td><p><span data-ttu-id="0695e-351">только для чтения</span><span class="sxs-lookup"><span data-stu-id="0695e-351">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-352"><a href="source-property-ado-recordset.md">Source</a></span><span class="sxs-lookup"><span data-stu-id="0695e-352"><a href="source-property-ado-recordset.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="0695e-353">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0695e-353">read/write</span></span></p></td>
<td><p><span data-ttu-id="0695e-354">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0695e-354">read/write</span></span></p></td>
<td><p><span data-ttu-id="0695e-355">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0695e-355">read/write</span></span></p></td>
<td><p><span data-ttu-id="0695e-356">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0695e-356">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-357"><a href="state-property-ado.md">State</a></span><span class="sxs-lookup"><span data-stu-id="0695e-357"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="0695e-358">только для чтения</span><span class="sxs-lookup"><span data-stu-id="0695e-358">read-only</span></span></p></td>
<td><p><span data-ttu-id="0695e-359">только для чтения</span><span class="sxs-lookup"><span data-stu-id="0695e-359">read-only</span></span></p></td>
<td><p><span data-ttu-id="0695e-360">только для чтения</span><span class="sxs-lookup"><span data-stu-id="0695e-360">read-only</span></span></p></td>
<td><p><span data-ttu-id="0695e-361">только для чтения</span><span class="sxs-lookup"><span data-stu-id="0695e-361">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-362"><a href="status-property-ado-recordset.md">Состояние</a></span><span class="sxs-lookup"><span data-stu-id="0695e-362"><a href="status-property-ado-recordset.md">Status</a></span></span></p></td>
<td><p><span data-ttu-id="0695e-363">только для чтения</span><span class="sxs-lookup"><span data-stu-id="0695e-363">read-only</span></span></p></td>
<td><p><span data-ttu-id="0695e-364">только для чтения</span><span class="sxs-lookup"><span data-stu-id="0695e-364">read-only</span></span></p></td>
<td><p><span data-ttu-id="0695e-365">только для чтения</span><span class="sxs-lookup"><span data-stu-id="0695e-365">read-only</span></span></p></td>
<td><p><span data-ttu-id="0695e-366">только для чтения</span><span class="sxs-lookup"><span data-stu-id="0695e-366">read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0695e-367">Свойства [AbsolutePosition](absoluteposition-property-ado.md) и [AbsolutePage](absolutepage-property-ado.md) доступны только для записи при использовании ADO с версии 1.0 поставщик Microsoft OLE DB для ODBC.</span><span class="sxs-lookup"><span data-stu-id="0695e-367">The [AbsolutePosition](absoluteposition-property-ado.md) and [AbsolutePage](absolutepage-property-ado.md) properties are write-only when ADO is used with version 1.0 of the Microsoft OLE DB Provider for ODBC.</span></span>

<span data-ttu-id="0695e-368">Доступность стандартных способов ADO **набора записей** :</span><span class="sxs-lookup"><span data-stu-id="0695e-368">Availability of standard ADO **Recordset** methods:</span></span>

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
<th><p><span data-ttu-id="0695e-369">Метод</span><span class="sxs-lookup"><span data-stu-id="0695e-369">Method</span></span></p></th>
<th><p><span data-ttu-id="0695e-370">ForwardOnly</span><span class="sxs-lookup"><span data-stu-id="0695e-370">ForwardOnly</span></span></p></th>
<th><p><span data-ttu-id="0695e-371">Динамическая группа</span><span class="sxs-lookup"><span data-stu-id="0695e-371">Dynamic</span></span></p></th>
<th><p><span data-ttu-id="0695e-372">Набор ключей</span><span class="sxs-lookup"><span data-stu-id="0695e-372">Keyset</span></span></p></th>
<th><p><span data-ttu-id="0695e-373">Статическое</span><span class="sxs-lookup"><span data-stu-id="0695e-373">Static</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0695e-374"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="0695e-374"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="0695e-375">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-375">Yes</span></span></p></td>
<td><p><span data-ttu-id="0695e-376">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-376">Yes</span></span></p></td>
<td><p><span data-ttu-id="0695e-377">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-377">Yes</span></span></p></td>
<td><p><span data-ttu-id="0695e-378">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-378">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-379"><a href="cancel-method-ado.md">Отмена</a></span><span class="sxs-lookup"><span data-stu-id="0695e-379"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="0695e-380">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-380">Yes</span></span></p></td>
<td><p><span data-ttu-id="0695e-381">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-381">Yes</span></span></p></td>
<td><p><span data-ttu-id="0695e-382">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-382">Yes</span></span></p></td>
<td><p><span data-ttu-id="0695e-383">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-383">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-384"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="0695e-384"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="0695e-385">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-385">Yes</span></span></p></td>
<td><p><span data-ttu-id="0695e-386">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-386">Yes</span></span></p></td>
<td><p><span data-ttu-id="0695e-387">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-387">Yes</span></span></p></td>
<td><p><span data-ttu-id="0695e-388">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-388">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-389"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="0695e-389"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="0695e-390">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-390">Yes</span></span></p></td>
<td><p><span data-ttu-id="0695e-391">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-391">Yes</span></span></p></td>
<td><p><span data-ttu-id="0695e-392">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-392">Yes</span></span></p></td>
<td><p><span data-ttu-id="0695e-393">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-393">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-394"><a href="clone-method-ado.md">Копия</a></span><span class="sxs-lookup"><span data-stu-id="0695e-394"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="0695e-395">Нет</span><span class="sxs-lookup"><span data-stu-id="0695e-395">No</span></span></p></td>
<td><p><span data-ttu-id="0695e-396">Нет</span><span class="sxs-lookup"><span data-stu-id="0695e-396">No</span></span></p></td>
<td><p><span data-ttu-id="0695e-397">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-397">Yes</span></span></p></td>
<td><p><span data-ttu-id="0695e-398">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-398">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-399"><a href="close-method-ado.md">Закрыть</a></span><span class="sxs-lookup"><span data-stu-id="0695e-399"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="0695e-400">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-400">Yes</span></span></p></td>
<td><p><span data-ttu-id="0695e-401">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-401">Yes</span></span></p></td>
<td><p><span data-ttu-id="0695e-402">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-402">Yes</span></span></p></td>
<td><p><span data-ttu-id="0695e-403">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-403">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-404"><a href="delete-method-ado-recordset.md">Delete</a></span><span class="sxs-lookup"><span data-stu-id="0695e-404"><a href="delete-method-ado-recordset.md">Delete</a></span></span></p></td>
<td><p><span data-ttu-id="0695e-405">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-405">Yes</span></span></p></td>
<td><p><span data-ttu-id="0695e-406">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-406">Yes</span></span></p></td>
<td><p><span data-ttu-id="0695e-407">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-407">Yes</span></span></p></td>
<td><p><span data-ttu-id="0695e-408">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-408">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-409"><a href="getrows-method-ado.md">Получение строк</a></span><span class="sxs-lookup"><span data-stu-id="0695e-409"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="0695e-410">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-410">Yes</span></span></p></td>
<td><p><span data-ttu-id="0695e-411">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-411">Yes</span></span></p></td>
<td><p><span data-ttu-id="0695e-412">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-412">Yes</span></span></p></td>
<td><p><span data-ttu-id="0695e-413">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-413">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-414"><a href="move-method-ado.md">Перемещение</a></span><span class="sxs-lookup"><span data-stu-id="0695e-414"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="0695e-415">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-415">Yes</span></span></p></td>
<td><p><span data-ttu-id="0695e-416">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-416">Yes</span></span></p></td>
<td><p><span data-ttu-id="0695e-417">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-417">Yes</span></span></p></td>
<td><p><span data-ttu-id="0695e-418">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-418">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-419"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span><span class="sxs-lookup"><span data-stu-id="0695e-419"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span></span></p></td>
<td><p><span data-ttu-id="0695e-420">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-420">Yes</span></span></p></td>
<td><p><span data-ttu-id="0695e-421">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-421">Yes</span></span></p></td>
<td><p><span data-ttu-id="0695e-422">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-422">Yes</span></span></p></td>
<td><p><span data-ttu-id="0695e-423">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-423">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-424"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span><span class="sxs-lookup"><span data-stu-id="0695e-424"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span></span></p></td>
<td><p><span data-ttu-id="0695e-425">Нет</span><span class="sxs-lookup"><span data-stu-id="0695e-425">No</span></span></p></td>
<td><p><span data-ttu-id="0695e-426">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-426">Yes</span></span></p></td>
<td><p><span data-ttu-id="0695e-427">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-427">Yes</span></span></p></td>
<td><p><span data-ttu-id="0695e-428">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-428">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-429"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span><span class="sxs-lookup"><span data-stu-id="0695e-429"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span></span></p></td>
<td><p><span data-ttu-id="0695e-430">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-430">Yes</span></span></p></td>
<td><p><span data-ttu-id="0695e-431">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-431">Yes</span></span></p></td>
<td><p><span data-ttu-id="0695e-432">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-432">Yes</span></span></p></td>
<td><p><span data-ttu-id="0695e-433">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-433">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-434"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span><span class="sxs-lookup"><span data-stu-id="0695e-434"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span></span></p></td>
<td><p><span data-ttu-id="0695e-435">Нет</span><span class="sxs-lookup"><span data-stu-id="0695e-435">No</span></span></p></td>
<td><p><span data-ttu-id="0695e-436">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-436">Yes</span></span></p></td>
<td><p><span data-ttu-id="0695e-437">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-437">Yes</span></span></p></td>
<td><p><span data-ttu-id="0695e-438">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-438">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-439"><a href="nextrecordset-method-ado.md">NextRecordset</a>\*</span><span class="sxs-lookup"><span data-stu-id="0695e-439"><a href="nextrecordset-method-ado.md">NextRecordset</a>\*</span></span></p></td>
<td><p><span data-ttu-id="0695e-440">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-440">Yes</span></span></p></td>
<td><p><span data-ttu-id="0695e-441">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-441">Yes</span></span></p></td>
<td><p><span data-ttu-id="0695e-442">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-442">Yes</span></span></p></td>
<td><p><span data-ttu-id="0695e-443">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-443">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-444"><a href="open-method-ado-recordset.md">Открытие</a></span><span class="sxs-lookup"><span data-stu-id="0695e-444"><a href="open-method-ado-recordset.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="0695e-445">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-445">Yes</span></span></p></td>
<td><p><span data-ttu-id="0695e-446">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-446">Yes</span></span></p></td>
<td><p><span data-ttu-id="0695e-447">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-447">Yes</span></span></p></td>
<td><p><span data-ttu-id="0695e-448">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-448">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-449"><a href="requery-method-ado.md">Обновление</a></span><span class="sxs-lookup"><span data-stu-id="0695e-449"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="0695e-450">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-450">Yes</span></span></p></td>
<td><p><span data-ttu-id="0695e-451">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-451">Yes</span></span></p></td>
<td><p><span data-ttu-id="0695e-452">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-452">Yes</span></span></p></td>
<td><p><span data-ttu-id="0695e-453">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-453">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-454"><a href="resync-method-ado.md">Выполнить повторную синхронизацию</a></span><span class="sxs-lookup"><span data-stu-id="0695e-454"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="0695e-455">Нет</span><span class="sxs-lookup"><span data-stu-id="0695e-455">No</span></span></p></td>
<td><p><span data-ttu-id="0695e-456">Нет</span><span class="sxs-lookup"><span data-stu-id="0695e-456">No</span></span></p></td>
<td><p><span data-ttu-id="0695e-457">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-457">Yes</span></span></p></td>
<td><p><span data-ttu-id="0695e-458">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-458">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-459"><a href="supports-method-ado.md">Поддерживает</a></span><span class="sxs-lookup"><span data-stu-id="0695e-459"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="0695e-460">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-460">Yes</span></span></p></td>
<td><p><span data-ttu-id="0695e-461">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-461">Yes</span></span></p></td>
<td><p><span data-ttu-id="0695e-462">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-462">Yes</span></span></p></td>
<td><p><span data-ttu-id="0695e-463">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-463">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-464"><a href="update-method-ado.md">обновление</a>.</span><span class="sxs-lookup"><span data-stu-id="0695e-464"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="0695e-465">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-465">Yes</span></span></p></td>
<td><p><span data-ttu-id="0695e-466">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-466">Yes</span></span></p></td>
<td><p><span data-ttu-id="0695e-467">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-467">Yes</span></span></p></td>
<td><p><span data-ttu-id="0695e-468">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-468">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-469"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="0695e-469"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="0695e-470">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-470">Yes</span></span></p></td>
<td><p><span data-ttu-id="0695e-471">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-471">Yes</span></span></p></td>
<td><p><span data-ttu-id="0695e-472">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-472">Yes</span></span></p></td>
<td><p><span data-ttu-id="0695e-473">Да</span><span class="sxs-lookup"><span data-stu-id="0695e-473">Yes</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0695e-474">\*Не поддерживается для баз данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="0695e-474">\*Not supported for Microsoft Access databases.</span></span>

## <a name="dynamic-properties"></a><span data-ttu-id="0695e-475">Динамические свойства</span><span class="sxs-lookup"><span data-stu-id="0695e-475">Dynamic Properties</span></span>

<span data-ttu-id="0695e-476">Поставщик Microsoft OLE DB для ODBC вставляет несколько динамических свойств в коллекцию **свойств** объектов неоткрытый [подключения](connection-object-ado.md), [записей](recordset-object-ado.md)и [команды](command-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="0695e-476">The Microsoft OLE DB Provider for ODBC inserts several dynamic properties into the **Properties** collection of the unopened [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md), and [Command](command-object-ado.md) objects.</span></span>

<span data-ttu-id="0695e-477">В таблицах ниже — это cross-index имен ADO и OLE DB для каждого динамического свойства.</span><span class="sxs-lookup"><span data-stu-id="0695e-477">The tables below are a cross-index of the ADO and OLE DB names for each dynamic property.</span></span> <span data-ttu-id="0695e-478">Справочник программиста OLE DB указано имя свойства ADO по слову «Описание».</span><span class="sxs-lookup"><span data-stu-id="0695e-478">The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description."</span></span> <span data-ttu-id="0695e-479">Дополнительные сведения об этих свойств можно найти в Справочник программиста OLE DB.</span><span class="sxs-lookup"><span data-stu-id="0695e-479">You can find more information about these properties in the OLE DB Programmer's Reference.</span></span> <span data-ttu-id="0695e-480">Поиск имени свойства OLE DB в индексе или просмотреть приложение C: OLE DB свойства.</span><span class="sxs-lookup"><span data-stu-id="0695e-480">Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span></span>

## <a name="connection-dynamic-properties"></a><span data-ttu-id="0695e-481">Динамические свойства подключения</span><span class="sxs-lookup"><span data-stu-id="0695e-481">Connection Dynamic Properties</span></span>

<span data-ttu-id="0695e-482">Коллекция **Properties** объект **подключения** добавляются следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="0695e-482">The following properties are added to the **Connection** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0695e-483">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="0695e-483">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="0695e-484">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="0695e-484">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0695e-485">Активных сеансов</span><span class="sxs-lookup"><span data-stu-id="0695e-485">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="0695e-486">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="0695e-486">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-487">Прерывание Asynchable</span><span class="sxs-lookup"><span data-stu-id="0695e-487">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="0695e-488">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="0695e-488">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-489">Зафиксировать Asynchable</span><span class="sxs-lookup"><span data-stu-id="0695e-489">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="0695e-490">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="0695e-490">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-491">Уровни изоляции автоматической фиксации</span><span class="sxs-lookup"><span data-stu-id="0695e-491">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="0695e-492">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="0695e-492">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-493">Расположение каталога</span><span class="sxs-lookup"><span data-stu-id="0695e-493">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="0695e-494">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="0695e-494">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-495">Каталог терминов</span><span class="sxs-lookup"><span data-stu-id="0695e-495">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="0695e-496">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="0695e-496">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-497">Определение столбца</span><span class="sxs-lookup"><span data-stu-id="0695e-497">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="0695e-498">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="0695e-498">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-499">Время ожидания подключения</span><span class="sxs-lookup"><span data-stu-id="0695e-499">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="0695e-500">DBPROP_INIT_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="0695e-500">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-501">Текущий каталог</span><span class="sxs-lookup"><span data-stu-id="0695e-501">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="0695e-502">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="0695e-502">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-503">Источник данных</span><span class="sxs-lookup"><span data-stu-id="0695e-503">Data Source</span></span></p></td>
<td><p><span data-ttu-id="0695e-504">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="0695e-504">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-505">Имя источника данных</span><span class="sxs-lookup"><span data-stu-id="0695e-505">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="0695e-506">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="0695e-506">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-507">Модель потоков объекта источника данных</span><span class="sxs-lookup"><span data-stu-id="0695e-507">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="0695e-508">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="0695e-508">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-509">Имя СУБД</span><span class="sxs-lookup"><span data-stu-id="0695e-509">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="0695e-510">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="0695e-510">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-511">Версия СУБД</span><span class="sxs-lookup"><span data-stu-id="0695e-511">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="0695e-512">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="0695e-512">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-513">Расширенные свойства</span><span class="sxs-lookup"><span data-stu-id="0695e-513">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="0695e-514">DBPROP_INIT_PROVIDERSTRING</span><span class="sxs-lookup"><span data-stu-id="0695e-514">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-515">ГРУППИРОВКА по поддержке</span><span class="sxs-lookup"><span data-stu-id="0695e-515">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="0695e-516">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="0695e-516">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-517">Поддержка разнородных таблиц</span><span class="sxs-lookup"><span data-stu-id="0695e-517">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="0695e-518">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="0695e-518">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-519">Идентификатор регистра</span><span class="sxs-lookup"><span data-stu-id="0695e-519">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="0695e-520">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="0695e-520">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-521">Исходный каталог</span><span class="sxs-lookup"><span data-stu-id="0695e-521">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="0695e-522">DBPROP_INIT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="0695e-522">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-523">Уровни изоляции</span><span class="sxs-lookup"><span data-stu-id="0695e-523">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="0695e-524">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="0695e-524">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-525">Хранение изоляции</span><span class="sxs-lookup"><span data-stu-id="0695e-525">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="0695e-526">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="0695e-526">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-527">Идентификатор языка</span><span class="sxs-lookup"><span data-stu-id="0695e-527">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="0695e-528">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="0695e-528">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-529">Location</span><span class="sxs-lookup"><span data-stu-id="0695e-529">Location</span></span></p></td>
<td><p><span data-ttu-id="0695e-530">DBPROP_INIT_LOCATION</span><span class="sxs-lookup"><span data-stu-id="0695e-530">DBPROP_INIT_LOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-531">Максимальный размер индекса</span><span class="sxs-lookup"><span data-stu-id="0695e-531">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="0695e-532">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="0695e-532">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-533">Максимальный размер строки</span><span class="sxs-lookup"><span data-stu-id="0695e-533">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="0695e-534">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="0695e-534">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-535">Максимальный размер строки включает в себя больших двоичных ОБЪЕКТОВ</span><span class="sxs-lookup"><span data-stu-id="0695e-535">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="0695e-536">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="0695e-536">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-537">Максимальная таблиц в Выбор</span><span class="sxs-lookup"><span data-stu-id="0695e-537">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="0695e-538">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="0695e-538">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-539">Mode</span><span class="sxs-lookup"><span data-stu-id="0695e-539">Mode</span></span></p></td>
<td><p><span data-ttu-id="0695e-540">DBPROP_INIT_MODE</span><span class="sxs-lookup"><span data-stu-id="0695e-540">DBPROP_INIT_MODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-541">Несколько наборов параметров</span><span class="sxs-lookup"><span data-stu-id="0695e-541">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="0695e-542">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="0695e-542">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-543">Несколько результатов</span><span class="sxs-lookup"><span data-stu-id="0695e-543">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="0695e-544">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="0695e-544">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-545">Несколько объектов хранения</span><span class="sxs-lookup"><span data-stu-id="0695e-545">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="0695e-546">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="0695e-546">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-547">Обновление нескольких таблицы</span><span class="sxs-lookup"><span data-stu-id="0695e-547">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="0695e-548">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="0695e-548">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-549">Порядок сортировки значений NULL</span><span class="sxs-lookup"><span data-stu-id="0695e-549">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="0695e-550">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="0695e-550">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-551">Поведение NULL объединения</span><span class="sxs-lookup"><span data-stu-id="0695e-551">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="0695e-552">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="0695e-552">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-553">Службы OLE DB</span><span class="sxs-lookup"><span data-stu-id="0695e-553">OLE DB Services</span></span></p></td>
<td><p><span data-ttu-id="0695e-554">DBPROP_INIT_OLEDBSERVICES, УСТАНОВИТЬ</span><span class="sxs-lookup"><span data-stu-id="0695e-554">DBPROP_INIT_OLEDBSERVICES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-555">Версия OLE DB</span><span class="sxs-lookup"><span data-stu-id="0695e-555">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="0695e-556">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="0695e-556">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-557">Поддержка OLE-объектов</span><span class="sxs-lookup"><span data-stu-id="0695e-557">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="0695e-558">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="0695e-558">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-559">Поддержка открытых наборов строк</span><span class="sxs-lookup"><span data-stu-id="0695e-559">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="0695e-560">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="0695e-560">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-561">ORDER BY столбцы в списке Select</span><span class="sxs-lookup"><span data-stu-id="0695e-561">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="0695e-562">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="0695e-562">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-563">Выходной параметр доступности</span><span class="sxs-lookup"><span data-stu-id="0695e-563">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="0695e-564">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="0695e-564">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-565">Пароль</span><span class="sxs-lookup"><span data-stu-id="0695e-565">Password</span></span></p></td>
<td><p><span data-ttu-id="0695e-566">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="0695e-566">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-567">Передайте с указанные методы</span><span class="sxs-lookup"><span data-stu-id="0695e-567">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="0695e-568">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="0695e-568">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-569">Сохранять сведения о безопасности</span><span class="sxs-lookup"><span data-stu-id="0695e-569">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="0695e-570">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span><span class="sxs-lookup"><span data-stu-id="0695e-570">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-571">Тип сохраняемого идентификатора</span><span class="sxs-lookup"><span data-stu-id="0695e-571">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="0695e-572">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="0695e-572">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-573">Подготовка поведение аварийное завершение</span><span class="sxs-lookup"><span data-stu-id="0695e-573">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="0695e-574">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="0695e-574">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-575">Подготовка поведение выделения</span><span class="sxs-lookup"><span data-stu-id="0695e-575">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="0695e-576">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="0695e-576">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-577">Процедура терминов</span><span class="sxs-lookup"><span data-stu-id="0695e-577">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="0695e-578">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="0695e-578">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-579">Запрос</span><span class="sxs-lookup"><span data-stu-id="0695e-579">Prompt</span></span></p></td>
<td><p><span data-ttu-id="0695e-580">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="0695e-580">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-581">Понятное имя поставщика</span><span class="sxs-lookup"><span data-stu-id="0695e-581">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="0695e-582">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="0695e-582">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-583">Имя поставщика</span><span class="sxs-lookup"><span data-stu-id="0695e-583">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="0695e-584">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="0695e-584">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-585">Версия поставщика</span><span class="sxs-lookup"><span data-stu-id="0695e-585">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="0695e-586">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="0695e-586">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-587">Источник данных только для чтения</span><span class="sxs-lookup"><span data-stu-id="0695e-587">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="0695e-588">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="0695e-588">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-589">Преобразование строк на команду</span><span class="sxs-lookup"><span data-stu-id="0695e-589">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="0695e-590">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="0695e-590">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-591">Схема терминов</span><span class="sxs-lookup"><span data-stu-id="0695e-591">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="0695e-592">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="0695e-592">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-593">Об использовании схемы</span><span class="sxs-lookup"><span data-stu-id="0695e-593">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="0695e-594">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="0695e-594">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-595">Поддержка SQL</span><span class="sxs-lookup"><span data-stu-id="0695e-595">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="0695e-596">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="0695e-596">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-597">Структурированное хранилище</span><span class="sxs-lookup"><span data-stu-id="0695e-597">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="0695e-598">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="0695e-598">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-599">Поддержка вложенного запроса</span><span class="sxs-lookup"><span data-stu-id="0695e-599">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="0695e-600">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="0695e-600">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-601">В таблице терминов</span><span class="sxs-lookup"><span data-stu-id="0695e-601">Table Term</span></span></p></td>
<td><p><span data-ttu-id="0695e-602">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="0695e-602">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-603">Транзакций DDL</span><span class="sxs-lookup"><span data-stu-id="0695e-603">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="0695e-604">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="0695e-604">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-605">Идентификатор пользователя</span><span class="sxs-lookup"><span data-stu-id="0695e-605">User ID</span></span></p></td>
<td><p><span data-ttu-id="0695e-606">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="0695e-606">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-607">Имя пользователя</span><span class="sxs-lookup"><span data-stu-id="0695e-607">User Name</span></span></p></td>
<td><p><span data-ttu-id="0695e-608">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="0695e-608">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-609">Дескриптор окна</span><span class="sxs-lookup"><span data-stu-id="0695e-609">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="0695e-610">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="0695e-610">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a><span data-ttu-id="0695e-611">Свойства динамической набора записей</span><span class="sxs-lookup"><span data-stu-id="0695e-611">Recordset Dynamic Properties</span></span>

<span data-ttu-id="0695e-612">Следующие свойства добавляются в коллекцию **свойств** объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="0695e-612">The following properties are added to the **Recordset** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0695e-613">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="0695e-613">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="0695e-614">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="0695e-614">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0695e-615">Порядок доступа</span><span class="sxs-lookup"><span data-stu-id="0695e-615">Access Order</span></span></p></td>
<td><p><span data-ttu-id="0695e-616">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="0695e-616">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-617">Блокировка объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="0695e-617">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="0695e-618">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="0695e-618">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-619">Тип закладки</span><span class="sxs-lookup"><span data-stu-id="0695e-619">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="0695e-620">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="0695e-620">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-621">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="0695e-621">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="0695e-622">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="0695e-622">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-623">Изменение вставленных строк</span><span class="sxs-lookup"><span data-stu-id="0695e-623">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="0695e-624">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="0695e-624">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-625">Права доступа столбца</span><span class="sxs-lookup"><span data-stu-id="0695e-625">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="0695e-626">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="0695e-626">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-627">Столбец набор уведомлений</span><span class="sxs-lookup"><span data-stu-id="0695e-627">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="0695e-628">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="0695e-628">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-629">Отложенное обновление объекта хранения</span><span class="sxs-lookup"><span data-stu-id="0695e-629">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="0695e-630">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="0695e-630">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-631">Выборку</span><span class="sxs-lookup"><span data-stu-id="0695e-631">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="0695e-632">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="0695e-632">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-633">Хранение строк</span><span class="sxs-lookup"><span data-stu-id="0695e-633">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="0695e-634">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="0695e-634">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-635">IAccessor</span><span class="sxs-lookup"><span data-stu-id="0695e-635">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="0695e-636">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="0695e-636">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-637">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="0695e-637">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="0695e-638">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="0695e-638">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-639">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="0695e-639">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="0695e-640">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="0695e-640">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-641">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="0695e-641">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="0695e-642">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="0695e-642">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-643">IConvertType</span><span class="sxs-lookup"><span data-stu-id="0695e-643">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="0695e-644">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="0695e-644">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-645">Немобильные строки</span><span class="sxs-lookup"><span data-stu-id="0695e-645">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="0695e-646">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="0695e-646">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-647">IRowset</span><span class="sxs-lookup"><span data-stu-id="0695e-647">IRowset</span></span></p></td>
<td><p><span data-ttu-id="0695e-648">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="0695e-648">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-649">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="0695e-649">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="0695e-650">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="0695e-650">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-651">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="0695e-651">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="0695e-652">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="0695e-652">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-653">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="0695e-653">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="0695e-654">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="0695e-654">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-655">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="0695e-655">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="0695e-656">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="0695e-656">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-657">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="0695e-657">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-658">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="0695e-658">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="0695e-659">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="0695e-659">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-660">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="0695e-660">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="0695e-661">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="0695e-661">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-662">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="0695e-662">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="0695e-663">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="0695e-663">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-664">Литерал закладки</span><span class="sxs-lookup"><span data-stu-id="0695e-664">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="0695e-665">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="0695e-665">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-666">Удостоверение литерала строки</span><span class="sxs-lookup"><span data-stu-id="0695e-666">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="0695e-667">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="0695e-667">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-668">Максимальное число открытых строк</span><span class="sxs-lookup"><span data-stu-id="0695e-668">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="0695e-669">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="0695e-669">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-670">Максимум ожидающие строк</span><span class="sxs-lookup"><span data-stu-id="0695e-670">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="0695e-671">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="0695e-671">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-672">Максимальное число строк</span><span class="sxs-lookup"><span data-stu-id="0695e-672">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="0695e-673">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="0695e-673">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-674">Степень детализации уведомлений</span><span class="sxs-lookup"><span data-stu-id="0695e-674">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="0695e-675">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="0695e-675">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-676">Этапы уведомлений</span><span class="sxs-lookup"><span data-stu-id="0695e-676">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="0695e-677">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="0695e-677">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-678">Объекты в транзакции</span><span class="sxs-lookup"><span data-stu-id="0695e-678">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="0695e-679">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="0695e-679">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-680">Видны собственные изменения</span><span class="sxs-lookup"><span data-stu-id="0695e-680">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="0695e-681">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="0695e-681">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-682">Видны собственные операции вставки</span><span class="sxs-lookup"><span data-stu-id="0695e-682">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="0695e-683">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="0695e-683">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-684">Сохранять при аварийном завершении</span><span class="sxs-lookup"><span data-stu-id="0695e-684">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="0695e-685">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="0695e-685">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-686">Сохранять при фиксации</span><span class="sxs-lookup"><span data-stu-id="0695e-686">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="0695e-687">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="0695e-687">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-688">Быстрый перезапуск</span><span class="sxs-lookup"><span data-stu-id="0695e-688">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="0695e-689">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="0695e-689">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-690">Повторные события</span><span class="sxs-lookup"><span data-stu-id="0695e-690">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="0695e-691">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="0695e-691">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-692">Удаление удаленных строк</span><span class="sxs-lookup"><span data-stu-id="0695e-692">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="0695e-693">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="0695e-693">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-694">Сообщить о нескольких изменений</span><span class="sxs-lookup"><span data-stu-id="0695e-694">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="0695e-695">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="0695e-695">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-696">Вернуть ожидающие вставки</span><span class="sxs-lookup"><span data-stu-id="0695e-696">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="0695e-697">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="0695e-697">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-698">Удалить строку уведомлений</span><span class="sxs-lookup"><span data-stu-id="0695e-698">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="0695e-699">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="0695e-699">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-700">Строка первого уведомления об изменении</span><span class="sxs-lookup"><span data-stu-id="0695e-700">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="0695e-701">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="0695e-701">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-702">Строка вставки уведомлений</span><span class="sxs-lookup"><span data-stu-id="0695e-702">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="0695e-703">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="0695e-703">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-704">Привилегии строки</span><span class="sxs-lookup"><span data-stu-id="0695e-704">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="0695e-705">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="0695e-705">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-706">Уведомления о повторной синхронизации строки</span><span class="sxs-lookup"><span data-stu-id="0695e-706">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="0695e-707">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="0695e-707">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-708">Строка, потоковой модели</span><span class="sxs-lookup"><span data-stu-id="0695e-708">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="0695e-709">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="0695e-709">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-710">Уведомление об изменении отмены строки</span><span class="sxs-lookup"><span data-stu-id="0695e-710">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="0695e-711">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="0695e-711">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-712">Строка отмены Delete уведомлений</span><span class="sxs-lookup"><span data-stu-id="0695e-712">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="0695e-713">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="0695e-713">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-714">Вставка отмены строки уведомлений</span><span class="sxs-lookup"><span data-stu-id="0695e-714">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="0695e-715">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="0695e-715">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-716">Уведомление об обновлении строки</span><span class="sxs-lookup"><span data-stu-id="0695e-716">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="0695e-717">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="0695e-717">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-718">Уведомление об изменении положения строк выборки</span><span class="sxs-lookup"><span data-stu-id="0695e-718">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="0695e-719">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="0695e-719">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-720">Уведомление о выпуске набора строк</span><span class="sxs-lookup"><span data-stu-id="0695e-720">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="0695e-721">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="0695e-721">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-722">Прокрутка назад</span><span class="sxs-lookup"><span data-stu-id="0695e-722">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="0695e-723">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="0695e-723">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-724">Пропустить удаленных закладки</span><span class="sxs-lookup"><span data-stu-id="0695e-724">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="0695e-725">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="0695e-725">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-726">Строка строгого удостоверений</span><span class="sxs-lookup"><span data-stu-id="0695e-726">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="0695e-727">DBPROP_STRONGITDENTITY</span><span class="sxs-lookup"><span data-stu-id="0695e-727">DBPROP_STRONGITDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-728">Уникальные строки</span><span class="sxs-lookup"><span data-stu-id="0695e-728">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="0695e-729">DBPROP_UNIQUEROWS</span><span class="sxs-lookup"><span data-stu-id="0695e-729">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-730">Возможности обновления</span><span class="sxs-lookup"><span data-stu-id="0695e-730">Updatability</span></span></p></td>
<td><p><span data-ttu-id="0695e-731">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="0695e-731">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-732">Использование закладок</span><span class="sxs-lookup"><span data-stu-id="0695e-732">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="0695e-733">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="0695e-733">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a><span data-ttu-id="0695e-734">Динамические свойства команды</span><span class="sxs-lookup"><span data-stu-id="0695e-734">Command Dynamic Properties</span></span>

<span data-ttu-id="0695e-735">Следующие свойства добавляются в коллекцию **свойств** объекта **команды** .</span><span class="sxs-lookup"><span data-stu-id="0695e-735">The following properties are added to the **Command** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0695e-736">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="0695e-736">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="0695e-737">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="0695e-737">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0695e-738">Порядок доступа</span><span class="sxs-lookup"><span data-stu-id="0695e-738">Access Order</span></span></p></td>
<td><p><span data-ttu-id="0695e-739">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="0695e-739">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-740">Блокировка объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="0695e-740">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="0695e-741">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="0695e-741">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-742">Тип закладки</span><span class="sxs-lookup"><span data-stu-id="0695e-742">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="0695e-743">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="0695e-743">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-744">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="0695e-744">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="0695e-745">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="0695e-745">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-746">Изменение вставленных строк</span><span class="sxs-lookup"><span data-stu-id="0695e-746">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="0695e-747">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="0695e-747">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-748">Права доступа столбца</span><span class="sxs-lookup"><span data-stu-id="0695e-748">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="0695e-749">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="0695e-749">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-750">Столбец набор уведомлений</span><span class="sxs-lookup"><span data-stu-id="0695e-750">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="0695e-751">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="0695e-751">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-752">Отложенное обновление объекта хранения</span><span class="sxs-lookup"><span data-stu-id="0695e-752">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="0695e-753">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="0695e-753">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-754">Выборку</span><span class="sxs-lookup"><span data-stu-id="0695e-754">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="0695e-755">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="0695e-755">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-756">Хранение строк</span><span class="sxs-lookup"><span data-stu-id="0695e-756">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="0695e-757">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="0695e-757">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-758">IAccessor</span><span class="sxs-lookup"><span data-stu-id="0695e-758">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="0695e-759">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="0695e-759">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-760">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="0695e-760">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="0695e-761">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="0695e-761">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-762">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="0695e-762">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="0695e-763">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="0695e-763">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-764">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="0695e-764">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="0695e-765">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="0695e-765">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-766">IConvertType</span><span class="sxs-lookup"><span data-stu-id="0695e-766">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="0695e-767">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="0695e-767">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-768">Немобильные строки</span><span class="sxs-lookup"><span data-stu-id="0695e-768">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="0695e-769">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="0695e-769">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-770">IRowset</span><span class="sxs-lookup"><span data-stu-id="0695e-770">IRowset</span></span></p></td>
<td><p><span data-ttu-id="0695e-771">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="0695e-771">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-772">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="0695e-772">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="0695e-773">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="0695e-773">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-774">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="0695e-774">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="0695e-775">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="0695e-775">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-776">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="0695e-776">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="0695e-777">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="0695e-777">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-778">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="0695e-778">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="0695e-779">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="0695e-779">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-780">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="0695e-780">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-781">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="0695e-781">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="0695e-782">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="0695e-782">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-783">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="0695e-783">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="0695e-784">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="0695e-784">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-785">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="0695e-785">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="0695e-786">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="0695e-786">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-787">Литерал закладки</span><span class="sxs-lookup"><span data-stu-id="0695e-787">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="0695e-788">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="0695e-788">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-789">Удостоверение литерала строки</span><span class="sxs-lookup"><span data-stu-id="0695e-789">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="0695e-790">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="0695e-790">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-791">Максимальное число открытых строк</span><span class="sxs-lookup"><span data-stu-id="0695e-791">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="0695e-792">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="0695e-792">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-793">Максимум ожидающие строк</span><span class="sxs-lookup"><span data-stu-id="0695e-793">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="0695e-794">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="0695e-794">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-795">Максимальное число строк</span><span class="sxs-lookup"><span data-stu-id="0695e-795">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="0695e-796">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="0695e-796">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-797">Степень детализации уведомлений</span><span class="sxs-lookup"><span data-stu-id="0695e-797">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="0695e-798">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="0695e-798">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-799">Этапы уведомлений</span><span class="sxs-lookup"><span data-stu-id="0695e-799">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="0695e-800">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="0695e-800">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-801">Объекты в транзакции</span><span class="sxs-lookup"><span data-stu-id="0695e-801">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="0695e-802">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="0695e-802">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-803">Видны собственные изменения</span><span class="sxs-lookup"><span data-stu-id="0695e-803">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="0695e-804">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="0695e-804">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-805">Видны собственные операции вставки</span><span class="sxs-lookup"><span data-stu-id="0695e-805">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="0695e-806">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="0695e-806">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-807">Сохранять при аварийном завершении</span><span class="sxs-lookup"><span data-stu-id="0695e-807">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="0695e-808">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="0695e-808">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-809">Сохранять при фиксации</span><span class="sxs-lookup"><span data-stu-id="0695e-809">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="0695e-810">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="0695e-810">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-811">Быстрый перезапуск</span><span class="sxs-lookup"><span data-stu-id="0695e-811">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="0695e-812">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="0695e-812">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-813">Повторные события</span><span class="sxs-lookup"><span data-stu-id="0695e-813">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="0695e-814">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="0695e-814">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-815">Удаление удаленных строк</span><span class="sxs-lookup"><span data-stu-id="0695e-815">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="0695e-816">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="0695e-816">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-817">Сообщить о нескольких изменений</span><span class="sxs-lookup"><span data-stu-id="0695e-817">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="0695e-818">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="0695e-818">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-819">Вернуть ожидающие вставки</span><span class="sxs-lookup"><span data-stu-id="0695e-819">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="0695e-820">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="0695e-820">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-821">Удалить строку уведомлений</span><span class="sxs-lookup"><span data-stu-id="0695e-821">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="0695e-822">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="0695e-822">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-823">Строка первого уведомления об изменении</span><span class="sxs-lookup"><span data-stu-id="0695e-823">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="0695e-824">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="0695e-824">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-825">Строка вставки уведомлений</span><span class="sxs-lookup"><span data-stu-id="0695e-825">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="0695e-826">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="0695e-826">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-827">Привилегии строки</span><span class="sxs-lookup"><span data-stu-id="0695e-827">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="0695e-828">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="0695e-828">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-829">Уведомления о повторной синхронизации строки</span><span class="sxs-lookup"><span data-stu-id="0695e-829">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="0695e-830">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="0695e-830">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-831">Строка, потоковой модели</span><span class="sxs-lookup"><span data-stu-id="0695e-831">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="0695e-832">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="0695e-832">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-833">Уведомление об изменении отмены строки</span><span class="sxs-lookup"><span data-stu-id="0695e-833">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="0695e-834">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="0695e-834">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-835">Строка отмены Delete уведомлений</span><span class="sxs-lookup"><span data-stu-id="0695e-835">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="0695e-836">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="0695e-836">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-837">Вставка отмены строки уведомлений</span><span class="sxs-lookup"><span data-stu-id="0695e-837">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="0695e-838">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="0695e-838">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-839">Уведомление об обновлении строки</span><span class="sxs-lookup"><span data-stu-id="0695e-839">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="0695e-840">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="0695e-840">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-841">Уведомление об изменении положения строк выборки</span><span class="sxs-lookup"><span data-stu-id="0695e-841">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="0695e-842">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="0695e-842">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-843">Уведомление о выпуске набора строк</span><span class="sxs-lookup"><span data-stu-id="0695e-843">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="0695e-844">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="0695e-844">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-845">Прокрутка назад</span><span class="sxs-lookup"><span data-stu-id="0695e-845">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="0695e-846">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="0695e-846">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-847">Пропустить удаленных закладки</span><span class="sxs-lookup"><span data-stu-id="0695e-847">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="0695e-848">DBPROP_BOOKMARKSKIP</span><span class="sxs-lookup"><span data-stu-id="0695e-848">DBPROP_BOOKMARKSKIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-849">Строка строгого удостоверений</span><span class="sxs-lookup"><span data-stu-id="0695e-849">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="0695e-850">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="0695e-850">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0695e-851">Возможности обновления</span><span class="sxs-lookup"><span data-stu-id="0695e-851">Updatability</span></span></p></td>
<td><p><span data-ttu-id="0695e-852">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="0695e-852">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0695e-853">Использование закладок</span><span class="sxs-lookup"><span data-stu-id="0695e-853">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="0695e-854">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="0695e-854">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="0695e-855">См. также</span><span class="sxs-lookup"><span data-stu-id="0695e-855">See also</span></span>

<span data-ttu-id="0695e-856">Для получения дополнительных сведений о реализации и функциональным сведения о поставщик Microsoft OLE DB для ODBC обратитесь к [OLE DB Руководство программиста](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85)) или посетите [Центр разработчиков данных платформы](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).</span><span class="sxs-lookup"><span data-stu-id="0695e-856">For details regarding specific implementation and functional information about the Microsoft OLE DB Provider for ODBC, consult the [OLE DB Programmer's Guide](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85)) or visit the [Data Platform Developer Center](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).</span></span>

