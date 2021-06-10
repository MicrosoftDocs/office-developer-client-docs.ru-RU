---
title: Сохраняющиеся данные (ссылка на настольные базы данных)
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
# <a name="persisting-data"></a><span data-ttu-id="e3b99-102">Сохранение данных</span><span class="sxs-lookup"><span data-stu-id="e3b99-102">Persisting data</span></span>


<span data-ttu-id="e3b99-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e3b99-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e3b99-104">Переносные вычисления (например, с помощью ноутбуков) создали потребность в приложениях, которые могут работать как в подключенной, так и отключенной состоянии.</span><span class="sxs-lookup"><span data-stu-id="e3b99-104">Portable computing (for example, using laptops) has generated the need for applications that can run in both a connected and disconnected state.</span></span> <span data-ttu-id="e3b99-105">ADO добавила поддержку для этого, дав разработчику возможность сохранить клиентский курсор **Recordset** на диске и перезагрузить его позже.</span><span class="sxs-lookup"><span data-stu-id="e3b99-105">ADO has added support for this by giving the developer the ability to save a client cursor **Recordset** to disk and reload it later.</span></span>

<span data-ttu-id="e3b99-106">Существует несколько сценариев, в которых можно использовать этот тип функции, включая следующие:</span><span class="sxs-lookup"><span data-stu-id="e3b99-106">There are several scenarios in which you could use this type of feature, including the following:</span></span>

- <span data-ttu-id="e3b99-107">**Путешествия:** При принятии приложения на дороге жизненно важно предоставить возможность вносить изменения и добавлять новые записи, которые затем могут быть подключены к базе данных позже и зафиксированы.</span><span class="sxs-lookup"><span data-stu-id="e3b99-107">**Traveling:** When taking the application on the road, it is vital to supply the ability to make changes and add new records that can then be reconnected to the database later and committed.</span></span>

- <span data-ttu-id="e3b99-108">**Нечасто обновляются просмотры:** Часто в приложении таблицы используются в качестве lookups ( например, таблицы налога на состояние).</span><span class="sxs-lookup"><span data-stu-id="e3b99-108">**Infrequently updated lookups:** Often in an application, tables are used as lookups — for example, state tax tables.</span></span> <span data-ttu-id="e3b99-109">Они нечасто обновляются и только для чтения.</span><span class="sxs-lookup"><span data-stu-id="e3b99-109">They are infrequently updated and are read-only.</span></span> <span data-ttu-id="e3b99-110">Вместо того, чтобы перечитывать эти данные с сервера каждый раз, когда приложение запущено, приложение может просто загрузить данные из локально сохраняемого **Набор записей**.</span><span class="sxs-lookup"><span data-stu-id="e3b99-110">Instead of rereading this data from the server each time the application is started, the application can simply load the data from a locally persisted **Recordset**.</span></span>

<span data-ttu-id="e3b99-111">В ADO для сохранения и загрузки наборов записей используйте методы **Recordset.Save** и **Recordset.Open (,,,,adCmdFile)** для объекта ADO  **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="e3b99-111">In ADO, to save and load **Recordsets**, use the **Recordset.Save** and **Recordset.Open(,,,,adCmdFile)** methods on the ADO **Recordset** object.</span></span>

<span data-ttu-id="e3b99-112">Вы можете использовать метод **Recordset** **Save,** чтобы сохранить набор записей **ADO** в файле на диске.</span><span class="sxs-lookup"><span data-stu-id="e3b99-112">You can use the **Recordset** **Save** method to persist your ADO **Recordset** to a file on a disk.</span></span> <span data-ttu-id="e3b99-113">(Вы также можете сохранить **набор записей для** объекта ADO **Stream.**</span><span class="sxs-lookup"><span data-stu-id="e3b99-113">(You can also save a **Recordset** to an ADO **Stream** object.</span></span> <span data-ttu-id="e3b99-114">**Объекты** потока обсуждаются позже в руководстве.) Позже можно использовать метод **Open** для повторного открытия **наборов записей,** когда вы будете готовы к его использованию.</span><span class="sxs-lookup"><span data-stu-id="e3b99-114">**Stream** objects are discussed later in the guide.) Later, you can use the **Open** method to reopen the **Recordset** when you are ready to use it.</span></span> <span data-ttu-id="e3b99-115">По умолчанию ADO сохраняет набор **записей** в несвободном формате Microsoft Advanced Data TableGram (ADTG).</span><span class="sxs-lookup"><span data-stu-id="e3b99-115">By default, ADO saves the **Recordset** into the proprietary Microsoft Advanced Data TableGram (ADTG) format.</span></span> <span data-ttu-id="e3b99-116">Этот двоичный формат определяется с помощью **значения adPersistADTG** **PersistFormatEnum.**</span><span class="sxs-lookup"><span data-stu-id="e3b99-116">This binary format is specified using the **adPersistADTG** **PersistFormatEnum** value.</span></span> <span data-ttu-id="e3b99-117">Кроме того, вы можете сохранить набор **записей** в качестве XML вместо **использования adPersistXML.**</span><span class="sxs-lookup"><span data-stu-id="e3b99-117">Alternatively, you may choose to save your **Recordset** out as XML instead using **adPersistXML**.</span></span> <span data-ttu-id="e3b99-118">Дополнительные сведения о сохранении записей в виде XML см. в рублях "Сохранение записей [в формате XML".](persisting-records-in-xml-format.md)</span><span class="sxs-lookup"><span data-stu-id="e3b99-118">For more information about saving Recordsets as XML, see [Persisting Records in XML Format](persisting-records-in-xml-format.md).</span></span>

