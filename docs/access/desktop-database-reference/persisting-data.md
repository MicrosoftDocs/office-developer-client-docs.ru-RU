---
title: Persisting data (Access desktop database reference)
TOCTitle: Persisting data
ms:assetid: cb8a32f7-2cdc-26ed-c6d4-dd93c1ac37ba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250010(v=office.15)
ms:contentKeyID: 48547715
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f5788216a20e62cfc39fd2081f4f672bc4f9b808
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287603"
---
# <a name="persisting-data"></a><span data-ttu-id="0439b-102">Сохранение данных</span><span class="sxs-lookup"><span data-stu-id="0439b-102">Persisting data</span></span>


<span data-ttu-id="0439b-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0439b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0439b-104">Переносимые вычисления (например, на ноутбуках) создали потребность в приложениях, которые могут работать как в подключенных, так и в отключенных состояниях.</span><span class="sxs-lookup"><span data-stu-id="0439b-104">Portable computing (for example, using laptops) has generated the need for applications that can run in both a connected and disconnected state.</span></span> <span data-ttu-id="0439b-105">ADO добавила поддержку этого, предоставляя разработчику возможность сохранить  набор записей курсора клиента на диск и перезагрузить его позже.</span><span class="sxs-lookup"><span data-stu-id="0439b-105">ADO has added support for this by giving the developer the ability to save a client cursor **Recordset** to disk and reload it later.</span></span>

<span data-ttu-id="0439b-106">Существует несколько сценариев, в которых можно использовать этот тип функций, в том числе следующие:</span><span class="sxs-lookup"><span data-stu-id="0439b-106">There are several scenarios in which you could use this type of feature, including the following:</span></span>

- <span data-ttu-id="0439b-107">**В пути:** При получении приложения в пути важно предоставить возможность вносить изменения и добавлять новые записи, которые затем можно будет повторно подключить к базе данных позже и зафиксировать.</span><span class="sxs-lookup"><span data-stu-id="0439b-107">**Traveling:** When taking the application on the road, it is vital to supply the ability to make changes and add new records that can then be reconnected to the database later and committed.</span></span>

- <span data-ttu-id="0439b-108">**Редко обновляются подыскаки:** Часто в приложении таблицы используются в качестве подсмотра, например таблицы налога на состояние.</span><span class="sxs-lookup"><span data-stu-id="0439b-108">**Infrequently updated lookups:** Often in an application, tables are used as lookups — for example, state tax tables.</span></span> <span data-ttu-id="0439b-109">Они обновляются редко и являются только для чтения.</span><span class="sxs-lookup"><span data-stu-id="0439b-109">They are infrequently updated and are read-only.</span></span> <span data-ttu-id="0439b-110">Вместо того чтобы перечитать эти данные с сервера при каждом начале работы приложения, приложение может просто загрузить данные из локально сохраняемого **наборов записей.**</span><span class="sxs-lookup"><span data-stu-id="0439b-110">Instead of rereading this data from the server each time the application is started, the application can simply load the data from a locally persisted **Recordset**.</span></span>

<span data-ttu-id="0439b-111">In ADO, to save and load **Recordsets,** use the **Recordset.Save** and **Recordset.Open(,,,,adCmdFile)** methods on the ADO **Recordset** object.</span><span class="sxs-lookup"><span data-stu-id="0439b-111">In ADO, to save and load **Recordsets**, use the **Recordset.Save** and **Recordset.Open(,,,,adCmdFile)** methods on the ADO **Recordset** object.</span></span>

<span data-ttu-id="0439b-112">С помощью метода **Recordset** **Save** можно сохранить набор записей **ADO** в файле на диске.</span><span class="sxs-lookup"><span data-stu-id="0439b-112">You can use the **Recordset** **Save** method to persist your ADO **Recordset** to a file on a disk.</span></span> <span data-ttu-id="0439b-113">(Вы также можете сохранить **объект Recordset** в объекте ADO **Stream.**</span><span class="sxs-lookup"><span data-stu-id="0439b-113">(You can also save a **Recordset** to an ADO **Stream** object.</span></span> <span data-ttu-id="0439b-114">**Объекты Stream** обсуждаются далее в руководстве.) Позже вы можете использовать метод **Open,** чтобы повторно открыть **набор записей,** когда будете готовы к его использованию.</span><span class="sxs-lookup"><span data-stu-id="0439b-114">**Stream** objects are discussed later in the guide.) Later, you can use the **Open** method to reopen the **Recordset** when you are ready to use it.</span></span> <span data-ttu-id="0439b-115">По умолчанию ADO сохраняет **набор recordset** в проприетарном формате Microsoft Advanced Data TableGram (ADTG).</span><span class="sxs-lookup"><span data-stu-id="0439b-115">By default, ADO saves the **Recordset** into the proprietary Microsoft Advanced Data TableGram (ADTG) format.</span></span> <span data-ttu-id="0439b-116">Этот двоичный формат указывается с помощью значения **adPersistADTG** **PersistFormatEnum.**</span><span class="sxs-lookup"><span data-stu-id="0439b-116">This binary format is specified using the **adPersistADTG** **PersistFormatEnum** value.</span></span> <span data-ttu-id="0439b-117">Кроме того, вы можете сохранить набор **записей** в XML вместо **adPersistXML.**</span><span class="sxs-lookup"><span data-stu-id="0439b-117">Alternatively, you may choose to save your **Recordset** out as XML instead using **adPersistXML**.</span></span> <span data-ttu-id="0439b-118">Дополнительные сведения о сохранении записей в формате XML см. в подсети [Persisting Records in XML Format.](persisting-records-in-xml-format.md)</span><span class="sxs-lookup"><span data-stu-id="0439b-118">For more information about saving Recordsets as XML, see [Persisting Records in XML Format](persisting-records-in-xml-format.md).</span></span>

