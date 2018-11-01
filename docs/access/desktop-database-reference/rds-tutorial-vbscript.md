---
title: Руководство по RDS (VBScript)
TOCTitle: RDS Tutorial (VBScript)
ms:assetid: 7a6596fd-00b9-a637-7d00-fb55a621305f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249506(v=office.15)
ms:contentKeyID: 48545792
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 449a752d4ab9e1680a3cf318e73802d39d7033fb
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884204"
---
# <a name="rds-tutorial-vbscript"></a>Руководство по RDS (VBScript)


**Применимо к**: Access 2013, Office 2013

Это учебник служб удаленных рабочих СТОЛОВ, написанных на языке Visual Basic Scripting Edition. Описание назначения в этом руководстве в разделе [При помощи учебника по служб удаленных рабочих СТОЛОВ](chapter-12-rds-tutorial.md).

В этом руководстве [RDS. DataControl](datacontrol-object-rds.md) и [RDS. Пространства данных](dataspace-object-rds.md) создан во время разработки, то есть, определенные с помощью тегов объектов, следующим образом:. Кроме того они может быть создан во время выполнения с помощью метода **Server.CreateObject** . Например **RDS. DataControl** может быть создан следующим образом:

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

**Шаг 1 — Укажите программы сервера**

VBScript можно получить имя веб-сервера IIS, его, на котором выполняется с помощью метода VBScript **Request.ServerVariables** для страницы ASP:

```vb 
 
"https://<%=Request.ServerVariables("SERVER_NAME")%>" 
```

Тем не менее в этом руководстве используйте мнимой server «сервер».


> [!NOTE]
> <P>Обратите внимание на тип данных <STRONG>ByRef</STRONG> аргументов. VBScript не позволяет указать тип переменной, поэтому всегда необходимо передать переменную типа Variant. При использовании HTTP, служб удаленных рабочих СТОЛОВ можно передать переменную типа Variant в метод, требующей не тип Variant, если вызвать его с <STRONG>RDS. Пространства данных</STRONG> объекта метод <A href="createobject-method-rds.md">CreateObject</A> . При использовании DCOM или на сервере в процессе, соответствующие типы параметров на сторонах клиента и сервера или появится сообщение об ошибке «Несоответствие типов».</P>

```vb
 
Set DF1 = DS1.CreateObject("RDSServer.DataFactory", "https://yourServer") 
```

**Шаг 2a — вызова программы сервера с RDS. DataControl**

В этом примере — это просто комментарий, демонстрации поведения по умолчанию **RDS. DataControl** для выполнения указанного запроса.

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

**Этап 2б — вызова программы сервера с RDSServer.DataFactory**

**Шаг 3 — Сервер получает набор записей**

**Шаг 4 — Сервер возвращает набор записей**

```vb
 
Set RS = DF1.Query("DSN=Pubs;", "SELECT * FROM Authors") 
```

**Шаг 5 — DataControl осуществляется могут использоваться элементы управления visual**

```vb
 
' Assign the returned recordset to the DataControl. 
 
DC1.SourceRecordset = RS 
```

**Шаг 6a — изменения отправляются на сервер с RDS. DataControl**

В этом примере — это просто комментарий демонстрируется, как **RDS. DataControl** выполняет обновление.

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

**Шаг 6b — изменения отправляются на сервер с RDSServer.DataFactory**

```vb
 
DF.SubmitChanges"DSN=Pubs", RS 
 
End Sub 
</SCRIPT> 
</BODY> 
</HTML> 
```

**Это конце обучения.**

