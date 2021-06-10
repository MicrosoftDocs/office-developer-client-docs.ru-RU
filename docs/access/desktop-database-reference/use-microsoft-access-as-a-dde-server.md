---
title: Использование Microsoft Access в качестве сервера DDE
TOCTitle: Use Microsoft Access as a DDE Server
description: Microsoft Access поддерживает динамический обмен данными (DDE) в качестве приложения назначения (клиента) или приложения-источника (сервера).
ms:assetid: a3e82bf7-94b5-8eec-86bc-2d5387d66738
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821067(v=office.15)
ms:contentKeyID: 48546801
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5186349
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 0750bdce0e1cda383c48f9c16e62e00997fdfb0a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313393"
---
# <a name="use-microsoft-access-as-a-dde-server"></a><span data-ttu-id="936a0-103">Использование Microsoft Access в качестве сервера DDE</span><span class="sxs-lookup"><span data-stu-id="936a0-103">Use Microsoft Access as a DDE server</span></span>

<span data-ttu-id="936a0-104">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="936a0-104">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="936a0-105">Microsoft Access поддерживает динамический обмен данными (DDE) в качестве приложения назначения (клиента) или приложения-источника (сервера).</span><span class="sxs-lookup"><span data-stu-id="936a0-105">Microsoft Access supports dynamic data exchange (DDE) as either a destination (client) application or a source (server) application.</span></span> <span data-ttu-id="936a0-106">Например, такое приложение, как Microsoft Word клиент, может запрашивать данные через DDE из базы данных Microsoft Access, которая действует как сервер.</span><span class="sxs-lookup"><span data-stu-id="936a0-106">For example, an application such as Microsoft Word, acting as a client, can request data through DDE from a Microsoft Access database that's acting as a server.</span></span>

> [!TIP]
> <span data-ttu-id="936a0-107">Если вам нужно управлять объектами Microsoft Access из другого приложения, возможно, потребуется использовать автоматизацию.</span><span class="sxs-lookup"><span data-stu-id="936a0-107">If you need to manipulate Microsoft Access objects from another application, you may want to consider using Automation.</span></span>

<span data-ttu-id="936a0-108">Диалог DDE между клиентом и сервером устанавливается по определенной теме.</span><span class="sxs-lookup"><span data-stu-id="936a0-108">A DDE conversation between a client and server is established on a particular topic.</span></span> <span data-ttu-id="936a0-109">Темой может быть либо файл данных в формате, поддерживаемом серверным приложением, либо тема System, которая поставляет сведения о самом приложении сервера.</span><span class="sxs-lookup"><span data-stu-id="936a0-109">A topic can be either a data file in the format supported by the server application, or it can be the System topic, which supplies information about the server application itself.</span></span> <span data-ttu-id="936a0-110">После начала беседы по определенной теме может быть передан только элемент данных, связанный с этой темой.</span><span class="sxs-lookup"><span data-stu-id="936a0-110">After a conversation has begun on a particular topic, only a data item associated with that topic can be transferred.</span></span>

<span data-ttu-id="936a0-111">Например, предположим, что вы Microsoft Word и хотите вставить данные из определенной базы данных Microsoft Access в документ.</span><span class="sxs-lookup"><span data-stu-id="936a0-111">For example, suppose you are running Microsoft Word and want to insert data from a particular Microsoft Access database into a document.</span></span> <span data-ttu-id="936a0-112">Вы начинаете беседу dDE с Microsoft Access, открыв канал DDE с функцией **DDEInitiate** и указав в качестве темы имя файла базы данных.</span><span class="sxs-lookup"><span data-stu-id="936a0-112">You begin a DDE conversation with Microsoft Access by opening a DDE channel with the **DDEInitiate** function and specifying the database file name as the topic.</span></span> <span data-ttu-id="936a0-113">Затем можно передать данные из этой базы данных в Microsoft Word по этому каналу.</span><span class="sxs-lookup"><span data-stu-id="936a0-113">You can then transfer data from that database to Microsoft Word through that channel.</span></span>

