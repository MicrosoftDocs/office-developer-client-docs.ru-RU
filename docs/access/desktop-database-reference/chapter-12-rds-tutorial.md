---
title: 'Глава 12: Учебник удаленной службы данных (RDS)'
TOCTitle: 'Chapter 12: RDS tutorial'
ms:assetid: fa44a5e8-e4df-dfdd-d7a1-a870ec3cabdd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250277(v=office.15)
ms:contentKeyID: 48548837
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aca77ac08688e643327bdbf229ab6c1dec40d109
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704807"
---
# <a name="chapter-12-remote-data-service-rds-tutorial"></a><span data-ttu-id="99501-102">Глава 12: Учебник удаленной службы данных (RDS)</span><span class="sxs-lookup"><span data-stu-id="99501-102">Chapter 12: Remote Data Service (RDS) tutorial</span></span>

<span data-ttu-id="99501-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="99501-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="99501-104">В этом руководстве описывается использование модели программирования служб удаленных рабочих СТОЛОВ для запроса и обновления в источнике данных.</span><span class="sxs-lookup"><span data-stu-id="99501-104">This tutorial illustrates using the RDS programming model to query and update a data source.</span></span> <span data-ttu-id="99501-105">Во-первых описываются действия, необходимые для выполнения этой задачи.</span><span class="sxs-lookup"><span data-stu-id="99501-105">First, it describes the steps necessary to accomplish this task.</span></span> <span data-ttu-id="99501-106">Затем учебника по повторяется в Microsoft Visual Basic Scripting Edition и Microsoft Visual J ++, продолжительностью ADO для Windows классов (ADO/WFC).</span><span class="sxs-lookup"><span data-stu-id="99501-106">Then the tutorial is repeated in Microsoft Visual Basic Scripting Edition and Microsoft Visual J++, featuring ADO for Windows Foundation Classes (ADO/WFC).</span></span>

<span data-ttu-id="99501-107">В этом руководстве закодированные на разных языках по двум причинам:</span><span class="sxs-lookup"><span data-stu-id="99501-107">This tutorial is coded in different languages for two reasons:</span></span>

- <span data-ttu-id="99501-108">В документации для служб удаленных рабочих СТОЛОВ предполагается коды чтения в Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="99501-108">The documentation for RDS assumes the reader codes in Visual Basic.</span></span> <span data-ttu-id="99501-109">Это делает документации удобным для программистов Visual Basic, но меньше полезен для программистов, использовать другие языки.</span><span class="sxs-lookup"><span data-stu-id="99501-109">This makes the documentation convenient for Visual Basic programmers, but less useful for programmers who use other languages.</span></span>

- <span data-ttu-id="99501-110">Если вы не уверены в определенный компонент служб удаленных рабочих СТОЛОВ и вам известно немного из другой язык, может иметь возможность сопоставлять вопрос, используя для одного компонента выразить на другом языке.</span><span class="sxs-lookup"><span data-stu-id="99501-110">If you are uncertain about a particular RDS feature and you know a little of another language, you might be able to resolve your question by looking for the same feature expressed in another language.</span></span>

<span data-ttu-id="99501-111">В этом руководстве основано на модели программирования служб удаленных рабочих СТОЛОВ.</span><span class="sxs-lookup"><span data-stu-id="99501-111">This tutorial is based on the RDS programming model.</span></span> <span data-ttu-id="99501-112">По отдельности рассматривается каждый шаг модели программирования.</span><span class="sxs-lookup"><span data-stu-id="99501-112">It discusses each step of the programming model individually.</span></span> <span data-ttu-id="99501-113">Кроме того показан фрагмент кода Visual Basic по каждому шагу.</span><span class="sxs-lookup"><span data-stu-id="99501-113">In addition, it illustrates each step with a fragment of Visual Basic code.</span></span>

<span data-ttu-id="99501-114">В примере кода повторяется на других языках с минимальными обсуждений.</span><span class="sxs-lookup"><span data-stu-id="99501-114">The code example is repeated in other languages with minimal discussion.</span></span> <span data-ttu-id="99501-115">Каждый шаг в учебном курсе заданного языка программирования в модель программирования и описания при помощи учебника по помечен соответствующие действия.</span><span class="sxs-lookup"><span data-stu-id="99501-115">Each step in a given programming language tutorial is marked with the corresponding step in the programming model and descriptive tutorial.</span></span> <span data-ttu-id="99501-116">Используйте номер шага для ссылки на обсуждения в описательное учебном курсе.</span><span class="sxs-lookup"><span data-stu-id="99501-116">Use the number of the step to refer to the discussion in the descriptive tutorial.</span></span>

