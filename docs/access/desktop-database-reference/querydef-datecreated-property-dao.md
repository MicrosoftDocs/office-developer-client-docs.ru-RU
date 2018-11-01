---
title: QueryDef.DateCreated Property (DAO)
TOCTitle: DateCreated Property
ms:assetid: f7585b34-8314-fb9f-daa6-cd1a8ad59d91
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836910(v=office.15)
ms:contentKeyID: 48548763
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2d770decd0bf023a9c2ad8699a8aca4686d73491
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875415"
---
# <a name="querydefdatecreated-property-dao"></a><span data-ttu-id="2db50-102">QueryDef.DateCreated Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="2db50-102">QueryDef.DateCreated Property (DAO)</span></span>


<span data-ttu-id="2db50-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2db50-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2db50-104">Возвращает дату и время создания объекта (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="2db50-104">Returns the date and time that an object was created (Microsoft Access workspaces only).</span></span> <span data-ttu-id="2db50-105">Только для чтения **Variant**.</span><span class="sxs-lookup"><span data-stu-id="2db50-105">Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="2db50-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2db50-106">Syntax</span></span>

<span data-ttu-id="2db50-107">*выражение* . DateCreated</span><span class="sxs-lookup"><span data-stu-id="2db50-107">*expression* .DateCreated</span></span>

<span data-ttu-id="2db50-108">*выражение* Переменная, которая представляет собой объект- **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="2db50-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2db50-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="2db50-109">Remarks</span></span>

<span data-ttu-id="2db50-110">**DateCreated** и **LastUpdated** возвращают дату и время создания или последнего обновления.</span><span class="sxs-lookup"><span data-stu-id="2db50-110">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated.</span></span> <span data-ttu-id="2db50-111">В многопользовательской среде пользователи должны получить эти параметры непосредственно из файлового сервера, чтобы избежать несоответствия в DateCreated и параметры свойства LastUpdated.</span><span class="sxs-lookup"><span data-stu-id="2db50-111">In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

