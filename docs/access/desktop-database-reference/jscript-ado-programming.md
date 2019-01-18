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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708974"
---
# <a name="jscript-ado-programming"></a>Программирование для ADO на JScript


**Применимо к**: Access 2013, Office 2013


## <a name="creating-an-ado-project"></a>Создание проекта ADO

Microsoft JScript не поддерживает библиотеки типов, поэтому нет необходимости ссылку ADO в проекте. Следовательно не связанные функции, например завершения командной строки, поддерживаются. Кроме того по умолчанию, ADO перечисленных констант не определены в JScript.

Тем не менее ADO предоставляет вам с двумя включают файлы, содержащие следующие определения, который будет использоваться с JScript:

- Для использования на сервере сценариев Adojavas.inc, которая устанавливается в c:\\Program Files\\общие файлы\\системы\\ado\\ папки по умолчанию.

- Для использования сценариев на стороне клиента Adcjavas.inc, которая устанавливается в c:\\Program Files\\общие файлы\\системы\\msdac\\ папки по умолчанию.

Можно скопировать и вставить определения констант из этих файлов в страницы ASP или, при выполнении сценариев на стороне сервера, скопируйте файл Adojavas.inc в папку на веб-сайте и ссылается на странице ASP следующим образом:

```javascript  
 
<!--#include File="adojavas.inc"--> 
```

## <a name="creating-ado-objects-in-jscript"></a>Создание объектов ADO в JScript

Необходимо использовать вместо этого вызов функции **CreateObject** :

```javascript  
 
var Rs1; 
Rs1 = Server.CreateObject("ADODB.Recordset"); 
```

## <a name="jscript-example"></a>Пример JScript

Ниже показан общий пример программирования JScript на сервере в файле страницы ASP (Active Server), который открывает объект **набора записей** :

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

