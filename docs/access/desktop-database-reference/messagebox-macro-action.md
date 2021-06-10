---
title: Макрокоманда MessageBox
TOCTitle: MessageBox macro action
ms:assetid: 326a0e68-38fb-4f81-b319-5a70caa5aec4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192304(v=office.15)
ms:contentKeyID: 48544077
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1175e3903e54fd3420be43dfd9e3652d9990468b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289158"
---
# <a name="messagebox-macro-action"></a>Макрокоманда MessageBox

**Область применения**: Access 2013, Office 2013

Вы можете использовать **действие MessageBox** для отображения окна сообщений, содержащего предупреждение или информационное сообщение. Например, можно использовать действие **MessageBox** с макросами проверки. Если в макросе у управления или записи не получается условие проверки, окно сообщений может отображать сообщение об ошибке и давать инструкции о том, какие данные следует в них вписать.

## <a name="setting"></a>Параметр

В **действии MessageBox** есть следующие аргументы.

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
<td><p><strong>Message</strong></p></td>
<td><p>Текст в поле сообщений. Введите текст сообщения в поле <strong>Сообщение</strong> в разделе <strong>Аргументы</strong> действий в области Macro Builder. Можно ввести до 255 символов или ввести выражение (предшествующего равному знаку).</p></td>
</tr>
<tr class="even">
<td><p><strong>Beep</strong></p></td>
<td><p>Указывает, звучит ли звуковой сигнал в динамике компьютера при показе сообщения. Щелкните <strong>Да</strong> (звук звукового сигнала) или <strong>Нет</strong> (не звучайте звуковой сигнал). По умолчанию — <strong>Да.</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>Тип</strong></p></td>
<td><p>Тип окна сообщений. Каждый тип имеет другой значок. Щелкните <strong>Нет,</strong> <strong>Критический</strong>, <strong>Предупреждение?</strong>, <strong>Предупреждение!</strong>, или <strong>сведения</strong>. По умолчанию <strong>нет</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Title</strong></p></td>
<td><p>Текст, отображаемый в панели заголовка окна сообщений. Например, в панели заголовков может &quot; отображаться проверка удостоверения &quot; клиента. Если оставить этот аргумент пустым, &quot; отображается Microsoft &quot; Access.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Вы можете использовать **действие MessageBox** для создания форматного сообщения об ошибке, аналогичного встроенным сообщениям об ошибках, отображаемой Microsoft Access. Действие **MessageBox** позволяет отправлять сообщение в трех разделах для аргумента Сообщение. Разделы разделов разделяют с помощью символа "@".

В следующем примере отображается форматированный ящик сообщений с раздельным сообщением. Первый раздел текста в сообщении отображается в виде смелого заголовка. Второй раздел отображается в виде простого текста под этим заголовком. Третий раздел отображается в виде простого текста под вторым разделом с пустой линией между ними.

Введите следующую строку в **аргументе Сообщение:**

**\!Неправильная @This кнопка не work.@Try другой.**

Вы не можете запустить действие **MessageBox** в модуле Visual Basic для приложений (VBA). Вместо этого используйте **функцию MsgBox.**

## <a name="examples"></a>Примеры

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
<td><p>IsNull([SupplierID])</p></td>
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
<td><p><strong>Имя формы</strong>: Представление списка <strong>продуктов:</strong> <strong>Имя DatasheetFilter</strong>: Where <strong>Condition</strong>: [SupplierID] = [Forms]! [Поставщики]! [SupplierID] <strong>Режим данных:</strong> <strong>Режим чтения OnlyWindow</strong>: <strong>Нормальный</strong></p></td>
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


**Проверка данных с помощью макроса**

Следующий макрос проверки проверяет почтовые коды, вступив в форму Поставщики. В нем показано использование действий **StopMacro,** **MessageBox,** **CancelEvent** и **GoToControl.** Условное выражение проверяет страну/регион и почтовый код, вписаный в запись в форме. Если почтовый код не в нужном формате для страны или региона, макрос отображает окно сообщений и отменяет сохранение записи. Затем он возвращает вас в пункт управления почтовым кодом, где можно исправить ошибку. Этот макрос должен быть присоединен к свойству **BeforeUpdate** формы Поставщики.

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
<td><p>IsNull([CountryRegion])</p></td>
<td><p><strong>StopMacro</strong></p></td>
<td><p></p></td>
<td><p>Если CountryRegion <strong>является Null,</strong>почтовый код не может быть проверен.</p></td>
</tr>
<tr class="even">
<td><p>[CountryRegion] В ( &quot; &quot; Франция, &quot; &quot; Италия, &quot; Испания &quot; ) и Len ([Почтовый индекс]) &lt; &gt; 5</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Сообщение.</strong>Почтовый код должен быть 5 символов. <strong>Звуковой сигнал</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Ошибка почтового кода</p></td>
<td><p>Если почтовый код не имеет 5 символов, отобразить сообщение.</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p><strong>CancelEvent</strong></p></td>
<td><p></p></td>
<td><p>Отмена события.</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Имя управления:</strong>PostalCode</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>[CountryRegion] В ( &quot; Австралия , Сингапур ) и &quot; &quot; &quot; Len ([Почтовый индекс]) &lt; &gt; 4</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Сообщение.</strong>Почтовый код должен быть 4 символа. <strong>Звуковой сигнал</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Ошибка почтового кода</p></td>
<td><p>Если почтовый код не 4 символа, отобразить сообщение.</p></td>
</tr>
<tr class="even">
<td><p>...</p></td>
<td><p><strong>CancelEvent</strong></p></td>
<td><p></p></td>
<td><p>Отмена события.</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Имя управления:</strong>PostalCode</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>([CountryRegion] = &quot; Канада ) и &quot; ([Почтовый индекс] Не нравится &quot; [A-Z][0-9][A-Z] [0-9][A-Z][0-9] &quot; )</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Сообщение.</strong>Почтовый код не является допустимым. Пример канадского кода: сигнал H1J 1C3 <strong></strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Ошибка почтового кода</p></td>
<td><p>Если почтовый код не является правильным для Канады, отобразить сообщение. (Пример канадского кода: H1J 1C3)</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p><strong>CancelEvent</strong></p></td>
<td><p></p></td>
<td><p>Отмена события.</p></td>
</tr>
</tbody>
</table>

