---
title: имапиформмгрлоадформ
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
# <a name="imapiformmgrloadform"></a><span data-ttu-id="b2c59-103">IMAPIFormMgr::LoadForm</span><span class="sxs-lookup"><span data-stu-id="b2c59-103">IMAPIFormMgr::LoadForm</span></span>

  
  
<span data-ttu-id="b2c59-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b2c59-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b2c59-105">Запускает форму, чтобы открыть существующее сообщение.</span><span class="sxs-lookup"><span data-stu-id="b2c59-105">Starts a form to open an existing message.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="b2c59-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b2c59-106">Parameters</span></span>

 <span data-ttu-id="b2c59-107">_улуипарам_</span><span class="sxs-lookup"><span data-stu-id="b2c59-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="b2c59-108">возврата Дескриптор родительского окна индикатора хода выполнения, отображаемого при открытии формы.</span><span class="sxs-lookup"><span data-stu-id="b2c59-108">[in] A handle to the parent window of the progress indicator that is displayed while the form is opened.</span></span> <span data-ttu-id="b2c59-109">Параметр _улуипарам_ игнорируется, если в параметре _ulFlags_ не задан флаг MAPI_DIALOG.</span><span class="sxs-lookup"><span data-stu-id="b2c59-109">The  _ulUIParam_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="b2c59-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b2c59-110">_ulFlags_</span></span>
  
> <span data-ttu-id="b2c59-111">возврата Битовая маска флагов, определяющих способ открытия формы.</span><span class="sxs-lookup"><span data-stu-id="b2c59-111">[in] A bitmask of flags that controls how the form is opened.</span></span> <span data-ttu-id="b2c59-112">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="b2c59-112">The following flags can be set:</span></span>
    
<span data-ttu-id="b2c59-113">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="b2c59-113">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="b2c59-114">Отображает пользовательский интерфейс для предоставления сведений о состоянии или предлагает пользователю ввести дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="b2c59-114">Displays a user interface to provide status or prompt the user for more information.</span></span> <span data-ttu-id="b2c59-115">Если этот флаг не установлен, Пользовательский интерфейс не отображается.</span><span class="sxs-lookup"><span data-stu-id="b2c59-115">If this flag is not set, no user interface is displayed.</span></span>
    
<span data-ttu-id="b2c59-116">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="b2c59-116">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="b2c59-117">Необходимо разрешить только строки класса сообщений с точным совпадением.</span><span class="sxs-lookup"><span data-stu-id="b2c59-117">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="b2c59-118">_лпсзмессажекласс_</span><span class="sxs-lookup"><span data-stu-id="b2c59-118">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="b2c59-119">возврата Указатель на строку, которая присваивает имя классу сообщения, которое необходимо загрузить.</span><span class="sxs-lookup"><span data-stu-id="b2c59-119">[in] A pointer to a string that names the message class of the message to be loaded.</span></span> <span data-ttu-id="b2c59-120">Если в параметре _лпсзмессажекласс_ передается значение null, класс Message определяется на основе сообщения, на которое указывает параметр _ПМСГ_ .</span><span class="sxs-lookup"><span data-stu-id="b2c59-120">If NULL is passed in the  _lpszMessageClass_ parameter, the message class is determined from the message pointed to by the  _pmsg_ parameter.</span></span> 
    
 <span data-ttu-id="b2c59-121">_улмессажестатус_</span><span class="sxs-lookup"><span data-stu-id="b2c59-121">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="b2c59-122">возврата Битовая маска заданных клиентом или поставщиками флагов, скопированных из свойства **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) сообщения, которое содержит сведения о состоянии сообщения.</span><span class="sxs-lookup"><span data-stu-id="b2c59-122">[in] A bitmask of client-defined or provider-defined flags copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of the message that provides information about the state of the message.</span></span> <span data-ttu-id="b2c59-123">Если _лпсзмессажекласс_ не имеет значение null, необходимо задать параметр _улмессажестатус_ . в противном случае _улмессажестатус_ игнорируется.</span><span class="sxs-lookup"><span data-stu-id="b2c59-123">The  _ulMessageStatus_ parameter must be set if  _lpszMessageClass_ is non-NULL; otherwise,  _ulMessageStatus_ is ignored.</span></span> 
    
 <span data-ttu-id="b2c59-124">_улмессажефлагс_</span><span class="sxs-lookup"><span data-stu-id="b2c59-124">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="b2c59-125">возврата Указатель на битовую маску флагов, скопированных из свойства **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) сообщения, которое показывает текущее состояние сообщения.</span><span class="sxs-lookup"><span data-stu-id="b2c59-125">[in] A pointer to a bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the message that indicates the current state of the message.</span></span> <span data-ttu-id="b2c59-126">Если _лпсзмессажекласс_ не имеет значение null, необходимо задать параметр _улмессажефлагс_ . в противном случае _улмессажефлагс_ игнорируется.</span><span class="sxs-lookup"><span data-stu-id="b2c59-126">The  _ulMessageFlags_ parameter must be set if  _lpszMessageClass_ is non-NULL; otherwise,  _ulMessageFlags_ is ignored.</span></span> 
    
 <span data-ttu-id="b2c59-127">_пфолдерфокус_</span><span class="sxs-lookup"><span data-stu-id="b2c59-127">_pFolderFocus_</span></span>
  
