---
title: Свойство PageCount (ADO)
TOCTitle: PageCount property (ADO)
ms:assetid: 9cd8bf5c-b1e7-a453-4629-9cba7e408f53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249712(v=office.15)
ms:contentKeyID: 48546609
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b37ccc0c9a61e00b3c2e8f5eb3367831e5ddea43
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704555"
---
# <a name="pagecount-property-ado"></a><span data-ttu-id="440a7-102">Свойство PageCount (ADO)</span><span class="sxs-lookup"><span data-stu-id="440a7-102">PageCount property (ADO)</span></span>


<span data-ttu-id="440a7-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="440a7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="440a7-104">Показывает, сколько страниц данных содержит объекта [набора записей](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="440a7-104">Indicates how many pages of data the [Recordset](recordset-object-ado.md) object contains.</span></span>

## <a name="return-value"></a><span data-ttu-id="440a7-105">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="440a7-105">Return value</span></span>

<span data-ttu-id="440a7-106">Возвращает значение типа **Long** , показывает, сколько страниц в **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="440a7-106">Returns a **Long** value that indicates the number of pages in the **Recordset**.</span></span>

## <a name="remarks"></a><span data-ttu-id="440a7-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="440a7-107">Remarks</span></span>

<span data-ttu-id="440a7-108">Используйте свойство **PageCount** , чтобы определить, сколько страниц данных находятся в объекте **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="440a7-108">Use the **PageCount** property to determine how many pages of data are in the **Recordset** object.</span></span> <span data-ttu-id="440a7-109">*Страницы* — это группы, размер которого равен значение свойства [PageSize](pagesize-property-ado.md) записей.</span><span class="sxs-lookup"><span data-stu-id="440a7-109">*Pages* are groups of records whose size equals the [PageSize](pagesize-property-ado.md) property setting.</span></span> <span data-ttu-id="440a7-110">Даже в том случае, если последней странице не заполнен, так как меньше записей, чем значение **PageSize** , счетчиков на дополнительные в качестве значения **PageCount** .</span><span class="sxs-lookup"><span data-stu-id="440a7-110">Even if the last page is incomplete because there are fewer records than the **PageSize** value, it counts as an additional page in the **PageCount** value.</span></span> <span data-ttu-id="440a7-111">Если объекта **набора записей** не поддерживает это свойство, значение будет равно -1, указывая, что **PageCount** неопределенной.</span><span class="sxs-lookup"><span data-stu-id="440a7-111">If the **Recordset** object does not support this property, the value will be -1 to indicate that the **PageCount** is indeterminable.</span></span>

<span data-ttu-id="440a7-112">В разделе свойства **PageSize** и [AbsolutePage](absolutepage-property-ado.md) больше функциональных возможностей на страницу.</span><span class="sxs-lookup"><span data-stu-id="440a7-112">See the **PageSize** and [AbsolutePage](absolutepage-property-ado.md) properties for more on page functionality.</span></span>

