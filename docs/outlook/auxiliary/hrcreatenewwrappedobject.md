---
title: HrCreateNewWrappedObject
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 780ade1c-88d0-04d2-ba7e-251c19c43438
description: Создает объект, к которому клиент может получить доступ в предпочтительном символьном формате.
ms.openlocfilehash: 3f68e0f275bcc5df065b3113d3322d6957f76df0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317607"
---
# <a name="hrcreatenewwrappedobject"></a><span data-ttu-id="b67ac-103">HrCreateNewWrappedObject</span><span class="sxs-lookup"><span data-stu-id="b67ac-103">HrCreateNewWrappedObject</span></span>

<span data-ttu-id="b67ac-104">Создает объект, к которому клиент может получить доступ в предпочтительном символьном формате.</span><span class="sxs-lookup"><span data-stu-id="b67ac-104">Creates an object that a client can access in a preferred character format.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b67ac-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="b67ac-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b67ac-106">Экспортировано:</span><span class="sxs-lookup"><span data-stu-id="b67ac-106">Exported by:</span></span>  <br/> |<span data-ttu-id="b67ac-107">MSMapi32. dll</span><span class="sxs-lookup"><span data-stu-id="b67ac-107">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="b67ac-108">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="b67ac-108">Called by:</span></span>  <br/> |<span data-ttu-id="b67ac-109">Client</span><span class="sxs-lookup"><span data-stu-id="b67ac-109">Client</span></span>  <br/> |
|<span data-ttu-id="b67ac-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="b67ac-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="b67ac-111">Outlook</span><span class="sxs-lookup"><span data-stu-id="b67ac-111">Outlook</span></span>  <br/> |
   
```cpp
HRESULT HrCreateNewWrappedObject( 
    LPVOID        pvUnwrapped, 
    ULONG         ulUnwrappedFlags, 
    ULONG         ulWrappedFlags, 
    const IID     *pIID, 
    const ULONG   *pulReserved, 
    BOOL          fCheckWrap, 
    LPVOID       *ppvWrapped 
);

```

## <a name="parameters"></a><span data-ttu-id="b67ac-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="b67ac-112">Parameters</span></span>

<span data-ttu-id="b67ac-113">_пвунвраппед_</span><span class="sxs-lookup"><span data-stu-id="b67ac-113">_pvUnwrapped_</span></span>
  
