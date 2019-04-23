---
title: Макрокоманда SetLocalVar
TOCTitle: SetLocalVar macro action
ms:assetid: 8a6af395-0f76-72e2-37f3-2cff22a38b3c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197097(v=office.15)
ms:contentKeyID: 48546190
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm176660
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 091b9717b9a2e35cfc8d0c8555e28570628065ef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314590"
---
# <a name="setlocalvar-macro-action"></a>Макрокоманда SetLocalVar

**Область применения**: Access 2013, Office 2013

Действие **SetLocalVar** создает временную переменную и присваивает ей определенное значение.

## <a name="setting"></a>Параметр

Действие **GoToControl** имеет следующие аргументы.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Аргумент</p></th>
<th><p>Обязательный</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Name</strong></p></td>
<td><p>Да</p></td>
<td><p>Строка, определяющая имя переменной.</p></td>
</tr>
<tr class="even">
<td><p><strong>Expression</strong></p></td>
<td><p>Да</p></td>
<td><p>Выражение, которое будет использоваться для задания значений для данной временной переменной. Не ставьте перед выражением знак равенства (=). Вы можете нажать кнопку <strong>Build</strong>, чтобы использовать <strong>Создатель выражений</strong> для установки данного аргумента.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Комментарии

Переменные, созданные действием **SetLocalVar**, можно использовать только в макросе, в котором они определены. Используйте действие **[SetTempVar](settempvar-macro-action.md)** для определения переменной, которая может использоваться в других макросах, процедурах обработки событий, формах и отчетах.

После создания временной переменной вы можете ссылаться на нее в выражении. Например, если вы создали временную переменную с именем TotalAmount, вы можете применять ее в качестве источника управления для текстового поля, используя следующий синтаксис.

`=[LocalVars]![TotalAmount]`

> [!NOTE]
> В макросе данных у вас нет необходимости использовать коллекцию LocalVars, чтобы сослаться на переменную. Например, если вы создали временную переменную в макросе данных с именем TotalAmount, вы можете применять ее в качестве источника управления для текстового поля, используя следующий синтаксис: `=[TotalAmount]`.

