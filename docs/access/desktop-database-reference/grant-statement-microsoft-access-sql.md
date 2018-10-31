---
title: Инструкция GRANT (Microsoft Access SQL)
TOCTitle: GRANT statement (Microsoft Access SQL)
ms:assetid: 50ae97ae-d5be-57e5-d9da-f3fc42f01d83
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193820(v=office.15)
ms:contentKeyID: 48544800
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277478
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 4e37c0853c2b80c42bb2560cb0a19122c45f85f4
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860879"
---
# <a name="grant-statement-microsoft-access-sql"></a>Инструкция GRANT (Microsoft Access SQL)

**Применимо к**: Access 2013 | Office 2013

Предоставление определенных привилегий существующему пользователю или группе.

## <a name="syntax"></a>Синтаксис

Предоставление {*принципу предоставления минимальных прав*\[, *принципу предоставления минимальных прав*,... \]} Д {таблицы в *таблице* | Объект *object*|

КОНТЕЙНЕР *container* } Кому {*имя_обладателя_прав*\[, *имя_обладателя_прав*,... \]}

Инструкция GRANT состоит из следующих частей:

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
<td><p><em>принципу предоставления минимальных прав</em></p></td>
<td><p>Принципу предоставления минимальных прав или предоставляемые привилегии. Привилегии задаются с помощью следующих ключевых слов: выбор, DELETE, INSERT, UPDATE, размещения сообщений, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, создать, SELECTSCHEMA, СХЕМЫ и UPDATEOWNER.</p></td>
</tr>
<tr class="even">
<td><p><em>TableName</em></p></td>
<td><p>Любое допустимое имя таблицы.</p></td>
</tr>
<tr class="odd">
<td><p><em>object</em></p></td>
<td><p>Это могут использовать любой объект не таблицы. Сохраненные запрос (представления или процедуры) — один пример.</p></td>
</tr>
<tr class="even">
<td><p><em>контейнер</em></p></td>
<td><p>Имя допустимого хранилища.</p></td>
</tr>
<tr class="odd">
<td><p><em>имя_обладателя_прав</em></p></td>
<td><p>Имя пользователя или группы.</p></td>
</tr>
</tbody>
</table>

