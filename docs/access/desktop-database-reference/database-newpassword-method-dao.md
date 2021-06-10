---
title: Метод Database.NewPassword (DAO)
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
# <a name="databasenewpassword-method-dao"></a>Метод Database.NewPassword (DAO)

**Область применения**: Access 2013, Office 2013

Изменяет пароль существующей базы данных базы данных Microsoft Access (только в рабочей области Microsoft Access).

## <a name="syntax"></a>Синтаксис

*выражения* . NewPassword ***(bstrOld***, ***bstrNew***)

*выражение* Выражение, возвращаемая **объекту Database.**

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
<th><p>Обязательный/необязательный</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>bstrOld</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Текущий параметр свойства <strong>Password</strong> объекта <strong>Database.</strong></p></td>
</tr>
<tr class="even">
<td><p><em>bstrNew</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Новый параметр свойства <strong>Password</strong> объекта <strong>Database.</strong></p>
<p><strong>ПРИМЕЧАНИЕ.</strong>Используйте надежные пароли, сочетая в себе буквы, цифры и символы верхнего и нижнего регистров. В ненадежных паролях не используются сочетания таких элементов. Надежный пароль: Y6dh!et5. Слабый пароль: House27. Используйте надежный пароль, который можно запомнить, чтобы не пришлось его записывать.</p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Строки bstrOld и bstrNew могут быть длиной до 20 символов и могут включать любые символы, кроме символа ASCII 0 (null). Чтобы очистить пароль, используйте строку нулевой длины ("") для bstrNew.

В паролях учитывается регистр.

Если в базе данных нет пароля, то двигатель базы данных Microsoft Access автоматически создает его, передав строку нулевой длины ("") для старого пароля.


> [!IMPORTANT]
> Если вы потеряете пароль, вы никогда не сможете открыть базу данных снова.


