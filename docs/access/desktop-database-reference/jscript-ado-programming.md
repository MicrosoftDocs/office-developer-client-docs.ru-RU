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
# <a name="jscript-ado-programming"></a><span data-ttu-id="76181-102">Программирование для ADO на JScript</span><span class="sxs-lookup"><span data-stu-id="76181-102">JScript ADO programming</span></span>


<span data-ttu-id="76181-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="76181-103">**Applies to**: Access 2013, Office 2013</span></span>


## <a name="creating-an-ado-project"></a><span data-ttu-id="76181-104">Создание проекта ADO</span><span class="sxs-lookup"><span data-stu-id="76181-104">Creating an ADO Project</span></span>

<span data-ttu-id="76181-105">Microsoft JScript не поддерживает библиотеки типов, поэтому вам не нужно ссылаться на ADO в проекте.</span><span class="sxs-lookup"><span data-stu-id="76181-105">Microsoft JScript does not support type libraries, so you do not need to reference ADO in your project.</span></span> <span data-ttu-id="76181-106">Следовательно, не поддерживаются связанные функции, такие как завершение командной строки.</span><span class="sxs-lookup"><span data-stu-id="76181-106">Consequently, no associated features such as command line completion are supported.</span></span> <span data-ttu-id="76181-107">Кроме того, перечисленные константы ADO по умолчанию не определены в JScript.</span><span class="sxs-lookup"><span data-stu-id="76181-107">Also, by default, ADO enumerated constants are not defined in JScript.</span></span>

<span data-ttu-id="76181-108">Тем не менее, ADO предоставляет два включаемых файла со следующими определениями, которые будут использоваться в JScript:</span><span class="sxs-lookup"><span data-stu-id="76181-108">However, ADO provides you with two include files containing the following definitions to be used with JScript:</span></span>

- <span data-ttu-id="76181-109">Для серверного скрипта используйте Адожавас. Inc, установленный\\в\\\\\\\\ папке "общие файлы" системы c: Program Files по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="76181-109">For server-side scripting use Adojavas.inc, which is installed in the c:\\Program Files\\Common Files\\System\\ado\\ folder by default.</span></span>

- <span data-ttu-id="76181-110">Для клиентских скриптов используйте Адкжавас. Inc, установленный в папке\\c: Program Files\\\\System\\мсдак\\ по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="76181-110">For client-side scripting use Adcjavas.inc, which is installed in the c:\\Program Files\\Common Files\\System\\msdac\\ folder by default.</span></span>

<span data-ttu-id="76181-111">Вы можете копировать и вставлять определения констант из этих файлов на страницы ASP или, если вы выполняете сценарии на стороне сервера, скопируйте файл Адожавас. Inc в папку на веб-сайте и ссылается на нее со страницы ASP следующим образом:</span><span class="sxs-lookup"><span data-stu-id="76181-111">You can either copy and paste constant definitions from these files into your ASP pages, or, if you are doing server-side scripting, copy Adojavas.inc file to a folder on your website and references it from your ASP page like this:</span></span>

```javascript  
 
<!--#include File="adojavas.inc"--> 
```

## <a name="creating-ado-objects-in-jscript"></a><span data-ttu-id="76181-112">Создание объектов ADO в JScript</span><span class="sxs-lookup"><span data-stu-id="76181-112">Creating ADO Objects in JScript</span></span>

<span data-ttu-id="76181-113">Вместо этого необходимо использовать вызов функции **CreateObject** :</span><span class="sxs-lookup"><span data-stu-id="76181-113">You must instead use the **CreateObject** function call:</span></span>

```javascript  
 
var Rs1; 
Rs1 = Server.CreateObject("ADODB.Recordset"); 
```

## <a name="jscript-example"></a><span data-ttu-id="76181-114">Пример JScript</span><span class="sxs-lookup"><span data-stu-id="76181-114">JScript Example</span></span>

<span data-ttu-id="76181-115">Приведенный ниже код представляет собой общий пример программирования на стороне сервера JScript в файле страницы Active Server Page (ASP), который открывает объект **Recordset** :</span><span class="sxs-lookup"><span data-stu-id="76181-115">The following code is a generic example of JScript server-side programming in an Active Server Page (ASP) file that opens a **Recordset** object:</span></span>

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

