---
title: Удаление сообщения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9ed166b4-6b7b-478f-bbe5-4115bb818ac0
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 663eebfcd1b8862b22d8c822957024c4f31499de
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433166"
---
# <a name="deleting-a-message"></a><span data-ttu-id="079a2-103">Удаление сообщения</span><span class="sxs-lookup"><span data-stu-id="079a2-103">Deleting a Message</span></span>

  
  
<span data-ttu-id="079a2-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="079a2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="079a2-105">Клиент может удалить сообщение, когда оно открыто и пользователь его просматривает, или когда он закрывается, и пользователь просматривает таблицу содержимого.</span><span class="sxs-lookup"><span data-stu-id="079a2-105">A client can delete a message when it is open and the user is reading it, or when it is closed and the user is viewing the contents table.</span></span> <span data-ttu-id="079a2-106">Чтобы предотвратить случайное удаление сообщения пользователем, MAPI определяет удаление сообщения в ходе выполнения двух этапов:</span><span class="sxs-lookup"><span data-stu-id="079a2-106">To protect a user from inadvertently removing a message, MAPI defines message deletion as a two step process:</span></span>
  
1. <span data-ttu-id="079a2-107">ПоМетить сообщение для удаления, переместив его в папку, которая была назначена в качестве папки "Удаленные" — папка, идентификатор записи которой хранится в свойстве **пр_ипм_вастебаскет_ентрид** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="079a2-107">Mark a message for deletion by moving it to the folder that has been designated as the Deleted Items folder — the folder whose entry identifier is stored in the **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) property.</span></span> 
    
2. <span data-ttu-id="079a2-108">Удалите сообщение, вызвав метод [IMAPIFolder::D елетемессажес](imapifolder-deletemessages.md) .</span><span class="sxs-lookup"><span data-stu-id="079a2-108">Remove the message by calling the [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md) method.</span></span> 
    
<span data-ttu-id="079a2-109">Когда пользователь выбирает удаление сообщения из папки, отличной от папки "Удаленные", помечайте ее для удаления.</span><span class="sxs-lookup"><span data-stu-id="079a2-109">When a user chooses to delete a message in a folder other than the Deleted Items folder, mark it for deletion.</span></span> <span data-ttu-id="079a2-110">Только когда пользователь выбирает сообщения из папки "Удаленные", должны ли сообщения физически удаляться с рабочей станции.</span><span class="sxs-lookup"><span data-stu-id="079a2-110">Only when a user selects messages from within the Deleted Items folder should the messages be physically removed from the workstation.</span></span> <span data-ttu-id="079a2-111">Вы можете предложить пользователю подтвердить, что пользователь действительно предназначен для выполнения удаления.</span><span class="sxs-lookup"><span data-stu-id="079a2-111">You can prompt the user to verify that the user really intended to perform the deletion.</span></span>
  
 <span data-ttu-id="079a2-112">**Удаление сообщения**</span><span class="sxs-lookup"><span data-stu-id="079a2-112">**To delete a message**</span></span>
  
1. <span data-ttu-id="079a2-113">Выясните у пользователя, что преднамеренное удаление преднамерено.</span><span class="sxs-lookup"><span data-stu-id="079a2-113">Confirm with the user that the impending deletion is intentional.</span></span>
    
2. <span data-ttu-id="079a2-114">Определите родительский объект удаляемой папки.</span><span class="sxs-lookup"><span data-stu-id="079a2-114">Determine the parent of the folder to be deleted.</span></span> <span data-ttu-id="079a2-115">Если это папка "Удаленные" или вложенная папка в папке "Удаленные", вызовите [IMAPIFolder::D елетемессажес](imapifolder-deletemessages.md) , чтобы удалить сообщение.</span><span class="sxs-lookup"><span data-stu-id="079a2-115">If it is the Deleted Items folder or a subfolder within the Deleted Items folder, call [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md) to remove the message.</span></span> 
    
3. <span data-ttu-id="079a2-116">Если папка не находится в папке "Удаленные", вызовите [IMAPIFolder:: копимессажес](imapifolder-copymessages.md) с установленным флагом мессаже_мове, чтобы переместить сообщение в папку "Удаленные".</span><span class="sxs-lookup"><span data-stu-id="079a2-116">If the folder is not contained within the Deleted Items folder, call [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) with the MESSAGE_MOVE flag set to relocate the message to the Deleted Items folder.</span></span> 
    

