---
title: Макрокоманда GoToControl
TOCTitle: GoToControl macro action
ms:assetid: caff76dc-7ca8-4f87-8144-89445ed4600d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834370(v=office.15)
ms:contentKeyID: 48547705
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c056f2b0922402ea7cde7cf767969b73f912f572
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292169"
---
# <a name="gotocontrol-macro-action"></a>Макрокоманда GoToControl

**Область применения**: Access 2013, Office 2013

Вы можете использовать действие **GoToControl,** чтобы переместить фокус на указанное поле или управление в текущей записи открытой формы, таблицы данных форм, таблицы данных или таблицы запросов. Эта макрокоманда позволяет переместить фокус на определенное поле или на другой элемент управления. Затем это поле или управление можно использовать для сравнения или действий **FindRecord.** Кроме того, можно использовать эту макрокоманду для навигации в форме в соответствии с определенными условиями. Например, если пользователь введет "Нет" в элементе управления "Брак" формы медицинского страхования, фокус может сразу автоматически переместиться на элемент управления, следующий за элементом управления "Имя партнера".

## <a name="setting"></a>Setting

> [!NOTE]
> Это действие не доступно для использования со страницами доступа к данным.

Макрокоманда **GoToControl** имеет указанный ниже аргумент.

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
<td><p><strong>Имя элемента управления</strong></p></td>
<td><p>Имя поля или элемента управления, куда необходимо переместить фокус. Введите имя поля или управления в поле <strong>"Имя</strong> управления" в разделе <strong>"Аргументы</strong> действий" области построитель макроса. Это обязательный аргумент.</p>
<p><strong>ПРИМЕЧАНИЕ.</strong>Введите только имя поля или управления в <strong>аргументе "Имя</strong> управления", а не полный идентификатор, например Forms! Продукты! [ИД продукта].</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Заметки

Действие **GoToControl** нельзя использовать для перемещения фокуса на управление скрытой формой.

> [!TIP]
> Вы можете использовать **действие GoToControl** для перемещения в подформу, которая является типом управления. Затем можно использовать действие **GoToRecord** для перемещения к определенной записи в подформе. Вы также можете перейти к подформе в подформе с помощью действия **GoToControl,** чтобы перейти сначала в подформу, а затем в подформу.

Чтобы запустить действие **GoToControl** в модуле Visual Basic для приложений (VBA), используйте метод **GoToControl** объекта **DoCmd.** Вы также можете использовать метод **SetFocus,** чтобы переместить фокус на управление в форме или любой из ее подформ, а также на поле в открытой таблице, запросе или таблице данных формы.

## <a name="examples"></a>Примеры

**Установка значения элемента управления с помощью макроса**

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
<td><p>Закроем форму "Список продуктов".</p></td>
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


**Проверка данных с помощью макроса**

Следующий макрос проверки проверяет почтовые коды, вступив в форму "Поставщики". Здесь показано использование действий **StopMacro,** **MessageBox,** **CancelEvent** и **GoToControl.** Условное выражение проверяет страну или регион и почтовый код, внося в запись в форме. Если почтовый код не имеет нужного формата для страны или региона, макрос отображает окно сообщения и отменяет сохранение записи. Затем макрос возвращает вас в почтовый индекс, где можно исправить ошибку. Этот макрос следует присоединить к свойству **BeforeUpdate** формы "Поставщики".

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
<td><p>IsNull([CountryRegion])</p></td>
<td><p><strong>StopMacro</strong></p></td>
<td><p></p></td>
<td><p>Если countryRegion имеет <strong>null,</strong>почтовый код не может быть проверен.</p></td>
</tr>
<tr class="even">
<td><p>[CountryRegion] In &quot; &quot; (Франция, &quot; &quot; Италия, &quot; &quot; Испания) и Len([Почтовый индекс]) &lt; &gt; 5</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Сообщение:</strong>почтовый индекс должен иметь 5 символов. <strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</p></td>
<td><p>Если почтовый индекс не имеет 5 символов, отобразить сообщение.</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p><strong>CancelEvent</strong></p></td>
<td><p></p></td>
<td><p>Отмените событие.</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Имя управления</strong>: PostalCode</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>[CountryRegion] In &quot; &quot; (Australia, &quot; &quot; Singapore) and Len([Postal Code]) &lt; &gt; 4</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p>Сообщение: почтовый индекс должен иметь 4 символа. <strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</p></td>
<td><p>Если почтовый индекс не имеет 4 символов, отобразить сообщение.</p></td>
</tr>
<tr class="even">
<td><p>...</p></td>
<td><p><strong>CancelEvent</strong></p></td>
<td><p></p></td>
<td><p>Отмените событие.</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Имя управления</strong>: PostalCode</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>([CountryRegion] = &quot; Канада) и ([Почтовый код] не нравится &quot; &quot; [A-Z][0-9][A-Z] [0-9][A-Z][0-9] &quot; )</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Сообщение:</strong>почтовый индекс не является допустимым. Пример кода для Канады: H1J 1C3 <strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</p></td>
<td><p>Если почтовый индекс некорректно для Канады, отобразить сообщение. (Пример кода для Канады: H1J 1C3)</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p><strong>CancelEvent</strong></p></td>
<td><p></p></td>
<td><p>Отмените событие.</p></td>
</tr>
</tbody>
</table>

