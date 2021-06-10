---
title: Действие макроса Echo (Ссылка на настольные базы данных)
TOCTitle: Echo macro action
ms:assetid: 38dfb2cf-8db5-44b3-91fa-e490932b940b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192516(v=office.15)
ms:contentKeyID: 48544227
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7d536ed47c780b7f9f1675a9879e86aeff80b67f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293625"
---
# <a name="echo-macro-action"></a>Макрокоманда Echo

**Область применения**: Access 2013, Office 2013

Вы можете использовать действие **Echo,** чтобы указать, включено ли эхо. Например, это действие можно использовать для сокрытия или демонстрации результатов макроса во время его работы.

## <a name="setting"></a>Параметр

> [!NOTE]
> Эта макрокоманда доступна только для доверенных баз данных.

Действие **Echo** приводит следующие аргументы.

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
<td><p><strong>Echo On</strong></p></td>
<td><p>Щелкните <strong>Да</strong> (включите эхо) или <strong>Нет</strong> (отключите <strong></strong> эхо) в поле <strong>Эхо</strong> на поле в разделе Аргументы действий области Macro Builder. По умолчанию — <strong>Да.</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Текст панели состояния</strong></p></td>
<td><p>Текст, отображаемый в панели состояния при выключении эхо. Например, когда эхо отключено, в панели состояния может &quot; отображаться запущен макрос.&quot;</p></td>
</tr>
</tbody>
</table>


При запуске макроса обновление экрана часто показывает сведения, не важные для функционирования макроса. При наборе **аргумента Эхо на** **нет** макрос выполняется без обновления экрана. Когда макрос завершится, Access автоматически включает эхо и переклинирует окно. Параметр **No** для **аргумента Echo On** не влияет на функциональность макроса или его результаты.

Действие **Echo** не подавляет отображение модальных диалоговых ящиков, таких как сообщения об ошибках или всплывающие формы, такие как листы свойств. Вы можете использовать диалоговое окно и всплывающие формы для сбора или отображения информации, даже если отключается эхо. Чтобы подавлять все ящики сообщений или диалогов, за исключением ящиков сообщений об ошибках и диалогов, которые требуют ввода сведений пользователем, используйте **действие SetWarnings.**

Вы можете выполнить действие **Echo** несколько раз в макрос. Это позволяет изменять текст панели состояния при запуске макроса.

Если вы отключите эхо, вы можете использовать действие **DisplayHourglassPointer,** чтобы изменить указатель мыши на значок песочных часов (или любой значок указателя мыши, заданный для "Busy"), чтобы предоставить визуальное указание на то, что макрос запущен.

Чтобы выполнить действие **Echo** в Visual Basic для приложений (VBA), используйте метод **Echo** объекта **DoCmd.**

## <a name="examples"></a>Примеры

### <a name="set-the-value-of-a-control-by-using-a-macro"></a>Установка значения элемента управления с помощью макроса

Следующий макрос открывает форму "Добавить товары" с помощью кнопки в форме "Поставщики". Он демонстрирует применение макрокоманд **ВыводНаЭкран**, **ЗакрытьОкно**, **ОткрытьФорму**, **ЗадатьЗначение** и **КЭлементуУправления**. Действие **SetValue задает** контроль поставщика в форме Продуктов текущему поставщику в форме Поставщики. Затем **действие GoToControl** перемещает фокус в поле Category ID, где можно начать ввод данных для нового продукта. Этот макрос должен быть привязан к кнопке "Добавить товары" в форме "Поставщики".

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Макрокоманда</p></th>
<th><p>Аргументы: параметр</p></th>
<th><p>Примечание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>ВыводНаЭкран</strong></p></td>
<td><p><strong>Включить вывод</strong>: <strong>Нет</strong></p></td>
<td><p>Приостанавливает обновление экрана, пока выполняется макрос.</p></td>
</tr>
<tr class="even">
<td><p><strong>ЗакрытьОкно</strong></p></td>
<td><p><strong>Тип объекта</strong>: <strong>FormObject Имя</strong>: Список товаров <strong>Сохранить</strong>: <strong>Нет</strong></p></td>
<td><p>Закрывает форму "Список товаров".</p></td>
</tr>
<tr class="odd">
<td><p><strong>ОткрытьФорму</strong></p></td>
<td><p><strong>Имя формы</strong>: Товары <strong>Представление</strong>: <strong>FormData Режим</strong>: <strong>AddWindow Режим</strong>: <strong>Обычный</strong></p></td>
<td><p>Открывает форму "Товары".</p></td>
</tr>
<tr class="even">
<td><p><strong>ЗадатьЗначение</strong></p></td>
<td><p><strong>Элемент</strong>: [Forms]![Товары]![КодПоставщика] <strong>Выражение</strong>: КодПоставщика</p></td>
<td><p>Установите контроль поставщика для текущего поставщика в форме Поставщики.</p></td>
</tr>
<tr class="odd">
<td><p><strong>КЭлементуУправления</strong></p></td>
<td><p><strong>Имя элемента управления</strong>: КодКатегории</p></td>
<td><p>Перейдите к контролю category ID.</p></td>
</tr>
</tbody>
</table>


### <a name="synchronize-forms-by-using-a-macro"></a>Синхронизация форм с помощью макроса

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
<td><p>...</p></td>
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

