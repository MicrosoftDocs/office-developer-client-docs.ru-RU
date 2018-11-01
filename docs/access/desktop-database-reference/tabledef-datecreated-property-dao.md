---
title: TableDef.DateCreated Property (DAO)
TOCTitle: DateCreated Property
ms:assetid: fedd28e9-41a4-db7f-9ba9-6ada350d594a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837292(v=office.15)
ms:contentKeyID: 48548947
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2cf97df5d5861a3bb0fdac34ceabc8f732a87d5c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885600"
---
# <a name="tabledefdatecreated-property-dao"></a><span data-ttu-id="455a7-102">TableDef.DateCreated Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="455a7-102">TableDef.DateCreated Property (DAO)</span></span>


<span data-ttu-id="455a7-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="455a7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="455a7-104">Возвращает дату и время создания объекта (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="455a7-104">Returns the date and time that an object was created (Microsoft Access workspaces only).</span></span> <span data-ttu-id="455a7-105">Только для чтения **Variant**.</span><span class="sxs-lookup"><span data-stu-id="455a7-105">Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="455a7-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="455a7-106">Syntax</span></span>

<span data-ttu-id="455a7-107">*выражение* . DateCreated</span><span class="sxs-lookup"><span data-stu-id="455a7-107">*expression* .DateCreated</span></span>

<span data-ttu-id="455a7-108">*выражение* Переменная, которая представляет собой объект- **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="455a7-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="455a7-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="455a7-109">Remarks</span></span>

<span data-ttu-id="455a7-110">**DateCreated** и **LastUpdated** возвращают дату и время создания или последнего обновления.</span><span class="sxs-lookup"><span data-stu-id="455a7-110">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated.</span></span> <span data-ttu-id="455a7-111">В многопользовательской среде пользователи должны получить эти параметры непосредственно из файлового сервера, чтобы избежать несоответствия в DateCreated и параметры свойства LastUpdated.</span><span class="sxs-lookup"><span data-stu-id="455a7-111">In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

