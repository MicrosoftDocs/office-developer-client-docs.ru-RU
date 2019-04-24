---
title: 'Глава 12: руководство по удаленным службам данных (RDS)'
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
# <a name="chapter-12-remote-data-service-rds-tutorial"></a><span data-ttu-id="1c48f-102">Глава 12: руководство по удаленным службам данных (RDS)</span><span class="sxs-lookup"><span data-stu-id="1c48f-102">Chapter 12: Remote Data Service (RDS) tutorial</span></span>

<span data-ttu-id="1c48f-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1c48f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1c48f-104">В этом руководстве показано, как использовать модель программирования RDS для запроса и обновления источника данных.</span><span class="sxs-lookup"><span data-stu-id="1c48f-104">This tutorial illustrates using the RDS programming model to query and update a data source.</span></span> <span data-ttu-id="1c48f-105">Сначала он описывает действия, необходимые для выполнения этой задачи.</span><span class="sxs-lookup"><span data-stu-id="1c48f-105">First, it describes the steps necessary to accomplish this task.</span></span> <span data-ttu-id="1c48f-106">После этого руководство повторяется в Microsoft Visual Basic Scripting Edition и Microsoft Visual J++, на которых можно использовать классы ADO для Windows Foundation (ADO/WFC).</span><span class="sxs-lookup"><span data-stu-id="1c48f-106">Then the tutorial is repeated in Microsoft Visual Basic Scripting Edition and Microsoft Visual J++, featuring ADO for Windows Foundation Classes (ADO/WFC).</span></span>

<span data-ttu-id="1c48f-107">Это руководство запрограммировано на разных языках по двум причинам:</span><span class="sxs-lookup"><span data-stu-id="1c48f-107">This tutorial is coded in different languages for two reasons:</span></span>

- <span data-ttu-id="1c48f-108">Документация для RDS предполагает, что коды средства чтения в Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="1c48f-108">The documentation for RDS assumes the reader codes in Visual Basic.</span></span> <span data-ttu-id="1c48f-109">Это делает документацию удобной для программистов Visual Basic, но не менее полезна для программистов, использующих другие языки.</span><span class="sxs-lookup"><span data-stu-id="1c48f-109">This makes the documentation convenient for Visual Basic programmers, but less useful for programmers who use other languages.</span></span>

- <span data-ttu-id="1c48f-110">Если вы не уверены в определенном компоненте RDS и вы знаете немного другого языка, вы можете разрешить свой вопрос, выполнив поиск того же компонента, представленного на другом языке.</span><span class="sxs-lookup"><span data-stu-id="1c48f-110">If you are uncertain about a particular RDS feature and you know a little of another language, you might be able to resolve your question by looking for the same feature expressed in another language.</span></span>

<span data-ttu-id="1c48f-111">Это руководство основано на модели программирования RDS.</span><span class="sxs-lookup"><span data-stu-id="1c48f-111">This tutorial is based on the RDS programming model.</span></span> <span data-ttu-id="1c48f-112">Здесь обсуждается каждый шаг модели программирования по отдельности.</span><span class="sxs-lookup"><span data-stu-id="1c48f-112">It discusses each step of the programming model individually.</span></span> <span data-ttu-id="1c48f-113">Кроме того, он иллюстрирует каждый шаг с фрагментом кода Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="1c48f-113">In addition, it illustrates each step with a fragment of Visual Basic code.</span></span>

<span data-ttu-id="1c48f-114">Пример кода повторяется на других языках с минимальным обсуждением.</span><span class="sxs-lookup"><span data-stu-id="1c48f-114">The code example is repeated in other languages with minimal discussion.</span></span> <span data-ttu-id="1c48f-115">Каждый шаг в данном руководстве по языку программирования отмечен соответствующими шагами в модели программирования и в описательном руководстве.</span><span class="sxs-lookup"><span data-stu-id="1c48f-115">Each step in a given programming language tutorial is marked with the corresponding step in the programming model and descriptive tutorial.</span></span> <span data-ttu-id="1c48f-116">Используйте номер шага, чтобы сослаться на обсуждение в подробном руководстве.</span><span class="sxs-lookup"><span data-stu-id="1c48f-116">Use the number of the step to refer to the discussion in the descriptive tutorial.</span></span>

