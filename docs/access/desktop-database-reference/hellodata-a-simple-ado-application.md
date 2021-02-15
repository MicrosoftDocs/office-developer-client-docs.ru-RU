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

Чтобы заложить основу для изучения библиотеки ADO, рассмотрите простое приложение ADO под названием "HelloData". HelloData по шагам в каждой из четырех основных операций ADO (получение, изучение, редактирование и обновление данных). Чтобы сосредоточиться на основах ADO и предотвратить помехи в коде, в примере делается минимальная обработка ошибок.

Приложение запрашивает пример базы данных Northwind, включаемую в Microsoft SQL Server 2000.

**Запуск HelloData**

1.  Создайте новый стандартный исполняемый Visual Basic Project, который ссылается на библиотеку ADO 2.5.

2.  Создайте четыре кнопки команд в верхней части формы, установив для свойств **Name** и **Caption** значения, показанные в таблице ниже.

3.  Под кнопками добавьте microsoft **DataGrid Control** (Msdatgrd.ocx). Файл Msdatgrd.ocx поставляется с Visual Basic и находится в каталоге \\ Windows \\ system32 или \\ winnt \\ system32. Чтобы добавить элемент управления DataGrid в Visual Basic панели элементов, выберите "Компоненты"... в меню **"Проект".**  Затем пойдите в поле "Microsoft DataGrid Control 6.0 (SP3) (OLEDB)" и нажмите кнопку **"ОК".** Чтобы добавить этот контроль в проект, перетащите его с панели инструментов на Visual Basic формы.

4.  Создайте **TextBox** на форме под сеткой и задайте его свойства, как показано в таблице. По завершению форма должна выглядеть примерно так, как на следующем рисунке.

5.  Наконец, скопируйте код, указанный в [коде HelloData,](hellodata-code.md) и в paste его в окне редактора кода формы. Нажмите **F5,** чтобы запустить код.

> [!NOTE]
> В следующем примере и во всем руководстве для проверки подлинности на сервере используется код MyId с паролем "123aBc". Эти значения следует заменить действительными учетными данными для входа на сервер. Кроме того, замените значение MyServer именем сервера.

Подробное описание кода см. в описании [HelloData Details.](hellodata-details.md)

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
<td><p>Имя</p></td>
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
<td><p>Имя</p></td>
<td><p>grdDisplay1</p></td>
</tr>
<tr class="odd">
<td><p>TextBox</p></td>
<td><p>Имя</p></td>
<td><p>txtDisplay1</p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p>Многолинейная</p></td>
<td><p>true</p></td>
</tr>
<tr class="odd">
<td><p>Кнопка команды</p></td>
<td><p>Имя</p></td>
<td><p>cmdGetData</p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p>Подпись</p></td>
<td><p>Получить данные</p></td>
</tr>
<tr class="odd">
<td><p>Кнопка команды</p></td>
<td><p>Имя</p></td>
<td><p>cmdExamineData</p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p>Подпись</p></td>
<td><p>Изучение данных</p></td>
</tr>
<tr class="odd">
<td><p>Кнопка команды</p></td>
<td><p>Имя</p></td>
<td><p>cmdEditData</p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p>Подпись</p></td>
<td><p>Изменение данных</p></td>
</tr>
<tr class="odd">
<td><p>Кнопка команды</p></td>
<td><p>Имя</p></td>
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



