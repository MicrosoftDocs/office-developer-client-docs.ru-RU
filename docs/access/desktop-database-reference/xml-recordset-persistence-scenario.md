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
# <a name="xml-recordset-persistence-scenario"></a>Сценарий хранение записей XML

**Применимо к**: Access 2013, Office 2013

В данном сценарии создается приложение Active Server Pages (ASP), сохранение содержимого объекта **набора записей** непосредственно к объекту ASP **ответа** .

> [!NOTE]
> В этом случае необходимо, что сервер Internet Information Server 5.0 (IIS) или более поздней версии.

Возвращенный **набор записей** отображается в браузере Internet Explorer с помощью [RDS. DataControl](datacontrol-object-rds.md).

Для создания этого сценария необходимы следующие действия:

1.  Настройка приложения.
2.  Получение данных.
3.  Отправка данных.
4.  Получение и отображения данных.

## <a name="step-1-set-up-the-application"></a>Этап 1: Настройка приложения

1. Создайте виртуальный каталог IIS, с именем **XMLPersist** с разрешениями скрипта. 

2. Создайте две новые текстовые файлы в папку, на который указывает виртуальный каталог, один именованный **XMLResponse.asp**и другое с именем **Default.htm**.


## <a name="step-2-get-the-data"></a>Шаг 2: Получение данных

На этом этапе будет написание кода для открытия набора **записей** ADO и подготовка для отправки клиенту. 

1. Откройте файл XMLResponse.asp в текстовом редакторе, например в Блокноте и вставьте следующий код:

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

2. Не забудьте изменить значение параметра источника данных в strCon к имени компьютера Microsoft SQL Server.

3. Сохранение файла перейдите к следующему шагу.

## <a name="step-3-send-the-data"></a>Шаг 3: Отправка данных

Теперь, когда у вас есть **набор записей**, необходимо отправить его клиенту путем сохранения в формате XML объект ASP **ответа** . 

1. Добавьте следующий код в конец XMLResponse.asp:

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

   Обратите внимание на то, что объект ASP **ответа** указан как назначения для метода **записей** [Сохранить](save-method-ado.md) . Конечный метод **Save** может быть любой объект, который поддерживает интерфейс **IStream** , например, объект ADO [потока](stream-object-ado.md) или имя файла, который включает в себя полный путь к которой должен быть сохранен **набора записей** .

2. Сохраните и закройте XMLResponse.asp перед переходом к следующему шагу. Также скопируйте файл adovbs.inc из C:\\Program Files\\общие файлы\\системы\\Ado папки в ту же папку, где у вас есть файл XMLResponse.asp.

## <a name="step-4-receive-and-display-the-data"></a>Шаг 4: Получение и отображения данных

На этом этапе создается HTML-файла с внедренным [RDS. DataControl](datacontrol-object-rds.md) объект, указывающий на файл XMLResponse.asp для получения **набора записей**. 

1. Откройте файл default.htm в текстовом редакторе, например в Блокноте и добавьте следующий код. Замените «sqlserver» в URL-имя компьютера сервера.

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

2. Закройте файл default.htm и сохраните его в ту же папку, где был сохранен XMLResponse.asp. 

3. Internet Explorer версии 4.0 или более поздних версий, откройте URL-адрес `https://<sqlserver>/XMLPersist/default.htm` и просмотрите результаты. Данные отображаются в связанной таблице DHTML. 

4. Теперь откройте URL-адрес `https://<sqlserver>/XMLPersist/XMLResponse.asp` и просмотрите результаты. XML-код отображается.