<span data-ttu-id="99501-117">Модель программирования служб удаленных рабочих СТОЛОВ указанное ниже.</span><span class="sxs-lookup"><span data-stu-id="99501-117">The RDS programming model is stated below.</span></span> <span data-ttu-id="99501-118">Используйте его в качестве руководства, как во время выполнения учебника по.</span><span class="sxs-lookup"><span data-stu-id="99501-118">Use it as a roadmap as you proceed through the tutorial.</span></span>

### <a name="rds-programming-model-with-objects"></a><span data-ttu-id="99501-119">Модель программирования RDS с объектами</span><span class="sxs-lookup"><span data-stu-id="99501-119">RDS programming model with objects</span></span>

- <span data-ttu-id="99501-120">Укажите программу для вызова на сервере и получить способом (прокси-сервер), обратитесь к нему из клиента.</span><span class="sxs-lookup"><span data-stu-id="99501-120">Specify the program to be invoked on the server, and obtain a way (proxy) to refer to it from the client.</span></span>

- <span data-ttu-id="99501-121">Вызов программы сервера.</span><span class="sxs-lookup"><span data-stu-id="99501-121">Invoke the server program.</span></span> <span data-ttu-id="99501-122">Передайте параметры программы сервера, которое идентифицирует источник данных и команды для выдачи.</span><span class="sxs-lookup"><span data-stu-id="99501-122">Pass parameters to the server program that identifies the data source and the command to issue.</span></span>

- <span data-ttu-id="99501-123">Программы сервера получает объект [набора записей](recordset-object-ado.md) из источника данных, обычно с помощью ADO.</span><span class="sxs-lookup"><span data-stu-id="99501-123">The server program obtains a [Recordset](recordset-object-ado.md) object from the data source, typically by using ADO.</span></span> <span data-ttu-id="99501-124">Кроме того в объект **набора записей** обрабатывается на сервере.</span><span class="sxs-lookup"><span data-stu-id="99501-124">Optionally, the **Recordset** object is processed on the server.</span></span>

- <span data-ttu-id="99501-125">Программы сервера возвращает окончательный объекта **набора записей** для клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="99501-125">The server program returns the final **Recordset** object to the client application.</span></span>

- <span data-ttu-id="99501-126">В клиенте объекта **набора записей** при необходимости поместите в форму, можно легко использовать визуальные элементы управления.</span><span class="sxs-lookup"><span data-stu-id="99501-126">On the client, the **Recordset** object is optionally put into a form that can be easily used by visual controls.</span></span>

- <span data-ttu-id="99501-127">Изменения в объект **набора записей** отправляются на сервер и используется для обновления источника данных.</span><span class="sxs-lookup"><span data-stu-id="99501-127">Changes to the **Recordset** object are sent back to the server and used to update the data source.</span></span>

## <a name="step-1-specify-a-server-program"></a><span data-ttu-id="99501-128">Шаг 1: Укажите программу сервера</span><span class="sxs-lookup"><span data-stu-id="99501-128">Step 1: Specify a server program</span></span>

<span data-ttu-id="99501-129">В общем случае используйте [RDS. Пространства данных](dataspace-object-rds.md) объекта метод [CreateObject](createobject-method-rds.md) , чтобы указать программы сервера по умолчанию, [RDSServer.DataFactory](datafactory-object-rdsserver.md)или собственную программу настраиваемый серверный (бизнес-объект).</span><span class="sxs-lookup"><span data-stu-id="99501-129">In the most general case, use the [RDS.DataSpace](dataspace-object-rds.md) object [CreateObject](createobject-method-rds.md) method to specify the default server program, [RDSServer.DataFactory](datafactory-object-rdsserver.md), or your own custom server program (business object).</span></span> <span data-ttu-id="99501-130">Программа сервера создается на сервере и ссылку на программу сервера или *прокси-сервера*, возвращается.</span><span class="sxs-lookup"><span data-stu-id="99501-130">A server program is instantiated on the server, and a reference to the server program, or *proxy*, is returned.</span></span>

