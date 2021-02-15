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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288121"
---
# <a name="pagecount-property-ado"></a><span data-ttu-id="1405c-102">Свойство PageCount (ADO)</span><span class="sxs-lookup"><span data-stu-id="1405c-102">PageCount property (ADO)</span></span>


<span data-ttu-id="1405c-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1405c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1405c-104">Указывает, сколько страниц данных содержит объект [Recordset.](recordset-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="1405c-104">Indicates how many pages of data the [Recordset](recordset-object-ado.md) object contains.</span></span>

## <a name="return-value"></a><span data-ttu-id="1405c-105">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1405c-105">Return value</span></span>

<span data-ttu-id="1405c-106">Возвращает **длинное** значение, которое указывает количество страниц в **наборе записей.**</span><span class="sxs-lookup"><span data-stu-id="1405c-106">Returns a **Long** value that indicates the number of pages in the **Recordset**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1405c-107">Заметки</span><span class="sxs-lookup"><span data-stu-id="1405c-107">Remarks</span></span>

<span data-ttu-id="1405c-108">Используйте свойство **PageCount,** чтобы определить, сколько страниц данных находится в **объекте Recordset.**</span><span class="sxs-lookup"><span data-stu-id="1405c-108">Use the **PageCount** property to determine how many pages of data are in the **Recordset** object.</span></span> <span data-ttu-id="1405c-109">*Страницы —* это группы записей, размер которых равен параметру свойства [PageSize.](pagesize-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="1405c-109">*Pages* are groups of records whose size equals the [PageSize](pagesize-property-ado.md) property setting.</span></span> <span data-ttu-id="1405c-110">Даже если последняя страница является неполной, так как записей меньше, чем значение **PageSize,** она считается дополнительной страницей в значении **PageCount.**</span><span class="sxs-lookup"><span data-stu-id="1405c-110">Even if the last page is incomplete because there are fewer records than the **PageSize** value, it counts as an additional page in the **PageCount** value.</span></span> <span data-ttu-id="1405c-111">Если объект **Recordset** не поддерживает это свойство, значение будет -1, чтобы указать, что **PageCount** неопределен.</span><span class="sxs-lookup"><span data-stu-id="1405c-111">If the **Recordset** object does not support this property, the value will be -1 to indicate that the **PageCount** is indeterminable.</span></span>

<span data-ttu-id="1405c-112">Дополнительные возможности страниц см. в свойствах **PageSize** и [AbsolutePage.](absolutepage-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="1405c-112">See the **PageSize** and [AbsolutePage](absolutepage-property-ado.md) properties for more on page functionality.</span></span>

