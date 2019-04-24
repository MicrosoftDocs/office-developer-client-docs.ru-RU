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
# <a name="pidtagmemberrights-canonical-property"></a><span data-ttu-id="ad683-103">Каноническое свойство PidTagMemberRights</span><span class="sxs-lookup"><span data-stu-id="ad683-103">PidTagMemberRights Canonical Property</span></span>

  
  
<span data-ttu-id="ad683-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ad683-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ad683-105">Содержит набор битов, в которых указаны права этого члена для папки или почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="ad683-105">Contains a set of bits that indicated the rights of this member on a folder or mailbox.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ad683-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="ad683-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ad683-107">ПР_МЕМБЕР_РИГХТС</span><span class="sxs-lookup"><span data-stu-id="ad683-107">PR_MEMBER_RIGHTS</span></span>  <br/> |
|<span data-ttu-id="ad683-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="ad683-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ad683-109">0x6673</span><span class="sxs-lookup"><span data-stu-id="ad683-109">0x6673</span></span>  <br/> |
|<span data-ttu-id="ad683-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="ad683-110">Data type:</span></span>  <br/> |<span data-ttu-id="ad683-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ad683-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ad683-112">Область:</span><span class="sxs-lookup"><span data-stu-id="ad683-112">Area:</span></span>  <br/> |<span data-ttu-id="ad683-113">Управление доступом</span><span class="sxs-lookup"><span data-stu-id="ad683-113">Access Control</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ad683-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ad683-114">Remarks</span></span>

<span data-ttu-id="ad683-115">Это свойство используется интерфейсом [иексчанжемодифитабле](iexchangemodifytableiunknown.md) для определения прав члена папки.</span><span class="sxs-lookup"><span data-stu-id="ad683-115">This property is used by the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface to define rights of a member on a folder.</span></span> <span data-ttu-id="ad683-116">Эти права могут быть отображены и изменены.</span><span class="sxs-lookup"><span data-stu-id="ad683-116">These rights can be displayed and modified.</span></span> <span data-ttu-id="ad683-117">Для этого свойства определены права, указанные ниже.</span><span class="sxs-lookup"><span data-stu-id="ad683-117">The following values are rights defined for this property.</span></span> 
  
<span data-ttu-id="ad683-118">Фригхтсреадани</span><span class="sxs-lookup"><span data-stu-id="ad683-118">frightsReadAny</span></span>
  
> <span data-ttu-id="ad683-119">Член может читать любые сообщения.</span><span class="sxs-lookup"><span data-stu-id="ad683-119">Member can read any messages.</span></span>
    
<span data-ttu-id="ad683-120">Фригхтскреате</span><span class="sxs-lookup"><span data-stu-id="ad683-120">frightsCreate</span></span>
  
> <span data-ttu-id="ad683-121">Член может создавать сообщения.</span><span class="sxs-lookup"><span data-stu-id="ad683-121">Member can create messages.</span></span>
    
<span data-ttu-id="ad683-122">Фригхтседитовнед</span><span class="sxs-lookup"><span data-stu-id="ad683-122">frightsEditOwned</span></span>
  
> <span data-ttu-id="ad683-123">Участник может изменять любые сообщения, принадлежащие пользователю.</span><span class="sxs-lookup"><span data-stu-id="ad683-123">Member can edit any messages owned by the user.</span></span>
    
<span data-ttu-id="ad683-124">Фригхтсделетеовнед</span><span class="sxs-lookup"><span data-stu-id="ad683-124">frightsDeleteOwned</span></span>
  
> <span data-ttu-id="ad683-125">Участник может удалять любые сообщения, принадлежащие пользователю.</span><span class="sxs-lookup"><span data-stu-id="ad683-125">Member can delete any messages owned by the user.</span></span>
    
<span data-ttu-id="ad683-126">Фригхтседитани</span><span class="sxs-lookup"><span data-stu-id="ad683-126">frightsEditAny</span></span>
  
> <span data-ttu-id="ad683-127">Член может изменять любое сообщение.</span><span class="sxs-lookup"><span data-stu-id="ad683-127">Member can edit any message.</span></span>
    
<span data-ttu-id="ad683-128">Фригхтсделетеани</span><span class="sxs-lookup"><span data-stu-id="ad683-128">frightsDeleteAny</span></span>
  
> <span data-ttu-id="ad683-129">Член может удалить любое сообщение.</span><span class="sxs-lookup"><span data-stu-id="ad683-129">Member can delete any message.</span></span>
    
<span data-ttu-id="ad683-130">Фригхтскреатесубфолдер</span><span class="sxs-lookup"><span data-stu-id="ad683-130">frightsCreateSubfolder</span></span>
  
