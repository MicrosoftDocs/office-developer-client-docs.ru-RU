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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389059"
---
# <a name="imapiformfactorylockserver"></a><span data-ttu-id="f8133-103">IMAPIFormFactory::LockServer</span><span class="sxs-lookup"><span data-stu-id="f8133-103">IMAPIFormFactory::LockServer</span></span>

  
  
<span data-ttu-id="f8133-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f8133-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f8133-105">Сохраняет это сервер открытой формы в памяти.</span><span class="sxs-lookup"><span data-stu-id="f8133-105">Keeps an open form server in memory.</span></span>
  
```cpp
HRESULT LockServer(
  ULONG ulFlags,
  ULONG fLockServer
);
```

## <a name="parameters"></a><span data-ttu-id="f8133-106">���������</span><span class="sxs-lookup"><span data-stu-id="f8133-106">Parameters</span></span>

 <span data-ttu-id="f8133-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f8133-107">_ulFlags_</span></span>
  
> <span data-ttu-id="f8133-108">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="f8133-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="f8133-109">_fLockServer_</span><span class="sxs-lookup"><span data-stu-id="f8133-109">_fLockServer_</span></span>
  
> <span data-ttu-id="f8133-110">[in] **значение true** для увеличения значения счетчика блокировок; в противном случае — **false**.</span><span class="sxs-lookup"><span data-stu-id="f8133-110">[in] **true** to increment the lock count; otherwise, **false**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f8133-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f8133-111">Return value</span></span>

<span data-ttu-id="f8133-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="f8133-112">S_OK</span></span> 
  
> <span data-ttu-id="f8133-113">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="f8133-113">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f8133-114">���������</span><span class="sxs-lookup"><span data-stu-id="f8133-114">Remarks</span></span>

<span data-ttu-id="f8133-115">Средства просмотра форм вызовите метод **IMAPIFormFactory::LockServer** для хранения приложения сервера открытой формы в памяти.</span><span class="sxs-lookup"><span data-stu-id="f8133-115">Form viewers call the **IMAPIFormFactory::LockServer** method to keep an open form server application in memory.</span></span> <span data-ttu-id="f8133-116">Поддержание сервера форм в памяти повышает эффективность своей работы, когда часто создаются и выпущен форм.</span><span class="sxs-lookup"><span data-stu-id="f8133-116">Keeping the form server in memory improves its performance when forms are frequently created and released.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="f8133-117">Примечания для реализующих</span><span class="sxs-lookup"><span data-stu-id="f8133-117">Notes to implementers</span></span>

<span data-ttu-id="f8133-118">Метод **IMAPIFormFactory::LockServer** очень похож на метод [IClassFactory::LockServer](https://msdn.microsoft.com/library/ms682332%28v=VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f8133-118">The **IMAPIFormFactory::LockServer** method is very similar to the [IClassFactory::LockServer](https://msdn.microsoft.com/library/ms682332%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="f8133-119">В сущности метод **IMAPIFormFactory::LockServer** поддерживает вызова число сколько раз; Поскольку это число больше 0, метод предотвращает выгрузки из памяти сервера форм.</span><span class="sxs-lookup"><span data-stu-id="f8133-119">Essentially, the **IMAPIFormFactory::LockServer** method maintains a count of how many times it has been called; as long as that count is greater than 0, the method prevents the form server from being unloaded from memory.</span></span> <span data-ttu-id="f8133-120">Чтобы реализовать ее можно использовать функцию [CoLockObjectExternal](https://msdn.microsoft.com/library/ms680592%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f8133-120">You can use the [CoLockObjectExternal](https://msdn.microsoft.com/library/ms680592%28VS.85%29.aspx) function to implement this.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f8133-121">См. также</span><span class="sxs-lookup"><span data-stu-id="f8133-121">See also</span></span>



[<span data-ttu-id="f8133-122">IMAPIFormFactory : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f8133-122">IMAPIFormFactory : IUnknown</span></span>](imapiformfactoryiunknown.md)

