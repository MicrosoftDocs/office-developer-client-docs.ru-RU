---
title: Действия макроса StartNewWorkflow
TOCTitle: StartNewWorkflow Macro Action
ms:assetid: b3e81a11-b816-0eef-fc70-6d6da7a5a845
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822054(v=office.15)
ms:contentKeyID: 48547206
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm198223
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 6ba9d38caaa85ab9dd582abdbeb37aff5c7b340e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886496"
---
# <a name="startnewworkflow-macro-action"></a>Действия макроса StartNewWorkflow


**Применимо к**: Access 2013, Office 2013

Действие **StartNewWorkflow** можно использовать для запуска нового рабочего процесса для элемента в связанном списке Microsoft SharePoint Foundation.

## <a name="setting"></a>Параметр

Действие **StartNewWorkflow** использует следующий аргумент.

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
<td><p>Положение элемента в списке SharePoint Foundation, начиная с <strong>1</strong> для первого элемента в списке, <strong>2</strong> — для второго элемента, и т. д. Можно также ввести выражение для этого аргумента.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

  - Действие **StartNewWorkflow** открывает диалоговое окно **Запуск нового рабочего процесса** . Это диалоговое окно отображает все рабочие процессы, доступные для заданного элемента. Необходимо определить рабочего процесса для списка в Windows SharePoint Services, перед тем как начать с помощью этого действия.

  - Действие **StartNewWorkflow** может использоваться только после того как связанный список SharePoint открыт и выбрано. Чтобы открыть и выберите связанный список, используйте **ОткрытьТаблицу** . **Если список open, макрокоманда выберите его.**

  - Действие **StartNewWorkflow** имеет тот же эффект, что правой кнопкой мыши любую ячейку в связанном списке SharePoint, когда он открыт в представлении таблицы данных, с указанием **рабочего процесса**и затем выбрав **Запуск нового рабочего процесса**.

  - Чтобы выполнить действие **StartNewWorkflow** в модуле VBA, используйте метод **StartNewWorkflow** **объекта** .

