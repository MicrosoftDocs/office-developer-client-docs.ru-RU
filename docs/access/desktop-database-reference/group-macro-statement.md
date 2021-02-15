---
title: Оператор макроса Group
TOCTitle: Group macro statement
ms:assetid: 42aa4afa-ab5d-9dcc-2182-786f025e316d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192918(v=office.15)
ms:contentKeyID: 48544481
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2dc25621a49d8fd23078a926d6ec6c5de54e54d9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292113"
---
# <a name="group-macro-statement"></a><span data-ttu-id="780a5-102">Оператор макроса Group</span><span class="sxs-lookup"><span data-stu-id="780a5-102">Group macro statement</span></span>


<span data-ttu-id="780a5-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="780a5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="780a5-104">Заявление **Group** позволяет указать блок действий в макросах, которые можно развернуть или свернуть.</span><span class="sxs-lookup"><span data-stu-id="780a5-104">The **Group** statement enables you to specify a block of actions within a macro that you can expand or collapse.</span></span>

## <a name="setting"></a><span data-ttu-id="780a5-105">Setting</span><span class="sxs-lookup"><span data-stu-id="780a5-105">Setting</span></span>

<span data-ttu-id="780a5-106">Действие **Group** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="780a5-106">The **Group** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="780a5-107">Аргумент</span><span class="sxs-lookup"><span data-stu-id="780a5-107">Argument</span></span></p></th>
<th><p><span data-ttu-id="780a5-108">Обязательный</span><span class="sxs-lookup"><span data-stu-id="780a5-108">Required</span></span></p></th>
<th><p><span data-ttu-id="780a5-109">Описание</span><span class="sxs-lookup"><span data-stu-id="780a5-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="780a5-110"><strong>Описание</strong></span><span class="sxs-lookup"><span data-stu-id="780a5-110"><strong>Description</strong></span></span></p></td>
<td><p><span data-ttu-id="780a5-111">Нет</span><span class="sxs-lookup"><span data-stu-id="780a5-111">No</span></span></p></td>
<td><p><span data-ttu-id="780a5-112">Строка, которая отображается в качестве заголовка группы при ее свернутом.</span><span class="sxs-lookup"><span data-stu-id="780a5-112">A string that appears as the title of a group when it is collapsed.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="780a5-113">Заметки</span><span class="sxs-lookup"><span data-stu-id="780a5-113">Remarks</span></span>

<span data-ttu-id="780a5-114">В **заявлении Group** не определяется область макроса, которую можно выполнять отдельно.</span><span class="sxs-lookup"><span data-stu-id="780a5-114">The **Group** statment does not define a region of a macro that can be executed separately.</span></span> <span data-ttu-id="780a5-115">Используйте **[подмакрой](submacro-macro-statement.md)** для определения набора действий, которые необходимо выполнять отдельно в окне конструктора **макроса.**</span><span class="sxs-lookup"><span data-stu-id="780a5-115">Use the **[Submacro](submacro-macro-statement.md)** statment to define a set of actions to be executed separately in the **Macro Designer** window.</span></span>

