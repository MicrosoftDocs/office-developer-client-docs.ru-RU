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
ms.openlocfilehash: edabb9a0f55cb34b4e144672e91ea50b8e9193b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809605"
---
# <a name="itnefencoderecips"></a><span data-ttu-id="287e9-103">ITnef::EncodeRecips</span><span class="sxs-lookup"><span data-stu-id="287e9-103">ITnef::EncodeRecips</span></span>

  
  
<span data-ttu-id="287e9-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="287e9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="287e9-105">Кодирует представления для таблицы получателей сообщения в потоке данных Transport-Neutral Encapsulation формата TNEF в сообщении.</span><span class="sxs-lookup"><span data-stu-id="287e9-105">Encodes a view for a message's recipient table in the Transport-Neutral Encapsulation Format (TNEF) data stream for the message.</span></span>
  
```cpp
HRESULT EncodeRecips(
  ULONG ulFlags,
  LPMAPITABLE lpRecipientTable
);
```

## <a name="parameters"></a><span data-ttu-id="287e9-106">���������</span><span class="sxs-lookup"><span data-stu-id="287e9-106">Parameters</span></span>

 <span data-ttu-id="287e9-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="287e9-107">_ulFlags_</span></span>
  
> <span data-ttu-id="287e9-108">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="287e9-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="287e9-109">_lpRecipientTable_</span><span class="sxs-lookup"><span data-stu-id="287e9-109">_lpRecipientTable_</span></span>
  
> <span data-ttu-id="287e9-110">[in] Указатель на таблицу получателей, для которого кодируется в представлении.</span><span class="sxs-lookup"><span data-stu-id="287e9-110">[in] A pointer to the recipient table for which the view is encoded.</span></span> <span data-ttu-id="287e9-111">Параметр _lpRecipientTable_ может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="287e9-111">The  _lpRecipientTable_ parameter can be NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="287e9-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2">Return value</span></span>

<span data-ttu-id="287e9-113">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="287e9-113">S_OK</span></span> 
  
> <span data-ttu-id="287e9-114">Вызов успешно и возвращается ожидаемым значением или значения.</span><span class="sxs-lookup"><span data-stu-id="287e9-114">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="287e9-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="287e9-115">Remarks</span></span>

<span data-ttu-id="287e9-116">Для передачи поставщиков, поставщиков хранилища сообщений и шлюзов вызова метода **ITnef::EncodeRecips** для выполнения кодировка TNEF для определенного получателя таблицы представления.</span><span class="sxs-lookup"><span data-stu-id="287e9-116">Transport providers, message store providers, and gateways call the **ITnef::EncodeRecips** method to perform TNEF encoding for a particular recipient table view.</span></span> <span data-ttu-id="287e9-117">Кодировка TNEF функция особенно полезна, например, если поставщик или шлюз требует определенного столбца, порядок сортировки или ограничения для получателей таблицы.</span><span class="sxs-lookup"><span data-stu-id="287e9-117">TNEF encoding is useful, for example, if a provider or gateway requires a particular column set, sort order, or restriction for the recipient table.</span></span> 
  
<span data-ttu-id="287e9-118">Поставщик или шлюз передает в табличном представлении кодируемые с помощью параметра _lpRecipientTable_ .</span><span class="sxs-lookup"><span data-stu-id="287e9-118">A provider or gateway passes the table view to be encoded in the  _lpRecipientTable_ parameter.</span></span> <span data-ttu-id="287e9-119">Реализация TNEF кодирует получателей таблица с заданным представления, с помощью набора данным столбцом, порядок сортировки, ограничения и положение.</span><span class="sxs-lookup"><span data-stu-id="287e9-119">The TNEF implementation encodes the recipient table with the given view, using the given column set, sort order, restriction, and position.</span></span> <span data-ttu-id="287e9-120">Если поставщик или шлюз передает NULL _lpRecipientTable_, TNEF получает таблицы получателя из сообщения с помощью метода [IMessage::GetRecipientTable](imessage-getrecipienttable.md) кодирования, процессов и каждой строки в таблице в поток TNEF с помощью текущие параметры таблицы.</span><span class="sxs-lookup"><span data-stu-id="287e9-120">If a provider or gateway passes NULL in  _lpRecipientTable_, TNEF gets the recipient table from the message being encoded by using the [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method, and processes every row of the table into the TNEF stream by using the table's current settings.</span></span> 
  
<span data-ttu-id="287e9-121">Вызов **EncodeRecips** с NULL в _lpRecipientTable_ таким образом кодирует всех получателей сообщений и эквивалентен вызову метода [ITnef::AddProps](itnef-addprops.md) с флагом TNEF_PROP_INCLUDE в его параметр _ulFlags_ и **PR_ MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) свойство в его параметра _lpPropList_ .</span><span class="sxs-lookup"><span data-stu-id="287e9-121">Calling **EncodeRecips** with NULL in  _lpRecipientTable_ thus encodes all message recipients and is equivalent to calling the [ITnef::AddProps](itnef-addprops.md) method with the TNEF_PROP_INCLUDE flag in its  _ulFlags_ parameter and the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property in its  _lpPropList_ parameter.</span></span> 
  
<span data-ttu-id="287e9-122">Обратите внимание на то, что это редко необходимо для вызова **EncodeRecips** , если не требуется для кодирования представление определенного получателя в таблице.</span><span class="sxs-lookup"><span data-stu-id="287e9-122">Note that it is rarely necessary to call **EncodeRecips** unless there is a requirement to encode a particular recipient table view.</span></span> <span data-ttu-id="287e9-123">Внешние системы обмена сообщениями почти всегда иметь средства для обработки получателей списков, которые являются недостаточно для удовлетворения распространенных потребностей кодирования получателей списков; Таким образом эти системы почти никогда не требуют TNEF для этой цели.</span><span class="sxs-lookup"><span data-stu-id="287e9-123">Foreign messaging systems almost always have facilities for handling recipient lists that are powerful enough to handle the common needs of encoding recipient lists; therefore, these systems almost never require TNEF for this purpose.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="287e9-124">См. также</span><span class="sxs-lookup"><span data-stu-id="287e9-124">See also</span></span>



[<span data-ttu-id="287e9-125">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="287e9-125">IMessage::GetRecipientTable</span></span>](imessage-getrecipienttable.md)
  
[<span data-ttu-id="287e9-126">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="287e9-126">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="287e9-127">Каноническое свойство PidTagMessageRecipients</span><span class="sxs-lookup"><span data-stu-id="287e9-127">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="287e9-128">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="287e9-128">ITnef : IUnknown</span></span>](itnefiunknown.md)

