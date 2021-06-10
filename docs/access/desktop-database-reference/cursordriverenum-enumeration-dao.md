---
title: Enumeration CursorDriverEnum (DAO)
TOCTitle: CursorDriverEnum enumeration
ms:assetid: d0312ece-c30a-7d61-d5f3-75edf0d0afc8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834707(v=office.15)
ms:contentKeyID: 48547832
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2f2bf52943a84d6f2e60891d63810bc0bbb6ecb3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295249"
---
# <a name="cursordriverenum-enumeration-dao"></a><span data-ttu-id="b0b8f-102">Enumeration CursorDriverEnum (DAO)</span><span class="sxs-lookup"><span data-stu-id="b0b8f-102">CursorDriverEnum enumeration (DAO)</span></span>

<span data-ttu-id="b0b8f-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b0b8f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b0b8f-104">Указывает тип драйвера курсора.</span><span class="sxs-lookup"><span data-stu-id="b0b8f-104">Specifies the type of cursor driver.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b0b8f-105">Имя</span><span class="sxs-lookup"><span data-stu-id="b0b8f-105">Name</span></span></p></th>
<th><p><span data-ttu-id="b0b8f-106">Значение</span><span class="sxs-lookup"><span data-stu-id="b0b8f-106">Value</span></span></p></th>
<th><p><span data-ttu-id="b0b8f-107">Описание</span><span class="sxs-lookup"><span data-stu-id="b0b8f-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b0b8f-108">dbUseClientBatchCursor</span><span class="sxs-lookup"><span data-stu-id="b0b8f-108">dbUseClientBatchCursor</span></span></p></td>
<td><p><span data-ttu-id="b0b8f-109">3</span><span class="sxs-lookup"><span data-stu-id="b0b8f-109">3</span></span></p></td>
<td><p><span data-ttu-id="b0b8f-110">Всегда использует библиотеку курсоров FoxPro.</span><span class="sxs-lookup"><span data-stu-id="b0b8f-110">Always uses the FoxPro Cursor Library.</span></span> <span data-ttu-id="b0b8f-111">Этот параметр необходим для выполнения пакетных обновлений.</span><span class="sxs-lookup"><span data-stu-id="b0b8f-111">This option is required for performing batch updates.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0b8f-112">dbUseDefaultCursor</span><span class="sxs-lookup"><span data-stu-id="b0b8f-112">dbUseDefaultCursor</span></span></p></td>
<td><p><span data-ttu-id="b0b8f-113">–1</span><span class="sxs-lookup"><span data-stu-id="b0b8f-113">-1</span></span></p></td>
<td><p><span data-ttu-id="b0b8f-114">(По умолчанию) Использует курсоры на стороне сервера, если сервер поддерживает их; в противном случае используется библиотека курсоров ODBC.</span><span class="sxs-lookup"><span data-stu-id="b0b8f-114">(Default) Uses server-side cursors if the server supports them; otherwise uses the ODBC Cursor Library.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0b8f-115">dbUseNoCursor</span><span class="sxs-lookup"><span data-stu-id="b0b8f-115">dbUseNoCursor</span></span></p></td>
<td><p><span data-ttu-id="b0b8f-116">4 </span><span class="sxs-lookup"><span data-stu-id="b0b8f-116">4</span></span></p></td>
<td><p><span data-ttu-id="b0b8f-117">Открывает все курсоры (то есть <strong>объекты Recordset)</strong> как тип только для чтения, только для чтения, с размером строки 1.</span><span class="sxs-lookup"><span data-stu-id="b0b8f-117">Opens all cursors (that is, <strong>Recordset</strong> objects) as forward-only type, read-only, with a rowset size of 1.</span></span> <span data-ttu-id="b0b8f-118">Также известен как &quot; запросы без курсоров.&quot;</span><span class="sxs-lookup"><span data-stu-id="b0b8f-118">Also known as &quot;cursorless queries.&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0b8f-119">dbUseODBCCursor</span><span class="sxs-lookup"><span data-stu-id="b0b8f-119">dbUseODBCCursor</span></span></p></td>
<td><p><span data-ttu-id="b0b8f-120">1</span><span class="sxs-lookup"><span data-stu-id="b0b8f-120">1</span></span></p></td>
<td><p><span data-ttu-id="b0b8f-121">Всегда использует библиотеку курсоров ODBC.</span><span class="sxs-lookup"><span data-stu-id="b0b8f-121">Always uses the ODBC Cursor Library.</span></span> <span data-ttu-id="b0b8f-122">Этот параметр обеспечивает лучшую производительность для небольших наборов результатов, но быстро снижается для больших наборов результатов.</span><span class="sxs-lookup"><span data-stu-id="b0b8f-122">This option provides better performance for small result sets, but degrades quickly for larger result sets.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0b8f-123">dbUseServerCursor</span><span class="sxs-lookup"><span data-stu-id="b0b8f-123">dbUseServerCursor</span></span></p></td>
<td><p><span data-ttu-id="b0b8f-124">2</span><span class="sxs-lookup"><span data-stu-id="b0b8f-124">2</span></span></p></td>
<td><p><span data-ttu-id="b0b8f-125">Всегда использует курсоры на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="b0b8f-125">Always uses server-side cursors.</span></span> <span data-ttu-id="b0b8f-126">Для большинства крупных операций этот параметр обеспечивает лучшую производительность, но может привести к большему сетевому трафику.</span><span class="sxs-lookup"><span data-stu-id="b0b8f-126">For most large operations this option provides better performance, but might cause more network traffic.</span></span></p></td>
</tr>
</tbody>
</table>

