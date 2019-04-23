---
title: Макрокоманда LockNavigationPane
TOCTitle: LockNavigationPane macro action
ms:assetid: abf7a989-c7cf-3efa-8df4-3c5b075d0e5f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821487(v=office.15)
ms:contentKeyID: 48546986
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm172454
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 7f6ee19edaf2efdc03301e98e709db6dd69f101a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289873"
---
# <a name="locknavigationpane-macro-action"></a>Макрокоманда LockNavigationPane


**Область применения**: Access 2013, Office 2013

Вы можете использовать действие **локкнавигатионпане** , чтобы запретить пользователям удалять объекты базы данных, отображаемые в области навигации.

## <a name="setting"></a>Параметр

Действие **локкнавигатионпане** имеет следующий аргумент.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Аргумент макрокоманды</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Lock</strong></p></td>
<td><p>Нажмите <strong>кнопку Да</strong> , чтобы заблокировать область навигации, или <strong>нет</strong> , чтобы разблокировать область навигации.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

Блокировка области навигации предотвращает удаление объектов базы данных или удаление объектов базы данных в буфер обмена. Она *не* препятствует выполнению следующих операций:

  - Копирование объектов базы данных в буфер обмена

  - Вставке объектов базы данных из буфера обмена

  - Отображение или скрытие области навигации

  - Выбор различных схем организации в области навигации

  - Отображение или скрытие разделов в области навигации

Чтобы выполнить действие **локкнавигатионпане** в модуле VBA, используйте метод **локкнавигатионпане** объекта **DoCmd** .

