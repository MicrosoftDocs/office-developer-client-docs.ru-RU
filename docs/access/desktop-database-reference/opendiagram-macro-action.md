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

В проекте Access можно использовать действие **OpenDiagram,** чтобы открыть схему базы данных в представлении конструктора.

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
<td><p>Имя открываемой схемы базы данных. В <strong>поле "Имя</strong> схемы" в разделе <strong>"Аргументы</strong> действий" области построитель макроса показаны все схемы базы данных в текущей базе данных. Это обязательный аргумент. При запуске макроса, содержащего действие <strong>OpenDiagram</strong> в базе данных библиотеки, Microsoft Access сначала ищет схему с этим именем в базе данных библиотеки, а затем в текущей базе данных.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Заметки

Это действие аналогично двойному щелчку по схеме базы данных в области навигации или щелчку правой кнопкой мыши схемы базы данных в области навигации и нажатию кнопки **"Конструктор".**

> [!TIP]
> Схему базы данных можно перетащить из области навигации в строку макроса. При этом автоматически создается действие **OpenDiagram,** которое открывает схему базы данных в режиме конструктора.

Чтобы выполнить действие **OpenDiagram** в модуле Visual Basic для приложений (VBA), используйте метод **OpenDiagram** объекта **DoCmd.**

