---
title: 'Глава 12: Учебник удаленной службы данных (RDS)'
TOCTitle: 'Chapter 12: RDS tutorial'
ms:assetid: fa44a5e8-e4df-dfdd-d7a1-a870ec3cabdd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250277(v=office.15)
ms:contentKeyID: 48548837
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fb29fd070a693b608cede1d21329b3749c18e852
ms.sourcegitcommit: 007141520d6479860f452371532f9267f33eb260
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25999503"
---
# <a name="chapter-12-remote-data-service-rds-tutorial"></a>Глава 12: Учебник удаленной службы данных (RDS)

**Применимо к**: Access 2013, Office 2013

В этом руководстве описывается использование модели программирования служб удаленных рабочих СТОЛОВ для запроса и обновления в источнике данных. Во-первых описываются действия, необходимые для выполнения этой задачи. Затем учебника по повторяется в Microsoft Visual Basic Scripting Edition и Microsoft Visual J ++, продолжительностью ADO для Windows классов (ADO/WFC).

В этом руководстве закодированные на разных языках по двум причинам:

- В документации для служб удаленных рабочих СТОЛОВ предполагается коды чтения в Visual Basic. Это делает документации удобным для программистов Visual Basic, но меньше полезен для программистов, использовать другие языки.

- Если вы не уверены в определенный компонент служб удаленных рабочих СТОЛОВ и вам известно немного из другой язык, может иметь возможность сопоставлять вопрос, используя для одного компонента выразить на другом языке.

В этом руководстве основано на модели программирования служб удаленных рабочих СТОЛОВ. По отдельности рассматривается каждый шаг модели программирования. Кроме того показан фрагмент кода Visual Basic по каждому шагу.

В примере кода повторяется на других языках с минимальными обсуждений. Каждый шаг в учебном курсе заданного языка программирования в модель программирования и описания при помощи учебника по помечен соответствующие действия. Используйте номер шага для ссылки на обсуждения в описательное учебном курсе.

Модель программирования служб удаленных рабочих СТОЛОВ указанное ниже. Используйте его в качестве руководства, как во время выполнения учебника по.

### <a name="rds-programming-model-with-objects"></a>Модель программирования служб удаленных рабочих СТОЛОВ с объектами

- Укажите программу для вызова на сервере и получить способом (прокси-сервер), обратитесь к нему из клиента.

- Вызов программы сервера. Передайте параметры программы сервера, которое идентифицирует источник данных и команды для выдачи.

- Программы сервера получает объект [набора записей](recordset-object-ado.md) из источника данных, обычно с помощью ADO. Кроме того в объект **набора записей** обрабатывается на сервере.

- Программы сервера возвращает окончательный объекта **набора записей** для клиентского приложения.

- В клиенте объекта **набора записей** при необходимости поместите в форму, можно легко использовать визуальные элементы управления.

- Изменения в объект **набора записей** отправляются на сервер и используется для обновления источника данных.

## <a name="step-1-specify-a-server-program"></a>Шаг 1: Укажите программы сервера

В общем случае используйте [RDS. Пространства данных](dataspace-object-rds.md) объекта метод [CreateObject](createobject-method-rds.md) , чтобы указать программы сервера по умолчанию, [RDSServer.DataFactory](datafactory-object-rdsserver.md)или собственную программу настраиваемый серверный (бизнес-объект). Программа сервера создается на сервере и ссылку на программу сервера или *прокси-сервера*, возвращается.

В этом руководстве использует программы сервера по умолчанию:

```vb 
 
Sub RDSTutorial1() 
 Dim DS as New RDS.DataSpace 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
... 
``` 

## <a name="step-2-invoke-the-server-program"></a>Шаг 2: Вызова программы сервера 

При вызове метода для клиента *прокси-сервера*, самой программы на сервере выполняется метод. На этом этапе будет выполнить запрос на сервере.

### <a name="part-a"></a>Часть "A"

Если не были [RDSServer.DataFactory](datafactory-object-rdsserver.md) в этом руководстве, самый удобный способ выполните этот шаг будет использовать [RDS. DataControl](datacontrol-object-rds.md) объекта. **RDS. DataControl** объединяет предыдущие действия по созданию прокси-сервер, с помощью этот шаг, выполнение запроса.

