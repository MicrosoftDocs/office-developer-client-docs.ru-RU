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
ms.openlocfilehash: 3cd84e4ddb6d722d9f3de11d65b100d86e69ecae
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571817"
---
# <a name="imapiformmgrresolvemessageclass"></a><span data-ttu-id="edace-103">IMAPIFormMgr::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="edace-103">IMAPIFormMgr::ResolveMessageClass</span></span>

  
  
<span data-ttu-id="edace-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="edace-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="edace-105">Разрешает класс сообщения в его формы в контейнере формы и возвращает объект сведения формы для этой формы.</span><span class="sxs-lookup"><span data-stu-id="edace-105">Resolves a message class to its form within a form container, and returns a form information object for that form.</span></span>
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMsgClass,
  ULONG ulFlags,
  LPMAPIFOLDER pFolderFocus,
  LPMAPIFORMINFO FAR * ppResult
);
```

## <a name="parameters"></a><span data-ttu-id="edace-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="edace-106">Parameters</span></span>

 <span data-ttu-id="edace-107">_szMsgClass_</span><span class="sxs-lookup"><span data-stu-id="edace-107">_szMsgClass_</span></span>
  
> <span data-ttu-id="edace-108">[in] Строка, имена класс сообщения, в которой необходимо разрешить.</span><span class="sxs-lookup"><span data-stu-id="edace-108">[in] A string that names the message class being resolved.</span></span>
    
 <span data-ttu-id="edace-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="edace-109">_ulFlags_</span></span>
  
> <span data-ttu-id="edace-110">[in] Битовая маска флаги, который определяет, как устранена класс сообщения.</span><span class="sxs-lookup"><span data-stu-id="edace-110">[in] A bitmask of flags that controls how the message class is resolved.</span></span> <span data-ttu-id="edace-111">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="edace-111">The following flag can be set:</span></span>
    
<span data-ttu-id="edace-112">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="edace-112">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="edace-113">Следует разрешить только класс строки сообщения, которые являются точное совпадение.</span><span class="sxs-lookup"><span data-stu-id="edace-113">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="edace-114">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="edace-114">_pFolderFocus_</span></span>
  
> <span data-ttu-id="edace-115">[in] Указатель на папку, содержащую сообщение, в которой необходимо разрешить.</span><span class="sxs-lookup"><span data-stu-id="edace-115">[in] A pointer to the folder that contains the message being resolved.</span></span> <span data-ttu-id="edace-116">Параметр _pFolderFocus_ может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="edace-116">The  _pFolderFocus_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="edace-117">_ppResult_</span><span class="sxs-lookup"><span data-stu-id="edace-117">_ppResult_</span></span>
  
> <span data-ttu-id="edace-118">[out] Указатель на указатель на объект сведения возвращенные формы.</span><span class="sxs-lookup"><span data-stu-id="edace-118">[out] A pointer to a pointer to a returned form information object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="edace-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="edace-119">Return value</span></span>

<span data-ttu-id="edace-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="edace-120">S_OK</span></span> 
  
> <span data-ttu-id="edace-121">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="edace-121">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="edace-122">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="edace-122">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="edace-123">Класс сообщения, переданной в параметре _szMsgClass_ не соответствует класс сообщения для формы в библиотеке форм.</span><span class="sxs-lookup"><span data-stu-id="edace-123">The message class passed in the  _szMsgClass_ parameter does not match the message class for any form in the form library.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="edace-124">Замечания</span><span class="sxs-lookup"><span data-stu-id="edace-124">Remarks</span></span>

<span data-ttu-id="edace-125">Средства просмотра форм вызовите метод **IMAPIFormMgr::ResolveMessageClass** для разрешения класс сообщения в его формы в контейнере формы.</span><span class="sxs-lookup"><span data-stu-id="edace-125">Form viewers call the **IMAPIFormMgr::ResolveMessageClass** method to resolve a message class to its form within a form container.</span></span> <span data-ttu-id="edace-126">Объекта формы сведения, возвращаемые в параметре _ppResult_ дальнейшей предоставляет доступ к свойствам формы, имеющей класса данного сообщения.</span><span class="sxs-lookup"><span data-stu-id="edace-126">The form information object returned in the  _ppResult_ parameter provides further access to the properties of the form that has the given message class.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="edace-127">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="edace-127">Notes to callers</span></span>

<span data-ttu-id="edace-128">Чтобы устранить класс сообщения в форму, форма просмотра передает имя класса сообщения разрешения, например, " `IPM.HelpDesk.Software`«.</span><span class="sxs-lookup"><span data-stu-id="edace-128">To resolve a message class to a form, a form viewer passes in the name of the message class to be resolved, such as " `IPM.HelpDesk.Software`".</span></span> <span data-ttu-id="edace-129">Для принудительной разрешение, точное (то есть, чтобы запретить разрешение базового класса класс сообщения, когда точно соответствующие формы сервер недоступен), флаг MAPIFORM_EXACTMATCH может быть передан в параметре _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="edace-129">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class when an exactly matching form server is not available), the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="edace-130">Если параметр _pFolderFocus_ имеет значение NULL, процесс разрешения класс сообщения не выполняет поиск контейнера папки.</span><span class="sxs-lookup"><span data-stu-id="edace-130">If the  _pFolderFocus_ parameter is NULL, the message-class resolution process does not search a folder container.</span></span> 
  
<span data-ttu-id="edace-131">Порядок поиска контейнеры зависит от реализации поставщика библиотеки форм.</span><span class="sxs-lookup"><span data-stu-id="edace-131">The order of the containers searched depends on the implementation of the form library provider.</span></span> <span data-ttu-id="edace-132">Поставщик библиотеки форм по умолчанию выполняется поиск сначала локального контейнер, а затем в контейнере папки передается в папку, контейнер личных форм и, наконец, контейнер организации.</span><span class="sxs-lookup"><span data-stu-id="edace-132">The default form library provider searches first the local container, then the folder container for the passed-in folder, the personal form container and, finally, the organization container.</span></span>
  
<span data-ttu-id="edace-133">Имена классов сообщений всегда являются строками ANSI, никогда не Юникод.</span><span class="sxs-lookup"><span data-stu-id="edace-133">Message class names are always ANSI strings, never Unicode.</span></span>
  
<span data-ttu-id="edace-134">Идентификатор класса для класса разрешить сообщение возвращается в составе объекта данные формы.</span><span class="sxs-lookup"><span data-stu-id="edace-134">The class identifier for the resolved message class is returned as part of the form information object.</span></span> <span data-ttu-id="edace-135">Предполагается, что идентификатор класса существует в библиотеке OLE до того времени, после просмотра формы называется [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) метод или метод [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) просмотра формы не работают.</span><span class="sxs-lookup"><span data-stu-id="edace-135">A form viewer should not work on the assumption that the class identifier exists in the OLE library until after the form viewer has called either the [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) method or the [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="edace-136">См. также</span><span class="sxs-lookup"><span data-stu-id="edace-136">See also</span></span>



[<span data-ttu-id="edace-137">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="edace-137">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)
  
[<span data-ttu-id="edace-138">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="edace-138">IMAPIFormMgr::CreateForm</span></span>](imapiformmgr-createform.md)
  
[<span data-ttu-id="edace-139">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="edace-139">IMAPIFormMgr::PrepareForm</span></span>](imapiformmgr-prepareform.md)
  
[<span data-ttu-id="edace-140">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="edace-140">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

