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
localization_priority: Normal
ms.openlocfilehash: 1c37e798e0624a5655b63a76332073e5b57c0823
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288604"
---
# <a name="navigateto-macro-action"></a>Макрокоманда NavigateTo

**Область применения**: Access 2013, Office 2013

Вы можете использовать действие **NavigateTo** для управления отображением объектов базы данных в области навигации. Например, вы можете изменить способ классификации объектов базы данных, а также отфильтровать объекты, чтобы отображались только некоторые из них.

## <a name="setting"></a>Параметр

Макрокоманда **NavigateTo** имеет следующие аргументы.

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
<td><p>Обязательный. Категория, на которую будет отображаться объект области навигации. В поле <strong>Категория</strong> щелкните <strong>тип объекта</strong>, <strong>таблицы и представления</strong>, <strong>Дата изменения</strong>, <strong>Дата создания</strong>или <strong>Пользовательская</strong> .</p></td>
</tr>
<tr class="even">
<td><p><strong>Group</strong></p></td>
<td><p>Необязательный атрибут. Аргумент <strong>Group</strong> устанавливает, какие объекты в категории отображаются в области навигации. Если оставить аргумент <strong>группы</strong> пустым, в области навигации будут отображены все объекты базы данных, классифицированные по критериям, указанным в аргументе <strong>Category (категория</strong> ). Примеры допустимых аргументов <strong>группы</strong> для различных аргументов <strong>категории</strong> показаны в следующей таблице.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

- Это действие аналогично выбору категорий и групп в строке заголовка области навигации.

- Допустимые аргументы **группы** зависят от используемого аргумента **Category** . Если ввести недопустимый аргумент **группы** , будет выведено сообщение об ошибке. В следующей таблице приведены примеры допустимых аргументов **группы** для каждого аргумента **Category** .
    
  <table>
  <colgroup>
  <col style="width: 50%" />
  <col style="width: 50%" />
  </colgroup>
  <thead>
  <tr class="header">
  <th><p>Аргумент Category</p></th>
  <th><p>Примеры аргументов группы</p></th>
  </tr>
  </thead>
  <tbody>
  <tr class="odd">
  <td><p>Тип объекта</p></td>
  <td><p>Table Формирует Запросе Страниц Макросы Модуля</p></td>
  </tr>
  <tr class="even">
  <td><p>Таблицы и представления</p></td>
  <td><p>Имена определенных таблиц в базе данных</p></td>
  </tr>
  <tr class="odd">
  <td><p>Дата изменения</p></td>
  <td><p>Посещения Вчерашни Прошлый месяц; Старше</p></td>
  </tr>
  <tr class="even">
  <td><p>Created Date (дата создания)</p></td>
  <td><p>Посещения Вчерашни Прошлый месяц; Старше</p></td>
  </tr>
  <tr class="odd">
  <td><p>Настраиваемая категория</p></td>
  <td><p>Имена групп, созданных для указанной настраиваемой категории</p></td>
  </tr>
  </tbody>
  </table>

- Чтобы выполнить действие **NavigateTo** в модуле VBA, используйте метод **NavigateTo** объекта **DoCmd** .

> [!NOTE]
> Чтобы перейти к верхнему уровню категории (например, **ко всем таблицам**, ко **всем объектам Access**или **ко всем датам**), необходимо оставить аргумент группы пустым. Например, если аргумент **Category** имеет **тип Object**, то при вводе **всех объектов Access** в качестве аргумента **Group** возникает ошибка.


