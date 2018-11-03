---
title: Сценарий хранение записей XML
TOCTitle: XML Recordset persistence scenario
ms:assetid: 08f464da-10ba-b649-7571-766a40da2e04
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248825(v=office.15)
ms:contentKeyID: 48543107
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4840b59f8f145b17b45a9732443d3f844b336868
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945490"
---
# <a name="xml-recordset-persistence-scenario"></a><span data-ttu-id="88216-102">Сценарий хранение записей XML</span><span class="sxs-lookup"><span data-stu-id="88216-102">XML Recordset persistence scenario</span></span>

<span data-ttu-id="88216-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="88216-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="88216-104">В данном сценарии создается приложение Active Server Pages (ASP), сохранение содержимого объекта **набора записей** непосредственно к объекту ASP **ответа** .</span><span class="sxs-lookup"><span data-stu-id="88216-104">In this scenario, you will create an Active Server Pages (ASP) application that saves the contents of a **Recordset** object directly to the ASP **Response** object.</span></span>

> [!NOTE]
> <span data-ttu-id="88216-105">В этом случае необходимо, что сервер Internet Information Server 5.0 (IIS) или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="88216-105">This scenario requires that your server have Internet Information Server 5.0 (IIS) or later installed.</span></span>

<span data-ttu-id="88216-106">Возвращенный **набор записей** отображается в браузере Internet Explorer с помощью [RDS. DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="88216-106">The returned **Recordset** is displayed in Internet Explorer using an [RDS.DataControl](datacontrol-object-rds.md).</span></span>

<span data-ttu-id="88216-107">Для создания этого сценария необходимы следующие действия:</span><span class="sxs-lookup"><span data-stu-id="88216-107">The following steps are necessary to create this scenario:</span></span>

1.  <span data-ttu-id="88216-108">Настройка приложения.</span><span class="sxs-lookup"><span data-stu-id="88216-108">Set up the application.</span></span>
2.  <span data-ttu-id="88216-109">Получение данных.</span><span class="sxs-lookup"><span data-stu-id="88216-109">Get the data.</span></span>
3.  <span data-ttu-id="88216-110">Отправка данных.</span><span class="sxs-lookup"><span data-stu-id="88216-110">Send the data.</span></span>
4.  <span data-ttu-id="88216-111">Получение и отображения данных.</span><span class="sxs-lookup"><span data-stu-id="88216-111">Receive and display the data.</span></span>

## <a name="step-1-set-up-the-application"></a><span data-ttu-id="88216-112">Этап 1: Настройка приложения</span><span class="sxs-lookup"><span data-stu-id="88216-112">Step 1: Set up the application</span></span>

1. <span data-ttu-id="88216-113">Создайте виртуальный каталог IIS, с именем **XMLPersist** с разрешениями скрипта.</span><span class="sxs-lookup"><span data-stu-id="88216-113">Create an IIS virtual directory named **XMLPersist** with script permissions.</span></span> 

2. <span data-ttu-id="88216-114">Создайте две новые текстовые файлы в папку, на который указывает виртуальный каталог, один именованный **XMLResponse.asp**и другое с именем **Default.htm**.</span><span class="sxs-lookup"><span data-stu-id="88216-114">Create two new text files in the folder to which the virtual directory points, one named **XMLResponse.asp**, and the other named **Default.htm**.</span></span>


## <a name="step-2-get-the-data"></a><span data-ttu-id="88216-115">Шаг 2: Получение данных</span><span class="sxs-lookup"><span data-stu-id="88216-115">Step 2: Get the data</span></span>

<span data-ttu-id="88216-116">На этом этапе будет написание кода для открытия набора **записей** ADO и подготовка для отправки клиенту.</span><span class="sxs-lookup"><span data-stu-id="88216-116">In this step, you will write the code to open an ADO **Recordset** and prepare to send it to the client.</span></span> 

1. <span data-ttu-id="88216-117">Откройте файл XMLResponse.asp в текстовом редакторе, например в Блокноте и вставьте следующий код:</span><span class="sxs-lookup"><span data-stu-id="88216-117">Open the file XMLResponse.asp with a text editor, such as Windows Notepad, and insert the following code:</span></span>

   ```vb 
        
        <%@ language="VBScript" %> 
        
        <!-- #include file='adovbs.inc' --> 
        
        <% 
        Dim strSQL, strCon 
        Dim adoRec  
        Dim adoCon  
        Dim xmlDoc  
        
        ' You will need to change "slqServer" below to the name of the SQL  
        ' server machine to which you want to connect. 
        strCon = "Provider=sqloledb;Data Source=sqlServer;Initial Catalog=Pubs;Integrated Security=SSPI;" 
        Set adoCon = server.createObject("ADODB.Connection") 
        adoCon.Open strCon 
        
        strSQL = "SELECT Title, Price FROM Titles ORDER BY Price" 
        Set adoRec = Server.CreateObject("ADODB.Recordset") 
        adoRec.Open strSQL, adoCon, adOpenStatic, adLockOptimistic, adCmdText 
   ```

2. <span data-ttu-id="88216-118">Не забудьте изменить значение параметра источника данных в strCon к имени компьютера Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="88216-118">Be sure to change the value of the Data Source parameter in strCon to the name of your Microsoft SQL Server computer.</span></span>

3. <span data-ttu-id="88216-119">Сохранение файла перейдите к следующему шагу.</span><span class="sxs-lookup"><span data-stu-id="88216-119">Keep the file open and go on to the next step.</span></span>

## <a name="step-3-send-the-data"></a><span data-ttu-id="88216-120">Шаг 3: Отправка данных</span><span class="sxs-lookup"><span data-stu-id="88216-120">Step 3: Send the data</span></span>

<span data-ttu-id="88216-121">Теперь, когда у вас есть **набор записей**, необходимо отправить его клиенту путем сохранения в формате XML объект ASP **ответа** .</span><span class="sxs-lookup"><span data-stu-id="88216-121">Now that you have a **Recordset**, you need to send it to the client by saving it as XML to the ASP **Response** object.</span></span> 

1. <span data-ttu-id="88216-122">Добавьте следующий код в конец XMLResponse.asp:</span><span class="sxs-lookup"><span data-stu-id="88216-122">Add the following code to the bottom of XMLResponse.asp:</span></span>

   ```vb 
    
    Response.ContentType = "text/xml" 
    Response.Expires = 0 
    Response.Buffer = False 
    
    
    Response.Write "<?xml version='1.0'?>" & vbNewLine 
    adoRec.save Response, adPersistXML 
    adoRec.Close 
    Set adoRec=Nothing 
    %> 
   ```

   <span data-ttu-id="88216-123">Обратите внимание на то, что объект ASP **ответа** указан как назначения для метода **записей** [Сохранить](save-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="88216-123">Notice that the ASP **Response** object is specified as the destination for the **Recordset** [Save](save-method-ado.md) method.</span></span> <span data-ttu-id="88216-124">Конечный метод **Save** может быть любой объект, который поддерживает интерфейс **IStream** , например, объект ADO [потока](stream-object-ado.md) или имя файла, который включает в себя полный путь к которой должен быть сохранен **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="88216-124">The destination of the **Save** method can be any object that supports the **IStream** interface, such as an ADO [Stream](stream-object-ado.md) object, or a file name that includes the complete path to which the **Recordset** is to be saved.</span></span>

2. <span data-ttu-id="88216-125">Сохраните и закройте XMLResponse.asp перед переходом к следующему шагу.</span><span class="sxs-lookup"><span data-stu-id="88216-125">Save and close XMLResponse.asp before going to the next step.</span></span> <span data-ttu-id="88216-126">Также скопируйте файл adovbs.inc из C:\\Program Files\\общие файлы\\системы\\Ado папки в ту же папку, где у вас есть файл XMLResponse.asp.</span><span class="sxs-lookup"><span data-stu-id="88216-126">Also copy the adovbs.inc file from C:\\Program Files\\Common Files\\System\\Ado folder to the same folder where you have the XMLResponse.asp file.</span></span>

## <a name="step-4-receive-and-display-the-data"></a><span data-ttu-id="88216-127">Шаг 4: Получение и отображения данных</span><span class="sxs-lookup"><span data-stu-id="88216-127">Step 4: Receive and display the data</span></span>

<span data-ttu-id="88216-128">На этом этапе создается HTML-файла с внедренным [RDS. DataControl](datacontrol-object-rds.md) объект, указывающий на файл XMLResponse.asp для получения **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="88216-128">In this step, you will create an HTML file with an embedded [RDS.DataControl](datacontrol-object-rds.md) object that points at the XMLResponse.asp file to get the **Recordset**.</span></span> 

1. <span data-ttu-id="88216-129">Откройте файл default.htm в текстовом редакторе, например в Блокноте и добавьте следующий код.</span><span class="sxs-lookup"><span data-stu-id="88216-129">Open default.htm with a text editor, such as Windows Notepad, and add the following code.</span></span> <span data-ttu-id="88216-130">Замените «sqlserver» в URL-имя компьютера сервера.</span><span class="sxs-lookup"><span data-stu-id="88216-130">Replace "sqlserver" in the URL with the name of your server computer.</span></span>

   ```html 
    
    <HTML> 
    <HEAD><TITLE>ADO Recordset Persistence Sample</TITLE></HEAD> 
    <BODY> 
    
    <TABLE DATASRC="#RDC1" border="1"> 
    <TR> 
    <TD><SPAN DATAFLD="title"></SPAN></TD> 
    <TD><SPAN DATAFLD="price"></SPAN></TD> 
    </TR> 
    </TABLE> 

    <OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="RDC1"> 
    <PARAM NAME="URL" VALUE="XMLResponse.asp"> 
    </OBJECT> 
    
    </BODY> 
    </HTML> 
   ```

2. <span data-ttu-id="88216-131">Закройте файл default.htm и сохраните его в ту же папку, где был сохранен XMLResponse.asp.</span><span class="sxs-lookup"><span data-stu-id="88216-131">Close the default.htm file and save it to the same folder where you saved XMLResponse.asp.</span></span> 

3. <span data-ttu-id="88216-132">Internet Explorer версии 4.0 или более поздних версий, откройте URL-адрес `https://<sqlserver>/XMLPersist/default.htm` и просмотрите результаты.</span><span class="sxs-lookup"><span data-stu-id="88216-132">Using Internet Explorer 4.0 or later, open the URL `https://<sqlserver>/XMLPersist/default.htm` and observe the results.</span></span> <span data-ttu-id="88216-133">Данные отображаются в связанной таблице DHTML.</span><span class="sxs-lookup"><span data-stu-id="88216-133">The data is displayed in a bound DHTML table.</span></span> 

4. <span data-ttu-id="88216-134">Теперь откройте URL-адрес `https://<sqlserver>/XMLPersist/XMLResponse.asp` и просмотрите результаты.</span><span class="sxs-lookup"><span data-stu-id="88216-134">Now open the URL `https://<sqlserver>/XMLPersist/XMLResponse.asp` and observe the results.</span></span> <span data-ttu-id="88216-135">XML-код отображается.</span><span class="sxs-lookup"><span data-stu-id="88216-135">The XML is displayed.</span></span>