<span data-ttu-id="99501-131">В этом руководстве использует программы сервера по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="99501-131">This tutorial uses the default server program:</span></span>

```vb 
 
Sub RDSTutorial1() 
 Dim DS as New RDS.DataSpace 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
... 
``` 

## <a name="step-2-invoke-the-server-program"></a><span data-ttu-id="99501-132">Шаг 2: Вызовите программу сервера</span><span class="sxs-lookup"><span data-stu-id="99501-132">Step 2: Invoke the server program</span></span> 

<span data-ttu-id="99501-133">При вызове метода для клиента *прокси-сервера*, самой программы на сервере выполняется метод.</span><span class="sxs-lookup"><span data-stu-id="99501-133">When you invoke a method on the client *proxy*, the actual program on the server executes the method.</span></span> <span data-ttu-id="99501-134">На этом этапе будет выполнить запрос на сервере.</span><span class="sxs-lookup"><span data-stu-id="99501-134">In this step, you'll execute a query on the server.</span></span>

### <a name="part-a"></a><span data-ttu-id="99501-135">Часть "A"</span><span class="sxs-lookup"><span data-stu-id="99501-135">Part A</span></span>

<span data-ttu-id="99501-136">Если не были [RDSServer.DataFactory](datafactory-object-rdsserver.md) в этом руководстве, самый удобный способ выполните этот шаг будет использовать [RDS. DataControl](datacontrol-object-rds.md) объекта.</span><span class="sxs-lookup"><span data-stu-id="99501-136">If you weren't using [RDSServer.DataFactory](datafactory-object-rdsserver.md) in this tutorial, the most convenient way to perform this step would be to use the [RDS.DataControl](datacontrol-object-rds.md) object.</span></span> <span data-ttu-id="99501-137">**RDS. DataControl** объединяет предыдущие действия по созданию прокси-сервер, с помощью этот шаг, выполнение запроса.</span><span class="sxs-lookup"><span data-stu-id="99501-137">The **RDS.DataControl** combines the previous step of creating a proxy, with this step, issuing the query.</span></span>

1. <span data-ttu-id="99501-138">Установка **RDS. DataControl** объекта свойства [сервера](server-property-rds.md) для идентификации, где следует создать экземпляр программы сервера.</span><span class="sxs-lookup"><span data-stu-id="99501-138">Set the **RDS.DataControl** object [Server](server-property-rds.md) property to identify where the server program should be instantiated.</span></span>

2. <span data-ttu-id="99501-139">Присвойте свойству [подключение](connect-property-rds.md) для указания строки подключения для доступа к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="99501-139">Set the [Connect](connect-property-rds.md) property to specify the connect string to access the data source.</span></span>

3. <span data-ttu-id="99501-140">Присвойте свойству [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) для указания текст команды запроса.</span><span class="sxs-lookup"><span data-stu-id="99501-140">Set the [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) property to specify the query command text.</span></span> 

4. <span data-ttu-id="99501-141">Выдача метод [Refresh](refresh-method-rds.md) , чтобы программа server для подключения к источнику данных, извлечение строк, указанным в запросе и возврата объекта **набора записей** для клиента.</span><span class="sxs-lookup"><span data-stu-id="99501-141">Issue the [Refresh](refresh-method-rds.md) method to cause the server program to connect to the data source, retrieve rows specified by the query, and return a **Recordset** object to the client.</span></span>

<span data-ttu-id="99501-142">В этом руководстве не использует **RDS. DataControl**, но это, как она будет выглядеть при как:</span><span class="sxs-lookup"><span data-stu-id="99501-142">This tutorial does not use the **RDS.DataControl**, but this is how it would look if it did:</span></span>

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

