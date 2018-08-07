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
ms.openlocfilehash: 90ae9cee915296475d7fe64952b40ab7344e89e2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809267"
---
# <a name="imessagegetrecipienttable"></a><span data-ttu-id="c1076-103">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="c1076-103">IMessage::GetRecipientTable</span></span>

  
  
<span data-ttu-id="c1076-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c1076-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c1076-105">Возвращает таблицу получателей сообщения.</span><span class="sxs-lookup"><span data-stu-id="c1076-105">Returns the message's recipient table.</span></span>
  
```cpp
HRESULT GetRecipientTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="c1076-106">���������</span><span class="sxs-lookup"><span data-stu-id="c1076-106">Parameters</span></span>

 <span data-ttu-id="c1076-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c1076-107">_ulFlags_</span></span>
  
> <span data-ttu-id="c1076-108">[in] Битовая маска флаги, который управляет return таблицы.</span><span class="sxs-lookup"><span data-stu-id="c1076-108">[in] Bitmask of flags that controls the return of the table.</span></span> <span data-ttu-id="c1076-109">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="c1076-109">The following flags can be set:</span></span>
    
<span data-ttu-id="c1076-110">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="c1076-110">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="c1076-111">Позволяет **GetRecipientTable** для возврата успешно, возможно перед таблице доступными для клиента.</span><span class="sxs-lookup"><span data-stu-id="c1076-111">Allows **GetRecipientTable** to return successfully, possibly before the table is fully available to the calling client.</span></span> <span data-ttu-id="c1076-112">Если в таблице не поддерживается, последующие подключения к нему может вызвать ошибку.</span><span class="sxs-lookup"><span data-stu-id="c1076-112">If the table is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="c1076-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c1076-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="c1076-114">Строковых столбцов должны быть в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="c1076-114">String columns should be in Unicode format.</span></span> <span data-ttu-id="c1076-115">Если флаг MAPI_UNICODE не установлен, столбцы строки должен быть в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="c1076-115">If the MAPI_UNICODE flag is not set, the string columns should be in ANSI format.</span></span>
    
 <span data-ttu-id="c1076-116">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="c1076-116">_lppTable_</span></span>
  
> <span data-ttu-id="c1076-117">[out] Указатель на указатель на таблицу получателей.</span><span class="sxs-lookup"><span data-stu-id="c1076-117">[out] Pointer to a pointer to the recipient table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c1076-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8">Return value</span></span>

<span data-ttu-id="c1076-119">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="c1076-119">S_OK</span></span> 
  
> <span data-ttu-id="c1076-120">В таблице получателей успешно возвращен.</span><span class="sxs-lookup"><span data-stu-id="c1076-120">The recipient table was returned successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c1076-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="c1076-121">Remarks</span></span>

<span data-ttu-id="c1076-122">Метод **IMessage::GetRecipientTable** возвращает указатель на таблицу получателей сообщения, в которой содержатся сведения о всех получателей сообщения.</span><span class="sxs-lookup"><span data-stu-id="c1076-122">The **IMessage::GetRecipientTable** method returns a pointer to the message's recipient table, which includes information about all of the recipients for the message.</span></span> <span data-ttu-id="c1076-123">Имеется одна строка для каждого получателя.</span><span class="sxs-lookup"><span data-stu-id="c1076-123">There is one row for every recipient.</span></span> 
  
<span data-ttu-id="c1076-124">Получателей таблицы имеют набор в зависимости от того, является ли сообщение отправлено различных столбцов.</span><span class="sxs-lookup"><span data-stu-id="c1076-124">Recipient tables have a different column set depending on whether the message has been submitted.</span></span> <span data-ttu-id="c1076-125">Полный список столбцов в таблице получателей [Получатель](recipient-tables.md)см.</span><span class="sxs-lookup"><span data-stu-id="c1076-125">For a complete list of the columns in a recipient table, see [Recipient Tables](recipient-tables.md).</span></span>
  
<span data-ttu-id="c1076-126">Некоторые получателей таблицы поддерживает широкий спектр ограничения; некоторые — нет.</span><span class="sxs-lookup"><span data-stu-id="c1076-126">Some recipient tables support a wide variety of restrictions; others do not.</span></span> <span data-ttu-id="c1076-127">Поддержка ограничений зависит от реализации поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="c1076-127">Support for restrictions depends on the message store provider's implementation.</span></span> 
  
<span data-ttu-id="c1076-128">Установка флага MAPI_UNICODE с помощью параметра _ulFlags_ влияет на следующие вызовы получателей таблицы:</span><span class="sxs-lookup"><span data-stu-id="c1076-128">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the following calls to the recipient table:</span></span> 
  
- <span data-ttu-id="c1076-129">[IMAPITable::QueryColumns](imapitable-querycolumns.md) для получения набора столбцов.</span><span class="sxs-lookup"><span data-stu-id="c1076-129">[IMAPITable::QueryColumns](imapitable-querycolumns.md) to retrieve the column set.</span></span> 
    
- <span data-ttu-id="c1076-130">[IMAPITable::QueryRows](imapitable-queryrows.md) для извлечения строк.</span><span class="sxs-lookup"><span data-stu-id="c1076-130">[IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve rows.</span></span> 
    
- <span data-ttu-id="c1076-131">[IMAPITable::QuerySortOrder](imapitable-querysortorder.md) для получения порядок сортировки.</span><span class="sxs-lookup"><span data-stu-id="c1076-131">[IMAPITable::QuerySortOrder](imapitable-querysortorder.md) to retrieve the sort order.</span></span> 
    
<span data-ttu-id="c1076-132">Настройка запросов флаг Юникод, сведения о любой строки столбцов, возвращаемых из них быть в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="c1076-132">Setting the Unicode flag requests that the information for any string columns returned from these calls be in Unicode format.</span></span> <span data-ttu-id="c1076-133">Тем не менее так как не все поставщики хранилища сообщений поддерживают Юникод, этот флаг установлен представляет собой запрос.</span><span class="sxs-lookup"><span data-stu-id="c1076-133">However, because not all message store providers support Unicode, setting this flag is only a request.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="c1076-134">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="c1076-134">Notes to callers</span></span>

<span data-ttu-id="c1076-135">Можно изменить таблице получателей, когда он открыт путем вызова метода [IMessage::ModifyRecipients](imessage-modifyrecipients.md) .</span><span class="sxs-lookup"><span data-stu-id="c1076-135">You can change a recipient table while it is open by calling the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> <span data-ttu-id="c1076-136">**ModifyRecipients** добавляет получателей, удаляет получателей и изменение параметров учетной записи получателя.</span><span class="sxs-lookup"><span data-stu-id="c1076-136">**ModifyRecipients** adds recipients, deletes recipients, or modifies recipient properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c1076-137">См. также</span><span class="sxs-lookup"><span data-stu-id="c1076-137">See also</span></span>



[<span data-ttu-id="c1076-138">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="c1076-138">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="c1076-139">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="c1076-139">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="c1076-140">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="c1076-140">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="c1076-141">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="c1076-141">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

