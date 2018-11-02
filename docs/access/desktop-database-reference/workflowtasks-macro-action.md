---
title: Макрокоманда WorkflowTasks
TOCTitle: WorkflowTasks macro action
ms:assetid: 4b299681-b45b-f6d1-2cfe-ebf01712bfc1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193503(v=office.15)
ms:contentKeyID: 48544684
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm8454
f1_categories:
- Office.Version=v15
ms.openlocfilehash: f22d1a30a2dc7de003510f54d64fcafc9f0f7878
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920209"
---
# <a name="workflowtasks-macro-action"></a>Макрокоманда WorkflowTasks


**Применимо к**: Access 2013, Office 2013

Чтобы открыть диалоговое окно **Задачи рабочего процесса** можно использовать действие **WorkflowTasks** .

## <a name="setting"></a>Параметр

Действие **WorkflowTasks** использует следующий аргумент.

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
<td><p><strong>Номер записи</strong></p></td>
<td><p>Положение элемента в списке Microsoft SharePoint Foundation, начиная с <strong>1</strong> для первого элемента в списке, <strong>2</strong> — для второго элемента, и т. д. Можно также ввести выражение для этого аргумента.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

  - Действие **WorkflowTasks** открывает диалоговое окно **Задачи рабочего процесса** . Это диалоговое окно отображает все задачи, доступные для заданного элемента. Рабочий процесс необходимо определить для списка в Windows SharePoint Services.

  - Действие **WorkflowTasks** может использоваться только после того как связанный список SharePoint Foundation открывается и выбран. Чтобы открыть и выберите связанный список, используйте **ОткрытьТаблицу** . **Если список open, макрокоманда выберите его.**

  - Действие **WorkflowTasks** имеет тот же эффект, как правой кнопкой мыши любую ячейку в связанном списке SharePoint Foundation, когда он открыт в представлении таблицы данных, с указанием **рабочего процесса**и затем выбрав **Задачи рабочего процесса**.

  - Чтобы выполнить действие **WorkflowTasks** в модуле VBA, используйте метод **WorkflowTasks** **объекта** .

