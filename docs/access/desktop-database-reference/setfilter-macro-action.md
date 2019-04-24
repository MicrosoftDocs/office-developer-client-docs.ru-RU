---
title: Макрокоманда SetFilter
TOCTitle: SetFilter macro action
ms:assetid: dee699e2-0840-1612-23ce-199ef8d30566
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835438(v=office.15)
ms:contentKeyID: 48548203
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm122943
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: ac1a2c8a603fb74b56d71f73605455ecdbc87035
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308696"
---
# <a name="setfilter-macro-action"></a>Макрокоманда SetFilter

**Область применения**: Access 2013, Office 2013

Вы можете использовать действие **SetFilter** , чтобы применить фильтр к записям в активной таблице, форме, отчете или таблице.

## <a name="setting"></a>Параметр

Макрокоманда **SetFilter** имеет следующие аргументы.

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
<td><p>Если этот параметр указан, имя запроса или фильтра сохраняется как запрос. Этот аргумент или аргумент WhereCondition является обязательным в клиентской базе данных. В веб-базе данных этот аргумент недоступен.</p></td>
</tr>
<tr class="even">
<td><p>Условие отбора</p></td>
<td><p>Если этот параметр указан, предложение WHERE (SQL), которое ограничит записи в таблице, форме, отчете или таблице. В веб-базе данных этот аргумент является обязательным.</p></td>
</tr>
<tr class="odd">
<td><p>Контрольное имя</p></td>
<td><p>Если этот параметр указан, то имя элемента управления, соответствующего подчиненной форме или подчиненному отчету, который будет фильтроваться. Если этот параметр не задан, то фильтруется текущий объект.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

В веб-базе данных аргумент условия WHERE не может начинаться со знака равенства (=).

При выполнении этого действия фильтр применяется к таблице, форме, отчету или таблице (например, результату запроса), которая активна и находится в фокусе.

Свойство **Filter** активного объекта используется для сохранения аргумента WhereCondition и его применения в дальнейшем. Фильтры сохраняются с объектами, в которых они созданы. Они автоматически загружаются при открытии объекта, но не применяются автоматически.

В клиентской базе данных для автоматического применения фильтра при открытии объекта задайте для свойства **Филтеронлоад** значение true.

В веб-базе данных для автоматического применения фильтра при открытии объекта добавьте действие **SetFilter** в макрос и добавьте макрос в событие OnLoad объекта. ****

## <a name="example"></a>Пример

В приведенном ниже примере показано, как использовать действие SetFilter для фильтрации формы, в которой определен макрос.

**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

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
