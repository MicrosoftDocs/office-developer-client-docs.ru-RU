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
# <a name="deleting-a-message"></a><span data-ttu-id="4a2f3-103">Удаление сообщения</span><span class="sxs-lookup"><span data-stu-id="4a2f3-103">Deleting a Message</span></span>

  
  
<span data-ttu-id="4a2f3-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4a2f3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4a2f3-105">Клиент может удалить сообщение, когда оно открыто и пользователь читает его, или если оно закрыто и пользователь просматривает таблицу содержимого.</span><span class="sxs-lookup"><span data-stu-id="4a2f3-105">A client can delete a message when it is open and the user is reading it, or when it is closed and the user is viewing the contents table.</span></span> <span data-ttu-id="4a2f3-106">Чтобы защитить пользователя от случайного удаления сообщения, MAPI определяет удаление сообщения как двухшаговую процедуру:</span><span class="sxs-lookup"><span data-stu-id="4a2f3-106">To protect a user from inadvertently removing a message, MAPI defines message deletion as a two step process:</span></span>
  
1. <span data-ttu-id="4a2f3-107">Пометить сообщение для удаления, перемещая его в папку, назначенную в качестве папки "Удаленные", — папку, идентификатор записи которой хранится в свойстве **PR_IPM_WASTEBASKET_ENTRYID** [(PidTagIpmWastebasketEntryId).](pidtagipmwastebasketentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="4a2f3-107">Mark a message for deletion by moving it to the folder that has been designated as the Deleted Items folder — the folder whose entry identifier is stored in the **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) property.</span></span> 
    
2. <span data-ttu-id="4a2f3-108">Удалите сообщение, вызывая метод [IMAPIFolder::D eleteMessages.](imapifolder-deletemessages.md)</span><span class="sxs-lookup"><span data-stu-id="4a2f3-108">Remove the message by calling the [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md) method.</span></span> 
    
<span data-ttu-id="4a2f3-109">Когда пользователь выбирает удаление сообщения в папке, не вложенной в папку "Удаленные", пометите его для удаления.</span><span class="sxs-lookup"><span data-stu-id="4a2f3-109">When a user chooses to delete a message in a folder other than the Deleted Items folder, mark it for deletion.</span></span> <span data-ttu-id="4a2f3-110">Только если пользователь выбирает сообщения из папки "Удаленные", они должны быть физически удалены с рабочей станции.</span><span class="sxs-lookup"><span data-stu-id="4a2f3-110">Only when a user selects messages from within the Deleted Items folder should the messages be physically removed from the workstation.</span></span> <span data-ttu-id="4a2f3-111">Вы можете побудить пользователя убедиться, что пользователь действительно намерен выполнить удаление.</span><span class="sxs-lookup"><span data-stu-id="4a2f3-111">You can prompt the user to verify that the user really intended to perform the deletion.</span></span>
  
 <span data-ttu-id="4a2f3-112">**Удаление сообщения**</span><span class="sxs-lookup"><span data-stu-id="4a2f3-112">**To delete a message**</span></span>
  
1. <span data-ttu-id="4a2f3-113">Подтвердим пользователю, что предстоящее удаление является преднамеренным.</span><span class="sxs-lookup"><span data-stu-id="4a2f3-113">Confirm with the user that the impending deletion is intentional.</span></span>
    
2. <span data-ttu-id="4a2f3-114">Определите родительский родитель папки, которая должна быть удалена.</span><span class="sxs-lookup"><span data-stu-id="4a2f3-114">Determine the parent of the folder to be deleted.</span></span> <span data-ttu-id="4a2f3-115">Если это папка "Удаленные" или вложенная папка в папке "Удаленные", вызовите [IMAPIFolder::D eleteMessages,](imapifolder-deletemessages.md) чтобы удалить сообщение.</span><span class="sxs-lookup"><span data-stu-id="4a2f3-115">If it is the Deleted Items folder or a subfolder within the Deleted Items folder, call [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md) to remove the message.</span></span> 
    
3. <span data-ttu-id="4a2f3-116">Если папка не находится в папке "Удаленные", вызовите [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) с флагом MESSAGE_MOVE, чтобы переместить сообщение в папку "Удаленные".</span><span class="sxs-lookup"><span data-stu-id="4a2f3-116">If the folder is not contained within the Deleted Items folder, call [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) with the MESSAGE_MOVE flag set to relocate the message to the Deleted Items folder.</span></span> 
    

