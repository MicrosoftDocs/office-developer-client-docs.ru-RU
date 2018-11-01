---
title: Поставщик Microsoft OLE DB для ODBC
TOCTitle: Microsoft OLE DB Provider for ODBC
ms:assetid: c507567e-5ad1-b32a-f6ad-5ba2c39aa4c2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249964(v=office.15)
ms:contentKeyID: 48547602
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 66ef27165e6f5823cc97a295643dfc2ae5c205c2
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883185"
---
# <a name="microsoft-ole-db-provider-for-odbc"></a><span data-ttu-id="a1088-102">Поставщик Microsoft OLE DB для ODBC</span><span class="sxs-lookup"><span data-stu-id="a1088-102">Microsoft OLE DB Provider for ODBC</span></span>

<span data-ttu-id="a1088-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a1088-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a1088-104">Чтобы программист ADO или служб удаленных рабочих СТОЛОВ идеальном мире бы одно в каждом данных источника предоставляет интерфейс OLE DB, чтобы вызвать непосредственно в источник данных ADO.</span><span class="sxs-lookup"><span data-stu-id="a1088-104">To an ADO or RDS programmer, an ideal world would be one in which every data source exposes an OLE DB interface, so that ADO could call directly into the data source.</span></span> <span data-ttu-id="a1088-105">Несмотря на то, что все больше дополнительные базы данных поставщиков реализует интерфейсы OLE DB, некоторые источники данных не еще не представленных таким способом.</span><span class="sxs-lookup"><span data-stu-id="a1088-105">Although increasingly more database vendors are implementing OLE DB interfaces, some data sources are not yet exposed this way.</span></span> <span data-ttu-id="a1088-106">Тем не менее практически все СУБД в настоящее время может осуществляться через ODBC.</span><span class="sxs-lookup"><span data-stu-id="a1088-106">However, virtually all DBMS systems in use today can be accessed through ODBC.</span></span>

<span data-ttu-id="a1088-107">Драйверы ODBC доступны для всех основных СУБД, в настоящее время, включая Microsoft SQL Server, Microsoft Access (базы данных Microsoft Jet) и Microsoft FoxPro, кроме базы данных сторонних продуктов, таких как Oracle.</span><span class="sxs-lookup"><span data-stu-id="a1088-107">ODBC drivers are available for every major DBMS in use today, including Microsoft SQL Server, Microsoft Access (Microsoft Jet database engine), and Microsoft FoxPro, in addition to non-Microsoft database products such as Oracle.</span></span>

<span data-ttu-id="a1088-108">Поставщик ODBC Microsoft, однако позволяет ADO для подключения к источникам данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="a1088-108">The Microsoft ODBC Provider, however, allows ADO to connect to any ODBC data source.</span></span> <span data-ttu-id="a1088-109">Поставщик свободных потоков и Юникод.</span><span class="sxs-lookup"><span data-stu-id="a1088-109">The provider is free-threaded and Unicode enabled.</span></span>

<span data-ttu-id="a1088-110">Поставщик поддерживает транзакции, несмотря на то, что разные ядра СУБД предлагают различные виды поддержки транзакций.</span><span class="sxs-lookup"><span data-stu-id="a1088-110">The provider supports transactions, although different DBMS engines offer different types of transaction support.</span></span> <span data-ttu-id="a1088-111">Например Microsoft Access поддерживает до пяти уровней вложенных транзакций.</span><span class="sxs-lookup"><span data-stu-id="a1088-111">For example, Microsoft Access supports nested transactions up to five levels deep.</span></span>

<span data-ttu-id="a1088-112">Поставщик по умолчанию для ADO и поддерживаются все зависящие от поставщика ADO свойства и методы.</span><span class="sxs-lookup"><span data-stu-id="a1088-112">This is the default provider for ADO, and all provider-dependent ADO properties and methods are supported.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="a1088-113">Параметры строки подключения</span><span class="sxs-lookup"><span data-stu-id="a1088-113">Connection String Parameters</span></span>

<span data-ttu-id="a1088-114">Для подключения к данным поставщиком, задайте **поставщика =** аргумент свойства [ConnectionString](connectionstring-property-ado.md) для:</span><span class="sxs-lookup"><span data-stu-id="a1088-114">To connect to this provider, set the **Provider=** argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```sql 
 
MSDASQL 
```

<span data-ttu-id="a1088-115">Чтение свойства [поставщика](provider-property-ado.md) будет возвращать также этой строки.</span><span class="sxs-lookup"><span data-stu-id="a1088-115">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="a1088-116">Типичная строка подключения</span><span class="sxs-lookup"><span data-stu-id="a1088-116">Typical Connection String</span></span>

<span data-ttu-id="a1088-117">— Это строка соединения для данного поставщика:</span><span class="sxs-lookup"><span data-stu-id="a1088-117">A typical connection string for this provider is:</span></span>

```sql 
 
"Provider=MSDASQL;DSN=dsnName;UID=userName;PWD=userPassword;" 
```

<span data-ttu-id="a1088-118">Строка состоит из следующих ключевых слов:</span><span class="sxs-lookup"><span data-stu-id="a1088-118">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a1088-119">Keyword</span><span class="sxs-lookup"><span data-stu-id="a1088-119">Keyword</span></span></p></th>
<th><p><span data-ttu-id="a1088-120">Описание</span><span class="sxs-lookup"><span data-stu-id="a1088-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a1088-121"><strong>Поставщик</strong></span><span class="sxs-lookup"><span data-stu-id="a1088-121"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="a1088-122">Задает поставщика OLE DB для ODBC.</span><span class="sxs-lookup"><span data-stu-id="a1088-122">Specifies the OLE DB Provider for ODBC.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-123"><strong>УВЕДОМЛЕНИЯ О ДОСТАВКЕ</strong></span><span class="sxs-lookup"><span data-stu-id="a1088-123"><strong>DSN</strong></span></span></p></td>
<td><p><span data-ttu-id="a1088-124">Указывает имя источника данных.</span><span class="sxs-lookup"><span data-stu-id="a1088-124">Specifies the data source name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-125"><strong>UID</strong></span><span class="sxs-lookup"><span data-stu-id="a1088-125"><strong>UID</strong></span></span></p></td>
<td><p><span data-ttu-id="a1088-126">Задает имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="a1088-126">Specifies the user name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-127"><strong>PWD</strong></span><span class="sxs-lookup"><span data-stu-id="a1088-127"><strong>PWD</strong></span></span></p></td>
<td><p><span data-ttu-id="a1088-128">Задает пароль пользователя.</span><span class="sxs-lookup"><span data-stu-id="a1088-128">Specifies the user password.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-129"><strong>URL</strong>.</span><span class="sxs-lookup"><span data-stu-id="a1088-129"><strong>URL</strong></span></span></p></td>
<td><p><span data-ttu-id="a1088-130">Задает URL-адрес файла или папки, опубликованной в веб-папку.</span><span class="sxs-lookup"><span data-stu-id="a1088-130">Specifies the URL of a file or directory published in a web folder.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a1088-131">Так как это поставщика по умолчанию для ADO, если опустить **поставщика =** параметра в строке подключения ADO пытается установить подключение к данным поставщиком.</span><span class="sxs-lookup"><span data-stu-id="a1088-131">Because this is the default provider for ADO, if you omit the **Provider=** parameter from the connection string, ADO will attempt to establish a connection to this provider.</span></span>

<span data-ttu-id="a1088-132">Поставщик не поддерживает параметры подключения в дополнение к определяемые ADO.</span><span class="sxs-lookup"><span data-stu-id="a1088-132">The provider does not support any specific connection parameters in addition to those defined by ADO.</span></span> <span data-ttu-id="a1088-133">Тем не менее Поставщик передает параметры соединения не ADO драйвера ODBC.</span><span class="sxs-lookup"><span data-stu-id="a1088-133">However, the provider will pass any non-ADO connection parameters to the ODBC driver manager.</span></span>

<span data-ttu-id="a1088-134">Так как можно опустить параметр **поставщика** , таким образом можно создать строку подключения ADO, идентичный строки подключения ODBC для одного источника данных.</span><span class="sxs-lookup"><span data-stu-id="a1088-134">Because you can omit the **Provider** parameter, you can therefore compose an ADO connection string that is identical to an ODBC connection string for the same data source.</span></span> <span data-ttu-id="a1088-135">Используйте одинаковые имена параметров (**ДРАЙВЕРА =**, **базы данных =**, **уведомления о Доставке =** и так далее), значения и синтаксис, как вы бы при создании строки подключения ODBC.</span><span class="sxs-lookup"><span data-stu-id="a1088-135">Use the same parameter names (**DRIVER=**, **DATABASE=**, **DSN=**, and so on), values, and syntax as you would when composing an ODBC connection string.</span></span> <span data-ttu-id="a1088-136">Можно подключить с и без имя источника данных (DSN) или FileDSN.</span><span class="sxs-lookup"><span data-stu-id="a1088-136">You can connect with or without a predefined data source name (DSN) or FileDSN.</span></span>

<span data-ttu-id="a1088-137">**Синтаксис с уведомления о Доставке или FileDSN:**</span><span class="sxs-lookup"><span data-stu-id="a1088-137">**Syntax with a DSN or FileDSN:**</span></span>

`"[Provider=MSDASQL;] { DSN=name | FileDSN=filename } ; [DATABASE=database;] UID=user; PWD=password"`

<span data-ttu-id="a1088-138">**Синтаксис без уведомления о Доставке (соединения):**</span><span class="sxs-lookup"><span data-stu-id="a1088-138">**Syntax without a DSN (DSN-less connection):**</span></span>

`"[Provider=MSDASQL;] DRIVER=driver; SERVER=server;DATABASE=database; UID=user; PWD=password"`

<span data-ttu-id="a1088-139">Если вы используете **уведомления о Доставке** или **FileDSN**, его необходимо определить через источники данных ODBC в панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="a1088-139">If you use a **DSN** or **FileDSN**, it must be defined through the ODBC Data Source Administrator in the Windows Control Panel.</span></span> <span data-ttu-id="a1088-140">В Microsoft Windows 2000 администратор ODBC находится в разделе Администрирование.</span><span class="sxs-lookup"><span data-stu-id="a1088-140">In Microsoft Windows 2000, the ODBC Administrator is located under Administrative Tools.</span></span> <span data-ttu-id="a1088-141">В предыдущих версиях Windows значок администратор ODBC называется **32-разрядная версия ODBC** или просто **ODBC**.</span><span class="sxs-lookup"><span data-stu-id="a1088-141">In previous versions of Windows, the ODBC Administrator icon is named **32-bit ODBC** or simply **ODBC**.</span></span>

<span data-ttu-id="a1088-142">В качестве альтернативы для установки **уведомления о Доставке**, можно указать драйвер ODBC (**ДРАЙВЕРА =**), например «SQL Server»; имя сервера (**SERVER =**); и имя базы данных (**базы данных =**).</span><span class="sxs-lookup"><span data-stu-id="a1088-142">As an alternative to setting a **DSN**, you can specify the ODBC driver (**DRIVER=**), such as "SQL Server;" the server name (**SERVER=**); and the database name (**DATABASE=**).</span></span>

<span data-ttu-id="a1088-143">Также можно указать имя учетной записи пользователя (**UID =**) и пароль для учетной записи пользователя (**PWD =**) в параметры, относящиеся к ODBC или в стандартный определенные ADO *пользователя* и *пароль* параметры.</span><span class="sxs-lookup"><span data-stu-id="a1088-143">You can also specify a user account name (**UID=**), and the password for the user account (**PWD=**) in the ODBC-specific parameters or in the standard ADO-defined *user* and *password* parameters.</span></span>

