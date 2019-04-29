---
title: Копирование профиля
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b722a157-0d92-404d-9075-39547241dbb7
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 86f381eff1dab0144afe0f94dcd6dd54d1ad7fa8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424730"
---
# <a name="copying-a-profile"></a><span data-ttu-id="eb6a1-103">Копирование профиля</span><span class="sxs-lookup"><span data-stu-id="eb6a1-103">Copying a Profile</span></span>

  
  
<span data-ttu-id="eb6a1-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eb6a1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eb6a1-105">Один из способов создания профиля — копирование из существующего профиля и изменение необходимых служб сообщений и поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="eb6a1-105">One way to create a profile is to copy from an existing profile and alter the necessary message services and service providers.</span></span> <span data-ttu-id="eb6a1-106">Копирование профиля включает в себя использование объекта администрирования профиля, предоставляемого MAPI с помощью функции [мапиадминпрофилес](mapiadminprofiles.md) .</span><span class="sxs-lookup"><span data-stu-id="eb6a1-106">Copying a profile involves using a profile administration object, provided by MAPI through the [MAPIAdminProfiles](mapiadminprofiles.md) function.</span></span> 
  
 <span data-ttu-id="eb6a1-107">**Копирование профиля**</span><span class="sxs-lookup"><span data-stu-id="eb6a1-107">**To copy a profile**</span></span>
  
1. <span data-ttu-id="eb6a1-108">ВыЗовите **мапиадминпрофилес** , чтобы получить указатель интерфейса **ипрофадмин** .</span><span class="sxs-lookup"><span data-stu-id="eb6a1-108">Call **MAPIAdminProfiles** to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
2. <span data-ttu-id="eb6a1-109">Call [ипрофадмин:: жетпрофилетабле](iprofadmin-getprofiletable.md) для доступа к таблице профилей.</span><span class="sxs-lookup"><span data-stu-id="eb6a1-109">Call [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) to access the profile table.</span></span> 
    
3. <span data-ttu-id="eb6a1-110">Создайте ограничение свойства с помощью структуры [спропертирестриктион](spropertyrestriction.md) для сравнения **пр_дисплай_наме** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) с именем профиля, который необходимо скопировать.</span><span class="sxs-lookup"><span data-stu-id="eb6a1-110">Build a property restriction with an [SPropertyRestriction](spropertyrestriction.md) structure to match **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) with the name of the profile to be copied.</span></span> 
    
4. <span data-ttu-id="eb6a1-111">Call [IMAPITable:: FindRow](imapitable-findrow.md) для обнаружения соответствующей строки в таблице Profile.</span><span class="sxs-lookup"><span data-stu-id="eb6a1-111">Call [IMAPITable::FindRow](imapitable-findrow.md) to locate the appropriate row in the profile table.</span></span> 
    
5. <span data-ttu-id="eb6a1-112">Call [ипрофадмин:: копипрофиле](iprofadmin-copyprofile.md), передавая значение столбца **пр_дисплай_наме** в качестве параметра _лпсзолдпрофиленаме_ .</span><span class="sxs-lookup"><span data-stu-id="eb6a1-112">Call [IProfAdmin::CopyProfile](iprofadmin-copyprofile.md), passing the value of the **PR_DISPLAY_NAME** column as the  _lpszOldProfileName_ parameter.</span></span> 
    