<span data-ttu-id="1c48f-117">Ниже приведен пример модели программирования RDS.</span><span class="sxs-lookup"><span data-stu-id="1c48f-117">The RDS programming model is stated below.</span></span> <span data-ttu-id="1c48f-118">Используйте его в качестве схемы, когда вы пройдете в руководстве.</span><span class="sxs-lookup"><span data-stu-id="1c48f-118">Use it as a roadmap as you proceed through the tutorial.</span></span>

### <a name="rds-programming-model-with-objects"></a><span data-ttu-id="1c48f-119">Модель программирования RDS с объектами</span><span class="sxs-lookup"><span data-stu-id="1c48f-119">RDS programming model with objects</span></span>

- <span data-ttu-id="1c48f-120">Укажите программу, которая будет вызываться на сервере, и получите способ (прокси) для ссылки на него из клиента.</span><span class="sxs-lookup"><span data-stu-id="1c48f-120">Specify the program to be invoked on the server, and obtain a way (proxy) to refer to it from the client.</span></span>

- <span data-ttu-id="1c48f-121">Вызов серверной программы.</span><span class="sxs-lookup"><span data-stu-id="1c48f-121">Invoke the server program.</span></span> <span data-ttu-id="1c48f-122">Передайте параметры в серверную программу, определяющую источник данных, и команду, которая будет выдаваться.</span><span class="sxs-lookup"><span data-stu-id="1c48f-122">Pass parameters to the server program that identifies the data source and the command to issue.</span></span>

- <span data-ttu-id="1c48f-123">Серверная программа получает объект [Recordset](recordset-object-ado.md) из источника данных, как правило, с помощью ADO.</span><span class="sxs-lookup"><span data-stu-id="1c48f-123">The server program obtains a [Recordset](recordset-object-ado.md) object from the data source, typically by using ADO.</span></span> <span data-ttu-id="1c48f-124">При необходимости объект **Recordset** обрабатывается на сервере.</span><span class="sxs-lookup"><span data-stu-id="1c48f-124">Optionally, the **Recordset** object is processed on the server.</span></span>

- <span data-ttu-id="1c48f-125">Серверная программа возвращает конечный объект **Recordset** клиентскому приложению.</span><span class="sxs-lookup"><span data-stu-id="1c48f-125">The server program returns the final **Recordset** object to the client application.</span></span>

- <span data-ttu-id="1c48f-126">В клиенте объект **Recordset** можно дополнительно поместить в форму, которая может быть легко использоваться визуальными элементами управления.</span><span class="sxs-lookup"><span data-stu-id="1c48f-126">On the client, the **Recordset** object is optionally put into a form that can be easily used by visual controls.</span></span>

- <span data-ttu-id="1c48f-127">Изменения объекта **Recordset** отправляются обратно на сервер и используются для обновления источника данных.</span><span class="sxs-lookup"><span data-stu-id="1c48f-127">Changes to the **Recordset** object are sent back to the server and used to update the data source.</span></span>

## <a name="step-1-specify-a-server-program"></a><span data-ttu-id="1c48f-128">Шаг 1: указание серверной программы</span><span class="sxs-lookup"><span data-stu-id="1c48f-128">Step 1: Specify a server program</span></span>

<span data-ttu-id="1c48f-129">В общем случае используйте [RDS. ](dataspace-object-rds.md)Метод [CreateObject](createobject-method-rds.md) объекта Space для указания программы сервера по умолчанию, [рдссервер.](datafactory-object-rdsserver.md)DataObject или собственной настраиваемой серверной программы (бизнес-объект).</span><span class="sxs-lookup"><span data-stu-id="1c48f-129">In the most general case, use the [RDS.DataSpace](dataspace-object-rds.md) object [CreateObject](createobject-method-rds.md) method to specify the default server program, [RDSServer.DataFactory](datafactory-object-rdsserver.md), or your own custom server program (business object).</span></span> <span data-ttu-id="1c48f-130">На сервере создается экземпляр серверной программы, а также возвращается ссылка на программу или *прокси-* сервер.</span><span class="sxs-lookup"><span data-stu-id="1c48f-130">A server program is instantiated on the server, and a reference to the server program, or *proxy*, is returned.</span></span>

<span data-ttu-id="1c48f-131">В этом руководстве используется серверная программа по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="1c48f-131">This tutorial uses the default server program:</span></span>

