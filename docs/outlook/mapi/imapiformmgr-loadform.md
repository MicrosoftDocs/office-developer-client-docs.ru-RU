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
ms.openlocfilehash: 3e758acfa1cf0c11be666dd730d9bf589d2e9d77
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586216"
---
# <a name="imapiformmgrloadform"></a><span data-ttu-id="47532-103">IMAPIFormMgr::LoadForm</span><span class="sxs-lookup"><span data-stu-id="47532-103">IMAPIFormMgr::LoadForm</span></span>

  
  
<span data-ttu-id="47532-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="47532-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="47532-105">Запускает существующее сообщение при открытии формы.</span><span class="sxs-lookup"><span data-stu-id="47532-105">Starts a form to open an existing message.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="47532-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="47532-106">Parameters</span></span>

 <span data-ttu-id="47532-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="47532-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="47532-108">[in] Дескриптор родительского окна индикатор хода выполнения, отображаемое при открытии формы.</span><span class="sxs-lookup"><span data-stu-id="47532-108">[in] A handle to the parent window of the progress indicator that is displayed while the form is opened.</span></span> <span data-ttu-id="47532-109">Параметр _ulUIParam_ игнорируется, пока флаг MAPI_DIALOG будет выполнен с помощью параметра _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="47532-109">The  _ulUIParam_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="47532-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="47532-110">_ulFlags_</span></span>
  
> <span data-ttu-id="47532-111">[in] Битовая маска флаги, который определяет, как форма будет открыта.</span><span class="sxs-lookup"><span data-stu-id="47532-111">[in] A bitmask of flags that controls how the form is opened.</span></span> <span data-ttu-id="47532-112">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="47532-112">The following flags can be set:</span></span>
    
<span data-ttu-id="47532-113">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="47532-113">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="47532-114">Отображает пользовательский интерфейс для предоставления состояния или запрашивать у пользователя для получения дополнительных сведений.</span><span class="sxs-lookup"><span data-stu-id="47532-114">Displays a user interface to provide status or prompt the user for more information.</span></span> <span data-ttu-id="47532-115">Если этот флаг не установлен, пользовательский интерфейс не отображается.</span><span class="sxs-lookup"><span data-stu-id="47532-115">If this flag is not set, no user interface is displayed.</span></span>
    
<span data-ttu-id="47532-116">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="47532-116">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="47532-117">Следует разрешить только класс строки сообщения, которые являются точное совпадение.</span><span class="sxs-lookup"><span data-stu-id="47532-117">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="47532-118">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="47532-118">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="47532-119">[in] Указатель на строку с именем класса сообщений для сообщений для загрузки.</span><span class="sxs-lookup"><span data-stu-id="47532-119">[in] A pointer to a string that names the message class of the message to be loaded.</span></span> <span data-ttu-id="47532-120">Если значение NULL передается в параметре _lpszMessageClass_ , класс сообщения определяет, какие из сообщения, на который указывает параметр _pmsg_ .</span><span class="sxs-lookup"><span data-stu-id="47532-120">If NULL is passed in the  _lpszMessageClass_ parameter, the message class is determined from the message pointed to by the  _pmsg_ parameter.</span></span> 
    
 <span data-ttu-id="47532-121">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="47532-121">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="47532-122">[in] Битовая маска флагов клиента или поставщика, скопированные из свойства **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) сообщения, предоставляющий информацию о состоянии сообщения.</span><span class="sxs-lookup"><span data-stu-id="47532-122">[in] A bitmask of client-defined or provider-defined flags copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of the message that provides information about the state of the message.</span></span> <span data-ttu-id="47532-123">Необходимо задать параметр _ulMessageStatus_ , если _lpszMessageClass_ отлично от NULL; в противном случае _ulMessageStatus_ игнорируется.</span><span class="sxs-lookup"><span data-stu-id="47532-123">The  _ulMessageStatus_ parameter must be set if  _lpszMessageClass_ is non-NULL; otherwise,  _ulMessageStatus_ is ignored.</span></span> 
    
 <span data-ttu-id="47532-124">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="47532-124">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="47532-125">[in] Указатель на битовой маски флагов, скопированные из свойства **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) сообщения, которое указывает, текущее состояние сообщения.</span><span class="sxs-lookup"><span data-stu-id="47532-125">[in] A pointer to a bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the message that indicates the current state of the message.</span></span> <span data-ttu-id="47532-126">Необходимо задать параметр _ulMessageFlags_ , если _lpszMessageClass_ отлично от NULL; в противном случае _ulMessageFlags_ игнорируется.</span><span class="sxs-lookup"><span data-stu-id="47532-126">The  _ulMessageFlags_ parameter must be set if  _lpszMessageClass_ is non-NULL; otherwise,  _ulMessageFlags_ is ignored.</span></span> 
    
 <span data-ttu-id="47532-127">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="47532-127">_pFolderFocus_</span></span>
  
