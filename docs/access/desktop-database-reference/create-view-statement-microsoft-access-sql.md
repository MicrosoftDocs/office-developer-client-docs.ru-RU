---
title: Инструкция CREATE VIEW (Microsoft Access SQL)
TOCTitle: CREATE VIEW statement (Microsoft Access SQL)
ms:assetid: ecaabd75-3081-fd35-830d-5a59b0a51922
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836312(v=office.15)
ms:contentKeyID: 48548519
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 73fac5ff9dd1f5cf277b8cb241044af23609b764
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706627"
---
# <a name="create-view-statement-microsoft-access-sql"></a>Инструкция CREATE VIEW (Microsoft Access SQL)

**Применимо к**: Access 2013, Office 2013

Создание нового представления.

> [!NOTE]
> Ядро СУБД Microsoft Access не поддерживает использование CREATE VIEW или любой другой инструкции DDL с базами данных, ядро базы данных Microsoft Access.

## <a name="syntax"></a>Синтаксис

Создание ПРЕДСТАВЛЕНИЯ *представление* \[(*field1*\[, *поле2*\[,... \] \])\] Как *selectstatement*

Инструкция CREATE VIEW состоит из следующих частей:

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
<td><p><em>view</em></p></td>
<td><p>Имя представления будет создан.</p></td>
</tr>
<tr class="even">
<td><p><em>field1</em>, <em>field2</em></p></td>
<td><p>Имя поля или полей для соответствующих полей, определенных в <em>selectstatement</em>.</p></td>
</tr>
<tr class="odd">
<td><p><em>selectstatement</em></p></td>
<td><p>Инструкция SQL SELECT. Дополнительные сведения см в <a href="select-statement-microsoft-access-sql.md">оператор SELECT</a>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

ВЫБЕРИТЕ оператор, определяющий представление, не может быть инструкции [SELECT INTO](select-into-statement-microsoft-access-sql.md) .

ВЫБЕРИТЕ оператор, определяющий представление, не может содержать каких-либо параметров.

Имя представления не может быть имя существующей таблицы.

Если запрос, определенные в инструкции SELECT является обновляемым, представление также может обновляться. В противном случае представление доступно только для чтения.

Если любые два поля в запросе, определенные в инструкции SELECT имеет то же имя, определение представления должно содержать список полей, определяющее уникальные имена для каждого поля в запросе.

