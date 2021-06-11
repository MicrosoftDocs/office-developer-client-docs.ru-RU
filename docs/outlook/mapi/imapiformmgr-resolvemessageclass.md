---
title: IMAPIFormMgrResolveMessageClass
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.ResolveMessageClass
api_type:
- COM
ms.assetid: c2af7516-3a97-4422-874d-b1e3a0d4f316
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: e99cff77fe872018722395c53c605e4d8fabfdde
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426396"
---
# <a name="imapiformmgrresolvemessageclass"></a><span data-ttu-id="a40c2-103">IMAPIFormMgr::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="a40c2-103">IMAPIFormMgr::ResolveMessageClass</span></span>

  
  
<span data-ttu-id="a40c2-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a40c2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a40c2-105">Устраняет класс сообщений в его форму в контейнере форм и возвращает информационный объект формы для этой формы.</span><span class="sxs-lookup"><span data-stu-id="a40c2-105">Resolves a message class to its form within a form container, and returns a form information object for that form.</span></span>
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMsgClass,
  ULONG ulFlags,
  LPMAPIFOLDER pFolderFocus,
  LPMAPIFORMINFO FAR * ppResult
);
```

## <a name="parameters"></a><span data-ttu-id="a40c2-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="a40c2-106">Parameters</span></span>

 <span data-ttu-id="a40c2-107">_szMsgClass_</span><span class="sxs-lookup"><span data-stu-id="a40c2-107">_szMsgClass_</span></span>
  
> <span data-ttu-id="a40c2-108">[in] Строка, которая называет разрешенный класс сообщений.</span><span class="sxs-lookup"><span data-stu-id="a40c2-108">[in] A string that names the message class being resolved.</span></span>
    
 <span data-ttu-id="a40c2-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a40c2-109">_ulFlags_</span></span>
  
> <span data-ttu-id="a40c2-110">[in] Немного флагов, которые контролируют решение класса сообщений.</span><span class="sxs-lookup"><span data-stu-id="a40c2-110">[in] A bitmask of flags that controls how the message class is resolved.</span></span> <span data-ttu-id="a40c2-111">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="a40c2-111">The following flag can be set:</span></span>
    
<span data-ttu-id="a40c2-112">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="a40c2-112">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="a40c2-113">Разрешены только строки класса сообщений, которые соответствуют точному типу.</span><span class="sxs-lookup"><span data-stu-id="a40c2-113">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="a40c2-114">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="a40c2-114">_pFolderFocus_</span></span>
  
> <span data-ttu-id="a40c2-115">[in] Указатель на папку с разрешенным сообщением.</span><span class="sxs-lookup"><span data-stu-id="a40c2-115">[in] A pointer to the folder that contains the message being resolved.</span></span> <span data-ttu-id="a40c2-116">Параметр  _pFolderFocus_ может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="a40c2-116">The  _pFolderFocus_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="a40c2-117">_ppResult_</span><span class="sxs-lookup"><span data-stu-id="a40c2-117">_ppResult_</span></span>
  
> <span data-ttu-id="a40c2-118">[вышел] Указатель на указатель на возвращенный информационный объект формы.</span><span class="sxs-lookup"><span data-stu-id="a40c2-118">[out] A pointer to a pointer to a returned form information object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a40c2-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a40c2-119">Return value</span></span>

<span data-ttu-id="a40c2-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="a40c2-120">S_OK</span></span> 
  
> <span data-ttu-id="a40c2-121">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="a40c2-121">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="a40c2-122">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="a40c2-122">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="a40c2-123">Класс сообщений, переданный в  _параметре szMsgClass,_ не соответствует классу сообщений для любой формы в библиотеке форм.</span><span class="sxs-lookup"><span data-stu-id="a40c2-123">The message class passed in the  _szMsgClass_ parameter does not match the message class for any form in the form library.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a40c2-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="a40c2-124">Remarks</span></span>

<span data-ttu-id="a40c2-125">Зрители формы звонят по методу **IMAPIFormMgr::ResolveMessageClass,** чтобы разрешить класс сообщений в его форме в контейнере формы.</span><span class="sxs-lookup"><span data-stu-id="a40c2-125">Form viewers call the **IMAPIFormMgr::ResolveMessageClass** method to resolve a message class to its form within a form container.</span></span> <span data-ttu-id="a40c2-126">Объект информации о форме, возвращенный в  _параметре ppResult,_ предоставляет дополнительный доступ к свойствам формы, которая имеет данный класс сообщений.</span><span class="sxs-lookup"><span data-stu-id="a40c2-126">The form information object returned in the  _ppResult_ parameter provides further access to the properties of the form that has the given message class.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a40c2-127">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="a40c2-127">Notes to callers</span></span>

<span data-ttu-id="a40c2-128">Чтобы разрешить класс сообщений в форму, зритель формы передает имя разрешенного класса сообщений, например `IPM.HelpDesk.Software` "".</span><span class="sxs-lookup"><span data-stu-id="a40c2-128">To resolve a message class to a form, a form viewer passes in the name of the message class to be resolved, such as " `IPM.HelpDesk.Software`".</span></span> <span data-ttu-id="a40c2-129">Чтобы заставить разрешение быть точным (то есть предотвратить разрешение базового класса класса сообщений, когда не доступен точно совпадающий сервер формы), флаг MAPIFORM_EXACTMATCH может быть передан в _параметре ulFlags._</span><span class="sxs-lookup"><span data-stu-id="a40c2-129">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class when an exactly matching form server is not available), the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="a40c2-130">Если  _параметром pFolderFocus_ является NULL, процесс разрешения класса сообщения не будет искать контейнер папки.</span><span class="sxs-lookup"><span data-stu-id="a40c2-130">If the  _pFolderFocus_ parameter is NULL, the message-class resolution process does not search a folder container.</span></span> 
  
<span data-ttu-id="a40c2-131">Порядок поиска контейнеров зависит от реализации поставщика библиотеки форм.</span><span class="sxs-lookup"><span data-stu-id="a40c2-131">The order of the containers searched depends on the implementation of the form library provider.</span></span> <span data-ttu-id="a40c2-132">Поставщик библиотеки форм по умолчанию сначала выполняет поиск локального контейнера, затем контейнера папок для переданной папки, контейнера личной формы и, наконец, контейнера организации.</span><span class="sxs-lookup"><span data-stu-id="a40c2-132">The default form library provider searches first the local container, then the folder container for the passed-in folder, the personal form container and, finally, the organization container.</span></span>
  
<span data-ttu-id="a40c2-133">Имена классов сообщений всегда являются строками ANSI, а не Unicode.</span><span class="sxs-lookup"><span data-stu-id="a40c2-133">Message class names are always ANSI strings, never Unicode.</span></span>
  
<span data-ttu-id="a40c2-134">Идентификатор класса для разрешенного класса сообщений возвращается как часть информационного объекта формы.</span><span class="sxs-lookup"><span data-stu-id="a40c2-134">The class identifier for the resolved message class is returned as part of the form information object.</span></span> <span data-ttu-id="a40c2-135">Просмотр формы не должен работать с предположением о том, что идентификатор класса существует в библиотеке OLE до тех пор, пока зритель формы не вызвал метод [IMAPIFormMgr::P repareForm](imapiformmgr-prepareform.md) или [метод IMAPIFormMgr::CreateForm.](imapiformmgr-createform.md)</span><span class="sxs-lookup"><span data-stu-id="a40c2-135">A form viewer should not work on the assumption that the class identifier exists in the OLE library until after the form viewer has called either the [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) method or the [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a40c2-136">См. также</span><span class="sxs-lookup"><span data-stu-id="a40c2-136">See also</span></span>



[<span data-ttu-id="a40c2-137">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a40c2-137">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)
  
[<span data-ttu-id="a40c2-138">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="a40c2-138">IMAPIFormMgr::CreateForm</span></span>](imapiformmgr-createform.md)
  
[<span data-ttu-id="a40c2-139">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="a40c2-139">IMAPIFormMgr::PrepareForm</span></span>](imapiformmgr-prepareform.md)
  
[<span data-ttu-id="a40c2-140">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a40c2-140">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

