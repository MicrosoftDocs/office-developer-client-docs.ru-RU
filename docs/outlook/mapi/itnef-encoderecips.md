---
title: ITnefEncodeRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.EncodeRecips
api_type:
- COM
ms.assetid: b3ce4b0e-4f48-4a7e-a30c-c4754bccb12c
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: d8caa503e557d35e259db743505d39ea4809dbfd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437653"
---
# <a name="itnefencoderecips"></a><span data-ttu-id="8d602-103">ITnef::EncodeRecips</span><span class="sxs-lookup"><span data-stu-id="8d602-103">ITnef::EncodeRecips</span></span>

  
  
<span data-ttu-id="8d602-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8d602-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8d602-105">Кодирует представление таблицы получателей сообщения в потоке Transport-Neutral формата Инкапсуляции (TNEF) для сообщения.</span><span class="sxs-lookup"><span data-stu-id="8d602-105">Encodes a view for a message's recipient table in the Transport-Neutral Encapsulation Format (TNEF) data stream for the message.</span></span>
  
```cpp
HRESULT EncodeRecips(
  ULONG ulFlags,
  LPMAPITABLE lpRecipientTable
);
```

## <a name="parameters"></a><span data-ttu-id="8d602-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="8d602-106">Parameters</span></span>

 <span data-ttu-id="8d602-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8d602-107">_ulFlags_</span></span>
  
> <span data-ttu-id="8d602-108">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="8d602-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="8d602-109">_lpRecipientTable_</span><span class="sxs-lookup"><span data-stu-id="8d602-109">_lpRecipientTable_</span></span>
  
> <span data-ttu-id="8d602-110">[in] Указатель на таблицу получателей, для которой кодируются представления.</span><span class="sxs-lookup"><span data-stu-id="8d602-110">[in] A pointer to the recipient table for which the view is encoded.</span></span> <span data-ttu-id="8d602-111">Параметр  _lpRecipientTable может_ быть NULL.</span><span class="sxs-lookup"><span data-stu-id="8d602-111">The  _lpRecipientTable_ parameter can be NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8d602-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8d602-112">Return value</span></span>

<span data-ttu-id="8d602-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="8d602-113">S_OK</span></span> 
  
> <span data-ttu-id="8d602-114">Вызов удался и возвращает ожидаемое значение или значения.</span><span class="sxs-lookup"><span data-stu-id="8d602-114">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8d602-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="8d602-115">Remarks</span></span>

<span data-ttu-id="8d602-116">Поставщики транспорта, поставщики магазинов сообщений и шлюзы звонят **методу ITnef::EncodeRecips** для выполнения кодирования TNEF для определенного представления таблицы получателей.</span><span class="sxs-lookup"><span data-stu-id="8d602-116">Transport providers, message store providers, and gateways call the **ITnef::EncodeRecips** method to perform TNEF encoding for a particular recipient table view.</span></span> <span data-ttu-id="8d602-117">Кодификат TNEF полезен, например, если поставщику или шлюзу требуется определенный набор столбцов, порядок сортировки или ограничение для таблицы получателей.</span><span class="sxs-lookup"><span data-stu-id="8d602-117">TNEF encoding is useful, for example, if a provider or gateway requires a particular column set, sort order, or restriction for the recipient table.</span></span> 
  
<span data-ttu-id="8d602-118">Поставщик или шлюз передает представление таблицы, кодированное в _параметре lpRecipientTable._</span><span class="sxs-lookup"><span data-stu-id="8d602-118">A provider or gateway passes the table view to be encoded in the  _lpRecipientTable_ parameter.</span></span> <span data-ttu-id="8d602-119">Реализация TNEF кодирует таблицу получателей с заданным представлением, используя заданный набор столбцов, порядок сортировки, ограничение и положение.</span><span class="sxs-lookup"><span data-stu-id="8d602-119">The TNEF implementation encodes the recipient table with the given view, using the given column set, sort order, restriction, and position.</span></span> <span data-ttu-id="8d602-120">Если поставщик или шлюз передает NULL в  _lpRecipientTable,_ TNEF получает таблицу получателей из зашифрованного сообщения с помощью метода [IMessage::GetRecipientTable](imessage-getrecipienttable.md) и обрабатывает каждую строку таблицы в поток TNEF с помощью текущих параметров таблицы.</span><span class="sxs-lookup"><span data-stu-id="8d602-120">If a provider or gateway passes NULL in  _lpRecipientTable_, TNEF gets the recipient table from the message being encoded by using the [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method, and processes every row of the table into the TNEF stream by using the table's current settings.</span></span> 
  
<span data-ttu-id="8d602-121">Вызов **EncodeRecips** с NULL в _lpRecipientTable_ таким образом кодирует всех получателей сообщений и эквивалентен вызову метода [ITnef::AddProps](itnef-addprops.md) с флагом TNEF_PROP_INCLUDE в его параметре _ulFlags_ и **свойством PR_MESSAGE_RECIPIENTS** [(PidTagMessageRecipients)](pidtagmessagerecipients-canonical-property.md)в параметре _lpPropList._</span><span class="sxs-lookup"><span data-stu-id="8d602-121">Calling **EncodeRecips** with NULL in  _lpRecipientTable_ thus encodes all message recipients and is equivalent to calling the [ITnef::AddProps](itnef-addprops.md) method with the TNEF_PROP_INCLUDE flag in its  _ulFlags_ parameter and the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property in its  _lpPropList_ parameter.</span></span> 
  
<span data-ttu-id="8d602-122">Обратите внимание, что редко необходимо вызывать **EncodeRecips,** если не требуется кодировать определенное представление таблицы получателей.</span><span class="sxs-lookup"><span data-stu-id="8d602-122">Note that it is rarely necessary to call **EncodeRecips** unless there is a requirement to encode a particular recipient table view.</span></span> <span data-ttu-id="8d602-123">В иностранных системах обмена сообщениями почти всегда есть возможности для обработки списков получателей, которые достаточно мощны для обработки общих потребностей списков получателей; поэтому эти системы почти никогда не требуют TNEF для этой цели.</span><span class="sxs-lookup"><span data-stu-id="8d602-123">Foreign messaging systems almost always have facilities for handling recipient lists that are powerful enough to handle the common needs of encoding recipient lists; therefore, these systems almost never require TNEF for this purpose.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8d602-124">См. также</span><span class="sxs-lookup"><span data-stu-id="8d602-124">See also</span></span>



[<span data-ttu-id="8d602-125">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="8d602-125">IMessage::GetRecipientTable</span></span>](imessage-getrecipienttable.md)
  
[<span data-ttu-id="8d602-126">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="8d602-126">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="8d602-127">Каноническое свойство PidTagMessageRecipients</span><span class="sxs-lookup"><span data-stu-id="8d602-127">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="8d602-128">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8d602-128">ITnef : IUnknown</span></span>](itnefiunknown.md)

