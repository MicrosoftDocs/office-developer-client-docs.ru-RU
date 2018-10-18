---
title: RDS Tutorial (VBScript)
TOCTitle: RDS Tutorial (VBScript)
ms:assetid: 7a6596fd-00b9-a637-7d00-fb55a621305f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249506(v=office.15)
ms:contentKeyID: 48545792
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d87dc84217b716505302464825a1857fecf67669
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606824"
---
# <a name="rds-tutorial-vbscript"></a><span data-ttu-id="8bf98-102">RDS Tutorial (VBScript)</span><span class="sxs-lookup"><span data-stu-id="8bf98-102">RDS Tutorial (VBScript)</span></span>


<span data-ttu-id="8bf98-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8bf98-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="8bf98-104">Это учебник служб удаленных рабочих СТОЛОВ, написанных на языке Visual Basic Scripting Edition.</span><span class="sxs-lookup"><span data-stu-id="8bf98-104">This is the RDS Tutorial, written in Microsoft Visual Basic Scripting Edition.</span></span> <span data-ttu-id="8bf98-105">Описание назначения в этом руководстве в разделе [При помощи учебника по служб удаленных рабочих СТОЛОВ](chapter-12-rds-tutorial.md).</span><span class="sxs-lookup"><span data-stu-id="8bf98-105">For a description of the purpose of this tutorial, see the [RDS Tutorial](chapter-12-rds-tutorial.md).</span></span>

<span data-ttu-id="8bf98-106">В этом руководстве [RDS. DataControl](datacontrol-object-rds.md) и [RDS. Пространства данных](dataspace-object-rds.md) создан во время разработки, то есть, определенные с помощью тегов объектов, следующим образом:.</span><span class="sxs-lookup"><span data-stu-id="8bf98-106">In this tutorial, [RDS.DataControl](datacontrol-object-rds.md) and [RDS.DataSpace](dataspace-object-rds.md) are created at design time — that is, they are defined with object tags, like this: .</span></span> <span data-ttu-id="8bf98-107">Кроме того они может быть создан во время выполнения с помощью метода **Server.CreateObject** .</span><span class="sxs-lookup"><span data-stu-id="8bf98-107">Alternatively, they could be created at run time with the **Server.CreateObject** method.</span></span> <span data-ttu-id="8bf98-108">Например **RDS. DataControl** может быть создан следующим образом:</span><span class="sxs-lookup"><span data-stu-id="8bf98-108">For example, the **RDS.DataControl** object could be created like this:</span></span>

```vb
    Set DC = Server.CreateObject("RDS.DataControl") 
     <!-- RDS.DataControl --> 
     <OBJECT 
     ID="DC1" CLASSID="CLSID:BD96C556-65A3-11D0-983A-00C04FC29E33"> 
     </OBJECT> 
     
     <!-- RDS.DataSpace --> 
     <OBJECT 
     ID="DS1" WIDTH=1 HEIGHT=1 
     CLASSID="CLSID:BD96C556-65A3-11D0-983A-00C04FC29E36"> 
     </OBJECT> 
     
     <SCRIPT LANGUAGE="VBScript"> 
     
     Sub RDSTutorial() 
     Dim DF1 
```

<span data-ttu-id="8bf98-109">**Шаг 1 — Укажите программы сервера**</span><span class="sxs-lookup"><span data-stu-id="8bf98-109">**Step 1 — Specify a server program**</span></span>

<span data-ttu-id="8bf98-110"><<<<<<< HEAD VBScript можно получить имя веб-сервера IIS он выполняется с помощью метода VBScript **Request.ServerVariables** для страницы ASP: === VBScript можно получить имя веб-сайта IIS Server он выполняется с помощью метода VBScript **Request.ServerVariables** для страницы ASP:</span><span class="sxs-lookup"><span data-stu-id="8bf98-110"><<<<<<< HEAD VBScript can discover the name of the IIS Web server it is running on by accessing the VBScript **Request.ServerVariables** method available to Active Server Pages: ======= VBScript can discover the name of the IIS web server it is running on by accessing the VBScript **Request.ServerVariables** method available to Active Server Pages:</span></span>
>>>>>>> <span data-ttu-id="8bf98-111">master</span><span class="sxs-lookup"><span data-stu-id="8bf98-111">master</span></span>

```vb 
 
"https://<%=Request.ServerVariables("SERVER_NAME")%>" 
```

<span data-ttu-id="8bf98-112">Тем не менее в этом руководстве используйте мнимой server «сервер».</span><span class="sxs-lookup"><span data-stu-id="8bf98-112">However, for this tutorial, use the imaginary server, "yourServer".</span></span>


