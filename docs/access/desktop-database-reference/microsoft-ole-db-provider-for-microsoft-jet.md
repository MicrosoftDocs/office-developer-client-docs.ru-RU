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
# <a name="microsoft-ole-db-provider-for-microsoft-jet"></a><span data-ttu-id="4e1ec-102">Поставщик Microsoft OLE DB для Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="4e1ec-102">Microsoft OLE DB Provider for Microsoft Jet</span></span>

<span data-ttu-id="4e1ec-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4e1ec-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4e1ec-104">Поставщик OLE DB для Microsoft Jet позволяет ADO получать доступ к базам данных Microsoft Jet.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-104">The OLE DB Provider for Microsoft Jet allows ADO to access Microsoft Jet databases.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="4e1ec-105">Параметры строки подключения</span><span class="sxs-lookup"><span data-stu-id="4e1ec-105">Connection String Parameters</span></span>

<span data-ttu-id="4e1ec-106">Чтобы подключиться к поставщику, присвойте аргументу *provider* свойства [ConnectionString](connectionstring-property-ado.md) значение:</span><span class="sxs-lookup"><span data-stu-id="4e1ec-106">To connect to this provider, set the *Provider* argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```vb 
 
Microsoft.Jet.OLEDB.4.0 
```

<span data-ttu-id="4e1ec-107">Считывание свойства [provider](provider-property-ado.md) также возвратит эту строку.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-107">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="4e1ec-108">Типичная строка подключения</span><span class="sxs-lookup"><span data-stu-id="4e1ec-108">Typical Connection String</span></span>

<span data-ttu-id="4e1ec-109">Типичная строка подключения для этого поставщика:</span><span class="sxs-lookup"><span data-stu-id="4e1ec-109">A typical connection string for this provider is:</span></span>

