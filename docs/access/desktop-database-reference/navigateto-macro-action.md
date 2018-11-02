---
title: Макрокоманда NavigateTo
TOCTitle: NavigateTo macro action
ms:assetid: 6594d614-3ea6-7851-b70e-1661d24f8ba0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195165(v=office.15)
ms:contentKeyID: 48545324
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm119055
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 9d8747c5c4fd1a32a36841f648017bc0cab3de8f
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920811"
---
# <a name="navigateto-macro-action"></a>Макрокоманда NavigateTo


**Применимо к**: Access 2013, Office 2013

Действие **NavigateTo** можно использовать для управления отображением объектов базы данных в области навигации. Например можно изменить как классифицируются объекты базы данных и объекты можно отфильтровать так, чтобы отображались только некоторые из них.

## <a name="setting"></a>Параметр

Действие **NavigateTo** состоит из следующих аргументов.

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
<td><p><strong>Категория</strong></p></td>
<td><p>Обязательно указывать. Категория, по которому требуется области навигации для отображения объектов. Выберите <strong>Тип объекта</strong>, <strong>таблицы и представления</strong>, <strong>Дата изменения</strong>, <strong>Дата создания</strong>или <strong>Custom</strong> в поле <strong>категории</strong> .</p></td>
</tr>
<tr class="even">
<td><p><strong>group</strong></p></td>
<td><p>Необязательно указывать. Ограничения аргумент для <strong>групп</strong> , которые объектов в категории, отображаются в области навигации. Если <strong>Группа</strong> аргумента оставлено пустым, области навигации отображает все объекты базы данных, упорядоченные по условиям, указанным в аргументе <strong>категории</strong> . В следующей таблице показаны примеры допустимых аргументов <strong>группы</strong> для различных <strong>категорий</strong> аргументов.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

  - Это действие аналогично Выбор категории и группы из строки заголовка в области переходов.

  - Допустимые аргументы **группы** зависят от того, какие **категории** используется аргумент. Если указан недопустимый аргумент **группы** , появляется сообщение об ошибке. В следующей таблице приведены примеры допустимых аргументов **группы** для каждой **категории** аргумента.
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p>Аргумент категории</p></th>
    <th><p>Пример группового аргументов</p></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p>Тип объекта</p></td>
    <td><p>Таблиц; Форм; Запросы; Страницы; Макросы; Модули</p></td>
    </tr>
    <tr class="even">
    <td><p>Таблицы и представления</p></td>
    <td><p>Имена отдельных таблиц в базе данных</p></td>
    </tr>
    <tr class="odd">
    <td><p>Дата изменения</p></td>
    <td><p>Текущая; Устаревшее; Последний месяц; Более старые</p></td>
    </tr>
    <tr class="even">
    <td><p>Created Date (дата создания)</p></td>
    <td><p>Текущая; Устаревшее; Последний месяц; Более старые</p></td>
    </tr>
    <tr class="odd">
    <td><p>Настраиваемые категории</p></td>
    <td><p>Имена групп, созданные для указанного настраиваемые категории</p></td>
    </tr>
    </tbody>
    </table>


  - Чтобы выполнить действие **NavigateTo** в модуле VBA, используйте метод **NavigateTo** **объекта** .


> [!NOTE]
> <P>Чтобы перейти на верхний уровень категории (например, <STRONG>Все таблицы</STRONG>, <STRONG>Все объекты доступа</STRONG>или <STRONG>Все даты</STRONG>), аргумент группы необходимо оставить пустым. К примеру при аргумент <STRONG>категории</STRONG> — это <STRONG>Тип объекта</STRONG>, ввод <STRONG>Всех объектов доступа</STRONG> как аргумент <STRONG>группы</STRONG> , приведет к ошибке.</P>


