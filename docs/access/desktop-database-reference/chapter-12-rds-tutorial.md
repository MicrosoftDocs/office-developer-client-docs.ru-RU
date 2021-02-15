---
title: Глава 12. Руководство по удаленной службе данных (RDS)
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
# <a name="chapter-12-remote-data-service-rds-tutorial"></a>Глава 12. Руководство по удаленной службе данных (RDS)

**Область применения**: Access 2013, Office 2013

В этом руководстве показано использование модели программирования RDS для запроса и обновления источника данных. Во-первых, в нем описываются действия, необходимые для выполнения этой задачи. Затем учебник повторяется в Microsoft Visual Basic Scripting Edition и Microsoft Visual J++, в котором представлены классы ADO для Windows Foundation (ADO/WFC).

Этот учебник коден на разных языках по двум причинам:

- В документации по RDS предполагается, что коды чтения в Visual Basic. Это делает документацию удобной для Visual Basic программистов, но менее полезной для программистов, которые используют другие языки.

- Если вы не уверены в определенной функции RDS и знаете немного другой язык, вы можете разрешить свой вопрос, выполнив поиск той же функции, которая выражается на другом языке.

Это руководство основано на модели программирования RDS. В ней каждый этап модели программирования обсуждается по отдельности. Кроме того, он иллюстрирует каждый шаг с фрагментом Visual Basic кода.

Пример кода повторяется на других языках с минимальным обсуждением. Каждый шаг в данном учебнике по языку программирования помечен соответствующим шагом в модели программирования и описательном руководстве. Используйте номер шага для ссылки на обсуждение в описательной учебнике.

Модель программирования RDS приведена ниже. Используйте его в качестве плана по мере перехода к учебнику.

### <a name="rds-programming-model-with-objects"></a>Модель программирования RDS с объектами

- Укажите вызываемую на сервере программу и получите способ (прокси-сервер) ссылаться на нее от клиента.

- Вызов серверной программы. Передав параметры серверной программе, которая определяет источник данных и команду для выдачи.

- Серверная программа получает объект [Recordset](recordset-object-ado.md) из источника данных, обычно с помощью ADO. При желании **объект Recordset** обрабатывается на сервере.

- Серверная программа возвращает конечный **объект Recordset** в клиентском приложении.

- В клиенте объект **Recordset** при желании можно поместить в форму, которая может быть легко использована визуальными элементами управления.

- Изменения объекта **Recordset** отправляются обратно на сервер и используются для обновления источника данных.

## <a name="step-1-specify-a-server-program"></a>Шаг 1. Указание серверной программы

В большинстве общих случаях используйте [RDS. Метод](dataspace-object-rds.md) [CreateObject](createobject-method-rds.md) объекта DataSpace для указания серверной программы по умолчанию, [RDSServer.DataFactory](datafactory-object-rdsserver.md)или собственной программы настраиваемого сервера (бизнес-объекта). На сервере и возвращается ссылка на серверную программу или прокси-сервер.

В этом руководстве используется серверная программа по умолчанию:

```vb 
 
Sub RDSTutorial1() 
 Dim DS as New RDS.DataSpace 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
... 
``` 

## <a name="step-2-invoke-the-server-program"></a>Шаг 2. Вызов серверной программы 

При вызове метода на прокси-сервере клиента его выполняет фактическая программа на сервере. На этом этапе выполняется запрос на сервере.

### <a name="part-a"></a>Часть A

Если вы не использовали [RDSServer.DataFactory](datafactory-object-rdsserver.md) в этом руководстве, наиболее удобным способом выполнения этого шага будет использование [RDS. Объект DataControl.](datacontrol-object-rds.md) The **RDS. DataControl** объединяет предыдущий этап создания прокси-сервера, а на этом этапе — выдачу запроса.

1. Установите **RDS. Свойство DataControl** object [Server](server-property-rds.md) для определения места, где следует установить серверную программу.

2. Установите свойство [Connect,](connect-property-rds.md) чтобы указать строку подключения для доступа к источнику данных.

3. Закажите [SQL,](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) чтобы указать текст команды запроса. 

4. Выдайте метод [Refresh,](refresh-method-rds.md) чтобы серверная программа подключалась к источнику данных, извлекла строки, указанные в запросе, и возвращала клиенту объект **Recordset.**

В этом руководстве не используется **RDS. DataControl**, но это будет выглядеть, если бы он:

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

