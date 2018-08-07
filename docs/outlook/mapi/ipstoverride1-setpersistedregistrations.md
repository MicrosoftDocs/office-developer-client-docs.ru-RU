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
ms.openlocfilehash: 9895c558af94eebebe2dacdb6f9bf674e3de6263
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809564"
---
# <a name="ipstoverride1setpersistedregistrations"></a><span data-ttu-id="7ba83-103">IPSTOVERRIDE1::SetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="7ba83-103">IPSTOVERRIDE1::SetPersistedRegistrations</span></span>

<span data-ttu-id="7ba83-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7ba83-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7ba83-105">Регистрирует файлы личных папок (PST) для автоматического разблокирование Предотвращение дальнейшие вызовы HrTrustedPSTOverrideHandlerCallback.</span><span class="sxs-lookup"><span data-stu-id="7ba83-105">Registers Personal Folders (.pst) files for automatic unlocking, avoiding further calls to the HrTrustedPSTOverrideHandlerCallback.</span></span>
  
```cpp
HRESULT SetPersistedRegistrations(
  SPropValue *pmval
);
```

## <a name="parameters"></a><span data-ttu-id="7ba83-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7ba83-106">Parameters</span></span>

<span data-ttu-id="7ba83-107">_pmval_</span><span class="sxs-lookup"><span data-stu-id="7ba83-107">_pmval_</span></span>
  
> <span data-ttu-id="7ba83-108">[in] Структура [SPropValue](spropvalue.md) , содержащая указатель на путь библиотеки динамической компоновки (DLL) для регистрации.</span><span class="sxs-lookup"><span data-stu-id="7ba83-108">[in] An [SPropValue](spropvalue.md) structure that contains a pointer to the path of the dynamic-link library (DLL) to register.</span></span> <span data-ttu-id="7ba83-109">Структура имеет следующие характеристики:</span><span class="sxs-lookup"><span data-stu-id="7ba83-109">The structure has the following characteristics:</span></span> 
    
   - <span data-ttu-id="7ba83-110">UlPropTag [PROP_TAG](prop_tag.md)(PT_MV_UNICODE, PROP_ID_NULL).</span><span class="sxs-lookup"><span data-stu-id="7ba83-110">A ulPropTag of [PROP_TAG](prop_tag.md)(PT_MV_UNICODE, PROP_ID_NULL).</span></span>
    
   - <span data-ttu-id="7ba83-111">Свойство value MVszW, заданный в массив строк символ Unicode символом null.</span><span class="sxs-lookup"><span data-stu-id="7ba83-111">An MVszW value property that is set to an array of null-terminated Unicode character strings.</span></span> <span data-ttu-id="7ba83-112">Дополнительные сведения см в разделе [SWStringArray](swstringarray.md) .</span><span class="sxs-lookup"><span data-stu-id="7ba83-112">For more information see the [SWStringArray](swstringarray.md) topic.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="7ba83-113">SPropValue хранится в свойстве MAPI в диапазоне внутренних PST-файлов.</span><span class="sxs-lookup"><span data-stu-id="7ba83-113">The SPropValue is stored in a MAPI property in the PST's internal range.</span></span> <span data-ttu-id="7ba83-114">Это свойство недоступно для обычных приложений MAPI.</span><span class="sxs-lookup"><span data-stu-id="7ba83-114">This property is inaccessible to ordinary MAPI applications.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="7ba83-115">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="7ba83-115">Return value</span></span>

<span data-ttu-id="7ba83-116">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="7ba83-116">S_OK</span></span> 
  
> <span data-ttu-id="7ba83-117">Вызов функции прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="7ba83-117">The function call was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7ba83-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="7ba83-118">Remarks</span></span>

<span data-ttu-id="7ba83-119">Постоянные регистраций может отрицательно сказаться на производительности приложения, такие как Outlook и Windows Desktop Search, откройте PST-файлов.</span><span class="sxs-lookup"><span data-stu-id="7ba83-119">Persisted registrations may adversely affect the performance of applications, such as Outlook and Windows Desktop Search, that open PSTs.</span></span> <span data-ttu-id="7ba83-120">Рассмотрите возможность влияют на производительность при использовании или расширении использования постоянных регистрации.</span><span class="sxs-lookup"><span data-stu-id="7ba83-120">Consider the performance effect when using or expanding the usage of persisted registrations.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="7ba83-121">Этот метод реализован только для кодировки Юникод.</span><span class="sxs-lookup"><span data-stu-id="7ba83-121">This method is implemented for Unicode only.</span></span> <span data-ttu-id="7ba83-122">Более того он будет заблаговременно ошибкой, если какие-либо из следующих путей в массиве имеет расширение имени файла из библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="7ba83-122">Further, it will preemptively fail if any of the paths in the array do not have a file name extension of .dll.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7ba83-123">См. также</span><span class="sxs-lookup"><span data-stu-id="7ba83-123">See also</span></span>

- [<span data-ttu-id="7ba83-124">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7ba83-124">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md) 
- [<span data-ttu-id="7ba83-125">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7ba83-125">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