> [!NOTE]
> <P><span data-ttu-id="8bf98-113">Обратите внимание на тип данных <STRONG>ByRef</STRONG> аргументов.</span><span class="sxs-lookup"><span data-stu-id="8bf98-113">Pay attention to the data type of <STRONG>ByRef</STRONG> arguments.</span></span> <span data-ttu-id="8bf98-114">VBScript не позволяет указать тип переменной, поэтому всегда необходимо передать переменную типа Variant.</span><span class="sxs-lookup"><span data-stu-id="8bf98-114">VBScript does not let you specify the variable type, so you must always pass a Variant.</span></span> <span data-ttu-id="8bf98-115">При использовании HTTP, служб удаленных рабочих СТОЛОВ можно передать переменную типа Variant в метод, требующей не тип Variant, если вызвать его с <STRONG>RDS. Пространства данных</STRONG> объекта метод <A href="createobject-method-rds.md">CreateObject</A> .</span><span class="sxs-lookup"><span data-stu-id="8bf98-115">When using HTTP, RDS will allow you to pass a Variant to a method that expects a non-Variant if you invoke it with the <STRONG>RDS.DataSpace</STRONG> object <A href="createobject-method-rds.md">CreateObject</A> method.</span></span> <span data-ttu-id="8bf98-116">При использовании DCOM или на сервере в процессе, соответствующие типы параметров на сторонах клиента и сервера или появится сообщение об ошибке «Несоответствие типов».</span><span class="sxs-lookup"><span data-stu-id="8bf98-116">When using DCOM or an in-process server, match the parameter types on the client and server sides or you will receive a "Type Mismatch" error.</span></span></P>

```vb
 
Set DF1 = DS1.CreateObject("RDSServer.DataFactory", "https://yourServer") 
```

<span data-ttu-id="8bf98-117">**Шаг 2a — вызова программы сервера с RDS. DataControl**</span><span class="sxs-lookup"><span data-stu-id="8bf98-117">**Step 2a — Invoke the server program with RDS.DataControl**</span></span>

<span data-ttu-id="8bf98-118">В этом примере — это просто комментарий, демонстрации поведения по умолчанию **RDS. DataControl** для выполнения указанного запроса.</span><span class="sxs-lookup"><span data-stu-id="8bf98-118">This example is merely a comment demonstrating that the default behavior of the **RDS.DataControl** is to perform the specified query.</span></span>

```vb
 
<OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="DC1"> 
 <PARAM NAME="SQL" VALUE="SELECT * FROM Authors"> 
 <PARAM NAME="Connect" VALUE="DSN=Pubs;"> 
 <PARAM NAME="Server" VALUE="https://yourServer/"> 
</OBJECT> 
... 
<SCRIPT LANGUAGE="VBScript"> 
 
Sub RDSTutorial2A() 
 Dim RS 
 DC1.Refresh 
 Set RS = DC1.Recordset 
... 
```

<span data-ttu-id="8bf98-119">**Этап 2б — вызова программы сервера с RDSServer.DataFactory**</span><span class="sxs-lookup"><span data-stu-id="8bf98-119">**Step 2b — Invoke the server program with RDSServer.DataFactory**</span></span>

<span data-ttu-id="8bf98-120">**Шаг 3 — Сервер получает набор записей**</span><span class="sxs-lookup"><span data-stu-id="8bf98-120">**Step 3 — Server obtains a Recordset**</span></span>

<span data-ttu-id="8bf98-121">**Шаг 4 — Сервер возвращает набор записей**</span><span class="sxs-lookup"><span data-stu-id="8bf98-121">**Step 4 — Server returns the Recordset**</span></span>

```vb
 
Set RS = DF1.Query("DSN=Pubs;", "SELECT * FROM Authors") 
```

<span data-ttu-id="8bf98-122">**Шаг 5 — DataControl осуществляется могут использоваться элементы управления visual**</span><span class="sxs-lookup"><span data-stu-id="8bf98-122">**Step 5 — DataControl is made usable by visual controls**</span></span>

```vb
 
' Assign the returned recordset to the DataControl. 
 
DC1.SourceRecordset = RS 
```

<span data-ttu-id="8bf98-123">**Шаг 6a — изменения отправляются на сервер с RDS. DataControl**</span><span class="sxs-lookup"><span data-stu-id="8bf98-123">**Step 6a — Changes are sent to the server with RDS.DataControl**</span></span>

<span data-ttu-id="8bf98-124">В этом примере — это просто комментарий демонстрируется, как **RDS. DataControl** выполняет обновление.</span><span class="sxs-lookup"><span data-stu-id="8bf98-124">This example is merely a comment demonstrating how the **RDS.DataControl** performs updates.</span></span>

```vb
 
<OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="DC1"> 
 <PARAM NAME="SQL" VALUE="SELECT * FROM Authors"> 
 <PARAM NAME="Connect" VALUE="DSN=Pubs;"> 
 <PARAM NAME="Server" VALUE="https://yourServer/"> 
</OBJECT> 
... 
<SCRIPT LANGUAGE="VBScript"> 
 
Sub RDSTutorial6A() 
Dim RS 
DC1.Refresh 
... 
Set RS = DC1.Recordset 
' Edit the Recordset object... 
' The SERVER and CONNECT properties are already set from Step 2A. 
Set DC1.SourceRecordset = RS 
... 
DC1.SubmitChanges 
```

<span data-ttu-id="8bf98-125">**Шаг 6b — изменения отправляются на сервер с RDSServer.DataFactory**</span><span class="sxs-lookup"><span data-stu-id="8bf98-125">**Step 6b — Changes are sent to the server with RDSServer.DataFactory**</span></span>

```vb
 
DF.SubmitChanges"DSN=Pubs", RS 
 
End Sub 
</SCRIPT> 
</BODY> 
</HTML> 
```

<span data-ttu-id="8bf98-126">**Это конце обучения.**</span><span class="sxs-lookup"><span data-stu-id="8bf98-126">**This is the end of the tutorial.**</span></span>

