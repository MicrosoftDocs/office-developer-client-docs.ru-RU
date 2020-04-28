---
title: Использование Microsoft Access в качестве сервера DDE
TOCTitle: Use Microsoft Access as a DDE Server
description: Microsoft Access поддерживает динамический обмен данными (DDE) в качестве конечного (клиентского) приложения или приложения-источника (сервера).
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

Microsoft Access поддерживает динамический обмен данными (DDE) в качестве конечного (клиентского) приложения или приложения-источника (сервера). Например, приложение, например Microsoft Word, выполняющее функции клиента, может запрашивать данные с помощью DDE из базы данных Microsoft Access, работающей в качестве сервера.

> [!TIP]
> Если вам нужно манипулировать объектами Microsoft Access из другого приложения, вы можете использовать автоматизацию.

Сеанс DDE между клиентом и сервером устанавливается в определенном разделе. Тема может представлять собой файл данных в формате, поддерживаемом серверным приложением, или может быть системным разделом, предоставляющим сведения о самом серверном приложении. После начала беседы с определенным разделом можно переносить только элементы данных, связанные с этим разделом.

Например, предположим, что вы используете Microsoft Word и хотите вставить данные из определенной базы данных Microsoft Access в документ. Вы начинаете сеанс DDE с Microsoft Access, открыв канал DDE с помощью функции **ддеинитиате** и указав имя файла базы данных в качестве раздела. Затем вы можете перенести данные из этой базы данных в Microsoft Word через этот канал.

Как сервер DDE, Microsoft Access поддерживает следующие разделы:

- Раздел "система"

- Имя базы данных (раздел*базы данных* )

- Имя таблицы (раздел*имя_таблицы* )

- Имя запроса (раздел*куеринаме* )

- Строка SQL Microsoft Access (раздел "*склстринг* ")

После установки беседы DDE можно использовать инструкцию **ддиксекуте** для отправки команды от клиента к приложению сервера. При использовании в качестве сервера DDE в качестве допустимой команды Microsoft Access распознает любую из следующих команд:

- Имя макроса в текущей базе данных.

- Все действия, которые можно выполнить в Visual Basic, с помощью одного из методов объекта **DoCmd** .

- Действия OpenDatabase и Клоседатабасе, которые используются только для операций DDE. (Пример использования этих действий представлен в примере далее в этом разделе.)

> [!NOTE]
> При указании макрокоманды в качестве оператора **ддиксекуте** действие и все аргументы следуют за синтаксисом объекта **DoCmd** и должны быть заключены в квадратные скобки ([]). Однако приложения, поддерживающие DDE, не распознают встроенные константы в операциях DDE. Кроме того, строковые аргументы должны быть заключены в кавычки (""), если строка содержит запятую. В противном случае кавычки не требуются.

Клиентское приложение может использовать функцию **ддерекуест** для запроса текстовых данных из серверного приложения через открытый канал DDE. Или клиент может использовать инструкцию **ддепоке** для отправки данных в серверное приложение. После завершения передачи данных клиент может использовать оператор **ддетерминате** для закрытия канала DDE или инструкцию **ддетерминатеалл** для закрытия всех открытых каналов.

> [!NOTE]
> Когда клиентское приложение завершит получение данных по каналу DDE, оно должно закрыть этот канал для экономии ресурсов памяти.

В приведенном ниже примере показано, как создать процедуру Microsoft Word с помощью Visual Basic, использующей Microsoft Access в качестве сервера DDE. (Для работы этого примера должна быть запущена служба Microsoft Access.)

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

В следующих разделах приведены сведения о действительных темах DDE, поддерживаемых в Microsoft Access.

## <a name="the-system-topic"></a>Раздел "система"

Раздел System — это стандартный раздел для всех приложений на основе Microsoft Windows. Он предоставляет сведения о других темах, поддерживаемых приложением. Чтобы получить доступ к этим сведениям, код должен сначала вызвать функцию **ддеинитиате** с аргументом *Topic* , а затем выполнить инструкцию **ддерекуест** с одним из следующих элементов, предоставленных для аргумента *Item* .

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Item</p></th>
<th><p>Возвращаемое значение</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>сиситемс</p></td>
<td><p>Список элементов, которые поддерживаются в разделе System в Microsoft Access.</p></td>
</tr>
<tr class="even">
<td><p>Различных</p></td>
<td><p>Список форматов, которые Microsoft Access может скопировать в буфер обмена.</p></td>
</tr>
<tr class="odd">
<td><p>Состояние</p></td>
<td><p>&quot;&quot; Занято &quot;или&quot;готово.</p></td>
</tr>
<tr class="even">
<td><p>Темы</p></td>
<td><p>Список всех открытых баз данных.</p></td>
</tr>
</tbody>
</table>

<br/>

В следующем примере показано использование функций **ддеинитиате** и **Ддерекуест** с темой системы:

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

## <a name="the-database-topic"></a>Раздел Database

Раздел *Database* — это имя существующего файла базы данных. Можно ввести только базовое имя (Northwind) или его путь и расширение MDB (C:\\Samples\\\\Access Northwind. mdb). После того как вы начнете сеанс DDE с базой данных, вы можете запросить список объектов в этой базе данных.

> [!NOTE]
> Невозможно использовать DDE для запроса к файлу сведений рабочей группы Microsoft Access.

