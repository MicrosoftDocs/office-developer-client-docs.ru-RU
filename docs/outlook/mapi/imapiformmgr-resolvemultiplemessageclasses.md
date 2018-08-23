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
ms.openlocfilehash: 968be38e794793405aac15340a92ccd6d680498d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571698"
---
# <a name="imapiformmgrresolvemultiplemessageclasses"></a><span data-ttu-id="e784f-103">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="e784f-103">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>

  
  
<span data-ttu-id="e784f-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e784f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e784f-105">Разрешает группу классов сообщений в формах в контейнере формы и возвращает массив формы объекты для этих форм.</span><span class="sxs-lookup"><span data-stu-id="e784f-105">Resolves a group of message classes to their forms within a form container, and returns an array of form information objects for those forms.</span></span>
  
```cpp
HRESULT ResolveMultipleMessageClasses(
  LPSMESSAGECLASSARRAY pMsgClasses,
  ULONG ulFlags,
  LPMAPIFOLDER pFolderFocus,
  LPSMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a><span data-ttu-id="e784f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e784f-106">Parameters</span></span>

 <span data-ttu-id="e784f-107">_pMsgClasses_</span><span class="sxs-lookup"><span data-stu-id="e784f-107">_pMsgClasses_</span></span>
  
> <span data-ttu-id="e784f-108">[in] Указатель на массив, содержащий имена классов сообщений для решения.</span><span class="sxs-lookup"><span data-stu-id="e784f-108">[in] A pointer to an array that contains the names of the message classes to resolve.</span></span>
    
 <span data-ttu-id="e784f-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e784f-109">_ulFlags_</span></span>
  
> <span data-ttu-id="e784f-110">[in] Битовая маска флаги, который определяет, как разрешаются классов сообщений.</span><span class="sxs-lookup"><span data-stu-id="e784f-110">[in] A bitmask of flags that controls how the message classes are resolved.</span></span> <span data-ttu-id="e784f-111">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="e784f-111">The following flag can be set:</span></span>
    
<span data-ttu-id="e784f-112">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="e784f-112">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="e784f-113">Следует разрешить только класс строки сообщения, которые являются точное совпадение.</span><span class="sxs-lookup"><span data-stu-id="e784f-113">Only message class strings that are an exact match should be resolved.</span></span>
    
<span data-ttu-id="e784f-114">MAPIFORM_LOCALONLY</span><span class="sxs-lookup"><span data-stu-id="e784f-114">MAPIFORM_LOCALONLY</span></span>
  
> <span data-ttu-id="e784f-115">Не включайте кэшированные формы.</span><span class="sxs-lookup"><span data-stu-id="e784f-115">Do not include cached forms.</span></span>
    
 <span data-ttu-id="e784f-116">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="e784f-116">_pFolderFocus_</span></span>
  
> <span data-ttu-id="e784f-117">[in] Указатель на папку, содержащую форму, разрешения которого класс сообщения.</span><span class="sxs-lookup"><span data-stu-id="e784f-117">[in] A pointer to the folder that contains the form whose message class is being resolved.</span></span> <span data-ttu-id="e784f-118">Параметр _pFolderFocus_ может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="e784f-118">The  _pFolderFocus_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="e784f-119">_ppfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="e784f-119">_ppfrminfoarray_</span></span>
  
> <span data-ttu-id="e784f-120">[out] Указатель на указатель на массив объектов данные формы.</span><span class="sxs-lookup"><span data-stu-id="e784f-120">[out] A pointer to a pointer to an array of form information objects.</span></span> <span data-ttu-id="e784f-121">Если средство просмотра формы с помощью параметра _pMsgClasses_ передает значение NULL, параметр _ppfrminfoarray_ содержит объекты формы для всех форм в контейнере.</span><span class="sxs-lookup"><span data-stu-id="e784f-121">If a form viewer passes NULL in the  _pMsgClasses_ parameter, the  _ppfrminfoarray_ parameter contains form information objects for all forms in the container.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e784f-122">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="e784f-122">Return value</span></span>

<span data-ttu-id="e784f-123">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="e784f-123">S_OK</span></span> 
  
> <span data-ttu-id="e784f-124">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="e784f-124">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e784f-125">���������</span><span class="sxs-lookup"><span data-stu-id="e784f-125">Remarks</span></span>

<span data-ttu-id="e784f-126">Средства просмотра форм вызовите метод **IMAPIFormMgr::ResolveMultipleMessageClasses** для разрешения группы классов сообщений для форм в контейнере формы.</span><span class="sxs-lookup"><span data-stu-id="e784f-126">Form viewers call the **IMAPIFormMgr::ResolveMultipleMessageClasses** method to resolve a group of message classes to forms within a form container.</span></span> <span data-ttu-id="e784f-127">Массив объектов формы сведений, возвращаемых _ppfrminfoarray_ дальнейшей предоставляет доступ к каждой из свойства форм.</span><span class="sxs-lookup"><span data-stu-id="e784f-127">The array of form information objects returned in  _ppfrminfoarray_ provides further access to each of the forms' properties.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e784f-128">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="e784f-128">Notes to callers</span></span>

<span data-ttu-id="e784f-129">Для разрешения группы классов сообщений в формах, форма просмотра передает в массиве разрешения имен классов сообщений.</span><span class="sxs-lookup"><span data-stu-id="e784f-129">To resolve a group of message classes to forms, a form viewer passes in an array of message class names to be resolved.</span></span> <span data-ttu-id="e784f-130">Для принудительной разрешение, точное (то есть, чтобы запретить разрешение базового класса класс сообщения, когда точно соответствующие формы сервер не доступен) флаг MAPIFORM_EXACTMATCH может быть передан в параметре _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="e784f-130">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class when an exactly matching form server is not available) the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="e784f-131">Имена классов сообщений всегда являются строками ANSI, никогда не Юникод.</span><span class="sxs-lookup"><span data-stu-id="e784f-131">Message class names are always ANSI strings, never Unicode.</span></span>
  
<span data-ttu-id="e784f-132">Если класс сообщения не может быть разрешен в форму, для этого класса сообщений в массиве сведения формы будет возвращено значение NULL.</span><span class="sxs-lookup"><span data-stu-id="e784f-132">If a message class cannot be resolved to a form, NULL is returned for that message class in the form information array.</span></span> <span data-ttu-id="e784f-133">Таким образом даже в том случае, если метод возвращает значение S_OK, средства просмотра формы не должны работать предполагается, что все классы сообщений устранены успешно.</span><span class="sxs-lookup"><span data-stu-id="e784f-133">Therefore, even if the method returns S_OK, form viewers should not work on the assumption that all message classes have been successfully resolved.</span></span> <span data-ttu-id="e784f-134">Вместо этого средства просмотра формы должен проверить, значения в массиве.</span><span class="sxs-lookup"><span data-stu-id="e784f-134">Instead, form viewers should check the values in the returned array.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e784f-135">См. также</span><span class="sxs-lookup"><span data-stu-id="e784f-135">See also</span></span>



[<span data-ttu-id="e784f-136">IMAPIFormMgr::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="e784f-136">IMAPIFormMgr::ResolveMessageClass</span></span>](imapiformmgr-resolvemessageclass.md)
  
[<span data-ttu-id="e784f-137">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e784f-137">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

