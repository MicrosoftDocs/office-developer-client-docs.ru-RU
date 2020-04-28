---
title: Макрокоманда SendEmail
TOCTitle: SendEmail macro action
ms:assetid: 84ff6b46-d239-4716-9964-5b909656d347
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196780(v=office.15)
ms:contentKeyID: 48546046
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c0fa220b3088cde46b0e82631c06520afd839c64
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314653"
---
# <a name="sendemail-macro-action"></a>Макрокоманда SendEmail

**Область применения**: Access 2013, Office 2013

Действие **SendEmail** отправляет сообщение электронной почты.

> [!NOTE]
> Действие **SendEmail** доступно только в макросах данных.

## <a name="setting"></a>Параметр

Макрокоманда **SendEmail** имеет следующие аргументы.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Аргумент</p></th>
<th><p>Обязательный</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>To</strong></p></td>
<td><p>Да</p></td>
<td><p>Получатели сообщения, чьи имена вы хотите поместить в строку " <strong>Кому</strong> " в сообщении. Разделяйте имена получателей, указанные в этом аргументе (а в аргументах <em>"копия"</em> и <em>"СК"</em> ), точкой с запятой (;).</p></td>
</tr>
<tr class="even">
<td><p><strong>Cc</strong></p></td>
<td><p>Нет</p></td>
<td><p>Получатели сообщения, чьи имена вы хотите поместить в строку CC (&quot;копия&quot;) сообщения.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Bcc</strong></p></td>
<td><p>Нет</p></td>
<td><p>Получатели сообщения, имена которых необходимо поместить в строку "СК" (&quot;Скрытая копия&quot;) в сообщении.</p></td>
</tr>
<tr class="even">
<td><p><strong>Тема</strong></p></td>
<td><p>Нет</p></td>
<td><p>Тема сообщения. Этот текст отображается в строке <strong>темы</strong> сообщения.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Основной текст</strong></p></td>
<td><p>Нет</p></td>
<td><p>Текст, который необходимо включить в основной текст почтового сообщения. Если оставить этот аргумент пустым, в сообщение не будет добавлен никакой дополнительный текст.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Действие **SendEmail** доступно только в макросах **[после удаления](after-delete-macro-event.md)**, **[после вставки](after-insert-macro-event.md)** и **[после обновления](after-update-macro-event.md)** событий макросов.

Действие **SendEmail** не отображает сообщение для редактирования.

