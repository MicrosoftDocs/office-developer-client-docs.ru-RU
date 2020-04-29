---
title: имапиформмгрресолвемултиплемессажеклассес
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.ResolveMultipleMessageClasses
api_type:
- COM
ms.assetid: d3cc6658-e46d-42dd-b1ac-65c88cfef8ca
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 515061c6c208008c4752e5ff2f23933a4c259c00
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428020"
---
# <a name="imapiformmgrresolvemultiplemessageclasses"></a><span data-ttu-id="90b4a-103">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="90b4a-103">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>

  
  
<span data-ttu-id="90b4a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="90b4a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="90b4a-105">Разрешает группу классов сообщений в свои формы в контейнере формы и возвращает массив объектов данных формы для этих форм.</span><span class="sxs-lookup"><span data-stu-id="90b4a-105">Resolves a group of message classes to their forms within a form container, and returns an array of form information objects for those forms.</span></span>
  
```cpp
HRESULT ResolveMultipleMessageClasses(
  LPSMESSAGECLASSARRAY pMsgClasses,
  ULONG ulFlags,
  LPMAPIFOLDER pFolderFocus,
  LPSMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a><span data-ttu-id="90b4a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="90b4a-106">Parameters</span></span>

 <span data-ttu-id="90b4a-107">_пмсгклассес_</span><span class="sxs-lookup"><span data-stu-id="90b4a-107">_pMsgClasses_</span></span>
  
> <span data-ttu-id="90b4a-108">возврата Указатель на массив, содержащий имена классов сообщений, которые требуется разрешить.</span><span class="sxs-lookup"><span data-stu-id="90b4a-108">[in] A pointer to an array that contains the names of the message classes to resolve.</span></span>
    
 <span data-ttu-id="90b4a-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="90b4a-109">_ulFlags_</span></span>
  
> <span data-ttu-id="90b4a-110">возврата Битовая маска флагов, определяющих способ разрешения классов сообщений.</span><span class="sxs-lookup"><span data-stu-id="90b4a-110">[in] A bitmask of flags that controls how the message classes are resolved.</span></span> <span data-ttu-id="90b4a-111">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="90b4a-111">The following flag can be set:</span></span>
    
<span data-ttu-id="90b4a-112">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="90b4a-112">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="90b4a-113">Необходимо разрешить только строки класса сообщений с точным совпадением.</span><span class="sxs-lookup"><span data-stu-id="90b4a-113">Only message class strings that are an exact match should be resolved.</span></span>
    
<span data-ttu-id="90b4a-114">MAPIFORM_LOCALONLY</span><span class="sxs-lookup"><span data-stu-id="90b4a-114">MAPIFORM_LOCALONLY</span></span>
  
> <span data-ttu-id="90b4a-115">Не включайте кэшированные формы.</span><span class="sxs-lookup"><span data-stu-id="90b4a-115">Do not include cached forms.</span></span>
    
 <span data-ttu-id="90b4a-116">_пфолдерфокус_</span><span class="sxs-lookup"><span data-stu-id="90b4a-116">_pFolderFocus_</span></span>
  
> <span data-ttu-id="90b4a-117">возврата Указатель на папку, содержащую форму, класс сообщений которой разрешается.</span><span class="sxs-lookup"><span data-stu-id="90b4a-117">[in] A pointer to the folder that contains the form whose message class is being resolved.</span></span> <span data-ttu-id="90b4a-118">Параметр _пфолдерфокус_ может иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="90b4a-118">The  _pFolderFocus_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="90b4a-119">_ппфрминфоаррай_</span><span class="sxs-lookup"><span data-stu-id="90b4a-119">_ppfrminfoarray_</span></span>
  
> <span data-ttu-id="90b4a-120">вышли Указатель на указатель на массив объектов сведений о форме.</span><span class="sxs-lookup"><span data-stu-id="90b4a-120">[out] A pointer to a pointer to an array of form information objects.</span></span> <span data-ttu-id="90b4a-121">Если средство просмотра формы передает значение NULL в параметр _пмсгклассес_ , параметр _ппфрминфоаррай_ содержит объекты информации формы для всех форм в контейнере.</span><span class="sxs-lookup"><span data-stu-id="90b4a-121">If a form viewer passes NULL in the  _pMsgClasses_ parameter, the  _ppfrminfoarray_ parameter contains form information objects for all forms in the container.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="90b4a-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="90b4a-122">Return value</span></span>

<span data-ttu-id="90b4a-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="90b4a-123">S_OK</span></span> 
  
> <span data-ttu-id="90b4a-124">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="90b4a-124">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="90b4a-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="90b4a-125">Remarks</span></span>

<span data-ttu-id="90b4a-126">Средства просмотра форм вызывают метод **имапиформмгр:: ресолвемултиплемессажеклассес** для разрешения группы классов сообщений в формы в контейнере формы.</span><span class="sxs-lookup"><span data-stu-id="90b4a-126">Form viewers call the **IMAPIFormMgr::ResolveMultipleMessageClasses** method to resolve a group of message classes to forms within a form container.</span></span> <span data-ttu-id="90b4a-127">Массив объектов данных формы, возвращаемых в _ппфрминфоаррай_ , обеспечивает дополнительный доступ к каждому из свойств формы.</span><span class="sxs-lookup"><span data-stu-id="90b4a-127">The array of form information objects returned in  _ppfrminfoarray_ provides further access to each of the forms' properties.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="90b4a-128">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="90b4a-128">Notes to callers</span></span>

<span data-ttu-id="90b4a-129">Чтобы разрешить группу классов сообщений для форм, средство просмотра формы передает массив имен классов сообщений, которые требуется разрешить.</span><span class="sxs-lookup"><span data-stu-id="90b4a-129">To resolve a group of message classes to forms, a form viewer passes in an array of message class names to be resolved.</span></span> <span data-ttu-id="90b4a-130">Чтобы обеспечить точное разрешение (то есть, чтобы запретить разрешение для базового класса класса Message, если недоступен точный сервер формы), флаг MAPIFORM_EXACTMATCH можно передать в параметре _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="90b4a-130">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class when an exactly matching form server is not available) the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="90b4a-131">Имена классов сообщений всегда являются строками ANSI, а не Юникодом.</span><span class="sxs-lookup"><span data-stu-id="90b4a-131">Message class names are always ANSI strings, never Unicode.</span></span>
  
<span data-ttu-id="90b4a-132">Если класс сообщения невозможно разрешить в форму, возвращается значение NULL для этого класса сообщения в массиве данных формы.</span><span class="sxs-lookup"><span data-stu-id="90b4a-132">If a message class cannot be resolved to a form, NULL is returned for that message class in the form information array.</span></span> <span data-ttu-id="90b4a-133">Таким образом, даже если метод возвращает S_OK, средства просмотра форм не должны работать в предположении, что все классы сообщений успешно разрешены.</span><span class="sxs-lookup"><span data-stu-id="90b4a-133">Therefore, even if the method returns S_OK, form viewers should not work on the assumption that all message classes have been successfully resolved.</span></span> <span data-ttu-id="90b4a-134">Вместо этого средства просмотра форм должны проверять значения в возвращенном массиве.</span><span class="sxs-lookup"><span data-stu-id="90b4a-134">Instead, form viewers should check the values in the returned array.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="90b4a-135">См. также</span><span class="sxs-lookup"><span data-stu-id="90b4a-135">See also</span></span>



[<span data-ttu-id="90b4a-136">IMAPIFormMgr::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="90b4a-136">IMAPIFormMgr::ResolveMessageClass</span></span>](imapiformmgr-resolvemessageclass.md)
  
[<span data-ttu-id="90b4a-137">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="90b4a-137">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

