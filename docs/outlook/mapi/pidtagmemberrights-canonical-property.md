---
title: Каноническое свойство PidTagMemberRights
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMemberRights
api_type:
- HeaderDef
ms.assetid: 3e526b93-1f64-41ea-b43c-5b03fe1c56ed
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a120c44a83ad5e5a822e3959417b162e8ccbdd8c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566917"
---
# <a name="pidtagmemberrights-canonical-property"></a><span data-ttu-id="aaa1c-103">Каноническое свойство PidTagMemberRights</span><span class="sxs-lookup"><span data-stu-id="aaa1c-103">PidTagMemberRights Canonical Property</span></span>

  
  
<span data-ttu-id="aaa1c-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aaa1c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aaa1c-105">Содержит набор битов, указанных правами этот член в папке или почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="aaa1c-105">Contains a set of bits that indicated the rights of this member on a folder or mailbox.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="aaa1c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="aaa1c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="aaa1c-107">PR_MEMBER_RIGHTS</span><span class="sxs-lookup"><span data-stu-id="aaa1c-107">PR_MEMBER_RIGHTS</span></span>  <br/> |
|<span data-ttu-id="aaa1c-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="aaa1c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="aaa1c-109">0x6673</span><span class="sxs-lookup"><span data-stu-id="aaa1c-109">0x6673</span></span>  <br/> |
|<span data-ttu-id="aaa1c-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="aaa1c-110">Data type:</span></span>  <br/> |<span data-ttu-id="aaa1c-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="aaa1c-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="aaa1c-112">Область:</span><span class="sxs-lookup"><span data-stu-id="aaa1c-112">Area:</span></span>  <br/> |<span data-ttu-id="aaa1c-113">Управление доступом</span><span class="sxs-lookup"><span data-stu-id="aaa1c-113">Access Control</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aaa1c-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="aaa1c-114">Remarks</span></span>

<span data-ttu-id="aaa1c-115">Это свойство используется интерфейс [IExchangeModifyTable](iexchangemodifytableiunknown.md) для определения прав элемента в папке.</span><span class="sxs-lookup"><span data-stu-id="aaa1c-115">This property is used by the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface to define rights of a member on a folder.</span></span> <span data-ttu-id="aaa1c-116">Эти права можно отображения и изменения.</span><span class="sxs-lookup"><span data-stu-id="aaa1c-116">These rights can be displayed and modified.</span></span> <span data-ttu-id="aaa1c-117">Права, определенные для этого свойства являются следующие значения.</span><span class="sxs-lookup"><span data-stu-id="aaa1c-117">The following values are rights defined for this property.</span></span> 
  
<span data-ttu-id="aaa1c-118">frightsReadAny</span><span class="sxs-lookup"><span data-stu-id="aaa1c-118">frightsReadAny</span></span>
  
> <span data-ttu-id="aaa1c-119">Член могут читать все сообщения.</span><span class="sxs-lookup"><span data-stu-id="aaa1c-119">Member can read any messages.</span></span>
    
<span data-ttu-id="aaa1c-120">frightsCreate</span><span class="sxs-lookup"><span data-stu-id="aaa1c-120">frightsCreate</span></span>
  
> <span data-ttu-id="aaa1c-121">Член можно создавать сообщения.</span><span class="sxs-lookup"><span data-stu-id="aaa1c-121">Member can create messages.</span></span>
    
<span data-ttu-id="aaa1c-122">frightsEditOwned</span><span class="sxs-lookup"><span data-stu-id="aaa1c-122">frightsEditOwned</span></span>
  
> <span data-ttu-id="aaa1c-123">Участник может изменять все сообщения, принадлежащие пользователю.</span><span class="sxs-lookup"><span data-stu-id="aaa1c-123">Member can edit any messages owned by the user.</span></span>
    
<span data-ttu-id="aaa1c-124">frightsDeleteOwned</span><span class="sxs-lookup"><span data-stu-id="aaa1c-124">frightsDeleteOwned</span></span>
  
> <span data-ttu-id="aaa1c-125">Член можно удалить все сообщения, принадлежащие пользователю.</span><span class="sxs-lookup"><span data-stu-id="aaa1c-125">Member can delete any messages owned by the user.</span></span>
    
<span data-ttu-id="aaa1c-126">frightsEditAny</span><span class="sxs-lookup"><span data-stu-id="aaa1c-126">frightsEditAny</span></span>
  
> <span data-ttu-id="aaa1c-127">Участник может изменять любые сообщения.</span><span class="sxs-lookup"><span data-stu-id="aaa1c-127">Member can edit any message.</span></span>
    
<span data-ttu-id="aaa1c-128">frightsDeleteAny</span><span class="sxs-lookup"><span data-stu-id="aaa1c-128">frightsDeleteAny</span></span>
  
> <span data-ttu-id="aaa1c-129">Член можно удалить все сообщения.</span><span class="sxs-lookup"><span data-stu-id="aaa1c-129">Member can delete any message.</span></span>
    
