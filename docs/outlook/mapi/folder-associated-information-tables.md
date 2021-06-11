---
title: Folder-Associated информационные таблицы
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b72a0d36-c489-41d6-af57-72fbf4b7a3f5
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 2332c2a2f7eb46816eab5305b73344e25b2832d7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426417"
---
# <a name="folder-associated-information-tables"></a><span data-ttu-id="8d669-103">Folder-Associated информационные таблицы</span><span class="sxs-lookup"><span data-stu-id="8d669-103">Folder-Associated Information Tables</span></span>

  
  
<span data-ttu-id="8d669-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8d669-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8d669-105">MAPI определяет флаг MAPI_ASSOCIATED для различных компонентов MAPI, которые необходимо использовать при работе с связанными таблицами информации.</span><span class="sxs-lookup"><span data-stu-id="8d669-105">MAPI defines the MAPI_ASSOCIATED flag for various MAPI components to use when dealing with associated information tables.</span></span> <span data-ttu-id="8d669-106">Каждая папка в хранилище сообщений должна иметь связанную таблицу содержимого вместе со стандартной таблицей содержимого.</span><span class="sxs-lookup"><span data-stu-id="8d669-106">Each folder in a message store should have an associated contents table along with its standard contents table.</span></span> <span data-ttu-id="8d669-107">Клиентские приложения хранят специальные сообщения в связанной таблице содержимого папки для хранения форм и представлений.</span><span class="sxs-lookup"><span data-stu-id="8d669-107">Client applications store special messages in a folder's associated contents table to hold forms and views.</span></span> <span data-ttu-id="8d669-108">Фактически для поддержки форм и представлений поставщик магазина сообщений должен реализовать связанные таблицы контента.</span><span class="sxs-lookup"><span data-stu-id="8d669-108">In fact, to support forms and views, your message store provider must implement associated contents tables.</span></span>
  
<span data-ttu-id="8d669-109">Чтобы реализовать связанные таблицы контента, поставщик магазина должен выполнить следующие меры:</span><span class="sxs-lookup"><span data-stu-id="8d669-109">To implement associated contents tables, your store provider must do the following:</span></span>
  
- <span data-ttu-id="8d669-110">Поддержка флага MAPI_ASSOCIATED в методе [IMAPIContainer::GetContentsTable,](imapicontainer-getcontentstable.md) чтобы клиентские приложения могли получать связанную таблицу содержимого папки вместо стандартной таблицы содержимого.</span><span class="sxs-lookup"><span data-stu-id="8d669-110">Support the MAPI_ASSOCIATED flag in the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method so client applications can get the folder's associated contents table instead of the standard contents table.</span></span> 
    
- <span data-ttu-id="8d669-111">Поддержка флага MAPI_ASSOCIATED в методе [IMAPIFolder::CreateMessage,](imapifolder-createmessage.md) чтобы клиентские приложения могли добавлять сообщения в связанную таблицу содержимого папки.</span><span class="sxs-lookup"><span data-stu-id="8d669-111">Support the MAPI_ASSOCIATED flag in the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method so client applications can add messages to a folder's associated contents table.</span></span> 
    
- <span data-ttu-id="8d669-112">Установите MAPI_ACCESS_CREATE_ASSOCIATED в **свойстве PR_ACCESS** [(PidTagAccess)](pidtagaccess-canonical-property.md)на объектах папок.</span><span class="sxs-lookup"><span data-stu-id="8d669-112">Set the MAPI_ACCESS_CREATE_ASSOCIATED bit in the **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) property on folder objects.</span></span>
    
- <span data-ttu-id="8d669-113">Поддержка флага DEL_ASSOCIATED в [методе IMAPIFolder::EmptyFolder.](imapifolder-emptyfolder.md)</span><span class="sxs-lookup"><span data-stu-id="8d669-113">Support the DEL_ASSOCIATED flag in the [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md) method.</span></span> 
    
- <span data-ttu-id="8d669-114">Установите MSGFLAG_ASSOCIATED в **свойстве PR_MESSAGE_FLAGS** [(PidTagMessageFlags)](pidtagmessageflags-canonical-property.md)для сообщений в связанной таблице содержимого.</span><span class="sxs-lookup"><span data-stu-id="8d669-114">Set the MSGFLAG_ASSOCIATED bit in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property for messages in the associated contents table.</span></span>
    
- <span data-ttu-id="8d669-115">Подвергайте и реагируйте на **свойство PR_FOLDER_ASSOCIATED_CONTENTS** [(PidTagFolderAssociatedContents)](pidtagfolderassociatedcontents-canonical-property.md)в папках.</span><span class="sxs-lookup"><span data-stu-id="8d669-115">Expose and respond to the **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) property on folders.</span></span>
    
- <span data-ttu-id="8d669-116">Сохранение **свойства PR_ASSOC_CONTENT_COUNT** [(PidTagAssociatedContentCount)](pidtagassociatedcontentcount-canonical-property.md)в папках.</span><span class="sxs-lookup"><span data-stu-id="8d669-116">Maintain the **PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md)) property on folders.</span></span>
    
<span data-ttu-id="8d669-117">В свойстве **PR_STORE_SUPPORT_MASK** [(PidTagStoreSupportMask)](pidtagstoresupportmask-canonical-property.md)нет бита, чтобы указать, поддерживает ли поставщик магазина сообщений связанные таблицы контента.</span><span class="sxs-lookup"><span data-stu-id="8d669-117">There is no bit in the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property to indicate whether your message store provider supports associated contents tables.</span></span> <span data-ttu-id="8d669-118">Если поставщик магазина сообщений не поддерживает их, он должен возвращать MAPI_E_NO_SUPPORT, когда клиентские приложения звонят любым из вышеуказанных методов с MAPI_ASSOCIATED флагом.</span><span class="sxs-lookup"><span data-stu-id="8d669-118">If your message store provider does not support them, it should return MAPI_E_NO_SUPPORT when client applications call any of the above methods with the MAPI_ASSOCIATED flag.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8d669-119">См. также</span><span class="sxs-lookup"><span data-stu-id="8d669-119">See also</span></span>



[<span data-ttu-id="8d669-120">���������� ��������� ���������</span><span class="sxs-lookup"><span data-stu-id="8d669-120">Message Store Features</span></span>](message-store-features.md)

