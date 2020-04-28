---
title: 'Глава 12: руководство по удаленным службам данных (RDS)'
TOCTitle: 'Chapter 12: RDS tutorial'
ms:assetid: fa44a5e8-e4df-dfdd-d7a1-a870ec3cabdd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250277(v=office.15)
ms:contentKeyID: 48548837
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aca77ac08688e643327bdbf229ab6c1dec40d109
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296481"
---
# <a name="chapter-12-remote-data-service-rds-tutorial"></a>Глава 12: руководство по удаленным службам данных (RDS)

**Область применения**: Access 2013, Office 2013

В этом руководстве показано, как использовать модель программирования RDS для запроса и обновления источника данных. Сначала он описывает действия, необходимые для выполнения этой задачи. После этого руководство повторяется в Microsoft Visual Basic Scripting Edition и Microsoft Visual J++, на которых можно использовать классы ADO для Windows Foundation (ADO/WFC).

Это руководство запрограммировано на разных языках по двум причинам:

- Документация для RDS предполагает, что коды средства чтения в Visual Basic. Это делает документацию удобной для программистов Visual Basic, но не менее полезна для программистов, использующих другие языки.

- Если вы не уверены в определенном компоненте RDS и вы знаете немного другого языка, вы можете разрешить свой вопрос, выполнив поиск того же компонента, представленного на другом языке.

Это руководство основано на модели программирования RDS. Здесь обсуждается каждый шаг модели программирования по отдельности. Кроме того, он иллюстрирует каждый шаг с фрагментом кода Visual Basic.

Пример кода повторяется на других языках с минимальным обсуждением. Каждый шаг в данном руководстве по языку программирования отмечен соответствующими шагами в модели программирования и в описательном руководстве. Используйте номер шага, чтобы сослаться на обсуждение в подробном руководстве.

Ниже приведен пример модели программирования RDS. Используйте его в качестве схемы, когда вы пройдете в руководстве.

### <a name="rds-programming-model-with-objects"></a>Модель программирования RDS с объектами

- Укажите программу, которая будет вызываться на сервере, и получите способ (прокси) для ссылки на него из клиента.

- Вызов серверной программы. Передайте параметры в серверную программу, определяющую источник данных, и команду, которая будет выдаваться.

- Серверная программа получает объект [Recordset](recordset-object-ado.md) из источника данных, как правило, с помощью ADO. При необходимости объект **Recordset** обрабатывается на сервере.

- Серверная программа возвращает конечный объект **Recordset** клиентскому приложению.

- В клиенте объект **Recordset** можно дополнительно поместить в форму, которая может быть легко использоваться визуальными элементами управления.

- Изменения объекта **Recordset** отправляются обратно на сервер и используются для обновления источника данных.

## <a name="step-1-specify-a-server-program"></a>Шаг 1: указание серверной программы

В общем случае используйте [RDS. ](dataspace-object-rds.md)Метод [CreateObject](createobject-method-rds.md) объекта Space для указания программы сервера по умолчанию, [рдссервер.](datafactory-object-rdsserver.md)DataObject или собственной настраиваемой серверной программы (бизнес-объект). На сервере создается экземпляр серверной программы, а также возвращается ссылка на программу или *прокси-* сервер.

В этом руководстве используется серверная программа по умолчанию:

```vb 
 
Sub RDSTutorial1() 
 Dim DS as New RDS.DataSpace 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
... 
``` 

## <a name="step-2-invoke-the-server-program"></a>Шаг 2: вызов серверной программы 

При вызове метода на клиентском *прокси*фактическая программа на сервере выполняет метод. На этом этапе вы выполняете запрос на сервере.

### <a name="part-a"></a>Часть A

Если вы не использовали [рдссервер.](datafactory-object-rdsserver.md) в этом руководстве, самый удобный способ выполнения этого действия — использование [RDS. Объект управления](datacontrol-object-rds.md) DataObject. **RDS. Элемент управления** данными объединяет предыдущий этап создания прокси-сервера с помощью этого шага, выдавая запрос.

1. Задайте для **RDS. **Свойство [сервера](server-property-rds.md) объектов DataObject для определения места создания экземпляра программы сервера.

2. Задайте свойство [Connect](connect-property-rds.md) , чтобы указать строку подключения для доступа к источнику данных.

3. Задайте свойство [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) , чтобы указать текст команды запроса. 

4. Выдайте метод [Refresh](refresh-method-rds.md) для подключения программы сервера к источнику данных, получения строк, указанных запросом, и возврата объекта **Recordset** клиенту.

В этом руководстве не используется **RDS. Элемент управления**данным, но это будет выглядеть, как показано ниже:

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

