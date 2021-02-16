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
# <a name="itnefencoderecips"></a><span data-ttu-id="02892-103">ITnef::EncodeRecips</span><span class="sxs-lookup"><span data-stu-id="02892-103">ITnef::EncodeRecips</span></span>

  
  
<span data-ttu-id="02892-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="02892-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="02892-105">Кодирует представление таблицы получателей сообщения в потоке данных Transport-Neutral формата Инкапсуляции (TNEF) для сообщения.</span><span class="sxs-lookup"><span data-stu-id="02892-105">Encodes a view for a message's recipient table in the Transport-Neutral Encapsulation Format (TNEF) data stream for the message.</span></span>
  
```cpp
HRESULT EncodeRecips(
  ULONG ulFlags,
  LPMAPITABLE lpRecipientTable
);
```

## <a name="parameters"></a><span data-ttu-id="02892-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="02892-106">Parameters</span></span>

 <span data-ttu-id="02892-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="02892-107">_ulFlags_</span></span>
  
> <span data-ttu-id="02892-108">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="02892-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="02892-109">_lpRecipientTable_</span><span class="sxs-lookup"><span data-stu-id="02892-109">_lpRecipientTable_</span></span>
  
> <span data-ttu-id="02892-110">[in] Указатель на таблицу получателей, для которой закодировано представление.</span><span class="sxs-lookup"><span data-stu-id="02892-110">[in] A pointer to the recipient table for which the view is encoded.</span></span> <span data-ttu-id="02892-111">Параметр  _lpRecipientTable может_ иметь NULL.</span><span class="sxs-lookup"><span data-stu-id="02892-111">The  _lpRecipientTable_ parameter can be NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="02892-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="02892-112">Return value</span></span>

<span data-ttu-id="02892-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="02892-113">S_OK</span></span> 
  
> <span data-ttu-id="02892-114">Вызов был успешным и возвратил ожидаемое значение или значения.</span><span class="sxs-lookup"><span data-stu-id="02892-114">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="02892-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="02892-115">Remarks</span></span>

<span data-ttu-id="02892-116">Поставщики транспорта, поставщики хранимых сообщений и шлюзы звонят **методу ITnef::EncodeRecips** для выполнения кодирования TNEF для определенного представления таблицы получателей.</span><span class="sxs-lookup"><span data-stu-id="02892-116">Transport providers, message store providers, and gateways call the **ITnef::EncodeRecips** method to perform TNEF encoding for a particular recipient table view.</span></span> <span data-ttu-id="02892-117">Кодировать TNEF удобно, например, если поставщику или шлюзу требуется определенный набор столбцов, порядок сортировки или ограничение для таблицы получателей.</span><span class="sxs-lookup"><span data-stu-id="02892-117">TNEF encoding is useful, for example, if a provider or gateway requires a particular column set, sort order, or restriction for the recipient table.</span></span> 
  
<span data-ttu-id="02892-118">Поставщик или шлюз передает представление таблицы для кодирования в _параметре lpRecipientTable._</span><span class="sxs-lookup"><span data-stu-id="02892-118">A provider or gateway passes the table view to be encoded in the  _lpRecipientTable_ parameter.</span></span> <span data-ttu-id="02892-119">Реализация TNEF кодирует таблицу получателей в заданном представлении, используя заданный набор столбцов, порядок сортировки, ограничение и положение.</span><span class="sxs-lookup"><span data-stu-id="02892-119">The TNEF implementation encodes the recipient table with the given view, using the given column set, sort order, restriction, and position.</span></span> <span data-ttu-id="02892-120">Если поставщик или шлюз передает NULL в  _lpRecipientTable,_ TNEF получает таблицу получателей из сообщения, закодированного с помощью метода [IMessage::GetRecipientTable,](imessage-getrecipienttable.md) и обрабатывает каждую строку таблицы в потоке TNEF с помощью текущих параметров таблицы.</span><span class="sxs-lookup"><span data-stu-id="02892-120">If a provider or gateway passes NULL in  _lpRecipientTable_, TNEF gets the recipient table from the message being encoded by using the [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method, and processes every row of the table into the TNEF stream by using the table's current settings.</span></span> 
  
<span data-ttu-id="02892-121">Вызов **Метода EncodeRecips** с NULL в _lpRecipientTable_ кодирует всех получателей сообщений и эквивалентен вызову метода [ITnef::AddProps](itnef-addprops.md) с флагом TNEF_PROP_INCLUDE в параметре _ulFlags_ и **свойством PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients)](pidtagmessagerecipients-canonical-property.md)в параметре _lpPropList._</span><span class="sxs-lookup"><span data-stu-id="02892-121">Calling **EncodeRecips** with NULL in  _lpRecipientTable_ thus encodes all message recipients and is equivalent to calling the [ITnef::AddProps](itnef-addprops.md) method with the TNEF_PROP_INCLUDE flag in its  _ulFlags_ parameter and the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property in its  _lpPropList_ parameter.</span></span> 
  
<span data-ttu-id="02892-122">Обратите внимание, что редко требуется вызывать **EncodeRecips,** если не требуется кодировать определенное представление таблицы получателей.</span><span class="sxs-lookup"><span data-stu-id="02892-122">Note that it is rarely necessary to call **EncodeRecips** unless there is a requirement to encode a particular recipient table view.</span></span> <span data-ttu-id="02892-123">Внешние системы обмена сообщениями почти всегда имеют средства для обработки списков получателей, которые достаточно мощны для обработки общих потребностей в коде списков получателей; Поэтому для этих систем почти никогда не требуется TNEF.</span><span class="sxs-lookup"><span data-stu-id="02892-123">Foreign messaging systems almost always have facilities for handling recipient lists that are powerful enough to handle the common needs of encoding recipient lists; therefore, these systems almost never require TNEF for this purpose.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="02892-124">См. также</span><span class="sxs-lookup"><span data-stu-id="02892-124">See also</span></span>



[<span data-ttu-id="02892-125">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="02892-125">IMessage::GetRecipientTable</span></span>](imessage-getrecipienttable.md)
  
[<span data-ttu-id="02892-126">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="02892-126">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="02892-127">Каноническое свойство PidTagMessageRecipients</span><span class="sxs-lookup"><span data-stu-id="02892-127">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="02892-128">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="02892-128">ITnef : IUnknown</span></span>](itnefiunknown.md)

