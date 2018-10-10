---
title: MaxRecords Property (ADO)
TOCTitle: MaxRecords Property (ADO)
ms:assetid: 424b2d41-073a-3fbe-30aa-99fac94f9a81
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249195(v=office.15)
ms:contentKeyID: 48544475
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d8753bf09655371042e97ead083c6849f1736b8b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481298"
---
# <a name="maxrecords-property-ado"></a><span data-ttu-id="b40fc-102">MaxRecords Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="b40fc-102">MaxRecords Property (ADO)</span></span>


<span data-ttu-id="b40fc-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b40fc-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b40fc-104">Указывает максимальное число записей для возврата [набора записей](recordset-object-ado.md) из запроса.</span><span class="sxs-lookup"><span data-stu-id="b40fc-104">Indicates the maximum number of records to return to a [Recordset](recordset-object-ado.md) from a query.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="b40fc-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="b40fc-105">Settings and Return Values</span></span>

<span data-ttu-id="b40fc-106">Задает или возвращает значение типа **Long** , указывающее максимальное число возвращаемых записей.</span><span class="sxs-lookup"><span data-stu-id="b40fc-106">Sets or returns a **Long** value that indicates the maximum number of records to return.</span></span> <span data-ttu-id="b40fc-107">Значение по умолчанию — 0 (без ограничений).</span><span class="sxs-lookup"><span data-stu-id="b40fc-107">Default is zero (no limit).</span></span>

## <a name="remarks"></a><span data-ttu-id="b40fc-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="b40fc-108">Remarks</span></span>

<span data-ttu-id="b40fc-109">Свойство **MaxRecords** максимальное число записей, которые поставщик возвращает из источника данных.</span><span class="sxs-lookup"><span data-stu-id="b40fc-109">Use the **MaxRecords** property to limit the number of records that the provider returns from the data source.</span></span> <span data-ttu-id="b40fc-110">По умолчанию этого свойства равно нулю, что означает, что поставщик возвращает все запрошенные записей.</span><span class="sxs-lookup"><span data-stu-id="b40fc-110">The default setting of this property is zero, which means the provider returns all requested records.</span></span>

<span data-ttu-id="b40fc-111">Свойство **MaxRecords** при чтение и запись **набора записей** закрытой и только для чтения, при открытии.</span><span class="sxs-lookup"><span data-stu-id="b40fc-111">The **MaxRecords** property is read/write when the **Recordset** is closed and read-only when it is open.</span></span>