> <span data-ttu-id="ad683-131">Член может создавать вложенные папки для папки.</span><span class="sxs-lookup"><span data-stu-id="ad683-131">Member can create subfolders for the folder.</span></span>
    
<span data-ttu-id="ad683-132">Фригхтсовнер</span><span class="sxs-lookup"><span data-stu-id="ad683-132">frightsOwner</span></span>
  
> <span data-ttu-id="ad683-133">Член имеет все предыдущие права для папки.</span><span class="sxs-lookup"><span data-stu-id="ad683-133">Member has all the previous rights on the folder.</span></span>
    
<span data-ttu-id="ad683-134">Фригхтсконтакт</span><span class="sxs-lookup"><span data-stu-id="ad683-134">frightsContact</span></span>
  
> <span data-ttu-id="ad683-135">Член может иметь ваше имя в виде контакта в папке.</span><span class="sxs-lookup"><span data-stu-id="ad683-135">Member can have your name appear as the contact on the folder.</span></span>
    
<span data-ttu-id="ad683-136">Фригхтсвисибле</span><span class="sxs-lookup"><span data-stu-id="ad683-136">frightsVisible</span></span>
  
> <span data-ttu-id="ad683-137">Член может видеть, что папка существует.</span><span class="sxs-lookup"><span data-stu-id="ad683-137">Member can see that the folder exists.</span></span>
    
<span data-ttu-id="ad683-138">Ригхтсноне</span><span class="sxs-lookup"><span data-stu-id="ad683-138">rightsNone</span></span>
  
> <span data-ttu-id="ad683-139">У члена нет прав на доступ к папке.</span><span class="sxs-lookup"><span data-stu-id="ad683-139">Member does not have rights on the folder.</span></span>
    
<span data-ttu-id="ad683-140">Ригхтсреадонли</span><span class="sxs-lookup"><span data-stu-id="ad683-140">rightsReadOnly</span></span>
  
> <span data-ttu-id="ad683-141">Член может читать любое сообщение в папке.</span><span class="sxs-lookup"><span data-stu-id="ad683-141">Member can read any message in the folder.</span></span>
    
<span data-ttu-id="ad683-142">Ригхтсреадврите</span><span class="sxs-lookup"><span data-stu-id="ad683-142">rightsReadWrite</span></span>
  
> <span data-ttu-id="ad683-143">Член может выполнять чтение и запись в любое сообщение в папке.</span><span class="sxs-lookup"><span data-stu-id="ad683-143">Member can read from and write to any message in the folder.</span></span>
    
<span data-ttu-id="ad683-144">Ригхтсалл</span><span class="sxs-lookup"><span data-stu-id="ad683-144">rightsAll</span></span>
  
> <span data-ttu-id="ad683-145">Член имеет все предыдущие права для папки.</span><span class="sxs-lookup"><span data-stu-id="ad683-145">Member has all the previous rights on the folder.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="ad683-146">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ad683-146">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ad683-147">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="ad683-147">Protocol specifications</span></span>

<span data-ttu-id="ad683-148">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ad683-148">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ad683-149">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="ad683-149">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ad683-150">[[MS — ОКСКФОЛД]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ad683-150">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ad683-151">Обрабатывает операции с папками.</span><span class="sxs-lookup"><span data-stu-id="ad683-151">Handles folder operations.</span></span>
    
<span data-ttu-id="ad683-152">[[MS — ОКСКПЕРМ]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ad683-152">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ad683-153">Обрабатывает получение списков разрешений на доступ к папкам, которые хранятся на сервере.</span><span class="sxs-lookup"><span data-stu-id="ad683-153">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
<span data-ttu-id="ad683-154">[[MS — ОКСОДЛГТ]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ad683-154">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ad683-155">Задает методы для подключения и настройки почтовых ящиков в качестве делегатов и взаимодействия с элементами Message и Calendar, когда они действуют от имени другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="ad683-155">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar items when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ad683-156">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="ad683-156">Header files</span></span>

<span data-ttu-id="ad683-157">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="ad683-157">Mapidefs.h</span></span>
  
> <span data-ttu-id="ad683-158">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="ad683-158">Provides data type definitions.</span></span>
    
<span data-ttu-id="ad683-159">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="ad683-159">Mapitags.h</span></span>
  
> <span data-ttu-id="ad683-160">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="ad683-160">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ad683-161">См. также</span><span class="sxs-lookup"><span data-stu-id="ad683-161">See also</span></span>



[<span data-ttu-id="ad683-162">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ad683-162">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="ad683-163">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ad683-163">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ad683-164">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="ad683-164">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ad683-165">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="ad683-165">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ad683-166">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="ad683-166">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

