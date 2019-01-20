---
title: Предложение CONSTRAINT (Microsoft Access SQL)
TOCTitle: CONSTRAINT clause (Microsoft Access SQL)
ms:assetid: f8e89a91-a69e-1811-42a7-921692110bcb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836971(v=office.15)
ms:contentKeyID: 48548797
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277561
dev_langs:
- sql
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 356620376658bb927c690056f4de9a01554aa47e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703785"
---
# <a name="constraint-clause-microsoft-access-sql"></a>Предложение CONSTRAINT (Microsoft Access SQL)

**Область применения**: Access 2013, Office 2013

Ограничение похоже на индекс, несмотря на то, что его можно также использовать для создания связи с другой таблицей.

Вы можете использовать предложение CONSTRAINT в оператораъ [ALTER TABLE](alter-table-statement-microsoft-access-sql.md) и [CREATE TABLE](create-table-statement-microsoft-access-sql.md)для создания или удаления ограничений. Существует два типа предложений CONSTRAINT: одно для создания ограничения на отдельном поле, а другое — для создания ограничения на нескольких полях.

> [!NOTE]
> Ядро СУБД Access не поддерживает использование CONSTRAINT или любые операторы DDL с базами данных с ядром СУБД, не принадлежащими Microsoft. Используйте вместо этого методы DAO **Create**.

## <a name="syntax"></a>Синтаксис

### <a name="single-field-constraint"></a>Ограничения одного поля

CONSTRAINT *name* {PRIMARY KEY | UNIQUE | NOT NULL | REFERENCES *foreigntable* \[(*foreignfield1, foreignfield2*)\] \[ON UPDATE CASCADE | SET NULL\] \[ON DELETE CASCADE | SET NULL\]}

### <a name="multiple-field-constraint"></a>Ограничения нескольких полей

CONSTRAINT *name* {PRIMARY KEY (*primary1*\[, *primary2* \[, …\]\]) | UNIQUE (*unique1*\[, *unique2* \[, …\]\]) | NOT NULL (*notnull1*\[, *notnull2* \[, …\]\]) | FOREIGN KEY \[NO INDEX\] (*ref1*\[, *ref2* \[, …\]\]) REFERENCES *foreigntable* \[(*foreignfield1* \[, *foreignfield2* \[, …\]\])\] \[ON UPDATE CASCADE | SET NULL\] \[ON DELETE CASCADE | SET NULL\]}

Предложение CONSTRAINT состоит из следующих частей:

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
<td><p><em>name</em></p></td>
<td><p>Имя ограничения, которое необходимо создать.</p></td>
</tr>
<tr class="even">
<td><p><em>primary1</em>, <em>primary2</em></p></td>
<td><p>Имя поля или полей, которые будут назначены для первичного ключа.</p></td>
</tr>
<tr class="odd">
<td><p><em>unique1</em>, <em>unique2</em></p></td>
<td><p>Имя поля или полей, которые будут назначены для уникального ключа.</p></td>
</tr>
<tr class="even">
<td><p><em>notnull1, notnull2</em></p></td>
<td><p>Имя поля или полей, которые ограничены значениями, отличными от Null.</p></td>
</tr>
<tr class="odd">
<td><p><em>ref1</em>, <em>ref2</em></p></td>
<td><p>Имя поля или полей внешнего ключа, который ссылается на поля в другой таблице.</p></td>
</tr>
<tr class="even">
<td><p><em>foreigntable</em></p></td>
<td><p>Имя внешней таблицы, содержащей одно или несколько полей, заданных <em>foreignfield</em>.</p></td>
</tr>
<tr class="odd">
<td><p><em>foreignfield1</em>, <em>foreignfield2</em></p></td>
<td><p>Имя поля или полей в <em>foreigntable</em>, определяемых <em>ref1</em>, <em>ref2</em>. Это предложение можно опустить, если поле, на которое ссылаются, представляет собой первичный ключ <em>foreigntable</em>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Комментарии

Используйте синтаксис для ограничения одного поля в предложении, определяющем поле, оператора ALTER TABLE или CREATE TABLE непосредственно после спецификации типа данных поля.

Используйте данный синтаксис для ограничения нескольких полей в случае, когда вы используете зарезервированное слово CONSTRAINT за пределами определяющего поле предложение в операторе ALTER TABLE или CREATE TABLE.

С помощью CONSTRAINT можно назначить поле в качестве одного из следующих типов ограничений:

- Чтобы указать поле в качестве уникального ключа можно использовать зарезервированное слово UNIQUE. Это значит, что две записей в таблице не могут иметь одно и то же значение в этом поле. Вы можете задать ограничение для любого поля или списка полей как уникальные. Если ограничение для множества полей используется в качестве уникального ключа, объединенные значения всех полей в индексе должны быть уникальными, даже если две или более записи имеют одно значение в одном из полей.

- С помощью зарезервированного слова PRIMARY KEY можно назначить одно поле или набор полей в таблице в качестве первичного ключа. Все значения в первичном ключе должны быть уникальными и не быть равными **Null**, а для таблицы может быть только один первичный ключ.
    
  > [!NOTE]
  > Не используйте ограничение PRIMARY KEY в таблице, в которой уже есть первичный ключ; если вы сделаете это, возникнет ошибка.

