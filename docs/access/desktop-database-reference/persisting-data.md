---
title: Сохранение данных (Справочник по для настольных баз данных Access)
TOCTitle: Persisting Data
ms:assetid: cb8a32f7-2cdc-26ed-c6d4-dd93c1ac37ba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250010(v=office.15)
ms:contentKeyID: 48547715
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1fdac02c2293088c60c3346b333b6619777b9a18
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862914"
---
# <a name="persisting-data"></a><span data-ttu-id="e2ee2-102">Сохранение данных</span><span class="sxs-lookup"><span data-stu-id="e2ee2-102">Persisting Data</span></span>


<span data-ttu-id="e2ee2-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e2ee2-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e2ee2-104">Портативные компьютеры (например, с помощью ноутбуков) создала потребность в приложениях, которые могут работать в подключенных и отключенных состояний.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-104">Portable computing (for example, using laptops) has generated the need for applications that can run in both a connected and disconnected state.</span></span> <span data-ttu-id="e2ee2-105">ADO добавил поддерживает это, предоставляя ее разработчик возможность сохранения курсор клиента **записей** на диск и перезагрузить его позже.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-105">ADO has added support for this by giving the developer the ability to save a client cursor **Recordset** to disk and reload it later.</span></span>

<span data-ttu-id="e2ee2-106">Существует несколько сценариев, в которых можно использовать этот тип функции, в том числе следующие:</span><span class="sxs-lookup"><span data-stu-id="e2ee2-106">There are several scenarios in which you could use this type of feature, including the following:</span></span>

- <span data-ttu-id="e2ee2-107">**Дороге:** При извлечении приложения в дорогу, крайне важно для предоставления возможности внести изменения и добавления новых записей, которые затем можно использовать подключение к базе данных более поздней версии и фиксации.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-107">**Traveling:** When taking the application on the road, it is vital to supply the ability to make changes and add new records that can then be reconnected to the database later and committed.</span></span>

- <span data-ttu-id="e2ee2-108">**Редко обновляются операции поиска:** Зачастую в приложении, таблиц используются в качестве операции поиска —, например состояний таблиц налога.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-108">**Infrequently updated lookups:** Often in an application, tables are used as lookups — for example, state tax tables.</span></span> <span data-ttu-id="e2ee2-109">Они редко обновляются и доступны только для чтения.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-109">They are infrequently updated and are read-only.</span></span> <span data-ttu-id="e2ee2-110">Вместо повторного чтения этих данных с сервера каждый раз при запуске приложения, приложение может просто загрузить данные из локально сохраненного **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-110">Instead of rereading this data from the server each time the application is started, the application can simply load the data from a locally persisted **Recordset**.</span></span>

<span data-ttu-id="e2ee2-111">В ADO сохранить и загрузить **наборы записей**, используйте методы **Recordset.Save** и **Recordset.Open(,,,adCmdFile)** на объект ADO **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="e2ee2-111">In ADO, to save and load **Recordsets**, use the **Recordset.Save** and **Recordset.Open(,,,,adCmdFile)** methods on the ADO **Recordset** object.</span></span>

