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

С помощью действия **MessageBox** можно отобразить окно сообщения, содержащее предупреждение или информационное сообщение. Например, вы можете использовать действие **MessageBox** с макросами проверки. Если в макросе не удается найти условие проверки для какого-либо из них, в окне сообщения может отображаться сообщение об ошибке и указаны инструкции по типу данных, которые необходимо в введены.

## <a name="setting"></a>Setting

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
<td><p><strong>Message</strong></p></td>
<td><p>Текст в окне сообщения. Введите текст сообщения в поле <strong>"Сообщение"</strong> в разделе <strong>"Аргументы действий"</strong> области построитель макроса. Можно ввести до 255 символов или ввести выражение (предшествует знаку "равно").</p></td>
</tr>
<tr class="even">
<td><p><strong>Beep</strong></p></td>
<td><p>Указывает, звучит ли звуковой сигнал динамика компьютера при отображе сообщения. Нажмите <strong>кнопку "Да"</strong> (звук звукового сигнала) или <strong>"Нет"</strong> (не звучайте звуковой сигнал). Значение по умолчанию <strong>— Да.</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>Тип</strong></p></td>
<td><p>Тип окна сообщения. Каждый тип имеет разные значки. Щелкните <strong>"Нет",</strong> <strong>"Критическое",</strong> <strong>"Предупреждение?",</strong> <strong>"Предупреждение!"</strong>или <strong>"Сведения".</strong> Значение по умолчанию <strong>— None</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Title</strong></p></td>
<td><p>Текст, отображаемой в заголовке окна сообщения. Например, в заголовке заголовка может &quot; отображаться проверка кодов &quot; клиентов. Если оставить этот аргумент пустым, &quot; будет отображаться Microsoft &quot; Access.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Заметки

С помощью действия **MessageBox** можно создать отформатированные сообщения об ошибке, аналогичные встроенным сообщениям об ошибках, отображаемой Microsoft Access. Действие **MessageBox** позволяет предоставить сообщение в трех разделах для аргумента Message. Разделы разделов разделяют символами "@".

В следующем примере отображается отформатированные сообщения с раздельным сообщением. Первый раздел текста в сообщении отображается полужирным шрифтом. Второй раздел отображается в виде обычного текста под этим заголовком. Третий раздел отображается в виде обычного текста под вторым разделом с пустой строкой между ними.

Введите в **аргументе Message** следующую строку:

**\!Неправильная @This кнопка не work.@Try другой.**

Действие **MessageBox** нельзя запустить в модуле Visual Basic для приложений (VBA). Вместо этого **используйте функцию MsgBox.**

## <a name="examples"></a>Примеры

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


**Проверка данных с помощью макроса**

Следующий макрос проверки проверяет почтовые коды, вступив в форму "Поставщики". Здесь показано использование действий **StopMacro,** **MessageBox,** **CancelEvent** и **GoToControl.** Условное выражение проверяет страну или регион и почтовый код, внося в запись в форме. Если почтовый код не имеет правильного формата для страны или региона, макрос отображает окно сообщения и отменяет сохранение записи. Затем он возвращает вас в пункт управления PostalCode, где можно исправить ошибку. Этот макрос следует присоединить к свойству **BeforeUpdate** формы "Поставщики".

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
<td><p>Если countryRegion <strong>имеет null,</strong>почтовый код не может быть проверен.</p></td>
</tr>
<tr class="even">
<td><p>[CountryRegion] In &quot; &quot; (Франция, &quot; &quot; Италия, &quot; &quot; Испания) и Len([PostalCode]) &lt; &gt; 5</p></td>
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
<td><p>[CountryRegion] In &quot; &quot; (Australia, &quot; &quot; Singapore) and Len([PostalCode]) &lt; &gt; 4</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Сообщение:</strong>почтовый индекс должен иметь 4 символа. <strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</p></td>
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
<td><p>([CountryRegion] = &quot; Канада) и &quot; ([PostalCode] не нравится &quot; [A-Z][0-9][A-Z] [0-9][A-Z][0-9] &quot; )</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Сообщение:</strong>почтовый индекс не является допустимым. Пример кода для Канады: H1J 1C3 <strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</p></td>
<td><p>Если почтовый индекс неправиа для Канады, отобразить сообщение. (Пример кода для Канады: H1J 1C3)</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p><strong>CancelEvent</strong></p></td>
<td><p></p></td>
<td><p>Отмените событие.</p></td>
</tr>
</tbody>
</table>

