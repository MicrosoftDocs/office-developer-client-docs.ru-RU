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

В проекте Access вы можете использовать действие **опендиаграм** , чтобы открыть схему базы данных в режиме конструктора.

> [!NOTE]
> Эта макрокоманда доступна только для доверенных баз данных. 

## <a name="setting"></a>Параметры

Действие **опендиаграм** имеет следующий аргумент.

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
<td><p>Имя схемы базы данных, которую требуется открыть. В поле <strong>имя схемы</strong> в разделе <strong>аргументы макрокоманды</strong> области построителя макросов отображаются все схемы базы данных в текущей базе данных. Обязательный аргумент. При запуске макроса, содержащего действие <strong>опендиаграм</strong> , в библиотечной базе данных Microsoft Access сначала выполняет поиск схемы с этим именем в библиотечной базе данных, а затем в текущей базе данных.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Замечания

Это действие аналогично двойному щелчку схемы базы данных в области навигации или щелчку правой кнопкой мыши схемы базы данных в области навигации и выбора **режима конструктора**.

> [!TIP]
> Схему базы данных можно перетащить из области навигации в строку макрокоманды. При этом автоматически создается действие **опендиаграм** , которое открывает схему базы данных в представлении конструктора.

Чтобы запустить действие **опендиаграм** в модуле Visual Basic для приложений (VBA), используйте метод **опендиаграм** объекта **DoCmd** .

