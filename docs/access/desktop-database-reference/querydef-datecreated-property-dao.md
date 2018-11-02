---
title: Свойство QueryDef.DateCreated (DAO)
TOCTitle: DateCreated Property
ms:assetid: f7585b34-8314-fb9f-daa6-cd1a8ad59d91
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836910(v=office.15)
ms:contentKeyID: 48548763
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3eb3d4664f6fce30812904612f458d24f3a8b159
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927027"
---
# <a name="querydefdatecreated-property-dao"></a><span data-ttu-id="b3e8f-102">Свойство QueryDef.DateCreated (DAO)</span><span class="sxs-lookup"><span data-stu-id="b3e8f-102">QueryDef.DateCreated property (DAO)</span></span>


<span data-ttu-id="b3e8f-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b3e8f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b3e8f-104">Возвращает дату и время создания объекта (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="b3e8f-104">Returns the date and time that an object was created (Microsoft Access workspaces only).</span></span> <span data-ttu-id="b3e8f-105">Только для чтения **Variant**.</span><span class="sxs-lookup"><span data-stu-id="b3e8f-105">Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3e8f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b3e8f-106">Syntax</span></span>

<span data-ttu-id="b3e8f-107">*выражение* . DateCreated</span><span class="sxs-lookup"><span data-stu-id="b3e8f-107">*expression* .DateCreated</span></span>

<span data-ttu-id="b3e8f-108">*выражение* Переменная, которая представляет собой объект- **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="b3e8f-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3e8f-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="b3e8f-109">Remarks</span></span>

<span data-ttu-id="b3e8f-110">**DateCreated** и **LastUpdated** возвращают дату и время создания или последнего обновления.</span><span class="sxs-lookup"><span data-stu-id="b3e8f-110">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated.</span></span> <span data-ttu-id="b3e8f-111">В многопользовательской среде пользователи должны получить эти параметры непосредственно из файлового сервера, чтобы избежать несоответствия в DateCreated и параметры свойства LastUpdated.</span><span class="sxs-lookup"><span data-stu-id="b3e8f-111">In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

