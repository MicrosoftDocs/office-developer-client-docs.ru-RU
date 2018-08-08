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
ms.openlocfilehash: c1da292943d6e4d9625c6ce37019c630471e200b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808911"
---
# <a name="imapiformcontainerresolvemultiplemessageclasses"></a><span data-ttu-id="7b207-103">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="7b207-103">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>

  
  
<span data-ttu-id="7b207-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7b207-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7b207-105">Разрешает группу классов сообщений в формах в контейнере формы и возвращает массив формы объекты для этих форм.</span><span class="sxs-lookup"><span data-stu-id="7b207-105">Resolves a group of message classes to their forms in a form container and returns an array of form information objects for those forms.</span></span>
  
```cpp
HRESULT ResolveMultipleMessageClasses(
  LPSMESSAGECLASSARRAY pMsgClassArray,
  ULONG ulFlags,
  LPSMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a><span data-ttu-id="7b207-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7b207-106">Parameters</span></span>

 <span data-ttu-id="7b207-107">_pMsgClassArray_</span><span class="sxs-lookup"><span data-stu-id="7b207-107">_pMsgClassArray_</span></span>
  
> <span data-ttu-id="7b207-108">[in] Указатель на массив, содержащий имена классов сообщений для решения.</span><span class="sxs-lookup"><span data-stu-id="7b207-108">[in] A pointer to an array that contains the names of the message classes to resolve.</span></span> <span data-ttu-id="7b207-109">Имена классов сообщений всегда являются строками ANSI, никогда не Юникод.</span><span class="sxs-lookup"><span data-stu-id="7b207-109">Message class names are always ANSI strings, never Unicode.</span></span>
    
 <span data-ttu-id="7b207-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7b207-110">_ulFlags_</span></span>
  
> <span data-ttu-id="7b207-111">[in] Битовая маска флаги, который определяет, как разрешаются классов сообщений.</span><span class="sxs-lookup"><span data-stu-id="7b207-111">[in] A bitmask of flags that controls how the message classes are resolved.</span></span> <span data-ttu-id="7b207-112">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="7b207-112">The following flag can be set:</span></span>
    
<span data-ttu-id="7b207-113">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="7b207-113">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="7b207-114">Следует разрешить только класс строки сообщения, которые являются точное совпадение.</span><span class="sxs-lookup"><span data-stu-id="7b207-114">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="7b207-115">_ppfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="7b207-115">_ppfrminfoarray_</span></span>
  
> <span data-ttu-id="7b207-116">[out] Указатель на указатель на массив объектов данные формы.</span><span class="sxs-lookup"><span data-stu-id="7b207-116">[out] A pointer to a pointer to an array of form information objects.</span></span> <span data-ttu-id="7b207-117">Если клиентское приложение с помощью параметра _pMsgClassArray_ передает значение NULL, параметр _ppfrminfoarray_ содержит объекты формы для всех форм в контейнере.</span><span class="sxs-lookup"><span data-stu-id="7b207-117">If a client application passes NULL in the  _pMsgClassArray_ parameter, the  _ppfrminfoarray_ parameter contains form information objects for all forms in the container.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7b207-118">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="7b207-118">Return value</span></span>

<span data-ttu-id="7b207-119">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="7b207-119">S_OK</span></span> 
  
> <span data-ttu-id="7b207-120">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="7b207-120">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7b207-121">���������</span><span class="sxs-lookup"><span data-stu-id="7b207-121">Remarks</span></span>

<span data-ttu-id="7b207-122">Клиентские приложения вызовите метод **IMAPIFormContainer::ResolveMultipleMessageClasses** для разрешения группы классов сообщений для форм в контейнере формы.</span><span class="sxs-lookup"><span data-stu-id="7b207-122">Client applications call the **IMAPIFormContainer::ResolveMultipleMessageClasses** method to resolve a group of message classes to forms within a form container.</span></span> <span data-ttu-id="7b207-123">Массив объектов формы сведений, возвращаемых в параметре _ppfrminfoarray_ дальнейшей предоставляет доступ к каждому из свойств форм.</span><span class="sxs-lookup"><span data-stu-id="7b207-123">The array of form information objects returned in the  _ppfrminfoarray_ parameter provides further access to each of the forms' properties.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="7b207-124">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="7b207-124">Notes to callers</span></span>

<span data-ttu-id="7b207-125">Чтобы устранить группу классов сообщений для форм, передайте массив разрешения имен классов сообщений.</span><span class="sxs-lookup"><span data-stu-id="7b207-125">To resolve a group of message classes to forms, pass in an array of message class names to be resolved.</span></span> <span data-ttu-id="7b207-126">Для принудительной разрешение, точное (то есть, чтобы запретить разрешение базового класса класса сообщения), флаг MAPIFORM_EXACTMATCH может быть передан в параметре _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="7b207-126">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class), the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="7b207-127">Если класс сообщения не может быть разрешен в форму, для этого класса сообщений в массиве сведения формы будет возвращено значение NULL.</span><span class="sxs-lookup"><span data-stu-id="7b207-127">If a message class cannot be resolved to a form, NULL is returned for that message class in the form information array.</span></span> <span data-ttu-id="7b207-128">Таким образом даже в том случае, если метод возвращает значение S_OK, не предполагают, что все классы сообщений устранены успешно.</span><span class="sxs-lookup"><span data-stu-id="7b207-128">Therefore, even if the method returns S_OK, do not assume that all message classes have been successfully resolved.</span></span> <span data-ttu-id="7b207-129">Вместо этого проверьте значения в массиве.</span><span class="sxs-lookup"><span data-stu-id="7b207-129">Instead, check the values in the returned array.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="7b207-130">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="7b207-130">MFCMAPI reference</span></span>

<span data-ttu-id="7b207-131">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="7b207-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7b207-132">**����**</span><span class="sxs-lookup"><span data-stu-id="7b207-132">**File**</span></span>|<span data-ttu-id="7b207-133">**�������**</span><span class="sxs-lookup"><span data-stu-id="7b207-133">**Function**</span></span>|<span data-ttu-id="7b207-134">**�����������**</span><span class="sxs-lookup"><span data-stu-id="7b207-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7b207-135">FormContainerDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="7b207-135">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="7b207-136">CFormContainerDlg::OnResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="7b207-136">CFormContainerDlg::OnResolveMultipleMessageClasses</span></span>  <br/> |<span data-ttu-id="7b207-137">Mfcmapi (en) использует метод **IMAPIFormContainer::ResolveMultipleMessageClasses** для обнаружения формы, связанный с набором классов сообщений.</span><span class="sxs-lookup"><span data-stu-id="7b207-137">MFCMAPI uses the **IMAPIFormContainer::ResolveMultipleMessageClasses** method to locate a form that is associated with a set of message classes.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7b207-138">См. также</span><span class="sxs-lookup"><span data-stu-id="7b207-138">See also</span></span>



[<span data-ttu-id="7b207-139">IMAPIFormContainer::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="7b207-139">IMAPIFormContainer::ResolveMessageClass</span></span>](imapiformcontainer-resolvemessageclass.md)
  
[<span data-ttu-id="7b207-140">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7b207-140">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)


[<span data-ttu-id="7b207-141">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="7b207-141">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