<span data-ttu-id="e2ee2-112">Метод **Save** **записей** можно использовать для хранения набора **записей** ADO в файл на диске.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-112">You can use the **Recordset** **Save** method to persist your ADO **Recordset** to a file on a disk.</span></span> <span data-ttu-id="e2ee2-113">(Можно также сохранить **записей** на объект ADO **потока** .</span><span class="sxs-lookup"><span data-stu-id="e2ee2-113">(You can also save a **Recordset** to an ADO **Stream** object.</span></span> <span data-ttu-id="e2ee2-114">Объекты **потока** рассматриваются далее в руководстве.) Более поздних версий можно использовать метод **Open** и снова откройте **записей** , когда вы готовы к его использования.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-114">**Stream** objects are discussed later in the guide.) Later, you can use the **Open** method to reopen the **Recordset** when you are ready to use it.</span></span> <span data-ttu-id="e2ee2-115">По умолчанию ADO сохраняет **записей** в собственный формат TableGram дополнительные данные (ADTG).</span><span class="sxs-lookup"><span data-stu-id="e2ee2-115">By default, ADO saves the **Recordset** into the proprietary Microsoft Advanced Data TableGram (ADTG) format.</span></span> <span data-ttu-id="e2ee2-116">В этом двоичном формате задается с помощью **adPersistADTG** **PersistFormatEnum** значение.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-116">This binary format is specified using the **adPersistADTG** **PersistFormatEnum** value.</span></span> <span data-ttu-id="e2ee2-117">Кроме того можно сохранить набора **записей** в работе в формате XML вместо использования **adPersistXML**.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-117">Alternatively, you may choose to save your **Recordset** out as XML instead using **adPersistXML**.</span></span> <span data-ttu-id="e2ee2-118">Дополнительные сведения о сохранении наборов записей в формате XML можно [Сохранение записей в формате XML](persisting-records-in-xml-format.md).</span><span class="sxs-lookup"><span data-stu-id="e2ee2-118">For more information about saving Recordsets as XML, see [Persisting Records in XML Format](persisting-records-in-xml-format.md).</span></span>

<span data-ttu-id="e2ee2-119">Синтаксис метода **Save** выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="e2ee2-119">The syntax of the **Save** method is as follows:</span></span>

`recordset.Save Destination, PersistFormat`

<span data-ttu-id="e2ee2-120">При первом сохранении **набора записей**, он не является обязательным для указания *назначения*.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-120">The first time you save the **Recordset**, it is optional to specify *Destination*.</span></span> <span data-ttu-id="e2ee2-121">Если параметр *результат*не задан, будет создан новый файл с именем, задайте значение свойства [источника](source-property-ado-recordset.md) **записей**.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-121">If you omit *Destination*, a new file will be created with a name set to the value of the [Source](source-property-ado-recordset.md) property of the **Recordset**.</span></span>

<span data-ttu-id="e2ee2-122">Параметр *результат* не задан, при последовательном вызове **Сохранить** после первого сохранить или произойдет ошибка во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-122">Omit *Destination* when you subsequently call **Save** after the first save or a run-time error will occur.</span></span> <span data-ttu-id="e2ee2-123">При последующем вызове **Сохранить** с нового *назначения*, **записей** сохраняется в новое место назначения.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-123">If you subsequently call **Save** with a new *Destination*, the **Recordset** is saved to the new destination.</span></span> <span data-ttu-id="e2ee2-124">Тем не менее новые назначения и конечный оба будет открыть.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-124">However, the new destination and the original destination will both be open.</span></span>

<span data-ttu-id="e2ee2-125">**Сохранить** не закрывается **записей** или *назначения*, поэтому можно продолжать работать с **набора записей** и сохраните изменения.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-125">**Save** does not close the **Recordset** or *Destination*, so you can continue to work with the **Recordset** and save your most recent changes.</span></span> <span data-ttu-id="e2ee2-126">*Конечный* открыта, пока **записей** работает, во время которых время другие приложения для чтения, но не запись в *место назначения*.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-126">*Destination* remains open until the **Recordset** is closed, during which time other applications can read but not write to *Destination*.</span></span>

<span data-ttu-id="e2ee2-127">По соображениям безопасности метод **Save** разрешает использование безопасности низкой и пользовательские параметры из сценарий, выполняемый с Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-127">For reasons of security, the **Save** method permits only the use of low and custom security settings from a script executed by Microsoft Internet Explorer.</span></span> <span data-ttu-id="e2ee2-128">Более подробное описание проблемы безопасности в разделе «ADO и RDS безопасности проблемы в Microsoft Internet Explorer» в разделе ActiveX Data Objects (ADO) технические статьи в технические статьи доступа к данным Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-128">For a more detailed explanation of security issues, see "ADO and RDS Security Issues in Microsoft Internet Explorer" under ActiveX Data Objects (ADO) Technical Articles in Microsoft Data Access Technical Articles.</span></span>