> <span data-ttu-id="47532-128">[in] Указатель на папку, содержащую сообщение напрямую.</span><span class="sxs-lookup"><span data-stu-id="47532-128">[in] A pointer to the folder that directly contains the message.</span></span> <span data-ttu-id="47532-129">Параметр _pFolderFocus_ может быть NULL, если такая папка не существует (например, если сообщение встроена в другое сообщение).</span><span class="sxs-lookup"><span data-stu-id="47532-129">The  _pFolderFocus_ parameter can be NULL if such a folder does not exist (for example, if the message is embedded in another message).</span></span> 
    
 <span data-ttu-id="47532-130">_pMessageSite_</span><span class="sxs-lookup"><span data-stu-id="47532-130">_pMessageSite_</span></span>
  
> <span data-ttu-id="47532-131">[in] Указатель на сайте сообщение сообщения.</span><span class="sxs-lookup"><span data-stu-id="47532-131">[in] A pointer to the message site of the message.</span></span>
    
 <span data-ttu-id="47532-132">_pmsg_</span><span class="sxs-lookup"><span data-stu-id="47532-132">_pmsg_</span></span>
  
> <span data-ttu-id="47532-133">[in] Указатель на сообщение.</span><span class="sxs-lookup"><span data-stu-id="47532-133">[in] A pointer to the message.</span></span>
    
 <span data-ttu-id="47532-134">_pViewContext_</span><span class="sxs-lookup"><span data-stu-id="47532-134">_pViewContext_</span></span>
  
> <span data-ttu-id="47532-135">[in] Указатель на контекст представления для сообщения.</span><span class="sxs-lookup"><span data-stu-id="47532-135">[in] A pointer to the view context for the message.</span></span> <span data-ttu-id="47532-136">Параметр _pViewContext_ может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="47532-136">The  _pViewContext_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="47532-137">_riid_</span><span class="sxs-lookup"><span data-stu-id="47532-137">_riid_</span></span>
  
> <span data-ttu-id="47532-138">[in] Идентификатор (ИД интерфейса) интерфейса, которое будет использоваться для объекта возвращенные формы.</span><span class="sxs-lookup"><span data-stu-id="47532-138">[in] The interface identifier (IID) of the interface to be used for the returned form object.</span></span> <span data-ttu-id="47532-139">Параметр _riid_ не должна быть NULL.</span><span class="sxs-lookup"><span data-stu-id="47532-139">The  _riid_ parameter must not be NULL.</span></span> 
    
 <span data-ttu-id="47532-140">_ppvObj_</span><span class="sxs-lookup"><span data-stu-id="47532-140">_ppvObj_</span></span>
  
> <span data-ttu-id="47532-141">[out] Указатель на указатель на возвращенный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="47532-141">[out] A pointer to a pointer to the returned interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="47532-142">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="47532-142">Return value</span></span>

<span data-ttu-id="47532-143">S_OK</span><span class="sxs-lookup"><span data-stu-id="47532-143">S_OK</span></span> 
  
> <span data-ttu-id="47532-144">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="47532-144">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="47532-145">MAPI_E_NO_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="47532-145">MAPI_E_NO_INTERFACE</span></span> 
  
> <span data-ttu-id="47532-146">Форма не поддерживает запрошенный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="47532-146">The form does not support the requested interface.</span></span>
    
