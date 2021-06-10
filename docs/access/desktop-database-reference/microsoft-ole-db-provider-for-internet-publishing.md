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
# <a name="microsoft-ole-db-provider-for-internet-publishing"></a><span data-ttu-id="f6127-102">Поставщик Microsoft OLE DB для публикации в Интернете</span><span class="sxs-lookup"><span data-stu-id="f6127-102">Microsoft OLE DB Provider for Internet Publishing</span></span>

<span data-ttu-id="f6127-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f6127-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f6127-104">Поставщик DB Microsoft OLE для публикации в Интернете позволяет ADO получать доступ к ресурсам, обслуживаемой Microsoft FrontPage или Microsoft Internet Information Server.</span><span class="sxs-lookup"><span data-stu-id="f6127-104">The Microsoft OLE DB Provider for Internet Publishing allows ADO to access resources served by Microsoft FrontPage or Microsoft Internet Information Server.</span></span> <span data-ttu-id="f6127-105">Ресурсы включают файлы веб-источников, такие как HTML-файлы или Windows 2000 веб-папок.</span><span class="sxs-lookup"><span data-stu-id="f6127-105">Resources include web source files such as HTML files, or Windows 2000 web folders.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="f6127-106">Параметры строки подключения</span><span class="sxs-lookup"><span data-stu-id="f6127-106">Connection string parameters</span></span>

<span data-ttu-id="f6127-107">Чтобы подключиться к этому поставщику, установите *аргумент поставщика* свойства [ConnectionString:](connectionstring-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="f6127-107">To connect to this provider, set the *Provider* argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```vb 
 
MSDAIPP.DSO 
```

<span data-ttu-id="f6127-108">Это значение также можно установить или прочитать с помощью свойства [Provider.](provider-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="f6127-108">This value can also be set or read using the [Provider](provider-property-ado.md) property.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="f6127-109">Типичная строка подключения</span><span class="sxs-lookup"><span data-stu-id="f6127-109">Typical connection string</span></span>

<span data-ttu-id="f6127-110">Типичная строка подключения для этого поставщика:</span><span class="sxs-lookup"><span data-stu-id="f6127-110">A typical connection string for this provider is:</span></span>

```vb 
 
"Provider=MSDAIPP.DSO;Data Source=ResourceURL;User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="f6127-111">\-or-</span><span class="sxs-lookup"><span data-stu-id="f6127-111">\-or-</span></span>

```vb 
 
"URL=ResourceURL;User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="f6127-112">Строка состоит из этих ключевых слов:</span><span class="sxs-lookup"><span data-stu-id="f6127-112">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f6127-113">Ключевое слово</span><span class="sxs-lookup"><span data-stu-id="f6127-113">Keyword</span></span></p></th>
<th><p><span data-ttu-id="f6127-114">Description</span><span class="sxs-lookup"><span data-stu-id="f6127-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f6127-115"><strong>Поставщик</strong></span><span class="sxs-lookup"><span data-stu-id="f6127-115"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="f6127-116">Указывает поставщика OLE DB для интернет-публикации.</span><span class="sxs-lookup"><span data-stu-id="f6127-116">Specifies the OLE DB Provider for Internet Publishing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f6127-117"><strong>Источник</strong> данных или <strong>URL-адрес</strong></span><span class="sxs-lookup"><span data-stu-id="f6127-117"><strong>Data Source</strong> -or- <strong>URL</strong></span></span></p></td>
<td><p><span data-ttu-id="f6127-118">Указывает URL-адрес файла или каталога, опубликованный в веб-папке.</span><span class="sxs-lookup"><span data-stu-id="f6127-118">Specifies the URL of a file or directory published in a web folder.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f6127-119"><strong>Идентификатор пользователя</strong></span><span class="sxs-lookup"><span data-stu-id="f6127-119"><strong>User ID</strong></span></span></p></td>
<td><p><span data-ttu-id="f6127-120">Задает имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="f6127-120">Specifies the user name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f6127-121"><strong>Password</strong></span><span class="sxs-lookup"><span data-stu-id="f6127-121"><strong>Password</strong></span></span></p></td>
<td><p><span data-ttu-id="f6127-122">Указывает пароль пользователя.</span><span class="sxs-lookup"><span data-stu-id="f6127-122">Specifies the user password.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f6127-123">Если значение *ResourceURL* в строке подключения "URL=" задано как недействительное, по умолчанию поставщик публикаций в Интернете поднимает диалоговое окно для запроса допустимого значения.</span><span class="sxs-lookup"><span data-stu-id="f6127-123">If you set the *ResourceURL* value from the "URL=" in the connection string to an invalid value, by default the Internet Publishing Provider raises a dialog box to prompt for a valid value.</span></span> <span data-ttu-id="f6127-124">Это нежелательное поведение для компонента в среднем уровне приложения, так как оно приостанавливать выполнение программы до тех пор, пока диалоговое окно не будет очищено, а клиент, как представляется, замерзнет, так как не получил ответа от компонента.</span><span class="sxs-lookup"><span data-stu-id="f6127-124">This is undesirable behavior for a component in the middle tier of an application, because it suspends program execution until the dialog box is cleared and the client appears to freeze because it has not received a response from the component.</span></span>

> [!NOTE]
> <span data-ttu-id="f6127-125">Если MSDAIPP. DSO явно указывается как значение поставщика, либо  с ключевым словом  строки подключения поставщика или свойством Provider, вы не можете использовать URL=" в строке подключения.</span><span class="sxs-lookup"><span data-stu-id="f6127-125">If MSDAIPP.DSO is explicitly specified as the value of the provider, either with the *Provider* connection string keyword or the **Provider** property, you cannot use "URL=" in the connection string.</span></span> <span data-ttu-id="f6127-126">Если это произойдет, произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="f6127-126">If you do, an error will occur.</span></span> <span data-ttu-id="f6127-127">Вместо этого просто укажите URL-адрес, как показано в разделе [Использование ADO с поставщиком OLE DB для публикации в Интернете](the-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="f6127-127">Instead, simply specify the URL as shown in the topic [Using ADO with the OLE DB Provider for Internet Publishing](the-ole-db-provider-for-internet-publishing.md).</span></span>

