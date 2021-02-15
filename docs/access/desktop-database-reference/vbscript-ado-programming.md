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

## <a name="creating-an-ado-project"></a>Создание проекта ADO

Microsoft Visual Basic Scripting Edition не поддерживает библиотеки типов, поэтому нет необходимости ссылаться на ADO в проекте. Следовательно, связанные функции, такие как завершение командной строки, не поддерживаются. Кроме того, по умолчанию в VBScript не определены константы из индекса ADO.

Однако ADO предоставляет два файла, содержащих следующие определения, которые будут использоваться с VBScript:

  - Для сценариев на стороне сервера используйте Adovbs.inc, установленный в папке c: \\ Program Files Common Files System \\ \\ \\ ado \\ folder by default.

  - Для клиентских сценариев используйте файл Adcvbs.inc, установленный в папке \\ msdac program Files Common Files System по \\ \\ \\ \\ умолчанию.

Вы можете скопировать и вложить определения констант из этих файлов на страницы ASP или, если вы работаете с серверными сценариями, скопировать файл Adovbs.inc в папку на вашем веб-сайте и сослаться на него со страницы ASP, как по этому:

```vb 
 
<!--#include File="adovbs.inc"--> 
```

## <a name="creating-ado-objects-in-vbscript"></a>Создание объектов ADO в VBScript

Для назначения объектов определенному типу в VBScript нельзя использовать утверждение **Dim.** Кроме того, VBScript  не поддерживает новый синтаксис, используемый с помощью заявления **Dim** в Visual Basic для приложений. Вместо этого необходимо использовать вызов **функции CreateObject:**

```vb 
 
Dim Rs1 
Set Rs1 = Server.CreateObject( "ADODB.Recordset" ) 
```

## <a name="vbscript-examples"></a>Примеры VBScript

Следующий код является универсальным примером программирования на стороне сервера VBScript в ASP-файле:

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

Использование ADO с VBScript аналогично использованию ADO с Visual Basic множеством способов, включая использование синтаксиса. Однако существуют некоторые существенные различия:

- VBScript поддерживает только тип данных Variant, который может поддерживать различные типы данных. Необходимые данные можно хранить в типе данных Variant, и эти данные будут работать надлежащим образом из-за выполнения VBScript приведите данные. Он распознает тип, необходимый для ADO, и преобразует значение в Variant соответствующим образом.

- В `on error goto <label>` VBScript нельзя использовать.

- VBScript поддерживает некоторые встроенные функции Visual Basic, такие как **Msgbox,** **Date** и **IsNumeric.** Однако поскольку VBScript является подмножество Visual Basic, поддерживаются не все встроенные функции. Например, VBScript не поддерживает **функции Format** и функции I/O файла.

