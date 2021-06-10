---
title: VBScript ADO Programming
TOCTitle: VBScript ADO Programming
ms:assetid: 24be1c70-8813-ed98-c3e5-fb33a68e7b41
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249019(v=office.15)
ms:contentKeyID: 48543764
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4aff2c8b3394321367851ad82e4e7efe98badff8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306029"
---
# <a name="vbscript-ado-programming"></a><span data-ttu-id="ff5b7-102">Программирование для ADO на VBScript</span><span class="sxs-lookup"><span data-stu-id="ff5b7-102">VBScript ADO programming</span></span>


<span data-ttu-id="ff5b7-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ff5b7-103">**Applies to**: Access 2013, Office 2013</span></span> 

## <a name="creating-an-ado-project"></a><span data-ttu-id="ff5b7-104">Создание ADO-Project</span><span class="sxs-lookup"><span data-stu-id="ff5b7-104">Creating an ADO Project</span></span>

<span data-ttu-id="ff5b7-105">Microsoft Visual Basic, Scripting Edition не поддерживает библиотеки типов, поэтому вам не нужно ссылаться на ADO в проекте.</span><span class="sxs-lookup"><span data-stu-id="ff5b7-105">Microsoft Visual Basic, Scripting Edition does not support type libraries, so you do not need to reference ADO in your project.</span></span> <span data-ttu-id="ff5b7-106">Следовательно, не поддерживаются связанные функции, такие как завершение командной строки.</span><span class="sxs-lookup"><span data-stu-id="ff5b7-106">Consequently, no associated features such as command line completion are supported.</span></span> <span data-ttu-id="ff5b7-107">Кроме того, по умолчанию в VBScript не определены константы ADO.</span><span class="sxs-lookup"><span data-stu-id="ff5b7-107">Also, by default, ADO enumerated constants are not defined in VBScript.</span></span>

<span data-ttu-id="ff5b7-108">Тем не менее, ADO предоставляет вам два файла, содержащих следующие определения, которые будут использоваться с VBScript:</span><span class="sxs-lookup"><span data-stu-id="ff5b7-108">However, ADO provides you with two include files containing the following definitions to be used with VBScript:</span></span>

  - <span data-ttu-id="ff5b7-109">Для серверного скриптинга используйте Adovbs.inc, который устанавливается в папке ado c: \\ Program Files Common Files System по \\ \\ \\ \\ умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ff5b7-109">For server-side scripting use Adovbs.inc, which is installed in the c:\\Program Files\\Common Files\\System\\ado\\ folder by default.</span></span>

  - <span data-ttu-id="ff5b7-110">Для клиентского скриптинга используйте Adcvbs.inc, который устанавливается в папке c: Program \\ Files Common Files System \\ \\ \\ msdac по \\ умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ff5b7-110">For client-side scripting use Adcvbs.inc, which is installed in the c:\\Program Files\\Common Files\\System\\msdac\\ folder by default.</span></span>

<span data-ttu-id="ff5b7-111">Вы можете скопировать и вклеить постоянные определения из этих файлов на страницы ASP или, если вы работаете над сценарием на сервере, скопируйте файл Adovbs.inc в папку на веб-сайте и соположите его со страницы ASP:</span><span class="sxs-lookup"><span data-stu-id="ff5b7-111">You can either copy and paste constant definitions from these files into your ASP pages, or, if you are doing server-side scripting, copy Adovbs.inc file to a folder on your website and referencing it from your ASP page like this:</span></span>

```vb 
 
<!--#include File="adovbs.inc"--> 
```

## <a name="creating-ado-objects-in-vbscript"></a><span data-ttu-id="ff5b7-112">Создание объектов ADO в VBScript</span><span class="sxs-lookup"><span data-stu-id="ff5b7-112">Creating ADO Objects in VBScript</span></span>

<span data-ttu-id="ff5b7-113">Для назначения объектов определенному типу в VBScript нельзя использовать заявление **Dim.**</span><span class="sxs-lookup"><span data-stu-id="ff5b7-113">You cannot use the **Dim** statement to assign objects to a specific type in VBScript.</span></span> <span data-ttu-id="ff5b7-114">Кроме того, VBScript  не поддерживает новый синтаксис, используемый с помощью дим-Visual Basic для приложений. </span><span class="sxs-lookup"><span data-stu-id="ff5b7-114">Also, VBScript does not support the **New** syntax used with the **Dim** statement in Visual Basic for Applications.</span></span> <span data-ttu-id="ff5b7-115">Вместо этого необходимо использовать **вызов функции CreateObject:**</span><span class="sxs-lookup"><span data-stu-id="ff5b7-115">You must instead use the **CreateObject** function call:</span></span>

```vb 
 
Dim Rs1 
Set Rs1 = Server.CreateObject( "ADODB.Recordset" ) 
```

