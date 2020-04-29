---
title: CONTAB_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 84251222-dac4-4f4d-97b9-aa0e2cd26c44
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a2a204f76b62c8c6bc6d8a4e793c936a0184dc65
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424086"
---
# <a name="contab_entryid"></a><span data-ttu-id="5ceeb-103">CONTAB_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="5ceeb-103">CONTAB_ENTRYID</span></span>

  
  
<span data-ttu-id="5ceeb-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5ceeb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5ceeb-105">Содержит идентификатор папки "Контакты".</span><span class="sxs-lookup"><span data-stu-id="5ceeb-105">Contains the entry ID of the contacts folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5ceeb-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="5ceeb-106">Header file:</span></span>  <br/> |<span data-ttu-id="5ceeb-107">мсомапиутил. h</span><span class="sxs-lookup"><span data-stu-id="5ceeb-107">msomapiutil.h</span></span>  <br/> |
   
```cpp
#pragma pack(4) 
typedef struct _contab_entryid
{
    BYTE abFlags[4];
    MAPIUID muid;
    ULONG ulVersion;
    ULONG ulType;
    ULONG ulIndex;
    ULONG cbeid;
    BYTE abeid[1];
}   CONTAB_ENTRYID, *LPCONTAB_ENTRYID;
#pragma pack() 
```

## <a name="members"></a><span data-ttu-id="5ceeb-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="5ceeb-108">Members</span></span>

 <span data-ttu-id="5ceeb-109">**абфлагс**</span><span class="sxs-lookup"><span data-stu-id="5ceeb-109">**abFlags**</span></span>
  
> <span data-ttu-id="5ceeb-110">Битовая маска флагов, предоставляющая информацию, описывающую объект.</span><span class="sxs-lookup"><span data-stu-id="5ceeb-110">A bitmask of flags that provides information describing the object.</span></span> <span data-ttu-id="5ceeb-111">Дополнительные сведения можно найти в описании поля **абфлагс** структуры [EntryID](entryid.md) .</span><span class="sxs-lookup"><span data-stu-id="5ceeb-111">For more information, see the description of the **abFlags** field of an [ENTRYID](entryid.md) structure.</span></span> 
    
 <span data-ttu-id="5ceeb-112">**Muid**</span><span class="sxs-lookup"><span data-stu-id="5ceeb-112">**muid**</span></span>
  
> <span data-ttu-id="5ceeb-113">GUID, определяющий поставщика хранилища.</span><span class="sxs-lookup"><span data-stu-id="5ceeb-113">GUID that identifies the store provider.</span></span>
    
 <span data-ttu-id="5ceeb-114">**улверсион**</span><span class="sxs-lookup"><span data-stu-id="5ceeb-114">**ulVersion**</span></span>
  
> <span data-ttu-id="5ceeb-115">Номер версии структуры **CONTAB_ENTRYID** .</span><span class="sxs-lookup"><span data-stu-id="5ceeb-115">The version number of the **CONTAB_ENTRYID** structure.</span></span> <span data-ttu-id="5ceeb-116">Необходимо задать значение CONTAB_VERSION.</span><span class="sxs-lookup"><span data-stu-id="5ceeb-116">Must be set to CONTAB_VERSION.</span></span> 
    
 <span data-ttu-id="5ceeb-117">**ултипе**</span><span class="sxs-lookup"><span data-stu-id="5ceeb-117">**ulType**</span></span>
  
> <span data-ttu-id="5ceeb-118">Целое число, представляющее тип идентификатора записи контакта.</span><span class="sxs-lookup"><span data-stu-id="5ceeb-118">An integer representing the contact entry ID type.</span></span> <span data-ttu-id="5ceeb-119">Он должен иметь одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="5ceeb-119">It must be one of the following values:</span></span>
    
|<span data-ttu-id="5ceeb-120">**Название**</span><span class="sxs-lookup"><span data-stu-id="5ceeb-120">**Name**</span></span>|<span data-ttu-id="5ceeb-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5ceeb-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5ceeb-122">CONTAB_USER</span><span class="sxs-lookup"><span data-stu-id="5ceeb-122">CONTAB_USER</span></span>  <br/> |<span data-ttu-id="5ceeb-123">Объект пользователя, отправляющего сообщение.</span><span class="sxs-lookup"><span data-stu-id="5ceeb-123">A messaging user object.</span></span>  <br/> |
|<span data-ttu-id="5ceeb-124">CONTAB_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="5ceeb-124">CONTAB_DISTLIST</span></span>  <br/> |<span data-ttu-id="5ceeb-125">Объект списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="5ceeb-125">A distribution list object.</span></span>  <br/> |
   
 <span data-ttu-id="5ceeb-126">**улиндекс**</span><span class="sxs-lookup"><span data-stu-id="5ceeb-126">**ulIndex**</span></span>
  
