---
title: Открытие дескриптора представления
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1940feb0-9e0f-4d96-9fb9-b9a35a0aa661
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: ce53e5a91f6fa340728872457eae7f6514e287aa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413040"
---
# <a name="opening-a-view-descriptor"></a><span data-ttu-id="2c911-103">Открытие дескриптора представления</span><span class="sxs-lookup"><span data-stu-id="2c911-103">Opening a view descriptor</span></span>
  
<span data-ttu-id="2c911-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2c911-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2c911-105">Многие папки можно открыть с обычным представлением, представлением по умолчанию или любым количеством настраиваемых представлений.</span><span class="sxs-lookup"><span data-stu-id="2c911-105">Many folders can be opened with a normal view, a default view, or any number of personalized views.</span></span> <span data-ttu-id="2c911-106">В этом представлении показано, как отобразить содержимое папки.</span><span class="sxs-lookup"><span data-stu-id="2c911-106">A view describes how to display the contents of a folder.</span></span> <span data-ttu-id="2c911-107">Обычное представление используется при отсутствии альтернативного представления и при первом открытии папки.</span><span class="sxs-lookup"><span data-stu-id="2c911-107">The normal view is used when there is no alternative view and when you are opening the folder for the first time.</span></span> <span data-ttu-id="2c911-108">Если альтернативное представление существует, его необходимо использовать для открытия папки.</span><span class="sxs-lookup"><span data-stu-id="2c911-108">When an alternative view does exist, you must use it to open the folder.</span></span>
  
<span data-ttu-id="2c911-109">Представление описывается в сообщении, называемом дескриптором представления.</span><span class="sxs-lookup"><span data-stu-id="2c911-109">A view is described in a message known as a view descriptor.</span></span> <span data-ttu-id="2c911-110">Дескрипторы представлений обычно создаются как связанные сообщения и могут отображаться в папках "Общие" или "личное представление" или в любой папке IPM.</span><span class="sxs-lookup"><span data-stu-id="2c911-110">View descriptors are typically created as associated messages and can appear in either the common or personal view folders or in any IPM folder.</span></span>
  
### <a name="to-open-a-view-descriptor"></a><span data-ttu-id="2c911-111">Открытие дескриптора представления</span><span class="sxs-lookup"><span data-stu-id="2c911-111">To open a view descriptor</span></span>
  
1. <span data-ttu-id="2c911-112">Call [IMAPIContainer:: жетконтентстабле](imapicontainer-getcontentstable.md) , чтобы получить связанную таблицу содержимого для папки.</span><span class="sxs-lookup"><span data-stu-id="2c911-112">Call [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) to retrieve the associated contents table for the folder.</span></span> 
    
2. <span data-ttu-id="2c911-113">Создайте ограничение, которое будет искать только сообщения с классом сообщений, зарезервированным для дескрипторов просмотра и вызовов [IMAPITable:: restrict](imapitable-restrict.md) to Limit для таблицы и [IMAPITable:: QueryRows](imapitable-queryrows.md) для получения соответствующих строк или...</span><span class="sxs-lookup"><span data-stu-id="2c911-113">Create a restriction that locates only messages with the message class reserved for view descriptors and call [IMAPITable::Restrict](imapitable-restrict.md) to limit the table and [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve the appropriate rows, or...</span></span>
    
   <span data-ttu-id="2c911-114">ВыЗовите метод [IMAPIProp::](imapiprop-getprops.md) -PROPS папки, чтобы получить свойство **пр_дефаулт_виев_ентрид** ([PidTagDefaultViewEntryId](pidtagdefaultviewentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="2c911-114">Call the folder's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_DEFAULT_VIEW_ENTRYID** ([PidTagDefaultViewEntryId](pidtagdefaultviewentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="2c911-115">**Пр_дефаулт_виев_ентрид** содержит идентификатор записи для сообщения, содержащего дескриптор представления по умолчанию для папки.</span><span class="sxs-lookup"><span data-stu-id="2c911-115">**PR_DEFAULT_VIEW_ENTRYID** contains the entry identifier for the message containing the default view descriptor for a folder.</span></span> <span data-ttu-id="2c911-116">Этот вызов будет успешным, если папка поддерживает использование флага МАПИ_АССОЦИАТЕД при вызовах [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) и [IMAPIContainer:: жетконтентстабле](imapicontainer-getcontentstable.md).</span><span class="sxs-lookup"><span data-stu-id="2c911-116">This call will succeed if the folder supports the use of the MAPI_ASSOCIATED flag on calls to [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) and [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md).</span></span>
    
3. <span data-ttu-id="2c911-117">Call [IMsgStore:: OpenEntry](imsgstore-openentry.md) с идентификатором элемента дескриптора представления, чтобы открыть его.</span><span class="sxs-lookup"><span data-stu-id="2c911-117">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) with the entry identifier of the view descriptor to open it.</span></span> 
    

