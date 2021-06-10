---
title: Свойство state (ADO MD)
TOCTitle: State property (ADO MD)
ms:assetid: 4df09f45-9b62-33ce-b4ed-230e41eaac7a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249249(v=office.15)
ms:contentKeyID: 48544744
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 051a9f0cc50ae3a60edb033f6807f72fc0688976
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306365"
---
# <a name="state-property-ado-md"></a><span data-ttu-id="fb5a9-102">Свойство state (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="fb5a9-102">State property (ADO MD)</span></span>


<span data-ttu-id="fb5a9-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fb5a9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fb5a9-104">Указывает текущее состояние ячейки.</span><span class="sxs-lookup"><span data-stu-id="fb5a9-104">Indicates the current state of the cellset.</span></span>

## <a name="return-values"></a><span data-ttu-id="fb5a9-105">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="fb5a9-105">Return values</span></span>

<span data-ttu-id="fb5a9-106">Возвращает **длинное** количество, указывающее текущее состояние объекта [Cellset,](cellset-object-ado-md.md) и только для чтения.</span><span class="sxs-lookup"><span data-stu-id="fb5a9-106">Returns a **Long** integer indicating the current condition of the [Cellset](cellset-object-ado-md.md) object and is read-only.</span></span> <span data-ttu-id="fb5a9-107">Допустимы следующие значения: **adStateClosed** (0) и **adStateOpen** (1).</span><span class="sxs-lookup"><span data-stu-id="fb5a9-107">The following values are valid: **adStateClosed** (0) and **adStateOpen** (1).</span></span>

## <a name="remarks"></a><span data-ttu-id="fb5a9-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="fb5a9-108">Remarks</span></span>

<span data-ttu-id="fb5a9-109">Чтобы использовать [постоянные имена ObjectStateEnum,](objectstateenum.md) в проекте должна быть ссылаться библиотека типов ADO.</span><span class="sxs-lookup"><span data-stu-id="fb5a9-109">To use the [ObjectStateEnum](objectstateenum.md) constant names, you must have the ADO type library referenced in your project.</span></span> <span data-ttu-id="fb5a9-110">Дополнительные сведения см. [в использовании ADO с ADO MD.](using-ado-with-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="fb5a9-110">See [Using ADO with ADO MD](using-ado-with-ado-md.md) for more information.</span></span>

