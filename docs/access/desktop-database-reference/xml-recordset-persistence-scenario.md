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
# <a name="xml-recordset-persistence-scenario"></a>Сценарий сохранения набора записей XML

**Область применения**: Access 2013, Office 2013

В этом сценарии создается ASP ASP, которое сохраняет содержимое объекта **Recordset** непосредственно в объекте ответа **ASP.**

> [!NOTE]
> Для этого сценария требуется, чтобы на сервере был установлен internet Information Server 5.0 (IIS) или более поздней.

Возвращенный **набор записей** отображается в Internet Explorer с помощью [RDS. DataControl](datacontrol-object-rds.md).

Для создания этого сценария необходимо следующее:

1.  Настройка приложения.
2.  Получите данные.
3.  Отправьте данные.
4.  Получение и отображение данных.

## <a name="step-1-set-up-the-application"></a>Шаг 1. Настройка приложения

1. Создайте виртуальный каталог IIS с именем **XMLPersist** с разрешениями скрипта. 

2. Создайте два текстовых файла в папке, на которую указывает виртуальный каталог: один с именем **XMLResponse.asp,** а другой с именем **Default.htm**.


## <a name="step-2-get-the-data"></a>Шаг 2. Получите данные

На этом этапе вы напишете код, чтобы открыть набор записей **ADO** и подготовиться к его отправке клиенту. 

1. Откройте файл XMLResponse.asp в текстовом редакторе, например в Блокноте Windows, и вставьте следующий код:

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

2. Обязательно измените значение параметра источника данных в strCon на имя Microsoft SQL Server компьютера.

3. Оохраняем файл открытым и перейдите к следующему шагу.

## <a name="step-3-send-the-data"></a>Шаг 3. Отправка данных

Теперь, когда у вас есть **набор записей,** необходимо отправить его клиенту, с сохранением его в XML-объекте ответа **ASP.** 

1. Добавьте следующий код в нижнюю часть XMLResponse.asp:

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

   Обратите внимание, что **объект ответа** ASP указывается в качестве назначения для метода Save **в наборе** [записей.](save-method-ado.md) Назначением метода **Save** может быть любой объект, который поддерживает **интерфейс IStream,** например объект ADO [Stream,](stream-object-ado.md) или имя  файла, который включает полный путь, по которому будет сохранен набор записей.

2. Сохраните и закроите XMLResponse.asp, прежде чем переходить к следующему шагу. Кроме того, скопируйте файл adovbs.inc из папки C: Program Files Common Files System Ado в ту же папку, в которой находится файл \\ \\ \\ \\ XMLResponse.asp.

## <a name="step-4-receive-and-display-the-data"></a>Шаг 4. Получение и отображение данных

На этом этапе вы создадим HTML-файл с внедренными [RDS. Объект DataControl,](datacontrol-object-rds.md) который указывает на файл XMLResponse.asp для получения **объекта Recordset.** 

1. Откройте default.htm с помощью текстового редактора, например Блокнота Windows, и добавьте следующий код. Замените "sqlserver" в URL-адресе именем сервера.

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

2. Закроем default.htm и сохраните его в той же папке, в которой сохранен файл XMLResponse.asp. 

3. В Internet Explorer 4.0 или более поздней версии откройте URL-адрес `https://<sqlserver>/XMLPersist/default.htm` и наблюдайте за результатами. Данные отображаются в привязанной таблице DHTML. 

4. Теперь откройте URL-адрес `https://<sqlserver>/XMLPersist/XMLResponse.asp` и понаблюдать за результатами. Отобразит XML..




