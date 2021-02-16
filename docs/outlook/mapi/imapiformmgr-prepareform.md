---
title: IMAPIFormMgrPrepareForm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.PrepareForm
api_type:
- COM
ms.assetid: 8f8ee2cb-1c2a-4958-b01e-2f4aab689f89
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: d0d5d8fe13a3c192dc0b0a8ddc0f5f945fa16f15
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416652"
---
# <a name="imapiformmgrprepareform"></a><span data-ttu-id="df324-103">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="df324-103">IMAPIFormMgr::PrepareForm</span></span>

  
  
<span data-ttu-id="df324-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="df324-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="df324-105">Скачивает форму для открытия.</span><span class="sxs-lookup"><span data-stu-id="df324-105">Downloads a form for opening.</span></span>
  
```cpp
HRESULT PrepareForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMINFO pfrmiInfo
);
```

## <a name="parameters"></a><span data-ttu-id="df324-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="df324-106">Parameters</span></span>

 <span data-ttu-id="df324-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="df324-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="df324-108">[in] Handle to the parent window of the progress indicator that is displayed while the form is downloaded.</span><span class="sxs-lookup"><span data-stu-id="df324-108">[in] A handle to the parent window of the progress indicator that is displayed while the form is downloaded.</span></span> <span data-ttu-id="df324-109">Параметр _ulUIParam_ игнорируется, если MAPI_DIALOG флага в параметре _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="df324-109">The  _ulUIParam_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="df324-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="df324-110">_ulFlags_</span></span>
  
> <span data-ttu-id="df324-111">[in] Битоваяmas флагов, которая управляет загрузкой формы.</span><span class="sxs-lookup"><span data-stu-id="df324-111">[in] A bitmask of flags that controls how the form is downloaded.</span></span> <span data-ttu-id="df324-112">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="df324-112">The following flag can be set:</span></span>
    
<span data-ttu-id="df324-113">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="df324-113">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="df324-114">Отображает пользовательский интерфейс для предоставления состояния или запроса дополнительных сведений.</span><span class="sxs-lookup"><span data-stu-id="df324-114">Displays a user interface to provide status or prompt the user for more information.</span></span> <span data-ttu-id="df324-115">Если этот флаг не установлен, пользовательский интерфейс не отображается.</span><span class="sxs-lookup"><span data-stu-id="df324-115">If this flag is not set, no user interface is displayed.</span></span>
    
 <span data-ttu-id="df324-116">_pfrmiInfo_</span><span class="sxs-lookup"><span data-stu-id="df324-116">_pfrmiInfo_</span></span>
  
> <span data-ttu-id="df324-117">[in] Указатель на объект сведений о форме для скачивания формы.</span><span class="sxs-lookup"><span data-stu-id="df324-117">[in] A pointer to a form information object for the form to be downloaded.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="df324-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="df324-118">Return value</span></span>

<span data-ttu-id="df324-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="df324-119">S_OK</span></span> 
  
> <span data-ttu-id="df324-120">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="df324-120">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="df324-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="df324-121">Remarks</span></span>

<span data-ttu-id="df324-122">Посетители форм вызовите **метод IMAPIFormMgr::P repareForm,** чтобы скачать форму из контейнера формы для открытия.</span><span class="sxs-lookup"><span data-stu-id="df324-122">Form viewers call the **IMAPIFormMgr::PrepareForm** method to download a form from a form container for opening.</span></span> <span data-ttu-id="df324-123">Большинству средств просмотра форм не нужно вызывать **PrepareForm,** так как методы [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) и [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) при необходимости называют **PrepareForm.**</span><span class="sxs-lookup"><span data-stu-id="df324-123">Most form viewers do not need to call **PrepareForm**, because both the [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) and [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) methods call **PrepareForm**, if necessary.</span></span> 
  
<span data-ttu-id="df324-124">Вы можете использовать **PrepareForm** для получения библиотек динамической ссылки (DLL) и других файлов, связанных с формой, для их изменения.</span><span class="sxs-lookup"><span data-stu-id="df324-124">You can use **PrepareForm** to obtain the dynamic-link libraries (DLLs) and other files associated with a form to modify them.</span></span> <span data-ttu-id="df324-125">Если измененная форма загружается обратно в контейнер формы, ее необходимо переустановить.</span><span class="sxs-lookup"><span data-stu-id="df324-125">If the modified form is loaded back into its form container, it must be reinstalled.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="df324-126">См. также</span><span class="sxs-lookup"><span data-stu-id="df324-126">See also</span></span>



[<span data-ttu-id="df324-127">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="df324-127">IMAPIFormMgr::CreateForm</span></span>](imapiformmgr-createform.md)
  
[<span data-ttu-id="df324-128">IMAPIFormMgr::LoadForm</span><span class="sxs-lookup"><span data-stu-id="df324-128">IMAPIFormMgr::LoadForm</span></span>](imapiformmgr-loadform.md)
  
[<span data-ttu-id="df324-129">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="df324-129">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

