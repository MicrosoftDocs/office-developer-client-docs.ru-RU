---
title: Предложение ограничения (Microsoft Access SQL)
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
ms.openlocfilehash: 87870d824f9e26f601529bc60b737f1e46b12960
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863005"
---
# <a name="constraint-clause-microsoft-access-sql"></a>Предложение ограничения (Microsoft Access SQL)

**Применимо к**: Access 2013 | Office 2013

Ограничение аналогична индекса, хотя он также можно использовать для создания связи с другой таблицей.

Используйте предложение ограничения в инструкциях [CREATE TABLE](create-table-statement-microsoft-access-sql.md) и [ALTER TABLE](alter-table-statement-microsoft-access-sql.md) для создания или удаления ограничения. Существует два типа предложений ограничений: один для создания ограничения на одно поле и для создания ограничения на более одного поля.

> [!NOTE]
> Ядро СУБД Microsoft Access не поддерживает использование ограничения или любой другой инструкции языка определения данных (DDL), с базами данных, ядро базы данных Microsoft Access. Используйте методы DAO **Создать** .

## <a name="syntax"></a>Синтаксис

**Простые ограничения**:

ОГРАНИЧЕНИЕ *имени* {первичный ключ | УНИКАЛЬНЫЙ | NOT NULL | Справочные материалы *таблицавнешнегоключа* \[(*foreignfield1, foreignfield2*)\] \[ON UPDATE CASCADE | ЗАДАЙТЕ значение NULL,\] \[ON DELETE CASCADE | ЗАДАЙТЕ значение NULL,\]}

**Составные ограничения**:

ОГРАНИЧЕНИЕ *имени* {первичный ключ (*primary1*\[, *primary2* \[,... \]\]) | УНИКАЛЬНЫЙ (*unique1*\[, *unique2* \[,... \]\]) | NOT NULL (*notnull1*\[, *notnull2* \[,... \]\]) | ВНЕШНИЙ ключ \[без ИНДЕКСА\] (*аргументов ссылка1*\[, *ref2* \[,... \] \]) Ссылки *таблицавнешнегоключа* \[(*foreignfield1* \[, *foreignfield2* \[,... \] \])\] \[ON UPDATE CASCADE | ЗАДАЙТЕ значение NULL,\] \[ON DELETE CASCADE | ЗАДАЙТЕ значение NULL,\]}

Предложение ограничения состоит из следующих частей:

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
<td><p>Имя ограничения будет создан.</p></td>
</tr>
<tr class="even">
<td><p><em>primary1</em>, <em>primary2</em></p></td>
<td><p>Имя поля или полей, определяемых первичный ключ.</p></td>
</tr>
<tr class="odd">
<td><p><em>unique1</em>, <em>unique2</em></p></td>
<td><p>Имя поля или полей, определяемых как уникальный ключ.</p></td>
</tr>
<tr class="even">
<td><p><em>notnull1 notnull2</em></p></td>
<td><p>Имя поля, которые ограничены непустых значений.</p></td>
</tr>
<tr class="odd">
<td><p><em>аргументов ссылка1</em>, <em>ref2</em></p></td>
<td><p>Имя поля внешнего ключа или полей, которые ссылаются на поля в другой таблице.</p></td>
</tr>
<tr class="even">
<td><p><em>таблицавнешнегоключа</em></p></td>
<td><p>Имя внешнего таблицы, содержащей поле или поля, указанного идентификатором <em>foreignfield</em>.</p></td>
</tr>
<tr class="odd">
<td><p><em>foreignfield1</em>, <em>foreignfield2</em></p></td>
<td><p>Имя поля в <em>таблицавнешнегоключа</em> , указанного идентификатором <em>аргументов ссылка1</em>, <em>ref2</em>. Это предложение можно опустить, если указанное поле первичный ключ <em>таблицавнешнегоключа</em>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

Используйте следующий синтаксис для простых ограничений в предложении определения поля инструкции ALTER TABLE или CREATE TABLE сразу после спецификации тип данных.

Используйте синтаксис для составные ограничения при использовании зарезервированным словом ограничение за пределами предложение определение поля в оператор ALTER TABLE или CREATE TABLE.

Использование ограничения можно назначить полю один из следующих типов ограничений:

- УНИКАЛЬНЫЙ зарезервированным словом можно использовать для назначения поля в качестве уникального ключа. Это означает, что две записи в таблице может иметь такое же значение в этом поле. Можно ограничить все поля или список полей как уникальный. Если составные ограничения используется в качестве уникального ключа, объединенные значения всех полей в индексе должно быть уникальным, даже в том случае, если две или более записи с таким же значением в одном из полей.

