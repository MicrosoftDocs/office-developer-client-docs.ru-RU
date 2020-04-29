---
title: имапиформмгрпрепареформ
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
# <a name="imapiformmgrprepareform"></a><span data-ttu-id="a03a9-103">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="a03a9-103">IMAPIFormMgr::PrepareForm</span></span>

  
  
<span data-ttu-id="a03a9-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a03a9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a03a9-105">Загружает форму для открытия.</span><span class="sxs-lookup"><span data-stu-id="a03a9-105">Downloads a form for opening.</span></span>
  
```cpp
HRESULT PrepareForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMINFO pfrmiInfo
);
```

## <a name="parameters"></a><span data-ttu-id="a03a9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a03a9-106">Parameters</span></span>

 <span data-ttu-id="a03a9-107">_улуипарам_</span><span class="sxs-lookup"><span data-stu-id="a03a9-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="a03a9-108">возврата Дескриптор родительского окна индикатора хода выполнения, отображаемого при загрузке формы.</span><span class="sxs-lookup"><span data-stu-id="a03a9-108">[in] A handle to the parent window of the progress indicator that is displayed while the form is downloaded.</span></span> <span data-ttu-id="a03a9-109">Параметр _улуипарам_ игнорируется, если в параметре _ulFlags_ не задан флаг MAPI_DIALOG.</span><span class="sxs-lookup"><span data-stu-id="a03a9-109">The  _ulUIParam_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="a03a9-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a03a9-110">_ulFlags_</span></span>
  
> <span data-ttu-id="a03a9-111">возврата Битовая маска флагов, определяющих способ загрузки формы.</span><span class="sxs-lookup"><span data-stu-id="a03a9-111">[in] A bitmask of flags that controls how the form is downloaded.</span></span> <span data-ttu-id="a03a9-112">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="a03a9-112">The following flag can be set:</span></span>
    
<span data-ttu-id="a03a9-113">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="a03a9-113">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="a03a9-114">Отображает пользовательский интерфейс для предоставления сведений о состоянии или предлагает пользователю ввести дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="a03a9-114">Displays a user interface to provide status or prompt the user for more information.</span></span> <span data-ttu-id="a03a9-115">Если этот флаг не установлен, Пользовательский интерфейс не отображается.</span><span class="sxs-lookup"><span data-stu-id="a03a9-115">If this flag is not set, no user interface is displayed.</span></span>
    
 <span data-ttu-id="a03a9-116">_пфрмиинфо_</span><span class="sxs-lookup"><span data-stu-id="a03a9-116">_pfrmiInfo_</span></span>
  
> <span data-ttu-id="a03a9-117">возврата Указатель на объект информации формы для загружаемой формы.</span><span class="sxs-lookup"><span data-stu-id="a03a9-117">[in] A pointer to a form information object for the form to be downloaded.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a03a9-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a03a9-118">Return value</span></span>

<span data-ttu-id="a03a9-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="a03a9-119">S_OK</span></span> 
  
> <span data-ttu-id="a03a9-120">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="a03a9-120">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a03a9-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="a03a9-121">Remarks</span></span>

<span data-ttu-id="a03a9-122">Средства просмотра форм вызывают метод **имапиформмгр::P репареформ** для загрузки формы из контейнера формы для открытия.</span><span class="sxs-lookup"><span data-stu-id="a03a9-122">Form viewers call the **IMAPIFormMgr::PrepareForm** method to download a form from a form container for opening.</span></span> <span data-ttu-id="a03a9-123">Большинству средству просмотра форм не требуется вызывать **препареформ**, так как методы [Имапиформмгр:: креатеформ](imapiformmgr-createform.md) и [Имапиформмгр:: лоадформ](imapiformmgr-loadform.md) вызывают **препареформ**, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="a03a9-123">Most form viewers do not need to call **PrepareForm**, because both the [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) and [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) methods call **PrepareForm**, if necessary.</span></span> 
  
<span data-ttu-id="a03a9-124">С помощью **препареформ** можно получить библиотеки динамической компоновки (DLL) и другие файлы, связанные с формой, чтобы изменить их.</span><span class="sxs-lookup"><span data-stu-id="a03a9-124">You can use **PrepareForm** to obtain the dynamic-link libraries (DLLs) and other files associated with a form to modify them.</span></span> <span data-ttu-id="a03a9-125">Если измененная форма загружается обратно в контейнер форм, ее необходимо переустановить.</span><span class="sxs-lookup"><span data-stu-id="a03a9-125">If the modified form is loaded back into its form container, it must be reinstalled.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a03a9-126">См. также</span><span class="sxs-lookup"><span data-stu-id="a03a9-126">See also</span></span>



[<span data-ttu-id="a03a9-127">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="a03a9-127">IMAPIFormMgr::CreateForm</span></span>](imapiformmgr-createform.md)
  
[<span data-ttu-id="a03a9-128">IMAPIFormMgr::LoadForm</span><span class="sxs-lookup"><span data-stu-id="a03a9-128">IMAPIFormMgr::LoadForm</span></span>](imapiformmgr-loadform.md)
  
[<span data-ttu-id="a03a9-129">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a03a9-129">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

