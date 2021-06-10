---
title: Глава 12. Руководство по удаленной службе данных (RDS)
TOCTitle: 'Chapter 12: RDS tutorial'
ms:assetid: fa44a5e8-e4df-dfdd-d7a1-a870ec3cabdd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250277(v=office.15)
ms:contentKeyID: 48548837
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aca77ac08688e643327bdbf229ab6c1dec40d109
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296481"
---
# <a name="chapter-12-remote-data-service-rds-tutorial"></a><span data-ttu-id="3c275-102">Глава 12. Руководство по удаленной службе данных (RDS)</span><span class="sxs-lookup"><span data-stu-id="3c275-102">Chapter 12: Remote Data Service (RDS) tutorial</span></span>

<span data-ttu-id="3c275-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3c275-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3c275-104">В этом руководстве показано использование модели программирования RDS для запроса и обновления источника данных.</span><span class="sxs-lookup"><span data-stu-id="3c275-104">This tutorial illustrates using the RDS programming model to query and update a data source.</span></span> <span data-ttu-id="3c275-105">Во-первых, в нем описываются действия, необходимые для выполнения этой задачи.</span><span class="sxs-lookup"><span data-stu-id="3c275-105">First, it describes the steps necessary to accomplish this task.</span></span> <span data-ttu-id="3c275-106">Затем учебник повторяется в Microsoft Visual Basic Scripting Edition и Microsoft Visual J++, в котором представлены ADO для Windows классов Foundation (ADO/WFC).</span><span class="sxs-lookup"><span data-stu-id="3c275-106">Then the tutorial is repeated in Microsoft Visual Basic Scripting Edition and Microsoft Visual J++, featuring ADO for Windows Foundation Classes (ADO/WFC).</span></span>

<span data-ttu-id="3c275-107">Этот учебник закодировать на разных языках по двум причинам:</span><span class="sxs-lookup"><span data-stu-id="3c275-107">This tutorial is coded in different languages for two reasons:</span></span>

- <span data-ttu-id="3c275-108">Документация для RDS предполагает коды чтения в Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="3c275-108">The documentation for RDS assumes the reader codes in Visual Basic.</span></span> <span data-ttu-id="3c275-109">Это делает документацию удобной для Visual Basic, но менее полезной для программистов, которые используют другие языки.</span><span class="sxs-lookup"><span data-stu-id="3c275-109">This makes the documentation convenient for Visual Basic programmers, but less useful for programmers who use other languages.</span></span>

- <span data-ttu-id="3c275-110">Если вы не уверены в определенной функции RDS и знаете немного другого языка, вы можете решить свой вопрос, ищите ту же функцию, выраженную на другом языке.</span><span class="sxs-lookup"><span data-stu-id="3c275-110">If you are uncertain about a particular RDS feature and you know a little of another language, you might be able to resolve your question by looking for the same feature expressed in another language.</span></span>

<span data-ttu-id="3c275-111">Этот учебник основан на модели программирования RDS.</span><span class="sxs-lookup"><span data-stu-id="3c275-111">This tutorial is based on the RDS programming model.</span></span> <span data-ttu-id="3c275-112">В нем обсуждаются каждый шаг модели программирования по отдельности.</span><span class="sxs-lookup"><span data-stu-id="3c275-112">It discusses each step of the programming model individually.</span></span> <span data-ttu-id="3c275-113">Кроме того, он иллюстрирует каждый шаг фрагментом Visual Basic кода.</span><span class="sxs-lookup"><span data-stu-id="3c275-113">In addition, it illustrates each step with a fragment of Visual Basic code.</span></span>

<span data-ttu-id="3c275-114">Пример кода повторяется на других языках с минимальным обсуждением.</span><span class="sxs-lookup"><span data-stu-id="3c275-114">The code example is repeated in other languages with minimal discussion.</span></span> <span data-ttu-id="3c275-115">Каждый шаг в данном учебнике по языку программирования отмечен соответствующим шагом в модели программирования и описательным учебником.</span><span class="sxs-lookup"><span data-stu-id="3c275-115">Each step in a given programming language tutorial is marked with the corresponding step in the programming model and descriptive tutorial.</span></span> <span data-ttu-id="3c275-116">Используйте число шага, чтобы сослаться на обсуждение в описательном учебнике.</span><span class="sxs-lookup"><span data-stu-id="3c275-116">Use the number of the step to refer to the discussion in the descriptive tutorial.</span></span>

<span data-ttu-id="3c275-117">Модель программирования RDS приведена ниже.</span><span class="sxs-lookup"><span data-stu-id="3c275-117">The RDS programming model is stated below.</span></span> <span data-ttu-id="3c275-118">Используйте его как дорожную карту при перейти к учебнику.</span><span class="sxs-lookup"><span data-stu-id="3c275-118">Use it as a roadmap as you proceed through the tutorial.</span></span>