```vb 
 
Sub RDSTutorial1() 
 Dim DS as New RDS.DataSpace 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
... 
``` 

## <a name="step-2-invoke-the-server-program"></a><span data-ttu-id="1c48f-132">Шаг 2: вызов серверной программы</span><span class="sxs-lookup"><span data-stu-id="1c48f-132">Step 2: Invoke the server program</span></span> 

<span data-ttu-id="1c48f-133">При вызове метода на клиентском *прокси*фактическая программа на сервере выполняет метод.</span><span class="sxs-lookup"><span data-stu-id="1c48f-133">When you invoke a method on the client *proxy*, the actual program on the server executes the method.</span></span> <span data-ttu-id="1c48f-134">На этом этапе вы выполняете запрос на сервере.</span><span class="sxs-lookup"><span data-stu-id="1c48f-134">In this step, you'll execute a query on the server.</span></span>

### <a name="part-a"></a><span data-ttu-id="1c48f-135">Часть A</span><span class="sxs-lookup"><span data-stu-id="1c48f-135">Part A</span></span>

<span data-ttu-id="1c48f-136">Если вы не использовали [рдссервер.](datafactory-object-rdsserver.md) в этом руководстве, самый удобный способ выполнения этого действия — использование [RDS. Объект управления](datacontrol-object-rds.md) DataObject.</span><span class="sxs-lookup"><span data-stu-id="1c48f-136">If you weren't using [RDSServer.DataFactory](datafactory-object-rdsserver.md) in this tutorial, the most convenient way to perform this step would be to use the [RDS.DataControl](datacontrol-object-rds.md) object.</span></span> <span data-ttu-id="1c48f-137">**RDS. Элемент управления** данными объединяет предыдущий этап создания прокси-сервера с помощью этого шага, выдавая запрос.</span><span class="sxs-lookup"><span data-stu-id="1c48f-137">The **RDS.DataControl** combines the previous step of creating a proxy, with this step, issuing the query.</span></span>

1. <span data-ttu-id="1c48f-138">Задайте для \*\*RDS. \*\*Свойство [сервера](server-property-rds.md) объектов DataObject для определения места создания экземпляра программы сервера.</span><span class="sxs-lookup"><span data-stu-id="1c48f-138">Set the **RDS.DataControl** object [Server](server-property-rds.md) property to identify where the server program should be instantiated.</span></span>

2. <span data-ttu-id="1c48f-139">Задайте свойство [Connect](connect-property-rds.md) , чтобы указать строку подключения для доступа к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="1c48f-139">Set the [Connect](connect-property-rds.md) property to specify the connect string to access the data source.</span></span>

3. <span data-ttu-id="1c48f-140">Задайте свойство [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) , чтобы указать текст команды запроса.</span><span class="sxs-lookup"><span data-stu-id="1c48f-140">Set the [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) property to specify the query command text.</span></span> 

4. <span data-ttu-id="1c48f-141">ВыДайте метод [Refresh](refresh-method-rds.md) для подключения программы сервера к источнику данных, получения строк, указанных запросом, и возврата объекта **Recordset** клиенту.</span><span class="sxs-lookup"><span data-stu-id="1c48f-141">Issue the [Refresh](refresh-method-rds.md) method to cause the server program to connect to the data source, retrieve rows specified by the query, and return a **Recordset** object to the client.</span></span>

<span data-ttu-id="1c48f-142">В этом руководстве не используется **RDS. Элемент управления**данным, но это будет выглядеть, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="1c48f-142">This tutorial does not use the **RDS.DataControl**, but this is how it would look if it did:</span></span>

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

