---
title: Макрокоманда DeleteObject
TOCTitle: DeleteObject macro action
ms:assetid: a8deb2a7-4e73-8696-b8c1-3a3939d813f7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821415(v=office.15)
ms:contentKeyID: 48546912
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm152112
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: dae5718e7b4cb609cb50bd65ee6e2486f4ebaab6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294031"
---
# <a name="deleteobject-macro-action"></a>Макрокоманда DeleteObject

**Область применения**: Access 2013, Office 2013

Вы можете использовать действие **DeleteObject** , чтобы удалить указанный объект базы данных.

> [!NOTE]
> Эта макрокоманда доступна только для доверенных баз данных. 

## <a name="setting"></a>Параметры

Макрокоманда **DeleteObject** имеет следующие аргументы.

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
<td><p><strong>Object Type</strong></p></td>
<td><p>Тип удаляемого объекта. Щелкните <strong>Таблица</strong>, <strong>запрос</strong>, <strong>форма</strong>, <strong>отчет</strong>, <strong>макрос</strong>, <strong>модуль</strong>, <strong>Страница доступа к данным</strong>, <strong>представление сервера</strong>, <strong>схема</strong>, <strong>хранимая процедура</strong>или <strong>функция</strong> в <strong>типе объекта. </strong>в разделе <strong>аргументы макрокоманды</strong> в панели построителя макросов. Чтобы удалить объект, выбранный в области навигации, оставьте этот аргумент пустым.</p></td>
</tr>
<tr class="even">
<td><p><strong>Object Name</strong></p></td>
<td><p>Имя удаляемого объекта. Поле <strong>Object Name</strong> отображает все объекты базы данных, относящиеся к типу, заданному аргументом <strong>Object Type</strong>. Если оставить поле <strong>тип объекта</strong> пустым, также оставьте это поле пустым. При запуске макроса, содержащего действие <strong>DeleteObject</strong> в библиотечной базе данных, Microsoft Office Access 2007 сначала ищет объект с этим именем в библиотечной базе данных, а затем в текущей базе данных.</p></td>
</tr>
</tbody>
</table>

> [!WARNING]
> Если оставить поля **тип объекта** и **имя объекта** пустыми, Access удаляет объект, выбранный в области навигации, без отображения предупреждения при обнаружении действия **DeleteObject** .

## <a name="remarks"></a>Замечания

Вы можете использовать действие **DeleteObject** для удаления временных объектов, созданных во время запуска макроса. Например, с помощью действия **OPENQUERY** можно выполнить запрос на создание таблицы, который создает временную таблицу. По завершении использования временной таблицы можно удалить ее с помощью действия **DeleteObject** .

Это действие эквивалентно выбору объекта в области навигации и нажатию клавиши DEL или щелчку правой кнопкой мыши объекта в области навигации и нажатию кнопки **Удалить**.

Чтобы запустить действие **DeleteObject** в модуле Visual Basic для приложений, можно использовать метод **DeleteObject** объекта **DoCmd** .

