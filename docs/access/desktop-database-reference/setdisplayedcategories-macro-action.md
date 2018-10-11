---
title: SetDisplayedCategories Macro Action
TOCTitle: SetDisplayedCategories Macro Action
ms:assetid: e8bf39a6-c639-2232-7b21-3b0badf37e4b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836053(v=office.15)
ms:contentKeyID: 48548429
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm20026
f1_categories:
- Office.Version=v15
ms.openlocfilehash: af4b491ff76a28c998e1ec195a861dbf065d36c8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482507"
---
# <a name="setdisplayedcategories-macro-action"></a>SetDisplayedCategories Macro Action


**Применимо к**: Access 2013 | Office 2013

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


## <a name="remarks"></a>Замечания

  - Заголовок в строке заголовка области переходов указывает, какие фильтра при их наличии, в настоящее время активно. Щелкните в любом месте панели для отображения раскрывающегося списка. Элементы, которыми управляет это действие макроса перечислены в разделе **Перейти по категории**.

  - Это действие только включает или отключает отображение указанной категории, или; не выполняет переключение отображения области переходов. К примеру при отображении объектов, отсортированные по **Дата создания** и использовать действие **SetDisplayedCategories** , чтобы отключить параметр **Дата создания** , доступа не переключитесь в области навигации другой категории.

  - Чтобы выполнить действие **SetDisplayedCategories** в модуле VBA, используйте метод **SetDisplayedCategories** **объекта** .

