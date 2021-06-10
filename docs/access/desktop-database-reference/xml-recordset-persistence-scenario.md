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

В этом сценарии будет создаваться приложение ASP (ASP), которое сохраняет содержимое объекта **Recordset** непосредственно к объекту asP **Response.**

> [!NOTE]
> Этот сценарий требует, чтобы на вашем сервере был установлен сервер информации в Интернете 5.0 (IIS) или позднее.

Возвращенный **набор записей** отображается в Internet Explorer с помощью [RDS. DataControl](datacontrol-object-rds.md).

Для создания этого сценария необходимы следующие действия:

1.  Настройка приложения.
2.  Получите данные.
3.  Отправка данных.
4.  Получение и отображение данных.

## <a name="step-1-set-up-the-application"></a>Шаг 1. Настройка приложения

1. Создайте виртуальный каталог IIS с именем **XMLPersist с** разрешениями скрипта. 

2. Создайте два новых текстовых файла в папке, в которую указывает виртуальный каталог, один с именем **XMLResponse.asp** и другой с именем **Default.htm**.


## <a name="step-2-get-the-data"></a>Шаг 2. Получить данные

На этом этапе вы напишете код, чтобы открыть ADO **Recordset** и подготовиться к отправке его клиенту. 

1. Откройте файл XMLResponse.asp с помощью текстового редактора, например Windows Блокнот, и вставьте следующий код:

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

2. Обязательно измените значение параметра Источник данных в strCon на имя Microsoft SQL Server компьютера.

3. Держите файл открытым и перейдите к следующему шагу.

## <a name="step-3-send-the-data"></a>Шаг 3. Отправка данных

Теперь, когда у вас есть **Набор записей,** необходимо отправить его клиенту, сэкономив его в качестве XML для объекта asP **Response.** 

1. Добавьте следующий код в нижней части XMLResponse.asp:

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

   Обратите внимание, что объект asP **Response** указывается в качестве назначения для метода **Сохранить** [набор](save-method-ado.md) записей. Предназначением метода **Сохранить** может быть любой объект, поддерживаюходящий интерфейс **IStream,** например объект ADO [Stream,](stream-object-ado.md) или имя файла, которое включает полный путь, к которому должен быть сохранен **набор** записей.

2. Сохраните и закрой XMLResponse.asp перед следующим шагом. Кроме того, скопируйте файл adovbs.inc из папки C: Program Files Common Files System Ado в ту же папку, где у вас есть \\ \\ файл \\ \\ XMLResponse.asp.

## <a name="step-4-receive-and-display-the-data"></a>Шаг 4. Получение и отображение данных

На этом этапе будет создаваться HTML-файл со встроенным [RDS. Объект DataControl,](datacontrol-object-rds.md) который указывает на файл XMLResponse.asp, чтобы получить **набор записей.** 

1. Откройте default.htm с текстовым редактором, например Windows Блокнот, и добавьте следующий код. Замените "sqlserver" в URL-адресе именем сервера.

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

2. Закрой default.htm файл и сохраните его в той же папке, в которой сохранен XMLResponse.asp. 

3. С помощью Internet Explorer 4.0 или более поздней версии откройте URL-адрес `https://<sqlserver>/XMLPersist/default.htm` и понаблюдать за результатами. Данные отображаются в связанной таблице DHTML. 

4. Теперь откройте URL-адрес `https://<sqlserver>/XMLPersist/XMLResponse.asp` и понаблюдать за результатами. Отображается XML.




