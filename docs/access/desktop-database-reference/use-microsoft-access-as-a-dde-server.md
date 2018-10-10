---
title: Использовать Microsoft Access в качестве сервера DDE
TOCTitle: Use Microsoft Access as a DDE Server
ms:assetid: a3e82bf7-94b5-8eec-86bc-2d5387d66738
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821067(v=office.15)
ms:contentKeyID: 48546801
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5186349
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 84b4e30877488d84e03839764c1996053e76a2e7
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482306"
---
# <a name="use-microsoft-access-as-a-dde-server"></a><span data-ttu-id="b8b9d-102">Использовать Microsoft Access в качестве сервера DDE</span><span class="sxs-lookup"><span data-stu-id="b8b9d-102">Use Microsoft Access as a DDE server</span></span>

<span data-ttu-id="b8b9d-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b8b9d-103">**Applies to**: Access 2013 | Office 2013</span></span> 

<span data-ttu-id="b8b9d-104">Microsoft Access поддерживает динамический обмен данными (DDE) как назначения (клиент) приложение или приложение источник (сервер).</span><span class="sxs-lookup"><span data-stu-id="b8b9d-104">Microsoft Access supports dynamic data exchange (DDE) as either a destination (client) application or a source (server) application.</span></span> <span data-ttu-id="b8b9d-105">Например приложения, например Microsoft Word, действующие в качестве клиента, можно запросить данных через DDE из базы данных Microsoft Access, который используется в качестве сервера.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-105">For example, an application such as Microsoft Word, acting as a client, can request data through DDE from a Microsoft Access database that's acting as a server.</span></span>

> [!TIP]
> <span data-ttu-id="b8b9d-106">Если вам требуется для работы с Microsoft Access объекты из другого приложения, можно с помощью автоматизации.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-106">If you need to manipulate Microsoft Access objects from another application, you may want to consider using Automation.</span></span>

<span data-ttu-id="b8b9d-107">DDE между клиентом и сервером устанавливается по определенной теме.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-107">A DDE conversation between a client and server is established on a particular topic.</span></span> <span data-ttu-id="b8b9d-108">Раздел может быть данные файлов в формат, поддерживаемый серверное приложение, или она может быть темы системы, который предоставляет сведения о само приложение сервера.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-108">A topic can be either a data file in the format supported by the server application, or it can be the System topic, which supplies information about the server application itself.</span></span> <span data-ttu-id="b8b9d-109">После начала беседы по определенной теме можно перенести только элемент данных, связанный с этой теме.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-109">Once a conversation has begun on a particular topic, only a data item associated with that topic can be transferred.</span></span>

<span data-ttu-id="b8b9d-110">Например предположим, выполняется Microsoft Word и для вставки данных из конкретной базы данных Microsoft Access в документ.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-110">For example, suppose you are running Microsoft Word and want to insert data from a particular Microsoft Access database into a document.</span></span> <span data-ttu-id="b8b9d-111">Начните сеанс DDE с Microsoft Access с открытия канала DDE **отношением** , указав имя файла базы данных в разделе.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-111">You begin a DDE conversation with Microsoft Access by opening a DDE channel with the **DDEInitiate** function and specifying the database file name as the topic.</span></span> <span data-ttu-id="b8b9d-112">Затем можно перенести данные из базы данных в Microsoft Word по этому каналу.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-112">You can then transfer data from that database to Microsoft Word through that channel.</span></span>

