---
title: Использование Microsoft Access в качестве сервера DDE
TOCTitle: Use Microsoft Access as a DDE Server
description: Microsoft Access поддерживает динамический обмен данными (DDE) как назначения (клиент) приложение или приложение источник (сервер).
ms:assetid: a3e82bf7-94b5-8eec-86bc-2d5387d66738
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821067(v=office.15)
ms:contentKeyID: 48546801
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5186349
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 0e22eb03571d51f28344f6d41fdcaa47321f67af
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870922"
---
# <a name="use-microsoft-access-as-a-dde-server"></a><span data-ttu-id="538b6-103">Использование Microsoft Access в качестве сервера DDE</span><span class="sxs-lookup"><span data-stu-id="538b6-103">Use Microsoft Access as a DDE server</span></span>

<span data-ttu-id="538b6-104">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="538b6-104">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="538b6-105">Microsoft Access поддерживает динамический обмен данными (DDE) как назначения (клиент) приложение или приложение источник (сервер).</span><span class="sxs-lookup"><span data-stu-id="538b6-105">Microsoft Access supports dynamic data exchange (DDE) as either a destination (client) application or a source (server) application.</span></span> <span data-ttu-id="538b6-106">Например приложения, например Microsoft Word, действующие в качестве клиента, можно запросить данных через DDE из базы данных Microsoft Access, который используется в качестве сервера.</span><span class="sxs-lookup"><span data-stu-id="538b6-106">For example, an application such as Microsoft Word, acting as a client, can request data through DDE from a Microsoft Access database that's acting as a server.</span></span>

> [!TIP]
> <span data-ttu-id="538b6-107">Если вам требуется для работы с Microsoft Access объекты из другого приложения, можно с помощью автоматизации.</span><span class="sxs-lookup"><span data-stu-id="538b6-107">If you need to manipulate Microsoft Access objects from another application, you may want to consider using Automation.</span></span>

<span data-ttu-id="538b6-108">DDE между клиентом и сервером устанавливается по определенной теме.</span><span class="sxs-lookup"><span data-stu-id="538b6-108">A DDE conversation between a client and server is established on a particular topic.</span></span> <span data-ttu-id="538b6-109">Раздел может быть данные файлов в формат, поддерживаемый серверное приложение, или она может быть темы системы, который предоставляет сведения о само приложение сервера.</span><span class="sxs-lookup"><span data-stu-id="538b6-109">A topic can be either a data file in the format supported by the server application, or it can be the System topic, which supplies information about the server application itself.</span></span> <span data-ttu-id="538b6-110">После начала беседы по определенной теме можно перенести только элемент данных, связанный с этой теме.</span><span class="sxs-lookup"><span data-stu-id="538b6-110">After a conversation has begun on a particular topic, only a data item associated with that topic can be transferred.</span></span>

<span data-ttu-id="538b6-111">Например предположим, выполняется Microsoft Word и для вставки данных из конкретной базы данных Microsoft Access в документ.</span><span class="sxs-lookup"><span data-stu-id="538b6-111">For example, suppose you are running Microsoft Word and want to insert data from a particular Microsoft Access database into a document.</span></span> <span data-ttu-id="538b6-112">Начните сеанс DDE с Microsoft Access с открытия канала DDE **отношением** , указав имя файла базы данных в разделе.</span><span class="sxs-lookup"><span data-stu-id="538b6-112">You begin a DDE conversation with Microsoft Access by opening a DDE channel with the **DDEInitiate** function and specifying the database file name as the topic.</span></span> <span data-ttu-id="538b6-113">Затем можно перенести данные из базы данных в Microsoft Word по этому каналу.</span><span class="sxs-lookup"><span data-stu-id="538b6-113">You can then transfer data from that database to Microsoft Word through that channel.</span></span>

<span data-ttu-id="538b6-114">Как сервер DDE Microsoft Access поддерживает следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="538b6-114">As a DDE server, Microsoft Access supports the following topics:</span></span>

- <span data-ttu-id="538b6-115">В разделе системы</span><span class="sxs-lookup"><span data-stu-id="538b6-115">The System topic</span></span>

- <span data-ttu-id="538b6-116">Имя базы данных (*базы данных* раздел)</span><span class="sxs-lookup"><span data-stu-id="538b6-116">The name of a database (*database* topic)</span></span>