<span data-ttu-id="e3b99-119">Синтаксис метода **Сохранить** следующим образом:</span><span class="sxs-lookup"><span data-stu-id="e3b99-119">The syntax of the **Save** method is as follows:</span></span>

`recordset.Save Destination, PersistFormat`

<span data-ttu-id="e3b99-120">При первом сохранения **наборов записей** необязательно указывать *назначение.*</span><span class="sxs-lookup"><span data-stu-id="e3b99-120">The first time you save the **Recordset**, it is optional to specify *Destination*.</span></span> <span data-ttu-id="e3b99-121">Если упустить *назначение,* будет создан новый файл с именем, за набором имени к значению свойства [Source](source-property-ado-recordset.md) **в Recordset.**</span><span class="sxs-lookup"><span data-stu-id="e3b99-121">If you omit *Destination*, a new file will be created with a name set to the value of the [Source](source-property-ado-recordset.md) property of the **Recordset**.</span></span>

<span data-ttu-id="e3b99-122">Omit *Destination,* когда вы впоследствии вызываете **Сохранить** после первого сохранения или ошибки времени запуска произойдет.</span><span class="sxs-lookup"><span data-stu-id="e3b99-122">Omit *Destination* when you subsequently call **Save** after the first save or a run-time error will occur.</span></span> <span data-ttu-id="e3b99-123">Если впоследствии вы вызываете **Сохранить** с помощью нового *назначения,* **набор записей** сохраняется в новом пункте назначения.</span><span class="sxs-lookup"><span data-stu-id="e3b99-123">If you subsequently call **Save** with a new *Destination*, the **Recordset** is saved to the new destination.</span></span> <span data-ttu-id="e3b99-124">Однако новое назначение и исходное назначение будут открыты.</span><span class="sxs-lookup"><span data-stu-id="e3b99-124">However, the new destination and the original destination will both be open.</span></span>

<span data-ttu-id="e3b99-125">**Сохранение** не закрывает **набор записей** или *назначения,* поэтому вы можете продолжить работу с **набором записей** и сохранить последние изменения.</span><span class="sxs-lookup"><span data-stu-id="e3b99-125">**Save** does not close the **Recordset** or *Destination*, so you can continue to work with the **Recordset** and save your most recent changes.</span></span> <span data-ttu-id="e3b99-126">*Пункт назначения* остается открытым до закрытия **Набор записей,** в течение которого другие приложения могут читать, но не писать в *Пункт назначения.*</span><span class="sxs-lookup"><span data-stu-id="e3b99-126">*Destination* remains open until the **Recordset** is closed, during which time other applications can read but not write to *Destination*.</span></span>

<span data-ttu-id="e3b99-127">По соображениям безопасности метод **Save** позволяет использовать только низкие и настраиваемые параметры безопасности из сценария, выполненного Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="e3b99-127">For reasons of security, the **Save** method permits only the use of low and custom security settings from a script executed by Microsoft Internet Explorer.</span></span> <span data-ttu-id="e3b99-128">Дополнительные сведения о проблемах безопасности см. в статье "Проблемы безопасности ADO и RDS в Microsoft Internet Explorer" в статье ActiveX Объекты данных (ADO) в технических статьях Microsoft Data Access.</span><span class="sxs-lookup"><span data-stu-id="e3b99-128">For a more detailed explanation of security issues, see "ADO and RDS Security Issues in Microsoft Internet Explorer" under ActiveX Data Objects (ADO) Technical Articles in Microsoft Data Access Technical Articles.</span></span>

