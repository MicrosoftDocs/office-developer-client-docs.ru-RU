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

Microsoft Visual Basic, Scripting Edition не поддерживает библиотеки типов, поэтому вам не нужно ссылаться на ADO в проекте. Следовательно, не поддерживаются связанные функции, такие как завершение командной строки. Кроме того, по умолчанию перечислимые константы ADO не определяются в VBScript.

Однако ADO предоставляет два включаемых файла, содержащие следующие определения для использования с VBScript:

  - Для серверного скрипта используйте Адовбс. Inc, установленный\\в\\\\\\\\ папке "общие файлы" системы c: Program Files по умолчанию.

  - Для клиентских скриптов используйте Адквбс. Inc, установленный в папке\\c: Program Files\\\\System\\мсдак\\ по умолчанию.

Вы можете копировать и вставлять определения констант из этих файлов на страницы ASP или, если вы выполняете сценарии на стороне сервера, скопируйте файл Адовбс. Inc в папку на веб-сайте и сослаться на нее со страницы ASP следующим образом:

```vb 
 
<!--#include File="adovbs.inc"--> 
```

## <a name="creating-ado-objects-in-vbscript"></a>Создание объектов ADO в VBScript

Оператор **Dim** нельзя использовать для назначения объектов определенному типу в VBScript. Кроме того, VBScript не поддерживает **Новый** синтаксис, используемый с оператором **Dim** в Visual Basic для приложений. Вместо этого необходимо использовать вызов функции **CreateObject** :

```vb 
 
Dim Rs1 
Set Rs1 = Server.CreateObject( "ADODB.Recordset" ) 
```

## <a name="vbscript-examples"></a>Примеры VBScript

Приведенный ниже код представляет собой общий пример программирования на стороне сервера VBScript в файле страницы ASP:

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

Более конкретные примеры VBScript включены в документацию по ADO. Для получения дополнительных сведений см. [примеры кода ADO в Microsoft Visual Basic scriptIng Edition](ado-code-examples-in-microsoft-visual-basic-scripting-edition.md).

## <a name="differences-between-vbscript-and-visual-basic"></a>Различия между VBScript и Visual Basic

Использование ADO с VBScript аналогично использованию ADO с Visual Basic множеством способов, в том числе с использованием синтаксиса. Однако существуют некоторые существенные отличия.

- VBScript поддерживает только тип данных Variant, который может содержать различные типы данных. Вы можете хранить нужные данные в типе данных Variant, и данные будут работать надлежащим образом из-за приведения, выполняемой с помощью VBScript. Он распознает тип, необходимый для ADO, и преобразует значение в соответствующем варианте.

- Нельзя использовать `on error goto <label>` в VBScript.

- VBScript поддерживает некоторые встроенные функции Visual Basic, такие как **MsgBox**, **Date**и **ISNUMERIC**. Однако так как VBScript является подмножеством Visual Basic, поддерживаются не все встроенные функции. Например, сценарий VBScript не поддерживает функцию **Format** и функции файлового ввода-вывода.

