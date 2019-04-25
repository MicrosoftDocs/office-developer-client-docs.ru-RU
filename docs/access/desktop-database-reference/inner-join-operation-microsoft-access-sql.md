---
title: Операция INNER JOIN (Microsoft Access SQL)
TOCTitle: INNER JOIN operation (Microsoft Access SQL)
ms:assetid: 8d16c74c-02c6-12b7-b180-3e7744ef65f3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197346(v=office.15)
ms:contentKeyID: 48546247
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277574
dev_langs:
- sql
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 6ff2ad40d318801ecec2332b53b41f327c20fbc5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291402"
---
# <a name="inner-join-operation-microsoft-access-sql"></a>Операция INNER JOIN (Microsoft Access SQL)


**Область применения**: Access 2013, Office 2013


Объединяет записи из двух таблиц, если в связующих полях этих таблиц содержатся одинаковые значения.

## <a name="syntax"></a>Синтаксис

FROM *таблица1* INNER JOIN *таблица2* ON *таблица1*.*поле1* *оператор_сравнения таблица2*.*поле2*

Операция INNER JOIN состоит из следующих элементов:

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
<td><p><em>таблица1</em>, <em>таблица2</em></p></td>
<td><p>Имена таблиц, содержащих объединяемые записи.</p></td>
</tr>
<tr class="even">
<td><p><em>поле1</em>, <em>поле2</em></p></td>
<td><p>Имена объединяемых полей. Поля, не являющиеся числовыми, должны относиться к одному типу данных и содержать данные одного вида. Однако имена этих полей могут быть разными.</p></td>
</tr>
<tr class="odd">
<td><p><em>оператор_сравнения</em></p></td>
<td><p>Любой оператор сравнения: &quot;=,&quot; &quot;&lt;,&quot; &quot;&gt;,&quot; &quot;&lt;=,&quot; &quot;&gt;=,&quot; или &quot;&lt;&gt;.&quot;</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Операцию INNER JOIN можно использовать в любом предложении [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql). Это самый распространенный тип объединения. С его помощью происходит объединение записей из двух таблиц по связующему полю, если оно содержит одинаковые значения в обеих таблицах.

При работе с таблицами "Отделы" и "Сотрудники" операцией INNER JOIN можно воспользоваться для выбора всех сотрудников в каждом отделе. Если же требуется выбрать все отделы (включая те из них, в которых нет сотрудников) или всех сотрудников (в том числе и не закрепленных за отделом), можно при помощи операции [LEFT JOIN или RIGHT JOIN](left-join-right-join-operations-microsoft-access-sql.md) создать внешнее соединение.

При попытке связи полей, содержащих данные типа Memo или объекты OLE, возникнет ошибка.

Можно связать любые два числовых поля аналогичных типов. Например, можно связать поля AutoNumber и Long, так как эти типы аналогичны, однако не поля Single и Double.

В следующем примере показано, как можно объединить таблицы Categories и Products по полю CategoryID.

```sql
SELECT CategoryName, ProductName 
FROM Categories INNER JOIN Products 
ON Categories.CategoryID = Products.CategoryID;
```

В предыдущем примере CategoryID является объединенным полем, но оно не включается в результаты запроса, поскольку не указано в инструкции [SELECT](select-statement-microsoft-access-sql.md). Чтобы включить объединенное поле в результаты запроса, добавьте его имя в инструкцию SELECT. В данном случае это Categories.CategoryID.

В инструкции JOIN можно также связать несколько предложений ON, используя следующий синтаксис:

SELECT *поля* FROM *поле1* INNER JOIN *таблица2* ON *таблица1*.*поле1* *оператор_сравнения* *таблица2*.*поле1* AND ON *таблица1*.*поле2* *оператор_сравнения* *таблица2*.*поле2*) OR ON *таблица1*.*поле3* *оператор_сравнения* *таблица2*.*поле3*)\];

Ниже приведен пример синтаксиса, с помощью которого можно составлять вложенные инструкции JOIN.

SELECT *поля* FROM *таблица1* INNER JOIN (*таблица2* INNER JOIN \[( \]*таблица3* \[INNER JOIN \[( \]*таблицаx* \[INNER JOIN …)\] ON *таблица3*.*поле3* *оператор_сравнения* *таблицаx*.*полеx*)\] ON *таблица2*.*поле2* *оператор_сравнения* *таблица3*.*поле3*) ON *таблица1*.*поле1* *оператор_сравнения* *таблица2*.*поле2*;

Операции LEFT JOIN и RIGHT JOIN могут быть вложены в операцию INNER JOIN, но операция INNER JOIN не может быть вложена в операцию LEFT JOIN или RIGHT JOIN.

## <a name="example"></a>Пример

В этом примере создается два уравнивающих соединения: одно между таблицами Order Details (Сведения о заказах) и Orders (Заказы), а другое между таблицами Orders (Заказы) и Employees (Сотрудники). Это необходимо, так как таблица Employees (Сотрудники) не содержит данные о продажах, а таблица Order Details (Сведения о заказах) не содержит данные сотрудников. Результат запроса представляет собой список сотрудников и их общие объемы продаж.

В этом примере вызывается процедура EnumFields, которую можно найти в примере инструкции SELECT.

```vb
    Sub InnerJoinX() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Create a join between the Order Details and  
        ' Orders tables and another between the Orders and  
        ' Employees tables. Get a list of employees and  
        ' their total sales. 
        Set rst = dbs.OpenRecordset("SELECT DISTINCTROW " _ 
            & "Sum(UnitPrice * Quantity) AS Sales, " _ 
            & "(FirstName & Chr(32) & LastName) AS Name " _ 
            & "FROM Employees INNER JOIN(Orders " _ 
            & "INNER JOIN [Order Details] " _ 
            & "ON [Order Details].OrderID = " _ 
            & "Orders.OrderID ) " _ 
            & "ON Orders.EmployeeID = " _ 
            & "Employees.EmployeeID " _ 
            & "GROUP BY (FirstName & Chr(32) & LastName);") 
         
        ' Populate the Recordset. 
        rst.MoveLast 
         
        ' Call EnumFields to print the contents of the  
        ' Recordset. Pass the Recordset object and desired 
        ' field width. 
        EnumFields rst, 20 
     
        dbs.Close 
     
    End Sub
```
