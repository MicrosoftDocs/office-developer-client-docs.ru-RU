---
title: Свойство Ordinal (Position в ADO MD)
TOCTitle: Ordinal property (ADO MD Position)
ms:assetid: fb132ab5-d2b5-317d-e885-5e37ddaf90fb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250284(v=office.15)
ms:contentKeyID: 48548861
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2e29b5c86e8f37d84116aa92432e93eb8943e29e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711746"
---
# <a name="ordinal-property-ado-md-position"></a><span data-ttu-id="2a4e4-102">Свойство Ordinal (Position в ADO MD)</span><span class="sxs-lookup"><span data-stu-id="2a4e4-102">Ordinal property (ADO MD Position)</span></span>


<span data-ttu-id="2a4e4-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2a4e4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2a4e4-104">Однозначно определяет положение оси.</span><span class="sxs-lookup"><span data-stu-id="2a4e4-104">Uniquely identifies a position along an axis.</span></span>

## <a name="return-values"></a><span data-ttu-id="2a4e4-105">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="2a4e4-105">Return values</span></span>

<span data-ttu-id="2a4e4-106">Возвращает значение типа **Long** integer и доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="2a4e4-106">Returns a **Long** integer and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a4e4-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="2a4e4-107">Remarks</span></span>

<span data-ttu-id="2a4e4-108">**Порядковый номер** [позиции](position-object-ado-md.md) объекта соответствует индекс **позиции** в коллекции [положения](positions-collection-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="2a4e4-108">The **Ordinal** of a [Position](position-object-ado-md.md) object corresponds to the index of the **Position** within the [Positions](positions-collection-ado-md.md) collection.</span></span>

<span data-ttu-id="2a4e4-109">Ячейки можно быстро получить с помощью **порядковый номер** **позиции** каждой оси со свойством [Item](item-property-ado-md-cellset.md) объекта [ячеек](cellset-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="2a4e4-109">A cell can quickly be retrieved using the **Ordinal** of the **Position** along each axis with the [Item](item-property-ado-md-cellset.md) property of the [Cellset](cellset-object-ado-md.md) object.</span></span>

