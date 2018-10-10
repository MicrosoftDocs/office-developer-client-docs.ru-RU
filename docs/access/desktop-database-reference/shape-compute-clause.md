---
title: Shape Compute Clause
TOCTitle: Shape Compute Clause
ms:assetid: f4fee4a6-ec9e-c0b6-40e0-258f76c4696f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250245(v=office.15)
ms:contentKeyID: 48548699
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 634a0ea648646d95995054ce7458cea492c40e47
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482942"
---
# <a name="shape-compute-clause"></a>Shape Compute Clause

**Применимо к**: Access 2013 | Office 2013

Предложение COMPUTE фигуры создает родительский объект **набора записей**, столбцы которых состоят из ссылки на дочерних **записей**; необязательные столбцы, содержимое которых главы новыми, или вычисляемых столбцов или в результате выполнения агрегатных функций на дочерних **записей** или ранее формы **набора записей**; и все столбцы из дочерних **записей** из списка в необязательном ПРЕДЛОЖЕНИЕМ.

## <a name="syntax"></a>Синтаксис

```vb 
 
SHAPE child-command [AS] child-alias 
   COMPUTE child-alias [[AS] name], [appended-column-list] 
   [BY grp-field-list] 
```

## <a name="description"></a>Описание

Части это предложение, следующим образом:

- *Команда дочерних*

  - Состоит из одной из следующих:
    
    - Команды запроса в фигурные скобки (»{}«), который возвращает дочернего объекта **набора записей** . Команды для базового поставщика данных, и его синтаксис зависит от требований этого поставщика. Обычно это будет языка SQL, несмотря на то, что ADO не требуется любой язык, определенного запроса.
    
    - Имя существующего форме **набора записей**.
    
    - Другой команды фигуры.
    
    - В ТАБЛИЦЕ ключевого слова, за которым следует имя таблицы в поставщике данных.

- *псевдоним дочерних*

  - Псевдоним, используемое для ссылки на **набор записей** , возвращаемых *дочерних command.* *Псевдоним дочерних* требуется в список столбцов в предложении COMPUTE и определяет отношение между родительских и дочерних объектов **набора записей** .

- *добавлено--список столбцов*

  - Список, в котором каждый элемент определяет столбец в созданный родительского. Каждый элемент содержит столбец, новый столбец, вычисляемый столбец или значение, полученное статистические функции на дочерних **записей**.

- *Список полей группу*

  - Список столбцов в родительских и дочерних объектов **набора записей** , который определяет группировку строк в дочернем. Для каждого столбца в *группу--список полей,* существует соответствующий столбец дочерних и родительских объектов **набора записей** . Для каждой строки в родительском **записей**столбцы *списка полей группу* иметь уникальные значения и дочерних **записей** ссылается родительской строки состоит только из дочерних строк, *список полей группу* столбцы имеют те же значения, как родительской строки.

Если предложение по включено, дочерних **записей**в строках будут группироваться основанным на столбцы в предложении COMPUTE. Родительский **набор записей** будет содержать одну строку для каждой группы строк в дочерних **записей**.

Если предложение по указано, все дочерние **записей** обрабатывается как единая группа и родительских **записей** будет содержать только одну строку. Соответствующая строка ссылаются на всей дочерних **записей**. Пропуск предложения по позволяет вычисления «Итого» статистических данных по всей дочерних **записей**.

Пример:

```vb
    SHAPE {select * from Orders} AS orders
       COMPUTE orders, SUM(orders.OrderAmount) as TotalSales
```

Независимо от того, какой способ родительского **набора записей** сформирован (с помощью COMPUTE или APPEND) он будет содержать столбец, используемый для связи дочерних **записей**. Если вы хотите родительского **набора записей** также может содержать столбцы, содержащие статистические функции (SUM, MIN, MAX и т.д.) через дочерние строки. Родительских и дочерних **записей** может содержать столбцы, которые содержат выражения в строке, в **набор записей**, а также столбцы, которые являются новыми и изначально очистить.

## <a name="operation"></a>Операция

*Команда дочерних* должен быть выдан поставщика, который возвращает дочерний элемент **набора записей**.

Предложение COMPUTE указывает столбцы родительского **набора записей**, который может быть ссылку на дочерних **записей**, статистические выражения на один или несколько, расчетного выражения или новых столбцов. В случае предложение BY столбцы, которые он определяет также присоединяются к родительского **набора записей**. Предложение по указывает способ группировки строк дочерних **записей** .

