---
Заголовок: использование Microsoft Access как сервер DDE TOCTitle: использование Microsoft Access как сервер DDE <<<<<<< HEAD ms:assetid: a3e82bf7-94b5-8eec-86bc-2d5387d66738 ms:mtpsurl: https://msdn.microsoft.com/library/Ff821067(v=office.15) ms:contentKeyID: 48546801 ms.date: 09/18/2015 === Описание: Microsoft Access поддерживает динамический обмен данными (DDE) как назначения (клиент) приложение или приложение источник (сервер).  
MS:AssetId: a3e82bf7-94b5-8eec-86bc-2d5387d66738 ms:mtpsurl: https://msdn.microsoft.com/library/Ff821067(v=office.15) ms:contentKeyID: 48546801 ms.date: 10/16/2018
>>>>>>> главные mtps_version: v=office.15 f1_keywords:
- vbaac10.chm5186349 f1_categories:
- Office.Version=v15
---

# <a name="use-microsoft-access-as-a-dde-server"></a>Использовать Microsoft Access в качестве сервера DDE

**Применимо к**: Access 2013 | Office 2013 

Microsoft Access поддерживает динамический обмен данными (DDE) как назначения (клиент) приложение или приложение источник (сервер). Например приложения, например Microsoft Word, действующие в качестве клиента, можно запросить данных через DDE из базы данных Microsoft Access, который используется в качестве сервера.

> [!TIP]
> Если вам требуется для работы с Microsoft Access объекты из другого приложения, можно с помощью автоматизации.

<<<<<<< HEAD DDE между клиентом и сервером устанавливается по определенной теме. Раздел может быть данные файлов в формат, поддерживаемый серверное приложение, или она может быть темы системы, который предоставляет сведения о само приложение сервера. После начала беседы по определенной теме можно перенести только элемент данных, связанный с этой теме.
=== DDE между клиентом и сервером устанавливается по определенной теме. Раздел может быть данные файлов в формат, поддерживаемый серверное приложение, или она может быть темы системы, который предоставляет сведения о само приложение сервера. После начала беседы по определенной теме можно перенести только элемент данных, связанный с этой теме.
>>>>>>> master

Например предположим, выполняется Microsoft Word и для вставки данных из конкретной базы данных Microsoft Access в документ. Начните сеанс DDE с Microsoft Access с открытия канала DDE **отношением** , указав имя файла базы данных в разделе. Затем можно перенести данные из базы данных в Microsoft Word по этому каналу.

Как сервер DDE Microsoft Access поддерживает следующие разделы:

<<<<<<< HEAD
  - В разделе системы

  - Имя базы данных (*базы данных* раздел)

  - Имя таблицы (*tablename* раздел)

  - Имя запроса (*имя запроса* раздел)

  - Строка Microsoft Access SQL (*sqlstring* раздел)

Если установлено сеанс DDE, оператор **DDEExecute** для отправки команду от клиента на сервер приложений. Если используется как сервер DDE, Microsoft Access распознает любое из указанных как действительный команду:

  - Имя макроса в текущей базе данных.

  - Все действия, которые можно выполнить в Visual Basic с помощью одного из методов **объекта** .

  - OpenDatabase и CloseDatabase действия, которые используются только для операции DDE. (Пример использования этих действий, см. пример далее в этом разделе).


> [!NOTE]
> <P>При указании действия макроса в качестве оператора <STRONG>DDEExecute</STRONG> действие и все аргументы синтаксис объекта <STRONG>DoCmd</STRONG> и должны заключаться в скобки ([]). Тем не менее приложения, поддерживающие DDE не распознает встроенные константы в операции DDE. Кроме того, строковые аргументы должны заключаться в кавычки (» «) Если строка содержит их запятыми. В противном случае кавычки, не являются обязательными.</P>



Клиентское приложение можно использовать функцию **DDERequest** к данным текст запроса из приложения сервера по каналу DDE open. Или клиент может использовать оператор **DDEPoke** для отправки данных в серверное приложение. По завершении передачи данных клиент может использовать оператор **DDETerminate** для закрытия канала DDE или оператор **DDETerminateAll** , чтобы закрыть все открытые каналы.


> [!NOTE]
> <P>По завершении клиентское приложение получает данные по каналу DDE, его следует закрыть канала для сохранения ресурсов памяти.</P>


=======
- В разделе системы

- Имя базы данных (*базы данных* раздел)

- Имя таблицы (*tablename* раздел)

- Имя запроса (*имя запроса* раздел)

- Строка Microsoft Access SQL (*sqlstring* раздел)

После установки вы сеанс DDE, оператор **DDEExecute** для отправки команду от клиента на сервер приложений. Если используется как сервер DDE, Microsoft Access распознает любое из указанных как действительный команду:

- Имя макроса в текущей базе данных.

- Все действия, которые можно выполнить в Visual Basic с помощью одного из методов **объекта** .

