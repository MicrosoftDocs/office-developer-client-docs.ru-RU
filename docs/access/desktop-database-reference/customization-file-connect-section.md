---
title: Раздел Connect в файле настройки
TOCTitle: Customization File Connect Section
ms:assetid: 037abfb4-798d-4b09-6133-356969aee95c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248802(v=office.15)
ms:contentKeyID: 48542985
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f160fe06167cde6527b08c23ab3de69731f56dde
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867525"
---
# <a name="customization-file-connect-section"></a><span data-ttu-id="4de81-102">Раздел Connect в файле настройки</span><span class="sxs-lookup"><span data-stu-id="4de81-102">Customization File Connect Section</span></span>

<span data-ttu-id="4de81-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4de81-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4de81-104">Поведение по умолчанию обработчика является запретить все подключения.</span><span class="sxs-lookup"><span data-stu-id="4de81-104">The default behavior of the handler is to deny all connections.</span></span> <span data-ttu-id="4de81-105">В разделе **подключение** указывает исключения, чтобы это поведение.</span><span class="sxs-lookup"><span data-stu-id="4de81-105">The **connect** section specifies exceptions to that behavior.</span></span> <span data-ttu-id="4de81-106">Например если все разделы **подключение** отсутствует или пустой, затем по умолчанию подключения не удалось выполнить.</span><span class="sxs-lookup"><span data-stu-id="4de81-106">For example, if all the **connect** sections were absent or empty, then by default no connections could be made.</span></span>

<span data-ttu-id="4de81-107">В разделе **подключение** может содержать:</span><span class="sxs-lookup"><span data-stu-id="4de81-107">The **connect** section can contain:</span></span>

- <span data-ttu-id="4de81-108">Запись доступа по умолчанию определяет значение по умолчанию операций чтения и записи на этом компьютере.</span><span class="sxs-lookup"><span data-stu-id="4de81-108">A default access entry that specifies the default read and write operations allowed on this connection.</span></span> <span data-ttu-id="4de81-109">Если отсутствует запись доступа по умолчанию в разделе, разделе будет игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="4de81-109">If there is no default access entry in the section, the section will be ignored.</span></span>

- <span data-ttu-id="4de81-110">Новую строку подключения, которая заменяет строка подключения клиента.</span><span class="sxs-lookup"><span data-stu-id="4de81-110">A new connection string that replaces the client connection string.</span></span>

## <a name="syntax"></a><span data-ttu-id="4de81-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4de81-111">Syntax</span></span>

<span data-ttu-id="4de81-112">Запись доступа по умолчанию имеет вид:</span><span class="sxs-lookup"><span data-stu-id="4de81-112">A default access entry is of the form:</span></span>

`Access=accessRight`

<span data-ttu-id="4de81-113">Запись строки подключения замены имеет форму:</span><span class="sxs-lookup"><span data-stu-id="4de81-113">A replacement connection string entry is of the form:</span></span>

`Connect=connectionString`

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4de81-114">Часть</span><span class="sxs-lookup"><span data-stu-id="4de81-114">Part</span></span></p></th>
<th><p><span data-ttu-id="4de81-115">Описание</span><span class="sxs-lookup"><span data-stu-id="4de81-115">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4de81-116"><strong>Подключение</strong></span><span class="sxs-lookup"><span data-stu-id="4de81-116"><strong>Connect</strong></span></span></p></td>
<td><p><span data-ttu-id="4de81-117">Строковый литерал, которое указывает, это является запись строки подключения.</span><span class="sxs-lookup"><span data-stu-id="4de81-117">A literal string that indicates this is a connection string entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4de81-118"><strong><em>connectionString</em></strong></span><span class="sxs-lookup"><span data-stu-id="4de81-118"><strong><em>connectionString</em></strong></span></span></p></td>
<td><p><span data-ttu-id="4de81-119">Строка, которая заменяет строка подключения всей клиента.</span><span class="sxs-lookup"><span data-stu-id="4de81-119">A string that replaces the whole client connection string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4de81-120"><strong>Access</strong></span><span class="sxs-lookup"><span data-stu-id="4de81-120"><strong>Access</strong></span></span></p></td>
<td><p><span data-ttu-id="4de81-121">Строковый литерал, которое указывает, это является записью доступа.</span><span class="sxs-lookup"><span data-stu-id="4de81-121">A literal string that indicates this is an access entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4de81-122"><strong><em>accessRight</em></strong></span><span class="sxs-lookup"><span data-stu-id="4de81-122"><strong><em>accessRight</em></strong></span></span></p></td>
<td><p><span data-ttu-id="4de81-123">Один из следующих прав доступа.</span><span class="sxs-lookup"><span data-stu-id="4de81-123">One of the following access rights:</span></span></p>
<p></p>
<ul>
<li><p><span data-ttu-id="4de81-124"><strong>NoAccess</strong> — пользователь не может получить доступ к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="4de81-124"><strong>NoAccess</strong> — User cannot access the data source.</span></span></p></li>
<li><p><span data-ttu-id="4de81-125"><strong>ReadOnly</strong> — пользователи могут читать источника данных.</span><span class="sxs-lookup"><span data-stu-id="4de81-125"><strong>ReadOnly</strong> — User can read the data source.</span></span></p></li>
<li><p><span data-ttu-id="4de81-126"><strong>ReadWrite</strong> — пользователь может чтение или запись в источник данных.</span><span class="sxs-lookup"><span data-stu-id="4de81-126"><strong>ReadWrite</strong> — User can read or write to the data source.</span></span></p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4de81-127">Если вы хотите разрешить любые подключения (в силу, отключение обработчика поведение по умолчанию), запись доступа к набора в разделе **Подключение по умолчанию** и удалите или закомментировать любые другие **подключения** *идентификатор* раздела.</span><span class="sxs-lookup"><span data-stu-id="4de81-127">If you want to allow any connection (in effect, disabling the default handler behavior), set the access entry in the **connect default** section to , and delete or comment out any other **connect** *identifier* section.</span></span>