Предположим, у вас есть таблицы — демографии, состоящий из состояний, города и заполнения полей (данные совокупности предназначены исключительно для иллюстрации).

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>State</p></th>
<th><p>City</p></th>
<th><p>Заполнение</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>ШТАТ ВАШИНГТОН</p></td>
<td><p>Сиэтл</p></td>
<td><p>700 000</p></td>
</tr>
<tr class="even">
<td><p>OR</p></td>
<td><p>Medford</p></td>
<td><p>200 000</p></td>
</tr>
<tr class="odd">
<td><p>OR</p></td>
<td><p>Портленд</p></td>
<td><p>400 000 долларов</p></td>
</tr>
<tr class="even">
<td><p>ЦЕНТР СЕРТИФИКАЦИИ</p></td>
<td><p>Лос-Анджелес</p></td>
<td><p>800,000</p></td>
</tr>
<tr class="odd">
<td><p>ЦЕНТР СЕРТИФИКАЦИИ</p></td>
<td><p>Москва</p></td>
<td><p>600 000</p></td>
</tr>
<tr class="even">
<td><p>ШТАТ ВАШИНГТОН</p></td>
<td><p>Москва</p></td>
<td><p>500 000</p></td>
</tr>
<tr class="odd">
<td><p>OR</p></td>
<td><p>Corvallis</p></td>
<td><p>300 000</p></td>
</tr>
</tbody>
</table>


Теперь выполните эту команду фигуры:

```vb 
 
rst.Open  "SHAPE {select * from demographics} AS rs "  & _ 
          "COMPUTE rs, SUM(rs.population) BY state", _ 
           objConnection 
```

Эта команда открывает формы **набора записей** с двумя уровнями. Родительский уровень — это созданный **набора записей** с составного столбца (SUM(rs.population)), столбец, создание ссылок на дочерних **записей** (rs) и столбца для группировки дочерних **записей** (состояние). Дочерний уровень — это **набор записей** , возвращаемых () команду запроса, столбец, создание ссылок на дочерних **записей** (rs) и столбца для группировки дочерних **записей** (состояние). Уровень дочерних — это **набор записей** , возвращаемые командой запроса (выберите \* из демографии).

Строки сведений о дочерних **наборов записей** будут, сгруппированных по состоянию, но в произвольном порядке, в противном случае —. То есть группы не будет находиться в или алфавитном порядке. Если вы хотите родительского **набора записей** упорядоченный, можно использовать метод **сортировки** **набора записей** для упорядочения родительского **набора записей**.

Теперь можно перейдите открыт родительского **набора записей** и доступ к сведений о **записей** дочерние объекты. Для получения дополнительных сведений см. [Доступ к строк в иерархической записей](accessing-rows-in-a-hierarchical-recordset.md).

**Результирующее родительских и дочерних наборов записей подробно**

**Parent**

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Сумма (rs. Заполнение)</p></th>
<th><p>RS</p></th>
<th><p>State</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1,300,000</p></td>
<td><p>Ссылка на child1</p></td>
<td><p>ЦЕНТР СЕРТИФИКАЦИИ</p></td>
</tr>
<tr class="even">
<td><p>1,200,000</p></td>
<td><p>Ссылка на child2</p></td>
<td><p>ШТАТ ВАШИНГТОН</p></td>
</tr>
<tr class="odd">
<td><p>1,100,000</p></td>
<td><p>Ссылка на child3</p></td>
<td><p>OR</p></td>
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
<th><p>State</p></th>
<th><p>City</p></th>
<th><p>Заполнение</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>ЦЕНТР СЕРТИФИКАЦИИ</p></td>
<td><p>Лос-Анджелес</p></td>
<td><p>800,000</p></td>
</tr>
<tr class="even">
<td><p>ЦЕНТР СЕРТИФИКАЦИИ</p></td>
<td><p>Москва</p></td>
<td><p>600 000</p></td>
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
<th><p>State</p></th>
<th><p>City</p></th>
<th><p>Заполнение</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>ШТАТ ВАШИНГТОН</p></td>
<td><p>Сиэтл</p></td>
<td><p>700 000</p></td>
</tr>
<tr class="even">
<td><p>ШТАТ ВАШИНГТОН</p></td>
<td><p>Москва</p></td>
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
<th><p>State</p></th>
<th><p>City</p></th>
<th><p>Заполнение</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>OR</p></td>
<td><p>Medford</p></td>
<td><p>200 000</p></td>
</tr>
<tr class="even">
<td><p>OR</p></td>
<td><p>Портленд</p></td>
<td><p>400 000 долларов</p></td>
</tr>
<tr class="odd">
<td><p>OR</p></td>
<td><p>Corvallis</p></td>
<td><p>300 000</p></td>
</tr>
</tbody>
</table>
