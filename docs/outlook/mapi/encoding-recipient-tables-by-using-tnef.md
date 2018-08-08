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
ms.openlocfilehash: 8110eff9b38c76023621f34396d65714a4316d91
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808391"
---
# <a name="encoding-recipient-tables-by-using-tnef"></a><span data-ttu-id="68f65-103">Кодирование таблиц получателей с помощью TNEF</span><span class="sxs-lookup"><span data-stu-id="68f65-103">Encoding Recipient Tables by Using TNEF</span></span>

  
  
<span data-ttu-id="68f65-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="68f65-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="68f65-105">Кодирования таблице получателей в поток TNEF редко, так как систем обмена сообщениями наиболее поддерживает получателей списки непосредственно.</span><span class="sxs-lookup"><span data-stu-id="68f65-105">The encoding of a recipient table into the TNEF stream is rarely necessary since most messaging systems support recipient lists directly.</span></span> <span data-ttu-id="68f65-106">В общем случае свойствами получателя передаются в заголовке сообщения.</span><span class="sxs-lookup"><span data-stu-id="68f65-106">In general, the recipient properties are transmitted in the message header.</span></span> <span data-ttu-id="68f65-107">При необходимости включения получателей таблицы TNEF можно закодировать таблицы получателей в рамках обычного обработки.</span><span class="sxs-lookup"><span data-stu-id="68f65-107">When inclusion of the recipient table is necessary, TNEF can encode the recipient table as a part of its usual processing.</span></span> <span data-ttu-id="68f65-108">Для этого на начальном этапе обработки TNEF.</span><span class="sxs-lookup"><span data-stu-id="68f65-108">This is done during the initial phase of TNEF processing.</span></span> <span data-ttu-id="68f65-109">Путем вызова метода [ITnef::AddProps](itnef-addprops.md) со свойством **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)), указанный в списке включения поставщика транспорта может включать таблицы получателя сообщения.</span><span class="sxs-lookup"><span data-stu-id="68f65-109">The transport provider can include the message's recipient table by calling the [ITnef::AddProps](itnef-addprops.md) method with the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property specified in the inclusion list.</span></span> <span data-ttu-id="68f65-110">Формат TNEF получает таблицы получателя из сообщения, запрашивает набор столбцов и обрабатывает каждой строки в таблице в поток TNEF.</span><span class="sxs-lookup"><span data-stu-id="68f65-110">TNEF gets the recipient table from the message, queries the column set, and processes every row of the table into the TNEF stream.</span></span>
  
<span data-ttu-id="68f65-111">Следующий метод доступен, если поставщик транспорта должен изменить получателя таблицы перед кодированием.</span><span class="sxs-lookup"><span data-stu-id="68f65-111">An alternate method is available if the transport provider needs to modify the recipient table before it is encoded.</span></span> <span data-ttu-id="68f65-112">Поставщика транспорта можно создать необходимые таблицы и затем вызвать метод [ITnef::EncodeRecips](itnef-encoderecips.md) .</span><span class="sxs-lookup"><span data-stu-id="68f65-112">The transport provider can construct the necessary table and then call the [ITnef::EncodeRecips](itnef-encoderecips.md) method.</span></span> <span data-ttu-id="68f65-113">Если NULL передается в параметре _lpRecipTable_ , таблицы получателя берется непосредственно из сообщения, как описано для **ITnef::AddProps**.</span><span class="sxs-lookup"><span data-stu-id="68f65-113">If NULL is passed in the  _lpRecipTable_ parameter, then the recipient table is taken directly from the message as described for **ITnef::AddProps**.</span></span>
  

