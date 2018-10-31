---
title: Программирование для ADO на VBScript
TOCTitle: VBScript ADO Programming
ms:assetid: 24be1c70-8813-ed98-c3e5-fb33a68e7b41
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249019(v=office.15)
ms:contentKeyID: 48543764
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e94f4d313a9c43d08c9786c6f27fd49624709249
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863068"
---
# <a name="vbscript-ado-programming"></a><span data-ttu-id="ae298-102">Программирование для ADO на VBScript</span><span class="sxs-lookup"><span data-stu-id="ae298-102">VBScript ADO Programming</span></span>


<span data-ttu-id="ae298-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ae298-103">**Applies to**: Access 2013 | Office 2013</span></span> 

## <a name="creating-an-ado-project"></a><span data-ttu-id="ae298-104">Создание проекта ADO</span><span class="sxs-lookup"><span data-stu-id="ae298-104">Creating an ADO Project</span></span>

<span data-ttu-id="ae298-105">Microsoft Visual Basic, Scripting Edition не поддерживает библиотеки типов, поэтому не нужно ссылке ADO в проекте.</span><span class="sxs-lookup"><span data-stu-id="ae298-105">Microsoft Visual Basic, Scripting Edition does not support type libraries, so you do not need to reference ADO in your project.</span></span> <span data-ttu-id="ae298-106">Следовательно не связанные функции, например завершения командной строки, поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="ae298-106">Consequently, no associated features such as command line completion are supported.</span></span> <span data-ttu-id="ae298-107">Кроме того по умолчанию, ADO перечисленных констант не определены в VBScript.</span><span class="sxs-lookup"><span data-stu-id="ae298-107">Also, by default, ADO enumerated constants are not defined in VBScript.</span></span>

<span data-ttu-id="ae298-108">Тем не менее ADO предоставляет вам с двумя включают файлы, содержащие следующие определения, который будет использоваться с VBScript:</span><span class="sxs-lookup"><span data-stu-id="ae298-108">However, ADO provides you with two include files containing the following definitions to be used with VBScript:</span></span>

  - <span data-ttu-id="ae298-109">Для использования на сервере сценариев Adovbs.inc, которая устанавливается в c:\\Program Files\\общие файлы\\системы\\ado\\ папки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ae298-109">For server-side scripting use Adovbs.inc, which is installed in the c:\\Program Files\\Common Files\\System\\ado\\ folder by default.</span></span>

  - <span data-ttu-id="ae298-110">Для использования сценариев на стороне клиента Adcvbs.inc, которая устанавливается в c:\\Program Files\\общие файлы\\системы\\msdac\\ папки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ae298-110">For client-side scripting use Adcvbs.inc, which is installed in the c:\\Program Files\\Common Files\\System\\msdac\\ folder by default.</span></span>

<span data-ttu-id="ae298-111">Можно скопировать и вставить определения констант из этих файлов в страницы ASP или, при выполнении сценариев на стороне сервера, скопируйте файл Adovbs.inc в папку на веб-сайта и создание ссылок на со страницы ASP следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ae298-111">You can either copy and paste constant definitions from these files into your ASP pages, or, if you are doing server-side scripting, copy Adovbs.inc file to a folder on your website and referencing it from your ASP page like this:</span></span>

```vb 
 
<!--#include File="adovbs.inc"--> 
```

## <a name="creating-ado-objects-in-vbscript"></a><span data-ttu-id="ae298-112">Создание объектов ADO в VBScript</span><span class="sxs-lookup"><span data-stu-id="ae298-112">Creating ADO Objects in VBScript</span></span>

<span data-ttu-id="ae298-113">Этот оператор **Dim** нельзя использовать для назначения объекты для конкретного типа в VBScript.</span><span class="sxs-lookup"><span data-stu-id="ae298-113">You cannot use the **Dim** statement to assign objects to a specific type in VBScript.</span></span> <span data-ttu-id="ae298-114">Кроме того VBScript не поддерживает синтаксис **Создать** с помощью оператора **Dim** в Visual Basic для приложений.</span><span class="sxs-lookup"><span data-stu-id="ae298-114">Also, VBScript does not support the **New** syntax used with the **Dim** statement in Visual Basic for Applications.</span></span> <span data-ttu-id="ae298-115">Необходимо использовать вместо этого вызов функции **CreateObject** :</span><span class="sxs-lookup"><span data-stu-id="ae298-115">You must instead use the **CreateObject** function call:</span></span>

