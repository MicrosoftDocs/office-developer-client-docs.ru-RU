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

Чтобы создать основу для исследования библиотеки ADO, рассмотрим простое приложение ADO под названием "HelloData". HelloData пошаговые инструкции по каждой из четырех основных операций ADO (знакомство, просмотр, редактирование и обновление данных). Чтобы сосредоточиться на основных понятиях ADO и предотвратить несрочный код, в этом примере выполняется минимальная обработка ошибок.

Приложение запрашивает учебную базу данных Northwind, которая входит в состав Microsoft SQL Server 2000.

**Запуск HelloData**

1.  Создайте новый стандартный исполняемый проект Visual Basic, который ссылается на библиотеку ADO 2,5.

2.  Создайте четыре кнопки в верхней части формы, задав для свойств **Name** и **Caption** значения, указанные в приведенной ниже таблице.

3.  Под кнопками добавьте **элемент управления Microsoft DataGrid** (мсдатгрд. ocx). Файл Мсдатгрд. ocx поставляется с Visual Basic и находится в \\каталоге Windows\\System32 или \\WinNT\\System32. Чтобы добавить элемент управления DataGrid на панель элементов Visual Basic, выберите **компоненты...** в меню **проект** . Затем установите флажок "элемент управления Microsoft DataGrid 6,0 (с пакетом обновления 3) (OLEDB)" и нажмите кнопку **ОК**. Чтобы добавить элемент управления в проект, перетащите элемент управления DataGrid из панели элементов в форму Visual Basic.

4.  Создайте **текстовое поле** в форме под сеткой и задайте его свойства, как показано в таблице. По завершении форма должна выглядеть примерно так, как показано на следующем рисунке.

5.  Наконец, скопируйте код, приведенный в [HelloData Code](hellodata-code.md) , и вставьте его в окно редактора кода формы. Нажмите клавишу **F5** , чтобы запустить код.

> [!NOTE]
> В приведенном ниже примере и в рамках руководства для проверки подлинности на сервере используется идентификатор пользователя "MyId" с паролем "123aBc". Необходимо заменить эти значения действительными учетными данными для входа на сервер. Кроме того, замените "MyServer" на имя вашего сервера.

Подробное описание кода приведено в разделе [HelloData Details](hellodata-details.md).

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
<td><p>Форма</p></td>
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
<td><p>Скидок</p></td>
<td><p>true</p></td>
</tr>
<tr class="odd">
<td><p>Кнопка</p></td>
<td><p>Имя</p></td>
<td><p>кмджетдата</p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p>Подпись</p></td>
<td><p>Получение данных</p></td>
</tr>
<tr class="odd">
<td><p>Кнопка</p></td>
<td><p>Имя</p></td>
<td><p>кмдексаминедата</p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p>Подпись</p></td>
<td><p>Анализ данных</p></td>
</tr>
<tr class="odd">
<td><p>Кнопка</p></td>
<td><p>Имя</p></td>
<td><p>кмдедитдата</p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p>Подпись</p></td>
<td><p>Изменение данных</p></td>
</tr>
<tr class="odd">
<td><p>Кнопка</p></td>
<td><p>Имя</p></td>
<td><p>кмдупдатедата</p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p>Подпись</p></td>
<td><p>Обновление данных</p></td>
</tr>
</tbody>
</table>



