---
title: Макрокоманда StartNewWorkflow
TOCTitle: StartNewWorkflow macro action
ms:assetid: b3e81a11-b816-0eef-fc70-6d6da7a5a845
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822054(v=office.15)
ms:contentKeyID: 48547206
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm198223
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 1e37d72754531fc4dd51427eefb355a057d08073
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306400"
---
# <a name="startnewworkflow-macro-action"></a>Макрокоманда StartNewWorkflow


**Область применения**: Access 2013, Office 2013

С помощью действия **StartNewWorkflow** можно запустить новый рабочий процесс для элемента в связанном списке Microsoft SharePoint Foundation.

## <a name="setting"></a>Setting

Действие **StartNewWorkflow** имеет следующий аргумент.

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
<td><p>Положение элемента в списке SharePoint Foundation, начиная с <strong>1</strong> для первого элемента в списке, <strong>2</strong> для второго элемента и так далее. Вы также можете ввести выражение для этого аргумента.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Заметки

  - Действие **StartNewWorkflow** открывает диалоговое окно **"Начать** новый рабочий процесс". В этом диалоговом окне отображаются все доступные для указанного элемента процессы. Рабочий процесс должен быть определен для списка в SharePoint Foundation, прежде чем можно будет запустить его с помощью этого действия.

  - Действие **StartNewWorkflow** можно использовать только после открытия и выбора связанного списка SharePoint. Чтобы открыть и выбрать связанный список, используйте действие **OpenTable.** Если список уже открыт, выберите его с помощью действия **SelectObject.**

  - Действие **StartNewWorkflow** имеет тот же эффект, что и щелчок правой кнопкой мыши любую ячейку в связанном списке SharePoint, когда она открыта в представлении таблицы, указывая на рабочий **процесс,** а затем щелкнув "Начать новый рабочий процесс". 

  - Чтобы запустить действие **StartNewWorkflow** в модуле VBA, используйте метод **StartNewWorkflow** объекта **DoCmd.**

