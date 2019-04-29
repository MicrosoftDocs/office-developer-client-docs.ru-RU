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
ms.openlocfilehash: 2332c2a2f7eb46816eab5305b73344e25b2832d7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426417"
---
# <a name="folder-associated-information-tables"></a><span data-ttu-id="68a91-103">Таблицы сведений, связанных с папками</span><span class="sxs-lookup"><span data-stu-id="68a91-103">Folder-Associated Information Tables</span></span>

  
  
<span data-ttu-id="68a91-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="68a91-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="68a91-105">MAPI определяет флаг МАПИ_АССОЦИАТЕД для различных компонентов MAPI, используемых при работе со связанными таблицами сведений.</span><span class="sxs-lookup"><span data-stu-id="68a91-105">MAPI defines the MAPI_ASSOCIATED flag for various MAPI components to use when dealing with associated information tables.</span></span> <span data-ttu-id="68a91-106">Каждая папка в хранилище сообщений должна содержать связанную таблицу с содержимым, а также ее стандартные таблицы контента.</span><span class="sxs-lookup"><span data-stu-id="68a91-106">Each folder in a message store should have an associated contents table along with its standard contents table.</span></span> <span data-ttu-id="68a91-107">Клиентские приложения хранят специальные сообщения в таблице содержимого, связанной с папкой, для хранения форм и представлений.</span><span class="sxs-lookup"><span data-stu-id="68a91-107">Client applications store special messages in a folder's associated contents table to hold forms and views.</span></span> <span data-ttu-id="68a91-108">В действительности для поддержки форм и представлений поставщик хранилища сообщений должен реализовать связанные таблицы содержимого.</span><span class="sxs-lookup"><span data-stu-id="68a91-108">In fact, to support forms and views, your message store provider must implement associated contents tables.</span></span>
  
<span data-ttu-id="68a91-109">Для реализации связанных таблиц содержимого поставщик магазина должен выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="68a91-109">To implement associated contents tables, your store provider must do the following:</span></span>
  
- <span data-ttu-id="68a91-110">Поддерживает флаг МАПИ_АССОЦИАТЕД в методе [IMAPIContainer:: жетконтентстабле](imapicontainer-getcontentstable.md) , чтобы клиентские приложения могли получить связанную с папкой таблицу содержимого, а не стандартные таблицы содержимого.</span><span class="sxs-lookup"><span data-stu-id="68a91-110">Support the MAPI_ASSOCIATED flag in the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method so client applications can get the folder's associated contents table instead of the standard contents table.</span></span> 
    
- <span data-ttu-id="68a91-111">Поддерживает флаг МАПИ_АССОЦИАТЕД в методе [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) , чтобы клиентские приложения могли добавлять сообщения в таблицу с содержимым, связанным с папкой.</span><span class="sxs-lookup"><span data-stu-id="68a91-111">Support the MAPI_ASSOCIATED flag in the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method so client applications can add messages to a folder's associated contents table.</span></span> 
    
- <span data-ttu-id="68a91-112">Установите бит МАПИ_АКЦЕСС_КРЕАТЕ_АССОЦИАТЕД в свойстве \*\*пр_акцесс\*\* ([PidTagAccess](pidtagaccess-canonical-property.md)) для объектов Folder.</span><span class="sxs-lookup"><span data-stu-id="68a91-112">Set the MAPI_ACCESS_CREATE_ASSOCIATED bit in the **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) property on folder objects.</span></span>
    
- <span data-ttu-id="68a91-113">Поддерживает флаг ДЕЛ_АССОЦИАТЕД в методе [IMAPIFolder:: EmptyFolder](imapifolder-emptyfolder.md) .</span><span class="sxs-lookup"><span data-stu-id="68a91-113">Support the DEL_ASSOCIATED flag in the [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md) method.</span></span> 
    
- <span data-ttu-id="68a91-114">Установите бит МСГФЛАГ_АССОЦИАТЕД в свойстве \*\*пр_мессаже_флагс\*\* ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) для сообщений в связанной таблице содержимого.</span><span class="sxs-lookup"><span data-stu-id="68a91-114">Set the MSGFLAG_ASSOCIATED bit in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property for messages in the associated contents table.</span></span>
    
- <span data-ttu-id="68a91-115">Предоставление и ответ на свойство **пр_фолдер_ассоЦиатед_контентс** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) в папках.</span><span class="sxs-lookup"><span data-stu-id="68a91-115">Expose and respond to the **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) property on folders.</span></span>
    
- <span data-ttu-id="68a91-116">Настройте свойство **пр_ассок_контент_каунт** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md)) для папок.</span><span class="sxs-lookup"><span data-stu-id="68a91-116">Maintain the **PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md)) property on folders.</span></span>
    
<span data-ttu-id="68a91-117">В свойстве **пр_сторе_суппорт_маск** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) отсутствует бит, указывающий, поддерживает ли поставщик хранилища сообщений связанные таблицы содержимого.</span><span class="sxs-lookup"><span data-stu-id="68a91-117">There is no bit in the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property to indicate whether your message store provider supports associated contents tables.</span></span> <span data-ttu-id="68a91-118">Если поставщик хранилища сообщений не поддерживает их, он должен возвратить МАПИ_Е_НО_СУППОРТ, когда клиентские приложения вызывают любой из вышеупомянутых методов с флагом МАПИ_АССОЦИАТЕД.</span><span class="sxs-lookup"><span data-stu-id="68a91-118">If your message store provider does not support them, it should return MAPI_E_NO_SUPPORT when client applications call any of the above methods with the MAPI_ASSOCIATED flag.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="68a91-119">См. также</span><span class="sxs-lookup"><span data-stu-id="68a91-119">See also</span></span>



[<span data-ttu-id="68a91-120">���������� ��������� ���������</span><span class="sxs-lookup"><span data-stu-id="68a91-120">Message Store Features</span></span>](message-store-features.md)

