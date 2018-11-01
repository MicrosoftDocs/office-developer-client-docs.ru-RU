---
title: Действия макроса MessageBox
TOCTitle: MessageBox Macro Action
ms:assetid: 326a0e68-38fb-4f81-b319-5a70caa5aec4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192304(v=office.15)
ms:contentKeyID: 48544077
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6654d2994b472ff2d495b60fffd5fcdbd6e58089
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885236"
---
# <a name="messagebox-macro-action"></a>Действия макроса MessageBox


**Применимо к**: Access 2013, Office 2013




Действие **MessageBox** можно использовать для отображения окна сообщения, содержащее предупреждение или информационное сообщение. Например можно использовать действие **MessageBox** с макросами проверки. Элемент управления или запись не условие в макросе, прошедших окно сообщения можно отображать сообщение об ошибке и приведены инструкции по тип данных, который должен быть введен.

## <a name="setting"></a>Параметр

Действие **MessageBox** имеет следующие аргументы.

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
<td><p><strong>Сообщение</strong></p></td>
<td><p>Текст в окне сообщения. Введите текст сообщения в окне <strong>сообщения</strong> в разделе <strong>Действие аргументы</strong> в области построения макросов. Можно ввести до 255 знаков или введите выражение (стоять знак равенства).</p></td>
</tr>
<tr class="even">
<td><p><strong>Beep</strong></p></td>
<td><p>Указывает ли ваше звукового сигнала при выводе сообщения. Нажмите кнопку <strong>Да</strong> (звук сигнала) или <strong>Нет</strong> (не звук сигнала). По умолчанию используется значение <strong>Да</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Тип</strong></p></td>
<td><p>Тип окна сообщения. Каждый тип имеет другой значок. Нажмите кнопку <strong>Нет</strong>, <strong>важных</strong>, <strong>Предупреждение?</strong>, <strong>Предупреждение!</strong>, или <strong>сведения</strong>. Значение по умолчанию — <strong>None</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Название</strong></p></td>
<td><p>Текст, отображаемый в строке заголовка окна сообщения. Например имеется отображения панели заголовка &quot;проверка кода клиента&quot;. Если оставить этот аргумент пустым, &quot;Microsoft Access&quot; отображается.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

Действие **MessageBox** можно использовать для создания форматированное сообщение об ошибке, аналогичное встроенным сообщениям об ошибках в Microsoft Access. Действие **MessageBox** позволяет ввести сообщение из трех разделов для аргумента сообщения. Разделите разделы с «@» символов.

Следующий пример отображает окно с форматированным сообщением. В первом разделе текста в сообщении отображается как заголовок полужирным шрифтом. Во втором разделе отображается в виде обычного текста под заголовком. Третий раздел отображается в виде обычного текста под во втором разделе с пустой строки между ними.

Введите следующую строку в аргументе **сообщения** :

**Неверный кнопка\!@This кнопка не Work.@Try другую.**

Не удается выполнить действие **MessageBox** в Visual Basic для приложений (VBA) модуля. Вместо этого используйте функции **MsgBox** .

## <a name="examples"></a>Примеры

**Синхронизация форм с помощью макроса (en)**

