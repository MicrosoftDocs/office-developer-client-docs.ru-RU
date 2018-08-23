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
ms.openlocfilehash: ff088dc5bf62f407692c9eec649ff388f79d549d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567155"
---
# <a name="contabentryid"></a><span data-ttu-id="9aec3-103">CONTAB_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="9aec3-103">CONTAB_ENTRYID</span></span>

  
  
<span data-ttu-id="9aec3-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9aec3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9aec3-105">Содержит идентификатор записи из папки «Контакты».</span><span class="sxs-lookup"><span data-stu-id="9aec3-105">Contains the entry ID of the contacts folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9aec3-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="9aec3-106">Header file:</span></span>  <br/> |<span data-ttu-id="9aec3-107">msomapiutil.h</span><span class="sxs-lookup"><span data-stu-id="9aec3-107">msomapiutil.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="9aec3-108">Members</span><span class="sxs-lookup"><span data-stu-id="9aec3-108">Members</span></span>

 <span data-ttu-id="9aec3-109">**abFlags**</span><span class="sxs-lookup"><span data-stu-id="9aec3-109">**abFlags**</span></span>
  
> <span data-ttu-id="9aec3-110">Битовая маска флаги, который содержит сведения, описывающие этот объект.</span><span class="sxs-lookup"><span data-stu-id="9aec3-110">A bitmask of flags that provides information describing the object.</span></span> <span data-ttu-id="9aec3-111">Для получения дополнительных сведений в разделе Описание поля **abFlags** структуры [ENTRYID](entryid.md) .</span><span class="sxs-lookup"><span data-stu-id="9aec3-111">For more information, see the description of the **abFlags** field of an [ENTRYID](entryid.md) structure.</span></span> 
    
 <span data-ttu-id="9aec3-112">**muid**</span><span class="sxs-lookup"><span data-stu-id="9aec3-112">**muid**</span></span>
  
> <span data-ttu-id="9aec3-113">GUID, идентифицирующий поставщика хранилища.</span><span class="sxs-lookup"><span data-stu-id="9aec3-113">GUID that identifies the store provider.</span></span>
    
 <span data-ttu-id="9aec3-114">**ulVersion**</span><span class="sxs-lookup"><span data-stu-id="9aec3-114">**ulVersion**</span></span>
  
> <span data-ttu-id="9aec3-115">Номер версии структуры **CONTAB_ENTRYID** .</span><span class="sxs-lookup"><span data-stu-id="9aec3-115">The version number of the **CONTAB_ENTRYID** structure.</span></span> <span data-ttu-id="9aec3-116">Должен иметь значение CONTAB_VERSION.</span><span class="sxs-lookup"><span data-stu-id="9aec3-116">Must be set to CONTAB_VERSION.</span></span> 
    
 <span data-ttu-id="9aec3-117">**ulType**</span><span class="sxs-lookup"><span data-stu-id="9aec3-117">**ulType**</span></span>
  
> <span data-ttu-id="9aec3-118">Целое число, представляющее тип идентификатора запись контакта.</span><span class="sxs-lookup"><span data-stu-id="9aec3-118">An integer representing the contact entry ID type.</span></span> <span data-ttu-id="9aec3-119">Оно должно быть одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="9aec3-119">It must be one of the following values:</span></span>
    
|<span data-ttu-id="9aec3-120">**Имя**</span><span class="sxs-lookup"><span data-stu-id="9aec3-120">**Name**</span></span>|<span data-ttu-id="9aec3-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9aec3-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9aec3-122">CONTAB_USER</span><span class="sxs-lookup"><span data-stu-id="9aec3-122">CONTAB_USER</span></span>  <br/> |<span data-ttu-id="9aec3-123">������ ������������, ������ ����������� �����������.</span><span class="sxs-lookup"><span data-stu-id="9aec3-123">A messaging user object.</span></span>  <br/> |
|<span data-ttu-id="9aec3-124">CONTAB_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="9aec3-124">CONTAB_DISTLIST</span></span>  <br/> |<span data-ttu-id="9aec3-125">������ ������ ��������.</span><span class="sxs-lookup"><span data-stu-id="9aec3-125">A distribution list object.</span></span>  <br/> |
   
 <span data-ttu-id="9aec3-126">**ulIndex**</span><span class="sxs-lookup"><span data-stu-id="9aec3-126">**ulIndex**</span></span>
  
> <span data-ttu-id="9aec3-127">Индекс в набор свойств электронной почты.</span><span class="sxs-lookup"><span data-stu-id="9aec3-127">The index into the email property subset.</span></span>
    
 <span data-ttu-id="9aec3-128">**cbeid**</span><span class="sxs-lookup"><span data-stu-id="9aec3-128">**cbeid**</span></span>
  
