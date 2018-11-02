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
ms.openlocfilehash: 985630f65508f7fca37de24f93649c8cf6047180
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920321"
---
# <a name="setdisplayedcategories-macro-action"></a>Макрокоманда SetDisplayedCategories


**Применимо к**: Access 2013, Office 2013

Чтобы указать, какие категории отображаются в разделе **Перейти по категории** в строке заголовка области переходов можно использовать действие **SetDisplayedCategories** . Например если вы хотите запретить пользователям переходить на панели переходов, чтобы она отображала объекты, отсортированные по **Дата создания**, можно использовать это действие для скрытия соответствующий параметр в строке заголовка раскрывающегося списка.

## <a name="setting"></a>Параметр

Действие **SetDisplayedCategories** состоит из следующих аргументов.

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
<td><p><strong>Show</strong> (Отображение)</p></td>
<td><p>Выберите <strong>Да,</strong> чтобы показать категорию или категории. Выберите <strong>Нет</strong> , чтобы скрыть их.</p></td>
</tr>
<tr class="even">
<td><p><strong>Категория</strong></p></td>
<td><p>Введите или выберите имя категории, которые необходимо показать или скрыть. Оставьте поле пустым, чтобы показать или скрыть все категории.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

  - Заголовок в строке заголовка области переходов указывает, какие фильтра при их наличии, в настоящее время активно. Щелкните в любом месте панели для отображения раскрывающегося списка. Элементы, которыми управляет это действие макроса перечислены в разделе **Перейти по категории**.

  - Это действие только включает или отключает отображение указанной категории, или; не выполняет переключение отображения области переходов. К примеру при отображении объектов, отсортированные по **Дата создания** и использовать действие **SetDisplayedCategories** , чтобы отключить параметр **Дата создания** , доступа не переключитесь в области навигации другой категории.

  - Чтобы выполнить действие **SetDisplayedCategories** в модуле VBA, используйте метод **SetDisplayedCategories** **объекта** .

