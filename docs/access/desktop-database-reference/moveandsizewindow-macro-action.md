---
title: Макрокоманда MoveAndSizeWindow
TOCTitle: MoveAndSizeWindow macro action
ms:assetid: 86bcf45f-90ce-4ca2-a7fb-efbe5347d137
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197001(v=office.15)
ms:contentKeyID: 48546090
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c1b127995a2f9a0af7da80e9df862259b570870e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288808"
---
# <a name="moveandsizewindow-macro-action"></a>Макрокоманда MoveAndSizeWindow

**Область применения**: Access 2013, Office 2013

Если параметры окна документа настроены на использование перекрывающихся окон вместо документов с вкладками, можно использовать действие **MoveAndSizeWindow** для перемещения или настройки активного окна. Сведения о том, как настроить параметры окна документа, см. в разделе "Замечания".

## <a name="setting"></a>Setting

Действие **MoveAndSizeWindow** имеет следующие аргументы.

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
<td><p><strong>Right</strong></p></td>
<td><p>Новое горизонтальное положение левого верхнего угла окна, измеряемого от левого края окна, содержащего его. Введите положение в правом <strong>поле</strong> в разделе <strong>"Аргументы действий"</strong> области построитель макроса.</p></td>
</tr>
<tr class="even">
<td><p><strong>Вниз</strong></p></td>
<td><p>Новое вертикальное положение левого верхнего угла окна, измеряемого от верхнего края окна, содержащего его.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Width</strong></p></td>
<td><p>Новая ширина окна.</p></td>
</tr>
<tr class="even">
<td><p><strong>Height</strong></p></td>
<td><p>Новая высота окна.</p></td>
</tr>
</tbody>
</table>


Если оставить аргумент пустым, Microsoft Access использует текущий параметр окна.

Необходимо ввести значение по крайней мере для одного аргумента.

> [!NOTE]
> Размер каждого измерения зависит от региональных параметров панели управления Windows в дюймах или см.

## <a name="remarks"></a>Заметки

Чтобы настроить приложение для использования перекрывающихся окон вместо документов с вкладками, используйте следующую процедуру:

1.  Параметры **щелчка**

2.  Щелкните **"Текущая база данных".**

3.  В разделе **"Параметры приложения"** в разделе **"Параметры окна документа"** щелкните **"Перекрывающиеся окна Windows".**

4.  Нажмите **кнопку "ОК",** а затем закроем и снова откроете базу данных.

Это действие аналогично нажатию кнопки **"Переместить"** или **"Размер"** в меню **"Управление" окна.** С помощью команд меню можно использовать клавиши со стрелками клавиатуры для перемещения или настройки окна. С помощью **действия MoveAndSizeWindow** вы вводите измерения положения и размера напрямую. Вы также можете использовать мышь для перемещения и размера окон.

Это действие можно использовать в любом окне, в любом представлении.

> [!TIP]
> - Чтобы переместить окно без его размеров, введите  значения для аргументов **"Право"** и "Вниз", но оставьте аргументы **Width** и **Height** пустыми.
> - Чтобы не перемещать окно, введите значения аргументов **Width** и **Height,** но оставьте аргументы **Right** и **Down** пустыми.

Чтобы запустить действие **MoveAndSizeWindow** в модуле Visual Basic для приложений (VBA), используйте метод **MoveSize** объекта **DoCmd.**

## <a name="example"></a>Пример

**Синхронизация форм с помощью макроса**

Следующий макрос открывает форму "Список продуктов" в правом нижнем углу формы "Поставщики", отображая продукты текущего поставщика. Здесь показано использование действий **Echo,** **MessageBox,** **GoToControl,** **StopMacro,** **OpenForm** и **MoveAndSizeWindow.** Здесь также показано использование условного выражения с действиями **MessageBox,** **GoToControl** и **StopMacro.** Этот макрос следует прикрепить к кнопке "Обзор продуктов" в форме "Поставщики".

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Condition</p></th>
<th><p>Макрокоманда</p></th>
<th><p>Аргументы: параметр</p></th>
<th><p>Примечание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><strong>ВыводНаЭкран</strong></p></td>
<td><p><strong>Включить вывод</strong>: <strong>Нет</strong></p></td>
<td><p>Приостанавливает обновление экрана, пока выполняется макрос.</p></td>
</tr>
<tr class="even">
<td><p>IsNull([ИД поставщика])</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Сообщение:</strong>перейдите к записи поставщика, продукты которой вы хотите просмотреть, а затем снова нажмите кнопку "Просмотреть продукты". <strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</p></td>
<td><p>Если в форме "Поставщики" нет текущего поставщика, отобразить сообщение.</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Имя управления</strong>: CompanyName</p></td>
<td><p>Переместите фокус на управление CompanyName.</p></td>
</tr>
<tr class="even">
<td><p>...</p></td>
<td><p><strong>StopMacro</strong></p></td>
<td><p></p></td>
<td><p>Остановите макрос.</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>OpenForm</strong></p></td>
<td><p><strong>Form Name</strong>: Product List <strong>View</strong>: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [Supplier ID] = [Forms]! [Поставщики]! [SupplierID] <strong>Режим данных:</strong> <strong>режим только чтенияWindow</strong>: <strong>обычный</strong></p></td>
<td><p>Откройте форму "Список продуктов" и откажите продукты текущего поставщика.</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><strong>MoveAndSizeWindow</strong></p></td>
<td><p><strong>Right</strong>: 0.7799 &quot; <strong>Down</strong>: 1.8&quot;</p></td>
<td><p>Расположить форму "Список продуктов" в правом нижнем правом месте формы "Поставщики".</p></td>
</tr>
</tbody>
</table>

