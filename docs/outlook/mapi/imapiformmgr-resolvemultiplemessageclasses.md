---
title: IMAPIFormMgrResolveMultipleMessageClasses
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
# <a name="imapiformmgrresolvemultiplemessageclasses"></a><span data-ttu-id="167a3-103">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="167a3-103">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>

  
  
<span data-ttu-id="167a3-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="167a3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="167a3-105">Разрешит группу классов сообщений в их формы в контейнере формы и возвращает массив информационных объектов формы для этих форм.</span><span class="sxs-lookup"><span data-stu-id="167a3-105">Resolves a group of message classes to their forms within a form container, and returns an array of form information objects for those forms.</span></span>
  
```cpp
HRESULT ResolveMultipleMessageClasses(
  LPSMESSAGECLASSARRAY pMsgClasses,
  ULONG ulFlags,
  LPMAPIFOLDER pFolderFocus,
  LPSMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a><span data-ttu-id="167a3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="167a3-106">Parameters</span></span>

 <span data-ttu-id="167a3-107">_pMsgClasses_</span><span class="sxs-lookup"><span data-stu-id="167a3-107">_pMsgClasses_</span></span>
  
> <span data-ttu-id="167a3-108">[in] Указатель на массив, содержащий имена классов сообщений, которые необходимо разрешить.</span><span class="sxs-lookup"><span data-stu-id="167a3-108">[in] A pointer to an array that contains the names of the message classes to resolve.</span></span>
    
 <span data-ttu-id="167a3-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="167a3-109">_ulFlags_</span></span>
  
> <span data-ttu-id="167a3-110">[in] Битоваяmas флагов, которая управляет решением классов сообщений.</span><span class="sxs-lookup"><span data-stu-id="167a3-110">[in] A bitmask of flags that controls how the message classes are resolved.</span></span> <span data-ttu-id="167a3-111">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="167a3-111">The following flag can be set:</span></span>
    
<span data-ttu-id="167a3-112">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="167a3-112">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="167a3-113">Должны быть разрешены только строки класса сообщений, точно совпадают.</span><span class="sxs-lookup"><span data-stu-id="167a3-113">Only message class strings that are an exact match should be resolved.</span></span>
    
<span data-ttu-id="167a3-114">MAPIFORM_LOCALONLY</span><span class="sxs-lookup"><span data-stu-id="167a3-114">MAPIFORM_LOCALONLY</span></span>
  
> <span data-ttu-id="167a3-115">Не включаем кэшные формы.</span><span class="sxs-lookup"><span data-stu-id="167a3-115">Do not include cached forms.</span></span>
    
 <span data-ttu-id="167a3-116">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="167a3-116">_pFolderFocus_</span></span>
  
> <span data-ttu-id="167a3-117">[in] Указатель на папку, содержаную форму, класс сообщения которой разрешен.</span><span class="sxs-lookup"><span data-stu-id="167a3-117">[in] A pointer to the folder that contains the form whose message class is being resolved.</span></span> <span data-ttu-id="167a3-118">Параметр  _pFolderFocus может_ иметь NULL.</span><span class="sxs-lookup"><span data-stu-id="167a3-118">The  _pFolderFocus_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="167a3-119">_ppfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="167a3-119">_ppfrminfoarray_</span></span>
  
> <span data-ttu-id="167a3-120">[out] Указатель на указатель на массив информационных объектов формы.</span><span class="sxs-lookup"><span data-stu-id="167a3-120">[out] A pointer to a pointer to an array of form information objects.</span></span> <span data-ttu-id="167a3-121">Если просмотр формы передает NULL в  _параметре pMsgClasses,_ параметр  _ppfrminfoarray_ содержит информационные объекты формы для всех форм в контейнере.</span><span class="sxs-lookup"><span data-stu-id="167a3-121">If a form viewer passes NULL in the  _pMsgClasses_ parameter, the  _ppfrminfoarray_ parameter contains form information objects for all forms in the container.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="167a3-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="167a3-122">Return value</span></span>

<span data-ttu-id="167a3-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="167a3-123">S_OK</span></span> 
  
> <span data-ttu-id="167a3-124">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="167a3-124">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="167a3-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="167a3-125">Remarks</span></span>

<span data-ttu-id="167a3-126">С помощью метода **IMAPIFormMgr::ResolveMultipleMessageClasses можно вызвать метод IMAPIFormMgr::ResolveMultipleMessageClasses,** чтобы разрешить группу классов сообщений в формы в контейнере формы.</span><span class="sxs-lookup"><span data-stu-id="167a3-126">Form viewers call the **IMAPIFormMgr::ResolveMultipleMessageClasses** method to resolve a group of message classes to forms within a form container.</span></span> <span data-ttu-id="167a3-127">Массив информационных объектов формы, возвращаемого  _в ppfrminfoarray,_ обеспечивает дополнительный доступ к каждому свойству формы.</span><span class="sxs-lookup"><span data-stu-id="167a3-127">The array of form information objects returned in  _ppfrminfoarray_ provides further access to each of the forms' properties.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="167a3-128">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="167a3-128">Notes to callers</span></span>

<span data-ttu-id="167a3-129">Чтобы разрешить группу классов сообщений в формы, просмотр форм передает массив имен классов сообщений для разрешения.</span><span class="sxs-lookup"><span data-stu-id="167a3-129">To resolve a group of message classes to forms, a form viewer passes in an array of message class names to be resolved.</span></span> <span data-ttu-id="167a3-130">Чтобы принудительное разрешение было точным (то есть, чтобы предотвратить разрешение базового класса класса сообщений, когда сервер форм, точно совпадающий с другим, недо доступен), флаг MAPIFORM_EXACTMATCH можно передать в _параметре ulFlags._</span><span class="sxs-lookup"><span data-stu-id="167a3-130">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class when an exactly matching form server is not available) the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="167a3-131">Имена классов сообщений всегда являются строками ANSI, а не Юникодом.</span><span class="sxs-lookup"><span data-stu-id="167a3-131">Message class names are always ANSI strings, never Unicode.</span></span>
  
<span data-ttu-id="167a3-132">Если класс сообщения не может быть разрешен в форму, для этого класса сообщения возвращается NULL в массиве сведений формы.</span><span class="sxs-lookup"><span data-stu-id="167a3-132">If a message class cannot be resolved to a form, NULL is returned for that message class in the form information array.</span></span> <span data-ttu-id="167a3-133">Следовательно, даже если метод возвращает S_OK, просмотр форм не должен работать при предположении, что все классы сообщений успешно разрешены.</span><span class="sxs-lookup"><span data-stu-id="167a3-133">Therefore, even if the method returns S_OK, form viewers should not work on the assumption that all message classes have been successfully resolved.</span></span> <span data-ttu-id="167a3-134">Вместо этого, просмотры форм должны проверять значения в возвращаемом массиве.</span><span class="sxs-lookup"><span data-stu-id="167a3-134">Instead, form viewers should check the values in the returned array.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="167a3-135">См. также</span><span class="sxs-lookup"><span data-stu-id="167a3-135">See also</span></span>



[<span data-ttu-id="167a3-136">IMAPIFormMgr::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="167a3-136">IMAPIFormMgr::ResolveMessageClass</span></span>](imapiformmgr-resolvemessageclass.md)
  
[<span data-ttu-id="167a3-137">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="167a3-137">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

