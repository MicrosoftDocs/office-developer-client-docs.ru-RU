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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303334"
---
# <a name="querydefupdatable-property-dao"></a><span data-ttu-id="26455-102">Свойство QueryDef.Updatable (DAO)</span><span class="sxs-lookup"><span data-stu-id="26455-102">QueryDef.Updatable property (DAO)</span></span>


<span data-ttu-id="26455-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="26455-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="26455-104">Возвращает значение, которое указывает на то, можно ли изменить DAO объект.</span><span class="sxs-lookup"><span data-stu-id="26455-104">Returns a value that indicates whether you can change a DAO object.</span></span> <span data-ttu-id="26455-105">Только для чтения, **Boolean**.</span><span class="sxs-lookup"><span data-stu-id="26455-105">Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="26455-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="26455-106">Syntax</span></span>

<span data-ttu-id="26455-107">*выражения* . Updatable</span><span class="sxs-lookup"><span data-stu-id="26455-107">*expression* .Updatable</span></span>

<span data-ttu-id="26455-108">*выражение*: переменная, представляющая объект **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="26455-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="26455-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="26455-109">Remarks</span></span>

<span data-ttu-id="26455-110">Свойство **Updatable** объекта **QueryDef** задалось true, если определение запроса может быть обновлено, даже если в результате объект **[Recordset](recordset-object-dao.md)** не является updatable. </span><span class="sxs-lookup"><span data-stu-id="26455-110">The **Updatable** property of a **QueryDef** object is set to **True** if the query definition can be updated, even if the resulting **[Recordset](recordset-object-dao.md)** object isn't updatable.</span></span>

