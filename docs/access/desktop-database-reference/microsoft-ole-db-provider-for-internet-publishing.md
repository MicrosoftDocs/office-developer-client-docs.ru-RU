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

Поставщик Microsoft OLE DB для публикации в Интернете позволяет ADO получать доступ к ресурсам, обслуживаемым Microsoft FrontPage или Microsoft Internet Information Server. Ресурсы включают в себя веб-исходные файлы, такие как HTML-файлы, или веб-папки Windows 2000.

## <a name="connection-string-parameters"></a>Параметры строки подключения

Чтобы подключиться к поставщику, присвойте аргументу *provider* свойства [ConnectionString](connectionstring-property-ado.md) значение:

```vb 
 
MSDAIPP.DSO 
```

Это значение также можно задать или прочитать с помощью свойства [provider](provider-property-ado.md) .

## <a name="typical-connection-string"></a>Типичная строка подключения

Типичная строка подключения для этого поставщика:

```vb 
 
"Provider=MSDAIPP.DSO;Data Source=ResourceURL;User ID=userName;Password=userPassword;" 
```

\-также

```vb 
 
"URL=ResourceURL;User ID=userName;Password=userPassword;" 
```

Строка состоит из следующих ключевых слов:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Ключевое слово</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Поставщик</strong></p></td>
<td><p>Указывает поставщика OLE DB для публикации в Интернете.</p></td>
</tr>
<tr class="even">
<td><p><strong>Источник данных</strong> или URL- <strong>адрес</strong></p></td>
<td><p>Указывает URL-адрес файла или каталога, опубликованного в веб-папке.</p></td>
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


Если вы задаете значение *resourceurl экземпляром* из "URL =" в строке подключения к недопустимому значению, то по умолчанию поставщик публикации в Интернете создает диалоговое окно с запросом на допустимое значение. Это нежелательное поведение компонента на среднем уровне приложения, так как оно приостанавливает выполнение программы, пока не будет снято диалоговое окно, и клиент перестанет закрепляться, так как он не получил ответ от компонента.

> [!NOTE]
> Если МСДАИПП. DSO явно задаются в качестве значения поставщика с помощью ключевого слова строки подключения *поставщика* или свойства **provider** , в строке подключения нельзя использовать значение "URL =". В противном случае возникнет ошибка. Вместо этого просто укажите URL-адрес, как показано в разделе [Использование ADO с поставщиком OLE DB для публикации в Интернете](the-ole-db-provider-for-internet-publishing.md).

