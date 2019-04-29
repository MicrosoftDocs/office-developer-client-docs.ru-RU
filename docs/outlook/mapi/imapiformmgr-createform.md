---
title: Имапиформмгркреатеформ
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
# <a name="imapiformmgrcreateform"></a><span data-ttu-id="a7703-103">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="a7703-103">IMAPIFormMgr::CreateForm</span></span>

  
  
<span data-ttu-id="a7703-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a7703-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a7703-105">Открывает форму для создания нового сообщения на основе класса сообщений формы.</span><span class="sxs-lookup"><span data-stu-id="a7703-105">Opens a form to create a new message based on the form's message class.</span></span>
  
```cpp
HRESULT CreateForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  IMAPIFormInfo pfrminfoToActivate,
  REFIID refiidToAsk,
  LPVOID FAR * ppvObj
);
```

## <a name="parameters"></a><span data-ttu-id="a7703-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a7703-106">Parameters</span></span>

 <span data-ttu-id="a7703-107">_Улуипарам_</span><span class="sxs-lookup"><span data-stu-id="a7703-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="a7703-108">возврата Дескриптор родительского окна для индикатора хода выполнения, отображаемого при открытии формы.</span><span class="sxs-lookup"><span data-stu-id="a7703-108">[in] A handle to the parent window for the progress indicator that is displayed while the form is opened.</span></span> <span data-ttu-id="a7703-109">Параметр _улуипарам_ игнорируется, если не установлен флаг мапи_диалог в параметре _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="a7703-109">The  _ulUIParam_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="a7703-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a7703-110">_ulFlags_</span></span>
  
> <span data-ttu-id="a7703-111">возврата Битовая маска флагов, определяющих способ открытия формы.</span><span class="sxs-lookup"><span data-stu-id="a7703-111">[in] A bitmask of flags that controls how the form is opened.</span></span> <span data-ttu-id="a7703-112">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="a7703-112">The following flag can be set:</span></span>
    
<span data-ttu-id="a7703-113">МАПИ_ДИАЛОГ</span><span class="sxs-lookup"><span data-stu-id="a7703-113">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="a7703-114">Отображает пользовательский интерфейс для предоставления сведений о состоянии или предлагает пользователю ввести дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="a7703-114">Displays a user interface to provide status or prompt the user for more information.</span></span> <span data-ttu-id="a7703-115">Если этот флаг не установлен, Пользовательский интерфейс не отображается.</span><span class="sxs-lookup"><span data-stu-id="a7703-115">If this flag is not set, no user interface is displayed.</span></span>
    
 <span data-ttu-id="a7703-116">_Пфрминфотоактивате_</span><span class="sxs-lookup"><span data-stu-id="a7703-116">_pfrminfoToActivate_</span></span>
  
> <span data-ttu-id="a7703-117">возврата Указатель на объект сведений о форме, используемый для открытия формы.</span><span class="sxs-lookup"><span data-stu-id="a7703-117">[in] A pointer to the form information object that is used to open the form.</span></span>
    
 <span data-ttu-id="a7703-118">_Рефиидтоаск_</span><span class="sxs-lookup"><span data-stu-id="a7703-118">_refiidToAsk_</span></span>
  
> <span data-ttu-id="a7703-119">возврата Указатель на идентификатор интерфейса (IID) для интерфейса, возвращаемого для объекта формы, который был создан.</span><span class="sxs-lookup"><span data-stu-id="a7703-119">[in] A pointer to the interface identifier (IID) for the interface to be returned for the form object that was created.</span></span> <span data-ttu-id="a7703-120">Параметр _рефиидтоаск_ не должен иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="a7703-120">The  _refiidToAsk_ parameter must not be NULL.</span></span> 
    
 <span data-ttu-id="a7703-121">_Ппвобж_</span><span class="sxs-lookup"><span data-stu-id="a7703-121">_ppvObj_</span></span>
  
> <span data-ttu-id="a7703-122">вышли Указатель на указатель на возвращенный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="a7703-122">[out] A pointer to a pointer to the returned interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a7703-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a7703-123">Return value</span></span>

<span data-ttu-id="a7703-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="a7703-124">S_OK</span></span> 
  
> <span data-ttu-id="a7703-125">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="a7703-125">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="a7703-126">МАПИ_Е_НО_ИНТЕРФАЦЕ</span><span class="sxs-lookup"><span data-stu-id="a7703-126">MAPI_E_NO_INTERFACE</span></span> 
  
