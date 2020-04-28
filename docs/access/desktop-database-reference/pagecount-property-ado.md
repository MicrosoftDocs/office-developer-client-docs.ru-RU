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
# <a name="pagecount-property-ado"></a><span data-ttu-id="573e6-102">Свойство PageCount (ADO)</span><span class="sxs-lookup"><span data-stu-id="573e6-102">PageCount property (ADO)</span></span>


<span data-ttu-id="573e6-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="573e6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="573e6-104">Указывает количество страниц данных, содержащихся в объекте [Recordset](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="573e6-104">Indicates how many pages of data the [Recordset](recordset-object-ado.md) object contains.</span></span>

## <a name="return-value"></a><span data-ttu-id="573e6-105">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="573e6-105">Return value</span></span>

<span data-ttu-id="573e6-106">Возвращает значение **типа Long** , которое указывает количество страниц в **наборе записей**.</span><span class="sxs-lookup"><span data-stu-id="573e6-106">Returns a **Long** value that indicates the number of pages in the **Recordset**.</span></span>

## <a name="remarks"></a><span data-ttu-id="573e6-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="573e6-107">Remarks</span></span>

<span data-ttu-id="573e6-108">Используйте свойство **PageCount** , чтобы определить, сколько страниц данных находится в объекте **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="573e6-108">Use the **PageCount** property to determine how many pages of data are in the **Recordset** object.</span></span> <span data-ttu-id="573e6-109">*Страницы* — это группы записей, размер которых равен значению свойства [pageSize](pagesize-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="573e6-109">*Pages* are groups of records whose size equals the [PageSize](pagesize-property-ado.md) property setting.</span></span> <span data-ttu-id="573e6-110">Даже если последняя страница неполна, так как число записей меньше, чем значение **pageSize** , оно считается дополнительной страницей в значении **PageCount** .</span><span class="sxs-lookup"><span data-stu-id="573e6-110">Even if the last page is incomplete because there are fewer records than the **PageSize** value, it counts as an additional page in the **PageCount** value.</span></span> <span data-ttu-id="573e6-111">Если объект **Recordset** не поддерживает это свойство, значение будет равно-1, чтобы указать, что **PageCount** недоступен.</span><span class="sxs-lookup"><span data-stu-id="573e6-111">If the **Recordset** object does not support this property, the value will be -1 to indicate that the **PageCount** is indeterminable.</span></span>

<span data-ttu-id="573e6-112">Чтобы узнать больше о функциональных возможностях страниц, ознакомьтесь со статьей свойства **pageSize** и [AbsolutePage](absolutepage-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="573e6-112">See the **PageSize** and [AbsolutePage](absolutepage-property-ado.md) properties for more on page functionality.</span></span>