- <span data-ttu-id="538b6-117">Имя таблицы (*tablename* раздел)</span><span class="sxs-lookup"><span data-stu-id="538b6-117">The name of a table (*tablename* topic)</span></span>

- <span data-ttu-id="538b6-118">Имя запроса (*имя запроса* раздел)</span><span class="sxs-lookup"><span data-stu-id="538b6-118">The name of a query (*queryname* topic)</span></span>

- <span data-ttu-id="538b6-119">Строка Microsoft Access SQL (*sqlstring* раздел)</span><span class="sxs-lookup"><span data-stu-id="538b6-119">A Microsoft Access SQL string (*sqlstring* topic)</span></span>

<span data-ttu-id="538b6-120">После установки вы сеанс DDE, оператор **DDEExecute** для отправки команду от клиента на сервер приложений.</span><span class="sxs-lookup"><span data-stu-id="538b6-120">After you've established a DDE conversation, you can use the **DDEExecute** statement to send a command from the client to the server application.</span></span> <span data-ttu-id="538b6-121">Если используется как сервер DDE, Microsoft Access распознает любое из указанных как действительный команду:</span><span class="sxs-lookup"><span data-stu-id="538b6-121">When used as a DDE server, Microsoft Access recognizes any of the following as a valid command:</span></span>

- <span data-ttu-id="538b6-122">Имя макроса в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="538b6-122">The name of a macro in the current database.</span></span>

- <span data-ttu-id="538b6-123">Все действия, которые можно выполнить в Visual Basic с помощью одного из методов **объекта** .</span><span class="sxs-lookup"><span data-stu-id="538b6-123">Any action that you can carry out in Visual Basic by using one of the methods of the **DoCmd** object.</span></span>

- <span data-ttu-id="538b6-124">OpenDatabase и CloseDatabase действия, которые используются только для операции DDE.</span><span class="sxs-lookup"><span data-stu-id="538b6-124">The OpenDatabase and CloseDatabase actions, which are used only for DDE operations.</span></span> <span data-ttu-id="538b6-125">(Пример использования этих действий, см. пример далее в этом разделе).</span><span class="sxs-lookup"><span data-stu-id="538b6-125">(For an example of how to use these actions, see the example later in this topic.)</span></span>

> [!NOTE]
> <span data-ttu-id="538b6-126">При указании действия макроса в качестве оператора **DDEExecute** действие и все аргументы синтаксис объекта **DoCmd** и должны заключаться в скобки ([]).</span><span class="sxs-lookup"><span data-stu-id="538b6-126">When you specify a macro action as a **DDEExecute** statement, the action and any arguments follow the **DoCmd** object syntax and must be enclosed in brackets ([ ]).</span></span> <span data-ttu-id="538b6-127">Тем не менее приложения, поддерживающие DDE не распознает встроенные константы в операции DDE.</span><span class="sxs-lookup"><span data-stu-id="538b6-127">However, applications that support DDE don't recognize intrinsic constants in DDE operations.</span></span> <span data-ttu-id="538b6-128">Кроме того, строковые аргументы должны заключаться в кавычки (» «) Если строка содержит их запятыми.</span><span class="sxs-lookup"><span data-stu-id="538b6-128">Also, string arguments must be enclosed in quotation marks (" ") if the string contains a comma.</span></span> <span data-ttu-id="538b6-129">В противном случае кавычки, не являются обязательными.</span><span class="sxs-lookup"><span data-stu-id="538b6-129">Otherwise, quotation marks aren't required.</span></span>

<span data-ttu-id="538b6-130">Клиентское приложение можно использовать функцию **DDERequest** к данным текст запроса из приложения сервера по каналу DDE open.</span><span class="sxs-lookup"><span data-stu-id="538b6-130">The client application can use the **DDERequest** function to request text data from the server application over an open DDE channel.</span></span> <span data-ttu-id="538b6-131">Или клиент может использовать оператор **DDEPoke** для отправки данных в серверное приложение.</span><span class="sxs-lookup"><span data-stu-id="538b6-131">Or the client can use the **DDEPoke** statement to send data to the server application.</span></span> <span data-ttu-id="538b6-132">По завершении передачи данных клиент может использовать оператор **DDETerminate** для закрытия канала DDE или оператор **DDETerminateAll** , чтобы закрыть все открытые каналы.</span><span class="sxs-lookup"><span data-stu-id="538b6-132">After the data transfer is complete, the client can use the **DDETerminate** statement to close the DDE channel, or the **DDETerminateAll** statement to close all open channels.</span></span>