> <span data-ttu-id="a7703-127">Запрошенный интерфейс не поддерживается объектом Form.</span><span class="sxs-lookup"><span data-stu-id="a7703-127">The requested interface is not supported by the form object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a7703-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="a7703-128">Remarks</span></span>

<span data-ttu-id="a7703-129">Средства просмотра форм вызывают метод **имапиформмгр:: креатеформ** , чтобы открыть форму для создания нового сообщения на основе класса сообщений формы.</span><span class="sxs-lookup"><span data-stu-id="a7703-129">Form viewers call the **IMAPIFormMgr::CreateForm** method to open a form to create a new message based on the form's message class.</span></span> <span data-ttu-id="a7703-130">**Креатеформ** открывает форму, создавая экземпляр сервера форм для этой формы, как описано в данном объекте сведений о форме.</span><span class="sxs-lookup"><span data-stu-id="a7703-130">**CreateForm** opens the form by creating an instance of the form server for that form as described in the given form information object.</span></span> <span data-ttu-id="a7703-131">При необходимости **креатеформ** вызывает метод [Имапиформмгр::P репареформ](imapiformmgr-prepareform.md) для загрузки кода сервера форм на диск пользователя.</span><span class="sxs-lookup"><span data-stu-id="a7703-131">If required, **CreateForm** calls the [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) method to download the form server code to the user's disk.</span></span> 
  
<span data-ttu-id="a7703-132">Параметр _пфрминфотоактивате_ должен указать на объект сведений о форме, который был правильно распознан.</span><span class="sxs-lookup"><span data-stu-id="a7703-132">The  _pfrminfoToActivate_ parameter must point to a form information object that has been correctly resolved.</span></span> 
  
<span data-ttu-id="a7703-133">После открытия формы средство просмотра формы должно настроить сообщение с помощью интерфейса [иперсистмессаже](ipersistmessageiunknown.md) и при необходимости может задать контекст представления для формы.</span><span class="sxs-lookup"><span data-stu-id="a7703-133">After the form has been opened, the calling form viewer must set up a message by using the [IPersistMessage](ipersistmessageiunknown.md) interface and can optionally set up a view context for the form.</span></span> <span data-ttu-id="a7703-134">Более подробную информацию можно узнать в статье [Запуск сервера форм](launching-a-form-server.md).</span><span class="sxs-lookup"><span data-stu-id="a7703-134">For more information, see [Launching a Form Server](launching-a-form-server.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a7703-135">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="a7703-135">MFCMAPI reference</span></span>

<span data-ttu-id="a7703-136">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="a7703-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a7703-137">**Файл**</span><span class="sxs-lookup"><span data-stu-id="a7703-137">**File**</span></span>|<span data-ttu-id="a7703-138">**Функция**</span><span class="sxs-lookup"><span data-stu-id="a7703-138">**Function**</span></span>|<span data-ttu-id="a7703-139">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="a7703-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a7703-140">Мапиформфунктионс. cpp</span><span class="sxs-lookup"><span data-stu-id="a7703-140">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="a7703-141">Креатеанддисплайневмаилинфолдер</span><span class="sxs-lookup"><span data-stu-id="a7703-141">CreateAndDisplayNewMailInFolder</span></span>  <br/> |<span data-ttu-id="a7703-142">MFCMAPI использует метод **имапиформмгр:: креатеформ** , чтобы создать форму перед ее отображением.</span><span class="sxs-lookup"><span data-stu-id="a7703-142">MFCMAPI uses the **IMAPIFormMgr::CreateForm** method to create a form before displaying it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a7703-143">См. также</span><span class="sxs-lookup"><span data-stu-id="a7703-143">See also</span></span>



[<span data-ttu-id="a7703-144">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="a7703-144">IMAPIFormMgr::PrepareForm</span></span>](imapiformmgr-prepareform.md)
  
[<span data-ttu-id="a7703-145">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a7703-145">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
  
[<span data-ttu-id="a7703-146">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a7703-146">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="a7703-147">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="a7703-147">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="a7703-148">Запуск сервера форм</span><span class="sxs-lookup"><span data-stu-id="a7703-148">Launching a Form Server</span></span>](launching-a-form-server.md)

