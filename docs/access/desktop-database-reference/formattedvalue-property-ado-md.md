---
title: Свойство FormattedValue (ADO MD)
TOCTitle: FormattedValue property (ADO MD)
ms:assetid: ea7962f2-b08b-52c9-34e5-c5490c72662f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250189(v=office.15)
ms:contentKeyID: 48548464
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d750944cd42feb95b09f53382c54329ea0c32e1d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292316"
---
# <a name="formattedvalue-property-ado-md"></a><span data-ttu-id="4526f-102">Свойство FormattedValue (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="4526f-102">FormattedValue property (ADO MD)</span></span>


<span data-ttu-id="4526f-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4526f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4526f-104">Указывает отформатированный дисплей значения ячейки.</span><span class="sxs-lookup"><span data-stu-id="4526f-104">Indicates the formatted display of a cell value.</span></span>

## <a name="return-values"></a><span data-ttu-id="4526f-105">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="4526f-105">Return values</span></span>

<span data-ttu-id="4526f-106">Возвращает **строку и** является только для чтения.</span><span class="sxs-lookup"><span data-stu-id="4526f-106">Returns a **String** and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="4526f-107">Заметки</span><span class="sxs-lookup"><span data-stu-id="4526f-107">Remarks</span></span>

<span data-ttu-id="4526f-108">Используйте свойство **FormattedValue** для получения отформатированных отображаемого значения свойства [Value](value-property-ado-md.md) объекта [Cell.](cell-object-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="4526f-108">Use the **FormattedValue** property to obtain the formatted display value of the [Value](value-property-ado-md.md) property of a [Cell](cell-object-ado-md.md) object.</span></span> <span data-ttu-id="4526f-109">Например, если значение ячейки было 1056,87, а это значение представляет сумму в долларах, **FormattedValue** будет 1 056,87 долл. США.</span><span class="sxs-lookup"><span data-stu-id="4526f-109">For example, if the value of a cell was 1056.87, and this value represented a dollar amount, **FormattedValue** would be $1,056.87.</span></span>

