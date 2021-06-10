---
title: Свойство Ordinal (Cell в ADO MD)
TOCTitle: Ordinal property (ADO MD Cell)
ms:assetid: be705823-6c5e-0c8f-f780-87df19423a72
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249924(v=office.15)
ms:contentKeyID: 48547462
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 91b8d66929e360f88385b6773a03fcaffb79161d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288205"
---
# <a name="ordinal-property-ado-md-cell"></a><span data-ttu-id="2d57e-102">Свойство Ordinal (Cell в ADO MD)</span><span class="sxs-lookup"><span data-stu-id="2d57e-102">Ordinal property (ADO MD Cell)</span></span>


<span data-ttu-id="2d57e-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2d57e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2d57e-104">Уникально определяет ячейку по ее положению в ячейке.</span><span class="sxs-lookup"><span data-stu-id="2d57e-104">Uniquely identifies a cell by its position within a cellset.</span></span>

## <a name="return-values"></a><span data-ttu-id="2d57e-105">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="2d57e-105">Return values</span></span>

<span data-ttu-id="2d57e-106">Возвращает длинный **ряд** и только для чтения.</span><span class="sxs-lookup"><span data-stu-id="2d57e-106">Returns a **Long** integer and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d57e-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="2d57e-107">Remarks</span></span>

<span data-ttu-id="2d57e-108">Координатное значение ячейки однозначно определяет ячейку в ячейке.</span><span class="sxs-lookup"><span data-stu-id="2d57e-108">The cell's ordinal value uniquely identifies the cell within a cellset.</span></span> <span data-ttu-id="2d57e-109">Концептуально ячейки нумеруются в ячейках так, как если бы ячейки были *p-мерным* массивом, где *p* — это число [осей.](axes-collection-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="2d57e-109">Conceptually, cells are numbered in a cellset as if the cellset were a *p*-dimensional array, where *p* is the number of [axes](axes-collection-ado-md.md).</span></span> <span data-ttu-id="2d57e-110">Ячейки прону номером начиная с нуля в порядке строка-мажор.</span><span class="sxs-lookup"><span data-stu-id="2d57e-110">Cells are numbered starting from zero in row-major order.</span></span>

<span data-ttu-id="2d57e-111">Координатное значение ячейки можно использовать с свойством [Item](item-property-ado-md-cellset.md) объекта [Cellset](cellset-object-ado-md.md) для быстрого получения [ячейки.](cell-object-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="2d57e-111">The cell's ordinal value can be used with the [Item](item-property-ado-md-cellset.md) property of the [Cellset](cellset-object-ado-md.md) object to quickly retrieve the [Cell](cell-object-ado-md.md).</span></span>

