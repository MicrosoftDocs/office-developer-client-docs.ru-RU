---
title: Свойство QueryDef.Updatable (DAO)
TOCTitle: Updatable Property
ms:assetid: 9b978b7d-1d76-ff27-a032-dd94660fb088
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198056(v=office.15)
ms:contentKeyID: 48546575
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b0c1a85029270641a944d822ee81954ca1f2528e
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919810"
---
# <a name="querydefupdatable-property-dao"></a><span data-ttu-id="bd390-102">Свойство QueryDef.Updatable (DAO)</span><span class="sxs-lookup"><span data-stu-id="bd390-102">QueryDef.Updatable property (DAO)</span></span>


<span data-ttu-id="bd390-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bd390-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bd390-104">Возвращает значение, указывающее, является ли объект DAO можно изменить.</span><span class="sxs-lookup"><span data-stu-id="bd390-104">Returns a value that indicates whether you can change a DAO object.</span></span> <span data-ttu-id="bd390-105">Только для чтения, **Boolean**.</span><span class="sxs-lookup"><span data-stu-id="bd390-105">Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd390-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bd390-106">Syntax</span></span>

<span data-ttu-id="bd390-107">*выражение* . Обновляемые</span><span class="sxs-lookup"><span data-stu-id="bd390-107">*expression* .Updatable</span></span>

<span data-ttu-id="bd390-108">*выражение* Переменная, которая представляет собой объект- **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="bd390-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd390-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="bd390-109">Remarks</span></span>

<span data-ttu-id="bd390-110">Свойство **с возможностью записи** объекта **QueryDef** имеет значение **True** , если определение запроса могут быть обновлены, даже в том случае, если не обновляемый объекте результирующего **[набора записей](recordset-object-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="bd390-110">The **Updatable** property of a **QueryDef** object is set to **True** if the query definition can be updated, even if the resulting **[Recordset](recordset-object-dao.md)** object isn't updatable.</span></span>

