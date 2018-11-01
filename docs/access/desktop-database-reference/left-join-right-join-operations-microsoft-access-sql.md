---
title: LEFT JOIN, RIGHT JOIN Operations (Microsoft Access SQL)
TOCTitle: LEFT JOIN, RIGHT JOIN Operations (Microsoft Access SQL)
ms:assetid: 9c10525f-98b1-fd4f-8b40-07a32c5c6502
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198084(v=office.15)
ms:contentKeyID: 48546586
ms.date: 09/18/2015
mtps_version: v=office.15
dev_langs:
- sql
ms.openlocfilehash: 4e2c9f8b47622bf9408d02b683af4e48d52c8662
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870529"
---
# <a name="left-join-right-join-operations-microsoft-access-sql"></a>LEFT JOIN, RIGHT JOIN Operations (Microsoft Access SQL)

**Применимо к**: Access 2013, Office 2013

Объединяет записи исходных таблиц при использовании в [любой FROM](https://msdn.microsoft.com/library/ff836674\(v=office.15\)) .

## <a name="syntax"></a>Синтаксис

ИЗ *table1* \[ влево | ПРАВО \] СОЕДИНЕНИЯ *Таблица2* на *Таблица1.поле1* *оператор_сравнения Таблица2.поле2*

Операции JOIN СЛЕВА и СПРАВА JOIN состоит из следующих частей:

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
<td><p>Имена полей, входящих в состав. Поля должны быть тот же тип данных и содержат одинаковые данные, но они не нужно с одинаковыми именами.</p></td>
</tr>
<tr class="odd">
<td><p><em>оператор_сравнения</em></p></td>
<td><p>Любой оператор сравнения: &quot;=,&quot; &quot; &lt;,&quot; &quot; &gt;,&quot; &quot; &lt;=,&quot; &quot; &gt;=,&quot; или &quot; &lt; &gt;.&quot;</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

Используйте операцию LEFT JOIN для создания левого внешнего соединения. Левые внешние соединения включают все записи из первой (левой) таблицы, даже если нет совпадающих значений для записей в таблице второй (справа).

Используйте операцию RIGHT JOIN для создания правого внешнего соединения. Правые внешние соединения включают все записи из второй (правой) таблицы, даже в том случае, если нет совпадающих значений для записей в таблице первой (левой).

Например можно использовать LEFT JOIN с отделов (слева) и сотрудникам (справа) таблицы для выбора всех отделов, включая те, которые не имеют сотрудников им. Чтобы выбрать всех сотрудников, включая те, кто не назначается отдел, используйте RIGHT JOIN.

В следующем примере показано, как можно объединить таблицы категорий и продуктов в поле Идентификатор категории. Запрос создает список всех типов, включая те, которые не содержат товаров:

```sql
SELECT CategoryName, 
ProductName 
FROM Categories LEFT JOIN Products 
ON Categories.CategoryID = Products.CategoryID;
```

В этом примере идентификатор категории — это поле объединения, но не включенный в результатах запроса, так как он не включен в операторе [SELECT](select-statement-microsoft-access-sql.md) . Чтобы включить поле объединения, введите имя поля в операторе SELECT — в данном случае Categories.CategoryID.

> [!NOTE]
> - Чтобы создать запрос, который включает в себя только записей, в которых данные в полях соединения зависит от того, используйте операцию [INNER JOIN](inner-join-operation-microsoft-access-sql.md) .
> - LEFT JOIN или RIGHT JOIN может быть вложенным в ВНУТРЕННЕЕ соединение, но ВНУТРЕННЕЕ соединение, не могут быть вложенными внутри LEFT JOIN или RIGHT JOIN. В разделе обсуждения вложения в разделе INNER JOIN, чтобы узнать, как вложить объединения.
> - Можно связать несколько предложений ON. В разделе обсуждения ссылки в разделе INNER JOIN, чтобы узнать, как это делается предложение.
> - При попытке объединить поля, содержащие данные Memo или OLE-объектов, возникает ошибка.

## <a name="example"></a>Пример

В этом примере:
- Предполагается наличие предполагаемую имя отдела и отдела идентификатор поля в таблице «Сотрудники». Обратите внимание на то, что фактически эти поля не существуют в таблице Employees базы данных Northwind.

- Выбирает все отделы, в том числе без сотрудников.

- Вызывает процедуру EnumFields, которые можно найти в примере инструкции SELECT.


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