<span data-ttu-id="936a0-114">Как сервер DDE Microsoft Access поддерживает следующие темы:</span><span class="sxs-lookup"><span data-stu-id="936a0-114">As a DDE server, Microsoft Access supports the following topics:</span></span>

- <span data-ttu-id="936a0-115">Тема "Система"</span><span class="sxs-lookup"><span data-stu-id="936a0-115">The System topic</span></span>

- <span data-ttu-id="936a0-116">Имя базы данных *(тема базы* данных)</span><span class="sxs-lookup"><span data-stu-id="936a0-116">The name of a database (*database* topic)</span></span>

- <span data-ttu-id="936a0-117">Имя таблицы *(тема таблицы)*</span><span class="sxs-lookup"><span data-stu-id="936a0-117">The name of a table (*tablename* topic)</span></span>

- <span data-ttu-id="936a0-118">Имя запроса *(тема запроса)*</span><span class="sxs-lookup"><span data-stu-id="936a0-118">The name of a query (*queryname* topic)</span></span>

- <span data-ttu-id="936a0-119">Строка microsoft Access SQL *(sqlstring* topic)</span><span class="sxs-lookup"><span data-stu-id="936a0-119">A Microsoft Access SQL string (*sqlstring* topic)</span></span>

<span data-ttu-id="936a0-120">После наладки беседы с DDE можно использовать заявление **DDEExecute** для отправки команды от клиента в приложение-сервер.</span><span class="sxs-lookup"><span data-stu-id="936a0-120">After you've established a DDE conversation, you can use the **DDEExecute** statement to send a command from the client to the server application.</span></span> <span data-ttu-id="936a0-121">В качестве сервера DDE Microsoft Access распознает любую из следующих команд:</span><span class="sxs-lookup"><span data-stu-id="936a0-121">When used as a DDE server, Microsoft Access recognizes any of the following as a valid command:</span></span>

- <span data-ttu-id="936a0-122">Имя макроса в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="936a0-122">The name of a macro in the current database.</span></span>

- <span data-ttu-id="936a0-123">Любое действие, которое можно выполнить в Visual Basic с помощью одного из методов **объекта DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="936a0-123">Any action that you can carry out in Visual Basic by using one of the methods of the **DoCmd** object.</span></span>

- <span data-ttu-id="936a0-124">Действия OpenDatabase и CloseDatabase, которые используются только для операций DDE.</span><span class="sxs-lookup"><span data-stu-id="936a0-124">The OpenDatabase and CloseDatabase actions, which are used only for DDE operations.</span></span> <span data-ttu-id="936a0-125">(Пример использования этих действий см. в примере далее в этой теме.)</span><span class="sxs-lookup"><span data-stu-id="936a0-125">(For an example of how to use these actions, see the example later in this topic.)</span></span>

> [!NOTE]
> <span data-ttu-id="936a0-126">При указании макрос действия в качестве заявления **DDEExecute** действие и любые аргументы следуют синтаксису объекта **DoCmd** и должны быть заключены в скобки ([]).</span><span class="sxs-lookup"><span data-stu-id="936a0-126">When you specify a macro action as a **DDEExecute** statement, the action and any arguments follow the **DoCmd** object syntax and must be enclosed in brackets ([ ]).</span></span> <span data-ttu-id="936a0-127">Однако приложения, поддерживают DDE, не распознают внутренние константы в операциях DDE.</span><span class="sxs-lookup"><span data-stu-id="936a0-127">However, applications that support DDE don't recognize intrinsic constants in DDE operations.</span></span> <span data-ttu-id="936a0-128">Кроме того, строки аргументы должны быть заключены в кавычках ("") если строка содержит запятую.</span><span class="sxs-lookup"><span data-stu-id="936a0-128">Also, string arguments must be enclosed in quotation marks (" ") if the string contains a comma.</span></span> <span data-ttu-id="936a0-129">В противном случае кавычка не требуется.</span><span class="sxs-lookup"><span data-stu-id="936a0-129">Otherwise, quotation marks aren't required.</span></span>

