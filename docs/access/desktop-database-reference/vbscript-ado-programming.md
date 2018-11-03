---
title: Программирование для ADO на VBScript
TOCTitle: VBScript ADO Programming
ms:assetid: 24be1c70-8813-ed98-c3e5-fb33a68e7b41
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249019(v=office.15)
ms:contentKeyID: 48543764
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 694580005a3d016448ea9e5e715fea236a1d93f5
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944867"
---
# <a name="vbscript-ado-programming"></a>Программирование VBScript ADO


**Применимо к**: Access 2013, Office 2013 

## <a name="creating-an-ado-project"></a>Создание проекта ADO

Microsoft Visual Basic, Scripting Edition не поддерживает библиотеки типов, поэтому не нужно ссылке ADO в проекте. Следовательно не связанные функции, например завершения командной строки, поддерживаются. Кроме того по умолчанию, ADO перечисленных констант не определены в VBScript.

Тем не менее ADO предоставляет вам с двумя включают файлы, содержащие следующие определения, который будет использоваться с VBScript:

  - Для использования на сервере сценариев Adovbs.inc, которая устанавливается в c:\\Program Files\\общие файлы\\системы\\ado\\ папки по умолчанию.

  - Для использования сценариев на стороне клиента Adcvbs.inc, которая устанавливается в c:\\Program Files\\общие файлы\\системы\\msdac\\ папки по умолчанию.

Можно скопировать и вставить определения констант из этих файлов в страницы ASP или, при выполнении сценариев на стороне сервера, скопируйте файл Adovbs.inc в папку на веб-сайта и создание ссылок на со страницы ASP следующим образом:

```vb 
 
<!--#include File="adovbs.inc"--> 
```

## <a name="creating-ado-objects-in-vbscript"></a>Создание объектов ADO в VBScript

Этот оператор **Dim** нельзя использовать для назначения объекты для конкретного типа в VBScript. Кроме того VBScript не поддерживает синтаксис **Создать** с помощью оператора **Dim** в Visual Basic для приложений. Необходимо использовать вместо этого вызов функции **CreateObject** :

```vb 
 
Dim Rs1 
Set Rs1 = Server.CreateObject( "ADODB.Recordset" ) 
```

## <a name="vbscript-examples"></a>Примеры VBScript

Ниже показан общий пример программирования на сервере VBScript в файле страницы ASP (Active Server):

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

В документации по ADO включены более конкретные примеры VBScript. Для получения дополнительных сведений см [ADO примеры кода на языках Microsoft Visual Basic Scripting Edition](ado-code-examples-in-microsoft-visual-basic-scripting-edition.md).

## <a name="differences-between-vbscript-and-visual-basic"></a>Различия между VBScript и Visual Basic

Использование ADO с VBScript аналогично работе с ADO с помощью Visual Basic несколькими способами, в том числе об использовании синтаксиса. Тем не менее существуют значительные различия:

- VBScript поддерживает только Variant тип данных, который может содержать различные типы данных. Можно хранить необходимых данных в тип данных Variant и данных будет работать неправильно, из-за приведения, выполняемой VBScript. Определяет тип, необходимые для ADO и соответствующим образом преобразует значение в тип Variant.

- Нельзя использовать `on error goto <label>` в рамках VBScript.

- VBScript поддерживает некоторые из встроенных функций Visual Basic, такие как **Msgbox**, **Дата**и **IsNumeric**. Тем не менее поскольку VBScript подмножество Visual Basic, поддерживаются не всех встроенных функций. Например VBScript не поддерживает функции **Format** и функций операций ввода-вывода файла.