Раздел *Database* поддерживает следующие элементы.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Item</p></th>
<th><p>Возвращаемое значение</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>таблелист</p></td>
<td><p>Список таблиц</p></td>
</tr>
<tr class="even">
<td><p>куерилист</p></td>
<td><p>Список запросов</p></td>
</tr>
<tr class="odd">
<td><p>формлист</p></td>
<td><p>Список форм</p></td>
</tr>
<tr class="even">
<td><p>ReportList</p></td>
<td><p>Список отчетов</p></td>
</tr>
<tr class="odd">
<td><p>макролист</p></td>
<td><p>Список макросов</p></td>
</tr>
<tr class="even">
<td><p>модулелист</p></td>
<td><p>Список модулей</p></td>
</tr>
<tr class="odd">
<td><p>ViewList</p></td>
<td><p>Список представлений</p></td>
</tr>
<tr class="even">
<td><p>сторедпроцедурелист</p></td>
<td><p>Список хранимых процедур</p></td>
</tr>
<tr class="odd">
<td><p>датабаседиаграмлист</p></td>
<td><p>Список схем базы данных</p></td>
</tr>
</tbody>
</table>

<br/>

В приведенном ниже примере показано, как можно открыть форму "сотрудники" в образце базы данных Northwind из процедуры Visual Basic:

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

## <a name="the-table-topic"></a>В этой статье описывается таблица

В этих разделах используется следующий синтаксис:

_DatabaseName_ ; **Таблица** _имя_таблицы_

_DatabaseName_ ; **Запрос** _куеринаме_

_DatabaseName_ ; **SQL** [ _склстринг_ ]

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
<td><p><em>DatabaseName</em></p></td>
<td><p>Имя базы данных, в которой находится таблица или запрос, или к которой применяется оператор SQL, за которым следует точка с запятой (;). Имя базы данных может быть только базовым именем (Northwind) или полным путем и MDB-расширением (К:\акцесс\самплес\норсвинд.МДБ).</p></td>
</tr>
<tr class="even">
<td><p><em>TableName</em></p></td>
<td><p>Имя существующей таблицы.</p></td>
</tr>
<tr class="odd">
<td><p><em>куеринаме</em></p></td>
<td><p>Имя существующего запроса.</p></td>
</tr>
<tr class="even">
<td><p><em>склстринг</em></p></td>
<td><p>Допустимая инструкция SQL длиной до 256 символов, заканчивающаяся точкой с запятой. Для обмена данными с более чем 256 символами опустите этот аргумент и используйте последовательные операторы <strong>ддепоке</strong> для создания оператора SQL. Например, в приведенном ниже коде Visual Basic используется оператор <strong>ддепоке</strong> для создания оператора SQL и запроса результатов запроса.</p></td>
</tr>
</tbody>
</table>

<br/>

В следующей таблице приведены допустимые элементы для ТАБЛИЦ *TableName*, Query *куеринаме*и SQL *склстринг* .

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Item</p></th>
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
<td><p>Список имен полей с одной строкой.</p></td>
</tr>
<tr class="even">
<td><p>"FieldNames"; Д</p></td>
<td><p>Список из двух строк с именами полей (первая строка) и их типы данных (вторая строка).</p>
<p>Возвращаемые значения:</p>
<p>Значение</p>
<p><ul>
<li>нуль</li>
<li>1,1</li>
<li>2</li>
<li>4</li>
<li>4 </li>
<li>5 </li>
<li>6 </li>
<li>7 </li>
<li>8 </li>
<li>9 </li>
<li>10 </li>
<li>11 </li>
<li>12 </li>
</ul>
</p>
</td>
</tr>
<tr class="even">
<td><p>некстров</p></td>
<td><p>Данные в следующей строке таблицы или запроса. При открытии канала Некстров возвращает данные из первой строки. Если текущая строка является последней и вы запускаете Некстров, запрос завершается с ошибкой.</p></td>
</tr>
<tr class="odd">
<td><p>превров</p></td>
<td><p>Данные из предыдущей строки таблицы или запроса. Если Превров является первым запросом в новом канале, возвращаются данные из последней строки таблицы или запроса. Если первая запись является текущей строкой, запрос для Превров завершается с ошибкой.</p></td>
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
<td><p>фиелдкаунт</p></td>
<td><p>Число полей в таблице или запросе.</p></td>
</tr>
<tr class="odd">
<td><p>SQLText</p></td>
<td><p>Оператор SQL, представляющий таблицу или запрос. Для таблиц этот элемент возвращает инструкцию SQL в форме &quot;выбор `*` из <em>таблицы</em>; &quot;.</p></td>
</tr>
<tr class="even">
<td><p>Склтекст; <em>n</em></p></td>
<td><p>Оператор SQL в <em>n</em>-символьных фрагментах, представляющий таблицу или запрос, где <em>n</em> — целое число до 256. Например, предположим, что запрос представлен следующей инструкцией &quot;SQL: элемент склтекст; 7&quot; возвращает следующие фрагменты, разделенные табуляцией: элемент &quot;склтекст; 7&quot; возвращает следующие разделенные табуляцией блоки:</p></td>
</tr>
</tbody>
</table>

<br/>

В приведенном ниже примере показано, как можно использовать DDE в Visual Basic для запроса данных из таблицы в образце базы данных Northwind и вставки этих данных в текстовый файл:

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
