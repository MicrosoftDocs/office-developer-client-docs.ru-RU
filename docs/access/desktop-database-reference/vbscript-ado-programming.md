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
# <a name="vbscript-ado-programming"></a>Программирование для ADO на VBScript


**Область применения**: Access 2013, Office 2013 

## <a name="creating-an-ado-project"></a>Создание ADO-Project

Microsoft Visual Basic, Scripting Edition не поддерживает библиотеки типов, поэтому вам не нужно ссылаться на ADO в проекте. Следовательно, не поддерживаются связанные функции, такие как завершение командной строки. Кроме того, по умолчанию в VBScript не определены константы ADO.

Тем не менее, ADO предоставляет вам два файла, содержащих следующие определения, которые будут использоваться с VBScript:

  - Для серверного скриптинга используйте Adovbs.inc, который устанавливается в папке ado c: \\ Program Files Common Files System по \\ \\ \\ \\ умолчанию.

  - Для клиентского скриптинга используйте Adcvbs.inc, который устанавливается в папке c: Program \\ Files Common Files System \\ \\ \\ msdac по \\ умолчанию.

Вы можете скопировать и вклеить постоянные определения из этих файлов на страницы ASP или, если вы работаете над сценарием на сервере, скопируйте файл Adovbs.inc в папку на веб-сайте и соположите его со страницы ASP:

```vb 
 
<!--#include File="adovbs.inc"--> 
```

## <a name="creating-ado-objects-in-vbscript"></a>Создание объектов ADO в VBScript

Для назначения объектов определенному типу в VBScript нельзя использовать заявление **Dim.** Кроме того, VBScript  не поддерживает новый синтаксис, используемый с помощью дим-Visual Basic для приложений.  Вместо этого необходимо использовать **вызов функции CreateObject:**

```vb 
 
Dim Rs1 
Set Rs1 = Server.CreateObject( "ADODB.Recordset" ) 
```

## <a name="vbscript-examples"></a>Примеры VBScript

Ниже приводится общий пример программирования сервера VBScript в файле Active Server Page (ASP):

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

Более конкретные примеры VBScript включены в документацию ADO. Дополнительные сведения см. в примерах кода ADO в [Microsoft Visual Basic Scripting Edition.](ado-code-examples-in-microsoft-visual-basic-scripting-edition.md)

## <a name="differences-between-vbscript-and-visual-basic"></a>Различия между VBScript и Visual Basic

Использование ADO с VBScript аналогично использованию ADO с Visual Basic многими способами, включая использование синтаксиса. Однако существуют некоторые существенные различия:

- VBScript поддерживает только тип данных Variant, который может держать различные типы данных. Вы можете хранить данные, необходимые в типе данных Variant, и данные будут функционировать надлежащим образом из-за литья, выполненного VBScript. Он распознает тип, необходимый ADO, и преобразует значение в варианте соответственно.

- Вы не можете использовать `on error goto <label>` в VBScript.

- VBScript поддерживает некоторые встроенные функции Visual Basic, такие как **Msgbox,** **Date** и **IsNumeric.** Однако, поскольку VBScript — это подмножество Visual Basic, не все встроенные функции поддерживаются. Например, VBScript не поддерживает функцию **Format** и функции I/O файла.

