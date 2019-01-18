---
title: Свойство QueryDef.DateCreated (DAO)
TOCTitle: DateCreated Property
ms:assetid: f7585b34-8314-fb9f-daa6-cd1a8ad59d91
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836910(v=office.15)
ms:contentKeyID: 48548763
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a4a120eed6c20db73e1c23f31ea9329d00da2f0d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699683"
---
# <a name="querydefdatecreated-property-dao"></a><span data-ttu-id="c960d-102">Свойство QueryDef.DateCreated (DAO)</span><span class="sxs-lookup"><span data-stu-id="c960d-102">QueryDef.DateCreated property (DAO)</span></span>


<span data-ttu-id="c960d-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c960d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c960d-104">Возвращает дату и время создания объекта (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="c960d-104">Returns the date and time that an object was created (Microsoft Access workspaces only).</span></span> <span data-ttu-id="c960d-105">Только для чтения, **Variant**.</span><span class="sxs-lookup"><span data-stu-id="c960d-105">Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="c960d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c960d-106">Syntax</span></span>

<span data-ttu-id="c960d-107">*выражение* . DateCreated</span><span class="sxs-lookup"><span data-stu-id="c960d-107">*expression* .DateCreated</span></span>

<span data-ttu-id="c960d-108">*выражение* Переменная, которая представляет собой объект- **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="c960d-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c960d-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="c960d-109">Remarks</span></span>

<span data-ttu-id="c960d-110">**DateCreated** и **LastUpdated** возвращают дату и время создания или последнего обновления.</span><span class="sxs-lookup"><span data-stu-id="c960d-110">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated.</span></span> <span data-ttu-id="c960d-111">В многопользовательской среде пользователи должны получить эти параметры непосредственно из файлового сервера, чтобы избежать несоответствия в DateCreated и параметры свойства LastUpdated.</span><span class="sxs-lookup"><span data-stu-id="c960d-111">In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

