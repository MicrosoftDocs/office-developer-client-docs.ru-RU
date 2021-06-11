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
# <a name="contab_entryid"></a><span data-ttu-id="3fd79-103">CONTAB_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="3fd79-103">CONTAB_ENTRYID</span></span>

  
  
<span data-ttu-id="3fd79-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3fd79-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3fd79-105">Содержит ID записи папки контактов.</span><span class="sxs-lookup"><span data-stu-id="3fd79-105">Contains the entry ID of the contacts folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3fd79-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="3fd79-106">Header file:</span></span>  <br/> |<span data-ttu-id="3fd79-107">msomapiutil.h</span><span class="sxs-lookup"><span data-stu-id="3fd79-107">msomapiutil.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="3fd79-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="3fd79-108">Members</span></span>

 <span data-ttu-id="3fd79-109">**abFlags**</span><span class="sxs-lookup"><span data-stu-id="3fd79-109">**abFlags**</span></span>
  
> <span data-ttu-id="3fd79-110">Битмашка флагов, которая содержит сведения, описывающие объект.</span><span class="sxs-lookup"><span data-stu-id="3fd79-110">A bitmask of flags that provides information describing the object.</span></span> <span data-ttu-id="3fd79-111">Дополнительные сведения см. в описании **поля abFlags** структуры [ENTRYID.](entryid.md)</span><span class="sxs-lookup"><span data-stu-id="3fd79-111">For more information, see the description of the **abFlags** field of an [ENTRYID](entryid.md) structure.</span></span> 
    
 <span data-ttu-id="3fd79-112">**muid**</span><span class="sxs-lookup"><span data-stu-id="3fd79-112">**muid**</span></span>
  
> <span data-ttu-id="3fd79-113">GUID, идентифицирует поставщика магазина.</span><span class="sxs-lookup"><span data-stu-id="3fd79-113">GUID that identifies the store provider.</span></span>
    
 <span data-ttu-id="3fd79-114">**ulVersion**</span><span class="sxs-lookup"><span data-stu-id="3fd79-114">**ulVersion**</span></span>
  
> <span data-ttu-id="3fd79-115">Номер версии структуры **CONTAB_ENTRYID.**</span><span class="sxs-lookup"><span data-stu-id="3fd79-115">The version number of the **CONTAB_ENTRYID** structure.</span></span> <span data-ttu-id="3fd79-116">Необходимо установить CONTAB_VERSION.</span><span class="sxs-lookup"><span data-stu-id="3fd79-116">Must be set to CONTAB_VERSION.</span></span> 
    
 <span data-ttu-id="3fd79-117">**ulType**</span><span class="sxs-lookup"><span data-stu-id="3fd79-117">**ulType**</span></span>
  
> <span data-ttu-id="3fd79-118">Integer, представляющий тип ID записи контакта.</span><span class="sxs-lookup"><span data-stu-id="3fd79-118">An integer representing the contact entry ID type.</span></span> <span data-ttu-id="3fd79-119">Это должно быть одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="3fd79-119">It must be one of the following values:</span></span>
    
|<span data-ttu-id="3fd79-120">**Имя**</span><span class="sxs-lookup"><span data-stu-id="3fd79-120">**Name**</span></span>|<span data-ttu-id="3fd79-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3fd79-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3fd79-122">CONTAB_USER</span><span class="sxs-lookup"><span data-stu-id="3fd79-122">CONTAB_USER</span></span>  <br/> |<span data-ttu-id="3fd79-123">Объект пользователя, отправляющего сообщение.</span><span class="sxs-lookup"><span data-stu-id="3fd79-123">A messaging user object.</span></span>  <br/> |
|<span data-ttu-id="3fd79-124">CONTAB_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="3fd79-124">CONTAB_DISTLIST</span></span>  <br/> |<span data-ttu-id="3fd79-125">Объект списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="3fd79-125">A distribution list object.</span></span>  <br/> |
   
 <span data-ttu-id="3fd79-126">**ulIndex**</span><span class="sxs-lookup"><span data-stu-id="3fd79-126">**ulIndex**</span></span>
  
> <span data-ttu-id="3fd79-127">Индекс в подмножество свойств электронной почты.</span><span class="sxs-lookup"><span data-stu-id="3fd79-127">The index into the email property subset.</span></span>
    
 <span data-ttu-id="3fd79-128">**cbeid**</span><span class="sxs-lookup"><span data-stu-id="3fd79-128">**cbeid**</span></span>
  
