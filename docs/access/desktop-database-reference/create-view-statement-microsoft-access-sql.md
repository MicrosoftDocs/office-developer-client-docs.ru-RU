---
title: Инструкция CREATE VIEW (Microsoft Access SQL)
TOCTitle: CREATE VIEW statement (Microsoft Access SQL)
ms:assetid: ecaabd75-3081-fd35-830d-5a59b0a51922
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836312(v=office.15)
ms:contentKeyID: 48548519
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 5a25327aa81979a81f3410a383c06a0eda9d3113
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873742"
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

