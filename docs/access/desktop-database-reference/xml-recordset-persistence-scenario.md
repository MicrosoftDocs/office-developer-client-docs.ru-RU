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

В этом сценарии создается приложение страниц Active Server (ASP), которое сохраняет содержимое объекта **Recordset** непосредственно в **ответном** объекте ASP.

> [!NOTE]
> Для этого сценария необходимо, чтобы на сервере был установлен сервер IIS 5,0 (IIS) или более поздней версии.

Возвращенный **набор записей** отображается в Internet Explorer с помощью [RDS. Элемент управления](datacontrol-object-rds.md).

Для создания этого сценария необходимо выполнить следующие действия:

1.  Настройка приложения.
2.  Получение данных.
3.  Отправьте данные.
4.  Получение и отображение данных.

## <a name="step-1-set-up-the-application"></a>Шаг 1: Настройка приложения

1. Создайте виртуальный каталог IIS с именем **ксмлперсист** с разрешениями для скриптов. 

2. Создайте два новых текстовых файла в папке, в которой указываются виртуальные каталоги, один с именем **ксмлреспонсе. ASP**и другой с именем **Default. htm**.


## <a name="step-2-get-the-data"></a>Шаг 2: получение данных

На этом этапе будет написан код для открытия **набора записей** ADO и подготовки к его отправке клиенту. 

1. Откройте файл Ксмлреспонсе. ASP в текстовом редакторе, например в блокноте Windows, и вставьте следующий код:

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

2. Не забудьте изменить значение параметра источника данных в Стркон на имя компьютера Microsoft SQL Server.

3. Оставьте файл открытым и перейдите к следующему шагу.

## <a name="step-3-send-the-data"></a>Шаг 3: отправка данных

Теперь, когда у вас есть объект **Recordset**, его необходимо отправить клиенту, сохранив его в виде XML-файла в **ответный** объект ASP. 

1. Добавьте следующий код в нижнюю часть Ксмлреспонсе. ASP:

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

   Обратите внимание, что объект **ответа** ASP указывается в качестве назначения для метода [Save](save-method-ado.md) **набора записей** . В качестве места назначения метода **Save** может быть любой объект, поддерживающий интерфейс **IStream** , например объект [Stream](stream-object-ado.md) объекта ADO, или имя файла, включающее полный путь, по которому необходимо сохранить **набор записей** .

2. Сохраните и закройте Ксмлреспонсе. ASP, прежде чем переходить к следующему шагу. Также скопируйте\\файл адовбс. Inc из C: Program Files\\Common Files\\\\System ADO в ту же папку, где находится файл ксмлреспонсе. ASP.

## <a name="step-4-receive-and-display-the-data"></a>Шаг 4: получение и отображение данных

На этом этапе создается HTML-файл с внедренной службой [RDS. Объект элемента управления](datacontrol-object-rds.md) данных, указывающий на файл ксмлреспонсе. ASP для получения **набора записей**. 

1. Откройте Default. htm в текстовом редакторе, например в блокноте Windows, и добавьте следующий код. Замените слово "SQLServer" в URL-АДРЕСе именем компьютера сервера.

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

2. Закройте файл Default. htm и сохраните его в той же папке, где вы сохранили Ксмлреспонсе. ASP. 

3. С помощью Internet Explorer 4,0 или более поздней версии `https://<sqlserver>/XMLPersist/default.htm` откройте URL-адрес и просмотрите результаты. Данные отображаются в связанной таблице DHTML. 

4. Теперь откройте URL- `https://<sqlserver>/XMLPersist/XMLResponse.asp` адрес и просмотрите результаты. Отобразится XML.




