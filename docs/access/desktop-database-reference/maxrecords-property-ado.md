---
title: Свойство MaxRecords (ADO)
TOCTitle: MaxRecords property (ADO)
ms:assetid: 424b2d41-073a-3fbe-30aa-99fac94f9a81
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249195(v=office.15)
ms:contentKeyID: 48544475
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7d66a26cffb14220670643c5b6b5aafe94e8fcb5
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870088"
---
# <a name="maxrecords-property-ado"></a><span data-ttu-id="46647-102">Свойство MaxRecords (ADO)</span><span class="sxs-lookup"><span data-stu-id="46647-102">MaxRecords property (ADO)</span></span>


<span data-ttu-id="46647-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="46647-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="46647-104">Указывает максимальное число записей для возврата [набора записей](recordset-object-ado.md) из запроса.</span><span class="sxs-lookup"><span data-stu-id="46647-104">Indicates the maximum number of records to return to a [Recordset](recordset-object-ado.md) from a query.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="46647-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="46647-105">Settings and return values</span></span>

<span data-ttu-id="46647-106">Задает или возвращает значение типа **Long** , указывающее максимальное число возвращаемых записей.</span><span class="sxs-lookup"><span data-stu-id="46647-106">Sets or returns a **Long** value that indicates the maximum number of records to return.</span></span> <span data-ttu-id="46647-107">Значение по умолчанию — 0 (без ограничений).</span><span class="sxs-lookup"><span data-stu-id="46647-107">Default is zero (no limit).</span></span>

## <a name="remarks"></a><span data-ttu-id="46647-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="46647-108">Remarks</span></span>

<span data-ttu-id="46647-109">Свойство **MaxRecords** максимальное число записей, которые поставщик возвращает из источника данных.</span><span class="sxs-lookup"><span data-stu-id="46647-109">Use the **MaxRecords** property to limit the number of records that the provider returns from the data source.</span></span> <span data-ttu-id="46647-110">По умолчанию этого свойства равно нулю, что означает, что поставщик возвращает все запрошенные записей.</span><span class="sxs-lookup"><span data-stu-id="46647-110">The default setting of this property is zero, which means the provider returns all requested records.</span></span>

<span data-ttu-id="46647-111">Свойство **MaxRecords** при чтение и запись **набора записей** закрытой и только для чтения, при открытии.</span><span class="sxs-lookup"><span data-stu-id="46647-111">The **MaxRecords** property is read/write when the **Recordset** is closed and read-only when it is open.</span></span>

