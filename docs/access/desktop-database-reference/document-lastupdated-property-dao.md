---
title: Свойство Document. Ластупдатед (DAO)
TOCTitle: LastUpdated Property
ms:assetid: 9307ceee-095f-0364-fd5b-905bc523b9c0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197661(v=office.15)
ms:contentKeyID: 48546388
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: abb766f7a47cbacaededf65eb2b5e9145bf88c60
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293807"
---
# <a name="documentlastupdated-property-dao"></a><span data-ttu-id="0b576-102">Свойство Document. Ластупдатед (DAO)</span><span class="sxs-lookup"><span data-stu-id="0b576-102">Document.LastUpdated property (DAO)</span></span>


<span data-ttu-id="0b576-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0b576-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0b576-104">Возвращает дату и время последнего изменения, внесенного в объект.</span><span class="sxs-lookup"><span data-stu-id="0b576-104">Returns the date and time of the most recent change made to an object.</span></span> <span data-ttu-id="0b576-105">Только для чтения, **Variant**.</span><span class="sxs-lookup"><span data-stu-id="0b576-105">Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b576-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0b576-106">Syntax</span></span>

<span data-ttu-id="0b576-107">*Expression* . ластупдатед</span><span class="sxs-lookup"><span data-stu-id="0b576-107">*expression* .LastUpdated</span></span>

<span data-ttu-id="0b576-108">*Expression (выражение* ) Переменная, представляющая объект **Document** .</span><span class="sxs-lookup"><span data-stu-id="0b576-108">*expression* A variable that represents a **Document** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b576-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="0b576-109">Remarks</span></span>

<span data-ttu-id="0b576-110">**DateCreated** и **ластупдатед** возвращают дату и время создания или последнего обновления объекта.</span><span class="sxs-lookup"><span data-stu-id="0b576-110">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated.</span></span> <span data-ttu-id="0b576-111">В многопользовательской среде пользователи должны получить эти параметры непосредственно с файлового сервера, чтобы избежать расхождений в параметрах свойств DateCreated и Ластупдатед.</span><span class="sxs-lookup"><span data-stu-id="0b576-111">In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

