---
title: Имапиформмгрлоадформ
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321699"
---
# <a name="imapiformmgrloadform"></a><span data-ttu-id="b4a7c-103">IMAPIFormMgr::LoadForm</span><span class="sxs-lookup"><span data-stu-id="b4a7c-103">IMAPIFormMgr::LoadForm</span></span>

  
  
<span data-ttu-id="b4a7c-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b4a7c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b4a7c-105">Запускает форму, чтобы открыть существующее сообщение.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-105">Starts a form to open an existing message.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="b4a7c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b4a7c-106">Parameters</span></span>

 <span data-ttu-id="b4a7c-107">_Улуипарам_</span><span class="sxs-lookup"><span data-stu-id="b4a7c-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="b4a7c-108">возврата Дескриптор родительского окна индикатора хода выполнения, отображаемого при открытии формы.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-108">[in] A handle to the parent window of the progress indicator that is displayed while the form is opened.</span></span> <span data-ttu-id="b4a7c-109">Параметр _улуипарам_ игнорируется, если не установлен флаг мапи_диалог в параметре _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="b4a7c-109">The  _ulUIParam_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="b4a7c-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b4a7c-110">_ulFlags_</span></span>
  
> <span data-ttu-id="b4a7c-111">возврата Битовая маска флагов, определяющих способ открытия формы.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-111">[in] A bitmask of flags that controls how the form is opened.</span></span> <span data-ttu-id="b4a7c-112">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="b4a7c-112">The following flags can be set:</span></span>
    
<span data-ttu-id="b4a7c-113">МАПИ_ДИАЛОГ</span><span class="sxs-lookup"><span data-stu-id="b4a7c-113">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="b4a7c-114">Отображает пользовательский интерфейс для предоставления сведений о состоянии или предлагает пользователю ввести дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-114">Displays a user interface to provide status or prompt the user for more information.</span></span> <span data-ttu-id="b4a7c-115">Если этот флаг не установлен, Пользовательский интерфейс не отображается.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-115">If this flag is not set, no user interface is displayed.</span></span>
    
<span data-ttu-id="b4a7c-116">МАПИФОРМ_ЕКСАКТМАТЧ</span><span class="sxs-lookup"><span data-stu-id="b4a7c-116">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="b4a7c-117">Необходимо разрешить только строки класса сообщений с точным совпадением.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-117">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="b4a7c-118">_Лпсзмессажекласс_</span><span class="sxs-lookup"><span data-stu-id="b4a7c-118">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="b4a7c-119">возврата Указатель на строку, которая присваивает имя классу сообщения, которое необходимо загрузить.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-119">[in] A pointer to a string that names the message class of the message to be loaded.</span></span> <span data-ttu-id="b4a7c-120">Если в параметре _лпсзмессажекласс_ переДАЕТСЯ значение null, класс Message определяется на основе сообщения, на которое указывает параметр _ПМСГ_ .</span><span class="sxs-lookup"><span data-stu-id="b4a7c-120">If NULL is passed in the  _lpszMessageClass_ parameter, the message class is determined from the message pointed to by the  _pmsg_ parameter.</span></span> 
    
 <span data-ttu-id="b4a7c-121">_Улмессажестатус_</span><span class="sxs-lookup"><span data-stu-id="b4a7c-121">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="b4a7c-122">возврата Битовая маска заданных клиентом или поставщиками флагов, скопированных из свойства **пр_мсг_статус** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) сообщения, которое содержит сведения о состоянии сообщения.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-122">[in] A bitmask of client-defined or provider-defined flags copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of the message that provides information about the state of the message.</span></span> <span data-ttu-id="b4a7c-123">Если _лпсзмессажекласс_ не имеет значение null, необходимо задать параметр _улмессажестатус_ . в противном случае _улмессажестатус_ игнорируется.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-123">The  _ulMessageStatus_ parameter must be set if  _lpszMessageClass_ is non-NULL; otherwise,  _ulMessageStatus_ is ignored.</span></span> 
    
 <span data-ttu-id="b4a7c-124">_Улмессажефлагс_</span><span class="sxs-lookup"><span data-stu-id="b4a7c-124">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="b4a7c-125">возврата Указатель на битовую маску флагов, скопированных из свойства **пр_мессаже_флагс** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) сообщения, которое показывает текущее состояние сообщения.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-125">[in] A pointer to a bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the message that indicates the current state of the message.</span></span> <span data-ttu-id="b4a7c-126">Если _лпсзмессажекласс_ не имеет значение null, необходимо задать параметр _улмессажефлагс_ . в противном случае _улмессажефлагс_ игнорируется.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-126">The  _ulMessageFlags_ parameter must be set if  _lpszMessageClass_ is non-NULL; otherwise,  _ulMessageFlags_ is ignored.</span></span> 
    
 <span data-ttu-id="b4a7c-127">_Пфолдерфокус_</span><span class="sxs-lookup"><span data-stu-id="b4a7c-127">_pFolderFocus_</span></span>
  
