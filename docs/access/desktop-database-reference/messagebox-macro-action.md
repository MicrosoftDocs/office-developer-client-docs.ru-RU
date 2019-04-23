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

С помощью макрокоманды **MessageBox** можно отобразить окно сообщения с предупреждением или информационным сообщением. Например, вы можете использовать действие **MessageBox** с макросами проверки. Когда элемент управления или запись не проходит условие проверки в макросе, в окне сообщения отображается сообщение об ошибке и предоставляются инструкции о типе вводимых данных.

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
<td><p><strong>Message</strong></p></td>
<td><p>Текст в окне сообщения. Введите текст сообщения в поле <strong>сообщение</strong> в разделе <strong>аргументы макрокоманды</strong> в панели построителя макросов. Можно ввести до 255 символов или ввести выражение (перед ним должен стоять знак равенства).</p></td>
</tr>
<tr class="even">
<td><p><strong>Beep</strong></p></td>
<td><p>Указывает, будет ли динамик компьютера звуковым сигналом при отображении сообщения. Нажмите кнопку <strong>Да</strong> (звук гудка гудка) или <strong>нет</strong> (не выдавать звуковой сигнал гудка). Значение по умолчанию — <strong>Yes</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Type</strong></p></td>
<td><p>Тип окна сообщения. Каждый тип имеет свой значок. Выберите <strong>None (нет</strong>), <strong>Critical</strong>( <strong>предупреждение</strong>), Warning ( <strong>предупреждение</strong>)) или <strong>Information (сведения</strong>). Значение по умолчанию — <strong>None</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Title</strong></p></td>
<td><p>Текст, отображаемый в строке заголовка окна сообщения. Например, можно отобразить &quot;для строки заголовка проверку&quot;кода клиента. Если оставить этот аргумент пустым, &quot;будет выведено&quot; приложение Microsoft Access.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

С помощью макрокоманды **MessageBox** можно создавать отформатированные сообщения об ошибках, аналогичные встроенным сообщениям об ошибках, отображаемЫм в Microsoft Access. Действие **MessageBox** позволяет указать сообщение в трех разделах для аргумента Message. Вы разделяете разделы символом "@".

В следующем примере отображается форматированное окно с сообщением с поразделным сообщением. Первый раздел текста сообщения отображается в виде полужирного начертания. Второй раздел отображается в виде обычного текста под заголовком. Третий раздел отображается как обычный текст под вторым разделом с пустой строкой между ними.

Введите в аргументе **Message** следующую строку:

**НеПравильное Нажатие\!кнопки @This кнопка не работает. @Try другой.**

Действие **MessageBox** невозможно выполнить в модуле Visual Basic для приложений (VBA). Вместо этого используйте функцию **MsgBox** .

## <a name="examples"></a>Примеры

**Синхронизация форм с помощью макроса**

Следующий макрос открывает форму списка товаров в правом нижнем углу формы поставщики, в которой отображаются продукты текущего поставщика. В нем показано использование действий **echo**, **MessageBox**, **КЭлементуУправления**, **Макрокоманда StopMacro**, **OpenForm**и **мовеандсизевиндов** . В нем также показано использование условного выражения с действиями **MessageBox**, **КЭлементуУправления**и **Макрокоманда StopMacro** . Этот макрос необходимо прикрепить к кнопке "проверить продукты" в форме "поставщики".

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
<th><p>Действие</p></th>
<th><p>Аргументы: Настройка</p></th>
<th><p>Комментарий</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><strong>Echo</strong></p></td>
<td><p><strong>Echo on</strong>: <strong>нет</strong></p></td>
<td><p>Остановить обновление экрана во время выполнения макроса.</p></td>
</tr>
<tr class="even">
<td><p>IsNull ([КодПоставщика])</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Сообщение</strong>: перейдите к записи поставщика, продукты которой вы хотите просмотреть, а затем снова нажмите кнопку Просмотр продуктов. <strong>Beep</strong>: <strong>естипе</strong>: <strong>нонетитле</strong>: выберите поставщика</p></td>
<td><p>Если в форме Поставщики нет текущего поставщика, отобразите сообщение.</p></td>
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
<td><p><strong>OpenForm</strong></p></td>
<td><p><strong>Имя формы</strong>: <strong>представление</strong>списка продуктов: <strong>даташитфилтер Name</strong>: <strong>WHERE Condition</strong>: [КодПоставщика] = [Forms]! [Поставщики]! Ключев <strong>Режим данных</strong>: <strong>режим чтения онливиндов</strong>: <strong>обычный</strong></p></td>
<td><p>Откройте форму Список продуктов и отобразите текущие продукты поставщика.</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><strong>Мовеандсизевиндов</strong></p></td>
<td><p><strong>Right</strong>: 0,7799&quot; <strong>вниз</strong>: 1,8&quot;</p></td>
<td><p>РасПоложите форму списка товаров в правом нижнем углу формы Поставщики.</p></td>
</tr>
</tbody>
</table>