<span data-ttu-id="b8b9d-113">Как сервер DDE Microsoft Access поддерживает следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="b8b9d-113">As a DDE server, Microsoft Access supports the following topics:</span></span>

  - <span data-ttu-id="b8b9d-114">В разделе системы</span><span class="sxs-lookup"><span data-stu-id="b8b9d-114">The System topic</span></span>

  - <span data-ttu-id="b8b9d-115">Имя базы данных (*базы данных* раздел)</span><span class="sxs-lookup"><span data-stu-id="b8b9d-115">The name of a database (*database* topic)</span></span>

  - <span data-ttu-id="b8b9d-116">Имя таблицы (*tablename* раздел)</span><span class="sxs-lookup"><span data-stu-id="b8b9d-116">The name of a table (*tablename* topic)</span></span>

  - <span data-ttu-id="b8b9d-117">Имя запроса (*имя запроса* раздел)</span><span class="sxs-lookup"><span data-stu-id="b8b9d-117">The name of a query (*queryname* topic)</span></span>

  - <span data-ttu-id="b8b9d-118">Строка Microsoft Access SQL (*sqlstring* раздел)</span><span class="sxs-lookup"><span data-stu-id="b8b9d-118">A Microsoft Access SQL string (*sqlstring* topic)</span></span>

<span data-ttu-id="b8b9d-119">Если установлено сеанс DDE, оператор **DDEExecute** для отправки команду от клиента на сервер приложений.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-119">Once you've established a DDE conversation, you can use the **DDEExecute** statement to send a command from the client to the server application.</span></span> <span data-ttu-id="b8b9d-120">Если используется как сервер DDE, Microsoft Access распознает любое из указанных как действительный команду:</span><span class="sxs-lookup"><span data-stu-id="b8b9d-120">When used as a DDE server, Microsoft Access recognizes any of the following as a valid command:</span></span>

  - <span data-ttu-id="b8b9d-121">Имя макроса в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-121">The name of a macro in the current database.</span></span>

  - <span data-ttu-id="b8b9d-122">Все действия, которые можно выполнить в Visual Basic с помощью одного из методов **объекта** .</span><span class="sxs-lookup"><span data-stu-id="b8b9d-122">Any action that you can carry out in Visual Basic by using one of the methods of the **DoCmd** object.</span></span>

  - <span data-ttu-id="b8b9d-123">OpenDatabase и CloseDatabase действия, которые используются только для операции DDE.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-123">The OpenDatabase and CloseDatabase actions, which are used only for DDE operations.</span></span> <span data-ttu-id="b8b9d-124">(Пример использования этих действий, см. пример далее в этом разделе).</span><span class="sxs-lookup"><span data-stu-id="b8b9d-124">(For an example of how to use these actions, see the example later in this topic.)</span></span>


> [!NOTE]
> <P><span data-ttu-id="b8b9d-125">При указании действия макроса в качестве оператора <STRONG>DDEExecute</STRONG> действие и все аргументы синтаксис объекта <STRONG>DoCmd</STRONG> и должны заключаться в скобки ([]).</span><span class="sxs-lookup"><span data-stu-id="b8b9d-125">When you specify a macro action as a <STRONG>DDEExecute</STRONG> statement, the action and any arguments follow the <STRONG>DoCmd</STRONG> object syntax and must be enclosed in brackets ([ ]).</span></span> <span data-ttu-id="b8b9d-126">Тем не менее приложения, поддерживающие DDE не распознает встроенные константы в операции DDE.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-126">However, applications that support DDE don't recognize intrinsic constants in DDE operations.</span></span> <span data-ttu-id="b8b9d-127">Кроме того, строковые аргументы должны заключаться в кавычки (» «) Если строка содержит их запятыми.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-127">Also, string arguments must be enclosed in quotation marks (" ") if the string contains a comma.</span></span> <span data-ttu-id="b8b9d-128">В противном случае кавычки, не являются обязательными.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-128">Otherwise, quotation marks aren't required.</span></span></P>



<span data-ttu-id="b8b9d-129">Клиентское приложение можно использовать функцию **DDERequest** к данным текст запроса из приложения сервера по каналу DDE open.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-129">The client application can use the **DDERequest** function to request text data from the server application over an open DDE channel.</span></span> <span data-ttu-id="b8b9d-130">Или клиент может использовать оператор **DDEPoke** для отправки данных в серверное приложение.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-130">Or the client can use the **DDEPoke** statement to send data to the server application.</span></span> <span data-ttu-id="b8b9d-131">По завершении передачи данных клиент может использовать оператор **DDETerminate** для закрытия канала DDE или оператор **DDETerminateAll** , чтобы закрыть все открытые каналы.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-131">Once the data transfer is complete, the client can use the **DDETerminate** statement to close the DDE channel, or the **DDETerminateAll** statement to close all open channels.</span></span>


