---
title: Understanding the Customization File
TOCTitle: Understanding the Customization File
ms:assetid: 98fd5ec1-d5bd-cdd2-5eb5-9a1682fbed79
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249686(v=office.15)
ms:contentKeyID: 48546507
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b977fc4273068ac52efe8960761a9e28a6234e2e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314072"
---
# <a name="understanding-the-customization-file"></a><span data-ttu-id="c8654-102">Understanding the Customization File</span><span class="sxs-lookup"><span data-stu-id="c8654-102">Understanding the Customization File</span></span>


<span data-ttu-id="c8654-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c8654-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c8654-104">Каждый загон раздела в файле настройки состоит из квадратных скобок ( **\[\]** ), содержащих тип и параметр.</span><span class="sxs-lookup"><span data-stu-id="c8654-104">Each section header in the customization file consists of square brackets (**\[\]**) containing a type and parameter.</span></span> <span data-ttu-id="c8654-105">Четыре типа разделов обозначены литеральными строками **подключения,** **sql,** **списком пользователей** или **журналами.**</span><span class="sxs-lookup"><span data-stu-id="c8654-105">The four section types are indicated by the literal strings **connect**, **sql**, **userlist**, or **logs**.</span></span> <span data-ttu-id="c8654-106">Параметром является литеральная строка, значение по умолчанию, указанный пользователем идентификатор или ничего.</span><span class="sxs-lookup"><span data-stu-id="c8654-106">The parameter is the literal string, the default, a user-specified identifier, or nothing.</span></span>

<span data-ttu-id="c8654-107">Поэтому каждый раздел помечен одним из следующих разделов:</span><span class="sxs-lookup"><span data-stu-id="c8654-107">Therefore, each section is marked with one of the following section headers:</span></span>

```text 
 
[ connect   default     ]
[ connect   identifier  ]
[ sql       default     ]
[ sql       identifier  ]
[ userlist  identifier  ]
[ logs                  ]
```

<span data-ttu-id="c8654-108">В заглавных разделах есть следующие части.</span><span class="sxs-lookup"><span data-stu-id="c8654-108">The section headers have the following parts.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c8654-109">Часть</span><span class="sxs-lookup"><span data-stu-id="c8654-109">Part</span></span></p></th>
<th><p><span data-ttu-id="c8654-110">Описание</span><span class="sxs-lookup"><span data-stu-id="c8654-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c8654-111"><strong>connect</strong></span><span class="sxs-lookup"><span data-stu-id="c8654-111"><strong>connect</strong></span></span></p></td>
<td><p><span data-ttu-id="c8654-112">Строка литералов, которая изменяет строку подключения.</span><span class="sxs-lookup"><span data-stu-id="c8654-112">A literal string that modifies a connection string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8654-113"><strong>sql</strong></span><span class="sxs-lookup"><span data-stu-id="c8654-113"><strong>sql</strong></span></span></p></td>
<td><p><span data-ttu-id="c8654-114">Строка литералов, которая изменяет строку команды.</span><span class="sxs-lookup"><span data-stu-id="c8654-114">A literal string that modifies a command string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8654-115"><strong>userlist</strong></span><span class="sxs-lookup"><span data-stu-id="c8654-115"><strong>userlist</strong></span></span></p></td>
<td><p><span data-ttu-id="c8654-116">Литеральная строка, которая изменяет права доступа определенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="c8654-116">A literal string that modifies the access rights of a specific user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8654-117"><strong>logs</strong></span><span class="sxs-lookup"><span data-stu-id="c8654-117"><strong>logs</strong></span></span></p></td>
<td><p><span data-ttu-id="c8654-118">Строка литералов, которая указывает операционные ошибки в файле журнала.</span><span class="sxs-lookup"><span data-stu-id="c8654-118">A literal string that specifies a log file recording operational errors.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8654-119"><strong>default</strong></span><span class="sxs-lookup"><span data-stu-id="c8654-119"><strong>default</strong></span></span></p></td>
<td><p><span data-ttu-id="c8654-120">Строка литералов, которая используется, если идентификатор не указан или не найден.</span><span class="sxs-lookup"><span data-stu-id="c8654-120">A literal string that is used if no identifier is specified or found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8654-121"><em>identifier</em></span><span class="sxs-lookup"><span data-stu-id="c8654-121"><em>identifier</em></span></span></p></td>
<td><p><span data-ttu-id="c8654-122">Строка, которая соответствует строке в <strong>строке подключения</strong> или <strong>команды.</strong></span><span class="sxs-lookup"><span data-stu-id="c8654-122">A string that matches a string in the <strong>connect</strong> or <strong>command</strong> string.</span></span></p>
<p></p>
<ul>
<li><p><span data-ttu-id="c8654-123">Используйте этот раздел, если заглавная строка раздела содержит <strong>подключение,</strong> а строка идентификатора находится в строке подключения.</span><span class="sxs-lookup"><span data-stu-id="c8654-123">Use this section if the section header contains <strong>connect</strong> and the identifier string is found in the connection string.</span></span></p></li>
<li><p><span data-ttu-id="c8654-124">Используйте этот раздел, если заголовка раздела содержит <strong>sql,</strong> а строка идентификатора находится в строке команды.</span><span class="sxs-lookup"><span data-stu-id="c8654-124">Use this section if the section header contains <strong>sql</strong> and the identifier string is found in the command string.</span></span></p></li>
<li><p><span data-ttu-id="c8654-125">Используйте этот раздел, если заглавная строка раздела содержит <strong>список</strong> пользователей, а строка идентификатора соответствует <strong>идентификатору</strong> раздела подключения.</span><span class="sxs-lookup"><span data-stu-id="c8654-125">Use this section if the section header contains <strong>userlist</strong> and the identifier string matches a <strong>connect</strong> section identifier.</span></span></p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c8654-126">**DataFactory** вызывает обработчик, передавая параметры клиента.</span><span class="sxs-lookup"><span data-stu-id="c8654-126">The **DataFactory** calls the handler, passing client parameters.</span></span> <span data-ttu-id="c8654-127">Обработчик ищет целые строки в параметрах клиента, соответствующие идентификаторам в соответствующих разделах.</span><span class="sxs-lookup"><span data-stu-id="c8654-127">The handler searches for whole strings in the client parameters that match identifiers in the appropriate section headers.</span></span> <span data-ttu-id="c8654-128">Если найдено совпадение, содержимое этого раздела применяется к параметру клиента.</span><span class="sxs-lookup"><span data-stu-id="c8654-128">If a match is found, the contents of that section are applied to the client parameter.</span></span>