<span data-ttu-id="aaa1c-130">frightsCreateSubfolder</span><span class="sxs-lookup"><span data-stu-id="aaa1c-130">frightsCreateSubfolder</span></span>
  
> <span data-ttu-id="aaa1c-131">Член можно создать вложенные папки.</span><span class="sxs-lookup"><span data-stu-id="aaa1c-131">Member can create subfolders for the folder.</span></span>
    
<span data-ttu-id="aaa1c-132">frightsOwner</span><span class="sxs-lookup"><span data-stu-id="aaa1c-132">frightsOwner</span></span>
  
> <span data-ttu-id="aaa1c-133">Элемент имеет все перечисленные выше права на папку.</span><span class="sxs-lookup"><span data-stu-id="aaa1c-133">Member has all the previous rights on the folder.</span></span>
    
<span data-ttu-id="aaa1c-134">frightsContact</span><span class="sxs-lookup"><span data-stu-id="aaa1c-134">frightsContact</span></span>
  
> <span data-ttu-id="aaa1c-135">Элемент может иметь свое имя контакта в общей папке.</span><span class="sxs-lookup"><span data-stu-id="aaa1c-135">Member can have your name appear as the contact on the folder.</span></span>
    
<span data-ttu-id="aaa1c-136">frightsVisible</span><span class="sxs-lookup"><span data-stu-id="aaa1c-136">frightsVisible</span></span>
  
> <span data-ttu-id="aaa1c-137">Член можно увидеть, что папка существует.</span><span class="sxs-lookup"><span data-stu-id="aaa1c-137">Member can see that the folder exists.</span></span>
    
<span data-ttu-id="aaa1c-138">rightsNone</span><span class="sxs-lookup"><span data-stu-id="aaa1c-138">rightsNone</span></span>
  
> <span data-ttu-id="aaa1c-139">Член не имеет права на папку.</span><span class="sxs-lookup"><span data-stu-id="aaa1c-139">Member does not have rights on the folder.</span></span>
    
<span data-ttu-id="aaa1c-140">rightsReadOnly</span><span class="sxs-lookup"><span data-stu-id="aaa1c-140">rightsReadOnly</span></span>
  
> <span data-ttu-id="aaa1c-141">Член могут читать все сообщения в папке.</span><span class="sxs-lookup"><span data-stu-id="aaa1c-141">Member can read any message in the folder.</span></span>
    
<span data-ttu-id="aaa1c-142">rightsReadWrite</span><span class="sxs-lookup"><span data-stu-id="aaa1c-142">rightsReadWrite</span></span>
  
> <span data-ttu-id="aaa1c-143">Член могут выполнять чтение и запись для всех сообщений в папке.</span><span class="sxs-lookup"><span data-stu-id="aaa1c-143">Member can read from and write to any message in the folder.</span></span>
    
<span data-ttu-id="aaa1c-144">rightsAll</span><span class="sxs-lookup"><span data-stu-id="aaa1c-144">rightsAll</span></span>
  
> <span data-ttu-id="aaa1c-145">Элемент имеет все перечисленные выше права на папку.</span><span class="sxs-lookup"><span data-stu-id="aaa1c-145">Member has all the previous rights on the folder.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="aaa1c-146">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="aaa1c-146">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="aaa1c-147">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="aaa1c-147">Protocol specifications</span></span>

<span data-ttu-id="aaa1c-148">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aaa1c-148">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aaa1c-149">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="aaa1c-149">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="aaa1c-150">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aaa1c-150">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aaa1c-151">Обрабатывает операции папки.</span><span class="sxs-lookup"><span data-stu-id="aaa1c-151">Handles folder operations.</span></span>
    
<span data-ttu-id="aaa1c-152">[[MS-OXCPERM]](http://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aaa1c-152">[[MS-OXCPERM]](http://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aaa1c-153">Обрабатывает извлечения списков разрешений папки, которые хранятся на сервере.</span><span class="sxs-lookup"><span data-stu-id="aaa1c-153">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
<span data-ttu-id="aaa1c-154">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aaa1c-154">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aaa1c-155">Указывает методы для подключений и настройки почтовых ящиков как делегаты и взаимодействия с элементами календаря и сообщения, когда они действовать от имени другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="aaa1c-155">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar items when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="aaa1c-156">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="aaa1c-156">Header files</span></span>

<span data-ttu-id="aaa1c-157">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="aaa1c-157">Mapidefs.h</span></span>
  
> <span data-ttu-id="aaa1c-158">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="aaa1c-158">Provides data type definitions.</span></span>
    
<span data-ttu-id="aaa1c-159">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="aaa1c-159">Mapitags.h</span></span>
  
> <span data-ttu-id="aaa1c-160">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="aaa1c-160">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="aaa1c-161">См. также</span><span class="sxs-lookup"><span data-stu-id="aaa1c-161">See also</span></span>



[<span data-ttu-id="aaa1c-162">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="aaa1c-162">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="aaa1c-163">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="aaa1c-163">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="aaa1c-164">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="aaa1c-164">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="aaa1c-165">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="aaa1c-165">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="aaa1c-166">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="aaa1c-166">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