- С помощью зарезервированного слова FOREIGN KEY можно назначить поле в качестве внешнего ключа. Если первичный ключ внешней таблицы состоит из нескольких полей, необходимо использовать определение ограничения для нескольких полей со списком всех полей со ссылками, имя внешней таблицы и названия полей со ссылками во внешней таблице в том же порядке, в каком перечислены поля со ссылками. Если поле или поля со ссылками представляют собой первичный ключ внешней таблицы, вы не можете указать поля со ссылками. По умолчанию ядро СУБД выступает так, как если бы первичный ключ внешней таблицы выступает в виде полей со ссылками. Ограничения внешнего ключа указывают определенные действия, которые необходимо выполнить при изменении соответствующего значения первичного ключа:

- Вы можете указать действия для выполнения для внешней таблицы с учетом соответствующего действия, выполняемого для первичного ключа в таблице, в котором содержится определение CONSTRAINT. Например, вы можете использовать следующие определения для таблицы Клиенты:
    
  ``` sql
    CREATE TABLE Customers (CustId INTEGER PRIMARY KEY, CLstNm NCHAR VARYING (50))
  ```
    
  Учитывайте следующее определение таблицы Заказы, которое определяет отношение внешнего ключа, ссылающегося на первичный ключ таблицы Клиенты.
    
  ``` sql
    CREATE TABLE Orders (OrderId INTEGER PRIMARY KEY, CustId INTEGER, OrderNotes NCHAR VARYING (255), CONSTRAINT FKOrdersCustId FOREIGN KEY (CustId) REFERENCES Customers ON UPDATE CASCADE ON DELETE CASCADE
  ```
    
  ON UPDATE CASCADE и ON DELETE CASCADE определяются на для внешнего ключа. Предложение ON UPDATE CASCADE означает, что если в таблице клиентов обновляется идентификатор клиента (CustId), будет выполняться каскадное обновление таблицы Заказы. Каждый заказ, содержащий соответствующее значение идентификатора клиента, будет автоматически обновляться с новым значением. Предложение ON DELETE CASCADE означает, что если клиент удаляется из таблицы Клиенты, все строки в таблице Заказы, содержащие то же значение идентификатора клиента, также будут удалены. Рассмотрите ниже разное определение таблицы Заказы, используя действие SET NULL, а не действие CASCADE:
  
  ``` sql
    CREATE TABLE Orders (OrderId INTEGER PRIMARY KEY, CustId INTEGER, OrderNotes NCHAR VARYING (255), CONSTRAINT FKOrdersCustId FOREIGN KEY (CustId) REFERENCES Customers ON UPDATE SET NULL ON DELETE SET NULL
  ```
    
  Предложении ON UPDATE SET NULL означает, что при обновлении идентификатора клиента (CustId) в таблице Клиенты, для соответствующих значений внешнего ключа из таблицы Заказы будет автоматически установлено значение NULL. Предложение ON DELETE SET NULL означает, что при удалении клиента из таблицы Клиенты, для всех соответствующих внешних ключей в таблице Заказы будет автоматически установлено значение NULL.

Чтобы предотвратить автоматическое создание индексов для внешних ключей, можно использовать модификатор NO INDEX. Данная форма определения внешнего ключа должна применяться только в случаях, где получаемые в результате значения индекса часто будет дублироваться. Если значения в индексе внешнего ключа часто дублируются, использование индекса может быть менее эффективным, чем простое выполнение сканирования таблицы. Поддержания данного типа индекса со строками, вставляемыми и удаляемым из таблицы, ухудшает производительность и не дает никаких преимуществ.

## <a name="example"></a>Пример

В этом примере создается новая таблица с именем ThisTable и двумя текстовыми полями.

```vb 
 Sub CreateTableX1()    
Dim dbs As Database 
 
    ' Modify this line to include the path to Northwind 
    ' on your computer. 
    Set dbs = OpenDatabase("Northwind.mdb") 
 
    ' Create a table with two text fields. 
    dbs.Execute "CREATE TABLE ThisTable " _ 
        & "(FirstName CHAR, LastName CHAR);" 
 
    dbs.Close 
 
End Sub
```

<br/>

В этом примере создается новая таблица с именем MyTable с двумя текстовыми поля, полем даты и времени и уникальным индексом, состоящим из всех трех полей.

```vb
    Sub CreateTableX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
     
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Create a table with three fields and a unique 
        ' index made up of all three fields. 
        dbs.Execute "CREATE TABLE MyTable " _ 
            & "(FirstName CHAR, LastName CHAR, " _ 
            & "DateOfBirth DATETIME, " _ 
            & "CONSTRAINT MyTableConstraint UNIQUE " _ 
            & "(FirstName, LastName, DateOfBirth));" 
     
        dbs.Close 
     
    End Sub
```

<br/>

В этом примере создается новая таблица с двумя текстовыми полями и полем **Integer**. Поле SSN является первичным ключом.

```vb
    Sub CreateTableX3() 
     
         Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Create a table with three fields and a primary 
        ' key. 
        dbs.Execute "CREATE TABLE NewTable " _ 
            & "(FirstName CHAR, LastName CHAR, " _ 
            & "SSN INTEGER CONSTRAINT MyFieldConstraint " _ 
            & "PRIMARY KEY);" 
     
        dbs.Close 
     
    End Sub
```

<br/>

