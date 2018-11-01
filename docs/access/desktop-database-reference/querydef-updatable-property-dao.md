---
title: QueryDef.Updatable Property (DAO)
TOCTitle: Updatable Property
ms:assetid: 9b978b7d-1d76-ff27-a032-dd94660fb088
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198056(v=office.15)
ms:contentKeyID: 48546575
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4ad761c2941cb556ce67c9f716247663220f753f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873693"
---
# <a name="querydefupdatable-property-dao"></a><span data-ttu-id="ffd9a-102">QueryDef.Updatable Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="ffd9a-102">QueryDef.Updatable Property (DAO)</span></span>


<span data-ttu-id="ffd9a-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ffd9a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ffd9a-104">Возвращает значение, указывающее, является ли объект DAO можно изменить.</span><span class="sxs-lookup"><span data-stu-id="ffd9a-104">Returns a value that indicates whether you can change a DAO object.</span></span> <span data-ttu-id="ffd9a-105">Только для чтения, **Boolean**.</span><span class="sxs-lookup"><span data-stu-id="ffd9a-105">Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffd9a-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ffd9a-106">Syntax</span></span>

<span data-ttu-id="ffd9a-107">*выражение* . Обновляемые</span><span class="sxs-lookup"><span data-stu-id="ffd9a-107">*expression* .Updatable</span></span>

<span data-ttu-id="ffd9a-108">*выражение* Переменная, которая представляет собой объект- **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="ffd9a-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ffd9a-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="ffd9a-109">Remarks</span></span>

<span data-ttu-id="ffd9a-110">Свойство **с возможностью записи** объекта **QueryDef** имеет значение **True** , если определение запроса могут быть обновлены, даже в том случае, если не обновляемый объекте результирующего **[набора записей](recordset-object-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="ffd9a-110">The **Updatable** property of a **QueryDef** object is set to **True** if the query definition can be updated, even if the resulting **[Recordset](recordset-object-dao.md)** object isn't updatable.</span></span>

