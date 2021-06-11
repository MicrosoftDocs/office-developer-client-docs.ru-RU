---
title: HrValidateIPMSubtree
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrValidateIPMSubtree
api_type:
- COM
ms.assetid: 6454c1fa-5216-4934-a908-48c634ac4a07
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6cf51985e534434c584eff4d63dfbf239121ee85
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436575"
---
# <a name="hrvalidateipmsubtree"></a><span data-ttu-id="37c78-103">HrValidateIPMSubtree</span><span class="sxs-lookup"><span data-stu-id="37c78-103">HrValidateIPMSubtree</span></span>

  
  
<span data-ttu-id="37c78-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="37c78-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="37c78-105">Добавляет стандартные папки межличностных сообщений (IPM) в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="37c78-105">Adds standard interpersonal message (IPM) folders to a message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="37c78-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="37c78-106">Header file:</span></span>  <br/> |<span data-ttu-id="37c78-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="37c78-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="37c78-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="37c78-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="37c78-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="37c78-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="37c78-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="37c78-110">Called by:</span></span>  <br/> |<span data-ttu-id="37c78-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="37c78-111">Client applications</span></span>  <br/> |
   
```cpp
HrValidateIPMSubtree(
  LPMDB lpMDB,
  ULONG ulFlags,
  ULONG FAR * lpcValues,
  LPSPropValue FAR * lppProps,
  LPMAPIERROR FAR * lppMapiError
);
```

## <a name="parameters"></a><span data-ttu-id="37c78-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="37c78-112">Parameters</span></span>

 <span data-ttu-id="37c78-113">_lpMDB_</span><span class="sxs-lookup"><span data-stu-id="37c78-113">_lpMDB_</span></span>
  
> <span data-ttu-id="37c78-114">[in] Указатель на объект магазина сообщений, к которому нужно добавить папки.</span><span class="sxs-lookup"><span data-stu-id="37c78-114">[in] Pointer to the message store object to which to add the folders.</span></span> 
    
 <span data-ttu-id="37c78-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="37c78-115">_ulFlags_</span></span>
  
> <span data-ttu-id="37c78-116">[in] Bitmask флагов, используемых для управления тем, как создаются папки.</span><span class="sxs-lookup"><span data-stu-id="37c78-116">[in] Bitmask of flags used to control how the folders are created.</span></span> <span data-ttu-id="37c78-117">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="37c78-117">The following flags can be set:</span></span>
    
<span data-ttu-id="37c78-118">MAPI_FORCE_CREATE</span><span class="sxs-lookup"><span data-stu-id="37c78-118">MAPI_FORCE_CREATE</span></span> 
  
> <span data-ttu-id="37c78-119">Папки должны проверяться перед созданием, даже если свойства магазина сообщений указывают, что они допустимы.</span><span class="sxs-lookup"><span data-stu-id="37c78-119">The folders should be verified before creation, even if message store properties indicate that they are valid.</span></span> <span data-ttu-id="37c78-120">Обычно клиентская заявка задает этот флаг, если ошибка указывает на повреждение структуры существующей папки.</span><span class="sxs-lookup"><span data-stu-id="37c78-120">A client application typically sets this flag when an error indicates that the structure of an existing folder has been damaged.</span></span> 
    
<span data-ttu-id="37c78-121">MAPI_FULL_IPM_TREE</span><span class="sxs-lookup"><span data-stu-id="37c78-121">MAPI_FULL_IPM_TREE</span></span> 
  
