---
title: INSERT INTO Statement (Microsoft Access SQL)
TOCTitle: INSERT INTO Statement (Microsoft Access SQL)
ms:assetid: d3e44258-79f2-caba-8629-bde03f898f2d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834799(v=office.15)
ms:contentKeyID: 48547918
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277575
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 751d2e2747a2d3b9aac4a0d36b8fac11a60c418f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481786"
---
# <a name="insert-into-statement-microsoft-access-sql"></a>INSERT INTO Statement (Microsoft Access SQL)

**Применимо к**: Access 2013 | Office 2013

Добавление одной или нескольких записей в таблицу. Это называется запрос.

## <a name="syntax"></a>Синтаксис

Запрос на добавление нескольких записей

Вставка в *целевой* \[(*field1*\[, *поле2*\[,... \] \])\] \[В *внешняя_база_данных* \] ВЫБЕРИТЕ \[ *источника*. \] *field1*\[, *поле2*\[,... \] Из *выражение_таблиц*

Запрос на добавление одной записи

Вставка в *целевой* \[(*field1*\[, *поле2*\[,... \] \])\] Значения (*значение1*\[, *значение2*\[,... \])

Инструкция INSERT INTO состоит из следующих частей:

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
<td><p><em>target</em></p></td>
<td><p>Имя таблицы или запроса для добавления записей.</p></td>
</tr>
<tr class="even">
<td><p><em>field1</em>, <em>field2</em></p></td>
<td><p>Имена полей для добавления данных, если после <em>конечного</em> аргумент или имена полей для получения данных из, если следующий аргумент <em>источника</em> .</p></td>
</tr>
<tr class="odd">
<td><p><em>внешняя_база_данных</em></p></td>
<td><p>Путь к внешней базе данных. Описание пути в разделе <a href="https://msdn.microsoft.com/library/ff194542(v=office.15)">в</a> предложение.</p></td>
</tr>
<tr class="even">
<td><p><em>source</em></p></td>
<td><p>Имя таблицы или запроса для копирования записей.</p></td>
</tr>
<tr class="odd">
<td><p><em>выражение_таблиц</em></p></td>
<td><p>Имя таблицы или таблиц, из которого извлекаются. Этот аргумент может быть имя одной таблицы или результирующее из операцию <a href="inner-join-operation-microsoft-access-sql.md">INNER JOIN</a>, <a href="left-join-right-join-operations-microsoft-access-sql.md">LEFT JOIN</a>или <a href="left-join-right-join-operations-microsoft-access-sql.md">RIGHT JOIN</a> или сохраненный запрос.</p></td>
</tr>
<tr class="even">
<td><p><em>значение1</em>, <em>значение2</em></p></td>
<td><p>Значения для вставки в определенных полях новую запись. Каждое значение вставляется в поле, соответствующее значение позиции в списке: <em>значение1</em> вставляется в <em>field1</em> новую запись, <em>значение2</em> в <em>поле2</em>и т. д. Необходимо разделять их запятыми значения и заключать текстовые поля в кавычки ("").</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

Инструкция INSERT INTO можно использовать для добавления одной записи в таблицу с помощью синтаксиса запроса Добавление одной записи, как показано выше. В этом случае код указывает имя и значение для каждого поля записи. Необходимо указать все поля из записи, который будет назначен значение и значение для этого поля. В каждом поле не указан, значение по умолчанию, или **значение Null,** вставляется для отсутствующих столбцов. Записи добавляются в конец таблицы.

Вставка в можно также использовать для добавления набора записей из другой таблицы или запроса с помощью ВЫБЕРИТЕ... FROM, как показано выше в синтаксисе запроса на добавление нескольких записей. В этом случае предложение SELECT задает поля для добавления в указанный *целевой* таблицы.

В таблице *или *целевых* * можно указать таблицы или запроса. Если запрос указан, ядро базы данных Microsoft Access добавляет записей все таблицы, указанные в запросе.

Вставка в является необязательным, но при включении, предшествует оператор [SELECT](select-statement-microsoft-access-sql.md) .

Если конечная таблица содержит основной ключ, убедитесь что добавьте уникальный, не являющиеся —**значение Null,** со значениями в поле первичного ключа или поля; Если вы не задан, ядро базы данных Microsoft Access не будет добавлять записи.

Если при добавлении записей в таблицу с полем счетчика и требуется изменить нумерацию добавленных записей, не включайте поле счетчика в запросе. Включите поле счетчика в запрос, если требуется сохранить исходные значения поля.

Используйте предложение для добавления записей в таблицу в другой базе данных.

Чтобы создать новую таблицу, используйте [Выбор... В](select-into-statement-microsoft-access-sql.md) оператор вместо этого для создания запроса на создание таблицы.

Чтобы определить, какие записи будут добавлены до выполнения запроса на добавление, выполнение и просмотр результатов запроса select, которое использует же критерии выбора.

Запрос копирует записей из одной или нескольких таблиц в другое. Запрос на добавление не влияет на таблицы, которые содержат записи, которые необходимо добавить.

Вместо добавления существующих записей из другой таблицы, можно указать значение для каждого поля в отдельной новой записи с помощью предложения значения. Если список полей опускается, предложение значения необходимо включить значение для каждого поля в таблице. в противном случае операция вставки завершится с ошибкой. Используйте дополнительные инструкции INSERT INTO с предложением значения для каждой дополнительной записи, которую требуется создать.

**Автор ссылки** [UtterAccess](https://www.utteraccess.com) сообщества. UtterAccess — это премьер форум вики-сайт и Справка по Microsoft Access.

  - [Создание последовательных номеров для инструкций INSERT/UPDATE](https://www.utteraccess.com/forum/generating-sequential-num-t446039.html)

  - [SQL форматирования данных VBA](https://www.utteraccess.com/forum/sql-vba-formatter-t1165308.html)

## <a name="example"></a>Пример

В этом примере выбирает все записи в таблице предполагаемую новых клиентов и добавляет их в таблице Customers. Когда отдельных столбцов не определен, имена столбцов в таблице ВЫБЕРИТЕ должны совпадать точно в вставки в таблице.

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

В этом примере создается новая запись в таблицу Employees.

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

