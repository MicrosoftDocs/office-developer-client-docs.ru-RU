---
title: Поставщик Microsoft OLE DB для публикации в Интернете
TOCTitle: Microsoft OLE DB Provider for Internet Publishing
ms:assetid: 5d1e8db5-dabb-0914-e11e-e2eac72bfa77
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249327(v=office.15)
ms:contentKeyID: 48545100
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c6f1c7c65d0ac1dd2a6d3ea132a31955f175bc7f
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997485"
---
# <a name="microsoft-ole-db-provider-for-internet-publishing"></a><span data-ttu-id="46893-102">Поставщик Microsoft OLE DB для публикации в Интернете</span><span class="sxs-lookup"><span data-stu-id="46893-102">Microsoft OLE DB Provider for Internet Publishing</span></span>

<span data-ttu-id="46893-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="46893-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="46893-104">Поставщик Microsoft OLE DB для публикации Интернет позволяет ADO для доступа к ресурсам удовлетворить с помощью Microsoft FrontPage или Microsoft Internet Information Server.</span><span class="sxs-lookup"><span data-stu-id="46893-104">The Microsoft OLE DB Provider for Internet Publishing allows ADO to access resources served by Microsoft FrontPage or Microsoft Internet Information Server.</span></span> <span data-ttu-id="46893-105">Ресурсы включают в себя web исходные файлы, такие как файлы HTML или веб-папок Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="46893-105">Resources include web source files such as HTML files, or Windows 2000 web folders.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="46893-106">Параметры строки подключения</span><span class="sxs-lookup"><span data-stu-id="46893-106">Connection string parameters</span></span>

<span data-ttu-id="46893-107">Для подключения к данным поставщиком, задайте для свойства [ConnectionString](connectionstring-property-ado.md) для аргумента *поставщика* :</span><span class="sxs-lookup"><span data-stu-id="46893-107">To connect to this provider, set the *Provider* argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```vb 
 
MSDAIPP.DSO 
```

<span data-ttu-id="46893-108">Это значение может быть задана или ознакомьтесь с помощью свойства [поставщика](provider-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="46893-108">This value can also be set or read using the [Provider](provider-property-ado.md) property.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="46893-109">Типичная строка подключения</span><span class="sxs-lookup"><span data-stu-id="46893-109">Typical connection string</span></span>

<span data-ttu-id="46893-110">— Это строка соединения для данного поставщика:</span><span class="sxs-lookup"><span data-stu-id="46893-110">A typical connection string for this provider is:</span></span>

```vb 
 
"Provider=MSDAIPP.DSO;Data Source=ResourceURL;User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="46893-111">\-или -</span><span class="sxs-lookup"><span data-stu-id="46893-111">\-or-</span></span>

```vb 
 
"URL=ResourceURL;User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="46893-112">Строка состоит из следующих ключевых слов:</span><span class="sxs-lookup"><span data-stu-id="46893-112">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="46893-113">Keyword</span><span class="sxs-lookup"><span data-stu-id="46893-113">Keyword</span></span></p></th>
<th><p><span data-ttu-id="46893-114">Описание</span><span class="sxs-lookup"><span data-stu-id="46893-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="46893-115"><strong>Поставщик</strong></span><span class="sxs-lookup"><span data-stu-id="46893-115"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="46893-116">Задает поставщика OLE DB для публикации в Интернете.</span><span class="sxs-lookup"><span data-stu-id="46893-116">Specifies the OLE DB Provider for Internet Publishing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46893-117"><strong>Источник данных</strong> - или - <strong>URL-адрес</strong></span><span class="sxs-lookup"><span data-stu-id="46893-117"><strong>Data Source</strong> -or- <strong>URL</strong></span></span></p></td>
<td><p><span data-ttu-id="46893-118">Задает URL-адрес файла или папки, опубликованной в веб-папку.</span><span class="sxs-lookup"><span data-stu-id="46893-118">Specifies the URL of a file or directory published in a web folder.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46893-119"><strong>Идентификатор пользователя</strong></span><span class="sxs-lookup"><span data-stu-id="46893-119"><strong>User ID</strong></span></span></p></td>
<td><p><span data-ttu-id="46893-120">Задает имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="46893-120">Specifies the user name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46893-121"><strong>Password</strong></span><span class="sxs-lookup"><span data-stu-id="46893-121"><strong>Password</strong></span></span></p></td>
<td><p><span data-ttu-id="46893-122">Задает пароль пользователя.</span><span class="sxs-lookup"><span data-stu-id="46893-122">Specifies the user password.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="46893-123">Если задано значение *ResourceURL* из «URL-адрес =» в строке подключения недопустимое значение по умолчанию службу публикации в Интернете вызывает диалоговое окно запрашивать допустимое значение.</span><span class="sxs-lookup"><span data-stu-id="46893-123">If you set the *ResourceURL* value from the "URL=" in the connection string to an invalid value, by default the Internet Publishing Provider raises a dialog box to prompt for a valid value.</span></span> <span data-ttu-id="46893-124">Это нежелательное поведение компонента на среднем уровне приложения, так как приостанавливает выполнение программы, пока диалоговое окно будет удалена, и отображается клиента для закрепления, так как не получил ответа из компонента.</span><span class="sxs-lookup"><span data-stu-id="46893-124">This is undesirable behavior for a component in the middle tier of an application, because it suspends program execution until the dialog box is cleared and the client appears to freeze because it has not received a response from the component.</span></span>

> [!NOTE]
> <span data-ttu-id="46893-125">Если MSDAIPP. DSO явным образом указаны как значение поставщика, либо с ключевым словом строки подключения *поставщика* или свойство **поставщика** , нельзя использовать «URL-адрес =» в строке подключения.</span><span class="sxs-lookup"><span data-stu-id="46893-125">If MSDAIPP.DSO is explicitly specified as the value of the provider, either with the *Provider* connection string keyword or the **Provider** property, you cannot use "URL=" in the connection string.</span></span> <span data-ttu-id="46893-126">В противном случае возникнет ошибка.</span><span class="sxs-lookup"><span data-stu-id="46893-126">If you do, an error will occur.</span></span> <span data-ttu-id="46893-127">Вместо этого просто укажите URL-адрес, как показано в разделе [С помощью ADO с помощью поставщика OLE DB для публикации Интернет](the-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="46893-127">Instead, simply specify the URL as shown in the topic [Using ADO with the OLE DB Provider for Internet Publishing](the-ole-db-provider-for-internet-publishing.md).</span></span>

