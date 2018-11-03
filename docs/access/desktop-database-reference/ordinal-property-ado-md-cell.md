---
title: Свойство Ordinal (ADO MD Cell)
TOCTitle: Ordinal property (ADO MD Cell)
ms:assetid: be705823-6c5e-0c8f-f780-87df19423a72
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249924(v=office.15)
ms:contentKeyID: 48547462
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4fbbe461390a5f8a068f839bcf41fab5e1ad66ff
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946757"
---
# <a name="ordinal-property-ado-md-cell"></a><span data-ttu-id="177d9-102">Свойство Ordinal (ADO MD Cell)</span><span class="sxs-lookup"><span data-stu-id="177d9-102">Ordinal property (ADO MD Cell)</span></span>


<span data-ttu-id="177d9-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="177d9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="177d9-104">Однозначно определяет ячейку по ее позиции в рамках набора ячеек.</span><span class="sxs-lookup"><span data-stu-id="177d9-104">Uniquely identifies a cell by its position within a cellset.</span></span>

## <a name="return-values"></a><span data-ttu-id="177d9-105">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="177d9-105">Return values</span></span>

<span data-ttu-id="177d9-106">Возвращает значение типа **Long** integer и доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="177d9-106">Returns a **Long** integer and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="177d9-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="177d9-107">Remarks</span></span>

<span data-ttu-id="177d9-108">Порядковый номер ячейки однозначно определяет ячейку в рамках набора ячеек.</span><span class="sxs-lookup"><span data-stu-id="177d9-108">The cell's ordinal value uniquely identifies the cell within a cellset.</span></span> <span data-ttu-id="177d9-109">Концептуально ячеек нумеруются в набора ячеек, как будто ячеек *p*-двумерного массива array, где *p* — это число [осей](axes-collection-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="177d9-109">Conceptually, cells are numbered in a cellset as if the cellset were a *p*-dimensional array, where *p* is the number of [axes](axes-collection-ado-md.md).</span></span> <span data-ttu-id="177d9-110">Ячейки нумеруются, начиная с нуля в строкам.</span><span class="sxs-lookup"><span data-stu-id="177d9-110">Cells are numbered starting from zero in row-major order.</span></span>

<span data-ttu-id="177d9-111">Порядковый номер ячейки можно использовать свойство [Item](item-property-ado-md-cellset.md) объекта [ячеек](cellset-object-ado-md.md) для быстрого извлечения [ячейки](cell-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="177d9-111">The cell's ordinal value can be used with the [Item](item-property-ado-md-cellset.md) property of the [Cellset](cellset-object-ado-md.md) object to quickly retrieve the [Cell](cell-object-ado-md.md).</span></span>

