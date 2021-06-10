---
title: Сценарий сохранения набора записей XML
TOCTitle: XML Recordset persistence scenario
ms:assetid: 08f464da-10ba-b649-7571-766a40da2e04
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248825(v=office.15)
ms:contentKeyID: 48543107
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5bae48f3e9b2b5c3967b955c41ba01c634546164
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302598"
---
# <a name="xml-recordset-persistence-scenario"></a><span data-ttu-id="b5dc5-102">Сценарий сохранения набора записей XML</span><span class="sxs-lookup"><span data-stu-id="b5dc5-102">XML Recordset persistence scenario</span></span>

<span data-ttu-id="b5dc5-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b5dc5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b5dc5-104">В этом сценарии будет создаваться приложение ASP (ASP), которое сохраняет содержимое объекта **Recordset** непосредственно к объекту asP **Response.**</span><span class="sxs-lookup"><span data-stu-id="b5dc5-104">In this scenario, you will create an Active Server Pages (ASP) application that saves the contents of a **Recordset** object directly to the ASP **Response** object.</span></span>

> [!NOTE]
> <span data-ttu-id="b5dc5-105">Этот сценарий требует, чтобы на вашем сервере был установлен сервер информации в Интернете 5.0 (IIS) или позднее.</span><span class="sxs-lookup"><span data-stu-id="b5dc5-105">This scenario requires that your server have Internet Information Server 5.0 (IIS) or later installed.</span></span>