<span data-ttu-id="e2ee2-129">Если метод **Save** вызывается при асинхронное извлечение **записей** , execute или обновить операция находится в стадии разработки, **Сохраните** блокировок до завершения асинхронной операции.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-129">If the **Save** method is called while an asynchronous **Recordset** fetch, execute, or update operation is in progress, **Save** waits until the asynchronous operation is complete.</span></span>

<span data-ttu-id="e2ee2-130">Записи сохраняются, начиная с первой строки текущего **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-130">Records are saved beginning with the first row of the **Recordset**.</span></span> <span data-ttu-id="e2ee2-131">После завершения метода **Save** первой строки текущего **набора записей**перемещаются текущей позиции строки.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-131">When the **Save** method is finished, the current row position is moved to the first row of the **Recordset**.</span></span>

<span data-ttu-id="e2ee2-132">Для достижения наилучших результатов присвойте свойству [CursorLocation](cursorlocation-property-ado.md) значение **adUseClient** с **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-132">For best results, set the [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient** with **Save**.</span></span> <span data-ttu-id="e2ee2-133">Если ваш поставщик поддерживает все функциональные возможности, необходимые для сохранения **записей** объекты, службы курсора будет предоставлять функциональные возможности.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-133">If your provider does not support all of the functionality necessary to save **Recordset** objects, the Cursor Service will provide that functionality.</span></span>

<span data-ttu-id="e2ee2-134">После сохранения **записей** со свойством **CursorLocation** , задайте значение **adUseServer**ограничено возможность обновления для **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="e2ee2-134">When a **Recordset** is persisted with the **CursorLocation** property set to **adUseServer**, the update capability for the **Recordset** is limited.</span></span> <span data-ttu-id="e2ee2-135">Как правило только для одной таблицы обновления, вставки и удаления могут (в зависимости от функциональности поставщика).</span><span class="sxs-lookup"><span data-stu-id="e2ee2-135">Typically, only single-table updates, insertions, and deletions are allowed (dependent on provider functionality).</span></span> <span data-ttu-id="e2ee2-136">Метод [выполнить повторную синхронизацию](resync-method-ado.md) также недоступен в этой конфигурации.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-136">The [Resync](resync-method-ado.md) method is also unavailable in this configuration.</span></span>

<span data-ttu-id="e2ee2-137">Так как параметр *назначения* может принимать любой объект, который поддерживает интерфейс OLE DB **IStream** , можно сохранить **записей** непосредственно к объекту ASP **ответа** .</span><span class="sxs-lookup"><span data-stu-id="e2ee2-137">Because the *Destination* parameter can accept any object that supports the OLE DB **IStream** interface, you can save a **Recordset** directly to the ASP **Response** object.</span></span>

<span data-ttu-id="e2ee2-138">В следующем примере методы **сохранения** и **открытия** используются для сохранения **записей** и более поздних версий ее снова:</span><span class="sxs-lookup"><span data-stu-id="e2ee2-138">In the following example, the **Save** and **Open** methods are used to persist a **Recordset** and later reopen it:</span></span>

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

<span data-ttu-id="e2ee2-139">В этом разделе содержатся следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="e2ee2-139">This section includes the following topics:</span></span>

- [<span data-ttu-id="e2ee2-140">Дополнительные сведения о сохранения наборов записей</span><span class="sxs-lookup"><span data-stu-id="e2ee2-140">More About Recordset Persistence</span></span>](more-about-recordset-persistence.md)

- [<span data-ttu-id="e2ee2-141">Сохранение отфильтрованных и иерархических наборов записей</span><span class="sxs-lookup"><span data-stu-id="e2ee2-141">Persisting Filtered and Hierarchical Recordsets</span></span>](persisting-filtered-and-hierarchical-recordsets.md)

- [<span data-ttu-id="e2ee2-142">Persisting Records in XML Format (ADO)</span><span class="sxs-lookup"><span data-stu-id="e2ee2-142">Persisting Records in XML Format (ADO)</span></span>](persisting-records-in-xml-format.md)