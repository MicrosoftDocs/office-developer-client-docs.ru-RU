---
title: Использование Microsoft Access в качестве сервера DDE
TOCTitle: Use Microsoft Access as a DDE Server
description: Microsoft Access поддерживает динамический обмен данными (DDE) как приложение назначения (клиент) или приложение источника (сервер).
ms:assetid: a3e82bf7-94b5-8eec-86bc-2d5387d66738
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821067(v=office.15)
ms:contentKeyID: 48546801
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5186349
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 0750bdce0e1cda383c48f9c16e62e00997fdfb0a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313393"
---
# <a name="use-microsoft-access-as-a-dde-server"></a>Использование Microsoft Access в качестве сервера DDE

**Область применения**: Access 2013, Office 2013 

Microsoft Access поддерживает динамический обмен данными (DDE) как приложение назначения (клиент) или приложение источника (сервер). Например, такое приложение, как Microsoft Word, действующее в качестве клиента, может запрашивать данные через DDE из базы данных Microsoft Access, которая действует как сервер.

> [!TIP]
> Если вам нужно управлять объектами Microsoft Access из другого приложения, можно рассмотреть возможность использования автоматизации.

Беседа DDE между клиентом и сервером устанавливается по определенной теме. Раздел может быть файлом данных в формате, поддерживаемом серверным приложением, или разделом "Система", который представляет сведения о самом серверном приложении. После начала беседы по определенному разделу можно перенести только элемент данных, связанный с этим разделом.

Например, предположим, что вы работаете с Microsoft Word и хотите вставить данные из определенной базы данных Microsoft Access в документ. Вы начинаете беседу DDE с Microsoft Access, открыв канал DDE с помощью функции **DDEInitiate** и указав имя файла базы данных в качестве темы. Затем можно передать данные из этой базы данных в Microsoft Word через этот канал.

Как сервер DDE Microsoft Access поддерживает следующие разделы:

- Раздел "Система"

- Имя базы данных (тема *базы* данных)

- Имя таблицы *(раздел "Имя таблицы")*

- Имя запроса (*раздел "Имя запроса")*

- Строка SQL Microsoft Access (*раздел sqlstring)*

После того как вы установили беседу DDE, можно использовать заявление **DDEExecute** для отправки команды от клиента в серверную приложение. При этом Microsoft Access распознает любое из следующих действий как допустимую команду:

- Имя макроса в текущей базе данных.

- Любое действие, которое можно выполнить в Visual Basic с помощью одного из методов объекта **DoCmd.**

- Действия OpenDatabase и CloseDatabase, которые используются только для операций DDE. (Пример использования этих действий см. в примере далее в этом разделе.)

> [!NOTE]
> Если макрокоманд указывается в качестве заявления **DDEExecute,** то действие и любые аргументы следуют синтаксису объекта **DoCmd** и должны быть заключены в скобки ([ ]). Однако приложения, которые поддерживают DDE, не распознают внутренние константы в операциях DDE. Кроме того, строки-аргументы должны быть заключены в кавычках (" "), если строка содержит запятую. В противном случае кавычка не требуется.

Клиентские приложения могут использовать **функцию DDERequest** для запроса текстовых данных из серверного приложения по открытому каналу DDE. Или клиент может использовать заявление **DDEPoke** для отправки данных в серверные приложения. После завершения передачи данных клиент может закрыть канал DDE с помощью заявления **DDETerminate** или **DDETerminateAll,** чтобы закрыть все открытые каналы.

> [!NOTE]
> Когда клиентские приложения завершат получение данных по каналу DDE, оно должно закрыть этот канал, чтобы сэкономить ресурсы памяти.

В следующем примере показано, как создать процедуру Microsoft Word с Visual Basic microsoft Access в качестве DDE-сервера. (Чтобы этот пример работал, необходимо использовать Microsoft Access.)

```vb
    Sub AccessDDE() 
        Dim intChan1 As Integer, intChan2 As Integer 
        Dim strQueryData As String 
     
        ' Use System topic to open Northwind sample database. 
        ' Database must be open before using other DDE topics. 
        intChan1 = DDEInitiate("MSAccess", "System") 
        ' You may need to change this path to point to actual location 
        ' of Northwind sample database. 
        DDEExecute intChan1, "[OpenDatabase C:\Access\Samples\Northwind.mdb]" 
     
        ' Get all data from Ten Most Expensive Products query. 
        intChan2 = DDEInitiate("MSAccess", "Northwind.mdb;" _ 
            & "QUERY Ten Most Expensive Products") 
        strQueryData = DDERequest(intChan2, "All") 
        DDETerminate intChan2 
     
        ' Close database. 
        DDEExecute intChan1, "[CloseDatabase]" 
        DDETerminate intChan1 
     
        ' Print retrieved data to Debug Window. 
        Debug.Print strQueryData 
    End Sub
```

<br/>

