---
title: Поставщик Microsoft OLE DB для Microsoft Jet
TOCTitle: Microsoft OLE DB Provider for Microsoft Jet
ms:assetid: 4a210d72-8c90-aa7c-4621-1a555a30a2d2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249228(v=office.15)
ms:contentKeyID: 48544660
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9b4f1c46b390e1f059e57f3b7a70fc667da4b09b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288927"
---
# <a name="microsoft-ole-db-provider-for-microsoft-jet"></a><span data-ttu-id="8f57c-102">Поставщик Microsoft OLE DB для Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="8f57c-102">Microsoft OLE DB Provider for Microsoft Jet</span></span>

<span data-ttu-id="8f57c-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8f57c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8f57c-104">Поставщик OLE DB для Microsoft Jet позволяет ADO получать доступ к базам данных Microsoft Jet.</span><span class="sxs-lookup"><span data-stu-id="8f57c-104">The OLE DB Provider for Microsoft Jet allows ADO to access Microsoft Jet databases.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="8f57c-105">Параметры строки подключения</span><span class="sxs-lookup"><span data-stu-id="8f57c-105">Connection String Parameters</span></span>

<span data-ttu-id="8f57c-106">Чтобы подключиться к этому поставщику, установите для аргумента *Provider* свойства [ConnectionString:](connectionstring-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="8f57c-106">To connect to this provider, set the *Provider* argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```vb 
 
Microsoft.Jet.OLEDB.4.0 
```

<span data-ttu-id="8f57c-107">При [чтении свойства Provider](provider-property-ado.md) также будет возвращена эта строка.</span><span class="sxs-lookup"><span data-stu-id="8f57c-107">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="8f57c-108">Типичная строка подключения</span><span class="sxs-lookup"><span data-stu-id="8f57c-108">Typical Connection String</span></span>

<span data-ttu-id="8f57c-109">Типичная строка подключения для этого поставщика:</span><span class="sxs-lookup"><span data-stu-id="8f57c-109">A typical connection string for this provider is:</span></span>

```vb 
 
"Provider=Microsoft.Jet.OLEDB.4.0;Data Source=databaseName;User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="8f57c-110">Строка состоит из таких ключевых слов:</span><span class="sxs-lookup"><span data-stu-id="8f57c-110">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8f57c-111">Ключевое слово</span><span class="sxs-lookup"><span data-stu-id="8f57c-111">Keyword</span></span></p></th>
<th><p><span data-ttu-id="8f57c-112">Описание</span><span class="sxs-lookup"><span data-stu-id="8f57c-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-113"><strong>Поставщик</strong></span><span class="sxs-lookup"><span data-stu-id="8f57c-113"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="8f57c-114">Указывает поставщика OLE DB для Microsoft Jet.</span><span class="sxs-lookup"><span data-stu-id="8f57c-114">Specifies the OLE DB Provider for Microsoft Jet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-115"><strong>Источник данных</strong></span><span class="sxs-lookup"><span data-stu-id="8f57c-115"><strong>Data Source</strong></span></span></p></td>
<td><p><span data-ttu-id="8f57c-116">Указывает путь к базе данных и имя файла (например, c:\Northwind.mdb).</span><span class="sxs-lookup"><span data-stu-id="8f57c-116">Specifies the database path and file name (for example, c:\Northwind.mdb).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-117"><strong>Идентификатор пользователя</strong></span><span class="sxs-lookup"><span data-stu-id="8f57c-117"><strong>User ID</strong></span></span></p></td>
<td><p><span data-ttu-id="8f57c-118">Задает имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="8f57c-118">Specifies the user name.</span></span> <span data-ttu-id="8f57c-119">Если это ключевое слово не указано, по умолчанию используется &quot; строка &quot; admin.</span><span class="sxs-lookup"><span data-stu-id="8f57c-119">If this keyword is not specified, the string, &quot;admin&quot;, is used by default.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-120"><strong>Password</strong></span><span class="sxs-lookup"><span data-stu-id="8f57c-120"><strong>Password</strong></span></span></p></td>
<td><p><span data-ttu-id="8f57c-121">Указывает пароль пользователя.</span><span class="sxs-lookup"><span data-stu-id="8f57c-121">Specifies the user password.</span></span> <span data-ttu-id="8f57c-122">Если это ключевое слово не указано, по умолчанию используется пустая строка ( &quot; &quot; ).</span><span class="sxs-lookup"><span data-stu-id="8f57c-122">If this keyword is not specified, the empty string (&quot;&quot;), is used by default.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-connection-parameters"></a><span data-ttu-id="8f57c-123">Provider-Specific connection parameters</span><span class="sxs-lookup"><span data-stu-id="8f57c-123">Provider-Specific Connection Parameters</span></span>

<span data-ttu-id="8f57c-124">Поставщик OLE DB для Microsoft Jet поддерживает несколько динамических свойств, в дополнение к определенным ADO.</span><span class="sxs-lookup"><span data-stu-id="8f57c-124">The OLE DB Provider for Microsoft Jet supports several provider-specific dynamic properties in addition to those defined by ADO.</span></span> <span data-ttu-id="8f57c-125">Как и все другие параметры **Connection,** их можно установить с помощью коллекции **свойств** объекта **Connection** или в составе строки подключения.</span><span class="sxs-lookup"><span data-stu-id="8f57c-125">As with all other **Connection** parameters, they can be set via the **Connection** object's **Properties** collection or as part of the connection string.</span></span>

<span data-ttu-id="8f57c-126">В следующей таблице перечислены эти свойства с соответствующим именем свойства OLE DB в скобки.</span><span class="sxs-lookup"><span data-stu-id="8f57c-126">The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8f57c-127">Параметр</span><span class="sxs-lookup"><span data-stu-id="8f57c-127">Parameter</span></span></p></th>
<th><p><span data-ttu-id="8f57c-128">Описание</span><span class="sxs-lookup"><span data-stu-id="8f57c-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-129">Jet OLEDB:Compact Reclaimed Space Amount</span><span class="sxs-lookup"><span data-stu-id="8f57c-129">Jet OLEDB:Compact Reclaimed Space Amount</span></span><br />
<span data-ttu-id="8f57c-130">(DBPROP_JETOLEDB_COMPACTFREESPACESIZE)</span><span class="sxs-lookup"><span data-stu-id="8f57c-130">(DBPROP_JETOLEDB_COMPACTFREESPACESIZE)</span></span></p></td>
<td><p><span data-ttu-id="8f57c-131">Указывает приблизительное количество пространства вбайтах, которое можно освободить, сжатие базы данных.</span><span class="sxs-lookup"><span data-stu-id="8f57c-131">Indicates an estimate of the amount of space, in bytes, that can be reclaimed by compacting the database.</span></span> <span data-ttu-id="8f57c-132">Это значение является допустимым только после того, как установлено подключение к базе данных.</span><span class="sxs-lookup"><span data-stu-id="8f57c-132">This value is only valid after a database connection has been established.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-133">Jet OLEDB:Connection Control</span><span class="sxs-lookup"><span data-stu-id="8f57c-133">Jet OLEDB:Connection Control</span></span><br />
<span data-ttu-id="8f57c-134">(DBPROP_JETOLEDB_CONNECTIONCONTROL)</span><span class="sxs-lookup"><span data-stu-id="8f57c-134">(DBPROP_JETOLEDB_CONNECTIONCONTROL)</span></span></p></td>
<td><p><span data-ttu-id="8f57c-135">Указывает, могут ли пользователи подключаться к базе данных.</span><span class="sxs-lookup"><span data-stu-id="8f57c-135">Indicates whether users can connect to the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-136">Jet OLEDB:Создание системной базы данных</span><span class="sxs-lookup"><span data-stu-id="8f57c-136">Jet OLEDB:Create System Database</span></span><br />
<span data-ttu-id="8f57c-137">(DBPROP_JETOLEDB_CREATESYSTEMDATABASE)</span><span class="sxs-lookup"><span data-stu-id="8f57c-137">(DBPROP_JETOLEDB_CREATESYSTEMDATABASE)</span></span></p></td>
<td><p><span data-ttu-id="8f57c-138">Указывает, следует ли создавать системную базу данных при создании нового источника данных.</span><span class="sxs-lookup"><span data-stu-id="8f57c-138">Indicates whether a system database should be created when creating a new data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-139">Jet OLEDB:Режим блокировки базы данных</span><span class="sxs-lookup"><span data-stu-id="8f57c-139">Jet OLEDB:Database Locking Mode</span></span><br />
<span data-ttu-id="8f57c-140">(DBPROP_JETOLEDB_DATABASELOCKMODE)</span><span class="sxs-lookup"><span data-stu-id="8f57c-140">(DBPROP_JETOLEDB_DATABASELOCKMODE)</span></span></p></td>
<td><p><span data-ttu-id="8f57c-141">Указывает режим блокировки для этой базы данных.</span><span class="sxs-lookup"><span data-stu-id="8f57c-141">Indicates the locking mode for this database.</span></span> <span data-ttu-id="8f57c-142">Первый пользователь, открывав базу данных, определяет режим, используемый при ее открытом режиме.</span><span class="sxs-lookup"><span data-stu-id="8f57c-142">The first user to open the database determines the mode used while the database is open.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-143">Jet OLEDB:Пароль базы данных</span><span class="sxs-lookup"><span data-stu-id="8f57c-143">Jet OLEDB:Database Password</span></span><br />
<span data-ttu-id="8f57c-144">(DBPROP_JETOLEDB_DATABASEPASSWORD)</span><span class="sxs-lookup"><span data-stu-id="8f57c-144">(DBPROP_JETOLEDB_DATABASEPASSWORD)</span></span></p></td>
<td><p><span data-ttu-id="8f57c-145">Указывает пароль базы данных.</span><span class="sxs-lookup"><span data-stu-id="8f57c-145">Indicates the database password.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-146">Jet OLEDB:Don't Copy Locale on Compact</span><span class="sxs-lookup"><span data-stu-id="8f57c-146">Jet OLEDB:Don't Copy Locale on Compact</span></span><br />
<span data-ttu-id="8f57c-147">(DBPROP_JETOLEDB_COMPACT_DONTCOPYLOCALE)</span><span class="sxs-lookup"><span data-stu-id="8f57c-147">(DBPROP_JETOLEDB_COMPACT_DONTCOPYLOCALE)</span></span></p></td>
<td><p><span data-ttu-id="8f57c-148">Указывает, следует ли jet копировать сведения о региональных особеннотах при сжатии базы данных.</span><span class="sxs-lookup"><span data-stu-id="8f57c-148">Indicates whether Jet should copy locale information when compacting a database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-149">Jet OLEDB:Encrypt Database</span><span class="sxs-lookup"><span data-stu-id="8f57c-149">Jet OLEDB:Encrypt Database</span></span><br />
<span data-ttu-id="8f57c-150">(DBPROP_JETOLEDB_ENCRYPTDATABASE)</span><span class="sxs-lookup"><span data-stu-id="8f57c-150">(DBPROP_JETOLEDB_ENCRYPTDATABASE)</span></span></p></td>
<td><p><span data-ttu-id="8f57c-151">Указывает, следует ли шифровать сжатую базу данных.</span><span class="sxs-lookup"><span data-stu-id="8f57c-151">Indicates whether a compacted database should be encrypted.</span></span> <span data-ttu-id="8f57c-152">Если это свойство не установлено, сжатая база данных будет зашифрована, если исходная база данных также была зашифрована.</span><span class="sxs-lookup"><span data-stu-id="8f57c-152">If this property is not set, the compacted database will be encrypted if the original database was also encrypted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-153">Jet OLEDB:Engine Type</span><span class="sxs-lookup"><span data-stu-id="8f57c-153">Jet OLEDB:Engine Type</span></span><br />
<span data-ttu-id="8f57c-154">(DBPROP_JETOLEDB_ENGINE)</span><span class="sxs-lookup"><span data-stu-id="8f57c-154">(DBPROP_JETOLEDB_ENGINE)</span></span></p></td>
<td><p><span data-ttu-id="8f57c-155">Указывает механизм хранения данных, используемый для доступа к текущему хранилищу данных.</span><span class="sxs-lookup"><span data-stu-id="8f57c-155">Indicates the storage engine used to access the current data store.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-156">Jet OLEDB:Монопольная астинктивная задержка</span><span class="sxs-lookup"><span data-stu-id="8f57c-156">Jet OLEDB:Exclusive Async Delay</span></span><br />
<span data-ttu-id="8f57c-157">(DBPROP_JETOLEDB_EXCLUSIVEASYNCDELAY)</span><span class="sxs-lookup"><span data-stu-id="8f57c-157">(DBPROP_JETOLEDB_EXCLUSIVEASYNCDELAY)</span></span></p></td>
<td><p><span data-ttu-id="8f57c-158">Указывает максимальную продолжительность времени (в миллисекунах), в течение которой Jet может откладывать асинхронные записи на диск, когда база данных открывается исключительно.</span><span class="sxs-lookup"><span data-stu-id="8f57c-158">Indicates the maximum length of time, in milliseconds, that Jet can delay asynchronous writes to disk when the database is opened exclusively.</span></span> <span data-ttu-id="8f57c-159">Это свойство игнорируется, если для <strong>jet OLEDB:Flush Transaction Timeout</strong> не установлено 0.</span><span class="sxs-lookup"><span data-stu-id="8f57c-159">This property is ignored unless <strong>Jet OLEDB:Flush Transaction Timeout</strong> is set to 0.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-160">Jet OLEDB:Время сброской транзакции</span><span class="sxs-lookup"><span data-stu-id="8f57c-160">Jet OLEDB:Flush Transaction Timeout</span></span><br />
<span data-ttu-id="8f57c-161">(DBPROP_JETOLEDB_FLUSHTRANSACTIONTIMEOUT)</span><span class="sxs-lookup"><span data-stu-id="8f57c-161">(DBPROP_JETOLEDB_FLUSHTRANSACTIONTIMEOUT)</span></span></p></td>
<td><p><span data-ttu-id="8f57c-162">Указывает время ожидания перед записью на диск данных, хранимых в кэше, для асинхронной записи.</span><span class="sxs-lookup"><span data-stu-id="8f57c-162">Indicates the amount of time to wait before data stored in a cache for asynchronous writing is actually written to disk.</span></span> <span data-ttu-id="8f57c-163">Этот параметр переопределяет значения для <strong>Jet OLEDB:Shared Async Delay</strong> и <strong>Jet OLEDB:Exclusive Async Delay.</strong></span><span class="sxs-lookup"><span data-stu-id="8f57c-163">This setting overrides the values for <strong>Jet OLEDB:Shared Async Delay</strong> and <strong>Jet OLEDB:Exclusive Async Delay</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-164">Jet OLEDB:Глобальные массовые транзакции</span><span class="sxs-lookup"><span data-stu-id="8f57c-164">Jet OLEDB:Global Bulk Transactions</span></span><br />
<span data-ttu-id="8f57c-165">(DBPROP_JETOLEDB_GLOBALBULKNOTRANSACTIONS)</span><span class="sxs-lookup"><span data-stu-id="8f57c-165">(DBPROP_JETOLEDB_GLOBALBULKNOTRANSACTIONS)</span></span></p></td>
<td><p><span data-ttu-id="8f57c-166">Указывает, SQL транзакции.</span><span class="sxs-lookup"><span data-stu-id="8f57c-166">Indicates whether SQL bulk transactions are transacted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-167">Jet OLEDB:Глобальные частичные массовые операции</span><span class="sxs-lookup"><span data-stu-id="8f57c-167">Jet OLEDB:Global Partial Bulk Ops</span></span><br />
<span data-ttu-id="8f57c-168">(DBPROP_JETOLEDB_GLOBALBULKPARTIAL)</span><span class="sxs-lookup"><span data-stu-id="8f57c-168">(DBPROP_JETOLEDB_GLOBALBULKPARTIAL)</span></span></p></td>
<td><p><span data-ttu-id="8f57c-169">Указывает пароль, используемый для открытия базы данных.</span><span class="sxs-lookup"><span data-stu-id="8f57c-169">Indicates the password used to open the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-170">Jet OLEDB:Implicit Commit Sync</span><span class="sxs-lookup"><span data-stu-id="8f57c-170">Jet OLEDB:Implicit Commit Sync</span></span><br />
<span data-ttu-id="8f57c-171">(DBPROP_JETOLEDB_IMPLICITCOMMITSYNC)</span><span class="sxs-lookup"><span data-stu-id="8f57c-171">(DBPROP_JETOLEDB_IMPLICITCOMMITSYNC)</span></span></p></td>
<td><p><span data-ttu-id="8f57c-172">Указывает, записаны ли изменения во внутренних неявных транзакциях в синхронном или асинхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="8f57c-172">Indicates whether changes made in internal implicit transactions are written in synchronous or asynchronous mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-173">Jet OLEDB:Lock Delay</span><span class="sxs-lookup"><span data-stu-id="8f57c-173">Jet OLEDB:Lock Delay</span></span><br />
<span data-ttu-id="8f57c-174">(DBPROP_JETOLEDB_LOCKDELAY)</span><span class="sxs-lookup"><span data-stu-id="8f57c-174">(DBPROP_JETOLEDB_LOCKDELAY)</span></span></p></td>
<td><p><span data-ttu-id="8f57c-175">Указывает количество миллисекунд, которые необходимо подождать, прежде чем пытаться получить блокировку после сбой предыдущей попытки.</span><span class="sxs-lookup"><span data-stu-id="8f57c-175">Indicates the number of milliseconds to wait before attempting to acquire a lock after a previous attempt has failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-176">Jet OLEDB:Lock Retry</span><span class="sxs-lookup"><span data-stu-id="8f57c-176">Jet OLEDB:Lock Retry</span></span><br />
<span data-ttu-id="8f57c-177">(DBPROP_JETOLEDB_LOCKRETRY)</span><span class="sxs-lookup"><span data-stu-id="8f57c-177">(DBPROP_JETOLEDB_LOCKRETRY)</span></span></p></td>
<td><p><span data-ttu-id="8f57c-178">Указывает, сколько раз повторяется попытка доступа к заблокированной странице.</span><span class="sxs-lookup"><span data-stu-id="8f57c-178">Indicates how many times an attempt to access a locked page is repeated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-179">Jet OLEDB:Максимальный размер буфера</span><span class="sxs-lookup"><span data-stu-id="8f57c-179">Jet OLEDB:Max Buffer Size</span></span><br />
<span data-ttu-id="8f57c-180">(DBPROP_JETOLEDB_MAXBUFFERSIZE)</span><span class="sxs-lookup"><span data-stu-id="8f57c-180">(DBPROP_JETOLEDB_MAXBUFFERSIZE)</span></span></p></td>
<td><p><span data-ttu-id="8f57c-181">Указывает максимальный объем памяти в килобайтах, который jet может использовать перед началом очистки изменений на диске.</span><span class="sxs-lookup"><span data-stu-id="8f57c-181">Indicates the maximum amount of memory, in kilobytes, Jet can use before it starts flushing changes to disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-182">Jet OLEDB:Max Locks Per File</span><span class="sxs-lookup"><span data-stu-id="8f57c-182">Jet OLEDB:Max Locks Per File</span></span><br />
<span data-ttu-id="8f57c-183">(DBPROP_JETOLEDB_MAXLOCKSPERFILE)</span><span class="sxs-lookup"><span data-stu-id="8f57c-183">(DBPROP_JETOLEDB_MAXLOCKSPERFILE)</span></span></p></td>
<td><p><span data-ttu-id="8f57c-184">Указывает максимальное число блокировок, которые Jet может разместить в базе данных.</span><span class="sxs-lookup"><span data-stu-id="8f57c-184">Indicates the maximum number of locks Jet can place on a database.</span></span> <span data-ttu-id="8f57c-185">Значение по умолчанию — 9500.</span><span class="sxs-lookup"><span data-stu-id="8f57c-185">The default value is 9500.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-186">Jet OLEDB:Новый пароль базы данных</span><span class="sxs-lookup"><span data-stu-id="8f57c-186">Jet OLEDB:New Database Password</span></span><br />
<span data-ttu-id="8f57c-187">(DBPROP_JETOLEDB_NEWDATABASEPASSWORD)</span><span class="sxs-lookup"><span data-stu-id="8f57c-187">(DBPROP_JETOLEDB_NEWDATABASEPASSWORD)</span></span></p></td>
<td><p><span data-ttu-id="8f57c-188">Указывает новый пароль для этой базы данных.</span><span class="sxs-lookup"><span data-stu-id="8f57c-188">Indicates the new password to be set for this database.</span></span> <span data-ttu-id="8f57c-189">Старый пароль хранится в <strong>Jet OLEDB:Database Password.</strong></span><span class="sxs-lookup"><span data-stu-id="8f57c-189">The old password is stored in <strong>Jet OLEDB:Database Password</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-190">Время простоя команды Jet OLEDB:ODBC</span><span class="sxs-lookup"><span data-stu-id="8f57c-190">Jet OLEDB:ODBC Command Time Out</span></span><br />
<span data-ttu-id="8f57c-191">(DBPROP_JETOLEDB_ODBCCOMMANDTIMEOUT)</span><span class="sxs-lookup"><span data-stu-id="8f57c-191">(DBPROP_JETOLEDB_ODBCCOMMANDTIMEOUT)</span></span></p></td>
<td><p><span data-ttu-id="8f57c-192">Указывает количество миллисекунд до того, как время выполнения удаленного запроса ODBC из Jet будет затмешено.</span><span class="sxs-lookup"><span data-stu-id="8f57c-192">Indicates the number of milliseconds before a remote ODBC query from Jet will timeout.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-193">Jet OLEDB:Page Locks to Table Lock</span><span class="sxs-lookup"><span data-stu-id="8f57c-193">Jet OLEDB:Page Locks to Table Lock</span></span><br />
<span data-ttu-id="8f57c-194">(DBPROP_JETOLEDB_PAGELOCKSTOTABLELOCK)</span><span class="sxs-lookup"><span data-stu-id="8f57c-194">(DBPROP_JETOLEDB_PAGELOCKSTOTABLELOCK)</span></span></p></td>
<td><p><span data-ttu-id="8f57c-195">Указывает, сколько страниц должно быть заблокировано в транзакции, прежде чем Jet пытается повысить блокировку до блокировки таблицы.</span><span class="sxs-lookup"><span data-stu-id="8f57c-195">Indicates how many pages need to be locked within a transaction before Jet attempts to promote the lock to a table lock.</span></span> <span data-ttu-id="8f57c-196">Если это значение 0, блокировка никогда не будет повышена.</span><span class="sxs-lookup"><span data-stu-id="8f57c-196">If this value is 0, then the lock is never promoted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-197">Jet OLEDB:Времяобывка страницы</span><span class="sxs-lookup"><span data-stu-id="8f57c-197">Jet OLEDB:Page Timeout</span></span><br />
<span data-ttu-id="8f57c-198">(DBPROP_JETOLEDB_PAGETIMEOUT)</span><span class="sxs-lookup"><span data-stu-id="8f57c-198">(DBPROP_JETOLEDB_PAGETIMEOUT)</span></span></p></td>
<td><p><span data-ttu-id="8f57c-199">Указывает количество миллисекунд, в которые Jet будет ждать перед проверкой того, устарел ли кэш файла базы данных.</span><span class="sxs-lookup"><span data-stu-id="8f57c-199">Indicates the number of milliseconds Jet will wait before checking to see if its cache is out of date with the database file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-200">Jet OLEDB:Recycle Long-Valued Pages</span><span class="sxs-lookup"><span data-stu-id="8f57c-200">Jet OLEDB:Recycle Long-Valued Pages</span></span><br />
<span data-ttu-id="8f57c-201">(DBPROP_JETOLEDB_RECYCLELONGVALUEPAGES)</span><span class="sxs-lookup"><span data-stu-id="8f57c-201">(DBPROP_JETOLEDB_RECYCLELONGVALUEPAGES)</span></span></p></td>
<td><p><span data-ttu-id="8f57c-202">Указывает, следует ли Jet активно пытаться освободить страницы BLOB при их освобождении.</span><span class="sxs-lookup"><span data-stu-id="8f57c-202">Indicates whether Jet should aggressively try to reclaim BLOB pages when they are freed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-203">Jet OLEDB:Registry Path</span><span class="sxs-lookup"><span data-stu-id="8f57c-203">Jet OLEDB:Registry Path</span></span><br />
<span data-ttu-id="8f57c-204">(DBPROP_JETOLEDB_REGPATH)</span><span class="sxs-lookup"><span data-stu-id="8f57c-204">(DBPROP_JETOLEDB_REGPATH)</span></span></p></td>
<td><p><span data-ttu-id="8f57c-205">Указывает ключ реестра Windows, содержащий значения для ядвижка базы данных Jet.</span><span class="sxs-lookup"><span data-stu-id="8f57c-205">Indicates the Windows registry key that contains values for the Jet database engine.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-206">Jet OLEDB:Reset ISAM Stats</span><span class="sxs-lookup"><span data-stu-id="8f57c-206">Jet OLEDB:Reset ISAM Stats</span></span><br />
<span data-ttu-id="8f57c-207">(DBPROP_JETOLEDB_RESETISAMSTATS)</span><span class="sxs-lookup"><span data-stu-id="8f57c-207">(DBPROP_JETOLEDB_RESETISAMSTATS)</span></span></p></td>
<td><p><span data-ttu-id="8f57c-208">Указывает, должен ли <strong></strong> набор записей схемы DBSCHEMA_JETOLEDB_ISAMSTATS счетчики производительности после возврата сведений о производительности.</span><span class="sxs-lookup"><span data-stu-id="8f57c-208">Indicates whether the schema <strong>Recordset</strong> DBSCHEMA_JETOLEDB_ISAMSTATS should reset its performance counters after returning performance information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-209">Jet OLEDB:Общая а async Delay</span><span class="sxs-lookup"><span data-stu-id="8f57c-209">Jet OLEDB:Shared Async Delay</span></span><br />
<span data-ttu-id="8f57c-210">(DBPROP_JETOLEDB_SHAREDASYNCDELAY)</span><span class="sxs-lookup"><span data-stu-id="8f57c-210">(DBPROP_JETOLEDB_SHAREDASYNCDELAY)</span></span></p></td>
<td><p><span data-ttu-id="8f57c-211">Указывает максимальное время (в миллисекунах), в течение которой Jet может откладывать асинхронные записи на диск, когда база данных открывается в многоязыковом режиме.</span><span class="sxs-lookup"><span data-stu-id="8f57c-211">Indicates the maximum amount of time, in milliseconds, Jet can delay asynchronous writes to disk when the database is opened in multi-user mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-212">Jet OLEDB:System Database</span><span class="sxs-lookup"><span data-stu-id="8f57c-212">Jet OLEDB:System Database</span></span><br />
<span data-ttu-id="8f57c-213">(DBPROP_JETOLEDB_SYSDBPATH)</span><span class="sxs-lookup"><span data-stu-id="8f57c-213">(DBPROP_JETOLEDB_SYSDBPATH)</span></span></p></td>
<td><p><span data-ttu-id="8f57c-214">Указывает путь и имя файла сведений о группе (системная база данных).</span><span class="sxs-lookup"><span data-stu-id="8f57c-214">Indicates the path and file name for the workgroup information file (system database).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-215">Jet OLEDB:Режим фиксации транзакций</span><span class="sxs-lookup"><span data-stu-id="8f57c-215">Jet OLEDB:Transaction Commit Mode</span></span><br />
<span data-ttu-id="8f57c-216">(DBPROP_JETOLEDB_TXNCOMMITMODE)</span><span class="sxs-lookup"><span data-stu-id="8f57c-216">(DBPROP_JETOLEDB_TXNCOMMITMODE)</span></span></p></td>
<td><p><span data-ttu-id="8f57c-217">Указывает, записывает ли Jet данные на диск синхронно или асинхронно при совершении транзакции.</span><span class="sxs-lookup"><span data-stu-id="8f57c-217">Indicates whether Jet writes data to disk synchronously or asynchronously when a transaction is committed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-218">Jet OLEDB:Синхронизация фиксации пользователя</span><span class="sxs-lookup"><span data-stu-id="8f57c-218">Jet OLEDB:User Commit Sync</span></span><br />
<span data-ttu-id="8f57c-219">(DBPROP_JETOLEDB_USERCOMMITSYNC)</span><span class="sxs-lookup"><span data-stu-id="8f57c-219">(DBPROP_JETOLEDB_USERCOMMITSYNC)</span></span></p></td>
<td><p><span data-ttu-id="8f57c-220">Указывает, записаны ли изменения в транзакциях в синхронном или асинхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="8f57c-220">Indicates whether changes made in transactions are written in synchronous or asynchronous mode.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-recordset-and-command-properties"></a><span data-ttu-id="8f57c-221">Provider-Specific Recordset and Command Properties</span><span class="sxs-lookup"><span data-stu-id="8f57c-221">Provider-Specific Recordset and Command Properties</span></span>

<span data-ttu-id="8f57c-222">Поставщик Jet также поддерживает несколько свойств **Recordset** и **Command** для определенного поставщика.</span><span class="sxs-lookup"><span data-stu-id="8f57c-222">The Jet provider also supports several provider-specific **Recordset** and **Command** properties.</span></span> <span data-ttu-id="8f57c-223">Доступ к этим свойствам и их настройка можно получить с помощью коллекции **свойств** объекта **Recordset** или **Command.**</span><span class="sxs-lookup"><span data-stu-id="8f57c-223">These properties are accessed and set through the **Properties** collection of the **Recordset** or **Command** object.</span></span> <span data-ttu-id="8f57c-224">В таблице перечислены имя свойства ADO и соответствующее имя свойства OLE DB в скобки.</span><span class="sxs-lookup"><span data-stu-id="8f57c-224">The table lists the ADO property name and its corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8f57c-225">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="8f57c-225">Property Name</span></span></p></th>
<th><p><span data-ttu-id="8f57c-226">Описание</span><span class="sxs-lookup"><span data-stu-id="8f57c-226">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-227">Jet OLEDB:Bulk Transactions</span><span class="sxs-lookup"><span data-stu-id="8f57c-227">Jet OLEDB:Bulk Transactions</span></span><br />
<span data-ttu-id="8f57c-228">(DBPROP_JETOLEDB_BULKNOTRANSACTIONS)</span><span class="sxs-lookup"><span data-stu-id="8f57c-228">(DBPROP_JETOLEDB_BULKNOTRANSACTIONS)</span></span></p></td>
<td><p><span data-ttu-id="8f57c-229">Указывает, SQL массовой операции.</span><span class="sxs-lookup"><span data-stu-id="8f57c-229">Indicates whether SQL bulk operations are transacted.</span></span> <span data-ttu-id="8f57c-230">Крупные массовые операции могут привести к сбойу при операциях из-за задержек ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8f57c-230">Large bulk operations might fail when transacted, due to resource delays.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-231">Jet OLEDB:Enable Fat Cursors</span><span class="sxs-lookup"><span data-stu-id="8f57c-231">Jet OLEDB:Enable Fat Cursors</span></span><br />
<span data-ttu-id="8f57c-232">(DBPROP_JETOLEDB_ENABLEFATCURSOR)</span><span class="sxs-lookup"><span data-stu-id="8f57c-232">(DBPROP_JETOLEDB_ENABLEFATCURSOR)</span></span></p></td>
<td><p><span data-ttu-id="8f57c-233">Указывает, следует ли jet кэшировать несколько строк при заполнении наборов записей для удаленных источников строк.</span><span class="sxs-lookup"><span data-stu-id="8f57c-233">Indicates whether Jet should cache multiple rows when populating a recordset for remote row sources.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-234">Jet OLEDB:Fat Cursor Cache Size</span><span class="sxs-lookup"><span data-stu-id="8f57c-234">Jet OLEDB:Fat Cursor Cache Size</span></span><br />
<span data-ttu-id="8f57c-235">(DBPROP_JETOLEDB_FATCURSORMAXROWS)</span><span class="sxs-lookup"><span data-stu-id="8f57c-235">(DBPROP_JETOLEDB_FATCURSORMAXROWS)</span></span></p></td>
<td><p><span data-ttu-id="8f57c-236">Указывает количество строк в кэше при использовании кэша строк удаленного хранения данных.</span><span class="sxs-lookup"><span data-stu-id="8f57c-236">Indicates the number of rows to cache when using remote data store row caching.</span></span> <span data-ttu-id="8f57c-237">Это значение игнорируется, если <strong>значение Jet OLEDB:Enable Fat Cursors</strong> имеет значение True.</span><span class="sxs-lookup"><span data-stu-id="8f57c-237">This value is ignored unless <strong>Jet OLEDB:Enable Fat Cursors</strong> is True.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-238">Jet OLEDB:Inconsistent</span><span class="sxs-lookup"><span data-stu-id="8f57c-238">Jet OLEDB:Inconsistent</span></span><br />
<span data-ttu-id="8f57c-239">(DBPROP_JETOLEDB_INCONSISTENT)</span><span class="sxs-lookup"><span data-stu-id="8f57c-239">(DBPROP_JETOLEDB_INCONSISTENT)</span></span></p></td>
<td><p><span data-ttu-id="8f57c-240">Указывает, допускает ли результаты запроса несогласованные обновления.</span><span class="sxs-lookup"><span data-stu-id="8f57c-240">Indicates whether query results allow inconsistent updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-241">Jet OLEDB:Locking Granularity</span><span class="sxs-lookup"><span data-stu-id="8f57c-241">Jet OLEDB:Locking Granularity</span></span><br />
<span data-ttu-id="8f57c-242">(DBPROP_JETOLEDB_LOCKGRANULARITY)</span><span class="sxs-lookup"><span data-stu-id="8f57c-242">(DBPROP_JETOLEDB_LOCKGRANULARITY)</span></span></p></td>
<td><p><span data-ttu-id="8f57c-243">Указывает, открыта ли таблица с помощью блокировки на уровне строки.</span><span class="sxs-lookup"><span data-stu-id="8f57c-243">Indicates whether a table is opened using row-level locking.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-244">Jet OLEDB:ODBC Pass-Through Statement</span><span class="sxs-lookup"><span data-stu-id="8f57c-244">Jet OLEDB:ODBC Pass-Through Statement</span></span><br />
<span data-ttu-id="8f57c-245">(DBPROP_JETOLEDB_ODBCPASSTHROUGH)</span><span class="sxs-lookup"><span data-stu-id="8f57c-245">(DBPROP_JETOLEDB_ODBCPASSTHROUGH)</span></span></p></td>
<td><p><span data-ttu-id="8f57c-246">Указывает, что Jet должен передать SQL текст в <strong>объекте Command</strong> на тыловую дальтоник.</span><span class="sxs-lookup"><span data-stu-id="8f57c-246">Indicates that Jet should pass the SQL text in a <strong>Command</strong> object to the back end unaltered.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-247">Jet OLEDB:частичные массовые операции</span><span class="sxs-lookup"><span data-stu-id="8f57c-247">Jet OLEDB:Partial Bulk Ops</span></span><br />
<span data-ttu-id="8f57c-248">(DBPROP_JETOLEDB_BULKPARTIAL)</span><span class="sxs-lookup"><span data-stu-id="8f57c-248">(DBPROP_JETOLEDB_BULKPARTIAL)</span></span></p></td>
<td><p><span data-ttu-id="8f57c-249">Указывает поведение Jet при с SQL DML.</span><span class="sxs-lookup"><span data-stu-id="8f57c-249">Indicates Jet's behavior when SQL DML operations fail.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-250">Jet OLEDB:Pass Through Query Bulk-Op</span><span class="sxs-lookup"><span data-stu-id="8f57c-250">Jet OLEDB:Pass Through Query Bulk-Op</span></span><br />
<span data-ttu-id="8f57c-251">(DBPROP_JETOLEDB_PASSTHROUGHBULKOP)</span><span class="sxs-lookup"><span data-stu-id="8f57c-251">(DBPROP_JETOLEDB_PASSTHROUGHBULKOP)</span></span></p></td>
<td><p><span data-ttu-id="8f57c-252">Указывает, передаются ли в источник <strong></strong> данных запросы, которые не возвращают набор записей.</span><span class="sxs-lookup"><span data-stu-id="8f57c-252">Indicates whether queries that do not return a <strong>Recordset</strong> are passed unaltered to the data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-253">Jet OLEDB:Pass Through Query Connect String</span><span class="sxs-lookup"><span data-stu-id="8f57c-253">Jet OLEDB:Pass Through Query Connect String</span></span><br />
<span data-ttu-id="8f57c-254">(DBPROP_JETOLEDB_ODBCPASSTHROUGHCONNECTSTRING)</span><span class="sxs-lookup"><span data-stu-id="8f57c-254">(DBPROP_JETOLEDB_ODBCPASSTHROUGHCONNECTSTRING)</span></span></p></td>
<td><p><span data-ttu-id="8f57c-255">Указывает строку подключения Jet, используемую для подключения к удаленному окне данных.</span><span class="sxs-lookup"><span data-stu-id="8f57c-255">Indicates the Jet connect string used to connect to a remote data store.</span></span> <span data-ttu-id="8f57c-256">Это значение игнорируется, если для <strong>jet OLEDB:ODBC Pass-Through Не задается значение</strong> True.</span><span class="sxs-lookup"><span data-stu-id="8f57c-256">This value is ignored unless <strong>Jet OLEDB:ODBC Pass-Through Statement</strong> is True.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-257">Jet OLEDB:Сохраненный запрос</span><span class="sxs-lookup"><span data-stu-id="8f57c-257">Jet OLEDB:Stored Query</span></span><br />
<span data-ttu-id="8f57c-258">(DBPROP_JETOLEDB_STOREDQUERY)</span><span class="sxs-lookup"><span data-stu-id="8f57c-258">(DBPROP_JETOLEDB_STOREDQUERY)</span></span></p></td>
<td><p><span data-ttu-id="8f57c-259">Указывает, следует ли интерпретировать текст команды как сохраненный запрос, а не как SQL команды.</span><span class="sxs-lookup"><span data-stu-id="8f57c-259">Indicates whether the command text should be interpreted as a stored query instead of an SQL command.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-260">Jet OLEDB:Проверка правил в наборе</span><span class="sxs-lookup"><span data-stu-id="8f57c-260">Jet OLEDB:Validate Rules On Set</span></span><br />
<span data-ttu-id="8f57c-261">(DBPROP_JETOLEDB_VALIDATEONSET)</span><span class="sxs-lookup"><span data-stu-id="8f57c-261">(DBPROP_JETOLEDB_VALIDATEONSET)</span></span></p></td>
<td><p><span data-ttu-id="8f57c-262">Указывает, оцениваются ли правила проверки Jet при наборе данных столбцов или при внесении изменений в базу данных.</span><span class="sxs-lookup"><span data-stu-id="8f57c-262">Indicates whether the Jet validation rules are evaluated when column data is set or when the changes are committed to the database.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8f57c-263">По умолчанию поставщик OLE DB для Microsoft Jet открывает базы данных Microsoft Jet в режиме чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="8f57c-263">By default, the OLE DB Provider for Microsoft Jet opens Microsoft Jet databases in read/write mode.</span></span> <span data-ttu-id="8f57c-264">Чтобы открыть базу данных в режиме только для чтения, задайте для свойства [Mode](mode-property-ado.md) объекта ADO **Connection** свойство **adModeRead.**</span><span class="sxs-lookup"><span data-stu-id="8f57c-264">To open a database in read-only mode, set the [Mode](mode-property-ado.md) property on the ADO **Connection** object to **adModeRead**.</span></span>

## <a name="command-object-usage"></a><span data-ttu-id="8f57c-265">Использование объекта Command</span><span class="sxs-lookup"><span data-stu-id="8f57c-265">Command Object Usage</span></span>

<span data-ttu-id="8f57c-266">Текст команды в [объекте Command](command-object-ado.md) использует диалект SQL Microsoft Jet.</span><span class="sxs-lookup"><span data-stu-id="8f57c-266">Command text in the [Command](command-object-ado.md) object uses the Microsoft Jet SQL dialect.</span></span> <span data-ttu-id="8f57c-267">В тексте команды можно указать запросы, запросы действий и имена таблиц, возвращающие строки; однако хранимые процедуры не поддерживаются и не должны быть указаны.</span><span class="sxs-lookup"><span data-stu-id="8f57c-267">You can specify row-returning queries, action queries, and table names in the command text; however, stored procedures are not supported and should not be specified.</span></span>

## <a name="recordset-behavior"></a><span data-ttu-id="8f57c-268">Поведение наборов записей</span><span class="sxs-lookup"><span data-stu-id="8f57c-268">Recordset Behavior</span></span>

<span data-ttu-id="8f57c-269">Ядр базы данных Microsoft Jet не поддерживает динамические курсоры.</span><span class="sxs-lookup"><span data-stu-id="8f57c-269">The Microsoft Jet database engine does not support dynamic cursors.</span></span> <span data-ttu-id="8f57c-270">Поэтому поставщик OLE DB для Microsoft Jet не поддерживает тип курсора **adLockDynamic.**</span><span class="sxs-lookup"><span data-stu-id="8f57c-270">Therefore, the OLE DB Provider for Microsoft Jet does not support the **adLockDynamic** cursor type.</span></span> <span data-ttu-id="8f57c-271">При запросе динамического курсора поставщик возвращает курсор наборов клавиш и сбрасывает свойство [CursorType,](cursortype-property-ado.md) чтобы указать тип возвращаемого объекта [Recordset.](recordset-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="8f57c-271">When a dynamic cursor is requested, the provider will return a keyset cursor and reset the [CursorType](cursortype-property-ado.md) property to indicate the type of [Recordset](recordset-object-ado.md) returned.</span></span> <span data-ttu-id="8f57c-272">Кроме того, если запрашивается updatable **Recordset** **(LockType** — **adLockOptimistic,** **adLockBatchOptimistic** или **adLockPessimistic),** поставщик также возвращает курсор наборов клавиш и сбрасывает свойство **CursorType.**</span><span class="sxs-lookup"><span data-stu-id="8f57c-272">Further, if an updatable **Recordset** is requested (**LockType** is **adLockOptimistic**, **adLockBatchOptimistic**, or **adLockPessimistic**) the provider will also return a keyset cursor and reset the **CursorType** property.</span></span>

## <a name="dynamic-properties"></a><span data-ttu-id="8f57c-273">Динамические свойства</span><span class="sxs-lookup"><span data-stu-id="8f57c-273">Dynamic Properties</span></span>

<span data-ttu-id="8f57c-274">Поставщик OLE DB для Microsoft Jet вставляет несколько динамических свойств в коллекцию **свойств** неподтвершенных объектов [Connection,](connection-object-ado.md) [Recordset](recordset-object-ado.md)и [Command.](command-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="8f57c-274">The OLE DB Provider for Microsoft Jet inserts several dynamic properties into the **Properties** collection of the unopened [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md), and [Command](command-object-ado.md) objects.</span></span>

<span data-ttu-id="8f57c-275">Таблицы ниже — это перекрестный индекс имен ADO и OLE DB для каждого динамического свойства.</span><span class="sxs-lookup"><span data-stu-id="8f57c-275">The tables below are a cross-index of the ADO and OLE DB names for each dynamic property.</span></span> <span data-ttu-id="8f57c-276">Справочник программиста OLE DB относится к имени свойства ADO по термину "Description".</span><span class="sxs-lookup"><span data-stu-id="8f57c-276">The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description."</span></span> <span data-ttu-id="8f57c-277">Дополнительные сведения об этих свойствах можно найти в справочнике программиста OLE DB.</span><span class="sxs-lookup"><span data-stu-id="8f57c-277">You can find more information about these properties in the OLE DB Programmer's Reference.</span></span> <span data-ttu-id="8f57c-278">Найди имя свойства OLE DB в индексе или см. приложение C: OLE DB Properties.</span><span class="sxs-lookup"><span data-stu-id="8f57c-278">Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span></span>

## <a name="connection-dynamic-properties"></a><span data-ttu-id="8f57c-279">Динамические свойства подключения</span><span class="sxs-lookup"><span data-stu-id="8f57c-279">Connection Dynamic Properties</span></span>

<span data-ttu-id="8f57c-280">Следующие свойства добавляются в коллекцию  свойств объекта **Connection.**</span><span class="sxs-lookup"><span data-stu-id="8f57c-280">The following properties are added to the **Connection** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8f57c-281">ADO Property Name</span><span class="sxs-lookup"><span data-stu-id="8f57c-281">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="8f57c-282">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="8f57c-282">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-283">Активные сеансы</span><span class="sxs-lookup"><span data-stu-id="8f57c-283">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="8f57c-284">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="8f57c-284">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-285">Asynchable Abort</span><span class="sxs-lookup"><span data-stu-id="8f57c-285">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="8f57c-286">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="8f57c-286">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-287">Asynchable Commit</span><span class="sxs-lookup"><span data-stu-id="8f57c-287">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="8f57c-288">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="8f57c-288">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-289">Уровни изоляции автозафикса</span><span class="sxs-lookup"><span data-stu-id="8f57c-289">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="8f57c-290">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="8f57c-290">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-291">Расположение каталога</span><span class="sxs-lookup"><span data-stu-id="8f57c-291">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="8f57c-292">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="8f57c-292">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-293">Термин каталога</span><span class="sxs-lookup"><span data-stu-id="8f57c-293">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="8f57c-294">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="8f57c-294">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-295">Определение столбца</span><span class="sxs-lookup"><span data-stu-id="8f57c-295">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="8f57c-296">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="8f57c-296">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-297">Текущий каталог</span><span class="sxs-lookup"><span data-stu-id="8f57c-297">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="8f57c-298">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="8f57c-298">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-299">Источник данных</span><span class="sxs-lookup"><span data-stu-id="8f57c-299">Data Source</span></span></p></td>
<td><p><span data-ttu-id="8f57c-300">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="8f57c-300">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-301">Имя источника данных</span><span class="sxs-lookup"><span data-stu-id="8f57c-301">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="8f57c-302">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="8f57c-302">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-303">Потоковая модель объектов источника данных</span><span class="sxs-lookup"><span data-stu-id="8f57c-303">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="8f57c-304">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="8f57c-304">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-305">DBMS Name</span><span class="sxs-lookup"><span data-stu-id="8f57c-305">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="8f57c-306">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="8f57c-306">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-307">Версия DBMS</span><span class="sxs-lookup"><span data-stu-id="8f57c-307">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="8f57c-308">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="8f57c-308">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-309">Поддержка GROUP BY</span><span class="sxs-lookup"><span data-stu-id="8f57c-309">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="8f57c-310">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="8f57c-310">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-311">Поддержка разнородных таблиц</span><span class="sxs-lookup"><span data-stu-id="8f57c-311">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="8f57c-312">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="8f57c-312">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-313">Чувствительность к делу идентификатора</span><span class="sxs-lookup"><span data-stu-id="8f57c-313">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="8f57c-314">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="8f57c-314">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-315">Уровни изоляции</span><span class="sxs-lookup"><span data-stu-id="8f57c-315">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="8f57c-316">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="8f57c-316">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-317">Хранение изоляции</span><span class="sxs-lookup"><span data-stu-id="8f57c-317">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="8f57c-318">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="8f57c-318">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-319">Код локализовки</span><span class="sxs-lookup"><span data-stu-id="8f57c-319">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="8f57c-320">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="8f57c-320">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-321">Максимальный размер индекса</span><span class="sxs-lookup"><span data-stu-id="8f57c-321">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="8f57c-322">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="8f57c-322">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-323">Максимальный размер строки</span><span class="sxs-lookup"><span data-stu-id="8f57c-323">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="8f57c-324">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="8f57c-324">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-325">Максимальный размер строки включает BLOB</span><span class="sxs-lookup"><span data-stu-id="8f57c-325">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="8f57c-326">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="8f57c-326">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-327">Максимальное число таблиц в SELECT</span><span class="sxs-lookup"><span data-stu-id="8f57c-327">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="8f57c-328">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="8f57c-328">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-329">Режим</span><span class="sxs-lookup"><span data-stu-id="8f57c-329">Mode</span></span></p></td>
<td><p><span data-ttu-id="8f57c-330">DBPROP_INIT_MODE</span><span class="sxs-lookup"><span data-stu-id="8f57c-330">DBPROP_INIT_MODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-331">Несколько наборов параметров</span><span class="sxs-lookup"><span data-stu-id="8f57c-331">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="8f57c-332">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="8f57c-332">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-333">Несколько результатов</span><span class="sxs-lookup"><span data-stu-id="8f57c-333">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="8f57c-334">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="8f57c-334">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-335">Несколько объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="8f57c-335">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="8f57c-336">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="8f57c-336">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-337">Обновление с несколькими таблицами</span><span class="sxs-lookup"><span data-stu-id="8f57c-337">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="8f57c-338">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="8f57c-338">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-339">Порядок оценки NULL</span><span class="sxs-lookup"><span data-stu-id="8f57c-339">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="8f57c-340">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="8f57c-340">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-341">Поведение при конкатенации NULL</span><span class="sxs-lookup"><span data-stu-id="8f57c-341">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="8f57c-342">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="8f57c-342">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-343">Версия OLE DB</span><span class="sxs-lookup"><span data-stu-id="8f57c-343">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="8f57c-344">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="8f57c-344">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-345">Поддержка объектов OLE</span><span class="sxs-lookup"><span data-stu-id="8f57c-345">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="8f57c-346">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="8f57c-346">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-347">Поддержка открытого наборов строк</span><span class="sxs-lookup"><span data-stu-id="8f57c-347">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="8f57c-348">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="8f57c-348">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-349">ORDER BY Columns in Select List</span><span class="sxs-lookup"><span data-stu-id="8f57c-349">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="8f57c-350">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="8f57c-350">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-351">Доступность выходных параметров</span><span class="sxs-lookup"><span data-stu-id="8f57c-351">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="8f57c-352">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="8f57c-352">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-353">Pass By Ref Accessors</span><span class="sxs-lookup"><span data-stu-id="8f57c-353">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="8f57c-354">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="8f57c-354">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-355">Password</span><span class="sxs-lookup"><span data-stu-id="8f57c-355">Password</span></span></p></td>
<td><p><span data-ttu-id="8f57c-356">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="8f57c-356">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-357">Тип сохраняемого ИД</span><span class="sxs-lookup"><span data-stu-id="8f57c-357">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="8f57c-358">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="8f57c-358">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-359">Подготовка поведения для отменить</span><span class="sxs-lookup"><span data-stu-id="8f57c-359">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="8f57c-360">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="8f57c-360">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-361">Подготовка поведения фиксации</span><span class="sxs-lookup"><span data-stu-id="8f57c-361">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="8f57c-362">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="8f57c-362">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-363">Термин процедуры</span><span class="sxs-lookup"><span data-stu-id="8f57c-363">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="8f57c-364">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="8f57c-364">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-365">Prompt</span><span class="sxs-lookup"><span data-stu-id="8f57c-365">Prompt</span></span></p></td>
<td><p><span data-ttu-id="8f57c-366">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="8f57c-366">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-367">Имя поставщика</span><span class="sxs-lookup"><span data-stu-id="8f57c-367">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="8f57c-368">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="8f57c-368">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-369">Имя поставщика</span><span class="sxs-lookup"><span data-stu-id="8f57c-369">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="8f57c-370">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="8f57c-370">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-371">Версия поставщика</span><span class="sxs-lookup"><span data-stu-id="8f57c-371">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="8f57c-372">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="8f57c-372">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-373">Read-Only данных</span><span class="sxs-lookup"><span data-stu-id="8f57c-373">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="8f57c-374">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="8f57c-374">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-375">Преобразование наборов строк в команде</span><span class="sxs-lookup"><span data-stu-id="8f57c-375">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="8f57c-376">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="8f57c-376">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-377">Термин схемы</span><span class="sxs-lookup"><span data-stu-id="8f57c-377">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="8f57c-378">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="8f57c-378">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-379">Использование схемы</span><span class="sxs-lookup"><span data-stu-id="8f57c-379">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="8f57c-380">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="8f57c-380">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-381">SQL поддержки</span><span class="sxs-lookup"><span data-stu-id="8f57c-381">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="8f57c-382">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="8f57c-382">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-383">Структурированное хранилище</span><span class="sxs-lookup"><span data-stu-id="8f57c-383">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="8f57c-384">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="8f57c-384">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-385">Поддержка ветвей</span><span class="sxs-lookup"><span data-stu-id="8f57c-385">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="8f57c-386">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="8f57c-386">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-387">Table Term</span><span class="sxs-lookup"><span data-stu-id="8f57c-387">Table Term</span></span></p></td>
<td><p><span data-ttu-id="8f57c-388">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="8f57c-388">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-389">DDL транзакции</span><span class="sxs-lookup"><span data-stu-id="8f57c-389">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="8f57c-390">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="8f57c-390">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-391">Идентификатор пользователя</span><span class="sxs-lookup"><span data-stu-id="8f57c-391">User ID</span></span></p></td>
<td><p><span data-ttu-id="8f57c-392">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="8f57c-392">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-393">имя пользователя;</span><span class="sxs-lookup"><span data-stu-id="8f57c-393">User Name</span></span></p></td>
<td><p><span data-ttu-id="8f57c-394">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="8f57c-394">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-395">Окне Окне</span><span class="sxs-lookup"><span data-stu-id="8f57c-395">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="8f57c-396">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="8f57c-396">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a><span data-ttu-id="8f57c-397">Динамические свойства recordset</span><span class="sxs-lookup"><span data-stu-id="8f57c-397">Recordset Dynamic Properties</span></span>

<span data-ttu-id="8f57c-398">Следующие свойства добавляются в коллекцию свойств  объекта **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="8f57c-398">The following properties are added to the **Recordset** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8f57c-399">ADO Property Name</span><span class="sxs-lookup"><span data-stu-id="8f57c-399">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="8f57c-400">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="8f57c-400">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-401">Порядок доступа</span><span class="sxs-lookup"><span data-stu-id="8f57c-401">Access Order</span></span></p></td>
<td><p><span data-ttu-id="8f57c-402">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="8f57c-402">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-403">Append-Only Rowset</span><span class="sxs-lookup"><span data-stu-id="8f57c-403">Append-Only Rowset</span></span></p></td>
<td><p><span data-ttu-id="8f57c-404">DBPROP_APPENDONLY</span><span class="sxs-lookup"><span data-stu-id="8f57c-404">DBPROP_APPENDONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-405">Блокировка объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="8f57c-405">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="8f57c-406">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="8f57c-406">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-407">Тип закладки</span><span class="sxs-lookup"><span data-stu-id="8f57c-407">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="8f57c-408">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="8f57c-408">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-409">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="8f57c-409">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="8f57c-410">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="8f57c-410">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-411">Bookmarks Ordered</span><span class="sxs-lookup"><span data-stu-id="8f57c-411">Bookmarks Ordered</span></span></p></td>
<td><p><span data-ttu-id="8f57c-412">DBPROP_ORDEREDBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="8f57c-412">DBPROP_ORDEREDBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-413">Отложенные столбцы кэша</span><span class="sxs-lookup"><span data-stu-id="8f57c-413">Cache Deferred Columns</span></span></p></td>
<td><p><span data-ttu-id="8f57c-414">DBPROP_CACHEDEFERRED</span><span class="sxs-lookup"><span data-stu-id="8f57c-414">DBPROP_CACHEDEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-415">Изменение вставленных строк</span><span class="sxs-lookup"><span data-stu-id="8f57c-415">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="8f57c-416">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="8f57c-416">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-417">Привилегии столбца</span><span class="sxs-lookup"><span data-stu-id="8f57c-417">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="8f57c-418">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="8f57c-418">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-419">Уведомление о наборе столбцов</span><span class="sxs-lookup"><span data-stu-id="8f57c-419">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="8f57c-420">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="8f57c-420">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-421">Для написываемых столбцов</span><span class="sxs-lookup"><span data-stu-id="8f57c-421">Column Writable</span></span></p></td>
<td><p><span data-ttu-id="8f57c-422">DBPROP_MAYWRITECOLUMN</span><span class="sxs-lookup"><span data-stu-id="8f57c-422">DBPROP_MAYWRITECOLUMN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-423">Отложить столбец</span><span class="sxs-lookup"><span data-stu-id="8f57c-423">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="8f57c-424">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="8f57c-424">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-425">Задержка обновлений объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="8f57c-425">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="8f57c-426">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="8f57c-426">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-427">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="8f57c-427">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="8f57c-428">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="8f57c-428">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-429">Строки удержания</span><span class="sxs-lookup"><span data-stu-id="8f57c-429">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="8f57c-430">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="8f57c-430">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-431">IAccessor</span><span class="sxs-lookup"><span data-stu-id="8f57c-431">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="8f57c-432">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="8f57c-432">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-433">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="8f57c-433">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="8f57c-434">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="8f57c-434">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-435">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="8f57c-435">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="8f57c-436">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="8f57c-436">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-437">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="8f57c-437">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="8f57c-438">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="8f57c-438">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-439">IConvertType</span><span class="sxs-lookup"><span data-stu-id="8f57c-439">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="8f57c-440">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="8f57c-440">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-441">ILockBytes</span><span class="sxs-lookup"><span data-stu-id="8f57c-441">ILockBytes</span></span></p></td>
<td><p><span data-ttu-id="8f57c-442">DBPROP_ILockBytes</span><span class="sxs-lookup"><span data-stu-id="8f57c-442">DBPROP_ILockBytes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-443">Строки Immobile</span><span class="sxs-lookup"><span data-stu-id="8f57c-443">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="8f57c-444">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="8f57c-444">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-445">IRowset</span><span class="sxs-lookup"><span data-stu-id="8f57c-445">IRowset</span></span></p></td>
<td><p><span data-ttu-id="8f57c-446">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="8f57c-446">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-447">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="8f57c-447">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="8f57c-448">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="8f57c-448">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-449">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="8f57c-449">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="8f57c-450">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="8f57c-450">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-451">IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="8f57c-451">IRowsetIndex</span></span></p></td>
<td><p><span data-ttu-id="8f57c-452">DBPROP_IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="8f57c-452">DBPROP_IRowsetIndex</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-453">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="8f57c-453">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="8f57c-454">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="8f57c-454">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-455">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="8f57c-455">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="8f57c-456">DBPROP_IRowsestLocate</span><span class="sxs-lookup"><span data-stu-id="8f57c-456">DBPROP_IRowsestLocate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-457">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="8f57c-457">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-458">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="8f57c-458">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="8f57c-459">DBPROP_IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="8f57c-459">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-460">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="8f57c-460">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="8f57c-461">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="8f57c-461">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-462">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="8f57c-462">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="8f57c-463">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="8f57c-463">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-464">IStorage</span><span class="sxs-lookup"><span data-stu-id="8f57c-464">IStorage</span></span></p></td>
<td><p><span data-ttu-id="8f57c-465">DBPROP_IStorage</span><span class="sxs-lookup"><span data-stu-id="8f57c-465">DBPROP_IStorage</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-466">IStream</span><span class="sxs-lookup"><span data-stu-id="8f57c-466">IStream</span></span></p></td>
<td><p><span data-ttu-id="8f57c-467">DBPROP_IStream</span><span class="sxs-lookup"><span data-stu-id="8f57c-467">DBPROP_IStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-468">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="8f57c-468">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="8f57c-469">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="8f57c-469">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-470">Литеральные закладки</span><span class="sxs-lookup"><span data-stu-id="8f57c-470">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="8f57c-471">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="8f57c-471">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-472">Идентификатор строки литералов</span><span class="sxs-lookup"><span data-stu-id="8f57c-472">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="8f57c-473">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="8f57c-473">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-474">Максимальное число открытых строк</span><span class="sxs-lookup"><span data-stu-id="8f57c-474">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="8f57c-475">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="8f57c-475">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-476">Максимальное число ожидающих строк</span><span class="sxs-lookup"><span data-stu-id="8f57c-476">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="8f57c-477">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="8f57c-477">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-478">Максимальное число строк</span><span class="sxs-lookup"><span data-stu-id="8f57c-478">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="8f57c-479">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="8f57c-479">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-480">Использование памяти</span><span class="sxs-lookup"><span data-stu-id="8f57c-480">Memory Usage</span></span></p></td>
<td><p><span data-ttu-id="8f57c-481">DBPROP_MEMORYUSAGE</span><span class="sxs-lookup"><span data-stu-id="8f57c-481">DBPROP_MEMORYUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-482">Детализация уведомлений</span><span class="sxs-lookup"><span data-stu-id="8f57c-482">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="8f57c-483">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="8f57c-483">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-484">Этапы уведомлений</span><span class="sxs-lookup"><span data-stu-id="8f57c-484">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="8f57c-485">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="8f57c-485">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-486">Transacted объектов</span><span class="sxs-lookup"><span data-stu-id="8f57c-486">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="8f57c-487">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="8f57c-487">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-488">Другие изменения видны</span><span class="sxs-lookup"><span data-stu-id="8f57c-488">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="8f57c-489">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="8f57c-489">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-490">Видимые вставки других</span><span class="sxs-lookup"><span data-stu-id="8f57c-490">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="8f57c-491">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="8f57c-491">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-492">Собственные изменения, видимые</span><span class="sxs-lookup"><span data-stu-id="8f57c-492">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="8f57c-493">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="8f57c-493">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-494">Собственные вставки видимые</span><span class="sxs-lookup"><span data-stu-id="8f57c-494">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="8f57c-495">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="8f57c-495">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-496">Сохранение при отменить</span><span class="sxs-lookup"><span data-stu-id="8f57c-496">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="8f57c-497">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="8f57c-497">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-498">Сохранение при фиксации</span><span class="sxs-lookup"><span data-stu-id="8f57c-498">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="8f57c-499">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="8f57c-499">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-500">Быстрая перезагрузка</span><span class="sxs-lookup"><span data-stu-id="8f57c-500">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="8f57c-501">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="8f57c-501">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-502">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="8f57c-502">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="8f57c-503">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="8f57c-503">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-504">Удаление удаленных строк</span><span class="sxs-lookup"><span data-stu-id="8f57c-504">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="8f57c-505">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="8f57c-505">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-506">Отчет о нескольких изменениях</span><span class="sxs-lookup"><span data-stu-id="8f57c-506">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="8f57c-507">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="8f57c-507">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-508">Возврат ожидающих вставки</span><span class="sxs-lookup"><span data-stu-id="8f57c-508">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="8f57c-509">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="8f57c-509">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-510">Уведомление об удалении строки</span><span class="sxs-lookup"><span data-stu-id="8f57c-510">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="8f57c-511">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="8f57c-511">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-512">Уведомление о первом изменении строки</span><span class="sxs-lookup"><span data-stu-id="8f57c-512">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="8f57c-513">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="8f57c-513">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-514">Уведомление о вставке строки</span><span class="sxs-lookup"><span data-stu-id="8f57c-514">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="8f57c-515">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="8f57c-515">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-516">Привилегии строки</span><span class="sxs-lookup"><span data-stu-id="8f57c-516">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="8f57c-517">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="8f57c-517">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-518">Уведомление о повторной синхронизации строк</span><span class="sxs-lookup"><span data-stu-id="8f57c-518">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="8f57c-519">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="8f57c-519">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-520">Модель потоков по строкам</span><span class="sxs-lookup"><span data-stu-id="8f57c-520">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="8f57c-521">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="8f57c-521">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-522">Уведомление об отмене строки</span><span class="sxs-lookup"><span data-stu-id="8f57c-522">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="8f57c-523">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="8f57c-523">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-524">Уведомление об отмене удаления строки</span><span class="sxs-lookup"><span data-stu-id="8f57c-524">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="8f57c-525">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="8f57c-525">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-526">Уведомление об отмене вставки строки</span><span class="sxs-lookup"><span data-stu-id="8f57c-526">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="8f57c-527">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="8f57c-527">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-528">Уведомление об обновлении строки</span><span class="sxs-lookup"><span data-stu-id="8f57c-528">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="8f57c-529">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="8f57c-529">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-530">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="8f57c-530">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="8f57c-531">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="8f57c-531">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-532">Уведомление о выпуске rowset</span><span class="sxs-lookup"><span data-stu-id="8f57c-532">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="8f57c-533">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="8f57c-533">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-534">Прокрутка назад</span><span class="sxs-lookup"><span data-stu-id="8f57c-534">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="8f57c-535">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="8f57c-535">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-536">Пропустить удаленные закладки</span><span class="sxs-lookup"><span data-stu-id="8f57c-536">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="8f57c-537">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="8f57c-537">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-538">Удостоверение строки strong</span><span class="sxs-lookup"><span data-stu-id="8f57c-538">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="8f57c-539">DBPROP_STRONGITDENTITY</span><span class="sxs-lookup"><span data-stu-id="8f57c-539">DBPROP_STRONGITDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-540">Updatability</span><span class="sxs-lookup"><span data-stu-id="8f57c-540">Updatability</span></span></p></td>
<td><p><span data-ttu-id="8f57c-541">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="8f57c-541">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-542">Использование закладок</span><span class="sxs-lookup"><span data-stu-id="8f57c-542">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="8f57c-543">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="8f57c-543">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a><span data-ttu-id="8f57c-544">Командные динамические свойства</span><span class="sxs-lookup"><span data-stu-id="8f57c-544">Command Dynamic Properties</span></span>

<span data-ttu-id="8f57c-545">Следующие свойства добавляются в  коллекцию **свойств объекта Command.**</span><span class="sxs-lookup"><span data-stu-id="8f57c-545">The following properties are added to the **Command** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8f57c-546">ADO Property Name</span><span class="sxs-lookup"><span data-stu-id="8f57c-546">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="8f57c-547">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="8f57c-547">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-548">Порядок доступа</span><span class="sxs-lookup"><span data-stu-id="8f57c-548">Access Order</span></span></p></td>
<td><p><span data-ttu-id="8f57c-549">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="8f57c-549">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-550">Append-Only Rowset</span><span class="sxs-lookup"><span data-stu-id="8f57c-550">Append-Only Rowset</span></span></p></td>
<td><p><span data-ttu-id="8f57c-551">DBPROP_APPENDONLY</span><span class="sxs-lookup"><span data-stu-id="8f57c-551">DBPROP_APPENDONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-552">Блокировка объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="8f57c-552">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="8f57c-553">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="8f57c-553">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-554">Тип закладки</span><span class="sxs-lookup"><span data-stu-id="8f57c-554">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="8f57c-555">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="8f57c-555">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-556">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="8f57c-556">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="8f57c-557">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="8f57c-557">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-558">Изменение вставленных строк</span><span class="sxs-lookup"><span data-stu-id="8f57c-558">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="8f57c-559">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="8f57c-559">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-560">Привилегии столбца</span><span class="sxs-lookup"><span data-stu-id="8f57c-560">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="8f57c-561">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="8f57c-561">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-562">Уведомление о наборе столбцов</span><span class="sxs-lookup"><span data-stu-id="8f57c-562">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="8f57c-563">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="8f57c-563">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-564">Отложить столбец</span><span class="sxs-lookup"><span data-stu-id="8f57c-564">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="8f57c-565">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="8f57c-565">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-566">Задержка обновлений объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="8f57c-566">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="8f57c-567">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="8f57c-567">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-568">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="8f57c-568">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="8f57c-569">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="8f57c-569">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-570">Строки удержания</span><span class="sxs-lookup"><span data-stu-id="8f57c-570">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="8f57c-571">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="8f57c-571">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-572">IAccessor</span><span class="sxs-lookup"><span data-stu-id="8f57c-572">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="8f57c-573">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="8f57c-573">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-574">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="8f57c-574">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="8f57c-575">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="8f57c-575">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-576">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="8f57c-576">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="8f57c-577">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="8f57c-577">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-578">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="8f57c-578">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="8f57c-579">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="8f57c-579">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-580">IConvertType</span><span class="sxs-lookup"><span data-stu-id="8f57c-580">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="8f57c-581">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="8f57c-581">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-582">ILockBytes</span><span class="sxs-lookup"><span data-stu-id="8f57c-582">ILockBytes</span></span></p></td>
<td><p><span data-ttu-id="8f57c-583">DBPROP_ILockBytes</span><span class="sxs-lookup"><span data-stu-id="8f57c-583">DBPROP_ILockBytes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-584">Строки Immobile</span><span class="sxs-lookup"><span data-stu-id="8f57c-584">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="8f57c-585">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="8f57c-585">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-586">IRowset</span><span class="sxs-lookup"><span data-stu-id="8f57c-586">IRowset</span></span></p></td>
<td><p><span data-ttu-id="8f57c-587">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="8f57c-587">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-588">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="8f57c-588">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="8f57c-589">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="8f57c-589">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-590">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="8f57c-590">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="8f57c-591">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="8f57c-591">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-592">IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="8f57c-592">IRowsetIndex</span></span></p></td>
<td><p><span data-ttu-id="8f57c-593">DBPROP_IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="8f57c-593">DBPROP_IRowsetIndex</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-594">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="8f57c-594">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="8f57c-595">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="8f57c-595">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-596">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="8f57c-596">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="8f57c-597">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="8f57c-597">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-598">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="8f57c-598">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-599">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="8f57c-599">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="8f57c-600">DBPROP_IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="8f57c-600">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-601">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="8f57c-601">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="8f57c-602">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="8f57c-602">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-603">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="8f57c-603">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="8f57c-604">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="8f57c-604">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-605">IStorage</span><span class="sxs-lookup"><span data-stu-id="8f57c-605">IStorage</span></span></p></td>
<td><p><span data-ttu-id="8f57c-606">DBPROP_IStorage</span><span class="sxs-lookup"><span data-stu-id="8f57c-606">DBPROP_IStorage</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-607">IStream</span><span class="sxs-lookup"><span data-stu-id="8f57c-607">IStream</span></span></p></td>
<td><p><span data-ttu-id="8f57c-608">DBPROP_IStream</span><span class="sxs-lookup"><span data-stu-id="8f57c-608">DBPROP_IStream</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-609">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="8f57c-609">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="8f57c-610">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="8f57c-610">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-611">Литеральные закладки</span><span class="sxs-lookup"><span data-stu-id="8f57c-611">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="8f57c-612">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="8f57c-612">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-613">Идентификатор строки литералов</span><span class="sxs-lookup"><span data-stu-id="8f57c-613">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="8f57c-614">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="8f57c-614">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-615">Режим блокировки</span><span class="sxs-lookup"><span data-stu-id="8f57c-615">Lock Mode</span></span></p></td>
<td><p><span data-ttu-id="8f57c-616">DBPROP_LOCKMODE</span><span class="sxs-lookup"><span data-stu-id="8f57c-616">DBPROP_LOCKMODE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-617">Максимальное число открытых строк</span><span class="sxs-lookup"><span data-stu-id="8f57c-617">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="8f57c-618">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="8f57c-618">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-619">Максимальное число ожидающих строк</span><span class="sxs-lookup"><span data-stu-id="8f57c-619">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="8f57c-620">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="8f57c-620">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-621">Максимальное число строк</span><span class="sxs-lookup"><span data-stu-id="8f57c-621">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="8f57c-622">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="8f57c-622">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-623">Детализация уведомлений</span><span class="sxs-lookup"><span data-stu-id="8f57c-623">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="8f57c-624">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="8f57c-624">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-625">Этапы уведомлений</span><span class="sxs-lookup"><span data-stu-id="8f57c-625">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="8f57c-626">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="8f57c-626">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-627">Transacted объектов</span><span class="sxs-lookup"><span data-stu-id="8f57c-627">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="8f57c-628">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="8f57c-628">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-629">Другие изменения видны</span><span class="sxs-lookup"><span data-stu-id="8f57c-629">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="8f57c-630">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="8f57c-630">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-631">Видимые вставки других</span><span class="sxs-lookup"><span data-stu-id="8f57c-631">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="8f57c-632">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="8f57c-632">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-633">Собственные изменения, видимые</span><span class="sxs-lookup"><span data-stu-id="8f57c-633">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="8f57c-634">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="8f57c-634">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-635">Собственные вставки видимые</span><span class="sxs-lookup"><span data-stu-id="8f57c-635">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="8f57c-636">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="8f57c-636">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-637">Сохранение при отменить</span><span class="sxs-lookup"><span data-stu-id="8f57c-637">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="8f57c-638">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="8f57c-638">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-639">Сохранение при фиксации</span><span class="sxs-lookup"><span data-stu-id="8f57c-639">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="8f57c-640">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="8f57c-640">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-641">Быстрая перезагрузка</span><span class="sxs-lookup"><span data-stu-id="8f57c-641">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="8f57c-642">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="8f57c-642">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-643">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="8f57c-643">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="8f57c-644">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="8f57c-644">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-645">Удаление удаленных строк</span><span class="sxs-lookup"><span data-stu-id="8f57c-645">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="8f57c-646">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="8f57c-646">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-647">Отчет о нескольких изменениях</span><span class="sxs-lookup"><span data-stu-id="8f57c-647">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="8f57c-648">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="8f57c-648">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-649">Возврат ожидающих вставки</span><span class="sxs-lookup"><span data-stu-id="8f57c-649">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="8f57c-650">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="8f57c-650">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-651">Уведомление об удалении строки</span><span class="sxs-lookup"><span data-stu-id="8f57c-651">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="8f57c-652">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="8f57c-652">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-653">Уведомление о первом изменении строки</span><span class="sxs-lookup"><span data-stu-id="8f57c-653">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="8f57c-654">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="8f57c-654">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-655">Уведомление о вставке строки</span><span class="sxs-lookup"><span data-stu-id="8f57c-655">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="8f57c-656">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="8f57c-656">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-657">Привилегии строки</span><span class="sxs-lookup"><span data-stu-id="8f57c-657">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="8f57c-658">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="8f57c-658">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-659">Уведомление о повторной синхронизации строк</span><span class="sxs-lookup"><span data-stu-id="8f57c-659">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="8f57c-660">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="8f57c-660">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-661">Модель потоков по строкам</span><span class="sxs-lookup"><span data-stu-id="8f57c-661">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="8f57c-662">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="8f57c-662">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-663">Уведомление об отмене строки</span><span class="sxs-lookup"><span data-stu-id="8f57c-663">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="8f57c-664">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="8f57c-664">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-665">Уведомление об отмене удаления строки</span><span class="sxs-lookup"><span data-stu-id="8f57c-665">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="8f57c-666">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="8f57c-666">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-667">Уведомление об отмене вставки строки</span><span class="sxs-lookup"><span data-stu-id="8f57c-667">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="8f57c-668">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="8f57c-668">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-669">Уведомление об обновлении строки</span><span class="sxs-lookup"><span data-stu-id="8f57c-669">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="8f57c-670">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="8f57c-670">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-671">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="8f57c-671">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="8f57c-672">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="8f57c-672">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-673">Уведомление о выпуске rowset</span><span class="sxs-lookup"><span data-stu-id="8f57c-673">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="8f57c-674">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="8f57c-674">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-675">Прокрутка назад</span><span class="sxs-lookup"><span data-stu-id="8f57c-675">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="8f57c-676">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="8f57c-676">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-677">Данные сервера при вставке</span><span class="sxs-lookup"><span data-stu-id="8f57c-677">Server Data on Insert</span></span></p></td>
<td><p><span data-ttu-id="8f57c-678">DBPROP_SERVERDATAONINSERT</span><span class="sxs-lookup"><span data-stu-id="8f57c-678">DBPROP_SERVERDATAONINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-679">Пропустить удаленные закладки</span><span class="sxs-lookup"><span data-stu-id="8f57c-679">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="8f57c-680">DBPROP_BOOKMARKSKIP</span><span class="sxs-lookup"><span data-stu-id="8f57c-680">DBPROP_BOOKMARKSKIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-681">Удостоверение строки strong</span><span class="sxs-lookup"><span data-stu-id="8f57c-681">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="8f57c-682">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="8f57c-682">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f57c-683">Updatability</span><span class="sxs-lookup"><span data-stu-id="8f57c-683">Updatability</span></span></p></td>
<td><p><span data-ttu-id="8f57c-684">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="8f57c-684">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f57c-685">Использование закладок</span><span class="sxs-lookup"><span data-stu-id="8f57c-685">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="8f57c-686">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="8f57c-686">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="8f57c-687">См. также</span><span class="sxs-lookup"><span data-stu-id="8f57c-687">See also</span></span>

<span data-ttu-id="8f57c-688">Подробные сведения о реализации и функциональные сведения о поставщике OLE DB для Microsoft Jet можно получить в документации по поставщику OLE DB для Microsoft Jet в MDAC SDK.</span><span class="sxs-lookup"><span data-stu-id="8f57c-688">For specific implementation details and functional information about the OLE DB Provider for Microsoft Jet, consult the OLE DB Provider for Microsoft Jet documentation in the MDAC SDK.</span></span>