Руководство также не вызывает RDS с объектами ADO, но в этом случае он будет выглядеть так:

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "SELECT * FROM Authors","Provider=MS Remote;Data Source=Pubs;" & _ 
"Remote Server=https://yourServer;Remote Provider=SQLOLEDB;" 
```

### <a name="part-b"></a>Часть B

Общий метод выполнения этого шага — вызвать метод запроса объекта **RDSServer.DataFactory.** [](query-method-rds.md) Этот метод принимает строку подключения, которая используется для подключения к источнику данных, и текст команды, который используется для указания строк, возвращаемой из источника данных.

В этом руководстве используется метод Запроса объекта **DataFactory:** 

```vb 
 
Sub RDSTutorial2B() 
 Dim DS as New RDS.DataSpace 
 Dim DF 
 Dim RS as ADODB.Recordset 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
... 
```

## <a name="step-3-server-obtains-a-recordset"></a>Шаг 3. Сервер получает набор записей 

Серверная программа использует строку подключения и текст команды для запроса источника данных для нужных строк. ADO обычно используется для извлечения этого **recordset,** хотя могут использоваться другие интерфейсы доступа к данным Майкрософт, такие как OLE DB.

Настраиваемая серверная программа может выглядеть так:

```vb 
 
Public Function ServerProgram(cn as String, qry as String) as Object 
Dim rs as New ADODB.Recordset 
 rs.CursorLocation = adUseClient 
 rs.Open qry, cn 
 rs.ActiveConnection = Nothing 
 Set ServerProgram = rs 
End Function 
```

## <a name="step-4-server-returns-the-recordset"></a>Шаг 4. Сервер возвращает набор записей 

RDS преобразует полученный объект **Recordset** в форму, которую можно отправить клиенту  (то есть маршалировать **объект Recordset).** Точная форма преобразования и его отправление зависят от того, находится ли сервер в Интернете, в интрасети, в локальной сети или в библиотеке динамической связи. Однако эта информация не является критической; Важно только то, что RDS отправляет **набор записей** обратно клиенту.

На стороне клиента объект **Recordset** возвращается и назначен локальной переменной.

```vb 
 
Sub RDSTutorial4() 
 Dim DS as New RDS.DataSpace 
 Dim RS as ADODB.Recordset 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query("DSN=Pubs", "SELECT * FROM Authors") 
... 
```

## <a name="step-5-datacontrol-is-made-usable"></a>Шаг 5. DataControl можно сделать можной 

Возвращенный **объект Recordset** доступен для использования. Вы можете изучать, перемещаться и редактировать его так же, как и любой другой **набор записей.** То, что можно сделать с **набором записей,** зависит от среды. Visual Basic Visual C++ имеют визуальные элементы управления, которые могут напрямую или косвенно использовать набор записей с помощью включаемого управления данными. 

Например, если вы отображаете веб-страницу в Internet Explorer, может потребоваться отобразить данные объекта **Recordset** в визуальном объекте управления. Визуальные элементы управления на веб-странице не могут получить прямой доступ **к объекту Recordset.** Однако они могут получить доступ к **объекту Recordset** через [RDS. DataControl](datacontrol-object-rds.md). The **RDS. DataControl** становится понятным для визуального управления, когда его свойство [SourceRecordset](recordset-sourcerecordset-properties-rds.md) имеет объект **Recordset.**

Для объекта визуального управления параметр **DATASRC** должен быть установлен в **RDS. DataControl и** его свойство **DATAFLD,** задав поле объекта **Recordset** (столбец).

В этом руководстве установите свойство **SourceRecordset:**

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

## <a name="step-6-changes-are-sent-to-the-server"></a>Шаг 6. Изменения отправляются на сервер

При **редактировании** объекта Recordset любые изменения (то есть добавляемая, измененная или удаленная строка) могут быть отправлены обратно на сервер.

Поведение RDS по умолчанию может быть вызвано неявно с объектами ADO и microsoft OLE DB Remoting Provider. Запросы могут возвращать **наборы записей,** а измененные наборы записей могут обновлять источник данных.  В этом руководстве не вызывается RDS с объектами ADO, но в этом случае он будет выглядеть так:

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "SELECT * FROM Authors","Provider=MS Remote;Data Source=Pubs;" & _ 
 "Remote Server=https://yourServer;Remote Provider=SQLOLEDB;" 
... ' Edit the Recordset. 
rs.UpdateBatch ' The equivalent of SubmitChanges. 
... 
```

### <a name="part-a"></a>Часть A

