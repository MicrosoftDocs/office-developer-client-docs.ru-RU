---
title: Действия SetFilter макроса
TOCTitle: SetFilter Macro Action
ms:assetid: dee699e2-0840-1612-23ce-199ef8d30566
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835438(v=office.15)
ms:contentKeyID: 48548203
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm122943
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 4292ded0638e8dbe3ad56aa835caa9c6541f0432
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874316"
---
# <a name="setfilter-macro-action"></a>Действия SetFilter макроса

**Применимо к**: Access 2013, Office 2013

Чтобы применить фильтр в записи в активной таблицы, формы, отчета или в таблице можно использовать действие **SetFilter** .

## <a name="setting"></a>Параметр

Действие **SetFilter** имеет следующие аргументы.

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
<td><p>Имя фильтра</p></td>
<td><p>Если этот параметр указан, имя запроса или фильтра, сохраненный как запрос. Этот аргумент или аргумент WhereCondition требуется в базе данных клиента. В веб-база данных этот аргумент недоступен.</p></td>
</tr>
<tr class="even">
<td><p>Условие отбора</p></td>
<td><p>Если этот параметр указан, SQL предложения WHERE, которое ограничивает число записей в таблице данных, форме, отчете или таблице. В веб-база данных этот аргумент является обязательным.</p></td>
</tr>
<tr class="odd">
<td><p>Контрольное имя</p></td>
<td><p>Если этот параметр указан, имя элемента управления, соответствующее подчиненной формы или отчета для фильтрации. Если пустые, фильтруется текущий объект.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

В веб-база данных где условие аргумент не может начинаться с знак равенства (=).

При выполнении этого действия, чтобы таблицы, формы, отчета или таблицы данных (например, результат запроса), который является активным и фокус находится на применяется фильтр.

Свойство **фильтра** активного объекта используется для сохранения WhereCondition аргумент, применять в дальнейшем. Фильтры сохраняются вместе с объектами, в которых они созданы. Автоматически загружаются при открытии объекта, но они не применяются автоматически.

В базе данных клиента чтобы автоматически применить фильтр при открытии объекта, присвойте свойству **FilterOnLoad** значение True.

В веб-база данных автоматически применить фильтр при открытии объекта, добавьте действие **SetFilter** макроса и добавить макрос для объекта события **OnLoad** .

## <a name="example"></a>Пример

Следующем примере показано, как использовать действие SetFilter для фильтрации формы, в котором определен макрос.

**Пример кода предоставлен** [Справочник программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    OpenForm
        Form Name sfrmFoods
        View Form
        Filter Name
        Where Condition
        Data Mode
        Window Mode Normal
    
    SetFilter
        Filter Name
        Where Condtion =[display_name] Like "*cheese*"
        Control Name
```
