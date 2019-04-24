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
# <a name="customization-file-connect-section"></a><span data-ttu-id="981a8-102">Раздел Connect в файле настройки</span><span class="sxs-lookup"><span data-stu-id="981a8-102">Customization File Connect section</span></span>

<span data-ttu-id="981a8-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="981a8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="981a8-104">Поведение обработчика по умолчанию — запретить все подключения.</span><span class="sxs-lookup"><span data-stu-id="981a8-104">The default behavior of the handler is to deny all connections.</span></span> <span data-ttu-id="981a8-105">В разделе **Connect** задаются исключения из этого правила.</span><span class="sxs-lookup"><span data-stu-id="981a8-105">The **connect** section specifies exceptions to that behavior.</span></span> <span data-ttu-id="981a8-106">Например, если все разделы **Connect** отсутствовали или пусты, по умолчанию подключения не доводились.</span><span class="sxs-lookup"><span data-stu-id="981a8-106">For example, if all the **connect** sections were absent or empty, then by default no connections could be made.</span></span>

<span data-ttu-id="981a8-107">Раздел **Connect** может содержать следующие компоненты:</span><span class="sxs-lookup"><span data-stu-id="981a8-107">The **connect** section can contain:</span></span>

- <span data-ttu-id="981a8-108">Запись доступа по умолчанию, указывающая на операции чтения и записи, разрешенные для данного подключения.</span><span class="sxs-lookup"><span data-stu-id="981a8-108">A default access entry that specifies the default read and write operations allowed on this connection.</span></span> <span data-ttu-id="981a8-109">Если в разделе нет записи доступа по умолчанию, раздел будет проигнорирован.</span><span class="sxs-lookup"><span data-stu-id="981a8-109">If there is no default access entry in the section, the section will be ignored.</span></span>

- <span data-ttu-id="981a8-110">Новая строка подключения, заменяющая строку подключения клиента.</span><span class="sxs-lookup"><span data-stu-id="981a8-110">A new connection string that replaces the client connection string.</span></span>

## <a name="syntax"></a><span data-ttu-id="981a8-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="981a8-111">Syntax</span></span>

<span data-ttu-id="981a8-112">Запись доступа по умолчанию имеет вид:</span><span class="sxs-lookup"><span data-stu-id="981a8-112">A default access entry is of the form:</span></span>

`Access=accessRight`

<span data-ttu-id="981a8-113">Для записи строки подключения заменяется форма:</span><span class="sxs-lookup"><span data-stu-id="981a8-113">A replacement connection string entry is of the form:</span></span>

`Connect=connectionString`

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="981a8-114">Часть</span><span class="sxs-lookup"><span data-stu-id="981a8-114">Part</span></span></p></th>
<th><p><span data-ttu-id="981a8-115">Описание</span><span class="sxs-lookup"><span data-stu-id="981a8-115">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="981a8-116"><strong>Connect</strong></span><span class="sxs-lookup"><span data-stu-id="981a8-116"><strong>Connect</strong></span></span></p></td>
<td><p><span data-ttu-id="981a8-117">Строка литерала, указывающая на запись строки подключения.</span><span class="sxs-lookup"><span data-stu-id="981a8-117">A literal string that indicates this is a connection string entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="981a8-118"><strong><em>connectionString</em></strong></span><span class="sxs-lookup"><span data-stu-id="981a8-118"><strong><em>connectionString</em></strong></span></span></p></td>
<td><p><span data-ttu-id="981a8-119">Строка, заменяющая всю строку подключения клиента.</span><span class="sxs-lookup"><span data-stu-id="981a8-119">A string that replaces the whole client connection string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="981a8-120"><strong>Access</strong></span><span class="sxs-lookup"><span data-stu-id="981a8-120"><strong>Access</strong></span></span></p></td>
<td><p><span data-ttu-id="981a8-121">Строка литерала, указывающая, что это запись доступа.</span><span class="sxs-lookup"><span data-stu-id="981a8-121">A literal string that indicates this is an access entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="981a8-122"><strong><em>Акцессригхт</em></strong></span><span class="sxs-lookup"><span data-stu-id="981a8-122"><strong><em>accessRight</em></strong></span></span></p></td>
<td><p><span data-ttu-id="981a8-123">Одно из следующих прав доступа:</span><span class="sxs-lookup"><span data-stu-id="981a8-123">One of the following access rights:</span></span></p>
<p></p>
<ul>
<li><p><span data-ttu-id="981a8-124">Нет <strong>доступа</strong> , пользователь не может получить доступ к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="981a8-124"><strong>NoAccess</strong> — User cannot access the data source.</span></span></p></li>
<li><p><span data-ttu-id="981a8-125"><strong>ReadOnly</strong> — пользователь может читать источник данных.</span><span class="sxs-lookup"><span data-stu-id="981a8-125"><strong>ReadOnly</strong> — User can read the data source.</span></span></p></li>
<li><p><span data-ttu-id="981a8-126"><strong>ReadWrite</strong> — пользователь может выполнять чтение или запись в источник данных.</span><span class="sxs-lookup"><span data-stu-id="981a8-126"><strong>ReadWrite</strong> — User can read or write to the data source.</span></span></p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="981a8-127">Если требуется разрешить любое подключение (в результате чего отключается поведение обработчика по умолчанию), задайте запись доступа в разделе **подключить по умолчанию** , а затем удалите или закомментируйте любой другой раздел **Connect** *identifier* .</span><span class="sxs-lookup"><span data-stu-id="981a8-127">If you want to allow any connection (in effect, disabling the default handler behavior), set the access entry in the **connect default** section to , and delete or comment out any other **connect** *identifier* section.</span></span>

