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
# <a name="understanding-the-customization-file"></a><span data-ttu-id="72b3f-102">Understanding the Customization File</span><span class="sxs-lookup"><span data-stu-id="72b3f-102">Understanding the Customization File</span></span>


<span data-ttu-id="72b3f-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="72b3f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="72b3f-104">Каждый заголовок раздела в файле настройки состоит из квадратных скобок (**\[**), содержащих тип и параметр.</span><span class="sxs-lookup"><span data-stu-id="72b3f-104">Each section header in the customization file consists of square brackets (**\[\]**) containing a type and parameter.</span></span> <span data-ttu-id="72b3f-105">Четыре типа разделов указываются с помощью строковых литералов **Connect**, **SQL**, **USERLIST**или **logs**.</span><span class="sxs-lookup"><span data-stu-id="72b3f-105">The four section types are indicated by the literal strings **connect**, **sql**, **userlist**, or **logs**.</span></span> <span data-ttu-id="72b3f-106">Параметр — это строка литерала, значение по умолчанию, идентификатор, заданный пользователем, или значение Nothing.</span><span class="sxs-lookup"><span data-stu-id="72b3f-106">The parameter is the literal string, the default, a user-specified identifier, or nothing.</span></span>

<span data-ttu-id="72b3f-107">Таким образом, каждый раздел помечается одним из следующих заголовков разделов:</span><span class="sxs-lookup"><span data-stu-id="72b3f-107">Therefore, each section is marked with one of the following section headers:</span></span>

```text 
 
[ connect   default     ]
[ connect   identifier  ]
[ sql       default     ]
[ sql       identifier  ]
[ userlist  identifier  ]
[ logs                  ]
```

<span data-ttu-id="72b3f-108">Заголовки разделов содержат следующие части.</span><span class="sxs-lookup"><span data-stu-id="72b3f-108">The section headers have the following parts.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="72b3f-109">Часть</span><span class="sxs-lookup"><span data-stu-id="72b3f-109">Part</span></span></p></th>
<th><p><span data-ttu-id="72b3f-110">Описание</span><span class="sxs-lookup"><span data-stu-id="72b3f-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="72b3f-111"><strong>Connect</strong></span><span class="sxs-lookup"><span data-stu-id="72b3f-111"><strong>connect</strong></span></span></p></td>
<td><p><span data-ttu-id="72b3f-112">Строка литерала, которая изменяет строку подключения.</span><span class="sxs-lookup"><span data-stu-id="72b3f-112">A literal string that modifies a connection string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72b3f-113"><strong>SQL</strong></span><span class="sxs-lookup"><span data-stu-id="72b3f-113"><strong>sql</strong></span></span></p></td>
<td><p><span data-ttu-id="72b3f-114">Строка литерала, которая изменяет командную строку.</span><span class="sxs-lookup"><span data-stu-id="72b3f-114">A literal string that modifies a command string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72b3f-115"><strong>USERLIST</strong></span><span class="sxs-lookup"><span data-stu-id="72b3f-115"><strong>userlist</strong></span></span></p></td>
<td><p><span data-ttu-id="72b3f-116">Строка литерала, которая изменяет права доступа определенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="72b3f-116">A literal string that modifies the access rights of a specific user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72b3f-117"><strong>входящий</strong></span><span class="sxs-lookup"><span data-stu-id="72b3f-117"><strong>logs</strong></span></span></p></td>
<td><p><span data-ttu-id="72b3f-118">Строка литерала, указывающая на рабочие ошибки записи файла журнала.</span><span class="sxs-lookup"><span data-stu-id="72b3f-118">A literal string that specifies a log file recording operational errors.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72b3f-119"><strong>default</strong></span><span class="sxs-lookup"><span data-stu-id="72b3f-119"><strong>default</strong></span></span></p></td>
<td><p><span data-ttu-id="72b3f-120">Строка литерала, которая используется, если идентификатор не указан или не найден.</span><span class="sxs-lookup"><span data-stu-id="72b3f-120">A literal string that is used if no identifier is specified or found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72b3f-121"><em>идентификацион</em></span><span class="sxs-lookup"><span data-stu-id="72b3f-121"><em>identifier</em></span></span></p></td>
<td><p><span data-ttu-id="72b3f-122">Строка, соответствующая строке в строке <strong>подключения</strong> или <strong>командной</strong> строке.</span><span class="sxs-lookup"><span data-stu-id="72b3f-122">A string that matches a string in the <strong>connect</strong> or <strong>command</strong> string.</span></span></p>
<p></p>
<ul>
<li><p><span data-ttu-id="72b3f-123">Используйте этот раздел, если заголовок раздела содержит <strong>Connect</strong> , а строка идентификатора найдена в строке подключения.</span><span class="sxs-lookup"><span data-stu-id="72b3f-123">Use this section if the section header contains <strong>connect</strong> and the identifier string is found in the connection string.</span></span></p></li>
<li><p><span data-ttu-id="72b3f-124">Используйте этот раздел, если заголовок раздела содержит <strong>SQL</strong> , а строка идентификатора найдена в командной строке.</span><span class="sxs-lookup"><span data-stu-id="72b3f-124">Use this section if the section header contains <strong>sql</strong> and the identifier string is found in the command string.</span></span></p></li>
<li><p><span data-ttu-id="72b3f-125">Используйте этот раздел, если заголовок раздела содержит <strong>USERLIST</strong> , а строка идентификатора соответствует идентификатору раздела <strong>подключения</strong> .</span><span class="sxs-lookup"><span data-stu-id="72b3f-125">Use this section if the section header contains <strong>userlist</strong> and the identifier string matches a <strong>connect</strong> section identifier.</span></span></p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="72b3f-126">Этот **факт** вызывает обработчик, передавая параметры клиента.</span><span class="sxs-lookup"><span data-stu-id="72b3f-126">The **DataFactory** calls the handler, passing client parameters.</span></span> <span data-ttu-id="72b3f-127">Обработчик ищет все строки в параметрах клиента, которые совпадают идентификаторы в соответствующих заголовках разделов.</span><span class="sxs-lookup"><span data-stu-id="72b3f-127">The handler searches for whole strings in the client parameters that match identifiers in the appropriate section headers.</span></span> <span data-ttu-id="72b3f-128">Если найдено сравнение, содержимое этого раздела применяется к параметру клиента.</span><span class="sxs-lookup"><span data-stu-id="72b3f-128">If a match is found, the contents of that section are applied to the client parameter.</span></span>

<span data-ttu-id="72b3f-129">Определенный раздел используется в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="72b3f-129">A particular section is used under the following circumstances:</span></span>

  - <span data-ttu-id="72b3f-130">Раздел **Connect** используется, если часть значения ключевого слова Connect Client Connect, "\**Data Source = \* \* \* value*", соответствует идентификатору раздела **Connect** *.*</span><span class="sxs-lookup"><span data-stu-id="72b3f-130">A **connect** section is used if the value part of the client connect string keyword, "\**Data Source=\*\*\*value*", matches a **connect** section identifier *.*</span></span>

  - <span data-ttu-id="72b3f-131">Раздел **SQL** используется, если строка команды клиента содержит строку, которая соответствует идентификатору раздела **SQL** .</span><span class="sxs-lookup"><span data-stu-id="72b3f-131">An **sql** section is used if the client command string contains a string that matches an **sql** section identifier.</span></span>

  - <span data-ttu-id="72b3f-132">Раздел **Connect** или **SQL** с параметром по умолчанию используется, если не существует совпадающего идентификатора.</span><span class="sxs-lookup"><span data-stu-id="72b3f-132">A **connect** or **sql** section with a default parameter is used if there is no matching identifier.</span></span>

  - <span data-ttu-id="72b3f-133">Раздел **USERLIST** используется, если идентификатор раздела **USERLIST** соответствует идентификатору раздела **Connect** .</span><span class="sxs-lookup"><span data-stu-id="72b3f-133">A **userlist** section is used if the **userlist** section identifier matches a **connect** section identifier.</span></span> <span data-ttu-id="72b3f-134">Если найдено соответствующее значение, содержимое раздела **USERLIST** применяется к подключению, управляемому с помощью раздела **Connect** .</span><span class="sxs-lookup"><span data-stu-id="72b3f-134">If there is a match, the contents of the **userlist** section are applied to the connection governed by the **connect** section.</span></span>

  - <span data-ttu-id="72b3f-135">Если строка в соединении или в командной строке не совпадают с идентификатором в любом заголовке раздела **подключения** или **SQL** , а отсутствует параметр **подключения** или заголовок раздела **SQL** с параметром по умолчанию, то клиентская строка используется без изменений.</span><span class="sxs-lookup"><span data-stu-id="72b3f-135">If the string in a connection or command string does not match the identifier in any **connect** or **sql** section header, and there is no **connect** or **sql** section header with a default parameter, then the client string is used without modification.</span></span>

  - <span data-ttu-id="72b3f-136">Раздел **logs** используется при работе с **фактом** .</span><span class="sxs-lookup"><span data-stu-id="72b3f-136">The **logs** section is used whenever the **DataFactory** is in operation.</span></span>

