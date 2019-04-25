---
title: Метод Database.OpenRecordset (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: a243bc79-cac4-fe12-768d-d3d017954e78
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820966(v=office.15)
ms:contentKeyID: 48546753
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052939
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 73bb48db5b47ff1824e962ac44324a17ae0636ad
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294841"
---
# <a name="databaseopenrecordset-method-dao"></a>Метод Database.OpenRecordset (DAO)

**Область применения**: Access 2013 | Office 2013

Создает новый объект **[Recordset](recordset-object-dao.md)** и добавляет его в коллекцию **Recordsets**.

## <a name="syntax"></a>Синтаксис

*выражение* .OpenRecordset(_**Name**_, _**Type**_, _**Options**_, _**LockEdit**_)

*выражение*: переменная, представляющая объект **Database**.

## <a name="parameters"></a>Параметры

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя</p></th>
<th><p>Обязательный/необязательный</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Источник записей для нового объекта <strong>Recordset</strong>. Источником может быть имя таблицы, имя запроса или оператор SQL, возвращающий записи. Для объектов <strong>Recordset</strong> табличного типа в базах данных ядра СУБД Microsoft Access источником может быть только имя таблицы.</p></td>
</tr>
<tr class="even">
<td><p><em>Type</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Константа <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong>, которая указывает на то, какой тип объекта <strong>Recordset</strong> нужно открыть.</p><p><strong>ПРИМЕЧАНИЕ</strong>: при открытии <strong>Recordset</strong> в рабочей области Microsoft Access, если вы не указали тип, <strong>OpenRecordset</strong> создает табличный тип <strong>Recordset</strong>, если возможно. Вы укажете связанную таблицу или запрос, <strong>OpenRecordset</strong> создаст объект <strong>Recordset</strong> типа dynaset.</p>
</td>
</tr>
<tr class="odd">
<td><p><em>Options</em></p></td>
<td><p>Необязательно</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Сочетание констант <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong>, которые указывают характеристики нового объекта <strong>Recordset</strong>.</p><p><strong>ПРИМЕЧАНИЕ</strong>. Константы <strong>dbConsistent</strong> и <strong>dbInconsistent</strong> являются взаимоисключающими, и использование обеих констант вызывает ошибку. Предоставление аргумента LockEdit, когда в качестве аргумента Options используется константа <strong>dbReadOnly</strong>, также приводит к возникновению ошибки.</p>
</td>
</tr>
<tr class="even">
<td><p><em>LockEdit</em></p></td>
<td><p>Необязательно</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Константа <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong>, определяющая блокировку <strong>Recordset</strong>.</p><p><strong>ПРИМЕЧАНИЕ</strong>. Вы можете использовать <strong>dbReadOnly</strong> в аргументе Options или в аргументе LockedEdit, но не одновременно. Если вы используете его для обоих аргументов, возникает ошибка во время выполнения.</p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Возвращаемое значение

Recordset

## <a name="remarks"></a>Примечания

Обычно если у пользователя возникает эта ошибка во время обновления записи, код должен обновлять содержимое полей и возвращать измененные значения. Если ошибка возникает при удалении записи, код может отобразить для пользователя данные новой записи и сообщение о недавнем изменении данных. В этот момент код может запросить у пользователя подтверждение удаления записи.

Вы также можете использовать константу **dbSeeChanges** при открытии **Recordset** в рабочей области ODBC, подключенной к ядру СУБД Microsoft Access для таблицы Microsoft SQL Server 6.0 (или более поздней версии), содержащей столбец IDENTITY, в противном случае может возникать ошибка.

Открытие нескольких объектов **Recordset** для источника данных ODBC может привести к завершению работы, так как подключение будет занято предыдущим вызовом **OpenRecordset**. Один из способов решения этой проблемы состоит в полном заполнении **Recordset** с помощью метода **MoveLast** непосредственно после открытия **Recordset**.

Закрытие **Recordset** с помощью метода **[Close](connection-close-method-dao.md)** автоматически удаляет его из коллекции **Recordsets**.


> [!NOTE]
> Если *источник* ссылается на оператор SQL, состоящий из строки, объединенной с нецелочисленным значением, а параметры системы содержат десятичные символы, не используемые в США, например, запятую (пример, strSQL = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), возникает ошибка при попытке открытия **Recordset**. Это возникает по причине того, что при объединении число будет преобразовано в строку с помощью используемого по умолчанию в вашей системе десятичного символа, а SQL поддерживает только десятичные символы, используемые в США.

**Ссылка, предоставляемая** сообществом [UtterAccess](https://www.utteraccess.com). UtterAccess — это премиальный вики-портал и форум, посвященный Microsoft Access.

- [Перенос данных из Access в Excel](https://www.utteraccess.com/forum/transfer-data-access-ex-t1672619.html)

## <a name="example"></a>Пример

В приведенном ниже примере показано, как открыть объект Recordset на основании запроса параметра.

**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    Dim dbs As DAO.Database
    Dim qdf As DAO.QueryDef
    Dim rst As DAO.Recordset
    
    Set dbs = CurrentDb
    
    'Get the parameter query
    Set qfd = dbs.QueryDefs("qryMyParameterQuery")
    
    'Supply the parameter value
    qdf.Parameters("EnterStartDate") = Date
    qdf.Parameters("EnterEndDate") = Date + 7
    
    'Open a Recordset based on the parameter query
    Set rst = qdf.OpenRecordset()
```

<br/>

В приведенном ниже примере показано, как открыть объект Recordset на основании таблицы или запроса.

```vb 
    Dim dbs As DAO.Database
    Dim rsTable As DAO.Recordset
    Dim rsQuery As DAO.Recordset
    
    Set dbs = CurrentDb
    
    'Open a table-type Recordset
    Set rsTable = dbs.OpenRecordset("Table1", dbOpenTable)
    
    'Open a dynaset-type Recordset using a saved query
    Set rsQuery = dbs.OpenRecordset("qryMyQuery", dbOpenDynaset)
```

<br/>

В приведенном ниже примере показано, как открыть объект Recordset на основании оператора SQL.

```vb
    Dim dbs As DAO.Database
    Dim rsSQL As DAO.Recordset
    Dim strSQL As String
    
    Set dbs = CurrentDb
    
    'Open a snapshot-type Recordset based on an SQL statement
    strSQL = "SELECT * FROM Table1 WHERE Field2 = 33"
    Set rsSQL = dbs.OpenRecordset(strSQL, dbOpenSnapshot)
```

<br/>

В примере ниже показано, как использовать свойство Filter для определения записей, которые нужно включить в открываемый впоследствии объект Recordset.

```vb
    Dim dbs As DAO.Database
    Dim rst As DAO.Recordset
    Dim rstFiltered As DAO.Recordset
    Dim strCity As String
    
    Set dbs = CurrentDb
    
    'Create the first filtered Recordset, returning customer records
    'for those visited between 30-60 days ago.
    Set rest = dbs.OpenRecordset(_ 
        "SELECT * FROM Customers WHERE LastVisitDate BETWEEN Date()-60 " & _
        "AND Date()-30 ORDER BY LastVisitDate DESC")
    
    'Begin row processing
    Do While Not rst.EOF
        
        'Retrieve the name of the first city in the selected rows
        strCity = rst!City
    
        'Now filter the Recordset to return only the customers from that city
        rst.Filter = "City = '" & strCity & "'"
        Set rstFiltered = rst.OpenRecordset
    
        'Process the rows
        Do While Not rstFiltered.EOF
            rstFiltered.Edit
            rstFiltered!ToBeVisited = True
            rstFiltered.Update
            rstFiltered.MoveNext
        Loop
    
        'We've done what was needed. Now exit
        Exit Do
        rst.MoveNext
       
    Loop
    
    'Cleanup
    rstFiltered.Close
    rst.Close
    
    Set rstFiltered = Nothing
    Set rst = Nothing
```