<span data-ttu-id="99501-143">Ни учебника по вызов служб удаленных рабочих СТОЛОВ с объектами ADO, но это, как она будет выглядеть при как:</span><span class="sxs-lookup"><span data-stu-id="99501-143">Nor does the tutorial invoke RDS with ADO objects, but this is how it would look if it did:</span></span>

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "SELECT * FROM Authors","Provider=MS Remote;Data Source=Pubs;" & _ 
"Remote Server=https://yourServer;Remote Provider=SQLOLEDB;" 
```

### <a name="part-b"></a><span data-ttu-id="99501-144">Часть "B"</span><span class="sxs-lookup"><span data-stu-id="99501-144">Part B</span></span>

<span data-ttu-id="99501-145">Общий метод выполнения этого этапа — это для вызова метода [Query](query-method-rds.md) объекта **RDSServer.DataFactory** .</span><span class="sxs-lookup"><span data-stu-id="99501-145">The general method of performing this step is to invoke the **RDSServer.DataFactory** object [Query](query-method-rds.md) method.</span></span> <span data-ttu-id="99501-146">Этот метод принимает строку подключения, которая используется для подключения к источнику данных, и текст команды, который используется для указания строк, возвращаемых из источника данных.</span><span class="sxs-lookup"><span data-stu-id="99501-146">That method takes a connect string, which is used to connect to a data source, and a command text, which is used to specify the rows to be returned from the data source.</span></span>

<span data-ttu-id="99501-147">В этом руководстве использует объект **DataFactory** метод **запроса** :</span><span class="sxs-lookup"><span data-stu-id="99501-147">This tutorial uses the **DataFactory** object **Query** method:</span></span>

```vb 
 
Sub RDSTutorial2B() 
 Dim DS as New RDS.DataSpace 
 Dim DF 
 Dim RS as ADODB.Recordset 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
... 
```

## <a name="step-3-server-obtains-a-recordset"></a><span data-ttu-id="99501-148">Шаг 3. Сервер получает набор записей</span><span class="sxs-lookup"><span data-stu-id="99501-148">Step 3: Server obtains a Recordset</span></span> 

<span data-ttu-id="99501-149">Программа сервера использует текст строки и команду подключение для запроса источника данных для нужного строк.</span><span class="sxs-lookup"><span data-stu-id="99501-149">The server program uses the connect string and command text to query the data source for the desired rows.</span></span> <span data-ttu-id="99501-150">ADO обычно используется для получения этого **набора записей**, несмотря на то, что другие данные Microsoft доступ к интерфейсы, такие как OLE DB, можно было бы использовать.</span><span class="sxs-lookup"><span data-stu-id="99501-150">ADO is typically used to retrieve this **Recordset**, although other Microsoft data access interfaces, such as OLE DB, could be used.</span></span>

<span data-ttu-id="99501-151">Настраиваемый серверный программы может выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="99501-151">A custom server program might look like this:</span></span>

```vb 
 
Public Function ServerProgram(cn as String, qry as String) as Object 
Dim rs as New ADODB.Recordset 
 rs.CursorLocation = adUseClient 
 rs.Open qry, cn 
 rs.ActiveConnection = Nothing 
 Set ServerProgram = rs 
End Function 
```

## <a name="step-4-server-returns-the-recordset"></a><span data-ttu-id="99501-152">Шаг 4. Сервер возвращает набор записей</span><span class="sxs-lookup"><span data-stu-id="99501-152">Step 4: Server returns the Recordset</span></span> 

<span data-ttu-id="99501-153">Служб удаленных рабочих СТОЛОВ преобразует полученного объекта **набора записей** в форме, могут быть отправлены клиенту (то есть, оно *выполняет маршалинг* **набора записей**).</span><span class="sxs-lookup"><span data-stu-id="99501-153">RDS converts the retrieved **Recordset** object to a form that can be sent back to the client (that is, it *marshals* the **Recordset**).</span></span> <span data-ttu-id="99501-154">Точное преобразование и способ отправки зависит ли сервера в Интернете или интрасети, локальной сети, или является библиотекой динамической компоновки.</span><span class="sxs-lookup"><span data-stu-id="99501-154">The exact form of the conversion and how it is sent depends on whether the server is on the Internet or an intranet, a local area network, or is a dynamic-link library.</span></span> <span data-ttu-id="99501-155">Тем не менее в этом сведений не является обязательным; все, что имеет значение, служб удаленных рабочих СТОЛОВ отправляет **записей** клиенту.</span><span class="sxs-lookup"><span data-stu-id="99501-155">However, this detail is not critical; all that matters is that RDS sends the **Recordset** back to the client.</span></span>

<span data-ttu-id="99501-156">На стороне клиента объекта **набора записей** возвращается и присваивается локальной переменной.</span><span class="sxs-lookup"><span data-stu-id="99501-156">On the client side, a **Recordset** object is returned and assigned to a local variable.</span></span>

```vb 
 
