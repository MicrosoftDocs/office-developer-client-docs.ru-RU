---
title: QueryDef.LastUpdated Property (DAO)
TOCTitle: LastUpdated Property
ms:assetid: 3b7818d4-054e-54e2-bf63-58b340bb4a90
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192665(v=office.15)
ms:contentKeyID: 48544287
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 370f8a9a1e503240f3764a18350a0d491af471f3
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877900"
---
# <a name="querydeflastupdated-property-dao"></a><span data-ttu-id="aaf9d-102">QueryDef.LastUpdated Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="aaf9d-102">QueryDef.LastUpdated Property (DAO)</span></span>


<span data-ttu-id="aaf9d-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="aaf9d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="aaf9d-104">Возвращает дату и время последнего изменения, внесенные в объект.</span><span class="sxs-lookup"><span data-stu-id="aaf9d-104">Returns the date and time of the most recent change made to an object.</span></span> <span data-ttu-id="aaf9d-105">Только для чтения **Variant**.</span><span class="sxs-lookup"><span data-stu-id="aaf9d-105">Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="aaf9d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aaf9d-106">Syntax</span></span>

<span data-ttu-id="aaf9d-107">*выражение* . LastUpdated</span><span class="sxs-lookup"><span data-stu-id="aaf9d-107">*expression* .LastUpdated</span></span>

<span data-ttu-id="aaf9d-108">*выражение* Переменная, которая представляет собой объект- **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="aaf9d-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="aaf9d-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="aaf9d-109">Remarks</span></span>

<span data-ttu-id="aaf9d-110">**DateCreated** и **LastUpdated** возвращают дату и время создания или последнего обновления.</span><span class="sxs-lookup"><span data-stu-id="aaf9d-110">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated.</span></span> <span data-ttu-id="aaf9d-111">В многопользовательской среде пользователи должны получить эти параметры непосредственно из файлового сервера, чтобы избежать несоответствия в DateCreated и параметры свойства LastUpdated.</span><span class="sxs-lookup"><span data-stu-id="aaf9d-111">In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