<span data-ttu-id="1c48f-143">Кроме того, не вызывайте группу RDS с объектами ADO, но вот как она будет выглядеть:</span><span class="sxs-lookup"><span data-stu-id="1c48f-143">Nor does the tutorial invoke RDS with ADO objects, but this is how it would look if it did:</span></span>

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "SELECT * FROM Authors","Provider=MS Remote;Data Source=Pubs;" & _ 
"Remote Server=https://yourServer;Remote Provider=SQLOLEDB;" 
```

### <a name="part-b"></a><span data-ttu-id="1c48f-144">Часть B</span><span class="sxs-lookup"><span data-stu-id="1c48f-144">Part B</span></span>

<span data-ttu-id="1c48f-145">Общий метод выполнения этого действия — вызов метода [запроса](query-method-rds.md) **рдссервер.** DataObject.</span><span class="sxs-lookup"><span data-stu-id="1c48f-145">The general method of performing this step is to invoke the **RDSServer.DataFactory** object [Query](query-method-rds.md) method.</span></span> <span data-ttu-id="1c48f-146">Этот метод принимает строку подключения, используемую для подключения к источнику данных, и текст команды, который используется для указания строк, возвращаемых из источника данных.</span><span class="sxs-lookup"><span data-stu-id="1c48f-146">That method takes a connect string, which is used to connect to a data source, and a command text, which is used to specify the rows to be returned from the data source.</span></span>

<span data-ttu-id="1c48f-147">В этом руководстве используется \*\*\*\* метод **запроса** объектов DataObject.</span><span class="sxs-lookup"><span data-stu-id="1c48f-147">This tutorial uses the **DataFactory** object **Query** method:</span></span>

```vb 
 
Sub RDSTutorial2B() 
 Dim DS as New RDS.DataSpace 
 Dim DF 
 Dim RS as ADODB.Recordset 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
... 
```

## <a name="step-3-server-obtains-a-recordset"></a><span data-ttu-id="1c48f-148">Шаг 3: сервер получает объект Recordset</span><span class="sxs-lookup"><span data-stu-id="1c48f-148">Step 3: Server obtains a Recordset</span></span> 

<span data-ttu-id="1c48f-149">Серверная программа использует строку подключения и текст команды, чтобы запросить нужные строки в источнике данных.</span><span class="sxs-lookup"><span data-stu-id="1c48f-149">The server program uses the connect string and command text to query the data source for the desired rows.</span></span> <span data-ttu-id="1c48f-150">ADO обычно используется для извлечения этого объекта **Recordset**, хотя можно использовать другие интерфейсы доступа к данным Майкрософт, такие как OLE DB.</span><span class="sxs-lookup"><span data-stu-id="1c48f-150">ADO is typically used to retrieve this **Recordset**, although other Microsoft data access interfaces, such as OLE DB, could be used.</span></span>

<span data-ttu-id="1c48f-151">Пользовательская серверная программа может выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="1c48f-151">A custom server program might look like this:</span></span>

```vb 
 
Public Function ServerProgram(cn as String, qry as String) as Object 
Dim rs as New ADODB.Recordset 
 rs.CursorLocation = adUseClient 
 rs.Open qry, cn 
 rs.ActiveConnection = Nothing 
 Set ServerProgram = rs 
End Function 
```

## <a name="step-4-server-returns-the-recordset"></a><span data-ttu-id="1c48f-152">Шаг 4: сервер возвращает объект Recordset</span><span class="sxs-lookup"><span data-stu-id="1c48f-152">Step 4: Server returns the Recordset</span></span> 

<span data-ttu-id="1c48f-153">RDS преобразует полученный объект **Recordset** в форму, которая может быть отправлена обратно клиенту (то есть, *маршалирует* объект **Recordset**).</span><span class="sxs-lookup"><span data-stu-id="1c48f-153">RDS converts the retrieved **Recordset** object to a form that can be sent back to the client (that is, it *marshals* the **Recordset**).</span></span> <span data-ttu-id="1c48f-154">Точная форма преобразования и способ его отправки зависит от того, находится ли сервер в Интернете или интрасети, в локальной сети или в библиотеке динамической компоновки.</span><span class="sxs-lookup"><span data-stu-id="1c48f-154">The exact form of the conversion and how it is sent depends on whether the server is on the Internet or an intranet, a local area network, or is a dynamic-link library.</span></span> <span data-ttu-id="1c48f-155">Тем не менее, эти сведения не являются критическими; все, что имеет значение, это то, что RDS отправляет **набор записей** обратно клиенту.</span><span class="sxs-lookup"><span data-stu-id="1c48f-155">However, this detail is not critical; all that matters is that RDS sends the **Recordset** back to the client.</span></span>

<span data-ttu-id="1c48f-156">На стороне клиента возвращается объект **Recordset** и назначается локальной переменной.</span><span class="sxs-lookup"><span data-stu-id="1c48f-156">On the client side, a **Recordset** object is returned and assigned to a local variable.</span></span>

```vb 
 
