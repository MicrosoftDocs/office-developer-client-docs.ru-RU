---
title: Макрокоманда OpenForm
TOCTitle: OpenForm macro action
ms:assetid: c519a9d7-99d4-4765-ad96-59c3fe1be9e3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823095(v=office.15)
ms:contentKeyID: 48547604
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cf89b61a65c11f09d5a07e52caeee5ad416c118a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288373"
---
# <a name="openform-macro-action"></a>Макрокоманда OpenForm

**Область применения**: Access 2013, Office 2013

Действие **OpenForm** можно использовать для открытия формы в представлении формы, представлении конструктора, предварительного просмотра или таблицы. Он позволяет выбирать режим ввода данных и режим окна для формы, а также ограничивать количество записей, отображаемых в форме.

## <a name="setting"></a>Setting

Действие **OpenForm** имеет следующие аргументы.

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
<td><p><strong>Имя формы</strong></p></td>
<td><p>Имя открываемой формы. В <strong>поле "Имя</strong> формы" в разделе <strong>"Аргументы</strong> действий" области построитель макроса показаны все формы в текущей базе данных. Это обязательный аргумент. При запуске макроса, содержащего действие <strong>OpenForm</strong> в базе данных библиотеки, Microsoft Access сначала ищет форму с этим именем в базе данных библиотеки, а затем в текущей базе данных.</p></td>
</tr>
<tr class="even">
<td><p><strong>View</strong></p></td>
<td><p>Представление, в котором откроется форма. Щелкните <strong></strong> <strong>"Форма",</strong> <strong>"Конструктор",</strong>"Предварительный <strong>просмотр",</strong>"Таблица данных", <strong></strong> <strong>"Сводная диаграмма</strong> в поле <strong>"Вид".</strong> Значение по умолчанию <strong>— Form</strong>.</p><p><strong>ПРИМЕЧАНИЕ.</strong> <STRONG>Параметр аргумента View</STRONG> переопределяет параметры свойств <STRONG>DefaultView</STRONG> и <STRONG>ViewsAllowed</STRONG> формы. Например, если свойство <STRONG>ViewsAllowed</STRONG> формы имеет вид <STRONG>Datasheet,</STRONG>вы по-прежнему можете использовать действие <STRONG>OpenForm,</STRONG> чтобы открыть форму в представлении формы.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Имя фильтра</strong></p></td>
<td><p>Фильтр, ограничивающий или сортировать записи формы. Можно ввести имя существующего запроса или фильтра, сохраненного в качестве запроса. Однако запрос должен включать все поля в открываемой форме или иметь свойство <strong>OutputAllFields</strong> со свойством <strong>Yes.</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Where Condition</strong></p></td>
<td><p>Допустимый SQL WHERE (без слова WHERE) или выражение, которое Access использует для выбора записей из таблицы или запроса формы. Если выбрать фильтр с аргументом <strong>"Имя</strong> фильтра", Access применяет это предложение WHERE к результатам фильтра. Чтобы открыть форму и ограничить ее записи теми, которые указаны значением управления в другой форме, используйте следующее выражение: <strong>[</strong><em>fieldname</em><strong>] = Forms![</strong> <em>formname</em><strong>]! [</strong><em>controlname on other form</em><strong>]</strong> Replace <em>fieldname</em> with the name of a field in the underlying table or query of the form you want to open. Замените <em>имя</em> формы и имя <em>controlname</em> на другой форме и на имя другой формы и на другой форме, который содержит значение, которое должны соответствовать записи в первой форме.</p><p><strong>ПРИМЕЧАНИЕ.</strong>Максимальная длина аргумента <STRONG>Where Condition</STRONG> составляет 255 символов. Если требуется ввести более сложную SQL WHERE, используйте метод <STRONG>OpenForm</STRONG> объекта <STRONG>DoCmd</STRONG> в модуле Visual Basic для приложений (VBA). Вы можете ввести SQL в VBA с предложением WHERE до 32 768 символов.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Режим данных</strong></p></td>
<td><p>Режим ввода данных для формы. Это относится только к формам, открываемым в режиме формы или режиме таблицы. Нажмите <strong></strong> кнопку "Добавить" (пользователь может добавлять новые записи, но не может редактировать существующие), <strong></strong> изменить (пользователь может редактировать существующие записи и добавлять новые) или "Только чтение" <strong>(пользователь</strong> может просматривать только записи). Значение по умолчанию <strong>— Edit</strong>. <strong>Примечания</strong></p>
<ul>
<li><p>Параметр <strong>аргумента</strong> режима данных переопределяет параметры свойств <strong>AllowEdits,</strong> <strong>AllowDeletions,</strong> <strong>AllowAdditions</strong>и <strong>DataEntry</strong> формы. Например, если для свойства <strong>AllowEdits</strong> формы за установлено свойство <strong>No,</strong>вы по-прежнему можете использовать действие <strong>OpenForm,</strong> чтобы открыть форму в режиме редактирования.</p></li>
<li><p>Если оставить этот аргумент пустым, Access откроет форму в режиме ввода данных, заданной свойствами <strong>AllowEdits,</strong> <strong>AllowDeletions,</strong> <strong>AllowAdditions</strong>и <strong>DataEntry</strong> формы.</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>Режим окна</strong></p></td>
<td><p>Режим окна, в котором открывается форма. Click <strong>Normal</strong> (the form opens in the mode set by its properties), <strong>Hidden</strong> (the form is hidden), <strong>Icon</strong> (the form opens minimized as a small title bar at the bottom of the screen) or <strong>Dialog</strong> (the form's <strong>Modal</strong> and <strong>PopUp</strong> properties are set to <strong>Yes</strong>). Значение по умолчанию — <strong>Normal</strong>.</p><p><strong>ПРИМЕЧАНИЕ.</strong>Некоторые <STRONG>параметры</STRONG> аргументов в режиме окна не применяются при использовании документов с вкладками. Чтобы переключиться на перекрывающиеся окна:</p>
<ol>
<li><p>Щелкните вкладку "Файл" и выберите <strong>"Параметры".</strong></p></li>
<li><p>В <strong>диалоговом окне "Параметры</strong> Access" щелкните <strong>"Текущая база данных".</strong></p></li>
<li><p>В разделе <strong>"Параметры приложения"</strong>в разделе <strong>"Параметры окна документа"</strong>щелкните <strong>"Перекрывающиеся окна Windows".</strong></p></li>
<li><p>Нажмите <strong>кнопку "ОК",</strong>а затем закроем и снова откроете базу данных.</p></li>
</ol></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Заметки

Это действие аналогично двойному щелчку формы в области навигации или щелчку правой кнопкой мыши формы в области навигации и выбору представления.

Форма может быть модальной (она должна быть закрыта или скрыта перед выполнением пользователем каких-либо других действий) или без режима (пользователь может перейти в другие окна, пока форма открыта). Это также может быть всплывающее окно (форма, используемая для сбора или отображения информации, которая остается поверх всех остальных окон Access). Свойства **Modal** и **PopUp** за устанавливаются при разработке формы. Если вы используете **normal** для аргумента **режима окна,** форма открывается в режиме, заданном этими настройками свойств. Если вы используете **Диалоговое окно** для **аргумента режима окна,** для обоих этих свойств установлено **"Да".** Форма, открытая как скрытая или в виде значка, возвращается в режим, указанный в параметрах ее свойств при ее от показе или восстановлении.

Когда вы открываете форму с аргументом **"Режим** окна", установленным в **диалоговом** окне, Access приостанавливать макрос, пока форма не будет закрыта или скрыта. Можно скрыть форму, установив для ее свойства **Visible** свойство **No** с помощью действия **SetValue.**

> [!TIP]
> Можно выбрать форму в области навигации и перетащить ее в строку макроса. При этом автоматически создается действие **OpenForm,** которое открывает форму в представлении формы.

Применяемое условие фильтра и where становится параметром свойства **Filter** формы.

## <a name="examples"></a>Примеры

**Установка значения элемента управления с помощью макроса**

Следующий макрос открывает форму "Добавить товары" с помощью кнопки в форме "Поставщики". Он демонстрирует применение макрокоманд **ВыводНаЭкран**, **ЗакрытьОкно**, **ОткрытьФорму**, **ЗадатьЗначение** и **КЭлементуУправления**. Действие **SetValue** задает для управления "ИД поставщика" в форме "Продукты" текущего поставщика в форме "Поставщики". Затем **действие GoToControl** перемещает фокус на поле "ИД категории", где можно начать ввод данных для нового продукта. Этот макрос должен быть привязан к кнопке "Добавить товары" в форме "Поставщики".

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


Следующий макрос открывает форму "Список продуктов" в правом нижнем углу формы "Поставщики", отображая продукты текущего поставщика. Здесь показано использование действий **Echo,** **MessageBox,** **GoToControl,** **StopMacro,** **OpenForm** и **MoveAndSizeWindow.** Здесь также показано использование условного выражения с действиями **MessageBox,** **GoToControl** и **StopMacro.** Этот макрос следует прикрепить к кнопке "Обзор продуктов" в форме "Поставщики".

**Синхронизация форм с помощью макроса**

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
<td><p>IsNull([SupplierID])</p></td>
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
<td><p><strong>Form Name</strong>: Product List <strong>View</strong>: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [SupplierID] = [Forms]! [Поставщики]! [SupplierID] <strong>Режим данных:</strong> <strong>режим только чтенияWindow</strong>: <strong>обычный</strong></p></td>
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