### <a name="rds-programming-model-with-objects"></a><span data-ttu-id="3c275-119">Модель программирования RDS с объектами</span><span class="sxs-lookup"><span data-stu-id="3c275-119">RDS programming model with objects</span></span>

- <span data-ttu-id="3c275-120">Укажите программу, вызываемую на сервере, и получите способ (прокси) ссылаться на нее от клиента.</span><span class="sxs-lookup"><span data-stu-id="3c275-120">Specify the program to be invoked on the server, and obtain a way (proxy) to refer to it from the client.</span></span>

- <span data-ttu-id="3c275-121">Вызов серверной программы.</span><span class="sxs-lookup"><span data-stu-id="3c275-121">Invoke the server program.</span></span> <span data-ttu-id="3c275-122">Передай параметры серверной программе, которая определяет источник данных и команду для выпуска.</span><span class="sxs-lookup"><span data-stu-id="3c275-122">Pass parameters to the server program that identifies the data source and the command to issue.</span></span>

- <span data-ttu-id="3c275-123">Серверная программа получает объект [Recordset](recordset-object-ado.md) из источника данных, как правило, с помощью ADO.</span><span class="sxs-lookup"><span data-stu-id="3c275-123">The server program obtains a [Recordset](recordset-object-ado.md) object from the data source, typically by using ADO.</span></span> <span data-ttu-id="3c275-124">Необязательный объект **Recordset** обрабатывается на сервере.</span><span class="sxs-lookup"><span data-stu-id="3c275-124">Optionally, the **Recordset** object is processed on the server.</span></span>

- <span data-ttu-id="3c275-125">Программа сервера возвращает конечный объект **Recordset** в клиентском приложении.</span><span class="sxs-lookup"><span data-stu-id="3c275-125">The server program returns the final **Recordset** object to the client application.</span></span>

- <span data-ttu-id="3c275-126">На клиенте объект **Recordset** необязательный, который можно легко использовать с помощью визуальных элементов управления.</span><span class="sxs-lookup"><span data-stu-id="3c275-126">On the client, the **Recordset** object is optionally put into a form that can be easily used by visual controls.</span></span>

- <span data-ttu-id="3c275-127">Изменения объекта **Recordset** отправляются обратно на сервер и используются для обновления источника данных.</span><span class="sxs-lookup"><span data-stu-id="3c275-127">Changes to the **Recordset** object are sent back to the server and used to update the data source.</span></span>

## <a name="step-1-specify-a-server-program"></a><span data-ttu-id="3c275-128">Шаг 1. Укажите серверную программу</span><span class="sxs-lookup"><span data-stu-id="3c275-128">Step 1: Specify a server program</span></span>

<span data-ttu-id="3c275-129">В наиболее общем случае используйте [RDS. Объект DataSpace](dataspace-object-rds.md) [CreateObject,](createobject-method-rds.md) чтобы указать серверную программу по [умолчанию, RDSServer.DataFactory](datafactory-object-rdsserver.md)или собственную настраиваемую серверную программу (бизнес-объект).</span><span class="sxs-lookup"><span data-stu-id="3c275-129">In the most general case, use the [RDS.DataSpace](dataspace-object-rds.md) object [CreateObject](createobject-method-rds.md) method to specify the default server program, [RDSServer.DataFactory](datafactory-object-rdsserver.md), or your own custom server program (business object).</span></span> <span data-ttu-id="3c275-130">Серверная программа мгновенно возвращается на сервере и возвращается ссылка на серверную программу или прокси-сервер.</span><span class="sxs-lookup"><span data-stu-id="3c275-130">A server program is instantiated on the server, and a reference to the server program, or *proxy*, is returned.</span></span>

<span data-ttu-id="3c275-131">В этом руководстве используется серверная программа по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="3c275-131">This tutorial uses the default server program:</span></span>

```vb 
 
Sub RDSTutorial1() 
 Dim DS as New RDS.DataSpace 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
... 
``` 

## <a name="step-2-invoke-the-server-program"></a><span data-ttu-id="3c275-132">Шаг 2. Вызов серверной программы</span><span class="sxs-lookup"><span data-stu-id="3c275-132">Step 2: Invoke the server program</span></span> 

<span data-ttu-id="3c275-133">При вызове метода в прокси-сервере клиента фактически программа на сервере выполняет этот метод.</span><span class="sxs-lookup"><span data-stu-id="3c275-133">When you invoke a method on the client *proxy*, the actual program on the server executes the method.</span></span> <span data-ttu-id="3c275-134">На этом шаге выполняется запрос на сервере.</span><span class="sxs-lookup"><span data-stu-id="3c275-134">In this step, you'll execute a query on the server.</span></span>

