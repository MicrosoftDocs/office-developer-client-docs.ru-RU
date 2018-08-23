---
title: Каноническое свойство PidTagIpmNoteEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmNoteEntryId
api_type:
- HeaderDef
ms.assetid: c003f7b9-b0cd-4656-98fa-3466fda6832c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3fdaa7edef50224ff2687201c5b19f61d31f49e4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580952"
---
# <a name="pidtagipmnoteentryid-canonical-property"></a><span data-ttu-id="a4b58-103">Каноническое свойство PidTagIpmNoteEntryId</span><span class="sxs-lookup"><span data-stu-id="a4b58-103">PidTagIpmNoteEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="a4b58-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a4b58-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a4b58-105">Содержит **идентификатор записи** папки заметок Outlook.</span><span class="sxs-lookup"><span data-stu-id="a4b58-105">Contains the **EntryID** of the Outlook Notes folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a4b58-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="a4b58-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a4b58-107">PR_IPM_NOTE_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="a4b58-107">PR_IPM_NOTE_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="a4b58-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="a4b58-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a4b58-109">0x36D3</span><span class="sxs-lookup"><span data-stu-id="a4b58-109">0x36D3</span></span>  <br/> |
|<span data-ttu-id="a4b58-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="a4b58-110">Data type:</span></span>  <br/> |<span data-ttu-id="a4b58-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="a4b58-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="a4b58-112">Область:</span><span class="sxs-lookup"><span data-stu-id="a4b58-112">Area:</span></span>  <br/> |<span data-ttu-id="a4b58-113">Folder</span><span class="sxs-lookup"><span data-stu-id="a4b58-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a4b58-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="a4b58-114">Remarks</span></span>

<span data-ttu-id="a4b58-115">Это свойство хранится в папке "Входящие", а также в корневую папку хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="a4b58-115">This property is stored in the Inbox folder as well as the root folder of the message store.</span></span> <span data-ttu-id="a4b58-116">Доступ к свойству для хранилища определенное сообщение, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a4b58-116">To access the property on a specific message store, do the following:</span></span> 
  
1. <span data-ttu-id="a4b58-117">Во-первых найдите свойство в папке "Входящие".</span><span class="sxs-lookup"><span data-stu-id="a4b58-117">First, look for the property in the Inbox folder.</span></span> <span data-ttu-id="a4b58-118">Используйте [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) для получения ссылки на **Код записи** для папки "Входящие".</span><span class="sxs-lookup"><span data-stu-id="a4b58-118">Use [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) to obtain a reference to the **EntryID** for the Inbox folder.</span></span> 
    
2. <span data-ttu-id="a4b58-119">Если ** IMsgStore::GetReceiveFolder ** выполнена успешно, а затем использовать ссылку на файл **EntryID** для папки "Входящие" и [IMsgStore::OpenEntry](imsgstore-openentry.md) для открытия папки «Входящие» и получить ссылку на объект **IMAPIFolder** .</span><span class="sxs-lookup"><span data-stu-id="a4b58-119">If ** IMsgStore::GetReceiveFolder ** is successful, then use the reference to the **EntryID** of the Inbox and [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the Inbox and obtain a reference to an **IMAPIFolder** object.</span></span> 
    
3. <span data-ttu-id="a4b58-120">Если **IMsgStore::OpenEntry** выполнена успешно, затем используйте возвращенный ссылку на объект **IMAPIFolder** и [IMAPIProp::GetProps](imapiprop-getprops.md) для получения нужное свойство.</span><span class="sxs-lookup"><span data-stu-id="a4b58-120">If **IMsgStore::OpenEntry** is successful, then use the returned reference to the **IMAPIFolder** object and [IMAPIProp::GetProps](imapiprop-getprops.md) to obtain the desired property.</span></span> 
    
4. <span data-ttu-id="a4b58-121">Если не удается выполнить шаг 1, 2 или 3, найдите свойство в корневой папке.</span><span class="sxs-lookup"><span data-stu-id="a4b58-121">If Step 1, 2, or 3 fails, look for the property in the root folder.</span></span> <span data-ttu-id="a4b58-122">Для этого используйте **IMsgStore::OpenEntry**, указание NULL для **lpEntryID**, чтобы открыть корневую папку хранилища сообщений и получить ссылку на объект **IMAPIFolder** .</span><span class="sxs-lookup"><span data-stu-id="a4b58-122">To do that, use **IMsgStore::OpenEntry**, specifying NULL for **lpEntryID**, to open the root folder of the message store and obtain a reference to the **IMAPIFolder** object.</span></span> 
    
5. <span data-ttu-id="a4b58-123">При успешном открытии в корневой папке затем используйте возвращенный ссылку на объект **IMAPIFolder** и **IMAPIProp::GetProps** для получения нужное свойство.</span><span class="sxs-lookup"><span data-stu-id="a4b58-123">If opening the root folder is successful, then use the returned reference to the **IMAPIFolder** object and **IMAPIProp::GetProps** to obtain the desired property.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="a4b58-124">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a4b58-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a4b58-125">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="a4b58-125">Protocol specifications</span></span>

<span data-ttu-id="a4b58-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a4b58-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a4b58-127">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="a4b58-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a4b58-128">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a4b58-128">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a4b58-129">Задает свойства и операции по созданию и поиск специальные папки в почтовом ящике.</span><span class="sxs-lookup"><span data-stu-id="a4b58-129">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="a4b58-130">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a4b58-130">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a4b58-131">Указывает методы для подключений и настройки почтовых ящиков как делегаты и взаимодействия с объектами сообщений и календаря, когда они действовать от имени другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="a4b58-131">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a4b58-132">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="a4b58-132">Header files</span></span>

<span data-ttu-id="a4b58-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a4b58-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="a4b58-134">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="a4b58-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="a4b58-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a4b58-135">Mapitags.h</span></span>
  
> <span data-ttu-id="a4b58-136">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="a4b58-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a4b58-137">См. также</span><span class="sxs-lookup"><span data-stu-id="a4b58-137">See also</span></span>



[<span data-ttu-id="a4b58-138">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a4b58-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a4b58-139">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a4b58-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a4b58-140">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="a4b58-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a4b58-141">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="a4b58-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

