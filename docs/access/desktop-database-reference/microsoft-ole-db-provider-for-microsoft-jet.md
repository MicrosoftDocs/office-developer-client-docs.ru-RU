---
title: Microsoft OLE DB Provider for Microsoft Jet
TOCTitle: Microsoft OLE DB Provider for Microsoft Jet
ms:assetid: 4a210d72-8c90-aa7c-4621-1a555a30a2d2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249228(v=office.15)
ms:contentKeyID: 48544660
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bd56f018a9eb8da4078848d7890e4543279a7362
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480332"
---
# <a name="microsoft-ole-db-provider-for-microsoft-jet"></a><span data-ttu-id="5dc3e-102">Microsoft OLE DB Provider for Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="5dc3e-102">Microsoft OLE DB Provider for Microsoft Jet</span></span>

<span data-ttu-id="5dc3e-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5dc3e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5dc3e-104">Поставщик OLE DB для Microsoft Jet позволяет ADO для доступа к базам данных Microsoft Jet.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-104">The OLE DB Provider for Microsoft Jet allows ADO to access Microsoft Jet databases.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="5dc3e-105">Параметры строки подключения</span><span class="sxs-lookup"><span data-stu-id="5dc3e-105">Connection String Parameters</span></span>

<span data-ttu-id="5dc3e-106">Для подключения к данным поставщиком, задайте для свойства [ConnectionString](connectionstring-property-ado.md) для аргумента *поставщика* :</span><span class="sxs-lookup"><span data-stu-id="5dc3e-106">To connect to this provider, set the *Provider* argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```vb 
 
Microsoft.Jet.OLEDB.4.0 
```

<span data-ttu-id="5dc3e-107">Чтение свойства [поставщика](provider-property-ado.md) будет возвращать также этой строки.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-107">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="5dc3e-108">Типичная строка подключения</span><span class="sxs-lookup"><span data-stu-id="5dc3e-108">Typical Connection String</span></span>

<span data-ttu-id="5dc3e-109">— Это строка соединения для данного поставщика:</span><span class="sxs-lookup"><span data-stu-id="5dc3e-109">A typical connection string for this provider is:</span></span>