Следующий макрос открывает форму списка продуктов в правом нижнем углу формы Поставщики, отображение текущего поставщика продуктов. Демонстрируется использование **эхо**, **MessageBox**, **КЭлементуУправления**, **ОстановитьМакрос**, **ОткрытьФорму**и **MoveAndSizeWindow** действий. Также показано использование условного выражения с **MessageBox**, **КЭлементуУправления**« **Поставщики** ». Этот макрос должен быть связан с кнопкой Обзор продуктов в форме Поставщики.

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
<th><p>Действие</p></th>
<th><p>Аргументы: параметр</p></th>
<th><p>Comment</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><strong>Эхо</strong></p></td>
<td><p><strong>Вывод на экран</strong>: <strong>Нет</strong></p></td>
<td><p>Остановите обновление экрана в процессе выполнения макроса.</p></td>
</tr>
<tr class="even">
<td><p>IsNull([SupplierID])</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Сообщение</strong>: перемещение на запись поставщика, продукты, чтобы увидеть, затем нажмите кнопку Предварительный просмотр еще раз. <strong>Звуковые сигналы</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Выбор поставщика</p></td>
<td><p>При отсутствии никто из современных поставщиков в форме Поставщики, отображается сообщение.</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Имя элемента управления</strong>: CompanyName</p></td>
<td><p>Перемещение фокуса на элемент управления CompanyName.</p></td>
</tr>
<tr class="even">
<td><p>...</p></td>
<td><p><strong>StopMacro</strong></p></td>
<td><p></p></td>
<td><p>Остановка макроса.</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>ОткрытьФорму</strong></p></td>
<td><p><strong>Имя формы</strong>: список продуктов <strong>представления</strong>: <strong>Имя DatasheetFilter</strong>: <strong>условие отбора</strong>: [код поставщика] = [Forms]! [Поставщики]! [Код поставщика] <strong>Режим данных</strong>: <strong>Режим чтения OnlyWindow</strong>: <strong>Обычный</strong></p></td>
<td><p>Откройте форму списка продуктов и отображение текущего поставщика продуктов.</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><strong>MoveAndSizeWindow</strong></p></td>
<td><p><strong>Право</strong>: 0,7799&quot; <strong>вниз</strong>: 1,8&quot;</p></td>
<td><p>Положение формы списка продуктов в нижней правой части формы Поставщики.</p></td>
</tr>
</tbody>
</table>


**Проверка данных с помощью макроса (en)**

Следующий макрос для проверки проверяет почтовые индексы, введенные в форме Поставщики. Демонстрируется использование **ОстановитьМакрос**, **MessageBox**, **ОтменитьСобытие**и **КЭлементуУправления** действия. Условным выражением проверяет страны или региона и почтового индекса в записи на форме. Если почтовый индекс не находится в нужном формате для страны или региона, макрос отображается окно сообщения и показано, как отменить сохранение записи. Оно будет снова к элементу управления PostalCode для исправления ошибки. Этот макрос должен быть связан свойством **BeforeUpdate** формы Поставщики.

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
<th><p>Действие</p></th>
<th><p>Аргументы: параметр</p></th>
<th><p>Comment</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>IsNull([CountryRegion])</p></td>
<td><p><strong>StopMacro</strong></p></td>
<td><p></p></td>
<td><p>Если Страна имеет <strong>значение Null</strong>, почтовый индекс не может быть проверен.</p></td>
</tr>
<tr class="even">
<td><p>[Страна] В (&quot;Франции&quot;,&quot;Италия&quot;,&quot;Испания&quot;) и Len([PostalCode]) &lt; &gt; 5</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Сообщение</strong>: почтовый индекс должен состоять из 5 знаков. <strong>Звуковые сигналы</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: ошибка почтовый индекс</p></td>
<td><p>Если почтовый индекс не 5 знаков, отобразите сообщение.</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p><strong>ОтменитьСобытие</strong></p></td>
<td><p></p></td>
<td><p>Отмените событие.</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Имя элемента управления</strong>: PostalCode</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>[Страна] В (&quot;Австралия&quot;,&quot;Сингапур&quot;) и Len([PostalCode]) &lt; &gt; 4</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Сообщение</strong>: почтовый индекс должен быть 4 символов. <strong>Звуковые сигналы</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: ошибка почтовый индекс</p></td>
<td><p>Если почтовый индекс не 4 символа, отобразите сообщение.</p></td>
</tr>
<tr class="even">
<td><p>...</p></td>
<td><p><strong>ОтменитьСобытие</strong></p></td>
<td><p></p></td>
<td><p>Отмените событие.</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Имя элемента управления</strong>: PostalCode</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>([Страна] = &quot;Канада&quot;) И ([PostalCode] не нравится&quot;[A-Z] [0-9] [A-Z] [0-9] [A-Z] [0-9]&quot;)</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Сообщение</strong>: почтовый индекс является недопустимым. Пример кода, английский (Канада): H1J 1 c 3 <strong>звуковые сигналы</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: почтовый код ошибки</p></td>
<td><p>Если почтовый индекс не соответствует формату для Канады, отобразите сообщение. (Пример кода, английский (Канада): H1J 1 c 3)</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p><strong>ОтменитьСобытие</strong></p></td>
<td><p></p></td>
<td><p>Отмените событие.</p></td>
</tr>
</tbody>
</table>

