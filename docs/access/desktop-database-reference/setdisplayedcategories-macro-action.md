---
title: Макрокоманда SetDisplayedCategories
TOCTitle: SetDisplayedCategories macro action
ms:assetid: e8bf39a6-c639-2232-7b21-3b0badf37e4b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836053(v=office.15)
ms:contentKeyID: 48548429
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm20026
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f08b9a8980fc6f08a9f91366d38f65e4365a037e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314627"
---
# <a name="setdisplayedcategories-macro-action"></a>Макрокоманда SetDisplayedCategories


**Область применения**: Access 2013, Office 2013

Вы можете использовать **действие SetDisplayedCategories,** чтобы указать, какие категории отображаются в статье **Перейдите** к категории в панели заголовков панели навигации. Например, если вы хотите запретить пользователям переключение панели навигации, чтобы она отображала объекты, отсортированные по **созданной** дате, вы можете использовать это действие, чтобы скрыть этот параметр в выпадаемом списке панели заголовка.

## <a name="setting"></a>Параметр

Действие **SetDisplayedCategories** имеет следующие аргументы.

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
<td><p><strong>Show</strong></p></td>
<td><p>Выберите <strong>Да,</strong> чтобы показать категорию или категории. Выберите <strong>Нет,</strong> чтобы скрыть их.</p></td>
</tr>
<tr class="even">
<td><p><strong>Категория</strong></p></td>
<td><p>Введите или выберите имя категории, которая будет показываться или скрываться. Оставьте пустым, чтобы показать или скрыть все категории.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

  - Подпись в панели заголовка панели навигации указывает, какой фильтр, если таково, в настоящее время активен. Щелкните в любом месте панели, чтобы отобразить выпадаемый список. Элементы, указанные в элементе управления макросами, перечислены в **статье Перейдите к категории**.

  - Это действие включает или отключает отображение указанной категории или категорий; он не выполняет переключения экрана навигации. Например, если отобразить объекты, отсортированные по дате создания, и вы используете действие **SetDisplayedCategories** для отключения параметра **Дата** создания, Access не переключает области навигации на другую категорию. 

  - Для запуска **действия SetDisplayedCategories** в модуле VBA используйте метод **SetDisplayedCategories** объекта **DoCmd.**