> [!NOTE]
> <span data-ttu-id="538b6-133">По завершении клиентское приложение получает данные по каналу DDE, его следует закрыть канала для сохранения ресурсов памяти.</span><span class="sxs-lookup"><span data-stu-id="538b6-133">When your client application has finished receiving data over a DDE channel, it should close that channel to conserve memory resources.</span></span>

<span data-ttu-id="538b6-134">Следующий пример демонстрирует создание процедуры Microsoft Word с помощью Visual Basic, который использует Microsoft Access, что сервер DDE.</span><span class="sxs-lookup"><span data-stu-id="538b6-134">The following example demonstrates how to create a Microsoft Word procedure with Visual Basic that uses Microsoft Access as a DDE server.</span></span> <span data-ttu-id="538b6-135">(В данном примере для работы Microsoft Access должен работать под управлением.)</span><span class="sxs-lookup"><span data-stu-id="538b6-135">(For this example to work, Microsoft Access must be running.)</span></span>

```vb
    Sub AccessDDE() 
        Dim intChan1 As Integer, intChan2 As Integer 
        Dim strQueryData As String 
     
        ' Use System topic to open Northwind sample database. 
        ' Database must be open before using other DDE topics. 
        intChan1 = DDEInitiate("MSAccess", "System") 
        ' You may need to change this path to point to actual location 
        ' of Northwind sample database. 
        DDEExecute intChan1, "[OpenDatabase C:\Access\Samples\Northwind.mdb]" 
     
        ' Get all data from Ten Most Expensive Products query. 
        intChan2 = DDEInitiate("MSAccess", "Northwind.mdb;" _ 
            & "QUERY Ten Most Expensive Products") 
        strQueryData = DDERequest(intChan2, "All") 
        DDETerminate intChan2 
     
        ' Close database. 
        DDEExecute intChan1, "[CloseDatabase]" 
        DDETerminate intChan1 
     
        ' Print retrieved data to Debug Window. 
        Debug.Print strQueryData 
    End Sub
```

<br/>

<span data-ttu-id="538b6-136">В следующих разделах сведения по темам допустимый DDE, поддерживаются в Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="538b6-136">The following sections provide information about the valid DDE topics supported by Microsoft Access.</span></span>

## <a name="the-system-topic"></a><span data-ttu-id="538b6-137">В разделе системы</span><span class="sxs-lookup"><span data-stu-id="538b6-137">The System topic</span></span>

<span data-ttu-id="538b6-138">В разделе система — это стандартный раздел для всех приложений на основе Windows Microsoft.</span><span class="sxs-lookup"><span data-stu-id="538b6-138">The System topic is a standard topic for all Microsoft Windows–based applications.</span></span> <span data-ttu-id="538b6-139">Она предоставляет сведения по темам, поддерживаемых приложением.</span><span class="sxs-lookup"><span data-stu-id="538b6-139">It supplies information about the other topics supported by the application.</span></span> <span data-ttu-id="538b6-140">Для доступа к этой информации, код должен сначала вызвать \*\*отношением с аргументом *раздел* \*\* и выполните оператор **DDERequest** с одним из следующих действий, предоставленных для аргумента *элемента* .</span><span class="sxs-lookup"><span data-stu-id="538b6-140">To access this information, your code must first call the **DDEInitiate** function with the *topic* argument, and then execute the **DDERequest** statement with one of the following supplied for the *item* argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="538b6-141">Item</span><span class="sxs-lookup"><span data-stu-id="538b6-141">Item</span></span></p></th>
<th><p><span data-ttu-id="538b6-142">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="538b6-142">Returns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="538b6-143">SysItems</span><span class="sxs-lookup"><span data-stu-id="538b6-143">SysItems</span></span></p></td>
<td><p><span data-ttu-id="538b6-144">Список элементов, поддерживаемых в разделе система Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="538b6-144">A list of items supported by the System topic in Microsoft Access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="538b6-145">Formats</span><span class="sxs-lookup"><span data-stu-id="538b6-145">Formats</span></span></p></td>
<td><p><span data-ttu-id="538b6-146">Список форматов Microsoft Access можно скопировать в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="538b6-146">A list of the formats Microsoft Access can copy onto the Clipboard.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="538b6-147">Status</span><span class="sxs-lookup"><span data-stu-id="538b6-147">Status</span></span></p></td>
<td><p><span data-ttu-id="538b6-148">&quot;«Занят»&quot; или &quot;готовы&quot;.</span><span class="sxs-lookup"><span data-stu-id="538b6-148">&quot;Busy&quot; or &quot;Ready&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="538b6-149">Разделы</span><span class="sxs-lookup"><span data-stu-id="538b6-149">Topics</span></span></p></td>
<td><p><span data-ttu-id="538b6-150">Список всех открытых баз данных.</span><span class="sxs-lookup"><span data-stu-id="538b6-150">A list of all open databases.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="538b6-151">В следующем примере показано использование функции **DDEInitiate** и **DDERequest** с разделом системы:</span><span class="sxs-lookup"><span data-stu-id="538b6-151">The following example demonstrates the use of the **DDEInitiate** and **DDERequest** functions with the System topic:</span></span>

