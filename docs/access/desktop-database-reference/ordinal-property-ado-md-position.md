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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288192"
---
# <a name="ordinal-property-ado-md-position"></a><span data-ttu-id="d7505-102">Свойство Ordinal (Position в ADO MD)</span><span class="sxs-lookup"><span data-stu-id="d7505-102">Ordinal property (ADO MD Position)</span></span>


<span data-ttu-id="d7505-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d7505-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d7505-104">Уникально определяет положение вдоль оси.</span><span class="sxs-lookup"><span data-stu-id="d7505-104">Uniquely identifies a position along an axis.</span></span>

## <a name="return-values"></a><span data-ttu-id="d7505-105">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="d7505-105">Return values</span></span>

<span data-ttu-id="d7505-106">Возвращает целое значение **типа Long** и доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d7505-106">Returns a **Long** integer and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7505-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="d7505-107">Remarks</span></span>

<span data-ttu-id="d7505-108">**ПорядкОвый номер** объекта [position](position-object-ado-md.md) соответствует индексу **позиции** в коллекции [Positions](positions-collection-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="d7505-108">The **Ordinal** of a [Position](position-object-ado-md.md) object corresponds to the index of the **Position** within the [Positions](positions-collection-ado-md.md) collection.</span></span>

<span data-ttu-id="d7505-109">Ячейка может быстро извлекаться с помощью **порядкОвого номера** **позиции** на каждой оси со свойством [Item](item-property-ado-md-cellset.md) объекта набора [ячеек](cellset-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="d7505-109">A cell can quickly be retrieved using the **Ordinal** of the **Position** along each axis with the [Item](item-property-ado-md-cellset.md) property of the [Cellset](cellset-object-ado-md.md) object.</span></span>

