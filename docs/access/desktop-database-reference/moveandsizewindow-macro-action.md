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

Если вы настроили параметры окна документов для использования перекрывающихся окон вместо вкладки документов, вы можете использовать действие **MoveAndSizeWindow** для перемещения или повторного использования активного окна. Сведения о том, как установить параметры окна документов, см. в разделе Примечание.

## <a name="setting"></a>Параметр

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
<td><p>Новое горизонтальное положение верхнего левого угла окна, измеряемого с левого края его содержащего окна. Введите позицию в <strong>правом</strong> окне в разделе <strong>Аргументы</strong> действий в области Macro Builder.</p></td>
</tr>
<tr class="even">
<td><p><strong>Down</strong></p></td>
<td><p>Новое вертикальное положение верхнего левого угла окна, измеряемого с верхнего края его содержащего окна.</p></td>
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
> Каждое измерение находится в дюймах или сантиметрах в зависимости от региональных параметров Windows панели управления.

## <a name="remarks"></a>Примечания

Чтобы настроить приложение для использования перекрывающихся окон вместо вкладки документов, используйте следующую процедуру:

1.  Щелкните **Параметры**

2.  Щелкните **текущую базу данных**.

3.  В разделе **Параметры приложений** в **разделе Параметры окна документов** нажмите **кнопку Перекрытие Windows**.

4.  Нажмите **кнопку ОК,** а затем закрыть и открыть базу данных.

Это действие аналогично нажатию **кнопки Move** или **Size** в меню **"Управление** окном". В командах меню для перемещения или повторного использования окна используются клавиши со стрелками клавиатуры. С помощью **действия MoveAndSizeWindow** вы вводите измерения положения и размера напрямую. Вы также можете использовать мышь для перемещения и размера окон.

Это действие можно использовать в любом окне, в любом представлении.

> [!TIP]
> - Чтобы переместить окно без его повторного использования, введите значения аргументов **"Право"** и "Вниз", но оставьте аргументы **Ширина** и Высота пустыми.  
> - Чтобы повторное значение окна не перемещалось, введите  значения для аргументов **Ширина** и Высота, но оставьте аргументы **Right** and **Down** пустыми.

Чтобы выполнить действие **MoveAndSizeWindow** в модуле Visual Basic для приложений (VBA), используйте метод **MoveSize** объекта **DoCmd.**

## <a name="example"></a>Пример

**Синхронизация форм с помощью макроса**

Следующий макрос открывает форму Списка продуктов в нижнем правом углу формы Поставщики, отображая продукты текущего поставщика. В нем показано использование действий **Echo,** **MessageBox,** **GoToControl,** **StopMacro,** **OpenForm** и **MoveAndSizeWindow.** В нем также показано использование условного выражения с **действиями MessageBox,** **GoToControl** и **StopMacro.** Этот макрос следует прикрепить к кнопке Review Products в форме Поставщики.

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Условие</p></th>
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
<td><p>IsNull([Поставщик ID])</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Сообщение.</strong>Перейдите к записи поставщика, продукты которого вы хотите видеть, а затем нажмите кнопку Обзор продуктов снова. <strong>Звуковой сигнал</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Выберите поставщика</p></td>
<td><p>Если в форме Поставщики нет текущего поставщика, отобразить сообщение.</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Имя управления:</strong>CompanyName</p></td>
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
<td><p><strong>Имя формы</strong>: Представление списка <strong>продуктов:</strong> <strong>Имя DatasheetFilter</strong>: Where <strong>Condition</strong>: [Supplier ID] = [Forms]! [Поставщики]! [SupplierID] <strong>Режим данных:</strong> <strong>Режим чтения OnlyWindow</strong>: <strong>Нормальный</strong></p></td>
<td><p>Откройте форму списка продуктов и покажите продукты текущего поставщика.</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><strong>MoveAndSizeWindow</strong></p></td>
<td><p><strong>Справа</strong>: 0.7799 &quot; <strong>Вниз</strong>: 1.8&quot;</p></td>
<td><p>Расположить форму списка продуктов в нижнем праве формы Поставщики.</p></td>
</tr>
</tbody>
</table>