<span data-ttu-id="0439b-119">Синтаксис метода **Save:**</span><span class="sxs-lookup"><span data-stu-id="0439b-119">The syntax of the **Save** method is as follows:</span></span>

`recordset.Save Destination, PersistFormat`

<span data-ttu-id="0439b-120">При первом сохранения **recordset** указывать назначение *необязательно.*</span><span class="sxs-lookup"><span data-stu-id="0439b-120">The first time you save the **Recordset**, it is optional to specify *Destination*.</span></span> <span data-ttu-id="0439b-121">Если опустить *destination,* будет создан новый файл со значением свойства [Source](source-property-ado-recordset.md) объекта **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="0439b-121">If you omit *Destination*, a new file will be created with a name set to the value of the [Source](source-property-ado-recordset.md) property of the **Recordset**.</span></span>

<span data-ttu-id="0439b-122">Опустить *назначение при* последующем вызове **"Сохранить"** после первого сохранения или возникновения ошибки во время запуска.</span><span class="sxs-lookup"><span data-stu-id="0439b-122">Omit *Destination* when you subsequently call **Save** after the first save or a run-time error will occur.</span></span> <span data-ttu-id="0439b-123">При последующем вызове **функции "Сохранить** с новым назначением" набор  **записей** сохраняется в новом месте назначения.</span><span class="sxs-lookup"><span data-stu-id="0439b-123">If you subsequently call **Save** with a new *Destination*, the **Recordset** is saved to the new destination.</span></span> <span data-ttu-id="0439b-124">Однако новое и исходное назначения будут открыты.</span><span class="sxs-lookup"><span data-stu-id="0439b-124">However, the new destination and the original destination will both be open.</span></span>

<span data-ttu-id="0439b-125">**Сохранение** не закрывает набор **записей** или *назначение,* поэтому вы можете продолжать работать с **набором записей** и сохранять последние изменения.</span><span class="sxs-lookup"><span data-stu-id="0439b-125">**Save** does not close the **Recordset** or *Destination*, so you can continue to work with the **Recordset** and save your most recent changes.</span></span> <span data-ttu-id="0439b-126">*Назначение* остается открытым, пока **набор записей** не будет закрыт, в течение которого другие приложения могут читать, но не записывать данные в *destination.*</span><span class="sxs-lookup"><span data-stu-id="0439b-126">*Destination* remains open until the **Recordset** is closed, during which time other applications can read but not write to *Destination*.</span></span>

<span data-ttu-id="0439b-127">В целях безопасности метод **Save** позволяет использовать только параметры низкой и настраиваемой безопасности из сценария, выполненного Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="0439b-127">For reasons of security, the **Save** method permits only the use of low and custom security settings from a script executed by Microsoft Internet Explorer.</span></span> <span data-ttu-id="0439b-128">Более подробное описание проблем безопасности см. в статье "ADO and RDS Security Issues in Microsoft Internet Explorer" статьи ActiveX Data Objects (ADO) Technical Articles in Microsoft Data Access Technical Articles.</span><span class="sxs-lookup"><span data-stu-id="0439b-128">For a more detailed explanation of security issues, see "ADO and RDS Security Issues in Microsoft Internet Explorer" under ActiveX Data Objects (ADO) Technical Articles in Microsoft Data Access Technical Articles.</span></span>

<span data-ttu-id="0439b-129">Если метод **Save** вызван во время  выполнения операции асинхронного получения, выполнения или обновления наборов записей,  сохранение будет выполняться до завершения асинхронной операции.</span><span class="sxs-lookup"><span data-stu-id="0439b-129">If the **Save** method is called while an asynchronous **Recordset** fetch, execute, or update operation is in progress, **Save** waits until the asynchronous operation is complete.</span></span>

<span data-ttu-id="0439b-130">Записи сохраняются, начиная с первой строки **наборов записей.**</span><span class="sxs-lookup"><span data-stu-id="0439b-130">Records are saved beginning with the first row of the **Recordset**.</span></span> <span data-ttu-id="0439b-131">После завершения работы метода **Save** текущая позиция строки перемещается в первую строку **recordset.**</span><span class="sxs-lookup"><span data-stu-id="0439b-131">When the **Save** method is finished, the current row position is moved to the first row of the **Recordset**.</span></span>

