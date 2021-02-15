---
title: Макрокоманда SearchForRecord
TOCTitle: SearchForRecord macro action
ms:assetid: a3483c41-adb5-5923-55f4-1a3c4f60cb2f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821023(v=office.15)
ms:contentKeyID: 48546781
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm118713
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: efa763a77250e1d5c617358f31421804c772468b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314646"
---
# <a name="searchforrecord-macro-action"></a>Макрокоманда SearchForRecord


**Область применения**: Access 2013, Office 2013

Вы можете использовать **действие SearchForRecord** для поиска определенной записи в таблице, запросе, форме или отчете.

## <a name="setting"></a>Setting

Действие **SearchForRecord** имеет следующие аргументы.

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
<td><p>Введите или выберите тип объекта базы данных, в которой вы ищете. Можно выбрать <strong>"Таблица",</strong> <strong>"Запрос",</strong> <strong>"Форма"</strong>или <strong>"Отчет".</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Object Name</strong></p></td>
<td><p>Введите или выберите конкретный объект, содержащий запись для поиска. В выпадаемом списке показаны все объекты базы данных типа, выбранного для <strong>аргумента Object Type.</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>Record</strong></p></td>
<td><p>Укажите точки начала и направление поиска.</p>
<div class="tableSection">
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Setting</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Previous</strong></p></td>
<td><p>Поиск в обратном направлении от текущей записи.</p></td>
</tr>
<tr class="even">
<td><p><strong>Next</strong></p></td>
<td><p>Поиск вперед из текущей записи.</p></td>
</tr>
<tr class="odd">
<td><p><strong>First</strong></p></td>
<td><p>Поиск вперед из первой записи. Это значение по умолчанию для этого аргумента.</p></td>
</tr>
<tr class="even">
<td><p><strong>Last</strong></p></td>
<td><p>Поиск в обратном направлении от последней записи.</p></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><p><strong>Where Condition</strong></p></td>
<td><p>Введите критерии поиска, используя тот же синтаксис, что и SQL WHERE, только без слова &quot; &quot; WHERE. Пример.</p>
<p>`Description = "Beverages"`</p>
<p>Чтобы создать критерий, который включает значение из текстового поле в форме, необходимо создать выражение, которое совмещая первую часть условия с именем текстового окна, содержащего значение, по которому следует искать. Например, следующий критерий будет искать значение в текстовом поле с именем txtDescription в форме frmCategories. Обратите внимание на знак равного () в начале выражения и использование одиночных кавычках ( ' ) с любой стороны ссылки <strong>=</strong> на текстовое<strong></strong>поле:</p>
<p>`="Description = ' " & Forms![frmCategories]![txtDescription] & "'"`</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Заметки

- В случаях, когда несколько записей соответствуют условиям в аргументе **Where Condition,** то, какая запись найдена, определяются следующими факторами:
    
  - **Параметр аргумента Record** Дополнительные сведения о аргументе **Record** см. в таблице в разделе "Параметры".
    
  - **Порядок сортировки записей** Например, если для аргумента **Record** установлено первое, изменение порядка сортировки записей может изменить найденную запись.

- Объект, указанный в **аргументе Object Name,** должен быть открыт перед запуском этого действия. В противном случае возникает ошибка.

- Если критерии в аргументе **Where Condition** не выполнены, ошибка не возникает, и фокус остается на текущей записи.

- При поиске предыдущей или следующей записи поиск не "обтекает", когда достигает конца данных. Если дополнительные записи, которые соответствуют условиям, не возникают ошибки и фокус остается на текущей записи. Чтобы убедиться, что совпадение найдено, можно ввести условие для следующего действия и сделать условие тем же, что и условие в аргументе **Where Condition.**

- Чтобы запустить **действие SearchForRecord** в модуле VBA, используйте метод **SearchForRecord** объекта **DoCmd.**

- Действие **SearchForRecord** аналогично действию **[FindRecord,](findrecord-macro-action.md)** но **SearchForRecord** имеет более мощные функции поиска. Действие **FindRecord** в основном используется для поиска строк и дублирует  функции диалоговых окна "Найти". Действие **SearchForRecord** использует условия, которые больше похожи на условия фильтра или SQL запроса. В следующем списке демонстрируются некоторые действия, которые можно сделать с **действием SearchForRecord:**
    
  - В аргументе Where **Condition** можно использовать сложные критерии, например
        
    `Description = "Beverages" and CategoryID = 11`
    
  - Вы можете ссылаться на поля, которые находятся в источнике записей формы или отчета, но не отображаются в форме или отчете. В предыдущем примере описание и CategoryID не должны отображаться в форме или отчете, чтобы критерии работали.
    
  - Вы можете использовать логические операторы, такие как **\<** **\>** , , **AND**, OR , **и** **BETWEEN**. Действие **FindRecord** соединит только строки, которые совпадают, начинаются со строки, для которых ведется поиск, или содержат ее.

## <a name="example"></a>Пример

Следующий макрос сначала открывает таблицу Categories с помощью действия **OpenTable.** Затем макрос использует действие **SearchForRecord** для поиска первой записи в таблице, в которой поле "Описание" равно "Пособники".

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Action</p></th>
<th><p>Аргументы</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>OpenTable</strong></p></td>
<td><p><strong>Имя таблицы</strong>: Categories<strong>View</strong>: <strong>DatasheetData Mode</strong>: <strong>Edit</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>SearchForRecord</strong></p></td>
<td><p><strong>Тип объекта</strong>: <strong>TableObject Name</strong>: Categories<strong>Record</strong>: <strong>FirstWhere Condition</strong>: Description &quot; =Ies&quot;</p></td>
</tr>
</tbody>
</table>