```vb
    ' In Visual Basic, initiate DDE conversation with Microsoft Access. 
    Dim intChan1 As Integer, strResults As String 
    intChan1 = DDEInitiate("MSAccess", "System") 
    ' Request list of topics supported by System topic. 
    strResults = DDERequest(intChan1, "SysItems") 
    ' Run OpenDatabase action to open Northwind.mdb. 
    ' You may need to change this path to point to actual location 
    ' of Northwind sample database. 
    DDEExecute intChan1, "[OpenDatabase C:\Access\Samples\Northwind.mdb]"
```

## <a name="the-database-topic"></a><span data-ttu-id="538b6-152">В разделе базы данных</span><span class="sxs-lookup"><span data-stu-id="538b6-152">The database topic</span></span>

<span data-ttu-id="538b6-153">В разделе *базы данных* — это имя файла существующей базы данных.</span><span class="sxs-lookup"><span data-stu-id="538b6-153">The *database* topic is the file name of an existing database.</span></span> <span data-ttu-id="538b6-154">Можно ввести только что базовое имя (Northwind) или его путь к MDB- и расширение (C:\\доступа\\примеры\\Northwind.mdb).</span><span class="sxs-lookup"><span data-stu-id="538b6-154">You can type either just the base name (Northwind), or its path and .mdb extension (C:\\Access\\Samples\\Northwind.mdb).</span></span> <span data-ttu-id="538b6-155">Начав сеанс DDE с базой данных, можно запросить список объектов в этой базе данных.</span><span class="sxs-lookup"><span data-stu-id="538b6-155">After you start a DDE conversation with the database, you can request a list of the objects in that database.</span></span>

> [!NOTE]
> <span data-ttu-id="538b6-156">Нельзя использовать DDE для запроса файл рабочей группы Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="538b6-156">You can't use DDE to query the Microsoft Access workgroup information file.</span></span>

