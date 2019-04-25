---
title: Инструкция ALTER TABLE (Microsoft Access SQL)
TOCTitle: ALTER TABLE statement (Microsoft Access SQL)
ms:assetid: 78e6c92c-e88c-e55f-6b89-435360c166a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196148(v=office.15)
ms:contentKeyID: 48545763
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277560
dev_langs:
- sql
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: b8bd9abac3aee8be8fe52e555fcd5247e804f258
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297160"
---
# <a name="alter-table-statement-microsoft-access-sql"></a>Инструкция ALTER TABLE (Microsoft Access SQL)

**Область применения**: Access 2013, Office 2013

Служит для изменения макета таблицы после того, как она была создана с помощью инструкции [CREATE TABLE](create-table-statement-microsoft-access-sql.md).

> [!NOTE]
> Ядро СУБД Microsoft Access не поддерживает использование ALTER TABLE или любых других инструкций DDL с базами данных, которые не основаны на Microsoft Access. Используйте вместо этого методы DAO **Create**.

## <a name="syntax"></a>Синтаксис

ALTER TABLE *таблица* {ADD {COLUMN *тип поля*\[(*размер*)\] \[NOT NULL\] \[CONSTRAINT *индекс*\] | ALTER COLUMN *тип поля*\[(*размер*)\] | CONSTRAINT *индекс_набора_полей*} | DROP {COLUMN *поле* I CONSTRAINT *имя_индекса*} }

Инструкция ALTER TABLE включает в себя следующие элементы:

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
<td><p><em>таблица</em></p></td>
<td><p>Имя таблицы, которую требуется изменить.</p></td>
</tr>
<tr class="even">
<td><p><em>поле</em></p></td>
<td><p>Имя поля, которое будет добавлено в <em>таблицу</em>, удалено из нее или изменено в ней.</p></td>
</tr>
<tr class="odd">
<td><p><em>тип</em></p></td>
<td><p>Тип данных <em>поля</em>.</p></td>
</tr>
<tr class="even">
<td><p><em>размер</em></p></td>
<td><p>Размер поля в знаках (только для полей с типом данных TEXT и BINARY).</p></td>
</tr>
<tr class="odd">
<td><p><em>индекс</em></p></td>
<td><p>Индекс <em>поля</em>. Дополнительные сведения о создании этого индекса см. в статье, посвященной <a href="constraint-clause-microsoft-access-sql.md">предложению CONSTRAINT</a>.</p></td>
</tr>
<tr class="even">
<td><p><em>индекс_набора_полей</em></p></td>
<td><p>Индекс набора полей, добавляемых в <em>таблицу</em>. Дополнительные сведения о создании этого индекса см. в статье, посвященной <a href="constraint-clause-microsoft-access-sql.md">предложению CONSTRAINT</a>.</p></td>
</tr>
<tr class="odd">
<td><p><em>имя_индекса</em></p></td>
<td><p>Имя удаляемого индекса набора полей.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Изменить существующую таблицу с помощью инструкции ALTER TABLE можно несколькими способами. Вы можете выполнить указанные ниже действия.

- Добавить поле в таблицу, используя инструкцию ADD COLUMN. Требуется указать имя поля и тип данных. Для полей с типом данных TEXT и BINARY можно также указать размер. Например, следующая инструкция добавляет поле Notes с типом данных TEXT размером 25 знаков в таблицу Employees:
    
  ```sql
    ALTER TABLE Employees ADD COLUMN Notes TEXT(25)
  ```
    
  Для этого поля можно также указать индекс. Дополнительные сведения об индексах одного поля см. в статье, посвященной [предложению CONSTRAINT](constraint-clause-microsoft-access-sql.md).
    
  Если для поля определено свойство NOT NULL, поле обязательно должно содержать допустимые данные.

