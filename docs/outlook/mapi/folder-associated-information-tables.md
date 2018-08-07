---
title: Таблицы сведений, связанных с папками
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b72a0d36-c489-41d6-af57-72fbf4b7a3f5
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 09cac591aac9d266571348531e378974b86a3a9d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808465"
---
# <a name="folder-associated-information-tables"></a><span data-ttu-id="1b052-103">Таблицы сведений, связанных с папками</span><span class="sxs-lookup"><span data-stu-id="1b052-103">Folder-Associated Information Tables</span></span>

  
  
<span data-ttu-id="1b052-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1b052-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1b052-105">MAPI определяет флаг MAPI_ASSOCIATED для различных компонентов интерфейса MAPI для использования при работе с таблицами связанные сведения.</span><span class="sxs-lookup"><span data-stu-id="1b052-105">MAPI defines the MAPI_ASSOCIATED flag for various MAPI components to use when dealing with associated information tables.</span></span> <span data-ttu-id="1b052-106">Каждой папке в хранилище сообщений должна быть таблица связанное содержимое вместе с его стандартных содержимое таблицы.</span><span class="sxs-lookup"><span data-stu-id="1b052-106">Each folder in a message store should have an associated contents table along with its standard contents table.</span></span> <span data-ttu-id="1b052-107">Клиентские приложения хранятся специальные сообщения в таблице связанное содержимое папки для хранения формы и представления.</span><span class="sxs-lookup"><span data-stu-id="1b052-107">Client applications store special messages in a folder's associated contents table to hold forms and views.</span></span> <span data-ttu-id="1b052-108">На самом деле для поддержки формы и представления, поставщиком хранилища сообщений необходимо реализовать связанного содержимого таблицы.</span><span class="sxs-lookup"><span data-stu-id="1b052-108">In fact, to support forms and views, your message store provider must implement associated contents tables.</span></span>
  
<span data-ttu-id="1b052-109">Для реализации связанного содержимого таблицы, поставщиком хранилища необходимо выполните следующее:</span><span class="sxs-lookup"><span data-stu-id="1b052-109">To implement associated contents tables, your store provider must do the following:</span></span>
  
- <span data-ttu-id="1b052-110">Поддерживает флаг MAPI_ASSOCIATED в методе [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) , поэтому клиентские приложения можно получить таблицы связанного содержимого папки, а не в таблице стандартных содержимое.</span><span class="sxs-lookup"><span data-stu-id="1b052-110">Support the MAPI_ASSOCIATED flag in the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method so client applications can get the folder's associated contents table instead of the standard contents table.</span></span> 
    
- <span data-ttu-id="1b052-111">Поддерживает флаг MAPI_ASSOCIATED в методе [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) , поэтому клиентские приложения можно добавить сообщения к таблице связанное содержимое папки.</span><span class="sxs-lookup"><span data-stu-id="1b052-111">Support the MAPI_ASSOCIATED flag in the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method so client applications can add messages to a folder's associated contents table.</span></span> 
    
- <span data-ttu-id="1b052-112">Установка бита MAPI_ACCESS_CREATE_ASSOCIATED в свойстве **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) на объектов папок.</span><span class="sxs-lookup"><span data-stu-id="1b052-112">Set the MAPI_ACCESS_CREATE_ASSOCIATED bit in the **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) property on folder objects.</span></span>
    
- <span data-ttu-id="1b052-113">Поддерживает флаг DEL_ASSOCIATED в методе [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md) .</span><span class="sxs-lookup"><span data-stu-id="1b052-113">Support the DEL_ASSOCIATED flag in the [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md) method.</span></span> 
    
- <span data-ttu-id="1b052-114">Задайте MSGFLAG_ASSOCIATED бит в свойстве **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) для сообщений в таблице связанного содержимого.</span><span class="sxs-lookup"><span data-stu-id="1b052-114">Set the MSGFLAG_ASSOCIATED bit in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property for messages in the associated contents table.</span></span>
    
- <span data-ttu-id="1b052-115">Предоставление доступа к и реагировать на свойство **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) для папок.</span><span class="sxs-lookup"><span data-stu-id="1b052-115">Expose and respond to the **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) property on folders.</span></span>
    
- <span data-ttu-id="1b052-116">Ведение свойство **PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md)) для папок.</span><span class="sxs-lookup"><span data-stu-id="1b052-116">Maintain the **PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md)) property on folders.</span></span>
    
<span data-ttu-id="1b052-117">Нет бит отсутствует в свойство **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)), указывающее, поддерживает ли поставщик хранилища сообщений связанного содержимого таблицы.</span><span class="sxs-lookup"><span data-stu-id="1b052-117">There is no bit in the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property to indicate whether your message store provider supports associated contents tables.</span></span> <span data-ttu-id="1b052-118">Если поставщик хранилища сообщений не поддерживает их, она возвращает MAPI_E_NO_SUPPORT при вызове клиентских приложений, приведенных выше способов с флагом MAPI_ASSOCIATED.</span><span class="sxs-lookup"><span data-stu-id="1b052-118">If your message store provider does not support them, it should return MAPI_E_NO_SUPPORT when client applications call any of the above methods with the MAPI_ASSOCIATED flag.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1b052-119">См. также</span><span class="sxs-lookup"><span data-stu-id="1b052-119">See also</span></span>



[<span data-ttu-id="1b052-120">���������� ��������� ���������</span><span class="sxs-lookup"><span data-stu-id="1b052-120">Message Store Features</span></span>](message-store-features.md)

