---
title: IMessageGetAttachmentTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.GetAttachmentTable
api_type:
- COM
ms.assetid: e568917e-6085-4094-8728-89ba90a78c40
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: bf100ed916080a91366062f45b9e3349516bdb98
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588519"
---
# <a name="imessagegetattachmenttable"></a><span data-ttu-id="05882-103">IMessage::GetAttachmentTable</span><span class="sxs-lookup"><span data-stu-id="05882-103">IMessage::GetAttachmentTable</span></span>

  
  
<span data-ttu-id="05882-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="05882-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="05882-105">Возвращает таблицу вложения сообщения.</span><span class="sxs-lookup"><span data-stu-id="05882-105">Returns the message's attachment table.</span></span>
  
```cpp
HRESULT GetAttachmentTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="05882-106">���������</span><span class="sxs-lookup"><span data-stu-id="05882-106">Parameters</span></span>

 <span data-ttu-id="05882-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="05882-107">_ulFlags_</span></span>
  
> <span data-ttu-id="05882-108">[in] Битовая маска флаги, влияющие на создание таблицы.</span><span class="sxs-lookup"><span data-stu-id="05882-108">[in] Bitmask of flags that relate to the creation of the table.</span></span> <span data-ttu-id="05882-109">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="05882-109">The following flag can be set:</span></span> 
    
<span data-ttu-id="05882-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="05882-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="05882-111">Столбцы строку, в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="05882-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="05882-112">Если флаг MAPI_UNICODE не установлен, столбцы строку, в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="05882-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
<span data-ttu-id="05882-113">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="05882-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="05882-114">Позволяет **GetAttachmentTable** для возврата успешно, возможно перед таблице доступными для клиента.</span><span class="sxs-lookup"><span data-stu-id="05882-114">Allows **GetAttachmentTable** to return successfully, possibly before the table is fully available to the calling client.</span></span> <span data-ttu-id="05882-115">Если в таблице не поддерживается, последующие подключения к нему может вызвать ошибку.</span><span class="sxs-lookup"><span data-stu-id="05882-115">If the table is not available, making a subsequent call to it can cause an error.</span></span> 
    
 <span data-ttu-id="05882-116">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="05882-116">_lppTable_</span></span>
  
> <span data-ttu-id="05882-117">[out] Указатель на указатель на таблице вложений.</span><span class="sxs-lookup"><span data-stu-id="05882-117">[out] Pointer to a pointer to the attachment table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="05882-118">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="05882-118">Return value</span></span>

<span data-ttu-id="05882-119">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="05882-119">S_OK</span></span> 
  
> <span data-ttu-id="05882-120">В таблице вложений был успешно извлечен.</span><span class="sxs-lookup"><span data-stu-id="05882-120">The attachment table was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="05882-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="05882-121">Remarks</span></span>

<span data-ttu-id="05882-122">Метод **IMessage::GetAttachmentTable** возвращает указатель на сообщение вложения таблицу, в которой содержатся сведения о всех вложений в сообщения.</span><span class="sxs-lookup"><span data-stu-id="05882-122">The **IMessage::GetAttachmentTable** method returns a pointer to the message's attachment table, which includes information about all of the attachments in the message.</span></span> <span data-ttu-id="05882-123">Клиенты могут получать доступ к вложения только с помощью таблицы вложений.</span><span class="sxs-lookup"><span data-stu-id="05882-123">Clients can get access to an attachment only through the attachment table.</span></span> <span data-ttu-id="05882-124">Путем получения вложений номер его свойство **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) клиент может использовать несколько методов **IMessage** для работы с вложением.</span><span class="sxs-lookup"><span data-stu-id="05882-124">By retrieving an attachment's number its **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property a client can use several of the **IMessage** methods to work with the attachment.</span></span> 
  
<span data-ttu-id="05882-125">Имеется одна строка для каждого вложения.</span><span class="sxs-lookup"><span data-stu-id="05882-125">There is one row for each attachment.</span></span> <span data-ttu-id="05882-126">Полный список столбцов таблицы вложения [Вложения](attachment-tables.md)см.</span><span class="sxs-lookup"><span data-stu-id="05882-126">For a complete list of the columns in an attachment table, see [Attachment Tables](attachment-tables.md).</span></span>
  
<span data-ttu-id="05882-127">Вложение обычно не отображается в таблице вложений до с помощью вызова [IMAPIProp::SaveChanges](imapiprop-savechanges.md)были сохранены как вложение и сообщение.</span><span class="sxs-lookup"><span data-stu-id="05882-127">An attachment usually does not appear in the attachment table until both the attachment and the message have been saved with a call to [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> <span data-ttu-id="05882-128">Таблицы вложения являются динамическими.</span><span class="sxs-lookup"><span data-stu-id="05882-128">Attachment tables are dynamic.</span></span> <span data-ttu-id="05882-129">Если клиент создает новое вложение, удаляет существующие вложения или изменяет одного или нескольких свойств после **SaveChanges** вызовы, сделанные на вложения в сообщение, в таблице вложения будут обновлены в соответствии с новой информации.</span><span class="sxs-lookup"><span data-stu-id="05882-129">If a client creates a new attachment, deletes an existing attachment, or changes one or more properties once the **SaveChanges** calls have been made on the attachment on the message, the attachment table will be updated to reflect the new information.</span></span> 
  
<span data-ttu-id="05882-130">Некоторые таблицы вложений поддерживает широкий спектр ограничения; некоторые — нет.</span><span class="sxs-lookup"><span data-stu-id="05882-130">Some attachment tables support a wide variety of restrictions; others do not.</span></span> <span data-ttu-id="05882-131">Поддержка ограничений зависит от реализации поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="05882-131">Support for restrictions depends on the message store provider's implementation.</span></span> 
  
<span data-ttu-id="05882-132">При первом открытии таблицы вложение не сортируются обязательно в любом порядке.</span><span class="sxs-lookup"><span data-stu-id="05882-132">When initially opened, attachment tables are not necessarily sorted in any particular order.</span></span> 
  
<span data-ttu-id="05882-133">Установка флага MAPI_UNICODE с помощью параметра _ulFlags_ влияет на следующие вызовы к таблице вложений:</span><span class="sxs-lookup"><span data-stu-id="05882-133">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the following calls to the attachment table:</span></span> 
  
- <span data-ttu-id="05882-134">[IMAPITable::QueryColumns](imapitable-querycolumns.md) для получения набора столбцов.</span><span class="sxs-lookup"><span data-stu-id="05882-134">[IMAPITable::QueryColumns](imapitable-querycolumns.md) to retrieve the column set.</span></span> 
    
- <span data-ttu-id="05882-135">[IMAPITable::QueryRows](imapitable-queryrows.md) для извлечения строк.</span><span class="sxs-lookup"><span data-stu-id="05882-135">[IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve rows.</span></span> 
    
- <span data-ttu-id="05882-136">[IMAPITable::QuerySortOrder](imapitable-querysortorder.md) для получения порядок сортировки.</span><span class="sxs-lookup"><span data-stu-id="05882-136">[IMAPITable::QuerySortOrder](imapitable-querysortorder.md) to retrieve the sort order.</span></span> 
    
<span data-ttu-id="05882-137">Настройка запросов флаг Юникод, сведения о любой строки столбцов, возвращаемых из них быть в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="05882-137">Setting the Unicode flag requests that the information for any string columns returned from these calls be in Unicode format.</span></span> <span data-ttu-id="05882-138">Тем не менее так как не все поставщики хранилища сообщений поддерживают Юникод, этот флаг установлен представляет собой запрос.</span><span class="sxs-lookup"><span data-stu-id="05882-138">However, because not all message store providers support Unicode, setting this flag is only a request.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="05882-139">См. также</span><span class="sxs-lookup"><span data-stu-id="05882-139">See also</span></span>



[<span data-ttu-id="05882-140">IMessage::CreateAttach</span><span class="sxs-lookup"><span data-stu-id="05882-140">IMessage::CreateAttach</span></span>](imessage-createattach.md)
  
[<span data-ttu-id="05882-141">IMessage::DeleteAttach</span><span class="sxs-lookup"><span data-stu-id="05882-141">IMessage::DeleteAttach</span></span>](imessage-deleteattach.md)
  
[<span data-ttu-id="05882-142">IMessage::OpenAttach</span><span class="sxs-lookup"><span data-stu-id="05882-142">IMessage::OpenAttach</span></span>](imessage-openattach.md)
  
[<span data-ttu-id="05882-143">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="05882-143">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

