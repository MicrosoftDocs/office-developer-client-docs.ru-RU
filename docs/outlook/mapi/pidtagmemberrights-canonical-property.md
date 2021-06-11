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
ms.openlocfilehash: dcbf8a323f5178a5a2e39d0963dd19415ab835bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342696"
---
# <a name="pidtagmemberrights-canonical-property"></a><span data-ttu-id="255a0-103">Каноническое свойство PidTagMemberRights</span><span class="sxs-lookup"><span data-stu-id="255a0-103">PidTagMemberRights Canonical Property</span></span>

  
  
<span data-ttu-id="255a0-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="255a0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="255a0-105">Содержит набор битов, которые указывали права этого члена на папку или почтовый ящик.</span><span class="sxs-lookup"><span data-stu-id="255a0-105">Contains a set of bits that indicated the rights of this member on a folder or mailbox.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="255a0-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="255a0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="255a0-107">PR_MEMBER_RIGHTS</span><span class="sxs-lookup"><span data-stu-id="255a0-107">PR_MEMBER_RIGHTS</span></span>  <br/> |
|<span data-ttu-id="255a0-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="255a0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="255a0-109">0x6673</span><span class="sxs-lookup"><span data-stu-id="255a0-109">0x6673</span></span>  <br/> |
|<span data-ttu-id="255a0-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="255a0-110">Data type:</span></span>  <br/> |<span data-ttu-id="255a0-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="255a0-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="255a0-112">Область:</span><span class="sxs-lookup"><span data-stu-id="255a0-112">Area:</span></span>  <br/> |<span data-ttu-id="255a0-113">Управление доступом</span><span class="sxs-lookup"><span data-stu-id="255a0-113">Access Control</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="255a0-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="255a0-114">Remarks</span></span>

<span data-ttu-id="255a0-115">Это свойство используется [интерфейсом IExchangeModifyTable](iexchangemodifytableiunknown.md) для определения прав участника в папке.</span><span class="sxs-lookup"><span data-stu-id="255a0-115">This property is used by the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface to define rights of a member on a folder.</span></span> <span data-ttu-id="255a0-116">Эти права можно отображать и изменять.</span><span class="sxs-lookup"><span data-stu-id="255a0-116">These rights can be displayed and modified.</span></span> <span data-ttu-id="255a0-117">Следующие значения — это права, определенные для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="255a0-117">The following values are rights defined for this property.</span></span> 
  
<span data-ttu-id="255a0-118">frightsReadAny</span><span class="sxs-lookup"><span data-stu-id="255a0-118">frightsReadAny</span></span>
  
> <span data-ttu-id="255a0-119">Участник может читать любые сообщения.</span><span class="sxs-lookup"><span data-stu-id="255a0-119">Member can read any messages.</span></span>
    
<span data-ttu-id="255a0-120">frightsCreate</span><span class="sxs-lookup"><span data-stu-id="255a0-120">frightsCreate</span></span>
  
> <span data-ttu-id="255a0-121">Участник может создавать сообщения.</span><span class="sxs-lookup"><span data-stu-id="255a0-121">Member can create messages.</span></span>
    
<span data-ttu-id="255a0-122">frightsEditOwned</span><span class="sxs-lookup"><span data-stu-id="255a0-122">frightsEditOwned</span></span>
  
> <span data-ttu-id="255a0-123">Участник может изменять любые сообщения, которые принадлежат пользователю.</span><span class="sxs-lookup"><span data-stu-id="255a0-123">Member can edit any messages owned by the user.</span></span>
    
<span data-ttu-id="255a0-124">frightsDeleteOwned</span><span class="sxs-lookup"><span data-stu-id="255a0-124">frightsDeleteOwned</span></span>
  
> <span data-ttu-id="255a0-125">Участник может удалять любые сообщения, которые принадлежат пользователю.</span><span class="sxs-lookup"><span data-stu-id="255a0-125">Member can delete any messages owned by the user.</span></span>
    
<span data-ttu-id="255a0-126">frightsEditAny</span><span class="sxs-lookup"><span data-stu-id="255a0-126">frightsEditAny</span></span>
  
> <span data-ttu-id="255a0-127">Участник может изменить любое сообщение.</span><span class="sxs-lookup"><span data-stu-id="255a0-127">Member can edit any message.</span></span>
    
<span data-ttu-id="255a0-128">frightsDeleteAny</span><span class="sxs-lookup"><span data-stu-id="255a0-128">frightsDeleteAny</span></span>
  
> <span data-ttu-id="255a0-129">Участник может удалить любое сообщение.</span><span class="sxs-lookup"><span data-stu-id="255a0-129">Member can delete any message.</span></span>
    
