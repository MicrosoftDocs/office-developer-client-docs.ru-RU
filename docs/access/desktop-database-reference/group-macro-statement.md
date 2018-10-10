---
title: Group Macro Statement
TOCTitle: Group Macro Statement
ms:assetid: 42aa4afa-ab5d-9dcc-2182-786f025e316d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192918(v=office.15)
ms:contentKeyID: 48544481
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 189744d228db0dadd3260ce77457daf8724828f8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481257"
---
# <a name="group-macro-statement"></a><span data-ttu-id="e1a8f-102">Group Macro Statement</span><span class="sxs-lookup"><span data-stu-id="e1a8f-102">Group Macro Statement</span></span>


<span data-ttu-id="e1a8f-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e1a8f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e1a8f-104">Оператор **группы** позволяет указать блок действия макроса, который можно развернуть или свернуть.</span><span class="sxs-lookup"><span data-stu-id="e1a8f-104">The **Group** statement enables you to specify a block of actions within a macro that you can expand or collapse.</span></span>

## <a name="setting"></a><span data-ttu-id="e1a8f-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="e1a8f-105">Setting</span></span>

<span data-ttu-id="e1a8f-106">Действие **группы** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="e1a8f-106">The **Group** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e1a8f-107">Argument</span><span class="sxs-lookup"><span data-stu-id="e1a8f-107">Argument</span></span></p></th>
<th><p><span data-ttu-id="e1a8f-108">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e1a8f-108">Required</span></span></p></th>
<th><p><span data-ttu-id="e1a8f-109">Описание</span><span class="sxs-lookup"><span data-stu-id="e1a8f-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e1a8f-110"><strong>Описание</strong></span><span class="sxs-lookup"><span data-stu-id="e1a8f-110"><strong>Description</strong></span></span></p></td>
<td><p><span data-ttu-id="e1a8f-111">НЕТ</span><span class="sxs-lookup"><span data-stu-id="e1a8f-111">No</span></span></p></td>
<td><p><span data-ttu-id="e1a8f-112">Строка, которая отображается как заголовок группы, когда она свернута.</span><span class="sxs-lookup"><span data-stu-id="e1a8f-112">A string that appears as the title of a group when it is collapsed.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="e1a8f-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="e1a8f-113">Remarks</span></span>

<span data-ttu-id="e1a8f-114">Оператор **группы** не определяет область макрос, который может выполняться отдельно.</span><span class="sxs-lookup"><span data-stu-id="e1a8f-114">The **Group** statment does not define a region of a macro that can be executed separately.</span></span> <span data-ttu-id="e1a8f-115">Оператор **[Вложенный макрос](submacro-macro-statement.md)** используется для определения набора действия для выполнения отдельно в окне **Конструктор макросов** .</span><span class="sxs-lookup"><span data-stu-id="e1a8f-115">Use the **[Submacro](submacro-macro-statement.md)** statment to define a set of actions to be executed separately in the **Macro Designer** window.</span></span>

