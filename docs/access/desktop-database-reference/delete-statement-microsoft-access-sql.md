---
title: Удалите оператор (Microsoft Access SQL)
TOCTitle: DELETE statement (Microsoft Access SQL)
ms:assetid: 64c235bc-5b1a-0a33-714a-9933ba7a81e5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195097(v=office.15)
ms:contentKeyID: 48545299
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277573
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7e41e7597a967e7029cb3ce6ae120bb382714288
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25864125"
---
# <a name="delete-statement-microsoft-access-sql"></a>Удалите оператор (Microsoft Access SQL)

**Применимо к**: Access 2013 | Office 2013

Создает запрос на удаление удаляет записи из одной или нескольких таблиц, перечисленных в предложении [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql) , которые удовлетворяют предложения [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) .

## <a name="syntax"></a>Синтаксис

Удаление \[ *в таблице*. \* \] Из *таблицы* WHERE *критериев*

Оператор DELETE состоит из следующих частей:

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
<td><p>Необязательное имя таблицы, из которой удаляются записи.</p></td>
</tr>
<tr class="even">
<td><p><em>table</em></p></td>
<td><p>Имя таблицы, из которой удаляются записи.</p></td>
</tr>
<tr class="odd">
<td><p><em>критерии</em></p></td>
<td><p>Выражение, которое определяет, какие записи для удаления.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

УДАЛИТЬ особенно полезна, если вы хотите удалить несколько записей.

Чтобы удалить всю таблицу из базы данных, можно использовать метод **Execute** с помощью инструкции [DROP](drop-statement-microsoft-access-sql.md) . При удалении таблицы, однако структура будут потеряны. С другой стороны при использовании DELETE, удаляется только данные; Структура таблицы и все ее свойства, такие как атрибуты полей и индексы, остаются без изменений.

Удалить можно использовать для удаления записи из таблицы, которые находятся в один ко многим отношения с другими таблицами. Операции каскадного удаления приводят записей в таблицах, которые находятся на разные стороны отношения к удалению при удалении соответствующей записи в одной части отношения в запросе. Например в связи между таблицами, клиенты таблицы с одной стороны, находится в таблице заказов на стороне много отношения. Удаление записи из результатов клиентов в соответствующие записи заказы, удаляется, если параметр каскадного удаления указанного.

Запрос на удаление удаляет все записи, не данных в определенных полях. Если вы хотите удалить значения конкретного поля, создайте запрос на обновление, которое изменяет значения в **Null**.

> [!IMPORTANT]
> - После удаления записей с помощью запроса на удаление, нельзя отменить операцию. Необходимо знать, какие записи будут удалены, выполните результатов выберите запрос, который использует тем же условиям и затем запустите запроса на удаление.
> - Создавать резервные копии данных в любое время. При удалении неверный записей, их можно восстановить из резервной копии.

## <a name="example"></a>Пример

В этом примере удаляются все записи для сотрудников с должностью ученик. Если предложение FROM содержит только одну таблицу, нет необходимости списка имя таблицы в инструкции DELETE.

```vb
    Sub DeleteX() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Delete employee records where title is Trainee.     
        dbs.Execute "DELETE * FROM " _ 
            & "Employees WHERE Title = 'Trainee';" 
         
        dbs.Close 
     
    End Sub
```