1. Установка **RDS. DataControl** объекта свойства [сервера](server-property-rds.md) для идентификации, где следует создать экземпляр программы сервера.

2. Присвойте свойству [подключение](connect-property-rds.md) для указания строки подключения для доступа к источнику данных.

3. Присвойте свойству [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) для указания текст команды запроса. 

4. Выдача метод [Refresh](refresh-method-rds.md) , чтобы программа server для подключения к источнику данных, извлечение строк, указанным в запросе и возврата объекта **набора записей** для клиента.

В этом руководстве не использует **RDS. DataControl**, но это, как она будет выглядеть при как:

```vb 
 
Sub RDSTutorial2A() 
 Dim DC as New RDS.DataControl 
 DC.Server = "https://yourServer" 
 DC.Connect = "DSN=Pubs" 
 DC.SQL = "SELECT * FROM Authors" 
 DC.Refresh 
... 
```

<br/>

Ни учебника по вызов служб удаленных рабочих СТОЛОВ с объектами ADO, но это, как она будет выглядеть при как:

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "SELECT * FROM Authors","Provider=MS Remote;Data Source=Pubs;" & _ 
"Remote Server=https://yourServer;Remote Provider=SQLOLEDB;" 
```

### <a name="part-b"></a>Часть "B"

Общий метод выполнения этого этапа — это для вызова метода [Query](query-method-rds.md) объекта **RDSServer.DataFactory** . Этот метод принимает строку подключения, которая используется для подключения к источнику данных, и текст команды, который используется для указания строк, возвращаемых из источника данных.

В этом руководстве использует объект **DataFactory** метод **запроса** :

```vb 
 
Sub RDSTutorial2B() 
 Dim DS as New RDS.DataSpace 
 Dim DF 
 Dim RS as ADODB.Recordset 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
... 
```

## <a name="step-3-server-obtains-a-recordset"></a>Шаг 3: Сервер получает набор записей 

Программа сервера использует текст строки и команду подключение для запроса источника данных для нужного строк. ADO обычно используется для получения этого **набора записей**, несмотря на то, что другие данные Microsoft доступ к интерфейсы, такие как OLE DB, можно было бы использовать.

Настраиваемый серверный программы может выглядеть следующим образом:

```vb 
 
Public Function ServerProgram(cn as String, qry as String) as Object 
Dim rs as New ADODB.Recordset 
 rs.CursorLocation = adUseClient 
 rs.Open qry, cn 
 rs.ActiveConnection = Nothing 
 Set ServerProgram = rs 
End Function 
```

## <a name="step-4-server-returns-the-recordset"></a>Шаг 4: Сервер возвращает набор записей 

Служб удаленных рабочих СТОЛОВ преобразует полученного объекта **набора записей** в форме, могут быть отправлены клиенту (то есть, оно *выполняет маршалинг* **набора записей**). Точное преобразование и способ отправки зависит ли сервера в Интернете или интрасети, локальной сети, или является библиотекой динамической компоновки. Тем не менее в этом сведений не является обязательным; все, что имеет значение, служб удаленных рабочих СТОЛОВ отправляет **записей** клиенту.

На стороне клиента объекта **набора записей** возвращается и присваивается локальной переменной.

```vb 
 
Sub RDSTutorial4() 
 Dim DS as New RDS.DataSpace 
 Dim RS as ADODB.Recordset 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query("DSN=Pubs", "SELECT * FROM Authors") 