> <span data-ttu-id="b2c59-128">возврата Указатель на папку, непосредственно содержащую сообщение.</span><span class="sxs-lookup"><span data-stu-id="b2c59-128">[in] A pointer to the folder that directly contains the message.</span></span> <span data-ttu-id="b2c59-129">Параметр _пфолдерфокус_ может иметь значение null, если такая папка не существует (например, если сообщение внедрено в другое сообщение).</span><span class="sxs-lookup"><span data-stu-id="b2c59-129">The  _pFolderFocus_ parameter can be NULL if such a folder does not exist (for example, if the message is embedded in another message).</span></span> 
    
 <span data-ttu-id="b2c59-130">_пмессажесите_</span><span class="sxs-lookup"><span data-stu-id="b2c59-130">_pMessageSite_</span></span>
  
> <span data-ttu-id="b2c59-131">возврата Указатель на сайт сообщения.</span><span class="sxs-lookup"><span data-stu-id="b2c59-131">[in] A pointer to the message site of the message.</span></span>
    
 <span data-ttu-id="b2c59-132">_пмсг_</span><span class="sxs-lookup"><span data-stu-id="b2c59-132">_pmsg_</span></span>
  
> <span data-ttu-id="b2c59-133">возврата Указатель на сообщение.</span><span class="sxs-lookup"><span data-stu-id="b2c59-133">[in] A pointer to the message.</span></span>
    
 <span data-ttu-id="b2c59-134">_пвиевконтекст_</span><span class="sxs-lookup"><span data-stu-id="b2c59-134">_pViewContext_</span></span>
  
> <span data-ttu-id="b2c59-135">возврата Указатель на контекст представления для сообщения.</span><span class="sxs-lookup"><span data-stu-id="b2c59-135">[in] A pointer to the view context for the message.</span></span> <span data-ttu-id="b2c59-136">Параметр _пвиевконтекст_ может иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="b2c59-136">The  _pViewContext_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="b2c59-137">_риид_</span><span class="sxs-lookup"><span data-stu-id="b2c59-137">_riid_</span></span>
  
> <span data-ttu-id="b2c59-138">возврата Идентификатор интерфейса (IID) интерфейса, который будет использоваться для возвращаемого объекта Form.</span><span class="sxs-lookup"><span data-stu-id="b2c59-138">[in] The interface identifier (IID) of the interface to be used for the returned form object.</span></span> <span data-ttu-id="b2c59-139">Параметр _РИИД_ не должен иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="b2c59-139">The  _riid_ parameter must not be NULL.</span></span> 
    
 <span data-ttu-id="b2c59-140">_ппвобж_</span><span class="sxs-lookup"><span data-stu-id="b2c59-140">_ppvObj_</span></span>
  
> <span data-ttu-id="b2c59-141">вышли Указатель на указатель на возвращенный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="b2c59-141">[out] A pointer to a pointer to the returned interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b2c59-142">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b2c59-142">Return value</span></span>

<span data-ttu-id="b2c59-143">S_OK</span><span class="sxs-lookup"><span data-stu-id="b2c59-143">S_OK</span></span> 
  
> <span data-ttu-id="b2c59-144">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="b2c59-144">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="b2c59-145">MAPI_E_NO_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="b2c59-145">MAPI_E_NO_INTERFACE</span></span> 
  
> <span data-ttu-id="b2c59-146">Форма не поддерживает запрошенный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="b2c59-146">The form does not support the requested interface.</span></span>
    
