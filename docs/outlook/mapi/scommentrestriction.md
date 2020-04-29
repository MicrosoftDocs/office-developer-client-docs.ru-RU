---
title: SCommentRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SCommentRestriction
api_type:
- COM
ms.assetid: 07631ae1-981e-4c8e-a30b-1213904fe079
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3f66f513cc16bc479dd24c53804d751a396141f4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430611"
---
# <a name="scommentrestriction"></a><span data-ttu-id="1db95-103">SCommentRestriction</span><span class="sxs-lookup"><span data-stu-id="1db95-103">SCommentRestriction</span></span>

  
  
<span data-ttu-id="1db95-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1db95-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1db95-105">Описывает ограничение комментариев, которое используется для аннотирования ограничения.</span><span class="sxs-lookup"><span data-stu-id="1db95-105">Describes a comment restriction, which is used to annotate a restriction.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1db95-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="1db95-106">Header file:</span></span>  <br/> |<span data-ttu-id="1db95-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="1db95-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SCommentRestriction
{
  ULONG          cValues;
  LPSRestriction lpRes;
  LPSPropValue   lpProp;
} SCommentRestriction;

```

## <a name="members"></a><span data-ttu-id="1db95-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="1db95-108">Members</span></span>

 <span data-ttu-id="1db95-109">**квалуес**</span><span class="sxs-lookup"><span data-stu-id="1db95-109">**cValues**</span></span>
  
> <span data-ttu-id="1db95-110">Количество значений свойств в массиве, на который указывает элемент **лппроп** .</span><span class="sxs-lookup"><span data-stu-id="1db95-110">Count of property values in the array pointed to by the **lpProp** member.</span></span> 
    
 <span data-ttu-id="1db95-111">**лпрес**</span><span class="sxs-lookup"><span data-stu-id="1db95-111">**lpRes**</span></span>
  
> <span data-ttu-id="1db95-112">Указатель на структуру [срестриктион](srestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="1db95-112">Pointer to an [SRestriction](srestriction.md) structure.</span></span> 
    
 <span data-ttu-id="1db95-113">**лппроп**</span><span class="sxs-lookup"><span data-stu-id="1db95-113">**lpProp**</span></span>
  
> <span data-ttu-id="1db95-114">Указатель на массив структур [спропвалуе](spropvalue.md) , каждый из которых содержит тег свойства и значение для именованного свойства.</span><span class="sxs-lookup"><span data-stu-id="1db95-114">Pointer to an array of [SPropValue](spropvalue.md) structures, each containing the property tag and value for a named property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="1db95-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="1db95-115">Remarks</span></span>

<span data-ttu-id="1db95-116">Структура **скомментрестриктион** связывает объект вместе с набором именованных свойств.</span><span class="sxs-lookup"><span data-stu-id="1db95-116">The **SCommentRestriction** structure associates an object together with a set of named properties.</span></span> <span data-ttu-id="1db95-117">Ограничения комментариев в отличие от других ограничений, так как они не оцениваются.</span><span class="sxs-lookup"><span data-stu-id="1db95-117">Comment restrictions are unlike other restrictions because they are not evaluated.</span></span> <span data-ttu-id="1db95-118">То есть они игнорируются методом [IMAPITable:: restrict](imapitable-restrict.md) .</span><span class="sxs-lookup"><span data-stu-id="1db95-118">That is, they are ignored by the [IMAPITable::Restrict](imapitable-restrict.md) method.</span></span> <span data-ttu-id="1db95-119">Не выполняется никаких действий для строк, возвращаемых методом [IMAPITable:: QueryRows](imapitable-queryrows.md) после выполнения вызова метода **IMAPITable:: restrict** .</span><span class="sxs-lookup"><span data-stu-id="1db95-119">There is no effect on the rows returned by the [IMAPITable::QueryRows](imapitable-queryrows.md) method after an **IMAPITable::Restrict** call has been made.</span></span> 
  
<span data-ttu-id="1db95-120">Структуру **скомментрестриктион** можно использовать для хранения сведений о конкретном приложении с ограничением при сохранении на диске.</span><span class="sxs-lookup"><span data-stu-id="1db95-120">The **SCommentRestriction** structure can be used to keep application-specific information with a restriction when it is saved on disk.</span></span> <span data-ttu-id="1db95-121">Например, клиент, который сохраняет имя именованного свойства, используемого в ограничении свойства, может сделать это в структуре **скомментрестриктион** .</span><span class="sxs-lookup"><span data-stu-id="1db95-121">For example, a client saving the name of a named property used in a property restriction can do so in an **SCommentRestriction** structure.</span></span> <span data-ttu-id="1db95-122">Сохранение имени свойства невозможно в ограничении свойства, так как связанная структура [спропертирестриктион](spropertyrestriction.md) содержит только Тег Property.</span><span class="sxs-lookup"><span data-stu-id="1db95-122">Saving a property name is not possible in a property restriction because the associated [SPropertyRestriction](spropertyrestriction.md) structure holds only the property tag.</span></span> 
  
<span data-ttu-id="1db95-123">Для получения дополнительных сведений о структуре и ограничениях **скомментрестриктион** в целом ознакомьтесь с [ограничениями](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="1db95-123">For more information about the **SCommentRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1db95-124">См. также</span><span class="sxs-lookup"><span data-stu-id="1db95-124">See also</span></span>



[<span data-ttu-id="1db95-125">SPropValue</span><span class="sxs-lookup"><span data-stu-id="1db95-125">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="1db95-126">SRestriction</span><span class="sxs-lookup"><span data-stu-id="1db95-126">SRestriction</span></span>](srestriction.md)
  
[<span data-ttu-id="1db95-127">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="1db95-127">SPropertyRestriction</span></span>](spropertyrestriction.md)


[<span data-ttu-id="1db95-128">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="1db95-128">MAPI Structures</span></span>](mapi-structures.md)