### <a name="part-a"></a><span data-ttu-id="3c275-135">Часть A</span><span class="sxs-lookup"><span data-stu-id="3c275-135">Part A</span></span>

<span data-ttu-id="3c275-136">Если бы вы не использовали [RDSServer.DataFactory](datafactory-object-rdsserver.md) в этом руководстве, наиболее удобным способом выполнения этого шага было бы использование [RDS. Объект DataControl.](datacontrol-object-rds.md)</span><span class="sxs-lookup"><span data-stu-id="3c275-136">If you weren't using [RDSServer.DataFactory](datafactory-object-rdsserver.md) in this tutorial, the most convenient way to perform this step would be to use the [RDS.DataControl](datacontrol-object-rds.md) object.</span></span> <span data-ttu-id="3c275-137">The **RDS. DataControl объединяет** предыдущий этап создания прокси-сервера с этим шагом, выпуская запрос.</span><span class="sxs-lookup"><span data-stu-id="3c275-137">The **RDS.DataControl** combines the previous step of creating a proxy, with this step, issuing the query.</span></span>

1. <span data-ttu-id="3c275-138">Установите **RDS. Свойство объекта DataControl** [Server,](server-property-rds.md) чтобы определить, где следует мгновенно использовать серверную программу.</span><span class="sxs-lookup"><span data-stu-id="3c275-138">Set the **RDS.DataControl** object [Server](server-property-rds.md) property to identify where the server program should be instantiated.</span></span>

2. <span data-ttu-id="3c275-139">Установите свойство [Подключение,](connect-property-rds.md) чтобы указать строку подключения для доступа к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="3c275-139">Set the [Connect](connect-property-rds.md) property to specify the connect string to access the data source.</span></span>

3. <span data-ttu-id="3c275-140">Установите свойство [SQL,](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) чтобы указать текст команды запроса.</span><span class="sxs-lookup"><span data-stu-id="3c275-140">Set the [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) property to specify the query command text.</span></span> 

4. <span data-ttu-id="3c275-141">Выдайте метод [Обновления,](refresh-method-rds.md) чтобы серверная программа подключилась к источнику данных, извлекла строки, указанные в запросе, и вернула объект **Recordset** клиенту.</span><span class="sxs-lookup"><span data-stu-id="3c275-141">Issue the [Refresh](refresh-method-rds.md) method to cause the server program to connect to the data source, retrieve rows specified by the query, and return a **Recordset** object to the client.</span></span>

<span data-ttu-id="3c275-142">В этом руководстве не используется **RDS. DataControl**, но это будет выглядеть, если он сделал:</span><span class="sxs-lookup"><span data-stu-id="3c275-142">This tutorial does not use the **RDS.DataControl**, but this is how it would look if it did:</span></span>

```vb 
 
Sub RDSTutorial2A() 
 Dim DC as New RDS.DataControl 
 DC.Server = "https://yourServer" 
 DC.Connect = "DSN=Pubs" 
 DC.SQL = "SELECT * FROM Authors" 
 DC.Refresh 
... 
```

<br/>

<span data-ttu-id="3c275-143">Кроме того, в учебнике не вызывается RDS с объектами ADO, но это будет выглядеть, если он сделал:</span><span class="sxs-lookup"><span data-stu-id="3c275-143">Nor does the tutorial invoke RDS with ADO objects, but this is how it would look if it did:</span></span>

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "SELECT * FROM Authors","Provider=MS Remote;Data Source=Pubs;" & _ 
"Remote Server=https://yourServer;Remote Provider=SQLOLEDB;" 
```

### <a name="part-b"></a><span data-ttu-id="3c275-144">Часть B</span><span class="sxs-lookup"><span data-stu-id="3c275-144">Part B</span></span>

<span data-ttu-id="3c275-145">Общий метод выполнения этого шага — вызвать метод запроса объекта **RDSServer.DataFactory.** [](query-method-rds.md)</span><span class="sxs-lookup"><span data-stu-id="3c275-145">The general method of performing this step is to invoke the **RDSServer.DataFactory** object [Query](query-method-rds.md) method.</span></span> <span data-ttu-id="3c275-146">Для этого метода используется строка подключения, которая используется для подключения к источнику данных, и командный текст, который используется для указания строк, которые будут возвращены из источника данных.</span><span class="sxs-lookup"><span data-stu-id="3c275-146">That method takes a connect string, which is used to connect to a data source, and a command text, which is used to specify the rows to be returned from the data source.</span></span>

<span data-ttu-id="3c275-147">В этом руководстве используется метод запроса объекта **DataFactory:** </span><span class="sxs-lookup"><span data-stu-id="3c275-147">This tutorial uses the **DataFactory** object **Query** method:</span></span>

```vb 
 
