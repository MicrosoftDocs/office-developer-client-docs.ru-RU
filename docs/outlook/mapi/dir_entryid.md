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
ms.openlocfilehash: 9ef3f37ab266469e83434d5d9bd0bc7e2ef897fa
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583346"
---
# <a name="direntryid"></a><span data-ttu-id="a05a9-103">DIR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="a05a9-103">DIR_ENTRYID</span></span>

  
  
<span data-ttu-id="a05a9-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a05a9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a05a9-105">Описание свойств идентификатора записи каталога.</span><span class="sxs-lookup"><span data-stu-id="a05a9-105">Describes the properties of a directory entry id.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a05a9-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="a05a9-106">Header file:</span></span>  <br/> |<span data-ttu-id="a05a9-107">ENTRYID.h</span><span class="sxs-lookup"><span data-stu-id="a05a9-107">entryid.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="a05a9-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="a05a9-108">Members</span></span>

 <span data-ttu-id="a05a9-109">**abFlags**</span><span class="sxs-lookup"><span data-stu-id="a05a9-109">**abFlags**</span></span>
  
> <span data-ttu-id="a05a9-110">Битовая маска флаги, который содержит сведения, описывающие этот объект.</span><span class="sxs-lookup"><span data-stu-id="a05a9-110">A bitmask of flags that provides information describing the object.</span></span> <span data-ttu-id="a05a9-111">Для получения дополнительных сведений в разделе Описание поля **abFlags** структуры [ENTRYID](entryid.md) .</span><span class="sxs-lookup"><span data-stu-id="a05a9-111">For more information, see the description of the **abFlags** field of an [ENTRYID](entryid.md) structure.</span></span> 
    
 <span data-ttu-id="a05a9-112">**muid**</span><span class="sxs-lookup"><span data-stu-id="a05a9-112">**muid**</span></span>
  
> <span data-ttu-id="a05a9-113">GUID, идентифицирующий поставщика хранилища.</span><span class="sxs-lookup"><span data-stu-id="a05a9-113">GUID that identifies the store provider.</span></span>
    
 <span data-ttu-id="a05a9-114">**ulVersion**</span><span class="sxs-lookup"><span data-stu-id="a05a9-114">**ulVersion**</span></span>
  
> <span data-ttu-id="a05a9-115">Номер версии структуры **DIR_ENTRYID** .</span><span class="sxs-lookup"><span data-stu-id="a05a9-115">The version number of the **DIR_ENTRYID** structure.</span></span> <span data-ttu-id="a05a9-116">Должен иметь значение CONTAB_VERSION.</span><span class="sxs-lookup"><span data-stu-id="a05a9-116">Must be set to CONTAB_VERSION.</span></span> 
    
 <span data-ttu-id="a05a9-117">**ulType**</span><span class="sxs-lookup"><span data-stu-id="a05a9-117">**ulType**</span></span>
  
> <span data-ttu-id="a05a9-118">Целое число, представляющее тип идентификатор записи каталога.</span><span class="sxs-lookup"><span data-stu-id="a05a9-118">An integer representing the directory entry ID type.</span></span> <span data-ttu-id="a05a9-119">Оно должно быть одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="a05a9-119">It must be one of the following values:</span></span>
    
|<span data-ttu-id="a05a9-120">**Имя**</span><span class="sxs-lookup"><span data-stu-id="a05a9-120">**Name**</span></span>|<span data-ttu-id="a05a9-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a05a9-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a05a9-122">CONTAB_ROOT</span><span class="sxs-lookup"><span data-stu-id="a05a9-122">CONTAB_ROOT</span></span>  <br/> |<span data-ttu-id="a05a9-123">Корневой папки для адресную книгу MAPI.</span><span class="sxs-lookup"><span data-stu-id="a05a9-123">The root folder for a MAPI address book.</span></span>  <br/> |
|<span data-ttu-id="a05a9-124">CONTAB_SUBROOT</span><span class="sxs-lookup"><span data-stu-id="a05a9-124">CONTAB_SUBROOT</span></span>  <br/> |<span data-ttu-id="a05a9-125">Вложенная папка, находящаяся в корневой папке объекта адресной книги MAPI.</span><span class="sxs-lookup"><span data-stu-id="a05a9-125">A subfolder contained within the root folder of the MAPI address book object.</span></span>  <br/> |
|<span data-ttu-id="a05a9-126">CONTAB_CONTAINER</span><span class="sxs-lookup"><span data-stu-id="a05a9-126">CONTAB_CONTAINER</span></span>  <br/> |<span data-ttu-id="a05a9-127">Объект-контейнер адресной книги.</span><span class="sxs-lookup"><span data-stu-id="a05a9-127">An address book container object.</span></span>  <br/> |
   
 <span data-ttu-id="a05a9-128">**muidID**</span><span class="sxs-lookup"><span data-stu-id="a05a9-128">**muidID**</span></span>
  
> <span data-ttu-id="a05a9-129">GUID, идентифицирующий объект вход в систему.</span><span class="sxs-lookup"><span data-stu-id="a05a9-129">A GUID that identifies the logon object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a05a9-130">Примечания</span><span class="sxs-lookup"><span data-stu-id="a05a9-130">Remarks</span></span>

<span data-ttu-id="a05a9-131">Структур **DIR_ENTRYID** и [CONTAB_ENTRYID](contab_entryid.md) идентичны, за исключением члена **ulType** .</span><span class="sxs-lookup"><span data-stu-id="a05a9-131">The structures **DIR_ENTRYID** and [CONTAB_ENTRYID](contab_entryid.md) are identical, except for the **ulType** member.</span></span> <span data-ttu-id="a05a9-132">Содержимое элемента **ulType** определяет, какие структуры подходит для остальных полях.</span><span class="sxs-lookup"><span data-stu-id="a05a9-132">The contents of the **ulType** member determine which structure is appropriate for the remaining fields.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a05a9-133">См. также</span><span class="sxs-lookup"><span data-stu-id="a05a9-133">See also</span></span>



[<span data-ttu-id="a05a9-134">CONTAB_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="a05a9-134">CONTAB_ENTRYID</span></span>](contab_entryid.md)


[<span data-ttu-id="a05a9-135">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="a05a9-135">MAPI Structures</span></span>](mapi-structures.md)

