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


Действие **ClearMacroError** можно использовать для очистки сведений об ошибке, хранимой в объекте **MacroError.**

## <a name="setting"></a>Setting

Действие **ClearMacroError** не имеет аргументов.

## <a name="remarks"></a>Заметки

- При ошибке макроса сведения об ошибке сохраняются в **объекте MacroError.** Если вы не использовали действие **[OnError](onerror-macro-action.md)** для подавления сообщений об ошибках, макрос останавливается, а сведения об ошибке отображаются в стандартном сообщении об ошибке. Однако если вы использовали действие **OnError** для подавления сообщений об ошибках, может потребоваться использовать сведения, хранимые в объекте **MacroError** в условии или в настраиваемом сообщении об ошибке.
    
  После обработки ошибки данные в объекте **MacroError** устарели, поэтому лучше очистить объект с помощью действия **ClearMacroError.** Это сбрасывает номер ошибки в **объекте MacroError** до 0 и очищает любые другие сведения об ошибке, хранимые в объекте, такие как описание ошибки, имя макроса, имя действия, условие и аргументы. Таким образом, вы сможете проверить объект **MacroError** позже, чтобы узнать, произошла ли другая ошибка.

- Объект **MacroError** автоматически очищается по окончании любого макроса, поэтому нет необходимости использовать действие **ClearMacroError** в конце макроса.

- Объект **MacroError содержит** сведения только об одной ошибке за раз. Если в макросах произошло несколько ошибок, объект **MacroError** содержит сведения только о последней ошибке.

- Чтобы запустить действие **ClearMacroError** в модуле VBA, используйте метод **ClearMacroError** объекта **DoCmd.**

## <a name="example"></a>Пример

Следующий макрос использует действие **OnError** с аргументом **Next** для подавления сообщений об ошибках, а затем использует действие **OpenForm** для открытия формы. В этом примере намеренно создается ошибка с помощью действия **GoToRecord,** чтобы перейти к предыдущей записи. Условие **\[ \] MacroError. \[ Номер \] \< \> 0** проверяет **объект MacroError.** Если произошла ошибка, номер ошибки не является нулем, и выполняется **действие MessageBox.** В окне сообщения отображается имя действия, вызвав которого произошла ошибка (в данном случае — действие **GoToRecord),** и отображается номер ошибки. Наконец, при запуске **действия ClearMacroError** очищается объект **MacroError.**

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Condition</p></th>
<th><p>Action</p></th>
<th><p>Аргументы</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><strong>OnError</strong></p></td>
<td><p><strong>Go to</strong>: <strong>Next</strong></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><strong>OpenForm</strong></p></td>
<td><p><strong>Имя формы</strong>: CategoryForm<strong>View</strong>: <strong>FormWindow Mode</strong>: <strong>Normal</strong></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>GoToRecord</strong></p></td>
<td><p><strong>Тип объекта</strong>: <strong>имя formObject</strong>: CategoryForm<strong>Record</strong>: Previous</p></td>
</tr>
<tr class="even">
<td><p>[MacroError]. [Number] &lt; &gt; 0</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Message</strong>: = &quot; Error # &quot; &amp; [MacroError].[ Number] &amp; &quot; on &quot; &amp; [MacroError].[ Действие &amp; &quot; ActionName]. &quot; <strong>Beep</strong>: <strong>YesType</strong>: Information</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>ClearMacroError</strong></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

