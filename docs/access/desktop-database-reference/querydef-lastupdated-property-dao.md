---
title: Свойство QueryDef.LastUpdated (DAO)
TOCTitle: LastUpdated Property
ms:assetid: 3b7818d4-054e-54e2-bf63-58b340bb4a90
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192665(v=office.15)
ms:contentKeyID: 48544287
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1876e92381828075edca3bbfcbae63e706a21365
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712563"
---
# <a name="querydeflastupdated-property-dao"></a><span data-ttu-id="88b35-102">Свойство QueryDef.LastUpdated (DAO)</span><span class="sxs-lookup"><span data-stu-id="88b35-102">QueryDef.LastUpdated property (DAO)</span></span>


<span data-ttu-id="88b35-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="88b35-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="88b35-104">Возвращает дату и время последнего изменения, внесенные в объект.</span><span class="sxs-lookup"><span data-stu-id="88b35-104">Returns the date and time of the most recent change made to an object.</span></span> <span data-ttu-id="88b35-105">Только для чтения, **Variant**.</span><span class="sxs-lookup"><span data-stu-id="88b35-105">Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="88b35-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="88b35-106">Syntax</span></span>

<span data-ttu-id="88b35-107">*выражение* . LastUpdated</span><span class="sxs-lookup"><span data-stu-id="88b35-107">*expression* .LastUpdated</span></span>

<span data-ttu-id="88b35-108">*выражение* Переменная, которая представляет собой объект- **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="88b35-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="88b35-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="88b35-109">Remarks</span></span>

<span data-ttu-id="88b35-110">**DateCreated** и **LastUpdated** возвращают дату и время создания или последнего обновления.</span><span class="sxs-lookup"><span data-stu-id="88b35-110">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated.</span></span> <span data-ttu-id="88b35-111">В многопользовательской среде пользователи должны получить эти параметры непосредственно из файлового сервера, чтобы избежать несоответствия в DateCreated и параметры свойства LastUpdated.</span><span class="sxs-lookup"><span data-stu-id="88b35-111">In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