<span data-ttu-id="936a0-130">Клиентские приложения могут использовать **функцию DDERequest** для запроса текстовых данных из серверного приложения по открытому каналу DDE.</span><span class="sxs-lookup"><span data-stu-id="936a0-130">The client application can use the **DDERequest** function to request text data from the server application over an open DDE channel.</span></span> <span data-ttu-id="936a0-131">Или клиент может использовать **заявление DDEPoke** для отправки данных в приложение сервера.</span><span class="sxs-lookup"><span data-stu-id="936a0-131">Or the client can use the **DDEPoke** statement to send data to the server application.</span></span> <span data-ttu-id="936a0-132">После завершения передачи данных клиент может использовать заявление **DDETerminate** для закрытия канала DDE или **DDETerminateAll** для закрытия всех открытых каналов.</span><span class="sxs-lookup"><span data-stu-id="936a0-132">After the data transfer is complete, the client can use the **DDETerminate** statement to close the DDE channel, or the **DDETerminateAll** statement to close all open channels.</span></span>

> [!NOTE]
> <span data-ttu-id="936a0-133">Когда клиентская приложение закончит получать данные по каналу DDE, оно должно закрыть этот канал для сохранения ресурсов памяти.</span><span class="sxs-lookup"><span data-stu-id="936a0-133">When your client application has finished receiving data over a DDE channel, it should close that channel to conserve memory resources.</span></span>

<span data-ttu-id="936a0-134">В следующем примере показано, как создать процедуру Microsoft Word с помощью Visual Basic microsoft Access в качестве сервера DDE.</span><span class="sxs-lookup"><span data-stu-id="936a0-134">The following example demonstrates how to create a Microsoft Word procedure with Visual Basic that uses Microsoft Access as a DDE server.</span></span> <span data-ttu-id="936a0-135">(Для работы в этом примере необходимо запускать Microsoft Access.)</span><span class="sxs-lookup"><span data-stu-id="936a0-135">(For this example to work, Microsoft Access must be running.)</span></span>

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

<span data-ttu-id="936a0-136">В следующих разделах приводится информация о допустимых разделах DDE, поддерживаемых Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="936a0-136">The following sections provide information about the valid DDE topics supported by Microsoft Access.</span></span>

## <a name="the-system-topic"></a><span data-ttu-id="936a0-137">Тема "Система"</span><span class="sxs-lookup"><span data-stu-id="936a0-137">The System topic</span></span>