<span data-ttu-id="a1088-144">Хотя **уведомления о Доставке** определение уже указывает базу данных, можно задать *параметр *базы данных* , в дополнение к **уведомления о Доставке** для подключения в другую базу данных* .</span><span class="sxs-lookup"><span data-stu-id="a1088-144">Although a **DSN** definition already specifies a database, you can specify *a* *database* parameter in addition to a **DSN** to connect to a different database.</span></span> <span data-ttu-id="a1088-145">Рекомендуется всегда включать \*параметр *базы данных* \* при использовании **уведомления о Доставке**.</span><span class="sxs-lookup"><span data-stu-id="a1088-145">It is a good idea to always include *the* *database* parameter when you use a **DSN**.</span></span> <span data-ttu-id="a1088-146">Это обеспечит подключиться к базе соответствующих прав в случае, когда другой пользователь изменить параметр базы данных по умолчанию с момента последнего извлечения определения **уведомления о Доставке** .</span><span class="sxs-lookup"><span data-stu-id="a1088-146">This will ensure that you connect to the proper database in the event that another user changed the default database parameter since you last checked the **DSN** definition.</span></span>

## <a name="provider-specific-connection-properties"></a><span data-ttu-id="a1088-147">Свойства подключения от поставщика</span><span class="sxs-lookup"><span data-stu-id="a1088-147">Provider-Specific Connection Properties</span></span>

