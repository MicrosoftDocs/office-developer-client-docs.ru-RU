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
# <a name="microsoft-ole-db-provider-for-microsoft-jet"></a><span data-ttu-id="9b0dc-102">Поставщик Microsoft OLE DB для Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="9b0dc-102">Microsoft OLE DB Provider for Microsoft Jet</span></span>

<span data-ttu-id="9b0dc-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9b0dc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9b0dc-104">Поставщик OLE DB для Microsoft Jet позволяет ADO получать доступ к базам данных Microsoft Jet.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-104">The OLE DB Provider for Microsoft Jet allows ADO to access Microsoft Jet databases.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="9b0dc-105">Параметры строки подключения</span><span class="sxs-lookup"><span data-stu-id="9b0dc-105">Connection String Parameters</span></span>

<span data-ttu-id="9b0dc-106">Чтобы подключиться к этому поставщику, установите *аргумент поставщика* свойства [ConnectionString:](connectionstring-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="9b0dc-106">To connect to this provider, set the *Provider* argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```vb 
 
Microsoft.Jet.OLEDB.4.0 
```

<span data-ttu-id="9b0dc-107">Чтение свойства [Provider](provider-property-ado.md) также вернет эту строку.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-107">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="9b0dc-108">Типичная строка подключения</span><span class="sxs-lookup"><span data-stu-id="9b0dc-108">Typical Connection String</span></span>

<span data-ttu-id="9b0dc-109">Типичная строка подключения для этого поставщика:</span><span class="sxs-lookup"><span data-stu-id="9b0dc-109">A typical connection string for this provider is:</span></span>

```vb 
 
"Provider=Microsoft.Jet.OLEDB.4.0;Data Source=databaseName;User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="9b0dc-110">Строка состоит из этих ключевых слов:</span><span class="sxs-lookup"><span data-stu-id="9b0dc-110">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9b0dc-111">Ключевое слово</span><span class="sxs-lookup"><span data-stu-id="9b0dc-111">Keyword</span></span></p></th>
<th><p><span data-ttu-id="9b0dc-112">Description</span><span class="sxs-lookup"><span data-stu-id="9b0dc-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-113"><strong>Поставщик</strong></span><span class="sxs-lookup"><span data-stu-id="9b0dc-113"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="9b0dc-114">Указывает поставщика OLE DB для Microsoft Jet.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-114">Specifies the OLE DB Provider for Microsoft Jet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-115"><strong>Источник данных</strong></span><span class="sxs-lookup"><span data-stu-id="9b0dc-115"><strong>Data Source</strong></span></span></p></td>
<td><p><span data-ttu-id="9b0dc-116">Указывает путь базы данных и имя файла (например, c:\Northwind.mdb).</span><span class="sxs-lookup"><span data-stu-id="9b0dc-116">Specifies the database path and file name (for example, c:\Northwind.mdb).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-117"><strong>Идентификатор пользователя</strong></span><span class="sxs-lookup"><span data-stu-id="9b0dc-117"><strong>User ID</strong></span></span></p></td>
<td><p><span data-ttu-id="9b0dc-118">Задает имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-118">Specifies the user name.</span></span> <span data-ttu-id="9b0dc-119">Если это ключевое слово не указано, строка &quot; &quot; администратора используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-119">If this keyword is not specified, the string, &quot;admin&quot;, is used by default.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-120"><strong>Password</strong></span><span class="sxs-lookup"><span data-stu-id="9b0dc-120"><strong>Password</strong></span></span></p></td>
<td><p><span data-ttu-id="9b0dc-121">Указывает пароль пользователя.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-121">Specifies the user password.</span></span> <span data-ttu-id="9b0dc-122">Если это ключевое слово не указано, пустая строка (), &quot; &quot; используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-122">If this keyword is not specified, the empty string (&quot;&quot;), is used by default.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-connection-parameters"></a><span data-ttu-id="9b0dc-123">Provider-Specific параметры подключения</span><span class="sxs-lookup"><span data-stu-id="9b0dc-123">Provider-Specific Connection Parameters</span></span>

<span data-ttu-id="9b0dc-124">Поставщик OLE DB для Microsoft Jet поддерживает несколько динамических свойств, определенных для конкретного поставщика, в дополнение к тем, которые определены ADO.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-124">The OLE DB Provider for Microsoft Jet supports several provider-specific dynamic properties in addition to those defined by ADO.</span></span> <span data-ttu-id="9b0dc-125">Как и все другие параметры **Подключения,**  их можно установить с помощью коллекции **Свойств** объекта Подключения или в составе строки подключения.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-125">As with all other **Connection** parameters, they can be set via the **Connection** object's **Properties** collection or as part of the connection string.</span></span>

<span data-ttu-id="9b0dc-126">В следующей таблице перечислены эти свойства с соответствующим именем свойства OLE DB в скобки.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-126">The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9b0dc-127">Параметр</span><span class="sxs-lookup"><span data-stu-id="9b0dc-127">Parameter</span></span></p></th>
<th><p><span data-ttu-id="9b0dc-128">Описание</span><span class="sxs-lookup"><span data-stu-id="9b0dc-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-129">Jet OLEDB:Compact Reclaimed Space Amount</span><span class="sxs-lookup"><span data-stu-id="9b0dc-129">Jet OLEDB:Compact Reclaimed Space Amount</span></span><br />
<span data-ttu-id="9b0dc-130">(DBPROP_JETOLEDB_COMPACTFREESPACESIZE)</span><span class="sxs-lookup"><span data-stu-id="9b0dc-130">(DBPROP_JETOLEDB_COMPACTFREESPACESIZE)</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-131">Указывает оценку количества пространства в bytes, которое можно восстановить, уплотнив базу данных.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-131">Indicates an estimate of the amount of space, in bytes, that can be reclaimed by compacting the database.</span></span> <span data-ttu-id="9b0dc-132">Это значение допустимо только после подключения к базе данных.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-132">This value is only valid after a database connection has been established.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-133">Jet OLEDB:Connection Control</span><span class="sxs-lookup"><span data-stu-id="9b0dc-133">Jet OLEDB:Connection Control</span></span><br />
<span data-ttu-id="9b0dc-134">(DBPROP_JETOLEDB_CONNECTIONCONTROL)</span><span class="sxs-lookup"><span data-stu-id="9b0dc-134">(DBPROP_JETOLEDB_CONNECTIONCONTROL)</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-135">Указывает, могут ли пользователи подключаться к базе данных.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-135">Indicates whether users can connect to the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-136">Jet OLEDB:Create System Database</span><span class="sxs-lookup"><span data-stu-id="9b0dc-136">Jet OLEDB:Create System Database</span></span><br />
<span data-ttu-id="9b0dc-137">(DBPROP_JETOLEDB_CREATESYSTEMDATABASE)</span><span class="sxs-lookup"><span data-stu-id="9b0dc-137">(DBPROP_JETOLEDB_CREATESYSTEMDATABASE)</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-138">Указывает, следует ли создавать системную базу данных при создании нового источника данных.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-138">Indicates whether a system database should be created when creating a new data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-139">Jet OLEDB:Database Locking Mode</span><span class="sxs-lookup"><span data-stu-id="9b0dc-139">Jet OLEDB:Database Locking Mode</span></span><br />
<span data-ttu-id="9b0dc-140">(DBPROP_JETOLEDB_DATABASELOCKMODE)</span><span class="sxs-lookup"><span data-stu-id="9b0dc-140">(DBPROP_JETOLEDB_DATABASELOCKMODE)</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-141">Указывает режим блокировки для этой базы данных.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-141">Indicates the locking mode for this database.</span></span> <span data-ttu-id="9b0dc-142">Первый пользователь, открывая базу данных, определяет режим, используемый во время открытия базы данных.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-142">The first user to open the database determines the mode used while the database is open.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-143">Пароль jet OLEDB:Database</span><span class="sxs-lookup"><span data-stu-id="9b0dc-143">Jet OLEDB:Database Password</span></span><br />
<span data-ttu-id="9b0dc-144">(DBPROP_JETOLEDB_DATABASEPASSWORD)</span><span class="sxs-lookup"><span data-stu-id="9b0dc-144">(DBPROP_JETOLEDB_DATABASEPASSWORD)</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-145">Указывает пароль базы данных.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-145">Indicates the database password.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-146">Jet OLEDB:Don't Copy Locale on Compact</span><span class="sxs-lookup"><span data-stu-id="9b0dc-146">Jet OLEDB:Don't Copy Locale on Compact</span></span><br />
<span data-ttu-id="9b0dc-147">(DBPROP_JETOLEDB_COMPACT_DONTCOPYLOCALE)</span><span class="sxs-lookup"><span data-stu-id="9b0dc-147">(DBPROP_JETOLEDB_COMPACT_DONTCOPYLOCALE)</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-148">Указывает, следует ли jet скопировать сведения о локальном уровне при сжатии базы данных.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-148">Indicates whether Jet should copy locale information when compacting a database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-149">Jet OLEDB:Encrypt Database</span><span class="sxs-lookup"><span data-stu-id="9b0dc-149">Jet OLEDB:Encrypt Database</span></span><br />
<span data-ttu-id="9b0dc-150">(DBPROP_JETOLEDB_ENCRYPTDATABASE)</span><span class="sxs-lookup"><span data-stu-id="9b0dc-150">(DBPROP_JETOLEDB_ENCRYPTDATABASE)</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-151">Указывает, следует ли шифровать сжатую базу данных.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-151">Indicates whether a compacted database should be encrypted.</span></span> <span data-ttu-id="9b0dc-152">Если это свойство не установлено, сжатая база данных будет зашифрована, если оригинальная база данных также была зашифрована.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-152">If this property is not set, the compacted database will be encrypted if the original database was also encrypted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-153">Тип двигателя OLEDB:Engine</span><span class="sxs-lookup"><span data-stu-id="9b0dc-153">Jet OLEDB:Engine Type</span></span><br />
<span data-ttu-id="9b0dc-154">(DBPROP_JETOLEDB_ENGINE)</span><span class="sxs-lookup"><span data-stu-id="9b0dc-154">(DBPROP_JETOLEDB_ENGINE)</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-155">Указывает двигатель хранения, используемый для доступа к текущему хранилище данных.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-155">Indicates the storage engine used to access the current data store.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-156">Jet OLEDB:Exclusive Async Delay</span><span class="sxs-lookup"><span data-stu-id="9b0dc-156">Jet OLEDB:Exclusive Async Delay</span></span><br />
<span data-ttu-id="9b0dc-157">(DBPROP_JETOLEDB_EXCLUSIVEASYNCDELAY)</span><span class="sxs-lookup"><span data-stu-id="9b0dc-157">(DBPROP_JETOLEDB_EXCLUSIVEASYNCDELAY)</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-158">Указывает максимальное время, в миллисекунд, что Jet может задерживать асинхронные записи на диск, когда база данных открыта исключительно.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-158">Indicates the maximum length of time, in milliseconds, that Jet can delay asynchronous writes to disk when the database is opened exclusively.</span></span> <span data-ttu-id="9b0dc-159">Это свойство игнорируется, если только время времени транзакции <strong>jet OLEDB:Flush</strong> не установлено до 0.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-159">This property is ignored unless <strong>Jet OLEDB:Flush Transaction Timeout</strong> is set to 0.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-160">Jet OLEDB:Flush Transaction Timeout</span><span class="sxs-lookup"><span data-stu-id="9b0dc-160">Jet OLEDB:Flush Transaction Timeout</span></span><br />
<span data-ttu-id="9b0dc-161">(DBPROP_JETOLEDB_FLUSHTRANSACTIONTIMEOUT)</span><span class="sxs-lookup"><span data-stu-id="9b0dc-161">(DBPROP_JETOLEDB_FLUSHTRANSACTIONTIMEOUT)</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-162">Указывает время ожидания, прежде чем данные, хранимые в кэше для асинхронной записи, фактически будут записаны на диск.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-162">Indicates the amount of time to wait before data stored in a cache for asynchronous writing is actually written to disk.</span></span> <span data-ttu-id="9b0dc-163">Этот параметр переопределяет значения для <strong>jet OLEDB:Shared Async Delay</strong> и <strong>Jet OLEDB:Exclusive Async Delay</strong>.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-163">This setting overrides the values for <strong>Jet OLEDB:Shared Async Delay</strong> and <strong>Jet OLEDB:Exclusive Async Delay</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-164">Jet OLEDB:Global Bulk Transactions</span><span class="sxs-lookup"><span data-stu-id="9b0dc-164">Jet OLEDB:Global Bulk Transactions</span></span><br />
<span data-ttu-id="9b0dc-165">(DBPROP_JETOLEDB_GLOBALBULKNOTRANSACTIONS)</span><span class="sxs-lookup"><span data-stu-id="9b0dc-165">(DBPROP_JETOLEDB_GLOBALBULKNOTRANSACTIONS)</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-166">Указывает, SQL транзакции.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-166">Indicates whether SQL bulk transactions are transacted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-167">Jet OLEDB:Global Partial Bulk Ops</span><span class="sxs-lookup"><span data-stu-id="9b0dc-167">Jet OLEDB:Global Partial Bulk Ops</span></span><br />
<span data-ttu-id="9b0dc-168">(DBPROP_JETOLEDB_GLOBALBULKPARTIAL)</span><span class="sxs-lookup"><span data-stu-id="9b0dc-168">(DBPROP_JETOLEDB_GLOBALBULKPARTIAL)</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-169">Указывает пароль, используемый для открытия базы данных.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-169">Indicates the password used to open the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-170">Синхронизация фиксации Jet OLEDB:Implicit</span><span class="sxs-lookup"><span data-stu-id="9b0dc-170">Jet OLEDB:Implicit Commit Sync</span></span><br />
<span data-ttu-id="9b0dc-171">(DBPROP_JETOLEDB_IMPLICITCOMMITSYNC)</span><span class="sxs-lookup"><span data-stu-id="9b0dc-171">(DBPROP_JETOLEDB_IMPLICITCOMMITSYNC)</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-172">Указывает, пишутся ли изменения во внутренних неявных транзакциях в синхронном или асинхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-172">Indicates whether changes made in internal implicit transactions are written in synchronous or asynchronous mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-173">Jet OLEDB:Lock Delay</span><span class="sxs-lookup"><span data-stu-id="9b0dc-173">Jet OLEDB:Lock Delay</span></span><br />
<span data-ttu-id="9b0dc-174">(DBPROP_JETOLEDB_LOCKDELAY)</span><span class="sxs-lookup"><span data-stu-id="9b0dc-174">(DBPROP_JETOLEDB_LOCKDELAY)</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-175">Указывает количество миллисекунд, которые следует ждать перед попыткой получить блокировку после сбой предыдущей попытки.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-175">Indicates the number of milliseconds to wait before attempting to acquire a lock after a previous attempt has failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-176">Jet OLEDB:Lock Retry</span><span class="sxs-lookup"><span data-stu-id="9b0dc-176">Jet OLEDB:Lock Retry</span></span><br />
<span data-ttu-id="9b0dc-177">(DBPROP_JETOLEDB_LOCKRETRY)</span><span class="sxs-lookup"><span data-stu-id="9b0dc-177">(DBPROP_JETOLEDB_LOCKRETRY)</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-178">Указывает, сколько раз повторяется попытка доступа к заблокированной странице.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-178">Indicates how many times an attempt to access a locked page is repeated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-179">Размер буфера Jet OLEDB:Max</span><span class="sxs-lookup"><span data-stu-id="9b0dc-179">Jet OLEDB:Max Buffer Size</span></span><br />
<span data-ttu-id="9b0dc-180">(DBPROP_JETOLEDB_MAXBUFFERSIZE)</span><span class="sxs-lookup"><span data-stu-id="9b0dc-180">(DBPROP_JETOLEDB_MAXBUFFERSIZE)</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-181">Указывает максимальное количество памяти в килобайтах, которые Jet может использовать до начала очистки изменений на диске.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-181">Indicates the maximum amount of memory, in kilobytes, Jet can use before it starts flushing changes to disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-182">Jet OLEDB:Max Locks Per File</span><span class="sxs-lookup"><span data-stu-id="9b0dc-182">Jet OLEDB:Max Locks Per File</span></span><br />
<span data-ttu-id="9b0dc-183">(DBPROP_JETOLEDB_MAXLOCKSPERFILE)</span><span class="sxs-lookup"><span data-stu-id="9b0dc-183">(DBPROP_JETOLEDB_MAXLOCKSPERFILE)</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-184">Указывает максимальное количество блокировок, которые Jet может разместить в базе данных.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-184">Indicates the maximum number of locks Jet can place on a database.</span></span> <span data-ttu-id="9b0dc-185">Значение по умолчанию — 9500.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-185">The default value is 9500.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-186">Jet OLEDB:Новый пароль базы данных</span><span class="sxs-lookup"><span data-stu-id="9b0dc-186">Jet OLEDB:New Database Password</span></span><br />
<span data-ttu-id="9b0dc-187">(DBPROP_JETOLEDB_NEWDATABASEPASSWORD)</span><span class="sxs-lookup"><span data-stu-id="9b0dc-187">(DBPROP_JETOLEDB_NEWDATABASEPASSWORD)</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-188">Указывает новый пароль, заданной для этой базы данных.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-188">Indicates the new password to be set for this database.</span></span> <span data-ttu-id="9b0dc-189">Старый пароль хранится в <strong>jet OLEDB:Database Password</strong>.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-189">The old password is stored in <strong>Jet OLEDB:Database Password</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-190">Jet OLEDB:ODBC Командный выход</span><span class="sxs-lookup"><span data-stu-id="9b0dc-190">Jet OLEDB:ODBC Command Time Out</span></span><br />
<span data-ttu-id="9b0dc-191">(DBPROP_JETOLEDB_ODBCCOMMANDTIMEOUT)</span><span class="sxs-lookup"><span data-stu-id="9b0dc-191">(DBPROP_JETOLEDB_ODBCCOMMANDTIMEOUT)</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-192">Указывает количество миллисекунд перед удаленным запросом ODBC от Jet.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-192">Indicates the number of milliseconds before a remote ODBC query from Jet will timeout.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-193">Jet OLEDB:Page Locks to Table Lock</span><span class="sxs-lookup"><span data-stu-id="9b0dc-193">Jet OLEDB:Page Locks to Table Lock</span></span><br />
<span data-ttu-id="9b0dc-194">(DBPROP_JETOLEDB_PAGELOCKSTOTABLELOCK)</span><span class="sxs-lookup"><span data-stu-id="9b0dc-194">(DBPROP_JETOLEDB_PAGELOCKSTOTABLELOCK)</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-195">Указывает, сколько страниц необходимо заблокировать в транзакции перед попыткой Jet продвинуть блокировку в блокировку таблицы.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-195">Indicates how many pages need to be locked within a transaction before Jet attempts to promote the lock to a table lock.</span></span> <span data-ttu-id="9b0dc-196">Если это значение 0, блокировка никогда не будет повышена.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-196">If this value is 0, then the lock is never promoted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-197">Jet OLEDB:Page Timeout</span><span class="sxs-lookup"><span data-stu-id="9b0dc-197">Jet OLEDB:Page Timeout</span></span><br />
<span data-ttu-id="9b0dc-198">(DBPROP_JETOLEDB_PAGETIMEOUT)</span><span class="sxs-lookup"><span data-stu-id="9b0dc-198">(DBPROP_JETOLEDB_PAGETIMEOUT)</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-199">Указывает количество миллисекунд Jet, которые будут ждать, прежде чем проверять, устарел ли кэш с файлом базы данных.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-199">Indicates the number of milliseconds Jet will wait before checking to see if its cache is out of date with the database file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-200">Jet OLEDB:Recycle Long-Valued Pages</span><span class="sxs-lookup"><span data-stu-id="9b0dc-200">Jet OLEDB:Recycle Long-Valued Pages</span></span><br />
<span data-ttu-id="9b0dc-201">(DBPROP_JETOLEDB_RECYCLELONGVALUEPAGES)</span><span class="sxs-lookup"><span data-stu-id="9b0dc-201">(DBPROP_JETOLEDB_RECYCLELONGVALUEPAGES)</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-202">Указывает, следует ли jet агрессивно пытаться вернуть страницы BLOB при их освобождении.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-202">Indicates whether Jet should aggressively try to reclaim BLOB pages when they are freed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-203">Jet OLEDB:Registry Path</span><span class="sxs-lookup"><span data-stu-id="9b0dc-203">Jet OLEDB:Registry Path</span></span><br />
<span data-ttu-id="9b0dc-204">(DBPROP_JETOLEDB_REGPATH)</span><span class="sxs-lookup"><span data-stu-id="9b0dc-204">(DBPROP_JETOLEDB_REGPATH)</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-205">Указывает ключ Windows реестра, содержащий значения для двигателя базы данных Jet.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-205">Indicates the Windows registry key that contains values for the Jet database engine.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-206">Jet OLEDB:Reset ISAM Stats</span><span class="sxs-lookup"><span data-stu-id="9b0dc-206">Jet OLEDB:Reset ISAM Stats</span></span><br />
<span data-ttu-id="9b0dc-207">(DBPROP_JETOLEDB_RESETISAMSTATS)</span><span class="sxs-lookup"><span data-stu-id="9b0dc-207">(DBPROP_JETOLEDB_RESETISAMSTATS)</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-208">Указывает, следует ли <strong></strong> DBSCHEMA_JETOLEDB_ISAMSTATS сбросить счетчики производительности после возврата сведений о производительности.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-208">Indicates whether the schema <strong>Recordset</strong> DBSCHEMA_JETOLEDB_ISAMSTATS should reset its performance counters after returning performance information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-209">Jet OLEDB:Shared Async Delay</span><span class="sxs-lookup"><span data-stu-id="9b0dc-209">Jet OLEDB:Shared Async Delay</span></span><br />
<span data-ttu-id="9b0dc-210">(DBPROP_JETOLEDB_SHAREDASYNCDELAY)</span><span class="sxs-lookup"><span data-stu-id="9b0dc-210">(DBPROP_JETOLEDB_SHAREDASYNCDELAY)</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-211">Указывает максимальное количество времени, в миллисекунде Jet может задерживать асинхронные записи на диск, когда база данных открывается в много пользователя режиме.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-211">Indicates the maximum amount of time, in milliseconds, Jet can delay asynchronous writes to disk when the database is opened in multi-user mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-212">База данных Jet OLEDB:System</span><span class="sxs-lookup"><span data-stu-id="9b0dc-212">Jet OLEDB:System Database</span></span><br />
<span data-ttu-id="9b0dc-213">(DBPROP_JETOLEDB_SYSDBPATH)</span><span class="sxs-lookup"><span data-stu-id="9b0dc-213">(DBPROP_JETOLEDB_SYSDBPATH)</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-214">Указывает путь и имя файла для информационного файла workgroup (база данных системы).</span><span class="sxs-lookup"><span data-stu-id="9b0dc-214">Indicates the path and file name for the workgroup information file (system database).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-215">Режим фиксации транзакций Jet OLEDB:Transaction</span><span class="sxs-lookup"><span data-stu-id="9b0dc-215">Jet OLEDB:Transaction Commit Mode</span></span><br />
<span data-ttu-id="9b0dc-216">(DBPROP_JETOLEDB_TXNCOMMITMODE)</span><span class="sxs-lookup"><span data-stu-id="9b0dc-216">(DBPROP_JETOLEDB_TXNCOMMITMODE)</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-217">Указывает, синхронно или асинхронно ли Jet записывает данные на диск при совершении транзакции.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-217">Indicates whether Jet writes data to disk synchronously or asynchronously when a transaction is committed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-218">Синхронизация фиксации jet OLEDB:User</span><span class="sxs-lookup"><span data-stu-id="9b0dc-218">Jet OLEDB:User Commit Sync</span></span><br />
<span data-ttu-id="9b0dc-219">(DBPROP_JETOLEDB_USERCOMMITSYNC)</span><span class="sxs-lookup"><span data-stu-id="9b0dc-219">(DBPROP_JETOLEDB_USERCOMMITSYNC)</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-220">Указывает, пишутся ли изменения в транзакциях в синхронном или асинхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-220">Indicates whether changes made in transactions are written in synchronous or asynchronous mode.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-recordset-and-command-properties"></a><span data-ttu-id="9b0dc-221">Provider-Specific Recordset и Command Properties</span><span class="sxs-lookup"><span data-stu-id="9b0dc-221">Provider-Specific Recordset and Command Properties</span></span>

<span data-ttu-id="9b0dc-222">Поставщик Jet также поддерживает несколько свойств **Recordset** и **Command,** определенных для поставщика.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-222">The Jet provider also supports several provider-specific **Recordset** and **Command** properties.</span></span> <span data-ttu-id="9b0dc-223">Доступ к этим свойствам устанавливается в коллекции **Свойств** объекта **Recordset** или **Command.**</span><span class="sxs-lookup"><span data-stu-id="9b0dc-223">These properties are accessed and set through the **Properties** collection of the **Recordset** or **Command** object.</span></span> <span data-ttu-id="9b0dc-224">В таблице перечислены имя свойства ADO и соответствующее имя свойства OLE DB в скобки.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-224">The table lists the ADO property name and its corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9b0dc-225">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="9b0dc-225">Property Name</span></span></p></th>
<th><p><span data-ttu-id="9b0dc-226">Description</span><span class="sxs-lookup"><span data-stu-id="9b0dc-226">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-227">Jet OLEDB:Bulk Transactions</span><span class="sxs-lookup"><span data-stu-id="9b0dc-227">Jet OLEDB:Bulk Transactions</span></span><br />
<span data-ttu-id="9b0dc-228">(DBPROP_JETOLEDB_BULKNOTRANSACTIONS)</span><span class="sxs-lookup"><span data-stu-id="9b0dc-228">(DBPROP_JETOLEDB_BULKNOTRANSACTIONS)</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-229">Указывает, SQL ли массовые операции.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-229">Indicates whether SQL bulk operations are transacted.</span></span> <span data-ttu-id="9b0dc-230">Крупные массовые операции могут привести к сбойу при переносе из-за задержек ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-230">Large bulk operations might fail when transacted, due to resource delays.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-231">Jet OLEDB:Enable Fat Cursors</span><span class="sxs-lookup"><span data-stu-id="9b0dc-231">Jet OLEDB:Enable Fat Cursors</span></span><br />
<span data-ttu-id="9b0dc-232">(DBPROP_JETOLEDB_ENABLEFATCURSOR)</span><span class="sxs-lookup"><span data-stu-id="9b0dc-232">(DBPROP_JETOLEDB_ENABLEFATCURSOR)</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-233">Указывает, должен ли Jet кэшировать несколько строк при заполнении наборов записей для удаленных источников строк.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-233">Indicates whether Jet should cache multiple rows when populating a recordset for remote row sources.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-234">Jet OLEDB:Fat Cursor Cache Size</span><span class="sxs-lookup"><span data-stu-id="9b0dc-234">Jet OLEDB:Fat Cursor Cache Size</span></span><br />
<span data-ttu-id="9b0dc-235">(DBPROP_JETOLEDB_FATCURSORMAXROWS)</span><span class="sxs-lookup"><span data-stu-id="9b0dc-235">(DBPROP_JETOLEDB_FATCURSORMAXROWS)</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-236">Указывает количество строк кэша при использовании удаленного кэша строк хранения данных.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-236">Indicates the number of rows to cache when using remote data store row caching.</span></span> <span data-ttu-id="9b0dc-237">Это значение игнорируется, если <strong>jet OLEDB:Enable Fat Cursors</strong> is True.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-237">This value is ignored unless <strong>Jet OLEDB:Enable Fat Cursors</strong> is True.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-238">Jet OLEDB:Inconsistent</span><span class="sxs-lookup"><span data-stu-id="9b0dc-238">Jet OLEDB:Inconsistent</span></span><br />
<span data-ttu-id="9b0dc-239">(DBPROP_JETOLEDB_INCONSISTENT)</span><span class="sxs-lookup"><span data-stu-id="9b0dc-239">(DBPROP_JETOLEDB_INCONSISTENT)</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-240">Указывает, позволяют ли результаты запроса несогласованные обновления.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-240">Indicates whether query results allow inconsistent updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-241">Jet OLEDB:Locking Granularity</span><span class="sxs-lookup"><span data-stu-id="9b0dc-241">Jet OLEDB:Locking Granularity</span></span><br />
<span data-ttu-id="9b0dc-242">(DBPROP_JETOLEDB_LOCKGRANULARITY)</span><span class="sxs-lookup"><span data-stu-id="9b0dc-242">(DBPROP_JETOLEDB_LOCKGRANULARITY)</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-243">Указывает, открыта ли таблица с помощью блокировки на уровне строки.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-243">Indicates whether a table is opened using row-level locking.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-244">Заявление jet OLEDB:ODBC Pass-Through</span><span class="sxs-lookup"><span data-stu-id="9b0dc-244">Jet OLEDB:ODBC Pass-Through Statement</span></span><br />
<span data-ttu-id="9b0dc-245">(DBPROP_JETOLEDB_ODBCPASSTHROUGH)</span><span class="sxs-lookup"><span data-stu-id="9b0dc-245">(DBPROP_JETOLEDB_ODBCPASSTHROUGH)</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-246">Указывает, что Jet должен передать SQL в <strong>объекте Command</strong> на задний конец безальтераторно.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-246">Indicates that Jet should pass the SQL text in a <strong>Command</strong> object to the back end unaltered.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-247">Jet OLEDB:Partial Bulk Ops</span><span class="sxs-lookup"><span data-stu-id="9b0dc-247">Jet OLEDB:Partial Bulk Ops</span></span><br />
<span data-ttu-id="9b0dc-248">(DBPROP_JETOLEDB_BULKPARTIAL)</span><span class="sxs-lookup"><span data-stu-id="9b0dc-248">(DBPROP_JETOLEDB_BULKPARTIAL)</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-249">Указывает поведение Jet при сбой SQL DML.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-249">Indicates Jet's behavior when SQL DML operations fail.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-250">Jet OLEDB:Pass Through Query Bulk-Op</span><span class="sxs-lookup"><span data-stu-id="9b0dc-250">Jet OLEDB:Pass Through Query Bulk-Op</span></span><br />
<span data-ttu-id="9b0dc-251">(DBPROP_JETOLEDB_PASSTHROUGHBULKOP)</span><span class="sxs-lookup"><span data-stu-id="9b0dc-251">(DBPROP_JETOLEDB_PASSTHROUGHBULKOP)</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-252">Указывает, передаются ли запросы, которые не возвращают <strong>набор записей,</strong> в источник данных.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-252">Indicates whether queries that do not return a <strong>Recordset</strong> are passed unaltered to the data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-253">Jet OLEDB:Pass Through Query Подключение String</span><span class="sxs-lookup"><span data-stu-id="9b0dc-253">Jet OLEDB:Pass Through Query Connect String</span></span><br />
<span data-ttu-id="9b0dc-254">(DBPROP_JETOLEDB_ODBCPASSTHROUGHCONNECTSTRING)</span><span class="sxs-lookup"><span data-stu-id="9b0dc-254">(DBPROP_JETOLEDB_ODBCPASSTHROUGHCONNECTSTRING)</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-255">Указывает строку jet connect, используемую для подключения к удаленному хранилище данных.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-255">Indicates the Jet connect string used to connect to a remote data store.</span></span> <span data-ttu-id="9b0dc-256">Это значение игнорируется, если <strong>заявление jet OLEDB:ODBC Pass-Through является</strong> true.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-256">This value is ignored unless <strong>Jet OLEDB:ODBC Pass-Through Statement</strong> is True.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-257">Запрос JET OLEDB:Stored</span><span class="sxs-lookup"><span data-stu-id="9b0dc-257">Jet OLEDB:Stored Query</span></span><br />
<span data-ttu-id="9b0dc-258">(DBPROP_JETOLEDB_STOREDQUERY)</span><span class="sxs-lookup"><span data-stu-id="9b0dc-258">(DBPROP_JETOLEDB_STOREDQUERY)</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-259">Указывает, следует ли интерпретировать текст команды как сохраненный запрос, а не SQL команду.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-259">Indicates whether the command text should be interpreted as a stored query instead of an SQL command.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-260">Jet OLEDB:Проверка правил в наборе</span><span class="sxs-lookup"><span data-stu-id="9b0dc-260">Jet OLEDB:Validate Rules On Set</span></span><br />
<span data-ttu-id="9b0dc-261">(DBPROP_JETOLEDB_VALIDATEONSET)</span><span class="sxs-lookup"><span data-stu-id="9b0dc-261">(DBPROP_JETOLEDB_VALIDATEONSET)</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-262">Указывает, оцениваются ли правила проверки jet при наборе данных столбцов или при внесении изменений в базу данных.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-262">Indicates whether the Jet validation rules are evaluated when column data is set or when the changes are committed to the database.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9b0dc-263">По умолчанию поставщик OLE DB для Microsoft Jet открывает базы данных Microsoft Jet в режиме чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-263">By default, the OLE DB Provider for Microsoft Jet opens Microsoft Jet databases in read/write mode.</span></span> <span data-ttu-id="9b0dc-264">Чтобы открыть базу данных в режиме только для чтения, установите свойство [Mode](mode-property-ado.md) на объекте ADO **Connection** **adModeRead.**</span><span class="sxs-lookup"><span data-stu-id="9b0dc-264">To open a database in read-only mode, set the [Mode](mode-property-ado.md) property on the ADO **Connection** object to **adModeRead**.</span></span>

## <a name="command-object-usage"></a><span data-ttu-id="9b0dc-265">Использование командных объектов</span><span class="sxs-lookup"><span data-stu-id="9b0dc-265">Command Object Usage</span></span>

<span data-ttu-id="9b0dc-266">Командный текст в [объекте Command](command-object-ado.md) использует диалект Microsoft Jet SQL.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-266">Command text in the [Command](command-object-ado.md) object uses the Microsoft Jet SQL dialect.</span></span> <span data-ttu-id="9b0dc-267">В тексте команды можно указать запросы, запросы действий и имена таблиц, возвращающие строки; однако сохраненные процедуры не поддерживаются и не должны быть указаны.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-267">You can specify row-returning queries, action queries, and table names in the command text; however, stored procedures are not supported and should not be specified.</span></span>

## <a name="recordset-behavior"></a><span data-ttu-id="9b0dc-268">Поведение наборов записей</span><span class="sxs-lookup"><span data-stu-id="9b0dc-268">Recordset Behavior</span></span>

<span data-ttu-id="9b0dc-269">Двигатель базы данных Microsoft Jet не поддерживает динамические курсоры.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-269">The Microsoft Jet database engine does not support dynamic cursors.</span></span> <span data-ttu-id="9b0dc-270">Поэтому поставщик OLE DB для Microsoft Jet не поддерживает тип **курсора adLockDynamic.**</span><span class="sxs-lookup"><span data-stu-id="9b0dc-270">Therefore, the OLE DB Provider for Microsoft Jet does not support the **adLockDynamic** cursor type.</span></span> <span data-ttu-id="9b0dc-271">Когда запрашивается динамический курсор, поставщик возвращает курсор наборов ключей и сбрасывает свойство [CursorType,](cursortype-property-ado.md) чтобы указать тип возвращенного [recordset.](recordset-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="9b0dc-271">When a dynamic cursor is requested, the provider will return a keyset cursor and reset the [CursorType](cursortype-property-ado.md) property to indicate the type of [Recordset](recordset-object-ado.md) returned.</span></span> <span data-ttu-id="9b0dc-272">Кроме того, если запрашивается updatable **Recordset** **(LockType** является **adLockOptimistic,** **adLockBatchOptimistic** или **adLockPessimistic),** поставщик также возвращает курсор наборов ключей и сбрасывает свойство **CursorType.**</span><span class="sxs-lookup"><span data-stu-id="9b0dc-272">Further, if an updatable **Recordset** is requested (**LockType** is **adLockOptimistic**, **adLockBatchOptimistic**, or **adLockPessimistic**) the provider will also return a keyset cursor and reset the **CursorType** property.</span></span>

## <a name="dynamic-properties"></a><span data-ttu-id="9b0dc-273">Dynamic Properties</span><span class="sxs-lookup"><span data-stu-id="9b0dc-273">Dynamic Properties</span></span>

<span data-ttu-id="9b0dc-274">Поставщик OLE DB для Microsoft Jet вставляет несколько динамических свойств в коллекцию **свойств** незапертых объектов [Connection,](connection-object-ado.md) [Recordset](recordset-object-ado.md)и [Command.](command-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="9b0dc-274">The OLE DB Provider for Microsoft Jet inserts several dynamic properties into the **Properties** collection of the unopened [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md), and [Command](command-object-ado.md) objects.</span></span>

<span data-ttu-id="9b0dc-275">Ниже приведены перекрестные индексы имен ADO и OLE DB для каждого динамического свойства.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-275">The tables below are a cross-index of the ADO and OLE DB names for each dynamic property.</span></span> <span data-ttu-id="9b0dc-276">Ссылка программиста OLE DB относится к имени свойства ADO по термину "Описание".</span><span class="sxs-lookup"><span data-stu-id="9b0dc-276">The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description."</span></span> <span data-ttu-id="9b0dc-277">Дополнительные сведения об этих свойствах можно найти в справке программиста OLE DB.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-277">You can find more information about these properties in the OLE DB Programmer's Reference.</span></span> <span data-ttu-id="9b0dc-278">Поиск имени свойства OLE DB в Индексе или см. в приложении C: OLE DB Properties.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-278">Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span></span>

## <a name="connection-dynamic-properties"></a><span data-ttu-id="9b0dc-279">Динамические свойства подключения</span><span class="sxs-lookup"><span data-stu-id="9b0dc-279">Connection Dynamic Properties</span></span>

<span data-ttu-id="9b0dc-280">Следующие свойства добавляются в коллекцию  Свойств объекта **Connection.**</span><span class="sxs-lookup"><span data-stu-id="9b0dc-280">The following properties are added to the **Connection** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9b0dc-281">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="9b0dc-281">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="9b0dc-282">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="9b0dc-282">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-283">Активные сеансы</span><span class="sxs-lookup"><span data-stu-id="9b0dc-283">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-284">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="9b0dc-284">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-285">Asynchable Abort</span><span class="sxs-lookup"><span data-stu-id="9b0dc-285">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-286">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="9b0dc-286">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-287">Asynchable Commit</span><span class="sxs-lookup"><span data-stu-id="9b0dc-287">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-288">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="9b0dc-288">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-289">Уровни изоляции автокоммита</span><span class="sxs-lookup"><span data-stu-id="9b0dc-289">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-290">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="9b0dc-290">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-291">Расположение каталога</span><span class="sxs-lookup"><span data-stu-id="9b0dc-291">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-292">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="9b0dc-292">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-293">Термин Каталог</span><span class="sxs-lookup"><span data-stu-id="9b0dc-293">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-294">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="9b0dc-294">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-295">Определение столбцов</span><span class="sxs-lookup"><span data-stu-id="9b0dc-295">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-296">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="9b0dc-296">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-297">Текущий каталог</span><span class="sxs-lookup"><span data-stu-id="9b0dc-297">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-298">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="9b0dc-298">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-299">Источник данных</span><span class="sxs-lookup"><span data-stu-id="9b0dc-299">Data Source</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-300">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="9b0dc-300">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-301">Имя источника данных</span><span class="sxs-lookup"><span data-stu-id="9b0dc-301">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-302">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="9b0dc-302">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-303">Модель потоковой обработки объектов источника данных</span><span class="sxs-lookup"><span data-stu-id="9b0dc-303">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-304">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="9b0dc-304">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-305">Имя DBMS</span><span class="sxs-lookup"><span data-stu-id="9b0dc-305">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-306">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="9b0dc-306">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-307">Версия DBMS</span><span class="sxs-lookup"><span data-stu-id="9b0dc-307">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-308">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="9b0dc-308">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-309">Поддержка GROUP BY</span><span class="sxs-lookup"><span data-stu-id="9b0dc-309">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-310">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="9b0dc-310">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-311">Гетерогенная поддержка таблиц</span><span class="sxs-lookup"><span data-stu-id="9b0dc-311">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-312">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="9b0dc-312">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-313">Чувствительность к делу идентификатора</span><span class="sxs-lookup"><span data-stu-id="9b0dc-313">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-314">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="9b0dc-314">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-315">Уровни изоляции</span><span class="sxs-lookup"><span data-stu-id="9b0dc-315">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-316">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="9b0dc-316">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-317">Хранение изоляции</span><span class="sxs-lookup"><span data-stu-id="9b0dc-317">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-318">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="9b0dc-318">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-319">Идентификатор locale</span><span class="sxs-lookup"><span data-stu-id="9b0dc-319">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-320">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="9b0dc-320">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-321">Максимальный размер индекса</span><span class="sxs-lookup"><span data-stu-id="9b0dc-321">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-322">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="9b0dc-322">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-323">Максимальный размер строки</span><span class="sxs-lookup"><span data-stu-id="9b0dc-323">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-324">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="9b0dc-324">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-325">Максимальный размер строки включает BLOB</span><span class="sxs-lookup"><span data-stu-id="9b0dc-325">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-326">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="9b0dc-326">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-327">Максимальные таблицы в SELECT</span><span class="sxs-lookup"><span data-stu-id="9b0dc-327">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-328">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="9b0dc-328">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-329">Режим</span><span class="sxs-lookup"><span data-stu-id="9b0dc-329">Mode</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-330">DBPROP_INIT_MODE</span><span class="sxs-lookup"><span data-stu-id="9b0dc-330">DBPROP_INIT_MODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-331">Несколько наборов параметров</span><span class="sxs-lookup"><span data-stu-id="9b0dc-331">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-332">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="9b0dc-332">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-333">Несколько результатов</span><span class="sxs-lookup"><span data-stu-id="9b0dc-333">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-334">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="9b0dc-334">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-335">Несколько служба хранилища объектов</span><span class="sxs-lookup"><span data-stu-id="9b0dc-335">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-336">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="9b0dc-336">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-337">Обновление с несколькими таблицами</span><span class="sxs-lookup"><span data-stu-id="9b0dc-337">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-338">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="9b0dc-338">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-339">Порядок коллансирования NULL</span><span class="sxs-lookup"><span data-stu-id="9b0dc-339">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-340">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="9b0dc-340">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-341">NULL Concatenation Behaviour</span><span class="sxs-lookup"><span data-stu-id="9b0dc-341">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-342">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="9b0dc-342">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-343">Версия OLE DB</span><span class="sxs-lookup"><span data-stu-id="9b0dc-343">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-344">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="9b0dc-344">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-345">Поддержка объектов OLE</span><span class="sxs-lookup"><span data-stu-id="9b0dc-345">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-346">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="9b0dc-346">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-347">Поддержка open Rowset</span><span class="sxs-lookup"><span data-stu-id="9b0dc-347">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-348">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="9b0dc-348">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-349">ORDER BY Columns in Select List</span><span class="sxs-lookup"><span data-stu-id="9b0dc-349">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-350">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="9b0dc-350">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-351">Доступность параметров вывода</span><span class="sxs-lookup"><span data-stu-id="9b0dc-351">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-352">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="9b0dc-352">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-353">Pass By Ref Accessors</span><span class="sxs-lookup"><span data-stu-id="9b0dc-353">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-354">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="9b0dc-354">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-355">Password</span><span class="sxs-lookup"><span data-stu-id="9b0dc-355">Password</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-356">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="9b0dc-356">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-357">Тип сохраняемого ID</span><span class="sxs-lookup"><span data-stu-id="9b0dc-357">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-358">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="9b0dc-358">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-359">Подготовка поведения прервать</span><span class="sxs-lookup"><span data-stu-id="9b0dc-359">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-360">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="9b0dc-360">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-361">Подготовка поведения фиксации</span><span class="sxs-lookup"><span data-stu-id="9b0dc-361">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-362">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="9b0dc-362">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-363">Термин процедуры</span><span class="sxs-lookup"><span data-stu-id="9b0dc-363">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-364">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="9b0dc-364">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-365">Prompt</span><span class="sxs-lookup"><span data-stu-id="9b0dc-365">Prompt</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-366">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="9b0dc-366">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-367">Удобное имя поставщика</span><span class="sxs-lookup"><span data-stu-id="9b0dc-367">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-368">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="9b0dc-368">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-369">Имя поставщика</span><span class="sxs-lookup"><span data-stu-id="9b0dc-369">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-370">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="9b0dc-370">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-371">Версия поставщика</span><span class="sxs-lookup"><span data-stu-id="9b0dc-371">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-372">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="9b0dc-372">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-373">Read-Only источник данных</span><span class="sxs-lookup"><span data-stu-id="9b0dc-373">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-374">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="9b0dc-374">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-375">Преобразования rowset в командной строке</span><span class="sxs-lookup"><span data-stu-id="9b0dc-375">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-376">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="9b0dc-376">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-377">Термин Схемы</span><span class="sxs-lookup"><span data-stu-id="9b0dc-377">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-378">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="9b0dc-378">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-379">Использование схемы</span><span class="sxs-lookup"><span data-stu-id="9b0dc-379">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-380">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="9b0dc-380">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-381">SQL Поддержка</span><span class="sxs-lookup"><span data-stu-id="9b0dc-381">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-382">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="9b0dc-382">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-383">Структурированные служба хранилища</span><span class="sxs-lookup"><span data-stu-id="9b0dc-383">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-384">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="9b0dc-384">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-385">Поддержка subquery</span><span class="sxs-lookup"><span data-stu-id="9b0dc-385">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-386">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="9b0dc-386">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-387">Термин Таблица</span><span class="sxs-lookup"><span data-stu-id="9b0dc-387">Table Term</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-388">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="9b0dc-388">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-389">DDL транзакций</span><span class="sxs-lookup"><span data-stu-id="9b0dc-389">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-390">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="9b0dc-390">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-391">Идентификатор пользователя</span><span class="sxs-lookup"><span data-stu-id="9b0dc-391">User ID</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-392">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="9b0dc-392">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-393">имя пользователя;</span><span class="sxs-lookup"><span data-stu-id="9b0dc-393">User Name</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-394">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="9b0dc-394">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-395">Ручка окна</span><span class="sxs-lookup"><span data-stu-id="9b0dc-395">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-396">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="9b0dc-396">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a><span data-ttu-id="9b0dc-397">Динамические свойства Recordset</span><span class="sxs-lookup"><span data-stu-id="9b0dc-397">Recordset Dynamic Properties</span></span>

<span data-ttu-id="9b0dc-398">Следующие свойства добавляются в коллекцию Свойств  объекта **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="9b0dc-398">The following properties are added to the **Recordset** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9b0dc-399">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="9b0dc-399">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="9b0dc-400">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="9b0dc-400">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-401">Порядок доступа</span><span class="sxs-lookup"><span data-stu-id="9b0dc-401">Access Order</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-402">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="9b0dc-402">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-403">Append-Only Rowset</span><span class="sxs-lookup"><span data-stu-id="9b0dc-403">Append-Only Rowset</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-404">DBPROP_APPENDONLY</span><span class="sxs-lookup"><span data-stu-id="9b0dc-404">DBPROP_APPENDONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-405">Блокировка служба хранилища объектов</span><span class="sxs-lookup"><span data-stu-id="9b0dc-405">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-406">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="9b0dc-406">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-407">Тип закладок</span><span class="sxs-lookup"><span data-stu-id="9b0dc-407">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-408">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="9b0dc-408">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-409">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="9b0dc-409">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-410">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="9b0dc-410">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-411">Закладки заказать</span><span class="sxs-lookup"><span data-stu-id="9b0dc-411">Bookmarks Ordered</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-412">DBPROP_ORDEREDBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="9b0dc-412">DBPROP_ORDEREDBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-413">Отложенные столбцы кэша</span><span class="sxs-lookup"><span data-stu-id="9b0dc-413">Cache Deferred Columns</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-414">DBPROP_CACHEDEFERRED</span><span class="sxs-lookup"><span data-stu-id="9b0dc-414">DBPROP_CACHEDEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-415">Изменение вставленных строк</span><span class="sxs-lookup"><span data-stu-id="9b0dc-415">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-416">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="9b0dc-416">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-417">Привилегии столбца</span><span class="sxs-lookup"><span data-stu-id="9b0dc-417">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-418">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="9b0dc-418">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-419">Уведомление о наборе столбцов</span><span class="sxs-lookup"><span data-stu-id="9b0dc-419">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-420">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="9b0dc-420">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-421">Колонка Writable</span><span class="sxs-lookup"><span data-stu-id="9b0dc-421">Column Writable</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-422">DBPROP_MAYWRITECOLUMN</span><span class="sxs-lookup"><span data-stu-id="9b0dc-422">DBPROP_MAYWRITECOLUMN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-423">Столбец Отсрочка</span><span class="sxs-lookup"><span data-stu-id="9b0dc-423">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-424">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="9b0dc-424">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-425">Задержка служба хранилища обновлений объектов</span><span class="sxs-lookup"><span data-stu-id="9b0dc-425">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-426">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="9b0dc-426">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-427">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="9b0dc-427">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-428">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="9b0dc-428">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-429">Строки удержания</span><span class="sxs-lookup"><span data-stu-id="9b0dc-429">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-430">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="9b0dc-430">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-431">IAccessor</span><span class="sxs-lookup"><span data-stu-id="9b0dc-431">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-432">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="9b0dc-432">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-433">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="9b0dc-433">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-434">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="9b0dc-434">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-435">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="9b0dc-435">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-436">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="9b0dc-436">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-437">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="9b0dc-437">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-438">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="9b0dc-438">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-439">IConvertType</span><span class="sxs-lookup"><span data-stu-id="9b0dc-439">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-440">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="9b0dc-440">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-441">ILockBytes</span><span class="sxs-lookup"><span data-stu-id="9b0dc-441">ILockBytes</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-442">DBPROP_ILockBytes</span><span class="sxs-lookup"><span data-stu-id="9b0dc-442">DBPROP_ILockBytes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-443">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="9b0dc-443">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-444">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="9b0dc-444">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-445">IRowset</span><span class="sxs-lookup"><span data-stu-id="9b0dc-445">IRowset</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-446">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="9b0dc-446">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-447">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="9b0dc-447">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-448">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="9b0dc-448">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-449">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="9b0dc-449">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-450">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="9b0dc-450">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-451">IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="9b0dc-451">IRowsetIndex</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-452">DBPROP_IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="9b0dc-452">DBPROP_IRowsetIndex</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-453">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="9b0dc-453">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-454">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="9b0dc-454">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-455">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="9b0dc-455">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-456">DBPROP_IRowsestLocate</span><span class="sxs-lookup"><span data-stu-id="9b0dc-456">DBPROP_IRowsestLocate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-457">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="9b0dc-457">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-458">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="9b0dc-458">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-459">DBPROP_IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="9b0dc-459">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-460">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="9b0dc-460">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-461">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="9b0dc-461">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-462">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="9b0dc-462">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-463">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="9b0dc-463">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-464">IStorage</span><span class="sxs-lookup"><span data-stu-id="9b0dc-464">IStorage</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-465">DBPROP_IStorage</span><span class="sxs-lookup"><span data-stu-id="9b0dc-465">DBPROP_IStorage</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-466">IStream</span><span class="sxs-lookup"><span data-stu-id="9b0dc-466">IStream</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-467">DBPROP_IStream</span><span class="sxs-lookup"><span data-stu-id="9b0dc-467">DBPROP_IStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-468">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="9b0dc-468">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-469">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="9b0dc-469">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-470">Буквальные закладки</span><span class="sxs-lookup"><span data-stu-id="9b0dc-470">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-471">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="9b0dc-471">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-472">Удостоверение буквальных строк</span><span class="sxs-lookup"><span data-stu-id="9b0dc-472">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-473">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="9b0dc-473">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-474">Максимальные открытые строки</span><span class="sxs-lookup"><span data-stu-id="9b0dc-474">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-475">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="9b0dc-475">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-476">Максимальное количество ожидающих строк</span><span class="sxs-lookup"><span data-stu-id="9b0dc-476">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-477">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="9b0dc-477">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-478">Максимальные строки</span><span class="sxs-lookup"><span data-stu-id="9b0dc-478">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-479">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="9b0dc-479">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-480">Использование памяти</span><span class="sxs-lookup"><span data-stu-id="9b0dc-480">Memory Usage</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-481">DBPROP_MEMORYUSAGE</span><span class="sxs-lookup"><span data-stu-id="9b0dc-481">DBPROP_MEMORYUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-482">Детализация уведомлений</span><span class="sxs-lookup"><span data-stu-id="9b0dc-482">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-483">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="9b0dc-483">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-484">Этапы уведомлений</span><span class="sxs-lookup"><span data-stu-id="9b0dc-484">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-485">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="9b0dc-485">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-486">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="9b0dc-486">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-487">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="9b0dc-487">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-488">Видимые изменения других</span><span class="sxs-lookup"><span data-stu-id="9b0dc-488">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-489">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="9b0dc-489">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-490">Видимые вставки других</span><span class="sxs-lookup"><span data-stu-id="9b0dc-490">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-491">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="9b0dc-491">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-492">Собственные изменения Видимые</span><span class="sxs-lookup"><span data-stu-id="9b0dc-492">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-493">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="9b0dc-493">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-494">Собственные вставки Видимые</span><span class="sxs-lookup"><span data-stu-id="9b0dc-494">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-495">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="9b0dc-495">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-496">Сохранение на abort</span><span class="sxs-lookup"><span data-stu-id="9b0dc-496">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-497">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="9b0dc-497">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-498">Сохранение на коммит</span><span class="sxs-lookup"><span data-stu-id="9b0dc-498">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-499">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="9b0dc-499">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-500">Быстрая перезагрузка</span><span class="sxs-lookup"><span data-stu-id="9b0dc-500">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-501">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="9b0dc-501">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-502">События для повторного антуламента</span><span class="sxs-lookup"><span data-stu-id="9b0dc-502">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-503">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="9b0dc-503">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-504">Удаление удаленных строк</span><span class="sxs-lookup"><span data-stu-id="9b0dc-504">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-505">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="9b0dc-505">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-506">Отчет о нескольких изменениях</span><span class="sxs-lookup"><span data-stu-id="9b0dc-506">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-507">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="9b0dc-507">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-508">Возвращение ожидающих вставок</span><span class="sxs-lookup"><span data-stu-id="9b0dc-508">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-509">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="9b0dc-509">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-510">Уведомление об удалении строки</span><span class="sxs-lookup"><span data-stu-id="9b0dc-510">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-511">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="9b0dc-511">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-512">Уведомление о первом изменении строки</span><span class="sxs-lookup"><span data-stu-id="9b0dc-512">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-513">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="9b0dc-513">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-514">Уведомление о вставке строки</span><span class="sxs-lookup"><span data-stu-id="9b0dc-514">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-515">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="9b0dc-515">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-516">Привилегии строки</span><span class="sxs-lookup"><span data-stu-id="9b0dc-516">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-517">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="9b0dc-517">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-518">Уведомление о повторной синхронизации строк</span><span class="sxs-lookup"><span data-stu-id="9b0dc-518">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-519">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="9b0dc-519">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-520">Модель потоков строки</span><span class="sxs-lookup"><span data-stu-id="9b0dc-520">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-521">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="9b0dc-521">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-522">Уведомление об отмене строки</span><span class="sxs-lookup"><span data-stu-id="9b0dc-522">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-523">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="9b0dc-523">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-524">Уведомление об отмене строки</span><span class="sxs-lookup"><span data-stu-id="9b0dc-524">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-525">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="9b0dc-525">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-526">Уведомление об отмене строки</span><span class="sxs-lookup"><span data-stu-id="9b0dc-526">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-527">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="9b0dc-527">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-528">Уведомление об обновлении строки</span><span class="sxs-lookup"><span data-stu-id="9b0dc-528">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-529">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="9b0dc-529">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-530">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="9b0dc-530">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-531">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="9b0dc-531">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-532">Уведомление о выпуске Rowset</span><span class="sxs-lookup"><span data-stu-id="9b0dc-532">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-533">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="9b0dc-533">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-534">Прокрутите назад</span><span class="sxs-lookup"><span data-stu-id="9b0dc-534">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-535">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="9b0dc-535">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-536">Пропустить удаленные закладки</span><span class="sxs-lookup"><span data-stu-id="9b0dc-536">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-537">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="9b0dc-537">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-538">Удостоверение Strong Row</span><span class="sxs-lookup"><span data-stu-id="9b0dc-538">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-539">DBPROP_STRONGITDENTITY</span><span class="sxs-lookup"><span data-stu-id="9b0dc-539">DBPROP_STRONGITDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-540">Updatability</span><span class="sxs-lookup"><span data-stu-id="9b0dc-540">Updatability</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-541">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="9b0dc-541">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-542">Использование закладок</span><span class="sxs-lookup"><span data-stu-id="9b0dc-542">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-543">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="9b0dc-543">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a><span data-ttu-id="9b0dc-544">Командные динамические свойства</span><span class="sxs-lookup"><span data-stu-id="9b0dc-544">Command Dynamic Properties</span></span>

<span data-ttu-id="9b0dc-545">Следующие свойства добавляются в коллекцию **Свойств** объекта **Command.**</span><span class="sxs-lookup"><span data-stu-id="9b0dc-545">The following properties are added to the **Command** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9b0dc-546">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="9b0dc-546">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="9b0dc-547">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="9b0dc-547">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-548">Порядок доступа</span><span class="sxs-lookup"><span data-stu-id="9b0dc-548">Access Order</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-549">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="9b0dc-549">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-550">Append-Only Rowset</span><span class="sxs-lookup"><span data-stu-id="9b0dc-550">Append-Only Rowset</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-551">DBPROP_APPENDONLY</span><span class="sxs-lookup"><span data-stu-id="9b0dc-551">DBPROP_APPENDONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-552">Блокировка служба хранилища объектов</span><span class="sxs-lookup"><span data-stu-id="9b0dc-552">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-553">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="9b0dc-553">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-554">Тип закладок</span><span class="sxs-lookup"><span data-stu-id="9b0dc-554">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-555">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="9b0dc-555">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-556">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="9b0dc-556">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-557">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="9b0dc-557">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-558">Изменение вставленных строк</span><span class="sxs-lookup"><span data-stu-id="9b0dc-558">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-559">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="9b0dc-559">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-560">Привилегии столбца</span><span class="sxs-lookup"><span data-stu-id="9b0dc-560">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-561">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="9b0dc-561">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-562">Уведомление о наборе столбцов</span><span class="sxs-lookup"><span data-stu-id="9b0dc-562">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-563">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="9b0dc-563">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-564">Столбец Отсрочка</span><span class="sxs-lookup"><span data-stu-id="9b0dc-564">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-565">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="9b0dc-565">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-566">Задержка служба хранилища обновлений объектов</span><span class="sxs-lookup"><span data-stu-id="9b0dc-566">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-567">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="9b0dc-567">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-568">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="9b0dc-568">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-569">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="9b0dc-569">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-570">Строки удержания</span><span class="sxs-lookup"><span data-stu-id="9b0dc-570">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-571">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="9b0dc-571">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-572">IAccessor</span><span class="sxs-lookup"><span data-stu-id="9b0dc-572">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-573">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="9b0dc-573">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-574">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="9b0dc-574">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-575">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="9b0dc-575">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-576">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="9b0dc-576">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-577">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="9b0dc-577">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-578">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="9b0dc-578">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-579">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="9b0dc-579">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-580">IConvertType</span><span class="sxs-lookup"><span data-stu-id="9b0dc-580">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-581">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="9b0dc-581">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-582">ILockBytes</span><span class="sxs-lookup"><span data-stu-id="9b0dc-582">ILockBytes</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-583">DBPROP_ILockBytes</span><span class="sxs-lookup"><span data-stu-id="9b0dc-583">DBPROP_ILockBytes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-584">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="9b0dc-584">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-585">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="9b0dc-585">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-586">IRowset</span><span class="sxs-lookup"><span data-stu-id="9b0dc-586">IRowset</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-587">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="9b0dc-587">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-588">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="9b0dc-588">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-589">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="9b0dc-589">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-590">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="9b0dc-590">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-591">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="9b0dc-591">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-592">IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="9b0dc-592">IRowsetIndex</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-593">DBPROP_IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="9b0dc-593">DBPROP_IRowsetIndex</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-594">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="9b0dc-594">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-595">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="9b0dc-595">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-596">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="9b0dc-596">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-597">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="9b0dc-597">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-598">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="9b0dc-598">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-599">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="9b0dc-599">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-600">DBPROP_IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="9b0dc-600">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-601">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="9b0dc-601">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-602">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="9b0dc-602">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-603">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="9b0dc-603">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-604">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="9b0dc-604">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-605">IStorage</span><span class="sxs-lookup"><span data-stu-id="9b0dc-605">IStorage</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-606">DBPROP_IStorage</span><span class="sxs-lookup"><span data-stu-id="9b0dc-606">DBPROP_IStorage</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-607">IStream</span><span class="sxs-lookup"><span data-stu-id="9b0dc-607">IStream</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-608">DBPROP_IStream</span><span class="sxs-lookup"><span data-stu-id="9b0dc-608">DBPROP_IStream</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-609">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="9b0dc-609">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-610">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="9b0dc-610">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-611">Буквальные закладки</span><span class="sxs-lookup"><span data-stu-id="9b0dc-611">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-612">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="9b0dc-612">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-613">Удостоверение буквальных строк</span><span class="sxs-lookup"><span data-stu-id="9b0dc-613">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-614">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="9b0dc-614">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-615">Режим блокировки</span><span class="sxs-lookup"><span data-stu-id="9b0dc-615">Lock Mode</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-616">DBPROP_LOCKMODE</span><span class="sxs-lookup"><span data-stu-id="9b0dc-616">DBPROP_LOCKMODE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-617">Максимальные открытые строки</span><span class="sxs-lookup"><span data-stu-id="9b0dc-617">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-618">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="9b0dc-618">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-619">Максимальное количество ожидающих строк</span><span class="sxs-lookup"><span data-stu-id="9b0dc-619">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-620">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="9b0dc-620">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-621">Максимальные строки</span><span class="sxs-lookup"><span data-stu-id="9b0dc-621">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-622">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="9b0dc-622">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-623">Детализация уведомлений</span><span class="sxs-lookup"><span data-stu-id="9b0dc-623">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-624">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="9b0dc-624">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-625">Этапы уведомлений</span><span class="sxs-lookup"><span data-stu-id="9b0dc-625">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-626">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="9b0dc-626">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-627">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="9b0dc-627">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-628">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="9b0dc-628">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-629">Видимые изменения других</span><span class="sxs-lookup"><span data-stu-id="9b0dc-629">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-630">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="9b0dc-630">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-631">Видимые вставки других</span><span class="sxs-lookup"><span data-stu-id="9b0dc-631">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-632">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="9b0dc-632">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-633">Собственные изменения Видимые</span><span class="sxs-lookup"><span data-stu-id="9b0dc-633">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-634">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="9b0dc-634">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-635">Собственные вставки Видимые</span><span class="sxs-lookup"><span data-stu-id="9b0dc-635">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-636">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="9b0dc-636">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-637">Сохранение на abort</span><span class="sxs-lookup"><span data-stu-id="9b0dc-637">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-638">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="9b0dc-638">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-639">Сохранение на коммит</span><span class="sxs-lookup"><span data-stu-id="9b0dc-639">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-640">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="9b0dc-640">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-641">Быстрая перезагрузка</span><span class="sxs-lookup"><span data-stu-id="9b0dc-641">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-642">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="9b0dc-642">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-643">События для повторного антуламента</span><span class="sxs-lookup"><span data-stu-id="9b0dc-643">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-644">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="9b0dc-644">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-645">Удаление удаленных строк</span><span class="sxs-lookup"><span data-stu-id="9b0dc-645">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-646">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="9b0dc-646">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-647">Отчет о нескольких изменениях</span><span class="sxs-lookup"><span data-stu-id="9b0dc-647">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-648">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="9b0dc-648">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-649">Возвращение ожидающих вставок</span><span class="sxs-lookup"><span data-stu-id="9b0dc-649">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-650">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="9b0dc-650">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-651">Уведомление об удалении строки</span><span class="sxs-lookup"><span data-stu-id="9b0dc-651">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-652">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="9b0dc-652">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-653">Уведомление о первом изменении строки</span><span class="sxs-lookup"><span data-stu-id="9b0dc-653">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-654">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="9b0dc-654">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-655">Уведомление о вставке строки</span><span class="sxs-lookup"><span data-stu-id="9b0dc-655">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-656">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="9b0dc-656">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-657">Привилегии строки</span><span class="sxs-lookup"><span data-stu-id="9b0dc-657">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-658">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="9b0dc-658">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-659">Уведомление о повторной синхронизации строк</span><span class="sxs-lookup"><span data-stu-id="9b0dc-659">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-660">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="9b0dc-660">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-661">Модель потоков строки</span><span class="sxs-lookup"><span data-stu-id="9b0dc-661">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-662">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="9b0dc-662">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-663">Уведомление об отмене строки</span><span class="sxs-lookup"><span data-stu-id="9b0dc-663">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-664">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="9b0dc-664">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-665">Уведомление об отмене строки</span><span class="sxs-lookup"><span data-stu-id="9b0dc-665">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-666">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="9b0dc-666">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-667">Уведомление об отмене строки</span><span class="sxs-lookup"><span data-stu-id="9b0dc-667">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-668">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="9b0dc-668">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-669">Уведомление об обновлении строки</span><span class="sxs-lookup"><span data-stu-id="9b0dc-669">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-670">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="9b0dc-670">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-671">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="9b0dc-671">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-672">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="9b0dc-672">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-673">Уведомление о выпуске Rowset</span><span class="sxs-lookup"><span data-stu-id="9b0dc-673">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-674">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="9b0dc-674">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-675">Прокрутите назад</span><span class="sxs-lookup"><span data-stu-id="9b0dc-675">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-676">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="9b0dc-676">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-677">Данные сервера на вставке</span><span class="sxs-lookup"><span data-stu-id="9b0dc-677">Server Data on Insert</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-678">DBPROP_SERVERDATAONINSERT</span><span class="sxs-lookup"><span data-stu-id="9b0dc-678">DBPROP_SERVERDATAONINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-679">Пропустить удаленные закладки</span><span class="sxs-lookup"><span data-stu-id="9b0dc-679">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-680">DBPROP_BOOKMARKSKIP</span><span class="sxs-lookup"><span data-stu-id="9b0dc-680">DBPROP_BOOKMARKSKIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-681">Удостоверение Strong Row</span><span class="sxs-lookup"><span data-stu-id="9b0dc-681">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-682">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="9b0dc-682">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b0dc-683">Updatability</span><span class="sxs-lookup"><span data-stu-id="9b0dc-683">Updatability</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-684">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="9b0dc-684">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b0dc-685">Использование закладок</span><span class="sxs-lookup"><span data-stu-id="9b0dc-685">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="9b0dc-686">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="9b0dc-686">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="9b0dc-687">См. также</span><span class="sxs-lookup"><span data-stu-id="9b0dc-687">See also</span></span>

<span data-ttu-id="9b0dc-688">Для получения конкретных сведений о реализации и функциональных сведений о поставщике OLE DB для Microsoft Jet обратитесь к поставщику OLE DB для документации Microsoft Jet в SDK MDAC.</span><span class="sxs-lookup"><span data-stu-id="9b0dc-688">For specific implementation details and functional information about the OLE DB Provider for Microsoft Jet, consult the OLE DB Provider for Microsoft Jet documentation in the MDAC SDK.</span></span>