> <span data-ttu-id="37c78-122">Полный набор папок IPM должен быть создан в корневой папке магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="37c78-122">The full set of IPM folders should be created in the message store's root folder.</span></span> <span data-ttu-id="37c78-123">Названия папок в иерархии:</span><span class="sxs-lookup"><span data-stu-id="37c78-123">The folder titles in the hierarchy are:</span></span>
    
    - <span data-ttu-id="37c78-124">Представления папок</span><span class="sxs-lookup"><span data-stu-id="37c78-124">Folder Views</span></span>
    
    - <span data-ttu-id="37c78-125">Общие представления</span><span class="sxs-lookup"><span data-stu-id="37c78-125">Common Views</span></span>
    
    - <span data-ttu-id="37c78-126">Корень поиска\*</span><span class="sxs-lookup"><span data-stu-id="37c78-126">Search Root\*</span></span>
    
    - <span data-ttu-id="37c78-127">Подтрий IPM\*</span><span class="sxs-lookup"><span data-stu-id="37c78-127">IPM Subtree\*</span></span>
    
    - <span data-ttu-id="37c78-128">Inbox;</span><span class="sxs-lookup"><span data-stu-id="37c78-128">Inbox</span></span>
    
    - <span data-ttu-id="37c78-129">Исходящие</span><span class="sxs-lookup"><span data-stu-id="37c78-129">Outbox</span></span>
    
    - <span data-ttu-id="37c78-130">Удаленные элементы\*</span><span class="sxs-lookup"><span data-stu-id="37c78-130">Deleted Items\*</span></span>
    
    - <span data-ttu-id="37c78-131">Отправленные</span><span class="sxs-lookup"><span data-stu-id="37c78-131">Sent Items</span></span>
    
    <span data-ttu-id="37c78-132">где отмечены три папки, это минимальный набор, созданный даже \* MAPI_FULL_IPM_TREE флага.</span><span class="sxs-lookup"><span data-stu-id="37c78-132">where the three folders marked with \* are the minimum set created even when the MAPI_FULL_IPM_TREE flag has not been set.</span></span> <span data-ttu-id="37c78-133">Обычно клиентская заявка задает этот флаг, когда хранилище сообщений, в котором должны быть созданы папки, является хранилищем по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="37c78-133">A client application typically sets this flag when the message store in which the folders are to be created is the default store.</span></span>
    
 <span data-ttu-id="37c78-134">_lpcValues_</span><span class="sxs-lookup"><span data-stu-id="37c78-134">_lpcValues_</span></span>
  
> <span data-ttu-id="37c78-135">[in, out] Указатель на количество [структур SPropValue](spropvalue.md) в массиве, возвращаемом в _параметре lppProps._</span><span class="sxs-lookup"><span data-stu-id="37c78-135">[in, out] Pointer to the number of [SPropValue](spropvalue.md) structures in the array returned in the  _lppProps_ parameter.</span></span> <span data-ttu-id="37c78-136">Значение параметра  _lpcValues_ может быть нулевым, если  _lppProps_ является NULL.</span><span class="sxs-lookup"><span data-stu-id="37c78-136">The value of the  _lpcValues_ parameter can be zero if  _lppProps_ is NULL.</span></span> 
    
 <span data-ttu-id="37c78-137">_lppProps_</span><span class="sxs-lookup"><span data-stu-id="37c78-137">_lppProps_</span></span>
  
> <span data-ttu-id="37c78-138">[in, out] Указатель на указатель на массив структур **SPropValue,** содержащий значения свойств **для свойства PR_VALID_FOLDER_MASK** [(PidTagValidFolderMask)](pidtagvalidfoldermask-canonical-property.md)и для соответствующих свойств идентификатора записи папок.</span><span class="sxs-lookup"><span data-stu-id="37c78-138">[in, out] Pointer to a pointer to an array of **SPropValue** structures that contains property values for the **PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)) property and for the appropriate folder entry identifier properties.</span></span> <span data-ttu-id="37c78-139">Если **HrValidateIPMSubtree** создает почтовый ящик в хранилище сообщений, массив **SPropValue** включает идентификатор входа в почтовый ящик со специальным тегом свойства под кодом  `PROP_TAG(PT_BINARY, PROP_ID_NULL)` .</span><span class="sxs-lookup"><span data-stu-id="37c78-139">If **HrValidateIPMSubtree** creates an Inbox in the message store, the **SPropValue** array includes an Inbox entry identifier with a special property tag coded as  `PROP_TAG(PT_BINARY, PROP_ID_NULL)`.</span></span> <span data-ttu-id="37c78-140">Параметр _lppProps_ может быть NULL, что указывает на то, что реализация вызовов не требует возврата **массива SPropValue.**</span><span class="sxs-lookup"><span data-stu-id="37c78-140">The  _lppProps_ parameter can be NULL, indicating that the calling implementation does not require that an **SPropValue** array be returned.</span></span> 
    
 <span data-ttu-id="37c78-141">_lppMapiError_</span><span class="sxs-lookup"><span data-stu-id="37c78-141">_lppMapiError_</span></span>
  
