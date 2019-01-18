---
title: Макрокоманда BrowseTo
TOCTitle: BrowseTo macro action
ms:assetid: b25e1cc6-c4ed-abd6-0285-94fc7dae0bdf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822020(v=office.15)
ms:contentKeyID: 48547167
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm35083
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 0bcf0a37f8c1596856f5d7b921430371d620f7a3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711072"
---
# <a name="browseto-macro-action"></a>Макрокоманда BrowseTo

**Применимо к**: Access 2013, Office 2013

Действие **ВыбратьОбъект** можно использовать для перехода между объектами на месте. Можно также изменить исходный объект подчиненной путем указания пути к подчиненной аргумент. Используйте **ВыбратьОбъект** для перехода от form1 form2, не открывая новое окно.

## <a name="setting"></a>Setting

Действие **ВыбратьОбъект** использует следующий аргумент.

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
<td><p>Тип объекта</p></td>
<td><p>Тип объекта, к которому следует обзор.</p></td>
</tr>
<tr class="even">
<td><p>Имя объекта</p></td>
<td><p>Объект, который загружает внутри элемента управления подчиненной формы, ссылается путь, который требуется аргумент управления подчиненной формы.</p></td>
</tr>
<tr class="odd">
<td><p>Путь к элементу управления подчиненной формы</p></td>
<td><p>Если указан, то путь из основной формы приложения, подчиненная форма конечного управления, загружает объект, указанный в аргументе имя объекта.</p></td>
</tr>
<tr class="even">
<td><p>Условие отбора</p></td>
<td><p>Если указано, заменяет условие источника записей объекта.</p></td>
</tr>
<tr class="odd">
<td><p>Page</p></td>
<td><p>Если указано, задает страницу непрерывного формы, в которой будет осуществляться текущей страницы. Этот аргумент представляет веб-узла только.</p></td>
</tr>
<tr class="even">
<td><p>Режим данных</p></td>
<td><p>Если указан, режим ввода данных формы.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

Аргумент PathToSubFormControl должен быть указан с помощью синтаксиса в следующем примере кода:

```vb
    Main Form.SubForm Ctrl 1>Form 2.SubForm Ctrl 2>Form 3.SubFormCtrl3
```

В этом примере форме основной — форма верхнего уровня в клиентском приложении Access. Путь, который требуется аргумент Sub элемента управления формы можно также необходимо указать имена элементов управления формы и подчиненной формы начальные из главной формы к элементу управления подчиненной формы, который является контейнером объект, указанный в аргументе имя объекта. Все элементы управления подчиненной формы, указанного значения элемента управления на форме, которая предшествует его. Путь должен завершаться управления подчиненной формы.

## <a name="example"></a>Пример

Следующем примере показано, как использовать ВыбратьОбъект действия, чтобы открыть отчет в элементе управления подчиненной формы или в элементе управления навигации.

**Пример кода предоставлен** [Справочник программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    OnError
        Go to Next
        Macro Name
    
    /* Try to load the report in the host form (frmAuthorsParameter)    */
    BrowseTo
        Object Type Report
        Object Name rptChapters
        Path to Subform Control frmAuthorsParameter.sfrmChild
        Where Condition
        Page
        Data Mode Edit
    
    Parameters
        SelectedAuthor =[cboAuthor]
    
    /* if this fails, try to load it in the navigation subform     */
    BrowseTo
        Object Type Report
        Object Name rptChapters
        Path to Subform Control frmMain.NavigationSubform>frmAuthorsParameter.sfrmChild
        Where Condition
        Page
        Data Mode Edit
    
    Parameters
        SelectedAuthor =[cboAuthor]
```