<span data-ttu-id="255a0-130">frightsCreateSubfolder</span><span class="sxs-lookup"><span data-stu-id="255a0-130">frightsCreateSubfolder</span></span>
  
> <span data-ttu-id="255a0-131">Участник может создавать подмостки для папки.</span><span class="sxs-lookup"><span data-stu-id="255a0-131">Member can create subfolders for the folder.</span></span>
    
<span data-ttu-id="255a0-132">frightsOwner</span><span class="sxs-lookup"><span data-stu-id="255a0-132">frightsOwner</span></span>
  
> <span data-ttu-id="255a0-133">У участника есть все предыдущие права в папке.</span><span class="sxs-lookup"><span data-stu-id="255a0-133">Member has all the previous rights on the folder.</span></span>
    
<span data-ttu-id="255a0-134">frightsContact</span><span class="sxs-lookup"><span data-stu-id="255a0-134">frightsContact</span></span>
  
> <span data-ttu-id="255a0-135">Участник может отображать ваше имя в качестве контакта в папке.</span><span class="sxs-lookup"><span data-stu-id="255a0-135">Member can have your name appear as the contact on the folder.</span></span>
    
<span data-ttu-id="255a0-136">frightsVisible</span><span class="sxs-lookup"><span data-stu-id="255a0-136">frightsVisible</span></span>
  
> <span data-ttu-id="255a0-137">Участник может видеть, что папка существует.</span><span class="sxs-lookup"><span data-stu-id="255a0-137">Member can see that the folder exists.</span></span>
    
<span data-ttu-id="255a0-138">rightsNone</span><span class="sxs-lookup"><span data-stu-id="255a0-138">rightsNone</span></span>
  
> <span data-ttu-id="255a0-139">У участника нет прав на папку.</span><span class="sxs-lookup"><span data-stu-id="255a0-139">Member does not have rights on the folder.</span></span>
    
<span data-ttu-id="255a0-140">rightsReadOnly</span><span class="sxs-lookup"><span data-stu-id="255a0-140">rightsReadOnly</span></span>
  
> <span data-ttu-id="255a0-141">Участник может читать любое сообщение в папке.</span><span class="sxs-lookup"><span data-stu-id="255a0-141">Member can read any message in the folder.</span></span>
    
<span data-ttu-id="255a0-142">rightsReadWrite</span><span class="sxs-lookup"><span data-stu-id="255a0-142">rightsReadWrite</span></span>
  
> <span data-ttu-id="255a0-143">Участник может читать и записывать любое сообщение в папке.</span><span class="sxs-lookup"><span data-stu-id="255a0-143">Member can read from and write to any message in the folder.</span></span>
    
<span data-ttu-id="255a0-144">rightsAll</span><span class="sxs-lookup"><span data-stu-id="255a0-144">rightsAll</span></span>
  
> <span data-ttu-id="255a0-145">У участника есть все предыдущие права в папке.</span><span class="sxs-lookup"><span data-stu-id="255a0-145">Member has all the previous rights on the folder.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="255a0-146">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="255a0-146">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="255a0-147">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="255a0-147">Protocol specifications</span></span>

<span data-ttu-id="255a0-148">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="255a0-148">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="255a0-149">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="255a0-149">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="255a0-150">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="255a0-150">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="255a0-151">Обрабатывает операции папок.</span><span class="sxs-lookup"><span data-stu-id="255a0-151">Handles folder operations.</span></span>
    
<span data-ttu-id="255a0-152">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="255a0-152">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="255a0-153">Обрабатывает ирисовку списков разрешений папок, хранимых на сервере.</span><span class="sxs-lookup"><span data-stu-id="255a0-153">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
<span data-ttu-id="255a0-154">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="255a0-154">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="255a0-155">Указывает методы подключения и настройки почтовых ящиков в качестве делегатов, а также взаимодействия с элементами сообщения и календаря, когда они действуют от имени другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="255a0-155">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar items when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="255a0-156">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="255a0-156">Header files</span></span>

<span data-ttu-id="255a0-157">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="255a0-157">Mapidefs.h</span></span>
  
> <span data-ttu-id="255a0-158">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="255a0-158">Provides data type definitions.</span></span>
    
<span data-ttu-id="255a0-159">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="255a0-159">Mapitags.h</span></span>
  
> <span data-ttu-id="255a0-160">Содержит определения свойств, перечисленных в качестве связанных свойств.</span><span class="sxs-lookup"><span data-stu-id="255a0-160">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="255a0-161">См. также</span><span class="sxs-lookup"><span data-stu-id="255a0-161">See also</span></span>



[<span data-ttu-id="255a0-162">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="255a0-162">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="255a0-163">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="255a0-163">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="255a0-164">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="255a0-164">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="255a0-165">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="255a0-165">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="255a0-166">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="255a0-166">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

