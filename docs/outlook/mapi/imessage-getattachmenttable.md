---
title: Имессажежетаттачменттабле
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
ms.openlocfilehash: 9a77d335f3c8980de29dab6e14079c83bd711b43
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421174"
---
# <a name="imessagegetattachmenttable"></a><span data-ttu-id="e93b6-103">IMessage::GetAttachmentTable</span><span class="sxs-lookup"><span data-stu-id="e93b6-103">IMessage::GetAttachmentTable</span></span>

  
  
<span data-ttu-id="e93b6-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e93b6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e93b6-105">Возвращает таблицу вложений сообщения.</span><span class="sxs-lookup"><span data-stu-id="e93b6-105">Returns the message's attachment table.</span></span>
  
```cpp
HRESULT GetAttachmentTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="e93b6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e93b6-106">Parameters</span></span>

 <span data-ttu-id="e93b6-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e93b6-107">_ulFlags_</span></span>
  
> <span data-ttu-id="e93b6-108">возврата Битовая маска флагов, связанных с созданием таблицы.</span><span class="sxs-lookup"><span data-stu-id="e93b6-108">[in] Bitmask of flags that relate to the creation of the table.</span></span> <span data-ttu-id="e93b6-109">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="e93b6-109">The following flag can be set:</span></span> 
    
<span data-ttu-id="e93b6-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e93b6-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="e93b6-111">Строковые столбцы представлены в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="e93b6-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="e93b6-112">Если флаг МАПИ_УНИКОДЕ не установлен, строковые столбцы представлены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="e93b6-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
<span data-ttu-id="e93b6-113">МАПИ_ДЕФЕРРЕД_ЕРРОРС</span><span class="sxs-lookup"><span data-stu-id="e93b6-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="e93b6-114">Разрешает успешное возвращение **жетаттачменттабле** , возможно, перед тем, как таблица будет полностью доступна вызывающему клиенту.</span><span class="sxs-lookup"><span data-stu-id="e93b6-114">Allows **GetAttachmentTable** to return successfully, possibly before the table is fully available to the calling client.</span></span> <span data-ttu-id="e93b6-115">Если таблица недоступна, то выполнение последующих вызовов может привести к ошибке.</span><span class="sxs-lookup"><span data-stu-id="e93b6-115">If the table is not available, making a subsequent call to it can cause an error.</span></span> 
    
 <span data-ttu-id="e93b6-116">_Лпптабле_</span><span class="sxs-lookup"><span data-stu-id="e93b6-116">_lppTable_</span></span>
  
> <span data-ttu-id="e93b6-117">вышли Указатель на указатель на таблицу вложений.</span><span class="sxs-lookup"><span data-stu-id="e93b6-117">[out] Pointer to a pointer to the attachment table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e93b6-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e93b6-118">Return value</span></span>

<span data-ttu-id="e93b6-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="e93b6-119">S_OK</span></span> 
  
> <span data-ttu-id="e93b6-120">Таблица вложений успешно получена.</span><span class="sxs-lookup"><span data-stu-id="e93b6-120">The attachment table was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e93b6-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="e93b6-121">Remarks</span></span>

<span data-ttu-id="e93b6-122">Метод **iMessage:: жетаттачменттабле** возвращает указатель на таблицу вложений сообщения, которая включает сведения обо всех вложениях в сообщении.</span><span class="sxs-lookup"><span data-stu-id="e93b6-122">The **IMessage::GetAttachmentTable** method returns a pointer to the message's attachment table, which includes information about all of the attachments in the message.</span></span> <span data-ttu-id="e93b6-123">Клиенты могут получать доступ к вложению только с помощью таблицы вложений.</span><span class="sxs-lookup"><span data-stu-id="e93b6-123">Clients can get access to an attachment only through the attachment table.</span></span> <span data-ttu-id="e93b6-124">При получении числа вложений его свойство **пр_аттач_нум** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) клиент может использовать несколько методов **iMessage** для работы с вложением.</span><span class="sxs-lookup"><span data-stu-id="e93b6-124">By retrieving an attachment's number its **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property a client can use several of the **IMessage** methods to work with the attachment.</span></span> 
  
<span data-ttu-id="e93b6-125">Для каждого вложения существует одна строка.</span><span class="sxs-lookup"><span data-stu-id="e93b6-125">There is one row for each attachment.</span></span> <span data-ttu-id="e93b6-126">Полный список столбцов таблицы вложений приведен в разделе [таблицы вложений](attachment-tables.md).</span><span class="sxs-lookup"><span data-stu-id="e93b6-126">For a complete list of the columns in an attachment table, see [Attachment Tables](attachment-tables.md).</span></span>
  
<span data-ttu-id="e93b6-127">Как правило, вложение не отображается в таблице вложений до тех пор, пока вложение и сообщение не будут сохранены с помощью вызова [IMAPIProp:: SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="e93b6-127">An attachment usually does not appear in the attachment table until both the attachment and the message have been saved with a call to [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> <span data-ttu-id="e93b6-128">Таблицы вложений являются динамическими.</span><span class="sxs-lookup"><span data-stu-id="e93b6-128">Attachment tables are dynamic.</span></span> <span data-ttu-id="e93b6-129">Если клиент создает новое вложение, удаляет существующее вложение или изменяет одно или несколько свойств после выполнения вызовов **SaveChanges** для вложения в сообщении, таблица вложений будет обновлена в соответствии с новыми сведениями.</span><span class="sxs-lookup"><span data-stu-id="e93b6-129">If a client creates a new attachment, deletes an existing attachment, or changes one or more properties once the **SaveChanges** calls have been made on the attachment on the message, the attachment table will be updated to reflect the new information.</span></span> 
  
<span data-ttu-id="e93b6-130">Некоторые таблицы вложений поддерживают широкий спектр ограничений; другие пользователи не могут.</span><span class="sxs-lookup"><span data-stu-id="e93b6-130">Some attachment tables support a wide variety of restrictions; others do not.</span></span> <span data-ttu-id="e93b6-131">Поддержка ограничений зависит от реализации поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="e93b6-131">Support for restrictions depends on the message store provider's implementation.</span></span> 
  
<span data-ttu-id="e93b6-132">При первом открытии таблицы вложений не обязательно сортируются в определенном порядке.</span><span class="sxs-lookup"><span data-stu-id="e93b6-132">When initially opened, attachment tables are not necessarily sorted in any particular order.</span></span> 
  
<span data-ttu-id="e93b6-133">Установка флага МАПИ_УНИКОДЕ в параметре _ulFlags_ влияет на следующие вызовы таблицы вложений:</span><span class="sxs-lookup"><span data-stu-id="e93b6-133">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the following calls to the attachment table:</span></span> 
  
- <span data-ttu-id="e93b6-134">[IMAPITable:: куериколумнс](imapitable-querycolumns.md) для получения набора столбцов.</span><span class="sxs-lookup"><span data-stu-id="e93b6-134">[IMAPITable::QueryColumns](imapitable-querycolumns.md) to retrieve the column set.</span></span> 
    
- <span data-ttu-id="e93b6-135">[IMAPITable:: QueryRows](imapitable-queryrows.md) для получения строк.</span><span class="sxs-lookup"><span data-stu-id="e93b6-135">[IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve rows.</span></span> 
    
- <span data-ttu-id="e93b6-136">[IMAPITable:: куерисортордер](imapitable-querysortorder.md) для получения порядка сортировки.</span><span class="sxs-lookup"><span data-stu-id="e93b6-136">[IMAPITable::QuerySortOrder](imapitable-querysortorder.md) to retrieve the sort order.</span></span> 
    
<span data-ttu-id="e93b6-137">Установка флага Юникода требует, чтобы сведения о строковых столбцах, возвращаемых из этих вызовов, были в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="e93b6-137">Setting the Unicode flag requests that the information for any string columns returned from these calls be in Unicode format.</span></span> <span data-ttu-id="e93b6-138">Однако так как не все поставщики хранилищ сообщений поддерживают Юникод, установка этого флага является только запросом.</span><span class="sxs-lookup"><span data-stu-id="e93b6-138">However, because not all message store providers support Unicode, setting this flag is only a request.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e93b6-139">См. также</span><span class="sxs-lookup"><span data-stu-id="e93b6-139">See also</span></span>



[<span data-ttu-id="e93b6-140">IMessage::CreateAttach</span><span class="sxs-lookup"><span data-stu-id="e93b6-140">IMessage::CreateAttach</span></span>](imessage-createattach.md)
  
[<span data-ttu-id="e93b6-141">IMessage::DeleteAttach</span><span class="sxs-lookup"><span data-stu-id="e93b6-141">IMessage::DeleteAttach</span></span>](imessage-deleteattach.md)
  
[<span data-ttu-id="e93b6-142">IMessage::OpenAttach</span><span class="sxs-lookup"><span data-stu-id="e93b6-142">IMessage::OpenAttach</span></span>](imessage-openattach.md)
  
[<span data-ttu-id="e93b6-143">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="e93b6-143">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

