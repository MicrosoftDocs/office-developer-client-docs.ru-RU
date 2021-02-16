---
title: IMAPIFormMgrLoadForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.LoadForm
api_type:
- COM
ms.assetid: 5ca500c3-c737-45a5-b0fc-473b75c1d68d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7e445646477ad1fc56b41141b541358d9b9f9616
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418787"
---
# <a name="imapiformmgrloadform"></a><span data-ttu-id="8dbbc-103">IMAPIFormMgr::LoadForm</span><span class="sxs-lookup"><span data-stu-id="8dbbc-103">IMAPIFormMgr::LoadForm</span></span>

  
  
<span data-ttu-id="8dbbc-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8dbbc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8dbbc-105">Запускает форму для открытия существующего сообщения.</span><span class="sxs-lookup"><span data-stu-id="8dbbc-105">Starts a form to open an existing message.</span></span>
  
```cpp
HRESULT LoadForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR lpszMessageClass,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags,
  LPMAPIFOLDER pFolderFocus,
  LPMAPIMESSAGESITE pMessageSite,
  LPMESSAGE pmsg,
  LPMAPIVIEWCONTEXT pViewContext,
  REFIID riid,
  LPVOID FAR * ppvObj
);
```

## <a name="parameters"></a><span data-ttu-id="8dbbc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8dbbc-106">Parameters</span></span>

 <span data-ttu-id="8dbbc-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="8dbbc-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="8dbbc-108">[in] Handle to the parent window of the progress indicator that is displayed while the form is opened.</span><span class="sxs-lookup"><span data-stu-id="8dbbc-108">[in] A handle to the parent window of the progress indicator that is displayed while the form is opened.</span></span> <span data-ttu-id="8dbbc-109">Параметр _ulUIParam_ игнорируется, если MAPI_DIALOG флага в параметре _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="8dbbc-109">The  _ulUIParam_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="8dbbc-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8dbbc-110">_ulFlags_</span></span>
  
> <span data-ttu-id="8dbbc-111">[in] Битоваяmas флагов, которая управляет открытием формы.</span><span class="sxs-lookup"><span data-stu-id="8dbbc-111">[in] A bitmask of flags that controls how the form is opened.</span></span> <span data-ttu-id="8dbbc-112">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="8dbbc-112">The following flags can be set:</span></span>
    
<span data-ttu-id="8dbbc-113">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="8dbbc-113">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="8dbbc-114">Отображает пользовательский интерфейс для предоставления состояния или запроса дополнительных сведений.</span><span class="sxs-lookup"><span data-stu-id="8dbbc-114">Displays a user interface to provide status or prompt the user for more information.</span></span> <span data-ttu-id="8dbbc-115">Если этот флаг не установлен, пользовательский интерфейс не отображается.</span><span class="sxs-lookup"><span data-stu-id="8dbbc-115">If this flag is not set, no user interface is displayed.</span></span>
    
<span data-ttu-id="8dbbc-116">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="8dbbc-116">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="8dbbc-117">Должны быть разрешены только строки класса сообщений, точно совпадают.</span><span class="sxs-lookup"><span data-stu-id="8dbbc-117">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="8dbbc-118">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="8dbbc-118">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="8dbbc-119">[in] Указатель на строку, которая именует класс сообщения для загрузки.</span><span class="sxs-lookup"><span data-stu-id="8dbbc-119">[in] A pointer to a string that names the message class of the message to be loaded.</span></span> <span data-ttu-id="8dbbc-120">Если в параметре _lpszMessageClass_ передается NULL, класс сообщения определяется из сообщения, на которое указывает параметр _pmsg._</span><span class="sxs-lookup"><span data-stu-id="8dbbc-120">If NULL is passed in the  _lpszMessageClass_ parameter, the message class is determined from the message pointed to by the  _pmsg_ parameter.</span></span> 
    
 <span data-ttu-id="8dbbc-121">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="8dbbc-121">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="8dbbc-122">[in] Битовая почта клиентских или определяемых поставщиком флагов, скопированная из свойства **PR_MSG_STATUS** ([PidTagMessageStatus)](pidtagmessagestatus-canonical-property.md)сообщения, которое предоставляет сведения о состоянии сообщения.</span><span class="sxs-lookup"><span data-stu-id="8dbbc-122">[in] A bitmask of client-defined or provider-defined flags copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of the message that provides information about the state of the message.</span></span> <span data-ttu-id="8dbbc-123">Параметр  _ulMessageStatus должен_ быть задан, если  _lpszMessageClass_ не имеет NULL; в противном  _случае ulMessageStatus_ игнорируется.</span><span class="sxs-lookup"><span data-stu-id="8dbbc-123">The  _ulMessageStatus_ parameter must be set if  _lpszMessageClass_ is non-NULL; otherwise,  _ulMessageStatus_ is ignored.</span></span> 
    
 <span data-ttu-id="8dbbc-124">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="8dbbc-124">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="8dbbc-125">[in] Указатель на битовуюmask флагов, скопированную из свойства **PR_MESSAGE_FLAGS** ([PidTagMessageFlags)](pidtagmessageflags-canonical-property.md)сообщения, которое указывает текущее состояние сообщения.</span><span class="sxs-lookup"><span data-stu-id="8dbbc-125">[in] A pointer to a bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the message that indicates the current state of the message.</span></span> <span data-ttu-id="8dbbc-126">Параметр  _ulMessageFlags необходимо_ установить, если  _lpszMessageClass_ не имеет NULL; в противном  _случае ulMessageFlags_ игнорируется.</span><span class="sxs-lookup"><span data-stu-id="8dbbc-126">The  _ulMessageFlags_ parameter must be set if  _lpszMessageClass_ is non-NULL; otherwise,  _ulMessageFlags_ is ignored.</span></span> 
    
 <span data-ttu-id="8dbbc-127">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="8dbbc-127">_pFolderFocus_</span></span>
  
