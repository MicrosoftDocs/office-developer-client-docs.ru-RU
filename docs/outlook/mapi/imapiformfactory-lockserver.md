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
ms.openlocfilehash: c33fea8a2aba875fcdc06dea3343add4b7ac5dde
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808899"
---
# <a name="imapiformfactorylockserver"></a><span data-ttu-id="0f648-103">IMAPIFormFactory::LockServer</span><span class="sxs-lookup"><span data-stu-id="0f648-103">IMAPIFormFactory::LockServer</span></span>

  
  
<span data-ttu-id="0f648-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0f648-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0f648-105">Сохраняет это сервер открытой формы в памяти.</span><span class="sxs-lookup"><span data-stu-id="0f648-105">Keeps an open form server in memory.</span></span>
  
```cpp
HRESULT LockServer(
  ULONG ulFlags,
  ULONG fLockServer
);
```

## <a name="parameters"></a><span data-ttu-id="0f648-106">���������</span><span class="sxs-lookup"><span data-stu-id="0f648-106">Parameters</span></span>

 <span data-ttu-id="0f648-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0f648-107">_ulFlags_</span></span>
  
> <span data-ttu-id="0f648-108">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="0f648-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="0f648-109">_fLockServer_</span><span class="sxs-lookup"><span data-stu-id="0f648-109">_fLockServer_</span></span>
  
> <span data-ttu-id="0f648-110">[in] **значение true** для увеличения значения счетчика блокировок; в противном случае — **false**.</span><span class="sxs-lookup"><span data-stu-id="0f648-110">[in] **true** to increment the lock count; otherwise, **false**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0f648-111">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="0f648-111">Return value</span></span>

<span data-ttu-id="0f648-112">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="0f648-112">S_OK</span></span> 
  
> <span data-ttu-id="0f648-113">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="0f648-113">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0f648-114">���������</span><span class="sxs-lookup"><span data-stu-id="0f648-114">Remarks</span></span>

<span data-ttu-id="0f648-115">Средства просмотра форм вызовите метод **IMAPIFormFactory::LockServer** для хранения приложения сервера открытой формы в памяти.</span><span class="sxs-lookup"><span data-stu-id="0f648-115">Form viewers call the **IMAPIFormFactory::LockServer** method to keep an open form server application in memory.</span></span> <span data-ttu-id="0f648-116">Поддержание сервера форм в памяти повышает эффективность своей работы, когда часто создаются и выпущен форм.</span><span class="sxs-lookup"><span data-stu-id="0f648-116">Keeping the form server in memory improves its performance when forms are frequently created and released.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="0f648-117">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="0f648-117">Notes to implementers</span></span>

<span data-ttu-id="0f648-118">Метод **IMAPIFormFactory::LockServer** очень похож на метод [IClassFactory::LockServer](http://msdn.microsoft.com/en-us/library/ms682332%28v=VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="0f648-118">The **IMAPIFormFactory::LockServer** method is very similar to the [IClassFactory::LockServer](http://msdn.microsoft.com/en-us/library/ms682332%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="0f648-119">В сущности метод **IMAPIFormFactory::LockServer** поддерживает вызова число сколько раз; Поскольку это число больше 0, метод предотвращает выгрузки из памяти сервера форм.</span><span class="sxs-lookup"><span data-stu-id="0f648-119">Essentially, the **IMAPIFormFactory::LockServer** method maintains a count of how many times it has been called; as long as that count is greater than 0, the method prevents the form server from being unloaded from memory.</span></span> <span data-ttu-id="0f648-120">Чтобы реализовать ее можно использовать функцию [CoLockObjectExternal](http://msdn.microsoft.com/en-us/library/ms680592%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="0f648-120">You can use the [CoLockObjectExternal](http://msdn.microsoft.com/en-us/library/ms680592%28VS.85%29.aspx) function to implement this.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0f648-121">См. также</span><span class="sxs-lookup"><span data-stu-id="0f648-121">See also</span></span>



[<span data-ttu-id="0f648-122">IMAPIFormFactory : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0f648-122">IMAPIFormFactory : IUnknown</span></span>](imapiformfactoryiunknown.md)

