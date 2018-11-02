---
title: Свойство Document.LastUpdated (DAO)
TOCTitle: LastUpdated Property
ms:assetid: 9307ceee-095f-0364-fd5b-905bc523b9c0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197661(v=office.15)
ms:contentKeyID: 48546388
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 57fb558330c602206831c1c72f09a13094eba799
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927314"
---
# <a name="documentlastupdated-property-dao"></a><span data-ttu-id="4e21b-102">Свойство Document.LastUpdated (DAO)</span><span class="sxs-lookup"><span data-stu-id="4e21b-102">Document.LastUpdated property (DAO)</span></span>


<span data-ttu-id="4e21b-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4e21b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4e21b-104">Возвращает дату и время последнего изменения, внесенные в объект.</span><span class="sxs-lookup"><span data-stu-id="4e21b-104">Returns the date and time of the most recent change made to an object.</span></span> <span data-ttu-id="4e21b-105">Только для чтения **Variant**.</span><span class="sxs-lookup"><span data-stu-id="4e21b-105">Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e21b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4e21b-106">Syntax</span></span>

<span data-ttu-id="4e21b-107">*выражение* . LastUpdated</span><span class="sxs-lookup"><span data-stu-id="4e21b-107">*expression* .LastUpdated</span></span>

<span data-ttu-id="4e21b-108">*выражение* Переменная, которая представляет собой объект- **документов** .</span><span class="sxs-lookup"><span data-stu-id="4e21b-108">*expression* A variable that represents a **Document** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e21b-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="4e21b-109">Remarks</span></span>

<span data-ttu-id="4e21b-110">**DateCreated** и **LastUpdated** возвращают дату и время создания или последнего обновления.</span><span class="sxs-lookup"><span data-stu-id="4e21b-110">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated.</span></span> <span data-ttu-id="4e21b-111">В многопользовательской среде пользователи должны получить эти параметры непосредственно из файлового сервера, чтобы избежать несоответствия в DateCreated и параметры свойства LastUpdated.</span><span class="sxs-lookup"><span data-stu-id="4e21b-111">In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

