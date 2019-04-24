---
title: Ипропдатахраддобжпропс
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData.HrAddObjProps
api_type:
- COM
ms.assetid: 683cf476-3c02-4b3b-939f-6fff6611f9aa
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: df63f08d3d453575816c4f7ab043f802023e21d0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315535"
---
# <a name="ipropdatahraddobjprops"></a><span data-ttu-id="622d1-103">IPropData::HrAddObjProps</span><span class="sxs-lookup"><span data-stu-id="622d1-103">IPropData::HrAddObjProps</span></span>

  
  
<span data-ttu-id="622d1-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="622d1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="622d1-105">Добавляет одно или несколько свойств типа ПТ_ОБЖЕКТ в объект.</span><span class="sxs-lookup"><span data-stu-id="622d1-105">Adds one or more properties of type PT_OBJECT to the object.</span></span>
  
```cpp
HRESULT HrAddObjProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="622d1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="622d1-106">Parameters</span></span>

 <span data-ttu-id="622d1-107">_Лппроптагаррай_</span><span class="sxs-lookup"><span data-stu-id="622d1-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="622d1-108">возврата Указатель на массив тегов свойств, указывающий свойства, которые требуется добавить.</span><span class="sxs-lookup"><span data-stu-id="622d1-108">[in] A pointer to an array of property tags that indicate the properties to add.</span></span>
    
 <span data-ttu-id="622d1-109">_Лпппроблемс_</span><span class="sxs-lookup"><span data-stu-id="622d1-109">_lppProblems_</span></span>
  
> <span data-ttu-id="622d1-110">[вход, выход] На входе, допустимый указатель на структуру [спроппроблемаррай](spropproblemarray.md) или значение null.</span><span class="sxs-lookup"><span data-stu-id="622d1-110">[in, out] On input, a valid pointer to an [SPropProblemArray](spropproblemarray.md) structure, or NULL.</span></span> <span data-ttu-id="622d1-111">В выходных данных указатель на указатель на структуру, содержащую сведения о свойствах, которые не удалось добавить, или значение NULL.</span><span class="sxs-lookup"><span data-stu-id="622d1-111">On output, a pointer to a pointer to a structure that contains information about properties that could not be added, or NULL.</span></span> <span data-ttu-id="622d1-112">Указатель на структуру массива неполадок свойств возвращается только в том случае, если передается допустимый указатель.</span><span class="sxs-lookup"><span data-stu-id="622d1-112">A pointer to a property problem array structure is returned only if a valid pointer is passed in.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="622d1-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="622d1-113">Return value</span></span>

<span data-ttu-id="622d1-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="622d1-114">S_OK</span></span> 
  
> <span data-ttu-id="622d1-115">Свойства успешно добавлены.</span><span class="sxs-lookup"><span data-stu-id="622d1-115">The properties were successfully added.</span></span>
    
<span data-ttu-id="622d1-116">МАПИ_Е_ИНВАЛИД_ТИПЕ</span><span class="sxs-lookup"><span data-stu-id="622d1-116">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="622d1-117">В массиве, на который указывает параметр _лппроптагаррай_ , был передан тип свойства, отличный от пт_обжект.</span><span class="sxs-lookup"><span data-stu-id="622d1-117">A property type other than PT_OBJECT was passed in the array that the  _lpPropTagArray_ parameter points to.</span></span> 
    
<span data-ttu-id="622d1-118">МАПИ_Е_НО_АКЦЕСС</span><span class="sxs-lookup"><span data-stu-id="622d1-118">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="622d1-119">Для объекта задано разрешение на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="622d1-119">The object has been set not to allow read/write permission.</span></span>
    
<span data-ttu-id="622d1-120">МАПИ_В_ПАРТИАЛ_КОМПЛЕТИОН</span><span class="sxs-lookup"><span data-stu-id="622d1-120">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="622d1-121">Некоторые (но не все) свойства были добавлены.</span><span class="sxs-lookup"><span data-stu-id="622d1-121">Some, but not all, of the properties were added.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="622d1-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="622d1-122">Remarks</span></span>

<span data-ttu-id="622d1-123">Метод **ипропдата:: храддобжпропс** добавляет одно или несколько свойств типа пт_обжект в объект.</span><span class="sxs-lookup"><span data-stu-id="622d1-123">The **IPropData::HrAddObjProps** method adds one or more properties of type PT_OBJECT to the object.</span></span> <span data-ttu-id="622d1-124">**Храддобжпропс** предоставляет альтернативу методу [IMAPIProp:: SetProps](imapiprop-setprops.md) для свойств объекта, так как свойства объекта невозможно создать с помощью метода **SetProps**.</span><span class="sxs-lookup"><span data-stu-id="622d1-124">**HrAddObjProps** provides an alternative to the [IMAPIProp::SetProps](imapiprop-setprops.md) method for object properties, because object properties cannot be created by calling **SetProps**.</span></span> <span data-ttu-id="622d1-125">При добавлении свойства объекта в тег свойства включается в список тегов свойств, возвращаемых методом [IMAPIProp:: жетпроплист](imapiprop-getproplist.md) .</span><span class="sxs-lookup"><span data-stu-id="622d1-125">Adding an object property results in the property tag being included in the list of property tags that the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method returns.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="622d1-126">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="622d1-126">Notes to callers</span></span>

<span data-ttu-id="622d1-127">Если **храддобжпропс** возвращает мапи_в_партиал_комплетион и вы настроили _лпппроблемс_ на допустимый указатель, Проверьте возвращаемую структуру [спроппроблемаррай](spropproblemarray.md) , чтобы узнать, какие свойства не были добавлены.</span><span class="sxs-lookup"><span data-stu-id="622d1-127">If **HrAddObjProps** returns MAPI_W_PARTIAL_COMPLETION and you have set  _lppProblems_ to a valid pointer, check the returned [SPropProblemArray](spropproblemarray.md) structure to find out which properties were not added.</span></span> <span data-ttu-id="622d1-128">Как правило, единственная неполадка связана с нехваткой памяти.</span><span class="sxs-lookup"><span data-stu-id="622d1-128">Typically, the only problem that occurs is lack of memory.</span></span> <span data-ttu-id="622d1-129">Освободите структуру **спроппроблемаррай** , вызвав функцию [мапифрибуффер](mapifreebuffer.md) по завершении работы с ней.</span><span class="sxs-lookup"><span data-stu-id="622d1-129">Free the **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function when you are finished with it.</span></span> 
  
<span data-ttu-id="622d1-130">Для добавления свойства целевой объект должен иметь разрешение на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="622d1-130">To add a property, the target object must have read/write permission.</span></span> <span data-ttu-id="622d1-131">Если **храддобжпропс** возвращает мапи_е_но_акцесс, невозможно добавить свойства объекта, так как он не разрешает изменение.</span><span class="sxs-lookup"><span data-stu-id="622d1-131">If **HrAddObjProps** returns MAPI_E_NO_ACCESS, you cannot add properties to the object because it does not permit modification.</span></span> <span data-ttu-id="622d1-132">Чтобы получить разрешение на чтение и запись для объекта перед вызовом **храддобжпропс**, вызовите [Ипропдата:: хрсетобжакцесс](ipropdata-hrsetobjaccess.md) и присвойте параметру _улакцесс_ значение ипроп_реадврите.</span><span class="sxs-lookup"><span data-stu-id="622d1-132">To obtain read/write permission to an object prior to calling **HrAddObjProps**, call [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) and set the  _ulAccess_ parameter to IPROP_READWRITE.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="622d1-133">См. также</span><span class="sxs-lookup"><span data-stu-id="622d1-133">See also</span></span>



[<span data-ttu-id="622d1-134">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="622d1-134">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="622d1-135">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="622d1-135">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="622d1-136">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="622d1-136">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="622d1-137">IPropData : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="622d1-137">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)