<span data-ttu-id="b2c59-147">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="b2c59-147">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="b2c59-148">Класс сообщения, переданный в _лпсзмессажекласс_ , не соответствует классу сообщения для любой формы в библиотеке форм.</span><span class="sxs-lookup"><span data-stu-id="b2c59-148">The message class passed in  _lpszMessageClass_ does not match the message class for any form in the form library.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b2c59-149">Примечания</span><span class="sxs-lookup"><span data-stu-id="b2c59-149">Remarks</span></span>

<span data-ttu-id="b2c59-150">Для просмотра форм вызывается метод **имапиформмгр:: лоадформ** , чтобы открыть форму для существующего сообщения.</span><span class="sxs-lookup"><span data-stu-id="b2c59-150">Form viewers call the **IMAPIFormMgr::LoadForm** method to open a form for an existing message.</span></span> <span data-ttu-id="b2c59-151">**Лоадформ** открывает объект Form, загружает сообщение в объект формы, настраивает соответствующий контекст представления, при необходимости и возвращает запрошенный интерфейс для объекта Form.</span><span class="sxs-lookup"><span data-stu-id="b2c59-151">**LoadForm** opens the form object, loads the message into the form object, sets up the appropriate view context, if necessary, and returns the requested interface for the form object.</span></span> 
  
<span data-ttu-id="b2c59-152">Параметр _пфолдерфокус_ указывает папку, в которой находится сообщение.</span><span class="sxs-lookup"><span data-stu-id="b2c59-152">The  _pFolderFocus_ parameter points to the folder that contains the message.</span></span> <span data-ttu-id="b2c59-153">Если сообщение внедрено в другое сообщение, _пфолдерфокус_ должно иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="b2c59-153">If the message is embedded in another message,  _pFolderFocus_ should be NULL.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="b2c59-154">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="b2c59-154">Notes to implementers</span></span>

<span data-ttu-id="b2c59-155">Если в _лпсзмессажекласс_передается значение null, то реализация получает класс сообщений, состояние и флаги сообщения из **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), **PR_MSG_STATUS** и **PR_MESSAGE_FLAGS** свойств.</span><span class="sxs-lookup"><span data-stu-id="b2c59-155">If NULL is passed in  _lpszMessageClass_, the implementation obtains the message's message class, status, and flags from the message's **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), **PR_MSG_STATUS** and **PR_MESSAGE_FLAGS** properties.</span></span> <span data-ttu-id="b2c59-156">Если строка класса сообщения предоставлена в _лпсзмессажекласс_, реализация должна использовать значения в _улмессажестатус_ и _улмессажефлагс_.</span><span class="sxs-lookup"><span data-stu-id="b2c59-156">If a message class string is provided in  _lpszMessageClass_, the implementation must use the values in  _ulMessageStatus_ and  _ulMessageFlags_.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b2c59-157">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="b2c59-157">MFCMAPI reference</span></span>

<span data-ttu-id="b2c59-158">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="b2c59-158">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b2c59-159">**Файл**</span><span class="sxs-lookup"><span data-stu-id="b2c59-159">**File**</span></span>|<span data-ttu-id="b2c59-160">**Функция**</span><span class="sxs-lookup"><span data-stu-id="b2c59-160">**Function**</span></span>|<span data-ttu-id="b2c59-161">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="b2c59-161">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b2c59-162">Мапиформфунктионс. cpp</span><span class="sxs-lookup"><span data-stu-id="b2c59-162">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="b2c59-163">опенмессаженонмодал</span><span class="sxs-lookup"><span data-stu-id="b2c59-163">OpenMessageNonModal</span></span>  <br/> |<span data-ttu-id="b2c59-164">MFCMAPI использует метод **имапиформмгр:: лоадформ** для загрузки формы перед ее отображением.</span><span class="sxs-lookup"><span data-stu-id="b2c59-164">MFCMAPI uses the **IMAPIFormMgr::LoadForm** method to load a form before displaying it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b2c59-165">См. также</span><span class="sxs-lookup"><span data-stu-id="b2c59-165">See also</span></span>



[<span data-ttu-id="b2c59-166">Каноническое свойство PidTagMessageClass</span><span class="sxs-lookup"><span data-stu-id="b2c59-166">PidTagMessageClass Canonical Property</span></span>](pidtagmessageclass-canonical-property.md)
  
[<span data-ttu-id="b2c59-167">Каноническое свойство PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="b2c59-167">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="b2c59-168">Каноническое свойство PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="b2c59-168">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="b2c59-169">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b2c59-169">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="b2c59-170">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="b2c59-170">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

