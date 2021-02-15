---
title: Макро макрос Echo (справочник по базе данных Access для настольных пк)
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

Вы можете использовать действие **Echo,** чтобы указать, включено ли эхо. Например, это действие можно использовать для скрытие или показа результатов макроса во время его работы.

## <a name="setting"></a>Setting

> [!NOTE]
> Эта макрокоманда доступна только для доверенных баз данных.

Действие **Echo** имеет следующие аргументы.

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
<td><p><strong>Эхо в ветвях</strong></p></td>
<td><p>Нажмите <strong>кнопку "Да"</strong> (включить эхо) или <strong>"Нет"</strong> <strong></strong> (отключить эхо) в поле <strong>"Эхо в</strong> действии" в разделе "Аргументы действий" области построитель макроса. Значение по умолчанию <strong>— Да.</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Текст в панели состояния</strong></p></td>
<td><p>Текст, который будет отображаться в панели состояния, когда эхо отключено. Например, если эхо отключено, в панели состояния может отображаться &quot; запущенный макрос.&quot;</p></td>
</tr>
</tbody>
</table>


При запуске макроса при обновлении экрана часто показываются сведения, не важные для работы макроса. Если для аргумента **Echo On** установлено **"Нет",** макрос выполняется без обновления экрана. После завершения макроса Access автоматически включает эхо и повторно обновляет окно. Параметр **"Нет"** для аргумента **Echo On** не влияет на функциональность макроса и его результаты.

Действие **Echo** не подавляет отображение модальных диалоговых окной, таких как сообщения об ошибках или всплывающие формы, такие как листы свойств. Для сбора или отображения информации можно использовать диалоговое окно и всплывающие формы, даже если эхо отключено. Чтобы подавлять все сообщения или диалоги, кроме полей сообщений об ошибках и диалогов, которые требуют ввода информации пользователем, используйте действие **SetWarnings.**

Макрос может **запускать макрос** несколько раз. Это позволяет изменять текст в панели состояния во время макроса.

Если вы отключите эхо, вы можете использовать действие **DisplayHourglassPointer,** чтобы изменить указатель мыши на значок песочных часов (или любой значок указателя мыши, заданный для "Занят"), чтобы показать, что макрос запущен.

Чтобы запустить действие **Echo** в модуле Visual Basic для приложений (VBA), используйте метод **Echo** объекта **DoCmd.**

## <a name="examples"></a>Примеры

### <a name="set-the-value-of-a-control-by-using-a-macro"></a>Установка значения элемента управления с помощью макроса

Следующий макрос открывает форму "Добавить товары" с помощью кнопки в форме "Поставщики". Он демонстрирует применение макрокоманд **ВыводНаЭкран**, **ЗакрытьОкно**, **ОткрытьФорму**, **ЗадатьЗначение** и **КЭлементуУправления**. Действие **SetValue** задает для контроля "ИД поставщика" в форме "Продукты" текущего поставщика в форме "Поставщики". Затем **действие GoToControl** перемещает фокус на поле "ИД категории", где можно начать ввод данных для нового продукта. Этот макрос должен быть привязан к кнопке "Добавить товары" в форме "Поставщики".

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
<td><p>Установите для управления "ИД поставщика" текущего поставщика в форме "Поставщики".</p></td>
</tr>
<tr class="odd">
<td><p><strong>КЭлементуУправления</strong></p></td>
<td><p><strong>Имя элемента управления</strong>: КодКатегории</p></td>
<td><p>Перейдите к окни управления "ИД категории".</p></td>
</tr>
</tbody>
</table>


### <a name="synchronize-forms-by-using-a-macro"></a>Синхронизация форм с помощью макроса

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
<td><p>...</p></td>
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

