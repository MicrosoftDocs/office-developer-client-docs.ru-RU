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
ms.openlocfilehash: 5908069f5fa887fd9d2e3f8c0df75f2e3d69515c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579538"
---
# <a name="imessagegetrecipienttable"></a><span data-ttu-id="c287e-103">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="c287e-103">IMessage::GetRecipientTable</span></span>

  
  
<span data-ttu-id="c287e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c287e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c287e-105">Возвращает таблицу получателей сообщения.</span><span class="sxs-lookup"><span data-stu-id="c287e-105">Returns the message's recipient table.</span></span>
  
```cpp
HRESULT GetRecipientTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="c287e-106">���������</span><span class="sxs-lookup"><span data-stu-id="c287e-106">Parameters</span></span>

 <span data-ttu-id="c287e-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c287e-107">_ulFlags_</span></span>
  
> <span data-ttu-id="c287e-108">[in] Битовая маска флаги, который управляет return таблицы.</span><span class="sxs-lookup"><span data-stu-id="c287e-108">[in] Bitmask of flags that controls the return of the table.</span></span> <span data-ttu-id="c287e-109">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="c287e-109">The following flags can be set:</span></span>
    
<span data-ttu-id="c287e-110">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="c287e-110">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="c287e-111">Позволяет **GetRecipientTable** для возврата успешно, возможно перед таблице доступными для клиента.</span><span class="sxs-lookup"><span data-stu-id="c287e-111">Allows **GetRecipientTable** to return successfully, possibly before the table is fully available to the calling client.</span></span> <span data-ttu-id="c287e-112">Если в таблице не поддерживается, последующие подключения к нему может вызвать ошибку.</span><span class="sxs-lookup"><span data-stu-id="c287e-112">If the table is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="c287e-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c287e-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="c287e-114">Строковых столбцов должны быть в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="c287e-114">String columns should be in Unicode format.</span></span> <span data-ttu-id="c287e-115">Если флаг MAPI_UNICODE не установлен, столбцы строки должен быть в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="c287e-115">If the MAPI_UNICODE flag is not set, the string columns should be in ANSI format.</span></span>
    
 <span data-ttu-id="c287e-116">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="c287e-116">_lppTable_</span></span>
  
> <span data-ttu-id="c287e-117">[out] Указатель на указатель на таблицу получателей.</span><span class="sxs-lookup"><span data-stu-id="c287e-117">[out] Pointer to a pointer to the recipient table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c287e-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c287e-118">Return value</span></span>

<span data-ttu-id="c287e-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="c287e-119">S_OK</span></span> 
  
> <span data-ttu-id="c287e-120">В таблице получателей успешно возвращен.</span><span class="sxs-lookup"><span data-stu-id="c287e-120">The recipient table was returned successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c287e-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="c287e-121">Remarks</span></span>

<span data-ttu-id="c287e-122">Метод **IMessage::GetRecipientTable** возвращает указатель на таблицу получателей сообщения, в которой содержатся сведения о всех получателей сообщения.</span><span class="sxs-lookup"><span data-stu-id="c287e-122">The **IMessage::GetRecipientTable** method returns a pointer to the message's recipient table, which includes information about all of the recipients for the message.</span></span> <span data-ttu-id="c287e-123">Имеется одна строка для каждого получателя.</span><span class="sxs-lookup"><span data-stu-id="c287e-123">There is one row for every recipient.</span></span> 
  
<span data-ttu-id="c287e-124">Получателей таблицы имеют набор в зависимости от того, является ли сообщение отправлено различных столбцов.</span><span class="sxs-lookup"><span data-stu-id="c287e-124">Recipient tables have a different column set depending on whether the message has been submitted.</span></span> <span data-ttu-id="c287e-125">Полный список столбцов в таблице получателей [Получатель](recipient-tables.md)см.</span><span class="sxs-lookup"><span data-stu-id="c287e-125">For a complete list of the columns in a recipient table, see [Recipient Tables](recipient-tables.md).</span></span>
  
<span data-ttu-id="c287e-126">Некоторые получателей таблицы поддерживает широкий спектр ограничения; некоторые — нет.</span><span class="sxs-lookup"><span data-stu-id="c287e-126">Some recipient tables support a wide variety of restrictions; others do not.</span></span> <span data-ttu-id="c287e-127">Поддержка ограничений зависит от реализации поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="c287e-127">Support for restrictions depends on the message store provider's implementation.</span></span> 
  
<span data-ttu-id="c287e-128">Установка флага MAPI_UNICODE с помощью параметра _ulFlags_ влияет на следующие вызовы получателей таблицы:</span><span class="sxs-lookup"><span data-stu-id="c287e-128">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the following calls to the recipient table:</span></span> 
  
- <span data-ttu-id="c287e-129">[IMAPITable::QueryColumns](imapitable-querycolumns.md) для получения набора столбцов.</span><span class="sxs-lookup"><span data-stu-id="c287e-129">[IMAPITable::QueryColumns](imapitable-querycolumns.md) to retrieve the column set.</span></span> 
    
- <span data-ttu-id="c287e-130">[IMAPITable::QueryRows](imapitable-queryrows.md) для извлечения строк.</span><span class="sxs-lookup"><span data-stu-id="c287e-130">[IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve rows.</span></span> 
    
- <span data-ttu-id="c287e-131">[IMAPITable::QuerySortOrder](imapitable-querysortorder.md) для получения порядок сортировки.</span><span class="sxs-lookup"><span data-stu-id="c287e-131">[IMAPITable::QuerySortOrder](imapitable-querysortorder.md) to retrieve the sort order.</span></span> 
    
<span data-ttu-id="c287e-132">Настройка запросов флаг Юникод, сведения о любой строки столбцов, возвращаемых из них быть в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="c287e-132">Setting the Unicode flag requests that the information for any string columns returned from these calls be in Unicode format.</span></span> <span data-ttu-id="c287e-133">Тем не менее так как не все поставщики хранилища сообщений поддерживают Юникод, этот флаг установлен представляет собой запрос.</span><span class="sxs-lookup"><span data-stu-id="c287e-133">However, because not all message store providers support Unicode, setting this flag is only a request.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="c287e-134">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="c287e-134">Notes to callers</span></span>

<span data-ttu-id="c287e-135">Можно изменить таблице получателей, когда он открыт путем вызова метода [IMessage::ModifyRecipients](imessage-modifyrecipients.md) .</span><span class="sxs-lookup"><span data-stu-id="c287e-135">You can change a recipient table while it is open by calling the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> <span data-ttu-id="c287e-136">**ModifyRecipients** добавляет получателей, удаляет получателей и изменение параметров учетной записи получателя.</span><span class="sxs-lookup"><span data-stu-id="c287e-136">**ModifyRecipients** adds recipients, deletes recipients, or modifies recipient properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c287e-137">См. также</span><span class="sxs-lookup"><span data-stu-id="c287e-137">See also</span></span>



[<span data-ttu-id="c287e-138">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="c287e-138">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="c287e-139">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="c287e-139">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="c287e-140">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="c287e-140">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="c287e-141">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="c287e-141">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

