---
title: Макрокоманда ShowAllRecords
TOCTitle: ShowAllRecords macro action
ms:assetid: 6f9741ad-0440-4b8d-abea-009063c111f8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195587(v=office.15)
ms:contentKeyID: 48545538
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 201b284a56fbd3030b41a95424b41c73ee13e385
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308647"
---
# <a name="showallrecords-macro-action"></a>Макрокоманда ShowAllRecords


**Область применения**: Access 2013, Office 2013


С помощью действия **ShowAllRecords** можно удалить любой примененный фильтр из активной таблицы, набора результатов запроса или формы, а также отобразить все записи в таблице, наборе результатов или всех записях в таблице или запросе формы.

## <a name="setting"></a>Setting

Действие **ShowAllRecords** не имеет аргументов.

## <a name="remarks"></a>Заметки

Это действие позволяет убедиться, что все записи (включая любые измененные или новые) отображаются для таблицы, набора результатов запроса или формы. Это действие вызывает повторное затевещение записей для формы или подчиненной формы.

Это действие также можно использовать для удаления любого фильтра, примененного с помощью действия **ApplyFilter,** команды **Filter** на вкладке **"Главная"** или аргумента **Filter Name** or Where **Condition** действия **OpenForm.**

Это действие имеет тот же эффект, что  и нажатие кнопки  **"Toggle Filter"** на вкладке "Главная" или щелчок правой кнопкой мыши отфильтрованного поля и нажатие кнопки "Очистить фильтр" в представлении формы, представлении макета или в представлении таблицы.

Чтобы запустить действие **ShowAllRecords** в модуле Visual Basic для приложений (VBA), используйте метод **ShowAllRecords** объекта **DoCmd.**

## <a name="example"></a>Пример

**Применение фильтра с помощью макроса**

Следующий макрос содержит набор действий, каждый из которых фильтрует записи для формы списка телефонов клиентов. Здесь показано использование действий **ApplyFilter,** **ShowAllRecords** и **GoToControl.** Здесь также показано использование условий для определения того, какая кнопка-перегона в группе окна была выбрана в форме. Каждая строка действий связана с кнопкой-перемежатой кнопкой, которая выбирает набор записей, начиная с A, B, C и так далее, или всех записей. Этот макрос следует присоединить к событию **AfterUpdate** группы окну CompanyNameFilter.

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Condition</p></th>
<th><p>Макрокоманда</p></th>
<th><p>Аргументы: параметр</p></th>
<th><p>Примечание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>[Фильтры названия компании] =1</p></td>
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Where Condition</strong>: [Company Name] Like &quot; [AÀÁÂÃÃ]*&quot;</p></td>
<td><p>Фильтрация названий компаний, которые начинаются с A, À, Á, Â, Ã или Â.</p></td>
</tr>
<tr class="even">
<td><p>[Фильтры названия компании] =2</p></td>
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Where Condition</strong>: [Company Name] Like &quot; B*&quot;</p></td>
<td><p>Фильтрация названий компаний, которые начинаются с Б.</p></td>
</tr>
<tr class="odd">
<td><p>[Фильтры названия компании] =3</p></td>
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Where Condition</strong>: [Company Name] Like &quot; [CÇ]*&quot;</p></td>
<td><p>Фильтрация названий компаний, которые начинаются с C или Ç.</p></td>
</tr>
<tr class="even">
<td><p>... Строки действий для D-Y имеют тот же формат, что и строки С и C...</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>[Фильтры названия компании] =26</p></td>
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Where Condition</strong>: [Company Name] Like &quot; [Z ЖЕСТКИ]*&quot;</p></td>
<td><p>Фильтрация названий компаний, которые начинаются с Z, М, М или Д.</p></td>
</tr>
<tr class="even">
<td><p>[Фильтры названия компании] =27</p></td>
<td><p><strong>ShowAllRecords</strong></p></td>
<td><p></p></td>
<td><p>Показать все записи.</p></td>
</tr>
<tr class="odd">
<td><p>[RecordsetClone]. [RecordCount] &gt; 0</p></td>
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Имя управления</strong>: CompanyName</p></td>
<td><p>Если записи возвращаются для выбранной буквы, переместите фокус на управление CompanyName.</p></td>
</tr>
</tbody>
</table>