```vb 
 
"Provider=Microsoft.Jet.OLEDB.4.0;Data Source=databaseName;User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="4e1ec-110">Строка состоит из следующих ключевых слов:</span><span class="sxs-lookup"><span data-stu-id="4e1ec-110">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4e1ec-111">Ключевое слово</span><span class="sxs-lookup"><span data-stu-id="4e1ec-111">Keyword</span></span></p></th>
<th><p><span data-ttu-id="4e1ec-112">Описание</span><span class="sxs-lookup"><span data-stu-id="4e1ec-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-113"><strong>Поставщик</strong></span><span class="sxs-lookup"><span data-stu-id="4e1ec-113"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="4e1ec-114">Указывает поставщика OLE DB для Microsoft Jet.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-114">Specifies the OLE DB Provider for Microsoft Jet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-115"><strong>Источник данных</strong></span><span class="sxs-lookup"><span data-stu-id="4e1ec-115"><strong>Data Source</strong></span></span></p></td>
<td><p><span data-ttu-id="4e1ec-116">Указывает путь к базе данных и имя файла (например, К:\норсвинд.МДБ).</span><span class="sxs-lookup"><span data-stu-id="4e1ec-116">Specifies the database path and file name (for example, c:\Northwind.mdb).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-117"><strong>Идентификатор пользователя</strong></span><span class="sxs-lookup"><span data-stu-id="4e1ec-117"><strong>User ID</strong></span></span></p></td>
<td><p><span data-ttu-id="4e1ec-118">Задает имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-118">Specifies the user name.</span></span> <span data-ttu-id="4e1ec-119">Если это ключевое слово не указано, по умолчанию используется строка, &quot;admin&quot;.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-119">If this keyword is not specified, the string, &quot;admin&quot;, is used by default.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-120"><strong>Password</strong></span><span class="sxs-lookup"><span data-stu-id="4e1ec-120"><strong>Password</strong></span></span></p></td>
<td><p><span data-ttu-id="4e1ec-121">Указывает пароль пользователя.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-121">Specifies the user password.</span></span> <span data-ttu-id="4e1ec-122">Если это ключевое слово не указано, по умолчанию&quot;&quot;используется пустая строка ().</span><span class="sxs-lookup"><span data-stu-id="4e1ec-122">If this keyword is not specified, the empty string (&quot;&quot;), is used by default.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-connection-parameters"></a><span data-ttu-id="4e1ec-123">Параметры подключения, зависящие от поставщика</span><span class="sxs-lookup"><span data-stu-id="4e1ec-123">Provider-Specific Connection Parameters</span></span>

<span data-ttu-id="4e1ec-124">Поставщик OLE DB для Microsoft Jet поддерживает несколько динамических свойств, относящихся к определенным поставщикам, в дополнение к тем, которые определены в ADO.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-124">The OLE DB Provider for Microsoft Jet supports several provider-specific dynamic properties in addition to those defined by ADO.</span></span> <span data-ttu-id="4e1ec-125">Как и во всех остальных параметрах **подключения** , их можно задать с помощью коллекции **свойств** объекта **Connection** или в строке подключения.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-125">As with all other **Connection** parameters, they can be set via the **Connection** object's **Properties** collection or as part of the connection string.</span></span>

<span data-ttu-id="4e1ec-126">В приведенной ниже таблице указаны эти свойства с соответствующим именем свойства OLE DB в круглых скобках.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-126">The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4e1ec-127">Параметр</span><span class="sxs-lookup"><span data-stu-id="4e1ec-127">Parameter</span></span></p></th>
<th><p><span data-ttu-id="4e1ec-128">Описание</span><span class="sxs-lookup"><span data-stu-id="4e1ec-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-129">Jet OLEDB: сжатие освобожденного объема дискового пространства</span><span class="sxs-lookup"><span data-stu-id="4e1ec-129">Jet OLEDB:Compact Reclaimed Space Amount</span></span><br />
<span data-ttu-id="4e1ec-130">(ДБПРОП_ЖЕТОЛЕДБ_КОМПАКТФРИСПАЦЕСИЗЕ)</span><span class="sxs-lookup"><span data-stu-id="4e1ec-130">(DBPROP_JETOLEDB_COMPACTFREESPACESIZE)</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-131">Указывает оценку объема пространства в байтах, которое может быть восстановлено с помощью сжатия базы данных.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-131">Indicates an estimate of the amount of space, in bytes, that can be reclaimed by compacting the database.</span></span> <span data-ttu-id="4e1ec-132">Это значение является допустимым только после установки подключения к базе данных.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-132">This value is only valid after a database connection has been established.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-133">Jet OLEDB: Управление подключением</span><span class="sxs-lookup"><span data-stu-id="4e1ec-133">Jet OLEDB:Connection Control</span></span><br />
<span data-ttu-id="4e1ec-134">(ДБПРОП_ЖЕТОЛЕДБ_КОННЕКТИОНКОНТРОЛ)</span><span class="sxs-lookup"><span data-stu-id="4e1ec-134">(DBPROP_JETOLEDB_CONNECTIONCONTROL)</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-135">Указывает, могут ли пользователи подключаться к базе данных.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-135">Indicates whether users can connect to the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-136">Jet OLEDB: Создание системной базы данных</span><span class="sxs-lookup"><span data-stu-id="4e1ec-136">Jet OLEDB:Create System Database</span></span><br />
<span data-ttu-id="4e1ec-137">(ДБПРОП_ЖЕТОЛЕДБ_КРЕАТЕСИСТЕМДАТАБАСЕ)</span><span class="sxs-lookup"><span data-stu-id="4e1ec-137">(DBPROP_JETOLEDB_CREATESYSTEMDATABASE)</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-138">Указывает, следует ли создавать системную базу данных при создании нового источника данных.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-138">Indicates whether a system database should be created when creating a new data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-139">Jet OLEDB: режим блокировки базы данных</span><span class="sxs-lookup"><span data-stu-id="4e1ec-139">Jet OLEDB:Database Locking Mode</span></span><br />
<span data-ttu-id="4e1ec-140">(ДБПРОП_ЖЕТОЛЕДБ_ДАТАБАСЕЛОККМОДЕ)</span><span class="sxs-lookup"><span data-stu-id="4e1ec-140">(DBPROP_JETOLEDB_DATABASELOCKMODE)</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-141">Указывает режим блокировки для этой базы данных.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-141">Indicates the locking mode for this database.</span></span> <span data-ttu-id="4e1ec-142">Первый пользователь, который открывает базу данных, определяет режим, используемый при открытии базы данных.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-142">The first user to open the database determines the mode used while the database is open.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-143">Jet OLEDB: пароль базы данных</span><span class="sxs-lookup"><span data-stu-id="4e1ec-143">Jet OLEDB:Database Password</span></span><br />
<span data-ttu-id="4e1ec-144">(ДБПРОП_ЖЕТОЛЕДБ_ДАТАБАСЕПАССВОРД)</span><span class="sxs-lookup"><span data-stu-id="4e1ec-144">(DBPROP_JETOLEDB_DATABASEPASSWORD)</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-145">Указывает пароль базы данных.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-145">Indicates the database password.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-146">Jet OLEDB: не копировать языковой стандарт в Compact</span><span class="sxs-lookup"><span data-stu-id="4e1ec-146">Jet OLEDB:Don't Copy Locale on Compact</span></span><br />
<span data-ttu-id="4e1ec-147">(ДБПРОП_ЖЕТОЛЕДБ_КОМПАКТ_ДОНТКОПИЛОКАЛЕ)</span><span class="sxs-lookup"><span data-stu-id="4e1ec-147">(DBPROP_JETOLEDB_COMPACT_DONTCOPYLOCALE)</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-148">Указывает, следует ли Jet копировать информацию о языковых стандартах при сжатии базы данных.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-148">Indicates whether Jet should copy locale information when compacting a database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-149">Jet OLEDB: шифрование базы данных</span><span class="sxs-lookup"><span data-stu-id="4e1ec-149">Jet OLEDB:Encrypt Database</span></span><br />
<span data-ttu-id="4e1ec-150">(ДБПРОП_ЖЕТОЛЕДБ_ЕНКРИПТДАТАБАСЕ)</span><span class="sxs-lookup"><span data-stu-id="4e1ec-150">(DBPROP_JETOLEDB_ENCRYPTDATABASE)</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-151">Указывает, следует ли шифровать сжатую базу данных.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-151">Indicates whether a compacted database should be encrypted.</span></span> <span data-ttu-id="4e1ec-152">Если это свойство не задано, сжатая база данных будет зашифрована, если исходная база данных также была зашифрована.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-152">If this property is not set, the compacted database will be encrypted if the original database was also encrypted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-153">Jet OLEDB: тип модуля</span><span class="sxs-lookup"><span data-stu-id="4e1ec-153">Jet OLEDB:Engine Type</span></span><br />
<span data-ttu-id="4e1ec-154">(ДБПРОП_ЖЕТОЛЕДБ_ЕНГИНЕ)</span><span class="sxs-lookup"><span data-stu-id="4e1ec-154">(DBPROP_JETOLEDB_ENGINE)</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-155">Указывает подсистему хранилища, используемую для доступа к текущему хранилищу данных.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-155">Indicates the storage engine used to access the current data store.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-156">Jet OLEDB: исключительная асинхронная задержка</span><span class="sxs-lookup"><span data-stu-id="4e1ec-156">Jet OLEDB:Exclusive Async Delay</span></span><br />
<span data-ttu-id="4e1ec-157">(ДБПРОП_ЖЕТОЛЕДБ_ЕКСКЛУСИВЕАСИНКДЕЛАЙ)</span><span class="sxs-lookup"><span data-stu-id="4e1ec-157">(DBPROP_JETOLEDB_EXCLUSIVEASYNCDELAY)</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-158">Указывает максимальное время (в миллисекундах), в течение которого Jet может задерживать асинхронные операции записи на диск, когда база данных открыта в монопольном режиме.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-158">Indicates the maximum length of time, in milliseconds, that Jet can delay asynchronous writes to disk when the database is opened exclusively.</span></span> <span data-ttu-id="4e1ec-159">Это свойство игнорируется, если <strong>Jet OLEDB: время ожидания транзакции на сброс</strong> устанавливается равным 0.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-159">This property is ignored unless <strong>Jet OLEDB:Flush Transaction Timeout</strong> is set to 0.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-160">Jet OLEDB: время ожидания очистки транзакций</span><span class="sxs-lookup"><span data-stu-id="4e1ec-160">Jet OLEDB:Flush Transaction Timeout</span></span><br />
<span data-ttu-id="4e1ec-161">(ДБПРОП_ЖЕТОЛЕДБ_ФЛУШТРАНСАКТИОНТИМЕАУТ)</span><span class="sxs-lookup"><span data-stu-id="4e1ec-161">(DBPROP_JETOLEDB_FLUSHTRANSACTIONTIMEOUT)</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-162">Указывает время ожидания, в течение которого данные, хранящиеся в кэше для асинхронной записи, фактически записываются на диск.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-162">Indicates the amount of time to wait before data stored in a cache for asynchronous writing is actually written to disk.</span></span> <span data-ttu-id="4e1ec-163">Этот параметр переопределяет значения для <strong>Jet OLEDB: Общая асинхронНая задержка</strong> и <strong>Jet OLEDB: исключительнАя асинхронная задержка</strong>.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-163">This setting overrides the values for <strong>Jet OLEDB:Shared Async Delay</strong> and <strong>Jet OLEDB:Exclusive Async Delay</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-164">Jet OLEDB: глобальные массовые транзакции</span><span class="sxs-lookup"><span data-stu-id="4e1ec-164">Jet OLEDB:Global Bulk Transactions</span></span><br />
<span data-ttu-id="4e1ec-165">(ДБПРОП_ЖЕТОЛЕДБ_ГЛОБАЛБУЛКНОТРАНСАКТИОНС)</span><span class="sxs-lookup"><span data-stu-id="4e1ec-165">(DBPROP_JETOLEDB_GLOBALBULKNOTRANSACTIONS)</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-166">Указывает, являются ли транзакции массовых транзакций SQL транзакционными.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-166">Indicates whether SQL bulk transactions are transacted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-167">Jet OLEDB: глобальные частичные массовые операции</span><span class="sxs-lookup"><span data-stu-id="4e1ec-167">Jet OLEDB:Global Partial Bulk Ops</span></span><br />
<span data-ttu-id="4e1ec-168">(ДБПРОП_ЖЕТОЛЕДБ_ГЛОБАЛБУЛКПАРТИАЛ)</span><span class="sxs-lookup"><span data-stu-id="4e1ec-168">(DBPROP_JETOLEDB_GLOBALBULKPARTIAL)</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-169">Указывает пароль, используемый для открытия базы данных.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-169">Indicates the password used to open the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-170">Jet OLEDB: неЯвная синхронизация фиксации</span><span class="sxs-lookup"><span data-stu-id="4e1ec-170">Jet OLEDB:Implicit Commit Sync</span></span><br />
<span data-ttu-id="4e1ec-171">(ДБПРОП_ЖЕТОЛЕДБ_ИМПЛИЦИТКОММИТСИНК)</span><span class="sxs-lookup"><span data-stu-id="4e1ec-171">(DBPROP_JETOLEDB_IMPLICITCOMMITSYNC)</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-172">Указывает, записываются ли изменения, внесенные во внутренние неявные транзакции, в синхронном или асинхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-172">Indicates whether changes made in internal implicit transactions are written in synchronous or asynchronous mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-173">Jet OLEDB: задержка блокировки</span><span class="sxs-lookup"><span data-stu-id="4e1ec-173">Jet OLEDB:Lock Delay</span></span><br />
<span data-ttu-id="4e1ec-174">(ДБПРОП_ЖЕТОЛЕДБ_ЛОККДЕЛАЙ)</span><span class="sxs-lookup"><span data-stu-id="4e1ec-174">(DBPROP_JETOLEDB_LOCKDELAY)</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-175">Указывает время ожидания в миллисекундах перед попыткой получить блокировку после сбоя предыдущей попытки.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-175">Indicates the number of milliseconds to wait before attempting to acquire a lock after a previous attempt has failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-176">Jet OLEDB: Блокировка повторных поПыток</span><span class="sxs-lookup"><span data-stu-id="4e1ec-176">Jet OLEDB:Lock Retry</span></span><br />
<span data-ttu-id="4e1ec-177">(ДБПРОП_ЖЕТОЛЕДБ_ЛОККРЕТРИ)</span><span class="sxs-lookup"><span data-stu-id="4e1ec-177">(DBPROP_JETOLEDB_LOCKRETRY)</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-178">Указывает, сколько раз попытка доступа к заблокированной странице повторяется.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-178">Indicates how many times an attempt to access a locked page is repeated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-179">Jet OLEDB: максимальный размер буфера</span><span class="sxs-lookup"><span data-stu-id="4e1ec-179">Jet OLEDB:Max Buffer Size</span></span><br />
<span data-ttu-id="4e1ec-180">(ДБПРОП_ЖЕТОЛЕДБ_МАКСБУФФЕРСИЗЕ)</span><span class="sxs-lookup"><span data-stu-id="4e1ec-180">(DBPROP_JETOLEDB_MAXBUFFERSIZE)</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-181">Указывает максимальный объем памяти (в килобайтах), который может использоваться Jet перед запуском очистки изменений на диске.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-181">Indicates the maximum amount of memory, in kilobytes, Jet can use before it starts flushing changes to disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-182">Jet OLEDB: максимальное число блокировок на файл</span><span class="sxs-lookup"><span data-stu-id="4e1ec-182">Jet OLEDB:Max Locks Per File</span></span><br />
<span data-ttu-id="4e1ec-183">(ДБПРОП_ЖЕТОЛЕДБ_МАКСЛОККСПЕРФИЛЕ)</span><span class="sxs-lookup"><span data-stu-id="4e1ec-183">(DBPROP_JETOLEDB_MAXLOCKSPERFILE)</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-184">Указывает максимальное число блокировок базы данных, которые Jet может разместить в базе данных.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-184">Indicates the maximum number of locks Jet can place on a database.</span></span> <span data-ttu-id="4e1ec-185">Значение по умолчанию — 9500.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-185">The default value is 9500.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-186">Jet OLEDB: новый пароль базы данных</span><span class="sxs-lookup"><span data-stu-id="4e1ec-186">Jet OLEDB:New Database Password</span></span><br />
<span data-ttu-id="4e1ec-187">(ДБПРОП_ЖЕТОЛЕДБ_НЕВДАТАБАСЕПАССВОРД)</span><span class="sxs-lookup"><span data-stu-id="4e1ec-187">(DBPROP_JETOLEDB_NEWDATABASEPASSWORD)</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-188">Указывает новый пароль, который необходимо задать для этой базы данных.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-188">Indicates the new password to be set for this database.</span></span> <span data-ttu-id="4e1ec-189">Старый пароль хранится в <strong>Jet OLEDB: пароль базы данных</strong>.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-189">The old password is stored in <strong>Jet OLEDB:Database Password</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-190">Jet OLEDB: время ожидания команды ODBC</span><span class="sxs-lookup"><span data-stu-id="4e1ec-190">Jet OLEDB:ODBC Command Time Out</span></span><br />
<span data-ttu-id="4e1ec-191">(ДБПРОП_ЖЕТОЛЕДБ_ОДБККОММАНДТИМЕАУТ)</span><span class="sxs-lookup"><span data-stu-id="4e1ec-191">(DBPROP_JETOLEDB_ODBCCOMMANDTIMEOUT)</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-192">Указывает количество миллисекунд, по истечении которого удаленный запрос ODBC из Jet будет истечет.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-192">Indicates the number of milliseconds before a remote ODBC query from Jet will timeout.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-193">Jet OLEDB: Блокировка страниц для блокировки таблицы</span><span class="sxs-lookup"><span data-stu-id="4e1ec-193">Jet OLEDB:Page Locks to Table Lock</span></span><br />
<span data-ttu-id="4e1ec-194">(ДБПРОП_ЖЕТОЛЕДБ_ПАЖЕЛОККСТОТАБЛЕЛОКК)</span><span class="sxs-lookup"><span data-stu-id="4e1ec-194">(DBPROP_JETOLEDB_PAGELOCKSTOTABLELOCK)</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-195">Указывает, сколько страниц необходимо заблокировать в транзакции, прежде чем Jet пытается превратить блокировку в блокировку таблицы.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-195">Indicates how many pages need to be locked within a transaction before Jet attempts to promote the lock to a table lock.</span></span> <span data-ttu-id="4e1ec-196">Если это значение равно 0, блокировка никогда не будет повышена.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-196">If this value is 0, then the lock is never promoted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-197">Jet OLEDB: время ожидания страницы</span><span class="sxs-lookup"><span data-stu-id="4e1ec-197">Jet OLEDB:Page Timeout</span></span><br />
<span data-ttu-id="4e1ec-198">(ДБПРОП_ЖЕТОЛЕДБ_ПАЖЕТИМЕАУТ)</span><span class="sxs-lookup"><span data-stu-id="4e1ec-198">(DBPROP_JETOLEDB_PAGETIMEOUT)</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-199">Указывает, что время ожидания Jet будет проверяться на наличие устаревших данных в файле базы данных в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-199">Indicates the number of milliseconds Jet will wait before checking to see if its cache is out of date with the database file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-200">Jet OLEDB: повторное переработка страниц с длинными значениями</span><span class="sxs-lookup"><span data-stu-id="4e1ec-200">Jet OLEDB:Recycle Long-Valued Pages</span></span><br />
<span data-ttu-id="4e1ec-201">(ДБПРОП_ЖЕТОЛЕДБ_РЕЦИКЛЕЛОНГВАЛУЕПАЖЕС)</span><span class="sxs-lookup"><span data-stu-id="4e1ec-201">(DBPROP_JETOLEDB_RECYCLELONGVALUEPAGES)</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-202">Указывает, следует ли использовать Jet для принудительного восстановления страниц BLOB при их освобождении.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-202">Indicates whether Jet should aggressively try to reclaim BLOB pages when they are freed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-203">Jet OLEDB: путь в реестре</span><span class="sxs-lookup"><span data-stu-id="4e1ec-203">Jet OLEDB:Registry Path</span></span><br />
<span data-ttu-id="4e1ec-204">(ДБПРОП_ЖЕТОЛЕДБ_РЕГПАС)</span><span class="sxs-lookup"><span data-stu-id="4e1ec-204">(DBPROP_JETOLEDB_REGPATH)</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-205">Указывает раздел реестра Windows, который содержит значения для ядра базы данных Jet.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-205">Indicates the Windows registry key that contains values for the Jet database engine.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-206">Jet OLEDB: Reset ISAM stats</span><span class="sxs-lookup"><span data-stu-id="4e1ec-206">Jet OLEDB:Reset ISAM Stats</span></span><br />
<span data-ttu-id="4e1ec-207">(ДБПРОП_ЖЕТОЛЕДБ_РЕСЕТИСАМСТАТС)</span><span class="sxs-lookup"><span data-stu-id="4e1ec-207">(DBPROP_JETOLEDB_RESETISAMSTATS)</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-208">Указывает, должен ли дбсчема_жетоледб_исамстатс <strong>набор записей</strong> схемы сбрасывать счетчики производительности после возврата сведений о производительности.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-208">Indicates whether the schema <strong>Recordset</strong> DBSCHEMA_JETOLEDB_ISAMSTATS should reset its performance counters after returning performance information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-209">Jet OLEDB: асинхронная асинхронная задержка</span><span class="sxs-lookup"><span data-stu-id="4e1ec-209">Jet OLEDB:Shared Async Delay</span></span><br />
<span data-ttu-id="4e1ec-210">(ДБПРОП_ЖЕТОЛЕДБ_ШАРЕДАСИНКДЕЛАЙ)</span><span class="sxs-lookup"><span data-stu-id="4e1ec-210">(DBPROP_JETOLEDB_SHAREDASYNCDELAY)</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-211">Указывает максимальное время (в миллисекундах), в течение которого Jet может задерживать асинхронные операции записи на диск при открытии базы данных в режиме с несколькими пользователями.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-211">Indicates the maximum amount of time, in milliseconds, Jet can delay asynchronous writes to disk when the database is opened in multi-user mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-212">Jet OLEDB: системная база данных</span><span class="sxs-lookup"><span data-stu-id="4e1ec-212">Jet OLEDB:System Database</span></span><br />
<span data-ttu-id="4e1ec-213">(ДБПРОП_ЖЕТОЛЕДБ_СИСДБПАС)</span><span class="sxs-lookup"><span data-stu-id="4e1ec-213">(DBPROP_JETOLEDB_SYSDBPATH)</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-214">Указывает путь и имя файла для файла сведений о рабочей группе (системная база данных).</span><span class="sxs-lookup"><span data-stu-id="4e1ec-214">Indicates the path and file name for the workgroup information file (system database).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-215">Jet OLEDB: режим фиксации транзакции</span><span class="sxs-lookup"><span data-stu-id="4e1ec-215">Jet OLEDB:Transaction Commit Mode</span></span><br />
<span data-ttu-id="4e1ec-216">(ДБПРОП_ЖЕТОЛЕДБ_ТКСНКОММИТМОДЕ)</span><span class="sxs-lookup"><span data-stu-id="4e1ec-216">(DBPROP_JETOLEDB_TXNCOMMITMODE)</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-217">Указывает, записывает ли Jet данные на диск синхронно или асинхронно при фиксации транзакции.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-217">Indicates whether Jet writes data to disk synchronously or asynchronously when a transaction is committed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-218">Jet OLEDB: Синхронизация с сохранением пользователей</span><span class="sxs-lookup"><span data-stu-id="4e1ec-218">Jet OLEDB:User Commit Sync</span></span><br />
<span data-ttu-id="4e1ec-219">(ДБПРОП_ЖЕТОЛЕДБ_УСЕРКОММИТСИНК)</span><span class="sxs-lookup"><span data-stu-id="4e1ec-219">(DBPROP_JETOLEDB_USERCOMMITSYNC)</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-220">Указывает, записываются ли изменения, внесенные в транзакции, в синхронном или асинхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-220">Indicates whether changes made in transactions are written in synchronous or asynchronous mode.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-recordset-and-command-properties"></a><span data-ttu-id="4e1ec-221">Специфические для поставщика наборы записей и свойства команд</span><span class="sxs-lookup"><span data-stu-id="4e1ec-221">Provider-Specific Recordset and Command Properties</span></span>

<span data-ttu-id="4e1ec-222">Поставщик Jet также поддерживает несколько специфических для конкретного поставщика **наборов записей** и свойств **команды** .</span><span class="sxs-lookup"><span data-stu-id="4e1ec-222">The Jet provider also supports several provider-specific **Recordset** and **Command** properties.</span></span> <span data-ttu-id="4e1ec-223">Доступ к этим свойствам и их настройка осуществляется с помощью коллекции **свойств** объекта **Recordset** или объекта **Command** .</span><span class="sxs-lookup"><span data-stu-id="4e1ec-223">These properties are accessed and set through the **Properties** collection of the **Recordset** or **Command** object.</span></span> <span data-ttu-id="4e1ec-224">В таблице перечислены имя свойства ADO и соответствующее имя свойства OLE DB в круглых скобках.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-224">The table lists the ADO property name and its corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4e1ec-225">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="4e1ec-225">Property Name</span></span></p></th>
<th><p><span data-ttu-id="4e1ec-226">Описание</span><span class="sxs-lookup"><span data-stu-id="4e1ec-226">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-227">Jet OLEDB: массовые транзакции</span><span class="sxs-lookup"><span data-stu-id="4e1ec-227">Jet OLEDB:Bulk Transactions</span></span><br />
<span data-ttu-id="4e1ec-228">(ДБПРОП_ЖЕТОЛЕДБ_БУЛКНОТРАНСАКТИОНС)</span><span class="sxs-lookup"><span data-stu-id="4e1ec-228">(DBPROP_JETOLEDB_BULKNOTRANSACTIONS)</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-229">Указывает, являются ли массовые операции SQL транзакционными.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-229">Indicates whether SQL bulk operations are transacted.</span></span> <span data-ttu-id="4e1ec-230">Большие массовые операции могут привести к сбою в связи с задержками ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-230">Large bulk operations might fail when transacted, due to resource delays.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-231">Jet OLEDB: включение курсоров FAT</span><span class="sxs-lookup"><span data-stu-id="4e1ec-231">Jet OLEDB:Enable Fat Cursors</span></span><br />
<span data-ttu-id="4e1ec-232">(ДБПРОП_ЖЕТОЛЕДБ_ЕНАБЛЕФАТКУРСОР)</span><span class="sxs-lookup"><span data-stu-id="4e1ec-232">(DBPROP_JETOLEDB_ENABLEFATCURSOR)</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-233">Указывает, должен ли Jet кэшировать несколько строк при заполнении набора записей для удаленных источников строк.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-233">Indicates whether Jet should cache multiple rows when populating a recordset for remote row sources.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-234">Jet OLEDB: размер кэша курсоров FAT</span><span class="sxs-lookup"><span data-stu-id="4e1ec-234">Jet OLEDB:Fat Cursor Cache Size</span></span><br />
<span data-ttu-id="4e1ec-235">(ДБПРОП_ЖЕТОЛЕДБ_ФАТКУРСОРМАКСРОВС)</span><span class="sxs-lookup"><span data-stu-id="4e1ec-235">(DBPROP_JETOLEDB_FATCURSORMAXROWS)</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-236">Указывает количество строк для кэширования при использовании кэширования строк удаленного хранилища данных.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-236">Indicates the number of rows to cache when using remote data store row caching.</span></span> <span data-ttu-id="4e1ec-237">Это значение игнорируется, если <strong>Jet OLEDB: enable FAT Cursors</strong> имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-237">This value is ignored unless <strong>Jet OLEDB:Enable Fat Cursors</strong> is True.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-238">Jet OLEDB: противоречивые</span><span class="sxs-lookup"><span data-stu-id="4e1ec-238">Jet OLEDB:Inconsistent</span></span><br />
<span data-ttu-id="4e1ec-239">(ДБПРОП_ЖЕТОЛЕДБ_ИНКОНСИСТЕНТ)</span><span class="sxs-lookup"><span data-stu-id="4e1ec-239">(DBPROP_JETOLEDB_INCONSISTENT)</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-240">Указывает, разрешены ли в результатах запроса несогласованные обновления.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-240">Indicates whether query results allow inconsistent updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-241">Jet OLEDB: Гранулярность блокировок</span><span class="sxs-lookup"><span data-stu-id="4e1ec-241">Jet OLEDB:Locking Granularity</span></span><br />
<span data-ttu-id="4e1ec-242">(ДБПРОП_ЖЕТОЛЕДБ_ЛОККГРАНУЛАРИТИ)</span><span class="sxs-lookup"><span data-stu-id="4e1ec-242">(DBPROP_JETOLEDB_LOCKGRANULARITY)</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-243">Указывает, открыта ли таблица с использованием блокировки на уровне строк.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-243">Indicates whether a table is opened using row-level locking.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-244">Jet OLEDB: оператор сквозного ODBC</span><span class="sxs-lookup"><span data-stu-id="4e1ec-244">Jet OLEDB:ODBC Pass-Through Statement</span></span><br />
<span data-ttu-id="4e1ec-245">(ДБПРОП_ЖЕТОЛЕДБ_ОДБКПАСССРАУГХ)</span><span class="sxs-lookup"><span data-stu-id="4e1ec-245">(DBPROP_JETOLEDB_ODBCPASSTHROUGH)</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-246">Указывает, что Jet должен передать текст SQL в объект <strong>Command</strong> обратно на сервер, не измененный.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-246">Indicates that Jet should pass the SQL text in a <strong>Command</strong> object to the back end unaltered.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-247">Jet OLEDB: частичные массовые операции</span><span class="sxs-lookup"><span data-stu-id="4e1ec-247">Jet OLEDB:Partial Bulk Ops</span></span><br />
<span data-ttu-id="4e1ec-248">(ДБПРОП_ЖЕТОЛЕДБ_БУЛКПАРТИАЛ)</span><span class="sxs-lookup"><span data-stu-id="4e1ec-248">(DBPROP_JETOLEDB_BULKPARTIAL)</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-249">Указывает поведение Jet при отказе операций SQL DML.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-249">Indicates Jet's behavior when SQL DML operations fail.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-250">Jet OLEDB: сквозная передача запроса массовой операции</span><span class="sxs-lookup"><span data-stu-id="4e1ec-250">Jet OLEDB:Pass Through Query Bulk-Op</span></span><br />
<span data-ttu-id="4e1ec-251">(ДБПРОП_ЖЕТОЛЕДБ_ПАСССРАУГХБУЛКОП)</span><span class="sxs-lookup"><span data-stu-id="4e1ec-251">(DBPROP_JETOLEDB_PASSTHROUGHBULKOP)</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-252">Указывает, передаются ли запросы, не возвращающие объект <strong>Recordset</strong> , в источник данных.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-252">Indicates whether queries that do not return a <strong>Recordset</strong> are passed unaltered to the data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-253">Jet OLEDB: строка сквозного подключения запроса</span><span class="sxs-lookup"><span data-stu-id="4e1ec-253">Jet OLEDB:Pass Through Query Connect String</span></span><br />
<span data-ttu-id="4e1ec-254">(ДБПРОП_ЖЕТОЛЕДБ_ОДБКПАСССРАУГХКОННЕКТСТРИНГ)</span><span class="sxs-lookup"><span data-stu-id="4e1ec-254">(DBPROP_JETOLEDB_ODBCPASSTHROUGHCONNECTSTRING)</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-255">Указывает строку подключения Jet, используемую для подключения к удаленному хранилищу данных.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-255">Indicates the Jet connect string used to connect to a remote data store.</span></span> <span data-ttu-id="4e1ec-256">Это значение игнорируется, если <strong>Jet OLEDB: сквозНой оператор ODBC</strong> имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-256">This value is ignored unless <strong>Jet OLEDB:ODBC Pass-Through Statement</strong> is True.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-257">Jet OLEDB: сохраненный запрос</span><span class="sxs-lookup"><span data-stu-id="4e1ec-257">Jet OLEDB:Stored Query</span></span><br />
<span data-ttu-id="4e1ec-258">(ДБПРОП_ЖЕТОЛЕДБ_СТОРЕДКУЕРИ)</span><span class="sxs-lookup"><span data-stu-id="4e1ec-258">(DBPROP_JETOLEDB_STOREDQUERY)</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-259">Указывает, следует ли интерпретировать текст команды как хранимый запрос вместо команды SQL.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-259">Indicates whether the command text should be interpreted as a stored query instead of an SQL command.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-260">Jet OLEDB: Проверка правил для набора</span><span class="sxs-lookup"><span data-stu-id="4e1ec-260">Jet OLEDB:Validate Rules On Set</span></span><br />
<span data-ttu-id="4e1ec-261">(ДБПРОП_ЖЕТОЛЕДБ_ВАЛИДАТЕОНСЕТ)</span><span class="sxs-lookup"><span data-stu-id="4e1ec-261">(DBPROP_JETOLEDB_VALIDATEONSET)</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-262">Указывает, оцениваются ли правила проверки Jet при задании данных столбцов или при фиксации изменений в базе данных.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-262">Indicates whether the Jet validation rules are evaluated when column data is set or when the changes are committed to the database.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4e1ec-263">По умолчанию поставщик OLE DB для Microsoft Jet открывает базы данных Microsoft Jet в режиме чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-263">By default, the OLE DB Provider for Microsoft Jet opens Microsoft Jet databases in read/write mode.</span></span> <span data-ttu-id="4e1ec-264">Чтобы открыть базу данных в режиме только для чтения, задайте для свойства [mode](mode-property-ado.md) объекта **подключения** ADO значение **адмодереад**.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-264">To open a database in read-only mode, set the [Mode](mode-property-ado.md) property on the ADO **Connection** object to **adModeRead**.</span></span>

## <a name="command-object-usage"></a><span data-ttu-id="4e1ec-265">Использование объекта Command</span><span class="sxs-lookup"><span data-stu-id="4e1ec-265">Command Object Usage</span></span>

<span data-ttu-id="4e1ec-266">Текст команды в объекте [Command](command-object-ado.md) использует диалект Microsoft Jet SQL.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-266">Command text in the [Command](command-object-ado.md) object uses the Microsoft Jet SQL dialect.</span></span> <span data-ttu-id="4e1ec-267">Можно указать запросы, возвращающие строки, запросы на изменение и имена таблиц, в тексте команды; Однако хранимые процедуры не поддерживаются и не должны указываться.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-267">You can specify row-returning queries, action queries, and table names in the command text; however, stored procedures are not supported and should not be specified.</span></span>

## <a name="recordset-behavior"></a><span data-ttu-id="4e1ec-268">Поведение набора записей</span><span class="sxs-lookup"><span data-stu-id="4e1ec-268">Recordset Behavior</span></span>

<span data-ttu-id="4e1ec-269">Ядро базы данных Microsoft Jet не поддерживает динамические курсоры.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-269">The Microsoft Jet database engine does not support dynamic cursors.</span></span> <span data-ttu-id="4e1ec-270">Таким образом, поставщик OLE DB для Microsoft Jet не поддерживает тип курсора **адлоккдинамик** .</span><span class="sxs-lookup"><span data-stu-id="4e1ec-270">Therefore, the OLE DB Provider for Microsoft Jet does not support the **adLockDynamic** cursor type.</span></span> <span data-ttu-id="4e1ec-271">При запросе динамического курсора поставщик возвращает курсор KEYSET и сбрасывает свойство [CursorType](cursortype-property-ado.md) , чтобы указать тип возвращаемого [набора записей](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="4e1ec-271">When a dynamic cursor is requested, the provider will return a keyset cursor and reset the [CursorType](cursortype-property-ado.md) property to indicate the type of [Recordset](recordset-object-ado.md) returned.</span></span> <span data-ttu-id="4e1ec-272">Кроме того, если запрашивается обновляемый **набор записей** (**LockType** — **адлоккоптимистик**, **адлоккбатчоптимистик**или **адлоккпессимистик**), поставщик также возвращает курсор набора ключей и сбрасывает значение **CursorType** свойств.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-272">Further, if an updatable **Recordset** is requested (**LockType** is **adLockOptimistic**, **adLockBatchOptimistic**, or **adLockPessimistic**) the provider will also return a keyset cursor and reset the **CursorType** property.</span></span>

## <a name="dynamic-properties"></a><span data-ttu-id="4e1ec-273">Динамические свойства</span><span class="sxs-lookup"><span data-stu-id="4e1ec-273">Dynamic Properties</span></span>

<span data-ttu-id="4e1ec-274">Поставщик OLE DB для Microsoft Jet вставляет несколько динамических свойств в коллекцию **свойств** неоткрытых [подключений](connection-object-ado.md), [наборов записей](recordset-object-ado.md)и объектов [команд](command-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="4e1ec-274">The OLE DB Provider for Microsoft Jet inserts several dynamic properties into the **Properties** collection of the unopened [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md), and [Command](command-object-ado.md) objects.</span></span>

<span data-ttu-id="4e1ec-275">В приведенных ниже таблицах указаны перекрестные индексы имен ADO и OLE DB для каждого динамического свойства.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-275">The tables below are a cross-index of the ADO and OLE DB names for each dynamic property.</span></span> <span data-ttu-id="4e1ec-276">Справочник программиста OLE DB ссылается на имя свойства ADO по термину "Описание".</span><span class="sxs-lookup"><span data-stu-id="4e1ec-276">The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description."</span></span> <span data-ttu-id="4e1ec-277">Дополнительные сведения об этих свойствах можно найти в справочнике программиста по OLE DB.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-277">You can find more information about these properties in the OLE DB Programmer's Reference.</span></span> <span data-ttu-id="4e1ec-278">Выполните поиск по имени свойства OLE DB в индексе или в разделе приложение C: свойства OLE DB.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-278">Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span></span>

## <a name="connection-dynamic-properties"></a><span data-ttu-id="4e1ec-279">Динамические свойства подключения</span><span class="sxs-lookup"><span data-stu-id="4e1ec-279">Connection Dynamic Properties</span></span>

<span data-ttu-id="4e1ec-280">Следующие свойства добавляются в коллекцию **свойств** объекта **Connection** .</span><span class="sxs-lookup"><span data-stu-id="4e1ec-280">The following properties are added to the **Connection** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4e1ec-281">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="4e1ec-281">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="4e1ec-282">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="4e1ec-282">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-283">Активные сеансы</span><span class="sxs-lookup"><span data-stu-id="4e1ec-283">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-284">ДБПРОП_АКТИВЕСЕССИОНС</span><span class="sxs-lookup"><span data-stu-id="4e1ec-284">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-285">Асинчабле Abort</span><span class="sxs-lookup"><span data-stu-id="4e1ec-285">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-286">ДБПРОП_АСИНКТКСНАБОРТ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-286">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-287">Фиксация Асинчабле</span><span class="sxs-lookup"><span data-stu-id="4e1ec-287">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-288">ДБПРОП_АСИНКТНКСКОММИТ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-288">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-289">Уровни изоляции для автоматической фиксации</span><span class="sxs-lookup"><span data-stu-id="4e1ec-289">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-290">ДБПРОП_СЕСС_АУТОКОММИТИСОЛЕВЕЛС</span><span class="sxs-lookup"><span data-stu-id="4e1ec-290">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-291">Расположение каталога</span><span class="sxs-lookup"><span data-stu-id="4e1ec-291">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-292">ДБПРОП_КАТАЛОГЛОКАТИОН</span><span class="sxs-lookup"><span data-stu-id="4e1ec-292">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-293">Термин каталога</span><span class="sxs-lookup"><span data-stu-id="4e1ec-293">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-294">ДБПРОП_КАТАЛОГТЕРМ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-294">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-295">Определение столбца</span><span class="sxs-lookup"><span data-stu-id="4e1ec-295">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-296">ДБПРОП_КОЛУМНДЕФИНИТИОН</span><span class="sxs-lookup"><span data-stu-id="4e1ec-296">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-297">Текущий каталог</span><span class="sxs-lookup"><span data-stu-id="4e1ec-297">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-298">ДБПРОП_КУРРЕНТКАТАЛОГ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-298">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-299">Источник данных</span><span class="sxs-lookup"><span data-stu-id="4e1ec-299">Data Source</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-300">ДБПРОП_ИНИТ_ДАТАСАУРЦЕ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-300">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-301">Имя источника данных</span><span class="sxs-lookup"><span data-stu-id="4e1ec-301">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-302">ДБПРОП_ДАТАСАУРЦЕНАМЕ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-302">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-303">Модель потоков объектов источника данных</span><span class="sxs-lookup"><span data-stu-id="4e1ec-303">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-304">ДБПРОП_ДСОСРЕАДМОДЕЛ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-304">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-305">Имя СУБД</span><span class="sxs-lookup"><span data-stu-id="4e1ec-305">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-306">ДБПРОП_ДБМСНАМЕ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-306">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-307">Версия DBMS</span><span class="sxs-lookup"><span data-stu-id="4e1ec-307">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-308">ДБПРОП_ДБМСВЕР</span><span class="sxs-lookup"><span data-stu-id="4e1ec-308">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-309">ГРУППИРОВКа по поддержке</span><span class="sxs-lookup"><span data-stu-id="4e1ec-309">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-310">ДБПРОП_ГРАУПБИ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-310">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-311">Поддержка гетерогенных таблиц</span><span class="sxs-lookup"><span data-stu-id="4e1ec-311">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-312">ДБПРОП_ХЕТЕРОЖЕНЕАУСТАБЛЕС</span><span class="sxs-lookup"><span data-stu-id="4e1ec-312">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-313">Чувствительность к регистру идентификаторов</span><span class="sxs-lookup"><span data-stu-id="4e1ec-313">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-314">ДБПРОП_ИДЕНТИФИЕРКАСЕ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-314">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-315">Уровни изоляции</span><span class="sxs-lookup"><span data-stu-id="4e1ec-315">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-316">ДБПРОП_СУППОРТЕДТКСНИСОЛЕВЕЛС</span><span class="sxs-lookup"><span data-stu-id="4e1ec-316">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-317">Хранение изоляции</span><span class="sxs-lookup"><span data-stu-id="4e1ec-317">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-318">ДБПРОП_СУППОРТЕДТКСНИСОРЕТАИН</span><span class="sxs-lookup"><span data-stu-id="4e1ec-318">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-319">Идентификатор языкового стандарта</span><span class="sxs-lookup"><span data-stu-id="4e1ec-319">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-320">ДБПРОП_ИНИТ_ЛЦИД</span><span class="sxs-lookup"><span data-stu-id="4e1ec-320">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-321">Максимальный размер индекса</span><span class="sxs-lookup"><span data-stu-id="4e1ec-321">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-322">ДБПРОП_МАКСИНДЕКССИЗЕ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-322">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-323">Максимальный размер строки</span><span class="sxs-lookup"><span data-stu-id="4e1ec-323">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-324">ДБПРОП_МАКСРОВСИЗЕ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-324">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-325">Максимальный размер строки включает большой ДВОИЧный объект</span><span class="sxs-lookup"><span data-stu-id="4e1ec-325">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-326">ДБПРОП_МАКСРОВСИЗЕИНКЛУДЕСБЛОБ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-326">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-327">Максимальное число таблиц в SELECT</span><span class="sxs-lookup"><span data-stu-id="4e1ec-327">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-328">ДБПРОП_МАКСТАБЛЕСИНСЕЛЕКТ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-328">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-329">Режим</span><span class="sxs-lookup"><span data-stu-id="4e1ec-329">Mode</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-330">ДБПРОП_ИНИТ_МОДЕ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-330">DBPROP_INIT_MODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-331">Наборы параметров с несколькими параметрами</span><span class="sxs-lookup"><span data-stu-id="4e1ec-331">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-332">ДБПРОП_МУЛТИПЛЕПАРАМСЕТС</span><span class="sxs-lookup"><span data-stu-id="4e1ec-332">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-333">Несколько результатов</span><span class="sxs-lookup"><span data-stu-id="4e1ec-333">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-334">ДБПРОП_МУЛТИПЛЕРЕСУЛТС</span><span class="sxs-lookup"><span data-stu-id="4e1ec-334">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-335">Несколько объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="4e1ec-335">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-336">ДБПРОП_МУЛТИПЛЕСТОРАЖЕОБЖЕКТС</span><span class="sxs-lookup"><span data-stu-id="4e1ec-336">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-337">Обновление с несколькими таблицами</span><span class="sxs-lookup"><span data-stu-id="4e1ec-337">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-338">ДБПРОП_МУЛТИТАБЛЕУПДАТЕ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-338">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-339">Порядок сортировки NULL</span><span class="sxs-lookup"><span data-stu-id="4e1ec-339">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-340">ДБПРОП_НУЛЛКОЛЛАТИОН</span><span class="sxs-lookup"><span data-stu-id="4e1ec-340">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-341">Поведение сцепления со ЗНАЧЕНИЕМ NULL</span><span class="sxs-lookup"><span data-stu-id="4e1ec-341">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-342">ДБПРОП_КОНКАТНУЛЛБЕХАВИОР</span><span class="sxs-lookup"><span data-stu-id="4e1ec-342">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-343">Версия OLE DB</span><span class="sxs-lookup"><span data-stu-id="4e1ec-343">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-344">ДБПРОП_ПРОВИДЕРОЛЕДБВЕР</span><span class="sxs-lookup"><span data-stu-id="4e1ec-344">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-345">Поддержка объектов OLE</span><span class="sxs-lookup"><span data-stu-id="4e1ec-345">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-346">ДБПРОП_ОЛЕОБЖЕКТС</span><span class="sxs-lookup"><span data-stu-id="4e1ec-346">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-347">Поддержка открытых наборов строк</span><span class="sxs-lookup"><span data-stu-id="4e1ec-347">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-348">ДБПРОП_ОПЕНРОВСЕТСУППОРТ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-348">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-349">УПОРЯДОЧЕНие по столбцам в списке выборки</span><span class="sxs-lookup"><span data-stu-id="4e1ec-349">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-350">ДБПРОП_ОРДЕРБИКОЛУМНСИНСЕЛЕКТ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-350">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-351">Доступность выходного параметра</span><span class="sxs-lookup"><span data-stu-id="4e1ec-351">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-352">ДБПРОП_АУТПУТПАРАМЕТЕРАВАИЛАБИЛИТИ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-352">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-353">Передача по параметрам доступа ref</span><span class="sxs-lookup"><span data-stu-id="4e1ec-353">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-354">ДБПРОП_БИРЕФАКЦЕССОРС</span><span class="sxs-lookup"><span data-stu-id="4e1ec-354">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-355">Пароль</span><span class="sxs-lookup"><span data-stu-id="4e1ec-355">Password</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-356">ДБПРОП_АУС_ПАССВОРД</span><span class="sxs-lookup"><span data-stu-id="4e1ec-356">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-357">Тип постоянного идентификатора</span><span class="sxs-lookup"><span data-stu-id="4e1ec-357">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-358">ДБПРОП_ПЕРСИСТЕНТИДТИПЕ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-358">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-359">Действие по подготовке к прерыванию</span><span class="sxs-lookup"><span data-stu-id="4e1ec-359">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-360">ДБПРОП_ПРЕПАРЕАБОРТБЕХАВИОР</span><span class="sxs-lookup"><span data-stu-id="4e1ec-360">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-361">Подготовка режима фиксации</span><span class="sxs-lookup"><span data-stu-id="4e1ec-361">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-362">ДБПРОП_ПРЕПАРЕКОММИТБЕХАВИОР</span><span class="sxs-lookup"><span data-stu-id="4e1ec-362">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-363">Термин процедуры</span><span class="sxs-lookup"><span data-stu-id="4e1ec-363">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-364">ДБПРОП_ПРОЦЕДУРЕТЕРМ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-364">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-365">Prompt</span><span class="sxs-lookup"><span data-stu-id="4e1ec-365">Prompt</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-366">ДБПРОП_ИНИТ_ПРОМПТ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-366">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-367">Понятное имя поставщика</span><span class="sxs-lookup"><span data-stu-id="4e1ec-367">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-368">ДБПРОП_ПРОВИДЕРФРИЕНДЛИНАМЕ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-368">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-369">Имя поставщика</span><span class="sxs-lookup"><span data-stu-id="4e1ec-369">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-370">ДБПРОП_ПРОВИДЕРФИЛЕНАМЕ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-370">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-371">Версия поставщика</span><span class="sxs-lookup"><span data-stu-id="4e1ec-371">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-372">ДБПРОП_ПРОВИДЕРВЕР</span><span class="sxs-lookup"><span data-stu-id="4e1ec-372">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-373">Источник данных, предназначенный только для чтения</span><span class="sxs-lookup"><span data-stu-id="4e1ec-373">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-374">ДБПРОП_ДАТАСАУРЦЕРЕАДОНЛИ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-374">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-375">Преобразования наборов строк для команды</span><span class="sxs-lookup"><span data-stu-id="4e1ec-375">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-376">ДБПРОП_РОВСЕТКОНВЕРСИОНСОНКОММАНД</span><span class="sxs-lookup"><span data-stu-id="4e1ec-376">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-377">Термин схемы</span><span class="sxs-lookup"><span data-stu-id="4e1ec-377">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-378">ДБПРОП_СЧЕМАТЕРМ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-378">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-379">Использование схемы</span><span class="sxs-lookup"><span data-stu-id="4e1ec-379">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-380">ДБПРОП_СЧЕМАУСАЖЕ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-380">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-381">Поддержка SQL</span><span class="sxs-lookup"><span data-stu-id="4e1ec-381">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-382">ДБПРОП_СКЛСУППОРТ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-382">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-383">Структурированное хранилище</span><span class="sxs-lookup"><span data-stu-id="4e1ec-383">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-384">ДБПРОП_СТРУКТУРЕДСТОРАЖЕ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-384">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-385">Поддержка вложенных запросов</span><span class="sxs-lookup"><span data-stu-id="4e1ec-385">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-386">ДБПРОП_СУБКУЕРИЕС</span><span class="sxs-lookup"><span data-stu-id="4e1ec-386">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-387">Табличный термин</span><span class="sxs-lookup"><span data-stu-id="4e1ec-387">Table Term</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-388">ДБПРОП_ТАБЛЕТЕРМ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-388">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-389">DDL транзакции</span><span class="sxs-lookup"><span data-stu-id="4e1ec-389">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-390">ДБПРОП_СУППОРТЕДТКСНДДЛ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-390">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-391">Идентификатор пользователя</span><span class="sxs-lookup"><span data-stu-id="4e1ec-391">User ID</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-392">ДБПРОП_АУС_УСЕРИД</span><span class="sxs-lookup"><span data-stu-id="4e1ec-392">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-393">имя пользователя;</span><span class="sxs-lookup"><span data-stu-id="4e1ec-393">User Name</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-394">ДБПРОП_УСЕРНАМЕ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-394">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-395">Дескриптор окна</span><span class="sxs-lookup"><span data-stu-id="4e1ec-395">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-396">ДБПРОП_ИНИТ_ХВНД</span><span class="sxs-lookup"><span data-stu-id="4e1ec-396">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a><span data-ttu-id="4e1ec-397">Динамические свойства Recordset</span><span class="sxs-lookup"><span data-stu-id="4e1ec-397">Recordset Dynamic Properties</span></span>

<span data-ttu-id="4e1ec-398">Следующие свойства добавляются в коллекцию **свойств** объекта **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="4e1ec-398">The following properties are added to the **Recordset** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4e1ec-399">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="4e1ec-399">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="4e1ec-400">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="4e1ec-400">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-401">Порядок доступа</span><span class="sxs-lookup"><span data-stu-id="4e1ec-401">Access Order</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-402">ДБПРОП_АКЦЕССОРДЕР</span><span class="sxs-lookup"><span data-stu-id="4e1ec-402">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-403">Набор строк только для добавления</span><span class="sxs-lookup"><span data-stu-id="4e1ec-403">Append-Only Rowset</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-404">ДБПРОП_АППЕНДОНЛИ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-404">DBPROP_APPENDONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-405">Блокировка объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="4e1ec-405">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-406">ДБПРОП_БЛОККИНГСТОРАЖЕОБЖЕКТС</span><span class="sxs-lookup"><span data-stu-id="4e1ec-406">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-407">Тип закладки</span><span class="sxs-lookup"><span data-stu-id="4e1ec-407">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-408">ДБПРОП_БУКМАРКТИПЕ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-408">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-409">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="4e1ec-409">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-410">ДБПРОП_ИРОВСЕТЛОКАТЕ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-410">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-411">Упорядоченные закладки</span><span class="sxs-lookup"><span data-stu-id="4e1ec-411">Bookmarks Ordered</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-412">ДБПРОП_ОРДЕРЕДБУКМАРКС</span><span class="sxs-lookup"><span data-stu-id="4e1ec-412">DBPROP_ORDEREDBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-413">Кэширование отложенных столбцов</span><span class="sxs-lookup"><span data-stu-id="4e1ec-413">Cache Deferred Columns</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-414">ДБПРОП_КАЧЕДЕФЕРРЕД</span><span class="sxs-lookup"><span data-stu-id="4e1ec-414">DBPROP_CACHEDEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-415">Изменение вставленных строк</span><span class="sxs-lookup"><span data-stu-id="4e1ec-415">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-416">ДБПРОП_ЧАНЖЕИНСЕРТЕДРОВС</span><span class="sxs-lookup"><span data-stu-id="4e1ec-416">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-417">Права на столбцы</span><span class="sxs-lookup"><span data-stu-id="4e1ec-417">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-418">ДБПРОП_КОЛУМНРЕСТРИКТ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-418">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-419">Уведомление о наборе столбцов</span><span class="sxs-lookup"><span data-stu-id="4e1ec-419">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-420">ДБПРОП_НОТИФИКОЛУМНСЕТ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-420">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-421">Столбец доступен для записи</span><span class="sxs-lookup"><span data-stu-id="4e1ec-421">Column Writable</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-422">ДБПРОП_МАЙВРИТЕКОЛУМН</span><span class="sxs-lookup"><span data-stu-id="4e1ec-422">DBPROP_MAYWRITECOLUMN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-423">ОтКладывание столбца</span><span class="sxs-lookup"><span data-stu-id="4e1ec-423">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-424">ДБПРОП_ДЕФЕРРЕД</span><span class="sxs-lookup"><span data-stu-id="4e1ec-424">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-425">ОтКладывание обновлений объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="4e1ec-425">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-426">ДБПРОП_ДЕЛАЙСТОРАЖЕОБЖЕКТС</span><span class="sxs-lookup"><span data-stu-id="4e1ec-426">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-427">Извлечение назад</span><span class="sxs-lookup"><span data-stu-id="4e1ec-427">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-428">ДБПРОП_КАНФЕТЧБАККВАРДС</span><span class="sxs-lookup"><span data-stu-id="4e1ec-428">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-429">Удержание строк</span><span class="sxs-lookup"><span data-stu-id="4e1ec-429">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-430">ДБПРОП_КАНХОЛДРОВС</span><span class="sxs-lookup"><span data-stu-id="4e1ec-430">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-431">Иакцессор</span><span class="sxs-lookup"><span data-stu-id="4e1ec-431">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-432">Дбпроп_иакцессор</span><span class="sxs-lookup"><span data-stu-id="4e1ec-432">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-433">Иколумнсинфо</span><span class="sxs-lookup"><span data-stu-id="4e1ec-433">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-434">Дбпроп_иколумнсинфо</span><span class="sxs-lookup"><span data-stu-id="4e1ec-434">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-435">Иколумнсровсет</span><span class="sxs-lookup"><span data-stu-id="4e1ec-435">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-436">Дбпроп_иколумнсровсет</span><span class="sxs-lookup"><span data-stu-id="4e1ec-436">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-437">Иконнектионпоинтконтаинер</span><span class="sxs-lookup"><span data-stu-id="4e1ec-437">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-438">Дбпроп_иконнектионпоинтконтаинер</span><span class="sxs-lookup"><span data-stu-id="4e1ec-438">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-439">Иконверттипе</span><span class="sxs-lookup"><span data-stu-id="4e1ec-439">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-440">Дбпроп_иконверттипе</span><span class="sxs-lookup"><span data-stu-id="4e1ec-440">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-441">ILockBytes</span><span class="sxs-lookup"><span data-stu-id="4e1ec-441">ILockBytes</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-442">Дбпроп_илоккбитес</span><span class="sxs-lookup"><span data-stu-id="4e1ec-442">DBPROP_ILockBytes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-443">Строки для мобильных устройств</span><span class="sxs-lookup"><span data-stu-id="4e1ec-443">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-444">ДБПРОП_ИММОБИЛЕРОВС</span><span class="sxs-lookup"><span data-stu-id="4e1ec-444">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-445">IRowset</span><span class="sxs-lookup"><span data-stu-id="4e1ec-445">IRowset</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-446">Дбпроп_ировсет</span><span class="sxs-lookup"><span data-stu-id="4e1ec-446">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-447">Ировсетчанже</span><span class="sxs-lookup"><span data-stu-id="4e1ec-447">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-448">Дбпроп_ировсетчанже</span><span class="sxs-lookup"><span data-stu-id="4e1ec-448">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-449">Ировсетидентити</span><span class="sxs-lookup"><span data-stu-id="4e1ec-449">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-450">Дбпроп_ировсетидентити</span><span class="sxs-lookup"><span data-stu-id="4e1ec-450">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-451">Ировсетиндекс</span><span class="sxs-lookup"><span data-stu-id="4e1ec-451">IRowsetIndex</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-452">Дбпроп_ировсетиндекс</span><span class="sxs-lookup"><span data-stu-id="4e1ec-452">DBPROP_IRowsetIndex</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-453">Ировсетинфо</span><span class="sxs-lookup"><span data-stu-id="4e1ec-453">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-454">Дбпроп_ировсетинфо</span><span class="sxs-lookup"><span data-stu-id="4e1ec-454">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-455">Ировсетлокате</span><span class="sxs-lookup"><span data-stu-id="4e1ec-455">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-456">Дбпроп_ировсестлокате</span><span class="sxs-lookup"><span data-stu-id="4e1ec-456">DBPROP_IRowsestLocate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-457">Ировсетресинч</span><span class="sxs-lookup"><span data-stu-id="4e1ec-457">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-458">Ировсетскролл</span><span class="sxs-lookup"><span data-stu-id="4e1ec-458">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-459">Дбпроп_ировсетскролл</span><span class="sxs-lookup"><span data-stu-id="4e1ec-459">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-460">Ировсетупдате</span><span class="sxs-lookup"><span data-stu-id="4e1ec-460">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-461">Дбпроп_ировсетупдате</span><span class="sxs-lookup"><span data-stu-id="4e1ec-461">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-462">Исекуентиалстреам</span><span class="sxs-lookup"><span data-stu-id="4e1ec-462">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-463">Дбпроп_исекуентиалстреам</span><span class="sxs-lookup"><span data-stu-id="4e1ec-463">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-464">Содержим</span><span class="sxs-lookup"><span data-stu-id="4e1ec-464">IStorage</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-465">Дбпроп_истораже</span><span class="sxs-lookup"><span data-stu-id="4e1ec-465">DBPROP_IStorage</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-466">IStream</span><span class="sxs-lookup"><span data-stu-id="4e1ec-466">IStream</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-467">Дбпроп_истреам</span><span class="sxs-lookup"><span data-stu-id="4e1ec-467">DBPROP_IStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-468">Исуппортерроринфо</span><span class="sxs-lookup"><span data-stu-id="4e1ec-468">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-469">Дбпроп_исуппортерроринфо</span><span class="sxs-lookup"><span data-stu-id="4e1ec-469">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-470">Литеральные закладки</span><span class="sxs-lookup"><span data-stu-id="4e1ec-470">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-471">ДБПРОП_ЛИТЕРАЛБУКМАРКС</span><span class="sxs-lookup"><span data-stu-id="4e1ec-471">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-472">Идентификация строк литералов</span><span class="sxs-lookup"><span data-stu-id="4e1ec-472">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-473">ДБПРОП_ЛИТЕРАЛИДЕНТИТИ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-473">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-474">Максимальное число открытых строк</span><span class="sxs-lookup"><span data-stu-id="4e1ec-474">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-475">ДБПРОП_МАКСОПЕНРОВС</span><span class="sxs-lookup"><span data-stu-id="4e1ec-475">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-476">Максимальное число ожидающих строк</span><span class="sxs-lookup"><span data-stu-id="4e1ec-476">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-477">ДБПРОП_МАКСПЕНДИНГРОВС</span><span class="sxs-lookup"><span data-stu-id="4e1ec-477">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-478">Максимальное число строк</span><span class="sxs-lookup"><span data-stu-id="4e1ec-478">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-479">ДБПРОП_МАКСРОВС</span><span class="sxs-lookup"><span data-stu-id="4e1ec-479">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-480">Использование памяти</span><span class="sxs-lookup"><span data-stu-id="4e1ec-480">Memory Usage</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-481">ДБПРОП_МЕМОРЮСАЖЕ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-481">DBPROP_MEMORYUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-482">Детализация уведомлений</span><span class="sxs-lookup"><span data-stu-id="4e1ec-482">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-483">ДБПРОП_НОТИФИКАТИОНГРАНУЛАРИТИ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-483">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-484">Этапы уведомления</span><span class="sxs-lookup"><span data-stu-id="4e1ec-484">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-485">ДБПРОП_НОТИФИКАТИОНФАСЕС</span><span class="sxs-lookup"><span data-stu-id="4e1ec-485">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-486">Объекты, транзакционные</span><span class="sxs-lookup"><span data-stu-id="4e1ec-486">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-487">ДБПРОП_ТРАНСАКТЕДОБЖЕКТ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-487">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-488">Видны другие изменения</span><span class="sxs-lookup"><span data-stu-id="4e1ec-488">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-489">ДБПРОП_ОСЕРУПДАТЕДЕЛЕТЕ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-489">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-490">Видимые вставки других пользователей</span><span class="sxs-lookup"><span data-stu-id="4e1ec-490">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-491">ДБПРОП_ОСЕРИНСЕРТ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-491">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-492">Видны изменения</span><span class="sxs-lookup"><span data-stu-id="4e1ec-492">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-493">ДБПРОП_ОВНУПДАТЕДЕЛЕТЕ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-493">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-494">Отображение собственных вставок</span><span class="sxs-lookup"><span data-stu-id="4e1ec-494">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-495">ДБПРОП_ОВНИНСЕРТ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-495">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-496">Сохранение при прерывании</span><span class="sxs-lookup"><span data-stu-id="4e1ec-496">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-497">ДБПРОП_АБОРТПРЕСЕРВЕ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-497">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-498">Сохранение при фиксации</span><span class="sxs-lookup"><span data-stu-id="4e1ec-498">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-499">ДБПРОП_КОММИТПРЕСЕРВЕ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-499">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-500">Быстрый перезапуск</span><span class="sxs-lookup"><span data-stu-id="4e1ec-500">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-501">ДБПРОП_КУИККРЕСТАРТ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-501">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-502">Повторные события</span><span class="sxs-lookup"><span data-stu-id="4e1ec-502">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-503">ДБПРОП_РИНТРАНТЕВЕНТС</span><span class="sxs-lookup"><span data-stu-id="4e1ec-503">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-504">Удаление удаленных строк</span><span class="sxs-lookup"><span data-stu-id="4e1ec-504">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-505">ДБПРОП_РЕМОВЕДЕЛЕТЕД</span><span class="sxs-lookup"><span data-stu-id="4e1ec-505">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-506">Отчет о нескольких изменениях</span><span class="sxs-lookup"><span data-stu-id="4e1ec-506">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-507">ДБПРОП_РЕПОРТМУЛТИПЛЕЧАНЖЕС</span><span class="sxs-lookup"><span data-stu-id="4e1ec-507">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-508">Возврат ожидающих вставок</span><span class="sxs-lookup"><span data-stu-id="4e1ec-508">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-509">ДБПРОП_РЕТУРНПЕНДИНГИНСЕРТС</span><span class="sxs-lookup"><span data-stu-id="4e1ec-509">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-510">Уведомление об удалении строки</span><span class="sxs-lookup"><span data-stu-id="4e1ec-510">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-511">ДБПРОП_НОТИФИРОВДЕЛЕТЕ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-511">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-512">Уведомление о первом изменении строки</span><span class="sxs-lookup"><span data-stu-id="4e1ec-512">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-513">ДБПРОП_НОТИФИРОВФИРСТЧАНЖЕ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-513">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-514">Уведомление о вставке строк</span><span class="sxs-lookup"><span data-stu-id="4e1ec-514">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-515">ДБПРОП_НОТИФИРОВИНСЕРТ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-515">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-516">Права на строки</span><span class="sxs-lookup"><span data-stu-id="4e1ec-516">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-517">ДБПРОП_РОВРЕСТРИКТ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-517">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-518">Уведомление о повторной синхронизации строк</span><span class="sxs-lookup"><span data-stu-id="4e1ec-518">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-519">ДБПРОП_НОТИФИРОВРЕСИНЧ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-519">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-520">Потоковая модель для строк</span><span class="sxs-lookup"><span data-stu-id="4e1ec-520">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-521">ДБПРОП_РОВСРЕАДМОДЕЛ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-521">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-522">Уведомление об отмене изменения строки</span><span class="sxs-lookup"><span data-stu-id="4e1ec-522">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-523">ДБПРОП_НОТИФИРОВУНДОЧАНЖЕ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-523">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-524">Уведомление о отмене удаления строки</span><span class="sxs-lookup"><span data-stu-id="4e1ec-524">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-525">ДБПРОП_НОТИФИРОВУНДОДЕЛЕТЕ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-525">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-526">Уведомление об отмене вставки строки</span><span class="sxs-lookup"><span data-stu-id="4e1ec-526">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-527">ДБПРОП_НОТИФИРОВУНДОИНСЕРТ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-527">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-528">Уведомление об обновлении строк</span><span class="sxs-lookup"><span data-stu-id="4e1ec-528">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-529">ДБПРОП_НОТИФИРОВУПДАТЕ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-529">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-530">Уведомление об изменении положения при получении набора строк</span><span class="sxs-lookup"><span data-stu-id="4e1ec-530">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-531">ДБПРОП_НОТИФИРОВСЕТФЕТЧПОСИСИОНЧАНЖЕ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-531">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-532">Уведомление о выПуске набора строк</span><span class="sxs-lookup"><span data-stu-id="4e1ec-532">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-533">ДБПРОП_НОТИФИРОВСЕТРЕЛЕАСЕ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-533">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-534">ПроКрутка назад</span><span class="sxs-lookup"><span data-stu-id="4e1ec-534">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-535">ДБПРОП_КАНСКРОЛЛБАККВАРДС</span><span class="sxs-lookup"><span data-stu-id="4e1ec-535">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-536">Пропуск удаленных закладок</span><span class="sxs-lookup"><span data-stu-id="4e1ec-536">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-537">ДБПРОП_БУКМАРКСКИППЕД</span><span class="sxs-lookup"><span data-stu-id="4e1ec-537">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-538">Строгая идентификация строк</span><span class="sxs-lookup"><span data-stu-id="4e1ec-538">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-539">ДБПРОП_СТРОНГИТДЕНТИТИ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-539">DBPROP_STRONGITDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-540">Обновление</span><span class="sxs-lookup"><span data-stu-id="4e1ec-540">Updatability</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-541">ДБПРОП_УПДАТАБИЛИТИ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-541">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-542">Использование закладок</span><span class="sxs-lookup"><span data-stu-id="4e1ec-542">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-543">ДБПРОП_БУКМАРКС</span><span class="sxs-lookup"><span data-stu-id="4e1ec-543">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a><span data-ttu-id="4e1ec-544">Динамические свойства команд</span><span class="sxs-lookup"><span data-stu-id="4e1ec-544">Command Dynamic Properties</span></span>

<span data-ttu-id="4e1ec-545">Указанные ниже свойства добавляются в коллекцию \*\*\*\* **свойств** командного объекта.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-545">The following properties are added to the **Command** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4e1ec-546">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="4e1ec-546">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="4e1ec-547">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="4e1ec-547">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-548">Порядок доступа</span><span class="sxs-lookup"><span data-stu-id="4e1ec-548">Access Order</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-549">ДБПРОП_АКЦЕССОРДЕР</span><span class="sxs-lookup"><span data-stu-id="4e1ec-549">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-550">Набор строк только для добавления</span><span class="sxs-lookup"><span data-stu-id="4e1ec-550">Append-Only Rowset</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-551">ДБПРОП_АППЕНДОНЛИ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-551">DBPROP_APPENDONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-552">Блокировка объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="4e1ec-552">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-553">ДБПРОП_БЛОККИНГСТОРАЖЕОБЖЕКТС</span><span class="sxs-lookup"><span data-stu-id="4e1ec-553">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-554">Тип закладки</span><span class="sxs-lookup"><span data-stu-id="4e1ec-554">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-555">ДБПРОП_БУКМАРКТИПЕ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-555">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-556">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="4e1ec-556">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-557">ДБПРОП_ИРОВСЕТЛОКАТЕ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-557">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-558">Изменение вставленных строк</span><span class="sxs-lookup"><span data-stu-id="4e1ec-558">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-559">ДБПРОП_ЧАНЖЕИНСЕРТЕДРОВС</span><span class="sxs-lookup"><span data-stu-id="4e1ec-559">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-560">Права на столбцы</span><span class="sxs-lookup"><span data-stu-id="4e1ec-560">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-561">ДБПРОП_КОЛУМНРЕСТРИКТ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-561">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-562">Уведомление о наборе столбцов</span><span class="sxs-lookup"><span data-stu-id="4e1ec-562">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-563">ДБПРОП_НОТИФИКОЛУМНСЕТ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-563">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-564">ОтКладывание столбца</span><span class="sxs-lookup"><span data-stu-id="4e1ec-564">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-565">ДБПРОП_ДЕФЕРРЕД</span><span class="sxs-lookup"><span data-stu-id="4e1ec-565">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-566">ОтКладывание обновлений объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="4e1ec-566">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-567">ДБПРОП_ДЕЛАЙСТОРАЖЕОБЖЕКТС</span><span class="sxs-lookup"><span data-stu-id="4e1ec-567">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-568">Извлечение назад</span><span class="sxs-lookup"><span data-stu-id="4e1ec-568">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-569">ДБПРОП_КАНФЕТЧБАККВАРДС</span><span class="sxs-lookup"><span data-stu-id="4e1ec-569">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-570">Удержание строк</span><span class="sxs-lookup"><span data-stu-id="4e1ec-570">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-571">ДБПРОП_КАНХОЛДРОВС</span><span class="sxs-lookup"><span data-stu-id="4e1ec-571">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-572">Иакцессор</span><span class="sxs-lookup"><span data-stu-id="4e1ec-572">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-573">Дбпроп_иакцессор</span><span class="sxs-lookup"><span data-stu-id="4e1ec-573">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-574">Иколумнсинфо</span><span class="sxs-lookup"><span data-stu-id="4e1ec-574">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-575">Дбпроп_иколумнсинфо</span><span class="sxs-lookup"><span data-stu-id="4e1ec-575">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-576">Иколумнсровсет</span><span class="sxs-lookup"><span data-stu-id="4e1ec-576">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-577">Дбпроп_иколумнсровсет</span><span class="sxs-lookup"><span data-stu-id="4e1ec-577">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-578">Иконнектионпоинтконтаинер</span><span class="sxs-lookup"><span data-stu-id="4e1ec-578">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-579">Дбпроп_иконнектионпоинтконтаинер</span><span class="sxs-lookup"><span data-stu-id="4e1ec-579">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-580">Иконверттипе</span><span class="sxs-lookup"><span data-stu-id="4e1ec-580">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-581">Дбпроп_иконверттипе</span><span class="sxs-lookup"><span data-stu-id="4e1ec-581">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-582">ILockBytes</span><span class="sxs-lookup"><span data-stu-id="4e1ec-582">ILockBytes</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-583">Дбпроп_илоккбитес</span><span class="sxs-lookup"><span data-stu-id="4e1ec-583">DBPROP_ILockBytes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-584">Строки для мобильных устройств</span><span class="sxs-lookup"><span data-stu-id="4e1ec-584">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-585">ДБПРОП_ИММОБИЛЕРОВС</span><span class="sxs-lookup"><span data-stu-id="4e1ec-585">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-586">IRowset</span><span class="sxs-lookup"><span data-stu-id="4e1ec-586">IRowset</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-587">Дбпроп_ировсет</span><span class="sxs-lookup"><span data-stu-id="4e1ec-587">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-588">Ировсетчанже</span><span class="sxs-lookup"><span data-stu-id="4e1ec-588">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-589">Дбпроп_ировсетчанже</span><span class="sxs-lookup"><span data-stu-id="4e1ec-589">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-590">Ировсетидентити</span><span class="sxs-lookup"><span data-stu-id="4e1ec-590">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-591">Дбпроп_ировсетидентити</span><span class="sxs-lookup"><span data-stu-id="4e1ec-591">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-592">Ировсетиндекс</span><span class="sxs-lookup"><span data-stu-id="4e1ec-592">IRowsetIndex</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-593">Дбпроп_ировсетиндекс</span><span class="sxs-lookup"><span data-stu-id="4e1ec-593">DBPROP_IRowsetIndex</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-594">Ировсетинфо</span><span class="sxs-lookup"><span data-stu-id="4e1ec-594">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-595">Дбпроп_ировсетинфо</span><span class="sxs-lookup"><span data-stu-id="4e1ec-595">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-596">Ировсетлокате</span><span class="sxs-lookup"><span data-stu-id="4e1ec-596">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-597">Дбпроп_ировсетлокате</span><span class="sxs-lookup"><span data-stu-id="4e1ec-597">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-598">Ировсетресинч</span><span class="sxs-lookup"><span data-stu-id="4e1ec-598">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-599">Ировсетскролл</span><span class="sxs-lookup"><span data-stu-id="4e1ec-599">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-600">Дбпроп_ировсетскролл</span><span class="sxs-lookup"><span data-stu-id="4e1ec-600">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-601">Ировсетупдате</span><span class="sxs-lookup"><span data-stu-id="4e1ec-601">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-602">Дбпроп_ировсетупдате</span><span class="sxs-lookup"><span data-stu-id="4e1ec-602">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-603">Исекуентиалстреам</span><span class="sxs-lookup"><span data-stu-id="4e1ec-603">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-604">Дбпроп_исекуентиалстреам</span><span class="sxs-lookup"><span data-stu-id="4e1ec-604">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-605">Содержим</span><span class="sxs-lookup"><span data-stu-id="4e1ec-605">IStorage</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-606">Дбпроп_истораже</span><span class="sxs-lookup"><span data-stu-id="4e1ec-606">DBPROP_IStorage</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-607">IStream</span><span class="sxs-lookup"><span data-stu-id="4e1ec-607">IStream</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-608">Дбпроп_истреам</span><span class="sxs-lookup"><span data-stu-id="4e1ec-608">DBPROP_IStream</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-609">Исуппортерроринфо</span><span class="sxs-lookup"><span data-stu-id="4e1ec-609">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-610">Дбпроп_исуппортерроринфо</span><span class="sxs-lookup"><span data-stu-id="4e1ec-610">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-611">Литеральные закладки</span><span class="sxs-lookup"><span data-stu-id="4e1ec-611">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-612">ДБПРОП_ЛИТЕРАЛБУКМАРКС</span><span class="sxs-lookup"><span data-stu-id="4e1ec-612">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-613">Идентификация строк литералов</span><span class="sxs-lookup"><span data-stu-id="4e1ec-613">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-614">ДБПРОП_ЛИТЕРАЛИДЕНТИТИ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-614">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-615">Режим блокировки</span><span class="sxs-lookup"><span data-stu-id="4e1ec-615">Lock Mode</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-616">ДБПРОП_ЛОККМОДЕ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-616">DBPROP_LOCKMODE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-617">Максимальное число открытых строк</span><span class="sxs-lookup"><span data-stu-id="4e1ec-617">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-618">ДБПРОП_МАКСОПЕНРОВС</span><span class="sxs-lookup"><span data-stu-id="4e1ec-618">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-619">Максимальное число ожидающих строк</span><span class="sxs-lookup"><span data-stu-id="4e1ec-619">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-620">ДБПРОП_МАКСПЕНДИНГРОВС</span><span class="sxs-lookup"><span data-stu-id="4e1ec-620">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-621">Максимальное число строк</span><span class="sxs-lookup"><span data-stu-id="4e1ec-621">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-622">ДБПРОП_МАКСРОВС</span><span class="sxs-lookup"><span data-stu-id="4e1ec-622">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-623">Детализация уведомлений</span><span class="sxs-lookup"><span data-stu-id="4e1ec-623">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-624">ДБПРОП_НОТИФИКАТИОНГРАНУЛАРИТИ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-624">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-625">Этапы уведомления</span><span class="sxs-lookup"><span data-stu-id="4e1ec-625">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-626">ДБПРОП_НОТИФИКАТИОНФАСЕС</span><span class="sxs-lookup"><span data-stu-id="4e1ec-626">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-627">Объекты, транзакционные</span><span class="sxs-lookup"><span data-stu-id="4e1ec-627">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-628">ДБПРОП_ТРАНСАКТЕДОБЖЕКТ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-628">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-629">Видны другие изменения</span><span class="sxs-lookup"><span data-stu-id="4e1ec-629">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-630">ДБПРОП_ОСЕРУПДАТЕДЕЛЕТЕ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-630">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-631">Видимые вставки других пользователей</span><span class="sxs-lookup"><span data-stu-id="4e1ec-631">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-632">ДБПРОП_ОСЕРИНСЕРТ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-632">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-633">Видны изменения</span><span class="sxs-lookup"><span data-stu-id="4e1ec-633">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-634">ДБПРОП_ОВНУПДАТЕДЕЛЕТЕ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-634">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-635">Отображение собственных вставок</span><span class="sxs-lookup"><span data-stu-id="4e1ec-635">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-636">ДБПРОП_ОВНИНСЕРТ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-636">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-637">Сохранение при прерывании</span><span class="sxs-lookup"><span data-stu-id="4e1ec-637">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-638">ДБПРОП_АБОРТПРЕСЕРВЕ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-638">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-639">Сохранение при фиксации</span><span class="sxs-lookup"><span data-stu-id="4e1ec-639">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-640">ДБПРОП_КОММИТПРЕСЕРВЕ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-640">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-641">Быстрый перезапуск</span><span class="sxs-lookup"><span data-stu-id="4e1ec-641">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-642">ДБПРОП_КУИККРЕСТАРТ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-642">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-643">Повторные события</span><span class="sxs-lookup"><span data-stu-id="4e1ec-643">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-644">ДБПРОП_РИНТРАНТЕВЕНТС</span><span class="sxs-lookup"><span data-stu-id="4e1ec-644">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-645">Удаление удаленных строк</span><span class="sxs-lookup"><span data-stu-id="4e1ec-645">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-646">ДБПРОП_РЕМОВЕДЕЛЕТЕД</span><span class="sxs-lookup"><span data-stu-id="4e1ec-646">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-647">Отчет о нескольких изменениях</span><span class="sxs-lookup"><span data-stu-id="4e1ec-647">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-648">ДБПРОП_РЕПОРТМУЛТИПЛЕЧАНЖЕС</span><span class="sxs-lookup"><span data-stu-id="4e1ec-648">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-649">Возврат ожидающих вставок</span><span class="sxs-lookup"><span data-stu-id="4e1ec-649">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-650">ДБПРОП_РЕТУРНПЕНДИНГИНСЕРТС</span><span class="sxs-lookup"><span data-stu-id="4e1ec-650">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-651">Уведомление об удалении строки</span><span class="sxs-lookup"><span data-stu-id="4e1ec-651">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-652">ДБПРОП_НОТИФИРОВДЕЛЕТЕ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-652">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-653">Уведомление о первом изменении строки</span><span class="sxs-lookup"><span data-stu-id="4e1ec-653">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-654">ДБПРОП_НОТИФИРОВФИРСТЧАНЖЕ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-654">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-655">Уведомление о вставке строк</span><span class="sxs-lookup"><span data-stu-id="4e1ec-655">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-656">ДБПРОП_НОТИФИРОВИНСЕРТ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-656">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-657">Права на строки</span><span class="sxs-lookup"><span data-stu-id="4e1ec-657">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-658">ДБПРОП_РОВРЕСТРИКТ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-658">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-659">Уведомление о повторной синхронизации строк</span><span class="sxs-lookup"><span data-stu-id="4e1ec-659">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-660">ДБПРОП_НОТИФИРОВРЕСИНЧ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-660">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-661">Потоковая модель для строк</span><span class="sxs-lookup"><span data-stu-id="4e1ec-661">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-662">ДБПРОП_РОВСРЕАДМОДЕЛ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-662">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-663">Уведомление об отмене изменения строки</span><span class="sxs-lookup"><span data-stu-id="4e1ec-663">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-664">ДБПРОП_НОТИФИРОВУНДОЧАНЖЕ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-664">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-665">Уведомление о отмене удаления строки</span><span class="sxs-lookup"><span data-stu-id="4e1ec-665">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-666">ДБПРОП_НОТИФИРОВУНДОДЕЛЕТЕ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-666">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-667">Уведомление об отмене вставки строки</span><span class="sxs-lookup"><span data-stu-id="4e1ec-667">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-668">ДБПРОП_НОТИФИРОВУНДОИНСЕРТ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-668">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-669">Уведомление об обновлении строк</span><span class="sxs-lookup"><span data-stu-id="4e1ec-669">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-670">ДБПРОП_НОТИФИРОВУПДАТЕ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-670">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-671">Уведомление об изменении положения при получении набора строк</span><span class="sxs-lookup"><span data-stu-id="4e1ec-671">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-672">ДБПРОП_НОТИФИРОВСЕТФЕТЧПОСИТИОНЧАНЖЕ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-672">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-673">Уведомление о выПуске набора строк</span><span class="sxs-lookup"><span data-stu-id="4e1ec-673">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-674">ДБПРОП_НОТИФИРОВСЕТРЕЛЕАСЕ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-674">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-675">ПроКрутка назад</span><span class="sxs-lookup"><span data-stu-id="4e1ec-675">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-676">ДБПРОП_КАНСКРОЛЛБАККВАРДС</span><span class="sxs-lookup"><span data-stu-id="4e1ec-676">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-677">Данные сервера при вставке</span><span class="sxs-lookup"><span data-stu-id="4e1ec-677">Server Data on Insert</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-678">ДБПРОП_СЕРВЕРДАТАОНИНСЕРТ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-678">DBPROP_SERVERDATAONINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-679">Пропуск удаленных закладок</span><span class="sxs-lookup"><span data-stu-id="4e1ec-679">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-680">ДБПРОП_БУКМАРКСКИП</span><span class="sxs-lookup"><span data-stu-id="4e1ec-680">DBPROP_BOOKMARKSKIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-681">Строгая идентификация строк</span><span class="sxs-lookup"><span data-stu-id="4e1ec-681">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-682">ДБПРОП_СТРОНГИДЕНТИТИ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-682">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1ec-683">Обновление</span><span class="sxs-lookup"><span data-stu-id="4e1ec-683">Updatability</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-684">ДБПРОП_УПДАТАБИЛИТИ</span><span class="sxs-lookup"><span data-stu-id="4e1ec-684">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1ec-685">Использование закладок</span><span class="sxs-lookup"><span data-stu-id="4e1ec-685">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="4e1ec-686">ДБПРОП_БУКМАРКС</span><span class="sxs-lookup"><span data-stu-id="4e1ec-686">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="4e1ec-687">См. также</span><span class="sxs-lookup"><span data-stu-id="4e1ec-687">See also</span></span>

<span data-ttu-id="4e1ec-688">Для получения подробных сведений о реализации и функциональных сведений о поставщике OLE DB для Microsoft Jet обратитесь к документации по поставщику OLE DB для Microsoft Jet в пакете MDAC SDK.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-688">For specific implementation details and functional information about the OLE DB Provider for Microsoft Jet, consult the OLE DB Provider for Microsoft Jet documentation in the MDAC SDK.</span></span>

