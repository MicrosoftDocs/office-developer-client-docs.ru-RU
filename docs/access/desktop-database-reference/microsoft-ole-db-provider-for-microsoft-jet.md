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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712843"
---
# <a name="microsoft-ole-db-provider-for-microsoft-jet"></a><span data-ttu-id="a96fa-102">Поставщик Microsoft OLE DB для Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="a96fa-102">Microsoft OLE DB Provider for Microsoft Jet</span></span>

<span data-ttu-id="a96fa-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a96fa-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a96fa-104">Поставщик OLE DB для Microsoft Jet позволяет ADO для доступа к базам данных Microsoft Jet.</span><span class="sxs-lookup"><span data-stu-id="a96fa-104">The OLE DB Provider for Microsoft Jet allows ADO to access Microsoft Jet databases.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="a96fa-105">Параметры строки подключения</span><span class="sxs-lookup"><span data-stu-id="a96fa-105">Connection String Parameters</span></span>

<span data-ttu-id="a96fa-106">Для подключения к данным поставщиком, задайте для свойства [ConnectionString](connectionstring-property-ado.md) для аргумента *поставщика* :</span><span class="sxs-lookup"><span data-stu-id="a96fa-106">To connect to this provider, set the *Provider* argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```vb 
 
Microsoft.Jet.OLEDB.4.0 
```

<span data-ttu-id="a96fa-107">Чтение свойства [поставщика](provider-property-ado.md) будет возвращать также этой строки.</span><span class="sxs-lookup"><span data-stu-id="a96fa-107">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="a96fa-108">Типичная строка подключения</span><span class="sxs-lookup"><span data-stu-id="a96fa-108">Typical Connection String</span></span>

<span data-ttu-id="a96fa-109">— Это строка соединения для данного поставщика:</span><span class="sxs-lookup"><span data-stu-id="a96fa-109">A typical connection string for this provider is:</span></span>

