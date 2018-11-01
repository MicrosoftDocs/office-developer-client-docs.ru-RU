---
title: Действия макроса LockNavigationPane
TOCTitle: LockNavigationPane Macro Action
ms:assetid: abf7a989-c7cf-3efa-8df4-3c5b075d0e5f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821487(v=office.15)
ms:contentKeyID: 48546986
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm172454
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 2db34ee9ea56c5fcb4c5aff6afa57c3f59d1f17c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870333"
---
# <a name="locknavigationpane-macro-action"></a>Действия макроса LockNavigationPane


**Применимо к**: Access 2013, Office 2013

Чтобы запретить пользователям удалять объекты базы данных, которые отображаются в области навигации можно использовать действие **LockNavigationPane** .

## <a name="setting"></a>Параметр

Действие **LockNavigationPane** использует следующий аргумент.

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
<td><p><strong>Блокировка</strong></p></td>
<td><p>Выберите <strong>Да</strong> для блокировки области переходов или <strong>Нет</strong> для разблокировки области навигации.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

Закрепление области переходов позволяет удалять объекты базы данных или обрезка объектов базы данных в буфер обмена. Оно делает это *не* препятствует выполнению любой из следующих операций:

  - Копирование объектов базы данных в буфер обмена

  - Вставка объектов базы данных из буфера обмена

  - Отображение или скрытие области переходов

  - Выбор другой схемы организации области переходов

  - Отображение или скрытие разделов области переходов

Чтобы выполнить действие **LockNavigationPane** в модуле VBA, используйте метод **LockNavigationPane** **объекта** .

