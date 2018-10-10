---
title: CursorDriverEnum Enumeration (DAO)
TOCTitle: CursorDriverEnum Enumeration
ms:assetid: d0312ece-c30a-7d61-d5f3-75edf0d0afc8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834707(v=office.15)
ms:contentKeyID: 48547832
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bcce8eefad7fcad7dee7e46274ffc45125dc36c9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482127"
---
# <a name="cursordriverenum-enumeration-dao"></a><span data-ttu-id="957df-102">CursorDriverEnum Enumeration (DAO)</span><span class="sxs-lookup"><span data-stu-id="957df-102">CursorDriverEnum Enumeration (DAO)</span></span>


<span data-ttu-id="957df-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="957df-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="957df-104">Указывает тип драйвера курсора.</span><span class="sxs-lookup"><span data-stu-id="957df-104">Specifies the type of cursor driver.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="957df-105">Имя</span><span class="sxs-lookup"><span data-stu-id="957df-105">Name</span></span></p></th>
<th><p><span data-ttu-id="957df-106">Значение</span><span class="sxs-lookup"><span data-stu-id="957df-106">Value</span></span></p></th>
<th><p><span data-ttu-id="957df-107">Описание</span><span class="sxs-lookup"><span data-stu-id="957df-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="957df-108">dbUseClientBatchCursor</span><span class="sxs-lookup"><span data-stu-id="957df-108">dbUseClientBatchCursor</span></span></p></td>
<td><p><span data-ttu-id="957df-109">3</span><span class="sxs-lookup"><span data-stu-id="957df-109">3</span></span></p></td>
<td><p><span data-ttu-id="957df-110">Всегда использует библиотеку FoxPro курсора.</span><span class="sxs-lookup"><span data-stu-id="957df-110">Always uses the FoxPro Cursor Library.</span></span> <span data-ttu-id="957df-111">Этот параметр является обязательным для выполнения пакета обновлений.</span><span class="sxs-lookup"><span data-stu-id="957df-111">This option is required for performing batch updates.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="957df-112">dbUseDefaultCursor</span><span class="sxs-lookup"><span data-stu-id="957df-112">dbUseDefaultCursor</span></span></p></td>
<td><p><span data-ttu-id="957df-113">-1</span><span class="sxs-lookup"><span data-stu-id="957df-113">-1</span></span></p></td>
<td><p><span data-ttu-id="957df-114">(По умолчанию) Использует записей на стороне сервера, если поддерживается сервером в противном случае используется библиотека курсора ODBC.</span><span class="sxs-lookup"><span data-stu-id="957df-114">(Default) Uses server-side cursors if the server supports them; otherwise uses the ODBC Cursor Library.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="957df-115">dbUseNoCursor</span><span class="sxs-lookup"><span data-stu-id="957df-115">dbUseNoCursor</span></span></p></td>
<td><p><span data-ttu-id="957df-116">4</span><span class="sxs-lookup"><span data-stu-id="957df-116">4</span></span></p></td>
<td><p><span data-ttu-id="957df-117">Открывает все курсоры (то есть, объекты <strong>набора записей</strong> ) в качестве типа, последовательного доступа только для чтения, имеющее размер строк 1.</span><span class="sxs-lookup"><span data-stu-id="957df-117">Opens all cursors (that is, <strong>Recordset</strong> objects) as forward-only type, read-only, with a rowset size of 1.</span></span> <span data-ttu-id="957df-118">Также известной как &quot;cursorless запросов.&quot;</span><span class="sxs-lookup"><span data-stu-id="957df-118">Also known as &quot;cursorless queries.&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="957df-119">dbUseODBCCursor</span><span class="sxs-lookup"><span data-stu-id="957df-119">dbUseODBCCursor</span></span></p></td>
<td><p><span data-ttu-id="957df-120">1</span><span class="sxs-lookup"><span data-stu-id="957df-120">1</span></span></p></td>
<td><p><span data-ttu-id="957df-121">Всегда используется библиотека курсора ODBC.</span><span class="sxs-lookup"><span data-stu-id="957df-121">Always uses the ODBC Cursor Library.</span></span> <span data-ttu-id="957df-122">Этот параметр обеспечивает более высокую производительность на небольшой результирующий набор, но снижает быстро для больших наборов результатов.</span><span class="sxs-lookup"><span data-stu-id="957df-122">This option provides better performance for small result sets, but degrades quickly for larger result sets.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="957df-123">dbUseServerCursor</span><span class="sxs-lookup"><span data-stu-id="957df-123">dbUseServerCursor</span></span></p></td>
<td><p><span data-ttu-id="957df-124">2</span><span class="sxs-lookup"><span data-stu-id="957df-124">2</span></span></p></td>
<td><p><span data-ttu-id="957df-125">Всегда использует записей на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="957df-125">Always uses server-side cursors.</span></span> <span data-ttu-id="957df-126">Для самых больших операций этого параметра обеспечивает более высокую производительность, но может привести к более сетевого трафика.</span><span class="sxs-lookup"><span data-stu-id="957df-126">For most large operations this option provides better performance, but might cause more network traffic.</span></span></p></td>
</tr>
</tbody>
</table>