<span data-ttu-id="0439b-132">Для наилучших результатов задайте для свойства [CursorLocation](cursorlocation-property-ado.md) свойство **adUseClient** с **сохранением.**</span><span class="sxs-lookup"><span data-stu-id="0439b-132">For best results, set the [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient** with **Save**.</span></span> <span data-ttu-id="0439b-133">Если поставщик не поддерживает все функции, необходимые для сохранения объектов **Recordset,** служба курсоров предоставляет эту функцию.</span><span class="sxs-lookup"><span data-stu-id="0439b-133">If your provider does not support all of the functionality necessary to save **Recordset** objects, the Cursor Service will provide that functionality.</span></span>

<span data-ttu-id="0439b-134">Если набор **записей** сохраняется со свойством **CursorLocation,** установленным для **adUseServer,** возможность обновления для **набора записей** ограничена.</span><span class="sxs-lookup"><span data-stu-id="0439b-134">When a **Recordset** is persisted with the **CursorLocation** property set to **adUseServer**, the update capability for the **Recordset** is limited.</span></span> <span data-ttu-id="0439b-135">Как правило, разрешены только обновления, вставки и удаления из одной таблицы (в зависимости от функциональности поставщика).</span><span class="sxs-lookup"><span data-stu-id="0439b-135">Typically, only single-table updates, insertions, and deletions are allowed (dependent on provider functionality).</span></span> <span data-ttu-id="0439b-136">Метод [Resync](resync-method-ado.md) также недоступен в этой конфигурации.</span><span class="sxs-lookup"><span data-stu-id="0439b-136">The [Resync](resync-method-ado.md) method is also unavailable in this configuration.</span></span>

<span data-ttu-id="0439b-137">Так как *параметр Destination* может принимать любой объект, который поддерживает интерфейс OLE DB **IStream,** можно сохранить **объект Recordset** непосредственно в объекте ответа **ASP.**</span><span class="sxs-lookup"><span data-stu-id="0439b-137">Because the *Destination* parameter can accept any object that supports the OLE DB **IStream** interface, you can save a **Recordset** directly to the ASP **Response** object.</span></span>

<span data-ttu-id="0439b-138">В следующем примере методы **Save** и **Open** используются для сохранения **recordset,** а затем повторного открытия:</span><span class="sxs-lookup"><span data-stu-id="0439b-138">In the following example, the **Save** and **Open** methods are used to persist a **Recordset** and later reopen it:</span></span>

```vb 
 
'BeginPersist 
 conn.ConnectionString = _ 
 "Provider='SQLOLEDB';Data Source='MySqlServer';" _ 
 & "Integrated Security='SSPI';Initial Catalog='pubs'" 
 conn.Open 
 
 conn.Execute "create table testtable (dbkey int " & _ 
 "primary key, field1 char(10))" 
 conn.Execute "insert into testtable values (1, 'string1')" 
 
 Set rst.ActiveConnection = conn 
 rst.CursorLocation = adUseClient 
 
 rst.Open "select * from testtable", conn, adOpenStatic, _ 
 adLockBatchOptimistic 
 
 'Change the row on the client 
 rst!field1 = "NewValue" 
 
 'Save to a file--the .dat extension is an example; choose 
 'your own extension. The changes will be saved in the file 
 'as well as the original data. 
 MyFile = Dir("c:\temp\temptbl.dat") 
 If MyFile <> "" Then 
 Kill "c:\temp\temptbl.dat" 
 End If 
 
 rst.Save "c:\temp\temptbl.dat", adPersistADTG 
 rst.Close 
 Set rst = Nothing 
 
 'Now reload the data from the file 
 Set rst = New ADODB.Recordset 
 rst.Open "c:\temp\temptbl.dat", , adOpenStatic, _ 
 adLockBatchOptimistic, adCmdFile 
 
 Debug.Print "After Loading the file from disk" 
 Debug.Print " Current Edited Value: " & rst!field1.Value 
 Debug.Print " Value Before Editing: " & rst!field1.OriginalValue 
 
 'Note that you can reconnect to a connection and 
 'submit the changes to the data source 
 Set rst.ActiveConnection = conn 
 rst.UpdateBatch 
'EndPersist 
```

<span data-ttu-id="0439b-139">В этой статье содержатся следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="0439b-139">This section includes the following topics:</span></span>

- [<span data-ttu-id="0439b-140">More About Recordset Persistence</span><span class="sxs-lookup"><span data-stu-id="0439b-140">More About Recordset Persistence</span></span>](more-about-recordset-persistence.md)

- [<span data-ttu-id="0439b-141">Persisting Filtered and Hierarchical Recordsets</span><span class="sxs-lookup"><span data-stu-id="0439b-141">Persisting Filtered and Hierarchical Recordsets</span></span>](persisting-filtered-and-hierarchical-recordsets.md)

- [<span data-ttu-id="0439b-142">Persisting Records in XML Format (ADO)</span><span class="sxs-lookup"><span data-stu-id="0439b-142">Persisting Records in XML Format (ADO)</span></span>](persisting-records-in-xml-format.md)