<span data-ttu-id="538b6-157">В разделе *База данных* поддерживает следующие элементы.</span><span class="sxs-lookup"><span data-stu-id="538b6-157">The *database* topic supports the following items.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="538b6-158">Item</span><span class="sxs-lookup"><span data-stu-id="538b6-158">Item</span></span></p></th>
<th><p><span data-ttu-id="538b6-159">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="538b6-159">Returns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="538b6-160">TableList</span><span class="sxs-lookup"><span data-stu-id="538b6-160">TableList</span></span></p></td>
<td><p><span data-ttu-id="538b6-161">Список таблиц</span><span class="sxs-lookup"><span data-stu-id="538b6-161">A list of tables</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="538b6-162">QueryList</span><span class="sxs-lookup"><span data-stu-id="538b6-162">QueryList</span></span></p></td>
<td><p><span data-ttu-id="538b6-163">Список запросов</span><span class="sxs-lookup"><span data-stu-id="538b6-163">A list of queries</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="538b6-164">FormList</span><span class="sxs-lookup"><span data-stu-id="538b6-164">FormList</span></span></p></td>
<td><p><span data-ttu-id="538b6-165">Список форм</span><span class="sxs-lookup"><span data-stu-id="538b6-165">A list of forms</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="538b6-166">ReportList</span><span class="sxs-lookup"><span data-stu-id="538b6-166">ReportList</span></span></p></td>
<td><p><span data-ttu-id="538b6-167">Список отчетов</span><span class="sxs-lookup"><span data-stu-id="538b6-167">A list of reports</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="538b6-168">MacroList</span><span class="sxs-lookup"><span data-stu-id="538b6-168">MacroList</span></span></p></td>
<td><p><span data-ttu-id="538b6-169">Список макросов</span><span class="sxs-lookup"><span data-stu-id="538b6-169">A list of macros</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="538b6-170">ModuleList</span><span class="sxs-lookup"><span data-stu-id="538b6-170">ModuleList</span></span></p></td>
<td><p><span data-ttu-id="538b6-171">Список модулей</span><span class="sxs-lookup"><span data-stu-id="538b6-171">A list of modules</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="538b6-172">ViewList</span><span class="sxs-lookup"><span data-stu-id="538b6-172">ViewList</span></span></p></td>
<td><p><span data-ttu-id="538b6-173">Список представлений</span><span class="sxs-lookup"><span data-stu-id="538b6-173">A list of views</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="538b6-174">StoredProcedureList</span><span class="sxs-lookup"><span data-stu-id="538b6-174">StoredProcedureList</span></span></p></td>
<td><p><span data-ttu-id="538b6-175">Список хранимых процедур</span><span class="sxs-lookup"><span data-stu-id="538b6-175">A list of stored procedures</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="538b6-176">DatabaseDiagramList</span><span class="sxs-lookup"><span data-stu-id="538b6-176">DatabaseDiagramList</span></span></p></td>
<td><p><span data-ttu-id="538b6-177">Список схемы базы данных</span><span class="sxs-lookup"><span data-stu-id="538b6-177">A list of database diagrams</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="538b6-178">В следующем примере показано, как сотрудники форму можно открыть в образце базы данных Northwind из процедуры Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="538b6-178">The following example shows how you can open the Employees form in the Northwind sample database from a Visual Basic procedure:</span></span>

```vb
    ' In Visual Basic, initiate DDE conversation with 
    ' Northwind sample database. 
    ' Make sure database is open. 
    intChan2 = DDEInitiate("MSAccess", "Northwind") 
    ' Request list of forms in Northwind sample database. 
    strResponse = DDERequest(intChan2, "FormList") 
    ' Run OpenForm action and arguments to open Employees form. 
    DDEExecute intChan2, "[OpenForm Employees,0,,,1,0]"
```

## <a name="the-table-topic"></a><span data-ttu-id="538b6-179">В разделе таблицы</span><span class="sxs-lookup"><span data-stu-id="538b6-179">The TABLE topic</span></span>

<span data-ttu-id="538b6-180">В этих разделах используйте следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="538b6-180">These topics use the following syntax:</span></span>

<span data-ttu-id="538b6-181">_имя базы данных_ ; **В ТАБЛИЦЕ** _TableName_</span><span class="sxs-lookup"><span data-stu-id="538b6-181">_databasename_ ; **TABLE** _tablename_</span></span>

<span data-ttu-id="538b6-182">_имя базы данных_ ; **Запрос** _имя запроса_</span><span class="sxs-lookup"><span data-stu-id="538b6-182">_databasename_ ; **QUERY** _queryname_</span></span>