> <span data-ttu-id="b4a7c-128">возврата Указатель на папку, непосредственно содержащую сообщение.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-128">[in] A pointer to the folder that directly contains the message.</span></span> <span data-ttu-id="b4a7c-129">Параметр _пфолдерфокус_ может иметь значение null, если такая папка не существует (например, если сообщение внедрено в другое сообщение).</span><span class="sxs-lookup"><span data-stu-id="b4a7c-129">The  _pFolderFocus_ parameter can be NULL if such a folder does not exist (for example, if the message is embedded in another message).</span></span> 
    
 <span data-ttu-id="b4a7c-130">_Пмессажесите_</span><span class="sxs-lookup"><span data-stu-id="b4a7c-130">_pMessageSite_</span></span>
  
> <span data-ttu-id="b4a7c-131">возврата Указатель на сайт сообщения.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-131">[in] A pointer to the message site of the message.</span></span>
    
 <span data-ttu-id="b4a7c-132">_ПМСГ_</span><span class="sxs-lookup"><span data-stu-id="b4a7c-132">_pmsg_</span></span>
  
> <span data-ttu-id="b4a7c-133">возврата Указатель на сообщение.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-133">[in] A pointer to the message.</span></span>
    
 <span data-ttu-id="b4a7c-134">_Пвиевконтекст_</span><span class="sxs-lookup"><span data-stu-id="b4a7c-134">_pViewContext_</span></span>
  
> <span data-ttu-id="b4a7c-135">возврата Указатель на контекст представления для сообщения.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-135">[in] A pointer to the view context for the message.</span></span> <span data-ttu-id="b4a7c-136">Параметр _пвиевконтекст_ может иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-136">The  _pViewContext_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="b4a7c-137">_РИИД_</span><span class="sxs-lookup"><span data-stu-id="b4a7c-137">_riid_</span></span>
  
> <span data-ttu-id="b4a7c-138">возврата Идентификатор интерфейса (IID) интерфейса, который будет использоваться для возвращаемого объекта Form.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-138">[in] The interface identifier (IID) of the interface to be used for the returned form object.</span></span> <span data-ttu-id="b4a7c-139">Параметр _РИИД_ не должен иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-139">The  _riid_ parameter must not be NULL.</span></span> 
    
 <span data-ttu-id="b4a7c-140">_Ппвобж_</span><span class="sxs-lookup"><span data-stu-id="b4a7c-140">_ppvObj_</span></span>
  
> <span data-ttu-id="b4a7c-141">вышли Указатель на указатель на возвращенный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-141">[out] A pointer to a pointer to the returned interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b4a7c-142">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b4a7c-142">Return value</span></span>

<span data-ttu-id="b4a7c-143">S_OK</span><span class="sxs-lookup"><span data-stu-id="b4a7c-143">S_OK</span></span> 
  
> <span data-ttu-id="b4a7c-144">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-144">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="b4a7c-145">МАПИ_Е_НО_ИНТЕРФАЦЕ</span><span class="sxs-lookup"><span data-stu-id="b4a7c-145">MAPI_E_NO_INTERFACE</span></span> 
  
> <span data-ttu-id="b4a7c-146">Форма не поддерживает запрошенный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-146">The form does not support the requested interface.</span></span>
    