Sub RDSTutorial2B() 
 Dim DS as New RDS.DataSpace 
 Dim DF 
 Dim RS as ADODB.Recordset 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
... 
```

## <a name="step-3-server-obtains-a-recordset"></a><span data-ttu-id="3c275-148">Шаг 3. Сервер получает набор записей</span><span class="sxs-lookup"><span data-stu-id="3c275-148">Step 3: Server obtains a Recordset</span></span> 

<span data-ttu-id="3c275-149">Серверная программа использует строку подключения и командный текст для запроса источника данных для нужных строк.</span><span class="sxs-lookup"><span data-stu-id="3c275-149">The server program uses the connect string and command text to query the data source for the desired rows.</span></span> <span data-ttu-id="3c275-150">ADO обычно используется для получения этого **Набор записей,** хотя другие интерфейсы доступа к данным Майкрософт, такие как OLE DB, можно использовать.</span><span class="sxs-lookup"><span data-stu-id="3c275-150">ADO is typically used to retrieve this **Recordset**, although other Microsoft data access interfaces, such as OLE DB, could be used.</span></span>

<span data-ttu-id="3c275-151">Настраиваемая серверная программа может выглядеть так:</span><span class="sxs-lookup"><span data-stu-id="3c275-151">A custom server program might look like this:</span></span>

```vb 
 
Public Function ServerProgram(cn as String, qry as String) as Object 
Dim rs as New ADODB.Recordset 
 rs.CursorLocation = adUseClient 
 rs.Open qry, cn 
 rs.ActiveConnection = Nothing 
 Set ServerProgram = rs 
End Function 
```

## <a name="step-4-server-returns-the-recordset"></a><span data-ttu-id="3c275-152">Шаг 4. Сервер возвращает набор записей</span><span class="sxs-lookup"><span data-stu-id="3c275-152">Step 4: Server returns the Recordset</span></span> 

<span data-ttu-id="3c275-153">RDS преобразует извлеченный объект **Recordset** в форму, которая может быть отправлена  клиенту (то есть маршалам **recordset).**</span><span class="sxs-lookup"><span data-stu-id="3c275-153">RDS converts the retrieved **Recordset** object to a form that can be sent back to the client (that is, it *marshals* the **Recordset**).</span></span> <span data-ttu-id="3c275-154">Точная форма преобразования и его отправление зависят от того, находится ли сервер в Интернете или интрасети, локальной локальной сети или является библиотекой динамических ссылок.</span><span class="sxs-lookup"><span data-stu-id="3c275-154">The exact form of the conversion and how it is sent depends on whether the server is on the Internet or an intranet, a local area network, or is a dynamic-link library.</span></span> <span data-ttu-id="3c275-155">Однако эта деталь не является критической. Важно только то, что RDS отправляет **набор записей** клиенту.</span><span class="sxs-lookup"><span data-stu-id="3c275-155">However, this detail is not critical; all that matters is that RDS sends the **Recordset** back to the client.</span></span>

<span data-ttu-id="3c275-156">Со стороны клиента объект **Recordset** возвращается и назначен локальной переменной.</span><span class="sxs-lookup"><span data-stu-id="3c275-156">On the client side, a **Recordset** object is returned and assigned to a local variable.</span></span>

```vb 
 
Sub RDSTutorial4() 
 Dim DS as New RDS.DataSpace 
 Dim RS as ADODB.Recordset 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query("DSN=Pubs", "SELECT * FROM Authors") 
