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
# <a name="maxrecords-property-ado"></a><span data-ttu-id="fcaea-102">Свойство MaxRecords (ADO)</span><span class="sxs-lookup"><span data-stu-id="fcaea-102">MaxRecords property (ADO)</span></span>


<span data-ttu-id="fcaea-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fcaea-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fcaea-104">Указывает максимальное количество записей, которые возвращаются в [набор записей](recordset-object-ado.md) из запроса.</span><span class="sxs-lookup"><span data-stu-id="fcaea-104">Indicates the maximum number of records to return to a [Recordset](recordset-object-ado.md) from a query.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="fcaea-105">Параметры и значения возврата</span><span class="sxs-lookup"><span data-stu-id="fcaea-105">Settings and return values</span></span>

<span data-ttu-id="fcaea-106">Задает или возвращает значение **Long,** которое указывает максимальное количество возвращаемых записей.</span><span class="sxs-lookup"><span data-stu-id="fcaea-106">Sets or returns a **Long** value that indicates the maximum number of records to return.</span></span> <span data-ttu-id="fcaea-107">По умолчанию — ноль (без ограничений).</span><span class="sxs-lookup"><span data-stu-id="fcaea-107">Default is zero (no limit).</span></span>

## <a name="remarks"></a><span data-ttu-id="fcaea-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="fcaea-108">Remarks</span></span>

<span data-ttu-id="fcaea-109">Используйте **свойство MaxRecords,** чтобы ограничить количество записей, которые поставщик возвращает из источника данных.</span><span class="sxs-lookup"><span data-stu-id="fcaea-109">Use the **MaxRecords** property to limit the number of records that the provider returns from the data source.</span></span> <span data-ttu-id="fcaea-110">Значение по умолчанию для этого свойства нулевое, что означает, что поставщик возвращает все запрашиваемые записи.</span><span class="sxs-lookup"><span data-stu-id="fcaea-110">The default setting of this property is zero, which means the provider returns all requested records.</span></span>

<span data-ttu-id="fcaea-111">Свойство **MaxRecords** считывало или записывало, когда **набор записей** закрыт и только для чтения, когда он открыт.</span><span class="sxs-lookup"><span data-stu-id="fcaea-111">The **MaxRecords** property is read/write when the **Recordset** is closed and read-only when it is open.</span></span>

