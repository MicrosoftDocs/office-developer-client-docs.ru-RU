---
title: QueryDef.Updatable Property (DAO)
TOCTitle: Updatable Property
ms:assetid: 9b978b7d-1d76-ff27-a032-dd94660fb088
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198056(v=office.15)
ms:contentKeyID: 48546575
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6ca30e86bd61bc5459a552423bd451c7b158996d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480041"
---
# <a name="querydefupdatable-property-dao"></a><span data-ttu-id="6d30e-102">QueryDef.Updatable Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="6d30e-102">QueryDef.Updatable Property (DAO)</span></span>


<span data-ttu-id="6d30e-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6d30e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6d30e-104">Возвращает значение, указывающее, является ли объект DAO можно изменить.</span><span class="sxs-lookup"><span data-stu-id="6d30e-104">Returns a value that indicates whether you can change a DAO object.</span></span> <span data-ttu-id="6d30e-105">Только для чтения, **Boolean**.</span><span class="sxs-lookup"><span data-stu-id="6d30e-105">Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d30e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6d30e-106">Syntax</span></span>

<span data-ttu-id="6d30e-107">*выражение* . Обновляемые</span><span class="sxs-lookup"><span data-stu-id="6d30e-107">*expression* .Updatable</span></span>

<span data-ttu-id="6d30e-108">*выражение* Переменная, которая представляет собой объект- **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="6d30e-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d30e-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="6d30e-109">Remarks</span></span>

<span data-ttu-id="6d30e-110">Свойство **с возможностью записи** объекта **QueryDef** имеет значение **True** , если определение запроса могут быть обновлены, даже в том случае, если не обновляемый объекте результирующего **[набора записей](recordset-object-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="6d30e-110">The **Updatable** property of a **QueryDef** object is set to **True** if the query definition can be updated, even if the resulting **[Recordset](recordset-object-dao.md)** object isn't updatable.</span></span>

