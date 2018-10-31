---
title: Удалите оператор (Microsoft Access SQL)
TOCTitle: DROP statement (Microsoft Access SQL)
ms:assetid: a8c79c35-22da-2e6d-88b5-620eb481bb61
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821409(v=office.15)
ms:contentKeyID: 48546907
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 7622c81e9c37f1fdd2f950c16cd9d8f30caa7cac
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861395"
---
# <a name="drop-statement-microsoft-access-sql"></a>Удалите оператор (Microsoft Access SQL)

**Применимо к**: Access 2013 | Office 2013

Удаление существующей таблицы, процедуры или представления из базы данных или удаление существующего индекса из таблицы.

> [!NOTE]
> Ядро СУБД Microsoft Access не поддерживает использование ПЕРЕТАСКИВАНИЯ или любой другой инструкции DDL с базами данных, ядро базы данных Microsoft Access. Используйте метод DAO **Удалить** .

## <a name="syntax"></a>Синтаксис

ПОМЕСТИТЕ {таблицы в *таблице* | Д *индекса* ИНДЕКСА *в таблице* | ПРОЦЕДУРА *процедуры* | Просмотр *представления*}

Инструкции DROP состоит из следующих частей:

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
<td><p>Имя таблицы для удаления или таблицы, из которого удаляется индекс.</p></td>
</tr>
<tr class="even">
<td><p><em>процедура</em></p></td>
<td><p>Имя процедуры, которую необходимо удалить.</p></td>
</tr>
<tr class="odd">
<td><p><em>view</em></p></td>
<td><p>Имя представления для удаления.</p></td>
</tr>
<tr class="even">
<td><p><em>index</em></p></td>
<td><p>Имя индекса, удаляемый из <em>таблицы.</em></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

Прежде чем удалить его или удаление индекса из его необходимо закрыть таблицы.

Можно также использовать [ALTER TABLE](alter-table-statement-microsoft-access-sql.md) удаление индекса из таблицы.

[Создание таблицы](create-table-statement-microsoft-access-sql.md) можно использовать для создания таблицы и [CREATE INDEX](create-index-statement-microsoft-access-sql.md) или ALTER TABLE, чтобы создать индекс. Для изменения таблицы, используйте ALTER TABLE.

## <a name="example"></a>Пример

В следующем примере предполагается существование предполагаемую NewIndex индекса на таблице Employees базы данных Northwind.

В этом примере удаляется индекс MyIndex из таблицы сотрудников.

```vb
    Sub DropX1() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Delete NewIndex from the Employees table. 
        dbs.Execute "DROP INDEX NewIndex ON Employees;" 
     
        dbs.Close 
     
    End Sub
```

<br/>

В этом примере удаляется таблицу Employees из базы данных.

```vb
    Sub DropX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Delete the Employees table. 
        dbs.Execute "DROP TABLE Employees;" 
     
        dbs.Close 
     
    End Sub
```