Sub RDSTutorial4() 
 Dim DS as New RDS.DataSpace 
 Dim RS as ADODB.Recordset 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query("DSN=Pubs", "SELECT * FROM Authors") 
... 
```

## <a name="step-5-datacontrol-is-made-usable"></a><span data-ttu-id="1c48f-157">Шаг 5: управление этими процессами осуществляется</span><span class="sxs-lookup"><span data-stu-id="1c48f-157">Step 5: DataControl is made usable</span></span> 

<span data-ttu-id="1c48f-158">Возвращенный объект **Recordset** доступен для использования.</span><span class="sxs-lookup"><span data-stu-id="1c48f-158">The returned **Recordset** object is available for use.</span></span> <span data-ttu-id="1c48f-159">Вы можете просматривать, перемещать и изменять его, как и любой другой **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="1c48f-159">You can examine, navigate, or edit it as you would any other **Recordset**.</span></span> <span data-ttu-id="1c48f-160">Действия, которые можно выполнять с **наборОм записей** , зависят от среды.</span><span class="sxs-lookup"><span data-stu-id="1c48f-160">What you can do with the **Recordset** depends on your environment.</span></span> <span data-ttu-id="1c48f-161">Visual Basic и Visual C++ имеют визуальные элементы управления, которые могут напрямую или косвенно использовать **набор записей** с помощью элемента управления "включение данных".</span><span class="sxs-lookup"><span data-stu-id="1c48f-161">Visual Basic and Visual C++ have visual controls that can use a **Recordset** directly or indirectly with the aid of an enabling data control.</span></span>

<span data-ttu-id="1c48f-162">Например, при отображении веб-страницы в Internet Explorer может потребоваться отобразить данные объекта **Recordset** в визуальном элементе управления.</span><span class="sxs-lookup"><span data-stu-id="1c48f-162">For example, if you are displaying a webpage in Internet Explorer, you might want to display the **Recordset** object data in a visual control.</span></span> <span data-ttu-id="1c48f-163">Визуальные элементы управления на веб-странице не могут напрямую получить доступ к объекту **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="1c48f-163">Visual controls on a webpage cannot access a **Recordset** object directly.</span></span> <span data-ttu-id="1c48f-164">Тем не менее, они могут получить доступ к объекту **Recordset** с помощью [RDS. Элемент управления](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="1c48f-164">However, they can access the **Recordset** object through the [RDS.DataControl](datacontrol-object-rds.md).</span></span> <span data-ttu-id="1c48f-165">**RDS. Элемент управления** данным используется визуальным элементом управления, если его свойство [SourceRecordset](recordset-sourcerecordset-properties-rds.md) задано для объекта **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="1c48f-165">The **RDS.DataControl** becomes usable by a visual control when its [SourceRecordset](recordset-sourcerecordset-properties-rds.md) property is set to the **Recordset** object.</span></span>

<span data-ttu-id="1c48f-166">Для объекта визуального элемента управления должен быть задан параметр **датасрк** для **RDS. Элемент управления**данным и его свойство **датафлд** , заданное для поля объекта **Recordset** (Column).</span><span class="sxs-lookup"><span data-stu-id="1c48f-166">The visual control object must have its **DATASRC** parameter set to the **RDS.DataControl**, and its **DATAFLD** property set to a **Recordset** object field (column).</span></span>

<span data-ttu-id="1c48f-167">В этом руководстве показано, как задать свойство **SourceRecordset** :</span><span class="sxs-lookup"><span data-stu-id="1c48f-167">In this tutorial, set the **SourceRecordset** property:</span></span>

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

## <a name="step-6-changes-are-sent-to-the-server"></a><span data-ttu-id="1c48f-168">Шаг 6: изменения отправляются на сервер</span><span class="sxs-lookup"><span data-stu-id="1c48f-168">Step 6: Changes are sent to the server</span></span>

<span data-ttu-id="1c48f-169">Если объект **Recordset** редактируется, любые изменения (то есть добавленные, измененные или удаленные строки) можно отправить обратно на сервер.</span><span class="sxs-lookup"><span data-stu-id="1c48f-169">If the **Recordset** object is edited, any changes (that is, rows that are added, changed, or deleted) can be sent back to the server.</span></span>

<span data-ttu-id="1c48f-170">Поведение RDS, используемое по умолчанию, может быть неявно вызвано объектами ADO и поставщиком удаленного взаимодействия Microsoft OLE DB.</span><span class="sxs-lookup"><span data-stu-id="1c48f-170">The default behavior of RDS can be invoked implicitly with ADO objects and the Microsoft OLE DB Remoting Provider.</span></span> <span data-ttu-id="1c48f-171">Запросы могут возвращать **наборы записей**, а измененные **наборы записей** могут обновлять источник данных.</span><span class="sxs-lookup"><span data-stu-id="1c48f-171">Queries can return **Recordsets**, and edited **Recordsets** can update the data source.</span></span> <span data-ttu-id="1c48f-172">В этом руководстве не происходит вызов RDS с объектами ADO, но именно так она будет выглядеть:</span><span class="sxs-lookup"><span data-stu-id="1c48f-172">This tutorial does not invoke RDS with ADO objects, but this is how it would look if it did:</span></span>

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "SELECT * FROM Authors","Provider=MS Remote;Data Source=Pubs;" & _ 
 "Remote Server=https://yourServer;Remote Provider=SQLOLEDB;" 
... ' Edit the Recordset. 
rs.UpdateBatch ' The equivalent of SubmitChanges. 
... 
```

