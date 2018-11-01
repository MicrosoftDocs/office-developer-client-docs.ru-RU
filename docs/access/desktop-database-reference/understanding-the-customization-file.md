---
title: Общие сведения о файле настройки
TOCTitle: Understanding the Customization File
ms:assetid: 98fd5ec1-d5bd-cdd2-5eb5-9a1682fbed79
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249686(v=office.15)
ms:contentKeyID: 48546507
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5c764c543c3d8734a47927d702daca1552e497b6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879475"
---
# <a name="understanding-the-customization-file"></a><span data-ttu-id="174a6-102">Общие сведения о файле настройки</span><span class="sxs-lookup"><span data-stu-id="174a6-102">Understanding the Customization File</span></span>


<span data-ttu-id="174a6-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="174a6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="174a6-104">Каждый раздел заголовка в файле параметров состоит из квадратные скобки (**\[**) содержит тип и параметр.</span><span class="sxs-lookup"><span data-stu-id="174a6-104">Each section header in the customization file consists of square brackets (**\[\]**) containing a type and parameter.</span></span> <span data-ttu-id="174a6-105">Типы четыре раздела указанный в параметре буквенные строки **подключения**, **sql**, **userlist**или **Журналы**.</span><span class="sxs-lookup"><span data-stu-id="174a6-105">The four section types are indicated by the literal strings **connect**, **sql**, **userlist**, or **logs**.</span></span> <span data-ttu-id="174a6-106">Параметр — это строковый литерал, по умолчанию, определенные пользователем идентификатор или ничего.</span><span class="sxs-lookup"><span data-stu-id="174a6-106">The parameter is the literal string, the default, a user-specified identifier, or nothing.</span></span>

<span data-ttu-id="174a6-107">Таким образом каждый раздел помечен с одним из следующих разделов:</span><span class="sxs-lookup"><span data-stu-id="174a6-107">Therefore, each section is marked with one of the following section headers:</span></span>

```text 
 
[ connect   default     ]
[ connect   identifier  ]
[ sql       default     ]
[ sql       identifier  ]
[ userlist  identifier  ]
[ logs                  ]
```

<span data-ttu-id="174a6-108">Заголовки разделов состоят из следующих частей.</span><span class="sxs-lookup"><span data-stu-id="174a6-108">The section headers have the following parts.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="174a6-109">Часть</span><span class="sxs-lookup"><span data-stu-id="174a6-109">Part</span></span></p></th>
<th><p><span data-ttu-id="174a6-110">Описание</span><span class="sxs-lookup"><span data-stu-id="174a6-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="174a6-111"><strong>connect</strong></span><span class="sxs-lookup"><span data-stu-id="174a6-111"><strong>connect</strong></span></span></p></td>
<td><p><span data-ttu-id="174a6-112">Строковый литерал, который изменяет строку подключения.</span><span class="sxs-lookup"><span data-stu-id="174a6-112">A literal string that modifies a connection string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="174a6-113"><strong>SQL</strong></span><span class="sxs-lookup"><span data-stu-id="174a6-113"><strong>sql</strong></span></span></p></td>
<td><p><span data-ttu-id="174a6-114">Строковый литерал, который изменяет командной строки.</span><span class="sxs-lookup"><span data-stu-id="174a6-114">A literal string that modifies a command string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="174a6-115"><strong>USERLIST</strong></span><span class="sxs-lookup"><span data-stu-id="174a6-115"><strong>userlist</strong></span></span></p></td>
<td><p><span data-ttu-id="174a6-116">Строковый литерал, обеспечивающий изменение прав доступа для определенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="174a6-116">A literal string that modifies the access rights of a specific user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="174a6-117"><strong>журналы</strong></span><span class="sxs-lookup"><span data-stu-id="174a6-117"><strong>logs</strong></span></span></p></td>
<td><p><span data-ttu-id="174a6-118">Строковый литерал, указывающее действующие ошибки записи файла журнала.</span><span class="sxs-lookup"><span data-stu-id="174a6-118">A literal string that specifies a log file recording operational errors.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="174a6-119"><strong>default</strong></span><span class="sxs-lookup"><span data-stu-id="174a6-119"><strong>default</strong></span></span></p></td>
<td><p><span data-ttu-id="174a6-120">Строковый литерал, который используется, если идентификатор не указан или найти.</span><span class="sxs-lookup"><span data-stu-id="174a6-120">A literal string that is used if no identifier is specified or found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="174a6-121"><em>Идентификатор</em></span><span class="sxs-lookup"><span data-stu-id="174a6-121"><em>identifier</em></span></span></p></td>
<td><p><span data-ttu-id="174a6-122">Строка, которая соответствует является строкой <strong>подключения</strong> или <strong>Командная</strong> строка.</span><span class="sxs-lookup"><span data-stu-id="174a6-122">A string that matches a string in the <strong>connect</strong> or <strong>command</strong> string.</span></span></p>
<p></p>
<ul>
<li><p><span data-ttu-id="174a6-123">Используйте этот раздел, если заголовок раздела содержит <strong>подключение</strong> и строка идентификатора найдена в строке подключения.</span><span class="sxs-lookup"><span data-stu-id="174a6-123">Use this section if the section header contains <strong>connect</strong> and the identifier string is found in the connection string.</span></span></p></li>
<li><p><span data-ttu-id="174a6-124">Используйте этот раздел, если заголовок раздела содержит <strong>sql</strong> и строка идентификатора найдена в командной строке.</span><span class="sxs-lookup"><span data-stu-id="174a6-124">Use this section if the section header contains <strong>sql</strong> and the identifier string is found in the command string.</span></span></p></li>
<li><p><span data-ttu-id="174a6-125">Используйте этот раздел, если заголовок раздела содержит <strong>userlist</strong> и строка идентификатора сопоставляет идентификатор раздела <strong>подключение</strong> .</span><span class="sxs-lookup"><span data-stu-id="174a6-125">Use this section if the section header contains <strong>userlist</strong> and the identifier string matches a <strong>connect</strong> section identifier.</span></span></p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="174a6-126">**DataFactory** вызывает обработчик, передача параметров клиента.</span><span class="sxs-lookup"><span data-stu-id="174a6-126">The **DataFactory** calls the handler, passing client parameters.</span></span> <span data-ttu-id="174a6-127">Обработчик выполняет поиск полных строк в параметрах клиента, соответствующие идентификаторы в соответствующий раздел заголовков.</span><span class="sxs-lookup"><span data-stu-id="174a6-127">The handler searches for whole strings in the client parameters that match identifiers in the appropriate section headers.</span></span> <span data-ttu-id="174a6-128">Если совпадение найдено, содержимое этого раздела применяются к параметра клиента.</span><span class="sxs-lookup"><span data-stu-id="174a6-128">If a match is found, the contents of that section are applied to the client parameter.</span></span>

<span data-ttu-id="174a6-129">Конкретный раздел используется в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="174a6-129">A particular section is used under the following circumstances:</span></span>

  - <span data-ttu-id="174a6-130">Раздел **подключение** используется, если значение частью клиента подключиться ключевое слово string «\**источник данных = \*\*\* значение*«, соответствует **подключения** идентификатор раздела *.*</span><span class="sxs-lookup"><span data-stu-id="174a6-130">A **connect** section is used if the value part of the client connect string keyword, "\**Data Source=\*\*\*value*", matches a **connect** section identifier *.*</span></span>

  - <span data-ttu-id="174a6-131">Раздел **sql** используется, если строка команды клиента содержит строку, которая сопоставляет идентификатор раздела **sql** .</span><span class="sxs-lookup"><span data-stu-id="174a6-131">An **sql** section is used if the client command string contains a string that matches an **sql** section identifier.</span></span>

  - <span data-ttu-id="174a6-132">Раздел **подключение** или **sql** с помощью параметра по умолчанию используется, если соответствующий идентификатор отсутствует.</span><span class="sxs-lookup"><span data-stu-id="174a6-132">A **connect** or **sql** section with a default parameter is used if there is no matching identifier.</span></span>

  - <span data-ttu-id="174a6-133">Раздел **userlist** используется, если идентификатор раздела **userlist** совпадает с идентификатором **подключения** раздела.</span><span class="sxs-lookup"><span data-stu-id="174a6-133">A **userlist** section is used if the **userlist** section identifier matches a **connect** section identifier.</span></span> <span data-ttu-id="174a6-134">Если совпадение, содержимое раздела **userlist** применяются к подключения, в соответствии с разделом **подключиться** .</span><span class="sxs-lookup"><span data-stu-id="174a6-134">If there is a match, the contents of the **userlist** section are applied to the connection governed by the **connect** section.</span></span>

  - <span data-ttu-id="174a6-135">Если строка в подключении или командной строки не соответствует идентификатор в заголовок раздела любого **подключения** или **sql** , и нет заголовка без **подключения** или **sql** с помощью параметра по умолчанию, то клиент используется строка без изменение.</span><span class="sxs-lookup"><span data-stu-id="174a6-135">If the string in a connection or command string does not match the identifier in any **connect** or **sql** section header, and there is no **connect** or **sql** section header with a default parameter, then the client string is used without modification.</span></span>

  - <span data-ttu-id="174a6-136">В разделе **Журналы** используется всякий раз, когда **DataFactory** в операции.</span><span class="sxs-lookup"><span data-stu-id="174a6-136">The **logs** section is used whenever the **DataFactory** is in operation.</span></span>

