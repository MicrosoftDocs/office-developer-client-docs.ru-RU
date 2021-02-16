---
title: PROP_ACCT_PREFERENCES_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ec0aac33-624e-48f7-8177-8f7b8db6af7d
description: Извлекает уникальный идентификатор (UID) для раздела профиля, в котором хранится настройка учетной записи.
ms.openlocfilehash: 97f1a858c8f58e13b72b8d5f052b35359581b718
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327638"
---
# <a name="prop_acct_preferences_uid"></a><span data-ttu-id="eb50b-103">PROP_ACCT_PREFERENCES_UID</span><span class="sxs-lookup"><span data-stu-id="eb50b-103">PROP_ACCT_PREFERENCES_UID</span></span>

<span data-ttu-id="eb50b-104">Извлекает уникальный идентификатор (UID) для раздела профиля, в котором хранится настройка учетной записи.</span><span class="sxs-lookup"><span data-stu-id="eb50b-104">Retrieves the unique identifier (UID) for the profile section that stores the account preferences.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="eb50b-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="eb50b-105">Quick info</span></span>

<span data-ttu-id="eb50b-106">См. [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="eb50b-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="eb50b-107">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="eb50b-107">Identifier:</span></span>  <br/> |<span data-ttu-id="eb50b-108">0x0022</span><span class="sxs-lookup"><span data-stu-id="eb50b-108">0x0022</span></span>  <br/> |
|<span data-ttu-id="eb50b-109">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="eb50b-109">Property type:</span></span>  <br/> |<span data-ttu-id="eb50b-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="eb50b-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="eb50b-111">Тег свойства:</span><span class="sxs-lookup"><span data-stu-id="eb50b-111">Property tag:</span></span>  <br/> |<span data-ttu-id="eb50b-112">0x00220102</span><span class="sxs-lookup"><span data-stu-id="eb50b-112">0x00220102</span></span>  <br/> |
|<span data-ttu-id="eb50b-113">Access:</span><span class="sxs-lookup"><span data-stu-id="eb50b-113">Access:</span></span>  <br/> |<span data-ttu-id="eb50b-114">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="eb50b-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eb50b-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="eb50b-115">Remarks</span></span>

<span data-ttu-id="eb50b-116">Используйте **PROP_ACCT_PREFERENCES_UID** вызовов [IMAPISupport::OpenProfileSection,](https://msdn.microsoft.com/library/cd1fa994-9531-46c4-94e5-505e7f90b884%28Office.15%29.aspx) чтобы получить раздел профиля, содержащий настройки учетной записи.</span><span class="sxs-lookup"><span data-stu-id="eb50b-116">Use **PROP_ACCT_PREFERENCES_UID** in calls to [IMAPISupport::OpenProfileSection](https://msdn.microsoft.com/library/cd1fa994-9531-46c4-94e5-505e7f90b884%28Office.15%29.aspx) to retrieve the profile section that contains account preferences.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="eb50b-117">См. также</span><span class="sxs-lookup"><span data-stu-id="eb50b-117">See also</span></span>

- [<span data-ttu-id="eb50b-118">Сведения об API управления учетными записями</span><span class="sxs-lookup"><span data-stu-id="eb50b-118">About the Account Management API</span></span>](about-the-account-management-api.md)
- [<span data-ttu-id="eb50b-119">Сведения о параметрах защиты от нежелательной почты</span><span class="sxs-lookup"><span data-stu-id="eb50b-119">About anti-spam settings</span></span>](about-anti-spam-settings.md)

