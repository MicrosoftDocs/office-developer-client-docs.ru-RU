---
title: Direction Property (ADO)
TOCTitle: Direction Property (ADO)
ms:assetid: 51a94abb-7ce9-9adb-2b76-5391eb9f6863
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249262(v=office.15)
ms:contentKeyID: 48544823
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 611e5efbe53964c5ba255380e2659f024bd6be9a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481744"
---
# <a name="direction-property-ado"></a><span data-ttu-id="8855e-102">Direction Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="8855e-102">Direction Property (ADO)</span></span>


<span data-ttu-id="8855e-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8855e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="8855e-104">Указывает [параметр](parameter-object-ado.md) представляет входного параметра, выходного параметра, входного и выходного параметра, или если параметр имеет значение, возвращаемое хранимой процедуры.</span><span class="sxs-lookup"><span data-stu-id="8855e-104">Indicates whether the [Parameter](parameter-object-ado.md) represents an input parameter, an output parameter, an input and an output parameter, or if the parameter is the return value from a stored procedure.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="8855e-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="8855e-105">Settings and Return Values</span></span>

<span data-ttu-id="8855e-106">Задает или возвращает значение [ParameterDirectionEnum](parameterdirectionenum.md) .</span><span class="sxs-lookup"><span data-stu-id="8855e-106">Sets or returns a [ParameterDirectionEnum](parameterdirectionenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8855e-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="8855e-107">Remarks</span></span>

<span data-ttu-id="8855e-108">Используйте свойство **направление** для указания передается как параметр или из процедуры.</span><span class="sxs-lookup"><span data-stu-id="8855e-108">Use the **Direction** property to specify how a parameter is passed to or from a procedure.</span></span> <span data-ttu-id="8855e-109">Является ли данное свойство **направление** чтения/записи; Это позволяет работать с поставщиками, которые не возвращают эти сведения или задать эти сведения при отсутствии ADO, чтобы сделать дополнительного обращения к поставщику для получения сведений о параметрах.</span><span class="sxs-lookup"><span data-stu-id="8855e-109">The **Direction** property is read/write; this allows you to work with providers that don't return this information or to set this information when you don't want ADO to make an extra call to the provider to retrieve parameter information.</span></span>

<span data-ttu-id="8855e-110">Не все поставщики можно определить направление параметры их хранимых процедур.</span><span class="sxs-lookup"><span data-stu-id="8855e-110">Not all providers can determine the direction of parameters in their stored procedures.</span></span> <span data-ttu-id="8855e-111">В таких случаях необходимо задать свойство **направление** до выполнения запроса.</span><span class="sxs-lookup"><span data-stu-id="8855e-111">In these cases, you must set the **Direction** property before you execute the query.</span></span>

