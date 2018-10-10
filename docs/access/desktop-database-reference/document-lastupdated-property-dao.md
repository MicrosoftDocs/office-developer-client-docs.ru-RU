---
title: Document.LastUpdated Property (DAO)
TOCTitle: LastUpdated Property
ms:assetid: 9307ceee-095f-0364-fd5b-905bc523b9c0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197661(v=office.15)
ms:contentKeyID: 48546388
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f8192dc32554b29c9fe024f34f08757cb512aa5b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483020"
---
# <a name="documentlastupdated-property-dao"></a><span data-ttu-id="62743-102">Document.LastUpdated Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="62743-102">Document.LastUpdated Property (DAO)</span></span>


<span data-ttu-id="62743-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="62743-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="62743-104">Возвращает дату и время последнего изменения, внесенные в объект.</span><span class="sxs-lookup"><span data-stu-id="62743-104">Returns the date and time of the most recent change made to an object.</span></span> <span data-ttu-id="62743-105">Только для чтения **Variant**.</span><span class="sxs-lookup"><span data-stu-id="62743-105">Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="62743-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62743-106">Syntax</span></span>

<span data-ttu-id="62743-107">*выражение* . LastUpdated</span><span class="sxs-lookup"><span data-stu-id="62743-107">*expression* .LastUpdated</span></span>

<span data-ttu-id="62743-108">*выражение* Переменная, которая представляет собой объект- **документов** .</span><span class="sxs-lookup"><span data-stu-id="62743-108">*expression* A variable that represents a **Document** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="62743-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="62743-109">Remarks</span></span>

<span data-ttu-id="62743-110">**DateCreated** и **LastUpdated** возвращают дату и время создания или последнего обновления.</span><span class="sxs-lookup"><span data-stu-id="62743-110">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated.</span></span> <span data-ttu-id="62743-111">В многопользовательской среде пользователи должны получить эти параметры непосредственно из файлового сервера, чтобы избежать несоответствия в DateCreated и параметры свойства LastUpdated.</span><span class="sxs-lookup"><span data-stu-id="62743-111">In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

