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
ms.openlocfilehash: ff40eddf63e67f45495e90c1a960e45b7cc6cfb0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812253"
---
# <a name="sending-messages-mapi-spooler-tasks"></a><span data-ttu-id="28886-103">�������� ���������: ������ ������� MAPI</span><span class="sxs-lookup"><span data-stu-id="28886-103">Sending Messages: MAPI Spooler Tasks</span></span>

  
  
<span data-ttu-id="28886-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="28886-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="28886-105">��������� ������� MAPI ��������� � �������� �������� ��������� ��� ��������� ��������� �� �������� ����� ��������� � ������� ���������� ���������� ����� ��������� ��������� � ���������� �� ������� ���������� ���������� � ��� ��������� ������� ��������������� ���������.</span><span class="sxs-lookup"><span data-stu-id="28886-105">The MAPI spooler is involved in the message transmission process when the message store is not tightly coupled with a transport provider, when the tightly coupled store and transport cannot handle a recipient, and when the message requires preprocessing.</span></span>
  
 <span data-ttu-id="28886-106">**��������� ������� MAPI ����� ����� ����������� ��������������� ���������, ���������� ��������� ��������� ��������:**</span><span class="sxs-lookup"><span data-stu-id="28886-106">**After any necessary preprocessing, the MAPI spooler performs the following steps:**</span></span>
  
1. <span data-ttu-id="28886-107">If the message is not locked, locks the message by using the [IMsgStore::SetLockState](imsgstore-setlockstate.md) method.</span><span class="sxs-lookup"><span data-stu-id="28886-107">If the message is not locked, locks the message by using the [IMsgStore::SetLockState](imsgstore-setlockstate.md) method.</span></span> 
    
2. <span data-ttu-id="28886-108">Имеет поставщика транспорта отправки сообщения для всех получателей, которые их **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) свойство должно быть указано значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="28886-108">Has the transport provider send the message to all recipients that have their **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property set to FALSE.</span></span> 
    
3. <span data-ttu-id="28886-109">Очистка любые дополнительные сведения, который был добавлен к сообщению для использования во время предварительной обработки, если свойство **PR_PREPROCESS** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md)) вызывает соответствующую функцию ([RemovePreprocessInfo](removepreprocessinfo.md)).</span><span class="sxs-lookup"><span data-stu-id="28886-109">Calls the appropriate function ([RemovePreprocessInfo](removepreprocessinfo.md)) for cleaning up any additional information that was added to the message for use during preprocessing if the **PR_PREPROCESS** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md)) property has been set.</span></span> <span data-ttu-id="28886-110">This function is specified when the transport provider registers its preprocessor function.</span><span class="sxs-lookup"><span data-stu-id="28886-110">This function is specified when the transport provider registers its preprocessor function.</span></span> 
    
4. <span data-ttu-id="28886-p102">Calls [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md) method. In **FinishedMsg**, the message store provider:</span><span class="sxs-lookup"><span data-stu-id="28886-p102">Calls [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md) method. In **FinishedMsg**, the message store provider:</span></span>
    
  - <span data-ttu-id="28886-113">������������ ���������.</span><span class="sxs-lookup"><span data-stu-id="28886-113">Unlocks the message.</span></span>
    
  - <span data-ttu-id="28886-114">Calls the [IMAPISupport::DoSentMail](imapisupport-dosentmail.md) method to perform outbound hook processing if a messaging hook provider exists.</span><span class="sxs-lookup"><span data-stu-id="28886-114">Calls the [IMAPISupport::DoSentMail](imapisupport-dosentmail.md) method to perform outbound hook processing if a messaging hook provider exists.</span></span> <span data-ttu-id="28886-115">Затем копирует сообщение в папку, указанную с идентификатором запись в свойство **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)), если не замещена обмена сообщениями поставщика обработчик отправленные обработки сообщений.</span><span class="sxs-lookup"><span data-stu-id="28886-115">It then copies the message to the folder identified by the entry identifier in the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property, if not superseded by a messaging hook provider's sent message processing.</span></span> <span data-ttu-id="28886-116">И, наконец удаляет сообщение, если свойство **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="28886-116">Finally, it deletes the message if the **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) property has been set to TRUE.</span></span> 
    

