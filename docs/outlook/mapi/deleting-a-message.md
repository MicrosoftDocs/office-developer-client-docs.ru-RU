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
ms.openlocfilehash: c8d46ac6f47eb4dc68aebfa4562403ef1b738213
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808272"
---
# <a name="deleting-a-message"></a><span data-ttu-id="83233-103">Удаление сообщения</span><span class="sxs-lookup"><span data-stu-id="83233-103">Deleting a Message</span></span>

  
  
<span data-ttu-id="83233-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="83233-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="83233-105">Клиент можно удалить сообщение после открытия и просматривает пользователь или при закрытии и пользователь просматривает таблицу содержимого.</span><span class="sxs-lookup"><span data-stu-id="83233-105">A client can delete a message when it is open and the user is reading it, or when it is closed and the user is viewing the contents table.</span></span> <span data-ttu-id="83233-106">Чтобы защитить пользователей от случайного удаления сообщения, MAPI определяет удаление сообщений как в два этапа:</span><span class="sxs-lookup"><span data-stu-id="83233-106">To protect a user from inadvertently removing a message, MAPI defines message deletion as a two step process:</span></span>
  
1. <span data-ttu-id="83233-107">Пометить сообщение для удаления путем перемещения в папку, который был определен как папки «Удаленные» — папка, идентификатор которого запись хранится в свойстве **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="83233-107">Mark a message for deletion by moving it to the folder that has been designated as the Deleted Items folder — the folder whose entry identifier is stored in the **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) property.</span></span> 
    
2. <span data-ttu-id="83233-108">Удаление сообщения путем вызова метода [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md) .</span><span class="sxs-lookup"><span data-stu-id="83233-108">Remove the message by calling the [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md) method.</span></span> 
    
<span data-ttu-id="83233-109">Если пользователь выбирает для удаления сообщения в папке, отличной от папки «Удаленные», помечается для удаления.</span><span class="sxs-lookup"><span data-stu-id="83233-109">When a user chooses to delete a message in a folder other than the Deleted Items folder, mark it for deletion.</span></span> <span data-ttu-id="83233-110">Только в том случае, когда пользователь выбирает сообщения из папки «Удаленные» следует сообщения физически удалены из рабочей станции.</span><span class="sxs-lookup"><span data-stu-id="83233-110">Only when a user selects messages from within the Deleted Items folder should the messages be physically removed from the workstation.</span></span> <span data-ttu-id="83233-111">Можно запрашивать пользователя, чтобы убедиться, что пользователь действительно предназначен для выполнения удаления.</span><span class="sxs-lookup"><span data-stu-id="83233-111">You can prompt the user to verify that the user really intended to perform the deletion.</span></span>
  
 <span data-ttu-id="83233-112">**Чтобы удалить сообщение**</span><span class="sxs-lookup"><span data-stu-id="83233-112">**To delete a message**</span></span>
  
1. <span data-ttu-id="83233-113">Убедитесь, что удаление предстоящих возникает с этим пользователем.</span><span class="sxs-lookup"><span data-stu-id="83233-113">Confirm with the user that the impending deletion is intentional.</span></span>
    
2. <span data-ttu-id="83233-114">Определения родительской папки для удаления.</span><span class="sxs-lookup"><span data-stu-id="83233-114">Determine the parent of the folder to be deleted.</span></span> <span data-ttu-id="83233-115">Если это папки "Удаленные" или вложенных папок в папку «Удаленные», вызовите [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md) для удаления сообщения.</span><span class="sxs-lookup"><span data-stu-id="83233-115">If it is the Deleted Items folder or a subfolder within the Deleted Items folder, call [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md) to remove the message.</span></span> 
    
3. <span data-ttu-id="83233-116">Если папка не находится в папку «Удаленные», вызовите [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) с установленным флагом MESSAGE_MOVE переместить сообщение в папки «Удаленные».</span><span class="sxs-lookup"><span data-stu-id="83233-116">If the folder is not contained within the Deleted Items folder, call [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) with the MESSAGE_MOVE flag set to relocate the message to the Deleted Items folder.</span></span> 
    