```vb 
 
Dim Rs1 
Set Rs1 = Server.CreateObject( "ADODB.Recordset" ) 
```

## <a name="vbscript-examples"></a><span data-ttu-id="ae298-116">Примеры VBScript</span><span class="sxs-lookup"><span data-stu-id="ae298-116">VBScript Examples</span></span>

<span data-ttu-id="ae298-117">Ниже показан общий пример программирования на сервере VBScript в файле страницы ASP (Active Server):</span><span class="sxs-lookup"><span data-stu-id="ae298-117">The following code is a generic example of VBScript server-side programming in an Active Server Page (ASP) file:</span></span>

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

<span data-ttu-id="ae298-118">В документации по ADO включены более конкретные примеры VBScript.</span><span class="sxs-lookup"><span data-stu-id="ae298-118">More specific VBScript examples are included with the ADO documentation.</span></span> <span data-ttu-id="ae298-119">Для получения дополнительных сведений см [ADO примеры кода на языках Microsoft Visual Basic Scripting Edition](ado-code-examples-in-microsoft-visual-basic-scripting-edition.md).</span><span class="sxs-lookup"><span data-stu-id="ae298-119">For more information, see [ADO code examples in Microsoft Visual Basic Scripting Edition](ado-code-examples-in-microsoft-visual-basic-scripting-edition.md).</span></span>

## <a name="differences-between-vbscript-and-visual-basic"></a><span data-ttu-id="ae298-120">Различия между VBScript и Visual Basic</span><span class="sxs-lookup"><span data-stu-id="ae298-120">Differences Between VBScript and Visual Basic</span></span>

<span data-ttu-id="ae298-121">Использование ADO с VBScript аналогично работе с ADO с помощью Visual Basic несколькими способами, в том числе об использовании синтаксиса.</span><span class="sxs-lookup"><span data-stu-id="ae298-121">Using ADO with VBScript is similar to using ADO with Visual Basic in many ways, including how syntax is used.</span></span> <span data-ttu-id="ae298-122">Тем не менее существуют значительные различия:</span><span class="sxs-lookup"><span data-stu-id="ae298-122">However, some significant differences exist:</span></span>

- <span data-ttu-id="ae298-123">VBScript поддерживает только Variant тип данных, который может содержать различные типы данных.</span><span class="sxs-lookup"><span data-stu-id="ae298-123">VBScript supports only the Variant data type, which can hold different types of data.</span></span> <span data-ttu-id="ae298-124">Можно хранить необходимых данных в тип данных Variant и данных будет работать неправильно, из-за приведения, выполняемой VBScript.</span><span class="sxs-lookup"><span data-stu-id="ae298-124">You can store the data you need in a Variant data type, and the data will function appropriately due to casting performed by VBScript.</span></span> <span data-ttu-id="ae298-125">Определяет тип, необходимые для ADO и соответствующим образом преобразует значение в тип Variant.</span><span class="sxs-lookup"><span data-stu-id="ae298-125">It recognizes the type required by ADO, and converts the value in the Variant accordingly.</span></span>

- <span data-ttu-id="ae298-126">Нельзя использовать `on error goto <label>` в рамках VBScript.</span><span class="sxs-lookup"><span data-stu-id="ae298-126">You cannot use `on error goto <label>` within VBScript.</span></span>

- <span data-ttu-id="ae298-127">VBScript поддерживает некоторые из встроенных функций Visual Basic, такие как **Msgbox**, **Дата**и **IsNumeric**.</span><span class="sxs-lookup"><span data-stu-id="ae298-127">VBScript supports some of the built-in Visual Basic functions such as **Msgbox**, **Date**, and **IsNumeric**.</span></span> <span data-ttu-id="ae298-128">Тем не менее поскольку VBScript подмножество Visual Basic, поддерживаются не всех встроенных функций.</span><span class="sxs-lookup"><span data-stu-id="ae298-128">However, because VBScript is a subset of Visual Basic, not all built-in functions are supported.</span></span> <span data-ttu-id="ae298-129">Например VBScript не поддерживает функции **Format** и функций операций ввода-вывода файла.</span><span class="sxs-lookup"><span data-stu-id="ae298-129">For example, VBScript does not support the **Format** function and the file I/O functions.</span></span>