Кроме того, не вызывайте группу RDS с объектами ADO, но вот как она будет выглядеть:

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "SELECT * FROM Authors","Provider=MS Remote;Data Source=Pubs;" & _ 
"Remote Server=https://yourServer;Remote Provider=SQLOLEDB;" 
```

### <a name="part-b"></a>Часть B

Общий метод выполнения этого действия — вызов метода [запроса](query-method-rds.md) **рдссервер.** DataObject. Этот метод принимает строку подключения, используемую для подключения к источнику данных, и текст команды, который используется для указания строк, возвращаемых из источника данных.

**В этом** руководстве используется метод **запроса** объектов DataObject.

```vb 
 
Sub RDSTutorial2B() 
 Dim DS as New RDS.DataSpace 
 Dim DF 
 Dim RS as ADODB.Recordset 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
... 
```

## <a name="step-3-server-obtains-a-recordset"></a>Шаг 3: сервер получает объект Recordset 

Серверная программа использует строку подключения и текст команды, чтобы запросить нужные строки в источнике данных. ADO обычно используется для извлечения этого объекта **Recordset**, хотя можно использовать другие интерфейсы доступа к данным Майкрософт, такие как OLE DB.

Пользовательская серверная программа может выглядеть следующим образом:

```vb 
 
Public Function ServerProgram(cn as String, qry as String) as Object 
Dim rs as New ADODB.Recordset 
 rs.CursorLocation = adUseClient 
 rs.Open qry, cn 
 rs.ActiveConnection = Nothing 
 Set ServerProgram = rs 
End Function 
```

## <a name="step-4-server-returns-the-recordset"></a>Шаг 4: сервер возвращает объект Recordset 

RDS преобразует полученный объект **Recordset** в форму, которая может быть отправлена обратно клиенту (то есть, *маршалирует* объект **Recordset**). Точная форма преобразования и способ его отправки зависит от того, находится ли сервер в Интернете или интрасети, в локальной сети или в библиотеке динамической компоновки. Тем не менее, эти сведения не являются критическими; все, что имеет значение, это то, что RDS отправляет **набор записей** обратно клиенту.

На стороне клиента возвращается объект **Recordset** и назначается локальной переменной.

```vb 
 
Sub RDSTutorial4() 
 Dim DS as New RDS.DataSpace 
 Dim RS as ADODB.Recordset 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query("DSN=Pubs", "SELECT * FROM Authors") 
... 
```

## <a name="step-5-datacontrol-is-made-usable"></a>Шаг 5: управление этими процессами осуществляется 

Возвращенный объект **Recordset** доступен для использования. Вы можете просматривать, перемещать и изменять его, как и любой другой **набор записей**. Действия, которые можно выполнять с **набором записей** , зависят от среды. Visual Basic и Visual C++ имеют визуальные элементы управления, которые могут напрямую или косвенно использовать **набор записей** с помощью элемента управления "включение данных".

Например, при отображении веб-страницы в Internet Explorer может потребоваться отобразить данные объекта **Recordset** в визуальном элементе управления. Визуальные элементы управления на веб-странице не могут напрямую получить доступ к объекту **Recordset** . Тем не менее, они могут получить доступ к объекту **Recordset** с помощью [RDS. Элемент управления](datacontrol-object-rds.md). **RDS. Элемент управления** данным используется визуальным элементом управления, если его свойство [SourceRecordset](recordset-sourcerecordset-properties-rds.md) задано для объекта **Recordset** .

Для объекта визуального элемента управления должен быть задан параметр **датасрк** для **RDS. Элемент управления**данным и его свойство **датафлд** , заданное для поля объекта **Recordset** (Column).

В этом руководстве показано, как задать свойство **SourceRecordset** :

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

## <a name="step-6-changes-are-sent-to-the-server"></a>Шаг 6: изменения отправляются на сервер

Если объект **Recordset** редактируется, любые изменения (то есть добавленные, измененные или удаленные строки) можно отправить обратно на сервер.

Поведение RDS, используемое по умолчанию, может быть неявно вызвано объектами ADO и поставщиком удаленного взаимодействия Microsoft OLE DB. Запросы могут возвращать **наборы записей**, а измененные **наборы записей** могут обновлять источник данных. В этом руководстве не происходит вызов RDS с объектами ADO, но именно так она будет выглядеть:

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "SELECT * FROM Authors","Provider=MS Remote;Data Source=Pubs;" & _ 
 "Remote Server=https://yourServer;Remote Provider=SQLOLEDB;" 
... ' Edit the Recordset. 
rs.UpdateBatch ' The equivalent of SubmitChanges. 
... 
```

### <a name="part-a"></a>Часть A

