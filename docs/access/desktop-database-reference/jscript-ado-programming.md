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


## <a name="creating-an-ado-project"></a>Создание ADO-Project

Microsoft JScript не поддерживает библиотеки типов, поэтому не нужно ссылаться на ADO в проекте. Следовательно, не поддерживаются связанные функции, такие как завершение командной строки. Кроме того, по умолчанию в JScript не определяются переопределенные константы ADO.

Тем не менее, ADO предоставляет вам два файла, содержащих следующие определения, которые будут использоваться с JScript:

- Для серверного скриптинга используйте Adojavas.inc, который устанавливается в папке c: \\ Program Files Common Files System \\ \\ \\ ado \\ folder по умолчанию.

- Для клиентского скриптинга используйте Adcjavas.inc, который устанавливается в папке c: \\ Program Files Common Files System \\ \\ \\ msdac по \\ умолчанию.

Вы можете скопировать и вклеить постоянные определения из этих файлов на страницы ASP или, если вы работаете над сценарием на сервере, скопируйте файл Adojavas.inc в папку на веб-сайте и ссылаетесь на него со страницы ASP:

```javascript  
 
<!--#include File="adojavas.inc"--> 
```

## <a name="creating-ado-objects-in-jscript"></a>Создание объектов ADO в JScript

Вместо этого необходимо использовать **вызов функции CreateObject:**

```javascript  
 
var Rs1; 
Rs1 = Server.CreateObject("ADODB.Recordset"); 
```

## <a name="jscript-example"></a>JScript Пример

Следующий код — это общий пример программирования JScript серверов в файле Active Server Page (ASP), открываемом **объекту Recordset:**

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

