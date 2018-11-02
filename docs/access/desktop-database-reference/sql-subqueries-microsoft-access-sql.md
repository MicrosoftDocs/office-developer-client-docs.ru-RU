---
title: Вложенные запросы SQL (Microsoft Access SQL)
TOCTitle: SQL subqueries (Microsoft Access SQL)
ms:assetid: 3b6c0a5d-ab24-e1cf-0175-3f8e68c2dfbf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192664(v=office.15)
ms:contentKeyID: 48544285
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277580
dev_langs:
- sql
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 72d9d9d27ac128ec587621231b5c899bc89c2752
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925953"
---
# <a name="sql-subqueries-microsoft-access-sql"></a>Вложенные запросы SQL (Microsoft Access SQL)


**Применимо к**: Access 2013, Office 2013

Вложенный запрос — это инструкция [SELECT](select-statement-microsoft-access-sql.md) , вложенных в SELECT, [SELECT... В](select-into-statement-microsoft-access-sql.md), [Вставка... В](insert-into-statement-microsoft-access-sql.md), [Удаление](delete-statement-microsoft-access-sql.md)или [обновление](update-statement-microsoft-access-sql.md) оператор или в другой вложенный запрос.

## <a name="syntax"></a>Синтаксис

Чтобы создать вложенный запрос можно использовать три вида синтаксиса:

*Сравнение* \[ANY | ВСЕ | НЕКОТОРЫЕ\] (*sqlstatement*)

*выражение* \[Не\] в (*sqlstatement*)

\[НЕ\] EXISTS (*sqlstatement*)

Вложенный состоит из следующих частей:

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
<td><p><em>Сравнение</em></p></td>
<td><p>Выражение и оператор сравнения, сравнивает выражение с результатами подчиненного запроса.</p></td>
</tr>
<tr class="even">
<td><p><em>expression</em></p></td>
<td><p>Выражение, для которого осуществляется в наборе результатов вложенного запроса.</p></td>
</tr>
<tr class="odd">
<td><p><em>SQLStatement</em></p></td>
<td><p>Инструкция SELECT, выполнив же формат и правила как любая другая инструкция SELECT. Она должна быть включена в скобки.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Вложенный запрос можно использовать вместо выражения в списке полей инструкции SELECT или в предложении [ГДЕ](https://msdn.microsoft.com/library/ff195245\(v=office.15\)) или [HAVING](https://msdn.microsoft.com/library/ff193795\(v=office.15\)) . Во вложенном запросе используйте инструкции SELECT для предоставления набора из одного или нескольких конкретных значений для оценки в WHERE или у выражения предложения.

С помощью предиката любой или НЕКОТОРЫЕ, которые являются синонимами, извлекаются записи в главном запросе, удовлетворяющие сравнению с любыми записями, полученные на вложенный запрос. Следующий пример возвращает все продукты, цена больше, чем любого товара, проданных со скидкой от 25% и выше:

```sql
SELECT * FROM Products 
WHERE UnitPrice > ANY 
(SELECT UnitPrice FROM OrderDetails 
WHERE Discount >= .25);
```

С помощью предиката [ALL](https://msdn.microsoft.com/library/ff195711\(v=office.15\)) извлекаются только те записи в главном запросе, которые удовлетворяют сравнению со всех записей, полученных во вложенном. При изменении любой ко всем в предыдущем примере запрос возвращает только продукты, чьи цена больше всех продуктов, проданных со скидкой от 25% и выше. Это намного более жесткие.

С помощью предиката IN извлекаются только те записи в главном запросе, для которого некоторые записи во вложенном содержат одинаковые значения. Следующий пример возвращает все продукты со скидкой 25 процентов или более:

```sql
SELECT * FROM Products 
WHERE ProductID IN 
(SELECT ProductID FROM OrderDetails 
WHERE Discount >= .25);
```

С другой стороны можно использовать NOT IN извлекаются только те записи в главном запросе, для которого нет записи во вложенном содержат одинаковые значения.

Предикат EXISTS (с НЕОБЯЗАТЕЛЬНЫМ зарезервированным словом) при сравнении ИСТИНА/ЛОЖЬ для определения, является ли вложенный запрос возвращает все записи.

Можно также использовать псевдонимы таблиц во вложенном запросе для обращения к таблицам, перечисленных в предложении [FROM](https://msdn.microsoft.com/library/ff836674\(v=office.15\)) за пределами подчиненного запроса. Следующий пример возвращает имена сотрудников, зарплата которых равно или больше средней заработной платы всех сотрудников, занимающих одну должность. В таблице сотрудников задается псевдоним «Т1».

```sql
SELECT LastName,
FirstName, Title, Salary 
FROM Employees AS T1 
WHERE Salary >= (SELECT Avg(Salary) 
FROM Employees 
WHERE T1.Title = Employees.Title) Order by Title;
```

В предыдущем примере зарезервированным словом является необязательным.

Некоторые подчиненные запросы разрешены в перекрестных запросов — только в качестве предикатов (в предложении WHERE). Подчиненные запросы в качестве выходных данных (в списке SELECT) в перекрестных запросах не разрешены.

## <a name="example"></a>Пример

В этом примере перечислены имя и контактов каждого клиента, выполнившим заказа во втором квартале 1995.

В этом примере вызывается процедура EnumFields, которые можно найти в примере инструкции SELECT.

```vb
    Sub SubQueryX() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' List the name and contact of every customer  
        ' who placed an order in the second quarter of 
        ' 1995. 
        Set rst = dbs.OpenRecordset("SELECT ContactName," _ 
            & " CompanyName, ContactTitle, Phone" _ 
            & " FROM Customers" _ 
            & " WHERE CustomerID" _ 
            & " IN (SELECT CustomerID FROM Orders" _ 
            & " WHERE OrderDate Between #04/1/95#" _ 
            & " And #07/1/95#);") 
         
        ' Populate the Recordset. 
        rst.MoveLast 
         
        ' Call EnumFields to print the contents of the  
        ' Recordset. Pass the Recordset object and desired 
        ' field width. 
        EnumFields rst, 25 
     
        dbs.Close 
     
    End Sub
```