Sub RDSTutorial4() 
 Dim DS as New RDS.DataSpace 
 Dim RS as ADODB.Recordset 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query("DSN=Pubs", "SELECT * FROM Authors") 
... 
```

## <a name="step-5-datacontrol-is-made-usable"></a><span data-ttu-id="99501-157">Шаг 5. Предоставление доступа к объекту DataControl</span><span class="sxs-lookup"><span data-stu-id="99501-157">Step 5: DataControl is made usable</span></span> 

<span data-ttu-id="99501-158">Возвращаемый объект **набора записей** доступна для использования.</span><span class="sxs-lookup"><span data-stu-id="99501-158">The returned **Recordset** object is available for use.</span></span> <span data-ttu-id="99501-159">Можно проверить, перейдите или измените его так, как и любой другой **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="99501-159">You can examine, navigate, or edit it as you would any other **Recordset**.</span></span> <span data-ttu-id="99501-160">Что можно сделать с помощью **набора записей** зависит от среды.</span><span class="sxs-lookup"><span data-stu-id="99501-160">What you can do with the **Recordset** depends on your environment.</span></span> <span data-ttu-id="99501-161">Visual Basic и Visual C++ имеют визуальные элементы управления, которые могут использовать **записей** прямо или косвенно с помощью Включение управления данными.</span><span class="sxs-lookup"><span data-stu-id="99501-161">Visual Basic and Visual C++ have visual controls that can use a **Recordset** directly or indirectly with the aid of an enabling data control.</span></span>

<span data-ttu-id="99501-162">Например при отображении веб-страницы в браузере Internet Explorer, может потребоваться отображение данных объекта **набора записей** в элементе управления visual.</span><span class="sxs-lookup"><span data-stu-id="99501-162">For example, if you are displaying a webpage in Internet Explorer, you might want to display the **Recordset** object data in a visual control.</span></span> <span data-ttu-id="99501-163">Визуальные элементы управления на веб-странице не может получить доступ к объекта **набора записей** напрямую.</span><span class="sxs-lookup"><span data-stu-id="99501-163">Visual controls on a webpage cannot access a **Recordset** object directly.</span></span> <span data-ttu-id="99501-164">Тем не менее они могут доступ к объекту **набора записей** с [RDS. DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="99501-164">However, they can access the **Recordset** object through the [RDS.DataControl](datacontrol-object-rds.md).</span></span> <span data-ttu-id="99501-165">**RDS. DataControl** становится могут использоваться с помощью визуального элемента управления, если свойство [SourceRecordset](recordset-sourcerecordset-properties-rds.md) имеет значение в объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="99501-165">The **RDS.DataControl** becomes usable by a visual control when its [SourceRecordset](recordset-sourcerecordset-properties-rds.md) property is set to the **Recordset** object.</span></span>

<span data-ttu-id="99501-166">Элемент управления visual объект должен иметь значение **RDS. параметра **DATASRC** DataControl**и его свойства **DATAFLD** поля объекта **набора записей** (столбца).</span><span class="sxs-lookup"><span data-stu-id="99501-166">The visual control object must have its **DATASRC** parameter set to the **RDS.DataControl**, and its **DATAFLD** property set to a **Recordset** object field (column).</span></span>

<span data-ttu-id="99501-167">В этом руководстве задайте для свойства **SourceRecordset** :</span><span class="sxs-lookup"><span data-stu-id="99501-167">In this tutorial, set the **SourceRecordset** property:</span></span>

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

## <a name="step-6-changes-are-sent-to-the-server"></a><span data-ttu-id="99501-168">Шаг 6. Отправка изменений на сервер</span><span class="sxs-lookup"><span data-stu-id="99501-168">Step 6: Changes are sent to the server</span></span>

<span data-ttu-id="99501-169">При редактировании объекта **набора записей** (строк, которые будут добавлены, изменены или удалены) изменения можно отправить на сервер.</span><span class="sxs-lookup"><span data-stu-id="99501-169">If the **Recordset** object is edited, any changes (that is, rows that are added, changed, or deleted) can be sent back to the server.</span></span>

<span data-ttu-id="99501-170">Поведение по умолчанию служб удаленных рабочих СТОЛОВ можно вызвать неявно с объекты ADO и поставщик удаленного взаимодействия Microsoft OLE DB.</span><span class="sxs-lookup"><span data-stu-id="99501-170">The default behavior of RDS can be invoked implicitly with ADO objects and the Microsoft OLE DB Remoting Provider.</span></span> <span data-ttu-id="99501-171">Запросы могут возвращать **наборов записей**и измененного **наборов записей** можно обновить источник данных.</span><span class="sxs-lookup"><span data-stu-id="99501-171">Queries can return **Recordsets**, and edited **Recordsets** can update the data source.</span></span> <span data-ttu-id="99501-172">В этом руководстве не вызывает служб удаленных рабочих СТОЛОВ с объектами ADO, но это, как она будет выглядеть при как:</span><span class="sxs-lookup"><span data-stu-id="99501-172">This tutorial does not invoke RDS with ADO objects, but this is how it would look if it did:</span></span>

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "SELECT * FROM Authors","Provider=MS Remote;Data Source=Pubs;" & _ 
 "Remote Server=https://yourServer;Remote Provider=SQLOLEDB;" 
... ' Edit the Recordset. 
rs.UpdateBatch ' The equivalent of SubmitChanges. 
... 
```