<span data-ttu-id="538b6-183">_имя базы данных_ ; **SQL** [ _sqlstring_ ]</span><span class="sxs-lookup"><span data-stu-id="538b6-183">_databasename_ ; **SQL** [ _sqlstring_ ]</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="538b6-184">Часть</span><span class="sxs-lookup"><span data-stu-id="538b6-184">Part</span></span></p></th>
<th><p><span data-ttu-id="538b6-185">Описание</span><span class="sxs-lookup"><span data-stu-id="538b6-185">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="538b6-186"><em>Имя базы данных</em></span><span class="sxs-lookup"><span data-stu-id="538b6-186"><em>databasename</em></span></span></p></td>
<td><p><span data-ttu-id="538b6-187">Имя базы данных, таблицы или запроса или, которое применяется инструкции SQL, а затем точка с запятой (;).</span><span class="sxs-lookup"><span data-stu-id="538b6-187">The name of the database that the table or query is in or that the SQL statement applies to, followed by a semicolon (;).</span></span> <span data-ttu-id="538b6-188">Имя базы данных может быть только что базовое имя (Northwind) или его полный путь к MDB- и расширение (C:\Access\Samples\Northwind.mdb).</span><span class="sxs-lookup"><span data-stu-id="538b6-188">The database name can be just the base name (Northwind) or its full path and .mdb extension (C:\Access\Samples\Northwind.mdb).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="538b6-189"><em>TableName</em></span><span class="sxs-lookup"><span data-stu-id="538b6-189"><em>tablename</em></span></span></p></td>
<td><p><span data-ttu-id="538b6-190">Имя существующей таблицы.</span><span class="sxs-lookup"><span data-stu-id="538b6-190">The name of an existing table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="538b6-191"><em>Имя запроса</em></span><span class="sxs-lookup"><span data-stu-id="538b6-191"><em>queryname</em></span></span></p></td>
<td><p><span data-ttu-id="538b6-192">Имя существующего запроса.</span><span class="sxs-lookup"><span data-stu-id="538b6-192">The name of an existing query.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="538b6-193"><em>SqlString</em></span><span class="sxs-lookup"><span data-stu-id="538b6-193"><em>sqlstring</em></span></span></p></td>
<td><p><span data-ttu-id="538b6-194">Допустимая инструкция SQL не должна превышать 256 знаков, конечные точки с запятой.</span><span class="sxs-lookup"><span data-stu-id="538b6-194">A valid SQL statement up to 256 characters long, ending with a semicolon.</span></span> <span data-ttu-id="538b6-195">Exchange более 256 символов, определяющее и вместо использования последовательных <strong>DDEPoke</strong> операторов для создания инструкции SQL.</span><span class="sxs-lookup"><span data-stu-id="538b6-195">To exchange more than 256 characters, omit this argument and instead use successive <strong>DDEPoke</strong> statements to build an SQL statement.</span></span> <span data-ttu-id="538b6-196">Например следующий код Visual Basic используется оператор <strong>DDEPoke</strong> построение инструкции SQL и затем запросить результаты запроса.</span><span class="sxs-lookup"><span data-stu-id="538b6-196">For example, the following Visual Basic code uses the <strong>DDEPoke</strong> statement to build an SQL statement and then request the results of the query.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="538b6-197">В следующей таблице перечислены допустимые элементы для таблицы *tablename*, ЗАПРОСА *имя запроса*и разделы *sqlstring* SQL.</span><span class="sxs-lookup"><span data-stu-id="538b6-197">The following table lists the valid items for the TABLE *tablename*, QUERY *queryname*, and SQL *sqlstring* topics.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="538b6-198">Item</span><span class="sxs-lookup"><span data-stu-id="538b6-198">Item</span></span></p></th>
<th><p><span data-ttu-id="538b6-199">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="538b6-199">Returns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="538b6-200">Все</span><span class="sxs-lookup"><span data-stu-id="538b6-200">All</span></span></p></td>
<td><p><span data-ttu-id="538b6-201">Все данные в таблице, в том числе имена полей.</span><span class="sxs-lookup"><span data-stu-id="538b6-201">All the data in the table, including field names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="538b6-202">Data</span><span class="sxs-lookup"><span data-stu-id="538b6-202">Data</span></span></p></td>
<td><p><span data-ttu-id="538b6-203">Все строки данных без имена полей.</span><span class="sxs-lookup"><span data-stu-id="538b6-203">All rows of data, without field names.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="538b6-204">Списке FieldNames</span><span class="sxs-lookup"><span data-stu-id="538b6-204">FieldNames</span></span></p></td>
<td><p><span data-ttu-id="538b6-205">Однострочный список имен полей.</span><span class="sxs-lookup"><span data-stu-id="538b6-205">A single-row list of field names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="538b6-206">В списке FieldNames; T</span><span class="sxs-lookup"><span data-stu-id="538b6-206">FieldNames;T</span></span></p></td>
<td><p><span data-ttu-id="538b6-207">Список полей двух строк имен (первой строки) и их данных типов (вторая строка).</span><span class="sxs-lookup"><span data-stu-id="538b6-207">A two-row list of field names (first row) and their data types (second row).</span></span></p>
<p><span data-ttu-id="538b6-208">Ниже приведены возвращаемые значения:</span><span class="sxs-lookup"><span data-stu-id="538b6-208">These are the values returned:</span></span></p>
<p><span data-ttu-id="538b6-209">Значение</span><span class="sxs-lookup"><span data-stu-id="538b6-209">Value</span></span></p>
<p><ul>
<li><span data-ttu-id="538b6-210">0</span><span class="sxs-lookup"><span data-stu-id="538b6-210">0</span></span></li>
<li><span data-ttu-id="538b6-211">1</span><span class="sxs-lookup"><span data-stu-id="538b6-211">1</span></span></li>
<li><span data-ttu-id="538b6-212">2</span><span class="sxs-lookup"><span data-stu-id="538b6-212">2</span></span></li>
<li><span data-ttu-id="538b6-213">3</span><span class="sxs-lookup"><span data-stu-id="538b6-213">3</span></span></li>
<li><span data-ttu-id="538b6-214">4</span><span class="sxs-lookup"><span data-stu-id="538b6-214">4</span></span></li>
<li><span data-ttu-id="538b6-215">5</span><span class="sxs-lookup"><span data-stu-id="538b6-215">5</span></span></li>
<li><span data-ttu-id="538b6-216">6</span><span class="sxs-lookup"><span data-stu-id="538b6-216">6</span></span></li>
<li><span data-ttu-id="538b6-217">7</span><span class="sxs-lookup"><span data-stu-id="538b6-217">7</span></span></li>
<li><span data-ttu-id="538b6-218">8</span><span class="sxs-lookup"><span data-stu-id="538b6-218">8</span></span></li>
<li><span data-ttu-id="538b6-219">9</span><span class="sxs-lookup"><span data-stu-id="538b6-219">9</span></span></li>
<li><span data-ttu-id="538b6-220">10</span><span class="sxs-lookup"><span data-stu-id="538b6-220">10</span></span></li>
<li><span data-ttu-id="538b6-221">11</span><span class="sxs-lookup"><span data-stu-id="538b6-221">11</span></span></li>
<li><span data-ttu-id="538b6-222">12</span><span class="sxs-lookup"><span data-stu-id="538b6-222">12</span></span></li>
</ul>
</p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="538b6-223">NextRow</span><span class="sxs-lookup"><span data-stu-id="538b6-223">NextRow</span></span></p></td>
<td><p><span data-ttu-id="538b6-224">Данные в следующей строке таблицы или запроса.</span><span class="sxs-lookup"><span data-stu-id="538b6-224">The data in the next row in the table or query.</span></span> <span data-ttu-id="538b6-225">При открытии канала NextRow возвращает данные в первой строке.</span><span class="sxs-lookup"><span data-stu-id="538b6-225">When you open a channel, NextRow returns the data in the first row.</span></span> <span data-ttu-id="538b6-226">Если текущей строки последней записи и запустите NextRow, запрос не выполняется.</span><span class="sxs-lookup"><span data-stu-id="538b6-226">If the current row is the last record and you run NextRow, the request fails.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="538b6-227">PrevRow</span><span class="sxs-lookup"><span data-stu-id="538b6-227">PrevRow</span></span></p></td>
<td><p><span data-ttu-id="538b6-228">Данные в предыдущей строки в таблице или запросе.</span><span class="sxs-lookup"><span data-stu-id="538b6-228">The data in the previous row in the table or query.</span></span> <span data-ttu-id="538b6-229">Если PrevRow первый запрос на новый канал, возвращаются данные в последней строке таблицы или запроса.</span><span class="sxs-lookup"><span data-stu-id="538b6-229">If PrevRow is the first request on a new channel, the data in the last row of the table or query is returned.</span></span> <span data-ttu-id="538b6-230">Если первая запись текущей строки, не удается выполнить запрос для PrevRow.</span><span class="sxs-lookup"><span data-stu-id="538b6-230">If the first record is the current row, the request for PrevRow fails.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="538b6-231">FirstRow</span><span class="sxs-lookup"><span data-stu-id="538b6-231">FirstRow</span></span></p></td>
<td><p><span data-ttu-id="538b6-232">Данные в первой строке таблицы или запроса.</span><span class="sxs-lookup"><span data-stu-id="538b6-232">The data in the first row of the table or query.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="538b6-233">LastRow</span><span class="sxs-lookup"><span data-stu-id="538b6-233">LastRow</span></span></p></td>
<td><p><span data-ttu-id="538b6-234">Данные в последней строке таблицы или запроса.</span><span class="sxs-lookup"><span data-stu-id="538b6-234">The data in the last row of the table or query.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="538b6-235">FieldCount</span><span class="sxs-lookup"><span data-stu-id="538b6-235">FieldCount</span></span></p></td>
<td><p><span data-ttu-id="538b6-236">Количество полей в таблице или запросе.</span><span class="sxs-lookup"><span data-stu-id="538b6-236">The number of fields in the table or query.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="538b6-237">SQLText</span><span class="sxs-lookup"><span data-stu-id="538b6-237">SQLText</span></span></p></td>
<td><p><span data-ttu-id="538b6-238">Инструкция SQL, представляющий таблицы или запроса.</span><span class="sxs-lookup"><span data-stu-id="538b6-238">An SQL statement representing the table or query.</span></span> <span data-ttu-id="538b6-239">Для таблиц, то возвращается инструкции SQL в виде &quot;ВЫБЕРИТЕ `*` из <em>таблицы</em>; &quot;.</span><span class="sxs-lookup"><span data-stu-id="538b6-239">For tables, this item returns an SQL statement in the form &quot;SELECT `*` FROM <em>table</em>;&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="538b6-240">SQLText; <em>n</em></span><span class="sxs-lookup"><span data-stu-id="538b6-240">SQLText;<em>n</em></span></span></p></td>
<td><p><span data-ttu-id="538b6-241">Инструкции SQL в <em>n</em>-блоки, представляющие таблицы или запроса, где <em>n</em> — целое число до 256 символов.</span><span class="sxs-lookup"><span data-stu-id="538b6-241">An SQL statement, in <em>n</em>-character chunks, representing the table or query, where <em>n</em> is an integer up to 256.</span></span> <span data-ttu-id="538b6-242">Предположим, например, представляется с помощью следующей инструкции SQL: элемента &quot;SQLText; 7&quot; возвращает следующие блоки разделители — знаки табуляции: элемента &quot;SQLText; 7&quot; возвращает следующие блоки разделители — знаки табуляции:</span><span class="sxs-lookup"><span data-stu-id="538b6-242">For example, suppose a query is represented by the following SQL statement: The item &quot;SQLText;7&quot; returns the following tab-delimited chunks: The item &quot;SQLText;7&quot; returns the following tab-delimited chunks:</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="538b6-243">В следующем примере показано, как использовать DDE в процедуре Visual Basic для запроса данных из таблицы в образце базы данных Northwind и вставить эти данные в текстовый файл:</span><span class="sxs-lookup"><span data-stu-id="538b6-243">The following example shows how you can use DDE in a Visual Basic procedure to request data from a table in the Northwind sample database and insert that data into a text file:</span></span>

