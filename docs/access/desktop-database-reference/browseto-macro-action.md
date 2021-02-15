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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296775"
---
# <a name="browseto-macro-action"></a>Макрокоманда BrowseTo

**Область применения**: Access 2013, Office 2013

Вы можете использовать действие **BrowseTo для перемещения** между объектами на месте. Вы также можете изменить исходный объект подформатного управления, указав аргумент "Путь к подформам". Use **BrowseTo** to navigate from form1 to form2 without opening up a new window.

## <a name="setting"></a>Setting

Действие **BrowseTo** имеет следующий аргумент.

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
<td><p>Object Type</p></td>
<td><p>Тип объекта, к которому необходимо получить обзор.</p></td>
</tr>
<tr class="even">
<td><p>Имя объекта</p></td>
<td><p>Объект, который загружается внутри подформатного управления, на который ссылается аргумент Path to Subform Control.</p></td>
</tr>
<tr class="odd">
<td><p>Путь к подформам управления</p></td>
<td><p>Если этот аргумент задан, путь от основной формы приложения к целевому в подчиненной форме, который загружает объект, указанный аргументом Object Name.</p></td>
</tr>
<tr class="even">
<td><p>Where Condition</p></td>
<td><p>Если этот код задан, заменяет условие Where источника записи объекта.</p></td>
</tr>
<tr class="odd">
<td><p>Page</p></td>
<td><p>Если задан, задана страница непрерывной формы, которая будет делаться текущей страницей. Этот аргумент является только веб-.</p></td>
</tr>
<tr class="even">
<td><p>Режим данных</p></td>
<td><p>Если задан, режим ввода данных формы.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Заметки

Аргумент PathToSubFormControl должен быть указан с помощью синтаксиса в следующем примере кода:

```vb
    Main Form.SubForm Ctrl 1>Form 2.SubForm Ctrl 2>Form 3.SubFormCtrl3
```

В этом примере основная форма является формой верхнего уровня в клиентского приложения Access. Аргумент Path to Sub Form Control должен поочередно указывать имена управления формы и подформы, ведущие от основной формы к подформам, который является контейнером объекта, указанного в аргументе Object Name. Каждый указанный подформатный контроль должен быть в форме, предшествующего ему. Путь должен заканчиваются подформатным управлением.

## <a name="example"></a>Пример

В следующем примере показано, как использовать действие BrowseTo для открытия отчета в подформе или в области навигации.

**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

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



