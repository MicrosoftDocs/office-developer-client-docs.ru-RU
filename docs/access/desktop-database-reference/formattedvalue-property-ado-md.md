---
title: FormattedValue Property (ADO MD)
TOCTitle: FormattedValue Property (ADO MD)
ms:assetid: ea7962f2-b08b-52c9-34e5-c5490c72662f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250189(v=office.15)
ms:contentKeyID: 48548464
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b867c44e80e3333d0dafdcef9fc166f4384e9469
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482108"
---
# <a name="formattedvalue-property-ado-md"></a><span data-ttu-id="e20ed-102">FormattedValue Property (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="e20ed-102">FormattedValue Property (ADO MD)</span></span>


<span data-ttu-id="e20ed-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e20ed-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e20ed-104">Указывает, отформатированный отображаемое значение ячейки.</span><span class="sxs-lookup"><span data-stu-id="e20ed-104">Indicates the formatted display of a cell value.</span></span>

## <a name="return-values"></a><span data-ttu-id="e20ed-105">Return Values</span><span class="sxs-lookup"><span data-stu-id="e20ed-105">Return Values</span></span>

<span data-ttu-id="e20ed-106">Возвращает **строку** и доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="e20ed-106">Returns a **String** and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="e20ed-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="e20ed-107">Remarks</span></span>

<span data-ttu-id="e20ed-108">Используйте свойство **FormattedValue** для получения форматированный отображаемое значение свойства [Value](value-property-ado-md.md) объекта [ячейки](cell-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="e20ed-108">Use the **FormattedValue** property to obtain the formatted display value of the [Value](value-property-ado-md.md) property of a [Cell](cell-object-ado-md.md) object.</span></span> <span data-ttu-id="e20ed-109">Например если значение ячейки было 1056.87, и это значение представлено денежное значение, **FormattedValue** будет 1,056.87 $.</span><span class="sxs-lookup"><span data-stu-id="e20ed-109">For example, if the value of a cell was 1056.87, and this value represented a dollar amount, **FormattedValue** would be $1,056.87.</span></span>