> [!NOTE]
> <P><span data-ttu-id="b8b9d-132">По завершении клиентское приложение получает данные по каналу DDE, его следует закрыть канала для сохранения ресурсов памяти.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-132">When your client application has finished receiving data over a DDE channel, it should close that channel to conserve memory resources.</span></span></P>



<span data-ttu-id="b8b9d-133">Следующий пример демонстрирует создание процедуры Microsoft Word с помощью Visual Basic, который использует Microsoft Access, что сервер DDE.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-133">The following example demonstrates how to create a Microsoft Word procedure with Visual Basic that uses Microsoft Access as a DDE server.</span></span> <span data-ttu-id="b8b9d-134">(В данном примере для работы Microsoft Access должен работать под управлением.)</span><span class="sxs-lookup"><span data-stu-id="b8b9d-134">(For this example to work, Microsoft Access must be running.)</span></span>

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

<span data-ttu-id="b8b9d-135">В следующих разделах сведения по темам допустимый DDE, поддерживаются в Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-135">The following sections provide information about the valid DDE topics supported by Microsoft Access.</span></span>

## <a name="the-system-topic"></a><span data-ttu-id="b8b9d-136">В разделе системы</span><span class="sxs-lookup"><span data-stu-id="b8b9d-136">The System topic</span></span>

<span data-ttu-id="b8b9d-137">В разделе система — это стандартный раздел для всех приложений на основе Windows Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-137">The System topic is a standard topic for all Microsoft Windows–based applications.</span></span> <span data-ttu-id="b8b9d-138">Она предоставляет сведения по темам, поддерживаемых приложением.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-138">It supplies information about the other topics supported by the application.</span></span> <span data-ttu-id="b8b9d-139">Для доступа к этой информации, код должен вызвать \*\*отношением с в качестве аргумента *раздел* \*\* и выполните оператор **DDERequest** с одним из следующих действий, предоставленных для аргумента *элемента* .</span><span class="sxs-lookup"><span data-stu-id="b8b9d-139">To access this information, your code must first call the **DDEInitiate** function with as the *topic* argument, and then execute the **DDERequest** statement with one of the following supplied for the *item* argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b8b9d-140">Item</span><span class="sxs-lookup"><span data-stu-id="b8b9d-140">Item</span></span></p></th>
<th><p><span data-ttu-id="b8b9d-141">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b8b9d-141">Returns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b8b9d-142">SysItems</span><span class="sxs-lookup"><span data-stu-id="b8b9d-142">SysItems</span></span></p></td>
<td><p><span data-ttu-id="b8b9d-143">Список элементов, поддерживаемых в разделе система Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-143">A list of items supported by the System topic in Microsoft Access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8b9d-144">Formats</span><span class="sxs-lookup"><span data-stu-id="b8b9d-144">Formats</span></span></p></td>
<td><p><span data-ttu-id="b8b9d-145">Список форматов Microsoft Access можно скопировать в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-145">A list of the formats Microsoft Access can copy onto the Clipboard.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8b9d-146">Status</span><span class="sxs-lookup"><span data-stu-id="b8b9d-146">Status</span></span></p></td>
<td><p><span data-ttu-id="b8b9d-147">&quot;«Занят»&quot; или &quot;готовы&quot;.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-147">&quot;Busy&quot; or &quot;Ready&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8b9d-148">Разделы</span><span class="sxs-lookup"><span data-stu-id="b8b9d-148">Topics</span></span></p></td>
<td><p><span data-ttu-id="b8b9d-149">Список всех открытых баз данных.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-149">A list of all open databases.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b8b9d-150">В следующем примере показано использование функции **DDEInitiate** и **DDERequest** с разделом системы:</span><span class="sxs-lookup"><span data-stu-id="b8b9d-150">The following example demonstrates the use of the **DDEInitiate** and **DDERequest** functions with the System topic:</span></span>

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