<span data-ttu-id="b4a7c-147">МАПИ_Е_НОТ_ФАУНД</span><span class="sxs-lookup"><span data-stu-id="b4a7c-147">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="b4a7c-148">Класс сообщения, переданный в _лпсзмессажекласс_ , не соответствует классу сообщения для любой формы в библиотеке форм.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-148">The message class passed in  _lpszMessageClass_ does not match the message class for any form in the form library.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b4a7c-149">Замечания</span><span class="sxs-lookup"><span data-stu-id="b4a7c-149">Remarks</span></span>

<span data-ttu-id="b4a7c-150">Для просмотра форм вызывается метод **имапиформмгр:: лоадформ** , чтобы открыть форму для существующего сообщения.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-150">Form viewers call the **IMAPIFormMgr::LoadForm** method to open a form for an existing message.</span></span> <span data-ttu-id="b4a7c-151">**Лоадформ** открывает объект Form, загружает сообщение в объект формы, настраивает соответствующий контекст представления, при необходимости и возвращает запрошенный интерфейс для объекта Form.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-151">**LoadForm** opens the form object, loads the message into the form object, sets up the appropriate view context, if necessary, and returns the requested interface for the form object.</span></span> 
  
<span data-ttu-id="b4a7c-152">Параметр _пфолдерфокус_ указывает папку, в которой находится сообщение.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-152">The  _pFolderFocus_ parameter points to the folder that contains the message.</span></span> <span data-ttu-id="b4a7c-153">Если сообщение внедрено в другое сообщение, _пфолдерфокус_ должно иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-153">If the message is embedded in another message,  _pFolderFocus_ should be NULL.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="b4a7c-154">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="b4a7c-154">Notes to implementers</span></span>

<span data-ttu-id="b4a7c-155">Если в _лпсзмессажекласс_переДАЕТСЯ значение null, то реализация получает класс сообщений, состояние и флаги сообщения **пр_мессаже_класс** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), **пр_мсг_статус** и \*\*пр_мессаже_флагс \*\*свойства.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-155">If NULL is passed in  _lpszMessageClass_, the implementation obtains the message's message class, status, and flags from the message's **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), **PR_MSG_STATUS** and **PR_MESSAGE_FLAGS** properties.</span></span> <span data-ttu-id="b4a7c-156">Если строка класса сообщения предоставлена в _лпсзмессажекласс_, реализация должна использовать значения в _улмессажестатус_ и _улмессажефлагс_.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-156">If a message class string is provided in  _lpszMessageClass_, the implementation must use the values in  _ulMessageStatus_ and  _ulMessageFlags_.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b4a7c-157">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="b4a7c-157">MFCMAPI reference</span></span>

<span data-ttu-id="b4a7c-158">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-158">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b4a7c-159">**Файл**</span><span class="sxs-lookup"><span data-stu-id="b4a7c-159">**File**</span></span>|<span data-ttu-id="b4a7c-160">**Функция**</span><span class="sxs-lookup"><span data-stu-id="b4a7c-160">**Function**</span></span>|<span data-ttu-id="b4a7c-161">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="b4a7c-161">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b4a7c-162">Мапиформфунктионс. cpp</span><span class="sxs-lookup"><span data-stu-id="b4a7c-162">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="b4a7c-163">Опенмессаженонмодал</span><span class="sxs-lookup"><span data-stu-id="b4a7c-163">OpenMessageNonModal</span></span>  <br/> |<span data-ttu-id="b4a7c-164">MFCMAPI использует метод **имапиформмгр:: лоадформ** для загрузки формы перед ее отображением.</span><span class="sxs-lookup"><span data-stu-id="b4a7c-164">MFCMAPI uses the **IMAPIFormMgr::LoadForm** method to load a form before displaying it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b4a7c-165">См. также</span><span class="sxs-lookup"><span data-stu-id="b4a7c-165">See also</span></span>



[<span data-ttu-id="b4a7c-166">Каноническое свойство PidTagMessageClass</span><span class="sxs-lookup"><span data-stu-id="b4a7c-166">PidTagMessageClass Canonical Property</span></span>](pidtagmessageclass-canonical-property.md)
  
[<span data-ttu-id="b4a7c-167">Каноническое свойство PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="b4a7c-167">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="b4a7c-168">Каноническое свойство PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="b4a7c-168">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="b4a7c-169">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b4a7c-169">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="b4a7c-170">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="b4a7c-170">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