```vb 
 
"Provider=Microsoft.Jet.OLEDB.4.0;Data Source=databaseName;User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="5dc3e-110">Строка состоит из следующих ключевых слов:</span><span class="sxs-lookup"><span data-stu-id="5dc3e-110">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5dc3e-111">Keyword</span><span class="sxs-lookup"><span data-stu-id="5dc3e-111">Keyword</span></span></p></th>
<th><p><span data-ttu-id="5dc3e-112">Описание</span><span class="sxs-lookup"><span data-stu-id="5dc3e-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-113"><strong>Поставщик</strong></span><span class="sxs-lookup"><span data-stu-id="5dc3e-113"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="5dc3e-114">Задает поставщика OLE DB для Microsoft Jet.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-114">Specifies the OLE DB Provider for Microsoft Jet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-115"><strong>Источник данных</strong></span><span class="sxs-lookup"><span data-stu-id="5dc3e-115"><strong>Data Source</strong></span></span></p></td>
<td><p><span data-ttu-id="5dc3e-116">Указывает базу данных путь и имя файла (например, c:\Northwind.mdb).</span><span class="sxs-lookup"><span data-stu-id="5dc3e-116">Specifies the database path and file name (for example, c:\Northwind.mdb).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-117"><strong>Идентификатор пользователя</strong></span><span class="sxs-lookup"><span data-stu-id="5dc3e-117"><strong>User ID</strong></span></span></p></td>
<td><p><span data-ttu-id="5dc3e-118">Задает имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-118">Specifies the user name.</span></span> <span data-ttu-id="5dc3e-119">Если это ключевое слово не указан, строка, &quot;администратора&quot;, используемый по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-119">If this keyword is not specified, the string, &quot;admin&quot;, is used by default.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-120"><strong>Password</strong></span><span class="sxs-lookup"><span data-stu-id="5dc3e-120"><strong>Password</strong></span></span></p></td>
<td><p><span data-ttu-id="5dc3e-121">Задает пароль пользователя.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-121">Specifies the user password.</span></span> <span data-ttu-id="5dc3e-122">Если это ключевое слово не указан, пустая строка (&quot;&quot;), используемый по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-122">If this keyword is not specified, the empty string (&quot;&quot;), is used by default.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-connection-parameters"></a><span data-ttu-id="5dc3e-123">Параметры подключения от поставщика</span><span class="sxs-lookup"><span data-stu-id="5dc3e-123">Provider-Specific Connection Parameters</span></span>

<span data-ttu-id="5dc3e-124">Поставщик OLE DB для Microsoft Jet поддерживает несколько динамические свойства от поставщика дополнение к тем определяется ADO.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-124">The OLE DB Provider for Microsoft Jet supports several provider-specific dynamic properties in addition to those defined by ADO.</span></span> <span data-ttu-id="5dc3e-125">Как вместе с другими параметрами **подключения** могут устанавливаться с помощью **Свойства** коллекции объект **подключения** или в качестве части строки подключения.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-125">As with all other **Connection** parameters, they can be set via the **Connection** object's **Properties** collection or as part of the connection string.</span></span>

<span data-ttu-id="5dc3e-126">В следующей таблице перечислены эти свойства имя соответствующего свойства OLE DB в скобки.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-126">The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5dc3e-127">Параметр</span><span class="sxs-lookup"><span data-stu-id="5dc3e-127">Parameter</span></span></p></th>
<th><p><span data-ttu-id="5dc3e-128">Описание</span><span class="sxs-lookup"><span data-stu-id="5dc3e-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-129">Освобожденное место сумма Jet OLEDB:Compact</span><span class="sxs-lookup"><span data-stu-id="5dc3e-129">Jet OLEDB:Compact Reclaimed Space Amount</span></span><br />
<span data-ttu-id="5dc3e-130">(DBPROP_JETOLEDB_COMPACTFREESPACESIZE)</span><span class="sxs-lookup"><span data-stu-id="5dc3e-130">(DBPROP_JETOLEDB_COMPACTFREESPACESIZE)</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-131">Указывает оценку дискового пространства, в байтах, который может быть восстановлена путем сжатие базы данных.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-131">Indicates an estimate of the amount of space, in bytes, that can be reclaimed by compacting the database.</span></span> <span data-ttu-id="5dc3e-132">Это значение допустимо только после установления подключения к базе данных.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-132">This value is only valid after a database connection has been established.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-133">Элемент управления OLEDB:Connection Jet</span><span class="sxs-lookup"><span data-stu-id="5dc3e-133">Jet OLEDB:Connection Control</span></span><br />
<span data-ttu-id="5dc3e-134">(DBPROP_JETOLEDB_CONNECTIONCONTROL)</span><span class="sxs-lookup"><span data-stu-id="5dc3e-134">(DBPROP_JETOLEDB_CONNECTIONCONTROL)</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-135">Указывает, будет ли пользователи могут подключаться к базе данных.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-135">Indicates whether users can connect to the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-136">Jet OLEDB: создание Системная база данных</span><span class="sxs-lookup"><span data-stu-id="5dc3e-136">Jet OLEDB:Create System Database</span></span><br />
<span data-ttu-id="5dc3e-137">(DBPROP_JETOLEDB_CREATESYSTEMDATABASE)</span><span class="sxs-lookup"><span data-stu-id="5dc3e-137">(DBPROP_JETOLEDB_CREATESYSTEMDATABASE)</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-138">Указывает, следует ли создавать Системная база данных при создании нового источника данных.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-138">Indicates whether a system database should be created when creating a new data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-139">Режим блокировки OLEDB:Database Jet</span><span class="sxs-lookup"><span data-stu-id="5dc3e-139">Jet OLEDB:Database Locking Mode</span></span><br />
<span data-ttu-id="5dc3e-140">(DBPROP_JETOLEDB_DATABASELOCKMODE)</span><span class="sxs-lookup"><span data-stu-id="5dc3e-140">(DBPROP_JETOLEDB_DATABASELOCKMODE)</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-141">Указывает режим блокировки для этой базы данных.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-141">Indicates the locking mode for this database.</span></span> <span data-ttu-id="5dc3e-142">Первый пользователю открывать базу данных определяет режим, используемый при открытом базы данных.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-142">The first user to open the database determines the mode used while the database is open.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-143">Пароль OLEDB:Database Jet</span><span class="sxs-lookup"><span data-stu-id="5dc3e-143">Jet OLEDB:Database Password</span></span><br />
<span data-ttu-id="5dc3e-144">(DBPROP_JETOLEDB_DATABASEPASSWORD)</span><span class="sxs-lookup"><span data-stu-id="5dc3e-144">(DBPROP_JETOLEDB_DATABASEPASSWORD)</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-145">Указывает пароль базы данных.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-145">Indicates the database password.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-146">Jet OLEDB: не копировать языковой стандарт на компакт</span><span class="sxs-lookup"><span data-stu-id="5dc3e-146">Jet OLEDB:Don't Copy Locale on Compact</span></span><br />
<span data-ttu-id="5dc3e-147">(DBPROP_JETOLEDB_COMPACT_DONTCOPYLOCALE)</span><span class="sxs-lookup"><span data-stu-id="5dc3e-147">(DBPROP_JETOLEDB_COMPACT_DONTCOPYLOCALE)</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-148">Указывает, следует ли Jet скопировать сведения о языковом стандарте при сжатии базы данных.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-148">Indicates whether Jet should copy locale information when compacting a database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-149">Jet OLEDB: шифрование базы данных</span><span class="sxs-lookup"><span data-stu-id="5dc3e-149">Jet OLEDB:Encrypt Database</span></span><br />
<span data-ttu-id="5dc3e-150">(DBPROP_JETOLEDB_ENCRYPTDATABASE)</span><span class="sxs-lookup"><span data-stu-id="5dc3e-150">(DBPROP_JETOLEDB_ENCRYPTDATABASE)</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-151">Указывает, должен быть зашифрован сжатии баз данных.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-151">Indicates whether a compacted database should be encrypted.</span></span> <span data-ttu-id="5dc3e-152">Если это свойство не задано, сжатии базы данных будет шифроваться, если также зашифрованные исходной базы данных.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-152">If this property is not set, the compacted database will be encrypted if the original database was also encrypted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-153">Тип OLEDB:Engine Jet</span><span class="sxs-lookup"><span data-stu-id="5dc3e-153">Jet OLEDB:Engine Type</span></span><br />
<span data-ttu-id="5dc3e-154">(DBPROP_JETOLEDB_ENGINE)</span><span class="sxs-lookup"><span data-stu-id="5dc3e-154">(DBPROP_JETOLEDB_ENGINE)</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-155">Указывает, подсистема хранилища для доступа к текущей хранилищу данных.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-155">Indicates the storage engine used to access the current data store.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-156">Асинхронная задержка Jet OLEDB:Exclusive</span><span class="sxs-lookup"><span data-stu-id="5dc3e-156">Jet OLEDB:Exclusive Async Delay</span></span><br />
<span data-ttu-id="5dc3e-157">(DBPROP_JETOLEDB_EXCLUSIVEASYNCDELAY)</span><span class="sxs-lookup"><span data-stu-id="5dc3e-157">(DBPROP_JETOLEDB_EXCLUSIVEASYNCDELAY)</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-158">Указывает максимальную длину время в миллисекундах, которые Jet может отложить асинхронных операций записи на диск при открытии исключительно базы данных.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-158">Indicates the maximum length of time, in milliseconds, that Jet can delay asynchronous writes to disk when the database is opened exclusively.</span></span> <span data-ttu-id="5dc3e-159">Это свойство игнорируется, если <strong>Время ожидания транзакций OLEDB:Flush Jet</strong> не задано значение 0.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-159">This property is ignored unless <strong>Jet OLEDB:Flush Transaction Timeout</strong> is set to 0.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-160">Время ожидания транзакций OLEDB:Flush Jet</span><span class="sxs-lookup"><span data-stu-id="5dc3e-160">Jet OLEDB:Flush Transaction Timeout</span></span><br />
<span data-ttu-id="5dc3e-161">(DBPROP_JETOLEDB_FLUSHTRANSACTIONTIMEOUT)</span><span class="sxs-lookup"><span data-stu-id="5dc3e-161">(DBPROP_JETOLEDB_FLUSHTRANSACTIONTIMEOUT)</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-162">Указывает время ожидания до фактически записи данных, сохраненных в кэше для асинхронной записи на диск.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-162">Indicates the amount of time to wait before data stored in a cache for asynchronous writing is actually written to disk.</span></span> <span data-ttu-id="5dc3e-163">Этот параметр переопределяет значения для <strong>Jet OLEDB: общих асинхронная задержка</strong> и <strong>Jet OLEDB:Exclusive асинхронная задержка</strong>.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-163">This setting overrides the values for <strong>Jet OLEDB:Shared Async Delay</strong> and <strong>Jet OLEDB:Exclusive Async Delay</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-164">Jet OLEDB: глобальные массовых операций</span><span class="sxs-lookup"><span data-stu-id="5dc3e-164">Jet OLEDB:Global Bulk Transactions</span></span><br />
<span data-ttu-id="5dc3e-165">(DBPROP_JETOLEDB_GLOBALBULKNOTRANSACTIONS)</span><span class="sxs-lookup"><span data-stu-id="5dc3e-165">(DBPROP_JETOLEDB_GLOBALBULKNOTRANSACTIONS)</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-166">Указывает, будет ли в рамках транзакции SQL массовых операций.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-166">Indicates whether SQL bulk transactions are transacted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-167">Jet OLEDB: глобальные частичное массового операций</span><span class="sxs-lookup"><span data-stu-id="5dc3e-167">Jet OLEDB:Global Partial Bulk Ops</span></span><br />
<span data-ttu-id="5dc3e-168">(DBPROP_JETOLEDB_GLOBALBULKPARTIAL)</span><span class="sxs-lookup"><span data-stu-id="5dc3e-168">(DBPROP_JETOLEDB_GLOBALBULKPARTIAL)</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-169">Указывает пароль, используемый для открытия базы данных.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-169">Indicates the password used to open the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-170">Jet OLEDB: неявных зафиксировать синхронизации</span><span class="sxs-lookup"><span data-stu-id="5dc3e-170">Jet OLEDB:Implicit Commit Sync</span></span><br />
<span data-ttu-id="5dc3e-171">(DBPROP_JETOLEDB_IMPLICITCOMMITSYNC)</span><span class="sxs-lookup"><span data-stu-id="5dc3e-171">(DBPROP_JETOLEDB_IMPLICITCOMMITSYNC)</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-172">Указывает, записываются ли изменения, внесенные в внутренних неявных транзакций в режиме синхронными и асинхронными.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-172">Indicates whether changes made in internal implicit transactions are written in synchronous or asynchronous mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-173">Задержка OLEDB:Lock Jet</span><span class="sxs-lookup"><span data-stu-id="5dc3e-173">Jet OLEDB:Lock Delay</span></span><br />
<span data-ttu-id="5dc3e-174">(DBPROP_JETOLEDB_LOCKDELAY)</span><span class="sxs-lookup"><span data-stu-id="5dc3e-174">(DBPROP_JETOLEDB_LOCKDELAY)</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-175">Указывает время в миллисекундах ожидания запроса блокировки после Предыдущая попытка не удалось выполнить.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-175">Indicates the number of milliseconds to wait before attempting to acquire a lock after a previous attempt has failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-176">Повтор OLEDB:Lock Jet</span><span class="sxs-lookup"><span data-stu-id="5dc3e-176">Jet OLEDB:Lock Retry</span></span><br />
<span data-ttu-id="5dc3e-177">(DBPROP_JETOLEDB_LOCKRETRY)</span><span class="sxs-lookup"><span data-stu-id="5dc3e-177">(DBPROP_JETOLEDB_LOCKRETRY)</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-178">Указывает, сколько раз при попытке доступа к заблокированной странице повторяется.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-178">Indicates how many times an attempt to access a locked page is repeated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-179">Размер буфера OLEDB:Max Jet</span><span class="sxs-lookup"><span data-stu-id="5dc3e-179">Jet OLEDB:Max Buffer Size</span></span><br />
<span data-ttu-id="5dc3e-180">(DBPROP_JETOLEDB_MAXBUFFERSIZE)</span><span class="sxs-lookup"><span data-stu-id="5dc3e-180">(DBPROP_JETOLEDB_MAXBUFFERSIZE)</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-181">Указывает максимальный объем памяти, в килобайтах Jet может использовать до начала записи изменений на диск.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-181">Indicates the maximum amount of memory, in kilobytes, Jet can use before it starts flushing changes to disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-182">Jet OLEDB:Max блокировок в файл</span><span class="sxs-lookup"><span data-stu-id="5dc3e-182">Jet OLEDB:Max Locks Per File</span></span><br />
<span data-ttu-id="5dc3e-183">(DBPROP_JETOLEDB_MAXLOCKSPERFILE)</span><span class="sxs-lookup"><span data-stu-id="5dc3e-183">(DBPROP_JETOLEDB_MAXLOCKSPERFILE)</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-184">Указывает максимальное количество блокировок, которые Jet можно поместить в базе данных.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-184">Indicates the maximum number of locks Jet can place on a database.</span></span> <span data-ttu-id="5dc3e-185">Значение по умолчанию — 9500.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-185">The default value is 9500.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-186">Jet OLEDB: новый пароль базы данных</span><span class="sxs-lookup"><span data-stu-id="5dc3e-186">Jet OLEDB:New Database Password</span></span><br />
<span data-ttu-id="5dc3e-187">(DBPROP_JETOLEDB_NEWDATABASEPASSWORD)</span><span class="sxs-lookup"><span data-stu-id="5dc3e-187">(DBPROP_JETOLEDB_NEWDATABASEPASSWORD)</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-188">Указывает новый пароль для этой базы данных.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-188">Indicates the new password to be set for this database.</span></span> <span data-ttu-id="5dc3e-189">Старый пароль хранится в <strong>Jet OLEDB:Database пароль</strong>.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-189">The old password is stored in <strong>Jet OLEDB:Database Password</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-190">Время ожидания команды OLEDB:ODBC Jet</span><span class="sxs-lookup"><span data-stu-id="5dc3e-190">Jet OLEDB:ODBC Command Time Out</span></span><br />
<span data-ttu-id="5dc3e-191">(DBPROP_JETOLEDB_ODBCCOMMANDTIMEOUT)</span><span class="sxs-lookup"><span data-stu-id="5dc3e-191">(DBPROP_JETOLEDB_ODBCCOMMANDTIMEOUT)</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-192">Указывает, что количество миллисекунд до удаленный запрос ODBC с Jet будет времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-192">Indicates the number of milliseconds before a remote ODBC query from Jet will timeout.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-193">Блокировки OLEDB:Page Jet для блокировки таблицы</span><span class="sxs-lookup"><span data-stu-id="5dc3e-193">Jet OLEDB:Page Locks to Table Lock</span></span><br />
<span data-ttu-id="5dc3e-194">(DBPROP_JETOLEDB_PAGELOCKSTOTABLELOCK)</span><span class="sxs-lookup"><span data-stu-id="5dc3e-194">(DBPROP_JETOLEDB_PAGELOCKSTOTABLELOCK)</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-195">Указывает, сколько страниц необходимо будут удалены в транзакции, прежде чем повышение уровня блокировки для блокировки таблицы.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-195">Indicates how many pages need to be locked within a transaction before Jet attempts to promote the lock to a table lock.</span></span> <span data-ttu-id="5dc3e-196">Если это значение равно 0, блокировки никогда не повышается.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-196">If this value is 0, then the lock is never promoted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-197">Время ожидания OLEDB:Page Jet</span><span class="sxs-lookup"><span data-stu-id="5dc3e-197">Jet OLEDB:Page Timeout</span></span><br />
<span data-ttu-id="5dc3e-198">(DBPROP_JETOLEDB_PAGETIMEOUT)</span><span class="sxs-lookup"><span data-stu-id="5dc3e-198">(DBPROP_JETOLEDB_PAGETIMEOUT)</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-199">Указывает количество миллисекунд ожидания Jet перед проверкой ли кэш устаревший с помощью файла базы данных.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-199">Indicates the number of milliseconds Jet will wait before checking to see if its cache is out of date with the database file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-200">Страницы табличное Long Jet OLEDB:Recycle</span><span class="sxs-lookup"><span data-stu-id="5dc3e-200">Jet OLEDB:Recycle Long-Valued Pages</span></span><br />
<span data-ttu-id="5dc3e-201">(DBPROP_JETOLEDB_RECYCLELONGVALUEPAGES)</span><span class="sxs-lookup"><span data-stu-id="5dc3e-201">(DBPROP_JETOLEDB_RECYCLELONGVALUEPAGES)</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-202">Указывает, следует ли Jet пытаться агрессивное освобождение страниц больших двоичных ОБЪЕКТОВ, когда их освобождения.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-202">Indicates whether Jet should aggressively try to reclaim BLOB pages when they are freed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-203">Путь OLEDB:Registry Jet</span><span class="sxs-lookup"><span data-stu-id="5dc3e-203">Jet OLEDB:Registry Path</span></span><br />
<span data-ttu-id="5dc3e-204">(DBPROP_JETOLEDB_REGPATH)</span><span class="sxs-lookup"><span data-stu-id="5dc3e-204">(DBPROP_JETOLEDB_REGPATH)</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-205">Указывает ключ реестра Windows, который содержит значения для базы данных Jet.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-205">Indicates the Windows registry key that contains values for the Jet database engine.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-206">Статистика ISAM OLEDB:Reset Jet</span><span class="sxs-lookup"><span data-stu-id="5dc3e-206">Jet OLEDB:Reset ISAM Stats</span></span><br />
<span data-ttu-id="5dc3e-207">(DBPROP_JETOLEDB_RESETISAMSTATS)</span><span class="sxs-lookup"><span data-stu-id="5dc3e-207">(DBPROP_JETOLEDB_RESETISAMSTATS)</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-208">Указывает, должно ли схема <strong>набора записей</strong> DBSCHEMA_JETOLEDB_ISAMSTATS сбросить его счетчики производительности после возврата сведений о производительности.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-208">Indicates whether the schema <strong>Recordset</strong> DBSCHEMA_JETOLEDB_ISAMSTATS should reset its performance counters after returning performance information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-209">Jet OLEDB: общих асинхронная задержка</span><span class="sxs-lookup"><span data-stu-id="5dc3e-209">Jet OLEDB:Shared Async Delay</span></span><br />
<span data-ttu-id="5dc3e-210">(DBPROP_JETOLEDB_SHAREDASYNCDELAY)</span><span class="sxs-lookup"><span data-stu-id="5dc3e-210">(DBPROP_JETOLEDB_SHAREDASYNCDELAY)</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-211">Указывает максимальное время в миллисекундах, Jet может отложить асинхронных операций записи на диск при открытии базы данных в режиме нескольких пользователей.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-211">Indicates the maximum amount of time, in milliseconds, Jet can delay asynchronous writes to disk when the database is opened in multi-user mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-212">База данных Microsoft Jet OLEDB: System</span><span class="sxs-lookup"><span data-stu-id="5dc3e-212">Jet OLEDB:System Database</span></span><br />
<span data-ttu-id="5dc3e-213">(DBPROP_JETOLEDB_SYSDBPATH)</span><span class="sxs-lookup"><span data-stu-id="5dc3e-213">(DBPROP_JETOLEDB_SYSDBPATH)</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-214">Указывает путь и имя файла для файла рабочей группы (системная база данных).</span><span class="sxs-lookup"><span data-stu-id="5dc3e-214">Indicates the path and file name for the workgroup information file (system database).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-215">Режим фиксации OLEDB:Transaction Jet</span><span class="sxs-lookup"><span data-stu-id="5dc3e-215">Jet OLEDB:Transaction Commit Mode</span></span><br />
<span data-ttu-id="5dc3e-216">(DBPROP_JETOLEDB_TXNCOMMITMODE)</span><span class="sxs-lookup"><span data-stu-id="5dc3e-216">(DBPROP_JETOLEDB_TXNCOMMITMODE)</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-217">Указывает, является ли Jet записывает данные на диск синхронно или асинхронно при фиксации транзакции.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-217">Indicates whether Jet writes data to disk synchronously or asynchronously when a transaction is committed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-218">Синхронизация зафиксировать OLEDB:User Jet</span><span class="sxs-lookup"><span data-stu-id="5dc3e-218">Jet OLEDB:User Commit Sync</span></span><br />
<span data-ttu-id="5dc3e-219">(DBPROP_JETOLEDB_USERCOMMITSYNC)</span><span class="sxs-lookup"><span data-stu-id="5dc3e-219">(DBPROP_JETOLEDB_USERCOMMITSYNC)</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-220">Указывает, записываются ли изменения, внесенные в транзакции в режиме синхронными и асинхронными.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-220">Indicates whether changes made in transactions are written in synchronous or asynchronous mode.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-recordset-and-command-properties"></a><span data-ttu-id="5dc3e-221">Свойства команды и записей от поставщика</span><span class="sxs-lookup"><span data-stu-id="5dc3e-221">Provider-Specific Recordset and Command Properties</span></span>

<span data-ttu-id="5dc3e-222">Поставщик Jet также поддерживает несколько свойств **набора записей** и **команду** от поставщика.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-222">The Jet provider also supports several provider-specific **Recordset** and **Command** properties.</span></span> <span data-ttu-id="5dc3e-223">Эти свойства доступны и задается с помощью коллекции **свойств** объекта **команду** или **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="5dc3e-223">These properties are accessed and set through the **Properties** collection of the **Recordset** or **Command** object.</span></span> <span data-ttu-id="5dc3e-224">В таблице перечислены имя свойства ADO и OLE DB название в скобки.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-224">The table lists the ADO property name and its corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5dc3e-225">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="5dc3e-225">Property Name</span></span></p></th>
<th><p><span data-ttu-id="5dc3e-226">Описание</span><span class="sxs-lookup"><span data-stu-id="5dc3e-226">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-227">Транзакции OLEDB:Bulk Jet</span><span class="sxs-lookup"><span data-stu-id="5dc3e-227">Jet OLEDB:Bulk Transactions</span></span><br />
<span data-ttu-id="5dc3e-228">(DBPROP_JETOLEDB_BULKNOTRANSACTIONS)</span><span class="sxs-lookup"><span data-stu-id="5dc3e-228">(DBPROP_JETOLEDB_BULKNOTRANSACTIONS)</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-229">Указывает, будет ли в рамках транзакции SQL массовых операций.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-229">Indicates whether SQL bulk operations are transacted.</span></span> <span data-ttu-id="5dc3e-230">Больших массовых операций может завершиться неудачно в рамках транзакции, из-за задержки ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-230">Large bulk operations might fail when transacted, due to resource delays.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-231">Курсоры Fat OLEDB:Enable Jet</span><span class="sxs-lookup"><span data-stu-id="5dc3e-231">Jet OLEDB:Enable Fat Cursors</span></span><br />
<span data-ttu-id="5dc3e-232">(DBPROP_JETOLEDB_ENABLEFATCURSOR)</span><span class="sxs-lookup"><span data-stu-id="5dc3e-232">(DBPROP_JETOLEDB_ENABLEFATCURSOR)</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-233">Указывает, следует ли Jet кэшировать несколько строк при заполнении набора записей для источников удаленной строки.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-233">Indicates whether Jet should cache multiple rows when populating a recordset for remote row sources.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-234">Размер кэша курсор OLEDB:Fat Jet</span><span class="sxs-lookup"><span data-stu-id="5dc3e-234">Jet OLEDB:Fat Cursor Cache Size</span></span><br />
<span data-ttu-id="5dc3e-235">(DBPROP_JETOLEDB_FATCURSORMAXROWS)</span><span class="sxs-lookup"><span data-stu-id="5dc3e-235">(DBPROP_JETOLEDB_FATCURSORMAXROWS)</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-236">Указывает число строк, кэш при использовании кэширования строку хранения удаленных данных.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-236">Indicates the number of rows to cache when using remote data store row caching.</span></span> <span data-ttu-id="5dc3e-237">Это значение используется только <strong>Fat курсоры Jet OLEDB:Enable</strong> имеет значение True.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-237">This value is ignored unless <strong>Jet OLEDB:Enable Fat Cursors</strong> is True.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-238">Jet OLEDB: несогласованные</span><span class="sxs-lookup"><span data-stu-id="5dc3e-238">Jet OLEDB:Inconsistent</span></span><br />
<span data-ttu-id="5dc3e-239">(DBPROP_JETOLEDB_INCONSISTENT)</span><span class="sxs-lookup"><span data-stu-id="5dc3e-239">(DBPROP_JETOLEDB_INCONSISTENT)</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-240">Указывает, разрешить ли результаты запроса несогласованных обновлений.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-240">Indicates whether query results allow inconsistent updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-241">Jet OLEDB: блокировка степень детализации</span><span class="sxs-lookup"><span data-stu-id="5dc3e-241">Jet OLEDB:Locking Granularity</span></span><br />
<span data-ttu-id="5dc3e-242">(DBPROP_JETOLEDB_LOCKGRANULARITY)</span><span class="sxs-lookup"><span data-stu-id="5dc3e-242">(DBPROP_JETOLEDB_LOCKGRANULARITY)</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-243">Указывает, открыт ли таблицы с помощью блокировка на уровне.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-243">Indicates whether a table is opened using row-level locking.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-244">Оператор к серверу OLEDB:ODBC Jet</span><span class="sxs-lookup"><span data-stu-id="5dc3e-244">Jet OLEDB:ODBC Pass-Through Statement</span></span><br />
<span data-ttu-id="5dc3e-245">(DBPROP_JETOLEDB_ODBCPASSTHROUGH)</span><span class="sxs-lookup"><span data-stu-id="5dc3e-245">(DBPROP_JETOLEDB_ODBCPASSTHROUGH)</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-246">Указывает, что Jet должен передаваться текст SQL в объект <strong>команды</strong> для серверного компонента без изменений.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-246">Indicates that Jet should pass the SQL text in a <strong>Command</strong> object to the back end unaltered.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-247">Jet OLEDB:Partial массовых операций</span><span class="sxs-lookup"><span data-stu-id="5dc3e-247">Jet OLEDB:Partial Bulk Ops</span></span><br />
<span data-ttu-id="5dc3e-248">(DBPROP_JETOLEDB_BULKPARTIAL)</span><span class="sxs-lookup"><span data-stu-id="5dc3e-248">(DBPROP_JETOLEDB_BULKPARTIAL)</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-249">Задает поведение Jet при операции SQL DML с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-249">Indicates Jet's behavior when SQL DML operations fail.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-250">OLEDB:Pass Jet через массовых операций запросов</span><span class="sxs-lookup"><span data-stu-id="5dc3e-250">Jet OLEDB:Pass Through Query Bulk-Op</span></span><br />
<span data-ttu-id="5dc3e-251">(DBPROP_JETOLEDB_PASSTHROUGHBULKOP)</span><span class="sxs-lookup"><span data-stu-id="5dc3e-251">(DBPROP_JETOLEDB_PASSTHROUGHBULKOP)</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-252">Указывает, запросов, которые не возвращает <strong>записей</strong> передаются ли изменена к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-252">Indicates whether queries that do not return a <strong>Recordset</strong> are passed unaltered to the data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-253">Строка подключения OLEDB:Pass Jet посредством запроса</span><span class="sxs-lookup"><span data-stu-id="5dc3e-253">Jet OLEDB:Pass Through Query Connect String</span></span><br />
<span data-ttu-id="5dc3e-254">(DBPROP_JETOLEDB_ODBCPASSTHROUGHCONNECTSTRING)</span><span class="sxs-lookup"><span data-stu-id="5dc3e-254">(DBPROP_JETOLEDB_ODBCPASSTHROUGHCONNECTSTRING)</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-255">Указывает Jet строку подключения, используемую для подключения к удаленному хранилищу.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-255">Indicates the Jet connect string used to connect to a remote data store.</span></span> <span data-ttu-id="5dc3e-256">Это значение используется только <strong>Jet OLEDB:ODBC к серверу оператор</strong> имеет значение True.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-256">This value is ignored unless <strong>Jet OLEDB:ODBC Pass-Through Statement</strong> is True.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-257">Jet OLEDB: хранимых запросов</span><span class="sxs-lookup"><span data-stu-id="5dc3e-257">Jet OLEDB:Stored Query</span></span><br />
<span data-ttu-id="5dc3e-258">(DBPROP_JETOLEDB_STOREDQUERY)</span><span class="sxs-lookup"><span data-stu-id="5dc3e-258">(DBPROP_JETOLEDB_STOREDQUERY)</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-259">Указывает, будет ли текст команды должны обрабатываются как сохраненного запроса вместо команды SQL.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-259">Indicates whether the command text should be interpreted as a stored query instead of an SQL command.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-260">Jet OLEDB: проверка правил набора</span><span class="sxs-lookup"><span data-stu-id="5dc3e-260">Jet OLEDB:Validate Rules On Set</span></span><br />
<span data-ttu-id="5dc3e-261">(DBPROP_JETOLEDB_VALIDATEONSET)</span><span class="sxs-lookup"><span data-stu-id="5dc3e-261">(DBPROP_JETOLEDB_VALIDATEONSET)</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-262">Указывает, будет ли правила проверки Jet вычисляются при имеет значение столбца или изменения применяются к базе данных.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-262">Indicates whether the Jet validation rules are evaluated when column data is set or when the changes are committed to the database.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5dc3e-263">По умолчанию поставщик OLE DB для Microsoft Jet открывается в режиме чтения и записи баз данных Microsoft Jet.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-263">By default, the OLE DB Provider for Microsoft Jet opens Microsoft Jet databases in read/write mode.</span></span> <span data-ttu-id="5dc3e-264">Чтобы открыть базу данных в режим только для чтения, присвойте свойству [режим](mode-property-ado.md) объекта ADO- **подключения** в **adModeRead**.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-264">To open a database in read-only mode, set the [Mode](mode-property-ado.md) property on the ADO **Connection** object to **adModeRead**.</span></span>

## <a name="command-object-usage"></a><span data-ttu-id="5dc3e-265">Использование объекта команды</span><span class="sxs-lookup"><span data-stu-id="5dc3e-265">Command Object Usage</span></span>

<span data-ttu-id="5dc3e-266">Текст команды в объекте [команда](command-object-ado.md) использует диалект Microsoft Jet SQL.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-266">Command text in the [Command](command-object-ado.md) object uses the Microsoft Jet SQL dialect.</span></span> <span data-ttu-id="5dc3e-267">Можно указать возвращающие строки запросов, запросов и имена таблиц в текст команды; Тем не менее хранимые процедуры не поддерживаются и не должен быть указан.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-267">You can specify row-returning queries, action queries, and table names in the command text; however, stored procedures are not supported and should not be specified.</span></span>

## <a name="recordset-behavior"></a><span data-ttu-id="5dc3e-268">Поведение набора записей</span><span class="sxs-lookup"><span data-stu-id="5dc3e-268">Recordset Behavior</span></span>

<span data-ttu-id="5dc3e-269">Базы данных Microsoft Jet не поддерживает динамические курсоры.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-269">The Microsoft Jet database engine does not support dynamic cursors.</span></span> <span data-ttu-id="5dc3e-270">Таким образом поставщик OLE DB для Microsoft Jet не поддерживает тип **adLockDynamic** курсора.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-270">Therefore, the OLE DB Provider for Microsoft Jet does not support the **adLockDynamic** cursor type.</span></span> <span data-ttu-id="5dc3e-271">При запросе динамического курсора поставщик вернуть курсор набора ключей и сброс свойство [CursorType](cursortype-property-ado.md) указывает, что возвращаемые тип [набора записей](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="5dc3e-271">When a dynamic cursor is requested, the provider will return a keyset cursor and reset the [CursorType](cursortype-property-ado.md) property to indicate the type of [Recordset](recordset-object-ado.md) returned.</span></span> <span data-ttu-id="5dc3e-272">Затем, если запрашивается обновляемых **записей** (**LockType для** — **adLockOptimistic**, **adLockBatchOptimistic**или **adLockPessimistic**) также вернет курсор набора ключей и Сброс **CursorType** поставщика свойство.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-272">Further, if an updatable **Recordset** is requested (**LockType** is **adLockOptimistic**, **adLockBatchOptimistic**, or **adLockPessimistic**) the provider will also return a keyset cursor and reset the **CursorType** property.</span></span>

## <a name="dynamic-properties"></a><span data-ttu-id="5dc3e-273">Динамические свойства</span><span class="sxs-lookup"><span data-stu-id="5dc3e-273">Dynamic Properties</span></span>

<span data-ttu-id="5dc3e-274">Поставщик OLE DB для Microsoft Jet вставляет несколько динамических свойств в коллекцию **свойств** объектов неоткрытый [подключения](connection-object-ado.md), [записей](recordset-object-ado.md)и [команды](command-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="5dc3e-274">The OLE DB Provider for Microsoft Jet inserts several dynamic properties into the **Properties** collection of the unopened [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md), and [Command](command-object-ado.md) objects.</span></span>

<span data-ttu-id="5dc3e-275">В таблицах ниже — это cross-index имен ADO и OLE DB для каждого динамического свойства.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-275">The tables below are a cross-index of the ADO and OLE DB names for each dynamic property.</span></span> <span data-ttu-id="5dc3e-276">Справочник программиста OLE DB указано имя свойства ADO по слову «Описание».</span><span class="sxs-lookup"><span data-stu-id="5dc3e-276">The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description."</span></span> <span data-ttu-id="5dc3e-277">Дополнительные сведения об этих свойств можно найти в Справочник программиста OLE DB.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-277">You can find more information about these properties in the OLE DB Programmer's Reference.</span></span> <span data-ttu-id="5dc3e-278">Поиск имени свойства OLE DB в индексе или просмотреть приложение C: OLE DB свойства.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-278">Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span></span>

## <a name="connection-dynamic-properties"></a><span data-ttu-id="5dc3e-279">Динамические свойства подключения</span><span class="sxs-lookup"><span data-stu-id="5dc3e-279">Connection Dynamic Properties</span></span>

<span data-ttu-id="5dc3e-280">Коллекция **Properties** объект **подключения** добавляются следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-280">The following properties are added to the **Connection** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5dc3e-281">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="5dc3e-281">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="5dc3e-282">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="5dc3e-282">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-283">Активных сеансов</span><span class="sxs-lookup"><span data-stu-id="5dc3e-283">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-284">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="5dc3e-284">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-285">Прерывание Asynchable</span><span class="sxs-lookup"><span data-stu-id="5dc3e-285">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-286">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="5dc3e-286">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-287">Зафиксировать Asynchable</span><span class="sxs-lookup"><span data-stu-id="5dc3e-287">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-288">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="5dc3e-288">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-289">Уровни изоляции автоматической фиксации</span><span class="sxs-lookup"><span data-stu-id="5dc3e-289">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-290">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="5dc3e-290">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-291">Расположение каталога</span><span class="sxs-lookup"><span data-stu-id="5dc3e-291">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-292">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="5dc3e-292">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-293">Каталог терминов</span><span class="sxs-lookup"><span data-stu-id="5dc3e-293">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-294">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="5dc3e-294">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-295">Определение столбца</span><span class="sxs-lookup"><span data-stu-id="5dc3e-295">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-296">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="5dc3e-296">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-297">Текущий каталог</span><span class="sxs-lookup"><span data-stu-id="5dc3e-297">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-298">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="5dc3e-298">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-299">Источник данных</span><span class="sxs-lookup"><span data-stu-id="5dc3e-299">Data Source</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-300">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="5dc3e-300">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-301">Имя источника данных</span><span class="sxs-lookup"><span data-stu-id="5dc3e-301">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-302">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="5dc3e-302">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-303">Модель потоков объекта источника данных</span><span class="sxs-lookup"><span data-stu-id="5dc3e-303">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-304">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="5dc3e-304">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-305">Имя СУБД</span><span class="sxs-lookup"><span data-stu-id="5dc3e-305">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-306">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="5dc3e-306">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-307">Версия СУБД</span><span class="sxs-lookup"><span data-stu-id="5dc3e-307">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-308">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="5dc3e-308">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-309">ГРУППИРОВКА по поддержке</span><span class="sxs-lookup"><span data-stu-id="5dc3e-309">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-310">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="5dc3e-310">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-311">Поддержка разнородных таблиц</span><span class="sxs-lookup"><span data-stu-id="5dc3e-311">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-312">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="5dc3e-312">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-313">Идентификатор регистра</span><span class="sxs-lookup"><span data-stu-id="5dc3e-313">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-314">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="5dc3e-314">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-315">Уровни изоляции</span><span class="sxs-lookup"><span data-stu-id="5dc3e-315">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-316">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="5dc3e-316">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-317">Хранение изоляции</span><span class="sxs-lookup"><span data-stu-id="5dc3e-317">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-318">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="5dc3e-318">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-319">Идентификатор языка</span><span class="sxs-lookup"><span data-stu-id="5dc3e-319">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-320">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="5dc3e-320">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-321">Максимальный размер индекса</span><span class="sxs-lookup"><span data-stu-id="5dc3e-321">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-322">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="5dc3e-322">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-323">Максимальный размер строки</span><span class="sxs-lookup"><span data-stu-id="5dc3e-323">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-324">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="5dc3e-324">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-325">Максимальный размер строки включает в себя больших двоичных ОБЪЕКТОВ</span><span class="sxs-lookup"><span data-stu-id="5dc3e-325">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-326">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="5dc3e-326">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-327">Максимальная таблиц в Выбор</span><span class="sxs-lookup"><span data-stu-id="5dc3e-327">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-328">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="5dc3e-328">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-329">Mode</span><span class="sxs-lookup"><span data-stu-id="5dc3e-329">Mode</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-330">DBPROP_INIT_MODE</span><span class="sxs-lookup"><span data-stu-id="5dc3e-330">DBPROP_INIT_MODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-331">Несколько наборов параметров</span><span class="sxs-lookup"><span data-stu-id="5dc3e-331">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-332">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="5dc3e-332">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-333">Несколько результатов</span><span class="sxs-lookup"><span data-stu-id="5dc3e-333">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-334">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="5dc3e-334">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-335">Несколько объектов хранения</span><span class="sxs-lookup"><span data-stu-id="5dc3e-335">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-336">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="5dc3e-336">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-337">Обновление нескольких таблицы</span><span class="sxs-lookup"><span data-stu-id="5dc3e-337">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-338">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="5dc3e-338">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-339">Порядок сортировки значений NULL</span><span class="sxs-lookup"><span data-stu-id="5dc3e-339">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-340">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="5dc3e-340">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-341">Поведение NULL объединения</span><span class="sxs-lookup"><span data-stu-id="5dc3e-341">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-342">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="5dc3e-342">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-343">Версия OLE DB</span><span class="sxs-lookup"><span data-stu-id="5dc3e-343">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-344">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="5dc3e-344">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-345">Поддержка OLE-объектов</span><span class="sxs-lookup"><span data-stu-id="5dc3e-345">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-346">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="5dc3e-346">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-347">Поддержка открытых наборов строк</span><span class="sxs-lookup"><span data-stu-id="5dc3e-347">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-348">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="5dc3e-348">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-349">ORDER BY столбцы в списке Select</span><span class="sxs-lookup"><span data-stu-id="5dc3e-349">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-350">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="5dc3e-350">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-351">Выходной параметр доступности</span><span class="sxs-lookup"><span data-stu-id="5dc3e-351">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-352">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="5dc3e-352">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-353">Передайте с указанные методы</span><span class="sxs-lookup"><span data-stu-id="5dc3e-353">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-354">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="5dc3e-354">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-355">Пароль</span><span class="sxs-lookup"><span data-stu-id="5dc3e-355">Password</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-356">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="5dc3e-356">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-357">Тип сохраняемого идентификатора</span><span class="sxs-lookup"><span data-stu-id="5dc3e-357">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-358">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="5dc3e-358">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-359">Подготовка поведение аварийное завершение</span><span class="sxs-lookup"><span data-stu-id="5dc3e-359">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-360">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="5dc3e-360">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-361">Подготовка поведение выделения</span><span class="sxs-lookup"><span data-stu-id="5dc3e-361">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-362">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="5dc3e-362">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-363">Процедура терминов</span><span class="sxs-lookup"><span data-stu-id="5dc3e-363">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-364">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="5dc3e-364">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-365">Запрос</span><span class="sxs-lookup"><span data-stu-id="5dc3e-365">Prompt</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-366">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="5dc3e-366">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-367">Понятное имя поставщика</span><span class="sxs-lookup"><span data-stu-id="5dc3e-367">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-368">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="5dc3e-368">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-369">Имя поставщика</span><span class="sxs-lookup"><span data-stu-id="5dc3e-369">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-370">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="5dc3e-370">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-371">Версия поставщика</span><span class="sxs-lookup"><span data-stu-id="5dc3e-371">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-372">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="5dc3e-372">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-373">Источник данных только для чтения</span><span class="sxs-lookup"><span data-stu-id="5dc3e-373">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-374">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="5dc3e-374">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-375">Преобразование строк на команду</span><span class="sxs-lookup"><span data-stu-id="5dc3e-375">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-376">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="5dc3e-376">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-377">Схема терминов</span><span class="sxs-lookup"><span data-stu-id="5dc3e-377">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-378">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="5dc3e-378">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-379">Об использовании схемы</span><span class="sxs-lookup"><span data-stu-id="5dc3e-379">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-380">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="5dc3e-380">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-381">Поддержка SQL</span><span class="sxs-lookup"><span data-stu-id="5dc3e-381">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-382">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="5dc3e-382">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-383">Структурированное хранилище</span><span class="sxs-lookup"><span data-stu-id="5dc3e-383">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-384">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="5dc3e-384">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-385">Поддержка вложенного запроса</span><span class="sxs-lookup"><span data-stu-id="5dc3e-385">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-386">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="5dc3e-386">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-387">В таблице терминов</span><span class="sxs-lookup"><span data-stu-id="5dc3e-387">Table Term</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-388">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="5dc3e-388">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-389">Транзакций DDL</span><span class="sxs-lookup"><span data-stu-id="5dc3e-389">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-390">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="5dc3e-390">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-391">Идентификатор пользователя</span><span class="sxs-lookup"><span data-stu-id="5dc3e-391">User ID</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-392">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="5dc3e-392">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-393">Имя пользователя</span><span class="sxs-lookup"><span data-stu-id="5dc3e-393">User Name</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-394">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="5dc3e-394">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-395">Дескриптор окна</span><span class="sxs-lookup"><span data-stu-id="5dc3e-395">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-396">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="5dc3e-396">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a><span data-ttu-id="5dc3e-397">Свойства динамической набора записей</span><span class="sxs-lookup"><span data-stu-id="5dc3e-397">Recordset Dynamic Properties</span></span>

<span data-ttu-id="5dc3e-398">Следующие свойства добавляются в коллекцию **свойств** объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="5dc3e-398">The following properties are added to the **Recordset** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5dc3e-399">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="5dc3e-399">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="5dc3e-400">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="5dc3e-400">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-401">Порядок доступа</span><span class="sxs-lookup"><span data-stu-id="5dc3e-401">Access Order</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-402">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="5dc3e-402">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-403">Только для добавления строк</span><span class="sxs-lookup"><span data-stu-id="5dc3e-403">Append-Only Rowset</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-404">DBPROP_APPENDONLY</span><span class="sxs-lookup"><span data-stu-id="5dc3e-404">DBPROP_APPENDONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-405">Блокировка объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="5dc3e-405">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-406">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="5dc3e-406">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-407">Тип закладки</span><span class="sxs-lookup"><span data-stu-id="5dc3e-407">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-408">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="5dc3e-408">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-409">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="5dc3e-409">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-410">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="5dc3e-410">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-411">Упорядоченные закладки</span><span class="sxs-lookup"><span data-stu-id="5dc3e-411">Bookmarks Ordered</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-412">DBPROP_ORDEREDBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="5dc3e-412">DBPROP_ORDEREDBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-413">Кэш отложенной столбцов</span><span class="sxs-lookup"><span data-stu-id="5dc3e-413">Cache Deferred Columns</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-414">DBPROP_CACHEDEFERRED</span><span class="sxs-lookup"><span data-stu-id="5dc3e-414">DBPROP_CACHEDEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-415">Изменение вставленных строк</span><span class="sxs-lookup"><span data-stu-id="5dc3e-415">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-416">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="5dc3e-416">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-417">Права доступа столбца</span><span class="sxs-lookup"><span data-stu-id="5dc3e-417">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-418">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="5dc3e-418">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-419">Столбец набор уведомлений</span><span class="sxs-lookup"><span data-stu-id="5dc3e-419">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-420">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="5dc3e-420">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-421">Столбец для записи</span><span class="sxs-lookup"><span data-stu-id="5dc3e-421">Column Writable</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-422">DBPROP_MAYWRITECOLUMN</span><span class="sxs-lookup"><span data-stu-id="5dc3e-422">DBPROP_MAYWRITECOLUMN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-423">Отложите столбца</span><span class="sxs-lookup"><span data-stu-id="5dc3e-423">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-424">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="5dc3e-424">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-425">Отложенное обновление объекта хранения</span><span class="sxs-lookup"><span data-stu-id="5dc3e-425">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-426">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="5dc3e-426">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-427">Выборку</span><span class="sxs-lookup"><span data-stu-id="5dc3e-427">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-428">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="5dc3e-428">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-429">Хранение строк</span><span class="sxs-lookup"><span data-stu-id="5dc3e-429">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-430">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="5dc3e-430">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-431">IAccessor</span><span class="sxs-lookup"><span data-stu-id="5dc3e-431">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-432">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="5dc3e-432">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-433">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="5dc3e-433">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-434">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="5dc3e-434">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-435">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="5dc3e-435">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-436">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="5dc3e-436">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-437">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="5dc3e-437">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-438">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="5dc3e-438">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-439">IConvertType</span><span class="sxs-lookup"><span data-stu-id="5dc3e-439">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-440">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="5dc3e-440">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-441">ILockBytes</span><span class="sxs-lookup"><span data-stu-id="5dc3e-441">ILockBytes</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-442">DBPROP_ILockBytes</span><span class="sxs-lookup"><span data-stu-id="5dc3e-442">DBPROP_ILockBytes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-443">Немобильные строки</span><span class="sxs-lookup"><span data-stu-id="5dc3e-443">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-444">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="5dc3e-444">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-445">IRowset</span><span class="sxs-lookup"><span data-stu-id="5dc3e-445">IRowset</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-446">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="5dc3e-446">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-447">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="5dc3e-447">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-448">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="5dc3e-448">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-449">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="5dc3e-449">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-450">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="5dc3e-450">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-451">IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="5dc3e-451">IRowsetIndex</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-452">DBPROP_IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="5dc3e-452">DBPROP_IRowsetIndex</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-453">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="5dc3e-453">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-454">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="5dc3e-454">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-455">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="5dc3e-455">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-456">DBPROP_IRowsestLocate</span><span class="sxs-lookup"><span data-stu-id="5dc3e-456">DBPROP_IRowsestLocate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-457">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="5dc3e-457">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-458">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="5dc3e-458">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-459">DBPROP_IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="5dc3e-459">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-460">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="5dc3e-460">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-461">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="5dc3e-461">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-462">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="5dc3e-462">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-463">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="5dc3e-463">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-464">IStorage</span><span class="sxs-lookup"><span data-stu-id="5dc3e-464">IStorage</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-465">DBPROP_IStorage</span><span class="sxs-lookup"><span data-stu-id="5dc3e-465">DBPROP_IStorage</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-466">IStream</span><span class="sxs-lookup"><span data-stu-id="5dc3e-466">IStream</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-467">DBPROP_IStream</span><span class="sxs-lookup"><span data-stu-id="5dc3e-467">DBPROP_IStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-468">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="5dc3e-468">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-469">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="5dc3e-469">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-470">Литерал закладки</span><span class="sxs-lookup"><span data-stu-id="5dc3e-470">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-471">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="5dc3e-471">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-472">Удостоверение литерала строки</span><span class="sxs-lookup"><span data-stu-id="5dc3e-472">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-473">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="5dc3e-473">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-474">Максимальное число открытых строк</span><span class="sxs-lookup"><span data-stu-id="5dc3e-474">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-475">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="5dc3e-475">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-476">Максимум ожидающие строк</span><span class="sxs-lookup"><span data-stu-id="5dc3e-476">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-477">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="5dc3e-477">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-478">Максимальное число строк</span><span class="sxs-lookup"><span data-stu-id="5dc3e-478">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-479">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="5dc3e-479">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-480">Использование памяти</span><span class="sxs-lookup"><span data-stu-id="5dc3e-480">Memory Usage</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-481">ОПРЕДЕЛЕН</span><span class="sxs-lookup"><span data-stu-id="5dc3e-481">DBPROP_MEMORYUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-482">Степень детализации уведомлений</span><span class="sxs-lookup"><span data-stu-id="5dc3e-482">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-483">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="5dc3e-483">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-484">Этапы уведомлений</span><span class="sxs-lookup"><span data-stu-id="5dc3e-484">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-485">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="5dc3e-485">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-486">Объекты в транзакции</span><span class="sxs-lookup"><span data-stu-id="5dc3e-486">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-487">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="5dc3e-487">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-488">Видны прочие изменения</span><span class="sxs-lookup"><span data-stu-id="5dc3e-488">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-489">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="5dc3e-489">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-490">Других пользователей вставки видимым</span><span class="sxs-lookup"><span data-stu-id="5dc3e-490">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-491">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="5dc3e-491">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-492">Видны собственные изменения</span><span class="sxs-lookup"><span data-stu-id="5dc3e-492">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-493">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="5dc3e-493">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-494">Видны собственные операции вставки</span><span class="sxs-lookup"><span data-stu-id="5dc3e-494">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-495">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="5dc3e-495">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-496">Сохранять при аварийном завершении</span><span class="sxs-lookup"><span data-stu-id="5dc3e-496">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-497">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="5dc3e-497">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-498">Сохранять при фиксации</span><span class="sxs-lookup"><span data-stu-id="5dc3e-498">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-499">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="5dc3e-499">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-500">Быстрый перезапуск</span><span class="sxs-lookup"><span data-stu-id="5dc3e-500">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-501">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="5dc3e-501">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-502">Повторные события</span><span class="sxs-lookup"><span data-stu-id="5dc3e-502">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-503">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="5dc3e-503">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-504">Удаление удаленных строк</span><span class="sxs-lookup"><span data-stu-id="5dc3e-504">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-505">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="5dc3e-505">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-506">Сообщить о нескольких изменений</span><span class="sxs-lookup"><span data-stu-id="5dc3e-506">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-507">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="5dc3e-507">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-508">Вернуть ожидающие вставки</span><span class="sxs-lookup"><span data-stu-id="5dc3e-508">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-509">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="5dc3e-509">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-510">Удалить строку уведомлений</span><span class="sxs-lookup"><span data-stu-id="5dc3e-510">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-511">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="5dc3e-511">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-512">Строка первого уведомления об изменении</span><span class="sxs-lookup"><span data-stu-id="5dc3e-512">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-513">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="5dc3e-513">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-514">Строка вставки уведомлений</span><span class="sxs-lookup"><span data-stu-id="5dc3e-514">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-515">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="5dc3e-515">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-516">Привилегии строки</span><span class="sxs-lookup"><span data-stu-id="5dc3e-516">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-517">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="5dc3e-517">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-518">Уведомления о повторной синхронизации строки</span><span class="sxs-lookup"><span data-stu-id="5dc3e-518">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-519">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="5dc3e-519">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-520">Строка, потоковой модели</span><span class="sxs-lookup"><span data-stu-id="5dc3e-520">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-521">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="5dc3e-521">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-522">Уведомление об изменении отмены строки</span><span class="sxs-lookup"><span data-stu-id="5dc3e-522">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-523">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="5dc3e-523">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-524">Строка отмены Delete уведомлений</span><span class="sxs-lookup"><span data-stu-id="5dc3e-524">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-525">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="5dc3e-525">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-526">Вставка отмены строки уведомлений</span><span class="sxs-lookup"><span data-stu-id="5dc3e-526">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-527">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="5dc3e-527">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-528">Уведомление об обновлении строки</span><span class="sxs-lookup"><span data-stu-id="5dc3e-528">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-529">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="5dc3e-529">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-530">Уведомление об изменении положения строк выборки</span><span class="sxs-lookup"><span data-stu-id="5dc3e-530">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-531">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="5dc3e-531">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-532">Уведомление о выпуске набора строк</span><span class="sxs-lookup"><span data-stu-id="5dc3e-532">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-533">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="5dc3e-533">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-534">Прокрутка назад</span><span class="sxs-lookup"><span data-stu-id="5dc3e-534">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-535">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="5dc3e-535">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-536">Пропустить удаленных закладки</span><span class="sxs-lookup"><span data-stu-id="5dc3e-536">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-537">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="5dc3e-537">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-538">Строка строгого удостоверений</span><span class="sxs-lookup"><span data-stu-id="5dc3e-538">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-539">DBPROP_STRONGITDENTITY</span><span class="sxs-lookup"><span data-stu-id="5dc3e-539">DBPROP_STRONGITDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-540">Возможности обновления</span><span class="sxs-lookup"><span data-stu-id="5dc3e-540">Updatability</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-541">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="5dc3e-541">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-542">Использование закладок</span><span class="sxs-lookup"><span data-stu-id="5dc3e-542">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-543">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="5dc3e-543">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a><span data-ttu-id="5dc3e-544">Динамические свойства команды</span><span class="sxs-lookup"><span data-stu-id="5dc3e-544">Command Dynamic Properties</span></span>

<span data-ttu-id="5dc3e-545">Следующие свойства добавляются в коллекцию **свойств** объекта **команды** .</span><span class="sxs-lookup"><span data-stu-id="5dc3e-545">The following properties are added to the **Command** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5dc3e-546">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="5dc3e-546">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="5dc3e-547">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="5dc3e-547">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-548">Порядок доступа</span><span class="sxs-lookup"><span data-stu-id="5dc3e-548">Access Order</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-549">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="5dc3e-549">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-550">Только для добавления строк</span><span class="sxs-lookup"><span data-stu-id="5dc3e-550">Append-Only Rowset</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-551">DBPROP_APPENDONLY</span><span class="sxs-lookup"><span data-stu-id="5dc3e-551">DBPROP_APPENDONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-552">Блокировка объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="5dc3e-552">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-553">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="5dc3e-553">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-554">Тип закладки</span><span class="sxs-lookup"><span data-stu-id="5dc3e-554">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-555">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="5dc3e-555">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-556">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="5dc3e-556">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-557">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="5dc3e-557">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-558">Изменение вставленных строк</span><span class="sxs-lookup"><span data-stu-id="5dc3e-558">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-559">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="5dc3e-559">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-560">Права доступа столбца</span><span class="sxs-lookup"><span data-stu-id="5dc3e-560">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-561">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="5dc3e-561">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-562">Столбец набор уведомлений</span><span class="sxs-lookup"><span data-stu-id="5dc3e-562">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-563">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="5dc3e-563">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-564">Отложите столбца</span><span class="sxs-lookup"><span data-stu-id="5dc3e-564">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-565">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="5dc3e-565">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-566">Отложенное обновление объекта хранения</span><span class="sxs-lookup"><span data-stu-id="5dc3e-566">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-567">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="5dc3e-567">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-568">Выборку</span><span class="sxs-lookup"><span data-stu-id="5dc3e-568">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-569">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="5dc3e-569">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-570">Хранение строк</span><span class="sxs-lookup"><span data-stu-id="5dc3e-570">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-571">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="5dc3e-571">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-572">IAccessor</span><span class="sxs-lookup"><span data-stu-id="5dc3e-572">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-573">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="5dc3e-573">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-574">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="5dc3e-574">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-575">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="5dc3e-575">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-576">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="5dc3e-576">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-577">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="5dc3e-577">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-578">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="5dc3e-578">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-579">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="5dc3e-579">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-580">IConvertType</span><span class="sxs-lookup"><span data-stu-id="5dc3e-580">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-581">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="5dc3e-581">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-582">ILockBytes</span><span class="sxs-lookup"><span data-stu-id="5dc3e-582">ILockBytes</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-583">DBPROP_ILockBytes</span><span class="sxs-lookup"><span data-stu-id="5dc3e-583">DBPROP_ILockBytes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-584">Немобильные строки</span><span class="sxs-lookup"><span data-stu-id="5dc3e-584">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-585">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="5dc3e-585">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-586">IRowset</span><span class="sxs-lookup"><span data-stu-id="5dc3e-586">IRowset</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-587">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="5dc3e-587">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-588">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="5dc3e-588">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-589">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="5dc3e-589">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-590">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="5dc3e-590">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-591">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="5dc3e-591">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-592">IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="5dc3e-592">IRowsetIndex</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-593">DBPROP_IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="5dc3e-593">DBPROP_IRowsetIndex</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-594">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="5dc3e-594">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-595">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="5dc3e-595">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-596">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="5dc3e-596">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-597">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="5dc3e-597">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-598">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="5dc3e-598">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-599">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="5dc3e-599">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-600">DBPROP_IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="5dc3e-600">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-601">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="5dc3e-601">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-602">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="5dc3e-602">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-603">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="5dc3e-603">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-604">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="5dc3e-604">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-605">IStorage</span><span class="sxs-lookup"><span data-stu-id="5dc3e-605">IStorage</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-606">DBPROP_IStorage</span><span class="sxs-lookup"><span data-stu-id="5dc3e-606">DBPROP_IStorage</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-607">IStream</span><span class="sxs-lookup"><span data-stu-id="5dc3e-607">IStream</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-608">DBPROP_IStream</span><span class="sxs-lookup"><span data-stu-id="5dc3e-608">DBPROP_IStream</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-609">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="5dc3e-609">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-610">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="5dc3e-610">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-611">Литерал закладки</span><span class="sxs-lookup"><span data-stu-id="5dc3e-611">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-612">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="5dc3e-612">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-613">Удостоверение литерала строки</span><span class="sxs-lookup"><span data-stu-id="5dc3e-613">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-614">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="5dc3e-614">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-615">Режим блокировки</span><span class="sxs-lookup"><span data-stu-id="5dc3e-615">Lock Mode</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-616">DBPROP_LOCKMODE</span><span class="sxs-lookup"><span data-stu-id="5dc3e-616">DBPROP_LOCKMODE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-617">Максимальное число открытых строк</span><span class="sxs-lookup"><span data-stu-id="5dc3e-617">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-618">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="5dc3e-618">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-619">Максимум ожидающие строк</span><span class="sxs-lookup"><span data-stu-id="5dc3e-619">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-620">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="5dc3e-620">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-621">Максимальное число строк</span><span class="sxs-lookup"><span data-stu-id="5dc3e-621">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-622">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="5dc3e-622">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-623">Степень детализации уведомлений</span><span class="sxs-lookup"><span data-stu-id="5dc3e-623">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-624">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="5dc3e-624">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-625">Этапы уведомлений</span><span class="sxs-lookup"><span data-stu-id="5dc3e-625">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-626">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="5dc3e-626">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-627">Объекты в транзакции</span><span class="sxs-lookup"><span data-stu-id="5dc3e-627">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-628">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="5dc3e-628">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-629">Видны прочие изменения</span><span class="sxs-lookup"><span data-stu-id="5dc3e-629">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-630">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="5dc3e-630">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-631">Других пользователей вставки видимым</span><span class="sxs-lookup"><span data-stu-id="5dc3e-631">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-632">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="5dc3e-632">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-633">Видны собственные изменения</span><span class="sxs-lookup"><span data-stu-id="5dc3e-633">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-634">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="5dc3e-634">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-635">Видны собственные операции вставки</span><span class="sxs-lookup"><span data-stu-id="5dc3e-635">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-636">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="5dc3e-636">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-637">Сохранять при аварийном завершении</span><span class="sxs-lookup"><span data-stu-id="5dc3e-637">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-638">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="5dc3e-638">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-639">Сохранять при фиксации</span><span class="sxs-lookup"><span data-stu-id="5dc3e-639">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-640">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="5dc3e-640">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-641">Быстрый перезапуск</span><span class="sxs-lookup"><span data-stu-id="5dc3e-641">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-642">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="5dc3e-642">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-643">Повторные события</span><span class="sxs-lookup"><span data-stu-id="5dc3e-643">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-644">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="5dc3e-644">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-645">Удаление удаленных строк</span><span class="sxs-lookup"><span data-stu-id="5dc3e-645">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-646">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="5dc3e-646">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-647">Сообщить о нескольких изменений</span><span class="sxs-lookup"><span data-stu-id="5dc3e-647">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-648">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="5dc3e-648">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-649">Вернуть ожидающие вставки</span><span class="sxs-lookup"><span data-stu-id="5dc3e-649">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-650">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="5dc3e-650">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-651">Удалить строку уведомлений</span><span class="sxs-lookup"><span data-stu-id="5dc3e-651">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-652">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="5dc3e-652">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-653">Строка первого уведомления об изменении</span><span class="sxs-lookup"><span data-stu-id="5dc3e-653">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-654">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="5dc3e-654">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-655">Строка вставки уведомлений</span><span class="sxs-lookup"><span data-stu-id="5dc3e-655">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-656">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="5dc3e-656">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-657">Привилегии строки</span><span class="sxs-lookup"><span data-stu-id="5dc3e-657">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-658">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="5dc3e-658">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-659">Уведомления о повторной синхронизации строки</span><span class="sxs-lookup"><span data-stu-id="5dc3e-659">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-660">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="5dc3e-660">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-661">Строка, потоковой модели</span><span class="sxs-lookup"><span data-stu-id="5dc3e-661">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-662">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="5dc3e-662">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-663">Уведомление об изменении отмены строки</span><span class="sxs-lookup"><span data-stu-id="5dc3e-663">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-664">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="5dc3e-664">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-665">Строка отмены Delete уведомлений</span><span class="sxs-lookup"><span data-stu-id="5dc3e-665">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-666">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="5dc3e-666">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-667">Вставка отмены строки уведомлений</span><span class="sxs-lookup"><span data-stu-id="5dc3e-667">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-668">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="5dc3e-668">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-669">Уведомление об обновлении строки</span><span class="sxs-lookup"><span data-stu-id="5dc3e-669">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-670">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="5dc3e-670">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-671">Уведомление об изменении положения строк выборки</span><span class="sxs-lookup"><span data-stu-id="5dc3e-671">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-672">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="5dc3e-672">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-673">Уведомление о выпуске набора строк</span><span class="sxs-lookup"><span data-stu-id="5dc3e-673">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-674">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="5dc3e-674">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-675">Прокрутка назад</span><span class="sxs-lookup"><span data-stu-id="5dc3e-675">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-676">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="5dc3e-676">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-677">Вставка данных сервера</span><span class="sxs-lookup"><span data-stu-id="5dc3e-677">Server Data on Insert</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-678">DBPROP_SERVERDATAONINSERT</span><span class="sxs-lookup"><span data-stu-id="5dc3e-678">DBPROP_SERVERDATAONINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-679">Пропустить удаленных закладки</span><span class="sxs-lookup"><span data-stu-id="5dc3e-679">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-680">DBPROP_BOOKMARKSKIP</span><span class="sxs-lookup"><span data-stu-id="5dc3e-680">DBPROP_BOOKMARKSKIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-681">Строка строгого удостоверений</span><span class="sxs-lookup"><span data-stu-id="5dc3e-681">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-682">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="5dc3e-682">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc3e-683">Возможности обновления</span><span class="sxs-lookup"><span data-stu-id="5dc3e-683">Updatability</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-684">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="5dc3e-684">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc3e-685">Использование закладок</span><span class="sxs-lookup"><span data-stu-id="5dc3e-685">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="5dc3e-686">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="5dc3e-686">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="5dc3e-687">См. также</span><span class="sxs-lookup"><span data-stu-id="5dc3e-687">See also</span></span>

<span data-ttu-id="5dc3e-688">Сведения о реализации и функциональным сведения о поставщика OLE DB для Microsoft Jet обратитесь к поставщика OLE DB для Microsoft Jet документации в пакете SDK MDAC.</span><span class="sxs-lookup"><span data-stu-id="5dc3e-688">For specific implementation details and functional information about the OLE DB Provider for Microsoft Jet, consult the OLE DB Provider for Microsoft Jet documentation in the MDAC SDK.</span></span>