Предположим, что в этом случае использовались только [RDS. Элемент управления](datacontrol-object-rds.md) данными и объект **Recordset** теперь связан с элементом **ActiveX RDS. Элемент управления**. Метод [SubmitChanges](submitchanges-method-rds.md) обновляет источник данных с использованием любых изменений объекта **Recordset** , если свойства [Server](server-property-rds.md) и [Connect](connect-property-rds.md) по-прежнему заданы.

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

### <a name="part-b"></a>Часть B

Кроме того, вы можете обновить сервер с помощью объекта [рдссервер.](datafactory-object-rdsserver.md) DataObject, указав соединение и объект **Recordset** .

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


## <a name="appendix-a-rds-tutorial-vbscript"></a>Приложение а: руководство по RDS (VBScript)

Это руководство по RDS, написанное в Microsoft Visual Basic Scripting Edition. Описание назначения этого руководства представлено в статье Введение в эту статью.

В этом руководстве [RDS. Элемент управления](datacontrol-object-rds.md) и [RDS. Пространство](dataspace-object-rds.md) , созданное во время конструирования; то есть они определяются с помощью тегов объекта. Кроме того, они могут быть созданы во время выполнения с помощью метода **Server. CreateObject** . 

Например, элемент **ActiveX RDS. Объект элемента управления** данным может быть создан следующим образом:

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

### <a name="step-1-specify-a-server-program"></a>Шаг 1: указание серверной программы

С помощью VBScript можно определить имя веб-сервера IIS, на котором он работает, путем доступа к методу **request. сервервариаблес** , доступный для ASP-страниц:

```vb 
 
"https://<%=Request.ServerVariables("SERVER_NAME")%>" 
```

Однако в этом руководстве используется мнимой сервер "Йоурсервер".

> [!NOTE]
> Обратите внимание на тип данных аргументов **ByRef** . VBScript не позволяет указать тип переменной, поэтому всегда необходимо передавать Variant. При использовании протокола HTTP RDS позволяет передать значение Variant методу, который ожидает неизменяемый метод, если он будет вызван с помощью **RDS. **Метод [CreateObject](createobject-method-rds.md) объекта Space. При использовании DCOM или внутрипроцессного сервера соответствуют типам параметров на стороне клиента и сервера, а также отображается сообщение об ошибке "несоответствие типов".

```vb
 
Set DF1 = DS1.CreateObject("RDSServer.DataFactory", "https://yourServer") 
```

### <a name="step-2-part-a-invoke-the-server-program-with-rdsdatacontrol"></a>Этап 2, часть A: вызов серверной программы с помощью RDS. DataControl

В этом примере показан только комментарий, демонстрирующий поведение RDS в качестве поведения по умолчанию **. Элемент управления** данных предназначен для выполнения указанного запроса.

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

### <a name="step-4-server-returns-the-recordset"></a>Шаг 4: сервер возвращает объект Recordset

```vb
 
Set RS = DF1.Query("DSN=Pubs;", "SELECT * FROM Authors") 
```

### <a name="step-5-datacontrol-is-made-usable-by-visual-controls"></a>Шаг 5: элемент управления с помощью визуальных элементов управления

```vb
 
' Assign the returned recordset to the DataControl. 
 
DC1.SourceRecordset = RS 
```

### <a name="step-6-part-a-changes-are-sent-to-the-server-with-rdsdatacontrol"></a>Шаг 6, часть A: изменения отправляются на сервер с помощью RDS. DataControl

В этом примере показан только комментарий, демонстрирующий, как **RDS. Элемент управления "элемент управления** " выполняет обновление.

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

### <a name="step-6-part-b-changes-are-sent-to-the-server-with-rdsserverdatafactory"></a>Шаг 6, часть B: изменения отправляются на сервер с помощью Рдссервер. факты

```vb
 
DF.SubmitChanges"DSN=Pubs", RS 
 
End Sub 
</SCRIPT> 
</BODY> 
</HTML> 
```

## <a name="appendix-b-rds-tutorial-visual-j"></a>Приложение б: руководство по RDS (Visual J++)

ADO/WFC не полностью следит за объектной моделью RDS, так как он не реализует [RDS. Объект управления](datacontrol-object-rds.md) DataObject. ADO/WFC реализует только клиентский класс [RDS. Пространство для ввода](dataspace-object-rds.md).

Класс **Space** реализует один метод, [CreateObject](createobject-method-rds.md), который возвращает объект [обжектпрокси](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/objectproxy-ado-wfc-syntax) . Класс **Space** также реализует свойство [InternetTimeout](internettimeout-property-rds.md) .

Класс **обжектпрокси** реализует один метод, Call, который может вызывать любой серверный бизнес-объект.

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



