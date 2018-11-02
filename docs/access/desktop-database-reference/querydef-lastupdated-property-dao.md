---
title: Свойство QueryDef.LastUpdated (DAO)
TOCTitle: LastUpdated Property
ms:assetid: 3b7818d4-054e-54e2-bf63-58b340bb4a90
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192665(v=office.15)
ms:contentKeyID: 48544287
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 98bb600e6f3f1c9587eca110269e8b6b3765e40f
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921274"
---
# <a name="querydeflastupdated-property-dao"></a><span data-ttu-id="1362b-102">Свойство QueryDef.LastUpdated (DAO)</span><span class="sxs-lookup"><span data-stu-id="1362b-102">QueryDef.LastUpdated property (DAO)</span></span>


<span data-ttu-id="1362b-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1362b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1362b-104">Возвращает дату и время последнего изменения, внесенные в объект.</span><span class="sxs-lookup"><span data-stu-id="1362b-104">Returns the date and time of the most recent change made to an object.</span></span> <span data-ttu-id="1362b-105">Только для чтения **Variant**.</span><span class="sxs-lookup"><span data-stu-id="1362b-105">Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="1362b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1362b-106">Syntax</span></span>

<span data-ttu-id="1362b-107">*выражение* . LastUpdated</span><span class="sxs-lookup"><span data-stu-id="1362b-107">*expression* .LastUpdated</span></span>

<span data-ttu-id="1362b-108">*выражение* Переменная, которая представляет собой объект- **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="1362b-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1362b-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="1362b-109">Remarks</span></span>

<span data-ttu-id="1362b-110">**DateCreated** и **LastUpdated** возвращают дату и время создания или последнего обновления.</span><span class="sxs-lookup"><span data-stu-id="1362b-110">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated.</span></span> <span data-ttu-id="1362b-111">В многопользовательской среде пользователи должны получить эти параметры непосредственно из файлового сервера, чтобы избежать несоответствия в DateCreated и параметры свойства LastUpdated.</span><span class="sxs-lookup"><span data-stu-id="1362b-111">In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