<span data-ttu-id="a1088-148">Поставщик OLE DB для ODBC добавляет несколько свойств в коллекцию [свойств](properties-collection-ado.md) объекта **подключения** .</span><span class="sxs-lookup"><span data-stu-id="a1088-148">The OLE DB provider for ODBC adds several properties to the [Properties](properties-collection-ado.md) collection of the **Connection** object.</span></span> <span data-ttu-id="a1088-149">В следующей таблице перечислены эти свойства имя соответствующего свойства OLE DB в скобки.</span><span class="sxs-lookup"><span data-stu-id="a1088-149">The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a1088-150">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="a1088-150">Property Name</span></span></p></th>
<th><p><span data-ttu-id="a1088-151">Описание</span><span class="sxs-lookup"><span data-stu-id="a1088-151">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a1088-152">Доступны процедуры</span><span class="sxs-lookup"><span data-stu-id="a1088-152">Accessible Procedures</span></span><br />
<span data-ttu-id="a1088-153">(KAGPROP_ACCESSIBLEPROCEDURES)</span><span class="sxs-lookup"><span data-stu-id="a1088-153">(KAGPROP_ACCESSIBLEPROCEDURES)</span></span></p></td>
<td><p><span data-ttu-id="a1088-154">Указывает, является ли пользователь имеет доступ к хранимые процедуры.</span><span class="sxs-lookup"><span data-stu-id="a1088-154">Indicates whether the user has access to stored procedures.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-155">Доступно таблиц</span><span class="sxs-lookup"><span data-stu-id="a1088-155">Accessible Tables</span></span><br />
<span data-ttu-id="a1088-156">(KAGPROP_ACCESSIBLETABLES)</span><span class="sxs-lookup"><span data-stu-id="a1088-156">(KAGPROP_ACCESSIBLETABLES)</span></span></p></td>
<td><p><span data-ttu-id="a1088-157">Указывает, является ли пользователь имеет разрешения на выполнение инструкций SELECT таблиц базы данных.</span><span class="sxs-lookup"><span data-stu-id="a1088-157">Indicates whether the user has permission to execute SELECT statements against the database tables.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-158">Активные операторы</span><span class="sxs-lookup"><span data-stu-id="a1088-158">Active Statements</span></span><br />
<span data-ttu-id="a1088-159">(KAGPROP_ACTIVESTATEMENTS)</span><span class="sxs-lookup"><span data-stu-id="a1088-159">(KAGPROP_ACTIVESTATEMENTS)</span></span></p></td>
<td><p><span data-ttu-id="a1088-160">Указывает число дескрипторов, которые может поддерживать драйвера ODBC для подключения.</span><span class="sxs-lookup"><span data-stu-id="a1088-160">Indicates the number of handles an ODBC driver can support on a connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-161">Имя драйвера</span><span class="sxs-lookup"><span data-stu-id="a1088-161">Driver Name</span></span><br />
<span data-ttu-id="a1088-162">(KAGPROP_DRIVERNAME)</span><span class="sxs-lookup"><span data-stu-id="a1088-162">(KAGPROP_DRIVERNAME)</span></span></p></td>
<td><p><span data-ttu-id="a1088-163">Указывает имя файла драйвера ODBC.</span><span class="sxs-lookup"><span data-stu-id="a1088-163">Indicates the file name of the ODBC driver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-164">Версия драйвера ODBC</span><span class="sxs-lookup"><span data-stu-id="a1088-164">Driver ODBC Version</span></span><br />
<span data-ttu-id="a1088-165">(KAGPROP_DRIVERODBCVER)</span><span class="sxs-lookup"><span data-stu-id="a1088-165">(KAGPROP_DRIVERODBCVER)</span></span></p></td>
<td><p><span data-ttu-id="a1088-166">Указывает версию, поддерживающего этот драйвер ODBC.</span><span class="sxs-lookup"><span data-stu-id="a1088-166">Indicates the version of ODBC that this driver supports.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-167">Использование файлов</span><span class="sxs-lookup"><span data-stu-id="a1088-167">File Usage</span></span><br />
<span data-ttu-id="a1088-168">(KAGPROP_FILEUSAGE)</span><span class="sxs-lookup"><span data-stu-id="a1088-168">(KAGPROP_FILEUSAGE)</span></span></p></td>
<td><p><span data-ttu-id="a1088-169">Указывает, как драйвер обрабатывает файл источника данных. как таблицы или как к каталогу.</span><span class="sxs-lookup"><span data-stu-id="a1088-169">Indicates how the driver treats a file in a data source; as a table or as a catalog.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-170">Как предложение escape-последовательности</span><span class="sxs-lookup"><span data-stu-id="a1088-170">Like Escape Clause</span></span><br />
<span data-ttu-id="a1088-171">(KAGPROP_LIKEESCAPECLAUSE)</span><span class="sxs-lookup"><span data-stu-id="a1088-171">(KAGPROP_LIKEESCAPECLAUSE)</span></span></p></td>
<td><p><span data-ttu-id="a1088-172">Указывает предикат LIKE предложение WHERE ли драйвер поддерживается в определение и использование escape-символ знаком процента (%) и символ подчеркивания (_).</span><span class="sxs-lookup"><span data-stu-id="a1088-172">Indicates whether the driver supports the definition and use of an escape character for the percent character (%) and underline character (_) in the LIKE predicate of a WHERE clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-173">Максимальное число столбцов в группировать по</span><span class="sxs-lookup"><span data-stu-id="a1088-173">Max Columns in Group By</span></span><br />
<span data-ttu-id="a1088-174">(KAGPROP_MAXCOLUMNSINGROUPBY)</span><span class="sxs-lookup"><span data-stu-id="a1088-174">(KAGPROP_MAXCOLUMNSINGROUPBY)</span></span></p></td>
<td><p><span data-ttu-id="a1088-175">Указывает максимальное число столбцов, которые могут быть перечислены в предложении GROUP BY инструкции SELECT.</span><span class="sxs-lookup"><span data-stu-id="a1088-175">Indicates the maximum number of columns that can be listed in the GROUP BY clause of a SELECT statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-176">Максимальное число столбцов в индексе</span><span class="sxs-lookup"><span data-stu-id="a1088-176">Max Columns in Index</span></span><br />
<span data-ttu-id="a1088-177">(KAGPROP_MAXCOLUMNSININDEX)</span><span class="sxs-lookup"><span data-stu-id="a1088-177">(KAGPROP_MAXCOLUMNSININDEX)</span></span></p></td>
<td><p><span data-ttu-id="a1088-178">Указывает максимальное число столбцов, которые можно включить в индекс.</span><span class="sxs-lookup"><span data-stu-id="a1088-178">Indicates the maximum number of columns that can be included in an index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-179">Максимальное число столбцов в порядке</span><span class="sxs-lookup"><span data-stu-id="a1088-179">Max Columns in Order By</span></span><br />
<span data-ttu-id="a1088-180">(KAGPROP_MAXCOLUMNSINORDERBY)</span><span class="sxs-lookup"><span data-stu-id="a1088-180">(KAGPROP_MAXCOLUMNSINORDERBY)</span></span></p></td>
<td><p><span data-ttu-id="a1088-181">Указывает максимальное число столбцов, которые могут быть перечислены в предложение ORDER BY инструкции SELECT.</span><span class="sxs-lookup"><span data-stu-id="a1088-181">Indicates the maximum number of columns that can be listed in the ORDER BY clause of a SELECT statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-182">Максимальное число столбцов в Выбор</span><span class="sxs-lookup"><span data-stu-id="a1088-182">Max Columns in Select</span></span><br />
<span data-ttu-id="a1088-183">(KAGPROP_MAXCOLUMNSINSELECT)</span><span class="sxs-lookup"><span data-stu-id="a1088-183">(KAGPROP_MAXCOLUMNSINSELECT)</span></span></p></td>
<td><p><span data-ttu-id="a1088-184">Указывает максимальное число столбцов, которые могут быть перечислены в разделе SELECT инструкции SELECT.</span><span class="sxs-lookup"><span data-stu-id="a1088-184">Indicates the maximum number of columns that can be listed in the SELECT portion of a SELECT statement.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-185">Максимальное число столбцов в таблице</span><span class="sxs-lookup"><span data-stu-id="a1088-185">Max Columns in Table</span></span><br />
<span data-ttu-id="a1088-186">(KAGPROP_MAXCOLUMNSINTABLE)</span><span class="sxs-lookup"><span data-stu-id="a1088-186">(KAGPROP_MAXCOLUMNSINTABLE)</span></span></p></td>
<td><p><span data-ttu-id="a1088-187">Указывает максимальное число столбцов в таблице.</span><span class="sxs-lookup"><span data-stu-id="a1088-187">Indicates the maximum number of columns allowed in a table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-188">Числовые функции</span><span class="sxs-lookup"><span data-stu-id="a1088-188">Numeric Functions</span></span><br />
<span data-ttu-id="a1088-189">(KAGPROP_NUMERICFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="a1088-189">(KAGPROP_NUMERICFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="a1088-190">Указывает, какие числовые функции поддерживаются драйвер ODBC.</span><span class="sxs-lookup"><span data-stu-id="a1088-190">Indicates which numeric functions are supported by the ODBC driver.</span></span> <span data-ttu-id="a1088-191">Список имен функций и связанные значения, используемые в этом Битовая маска, см в приложении д: скалярные в документации по ODBC.</span><span class="sxs-lookup"><span data-stu-id="a1088-191">For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-192">Возможности внешнего соединения</span><span class="sxs-lookup"><span data-stu-id="a1088-192">Outer Join Capabilities</span></span><br />
<span data-ttu-id="a1088-193">(KAGPROP_OJCAPABILITY)</span><span class="sxs-lookup"><span data-stu-id="a1088-193">(KAGPROP_OJCAPABILITY)</span></span></p></td>
<td><p><span data-ttu-id="a1088-194">Указывает типы ВНЕШНИЕ соединения, поддерживаемых поставщиком.</span><span class="sxs-lookup"><span data-stu-id="a1088-194">Indicates the types of OUTER JOINs supported by the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-195">Внешние соединения</span><span class="sxs-lookup"><span data-stu-id="a1088-195">Outer Joins</span></span><br />
<span data-ttu-id="a1088-196">(KAGPROP_OUTERJOINS)</span><span class="sxs-lookup"><span data-stu-id="a1088-196">(KAGPROP_OUTERJOINS)</span></span></p></td>
<td><p><span data-ttu-id="a1088-197">Указывает, является ли поставщик поддерживает ВНЕШНИЕ соединения.</span><span class="sxs-lookup"><span data-stu-id="a1088-197">Indicates whether the provider supports OUTER JOINs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-198">Специальные символы</span><span class="sxs-lookup"><span data-stu-id="a1088-198">Special Characters</span></span><br />
<span data-ttu-id="a1088-199">(KAGPROP_SPECIALCHARACTERS)</span><span class="sxs-lookup"><span data-stu-id="a1088-199">(KAGPROP_SPECIALCHARACTERS)</span></span></p></td>
<td><p><span data-ttu-id="a1088-200">Указывает, какие символы имеет особое значение для драйвера ODBC.</span><span class="sxs-lookup"><span data-stu-id="a1088-200">Indicates which characters have special meaning for the ODBC driver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-201">Хранимые процедуры</span><span class="sxs-lookup"><span data-stu-id="a1088-201">Stored Procedures</span></span><br />
<span data-ttu-id="a1088-202">(KAGPROP_PROCEDURES)</span><span class="sxs-lookup"><span data-stu-id="a1088-202">(KAGPROP_PROCEDURES)</span></span></p></td>
<td><p><span data-ttu-id="a1088-203">Указывает, доступны ли хранимые процедуры для использования с этой драйвер ODBC.</span><span class="sxs-lookup"><span data-stu-id="a1088-203">Indicates whether stored procedures are available for use with this ODBC driver.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-204">Строковые функции</span><span class="sxs-lookup"><span data-stu-id="a1088-204">String Functions</span></span><br />
<span data-ttu-id="a1088-205">(KAGPROP_STRINGFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="a1088-205">(KAGPROP_STRINGFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="a1088-206">Указывает, какие функции string, поддерживаются драйвер ODBC.</span><span class="sxs-lookup"><span data-stu-id="a1088-206">Indicates which string functions are supported by the ODBC driver.</span></span> <span data-ttu-id="a1088-207">Список имен функций и связанные значения, используемые в этом Битовая маска, см в приложении д: скалярные в документации по ODBC.</span><span class="sxs-lookup"><span data-stu-id="a1088-207">For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-208">Системные функции</span><span class="sxs-lookup"><span data-stu-id="a1088-208">System Functions</span></span><br />
<span data-ttu-id="a1088-209">(KAGPROP_SYSTEMFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="a1088-209">(KAGPROP_SYSTEMFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="a1088-210">Указывает, какие функции системы поддерживаются драйвер ODBC.</span><span class="sxs-lookup"><span data-stu-id="a1088-210">Indicates which system functions are supported by the ODBC driver.</span></span> <span data-ttu-id="a1088-211">Список имен функций и связанные значения, используемые в этом Битовая маска, см в приложении д: скалярные в документации по ODBC.</span><span class="sxs-lookup"><span data-stu-id="a1088-211">For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-212">Время и Дата функции</span><span class="sxs-lookup"><span data-stu-id="a1088-212">Time/Date Functions</span></span><br />
<span data-ttu-id="a1088-213">(KAGPROP_TIMEDATEFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="a1088-213">(KAGPROP_TIMEDATEFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="a1088-214">Указывает, какие функции даты и времени поддерживаются драйвер ODBC.</span><span class="sxs-lookup"><span data-stu-id="a1088-214">Indicates which time and date functions are supported by the ODBC driver.</span></span> <span data-ttu-id="a1088-215">Список имен функций и связанные значения, используемые в этом Битовая маска, см в приложении д: скалярные в документации по ODBC.</span><span class="sxs-lookup"><span data-stu-id="a1088-215">For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-216">Поддержка грамматики SQL</span><span class="sxs-lookup"><span data-stu-id="a1088-216">SQL Grammar Support</span></span><br />
<span data-ttu-id="a1088-217">(KAGPROP_ODBCSQLCONFORMANCE)</span><span class="sxs-lookup"><span data-stu-id="a1088-217">(KAGPROP_ODBCSQLCONFORMANCE)</span></span></p></td>
<td><p><span data-ttu-id="a1088-218">Указывает грамматику SQL, которая поддерживает драйвер ODBC.</span><span class="sxs-lookup"><span data-stu-id="a1088-218">Indicates the SQL grammar that the ODBC driver supports.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-recordset-and-command-properties"></a><span data-ttu-id="a1088-219">Свойства команды и записей от поставщика</span><span class="sxs-lookup"><span data-stu-id="a1088-219">Provider-Specific Recordset and Command Properties</span></span>

<span data-ttu-id="a1088-220">Поставщик OLE DB для ODBC добавляет несколько свойств **Свойства** набора **записей** и **командных** объектов.</span><span class="sxs-lookup"><span data-stu-id="a1088-220">The OLE DB provider for ODBC adds several properties to the **Properties** collection of the **Recordset** and **Command** objects.</span></span> <span data-ttu-id="a1088-221">В следующей таблице перечислены эти свойства имя соответствующего свойства OLE DB в скобки.</span><span class="sxs-lookup"><span data-stu-id="a1088-221">The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a1088-222">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="a1088-222">Property Name</span></span></p></th>
<th><p><span data-ttu-id="a1088-223">Описание</span><span class="sxs-lookup"><span data-stu-id="a1088-223">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a1088-224">Запрос на основе обновления, удаления или вставки</span><span class="sxs-lookup"><span data-stu-id="a1088-224">Query Based Updates/Deletes/Inserts</span></span><br />
<span data-ttu-id="a1088-225">(KAGPROP_QUERYBASEDUPDATES)</span><span class="sxs-lookup"><span data-stu-id="a1088-225">(KAGPROP_QUERYBASEDUPDATES)</span></span></p></td>
<td><p><span data-ttu-id="a1088-226">Указывает, будет ли обновления, удаления и вставки можно выполнить с помощью SQL-запросов.</span><span class="sxs-lookup"><span data-stu-id="a1088-226">Indicates whether updates, deletions, and insertions can be performed using SQL queries.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-227">Тип параллельного ODBC</span><span class="sxs-lookup"><span data-stu-id="a1088-227">ODBC Concurrency Type</span></span><br />
<span data-ttu-id="a1088-228">(KAGPROP_CONCURRENCY)</span><span class="sxs-lookup"><span data-stu-id="a1088-228">(KAGPROP_CONCURRENCY)</span></span></p></td>
<td><p><span data-ttu-id="a1088-229">Метод, используемый для уменьшения потенциальных проблем, вызванных двух пользователей одновременно к той же информации из источника данных.</span><span class="sxs-lookup"><span data-stu-id="a1088-229">Indicates the method used to reduce potential problems caused by two users attempting to access the same data from the data source simultaneously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-230">Специальные возможности больших двоичных ОБЪЕКТОВ на последовательный курсор</span><span class="sxs-lookup"><span data-stu-id="a1088-230">BLOB accessibility on Forward-Only cursor</span></span><br />
<span data-ttu-id="a1088-231">(KAGPROP_BLOBSONFOCURSOR)</span><span class="sxs-lookup"><span data-stu-id="a1088-231">(KAGPROP_BLOBSONFOCURSOR)</span></span></p></td>
<td><p><span data-ttu-id="a1088-232">Указывает, будет ли при использовании последовательный курсор возможен больших двоичных ОБЪЕКТОВ <strong>полей</strong> .</span><span class="sxs-lookup"><span data-stu-id="a1088-232">Indicates whether BLOB <strong>Fields</strong> can be accessed when using a forward-only cursor.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-233">Включить в предложения QBU WHERE SQL_FLOAT, SQL_DOUBLE и SQL_REAL</span><span class="sxs-lookup"><span data-stu-id="a1088-233">Include SQL_FLOAT, SQL_DOUBLE, and SQL_REAL in QBU WHERE clauses</span></span><br />
<span data-ttu-id="a1088-234">(KAGPROP_INCLUDENONEXACT)</span><span class="sxs-lookup"><span data-stu-id="a1088-234">(KAGPROP_INCLUDENONEXACT)</span></span></p></td>
<td><p><span data-ttu-id="a1088-235">Указывает, будет ли значения SQL_FLOAT, SQL_DOUBLE и SQL_REAL может быть включен в предложении QBU WHERE.</span><span class="sxs-lookup"><span data-stu-id="a1088-235">Indicates whether SQL_FLOAT, SQL_DOUBLE, and SQL_REAL values can be included in a QBU WHERE clause.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-236">Положение в последней строке после вставки</span><span class="sxs-lookup"><span data-stu-id="a1088-236">Position on the last row after insert</span></span><br />
<span data-ttu-id="a1088-237">(KAGPROP_POSITIONONNEWROW)</span><span class="sxs-lookup"><span data-stu-id="a1088-237">(KAGPROP_POSITIONONNEWROW)</span></span></p></td>
<td><p><span data-ttu-id="a1088-238">Указывает, что после вставки новой записи в таблице последней строки в таблице должны быть поступают текущей строки.</span><span class="sxs-lookup"><span data-stu-id="a1088-238">Indicates that after a new record has been inserted in a table, the last row in the table will be come the current row.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-239">IRowsetChangeExtInfo</span><span class="sxs-lookup"><span data-stu-id="a1088-239">IRowsetChangeExtInfo</span></span><br />
<span data-ttu-id="a1088-240">(KAGPROP_IROWSETCHANGEEXTINFO)</span><span class="sxs-lookup"><span data-stu-id="a1088-240">(KAGPROP_IROWSETCHANGEEXTINFO)</span></span></p></td>
<td><p><span data-ttu-id="a1088-241">Указывает, будет ли интерфейс <strong>IRowsetChange</strong> поддерживает расширенные сведения.</span><span class="sxs-lookup"><span data-stu-id="a1088-241">Indicates whether the <strong>IRowsetChange</strong> interface provides extended information support.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-242">Тип курсора ODBC</span><span class="sxs-lookup"><span data-stu-id="a1088-242">ODBC Cursor Type</span></span><br />
<span data-ttu-id="a1088-243">(KAGPROP_CURSOR)</span><span class="sxs-lookup"><span data-stu-id="a1088-243">(KAGPROP_CURSOR)</span></span></p></td>
<td><p><span data-ttu-id="a1088-244">Указывает тип курсора, используемого <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="a1088-244">Indicates the type of cursor used by the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-245">Создать набор строк, который может быть упакован</span><span class="sxs-lookup"><span data-stu-id="a1088-245">Generate a Rowset that can be marshaled</span></span><br />
<span data-ttu-id="a1088-246">(KAGPROP_MARSHALLABLE)</span><span class="sxs-lookup"><span data-stu-id="a1088-246">(KAGPROP_MARSHALLABLE)</span></span></p></td>
<td><p><span data-ttu-id="a1088-247">Указывает, что драйвер ODBC создает набор записей, который может быть упакован</span><span class="sxs-lookup"><span data-stu-id="a1088-247">Indicates that the ODBC driver generates a recordset that can be marshaled</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-text"></a><span data-ttu-id="a1088-248">Текст команды</span><span class="sxs-lookup"><span data-stu-id="a1088-248">Command Text</span></span>

<span data-ttu-id="a1088-249">Как использовать объект [команды](command-object-ado.md) во многом зависит от источника данных и какой тип оператора запроса или команды будет принимать.</span><span class="sxs-lookup"><span data-stu-id="a1088-249">How you use the [Command](command-object-ado.md) object largely depends on the data source, and what type of query or command statement it will accept.</span></span>

<span data-ttu-id="a1088-250">ODBC предоставляет определенный синтаксис для вызова хранимых процедур.</span><span class="sxs-lookup"><span data-stu-id="a1088-250">ODBC provides a specific syntax for calling stored procedures.</span></span> <span data-ttu-id="a1088-251">Для свойства [CommandText](commandtext-property-ado.md) объекта **команды** *CommandText* аргумента метода **Execute** на объект [подключения](connection-object-ado.md) и *исходный* аргумент методу **Open** на [набора записей](recordset-object-ado.md) объект передает в строку с помощью следующего синтаксиса:</span><span class="sxs-lookup"><span data-stu-id="a1088-251">For the [CommandText](commandtext-property-ado.md) property of a **Command** object, the *CommandText* argument to the **Execute** method on a [Connection](connection-object-ado.md) object, or the *Source* argument to the **Open** method on a [Recordset](recordset-object-ado.md) object, passes in a string with this syntax:</span></span>

`"{ [ ? = ] call procedure [ ( ? [, ? [ ,  ]] ) ] }"`

<span data-ttu-id="a1088-252">Каждый **?**</span><span class="sxs-lookup"><span data-stu-id="a1088-252">Each **?**</span></span> <span data-ttu-id="a1088-253">содержит ссылку на объект в коллекции [параметров](parameters-collection-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="a1088-253">references an object in the [Parameters](parameters-collection-ado.md) collection.</span></span> <span data-ttu-id="a1088-254">Первый **?**</span><span class="sxs-lookup"><span data-stu-id="a1088-254">The first **?**</span></span> <span data-ttu-id="a1088-255">ссылки на **Параметры**(0), Далее **?**</span><span class="sxs-lookup"><span data-stu-id="a1088-255">references **Parameters**(0), the next **?**</span></span> <span data-ttu-id="a1088-256">Создание ссылки **Параметры**(1) и т. д.</span><span class="sxs-lookup"><span data-stu-id="a1088-256">references **Parameters**(1), and so on.</span></span>

<span data-ttu-id="a1088-257">Параметр ссылки являются необязательными и зависят от структуры хранимую процедуру.</span><span class="sxs-lookup"><span data-stu-id="a1088-257">The parameter references are optional and depend on the structure of the stored procedure.</span></span> <span data-ttu-id="a1088-258">Если вы хотите вызвать хранимую процедуру, определяющий без параметров, строка будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a1088-258">If you want to call a stored procedure that defines no parameters, your string would look like this:</span></span>

`"{ call procedure }"`

<span data-ttu-id="a1088-259">Если у вас есть два параметра запроса, строка будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a1088-259">If you have two query parameters, your string would look like this:</span></span>

`"{ call procedure ( ?, ? ) }"`

<span data-ttu-id="a1088-260">Если хранимая процедура возвращает значение, возвращаемое значение обрабатывается как еще один параметр.</span><span class="sxs-lookup"><span data-stu-id="a1088-260">If the stored procedure will return a value, the return value is treated as another parameter.</span></span> <span data-ttu-id="a1088-261">Если у вас нет параметров запроса, но возвращаемое значение, строка будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a1088-261">If you have no query parameters but you do have a return value, your string would look like this:</span></span>

`"{ ? = call procedure }"`

<span data-ttu-id="a1088-262">И, наконец Если у вас есть возвращаемое значение и два параметра запроса, строка будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a1088-262">Finally, if you have a return value and two query parameters, your string would look like this:</span></span>

`"{ ? = call procedure ( ?, ? ) }"`

## <a name="recordset-behavior"></a><span data-ttu-id="a1088-263">Поведение набора записей</span><span class="sxs-lookup"><span data-stu-id="a1088-263">Recordset Behavior</span></span>

<span data-ttu-id="a1088-264">В следующих таблицах перечислены стандартные ADO методы и свойства, доступные для объекта **набора записей** , открытых с этим поставщиком.</span><span class="sxs-lookup"><span data-stu-id="a1088-264">The following tables list the standard ADO methods and properties available on a **Recordset** object opened with this provider.</span></span>

<span data-ttu-id="a1088-265">Для получения дополнительных сведений о поведении **набора записей** для вашей конфигурации поставщика, выполните метод [поддерживает](supports-method-ado.md) и перечисления коллекции **свойств** **набора записей** для определения целесообразности поставщиком динамических свойства отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="a1088-265">For more detailed information about **Recordset** behavior for your provider configuration, run the [Supports](supports-method-ado.md) method and enumerate the **Properties** collection of the **Recordset** to determine whether provider-specific dynamic properties are present.</span></span>

<span data-ttu-id="a1088-266">Доступность стандартными свойствами ADO **набора записей** :</span><span class="sxs-lookup"><span data-stu-id="a1088-266">Availability of standard ADO **Recordset** properties:</span></span>

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
<th><p><span data-ttu-id="a1088-267">Свойство</span><span class="sxs-lookup"><span data-stu-id="a1088-267">Property</span></span></p></th>
<th><p><span data-ttu-id="a1088-268">ForwardOnly</span><span class="sxs-lookup"><span data-stu-id="a1088-268">ForwardOnly</span></span></p></th>
<th><p><span data-ttu-id="a1088-269">Динамическая группа</span><span class="sxs-lookup"><span data-stu-id="a1088-269">Dynamic</span></span></p></th>
<th><p><span data-ttu-id="a1088-270">Набор ключей</span><span class="sxs-lookup"><span data-stu-id="a1088-270">Keyset</span></span></p></th>
<th><p><span data-ttu-id="a1088-271">Статическое</span><span class="sxs-lookup"><span data-stu-id="a1088-271">Static</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a1088-272"><a href="absolutepage-property-ado.md">AbsolutePage</a></span><span class="sxs-lookup"><span data-stu-id="a1088-272"><a href="absolutepage-property-ado.md">AbsolutePage</a></span></span></p></td>
<td><p><span data-ttu-id="a1088-273">Недоступен</span><span class="sxs-lookup"><span data-stu-id="a1088-273">not available</span></span></p></td>
<td><p><span data-ttu-id="a1088-274">Недоступен</span><span class="sxs-lookup"><span data-stu-id="a1088-274">not available</span></span></p></td>
<td><p><span data-ttu-id="a1088-275">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a1088-275">read/write</span></span></p></td>
<td><p><span data-ttu-id="a1088-276">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a1088-276">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-277"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span><span class="sxs-lookup"><span data-stu-id="a1088-277"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span></span></p></td>
<td><p><span data-ttu-id="a1088-278">Недоступен</span><span class="sxs-lookup"><span data-stu-id="a1088-278">not available</span></span></p></td>
<td><p><span data-ttu-id="a1088-279">Недоступен</span><span class="sxs-lookup"><span data-stu-id="a1088-279">not available</span></span></p></td>
<td><p><span data-ttu-id="a1088-280">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a1088-280">read/write</span></span></p></td>
<td><p><span data-ttu-id="a1088-281">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a1088-281">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-282"><a href="activeconnection-property-ado.md">ActiveConnection</a></span><span class="sxs-lookup"><span data-stu-id="a1088-282"><a href="activeconnection-property-ado.md">ActiveConnection</a></span></span></p></td>
<td><p><span data-ttu-id="a1088-283">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a1088-283">read/write</span></span></p></td>
<td><p><span data-ttu-id="a1088-284">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a1088-284">read/write</span></span></p></td>
<td><p><span data-ttu-id="a1088-285">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a1088-285">read/write</span></span></p></td>
<td><p><span data-ttu-id="a1088-286">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a1088-286">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-287"><a href="bof-eof-properties-ado.md">BOF</a></span><span class="sxs-lookup"><span data-stu-id="a1088-287"><a href="bof-eof-properties-ado.md">BOF</a></span></span></p></td>
<td><p><span data-ttu-id="a1088-288">только для чтения</span><span class="sxs-lookup"><span data-stu-id="a1088-288">read-only</span></span></p></td>
<td><p><span data-ttu-id="a1088-289">только для чтения</span><span class="sxs-lookup"><span data-stu-id="a1088-289">read-only</span></span></p></td>
<td><p><span data-ttu-id="a1088-290">только для чтения</span><span class="sxs-lookup"><span data-stu-id="a1088-290">read-only</span></span></p></td>
<td><p><span data-ttu-id="a1088-291">только для чтения</span><span class="sxs-lookup"><span data-stu-id="a1088-291">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-292"><a href="bookmark-property-ado.md">Закладка</a></span><span class="sxs-lookup"><span data-stu-id="a1088-292"><a href="bookmark-property-ado.md">Bookmark</a></span></span></p></td>
<td><p><span data-ttu-id="a1088-293">Недоступен</span><span class="sxs-lookup"><span data-stu-id="a1088-293">not available</span></span></p></td>
<td><p><span data-ttu-id="a1088-294">Недоступен</span><span class="sxs-lookup"><span data-stu-id="a1088-294">not available</span></span></p></td>
<td><p><span data-ttu-id="a1088-295">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a1088-295">read/write</span></span></p></td>
<td><p><span data-ttu-id="a1088-296">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a1088-296">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-297"><a href="cachesize-property-ado.md">CacheSize</a></span><span class="sxs-lookup"><span data-stu-id="a1088-297"><a href="cachesize-property-ado.md">CacheSize</a></span></span></p></td>
<td><p><span data-ttu-id="a1088-298">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a1088-298">read/write</span></span></p></td>
<td><p><span data-ttu-id="a1088-299">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a1088-299">read/write</span></span></p></td>
<td><p><span data-ttu-id="a1088-300">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a1088-300">read/write</span></span></p></td>
<td><p><span data-ttu-id="a1088-301">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a1088-301">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-302"><a href="cursorlocation-property-ado.md">CursorLocation</a></span><span class="sxs-lookup"><span data-stu-id="a1088-302"><a href="cursorlocation-property-ado.md">CursorLocation</a></span></span></p></td>
<td><p><span data-ttu-id="a1088-303">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a1088-303">read/write</span></span></p></td>
<td><p><span data-ttu-id="a1088-304">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a1088-304">read/write</span></span></p></td>
<td><p><span data-ttu-id="a1088-305">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a1088-305">read/write</span></span></p></td>
<td><p><span data-ttu-id="a1088-306">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a1088-306">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-307"><a href="cursortype-property-ado.md">CursorType</a></span><span class="sxs-lookup"><span data-stu-id="a1088-307"><a href="cursortype-property-ado.md">CursorType</a></span></span></p></td>
<td><p><span data-ttu-id="a1088-308">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a1088-308">read/write</span></span></p></td>
<td><p><span data-ttu-id="a1088-309">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a1088-309">read/write</span></span></p></td>
<td><p><span data-ttu-id="a1088-310">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a1088-310">read/write</span></span></p></td>
<td><p><span data-ttu-id="a1088-311">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a1088-311">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-312"><a href="editmode-property-ado.md">EditMode</a></span><span class="sxs-lookup"><span data-stu-id="a1088-312"><a href="editmode-property-ado.md">EditMode</a></span></span></p></td>
<td><p><span data-ttu-id="a1088-313">только для чтения</span><span class="sxs-lookup"><span data-stu-id="a1088-313">read-only</span></span></p></td>
<td><p><span data-ttu-id="a1088-314">только для чтения</span><span class="sxs-lookup"><span data-stu-id="a1088-314">read-only</span></span></p></td>
<td><p><span data-ttu-id="a1088-315">только для чтения</span><span class="sxs-lookup"><span data-stu-id="a1088-315">read-only</span></span></p></td>
<td><p><span data-ttu-id="a1088-316">только для чтения</span><span class="sxs-lookup"><span data-stu-id="a1088-316">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-317"><a href="filter-property-ado.md">Filter</a></span><span class="sxs-lookup"><span data-stu-id="a1088-317"><a href="filter-property-ado.md">Filter</a></span></span></p></td>
<td><p><span data-ttu-id="a1088-318">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a1088-318">read/write</span></span></p></td>
<td><p><span data-ttu-id="a1088-319">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a1088-319">read/write</span></span></p></td>
<td><p><span data-ttu-id="a1088-320">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a1088-320">read/write</span></span></p></td>
<td><p><span data-ttu-id="a1088-321">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a1088-321">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-322"><a href="locktype-property-ado.md">LockType для</a></span><span class="sxs-lookup"><span data-stu-id="a1088-322"><a href="locktype-property-ado.md">LockType</a></span></span></p></td>
<td><p><span data-ttu-id="a1088-323">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a1088-323">read/write</span></span></p></td>
<td><p><span data-ttu-id="a1088-324">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a1088-324">read/write</span></span></p></td>
<td><p><span data-ttu-id="a1088-325">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a1088-325">read/write</span></span></p></td>
<td><p><span data-ttu-id="a1088-326">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a1088-326">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-327"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span><span class="sxs-lookup"><span data-stu-id="a1088-327"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span></span></p></td>
<td><p><span data-ttu-id="a1088-328">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a1088-328">read/write</span></span></p></td>
<td><p><span data-ttu-id="a1088-329">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a1088-329">read/write</span></span></p></td>
<td><p><span data-ttu-id="a1088-330">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a1088-330">read/write</span></span></p></td>
<td><p><span data-ttu-id="a1088-331">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a1088-331">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-332"><a href="maxrecords-property-ado.md">MaxRecords</a></span><span class="sxs-lookup"><span data-stu-id="a1088-332"><a href="maxrecords-property-ado.md">MaxRecords</a></span></span></p></td>
<td><p><span data-ttu-id="a1088-333">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a1088-333">read/write</span></span></p></td>
<td><p><span data-ttu-id="a1088-334">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a1088-334">read/write</span></span></p></td>
<td><p><span data-ttu-id="a1088-335">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a1088-335">read/write</span></span></p></td>
<td><p><span data-ttu-id="a1088-336">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a1088-336">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-337"><a href="pagecount-property-ado.md">PageCount</a></span><span class="sxs-lookup"><span data-stu-id="a1088-337"><a href="pagecount-property-ado.md">PageCount</a></span></span></p></td>
<td><p><span data-ttu-id="a1088-338">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a1088-338">read/write</span></span></p></td>
<td><p><span data-ttu-id="a1088-339">Недоступен</span><span class="sxs-lookup"><span data-stu-id="a1088-339">not available</span></span></p></td>
<td><p><span data-ttu-id="a1088-340">только для чтения</span><span class="sxs-lookup"><span data-stu-id="a1088-340">read-only</span></span></p></td>
<td><p><span data-ttu-id="a1088-341">только для чтения</span><span class="sxs-lookup"><span data-stu-id="a1088-341">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-342"><a href="pagesize-property-ado.md">PageSize</a></span><span class="sxs-lookup"><span data-stu-id="a1088-342"><a href="pagesize-property-ado.md">PageSize</a></span></span></p></td>
<td><p><span data-ttu-id="a1088-343">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a1088-343">read/write</span></span></p></td>
<td><p><span data-ttu-id="a1088-344">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a1088-344">read/write</span></span></p></td>
<td><p><span data-ttu-id="a1088-345">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a1088-345">read/write</span></span></p></td>
<td><p><span data-ttu-id="a1088-346">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a1088-346">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-347"><a href="recordcount-property-ado.md">RecordCount</a></span><span class="sxs-lookup"><span data-stu-id="a1088-347"><a href="recordcount-property-ado.md">RecordCount</a></span></span></p></td>
<td><p><span data-ttu-id="a1088-348">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a1088-348">read/write</span></span></p></td>
<td><p><span data-ttu-id="a1088-349">Недоступен</span><span class="sxs-lookup"><span data-stu-id="a1088-349">not available</span></span></p></td>
<td><p><span data-ttu-id="a1088-350">только для чтения</span><span class="sxs-lookup"><span data-stu-id="a1088-350">read-only</span></span></p></td>
<td><p><span data-ttu-id="a1088-351">только для чтения</span><span class="sxs-lookup"><span data-stu-id="a1088-351">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-352"><a href="source-property-ado-recordset.md">Source</a></span><span class="sxs-lookup"><span data-stu-id="a1088-352"><a href="source-property-ado-recordset.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="a1088-353">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a1088-353">read/write</span></span></p></td>
<td><p><span data-ttu-id="a1088-354">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a1088-354">read/write</span></span></p></td>
<td><p><span data-ttu-id="a1088-355">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a1088-355">read/write</span></span></p></td>
<td><p><span data-ttu-id="a1088-356">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a1088-356">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-357"><a href="state-property-ado.md">State</a></span><span class="sxs-lookup"><span data-stu-id="a1088-357"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="a1088-358">только для чтения</span><span class="sxs-lookup"><span data-stu-id="a1088-358">read-only</span></span></p></td>
<td><p><span data-ttu-id="a1088-359">только для чтения</span><span class="sxs-lookup"><span data-stu-id="a1088-359">read-only</span></span></p></td>
<td><p><span data-ttu-id="a1088-360">только для чтения</span><span class="sxs-lookup"><span data-stu-id="a1088-360">read-only</span></span></p></td>
<td><p><span data-ttu-id="a1088-361">только для чтения</span><span class="sxs-lookup"><span data-stu-id="a1088-361">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-362"><a href="status-property-ado-recordset.md">Состояние</a></span><span class="sxs-lookup"><span data-stu-id="a1088-362"><a href="status-property-ado-recordset.md">Status</a></span></span></p></td>
<td><p><span data-ttu-id="a1088-363">только для чтения</span><span class="sxs-lookup"><span data-stu-id="a1088-363">read-only</span></span></p></td>
<td><p><span data-ttu-id="a1088-364">только для чтения</span><span class="sxs-lookup"><span data-stu-id="a1088-364">read-only</span></span></p></td>
<td><p><span data-ttu-id="a1088-365">только для чтения</span><span class="sxs-lookup"><span data-stu-id="a1088-365">read-only</span></span></p></td>
<td><p><span data-ttu-id="a1088-366">только для чтения</span><span class="sxs-lookup"><span data-stu-id="a1088-366">read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a1088-367">Свойства [AbsolutePosition](absoluteposition-property-ado.md) и [AbsolutePage](absolutepage-property-ado.md) доступны только для записи при использовании ADO с версии 1.0 поставщик Microsoft OLE DB для ODBC.</span><span class="sxs-lookup"><span data-stu-id="a1088-367">The [AbsolutePosition](absoluteposition-property-ado.md) and [AbsolutePage](absolutepage-property-ado.md) properties are write-only when ADO is used with version 1.0 of the Microsoft OLE DB Provider for ODBC.</span></span>

<span data-ttu-id="a1088-368">Доступность стандартных способов ADO **набора записей** :</span><span class="sxs-lookup"><span data-stu-id="a1088-368">Availability of standard ADO **Recordset** methods:</span></span>

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
<th><p><span data-ttu-id="a1088-369">Метод</span><span class="sxs-lookup"><span data-stu-id="a1088-369">Method</span></span></p></th>
<th><p><span data-ttu-id="a1088-370">ForwardOnly</span><span class="sxs-lookup"><span data-stu-id="a1088-370">ForwardOnly</span></span></p></th>
<th><p><span data-ttu-id="a1088-371">Динамическая группа</span><span class="sxs-lookup"><span data-stu-id="a1088-371">Dynamic</span></span></p></th>
<th><p><span data-ttu-id="a1088-372">Набор ключей</span><span class="sxs-lookup"><span data-stu-id="a1088-372">Keyset</span></span></p></th>
<th><p><span data-ttu-id="a1088-373">Статическое</span><span class="sxs-lookup"><span data-stu-id="a1088-373">Static</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a1088-374"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="a1088-374"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="a1088-375">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-375">Yes</span></span></p></td>
<td><p><span data-ttu-id="a1088-376">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-376">Yes</span></span></p></td>
<td><p><span data-ttu-id="a1088-377">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-377">Yes</span></span></p></td>
<td><p><span data-ttu-id="a1088-378">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-378">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-379"><a href="cancel-method-ado.md">Отмена</a></span><span class="sxs-lookup"><span data-stu-id="a1088-379"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="a1088-380">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-380">Yes</span></span></p></td>
<td><p><span data-ttu-id="a1088-381">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-381">Yes</span></span></p></td>
<td><p><span data-ttu-id="a1088-382">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-382">Yes</span></span></p></td>
<td><p><span data-ttu-id="a1088-383">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-383">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-384"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="a1088-384"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="a1088-385">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-385">Yes</span></span></p></td>
<td><p><span data-ttu-id="a1088-386">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-386">Yes</span></span></p></td>
<td><p><span data-ttu-id="a1088-387">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-387">Yes</span></span></p></td>
<td><p><span data-ttu-id="a1088-388">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-388">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-389"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="a1088-389"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="a1088-390">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-390">Yes</span></span></p></td>
<td><p><span data-ttu-id="a1088-391">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-391">Yes</span></span></p></td>
<td><p><span data-ttu-id="a1088-392">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-392">Yes</span></span></p></td>
<td><p><span data-ttu-id="a1088-393">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-393">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-394"><a href="clone-method-ado.md">Копия</a></span><span class="sxs-lookup"><span data-stu-id="a1088-394"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="a1088-395">Нет</span><span class="sxs-lookup"><span data-stu-id="a1088-395">No</span></span></p></td>
<td><p><span data-ttu-id="a1088-396">Нет</span><span class="sxs-lookup"><span data-stu-id="a1088-396">No</span></span></p></td>
<td><p><span data-ttu-id="a1088-397">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-397">Yes</span></span></p></td>
<td><p><span data-ttu-id="a1088-398">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-398">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-399"><a href="close-method-ado.md">Закрыть</a></span><span class="sxs-lookup"><span data-stu-id="a1088-399"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="a1088-400">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-400">Yes</span></span></p></td>
<td><p><span data-ttu-id="a1088-401">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-401">Yes</span></span></p></td>
<td><p><span data-ttu-id="a1088-402">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-402">Yes</span></span></p></td>
<td><p><span data-ttu-id="a1088-403">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-403">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-404"><a href="delete-method-ado-recordset.md">Delete</a></span><span class="sxs-lookup"><span data-stu-id="a1088-404"><a href="delete-method-ado-recordset.md">Delete</a></span></span></p></td>
<td><p><span data-ttu-id="a1088-405">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-405">Yes</span></span></p></td>
<td><p><span data-ttu-id="a1088-406">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-406">Yes</span></span></p></td>
<td><p><span data-ttu-id="a1088-407">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-407">Yes</span></span></p></td>
<td><p><span data-ttu-id="a1088-408">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-408">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-409"><a href="getrows-method-ado.md">Получение строк</a></span><span class="sxs-lookup"><span data-stu-id="a1088-409"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="a1088-410">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-410">Yes</span></span></p></td>
<td><p><span data-ttu-id="a1088-411">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-411">Yes</span></span></p></td>
<td><p><span data-ttu-id="a1088-412">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-412">Yes</span></span></p></td>
<td><p><span data-ttu-id="a1088-413">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-413">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-414"><a href="move-method-ado.md">Перемещение</a></span><span class="sxs-lookup"><span data-stu-id="a1088-414"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="a1088-415">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-415">Yes</span></span></p></td>
<td><p><span data-ttu-id="a1088-416">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-416">Yes</span></span></p></td>
<td><p><span data-ttu-id="a1088-417">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-417">Yes</span></span></p></td>
<td><p><span data-ttu-id="a1088-418">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-418">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-419"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span><span class="sxs-lookup"><span data-stu-id="a1088-419"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span></span></p></td>
<td><p><span data-ttu-id="a1088-420">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-420">Yes</span></span></p></td>
<td><p><span data-ttu-id="a1088-421">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-421">Yes</span></span></p></td>
<td><p><span data-ttu-id="a1088-422">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-422">Yes</span></span></p></td>
<td><p><span data-ttu-id="a1088-423">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-423">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-424"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span><span class="sxs-lookup"><span data-stu-id="a1088-424"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span></span></p></td>
<td><p><span data-ttu-id="a1088-425">Нет</span><span class="sxs-lookup"><span data-stu-id="a1088-425">No</span></span></p></td>
<td><p><span data-ttu-id="a1088-426">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-426">Yes</span></span></p></td>
<td><p><span data-ttu-id="a1088-427">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-427">Yes</span></span></p></td>
<td><p><span data-ttu-id="a1088-428">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-428">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-429"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span><span class="sxs-lookup"><span data-stu-id="a1088-429"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span></span></p></td>
<td><p><span data-ttu-id="a1088-430">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-430">Yes</span></span></p></td>
<td><p><span data-ttu-id="a1088-431">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-431">Yes</span></span></p></td>
<td><p><span data-ttu-id="a1088-432">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-432">Yes</span></span></p></td>
<td><p><span data-ttu-id="a1088-433">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-433">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-434"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span><span class="sxs-lookup"><span data-stu-id="a1088-434"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span></span></p></td>
<td><p><span data-ttu-id="a1088-435">Нет</span><span class="sxs-lookup"><span data-stu-id="a1088-435">No</span></span></p></td>
<td><p><span data-ttu-id="a1088-436">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-436">Yes</span></span></p></td>
<td><p><span data-ttu-id="a1088-437">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-437">Yes</span></span></p></td>
<td><p><span data-ttu-id="a1088-438">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-438">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-439"><a href="nextrecordset-method-ado.md">NextRecordset</a>\*</span><span class="sxs-lookup"><span data-stu-id="a1088-439"><a href="nextrecordset-method-ado.md">NextRecordset</a>\*</span></span></p></td>
<td><p><span data-ttu-id="a1088-440">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-440">Yes</span></span></p></td>
<td><p><span data-ttu-id="a1088-441">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-441">Yes</span></span></p></td>
<td><p><span data-ttu-id="a1088-442">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-442">Yes</span></span></p></td>
<td><p><span data-ttu-id="a1088-443">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-443">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-444"><a href="open-method-ado-recordset.md">Открытие</a></span><span class="sxs-lookup"><span data-stu-id="a1088-444"><a href="open-method-ado-recordset.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="a1088-445">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-445">Yes</span></span></p></td>
<td><p><span data-ttu-id="a1088-446">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-446">Yes</span></span></p></td>
<td><p><span data-ttu-id="a1088-447">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-447">Yes</span></span></p></td>
<td><p><span data-ttu-id="a1088-448">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-448">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-449"><a href="requery-method-ado.md">Обновление</a></span><span class="sxs-lookup"><span data-stu-id="a1088-449"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="a1088-450">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-450">Yes</span></span></p></td>
<td><p><span data-ttu-id="a1088-451">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-451">Yes</span></span></p></td>
<td><p><span data-ttu-id="a1088-452">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-452">Yes</span></span></p></td>
<td><p><span data-ttu-id="a1088-453">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-453">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-454"><a href="resync-method-ado.md">Выполнить повторную синхронизацию</a></span><span class="sxs-lookup"><span data-stu-id="a1088-454"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="a1088-455">Нет</span><span class="sxs-lookup"><span data-stu-id="a1088-455">No</span></span></p></td>
<td><p><span data-ttu-id="a1088-456">Нет</span><span class="sxs-lookup"><span data-stu-id="a1088-456">No</span></span></p></td>
<td><p><span data-ttu-id="a1088-457">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-457">Yes</span></span></p></td>
<td><p><span data-ttu-id="a1088-458">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-458">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-459"><a href="supports-method-ado.md">Поддерживает</a></span><span class="sxs-lookup"><span data-stu-id="a1088-459"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="a1088-460">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-460">Yes</span></span></p></td>
<td><p><span data-ttu-id="a1088-461">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-461">Yes</span></span></p></td>
<td><p><span data-ttu-id="a1088-462">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-462">Yes</span></span></p></td>
<td><p><span data-ttu-id="a1088-463">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-463">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-464"><a href="update-method-ado.md">обновление</a>.</span><span class="sxs-lookup"><span data-stu-id="a1088-464"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="a1088-465">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-465">Yes</span></span></p></td>
<td><p><span data-ttu-id="a1088-466">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-466">Yes</span></span></p></td>
<td><p><span data-ttu-id="a1088-467">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-467">Yes</span></span></p></td>
<td><p><span data-ttu-id="a1088-468">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-468">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-469"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="a1088-469"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="a1088-470">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-470">Yes</span></span></p></td>
<td><p><span data-ttu-id="a1088-471">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-471">Yes</span></span></p></td>
<td><p><span data-ttu-id="a1088-472">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-472">Yes</span></span></p></td>
<td><p><span data-ttu-id="a1088-473">Да</span><span class="sxs-lookup"><span data-stu-id="a1088-473">Yes</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a1088-474">\*Не поддерживается для баз данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="a1088-474">\*Not supported for Microsoft Access databases.</span></span>

## <a name="dynamic-properties"></a><span data-ttu-id="a1088-475">Динамические свойства</span><span class="sxs-lookup"><span data-stu-id="a1088-475">Dynamic Properties</span></span>

<span data-ttu-id="a1088-476">Поставщик Microsoft OLE DB для ODBC вставляет несколько динамических свойств в коллекцию **свойств** объектов неоткрытый [подключения](connection-object-ado.md), [записей](recordset-object-ado.md)и [команды](command-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="a1088-476">The Microsoft OLE DB Provider for ODBC inserts several dynamic properties into the **Properties** collection of the unopened [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md), and [Command](command-object-ado.md) objects.</span></span>

<span data-ttu-id="a1088-477">В таблицах ниже — это cross-index имен ADO и OLE DB для каждого динамического свойства.</span><span class="sxs-lookup"><span data-stu-id="a1088-477">The tables below are a cross-index of the ADO and OLE DB names for each dynamic property.</span></span> <span data-ttu-id="a1088-478">Справочник программиста OLE DB указано имя свойства ADO по слову «Описание».</span><span class="sxs-lookup"><span data-stu-id="a1088-478">The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description."</span></span> <span data-ttu-id="a1088-479">Дополнительные сведения об этих свойств можно найти в Справочник программиста OLE DB.</span><span class="sxs-lookup"><span data-stu-id="a1088-479">You can find more information about these properties in the OLE DB Programmer's Reference.</span></span> <span data-ttu-id="a1088-480">Поиск имени свойства OLE DB в индексе или просмотреть приложение C: OLE DB свойства.</span><span class="sxs-lookup"><span data-stu-id="a1088-480">Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span></span>

## <a name="connection-dynamic-properties"></a><span data-ttu-id="a1088-481">Динамические свойства подключения</span><span class="sxs-lookup"><span data-stu-id="a1088-481">Connection Dynamic Properties</span></span>

<span data-ttu-id="a1088-482">Коллекция **Properties** объект **подключения** добавляются следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a1088-482">The following properties are added to the **Connection** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a1088-483">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="a1088-483">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="a1088-484">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="a1088-484">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a1088-485">Активных сеансов</span><span class="sxs-lookup"><span data-stu-id="a1088-485">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="a1088-486">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="a1088-486">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-487">Прерывание Asynchable</span><span class="sxs-lookup"><span data-stu-id="a1088-487">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="a1088-488">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="a1088-488">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-489">Зафиксировать Asynchable</span><span class="sxs-lookup"><span data-stu-id="a1088-489">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="a1088-490">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="a1088-490">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-491">Уровни изоляции автоматической фиксации</span><span class="sxs-lookup"><span data-stu-id="a1088-491">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="a1088-492">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="a1088-492">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-493">Расположение каталога</span><span class="sxs-lookup"><span data-stu-id="a1088-493">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="a1088-494">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="a1088-494">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-495">Каталог терминов</span><span class="sxs-lookup"><span data-stu-id="a1088-495">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="a1088-496">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="a1088-496">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-497">Определение столбца</span><span class="sxs-lookup"><span data-stu-id="a1088-497">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="a1088-498">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="a1088-498">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-499">Время ожидания подключения</span><span class="sxs-lookup"><span data-stu-id="a1088-499">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="a1088-500">DBPROP_INIT_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="a1088-500">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-501">Текущий каталог</span><span class="sxs-lookup"><span data-stu-id="a1088-501">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="a1088-502">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="a1088-502">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-503">Источник данных</span><span class="sxs-lookup"><span data-stu-id="a1088-503">Data Source</span></span></p></td>
<td><p><span data-ttu-id="a1088-504">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="a1088-504">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-505">Имя источника данных</span><span class="sxs-lookup"><span data-stu-id="a1088-505">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="a1088-506">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="a1088-506">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-507">Модель потоков объекта источника данных</span><span class="sxs-lookup"><span data-stu-id="a1088-507">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="a1088-508">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="a1088-508">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-509">Имя СУБД</span><span class="sxs-lookup"><span data-stu-id="a1088-509">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="a1088-510">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="a1088-510">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-511">Версия СУБД</span><span class="sxs-lookup"><span data-stu-id="a1088-511">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="a1088-512">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="a1088-512">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-513">Расширенные свойства</span><span class="sxs-lookup"><span data-stu-id="a1088-513">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="a1088-514">DBPROP_INIT_PROVIDERSTRING</span><span class="sxs-lookup"><span data-stu-id="a1088-514">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-515">ГРУППИРОВКА по поддержке</span><span class="sxs-lookup"><span data-stu-id="a1088-515">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="a1088-516">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="a1088-516">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-517">Поддержка разнородных таблиц</span><span class="sxs-lookup"><span data-stu-id="a1088-517">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="a1088-518">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="a1088-518">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-519">Идентификатор регистра</span><span class="sxs-lookup"><span data-stu-id="a1088-519">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="a1088-520">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="a1088-520">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-521">Исходный каталог</span><span class="sxs-lookup"><span data-stu-id="a1088-521">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="a1088-522">DBPROP_INIT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="a1088-522">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-523">Уровни изоляции</span><span class="sxs-lookup"><span data-stu-id="a1088-523">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="a1088-524">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="a1088-524">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-525">Хранение изоляции</span><span class="sxs-lookup"><span data-stu-id="a1088-525">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="a1088-526">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="a1088-526">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-527">Идентификатор языка</span><span class="sxs-lookup"><span data-stu-id="a1088-527">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="a1088-528">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="a1088-528">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-529">Location</span><span class="sxs-lookup"><span data-stu-id="a1088-529">Location</span></span></p></td>
<td><p><span data-ttu-id="a1088-530">DBPROP_INIT_LOCATION</span><span class="sxs-lookup"><span data-stu-id="a1088-530">DBPROP_INIT_LOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-531">Максимальный размер индекса</span><span class="sxs-lookup"><span data-stu-id="a1088-531">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="a1088-532">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="a1088-532">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-533">Максимальный размер строки</span><span class="sxs-lookup"><span data-stu-id="a1088-533">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="a1088-534">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="a1088-534">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-535">Максимальный размер строки включает в себя больших двоичных ОБЪЕКТОВ</span><span class="sxs-lookup"><span data-stu-id="a1088-535">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="a1088-536">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="a1088-536">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-537">Максимальная таблиц в Выбор</span><span class="sxs-lookup"><span data-stu-id="a1088-537">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="a1088-538">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="a1088-538">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-539">Mode</span><span class="sxs-lookup"><span data-stu-id="a1088-539">Mode</span></span></p></td>
<td><p><span data-ttu-id="a1088-540">DBPROP_INIT_MODE</span><span class="sxs-lookup"><span data-stu-id="a1088-540">DBPROP_INIT_MODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-541">Несколько наборов параметров</span><span class="sxs-lookup"><span data-stu-id="a1088-541">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="a1088-542">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="a1088-542">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-543">Несколько результатов</span><span class="sxs-lookup"><span data-stu-id="a1088-543">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="a1088-544">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="a1088-544">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-545">Несколько объектов хранения</span><span class="sxs-lookup"><span data-stu-id="a1088-545">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="a1088-546">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="a1088-546">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-547">Обновление нескольких таблицы</span><span class="sxs-lookup"><span data-stu-id="a1088-547">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="a1088-548">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="a1088-548">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-549">Порядок сортировки значений NULL</span><span class="sxs-lookup"><span data-stu-id="a1088-549">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="a1088-550">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="a1088-550">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-551">Поведение NULL объединения</span><span class="sxs-lookup"><span data-stu-id="a1088-551">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="a1088-552">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="a1088-552">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-553">Службы OLE DB</span><span class="sxs-lookup"><span data-stu-id="a1088-553">OLE DB Services</span></span></p></td>
<td><p><span data-ttu-id="a1088-554">DBPROP_INIT_OLEDBSERVICES, УСТАНОВИТЬ</span><span class="sxs-lookup"><span data-stu-id="a1088-554">DBPROP_INIT_OLEDBSERVICES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-555">Версия OLE DB</span><span class="sxs-lookup"><span data-stu-id="a1088-555">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="a1088-556">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="a1088-556">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-557">Поддержка OLE-объектов</span><span class="sxs-lookup"><span data-stu-id="a1088-557">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="a1088-558">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="a1088-558">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-559">Поддержка открытых наборов строк</span><span class="sxs-lookup"><span data-stu-id="a1088-559">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="a1088-560">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="a1088-560">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-561">ORDER BY столбцы в списке Select</span><span class="sxs-lookup"><span data-stu-id="a1088-561">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="a1088-562">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="a1088-562">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-563">Выходной параметр доступности</span><span class="sxs-lookup"><span data-stu-id="a1088-563">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="a1088-564">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="a1088-564">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-565">Пароль</span><span class="sxs-lookup"><span data-stu-id="a1088-565">Password</span></span></p></td>
<td><p><span data-ttu-id="a1088-566">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="a1088-566">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-567">Передайте с указанные методы</span><span class="sxs-lookup"><span data-stu-id="a1088-567">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="a1088-568">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="a1088-568">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-569">Сохранять сведения о безопасности</span><span class="sxs-lookup"><span data-stu-id="a1088-569">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="a1088-570">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span><span class="sxs-lookup"><span data-stu-id="a1088-570">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-571">Тип сохраняемого идентификатора</span><span class="sxs-lookup"><span data-stu-id="a1088-571">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="a1088-572">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="a1088-572">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-573">Подготовка поведение аварийное завершение</span><span class="sxs-lookup"><span data-stu-id="a1088-573">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="a1088-574">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="a1088-574">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-575">Подготовка поведение выделения</span><span class="sxs-lookup"><span data-stu-id="a1088-575">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="a1088-576">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="a1088-576">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-577">Процедура терминов</span><span class="sxs-lookup"><span data-stu-id="a1088-577">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="a1088-578">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="a1088-578">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-579">Запрос</span><span class="sxs-lookup"><span data-stu-id="a1088-579">Prompt</span></span></p></td>
<td><p><span data-ttu-id="a1088-580">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="a1088-580">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-581">Понятное имя поставщика</span><span class="sxs-lookup"><span data-stu-id="a1088-581">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="a1088-582">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="a1088-582">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-583">Имя поставщика</span><span class="sxs-lookup"><span data-stu-id="a1088-583">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="a1088-584">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="a1088-584">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-585">Версия поставщика</span><span class="sxs-lookup"><span data-stu-id="a1088-585">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="a1088-586">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="a1088-586">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-587">Источник данных только для чтения</span><span class="sxs-lookup"><span data-stu-id="a1088-587">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="a1088-588">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="a1088-588">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-589">Преобразование строк на команду</span><span class="sxs-lookup"><span data-stu-id="a1088-589">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="a1088-590">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="a1088-590">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-591">Схема терминов</span><span class="sxs-lookup"><span data-stu-id="a1088-591">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="a1088-592">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="a1088-592">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-593">Об использовании схемы</span><span class="sxs-lookup"><span data-stu-id="a1088-593">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="a1088-594">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="a1088-594">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-595">Поддержка SQL</span><span class="sxs-lookup"><span data-stu-id="a1088-595">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="a1088-596">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="a1088-596">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-597">Структурированное хранилище</span><span class="sxs-lookup"><span data-stu-id="a1088-597">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="a1088-598">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="a1088-598">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-599">Поддержка вложенного запроса</span><span class="sxs-lookup"><span data-stu-id="a1088-599">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="a1088-600">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="a1088-600">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-601">В таблице терминов</span><span class="sxs-lookup"><span data-stu-id="a1088-601">Table Term</span></span></p></td>
<td><p><span data-ttu-id="a1088-602">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="a1088-602">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-603">Транзакций DDL</span><span class="sxs-lookup"><span data-stu-id="a1088-603">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="a1088-604">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="a1088-604">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-605">Идентификатор пользователя</span><span class="sxs-lookup"><span data-stu-id="a1088-605">User ID</span></span></p></td>
<td><p><span data-ttu-id="a1088-606">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="a1088-606">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-607">Имя пользователя</span><span class="sxs-lookup"><span data-stu-id="a1088-607">User Name</span></span></p></td>
<td><p><span data-ttu-id="a1088-608">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="a1088-608">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-609">Дескриптор окна</span><span class="sxs-lookup"><span data-stu-id="a1088-609">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="a1088-610">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="a1088-610">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a><span data-ttu-id="a1088-611">Свойства динамической набора записей</span><span class="sxs-lookup"><span data-stu-id="a1088-611">Recordset Dynamic Properties</span></span>

<span data-ttu-id="a1088-612">Следующие свойства добавляются в коллекцию **свойств** объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="a1088-612">The following properties are added to the **Recordset** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a1088-613">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="a1088-613">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="a1088-614">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="a1088-614">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a1088-615">Порядок доступа</span><span class="sxs-lookup"><span data-stu-id="a1088-615">Access Order</span></span></p></td>
<td><p><span data-ttu-id="a1088-616">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="a1088-616">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-617">Блокировка объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="a1088-617">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="a1088-618">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="a1088-618">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-619">Тип закладки</span><span class="sxs-lookup"><span data-stu-id="a1088-619">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="a1088-620">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="a1088-620">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-621">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="a1088-621">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="a1088-622">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="a1088-622">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-623">Изменение вставленных строк</span><span class="sxs-lookup"><span data-stu-id="a1088-623">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="a1088-624">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="a1088-624">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-625">Права доступа столбца</span><span class="sxs-lookup"><span data-stu-id="a1088-625">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="a1088-626">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="a1088-626">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-627">Столбец набор уведомлений</span><span class="sxs-lookup"><span data-stu-id="a1088-627">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="a1088-628">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="a1088-628">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-629">Отложенное обновление объекта хранения</span><span class="sxs-lookup"><span data-stu-id="a1088-629">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="a1088-630">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="a1088-630">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-631">Выборку</span><span class="sxs-lookup"><span data-stu-id="a1088-631">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="a1088-632">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="a1088-632">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-633">Хранение строк</span><span class="sxs-lookup"><span data-stu-id="a1088-633">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="a1088-634">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="a1088-634">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-635">IAccessor</span><span class="sxs-lookup"><span data-stu-id="a1088-635">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="a1088-636">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="a1088-636">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-637">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="a1088-637">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="a1088-638">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="a1088-638">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-639">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="a1088-639">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="a1088-640">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="a1088-640">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-641">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="a1088-641">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="a1088-642">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="a1088-642">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-643">IConvertType</span><span class="sxs-lookup"><span data-stu-id="a1088-643">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="a1088-644">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="a1088-644">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-645">Немобильные строки</span><span class="sxs-lookup"><span data-stu-id="a1088-645">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="a1088-646">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="a1088-646">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-647">IRowset</span><span class="sxs-lookup"><span data-stu-id="a1088-647">IRowset</span></span></p></td>
<td><p><span data-ttu-id="a1088-648">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="a1088-648">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-649">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="a1088-649">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="a1088-650">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="a1088-650">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-651">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="a1088-651">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="a1088-652">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="a1088-652">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-653">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="a1088-653">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="a1088-654">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="a1088-654">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-655">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="a1088-655">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="a1088-656">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="a1088-656">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-657">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="a1088-657">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-658">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="a1088-658">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="a1088-659">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="a1088-659">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-660">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="a1088-660">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="a1088-661">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="a1088-661">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-662">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="a1088-662">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="a1088-663">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="a1088-663">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-664">Литерал закладки</span><span class="sxs-lookup"><span data-stu-id="a1088-664">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="a1088-665">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="a1088-665">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-666">Удостоверение литерала строки</span><span class="sxs-lookup"><span data-stu-id="a1088-666">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="a1088-667">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="a1088-667">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-668">Максимальное число открытых строк</span><span class="sxs-lookup"><span data-stu-id="a1088-668">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="a1088-669">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="a1088-669">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-670">Максимум ожидающие строк</span><span class="sxs-lookup"><span data-stu-id="a1088-670">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="a1088-671">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="a1088-671">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-672">Максимальное число строк</span><span class="sxs-lookup"><span data-stu-id="a1088-672">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="a1088-673">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="a1088-673">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-674">Степень детализации уведомлений</span><span class="sxs-lookup"><span data-stu-id="a1088-674">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="a1088-675">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="a1088-675">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-676">Этапы уведомлений</span><span class="sxs-lookup"><span data-stu-id="a1088-676">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="a1088-677">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="a1088-677">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-678">Объекты в транзакции</span><span class="sxs-lookup"><span data-stu-id="a1088-678">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="a1088-679">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="a1088-679">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-680">Видны собственные изменения</span><span class="sxs-lookup"><span data-stu-id="a1088-680">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="a1088-681">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="a1088-681">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-682">Видны собственные операции вставки</span><span class="sxs-lookup"><span data-stu-id="a1088-682">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="a1088-683">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="a1088-683">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-684">Сохранять при аварийном завершении</span><span class="sxs-lookup"><span data-stu-id="a1088-684">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="a1088-685">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="a1088-685">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-686">Сохранять при фиксации</span><span class="sxs-lookup"><span data-stu-id="a1088-686">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="a1088-687">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="a1088-687">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-688">Быстрый перезапуск</span><span class="sxs-lookup"><span data-stu-id="a1088-688">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="a1088-689">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="a1088-689">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-690">Повторные события</span><span class="sxs-lookup"><span data-stu-id="a1088-690">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="a1088-691">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="a1088-691">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-692">Удаление удаленных строк</span><span class="sxs-lookup"><span data-stu-id="a1088-692">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="a1088-693">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="a1088-693">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-694">Сообщить о нескольких изменений</span><span class="sxs-lookup"><span data-stu-id="a1088-694">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="a1088-695">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="a1088-695">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-696">Вернуть ожидающие вставки</span><span class="sxs-lookup"><span data-stu-id="a1088-696">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="a1088-697">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="a1088-697">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-698">Удалить строку уведомлений</span><span class="sxs-lookup"><span data-stu-id="a1088-698">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="a1088-699">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="a1088-699">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-700">Строка первого уведомления об изменении</span><span class="sxs-lookup"><span data-stu-id="a1088-700">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="a1088-701">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="a1088-701">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-702">Строка вставки уведомлений</span><span class="sxs-lookup"><span data-stu-id="a1088-702">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="a1088-703">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="a1088-703">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-704">Привилегии строки</span><span class="sxs-lookup"><span data-stu-id="a1088-704">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="a1088-705">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="a1088-705">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-706">Уведомления о повторной синхронизации строки</span><span class="sxs-lookup"><span data-stu-id="a1088-706">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="a1088-707">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="a1088-707">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-708">Строка, потоковой модели</span><span class="sxs-lookup"><span data-stu-id="a1088-708">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="a1088-709">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="a1088-709">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-710">Уведомление об изменении отмены строки</span><span class="sxs-lookup"><span data-stu-id="a1088-710">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="a1088-711">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="a1088-711">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-712">Строка отмены Delete уведомлений</span><span class="sxs-lookup"><span data-stu-id="a1088-712">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="a1088-713">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="a1088-713">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-714">Вставка отмены строки уведомлений</span><span class="sxs-lookup"><span data-stu-id="a1088-714">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="a1088-715">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="a1088-715">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-716">Уведомление об обновлении строки</span><span class="sxs-lookup"><span data-stu-id="a1088-716">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="a1088-717">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="a1088-717">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-718">Уведомление об изменении положения строк выборки</span><span class="sxs-lookup"><span data-stu-id="a1088-718">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="a1088-719">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="a1088-719">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-720">Уведомление о выпуске набора строк</span><span class="sxs-lookup"><span data-stu-id="a1088-720">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="a1088-721">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="a1088-721">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-722">Прокрутка назад</span><span class="sxs-lookup"><span data-stu-id="a1088-722">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="a1088-723">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="a1088-723">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-724">Пропустить удаленных закладки</span><span class="sxs-lookup"><span data-stu-id="a1088-724">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="a1088-725">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="a1088-725">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-726">Строка строгого удостоверений</span><span class="sxs-lookup"><span data-stu-id="a1088-726">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="a1088-727">DBPROP_STRONGITDENTITY</span><span class="sxs-lookup"><span data-stu-id="a1088-727">DBPROP_STRONGITDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-728">Уникальные строки</span><span class="sxs-lookup"><span data-stu-id="a1088-728">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="a1088-729">DBPROP_UNIQUEROWS</span><span class="sxs-lookup"><span data-stu-id="a1088-729">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-730">Возможности обновления</span><span class="sxs-lookup"><span data-stu-id="a1088-730">Updatability</span></span></p></td>
<td><p><span data-ttu-id="a1088-731">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="a1088-731">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-732">Использование закладок</span><span class="sxs-lookup"><span data-stu-id="a1088-732">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="a1088-733">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="a1088-733">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a><span data-ttu-id="a1088-734">Динамические свойства команды</span><span class="sxs-lookup"><span data-stu-id="a1088-734">Command Dynamic Properties</span></span>

<span data-ttu-id="a1088-735">Следующие свойства добавляются в коллекцию **свойств** объекта **команды** .</span><span class="sxs-lookup"><span data-stu-id="a1088-735">The following properties are added to the **Command** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a1088-736">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="a1088-736">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="a1088-737">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="a1088-737">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a1088-738">Порядок доступа</span><span class="sxs-lookup"><span data-stu-id="a1088-738">Access Order</span></span></p></td>
<td><p><span data-ttu-id="a1088-739">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="a1088-739">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-740">Блокировка объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="a1088-740">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="a1088-741">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="a1088-741">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-742">Тип закладки</span><span class="sxs-lookup"><span data-stu-id="a1088-742">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="a1088-743">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="a1088-743">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-744">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="a1088-744">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="a1088-745">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="a1088-745">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-746">Изменение вставленных строк</span><span class="sxs-lookup"><span data-stu-id="a1088-746">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="a1088-747">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="a1088-747">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-748">Права доступа столбца</span><span class="sxs-lookup"><span data-stu-id="a1088-748">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="a1088-749">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="a1088-749">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-750">Столбец набор уведомлений</span><span class="sxs-lookup"><span data-stu-id="a1088-750">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="a1088-751">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="a1088-751">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-752">Отложенное обновление объекта хранения</span><span class="sxs-lookup"><span data-stu-id="a1088-752">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="a1088-753">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="a1088-753">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-754">Выборку</span><span class="sxs-lookup"><span data-stu-id="a1088-754">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="a1088-755">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="a1088-755">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-756">Хранение строк</span><span class="sxs-lookup"><span data-stu-id="a1088-756">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="a1088-757">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="a1088-757">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-758">IAccessor</span><span class="sxs-lookup"><span data-stu-id="a1088-758">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="a1088-759">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="a1088-759">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-760">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="a1088-760">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="a1088-761">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="a1088-761">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-762">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="a1088-762">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="a1088-763">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="a1088-763">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-764">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="a1088-764">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="a1088-765">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="a1088-765">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-766">IConvertType</span><span class="sxs-lookup"><span data-stu-id="a1088-766">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="a1088-767">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="a1088-767">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-768">Немобильные строки</span><span class="sxs-lookup"><span data-stu-id="a1088-768">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="a1088-769">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="a1088-769">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-770">IRowset</span><span class="sxs-lookup"><span data-stu-id="a1088-770">IRowset</span></span></p></td>
<td><p><span data-ttu-id="a1088-771">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="a1088-771">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-772">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="a1088-772">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="a1088-773">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="a1088-773">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-774">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="a1088-774">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="a1088-775">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="a1088-775">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-776">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="a1088-776">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="a1088-777">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="a1088-777">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-778">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="a1088-778">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="a1088-779">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="a1088-779">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-780">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="a1088-780">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-781">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="a1088-781">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="a1088-782">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="a1088-782">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-783">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="a1088-783">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="a1088-784">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="a1088-784">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-785">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="a1088-785">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="a1088-786">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="a1088-786">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-787">Литерал закладки</span><span class="sxs-lookup"><span data-stu-id="a1088-787">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="a1088-788">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="a1088-788">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-789">Удостоверение литерала строки</span><span class="sxs-lookup"><span data-stu-id="a1088-789">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="a1088-790">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="a1088-790">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-791">Максимальное число открытых строк</span><span class="sxs-lookup"><span data-stu-id="a1088-791">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="a1088-792">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="a1088-792">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-793">Максимум ожидающие строк</span><span class="sxs-lookup"><span data-stu-id="a1088-793">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="a1088-794">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="a1088-794">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-795">Максимальное число строк</span><span class="sxs-lookup"><span data-stu-id="a1088-795">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="a1088-796">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="a1088-796">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-797">Степень детализации уведомлений</span><span class="sxs-lookup"><span data-stu-id="a1088-797">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="a1088-798">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="a1088-798">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-799">Этапы уведомлений</span><span class="sxs-lookup"><span data-stu-id="a1088-799">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="a1088-800">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="a1088-800">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-801">Объекты в транзакции</span><span class="sxs-lookup"><span data-stu-id="a1088-801">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="a1088-802">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="a1088-802">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-803">Видны собственные изменения</span><span class="sxs-lookup"><span data-stu-id="a1088-803">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="a1088-804">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="a1088-804">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-805">Видны собственные операции вставки</span><span class="sxs-lookup"><span data-stu-id="a1088-805">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="a1088-806">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="a1088-806">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-807">Сохранять при аварийном завершении</span><span class="sxs-lookup"><span data-stu-id="a1088-807">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="a1088-808">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="a1088-808">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-809">Сохранять при фиксации</span><span class="sxs-lookup"><span data-stu-id="a1088-809">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="a1088-810">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="a1088-810">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-811">Быстрый перезапуск</span><span class="sxs-lookup"><span data-stu-id="a1088-811">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="a1088-812">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="a1088-812">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-813">Повторные события</span><span class="sxs-lookup"><span data-stu-id="a1088-813">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="a1088-814">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="a1088-814">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-815">Удаление удаленных строк</span><span class="sxs-lookup"><span data-stu-id="a1088-815">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="a1088-816">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="a1088-816">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-817">Сообщить о нескольких изменений</span><span class="sxs-lookup"><span data-stu-id="a1088-817">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="a1088-818">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="a1088-818">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-819">Вернуть ожидающие вставки</span><span class="sxs-lookup"><span data-stu-id="a1088-819">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="a1088-820">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="a1088-820">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-821">Удалить строку уведомлений</span><span class="sxs-lookup"><span data-stu-id="a1088-821">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="a1088-822">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="a1088-822">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-823">Строка первого уведомления об изменении</span><span class="sxs-lookup"><span data-stu-id="a1088-823">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="a1088-824">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="a1088-824">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-825">Строка вставки уведомлений</span><span class="sxs-lookup"><span data-stu-id="a1088-825">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="a1088-826">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="a1088-826">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-827">Привилегии строки</span><span class="sxs-lookup"><span data-stu-id="a1088-827">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="a1088-828">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="a1088-828">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-829">Уведомления о повторной синхронизации строки</span><span class="sxs-lookup"><span data-stu-id="a1088-829">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="a1088-830">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="a1088-830">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-831">Строка, потоковой модели</span><span class="sxs-lookup"><span data-stu-id="a1088-831">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="a1088-832">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="a1088-832">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-833">Уведомление об изменении отмены строки</span><span class="sxs-lookup"><span data-stu-id="a1088-833">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="a1088-834">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="a1088-834">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-835">Строка отмены Delete уведомлений</span><span class="sxs-lookup"><span data-stu-id="a1088-835">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="a1088-836">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="a1088-836">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-837">Вставка отмены строки уведомлений</span><span class="sxs-lookup"><span data-stu-id="a1088-837">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="a1088-838">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="a1088-838">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-839">Уведомление об обновлении строки</span><span class="sxs-lookup"><span data-stu-id="a1088-839">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="a1088-840">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="a1088-840">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-841">Уведомление об изменении положения строк выборки</span><span class="sxs-lookup"><span data-stu-id="a1088-841">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="a1088-842">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="a1088-842">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-843">Уведомление о выпуске набора строк</span><span class="sxs-lookup"><span data-stu-id="a1088-843">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="a1088-844">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="a1088-844">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-845">Прокрутка назад</span><span class="sxs-lookup"><span data-stu-id="a1088-845">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="a1088-846">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="a1088-846">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-847">Пропустить удаленных закладки</span><span class="sxs-lookup"><span data-stu-id="a1088-847">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="a1088-848">DBPROP_BOOKMARKSKIP</span><span class="sxs-lookup"><span data-stu-id="a1088-848">DBPROP_BOOKMARKSKIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-849">Строка строгого удостоверений</span><span class="sxs-lookup"><span data-stu-id="a1088-849">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="a1088-850">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="a1088-850">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1088-851">Возможности обновления</span><span class="sxs-lookup"><span data-stu-id="a1088-851">Updatability</span></span></p></td>
<td><p><span data-ttu-id="a1088-852">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="a1088-852">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1088-853">Использование закладок</span><span class="sxs-lookup"><span data-stu-id="a1088-853">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="a1088-854">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="a1088-854">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="a1088-855">См. также</span><span class="sxs-lookup"><span data-stu-id="a1088-855">See also</span></span>

<span data-ttu-id="a1088-856">Для получения дополнительных сведений о реализации и функциональным сведения о поставщик Microsoft OLE DB для ODBC обратитесь к [OLE DB Руководство программиста](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85)) или посетите [Центр разработчиков данных платформы](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).</span><span class="sxs-lookup"><span data-stu-id="a1088-856">For details regarding specific implementation and functional information about the Microsoft OLE DB Provider for ODBC, consult the [OLE DB Programmer's Guide](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85)) or visit the [Data Platform Developer Center](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).</span></span>