## <a name="the-database-topic"></a><span data-ttu-id="b8b9d-151">В разделе базы данных</span><span class="sxs-lookup"><span data-stu-id="b8b9d-151">The database topic</span></span>

<span data-ttu-id="b8b9d-152">В разделе *базы данных* — это имя файла существующей базы данных.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-152">The *database* topic is the file name of an existing database.</span></span> <span data-ttu-id="b8b9d-153">Можно ввести только что базовое имя (Northwind) или его путь к MDB- и расширение (C:\\доступа\\примеры\\Northwind.mdb).</span><span class="sxs-lookup"><span data-stu-id="b8b9d-153">You can type either just the base name (Northwind), or its path and .mdb extension (C:\\Access\\Samples\\Northwind.mdb).</span></span> <span data-ttu-id="b8b9d-154">Начав сеанс DDE с базой данных, можно запросить список объектов в этой базе данных.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-154">After you start a DDE conversation with the database, you can request a list of the objects in that database.</span></span>


> [!NOTE]
> <P><span data-ttu-id="b8b9d-155">Нельзя использовать DDE для запроса файл рабочей группы Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-155">You can't use DDE to query the Microsoft Access workgroup information file.</span></span></P>



<span data-ttu-id="b8b9d-156">В разделе *База данных* поддерживает следующие элементы.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-156">The *database* topic supports the following items.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b8b9d-157">Item</span><span class="sxs-lookup"><span data-stu-id="b8b9d-157">Item</span></span></p></th>
<th><p><span data-ttu-id="b8b9d-158">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b8b9d-158">Returns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b8b9d-159">TableList</span><span class="sxs-lookup"><span data-stu-id="b8b9d-159">TableList</span></span></p></td>
<td><p><span data-ttu-id="b8b9d-160">Список таблиц.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-160">A list of tables.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8b9d-161">QueryList</span><span class="sxs-lookup"><span data-stu-id="b8b9d-161">QueryList</span></span></p></td>
<td><p><span data-ttu-id="b8b9d-162">Список запросов.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-162">A list of queries.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8b9d-163">FormList</span><span class="sxs-lookup"><span data-stu-id="b8b9d-163">FormList</span></span></p></td>
<td><p><span data-ttu-id="b8b9d-164">Список форм.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-164">A list of forms.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8b9d-165">ReportList</span><span class="sxs-lookup"><span data-stu-id="b8b9d-165">ReportList</span></span></p></td>
<td><p><span data-ttu-id="b8b9d-166">Список отчетов.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-166">A list of reports.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8b9d-167">MacroList</span><span class="sxs-lookup"><span data-stu-id="b8b9d-167">MacroList</span></span></p></td>
<td><p><span data-ttu-id="b8b9d-168">Список макросов.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-168">A list of macros.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8b9d-169">ModuleList</span><span class="sxs-lookup"><span data-stu-id="b8b9d-169">ModuleList</span></span></p></td>
<td><p><span data-ttu-id="b8b9d-170">Список модулей.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-170">A list of modules.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8b9d-171">ViewList</span><span class="sxs-lookup"><span data-stu-id="b8b9d-171">ViewList</span></span></p></td>
<td><p><span data-ttu-id="b8b9d-172">Список представлений</span><span class="sxs-lookup"><span data-stu-id="b8b9d-172">A list of views</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8b9d-173">StoredProcedureList</span><span class="sxs-lookup"><span data-stu-id="b8b9d-173">StoredProcedureList</span></span></p></td>
<td><p><span data-ttu-id="b8b9d-174">Список хранимых процедур</span><span class="sxs-lookup"><span data-stu-id="b8b9d-174">A list of stored procedures</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8b9d-175">DatabaseDiagramList</span><span class="sxs-lookup"><span data-stu-id="b8b9d-175">DatabaseDiagramList</span></span></p></td>
<td><p><span data-ttu-id="b8b9d-176">Список схемы базы данных</span><span class="sxs-lookup"><span data-stu-id="b8b9d-176">A list of database diagrams</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b8b9d-177">В следующем примере показано, как сотрудники форму можно открыть в образце базы данных Northwind из процедуры Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="b8b9d-177">The following example shows how you can open the Employees form in the Northwind sample database from a Visual Basic procedure:</span></span>

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

