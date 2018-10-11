---
title: CREATE INDEX Statement (Microsoft Access SQL)
TOCTitle: CREATE INDEX Statement (Microsoft Access SQL)
ms:assetid: c5919ef4-a08d-df06-7078-5331adbcb45c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823109(v=office.15)
ms:contentKeyID: 48547612
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277562
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ab501348d19ad8577bf1a55a3f37c6c3923381b1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480157"
---
# <a name="create-index-statement-microsoft-access-sql"></a>CREATE INDEX Statement (Microsoft Access SQL)

**Применимо к**: Access 2013 | Office 2013

Создает новый индекс на существующей таблицы.

> [!NOTE]
> Для баз данных Microsoft Access atabse модуль ядро базы данных Microsoft Access не поддерживает использование CREATE INDEX (за исключением создания псевдоиндекса на связанная таблица ODBC) и любых других инструкций языка (DDL). Используйте методы создания DAO. Для получения дополнительных сведений см.

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

В необязательном с предложения, вы можете принудительно правила проверки данных. Вы можете выполнить указанные ниже действия.

- Запретить Null записей в одном или нескольких индексированных полях для новых записей с помощью параметра DISALLOW NULL.

- Запретить **пустые** записи в индексированные поля или полей, включенных в индекс с помощью параметра IGNORE NULL.

- Назначьте индексированных полей или поля в качестве первичного ключа с помощью ОСНОВНОЙ зарезервированным словом. Это означает, что ключ является уникальным, поэтому можно опустить УНИКАЛЬНЫЙ зарезервированным словом.

CREATE INDEX можно использовать для создания псевдоиндекса в связанной таблицы в источник данных ODBC, например Microsoft® SQL Server™, который не имеет индекса. Нет необходимости разрешения и доступ к удаленному серверу для создания псевдоиндекса и удаленной базы данных не и не затрагиваются псевдоиндекса. Используйте тот же синтаксис для связанных и оригинальных таблиц. Создание виртуального индекса в таблице, которая будет использоваться только для чтения может быть особенно полезным.

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
