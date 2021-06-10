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


Вы можете использовать действие **ShowAllRecords** для удаления любого примененного фильтра из активной таблицы, набора результатов запроса или формы и отображения всех записей в таблице или наборе результатов или всех записей в таблице или запросе формы.

## <a name="setting"></a>Параметр

Действие **ShowAllRecords** не имеет аргументов.

## <a name="remarks"></a>Примечания

Это действие можно использовать для отображения всех записей (включая измененные или новые) для таблицы, набора результатов запроса или формы. Это действие вызывает requery записей для формы или подформы.

Это действие также можно использовать для удаления любого фильтра, применяемого  с помощью действия **ApplyFilter,** команды Filter на вкладке **Home** или аргумента **Filter Name** or **Where Condition** действия **OpenForm.**

Это действие имеет тот же эффект, что  щелкнуть фильтр **Toggle** на вкладке Home или щелкнуть правой кнопкой мыши фильтрованное поле и щелкнуть фильтр **Clear из...** в представлении формы, представлении макета или представлении таблицы данных.

Чтобы выполнить действие **ShowAllRecords** в модуле Visual Basic для приложений (VBA), используйте метод **ShowAllRecords** объекта **DoCmd.**

## <a name="example"></a>Пример

**Применение фильтра с помощью макроса**

Следующий макрос содержит набор действий, каждый из которых фильтрует записи для формы списка Телефон клиента. В нем показано использование действий **ApplyFilter,** **ShowAllRecords** и **GoToControl.** В нем также показано использование условий для определения того, какая кнопка для включения в группу опций была выбрана в форме. Каждая строка действий связана с кнопкой toggle, которая выбирает набор записей, начиная с A, B, C и так далее или всех записей. Этот макрос должен быть присоединен к событию **AfterUpdate** группы параметра CompanyNameFilter.

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Условие</p></th>
<th><p>Макрокоманда</p></th>
<th><p>Аргументы: параметр</p></th>
<th><p>Примечание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>[Фильтры имени компании] =1</p></td>
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Где условие:</strong>[имя компании] Как &quot; [AÀÁÂÃÄ]*&quot;</p></td>
<td><p>Фильтр для имен компаний, которые начинаются с A, À, Á, Â, Ã или Ä.</p></td>
</tr>
<tr class="even">
<td><p>[Фильтры имени компании] =2</p></td>
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Где условие</strong>: [Имя компании] Как &quot; B*&quot;</p></td>
<td><p>Фильтр для имен компаний, которые начинаются с B.</p></td>
</tr>
<tr class="odd">
<td><p>[Фильтры имени компании] =3</p></td>
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Где условие:</strong>[Имя компании] Как &quot; [CÇ]*&quot;</p></td>
<td><p>Фильтр для имен компаний, которые начинаются с C или Ç.</p></td>
</tr>
<tr class="even">
<td><p>... Строки действия для D до Y имеют тот же формат, что и A through C ...</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>[Фильтры имени компании] =26</p></td>
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Где условие:</strong>[имя компании] Как &quot; [ZÆØÅ]*&quot;</p></td>
<td><p>Фильтр для имен компаний, которые начинаются с Z, Æ, Ø или Å.</p></td>
</tr>
<tr class="even">
<td><p>[Фильтры имени компании] =27</p></td>
<td><p><strong>ShowAllRecords</strong></p></td>
<td><p></p></td>
<td><p>Показать все записи.</p></td>
</tr>
<tr class="odd">
<td><p>[RecordsetClone]. [RecordCount] &gt; 0</p></td>
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Имя управления:</strong>CompanyName</p></td>
<td><p>Если записи возвращаются для выбранного письма, переместите фокус на управление CompanyName.</p></td>
</tr>
</tbody>
</table>

