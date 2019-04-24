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
# <a name="group-macro-statement"></a><span data-ttu-id="92e2e-102">Оператор макроса Group</span><span class="sxs-lookup"><span data-stu-id="92e2e-102">Group macro statement</span></span>


<span data-ttu-id="92e2e-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="92e2e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="92e2e-104">Оператор **Group** позволяет указать блок действий в макросе, который можно развернуть или свернуть.</span><span class="sxs-lookup"><span data-stu-id="92e2e-104">The **Group** statement enables you to specify a block of actions within a macro that you can expand or collapse.</span></span>

## <a name="setting"></a><span data-ttu-id="92e2e-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="92e2e-105">Setting</span></span>

<span data-ttu-id="92e2e-106">Действие **группы** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="92e2e-106">The **Group** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="92e2e-107">Аргумент</span><span class="sxs-lookup"><span data-stu-id="92e2e-107">Argument</span></span></p></th>
<th><p><span data-ttu-id="92e2e-108">Обязательный</span><span class="sxs-lookup"><span data-stu-id="92e2e-108">Required</span></span></p></th>
<th><p><span data-ttu-id="92e2e-109">Описание</span><span class="sxs-lookup"><span data-stu-id="92e2e-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="92e2e-110"><strong>Описание</strong></span><span class="sxs-lookup"><span data-stu-id="92e2e-110"><strong>Description</strong></span></span></p></td>
<td><p><span data-ttu-id="92e2e-111">Нет</span><span class="sxs-lookup"><span data-stu-id="92e2e-111">No</span></span></p></td>
<td><p><span data-ttu-id="92e2e-112">Строка, которая отображается в качестве заголовка группы при его свертывании.</span><span class="sxs-lookup"><span data-stu-id="92e2e-112">A string that appears as the title of a group when it is collapsed.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="92e2e-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="92e2e-113">Remarks</span></span>

<span data-ttu-id="92e2e-114">Оператор **Group** не определяет область макроса, который может выполняться по отдельности.</span><span class="sxs-lookup"><span data-stu-id="92e2e-114">The **Group** statment does not define a region of a macro that can be executed separately.</span></span> <span data-ttu-id="92e2e-115">Используйте инструкцию вложенного **[макроса](submacro-macro-statement.md)** , чтобы определить набор действий, которые будут выполняться отдельно в окне **конструктора макросов** .</span><span class="sxs-lookup"><span data-stu-id="92e2e-115">Use the **[Submacro](submacro-macro-statement.md)** statment to define a set of actions to be executed separately in the **Macro Designer** window.</span></span>