... 
```

## <a name="step-5-datacontrol-is-made-usable"></a><span data-ttu-id="3c275-157">Шаг 5. DataControl можно</span><span class="sxs-lookup"><span data-stu-id="3c275-157">Step 5: DataControl is made usable</span></span> 

<span data-ttu-id="3c275-158">Возвращенный **объект Recordset** доступен для использования.</span><span class="sxs-lookup"><span data-stu-id="3c275-158">The returned **Recordset** object is available for use.</span></span> <span data-ttu-id="3c275-159">Вы можете исследовать, перемещаться или редактировать его так же, как и любой другой **Набор записей.**</span><span class="sxs-lookup"><span data-stu-id="3c275-159">You can examine, navigate, or edit it as you would any other **Recordset**.</span></span> <span data-ttu-id="3c275-160">То, что можно сделать с **набором записей,** зависит от среды.</span><span class="sxs-lookup"><span data-stu-id="3c275-160">What you can do with the **Recordset** depends on your environment.</span></span> <span data-ttu-id="3c275-161">Visual Basic Visual C++ имеют визуальные элементы управления, которые могут напрямую или косвенно использовать **Набор** записей с помощью включения управления данными.</span><span class="sxs-lookup"><span data-stu-id="3c275-161">Visual Basic and Visual C++ have visual controls that can use a **Recordset** directly or indirectly with the aid of an enabling data control.</span></span>

<span data-ttu-id="3c275-162">Например, если вы отображаете веб-страницу в Internet Explorer, может потребоваться отобразить данные объекта **Recordset** в визуальном контроле.</span><span class="sxs-lookup"><span data-stu-id="3c275-162">For example, if you are displaying a webpage in Internet Explorer, you might want to display the **Recordset** object data in a visual control.</span></span> <span data-ttu-id="3c275-163">Визуальные элементы управления на веб-странице не могут напрямую получить доступ к **объекту Recordset.**</span><span class="sxs-lookup"><span data-stu-id="3c275-163">Visual controls on a webpage cannot access a **Recordset** object directly.</span></span> <span data-ttu-id="3c275-164">Однако они могут получить доступ к **объекту Recordset** через [RDS. DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="3c275-164">However, they can access the **Recordset** object through the [RDS.DataControl](datacontrol-object-rds.md).</span></span> <span data-ttu-id="3c275-165">The **RDS. DataControl** становится доступной с помощью визуального управления, когда его свойство [SourceRecordset](recordset-sourcerecordset-properties-rds.md) задалось **объекту Recordset.**</span><span class="sxs-lookup"><span data-stu-id="3c275-165">The **RDS.DataControl** becomes usable by a visual control when its [SourceRecordset](recordset-sourcerecordset-properties-rds.md) property is set to the **Recordset** object.</span></span>

<span data-ttu-id="3c275-166">Объект визуального управления должен иметь параметр **DATASRC** для **RDS. DataControl и** его **свойство DATAFLD** задают объектное поле **Recordset** (столбец).</span><span class="sxs-lookup"><span data-stu-id="3c275-166">The visual control object must have its **DATASRC** parameter set to the **RDS.DataControl**, and its **DATAFLD** property set to a **Recordset** object field (column).</span></span>

<span data-ttu-id="3c275-167">В этом руководстве задай свойство **SourceRecordset:**</span><span class="sxs-lookup"><span data-stu-id="3c275-167">In this tutorial, set the **SourceRecordset** property:</span></span>

```vb 
 
Sub RDSTutorial5() 
 Dim DS as New RDS.DataSpace 
 Dim RS as ADODB.Recordset 
 Dim DC as New RDS.DataControl 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
 DC.SourceRecordset = RS ' Visual controls can now bind to DC. 
... 
```

## <a name="step-6-changes-are-sent-to-the-server"></a><span data-ttu-id="3c275-168">Шаг 6. Изменения отправляются на сервер</span><span class="sxs-lookup"><span data-stu-id="3c275-168">Step 6: Changes are sent to the server</span></span>

<span data-ttu-id="3c275-169">Если объект **Recordset** редактирован, все изменения (то есть строки, которые добавляются, меняются или удаляются) могут быть отправлены обратно на сервер.</span><span class="sxs-lookup"><span data-stu-id="3c275-169">If the **Recordset** object is edited, any changes (that is, rows that are added, changed, or deleted) can be sent back to the server.</span></span>

<span data-ttu-id="3c275-170">По умолчанию поведение RDS можно вызывать неявно с объектами ADO и поставщиком remoting Microsoft OLE DB.</span><span class="sxs-lookup"><span data-stu-id="3c275-170">The default behavior of RDS can be invoked implicitly with ADO objects and the Microsoft OLE DB Remoting Provider.</span></span> <span data-ttu-id="3c275-171">Запросы могут возвращать **наборы записей,** а измененные наборы записей **могут** обновлять источник данных.</span><span class="sxs-lookup"><span data-stu-id="3c275-171">Queries can return **Recordsets**, and edited **Recordsets** can update the data source.</span></span> <span data-ttu-id="3c275-172">В этом руководстве не вызывается RDS с объектами ADO, но это будет выглядеть, если он сделал:</span><span class="sxs-lookup"><span data-stu-id="3c275-172">This tutorial does not invoke RDS with ADO objects, but this is how it would look if it did:</span></span>

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "SELECT * FROM Authors","Provider=MS Remote;Data Source=Pubs;" & _ 
 "Remote Server=https://yourServer;Remote Provider=SQLOLEDB;" 
... ' Edit the Recordset. 
rs.UpdateBatch ' The equivalent of SubmitChanges. 
... 
```

### <a name="part-a"></a><span data-ttu-id="3c275-173">Часть A</span><span class="sxs-lookup"><span data-stu-id="3c275-173">Part A</span></span>