- ПЕРВИЧНЫЙ ключ зарезервированные слова можно использовать для назначения одного поля или набор полей в таблице в качестве первичного ключа. Все значения в первичный ключ должно быть уникальным и не **может быть Null**и может существовать только один первичный ключ для таблицы.
    
  > [!NOTE]
  > Не задано ограничение первичный ключ в таблице, уже имеет первичный ключ; в противном случае возникает ошибка.

- ВНЕШНИЙ ключ для зарезервированные слова используются для назначения поля в качестве внешнего ключа. Если первичный ключ внешней таблицы состоит из нескольких полей, необходимо использовать определении ограничения нескольких полей со списком всех ссылающиеся поля, имя внешней таблицы и имена указанного поля в таблице внешнего в том же порядке что перечислены ссылающиеся поля. Если указанного поля или поля таблицы внешнего первичный ключ, не нужно указывать поля, который указывает ссылка. По умолчанию ядро базы данных происходит так, как в случае первичный ключ таблицы внешнего указанного поля. Ограничения внешнего ключа задают конкретные действия, выполняемые при изменении значения соответствующего первичного ключа:

- Можно указать действий, выполняемых на основании соответствующих действий, выполняемых на первичный ключ в таблице, на котором определяется ограничение таблицы внешнего. Например рассмотрим следующее определение для таблицы клиентов.
    
  ``` sql
    CREATE TABLE Customers (CustId INTEGER PRIMARY KEY, CLstNm NCHAR VARYING (50))
  ```
    
  Рассмотрим следующее определение таблицы Orders, в котором определяется внешнего ключа ссылки на первичный ключ в таблице клиентов.
    
  ``` sql
    CREATE TABLE Orders (OrderId INTEGER PRIMARY KEY, CustId INTEGER, OrderNotes NCHAR VARYING (255), CONSTRAINT FKOrdersCustId FOREIGN KEY (CustId) REFERENCES Customers ON UPDATE CASCADE ON DELETE CASCADE
  ```
    
  Предложение ON DELETE CASCADE и ON UPDATE CASCADE определены для внешнего ключа. Предложения ON CASCADE обновление означает, что если идентификатора клиента (CustId) обновляется в таблице клиентов, обновление будет каскадным таблицы заказов. Каждый заказ, содержащий соответствующее значение идентификатора клиента будут автоматически обновлены с новым значением. Предложение ON DELETE CASCADE означает, что при удалении клиента из таблицы Клиент все строки в таблице Orders, содержащий то же значение идентификатора клиента также будут удалены. Рассмотрим следующие различные определения таблицы Orders с использованием действия SET NULL вместо действия CASCADE.
  
  ``` sql
    CREATE TABLE Orders (OrderId INTEGER PRIMARY KEY, CustId INTEGER, OrderNotes NCHAR VARYING (255), CONSTRAINT FKOrdersCustId FOREIGN KEY (CustId) REFERENCES Customers ON UPDATE SET NULL ON DELETE SET NULL
  ```
    
  Предложение ON UPDATE SET NULL означает, что если идентификатора клиента (CustId) обновляется в таблице клиентов, соответствующие значения внешнего ключа в таблице Orders автоматически устанавливается значение NULL. Аналогично предложение ON DELETE SET NULL означает, что при удалении клиента из таблицы Клиент все соответствующие внешние ключи в таблице Orders автоматически устанавливается значение NULL.

Чтобы запретить автоматическое создание индексов для внешних ключей, можно использовать модификатор NO INDEX. Определение внешнего ключа в этой форме можно использовать только в тех случаях, где результирующего значения индексов будут часто повторяться. Где часто повторяющихся значений в индексе внешнего ключа, с помощью индекса может быть менее эффективным, чем просто сканирование таблицы. Сохранение такого индекса, со строками вставлен и удалены из таблицы снижает производительность и не предоставляет никаких преимуществ.

## <a name="example"></a>Пример

В этом примере создается новая таблица с именем ThisTable с двух текстовых полей.

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

В этом примере создается новая таблица с именем MyTable с двух текстовых полей, поля даты/времени и уникальный индекс, состоящих из всех трех полей.

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

В этом примере создается новая таблица с двух текстовых полей и **целого** поля. В поле SSN — основной ключ.

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

