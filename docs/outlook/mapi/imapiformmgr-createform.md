---
title: имапиформмгркреатеформ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.CreateForm
api_type:
- COM
ms.assetid: 7d4d50f8-3904-4e93-a535-ac7decceb1a3
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c6e18ee9f8ea1d7dc6592d576c5a1163db526639
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419851"
---
# <a name="imapiformmgrcreateform"></a><span data-ttu-id="befab-103">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="befab-103">IMAPIFormMgr::CreateForm</span></span>

  
  
<span data-ttu-id="befab-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="befab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="befab-105">Открывает форму для создания нового сообщения на основе класса сообщений формы.</span><span class="sxs-lookup"><span data-stu-id="befab-105">Opens a form to create a new message based on the form's message class.</span></span>
  
```cpp
HRESULT CreateForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  IMAPIFormInfo pfrminfoToActivate,
  REFIID refiidToAsk,
  LPVOID FAR * ppvObj
);
```

## <a name="parameters"></a><span data-ttu-id="befab-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="befab-106">Parameters</span></span>

 <span data-ttu-id="befab-107">_улуипарам_</span><span class="sxs-lookup"><span data-stu-id="befab-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="befab-108">возврата Дескриптор родительского окна для индикатора хода выполнения, отображаемого при открытии формы.</span><span class="sxs-lookup"><span data-stu-id="befab-108">[in] A handle to the parent window for the progress indicator that is displayed while the form is opened.</span></span> <span data-ttu-id="befab-109">Параметр _улуипарам_ игнорируется, если в параметре _ulFlags_ не задан флаг MAPI_DIALOG.</span><span class="sxs-lookup"><span data-stu-id="befab-109">The  _ulUIParam_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="befab-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="befab-110">_ulFlags_</span></span>
  
> <span data-ttu-id="befab-111">возврата Битовая маска флагов, определяющих способ открытия формы.</span><span class="sxs-lookup"><span data-stu-id="befab-111">[in] A bitmask of flags that controls how the form is opened.</span></span> <span data-ttu-id="befab-112">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="befab-112">The following flag can be set:</span></span>
    
<span data-ttu-id="befab-113">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="befab-113">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="befab-114">Отображает пользовательский интерфейс для предоставления сведений о состоянии или предлагает пользователю ввести дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="befab-114">Displays a user interface to provide status or prompt the user for more information.</span></span> <span data-ttu-id="befab-115">Если этот флаг не установлен, Пользовательский интерфейс не отображается.</span><span class="sxs-lookup"><span data-stu-id="befab-115">If this flag is not set, no user interface is displayed.</span></span>
    
 <span data-ttu-id="befab-116">_пфрминфотоактивате_</span><span class="sxs-lookup"><span data-stu-id="befab-116">_pfrminfoToActivate_</span></span>
  
> <span data-ttu-id="befab-117">возврата Указатель на объект сведений о форме, используемый для открытия формы.</span><span class="sxs-lookup"><span data-stu-id="befab-117">[in] A pointer to the form information object that is used to open the form.</span></span>
    
 <span data-ttu-id="befab-118">_рефиидтоаск_</span><span class="sxs-lookup"><span data-stu-id="befab-118">_refiidToAsk_</span></span>
  
> <span data-ttu-id="befab-119">возврата Указатель на идентификатор интерфейса (IID) для интерфейса, возвращаемого для объекта формы, который был создан.</span><span class="sxs-lookup"><span data-stu-id="befab-119">[in] A pointer to the interface identifier (IID) for the interface to be returned for the form object that was created.</span></span> <span data-ttu-id="befab-120">Параметр _рефиидтоаск_ не должен иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="befab-120">The  _refiidToAsk_ parameter must not be NULL.</span></span> 
    
 <span data-ttu-id="befab-121">_ппвобж_</span><span class="sxs-lookup"><span data-stu-id="befab-121">_ppvObj_</span></span>
  
> <span data-ttu-id="befab-122">вышли Указатель на указатель на возвращенный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="befab-122">[out] A pointer to a pointer to the returned interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="befab-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="befab-123">Return value</span></span>

<span data-ttu-id="befab-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="befab-124">S_OK</span></span> 
  