В следующих разделах приводится информация о допустимых разделах DDE, поддерживаемых Microsoft Access.

## <a name="the-system-topic"></a>Раздел "Система"

Раздел "Система" является стандартным разделом для всех приложений на основе Microsoft Windows. В нем данная информация о других темах, поддерживаемых приложением. Чтобы получить доступ к этой информации, код должен сначала  вызвать функцию **DDEInitiate** с аргументом темы, а  затем выполнить заявление **DDERequest** с одним из следующих аргументов элемента.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Элемент</p></th>
<th><p>Возвращаемое значение</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>SysItems</p></td>
<td><p>Список элементов, поддерживаемых разделом "Система" в Microsoft Access.</p></td>
</tr>
<tr class="even">
<td><p>Форматы</p></td>
<td><p>Список форматов, которые Microsoft Access может скопировать в буфер обмена.</p></td>
</tr>
<tr class="odd">
<td><p>Состояние</p></td>
<td><p>&quot;Занят &quot; или &quot; &quot; готов.</p></td>
</tr>
<tr class="even">
<td><p>Темы</p></td>
<td><p>Список всех открытых баз данных.</p></td>
</tr>
</tbody>
</table>

<br/>

В следующем примере показано использование функций **DDEInitiate** и **DDERequest** в разделе "Система":

```vb
    ' In Visual Basic, initiate DDE conversation with Microsoft Access. 
    Dim intChan1 As Integer, strResults As String 
    intChan1 = DDEInitiate("MSAccess", "System") 
    ' Request list of topics supported by System topic. 
    strResults = DDERequest(intChan1, "SysItems") 
    ' Run OpenDatabase action to open Northwind.mdb. 
    ' You may need to change this path to point to actual location 
    ' of Northwind sample database. 
    DDEExecute intChan1, "[OpenDatabase C:\Access\Samples\Northwind.mdb]"
```

## <a name="the-database-topic"></a>Тема базы данных

Тема *базы* данных — имя файла существующей базы данных. Можно ввести только базовое имя (Northwind) или его путь и расширение MDB (C: \\ Access \\ Samples \\ Northwind.mdb). После начала беседы DDE с базой данных можно запросить список объектов в этой базе данных.

> [!NOTE]
> Нельзя использовать DDE для запроса файла сведений о группе Microsoft Access.

В *разделе базы* данных поддерживаются следующие элементы.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Элемент</p></th>
<th><p>Возвращаемое значение</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>TableList</p></td>
<td><p>Список таблиц</p></td>
</tr>
<tr class="even">
<td><p>QueryList</p></td>
<td><p>Список запросов</p></td>
</tr>
<tr class="odd">
<td><p>FormList</p></td>
<td><p>Список форм</p></td>
</tr>
<tr class="even">
<td><p>ReportList</p></td>
<td><p>Список отчетов</p></td>
</tr>
<tr class="odd">
<td><p>MacroList</p></td>
<td><p>Список макроса</p></td>
</tr>
<tr class="even">
<td><p>ModuleList</p></td>
<td><p>Список модулей</p></td>
</tr>
<tr class="odd">
<td><p>ViewList</p></td>
<td><p>Список представлений</p></td>
</tr>
<tr class="even">
<td><p>StoredProcedureList</p></td>
<td><p>Список хранимой процедуры</p></td>
</tr>
<tr class="odd">
<td><p>DatabaseDiagramList</p></td>
<td><p>Список схем базы данных</p></td>
</tr>
</tbody>
</table>

<br/>

В следующем примере показано, как можно открыть форму Employees в образце базы данных Northwind из Visual Basic процедуры:

```vb
    ' In Visual Basic, initiate DDE conversation with 
    ' Northwind sample database. 
    ' Make sure database is open. 
    intChan2 = DDEInitiate("MSAccess", "Northwind") 
    ' Request list of forms in Northwind sample database. 
    strResponse = DDERequest(intChan2, "FormList") 
    ' Run OpenForm action and arguments to open Employees form. 
    DDEExecute intChan2, "[OpenForm Employees,0,,,1,0]"
```

## <a name="the-table-topic"></a>Раздел "ТАБЛИЦА"

В этих темах используется следующий синтаксис:

_databasename;_ **TABLE** _tablename_

_databasename;_ **QUERY** _queryname_

_databasename;_ **SQL** [ _sqlstring_ ]

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Часть</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>databasename</em></p></td>
<td><p>Имя базы данных, в которой находится таблица или запрос, или к SQL применяется ;). Имя базы данных может быть только базовым именем (Northwind) или полным путем и расширением MDB (C:\Access\Samples\Northwind.mdb).</p></td>
</tr>
<tr class="even">
<td><p><em>tablename</em></p></td>
<td><p>Имя существующей таблицы.</p></td>
</tr>
<tr class="odd">
<td><p><em>queryname</em></p></td>
<td><p>Имя существующего запроса.</p></td>
</tr>
<tr class="even">
<td><p><em>sqlstring</em></p></td>
<td><p>Допустимый SQL длиной до 256 символов, заканчивающийся на зачетную. Чтобы обменяться более 256 символами, опустить этот аргумент и вместо этого используйте последовательные заявления <strong>DDEPoke</strong> для создания SQL. Например, следующий код Visual Basic использует для создания SQL <strong>DDEPoke,</strong> а затем запрашивает результаты запроса.</p></td>
</tr>
</tbody>
</table>

