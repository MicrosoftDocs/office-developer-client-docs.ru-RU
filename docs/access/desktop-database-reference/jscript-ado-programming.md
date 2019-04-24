---
title: Программирование для ADO на JScript
TOCTitle: JScript ADO programming
ms:assetid: 2254f111-e6c2-1ad7-eb65-ee0550056d89
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249002(v=office.15)
ms:contentKeyID: 48543706
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 88a84f6fa3604286ca27651cefc999c96ff41d0e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32290893"
---
# <a name="jscript-ado-programming"></a>Программирование для ADO на JScript


**Область применения**: Access 2013, Office 2013


## <a name="creating-an-ado-project"></a>Создание проекта ADO

Microsoft JScript не поддерживает библиотеки типов, поэтому вам не нужно ссылаться на ADO в проекте. Следовательно, не поддерживаются связанные функции, такие как завершение командной строки. Кроме того, перечисленные константы ADO по умолчанию не определены в JScript.

Тем не менее, ADO предоставляет два включаемых файла со следующими определениями, которые будут использоваться в JScript:

- Для серверного скрипта используйте Адожавас. Inc, установленный\\в\\\\\\\\ папке "общие файлы" системы c: Program Files по умолчанию.

- Для клиентских скриптов используйте Адкжавас. Inc, установленный в папке\\c: Program Files\\\\System\\мсдак\\ по умолчанию.

Вы можете копировать и вставлять определения констант из этих файлов на страницы ASP или, если вы выполняете сценарии на стороне сервера, скопируйте файл Адожавас. Inc в папку на веб-сайте и ссылается на нее со страницы ASP следующим образом:

```javascript  
 
<!--#include File="adojavas.inc"--> 
```

## <a name="creating-ado-objects-in-jscript"></a>Создание объектов ADO в JScript

Вместо этого необходимо использовать вызов функции **CreateObject** :

```javascript  
 
var Rs1; 
Rs1 = Server.CreateObject("ADODB.Recordset"); 
```

## <a name="jscript-example"></a>Пример JScript

Приведенный ниже код представляет собой общий пример программирования на стороне сервера JScript в файле страницы Active Server Page (ASP), который открывает объект **Recordset** :

```javascript 
 
<%  @LANGUAGE="JScript" %> 
<!--#include File="adojavas.inc"--> 
<HTML> 
<BODY BGCOLOR="White" topmargin="10" leftmargin="10"> 
<% 
var Source = "SELECT * FROM Authors"; 
var Connect =  "Provider=sqloledb;Data Source=srv;" + 
    "Initial Catalog=Pubs;Integrated Security=SSPI;" 
var Rs1 = Server.CreateObject( "ADODB.Recordset.2.5" ); 
Rs1.Open(Source,Connect,adOpenForwardOnly); 
Response.Write("Success!"); 
%> 
</BODY> 
</HTML> 
```