<span data-ttu-id="936a0-138">Тема System — это стандартная тема для всех Windows приложений На основе Microsoft.</span><span class="sxs-lookup"><span data-stu-id="936a0-138">The System topic is a standard topic for all Microsoft Windows–based applications.</span></span> <span data-ttu-id="936a0-139">Он поставляет сведения о других темах, поддерживаемых приложением.</span><span class="sxs-lookup"><span data-stu-id="936a0-139">It supplies information about the other topics supported by the application.</span></span> <span data-ttu-id="936a0-140">Чтобы получить доступ к этой информации, код должен сначала  вызвать функцию **DDEInitiate** с аргументом темы, а  затем выполнить заявление **DDERequest** с одним из следующих аргументов элемента.</span><span class="sxs-lookup"><span data-stu-id="936a0-140">To access this information, your code must first call the **DDEInitiate** function with the *topic* argument, and then execute the **DDERequest** statement with one of the following supplied for the *item* argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="936a0-141">Item</span><span class="sxs-lookup"><span data-stu-id="936a0-141">Item</span></span></p></th>
<th><p><span data-ttu-id="936a0-142">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="936a0-142">Returns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="936a0-143">SysItems</span><span class="sxs-lookup"><span data-stu-id="936a0-143">SysItems</span></span></p></td>
<td><p><span data-ttu-id="936a0-144">Список элементов, поддерживаемых темой System в Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="936a0-144">A list of items supported by the System topic in Microsoft Access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="936a0-145">Форматы</span><span class="sxs-lookup"><span data-stu-id="936a0-145">Formats</span></span></p></td>
<td><p><span data-ttu-id="936a0-146">Список форматов, которые Microsoft Access может скопировать на буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="936a0-146">A list of the formats Microsoft Access can copy onto the Clipboard.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="936a0-147">Состояние</span><span class="sxs-lookup"><span data-stu-id="936a0-147">Status</span></span></p></td>
<td><p><span data-ttu-id="936a0-148">&quot;Занят &quot; или &quot; готов &quot; .</span><span class="sxs-lookup"><span data-stu-id="936a0-148">&quot;Busy&quot; or &quot;Ready&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="936a0-149">Темы</span><span class="sxs-lookup"><span data-stu-id="936a0-149">Topics</span></span></p></td>
<td><p><span data-ttu-id="936a0-150">Список всех открытых баз данных.</span><span class="sxs-lookup"><span data-stu-id="936a0-150">A list of all open databases.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="936a0-151">В следующем примере показано использование функций **DDEInitiate** и **DDERequest** в разделе System:</span><span class="sxs-lookup"><span data-stu-id="936a0-151">The following example demonstrates the use of the **DDEInitiate** and **DDERequest** functions with the System topic:</span></span>

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

## <a name="the-database-topic"></a><span data-ttu-id="936a0-152">Тема базы данных</span><span class="sxs-lookup"><span data-stu-id="936a0-152">The database topic</span></span>

<span data-ttu-id="936a0-153">Тема *базы* данных — это имя файла существующей базы данных.</span><span class="sxs-lookup"><span data-stu-id="936a0-153">The *database* topic is the file name of an existing database.</span></span> <span data-ttu-id="936a0-154">Вы можете ввести только базовое имя (Northwind), или его путь и расширение .mdb (C: \\ Access \\ Samples \\ Northwind.mdb).</span><span class="sxs-lookup"><span data-stu-id="936a0-154">You can type either just the base name (Northwind), or its path and .mdb extension (C:\\Access\\Samples\\Northwind.mdb).</span></span> <span data-ttu-id="936a0-155">После начала беседы dDE с базой данных можно запросить список объектов в этой базе данных.</span><span class="sxs-lookup"><span data-stu-id="936a0-155">After you start a DDE conversation with the database, you can request a list of the objects in that database.</span></span>

> [!NOTE]
> <span data-ttu-id="936a0-156">Вы не можете использовать DDE для запроса информационного файла группы Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="936a0-156">You can't use DDE to query the Microsoft Access workgroup information file.</span></span>

