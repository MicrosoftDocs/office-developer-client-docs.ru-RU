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
# <a name="microsoft-ole-db-provider-for-internet-publishing"></a><span data-ttu-id="30972-102">Поставщик Microsoft OLE DB для публикации в Интернете</span><span class="sxs-lookup"><span data-stu-id="30972-102">Microsoft OLE DB Provider for Internet Publishing</span></span>

<span data-ttu-id="30972-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="30972-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="30972-104">Поставщик Microsoft OLE DB для публикации в Интернете позволяет ADO получать доступ к ресурсам, обслуживаемым Microsoft FrontPage или Microsoft Internet Information Server.</span><span class="sxs-lookup"><span data-stu-id="30972-104">The Microsoft OLE DB Provider for Internet Publishing allows ADO to access resources served by Microsoft FrontPage or Microsoft Internet Information Server.</span></span> <span data-ttu-id="30972-105">Ресурсы включают в себя веб-исходные файлы, такие как HTML-файлы, или веб-папки Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="30972-105">Resources include web source files such as HTML files, or Windows 2000 web folders.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="30972-106">Параметры строки подключения</span><span class="sxs-lookup"><span data-stu-id="30972-106">Connection string parameters</span></span>

<span data-ttu-id="30972-107">Чтобы подключиться к поставщику, присвойте аргументу *provider* свойства [ConnectionString](connectionstring-property-ado.md) значение:</span><span class="sxs-lookup"><span data-stu-id="30972-107">To connect to this provider, set the *Provider* argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```vb 
 
MSDAIPP.DSO 
```

<span data-ttu-id="30972-108">Это значение также можно задать или прочитать с помощью свойства [provider](provider-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="30972-108">This value can also be set or read using the [Provider](provider-property-ado.md) property.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="30972-109">Типичная строка подключения</span><span class="sxs-lookup"><span data-stu-id="30972-109">Typical connection string</span></span>

<span data-ttu-id="30972-110">Типичная строка подключения для этого поставщика:</span><span class="sxs-lookup"><span data-stu-id="30972-110">A typical connection string for this provider is:</span></span>

```vb 
 
"Provider=MSDAIPP.DSO;Data Source=ResourceURL;User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="30972-111">\-также</span><span class="sxs-lookup"><span data-stu-id="30972-111">\-or-</span></span>

```vb 
 
"URL=ResourceURL;User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="30972-112">Строка состоит из следующих ключевых слов:</span><span class="sxs-lookup"><span data-stu-id="30972-112">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="30972-113">Ключевое слово</span><span class="sxs-lookup"><span data-stu-id="30972-113">Keyword</span></span></p></th>
<th><p><span data-ttu-id="30972-114">Описание</span><span class="sxs-lookup"><span data-stu-id="30972-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="30972-115"><strong>Поставщик</strong></span><span class="sxs-lookup"><span data-stu-id="30972-115"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="30972-116">Указывает поставщика OLE DB для публикации в Интернете.</span><span class="sxs-lookup"><span data-stu-id="30972-116">Specifies the OLE DB Provider for Internet Publishing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30972-117"><strong>Источник данных</strong> или URL- <strong>адрес</strong></span><span class="sxs-lookup"><span data-stu-id="30972-117"><strong>Data Source</strong> -or- <strong>URL</strong></span></span></p></td>
<td><p><span data-ttu-id="30972-118">Указывает URL-адрес файла или каталога, опубликованного в веб-папке.</span><span class="sxs-lookup"><span data-stu-id="30972-118">Specifies the URL of a file or directory published in a web folder.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="30972-119"><strong>Идентификатор пользователя</strong></span><span class="sxs-lookup"><span data-stu-id="30972-119"><strong>User ID</strong></span></span></p></td>
<td><p><span data-ttu-id="30972-120">Задает имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="30972-120">Specifies the user name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30972-121"><strong>Password</strong></span><span class="sxs-lookup"><span data-stu-id="30972-121"><strong>Password</strong></span></span></p></td>
<td><p><span data-ttu-id="30972-122">Указывает пароль пользователя.</span><span class="sxs-lookup"><span data-stu-id="30972-122">Specifies the user password.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="30972-123">Если вы задаете значение *resourceurl экземпляром* из "URL =" в строке подключения к недопустимому значению, то по умолчанию поставщик публикации в Интернете создает диалоговое окно с запросом на допустимое значение.</span><span class="sxs-lookup"><span data-stu-id="30972-123">If you set the *ResourceURL* value from the "URL=" in the connection string to an invalid value, by default the Internet Publishing Provider raises a dialog box to prompt for a valid value.</span></span> <span data-ttu-id="30972-124">Это нежелательное поведение компонента на среднем уровне приложения, так как оно приостанавливает выполнение программы, пока не будет снято диалоговое окно, и клиент перестанет закрепляться, так как он не получил ответ от компонента.</span><span class="sxs-lookup"><span data-stu-id="30972-124">This is undesirable behavior for a component in the middle tier of an application, because it suspends program execution until the dialog box is cleared and the client appears to freeze because it has not received a response from the component.</span></span>

> [!NOTE]
> <span data-ttu-id="30972-125">Если МСДАИПП. DSO явно задаются в качестве значения поставщика с помощью ключевого слова строки подключения *поставщика* или свойства **provider** , в строке подключения нельзя использовать значение "URL =".</span><span class="sxs-lookup"><span data-stu-id="30972-125">If MSDAIPP.DSO is explicitly specified as the value of the provider, either with the *Provider* connection string keyword or the **Provider** property, you cannot use "URL=" in the connection string.</span></span> <span data-ttu-id="30972-126">В противном случае возникнет ошибка.</span><span class="sxs-lookup"><span data-stu-id="30972-126">If you do, an error will occur.</span></span> <span data-ttu-id="30972-127">Вместо этого просто укажите URL-адрес, как показано в разделе [Использование ADO с поставщиком OLE DB для публикации в Интернете](the-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="30972-127">Instead, simply specify the URL as shown in the topic [Using ADO with the OLE DB Provider for Internet Publishing](the-ole-db-provider-for-internet-publishing.md).</span></span>

