---
title: Макрокоманда RunCode
TOCTitle: RunCode macro action
ms:assetid: cb0625be-4b5d-4927-9b0e-59a6e411b5bb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834373(v=office.15)
ms:contentKeyID: 48547706
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm98700
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 646c1393cc798c1f827e6ceaebf46bfe7c87bcbd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306834"
---
# <a name="runcode-macro-action"></a>Макрокоманда RunCode

**Область применения**: Access 2013, Office 2013

Вы можете использовать действие **RunCode** для вызова процедуры Visual Basic для приложений (VBA).

## <a name="setting"></a>Параметр

Действие **RunCode** имеет следующий аргумент.

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
<td><p><strong>Имя функции</strong></p></td>
<td><p>Имя процедуры VBA Function для вызова. Заключите все аргументы функций в скобки. Введите имя функции в поле <strong>Имя функции</strong> в разделе <strong>Аргументы</strong> действий области Macro Builder. Это обязательный аргумент.</p><p><strong>ПРИМЕЧАНИЕ.</strong>В базе данных access (.mdb или .accdb) нажмите кнопку <strong>Сборка,</strong> чтобы использовать конструктор выражения для выбора функции для этого аргумента. Щелкните нужную функцию в списке в конструкторе выражений.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Процедуры функции, определенные пользователем, хранятся в модулях Microsoft Access.

Необходимо включить скобки, даже если в процедуре Function нет аргументов, как в следующем примере:

`TestFunction()`

В отличие от имен функций, определенных пользователем, используемых для параметров свойств событий, имя функции в аргументе **Имя** функции не начинается с равного знака ( **=** ).

Доступ игнорирует возвращаемую стоимость функции.

> [!NOTE]
> Нельзя вызывать процедуру Function с макроса, если имя функции такое же, как имя модуля.

> [!TIP]
> Чтобы запустить процедуру Sub или процедуру события, написанную в Visual Basic, создайте процедуру Function, которая вызывает процедуру Sub или процедуру события. Затем используйте действие **RunCode** для запуска процедуры Function.

Если для вызова функции используется действие **RunCode,** Access ищет функцию с именем, указанным аргументом **"Имя** функции" в стандартных модулях базы данных. Однако, когда это действие выполняется в ответ на нажатие команды меню на форму или отчет или в ответ на событие в форме или отчете, Access сначала ищет функцию в классе формы или отчета, а затем в стандартных модулях. Доступ не позволяет искать модули классов, которые отображаются в области **Модулей** области навигации для функции, указанной **аргументом "Имя функции".**

Эта макрокоманда недоступна в модуле VBA.  Вместо этого запустите нужную процедуру Function непосредственно в VBA.

