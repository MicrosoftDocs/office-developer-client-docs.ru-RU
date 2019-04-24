---
title: Метод Database. NewPassword (DAO)
TOCTitle: NewPassword Method
ms:assetid: 01c1c454-d651-222c-225a-2b02734a1b7a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844754(v=office.15)
ms:contentKeyID: 48542941
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052943
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 20f09dbfba50526409472f7eb804ba2c47e4d1d5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294857"
---
# <a name="databasenewpassword-method-dao"></a>Метод Database. NewPassword (DAO)

**Область применения**: Access 2013, Office 2013

Изменяет пароль существующей базы данных ядра СУБД Microsoft Access (только для рабочих областей Microsoft Access).

## <a name="syntax"></a>Синтаксис

*Expression* . NewPassword (***бстролд***, ***бстрнев***)

*Expression (выражение* ) Выражение, возвращающее объект **базы данных** .

## <a name="parameters"></a>Параметры

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя</p></th>
<th><p>Обязательно/необязательно</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Бстролд</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Текущее значение свойства <strong>Password</strong> объекта <strong>Database</strong> .</p></td>
</tr>
<tr class="even">
<td><p><em>Бстрнев</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Новый параметр свойства <strong>Password</strong> объекта <strong>Database</strong> .</p>
<p><strong>Note</strong>: Используйте надежные пароли, объединяющие прописные и строчные буквы, цифры и символы. В слабых паролях эти элементы не комбинируются. Надежный пароль: Y6dh!et5. Слабый пароль: House27. Используйте надежный пароль, который можно запомнить, чтобы не записывать его.</p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

Строки Бстролд и Бстрнев могут иметь длину до 20 символов и могут содержать любые символы, кроме символов ASCII 0 (null). Чтобы очистить пароль, используйте строку нулевой длины ("") для Бстрнев.

В паролях учитывается регистр.

Если база данных не имеет пароля, ядро СУБД Microsoft Access автоматически создаст ее, передав для старого пароля строку нулевой длины ("").


> [!IMPORTANT]
> Если вы потеряли пароль, вы не сможете повторно открыть базу данных.