<span data-ttu-id="3c275-174">Предположим, что в этом случае используется только [RDS. DataControl](datacontrol-object-rds.md) и объект **Recordset** теперь связаны с **RDS. DataControl**.</span><span class="sxs-lookup"><span data-stu-id="3c275-174">Assume for this case that you have only used the [RDS.DataControl](datacontrol-object-rds.md) and that a **Recordset** object is now associated with the **RDS.DataControl**.</span></span> <span data-ttu-id="3c275-175">Метод [SubmitChanges](submitchanges-method-rds.md) обновляет источник данных с любыми изменениями в [](server-property-rds.md) **объекте Recordset,** если Подключение сервер и свойства по-прежнему настроены. [](connect-property-rds.md)</span><span class="sxs-lookup"><span data-stu-id="3c275-175">The [SubmitChanges](submitchanges-method-rds.md) method updates the data source with any changes to the **Recordset** object if the [Server](server-property-rds.md) and [Connect](connect-property-rds.md) properties are still set.</span></span>

```vb 
 
Sub RDSTutorial6A() 
Dim DC as New RDS.DataControl 
Dim RS as ADODB.Recordset 
DC.Server = "https://yourServer" 
DC.Connect = "DSN=Pubs" 
DC.SQL = "SELECT * FROM Authors" 
DC.Refresh 
... 
Set RS = DC.Recordset 
 ' Edit the Recordset. 
... 
DC.SubmitChanges 
... 
```

### <a name="part-b"></a><span data-ttu-id="3c275-176">Часть B</span><span class="sxs-lookup"><span data-stu-id="3c275-176">Part B</span></span>

<span data-ttu-id="3c275-177">Кроме того, можно обновить сервер с помощью [объекта RDSServer.DataFactory,](datafactory-object-rdsserver.md) указав подключение и объект **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="3c275-177">Alternatively, you could update the server with the [RDSServer.DataFactory](datafactory-object-rdsserver.md) object, specifying a connection and a **Recordset** object.</span></span>

```vb 
 
Sub RDSTutorial6B() 
Dim DS As New RDS.DataSpace 
Dim RS As ADODB.Recordset 
Dim DC As New RDS.DataControl 
Dim DF As Object 
Dim blnStatus As Boolean 
Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
DC.SourceRecordset = RS ' Visual controls can now bind to DC. 
 ' Edit the Recordset. 
blnStatus = DF.SubmitChanges "DSN=Pubs", RS 
End Sub 
```


## <a name="appendix-a-rds-tutorial-vbscript"></a><span data-ttu-id="3c275-178">Приложение A: учебник по RDS (VBScript)</span><span class="sxs-lookup"><span data-stu-id="3c275-178">Appendix A: RDS tutorial (VBScript)</span></span>

<span data-ttu-id="3c275-179">Это учебник по RDS, написанный в Microsoft Visual Basic Scripting Edition.</span><span class="sxs-lookup"><span data-stu-id="3c275-179">This is the RDS tutorial, written in Microsoft Visual Basic Scripting Edition.</span></span> <span data-ttu-id="3c275-180">Описание цели этого руководства см. в разделе Введение к этой теме.</span><span class="sxs-lookup"><span data-stu-id="3c275-180">For a description of the purpose of this tutorial, see the introduction to this topic.</span></span>

<span data-ttu-id="3c275-181">В этом руководстве [RDS. DataControl](datacontrol-object-rds.md) и [RDS. DataSpace](dataspace-object-rds.md) создается во время разработки; то есть они определяются тегами объектов.</span><span class="sxs-lookup"><span data-stu-id="3c275-181">In this tutorial, [RDS.DataControl](datacontrol-object-rds.md) and [RDS.DataSpace](dataspace-object-rds.md) are created at design time; that is, they are defined with object tags.</span></span> <span data-ttu-id="3c275-182">Кроме того, они могут быть созданы во время запуска с помощью **метода Server.CreateObject.**</span><span class="sxs-lookup"><span data-stu-id="3c275-182">Alternatively, they could be created at run time with the **Server.CreateObject** method.</span></span> 

<span data-ttu-id="3c275-183">Например, **RDS. Объект DataControl** можно создать так:</span><span class="sxs-lookup"><span data-stu-id="3c275-183">For example, the **RDS.DataControl** object could be created like this:</span></span>

```vb
    Set DC = Server.CreateObject("RDS.DataControl") 
     <!-- RDS.DataControl --> 
     <OBJECT 
     ID="DC1" CLASSID="CLSID:BD96C556-65A3-11D0-983A-00C04FC29E33"> 
     </OBJECT> 
     
     <!-- RDS.DataSpace --> 
     <OBJECT 
     ID="DS1" WIDTH=1 HEIGHT=1 
     CLASSID="CLSID:BD96C556-65A3-11D0-983A-00C04FC29E36"> 
     </OBJECT> 
     
     <SCRIPT LANGUAGE="VBScript"> 
     
     Sub RDSTutorial() 
     Dim DF1 
```

