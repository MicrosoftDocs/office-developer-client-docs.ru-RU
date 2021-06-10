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

## <a name="setting"></a>Параметр

Действие **SearchForRecord имеет** следующие аргументы.

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
<td><p>Введите или выберите тип объекта базы данных, в который вы ищете. Вы можете выбрать <strong>таблицу,</strong> <strong>запрос,</strong> <strong>форму</strong>или <strong>отчет.</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Object Name</strong></p></td>
<td><p>Введите или выберите определенный объект, содержащий запись для поиска. В выпадаемом списке показаны все объекты базы данных типа, выбранного для <strong>аргумента Object Type.</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>Record</strong></p></td>
<td><p>Укажите отправную точку и направление поиска.</p>
<div class="tableSection">
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Параметр</p></th>
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
<td><p>Поиск назад из последней записи.</p></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><p><strong>Где состояние</strong></p></td>
<td><p>Введите критерии поиска, используя тот же синтаксис, что и SQL where, только без &quot; слова WHERE &quot; . Пример.</p>
<p>`Description = "Beverages"`</p>
<p>Чтобы создать критерий, содержащий значение из текстового окна в форме, необходимо создать выражение, которое соединять первую часть критерия с именем текстового окна, содержащего значение, для которого необходимо искать. Например, следующий критерий будет искать в поле Описание значение в текстовом поле с именем txtDescription в форме с именем frmCategories. Обратите внимание на равный знак () в начале выражения и использование одиночных кавычках ( ' ) по обе стороны ссылки <strong>=</strong> на текстовое<strong></strong>поле:</p>
<p>`="Description = ' " & Forms![frmCategories]![txtDescription] & "'"`</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

- В тех случаях, когда несколько записей соответствуют критериям аргумента **Where Condition,** следующие факторы определяют, какая запись найдена:
    
  - **Параметр Аргумент Записи** Дополнительные сведения о аргументе Запись см. в Параметры в разделе **"Запись".**
    
  - **Порядок сортировки записей** Например, если аргумент **Записи** настроен на **First,** изменение порядка сортировки записей может изменить найденную запись.

- Объект, указанный в **аргументе "Имя объекта",** должен быть открыт перед запуском этого действия. В противном случае возникает ошибка.

- Если критерии в аргументе **Where Condition** не выполнены, ошибка не возникает, и основное внимание остается на текущей записи.

- При поиске предыдущей или следующей записи поиск не "оборачивается", когда достигает конца данных. Если нет дополнительных записей, которые соответствуют критериям, ошибки не происходит, и основное внимание остается на текущей записи. Чтобы убедиться в обнаружении совпадения, можно ввести условие для следующего действия и сделать условие таким же, как и критерии в аргументе **Where Condition.**

- Чтобы выполнить **действие SearchForRecord** в модуле VBA, используйте метод **SearchForRecord** объекта **DoCmd.**

- Действие **SearchForRecord** аналогично действию **[FindRecord,](findrecord-macro-action.md)** но **SearchForRecord имеет** более мощные функции поиска. Действие **FindRecord** используется в основном для поиска строк и дублирует функции диалогового окна **Find.** Действие **SearchForRecord использует** критерии, которые больше похожи на критерии фильтра или SQL запроса. В следующем списке показано, что можно сделать с действием **SearchForRecord:**
    
  - В аргументе Where **Condition** можно использовать сложные критерии, такие как
        
    `Description = "Beverages" and CategoryID = 11`
    
  - Вы можете ссылаться на поля, которые находятся в источнике записи формы или отчета, но не отображаются в форме или отчете. В предыдущем примере ни Описание, ни CategoryID не должны отображаться в форме или отчете для работы критериев.
    
  - Вы можете использовать логических операторов, таких как **\<** , И , ИЛИ , **\>** **и** **МЕЖДУ**.  Действие **FindRecord** совпадает только со строками, которые равны, начинаются с строки, для которых ведется поиск, или содержат ее.

## <a name="example"></a>Пример

Следующий макрос открывает таблицу Категорий с помощью **действия OpenTable.** Затем макрос использует **действие SearchForRecord** для поиска первой записи в таблице, где поле Description равно "Напитки".

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
<td><p><strong>Имя</strong>таблицы:<strong></strong>Просмотр категорий: <strong>Режим DatasheetData</strong>: <strong>Изменение</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>SearchForRecord</strong></p></td>
<td><p><strong>Тип объекта:</strong> <strong>Имя TableObject</strong>: Запись категорий<strong>:</strong>Состояние <strong>FirstWhere</strong>: Описание = &quot; Напитки&quot;</p></td>
</tr>
</tbody>
</table>

