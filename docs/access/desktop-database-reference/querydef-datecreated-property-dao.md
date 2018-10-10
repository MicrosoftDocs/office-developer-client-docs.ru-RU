---
title: QueryDef.DateCreated Property (DAO)
TOCTitle: DateCreated Property
ms:assetid: f7585b34-8314-fb9f-daa6-cd1a8ad59d91
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836910(v=office.15)
ms:contentKeyID: 48548763
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 62fcad68a50ac7f2a09675d9ac51734c4147d207
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482720"
---
# <a name="querydefdatecreated-property-dao"></a><span data-ttu-id="7e038-102">QueryDef.DateCreated Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="7e038-102">QueryDef.DateCreated Property (DAO)</span></span>


<span data-ttu-id="7e038-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7e038-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="7e038-104">Возвращает дату и время создания объекта (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="7e038-104">Returns the date and time that an object was created (Microsoft Access workspaces only).</span></span> <span data-ttu-id="7e038-105">Только для чтения **Variant**.</span><span class="sxs-lookup"><span data-stu-id="7e038-105">Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e038-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7e038-106">Syntax</span></span>

<span data-ttu-id="7e038-107">*выражение* . DateCreated</span><span class="sxs-lookup"><span data-stu-id="7e038-107">*expression* .DateCreated</span></span>

<span data-ttu-id="7e038-108">*выражение* Переменная, которая представляет собой объект- **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="7e038-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e038-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="7e038-109">Remarks</span></span>

<span data-ttu-id="7e038-110">**DateCreated** и **LastUpdated** возвращают дату и время создания или последнего обновления.</span><span class="sxs-lookup"><span data-stu-id="7e038-110">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated.</span></span> <span data-ttu-id="7e038-111">В многопользовательской среде пользователи должны получить эти параметры непосредственно из файлового сервера, чтобы избежать несоответствия в DateCreated и параметры свойства LastUpdated.</span><span class="sxs-lookup"><span data-stu-id="7e038-111">In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