### <a name="part-a"></a><span data-ttu-id="99501-173">Часть "A"</span><span class="sxs-lookup"><span data-stu-id="99501-173">Part A</span></span>

<span data-ttu-id="99501-174">Предположим, в этом случае только использовали [RDS. DataControl](datacontrol-object-rds.md) , а теперь — объект **набора записей** , связанных с **RDS. DataControl**.</span><span class="sxs-lookup"><span data-stu-id="99501-174">Assume for this case that you have only used the [RDS.DataControl](datacontrol-object-rds.md) and that a **Recordset** object is now associated with the **RDS.DataControl**.</span></span> <span data-ttu-id="99501-175">Метод [SubmitChanges](submitchanges-method-rds.md) обновляет источник данных все изменения в объект **набора записей** Если свойства [сервера](server-property-rds.md) и [подключение](connect-property-rds.md) по-прежнему.</span><span class="sxs-lookup"><span data-stu-id="99501-175">The [SubmitChanges](submitchanges-method-rds.md) method updates the data source with any changes to the **Recordset** object if the [Server](server-property-rds.md) and [Connect](connect-property-rds.md) properties are still set.</span></span>

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

### <a name="part-b"></a><span data-ttu-id="99501-176">Часть "B"</span><span class="sxs-lookup"><span data-stu-id="99501-176">Part B</span></span>

<span data-ttu-id="99501-177">Кроме того может обновить сервер с объектом [RDSServer.DataFactory](datafactory-object-rdsserver.md) определения подключения и объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="99501-177">Alternatively, you could update the server with the [RDSServer.DataFactory](datafactory-object-rdsserver.md) object, specifying a connection and a **Recordset** object.</span></span>

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


## <a name="appendix-a-rds-tutorial-vbscript"></a><span data-ttu-id="99501-178">Приложение а учебника по служб удаленных рабочих СТОЛОВ (VBScript)</span><span class="sxs-lookup"><span data-stu-id="99501-178">Appendix A: RDS tutorial (VBScript)</span></span>

<span data-ttu-id="99501-179">Это учебник служб удаленных рабочих СТОЛОВ, написанных на языке Visual Basic Scripting Edition.</span><span class="sxs-lookup"><span data-stu-id="99501-179">This is the RDS tutorial, written in Microsoft Visual Basic Scripting Edition.</span></span> <span data-ttu-id="99501-180">Описание назначения в этом руководстве см в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="99501-180">For a description of the purpose of this tutorial, see the introduction to this topic.</span></span>