**Проверка данных с помощью макроса**

Следующий макрос проверки проверяет почтовые индексы, введенные в форме Поставщики. В нем показано использование действий **Макрокоманда StopMacro**, **MessageBox**, **Макрокоманда CancelEvent**и **КЭлементуУправления** . Условное выражение проверяет страну, регион и почтовый индекс, введенные в записи в форме. Если почтовый индекс находится в неправильном формате для страны или региона, макрос выводит окно сообщения и отменяет сохранение записи. Затем выполняется возврат к элементу управления PostalCode, в котором можно исправить ошибку. Этот макрос необходимо вложить в свойство **BeforeUpdate** формы "поставщики".

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
<th><p>Действие</p></th>
<th><p>Аргументы: Настройка</p></th>
<th><p>Комментарий</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>IsNull ([страна])</p></td>
<td><p><strong>StopMacro</strong></p></td>
<td><p></p></td>
<td><p>Если параметру страна не присвоено <strong>значение NULL</strong>, почтовый индекс не может быть проверен.</p></td>
</tr>
<tr class="even">
<td><p>Ватикан В (&quot;Франция&quot;,&quot;Италия&quot;,&quot;Испания&quot;) и len ([PostalCode]) &lt; &gt; 5</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Сообщение</strong>: длина почтового индекса не должна превышать 5 символов. <strong>Гудок</strong>: <strong>естипе</strong>: <strong>Информатионтитле</strong>: ошибка почтового кода</p></td>
<td><p>Если почтовый индекс не имеет 5 символов, отобразится сообщение.</p></td>
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
<td><p><strong>Имя элемента управления</strong>: PostalCode</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Ватикан В (&quot;Австралия&quot;,&quot;Сингапур&quot;) и len ([PostalCode]) &lt; &gt; 4</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Сообщение</strong>: почтовый индекс должен иметь 4 символа. <strong>Гудок</strong>: <strong>естипе</strong>: <strong>Информатионтитле</strong>: ошибка почтового кода</p></td>
<td><p>Если почтовый индекс не имеет 4 символов, отобразится сообщение.</p></td>
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
<td><p><strong>Имя элемента управления</strong>: PostalCode</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>([Страна] = &quot;Канада&quot;) And ([PostalCode], не&quot;например [A-z] [0-9] [A-z] [0-9] [A-z] [0-9&quot;])</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Сообщение</strong>: недопустимый почтовый индекс. Пример кода канадского канадского: H1J 1C3 <strong>Beep</strong>: <strong>естипе</strong>: <strong>Информатионтитле</strong>: ошибка почтового кода</p></td>
<td><p>Если почтовый индекс не подходит для Канады, отобразите сообщение. (Пример канадского кода: H1J 1C3)</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p><strong>CancelEvent</strong></p></td>
<td><p></p></td>
<td><p>Отмена события.</p></td>
</tr>
</tbody>
</table>