<br/>

В следующей таблице перечислены допустимые элементы для таблиц *TABLEname,* QUERY *queryname* и SQL *sqlstring.*

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Элемент</p></th>
<th><p>Возвращаемое значение</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Все</p></td>
<td><p>Все данные в таблице, включая имена полей.</p></td>
</tr>
<tr class="even">
<td><p>Данные</p></td>
<td><p>Все строки данных без имен полей.</p></td>
</tr>
<tr class="odd">
<td><p>FieldNames</p></td>
<td><p>Список имен полей из одной строки.</p></td>
</tr>
<tr class="even">
<td><p>FieldNames; T</p></td>
<td><p>Список имен полей из двух строк (первая строка) и их типов данных (вторая строка).</p>
<p>Возвращаются указанные значения.</p>
<p>Значение</p>
<p><ul>
<li>0</li>
<li>1 </li>
<li>2 </li>
<li>3 </li>
<li>4 </li>
<li>5 </li>
<li>6 </li>
<li>7 </li>
<li>8 </li>
<li>9 </li>
<li>10 </li>
<li>11</li>
<li>12 </li>
</ul>
</p>
</td>
</tr>
<tr class="even">
<td><p>NextRow</p></td>
<td><p>Данные в следующей строке таблицы или запроса. При открываемом канале NextRow возвращает данные в первой строке. Если текущая строка является последней записью и вы запустите NextRow, запрос не будет работать.</p></td>
</tr>
<tr class="odd">
<td><p>PrevRow</p></td>
<td><p>Данные в предыдущей строке таблицы или запроса. Если PrevRow является первым запросом для нового канала, возвращаются данные в последней строке таблицы или запроса. Если первой записью является текущая строка, запрос PrevRow не будет.</p></td>
</tr>
<tr class="even">
<td><p>FirstRow</p></td>
<td><p>Данные в первой строке таблицы или запроса.</p></td>
</tr>
<tr class="odd">
<td><p>LastRow</p></td>
<td><p>Данные в последней строке таблицы или запроса.</p></td>
</tr>
<tr class="even">
<td><p>FieldCount</p></td>
<td><p>Количество полей в таблице или запросе.</p></td>
</tr>
<tr class="odd">
<td><p>SQLText</p></td>
<td><p>SQL, представляющий таблицу или запрос. Для таблиц этот элемент возвращает SQL в виде &quot; таблицы SELECT `*` FROM ; <em></em> &quot; .</p></td>
</tr>
<tr class="even">
<td><p>SQLText; <em>n</em></p></td>
<td><p>An SQL, in <em>n</em>-character chunks, representing the table or query, where <em>n</em> is an integer up to 256. Например, предположим, что запрос представлен следующим SQL: элемент SQLText;7 возвращает следующие блоки с делегировками &quot; &quot; вкладок: элемент &quot; SQLText;7 возвращает следующие блоки с делегировками &quot; вкладок:</p></td>
</tr>
</tbody>
</table>

<br/>

В следующем примере показано, как можно использовать DDE в процедуре Visual Basic для запроса данных из таблицы в образце базы данных Northwind и вставки этих данных в текстовый файл:

```vb
    Sub NorthwindDDE 
        Dim intChan1 As Integer, intChan2 As Integer, intChan3 As Integer 
        Dim strResp1 As Variant, strResp2 As Variant, strResp3 As Variant 
     
        ' In a Visual Basic module, get data from Categories table, 
        ' Catalog query, and Orders table in Northwind.mdb. 
        ' Make sure database is open first. 
        intChan1 = DDEInitiate("MSAccess", "Northwind;TABLE Shippers") 
        intChan2 = DDEInitiate("MSAccess", "Northwind;QUERY Catalog") 
        intChan3 = DDEInitiate("MSAccess", "Northwind;SQL SELECT * " _ 
            & "FROM Orders " _ 
            & "WHERE OrderID > 10050;") 
     
        strResp1 = DDERequest(intChan1, "All") 
        strResp2 = DDERequest(intChan2, "FieldNames;T") 
        strResp3 = DDERequest(intChan3, "FieldNames;T") 
        DDETerminate intChan1 
        DDETerminate intChan2 
        DDETerminate intChan3 
     
        ' Insert data into text file. 
        Open "C:\DATA.TXT" For Append As #1 
        Print #1, strResp1 
        Print #1, strResp2 
        Print #1, strResp3 
        Close #1 
    End Sub
```
