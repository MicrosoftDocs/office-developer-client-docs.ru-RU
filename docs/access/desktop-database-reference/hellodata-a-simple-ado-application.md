---
title: 'HelloData: простое приложение ADO'
TOCTitle: 'HelloData: A simple ADO application'
ms:assetid: c271abeb-8865-81f9-db8e-47d3db87ad30
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249950(v=office.15)
ms:contentKeyID: 48547554
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3c7d9be9b91b3f847516eb3c22aa37e46c8a551d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292022"
---
# <a name="hellodata-a-simple-ado-application"></a>HelloData: простое приложение ADO

**Область применения**: Access 2013, Office 2013

Чтобы заложить основу для исследования библиотеки ADO, рассмотрим простое приложение ADO под названием "HelloData". HelloData проходит каждую из четырех основных операций ADO (получение, изучение, редактирование и обновление данных). Чтобы сосредоточиться на основах ADO и предотвратить захламленность кода, в примере делается минимальная обработка ошибок.

Приложение запрашивает примерную базу данных Northwind, включенную в Microsoft SQL Server 2000.

**Запуск HelloData**

1.  Создайте новый стандартный Visual Basic Project, который ссылается на библиотеку ADO 2.5.

2.  Создайте четыре кнопки команд в верхней части формы, установив свойства **Name** и **Caption** к значениям, показанным в таблице ниже.

3.  Ниже кнопок добавьте **microsoft DataGrid Control** (Msdatgrd.ocx). Файл Msdatgrd.ocx поставляется с Visual Basic и расположен в каталоге \\ windows \\ system32 или \\ winnt \\ system32. Чтобы добавить элемент управления DataGrid в Visual Basic панели инструментов, выберите **компоненты...** из **Project** меню. Затем проверьте поле рядом с "Microsoft DataGrid Control 6.0 (SP3) (OLEDB)" и нажмите **кнопку ОК**. Чтобы добавить управление в проект, перетащите управление DataGrid из панели инструментов в форму Visual Basic.

4.  Создайте **TextBox** на форме ниже сетки и задайте ее свойства, как показано в таблице. Форма должна выглядеть аналогично следующей фигуре по завершению.

5.  Наконец, скопируйте код, указанный в [Коде HelloData,](hellodata-code.md) и вклеите его в окно редактора кода формы. Нажмите **кнопку F5** для запуска кода.

> [!NOTE]
> В следующем примере и во всем руководстве для проверки подлинности на сервере используется пользовательский id "MyId" с паролем "123aBc". Эти значения следует заменить действительными учетными данными с логотипом для сервера. Кроме того, замените значение "MyServer" именем сервера.

Подробные сведения о коде см. в [материале HelloData Details.](hellodata-details.md)

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Тип элемента управления</p></th>
<th><p>Свойство</p></th>
<th><p>Значение</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Form</p></td>
<td><p>Name</p></td>
<td><p>Form1</p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p>Height</p></td>
<td><p>6500</p></td>
</tr>
<tr class="odd">
<td><p><br />
</p></td>
<td><p>Width</p></td>
<td><p>6500</p></td>
</tr>
<tr class="even">
<td><p>MS DataGrid</p></td>
<td><p>Name</p></td>
<td><p>grdDisplay1</p></td>
</tr>
<tr class="odd">
<td><p>TextBox</p></td>
<td><p>Name</p></td>
<td><p>txtDisplay1</p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p>Multiline</p></td>
<td><p>true</p></td>
</tr>
<tr class="odd">
<td><p>Кнопка Командная</p></td>
<td><p>Name</p></td>
<td><p>cmdGetData</p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p>Подпись</p></td>
<td><p>Get Data</p></td>
</tr>
<tr class="odd">
<td><p>Кнопка Командная</p></td>
<td><p>Name</p></td>
<td><p>cmdExamineData</p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p>Подпись</p></td>
<td><p>Изучение данных</p></td>
</tr>
<tr class="odd">
<td><p>Кнопка Командная</p></td>
<td><p>Name</p></td>
<td><p>cmdEditData</p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p>Подпись</p></td>
<td><p>Изменение данных</p></td>
</tr>
<tr class="odd">
<td><p>Кнопка Командная</p></td>
<td><p>Name</p></td>
<td><p>cmdUpdateData</p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p>Подпись</p></td>
<td><p>Обновление данных</p></td>
</tr>
</tbody>
</table>



