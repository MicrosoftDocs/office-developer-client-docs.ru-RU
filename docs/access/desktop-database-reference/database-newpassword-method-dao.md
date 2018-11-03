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
ms.openlocfilehash: d721102039a0fffbc8bbdc4696712bc530967fd8
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936856"
---
# <a name="databasenewpassword-method-dao"></a>Метод Database.NewPassword (DAO)


**Применимо к**: Access 2013, Office 2013

Изменение пароля существующей базы данных ядра базы данных Microsoft Access (только для рабочих областей Microsoft Access).

## <a name="syntax"></a>Синтаксис

*выражение* . Новый_пароль (***bstrOld***, ***bstrNew***)

*выражение* Выражение, возвращающее объект **базы данных** .

### <a name="parameters"></a>Параметры

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
<th><p>Обязательный или необязательный</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>bstrOld</p></td>
<td><p>Обязательный</p></td>
<td><p><strong>Строка</strong></p></td>
<td><p>Текущего значения свойства <strong>Password</strong> объекта <strong>базы данных</strong> .</p></td>
</tr>
<tr class="even">
<td><p>bstrNew</p></td>
<td><p>Обязательный</p></td>
<td><p><strong>Строка</strong></p></td>
<td><p>Новый параметр <strong>Password</strong> свойство объекта <strong>базы данных</strong> .</p>
<p><strong>Примечание</strong> Используйте надежные пароли, содержащие верхний и строчные буквы, числа и символы. Ненадежные пароли не смешивайте этих элементов. Надежный пароль: Y6dh! et5. Ненадежный пароль: House27. Используйте надежный пароль, который вы можете запомнить, чтобы записать его не нужно.</p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Строки bstrOld и bstrNew может иметь длину до 20 символов и может содержать все символы, за исключением символа ASCII 0 (null). Чтобы удалить пароль, используйте строку нулевой длины ("») для bstrNew.

Пароли зависят от регистра символов.

Если базы данных не имеет пароля, ядро базы данных Microsoft Access автоматически создаст, передав строку нулевой длины ("») для старого пароля.


> [!IMPORTANT]
> Если пароль утерян, могут никогда не откройте базу данных еще раз.


