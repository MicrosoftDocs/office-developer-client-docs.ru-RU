---
title: Инструкция INSERT INTO (Microsoft Access SQL)
TOCTitle: INSERT INTO statement (Microsoft Access SQL)
ms:assetid: d3e44258-79f2-caba-8629-bde03f898f2d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834799(v=office.15)
ms:contentKeyID: 48547918
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277575
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 4fee5e9e8878274f2c20dd83a3dbedaf2903ca62
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291335"
---
# <a name="insert-into-statement-microsoft-access-sql"></a>Инструкция INSERT INTO (Microsoft Access SQL)

**Область применения**: Access 2013, Office 2013

Эта инструкция добавляет одну или несколько записей в таблицу Это называется запросом на добавление.

## <a name="syntax"></a>Синтаксис

### <a name="multiple-record-append-query"></a>Запрос на добавление нескольких записей

INSERT INTO *конечный_объект* \[(*поле1*\[, *поле2*\[, …\]\])\] \[IN *внешняя_база_данных*\] SELECT \[*источник*.\]*поле1*\[, *поле2*\[, …\] FROM *выражение_таблицы*

### <a name="single-record-append-query"></a>Запрос на добавление одной записи

INSERT INTO *конечный_объект* \[(*поле1*\[, *поле2*\[, …\]\])\] VALUES (*значение1*\[, *значение2*\[, …\])

Инструкция INSERT INTO состоит из следующих элементов:

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
<td><p><em>конечный объект</em></p></td>
<td><p>Имя таблицы или запроса, куда добавляются записи.</p></td>
</tr>
<tr class="even">
<td><p><em>поле1</em>, <em>поле2</em></p></td>
<td><p>После аргумента <em>конечный_объект</em> — имена полей, в которые добавляются данные; после аргумента <em>источник</em> — имена полей, из которых извлекаются данные.</p></td>
</tr>
<tr class="odd">
<td><p><em>внешняя_база_данных</em></p></td>
<td><p>Путь к внешней базе данных. Описание пути см. в статье, посвященной предложению <a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-clause-microsoft-access-sql">IN</a>.</p></td>
</tr>
<tr class="even">
<td><p><em>источник</em></p></td>
<td><p>Имя таблицы или запроса, откуда копируются записи.</p></td>
</tr>
<tr class="odd">
<td><p><em>выражение_таблицы</em></p></td>
<td><p>Одно или несколько имен таблиц, из которых требуется получить записи. Этот аргумент может представлять собой имя отдельной таблицы, результирующее выражение, составленное с использованием операций <a href="inner-join-operation-microsoft-access-sql.md">INNER JOIN</a>, <a href="left-join-right-join-operations-microsoft-access-sql.md">LEFT JOIN</a> или <a href="left-join-right-join-operations-microsoft-access-sql.md">RIGHT JOIN</a>, или сохраненный запрос.</p></td>
</tr>
<tr class="even">
<td><p><em>значение1</em>, <em>значение2</em></p></td>
<td><p>Значения, которые будут добавлены в определенные поля новой записи. Каждое значение вставляется в поле, соответствующее его положению в списке: <em>значение1</em> добавляется в <em>поле1</em> новой записи, <em>значение2</em> — в <em>поле2</em> и т. д. Необходимо разделять значения запятой и заключать текстовые поля в кавычки (' ').</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

С помощью инструкции INSERT INTO можно добавить в таблицу одну запись, используя указанный выше синтаксис. В этом случае указываются имена и значения для каждого поля записи. Необходимо указать все поля записи, которым присваиваются значения, и соответствующие значения. Если не указать значение поля, ему будет присвоено значение по умолчанию или **Null**. Записи добавляются в конец таблицы.

С помощью инструкции INSERT INTO также можно добавить набор записей из другой таблицы или запроса, используя предложение SELECT... FROM, как показано выше (см. синтаксис запроса на добавление нескольких записей). В этом случае предложение SELECT задает поля для добавления в указанный *конечный_объект*.

*Источник* или *конечный_объект* может быть таблицей или запросом. Если задан запрос, ядро СУБД Microsoft Access добавляет записи ко всем таблицам, которые возвращает этот запрос.

Использование инструкции INSERT INTO не является обязательным. Если она указана, она должна предшествовать инструкции [SELECT](select-statement-microsoft-access-sql.md).

Если конечная таблица содержит первичный ключ, убедитесь, что значения, добавляемые в одно или несколько полей первичного ключа, уникальны и отличны от **NULL**. В противном случае записи не будут добавлены.

Если записи добавляются в таблицу с полем "Счетчик" и вы хотите изменить их нумерацию, не включайте поле "Счетчик" в запрос. Включите поле "Счетчик" в запрос, если вы хотите сохранить исходные значения из поля.

Добавить записи в таблицу другой базы данных можно с помощью предложения IN.

Чтобы создать таблицу, используйте инструкцию [SELECT... INTO](select-into-statement-microsoft-access-sql.md) для получения запроса на создание таблицы.

Прежде чем выполнять запрос на добавление, воспользуйтесь запросом на выборку с такими же условиями отбора, чтобы по полученным результатам определить, какие записи будут добавлены.

Запрос на добавление копирует записи из одной или нескольких таблиц в другую таблицу. При этом таблицы, содержащие добавляемые записи, остаются без изменений.

Вместо добавления записей из другой таблицы можно задать значение каждого поля в отдельной новой записи с помощью предложения VALUES. Если список полей опущен, в предложение VALUES необходимо включить соответствующие значения каждого поля таблицы; в противном случае операция INSERT не будет выполнена. Воспользуйтесь инструкцией INSERT INTO вместе с предложением VALUES для каждой дополнительной записи, которую требуется создать.

**Ссылки, предоставляемые** сообществом [UtterAccess](https://www.utteraccess.com). UtterAccess — это премиальный вики-портал и форум, посвященный Microsoft Access.

- [Создание последовательных чисел для инструкций INSERT/UPDATE](https://www.utteraccess.com/forum/generating-sequential-num-t446039.html)

- [Форматирования SQL в VBA](https://www.utteraccess.com/forum/sql-vba-formatter-t1165308.html)

## <a name="example"></a>Пример

В этом примере выбираются все записи из гипотетический таблицы New Customers, а затем они добавляются в таблицу Customers. Если отдельные столбцы не указаны, имена столбцов таблицы в инструкции SELECT должны в точности совпадать с именами столбцов таблицы в инструкции INSERT INTO.

```vb
    Sub InsertIntoX1() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Select all records in the New Customers table  
        ' and add them to the Customers table. 
        dbs.Execute " INSERT INTO Customers " _ 
            & "SELECT * " _ 
            & "FROM [New Customers];" 
             
        dbs.Close 
     
    End Sub
```

<br/>

В этом примере создается новая запись в таблице Employees.

```vb
    Sub InsertIntoX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Create a new record in the Employees table. The  
        ' first name is Harry, the last name is Washington,  
        ' and the job title is Trainee. 
        dbs.Execute " INSERT INTO Employees " _ 
            & "(FirstName,LastName, Title) VALUES " _ 
            & "('Harry', 'Washington', 'Trainee');" 
             
        dbs.Close 
     
    End Sub 
```