- Изменить тип данных для существующего поля, используя инструкцию ALTER COLUMN. Требуется указать имя поля и новый тип данных. Для полей с типом данных TEXT и BINARY можно также указать размер. Например, следующая инструкция в таблице Employees изменит тип данных поля ZipCode (начальный тип данных — INTEGER) на тип данных TEXT размером 10 знаков:
    
  ```sql
    ALTER TABLE Employees ALTER COLUMN ZipCode TEXT(10)
  ```

- Добавить индекс набора полей, используя инструкцию ADD CONSTRAINT. Дополнительные сведения об индексах набора полей см. в статье, посвященной [предложению CONSTRAINT](constraint-clause-microsoft-access-sql.md).

- Удалить поле, используя инструкцию DROP COLUMN. Требуется указать только имя поля.

- Использовать DROP CONSTRAINT, чтобы удалить индекс набора полей. Требуется указать только имя индекса после зарезервированного слова CONSTRAINT.


> [!NOTE] 
> - Невозможно одновременно добавить или удалить несколько полей или индексов.
> - Чтобы добавить индекс для одного поля или для набора полей в таблице, используйте инструкцию [CREATE INDEX](create-index-statement-microsoft-access-sql.md). Чтобы удалить индекс, созданный с помощью инструкции ALTER TABLE или CREATE INDEX, можно использовать инструкцию ALTER TABLE или [DROP](drop-statement-microsoft-access-sql.md).
> - Свойство NOT NULL можно задавать для одного поля или внутри именованного предложения CONSTRAINT для одного или нескольких полей. Свойство NOT NULL для поля можно задать только один раз. Попытка определить это свойство повторно приведет к ошибке выполнения.

## <a name="example"></a>Пример

В этом примере добавляется поле Salary (Заработная плата) с типом данных **Money** в таблицу Employees (Сотрудники).

```vb
    Sub AlterTableX1() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Add the Salary field to the Employees table  
        ' and make it a Money data type. 
        dbs.Execute "ALTER TABLE Employees " _ 
            & "ADD COLUMN Salary MONEY;" 
     
        dbs.Close 
     
    End Sub 
```

<br/>

В этом примере тип данных поля Salary (Заработная плата) изменяется с **Money** на **Char**.

```vb
    Sub AlterTableX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Add the Salary field to the Employees table  
        ' and make it a Money data type. 
        dbs.Execute "ALTER TABLE Employees " _ 
            & "ALTER COLUMN Salary CHAR(20);" 
     
        dbs.Close 
     
    End Sub 
```

<br/>

В этом примере удаляется поле Salary (Заработная плата) из таблицы Employees (Сотрудники).

```vb
    Sub AlterTableX3() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Delete the Salary field from the Employees table. 
        dbs.Execute "ALTER TABLE Employees " _ 
            & "DROP COLUMN Salary;" 
     
        dbs.Close 
     
    End Sub
```

<br/>

В этом примере добавляется внешний ключ для таблицы Orders (Заказы). Внешний ключ основан на поле EmployeeID (Код сотрудника) и ссылается на поле EmployeeID (Код сотрудника) таблицы Employees (Сотрудники). В этом примере не требуется перечислять поле EmployeeID (Код сотрудника) после таблицы Employees (Сотрудники) в предложении REFERENCES, так как EmployeeID — это первичный ключ таблицы Employees (Сотрудники).

```vb
    Sub AlterTableX4() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Add a foreign key to the Orders table. 
        dbs.Execute "ALTER TABLE Orders " _ 
            & "ADD CONSTRAINT OrdersRelationship " _ 
            & "FOREIGN KEY (EmployeeID) " _ 
            & "REFERENCES Employees (EmployeeID);" 
     
        dbs.Close 
     
    End Sub 
```

<br/>

В этом примере удаляется внешний ключ из таблицы Orders (Заказы).

```vb
    Sub AlterTableX5() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Remove the OrdersRelationship foreign key from 
        ' the Orders table. 
        dbs.Execute "ALTER TABLE Orders " _ 
            & "DROP CONSTRAINT OrdersRelationship;" 
     
        dbs.Close 
     
    End Sub
```
