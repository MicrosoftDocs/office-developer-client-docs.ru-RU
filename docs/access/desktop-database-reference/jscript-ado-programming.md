---
title: Программирование для ADO на JScript
TOCTitle: JScript ADO Programming
ms:assetid: 2254f111-e6c2-1ad7-eb65-ee0550056d89
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249002(v=office.15)
ms:contentKeyID: 48543706
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dd470482c8e4a2e9228247c5eea4512367ca6483
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867239"
---
# <a name="jscript-ado-programming"></a><span data-ttu-id="58022-102">Программирование для ADO на JScript</span><span class="sxs-lookup"><span data-stu-id="58022-102">JScript ADO Programming</span></span>


<span data-ttu-id="58022-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="58022-103">**Applies to**: Access 2013, Office 2013</span></span>


## <a name="creating-an-ado-project"></a><span data-ttu-id="58022-104">Создание проекта ADO</span><span class="sxs-lookup"><span data-stu-id="58022-104">Creating an ADO Project</span></span>

<span data-ttu-id="58022-105">Microsoft JScript не поддерживает библиотеки типов, поэтому нет необходимости ссылку ADO в проекте.</span><span class="sxs-lookup"><span data-stu-id="58022-105">Microsoft JScript does not support type libraries, so you do not need to reference ADO in your project.</span></span> <span data-ttu-id="58022-106">Следовательно не связанные функции, например завершения командной строки, поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="58022-106">Consequently, no associated features such as command line completion are supported.</span></span> <span data-ttu-id="58022-107">Кроме того по умолчанию, ADO перечисленных констант не определены в JScript.</span><span class="sxs-lookup"><span data-stu-id="58022-107">Also, by default, ADO enumerated constants are not defined in JScript.</span></span>

<span data-ttu-id="58022-108">Тем не менее ADO предоставляет вам с двумя включают файлы, содержащие следующие определения, который будет использоваться с JScript:</span><span class="sxs-lookup"><span data-stu-id="58022-108">However, ADO provides you with two include files containing the following definitions to be used with JScript:</span></span>

- <span data-ttu-id="58022-109">Для использования на сервере сценариев Adojavas.inc, которая устанавливается в c:\\Program Files\\общие файлы\\системы\\ado\\ папки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="58022-109">For server-side scripting use Adojavas.inc, which is installed in the c:\\Program Files\\Common Files\\System\\ado\\ folder by default.</span></span>

- <span data-ttu-id="58022-110">Для использования сценариев на стороне клиента Adcjavas.inc, которая устанавливается в c:\\Program Files\\общие файлы\\системы\\msdac\\ папки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="58022-110">For client-side scripting use Adcjavas.inc, which is installed in the c:\\Program Files\\Common Files\\System\\msdac\\ folder by default.</span></span>

<span data-ttu-id="58022-111">Можно скопировать и вставить определения констант из этих файлов в страницы ASP или, при выполнении сценариев на стороне сервера, скопируйте файл Adojavas.inc в папку на веб-сайте и ссылается на странице ASP следующим образом:</span><span class="sxs-lookup"><span data-stu-id="58022-111">You can either copy and paste constant definitions from these files into your ASP pages, or, if you are doing server-side scripting, copy Adojavas.inc file to a folder on your website and references it from your ASP page like this:</span></span>

```javascript  
 
<!--#include File="adojavas.inc"--> 
```

## <a name="creating-ado-objects-in-jscript"></a><span data-ttu-id="58022-112">Создание объектов ADO в JScript</span><span class="sxs-lookup"><span data-stu-id="58022-112">Creating ADO Objects in JScript</span></span>

<span data-ttu-id="58022-113">Необходимо использовать вместо этого вызов функции **CreateObject** :</span><span class="sxs-lookup"><span data-stu-id="58022-113">You must instead use the **CreateObject** function call:</span></span>

```javascript  
 
var Rs1; 
Rs1 = Server.CreateObject("ADODB.Recordset"); 
```

## <a name="jscript-example"></a><span data-ttu-id="58022-114">Пример JScript</span><span class="sxs-lookup"><span data-stu-id="58022-114">JScript Example</span></span>

<span data-ttu-id="58022-115">Ниже показан общий пример программирования JScript на сервере в файле страницы ASP (Active Server), который открывает объект **набора записей** :</span><span class="sxs-lookup"><span data-stu-id="58022-115">The following code is a generic example of JScript server-side programming in an Active Server Page (ASP) file that opens a **Recordset** object:</span></span>

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