> <span data-ttu-id="37c78-142">[вышел] Указатель на указатель на структуру [MAPIERROR,](mapierror.md) которая содержит сведения о версии, компоненте и контексте для ошибки.</span><span class="sxs-lookup"><span data-stu-id="37c78-142">[out] Pointer to a pointer to a [MAPIERROR](mapierror.md) structure that contains version, component, and context information for an error.</span></span> <span data-ttu-id="37c78-143">Параметр _lppMAPIError задан_ в NULL, если не возвращается структура **MAPIERROR.**</span><span class="sxs-lookup"><span data-stu-id="37c78-143">The  _lppMAPIError_ parameter is set to NULL if no **MAPIERROR** structure is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="37c78-144">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="37c78-144">Return value</span></span>

<span data-ttu-id="37c78-145">Нет.</span><span class="sxs-lookup"><span data-stu-id="37c78-145">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="37c78-146">Примечания</span><span class="sxs-lookup"><span data-stu-id="37c78-146">Remarks</span></span>

<span data-ttu-id="37c78-147">MAPI использует функцию **HrValidateIPMSubtree** для создания стандартного подтрия IPM в хранилище сообщений при первом открытие магазина или при изготовлении магазина по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="37c78-147">MAPI uses the **HrValidateIPMSubtree** function internally to construct the standard IPM subtree in a message store when the store is first opened, or when a store is made the default store.</span></span> <span data-ttu-id="37c78-148">Эта функция также может использоваться клиентских приложений для проверки или ремонта стандартных папок сообщений.</span><span class="sxs-lookup"><span data-stu-id="37c78-148">This function can also be used by client applications to validate or repair standard message folders.</span></span> 
  
 <span data-ttu-id="37c78-149">**HrValidateIPMSubtree** всегда создает папки Root и IPM Subtree в корневой папке магазина и папку "Удаленные элементы" в папке Подтрия IPM.</span><span class="sxs-lookup"><span data-stu-id="37c78-149">**HrValidateIPMSubtree** always creates the Search Root and IPM Subtree folders in the store's root folder and the Deleted Items folder in the IPM Subtree folder.</span></span> <span data-ttu-id="37c78-150">Папка подтриба IPM является корнем иерархии IPM в этом хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="37c78-150">The IPM Subtree folder is the root of the IPM hierarchy in that message store.</span></span> <span data-ttu-id="37c78-151">Корневая папка поиска может использоваться в качестве корневого подтриба для папок результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="37c78-151">The Search Root folder can be used as the root of a subtree for search-results folders.</span></span> 
  
