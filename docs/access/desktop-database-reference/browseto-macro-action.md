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

Вы можете использовать действие **бровсето** для перехода между объектами на месте. Кроме того, можно изменить исходный объект элемента управления подчиненной формы, указав аргумент путь к элементу управления подчиненной формы. С помощью **бровсето** можно переходить с Form1 на Form2, не открывая новое окно.

## <a name="setting"></a>Параметр

Действие **бровсето** имеет следующий аргумент.

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
<td><p>Тип объекта, в котором необходимо выполнить обзор.</p></td>
</tr>
<tr class="even">
<td><p>Имя объекта</p></td>
<td><p>Объект, который загружается в элемент управления подчиненной формы, на который ссылается аргумент элемента управления "путь к подчиненной форме".</p></td>
</tr>
<tr class="odd">
<td><p>Путь к элементу управления подчиненной формы</p></td>
<td><p>Если этот параметр указан, то путь из основной формы приложения к целевому элементу управления подчиненной формы, который загружает объект, заданный аргументом "имя объекта".</p></td>
</tr>
<tr class="even">
<td><p>Условие отбора</p></td>
<td><p>Если этот параметр указан, заменяется условие WHERE источника записей объекта.</p></td>
</tr>
<tr class="odd">
<td><p>Page</p></td>
<td><p>Если этот параметр указан, задает страницу ленточной формы, которая будет сделана на текущей странице. Этот аргумент относится только к веб-сайтам.</p></td>
</tr>
<tr class="even">
<td><p>Режим данных</p></td>
<td><p>Если этот параметр указан, то режим ввода данных в форме.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Аргумент Пастосубформконтрол должен быть указан с помощью синтаксиса в следующем примере кода:

```vb
    Main Form.SubForm Ctrl 1>Form 2.SubForm Ctrl 2>Form 3.SubFormCtrl3
```

В этом примере Главная форма является формой верхнего уровня в клиентском приложении Access. Аргумент элемента управления "путь к подчиненной форме" должен указывать имена элементов управления формы и подчиненной формы, ведущие от главной формы к элементу управления подчиненной формы, который является контейнером объекта, указанного аргументом "имя объекта". Каждый указанный элемент управления подчиненной формы должен быть элементом управления в форме, предшествующей ему. Путь должен заканчиваться элементом управления подчиненной формы.

## <a name="example"></a>Пример

В приведенном ниже примере показано, как использовать действие Бровсето для открытия отчета в элементе управления подчиненной формы или в элементе управления навигацией.

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



