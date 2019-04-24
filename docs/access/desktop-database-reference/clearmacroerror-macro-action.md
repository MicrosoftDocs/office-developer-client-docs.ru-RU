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


С помощью действия **клеармакроеррор** можно очистить сведения об ошибке, которая хранится в объекте **MacroError** .

## <a name="setting"></a>Параметр

Действие **клеармакроеррор** не имеет аргументов.

## <a name="remarks"></a>Замечания

- При возникновении ошибки в макросе сведения об ошибке хранятся в объекте **MacroError** . Если вы не использовали действие **[OnError](onerror-macro-action.md)** для подавления сообщений об ошибках, макрос перестает работать, а сведения об ошибке отображаются в стандартном сообщении об ошибке. Тем не менее, если вы использовали **** действие OnError для подавления сообщений об ошибках, может потребоваться использовать сведения, хранящиеся в объекте **MacroError** в условии или в настраиваемом сообщении об ошибке.
    
  После того как ошибка будет обработана, сведения в объекте **MacroError** устарели, поэтому рекомендуется очистить объект с помощью действия **клеармакроеррор** . При этом номер ошибки в объекте **MacroError** сбрасывается на 0 и удаляется любая другая информация об ошибке, которая хранится в объекте, например описание ошибки, имя макроса, имя действия, условие и аргументы. Таким образом, вы можете снова проверить объект **MacroError** , чтобы проверить, произошла ли другая ошибка.

- Объект **MacroError** автоматически очищается при завершении любого макроса, поэтому не нужно использовать действие **клеармакроеррор** в конце макроса.

- Объект **MacroError** содержит сведения только об одной ошибке за раз. Если в макросе произошла более одной ошибки, объект **MacroError** содержит сведения только о последней ошибке.

- Чтобы выполнить действие **клеармакроеррор** в модуле VBA, используйте метод **клеармакроеррор** объекта **DoCmd** .

## <a name="example"></a>Пример

Следующий макрос использует действие **OnError** со **следующим** аргументом для подавления сообщений об ошибках, а затем использует макрокоманду "ОткрытьФорму" ( **OpenForm** ) для открытия формы. В этом примере ошибка намеренно создается с помощью действия **GoToRecord** для перехода к предыдущей записи. Условие ** \[MacroError\].\[ \>Номер\]\<0** тестирует объект **MacroError** . При возникновении ошибки номер ошибки не равен нулю и выполняется действие **MessageBox** . В окне сообщения отображается имя действия, которое вызвало ошибку (в данном случае, действие **GoToRecord** ) и отображается номер ошибки. Наконец, выполнение действия **клеармакроеррор** очищает объект **MacroError** .

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Условие</p></th>
<th><p>Действие</p></th>
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
<td><p><strong>Имя формы</strong>: категориформ<strong>View</strong>: <strong>режим формвиндов</strong>: <strong>обычный</strong></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>GoToRecord</strong></p></td>
<td><p><strong>Тип объекта</strong>: <strong>формобжект Name</strong>: категориформ<strong>Record</strong>: Previous</p></td>
</tr>
<tr class="even">
<td><p>[MacroError]. Значение &lt; &gt;0</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Сообщение</strong>: =&quot;ошибка # &quot; &amp; [MacroError]. Значение &amp; &quot; [ &quot; MacroError &amp; ]. ActionName &amp; &quot; ). &quot; <strong>Гудок</strong>: <strong>естипе</strong>: Information</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>ClearMacroError</strong></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

