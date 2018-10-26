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
ms.openlocfilehash: 2625b148d15c2f5ccf65eedf3a1b1f2c9d0d133e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592047"
---
# <a name="hrvalidateipmsubtree"></a><span data-ttu-id="17aea-103">HrValidateIPMSubtree</span><span class="sxs-lookup"><span data-stu-id="17aea-103">HrValidateIPMSubtree</span></span>

  
  
<span data-ttu-id="17aea-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="17aea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="17aea-105">Добавление папки электронной почты — это стандартные сообщений (IPM) хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="17aea-105">Adds standard interpersonal message (IPM) folders to a message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="17aea-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="17aea-106">Header file:</span></span>  <br/> |<span data-ttu-id="17aea-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="17aea-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="17aea-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="17aea-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="17aea-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="17aea-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="17aea-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="17aea-110">Called by:</span></span>  <br/> |<span data-ttu-id="17aea-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="17aea-111">Client applications</span></span>  <br/> |
   
```cpp
HrValidateIPMSubtree(
  LPMDB lpMDB,
  ULONG ulFlags,
  ULONG FAR * lpcValues,
  LPSPropValue FAR * lppProps,
  LPMAPIERROR FAR * lppMapiError
);
```

## <a name="parameters"></a><span data-ttu-id="17aea-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="17aea-112">Parameters</span></span>

 <span data-ttu-id="17aea-113">_lpMDB_</span><span class="sxs-lookup"><span data-stu-id="17aea-113">_lpMDB_</span></span>
  
> <span data-ttu-id="17aea-114">[in] Указатель на сообщение хранения объектов, в которую нужно добавить в папки.</span><span class="sxs-lookup"><span data-stu-id="17aea-114">[in] Pointer to the message store object to which to add the folders.</span></span> 
    
 <span data-ttu-id="17aea-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="17aea-115">_ulFlags_</span></span>
  
> <span data-ttu-id="17aea-116">[in] Битовая маска флаги, используемые для управления Создание папки.</span><span class="sxs-lookup"><span data-stu-id="17aea-116">[in] Bitmask of flags used to control how the folders are created.</span></span> <span data-ttu-id="17aea-117">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="17aea-117">The following flags can be set:</span></span>
    
<span data-ttu-id="17aea-118">MAPI_FORCE_CREATE</span><span class="sxs-lookup"><span data-stu-id="17aea-118">MAPI_FORCE_CREATE</span></span> 
  
> <span data-ttu-id="17aea-119">Папки следует проверить перед созданием, даже в том случае, если свойства хранилища сообщений показывают, что они являются допустимыми.</span><span class="sxs-lookup"><span data-stu-id="17aea-119">The folders should be verified before creation, even if message store properties indicate that they are valid.</span></span> <span data-ttu-id="17aea-120">Клиентское приложение обычно устанавливает этот флаг при появится сообщение о том поврежден структура существующую папку.</span><span class="sxs-lookup"><span data-stu-id="17aea-120">A client application typically sets this flag when an error indicates that the structure of an existing folder has been damaged.</span></span> 
    
<span data-ttu-id="17aea-121">MAPI_FULL_IPM_TREE</span><span class="sxs-lookup"><span data-stu-id="17aea-121">MAPI_FULL_IPM_TREE</span></span> 
  
> <span data-ttu-id="17aea-122">Полный набор папок IPM должны создаваться в корневую папку хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="17aea-122">The full set of IPM folders should be created in the message store's root folder.</span></span> <span data-ttu-id="17aea-123">Названия папок в иерархии являются:</span><span class="sxs-lookup"><span data-stu-id="17aea-123">The folder titles in the hierarchy are:</span></span>
    
    - <span data-ttu-id="17aea-124">Представления папок</span><span class="sxs-lookup"><span data-stu-id="17aea-124">Folder Views</span></span>
    
    - <span data-ttu-id="17aea-125">Общие представления</span><span class="sxs-lookup"><span data-stu-id="17aea-125">Common Views</span></span>
    
    - <span data-ttu-id="17aea-126">Корневая папка поиска\*</span><span class="sxs-lookup"><span data-stu-id="17aea-126">Search Root\*</span></span>
    
    - <span data-ttu-id="17aea-127">Поддерева IPM\*</span><span class="sxs-lookup"><span data-stu-id="17aea-127">IPM Subtree\*</span></span>
    
    - <span data-ttu-id="17aea-128">Inbox</span><span class="sxs-lookup"><span data-stu-id="17aea-128">Inbox</span></span>
    
    - <span data-ttu-id="17aea-129">Исходящие</span><span class="sxs-lookup"><span data-stu-id="17aea-129">Outbox</span></span>
    
    - <span data-ttu-id="17aea-130">"Удаленные"\*</span><span class="sxs-lookup"><span data-stu-id="17aea-130">Deleted Items\*</span></span>
    
    - <span data-ttu-id="17aea-131">Отправленные элементы</span><span class="sxs-lookup"><span data-stu-id="17aea-131">Sent Items</span></span>
    
    <span data-ttu-id="17aea-132">где отмеченный три папки \* являются минимальный набор создан даже в том случае, если флаг MAPI_FULL_IPM_TREE не задано.</span><span class="sxs-lookup"><span data-stu-id="17aea-132">where the three folders marked with \* are the minimum set created even when the MAPI_FULL_IPM_TREE flag has not been set.</span></span> <span data-ttu-id="17aea-133">Клиентское приложение обычно устанавливает этот флаг при хранилища сообщений, в котором будут создаваться папки — это хранилище по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="17aea-133">A client application typically sets this flag when the message store in which the folders are to be created is the default store.</span></span>
    
 <span data-ttu-id="17aea-134">_lpcValues_</span><span class="sxs-lookup"><span data-stu-id="17aea-134">_lpcValues_</span></span>
  
