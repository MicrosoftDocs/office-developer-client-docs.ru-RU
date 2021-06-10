---
title: Раздел Connect в файле настройки
TOCTitle: Customization File Connect section
ms:assetid: 037abfb4-798d-4b09-6133-356969aee95c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248802(v=office.15)
ms:contentKeyID: 48542985
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8652aa2c028350aab79cdf101cba189026b9a5ae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295144"
---
# <a name="customization-file-connect-section"></a><span data-ttu-id="7bdc4-102">Раздел Connect в файле настройки</span><span class="sxs-lookup"><span data-stu-id="7bdc4-102">Customization File Connect section</span></span>

<span data-ttu-id="7bdc4-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7bdc4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7bdc4-104">Поведение обработера по умолчанию — отказ от всех подключений.</span><span class="sxs-lookup"><span data-stu-id="7bdc4-104">The default behavior of the handler is to deny all connections.</span></span> <span data-ttu-id="7bdc4-105">Раздел **connect** указывает исключения из этого поведения.</span><span class="sxs-lookup"><span data-stu-id="7bdc4-105">The **connect** section specifies exceptions to that behavior.</span></span> <span data-ttu-id="7bdc4-106">Например, если все разделы **подключения** отсутствовали или пусто, то по умолчанию подключения не удалось сделать.</span><span class="sxs-lookup"><span data-stu-id="7bdc4-106">For example, if all the **connect** sections were absent or empty, then by default no connections could be made.</span></span>

<span data-ttu-id="7bdc4-107">Раздел **подключения** может содержать:</span><span class="sxs-lookup"><span data-stu-id="7bdc4-107">The **connect** section can contain:</span></span>

- <span data-ttu-id="7bdc4-108">Запись доступа по умолчанию, которая указывает операции чтения и записи по умолчанию, разрешенные для этого подключения.</span><span class="sxs-lookup"><span data-stu-id="7bdc4-108">A default access entry that specifies the default read and write operations allowed on this connection.</span></span> <span data-ttu-id="7bdc4-109">Если в разделе нет записи доступа по умолчанию, раздел будет игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="7bdc4-109">If there is no default access entry in the section, the section will be ignored.</span></span>

- <span data-ttu-id="7bdc4-110">Новая строка подключения, которая заменяет строку клиентского подключения.</span><span class="sxs-lookup"><span data-stu-id="7bdc4-110">A new connection string that replaces the client connection string.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bdc4-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7bdc4-111">Syntax</span></span>

<span data-ttu-id="7bdc4-112">Запись доступа по умолчанию имеет форму:</span><span class="sxs-lookup"><span data-stu-id="7bdc4-112">A default access entry is of the form:</span></span>

`Access=accessRight`

<span data-ttu-id="7bdc4-113">Запись строки подключения замены имеет форму:</span><span class="sxs-lookup"><span data-stu-id="7bdc4-113">A replacement connection string entry is of the form:</span></span>

`Connect=connectionString`

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7bdc4-114">Part</span><span class="sxs-lookup"><span data-stu-id="7bdc4-114">Part</span></span></p></th>
<th><p><span data-ttu-id="7bdc4-115">Описание</span><span class="sxs-lookup"><span data-stu-id="7bdc4-115">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7bdc4-116"><strong>Connect</strong></span><span class="sxs-lookup"><span data-stu-id="7bdc4-116"><strong>Connect</strong></span></span></p></td>
<td><p><span data-ttu-id="7bdc4-117">Буквальная строка, которая указывает, что это запись строки подключения.</span><span class="sxs-lookup"><span data-stu-id="7bdc4-117">A literal string that indicates this is a connection string entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bdc4-118"><strong><em>connectionString</em></strong></span><span class="sxs-lookup"><span data-stu-id="7bdc4-118"><strong><em>connectionString</em></strong></span></span></p></td>
<td><p><span data-ttu-id="7bdc4-119">Строка, которая заменяет всю строку клиентского подключения.</span><span class="sxs-lookup"><span data-stu-id="7bdc4-119">A string that replaces the whole client connection string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bdc4-120"><strong>Access</strong></span><span class="sxs-lookup"><span data-stu-id="7bdc4-120"><strong>Access</strong></span></span></p></td>
<td><p><span data-ttu-id="7bdc4-121">Буквальная строка, которая указывает, что это запись доступа.</span><span class="sxs-lookup"><span data-stu-id="7bdc4-121">A literal string that indicates this is an access entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bdc4-122"><strong><em>accessRight</em></strong></span><span class="sxs-lookup"><span data-stu-id="7bdc4-122"><strong><em>accessRight</em></strong></span></span></p></td>
<td><p><span data-ttu-id="7bdc4-123">Одно из следующих прав доступа:</span><span class="sxs-lookup"><span data-stu-id="7bdc4-123">One of the following access rights:</span></span></p>
<p></p>
<ul>
<li><p><span data-ttu-id="7bdc4-124"><strong>NoAccess —</strong> пользователь не может получить доступ к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="7bdc4-124"><strong>NoAccess</strong> — User cannot access the data source.</span></span></p></li>
<li><p><span data-ttu-id="7bdc4-125"><strong>ReadOnly</strong> — пользователь может читать источник данных.</span><span class="sxs-lookup"><span data-stu-id="7bdc4-125"><strong>ReadOnly</strong> — User can read the data source.</span></span></p></li>
<li><p><span data-ttu-id="7bdc4-126"><strong>ReadWrite</strong> — пользователь может читать или писать в источник данных.</span><span class="sxs-lookup"><span data-stu-id="7bdc4-126"><strong>ReadWrite</strong> — User can read or write to the data source.</span></span></p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7bdc4-127">Если вы хотите разрешить любое подключение (фактически отключив поведение обработщиков по умолчанию), установите запись доступа   в разделе подключение по умолчанию и удалите или закомментировать любой другой раздел идентификатора подключения. </span><span class="sxs-lookup"><span data-stu-id="7bdc4-127">If you want to allow any connection (in effect, disabling the default handler behavior), set the access entry in the **connect default** section to , and delete or comment out any other **connect** *identifier* section.</span></span>

