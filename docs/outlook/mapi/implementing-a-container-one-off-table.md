---
title: Реализация одноразовой таблицы контейнера
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eabbde74-49a1-4eeb-a01d-67e45ae4b343
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 72dc73b6ed8519be2d8010544fdd5dc5b7b0f759
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332888"
---
# <a name="implementing-a-container-one-off-table"></a><span data-ttu-id="a3d91-103">Реализация одноразовой таблицы контейнера</span><span class="sxs-lookup"><span data-stu-id="a3d91-103">Implementing a Container One-Off Table</span></span>

  
  
<span data-ttu-id="a3d91-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a3d91-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a3d91-105">Для доступа к односторонней таблице, принадлежащей одному из контейнеров, MAPI вызывает метод контейнера [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) , чтобы открыть свойство **пр_креате_темплатес** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) с помощью **IMAPITable** . взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="a3d91-105">To access the one-off table belonging to one of your containers, MAPI calls the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property with the **IMAPITable** interface.</span></span> <span data-ttu-id="a3d91-106">В вашем контейнере предлагается возврат обратной таблицы, когда клиентское приложение пытается добавить получателя в контейнер.</span><span class="sxs-lookup"><span data-stu-id="a3d91-106">Your container is asked to return its one-off table when a client application is trying to add a recipient to the container.</span></span> <span data-ttu-id="a3d91-107">Если контейнер позволяет любому получателю, поставщик может возвратить свою собственную реализацию или вызов [имаписуппорт:: жетонеоффтабле](imapisupport-getoneofftable.md) , чтобы вернуть реализацию MAPI.</span><span class="sxs-lookup"><span data-stu-id="a3d91-107">If the container allows any recipients, your provider can either return its own table implementation or call [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md) to return the MAPI implementation.</span></span> 
  
<span data-ttu-id="a3d91-108">Набор шаблонов в таблице отбираемых контейнеров должен отражать тип получателей, которые могут храниться в определенном контейнере.</span><span class="sxs-lookup"><span data-stu-id="a3d91-108">The set of templates in the container one-off table should reflect the type of recipients that the particular container can hold.</span></span> <span data-ttu-id="a3d91-109">Как правило, это включает один или два шаблона, шаблоны для создания отдельного пользователя обмена сообщениями или списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="a3d91-109">Typically, this includes one or two templates, templates for creating an individual messaging user or a distribution list.</span></span> <span data-ttu-id="a3d91-110">Идентификаторы записей для этих шаблонов хранятся в свойствах **пр_деф_креате_маилусер** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) и **пр_деф_креате_дл** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a3d91-110">The entry identifiers for these templates are held in the **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) and **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)) properties.</span></span> <span data-ttu-id="a3d91-111">Однако контейнеры не ограничиваются этими типами записей.</span><span class="sxs-lookup"><span data-stu-id="a3d91-111">However, containers are by no means limited to these types of entries.</span></span> <span data-ttu-id="a3d91-112">Они могут содержать других типов получателей или записей, отличных от получателей, таких как каталоги.</span><span class="sxs-lookup"><span data-stu-id="a3d91-112">They can hold other types of recipients or non-recipient entries such as directories.</span></span> 
  

