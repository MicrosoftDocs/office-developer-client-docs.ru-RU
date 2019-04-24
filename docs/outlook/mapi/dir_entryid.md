---
title: DIR_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9e055269-f3bf-4b64-8384-3cbc372c0b34
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e7abcb2c86ff5cabe0b8f5664ec316244617ac09
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316676"
---
# <a name="direntryid"></a><span data-ttu-id="ebfa3-103">DIR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="ebfa3-103">DIR_ENTRYID</span></span>

  
  
<span data-ttu-id="ebfa3-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ebfa3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ebfa3-105">Описывает свойства идентификатора записи каталога.</span><span class="sxs-lookup"><span data-stu-id="ebfa3-105">Describes the properties of a directory entry id.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ebfa3-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="ebfa3-106">Header file:</span></span>  <br/> |<span data-ttu-id="ebfa3-107">код EntryID. h</span><span class="sxs-lookup"><span data-stu-id="ebfa3-107">entryid.h</span></span>  <br/> |
   
```cpp
#pragma pack(4)
typedef struct _dir_entryid
{
    BYTE abFlags[4]; 
    MAPIUID muid; 
    ULONG ulVersion; 
    ULONG ulType; 
    MAPIUID muidID; 
}   DIR_ENTRYID, *LPDIR_ENTRYID; 
#pragma pack()
```

## <a name="members"></a><span data-ttu-id="ebfa3-108">Members</span><span class="sxs-lookup"><span data-stu-id="ebfa3-108">Members</span></span>

 <span data-ttu-id="ebfa3-109">**Абфлагс**</span><span class="sxs-lookup"><span data-stu-id="ebfa3-109">**abFlags**</span></span>
  
> <span data-ttu-id="ebfa3-110">Битовая маска флагов, предоставляющая информацию, описывающую объект.</span><span class="sxs-lookup"><span data-stu-id="ebfa3-110">A bitmask of flags that provides information describing the object.</span></span> <span data-ttu-id="ebfa3-111">Дополнительные сведения можно найти в описании поля **абфлагс** структуры [EntryID](entryid.md) .</span><span class="sxs-lookup"><span data-stu-id="ebfa3-111">For more information, see the description of the **abFlags** field of an [ENTRYID](entryid.md) structure.</span></span> 
    
 <span data-ttu-id="ebfa3-112">**Muid**</span><span class="sxs-lookup"><span data-stu-id="ebfa3-112">**muid**</span></span>
  
> <span data-ttu-id="ebfa3-113">GUID, определяющий поставщика хранилища.</span><span class="sxs-lookup"><span data-stu-id="ebfa3-113">GUID that identifies the store provider.</span></span>
    
 <span data-ttu-id="ebfa3-114">**Улверсион**</span><span class="sxs-lookup"><span data-stu-id="ebfa3-114">**ulVersion**</span></span>
  
> <span data-ttu-id="ebfa3-115">Номер версии структуры **дир_ентрид** .</span><span class="sxs-lookup"><span data-stu-id="ebfa3-115">The version number of the **DIR_ENTRYID** structure.</span></span> <span data-ttu-id="ebfa3-116">Должен иметь значение КОНТАБ_ВЕРСИОН.</span><span class="sxs-lookup"><span data-stu-id="ebfa3-116">Must be set to CONTAB_VERSION.</span></span> 
    
 <span data-ttu-id="ebfa3-117">**Ултипе**</span><span class="sxs-lookup"><span data-stu-id="ebfa3-117">**ulType**</span></span>
  
> <span data-ttu-id="ebfa3-118">Целое число, представляющее тип идентификатора записи каталога.</span><span class="sxs-lookup"><span data-stu-id="ebfa3-118">An integer representing the directory entry ID type.</span></span> <span data-ttu-id="ebfa3-119">Он должен иметь одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="ebfa3-119">It must be one of the following values:</span></span>
    
|<span data-ttu-id="ebfa3-120">**Имя**</span><span class="sxs-lookup"><span data-stu-id="ebfa3-120">**Name**</span></span>|<span data-ttu-id="ebfa3-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ebfa3-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ebfa3-122">CONTAB_ROOT</span><span class="sxs-lookup"><span data-stu-id="ebfa3-122">CONTAB_ROOT</span></span>  <br/> |<span data-ttu-id="ebfa3-123">Корневая папка для адресной книги MAPI.</span><span class="sxs-lookup"><span data-stu-id="ebfa3-123">The root folder for a MAPI address book.</span></span>  <br/> |
|<span data-ttu-id="ebfa3-124">CONTAB_SUBROOT</span><span class="sxs-lookup"><span data-stu-id="ebfa3-124">CONTAB_SUBROOT</span></span>  <br/> |<span data-ttu-id="ebfa3-125">Вложенная папка, находящаяся в корневой папке объекта адресной книги MAPI.</span><span class="sxs-lookup"><span data-stu-id="ebfa3-125">A subfolder contained within the root folder of the MAPI address book object.</span></span>  <br/> |
|<span data-ttu-id="ebfa3-126">CONTAB_CONTAINER</span><span class="sxs-lookup"><span data-stu-id="ebfa3-126">CONTAB_CONTAINER</span></span>  <br/> |<span data-ttu-id="ebfa3-127">Объект-контейнер адресной книги.</span><span class="sxs-lookup"><span data-stu-id="ebfa3-127">An address book container object.</span></span>  <br/> |
   
 <span data-ttu-id="ebfa3-128">**Муидид**</span><span class="sxs-lookup"><span data-stu-id="ebfa3-128">**muidID**</span></span>
  
> <span data-ttu-id="ebfa3-129">Идентификатор GUID, определяющий объект logon.</span><span class="sxs-lookup"><span data-stu-id="ebfa3-129">A GUID that identifies the logon object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ebfa3-130">Замечания</span><span class="sxs-lookup"><span data-stu-id="ebfa3-130">Remarks</span></span>

<span data-ttu-id="ebfa3-131">Структуры **дир_ентрид** и [контаб_ентрид](contab_entryid.md) идентичны, за исключением элемента **ултипе** .</span><span class="sxs-lookup"><span data-stu-id="ebfa3-131">The structures **DIR_ENTRYID** and [CONTAB_ENTRYID](contab_entryid.md) are identical, except for the **ulType** member.</span></span> <span data-ttu-id="ebfa3-132">Содержимое элемента **ултипе** определяет, какая структура подходит для остальных полей.</span><span class="sxs-lookup"><span data-stu-id="ebfa3-132">The contents of the **ulType** member determine which structure is appropriate for the remaining fields.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ebfa3-133">См. также</span><span class="sxs-lookup"><span data-stu-id="ebfa3-133">See also</span></span>



[<span data-ttu-id="ebfa3-134">CONTAB_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="ebfa3-134">CONTAB_ENTRYID</span></span>](contab_entryid.md)


[<span data-ttu-id="ebfa3-135">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="ebfa3-135">MAPI Structures</span></span>](mapi-structures.md)

