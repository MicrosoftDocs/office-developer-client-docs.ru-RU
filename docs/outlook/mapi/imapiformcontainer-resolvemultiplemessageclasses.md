---
title: IMAPIFormContainerResolveMultipleMessageClasses
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.ResolveMultipleMessageCla
api_type:
- COM
ms.assetid: f18c2dd1-366f-48b4-b335-ebbc0651f467
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0730da9c3877985853e2cd0a55420e64fbd98e0c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412543"
---
# <a name="imapiformcontainerresolvemultiplemessageclasses"></a><span data-ttu-id="87a6a-103">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="87a6a-103">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>

  
  
<span data-ttu-id="87a6a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="87a6a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="87a6a-105">Разрешит группу классов сообщений в их формы в контейнере формы и возвращает массив информационных объектов формы для этих форм.</span><span class="sxs-lookup"><span data-stu-id="87a6a-105">Resolves a group of message classes to their forms in a form container and returns an array of form information objects for those forms.</span></span>
  
```cpp
HRESULT ResolveMultipleMessageClasses(
  LPSMESSAGECLASSARRAY pMsgClassArray,
  ULONG ulFlags,
  LPSMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a><span data-ttu-id="87a6a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="87a6a-106">Parameters</span></span>

 <span data-ttu-id="87a6a-107">_pMsgClassArray_</span><span class="sxs-lookup"><span data-stu-id="87a6a-107">_pMsgClassArray_</span></span>
  
> <span data-ttu-id="87a6a-108">[in] Указатель на массив, содержащий имена классов сообщений, которые необходимо разрешить.</span><span class="sxs-lookup"><span data-stu-id="87a6a-108">[in] A pointer to an array that contains the names of the message classes to resolve.</span></span> <span data-ttu-id="87a6a-109">Имена классов сообщений всегда являются строками ANSI, а не Юникодом.</span><span class="sxs-lookup"><span data-stu-id="87a6a-109">Message class names are always ANSI strings, never Unicode.</span></span>
    
 <span data-ttu-id="87a6a-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="87a6a-110">_ulFlags_</span></span>
  
> <span data-ttu-id="87a6a-111">[in] Битоваяmas флагов, которая управляет решением классов сообщений.</span><span class="sxs-lookup"><span data-stu-id="87a6a-111">[in] A bitmask of flags that controls how the message classes are resolved.</span></span> <span data-ttu-id="87a6a-112">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="87a6a-112">The following flag can be set:</span></span>
    
<span data-ttu-id="87a6a-113">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="87a6a-113">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="87a6a-114">Должны быть разрешены только строки класса сообщений, точно совпадают.</span><span class="sxs-lookup"><span data-stu-id="87a6a-114">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="87a6a-115">_ppfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="87a6a-115">_ppfrminfoarray_</span></span>
  
> <span data-ttu-id="87a6a-116">[out] Указатель на указатель на массив информационных объектов формы.</span><span class="sxs-lookup"><span data-stu-id="87a6a-116">[out] A pointer to a pointer to an array of form information objects.</span></span> <span data-ttu-id="87a6a-117">Если клиентские приложения проходят NULL в  _параметре pMsgClassArray,_ параметр  _ppfrminfoarray_ содержит объекты сведений формы для всех форм в контейнере.</span><span class="sxs-lookup"><span data-stu-id="87a6a-117">If a client application passes NULL in the  _pMsgClassArray_ parameter, the  _ppfrminfoarray_ parameter contains form information objects for all forms in the container.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="87a6a-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="87a6a-118">Return value</span></span>

<span data-ttu-id="87a6a-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="87a6a-119">S_OK</span></span> 
  
> <span data-ttu-id="87a6a-120">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="87a6a-120">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="87a6a-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="87a6a-121">Remarks</span></span>

<span data-ttu-id="87a6a-122">Клиентские приложения вызывать метод **IMAPIFormContainer::ResolveMultipleMessageClasses,** чтобы разрешить группу классов сообщений в формы в контейнере формы.</span><span class="sxs-lookup"><span data-stu-id="87a6a-122">Client applications call the **IMAPIFormContainer::ResolveMultipleMessageClasses** method to resolve a group of message classes to forms within a form container.</span></span> <span data-ttu-id="87a6a-123">Массив информационных объектов формы, возвращаемого в  _параметре ppfrminfoarray,_ обеспечивает дополнительный доступ к каждому свойству формы.</span><span class="sxs-lookup"><span data-stu-id="87a6a-123">The array of form information objects returned in the  _ppfrminfoarray_ parameter provides further access to each of the forms' properties.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="87a6a-124">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="87a6a-124">Notes to callers</span></span>

<span data-ttu-id="87a6a-125">Чтобы разрешить группу классов сообщений в формы, передав массив имен классов сообщений для разрешения.</span><span class="sxs-lookup"><span data-stu-id="87a6a-125">To resolve a group of message classes to forms, pass in an array of message class names to be resolved.</span></span> <span data-ttu-id="87a6a-126">Чтобы разрешение было точным (то есть, чтобы предотвратить разрешение базового класса класса сообщения), флаг MAPIFORM_EXACTMATCH можно передать в _параметре ulFlags._</span><span class="sxs-lookup"><span data-stu-id="87a6a-126">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class), the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="87a6a-127">Если класс сообщения не может быть разрешен в форму, для этого класса сообщения возвращается NULL в массиве сведений формы.</span><span class="sxs-lookup"><span data-stu-id="87a6a-127">If a message class cannot be resolved to a form, NULL is returned for that message class in the form information array.</span></span> <span data-ttu-id="87a6a-128">Поэтому даже если метод возвращает S_OK, не следует предполагать, что все классы сообщений успешно разрешены.</span><span class="sxs-lookup"><span data-stu-id="87a6a-128">Therefore, even if the method returns S_OK, do not assume that all message classes have been successfully resolved.</span></span> <span data-ttu-id="87a6a-129">Вместо этого проверьте значения в возвращаемом массиве.</span><span class="sxs-lookup"><span data-stu-id="87a6a-129">Instead, check the values in the returned array.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="87a6a-130">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="87a6a-130">MFCMAPI reference</span></span>

<span data-ttu-id="87a6a-131">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="87a6a-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="87a6a-132">**Файл**</span><span class="sxs-lookup"><span data-stu-id="87a6a-132">**File**</span></span>|<span data-ttu-id="87a6a-133">**Функция**</span><span class="sxs-lookup"><span data-stu-id="87a6a-133">**Function**</span></span>|<span data-ttu-id="87a6a-134">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="87a6a-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="87a6a-135">FormContainerDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="87a6a-135">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="87a6a-136">CFormContainerDlg::OnResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="87a6a-136">CFormContainerDlg::OnResolveMultipleMessageClasses</span></span>  <br/> |<span data-ttu-id="87a6a-137">MFCMAPI использует метод **IMAPIFormContainer::ResolveMultipleMessageClasses** для поиска формы, связанной с набором классов сообщений.</span><span class="sxs-lookup"><span data-stu-id="87a6a-137">MFCMAPI uses the **IMAPIFormContainer::ResolveMultipleMessageClasses** method to locate a form that is associated with a set of message classes.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="87a6a-138">См. также</span><span class="sxs-lookup"><span data-stu-id="87a6a-138">See also</span></span>



[<span data-ttu-id="87a6a-139">IMAPIFormContainer::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="87a6a-139">IMAPIFormContainer::ResolveMessageClass</span></span>](imapiformcontainer-resolvemessageclass.md)
  
[<span data-ttu-id="87a6a-140">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="87a6a-140">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)


[<span data-ttu-id="87a6a-141">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="87a6a-141">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

