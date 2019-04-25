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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295368"
---
# <a name="create-view-statement-microsoft-access-sql"></a>Инструкция CREATE VIEW (Microsoft Access SQL)

**Область применения**: Access 2013, Office 2013

Создает представление.

> [!NOTE]
> Ядро СУБД Microsoft Access не поддерживает использование CREATE VIEW или любой другой инструкции DDL с базами данных не на основе ядра СУБД Microsoft Access.

## <a name="syntax"></a>Синтаксис

CREATE VIEW *представление* \[(*поле1*\[, *поле2*\[, …\]\])\] AS *инструкция_SELECT*

Инструкция CREATE VIEW включает приведенные ниже элементы.

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
<td><p><em>представление</em></p></td>
<td><p>Имя создаваемого представления.</p></td>
</tr>
<tr class="even">
<td><p><em>поле1</em>, <em>поле2</em></p></td>
<td><p>Имена соответствующих полей, заданных в элементе <em>инструкция_SELECT</em>.</p></td>
</tr>
<tr class="odd">
<td><p><em>инструкция_SELECT</em></p></td>
<td><p>Инструкция SQL SELECT. Дополнительные сведения см. в статье <a href="select-statement-microsoft-access-sql.md">Инструкция SELECT</a>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Инструкция SELECT, определяющая представление, не может быть инструкцией [SELECT INTO](select-into-statement-microsoft-access-sql.md).

Инструкция SELECT, определяющая представление, не должна содержать параметров.

Имя представления не может совпадать с именем существующей таблицы.

Если запрос, определенный инструкцией SELECT, является обновляемым, представление также может обновляться. В противном случае оно предназначено только для чтения.

Если любые два поля в запросе, определенном инструкцией SELECT, имеют одинаковые имена, определение представления должно содержать список уникальных имен для каждого поля в запросе.

