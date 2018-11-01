---
title: 'HelloData: простое приложение ADO'
TOCTitle: 'HelloData: A Simple ADO Application'
ms:assetid: c271abeb-8865-81f9-db8e-47d3db87ad30
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249950(v=office.15)
ms:contentKeyID: 48547554
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8828d65427eb85eecc9994b14017c4f35249ce7a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/01/2018
ms.locfileid: "25891207"
---
# <a name="hellodata-a-simple-ado-application"></a>HelloData: простое приложение ADO


**Применимо к**: Access 2013, Office 2013

Чтобы подготовиться к просмотра библиотеки ADO, рассмотрим простое приложение ADO называется «HelloData». HelloData шаги по каждой из четырех основных операций ADO (начало, проверки, изменение и обновление данных). Чтобы сосредоточиться на основ ADO и избежать лишних кода, обработка ошибок минимальной выполняется в примере.

Приложение запрашивает образце базы данных Northwind, который входит в состав Microsoft SQL Server 2000.

**Для запуска HelloData**

1.  Создание нового проекта Visual Basic стандартный исполняемый файл, который ссылается ADO 2.5 библиотеки.

2.  Создайте четыре командные кнопки в верхней части формы, установка для свойства **Name** и **Caption** значения, указанные в следующей таблице.

3.  Ниже кнопок добавьте элемент **Управления DataGrid Microsoft** (Msdatgrd.ocx). Файл Msdatgrd.ocx, поступающие с помощью Visual Basic и находится в вашей \\windows\\system32 или \\winnt\\каталог system32. Чтобы добавить элемент управления DataGrid в область элементов Visual Basic, выберите **компоненты...** в меню **проект** . Затем установите флажок рядом с элементом «элемент управления DataGrid Microsoft 6.0 (SP3) (OLEDB)» и нажмите **кнопку ОК**. Чтобы добавить элемент управления в проект, перетащите элемент управления DataGrid из панели элементов Visual Basic форму.

4.  Создание **текстового поля** на форме под сетку и задайте его свойства, как показано в таблице. Формы должен выглядеть на следующем рисунке, после завершения.

5.  И, наконец скопируйте код, приведенный в [HelloData код](hellodata-code.md) и вставьте его в окно редактора кода формы. Нажмите клавишу **F5** , чтобы запустить код.


> [!NOTE]
> <P>В следующем примере и в руководстве идентификатор пользователя «Мой_идентификатор» пароль «123aBc» используется для проверки подлинности на сервере. Необходимо заменить эти значения с действительные учетные данные для сервера. Кроме того замените «MyServer» значение с именем сервера.</P>



Подробное описание код ознакомиться с [Подробными сведениями HelloData](hellodata-details.md).

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
<td><p>DataGrid мс</p></td>
<td><p>Имя</p></td>
<td><p>grdDisplay1</p></td>
</tr>
<tr class="odd">
<td><p>Текстовое поле</p></td>
<td><p>Имя</p></td>
<td><p>txtDisplay1</p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p>Multiline</p></td>
<td><p>true</p></td>
</tr>
<tr class="odd">
<td><p>Кнопки</p></td>
<td><p>Имя</p></td>
<td><p>cmdGetData</p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p>Caption</p></td>
<td><p>Получение данных</p></td>
</tr>
<tr class="odd">
<td><p>Кнопки</p></td>
<td><p>Имя</p></td>
<td><p>cmdExamineData</p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p>Caption</p></td>
<td><p>Проверка данных</p></td>
</tr>
<tr class="odd">
<td><p>Кнопки</p></td>
<td><p>Имя</p></td>
<td><p>cmdEditData</p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p>Caption</p></td>
<td><p>Изменение данных</p></td>
</tr>
<tr class="odd">
<td><p>Кнопки</p></td>
<td><p>Имя</p></td>
<td><p>cmdUpdateData</p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p>Caption</p></td>
<td><p>Обновление данных</p></td>
</tr>
</tbody>
</table>



