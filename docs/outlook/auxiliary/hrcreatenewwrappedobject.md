---
title: HrCreateNewWrappedObject
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 780ade1c-88d0-04d2-ba7e-251c19c43438
description: Создает объект, клиент может получить доступ в предпочтительном символьном формате.
ms.openlocfilehash: 3f68e0f275bcc5df065b3113d3322d6957f76df0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384194"
---
# <a name="hrcreatenewwrappedobject"></a><span data-ttu-id="291d4-103">HrCreateNewWrappedObject</span><span class="sxs-lookup"><span data-stu-id="291d4-103">HrCreateNewWrappedObject</span></span>

<span data-ttu-id="291d4-104">Создает объект, клиент может получить доступ в предпочтительном символьном формате.</span><span class="sxs-lookup"><span data-stu-id="291d4-104">Creates an object that a client can access in a preferred character format.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="291d4-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="291d4-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="291d4-106">Экспортировать с:</span><span class="sxs-lookup"><span data-stu-id="291d4-106">Exported by:</span></span>  <br/> |<span data-ttu-id="291d4-107">Msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="291d4-107">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="291d4-108">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="291d4-108">Called by:</span></span>  <br/> |<span data-ttu-id="291d4-109">Клиент</span><span class="sxs-lookup"><span data-stu-id="291d4-109">Client</span></span>  <br/> |
|<span data-ttu-id="291d4-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="291d4-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="291d4-111">Outlook</span><span class="sxs-lookup"><span data-stu-id="291d4-111">Outlook</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="291d4-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="291d4-112">Parameters</span></span>

<span data-ttu-id="291d4-113">_pvUnwrapped_</span><span class="sxs-lookup"><span data-stu-id="291d4-113">_pvUnwrapped_</span></span>
  