Предположим, что в этом случае вы использовали только [RDS. DataControl](datacontrol-object-rds.md) и объект **Recordset** теперь связан с **RDS. DataControl**. Метод [SubmitChanges](submitchanges-method-rds.md) обновляет источник данных, внося любые изменения в объект **Recordset,** если свойства [Server](server-property-rds.md) и [Connect](connect-property-rds.md) по-прежнему за установлены.

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

Кроме того, можно обновить сервер с помощью объекта [RDSServer.DataFactory,](datafactory-object-rdsserver.md) указав подключение и **объект Recordset.**

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


## <a name="appendix-a-rds-tutorial-vbscript"></a>Приложение А. Руководство по RDS (VBScript)

Это руководство по RDS, написанное в Microsoft Visual Basic Scripting Edition. Описание назначения этого руководства см. в разделе, введении в этот раздел.

В этом руководстве [RDS. DataControl](datacontrol-object-rds.md) и [RDS. Пространство данных](dataspace-object-rds.md) создается во время разработки; то есть они определяются с помощью тегов объектов. Кроме того, их можно создать во время работы с помощью метода **Server.CreateObject.** 

Например, **RDS. Объект DataControl** можно создать так:

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

### <a name="step-1-specify-a-server-program"></a>Шаг 1. Указание серверной программы

VBScript может обнаружить имя веб-сервера IIS, на который он запущен, открыв метод VBScript **Request.ServerVariables,** доступный для ASP:

```vb 
 
"https://<%=Request.ServerVariables("SERVER_NAME")%>" 
```

Однако в этом руководстве используйте вымышленный сервер "yourServer".

> [!NOTE]
> Обратите внимание на тип данных аргументов **ByRef.** VBScript не дает указать тип переменной, поэтому необходимо всегда передавать variant. При использовании ПРОТОКОЛА HTTP RDS позволяет передать Variant методу, который ожидает не-Variant, если вызвать его с **помощью RDS. Метод** [CreateObject](createobject-method-rds.md) объекта DataSpace. При использовании DCOM или сервера, используемого в процессе, соведите типы параметров на стороне клиента и сервера или вы получите сообщение об ошибке "Несоответствие типов".

```vb
 
Set DF1 = DS1.CreateObject("RDSServer.DataFactory", "https://yourServer") 
```

### <a name="step-2-part-a-invoke-the-server-program-with-rdsdatacontrol"></a>Шаг 2. Часть A. Вызов серверной программы с помощью RDS. DataControl

В этом примере просто демонстрируется поведение **RDS по умолчанию. DataControl** выполняет указанный запрос.

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

Переперейти к следующему шагу.

### <a name="step-4-server-returns-the-recordset"></a>Шаг 4. Сервер возвращает набор записей

```vb
 
Set RS = DF1.Query("DSN=Pubs;", "SELECT * FROM Authors") 
```

### <a name="step-5-datacontrol-is-made-usable-by-visual-controls"></a>Шаг 5. Элемент управления DataControl можно сделать понятным с помощью визуальных элементов управления

```vb
 
' Assign the returned recordset to the DataControl. 
 
DC1.SourceRecordset = RS 
```

### <a name="step-6-part-a-changes-are-sent-to-the-server-with-rdsdatacontrol"></a>Шаг 6. Часть A. Изменения отправляются на сервер с RDS. DataControl

В этом примере просто демонстрируется, как **RDS. DataControl** выполняет обновления.

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

### <a name="step-6-part-b-changes-are-sent-to-the-server-with-rdsserverdatafactory"></a>Шаг 6, часть Б. Изменения отправляются на сервер с помощью RDSServer.DataFactory

```vb
 
DF.SubmitChanges"DSN=Pubs", RS 
 
End Sub 
</SCRIPT> 
</BODY> 
</HTML> 
```

## <a name="appendix-b-rds-tutorial-visual-j"></a>Приложение Б. Руководство по RDS (Visual J++)

ADO/WFC не полностью следует объектной модели RDS, так как не реализует [RDS. Объект DataControl.](datacontrol-object-rds.md) ADO/WFC реализует только клиентский класс [RDS. DataSpace](dataspace-object-rds.md).

Класс **DataSpace** реализует один [метод, CreateObject,](createobject-method-rds.md)который возвращает [объект ObjectProxy.](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/objectproxy-ado-wfc-syntax) Класс **DataSpace** также реализует свойство [InternetTimeout.](internettimeout-property-rds.md)

Класс **ObjectProxy** реализует один метод— вызов, который может вызывать любой серверный бизнес-объект.

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



