---
title: Свойство Direction (ADO)
TOCTitle: Direction property (ADO)
ms:assetid: 51a94abb-7ce9-9adb-2b76-5391eb9f6863
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249262(v=office.15)
ms:contentKeyID: 48544823
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5885e89a3bce5d8b16ea855ce14689380655ad45
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706333"
---
# <a name="direction-property-ado"></a><span data-ttu-id="410a1-102">Свойство Direction (ADO)</span><span class="sxs-lookup"><span data-stu-id="410a1-102">Direction property (ADO)</span></span>


<span data-ttu-id="410a1-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="410a1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="410a1-104">Указывает [параметр](parameter-object-ado.md) представляет входного параметра, выходного параметра, входного и выходного параметра, или если параметр имеет значение, возвращаемое хранимой процедуры.</span><span class="sxs-lookup"><span data-stu-id="410a1-104">Indicates whether the [Parameter](parameter-object-ado.md) represents an input parameter, an output parameter, an input and an output parameter, or if the parameter is the return value from a stored procedure.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="410a1-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="410a1-105">Settings and return values</span></span>

<span data-ttu-id="410a1-106">Задает или возвращает значение [ParameterDirectionEnum](parameterdirectionenum.md) .</span><span class="sxs-lookup"><span data-stu-id="410a1-106">Sets or returns a [ParameterDirectionEnum](parameterdirectionenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="410a1-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="410a1-107">Remarks</span></span>

<span data-ttu-id="410a1-108">Используйте свойство **направление** для указания передается как параметр или из процедуры.</span><span class="sxs-lookup"><span data-stu-id="410a1-108">Use the **Direction** property to specify how a parameter is passed to or from a procedure.</span></span> <span data-ttu-id="410a1-109">Является ли данное свойство **направление** чтения/записи; Это позволяет работать с поставщиками, которые не возвращают эти сведения или задать эти сведения при отсутствии ADO, чтобы сделать дополнительного обращения к поставщику для получения сведений о параметрах.</span><span class="sxs-lookup"><span data-stu-id="410a1-109">The **Direction** property is read/write; this allows you to work with providers that don't return this information or to set this information when you don't want ADO to make an extra call to the provider to retrieve parameter information.</span></span>

<span data-ttu-id="410a1-110">Не все поставщики можно определить направление параметры их хранимых процедур.</span><span class="sxs-lookup"><span data-stu-id="410a1-110">Not all providers can determine the direction of parameters in their stored procedures.</span></span> <span data-ttu-id="410a1-111">В таких случаях необходимо задать свойство **направление** до выполнения запроса.</span><span class="sxs-lookup"><span data-stu-id="410a1-111">In these cases, you must set the **Direction** property before you execute the query.</span></span>

