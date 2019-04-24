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
localization_priority: Priority
ms.openlocfilehash: 7beda04d1f18014101f00078de1d125c1fd67a69
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314569"
---
# <a name="sql-subqueries-microsoft-access-sql"></a>Вложенные запросы SQL (Microsoft Access SQL)


**Область применения**: Access 2013, Office 2013

Вложенный запрос - это оператор [SELECT](select-statement-microsoft-access-sql.md), вложенный в оператор [SELECT…INTO](select-into-statement-microsoft-access-sql.md), [INSERT…INTO](insert-into-statement-microsoft-access-sql.md), [DELETE](delete-statement-microsoft-access-sql.md) или [UPDATE](update-statement-microsoft-access-sql.md) или в другой вложенный запрос.

## <a name="syntax"></a>Синтаксис

Вы можете использовать три формы синтаксиса для создания вложенного запроса:

*сравнение* \[ANY | ALL | SOME \] (*sqlstatement*)

*выражение* \[NOT\] IN (*sqlstatement*)

\[NOT\] EXISTS (*sqlstatement*)

Вложенный запрос состоит из следующих частей:

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
<td><p><em>сравнение</em></p></td>
<td><p>Выражение и оператор сравнения, который сравнивает выражение с результатами вложенного запроса.</p></td>
</tr>
<tr class="even">
<td><p><em>выражение</em></p></td>
<td><p>Выражение, для которого выполняется поиск по набору результатов для вложенного запроса.</p></td>
</tr>
<tr class="odd">
<td><p><em>sqlstatement</em></p></td>
<td><p>Оператор SELECT с тем же форматом и правилами, что и любой другой оператор SELECT. Его необходимо включать в скобки.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Вы можете использовать вложенный запрос вместо выражения в списке полей оператора SELECT или предложении [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) или [HAVING](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/having-clause-microsoft-access-sql). Во вложенном запросе вы используете оператор SELECT для предоставления набора одного или нескольких определенных значений для оценки в выражении для предложения WHERE или HAVING.

Используйте предикат ANY или SOME, которые являются синонимами, для получения записей в основном запросе, который удовлетворяет сравнению с любыми записями, полученными во вложенном запросе. Следующий пример возвращает все продукты, для которых цена за единицу выше, чем у любого продукта, продаваемого со скидкой 25 процентов или более:

```sql
SELECT * FROM Products 
WHERE UnitPrice > ANY 
(SELECT UnitPrice FROM OrderDetails 
WHERE Discount >= .25);
```

Используйте предикат [ALL](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/all-distinct-distinctrow-top-predicates-microsoft-access-sql) для получения записей в основном запросе, который удовлетворяет сравнению со всеми записями, полученными во вложенном запросе. Если вы изменили предикат с ANY на ALL в предыдущем примере, запрос будет возвращать только те продукты, у которых цена за единицу больше, чем у всех продуктов, проданных со скидкой 25 процентов или более. Это гораздо более строгое ограничение.

Используйте предикат IN для получения только тех записей в основном запросе, для которых определенная запись во вложенном запросе содержит одинаковое значение. В примере ниже возвращаются все продукты со скидкой 25 процентов или больше:

```sql
SELECT * FROM Products 
WHERE ProductID IN 
(SELECT ProductID FROM OrderDetails 
WHERE Discount >= .25);
```

С другой стороны, вы можете использовать NOT IN для получения только тех записей в основном запросе, для которых ни одна запись во вложенном запросе не содержит одинаковое значение.

Используйте предикат EXISTS (с необязательным зарезервированным словом NOT) в сравнениях ИСТИНА/ЛОЖЬ, чтобы определить, возвращает ли вложенный запрос какие-либо записи.

Также можно использовать псевдонимы имени таблицы во вложенном запросе для ссылки на таблицы, указанные в предложении [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql) за пределами вложенного запроса. Пример ниже возвращает имена сотрудников, чья заработная плата равна или выше средней заработной платы всех сотрудников на аналогичной должности. Для таблицы "Сотрудники" присваивается псевдоним "T1":

```sql
SELECT LastName,
FirstName, Title, Salary 
FROM Employees AS T1 
WHERE Salary >= (SELECT Avg(Salary) 
FROM Employees 
WHERE T1.Title = Employees.Title) Order by Title;
```

В приведенном выше примере зарезервированное слово AS не является обязательным.

Некоторые вложенные запросы поддерживаются в перекрестных запросах, в частности, в качестве предикатов (например в предложении WHERE). Вложенные запросы в виде выходных данных (в списке SELECT) не поддерживаются в перекрестных запросах.

## <a name="example"></a>Пример

В данном примере перечислены имена и контактные данные каждого клиента, разместившего заказ во втором квартале 1995 года. В этом примере выполняется вызов процедуры EnumFields, которую можно найти в примере для оператора SELECT.

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