<span data-ttu-id="99501-181">В этом руководстве [RDS. DataControl](datacontrol-object-rds.md) и [RDS. Пространства данных](dataspace-object-rds.md) создан во время разработки; то есть они определены с помощью тегов объектов.</span><span class="sxs-lookup"><span data-stu-id="99501-181">In this tutorial, [RDS.DataControl](datacontrol-object-rds.md) and [RDS.DataSpace](dataspace-object-rds.md) are created at design time; that is, they are defined with object tags.</span></span> <span data-ttu-id="99501-182">Кроме того они может быть создан во время выполнения с помощью метода **Server.CreateObject** .</span><span class="sxs-lookup"><span data-stu-id="99501-182">Alternatively, they could be created at run time with the **Server.CreateObject** method.</span></span> 

<span data-ttu-id="99501-183">Например **RDS. DataControl** может быть создан следующим образом:</span><span class="sxs-lookup"><span data-stu-id="99501-183">For example, the **RDS.DataControl** object could be created like this:</span></span>

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

### <a name="step-1-specify-a-server-program"></a><span data-ttu-id="99501-184">Шаг 1: Укажите программу сервера</span><span class="sxs-lookup"><span data-stu-id="99501-184">Step 1: Specify a server program</span></span>

<span data-ttu-id="99501-185">VBScript можно получить имя веб-сервера IIS, его, на котором выполняется с помощью метода VBScript **Request.ServerVariables** для страницы ASP:</span><span class="sxs-lookup"><span data-stu-id="99501-185">VBScript can discover the name of the IIS web server it is running on by accessing the VBScript **Request.ServerVariables** method available to Active Server Pages:</span></span>

```vb 
 
"https://<%=Request.ServerVariables("SERVER_NAME")%>" 
```

<span data-ttu-id="99501-186">Тем не менее в этом руководстве используйте мнимой server «сервер».</span><span class="sxs-lookup"><span data-stu-id="99501-186">However, for this tutorial, use the imaginary server, "yourServer."</span></span>

> [!NOTE]
> <span data-ttu-id="99501-187">Обратите внимание на тип данных **ByRef** аргументов.</span><span class="sxs-lookup"><span data-stu-id="99501-187">Pay attention to the data type of **ByRef** arguments.</span></span> <span data-ttu-id="99501-188">VBScript не позволяет указать тип переменной, поэтому всегда необходимо передать переменную типа Variant.</span><span class="sxs-lookup"><span data-stu-id="99501-188">VBScript does not let you specify the variable type, so you must always pass a Variant.</span></span> <span data-ttu-id="99501-189">При использовании HTTP, служб удаленных рабочих СТОЛОВ можно передать переменную типа Variant в метод, требующей не тип Variant, если вызвать его с **RDS. Пространства данных** объекта метод [CreateObject](createobject-method-rds.md) .</span><span class="sxs-lookup"><span data-stu-id="99501-189">When using HTTP, RDS will allow you to pass a Variant to a method that expects a non-Variant if you invoke it with the **RDS.DataSpace** object [CreateObject](createobject-method-rds.md) method.</span></span> <span data-ttu-id="99501-190">При использовании DCOM или на сервере в процессе, соответствующие типы параметров на сторонах клиента и сервера или появится сообщение об ошибке «Несоответствие типов».</span><span class="sxs-lookup"><span data-stu-id="99501-190">When using DCOM or an in-process server, match the parameter types on the client and server sides or you will receive a "Type Mismatch" error.</span></span>

```vb
 
Set DF1 = DS1.CreateObject("RDSServer.DataFactory", "https://yourServer") 
```

### <a name="step-2-part-a-invoke-the-server-program-with-rdsdatacontrol"></a><span data-ttu-id="99501-191">Шаг 2, вызов ответ: часть программы сервера с RDS. DataControl</span><span class="sxs-lookup"><span data-stu-id="99501-191">Step 2, Part A: Invoke the server program with RDS.DataControl</span></span>

<span data-ttu-id="99501-192">В этом примере — это просто комментарий, демонстрации поведения по умолчанию **RDS. DataControl** для выполнения указанного запроса.</span><span class="sxs-lookup"><span data-stu-id="99501-192">This example is merely a comment demonstrating that the default behavior of the **RDS.DataControl** is to perform the specified query.</span></span>

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

<span data-ttu-id="99501-193">Перейдите к следующему шагу.</span><span class="sxs-lookup"><span data-stu-id="99501-193">Skip to the following step.</span></span>