```vb 
 
"Provider=Microsoft.Jet.OLEDB.4.0;Data Source=databaseName;User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="a96fa-110">Строка состоит из следующих ключевых слов:</span><span class="sxs-lookup"><span data-stu-id="a96fa-110">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a96fa-111">Keyword</span><span class="sxs-lookup"><span data-stu-id="a96fa-111">Keyword</span></span></p></th>
<th><p><span data-ttu-id="a96fa-112">Описание</span><span class="sxs-lookup"><span data-stu-id="a96fa-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-113"><strong>Поставщик</strong></span><span class="sxs-lookup"><span data-stu-id="a96fa-113"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="a96fa-114">Задает поставщика OLE DB для Microsoft Jet.</span><span class="sxs-lookup"><span data-stu-id="a96fa-114">Specifies the OLE DB Provider for Microsoft Jet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-115"><strong>Источник данных</strong></span><span class="sxs-lookup"><span data-stu-id="a96fa-115"><strong>Data Source</strong></span></span></p></td>
<td><p><span data-ttu-id="a96fa-116">Указывает базу данных путь и имя файла (например, c:\Northwind.mdb).</span><span class="sxs-lookup"><span data-stu-id="a96fa-116">Specifies the database path and file name (for example, c:\Northwind.mdb).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-117"><strong>Идентификатор пользователя</strong></span><span class="sxs-lookup"><span data-stu-id="a96fa-117"><strong>User ID</strong></span></span></p></td>
<td><p><span data-ttu-id="a96fa-118">Задает имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="a96fa-118">Specifies the user name.</span></span> <span data-ttu-id="a96fa-119">Если это ключевое слово не указан, строка, &quot;администратора&quot;, используемый по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a96fa-119">If this keyword is not specified, the string, &quot;admin&quot;, is used by default.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-120"><strong>Password</strong></span><span class="sxs-lookup"><span data-stu-id="a96fa-120"><strong>Password</strong></span></span></p></td>
<td><p><span data-ttu-id="a96fa-121">Задает пароль пользователя.</span><span class="sxs-lookup"><span data-stu-id="a96fa-121">Specifies the user password.</span></span> <span data-ttu-id="a96fa-122">Если это ключевое слово не указан, пустая строка (&quot;&quot;), используемый по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a96fa-122">If this keyword is not specified, the empty string (&quot;&quot;), is used by default.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-connection-parameters"></a><span data-ttu-id="a96fa-123">Параметры подключения от поставщика</span><span class="sxs-lookup"><span data-stu-id="a96fa-123">Provider-Specific Connection Parameters</span></span>

<span data-ttu-id="a96fa-124">Поставщик OLE DB для Microsoft Jet поддерживает несколько динамические свойства от поставщика дополнение к тем определяется ADO.</span><span class="sxs-lookup"><span data-stu-id="a96fa-124">The OLE DB Provider for Microsoft Jet supports several provider-specific dynamic properties in addition to those defined by ADO.</span></span> <span data-ttu-id="a96fa-125">Как вместе с другими параметрами **подключения** могут устанавливаться с помощью **Свойства** коллекции объект **подключения** или в качестве части строки подключения.</span><span class="sxs-lookup"><span data-stu-id="a96fa-125">As with all other **Connection** parameters, they can be set via the **Connection** object's **Properties** collection or as part of the connection string.</span></span>

<span data-ttu-id="a96fa-126">В следующей таблице перечислены эти свойства имя соответствующего свойства OLE DB в скобки.</span><span class="sxs-lookup"><span data-stu-id="a96fa-126">The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a96fa-127">Параметр</span><span class="sxs-lookup"><span data-stu-id="a96fa-127">Parameter</span></span></p></th>
<th><p><span data-ttu-id="a96fa-128">Описание</span><span class="sxs-lookup"><span data-stu-id="a96fa-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-129">Освобожденное место сумма Jet OLEDB:Compact</span><span class="sxs-lookup"><span data-stu-id="a96fa-129">Jet OLEDB:Compact Reclaimed Space Amount</span></span><br />
<span data-ttu-id="a96fa-130">(DBPROP_JETOLEDB_COMPACTFREESPACESIZE)</span><span class="sxs-lookup"><span data-stu-id="a96fa-130">(DBPROP_JETOLEDB_COMPACTFREESPACESIZE)</span></span></p></td>
<td><p><span data-ttu-id="a96fa-131">Указывает оценку дискового пространства, в байтах, который может быть восстановлена путем сжатие базы данных.</span><span class="sxs-lookup"><span data-stu-id="a96fa-131">Indicates an estimate of the amount of space, in bytes, that can be reclaimed by compacting the database.</span></span> <span data-ttu-id="a96fa-132">Это значение допустимо только после установления подключения к базе данных.</span><span class="sxs-lookup"><span data-stu-id="a96fa-132">This value is only valid after a database connection has been established.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-133">Элемент управления OLEDB:Connection Jet</span><span class="sxs-lookup"><span data-stu-id="a96fa-133">Jet OLEDB:Connection Control</span></span><br />
<span data-ttu-id="a96fa-134">(DBPROP_JETOLEDB_CONNECTIONCONTROL)</span><span class="sxs-lookup"><span data-stu-id="a96fa-134">(DBPROP_JETOLEDB_CONNECTIONCONTROL)</span></span></p></td>
<td><p><span data-ttu-id="a96fa-135">Указывает, будет ли пользователи могут подключаться к базе данных.</span><span class="sxs-lookup"><span data-stu-id="a96fa-135">Indicates whether users can connect to the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-136">Jet OLEDB: создание Системная база данных</span><span class="sxs-lookup"><span data-stu-id="a96fa-136">Jet OLEDB:Create System Database</span></span><br />
<span data-ttu-id="a96fa-137">(DBPROP_JETOLEDB_CREATESYSTEMDATABASE)</span><span class="sxs-lookup"><span data-stu-id="a96fa-137">(DBPROP_JETOLEDB_CREATESYSTEMDATABASE)</span></span></p></td>
<td><p><span data-ttu-id="a96fa-138">Указывает, следует ли создавать Системная база данных при создании нового источника данных.</span><span class="sxs-lookup"><span data-stu-id="a96fa-138">Indicates whether a system database should be created when creating a new data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-139">Режим блокировки OLEDB:Database Jet</span><span class="sxs-lookup"><span data-stu-id="a96fa-139">Jet OLEDB:Database Locking Mode</span></span><br />
<span data-ttu-id="a96fa-140">(DBPROP_JETOLEDB_DATABASELOCKMODE)</span><span class="sxs-lookup"><span data-stu-id="a96fa-140">(DBPROP_JETOLEDB_DATABASELOCKMODE)</span></span></p></td>
<td><p><span data-ttu-id="a96fa-141">Указывает режим блокировки для этой базы данных.</span><span class="sxs-lookup"><span data-stu-id="a96fa-141">Indicates the locking mode for this database.</span></span> <span data-ttu-id="a96fa-142">Первый пользователю открывать базу данных определяет режим, используемый при открытом базы данных.</span><span class="sxs-lookup"><span data-stu-id="a96fa-142">The first user to open the database determines the mode used while the database is open.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-143">Пароль OLEDB:Database Jet</span><span class="sxs-lookup"><span data-stu-id="a96fa-143">Jet OLEDB:Database Password</span></span><br />
<span data-ttu-id="a96fa-144">(DBPROP_JETOLEDB_DATABASEPASSWORD)</span><span class="sxs-lookup"><span data-stu-id="a96fa-144">(DBPROP_JETOLEDB_DATABASEPASSWORD)</span></span></p></td>
<td><p><span data-ttu-id="a96fa-145">Указывает пароль базы данных.</span><span class="sxs-lookup"><span data-stu-id="a96fa-145">Indicates the database password.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-146">Jet OLEDB: не копировать языковой стандарт на компакт</span><span class="sxs-lookup"><span data-stu-id="a96fa-146">Jet OLEDB:Don't Copy Locale on Compact</span></span><br />
<span data-ttu-id="a96fa-147">(DBPROP_JETOLEDB_COMPACT_DONTCOPYLOCALE)</span><span class="sxs-lookup"><span data-stu-id="a96fa-147">(DBPROP_JETOLEDB_COMPACT_DONTCOPYLOCALE)</span></span></p></td>
<td><p><span data-ttu-id="a96fa-148">Указывает, следует ли Jet скопировать сведения о языковом стандарте при сжатии базы данных.</span><span class="sxs-lookup"><span data-stu-id="a96fa-148">Indicates whether Jet should copy locale information when compacting a database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-149">Jet OLEDB: шифрование базы данных</span><span class="sxs-lookup"><span data-stu-id="a96fa-149">Jet OLEDB:Encrypt Database</span></span><br />
<span data-ttu-id="a96fa-150">(DBPROP_JETOLEDB_ENCRYPTDATABASE)</span><span class="sxs-lookup"><span data-stu-id="a96fa-150">(DBPROP_JETOLEDB_ENCRYPTDATABASE)</span></span></p></td>
<td><p><span data-ttu-id="a96fa-151">Указывает, должен быть зашифрован сжатии баз данных.</span><span class="sxs-lookup"><span data-stu-id="a96fa-151">Indicates whether a compacted database should be encrypted.</span></span> <span data-ttu-id="a96fa-152">Если это свойство не задано, сжатии базы данных будет шифроваться, если также зашифрованные исходной базы данных.</span><span class="sxs-lookup"><span data-stu-id="a96fa-152">If this property is not set, the compacted database will be encrypted if the original database was also encrypted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-153">Тип OLEDB:Engine Jet</span><span class="sxs-lookup"><span data-stu-id="a96fa-153">Jet OLEDB:Engine Type</span></span><br />
<span data-ttu-id="a96fa-154">(DBPROP_JETOLEDB_ENGINE)</span><span class="sxs-lookup"><span data-stu-id="a96fa-154">(DBPROP_JETOLEDB_ENGINE)</span></span></p></td>
<td><p><span data-ttu-id="a96fa-155">Указывает, подсистема хранилища для доступа к текущей хранилищу данных.</span><span class="sxs-lookup"><span data-stu-id="a96fa-155">Indicates the storage engine used to access the current data store.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-156">Асинхронная задержка Jet OLEDB:Exclusive</span><span class="sxs-lookup"><span data-stu-id="a96fa-156">Jet OLEDB:Exclusive Async Delay</span></span><br />
<span data-ttu-id="a96fa-157">(DBPROP_JETOLEDB_EXCLUSIVEASYNCDELAY)</span><span class="sxs-lookup"><span data-stu-id="a96fa-157">(DBPROP_JETOLEDB_EXCLUSIVEASYNCDELAY)</span></span></p></td>
<td><p><span data-ttu-id="a96fa-158">Указывает максимальную длину время в миллисекундах, которые Jet может отложить асинхронных операций записи на диск при открытии исключительно базы данных.</span><span class="sxs-lookup"><span data-stu-id="a96fa-158">Indicates the maximum length of time, in milliseconds, that Jet can delay asynchronous writes to disk when the database is opened exclusively.</span></span> <span data-ttu-id="a96fa-159">Это свойство игнорируется, если <strong>Время ожидания транзакций OLEDB:Flush Jet</strong> не задано значение 0.</span><span class="sxs-lookup"><span data-stu-id="a96fa-159">This property is ignored unless <strong>Jet OLEDB:Flush Transaction Timeout</strong> is set to 0.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-160">Время ожидания транзакций OLEDB:Flush Jet</span><span class="sxs-lookup"><span data-stu-id="a96fa-160">Jet OLEDB:Flush Transaction Timeout</span></span><br />
<span data-ttu-id="a96fa-161">(DBPROP_JETOLEDB_FLUSHTRANSACTIONTIMEOUT)</span><span class="sxs-lookup"><span data-stu-id="a96fa-161">(DBPROP_JETOLEDB_FLUSHTRANSACTIONTIMEOUT)</span></span></p></td>
<td><p><span data-ttu-id="a96fa-162">Указывает время ожидания до фактически записи данных, сохраненных в кэше для асинхронной записи на диск.</span><span class="sxs-lookup"><span data-stu-id="a96fa-162">Indicates the amount of time to wait before data stored in a cache for asynchronous writing is actually written to disk.</span></span> <span data-ttu-id="a96fa-163">Этот параметр переопределяет значения для <strong>Jet OLEDB: общих асинхронная задержка</strong> и <strong>Jet OLEDB:Exclusive асинхронная задержка</strong>.</span><span class="sxs-lookup"><span data-stu-id="a96fa-163">This setting overrides the values for <strong>Jet OLEDB:Shared Async Delay</strong> and <strong>Jet OLEDB:Exclusive Async Delay</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-164">Jet OLEDB: глобальные массовых операций</span><span class="sxs-lookup"><span data-stu-id="a96fa-164">Jet OLEDB:Global Bulk Transactions</span></span><br />
<span data-ttu-id="a96fa-165">(DBPROP_JETOLEDB_GLOBALBULKNOTRANSACTIONS)</span><span class="sxs-lookup"><span data-stu-id="a96fa-165">(DBPROP_JETOLEDB_GLOBALBULKNOTRANSACTIONS)</span></span></p></td>
<td><p><span data-ttu-id="a96fa-166">Указывает, будет ли в рамках транзакции SQL массовых операций.</span><span class="sxs-lookup"><span data-stu-id="a96fa-166">Indicates whether SQL bulk transactions are transacted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-167">Jet OLEDB: глобальные частичное массового операций</span><span class="sxs-lookup"><span data-stu-id="a96fa-167">Jet OLEDB:Global Partial Bulk Ops</span></span><br />
<span data-ttu-id="a96fa-168">(DBPROP_JETOLEDB_GLOBALBULKPARTIAL)</span><span class="sxs-lookup"><span data-stu-id="a96fa-168">(DBPROP_JETOLEDB_GLOBALBULKPARTIAL)</span></span></p></td>
<td><p><span data-ttu-id="a96fa-169">Указывает пароль, используемый для открытия базы данных.</span><span class="sxs-lookup"><span data-stu-id="a96fa-169">Indicates the password used to open the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-170">Jet OLEDB: неявных зафиксировать синхронизации</span><span class="sxs-lookup"><span data-stu-id="a96fa-170">Jet OLEDB:Implicit Commit Sync</span></span><br />
<span data-ttu-id="a96fa-171">(DBPROP_JETOLEDB_IMPLICITCOMMITSYNC)</span><span class="sxs-lookup"><span data-stu-id="a96fa-171">(DBPROP_JETOLEDB_IMPLICITCOMMITSYNC)</span></span></p></td>
<td><p><span data-ttu-id="a96fa-172">Указывает, записываются ли изменения, внесенные в внутренних неявных транзакций в режиме синхронными и асинхронными.</span><span class="sxs-lookup"><span data-stu-id="a96fa-172">Indicates whether changes made in internal implicit transactions are written in synchronous or asynchronous mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-173">Задержка OLEDB:Lock Jet</span><span class="sxs-lookup"><span data-stu-id="a96fa-173">Jet OLEDB:Lock Delay</span></span><br />
<span data-ttu-id="a96fa-174">(DBPROP_JETOLEDB_LOCKDELAY)</span><span class="sxs-lookup"><span data-stu-id="a96fa-174">(DBPROP_JETOLEDB_LOCKDELAY)</span></span></p></td>
<td><p><span data-ttu-id="a96fa-175">Указывает время в миллисекундах ожидания запроса блокировки после Предыдущая попытка не удалось выполнить.</span><span class="sxs-lookup"><span data-stu-id="a96fa-175">Indicates the number of milliseconds to wait before attempting to acquire a lock after a previous attempt has failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-176">Повтор OLEDB:Lock Jet</span><span class="sxs-lookup"><span data-stu-id="a96fa-176">Jet OLEDB:Lock Retry</span></span><br />
<span data-ttu-id="a96fa-177">(DBPROP_JETOLEDB_LOCKRETRY)</span><span class="sxs-lookup"><span data-stu-id="a96fa-177">(DBPROP_JETOLEDB_LOCKRETRY)</span></span></p></td>
<td><p><span data-ttu-id="a96fa-178">Указывает, сколько раз при попытке доступа к заблокированной странице повторяется.</span><span class="sxs-lookup"><span data-stu-id="a96fa-178">Indicates how many times an attempt to access a locked page is repeated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-179">Размер буфера OLEDB:Max Jet</span><span class="sxs-lookup"><span data-stu-id="a96fa-179">Jet OLEDB:Max Buffer Size</span></span><br />
<span data-ttu-id="a96fa-180">(DBPROP_JETOLEDB_MAXBUFFERSIZE)</span><span class="sxs-lookup"><span data-stu-id="a96fa-180">(DBPROP_JETOLEDB_MAXBUFFERSIZE)</span></span></p></td>
<td><p><span data-ttu-id="a96fa-181">Указывает максимальный объем памяти, в килобайтах Jet может использовать до начала записи изменений на диск.</span><span class="sxs-lookup"><span data-stu-id="a96fa-181">Indicates the maximum amount of memory, in kilobytes, Jet can use before it starts flushing changes to disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-182">Jet OLEDB:Max блокировок в файл</span><span class="sxs-lookup"><span data-stu-id="a96fa-182">Jet OLEDB:Max Locks Per File</span></span><br />
<span data-ttu-id="a96fa-183">(DBPROP_JETOLEDB_MAXLOCKSPERFILE)</span><span class="sxs-lookup"><span data-stu-id="a96fa-183">(DBPROP_JETOLEDB_MAXLOCKSPERFILE)</span></span></p></td>
<td><p><span data-ttu-id="a96fa-184">Указывает максимальное количество блокировок, которые Jet можно поместить в базе данных.</span><span class="sxs-lookup"><span data-stu-id="a96fa-184">Indicates the maximum number of locks Jet can place on a database.</span></span> <span data-ttu-id="a96fa-185">Значение по умолчанию — 9500.</span><span class="sxs-lookup"><span data-stu-id="a96fa-185">The default value is 9500.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-186">Jet OLEDB: новый пароль базы данных</span><span class="sxs-lookup"><span data-stu-id="a96fa-186">Jet OLEDB:New Database Password</span></span><br />
<span data-ttu-id="a96fa-187">(DBPROP_JETOLEDB_NEWDATABASEPASSWORD)</span><span class="sxs-lookup"><span data-stu-id="a96fa-187">(DBPROP_JETOLEDB_NEWDATABASEPASSWORD)</span></span></p></td>
<td><p><span data-ttu-id="a96fa-188">Указывает новый пароль для этой базы данных.</span><span class="sxs-lookup"><span data-stu-id="a96fa-188">Indicates the new password to be set for this database.</span></span> <span data-ttu-id="a96fa-189">Старый пароль хранится в <strong>Jet OLEDB:Database пароль</strong>.</span><span class="sxs-lookup"><span data-stu-id="a96fa-189">The old password is stored in <strong>Jet OLEDB:Database Password</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-190">Время ожидания команды OLEDB:ODBC Jet</span><span class="sxs-lookup"><span data-stu-id="a96fa-190">Jet OLEDB:ODBC Command Time Out</span></span><br />
<span data-ttu-id="a96fa-191">(DBPROP_JETOLEDB_ODBCCOMMANDTIMEOUT)</span><span class="sxs-lookup"><span data-stu-id="a96fa-191">(DBPROP_JETOLEDB_ODBCCOMMANDTIMEOUT)</span></span></p></td>
<td><p><span data-ttu-id="a96fa-192">Указывает, что количество миллисекунд до удаленный запрос ODBC с Jet будет времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="a96fa-192">Indicates the number of milliseconds before a remote ODBC query from Jet will timeout.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-193">Блокировки OLEDB:Page Jet для блокировки таблицы</span><span class="sxs-lookup"><span data-stu-id="a96fa-193">Jet OLEDB:Page Locks to Table Lock</span></span><br />
<span data-ttu-id="a96fa-194">(DBPROP_JETOLEDB_PAGELOCKSTOTABLELOCK)</span><span class="sxs-lookup"><span data-stu-id="a96fa-194">(DBPROP_JETOLEDB_PAGELOCKSTOTABLELOCK)</span></span></p></td>
<td><p><span data-ttu-id="a96fa-195">Указывает, сколько страниц необходимо будут удалены в транзакции, прежде чем повышение уровня блокировки для блокировки таблицы.</span><span class="sxs-lookup"><span data-stu-id="a96fa-195">Indicates how many pages need to be locked within a transaction before Jet attempts to promote the lock to a table lock.</span></span> <span data-ttu-id="a96fa-196">Если это значение равно 0, блокировки никогда не повышается.</span><span class="sxs-lookup"><span data-stu-id="a96fa-196">If this value is 0, then the lock is never promoted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-197">Время ожидания OLEDB:Page Jet</span><span class="sxs-lookup"><span data-stu-id="a96fa-197">Jet OLEDB:Page Timeout</span></span><br />
<span data-ttu-id="a96fa-198">(DBPROP_JETOLEDB_PAGETIMEOUT)</span><span class="sxs-lookup"><span data-stu-id="a96fa-198">(DBPROP_JETOLEDB_PAGETIMEOUT)</span></span></p></td>
<td><p><span data-ttu-id="a96fa-199">Указывает количество миллисекунд ожидания Jet перед проверкой ли кэш устаревший с помощью файла базы данных.</span><span class="sxs-lookup"><span data-stu-id="a96fa-199">Indicates the number of milliseconds Jet will wait before checking to see if its cache is out of date with the database file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-200">Страницы табличное Long Jet OLEDB:Recycle</span><span class="sxs-lookup"><span data-stu-id="a96fa-200">Jet OLEDB:Recycle Long-Valued Pages</span></span><br />
<span data-ttu-id="a96fa-201">(DBPROP_JETOLEDB_RECYCLELONGVALUEPAGES)</span><span class="sxs-lookup"><span data-stu-id="a96fa-201">(DBPROP_JETOLEDB_RECYCLELONGVALUEPAGES)</span></span></p></td>
<td><p><span data-ttu-id="a96fa-202">Указывает, следует ли Jet пытаться агрессивное освобождение страниц больших двоичных ОБЪЕКТОВ, когда их освобождения.</span><span class="sxs-lookup"><span data-stu-id="a96fa-202">Indicates whether Jet should aggressively try to reclaim BLOB pages when they are freed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-203">Путь OLEDB:Registry Jet</span><span class="sxs-lookup"><span data-stu-id="a96fa-203">Jet OLEDB:Registry Path</span></span><br />
<span data-ttu-id="a96fa-204">(DBPROP_JETOLEDB_REGPATH)</span><span class="sxs-lookup"><span data-stu-id="a96fa-204">(DBPROP_JETOLEDB_REGPATH)</span></span></p></td>
<td><p><span data-ttu-id="a96fa-205">Указывает ключ реестра Windows, который содержит значения для базы данных Jet.</span><span class="sxs-lookup"><span data-stu-id="a96fa-205">Indicates the Windows registry key that contains values for the Jet database engine.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-206">Статистика ISAM OLEDB:Reset Jet</span><span class="sxs-lookup"><span data-stu-id="a96fa-206">Jet OLEDB:Reset ISAM Stats</span></span><br />
<span data-ttu-id="a96fa-207">(DBPROP_JETOLEDB_RESETISAMSTATS)</span><span class="sxs-lookup"><span data-stu-id="a96fa-207">(DBPROP_JETOLEDB_RESETISAMSTATS)</span></span></p></td>
<td><p><span data-ttu-id="a96fa-208">Указывает, должно ли схема <strong>набора записей</strong> DBSCHEMA_JETOLEDB_ISAMSTATS сбросить его счетчики производительности после возврата сведений о производительности.</span><span class="sxs-lookup"><span data-stu-id="a96fa-208">Indicates whether the schema <strong>Recordset</strong> DBSCHEMA_JETOLEDB_ISAMSTATS should reset its performance counters after returning performance information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-209">Jet OLEDB: общих асинхронная задержка</span><span class="sxs-lookup"><span data-stu-id="a96fa-209">Jet OLEDB:Shared Async Delay</span></span><br />
<span data-ttu-id="a96fa-210">(DBPROP_JETOLEDB_SHAREDASYNCDELAY)</span><span class="sxs-lookup"><span data-stu-id="a96fa-210">(DBPROP_JETOLEDB_SHAREDASYNCDELAY)</span></span></p></td>
<td><p><span data-ttu-id="a96fa-211">Указывает максимальное время в миллисекундах, Jet может отложить асинхронных операций записи на диск при открытии базы данных в режиме нескольких пользователей.</span><span class="sxs-lookup"><span data-stu-id="a96fa-211">Indicates the maximum amount of time, in milliseconds, Jet can delay asynchronous writes to disk when the database is opened in multi-user mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-212">База данных Microsoft Jet OLEDB: System</span><span class="sxs-lookup"><span data-stu-id="a96fa-212">Jet OLEDB:System Database</span></span><br />
<span data-ttu-id="a96fa-213">(DBPROP_JETOLEDB_SYSDBPATH)</span><span class="sxs-lookup"><span data-stu-id="a96fa-213">(DBPROP_JETOLEDB_SYSDBPATH)</span></span></p></td>
<td><p><span data-ttu-id="a96fa-214">Указывает путь и имя файла для файла рабочей группы (системная база данных).</span><span class="sxs-lookup"><span data-stu-id="a96fa-214">Indicates the path and file name for the workgroup information file (system database).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-215">Режим фиксации OLEDB:Transaction Jet</span><span class="sxs-lookup"><span data-stu-id="a96fa-215">Jet OLEDB:Transaction Commit Mode</span></span><br />
<span data-ttu-id="a96fa-216">(DBPROP_JETOLEDB_TXNCOMMITMODE)</span><span class="sxs-lookup"><span data-stu-id="a96fa-216">(DBPROP_JETOLEDB_TXNCOMMITMODE)</span></span></p></td>
<td><p><span data-ttu-id="a96fa-217">Указывает, является ли Jet записывает данные на диск синхронно или асинхронно при фиксации транзакции.</span><span class="sxs-lookup"><span data-stu-id="a96fa-217">Indicates whether Jet writes data to disk synchronously or asynchronously when a transaction is committed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-218">Синхронизация зафиксировать OLEDB:User Jet</span><span class="sxs-lookup"><span data-stu-id="a96fa-218">Jet OLEDB:User Commit Sync</span></span><br />
<span data-ttu-id="a96fa-219">(DBPROP_JETOLEDB_USERCOMMITSYNC)</span><span class="sxs-lookup"><span data-stu-id="a96fa-219">(DBPROP_JETOLEDB_USERCOMMITSYNC)</span></span></p></td>
<td><p><span data-ttu-id="a96fa-220">Указывает, записываются ли изменения, внесенные в транзакции в режиме синхронными и асинхронными.</span><span class="sxs-lookup"><span data-stu-id="a96fa-220">Indicates whether changes made in transactions are written in synchronous or asynchronous mode.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-recordset-and-command-properties"></a><span data-ttu-id="a96fa-221">Свойства команды и записей от поставщика</span><span class="sxs-lookup"><span data-stu-id="a96fa-221">Provider-Specific Recordset and Command Properties</span></span>

<span data-ttu-id="a96fa-222">Поставщик Jet также поддерживает несколько свойств **набора записей** и **команду** от поставщика.</span><span class="sxs-lookup"><span data-stu-id="a96fa-222">The Jet provider also supports several provider-specific **Recordset** and **Command** properties.</span></span> <span data-ttu-id="a96fa-223">Эти свойства доступны и задается с помощью коллекции **свойств** объекта **команду** или **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="a96fa-223">These properties are accessed and set through the **Properties** collection of the **Recordset** or **Command** object.</span></span> <span data-ttu-id="a96fa-224">В таблице перечислены имя свойства ADO и OLE DB название в скобки.</span><span class="sxs-lookup"><span data-stu-id="a96fa-224">The table lists the ADO property name and its corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a96fa-225">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="a96fa-225">Property Name</span></span></p></th>
<th><p><span data-ttu-id="a96fa-226">Описание</span><span class="sxs-lookup"><span data-stu-id="a96fa-226">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-227">Транзакции OLEDB:Bulk Jet</span><span class="sxs-lookup"><span data-stu-id="a96fa-227">Jet OLEDB:Bulk Transactions</span></span><br />
<span data-ttu-id="a96fa-228">(DBPROP_JETOLEDB_BULKNOTRANSACTIONS)</span><span class="sxs-lookup"><span data-stu-id="a96fa-228">(DBPROP_JETOLEDB_BULKNOTRANSACTIONS)</span></span></p></td>
<td><p><span data-ttu-id="a96fa-229">Указывает, будет ли в рамках транзакции SQL массовых операций.</span><span class="sxs-lookup"><span data-stu-id="a96fa-229">Indicates whether SQL bulk operations are transacted.</span></span> <span data-ttu-id="a96fa-230">Больших массовых операций может завершиться неудачно в рамках транзакции, из-за задержки ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a96fa-230">Large bulk operations might fail when transacted, due to resource delays.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-231">Курсоры Fat OLEDB:Enable Jet</span><span class="sxs-lookup"><span data-stu-id="a96fa-231">Jet OLEDB:Enable Fat Cursors</span></span><br />
<span data-ttu-id="a96fa-232">(DBPROP_JETOLEDB_ENABLEFATCURSOR)</span><span class="sxs-lookup"><span data-stu-id="a96fa-232">(DBPROP_JETOLEDB_ENABLEFATCURSOR)</span></span></p></td>
<td><p><span data-ttu-id="a96fa-233">Указывает, следует ли Jet кэшировать несколько строк при заполнении набора записей для источников удаленной строки.</span><span class="sxs-lookup"><span data-stu-id="a96fa-233">Indicates whether Jet should cache multiple rows when populating a recordset for remote row sources.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-234">Размер кэша курсор OLEDB:Fat Jet</span><span class="sxs-lookup"><span data-stu-id="a96fa-234">Jet OLEDB:Fat Cursor Cache Size</span></span><br />
<span data-ttu-id="a96fa-235">(DBPROP_JETOLEDB_FATCURSORMAXROWS)</span><span class="sxs-lookup"><span data-stu-id="a96fa-235">(DBPROP_JETOLEDB_FATCURSORMAXROWS)</span></span></p></td>
<td><p><span data-ttu-id="a96fa-236">Указывает число строк, кэш при использовании кэширования строку хранения удаленных данных.</span><span class="sxs-lookup"><span data-stu-id="a96fa-236">Indicates the number of rows to cache when using remote data store row caching.</span></span> <span data-ttu-id="a96fa-237">Это значение используется только <strong>Fat курсоры Jet OLEDB:Enable</strong> имеет значение True.</span><span class="sxs-lookup"><span data-stu-id="a96fa-237">This value is ignored unless <strong>Jet OLEDB:Enable Fat Cursors</strong> is True.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-238">Jet OLEDB: несогласованные</span><span class="sxs-lookup"><span data-stu-id="a96fa-238">Jet OLEDB:Inconsistent</span></span><br />
<span data-ttu-id="a96fa-239">(DBPROP_JETOLEDB_INCONSISTENT)</span><span class="sxs-lookup"><span data-stu-id="a96fa-239">(DBPROP_JETOLEDB_INCONSISTENT)</span></span></p></td>
<td><p><span data-ttu-id="a96fa-240">Указывает, разрешить ли результаты запроса несогласованных обновлений.</span><span class="sxs-lookup"><span data-stu-id="a96fa-240">Indicates whether query results allow inconsistent updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-241">Jet OLEDB: блокировка степень детализации</span><span class="sxs-lookup"><span data-stu-id="a96fa-241">Jet OLEDB:Locking Granularity</span></span><br />
<span data-ttu-id="a96fa-242">(DBPROP_JETOLEDB_LOCKGRANULARITY)</span><span class="sxs-lookup"><span data-stu-id="a96fa-242">(DBPROP_JETOLEDB_LOCKGRANULARITY)</span></span></p></td>
<td><p><span data-ttu-id="a96fa-243">Указывает, открыт ли таблицы с помощью блокировка на уровне.</span><span class="sxs-lookup"><span data-stu-id="a96fa-243">Indicates whether a table is opened using row-level locking.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-244">Оператор к серверу OLEDB:ODBC Jet</span><span class="sxs-lookup"><span data-stu-id="a96fa-244">Jet OLEDB:ODBC Pass-Through Statement</span></span><br />
<span data-ttu-id="a96fa-245">(DBPROP_JETOLEDB_ODBCPASSTHROUGH)</span><span class="sxs-lookup"><span data-stu-id="a96fa-245">(DBPROP_JETOLEDB_ODBCPASSTHROUGH)</span></span></p></td>
<td><p><span data-ttu-id="a96fa-246">Указывает, что Jet должен передаваться текст SQL в объект <strong>команды</strong> для серверного компонента без изменений.</span><span class="sxs-lookup"><span data-stu-id="a96fa-246">Indicates that Jet should pass the SQL text in a <strong>Command</strong> object to the back end unaltered.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-247">Jet OLEDB:Partial массовых операций</span><span class="sxs-lookup"><span data-stu-id="a96fa-247">Jet OLEDB:Partial Bulk Ops</span></span><br />
<span data-ttu-id="a96fa-248">(DBPROP_JETOLEDB_BULKPARTIAL)</span><span class="sxs-lookup"><span data-stu-id="a96fa-248">(DBPROP_JETOLEDB_BULKPARTIAL)</span></span></p></td>
<td><p><span data-ttu-id="a96fa-249">Задает поведение Jet при операции SQL DML с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="a96fa-249">Indicates Jet's behavior when SQL DML operations fail.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-250">OLEDB:Pass Jet через массовых операций запросов</span><span class="sxs-lookup"><span data-stu-id="a96fa-250">Jet OLEDB:Pass Through Query Bulk-Op</span></span><br />
<span data-ttu-id="a96fa-251">(DBPROP_JETOLEDB_PASSTHROUGHBULKOP)</span><span class="sxs-lookup"><span data-stu-id="a96fa-251">(DBPROP_JETOLEDB_PASSTHROUGHBULKOP)</span></span></p></td>
<td><p><span data-ttu-id="a96fa-252">Указывает, запросов, которые не возвращает <strong>записей</strong> передаются ли изменена к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="a96fa-252">Indicates whether queries that do not return a <strong>Recordset</strong> are passed unaltered to the data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-253">Строка подключения OLEDB:Pass Jet посредством запроса</span><span class="sxs-lookup"><span data-stu-id="a96fa-253">Jet OLEDB:Pass Through Query Connect String</span></span><br />
<span data-ttu-id="a96fa-254">(DBPROP_JETOLEDB_ODBCPASSTHROUGHCONNECTSTRING)</span><span class="sxs-lookup"><span data-stu-id="a96fa-254">(DBPROP_JETOLEDB_ODBCPASSTHROUGHCONNECTSTRING)</span></span></p></td>
<td><p><span data-ttu-id="a96fa-255">Указывает Jet строку подключения, используемую для подключения к удаленному хранилищу.</span><span class="sxs-lookup"><span data-stu-id="a96fa-255">Indicates the Jet connect string used to connect to a remote data store.</span></span> <span data-ttu-id="a96fa-256">Это значение используется только <strong>Jet OLEDB:ODBC к серверу оператор</strong> имеет значение True.</span><span class="sxs-lookup"><span data-stu-id="a96fa-256">This value is ignored unless <strong>Jet OLEDB:ODBC Pass-Through Statement</strong> is True.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-257">Jet OLEDB: хранимых запросов</span><span class="sxs-lookup"><span data-stu-id="a96fa-257">Jet OLEDB:Stored Query</span></span><br />
<span data-ttu-id="a96fa-258">(DBPROP_JETOLEDB_STOREDQUERY)</span><span class="sxs-lookup"><span data-stu-id="a96fa-258">(DBPROP_JETOLEDB_STOREDQUERY)</span></span></p></td>
<td><p><span data-ttu-id="a96fa-259">Указывает, будет ли текст команды должны обрабатываются как сохраненного запроса вместо команды SQL.</span><span class="sxs-lookup"><span data-stu-id="a96fa-259">Indicates whether the command text should be interpreted as a stored query instead of an SQL command.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-260">Jet OLEDB: проверка правил набора</span><span class="sxs-lookup"><span data-stu-id="a96fa-260">Jet OLEDB:Validate Rules On Set</span></span><br />
<span data-ttu-id="a96fa-261">(DBPROP_JETOLEDB_VALIDATEONSET)</span><span class="sxs-lookup"><span data-stu-id="a96fa-261">(DBPROP_JETOLEDB_VALIDATEONSET)</span></span></p></td>
<td><p><span data-ttu-id="a96fa-262">Указывает, будет ли правила проверки Jet вычисляются при имеет значение столбца или изменения применяются к базе данных.</span><span class="sxs-lookup"><span data-stu-id="a96fa-262">Indicates whether the Jet validation rules are evaluated when column data is set or when the changes are committed to the database.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a96fa-263">По умолчанию поставщик OLE DB для Microsoft Jet открывается в режиме чтения и записи баз данных Microsoft Jet.</span><span class="sxs-lookup"><span data-stu-id="a96fa-263">By default, the OLE DB Provider for Microsoft Jet opens Microsoft Jet databases in read/write mode.</span></span> <span data-ttu-id="a96fa-264">Чтобы открыть базу данных в режим только для чтения, присвойте свойству [режим](mode-property-ado.md) объекта ADO- **подключения** в **adModeRead**.</span><span class="sxs-lookup"><span data-stu-id="a96fa-264">To open a database in read-only mode, set the [Mode](mode-property-ado.md) property on the ADO **Connection** object to **adModeRead**.</span></span>

## <a name="command-object-usage"></a><span data-ttu-id="a96fa-265">Использование объекта команды</span><span class="sxs-lookup"><span data-stu-id="a96fa-265">Command Object Usage</span></span>

<span data-ttu-id="a96fa-266">Текст команды в объекте [команда](command-object-ado.md) использует диалект Microsoft Jet SQL.</span><span class="sxs-lookup"><span data-stu-id="a96fa-266">Command text in the [Command](command-object-ado.md) object uses the Microsoft Jet SQL dialect.</span></span> <span data-ttu-id="a96fa-267">Можно указать возвращающие строки запросов, запросов и имена таблиц в текст команды; Тем не менее хранимые процедуры не поддерживаются и не должен быть указан.</span><span class="sxs-lookup"><span data-stu-id="a96fa-267">You can specify row-returning queries, action queries, and table names in the command text; however, stored procedures are not supported and should not be specified.</span></span>

## <a name="recordset-behavior"></a><span data-ttu-id="a96fa-268">Поведение набора записей</span><span class="sxs-lookup"><span data-stu-id="a96fa-268">Recordset Behavior</span></span>

<span data-ttu-id="a96fa-269">Базы данных Microsoft Jet не поддерживает динамические курсоры.</span><span class="sxs-lookup"><span data-stu-id="a96fa-269">The Microsoft Jet database engine does not support dynamic cursors.</span></span> <span data-ttu-id="a96fa-270">Таким образом поставщик OLE DB для Microsoft Jet не поддерживает тип **adLockDynamic** курсора.</span><span class="sxs-lookup"><span data-stu-id="a96fa-270">Therefore, the OLE DB Provider for Microsoft Jet does not support the **adLockDynamic** cursor type.</span></span> <span data-ttu-id="a96fa-271">При запросе динамического курсора поставщик вернуть курсор набора ключей и сброс свойство [CursorType](cursortype-property-ado.md) указывает, что возвращаемые тип [набора записей](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="a96fa-271">When a dynamic cursor is requested, the provider will return a keyset cursor and reset the [CursorType](cursortype-property-ado.md) property to indicate the type of [Recordset](recordset-object-ado.md) returned.</span></span> <span data-ttu-id="a96fa-272">Затем, если запрашивается обновляемых **записей** (**LockType для** — **adLockOptimistic**, **adLockBatchOptimistic**или **adLockPessimistic**) также вернет курсор набора ключей и Сброс **CursorType** поставщика свойство.</span><span class="sxs-lookup"><span data-stu-id="a96fa-272">Further, if an updatable **Recordset** is requested (**LockType** is **adLockOptimistic**, **adLockBatchOptimistic**, or **adLockPessimistic**) the provider will also return a keyset cursor and reset the **CursorType** property.</span></span>

## <a name="dynamic-properties"></a><span data-ttu-id="a96fa-273">Динамические свойства</span><span class="sxs-lookup"><span data-stu-id="a96fa-273">Dynamic Properties</span></span>

<span data-ttu-id="a96fa-274">Поставщик OLE DB для Microsoft Jet вставляет несколько динамических свойств в коллекцию **свойств** объектов неоткрытый [подключения](connection-object-ado.md), [записей](recordset-object-ado.md)и [команды](command-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="a96fa-274">The OLE DB Provider for Microsoft Jet inserts several dynamic properties into the **Properties** collection of the unopened [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md), and [Command](command-object-ado.md) objects.</span></span>

<span data-ttu-id="a96fa-275">В таблицах ниже — это cross-index имен ADO и OLE DB для каждого динамического свойства.</span><span class="sxs-lookup"><span data-stu-id="a96fa-275">The tables below are a cross-index of the ADO and OLE DB names for each dynamic property.</span></span> <span data-ttu-id="a96fa-276">Справочник программиста OLE DB указано имя свойства ADO по слову «Описание».</span><span class="sxs-lookup"><span data-stu-id="a96fa-276">The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description."</span></span> <span data-ttu-id="a96fa-277">Дополнительные сведения об этих свойств можно найти в Справочник программиста OLE DB.</span><span class="sxs-lookup"><span data-stu-id="a96fa-277">You can find more information about these properties in the OLE DB Programmer's Reference.</span></span> <span data-ttu-id="a96fa-278">Поиск имени свойства OLE DB в индексе или просмотреть приложение C: OLE DB свойства.</span><span class="sxs-lookup"><span data-stu-id="a96fa-278">Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span></span>

## <a name="connection-dynamic-properties"></a><span data-ttu-id="a96fa-279">Динамические свойства подключения</span><span class="sxs-lookup"><span data-stu-id="a96fa-279">Connection Dynamic Properties</span></span>

<span data-ttu-id="a96fa-280">Коллекция **Properties** объект **подключения** добавляются следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a96fa-280">The following properties are added to the **Connection** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a96fa-281">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="a96fa-281">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="a96fa-282">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="a96fa-282">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-283">Активных сеансов</span><span class="sxs-lookup"><span data-stu-id="a96fa-283">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="a96fa-284">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="a96fa-284">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-285">Прерывание Asynchable</span><span class="sxs-lookup"><span data-stu-id="a96fa-285">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="a96fa-286">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="a96fa-286">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-287">Зафиксировать Asynchable</span><span class="sxs-lookup"><span data-stu-id="a96fa-287">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="a96fa-288">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="a96fa-288">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-289">Уровни изоляции автоматической фиксации</span><span class="sxs-lookup"><span data-stu-id="a96fa-289">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="a96fa-290">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="a96fa-290">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-291">Расположение каталога</span><span class="sxs-lookup"><span data-stu-id="a96fa-291">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="a96fa-292">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="a96fa-292">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-293">Каталог терминов</span><span class="sxs-lookup"><span data-stu-id="a96fa-293">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="a96fa-294">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="a96fa-294">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-295">Определение столбца</span><span class="sxs-lookup"><span data-stu-id="a96fa-295">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="a96fa-296">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="a96fa-296">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-297">Текущий каталог</span><span class="sxs-lookup"><span data-stu-id="a96fa-297">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="a96fa-298">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="a96fa-298">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-299">Источник данных</span><span class="sxs-lookup"><span data-stu-id="a96fa-299">Data Source</span></span></p></td>
<td><p><span data-ttu-id="a96fa-300">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="a96fa-300">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-301">Имя источника данных</span><span class="sxs-lookup"><span data-stu-id="a96fa-301">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="a96fa-302">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="a96fa-302">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-303">Модель потоков объекта источника данных</span><span class="sxs-lookup"><span data-stu-id="a96fa-303">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="a96fa-304">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="a96fa-304">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-305">Имя СУБД</span><span class="sxs-lookup"><span data-stu-id="a96fa-305">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="a96fa-306">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="a96fa-306">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-307">Версия СУБД</span><span class="sxs-lookup"><span data-stu-id="a96fa-307">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="a96fa-308">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="a96fa-308">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-309">ГРУППИРОВКА по поддержке</span><span class="sxs-lookup"><span data-stu-id="a96fa-309">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="a96fa-310">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="a96fa-310">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-311">Поддержка разнородных таблиц</span><span class="sxs-lookup"><span data-stu-id="a96fa-311">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="a96fa-312">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="a96fa-312">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-313">Идентификатор регистра</span><span class="sxs-lookup"><span data-stu-id="a96fa-313">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="a96fa-314">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="a96fa-314">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-315">Уровни изоляции</span><span class="sxs-lookup"><span data-stu-id="a96fa-315">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="a96fa-316">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="a96fa-316">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-317">Хранение изоляции</span><span class="sxs-lookup"><span data-stu-id="a96fa-317">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="a96fa-318">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="a96fa-318">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-319">Идентификатор языка</span><span class="sxs-lookup"><span data-stu-id="a96fa-319">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="a96fa-320">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="a96fa-320">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-321">Максимальный размер индекса</span><span class="sxs-lookup"><span data-stu-id="a96fa-321">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="a96fa-322">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="a96fa-322">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-323">Максимальный размер строки</span><span class="sxs-lookup"><span data-stu-id="a96fa-323">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="a96fa-324">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="a96fa-324">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-325">Максимальный размер строки включает в себя больших двоичных ОБЪЕКТОВ</span><span class="sxs-lookup"><span data-stu-id="a96fa-325">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="a96fa-326">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="a96fa-326">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-327">Максимальная таблиц в Выбор</span><span class="sxs-lookup"><span data-stu-id="a96fa-327">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="a96fa-328">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="a96fa-328">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-329">Режим</span><span class="sxs-lookup"><span data-stu-id="a96fa-329">Mode</span></span></p></td>
<td><p><span data-ttu-id="a96fa-330">DBPROP_INIT_MODE</span><span class="sxs-lookup"><span data-stu-id="a96fa-330">DBPROP_INIT_MODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-331">Несколько наборов параметров</span><span class="sxs-lookup"><span data-stu-id="a96fa-331">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="a96fa-332">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="a96fa-332">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-333">Несколько результатов</span><span class="sxs-lookup"><span data-stu-id="a96fa-333">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="a96fa-334">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="a96fa-334">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-335">Несколько объектов хранения</span><span class="sxs-lookup"><span data-stu-id="a96fa-335">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="a96fa-336">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="a96fa-336">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-337">Обновление нескольких таблицы</span><span class="sxs-lookup"><span data-stu-id="a96fa-337">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="a96fa-338">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="a96fa-338">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-339">Порядок сортировки значений NULL</span><span class="sxs-lookup"><span data-stu-id="a96fa-339">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="a96fa-340">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="a96fa-340">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-341">Поведение NULL объединения</span><span class="sxs-lookup"><span data-stu-id="a96fa-341">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="a96fa-342">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="a96fa-342">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-343">Версия OLE DB</span><span class="sxs-lookup"><span data-stu-id="a96fa-343">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="a96fa-344">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="a96fa-344">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-345">Поддержка OLE-объектов</span><span class="sxs-lookup"><span data-stu-id="a96fa-345">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="a96fa-346">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="a96fa-346">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-347">Поддержка открытых наборов строк</span><span class="sxs-lookup"><span data-stu-id="a96fa-347">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="a96fa-348">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="a96fa-348">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-349">ORDER BY столбцы в списке Select</span><span class="sxs-lookup"><span data-stu-id="a96fa-349">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="a96fa-350">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="a96fa-350">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-351">Выходной параметр доступности</span><span class="sxs-lookup"><span data-stu-id="a96fa-351">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="a96fa-352">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="a96fa-352">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-353">Передайте с указанные методы</span><span class="sxs-lookup"><span data-stu-id="a96fa-353">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="a96fa-354">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="a96fa-354">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-355">Password</span><span class="sxs-lookup"><span data-stu-id="a96fa-355">Password</span></span></p></td>
<td><p><span data-ttu-id="a96fa-356">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="a96fa-356">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-357">Тип сохраняемого идентификатора</span><span class="sxs-lookup"><span data-stu-id="a96fa-357">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="a96fa-358">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="a96fa-358">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-359">Подготовка поведение аварийное завершение</span><span class="sxs-lookup"><span data-stu-id="a96fa-359">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="a96fa-360">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="a96fa-360">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-361">Подготовка поведение выделения</span><span class="sxs-lookup"><span data-stu-id="a96fa-361">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="a96fa-362">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="a96fa-362">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-363">Процедура терминов</span><span class="sxs-lookup"><span data-stu-id="a96fa-363">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="a96fa-364">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="a96fa-364">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-365">Запрос</span><span class="sxs-lookup"><span data-stu-id="a96fa-365">Prompt</span></span></p></td>
<td><p><span data-ttu-id="a96fa-366">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="a96fa-366">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-367">Понятное имя поставщика</span><span class="sxs-lookup"><span data-stu-id="a96fa-367">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="a96fa-368">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="a96fa-368">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-369">Имя поставщика</span><span class="sxs-lookup"><span data-stu-id="a96fa-369">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="a96fa-370">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="a96fa-370">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-371">Версия поставщика</span><span class="sxs-lookup"><span data-stu-id="a96fa-371">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="a96fa-372">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="a96fa-372">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-373">Источник данных только для чтения</span><span class="sxs-lookup"><span data-stu-id="a96fa-373">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="a96fa-374">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="a96fa-374">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-375">Преобразование строк на команду</span><span class="sxs-lookup"><span data-stu-id="a96fa-375">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="a96fa-376">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="a96fa-376">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-377">Схема терминов</span><span class="sxs-lookup"><span data-stu-id="a96fa-377">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="a96fa-378">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="a96fa-378">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-379">Об использовании схемы</span><span class="sxs-lookup"><span data-stu-id="a96fa-379">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="a96fa-380">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="a96fa-380">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-381">Поддержка SQL</span><span class="sxs-lookup"><span data-stu-id="a96fa-381">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="a96fa-382">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="a96fa-382">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-383">Структурированное хранилище</span><span class="sxs-lookup"><span data-stu-id="a96fa-383">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="a96fa-384">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="a96fa-384">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-385">Поддержка вложенного запроса</span><span class="sxs-lookup"><span data-stu-id="a96fa-385">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="a96fa-386">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="a96fa-386">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-387">В таблице терминов</span><span class="sxs-lookup"><span data-stu-id="a96fa-387">Table Term</span></span></p></td>
<td><p><span data-ttu-id="a96fa-388">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="a96fa-388">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-389">Транзакций DDL</span><span class="sxs-lookup"><span data-stu-id="a96fa-389">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="a96fa-390">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="a96fa-390">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-391">Идентификатор пользователя</span><span class="sxs-lookup"><span data-stu-id="a96fa-391">User ID</span></span></p></td>
<td><p><span data-ttu-id="a96fa-392">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="a96fa-392">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-393">Имя пользователя</span><span class="sxs-lookup"><span data-stu-id="a96fa-393">User Name</span></span></p></td>
<td><p><span data-ttu-id="a96fa-394">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="a96fa-394">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-395">Дескриптор окна</span><span class="sxs-lookup"><span data-stu-id="a96fa-395">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="a96fa-396">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="a96fa-396">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a><span data-ttu-id="a96fa-397">Свойства динамической набора записей</span><span class="sxs-lookup"><span data-stu-id="a96fa-397">Recordset Dynamic Properties</span></span>

<span data-ttu-id="a96fa-398">Следующие свойства добавляются в коллекцию **свойств** объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="a96fa-398">The following properties are added to the **Recordset** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a96fa-399">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="a96fa-399">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="a96fa-400">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="a96fa-400">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-401">Порядок доступа</span><span class="sxs-lookup"><span data-stu-id="a96fa-401">Access Order</span></span></p></td>
<td><p><span data-ttu-id="a96fa-402">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="a96fa-402">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-403">Только для добавления строк</span><span class="sxs-lookup"><span data-stu-id="a96fa-403">Append-Only Rowset</span></span></p></td>
<td><p><span data-ttu-id="a96fa-404">DBPROP_APPENDONLY</span><span class="sxs-lookup"><span data-stu-id="a96fa-404">DBPROP_APPENDONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-405">Блокировка объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="a96fa-405">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="a96fa-406">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="a96fa-406">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-407">Тип закладки</span><span class="sxs-lookup"><span data-stu-id="a96fa-407">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="a96fa-408">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="a96fa-408">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-409">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="a96fa-409">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="a96fa-410">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="a96fa-410">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-411">Упорядоченные закладки</span><span class="sxs-lookup"><span data-stu-id="a96fa-411">Bookmarks Ordered</span></span></p></td>
<td><p><span data-ttu-id="a96fa-412">DBPROP_ORDEREDBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="a96fa-412">DBPROP_ORDEREDBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-413">Кэш отложенной столбцов</span><span class="sxs-lookup"><span data-stu-id="a96fa-413">Cache Deferred Columns</span></span></p></td>
<td><p><span data-ttu-id="a96fa-414">DBPROP_CACHEDEFERRED</span><span class="sxs-lookup"><span data-stu-id="a96fa-414">DBPROP_CACHEDEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-415">Изменение вставленных строк</span><span class="sxs-lookup"><span data-stu-id="a96fa-415">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="a96fa-416">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="a96fa-416">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-417">Права доступа столбца</span><span class="sxs-lookup"><span data-stu-id="a96fa-417">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="a96fa-418">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="a96fa-418">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-419">Столбец набор уведомлений</span><span class="sxs-lookup"><span data-stu-id="a96fa-419">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="a96fa-420">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="a96fa-420">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-421">Столбец для записи</span><span class="sxs-lookup"><span data-stu-id="a96fa-421">Column Writable</span></span></p></td>
<td><p><span data-ttu-id="a96fa-422">DBPROP_MAYWRITECOLUMN</span><span class="sxs-lookup"><span data-stu-id="a96fa-422">DBPROP_MAYWRITECOLUMN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-423">Отложите столбца</span><span class="sxs-lookup"><span data-stu-id="a96fa-423">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="a96fa-424">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="a96fa-424">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-425">Отложенное обновление объекта хранения</span><span class="sxs-lookup"><span data-stu-id="a96fa-425">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="a96fa-426">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="a96fa-426">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-427">Выборку</span><span class="sxs-lookup"><span data-stu-id="a96fa-427">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="a96fa-428">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="a96fa-428">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-429">Хранение строк</span><span class="sxs-lookup"><span data-stu-id="a96fa-429">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="a96fa-430">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="a96fa-430">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-431">IAccessor</span><span class="sxs-lookup"><span data-stu-id="a96fa-431">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="a96fa-432">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="a96fa-432">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-433">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="a96fa-433">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="a96fa-434">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="a96fa-434">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-435">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="a96fa-435">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="a96fa-436">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="a96fa-436">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-437">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="a96fa-437">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="a96fa-438">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="a96fa-438">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-439">IConvertType</span><span class="sxs-lookup"><span data-stu-id="a96fa-439">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="a96fa-440">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="a96fa-440">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-441">ILockBytes</span><span class="sxs-lookup"><span data-stu-id="a96fa-441">ILockBytes</span></span></p></td>
<td><p><span data-ttu-id="a96fa-442">DBPROP_ILockBytes</span><span class="sxs-lookup"><span data-stu-id="a96fa-442">DBPROP_ILockBytes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-443">Немобильные строки</span><span class="sxs-lookup"><span data-stu-id="a96fa-443">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="a96fa-444">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="a96fa-444">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-445">IRowset</span><span class="sxs-lookup"><span data-stu-id="a96fa-445">IRowset</span></span></p></td>
<td><p><span data-ttu-id="a96fa-446">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="a96fa-446">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-447">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="a96fa-447">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="a96fa-448">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="a96fa-448">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-449">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="a96fa-449">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="a96fa-450">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="a96fa-450">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-451">IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="a96fa-451">IRowsetIndex</span></span></p></td>
<td><p><span data-ttu-id="a96fa-452">DBPROP_IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="a96fa-452">DBPROP_IRowsetIndex</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-453">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="a96fa-453">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="a96fa-454">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="a96fa-454">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-455">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="a96fa-455">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="a96fa-456">DBPROP_IRowsestLocate</span><span class="sxs-lookup"><span data-stu-id="a96fa-456">DBPROP_IRowsestLocate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-457">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="a96fa-457">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-458">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="a96fa-458">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="a96fa-459">DBPROP_IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="a96fa-459">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-460">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="a96fa-460">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="a96fa-461">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="a96fa-461">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-462">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="a96fa-462">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="a96fa-463">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="a96fa-463">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-464">IStorage</span><span class="sxs-lookup"><span data-stu-id="a96fa-464">IStorage</span></span></p></td>
<td><p><span data-ttu-id="a96fa-465">DBPROP_IStorage</span><span class="sxs-lookup"><span data-stu-id="a96fa-465">DBPROP_IStorage</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-466">IStream</span><span class="sxs-lookup"><span data-stu-id="a96fa-466">IStream</span></span></p></td>
<td><p><span data-ttu-id="a96fa-467">DBPROP_IStream</span><span class="sxs-lookup"><span data-stu-id="a96fa-467">DBPROP_IStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-468">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="a96fa-468">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="a96fa-469">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="a96fa-469">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-470">Литерал закладки</span><span class="sxs-lookup"><span data-stu-id="a96fa-470">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="a96fa-471">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="a96fa-471">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-472">Удостоверение литерала строки</span><span class="sxs-lookup"><span data-stu-id="a96fa-472">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="a96fa-473">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="a96fa-473">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-474">Максимальное число открытых строк</span><span class="sxs-lookup"><span data-stu-id="a96fa-474">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="a96fa-475">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="a96fa-475">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-476">Максимум ожидающие строк</span><span class="sxs-lookup"><span data-stu-id="a96fa-476">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="a96fa-477">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="a96fa-477">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-478">Максимальное число строк</span><span class="sxs-lookup"><span data-stu-id="a96fa-478">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="a96fa-479">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="a96fa-479">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-480">Использование памяти</span><span class="sxs-lookup"><span data-stu-id="a96fa-480">Memory Usage</span></span></p></td>
<td><p><span data-ttu-id="a96fa-481">ОПРЕДЕЛЕН</span><span class="sxs-lookup"><span data-stu-id="a96fa-481">DBPROP_MEMORYUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-482">Степень детализации уведомлений</span><span class="sxs-lookup"><span data-stu-id="a96fa-482">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="a96fa-483">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="a96fa-483">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-484">Этапы уведомлений</span><span class="sxs-lookup"><span data-stu-id="a96fa-484">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="a96fa-485">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="a96fa-485">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-486">Объекты в транзакции</span><span class="sxs-lookup"><span data-stu-id="a96fa-486">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="a96fa-487">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="a96fa-487">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-488">Видны прочие изменения</span><span class="sxs-lookup"><span data-stu-id="a96fa-488">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="a96fa-489">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="a96fa-489">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-490">Других пользователей вставки видимым</span><span class="sxs-lookup"><span data-stu-id="a96fa-490">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="a96fa-491">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="a96fa-491">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-492">Видны собственные изменения</span><span class="sxs-lookup"><span data-stu-id="a96fa-492">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="a96fa-493">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="a96fa-493">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-494">Видны собственные операции вставки</span><span class="sxs-lookup"><span data-stu-id="a96fa-494">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="a96fa-495">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="a96fa-495">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-496">Сохранять при аварийном завершении</span><span class="sxs-lookup"><span data-stu-id="a96fa-496">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="a96fa-497">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="a96fa-497">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-498">Сохранять при фиксации</span><span class="sxs-lookup"><span data-stu-id="a96fa-498">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="a96fa-499">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="a96fa-499">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-500">Быстрый перезапуск</span><span class="sxs-lookup"><span data-stu-id="a96fa-500">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="a96fa-501">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="a96fa-501">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-502">Повторные события</span><span class="sxs-lookup"><span data-stu-id="a96fa-502">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="a96fa-503">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="a96fa-503">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-504">Удаление удаленных строк</span><span class="sxs-lookup"><span data-stu-id="a96fa-504">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="a96fa-505">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="a96fa-505">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-506">Сообщить о нескольких изменений</span><span class="sxs-lookup"><span data-stu-id="a96fa-506">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="a96fa-507">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="a96fa-507">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-508">Вернуть ожидающие вставки</span><span class="sxs-lookup"><span data-stu-id="a96fa-508">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="a96fa-509">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="a96fa-509">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-510">Удалить строку уведомлений</span><span class="sxs-lookup"><span data-stu-id="a96fa-510">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="a96fa-511">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="a96fa-511">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-512">Строка первого уведомления об изменении</span><span class="sxs-lookup"><span data-stu-id="a96fa-512">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="a96fa-513">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="a96fa-513">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-514">Строка вставки уведомлений</span><span class="sxs-lookup"><span data-stu-id="a96fa-514">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="a96fa-515">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="a96fa-515">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-516">Привилегии строки</span><span class="sxs-lookup"><span data-stu-id="a96fa-516">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="a96fa-517">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="a96fa-517">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-518">Уведомления о повторной синхронизации строки</span><span class="sxs-lookup"><span data-stu-id="a96fa-518">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="a96fa-519">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="a96fa-519">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-520">Строка, потоковой модели</span><span class="sxs-lookup"><span data-stu-id="a96fa-520">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="a96fa-521">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="a96fa-521">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-522">Уведомление об изменении отмены строки</span><span class="sxs-lookup"><span data-stu-id="a96fa-522">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="a96fa-523">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="a96fa-523">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-524">Строка отмены Delete уведомлений</span><span class="sxs-lookup"><span data-stu-id="a96fa-524">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="a96fa-525">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="a96fa-525">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-526">Вставка отмены строки уведомлений</span><span class="sxs-lookup"><span data-stu-id="a96fa-526">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="a96fa-527">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="a96fa-527">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-528">Уведомление об обновлении строки</span><span class="sxs-lookup"><span data-stu-id="a96fa-528">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="a96fa-529">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="a96fa-529">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-530">Уведомление об изменении положения строк выборки</span><span class="sxs-lookup"><span data-stu-id="a96fa-530">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="a96fa-531">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="a96fa-531">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-532">Уведомление о выпуске набора строк</span><span class="sxs-lookup"><span data-stu-id="a96fa-532">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="a96fa-533">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="a96fa-533">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-534">Прокрутка назад</span><span class="sxs-lookup"><span data-stu-id="a96fa-534">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="a96fa-535">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="a96fa-535">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-536">Пропустить удаленных закладки</span><span class="sxs-lookup"><span data-stu-id="a96fa-536">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="a96fa-537">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="a96fa-537">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-538">Строка строгого удостоверений</span><span class="sxs-lookup"><span data-stu-id="a96fa-538">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="a96fa-539">DBPROP_STRONGITDENTITY</span><span class="sxs-lookup"><span data-stu-id="a96fa-539">DBPROP_STRONGITDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-540">Возможности обновления</span><span class="sxs-lookup"><span data-stu-id="a96fa-540">Updatability</span></span></p></td>
<td><p><span data-ttu-id="a96fa-541">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="a96fa-541">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-542">Использование закладок</span><span class="sxs-lookup"><span data-stu-id="a96fa-542">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="a96fa-543">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="a96fa-543">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a><span data-ttu-id="a96fa-544">Динамические свойства команды</span><span class="sxs-lookup"><span data-stu-id="a96fa-544">Command Dynamic Properties</span></span>

<span data-ttu-id="a96fa-545">Следующие свойства добавляются в коллекцию **свойств** объекта **команды** .</span><span class="sxs-lookup"><span data-stu-id="a96fa-545">The following properties are added to the **Command** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a96fa-546">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="a96fa-546">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="a96fa-547">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="a96fa-547">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-548">Порядок доступа</span><span class="sxs-lookup"><span data-stu-id="a96fa-548">Access Order</span></span></p></td>
<td><p><span data-ttu-id="a96fa-549">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="a96fa-549">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-550">Только для добавления строк</span><span class="sxs-lookup"><span data-stu-id="a96fa-550">Append-Only Rowset</span></span></p></td>
<td><p><span data-ttu-id="a96fa-551">DBPROP_APPENDONLY</span><span class="sxs-lookup"><span data-stu-id="a96fa-551">DBPROP_APPENDONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-552">Блокировка объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="a96fa-552">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="a96fa-553">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="a96fa-553">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-554">Тип закладки</span><span class="sxs-lookup"><span data-stu-id="a96fa-554">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="a96fa-555">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="a96fa-555">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-556">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="a96fa-556">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="a96fa-557">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="a96fa-557">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-558">Изменение вставленных строк</span><span class="sxs-lookup"><span data-stu-id="a96fa-558">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="a96fa-559">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="a96fa-559">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-560">Права доступа столбца</span><span class="sxs-lookup"><span data-stu-id="a96fa-560">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="a96fa-561">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="a96fa-561">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-562">Столбец набор уведомлений</span><span class="sxs-lookup"><span data-stu-id="a96fa-562">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="a96fa-563">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="a96fa-563">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-564">Отложите столбца</span><span class="sxs-lookup"><span data-stu-id="a96fa-564">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="a96fa-565">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="a96fa-565">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-566">Отложенное обновление объекта хранения</span><span class="sxs-lookup"><span data-stu-id="a96fa-566">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="a96fa-567">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="a96fa-567">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-568">Выборку</span><span class="sxs-lookup"><span data-stu-id="a96fa-568">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="a96fa-569">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="a96fa-569">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-570">Хранение строк</span><span class="sxs-lookup"><span data-stu-id="a96fa-570">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="a96fa-571">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="a96fa-571">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-572">IAccessor</span><span class="sxs-lookup"><span data-stu-id="a96fa-572">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="a96fa-573">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="a96fa-573">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-574">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="a96fa-574">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="a96fa-575">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="a96fa-575">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-576">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="a96fa-576">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="a96fa-577">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="a96fa-577">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-578">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="a96fa-578">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="a96fa-579">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="a96fa-579">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-580">IConvertType</span><span class="sxs-lookup"><span data-stu-id="a96fa-580">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="a96fa-581">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="a96fa-581">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-582">ILockBytes</span><span class="sxs-lookup"><span data-stu-id="a96fa-582">ILockBytes</span></span></p></td>
<td><p><span data-ttu-id="a96fa-583">DBPROP_ILockBytes</span><span class="sxs-lookup"><span data-stu-id="a96fa-583">DBPROP_ILockBytes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-584">Немобильные строки</span><span class="sxs-lookup"><span data-stu-id="a96fa-584">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="a96fa-585">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="a96fa-585">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-586">IRowset</span><span class="sxs-lookup"><span data-stu-id="a96fa-586">IRowset</span></span></p></td>
<td><p><span data-ttu-id="a96fa-587">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="a96fa-587">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-588">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="a96fa-588">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="a96fa-589">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="a96fa-589">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-590">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="a96fa-590">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="a96fa-591">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="a96fa-591">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-592">IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="a96fa-592">IRowsetIndex</span></span></p></td>
<td><p><span data-ttu-id="a96fa-593">DBPROP_IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="a96fa-593">DBPROP_IRowsetIndex</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-594">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="a96fa-594">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="a96fa-595">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="a96fa-595">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-596">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="a96fa-596">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="a96fa-597">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="a96fa-597">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-598">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="a96fa-598">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-599">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="a96fa-599">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="a96fa-600">DBPROP_IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="a96fa-600">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-601">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="a96fa-601">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="a96fa-602">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="a96fa-602">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-603">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="a96fa-603">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="a96fa-604">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="a96fa-604">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-605">IStorage</span><span class="sxs-lookup"><span data-stu-id="a96fa-605">IStorage</span></span></p></td>
<td><p><span data-ttu-id="a96fa-606">DBPROP_IStorage</span><span class="sxs-lookup"><span data-stu-id="a96fa-606">DBPROP_IStorage</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-607">IStream</span><span class="sxs-lookup"><span data-stu-id="a96fa-607">IStream</span></span></p></td>
<td><p><span data-ttu-id="a96fa-608">DBPROP_IStream</span><span class="sxs-lookup"><span data-stu-id="a96fa-608">DBPROP_IStream</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-609">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="a96fa-609">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="a96fa-610">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="a96fa-610">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-611">Литерал закладки</span><span class="sxs-lookup"><span data-stu-id="a96fa-611">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="a96fa-612">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="a96fa-612">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-613">Удостоверение литерала строки</span><span class="sxs-lookup"><span data-stu-id="a96fa-613">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="a96fa-614">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="a96fa-614">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-615">Режим блокировки</span><span class="sxs-lookup"><span data-stu-id="a96fa-615">Lock Mode</span></span></p></td>
<td><p><span data-ttu-id="a96fa-616">DBPROP_LOCKMODE</span><span class="sxs-lookup"><span data-stu-id="a96fa-616">DBPROP_LOCKMODE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-617">Максимальное число открытых строк</span><span class="sxs-lookup"><span data-stu-id="a96fa-617">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="a96fa-618">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="a96fa-618">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-619">Максимум ожидающие строк</span><span class="sxs-lookup"><span data-stu-id="a96fa-619">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="a96fa-620">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="a96fa-620">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-621">Максимальное число строк</span><span class="sxs-lookup"><span data-stu-id="a96fa-621">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="a96fa-622">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="a96fa-622">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-623">Степень детализации уведомлений</span><span class="sxs-lookup"><span data-stu-id="a96fa-623">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="a96fa-624">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="a96fa-624">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-625">Этапы уведомлений</span><span class="sxs-lookup"><span data-stu-id="a96fa-625">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="a96fa-626">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="a96fa-626">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-627">Объекты в транзакции</span><span class="sxs-lookup"><span data-stu-id="a96fa-627">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="a96fa-628">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="a96fa-628">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-629">Видны прочие изменения</span><span class="sxs-lookup"><span data-stu-id="a96fa-629">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="a96fa-630">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="a96fa-630">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-631">Других пользователей вставки видимым</span><span class="sxs-lookup"><span data-stu-id="a96fa-631">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="a96fa-632">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="a96fa-632">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-633">Видны собственные изменения</span><span class="sxs-lookup"><span data-stu-id="a96fa-633">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="a96fa-634">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="a96fa-634">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-635">Видны собственные операции вставки</span><span class="sxs-lookup"><span data-stu-id="a96fa-635">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="a96fa-636">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="a96fa-636">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-637">Сохранять при аварийном завершении</span><span class="sxs-lookup"><span data-stu-id="a96fa-637">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="a96fa-638">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="a96fa-638">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-639">Сохранять при фиксации</span><span class="sxs-lookup"><span data-stu-id="a96fa-639">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="a96fa-640">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="a96fa-640">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-641">Быстрый перезапуск</span><span class="sxs-lookup"><span data-stu-id="a96fa-641">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="a96fa-642">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="a96fa-642">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-643">Повторные события</span><span class="sxs-lookup"><span data-stu-id="a96fa-643">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="a96fa-644">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="a96fa-644">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-645">Удаление удаленных строк</span><span class="sxs-lookup"><span data-stu-id="a96fa-645">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="a96fa-646">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="a96fa-646">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-647">Сообщить о нескольких изменений</span><span class="sxs-lookup"><span data-stu-id="a96fa-647">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="a96fa-648">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="a96fa-648">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-649">Вернуть ожидающие вставки</span><span class="sxs-lookup"><span data-stu-id="a96fa-649">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="a96fa-650">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="a96fa-650">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-651">Удалить строку уведомлений</span><span class="sxs-lookup"><span data-stu-id="a96fa-651">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="a96fa-652">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="a96fa-652">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-653">Строка первого уведомления об изменении</span><span class="sxs-lookup"><span data-stu-id="a96fa-653">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="a96fa-654">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="a96fa-654">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-655">Строка вставки уведомлений</span><span class="sxs-lookup"><span data-stu-id="a96fa-655">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="a96fa-656">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="a96fa-656">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-657">Привилегии строки</span><span class="sxs-lookup"><span data-stu-id="a96fa-657">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="a96fa-658">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="a96fa-658">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-659">Уведомления о повторной синхронизации строки</span><span class="sxs-lookup"><span data-stu-id="a96fa-659">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="a96fa-660">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="a96fa-660">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-661">Строка, потоковой модели</span><span class="sxs-lookup"><span data-stu-id="a96fa-661">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="a96fa-662">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="a96fa-662">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-663">Уведомление об изменении отмены строки</span><span class="sxs-lookup"><span data-stu-id="a96fa-663">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="a96fa-664">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="a96fa-664">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-665">Строка отмены Delete уведомлений</span><span class="sxs-lookup"><span data-stu-id="a96fa-665">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="a96fa-666">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="a96fa-666">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-667">Вставка отмены строки уведомлений</span><span class="sxs-lookup"><span data-stu-id="a96fa-667">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="a96fa-668">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="a96fa-668">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-669">Уведомление об обновлении строки</span><span class="sxs-lookup"><span data-stu-id="a96fa-669">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="a96fa-670">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="a96fa-670">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-671">Уведомление об изменении положения строк выборки</span><span class="sxs-lookup"><span data-stu-id="a96fa-671">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="a96fa-672">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="a96fa-672">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-673">Уведомление о выпуске набора строк</span><span class="sxs-lookup"><span data-stu-id="a96fa-673">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="a96fa-674">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="a96fa-674">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-675">Прокрутка назад</span><span class="sxs-lookup"><span data-stu-id="a96fa-675">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="a96fa-676">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="a96fa-676">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-677">Вставка данных сервера</span><span class="sxs-lookup"><span data-stu-id="a96fa-677">Server Data on Insert</span></span></p></td>
<td><p><span data-ttu-id="a96fa-678">DBPROP_SERVERDATAONINSERT</span><span class="sxs-lookup"><span data-stu-id="a96fa-678">DBPROP_SERVERDATAONINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-679">Пропустить удаленных закладки</span><span class="sxs-lookup"><span data-stu-id="a96fa-679">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="a96fa-680">DBPROP_BOOKMARKSKIP</span><span class="sxs-lookup"><span data-stu-id="a96fa-680">DBPROP_BOOKMARKSKIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-681">Строка строгого удостоверений</span><span class="sxs-lookup"><span data-stu-id="a96fa-681">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="a96fa-682">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="a96fa-682">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96fa-683">Возможности обновления</span><span class="sxs-lookup"><span data-stu-id="a96fa-683">Updatability</span></span></p></td>
<td><p><span data-ttu-id="a96fa-684">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="a96fa-684">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96fa-685">Использование закладок</span><span class="sxs-lookup"><span data-stu-id="a96fa-685">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="a96fa-686">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="a96fa-686">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="a96fa-687">См. также</span><span class="sxs-lookup"><span data-stu-id="a96fa-687">See also</span></span>

<span data-ttu-id="a96fa-688">Сведения о реализации и функциональным сведения о поставщика OLE DB для Microsoft Jet обратитесь к поставщика OLE DB для Microsoft Jet документации в пакете SDK MDAC.</span><span class="sxs-lookup"><span data-stu-id="a96fa-688">For specific implementation details and functional information about the OLE DB Provider for Microsoft Jet, consult the OLE DB Provider for Microsoft Jet documentation in the MDAC SDK.</span></span>