### <a name="step-1-specify-a-server-program"></a><span data-ttu-id="3c275-184">Шаг 1. Укажите серверную программу</span><span class="sxs-lookup"><span data-stu-id="3c275-184">Step 1: Specify a server program</span></span>

<span data-ttu-id="3c275-185">VBScript может узнать имя веб-сервера IIS, на который он запущен, обратившись к методу VBScript **Request.ServerVariables,** доступному ASP:</span><span class="sxs-lookup"><span data-stu-id="3c275-185">VBScript can discover the name of the IIS web server it is running on by accessing the VBScript **Request.ServerVariables** method available to Active Server Pages:</span></span>

```vb 
 
"https://<%=Request.ServerVariables("SERVER_NAME")%>" 
```

<span data-ttu-id="3c275-186">Однако для этого руководства используйте воображаемый сервер "yourServer".</span><span class="sxs-lookup"><span data-stu-id="3c275-186">However, for this tutorial, use the imaginary server, "yourServer."</span></span>

> [!NOTE]
> <span data-ttu-id="3c275-187">Обратите внимание на тип данных **аргументов ByRef.**</span><span class="sxs-lookup"><span data-stu-id="3c275-187">Pay attention to the data type of **ByRef** arguments.</span></span> <span data-ttu-id="3c275-188">VBScript не дает указать тип переменной, поэтому всегда необходимо передать вариант.</span><span class="sxs-lookup"><span data-stu-id="3c275-188">VBScript does not let you specify the variable type, so you must always pass a Variant.</span></span> <span data-ttu-id="3c275-189">При использовании HTTP, RDS позволит передать вариант методу, который ожидает, что не вариант, если вы вызываете его с **RDS. Метод Объекта DataSpace** [CreateObject.](createobject-method-rds.md)</span><span class="sxs-lookup"><span data-stu-id="3c275-189">When using HTTP, RDS will allow you to pass a Variant to a method that expects a non-Variant if you invoke it with the **RDS.DataSpace** object [CreateObject](createobject-method-rds.md) method.</span></span> <span data-ttu-id="3c275-190">При использовании DCOM или в процессе сервера соизмерять типы параметров на стороне клиента и сервера или вы получите ошибку "Type Mismatch".</span><span class="sxs-lookup"><span data-stu-id="3c275-190">When using DCOM or an in-process server, match the parameter types on the client and server sides or you will receive a "Type Mismatch" error.</span></span>

```vb
 
Set DF1 = DS1.CreateObject("RDSServer.DataFactory", "https://yourServer") 
```

### <a name="step-2-part-a-invoke-the-server-program-with-rdsdatacontrol"></a><span data-ttu-id="3c275-191">Шаг 2, часть A. Вызов серверной программы с помощью RDS. DataControl</span><span class="sxs-lookup"><span data-stu-id="3c275-191">Step 2, Part A: Invoke the server program with RDS.DataControl</span></span>

<span data-ttu-id="3c275-192">В этом примере просто комментарий, демонстрирующий, что поведение **RDS по умолчанию. DataControl** выполняет указанный запрос.</span><span class="sxs-lookup"><span data-stu-id="3c275-192">This example is merely a comment demonstrating that the default behavior of the **RDS.DataControl** is to perform the specified query.</span></span>

```vb
 
<OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="DC1"> 
 <PARAM NAME="SQL" VALUE="SELECT * FROM Authors"> 
 <PARAM NAME="Connect" VALUE="DSN=Pubs;"> 
 <PARAM NAME="Server" VALUE="https://yourServer/"> 
</OBJECT> 
... 
<SCRIPT LANGUAGE="VBScript"> 
 
Sub RDSTutorial2A() 
 Dim RS 
 DC1.Refresh 
 Set RS = DC1.Recordset 
... 
```

<span data-ttu-id="3c275-193">Перейти к следующему шагу.</span><span class="sxs-lookup"><span data-stu-id="3c275-193">Skip to the following step.</span></span>

### <a name="step-4-server-returns-the-recordset"></a><span data-ttu-id="3c275-194">Шаг 4. Сервер возвращает набор записей</span><span class="sxs-lookup"><span data-stu-id="3c275-194">Step 4: Server returns the Recordset</span></span>

```vb
 
Set RS = DF1.Query("DSN=Pubs;", "SELECT * FROM Authors") 
```

### <a name="step-5-datacontrol-is-made-usable-by-visual-controls"></a><span data-ttu-id="3c275-195">Шаг 5. DataControl может быть выполнен с помощью визуальных элементов управления</span><span class="sxs-lookup"><span data-stu-id="3c275-195">Step 5: DataControl is made usable by visual controls</span></span>

