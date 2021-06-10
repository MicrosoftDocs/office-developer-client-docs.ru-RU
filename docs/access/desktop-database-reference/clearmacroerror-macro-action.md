---
title: Макрокоманда ClearMacroError
TOCTitle: ClearMacroError macro action
ms:assetid: 1091747e-e957-38c6-6454-5169f091323e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845338(v=office.15)
ms:contentKeyID: 48543296
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm109100
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f42386674ff76d550fb47a971860b4e1a5905236
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296376"
---
# <a name="clearmacroerror-macro-action"></a>Макрокоманда ClearMacroError


**Область применения**: Access 2013, Office 2013


Вы можете использовать **действие ClearMacroError** для очистки сведений об ошибке, хранимой в объекте **MacroError.**

## <a name="setting"></a>Параметр

Действие **ClearMacroError** не имеет аргументов.

## <a name="remarks"></a>Примечания

- При ошибке макроса сведения об ошибке хранятся в объекте **MacroError.** Если вы не использовали действие **[OnError](onerror-macro-action.md)** для подавления сообщений об ошибках, макрос останавливается, а сведения об ошибках отображаются в стандартном сообщении об ошибке. Однако если для подавления сообщений об ошибках используется действие **OnError,** может потребоваться использовать сведения, хранимые в объекте **MacroError** в состоянии или в настраиваемом сообщении об ошибке.
    
  После обработки ошибки сведения в объекте **MacroError** устарели, поэтому лучше очистить объект с помощью действия **ClearMacroError.** При этом номер ошибки в объекте **MacroError** сбрасывается до 0 и очищается от любых других сведений об ошибке, хранимой в объекте, таких как описание ошибки, имя макроса, имя действия, состояние и аргументы. Таким образом, вы можете проверить объект **MacroError** еще раз позже, чтобы узнать, произошла ли еще одна ошибка.

- Объект **MacroError** автоматически очищается после окончания макроса, поэтому в конце макроса не требуется использовать действие **ClearMacroError.**

- Объект **MacroError содержит** сведения только об одной ошибке одновременно. Если на макросе произошло несколько ошибок, объект **MacroError** содержит сведения только о последней ошибке.

- Чтобы выполнить **действие ClearMacroError** в модуле VBA, используйте метод **ClearMacroError** объекта **DoCmd.**

## <a name="example"></a>Пример

Следующий макрос использует действие **OnError** с аргументом **Next** для подавления сообщений об ошибках, а затем использует **действие OpenForm** для открытия формы. В этом примере ошибка намеренно создается с помощью **действия GoToRecord** для перейти к предыдущей записи. Условие **\[ MacroError \] . \[ Номер \] \< \> 0** проверяет **объект MacroError.** Если произошла ошибка, номер ошибки не нулевой, а действие **MessageBox** выполняется. В поле сообщений отображается имя действия, вызываемого ошибкой (в данном случае действия **GoToRecord),** и отображается номер ошибки. Наконец, при запуске **действия ClearMacroError** очищается **объект MacroError.**

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Условие</p></th>
<th><p>Action</p></th>
<th><p>Аргументы</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><strong>OnError</strong></p></td>
<td><p><strong>Перейти к</strong>: <strong>Далее</strong></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><strong>OpenForm</strong></p></td>
<td><p><strong>Имя формы:</strong>Представление<strong></strong>CategoryForm : <strong>FormWindow Mode</strong>: <strong>Normal</strong></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>GoToRecord</strong></p></td>
<td><p><strong>Тип объекта:</strong> <strong>Имя FormObject</strong>: CategoryForm<strong>Record</strong>: Previous</p></td>
</tr>
<tr class="even">
<td><p>[MacroError]. [Номер] &lt; &gt; 0</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Сообщение:</strong>= &quot; Ошибка # &quot; &amp; [MacroError].[ Номер] &amp; &quot; &quot; &amp; на [MacroError].[ Действие &amp; &quot; ActionName. &quot; <strong>Звуковой сигнал:</strong> <strong>YesType</strong>: Информация</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>ClearMacroError</strong></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