```vb
    Sub NorthwindDDE 
        Dim intChan1 As Integer, intChan2 As Integer, intChan3 As Integer 
        Dim strResp1 As Variant, strResp2 As Variant, strResp3 As Variant 
     
        ' In a Visual Basic module, get data from Categories table, 
        ' Catalog query, and Orders table in Northwind.mdb. 
        ' Make sure database is open first. 
        intChan1 = DDEInitiate("MSAccess", "Northwind;TABLE Shippers") 
        intChan2 = DDEInitiate("MSAccess", "Northwind;QUERY Catalog") 
        intChan3 = DDEInitiate("MSAccess", "Northwind;SQL SELECT * " _ 
            & "FROM Orders " _ 
            & "WHERE OrderID > 10050;") 
     
        strResp1 = DDERequest(intChan1, "All") 
        strResp2 = DDERequest(intChan2, "FieldNames;T") 
        strResp3 = DDERequest(intChan3, "FieldNames;T") 
        DDETerminate intChan1 
        DDETerminate intChan2 
        DDETerminate intChan3 
     
        ' Insert data into text file. 
        Open "C:\DATA.TXT" For Append As #1 
        Print #1, strResp1 
        Print #1, strResp2 
        Print #1, strResp3 
        Close #1 
    End Sub
```
