---
title: ALTER TABLE Statement (Microsoft Access SQL)
TOCTitle: ALTER TABLE Statement (Microsoft Access SQL)
ms:assetid: 78e6c92c-e88c-e55f-6b89-435360c166a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196148(v=office.15)
ms:contentKeyID: 48545763
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277560
dev_langs:
- sql
f1_categories:
- Office.Version=v15
ms.openlocfilehash: b8fc826d438973b4d079e9b90d3663ab755821cc
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482751"
---
# <a name="alter-table-statement-microsoft-access-sql"></a>ALTER TABLE Statement (Microsoft Access SQL)


**Применимо к**: Access 2013 | Office 2013



Изменяет макет таблицы после его создания с помощью инструкции [CREATE TABLE](create-table-statement-microsoft-access-sql.md) .


> [!NOTE]
> Ядро СУБД Microsoft Access не поддерживает использование ALTER TABLE или любой другой инструкции языка определения данных (DDL), с базами данных Microsoft Access. Используйте методы создания DAO.



## <a name="syntax"></a>Синтаксис

ALTER TABLE в *таблице* {ДОБАВЬТЕ {СТОЛБЦА *типа поля*\[(*размер*)\] \[NOT NULL\] \[ограничения *индекса* \] | Изменение СТОЛБЦА *типа поля*\[(*размер*)\] | ОГРАНИЧЕНИЕ *multifieldindex*} | ПОМЕСТИТЕ {СТОЛБЦА *поле* я ограничение *имя_индекса*}}

Оператор ALTER TABLE состоит из следующих частей:

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
<td><p><em>table</em></p></td>
<td><p>Имя таблицы.</p></td>
</tr>
<tr class="even">
<td><p><em>поля</em></p></td>
<td><p>Имя поля, по которому добавляется или удаляется из <em>таблицы</em>. Или же имя поля, которое будет изменено в <em>таблице</em>.</p></td>
</tr>
<tr class="odd">
<td><p><em>type</em></p></td>
<td><p>Тип данных <em>поля</em>.</p></td>
</tr>
<tr class="even">
<td><p><em>size</em>.</p></td>
<td><p>Размер поля в знаках (только текст и двоичные поля).</p></td>
</tr>
<tr class="odd">
<td><p><em>index</em></p></td>
<td><p>Индекс для <em>поля</em>. Для получения дополнительных сведений о способах создания этого индекса видеть <a href="constraint-clause-microsoft-access-sql.md">Предложение ограничения</a>.</p></td>
</tr>
<tr class="even">
<td><p><em>multifieldindex</em></p></td>
<td><p>Определение составной индекс для добавления <em>в таблицу</em>. Для получения дополнительных сведений о способах создания этого индекса видеть <a href="constraint-clause-microsoft-access-sql.md">Предложение ограничения</a>.</p></td>
</tr>
<tr class="odd">
<td><p><em>имя_индекса</em></p></td>
<td><p>Имя составной индекс требуется удалить.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

С помощью оператора изменения таблицы можно изменить существующую таблицу несколькими способами. Вы можете выполнить указанные ниже действия.

  - Используйте добавить столбец для добавления нового поля в таблице. Укажите имя поля, тип данных и (для текста и двоичный полей) требуемый размер. Например следующий оператор добавляет 25-значный текстовое поле примечания к таблице Employees.
    
    ```sql
    ALTER TABLE Employees ADD COLUMN Notes TEXT(25)
    ```
    
    Можно также определить индекс для этого поля. Дополнительные сведения для одного поля индексов можно [Предложение ограничения](constraint-clause-microsoft-access-sql.md).
    
    Если указать не значение NULL для поля новые записи должны иметь допустимые данные в этих полях.

  - Используйте ALTER COLUMN, чтобы изменить тип данных для существующего поля. Укажите имя поля, новый тип данных и требуемый размер для двоичных полей и текст. Например следующий оператор изменяет тип данных поля в таблице сотрудников, называется ZipCode (изначально определена как целое число) текстового поля 10 символов:
    
    ```sql
    ALTER TABLE Employees ALTER COLUMN ZipCode TEXT(10)
    ```

  - Используйте ограничение ADD для добавления составной индекс. Для получения дополнительных сведений о составные индексы видеть [Предложение ограничения](constraint-clause-microsoft-access-sql.md).

  - Удаление СТОЛБЦА используется для удаления поля. Указать только имя поля.

  - ПОМЕСТИТЕ ограничение используется для удаления составной индекс. Укажите следующие ограничения имя индекса зарезервированным словом.


> [!NOTE]
> <UL>
> <LI>
> <P>Не удается добавить или удалить более одного поля или индекса за раз.</P>
> <LI>
> <P>Инструкция <A href="create-index-statement-microsoft-access-sql.md">CREATE INDEX</A> можно использовать для добавления одного или нескольких полей индекса в таблицу и ALTER TABLE или инструкции <A href="drop-statement-microsoft-access-sql.md">DROP</A> можно использовать для удаления индекса, созданных с помощью ALTER TABLE или CREATE INDEX.</P>
> <LI>
> <P>НЕ NULL можно использовать на одного поля или внутри именованного предложения ограничения для одного или для нескольких полей с именем ограничения. Тем не менее можно применить к полю ограничение NOT NULL только один раз. Попытка использовать это ограничение более одного раза появлению ошибку времени выполнения.</P></LI></UL>



## <a name="example"></a>Пример

В этом примере добавляет поле заработной платы с типом данных **деньги** в таблицу Employees.

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

В этом примере изменяется поле Salary и типа данных **деньги** **знаков**типу данных.

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

В этом примере удаляется поле Salary из таблицы сотрудников.

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

В этом примере добавляется внешний ключ для таблицы Orders. Внешний ключ основано на поле EmployeeID и ссылается на поле EmployeeID таблицы «Сотрудники». В этом примере не нужно указать поле EmployeeID после таблице Employees в предложении справочные материалы, поскольку EmployeeID — это первичный ключ в таблице сотрудников.

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

В этом примере удаляется внешний ключ из таблицы заказов.

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
