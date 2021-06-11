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
# <a name="deleting-a-message"></a><span data-ttu-id="1bf32-103">Удаление сообщения</span><span class="sxs-lookup"><span data-stu-id="1bf32-103">Deleting a Message</span></span>

  
  
<span data-ttu-id="1bf32-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1bf32-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1bf32-105">Клиент может удалить сообщение, когда оно открыто и пользователь читает его, или когда оно закрывается и пользователь просматривает таблицу содержимого.</span><span class="sxs-lookup"><span data-stu-id="1bf32-105">A client can delete a message when it is open and the user is reading it, or when it is closed and the user is viewing the contents table.</span></span> <span data-ttu-id="1bf32-106">Чтобы защитить пользователя от непреднамеренного удаления сообщения, MAPI определяет удаление сообщения как двухшаговой процесс:</span><span class="sxs-lookup"><span data-stu-id="1bf32-106">To protect a user from inadvertently removing a message, MAPI defines message deletion as a two step process:</span></span>
  
1. <span data-ttu-id="1bf32-107">Пометить сообщение для удаления, перемещая его в папку, назначенную как папка "Удаленные элементы" — папку, идентификатор записи которой хранится в свойстве **PR_IPM_WASTEBASKET_ENTRYID** [(PidTagIpmWastebasketEntryId).](pidtagipmwastebasketentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="1bf32-107">Mark a message for deletion by moving it to the folder that has been designated as the Deleted Items folder — the folder whose entry identifier is stored in the **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) property.</span></span> 
    
2. <span data-ttu-id="1bf32-108">Удалите сообщение, позвонив по методу [IMAPIFolder::D eleteMessages.](imapifolder-deletemessages.md)</span><span class="sxs-lookup"><span data-stu-id="1bf32-108">Remove the message by calling the [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md) method.</span></span> 
    
<span data-ttu-id="1bf32-109">Если пользователь выбирает удаление сообщения в папке, помимо папки "Удаленные элементы", пометите его для удаления.</span><span class="sxs-lookup"><span data-stu-id="1bf32-109">When a user chooses to delete a message in a folder other than the Deleted Items folder, mark it for deletion.</span></span> <span data-ttu-id="1bf32-110">Только если пользователь выбирает сообщения из папки "Удаленные элементы", они будут физически удалены с рабочей станции.</span><span class="sxs-lookup"><span data-stu-id="1bf32-110">Only when a user selects messages from within the Deleted Items folder should the messages be physically removed from the workstation.</span></span> <span data-ttu-id="1bf32-111">Вы можете побудить пользователя проверить, действительно ли пользователь намеревался выполнить удаление.</span><span class="sxs-lookup"><span data-stu-id="1bf32-111">You can prompt the user to verify that the user really intended to perform the deletion.</span></span>
  
 <span data-ttu-id="1bf32-112">**Удаление сообщения**</span><span class="sxs-lookup"><span data-stu-id="1bf32-112">**To delete a message**</span></span>
  
1. <span data-ttu-id="1bf32-113">Подтвердим с пользователем, что предстоящее удаление является преднамеренным.</span><span class="sxs-lookup"><span data-stu-id="1bf32-113">Confirm with the user that the impending deletion is intentional.</span></span>
    
2. <span data-ttu-id="1bf32-114">Определите родитель папки, которая будет удалена.</span><span class="sxs-lookup"><span data-stu-id="1bf32-114">Determine the parent of the folder to be deleted.</span></span> <span data-ttu-id="1bf32-115">Если это папка "Удаленные элементы" или подмостки в папке "Удаленные элементы", позвоните [в IMAPIFolder::D eleteMessages,](imapifolder-deletemessages.md) чтобы удалить сообщение.</span><span class="sxs-lookup"><span data-stu-id="1bf32-115">If it is the Deleted Items folder or a subfolder within the Deleted Items folder, call [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md) to remove the message.</span></span> 
    
3. <span data-ttu-id="1bf32-116">Если папка не содержится в папке "Удаленные элементы", позвоните [в IMAPIFolder::CopyMessages](imapifolder-copymessages.md) с флагом MESSAGE_MOVE, чтобы переместить сообщение в папку "Удаленные элементы".</span><span class="sxs-lookup"><span data-stu-id="1bf32-116">If the folder is not contained within the Deleted Items folder, call [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) with the MESSAGE_MOVE flag set to relocate the message to the Deleted Items folder.</span></span> 
    

