---
title: �������� ��������� ������ ������� MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 81c65f21-03ba-43eb-a6d4-d311e660ac5c
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 8a6730cca5c75a888afb5ff0a44f1e2a0a6465e6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420201"
---
# <a name="sending-messages-mapi-spooler-tasks"></a><span data-ttu-id="a13ee-103">Отправка сообщений: задачи системы буферизации MAPI</span><span class="sxs-lookup"><span data-stu-id="a13ee-103">Sending Messages: MAPI Spooler Tasks</span></span>

  
  
<span data-ttu-id="a13ee-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a13ee-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a13ee-105">��������� ������� MAPI ��������� � �������� �������� ��������� ��� ��������� ��������� �� �������� ����� ��������� � ������� ���������� ���������� ����� ��������� ��������� � ���������� �� ������� ���������� ���������� � ��� ��������� ������� ��������������� ���������.</span><span class="sxs-lookup"><span data-stu-id="a13ee-105">The MAPI spooler is involved in the message transmission process when the message store is not tightly coupled with a transport provider, when the tightly coupled store and transport cannot handle a recipient, and when the message requires preprocessing.</span></span>
  
 <span data-ttu-id="a13ee-106">**��������� ������� MAPI ����� ����� ����������� ��������������� ���������, ���������� ��������� ��������� ��������:**</span><span class="sxs-lookup"><span data-stu-id="a13ee-106">**After any necessary preprocessing, the MAPI spooler performs the following steps:**</span></span>
  
1. <span data-ttu-id="a13ee-107">If the message is not locked, locks the message by using the [IMsgStore::SetLockState](imsgstore-setlockstate.md) method.</span><span class="sxs-lookup"><span data-stu-id="a13ee-107">If the message is not locked, locks the message by using the [IMsgStore::SetLockState](imsgstore-setlockstate.md) method.</span></span> 
    
2. <span data-ttu-id="a13ee-108">Поставщик транспорта отправляет сообщение всем получателям, у которых для свойства **пр_респонсибилити** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) задано значение false.</span><span class="sxs-lookup"><span data-stu-id="a13ee-108">Has the transport provider send the message to all recipients that have their **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property set to FALSE.</span></span> 
    
3. <span data-ttu-id="a13ee-109">Вызывает соответствующую функцию ([ремовепрепроцессинфо](removepreprocessinfo.md)), чтобы очистить дополнительные сведения, добавленные к сообщению для использования во время предварительной обработки, если было задано свойство **пр_препроцесс** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a13ee-109">Calls the appropriate function ([RemovePreprocessInfo](removepreprocessinfo.md)) for cleaning up any additional information that was added to the message for use during preprocessing if the **PR_PREPROCESS** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md)) property has been set.</span></span> <span data-ttu-id="a13ee-110">This function is specified when the transport provider registers its preprocessor function.</span><span class="sxs-lookup"><span data-stu-id="a13ee-110">This function is specified when the transport provider registers its preprocessor function.</span></span> 
    
4. <span data-ttu-id="a13ee-p102">Calls [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md) method. In **FinishedMsg**, the message store provider:</span><span class="sxs-lookup"><span data-stu-id="a13ee-p102">Calls [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md) method. In **FinishedMsg**, the message store provider:</span></span>
    
  - <span data-ttu-id="a13ee-113">������������ ���������.</span><span class="sxs-lookup"><span data-stu-id="a13ee-113">Unlocks the message.</span></span>
    
  - <span data-ttu-id="a13ee-114">Calls the [IMAPISupport::DoSentMail](imapisupport-dosentmail.md) method to perform outbound hook processing if a messaging hook provider exists.</span><span class="sxs-lookup"><span data-stu-id="a13ee-114">Calls the [IMAPISupport::DoSentMail](imapisupport-dosentmail.md) method to perform outbound hook processing if a messaging hook provider exists.</span></span> <span data-ttu-id="a13ee-115">После этого сообщение копируется в папку, указанную идентификатором записи, в свойстве **пр_сентмаил_ентрид** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)), если она не была заменена с помощью отправленной обработки сообщений поставщика обработчиков обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="a13ee-115">It then copies the message to the folder identified by the entry identifier in the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property, if not superseded by a messaging hook provider's sent message processing.</span></span> <span data-ttu-id="a13ee-116">Наконец, он удаляет сообщение, если для свойства **пр_делете_афтер_субмит** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) задано значение true.</span><span class="sxs-lookup"><span data-stu-id="a13ee-116">Finally, it deletes the message if the **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) property has been set to TRUE.</span></span> 
    

