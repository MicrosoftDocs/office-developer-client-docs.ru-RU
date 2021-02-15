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
localization_priority: Normal
ms.openlocfilehash: 921396edd480e06194d1c3dcbb683aa8556553e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306008"
---
# <a name="workflowtasks-macro-action"></a>Макрокоманда WorkflowTasks


**Область применения**: Access 2013, Office 2013

Вы можете использовать **действие WorkflowTasks,** чтобы отобразить диалоговое окно "Задача **рабочего** процесса".

## <a name="setting"></a>Setting

Действие **WorkflowTasks имеет** следующий аргумент.

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
<td><p>Положение элемента в списке Microsoft SharePoint Foundation, начиная с <strong>1</strong> для первого элемента в списке, <strong>2</strong> для второго элемента и так далее. Вы также можете ввести выражение для этого аргумента.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Заметки

  - Действие **WorkflowTasks** открывает **диалоговое** окно "Задачи рабочего процесса". В этом диалоговом окне отображаются все задачи, доступные для указанного элемента. Рабочий процесс должен быть определен для списка в SharePoint Foundation.

  - Действие **WorkflowTasks** можно использовать только после открытия и выбора связанного списка SharePoint Foundation. Чтобы открыть и выбрать связанный список, используйте действие **OpenTable.** Если список уже открыт, выберите его с помощью действия **SelectObject.**

  - Действие **WorkflowTasks** имеет тот же эффект, что и щелчок правой кнопкой мыши любую ячейку в связанном списке SharePoint Foundation, когда она открыта в представлении таблицы, указывая на рабочий **процесс,** а затем щелкнув "Задачи рабочего процесса". 

  - Чтобы запустить **действие WorkflowTasks** в модуле VBA, используйте метод **WorkflowTasks** объекта **DoCmd.**