<span data-ttu-id="b5dc5-106">Возвращенный **набор записей** отображается в Internet Explorer с помощью [RDS. DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="b5dc5-106">The returned **Recordset** is displayed in Internet Explorer using an [RDS.DataControl](datacontrol-object-rds.md).</span></span>

<span data-ttu-id="b5dc5-107">Для создания этого сценария необходимы следующие действия:</span><span class="sxs-lookup"><span data-stu-id="b5dc5-107">The following steps are necessary to create this scenario:</span></span>

1.  <span data-ttu-id="b5dc5-108">Настройка приложения.</span><span class="sxs-lookup"><span data-stu-id="b5dc5-108">Set up the application.</span></span>
2.  <span data-ttu-id="b5dc5-109">Получите данные.</span><span class="sxs-lookup"><span data-stu-id="b5dc5-109">Get the data.</span></span>
3.  <span data-ttu-id="b5dc5-110">Отправка данных.</span><span class="sxs-lookup"><span data-stu-id="b5dc5-110">Send the data.</span></span>
4.  <span data-ttu-id="b5dc5-111">Получение и отображение данных.</span><span class="sxs-lookup"><span data-stu-id="b5dc5-111">Receive and display the data.</span></span>

## <a name="step-1-set-up-the-application"></a><span data-ttu-id="b5dc5-112">Шаг 1. Настройка приложения</span><span class="sxs-lookup"><span data-stu-id="b5dc5-112">Step 1: Set up the application</span></span>

1. <span data-ttu-id="b5dc5-113">Создайте виртуальный каталог IIS с именем **XMLPersist с** разрешениями скрипта.</span><span class="sxs-lookup"><span data-stu-id="b5dc5-113">Create an IIS virtual directory named **XMLPersist** with script permissions.</span></span> 

2. <span data-ttu-id="b5dc5-114">Создайте два новых текстовых файла в папке, в которую указывает виртуальный каталог, один с именем **XMLResponse.asp** и другой с именем **Default.htm**.</span><span class="sxs-lookup"><span data-stu-id="b5dc5-114">Create two new text files in the folder to which the virtual directory points, one named **XMLResponse.asp**, and the other named **Default.htm**.</span></span>


## <a name="step-2-get-the-data"></a><span data-ttu-id="b5dc5-115">Шаг 2. Получить данные</span><span class="sxs-lookup"><span data-stu-id="b5dc5-115">Step 2: Get the data</span></span>

<span data-ttu-id="b5dc5-116">На этом этапе вы напишете код, чтобы открыть ADO **Recordset** и подготовиться к отправке его клиенту.</span><span class="sxs-lookup"><span data-stu-id="b5dc5-116">In this step, you will write the code to open an ADO **Recordset** and prepare to send it to the client.</span></span> 

1. <span data-ttu-id="b5dc5-117">Откройте файл XMLResponse.asp с помощью текстового редактора, например Windows Блокнот, и вставьте следующий код:</span><span class="sxs-lookup"><span data-stu-id="b5dc5-117">Open the file XMLResponse.asp with a text editor, such as Windows Notepad, and insert the following code:</span></span>

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

2. <span data-ttu-id="b5dc5-118">Обязательно измените значение параметра Источник данных в strCon на имя Microsoft SQL Server компьютера.</span><span class="sxs-lookup"><span data-stu-id="b5dc5-118">Be sure to change the value of the Data Source parameter in strCon to the name of your Microsoft SQL Server computer.</span></span>

3. <span data-ttu-id="b5dc5-119">Держите файл открытым и перейдите к следующему шагу.</span><span class="sxs-lookup"><span data-stu-id="b5dc5-119">Keep the file open and go on to the next step.</span></span>

## <a name="step-3-send-the-data"></a><span data-ttu-id="b5dc5-120">Шаг 3. Отправка данных</span><span class="sxs-lookup"><span data-stu-id="b5dc5-120">Step 3: Send the data</span></span>

<span data-ttu-id="b5dc5-121">Теперь, когда у вас есть **Набор записей,** необходимо отправить его клиенту, сэкономив его в качестве XML для объекта asP **Response.**</span><span class="sxs-lookup"><span data-stu-id="b5dc5-121">Now that you have a **Recordset**, you need to send it to the client by saving it as XML to the ASP **Response** object.</span></span> 

1. <span data-ttu-id="b5dc5-122">Добавьте следующий код в нижней части XMLResponse.asp:</span><span class="sxs-lookup"><span data-stu-id="b5dc5-122">Add the following code to the bottom of XMLResponse.asp:</span></span>

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

   <span data-ttu-id="b5dc5-123">Обратите внимание, что объект asP **Response** указывается в качестве назначения для метода **Сохранить** [набор](save-method-ado.md) записей.</span><span class="sxs-lookup"><span data-stu-id="b5dc5-123">Notice that the ASP **Response** object is specified as the destination for the **Recordset** [Save](save-method-ado.md) method.</span></span> <span data-ttu-id="b5dc5-124">Предназначением метода **Сохранить** может быть любой объект, поддерживаюходящий интерфейс **IStream,** например объект ADO [Stream,](stream-object-ado.md) или имя файла, которое включает полный путь, к которому должен быть сохранен **набор** записей.</span><span class="sxs-lookup"><span data-stu-id="b5dc5-124">The destination of the **Save** method can be any object that supports the **IStream** interface, such as an ADO [Stream](stream-object-ado.md) object, or a file name that includes the complete path to which the **Recordset** is to be saved.</span></span>

2. <span data-ttu-id="b5dc5-125">Сохраните и закрой XMLResponse.asp перед следующим шагом.</span><span class="sxs-lookup"><span data-stu-id="b5dc5-125">Save and close XMLResponse.asp before going to the next step.</span></span> <span data-ttu-id="b5dc5-126">Кроме того, скопируйте файл adovbs.inc из папки C: Program Files Common Files System Ado в ту же папку, где у вас есть \\ \\ файл \\ \\ XMLResponse.asp.</span><span class="sxs-lookup"><span data-stu-id="b5dc5-126">Also copy the adovbs.inc file from C:\\Program Files\\Common Files\\System\\Ado folder to the same folder where you have the XMLResponse.asp file.</span></span>

## <a name="step-4-receive-and-display-the-data"></a><span data-ttu-id="b5dc5-127">Шаг 4. Получение и отображение данных</span><span class="sxs-lookup"><span data-stu-id="b5dc5-127">Step 4: Receive and display the data</span></span>

<span data-ttu-id="b5dc5-128">На этом этапе будет создаваться HTML-файл со встроенным [RDS. Объект DataControl,](datacontrol-object-rds.md) который указывает на файл XMLResponse.asp, чтобы получить **набор записей.**</span><span class="sxs-lookup"><span data-stu-id="b5dc5-128">In this step, you will create an HTML file with an embedded [RDS.DataControl](datacontrol-object-rds.md) object that points at the XMLResponse.asp file to get the **Recordset**.</span></span> 

1. <span data-ttu-id="b5dc5-129">Откройте default.htm с текстовым редактором, например Windows Блокнот, и добавьте следующий код.</span><span class="sxs-lookup"><span data-stu-id="b5dc5-129">Open default.htm with a text editor, such as Windows Notepad, and add the following code.</span></span> <span data-ttu-id="b5dc5-130">Замените "sqlserver" в URL-адресе именем сервера.</span><span class="sxs-lookup"><span data-stu-id="b5dc5-130">Replace "sqlserver" in the URL with the name of your server computer.</span></span>

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

2. <span data-ttu-id="b5dc5-131">Закрой default.htm файл и сохраните его в той же папке, в которой сохранен XMLResponse.asp.</span><span class="sxs-lookup"><span data-stu-id="b5dc5-131">Close the default.htm file and save it to the same folder where you saved XMLResponse.asp.</span></span> 

3. <span data-ttu-id="b5dc5-132">С помощью Internet Explorer 4.0 или более поздней версии откройте URL-адрес `https://<sqlserver>/XMLPersist/default.htm` и понаблюдать за результатами.</span><span class="sxs-lookup"><span data-stu-id="b5dc5-132">Using Internet Explorer 4.0 or later, open the URL `https://<sqlserver>/XMLPersist/default.htm` and observe the results.</span></span> <span data-ttu-id="b5dc5-133">Данные отображаются в связанной таблице DHTML.</span><span class="sxs-lookup"><span data-stu-id="b5dc5-133">The data is displayed in a bound DHTML table.</span></span> 

4. <span data-ttu-id="b5dc5-134">Теперь откройте URL-адрес `https://<sqlserver>/XMLPersist/XMLResponse.asp` и понаблюдать за результатами.</span><span class="sxs-lookup"><span data-stu-id="b5dc5-134">Now open the URL `https://<sqlserver>/XMLPersist/XMLResponse.asp` and observe the results.</span></span> <span data-ttu-id="b5dc5-135">Отображается XML.</span><span class="sxs-lookup"><span data-stu-id="b5dc5-135">The XML is displayed.</span></span>