<span data-ttu-id="936a0-157">Тема *базы данных* поддерживает следующие элементы.</span><span class="sxs-lookup"><span data-stu-id="936a0-157">The *database* topic supports the following items.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="936a0-158">Item</span><span class="sxs-lookup"><span data-stu-id="936a0-158">Item</span></span></p></th>
<th><p><span data-ttu-id="936a0-159">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="936a0-159">Returns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="936a0-160">TableList</span><span class="sxs-lookup"><span data-stu-id="936a0-160">TableList</span></span></p></td>
<td><p><span data-ttu-id="936a0-161">Список таблиц</span><span class="sxs-lookup"><span data-stu-id="936a0-161">A list of tables</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="936a0-162">QueryList</span><span class="sxs-lookup"><span data-stu-id="936a0-162">QueryList</span></span></p></td>
<td><p><span data-ttu-id="936a0-163">Список запросов</span><span class="sxs-lookup"><span data-stu-id="936a0-163">A list of queries</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="936a0-164">FormList</span><span class="sxs-lookup"><span data-stu-id="936a0-164">FormList</span></span></p></td>
<td><p><span data-ttu-id="936a0-165">Список форм</span><span class="sxs-lookup"><span data-stu-id="936a0-165">A list of forms</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="936a0-166">ReportList</span><span class="sxs-lookup"><span data-stu-id="936a0-166">ReportList</span></span></p></td>
<td><p><span data-ttu-id="936a0-167">Список отчетов</span><span class="sxs-lookup"><span data-stu-id="936a0-167">A list of reports</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="936a0-168">MacroList</span><span class="sxs-lookup"><span data-stu-id="936a0-168">MacroList</span></span></p></td>
<td><p><span data-ttu-id="936a0-169">Список макрос</span><span class="sxs-lookup"><span data-stu-id="936a0-169">A list of macros</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="936a0-170">ModuleList</span><span class="sxs-lookup"><span data-stu-id="936a0-170">ModuleList</span></span></p></td>
<td><p><span data-ttu-id="936a0-171">Список модулей</span><span class="sxs-lookup"><span data-stu-id="936a0-171">A list of modules</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="936a0-172">ViewList</span><span class="sxs-lookup"><span data-stu-id="936a0-172">ViewList</span></span></p></td>
<td><p><span data-ttu-id="936a0-173">Список представлений</span><span class="sxs-lookup"><span data-stu-id="936a0-173">A list of views</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="936a0-174">StoredProcedureList</span><span class="sxs-lookup"><span data-stu-id="936a0-174">StoredProcedureList</span></span></p></td>
<td><p><span data-ttu-id="936a0-175">Список сохраненных процедур</span><span class="sxs-lookup"><span data-stu-id="936a0-175">A list of stored procedures</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="936a0-176">DatabaseDiagramList</span><span class="sxs-lookup"><span data-stu-id="936a0-176">DatabaseDiagramList</span></span></p></td>
<td><p><span data-ttu-id="936a0-177">Список схем баз данных</span><span class="sxs-lookup"><span data-stu-id="936a0-177">A list of database diagrams</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="936a0-178">В следующем примере показано, как открыть форму Сотрудников в примере базы данных Northwind с Visual Basic процедуры:</span><span class="sxs-lookup"><span data-stu-id="936a0-178">The following example shows how you can open the Employees form in the Northwind sample database from a Visual Basic procedure:</span></span>

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

## <a name="the-table-topic"></a><span data-ttu-id="936a0-179">Тема TABLE</span><span class="sxs-lookup"><span data-stu-id="936a0-179">The TABLE topic</span></span>

<span data-ttu-id="936a0-180">В этих темах используется следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="936a0-180">These topics use the following syntax:</span></span>

<span data-ttu-id="936a0-181">_имя базы данных;_ **Имя таблицы** _TABLE_</span><span class="sxs-lookup"><span data-stu-id="936a0-181">_databasename_ ; **TABLE** _tablename_</span></span>

<span data-ttu-id="936a0-182">_имя базы данных;_ **Имя** _запроса QUERY_</span><span class="sxs-lookup"><span data-stu-id="936a0-182">_databasename_ ; **QUERY** _queryname_</span></span>

