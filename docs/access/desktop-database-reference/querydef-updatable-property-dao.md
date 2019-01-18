---
title: Свойство QueryDef.Updatable (DAO)
TOCTitle: Updatable Property
ms:assetid: 9b978b7d-1d76-ff27-a032-dd94660fb088
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198056(v=office.15)
ms:contentKeyID: 48546575
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c5321e834f1dd5ed663033cacb530962d7beeb5a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713368"
---
# <a name="querydefupdatable-property-dao"></a><span data-ttu-id="6d5cd-102">Свойство QueryDef.Updatable (DAO)</span><span class="sxs-lookup"><span data-stu-id="6d5cd-102">QueryDef.Updatable property (DAO)</span></span>


<span data-ttu-id="6d5cd-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6d5cd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6d5cd-104">Возвращает значение, указывающее, является ли объект DAO можно изменить.</span><span class="sxs-lookup"><span data-stu-id="6d5cd-104">Returns a value that indicates whether you can change a DAO object.</span></span> <span data-ttu-id="6d5cd-105">Только для чтения, **Boolean**.</span><span class="sxs-lookup"><span data-stu-id="6d5cd-105">Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d5cd-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6d5cd-106">Syntax</span></span>

<span data-ttu-id="6d5cd-107">*выражение* . Обновляемые</span><span class="sxs-lookup"><span data-stu-id="6d5cd-107">*expression* .Updatable</span></span>

<span data-ttu-id="6d5cd-108">*выражение* Переменная, которая представляет собой объект- **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="6d5cd-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d5cd-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="6d5cd-109">Remarks</span></span>

<span data-ttu-id="6d5cd-110">Свойство **с возможностью записи** объекта **QueryDef** имеет значение **True** , если определение запроса могут быть обновлены, даже в том случае, если не обновляемый объекте результирующего **[набора записей](recordset-object-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="6d5cd-110">The **Updatable** property of a **QueryDef** object is set to **True** if the query definition can be updated, even if the resulting **[Recordset](recordset-object-dao.md)** object isn't updatable.</span></span>

