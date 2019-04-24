---
title: Ипстоверридерекрегистертрустедпстоверридехандлер
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
description: 'Дата последнего изменения: 24 февраля 2013 г.'
ms.openlocfilehash: acc0986dd80b549b0cb2b941a6937d47a4a959fe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279537"
---
# <a name="ipstoverridereqregistertrustedpstoverridehandler"></a><span data-ttu-id="8ccd6-103">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span><span class="sxs-lookup"><span data-stu-id="8ccd6-103">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span></span>

 
  
<span data-ttu-id="8ccd6-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8ccd6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8ccd6-105">Инициирует процедуру разблокировки для файла личных папок (PST).</span><span class="sxs-lookup"><span data-stu-id="8ccd6-105">Initiates the unlocking procedure for a Personal Folders (.pst) file.</span></span>
  
```cpp
HRESULT RegisterTrustedPSTOverrideHandler (
  LPCWSTR pwzDllPath, 
  LPVOID pvClientData
); 

```

## <a name="parameters"></a><span data-ttu-id="8ccd6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8ccd6-106">Parameters</span></span>

 <span data-ttu-id="8ccd6-107">_Пвздллпас_</span><span class="sxs-lookup"><span data-stu-id="8ccd6-107">_pwzDllPath_</span></span>
  
> <span data-ttu-id="8ccd6-108">возврата Указатель на путь к сторонней библиотеке динамической компоновки (DLL).</span><span class="sxs-lookup"><span data-stu-id="8ccd6-108">[in] A pointer to the path of a third-party dynamic-link library (DLL).</span></span>
    
 <span data-ttu-id="8ccd6-109">_Пвклиентдата_</span><span class="sxs-lookup"><span data-stu-id="8ccd6-109">_pvClientData_</span></span>
  
> <span data-ttu-id="8ccd6-110">возврата Указатель на клиентские данные, которые будут переданы поставщиком PST при последующих вызовах функции Хртрустедпстоверридехандлеркаллбакк библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="8ccd6-110">[in] A pointer to client data, which will be passed by the PST provider into subsequent calls to the DLL's HrTrustedPSTOverrideHandlerCallback function.</span></span> <span data-ttu-id="8ccd6-111">Эти данные клиента могут использоваться БИБЛИОТЕКой DLL для помощи в проверке того, следует ли разблокировать PST-файл.</span><span class="sxs-lookup"><span data-stu-id="8ccd6-111">This client data may be used by the DLL to assist in verifying whether the PST should be unlocked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8ccd6-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8ccd6-112">Return value</span></span>

<span data-ttu-id="8ccd6-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="8ccd6-113">S_OK</span></span>
  
> <span data-ttu-id="8ccd6-114">Вызов функции выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="8ccd6-114">The function call was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8ccd6-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="8ccd6-115">Remarks</span></span>

<span data-ttu-id="8ccd6-116">Библиотека DLL, заданная параметром Вздллпас, должна быть подписана с помощью цифрового сертификата.</span><span class="sxs-lookup"><span data-stu-id="8ccd6-116">The DLL specified by the wzDllPath parameter must be signed using a digital certificate.</span></span> <span data-ttu-id="8ccd6-117">Кроме того, Библиотека DLL должна экспортировать функцию со следующей подписью.</span><span class="sxs-lookup"><span data-stu-id="8ccd6-117">The DLL must also export a function with the following signature.</span></span>
  
```
extern "C" HRESULT __cdecl HrTrustedPSTOverrideHandlerCallback(IMsgStore *pmstore, IUnknown *pOverride, LPVOID pvClientData)
```

<span data-ttu-id="8ccd6-118">Эта функция будет вызываться с указателем на объект IMsgStore для PST-файла, указателем на объект IUnknown, который реализует интерфейс IPSTOVERRIDE1, и указателем на данные, изначально предоставленные с помощью Пвклиентдата.</span><span class="sxs-lookup"><span data-stu-id="8ccd6-118">This function will be called with a pointer to the IMsgStore object for the PST, a pointer to an IUnknown object that implements the IPSTOVERRIDE1 interface, and a pointer to the data originally supplied through pvClientData.</span></span>
  
<span data-ttu-id="8ccd6-119">Для получения дополнительных сведений Узнайте, [как реализовать обработчик переопределения PST-файлов, чтобы обойти политику пстдисаблегров в Outlook 2007](https://support.microsoft.com/kb/956070).</span><span class="sxs-lookup"><span data-stu-id="8ccd6-119">For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](https://support.microsoft.com/kb/956070).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8ccd6-120">См. также</span><span class="sxs-lookup"><span data-stu-id="8ccd6-120">See also</span></span>



[<span data-ttu-id="8ccd6-121">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8ccd6-121">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md)
  
[<span data-ttu-id="8ccd6-122">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8ccd6-122">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

