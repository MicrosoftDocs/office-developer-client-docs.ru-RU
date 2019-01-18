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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722321"
---
# <a name="setfield-macro-action"></a><span data-ttu-id="e19c0-102">Макрокоманда SetField</span><span class="sxs-lookup"><span data-stu-id="e19c0-102">SetField macro action</span></span>

<span data-ttu-id="e19c0-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e19c0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e19c0-104">Действие **SetField** используется для присвоения значения поля.</span><span class="sxs-lookup"><span data-stu-id="e19c0-104">The **SetField** action can be used to assign a value to a field.</span></span>

> [!NOTE]
> <span data-ttu-id="e19c0-105">**SetField** действие доступно только в макросов данных.</span><span class="sxs-lookup"><span data-stu-id="e19c0-105">The **SetField** action is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="e19c0-106">Setting</span><span class="sxs-lookup"><span data-stu-id="e19c0-106">Setting</span></span>

<span data-ttu-id="e19c0-107">Действие **SetField** содержит аргументы, перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="e19c0-107">The **SetField** action has the arguments listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e19c0-108">Аргумент</span><span class="sxs-lookup"><span data-stu-id="e19c0-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="e19c0-109">Описание</span><span class="sxs-lookup"><span data-stu-id="e19c0-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e19c0-110"><strong>Name</strong></span><span class="sxs-lookup"><span data-stu-id="e19c0-110"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="e19c0-111">Строка, идентифицирующая поле.</span><span class="sxs-lookup"><span data-stu-id="e19c0-111">A string that identifies the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e19c0-112"><strong>Value</strong></span><span class="sxs-lookup"><span data-stu-id="e19c0-112"><strong>Value</strong></span></span></p></td>
<td><p><span data-ttu-id="e19c0-113">Выражение, которое задает значение, задаваемое в поле.</span><span class="sxs-lookup"><span data-stu-id="e19c0-113">An expression that specifies the value to assign to the field.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="e19c0-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="e19c0-114">Remarks</span></span>

<span data-ttu-id="e19c0-115">Действие **SetField** не может использоваться вне блока данных **[СоздатьЗапись](createrecord-data-block.md)** или **[ИзменитьЗапись](editrecord-data-block.md)** .</span><span class="sxs-lookup"><span data-stu-id="e19c0-115">The **SetField** action cannot be used outside of an **[CreateRecord](createrecord-data-block.md)** or **[EditRecord](editrecord-data-block.md)** data block.</span></span>

