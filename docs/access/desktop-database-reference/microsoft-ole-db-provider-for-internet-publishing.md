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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699781"
---
# <a name="microsoft-ole-db-provider-for-internet-publishing"></a>Поставщик Microsoft OLE DB для публикации в Интернете

**Применимо к**: Access 2013, Office 2013

Поставщик Microsoft OLE DB для публикации Интернет позволяет ADO для доступа к ресурсам удовлетворить с помощью Microsoft FrontPage или Microsoft Internet Information Server. Ресурсы включают в себя web исходные файлы, такие как файлы HTML или веб-папок Windows 2000.

## <a name="connection-string-parameters"></a>Параметры строки подключения

Для подключения к данным поставщиком, задайте для свойства [ConnectionString](connectionstring-property-ado.md) для аргумента *поставщика* :

```vb 
 
MSDAIPP.DSO 
```

Это значение может быть задана или ознакомьтесь с помощью свойства [поставщика](provider-property-ado.md) .

## <a name="typical-connection-string"></a>Типичная строка подключения

— Это строка соединения для данного поставщика:

```vb 
 
"Provider=MSDAIPP.DSO;Data Source=ResourceURL;User ID=userName;Password=userPassword;" 
```

\-или -

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
<th><p>Keyword</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Поставщик</strong></p></td>
<td><p>Задает поставщика OLE DB для публикации в Интернете.</p></td>
</tr>
<tr class="even">
<td><p><strong>Источник данных</strong> - или - <strong>URL-адрес</strong></p></td>
<td><p>Задает URL-адрес файла или папки, опубликованной в веб-папку.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Идентификатор пользователя</strong></p></td>
<td><p>Задает имя пользователя.</p></td>
</tr>
<tr class="even">
<td><p><strong>Password</strong></p></td>
<td><p>Задает пароль пользователя.</p></td>
</tr>
</tbody>
</table>


Если задано значение *ResourceURL* из «URL-адрес =» в строке подключения недопустимое значение по умолчанию службу публикации в Интернете вызывает диалоговое окно запрашивать допустимое значение. Это нежелательное поведение компонента на среднем уровне приложения, так как приостанавливает выполнение программы, пока диалоговое окно будет удалена, и отображается клиента для закрепления, так как не получил ответа из компонента.

> [!NOTE]
> Если MSDAIPP. DSO явным образом указаны как значение поставщика, либо с ключевым словом строки подключения *поставщика* или свойство **поставщика** , нельзя использовать «URL-адрес =» в строке подключения. В противном случае возникнет ошибка. Вместо этого просто укажите URL-адрес, как показано в разделе [С помощью ADO с помощью поставщика OLE DB для публикации Интернет](the-ole-db-provider-for-internet-publishing.md).

