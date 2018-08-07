---
title: PROP_ACCT_PREFERENCES_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ec0aac33-624e-48f7-8177-8f7b8db6af7d
description: Получает уникальный идентификатор (UID) для раздела профиля, в которой хранятся параметры учетной записи.
ms.openlocfilehash: 70e61264e5525f26e9f52e402bc785b544a0b90e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807949"
---
# <a name="propacctpreferencesuid"></a><span data-ttu-id="04408-103">PROP_ACCT_PREFERENCES_UID</span><span class="sxs-lookup"><span data-stu-id="04408-103">PROP_ACCT_PREFERENCES_UID</span></span>

<span data-ttu-id="04408-104">Получает уникальный идентификатор (UID) для раздела профиля, в которой хранятся параметры учетной записи.</span><span class="sxs-lookup"><span data-stu-id="04408-104">Retrieves the unique identifier (UID) for the profile section that stores the account preferences.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="04408-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="04408-105">Quick info</span></span>

<span data-ttu-id="04408-106">В разделе [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="04408-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="04408-107">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="04408-107">Identifier:</span></span>  <br/> |<span data-ttu-id="04408-108">0x0022</span><span class="sxs-lookup"><span data-stu-id="04408-108">0x0022</span></span>  <br/> |
|<span data-ttu-id="04408-109">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="04408-109">Property type:</span></span>  <br/> |<span data-ttu-id="04408-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="04408-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="04408-111">Свойство tag:</span><span class="sxs-lookup"><span data-stu-id="04408-111">Property tag:</span></span>  <br/> |<span data-ttu-id="04408-112">0x00220102</span><span class="sxs-lookup"><span data-stu-id="04408-112">0x00220102</span></span>  <br/> |
|<span data-ttu-id="04408-113">Access:</span><span class="sxs-lookup"><span data-stu-id="04408-113">Access:</span></span>  <br/> |<span data-ttu-id="04408-114">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="04408-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="04408-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="04408-115">Remarks</span></span>

<span data-ttu-id="04408-116">Используйте **PROP_ACCT_PREFERENCES_UID** вызовы [IMAPISupport::OpenProfileSection](http://msdn.microsoft.com/library/cd1fa994-9531-46c4-94e5-505e7f90b884%28Office.15%29.aspx) для получения раздела профиля, который содержит параметры учетной записи.</span><span class="sxs-lookup"><span data-stu-id="04408-116">Use **PROP_ACCT_PREFERENCES_UID** in calls to [IMAPISupport::OpenProfileSection](http://msdn.microsoft.com/library/cd1fa994-9531-46c4-94e5-505e7f90b884%28Office.15%29.aspx) to retrieve the profile section that contains account preferences.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="04408-117">См. также</span><span class="sxs-lookup"><span data-stu-id="04408-117">See also</span></span>

- [<span data-ttu-id="04408-118">About the Account Management API</span><span class="sxs-lookup"><span data-stu-id="04408-118">About the Account Management API</span></span>](about-the-account-management-api.md)
- [<span data-ttu-id="04408-119">About anti-spam settings</span><span class="sxs-lookup"><span data-stu-id="04408-119">About anti-spam settings</span></span>](about-anti-spam-settings.md)

