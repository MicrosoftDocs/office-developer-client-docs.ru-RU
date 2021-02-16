---
title: Кодив таблицы получателей с помощью TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cd2f595f-4dd0-4704-b670-6857d6c843ca
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 1ed047424e4a6d64c08b511a15769c081a0d8c4e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417961"
---
# <a name="encoding-recipient-tables-by-using-tnef"></a><span data-ttu-id="9ce7e-103">Кодив таблицы получателей с помощью TNEF</span><span class="sxs-lookup"><span data-stu-id="9ce7e-103">Encoding Recipient Tables by Using TNEF</span></span>

  
  
<span data-ttu-id="9ce7e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9ce7e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9ce7e-105">Кодив таблицу получателей в потоке TNEF, редко требуется, так как большинство систем обмена сообщениями поддерживают списки получателей напрямую.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-105">The encoding of a recipient table into the TNEF stream is rarely necessary since most messaging systems support recipient lists directly.</span></span> <span data-ttu-id="9ce7e-106">Как правило, свойства получателя передаются в заголке сообщения.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-106">In general, the recipient properties are transmitted in the message header.</span></span> <span data-ttu-id="9ce7e-107">Если необходимо включить таблицу получателей, TNEF может закодировать таблицу получателей как часть обычной обработки.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-107">When inclusion of the recipient table is necessary, TNEF can encode the recipient table as a part of its usual processing.</span></span> <span data-ttu-id="9ce7e-108">Это делается на начальном этапе обработки TNEF.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-108">This is done during the initial phase of TNEF processing.</span></span> <span data-ttu-id="9ce7e-109">Поставщик транспорта может включить таблицу получателей сообщения, вызывая метод [ITnef::AddProps](itnef-addprops.md) со свойством **PR_MESSAGE_RECIPIENTS** [(PidTagMessageRecipients),](pidtagmessagerecipients-canonical-property.md)указанным в списке включения.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-109">The transport provider can include the message's recipient table by calling the [ITnef::AddProps](itnef-addprops.md) method with the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property specified in the inclusion list.</span></span> <span data-ttu-id="9ce7e-110">TNEF получает таблицу получателей из сообщения, запрашивает набор столбцов и обрабатывает каждую строку таблицы в потоке TNEF.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-110">TNEF gets the recipient table from the message, queries the column set, and processes every row of the table into the TNEF stream.</span></span>
  
<span data-ttu-id="9ce7e-111">Альтернативный метод доступен, если поставщику транспорта необходимо изменить таблицу получателей перед ее кодированием.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-111">An alternate method is available if the transport provider needs to modify the recipient table before it is encoded.</span></span> <span data-ttu-id="9ce7e-112">Поставщик транспорта может создать необходимую таблицу и вызвать метод [ITnef::EncodeRecips.](itnef-encoderecips.md)</span><span class="sxs-lookup"><span data-stu-id="9ce7e-112">The transport provider can construct the necessary table and then call the [ITnef::EncodeRecips](itnef-encoderecips.md) method.</span></span> <span data-ttu-id="9ce7e-113">Если в параметре _lpRecipTable_ передается NULL, таблица получателей будет взята непосредственно из сообщения, как описано для **ITnef::AddProps.**</span><span class="sxs-lookup"><span data-stu-id="9ce7e-113">If NULL is passed in the  _lpRecipTable_ parameter, then the recipient table is taken directly from the message as described for **ITnef::AddProps**.</span></span>
  