> <span data-ttu-id="17aea-135">[in, out] Указатель на число структур [SPropValue](spropvalue.md) в массива, возвращаемого в параметре _lppProps_ .</span><span class="sxs-lookup"><span data-stu-id="17aea-135">[in, out] Pointer to the number of [SPropValue](spropvalue.md) structures in the array returned in the  _lppProps_ parameter.</span></span> <span data-ttu-id="17aea-136">Значение параметра _lpcValues_ может быть равно нулю, если _lppProps_ имеет значение NULL.</span><span class="sxs-lookup"><span data-stu-id="17aea-136">The value of the  _lpcValues_ parameter can be zero if  _lppProps_ is NULL.</span></span> 
    
 <span data-ttu-id="17aea-137">_lppProps_</span><span class="sxs-lookup"><span data-stu-id="17aea-137">_lppProps_</span></span>
  
> <span data-ttu-id="17aea-138">[in, out] Указатель на указатель для массива структур **SPropValue** , который содержит значения свойств для свойства **PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)), а также для свойства идентификатор записи соответствующую папку.</span><span class="sxs-lookup"><span data-stu-id="17aea-138">[in, out] Pointer to a pointer to an array of **SPropValue** structures that contains property values for the **PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)) property and for the appropriate folder entry identifier properties.</span></span> <span data-ttu-id="17aea-139">Если **HrValidateIPMSubtree** создает папки "Входящие" в хранилище сообщений, массива **SPropValue** включает в себя идентификатор записи папки "Входящие" с тег специальные свойства, кодированных как `PROP_TAG(PT_BINARY, PROP_ID_NULL)`.</span><span class="sxs-lookup"><span data-stu-id="17aea-139">If **HrValidateIPMSubtree** creates an Inbox in the message store, the **SPropValue** array includes an Inbox entry identifier with a special property tag coded as  `PROP_TAG(PT_BINARY, PROP_ID_NULL)`.</span></span> <span data-ttu-id="17aea-140">Параметр _lppProps_ может быть NULL, указывающего на то, что вызывающий реализации не требуется, что возвращаться массив **SPropValue** .</span><span class="sxs-lookup"><span data-stu-id="17aea-140">The  _lppProps_ parameter can be NULL, indicating that the calling implementation does not require that an **SPropValue** array be returned.</span></span> 
    
 <span data-ttu-id="17aea-141">_lppMapiError_</span><span class="sxs-lookup"><span data-stu-id="17aea-141">_lppMapiError_</span></span>
  
> <span data-ttu-id="17aea-142">[out] Указатель на указатель на структуру [MAPIERROR](mapierror.md) , который содержит сведения о версии, компонент и контекста для ошибки.</span><span class="sxs-lookup"><span data-stu-id="17aea-142">[out] Pointer to a pointer to a [MAPIERROR](mapierror.md) structure that contains version, component, and context information for an error.</span></span> <span data-ttu-id="17aea-143">Параметр _lppMAPIError_ задано значение NULL, если структура не **MAPIERROR** возвращается.</span><span class="sxs-lookup"><span data-stu-id="17aea-143">The  _lppMAPIError_ parameter is set to NULL if no **MAPIERROR** structure is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="17aea-144">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="17aea-144">Return value</span></span>

<span data-ttu-id="17aea-145">Нет.</span><span class="sxs-lookup"><span data-stu-id="17aea-145">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="17aea-146">Замечания</span><span class="sxs-lookup"><span data-stu-id="17aea-146">Remarks</span></span>

<span data-ttu-id="17aea-147">MAPI функция **HrValidateIPMSubtree** во внутренней сети для создания стандартных поддерева IPM в хранилище сообщений при первом открытии хранилища или хранилища выполняется хранения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="17aea-147">MAPI uses the **HrValidateIPMSubtree** function internally to construct the standard IPM subtree in a message store when the store is first opened, or when a store is made the default store.</span></span> <span data-ttu-id="17aea-148">Также эта функция можно использовать с клиентскими приложениями для проверки или исправления папки стандартных сообщений.</span><span class="sxs-lookup"><span data-stu-id="17aea-148">This function can also be used by client applications to validate or repair standard message folders.</span></span> 
  
 <span data-ttu-id="17aea-149">**HrValidateIPMSubtree** всегда создает папки поиска корневые папки и поддерева IPM в хранилище корневой папки и папки «Удаленные» в папке поддерева IPM.</span><span class="sxs-lookup"><span data-stu-id="17aea-149">**HrValidateIPMSubtree** always creates the Search Root and IPM Subtree folders in the store's root folder and the Deleted Items folder in the IPM Subtree folder.</span></span> <span data-ttu-id="17aea-150">Папка поддерева IPM — корневой каталог иерархии IPM в этого хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="17aea-150">The IPM Subtree folder is the root of the IPM hierarchy in that message store.</span></span> <span data-ttu-id="17aea-151">Поиск корневую папку можно использовать в качестве корневого поддерева для результатов поиска папок.</span><span class="sxs-lookup"><span data-stu-id="17aea-151">The Search Root folder can be used as the root of a subtree for search-results folders.</span></span> 
  
