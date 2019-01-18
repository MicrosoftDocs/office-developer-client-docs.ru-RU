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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709357"
---
# <a name="maxrecords-property-ado"></a><span data-ttu-id="cc9c0-102">Свойство MaxRecords (ADO)</span><span class="sxs-lookup"><span data-stu-id="cc9c0-102">MaxRecords property (ADO)</span></span>


<span data-ttu-id="cc9c0-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cc9c0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cc9c0-104">Указывает максимальное число записей для возврата [набора записей](recordset-object-ado.md) из запроса.</span><span class="sxs-lookup"><span data-stu-id="cc9c0-104">Indicates the maximum number of records to return to a [Recordset](recordset-object-ado.md) from a query.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="cc9c0-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="cc9c0-105">Settings and return values</span></span>

<span data-ttu-id="cc9c0-106">Задает или возвращает значение типа **Long** , указывающее максимальное число возвращаемых записей.</span><span class="sxs-lookup"><span data-stu-id="cc9c0-106">Sets or returns a **Long** value that indicates the maximum number of records to return.</span></span> <span data-ttu-id="cc9c0-107">Значение по умолчанию — 0 (без ограничений).</span><span class="sxs-lookup"><span data-stu-id="cc9c0-107">Default is zero (no limit).</span></span>

## <a name="remarks"></a><span data-ttu-id="cc9c0-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="cc9c0-108">Remarks</span></span>

<span data-ttu-id="cc9c0-109">Свойство **MaxRecords** максимальное число записей, которые поставщик возвращает из источника данных.</span><span class="sxs-lookup"><span data-stu-id="cc9c0-109">Use the **MaxRecords** property to limit the number of records that the provider returns from the data source.</span></span> <span data-ttu-id="cc9c0-110">По умолчанию этого свойства равно нулю, что означает, что поставщик возвращает все запрошенные записей.</span><span class="sxs-lookup"><span data-stu-id="cc9c0-110">The default setting of this property is zero, which means the provider returns all requested records.</span></span>

<span data-ttu-id="cc9c0-111">Свойство **MaxRecords** при чтение и запись **набора записей** закрытой и только для чтения, при открытии.</span><span class="sxs-lookup"><span data-stu-id="cc9c0-111">The **MaxRecords** property is read/write when the **Recordset** is closed and read-only when it is open.</span></span>