## <a name="vbscript-examples"></a><span data-ttu-id="ff5b7-116">Примеры VBScript</span><span class="sxs-lookup"><span data-stu-id="ff5b7-116">VBScript Examples</span></span>

<span data-ttu-id="ff5b7-117">Ниже приводится общий пример программирования сервера VBScript в файле Active Server Page (ASP):</span><span class="sxs-lookup"><span data-stu-id="ff5b7-117">The following code is a generic example of VBScript server-side programming in an Active Server Page (ASP) file:</span></span>

```vb 
 
<%  @LANGUAGE="VBSCRIPT" %> 
<%  Option Explicit %> 
<!--#include File="adovbs.inc"--> 
<HTML> 
    <BODY BGCOLOR="White" topmargin="10" leftmargin="10"> 
 
    <!-- Your ASP Code goes here --> 
<% 
Dim Source 
Dim Connect 
Dim Rs1 
     
Source = "SELECT * FROM Authors" 
Connect = "Provider=sqloledb;Data Source=srv;" & _ 
    "Initial Catalog=Pubs;Integrated Security=SSPI;" 
 
Set Rs1 = Server.CreateObject( "ADODB.Recordset" ) 
Rs1.Open Source, Connect, adOpenForwardOnly 
Response.Write("Success!") 
%> 
    </BODY> 
</HTML> 
```

<span data-ttu-id="ff5b7-118">Более конкретные примеры VBScript включены в документацию ADO.</span><span class="sxs-lookup"><span data-stu-id="ff5b7-118">More specific VBScript examples are included with the ADO documentation.</span></span> <span data-ttu-id="ff5b7-119">Дополнительные сведения см. в примерах кода ADO в [Microsoft Visual Basic Scripting Edition.](ado-code-examples-in-microsoft-visual-basic-scripting-edition.md)</span><span class="sxs-lookup"><span data-stu-id="ff5b7-119">For more information, see [ADO code examples in Microsoft Visual Basic Scripting Edition](ado-code-examples-in-microsoft-visual-basic-scripting-edition.md).</span></span>

## <a name="differences-between-vbscript-and-visual-basic"></a><span data-ttu-id="ff5b7-120">Различия между VBScript и Visual Basic</span><span class="sxs-lookup"><span data-stu-id="ff5b7-120">Differences Between VBScript and Visual Basic</span></span>

<span data-ttu-id="ff5b7-121">Использование ADO с VBScript аналогично использованию ADO с Visual Basic многими способами, включая использование синтаксиса.</span><span class="sxs-lookup"><span data-stu-id="ff5b7-121">Using ADO with VBScript is similar to using ADO with Visual Basic in many ways, including how syntax is used.</span></span> <span data-ttu-id="ff5b7-122">Однако существуют некоторые существенные различия:</span><span class="sxs-lookup"><span data-stu-id="ff5b7-122">However, some significant differences exist:</span></span>

- <span data-ttu-id="ff5b7-123">VBScript поддерживает только тип данных Variant, который может держать различные типы данных.</span><span class="sxs-lookup"><span data-stu-id="ff5b7-123">VBScript supports only the Variant data type, which can hold different types of data.</span></span> <span data-ttu-id="ff5b7-124">Вы можете хранить данные, необходимые в типе данных Variant, и данные будут функционировать надлежащим образом из-за литья, выполненного VBScript.</span><span class="sxs-lookup"><span data-stu-id="ff5b7-124">You can store the data you need in a Variant data type, and the data will function appropriately due to casting performed by VBScript.</span></span> <span data-ttu-id="ff5b7-125">Он распознает тип, необходимый ADO, и преобразует значение в варианте соответственно.</span><span class="sxs-lookup"><span data-stu-id="ff5b7-125">It recognizes the type required by ADO, and converts the value in the Variant accordingly.</span></span>

- <span data-ttu-id="ff5b7-126">Вы не можете использовать `on error goto <label>` в VBScript.</span><span class="sxs-lookup"><span data-stu-id="ff5b7-126">You cannot use `on error goto <label>` within VBScript.</span></span>

- <span data-ttu-id="ff5b7-127">VBScript поддерживает некоторые встроенные функции Visual Basic, такие как **Msgbox,** **Date** и **IsNumeric.**</span><span class="sxs-lookup"><span data-stu-id="ff5b7-127">VBScript supports some of the built-in Visual Basic functions such as **Msgbox**, **Date**, and **IsNumeric**.</span></span> <span data-ttu-id="ff5b7-128">Однако, поскольку VBScript — это подмножество Visual Basic, не все встроенные функции поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="ff5b7-128">However, because VBScript is a subset of Visual Basic, not all built-in functions are supported.</span></span> <span data-ttu-id="ff5b7-129">Например, VBScript не поддерживает функцию **Format** и функции I/O файла.</span><span class="sxs-lookup"><span data-stu-id="ff5b7-129">For example, VBScript does not support the **Format** function and the file I/O functions.</span></span>

