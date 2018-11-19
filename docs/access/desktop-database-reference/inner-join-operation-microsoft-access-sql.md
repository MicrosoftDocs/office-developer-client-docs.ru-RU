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
ms.openlocfilehash: e4179087408a9f7a68bccc673bcd456305ba41d5
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026486"
---
# <a name="inner-join-operation-microsoft-access-sql"></a>Операция INNER JOIN (Microsoft Access SQL)


**Применимо к**: Access 2013, Office 2013


Объединяет записи из двух таблиц при каждом содержат одинаковые значения общего поля.

## <a name="syntax"></a>Синтаксис

ИЗ внутреннего СОЕДИНЕНИЯ *table1* *Таблица2* на *table1*. *field1* *оператор_сравнения Таблица2*. *поле2*

Операция INNER JOIN состоит из следующих частей:

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
<td><p><em>table1</em>, <em>Таблица2</em></p></td>
<td><p>Имена таблиц, из которых объединяются записи.</p></td>
</tr>
<tr class="even">
<td><p><em>field1</em>, <em>field2</em></p></td>
<td><p>Имена полей, входящих в состав. Если они не числовое, поля должны быть тот же тип данных и содержат одинаковые данные, но нет необходимости с одинаковыми именами.</p></td>
</tr>
<tr class="odd">
<td><p><em>оператор_сравнения</em></p></td>
<td><p>Любой оператор сравнения: &quot;=,&quot; &quot; &lt;,&quot; &quot; &gt;,&quot; &quot; &lt;=,&quot; &quot; &gt;=,&quot; или &quot; &lt; &gt;.&quot;</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Можно использовать операцию INNER JOIN в [любой FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql) . Это наиболее распространенный тип объединения. Объединение записей из двух таблиц всякий раз, когда они соответствуют в поле обеих таблицах.

Можно использовать INNER JOIN с таблицами отделов и сотрудников для выбора всех сотрудников в каждого подразделения. С другой стороны чтобы выбрать все отделы (даже если некоторые имеют нет сотрудников) или всех сотрудников (даже если некоторые не назначены отделом), можно использовать операцию [LEFT JOIN или RIGHT JOIN](left-join-right-join-operations-microsoft-access-sql.md) для создания внешнего соединения.

При попытке объединить поля, содержащие данные Memo или OLE-объектов, возникает ошибка.

Можно объединить два числовых поля из как типы. Например можно объединить для счетчика и много полей, так как они являются как типы. Тем не менее не может присоединиться к Single и Double типов полей.

В следующем примере показано, как можно объединить таблицы категорий и продуктов в поле Идентификатор категории:

```sql
SELECT CategoryName, ProductName 
FROM Categories INNER JOIN Products 
ON Categories.CategoryID = Products.CategoryID;
```

В предыдущем примере идентификатор категории — это поле объединения, но не включенный в выходных данных запроса, так как он не включен в операторе [SELECT](select-statement-microsoft-access-sql.md) . Чтобы включить поле объединения, добавьте имя поля в операторе SELECT — в данном случае Categories.CategoryID.

Также можно связать несколько предложений ON в операторе JOIN, используя следующий синтаксис:

ВЫБЕРИТЕ из *поля* *table1* INNER JOIN *Таблица2* д *table1*. *field1* *оператор_сравнения* *Таблица2*. *field1* И на *table1*. *поле2* *оператор_сравнения* *Таблица2*. *поле2*) ИЛИ на *table1*. *поле3* *оператор_сравнения* *Таблица2*. *поле3*) \];

Кроме того, можно вкладывать инструкций СОЕДИНЕНИЯ, используя следующий синтаксис:

ВЫБЕРИТЕ из *поля* *table1* INNER JOIN (*Таблица2* INNER JOIN \[( \] *Таблица3* \[INNER JOIN \[( \] *tablex* \[INNER JOIN...) \] На *Таблица3*. *поле3* *оператор_сравнения* *tablex*. *fieldx*) \] На *Таблица2*. *поле2* *оператор_сравнения* *Таблица3*. *поле3*) НА *table1*. *field1* *оператор_сравнения* *Таблица2*. *поле2*;

LEFT JOIN или RIGHT JOIN может быть вложена в ВНУТРЕННЕЕ соединение, но ВНУТРЕННЕЕ соединение не могут быть вложены внутри LEFT JOIN или RIGHT JOIN.

## <a name="example"></a>Пример

В этом примере создается два эквивалентные соединения: один между сведения о заказе и заказы таблиц между таблицами заказы и сотрудников. Это необходимо, так как в таблице сотрудников не содержит данные о продажах и в таблице сведения о заказе не содержит данные о сотрудниках. Запрос создает список сотрудников и общего объема продаж.

В этом примере вызывается процедура EnumFields, которые можно найти в примере инструкции SELECT.

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