- OpenDatabase и CloseDatabase действия, которые используются только для операции DDE. (Пример использования этих действий, см. пример далее в этом разделе).

> [!NOTE]
> При указании действия макроса в качестве оператора **DDEExecute** действие и все аргументы синтаксис объекта **DoCmd** и должны заключаться в скобки ([]). Тем не менее приложения, поддерживающие DDE не распознает встроенные константы в операции DDE. Кроме того, строковые аргументы должны заключаться в кавычки (» «) Если строка содержит их запятыми. В противном случае кавычки, не являются обязательными.

Клиентское приложение можно использовать функцию **DDERequest** к данным текст запроса из приложения сервера по каналу DDE open. Или клиент может использовать оператор **DDEPoke** для отправки данных в серверное приложение. По завершении передачи данных клиент может использовать оператор **DDETerminate** для закрытия канала DDE или оператор **DDETerminateAll** , чтобы закрыть все открытые каналы.

> [!NOTE]
> По завершении клиентское приложение получает данные по каналу DDE, его следует закрыть канала для сохранения ресурсов памяти.
>>>>>>> master

Следующий пример демонстрирует создание процедуры Microsoft Word с помощью Visual Basic, который использует Microsoft Access, что сервер DDE. (В данном примере для работы Microsoft Access должен работать под управлением.)

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

<a name="-head"></a><<<<<<< HEAD
=======
<br/>

>>>>>>> Образец, который следующих разделах представлены сведения по темам допустимый DDE, поддерживаются в Microsoft Access.

## <a name="the-system-topic"></a>В разделе системы

<<<<<<< Раздел HEAD системы — стандартный раздел для всех приложений на основе Windows Microsoft. Она предоставляет сведения по темам, поддерживаемых приложением. Для доступа к этой информации, код должен вызвать **отношением с в качестве аргумента *раздел* ** и выполните оператор **DDERequest** с одним из следующих действий, предоставленных для аргумента *элемента* .
=== С разделом системы — это стандартный раздел для всех приложений на основе Windows корпорации Майкрософт. Она предоставляет сведения по темам, поддерживаемых приложением. Для доступа к этой информации, код должен сначала вызвать **отношением с аргументом *раздел* ** и выполните оператор **DDERequest** с одним из следующих действий, предоставленных для аргумента *элемента* .
>>>>>>> master

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
<td><p>SysItems</p></td>
<td><p>Список элементов, поддерживаемых в разделе система Microsoft Access.</p></td>
</tr>
<tr class="even">
<td><p>Formats</p></td>
<td><p>Список форматов Microsoft Access можно скопировать в буфер обмена.</p></td>
</tr>
<tr class="odd">
<td><p>Status</p></td>
<td><p>&quot;«Занят»&quot; или &quot;готовы&quot;.</p></td>
</tr>
<tr class="even">
<td><p>Разделы</p></td>
<td><p>Список всех открытых баз данных.</p></td>
</tr>
</tbody>
</table>

<a name="-head"></a><<<<<<< HEAD
=======
<br/>
>>>>>>> master

В следующем примере показано использование функции **DDEInitiate** и **DDERequest** с разделом системы:

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

## <a name="the-database-topic"></a>В разделе базы данных

В разделе *базы данных* — это имя файла существующей базы данных. Можно ввести только что базовое имя (Northwind) или его путь к MDB- и расширение (C:\\доступа\\примеры\\Northwind.mdb). Начав сеанс DDE с базой данных, можно запросить список объектов в этой базе данных.

<<<<<<< HEAD

> [!NOTE]
> <P>Нельзя использовать DDE для запроса файл рабочей группы Microsoft Access.</P>


=======
> [!NOTE]
> Нельзя использовать DDE для запроса файл рабочей группы Microsoft Access.
>>>>>>> master

В разделе *База данных* поддерживает следующие элементы.

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
<td><p>TableList</p></td>
<<<<<<< HEAD
<td><p>Список таблиц.</p></td>
</tr>
<tr class="even">
<td><p>QueryList</p></td>
<td><p>Список запросов.</p></td>
</tr>
<tr class="odd">
<td><p>FormList</p></td>
<td><p>Список форм.</p></td>
</tr>
<tr class="even">
<td><p>ReportList</p></td>
<td><p>Список отчетов.</p></td>
</tr>
<tr class="odd">
<td><p>MacroList</p></td>
<td><p>Список макросов.</p></td>
</tr>
<tr class="even">
<td><p>ModuleList</p></td>
<td><p>Список модулей.</p></td>
=======
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
<td><p>Список макросов</p></td>
</tr>
<tr class="even">
<td><p>ModuleList</p></td>
<td><p>Список модулей</p></td>
>>>>>>>Образец
</tr>
<tr class="odd">
<td><p>ViewList</p></td>
<td><p>Список представлений</p></td>
</tr>
<tr class="even">
<td><p>StoredProcedureList</p></td>
<td><p>Список хранимых процедур</p></td>
</tr>
<tr class="odd">
<td><p>DatabaseDiagramList</p></td>
<td><p>Список схемы базы данных</p></td>
</tr>
</tbody>
</table>

