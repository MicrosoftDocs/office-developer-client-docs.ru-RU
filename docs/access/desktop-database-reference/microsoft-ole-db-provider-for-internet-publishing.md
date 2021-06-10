---
title: Поставщик Microsoft OLE DB для публикации в Интернете
TOCTitle: Microsoft OLE DB Provider for Internet Publishing
ms:assetid: 5d1e8db5-dabb-0914-e11e-e2eac72bfa77
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249327(v=office.15)
ms:contentKeyID: 48545100
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 38183cd8306f2425a362bd2650639120a2d16845
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288969"
---
# <a name="microsoft-ole-db-provider-for-internet-publishing"></a>Поставщик Microsoft OLE DB для публикации в Интернете

**Область применения**: Access 2013, Office 2013

Поставщик DB Microsoft OLE для публикации в Интернете позволяет ADO получать доступ к ресурсам, обслуживаемой Microsoft FrontPage или Microsoft Internet Information Server. Ресурсы включают файлы веб-источников, такие как HTML-файлы или Windows 2000 веб-папок.

## <a name="connection-string-parameters"></a>Параметры строки подключения

Чтобы подключиться к этому поставщику, установите *аргумент поставщика* свойства [ConnectionString:](connectionstring-property-ado.md)

```vb 
 
MSDAIPP.DSO 
```

Это значение также можно установить или прочитать с помощью свойства [Provider.](provider-property-ado.md)

## <a name="typical-connection-string"></a>Типичная строка подключения

Типичная строка подключения для этого поставщика:

```vb 
 
"Provider=MSDAIPP.DSO;Data Source=ResourceURL;User ID=userName;Password=userPassword;" 
```

\-or-

```vb 
 
"URL=ResourceURL;User ID=userName;Password=userPassword;" 
```

Строка состоит из этих ключевых слов:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Ключевое слово</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Поставщик</strong></p></td>
<td><p>Указывает поставщика OLE DB для интернет-публикации.</p></td>
</tr>
<tr class="even">
<td><p><strong>Источник</strong> данных или <strong>URL-адрес</strong></p></td>
<td><p>Указывает URL-адрес файла или каталога, опубликованный в веб-папке.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Идентификатор пользователя</strong></p></td>
<td><p>Задает имя пользователя.</p></td>
</tr>
<tr class="even">
<td><p><strong>Password</strong></p></td>
<td><p>Указывает пароль пользователя.</p></td>
</tr>
</tbody>
</table>


Если значение *ResourceURL* в строке подключения "URL=" задано как недействительное, по умолчанию поставщик публикаций в Интернете поднимает диалоговое окно для запроса допустимого значения. Это нежелательное поведение для компонента в среднем уровне приложения, так как оно приостанавливать выполнение программы до тех пор, пока диалоговое окно не будет очищено, а клиент, как представляется, замерзнет, так как не получил ответа от компонента.

> [!NOTE]
> Если MSDAIPP. DSO явно указывается как значение поставщика, либо  с ключевым словом  строки подключения поставщика или свойством Provider, вы не можете использовать URL=" в строке подключения. Если это произойдет, произойдет ошибка. Вместо этого просто укажите URL-адрес, как показано в разделе [Использование ADO с поставщиком OLE DB для публикации в Интернете](the-ole-db-provider-for-internet-publishing.md).