### <a name="part-a"></a><span data-ttu-id="1c48f-173">Часть A</span><span class="sxs-lookup"><span data-stu-id="1c48f-173">Part A</span></span>

<span data-ttu-id="1c48f-174">Предположим, что в этом случае использовались только [RDS. Элемент управления](datacontrol-object-rds.md) данными и объект **Recordset** теперь связан с элементом **ActiveX RDS. Элемент управления**.</span><span class="sxs-lookup"><span data-stu-id="1c48f-174">Assume for this case that you have only used the [RDS.DataControl](datacontrol-object-rds.md) and that a **Recordset** object is now associated with the **RDS.DataControl**.</span></span> <span data-ttu-id="1c48f-175">Метод [SubmitChanges](submitchanges-method-rds.md) обновляет источник данных с использованием любых изменений объекта **Recordset** , если свойства [Server](server-property-rds.md) и [Connect](connect-property-rds.md) по-прежнему заданы.</span><span class="sxs-lookup"><span data-stu-id="1c48f-175">The [SubmitChanges](submitchanges-method-rds.md) method updates the data source with any changes to the **Recordset** object if the [Server](server-property-rds.md) and [Connect](connect-property-rds.md) properties are still set.</span></span>

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

### <a name="part-b"></a><span data-ttu-id="1c48f-176">Часть B</span><span class="sxs-lookup"><span data-stu-id="1c48f-176">Part B</span></span>

<span data-ttu-id="1c48f-177">Кроме того, вы можете обновить сервер с помощью объекта [рдссервер.](datafactory-object-rdsserver.md) DataObject, указав соединение и объект **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="1c48f-177">Alternatively, you could update the server with the [RDSServer.DataFactory](datafactory-object-rdsserver.md) object, specifying a connection and a **Recordset** object.</span></span>

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


## <a name="appendix-a-rds-tutorial-vbscript"></a><span data-ttu-id="1c48f-178">Приложение А: руководство по RDS (VBScript)</span><span class="sxs-lookup"><span data-stu-id="1c48f-178">Appendix A: RDS tutorial (VBScript)</span></span>

<span data-ttu-id="1c48f-179">Это руководство по RDS, написанное в Microsoft Visual Basic Scripting Edition.</span><span class="sxs-lookup"><span data-stu-id="1c48f-179">This is the RDS tutorial, written in Microsoft Visual Basic Scripting Edition.</span></span> <span data-ttu-id="1c48f-180">Описание назначения этого руководства представлено в статье Введение в эту статью.</span><span class="sxs-lookup"><span data-stu-id="1c48f-180">For a description of the purpose of this tutorial, see the introduction to this topic.</span></span>