... 
```

## <a name="step-5-datacontrol-is-made-usable"></a>Шаг 5: DataControl сделано могут использоваться 

Возвращаемый объект **набора записей** доступна для использования. Можно проверить, перейдите или измените его так, как и любой другой **набора записей**. Что можно сделать с помощью **набора записей** зависит от среды. Visual Basic и Visual C++ имеют визуальные элементы управления, которые могут использовать **записей** прямо или косвенно с помощью Включение управления данными.

Например при отображении веб-страницы в браузере Internet Explorer, может потребоваться отображение данных объекта **набора записей** в элементе управления visual. Визуальные элементы управления на веб-странице не может получить доступ к объекта **набора записей** напрямую. Тем не менее они могут доступ к объекту **набора записей** с [RDS. DataControl](datacontrol-object-rds.md). **RDS. DataControl** становится могут использоваться с помощью визуального элемента управления, если свойство [SourceRecordset](recordset-sourcerecordset-properties-rds.md) имеет значение в объект **набора записей** .

Элемент управления visual объект должен иметь значение **RDS. параметра **DATASRC** DataControl**и его свойства **DATAFLD** поля объекта **набора записей** (столбца).

В этом руководстве задайте для свойства **SourceRecordset** :

```vb 
 
Sub RDSTutorial5() 
 Dim DS as New RDS.DataSpace 
 Dim RS as ADODB.Recordset 
 Dim DC as New RDS.DataControl 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
 DC.SourceRecordset = RS ' Visual controls can now bind to DC. 
... 
```

## <a name="step-6-changes-are-sent-to-the-server"></a>Шаг 6: Изменения отправляются на сервер

При редактировании объекта **набора записей** (строк, которые будут добавлены, изменены или удалены) изменения можно отправить на сервер.

Поведение по умолчанию служб удаленных рабочих СТОЛОВ можно вызвать неявно с объекты ADO и поставщик удаленного взаимодействия Microsoft OLE DB. Запросы могут возвращать **наборов записей**и измененного **наборов записей** можно обновить источник данных. В этом руководстве не вызывает служб удаленных рабочих СТОЛОВ с объектами ADO, но это, как она будет выглядеть при как:

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "SELECT * FROM Authors","Provider=MS Remote;Data Source=Pubs;" & _ 
 "Remote Server=https://yourServer;Remote Provider=SQLOLEDB;" 
... ' Edit the Recordset. 
rs.UpdateBatch ' The equivalent of SubmitChanges. 
... 
```

### <a name="part-a"></a>Часть "A"

Предположим, в этом случае только использовали [RDS. DataControl](datacontrol-object-rds.md) , а теперь — объект **набора записей** , связанных с **RDS. DataControl**. Метод [SubmitChanges](submitchanges-method-rds.md) обновляет источник данных все изменения в объект **набора записей** Если свойства [сервера](server-property-rds.md) и [подключение](connect-property-rds.md) по-прежнему.

```vb 
 
Sub RDSTutorial6A() 
Dim DC as New RDS.DataControl 
Dim RS as ADODB.Recordset 
DC.Server = "https://yourServer" 
DC.Connect = "DSN=Pubs" 
DC.SQL = "SELECT * FROM Authors" 
DC.Refresh 
... 
Set RS = DC.Recordset 
 ' Edit the Recordset. 
... 
DC.SubmitChanges 
... 
```

### <a name="part-b"></a>Часть "B"

Кроме того может обновить сервер с объектом [RDSServer.DataFactory](datafactory-object-rdsserver.md) определения подключения и объект **набора записей** .

```vb 
 
Sub RDSTutorial6B() 
Dim DS As New RDS.DataSpace 
Dim RS As ADODB.Recordset 
Dim DC As New RDS.DataControl 
Dim DF As Object 
Dim blnStatus As Boolean 
Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
DC.SourceRecordset = RS ' Visual controls can now bind to DC. 
 ' Edit the Recordset. 
blnStatus = DF.SubmitChanges "DSN=Pubs", RS 
End Sub 
```


## <a name="appendix-a-rds-tutorial-vbscript"></a>Приложение а учебника по служб удаленных рабочих СТОЛОВ (VBScript)

Это учебник служб удаленных рабочих СТОЛОВ, написанных на языке Visual Basic Scripting Edition. Описание назначения в этом руководстве см в этом разделе.

В этом руководстве [RDS. DataControl](datacontrol-object-rds.md) и [RDS. Пространства данных](dataspace-object-rds.md) создан во время разработки; то есть они определены с помощью тегов объектов. Кроме того они может быть создан во время выполнения с помощью метода **Server.CreateObject** . 