> <span data-ttu-id="8dbbc-128">[in] Указатель на папку, которая непосредственно содержит сообщение.</span><span class="sxs-lookup"><span data-stu-id="8dbbc-128">[in] A pointer to the folder that directly contains the message.</span></span> <span data-ttu-id="8dbbc-129">Параметр  _pFolderFocus_ может иметь NULL, если такая папка не существует (например, если сообщение внедрено в другое сообщение).</span><span class="sxs-lookup"><span data-stu-id="8dbbc-129">The  _pFolderFocus_ parameter can be NULL if such a folder does not exist (for example, if the message is embedded in another message).</span></span> 
    
 <span data-ttu-id="8dbbc-130">_pMessageSite_</span><span class="sxs-lookup"><span data-stu-id="8dbbc-130">_pMessageSite_</span></span>
  
> <span data-ttu-id="8dbbc-131">[in] Указатель на сайт сообщения сообщения.</span><span class="sxs-lookup"><span data-stu-id="8dbbc-131">[in] A pointer to the message site of the message.</span></span>
    
 <span data-ttu-id="8dbbc-132">_pmsg_</span><span class="sxs-lookup"><span data-stu-id="8dbbc-132">_pmsg_</span></span>
  
> <span data-ttu-id="8dbbc-133">[in] Указатель на сообщение.</span><span class="sxs-lookup"><span data-stu-id="8dbbc-133">[in] A pointer to the message.</span></span>
    
 <span data-ttu-id="8dbbc-134">_pViewContext_</span><span class="sxs-lookup"><span data-stu-id="8dbbc-134">_pViewContext_</span></span>
  
> <span data-ttu-id="8dbbc-135">[in] Указатель на контекст представления сообщения.</span><span class="sxs-lookup"><span data-stu-id="8dbbc-135">[in] A pointer to the view context for the message.</span></span> <span data-ttu-id="8dbbc-136">Параметр  _pViewContext может_ иметь NULL.</span><span class="sxs-lookup"><span data-stu-id="8dbbc-136">The  _pViewContext_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="8dbbc-137">_riid_</span><span class="sxs-lookup"><span data-stu-id="8dbbc-137">_riid_</span></span>
  
> <span data-ttu-id="8dbbc-138">[in] Идентификатор интерфейса, используемый для возвращаемого объекта формы.</span><span class="sxs-lookup"><span data-stu-id="8dbbc-138">[in] The interface identifier (IID) of the interface to be used for the returned form object.</span></span> <span data-ttu-id="8dbbc-139">Параметр  _riid_ не должен иметь NULL.</span><span class="sxs-lookup"><span data-stu-id="8dbbc-139">The  _riid_ parameter must not be NULL.</span></span> 
    
 <span data-ttu-id="8dbbc-140">_ppvObj_</span><span class="sxs-lookup"><span data-stu-id="8dbbc-140">_ppvObj_</span></span>
  
> <span data-ttu-id="8dbbc-141">[out] Указатель на указатель на возвращенный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="8dbbc-141">[out] A pointer to a pointer to the returned interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8dbbc-142">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8dbbc-142">Return value</span></span>

<span data-ttu-id="8dbbc-143">S_OK</span><span class="sxs-lookup"><span data-stu-id="8dbbc-143">S_OK</span></span> 
  
> <span data-ttu-id="8dbbc-144">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="8dbbc-144">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="8dbbc-145">MAPI_E_NO_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="8dbbc-145">MAPI_E_NO_INTERFACE</span></span> 
  
> <span data-ttu-id="8dbbc-146">Форма не поддерживает запрашиваемую интерфейс.</span><span class="sxs-lookup"><span data-stu-id="8dbbc-146">The form does not support the requested interface.</span></span>
    