> <span data-ttu-id="5ceeb-127">Индекс в подмножестве свойств электронной почты.</span><span class="sxs-lookup"><span data-stu-id="5ceeb-127">The index into the email property subset.</span></span>
    
 <span data-ttu-id="5ceeb-128">**кбеид**</span><span class="sxs-lookup"><span data-stu-id="5ceeb-128">**cbeid**</span></span>
  
> <span data-ttu-id="5ceeb-129">Размер идентификатора записи контактного сообщения, связанного с данной записью в адресной книге контактов.</span><span class="sxs-lookup"><span data-stu-id="5ceeb-129">The size of the entry identifier of the Contact message associated with this entry in the Contacts Address Book.</span></span>
    
 <span data-ttu-id="5ceeb-130">**абеид**</span><span class="sxs-lookup"><span data-stu-id="5ceeb-130">**abeid**</span></span>
  
> <span data-ttu-id="5ceeb-131">Идентификатор записи контактного сообщения, связанного с этой записью в адресной книге Contacts.</span><span class="sxs-lookup"><span data-stu-id="5ceeb-131">The entry identifier of the Contact message associated with this entry in the Contacts Address Book.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5ceeb-132">Примечания</span><span class="sxs-lookup"><span data-stu-id="5ceeb-132">Remarks</span></span>

<span data-ttu-id="5ceeb-133">Адресная книга контактов — это адресная книга, содержащая все элементы контактов в папке "Контакты", у которых есть адрес электронной почты или номер факса.</span><span class="sxs-lookup"><span data-stu-id="5ceeb-133">A Contacts Address Book is an Address Book that contains all the contact items in a Contacts folder that have either an email address or a fax number.</span></span> <span data-ttu-id="5ceeb-134">Каждая запись в адресной книге контактов связана либо с адресом электронной почты, либо с номером факса.</span><span class="sxs-lookup"><span data-stu-id="5ceeb-134">Each entry in a Contacts Address Book is associated with either an email address or a fax number.</span></span> <span data-ttu-id="5ceeb-135">Так как элемент контакта может иметь до трех адресов электронной почты и три номера факса, элемент контакта можно представить в виде шести записей в адресной книге контактов.</span><span class="sxs-lookup"><span data-stu-id="5ceeb-135">Since a contact item can have up to three email addresses and three fax numbers, a contact item can be represented by up to six entries in the corresponding Contacts Address Book.</span></span>
  
<span data-ttu-id="5ceeb-136">Адресная книга контактов предназначена для поддержки пользователей, обращающихся к сообщениям электронной почты с контактами в папке "Контакты".</span><span class="sxs-lookup"><span data-stu-id="5ceeb-136">The purpose of a Contacts Address Book is to support users addressing email messages to contacts in a Contacts folder.</span></span> <span data-ttu-id="5ceeb-137">Поставщик адресной книги Contacts, поддерживаемый Microsoft Outlook 2010 и Microsoft Outlook 2013 — contab32. dll.</span><span class="sxs-lookup"><span data-stu-id="5ceeb-137">The Contacts Address Book provider that Microsoft Outlook 2010 and Microsoft Outlook 2013 support is contab32.dll.</span></span>
  
<span data-ttu-id="5ceeb-138">Структура **CONTAB_ENTRYID** поддерживает подмножество сведений, присутствующих в базовом сообщении MAPI.</span><span class="sxs-lookup"><span data-stu-id="5ceeb-138">The **CONTAB_ENTRYID** structure supports a subset of the information that is present in the underlying MAPI Contact message.</span></span> <span data-ttu-id="5ceeb-139">Он определяет Контактное сообщение, с которым связана запись адресной книги для определенных контактов.</span><span class="sxs-lookup"><span data-stu-id="5ceeb-139">It identifies the Contact message that a particular Contacts Address Book entry is associated with.</span></span> 
  
<span data-ttu-id="5ceeb-140">Поля **кбеид** и **абеид** являются допустимыми только в том случае, если для поля **ултипе** задано значение CONTAB_DISTLIST или CONTAB_USER.</span><span class="sxs-lookup"><span data-stu-id="5ceeb-140">The **cbeid** and **abeid** fields are only valid when the **ulType** field value is set to CONTAB_DISTLIST or CONTAB_USER.</span></span> <span data-ttu-id="5ceeb-141">Если для поля **ултипе** задано значение CONTAB_ROOT, CONTAB_SUBROOT или CONTAB_CONTAINER, вместо этого следует использовать структуру [DIR_ENTRYID](dir_entryid.md) .</span><span class="sxs-lookup"><span data-stu-id="5ceeb-141">When the **ulType** field value is set to CONTAB_ROOT, CONTAB_SUBROOT, or CONTAB_CONTAINER, the [DIR_ENTRYID](dir_entryid.md) structure should be used instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5ceeb-142">См. также</span><span class="sxs-lookup"><span data-stu-id="5ceeb-142">See also</span></span>



[<span data-ttu-id="5ceeb-143">DIR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="5ceeb-143">DIR_ENTRYID</span></span>](dir_entryid.md)


[<span data-ttu-id="5ceeb-144">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="5ceeb-144">MAPI Structures</span></span>](mapi-structures.md)

