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

Действие **NavigateTo** можно использовать для управления отображением объектов базы данных в области навигации. Например, можно изменить категорию объектов базы данных и отфильтровать их таким образом, чтобы отображались только определенные объекты.

## <a name="setting"></a>Setting

Действие **NavigateTo** имеет следующие аргументы.

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
<td><p>Обязательный. Категория, по которой в области навигации должны отображаться объекты. Щелкните <strong>"Тип объекта",</strong> <strong>"Таблицы и</strong> <strong>представления", "Дата изменения",</strong> <strong>"Дата создания"</strong>или <strong>"Настраиваемый"</strong> в поле <strong>"Категория".</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Group</strong></p></td>
<td><p>Необязательный параметр. Аргумент <strong>Group</strong> ограничивает, какие объекты в категории отображаются в области навигации. Если оставить аргумент <strong>Group</strong> пустым, в области навигации отображаются все объекты базы данных, классифицируются по критериям, заданной в <strong>аргументе Category.</strong> Примеры допустимого <strong>аргумента Group</strong> для различных <strong>аргументов Category</strong> показаны в следующей таблице.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Заметки

- Это действие аналогично выбору категорий и групп в заголовке панели навигации.

- **Допустимые** аргументы группы зависят **от используемой категории** аргумента. Если ввести недопустимый **аргумент Group,** появится сообщение об ошибке. В следующей таблице представлены примеры допустимого **аргумента Group** для каждого **аргумента Category.**
    
  <table>
  <colgroup>
  <col style="width: 50%" />
  <col style="width: 50%" />
  </colgroup>
  <thead>
  <tr class="header">
  <th><p>Аргумент category</p></th>
  <th><p>Примеры аргументов group</p></th>
  </tr>
  </thead>
  <tbody>
  <tr class="odd">
  <td><p>Тип объекта</p></td>
  <td><p>Таблицы; Forms; Запросы; Страницы; Макрос; Модули</p></td>
  </tr>
  <tr class="even">
  <td><p>Таблицы и представления</p></td>
  <td><p>Имена определенных таблиц в базе данных</p></td>
  </tr>
  <tr class="odd">
  <td><p>Дата изменения</p></td>
  <td><p>Сегодня; Сегодня; Last Month; Более старые</p></td>
  </tr>
  <tr class="even">
  <td><p>Created Date (дата создания)</p></td>
  <td><p>Сегодня; Сегодня; Last Month; Более старые</p></td>
  </tr>
  <tr class="odd">
  <td><p>Настраиваемая категория</p></td>
  <td><p>Имена групп, созданных для указанной настраиваемой категории</p></td>
  </tr>
  </tbody>
  </table>

- Чтобы запустить действие **NavigateTo** в модуле VBA, используйте метод **NavigateTo** объекта **DoCmd.**

> [!NOTE]
> Чтобы перейти на верхний уровень категории **(например,**"Все таблицы", "Все объекты доступа" или **"Все** даты"), необходимо оставить аргумент Group пустым. Например, если аргумент **category** имеет тип **объекта,** при  вводе всех объектов **Access** в качестве группового аргумента происходит ошибка.


