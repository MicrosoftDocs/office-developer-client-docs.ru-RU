---
title: Кодирование таблиц получателей с помощью TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cd2f595f-4dd0-4704-b670-6857d6c843ca
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 1ed047424e4a6d64c08b511a15769c081a0d8c4e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339405"
---
# <a name="encoding-recipient-tables-by-using-tnef"></a><span data-ttu-id="9216f-103">Кодирование таблиц получателей с помощью TNEF</span><span class="sxs-lookup"><span data-stu-id="9216f-103">Encoding Recipient Tables by Using TNEF</span></span>

  
  
<span data-ttu-id="9216f-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9216f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9216f-105">Кодирование таблицы получателей в потоке TNEF редко требуется, так как большинство систем обмена сообщениями напрямую поддерживают списки получателей.</span><span class="sxs-lookup"><span data-stu-id="9216f-105">The encoding of a recipient table into the TNEF stream is rarely necessary since most messaging systems support recipient lists directly.</span></span> <span data-ttu-id="9216f-106">В общем случае свойства получателей передаются в заголовке сообщения.</span><span class="sxs-lookup"><span data-stu-id="9216f-106">In general, the recipient properties are transmitted in the message header.</span></span> <span data-ttu-id="9216f-107">При включении таблицы получателей TNEF может кодировать таблицу получателей в рамках обычной обработки.</span><span class="sxs-lookup"><span data-stu-id="9216f-107">When inclusion of the recipient table is necessary, TNEF can encode the recipient table as a part of its usual processing.</span></span> <span data-ttu-id="9216f-108">Это выполняется на начальном этапе обработки TNEF.</span><span class="sxs-lookup"><span data-stu-id="9216f-108">This is done during the initial phase of TNEF processing.</span></span> <span data-ttu-id="9216f-109">Поставщик транспорта может включать таблицу получателей сообщения, вызывая метод [итнеф:: аддпропс](itnef-addprops.md) со свойством **пр_мессаже_реЦипиентс** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)), указанным в списке включений.</span><span class="sxs-lookup"><span data-stu-id="9216f-109">The transport provider can include the message's recipient table by calling the [ITnef::AddProps](itnef-addprops.md) method with the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property specified in the inclusion list.</span></span> <span data-ttu-id="9216f-110">TNEF получает таблицу получателей из сообщения, запрашивает набор столбцов и обрабатывает каждую строку таблицы в поток TNEF.</span><span class="sxs-lookup"><span data-stu-id="9216f-110">TNEF gets the recipient table from the message, queries the column set, and processes every row of the table into the TNEF stream.</span></span>
  
<span data-ttu-id="9216f-111">Альтернативный метод доступен, если поставщик транспорта должен изменить таблицу получателей, прежде чем она будет закодирована.</span><span class="sxs-lookup"><span data-stu-id="9216f-111">An alternate method is available if the transport provider needs to modify the recipient table before it is encoded.</span></span> <span data-ttu-id="9216f-112">Поставщик транспорта может создать необходимую таблицу и затем вызвать метод [итнеф:: енкодереЦипс](itnef-encoderecips.md) .</span><span class="sxs-lookup"><span data-stu-id="9216f-112">The transport provider can construct the necessary table and then call the [ITnef::EncodeRecips](itnef-encoderecips.md) method.</span></span> <span data-ttu-id="9216f-113">Если в параметре _лпреЦиптабле_ переДАЕТСЯ значение null, то таблица получателей берется непосредственно из сообщения, как описано в **Итнеф:: аддпропс**.</span><span class="sxs-lookup"><span data-stu-id="9216f-113">If NULL is passed in the  _lpRecipTable_ parameter, then the recipient table is taken directly from the message as described for **ITnef::AddProps**.</span></span>
  

