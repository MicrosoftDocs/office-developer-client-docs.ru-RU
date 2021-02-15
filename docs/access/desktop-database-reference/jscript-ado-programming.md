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
# <a name="jscript-ado-programming"></a><span data-ttu-id="6dae7-102">Программирование для ADO на JScript</span><span class="sxs-lookup"><span data-stu-id="6dae7-102">JScript ADO programming</span></span>


<span data-ttu-id="6dae7-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6dae7-103">**Applies to**: Access 2013, Office 2013</span></span>


## <a name="creating-an-ado-project"></a><span data-ttu-id="6dae7-104">Создание проекта ADO</span><span class="sxs-lookup"><span data-stu-id="6dae7-104">Creating an ADO Project</span></span>

<span data-ttu-id="6dae7-105">Microsoft JScript не поддерживает библиотеки типов, поэтому нет необходимости ссылаться на ADO в проекте.</span><span class="sxs-lookup"><span data-stu-id="6dae7-105">Microsoft JScript does not support type libraries, so you do not need to reference ADO in your project.</span></span> <span data-ttu-id="6dae7-106">Следовательно, связанные функции, такие как завершение командной строки, не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="6dae7-106">Consequently, no associated features such as command line completion are supported.</span></span> <span data-ttu-id="6dae7-107">Кроме того, по умолчанию в JScript не определены константы из JScript.</span><span class="sxs-lookup"><span data-stu-id="6dae7-107">Also, by default, ADO enumerated constants are not defined in JScript.</span></span>

<span data-ttu-id="6dae7-108">Однако ADO предоставляет два файла, содержащих следующие определения, которые будут использоваться с JScript:</span><span class="sxs-lookup"><span data-stu-id="6dae7-108">However, ADO provides you with two include files containing the following definitions to be used with JScript:</span></span>

- <span data-ttu-id="6dae7-109">Для сценариев на стороне сервера используйте Adojavas.inc, который по умолчанию устанавливается в папке c: \\ Program Files Common Files System \\ \\ \\ \\ ado.</span><span class="sxs-lookup"><span data-stu-id="6dae7-109">For server-side scripting use Adojavas.inc, which is installed in the c:\\Program Files\\Common Files\\System\\ado\\ folder by default.</span></span>

- <span data-ttu-id="6dae7-110">Для клиентских сценариев используйте файл Adcjavas.inc, установленный в папке \\ msdac program Files Common Files System по \\ \\ \\ \\ умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6dae7-110">For client-side scripting use Adcjavas.inc, which is installed in the c:\\Program Files\\Common Files\\System\\msdac\\ folder by default.</span></span>

<span data-ttu-id="6dae7-111">Вы можете либо скопировать и вложить определения констант из этих файлов на страницы ASP, либо, если вы работаете с серверными сценариями, скопируйте файл Adojavas.inc в папку на вашем веб-сайте и ссылаетесь на него со страницы ASP, как по этому:</span><span class="sxs-lookup"><span data-stu-id="6dae7-111">You can either copy and paste constant definitions from these files into your ASP pages, or, if you are doing server-side scripting, copy Adojavas.inc file to a folder on your website and references it from your ASP page like this:</span></span>

```javascript  
 
<!--#include File="adojavas.inc"--> 
```

## <a name="creating-ado-objects-in-jscript"></a><span data-ttu-id="6dae7-112">Создание объектов ADO в JScript</span><span class="sxs-lookup"><span data-stu-id="6dae7-112">Creating ADO Objects in JScript</span></span>

<span data-ttu-id="6dae7-113">Вместо этого необходимо использовать вызов **функции CreateObject:**</span><span class="sxs-lookup"><span data-stu-id="6dae7-113">You must instead use the **CreateObject** function call:</span></span>

```javascript  
 
var Rs1; 
Rs1 = Server.CreateObject("ADODB.Recordset"); 
```

## <a name="jscript-example"></a><span data-ttu-id="6dae7-114">JScript пример</span><span class="sxs-lookup"><span data-stu-id="6dae7-114">JScript Example</span></span>

<span data-ttu-id="6dae7-115">Следующий код является универсальным примером программирования JScript на стороне сервера в ASP-файле, который открывает объект **Recordset:**</span><span class="sxs-lookup"><span data-stu-id="6dae7-115">The following code is a generic example of JScript server-side programming in an Active Server Page (ASP) file that opens a **Recordset** object:</span></span>

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

