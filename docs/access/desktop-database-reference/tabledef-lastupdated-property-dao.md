---
title: TableDef.LastUpdated Property (DAO)
TOCTitle: LastUpdated Property
ms:assetid: fafe54e2-2cf0-5874-92b9-6e20a65e77ef
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837164(v=office.15)
ms:contentKeyID: 48548859
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 10d0203bd30c2e03f7cd2aaa761ac1cf76b12f94
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870865"
---
# <a name="tabledeflastupdated-property-dao"></a><span data-ttu-id="62b09-102">TableDef.LastUpdated Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="62b09-102">TableDef.LastUpdated Property (DAO)</span></span>


<span data-ttu-id="62b09-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="62b09-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="62b09-104">Возвращает дату и время последнего изменения, внесенные в объект.</span><span class="sxs-lookup"><span data-stu-id="62b09-104">Returns the date and time of the most recent change made to an object.</span></span> <span data-ttu-id="62b09-105">Только для чтения **Variant**.</span><span class="sxs-lookup"><span data-stu-id="62b09-105">Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="62b09-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62b09-106">Syntax</span></span>

<span data-ttu-id="62b09-107">*выражение* . LastUpdated</span><span class="sxs-lookup"><span data-stu-id="62b09-107">*expression* .LastUpdated</span></span>

<span data-ttu-id="62b09-108">*выражение* Переменная, которая представляет собой объект- **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="62b09-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="62b09-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="62b09-109">Remarks</span></span>

<span data-ttu-id="62b09-110">**DateCreated** и **LastUpdated** возвращают дату и время создания или последнего обновления.</span><span class="sxs-lookup"><span data-stu-id="62b09-110">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated.</span></span> <span data-ttu-id="62b09-111">В многопользовательской среде пользователи должны получить эти параметры непосредственно из файлового сервера, чтобы избежать несоответствия в DateCreated и параметры свойства LastUpdated.</span><span class="sxs-lookup"><span data-stu-id="62b09-111">In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