<span data-ttu-id="1c48f-181">В этом руководстве [RDS. Элемент управления](datacontrol-object-rds.md) и [RDS. Пространство](dataspace-object-rds.md) , созданное во время конструирования; то есть они определяются с помощью тегов объекта.</span><span class="sxs-lookup"><span data-stu-id="1c48f-181">In this tutorial, [RDS.DataControl](datacontrol-object-rds.md) and [RDS.DataSpace](dataspace-object-rds.md) are created at design time; that is, they are defined with object tags.</span></span> <span data-ttu-id="1c48f-182">Кроме того, они могут быть созданы во время выполнения с помощью метода **Server. CreateObject** .</span><span class="sxs-lookup"><span data-stu-id="1c48f-182">Alternatively, they could be created at run time with the **Server.CreateObject** method.</span></span> 

<span data-ttu-id="1c48f-183">Например, элемент **ActiveX RDS. Объект элемента управления** данным может быть создан следующим образом:</span><span class="sxs-lookup"><span data-stu-id="1c48f-183">For example, the **RDS.DataControl** object could be created like this:</span></span>

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

### <a name="step-1-specify-a-server-program"></a><span data-ttu-id="1c48f-184">Шаг 1: указание серверной программы</span><span class="sxs-lookup"><span data-stu-id="1c48f-184">Step 1: Specify a server program</span></span>

<span data-ttu-id="1c48f-185">С помощью VBScript можно определить имя веб-сервера IIS, на котором он работает, путем доступа к методу **request. сервервариаблес** , доступный для ASP-страниц:</span><span class="sxs-lookup"><span data-stu-id="1c48f-185">VBScript can discover the name of the IIS web server it is running on by accessing the VBScript **Request.ServerVariables** method available to Active Server Pages:</span></span>

```vb 
 
"https://<%=Request.ServerVariables("SERVER_NAME")%>" 
```

<span data-ttu-id="1c48f-186">Однако в этом руководстве используется мнимой сервер "Йоурсервер".</span><span class="sxs-lookup"><span data-stu-id="1c48f-186">However, for this tutorial, use the imaginary server, "yourServer."</span></span>

> [!NOTE]
> <span data-ttu-id="1c48f-187">Обратите внимание на тип данных аргументов **ByRef** .</span><span class="sxs-lookup"><span data-stu-id="1c48f-187">Pay attention to the data type of **ByRef** arguments.</span></span> <span data-ttu-id="1c48f-188">VBScript не позволяет указать тип переменной, поэтому всегда необходимо передавать Variant.</span><span class="sxs-lookup"><span data-stu-id="1c48f-188">VBScript does not let you specify the variable type, so you must always pass a Variant.</span></span> <span data-ttu-id="1c48f-189">При использовании протокола HTTP RDS позволяет передать значение Variant методу, который ожидает неИзменяемый метод, если он будет вызван с помощью \*\*RDS. \*\*Метод [CreateObject](createobject-method-rds.md) объекта Space.</span><span class="sxs-lookup"><span data-stu-id="1c48f-189">When using HTTP, RDS will allow you to pass a Variant to a method that expects a non-Variant if you invoke it with the **RDS.DataSpace** object [CreateObject](createobject-method-rds.md) method.</span></span> <span data-ttu-id="1c48f-190">При использовании DCOM или внутрипроцессного сервера соответствуют типам параметров на стороне клиента и сервера, а также отображается сообщение об ошибке "неСоответствие типов".</span><span class="sxs-lookup"><span data-stu-id="1c48f-190">When using DCOM or an in-process server, match the parameter types on the client and server sides or you will receive a "Type Mismatch" error.</span></span>

```vb
 
Set DF1 = DS1.CreateObject("RDSServer.DataFactory", "https://yourServer") 
```

### <a name="step-2-part-a-invoke-the-server-program-with-rdsdatacontrol"></a><span data-ttu-id="1c48f-191">Этап 2, часть A: вызов серверной программы с помощью RDS. DataControl</span><span class="sxs-lookup"><span data-stu-id="1c48f-191">Step 2, Part A: Invoke the server program with RDS.DataControl</span></span>

<span data-ttu-id="1c48f-192">В этом примере показан только комментарий, демонстрирующий поведение RDS в качестве поведения по умолчанию **. Элемент управления** данных предназначен для выполнения указанного запроса.</span><span class="sxs-lookup"><span data-stu-id="1c48f-192">This example is merely a comment demonstrating that the default behavior of the **RDS.DataControl** is to perform the specified query.</span></span>

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

<span data-ttu-id="1c48f-193">Перейдите к следующему шагу.</span><span class="sxs-lookup"><span data-stu-id="1c48f-193">Skip to the following step.</span></span>