> <span data-ttu-id="befab-125">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="befab-125">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="befab-126">MAPI_E_NO_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="befab-126">MAPI_E_NO_INTERFACE</span></span> 
  
> <span data-ttu-id="befab-127">Запрошенный интерфейс не поддерживается объектом Form.</span><span class="sxs-lookup"><span data-stu-id="befab-127">The requested interface is not supported by the form object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="befab-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="befab-128">Remarks</span></span>

<span data-ttu-id="befab-129">Средства просмотра форм вызывают метод **имапиформмгр:: креатеформ** , чтобы открыть форму для создания нового сообщения на основе класса сообщений формы.</span><span class="sxs-lookup"><span data-stu-id="befab-129">Form viewers call the **IMAPIFormMgr::CreateForm** method to open a form to create a new message based on the form's message class.</span></span> <span data-ttu-id="befab-130">**Креатеформ** открывает форму, создавая экземпляр сервера форм для этой формы, как описано в данном объекте сведений о форме.</span><span class="sxs-lookup"><span data-stu-id="befab-130">**CreateForm** opens the form by creating an instance of the form server for that form as described in the given form information object.</span></span> <span data-ttu-id="befab-131">При необходимости **креатеформ** вызывает метод [Имапиформмгр::P репареформ](imapiformmgr-prepareform.md) для загрузки кода сервера форм на диск пользователя.</span><span class="sxs-lookup"><span data-stu-id="befab-131">If required, **CreateForm** calls the [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) method to download the form server code to the user's disk.</span></span> 
  
<span data-ttu-id="befab-132">Параметр _пфрминфотоактивате_ должен указать на объект сведений о форме, который был правильно распознан.</span><span class="sxs-lookup"><span data-stu-id="befab-132">The  _pfrminfoToActivate_ parameter must point to a form information object that has been correctly resolved.</span></span> 
  
<span data-ttu-id="befab-133">После открытия формы средство просмотра формы должно настроить сообщение с помощью интерфейса [иперсистмессаже](ipersistmessageiunknown.md) и при необходимости может задать контекст представления для формы.</span><span class="sxs-lookup"><span data-stu-id="befab-133">After the form has been opened, the calling form viewer must set up a message by using the [IPersistMessage](ipersistmessageiunknown.md) interface and can optionally set up a view context for the form.</span></span> <span data-ttu-id="befab-134">Более подробную информацию можно узнать в статье [Запуск сервера форм](launching-a-form-server.md).</span><span class="sxs-lookup"><span data-stu-id="befab-134">For more information, see [Launching a Form Server](launching-a-form-server.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="befab-135">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="befab-135">MFCMAPI reference</span></span>

<span data-ttu-id="befab-136">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="befab-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="befab-137">**Файл**</span><span class="sxs-lookup"><span data-stu-id="befab-137">**File**</span></span>|<span data-ttu-id="befab-138">**Функция**</span><span class="sxs-lookup"><span data-stu-id="befab-138">**Function**</span></span>|<span data-ttu-id="befab-139">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="befab-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="befab-140">Мапиформфунктионс. cpp</span><span class="sxs-lookup"><span data-stu-id="befab-140">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="befab-141">креатеанддисплайневмаилинфолдер</span><span class="sxs-lookup"><span data-stu-id="befab-141">CreateAndDisplayNewMailInFolder</span></span>  <br/> |<span data-ttu-id="befab-142">MFCMAPI использует метод **имапиформмгр:: креатеформ** , чтобы создать форму перед ее отображением.</span><span class="sxs-lookup"><span data-stu-id="befab-142">MFCMAPI uses the **IMAPIFormMgr::CreateForm** method to create a form before displaying it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="befab-143">См. также</span><span class="sxs-lookup"><span data-stu-id="befab-143">See also</span></span>



[<span data-ttu-id="befab-144">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="befab-144">IMAPIFormMgr::PrepareForm</span></span>](imapiformmgr-prepareform.md)
  
[<span data-ttu-id="befab-145">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="befab-145">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
  
[<span data-ttu-id="befab-146">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="befab-146">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="befab-147">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="befab-147">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="befab-148">Запуск сервера форм</span><span class="sxs-lookup"><span data-stu-id="befab-148">Launching a Form Server</span></span>](launching-a-form-server.md)

