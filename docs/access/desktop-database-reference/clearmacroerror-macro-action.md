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
ms.openlocfilehash: cbf672ea3dde9725916128593e18d4289fd89057
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945385"
---
# <a name="clearmacroerror-macro-action"></a>Макрокоманда ClearMacroError


**Применимо к**: Access 2013, Office 2013


Чтобы очистить сведения об ошибке, которая хранится в объекте **MacroError** можно использовать действие **ClearMacroError** .

## <a name="setting"></a>Параметр

Действие **ClearMacroError** не имеет каких-либо аргументов.

## <a name="remarks"></a>Примечания

- При возникновении ошибки в макросе, в объекте **MacroError** хранятся сведения об ошибке. Если вы не использовали **[ПриОшибке](onerror-macro-action.md)** для отмены вывода сообщений об ошибках, останавливает макросов и сведения об ошибке отображается в стандартное сообщение об ошибке. Тем не менее если используется **ПриОшибке** для отмены вывода сообщений об ошибках, можно использовать данные, хранящиеся в объекте **MacroError** в условие или пользовательское сообщение об ошибке.
    
  После обработки ошибки сведения в объекте **MacroError** является устаревшим, поэтому рекомендуется очистки объекта с помощью действия **ClearMacroError** . Это номер ошибки в объекте **MacroError** восстанавливаются значения по умолчанию 0 и очищает любые другие сведения об ошибке, хранящиеся в объекте, такие как описание ошибки, имя макроса, имя действия, условия и аргументы. Таким образом, можно проверить объект **MacroError** попытку позже для просмотра, если другой ошибки.

- Объект **MacroError** автоматически очищается после завершения любой макрос, необходимо использовать действие **ClearMacroError** в конце макроса.

- Объект **MacroError** содержит сведения об ошибке только один за раз. Если более одного ошибка в макросе, объект **MacroError** содержит сведения только о последней ошибке.

- Чтобы выполнить действие **ClearMacroError** в модуле VBA, используйте метод **ClearMacroError** **объекта** .

## <a name="example"></a>Пример

Следующий макрос использует **ПриОшибке** с **следующий** аргумент для отмены вывода сообщений об ошибках, а затем использует **ОткрытьФорму** для открытия формы. В данном примере ошибка намеренно создается с помощью **НаЗапись** для перехода к предыдущей записи. Условие ** \[MacroError\].\[ Номер\]\<\>0** тестирует объект **MacroError** . Если произошла ошибка, номер ошибки не равно нулю, и выполняется действие **MessageBox** . В окне сообщения отображается имя действия, вызвавшей ошибку (в данном случае **НаЗапись** ), и отображается номер ошибки. И, наконец выполнение действия **ClearMacroError** удаляет объект **MacroError** .

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Condition</p></th>
<th><p>Действие</p></th>
<th><p>Аргументы</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><strong>OnError</strong></p></td>
<td><p><strong>Перейдите к</strong>: <strong>Далее</strong></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><strong>ОткрытьФорму</strong></p></td>
<td><p><strong>Имя формы</strong>: CategoryForm<strong>представление</strong>: <strong>Режим FormWindow</strong>: <strong>Обычный</strong></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>GoToRecord</strong></p></td>
<td><p><strong>Тип объекта</strong>: <strong>Имя FormObject</strong>: CategoryForm<strong>запись</strong>: предыдущей</p></td>
</tr>
<tr class="even">
<td><p>[MacroError]. [Число] &lt; &gt;0</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Сообщение</strong>: =&quot;ошибка # &quot; &amp; [MacroError]. [Число] &amp; &quot; на &quot; &amp; [MacroError]. [Имя действия] &amp; &quot; действие. &quot; <strong>Звуковые сигналы</strong>: <strong>YesType</strong>: сведения</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>ClearMacroError</strong></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

