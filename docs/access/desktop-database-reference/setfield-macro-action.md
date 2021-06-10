---
title: Макрокоманда SetField
TOCTitle: SetField macro action
ms:assetid: 66bd26e3-e8c3-b9a1-2f16-f29adc44a345
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195227(v=office.15)
ms:contentKeyID: 48545349
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4fbf7252729c7b376da6ebe67f59941c1caf924d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314618"
---
# <a name="setfield-macro-action"></a><span data-ttu-id="f89af-102">Макрокоманда SetField</span><span class="sxs-lookup"><span data-stu-id="f89af-102">SetField macro action</span></span>

<span data-ttu-id="f89af-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f89af-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f89af-104">Действие **SetField** можно использовать для назначения значения для поля.</span><span class="sxs-lookup"><span data-stu-id="f89af-104">The **SetField** action can be used to assign a value to a field.</span></span>

> [!NOTE]
> <span data-ttu-id="f89af-105">Действие **SetField** доступно только в макросах данных.</span><span class="sxs-lookup"><span data-stu-id="f89af-105">The **SetField** action is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="f89af-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="f89af-106">Setting</span></span>

<span data-ttu-id="f89af-107">Действие **SetField** имеет аргументы, перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="f89af-107">The **SetField** action has the arguments listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f89af-108">Аргументация</span><span class="sxs-lookup"><span data-stu-id="f89af-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="f89af-109">Описание</span><span class="sxs-lookup"><span data-stu-id="f89af-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f89af-110"><strong>Name</strong></span><span class="sxs-lookup"><span data-stu-id="f89af-110"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="f89af-111">Строка, определяемая полем.</span><span class="sxs-lookup"><span data-stu-id="f89af-111">A string that identifies the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f89af-112"><strong>Значение</strong></span><span class="sxs-lookup"><span data-stu-id="f89af-112"><strong>Value</strong></span></span></p></td>
<td><p><span data-ttu-id="f89af-113">Выражение, которое указывает значение, которое необходимо назначить поле.</span><span class="sxs-lookup"><span data-stu-id="f89af-113">An expression that specifies the value to assign to the field.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="f89af-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="f89af-114">Remarks</span></span>

<span data-ttu-id="f89af-115">Действие **SetField** нельзя использовать вне блока **[данных CreateRecord](createrecord-data-block.md)** или **[EditRecord.](editrecord-data-block.md)**</span><span class="sxs-lookup"><span data-stu-id="f89af-115">The **SetField** action cannot be used outside of an **[CreateRecord](createrecord-data-block.md)** or **[EditRecord](editrecord-data-block.md)** data block.</span></span>

