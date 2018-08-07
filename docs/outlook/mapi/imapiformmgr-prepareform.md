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
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 3b10ac5906be0f95930be3bef51fe2d78d583b03
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808949"
---
# <a name="imapiformmgrprepareform"></a><span data-ttu-id="dc799-103">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="dc799-103">IMAPIFormMgr::PrepareForm</span></span>

  
  
<span data-ttu-id="dc799-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dc799-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dc799-105">Файлы для загрузки для открытия формы.</span><span class="sxs-lookup"><span data-stu-id="dc799-105">Downloads a form for opening.</span></span>
  
```cpp
HRESULT PrepareForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMINFO pfrmiInfo
);
```

## <a name="parameters"></a><span data-ttu-id="dc799-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="dc799-106">Parameters</span></span>

 <span data-ttu-id="dc799-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="dc799-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="dc799-108">[in] Дескриптор родительского окна индикатор хода выполнения, который отображается при загрузке формы.</span><span class="sxs-lookup"><span data-stu-id="dc799-108">[in] A handle to the parent window of the progress indicator that is displayed while the form is downloaded.</span></span> <span data-ttu-id="dc799-109">Параметр _ulUIParam_ игнорируется, пока флаг MAPI_DIALOG будет выполнен с помощью параметра _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="dc799-109">The  _ulUIParam_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="dc799-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="dc799-110">_ulFlags_</span></span>
  
> <span data-ttu-id="dc799-111">[in] Битовая маска флаги, который управляет способа загрузки формы.</span><span class="sxs-lookup"><span data-stu-id="dc799-111">[in] A bitmask of flags that controls how the form is downloaded.</span></span> <span data-ttu-id="dc799-112">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="dc799-112">The following flag can be set:</span></span>
    
<span data-ttu-id="dc799-113">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="dc799-113">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="dc799-114">Отображает пользовательский интерфейс для предоставления состояния или запрашивать у пользователя для получения дополнительных сведений.</span><span class="sxs-lookup"><span data-stu-id="dc799-114">Displays a user interface to provide status or prompt the user for more information.</span></span> <span data-ttu-id="dc799-115">Если этот флаг не установлен, пользовательский интерфейс не отображается.</span><span class="sxs-lookup"><span data-stu-id="dc799-115">If this flag is not set, no user interface is displayed.</span></span>
    
 <span data-ttu-id="dc799-116">_pfrmiInfo_</span><span class="sxs-lookup"><span data-stu-id="dc799-116">_pfrmiInfo_</span></span>
  
> <span data-ttu-id="dc799-117">[in] Указатель на объект сведения формы для формы веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="dc799-117">[in] A pointer to a form information object for the form to be downloaded.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="dc799-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8">Return value</span></span>

<span data-ttu-id="dc799-119">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="dc799-119">S_OK</span></span> 
  
> <span data-ttu-id="dc799-120">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="dc799-120">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dc799-121">���������</span><span class="sxs-lookup"><span data-stu-id="dc799-121">Remarks</span></span>

<span data-ttu-id="dc799-122">Средства просмотра форм вызовите метод **IMAPIFormMgr::PrepareForm** можно загрузить из контейнера формы для открытия формы.</span><span class="sxs-lookup"><span data-stu-id="dc799-122">Form viewers call the **IMAPIFormMgr::PrepareForm** method to download a form from a form container for opening.</span></span> <span data-ttu-id="dc799-123">Большинство средств просмотра формы не нужно вызвать **PrepareForm**, так как как [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) , так и [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) методы вызова **PrepareForm**, при необходимости.</span><span class="sxs-lookup"><span data-stu-id="dc799-123">Most form viewers do not need to call **PrepareForm**, because both the [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) and [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) methods call **PrepareForm**, if necessary.</span></span> 
  
<span data-ttu-id="dc799-124">**PrepareForm** можно использовать для получения библиотеки динамической компоновки (DLL) и других файлов, связанный с формой для изменения их.</span><span class="sxs-lookup"><span data-stu-id="dc799-124">You can use **PrepareForm** to obtain the dynamic-link libraries (DLLs) and other files associated with a form to modify them.</span></span> <span data-ttu-id="dc799-125">Измененная форма загружается обратно в форму контейнера, необходимо повторно установить.</span><span class="sxs-lookup"><span data-stu-id="dc799-125">If the modified form is loaded back into its form container, it must be reinstalled.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dc799-126">См. также</span><span class="sxs-lookup"><span data-stu-id="dc799-126">See also</span></span>



[<span data-ttu-id="dc799-127">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="dc799-127">IMAPIFormMgr::CreateForm</span></span>](imapiformmgr-createform.md)
  
[<span data-ttu-id="dc799-128">IMAPIFormMgr::LoadForm</span><span class="sxs-lookup"><span data-stu-id="dc799-128">IMAPIFormMgr::LoadForm</span></span>](imapiformmgr-loadform.md)
  
[<span data-ttu-id="dc799-129">IMAPIFormMgr: IUnknown</span><span class="sxs-lookup"><span data-stu-id="dc799-129">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

