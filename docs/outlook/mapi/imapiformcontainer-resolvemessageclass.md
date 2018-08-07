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
ms.openlocfilehash: 713a177d5ceddf5fd4d97a0e35d87b2250748faf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808906"
---
# <a name="imapiformcontainerresolvemessageclass"></a><span data-ttu-id="91d3f-103">IMAPIFormContainer::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="91d3f-103">IMAPIFormContainer::ResolveMessageClass</span></span>

  
  
<span data-ttu-id="91d3f-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="91d3f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="91d3f-105">Разрешает класс сообщения в его формы в контейнере формы и возвращает объект сведения формы для этой формы.</span><span class="sxs-lookup"><span data-stu-id="91d3f-105">Resolves a message class to its form in a form container and returns a form information object for that form.</span></span>
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMessageClass,
  ULONG ulFlags,
  LPMAPIFORMINFO FAR * ppforminfo
);
```

## <a name="parameters"></a><span data-ttu-id="91d3f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="91d3f-106">Parameters</span></span>

 <span data-ttu-id="91d3f-107">_szMessageClass_</span><span class="sxs-lookup"><span data-stu-id="91d3f-107">_szMessageClass_</span></span>
  
> <span data-ttu-id="91d3f-108">[in] Строка, имена класс сообщения, в которой необходимо разрешить.</span><span class="sxs-lookup"><span data-stu-id="91d3f-108">[in] A string that names the message class being resolved.</span></span> <span data-ttu-id="91d3f-109">Имена классов сообщений всегда являются строками ANSI, никогда не Юникод.</span><span class="sxs-lookup"><span data-stu-id="91d3f-109">Message class names are always ANSI strings, never Unicode.</span></span>
    
 <span data-ttu-id="91d3f-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="91d3f-110">_ulFlags_</span></span>
  
> <span data-ttu-id="91d3f-111">[in] Битовая маска флаги, который определяет, как устранена класс сообщения.</span><span class="sxs-lookup"><span data-stu-id="91d3f-111">[in] A bitmask of flags that controls how the message class is resolved.</span></span> <span data-ttu-id="91d3f-112">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="91d3f-112">The following flag can be set:</span></span>
    
<span data-ttu-id="91d3f-113">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="91d3f-113">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="91d3f-114">Следует разрешить только класс строки сообщения, которые являются точное совпадение.</span><span class="sxs-lookup"><span data-stu-id="91d3f-114">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="91d3f-115">_ppforminfo_</span><span class="sxs-lookup"><span data-stu-id="91d3f-115">_ppforminfo_</span></span>
  
> <span data-ttu-id="91d3f-116">[out] Указатель на указатель на объект сведения возвращенные формы.</span><span class="sxs-lookup"><span data-stu-id="91d3f-116">[out] A pointer to a pointer to the returned form information object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="91d3f-117">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="91d3f-117">Return value</span></span>

<span data-ttu-id="91d3f-118">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="91d3f-118">S_OK</span></span> 
  
> <span data-ttu-id="91d3f-119">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="91d3f-119">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="91d3f-120">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="91d3f-120">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="91d3f-121">Класс сообщения, переданной в параметре _szMessageClass_ не соответствует класс сообщения для формы в контейнере формы.</span><span class="sxs-lookup"><span data-stu-id="91d3f-121">The message class passed in the  _szMessageClass_ parameter does not match the message class for any form in the form container.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="91d3f-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="91d3f-122">Remarks</span></span>

<span data-ttu-id="91d3f-123">Клиентские приложения вызовите метод **IMAPIFormContainer::ResolveMessageClass** разрешении класс сообщения в форму в контейнере формы.</span><span class="sxs-lookup"><span data-stu-id="91d3f-123">Client applications call the **IMAPIFormContainer::ResolveMessageClass** method to resolve a message class to a form within a form container.</span></span> <span data-ttu-id="91d3f-124">Объекта формы сведения, возвращаемые в параметре _ppforminfo_ дальнейшей предоставляет доступ к свойствам формы с классом данного сообщения.</span><span class="sxs-lookup"><span data-stu-id="91d3f-124">The form information object returned in the  _ppforminfo_ parameter provides further access to the properties of the form with the given message class.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="91d3f-125">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="91d3f-125">Notes to callers</span></span>

<span data-ttu-id="91d3f-126">Чтобы устранить класс сообщения в форму, передайте имя класса сообщений (например, `IPM.HelpDesk.Software`).</span><span class="sxs-lookup"><span data-stu-id="91d3f-126">To resolve a message class to a form, pass in the name of the message class to be resolved (for example,  `IPM.HelpDesk.Software`).</span></span> <span data-ttu-id="91d3f-127">Для принудительной разрешение, точное (то есть, чтобы запретить разрешение базового класса класса сообщения), флаг MAPIFORM_EXACTMATCH может быть передан в параметре _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="91d3f-127">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class), the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="91d3f-128">Идентификатор класса для класса разрешить сообщение возвращается в составе объекта данные формы.</span><span class="sxs-lookup"><span data-stu-id="91d3f-128">The class identifier for the resolved message class is returned as part of the form information object.</span></span> <span data-ttu-id="91d3f-129">Не следует считать, что идентификатор класса существует в библиотеке OLE до того времени, после вызова метода либо [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) , либо [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) .</span><span class="sxs-lookup"><span data-stu-id="91d3f-129">Do not assume that the class identifier exists in the OLE library until after you call either the [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) or [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="91d3f-130">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="91d3f-130">MFCMAPI reference</span></span>

<span data-ttu-id="91d3f-131">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="91d3f-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="91d3f-132">**����**</span><span class="sxs-lookup"><span data-stu-id="91d3f-132">**File**</span></span>|<span data-ttu-id="91d3f-133">**�������**</span><span class="sxs-lookup"><span data-stu-id="91d3f-133">**Function**</span></span>|<span data-ttu-id="91d3f-134">**�����������**</span><span class="sxs-lookup"><span data-stu-id="91d3f-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="91d3f-135">FormContainerDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="91d3f-135">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="91d3f-136">CFormContainerDlg::OnResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="91d3f-136">CFormContainerDlg::OnResolveMessageClass</span></span>  <br/> |<span data-ttu-id="91d3f-137">Mfcmapi (en) использует метод **IMAPIFormContainer::ResolveMessageClass** для обнаружения формы, который связан с классом сообщения.</span><span class="sxs-lookup"><span data-stu-id="91d3f-137">MFCMAPI uses the **IMAPIFormContainer::ResolveMessageClass** method to locate a form that is associated with a message class.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="91d3f-138">См. также</span><span class="sxs-lookup"><span data-stu-id="91d3f-138">See also</span></span>



[<span data-ttu-id="91d3f-139">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="91d3f-139">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)
  
[<span data-ttu-id="91d3f-140">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="91d3f-140">IMAPIFormMgr::CreateForm</span></span>](imapiformmgr-createform.md)
  
[<span data-ttu-id="91d3f-141">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="91d3f-141">IMAPIFormMgr::PrepareForm</span></span>](imapiformmgr-prepareform.md)
  
[<span data-ttu-id="91d3f-142">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="91d3f-142">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)

