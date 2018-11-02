---
title: Свойство FormattedValue (ADO MD)
TOCTitle: FormattedValue property (ADO MD)
ms:assetid: ea7962f2-b08b-52c9-34e5-c5490c72662f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250189(v=office.15)
ms:contentKeyID: 48548464
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 547feea04a7e6d103f30071094070650705789be
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922113"
---
# <a name="formattedvalue-property-ado-md"></a><span data-ttu-id="21951-102">Свойство FormattedValue (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="21951-102">FormattedValue property (ADO MD)</span></span>


<span data-ttu-id="21951-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="21951-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="21951-104">Указывает, отформатированный отображаемое значение ячейки.</span><span class="sxs-lookup"><span data-stu-id="21951-104">Indicates the formatted display of a cell value.</span></span>

## <a name="return-values"></a><span data-ttu-id="21951-105">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="21951-105">Return values</span></span>

<span data-ttu-id="21951-106">Возвращает **строку** и доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="21951-106">Returns a **String** and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="21951-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="21951-107">Remarks</span></span>

<span data-ttu-id="21951-108">Используйте свойство **FormattedValue** для получения форматированный отображаемое значение свойства [Value](value-property-ado-md.md) объекта [ячейки](cell-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="21951-108">Use the **FormattedValue** property to obtain the formatted display value of the [Value](value-property-ado-md.md) property of a [Cell](cell-object-ado-md.md) object.</span></span> <span data-ttu-id="21951-109">Например если значение ячейки было 1056.87, и это значение представлено денежное значение, **FormattedValue** будет 1,056.87 $.</span><span class="sxs-lookup"><span data-stu-id="21951-109">For example, if the value of a cell was 1056.87, and this value represented a dollar amount, **FormattedValue** would be $1,056.87.</span></span>

