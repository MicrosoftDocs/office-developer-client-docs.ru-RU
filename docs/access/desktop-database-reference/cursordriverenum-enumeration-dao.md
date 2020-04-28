---
title: Перечисление Курсордриверенум (DAO)
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
# <a name="cursordriverenum-enumeration-dao"></a><span data-ttu-id="3aa4e-102">Перечисление Курсордриверенум (DAO)</span><span class="sxs-lookup"><span data-stu-id="3aa4e-102">CursorDriverEnum enumeration (DAO)</span></span>

<span data-ttu-id="3aa4e-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3aa4e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3aa4e-104">Указывает тип драйвера курсора.</span><span class="sxs-lookup"><span data-stu-id="3aa4e-104">Specifies the type of cursor driver.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3aa4e-105">Имя</span><span class="sxs-lookup"><span data-stu-id="3aa4e-105">Name</span></span></p></th>
<th><p><span data-ttu-id="3aa4e-106">Значение</span><span class="sxs-lookup"><span data-stu-id="3aa4e-106">Value</span></span></p></th>
<th><p><span data-ttu-id="3aa4e-107">Описание</span><span class="sxs-lookup"><span data-stu-id="3aa4e-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3aa4e-108">дбусеклиентбатчкурсор</span><span class="sxs-lookup"><span data-stu-id="3aa4e-108">dbUseClientBatchCursor</span></span></p></td>
<td><p><span data-ttu-id="3aa4e-109">4</span><span class="sxs-lookup"><span data-stu-id="3aa4e-109">3</span></span></p></td>
<td><p><span data-ttu-id="3aa4e-110">Всегда использует библиотеку курсоров FoxPro.</span><span class="sxs-lookup"><span data-stu-id="3aa4e-110">Always uses the FoxPro Cursor Library.</span></span> <span data-ttu-id="3aa4e-111">Этот параметр необходим для выполнения пакетных обновлений.</span><span class="sxs-lookup"><span data-stu-id="3aa4e-111">This option is required for performing batch updates.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3aa4e-112">дбуседефаулткурсор</span><span class="sxs-lookup"><span data-stu-id="3aa4e-112">dbUseDefaultCursor</span></span></p></td>
<td><p><span data-ttu-id="3aa4e-113">–1</span><span class="sxs-lookup"><span data-stu-id="3aa4e-113">-1</span></span></p></td>
<td><p><span data-ttu-id="3aa4e-114">Умолчани Использует курсоры на стороне сервера, если они поддерживаются сервером; в противном случае используется библиотека курсоров ODBC.</span><span class="sxs-lookup"><span data-stu-id="3aa4e-114">(Default) Uses server-side cursors if the server supports them; otherwise uses the ODBC Cursor Library.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3aa4e-115">дбусенокурсор</span><span class="sxs-lookup"><span data-stu-id="3aa4e-115">dbUseNoCursor</span></span></p></td>
<td><p><span data-ttu-id="3aa4e-116">4 </span><span class="sxs-lookup"><span data-stu-id="3aa4e-116">4</span></span></p></td>
<td><p><span data-ttu-id="3aa4e-117">Открывает все курсоры (то есть объекты <strong>Recordset</strong> ) в качестве однонаправленного типа, доступного только для чтения, с размером набора строк 1.</span><span class="sxs-lookup"><span data-stu-id="3aa4e-117">Opens all cursors (that is, <strong>Recordset</strong> objects) as forward-only type, read-only, with a rowset size of 1.</span></span> <span data-ttu-id="3aa4e-118">Также называются &quot;запросами без курсора.&quot;</span><span class="sxs-lookup"><span data-stu-id="3aa4e-118">Also known as &quot;cursorless queries.&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3aa4e-119">дбусеодбккурсор</span><span class="sxs-lookup"><span data-stu-id="3aa4e-119">dbUseODBCCursor</span></span></p></td>
<td><p><span data-ttu-id="3aa4e-120">1,1</span><span class="sxs-lookup"><span data-stu-id="3aa4e-120">1</span></span></p></td>
<td><p><span data-ttu-id="3aa4e-121">Всегда использует библиотеку курсоров ODBC.</span><span class="sxs-lookup"><span data-stu-id="3aa4e-121">Always uses the ODBC Cursor Library.</span></span> <span data-ttu-id="3aa4e-122">Этот параметр обеспечивает лучшую производительность для небольших наборов результатов, но быстро уменьшает масштаб для наборов результатов.</span><span class="sxs-lookup"><span data-stu-id="3aa4e-122">This option provides better performance for small result sets, but degrades quickly for larger result sets.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3aa4e-123">дбусесерверкурсор</span><span class="sxs-lookup"><span data-stu-id="3aa4e-123">dbUseServerCursor</span></span></p></td>
<td><p><span data-ttu-id="3aa4e-124">2</span><span class="sxs-lookup"><span data-stu-id="3aa4e-124">2</span></span></p></td>
<td><p><span data-ttu-id="3aa4e-125">Всегда использует курсоры на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="3aa4e-125">Always uses server-side cursors.</span></span> <span data-ttu-id="3aa4e-126">Для большинства операций этот вариант обеспечивает лучшую производительность, но может привести к увеличению объема сетевого трафика.</span><span class="sxs-lookup"><span data-stu-id="3aa4e-126">For most large operations this option provides better performance, but might cause more network traffic.</span></span></p></td>
</tr>
</tbody>
</table>

