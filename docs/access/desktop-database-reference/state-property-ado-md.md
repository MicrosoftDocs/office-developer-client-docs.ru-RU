---
title: Свойство State (ADO MD)
TOCTitle: State property (ADO MD)
ms:assetid: 4df09f45-9b62-33ce-b4ed-230e41eaac7a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249249(v=office.15)
ms:contentKeyID: 48544744
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 051a9f0cc50ae3a60edb033f6807f72fc0688976
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702448"
---
# <a name="state-property-ado-md"></a><span data-ttu-id="a640e-102">Свойство State (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="a640e-102">State property (ADO MD)</span></span>


<span data-ttu-id="a640e-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a640e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a640e-104">Указывает текущее состояние ячеек.</span><span class="sxs-lookup"><span data-stu-id="a640e-104">Indicates the current state of the cellset.</span></span>

## <a name="return-values"></a><span data-ttu-id="a640e-105">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="a640e-105">Return values</span></span>

<span data-ttu-id="a640e-106">Возвращает **длинное** целое число, указывающее текущее состояние объекта [ячеек](cellset-object-ado-md.md) и доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="a640e-106">Returns a **Long** integer indicating the current condition of the [Cellset](cellset-object-ado-md.md) object and is read-only.</span></span> <span data-ttu-id="a640e-107">Допустимыми являются следующие значения: **adStateClosed** (0) и **adStateOpen** (1).</span><span class="sxs-lookup"><span data-stu-id="a640e-107">The following values are valid: **adStateClosed** (0) and **adStateOpen** (1).</span></span>

## <a name="remarks"></a><span data-ttu-id="a640e-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="a640e-108">Remarks</span></span>

<span data-ttu-id="a640e-109">Чтобы использовать имена констант [ObjectStateEnum](objectstateenum.md) , необходимо иметь на библиотеку типов ADO ссылается проект.</span><span class="sxs-lookup"><span data-stu-id="a640e-109">To use the [ObjectStateEnum](objectstateenum.md) constant names, you must have the ADO type library referenced in your project.</span></span> <span data-ttu-id="a640e-110">[С помощью ADO с ADO MD](using-ado-with-ado-md.md) более подробные сведения.</span><span class="sxs-lookup"><span data-stu-id="a640e-110">See [Using ADO with ADO MD](using-ado-with-ado-md.md) for more information.</span></span>