<span data-ttu-id="936a0-183">_имя базы данных;_ **SQL** [ _sqlstring_ ]</span><span class="sxs-lookup"><span data-stu-id="936a0-183">_databasename_ ; **SQL** [ _sqlstring_ ]</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="936a0-184">Part</span><span class="sxs-lookup"><span data-stu-id="936a0-184">Part</span></span></p></th>
<th><p><span data-ttu-id="936a0-185">Описание</span><span class="sxs-lookup"><span data-stu-id="936a0-185">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="936a0-186"><em>имя базы данных</em></span><span class="sxs-lookup"><span data-stu-id="936a0-186"><em>databasename</em></span></span></p></td>
<td><p><span data-ttu-id="936a0-187">Имя базы данных, в которой находится таблица или запрос или к которой применяется SQL, а затем полуколон (;).</span><span class="sxs-lookup"><span data-stu-id="936a0-187">The name of the database that the table or query is in or that the SQL statement applies to, followed by a semicolon (;).</span></span> <span data-ttu-id="936a0-188">Имя базы данных может быть только базовым именем (Northwind) или полным путем и расширением .mdb (C:\Access\Samples\Northwind.mdb).</span><span class="sxs-lookup"><span data-stu-id="936a0-188">The database name can be just the base name (Northwind) or its full path and .mdb extension (C:\Access\Samples\Northwind.mdb).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="936a0-189"><em>имя таблицы</em></span><span class="sxs-lookup"><span data-stu-id="936a0-189"><em>tablename</em></span></span></p></td>
<td><p><span data-ttu-id="936a0-190">Имя существующей таблицы.</span><span class="sxs-lookup"><span data-stu-id="936a0-190">The name of an existing table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="936a0-191"><em>имя запроса</em></span><span class="sxs-lookup"><span data-stu-id="936a0-191"><em>queryname</em></span></span></p></td>
<td><p><span data-ttu-id="936a0-192">Имя существующего запроса.</span><span class="sxs-lookup"><span data-stu-id="936a0-192">The name of an existing query.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="936a0-193"><em>sqlstring</em></span><span class="sxs-lookup"><span data-stu-id="936a0-193"><em>sqlstring</em></span></span></p></td>
<td><p><span data-ttu-id="936a0-194">Допустимая SQL до 256 символов длиной, заканчивающаяся полуколоном.</span><span class="sxs-lookup"><span data-stu-id="936a0-194">A valid SQL statement up to 256 characters long, ending with a semicolon.</span></span> <span data-ttu-id="936a0-195">Чтобы обменять более 256 символов, ограничь этот аргумент и вместо этого используйте последовательные заявления <strong>DDEPoke</strong> для создания SQL.</span><span class="sxs-lookup"><span data-stu-id="936a0-195">To exchange more than 256 characters, omit this argument and instead use successive <strong>DDEPoke</strong> statements to build an SQL statement.</span></span> <span data-ttu-id="936a0-196">Например, в следующем Visual Basic используется заявление <strong>DDEPoke</strong> для создания SQL, а затем запроса результатов запроса.</span><span class="sxs-lookup"><span data-stu-id="936a0-196">For example, the following Visual Basic code uses the <strong>DDEPoke</strong> statement to build an SQL statement and then request the results of the query.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="936a0-197">В следующей таблице перечислены допустимые элементы для имен *таблицы* TABLE, *queryname* и SQL *sqlstring.*</span><span class="sxs-lookup"><span data-stu-id="936a0-197">The following table lists the valid items for the TABLE *tablename*, QUERY *queryname*, and SQL *sqlstring* topics.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="936a0-198">Item</span><span class="sxs-lookup"><span data-stu-id="936a0-198">Item</span></span></p></th>
<th><p><span data-ttu-id="936a0-199">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="936a0-199">Returns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="936a0-200">Все</span><span class="sxs-lookup"><span data-stu-id="936a0-200">All</span></span></p></td>
<td><p><span data-ttu-id="936a0-201">Все данные в таблице, включая имена полей.</span><span class="sxs-lookup"><span data-stu-id="936a0-201">All the data in the table, including field names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="936a0-202">Данные</span><span class="sxs-lookup"><span data-stu-id="936a0-202">Data</span></span></p></td>
<td><p><span data-ttu-id="936a0-203">Все строки данных без имен полей.</span><span class="sxs-lookup"><span data-stu-id="936a0-203">All rows of data, without field names.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="936a0-204">FieldNames</span><span class="sxs-lookup"><span data-stu-id="936a0-204">FieldNames</span></span></p></td>
<td><p><span data-ttu-id="936a0-205">Список однорядных имен полей.</span><span class="sxs-lookup"><span data-stu-id="936a0-205">A single-row list of field names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="936a0-206">FieldNames; T</span><span class="sxs-lookup"><span data-stu-id="936a0-206">FieldNames;T</span></span></p></td>
<td><p><span data-ttu-id="936a0-207">Двухрядный список имен полей (первая строка) и их типов данных (вторая строка).</span><span class="sxs-lookup"><span data-stu-id="936a0-207">A two-row list of field names (first row) and their data types (second row).</span></span></p>
<p><span data-ttu-id="936a0-208">Возвращаемые значения:</span><span class="sxs-lookup"><span data-stu-id="936a0-208">These are the values returned:</span></span></p>
<p><span data-ttu-id="936a0-209">Значение</span><span class="sxs-lookup"><span data-stu-id="936a0-209">Value</span></span></p>
<p><ul>
<li><span data-ttu-id="936a0-210">0</span><span class="sxs-lookup"><span data-stu-id="936a0-210">0</span></span></li>
<li><span data-ttu-id="936a0-211">1</span><span class="sxs-lookup"><span data-stu-id="936a0-211">1</span></span></li>
<li><span data-ttu-id="936a0-212">2</span><span class="sxs-lookup"><span data-stu-id="936a0-212">2</span></span></li>
<li><span data-ttu-id="936a0-213">3</span><span class="sxs-lookup"><span data-stu-id="936a0-213">3</span></span></li>
<li><span data-ttu-id="936a0-214">4 </span><span class="sxs-lookup"><span data-stu-id="936a0-214">4</span></span></li>
<li><span data-ttu-id="936a0-215">5 </span><span class="sxs-lookup"><span data-stu-id="936a0-215">5</span></span></li>
<li><span data-ttu-id="936a0-216">6 </span><span class="sxs-lookup"><span data-stu-id="936a0-216">6</span></span></li>
<li><span data-ttu-id="936a0-217">7 </span><span class="sxs-lookup"><span data-stu-id="936a0-217">7</span></span></li>
<li><span data-ttu-id="936a0-218">8 </span><span class="sxs-lookup"><span data-stu-id="936a0-218">8</span></span></li>
<li><span data-ttu-id="936a0-219">9 </span><span class="sxs-lookup"><span data-stu-id="936a0-219">9</span></span></li>
<li><span data-ttu-id="936a0-220">10 </span><span class="sxs-lookup"><span data-stu-id="936a0-220">10</span></span></li>
<li><span data-ttu-id="936a0-221">11</span><span class="sxs-lookup"><span data-stu-id="936a0-221">11</span></span></li>
<li><span data-ttu-id="936a0-222">12 </span><span class="sxs-lookup"><span data-stu-id="936a0-222">12</span></span></li>
</ul>
</p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="936a0-223">NextRow</span><span class="sxs-lookup"><span data-stu-id="936a0-223">NextRow</span></span></p></td>
<td><p><span data-ttu-id="936a0-224">Данные в следующей строке в таблице или запросе.</span><span class="sxs-lookup"><span data-stu-id="936a0-224">The data in the next row in the table or query.</span></span> <span data-ttu-id="936a0-225">При открываемом канале NextRow возвращает данные в первом ряду.</span><span class="sxs-lookup"><span data-stu-id="936a0-225">When you open a channel, NextRow returns the data in the first row.</span></span> <span data-ttu-id="936a0-226">Если текущая строка является последней записью и вы запустите NextRow, запрос сбой.</span><span class="sxs-lookup"><span data-stu-id="936a0-226">If the current row is the last record and you run NextRow, the request fails.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="936a0-227">PrevRow</span><span class="sxs-lookup"><span data-stu-id="936a0-227">PrevRow</span></span></p></td>
<td><p><span data-ttu-id="936a0-228">Данные в предыдущей строке в таблице или запросе.</span><span class="sxs-lookup"><span data-stu-id="936a0-228">The data in the previous row in the table or query.</span></span> <span data-ttu-id="936a0-229">Если PrevRow является первым запросом на новом канале, возвращаются данные в последнем ряду таблицы или запроса.</span><span class="sxs-lookup"><span data-stu-id="936a0-229">If PrevRow is the first request on a new channel, the data in the last row of the table or query is returned.</span></span> <span data-ttu-id="936a0-230">Если первая запись — текущая строка, запрос на PrevRow не удается.</span><span class="sxs-lookup"><span data-stu-id="936a0-230">If the first record is the current row, the request for PrevRow fails.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="936a0-231">FirstRow</span><span class="sxs-lookup"><span data-stu-id="936a0-231">FirstRow</span></span></p></td>
<td><p><span data-ttu-id="936a0-232">Данные в первом ряду таблицы или запроса.</span><span class="sxs-lookup"><span data-stu-id="936a0-232">The data in the first row of the table or query.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="936a0-233">LastRow</span><span class="sxs-lookup"><span data-stu-id="936a0-233">LastRow</span></span></p></td>
<td><p><span data-ttu-id="936a0-234">Данные в последнем ряду таблицы или запроса.</span><span class="sxs-lookup"><span data-stu-id="936a0-234">The data in the last row of the table or query.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="936a0-235">FieldCount</span><span class="sxs-lookup"><span data-stu-id="936a0-235">FieldCount</span></span></p></td>
<td><p><span data-ttu-id="936a0-236">Количество полей в таблице или запросе.</span><span class="sxs-lookup"><span data-stu-id="936a0-236">The number of fields in the table or query.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="936a0-237">SQLText</span><span class="sxs-lookup"><span data-stu-id="936a0-237">SQLText</span></span></p></td>
<td><p><span data-ttu-id="936a0-238">Заявление SQL, представляющее таблицу или запрос.</span><span class="sxs-lookup"><span data-stu-id="936a0-238">An SQL statement representing the table or query.</span></span> <span data-ttu-id="936a0-239">Для таблиц этот элемент возвращает SQL в таблице &quot; SELECT `*` FROM; <em></em> &quot; .</span><span class="sxs-lookup"><span data-stu-id="936a0-239">For tables, this item returns an SQL statement in the form &quot;SELECT `*` FROM <em>table</em>;&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="936a0-240">SQLText; <em>n</em></span><span class="sxs-lookup"><span data-stu-id="936a0-240">SQLText;<em>n</em></span></span></p></td>
<td><p><span data-ttu-id="936a0-241">Заявление SQL n-character, <em></em>представляющее таблицу или запрос, где <em>n</em> — это integer до 256.</span><span class="sxs-lookup"><span data-stu-id="936a0-241">An SQL statement, in <em>n</em>-character chunks, representing the table or query, where <em>n</em> is an integer up to 256.</span></span> <span data-ttu-id="936a0-242">Например, предположим, что запрос представлен следующим заявлением SQL: элемент SQLText;7 возвращает следующие фрагменты, относя к вкладке: элемент &quot; &quot; &quot; SQLText;7 возвращает следующие фрагменты, относя к &quot; вкладке:</span><span class="sxs-lookup"><span data-stu-id="936a0-242">For example, suppose a query is represented by the following SQL statement: The item &quot;SQLText;7&quot; returns the following tab-delimited chunks: The item &quot;SQLText;7&quot; returns the following tab-delimited chunks:</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="936a0-243">В следующем примере показано, как можно использовать DDE в процедуре Visual Basic для запроса данных из таблицы в примере базы данных Northwind и вставки этих данных в текстовый файл:</span><span class="sxs-lookup"><span data-stu-id="936a0-243">The following example shows how you can use DDE in a Visual Basic procedure to request data from a table in the Northwind sample database and insert that data into a text file:</span></span>

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