<span data-ttu-id="17aea-152">Клиенты IPM должны отображать их представления папок, начиная с корневой папки поддерева IPM и отображение дочерних папок под ним.</span><span class="sxs-lookup"><span data-stu-id="17aea-152">IPM clients should display their folder view starting at the IPM subtree root folder and showing child folders beneath it.</span></span> <span data-ttu-id="17aea-153">Сведения в корневую папку хранилища сообщений не должно быть в пользовательский интерфейс клиента.</span><span class="sxs-lookup"><span data-stu-id="17aea-153">Information in the root folder of a message store should not appear in a client's user interface.</span></span> <span data-ttu-id="17aea-154">Данная функциональная возможность означает, что если это клиент должен скрывать сведения, сведения может быть помещена в корневом каталоге поддерева IPM которых не отображается для пользователя.</span><span class="sxs-lookup"><span data-stu-id="17aea-154">This functionality means that if a client must hide information, the information can be put in the IPM subtree root directory, where it is not visible to the user.</span></span> <span data-ttu-id="17aea-155">С другой стороны не являющиеся IPM приложений, которым требуется сообщений и папок быть невидимым для пользователя, например в хранилище сообщений на стороне сервера, их можно поместить за пределами иерархии IPM.</span><span class="sxs-lookup"><span data-stu-id="17aea-155">In contrast, non-IPM applications that require messages and folders to be invisible to the user, for example in a server-based message store, can put them outside the IPM hierarchy.</span></span> 
  
 <span data-ttu-id="17aea-156">**HrValidateIPMSubtree** задает свойство **PR_VALID_FOLDER_MASK** значение, указывающее, является ли каждой папки IPM, которые он создает допустимым идентификатором.</span><span class="sxs-lookup"><span data-stu-id="17aea-156">**HrValidateIPMSubtree** sets the **PR_VALID_FOLDER_MASK** property to indicate whether each IPM folder it creates has a valid entry identifier.</span></span> <span data-ttu-id="17aea-157">Следующие свойства идентификатор записи хранилища сообщений задать идентификаторы записей из соответствующих папок и возвращаются в параметре _lppProps_ , а также **PR_VALID_FOLDER_MASK**:</span><span class="sxs-lookup"><span data-stu-id="17aea-157">The following entry identifier properties of the message store are set to the entry identifiers of the corresponding folders and returned in the  _lppProps_ parameter along with **PR_VALID_FOLDER_MASK**:</span></span> 
  
 <span data-ttu-id="17aea-158">**PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="17aea-158">**PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="17aea-159">**PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="17aea-159">**PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="17aea-160">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="17aea-160">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="17aea-161">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="17aea-161">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="17aea-162">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="17aea-162">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="17aea-163">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="17aea-163">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="17aea-164">**PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="17aea-164">**PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="17aea-165">Заполнитель [PROP_TAG](prop_tag.md) для IPM папки «Входящие» (PT_BINARY, PROP_ID_NULL).</span><span class="sxs-lookup"><span data-stu-id="17aea-165">A placeholder [PROP_TAG](prop_tag.md) for the IPM Inbox (PT_BINARY, PROP_ID_NULL).</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="17aea-166">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="17aea-166">MFCMAPI reference</span></span>

<span data-ttu-id="17aea-167">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="17aea-167">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="17aea-168">**Файл**</span><span class="sxs-lookup"><span data-stu-id="17aea-168">**File**</span></span>|<span data-ttu-id="17aea-169">**Функция**</span><span class="sxs-lookup"><span data-stu-id="17aea-169">**Function**</span></span>|<span data-ttu-id="17aea-170">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="17aea-170">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="17aea-171">MstStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="17aea-171">MstStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="17aea-172">CMsgStoreDlg::OnValidateIPMSubtree</span><span class="sxs-lookup"><span data-stu-id="17aea-172">CMsgStoreDlg::OnValidateIPMSubtree</span></span>  <br/> |<span data-ttu-id="17aea-173">Mfcmapi (en) метод **HrValidateIPMSubtree** используется для добавления стандартные папки для хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="17aea-173">MFCMAPI uses the **HrValidateIPMSubtree** method to add standard folders to a message store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="17aea-174">См. также</span><span class="sxs-lookup"><span data-stu-id="17aea-174">See also</span></span>



[<span data-ttu-id="17aea-175">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="17aea-175">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)


[<span data-ttu-id="17aea-176">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="17aea-176">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

