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
ms.openlocfilehash: db4b8d99c960deb3de3d228b2bf9549738501bcc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576283"
---
# <a name="imapiformcontainerresolvemessageclass"></a><span data-ttu-id="851ac-103">IMAPIFormContainer::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="851ac-103">IMAPIFormContainer::ResolveMessageClass</span></span>

  
  
<span data-ttu-id="851ac-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="851ac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="851ac-105">Разрешает класс сообщения в его формы в контейнере формы и возвращает объект сведения формы для этой формы.</span><span class="sxs-lookup"><span data-stu-id="851ac-105">Resolves a message class to its form in a form container and returns a form information object for that form.</span></span>
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMessageClass,
  ULONG ulFlags,
  LPMAPIFORMINFO FAR * ppforminfo
);
```

## <a name="parameters"></a><span data-ttu-id="851ac-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="851ac-106">Parameters</span></span>

 <span data-ttu-id="851ac-107">_szMessageClass_</span><span class="sxs-lookup"><span data-stu-id="851ac-107">_szMessageClass_</span></span>
  
> <span data-ttu-id="851ac-108">[in] Строка, имена класс сообщения, в которой необходимо разрешить.</span><span class="sxs-lookup"><span data-stu-id="851ac-108">[in] A string that names the message class being resolved.</span></span> <span data-ttu-id="851ac-109">Имена классов сообщений всегда являются строками ANSI, никогда не Юникод.</span><span class="sxs-lookup"><span data-stu-id="851ac-109">Message class names are always ANSI strings, never Unicode.</span></span>
    
 <span data-ttu-id="851ac-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="851ac-110">_ulFlags_</span></span>
  
> <span data-ttu-id="851ac-111">[in] Битовая маска флаги, который определяет, как устранена класс сообщения.</span><span class="sxs-lookup"><span data-stu-id="851ac-111">[in] A bitmask of flags that controls how the message class is resolved.</span></span> <span data-ttu-id="851ac-112">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="851ac-112">The following flag can be set:</span></span>
    
<span data-ttu-id="851ac-113">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="851ac-113">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="851ac-114">Следует разрешить только класс строки сообщения, которые являются точное совпадение.</span><span class="sxs-lookup"><span data-stu-id="851ac-114">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="851ac-115">_ppforminfo_</span><span class="sxs-lookup"><span data-stu-id="851ac-115">_ppforminfo_</span></span>
  
> <span data-ttu-id="851ac-116">[out] Указатель на указатель на объект сведения возвращенные формы.</span><span class="sxs-lookup"><span data-stu-id="851ac-116">[out] A pointer to a pointer to the returned form information object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="851ac-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="851ac-117">Return value</span></span>

<span data-ttu-id="851ac-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="851ac-118">S_OK</span></span> 
  
> <span data-ttu-id="851ac-119">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="851ac-119">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="851ac-120">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="851ac-120">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="851ac-121">Класс сообщения, переданной в параметре _szMessageClass_ не соответствует класс сообщения для формы в контейнере формы.</span><span class="sxs-lookup"><span data-stu-id="851ac-121">The message class passed in the  _szMessageClass_ parameter does not match the message class for any form in the form container.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="851ac-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="851ac-122">Remarks</span></span>

<span data-ttu-id="851ac-123">Клиентские приложения вызовите метод **IMAPIFormContainer::ResolveMessageClass** разрешении класс сообщения в форму в контейнере формы.</span><span class="sxs-lookup"><span data-stu-id="851ac-123">Client applications call the **IMAPIFormContainer::ResolveMessageClass** method to resolve a message class to a form within a form container.</span></span> <span data-ttu-id="851ac-124">Объекта формы сведения, возвращаемые в параметре _ppforminfo_ дальнейшей предоставляет доступ к свойствам формы с классом данного сообщения.</span><span class="sxs-lookup"><span data-stu-id="851ac-124">The form information object returned in the  _ppforminfo_ parameter provides further access to the properties of the form with the given message class.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="851ac-125">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="851ac-125">Notes to callers</span></span>

<span data-ttu-id="851ac-126">Чтобы устранить класс сообщения в форму, передайте имя класса сообщений (например, `IPM.HelpDesk.Software`).</span><span class="sxs-lookup"><span data-stu-id="851ac-126">To resolve a message class to a form, pass in the name of the message class to be resolved (for example,  `IPM.HelpDesk.Software`).</span></span> <span data-ttu-id="851ac-127">Для принудительной разрешение, точное (то есть, чтобы запретить разрешение базового класса класса сообщения), флаг MAPIFORM_EXACTMATCH может быть передан в параметре _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="851ac-127">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class), the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="851ac-128">Идентификатор класса для класса разрешить сообщение возвращается в составе объекта данные формы.</span><span class="sxs-lookup"><span data-stu-id="851ac-128">The class identifier for the resolved message class is returned as part of the form information object.</span></span> <span data-ttu-id="851ac-129">Не следует считать, что идентификатор класса существует в библиотеке OLE до того времени, после вызова метода либо [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) , либо [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) .</span><span class="sxs-lookup"><span data-stu-id="851ac-129">Do not assume that the class identifier exists in the OLE library until after you call either the [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) or [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="851ac-130">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="851ac-130">MFCMAPI reference</span></span>

<span data-ttu-id="851ac-131">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="851ac-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="851ac-132">**Файл**</span><span class="sxs-lookup"><span data-stu-id="851ac-132">**File**</span></span>|<span data-ttu-id="851ac-133">**Функция**</span><span class="sxs-lookup"><span data-stu-id="851ac-133">**Function**</span></span>|<span data-ttu-id="851ac-134">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="851ac-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="851ac-135">FormContainerDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="851ac-135">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="851ac-136">CFormContainerDlg::OnResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="851ac-136">CFormContainerDlg::OnResolveMessageClass</span></span>  <br/> |<span data-ttu-id="851ac-137">Mfcmapi (en) использует метод **IMAPIFormContainer::ResolveMessageClass** для обнаружения формы, который связан с классом сообщения.</span><span class="sxs-lookup"><span data-stu-id="851ac-137">MFCMAPI uses the **IMAPIFormContainer::ResolveMessageClass** method to locate a form that is associated with a message class.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="851ac-138">См. также</span><span class="sxs-lookup"><span data-stu-id="851ac-138">See also</span></span>



[<span data-ttu-id="851ac-139">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="851ac-139">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)
  
[<span data-ttu-id="851ac-140">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="851ac-140">IMAPIFormMgr::CreateForm</span></span>](imapiformmgr-createform.md)
  
[<span data-ttu-id="851ac-141">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="851ac-141">IMAPIFormMgr::PrepareForm</span></span>](imapiformmgr-prepareform.md)
  
[<span data-ttu-id="851ac-142">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="851ac-142">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)

