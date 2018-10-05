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
description: 'Последнее изменение: 24 февраля 2013 г.'
ms.openlocfilehash: acc0986dd80b549b0cb2b941a6937d47a4a959fe
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393875"
---
# <a name="ipstoverridereqregistertrustedpstoverridehandler"></a><span data-ttu-id="a5341-103">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span><span class="sxs-lookup"><span data-stu-id="a5341-103">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span></span>

 
  
<span data-ttu-id="a5341-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a5341-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a5341-105">Инициирует разблокировка процедура файл личных папок (PST).</span><span class="sxs-lookup"><span data-stu-id="a5341-105">Initiates the unlocking procedure for a Personal Folders (.pst) file.</span></span>
  
```cpp
HRESULT RegisterTrustedPSTOverrideHandler (
  LPCWSTR pwzDllPath, 
  LPVOID pvClientData
); 

```

## <a name="parameters"></a><span data-ttu-id="a5341-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a5341-106">Parameters</span></span>

 <span data-ttu-id="a5341-107">_pwzDllPath_</span><span class="sxs-lookup"><span data-stu-id="a5341-107">_pwzDllPath_</span></span>
  
> <span data-ttu-id="a5341-108">[in] Указатель на путь сторонних производителей библиотеки динамической компоновки (DLL).</span><span class="sxs-lookup"><span data-stu-id="a5341-108">[in] A pointer to the path of a third-party dynamic-link library (DLL).</span></span>
    
 <span data-ttu-id="a5341-109">_pvClientData_</span><span class="sxs-lookup"><span data-stu-id="a5341-109">_pvClientData_</span></span>
  
> <span data-ttu-id="a5341-110">[in] Указатель на данные клиента, которые будут передаваться поставщиком PST-файлов в последующие вызовы функции HrTrustedPSTOverrideHandlerCallback библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="a5341-110">[in] A pointer to client data, which will be passed by the PST provider into subsequent calls to the DLL's HrTrustedPSTOverrideHandlerCallback function.</span></span> <span data-ttu-id="a5341-111">Эти данные клиента могут быть использованы с библиотеки DLL для помощи при проверке, следует ли разблокированными PST-файлов.</span><span class="sxs-lookup"><span data-stu-id="a5341-111">This client data may be used by the DLL to assist in verifying whether the PST should be unlocked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a5341-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a5341-112">Return value</span></span>

<span data-ttu-id="a5341-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="a5341-113">S_OK</span></span>
  
> <span data-ttu-id="a5341-114">Вызов функции прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="a5341-114">The function call was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a5341-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="a5341-115">Remarks</span></span>

<span data-ttu-id="a5341-116">DLL, указанного с помощью параметра wzDllPath должны быть подписаны цифровым сертификатом.</span><span class="sxs-lookup"><span data-stu-id="a5341-116">The DLL specified by the wzDllPath parameter must be signed using a digital certificate.</span></span> <span data-ttu-id="a5341-117">Библиотеки DLL необходимо экспортировать функции с указанной ниже сигнатурой.</span><span class="sxs-lookup"><span data-stu-id="a5341-117">The DLL must also export a function with the following signature.</span></span>
  
```
extern "C" HRESULT __cdecl HrTrustedPSTOverrideHandlerCallback(IMsgStore *pmstore, IUnknown *pOverride, LPVOID pvClientData)
```

<span data-ttu-id="a5341-118">Эта функция будет вызываться с указатель на объект IMsgStore для PST-файлов, указатель на объект IUnknown, который реализует интерфейс IPSTOVERRIDE1 и указатель на данные, изначально обеспечиваться pvClientData.</span><span class="sxs-lookup"><span data-stu-id="a5341-118">This function will be called with a pointer to the IMsgStore object for the PST, a pointer to an IUnknown object that implements the IPSTOVERRIDE1 interface, and a pointer to the data originally supplied through pvClientData.</span></span>
  
<span data-ttu-id="a5341-119">Дополнительные сведения см в [реализации обработчика переопределение PST-файлов для обхода политики PSTDisableGrow в Outlook 2007](https://support.microsoft.com/kb/956070).</span><span class="sxs-lookup"><span data-stu-id="a5341-119">For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](https://support.microsoft.com/kb/956070).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a5341-120">См. также</span><span class="sxs-lookup"><span data-stu-id="a5341-120">See also</span></span>



[<span data-ttu-id="a5341-121">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a5341-121">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md)
  
[<span data-ttu-id="a5341-122">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a5341-122">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

