---
title: Свойство TableDef.LastUpdated (DAO)
TOCTitle: LastUpdated Property
ms:assetid: fafe54e2-2cf0-5874-92b9-6e20a65e77ef
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837164(v=office.15)
ms:contentKeyID: 48548859
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 994543132fb5323566bd876da066419d0986bd91
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722776"
---
# <a name="tabledeflastupdated-property-dao"></a><span data-ttu-id="b5952-102">Свойство TableDef.LastUpdated (DAO)</span><span class="sxs-lookup"><span data-stu-id="b5952-102">TableDef.LastUpdated property (DAO)</span></span>


<span data-ttu-id="b5952-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b5952-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b5952-104">Возвращает дату и время последнего изменения, внесенные в объект.</span><span class="sxs-lookup"><span data-stu-id="b5952-104">Returns the date and time of the most recent change made to an object.</span></span> <span data-ttu-id="b5952-105">Только для чтения, **Variant**.</span><span class="sxs-lookup"><span data-stu-id="b5952-105">Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5952-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b5952-106">Syntax</span></span>

<span data-ttu-id="b5952-107">*выражение* . LastUpdated</span><span class="sxs-lookup"><span data-stu-id="b5952-107">*expression* .LastUpdated</span></span>

<span data-ttu-id="b5952-108">*выражение* Переменная, которая представляет собой объект- **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="b5952-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5952-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="b5952-109">Remarks</span></span>

<span data-ttu-id="b5952-110">**DateCreated** и **LastUpdated** возвращают дату и время создания или последнего обновления.</span><span class="sxs-lookup"><span data-stu-id="b5952-110">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated.</span></span> <span data-ttu-id="b5952-111">В многопользовательской среде пользователи должны получить эти параметры непосредственно из файлового сервера, чтобы избежать несоответствия в DateCreated и параметры свойства LastUpdated.</span><span class="sxs-lookup"><span data-stu-id="b5952-111">In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