## <a name="the-table-topic"></a><span data-ttu-id="b8b9d-178">В разделе таблицы</span><span class="sxs-lookup"><span data-stu-id="b8b9d-178">The TABLE topic</span></span>

<span data-ttu-id="b8b9d-179">В этих разделах используйте следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="b8b9d-179">These topics use the following syntax:</span></span>

<span data-ttu-id="b8b9d-180">_имя базы данных_ ; **В ТАБЛИЦЕ** _TableName_</span><span class="sxs-lookup"><span data-stu-id="b8b9d-180">_databasename_ ; **TABLE** _tablename_</span></span>

<span data-ttu-id="b8b9d-181">_имя базы данных_ ; **Запрос** _имя запроса_</span><span class="sxs-lookup"><span data-stu-id="b8b9d-181">_databasename_ ; **QUERY** _queryname_</span></span>

<span data-ttu-id="b8b9d-182">_имя базы данных_ ; **SQL** [ _sqlstring_ ]</span><span class="sxs-lookup"><span data-stu-id="b8b9d-182">_databasename_ ; **SQL** [ _sqlstring_ ]</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b8b9d-183">Часть</span><span class="sxs-lookup"><span data-stu-id="b8b9d-183">Part</span></span></p></th>
<th><p><span data-ttu-id="b8b9d-184">Описание</span><span class="sxs-lookup"><span data-stu-id="b8b9d-184">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b8b9d-185"><em>Имя базы данных</em></span><span class="sxs-lookup"><span data-stu-id="b8b9d-185"><em>databasename</em></span></span></p></td>
<td><p><span data-ttu-id="b8b9d-186">Имя базы данных, таблицы или запроса или, которое применяется инструкции SQL, а затем точка с запятой (;).</span><span class="sxs-lookup"><span data-stu-id="b8b9d-186">The name of the database that the table or query is in or that the SQL statement applies to, followed by a semicolon (;).</span></span> <span data-ttu-id="b8b9d-187">Имя базы данных может быть только что базовое имя (Northwind) или его полный путь к MDB- и расширение (C:\Access\Samples\Northwind.mdb).</span><span class="sxs-lookup"><span data-stu-id="b8b9d-187">The database name can be just the base name (Northwind) or its full path and .mdb extension (C:\Access\Samples\Northwind.mdb).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8b9d-188"><em>TableName</em></span><span class="sxs-lookup"><span data-stu-id="b8b9d-188"><em>tablename</em></span></span></p></td>
<td><p><span data-ttu-id="b8b9d-189">Имя существующей таблицы.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-189">The name of an existing table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8b9d-190"><em>Имя запроса</em></span><span class="sxs-lookup"><span data-stu-id="b8b9d-190"><em>queryname</em></span></span></p></td>
<td><p><span data-ttu-id="b8b9d-191">Имя существующего запроса.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-191">The name of an existing query.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8b9d-192"><em>SqlString</em></span><span class="sxs-lookup"><span data-stu-id="b8b9d-192"><em>sqlstring</em></span></span></p></td>
<td><p><span data-ttu-id="b8b9d-193">Допустимая инструкция SQL не должна превышать 256 знаков, конечные точки с запятой.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-193">A valid SQL statement up to 256 characters long, ending with a semicolon.</span></span> <span data-ttu-id="b8b9d-194">Exchange более 256 символов, определяющее и вместо использования последовательных <strong>DDEPoke</strong> операторов для создания инструкции SQL.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-194">To exchange more than 256 characters, omit this argument and instead use successive <strong>DDEPoke</strong> statements to build an SQL statement.</span></span> <span data-ttu-id="b8b9d-195">Например следующий код Visual Basic используется оператор <strong>DDEPoke</strong> построение инструкции SQL и затем запросить результаты запроса.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-195">For example, the following Visual Basic code uses the <strong>DDEPoke</strong> statement to build an SQL statement and then request the results of the query.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="b8b9d-196">В следующей таблице перечислены допустимые элементы для таблицы *tablename*, ЗАПРОСА *имя запроса*и разделы *sqlstring* SQL.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-196">The following table lists the valid items for the TABLE *tablename*, QUERY *queryname*, and SQL *sqlstring* topics.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b8b9d-197">Item</span><span class="sxs-lookup"><span data-stu-id="b8b9d-197">Item</span></span></p></th>
<th><p><span data-ttu-id="b8b9d-198">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b8b9d-198">Returns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b8b9d-199">Все</span><span class="sxs-lookup"><span data-stu-id="b8b9d-199">All</span></span></p></td>
<td><p><span data-ttu-id="b8b9d-200">Все данные в таблице, в том числе имена полей.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-200">All the data in the table, including field names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8b9d-201">Data</span><span class="sxs-lookup"><span data-stu-id="b8b9d-201">Data</span></span></p></td>
<td><p><span data-ttu-id="b8b9d-202">Все строки данных без имена полей.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-202">All rows of data, without field names.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8b9d-203">Списке FieldNames</span><span class="sxs-lookup"><span data-stu-id="b8b9d-203">FieldNames</span></span></p></td>
<td><p><span data-ttu-id="b8b9d-204">Однострочный список имен полей.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-204">A single-row list of field names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8b9d-205">В списке FieldNames; T</span><span class="sxs-lookup"><span data-stu-id="b8b9d-205">FieldNames;T</span></span></p></td>
<td><p><span data-ttu-id="b8b9d-206">Список полей двух строк имен (первой строки) и их данных типов (вторая строка).</span><span class="sxs-lookup"><span data-stu-id="b8b9d-206">A two-row list of field names (first row) and their data types (second row).</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="b8b9d-207">Далее представлены значения, возвращаемые и типы данных они представляют:</span><span class="sxs-lookup"><span data-stu-id="b8b9d-207">These are the values returned and the data types they represent:</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="b8b9d-208"><b>Значение</b></span><span class="sxs-lookup"><span data-stu-id="b8b9d-208"><b>Value</b></span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="b8b9d-209">0</span><span class="sxs-lookup"><span data-stu-id="b8b9d-209">0</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="b8b9d-210">1</span><span class="sxs-lookup"><span data-stu-id="b8b9d-210">1</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="b8b9d-211">2</span><span class="sxs-lookup"><span data-stu-id="b8b9d-211">2</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="b8b9d-212">3</span><span class="sxs-lookup"><span data-stu-id="b8b9d-212">3</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="b8b9d-213">4</span><span class="sxs-lookup"><span data-stu-id="b8b9d-213">4</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="b8b9d-214">5</span><span class="sxs-lookup"><span data-stu-id="b8b9d-214">5</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="b8b9d-215">6</span><span class="sxs-lookup"><span data-stu-id="b8b9d-215">6</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="b8b9d-216">7</span><span class="sxs-lookup"><span data-stu-id="b8b9d-216">7</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="b8b9d-217">8</span><span class="sxs-lookup"><span data-stu-id="b8b9d-217">8</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="b8b9d-218">9</span><span class="sxs-lookup"><span data-stu-id="b8b9d-218">9</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="b8b9d-219">10</span><span class="sxs-lookup"><span data-stu-id="b8b9d-219">10</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="b8b9d-220">11</span><span class="sxs-lookup"><span data-stu-id="b8b9d-220">11</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="b8b9d-221">12</span><span class="sxs-lookup"><span data-stu-id="b8b9d-221">12</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8b9d-222">NextRow</span><span class="sxs-lookup"><span data-stu-id="b8b9d-222">NextRow</span></span></p></td>
<td><p><span data-ttu-id="b8b9d-223">Данные в следующей строке таблицы или запроса.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-223">The data in the next row in the table or query.</span></span> <span data-ttu-id="b8b9d-224">При открытии канала NextRow возвращает данные в первой строке.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-224">When you open a channel, NextRow returns the data in the first row.</span></span> <span data-ttu-id="b8b9d-225">Если текущей строки последней записи и запустите NextRow, запрос не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-225">If the current row is the last record and you run NextRow, the request fails.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8b9d-226">PrevRow</span><span class="sxs-lookup"><span data-stu-id="b8b9d-226">PrevRow</span></span></p></td>
<td><p><span data-ttu-id="b8b9d-227">Данные в предыдущей строки в таблице или запросе.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-227">The data in the previous row in the table or query.</span></span> <span data-ttu-id="b8b9d-228">Если PrevRow первый запрос на новый канал, возвращаются данные в последней строке таблицы или запроса.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-228">If PrevRow is the first request on a new channel, the data in the last row of the table or query is returned.</span></span> <span data-ttu-id="b8b9d-229">Если первая запись текущей строки, не удается выполнить запрос для PrevRow.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-229">If the first record is the current row, the request for PrevRow fails.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8b9d-230">FirstRow</span><span class="sxs-lookup"><span data-stu-id="b8b9d-230">FirstRow</span></span></p></td>
<td><p><span data-ttu-id="b8b9d-231">Данные в первой строке таблицы или запроса.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-231">The data in the first row of the table or query.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8b9d-232">LastRow</span><span class="sxs-lookup"><span data-stu-id="b8b9d-232">LastRow</span></span></p></td>
<td><p><span data-ttu-id="b8b9d-233">Данные в последней строке таблицы или запроса.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-233">The data in the last row of the table or query.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8b9d-234">FieldCount</span><span class="sxs-lookup"><span data-stu-id="b8b9d-234">FieldCount</span></span></p></td>
<td><p><span data-ttu-id="b8b9d-235">Количество полей в таблице или запросе.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-235">The number of fields in the table or query.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8b9d-236">SQLText</span><span class="sxs-lookup"><span data-stu-id="b8b9d-236">SQLText</span></span></p></td>
<td><p><span data-ttu-id="b8b9d-237">Инструкция SQL, представляющий таблицы или запроса.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-237">An SQL statement representing the table or query.</span></span> <span data-ttu-id="b8b9d-238">Для таблиц, то возвращается инструкции SQL в виде &quot;ВЫБЕРИТЕ `*` из <em>таблицы</em>; &quot;.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-238">For tables, this item returns an SQL statement in the form &quot;SELECT `*` FROM <em>table</em>;&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8b9d-239">SQLText; <em>n</em></span><span class="sxs-lookup"><span data-stu-id="b8b9d-239">SQLText;<em>n</em></span></span></p></td>
<td><p><span data-ttu-id="b8b9d-240">Инструкции SQL в <em>n</em>-блоки, представляющие таблицы или запроса, где <em>n</em> — целое число до 256 символов.</span><span class="sxs-lookup"><span data-stu-id="b8b9d-240">An SQL statement, in <em>n</em>-character chunks, representing the table or query, where <em>n</em> is an integer up to 256.</span></span> <span data-ttu-id="b8b9d-241">Предположим, например, представляется с помощью следующей инструкции SQL: элемента &quot;SQLText; 7&quot; возвращает следующие блоки разделители — знаки табуляции: элемента &quot;SQLText; 7&quot; возвращает следующие блоки разделители — знаки табуляции:</span><span class="sxs-lookup"><span data-stu-id="b8b9d-241">For example, suppose a query is represented by the following SQL statement: The item &quot;SQLText;7&quot; returns the following tab-delimited chunks: The item &quot;SQLText;7&quot; returns the following tab-delimited chunks:</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b8b9d-242">В следующем примере показано, как использовать DDE в процедуре Visual Basic для запроса данных из таблицы в образце базы данных Northwind и вставить эти данные в текстовый файл:</span><span class="sxs-lookup"><span data-stu-id="b8b9d-242">The following example shows how you can use DDE in a Visual Basic procedure to request data from a table in the Northwind sample database and insert that data into a text file:</span></span>

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
