---
title: IMessageGetRecipientTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.GetRecipientTable
api_type:
- COM
ms.assetid: a335dfca-44da-452e-b16f-25d314b1758f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: ca42e91528cdb7e61ae3620989c4a89966db1061
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424611"
---
# <a name="imessagegetrecipienttable"></a><span data-ttu-id="5e83b-103">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="5e83b-103">IMessage::GetRecipientTable</span></span>

  
  
<span data-ttu-id="5e83b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5e83b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5e83b-105">Возвращает таблицу получателей сообщения.</span><span class="sxs-lookup"><span data-stu-id="5e83b-105">Returns the message's recipient table.</span></span>
  
```cpp
HRESULT GetRecipientTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="5e83b-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="5e83b-106">Parameters</span></span>

 <span data-ttu-id="5e83b-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5e83b-107">_ulFlags_</span></span>
  
> <span data-ttu-id="5e83b-108">[in] Bitmask флагов, которые контролируют возвращение таблицы.</span><span class="sxs-lookup"><span data-stu-id="5e83b-108">[in] Bitmask of flags that controls the return of the table.</span></span> <span data-ttu-id="5e83b-109">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="5e83b-109">The following flags can be set:</span></span>
    
<span data-ttu-id="5e83b-110">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="5e83b-110">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="5e83b-111">Позволяет **GetRecipientTable** успешно возвращаться, возможно, до того, как таблица будет полностью доступна для вызываемого клиента.</span><span class="sxs-lookup"><span data-stu-id="5e83b-111">Allows **GetRecipientTable** to return successfully, possibly before the table is fully available to the calling client.</span></span> <span data-ttu-id="5e83b-112">Если таблица недоступна, последующий вызов может привести к ошибке.</span><span class="sxs-lookup"><span data-stu-id="5e83b-112">If the table is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="5e83b-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5e83b-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="5e83b-114">Столбцы строки должны быть в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="5e83b-114">String columns should be in Unicode format.</span></span> <span data-ttu-id="5e83b-115">Если флаг MAPI_UNICODE не установлен, столбцы строки должны быть в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="5e83b-115">If the MAPI_UNICODE flag is not set, the string columns should be in ANSI format.</span></span>
    
 <span data-ttu-id="5e83b-116">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="5e83b-116">_lppTable_</span></span>
  
> <span data-ttu-id="5e83b-117">[вышел] Указатель на указатель на таблицу получателей.</span><span class="sxs-lookup"><span data-stu-id="5e83b-117">[out] Pointer to a pointer to the recipient table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5e83b-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5e83b-118">Return value</span></span>

<span data-ttu-id="5e83b-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="5e83b-119">S_OK</span></span> 
  
> <span data-ttu-id="5e83b-120">Таблица получателей была возвращена успешно.</span><span class="sxs-lookup"><span data-stu-id="5e83b-120">The recipient table was returned successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5e83b-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="5e83b-121">Remarks</span></span>

<span data-ttu-id="5e83b-122">Метод **IMessage::GetRecipientTable** возвращает указатель в таблицу получателей сообщения, которая включает сведения обо всех получателях сообщения.</span><span class="sxs-lookup"><span data-stu-id="5e83b-122">The **IMessage::GetRecipientTable** method returns a pointer to the message's recipient table, which includes information about all of the recipients for the message.</span></span> <span data-ttu-id="5e83b-123">Для каждого получателя имеется одна строка.</span><span class="sxs-lookup"><span data-stu-id="5e83b-123">There is one row for every recipient.</span></span> 
  
<span data-ttu-id="5e83b-124">Таблицы получателей имеют другой набор столбцов в зависимости от того, было ли отправлено сообщение.</span><span class="sxs-lookup"><span data-stu-id="5e83b-124">Recipient tables have a different column set depending on whether the message has been submitted.</span></span> <span data-ttu-id="5e83b-125">Полный список столбцов в таблице получателей см. в статье [Таблицы получателей.](recipient-tables.md)</span><span class="sxs-lookup"><span data-stu-id="5e83b-125">For a complete list of the columns in a recipient table, see [Recipient Tables](recipient-tables.md).</span></span>
  
<span data-ttu-id="5e83b-126">Некоторые таблицы получателей поддерживают широкий спектр ограничений; другие этого не делают.</span><span class="sxs-lookup"><span data-stu-id="5e83b-126">Some recipient tables support a wide variety of restrictions; others do not.</span></span> <span data-ttu-id="5e83b-127">Поддержка ограничений зависит от реализации поставщика магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="5e83b-127">Support for restrictions depends on the message store provider's implementation.</span></span> 
  
<span data-ttu-id="5e83b-128">Установка флага MAPI_UNICODE в  _параметре ulFlags_ влияет на следующие вызовы в таблицу получателей:</span><span class="sxs-lookup"><span data-stu-id="5e83b-128">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the following calls to the recipient table:</span></span> 
  
- <span data-ttu-id="5e83b-129">[IMAPITable::QueryColumns](imapitable-querycolumns.md) для получения набора столбцов.</span><span class="sxs-lookup"><span data-stu-id="5e83b-129">[IMAPITable::QueryColumns](imapitable-querycolumns.md) to retrieve the column set.</span></span> 
    
- <span data-ttu-id="5e83b-130">[IMAPITable::QueryRows](imapitable-queryrows.md) для получения строк.</span><span class="sxs-lookup"><span data-stu-id="5e83b-130">[IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve rows.</span></span> 
    
- <span data-ttu-id="5e83b-131">[IMAPITable::QuerySortOrder](imapitable-querysortorder.md) для получения порядка сортировки.</span><span class="sxs-lookup"><span data-stu-id="5e83b-131">[IMAPITable::QuerySortOrder](imapitable-querysortorder.md) to retrieve the sort order.</span></span> 
    
<span data-ttu-id="5e83b-132">Настройка флага Юникод требует, чтобы сведения для любых столбцов строк, возвращались из этих вызовов, были в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="5e83b-132">Setting the Unicode flag requests that the information for any string columns returned from these calls be in Unicode format.</span></span> <span data-ttu-id="5e83b-133">Однако, поскольку не все поставщики магазинов сообщений поддерживают Юникод, установка этого флага является только запросом.</span><span class="sxs-lookup"><span data-stu-id="5e83b-133">However, because not all message store providers support Unicode, setting this flag is only a request.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="5e83b-134">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="5e83b-134">Notes to callers</span></span>

<span data-ttu-id="5e83b-135">Вы можете изменить таблицу получателей, пока она открыта, позвонив [методу IMessage::ModifyRecipients.](imessage-modifyrecipients.md)</span><span class="sxs-lookup"><span data-stu-id="5e83b-135">You can change a recipient table while it is open by calling the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> <span data-ttu-id="5e83b-136">**ModifyRecipients** добавляет получателей, удаляет получателей или изменяет свойства получателей.</span><span class="sxs-lookup"><span data-stu-id="5e83b-136">**ModifyRecipients** adds recipients, deletes recipients, or modifies recipient properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5e83b-137">См. также</span><span class="sxs-lookup"><span data-stu-id="5e83b-137">See also</span></span>



[<span data-ttu-id="5e83b-138">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="5e83b-138">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="5e83b-139">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="5e83b-139">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="5e83b-140">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="5e83b-140">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="5e83b-141">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="5e83b-141">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

