---
title: Макрокоманда SendEmail
TOCTitle: SendEmail macro action
ms:assetid: 84ff6b46-d239-4716-9964-5b909656d347
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196780(v=office.15)
ms:contentKeyID: 48546046
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a5016500b62a465f21ecab93a6fb66c9e6d514e1
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998842"
---
# <a name="sendemail-macro-action"></a>Макрокоманда SendEmail

**Применимо к**: Access 2013, Office 2013

Действие **sendemail действие** отправляет сообщение электронной почты.

> [!NOTE]
> Действие **sendemail действие** доступно только в макросов данных.

## <a name="setting"></a>Параметр

Действие **sendemail действие** имеет следующие аргументы.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument</p></th>
<th><p>Обязательный</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Задача</strong></p></td>
<td><p>Да</p></td>
<td><p>Получатели сообщения, имена которых требуется включить в строке <strong>Кому</strong> в сообщении. Разделите имена получателей, которые задают этот аргумент (и аргументы <em>«копия»</em> и <em>«СК»</em> ) точкой с запятой (;).</p></td>
</tr>
<tr class="even">
<td><p><strong>«Копия»</strong></p></td>
<td><p>Нет</p></td>
<td><p>Получатели сообщения, имена которых следует разместить на «копия» (&quot;копии&quot;) в строке сообщения.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Скрытой копии</strong></p></td>
<td><p>Нет</p></td>
<td><p>Получатели сообщения, имена которых требуется включить в скрытой копии (&quot;скрытой копии&quot;) в строке сообщения.</p></td>
</tr>
<tr class="even">
<td><p><strong>Subject</strong></p></td>
<td><p>Нет</p></td>
<td><p>Тема сообщения. Этот текст отображается в строке <strong>темы</strong> сообщения.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Body</strong></p></td>
<td><p>Нет</p></td>
<td><p>Текст, который требуется включить в основном тексте сообщения электронной почты. Если оставить это аргумент, никакой текст включается в сообщении.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

**Sendemail действие** действие доступно только в **[После удаления](after-delete-macro-event.md)**, **[После вставки](after-insert-macro-event.md)** и события макрос **[После обновления](after-update-macro-event.md)** .

Действие **sendemail действие** не отображает сообщение для редактирования.

