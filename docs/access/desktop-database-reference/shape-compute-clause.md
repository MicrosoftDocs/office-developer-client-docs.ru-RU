---
title: Предложение Compute команды Shape
TOCTitle: Shape Compute clause
ms:assetid: f4fee4a6-ec9e-c0b6-40e0-258f76c4696f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250245(v=office.15)
ms:contentKeyID: 48548699
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: eadc448d59814f0573a959c6c1038f9c4afdbac9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306456"
---
# <a name="shape-compute-clause"></a>Предложение Compute команды Shape

**Область применения**: Access 2013, Office 2013

Положение COMPUTE формы создает родительский **набор записей,** столбцы которого состоят из ссылки на детский **набор записей;** необязательные столбцы, содержимое которых — это главы, новые или рассчитанные столбцы, или результат выполнения совокупных функций в детском наборе записей или ранее сформированном **Наборе записей;**  и любые столбцы из списка **записей ребенка,** указанные в необязательных статьях BY.

## <a name="syntax"></a>Синтаксис

```vb 
 
SHAPE child-command [AS] child-alias 
   COMPUTE child-alias [[AS] name], [appended-column-list] 
   [BY grp-field-list] 
```

## <a name="description"></a>Описание

Части этого положения:

- *детская команда*

  - Состоит из одного из следующих:
    
    - Команда запроса в фигурных скобки ("), которая {} возвращает объект **recordset** ребенка. Команда выдана основному поставщику данных, и ее синтаксис зависит от требований этого поставщика. Обычно это будет язык SQL, хотя ADO не требует какого-либо конкретного языка запросов.
    
    - Имя существующего формы **Recordset**.
    
    - Еще одна команда фигуры.
    
    - Ключевое слово TABLE с именем таблицы в поставщике данных.

- *псевдоним ребенка*

  - Псевдоним, используемый для ссылки на **набор записей,** возвращенный *детской командой.* Псевдоним *ребенка* требуется в списке столбцов в статье COMPUTE и определяет связь между родительскими и детскими **объектами Recordset.**

- *appended-column-list*

  - Список, в котором каждый элемент определяет столбец в сгенерированной родительской. Каждый элемент содержит столбец главы, новый столбец, вычисляемую колонку или значение, которое является результатом совокупной функции в детском **наборе записей.**

- *grp-field-list*

  - Список столбцов в родительских и детских объектах **Recordset,** который указывает, как следует сгруппировать строки в ребенке. Для каждого столбца в *списке grp-field имеется* соответствующий столбец в объектах **recordset** для детей и родителей. Для каждой строки в родительском Наборе записей столбцы списков grp-field имеют уникальные значения, а детский набор записей, на который ссылается родительская строка, состоит исключительно из детских строк, столбцы которых  *grp-field-list* имеют те же значения, что и родительская строка. 

Если предложение BY включено, строки записи ребенка будут сгруппироваться на основе столбцов в пункте COMPUTE. Родительский **набор записей** будет содержать по одной строке для каждой группы строк в детском **наборе записей.**

Если предложение BY опущено,  весь набор записей для детей рассматривается как одна группа, а родительский набор **записей** будет содержать ровно одну строку. Эта строка будет ссылаться на весь набор **записей ребенка**. Опущение пункта BY позволяет вычислять совокупные суммы по всему детскому **набору записей.**

Пример.

```vb
    SHAPE {select * from Orders} AS orders
       COMPUTE orders, SUM(orders.OrderAmount) as TotalSales
```

Независимо от того,  каким образом формируется родительский набор записей (с помощью COMPUTE или с помощью APPEND), он будет содержать столбец главы, который используется для его соотноски с ребенком **Recordset**. При желании родительский набор **записей** также может содержать столбцы, содержащие сводки (SUM, MIN, MAX и так далее) над детскими строками. Родительский и детский  набор записей могут содержать столбцы, содержащие выражение строки в Наборе записей, а также столбцы, которые являются новыми и изначально пустыми.

## <a name="operation"></a>Операция

Команда *для детей* выдана поставщику, который возвращает детский набор **записей.**

В статье COMPUTE указаны столбцы родительского набора записей, которые могут быть ссылкой на детский набор записей, один или несколько агрегатов, вычислимое выражение или новые столбцы. Если есть пункт BY, столбцы, которые он определяет, также примыкают к родительскому **набору записей.** В статье BY указывается, как сгруппировать строки детского **набора** записей.

Например, предположим, что у вас есть таблица — Демографические поля, состоящие из областей состояния, города и населения (цифры населения являются исключительно иллюстрациями).

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Состояние</p></th>
<th><p>Город</p></th>
<th><p>Население</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Wa</p></td>
<td><p>Сиэтл</p></td>
<td><p>700,000</p></td>
</tr>
<tr class="even">
<td><p>ИЛИ</p></td>
<td><p>Medford</p></td>
<td><p>200 000</p></td>
</tr>
<tr class="odd">
<td><p>ИЛИ</p></td>
<td><p>Портленд</p></td>
<td><p>400,000</p></td>
</tr>
<tr class="even">
<td><p>CA</p></td>
<td><p>Лос-Анджелес</p></td>
<td><p>800,000</p></td>
</tr>
<tr class="odd">
<td><p>CA</p></td>
<td><p>Сан-Диего</p></td>
<td><p>600 000</p></td>
</tr>
<tr class="even">
<td><p>Wa</p></td>
<td><p>Tacoma</p></td>
<td><p>500 000</p></td>
</tr>
<tr class="odd">
<td><p>ИЛИ</p></td>
<td><p>Corvallis</p></td>
<td><p>300,000</p></td>
</tr>
</tbody>
</table>


Теперь выдай эту команду фигуры:

```vb 
 
rst.Open  "SHAPE {select * from demographics} AS rs "  & _ 
          "COMPUTE rs, SUM(rs.population) BY state", _ 
           objConnection 
```

Эта команда открывает сформированный **набор записей с** двумя уровнями. Родительский уровень —  это созданный набор записей со сводным столбцом (SUM(rs.population), столбец, ссылающийся на детский набор записей  (rs) и столбец для группировки детского **recordset** (состояние). Уровень ребенка —  это набор записей, возвращаемый командой запроса (), столбец, отсылающий к детскому набору записей  (rs) и столбец для группировки ребенка **Recordset** (состояние). Уровень ребенка — это **набор записей,** возвращаемый командой запросов (выберите \* из демографических показателей).

Строки **данных о** ребенке будут сгруппироваться по состояниям, но в противном случае не будут в определенном порядке. То есть группы не будут в алфавитном или числовом порядке. Если необходимо заказать **родительский** набор записей, можно заказать родительский набор записей с помощью метода  **сортировки** **recordset.**

Теперь можно перемещаться по открываемой родительской **записи и** получать доступ к объектам **учетной** записи для детей. Дополнительные сведения см. [в рублях Accessing Rows in a Hierarchical Recordset.](accessing-rows-in-a-hierarchical-recordset.md)

**Итоги записей родительских и детских деталей**

**Parent**

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>SUM (rs. Население)</p></th>
<th><p>rs</p></th>
<th><p>Состояние</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1,300,000</p></td>
<td><p>Ссылка на child1</p></td>
<td><p>CA</p></td>
</tr>
<tr class="even">
<td><p>1,200,000</p></td>
<td><p>Ссылка на child2</p></td>
<td><p>Wa</p></td>
</tr>
<tr class="odd">
<td><p>1,100,000</p></td>
<td><p>Ссылка на child3</p></td>
<td><p>ИЛИ</p></td>
</tr>
</tbody>
</table>


**Child1**

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Состояние</p></th>
<th><p>Город</p></th>
<th><p>Население</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>CA</p></td>
<td><p>Лос-Анджелес</p></td>
<td><p>800,000</p></td>
</tr>
<tr class="even">
<td><p>CA</p></td>
<td><p>Сан-Диего</p></td>
<td><p>600 000</p></td>
</tr>
</tbody>
</table>


**Child2**

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Состояние</p></th>
<th><p>Город</p></th>
<th><p>Население</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Wa</p></td>
<td><p>Сиэтл</p></td>
<td><p>700,000</p></td>
</tr>
<tr class="even">
<td><p>Wa</p></td>
<td><p>Tacoma</p></td>
<td><p>500 000</p></td>
</tr>
</tbody>
</table>


**Child3**

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Состояние</p></th>
<th><p>Город</p></th>
<th><p>Население</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>ИЛИ</p></td>
<td><p>Medford</p></td>
<td><p>200 000</p></td>
</tr>
<tr class="even">
<td><p>ИЛИ</p></td>
<td><p>Портленд</p></td>
<td><p>400,000</p></td>
</tr>
<tr class="odd">
<td><p>ИЛИ</p></td>
<td><p>Corvallis</p></td>
<td><p>300,000</p></td>
</tr>
</tbody>
</table>

