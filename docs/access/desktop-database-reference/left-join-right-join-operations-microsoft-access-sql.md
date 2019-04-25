---
title: Операции LEFT JOIN, RIGHT JOIN (Microsoft Access SQL)
TOCTitle: LEFT JOIN, RIGHT JOIN operations (Microsoft Access SQL)
ms:assetid: 9c10525f-98b1-fd4f-8b40-07a32c5c6502
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198084(v=office.15)
ms:contentKeyID: 48546586
ms.date: 09/18/2015
mtps_version: v=office.15
dev_langs:
- sql
localization_priority: Priority
ms.openlocfilehash: c6e37cd68d586e39a06fd650ccb453f35477253f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32290147"
---
# <a name="left-join-right-join-operations-microsoft-access-sql"></a>Операции LEFT JOIN, RIGHT JOIN (Microsoft Access SQL)

**Область применения**: Access 2013, Office 2013

Объединяют записи исходных таблиц при использовании в любом предложении [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql).

## <a name="syntax"></a>Синтаксис

FROM *таблица1* \[ LEFT | RIGHT \] JOIN *таблица2* ON *таблица1.поле1* *оператор_сравнения таблица2.поле2*

Операции LEFT JOIN и RIGHT JOIN состоят из следующих элементов:

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
<td><p>Имена объединяемых полей. Поля должны относиться к одному типу данных и содержать данные одного вида. Однако имена этих полей могут быть разными.</p></td>
</tr>
<tr class="odd">
<td><p><em>оператор_сравнения</em></p></td>
<td><p>Любой оператор сравнения: &quot;=,&quot; &quot;&lt;,&quot; &quot;&gt;,&quot; &quot;&lt;=,&quot; &quot;&gt;=,&quot; или &quot;&lt;&gt;.&quot;</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Операция LEFT JOIN создает левое внешнее соединение. С помощью левого внешнего соединения выбираются все записи первой (левой) таблицы, даже если они не соответствуют записям во второй (правой) таблице.

Операция RIGHT JOIN создает правое внешнее соединение. С помощью правого внешнего соединения выбираются все записи второй (правой) таблицы, даже если они не соответствуют записям в первой (левой) таблице.

Например, в случае с таблицами "Отделы" (левая) и "Сотрудники" (правая) можно воспользоваться операцией LEFT JOIN для выбора всех отделов (включая те, в которых нет сотрудников). Чтобы выбрать всех сотрудников (в том числе и не закрепленных за каким-либо отделом), используйте RIGHT JOIN.

В следующем примере показано, как можно объединить таблицы Categories и Products по полю CategoryID. Результат запроса представляет собой список категорий, включая те, которые не содержат товаров.

```sql
SELECT CategoryName, 
ProductName 
FROM Categories LEFT JOIN Products 
ON Categories.CategoryID = Products.CategoryID;
```

В этом примере CategoryID является объединенным полем, но оно не включается в результаты запроса, поскольку не указано в инструкции [SELECT](select-statement-microsoft-access-sql.md). Чтобы включить объединенное поле в результаты запроса, укажите его имя в инструкции SELECT. В данном случае это Categories.CategoryID.

> [!NOTE]
> - Чтобы создать запрос, результатом которого являются только те записи, для которых совпадают данные в объединенных полях, воспользуйтесь операцией [INNER JOIN](inner-join-operation-microsoft-access-sql.md).
> - Операции LEFT JOIN и RIGHT JOIN могут быть вложены в операцию INNER JOIN, но операция INNER JOIN не может быть вложена в операцию LEFT JOIN или RIGHT JOIN. Подробные сведения о вложении объединений можно найти в статье, посвященной операции INNER JOIN.
> - Вы можете связать несколько предложений ON. Сведения о связывании предложений см. в статье, посвященной операции INNER JOIN.
> - При попытке связи полей, содержащих данные типа Memo или объекты OLE, возникнет ошибка.

## <a name="example"></a>Пример

В этом примере:
- Предполагается существование гипотетических полей Department Name (Название отдела) и Department ID (Код отдела) в таблице Employees (Сотрудники). Обратите внимание, что эти поля на самом деле не существуют в таблице Employees (Сотрудники) базы данных Northwind.

- Выбираются все отделы, в том числе без сотрудников.

- Выполняется вызов процедуры EnumFields, которую можно найти в примере для инструкции SELECT.


```vb
    Sub LeftRightJoinX() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Select all departments, including those  
        ' without employees. 
        Set rst = dbs.OpenRecordset _ 
            ("SELECT [Department Name], " _ 
            & "FirstName & Chr(32) & LastName AS Name " _ 
            & "FROM Departments LEFT JOIN Employees " _ 
            & "ON Departments.[Department ID] = " _ 
            & "Employees.[Department ID] " _ 
            & "ORDER BY [Department Name];") 
         
        ' Populate the Recordset. 
        rst.MoveLast 
         
        ' Call EnumFields to print the contents of the  
        ' Recordset. Pass the Recordset object and desired 
        ' field width. 
        EnumFields rst, 20 
     
        dbs.Close 
     
    End Sub
```