> <span data-ttu-id="b67ac-114">возврата Исходный неупакованный объект Outlook.</span><span class="sxs-lookup"><span data-stu-id="b67ac-114">[in] The initial unwrapped Outlook object.</span></span> <span data-ttu-id="b67ac-115">Необходимо реализовать один из следующих интерфейсов:</span><span class="sxs-lookup"><span data-stu-id="b67ac-115">Must implement one of the following interfaces:</span></span>
    
   - <span data-ttu-id="b67ac-116">[Имаилусер: IMAPIProp](https://msdn.microsoft.com/library/74c25870-62d9-484a-9a99-4dc35c52479e%28Office.15%29.aspx), [IMAPIFolder: IMAPIContainer](https://msdn.microsoft.com/library/bc2e8d17-7687-43c2-8f01-b677703f7288%28Office.15%29.aspx), [iMessage: IMAPIProp](https://msdn.microsoft.com/library/7e244d40-595e-432c-aa8c-f9f62ca3c138%28Office.15%29.aspx), [IMsgStore: IMAPIProp](https://msdn.microsoft.com/library/20090114-b183-4767-8971-a304a9aa47e6%28Office.15%29.aspx), [имслогон: IUnknown](https://msdn.microsoft.com/library/d87093dc-f705-465f-ab3c-944ca0cd3e54%28Office.15%29.aspx)или [иосткс](https://msdn.microsoft.com/library/f374d8d9-be8e-2489-d5fe-8a92e0ecfc6f%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="b67ac-116">[IMailUser : IMAPIProp](https://msdn.microsoft.com/library/74c25870-62d9-484a-9a99-4dc35c52479e%28Office.15%29.aspx), [IMAPIFolder : IMAPIContainer](https://msdn.microsoft.com/library/bc2e8d17-7687-43c2-8f01-b677703f7288%28Office.15%29.aspx), [IMessage : IMAPIProp](https://msdn.microsoft.com/library/7e244d40-595e-432c-aa8c-f9f62ca3c138%28Office.15%29.aspx), [IMsgStore : IMAPIProp](https://msdn.microsoft.com/library/20090114-b183-4767-8971-a304a9aa47e6%28Office.15%29.aspx), [IMSLogon : IUnknown](https://msdn.microsoft.com/library/d87093dc-f705-465f-ab3c-944ca0cd3e54%28Office.15%29.aspx), or [IOSTX](https://msdn.microsoft.com/library/f374d8d9-be8e-2489-d5fe-8a92e0ecfc6f%28Office.15%29.aspx).</span></span>
    
<span data-ttu-id="b67ac-117">_улунвраппедфлагс_</span><span class="sxs-lookup"><span data-stu-id="b67ac-117">_ulUnwrappedFlags_</span></span>
  
> <span data-ttu-id="b67ac-118">возврата Флаги, характеризующие неупакованный исходный объект.</span><span class="sxs-lookup"><span data-stu-id="b67ac-118">[in] Flags that characterize the unwrapped initial object.</span></span> <span data-ttu-id="b67ac-119">Должно иметь одно или несколько из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="b67ac-119">Must be one or more of the following values:</span></span>
    
   - <span data-ttu-id="b67ac-120">DDLWRAP_FLAG_ANSI — неупакованный объект — ANSI.</span><span class="sxs-lookup"><span data-stu-id="b67ac-120">DDLWRAP_FLAG_ANSI—Unwrapped object is ANSI.</span></span>
    
   - <span data-ttu-id="b67ac-121">DDLWRAP_FLAG_UNICODE — неупакованный объект — UNICODE.</span><span class="sxs-lookup"><span data-stu-id="b67ac-121">DDLWRAP_FLAG_UNICODE—Unwrapped object is UNICODE.</span></span>
    
<span data-ttu-id="b67ac-122">_улвраппедфлагс_</span><span class="sxs-lookup"><span data-stu-id="b67ac-122">_ulWrappedFlags_</span></span>
  
>  <span data-ttu-id="b67ac-123">возврата Флаги для предпочтительного формата знаков.</span><span class="sxs-lookup"><span data-stu-id="b67ac-123">[in] Flags for the preferred character format.</span></span> <span data-ttu-id="b67ac-124">Должно иметь одно или несколько из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="b67ac-124">Must be one or more of the following values:</span></span> 
    
   - <span data-ttu-id="b67ac-125">DDLWRAP_FLAG_ANSI, упакованный объект будет представлен в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="b67ac-125">DDLWRAP_FLAG_ANSI—Wrapped object will be exposed as ANSI.</span></span>
    
   - <span data-ttu-id="b67ac-126">DDLWRAP_FLAG_UNICODE, упакованный объект будет представлен в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="b67ac-126">DDLWRAP_FLAG_UNICODE—Wrapped object will be exposed as UNICODE.</span></span>
    
<span data-ttu-id="b67ac-127">_пиид_</span><span class="sxs-lookup"><span data-stu-id="b67ac-127">_pIID_</span></span>
  
>  <span data-ttu-id="b67ac-128">возврата Идентификатор интерфейса, поддерживаемого неупакованным объектом; Если этот параметр неизвестен, установите для него значение NULL.</span><span class="sxs-lookup"><span data-stu-id="b67ac-128">[in] The identifier of the interface supported by the unwrapped object; set it to NULL if this is unknown.</span></span> 
    
<span data-ttu-id="b67ac-129">_пулресервед_</span><span class="sxs-lookup"><span data-stu-id="b67ac-129">_pulReserved_</span></span>
  
>  <span data-ttu-id="b67ac-130">возврата Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="b67ac-130">[in] This parameter is not used.</span></span> <span data-ttu-id="b67ac-131">Он должен иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="b67ac-131">It must be NULL.</span></span> 
    
<span data-ttu-id="b67ac-132">_фчеккврап_</span><span class="sxs-lookup"><span data-stu-id="b67ac-132">_fCheckWrap_</span></span>
  
>  <span data-ttu-id="b67ac-133">возврата Установите для этого параметра **значение true** , если перед переносом в _пвунвраппед_ необходимо проверить его формат. Задайте для него значение **false** , если объект необходимо включить в оболочку без проверки.</span><span class="sxs-lookup"><span data-stu-id="b67ac-133">[in] Set this parameter to **true** if  _pvUnwrapped_ should be checked for its format before wrapping; set it to **false** if the object should be wrapped without checking.</span></span> 
    
<span data-ttu-id="b67ac-134">_ппввраппед_</span><span class="sxs-lookup"><span data-stu-id="b67ac-134">_ppvWrapped_</span></span>
  
>  <span data-ttu-id="b67ac-135">вышли Указатель на запрошенный объект, заключенный в оболочку запрошенного формата знаков.</span><span class="sxs-lookup"><span data-stu-id="b67ac-135">[out] A pointer to the requested object, wrapped in the requested character format.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="b67ac-136">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="b67ac-136">Return values</span></span>

<span data-ttu-id="b67ac-137">S_OK if the call succeeded; otherwise, an error code.</span><span class="sxs-lookup"><span data-stu-id="b67ac-137">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b67ac-138">Примечания</span><span class="sxs-lookup"><span data-stu-id="b67ac-138">Remarks</span></span>

<span data-ttu-id="b67ac-139">При передаче упакованного объекта с _фчеккврап_ , для которого задано **значение true** , будет получен неупакованный объект.</span><span class="sxs-lookup"><span data-stu-id="b67ac-139">Passing in a wrapped object with  _fCheckWrap_ set to **true** will result in an unwrapped object.</span></span> <span data-ttu-id="b67ac-140">Независимо от того, является ли возвращенный объект упакованным, клиент несет ответственность за освобождение ссылки на возвращенный объект.</span><span class="sxs-lookup"><span data-stu-id="b67ac-140">Regardless of whether or not the returned object is wrapped, the client is responsible for releasing the reference on the returned object.</span></span> 
  
<span data-ttu-id="b67ac-141">При использовании **GetProcAddress** для поиска адреса этой функции в MSMapi32. dll укажите **HrCreateNewWrappedObject@28** в качестве имени процедуры.</span><span class="sxs-lookup"><span data-stu-id="b67ac-141">When using **GetProcAddress** to look for the address of this function in msmapi32.dll, specify **HrCreateNewWrappedObject@28** as the procedure name.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b67ac-142">См. также</span><span class="sxs-lookup"><span data-stu-id="b67ac-142">See also</span></span>

- [<span data-ttu-id="b67ac-143">Сведения об API уровня ухудшения данных</span><span class="sxs-lookup"><span data-stu-id="b67ac-143">About the Data Degradation Layer API</span></span>](about-the-data-degradation-layer-api.md)
- [<span data-ttu-id="b67ac-144">Константы (API уровня замедления данных)</span><span class="sxs-lookup"><span data-stu-id="b67ac-144">Constants (Data degradation layer API)</span></span>](constants-data-degradation-layer-api.md)

