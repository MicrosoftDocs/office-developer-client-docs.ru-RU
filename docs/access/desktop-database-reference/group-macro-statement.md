---
title: Оператор макроса Group
TOCTitle: Group macro statement
ms:assetid: 42aa4afa-ab5d-9dcc-2182-786f025e316d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192918(v=office.15)
ms:contentKeyID: 48544481
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c82169ac430496587c6ebab5e439d70bc9319b5e
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930891"
---
# <a name="group-macro-statement"></a><span data-ttu-id="f5ef7-102">Оператор макроса Group</span><span class="sxs-lookup"><span data-stu-id="f5ef7-102">Group macro statement</span></span>


<span data-ttu-id="f5ef7-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f5ef7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f5ef7-104">Оператор **группы** позволяет указать блок действия макроса, который можно развернуть или свернуть.</span><span class="sxs-lookup"><span data-stu-id="f5ef7-104">The **Group** statement enables you to specify a block of actions within a macro that you can expand or collapse.</span></span>

## <a name="setting"></a><span data-ttu-id="f5ef7-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="f5ef7-105">Setting</span></span>

<span data-ttu-id="f5ef7-106">Действие **группы** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="f5ef7-106">The **Group** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f5ef7-107">Argument</span><span class="sxs-lookup"><span data-stu-id="f5ef7-107">Argument</span></span></p></th>
<th><p><span data-ttu-id="f5ef7-108">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f5ef7-108">Required</span></span></p></th>
<th><p><span data-ttu-id="f5ef7-109">Описание</span><span class="sxs-lookup"><span data-stu-id="f5ef7-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f5ef7-110"><strong>Описание</strong></span><span class="sxs-lookup"><span data-stu-id="f5ef7-110"><strong>Description</strong></span></span></p></td>
<td><p><span data-ttu-id="f5ef7-111">НЕТ</span><span class="sxs-lookup"><span data-stu-id="f5ef7-111">No</span></span></p></td>
<td><p><span data-ttu-id="f5ef7-112">Строка, которая отображается как заголовок группы, когда она свернута.</span><span class="sxs-lookup"><span data-stu-id="f5ef7-112">A string that appears as the title of a group when it is collapsed.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="f5ef7-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="f5ef7-113">Remarks</span></span>

<span data-ttu-id="f5ef7-114">Оператор **группы** не определяет область макрос, который может выполняться отдельно.</span><span class="sxs-lookup"><span data-stu-id="f5ef7-114">The **Group** statment does not define a region of a macro that can be executed separately.</span></span> <span data-ttu-id="f5ef7-115">Оператор **[Вложенный макрос](submacro-macro-statement.md)** используется для определения набора действия для выполнения отдельно в окне **Конструктор макросов** .</span><span class="sxs-lookup"><span data-stu-id="f5ef7-115">Use the **[Submacro](submacro-macro-statement.md)** statment to define a set of actions to be executed separately in the **Macro Designer** window.</span></span>