<a name="-head"></a><<<<<<< HEAD
=======
<br/>
>>>>>>> master

В следующем примере показано, как сотрудники форму можно открыть в образце базы данных Northwind из процедуры Visual Basic:

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

## <a name="the-table-topic"></a>В разделе таблицы

В этих разделах используйте следующий синтаксис:

_имя базы данных_ ; **В ТАБЛИЦЕ** _TableName_

_имя базы данных_ ; **Запрос** _имя запроса_

_имя базы данных_ ; **SQL** [ _sqlstring_ ]

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
<td><p><em>Имя базы данных</em></p></td>
<td><p>Имя базы данных, таблицы или запроса или, которое применяется инструкции SQL, а затем точка с запятой (;). Имя базы данных может быть только что базовое имя (Northwind) или его полный путь к MDB- и расширение (C:\Access\Samples\Northwind.mdb).</p></td>
</tr>
<tr class="even">
<td><p><em>TableName</em></p></td>
<td><p>Имя существующей таблицы.</p></td>
</tr>
<tr class="odd">
<td><p><em>Имя запроса</em></p></td>
<td><p>Имя существующего запроса.</p></td>
</tr>
<tr class="even">
<td><p><em>SqlString</em></p></td>
<td><p>Допустимая инструкция SQL не должна превышать 256 знаков, конечные точки с запятой. Exchange более 256 символов, определяющее и вместо использования последовательных <strong>DDEPoke</strong> операторов для создания инструкции SQL. Например следующий код Visual Basic используется оператор <strong>DDEPoke</strong> построение инструкции SQL и затем запросить результаты запроса.</p></td>
</tr>
</tbody>
</table>

<br/>

В следующей таблице перечислены допустимые элементы для таблицы *tablename*, ЗАПРОСА *имя запроса*и разделы *sqlstring* SQL.

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
<td><p>Все данные в таблице, в том числе имена полей.</p></td>
</tr>
<tr class="even">
<td><p>Data</p></td>
<td><p>Все строки данных без имена полей.</p></td>
</tr>
<tr class="odd">
<td><p>Списке FieldNames</p></td>
<td><p>Однострочный список имен полей.</p></td>
</tr>
<tr class="even">
<td><p>В списке FieldNames; T</p></td>
<<<<<<< HEAD
<td><p>Список полей двух строк имен (первой строки) и их данных типов (вторая строка).</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p>Далее представлены значения, возвращаемые и типы данных они представляют:</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><b>Значение</b></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p>0</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p>1</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p>2</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p>3</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p>4</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p>5</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p>6</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p>7</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p>8</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p>9</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p>10</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p>11</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p>12</p></td>
=======
<td><p>Список полей двух строк имен (первой строки) и их данных типов (вторая строка).</p>
<p>Ниже приведены возвращаемые значения:</p>
<p>Значение</p>
<p><ul>
<li>0</li>
<li>1</li>
<li>2</li>
<li>3</li>
<li>4</li>
<li>5</li>
<li>6</li>
<li>7</li>
<li>8</li>
<li>9</li>
<li>10</li>
<li>11</li>
<li>12</li>
</ul>
</p>
</td>
>>>>>>>Образец
</tr>
<tr class="even">
<td><p>NextRow</p></td>
<td><p>Данные в следующей строке таблицы или запроса. При открытии канала NextRow возвращает данные в первой строке. Если текущей строки последней записи и запустите NextRow, запрос не выполняется.</p></td>
</tr>
<tr class="odd">
<td><p>PrevRow</p></td>
<td><p>Данные в предыдущей строки в таблице или запросе. Если PrevRow первый запрос на новый канал, возвращаются данные в последней строке таблицы или запроса. Если первая запись текущей строки, не удается выполнить запрос для PrevRow.</p></td>
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
<td><p>Инструкция SQL, представляющий таблицы или запроса. Для таблиц, то возвращается инструкции SQL в виде &quot;ВЫБЕРИТЕ `*` из <em>таблицы</em>; &quot;.</p></td>
</tr>
<tr class="even">
<td><p>SQLText; <em>n</em></p></td>
<td><p>Инструкции SQL в <em>n</em>-блоки, представляющие таблицы или запроса, где <em>n</em> — целое число до 256 символов. Предположим, например, представляется с помощью следующей инструкции SQL: элемента &quot;SQLText; 7&quot; возвращает следующие блоки разделители — знаки табуляции: элемента &quot;SQLText; 7&quot; возвращает следующие блоки разделители — знаки табуляции:</p></td>
</tr>
</tbody>
</table>

<a name="-head"></a><<<<<<< HEAD
=======
<br/>
>>>>>>> master

В следующем примере показано, как использовать DDE в процедуре Visual Basic для запроса данных из таблицы в образце базы данных Northwind и вставить эти данные в текстовый файл:

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
