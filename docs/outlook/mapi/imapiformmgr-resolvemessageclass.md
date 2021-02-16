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
# <a name="imapiformmgrresolvemessageclass"></a><span data-ttu-id="a4909-103">IMAPIFormMgr::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="a4909-103">IMAPIFormMgr::ResolveMessageClass</span></span>

  
  
<span data-ttu-id="a4909-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a4909-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a4909-105">Разрешит класс сообщения в форму в контейнере формы и возвращает объект сведений о форме для этой формы.</span><span class="sxs-lookup"><span data-stu-id="a4909-105">Resolves a message class to its form within a form container, and returns a form information object for that form.</span></span>
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMsgClass,
  ULONG ulFlags,
  LPMAPIFOLDER pFolderFocus,
  LPMAPIFORMINFO FAR * ppResult
);
```

## <a name="parameters"></a><span data-ttu-id="a4909-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a4909-106">Parameters</span></span>

 <span data-ttu-id="a4909-107">_szMsgClass_</span><span class="sxs-lookup"><span data-stu-id="a4909-107">_szMsgClass_</span></span>
  
> <span data-ttu-id="a4909-108">[in] Строка, которая именует класс сообщения, который будет разрешен.</span><span class="sxs-lookup"><span data-stu-id="a4909-108">[in] A string that names the message class being resolved.</span></span>
    
 <span data-ttu-id="a4909-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a4909-109">_ulFlags_</span></span>
  
> <span data-ttu-id="a4909-110">[in] Битоваяmas флагов, которая управляет решением класса сообщения.</span><span class="sxs-lookup"><span data-stu-id="a4909-110">[in] A bitmask of flags that controls how the message class is resolved.</span></span> <span data-ttu-id="a4909-111">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="a4909-111">The following flag can be set:</span></span>
    
<span data-ttu-id="a4909-112">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="a4909-112">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="a4909-113">Должны быть разрешены только строки класса сообщений, точно совпадают.</span><span class="sxs-lookup"><span data-stu-id="a4909-113">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="a4909-114">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="a4909-114">_pFolderFocus_</span></span>
  
> <span data-ttu-id="a4909-115">[in] Указатель на папку, в которую входит разрешенное сообщение.</span><span class="sxs-lookup"><span data-stu-id="a4909-115">[in] A pointer to the folder that contains the message being resolved.</span></span> <span data-ttu-id="a4909-116">Параметр  _pFolderFocus может_ иметь NULL.</span><span class="sxs-lookup"><span data-stu-id="a4909-116">The  _pFolderFocus_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="a4909-117">_ppResult_</span><span class="sxs-lookup"><span data-stu-id="a4909-117">_ppResult_</span></span>
  
> <span data-ttu-id="a4909-118">[out] Указатель на указатель на возвращенный объект сведений о форме.</span><span class="sxs-lookup"><span data-stu-id="a4909-118">[out] A pointer to a pointer to a returned form information object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a4909-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a4909-119">Return value</span></span>

<span data-ttu-id="a4909-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="a4909-120">S_OK</span></span> 
  
> <span data-ttu-id="a4909-121">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="a4909-121">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="a4909-122">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="a4909-122">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="a4909-123">Класс сообщения, переданный в  _параметре szMsgClass,_ не соответствует классу сообщения для любой формы в библиотеке форм.</span><span class="sxs-lookup"><span data-stu-id="a4909-123">The message class passed in the  _szMsgClass_ parameter does not match the message class for any form in the form library.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a4909-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="a4909-124">Remarks</span></span>

<span data-ttu-id="a4909-125">С помощью метода **IMAPIFormMgr::ResolveMessageClass можно вызвать метод IMAPIFormMgr::ResolveMessageClass,** чтобы разрешить класс сообщения в форму в контейнере формы.</span><span class="sxs-lookup"><span data-stu-id="a4909-125">Form viewers call the **IMAPIFormMgr::ResolveMessageClass** method to resolve a message class to its form within a form container.</span></span> <span data-ttu-id="a4909-126">Объект сведений о форме, возвращенный в  _параметре ppResult,_ предоставляет дополнительный доступ к свойствам формы, которая имеет заданный класс сообщения.</span><span class="sxs-lookup"><span data-stu-id="a4909-126">The form information object returned in the  _ppResult_ parameter provides further access to the properties of the form that has the given message class.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a4909-127">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="a4909-127">Notes to callers</span></span>

<span data-ttu-id="a4909-128">Чтобы разрешить класс сообщения в форму, просмотр формы передает имя разрешаемого класса сообщения, например `IPM.HelpDesk.Software` " ".</span><span class="sxs-lookup"><span data-stu-id="a4909-128">To resolve a message class to a form, a form viewer passes in the name of the message class to be resolved, such as " `IPM.HelpDesk.Software`".</span></span> <span data-ttu-id="a4909-129">Чтобы принудительное разрешение было точным (то есть, чтобы предотвратить разрешение базового класса класса сообщений, когда сервер формы, точно совпадающий с другим, недо доступен), флаг MAPIFORM_EXACTMATCH можно передать в _параметре ulFlags._</span><span class="sxs-lookup"><span data-stu-id="a4909-129">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class when an exactly matching form server is not available), the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="a4909-130">Если параметр  _pFolderFocus_ имеет NULL, процесс разрешения класса сообщений не будет искать контейнер папок.</span><span class="sxs-lookup"><span data-stu-id="a4909-130">If the  _pFolderFocus_ parameter is NULL, the message-class resolution process does not search a folder container.</span></span> 
  
<span data-ttu-id="a4909-131">Порядок ищите контейнеров зависит от реализации поставщика библиотеки форм.</span><span class="sxs-lookup"><span data-stu-id="a4909-131">The order of the containers searched depends on the implementation of the form library provider.</span></span> <span data-ttu-id="a4909-132">Поставщик библиотеки форм по умолчанию сначала выполняет поиск локального контейнера, а затем контейнера папки для переданной папки, контейнера личной формы и, наконец, контейнера организации.</span><span class="sxs-lookup"><span data-stu-id="a4909-132">The default form library provider searches first the local container, then the folder container for the passed-in folder, the personal form container and, finally, the organization container.</span></span>
  
<span data-ttu-id="a4909-133">Имена классов сообщений всегда являются строками ANSI, но не Юникодом.</span><span class="sxs-lookup"><span data-stu-id="a4909-133">Message class names are always ANSI strings, never Unicode.</span></span>
  
<span data-ttu-id="a4909-134">Идентификатор класса для разрешенного класса сообщений возвращается как часть информационного объекта формы.</span><span class="sxs-lookup"><span data-stu-id="a4909-134">The class identifier for the resolved message class is returned as part of the form information object.</span></span> <span data-ttu-id="a4909-135">Просмотр формы не должен работать при предположении, что идентификатор класса существует в библиотеке OLE, пока оно не будет вызвано [методом IMAPIFormMgr::P repareForm](imapiformmgr-prepareform.md) или [IMAPIFormMgr::CreateForm.](imapiformmgr-createform.md)</span><span class="sxs-lookup"><span data-stu-id="a4909-135">A form viewer should not work on the assumption that the class identifier exists in the OLE library until after the form viewer has called either the [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) method or the [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a4909-136">См. также</span><span class="sxs-lookup"><span data-stu-id="a4909-136">See also</span></span>



[<span data-ttu-id="a4909-137">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a4909-137">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)
  
[<span data-ttu-id="a4909-138">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="a4909-138">IMAPIFormMgr::CreateForm</span></span>](imapiformmgr-createform.md)
  
[<span data-ttu-id="a4909-139">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="a4909-139">IMAPIFormMgr::PrepareForm</span></span>](imapiformmgr-prepareform.md)
  
[<span data-ttu-id="a4909-140">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a4909-140">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

