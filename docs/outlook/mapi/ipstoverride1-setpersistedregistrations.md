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
description: 'Последнее изменение: 08 ноября 2011 г.'
ms.openlocfilehash: 3592584a08bf14725c0289831740e91fb8f1a5b2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587623"
---
# <a name="ipstoverride1setpersistedregistrations"></a><span data-ttu-id="a0c74-103">IPSTOVERRIDE1::SetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="a0c74-103">IPSTOVERRIDE1::SetPersistedRegistrations</span></span>

<span data-ttu-id="a0c74-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a0c74-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a0c74-105">Регистрирует файлы личных папок (PST) для автоматического разблокирование Предотвращение дальнейшие вызовы HrTrustedPSTOverrideHandlerCallback.</span><span class="sxs-lookup"><span data-stu-id="a0c74-105">Registers Personal Folders (.pst) files for automatic unlocking, avoiding further calls to the HrTrustedPSTOverrideHandlerCallback.</span></span>
  
```cpp
HRESULT SetPersistedRegistrations(
  SPropValue *pmval
);
```

## <a name="parameters"></a><span data-ttu-id="a0c74-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a0c74-106">Parameters</span></span>

<span data-ttu-id="a0c74-107">_pmval_</span><span class="sxs-lookup"><span data-stu-id="a0c74-107">_pmval_</span></span>
  
> <span data-ttu-id="a0c74-108">[in] Структура [SPropValue](spropvalue.md) , содержащая указатель на путь библиотеки динамической компоновки (DLL) для регистрации.</span><span class="sxs-lookup"><span data-stu-id="a0c74-108">[in] An [SPropValue](spropvalue.md) structure that contains a pointer to the path of the dynamic-link library (DLL) to register.</span></span> <span data-ttu-id="a0c74-109">Структура имеет следующие характеристики:</span><span class="sxs-lookup"><span data-stu-id="a0c74-109">The structure has the following characteristics:</span></span> 
    
   - <span data-ttu-id="a0c74-110">UlPropTag [PROP_TAG](prop_tag.md)(PT_MV_UNICODE, PROP_ID_NULL).</span><span class="sxs-lookup"><span data-stu-id="a0c74-110">A ulPropTag of [PROP_TAG](prop_tag.md)(PT_MV_UNICODE, PROP_ID_NULL).</span></span>
    
   - <span data-ttu-id="a0c74-111">Свойство value MVszW, заданный в массив строк символ Unicode символом null.</span><span class="sxs-lookup"><span data-stu-id="a0c74-111">An MVszW value property that is set to an array of null-terminated Unicode character strings.</span></span> <span data-ttu-id="a0c74-112">Дополнительные сведения см в разделе [SWStringArray](swstringarray.md) .</span><span class="sxs-lookup"><span data-stu-id="a0c74-112">For more information see the [SWStringArray](swstringarray.md) topic.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="a0c74-113">SPropValue хранится в свойстве MAPI в диапазоне внутренних PST-файлов.</span><span class="sxs-lookup"><span data-stu-id="a0c74-113">The SPropValue is stored in a MAPI property in the PST's internal range.</span></span> <span data-ttu-id="a0c74-114">Это свойство недоступно для обычных приложений MAPI.</span><span class="sxs-lookup"><span data-stu-id="a0c74-114">This property is inaccessible to ordinary MAPI applications.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="a0c74-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a0c74-115">Return value</span></span>

<span data-ttu-id="a0c74-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="a0c74-116">S_OK</span></span> 
  
> <span data-ttu-id="a0c74-117">Вызов функции прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="a0c74-117">The function call was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a0c74-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="a0c74-118">Remarks</span></span>

<span data-ttu-id="a0c74-119">Постоянные регистраций может отрицательно сказаться на производительности приложения, такие как Outlook и Windows Desktop Search, откройте PST-файлов.</span><span class="sxs-lookup"><span data-stu-id="a0c74-119">Persisted registrations may adversely affect the performance of applications, such as Outlook and Windows Desktop Search, that open PSTs.</span></span> <span data-ttu-id="a0c74-120">Рассмотрите возможность влияют на производительность при использовании или расширении использования постоянных регистрации.</span><span class="sxs-lookup"><span data-stu-id="a0c74-120">Consider the performance effect when using or expanding the usage of persisted registrations.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="a0c74-121">Этот метод реализован только для кодировки Юникод.</span><span class="sxs-lookup"><span data-stu-id="a0c74-121">This method is implemented for Unicode only.</span></span> <span data-ttu-id="a0c74-122">Более того он будет заблаговременно ошибкой, если какие-либо из следующих путей в массиве имеет расширение имени файла из библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="a0c74-122">Further, it will preemptively fail if any of the paths in the array do not have a file name extension of .dll.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a0c74-123">См. также</span><span class="sxs-lookup"><span data-stu-id="a0c74-123">See also</span></span>

- [<span data-ttu-id="a0c74-124">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a0c74-124">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md) 
- [<span data-ttu-id="a0c74-125">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a0c74-125">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