<span data-ttu-id="37c78-152">Клиенты IPM должны отображать свое представление папки, начиная с корневой папки подтрия IPM, и показывать под ней детские папки.</span><span class="sxs-lookup"><span data-stu-id="37c78-152">IPM clients should display their folder view starting at the IPM subtree root folder and showing child folders beneath it.</span></span> <span data-ttu-id="37c78-153">Сведения в корневой папке магазина сообщений не должны отображаться в пользовательском интерфейсе клиента.</span><span class="sxs-lookup"><span data-stu-id="37c78-153">Information in the root folder of a message store should not appear in a client's user interface.</span></span> <span data-ttu-id="37c78-154">Эта функция означает, что если клиент должен скрыть сведения, эти сведения можно поместить в корневой каталог IPM, где она не видна пользователю.</span><span class="sxs-lookup"><span data-stu-id="37c78-154">This functionality means that if a client must hide information, the information can be put in the IPM subtree root directory, where it is not visible to the user.</span></span> <span data-ttu-id="37c78-155">Напротив, приложения, не вложенные в IPM, для которых сообщения и папки должны быть невидимыми для пользователя, например в серверном хранилище сообщений, могут выбрасывать их за пределы иерархии IPM.</span><span class="sxs-lookup"><span data-stu-id="37c78-155">In contrast, non-IPM applications that require messages and folders to be invisible to the user, for example in a server-based message store, can put them outside the IPM hierarchy.</span></span> 
  
 <span data-ttu-id="37c78-156">**HrValidateIPMSubtree** задает  свойство PR_VALID_FOLDER_MASK, чтобы указать, имеет ли каждая создаваемая папка IPM допустимый идентификатор входа.</span><span class="sxs-lookup"><span data-stu-id="37c78-156">**HrValidateIPMSubtree** sets the **PR_VALID_FOLDER_MASK** property to indicate whether each IPM folder it creates has a valid entry identifier.</span></span> <span data-ttu-id="37c78-157">Следующие свойства идентификатора записи в хранилище сообщений заданы идентификаторам записи соответствующих папок и возвращаются в _параметре lppProps_ вместе с **PR_VALID_FOLDER_MASK:**</span><span class="sxs-lookup"><span data-stu-id="37c78-157">The following entry identifier properties of the message store are set to the entry identifiers of the corresponding folders and returned in the  _lppProps_ parameter along with **PR_VALID_FOLDER_MASK**:</span></span> 
  
 <span data-ttu-id="37c78-158">**PR_COMMON_VIEWS_ENTRYID** [(PidTagCommonViewsEntryId)](pidtagcommonviewsentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="37c78-158">**PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="37c78-159">**PR_FINDER_ENTRYID** [(PidTagFinderEntryId)](pidtagfinderentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="37c78-159">**PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="37c78-160">**PR_IPM_OUTBOX_ENTRYID** [(PidTagIpmOutboxEntryId)](pidtagipmoutboxentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="37c78-160">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="37c78-161">**PR_IPM_SENTMAIL_ENTRYID** [(PidTagIpmSentMailEntryId)](pidtagipmsentmailentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="37c78-161">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="37c78-162">**PR_IPM_SUBTREE_ENTRYID** [(PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="37c78-162">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="37c78-163">**PR_IPM_WASTEBASKET_ENTRYID** [(PidTagIpmWastebasketEntryId)](pidtagipmwastebasketentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="37c78-163">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="37c78-164">**PR_VIEWS_ENTRYID** [(PidTagViewsEntryId)](pidtagviewsentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="37c78-164">**PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="37c78-165">Местообладатель [PROP_TAG](prop_tag.md) для почтового ящика IPM (PT_BINARY, PROP_ID_NULL).</span><span class="sxs-lookup"><span data-stu-id="37c78-165">A placeholder [PROP_TAG](prop_tag.md) for the IPM Inbox (PT_BINARY, PROP_ID_NULL).</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="37c78-166">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="37c78-166">MFCMAPI reference</span></span>

<span data-ttu-id="37c78-167">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="37c78-167">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="37c78-168">**Файл**</span><span class="sxs-lookup"><span data-stu-id="37c78-168">**File**</span></span>|<span data-ttu-id="37c78-169">**Функция**</span><span class="sxs-lookup"><span data-stu-id="37c78-169">**Function**</span></span>|<span data-ttu-id="37c78-170">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="37c78-170">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="37c78-171">MstStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="37c78-171">MstStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="37c78-172">CMsgStoreDlg::OnValidateIPMSubtree</span><span class="sxs-lookup"><span data-stu-id="37c78-172">CMsgStoreDlg::OnValidateIPMSubtree</span></span>  <br/> |<span data-ttu-id="37c78-173">MFCMAPI использует **метод HrValidateIPMSubtree** для добавления стандартных папок в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="37c78-173">MFCMAPI uses the **HrValidateIPMSubtree** method to add standard folders to a message store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="37c78-174">См. также</span><span class="sxs-lookup"><span data-stu-id="37c78-174">See also</span></span>



[<span data-ttu-id="37c78-175">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="37c78-175">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)


[<span data-ttu-id="37c78-176">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="37c78-176">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