> <span data-ttu-id="9aec3-129">Размер идентификатор записи сообщения контакту, связанный с этой записи в адресной книге контакты.</span><span class="sxs-lookup"><span data-stu-id="9aec3-129">The size of the entry identifier of the Contact message associated with this entry in the Contacts Address Book.</span></span>
    
 <span data-ttu-id="9aec3-130">**abeid**</span><span class="sxs-lookup"><span data-stu-id="9aec3-130">**abeid**</span></span>
  
> <span data-ttu-id="9aec3-131">Идентификатор записи сообщения контакту, связанного с этой записи в адресной книге контакты.</span><span class="sxs-lookup"><span data-stu-id="9aec3-131">The entry identifier of the Contact message associated with this entry in the Contacts Address Book.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9aec3-132">Замечания</span><span class="sxs-lookup"><span data-stu-id="9aec3-132">Remarks</span></span>

<span data-ttu-id="9aec3-133">В адресной книге контакты является к адресной книге, которая содержит все контактов в папке Контакты, имеющие адрес электронной почты или номер факса.</span><span class="sxs-lookup"><span data-stu-id="9aec3-133">A Contacts Address Book is an Address Book that contains all the contact items in a Contacts folder that have either an email address or a fax number.</span></span> <span data-ttu-id="9aec3-134">Каждая запись в адресной книге контакты связан с адресом электронной почты или номер факса.</span><span class="sxs-lookup"><span data-stu-id="9aec3-134">Each entry in a Contacts Address Book is associated with either an email address or a fax number.</span></span> <span data-ttu-id="9aec3-135">Поскольку элемента контакта может иметь до трех адресов электронной почты и три факсов номера, элемента контакта можно представить в виде длиной не более шести записей в соответствующем Контакты адресной книги.</span><span class="sxs-lookup"><span data-stu-id="9aec3-135">Since a contact item can have up to three email addresses and three fax numbers, a contact item can be represented by up to six entries in the corresponding Contacts Address Book.</span></span>
  
<span data-ttu-id="9aec3-136">В адресной книге контакты предназначен для поддержки пользователей адресации сообщений электронной почты для контактов в папке «Контакты».</span><span class="sxs-lookup"><span data-stu-id="9aec3-136">The purpose of a Contacts Address Book is to support users addressing email messages to contacts in a Contacts folder.</span></span> <span data-ttu-id="9aec3-137">Поставщик адресной книги контакты, Microsoft Outlook 2010 и Microsoft Outlook 2013 поддерживает — contab32.dll.</span><span class="sxs-lookup"><span data-stu-id="9aec3-137">The Contacts Address Book provider that Microsoft Outlook 2010 and Microsoft Outlook 2013 support is contab32.dll.</span></span>
  
<span data-ttu-id="9aec3-138">Структура **CONTAB_ENTRYID** поддерживает подмножества данных, которые присутствуют в базовом сообщения контакту MAPI.</span><span class="sxs-lookup"><span data-stu-id="9aec3-138">The **CONTAB_ENTRYID** structure supports a subset of the information that is present in the underlying MAPI Contact message.</span></span> <span data-ttu-id="9aec3-139">Он определяет сообщение контакта, с которым связана записи контактов адресной книги.</span><span class="sxs-lookup"><span data-stu-id="9aec3-139">It identifies the Contact message that a particular Contacts Address Book entry is associated with.</span></span> 
  
<span data-ttu-id="9aec3-140">Поля **cbeid** и **abeid** действительны только значение поля **ulType** задано значение CONTAB_DISTLIST или CONTAB_USER.</span><span class="sxs-lookup"><span data-stu-id="9aec3-140">The **cbeid** and **abeid** fields are only valid when the **ulType** field value is set to CONTAB_DISTLIST or CONTAB_USER.</span></span> <span data-ttu-id="9aec3-141">Если значение поля **ulType** CONTAB_ROOT, CONTAB_SUBROOT или CONTAB_CONTAINER, должен использоваться структуры [DIR_ENTRYID](dir_entryid.md) .</span><span class="sxs-lookup"><span data-stu-id="9aec3-141">When the **ulType** field value is set to CONTAB_ROOT, CONTAB_SUBROOT, or CONTAB_CONTAINER, the [DIR_ENTRYID](dir_entryid.md) structure should be used instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9aec3-142">См. также</span><span class="sxs-lookup"><span data-stu-id="9aec3-142">See also</span></span>



[<span data-ttu-id="9aec3-143">DIR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="9aec3-143">DIR_ENTRYID</span></span>](dir_entryid.md)


[<span data-ttu-id="9aec3-144">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="9aec3-144">MAPI Structures</span></span>](mapi-structures.md)

