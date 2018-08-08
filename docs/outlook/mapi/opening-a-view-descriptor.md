---
title: Открытие представления дескриптора
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1940feb0-9e0f-4d96-9fb9-b9a35a0aa661
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 525c817cfc3bdcf96455d35025e85486ec8b5b42
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810059"
---
# <a name="opening-a-view-descriptor"></a><span data-ttu-id="f1179-103">Открытие представления дескриптора</span><span class="sxs-lookup"><span data-stu-id="f1179-103">Opening a view descriptor</span></span>
  
<span data-ttu-id="f1179-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f1179-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f1179-105">Большое число папок могут быть открыты в обычном режиме, представление по умолчанию или любое количество личных представлений.</span><span class="sxs-lookup"><span data-stu-id="f1179-105">Many folders can be opened with a normal view, a default view, or any number of personalized views.</span></span> <span data-ttu-id="f1179-106">Представление описывает способ отображения содержимого папки.</span><span class="sxs-lookup"><span data-stu-id="f1179-106">A view describes how to display the contents of a folder.</span></span> <span data-ttu-id="f1179-107">Стандартное представление используется, когда нет альтернативные представления и при открытии папки в первый раз.</span><span class="sxs-lookup"><span data-stu-id="f1179-107">The normal view is used when there is no alternative view and when you are opening the folder for the first time.</span></span> <span data-ttu-id="f1179-108">При альтернативное представление существует, его необходимо использовать для откройте папку.</span><span class="sxs-lookup"><span data-stu-id="f1179-108">When an alternative view does exist, you must use it to open the folder.</span></span>
  
<span data-ttu-id="f1179-109">Представление описан в сообщении, называемый дескриптором представления.</span><span class="sxs-lookup"><span data-stu-id="f1179-109">A view is described in a message known as a view descriptor.</span></span> <span data-ttu-id="f1179-110">Просмотр дескрипторы обычно создаются в качестве связанного сообщения и может отображаться в папках распространенных или личном представлении или в любой папке IPM.</span><span class="sxs-lookup"><span data-stu-id="f1179-110">View descriptors are typically created as associated messages and can appear in either the common or personal view folders or in any IPM folder.</span></span>
  
### <a name="to-open-a-view-descriptor"></a><span data-ttu-id="f1179-111">Чтобы открыть представление дескриптора</span><span class="sxs-lookup"><span data-stu-id="f1179-111">To open a view descriptor</span></span>
  
1. <span data-ttu-id="f1179-112">Вызов [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) для получения таблицы связанного содержимого папки.</span><span class="sxs-lookup"><span data-stu-id="f1179-112">Call [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) to retrieve the associated contents table for the folder.</span></span> 
    
2. <span data-ttu-id="f1179-113">Создание ограничение, которое находит только сообщения с классом сообщения, зарезервировано для представления дескрипторов и вызова [IMAPITable::Restrict](imapitable-restrict.md) для ограничения в таблице и [IMAPITable::QueryRows](imapitable-queryrows.md) для получения соответствующих строк или...</span><span class="sxs-lookup"><span data-stu-id="f1179-113">Create a restriction that locates only messages with the message class reserved for view descriptors and call [IMAPITable::Restrict](imapitable-restrict.md) to limit the table and [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve the appropriate rows, or...</span></span>
    
   <span data-ttu-id="f1179-114">Вызов метода [IMAPIProp::GetProps](imapiprop-getprops.md) папки для получения его свойство **PR_DEFAULT_VIEW_ENTRYID** ([PidTagDefaultViewEntryId](pidtagdefaultviewentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f1179-114">Call the folder's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_DEFAULT_VIEW_ENTRYID** ([PidTagDefaultViewEntryId](pidtagdefaultviewentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="f1179-115">**PR_DEFAULT_VIEW_ENTRYID** содержит идентификатор записи на сообщение, содержащее дескриптор представления по умолчанию для папки.</span><span class="sxs-lookup"><span data-stu-id="f1179-115">**PR_DEFAULT_VIEW_ENTRYID** contains the entry identifier for the message containing the default view descriptor for a folder.</span></span> <span data-ttu-id="f1179-116">Этот звонок будет выполнено, если папка поддерживает использование флаг MAPI_ASSOCIATED на вызовы [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) и [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md).</span><span class="sxs-lookup"><span data-stu-id="f1179-116">This call will succeed if the folder supports the use of the MAPI_ASSOCIATED flag on calls to [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) and [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md).</span></span>
    
3. <span data-ttu-id="f1179-117">Вызов [IMsgStore::OpenEntry](imsgstore-openentry.md) с идентификатором записи дескриптора представление, чтобы открыть его.</span><span class="sxs-lookup"><span data-stu-id="f1179-117">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) with the entry identifier of the view descriptor to open it.</span></span> 
    

