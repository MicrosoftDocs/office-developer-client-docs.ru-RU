---
title: Макрокоманда OpenDiagram
TOCTitle: OpenDiagram macro action
ms:assetid: 408e7224-02bb-335a-b1b9-cbccbf6e36ec
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192875(v=office.15)
ms:contentKeyID: 48544427
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm154095
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f4273d6858ad98b723d66ba32fe3b9aa7c902d31
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288359"
---
# <a name="opendiagram-macro-action"></a>Макрокоманда OpenDiagram

**Область применения**: Access 2013, Office 2013

В проекте Access можно использовать действие **OpenDiagram** для открытия схемы базы данных в представлении Design.

> [!NOTE]
> Эта макрокоманда доступна только для доверенных баз данных. 

## <a name="setting"></a>Параметр

Действие **OpenDiagram** имеет следующий аргумент.

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
<td><p><strong>Имя схемы</strong></p></td>
<td><p>Имя схемы базы данных для открытия. Поле <strong>Имя диаграммы</strong> в разделе <strong>Аргументы</strong> действий в области Macro Builder отображает все схемы базы данных в текущей базе данных. Это обязательный аргумент. Если вы запустите макрос, содержащий действие <strong>OpenDiagram</strong> в базе данных библиотеки, Microsoft Access сначала ищет схему с этим именем в базе данных библиотеки, а затем в текущей базе данных.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Примечания

Это действие аналогично двойному нажатию диаграммы базы данных в области навигации или правой щелкнув диаграмму базы данных в области навигации, а затем щелкнув **Представление дизайна.**

> [!TIP]
> Схему базы данных можно перетаскивать из области навигации в строку действий макроса. Это автоматически создает действие **OpenDiagram,** которое открывает схему базы данных в представлении Design.

Чтобы выполнить **действие OpenDiagram** в Visual Basic для приложений (VBA), используйте метод **OpenDiagram** объекта **DoCmd.**

