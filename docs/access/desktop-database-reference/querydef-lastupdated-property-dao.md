---
title: Свойство QueryDef. Ластупдатед (DAO)
TOCTitle: LastUpdated Property
ms:assetid: 3b7818d4-054e-54e2-bf63-58b340bb4a90
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192665(v=office.15)
ms:contentKeyID: 48544287
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1876e92381828075edca3bbfcbae63e706a21365
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303313"
---
# <a name="querydeflastupdated-property-dao"></a><span data-ttu-id="14b60-102">Свойство QueryDef. Ластупдатед (DAO)</span><span class="sxs-lookup"><span data-stu-id="14b60-102">QueryDef.LastUpdated property (DAO)</span></span>


<span data-ttu-id="14b60-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="14b60-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="14b60-104">Возвращает дату и время последнего изменения, внесенного в объект.</span><span class="sxs-lookup"><span data-stu-id="14b60-104">Returns the date and time of the most recent change made to an object.</span></span> <span data-ttu-id="14b60-105">Только для чтения, **Variant**.</span><span class="sxs-lookup"><span data-stu-id="14b60-105">Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="14b60-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="14b60-106">Syntax</span></span>

<span data-ttu-id="14b60-107">*Expression* . ластупдатед</span><span class="sxs-lookup"><span data-stu-id="14b60-107">*expression* .LastUpdated</span></span>

<span data-ttu-id="14b60-108">*выражение*: переменная, представляющая объект **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="14b60-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="14b60-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="14b60-109">Remarks</span></span>

<span data-ttu-id="14b60-110">**DateCreated** и **ластупдатед** возвращают дату и время создания или последнего обновления объекта.</span><span class="sxs-lookup"><span data-stu-id="14b60-110">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated.</span></span> <span data-ttu-id="14b60-111">В многопользовательской среде пользователи должны получить эти параметры непосредственно с файлового сервера, чтобы избежать расхождений в параметрах свойств DateCreated и Ластупдатед.</span><span class="sxs-lookup"><span data-stu-id="14b60-111">In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

