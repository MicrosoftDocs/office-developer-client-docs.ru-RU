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
# <a name="xml-recordset-persistence-scenario"></a><span data-ttu-id="5a2ed-102">Сценарий сохранения набора записей XML</span><span class="sxs-lookup"><span data-stu-id="5a2ed-102">XML Recordset persistence scenario</span></span>

<span data-ttu-id="5a2ed-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5a2ed-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5a2ed-104">В этом сценарии создается приложение страниц Active Server (ASP), которое сохраняет содержимое объекта **Recordset** непосредственно в **ответном** объекте ASP.</span><span class="sxs-lookup"><span data-stu-id="5a2ed-104">In this scenario, you will create an Active Server Pages (ASP) application that saves the contents of a **Recordset** object directly to the ASP **Response** object.</span></span>

> [!NOTE]
> <span data-ttu-id="5a2ed-105">Для этого сценария необходимо, чтобы на сервере был установлен сервер IIS 5,0 (IIS) или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="5a2ed-105">This scenario requires that your server have Internet Information Server 5.0 (IIS) or later installed.</span></span>

<span data-ttu-id="5a2ed-106">Возвращенный **набор записей** отображается в Internet Explorer с помощью [RDS. Элемент управления](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="5a2ed-106">The returned **Recordset** is displayed in Internet Explorer using an [RDS.DataControl](datacontrol-object-rds.md).</span></span>

<span data-ttu-id="5a2ed-107">Для создания этого сценария необходимо выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="5a2ed-107">The following steps are necessary to create this scenario:</span></span>

1.  <span data-ttu-id="5a2ed-108">Настройка приложения.</span><span class="sxs-lookup"><span data-stu-id="5a2ed-108">Set up the application.</span></span>
2.  <span data-ttu-id="5a2ed-109">Получение данных.</span><span class="sxs-lookup"><span data-stu-id="5a2ed-109">Get the data.</span></span>
3.  <span data-ttu-id="5a2ed-110">Отправьте данные.</span><span class="sxs-lookup"><span data-stu-id="5a2ed-110">Send the data.</span></span>
4.  <span data-ttu-id="5a2ed-111">Получение и отображение данных.</span><span class="sxs-lookup"><span data-stu-id="5a2ed-111">Receive and display the data.</span></span>

## <a name="step-1-set-up-the-application"></a><span data-ttu-id="5a2ed-112">Шаг 1: Настройка приложения</span><span class="sxs-lookup"><span data-stu-id="5a2ed-112">Step 1: Set up the application</span></span>

1. <span data-ttu-id="5a2ed-113">Создайте виртуальный каталог IIS с именем **ксмлперсист** с разрешениями для скриптов.</span><span class="sxs-lookup"><span data-stu-id="5a2ed-113">Create an IIS virtual directory named **XMLPersist** with script permissions.</span></span> 

2. <span data-ttu-id="5a2ed-114">Создайте два новых текстовых файла в папке, в которой указываются виртуальные каталоги, один с именем **ксмлреспонсе. ASP**и другой с именем **Default. htm**.</span><span class="sxs-lookup"><span data-stu-id="5a2ed-114">Create two new text files in the folder to which the virtual directory points, one named **XMLResponse.asp**, and the other named **Default.htm**.</span></span>


## <a name="step-2-get-the-data"></a><span data-ttu-id="5a2ed-115">Шаг 2: получение данных</span><span class="sxs-lookup"><span data-stu-id="5a2ed-115">Step 2: Get the data</span></span>

<span data-ttu-id="5a2ed-116">На этом этапе будет написан код для открытия **набора записей** ADO и подготовки к его отправке клиенту.</span><span class="sxs-lookup"><span data-stu-id="5a2ed-116">In this step, you will write the code to open an ADO **Recordset** and prepare to send it to the client.</span></span> 

1. <span data-ttu-id="5a2ed-117">Откройте файл Ксмлреспонсе. ASP в текстовом редакторе, например в блокноте Windows, и вставьте следующий код:</span><span class="sxs-lookup"><span data-stu-id="5a2ed-117">Open the file XMLResponse.asp with a text editor, such as Windows Notepad, and insert the following code:</span></span>

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

2. <span data-ttu-id="5a2ed-118">Не забудьте изменить значение параметра источника данных в Стркон на имя компьютера Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5a2ed-118">Be sure to change the value of the Data Source parameter in strCon to the name of your Microsoft SQL Server computer.</span></span>

3. <span data-ttu-id="5a2ed-119">Оставьте файл открытым и перейдите к следующему шагу.</span><span class="sxs-lookup"><span data-stu-id="5a2ed-119">Keep the file open and go on to the next step.</span></span>

## <a name="step-3-send-the-data"></a><span data-ttu-id="5a2ed-120">Шаг 3: отправка данных</span><span class="sxs-lookup"><span data-stu-id="5a2ed-120">Step 3: Send the data</span></span>

<span data-ttu-id="5a2ed-121">Теперь, когда у вас есть объект **Recordset**, его необходимо отправить клиенту, сохранив его в виде XML-файла в **ответный** объект ASP.</span><span class="sxs-lookup"><span data-stu-id="5a2ed-121">Now that you have a **Recordset**, you need to send it to the client by saving it as XML to the ASP **Response** object.</span></span> 

1. <span data-ttu-id="5a2ed-122">Добавьте следующий код в нижнюю часть Ксмлреспонсе. ASP:</span><span class="sxs-lookup"><span data-stu-id="5a2ed-122">Add the following code to the bottom of XMLResponse.asp:</span></span>

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

   <span data-ttu-id="5a2ed-123">Обратите внимание, что объект **ответа** ASP указывается в качестве назначения для метода [Save](save-method-ado.md) **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="5a2ed-123">Notice that the ASP **Response** object is specified as the destination for the **Recordset** [Save](save-method-ado.md) method.</span></span> <span data-ttu-id="5a2ed-124">В качестве места назначения метода **Save** может быть любой объект, поддерживающий интерфейс **IStream** , например объект [Stream](stream-object-ado.md) объекта ADO, или имя файла, включающее полный путь, по которому необходимо сохранить **набор записей** .</span><span class="sxs-lookup"><span data-stu-id="5a2ed-124">The destination of the **Save** method can be any object that supports the **IStream** interface, such as an ADO [Stream](stream-object-ado.md) object, or a file name that includes the complete path to which the **Recordset** is to be saved.</span></span>

2. <span data-ttu-id="5a2ed-125">Сохраните и закройте Ксмлреспонсе. ASP, прежде чем переходить к следующему шагу.</span><span class="sxs-lookup"><span data-stu-id="5a2ed-125">Save and close XMLResponse.asp before going to the next step.</span></span> <span data-ttu-id="5a2ed-126">Также скопируйте\\файл адовбс. Inc из C: Program Files\\Common Files\\\\System ADO в ту же папку, где находится файл ксмлреспонсе. ASP.</span><span class="sxs-lookup"><span data-stu-id="5a2ed-126">Also copy the adovbs.inc file from C:\\Program Files\\Common Files\\System\\Ado folder to the same folder where you have the XMLResponse.asp file.</span></span>

## <a name="step-4-receive-and-display-the-data"></a><span data-ttu-id="5a2ed-127">Шаг 4: получение и отображение данных</span><span class="sxs-lookup"><span data-stu-id="5a2ed-127">Step 4: Receive and display the data</span></span>

<span data-ttu-id="5a2ed-128">На этом этапе создается HTML-файл с внедренной службой [RDS. Объект элемента управления](datacontrol-object-rds.md) данных, указывающий на файл ксмлреспонсе. ASP для получения **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="5a2ed-128">In this step, you will create an HTML file with an embedded [RDS.DataControl](datacontrol-object-rds.md) object that points at the XMLResponse.asp file to get the **Recordset**.</span></span> 

1. <span data-ttu-id="5a2ed-129">Откройте Default. htm в текстовом редакторе, например в блокноте Windows, и добавьте следующий код.</span><span class="sxs-lookup"><span data-stu-id="5a2ed-129">Open default.htm with a text editor, such as Windows Notepad, and add the following code.</span></span> <span data-ttu-id="5a2ed-130">Замените слово "SQLServer" в URL-АДРЕСе именем компьютера сервера.</span><span class="sxs-lookup"><span data-stu-id="5a2ed-130">Replace "sqlserver" in the URL with the name of your server computer.</span></span>

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

2. <span data-ttu-id="5a2ed-131">Закройте файл Default. htm и сохраните его в той же папке, где вы сохранили Ксмлреспонсе. ASP.</span><span class="sxs-lookup"><span data-stu-id="5a2ed-131">Close the default.htm file and save it to the same folder where you saved XMLResponse.asp.</span></span> 

3. <span data-ttu-id="5a2ed-132">С помощью Internet Explorer 4,0 или более поздней версии `https://<sqlserver>/XMLPersist/default.htm` откройте URL-адрес и просмотрите результаты.</span><span class="sxs-lookup"><span data-stu-id="5a2ed-132">Using Internet Explorer 4.0 or later, open the URL `https://<sqlserver>/XMLPersist/default.htm` and observe the results.</span></span> <span data-ttu-id="5a2ed-133">Данные отображаются в связанной таблице DHTML.</span><span class="sxs-lookup"><span data-stu-id="5a2ed-133">The data is displayed in a bound DHTML table.</span></span> 

4. <span data-ttu-id="5a2ed-134">Теперь откройте URL- `https://<sqlserver>/XMLPersist/XMLResponse.asp` адрес и просмотрите результаты.</span><span class="sxs-lookup"><span data-stu-id="5a2ed-134">Now open the URL `https://<sqlserver>/XMLPersist/XMLResponse.asp` and observe the results.</span></span> <span data-ttu-id="5a2ed-135">Отобразится XML.</span><span class="sxs-lookup"><span data-stu-id="5a2ed-135">The XML is displayed.</span></span>