<span data-ttu-id="c8654-129">Конкретный раздел используется при следующих обстоятельствах:</span><span class="sxs-lookup"><span data-stu-id="c8654-129">A particular section is used under the following circumstances:</span></span>

  - <span data-ttu-id="c8654-130">Раздел **подключения** используется, если значение части ключевого слова строки подключения клиента, "\* Data  *Source=\*\*\*value",* соответствует идентификатору раздела *подключения.*</span><span class="sxs-lookup"><span data-stu-id="c8654-130">A **connect** section is used if the value part of the client connect string keyword, "\**Data Source=\*\*\*value*", matches a **connect** section identifier *.*</span></span>

  - <span data-ttu-id="c8654-131">Раздел **sql** используется, если строка команд клиента содержит строку, которая соответствует идентификатору раздела **sql.**</span><span class="sxs-lookup"><span data-stu-id="c8654-131">An **sql** section is used if the client command string contains a string that matches an **sql** section identifier.</span></span>

  - <span data-ttu-id="c8654-132">Если **нет** совпадающих идентификаторов, используется раздел подключения или **sql** с параметром по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c8654-132">A **connect** or **sql** section with a default parameter is used if there is no matching identifier.</span></span>

  - <span data-ttu-id="c8654-133">Раздел **списка пользователей** используется, если идентификатор раздела **списка** пользователей совпадает с **идентификатором раздела** подключения.</span><span class="sxs-lookup"><span data-stu-id="c8654-133">A **userlist** section is used if the **userlist** section identifier matches a **connect** section identifier.</span></span> <span data-ttu-id="c8654-134">При совпадении содержимое раздела списка  пользователей применяется к подключению, управляемому разделом **подключения.**</span><span class="sxs-lookup"><span data-stu-id="c8654-134">If there is a match, the contents of the **userlist** section are applied to the connection governed by the **connect** section.</span></span>

  - <span data-ttu-id="c8654-135">Если строка в строке подключения или команды не  соответствует идентификатору в заголовке  раздела подключения или **sql** и нет заголовка раздела подключения или **sql** с параметром по умолчанию, то строка клиента используется без изменений.</span><span class="sxs-lookup"><span data-stu-id="c8654-135">If the string in a connection or command string does not match the identifier in any **connect** or **sql** section header, and there is no **connect** or **sql** section header with a default parameter, then the client string is used without modification.</span></span>

  - <span data-ttu-id="c8654-136">Раздел **"Журналы"** используется при работе **DataFactory.**</span><span class="sxs-lookup"><span data-stu-id="c8654-136">The **logs** section is used whenever the **DataFactory** is in operation.</span></span>