<span data-ttu-id="8dbbc-147">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="8dbbc-147">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="8dbbc-148">Класс сообщения, переданный  _в lpszMessageClass,_ не соответствует классу сообщения для любой формы в библиотеке форм.</span><span class="sxs-lookup"><span data-stu-id="8dbbc-148">The message class passed in  _lpszMessageClass_ does not match the message class for any form in the form library.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="8dbbc-149">Примечания</span><span class="sxs-lookup"><span data-stu-id="8dbbc-149">Remarks</span></span>

<span data-ttu-id="8dbbc-150">Посетители форм **звонят методу IMAPIFormMgr::LoadForm,** чтобы открыть форму для существующего сообщения.</span><span class="sxs-lookup"><span data-stu-id="8dbbc-150">Form viewers call the **IMAPIFormMgr::LoadForm** method to open a form for an existing message.</span></span> <span data-ttu-id="8dbbc-151">**LoadForm** открывает объект формы, загружает сообщение в объект формы, при необходимости настраивает соответствующий контекст представления и возвращает нужный интерфейс для объекта формы.</span><span class="sxs-lookup"><span data-stu-id="8dbbc-151">**LoadForm** opens the form object, loads the message into the form object, sets up the appropriate view context, if necessary, and returns the requested interface for the form object.</span></span> 
  
<span data-ttu-id="8dbbc-152">Параметр  _pFolderFocus_ указывает на папку, в которую входит сообщение.</span><span class="sxs-lookup"><span data-stu-id="8dbbc-152">The  _pFolderFocus_ parameter points to the folder that contains the message.</span></span> <span data-ttu-id="8dbbc-153">Если сообщение внедрено в другое сообщение,  _pFolderFocus_ должен иметь NULL.</span><span class="sxs-lookup"><span data-stu-id="8dbbc-153">If the message is embedded in another message,  _pFolderFocus_ should be NULL.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="8dbbc-154">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="8dbbc-154">Notes to implementers</span></span>

<span data-ttu-id="8dbbc-155">Если в  _lpszMessageClass_ передается NULL, реализация получает класс, состояние и флаги сообщения из свойств **PR_MESSAGE_CLASS** [(PidTagMessageClass),](pidtagmessageclass-canonical-property.md) **PR_MSG_STATUS** **и PR_MESSAGE_FLAGS** сообщения.</span><span class="sxs-lookup"><span data-stu-id="8dbbc-155">If NULL is passed in  _lpszMessageClass_, the implementation obtains the message's message class, status, and flags from the message's **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), **PR_MSG_STATUS** and **PR_MESSAGE_FLAGS** properties.</span></span> <span data-ttu-id="8dbbc-156">Если строка класса сообщения предоставляется в  _lpszMessageClass,_ реализация должна использовать значения  _в ulMessageStatus_ и  _ulMessageFlags_.</span><span class="sxs-lookup"><span data-stu-id="8dbbc-156">If a message class string is provided in  _lpszMessageClass_, the implementation must use the values in  _ulMessageStatus_ and  _ulMessageFlags_.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="8dbbc-157">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="8dbbc-157">MFCMAPI reference</span></span>

<span data-ttu-id="8dbbc-158">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="8dbbc-158">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="8dbbc-159">**Файл**</span><span class="sxs-lookup"><span data-stu-id="8dbbc-159">**File**</span></span>|<span data-ttu-id="8dbbc-160">**Функция**</span><span class="sxs-lookup"><span data-stu-id="8dbbc-160">**Function**</span></span>|<span data-ttu-id="8dbbc-161">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="8dbbc-161">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8dbbc-162">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="8dbbc-162">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="8dbbc-163">OpenMessageNonModal</span><span class="sxs-lookup"><span data-stu-id="8dbbc-163">OpenMessageNonModal</span></span>  <br/> |<span data-ttu-id="8dbbc-164">MFCMAPI использует метод **IMAPIFormMgr::LoadForm** для загрузки формы перед ее отображением.</span><span class="sxs-lookup"><span data-stu-id="8dbbc-164">MFCMAPI uses the **IMAPIFormMgr::LoadForm** method to load a form before displaying it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8dbbc-165">См. также</span><span class="sxs-lookup"><span data-stu-id="8dbbc-165">See also</span></span>



[<span data-ttu-id="8dbbc-166">Каноническое свойство PidTagMessageClass</span><span class="sxs-lookup"><span data-stu-id="8dbbc-166">PidTagMessageClass Canonical Property</span></span>](pidtagmessageclass-canonical-property.md)
  
[<span data-ttu-id="8dbbc-167">Каноническое свойство PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="8dbbc-167">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="8dbbc-168">Каноническое свойство PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="8dbbc-168">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="8dbbc-169">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8dbbc-169">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="8dbbc-170">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="8dbbc-170">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

