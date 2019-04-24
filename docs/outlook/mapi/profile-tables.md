---
title: Таблицы профилей
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cd8d60df-98fb-4e08-b547-0836bb31be79
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 15c07c05af82389bce697c300cd9b1d504e98736
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328562"
---
# <a name="profile-tables"></a><span data-ttu-id="ee55b-103">Таблицы профилей</span><span class="sxs-lookup"><span data-stu-id="ee55b-103">Profile Tables</span></span>

  
  
<span data-ttu-id="ee55b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ee55b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ee55b-105">В таблице Profile перечисляются сведения обо всех профилях, связанных с определенным клиентским приложением.</span><span class="sxs-lookup"><span data-stu-id="ee55b-105">The profile table lists information about all profiles associated with a particular client application.</span></span> <span data-ttu-id="ee55b-106">Для каждого сеанса существует одна таблица профилей, реализованная MAPI для использования клиентами.</span><span class="sxs-lookup"><span data-stu-id="ee55b-106">There is one profile table for every session, implemented by MAPI for use by clients.</span></span> 
  
<span data-ttu-id="ee55b-107">Клиенты получают доступ к таблице профилей, вызывая метод [ипрофадмин:: жетпрофилетабле](iprofadmin-getprofiletable.md) .</span><span class="sxs-lookup"><span data-stu-id="ee55b-107">Clients access the profile table by calling the [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) method.</span></span> 
  
<span data-ttu-id="ee55b-108">Таблица Profile является статической таблицей.</span><span class="sxs-lookup"><span data-stu-id="ee55b-108">The profile table is a static table.</span></span> <span data-ttu-id="ee55b-109">Профили, помеченные для удаления, не включаются в таблицу профилей.</span><span class="sxs-lookup"><span data-stu-id="ee55b-109">Profiles that have been marked for deletion are not included in the profile table.</span></span>
  
<span data-ttu-id="ee55b-110">Как и в большинстве реализаций таблиц, если **жетпрофилетабле** вызывается, а для клиента нет доступных профилей, таблица создается с нулевым количеством строк.</span><span class="sxs-lookup"><span data-stu-id="ee55b-110">As with most table implementations, if **GetProfileTable** is called and there are no profiles available to the client, the table is created with zero rows.</span></span> 
  
<span data-ttu-id="ee55b-111">Следующие свойства составляют обязательный набор столбцов в таблицах профилей:</span><span class="sxs-lookup"><span data-stu-id="ee55b-111">The following properties make up the required column set in profile tables:</span></span>
  
 <span data-ttu-id="ee55b-112">**Пр_дефаулт_профиле** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ee55b-112">**PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md))</span></span> 
  
 <span data-ttu-id="ee55b-113">**Пр_дисплай_наме** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ee55b-113">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ee55b-114">См. также</span><span class="sxs-lookup"><span data-stu-id="ee55b-114">See also</span></span>



[<span data-ttu-id="ee55b-115">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="ee55b-115">MAPI Tables</span></span>](mapi-tables.md)

