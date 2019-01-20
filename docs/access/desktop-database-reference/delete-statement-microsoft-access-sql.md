---
title: Оператор DELETE (Microsoft Access SQL)
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
localization_priority: Priority
ms.openlocfilehash: a4ef478e74f9851012d6f749e64b4ddb34f3a959
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715623"
---
# <a name="delete-statement-microsoft-access-sql"></a>Оператор DELETE (Microsoft Access SQL)

**Область применения**: Access 2013, Office 2013

Создает запрос на удаление, который удаляет записи из одной или нескольких таблиц, указанных в предложении [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql), отвечающих предложению [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql).

## <a name="syntax"></a>Синтаксис

DELETE \[*table*.\*\] FROM *table* WHERE *criteria*

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
<td><p><em>criteria</em></p></td>
<td><p>Выражение, определяющее, какие записи нужно удалить.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Комментарии

DELETE особенно полезен, если вы хотите удалить большое количество записей.

Чтобы удалить всю таблицу из базы данных, можно использовать метод **Execute** с оператором [DROP](drop-statement-microsoft-access-sql.md). Однако, если удалить таблицу, может потеряться структура. С другой стороны при использовании DELETE удаляются только данные; а структура таблицы и все ее свойства, такие как атрибуты поля и индексы, остаются нетронутыми.

Вы можете использовать DELETE, чтобы удалить записи из таблиц, которые находятся в связи "один ко многим" с другими таблицами. Операции каскадного удаления вызывают удаление записей в таблицах, расположенных на стороне многих связей, при удалении соответствующей записи на стороне одной связи при запросе. Например, в связи между таблицами Клиенты и Заказы, таблица Клиенты находится на стороне одной связи, а таблица Заказы находится на стороне многих связей. Удаление записи из результатов клиентов в соответствующих записях заказов, удаляемых в случае, если указан параметр каскадного удаления.

Запрос на удаление удаляет записи целиком, а не только данные в определенных полях. Если вы хотите удалить значения в определенном поле, создайте обновленный запрос, который изменяет значение на **Null**.

> [!IMPORTANT]
> - После удаления записи с помощью запроса на удаление невозможно отменить данную операцию. Если вы хотите узнать, какие записи были удалены, сначала проверьте результаты запроса на выборку, в котором используется то же самое условие, и снова запустите запрос на удаление.
> - Сохраняйте резервные копии ваших данных в любое время. Если вы удалили не те записи, вы сможете восстановить их из резервных копий.

## <a name="example"></a>Пример

В этом примере будут удалены все записи для сотрудников, чья должность — стажер. Если оператор FROM содержит только одну таблицу, нет необходимости перечислять имя таблицы в операторе DELETE.

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
