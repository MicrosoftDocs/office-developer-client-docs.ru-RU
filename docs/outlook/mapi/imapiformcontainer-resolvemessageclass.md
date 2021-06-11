---
title: IMAPIFormContainerResolveMessageClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.ResolveMessageClass
api_type:
- COM
ms.assetid: 9ce13f11-5787-4ea5-a84f-b1e3824529ee
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c0954d6f8b14b4088ece2ac276b045b6c163ed98
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408553"
---
# <a name="imapiformcontainerresolvemessageclass"></a><span data-ttu-id="a8cc2-103">IMAPIFormContainer::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="a8cc2-103">IMAPIFormContainer::ResolveMessageClass</span></span>

  
  
<span data-ttu-id="a8cc2-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a8cc2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a8cc2-105">Устраняет класс сообщения в его форму в контейнере формы и возвращает информационный объект формы для этой формы.</span><span class="sxs-lookup"><span data-stu-id="a8cc2-105">Resolves a message class to its form in a form container and returns a form information object for that form.</span></span>
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMessageClass,
  ULONG ulFlags,
  LPMAPIFORMINFO FAR * ppforminfo
);
```

## <a name="parameters"></a><span data-ttu-id="a8cc2-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="a8cc2-106">Parameters</span></span>

 <span data-ttu-id="a8cc2-107">_szMessageClass_</span><span class="sxs-lookup"><span data-stu-id="a8cc2-107">_szMessageClass_</span></span>
  
> <span data-ttu-id="a8cc2-108">[in] Строка, которая называет разрешенный класс сообщений.</span><span class="sxs-lookup"><span data-stu-id="a8cc2-108">[in] A string that names the message class being resolved.</span></span> <span data-ttu-id="a8cc2-109">Имена классов сообщений всегда являются строками ANSI, а не Unicode.</span><span class="sxs-lookup"><span data-stu-id="a8cc2-109">Message class names are always ANSI strings, never Unicode.</span></span>
    
 <span data-ttu-id="a8cc2-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a8cc2-110">_ulFlags_</span></span>
  
> <span data-ttu-id="a8cc2-111">[in] Немного флагов, которые контролируют решение класса сообщений.</span><span class="sxs-lookup"><span data-stu-id="a8cc2-111">[in] A bitmask of flags that controls how the message class is resolved.</span></span> <span data-ttu-id="a8cc2-112">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="a8cc2-112">The following flag can be set:</span></span>
    
<span data-ttu-id="a8cc2-113">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="a8cc2-113">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="a8cc2-114">Разрешены только строки класса сообщений, которые соответствуют точному типу.</span><span class="sxs-lookup"><span data-stu-id="a8cc2-114">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="a8cc2-115">_ppforminfo_</span><span class="sxs-lookup"><span data-stu-id="a8cc2-115">_ppforminfo_</span></span>
  
> <span data-ttu-id="a8cc2-116">[вышел] Указатель на указатель на возвращенный информационный объект формы.</span><span class="sxs-lookup"><span data-stu-id="a8cc2-116">[out] A pointer to a pointer to the returned form information object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a8cc2-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a8cc2-117">Return value</span></span>

<span data-ttu-id="a8cc2-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="a8cc2-118">S_OK</span></span> 
  
> <span data-ttu-id="a8cc2-119">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="a8cc2-119">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="a8cc2-120">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="a8cc2-120">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="a8cc2-121">Класс сообщений, переданный в  _параметре szMessageClass,_ не соответствует классу сообщений для любой формы в контейнере формы.</span><span class="sxs-lookup"><span data-stu-id="a8cc2-121">The message class passed in the  _szMessageClass_ parameter does not match the message class for any form in the form container.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a8cc2-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="a8cc2-122">Remarks</span></span>

<span data-ttu-id="a8cc2-123">Клиентские приложения звонят по методу **IMAPIFormContainer::ResolveMessageClass,** чтобы разрешить класс сообщений в форму в контейнере формы.</span><span class="sxs-lookup"><span data-stu-id="a8cc2-123">Client applications call the **IMAPIFormContainer::ResolveMessageClass** method to resolve a message class to a form within a form container.</span></span> <span data-ttu-id="a8cc2-124">Объект информации формы, возвращаемый в  _параметре ppforminfo,_ предоставляет дополнительный доступ к свойствам формы с данным классом сообщений.</span><span class="sxs-lookup"><span data-stu-id="a8cc2-124">The form information object returned in the  _ppforminfo_ parameter provides further access to the properties of the form with the given message class.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a8cc2-125">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="a8cc2-125">Notes to callers</span></span>

<span data-ttu-id="a8cc2-126">Чтобы разрешить класс сообщения в форму, передай имя разрешенного класса сообщений  `IPM.HelpDesk.Software` (например).</span><span class="sxs-lookup"><span data-stu-id="a8cc2-126">To resolve a message class to a form, pass in the name of the message class to be resolved (for example,  `IPM.HelpDesk.Software`).</span></span> <span data-ttu-id="a8cc2-127">Чтобы заставить разрешение быть точным (то есть для предотвращения разрешения для базового класса класса сообщений), флаг MAPIFORM_EXACTMATCH может быть передан в _параметре ulFlags._</span><span class="sxs-lookup"><span data-stu-id="a8cc2-127">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class), the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="a8cc2-128">Идентификатор класса для разрешенного класса сообщений возвращается как часть информационного объекта формы.</span><span class="sxs-lookup"><span data-stu-id="a8cc2-128">The class identifier for the resolved message class is returned as part of the form information object.</span></span> <span data-ttu-id="a8cc2-129">Не предполагайте, что идентификатор класса существует в библиотеке OLE до тех пор, пока не будет вызываться метод [IMAPIFormMgr::P repareForm](imapiformmgr-prepareform.md) или [IMAPIFormMgr::CreateForm.](imapiformmgr-createform.md)</span><span class="sxs-lookup"><span data-stu-id="a8cc2-129">Do not assume that the class identifier exists in the OLE library until after you call either the [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) or [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a8cc2-130">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="a8cc2-130">MFCMAPI reference</span></span>

<span data-ttu-id="a8cc2-131">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="a8cc2-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a8cc2-132">**Файл**</span><span class="sxs-lookup"><span data-stu-id="a8cc2-132">**File**</span></span>|<span data-ttu-id="a8cc2-133">**Функция**</span><span class="sxs-lookup"><span data-stu-id="a8cc2-133">**Function**</span></span>|<span data-ttu-id="a8cc2-134">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="a8cc2-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a8cc2-135">FormContainerDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="a8cc2-135">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="a8cc2-136">CFormContainerDlg::OnResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="a8cc2-136">CFormContainerDlg::OnResolveMessageClass</span></span>  <br/> |<span data-ttu-id="a8cc2-137">MFCMAPI использует **метод IMAPIFormContainer::ResolveMessageClass,** чтобы найти форму, связанную с классом сообщений.</span><span class="sxs-lookup"><span data-stu-id="a8cc2-137">MFCMAPI uses the **IMAPIFormContainer::ResolveMessageClass** method to locate a form that is associated with a message class.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a8cc2-138">См. также</span><span class="sxs-lookup"><span data-stu-id="a8cc2-138">See also</span></span>



[<span data-ttu-id="a8cc2-139">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a8cc2-139">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)
  
[<span data-ttu-id="a8cc2-140">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="a8cc2-140">IMAPIFormMgr::CreateForm</span></span>](imapiformmgr-createform.md)
  
[<span data-ttu-id="a8cc2-141">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="a8cc2-141">IMAPIFormMgr::PrepareForm</span></span>](imapiformmgr-prepareform.md)
  
[<span data-ttu-id="a8cc2-142">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a8cc2-142">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)

