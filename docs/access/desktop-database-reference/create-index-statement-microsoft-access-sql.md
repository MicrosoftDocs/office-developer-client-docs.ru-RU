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
localization_priority: Priority
ms.openlocfilehash: 46bc0a50e31555189c069e0ee09c4c84349c04c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295431"
---
# <a name="create-index-statement-microsoft-access-sql"></a>Инструкция CREATE INDEX (Microsoft Access SQL)

**Область применения**: Access 2013, Office 2013

Создает новый индекс в существующей таблице.

> [!NOTE]
> Ядро СУБД Microsoft Access не поддерживает использование CREATE INDEX (кроме как для создания псевдоиндекса в связанной таблице ODBC) или любых других инструкций DDL с базами данных, которые не основаны на ядре СУБД Microsoft Access. Используйте вместо этого методы DAO **Create**. Дополнительные сведения см. в разделе "Примечания".

## <a name="syntax"></a>Синтаксис

CREATE \[ UNIQUE \] INDEX *индекс* ON *таблица* (*поле* \[ASC|DESC\]\[, *поле* \[ASC|DESC\], …\]) \[WITH { PRIMARY | DISALLOW NULL | IGNORE NULL }\]

Инструкция CREATE INDEX включает в себя следующие элементы:

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
<td><p><em>индекс</em></p></td>
<td><p>Имя создаваемого индекса.</p></td>
</tr>
<tr class="even">
<td><p><em>таблица</em></p></td>
<td><p>Имя существующей таблицы, в которой будет создан индекс.</p></td>
</tr>
<tr class="odd">
<td><p><em>поле</em></p></td>
<td><p>Имя одного или нескольких полей для индексации. Чтобы создать индекс по одному полю, укажите имя поля в круглых скобках после имени таблицы. Чтобы создать индекс по нескольким полям, укажите имена всех полей, включаемых в индекс. Чтобы создать индексы с упорядочением по убыванию, используйте зарезервированное слово DESC; в противном случае будут созданы индексы с упорядочением по возрастанию.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Чтобы запретить появление повторяющихся значений в одном или нескольких индексированных полях, используйте зарезервированное слово UNIQUE.

Чтобы определить правила проверки данных, можно использовать необязательное предложение WITH. Вы можете выполнить указанные ниже действия.

- Запретить значения NULL в индексированных полях новых записей с помощью параметра DISALLOW NULL.

- Предотвратить индексирование записей со значениями **NULL** в одном или нескольких индексированных полях с помощью параметра IGNORE NULL.

- Определить одно или несколько индексированных полей в качестве первичного ключа с помощью зарезервированного слова PRIMARY. Поскольку подразумевается, что первичный ключ уникален, зарезервированное слово UNIQUE можно опустить.

Инструкция CREATE INDEX может быть использована для создания псевдоиндекса в связанной таблице источника данных ODBC, такого как Microsoft SQL Server, если в ней еще нет индекса. Для создания псевдоиндекса не требуется разрешения или доступа к удаленному серверу, а на удаленном сервере никак не отразится наличие псевдоиндекса. Для связанных и исходных таблиц используется один и тот же синтаксис. Особенно полезным может быть создание псевдоиндекса в таблице, которая будет использоваться преимущественно для чтения.

Чтобы добавить индекс по одному полю или по набору полей в таблице, можно также воспользоваться инструкцией [ALTER TABLE](alter-table-statement-microsoft-access-sql.md). Чтобы удалить индекс, созданный с помощью инструкции ALTER TABLE или CREATE INDEX, можно воспользоваться инструкцией ALTER TABLE или [DROP](drop-statement-microsoft-access-sql.md).

> [!NOTE]
> Если в таблице уже есть первичный ключ, не используйте зарезервированное слово PRIMARY при создании в ней нового индекса: это приведет к ошибке.

## <a name="example"></a>Пример

В этом примере создается индекс, состоящий из полей Home Phone (Домашний телефон) и Extension (Расширение) в таблице Employees (Сотрудники).

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

В этом примере создается индекс в таблице Customers (Клиенты) с помощью поля CustomerID (КодКлиента). Никакие две записи не могут содержать одинаковые данные в поле CustomerID (КодКлиента), и не допускаются значения NULL.

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