### <a name="step-4-server-returns-the-recordset"></a><span data-ttu-id="99501-194">Шаг 4. Сервер возвращает набор записей</span><span class="sxs-lookup"><span data-stu-id="99501-194">Step 4: Server returns the Recordset</span></span>

```vb
 
Set RS = DF1.Query("DSN=Pubs;", "SELECT * FROM Authors") 
```

### <a name="step-5-datacontrol-is-made-usable-by-visual-controls"></a><span data-ttu-id="99501-195">Шаг 5: DataControl осуществляется могут использоваться элементы управления visual</span><span class="sxs-lookup"><span data-stu-id="99501-195">Step 5: DataControl is made usable by visual controls</span></span>

```vb
 
' Assign the returned recordset to the DataControl. 
 
DC1.SourceRecordset = RS 
```

### <a name="step-6-part-a-changes-are-sent-to-the-server-with-rdsdatacontrol"></a><span data-ttu-id="99501-196">Шаг 6, часть A: изменения отправляются на сервер с RDS. DataControl</span><span class="sxs-lookup"><span data-stu-id="99501-196">Step 6, Part A: Changes are sent to the server with RDS.DataControl</span></span>

<span data-ttu-id="99501-197">В этом примере — это просто комментарий демонстрируется, как **RDS. DataControl** выполняет обновление.</span><span class="sxs-lookup"><span data-stu-id="99501-197">This example is merely a comment demonstrating how the **RDS.DataControl** performs updates.</span></span>

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

### <a name="step-6-part-b-changes-are-sent-to-the-server-with-rdsserverdatafactory"></a><span data-ttu-id="99501-198">Шаг 6, часть B: изменения отправляются на сервер с RDSServer.DataFactory</span><span class="sxs-lookup"><span data-stu-id="99501-198">Step 6, Part B: Changes are sent to the server with RDSServer.DataFactory</span></span>

```vb
 
DF.SubmitChanges"DSN=Pubs", RS 
 
End Sub 
</SCRIPT> 
</BODY> 
</HTML> 
```

## <a name="appendix-b-rds-tutorial-visual-j"></a><span data-ttu-id="99501-199">Приложение б. служб удаленных рабочих СТОЛОВ при помощи учебника по (Visual J ++)</span><span class="sxs-lookup"><span data-stu-id="99501-199">Appendix B: RDS tutorial (Visual J++)</span></span>

<span data-ttu-id="99501-200">ADO/WFC не соответствующего полностью объектной модели служб удаленных рабочих СТОЛОВ, то есть не реализует [RDS. DataControl](datacontrol-object-rds.md) объекта.</span><span class="sxs-lookup"><span data-stu-id="99501-200">ADO/WFC does not completely follow the RDS object model in that it does not implement the [RDS.DataControl](datacontrol-object-rds.md) object.</span></span> <span data-ttu-id="99501-201">ADO/WFC только реализует класс со стороны клиента, [RDS. Пространства данных](dataspace-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="99501-201">ADO/WFC only implements the client-side class, [RDS.DataSpace](dataspace-object-rds.md).</span></span>

<span data-ttu-id="99501-202">Класс **пространства данных** реализует один метод [CreateObject](createobject-method-rds.md), которое возвращает объект [ObjectProxy](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/objectproxy-ado-wfc-syntax) .</span><span class="sxs-lookup"><span data-stu-id="99501-202">The **DataSpace** class implements one method, [CreateObject](createobject-method-rds.md), which returns an [ObjectProxy](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/objectproxy-ado-wfc-syntax) object.</span></span> <span data-ttu-id="99501-203">Класс **пространства данных** также внедряет свойство [InternetTimeout](internettimeout-property-rds.md) .</span><span class="sxs-lookup"><span data-stu-id="99501-203">The **DataSpace** class also implements the [InternetTimeout](internettimeout-property-rds.md) property.</span></span>

<span data-ttu-id="99501-204">Класс **ObjectProxy** реализует один метод, позвонить, которой можно было вызвать любой объект бизнеса на сервере.</span><span class="sxs-lookup"><span data-stu-id="99501-204">The **ObjectProxy** class implements one method, call, which can invoke any server-side business object.</span></span>

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