> <span data-ttu-id="3fd79-129">Размер идентификатора записи сообщения Контакт, связанного с этой записью в адресной книге Контактов.</span><span class="sxs-lookup"><span data-stu-id="3fd79-129">The size of the entry identifier of the Contact message associated with this entry in the Contacts Address Book.</span></span>
    
 <span data-ttu-id="3fd79-130">**abeid**</span><span class="sxs-lookup"><span data-stu-id="3fd79-130">**abeid**</span></span>
  
> <span data-ttu-id="3fd79-131">Идентификатор записи сообщения Контакт, связанного с этой записью в адресной книге Контактов.</span><span class="sxs-lookup"><span data-stu-id="3fd79-131">The entry identifier of the Contact message associated with this entry in the Contacts Address Book.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3fd79-132">Примечания</span><span class="sxs-lookup"><span data-stu-id="3fd79-132">Remarks</span></span>

<span data-ttu-id="3fd79-133">Адресная книга контактов — это адресная книга, которая содержит все контактные элементы в папке Контакты, которые имеют либо адрес электронной почты, либо номер факса.</span><span class="sxs-lookup"><span data-stu-id="3fd79-133">A Contacts Address Book is an Address Book that contains all the contact items in a Contacts folder that have either an email address or a fax number.</span></span> <span data-ttu-id="3fd79-134">Каждая запись в адресной книге Контактов связана либо с адресом электронной почты, либо с номером факса.</span><span class="sxs-lookup"><span data-stu-id="3fd79-134">Each entry in a Contacts Address Book is associated with either an email address or a fax number.</span></span> <span data-ttu-id="3fd79-135">Так как контактный элемент может иметь до трех адресов электронной почты и три факса, контактный элемент может быть представлен до шести записей в соответствующей адресной книге Контактов.</span><span class="sxs-lookup"><span data-stu-id="3fd79-135">Since a contact item can have up to three email addresses and three fax numbers, a contact item can be represented by up to six entries in the corresponding Contacts Address Book.</span></span>
  
<span data-ttu-id="3fd79-136">Цель адресной книги "Контакты" заключается в поддержке пользователей, обращающихся с сообщениями электронной почты к контактам в папке Contacts.</span><span class="sxs-lookup"><span data-stu-id="3fd79-136">The purpose of a Contacts Address Book is to support users addressing email messages to contacts in a Contacts folder.</span></span> <span data-ttu-id="3fd79-137">Поставщик адресной книги Contacts, Microsoft Outlook 2010, русская версия и Microsoft Outlook 2013, contab32.dll.</span><span class="sxs-lookup"><span data-stu-id="3fd79-137">The Contacts Address Book provider that Microsoft Outlook 2010 and Microsoft Outlook 2013 support is contab32.dll.</span></span>
  
<span data-ttu-id="3fd79-138">Структура **CONTAB_ENTRYID** поддерживает подмножество сведений, присутствующих в основном сообщении контакта MAPI.</span><span class="sxs-lookup"><span data-stu-id="3fd79-138">The **CONTAB_ENTRYID** structure supports a subset of the information that is present in the underlying MAPI Contact message.</span></span> <span data-ttu-id="3fd79-139">Он определяет сообщение Контакт, с чем связана конкретная запись адресной книги Контактов.</span><span class="sxs-lookup"><span data-stu-id="3fd79-139">It identifies the Contact message that a particular Contacts Address Book entry is associated with.</span></span> 
  
<span data-ttu-id="3fd79-140">Поля **cbeid** и **abeid** действительны только в том случае, если значение **поля ulType** CONTAB_DISTLIST или CONTAB_USER.</span><span class="sxs-lookup"><span data-stu-id="3fd79-140">The **cbeid** and **abeid** fields are only valid when the **ulType** field value is set to CONTAB_DISTLIST or CONTAB_USER.</span></span> <span data-ttu-id="3fd79-141">Если значение **поля ulType** установлено для CONTAB_ROOT, CONTAB_SUBROOT или CONTAB_CONTAINER, вместо [](dir_entryid.md) DIR_ENTRYID следует использовать структуру DIR_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="3fd79-141">When the **ulType** field value is set to CONTAB_ROOT, CONTAB_SUBROOT, or CONTAB_CONTAINER, the [DIR_ENTRYID](dir_entryid.md) structure should be used instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3fd79-142">См. также</span><span class="sxs-lookup"><span data-stu-id="3fd79-142">See also</span></span>



[<span data-ttu-id="3fd79-143">DIR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="3fd79-143">DIR_ENTRYID</span></span>](dir_entryid.md)


[<span data-ttu-id="3fd79-144">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="3fd79-144">MAPI Structures</span></span>](mapi-structures.md)

