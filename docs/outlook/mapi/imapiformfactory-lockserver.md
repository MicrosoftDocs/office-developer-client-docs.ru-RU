---
title: IMAPIFormFactoryLockServer
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormFactory.LockServer
api_type:
- COM
ms.assetid: b9bd389a-6975-41a2-a2f4-e501312e434b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: ab51b939651bc3c121f357545969d26832a19d19
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342142"
---
# <a name="imapiformfactorylockserver"></a><span data-ttu-id="0ecd7-103">IMAPIFormFactory::LockServer</span><span class="sxs-lookup"><span data-stu-id="0ecd7-103">IMAPIFormFactory::LockServer</span></span>

  
  
<span data-ttu-id="0ecd7-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0ecd7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0ecd7-105">Сохраняет открытый сервер формы в памяти.</span><span class="sxs-lookup"><span data-stu-id="0ecd7-105">Keeps an open form server in memory.</span></span>
  
```cpp
HRESULT LockServer(
  ULONG ulFlags,
  ULONG fLockServer
);
```

## <a name="parameters"></a><span data-ttu-id="0ecd7-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="0ecd7-106">Parameters</span></span>

 <span data-ttu-id="0ecd7-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0ecd7-107">_ulFlags_</span></span>
  
> <span data-ttu-id="0ecd7-108">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="0ecd7-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="0ecd7-109">_fLockServer_</span><span class="sxs-lookup"><span data-stu-id="0ecd7-109">_fLockServer_</span></span>
  
> <span data-ttu-id="0ecd7-110">[in] **верно** для приумно-ления счета блокировки; в противном **случае, false**.</span><span class="sxs-lookup"><span data-stu-id="0ecd7-110">[in] **true** to increment the lock count; otherwise, **false**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0ecd7-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0ecd7-111">Return value</span></span>

<span data-ttu-id="0ecd7-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="0ecd7-112">S_OK</span></span> 
  
> <span data-ttu-id="0ecd7-113">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="0ecd7-113">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0ecd7-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="0ecd7-114">Remarks</span></span>

<span data-ttu-id="0ecd7-115">Зрители форм называют **метод IMAPIFormFactory::LockServer** для сохраняемого приложения сервера формы в памяти.</span><span class="sxs-lookup"><span data-stu-id="0ecd7-115">Form viewers call the **IMAPIFormFactory::LockServer** method to keep an open form server application in memory.</span></span> <span data-ttu-id="0ecd7-116">Сохранение сервера форм в памяти повышает его производительность, когда формы часто создаются и выпускаются.</span><span class="sxs-lookup"><span data-stu-id="0ecd7-116">Keeping the form server in memory improves its performance when forms are frequently created and released.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="0ecd7-117">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="0ecd7-117">Notes to implementers</span></span>

<span data-ttu-id="0ecd7-118">Метод **IMAPIFormFactory::LockServer** очень похож на [метод IClassFactory::LockServer.](https://msdn.microsoft.com/library/ms682332%28v=VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0ecd7-118">The **IMAPIFormFactory::LockServer** method is very similar to the [IClassFactory::LockServer](https://msdn.microsoft.com/library/ms682332%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="0ecd7-119">По сути, метод **IMAPIFormFactory::LockServer** поддерживает подсчет, сколько раз он был вызван; до тех пор, пока это количество превышает 0, метод предотвращает выгрузку сервера форм из памяти.</span><span class="sxs-lookup"><span data-stu-id="0ecd7-119">Essentially, the **IMAPIFormFactory::LockServer** method maintains a count of how many times it has been called; as long as that count is greater than 0, the method prevents the form server from being unloaded from memory.</span></span> <span data-ttu-id="0ecd7-120">Для реализации этой функции можно использовать функцию [CoLockObjectExternal.](https://msdn.microsoft.com/library/ms680592%28VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0ecd7-120">You can use the [CoLockObjectExternal](https://msdn.microsoft.com/library/ms680592%28VS.85%29.aspx) function to implement this.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0ecd7-121">См. также</span><span class="sxs-lookup"><span data-stu-id="0ecd7-121">See also</span></span>



[<span data-ttu-id="0ecd7-122">IMAPIFormFactory : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0ecd7-122">IMAPIFormFactory : IUnknown</span></span>](imapiformfactoryiunknown.md)