> <span data-ttu-id="291d4-114">[in] Начальное развернутый объект Outlook.</span><span class="sxs-lookup"><span data-stu-id="291d4-114">[in] The initial unwrapped Outlook object.</span></span> <span data-ttu-id="291d4-115">Должен реализовывать следующие интерфейсы:</span><span class="sxs-lookup"><span data-stu-id="291d4-115">Must implement one of the following interfaces:</span></span>
    
   - <span data-ttu-id="291d4-116">[IMailUser: IMAPIProp](https://msdn.microsoft.com/library/74c25870-62d9-484a-9a99-4dc35c52479e%28Office.15%29.aspx), [IMAPIFolder: IMAPIContainer](https://msdn.microsoft.com/library/bc2e8d17-7687-43c2-8f01-b677703f7288%28Office.15%29.aspx), [IMessage: IMAPIProp](https://msdn.microsoft.com/library/7e244d40-595e-432c-aa8c-f9f62ca3c138%28Office.15%29.aspx), [IMsgStore: IMAPIProp](https://msdn.microsoft.com/library/20090114-b183-4767-8971-a304a9aa47e6%28Office.15%29.aspx), [IMSLogon: IUnknown](https://msdn.microsoft.com/library/d87093dc-f705-465f-ab3c-944ca0cd3e54%28Office.15%29.aspx), или [IOSTX](https://msdn.microsoft.com/library/f374d8d9-be8e-2489-d5fe-8a92e0ecfc6f%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="291d4-116">[IMailUser : IMAPIProp](https://msdn.microsoft.com/library/74c25870-62d9-484a-9a99-4dc35c52479e%28Office.15%29.aspx), [IMAPIFolder : IMAPIContainer](https://msdn.microsoft.com/library/bc2e8d17-7687-43c2-8f01-b677703f7288%28Office.15%29.aspx), [IMessage : IMAPIProp](https://msdn.microsoft.com/library/7e244d40-595e-432c-aa8c-f9f62ca3c138%28Office.15%29.aspx), [IMsgStore : IMAPIProp](https://msdn.microsoft.com/library/20090114-b183-4767-8971-a304a9aa47e6%28Office.15%29.aspx), [IMSLogon : IUnknown](https://msdn.microsoft.com/library/d87093dc-f705-465f-ab3c-944ca0cd3e54%28Office.15%29.aspx), or [IOSTX](https://msdn.microsoft.com/library/f374d8d9-be8e-2489-d5fe-8a92e0ecfc6f%28Office.15%29.aspx).</span></span>
    
<span data-ttu-id="291d4-117">_ulUnwrappedFlags_</span><span class="sxs-lookup"><span data-stu-id="291d4-117">_ulUnwrappedFlags_</span></span>
  
> <span data-ttu-id="291d4-118">[in] Флаги, создание характеристик развернутый исходный объект.</span><span class="sxs-lookup"><span data-stu-id="291d4-118">[in] Flags that characterize the unwrapped initial object.</span></span> <span data-ttu-id="291d4-119">Должен быть один или несколько из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="291d4-119">Must be one or more of the following values:</span></span>
    
   - <span data-ttu-id="291d4-120">DDLWRAP_FLAG_ANSI — объект Unwrapped — ANSI.</span><span class="sxs-lookup"><span data-stu-id="291d4-120">DDLWRAP_FLAG_ANSI—Unwrapped object is ANSI.</span></span>
    
   - <span data-ttu-id="291d4-121">DDLWRAP_FLAG_UNICODE — объект Unwrapped — Юникод.</span><span class="sxs-lookup"><span data-stu-id="291d4-121">DDLWRAP_FLAG_UNICODE—Unwrapped object is UNICODE.</span></span>
    
<span data-ttu-id="291d4-122">_ulWrappedFlags_</span><span class="sxs-lookup"><span data-stu-id="291d4-122">_ulWrappedFlags_</span></span>
  
>  <span data-ttu-id="291d4-123">[in] Флаги предпочтительном символьном формате.</span><span class="sxs-lookup"><span data-stu-id="291d4-123">[in] Flags for the preferred character format.</span></span> <span data-ttu-id="291d4-124">Должен быть один или несколько из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="291d4-124">Must be one or more of the following values:</span></span> 
    
   - <span data-ttu-id="291d4-125">DDLWRAP_FLAG_ANSI — объект Wrapped будут предоставляться как ANSI.</span><span class="sxs-lookup"><span data-stu-id="291d4-125">DDLWRAP_FLAG_ANSI—Wrapped object will be exposed as ANSI.</span></span>
    
   - <span data-ttu-id="291d4-126">DDLWRAP_FLAG_UNICODE — объект Wrapped будет предоставлено в качестве Юникод.</span><span class="sxs-lookup"><span data-stu-id="291d4-126">DDLWRAP_FLAG_UNICODE—Wrapped object will be exposed as UNICODE.</span></span>
    
<span data-ttu-id="291d4-127">_pIID_</span><span class="sxs-lookup"><span data-stu-id="291d4-127">_pIID_</span></span>
  
>  <span data-ttu-id="291d4-128">[in] Идентификатор элемента интерфейс, поддерживаемый развернутый объект; Задайте его значение NULL, если это не известен.</span><span class="sxs-lookup"><span data-stu-id="291d4-128">[in] The identifier of the interface supported by the unwrapped object; set it to NULL if this is unknown.</span></span> 
    
<span data-ttu-id="291d4-129">_pulReserved_</span><span class="sxs-lookup"><span data-stu-id="291d4-129">_pulReserved_</span></span>
  
>  <span data-ttu-id="291d4-130">[in] Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="291d4-130">[in] This parameter is not used.</span></span> <span data-ttu-id="291d4-131">Это должен быть NULL.</span><span class="sxs-lookup"><span data-stu-id="291d4-131">It must be NULL.</span></span> 
    
<span data-ttu-id="291d4-132">_fCheckWrap_</span><span class="sxs-lookup"><span data-stu-id="291d4-132">_fCheckWrap_</span></span>
  
>  <span data-ttu-id="291d4-133">[in] Присвойте этому параметру значение **true** , если _pvUnwrapped_ необходимо проверить его формате перед переносом; Если объект, должны быть помещены без проверки, присвойте этому параметру **значение false** .</span><span class="sxs-lookup"><span data-stu-id="291d4-133">[in] Set this parameter to **true** if  _pvUnwrapped_ should be checked for its format before wrapping; set it to **false** if the object should be wrapped without checking.</span></span> 
    
<span data-ttu-id="291d4-134">_ppvWrapped_</span><span class="sxs-lookup"><span data-stu-id="291d4-134">_ppvWrapped_</span></span>
  
>  <span data-ttu-id="291d4-135">[out] Указатель на запрошенный объект, заключенное в запрошенные символьном формате.</span><span class="sxs-lookup"><span data-stu-id="291d4-135">[out] A pointer to the requested object, wrapped in the requested character format.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="291d4-136">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="291d4-136">Return values</span></span>

<span data-ttu-id="291d4-137">S_OK if the call succeeded; otherwise, an error code.</span><span class="sxs-lookup"><span data-stu-id="291d4-137">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="291d4-138">Remarks</span><span class="sxs-lookup"><span data-stu-id="291d4-138">Remarks</span></span>

<span data-ttu-id="291d4-139">Передача перенесенного объекта с _fCheckWrap_ присвоено **значение true** приведет к развернутый объект.</span><span class="sxs-lookup"><span data-stu-id="291d4-139">Passing in a wrapped object with  _fCheckWrap_ set to **true** will result in an unwrapped object.</span></span> <span data-ttu-id="291d4-140">Независимо от того, является ли оформлено возвращенного объекта клиент несет ответственность за освобождение ссылки на возвращенный объект.</span><span class="sxs-lookup"><span data-stu-id="291d4-140">Regardless of whether or not the returned object is wrapped, the client is responsible for releasing the reference on the returned object.</span></span> 
  
<span data-ttu-id="291d4-141">При использовании **GetProcAddress** следует искать адреса этой функции msmapi32.dll, укажите **HrCreateNewWrappedObject@28** в качестве имени процедуры.</span><span class="sxs-lookup"><span data-stu-id="291d4-141">When using **GetProcAddress** to look for the address of this function in msmapi32.dll, specify **HrCreateNewWrappedObject@28** as the procedure name.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="291d4-142">См. также</span><span class="sxs-lookup"><span data-stu-id="291d4-142">See also</span></span>

- [<span data-ttu-id="291d4-143">About the Data Degradation Layer API</span><span class="sxs-lookup"><span data-stu-id="291d4-143">About the Data Degradation Layer API</span></span>](about-the-data-degradation-layer-api.md)
- [<span data-ttu-id="291d4-144">Константы (layer уменьшение объема данных API).</span><span class="sxs-lookup"><span data-stu-id="291d4-144">Constants (Data degradation layer API)</span></span>](constants-data-degradation-layer-api.md)

