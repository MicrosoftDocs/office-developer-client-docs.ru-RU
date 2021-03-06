---
title: Макрокоманда SetWarnings
TOCTitle: SetWarnings macro action
ms:assetid: ff95b919-b1ee-c0a0-851d-71894851bb1d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837313(v=office.15)
ms:contentKeyID: 48548965
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm165020
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: acf541bde41c282b752532cb74d5ec4fa4a13ca9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308661"
---
# <a name="setwarnings-macro-action"></a>Макрокоманда SetWarnings

**Область применения**: Access 2013, Office 2013

Вы можете использовать **действие SetWarnings,** чтобы включить или отключить системные сообщения.

> [!NOTE]
> Эта макрокоманда доступна только для доверенных баз данных. 

## <a name="setting"></a>Параметр

Действие **SetWarnings имеет** следующий аргумент.

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
<td><p><strong>Предупреждения о</strong></p></td>
<td><p>Указывает, отображаются ли системные сообщения. Щелкните <strong>Да</strong> (чтобы включить системные сообщения) или <strong>Нет</strong> (для отключения системных сообщений) в поле <strong>Warnings On</strong> в разделе <strong>Аргументы</strong> действий в области макростроитель. По умолчанию используется значение <strong>Нет</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Это действие можно использовать для предотвращения остановки макроса предупреждениями и полями сообщений. Однако сообщения об ошибках всегда отображаются. Кроме того, Microsoft Access отображает любые диалоговые окна, которые требуют ввода, кроме выбора кнопки (например, **ОК,** Отмена, **Да** или **Нет)**— например, любое диалоговое окно, которое требует ввода текста или выбора одного из нескольких вариантов.

Проведение этого действия с набором аргументов **Warnings On** **Для аргумента "Нет"** имеет тот же эффект, что и нажатие ВВОДА при отображке окна предупреждения или сообщения. Обычно в ответ  на предупреждение или сообщение выбирается кнопка **ОК** или Да.

После завершения макроса Access автоматически включает отображение системных сообщений.

Часто это действие используется с помощью действия **Echo,** которое скрывает результаты макроса до завершения. Вы можете использовать **действие SetWarnings,** чтобы скрыть предупреждения и ящики сообщений.

> [!WARNING]
> Несмотря на то, что действие **SetWarnings** может упростить взаимодействие с макросами, необходимо тщательно отключить системные сообщения. В некоторых ситуациях не нужно продолжать макрос, если отображается определенное предупреждение. Если вы не уверены в результатах всех действий макроса, не следует использовать это действие.

Чтобы выполнить **действие SetWarnings** в Visual Basic для приложений (VBA), используйте метод **SetWarnings** объекта **DoCmd.**

