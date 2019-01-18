---
title: Свойство Document.LastUpdated (DAO)
TOCTitle: LastUpdated Property
ms:assetid: 9307ceee-095f-0364-fd5b-905bc523b9c0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197661(v=office.15)
ms:contentKeyID: 48546388
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: abb766f7a47cbacaededf65eb2b5e9145bf88c60
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698381"
---
# <a name="documentlastupdated-property-dao"></a><span data-ttu-id="4a846-102">Свойство Document.LastUpdated (DAO)</span><span class="sxs-lookup"><span data-stu-id="4a846-102">Document.LastUpdated property (DAO)</span></span>


<span data-ttu-id="4a846-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4a846-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4a846-104">Возвращает дату и время последнего изменения, внесенные в объект.</span><span class="sxs-lookup"><span data-stu-id="4a846-104">Returns the date and time of the most recent change made to an object.</span></span> <span data-ttu-id="4a846-105">Только для чтения, **Variant**.</span><span class="sxs-lookup"><span data-stu-id="4a846-105">Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a846-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4a846-106">Syntax</span></span>

<span data-ttu-id="4a846-107">*выражение* . LastUpdated</span><span class="sxs-lookup"><span data-stu-id="4a846-107">*expression* .LastUpdated</span></span>

<span data-ttu-id="4a846-108">*выражение* Переменная, которая представляет собой объект- **документов** .</span><span class="sxs-lookup"><span data-stu-id="4a846-108">*expression* A variable that represents a **Document** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a846-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="4a846-109">Remarks</span></span>

<span data-ttu-id="4a846-110">**DateCreated** и **LastUpdated** возвращают дату и время создания или последнего обновления.</span><span class="sxs-lookup"><span data-stu-id="4a846-110">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated.</span></span> <span data-ttu-id="4a846-111">В многопользовательской среде пользователи должны получить эти параметры непосредственно из файлового сервера, чтобы избежать несоответствия в DateCreated и параметры свойства LastUpdated.</span><span class="sxs-lookup"><span data-stu-id="4a846-111">In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

