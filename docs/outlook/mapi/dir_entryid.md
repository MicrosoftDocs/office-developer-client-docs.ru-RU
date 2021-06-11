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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421237"
---
# <a name="dir_entryid"></a><span data-ttu-id="e02e3-103">DIR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="e02e3-103">DIR_ENTRYID</span></span>

  
  
<span data-ttu-id="e02e3-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e02e3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e02e3-105">Описывает свойства id записи каталога.</span><span class="sxs-lookup"><span data-stu-id="e02e3-105">Describes the properties of a directory entry id.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e02e3-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="e02e3-106">Header file:</span></span>  <br/> |<span data-ttu-id="e02e3-107">entryid.h</span><span class="sxs-lookup"><span data-stu-id="e02e3-107">entryid.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="e02e3-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="e02e3-108">Members</span></span>

 <span data-ttu-id="e02e3-109">**abFlags**</span><span class="sxs-lookup"><span data-stu-id="e02e3-109">**abFlags**</span></span>
  
> <span data-ttu-id="e02e3-110">Битмашка флагов, которая содержит сведения, описывающие объект.</span><span class="sxs-lookup"><span data-stu-id="e02e3-110">A bitmask of flags that provides information describing the object.</span></span> <span data-ttu-id="e02e3-111">Дополнительные сведения см. в описании **поля abFlags** структуры [ENTRYID.](entryid.md)</span><span class="sxs-lookup"><span data-stu-id="e02e3-111">For more information, see the description of the **abFlags** field of an [ENTRYID](entryid.md) structure.</span></span> 
    
 <span data-ttu-id="e02e3-112">**muid**</span><span class="sxs-lookup"><span data-stu-id="e02e3-112">**muid**</span></span>
  
> <span data-ttu-id="e02e3-113">GUID, идентифицирует поставщика магазина.</span><span class="sxs-lookup"><span data-stu-id="e02e3-113">GUID that identifies the store provider.</span></span>
    
 <span data-ttu-id="e02e3-114">**ulVersion**</span><span class="sxs-lookup"><span data-stu-id="e02e3-114">**ulVersion**</span></span>
  
> <span data-ttu-id="e02e3-115">Номер версии структуры **DIR_ENTRYID.**</span><span class="sxs-lookup"><span data-stu-id="e02e3-115">The version number of the **DIR_ENTRYID** structure.</span></span> <span data-ttu-id="e02e3-116">Необходимо установить CONTAB_VERSION.</span><span class="sxs-lookup"><span data-stu-id="e02e3-116">Must be set to CONTAB_VERSION.</span></span> 
    
 <span data-ttu-id="e02e3-117">**ulType**</span><span class="sxs-lookup"><span data-stu-id="e02e3-117">**ulType**</span></span>
  
> <span data-ttu-id="e02e3-118">Integer, представляющий тип ID записи каталога.</span><span class="sxs-lookup"><span data-stu-id="e02e3-118">An integer representing the directory entry ID type.</span></span> <span data-ttu-id="e02e3-119">Это должно быть одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="e02e3-119">It must be one of the following values:</span></span>
    
|<span data-ttu-id="e02e3-120">**Имя**</span><span class="sxs-lookup"><span data-stu-id="e02e3-120">**Name**</span></span>|<span data-ttu-id="e02e3-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e02e3-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e02e3-122">CONTAB_ROOT</span><span class="sxs-lookup"><span data-stu-id="e02e3-122">CONTAB_ROOT</span></span>  <br/> |<span data-ttu-id="e02e3-123">Корневая папка для адресной книги MAPI.</span><span class="sxs-lookup"><span data-stu-id="e02e3-123">The root folder for a MAPI address book.</span></span>  <br/> |
|<span data-ttu-id="e02e3-124">CONTAB_SUBROOT</span><span class="sxs-lookup"><span data-stu-id="e02e3-124">CONTAB_SUBROOT</span></span>  <br/> |<span data-ttu-id="e02e3-125">Вложенная папка, находящаяся в корневой папке объекта адресной книги MAPI.</span><span class="sxs-lookup"><span data-stu-id="e02e3-125">A subfolder contained within the root folder of the MAPI address book object.</span></span>  <br/> |
|<span data-ttu-id="e02e3-126">CONTAB_CONTAINER</span><span class="sxs-lookup"><span data-stu-id="e02e3-126">CONTAB_CONTAINER</span></span>  <br/> |<span data-ttu-id="e02e3-127">Объект-контейнер адресной книги.</span><span class="sxs-lookup"><span data-stu-id="e02e3-127">An address book container object.</span></span>  <br/> |
   
 <span data-ttu-id="e02e3-128">**muidID**</span><span class="sxs-lookup"><span data-stu-id="e02e3-128">**muidID**</span></span>
  
> <span data-ttu-id="e02e3-129">GUID, идентифицирует объект logon.</span><span class="sxs-lookup"><span data-stu-id="e02e3-129">A GUID that identifies the logon object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e02e3-130">Примечания</span><span class="sxs-lookup"><span data-stu-id="e02e3-130">Remarks</span></span>

<span data-ttu-id="e02e3-131">Структуры DIR_ENTRYID  [и CONTAB_ENTRYID](contab_entryid.md) идентичны, за исключением члена **ulType.**</span><span class="sxs-lookup"><span data-stu-id="e02e3-131">The structures **DIR_ENTRYID** and [CONTAB_ENTRYID](contab_entryid.md) are identical, except for the **ulType** member.</span></span> <span data-ttu-id="e02e3-132">Содержимое члена **ulType** определяет, какая структура подходит для остальных полей.</span><span class="sxs-lookup"><span data-stu-id="e02e3-132">The contents of the **ulType** member determine which structure is appropriate for the remaining fields.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e02e3-133">См. также</span><span class="sxs-lookup"><span data-stu-id="e02e3-133">See also</span></span>



[<span data-ttu-id="e02e3-134">CONTAB_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="e02e3-134">CONTAB_ENTRYID</span></span>](contab_entryid.md)


[<span data-ttu-id="e02e3-135">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="e02e3-135">MAPI Structures</span></span>](mapi-structures.md)