<span data-ttu-id="e3b99-129">Если метод **Сохранить** вызван, пока выполняется асинхронная операция по извлечению, выполнению или обновлению, сохраните ожидание завершения асинхронной операции.  </span><span class="sxs-lookup"><span data-stu-id="e3b99-129">If the **Save** method is called while an asynchronous **Recordset** fetch, execute, or update operation is in progress, **Save** waits until the asynchronous operation is complete.</span></span>

<span data-ttu-id="e3b99-130">Записи сохраняются начиная с первого ряда **наборов записей.**</span><span class="sxs-lookup"><span data-stu-id="e3b99-130">Records are saved beginning with the first row of the **Recordset**.</span></span> <span data-ttu-id="e3b99-131">По **завершению** метода Сохранить текущая позиция строки перемещается в первую строку **наборов Записей.**</span><span class="sxs-lookup"><span data-stu-id="e3b99-131">When the **Save** method is finished, the current row position is moved to the first row of the **Recordset**.</span></span>

<span data-ttu-id="e3b99-132">Для наилучших результатов задайте [свойство CursorLocation](cursorlocation-property-ado.md) **adUseClient** с **сохранением**.</span><span class="sxs-lookup"><span data-stu-id="e3b99-132">For best results, set the [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient** with **Save**.</span></span> <span data-ttu-id="e3b99-133">Если поставщик не поддерживает все функции, необходимые для сохранения объектов **Recordset,** служба Cursor предоставит эти функции.</span><span class="sxs-lookup"><span data-stu-id="e3b99-133">If your provider does not support all of the functionality necessary to save **Recordset** objects, the Cursor Service will provide that functionality.</span></span>

<span data-ttu-id="e3b99-134">При **сохраняемом** наборе записей с свойством **CursorLocation,** задаваемом **adUseServer,** возможности обновления **для набора записей** ограничены.</span><span class="sxs-lookup"><span data-stu-id="e3b99-134">When a **Recordset** is persisted with the **CursorLocation** property set to **adUseServer**, the update capability for the **Recordset** is limited.</span></span> <span data-ttu-id="e3b99-135">Как правило, допускаются только одностоловые обновления, вставки и удаления (зависящие от функциональности поставщика).</span><span class="sxs-lookup"><span data-stu-id="e3b99-135">Typically, only single-table updates, insertions, and deletions are allowed (dependent on provider functionality).</span></span> <span data-ttu-id="e3b99-136">Метод [Resync](resync-method-ado.md) также недоступен в этой конфигурации.</span><span class="sxs-lookup"><span data-stu-id="e3b99-136">The [Resync](resync-method-ado.md) method is also unavailable in this configuration.</span></span>

<span data-ttu-id="e3b99-137">Так как *параметр Destination* может принимать любой объект, который поддерживает интерфейс **IStream** OLE DB, можно сохранить набор **Записей** непосредственно к объекту asP **Response.**</span><span class="sxs-lookup"><span data-stu-id="e3b99-137">Because the *Destination* parameter can accept any object that supports the OLE DB **IStream** interface, you can save a **Recordset** directly to the ASP **Response** object.</span></span>

<span data-ttu-id="e3b99-138">В следующем примере методы **Сохранить** и **Открыть** используются для сохранения **наборов Записей** и их повторного открытия.</span><span class="sxs-lookup"><span data-stu-id="e3b99-138">In the following example, the **Save** and **Open** methods are used to persist a **Recordset** and later reopen it:</span></span>

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

<span data-ttu-id="e3b99-139">В этой статье содержатся следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="e3b99-139">This section includes the following topics:</span></span>

- [<span data-ttu-id="e3b99-140">More About Recordset Persistence</span><span class="sxs-lookup"><span data-stu-id="e3b99-140">More About Recordset Persistence</span></span>](more-about-recordset-persistence.md)

- [<span data-ttu-id="e3b99-141">Persisting Filtered and Hierarchical Recordsets</span><span class="sxs-lookup"><span data-stu-id="e3b99-141">Persisting Filtered and Hierarchical Recordsets</span></span>](persisting-filtered-and-hierarchical-recordsets.md)

- [<span data-ttu-id="e3b99-142">Persisting Records in XML Format (ADO)</span><span class="sxs-lookup"><span data-stu-id="e3b99-142">Persisting Records in XML Format (ADO)</span></span>](persisting-records-in-xml-format.md)
