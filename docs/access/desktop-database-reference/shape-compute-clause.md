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

Предложение COMPUTE фигуры создает родительский набор **записей,** столбцы которого состоят из ссылки на child **Recordset;** необязательные столбцы, содержимое которых является главой, новым или вычисляемым столбцом, или результатом выполнения агрегатных функций в наборе записей или ранее сформированном наборе **записей;**  и все столбцы из child **Recordset, перечисленные** в необязательном предложении BY.

## <a name="syntax"></a>Синтаксис

```vb 
 
SHAPE child-command [AS] child-alias 
   COMPUTE child-alias [[AS] name], [appended-column-list] 
   [BY grp-field-list] 
```

## <a name="description"></a>Описание

Часть этого предложения:

- *child-command*

  - Состоит из одного из следующих ок.
    
    - Команда запроса в фигурных скобках (" "), которая возвращает {} объект **объекта Recordset.** Команда передается основному поставщику данных, и ее синтаксис зависит от требований этого поставщика. Обычно это язык SQL, хотя ADO не требует определенного языка запросов.
    
    - Имя существующего фигурного **наборов записей.**
    
    - Другая команда фигуры.
    
    - Ключевое слово TABLE, за которым следует имя таблицы в поставщике данных.

- *child-alias*

  - Псевдоним, используемый для ссылки на **набор записей,** возвращаемого *командой-child.* *Псевдоним-потомок* требуется в списке столбцов в предложении COMPUTE и определяет отношение между родительским и родительским **объектами Recordset.**

- *appended-column-list*

  - Список, в котором каждый элемент определяет столбец в сформированных родительских элементах. Каждый элемент содержит столбец главы, новый столбец, вычисленный столбец или значение, которое является результатом агрегированной функции в наборе **записей.**

- *grp-field-list*

  - Список столбцов в родительских и родительских объектах **Recordset,** который указывает, как строки должны быть сгрупплены в потомке. Для каждого столбца в *списке grp-field-list* имеется соответствующий столбец в объектах child и parent **Recordset.** Для каждой строки в родительском наборе записей столбцы *списка grp-field-list* имеют уникальные значения, а набор записей, на который ссылается родительская строка, состоит исключительно из всех строк, столбцы списка *grp-field-list* которых имеют те же значения, что и родительская строка. 

Если предложение BY включено, строки этого наборов записей будут сгруппироваться на основе столбцов в предложении COMPUTE. Родительский **набор записей** будет содержать по одной строке для каждой группы строк в этом наборе **записей.**

Если предложение BY опущено,  весь набор записей будет рассматриваться как одна группа, а родительский набор **записей** будет содержать ровно одну строку. Эта строка будет ссылаться на весь набор **записей.** Опущение предложения BY позволяет вычислить итоговые суммы по всему набору **записей.**

Например:

```vb
    SHAPE {select * from Orders} AS orders
       COMPUTE orders, SUM(orders.OrderAmount) as TotalSales
```

Независимо от того,  каким образом формируется родительский набор записей (с помощью COMPUTE или APPEND), он будет содержать столбец главы, который используется для его отношения с набором **записей.** При желании родительский набор записей также может содержать столбцы, которые содержат сводки (SUM, MIN, MAX и так далее) по этим строкам.  Родительский и родительский набор записей могут содержать столбцы, содержащие выражение в строке в наборе записей, а также новые и изначально пустые столбцы.  

## <a name="operation"></a>Operation

The *child-command* is issued to the provider, which returns a child **Recordset**.

Предложение COMPUTE указывает столбцы родительского наборов записей, которые могут быть ссылкой на набор записей, один или несколько агрегатов, вычисленное выражение или новые столбцы.  Если есть предложение BY, определенные в нем столбцы также будут приданы родительскому **набору записей.** Предложение BY указывает, как группировать строки из этого **наборов** записей.

Например, предположим, что у вас есть таблица "Демографические данные", состоящая из полей "State", "City" и "Population" (рисунки исключительно для иллюстрации).

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
<th><p>Population</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>WA</p></td>
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
<td><p>ЦС</p></td>
<td><p>Нью-Йорк</p></td>
<td><p>800,000</p></td>
</tr>
<tr class="odd">
<td><p>ЦС</p></td>
<td><p>Сан-Кио</p></td>
<td><p>600 000</p></td>
</tr>
<tr class="even">
<td><p>WA</p></td>
<td><p>Такома</p></td>
<td><p>500 000</p></td>
</tr>
<tr class="odd">
<td><p>ИЛИ</p></td>
<td><p>Corvallis</p></td>
<td><p>300,000</p></td>
</tr>
</tbody>
</table>


Теперь выдаем данной команде фигуры:

```vb 
 
rst.Open  "SHAPE {select * from demographics} AS rs "  & _ 
          "COMPUTE rs, SUM(rs.population) BY state", _ 
           objConnection 
```

Эта команда открывает фигурный набор **записей с** двумя уровнями. Родительский уровень —  это созданный набор записей со сводным столбцом (SUM(rs.population) ), столбцом, ссылаясь на потомок **recordset** (rs) и столбцом для группировки child **Recordset** (state). Уровень потомка  — это набор записей, возвращаемой командой запроса (), столбец, ссылающийся на потомок **Recordset** (rs), и столбец для группировки child **Recordset** (state). Уровень child — это **набор записей,** возвращаемой командой запроса (выберите \* из демографических данных).

Строки **подробных данных в** наборе записей будут сгруппироваться по состояниям, но в противном случае в определенном порядке. То есть группы не будут в алфавитном или числовом порядке. Если необходимо указать **родительский** набор записей, можно использовать метод **Recordset** **Sort** для упорядочения родительского **recordset.**

Теперь вы можете перемещаться по открытому родительскому набору **записей** и получать доступ к объектам **объекта Recordset для подробных данных.** Дополнительные сведения см. в подсети "Доступ к [строкам в иерархическом наборе записей".](accessing-rows-in-a-hierarchical-recordset.md)

**Resultant Parent and Child Detail Recordsets**

**Parent**

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>SUM (rs. Population)</p></th>
<th><p>rs</p></th>
<th><p>Состояние</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1,300,000</p></td>
<td><p>Ссылка на child1</p></td>
<td><p>ЦС</p></td>
</tr>
<tr class="even">
<td><p>1,200,000</p></td>
<td><p>Ссылка на child2</p></td>
<td><p>WA</p></td>
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
<th><p>Population</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>ЦС</p></td>
<td><p>Нью-Йорк</p></td>
<td><p>800,000</p></td>
</tr>
<tr class="even">
<td><p>ЦС</p></td>
<td><p>Сан-Кио</p></td>
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
<th><p>Population</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>WA</p></td>
<td><p>Сиэтл</p></td>
<td><p>700,000</p></td>
</tr>
<tr class="even">
<td><p>WA</p></td>
<td><p>Такома</p></td>
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
<th><p>Population</p></th>
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

