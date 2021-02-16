---
title: IPSTOVERRIDEREQRegisterTrustedPSTOverrideHandler
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDEREQ.RegisterTrustedPSTOverrideHandler
api_type:
- COM
ms.assetid: 4a73c77c-7e32-4302-bffe-a1ea13574731
description: 'Last modified: February 24, 2013'
ms.openlocfilehash: acc0986dd80b549b0cb2b941a6937d47a4a959fe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279537"
---
# <a name="ipstoverridereqregistertrustedpstoverridehandler"></a><span data-ttu-id="67280-103">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span><span class="sxs-lookup"><span data-stu-id="67280-103">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span></span>

 
  
<span data-ttu-id="67280-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="67280-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="67280-105">Инициирует процедуру разблокировки для файла личных папок (PST).</span><span class="sxs-lookup"><span data-stu-id="67280-105">Initiates the unlocking procedure for a Personal Folders (.pst) file.</span></span>
  
```cpp
HRESULT RegisterTrustedPSTOverrideHandler (
  LPCWSTR pwzDllPath, 
  LPVOID pvClientData
); 

```

## <a name="parameters"></a><span data-ttu-id="67280-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="67280-106">Parameters</span></span>

 <span data-ttu-id="67280-107">_pwzDllPath_</span><span class="sxs-lookup"><span data-stu-id="67280-107">_pwzDllPath_</span></span>
  
> <span data-ttu-id="67280-108">[in] Указатель на путь к стороннее библиотеке динамической ссылки (DLL).</span><span class="sxs-lookup"><span data-stu-id="67280-108">[in] A pointer to the path of a third-party dynamic-link library (DLL).</span></span>
    
 <span data-ttu-id="67280-109">_pvClientData_</span><span class="sxs-lookup"><span data-stu-id="67280-109">_pvClientData_</span></span>
  
> <span data-ttu-id="67280-110">[in] Указатель на данные клиента, который будет передаваться поставщиком PST в последующие вызовы функции HrTrustedPSTOverrideHandlerCallback DLL.</span><span class="sxs-lookup"><span data-stu-id="67280-110">[in] A pointer to client data, which will be passed by the PST provider into subsequent calls to the DLL's HrTrustedPSTOverrideHandlerCallback function.</span></span> <span data-ttu-id="67280-111">Эти данные клиента могут использоваться DLL для проверки того, следует ли разблокировать PST-данные.</span><span class="sxs-lookup"><span data-stu-id="67280-111">This client data may be used by the DLL to assist in verifying whether the PST should be unlocked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="67280-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="67280-112">Return value</span></span>

<span data-ttu-id="67280-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="67280-113">S_OK</span></span>
  
> <span data-ttu-id="67280-114">Вызов функции был успешным.</span><span class="sxs-lookup"><span data-stu-id="67280-114">The function call was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="67280-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="67280-115">Remarks</span></span>

<span data-ttu-id="67280-116">DLL,указанный параметром wzDllPath, должен быть подписан с помощью цифрового сертификата.</span><span class="sxs-lookup"><span data-stu-id="67280-116">The DLL specified by the wzDllPath parameter must be signed using a digital certificate.</span></span> <span data-ttu-id="67280-117">DLL также должен экспортировать функцию со следующей подписью.</span><span class="sxs-lookup"><span data-stu-id="67280-117">The DLL must also export a function with the following signature.</span></span>
  
```
extern "C" HRESULT __cdecl HrTrustedPSTOverrideHandlerCallback(IMsgStore *pmstore, IUnknown *pOverride, LPVOID pvClientData)
```

<span data-ttu-id="67280-118">Эта функция будет вызвана с указателем на объект IMsgStore для PST, указателем на объект IUnknown, который реализует интерфейс IPSTOVERRIDE1, и указателем на данные, изначально предоставленные через pvClientData.</span><span class="sxs-lookup"><span data-stu-id="67280-118">This function will be called with a pointer to the IMsgStore object for the PST, a pointer to an IUnknown object that implements the IPSTOVERRIDE1 interface, and a pointer to the data originally supplied through pvClientData.</span></span>
  
<span data-ttu-id="67280-119">Дополнительные сведения см. в реализации обработора переопределения PST-данных для обхода [политики PSTDisableGrow в Outlook 2007.](https://support.microsoft.com/kb/956070)</span><span class="sxs-lookup"><span data-stu-id="67280-119">For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](https://support.microsoft.com/kb/956070).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="67280-120">См. также</span><span class="sxs-lookup"><span data-stu-id="67280-120">See also</span></span>



[<span data-ttu-id="67280-121">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="67280-121">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md)
  
[<span data-ttu-id="67280-122">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="67280-122">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

