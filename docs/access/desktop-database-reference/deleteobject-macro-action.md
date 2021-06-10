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

Вы можете использовать **действие DeleteObject** для удаления указанного объекта базы данных.

> [!NOTE]
> Эта макрокоманда доступна только для доверенных баз данных. 

## <a name="setting"></a>Параметр

Действие **DeleteObject** имеет следующие аргументы.

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
<td><p>Тип объекта, который необходимо удалить. <strong>Щелкните</strong> <strong>таблицу,</strong> <strong>запрос,</strong>форма, отчет, макрос, модуль, <strong></strong> <strong></strong>страница доступа <strong></strong> к данным, представление сервера, схема, сохраненная процедура или функция в поле Тип объекта в разделе Аргументы действий области Macro Builder. <strong></strong> <strong></strong> <strong></strong> <strong></strong> <strong></strong> <strong></strong> <strong></strong> Чтобы удалить объект, выбранный в области навигации, оставьте этот аргумент пустым.</p></td>
</tr>
<tr class="even">
<td><p><strong>Object Name</strong></p></td>
<td><p>Имя удаляемого объекта. Поле <strong>Object Name</strong> отображает все объекты базы данных, относящиеся к типу, заданному аргументом <strong>Object Type</strong>. Если поле <strong>Типа объекта</strong> будет пустым, оставьте это поле пустым. Если вы запустите макрос, содержащий действие <strong>DeleteObject</strong> в базе данных библиотеки, Microsoft Office Access 2007 сначала ищет объект с этим именем в базе данных библиотеки, а затем в текущей базе данных.</p></td>
</tr>
</tbody>
</table>

> [!WARNING]
> Если поля **типа** объектов  и имен объектов не будут пустыми, Access удаляет объект, выбранный в области навигации, не отобразив предупреждающий сигнал при столкновении с действием **DeleteObject.**

## <a name="remarks"></a>Примечания

Вы можете использовать **действие DeleteObject** для удаления временных объектов, созданных во время работы макроса. Например, можно использовать действие **OpenQuery** для выполнения запроса на создание временной таблицы. Когда вы закончите использовать временную таблицу, вы можете удалить ее с помощью **действия DeleteObject.**

Это действие имеет тот же эффект, что и выбор объекта в области навигации, а затем нажатие клавиши DEL или щелкнуть правой кнопкой мыши объект в области навигации и нажать кнопку **Удалить**.

Для запуска **действия DeleteObject** в Visual Basic для приложений можно использовать метод **DeleteObject** объекта **DoCmd.**

