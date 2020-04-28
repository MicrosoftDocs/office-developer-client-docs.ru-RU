---
title: Свойство QueryDef. обновляемое свойство (DAO)
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
# <a name="querydefupdatable-property-dao"></a><span data-ttu-id="48812-102">Свойство QueryDef. обновляемое свойство (DAO)</span><span class="sxs-lookup"><span data-stu-id="48812-102">QueryDef.Updatable property (DAO)</span></span>


<span data-ttu-id="48812-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="48812-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="48812-104">Возвращает значение, которое указывает на то, можно ли изменить DAO объект.</span><span class="sxs-lookup"><span data-stu-id="48812-104">Returns a value that indicates whether you can change a DAO object.</span></span> <span data-ttu-id="48812-105">Только для чтения, **Boolean**.</span><span class="sxs-lookup"><span data-stu-id="48812-105">Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="48812-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="48812-106">Syntax</span></span>

<span data-ttu-id="48812-107">*Expression* . Updatable</span><span class="sxs-lookup"><span data-stu-id="48812-107">*expression* .Updatable</span></span>

<span data-ttu-id="48812-108">*выражение*: переменная, представляющая объект **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="48812-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="48812-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="48812-109">Remarks</span></span>

<span data-ttu-id="48812-110">Для свойства **обновляемого** объекта **QueryDef** задается значение **true** , если определение запроса можно обновить, даже если полученный объект **[Recordset](recordset-object-dao.md)** не обновляется.</span><span class="sxs-lookup"><span data-stu-id="48812-110">The **Updatable** property of a **QueryDef** object is set to **True** if the query definition can be updated, even if the resulting **[Recordset](recordset-object-dao.md)** object isn't updatable.</span></span>

