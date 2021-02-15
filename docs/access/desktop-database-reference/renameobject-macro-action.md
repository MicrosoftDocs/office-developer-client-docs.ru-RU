---
title: Макрокоманда RenameObject
TOCTitle: RenameObject macro action
ms:assetid: fee04eb0-23c0-5d57-b903-e1ae54f2d25e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837293(v=office.15)
ms:contentKeyID: 48548948
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm165893
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: ce16b86ea06e041d490d0c68917daf18bd80dbb6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306722"
---
# <a name="renameobject-macro-action"></a>Макрокоманда RenameObject

**Область применения**: Access 2013, Office 2013

С помощью действия **RenameObject** можно переименовать указанный объект базы данных.

> [!NOTE]
> Эта макрокоманда доступна только для доверенных баз данных.

## <a name="setting"></a>Параметр

Действие **RenameObject** имеет следующие аргументы.

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
<td><p><strong>Новое имя</strong></p></td>
<td><p>Новое имя объекта базы данных. Введите имя объекта в поле <strong>"Новое имя"</strong> в разделе <strong>"Аргументы действий"</strong> области построитель макроса. Это обязательный аргумент.</p></td>
</tr>
<tr class="even">
<td><p><strong>Object Type</strong></p></td>
<td><p>Тип объекта, который нужно переименовать. Щелкните <strong>"Таблица", "Запрос",</strong> <strong>"Форма",</strong> <strong>"Отчет",</strong> <strong></strong> <strong>"Макрос", "Модуль",</strong>"Страница доступа к <strong>данным",</strong>"Представление сервера", "Схема", "Хранимая <strong>процедура"</strong>или <strong>"Функция".</strong> <strong></strong> <strong></strong> <strong></strong> Чтобы переименовать объект, выбранный в области навигации, оставьте этот аргумент пустым.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Старое имя</strong></p></td>
<td><p>Имя объекта, который необходимо переименовать. В <strong>поле "Старое</strong> имя" показаны все объекты в базе данных типа, выбранного <strong>аргументом "Тип объекта".</strong> Если оставить аргумент <strong>Object Type</strong> пустым, также оставьте этот аргумент пустым.</p><p><strong>ПРИМЕЧАНИЕ.</strong>При запуске макроса, содержащего действие "Переименовать" в базе данных библиотеки, Microsoft Access сначала ищет объект с этим именем в базе данных библиотеки, а затем в текущей базе данных. <STRONG></STRONG></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Заметки

Новое имя объекта базы данных должно следовать стандартным соглашениям об именах для объектов Access.

Нельзя переименовать открытый объект.

Если оставить **аргументы Object Type** и **Old Name** пустыми, Access переименовает объект, выбранный в области навигации. Чтобы выбрать объект в области навигации, можно использовать действие  **SelectObject** с аргументом "Да" в области **навигации.**

Вы также можете переименовать объект, щелкнув его правой кнопкой мыши в области навигации, щелкнув "Переименовать" и введите новое имя. С помощью **действия RenameObject** не нужно сначала выбирать объект в области навигации, и вам не нужно останавливать макрос, чтобы ввести новое имя.

Это действие отличается от действия **CopyObject,** которое создает копию объекта под новым именем.

Чтобы выполнить действие **RenameObject** в модуле Visual Basic для приложений (VBA), используйте метод **Rename** объекта **DoCmd.**