```vb
 
' Assign the returned recordset to the DataControl. 
 
DC1.SourceRecordset = RS 
```

### <a name="step-6-part-a-changes-are-sent-to-the-server-with-rdsdatacontrol"></a><span data-ttu-id="3c275-196">Шаг 6, часть A. Изменения отправляются на сервер с помощью RDS. DataControl</span><span class="sxs-lookup"><span data-stu-id="3c275-196">Step 6, Part A: Changes are sent to the server with RDS.DataControl</span></span>

<span data-ttu-id="3c275-197">Этот пример — это просто комментарий, демонстрирующий, как **работает RDS. DataControl** выполняет обновления.</span><span class="sxs-lookup"><span data-stu-id="3c275-197">This example is merely a comment demonstrating how the **RDS.DataControl** performs updates.</span></span>

```vb
 
<OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="DC1"> 
 <PARAM NAME="SQL" VALUE="SELECT * FROM Authors"> 
 <PARAM NAME="Connect" VALUE="DSN=Pubs;"> 
 <PARAM NAME="Server" VALUE="https://yourServer/"> 
</OBJECT> 
... 
<SCRIPT LANGUAGE="VBScript"> 
 
Sub RDSTutorial6A() 
Dim RS 
DC1.Refresh 
... 
Set RS = DC1.Recordset 
' Edit the Recordset object... 
' The SERVER and CONNECT properties are already set from Step 2A. 
Set DC1.SourceRecordset = RS 
... 
DC1.SubmitChanges 
```

### <a name="step-6-part-b-changes-are-sent-to-the-server-with-rdsserverdatafactory"></a><span data-ttu-id="3c275-198">Шаг 6, часть B. Изменения отправляются на сервер с помощью RDSServer.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3c275-198">Step 6, Part B: Changes are sent to the server with RDSServer.DataFactory</span></span>

```vb
 
DF.SubmitChanges"DSN=Pubs", RS 
 
End Sub 
</SCRIPT> 
</BODY> 
</HTML> 
```

## <a name="appendix-b-rds-tutorial-visual-j"></a><span data-ttu-id="3c275-199">Приложение B. Учебник по RDS (Visual J++)</span><span class="sxs-lookup"><span data-stu-id="3c275-199">Appendix B: RDS tutorial (Visual J++)</span></span>

<span data-ttu-id="3c275-200">ADO/WFC не полностью следует объектной модели RDS в том, что она не реализует [RDS. Объект DataControl.](datacontrol-object-rds.md)</span><span class="sxs-lookup"><span data-stu-id="3c275-200">ADO/WFC does not completely follow the RDS object model in that it does not implement the [RDS.DataControl](datacontrol-object-rds.md) object.</span></span> <span data-ttu-id="3c275-201">ADO/WFC реализует только клиентский класс [RDS. DataSpace](dataspace-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="3c275-201">ADO/WFC only implements the client-side class, [RDS.DataSpace](dataspace-object-rds.md).</span></span>

<span data-ttu-id="3c275-202">Класс **DataSpace** реализует один метод [CreateObject,](createobject-method-rds.md)который возвращает [объект ObjectProxy.](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/objectproxy-ado-wfc-syntax)</span><span class="sxs-lookup"><span data-stu-id="3c275-202">The **DataSpace** class implements one method, [CreateObject](createobject-method-rds.md), which returns an [ObjectProxy](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/objectproxy-ado-wfc-syntax) object.</span></span> <span data-ttu-id="3c275-203">Класс **DataSpace** также реализует свойство [InternetTimeout.](internettimeout-property-rds.md)</span><span class="sxs-lookup"><span data-stu-id="3c275-203">The **DataSpace** class also implements the [InternetTimeout](internettimeout-property-rds.md) property.</span></span>

<span data-ttu-id="3c275-204">Класс **ObjectProxy** реализует один метод вызов, который может вызывать любой бизнес-объект на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="3c275-204">The **ObjectProxy** class implements one method, call, which can invoke any server-side business object.</span></span>

```java 
 
import com.ms.wfc.data.*; 
public class RDSTutorial 
{ 
 public void tutorial() 
 { 
// Step 1: Specify a server program. 
 ObjectProxy obj = 
 DataSpace.createObject( 
 "RDSServer.DataFactory", 
 "https://YourServer"); 
 
// Step 2: Server returns a Recordset. 
 Recordset rs = (Recordset) obj.call( 
 "Query", 
 new Object[] {"DSN=Pubs;", "SELECT * FROM Authors"}); 
 
// Step 3: Changes are sent to the server. 
 ... // Edit Recordset. 
 obj.call( 
 "SubmitChanges", 
 new Object[] {"DSN=Pubs;", rs}); 
 return; 
 } 
} 
```



