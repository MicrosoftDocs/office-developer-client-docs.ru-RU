---
title: Document.LastUpdated Property (DAO)
TOCTitle: LastUpdated Property
ms:assetid: 9307ceee-095f-0364-fd5b-905bc523b9c0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197661(v=office.15)
ms:contentKeyID: 48546388
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ad5a84dcc1765cc90fdfb08adfb6610be7057401
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879650"
---
# <a name="documentlastupdated-property-dao"></a><span data-ttu-id="d0c55-102">Document.LastUpdated Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="d0c55-102">Document.LastUpdated Property (DAO)</span></span>


<span data-ttu-id="d0c55-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d0c55-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d0c55-104">Возвращает дату и время последнего изменения, внесенные в объект.</span><span class="sxs-lookup"><span data-stu-id="d0c55-104">Returns the date and time of the most recent change made to an object.</span></span> <span data-ttu-id="d0c55-105">Только для чтения **Variant**.</span><span class="sxs-lookup"><span data-stu-id="d0c55-105">Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0c55-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d0c55-106">Syntax</span></span>

<span data-ttu-id="d0c55-107">*выражение* . LastUpdated</span><span class="sxs-lookup"><span data-stu-id="d0c55-107">*expression* .LastUpdated</span></span>

<span data-ttu-id="d0c55-108">*выражение* Переменная, которая представляет собой объект- **документов** .</span><span class="sxs-lookup"><span data-stu-id="d0c55-108">*expression* A variable that represents a **Document** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0c55-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="d0c55-109">Remarks</span></span>

<span data-ttu-id="d0c55-110">**DateCreated** и **LastUpdated** возвращают дату и время создания или последнего обновления.</span><span class="sxs-lookup"><span data-stu-id="d0c55-110">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated.</span></span> <span data-ttu-id="d0c55-111">В многопользовательской среде пользователи должны получить эти параметры непосредственно из файлового сервера, чтобы избежать несоответствия в DateCreated и параметры свойства LastUpdated.</span><span class="sxs-lookup"><span data-stu-id="d0c55-111">In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

