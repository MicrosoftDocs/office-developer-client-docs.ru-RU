---
title: Действия макроса WorkflowTasks
TOCTitle: WorkflowTasks Macro Action
ms:assetid: 4b299681-b45b-f6d1-2cfe-ebf01712bfc1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193503(v=office.15)
ms:contentKeyID: 48544684
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm8454
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 1bbb04600dc6f7ecea4ce9084b146d3bf696cd6b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878124"
---
# <a name="workflowtasks-macro-action"></a>Действия макроса WorkflowTasks


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


## <a name="remarks"></a>Замечания

  - Действие **WorkflowTasks** открывает диалоговое окно **Задачи рабочего процесса** . Это диалоговое окно отображает все задачи, доступные для заданного элемента. Рабочий процесс необходимо определить для списка в Windows SharePoint Services.

  - Действие **WorkflowTasks** может использоваться только после того как связанный список SharePoint Foundation открывается и выбран. Чтобы открыть и выберите связанный список, используйте **ОткрытьТаблицу** . **Если список open, макрокоманда выберите его.**

  - Действие **WorkflowTasks** имеет тот же эффект, как правой кнопкой мыши любую ячейку в связанном списке SharePoint Foundation, когда он открыт в представлении таблицы данных, с указанием **рабочего процесса**и затем выбрав **Задачи рабочего процесса**.

  - Чтобы выполнить действие **WorkflowTasks** в модуле VBA, используйте метод **WorkflowTasks** **объекта** .

