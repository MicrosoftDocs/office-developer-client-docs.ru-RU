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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717806"
---
# <a name="locknavigationpane-macro-action"></a>Макрокоманда LockNavigationPane


**Применимо к**: Access 2013, Office 2013

Чтобы запретить пользователям удалять объекты базы данных, которые отображаются в области навигации можно использовать действие **LockNavigationPane** .

## <a name="setting"></a>Setting

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
<td><p><strong>Lock</strong></p></td>
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