### <a name="step-4-server-returns-the-recordset"></a><span data-ttu-id="1c48f-194">Шаг 4: сервер возвращает объект Recordset</span><span class="sxs-lookup"><span data-stu-id="1c48f-194">Step 4: Server returns the Recordset</span></span>

```vb
 
Set RS = DF1.Query("DSN=Pubs;", "SELECT * FROM Authors") 
```

### <a name="step-5-datacontrol-is-made-usable-by-visual-controls"></a><span data-ttu-id="1c48f-195">Шаг 5: элемент управления с помощью визуальных элементов управления</span><span class="sxs-lookup"><span data-stu-id="1c48f-195">Step 5: DataControl is made usable by visual controls</span></span>

```vb
 
' Assign the returned recordset to the DataControl. 
 
DC1.SourceRecordset = RS 
```

### <a name="step-6-part-a-changes-are-sent-to-the-server-with-rdsdatacontrol"></a><span data-ttu-id="1c48f-196">Шаг 6, часть A: изменения отправляются на сервер с помощью RDS. DataControl</span><span class="sxs-lookup"><span data-stu-id="1c48f-196">Step 6, Part A: Changes are sent to the server with RDS.DataControl</span></span>

<span data-ttu-id="1c48f-197">В этом примере показан только комментарий, демонстрирующий, как **RDS. Элемент управления "элемент управления** " выполняет обновление.</span><span class="sxs-lookup"><span data-stu-id="1c48f-197">This example is merely a comment demonstrating how the **RDS.DataControl** performs updates.</span></span>

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

### <a name="step-6-part-b-changes-are-sent-to-the-server-with-rdsserverdatafactory"></a><span data-ttu-id="1c48f-198">Шаг 6, часть B: изменения отправляются на сервер с помощью Рдссервер. факты</span><span class="sxs-lookup"><span data-stu-id="1c48f-198">Step 6, Part B: Changes are sent to the server with RDSServer.DataFactory</span></span>

```vb
 
DF.SubmitChanges"DSN=Pubs", RS 
 
End Sub 
</SCRIPT> 
</BODY> 
</HTML> 
```

## <a name="appendix-b-rds-tutorial-visual-j"></a><span data-ttu-id="1c48f-199">Приложение Б: руководство по RDS (Visual J++)</span><span class="sxs-lookup"><span data-stu-id="1c48f-199">Appendix B: RDS tutorial (Visual J++)</span></span>

<span data-ttu-id="1c48f-200">ADO/WFC не полностью следит за объектной моделью RDS, так как он не реализует [RDS. Объект управления](datacontrol-object-rds.md) DataObject.</span><span class="sxs-lookup"><span data-stu-id="1c48f-200">ADO/WFC does not completely follow the RDS object model in that it does not implement the [RDS.DataControl](datacontrol-object-rds.md) object.</span></span> <span data-ttu-id="1c48f-201">ADO/WFC реализует только клиентский класс [RDS. Пространство для ввода](dataspace-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="1c48f-201">ADO/WFC only implements the client-side class, [RDS.DataSpace](dataspace-object-rds.md).</span></span>

<span data-ttu-id="1c48f-202">Класс **Space** реализует один метод, [CreateObject](createobject-method-rds.md), который возвращает объект [обжектпрокси](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/objectproxy-ado-wfc-syntax) .</span><span class="sxs-lookup"><span data-stu-id="1c48f-202">The **DataSpace** class implements one method, [CreateObject](createobject-method-rds.md), which returns an [ObjectProxy](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/objectproxy-ado-wfc-syntax) object.</span></span> <span data-ttu-id="1c48f-203">Класс **Space** также реализует свойство [InternetTimeout](internettimeout-property-rds.md) .</span><span class="sxs-lookup"><span data-stu-id="1c48f-203">The **DataSpace** class also implements the [InternetTimeout](internettimeout-property-rds.md) property.</span></span>

<span data-ttu-id="1c48f-204">Класс **обжектпрокси** реализует один метод, Call, который может вызывать любой серверный бизнес-объект.</span><span class="sxs-lookup"><span data-stu-id="1c48f-204">The **ObjectProxy** class implements one method, call, which can invoke any server-side business object.</span></span>

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



