---
title: Свойство MaxRecords (ADO)
TOCTitle: MaxRecords property (ADO)
ms:assetid: 424b2d41-073a-3fbe-30aa-99fac94f9a81
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249195(v=office.15)
ms:contentKeyID: 48544475
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8ed643ca3b1341d7f933901e15c20c84acb025f5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289723"
---
# <a name="maxrecords-property-ado"></a><span data-ttu-id="21825-102">Свойство MaxRecords (ADO)</span><span class="sxs-lookup"><span data-stu-id="21825-102">MaxRecords property (ADO)</span></span>


<span data-ttu-id="21825-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="21825-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="21825-104">Указывает максимальное число записей, возвращаемых в [набор записей](recordset-object-ado.md) из запроса.</span><span class="sxs-lookup"><span data-stu-id="21825-104">Indicates the maximum number of records to return to a [Recordset](recordset-object-ado.md) from a query.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="21825-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="21825-105">Settings and return values</span></span>

<span data-ttu-id="21825-106">Задает или возвращает значение **типа Long** , которое указывает максимальное число возвращаемых записей.</span><span class="sxs-lookup"><span data-stu-id="21825-106">Sets or returns a **Long** value that indicates the maximum number of records to return.</span></span> <span data-ttu-id="21825-107">Значение по умолчанию — ноль (без ограничений).</span><span class="sxs-lookup"><span data-stu-id="21825-107">Default is zero (no limit).</span></span>

## <a name="remarks"></a><span data-ttu-id="21825-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="21825-108">Remarks</span></span>

<span data-ttu-id="21825-109">Используйте свойство **maxRecords** , чтобы ограничить количество записей, возвращаемых поставщиком из источника данных.</span><span class="sxs-lookup"><span data-stu-id="21825-109">Use the **MaxRecords** property to limit the number of records that the provider returns from the data source.</span></span> <span data-ttu-id="21825-110">Значение по умолчанию для этого свойства равно нулю, что означает, что поставщик возвращает все запрошенные записи.</span><span class="sxs-lookup"><span data-stu-id="21825-110">The default setting of this property is zero, which means the provider returns all requested records.</span></span>

<span data-ttu-id="21825-111">Свойство **maxRecords** доступно для чтения и записи, когда **набор записей** закрывается и только для чтения, когда он открыт.</span><span class="sxs-lookup"><span data-stu-id="21825-111">The **MaxRecords** property is read/write when the **Recordset** is closed and read-only when it is open.</span></span>

