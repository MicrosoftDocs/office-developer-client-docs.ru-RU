---
title: IPSTOVERRIDE1SetPersistedRegistrations
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDE1.SetPersistedRegistrations
api_type:
- COM
ms.assetid: 5f4b62db-a759-41a2-9bea-29fc04b2962b
description: 'Дата последнего изменения: 08 ноября 2011 г.'
ms.openlocfilehash: 6583765d4df7c7bfae9e7a62606beaa857874954
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408350"
---
# <a name="ipstoverride1setpersistedregistrations"></a><span data-ttu-id="da243-103">IPSTOVERRIDE1::SetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="da243-103">IPSTOVERRIDE1::SetPersistedRegistrations</span></span>

<span data-ttu-id="da243-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="da243-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="da243-105">Регистрирует файлы личных папок (PST) для автоматической разблокировки, избегая дальнейших вызовов к Хртрустедпстоверридехандлеркаллбакк.</span><span class="sxs-lookup"><span data-stu-id="da243-105">Registers Personal Folders (.pst) files for automatic unlocking, avoiding further calls to the HrTrustedPSTOverrideHandlerCallback.</span></span>
  
```cpp
HRESULT SetPersistedRegistrations(
  SPropValue *pmval
);
```

## <a name="parameters"></a><span data-ttu-id="da243-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="da243-106">Parameters</span></span>

<span data-ttu-id="da243-107">_пмвал_</span><span class="sxs-lookup"><span data-stu-id="da243-107">_pmval_</span></span>
  
> <span data-ttu-id="da243-108">возврата Структура [спропвалуе](spropvalue.md) , содержащая указатель на путь к регистрируемой библиотеке динамической КОМПОНОВКИ (DLL).</span><span class="sxs-lookup"><span data-stu-id="da243-108">[in] An [SPropValue](spropvalue.md) structure that contains a pointer to the path of the dynamic-link library (DLL) to register.</span></span> <span data-ttu-id="da243-109">Структура имеет следующие характеристики:</span><span class="sxs-lookup"><span data-stu-id="da243-109">The structure has the following characteristics:</span></span> 
    
   - <span data-ttu-id="da243-110">Улпроптаг [PROP_TAG](prop_tag.md)(PT_MV_UNICODE, PROP_ID_NULL).</span><span class="sxs-lookup"><span data-stu-id="da243-110">A ulPropTag of [PROP_TAG](prop_tag.md)(PT_MV_UNICODE, PROP_ID_NULL).</span></span>
    
   - <span data-ttu-id="da243-111">Свойство Value Мвсзв, заданное для массива строк Юникода, заканчивающихся символами NULL.</span><span class="sxs-lookup"><span data-stu-id="da243-111">An MVszW value property that is set to an array of null-terminated Unicode character strings.</span></span> <span data-ttu-id="da243-112">Дополнительные сведения см. в разделе [свстрингаррай](swstringarray.md) .</span><span class="sxs-lookup"><span data-stu-id="da243-112">For more information see the [SWStringArray](swstringarray.md) topic.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="da243-113">Спропвалуе хранится в свойстве MAPI в внутреннем диапазоне PST-файла.</span><span class="sxs-lookup"><span data-stu-id="da243-113">The SPropValue is stored in a MAPI property in the PST's internal range.</span></span> <span data-ttu-id="da243-114">Это свойство недоступно для обычных MAPI-приложений.</span><span class="sxs-lookup"><span data-stu-id="da243-114">This property is inaccessible to ordinary MAPI applications.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="da243-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="da243-115">Return value</span></span>

<span data-ttu-id="da243-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="da243-116">S_OK</span></span> 
  
> <span data-ttu-id="da243-117">Вызов функции выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="da243-117">The function call was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="da243-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="da243-118">Remarks</span></span>

<span data-ttu-id="da243-119">Постоянные регистрации могут негативно повлиять на производительность приложений, таких как Outlook и панель поиска Windows, которые открывают PST.</span><span class="sxs-lookup"><span data-stu-id="da243-119">Persisted registrations may adversely affect the performance of applications, such as Outlook and Windows Desktop Search, that open PSTs.</span></span> <span data-ttu-id="da243-120">Учитывайте снижение производительности при использовании или развертывании постоянных регистраций.</span><span class="sxs-lookup"><span data-stu-id="da243-120">Consider the performance effect when using or expanding the usage of persisted registrations.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="da243-121">Этот метод реализован только для Юникода.</span><span class="sxs-lookup"><span data-stu-id="da243-121">This method is implemented for Unicode only.</span></span> <span data-ttu-id="da243-122">Кроме того, она завершается аварийно, если любой из путей в массиве не имеет расширения имени файла. dll.</span><span class="sxs-lookup"><span data-stu-id="da243-122">Further, it will preemptively fail if any of the paths in the array do not have a file name extension of .dll.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="da243-123">См. также</span><span class="sxs-lookup"><span data-stu-id="da243-123">See also</span></span>

- [<span data-ttu-id="da243-124">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="da243-124">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md) 
- [<span data-ttu-id="da243-125">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="da243-125">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