<span data-ttu-id="47532-147">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="47532-147">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="47532-148">Класс сообщения, переданные в _lpszMessageClass_ не соответствует класс сообщения для формы в библиотеке форм.</span><span class="sxs-lookup"><span data-stu-id="47532-148">The message class passed in  _lpszMessageClass_ does not match the message class for any form in the form library.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="47532-149">Замечания</span><span class="sxs-lookup"><span data-stu-id="47532-149">Remarks</span></span>

<span data-ttu-id="47532-150">Средства просмотра форм вызовите метод **IMAPIFormMgr::LoadForm** для открытия формы для существующего сообщения.</span><span class="sxs-lookup"><span data-stu-id="47532-150">Form viewers call the **IMAPIFormMgr::LoadForm** method to open a form for an existing message.</span></span> <span data-ttu-id="47532-151">**LoadForm** открывает объекта формы, загружает сообщения в объект формы, задает контекст соответствующее представление при необходимости и возвращает запрошенный интерфейс для объекта формы.</span><span class="sxs-lookup"><span data-stu-id="47532-151">**LoadForm** opens the form object, loads the message into the form object, sets up the appropriate view context, if necessary, and returns the requested interface for the form object.</span></span> 
  
<span data-ttu-id="47532-152">Параметр _pFolderFocus_ указывает на папку, содержащую сообщение.</span><span class="sxs-lookup"><span data-stu-id="47532-152">The  _pFolderFocus_ parameter points to the folder that contains the message.</span></span> <span data-ttu-id="47532-153">Если сообщение внедрен в другое сообщение, _pFolderFocus_ должен иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="47532-153">If the message is embedded in another message,  _pFolderFocus_ should be NULL.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="47532-154">Примечания для реализующих</span><span class="sxs-lookup"><span data-stu-id="47532-154">Notes to implementers</span></span>

<span data-ttu-id="47532-155">Если NULL передается в _lpszMessageClass_, реализация получает класс сообщения, состояние и флаги сообщения от **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), **PR_MSG_STATUS** и \*\*PR_MESSAGE_FLAGS сообщения \*\*свойства.</span><span class="sxs-lookup"><span data-stu-id="47532-155">If NULL is passed in  _lpszMessageClass_, the implementation obtains the message's message class, status, and flags from the message's **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), **PR_MSG_STATUS** and **PR_MESSAGE_FLAGS** properties.</span></span> <span data-ttu-id="47532-156">Если этот параметр указан в строке класс сообщения в _lpszMessageClass_реализации необходимо использовать значения в _ulMessageStatus_ и _ulMessageFlags_.</span><span class="sxs-lookup"><span data-stu-id="47532-156">If a message class string is provided in  _lpszMessageClass_, the implementation must use the values in  _ulMessageStatus_ and  _ulMessageFlags_.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="47532-157">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="47532-157">MFCMAPI reference</span></span>

<span data-ttu-id="47532-158">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="47532-158">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="47532-159">**Файл**</span><span class="sxs-lookup"><span data-stu-id="47532-159">**File**</span></span>|<span data-ttu-id="47532-160">**Функция**</span><span class="sxs-lookup"><span data-stu-id="47532-160">**Function**</span></span>|<span data-ttu-id="47532-161">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="47532-161">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="47532-162">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="47532-162">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="47532-163">OpenMessageNonModal</span><span class="sxs-lookup"><span data-stu-id="47532-163">OpenMessageNonModal</span></span>  <br/> |<span data-ttu-id="47532-164">Mfcmapi (en) использует метод **IMAPIFormMgr::LoadForm** для загрузки формы перед их отображением.</span><span class="sxs-lookup"><span data-stu-id="47532-164">MFCMAPI uses the **IMAPIFormMgr::LoadForm** method to load a form before displaying it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="47532-165">См. также</span><span class="sxs-lookup"><span data-stu-id="47532-165">See also</span></span>



[<span data-ttu-id="47532-166">Каноническое свойство PidTagMessageClass</span><span class="sxs-lookup"><span data-stu-id="47532-166">PidTagMessageClass Canonical Property</span></span>](pidtagmessageclass-canonical-property.md)
  
[<span data-ttu-id="47532-167">Каноническое свойство PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="47532-167">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="47532-168">Каноническое свойство PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="47532-168">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="47532-169">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="47532-169">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="47532-170">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="47532-170">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

