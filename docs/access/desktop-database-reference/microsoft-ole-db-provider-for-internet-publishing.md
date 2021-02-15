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
# <a name="microsoft-ole-db-provider-for-internet-publishing"></a><span data-ttu-id="eb703-102">Поставщик Microsoft OLE DB для публикации в Интернете</span><span class="sxs-lookup"><span data-stu-id="eb703-102">Microsoft OLE DB Provider for Internet Publishing</span></span>

<span data-ttu-id="eb703-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="eb703-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="eb703-104">Поставщик Microsoft OLE DB для публикации в Интернете позволяет ADO получать доступ к ресурсам Microsoft FrontPage или Microsoft Internet Information Server.</span><span class="sxs-lookup"><span data-stu-id="eb703-104">The Microsoft OLE DB Provider for Internet Publishing allows ADO to access resources served by Microsoft FrontPage or Microsoft Internet Information Server.</span></span> <span data-ttu-id="eb703-105">Ресурсы включают файлы веб-источника, такие как HTML-файлы, или веб-папки Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="eb703-105">Resources include web source files such as HTML files, or Windows 2000 web folders.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="eb703-106">Параметры строки подключения</span><span class="sxs-lookup"><span data-stu-id="eb703-106">Connection string parameters</span></span>

<span data-ttu-id="eb703-107">Чтобы подключиться к этому поставщику, установите для аргумента *Provider* свойства [ConnectionString:](connectionstring-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="eb703-107">To connect to this provider, set the *Provider* argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```vb 
 
MSDAIPP.DSO 
```

<span data-ttu-id="eb703-108">Это значение также можно установить или прочитать с помощью свойства [Provider.](provider-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="eb703-108">This value can also be set or read using the [Provider](provider-property-ado.md) property.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="eb703-109">Типичная строка подключения</span><span class="sxs-lookup"><span data-stu-id="eb703-109">Typical connection string</span></span>

<span data-ttu-id="eb703-110">Типичная строка подключения для этого поставщика:</span><span class="sxs-lookup"><span data-stu-id="eb703-110">A typical connection string for this provider is:</span></span>

```vb 
 
"Provider=MSDAIPP.DSO;Data Source=ResourceURL;User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="eb703-111">\-or-</span><span class="sxs-lookup"><span data-stu-id="eb703-111">\-or-</span></span>

```vb 
 
"URL=ResourceURL;User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="eb703-112">Строка состоит из таких ключевых слов:</span><span class="sxs-lookup"><span data-stu-id="eb703-112">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="eb703-113">Ключевое слово</span><span class="sxs-lookup"><span data-stu-id="eb703-113">Keyword</span></span></p></th>
<th><p><span data-ttu-id="eb703-114">Описание</span><span class="sxs-lookup"><span data-stu-id="eb703-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eb703-115"><strong>Поставщик</strong></span><span class="sxs-lookup"><span data-stu-id="eb703-115"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="eb703-116">Указывает поставщика OLE DB для публикации в Интернете.</span><span class="sxs-lookup"><span data-stu-id="eb703-116">Specifies the OLE DB Provider for Internet Publishing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb703-117"><strong>Источник данных</strong> -or-URL-адрес <strong></strong></span><span class="sxs-lookup"><span data-stu-id="eb703-117"><strong>Data Source</strong> -or- <strong>URL</strong></span></span></p></td>
<td><p><span data-ttu-id="eb703-118">Указывает URL-адрес файла или каталога, опубликованного в веб-папке.</span><span class="sxs-lookup"><span data-stu-id="eb703-118">Specifies the URL of a file or directory published in a web folder.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb703-119"><strong>Идентификатор пользователя</strong></span><span class="sxs-lookup"><span data-stu-id="eb703-119"><strong>User ID</strong></span></span></p></td>
<td><p><span data-ttu-id="eb703-120">Задает имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="eb703-120">Specifies the user name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb703-121"><strong>Password</strong></span><span class="sxs-lookup"><span data-stu-id="eb703-121"><strong>Password</strong></span></span></p></td>
<td><p><span data-ttu-id="eb703-122">Указывает пароль пользователя.</span><span class="sxs-lookup"><span data-stu-id="eb703-122">Specifies the user password.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="eb703-123">Если для значения *ResourceURL* в строке подключения задано недопустимое значение, по умолчанию поставщик публикации в Интернете вызывает диалоговое окно с запросом допустимого значения.</span><span class="sxs-lookup"><span data-stu-id="eb703-123">If you set the *ResourceURL* value from the "URL=" in the connection string to an invalid value, by default the Internet Publishing Provider raises a dialog box to prompt for a valid value.</span></span> <span data-ttu-id="eb703-124">Это нежелательно для компонента на среднем уровне приложения, так как оно приостанавливать выполнение программы, пока диалоговое окно не будет очищено и клиент завис, так как не получил ответ от компонента.</span><span class="sxs-lookup"><span data-stu-id="eb703-124">This is undesirable behavior for a component in the middle tier of an application, because it suspends program execution until the dialog box is cleared and the client appears to freeze because it has not received a response from the component.</span></span>

> [!NOTE]
> <span data-ttu-id="eb703-125">Если MSDAIPP. DSO явно указывается в качестве значения поставщика с  помощью ключевого слова "Строка подключения поставщика" или свойства **Provider,** в строке подключения нельзя использовать "URL=".</span><span class="sxs-lookup"><span data-stu-id="eb703-125">If MSDAIPP.DSO is explicitly specified as the value of the provider, either with the *Provider* connection string keyword or the **Provider** property, you cannot use "URL=" in the connection string.</span></span> <span data-ttu-id="eb703-126">В этом случае произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="eb703-126">If you do, an error will occur.</span></span> <span data-ttu-id="eb703-127">Вместо этого просто укажите URL-адрес, как показано в разделе ["Использование ADO с поставщиком OLE DB для публикации в Интернете".](the-ole-db-provider-for-internet-publishing.md)</span><span class="sxs-lookup"><span data-stu-id="eb703-127">Instead, simply specify the URL as shown in the topic [Using ADO with the OLE DB Provider for Internet Publishing](the-ole-db-provider-for-internet-publishing.md).</span></span>