Например **RDS. DataControl** может быть создан следующим образом:

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

### <a name="step-1-specify-a-server-program"></a>Шаг 1: Укажите программы сервера

VBScript можно получить имя веб-сервера IIS, его, на котором выполняется с помощью метода VBScript **Request.ServerVariables** для страницы ASP:

```vb 
 
"https://<%=Request.ServerVariables("SERVER_NAME")%>" 
```

Тем не менее в этом руководстве используйте мнимой server «сервер».

> [!NOTE]
> Обратите внимание на тип данных **ByRef** аргументов. VBScript не позволяет указать тип переменной, поэтому всегда необходимо передать переменную типа Variant. При использовании HTTP, служб удаленных рабочих СТОЛОВ можно передать переменную типа Variant в метод, требующей не тип Variant, если вызвать его с **RDS. Пространства данных** объекта метод [CreateObject](createobject-method-rds.md) . При использовании DCOM или на сервере в процессе, соответствующие типы параметров на сторонах клиента и сервера или появится сообщение об ошибке «Несоответствие типов».

```vb
 
Set DF1 = DS1.CreateObject("RDSServer.DataFactory", "https://yourServer") 
```

### <a name="step-2-part-a-invoke-the-server-program-with-rdsdatacontrol"></a>Шаг 2, вызов ответ: часть программы сервера с RDS. DataControl

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

Перейдите к следующему шагу.

### <a name="step-4-server-returns-the-recordset"></a>Шаг 4: Сервер возвращает набор записей

```vb
 
Set RS = DF1.Query("DSN=Pubs;", "SELECT * FROM Authors") 
```

### <a name="step-5-datacontrol-is-made-usable-by-visual-controls"></a>Шаг 5: DataControl осуществляется могут использоваться элементы управления visual

```vb
 
' Assign the returned recordset to the DataControl. 
 
DC1.SourceRecordset = RS 
```

### <a name="step-6-part-a-changes-are-sent-to-the-server-with-rdsdatacontrol"></a>Шаг 6, часть A: изменения отправляются на сервер с RDS. DataControl

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

### <a name="step-6-part-b-changes-are-sent-to-the-server-with-rdsserverdatafactory"></a>Шаг 6, часть B: изменения отправляются на сервер с RDSServer.DataFactory

```vb
 
DF.SubmitChanges"DSN=Pubs", RS 
 
End Sub 
</SCRIPT> 
</BODY> 
</HTML> 
```

## <a name="appendix-b-rds-tutorial-visual-j"></a>Приложение б. служб удаленных рабочих СТОЛОВ при помощи учебника по (Visual J ++)

ADO/WFC не соответствующего полностью объектной модели служб удаленных рабочих СТОЛОВ, то есть не реализует [RDS. DataControl](datacontrol-object-rds.md) объекта. ADO/WFC только реализует класс со стороны клиента, [RDS. Пространства данных](dataspace-object-rds.md).

Класс **пространства данных** реализует один метод [CreateObject](createobject-method-rds.md), которое возвращает объект [ObjectProxy](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/objectproxy-ado-wfc-syntax) . Класс **пространства данных** также внедряет свойство [InternetTimeout](internettimeout-property-rds.md) .

Класс **ObjectProxy** реализует один метод, позвонить, которой можно было вызвать любой объект бизнеса на сервере.

```java 
 
import com.ms.wfc.data.*; 
public class RDSTutorial 
{ 
 public void tutorial() 
 { 
// Step 1: Specify a server program. 
 ObjectProxy obj = 
 DataSpace.createObject( 
 "RDSServer.DataFactory", 
 "https://YourServer"); 
 
// Step 2: Server returns a Recordset. 
 Recordset rs = (Recordset) obj.call( 
 "Query", 
 new Object[] {"DSN=Pubs;", "SELECT * FROM Authors"}); 
 
// Step 3: Changes are sent to the server. 
 ... // Edit Recordset. 
 obj.call( 
 "SubmitChanges", 
 new Object[] {"DSN=Pubs;", rs}); 
 return; 
 } 
} 
```



