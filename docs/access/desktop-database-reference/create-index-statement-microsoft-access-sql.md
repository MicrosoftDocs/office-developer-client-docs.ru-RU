---
title: Инструкция CREATE INDEX (Microsoft Access SQL)
TOCTitle: CREATE INDEX statement (Microsoft Access SQL)
ms:assetid: c5919ef4-a08d-df06-7078-5331adbcb45c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823109(v=office.15)
ms:contentKeyID: 48547612
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277562
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7710dd89a645b10d20044e2eeaeb26986730c843
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861556"
---
# <a name="create-index-statement-microsoft-access-sql"></a>Инструкция CREATE INDEX (Microsoft Access SQL)

**Применимо к**: Access 2013 | Office 2013

Создает новый индекс на существующей таблицы.

> [!NOTE]
> Для баз данных ядра базы данных Microsoft Access ядро базы данных Microsoft Access не поддерживает использование CREATE INDEX (за исключением создания псевдоиндекса на связанная таблица ODBC) и любых других инструкций языка (DDL). Используйте методы **Создания DAO** . Для получения дополнительных сведений см.

## <a name="syntax"></a>Синтаксис

Создание \[ UNIQUE \] д *индекса* ИНДЕКСА *в таблице* (*поле* \[ASC | DESC\]\[, *поле* \[ASC | DESC\],... \]) \[WITH {ОСНОВНОЙ | DISALLOW NULL | ПРОПУСК NULL}\]

Инструкция CREATE INDEX состоит из следующих частей:

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
<td><p><em>index</em></p></td>
<td><p>Имя индекс, который требуется создать.</p></td>
</tr>
<tr class="even">
<td><p><em>table</em></p></td>
<td><p>Имя существующей таблицы, которая будет содержать индекс.</p></td>
</tr>
<tr class="odd">
<td><p><em>поля</em></p></td>
<td><p>Имя поля для индексирования. Чтобы создать индекс по одному полю, укажите имя поля в скобках после имени таблицы. Чтобы создать составной индекс, укажите имена всех полей, включаемых в индекс. Для создания индексов по убыванию используйте слово DESC; в противном случае индексов предполагается, что будет по возрастанию.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

Чтобы запретить повторяющиеся значения в одном или нескольких индексированных полей различные записи, используйте УНИКАЛЬНОЕ зарезервированным словом.

В необязательном с предложения может задать правила проверки данных. Вы можете выполнить указанные ниже действия.

- Запретить Null записей в одном или нескольких индексированных полях для новых записей с помощью параметра DISALLOW NULL.

- Запретить **пустые** записи в индексированные поля или полей, включенных в индекс с помощью параметра IGNORE NULL.

- Назначьте индексированных полей или поля в качестве первичного ключа с помощью ОСНОВНОЙ зарезервированным словом. Это означает, что ключ является уникальным, поэтому можно опустить УНИКАЛЬНЫЙ зарезервированным словом.

CREATE INDEX можно использовать для создания псевдоиндекса в связанной таблицы в источник данных ODBC, например Microsoft SQL Server, который не имеет индекса. Нет необходимости разрешения и доступ к удаленному серверу для создания псевдоиндекса и удаленной базы данных не и не затрагиваются псевдоиндекса. Используйте тот же синтаксис для связанных и оригинальных таблиц. Создание виртуального индекса в таблице, которая будет использоваться только для чтения может быть особенно полезным.

Можно также использовать инструкцию [ALTER](alter-table-statement-microsoft-access-sql.md) для добавления одного или нескольких полей индекса в таблицу и инструкцию ALTER или инструкции [DROP](drop-statement-microsoft-access-sql.md) можно использовать для удаления индекса, созданных с помощью ALTER TABLE или CREATE INDEX.

> [!NOTE]
> Не используйте ОСНОВНОЙ зарезервированным словом при создании нового индекса в таблице, уже имеет первичный ключ; в противном случае возникает ошибка.

## <a name="example"></a>Пример

В этом примере создается индекс, состоящий из поля домашний телефон и расширение в таблице сотрудников.

```vb
    Sub CreateIndexX1() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Create the NewIndex index on the Employees table. 
        dbs.Execute "CREATE INDEX NewIndex ON Employees " _ 
            & "(HomePhone, Extension);" 
     
        dbs.Close 
     
    End Sub 
```

<br/>

В этом примере создается индекса на таблице Customers, с помощью поля CustomerID. Две записи не могут иметь те же данные в поле CustomerID и значения Null не разрешены.

```vb
    Sub CreateIndexX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Create a unique index, CustID, on the  
        ' CustomerID field. 
        dbs.Execute "CREATE UNIQUE INDEX CustID " _ 
            & "ON Customers (CustomerID) " _ 
            & "WITH DISALLOW NULL;" 
     
        dbs.Close 
     
    End Sub
```
