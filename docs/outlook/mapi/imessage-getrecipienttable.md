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
# <a name="imessagegetrecipienttable"></a><span data-ttu-id="63650-103">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="63650-103">IMessage::GetRecipientTable</span></span>

  
  
<span data-ttu-id="63650-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="63650-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="63650-105">Возвращает таблицу получателей сообщения.</span><span class="sxs-lookup"><span data-stu-id="63650-105">Returns the message's recipient table.</span></span>
  
```cpp
HRESULT GetRecipientTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="63650-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="63650-106">Parameters</span></span>

 <span data-ttu-id="63650-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="63650-107">_ulFlags_</span></span>
  
> <span data-ttu-id="63650-108">[in] Битоваяmas флагов, которая управляет возвратом таблицы.</span><span class="sxs-lookup"><span data-stu-id="63650-108">[in] Bitmask of flags that controls the return of the table.</span></span> <span data-ttu-id="63650-109">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="63650-109">The following flags can be set:</span></span>
    
<span data-ttu-id="63650-110">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="63650-110">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="63650-111">Позволяет **GetRecipientTable** успешно возвращаться, возможно, до того, как таблица будет полностью доступна вызываемому клиенту.</span><span class="sxs-lookup"><span data-stu-id="63650-111">Allows **GetRecipientTable** to return successfully, possibly before the table is fully available to the calling client.</span></span> <span data-ttu-id="63650-112">Если таблица недоступна, последующий вызов может привести к ошибке.</span><span class="sxs-lookup"><span data-stu-id="63650-112">If the table is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="63650-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="63650-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="63650-114">Строки столбцов должны быть в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="63650-114">String columns should be in Unicode format.</span></span> <span data-ttu-id="63650-115">Если флаг MAPI_UNICODE не установлен, строки столбцов должны быть в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="63650-115">If the MAPI_UNICODE flag is not set, the string columns should be in ANSI format.</span></span>
    
 <span data-ttu-id="63650-116">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="63650-116">_lppTable_</span></span>
  
> <span data-ttu-id="63650-117">[out] Указатель на указатель на таблицу получателей.</span><span class="sxs-lookup"><span data-stu-id="63650-117">[out] Pointer to a pointer to the recipient table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="63650-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="63650-118">Return value</span></span>

<span data-ttu-id="63650-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="63650-119">S_OK</span></span> 
  
> <span data-ttu-id="63650-120">Таблица получателей возвращена успешно.</span><span class="sxs-lookup"><span data-stu-id="63650-120">The recipient table was returned successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="63650-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="63650-121">Remarks</span></span>

<span data-ttu-id="63650-122">Метод **IMessage::GetRecipientTable** возвращает указатель на таблицу получателей сообщения, которая включает сведения обо всех получателях сообщения.</span><span class="sxs-lookup"><span data-stu-id="63650-122">The **IMessage::GetRecipientTable** method returns a pointer to the message's recipient table, which includes information about all of the recipients for the message.</span></span> <span data-ttu-id="63650-123">Для каждого получателя существует одна строка.</span><span class="sxs-lookup"><span data-stu-id="63650-123">There is one row for every recipient.</span></span> 
  
<span data-ttu-id="63650-124">Таблицы получателей имеют другой набор столбцов в зависимости от того, было ли сообщение отправлено.</span><span class="sxs-lookup"><span data-stu-id="63650-124">Recipient tables have a different column set depending on whether the message has been submitted.</span></span> <span data-ttu-id="63650-125">Полный список столбцов в таблице получателей см. в [таблицах получателей.](recipient-tables.md)</span><span class="sxs-lookup"><span data-stu-id="63650-125">For a complete list of the columns in a recipient table, see [Recipient Tables](recipient-tables.md).</span></span>
  
<span data-ttu-id="63650-126">Некоторые таблицы получателей поддерживают широкий спектр ограничений; другие этого не делают.</span><span class="sxs-lookup"><span data-stu-id="63650-126">Some recipient tables support a wide variety of restrictions; others do not.</span></span> <span data-ttu-id="63650-127">Поддержка ограничений зависит от реализации поставщика store сообщений.</span><span class="sxs-lookup"><span data-stu-id="63650-127">Support for restrictions depends on the message store provider's implementation.</span></span> 
  
<span data-ttu-id="63650-128">Установка флага MAPI_UNICODE в параметре  _ulFlags_ влияет на следующие вызовы таблицы получателей:</span><span class="sxs-lookup"><span data-stu-id="63650-128">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the following calls to the recipient table:</span></span> 
  
- <span data-ttu-id="63650-129">[IMAPITable::QueryColumns](imapitable-querycolumns.md) для получения набора столбцов.</span><span class="sxs-lookup"><span data-stu-id="63650-129">[IMAPITable::QueryColumns](imapitable-querycolumns.md) to retrieve the column set.</span></span> 
    
- <span data-ttu-id="63650-130">[IMAPITable::QueryRows](imapitable-queryrows.md) для получения строк.</span><span class="sxs-lookup"><span data-stu-id="63650-130">[IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve rows.</span></span> 
    
- <span data-ttu-id="63650-131">[IMAPITable::QuerySortOrder](imapitable-querysortorder.md) для получения порядка сортировки.</span><span class="sxs-lookup"><span data-stu-id="63650-131">[IMAPITable::QuerySortOrder](imapitable-querysortorder.md) to retrieve the sort order.</span></span> 
    
<span data-ttu-id="63650-132">Установка флага Юникода требует, чтобы сведения для всех строкных столбцов, возвращенных этими вызовами, были в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="63650-132">Setting the Unicode flag requests that the information for any string columns returned from these calls be in Unicode format.</span></span> <span data-ttu-id="63650-133">Однако, поскольку не все поставщики параметров хранения сообщений поддерживают Юникод, установка этого флага является только запросом.</span><span class="sxs-lookup"><span data-stu-id="63650-133">However, because not all message store providers support Unicode, setting this flag is only a request.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="63650-134">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="63650-134">Notes to callers</span></span>

<span data-ttu-id="63650-135">Вы можете изменить таблицу получателей, когда она открыта, вызывая метод [IMessage::ModifyRecipients.](imessage-modifyrecipients.md)</span><span class="sxs-lookup"><span data-stu-id="63650-135">You can change a recipient table while it is open by calling the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> <span data-ttu-id="63650-136">**ModifyRecipients** добавляет получателей, удаляет получателей или изменяет свойства получателей.</span><span class="sxs-lookup"><span data-stu-id="63650-136">**ModifyRecipients** adds recipients, deletes recipients, or modifies recipient properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="63650-137">См. также</span><span class="sxs-lookup"><span data-stu-id="63650-137">See also</span></span>



[<span data-ttu-id="63650-138">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="63650-138">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="63650-139">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="63650-139">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="63650-140">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="63650-140">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="63650-141">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="63650-141">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

